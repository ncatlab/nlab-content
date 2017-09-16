[[!include contents]]

#Idea#

Unsurprisingly, **category theory** is the theory of [[category|categories]].

But maybe surprisingly, category theory turns out to be much more than the study of a particular mathematical structure. The degree to which category theory for instance is more encompassing than [[group theory]] is more drastic than the simple straightforward generalization from the mathematical structure [[group]] to the mathematical structure [[category]] might suggest. This is one of the main reasons for interest in category theory: it seems to provide a unified language for mathematics.

+--{.query}
Rafael: Eric, the first section don't have a headline and it also don't bring much new information that is not in the section what is category theory.
Is the first section really necessary?

Eric: Hi Rafael. I like what you wrote, but I also like these nontechnical paragraphs that Urs writes. It's not so important to be efficient, so I'd be hesitant about deleting material that others might find helpful. We often have an opening paragraph that is very light in nature like that. I added a common heading we use for such colloquial paragraphs: "Idea".

Rafael:
I like the idea sections. But this section looks more to me like an introduction section (or even more a nontechnical what is category theory section) than an idea section. I would be glad if someone, maby Urs, could reformulate it to make the perspective of an idea more explicit. Then maby Urs had that in mind but just did't put a headline.
=--

#What is category theory?#
**Category theory** is so useful because it can be seen from so many perspectives.

* The theory of [[category|categories]] as [[essentially algebraic theory|essentially algebraic structures]] with several objects and a relation (morphism) algebra on these objects. Structures in ordinary [[algebraic theory|abstract algebra]], like [[monoid]]s, have only one object.
* The theory of categories as primitive mathematical [[universe]]s or [[space]]s (nothing as fancy as a [[topos]]).
* A unifying tool and language in [[mathematics]].
* A top-down [[foundations|foundation of mathematics]] (that is structural and more than just type theories).
* An abstraction of an abstraction of an abstraction of .... The first level is [[set]]s and is most concrete. This is abstracted to categories (only some categories are categories of sets, hence the abstraction). The next abstraction is to categories of categories or more generally $2$-[[2-category|categories]]. This can be iterated to $n$-[[n-category|categories]] and [[infinity-category|indefinitely]]. This could be called the theory of abstractions.
* A description of partial [[symmetry|symmetries]], in the sense that [[group]]s describe symmetries.
* A generalized theory of [[representations]].
* The theory of combinatorial [[directed graph|directed multipseudographs]] with a [[composition]] law.
* A theory of [[type theory|type theories]]. There is a bijection between categories and type theories.
* A theory of [[deductive system]]s. There is a bijection between categories and deductive systems.

#Branches of category theory#
A good, but  imperfect perspective of category theory can be obtained from the [MSC subject classification (18-XX)](http://www.ams.org/mathscinet/msc/msc.html?t=18-XX) (but remember the current one is from 2000 and reflects ideas of the decade before that).  The subject has exploded into many new areas since.

+--{.query}
Rafael: Don't try to make logical sense of MSC. I have since very long abondoned it. It works better to bring chaos than order in a classification. The reason is that it was not made to classify mathematics but mathematical articles.

I think that this section can with help grow into a much better classification. Or it could even become in time an entry. The aim is in any case not to need MSC.
=--

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

#category theory entries#
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