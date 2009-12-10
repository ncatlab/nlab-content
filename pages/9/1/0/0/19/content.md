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

##In the narrow sense##

* The theory of [[category|categories]] as [[essentially algebraic theory|essentially algebraic structures]] with several objects and a relation (morphism) "algebra" on these objects. Structures in ordinary [[algebraic theory|abstract algebra]], like [[monoid|monoids]], have only one object. This theory also include [[functors]] between categories and [[natural transformation|natural transformations]].

* Categories may be regarded as 1-dimensional [[directed space]]s. 

  A precise version of this statement is obtained in the sense of the [[homotopy hypothesis]]: this asserts that [[infinity-groupoid|∞-groupoids]] are the same as (nice) [[topological space|space]]s. It is in this sense that [[(infinity,1)-category|(∞,1)-categories]] are like (nice) [[directed space]]s. (One may take this as the _definition_ of nice directed space.) An ordinary category is precisely an [[(∞,1)-category]] in which all [[k-morphism]]s of dimension $k \gt 1$ are trivial in some precise manner. So it is in this sense that categories are precisely the 1-dimensional (nice) directed spaces.

* A theory of **[[universe|universes]]** in which mathematics can be done. Much of ordinary mathematics can be thought of as taking place [[internalization|inside]] the archetypical category [[Set]] of sets. In as far as any other category may be thought of as a generalization of $Set$, a category is a universe inside which mathematics may take place.

