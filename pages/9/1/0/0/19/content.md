
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

\section{Idea}

_Category theory_ is a toolset for describing the general abstract structures in [[mathematics]]. 

+-- {: .un_remark}
###### Paradigm ####

As opposed to [[set theory]],  category theory focuses not on elements $x,y, \cdots$ -- called [[object]]s -- but on the **relations** between these objects: the ([[homomorphism|homo]])[[morphism]]s between them

$$
  x \stackrel{f}{\to} y
  \,.
$$

Later this will lead naturally on to an infinite sequence of steps:  first [[2-category theory]] which focuses on relation between relations, morphisms between morphisms: [[2-morphism]]s, then 3-category theory, etc. and to various variants, [[bicategories]], [[Gray categories]] .... Eventually this leads to [[higher category theory]], where one considers $k$-morphisms in all dimensions and to a wealth of interacting intuitions and concepts.

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
  \;\right)
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
  \;\;\;\right)
  \,.
$$

+-- {: .un_remark}
###### Examples ####

The archetypical example of a category is the category [[Set]] of [[set]]s and [[function]]s between sets. 

The classical examples of categories are [[concrete category|concrete categories]] whose [[object]]s are [[stuff, structure, property|sets with extra structure]] and whose [[morphism]]s are structure preserving functions of sets, such as [[Top]], [[Grp]], [[Vect]].  These are the examples from which the term _category_ derives: these categories literally _categorize_ mathematical structures by packing structures of the same _type_ (same category) and structure preserving mappings between them into a single whole structure, a category.

But it is far from the case that all categories are of this type. Categories are much more versatile than these classical examples suggest. After all, a [[category]] is just a [[quiver]] (a [[directed graph]]) with a notion of composition of its edges. As such it generalizes the concepts of [[monoid]] and [[poset]]. If the category is a [[groupoid]], it generalizes the concept of [[group]] (in a sense called [[horizontal categorification]]) and also the concept of [[equivalence relation]].  Thinking of a category as a generalized poset is particularly useful when studying [[limits]] and [[adjoint functors|adjunctions]].

Archetypical examples of non-[[concrete category|concrete]] categories are the [[fundamental groupoid]] of a [[topological space]] and the [[fundamental category]] of a [[directed space]]. 

=--


+-- {: .un_remark}
###### Terminology ####

Categories were named after the examples of [[concrete category|concrete categories]]. As [[Saunders Mac Lane]] writes

>Now the discovery of ideas as general as these is chiefly the willingness to make a brash or speculative abstraction, in this case supported by the pleasure of purloining words from the philosophers: "Category" from Aristotle and Kant, "Functor" from Carnap (Logische Syntax der Sprache), and "natural transformation" from then current informal parlance.

