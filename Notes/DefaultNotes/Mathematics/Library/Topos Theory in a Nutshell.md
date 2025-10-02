
---

## Topos Theory in a Nutshell

#### John Baez

#### October 10, 2021

Okay, you wanna know what a topos is? First I'll give you a hand-wavy vague explanation, then an actual definition, then a few consequences of this definition, and then some examples. Finally I'll tell you some more things to read.

I'll warn you: it takes a lot of work to learn enough topos theory to really _use it to solve problems_. Thus, when you're getting started the main reason to learn about it should not be to quickly solve some specific problems, but to broaden your horizons and break out of the box that traditional mathematics, based on set theory, imposes on your thinking.

### 1. Hand-Wavy Vague Explanation

Around 1963, Bill Lawvere decided to figure out new foundations for mathematics, based on category theory. His idea was to figure out what was so great about sets, strictly from the _category-theoretic_ point of view. This is an interesting project, since category theory is all about objects and morphisms. For the category of sets, this means _sets_ and _functions_. Of course, the usual axioms for set theory are all about _sets_ and _membership_. Thus analyzing set theory from the category-theoretic viewpoint forces a radical change of viewpoint, which downplays membership and emphasizes functions.

In the spring of 1966 Lawvere encountered the work of Alexander Grothendieck, who had invented a concept of "topos" in his work on algebraic geometry. The word "topos" means "place" in Greek. In algebraic geometry we are often interested not just in whether or not something is true, but in _where_ it is true. For example, given two functions on a space, where are they equal? Grothendieck thought about this very hard and invented his concept of topos, which is roughly _a category that serves as a place in which one can do mathematics_.

Ultimately, this led to a concept of truth that has a very general notion of "space" built into it!

By 1971, Lawvere and Myles Tierney had taken Grothendieck's original concept of topos — now called a "Grothendieck topos" — generalized and distilled it, and come up with the concept of topos I'll talk about here. This is sometimes called an "elementary topos", to distinguish it from Grothendieck's notion... but often it's just called a _topos_, and that's what I'll do.

So what is a topos?

A topos is category with certain extra properties that make it a lot like the category of sets. There are many different topoi; you can do a lot of the same mathematics in all of them; but there are also many differences between them. For example, the axiom of choice need not hold in a topos, and the law of the excluded middle ("either P or not(P)") need not hold. The reason is that truth is not a yes-or-no affair: instead, we keep track of "how" true statements are, or more precisely _where_ they are true. Some but not all topoi contain a "natural numbers object", which plays the role of the natural numbers.

But enough hand-waving. Let's see precisely what a topos is.

### 2. Definition

There are various equivalent definitions of a topos, some more terse than others. Here is a rather inefficient one:

A topos is a category with:

**A)** finite limits and colimits,

**B)** exponentials,

**C)** a subobject classifier.

It's not too long! But it could be made even shorter: we don't need to mention colimits, since that follows from the rest.

### 3. Some Consequences of the Definition

Unfortunately, if you don't know some category theory, the above definition will be mysterious and will require a further sequence of definitions to bring it back to the basic concepts of [category theory](https://math.ucr.edu/home/baez/categories.html) — object, morphism, composition, identity. Instead of doing all that, let me say a bit about what these items A)-C) amount to in the category of sets:

**A)** says that there are:

- an initial object (an object like the empty set)
- a terminal object (an object like a set with one element)
- binary coproducts (something like the disjoint union of two sets)
- binary products (something like the Cartesian product of two sets)
- equalizers (something like the subset of X consisting of all elements x such that f(x) = g(x), where f,g: X → Y)
- coequalizers (something like the quotient set of X where two elements f(y) and g(y) are identified, where f,g: Y → X)

In fact A) is equivalent to all this stuff. However, I should emphasize that A) says all this in an elegant unified way; it's a theorem that this elegant way is the same as all the crud I just listed.

**B)** says that for any objects X and Y, there is an object YX, called an "exponential", which acts like "the set of functions from X to Y".

**C)** says that there is an object called the "subobject classifier", Ω, which acts like the two-element set {0,1}. In the category of sets we use {0,1} as our set of "truth values". In particular, functions f: X → {0,1} are secretly the same as subsets of X. Similarly, for any object X in a topos, morphisms f: X → Ω are secretly the same as "subobjects" of X.

