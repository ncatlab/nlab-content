<div class="rightHandSide toc">
[[!include mathematicscontents]]
---
[[!include category theory - contents]]
</div>

#Contents#
* tic
{:toc}


#Idea#

+-- {: .un_remark}
###### Origin ####
Category theory was introduced by [[Samuel Eilenberg]] and [[Saunders Mac Lane]] in the 1945 paper **General theory of natural equivalences**. The reason for introducing [[category|categories]] was to introduce [[functor]]s, and the reason for introducing functors was to introduce [[natural transformation]]s (more specifically natural equivalences) in order to define what _natural_ means in mathematics. 

The paper was a clash of ideas from abstract [[algebra]] (Mac Lane) and [[topology]]/[[homotopy theory]] (Eilenberg). It was first rejected on the ground that it had no content but was later published. Unexpectedly category theory has flourished into almost all areas of mathematics, has found many applications outside mathematics and even attempts to build a [[foundations]] of mathematics. 
=--

+-- {: .un_remark}
###### Paradigm ####
The basic idea of category theory is to shift attention from the study of [[object]]s to the study of _maps_ or _relations_ between objects: of (homo)[[morphism]]s between objects. 
=--


+-- {: .un_remark}
###### Examples ####
The archetypical example of a category is the category [[Set]] of [[set]]s and functions between sets. 

The classical examples of categories are [[concrete category|concrete categories]] whose [[object]]s are [[stuff, structure, property|sets with extra structure]] and whose [[morphism]]s are structure preserving functions of sets, such as [[Top]], [[Grp]], [[Vect]].  These are the examples from which the term _category_ derives: these categories literally _categorize_ mathematical structures by packing structures of the same _type_ (same category) and structure preserving mappings between them into a single whole structure, a category.

But by far not all categories are of this type and categories are much more versatile than these classical examples suggest. After all, a [[category]] is just a [[directed graph]] with a notion of composition of its edges. As such it generalizes the concepts of [[monoid]] and [[poset]]. If the category is a [[groupoid]] it generalizes the concept of [[group]] (in a sense called [[horizontal categorification]]).  Thinking of a category as a generalized poset is particularly useful when studying [[limits]] and [[adjoint functors|adjunctions]].

Archetypical examples of non-[[concrete category|concrete]] categories are the [[fundamental groupoid]] of a [[topological space]] and the [[fundamental category]] of a [[directed space]]. 
=--

+-- {: .un_remark}
###### Category theory pointing beyond itself ####
These latter examples already pave the way to the [[homotopy hypothesis]], to the unification between category theory and [[homotopy theory]] in [[Higher Topos Theory|(∞,1)-category theory]] and thereby to [[higher category theory]]. 
=--


+-- {: .un_remark}
###### Terminology ####

Categories were named after the examples of [[concrete category|concrete categories]]. As [[Saunders Mac Lane]] writes

>Now the discovery of ideas as general as these is chiefly the willingness to make a brash or speculative abstraction, in this case supported by the pleasure of purloining words from the philosophers: "Category" from Aristotle and Kant, "Functor" from Carnap (Logische Syntax der Sprache), and "natural transformation" from then current informal parlance.

