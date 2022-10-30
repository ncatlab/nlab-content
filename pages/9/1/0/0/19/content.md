[[!include contents]]


#Idea#

+-- {: .un_remark}
###### Origin

Category theory was introduced by Samuel Eilenberg and Saunders Mac Lane in the 1945 paper **General theory of natural equivalences**. The reason for introducing [[category|categories]] was to introduce [[functor]]s, and the reason for introducing functors was to introduce [[natural transformation]]s (more specifically natural equivalences) in order to define what _natural_ means in mathematics. 

The paper was a clash of ideas from abstract [[algebra]] (Mac Lane) and [[topology]]/[[homotopy theory]] (Eilenberg). It was first rejected on the ground that it had no content but was later published. Unexpectedly category theory has flourished into almost all areas of mathematics, has found many applications outside mathematics and even attempts to build a [[foundations]] of mathematics. 
=--

+-- {: .un_remark}
###### Paradigm

The basic idea of category theory is to shift attention from the study of [[object]]s to the study of _maps_ or _relations_ between objects: of (homo)[[morphism]]s between objects. 
=--

+-- {: .un_remark}
###### Examples

The archetypical example of a category is the category [[Set]] of [[set]]s and functions between sets. 

The classical examples of categories are [[concrete category|concrete categories]] whose [[object]]s are [[stuff, structure, property|sets with extra structure]] and whose [[morphism]]s are structure preserving functions of sets, such as [[Top]], [[Grp]], [[Vect]].  These are the examples from which the term _category_ derives: these categories literally _categorize_ mathematical structures by packing structures of the same _type_ (same category) and structure preserving mappings between them into a single whole structure, a category.

But by far not all categories are of this type and categories are much more versatile than these classical examples suggest. After all, a [[category]] is just a [[directed graph]] with a notion of composition of its edges. As such it generalizes the concepts of [[monoid]] and [[poset]]. If the category is a [[groupoid]] it generalizes the concept of [[group]] (in a sense called [[horizontal categorification]]).  Thinking of a category as a generalized poset is particularly useful when studying [[limits]] and [[adjoint functors|adjunctions]].

Archetypical examples of non-[[concrete category|concrete]] categories are the [[fundamental groupoid]] of a [[topological space]] and the [[fundamental category]] of a [[directed space]]. 
=--

+-- {: .un_remark}
###### Category theory pointing beyond itself

These latter examples already pave the way to the [[homotopy hypothesis]], to the unification between category theory and [[homotopy theory]] in [[Higher Topos Theory|(infinity,1)-category theory]] and thereby to [[higher category theory]]. 
=--

+-- {: .un_remark}
###### Conceptual unification

One major driving force behind the development of category theory is its ability to abstract and unify concepts. General statements about categories apply to each specific [[concrete category]] of mathematical structures. The general notion of [[universal construction]]s in categories, such as [[representable functor]]s, [[adjoint functor]]s  and [[limit]]s, turns out to prevail throughout mathematics and manifest itself in myriads of special examples.
=--

+-- {: .un_remark}
###### Abstract nonsense

This abstraction power of category theory has traditionally caused different feelings about it. The popular term _abstract nonsense_ for category theoretic methods was meant pejoratively but is often used by now just as descriptively as in: "This property is not specific to this context, it already follows from abstract nonsense".

In the preface of his 1965 book _Theory of Categories_ Barry Mitchell writes:

>A number of sophisticated people tend to disparage category theory as consistently as others disparage certain kinds of classical music. When obliged to speak of a category they do so in an apologetic tone, similar to the way some say, "It was a gift &#8211; I've never even played it" when a record of Chopin Nocturnes is discovered in their possession. For this reason I add to the usual prerequisite that the reader have a fair amount of mathematical sophistication, the further prerequisite that he have no other kind.
=--


#What is category theory?#

**Category theory** is so useful because it can be seen from so many perspectives.

