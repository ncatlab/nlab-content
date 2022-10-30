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
* The theory of categories as primitive mathematical [[universe]]s or [[space]]s (nothing as fancy as a [[topos]]).

+-- {: .query}
Rafael: Preferrably as some 1D CW-complex that i am trying to figure out. Can someone fill that in.

_Urs Schreiber_: could you give more details? I don't see yet what you mean here.

_John Baez_: since a 1d CW complex is just a graph, I bet he's noting that categories are just graphs with extra structure. But be a little careful: categories are directed graphs with extra structure, while 1d CD complexes are undirected graphs.

_Rafael_: Sometimes i need to rest but i will slowly get back to write online now. I remember a description of a category as some CW-complex flashing by in google. Of cause you should not trust everything you find by google, but unfortunately i can't give more details since i can't find it again. The idea is to make this definition of a category as a space more mathematically precise. 

As i pointed out in the various definitions of a category theory a category is a directed multigraph with a composition law. This is not new for me. It is a good point there that CW-complexes are undirected :)
So a directed 1D CW-complex (whatever that is) is closer. Therefore other ways to define it as a space might be more natural. The point is that i don't see graphs as spaces (perhaps i should) and i wish to define a category as a space.

=--

* A unifying tool and language in [[mathematics]].
* A new [[foundations|foundation of mathematics]] that focuses attention on structural issues and away from how mathematical objects are 'built up' as sets.
* An abstraction of an abstraction of an abstraction of .... The first level is [[set]]s and is most concrete. This is abstracted to categories (only some categories are categories of sets, hence the abstraction). The next abstraction is to categories of categories or more generally $2$-[[2-category|categories]]. This can be iterated to $n$-[[n-category|categories]] and [[infinity-category|indefinitely]]. This could be called the theory of abstractions.
* A description of partial [[symmetry|symmetries]], in the sense that [[group]]s describe symmetries.
* A generalized theory of [[representations]]. In this view every functor is a representation of its domain in its codomain and natural transformations are the [[intertwining operator]]s between representations.
* The theory of [[directed graph|directed graphs]] with a [[composition]] law. This has given rise to the heavy use of diagrams in category theory.
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

No one of these is more fundamental than the other. Category theory is a holistic (structural) approach to mathematics that can (through such methods as Lawvere\'s [[ETCS]]) provide [[foundations]] of mathematics and (through [[algebraic set theory]]) reproduce all the different axiomatic set theories; elementary category theory does not need the concept of set to be formulated. Set theory is an analytic approach (element-wise) and can under some conditions reproduce category theory by simply defining all the concepts such as categories, functors and natural transformations needed by sets. The requirements are at least to be able to handle large categories for instance by classes instead of sets and to include an axiom that an inaccessible cardinal exist or an axiom that a Grothendieck universe exist to avoid Russel-type paradoxes. Lawvere pointed out that set theory is axiomatized by a binary membership relation while category theory is axiomatized by a ternary composition relation.

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

+--{.query}

Rafael: I am a bit skeptical if to interpret ETAC as a set theory.

_Toby_:  See [[set theory]] for the contrast between material and structural set theories.  See also [[foundations]]; there may be some overlap between what you intend to write here and what is or should be there.

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

_Rafael_: Ok. I have changed the text and hope it is better now. Thx. I don't read enough in nLab to keep track of all the links so i often skip them, sorry to let others make the links.
=--

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