>([[Saunders Mac Lane]], [[Categories Work|Categories for the Working Mathematician]], 29&#8211;30).

However, the [[category|categories]] of category theory are way more general than these [[concrete category|concrete categories]], and the way Aristotle and Kant use the term is not particularly related to what Eilenberg & Mac Lane did with it.

+-- {: .query}
I removed the refernce to type theory in the last paragraph, since I was probably the source for it, and it goes beyond what I meant to say or what I think is justified.  ---Toby
=--

=--




+-- {: .un_remark}
###### Conceptual unification ####
One major driving force behind the development of category theory is its ability to abstract and unify concepts. General statements about categories apply to each specific [[concrete category]] of mathematical structures. The general notion of [[universal construction]]s in categories, such as [[representable functor]]s, [[adjoint functor]]s  and [[limit]]s, turns out to prevail throughout mathematics and manifest itself in myriads of special examples.
=--

+-- {: .un_remark}
###### Abstract nonsense ####

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

There are generalizations of categories in the sense that they are categories with extra structure which reduce to structures equivalent to categories when the extra structure is trivial.

* [[internal category|Internal categories]]
* [[enriched category|Enriched categories]]
* [[category over an operad|Categories over operads]]
* [[strict n-category|Strict n-categories]]
* [[weak n-category|Weak n-categories]]
* [[multiple category|Multiple categories]]
* [[multicategory|Multicategories]]
* [[polycategory|Polycategories]]
* [[supercategory|Supercategories]]
* [[allegory|Allegories]]
* [[actegory|Actegories]]
* [[simplicial set|Simplicial sets]]
* [[opetopic set|Opetopic sets]]
* [[complicial set|Complicial sets]]


##Other structures##

These are a part of category theory even if they are not categories or reduce to categories as a special case.

* [[operad|Operads]]
* [[derivation scheme|Derivation schemes]] (for deriving categories)
* [[computad|Computads]] (a special case of a derivation scheme when the underlying category is a free 2-category)
* [[pseudocategory|Pseudocategories]] (nonstrict internal categories)
* [[sesquicategory|Sesquicategories]]
* [[monad|Monads]]
* [[sketch|Sketches]] (models of sketches give categories or more generally internal categories)
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

## Etymology

* Aristotle, _[Categories](http://ebooks.adelaide.edu.au/a/aristotle/categories/)_

* Kant

* C.S. Peirce, &ldquo;[On a New List of Categories](http://www.cspeirce.com/menu/library/bycsp/newlist/nl-frame.htm)&rdquo;

* Carnap, _[The Logical Syntax of Language](http://books.google.com/books?id=Yf9R6WFFLhYC&printsec=frontcover)_, _cf._ &ldquo;[Functor](http://books.google.com/books?id=Yf9R6WFFLhYC&printsec=frontcover#v=onepage&q=Functor&f=false)&rdquo;

+-- {: .query}

[[Todd Trimble]]: Can I ask what you mean when you call these "precursors"?

[[JA]]:  Anticipations, 4-runners, 4-shadowings, philosophical underpinnings &hellip;

_Toby_:  If I may presume to translate Todd\'s question for him:  Why do you think that Aristotle, Kant, Peirce, and Carnap are precursors, anticipations, forerunners, foreshadowings, or philosophical underpinnings of category theory?  The only thing that I can think of myself is that Eilenberg & Mac Lane borrowed the term 'category' from Aristotle & Kant and borrowed the term 'functor' from Carnap.  Otherwise, I do not see any connection.

However, I don\'t object to this list; it might or might not work better on a separate page (although it\'s short enough that it fits here well enough).  I just changed its heading to something that seems more appropriate to me. 

_Todd_: Yes, I thought what Jon wrote might have been what he had in mind (but I didn't want to put words in his mouth, so I left the question open-ended), and then what Toby wrote would have been my follow-up question. Mind you, I am open to the suggestion that there may be philosophical antecedents or anticipations of the notion of category in these earlier developments (and I'd find that very interesting), but it's not clear to me how that would be the case in any precise sense. I think Toby's recasting this as 'Etymology' is far safer, until more evidence is brought to the table.

[[JA]]: I don't think that E & MacL were simply punning, but I doubt if it's necessary to take up more space here, as this page already bogs down my connection.  Just for one thing to think about, though, you might reflect on the question of "natural kinds", and the part that it played in the thought of Aristotle, Kant, and Peirce. 

_Todd_: It's clear enough (especially in view of examples of 'large categories' which consist of various species of structured sets) that "categories" was not an altogether inappropriate choice of word, but that's speaking at a pretty broad philosophical level. The more specific sense of category as involving morphisms and their compositional algebra is a different matter. It's not clear (to me, yet) that the germ of any such sense can be traced to any of the aforementioned authors; IMO a more convincing precursor in this wise might be Klein's Erlangen Program. 

As for "functor": it's even less clear to me that there was any tight connection in Mac Lane's mind between Carnap's use and his (Mac Lane's) own appropriation. I suspect that it was meant more to conjure an association with "function" than with Carnap particularly.

[[JA]]: Brother, can you paradigm ...

> __Paradigm.__  The basic idea of category theory is to shift attention from the study of [[object]]s to the study of _maps_ or _relations_ between objects: of (homo)[[morphism]]s between objects.

See also:

1. Aristotle's "[Paradeigma](http://mywikibiz.com/Inquiry#Analogy)", or reasoning by analogy.  Analogies and metaphors are kissing cousins to morphisms.
1. Peirce's "[Pragmatic Maxim](http://knol.google.com/k/jon-awbrey/pragmatic-maxim/3fkwvf69kridz/6)", which has to do with clarifying concepts by translating them into their operational meanings.

_Todd_: Ah, thanks for drawing attention to this! Now the argument becomes rather more interesting for me. 

In particular, the diagram you drew in your wiki under 'analogy' (speaking to an example from Aristotle) is a perfect concrete illustration of the mathematical notion of [[span]]; even better, you've drawn a _morphism_ of spans (from A to B). Now it happens that a category can be defined as a monoid in the bicategory of spans; if $C_0$ denotes the collection of objects and $C_1$ the collection of morphisms of a category $C$, then the span has the shape 

$$\array{
& C_1 & \\
 dom \swarrow & & \searrow cod\\
C_0 & & C_0
}$$ 

I'll also mention that the connection between analogies and spans has come up in discussion on the blog; our good friend Jim Dolan has drawn attention to this. See Toby's comment [here](http://golem.ph.utexas.edu/category/2006/11/a_categorical_manifesto.html#c006085) and the ensuing discussion. 

=--

#Discussion#

Here are some discussion boxes that used to be inside the above text but have been largely resolved by now.

+-- {: .query}

>the following discussion originated from an earlier version of the above two items on "categories as mathematical universes" and "categories as spaces". The new form of the above items is supposed to be a result and wrap-up of the discussion below. But if it is not regarded as such by everyone, we need to continue discussing.  

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

_Rafael_: Toby, i like your approach to distinguish between abstract CW-complexes and "concrete" CW-complexes. Unfortunately it is not standard. How would you define
a general abstract CW-complex and relate it to abstract simplicial complexes? You could perhaps write or e-mail me your list of "equivalent" things (as much as you can remember and think of it). I also have such a list to sort out. The pattern seems to be skip "is" and use "equivalent to" instead. Which brings me to what Todd answered.

Todd, i have been thinking from time to time about what you wrote. I can't remember everything but this is a very good answer. A clever way to avoid to compare categories and presheaves on $\Delta$. This solves the essence of the problem. But i am not completely satisfied. What is the inverse functor to the nerve functor? Or even better, how do i construct a category from the data of a presheaf on $\Delta$? And do this equivalence preserve all structure? For instance what are the presheaves on $\Delta$ corresponding to abelian categories?

I changed my mind and moved some of the other structures in category theory on this page. After thinking that n-categories reduce to categories (for all n) when the higher cell are trivial. But i am still not sure about pseudocategories. Do they reduce as a special case to categories or internal categories?

I also deleted the beginning of this discussion to not hog some browsers. The page is now less than half as heavy and the beginning is in the history.

_Todd_: Rafael, the nerve functor embeds $Cat$ as a full subcategory of simplicial sets; not every simplicial set arises (up to isomorphism) as the nerve of a category. Those simplicial sets $X: \Delta^{op} \to Set$ that do can be characterized in terms of a property taking certain colimits in $\Delta$ to certain limits in $Set$; I don't feel like spelling this out now, but perhaps later I'll check if anyone has written it down in nLab, and if not I'll see about writing it up myself. The result was first observed by Grothendieck I think. 

So anyway, $Cat$ is not equivalent to simplicial sets, so there is no functor going the other way which is exactly inverse. There is however a left adjoint $F: Set^{\Delta^{op}} \to Cat$ to the nerve functor, which builds a category out of the data of a simplicial set, in which objects are 0-simplexes, morphisms are 1-simplexes (or formal composites of 1-simplexes), and $n$-simplexes for $n \geq 2$ force various equalities between morphisms by interpreting 2-simplexes as commutative triangles, 3-simplexes as commutative tetrahedra, and so on. If this is called the "categorization" of a simplicial set, then the categorization of the nerve of a category gives back the category up to isomorphism (the counit of the adjunction $F \dashv N$ is an isomorphism), but needless to say at this point, the nerve of the categorization of a simplicial set need not give back the simplicial set (up to isomorphism). I imagine a lot of this has been written up in nLab, under [[nerve]] maybe, where the categorization $F$ is formally constructed in terms of coends. 

As for extending this correspondence to embrace other properties/structures/stuff one can put on categories, I've not thought about examples of that sort of thing in detail, but anything not actually [[evil]] in the technical sense can in principle be transported across the equivalence between categories and those certain simplicial sets. 

_Toby_:  (Aside: Since the left adjoint returns the original category up to [[isomorphism of categories|isomorphism]], even some evil things can be so transported.)

_Rafael_: Todd, i thought it was obvious that i was not talking about presheaves on $\Delta$ but about presheaves on a full subcategory of $\Delta$, and the presheaves satisfying some conditions. The thing is that it is a bit long to be spelled out precisely all the time. I would actually be glad if someone could write these conditions down, or at least give a reference where they are wrtten down.

Now, unless the nerve functor defined on this specific symplectic full subcategory of $\Delta$ has an inverse the equivalence between these presheaves and categories break down. This equivalence was what i was really asking for, if it exist. If it don't exist i still don't see how these presheaves can be categories, since there must exist a 1-1 correspondence preserving categorical properties and categorical notions between Cat and these set valued presheaves on this simplicial cateory! Such as an equivalence of categories, no less. Perhaps one of the functors mentioned abowe can be modified so they become inverses. [[simplicial category]] think there is no such equivalence.

Then there was previously some doubt if the nerve can be defined for large categories. I have heard both yes and no here.

However i see the point of how to reconstruct a category from a simplicial set. And that every simplicial set can be "categorified" in the sense that objects become 0-simplexes, morphisms become 1-simplexes,... which is nice. By the way this functor needs a name. Now be careful with the terminology. You are suggesting that simplicial sets are these special Set valued presheaves on $\Delta$! What you mean is probably that these presheaves are equivalent to simplicial sets. So first this equivalence have to be proven. [[simplicial set]] suggest using the Yoneda lemma for the proof. How much this equivalence preserves is an issue, just as for the equivalence between Cat and these set valued presheaves on this special simplicial cateory discussed above. I am still thinking of a simplicial set as constructed out of simplicies. Why would i want to think of it as a presheaf? It might be easier if i knew that.

A category also have a composition that must be preserved, what would it translate to for these presheaves?

Now i remember what i didn't remember to write last time. Would it be ok to think of these presheaves as presentations of categories instead of as categories, since they are (so far supposed to be) equivalent to categories.
Actually, the same for simplicial sets. Would it be ok to think of these presheaves as presentations of simplicial sets? This would be so much easier and clearer.

[[David Roberts]]: Recall that simplicial sets are _defined_ to be presheaves on $\Delta$, and that the value of the functor on the object $[n]$ just returns the set of $n$-simplices...
=--

+--{.query}

>here is a discussion thaat started with a previous version of the paragraph on "abstract nonsense". This paragraph has now been changed according to this discussion. If there is still need to discuss, we need to revive this query box here.

Zoran: I think that the wikipedia [article](http://en.wikipedia.org/wiki/Abstract_nonsense) is far more up to the point than this paragraph above. Namely the main practioners and founders of the method did use the term very early meaning clean and general arguments rather than obscure and specific to special cases. The pejorative conotation is neither original nor primary. The above paragraph makes an impression that the term abstract nonsense is primarily pejorative and orginating mainly from the uncategorical community.

Todd: I think Zoran's basically right. The phrase is believed to have been coined by Norman Steenrod, who should be considered as friendly towards categorical methods. When snappily deployed, it's more likely than not an indication of the speaker's sophistication. Compare the deep truth underlying Freyd's witticism: "Perhaps the purpose of categorical algebra is to show that which is trivial is trivially trivial."
=--


[[!redirects abstract nonsense]]
[[!redirects general abstract nonsense]]
[[!redirects applied category theory]]