[[!include contents]]

#Idea#
Category theory was invented by Samuel Eilenberg and Saunders Mac Lane in the 1945 paper **General theory of natural equivalences**. The reason was to introduce functors, and the reason to introduced functors was to introduce natural transformations (more specifically natural equivalences) to define what natural means in mathematics. So the idea is to shift from the study of objects to the study of functions between objects (more precisely morphisms). Another reason was the need to find a common language that would unify and simplify many advances in the 1930's. Considering how many different categories there are one can now do things once and for all in general instead of in each category separately. The paper was a clash of ideas from abstract algebra (Mac Lane) and topology (Eilenberg). It was first rejected on the ground that it had no content but was later published. Unexpectedly category theory has flourished into almost all areas of mathematics, has found many applications outside mathematics and even attempts to build a foundation of mathematics. Category theory is very abstract but of course it is not abstract nonsense as some joke about it.

#What is category theory?#
**Category theory** is so useful because it can be seen from so many perspectives.

* The theory of [[category|categories]] as [[essentially algebraic theory|essentially algebraic structures]] with several objects and a relation (morphism) "algebra" on these objects. Structures in ordinary [[algebraic theory|abstract algebra]], like [[monoid]]s, have only one object. This theory also include [[functor]]s between categories and [[natural transformation]]s.
* The theory of categories as primitive mathematical [[universe]]s or [[space]]s (nothing as fancy as a [[topos]]).

+--{.query}
Rafael: Preferrably as some 1D CW-complex that i am trying to figure out. Can someone fill that in.
=--

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
* [[homological algebra|Homological algebra]].
* [[homotopical algebra|Homotopical algebra]].
* Topology using categories. It includes [[algebraic topology]], [[categorical topology]] (see [[topological concrete category]] for a bit of this), [[quantum topology]], [[low-dimensional topology]].
* [[internal logic|Categorical logic]] and [[set theory]] in the category-theoretic context such as [[algebraic set theory]].
* [[foundations|Foundations]] of mathematics building on categories, for instance [[topos theory]].
* Abstract [[geometry]], including [[algebraic geometry]] on the level of schemes and above, categorical [[noncommutative geometry]], different categorifications of [[differential geometry]], etc. 
* [[categorical quantization|Categorical quantization]] (in mathematics).
* [[applied category theory|Applied category theory]]. Especially to mathematical [[physics]], [[computer science]] and [[dynamic system]]s (categorical dynamics).

Most of these include some [[higher category theory]]. Some would define category theory as the human activity of [[category theorists]].

An imperfect perspective of category theory (for the purpose of classifying articles) can be obtained from the [MSC subject classification (18-XX)](http://www.ams.org/mathscinet/msc/msc.html?t=18-XX); the current one is from 2000 and reflects ideas of the decade before that.

#Contrast with set theory#
Here set theory is assumed to be a theory of the usual concept of sets, that is *material* [[set theory]].

No one of these is more fundamental than the other. Category theory is a holistic (structural) approach to mathematics that can (through such methods as Lawvere\'s [[ETCS]]) provide [[foundations]] of mathematics and (through [[algebraic set theory]]) reproduce all the different axiomatic set theories; elementary category theory does not need the concept of set to be formulated. Set theory is an analytic approach (element-wise) that can reproduce category theory by Lawvere's [[elementary theory of abstract categories]]. Lawvere also pointed out that set theory is axiomatized by a binary membership relation while category theory is axiomatized by a ternary composition relation.

|Set theory| |Category theory|
|----------|-|---------------|
|sets| |categories|
|membership relation| |-|
|elements| |objects|
|-| |morphisms|
|functions| |functors|
|equations between elements| |isomorphisms between objects|
|equations between sets| |equivalences between categories|
|equations between functions| |natural transformations between functors|

For more on this and for the many different generalized sets see

* Sets, categories and structuralism - Costas Drossos

+--{.query}

Rafael: I am a bit skeptical if to interpret ETAC as a set theory.

_Toby_:  See [[set theory]] for the contrast between material and structural set theories.  See also [[foundation]]s; there may be some overlap between what you intend to write here and what is or should be there.

I don\'t understand why you say that (material) set theory can reproduce category theory through ETAC.  Doesn\'t set theory reproduce category theory through the usual set-based definitions of category, functor, and natural transformation?

Rafael: Good answer.
I try to compare category theory to set theory. To do this i must be precise in what i mean by set theory. I mean set theory as a foundation since i am talking about "all" set theories. As for material set theory it seem to mean two different things. What i mean is sets as in ZFC set theory. I could not find an overlap with the links, but they are clearly related.

I had this idea of using plain set theory to define category theory just after posting this. Now i found problems with it. This does not mean that ETAC is better.
ETAC is not a theory of sets.

* Just because categories, functors, etc are defined from sets it does not make the definitions a foundation and not even a theory.
* Classes or something alike is needed instead of sets.
* An extra axiom for the existence of an universe must be added to the set theory used.

Perhaps i should contrast category theory with logic.

_Toby_:  Well, it\'s really [[ETCS]] that\'s a theory of sets.  ETAC is a theory of something a bit more, but it includes sets as the discrete categories.

By material set theory, I also mean a set theory in the style of ZFC (as opposed to the style of ETCS).  And category theory may be done using such a set theory as foundations by saying 'A category is a tuple consisting of a set $O$, a set $M$, functions $s, t: M \to O$, [...]' and so on, the way that it usually introduced to people that grew up on set theory, not by ETAC which is supposed to be an alternative foundation of its own.

(It\'s true that you should add a little something to ZFC to really do all of category theory, such as the language of classes ---replacing 'set' with 'class' in my quotation above--- or the axiom that an [[inaccessible cardinal]] exists or even that [[Grothendieck universe]]s exist.  But you still have a material set theory after having done so.)
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