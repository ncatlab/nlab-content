
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

The rational for introducing the concept of [[categories]] was to introduce the concept of [[functors]], and the reason for introducing functors was to introduce the concept of [[natural transformations]] (more specifically [[natural equivalences]]) in order to make precise the meaning of "natural" means in mathematics:

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

* [[Ralf Krömer]], *Tool and object: A history and philosophy of category theory*, Science Networks. Historical Studies **32** (2007) &lbrack;[doi:10.1007/978-3-7643-7524-9](https://doi.org/10.1007/978-3-7643-7524-9)&rbrack;

See also:

* [[Jean-Pierre Marquis]], *What is Category Theory?*, in G. Sica (ed.) *What is Category Theory?*, Polimetrica (2006) 221-256 &lbrack;[[Marquis-CategoryTheory.pdf:file]], [semanticscholar](https://www.semanticscholar.org/paper/What-is-category-theory-Sica/7737401202b220f89ae9c11cf9af65995a4dcf50)&rbrack;

* [[Jean-Pierre Marquis]], _From a Geometrical Point of View: A Study of the History and Philosophy of Category Theory_, Springer (2009) &lbrack;[doi:10.1007/978-1-4020-9384-5](https://doi.org/10.1007/978-1-4020-9384-5)&rbrack;



\subsection{Textbooks}
 {#TextBooks}


\subsubsection{Basic category theory}
 {#BasicTextBooks}

* {#Freyd64} [[Peter Freyd]], _Abelian Categories -- An Introduction to the theory of functors_, Harper and Row (1964), Reprints in Theory and Applications of Categories, **3** (2003)  &lbrack;[tac:tr3](http://www.emis.de/journals/TAC/reprints/articles/3/tr3abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/3/tr3.pdf)&rbrack;

* {#Freyd65} [[Peter Freyd]], _The theories of functors and models_, in: Proceedings of _Symposium on the Theory of Models_, North Holland (1965) &lbrack;[doi:10.1016/C2013-0-11897-1](https://doi.org/10.1016/C2013-0-11897-1)&rbrack;

* {#Mitchell65} [[Barry Mitchell]], *Theory of categories*, Pure and Applied Mathematics **17**, Academic Press (1965) &lbrack;[ISBN:978-0-12-499250-4](https://www.elsevier.com/books/theory-of-categories/mitchell/978-0-12-499250-4)&rbrack;


* [[Saunders MacLane]] (notes by [[Ellis Cooper]]), *[[Lectures on category theory]]*, Bowdoin Summer School (1969)  

* {#Hilton69} [[Peter Hilton]] (ed.) _Category Theory, Homology Theory and Their Applications_, 

  vol 1: Lecture Notes in Mathematics **86**, Springer (1969) &lbrack;[doi:10.1007/BFb0079380](https://doi.org/10.1007/BFb0079380)&rbrack;

  vol 2: Lecture Notes in Mathematics **92**, Springer (1969) &lbrack;[doi:10.1007/BFb0080761](https://doi.org/10.1007/BFb0080761)&rbrack;

  vol 3: Lecture Notes in Mathematics **99**, Springer (1969) &lbrack;[doi:10.1007/BFb0081959](https://doi.org/10.1007/BFb0081959)&rbrack;

* {#Pareigis70} [[Bodo Pareigis]], *Categories and Functors*, Pure and Applied Mathematics **39**, Academic Press (1970) &lbrack;[doi:10.5282/ubm/epub.7244](https://doi.org/10.5282/ubm/epub.7244), [pdf](https://epub.ub.uni-muenchen.de/7244/1/7244.pdf)&rbrack;

* {#MacLane97} [[Saunders MacLane]], _[[Categories for the Working Mathematician]]_, Graduate texts in mathematics **5**, Springer (1971, second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;




* {#Gray74} [[John Gray]], *[[Adjointness for 2-Categories|Formal category theory: adjointness for $2$-categories]]*, Lecture Notes in Mathematics, **391**, Springer 1974 ([doi:10.1007/BFb0061280](https://doi.org/10.1007/BFb0061280))

   ([[formal category theory]] in the [[2-category]] [[Cat]])

* [[Horst Schubert]], *Categories*, Springer (1972) &lbrack;[doi:10.1007/978-3-642-65364-3](https://doi.org/10.1007/978-3-642-65364-3)&rbrack;

* {#Geroch85} [[Robert Geroch]], *Mathematical Physics*, University of Chicago Press (1985) &lbrack;[ISBN:9780226223063](https://press.uchicago.edu/ucp/books/book/chicago/M/bo4158035.html)&rbrack;

  > (introduces categories by examples arising in [[mathematical physics]])

* [[Jiri Adamek]], [[Horst Herrlich]], [[George Strecker]], *[[Abstract and Concrete Categories]]*, John Wiley and Sons, New York (1990) reprinted as: Reprints in Theory and Applications of Categories **17** (2006) 1-507 &lbrack;[tac:tr17](http://www.tac.mta.ca/tac/reprints/articles/17/tr17abs.html), [book webpage](http://katmat.math.uni-bremen.de/acc/)&rbrack;


* [[Peter Freyd]], [[Andre Scedrov]], *[[Categories, Allegories]]*, Mathematical Library Vol 39, North-Holland (1990) ([ISBN 978-0-444-70368-2](https://www.elsevier.com/books/categories-allegories/freyd/978-0-444-70368-2))


* [[Benjamin Pierce]], _Basic category theory for computer scientists_, 1991 20 ([publisher](https://mitpress.mit.edu/books/basic-category-theory-computer-scientists))

* [[Francis Borceux]], _[[Handbook of Categorical Algebra]]_, Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994)

* [[Roy L. Crole]], *Categories for types*, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9781139172707](https://doi.org/10.1017/CBO9781139172707)&rbrack;

  > ([[categorical semantics]] of [[type theory]])

* {#BarrWells95} [[Michael Barr]], [[Charles Wells]], *Category theory for computing science*, Prentice-Hall International Series in Computer Science (1995); reprinted in: Reprints in Theory and Applications of Categories **22** (2012) 1-538 &lbrack;[pdf](http://www.math.mcgill.ca/barr/papers/ctcs.pdf), [tac:tr22](http://www.tac.mta.ca/tac/reprints/articles/22/tr22abs.html)&rbrack;

  > (aimed at [[computer science]], see *[[computational trilogy]]*)

* {#Awodey06} [[Steve Awodey]], *Category theory*, Oxford University Press (2006, 2010) &lbrack;[doi:10.1093/acprof:oso/9780198568612.001.0001](https://doi.org/10.1093/acprof:oso/9780198568612.001.0001), [ISBN:9780199237180](https://global.oup.com/ukhe/product/category-theory-9780199237180), [pdf](http://englishonlineclub.com/pdf/Category%20Teory%20%5BEnglishOnlineClub.com%5D.pdf)&rbrack;

* [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_, 2006


* {#LawvereSchanuel09} [[F. William Lawvere]] and [[Stephen Schanuel]], _Conceptual Mathematics: A first introduction to categories_, $2^{nd}$ Edition, Cambridge University Press 2009 ([pdf](https://img.4plebs.org/boards/tg/image/1460/05/1460059215690.pdf))
 




* [[David Spivak]], _Category theory for scientists_ ([arXiv:1302.6946](http://arxiv.org/abs/1302.6946))

* [[Tom Leinster]], _[Basic Category Theory](http://www.maths.ed.ac.uk/~tl/bct/)_, 2014

* {#RiehlCTInContext} [[Emily Riehl]], _[[Category Theory in Context]]_, Dover Publications (2017) &lbrack;[pdf](http://www.math.jhu.edu/~eriehl/context.pdf)&rbrack;

* [[Martin Brandenburg]], *Einführung in die Kategorientheorie*, Springer 2017 

  ([doi:10.1007/978-3-662-53521-9](https://link.springer.com/book/10.1007/978-3-662-53521-9))

* {#FongSpivak18} [[Brendan Fong]], [[David Spivak]], _An invitation to applied category theory_, 2018 ([web](http://math.mit.edu/~dspivak/teaching/sp18/), [pdf](http://math.mit.edu/~dspivak/teaching/sp18/7Sketches.pdf))

* {#HeunenVicary19} [[Chris Heunen]], [[Jamie Vicary]], *Categories for Quantum Theory*, Oxford University Press 2019 ([ISBN:9780198739616](https://global.oup.com/academic/product/categories-for-quantum-theory-9780198739616))

  > (emphasis on [[monoidal category]]-theory with an eye towards [[finite quantum mechanics in terms of dagger-compact categories]] and [[quantum computation]])

* [[Marco Grandis]], _Category Theory and Applications: A Textbook for Beginners_, World Scientific, 2021 ([doi:10.1142/12253](https://doi.org/10.1142/12253))

On category theory in [[computer science]]/[[programming languages]] (such as for [[monads in computer science]]):

* [[Bartosz Milewski]] (compiled by Igal Tabachnik), *Category Theory for Programmers*, Blurb (2019) &lbrack;[pdf](https://github.com/hmemcpy/milewski-ctfp-pdf/releases/download/v1.3.0/category-theory-for-programmers.pdf), [github](https://github.com/hmemcpy/milewski-ctfp-pdf), [webpage](https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/), [ISBN:9780464243878](https://www.blurb.com/b/9621951-category-theory-for-programmers-new-edition-hardco)&rbrack;



\subsubsection{Topos theory}
 {#ReferencesToposTheory}

Monographs with focus on [[topos theory]]:

* [[Peter Johnstone]], _Topos theory_, 1977.

* [[Michael Barr]], [[Charles Wells]], _[[Toposes, Triples, and Theories]]_, Grundlehren der math. Wissenschaften 278 Springer 1983 ([TAC reprints](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html))
  > (Here "triple" means" [[monad]]").

* [[Robert Goldblatt]], _Topoi, the categorial analysis of logic_, 1984 ([gbnooks](https://books.google.us/books/about/Topoi.html?id=AwLc-12-7LMC))

* [[Colin McLarty]], *[[Elementary Categories, Elementary Toposes]]*, Oxford University Press 1992 ([ISBN:9780198514732](https://global.oup.com/academic/product/elementary-categories-elementary-toposes-9780198514732?cc=ae&lang=en&))

* [[Ieke Moerdijk]], [[Saunders Mac Lane]], _[[Sheaves in Geometry and Logic]]_ Springer 1992


* [[Peter Johnstone]], _[[Elephant|Sketches of an Elephant]]_, vol 1-2, Oxford University Press 2002







\subsubsection{Higher category theory}

* [[Carlos Simpson]], _[[Homotopy Theory of Higher Categories]]_ ([pdf](http://hal.archives-ouvertes.fr/docs/00/44/98/26/PDF/main.pdf))

* Project description: higher categorical structures and their applications ([pdf] (http://www.math.uchicago.edu/~may/NCATS/ForWeb.pdf))

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ ([pdf](http://www.math.harvard.edu/~lurie/papers/highertopoi.pdf))

* [[Tom Leinster]], _Higher operads, higher categories_, [math.CT/0305049](http://arxiv.org/abs/math.CT/0305049) 

* [[Eugenia Cheng]], [[Aaron Lauda]], _Higher-dimensional categories: an illustrated guide book_ [free online] (http://cheng.staff.shef.ac.uk/guidebook/guidebook-new.pdf)

Towards [[homotopy theory]]:

* [[Birgit Richter]], _From categories to homotopy theory_, Cambridge Studies in Advanced Mathematics 188, Cambridge University Press 2020 ([doi:10.1017/9781108855891](https://doi.org/10.1017/9781108855891), [book webpage](https://www.math.uni-hamburg.de/home/richter/catbook.html), [pdf](https://www.math.uni-hamburg.de/home/richter/bookdraft.pdf))

\subsection{Foundations}

The [[foundation]] of category theory in [[homotopy type theory]] (see at _[[internal category in homotopy type theory]]_) is discussed in 

* [[Benedikt Ahrens]], [[Chris Kapulkin]], [[Michael Shulman]], _Univalent categories and the Rezk completion_ ([arXiv:1303.0584](http://arxiv.org/abs/1303.0584))



\subsection{Course notes}
 {#CourseNotes}


* [[Jaap van Oosten]], _Basic category theory_ (2002) &lbrack;[pdf](http://www.staff.science.uu.nl/~ooste110/syllabi/catsmoeder.pdf)&rbrack;

* [[Thomas Streicher]], *Introduction to Category Theory and Categorical Logic* (2003) &lbrack;[pdf](https://www2.mathematik.tu-darmstadt.de/~streicher/CTCL.pdf), [[Streicher-CategoryTheory.pdf:file]]&rbrack;

* [[Bodo Pareigis]], _Category theory_ (2004) &lbrack;[dvi](http://www.mathematik.uni-muenchen.de/~pareigis/Vorlesungen/04SS/Cats1.dvi), [ps](http://www.mathematik.uni-muenchen.de/~pareigis/Vorlesungen/04SS/Cats1.ps), [pdf](http://www.mathematik.uni-muenchen.de/~pareigis/Vorlesungen/04SS/Cats1.pdf)&rbrack;

* [[Tom Leinster]], _Notes on basic category theory_ (2007) &lbrack;[web](http://www.maths.ed.ac.uk/~tl/msci)&rbrack;

* [[David Spivak]], _Category theory for scientists_ &lbrack;[arXiv:1302.6946](http://arxiv.org/abs/1302.6946)&rbrack;


* [[Peter Johnstone]], _Category Theory_ , Lecture notes taken by David Mehrle, University of Cambridge (2015) &lbrack;[pdf](http://pi.math.cornell.edu/~dmehrle/notes/partiii/cattheory_partiii_notes.pdf)&rbrack;

* [[Paolo Perrone]], _Notes on Category Theory with examples from basic mathematics_ (2019) &lbrack;[arXiv:1912.10642](http://arxiv.org/abs/1912.10642)&rbrack


* [[André Joyal]], *[[joyalscatlab:Categories]]*

* [[Benedikt Ahrens]] and Kobe Wullaert, _Category Theory for Programming_ (2022)  &lbrack;[arXiv:2209.01259](https://arxiv.org/abs/2209.01259)&rbrack;

\subsection{Videos} 

* The Catsters, Videos on various topics in category theory. ([YouTube link](https://www.youtube.com/user/TheCatsters))

Videos at an introductory level that cover basic concepts and constructions of category theory. The Catsters are [[Eugenia Cheng]] and [[Simon Willerton]] (anyone else?). 

* {#LaGatta} [[Tom LaGatta]], _Category theory_ ([video](http://www.youtube.com/watch?v=o6L6XeNdd_k)) 

Enthusiastic, mostly nontechnical talk given by a probability theorist, made for an audience innocent of any exposure to category theory. 

\subsection{Relation to philosophy}
 {#ReferencesRelationToPhilosophy}

Discussion of the relation to and motivation from the [[philosophy of mathematics]] includes 

*  [[Colin McLarty]], _The Last Mathematician from Hilbert's G&#246;ttingen: Saunders Mac Lane as Philosopher of Mathematics_,Brit. J. Phil. Sci. 2007 ([pdf](http://www.cwru.edu/artsci/phil/BJPSMacLane.pdf))

\subsection{Further resources and links}

There are several networks of category theorists organised, initially, at a national level and aiming to join forces to organise conferences, online seminars, etc.:

* _[[networks of category theorists]]_.


[[!redirects abstract nonsense]]
[[!redirects general abstract nonsense]]