Learning more about all these concepts is probably the best use of your time if you wants to learn a little bit of topos theory. Even if you can't remember what a topos is, these concepts can help you become a stronger mathematician or mathematical physicist!

### 4. Examples

Suppose you're an old fuddy-duddy. Then you want to work in the topos Set, where the objects are sets and the morphisms are functions.

Suppose you know the symmetry group of the universe, G. And suppose you only want to work with sets on which this symmetry group acts, and functions which are compatible with this group action. Then you want to work in the topos G-Set.

Suppose you have a topological space that you really like. Then you might want to work in the topos of presheaves on X, or the topos of sheaves on X. Sheaves are important in twistor theory and other applications of algebraic geometry and topology to physics.

Generalizing the last two examples, you might prefer to work in the topos of presheaves on an arbitrary category C, also known as hom(Cop, Set).

For example, if C = Δ (the category of nonempty finite totally ordered sets), a presheaf on Δ is a simplicial set. Algebraic topologists love to work with these, and physicists need more and more algebraic topology these days, so as we grow up, eventually it pays to learn how to do algebraic topology using the category of simplicial sets, hom(Δop, Set).

Or, you might like to work in the topos of [sheaves](http://en.wikipedia.org/wiki/Sheaf_%28mathematics%29) on a topological space — or even on a "site", which is a category equipped with something like a topology. These ideas were invented by [Grothendieck](http://en.wikipedia.org/wiki/Grothendieck) as part of his strategy for proving the [Weil conjectures](http://en.wikipedia.org/wiki/Weil_conjectures). In fact, this is how topos theory got started. And the power of these ideas continues to grow. For example, in 2002, [Vladimir Voevodsky](http://en.wikipedia.org/wiki/Vladimir_Voevodsky) won the Fields medal for cracking a famous problem called [Milnor's Conjecture](http://www.ams.org/bull/1998-35-02/S0273-0979-98-00745-9/home.html) with the help of "simplicial sheaves". These are like simplicial sets, but with sets replaced by sheaves on a site. Again, they form a topos. Zounds!

But if all this sounds too terrifying, never mind - there are also examples with a more "foundational" flavor:

Suppose you're a finitist and you only want to work with finite sets. Then you want to work in the topos of finite sets, and functions between those. In topos theory, the infinite is not "built in" — it's an extra feature you can add if you want.

Suppose you're a constructivist and you only want to work with "effectively constructible" sets and "effectively computable" functions. Then you want to work in the "effective topos" developed by Martin Hyland.

Suppose you like doing calculus with infinitesimals, the way physicists do all the time — but you want to do it rigorously. Then you want to work in the "smooth topos" developed by Lawvere and Anders Kock.

Or suppose you're very concerned with the time of day, and you want to work with time-dependent sets and time-dependent functions between them. Then there's a topos for you — I don't know a spiffy name for it, but it exists: an object gives you a set S(t) for each time t, and a morphism gives you a function f(t): S(t) → T(t) for each time t. This too gives a topos!

People often go a bit further, and work with a topos where an object S consists of a set S(t) for each time t and a function St,t' : S(t) → S(t') whenever t ≤ t'. The idea here is that as time goes by you can learn new elements are in your set, or learn that two elements are equal, so you get a map from S(t) to S(t'). I'll let you guess what the morphisms should be in this topos.

There are lots of topoi! You can hand-craft them to your specific needs.

### 5. For more

If you want to learn more about topos theory, this could be the easiest place to start:

- F. William Lawvere and Steve Schanuel, _Conceptual Mathematics: A First Introduction to Categories_, Cambridge U. Press, Cambridge, 1997.

It may seem almost childish at first, but it gradually creeps up on you. Schanuel has told me that you _must_ do the exercises — if you don't, at some point the book will suddenly switch from being too easy to being way too hard! If you stick with it, by the end you will have all the basic concepts from topos theory under your belt, almost subconsciously.

After that, try this one:

- F. William Lawvere and Robert Rosebrugh, _Sets for Mathematics_, Cambridge U. Press, Cambridge, 2003.

This is a great introduction to category theory via the topos of sets: it describes ordinary set theory in topos-theoretic terms, making it clear which axioms will be dropped when we go to more general topoi, and why. It goes a lot further than the previous book, and you need some more sophistication to follow it, but it's still written for the beginner.

