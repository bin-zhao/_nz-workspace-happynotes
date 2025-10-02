
---

In [mathematics](https://en.wikipedia.org/wiki/Mathematics "Mathematics"), a **topos** ([US](https://en.wikipedia.org/wiki/American_English "American English"): [/ˈtɒpɒs/](https://en.wikipedia.org/wiki/Help:IPA/English "Help:IPA/English"), [UK](https://en.wikipedia.org/wiki/British_English "British English"): [/ˈtoʊpoʊs, ˈtoʊpɒs/](https://en.wikipedia.org/wiki/Help:IPA/English "Help:IPA/English"); plural **topoi** [/ˈtɒpɔɪ/](https://en.wikipedia.org/wiki/Help:IPA/English "Help:IPA/English") or [/ˈtoʊpɔɪ/](https://en.wikipedia.org/wiki/Help:IPA/English "Help:IPA/English"), or **toposes**) is a [category](https://en.wikipedia.org/wiki/Category_(mathematics) "Category (mathematics)") that behaves like the category of [sheaves](https://en.wikipedia.org/wiki/Sheaf_(mathematics) "Sheaf (mathematics)") of [sets](https://en.wikipedia.org/wiki/Set_(mathematics) "Set (mathematics)") on a [topological space](https://en.wikipedia.org/wiki/Topological_space "Topological space") (or more generally: on a [site](https://en.wikipedia.org/wiki/Site_(mathematics) "Site (mathematics)")). Topoi behave much like the [category of sets](https://en.wikipedia.org/wiki/Category_of_sets "Category of sets") and possess a notion of localization; they are a direct generalization of [point-set topology](https://en.wikipedia.org/wiki/Point-set_topology "Point-set topology").[[1]](https://en.wikipedia.org/wiki/Topos#cite_note-Illusie2004-1) The **Grothendieck topoi** find applications in [algebraic geometry](https://en.wikipedia.org/wiki/Algebraic_geometry "Algebraic geometry"); the more general **elementary topoi** are used in [logic](https://en.wikipedia.org/wiki/Mathematical_logic "Mathematical logic").

The mathematical field that studies topoi is called **topos theory**.

## Grothendieck topos (topos in geometry)

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=1 "Edit section: Grothendieck topos (topos in geometry)")]

Since the introduction of sheaves into mathematics in the 1940s, a major theme has been to study a space by studying sheaves on a space. This idea was expounded by [Alexander Grothendieck](https://en.wikipedia.org/wiki/Alexander_Grothendieck "Alexander Grothendieck") by introducing the notion of a "topos". The main utility of this notion is in the abundance of situations in mathematics where topological heuristics are very effective, but an honest topological space is lacking; it is sometimes possible to find a topos formalizing the heuristic. An important example of this programmatic idea is the [étale topos](https://en.wikipedia.org/wiki/%C3%89tale_topos "Étale topos") of a [scheme](https://en.wikipedia.org/wiki/Scheme_(mathematics) "Scheme (mathematics)"). Another illustration of the capability of Grothendieck topoi to incarnate the “essence” of different mathematical situations is given by their use as "bridges" for connecting theories which, albeit written in possibly very different languages, share a common mathematical content.[[2]](https://en.wikipedia.org/wiki/Topos#cite_note-2)[[3]](https://en.wikipedia.org/wiki/Topos#cite_note-3) These "bridges", according to mathematician [Olivia Caramello](https://en.wikipedia.org/wiki/Olivia_Caramello "Olivia Caramello"), who is the founder and president of the Grothendieck Institute research organisation, could also be "capable of facilitating the transfer of information between different domains".[[4]](https://en.wikipedia.org/wiki/Topos#cite_note-Caramel#-4) For this reason, the technology company [Huawei](https://en.wikipedia.org/wiki/Huawei "Huawei") has commissioned the mathematician [Laurent Lafforgue](https://en.wikipedia.org/wiki/Laurent_Lafforgue "Laurent Lafforgue") to delve deeper into this aspect in order to be able to use Grothendieck's pioneering studies for development in the field of research into increasingly effective AI.[[4]](https://en.wikipedia.org/wiki/Topos#cite_note-Caramel#-4)

### Equivalent definitions

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=2 "Edit section: Equivalent definitions")]

