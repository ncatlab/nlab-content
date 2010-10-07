
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Mathematics
+--{: .hide}
[[!include mathematicscontents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

* **category theory**

* [[2-category theory]]

* [[(∞,1)-category theory]]

* [[higher category theory]]


***


#Contents#
* tic
{:toc}


## Idea

_Category theory_ is a toolset for describing the general abstract structures in [[mathematics]]. 

+-- {: .un_remark}
###### Paradigm ####

As opposed to [[set theory]],  category theory focuses not on elements $x,y, \cdots$ -- called [[object]]s -- but on the **relations** between these objects: the ([[homomorphism|homo]])[[morphism]]s between them

$$
  x \stackrel{f}{\to} y
  \,.
$$

This is but the first in an infinite sequence of steps: [[2-category theory]] which focuses on relation between relations, morphisms between morphisms: [[2-morphisms]]. Eventually this leads to [[higher category theory]], where one considers [[k-morphism]]s _ad infinitum_ .

=--

The concept that formalizes this is that of a [[category]]: a collection of arrows/morphism that can be [[composition|composed]] if they are adjacent

$$
  \left(
    \array{
       x
       \\
       \downarrow^{\mathrlap{f}}
       \\
       y
       \\
       \downarrow^{\mathrlap{g}}
       \\
       z
    }
  \right)
  \;\;\;\;
  \mapsto
  \;\;\;\;
  \left(
    \array{
       x
       \\
       \downarrow^{\mathrlap{g \circ f}}
       \\
       z
    }
  \right)
  \,.
$$

+-- {: .un_remark}
###### Examples ####

The archetypical example of a category is the category [[Set]] of [[set]]s and [function]]s between sets. 

The classical examples of categories are [[concrete category|concrete categories]] whose [[object]]s are [[stuff, structure, property|sets with extra structure]] and whose [[morphism]]s are structure preserving functions of sets, such as [[Top]], [[Grp]], [[Vect]].  These are the examples from which the term _category_ derives: these categories literally _categorize_ mathematical structures by packing structures of the same _type_ (same category) and structure preserving mappings between them into a single whole structure, a category.

But by far not all categories are of this type and categories are much more versatile than these classical examples suggest. After all, a [[category]] is just a [[directed graph]] with a notion of composition of its edges. As such it generalizes the concepts of [[monoid]] and [[poset]]. If the category is a [[groupoid]] it generalizes the concept of [[group]] (in a sense called [[horizontal categorification]]).  Thinking of a category as a generalized poset is particularly useful when studying [[limits]] and [[adjoint functors|adjunctions]].

Archetypical examples of non-[[concrete category|concrete]] categories are the [[fundamental groupoid]] of a [[topological space]] and the [[fundamental category]] of a [[directed space]]. 

=--


+-- {: .un_remark}
###### Terminology ####

Categories were named after the examples of [[concrete category|concrete categories]]. As [[Saunders Mac Lane]] writes

>Now the discovery of ideas as general as these is chiefly the willingness to make a brash or speculative abstraction, in this case supported by the pleasure of purloining words from the philosophers: "Category" from Aristotle and Kant, "Functor" from Carnap (Logische Syntax der Sprache), and "natural transformation" from then current informal parlance.

>([[Saunders Mac Lane]], [[Categories Work|Categories for the Working Mathematician]], 29&#8211;30).

However, the [[category|categories]] of category theory are way more general than these [[concrete category|concrete categories]], and the way Aristotle and Kant use the term is not particularly related to what Eilenberg & Mac Lane did with it.

=--

+-- {: .un_remark}
###### The basic trinity of concepts ####

Category theory refledcts on itself. Categories are about collections of morphisms. And there are evident morphisms between categories: [[functor]]s. And there are evident morphisms between functors: [[natural transformation]]s.

This trinicty of concepts

1. [[category]]

1. [[functor]]

1. [[natural transformation]]

is what category theory is built on. 

In [[higher category theory]] this continues with

* $k$-[[transfor]]s for all $k \in \mathbb{N}$.

=--


+-- {: .un_remark}
###### Conceptual unification ####

A major driving force behind the development of category theory is its ability to abstract and unify concepts. General statements about categories apply to each specific [[concrete category]] of mathematical structures. The general notion of [[universal construction]]s in categories, such as [[representable functor]]s, [[adjoint functor]]s  and [[limit]]s, turns out to prevail throughout mathematics and manifest itself in myriads of special examples.

=--

+-- {: .un_remark}
###### Abstract nonsense ####

This abstraction power of category theory has led Norman Steenrod to coin the term _abstract nonsense_ or _general abstract nonsense_ for it. It is being used as in "This property is not specific to this context, it already follows from general abstract nonsense". Peter Freyd expressed a similar feeling by his witticism: 

>"Perhaps the purpose of categorical algebra is to show that which is trivial is trivially trivial."

But abstract nonsense still tends to meet with some resistance. In the preface of his 1965 book _Theory of Categories_ Barry Mitchell writes:

>A number of sophisticated people tend to disparage category theory as consistently as others disparage certain kinds of classical music. When obliged to speak of a category they do so in an apologetic tone, similar to the way some say, "It was a gift &#8211; I've never even played it" when a record of Chopin Nocturnes is discovered in their possession. For this reason I add to the usual prerequisite that the reader have a fair amount of mathematical sophistication, the further prerequisite that he have no other kind.

=--

+-- {: .un_remark}
###### The $n$-POV ####

The vast applicability and expressiveness of category theory leads to the observation that most structures in mathematics are best understood from a category theoretic or higher cstegory theoretic viewpoint. This is the [[nPOV]].

=--

## The central constructions

### Presheaves

Much of the power of category theory rests in the fact that it reflects on itself. For instance that [[functor]]s between two categories form themselves a category: the [[functor category]]. 

This leads to the notion of [[presheaf categories]] and [[sheaf toposes]]. Much of category theory is [[topos theory]].

Under [[Isbell duality]] this sets the stage for everything in mathematics related to [[space]] and [[algebra]] and their duality.

### Universal constructions

Elementary as it is, the definition of a [[category]] supports a powerful set of constructions: [[universal construction]]s. These include

* [[limit]]s and [[colimit]];

* [[adjunction]];

* [[Kan extension]]

* [[end]]s and [[coend]]s.

All these are special cases of each other and thus reflect different aspect of one single phenomenon. Applying category theory means applying these constructions in specific situations and using general abstract theorems for deducing statements about concrete contexts.

## The central theorems

Category theory has a handful of central lemmas and theorems. Their proof is typically easy, sometimes almost tautological. Their power rests in the fact that they apply over and over again all over mathematics. Many concrete constructions get simplified by observing that they are but special realizations of these general abstract results in category theory. These central theorems are

* first and foremost: the [[Yoneda lemma]];

* [[Isbell duality]];

* the [[Grothendieck construction]];

* the [[adjoint functor theorem]];

* the [[monadicity theorem]];

* [[Tannaka duality]].


## History

Category theory was introduced by [[Samuel Eilenberg]] and [[Saunders Mac Lane]] in the 1945 paper **General theory of natural equivalences**. The reason for introducing [[category|categories]] was to introduce [[functor]]s, and the reason for introducing functors was to introduce [[natural transformation]]s (more specifically natural equivalences) in order to define what _natural_ means in mathematics. 

The paper was a clash of ideas from abstract [[algebra]] (Mac Lane) and [[topology]]/[[homotopy theory]] (Eilenberg). It was first rejected on the ground that it had no content but was later published. Unexpectedly category theory has flourished into almost all areas of mathematics, has found many applications outside mathematics and even attempts to build a [[foundations]] of mathematics. 



## Branches of category theory

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
* [[applied category theory|Applied category theory]]. Especially to mathematical [[physics]], [[computer science]] and [[dynamical system]]s (categorical dynamics).

Most of these include some [[higher category theory]].

An imperfect perspective of category theory (for the purpose of classifying articles) can be obtained from the [MSC subject classification (18-XX)](http://www.ams.org/mathscinet/msc/msc.html?t=18-XX); the current one is from 2000 and reflects ideas of the decade before that.







## Contrast to theories of other objects

### Category theory vs. set theory

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

For a philosophical consideration of foundations covering and comparing sets, structuralism (a la Bourbaki?) and categories, see the article

* Sets, categories and structuralism - Costas Drossos

### Category theory vs. order theory

A category may be thought of as a [[categorification]] of a [[poset]] rather than of a [[set]]; much (but by no means all) of category theory also appears in [[order theory]].

See [[category theory vs order theory]] for more discussion.


## Generalizations and other structures

### Generalizations of categories

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


### Other structures

These are a part of category theory even if they are not categories or reduce to categories as a special case.

* [[operad|Operads]]
* [[derivation scheme|Derivation schemes]] (for deriving categories)
* [[computad|Computads]] (a special case of a derivation scheme when the underlying category is a free 2-category)
* [[pseudocategory|Pseudocategories]] (nonstrict internal categories)
* [[sesquicategory|Sesquicategories]]
* [[monad|Monads]]
* [[sketch|Sketches]] (models of sketches give categories or more generally internal categories)
* [[doctrine|Doctrines]]


## Applied category theory

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


## References

### Textbooks

Standard category theory textbooks for which the $n$Lab currently provides detailed linked indexes are

* Kashiwara and Schapira, _[[Categories and Sheaves]]_ .

* [[Ieke Moerdijk]], [[Saunders Mac Lane]], _[[Sheaves in Geometry and Logic]]_

Other standard references include:

* [[Saunders Mac Lane]], _[[Categories Work|Categories for the working mathematician]]_, 2nd ed. 

* [[Steve Awodey]], _Categories for everybody_. 

* [[Francis Borceux]], _Handbook of categorical algebra_, vol 1--3. 

* [[Colin McLarty]], _Elementary categories, elementary toposes_. 

* [[Jiri Adamek]], [[Horst Herrlich]], and [[George Strecker]], _Abstract and concrete categories: the joy of cats_. [free online](http://katmat.math.uni-bremen.de/acc/acc.pdf)

#### Topos theory

The standard monomgraph on [[topos theory]] is

* [[Peter Johnstone]], _[[Elephant|Topos theory]]_ .

Other texts include

* [[Michael Barr]] and [[Charles Wells]], _Toposes, triples and theories_. [free online](http://www.cwru.edu/artsci/math/wells/pub/ttt.html)

(Here "triple" mean [[monad]]).

* [[Robert Goldblatt]], _Topoi, the categorial analysis of logic_.
[free online](http://historical.library.cornell.edu/cgi-bin/cul.math/docviewer?did=Gold010&seq=&view=50&frames=0&pagenum=1)


#### Higher category theory

* [[Tom Leinster]], _Higher operads, higher categories_, [math.CT/0305049](http://arxiv.org/abs/math.CT/0305049) (see also Tom's online [notes](http://www.maths.gla.ac.uk/~tl/msci) on basic category theory)

* [[Eugenia Cheng]], [[Aaron Lauda]], _Higher-dimensional categories: an illustrated guide book_ [free online] (http://cheng.staff.shef.ac.uk/guidebook/guidebook-new.pdf)

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ ([pdf](http://www.math.harvard.edu/~lurie/papers/highertopoi.pdf))

* Project description: higher categorical structures and their applications ([pdf] (http://www.math.uchicago.edu/~may/NCATS/ForWeb.pdf))

### Course notes

* [[Jaap van Oosten]], _Basic category theory_ ([pdf](http://www.staff.science.uu.nl/~ooste110/syllabi/catsmoeder.pdf))

### Teaching category theory

* [[Andrew Stacey]], _Teaching category theory_ ([web](http://www.math.ntnu.no/~stacey/CountingOnMyFingers/TeachingCategories.html))


[[!redirects abstract nonsense]]
[[!redirects general abstract nonsense]]
[[!redirects applied category theory]]