I got a lot out of the following book:

- Robert Goldblatt, _[Topoi, the Categorial Analysis of Logic.](http://projecteuclid.org/euclid.bia/1403013939#toc)_ Also available from [Dover Publications](http://store.doverpublications.com/0486450260.html).

Don't be scared by the title: it starts at the beginning and explains categories before going on to topoi and their relation to logic. In fact, many toposophers complain that it's not substantial enough — it shows how topoi illuminate concepts from logic, but it doesn't show you can _do lots of cool stuff_ with topoi. But for beginners, this is probably just fine!

When you want to dig deeper, try this:

- Tom Leinster, [An informal introduction to topos theory](https://arxiv.org/abs/1012.5647).

It's a "short expository text for readers who are confident in basic category theory but know little or nothing about toposes". Then try this:

- Saunders Mac Lane and Ieke Moerdijk, _Sheaves in Geometry and Logic: a First Introduction to Topos Theory_, Springer, New York, 1992.

or this:

- Colin McLarty, _Elementary Categories, Elementary Toposes,_ Clarendon Press, Oxford, 1995.

Mac Lane and Moerdijk's book is both broad and deep, explaining in great detail how topos theory unifies logic and geometry. McLarty's is shorter, more laconic, and focused strongly on logic. If you want to hear McLarty talk in a less technical way about the big picture of topos theory, I highly recommend this:

- Colin McLarty, [The uses and abuses of the history of topos theory](https://web.archive.org/web/20180519003037/https://case.edu/artsci/phil/UsesandAbuses%20HistoryToposTheory.pdf), _Brit. J. Phil. Sci._ **41** (1990), 351–375.

He complains about the misperception, common among logicians, that topos theory arose as an attempt to generalize set theory:

> Category theory arose from a complicated array of practical problems in topology. Topos theory arose from Grothendieck's work in geometry, Tierney's interest in topology and Lawvere's interest in the foundations of physics. The two subjects are typical in this regard. An important mathematical concept will rarely arise from generalizing one earlier concept. More often it will arise from attempts to unify, explain, or deal with a mass of earlier concepts and problems. It becomes important because it makes things _easier_, so that an accurate historical treatment would begin at the hardest point. I will sketch a more accurate history of categories and toposes and show some ways the common sense history obscures their content and especially obscures categorical foundations for mathematics. Yet I doubt the more accurate history will help beginners learn category theory. I conclude with a more broadly falsified history that could help introduce the subject.

And after that... well, let's not rush this! For example, this classic is now available for free online:

- Michael Barr and Charles Wells, [_Toposes, Triples and Theories_](http://www.cwru.edu/artsci/math/wells/pub/ttt.html).

but it's advanced enough to make any beginner run away screaming! I love it now, but that took years.

These books are bound to have a similar effect:

- Peter Johnstone, _Topos Theory_, London Mathematical Society Monographs 10, Academic Press, 1977.
    
- Peter Johnstone, _Sketches of an Elephant: a Topos Theory Compendium_, Oxford U. Press, Oxford. Volume 1, comprising Part A: Toposes as Categories, and Part B: 2-categorical Aspects of Topos Theory, 720 pages, published in 2002. Volume 2, comprising Part C: Toposes as Spaces, and Part D: Toposes as Theories, 880 pages, published in 2002. Volume 3, comprising Part E: Homotopy and Cohomology, and Part F: Toposes as Mathematical Universes, in preparation.

... but once you get deeper into topos theory, you'll see they contain a massive hoard of wisdom. I'm trying to read them now. McLarty has said that you can tell you _really_ understand topoi if you can follow Johnstone's classic _Topos Theory_. It's long been the key text on the subject, but as a referee of his new trilogy wrote, it was "far too hard to read, and not for the faint-hearted". His _Sketches of an Elephant_ spend more time explaining things, but they're so packed with detailed information that nobody unfamiliar with topos theory would have a chance of seeing the forest for the trees. Also, they assume a fair amount of category theory. But they're great!

---

_Mathematics is not the rigid and rigidity-producing schema that the layman thinks it is; rather, in it we find ourselves at that meeting point of constraint and freedom that is the very essence of human nature._ — Hermann Weyl

© 2021 John Baez  
baez@math.removethis.ucr.andthis.edu

### [home](https://math.ucr.edu/home/baez/README.html)