A Grothendieck topos is a [category](https://en.wikipedia.org/wiki/Category_(mathematics) "Category (mathematics)") C![[Mathematics/Library/_Attachments/775be1eccdc7f2a266be45a98d65560f_MD5.svg]] which satisfies any one of the following three properties. (A [theorem](https://en.wikipedia.org/w/index.php?title=Giraud%27s_theorem&action=edit&redlink=1 "Giraud's theorem (page does not exist)") of [Jean Giraud](https://en.wikipedia.org/wiki/Jean_Giraud_(mathematician) "Jean Giraud (mathematician)") states that the properties below are all equivalent.)

- There is a [small category](https://en.wikipedia.org/wiki/Category_(mathematics)#Small_and_large_categories "Category (mathematics)") D![[Mathematics/Library/_Attachments/8f6a580f79cf6dc038a5617e6b0c8ebc_MD5.svg]] and an inclusion C↪PreshD![[e6b16dda793b423f3afcf12826af9568_MD5.svg]] that admits a finite-[limit-preserving](https://en.wikipedia.org/wiki/Adjoint_functor#Limit_preservation "Adjoint functor") [left adjoint](https://en.wikipedia.org/wiki/Left_adjoint "Left adjoint").
- C![[Mathematics/Library/_Attachments/775be1eccdc7f2a266be45a98d65560f_MD5.svg]] is the category of sheaves on a [Grothendieck site](https://en.wikipedia.org/wiki/Grothendieck_site "Grothendieck site").
- C![[Mathematics/Library/_Attachments/775be1eccdc7f2a266be45a98d65560f_MD5.svg]] satisfies Giraud's axioms, below.

Here Presh(_D_) denotes the category of [contravariant functors](https://en.wikipedia.org/wiki/Contravariant_functor#Covariance_and_contravariance "Contravariant functor") from _D_ to the category of sets; such a contravariant functor is frequently called a [presheaf](https://en.wikipedia.org/wiki/Presheaf_(category_theory) "Presheaf (category theory)").

#### Giraud's axioms

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=3 "Edit section: Giraud's axioms")]

Giraud's axioms for a [category](https://en.wikipedia.org/wiki/Category_(mathematics) "Category (mathematics)") _C_ are:

- _C_ has a small set of [generators](https://en.wikipedia.org/wiki/Generator_(category_theory) "Generator (category theory)"), and admits all small [colimits](https://en.wikipedia.org/wiki/Colimit "Colimit"). Furthermore, [fiber products](https://en.wikipedia.org/wiki/Fiber_product "Fiber product") distribute over coproducts. That is, given a set _I_, an _I_-indexed coproduct mapping to _A_, and a morphism _A'_ → _A_, the pullback is an _I_-indexed coproduct of the pullbacks:(∐i∈IBi)×AA′≅∐i∈I(Bi×AA′).![[bd17daf7b891cacb08d7cc800a23178d_MD5.svg]]
- Sums in _C_ are disjoint. In other words, the fiber product of _X_ and _Y_ over their sum is the [initial object](https://en.wikipedia.org/wiki/Initial_and_terminal_objects "Initial and terminal objects") in _C_.
- All [equivalence relations](https://en.wikipedia.org/wiki/Equivalence_relation "Equivalence relation") in _C_ are [effective](https://en.wikipedia.org/wiki/Regular_category#Exact_(effective)_categories "Regular category").

The last axiom needs the most explanation. If _X_ is an object of _C_, an "equivalence relation" _R_ on _X_ is a map _R_ → _X_ × _X_ in _C_ such that for any object _Y_ in _C_, the induced map Hom(_Y_, _R_) → Hom(_Y_, _X_) × Hom(_Y_, _X_) gives an ordinary equivalence relation on the set Hom(_Y_, _X_). Since _C_ has colimits we may form the [coequalizer](https://en.wikipedia.org/wiki/Coequalizer "Coequalizer") of the two maps _R_ → _X_; call this _X_/_R_. The equivalence relation is "effective" if the canonical map

R→X×X/RX![[6b86249f143c3653ad1563feb0b243b3_MD5.svg]]

is an isomorphism.

### Examples

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=4 "Edit section: Examples")]

Giraud's theorem already gives "sheaves on sites" as a complete list of examples. Note, however, that nonequivalent sites often give rise to equivalent topoi. As indicated in the introduction, sheaves on ordinary topological spaces motivate many of the basic definitions and results of topos theory.

#### Category of sets and G-sets

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=5 "Edit section: Category of sets and G-sets")]

The [category](https://en.wikipedia.org/wiki/Category_(mathematics) "Category (mathematics)") of sets is an important special case: it plays the role of a point in topos theory. Indeed, a set may be thought of as a sheaf on a point since functors on the singleton category with a single object and only the identity morphism are just specific sets in the category of sets.

Similarly, there is a topos BG![[30a0e5da1b107189704e5f2143057642_MD5.svg]] for any [group](https://en.wikipedia.org/wiki/Group_(mathematics) "Group (mathematics)") G![[8a01b8b901f9ef0093f7cafa1ddfb4f6_MD5.svg]] which is equivalent to the category of G![[8a01b8b901f9ef0093f7cafa1ddfb4f6_MD5.svg]]-sets. We construct this as the category of presheaves on the category with one object, but now the set of morphisms is given by the [group](https://en.wikipedia.org/wiki/Group_(mathematics) "Group (mathematics)") G![[8a01b8b901f9ef0093f7cafa1ddfb4f6_MD5.svg]]. Since any functor must give a G![[8a01b8b901f9ef0093f7cafa1ddfb4f6_MD5.svg]]-action on the target, this gives the category of G![[8a01b8b901f9ef0093f7cafa1ddfb4f6_MD5.svg]]-sets. Similarly, for a [groupoid](https://en.wikipedia.org/wiki/Groupoid "Groupoid") G![[320d1b7156503bf3f7a5c6685d923c73_MD5.svg]] the category of presheaves on G![[320d1b7156503bf3f7a5c6685d923c73_MD5.svg]] gives a collection of sets indexed by the set of objects in G![[320d1b7156503bf3f7a5c6685d923c73_MD5.svg]], and the automorphisms of an object in G![[320d1b7156503bf3f7a5c6685d923c73_MD5.svg]] has an action on the target of the functor.

#### Topoi from ringed spaces

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=6 "Edit section: Topoi from ringed spaces")]

More exotic examples, and the _raison d'être_ of topos theory, come from algebraic geometry. The basic example of a topos comes from the Zariski topos of a [scheme](https://en.wikipedia.org/wiki/Scheme_(mathematics) "Scheme (mathematics)"). For each scheme X![[Mathematics/Library/_Attachments/927f5aa510997acca075e1f83541f321_MD5.svg]] there is a site Open(X)![[cbde4ddbe3a2e4f3a388fb581a84529c_MD5.svg]] (of objects given by open subsets and morphisms given by inclusions) whose category of presheaves forms the Zariski topos (X)Zar![[fa37bcf528e5ec47c366958d6da8be7a_MD5.svg]]. But once distinguished classes of morphisms are considered, there are multiple generalizations of this which leads to non-trivial mathematics. Moreover, topoi give the foundations for studying schemes purely as functors on the category of algebras.

To a scheme and even a [stack](https://en.wikipedia.org/wiki/Stack_(mathematics) "Stack (mathematics)") one may associate an [étale](https://en.wikipedia.org/wiki/%C3%89tale_topology "Étale topology") topos, an [fppf](https://en.wikipedia.org/wiki/Flat_topology "Flat topology") topos, or a [Nisnevich](https://en.wikipedia.org/wiki/Nisnevich_topology "Nisnevich topology") topos. Another important example of a topos is from the [crystalline site](https://en.wikipedia.org/wiki/Crystal_(mathematics) "Crystal (mathematics)"). In the case of the étale topos, these form the foundational objects of study in [anabelian geometry](https://en.wikipedia.org/wiki/Anabelian_geometry "Anabelian geometry"), which studies objects in algebraic geometry that are determined entirely by the structure of their [étale fundamental group](https://en.wikipedia.org/wiki/%C3%89tale_fundamental_group "Étale fundamental group").

#### Pathologies

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=7 "Edit section: Pathologies")]

Topos theory is, in some sense, a generalization of classical point-set topology. One should therefore expect to see old and new instances of [pathological](https://en.wikipedia.org/wiki/Pathological_(mathematics) "Pathological (mathematics)") behavior. For instance, there is an example due to [Pierre Deligne](https://en.wikipedia.org/wiki/Pierre_Deligne "Pierre Deligne") of a nontrivial topos that has no points (see below for the definition of points of a topos).

### Geometric morphisms

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=8 "Edit section: Geometric morphisms")]