>([[Saunders Mac Lane]], *[[Categories for the Working Mathematician]]*, 29&#8211;30).

However, the [[category|categories]] of category theory are way more general than these [[concrete category|concrete categories]], and the way Aristotle and Kant use the [[category (philosophy)|term]] in philosophy is not particularly related to what Eilenberg & Mac Lane did with it.

=--

+-- {: .un_remark}
###### The basic trinity of concepts ####

Category theory reflects on itself. Categories are about collections of morphisms. And there are evident morphisms between categories: [[functor]]s. And there are evident morphisms between functors: [[natural transformation]]s.

This trinity of concepts

1. [[category]]

1. [[functor]]

1. [[natural transformation]]

is what category theory is built on. 

In [[higher category theory]] this continues with

* $k$-[[transfor]]s for all $k \in \mathbb{N}$.

=--


+-- {: .un_remark}
###### Conceptual unification ####

A major driving force behind the development of category theory is its ability to abstract and unify concepts. General statements about categories apply to each specific [[concrete category]] of mathematical structures. The general notion of [[universal constructions]] in categories, such as [[representable functors]], [[adjoint functors]]  and [[limits]], turns out to prevail throughout mathematics and manifest itself in myriads of special examples.

=--

+-- {: .un_remark}
###### Abstract nonsense ####

This abstraction power of category theory has led Norman Steenrod to coin the term _abstract nonsense_ or _general abstract nonsense_ for it. It is being used as in "This property is not specific to this context, it already follows from general abstract nonsense". Peter Freyd expressed a similar feeling by his witticism: 

> {#WhatIsTriviallyTrivial} "Perhaps the purpose of categorical algebra is to show that which is trivial is trivially trivial."

But abstract nonsense still tends to meet with some resistance. In the preface of [Mitchell (1965)](#Mitchell65) it says:

> A number of sophisticated people tend to disparage category theory as consistently as others disparage certain kinds of classical music. When obliged to speak of a category they do so in an apologetic tone, similar to the way some say, "It was a gift &#8211; I've never even played it" when a record of Chopin Nocturnes is discovered in their possession. For this reason I add to the usual prerequisite that the reader have a fair amount of mathematical sophistication, the further prerequisite that he have no other kind.

=--

+-- {: .un_remark}
###### The nPOV ####

The vast applicability and expressiveness of category theory leads to the observation that most structures in mathematics are best understood from a category theoretic or higher category theoretic viewpoint. This is the [[nPOV]].

=--

\section{The central constructions}

\subsection{Presheaves}

Much of the power of category theory rests in the fact that it reflects on itself. For instance that [[functors]] between two categories form themselves a category: the [[functor category]]. 

This leads to the notion of [[presheaf categories]] and [[sheaf toposes]]. Much of category theory is [[topos theory]].

Under [[Isbell duality]] this sets the stage for everything in mathematics related to [[space]] and [[algebra]] and their duality.

\subsection{Universal constructions}

Elementary as it is, the definition of a [[category]] supports a powerful set of constructions: [[universal constructions]]. These include

* [[limit]] and [[colimit]];

* [[adjunction]];

* [[Kan extension]]

* [[end]] and [[coend]].

All these are special cases of each other and thus reflect different aspect of one single phenomenon. Applying category theory means applying these constructions in specific situations and using general abstract theorems for deducing statements about concrete contexts.

\subsection{The central theorems}

Category theory has a handful of central lemmas and theorems. Their proof is typically easy, sometimes almost tautological. Their power rests in the fact that they apply over and over again all over mathematics. Many concrete constructions get simplified by observing that they are but special realizations of these general abstract results in category theory. Among these central theorems are

* first and foremost: the [[Yoneda lemma]];

* [[Isbell duality]];

* the [[Grothendieck construction]];

* the [[adjoint functor theorem]];

* the [[monadicity theorem]];

* [[Tannaka duality]].


\section{Applications}

For a detailed list of applications see

* [[applications of (higher) category theory]].

\subsection{In pure mathematics}

Apart from its general role in mathematics, category theory provides the high-level language for

* [[logic]] / [[type theory]]

* [[higher algebra]]

* [[higher geometry]] .

\subsection{Outside of mathematics}

Outside of pure mathematics, category theory finds major applications in

* fundamental [[physics]] -- see [[higher category theory and physics]]

* theoretical [[computer science]]

and is increasingly finding applications in such diverse areas as chemistry, network theory and natural language processing. Further information can be found on the [[applied category theory]] page.


\section{Contrast to theories of other objects}

\subsection{Category theory vs. set theory}

Here set theory is assumed to be a theory of the usual concept of sets, that is *material* [[set theory]].

No one of these is more fundamental than the other as a foundation of mathematics. Category theory is a holistic (structural) approach to mathematics that can (through such methods as Lawvere's [[ETCS]]) provide [[foundations]] of mathematics and (through [[algebraic set theory]]) reproduce all the different axiomatic set theories; elementary category theory does not need the concept of set to be formulated. Set theory is an analytic approach (element-wise) and can reproduce category theory by simply defining all the concepts in the usual way, as long as one include a technique to handle large categories (for instance by using [[class]]es instead of sets, or by including as an axiom that an uncountable [[inaccessible cardinal]] exists or even that [[Grothendieck universe]]s exist). 


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

\subsection{Category theory vs. order theory}

A category may be thought of as a [[categorification]] of a [[poset]] rather than of a [[set]]; much (but by no means all) of category theory also appears in [[order theory]].

See [[category theory vs order theory]] for more discussion.

\section{Theorems}
 {#Theorems}

* [[Yoneda lemma]]

* [[Isbell duality]]

* [[Grothendieck construction]]

* [[adjoint functor theorem]]

* [[monadicity theorem]]

* [[adjoint lifting theorem]]

* [[Tannaka duality]]

* [[Gabriel-Ulmer duality]]

* [[small object argument]]

* [[Freyd-Mitchell embedding theorem]]



\section{Related concepts}

* [[formal category theory]]

* [[enriched category theory]]

* [[internal category]] [[internalization|theory]]

[[!include table of category theories]]

* [[type theory]]

  * [[relation between category theory and type theory]]

* [[computer science]]

  * [[computational trinitarianism]]


\section{References}
 {#References}

For more see the references at *[[category]]*.

\subsection{History}
 {#History}

The concepts of _[[category]]_, _[[functor]]_ and _[[natural transformation]]_ were introduced in

* {#EilenbergMacLane45} [[Samuel Eilenberg]], [[Saunders MacLane]], *[[General Theory of Natural Equivalences]]*,  Transactions of the American Mathematical Society **58** 2 (1945) 231-294 &lbrack;[doi:10.1090/S0002-9947-1945-0013131-6](https://doi.org/10.1090/S0002-9947-1945-0013131-6), [jstor:1990284](http://www.jstor.org/stable/1990284)&rbrack;

apparently (see [there](Hans+Freudenthal#AsAForerunnerOfCategoryTheory)) taking inspiration from:

* {#Freudenthal37} [[Hans Freudenthal]], *Entwicklungen von Räumen und ihren Gruppen*, Comp. Math. **4** (1937) 145-234. &lbrack;[numdam](http://www.numdam.org/item/CM_1937__4__145_0/)&rbrack;  

The rational for introducing the concept of [[categories]] was to introduce the concept of [[functors]], and the reason for introducing functors was to introduce the concept of [[natural transformations]] (more specifically [[natural equivalences]]) in order to make precise the meaning of "natural" means in [[mathematics]] and specifically in [[algebraic topology]]:

> If [[topology]] were publicly defined as the study of families of sets closed under finite intersection and infinite unions a serious disservice would be perpetrated on embryonic students of topology. The mathematical correctness of such a definition reveals nothing about topology except that its basic axioms can be made quite simple. And with category theory we are confronted with the same pedagogical problem. The basic axioms, which we will shortly be forced to give, are much too simple.

> A better (albeit not perfect) description of topology is that it is the study of continuous maps; and category theory is likewise better described as the theory of functors. Both descriptions are logically inadmissible as initial definitions, but they more accurately reflect both the present and the historical motivations of the subjects. 

> {#CategoriesForNaturalTransformations} It is not too misleading, at least historically, to say that categories are what one must define in order to define natural transformations. 

> (from [Freyd 64, page 1](#Freyd64))

and

> {#CategoriesForNaturalTransformationsII} Category theory is an embodiment of Klein's dictum that it is the maps that count in mathematics. If the dictum is true, then it is the functors between categories that are important, not the categories. And such is the case. Indeed, the notion of category is best excused as that which is necessary in order to have the notion of functor. But the progression does not stop here. There are maps between functors, and they are called natural transformations. And it was in order to define these that Eilenberg and MacLane first defined functors. 

> (from [Freyd 65, beginning of Part Two](#Freyd65))


The paper [Eilenberg-Maclane 45](#EilenbergMacLane45) was a clash of ideas from abstract [[algebra]] (Mac Lane) and [[topology]]/[[homotopy theory]] (Eilenberg). It was first rejected on the ground that it had no content but was later published. Since then category theory has flourished into almost all areas of mathematics, has found many applications outside mathematics and even attempts to build a [[foundations]] of mathematics. 

This and much more history is recalled in

* {#MacLaneHistory} [[Saunders MacLane]], _Concepts and Categories in Perspective_, AMS ([pdf](http://www.ams.org/samplings/math-history/hmath1-maclane25.pdf))

* {#Krömer07} [[Ralf Krömer]]: *Tool and object: A history and philosophy of category theory*, Science Networks. Historical Studies **32** (2007) &lbrack;[doi:10.1007/978-3-7643-7524-9](https://doi.org/10.1007/978-3-7643-7524-9)&rbrack;

see specifically 

* [[Ralf Krömer]]: *Category theory in Algebraic Topology*, chapter 3 of: [Krömer 2007](#Krömer07) &lbrack;[doi:10.1007/978-3-7643-7524-9_2](https://doi.org/10.1007/978-3-7643-7524-9_2)&rbrack;

See also:

* [[Jean-Pierre Marquis]], *What is Category Theory?*, in G. Sica (ed.) *What is Category Theory?*, Polimetrica (2006) 221-256 &lbrack;[[Marquis-CategoryTheory.pdf:file]], [semanticscholar](https://www.semanticscholar.org/paper/What-is-category-theory-Sica/7737401202b220f89ae9c11cf9af65995a4dcf50)&rbrack;

* [[Jean-Pierre Marquis]], _From a Geometrical Point of View: A Study of the History and Philosophy of Category Theory_, Springer (2009) &lbrack;[doi:10.1007/978-1-4020-9384-5](https://doi.org/10.1007/978-1-4020-9384-5)&rbrack;

[[!include category theory -- references]]

[[!redirects abstract nonsense]]
[[!redirects general abstract nonsense]]
