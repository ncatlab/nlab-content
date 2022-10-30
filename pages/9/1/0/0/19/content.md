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

The classical examples of categories are [[concrete category|concrete categories]] whose [[object]]s are [[stuff, structure, property|sets with extra structure]] and whose [[morphism]]s are structure preserving functions of sets, such as [[Top]], [[Grp]], [[Vect]].  These are the examples from which the term _category_ derives: these categories literally _categorize_ mathematical structures.

But by far not all categories are of this type and categories are much more versatile than these classical examples suggest. After all, a [[category]] is just a [[directed graph]] with a notion of composition of its edges. As such it generalizes the concept of [[monoid]]. If the category is a [[groupoid]] it generalizes the concept of [[group]] (in a sense called [[horizontal categorification]]). 

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

This abstraction power of category theory has traditionally caused different feelings about it. The popular term _abstract nonsense_ for category theoretic methods was meant pejoratively but is often used by now just descriptively as in: "This property is not specific to this context, it already follows from abstract nonsense".

In the preface of his 1965 book _Theory of Categories_ Barry Mitchell writes:

>A number of sophisticated people tend to disparage category theory as consistently as others disparage certain kinds of classical music. When obliged to speak of a category they do so in an apologetic tone, similar to the way some say, "It was a gift &#8211; I've never even played it" when a record of Chopin Nocturnes is discovered in their possession. For this reason I add to the usual prerequisite that the reader have a fair amount of mathematical sophistication, the further prerequisite that he have no other kind.
=--


#What is category theory?#

**Category theory** is so useful because it can be seen from so many perspectives.

* The theory of [[category|categories]] as [[essentially algebraic theory|essentially algebraic structures]] with several objects and a relation (morphism) "algebra" on these objects. Structures in ordinary [[algebraic theory|abstract algebra]], like [[monoid|monoids]], have only one object. This theory also include [[functors]] between categories and [[natural transformation|natural transformations]].

* The theory of categories as primitive mathematical [[universe]]s or [[space]]s (nothing as fancy as a [[topos]]). As a space, a category is a [[simplicial set]] such that the [[Segal map]]s are isomorphisms. The simplicial set is the [[nerve]] of the category.


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

  =--


* A unifying tool and language in [[mathematics]].
* A new [[foundations|foundation of mathematics]] that focuses attention on structural issues and away from how mathematical objects are 'built up' as sets.
* An abstraction of an abstraction of an abstraction of .... The first level is [[set]]s and is most concrete. This is abstracted to categories (only some categories are categories of sets, hence the abstraction). The next abstraction is to categories of categories or more generally $2$-[[2-category|categories]]. This can be iterated to $n$-[[n-category|categories]] and [[infinity-category|indefinitely]]. This could be called the theory of abstractions.
* A description of partial [[symmetry|symmetries]], in the sense that [[group]]s describe symmetries.
* A generalized theory of [[representations]]. In this view every functor is a representation of its domain in its codomain and natural transformations are the [[intertwining operator]]s between representations.
* The theory of [[directed graph|directed graphs]] with a [[composition]] law. This has given rise to the heavy use of diagrams in category theory.
* A theory of [[type theory|type theories]]. There is a bijection between categories and type theories.
* A theory of [[deductive system]]s. There is a bijection between categories and deductive systems.
* A theory of [[presheaves]] with some properties on the full subcategory $[0] \overset{\rightarrow}{\underset{\rightarrow}\leftarrow} [1] \overset{\rightarrow}{\underset{\rightarrow}{\overset{\leftarrow}{\underset{\leftarrow}\rightarrow}}} [2]$ of $\Delta$.
  +-- {: .query}
  _Rafael_: I don't like this definition but maby others do. How do i edit multiple arrows, they are supposed to be on top of each other. And the numbers are supposed to be in square brackets that don't show! Anyone remembering the properties?

  _Toby_:  Put math between dollar signs!  The iTeX here is rather more like real LaTeX than the texvc at Wikipedia.  (That takes care of the brackets; for the arrows, learn to love `\overset` and `\underset`.)
  =--

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


#Contrast with set theory#
Here set theory is assumed to be a theory of the usual concept of sets, that is *material* [[set theory]].

No one of these is more fundamental than the other. Category theory is a holistic (structural) approach to mathematics that can (through such methods as Lawvere\'s [[ETCS]]) provide [[foundations]] of mathematics and (through [[algebraic set theory]]) reproduce all the different axiomatic set theories; elementary category theory does not need the concept of set to be formulated. Set theory is an analytic approach (element-wise) and can reproduce category theory by simply defining all the concepts in the usual way, as long as one include a technique to handle large categories (for instance by using [[class]]es instead of sets, or by including as an axiom that an uncountable [[inaccessible cardinal]] exists or even that [[Grothendieck universe]]s exist). Lawvere pointed out that set theory is axiomatized by a binary membership relation while category theory is axiomatized by a ternary composition relation.

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

For more on this and for the many different generalized sets see

* Sets, categories and structuralism - Costas Drossos

# References #

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


[[!redirects abstract nonsense]]
[[!redirects general abstract nonsense]]