[[!include contents]]

#Idea#
Category theory was invented by Samuel Eilenberg and Saunders Mac Lane in the 1945 paper **General theory of natural equivalences**. The reason was to introduce functors, and the reason to introduced functors was to introduce natural transformations (more specifically natural equivalences) to define what natural means in mathematics. So the idea is to shift from the study of objects to the study of functions between objects (more precisely morphisms). Another reason was the need to find a common language that would unify and simplify many advances in the 1930's. Considering how many different categories there are one can now do things once and for all in general instead of in each category separately. The paper was a clash of ideas from abstract algebra (Mac Lane) and topology (Eilenberg). It was first rejected on the ground that it had no content but was later published. Unexpectedly category theory has flourished into almost all areas of mathematics, has found many applications outside mathematics and even attempts to build a foundation of mathematics. Category theory is very abstract but of course it is not abstract nonsense as some joke about it.

#What is category theory?#
**Category theory** is so useful because it can be seen from so many perspectives.

* The theory of [[category|categories]] as [[essentially algebraic theory|essentially algebraic structures]] with several objects and a relation (morphism) "algebra" on these objects. Structures in ordinary [[algebraic theory|abstract algebra]], like [[monoid]]s, have only one object. This theory also include [[functor]]s between categories and [[natural transformation]]s.
* The theory of categories as primitive mathematical [[universe]]s or [[space]]s (nothing as fancy as a [[topos]]).
* A unifying tool and language in [[mathematics]].
* A top-down [[foundations|foundation of mathematics]] (that is structural and more than just type theories).
* An abstraction of an abstraction of an abstraction of .... The first level is [[set]]s and is most concrete. This is abstracted to categories (only some categories are categories of sets, hence the abstraction). The next abstraction is to categories of categories or more generally $2$-[[2-category|categories]]. This can be iterated to $n$-[[n-category|categories]] and [[infinity-category|indefinitely]]. This could be called the theory of abstractions.
* A description of partial [[symmetry|symmetries]], in the sense that [[group]]s describe symmetries.
* A generalized theory of [[representations]]. In this view every functor is a representation of its domain in its codomain and natural transformations are the [[intertwining operator]]s between representations.
* The theory of combinatorial [[directed graph|directed multipseudographs]] with a [[composition]] law. This have given rise to the heavy use of a "diagramatic language" in category theory.
* A theory of [[type theory|type theories]]. There is a bijection between categories and type theories.
* A theory of [[deductive system]]s. There is a bijection between categories and deductive systems.

#Branches of category theory#
A probably incomplete list is:

* Pure category theory (vaguely category theory without the use of any other branches of mathematics except essential concepts from them).
* Categorical abstract algebra, including [[representation theory]] of abstract algebraic structures and [[universal algebra]].
* [[homologica algebra|Homological algebra]].
* [[homotopical algebra|Homotopical algebra]].
* Topology using categories. It includes [[algebraic topology]], [[categorical topology]] (see [[topological concrete category]] for a bit of this), [[quantum topology]], [[low-dimensional topology]].
* [[internal logic|Categorical logic]] and [[set theory]] in the category-theoretic context such as [[algebraic set theory]].
* [[foundations|Foundations]] of mathematics building on categories, for instance [[topos theory]].
* Abstract [[geometry]], including [[algebraic geometry]] on the level of schemes and above, categorical [[noncommutative geometry]], different categorifications of [[differential geometry]], etc. 
* [[categorical quantization|Categorical quantization]] (in mathematics).
* [[applied category theory|Applied category theory]]. Especially to mathematical [[physics]], [[computer science]] and [[dynamic system]]s (categorical dynamics).

Most of these include some [[higher category theory]]. Some would define category theory as the human activity of [[category theorists]].

#Contrast with set theory#
Here set theory is assumed to be a theory of the usual concept of sets. No one of these is more fundamental than the other. Category theory is a holistic (structural) approach to mathematics that can by [[Algebraic set theory]] reproduce all the different axiomatic set theories and do not need the concept of set to be formulated. Set theory is an analytic approach (elementwise) that can reproduce category theory by Lawvere's [[Elementary theory of abstract categories]]. Lawvere also pointed out that set theory is axiomatized by a binary membership relation while category theory is axiomatized by a ternary composition relation.