If X![[Mathematics/Library/_Attachments/927f5aa510997acca075e1f83541f321_MD5.svg]] and Y![[2ff97d7c740f8d106fc609174f89ec2e_MD5.svg]] are topoi, a _geometric morphism_ u:X→Y![[Mathematics/Library/_Attachments/e47e4e340d5cf5962b539e50d995a60b_MD5.svg]] is a pair of [adjoint functors](https://en.wikipedia.org/wiki/Adjoint_functor "Adjoint functor") (_u_∗,_u_∗) (where _u_∗ : _Y_ → _X_ is left adjoint to _u_∗ : _X_ → _Y_) such that _u_∗ preserves finite limits. Note that _u_∗ automatically preserves colimits by virtue of having a right adjoint.

By [Freyd's adjoint functor theorem](https://en.wikipedia.org/wiki/Adjoint_functors#Existence "Adjoint functors"), to give a geometric morphism _X_ → _Y_ is to give a functor _u_∗: _Y_ → _X_ that preserves finite limits and all small colimits. Thus geometric morphisms between topoi may be seen as analogues of maps of [locales](https://en.wikipedia.org/wiki/Frames_and_locales "Frames and locales").

If X![[Mathematics/Library/_Attachments/927f5aa510997acca075e1f83541f321_MD5.svg]] and Y![[2ff97d7c740f8d106fc609174f89ec2e_MD5.svg]] are topological spaces and u![[Mathematics/Library/_Attachments/19666348527f98a56d3b5701a9f488f5_MD5.svg]] is a continuous map between them, then the pullback and pushforward operations on sheaves yield a geometric morphism between the associated topoi for the sites Open(X),Open(Y)![[2a2e1339b1840a8a0d485c3f6e56bbce_MD5.svg]].

#### Points of topoi

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=9 "Edit section: Points of topoi")]

A point of a topos X![[Mathematics/Library/_Attachments/927f5aa510997acca075e1f83541f321_MD5.svg]] is defined as a geometric morphism from the topos of sets to X![[Mathematics/Library/_Attachments/927f5aa510997acca075e1f83541f321_MD5.svg]].

If _X_ is an ordinary space and _x_ is a point of _X_, then the functor that takes a sheaf _F_ to its stalk _Fx_ has a right adjoint (the "skyscraper sheaf" functor), so an ordinary point of _X_ also determines a topos-theoretic point. These may be constructed as the pullback-pushforward along the continuous map _x_: _1_ → _X_.

For the etale topos (X)et![[c34eff1dcb2eead7eb201889476ba9a4_MD5.svg]] of a space X![[Mathematics/Library/_Attachments/927f5aa510997acca075e1f83541f321_MD5.svg]], a point is a bit more refined of an object. Given a point x:Spec(κ(x))→X![[8ecc93bbcc7ee57088af98f54afde574_MD5.svg]] of the underlying scheme X![[Mathematics/Library/_Attachments/927f5aa510997acca075e1f83541f321_MD5.svg]] a point x′![[eb623ba8a693ca57fbf6f6a2be97af6d_MD5.svg]] of the topos (X)et![[c34eff1dcb2eead7eb201889476ba9a4_MD5.svg]] is then given by a separable field extension k![[Mathematics/Library/_Attachments/2c38bdad4febcd2b5997c857b9303d7c_MD5.svg]] of κ(x)![[80ceda7d10885165a4f7917ecd97c0ef_MD5.svg]] such that the associated map x′:Spec(k)→X![[9c1954499a8d91621ac9b4dd6a6be2b0_MD5.svg]] factors through the original point x![[Mathematics/Library/_Attachments/d7e30fd6dc4f399f8a03b78dfca1b402_MD5.svg]]. Then, the factorization mapSpec(k)→Spec(κ(x))![[1fc53329a6889bb0865b5bfb6f64b92c_MD5.svg]]is an [etale morphism](https://en.wikipedia.org/wiki/%C3%89tale_morphism "Étale morphism") of schemes.

More precisely, those are the _global_ points. They are not adequate in themselves for displaying the space-like aspect of a topos, because a non-trivial topos may fail to have any. _Generalized_ points are geometric morphisms from a topos _Y_ (the _stage of definition_) to _X_. There are enough of these to display the space-like aspect. For example, if _X_ is the [classifying topos](https://en.wikipedia.org/wiki/Classifying_topos "Classifying topos") _S_[_T_] for a geometric theory _T_, then the universal property says that its points are the models of _T_ (in any stage of definition _Y_).

#### Essential geometric morphisms

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=10 "Edit section: Essential geometric morphisms")]

A geometric morphism (_u_∗,_u_∗) is _essential_ if _u_∗ has a further left adjoint _u_!, or equivalently (by the adjoint functor theorem) if _u_∗ preserves not only finite but all small limits.

### Ringed topoi

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=11 "Edit section: Ringed topoi")]

