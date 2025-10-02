
---

# nLabtopos

|  [Home Page](https://ncatlab.org/nlab/show/HomePage "Home page") | [All Pages](https://ncatlab.org/nlab/all_pages "List of all pages") | [Latest Revisions](https://ncatlab.org/nlab/latest_revisions "Latest edits and page creations") | [Discuss this page](https://nforum.ncatlab.org/discussion/189/#Item_37 "Discuss this page in its dedicated thread on the nForum") | 

### Context

#### Topos Theory

#### Category Theory

# Contents

- [1. Idea](https://ncatlab.org/nlab/show/topos#Idea)

- [‘What a topos is like:’](https://ncatlab.org/nlab/show/topos#what_a_topos_is_like)

- [2. Definitions](https://ncatlab.org/nlab/show/topos#definitions)

- [Elementary toposes](https://ncatlab.org/nlab/show/topos#ElementaryTopos)
- [Grothendieck/sheaf toposes](https://ncatlab.org/nlab/show/topos#SheafToposes)
- [W-toposes](https://ncatlab.org/nlab/show/topos#WToposes)
- [Toposes over a base](https://ncatlab.org/nlab/show/topos#toposes_over_a_base)
- [Morphisms of toposes](https://ncatlab.org/nlab/show/topos#morphisms_of_toposes)

- [3. Properties](https://ncatlab.org/nlab/show/topos#properties)

- [Extensivity](https://ncatlab.org/nlab/show/topos#extensivity)
- [Adhesiveness](https://ncatlab.org/nlab/show/topos#adhesiveness)
- [Epimorphisms](https://ncatlab.org/nlab/show/topos#epimorphisms)
- [Relation to abelian categories](https://ncatlab.org/nlab/show/topos#relation_to_abelian_categories)
- [Reasoning in a topos](https://ncatlab.org/nlab/show/topos#reasoning_in_a_topos)

- [4. Examples](https://ncatlab.org/nlab/show/topos#Examples)

- [Specific examples and key results](https://ncatlab.org/nlab/show/topos#specific_examples_and_key_results)
- [Classes of examples](https://ncatlab.org/nlab/show/topos#classes_of_examples)

- [5. Related concepts](https://ncatlab.org/nlab/show/topos#related_concepts)
- [6. References](https://ncatlab.org/nlab/show/topos#References)

- [Introductions](https://ncatlab.org/nlab/show/topos#Introductions)
- [Monographs](https://ncatlab.org/nlab/show/topos#ReferencesMonographs)
- [Classifying toposes](https://ncatlab.org/nlab/show/topos#classifying_toposes)
- [Categorical logic and elementary toposes](https://ncatlab.org/nlab/show/topos#CategoricalLogicAndElementaryToposes)
- [Algebra, ringed toposes, algebraic geometry](https://ncatlab.org/nlab/show/topos#algebra_ringed_toposes_algebraic_geometry)
- [Quantum theory](https://ncatlab.org/nlab/show/topos#quantum_theory)
- [Original articles](https://ncatlab.org/nlab/show/topos#original_articles)
- [History](https://ncatlab.org/nlab/show/topos#history)
- [General theory](https://ncatlab.org/nlab/show/topos#general_theory)

## 1. Idea

There are various different perspectives on the notion of _topos_. One is that a topos is a [category](https://ncatlab.org/nlab/show/category) that looks like a category of [space](https://ncatlab.org/nlab/show/space)s that sit by [local homeomorphisms](https://ncatlab.org/nlab/show/local+homeomorphisms) over a given base [space](https://ncatlab.org/nlab/show/space): all spaces that are _locally modeled on_ a given base space.

The archetypical class of examples are [sheaf topos](https://ncatlab.org/nlab/show/sheaf+topos)es Sh(X)=Et(X) over a [topological space](https://ncatlab.org/nlab/show/topological+space) X: these are the categories of [étale space](https://ncatlab.org/nlab/show/%C3%A9tale+space)s over X, topological spaces Y that are equipped with a [local homeomorphisms](https://ncatlab.org/nlab/show/local+homeomorphisms) Y→X.

When X=* is the [point](https://ncatlab.org/nlab/show/point), this is just the category [Set](https://ncatlab.org/nlab/show/Set) of all [sets](https://ncatlab.org/nlab/show/sets): spaces that are _modeled on the point_. This is the archetypical topos itself.

What makes the notion of topos powerful is the following fact: even though the general topos contains objects that are considerably different from and possibly considerably richer than plain sets and even richer than étale spaces over a topological space, the general abstract [category theoretic](https://ncatlab.org/nlab/show/category+theory) properties of every topos are essentially the same as those of [Set](https://ncatlab.org/nlab/show/Set). For instance in every topos all small [limits](https://ncatlab.org/nlab/show/limits) and [colimits](https://ncatlab.org/nlab/show/colimits) exist and it is [cartesian closed](https://ncatlab.org/nlab/show/cartesian+closed+category) (even [locally](https://ncatlab.org/nlab/show/locally+cartesian+closed+category)). This means that a large number of constructions in [Set](https://ncatlab.org/nlab/show/Set) have immediate analogs [internal to](https://ncatlab.org/nlab/show/internalization) every topos, and the analogs of the statements about these constructions that are true in Set are true in _every_ topos.

On the one hand this may be thought of as saying that toposes are _very nice categories of spaces_ in that whatever construction on spaces one thinks of – for instance formation of [quotient](https://ncatlab.org/nlab/show/quotient)s or of [fiber product](https://ncatlab.org/nlab/show/fiber+product)s or of [mapping space](https://ncatlab.org/nlab/show/mapping+space)s – the resulting space with the expected general abstract properties will exist in the topos. In this sense toposes are _convenient categories_ for geometry – as in: [convenient category of topological spaces](https://ncatlab.org/nlab/show/convenient+category+of+topological+spaces), but even more convenient than that.

On the other hand, by de-emphasizing the geometric interpretation of their objects and just using their good abstract properties, this means that toposes are contexts with a powerful [internal logic](https://ncatlab.org/nlab/show/internal+logic). The internal logic of toposes is [intuitionistic](https://ncatlab.org/nlab/show/intuitionistic+logic) [higher order logic](https://ncatlab.org/nlab/show/higher+order+logic). This means that, while the [law of excluded middle](https://ncatlab.org/nlab/show/law+of+excluded+middle) and the [axiom of choice](https://ncatlab.org/nlab/show/axiom+of+choice) may fail, apart from that, every logical statement not depending on these does hold [internal to](https://ncatlab.org/nlab/show/internalization) _every_ topos.

For this reason toposes are often studied as abstract contexts “in which one can do mathematics”, independently of their interpretation as categories of spaces. These two points of views on toposes, as being about geometry and about logic at the same time, is part of the richness of topos theory.

On a third hand, however, we can de-emphasize the role of the objects of the topos and instead treat the topos itself as a “generalized space” (and in particular, a [categorified](https://ncatlab.org/nlab/show/vertical+categorification) space). We then consider the topos Sh(X) as a representative of X itself, while toposes not of this form are “honestly generalized” spaces. This point of view is supported by the fact that the assignment X↦Sh(X) is a full embedding of (sufficiently nice) topological spaces into toposes, and that many topological properties of a space X can be detected at the level of Sh(X). (This is even more true once we pass to [(∞,1)-toposes](https://ncatlab.org/nlab/show/%28%E2%88%9E%2C1%29-toposes).)

From this point of view, the objects of a topos (regarded as a category) should be thought of instead as _sheaves on_ that topos (regarded as a generalized space). And just as sheaves on a topological space can be identified with local homeomorphisms over it, such “sheaves on a topos” (i.e. objects of the topos _qua_ category) can be identified with other _toposes_ that sit over the given topos via a [local homeomorphism of toposes](https://ncatlab.org/nlab/show/%C3%A9tale+geometric+morphism).

Finally, mixing this point of view with the second one, we can regard toposes over a given topos E instead as “toposes in the E-world of mathematics.” For this reason, the theory of toposes over a given base is formally quite similar to that of arbitrary toposes. And coming full circle, this fact allows the use of “base change arguments” as a very useful technical tool, even if our interest is only in one or two particular toposes _qua_ categories.

### ‘<span style="color:rgb(255, 0, 0)">What a topos is like:</span>’

(i) ‘A topos is a category of sheaves on a site’

(ii) ‘A topos is a category with finite limits and power-objects’

(iii) ‘A topos is (the embodiment of) an intuitionistic higher-order theory’

(iv) ‘A topos is (the extensional essence of) a first-order (infinitary) geometric theory’

(v) ‘A topos is a [totally cocomplete](https://ncatlab.org/nlab/show/total+category) object in the meta-2-category CART of cartesian (i.e. , finitely complete) categories’

(vi) ‘A topos is a generalized space’

(vii) ‘A topos is a semantics for intuitionistic formal systems’

(viii) ‘A topos is a Morita equivalence class of continuous groupoids’

(ix) ‘A topos is the category of maps of a power allegory’

(x) ‘A topos is a category whose canonical indexing over itself is complete and well-powered’

(xi) ‘A topos is the spatial manifestation of a giraud frame’

(xii) ‘A topos is a setting for synthetic differential geometry’

(xiii) ‘A topos is a setting for synthetic domain theory’,

And so on. But the important thing about the elephant is that ‘however you approach it, it is still the same animal’. [Elephant](https://ncatlab.org/nlab/show/Elephant)

## 2. Definitions

The general notion of _topos_ is that of

- [Elementary toposes](https://ncatlab.org/nlab/show/topos#ElementaryTopos).

A specialization of this which is important enough that much of the literature implicitly takes it to be the general definition is the notion of

- [Grothendieck/sheaf toposes](https://ncatlab.org/nlab/show/topos#SheafToposes)

This is the notion relevant for applications in [geometry](https://ncatlab.org/nlab/show/geometry) and [geometric logic](https://ncatlab.org/nlab/show/geometric+logic), whereas the notion of elementary toposes is relevant for more general applications in [logic](https://ncatlab.org/nlab/show/logic).

For standard notions of mathematics to be available [inside](https://ncatlab.org/nlab/show/internal+logic) a given topos one typically at least needs a [natural numbers object](https://ncatlab.org/nlab/show/natural+numbers+object). Its existence is guaranteed by the axioms of a sheaf topos, but not by the more general axioms of an elementary topos. Adding the existence of a natural numbers object to the axioms of an elementary topos yields the notion of a

- [W-topos](https://ncatlab.org/nlab/show/topos#WToposes).

### Elementary toposes

A quick formal definition is that an **elementary topos** is a [category](https://ncatlab.org/nlab/show/category) which

1. has [finite limits](https://ncatlab.org/nlab/show/finitely+complete+category),
    
2. is [cartesian closed](https://ncatlab.org/nlab/show/cartesian+closed+category), and
    
3. has a [subobject classifier](https://ncatlab.org/nlab/show/subobject+classifier).
    

There are alternative ways to state the definition; for instance,

1. has [finite limit](https://ncatlab.org/nlab/show/finite+limit)s and
2. has [power objects](https://ncatlab.org/nlab/show/power+objects).

In a way, however, these concise definitions can be misleading, because a topos has a great deal of other structure, which plays a very important role but just happens to follow automatically from these basic axioms. Most importantly, an elementary topos is all of the following:

- [locally cartesian closed](https://ncatlab.org/nlab/show/locally+cartesian+closed+category),
- [finitely cocomplete](https://ncatlab.org/nlab/show/finitely+cocomplete+category),
- a [Heyting category](https://ncatlab.org/nlab/show/Heyting+category),
- a [pretopos](https://ncatlab.org/nlab/show/pretopos).

The last two imply that it has an [internal logic](https://ncatlab.org/nlab/show/internal+logic) that resembles ordinary mathematical reasoning, and the presence of exponentials and power objects means that this logic is [higher order](https://ncatlab.org/nlab/show/higher+order+logic).

### <span style="color:rgb(255, 0, 0)">Grothendieck/sheaf toposes</span>

The above is the definition of an _elementary_ topos. We also have the (historically earlier) notion of [Grothendieck topos](https://ncatlab.org/nlab/show/Grothendieck+topos): a **Grothendieck topos** is a topos that is neither too small nor too large, in that it is:

- [cocomplete](https://ncatlab.org/nlab/show/cocomplete+category) (not too small), and
- has a [small](https://ncatlab.org/nlab/show/small+set) [generating set](https://ncatlab.org/nlab/show/generating+set) (not too large).

Equivalently, a Grothendieck topos is any category [equivalent](https://ncatlab.org/nlab/show/equivalence+of+categories) to the [category of sheaves](https://ncatlab.org/nlab/show/category+of+sheaves) on some [small](https://ncatlab.org/nlab/show/small+category) [site](https://ncatlab.org/nlab/show/site).

### W-toposes

There is a further elementary property of [Set](https://ncatlab.org/nlab/show/Set) that might have gone into the definition of elementary topos but historically did not: the existence of a [natural numbers object](https://ncatlab.org/nlab/show/natural+numbers+object). Any topos with this property is called a **topos with NNO** or a **W-topos**. The latter term comes from the result that any such topos must have (not only an NNO but also) all [W-types](https://ncatlab.org/nlab/show/W-types).

### Toposes over a base

- [base topos](https://ncatlab.org/nlab/show/base+topos)

### Morphisms of toposes

There are two kinds of [homomorphisms](https://ncatlab.org/nlab/show/homomorphisms) between toposes that one considers:

- [geometric morphism](https://ncatlab.org/nlab/show/geometric+morphism)– this is the kind of morphism that regards a topos as a generalized [topological space](https://ncatlab.org/nlab/show/topological+space).
    
- [logical morphism](https://ncatlab.org/nlab/show/logical+morphism)– this is the kind of morphism that regards a topos in terms of its [internal logic](https://ncatlab.org/nlab/show/internal+logic).
    

Accordingly there is a [2-category](https://ncatlab.org/nlab/show/2-category) [Topos](https://ncatlab.org/nlab/show/Topos) of toposes, whose

- [object](https://ncatlab.org/nlab/show/object)s are toposes;
    
- [morphism](https://ncatlab.org/nlab/show/morphism)s are [geometric morphism](https://ncatlab.org/nlab/show/geometric+morphism)s;
    
- [2-morphism](https://ncatlab.org/nlab/show/2-morphism)s are [natural transformation](https://ncatlab.org/nlab/show/natural+transformation)s between the [functor](https://ncatlab.org/nlab/show/functor)s underlying the geometric morphisms.
    

## 3. Properties

### Extensivity

Every topos is an [extensive category](https://ncatlab.org/nlab/show/extensive+category). For [Grothendieck toposes](https://ncatlab.org/nlab/show/Grothendieck+toposes), infinitary extensivity is part of the characterizing [Giraud's theorem](https://ncatlab.org/nlab/show/Giraud%27s+theorem). For elementary toposes, see [toposes are extensive](https://ncatlab.org/nlab/show/toposes+are+extensive).

### Adhesiveness

Every topos is an [adhesive category](https://ncatlab.org/nlab/show/adhesive+category). For [Grothendieck toposes](https://ncatlab.org/nlab/show/Grothendieck+toposes) this follows immediately from the adhesion of [Set](https://ncatlab.org/nlab/show/Set), for elementary toposes it is due to ([Lack-Sobocinski](https://ncatlab.org/nlab/show/topos#LackSobocinski)).

### Epimorphisms

In a topos [epimorphism](https://ncatlab.org/nlab/show/epimorphism)s are stable under [pullback](https://ncatlab.org/nlab/show/pullback) and hence the [(epi, mono) factorization system](https://ncatlab.org/nlab/show/%28epi%2C+mono%29+factorization+system) in a topos is a [stable factorization system](https://ncatlab.org/nlab/show/stable+factorization+system).

### Relation to <span style="color:rgb(255, 0, 0)">abelian categories</span>

While crucially different from [abelian categories](https://ncatlab.org/nlab/show/abelian+categories), there is some intimate relation between toposes and abelian categories. For more on that see [AT category](https://ncatlab.org/nlab/show/AT+category).

### Reasoning in a topos

Any result in [ordinary mathematics](https://ncatlab.org/nlab/show/ordinary+mathematics) whose proof is [finitist](https://ncatlab.org/nlab/show/finite+mathematics) and [constructive](https://ncatlab.org/nlab/show/constructive+mathematics) automatically holds in any topos. If you remove the restriction that the proof be finitist, then the result holds in any topos with a [natural numbers object](https://ncatlab.org/nlab/show/natural+numbers+object); if you remove the restrictions that the proof be constructive, then the result holds in any [boolean topos](https://ncatlab.org/nlab/show/boolean+topos). On the other hand, if you add the restriction that the proof be predicative in the weaker sense used by constructivists, then the result may fail in some toposes but holds in any Π-[pretopos](https://ncatlab.org/nlab/show/Pi-pretopos); if you add the restriction that the proof be predicative in a stronger sense, then the result holds in any [Heyting pretopos](https://ncatlab.org/nlab/show/Heyting+pretopos).

Therefore, one can prove results in toposes and similar categories by reasoning, not about the [objects](https://ncatlab.org/nlab/show/objects) and [morphisms](https://ncatlab.org/nlab/show/morphisms) in the topos themselves, but instead about [sets](https://ncatlab.org/nlab/show/sets) and [functions](https://ncatlab.org/nlab/show/functions) in the normal language of structural [set theory](https://ncatlab.org/nlab/show/set+theory), which is more familiar to most mathematicians. One merely has to be careful about what axioms one uses to get results of sufficient generality.

The [internal language](https://ncatlab.org/nlab/show/internal+logic) of a topos is called [Mitchell-Bénabou language](https://ncatlab.org/nlab/show/Mitchell-B%C3%A9nabou+language).

## 4. Examples

### Specific examples and key results

- The archetypical topos is [Set](https://ncatlab.org/nlab/show/Set). Notice that this happens to be a [Grothendieck topos](https://ncatlab.org/nlab/show/Grothendieck+topos): it is the [category of sheaves](https://ncatlab.org/nlab/show/category+of+sheaves) on the [point](https://ncatlab.org/nlab/show/point).
    
    The [full subcategory](https://ncatlab.org/nlab/show/full+subcategory) [FinSet](https://ncatlab.org/nlab/show/FinSet) is also an elementary topos, and the inclusion functor FinSet↪Set is a [logical morphism](https://ncatlab.org/nlab/show/logical+morphism). This is not a Grothendieck topos.
    
    More generally, for κ a [strong limit cardinal](https://ncatlab.org/nlab/show/cardinal) the full subcategory Setκ of sets or [cardinality](https://ncatlab.org/nlab/show/cardinality) less than κ is a topos.
    
- For C any (small) [site](https://ncatlab.org/nlab/show/site), the [category of sheaves](https://ncatlab.org/nlab/show/category+of+sheaves) Sh(C) is a [Grothendieck topos](https://ncatlab.org/nlab/show/Grothendieck+topos). Either by definition or by [Giraud's theorem](https://ncatlab.org/nlab/show/Giraud%27s+theorem), every Grothendieck topos arises in this way. Important examples include:
    
    - The case where the [Grothendieck topology](https://ncatlab.org/nlab/show/Grothendieck+topology) is the trivial one, so that also all categories of [presheaves](https://ncatlab.org/nlab/show/presheaf) (on small categories) are (Grothendieck) toposes.
        
    - The case of sheaves on (the [site](https://ncatlab.org/nlab/show/site) given by the [category of open subsets](https://ncatlab.org/nlab/show/category+of+open+subsets) of) a [topological space](https://ncatlab.org/nlab/show/topological+space), or more generally a [locale](https://ncatlab.org/nlab/show/locale).
        
    - The category GSet of [set](https://ncatlab.org/nlab/show/set)s equipped with the [action](https://ncatlab.org/nlab/show/action) of a [group](https://ncatlab.org/nlab/show/group) G: this is the topos of presheaves on the category BG which is the [delooping](https://ncatlab.org/nlab/show/delooping) [groupoid](https://ncatlab.org/nlab/show/groupoid) of G.
        
- Continuing the last example above, if G is a topological group, the category GSet of [sets with a continuous action of G](https://ncatlab.org/nlab/show/category+of+G-sets) (that is, the action map G×X→X is [continuous](https://ncatlab.org/nlab/show/continuous+map), where X has the [discrete topology](https://ncatlab.org/nlab/show/discrete+topology)) is a topos, and in fact a Grothendieck topos (though this may not be obvious).
    
- More generally, G may be a [topological groupoid](https://ncatlab.org/nlab/show/topological+groupoid), or even a [localic groupoid](https://ncatlab.org/nlab/show/localic+groupoid). In fact, it is a theorem that every Grothendieck topos can be presented as the topos of “continuous sheaves” on a localic groupoid.
    
- Again if G is a topological group, the category Unif(G) of _[uniformly continuous](https://ncatlab.org/nlab/show/uniformly+continuous+map)_ G-sets is also a topos, but not (in general) one of Grothendieck’s. For example, if G is the [profinite completion](https://ncatlab.org/nlab/show/profinite+completion) of ℤ, then a continuous G-set is a ℤ-set all of whose orbits are finite, while a uniformly continuous one is a ℤ-set with a finite upper bound on the size of all its orbits.
    
- For E a topos and X∈E any [object](https://ncatlab.org/nlab/show/object), also the [overcategory](https://ncatlab.org/nlab/show/overcategory) or [slice category](https://ncatlab.org/nlab/show/slice+category) E/X is again a topos. ([Elephant](https://ncatlab.org/nlab/show/Elephant), A.2.3.2). See also [over-topos](https://ncatlab.org/nlab/show/over-topos).
    
- If E is a topos and j:E→E is a [lex](https://ncatlab.org/nlab/show/exact+functor) idempotent monad, the category of j-algebras is a topos. Each such j corresponds to a [Lawvere-Tierney topology](https://ncatlab.org/nlab/show/Lawvere-Tierney+topology) in E, and the category of j-algebras is equivalent to the category of sheaves for this topology. An example is the [double-negation topology](https://ncatlab.org/nlab/show/double+negation).
    
- An obvious example of an elementary topos that is not a Grothendieck topos is the category [FinSet](https://ncatlab.org/nlab/show/FinSet) of finite sets. More generally, for any [strong limit cardinal](https://ncatlab.org/nlab/show/strong+limit+cardinal) κ, the category of sets of cardinality <κ is an elementary topos, and as long as κ>ω it has a [NNO](https://ncatlab.org/nlab/show/NNO). Set<κ doesn’t even admit a geometric morphism to Set.
    
- Since the definition of elementary topos is “algebraic,” there exist [free topos](https://ncatlab.org/nlab/show/free+topos)es generated by various kinds of data. The category of toposes (and [logical functor](https://ncatlab.org/nlab/show/logical+functor)s) is [2-monadic](https://ncatlab.org/nlab/show/2-monadic) over the 2-category of categories, functors, and natural isomorphisms. It has an [initial object](https://ncatlab.org/nlab/show/initial+object) which is sometimes called _the free topos_. More generally, any [higher-order](https://ncatlab.org/nlab/show/higher-order+logic) [type theory](https://ncatlab.org/nlab/show/type+theory) (of the sort which can be interpreted in the [internal logic](https://ncatlab.org/nlab/show/internal+logic) of a topos) generates a free topos containing a model of that theory. Such toposes (for a consistent theory) are never Grothendieck’s.
    
- If G is a [large](https://ncatlab.org/nlab/show/large+category) [groupoid](https://ncatlab.org/nlab/show/groupoid) with a small set of objects, then the category [G,Set] (which makes sense if we define “large” and “small” relative to a [Grothendieck universe](https://ncatlab.org/nlab/show/Grothendieck+universe)) is a topos, but not in general a Grothendieck topos. Note that this topos is in fact [complete](https://ncatlab.org/nlab/show/complete+category) and cocomplete, but it does not have a small generating set, and so is an [unbounded topos](https://ncatlab.org/nlab/show/unbounded+topos).
    
- If ℱ is a [filter](https://ncatlab.org/nlab/show/filter) of [subterminal objects](https://ncatlab.org/nlab/show/subterminal+objects) in any topos E, then there is a filterquotient[?](https://ncatlab.org/nlab/new/filterquotient) topos E//ℱ. Grothendieck-ness (and completeness and cocompleteness) are not in general preserved by this construction.
    
- If C and D are toposes and F:C→D is a [lex functor](https://ncatlab.org/nlab/show/lex+functor), then there is a topos Gl(F) called the [Artin gluing](https://ncatlab.org/nlab/show/Artin+gluing) of C and D along F, and defined to be the [comma category](https://ncatlab.org/nlab/show/comma+category) (D/F). If C and D are Grothendieck toposes then Gl(F) is a Set-topos. If F is [accessible](https://ncatlab.org/nlab/show/accessible+functor), then Gl(F) is again Grothendieck (hence [bounded](https://ncatlab.org/nlab/show/bounded+geometric+morphism)), but in general it may not be. (Note, though, that it is not clear whether it can be proven in ZFC that there exist any inaccessible lex functors between Grothendieck toposes, although from a proper class of [measurable cardinal](https://ncatlab.org/nlab/show/measurable+cardinal)s one can construct an inaccessible lex endofunctor of Set.)
    
- The [category of coalgebras](https://ncatlab.org/nlab/show/Eilenberg-Moore+category) for any [lex](https://ncatlab.org/nlab/show/exact+functor) [comonad](https://ncatlab.org/nlab/show/comonad) on a topos is again a topos: a [topos of coalgebras](https://ncatlab.org/nlab/show/topos+of+algebras+over+a+monad), and if the comonad is [accessible](https://ncatlab.org/nlab/show/accessible+functor), this construction preserves Grothendieck-ness. If the comonad is not accessible, then this topos is unbounded.
    
    For instance the [Artin gluing](https://ncatlab.org/nlab/show/Artin+gluing) Gl(F) is equivalent to the category of coalgebras for the comonad on the topos C×D defined by (c,d)↦(c,d×F(c)).
    
- More generally, the category of coalgebras for any [pullback-preserving](https://ncatlab.org/nlab/show/preserved+limit) comonad on a topos is again a topos. This covers both the preceding result and also the overcategory (slice category) result above, since E/X is the category of coalgebras for the pullback-preserving comonad given by X×−:E→E. It also covers Artin gluing along a pullback-preserving functor.
    
- More generally still, [Todd Trimble](https://ncatlab.org/nlab/show/Todd+Trimble) has a notion called a “modal operator” on a topos, from which one can construct a new topos of “G-structures”: see [Three topos theorems in one](https://ncatlab.org/toddtrimble/published/Three+topos+theorems+in+one). Special cases include the pullback-preserving comonad result just mentioned, and the result that the category of algebras for a lex [idempotent monad](https://ncatlab.org/nlab/show/idempotent+monad) is a topos. A related idea is Toby Kenney’s notion of lex distributive diad[?](https://ncatlab.org/nlab/new/diad), from which one can also construct a topos.
    
- From any [partial combinatory algebra](https://ncatlab.org/nlab/show/partial+combinatory+algebra) one can construct a [realizability topos](https://ncatlab.org/nlab/show/realizability+topos), whose [internal logic](https://ncatlab.org/nlab/show/internal+logic) is “computable” or “effective” mathematics relative to that PCA. In particular, for [Kleene's first algebra](https://ncatlab.org/nlab/show/Kleene%27s+first+algebra), one obtains the [effective topos](https://ncatlab.org/nlab/show/effective+topos), the most-studied of realizability toposes. Realizability toposes are generally not Grothendieck toposes.
    
- A topos can also be constructed from any [tripos](https://ncatlab.org/nlab/show/tripos). This includes realizability toposes as well as toposes of sheaves on locales.
    

### Classes of examples

For various applications one uses toposes that have [extra structure or properties](https://ncatlab.org/nlab/show/stuff%2C+structure%2C+property).

- In the [foundations](https://ncatlab.org/nlab/show/foundations) of mathematics, one often studies [well-pointed toposes](https://ncatlab.org/nlab/show/well-pointed+toposes), especially models of [ETCS](https://ncatlab.org/nlab/show/ETCS) as potential replacements for the category [Set](https://ncatlab.org/nlab/show/Set).
    
- In [synthetic differential geometry](https://ncatlab.org/nlab/show/synthetic+differential+geometry) one studies [smooth topos](https://ncatlab.org/nlab/show/smooth+topos)es as a context for axiomatic [differential geometry](https://ncatlab.org/nlab/show/differential+geometry).
    

## 5. Related concepts

- [category of sheaves](https://ncatlab.org/nlab/show/category+of+sheaves), [Giraud's theorem](https://ncatlab.org/nlab/show/Giraud%27s+theorem)
    
- [base topos](https://ncatlab.org/nlab/show/base+topos), [indexed topos](https://ncatlab.org/nlab/show/indexed+topos)
    
- [slice topos](https://ncatlab.org/nlab/show/slice+topos), [fundamental theorem of topos theory](https://ncatlab.org/nlab/show/fundamental+theorem+of+topos+theory)
    
- [predicative topos](https://ncatlab.org/nlab/show/predicative+topos)
    
- [boolean topos](https://ncatlab.org/nlab/show/boolean+topos)
    
- [local topos](https://ncatlab.org/nlab/show/local+topos), [locally connected topos](https://ncatlab.org/nlab/show/locally+connected+topos), [connected topos](https://ncatlab.org/nlab/show/connected+topos), [cohesive topos](https://ncatlab.org/nlab/show/cohesive+topos)
    
- [predicative topos](https://ncatlab.org/nlab/show/predicative+topos)
    
- [pretopos](https://ncatlab.org/nlab/show/pretopos), [Π-pretopos](https://ncatlab.org/nlab/show/%CE%A0-pretopos), [ΠW-pretopos](https://ncatlab.org/nlab/show/%CE%A0W-pretopos), [list-arithmetic pretopos](https://ncatlab.org/nlab/show/list-arithmetic+pretopos)
    
- [smooth structure on a topos](https://ncatlab.org/nlab/show/smooth+structure+on+a+topos)
    
- [monoidal topos](https://ncatlab.org/nlab/show/monoidal+topos)
    
- [isotropy group of a topos](https://ncatlab.org/nlab/show/isotropy+group+of+a+topos)
    
- [test topos](https://ncatlab.org/nlab/show/test+topos)
    
- [classifying topos](https://ncatlab.org/nlab/show/classifying+topos)
    

**flavors of [higher toposes](https://ncatlab.org/nlab/show/higher+topos+theory)**

- [1-topos](https://ncatlab.org/nlab/show/1-topos)
    
    - [(0,1)-topos](https://ncatlab.org/nlab/show/%280%2C1%29-topos)
        
    - [(1,1)-topos](https://ncatlab.org/nlab/show/%281%2C1%29-topos) = [topos](https://ncatlab.org/nlab/show/topos)
        
    - [(2,1)-topos](https://ncatlab.org/nlab/show/%282%2C1%29-topos)
        
    - [(n,1)-topos](https://ncatlab.org/nlab/show/%28n%2C1%29-topos)
        
    - [(∞,1)-topos](https://ncatlab.org/nlab/show/%28%E2%88%9E%2C1%29-topos) ([n-localic](https://ncatlab.org/nlab/show/n-localic+%28infinity%2C1%29-topos))
        
         [model topos](https://ncatlab.org/nlab/show/model+topos)
        
- [2-topos](https://ncatlab.org/nlab/show/2-topos)
    
    - [(2,2)-topos](https://ncatlab.org/nlab/show/%282%2C2%29-topos) ([n-localic](https://ncatlab.org/nlab/show/n-localic+2-topos))
        
    - [(∞,2)-topos](https://ncatlab.org/nlab/show/%28%E2%88%9E%2C2%29-topos)
        
- [n-topos](https://ncatlab.org/nlab/show/n-topos)
    
    - [(∞,n)-topos](https://ncatlab.org/nlab/show/%28%E2%88%9E%2Cn%29-topos)

**Locally presentable categories:** [Cocomplete](https://ncatlab.org/nlab/show/cocomplete+category) possibly-[large categories](https://ncatlab.org/nlab/show/large+categories) generated under [filtered colimits](https://ncatlab.org/nlab/show/filtered+colimits) by [small](https://ncatlab.org/nlab/show/small+object) [generators](https://ncatlab.org/nlab/show/generators) under [small](https://ncatlab.org/nlab/show/small+colimit) [relations](https://ncatlab.org/nlab/show/relations). Equivalently, [accessible](https://ncatlab.org/nlab/show/accessible+functor) [reflective localizations](https://ncatlab.org/nlab/show/reflective+localizations) of [free cocompletions](https://ncatlab.org/nlab/show/free+cocompletions). Accessible categories omit the cocompleteness requirement; toposes add the requirement of a [left exact](https://ncatlab.org/nlab/show/left+exact+functor) localization.

|[(n,r)-categories](https://ncatlab.org/nlab/show/%28n%2Cr%29-categories)|[toposes](https://ncatlab.org/nlab/show/toposes)|locally presentable|loc finitely pres|localization theorem|[free cocompletion](https://ncatlab.org/nlab/show/free+cocompletion)|accessible|
|---|---|---|---|---|---|---|
|**[(0,1)-category theory](https://ncatlab.org/nlab/show/%280%2C1%29-category+theory)**|[locales](https://ncatlab.org/nlab/show/locales)|[suplattice](https://ncatlab.org/nlab/show/suplattice)|[algebraic lattices](https://ncatlab.org/nlab/show/algebraic+lattices)|[Porst’s theorem](https://ncatlab.org/nlab/show/algebraic+lattice#RelationToLocallyFinitelyPresentableCategories)|[powerset](https://ncatlab.org/nlab/show/powerset)|[poset](https://ncatlab.org/nlab/show/poset)|
|**[category theory](https://ncatlab.org/nlab/show/category+theory)**|[toposes](https://ncatlab.org/nlab/show/Grothendieck+topos)|[locally presentable categories](https://ncatlab.org/nlab/show/locally+presentable+categories)|[locally finitely presentable categories](https://ncatlab.org/nlab/show/locally+finitely+presentable+categories)|[Gabriel–Ulmer’s theorem](https://ncatlab.org/nlab/show/locally+presentable+category#AsLocalizationsOfPresheafCategories)|[presheaf category](https://ncatlab.org/nlab/show/presheaf+category)|[accessible categories](https://ncatlab.org/nlab/show/accessible+categories)|
|**[model category theory](https://ncatlab.org/nlab/show/model+category)**|[model toposes](https://ncatlab.org/nlab/show/model+toposes)|[combinatorial model categories](https://ncatlab.org/nlab/show/combinatorial+model+categories)||[Dugger's theorem](https://ncatlab.org/nlab/show/Dugger%27s+theorem)|global [model structures on simplicial presheaves](https://ncatlab.org/nlab/show/model+structures+on+simplicial+presheaves)|n/a|
|**[(∞,1)-category theory](https://ncatlab.org/nlab/show/%28%E2%88%9E%2C1%29-category+theory)**|[(∞,1)-toposes](https://ncatlab.org/nlab/show/%28%E2%88%9E%2C1%29-toposes)|[locally presentable (∞,1)-categories](https://ncatlab.org/nlab/show/locally+presentable+%28%E2%88%9E%2C1%29-categories)||[Simpson’s theorem](https://ncatlab.org/nlab/show/locally+presentable+infinity-category#Definition)|[(∞,1)-presheaf (∞,1)-categories](https://ncatlab.org/nlab/show/%28%E2%88%9E%2C1%29-presheaf+%28%E2%88%9E%2C1%29-categories)|[accessible (∞,1)-categories](https://ncatlab.org/nlab/show/accessible+%28%E2%88%9E%2C1%29-categories)|

## 6. References

### Introductions

Brief expositions:

- [Ieke Moerdijk](https://ncatlab.org/nlab/show/Ieke+Moerdijk), _Background in topos theory_, chapter I in: _Classifying Spaces and Classifying Topoi_, Lecture Notes in Mathematics **1616**, Springer (1995) [[doi:10.1007/BFb0094441](https://doi.org/10.1007/BFb0094441)]
    
- [Luc Illusie](https://ncatlab.org/nlab/show/Luc+Illusie), _What is… a Topos?_, Notices of the AMS **51** 9 (2004) [[pdf](https://www.ams.org/notices/200409/what-is-illusie.pdf), full volume:[pdf](https://www.ams.org/notices/200409/200409FullIssue.pdf)]
    
- [Tom Leinster](https://ncatlab.org/nlab/show/Tom+Leinster), _[An informal introduction to topos theory](https://ncatlab.org/nlab/show/Leinster2010)_ (2010) [[arXiv:1012.5647](https://arxiv.org/abs/1012.5647)]
    
- [John Baez](https://ncatlab.org/nlab/show/John+Baez), _Topos Theory in a Nutshell_ (2021) [[web](http://math.ucr.edu/home/baez/topos.html)]
    
- MathProofsable, Category Theory - Toposes [video playlist](https://www.youtube.com/watch?v=gKYpvyQPhZo&list=PL4FD0wu2mjWM3ZSxXBj4LRNsNKWZYaT7k)
    

Lecture notes:

- [Jean Bénabou](https://ncatlab.org/nlab/show/Jean+B%C3%A9nabou), _Problèmes dans les topos_, Séminaire de mathématique pure **34**, Université de Louvain (1973) [[pdf](https://ncatlab.org/nlab/files/Benabou-ProblemesDansLesTopos.pdf "pdf")]
    
- [Ross Street](https://ncatlab.org/nlab/show/Ross+Street), _A survey of topos theory_, lecture notes (1978) [[pdf](http://www.math.mq.edu.au/~street/ToposSurvey.pdf), [pdf](https://ncatlab.org/nlab/files/Street-SurveyToposTheory.pdf "pdf")]
    
- [Oswald Wyler](https://ncatlab.org/nlab/show/Oswald+Wyler), _Lecture Notes on Topoi and Quasitopoi_, World Scientific (1991) [[doi:10.1142/1047](https://doi.org/10.1142/1047)]
    
- [André Joyal](https://ncatlab.org/nlab/show/Andr%C3%A9+Joyal), _[A crash course in topos theory – The big picture](https://ncatlab.org/nlab/show/A+crash+course+in+topos+theory+--+The+big+picture)_, lecture series at [Topos à l’IHES](https://indico.math.cnrs.fr/event/747/), Paris (November 2015)
    
- [André Joyal](https://ncatlab.org/nlab/show/Andr%C3%A9+Joyal), _Geometric aspects of topos theory in relation with logical doctrines_, talk at _[New Spaces for Mathematics and Physics](https://ncatlab.org/nlab/show/New+Spaces+for+Mathematics+and+Physics)_, IHP Paris 2015 ([video recording](https://www.youtube.com/watch?v=kaZpOEOAUzE))
    
- [Ieke Moerdijk](https://ncatlab.org/nlab/show/Ieke+Moerdijk), [Jaap van Oosten](https://ncatlab.org/nlab/show/Jaap+van+Oosten), _Topos Theory_, Master class notes (2007) [[pdf](http://www.staff.science.uu.nl/~ooste110/syllabi/toposmoeder.pdf)]
    
- [Jaap van Oosten](https://ncatlab.org/nlab/show/Jaap+van+Oosten), _Topos Theory_ (2018) [[pdf](https://webspace.science.uu.nl/~ooste110/syllabi/topostheory.pdf), [pdf](https://ncatlab.org/nlab/files/vanOosten-ToposTheory.pdf "pdf")]
    
- [Francis Borceux](https://ncatlab.org/nlab/show/Francis+Borceux), _Some glances at topos theory_, lecture notes, Como (2018) [[pdf](https://tcsc.lakecomoschool.org/files/2018/01/Borceux.pdf), [pdf](https://ncatlab.org/nlab/files/Borceux-ToposTheory.pdf "pdf"), [video playlist](https://www.youtube.com/watch?v=s_fN9euuVAY&list=PLh_3Q6ZRqWs0LBptMGClJ8OArR0fBT6Pp&index=11)]
    

A monograph that aims to be more expository, focusing on [presheaf toposes](https://ncatlab.org/nlab/show/presheaf+toposes):

- [Marie La Palme Reyes](https://ncatlab.org/nlab/show/Marie+La+Palme+Reyes), [Gonzalo E. Reyes](https://ncatlab.org/nlab/show/Gonzalo+E.+Reyes), [Houman Zolfaghari](https://ncatlab.org/nlab/show/Houman+Zolfaghari), _Generic figures and their glueings. A constructive approach to functor categories_, Polimetrica (2008) [[pdf](https://marieetgonzalo.files.wordpress.com/2004/06/generic-figures.pdf), ISBN:8876990046]

### Monographs

- [Peter Johnstone](https://ncatlab.org/nlab/show/Peter+Johnstone), _Topos theory_, London Math. Soc. Monographs **10**, Acad. Press 1977, xxiii+367 pp. (Dover reprint 2014)
    
- [Michael Barr](https://ncatlab.org/nlab/show/Michael+Barr), [Charles Wells](https://ncatlab.org/nlab/show/Charles+Wells), _[Toposes, Triples, and Theories](https://ncatlab.org/nlab/show/Toposes%2C+Triples%2C+and+Theories)_, Springer Heidelberg 1985. ([TAC reprint](http://www.tac.mta.ca/tac/reprints/articles/12/tr12.pdf))
    
- [Colin McLarty](https://ncatlab.org/nlab/show/Colin+McLarty), _[Elementary Categories, Elementary Toposes](https://ncatlab.org/nlab/show/Elementary+Categories%2C+Elementary+Toposes)_, Oxford University Press 1992 ([ISBN:9780198514732](https://global.oup.com/academic/product/elementary-categories-elementary-toposes-9780198514732?cc=ae&lang=en&))
    
- [Saunders MacLane](https://ncatlab.org/nlab/show/Saunders+MacLane), [Ieke Moerdijk](https://ncatlab.org/nlab/show/Ieke+Moerdijk), _[Sheaves in Geometry and Logic](https://ncatlab.org/nlab/show/Sheaves+in+Geometry+and+Logic)_, 1992
    
- [Francis Borceux](https://ncatlab.org/nlab/show/Francis+Borceux), _[Handbook of Categorical Algebra](https://ncatlab.org/nlab/show/Handbook+of+Categorical+Algebra) 3 - Categories of Sheaves_, Cambridge UP 1994 ([ISBN:9780521061247](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/handbook-categorical-algebra-volume-3?format=PB))
    
- [Peter Johnstone](https://ncatlab.org/nlab/show/Peter+Johnstone), _[Sketches of an elephant: a topos theory compendium](https://ncatlab.org/nlab/show/Elephant)_ Oxford University Press 2002, Volume 1 ([ISBN:9780198534259](https://global.oup.com/academic/product/sketches-of-an-elephant-9780198534259)), Volume 2 ([ISBN:9780198515982](https://global.oup.com/academic/product/sketches-of-an-elephant-9780198515982))
    
- [Garth Warner](https://ncatlab.org/nlab/show/Garth+Warner), _Homotopical Topos Theory_, EPrint Collection, University of Washington (2012) [[hdl:1773/19722](http://hdl.handle.net/1773/19722), [pdf](https://sites.math.washington.edu//~warner/HTT_Warner.pdf), [pdf](https://ncatlab.org/nlab/files/Waner-HomotopicalTopos.pdf "pdf")]
    

### Classifying toposes

Specifically on [classifying toposes](https://ncatlab.org/nlab/show/classifying+toposes):

- [Ieke Moerdijk](https://ncatlab.org/nlab/show/Ieke+Moerdijk), _Classifying Spaces and Classifying Topoi_, Lecture Notes in Mathematics 1616, Springer 1995 (ISBN: 978-3-540-60319-1, [doi:10.1007/BFb0094441](https://doi.org/10.1007/BFb0094441))
    
- [Olivia Caramello](https://ncatlab.org/nlab/show/Olivia+Caramello), _Theories, Sites, Toposes_, Oxford University Press, 2017.
    
    [doi](https://doi.org/10.1007/BFb0094441)
    

### Categorical logic and elementary toposes

On [categorical logic](https://ncatlab.org/nlab/show/categorical+logic) via toposes:

- [Colin McLarty](https://ncatlab.org/nlab/show/Colin+McLarty), _Elementary Categories, Elementary Toposes_, Oxford University Press 1992 (reprinted in 2005) ([ISBN:9780198514732](https://global.oup.com/academic/product/elementary-categories-elementary-toposes-9780198514732))
    
- Jonathan Chapman, Frederick Rowbottom, _Relative Category Theory and Geometric Morphisms. A Logical Approach_, Oxford University Press 1992 ([ISBN:9780198534341](https://global.oup.com/academic/product/relative-category-theory-and-geometric-morphisms-9780198534341))
    
- J. L. Bell, _Toposes and Local Set Theories. An Introduction_, Oxford University Press 1988 ([doi:10.2307/2274680](https://doi.org/10.2307/2274680))
    
- [Robert Goldblatt](https://ncatlab.org/nlab/show/Robert+Goldblatt), _Topoi. The categorial analysis of logic_, Studies in Logic and the Foundations of Math. **98**, North-Holland Publ. Co., Amsterdam, 1979, 1984; (Rus. transl. Mir Publ., Moscow 1983).
    
- [Joachim Lambek](https://ncatlab.org/nlab/show/Joachim+Lambek), [Philip J. Scott](https://ncatlab.org/nlab/show/Philip+J.+Scott), _Introduction to higher order categorical logic_, Cambridge Studies in Advanced Mathematics 7 (1986) ([ISBN: 0-521-24665-2](https://www.cambridge.org/ae/academic/subjects/mathematics/logic-categories-and-sets/introduction-higher-order-categorical-logic?format=PB&isbn=9780521356534))
    
- [Bart Jacobs](https://ncatlab.org/nlab/show/Bart+Jacobs), _Categorical logic and type theory_, Studies in Logic and the Foundations of Mathematics 141 (1999). North-Holland Publishing Co.
    
    ISBN: 0-444-50170-3
    

### Algebra, ringed toposes, algebraic geometry

- [Monique Hakim](https://ncatlab.org/nlab/show/Monique+Hakim), _Topos annelés et schémas relatifs_, Ergebnisse der Mathematik und ihrer Grenzgebiete 64 (1972) ([ISBN:9783540055730](https://www.springer.com/gp/book/9783540055730))
    
- [Francis Borceux](https://ncatlab.org/nlab/show/Francis+Borceux), Gilberte van den Bossche, _Algebra in a localic topos with applications to ring theory_, Lecture Notes in Mathematics 1038 (1983), ISBN: 3-540-12711-9 ([ISBN:9783540127116](https://www.springer.com/gp/book/9783540127116))
    

### Quantum theory

- [Cecilia Flori](https://ncatlab.org/nlab/show/Cecilia+Flori), _A first course in topos quantum theory_. Lecture Notes in Physics 868 (2013).
    
    ISBN: 978-3-642-35712-1; 978-3-642-35713-8
    
- [Cecilia Flori](https://ncatlab.org/nlab/show/Cecilia+Flori), _A second course in topos quantum theory_. Lecture Notes in Physics 944 (2018).
    
    ISBN: 978-3-319-71107-2; 978-3-319-71108-9
    

### Original articles

Original source of (Grothendieck) topoi:

- [SGA4](https://ncatlab.org/nlab/show/SGA4) Exposé IV by Grothendieck and Verdier (and Exposé V for cohomology in a (Grothendieck) topos)

That every topos is an [adhesive category](https://ncatlab.org/nlab/show/adhesive+category) is discussed in

- [Stephen Lack](https://ncatlab.org/nlab/show/Stephen+Lack), Pawel Sobociński, _Toposes are adhesive_ ([pdf](http://users.ecs.soton.ac.uk/ps/papers/toposesAdhesive.pdf))

### History

- [Colin McLarty](https://ncatlab.org/nlab/show/Colin+McLarty), _The Uses and Abuses of the History of Topos Theory_ , Brit. J. Phil. Sci., 41 (1990) ([JSTOR](http://www.jstor.org/stable/687825)) [PDF](http://bjps.oxfordjournals.org/content/41/3/351.full.pdf) ([direct link](http://www.cwru.edu/artsci/phil/UsesandAbuses%20HistoryToposTheory.pdf))
    
- [John W. Gray](https://ncatlab.org/nlab/show/John+W.+Gray), _Fragments of the history of sheaf theory_,
    
    in: Applications of Sheaves, pp. 1–79, Lecture Notes in Mathematics 753, ISBN: 978-3-540-09564-4, [doi](https://doi.org/10.1007/BFb0061812).
    

According to appendix C.1 in

- [William Lawvere](https://ncatlab.org/nlab/show/William+Lawvere), [Robert Rosebrugh](https://ncatlab.org/nlab/show/Robert+Rosebrugh), _[Sets for Mathematics](https://ncatlab.org/nlab/show/Sets+for+Mathematics)_ , Cambridge UP 2003. ([web](http://books.google.de/books?id=h3_7aZz9ZMoC&pg=PP1&dq=sets+for+mathematics))

> “Topos” is a Greek term intended to describe the objects studied by “[analysis situs](http://en.wikipedia.org/wiki/Analysis_Situs_%28paper%29),” the Latin term previously established by Poincaré to signify the science of place [or situation]; in keeping with those ideas, a 𝒰-topos was shown to have presentations in various “sites”.

A historical analysis of Grothendieck’s 1973 Buffalo lecture series on toposes and their precedents is in

- [Colin McLarty](https://ncatlab.org/nlab/show/Colin+McLarty), _Grothendieck’s 1973 topos lectures_, Séminaire Lectures grothendieckiennes, 3 May (2018) ([YouTube video](https://www.youtube.com/watch?v=hhWT5V0oaSI))

### General theory

On the application of diads[?](https://ncatlab.org/nlab/new/diads) to constructing toposes:

- Toby Kenney, _Diads and their Application to Topoi_, Applied Categorical Structures 17 (2009): 567-590.

Last revised on July 29, 2024 at 10:25:20. See the [history](https://ncatlab.org/nlab/history/topos) of this page for a list of all contributions to it.

[Edit](https://ncatlab.org/nlab/edit/topos)[Discuss](https://nforum.ncatlab.org/discussion/189/#Item_37)[Previous revision](https://ncatlab.org/nlab/revision/topos/122)[Changes from previous revision](https://ncatlab.org/nlab/show/diff/topos)[History (122 revisions)](https://ncatlab.org/nlab/history/topos) [Cite](https://ncatlab.org/nlab/show/topos/cite) [Print](https://ncatlab.org/nlab/print/topos) [Source](https://ncatlab.org/nlab/source/topos)