For more on this and for the many different generalized sets see

* Sets, categories and structuralism - Costas Drossos

+--{.query}
Rafael: I am a bit skeptical if to interpret ETAC as a set theory.
=--

#Literature#
* Categories for the working mathematician 2'nd ed. - Saunders Mac Lane
* Categories for everybody- Steve Awodey
* Handbook of categorical algebra vol 1-3 - Francis Borceux
* Categories and sheaves - Masaki Kashiwara and Pierre Schapira
* Elementary categories, elementary toposes - Collin McLarty
* Abstract and concrete categories - the joy of cats - Jiri Adamek, Horst Herrlich, George Strecker


#Category theory entries#
* [[(-1)-category]]
* [[2-morphism]]
* [[adjoint functor]]
* [[anafunctor]]
* [[braided monoidal category]]
* [[cartesian monoidal category]]
* [[category]]
* [[category algebra]]
* [[category theory]]
* [[composition]]
* [[diagram]]
* [[dichotomy between nice objects and nice categories]]
* [[directed graph]]
* [[directed n-graph]]
* [[discrete category]]
* [[duality]]
* [[enriched category]]
* [[enriched category theory]]
* [[epimorphism]]
* [[equality]]
* [[equivalence]]
* [[equivalence of categories]]
* [[essentially surjective functor]]
* [[extensive category]]
* [[faithful functor]]
* [[folk model structure]]
* [[forgetful functor]]
* [[foundations]]
* [[full functor]]
* [[full subcategory]]
* [[function]]
* [[functor]]
* [[functor category]]
* [[fundamental groupoid]]
* [[global element]]
* [[globe]]
* [[globular set]]
* [[group]]
* [[group theory]]
* [[groupoid]]
* [[groupoid cardinality]]
* [[higher category theory]]
* [[homotopy theory]]
* [[hom-set]]
* [[horizontal categorification]]
* [[identity morphism]]
* [[image]]
* [[infinity-groupoid]]
* [[infinity-stack]]
* [[internal category]]
* [[internalization]]
* [[isomorphism]]
* [[large category]]
* [[limit]]
* [[locally small category]]
* [[monoid]]
* [[monoidal category]]
* [[morphism]]
* [[multicategory]]
* [[natural isomorphism]]
* [[natural transformation]]
* [[object]]
* [[omega-graph]]
* [[oriental]]
* [[partial order]]
* [[preorder]]
* [[quiver]]
* [[quiver algebra]]
* [[regular epimorphism]]
* [[Rel]]
* [[semi-strict infinity-category]]
* [[set]]
* [[skeleton]]
* [[small category]]
* [[source]]
* [[subcategory]]
* [[symmetric monoidal category]]
* [[target]]
* [[tensor product]]
* [[terminal object]]
* [[topos]]
* [[vertical categorification]]

+--{.query}
Wouldn\'t it be simpler to list the entries that *aren\'t* related to category theory?

[[Urs Schreiber|Urs]] says: I do this for the following reasons: 

a) I want eventually all the encyclopedic entries on the $n$Lab to be listed in the main headline entries such as [[sheaf and topos theory]] so that people can efficiently see which information exists on the $n$Lab and search for keywords.

b) I expect that eventually pure category theoretic definitions will not dominate the $n$Lab entries. Currently they clearly do, since we found ourselves explaining things from the bottom up. But as soon as we start working more seriously on more specialized topics, for instance on the [[physics]] and [[philosophy]] sections pure category theoretic entries will become the minority. Clearly, I think, we don't want the $n$Lab to be or remain a _just_ category theory dictionary.

Toby: I see, this list is only for such dictionary-like terms, not for everything that uses category theory in some way (which I think probably *will* continue to be most). But we can make it shorter by, say, removing everything that\'s about [[higher category theory]] and making a single link to that (just as we don\'t list everything under [[mathematics]]).

[[Urs Schreiber|Urs]]: Sure, whatever works best for us. I see that this list here is getting a bit out of control, but it is part of my general attempt to keep the entries we build listed alphabetically in the main index pages, so to allow at least some sort of global picture of the state of the wiki. The best solution would be some automatically created list. Hm, now that I say this: we should maybe start adding "catgegory: xyz"-labels to the entries, where "xyz" is one of the headline items. Hm...
=--