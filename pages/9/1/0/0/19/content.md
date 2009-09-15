<div class="rightHandSide toc">
[[!include mathematicscontents]]
---
[[!include category theory - contents]]
</div>

#Idea#

+-- {: .un_remark}
#### Origin ####
Category theory was introduced by [[Samuel Eilenberg]] and [[Saunders Mac Lane]] in the 1945 paper **General theory of natural equivalences**. The reason for introducing [[category|categories]] was to introduce [[functor]]s, and the reason for introducing functors was to introduce [[natural transformation]]s (more specifically natural equivalences) in order to define what _natural_ means in mathematics. 

The paper was a clash of ideas from abstract [[algebra]] (Mac Lane) and [[topology]]/[[homotopy theory]] (Eilenberg). It was first rejected on the ground that it had no content but was later published. Unexpectedly category theory has flourished into almost all areas of mathematics, has found many applications outside mathematics and even attempts to build a [[foundations]] of mathematics. 
=--

+-- {: .un_remark}
#### Paradigm ####
The basic idea of category theory is to shift attention from the study of [[object]]s to the study of _maps_ or _relations_ between objects: of (homo)[[morphism]]s between objects. 
=--


+-- {: .un_remark}
#### Examples ####
The archetypical example of a category is the category [[Set]] of [[set]]s and functions between sets. 

The classical examples of categories are [[concrete category|concrete categories]] whose [[object]]s are [[stuff, structure, property|sets with extra structure]] and whose [[morphism]]s are structure preserving functions of sets, such as [[Top]], [[Grp]], [[Vect]].  These are the examples from which the term _category_ derives: these categories literally _categorize_ mathematical structures by packing structures of the same _type_ (same category) and structure preserving mappings between them into a single whole structure, a category.

But by far not all categories are of this type and categories are much more versatile than these classical examples suggest. After all, a [[category]] is just a [[directed graph]] with a notion of composition of its edges. As such it generalizes the concepts of [[monoid]] and [[poset]]. If the category is a [[groupoid]] it generalizes the concept of [[group]] (in a sense called [[horizontal categorification]]).  Thinking of a category as a generalized poset is particularly useful when studying [[limits]] and [[adjoint functors|adjunctions]].

Archetypical examples of non-[[concrete category|concrete]] categories are the [[fundamental groupoid]] of a [[topological space]] and the [[fundamental category]] of a [[directed space]]. 
=--

+-- {: .un_remark}
#### Category theory pointing beyond itself ####
These latter examples already pave the way to the [[homotopy hypothesis]], to the unification between category theory and [[homotopy theory]] in [[Higher Topos Theory|(∞,1)-category theory]] and thereby to [[higher category theory]]. 
=--


+-- {: .un_remark}
#### Terminology ####

Categories were named after the examples of [[concrete category|concrete categories]]. As [[Saunders Mac Lane]] writes

>Now the discovery of ideas as general as these is chiefly the willingness to make a brash or speculative abstraction, in this case supported by the pleasure of purloining words from the philosophers: "Category" from Aristotle and Kant, "Functor" from Carnap (Logische Syntax der Sprache), and "natural transformation" from then current informal parlance.