* A theory of models for [[homotopy type]]s. In [[Alexander Grothendieck|Grothendieck's]] approach to homotopy theory he called $Cat$ together with the class of functors that induced weak equivalences on nerves a [[fundamental localizer]]. See [[the homotopy theory of Grothendieck]].

* A description of partial [[symmetry|symmetries]], in the sense that [[group]]s describe symmetries.

* A generalized theory of [[representations]]. In this view every functor is a representation of its domain in its codomain and natural transformations are the [[intertwining operator]]s between representations.

* The theory of [[directed graph|directed multipseudographs]] with a [[composition]] law and identity loops. This has given rise to the heavy use of diagrams in category theory.

* A theory of [[type theory|type theories]]. See objects as types and morphisms as mappings between types. Every category\'s [[internal language]] is a type theory and every type theory of appropriate form defines a category, the type theory\'s [[free model]].

* A theory of [[deductive system]]s. By assimilating a category\'s objects to statements or formulas and morphisms to deductions (or proofs), a category can be presented equationally as a certain kind of deductive system (with an equivalence relation on deductions).

* A theory of possibly large [[simplicial sets]] presented by [[class]]-valued [[presheaves]] on the full subcategory $[0] \overset{\rightarrow}{\underset{\rightarrow}\leftarrow} [1] \overset{\rightarrow}{\underset{\rightarrow}{\overset{\leftarrow}{\underset{\leftarrow}\rightarrow}}} [2]$ of the [[simplex category]] $\Delta$. These possibly large simplicial sets must also satisfy the [[Segal condition]]: $X$ a possibly large simplicial set &#8658; the [[Segal map]]s $X_n \to X_1 \times_{X_0} X_1 \times_{X_0} \ldots \times_{X_0} X_1$ are isomorphisms for $n \geq 0$, and; the "middle" face operator $X_2 = X_1 \times_{X_0} X_1 \to X_1$ (that models the [[composition]] in the category) is associative. This very last condition can be skipped if the presheaves are on the full subcategory $[0] \overset{\rightarrow}{\underset{\rightarrow}\leftarrow} [1] \overset{\rightarrow}{\underset{\rightarrow}{\overset{\leftarrow}{\underset{\leftarrow}\rightarrow}}} [2] \cdots [3]$ of $\Delta$ instead. The correspondence is an [[equivalence of categories]] that constructs a category from its [[nerve]] by the categorical realization functor, and the inverse functor that constructs a category\'s nerve is the generalized [[nerve functor]] (a generalization of the nerve functor to have categories as its domain and possibly large simplicial sets as its codomain).

  The category corresponding to a possibly large simplicial set
is constructed as: objects are $0$-simplexes, morphisms are formal composites of $1$-simplexes,
and $n$-simplexes for $n \geq 2$ force various equalities between morphisms by interpreting $2$-simplexes as commutative triangles, $3$-simplexes as commutative tetrahedra, and so on. Composition in the category is modeled in the possibly large simplicial set by the "middle" face operator which in functorial language is $X(f)$, where $f$ is the monomorphism in $\Delta$ from the $2$-element ordinal to the $3$-element ordinal that leaves out the middle element. This equivalence transports in principle anything non-[[evil]] between [[Cat]] and the possibly large simplicial sets satisfying the two conditions above.

* A theory of [[Cat]], the $2$-[[2-category|category]] of categories. This is axiomatized in Lawvere\'s [[ETAC]].


##In the wide sense##

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


#Main principle of category theory and evil#

Category theory has a main principle:

_In any category it is unnatural and undesirable to speak about equality of two objects_.

To develop category theory within set theory (or even within first-order logic with equality) necessarily allows one to discuss [[evil]] by defining categories as [[strict categories]]; some alternative [[foundations of mathematics]] make this impossible, but otherwise it requires discipline to state definitions and theorem without evil.

Therefore there are many notions of equivalence in category theory (both [[equivalence]] in categories) and ([[equivalence of categories]]) to solve this obstacle.

For the theorem accepted as the fundamental theorem of category theory see the [[Yoneda lemma]].


# Contrast to theories of other objects

##Category theory vs. set theory

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

##Category theory vs. order theory

A category may be thought of as a [[categorification]] of a [[poset]] rather than of a [[set]]; much (but by no means all) of category theory also appears in [[order theory]].

See [[category theory vs order theory]] for more discussion.


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
* [[Jacob Lurie]], _[[Higher Topos Theory]]_ [free online](http://www.math.harvard.edu/~lurie/papers/highertopoi.pdf)
* Project description: higher categorical structures and their applications [free online] (http://www.math.uchicago.edu/~may/NCATS/ForWeb.pdf)


#Discussion#

Here are some discussion boxes that used to be inside the above text but have been largely resolved by now.

+-- {: .query}

>the following discussion originated from an earlier version of the above two items on "categories as mathematical universes" and "categories as spaces". The new form of the above items is supposed to be a result and wrap-up of the discussion below. But if it is not regarded as such by everyone, we need to continue discussing.  

_Rafael_: Please don't see me as complaining and opposing almost everything you write. I just like to get to the bottom of problems using logic. Which may involve often skipped details. Just because i write something it don't mean i am against the opposite of what i wrote. When i ask something i have usually tried to figure it out first, and in general it feels like there are many things in fairly basic category theory not written down or written out (explicitly as they should be). Mike Shulmans explanation of nerves of large categories being one of them. It should be added to [[nerve]].

Is this a good replacement for the sentence at the top of the page that started this last discussion?

**suggestion**

A theory of enlarged [[simplicial set|simplicial sets]] (in the sense of enlarging sets to classes) presented by Set-valued [[presheaf|presheaves]] on the full subcategory $[0] \overset{\rightarrow}{\underset{\rightarrow}\leftarrow} [1] \overset{\rightarrow}{\underset{\rightarrow}{\overset{\leftarrow}{\underset{\leftarrow}\rightarrow}}} [2]$ of $\Delta$ (where the [[simplex category]] $\Delta$ also contains large simplicies). The enlarged simplicial sets must also satisfy the condition: X an enlarged simplicial set $\Rightarrow$ the Segal maps $X_n \to X_1 \times_{X_0} X_1 \times_{X_0} \ldots \times_{X_0} X_1$ are isomorphisms for $n \geq 0$. The correspondence constructs a category from its [[nerve]] by the categorical realization functor, and the inverse functor constructing a categorys nerve is the generalized nerve functor (generalization of the nerve functor to have categories as its domain and enlarged simplicial sets as its codomain).

**end suggestion**

I recall this condition on the simplicial sets Todd gave. I did't put it this way but i was asking for it in terms of these presheaves. It feels funny starting with simplicial sets as sets, then see them as presheaves, and then see them as sets again.

It is fine to take limits and Kan extend simplicial sets as presheaves but one must not forget what it corresponds to for simplicial sets that are built out of simplicies. This "dictionary" is one of the things i can't find.

And i still wonder how the composition of a category looks like in this presheaf language.

_Todd_: Don't worry, I didn't see you as opposing me. I agree with you that someone should have used the word "small" when talking about categories as simplicial sets. 

The truncated simplicial sets you're considering have been considered; the level at which you truncated (I'll say "2-skeletal" since you truncated so as to leave the parts in dimension up to 2) is certainly sufficient to encode the <i>data</i> of a category via the evident 2-skeletal nerve. [1-skeletal simplicial sets are reflexive directed graphs, and for those things the 1-skeletal nerve functor is just the forgetful functor from categories to reflexive directed graphs.] 

To answer your last question: composition in the category is modeled in the nerve by the "middle" face operator 
$$C_2 = C_1 \times_{C_0} C_1 \to C_1$$ 
which in functorial language (thinking of a simplicial set $C$ as a presheaf) is $C(f)$, where $f$ is the monomorphism in $\Delta$ from the 2-element ordinal to the 3-element ordinal that leaves out the middle element. The same fact holds true for the 2-skeletal nerve. 

Yes, it's certainly possible to view small categories as 2-skeletal simplicial sets, but the Segal conditions are not quite sufficient to characterize 2-skeletal nerves of categories. The missing condition not accounted for by the Segal conditions is associativity of composition. On the other hand, for _3-skeletal_ nerves, the Segal conditions would be enough. 

_Rafael:_ I finally expanded and implemented the suggestion above, which become a bit too long but i don't know where else to put it. Don't hesitate to add links to it.

In general, would it be ok to think of all the different objects equivalent to categories as presentations of categories instead of as categories, since they are equivalent to categories but not categories explicitly. Since no one objected i assume it is ok to think of the presheaves above as presentations of simplicial sets.

As for if CW-complexes (that are the geometric realization of a simplicial complex) generalize simplicial complexes, the best way would to write CW-complexes and simplicial complexes as tuples of data and show that a particular kind of CW-complex data is a simplicial complex. That would be very satisfactory. A simplicial complex is $X=(X_0,X_1,X_2,...)$, where $X_i$ is a finite set of i-simplicies. Subject to subset closure. A CW-complex is more complicated but something similar to Y$=({Y_0,Y_1,Y_2,...},O(Y))$, where $Y_i$ constitue a filtration of their full union $Y$ and $O(Y)$ is the set of open sets in this union $Y$. Subject to being Hausdorff topological space with a weak topology, and some conditions on cells. To start, is there a particular choice of $Y_i$'s that gives $X_i$'s, or is the topology that makes the difference?

This might help to enlight how a 1D CW-complex is a graph.

_Toby_:  I would regard even the usual definition of a category (as a set or class of objects etc) as requiring more detail than a category itself has, and thus also merely a 'presentation' (as you put it) of categories within the language of (material or structural) [[set theory]].  (The usual definition really defines a [[strict category]], which has a natural notion of [[isomorphism of categories|isomorphism]] stricter than the correct notion of [[equivalence of categories|equivalence]].  Within the category, we can see this as a notion of [[equality]] of objects stricter than the correct notion of [[isomorphism]].  Strict categories are [[evil]], but they appear to be the only way to define categories within set theory.)

_Rafael_: I was wondering when this would crop up. So what is a correct definition of a (non-strict) category? As a model of the sketch Scat?

_Toby_:  Within set theory, I don\'t know any other definition of category.  Within some kinds of [[type theory]], one may draw a distinction between a [[preset]] and a set and define a category to have a preset of objects.  [[FOLDS]] handles un-evil $\infty$-category theory natively, but I\'m not very familiar with it.  Or one can try to axiomatise category theory directly in first-order logic *without* equality.

Incidentally:
*  The usual term is 'large' rather than 'enlarged': large group, large field, large simplicial set, etc.  In context, one often drops 'large', or says 'possibly large' to be pedantic (when small is also allowed).
*  The objects of $\Delta$ is all finite; there is no way to allow them to be large.  It is the *values* of the presheaves that may be large, not the abstract simplices, but the set (class) of concrete simplices.
*  The possessive of 'category' is 'category\'s', not 'categorys'.

Did you paste over my edits something that you\'d been working on offline?

_Rafael_: I don't really understand your question, but no, i compared the texts and changed back what i thought was better before and did't paste the old edit over the new, as a comparison must show. To compare in nLab is also almost a pain, it colors changes wrong (or in a stupid way for a human).

* In textbooks i can't remember them using the large terminology. Probably because they did't treat large structures, at best infinite structures, and then meaning size of any infinite cardinality and not of the size of a proper class :)

*  What i was hinting about was that the $\Delta$ here (not the standard $\Delta$) contains simplicies with any cardinality of vertices.
I think it is otherwise impossible to build large categories.

* I like my formulation of the Segal condition better. I hope the implication arrow shows up, i am forced to edit in an incompatible IE.
The other condition should also have a name, such as (central) boundary operator associativity condition. Boundary operator is a more familiar name for face operator. Faces are as i see them 2D, while boundaries can have any dimension.
=--


[[!redirects abstract nonsense]]
[[!redirects general abstract nonsense]]
[[!redirects applied category theory]]