* The theory of [[category|categories]] as [[essentially algebraic theory|essentially algebraic structures]] with several objects and a relation (morphism) "algebra" on these objects. Structures in ordinary [[algebraic theory|abstract algebra]], like [[monoid|monoids]], have only one object. This theory also include [[functors]] between categories and [[natural transformation|natural transformations]].
* The theory of categories as 1D primitive mathematical [[universe]]s or [[space]]s (nothing as fancy as a [[topos]]). As a space, a category is a [[simplicial set]] such that the [[Segal map]]s are isomorphisms. The simplicial set is the [[nerve]] of the category.
  +-- {: .query}
  Rafael: Preferrably as some 1D CW-complex that i am trying to figure out. Can someone fill that in.

  _Urs Schreiber_: could you give more details? I don't see yet what you mean here.

  _John Baez_: since a 1d CW complex is just a graph, I bet he's noting that categories are just graphs with extra structure. But be a little careful: categories are directed graphs with extra structure, while 1d CD complexes are undirected graphs.

  _Rafael_: Sometimes i need to rest but i will slowly get back to write online now. I remember a description of a category as some CW-complex flashing by in google. Of cause you should not trust everything you find by google, but unfortunately i can't give more details since i can't find it again. The idea is to make this definition of a category as a space more mathematically precise. 

  As i pointed out in the various definitions of a category theory a category is a directed multigraph with a composition law. This is not new for me. It is a good point there that CW-complexes are undirected :)
  So a directed 1D CW-complex (whatever that is) is closer. Therefore other ways to define it as a space might be more natural. The point is that i don't see graphs as spaces (perhaps i should) and i wish to define a category as a space.

  _Toby_:  I\'d say that you should see a graph as a space for *one* facet of a graph, just as you are trying to do here for *one* facet of a category.  (^_^)

  _Rafael_: I have it. :)

  [[Urs Schreiber]]: there are several different ways that "categories are spaces". I think what you are thinking of now is how to characterize simplicial sets that are nerves of categories. But notice that when you think of the simplicial set as a [[topological space]] that means turning the category it came from into an $\infty$-groupoid, so is not really the original category anymore but something different.

  By the way the link to [[universe]] takes one to [[Grothendieck universe]]. That does not seem to make sense to me in this context here.

  Another by the way: the characterization theorem of simplicial sets that are nerves of categories is given at [[nerve]]. Maybe the paragraph above that we are talking about here should just read as follows:

  * Categories can be conceived as [[simplicial set]]s with a special [[stuff, structure, property|property]]. This property is described at [[nerve]], since simplicial sets that have this property are called [[nerve]]s of categories. 

  This description is useful in that it opens a useful road to [[higher category theory]] in terms of [[geometric definition of higher category]]. Generally, a [[simplicial model for weak omega-categories]] is a characterization of [[simplicial set]]s with certain properties that generalize those of [[nerve]]s of ordinary categories.

  This is particularly well known for the case that the higher categories in question are [[infinity-groupoid]]s. These are modeled by simplicial sets that have the property that they are [[Kan complex]]es.

  That would be a suggestion. I must say I don't feel that the sentence "The theory of categories as primitive mathematical universes or spaces (nothing as fancy as a topos)." tells me anything. I'd suggest to either remove it completely or figure out what it means to say and then say it in somewhat different words.

  [[David Roberts]]: I think the constrast needs to be made between small categories, which are models for homotopy types, and categories which are to be considered ambient categories, like topoi, [[exact category|Barr-exact categories]], $(\infty,1)$-categories and so on. This is probably what Rafael means, but the juxtaposition in the sentence is slightly confusing. In fact, I've put a bit in about Grothendieck's views on small categories.

  [[Urs Schreiber]]: concerning homotopy types: yes, so that's what I tried to say: while a category _models_ a homotopy type, it can't really be identified with that. 
Many different categories model a given homotopy type. In fact, already all [[poset]]s model all homotopy types in this sense (namely in the sense that all homotopy types are obtained as [[geometric realization]]s of [[nerve]]s of them). 

  On David's other comment: tt is a good point that for practical purposes we may want to distinguish on which level of self-reflection of category theory we are speaking. Do we have a single $\infty$-category that happens to be used as a model for a homotopy type, or do we happen to consider an $\infty$-category of "all" $\infty$-categories of such sorts (or do we go even further).

  I'd think we need to hear back from Rafael a comment describing a bit more in words what the _intention_ of the above paragraph is. Then I would feel free to implement my suggestion for how one could phrase it.

  _Rafael_: Toby, a graph would be a too strange space. There are no rules how you can go (travel) between points in that space.

  Urs, i am not thinking of a simplicial sets as topological spaces. Just to start, what is an open subset of a simplicial set? To turn it into a set and then a topological space would require to apply the geometric realization functor |.|. Up to categorical equivalence nothing is lost in passing to the nerve which is a category and a special simplicial set (not a topological space). Further, the description is so short so there is no reason to refer to the nerve page. If someone has a better "definition" of a category as a space i would be happy to hear it.

  This point in the list is very important, it tells that categories have a geometry. You may think of them as geometric objects and not only algebraic objects.
