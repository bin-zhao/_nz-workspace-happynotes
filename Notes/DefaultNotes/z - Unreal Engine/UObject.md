
> TODO(zz) 把UObject构造和UObject反射严格划分开。

---

UObject对象构造过程

```c++
template< class T >
T* NewObject(
	UObject* Outer, 
	FName Name, 
	EObjectFlags Flags = RF_NoFlags, 
	UObject* Template = nullptr, 
	bool bCopyTransientsFromClassDefaults = false, 
	FObjectInstancingGraph* InInstanceGraph = nullptr)
{
	FStaticConstructObjectParameters Params(T::StaticClass());
	Params.Outer = Outer;
	Params.Name = Name;
	Params.SetFlags = Flags;
	Params.Template = Template;
	Params.bCopyTransientsFromClassDefaults = bCopyTransientsFromClassDefaults;
	Params.InstanceGraph = InInstanceGraph;

	// 完成C++构造的UObject子类对象。
	return static_cast<T*>(StaticConstructObject_Internal(Params));
}


UObject* StaticConstructObject_Internal(
	const FStaticConstructObjectParameters& Params
)
{
	UObject* Result = NULL;

	Result = StaticAllocateObject(
		InClass, 
		InOuter, 
		InName, 
		InFlags, 
		Params.InternalSetFlags, 
		bCanRecycleSubobjects, 
		&bRecycledSubobject, 
		Params.ExternalPackage);

    check(Result != nullptr);

	// 递归构造。
	// 这里的构造函数是真正的UObject子类的构造函数。
		// TODO(zz) 要完全确认。
	(*InClass->ClassConstructor)(FObjectInitializer(Result, Params));

	return Result;
}


// 对象是类在内存块上的表达。
// 这里获取的指针是UObject，但是，仍然只构造了UObjectBase。这个很值得思考：
// 可以看作是内存块上的“半对象”。但是，拥有父类一层后，子类就可以安全初始化了。
// 从这里看，继承只是个初始化规则。
UObject* StaticAllocateObject(
    const UClass*   InClass,
    UObject*        InOuter,
    FName           InName,
    EObjectFlags    InFlags,
    EInternalObjectFlags InternalSetFlags,
    bool bCanRecycleSubobjects,
    bool* bOutRecycledSubobject,
    UPackage* ExternalPackage
)
{
	UObject* Obj = NULL;
	// 对象内存大小携带在反射类里。
	int32 TotalSize = InClass->GetPropertiesSize();

	if( Obj == nullptr )
    {
		int32 Alignment = FMath::Max( 4, InClass->GetMinAlignment() );

		Obj = (UObject *)GUObjectAllocator.AllocateUObject(
			TotalSize,
			Alignment,
			GIsInitialLoad);
	}

	// 内存清零。
	FMemory::Memzero((void *)Obj, TotalSize);

	// 构造第一层：UObjectBase。
	new ((void *)Obj) UObjectBase(
		const_cast<UClass*>(InClass),
		InFlags|RF_NeedInitialization,
		InternalSetFlags,
		InOuter,
		InName);

	return Obj;
}


// 分配内存。
UObjectBase* FUObjectAllocator::AllocateUObject(
	int32 Size, 
	int32 Alignment, 
	bool bAllowPermanent
)
{
	UObjectBase* Result = nullptr;

	// 为内存块赋予类型。
	Result = (UObjectBase*)FMemory::Malloc( Size, Alignment );
	
	return Result;
}
```

```c++
class COREUOBJECT_API UObject
	: public UObjectBaseUtility
{
public:
	inline void* operator new(
		const size_t InSize,
		EInternal InInternalOnly,
		UObject* InOuter = (UObject*)GetTransientPackage(),
		FName InName = NAME_None,
		EObjectFlags InSetFlags = RF_NoFlags
	)
	{
		return StaticAllocateObject(
			StaticClass(),
			InOuter,
			InName,
			InSetFlags);
    }
};
```

---

Cast

> UObject -> Interface并没有想的那么好。Cast模板只认UObject的指针，UObject子类指针不认。这个非常蠢。要转为Interface指针，需要先转成UObject*。而且，这和C++的语义不一致。如果是子类实现的Interface，父类确实取不回来，而UObject体系通过这个方式做到了。

```c++
// 取回的是无类型的指针。
void* UObjectBaseUtility::GetInterfaceAddress( UClass* InterfaceClass )
{
	void* Result = NULL;

	if ( !InterfaceClass->HasAnyClassFlags(CLASS_Native) )
	{
		if ( GetClass()->ImplementsInterface(InterfaceClass) )
		{
			Result = this;
		}
	}
	else
	{
		for( UClass* CurrentClass=GetClass(); 
			Result == NULL && CurrentClass != NULL; 
			CurrentClass = CurrentClass->GetSuperClass() )
		{
			for (TArray<FImplementedInterface>::TIterator It(
				CurrentClass->Interfaces); 
				It; 
				++It)
			{
				FImplementedInterface& ImplInterface = *It;
				if ( !ImplInterface.bImplementedByK2 && 
					ImplInterface.Class->IsChildOf(InterfaceClass) )
				{
					// Interface指针在对象内存中的位置。
					// 如果没有额外的成员变量定义，会和对象指针重合。
						// C++中的Interface实现本质上是多重继承。
					Result = (uint8*)this + It->PointerOffset;
					break;
				}
			}
		}
	}

    return Result;
}


template <typename From, typename To>
struct TCastImpl<From, To, ECastType::UObjectToInterface>
{
	FORCEINLINE static To* DoCast( UObject* Src )
	{
		return Src ? 
		// 强制转化成目标类型。
		(To*)Src->GetInterfaceAddress(To::UClassType::StaticClass()) 
		: 
		nullptr;
	}
}


template <typename To, typename From>
FORCEINLINE To* Cast(From* Src)
{
	return TCastImpl<From, To>::DoCast(Src);
}
```


---