Main article: [Ringed topos](https://en.wikipedia.org/wiki/Ringed_topos "Ringed topos")

A **ringed topos** is a pair (_X_,_R_), where _X_ is a topos and _R_ is a commutative [ring object](https://en.wikipedia.org/wiki/Ring_object "Ring object") in _X_. Most of the constructions of [ringed spaces](https://en.wikipedia.org/wiki/Ringed_space "Ringed space") go through for ringed topoi. The category of [_R_-module](https://en.wikipedia.org/wiki/Module_(mathematics) "Module (mathematics)") objects in _X_ is an [abelian category](https://en.wikipedia.org/wiki/Abelian_category "Abelian category") with enough injectives. A more useful abelian category is the subcategory of [quasi-coherent](https://en.wikipedia.org/wiki/Coherent_sheaf "Coherent sheaf") _R_-modules: these are _R_-modules that admit a presentation.

Another important class of ringed topoi, besides ringed spaces, are the étale topoi of [Deligne–Mumford stacks](https://en.wikipedia.org/wiki/Algebraic_stack "Algebraic stack").

### Homotopy theory of topoi

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=12 "Edit section: Homotopy theory of topoi")]

[Michael Artin](https://en.wikipedia.org/wiki/Michael_Artin "Michael Artin") and [Barry Mazur](https://en.wikipedia.org/wiki/Barry_Mazur "Barry Mazur") associated to the site underlying a topos a [pro-simplicial set](https://en.wikipedia.org/wiki/Pro-simplicial_set "Pro-simplicial set") (up to [homotopy](https://en.wikipedia.org/wiki/Homotopy_category "Homotopy category")).[[5]](https://en.wikipedia.org/wiki/Topos#cite_note-5) (It's better to consider it in Ho(pro-SS); see Edwards) Using this [inverse system](https://en.wikipedia.org/wiki/Inverse_system "Inverse system") of simplicial sets one may _sometimes_ associate to a [homotopy invariant](https://en.wikipedia.org/wiki/Homotopy#Homotopy_invariance "Homotopy") in classical topology an inverse system of invariants in topos theory. The study of the pro-simplicial set associated to the étale topos of a scheme is called [étale homotopy theory](https://en.wikipedia.org/wiki/%C3%89tale_homotopy_theory "Étale homotopy theory").[[6]](https://en.wikipedia.org/wiki/Topos#cite_note-6) In good cases (if the scheme is [Noetherian](https://en.wikipedia.org/wiki/Noetherian_scheme "Noetherian scheme") and [geometrically unibranch](https://en.wikipedia.org/wiki/Geometrically_unibranch "Geometrically unibranch")), this pro-simplicial set is [pro-finite](https://en.wikipedia.org/wiki/Pro-finite "Pro-finite").

## Elementary topoi (topoi in logic)

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=13 "Edit section: Elementary topoi (topoi in logic)")]

### Introduction

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=14 "Edit section: Introduction")]

Since the early 20th century, the predominant axiomatic foundation of mathematics has been [set theory](https://en.wikipedia.org/wiki/Set_theory "Set theory"), in which all mathematical objects are ultimately represented by sets (including [functions](https://en.wikipedia.org/wiki/Function_(mathematics) "Function (mathematics)"), which map between sets). More recent work in category theory allows this foundation to be generalized using topoi; each topos completely defines its own mathematical framework. The category of sets forms a familiar topos, and working within this topos is equivalent to using traditional set-theoretic mathematics. But one could instead choose to work with many alternative topoi. A standard formulation of the [axiom of choice](https://en.wikipedia.org/wiki/Axiom_of_choice "Axiom of choice") makes sense in any topos, and there are topoi in which it is invalid. [Constructivists](https://en.wikipedia.org/wiki/Mathematical_constructivism "Mathematical constructivism") will be interested to work in a topos without the [law of excluded middle](https://en.wikipedia.org/wiki/Law_of_excluded_middle "Law of excluded middle"). If symmetry under a particular [group](https://en.wikipedia.org/wiki/Group_(mathematics) "Group (mathematics)") _G_ is of importance, one can use the topos consisting of all [_G_-sets](https://en.wikipedia.org/wiki/Group_action_(mathematics) "Group action (mathematics)").

It is also possible to encode an [algebraic theory](https://en.wikipedia.org/wiki/Universal_algebra "Universal algebra"), such as the theory of groups, as a topos, in the form of a [classifying topos](https://en.wikipedia.org/wiki/Classifying_topos "Classifying topos"). The individual models of the theory, i.e. the groups in our example, then correspond to [functors](https://en.wikipedia.org/wiki/Functor "Functor") from the encoding topos to the category of sets that respect the topos structure.

### Formal definition

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=15 "Edit section: Formal definition")]

When used for foundational work a topos will be defined axiomatically; set theory is then treated as a special case of topos theory. Building from category theory, there are multiple equivalent definitions of a topos. The following has the virtue of being concise:

A topos is a category that has the following two properties:

- All [limits](https://en.wikipedia.org/wiki/Limit_(category_theory) "Limit (category theory)") taken over finite index categories exist.
- Every object has a power object. This plays the role of the [powerset](https://en.wikipedia.org/wiki/Powerset "Powerset") in set theory.

Formally, a **power object** of an object X![[Mathematics/Library/_Attachments/927f5aa510997acca075e1f83541f321_MD5.svg]] is a pair (PX,∋X)![[8252316c8b6e04e0a1d982827703ba11_MD5.svg]] with ∋X⊆PX×X![[68daa32e2c97470ade5b2e631943c8ec_MD5.svg]], which classifies relations, in the following sense. First note that for every object I![[e08dc174d8938e02fcf3bfa6296178cd_MD5.svg]], a morphism r:I→PX![[4044c76348b4dcb5ed1d7fb2b3c84b24_MD5.svg]] ("a family of subsets") induces a subobject {(i,x) | x∈r(i)}⊆I×X![[4e3ca4fe87e65e4f1f8a5c74d07081ee_MD5.svg]]. Formally, this is defined by pulling back ∋X![[4a790bd2ec897e83b192827f80a613fd_MD5.svg]] along r×X:I×X→PX×X![[230bf11d33f510e706b252d74494835e_MD5.svg]]. The universal property of a power object is that every relation arises in this way, giving a bijective correspondence between relations R⊆I×X![[b4ddb7fc476dec71ac841ee0b9fcdade_MD5.svg]] and morphisms r:I→PX![[4044c76348b4dcb5ed1d7fb2b3c84b24_MD5.svg]].

From finite limits and power objects one can derive that

- All [colimits](https://en.wikipedia.org/wiki/Limit_(category_theory) "Limit (category theory)") taken over finite index categories exist.
- The category has a [subobject classifier](https://en.wikipedia.org/wiki/Subobject_classifier "Subobject classifier").
- The category is [Cartesian closed](https://en.wikipedia.org/wiki/Cartesian_closed_category "Cartesian closed category").

In some applications, the role of the subobject classifier is pivotal, whereas power objects are not. Thus some definitions reverse the roles of what is defined and what is derived.

### Logical functors

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=16 "Edit section: Logical functors")]

A _logical functor_ is a functor between topoi that preserves finite limits and power objects. Logical functors preserve the structures that topoi have. In particular, they preserve finite colimits, [subobject classifiers](https://en.wikipedia.org/wiki/Subobject_classifier "Subobject classifier"), and [exponential objects](https://en.wikipedia.org/wiki/Exponential_object "Exponential object").[[7]](https://en.wikipedia.org/wiki/Topos#cite_note-McLarty1992-7)

### Explanation

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=17 "Edit section: Explanation")]

A topos as defined above can be understood as a Cartesian closed category for which the notion of subobject of an object has an [elementary](https://en.wikipedia.org/wiki/First-order_logic "First-order logic") or first-order definition. This notion, as a natural categorical abstraction of the notions of [subset](https://en.wikipedia.org/wiki/Subset "Subset") of a set, [subgroup](https://en.wikipedia.org/wiki/Subgroup "Subgroup") of a group, and more generally [subalgebra](https://en.wikipedia.org/wiki/Subalgebra "Subalgebra") of any [algebraic structure](https://en.wikipedia.org/wiki/Algebraic_structure "Algebraic structure"), predates the notion of topos. It is definable in any category, not just topoi, in [second-order](https://en.wikipedia.org/wiki/Second-order_logic "Second-order logic") language, i.e. in terms of classes of morphisms instead of individual morphisms, as follows. Given two monics _m_, _n_ from respectively _Y_ and _Z_ to _X_, we say that _m_ ≤ _n_ when there exists a morphism _p_: _Y_ → _Z_ for which _np_ = _m_, inducing a [preorder](https://en.wikipedia.org/wiki/Preorder "Preorder") on monics to _X_. When _m_ ≤ _n_ and _n_ ≤ _m_ we say that _m_ and _n_ are equivalent. The subobjects of _X_ are the resulting equivalence classes of the monics to it.

In a topos "subobject" becomes, at least implicitly, a first-order notion, as follows.

As noted above, a topos is a category _C_ having all finite limits and hence in particular the empty limit or final object 1. It is then natural to treat morphisms of the form _x_: 1 → _X_ as _elements_ _x_ ∈ _X_. Morphisms _f_: _X_ → _Y_ thus correspond to functions mapping each element _x_ ∈ _X_ to the element _fx_ ∈ _Y_, with application realized by composition.

One might then think to define a subobject of _X_ as an equivalence class of monics _m_: _X′_ → _X_ having the same [image](https://en.wikipedia.org/wiki/Image_(mathematics) "Image (mathematics)") { _mx_ | _x_ ∈ _X′_ }. The catch is that two or more morphisms may correspond to the same function, that is, we cannot assume that _C_ is concrete in the sense that the functor _C_(1,-): _C_ → **Set** is faithful. For example the category **Grph** of [graphs](https://en.wikipedia.org/wiki/Multidigraph "Multidigraph") and their associated [homomorphisms](https://en.wikipedia.org/wiki/Homomorphism "Homomorphism") is a topos whose final object 1 is the graph with one vertex and one edge (a self-loop), but is not concrete because the elements 1 → _G_ of a graph _G_ correspond only to the self-loops and not the other edges, nor the vertices without self-loops. Whereas the second-order definition makes _G_ and the subgraph of all self-loops of _G_ (with their vertices) distinct subobjects of _G_ (unless every edge is, and every vertex has, a self-loop), this image-based one does not. This can be addressed for the graph example and related examples via the [Yoneda Lemma](https://en.wikipedia.org/wiki/Yoneda_Lemma "Yoneda Lemma") as described in the [Further examples](https://en.wikipedia.org/wiki/Topos#Further_examples) section below, but this then ceases to be first-order. Topoi provide a more abstract, general, and first-order solution.

[![[956c146eafe7422987b202f43eadbb72_MD5.png]]](https://en.wikipedia.org/wiki/File:SubobjectPullbackTopos.svg)

Figure 1. _m_ as a pullback of the generic subobject _t_ along _f_.

As noted above, a topos _C_ has a subobject classifier Ω, namely an object of _C_ with an element _t_ ∈ Ω, the _generic subobject_ of _C_, having the property that every [monic](https://en.wikipedia.org/wiki/Monomorphism "Monomorphism") _m_: _X′_ → _X_ arises as a pullback of the generic subobject along a unique morphism _f_: _X_ → Ω, as per Figure 1. Now the pullback of a monic is a monic, and all elements including _t_ are monics since there is only one morphism to 1 from any given object, whence the pullback of _t_ along _f_: _X_ → Ω is a monic. The monics to _X_ are therefore in bijection with the pullbacks of _t_ along morphisms from _X_ to Ω. The latter morphisms partition the monics into equivalence classes each determined by a morphism _f_: _X_ → Ω, the characteristic morphism of that class, which we take to be the subobject of _X_ characterized or named by _f_.

All this applies to any topos, whether or not concrete. In the concrete case, namely _C_(1,-) faithful, for example the category of sets, the situation reduces to the familiar behavior of functions. Here the monics _m_: _X′_ → _X_ are exactly the injections (one-one functions) from _X′_ to _X_, and those with a given image { _mx_ | _x_ ∈ _X′_ } constitute the subobject of _X_ corresponding to the morphism _f_: _X_ → Ω for which _f_−1(_t_) is that image. The monics of a subobject will in general have many domains, all of which however will be in bijection with each other.

To summarize, this first-order notion of subobject classifier implicitly defines for a topos the same equivalence relation on monics to _X_ as had previously been defined explicitly by the second-order notion of subobject for any category. The notion of equivalence relation on a class of morphisms is itself intrinsically second-order, which the definition of topos neatly sidesteps by explicitly defining only the notion of subobject _classifier_ Ω, leaving the notion of subobject of _X_ as an implicit consequence characterized (and hence namable) by its associated morphism _f_: _X_ → Ω.

### Further examples and non-examples

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=18 "Edit section: Further examples and non-examples")]

Every Grothendieck topos is an elementary topos, but the converse is not true (since every Grothendieck topos is cocomplete, which is not required from an elementary topos).

The categories of finite sets, of finite _G_-sets ([actions of a group](https://en.wikipedia.org/wiki/Group_action "Group action") _G_ on a finite set), and of finite graphs are elementary topoi that are not Grothendieck topoi.

If _C_ is a small category, then the [functor category](https://en.wikipedia.org/wiki/Functor_category "Functor category") **Set**_C_ (consisting of all covariant functors from _C_ to sets, with [natural transformations](https://en.wikipedia.org/wiki/Natural_transformation "Natural transformation") as morphisms) is a topos. For instance, the category **Grph** of graphs of the kind permitting multiple directed edges between two vertices is a topos. Such a graph consists of two sets, an edge set and a vertex set, and two functions _s,t_ between those sets, assigning to every edge _e_ its source _s_(_e_) and target _t_(_e_). **Grph** is thus [equivalent](https://en.wikipedia.org/wiki/Equivalent_categories "Equivalent categories") to the functor category **Set**_C_, where _C_ is the category with two objects _E_ and _V_ and two morphisms _s,t_: _E_ → _V_ giving respectively the source and target of each edge.

The [Yoneda lemma](https://en.wikipedia.org/wiki/Yoneda_lemma "Yoneda lemma") asserts that _C_op embeds in **Set**_C_ as a full subcategory. In the graph example the embedding represents _C_op as the subcategory of **Set**_C_ whose two objects are _V'_ as the one-vertex no-edge graph and _E'_ as the two-vertex one-edge graph (both as functors), and whose two nonidentity morphisms are the two graph homomorphisms from _V'_ to _E'_ (both as natural transformations). The natural transformations from _V'_ to an arbitrary graph (functor) _G_ constitute the vertices of _G_ while those from _E'_ to _G_ constitute its edges. Although **Set**_C_, which we can identify with **Grph**, is not made concrete by either _V'_ or _E'_ alone, the functor _U_: **Grph** → **Set**2 sending object _G_ to the pair of sets (**Grph**(_V'_ ,_G_), **Grph**(_E'_ ,_G_)) and morphism _h_: _G_ → _H_ to the pair of functions (**Grph**(_V'_ ,_h_), **Grph**(_E'_ ,_h_)) is faithful. That is, a morphism of graphs can be understood as a _pair_ of functions, one mapping the vertices and the other the edges, with application still realized as composition but now with multiple sorts of _generalized_ elements. This shows that the traditional concept of a concrete category as one whose objects have an underlying set can be generalized to cater for a wider range of topoi by allowing an object to have multiple underlying sets, that is, to be multisorted.

The category of [pointed sets](https://en.wikipedia.org/wiki/Pointed_set "Pointed set") with point-preserving functions is _not_ a topos, since it doesn't have power objects: if PX![[e92ce87c05b5c8f05b0142e9193ff150_MD5.svg]] were the power object of the pointed set X![[Mathematics/Library/_Attachments/927f5aa510997acca075e1f83541f321_MD5.svg]], and 1![[c53f6ab3c1688242ffd59990627cccf9_MD5.svg]] denotes the pointed singleton, then there is only one point-preserving function r:1→PX![[2d1092ec5c38c0dfd35a1e85d88f09f1_MD5.svg]], but the relations in 1×X![[f65ba044ce3d83a42b708eb18eba9cd7_MD5.svg]] are as numerous as the pointed subsets of X![[Mathematics/Library/_Attachments/927f5aa510997acca075e1f83541f321_MD5.svg]]. The [category of abelian groups](https://en.wikipedia.org/wiki/Category_of_abelian_groups "Category of abelian groups") is also not a topos, for a similar reason: every group homomorphism must map 0 to 0.

## See also

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=19 "Edit section: See also")]

- [![[d426ab780b20cd203fbe5032509f5c9d_MD5.png]]](https://en.wikipedia.org/wiki/File:Nuvola_apps_edu_mathematics_blue-p.svg)[Mathematics portal](https://en.wikipedia.org/wiki/Portal:Mathematics "Portal:Mathematics")

- [History of topos theory](https://en.wikipedia.org/wiki/History_of_topos_theory "History of topos theory")
- [Homotopy hypothesis](https://en.wikipedia.org/wiki/Homotopy_hypothesis "Homotopy hypothesis")
- [Intuitionistic type theory](https://en.wikipedia.org/wiki/Intuitionistic_type_theory "Intuitionistic type theory")
- [∞-topos](https://en.wikipedia.org/wiki/%E2%88%9E-topos "∞-topos")
- [Quasitopos](https://en.wikipedia.org/wiki/Quasitopos "Quasitopos")
- [Geometric logic](https://en.wikipedia.org/wiki/Geometric_logic "Geometric logic")
- [Generalized space](https://en.wikipedia.org/wiki/Generalized_space "Generalized space")

## Notes

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=20 "Edit section: Notes")]

1. **[^](https://en.wikipedia.org/wiki/Topos#cite_ref-Illusie2004_1-0 "Jump up")** [Illusie 2004](https://en.wikipedia.org/wiki/Topos#CITEREFIllusie2004)
2. **[^](https://en.wikipedia.org/wiki/Topos#cite_ref-2 "Jump up")** [Caramello, Olivia](https://en.wikipedia.org/wiki/Olivia_Caramello "Olivia Caramello") (2016). [_Grothendieck toposes as unifying 'bridges' in Mathematics_](https://www.oliviacaramello.com/Unification/HDROliviaCaramello.pdf) (PDF) (HDR). Paris Diderot University (Paris 7).
3. **[^](https://en.wikipedia.org/wiki/Topos#cite_ref-3 "Jump up")** Caramello, Olivia (2017). [_Theories, Sites, Toposes: Relating and studying mathematical theories through topos-theoretic 'bridges_](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198758914.001.0001/oso-9780198758914). Oxford University Press. [doi](https://en.wikipedia.org/wiki/Doi_(identifier) "Doi (identifier)"):[10.1093/oso/9780198758914.001.0001](https://doi.org/10.1093%2Foso%2F9780198758914.001.0001). [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [9780198758914](https://en.wikipedia.org/wiki/Special:BookSources/9780198758914 "Special:BookSources/9780198758914").
4. ^ [Jump up to:_**a**_](https://en.wikipedia.org/wiki/Topos#cite_ref-Caramel#_4-0) [_**b**_](https://en.wikipedia.org/wiki/Topos#cite_ref-Caramel#_4-1) Hoad, Phil (31 August 2024). ["'He was in mystic delirium': was this hermit mathematician a forgotten genius whose ideas could transform AI – or a lonely madman?"](https://www.theguardian.com/science/article/2024/aug/31/alexander-grothendieck-huawei-ai-artificial-intelligence). _[The Guardian](https://en.wikipedia.org/wiki/The_Guardian "The Guardian")_. Retrieved 17 September 2024.
5. **[^](https://en.wikipedia.org/wiki/Topos#cite_ref-5 "Jump up")** [Artin, Michael](https://en.wikipedia.org/wiki/Michael_Artin "Michael Artin"); [Mazur, Barry](https://en.wikipedia.org/wiki/Barry_Mazur "Barry Mazur") (1969). _Etale homotopy_. Lecture Notes in Mathematics. Vol. 100. [Springer-Verlag](https://en.wikipedia.org/wiki/Springer-Verlag "Springer-Verlag"). [doi](https://en.wikipedia.org/wiki/Doi_(identifier) "Doi (identifier)"):[10.1007/BFb0080957](https://doi.org/10.1007%2FBFb0080957). [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-3-540-36142-8](https://en.wikipedia.org/wiki/Special:BookSources/978-3-540-36142-8 "Special:BookSources/978-3-540-36142-8").
6. **[^](https://en.wikipedia.org/wiki/Topos#cite_ref-6 "Jump up")** [Friedlander, Eric M.](https://en.wikipedia.org/wiki/Eric_Friedlander "Eric Friedlander") (1982), _Étale homotopy of simplicial schemes_, Annals of Mathematics Studies, vol. 104, [Princeton University Press](https://en.wikipedia.org/wiki/Princeton_University_Press "Princeton University Press"), [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-0-691-08317-9](https://en.wikipedia.org/wiki/Special:BookSources/978-0-691-08317-9 "Special:BookSources/978-0-691-08317-9")
7. **[^](https://en.wikipedia.org/wiki/Topos#cite_ref-McLarty1992_7-0 "Jump up")** [McLarty 1992](https://en.wikipedia.org/wiki/Topos#CITEREFMcLarty1992), p. [159](https://books.google.com/books?id=V8cON1x39bIC&dq=%22Logical+functor%22)

## References

[[edit](https://en.wikipedia.org/w/index.php?title=Topos&action=edit&section=21 "Edit section: References")]

Some gentle papers

- Edwards, D.A.; Hastings, H.M. (Summer 1980). ["Čech Theory: its Past, Present, and Future"](https://projecteuclid.org/journals/rocky-mountain-journal-of-mathematics/volume-10/issue-3/Cech-Theory-Its-past-present-and-future/10.1216/RMJ-1980-10-3-429.pdf) (PDF). _Rocky Mountain Journal of Mathematics_. **10** (3): 429–468. [doi](https://en.wikipedia.org/wiki/Doi_(identifier) "Doi (identifier)"):[10.1216/RMJ-1980-10-3-429](https://doi.org/10.1216%2FRMJ-1980-10-3-429). [JSTOR](https://en.wikipedia.org/wiki/JSTOR_(identifier) "JSTOR (identifier)") [44236540](https://www.jstor.org/stable/44236540).
- [Baez, John](https://en.wikipedia.org/wiki/John_Baez "John Baez"). ["Topos theory in a nutshell"](http://math.ucr.edu/home/baez/topos.html). A gentle introduction.
- [Steven Vickers](https://en.wikipedia.org/wiki/Steve_Vickers_(computer_scientist) "Steve Vickers (computer scientist)"): "[Toposes pour les nuls](http://www.cs.bham.ac.uk/~sjv/papers.php)" and "[Toposes pour les vraiment nuls.](http://www.cs.bham.ac.uk/~sjv/TopPLVN.pdf)" Elementary and even more elementary introductions to toposes as generalized spaces.
- [Illusie, Luc](https://en.wikipedia.org/wiki/Luc_Illusie "Luc Illusie") (2004). ["What is...A Topos?"](http://www.ams.org/notices/200409/what-is-illusie.pdf) (PDF). _Notices of the AMS_. **51** (9): 160–1.

The following texts are easy-paced introductions to toposes and the basics of category theory. They should be suitable for those knowing little mathematical logic and set theory, even non-mathematicians.

- [Lawvere, F. William](https://en.wikipedia.org/wiki/F._William_Lawvere "F. William Lawvere"); Schanuel, Stephen H. (1997). [_Conceptual Mathematics: A First Introduction to Categories_](https://books.google.com/books?id=o1tHw4W5MZQC). Cambridge University Press. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-0-521-47817-5](https://en.wikipedia.org/wiki/Special:BookSources/978-0-521-47817-5 "Special:BookSources/978-0-521-47817-5"). An "introduction to categories for computer scientists, logicians, physicists, linguists, etc." (cited from cover text).
- Lawvere, F. William; Rosebrugh, Robert (2003). [_Sets for Mathematics_](https://archive.org/details/setsformathemati0000lawv). Cambridge University Press. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-0-521-01060-3](https://en.wikipedia.org/wiki/Special:BookSources/978-0-521-01060-3 "Special:BookSources/978-0-521-01060-3"). Introduces the foundations of mathematics from a categorical perspective.

Grothendieck foundational work on topoi:

- [Grothendieck, A.](https://en.wikipedia.org/wiki/Grothendieck "Grothendieck"); [Verdier, J.L.](https://en.wikipedia.org/wiki/Jean-Louis_Verdier "Jean-Louis Verdier") (1972). _Théorie des Topos et Cohomologie Etale des Schémas_. Lecture notes in mathematics. Vol. 269. Springer. [doi](https://en.wikipedia.org/wiki/Doi_(identifier) "Doi (identifier)"):[10.1007/BFb0081551](https://doi.org/10.1007%2FBFb0081551). [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-3-540-37549-4](https://en.wikipedia.org/wiki/Special:BookSources/978-3-540-37549-4 "Special:BookSources/978-3-540-37549-4"). _Tome 2_ **270** [doi](https://en.wikipedia.org/wiki/Doi_(identifier) "Doi (identifier)"):[10.1007/BFb0061319](https://doi.org/10.1007%2FBFb0061319) [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-3-540-37987-4](https://en.wikipedia.org/wiki/Special:BookSources/978-3-540-37987-4 "Special:BookSources/978-3-540-37987-4")

The following monographs include an introduction to some or all of topos theory, but do not cater primarily to beginning students. Listed in (perceived) order of increasing difficulty.

- [McLarty, Colin](https://en.wikipedia.org/wiki/Colin_McLarty "Colin McLarty") (1992). [_Elementary Categories, Elementary Toposes_](https://books.google.com/books?id=V8cON1x39bIC). Clarendon Press. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-0-19-158949-2](https://en.wikipedia.org/wiki/Special:BookSources/978-0-19-158949-2 "Special:BookSources/978-0-19-158949-2"). A nice introduction to the basics of category theory, topos theory, and topos logic. Assumes very few prerequisites.
- [Goldblatt, Robert](https://en.wikipedia.org/wiki/Robert_Goldblatt "Robert Goldblatt") (2013) [1984]. [_Topoi: The Categorial Analysis of Logic_](https://books.google.com/books?id=hLPDAgAAQBAJ). Courier Corporation. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-0-486-31796-0](https://en.wikipedia.org/wiki/Special:BookSources/978-0-486-31796-0 "Special:BookSources/978-0-486-31796-0"). A good start. Available [online](http://historical.library.cornell.edu/cgi-bin/cul.math/docviewer?did=Gold010&id=3) at [Robert Goldblatt's homepage.](http://www.mcs.vuw.ac.nz/~rob/)
- [Bell, John L.](https://en.wikipedia.org/wiki/John_Lane_Bell "John Lane Bell") (2001). ["The Development of Categorical Logic"](https://books.google.com/books?id=yObMqG9EcCEC&pg=PA279). In Gabbay, D.M.; Guenthner, Franz (eds.). _Handbook of Philosophical Logic_. Vol. 12 (2nd ed.). Springer. pp. 279–. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-1-4020-3091-8](https://en.wikipedia.org/wiki/Special:BookSources/978-1-4020-3091-8 "Special:BookSources/978-1-4020-3091-8"). Version available [online](http://publish.uwo.ca/~jbell/catlogprime.pdf) at [John Bell's homepage.](http://publish.uwo.ca/~jbell/)
- [MacLane, Saunders](https://en.wikipedia.org/wiki/Saunders_Mac_Lane "Saunders Mac Lane"); [Moerdijk, Ieke](https://en.wikipedia.org/wiki/Ieke_Moerdijk "Ieke Moerdijk") (2012) [1994]. [_Sheaves in Geometry and Logic: A First Introduction to Topos Theory_](https://books.google.com/books?id=LZWLBAAAQBAJ). Springer. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-1-4612-0927-0](https://en.wikipedia.org/wiki/Special:BookSources/978-1-4612-0927-0 "Special:BookSources/978-1-4612-0927-0"). More complete, and more difficult to read.
- [Barr, Michael](https://en.wikipedia.org/wiki/Michael_Barr_(mathematician) "Michael Barr (mathematician)"); [Wells, Charles](https://en.wikipedia.org/wiki/Charles_Wells_(mathematician) "Charles Wells (mathematician)") (2013) [1985]. [_Toposes, Triples and Theories_](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html). Springer. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-1-4899-0023-4](https://en.wikipedia.org/wiki/Special:BookSources/978-1-4899-0023-4 "Special:BookSources/978-1-4899-0023-4"). (Online version). More concise than _Sheaves in Geometry and Logic_, but hard on beginners.

Reference works for experts, less suitable for first introduction

- Edwards, D.A.; Hastings, H.M. (1976). _Čech and Steenrod homotopy theories with applications to geometric topology_. Lecture Notes in Maths. Vol. 542. Springer-Verlag. [doi](https://en.wikipedia.org/wiki/Doi_(identifier) "Doi (identifier)"):[10.1007/BFb0081083](https://doi.org/10.1007%2FBFb0081083). [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-3-540-38103-7](https://en.wikipedia.org/wiki/Special:BookSources/978-3-540-38103-7 "Special:BookSources/978-3-540-38103-7").
- Borceux, Francis (1994). [_Handbook of Categorical Algebra: Volume 3, Sheaf Theory_](https://books.google.com/books?id=7jgots78faUC). Encyclopedia of Mathematics and its Applications. Vol. 52. Cambridge University Press. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-0-521-44180-3](https://en.wikipedia.org/wiki/Special:BookSources/978-0-521-44180-3 "Special:BookSources/978-0-521-44180-3"). The third part of "Borceux' remarkable magnum opus", as Johnstone has labelled it. Still suitable as an introduction, though beginners may find it hard to recognize the most relevant results among the huge amount of material given.
- [Johnstone, Peter T.](https://en.wikipedia.org/wiki/Peter_Johnstone_(mathematician) "Peter Johnstone (mathematician)") (2014) [1977]. [_Topos Theory_](https://books.google.com/books?id=zO8WAgAAQBAJ). Courier. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-0-486-49336-7](https://en.wikipedia.org/wiki/Special:BookSources/978-0-486-49336-7 "Special:BookSources/978-0-486-49336-7"). For a long time the standard compendium on topos theory. However, even Johnstone describes this work as "far too hard to read, and not for the faint-hearted."
- Johnstone, Peter T. (2002). [_Sketches of an Elephant: A Topos Theory Compendium_](https://books.google.com/books?id=TLHfQPHNs0QC). Vol. 2. Clarendon Press. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-0-19-851598-2](https://en.wikipedia.org/wiki/Special:BookSources/978-0-19-851598-2 "Special:BookSources/978-0-19-851598-2"). As of early 2010, two of the scheduled three volumes of this overwhelming compendium were available.
- Caramello, Olivia (2017). [_Theories, Sites, Toposes: Relating and studying mathematical theories through topos-theoretic 'bridges_](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198758914.001.0001/oso-9780198758914). Oxford University Press. [doi](https://en.wikipedia.org/wiki/Doi_(identifier) "Doi (identifier)"):[10.1093/oso/9780198758914.001.0001](https://doi.org/10.1093%2Foso%2F9780198758914.001.0001). [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [9780198758914](https://en.wikipedia.org/wiki/Special:BookSources/9780198758914 "Special:BookSources/9780198758914").

Books that target special applications of topos theory

- Pedicchio, Maria Cristina; Tholen, Walter; Rota, G.C., eds. (2004). [_Categorical Foundations: Special Topics in Order, Topology, Algebra, and Sheaf Theory_](https://books.google.com/books?id=WHudOFwuMn8C). Encyclopedia of Mathematics and its Applications. Vol. 97. Cambridge University Press. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier) "ISBN (identifier)") [978-0-521-83414-8](https://en.wikipedia.org/wiki/Special:BookSources/978-0-521-83414-8 "Special:BookSources/978-0-521-83414-8"). Includes many interesting special applications.