Oversimplified, you can draw a category on paper instead of dealing with sets of objects, morphism, etc.

  This is what i mean by a primitive space. A collection of points with paths between the points on which you can move between the points in the primitive space. Since motion is directed the paths will be directed. I hope this helps. You might add that to this point in the list if you like.

  You also talk about identifying, this could mena many things. Identical in all respects, there exist a bijection, there exist an invertible functor,... 

  This reminds me of identifying (by bijection) points of sets with functions. I could accept it but it is like saying that i can use the fundamental forces of nature instead of my arms and legs just because both happen to be 4. I can then induce everything else on the forces from my arms and legs afterwards but it don't make sense. Something (everything) got lost in the translation. To end, i still claim that identifying the nerve of a category with a category is good enough (for small categories). No one seem to have objected to identify categories with for instance presheaves (i will work more on that).

  David, you do have a point there, this nerve only works for small categories. I don't know how to fix it to work with large categories yet. Is it an unsolved problem?

  I have taken the liberty to reformulate what you have written, hope you like it. It is more stright on.
Now i only wish i knew more about fundamental localizers to write more.

  Regarding Grothendieck universes. A Grothendieck universe contains what may be called the small sets in a set theory such as ZFC. Having an axiom that forces every set to be an element of some Grothendieck universe eliminate such sets as the set of all sets and the following paradoxes. Grothendieck was the first to see and formulate this in SGA in 1972. But i am no expert on this. I have not read the whole aricle on Grothendick universes. I wonder what Urs had in mind.

  References are: first part of first chapter of first volume of "Handbook of categorical algebra" - Borceux and "One universe as a foundation for category theory" - Mac Lane 1969. "Categories and sheaves" - Kashivara-Schapira do also mention briefly universes at the beginning.

  _Toby_:  The way that topologists think of a graph as a space is as a CW complex.  Each edge is modelled by a copy of the unit interval $[0,1]$ (which way doesn\'t matter up to homeomorphism), and each vertex is modelled by a single point, which is then identified with the appropriate endpoint of each edge interval that touches it.  (And if you want to be constructive, do a little completing here, but that\'s not important.)  Of course, this is all very much like taking the geometric realisation of a simplicial set, and it does not lose any information if you are talking about an undirected graph (even multipseudograph).

  If you have a specific reference, with page number, for your vision of a category as a space, I would like to see it.  I mean, I\'ve read Borceux, but I don\'t remember anything like this (I\'ll check again).  Is it just a matter of visualisation?, or something more rigorous?  If the former, then I think that I understand what you mean, but I\'m not getting the latter.

  _Rafael_: So you made a category into a set, now any topology on it will make it into a topological space. But the point was to still have a category and not a set with a topology. Anyway, i forgot two fundamental points. The points must all be of the same type! and the paths between two points must form a set (so there are not too many ways to move from one point to another) and nothing bigger. I did see it as a visualization but i am convinced it can, at least for smal categories, be made rigorous. And technically for smal categories it is nothing wrong to pass to their nerve. While others may prefer it as a characterization. I have a vague memory of one reference: The tale of n-categories, but quickly searching there for space gave nothing. It is there that i read that the Hom's must not be larger than sets.

  _Toby_:  I still don\'t know what you\'re talking about, but the construction that I mentioned comes with a topology (just do it in $Top$, or better in $Comp Met$).

  _Rafael_: You left out the topology, that's all. Then, at least Urs mentioned that you can't reconstruct a category from its homotopy type. I mentioned many things, you have to be specific what you don't know i am talking about.
If it is about the two points, it was with regard to what a primitive space is.

  _Toby_:  Actually, I defined a [[CW complex]]; that\'s a topological space.  The problem with what you\'ve mentioned all along is that it\'s incomplete.  (That\'s OK, we have a lot of incomplete ideas here.)  But I don\'t understand what you\'d just added, it\'s true; what do you mean to say that all of the points of this space must be of the same type? and why do you think that size issues matter?  (And now I don\'t understand what you mean by a 'primitive space'.)  But I\'m not sure that answering these questions will actually get anywhere; you need to make the idea more precise, and you may not be able to do that until you find the references that you remember.  (Again, that\'s OK, there are lots of places on the Lab where we say &#8249;I think that I saw this, but I can\'t remember it now.&#8250;.  So just because I say that I don\'t understand you, please don\'t think that this means that I demand that you explain!)

  _Rafael_: This is what i can explain and probably no further. The points should for instance not be mixed as {a differential operator, a function $R \rightarrow R$, a fractal set in C, a measure, a ring, a CW-complex, etc.}. I claim they are of different types. Then, it was not me that demanded that the Hom's must be sets, but obviously you can't get from one place to another changing your internal state arbitrary. This is how i see the condition that you can't get from one place to another in too many ways. 
Don't ask me for more details about it. Unfortunately this don't define a primitive space so maby forget about it.

  The CW-complex statement is more interesting. As i see they are equivalent. There is an invertible functor between them. I say again that if a topological space is a pair (X,{open subsets of X}), these open subsets have to be defined and given (or shown to exist) on the CW-complex. On the other hand CW-complexes are combinatorial objects, they are built by gluing together cells. A topological space have no cells defined!

  [[David Roberts]]: it seems to me (and I quite obviously may be wrong) that you are confusing globular sets and CW-complexes. The geometric realisation of a globular set is a CW-complex. The former is a purely combinatorial creature, but a CW complex is just a colimit of cells (namely balls in $R^n$), each of which have a canonical topology. Looking at the Wikipedia page for CW complex, we see that it is defined as _a Hausdorff topological space with a decomposition into cells_. The combinatorial structure (which is not a priori a globular set!) is derived from the decomposition which is information on top of an underlying space. In this sense one could consider the forgetful functor $CW \to Top$ (let us for arguments sake take cellular maps). The fibre over a given space may be empty (i.e. it does not admit the structure of a CW-complex - an example is the Hawaiian earring), but if the fibre is not empty, it should be apparent that a CW complex structure is not unique. Consider the following structures on the circle (defined as, say, a subspace of $R^2$, radius 1): one 0-cell and one 1-cell; and two 0-cells and two 1-cells. Indeed one can define an infinite number of CW-complex structures on the circle. But we still have the underlying circle!

  Now the globular set associated to a category is defined completely by its data in dimensions 0,1 and 2 - the last encodes the equations between arrows. This is what I feel you are contrasting with the CW-complex as described by Toby. 

  [[Urs Schreiber]]: I am sorry, but 

  * I still dont' understand the sentence (actually, it's not a sentence, maybe it would help to make it one) 

    "The theory of categories as 1D primitive mathematical [[universe]]s or [[space]]s (nothing as fancy as a [[topos]])."

    This sounds confusing to me. The only categories that deserve to be called "mathematical universes" are precisely toposes. And to say that a category is a "1d space" looks at best misleading to me. This is not the way the word "space" is usually used. Is this really a helpful statement for explaining what categories are?

  * i also still have quarrels with the next sentencee

    "As a space, a category is a [[simplicial set]] such that the [[Segal map]]s are isomorphisms. The simplicial set is the [[nerve]] of the category."

    If "space" here means "topological space" then this is not right. If you regard a category as a placeholder for the topological space that corresponds to the simplicial set that is its nerve then you loose information about the category. Namely about its non-invertible morphism. Can't we just say "A category is equivalently a simplicial set such that...".

    I am sorry for being what must come across as a pain. My impression is --  correct me if I am worng -- that the actually intended statement here is pretty much "A category is a [[directed graph]] with a a notion of composition of edges". And then maybe one could point out that a directed graph is much like a [[directed space]]. Would that be a compromise, that we say [[directed space]] instead of "space" above? 

  _Toby_:  We\'ve mostly been trying to talk about the space-like stuff here (and it\'s certain that 'space', whatever Rafael means by it, does *not* mean precisely [[topological space]]), but now I need to address the universe-like stuff.  In particular, I absolutely agree with
  > The theory of categories as primitive mathematical universes
  with 'universe' in the sense of a place to do mathematics, and I absolutely disagree with Urs\'s comment
  > The only categories that deserve to be called "mathematical universes" are precisely toposes.
  which (forgive me) strikes me as born of ignorance.

  A topos is a universe in which one can do finitist impredicative constructive ordinary mathematics, neither more nor less.  Every one of those four adjectives can be altered, and new ones might be included as well.  If you don\'t want to restrict yourself to finitist mathematics, then not just any topos will do; you need a $W$-topos (a topos with NNO).  If you do want to restrict yourself to predicativist mathematics, then something more general, such as a pretopos, will also work.  By 'ordinary' here, I mean that you\'re not using 'unbounded' or 'large' axioms like replacement or large cardinals, which are necessary for some post-Cantor mathematics.

  In particular, there is a small amount of mathematics ---not much, but something--- that can be done in an abitrary category, and any category can serve as a universe for that.  Personally, I need at least a finitely complete category to feel comfortable (although I\'m starting to learn how to do things in a site, in the sense of a category equipped with a Grothendieck pretopology), and I would certainly regard one of those as a good enough universe for a lot of mathematics ---including basic category theory.

[[David Roberts]]: I agree with Toby - as would I think Igor. Many things one would want to do with descent etc can be done in an [[exact category]] (Barr- not Quillen-) with little effort. But this is secretly just a site using the regular epimorphisms as covers. So one might as well use a site (preferably with a subcanonical (pre)topology). In a lot of cases, when push comes to shove, only covers need to be pulled back, and this is ensured by the axioms for a site. Thus one can do away with the requirement that we have pullbacks. Personally I like having binary products around the place, but I suppose if one is masochistic they aren't necessary ;)
  =--

* A theory of models for homotopy types. In [[Alexander Grothendieck|Grothendieck's]] approach to homotopy theory he called $Cat$ together with the class of functors that induced weak equivalences on nerves a [[fundamental localizer]]. See [[the homotopy theory of Grothendieck]].
* A unifying tool and language in [[mathematics]].
* An organizational tool in [[mathematics]].
* A new [[foundations|foundation of mathematics]] that focuses attention on structural issues and away from how mathematical objects are 'built up' as sets.
* An abstraction of an abstraction of an abstraction of .... The first level is [[set]]s and is most concrete. This is abstracted to categories (only some categories are categories of sets, hence the abstraction). The next abstraction is to categories of categories or more generally $2$-[[2-category|categories]]. This can be iterated to $n$-[[n-category|categories]] and [[infinity-category|indefinitely]]. This could be called the theory of abstractions.
* A description of partial [[symmetry|symmetries]], in the sense that [[group]]s describe symmetries.
* A generalized theory of [[representations]]. In this view every functor is a representation of its domain in its codomain and natural transformations are the [[intertwining operator]]s between representations.
* The theory of [[directed graph|directed multipseudographs]] with a [[composition]] law and identity loops. This has given rise to the heavy use of diagrams in category theory.
* A theory of [[type theory|type theories]]. There is a bijection between categories and type theories.
* A theory of [[deductive system]]s. There is a bijection between categories and deductive systems.
* A theory of [[presheaves]] with some properties on the full subcategory $[0] \overset{\rightarrow}{\underset{\rightarrow}\leftarrow} [1] \overset{\rightarrow}{\underset{\rightarrow}{\overset{\leftarrow}{\underset{\leftarrow}\rightarrow}}} [2]$ of $\Delta$.
* A theory of [[Cat]], the $2$-[[2-category|category]] of categories. This is axiomatized in Lawvere\'s [[ETAC]].

Some would define category theory as the human activity of [category theorists](http://ncatlab.org/nlab/list/people).


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

Most of these include some [[higher category theory]].

An imperfect perspective of category theory (for the purpose of classifying articles) can be obtained from the [MSC subject classification (18-XX)](http://www.ams.org/mathscinet/msc/msc.html?t=18-XX); the current one is from 2000 and reflects ideas of the decade before that.

#Main principle of category theory#
Category theory has a main principle:

_In any category it is unnatural and undesirable to speak about equality of two objects_.  See [[evil]].

For the theorem accepted as the fundamental theorem of category theory see the [[Yoneda lemma]].

#Contrast with set theory#
Here set theory is assumed to be a theory of the usual concept of sets, that is *material* [[set theory]].

No one of these is more fundamental than the other as a foundation of mathematics. Category theory is a holistic (structural) approach to mathematics that can (through such methods as Lawvere\'s [[ETCS]]) provide [[foundations]] of mathematics and (through [[algebraic set theory]]) reproduce all the different axiomatic set theories; elementary category theory does not need the concept of set to be formulated. Set theory is an analytic approach (element-wise) and can reproduce category theory by simply defining all the concepts in the usual way, as long as one include a technique to handle large categories (for instance by using [[class]]es instead of sets, or by including as an axiom that an uncountable [[inaccessible cardinal]] exists or even that [[Grothendieck universe]]s exist). 

+--{: .query}
[[David Roberts]]: one cannot both enrich and internalise category theory! There are some instances (e.g. $Top$-categories) where enriched categories can be considered as internal categories, but generally this requires copowers of the terminal object (to form the object of objects) and enough coproducts to form the object of arrows. There is not really any sense in which an internal category can be thought of as an enriched category, except one arising from the procedure mentioned. In any sense, one still needs at least a naive/meta set theory in which to define the ambient category or category over which one wants to enrich.

_Toby_:  Actually, one does *not* need any sort of meta set theory to define categories in the first place; I can\'t imagine how anyone familiar with categorial foundations could say that.  The concept of category is entirely first-order; sometimes one distinguishes 'meta-categories' (na&#239;ve) from 'categories' (modeled in some theory of sets), but that is not done in foundations.  One might *want* to use at least dependent type theory, but it is still possible to define a category in untyped first-order logic.

_Rafael_: So if one do not need sets to define categories, how do one completely eliminate the dependence on Set in the definition of a category? This is the first time i hear of the impossibility of mixing enrichment with internalization. Feel free to correct it instead of writing more arguments.

[[David Roberts]]: I think you credit me with more familiarity with (category theoretical) foundations than I have (but the undeserved compliment is nonetheless flattering) - it has always been something on my to-do list :S. If I remember correctly, my intention for including the naive set theory comment was for the purposes of enrichment and internalisation in what one might call \'the usual sense\', that is relative to some existing (set theory) foundation. If one is considering completely category theoretic foundations, then the idea of getting rid of sets by either internalising or enriching is, as you say, completely redundant. However, my point stands that the sentence is entirely confusing to the newcomer.

_Toby_:  The main point to understand is that both [[ZFC]] (we haven\'t written that yet, but y\'all know what I mean) and [[ETCS]] are written in the same language: first-order classical logic.  Neither requires any prior set theory, which is a good thing since they are supposed to be foundational.  (It may be convenient to express ETCS in the language of dependent type theory, or at least in a two-sorted language, but this is not necessary, as objects can be identified with their identity morphisms.  In any case, the dependent type theory that might be used falls far short of set theory; in fact, it\'s conservative over predicate calculus with equality.)  Of course, ETCS (which is intended as a replacement for ZFC) is an elementary theory of a category *of sets*, but you get an elementary theory of a category (call it ETC) by removing some axioms.  We are now only talking about one category at a time, however; so another way to go is to modify ETCS to become the elementary theory of a ($2$)-category *of categories* (call it ETCC); see Lawvere\'s 1966 _The category of categories as a foundation for mathematics_.

_[[John Baez]]_: I'm deleting the mistake that launched this discussion: "In fact the definition of a category depend on sets. To get rid of this dependence categories have to be internalized and enriched, which is enriched internal category theory."   

David R: Thankyou!

[[Mike Shulman]]: Coming in a bit late, I don't disagree with the conclusion (removing that sentence), but I also feel the need to point out that there _is_ a notion which generalizes both enriched and internal categories, and which also includes things that one might reasonably call "enriched internal categories."  I'm thinking of the notion of categories enriched in a [[bicategory]] (or, in my opinion more correctly, an [[equipment]]).  Ordinary enriched categories are categories enriched in a monoidal category considered as an equipment with one object; ordinary internal categories are categories with one object enriched in an equipment of spans.  And as a basic example of "enriched internal categories," consider for a nice category $S$ the equipment whose objects are those of $S$ and whose (pro)arrows from $X$ to $Y$ are internal abelian group objects in $S/(X\times Y)$.  A category enriched in this equipment (perhaps with one object) can be thought of as "a category internal to $S$ and enriched in (internal) abelian groups."

=--

|Set theory| |Category theory|
|----------|-|---------------|
|membership relation| |-|
|sets| |categories|
|elements| |objects|
|-| |morphisms|
|functions| |functors|
|equations between elements| |isomorphisms between objects|
|equations between sets| |equivalences between categories|
|equations between functions| |natural transformations between functors|

Lawvere pointed out that set theory is axiomatized by a binary membership relation while category theory is axiomatized by a ternary composition relation.

The process of going from sets to categories is called [[categorification]] and is a functor $Set \rightarrow Cat$, and the reverse process is called [[decategorification]].

+--{: .query}
[[David Roberts]]: Is this true??? I would have thought that categorification would be more like (and I'm not saying this is strictly true) a process $Cat \to 2Cat$, since what is does is take an ordinary category of things (like the category of groups) and replaces it with a 2-category of things (like the 2-category of (strict, say) 2-groups). What happens to the arrows is very important, as we could categorify group homomorphisms to strict morphisms of strict 2-groups or to weak morphisms of 2-groups.

_Toby_:  Categorification is nothing as precise as the inclusion functor $Set \to Cat$, but I think that it\'s fair to say that *decategorification* is its left adjoint $Cat \to Set$ ... well really, $Grpd \to Set$.  Sure, in categorification, we replace categories with $2$-categories, $2$-categories with $3$-categories, and so on, but we do this by replacing a set with a category at the top level.  So that\'s where it starts ... or actually, you could say that it starts with $TV \to Set$ (where $TV$ is the category of [[truth value]]s).

_Rafael_: Toby is pointing out my idea i was going to write. Categorification in its completeness is more like an ∞-functor or a sequence of functors $nCat \rightarrow (n+1)Cat$ with $0Cat=Set$ and $(-1)Cat=TV$. My functor above is only a part of this. Similarly it is possible to decategorify as $nCat \rightarrow (n-1)Cat$. The problem is, what is categorified? If i categorify sets i will get categories. This is all according to the categorical ladder of n-categories.

[[David Roberts]]: I maintain that Baez-Dolan categorification (not that any other sort of categorification is really different, but that is conceptually the easiest) is more about passing from $Cat$ to $Bicat$. Simply replacing hom-sets by categories (i.e. $Cat$-enrichment) is not quite enough - one needs weak enrichment in general. But alas my memory fails to provide a legitimate example for this claim just when I need one. We as categorifiers are constructing the mapping (I don\'t say functor, because it is not so systematic)  $Cat \to Bicat$ one object at a time: $Grp$, $Vect$, $Hilb$, $LieAlg$, $Tang$ and so on. 

_Toby_:  But from $Bicat$ you can categorify further to $Tricat$ etc, so why stop there?  (I guess that it depends on how strictly you interpret 'Baez--Dolan' categorification; I don\'t think that Baez and Dolan intended to limit the idea, but it\'s true that this is the sort of thing that they discussed in their paper _Categorification_.)  So in the limit, categorification is about going from $\infty Cat$ to $\infty Cat$, but in a nontrivial way.

Note that we do have articles [[categorification]] and [[decategorification]]; perhaps we should move this discussion to the former?

[[David Roberts]]: I agree - categorification is maybe a bit too much for people who are trying to find out why they might be interested in categories for the first time.
=--

For a philosophical consideration of foundations covering and comparing sets, structuralism [a la Bourbaki?] and categories, see the article

* Sets, categories and structuralism - Costas Drossos

+--{: .query}
[[David Roberts]]: This article is more of a philosophical examination of structuralism in a broad sense in the context of category theoretical approaches to foundations. I'm not sure how it goes as a reference for categorification or as an exposition of various approaches to foundations.

_Rafael_: This article is not as technical as the proof of the characterization theorem for higher toposes, but i think it explains everything in it well. It explains the difference between category theory and set theory as foundations (as is the title of this subsection) and even tries to compare and unify all the modern generalizations of sets. Structuralism is explained (as it should be) and is only slightly dominating over the set theoretic foundation. I never said it would explain categorification or should give a list of foundations. There is another article for that. And by the way, foundations have a philosophical aspect, even if i am not so good at that.
You could start a philosophical section about categorical foundations and put it there, i don't feel up to it.

[[David Roberts]]: I agree about the philosophical section, but that is more up [[David Corfield]]'s alley. Please don't take my comments on the Drossos paper as authoritative, but I just wanted to flag that it is in a very different vein to the rest of this page. I have rewritten your sentence above so as to show this - as it was it would have seemed to introduce a paper on categorification. For that purpose I believe Baez-Dolan would be better.
=--

#Other categorical structures#

These are often seen as a part of category theory even if they are only related to categories.

* [[allegory|Allegories]]

+-- {: .query}
I don\'t know what you mean here, Rafael.  An allegory *is* a category with extra bells and whistles.  Why do you put this here but not [[monoidal categories]] or $\infty$-[[infinity-category|categories]]?  ---Toby

_Rafael_: Yes, i see that, i was thinking in another way. It should be removed but there must be other examples in the same way that semigroups, quasigroups, monoids, groupoids etc. are related to groups as group like structures.

As a possible suggestion, what would happen if associativity or identities in a category would be given up?

I am also thinking about a chapter "Higher category theory". So far i am thinking what it should contain.
=--

#Applied category theory#

Here are some fields to which category theory has been applied; ultimately we should have articles on all of them.

* [[physics]] (ex: categorical spacetime in quantum gravity, the category of elementary particles and particle interactions, QFT and quantization)
* [[computer science]] (ex: data types, artificial intelligence, programming language semantics)
* [[categorical dynamics]]
* [[neural network]]s
* [[psychology]] (ex: perception, cognition, consciousness, teaching, knowledge)
* [[chemistry]] (the category of chemical elements and chemical reactions)
* [[nuclear physics]] (the category of atomic nuclei and nuclear reactions, graphical calculus for spin)
* [[biology]] (ex: detecting life)
* [[linguistics]]
* [[philosophy]]
* [[music]]

#References#

Category theory textbooks for which the $n$Lab currently provides detailed linked indexes are

* Kashiwara and Schapira, [[Categories and Sheaves]].

* Ieke Moerdijk and Saunders Mac Lane, [[Sheaves in Geometry and Logic]]

Other standard references include:

* Saunders Mac Lane, [[Categories Work|Categories for the working mathematician]], 2nd ed. 
* Steve Awodey, Categories for everybody. 
* Francis Borceux, Handbook of categorical algebra, vol 1--3. 
* Colin McLarty, Elementary categories, elementary toposes. 
* Jiri Adamek, Horst Herrlich, and George Strecker, Abstract and concrete categories -- the joy of cats. [free online](http://katmat.math.uni-bremen.de/acc/acc.pdf)
* Michael Barr and Charles Wells,
Toposes, triples and theories. [free online](http://www.cwru.edu/artsci/math/wells/pub/ttt.html)
* Robert Goldblatt, Topoi, the categorial analysis of logic.
[free online](http://historical.library.cornell.edu/cgi-bin/cul.math/docviewer?did=Gold010&seq=&view=50&frames=0&pagenum=1)
* Tom Leinster, Higher operads, higher categories [free online] (http://arxiv.org/PS_cache/math/pdf/0305/0305049v1.pdf)
* Eugenia Cheng, Aaron Lauda, Higher-dimensional categories - an illustrated guide book [free online] (http://cheng.staff.shef.ac.uk/guidebook/guidebook-new.pdf)
* [[Peter Johnstone]], Topos theory
* [[Jacob Lurie]], [[Higher Topos Theory]] 
* Project description - higher categorical structures and their applications [free online] (http://www.math.uchicago.edu/~may/NCATS/ForWeb.pdf)

[[!redirects abstract nonsense]]
[[!redirects general abstract nonsense]]
[[!redirects applied category theory]]