>([[Saunders Mac Lane]], [[Categories Work|Categories for the Working Mathematician]], 29&#8211;30).

However, the [[category|categories]] of category theory are way more general than these [[concrete category|concrete categories]] and the way Aristotle and Kant use the term is more related to what nowadays is called "type" in [[type theory]].

=--




+-- {: .un_remark}
#### Conceptual unification ####
One major driving force behind the development of category theory is its ability to abstract and unify concepts. General statements about categories apply to each specific [[concrete category]] of mathematical structures. The general notion of [[universal construction]]s in categories, such as [[representable functor]]s, [[adjoint functor]]s  and [[limit]]s, turns out to prevail throughout mathematics and manifest itself in myriads of special examples.
=--

+-- {: .un_remark}
#### Abstract nonsense ####

This abstraction power of category theory has led Norman Steenrod to coin the term _abstract nonsense_ or _general abstract nonsense_ for it. It is being used as in "This property is not specific to this context, it already follows from general abstract nonsense". Peter Freyd expressed a similar feeling by his witticism: 

>"Perhaps the purpose of categorical algebra is to show that which is trivial is trivially trivial."

But abstract nonsense still tends to meet with some resistance. In the preface of his 1965 book _Theory of Categories_ Barry Mitchell writes:

>A number of sophisticated people tend to disparage category theory as consistently as others disparage certain kinds of classical music. When obliged to speak of a category they do so in an apologetic tone, similar to the way some say, "It was a gift &#8211; I've never even played it" when a record of Chopin Nocturnes is discovered in their possession. For this reason I add to the usual prerequisite that the reader have a fair amount of mathematical sophistication, the further prerequisite that he have no other kind.
=--


#What is category theory?#

**Category theory** is so useful because it can be seen from so many perspectives.

###In the narrow sense###

* The theory of [[category|categories]] as [[essentially algebraic theory|essentially algebraic structures]] with several objects and a relation (morphism) "algebra" on these objects. Structures in ordinary [[algebraic theory|abstract algebra]], like [[monoid|monoids]], have only one object. This theory also include [[functors]] between categories and [[natural transformation|natural transformations]].

* Categories may be regarded as 1-dimensional [[directed space]]s. 

  A precise version of this statement is obtained in the sense of the [[homotopy hypothesis]]: this asserts that [[infinity-groupoid|∞-groupoids]] are the same as (nice) [[topological space|space]]s. It is in this sense that [[(infinity,1)-category|(∞,1)-categories]] are like (nice) [[directed space]]s. (One may take this as the _definition_ of nice directed space.) An ordinary category is precisely an [[(∞,1)-category]] in which all [[k-morphism]]s of dimension $k \gt 1$ are trivial in some precise manner. So it is in this sense that categories are precisely the 1-dimensional (nice) directed spaces.

  More concretely, if one thinks of an [[(∞,1)-category]] as being realized as a [[quasi-category]] given by a [[simplicial set]], the above turns into the maybe more familiar statement that categories may be identified with precisely those [[simplicial set]]s whose [[Segal map]]s are isomorphisms. 

  When distinguishing the category itself from the simplicial set that it corresponds to one says that the simplicial set is the [[nerve]] of the category. See there for more on this.

* Much of ordinary mathematics can be thought of as taking place [[internalization|inside]] the archetypical category [[Set]] of sets. In as far as any other category may be thought of as a generalization of $Set$, a category is a **[[universe]]** inside which mathematics may take place.


* A theory of models for [[homotopy type]]s. In [[Alexander Grothendieck|Grothendieck's]] approach to homotopy theory he called $Cat$ together with the class of functors that induced weak equivalences on nerves a [[fundamental localizer]]. See [[the homotopy theory of Grothendieck]].

* A description of partial [[symmetry|symmetries]], in the sense that [[group]]s describe symmetries.

* A generalized theory of [[representations]]. In this view every functor is a representation of its domain in its codomain and natural transformations are the [[intertwining operator]]s between representations.

* The theory of [[directed graph|directed multipseudographs]] with a [[composition]] law and identity loops. This has given rise to the heavy use of diagrams in category theory.

* A theory of [[type theory|type theories]]. See objects as types and morphisms as mappings between types. Every category\'s [[internal language]] is a type theory and every type theory of appropriate form defines a category, the type theory\'s [[free model]].

* A theory of [[deductive system]]s. By assimilating a category\'s objects to statements or formulas and morphisms to deductions (or proofs), a category can be presented equationally as a certain kind of deductive system (with an equivalence relation on deductions).

* A theory of [[presheaves]] with some properties on the full subcategory $[0] \overset{\rightarrow}{\underset{\rightarrow}\leftarrow} [1] \overset{\rightarrow}{\underset{\rightarrow}{\overset{\leftarrow}{\underset{\leftarrow}\rightarrow}}} [2]$ of $\Delta$.

* A theory of [[Cat]], the $2$-[[2-category|category]] of categories. This is axiomatized in Lawvere\'s [[ETAC]].

###In the wide sense###

* A new [[foundations|foundation of mathematics]] that focuses attention on structural issues and away from how mathematical objects are 'built up' as sets. One limited way is to see [[topos|toposes]] as a foundation of mathematics. By simply replacing the category Set by a topos, since they are modeled after Set. For a broader foundation more sophisticated structures are needed such as higher dimensional categories. 

* A unifying tool and language in [[mathematics]]. Most of mathematics (especially modern mathematics) can be regarded as category theory since it is related to category theory in the way that different objects (and mappings between them) studied in different branches of mathematics form categories. Other structures used in categore theory also appear throughout mathematics.

* An organizational tool in [[mathematics]].

* An abstraction of an abstraction of an abstraction of .... The first level is [[set]]s and is most concrete. This is abstracted to categories (only some categories are categories of sets, hence the abstraction). The next abstraction is to categories of categories or more generally $2$-[[2-category|categories]]. This can be iterated to $n$-[[n-category|categories]] and [[infinity-category|indefinitely]]. This could be called the theory of abstractions.

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

Therefore there are many notions of equivalence in category theory (both [[equivalence]] in categories) and ([[equivalence of categories]]) to solve this obstacle.

For the theorem accepted as the fundamental theorem of category theory see the [[Yoneda lemma]].


#Contrast with set theory#
Here set theory is assumed to be a theory of the usual concept of sets, that is *material* [[set theory]].

No one of these is more fundamental than the other as a foundation of mathematics. Category theory is a holistic (structural) approach to mathematics that can (through such methods as Lawvere\'s [[ETCS]]) provide [[foundations]] of mathematics and (through [[algebraic set theory]]) reproduce all the different axiomatic set theories; elementary category theory does not need the concept of set to be formulated. Set theory is an analytic approach (element-wise) and can reproduce category theory by simply defining all the concepts in the usual way, as long as one include a technique to handle large categories (for instance by using [[class]]es instead of sets, or by including as an axiom that an uncountable [[inaccessible cardinal]] exists or even that [[Grothendieck universe]]s exist). 

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

The process of going from sets to categories is a special case of [[categorification]] and the reverse process is a special case of [[decategorification]].

For a philosophical consideration of foundations covering and comparing sets, structuralism [a la Bourbaki?] and categories, see the article

* Sets, categories and structuralism - Costas Drossos


#Generalizations and other structures#

##Generalizations of categories##

There are generalizations of categories in the sense that they are categories with extra structure which reduce to categories when the extra structure is trivial.

* [[internal category|Internal categories]]
* [[enriched category|Enriched categories]]
* [[category over an operad|Categories over operads]]
* [[multicategory|Multicategories]]
* [[polycategory|Polycategories]]
* [[supercategory|Supercategories]]
* [[allegory|Allegories]]
* [[actegory|Actegories]]

##Other structures##

These are a part of category theory even if they are not categories or reduce to categories as a special case.

* [[strict n-category|Strict n-categories]]
* [[weak n-category|Weak n-categories]]
* [[multiple category|Multiple categories]]
* [[derivation scheme|Derivation schemes]] (for deriving categories)
* [[sesquicategory|Sesquicategories]]
* [[computad|Computads]] (a special case of a derivation scheme when the underlying category is a free 2-category)
* [[operad|Operads]]
* [[simplicial set|Simplicial sets]]
* [[opetopic set|Opetopic sets]]
* [[complicial set|Complicial sets]]
* [[pseudocategory|Pseudocategories]] (nonstrict internal categories)
* [[monad|Monads]]
* [[sketch|Sketches]]
* [[doctrine|Doctrines]]


#Applied category theory#

Here are some fields to which category theory has been applied; ultimately we should have articles on all of them.

* [[physics]] (ex: categorical spacetime in quantum gravity, the category of elementary particles and particle interactions, graphical representation of quantum systems in quantum mechanics, AQFT, higher gauge theory, Feynman diagrams, quantization of physical systems and string theory)
* [[computer science]] (ex: data types, artificial intelligence, programming language semantics)
* [[categorical dynamics]]
* [[neural network]]s
* [[psychology]] (ex: perception, cognition, consciousness, teaching, knowledge)
* [[chemistry]] (the category of chemical elements and chemical reactions)
* [[nuclear physics]] (the category of atomic nuclei and nuclear reactions, graphical calculus for spin)
* [[biology]] (ex: detecting life, organismic supercategories)
* [[linguistics]]
* [[philosophy]]
* [[music]]


#References#

Category theory textbooks for which the $n$Lab currently provides detailed linked indexes are

* Kashiwara and Schapira, [[Categories and Sheaves]].

* Ieke Moerdijk and Saunders Mac Lane, [[Sheaves in Geometry and Logic]]

Other standard references include:

* [[Saunders Mac Lane]], _[[Categories Work|Categories for the working mathematician]]_, 2nd ed. 
* [[Steve Awodey]], _Categories for everybody_. 
* [[Francis Borceux]], _Handbook of categorical algebra_, vol 1--3. 
* [[Colin McLarty]], _Elementary categories, elementary toposes_. 
* [[Jiri Adamek]], [[Horst Herrlich]], and [[George Strecker]], _Abstract and concrete categories: the joy of cats_. [free online](http://katmat.math.uni-bremen.de/acc/acc.pdf)
* [[Michael Barr]] and [[Charles Wells]], _Toposes, triples and theories_. [free online](http://www.cwru.edu/artsci/math/wells/pub/ttt.html)
* [[Robert Goldblatt]], _Topoi, the categorial analysis of logic_.
[free online](http://historical.library.cornell.edu/cgi-bin/cul.math/docviewer?did=Gold010&amp;seq=&amp;view=50&amp;frames=0&amp;pagenum=1)
* [[Tom Leinster]], _Higher operads, higher categories_ [free online] (http://arxiv.org/PS_cache/math/pdf/0305/0305049v1.pdf)
* [[Eugenia Cheng]], [[Aaron Lauda]], _Higher-dimensional categories: an illustrated guide book_ [free online] (http://cheng.staff.shef.ac.uk/guidebook/guidebook-new.pdf)
* [[Peter Johnstone]], _Topos theory_
* [[Jacob Lurie]], _[[Higher Topos Theory]]_ [free online] (http://www-math.mit.edu/~lurie/papers/highertopoi.pdf)
* Project description: higher categorical structures and their applications [free online] (http://www.math.uchicago.edu/~may/NCATS/ForWeb.pdf)



#Discussion#

Here are some discussion boxes that used to be inside the above text but have been largely resolved by now.

+-- {: .query}

>the following discussion originated from an earlier version of the above two items on "categories as mathematical universes" and "categories as spaces". The new form of the above items is supposed to be a result and wrap-up of the discussion below. But if it is not regarded as such by everyone, we need to continue discussing.  

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

[[Urs Schreiber]]: okay, I get it. So then I suggest that we say what you all just said more explicitly. Here is a suggestion for an alternative to the above sentences as far as "mathematical universes" are concerned:

**suggestion**

Much of ordinary mathematics can be thought of as taking place [[internalization|inside]] the the archetypical category [[Set]] of sets. In as far as any other category may be thought of as a generalization of [[Set]], a category is a _mathematical universe_ inside which mathematics may take place.

Of course, without further assumptions on the category, there is very little math that can be formulated inside it. For instance in the [[terminal category]] everything is trivial. But few extra properties and structures are usually necessary to provide already interesting structure.

For instance if the category is equipped with the structure of a [[site]] already many geometrical notions exist inside it. If it is [[finitely complete category]] one can already do a lot of mathematics inside it. If the category is a [[topos]], one can do finitist impredicative constructive ordinary mathematics inside it.

**end of suggestion**

What do you think? I may be ignorant, but possibly some readers interested in this page here are more ignorant than I am, so maybe if I find comments of the above kind helpful, others will, too.

[[David Roberts]]: Perhaps the following as a rewrite for your second paragraph:

**Start suggestion**

For instance if the category is equipped with the structure of a [[site]] geometrical notions, such as defining arrows locally on the domain with patching conditions (or more generally descent theory), exist inside it. If it is [[finitely complete category]], the existence of (finite) products and terminal objects means that varieties of algebras can be defined. If the category is a [[topos]], one can do finitist impredicative constructive ordinary mathematics inside it. Extra conditions on the category, such as being a _boolean_ topos or being a _superextensive_ site, bring the internal mathematics closer to that of $Set$.

**End suggestion**

With the appropriate links inserted (not that I like to over-burden the elves of the golf department, but it is locally late).

[[Urs Schreiber]]: okay, I moved my first suggested paragraph and your refined suggestion for the second paragraph out of the query box and into the main text above now.

_Toby_:  I like what is written above (with one exception), but I think that it\'s too much for this list.  We should have a brief sentence and then link to other articles that explain more.  To some extent, this sort of thing is at [[internalization]] and [[internal language]], but I propose to use these paragraphs as the start of a new entry [[universe]] (which currently redirects, somewhat parochially, to [[Grothendieck universe]]).  I\'ll probably do that myself in about an hour.  (The exception is this:  The wording implies that nothing can be formulated in the trivial category, but in fact *everything* can be formulated there ---up to and including a proof of $\bot$--- and *that* is what makes it useless: it is too strong, not too weak.)

_Toby_:  OK, I\'m doing this.

_Rafael_: Sorry for the delay but i have so much to do and i am not done with everything yet.

Toby, i like what you wrote about mathematical universes.

Urs, Directed space is better than space, thank you for the addition. I also like your compilation of the discussion and its corrected version by David.

Then, just a comment on "The theory of categories as primitive mathematical universes". You should be able to do some kind of geometry in a universe, i would say some kind of homotopy theory. But it is in fact a good idea to separate directed space and mathematical universe.

I suppose that the smalness condition on categories wasn't somehow necessary when taking the nerve since it has been removed.

Now that this is taken care of, to the discussion about the difference between CW-complexes and topological spaces.
I have done some research and think the discussion is really about how you view sets. There is an algebraic difference (but not geometric) between a set of cells and a set of points that make up cells.

I think that Nakaharas lovely book Geometry, Topology and Physics is to blame. It is here that this and related definitions rooted in my mind. He is speaking about simplicial complexes but the same holds for the more general CW-complexes or they would not be complexes (p 67):

"Let K be a set of finite number of simplexes in $R^m$. If these simplexes are nicely fitted together, K is called a simplicial complex. ...". He calls |K| the polyhedron of the simplicial complex. I have also seen 4 other definitions (not including the below) and only this one sees a "CW-complex" as a set of simplicies. A very clear minority. The other definitions are not identical either but close. No wonder no one understands mathematics, everyone say something different!!!

On the other hand a 1D CW-complex is a graph, as John remarked. A graph is an ordered pair ({vertices},{edges between vertices}) which nicely fits with Nakaharas definition.

This should explain that i was not thinking about globular sets (see Davids answer).

I must say that i don't like wikipedias definition of a CW-complex. See instead the definition at [planetmath](http://planetmath.org/encyclopedia/CWComplex.html) (which answers my question about which topology to impose, the weak topology) and [mathworld](http://mathworld.wolfram.com/CW-Complex.html).

So now i have to decide what a CW-complex is. If i go with the majority of definitions, what should i call a "set of nicely glued simplicies"? I can't call it a simplicial complex.

Mike Schulman, Thanks for your comment on "enriched internal categories" below.

Finally, an addition to primitive spaces just for completeness: Two separated points (when taken out) of a "set" (so there are no relations to other points) are of the same type if there exist a structure preserving mapping between the points such as a homomorphism. (i don't know precisely what this means for fractals so don't ask me about it.) It might say more about them or not.

_Rafael_: Since no one wants to reply, this discussion can be deleted?

[[Urs Schreiber]]: as far as I am aware a [[simplicial complex]] is essentially a special kind of [[simplicial set]], which means that it is a collection of _abstract_ simplices. You just remember that "here are 5 3-simplices and they touch each other in such and such a way" but you don't actually regard these simplices as being the standard concrete simplices as subsets of $\mathbb{R}^n$s, say. Instead, when you want to do that you pass to tthe [[geometric realization]] of the simplicial set/complex. That realizes each abstract simplex as a topological simplex. And the result of _that_ is then a CW-complex.

_Rafael_: Urs, Do you regard CW-complexes as a generalization of simplicial complexes?

Then, why is nobody using the term topological complex for the geometric realization of a simplicial complex. And analogously topological CW-complex for what the majority regard as a CW-complex. It would be so much easier to understand the logic and consistency then.

_[[John Baez]]_: yes, Rafael, a CW complex is a generalization of a simplicial complex.  It sounds like you're having trouble finding the standard definition of CW complex.  There is a standard definition, and you can find it on <a href = "http://www.math.cornell.edu/~hatcher/AT/ATch0.pdf#page=5">page 5</a> of Chapter 0 of Allen Hatcher's free online topology book.  By the way, this book is a good way to learn algebraic topology.

By the way, Urs, a [[simplicial complex]] is most elegantly defined as a set $S$ equipped with a collection of finite nonempty subsets such that if $X$ is in the collection and $Y \subseteq X$ is nonempty, then $Y$ is in the collection.  We think of $S$ as the set of vertices and any $(n+1)$-element set $X$ in the collection as an $n$-simplex.  Unlike a simplicial set, these simplices do not have an <i>ordered</i> set of vertices!   This concept is less useful than that of a simplicial set, but still very useful for many reasons.

[[Urs Schreiber]]: hm, I know that a simplicial complex is a simplicial set after we choose an ordering on the elements. That's why I said that a simplicial complex "is" not a CW complex, but that its [[geometric realization]] is.

But I see now that the Wikipedia entry on simplicial complexes says that "a simplicial complex is a topological spaces such that...". Is that a really good way to say it?

[[Todd Trimble]]: No, I think it's a terrible way to say it. What was evidently meant is that a simplicial complex is a type of presentation of a certain type of space (called polyhedra or polyhedral spaces), but one trouble is that there are many ways to triangulate such a space, so that the simplicial complex is not a priori given as an underlying structure. Another: consider the categories. A map between simplicial complexes is inherently much more restrictive than a continuous map between polyhedra. 

I'm also not too sympathetic to the idea that simplicial sets are "more abstract" than simplicial complexes, but as we Americans sometimes say, "whatever". 

[[Urs Schreiber]]: thanks, Todd. Concerning "abstract". I think I didn't say that simplicial complexes are more abstract than simplicial sets. What i said is that a cell in a simplicial set is an "abstract simplex" which becomes a concrete geometrical simplex after geometric realization.

Anyway, concerning Raphael's question: I am still thinking now that my original reply was correct: a simplicial complex (and a simplicial set) _is_ not a CW complex, but gives rise to one after [[geometric realization]]. But John replied differently above. We need to find some agreement.

Raphael, remind me: for which part ofthe entry here is this discussion relevant. I mean: what is the concrete paragraph whose phrasing we want to streamline?

[[Mike Shulman]]: I agree that simplicial complexes and simplicial sets _give rise to_ CW complexes after geometric realization.

[[Todd Trimble]]: I'm sorry, Urs, that I didn't make clear that I was criticizing the **WP article** (not you) over the sentiment that simplicial sets are more abstract than simplicial complexes. 

[[Rafael Borowiecki]]: No John, it's something worse than finding a standard definition. It's a consistency issues. But good definitions of advanced concepts are often hard to come by such as a definition of a sylleptic monoidal category that don't take three pages.

When i read i often first make a consistency check and surprisingly often i find that the definition or equation is inconsistent so it doesn't make sense. I call it data missmatch. The most typical example is when something that is a set becomes a map (that must go between sets)! They are conceptually different just as categories and functors are! Fortunately i have never seen a category being called a functor. There might be several reasons for this missmatch... I can only guess that what is ment is the image of the map.

I will remind Urs and others what this discussion is about. First it was about the definition of a CW-complex (which came up as a suggestion how a category can be a space, then i thought of it as a set {cell1,cell2,...} with some conditions on the cells). Is it a set of cells or a set that is the geometric realization of that? I now see it as a the later. I found out the problem with the definition. The way i was thinking is in the above sentence "There is an algebraic difference (but not geometric) between a set of cells and a set of points that make up cells". This means precisely that if you apply the geometric realization to a set of cells you will get a set of points that constitute the cells. Fine so far. Now i messed up with something as elementary as the union. A CW-complex is defined as a union of topological cells, say in $R^m$. This is not a set of cells but of points of the cells! Now it makes sense. Hence i still don't understand how a 1D CW-complex can be a graph of the form ({vertices},{edges between vertices}). Data missmatch again. I think of a segment as the geometric realization of an edge and do not consider them as equal.

Now the discussion is about what a simplicial complex is (some like to think of simplicial sets too). [Wikipedia](http://en.wikipedia.org/wiki/Simplicial_complex) and [mathworld](http://mathworld.wolfram.com/SimplicialComplex.html) see them as made up of points (the geometric realization of simplicies) instead of (abstract) simplicies, which is horrible as Todd pointed out. [Hazevinkels encyclopedia](http://eom.springer.de/S/s085360.htm) is not so clear but i think it also see a simplicial complex as a set of points. I would say their definition is wrong. Nakahara just speaks of simplicies in $R^m$ instead of abstract simplicies but gets it right. The book Cellular structures in topology by Fritsch and Piccinini takes the correct abstract approach that a simplicial complex is a finite set closed under subset formation but is not as explicit as i would wish. I think the best definition is at [planet math](http://planetmath.org/encyclopedia/SimplicialComplex.html).

So i would agree with Urs that the geometric realization of a simplicial complex is a CW-complex (which makes me now wonder what a complex is, geometrically i always thought of it as the space that represents or is formed by a chain complex in homological algebra, and not like a CW-complex, never mind). This explains that my question "[Are] CW-complexes ... a generalization of simplicial complexes" was about consistency. If CW-complexes (that are the geometric realization of a simplicial complex) generalize simplicial complexes, i can't understand how. I would like to hear from John and others about this and the graphs. I am now trying to see if there is a way out with Euclidean cell complexes. This is really not new stuff but i tend to forget things i don't use for a long time such as abstract simplicial geometry.

[[Mike Shulman]]: At this level of discussion, there are actually two things that one might mean by "CW complex," namely (1) a space that _can be_ built by attaching cells in such-and-such a way, or (2) a space _together with a recipe_ for constructing it by attaching cells in such-and-such a way.  People are often kind of inconsistent about which they mean, but usually it doesn't cause any trouble.  If by "CW complex" you mean (2), then it isn't just a topological space, but starts to look a little more like a simplicial complex.  (I still don't think that simplicial complexes _are_ CW complexes, though, even with that definition.)

BTW, a CW complex isn't really a union of points in $R^n$, rather it is an abstract topological space constructed by gluing together cells.  Not every CW complex admits an embedding into any $R^n$.

_Rafael_: Correction, assuming presheaves are equivalent to functors i did see a category be called a functor. It is above on this page, the seccond from the bottom explanation what category theory in the narrow sense is, where the $\Delta$ category is.

Mike, I like your (2) better.

[[Todd Trimble]]: Rafael, there's no problem (i.e., no type error or data mismatch problem) with the fact that there's a nerve functor $N: Cat \to Set^{\Delta^{op}}$, sending categories to presheaves on $\Delta$. This turns out to be full and faithful, so that $Cat$ as a category is equivalent to the category of presheaves on $\Delta$ of a certain type (those satisfying a certain exactness condition). When we say categories "are" certain presheaves on $\Delta$, we don't mean that literally, but rather that any statement in the language of category theory that is true for $Cat$ must also be true for the category of presheaves on $\Delta$ of this type, and conversely. In other words, for all categorical intents and purposes, we might as well consider $Cat$ "the same" as this category of presheaves. That's what is meant. 

This is similar to saying that the abelian group of integers, while not literally the same as the abelian group of even integers, is nevertheless isomorphic to it: they satisfy exactly the same properties as abelian groups. In that sense, they can be considered "the same". 

_Toby_:  I don\'t think that John\'s reference is very helpful at all!  Phrasing like 'A space $X$ constructed in this way' invites confusion.  John seems to want us to take it to mean that a CW complex is a topological space with certain properties.  OK, but then (page 6) Hatcher says that a graph (meaning a pseudograph in the terminology currently at [[graph]]) is a $1$-dimensional CW complex.  But it is not true that graph is a topological space with certain properties, since $\bullet - \bullet - \bullet$ is homeomorphic to $\bullet - \bullet$, but these are not isomorphic graphs.  (There is also the more technical mistake that a graph will have a dimension smaller than $1$ if it has no edges, which is possible.)  You could define a graph as a space with certain *structure*, but then you had better be clear about what it means to preserve the structure, which Hatcher is not.

Historically, simplicial complexes were originally spaces, or perhaps spaces equipped with a triangulation (compares Mike\'s (1) and (2) above); then came *abstract* simplicial complexes (merely collections of sets of points as John slickly defined them) whose geometric realisations were the *concrete* simplicial complexes that people had studied before.  This strikes me as very sensible language, and I would want to apply it to CW complexes just as well.  Then a graph may be defined as a $(\leq 1)$-dimensional abstract CW complex (or equivalently, as it happens, a $(\leq 1)$-dimensional abstract simplicial complex), but its geometric realisation is a space of a certain kind, whose homeomorphisms need not correspond to graph isomorphisms.  Another benefit is that we can sensibly speak of *smooth* functions between CW complexes, rather than just *continuous* ones, if we like; many notions of geometric realisation are open to us.

I had a bunch more written about when things should be considered the same, but I lost it all to careless button-pushing ('_').  Suffice to say that it\'s much safer to consider categories 'the same' as certain presheaves on $\Delta$ than to consider integers 'the same' as even integers, precisely because the type mismatch will alert you to the use of an [[equivalence of categories]], which you can then track down.
=--

+--{.query}

>here is a discussion thaat started with a previous version of the paragraph on "abstract nonsense". This paragraph has now been changed according to this discussion. If there is still need to discuss, we need to revive this query box here.

Zoran: I think that the wikipedia [article](http://en.wikipedia.org/wiki/Abstract_nonsense) is far more up to the point than this paragraph above. Namely the main practioners and founders of the method did use the term very early meaning clean and general arguments rather than obscure and specific to special cases. The pejorative conotation is neither original nor primary. The above paragraph makes an impression that the term abstract nonsense is primarily pejorative and orginating mainly from the uncategorical community.

Todd: I think Zoran's basically right. The phrase is believed to have been coined by Norman Steenrod, who should be considered as friendly towards categorical methods. When snappily deployed, it's more likely than not an indication of the speaker's sophistication. Compare the deep truth underlying Freyd's witticism: "Perhaps the purpose of categorical algebra is to show that which is trivial is trivially trivial."
=--



[[!redirects abstract nonsense]]
[[!redirects general abstract nonsense]]
[[!redirects applied category theory]]