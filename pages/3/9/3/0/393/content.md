
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

\tableofcontents

\section{Idea}

By a *homotopical category* authors tend to mean something like a [[relative category]]/[[category with weak equivalences]], possibly satisfying further axioms (notably [[two-out-of-six]], as in [Dwyer, Hirschhorn, Kan & Smith 2004](#DwyerHirschhornKanSmith04)), but in any case a [[1-category]] equipped with a [[class]] of morphisms to be called *[[weak equivalences]]* and satisfying some [[extra properties]]. 

The terminology is that of a [[concept with an attitude]]: One is interested in the [[localization]]/[[homotopy category]] with respect to the weak equivalences, or rather in the [[simplicial localization]], hence in the [[(infinity,1)-category|$(\infty,1)$-category]] and hence "the [[homotopy theory]]" presented by this data.

(An earlier proposal by [Grandis 1992](#Grandis92), [1994](#Grandis94) to say "homotopical categories" for 1-categories equipped instead with *[[extra structure]]* of [[homotopies]]/[[2-morphisms]] subject (only) to [[horizontal composition]] does not seem to have caught on.)

Accordingly, a [[functor]] between the underlying categories of homotopical categories which preserves the weak equivalences is called a *[[homotopical functor]]*.

\section{Definition}

Most authors seem to agree that a *homotopical category* is at least a [[strict category|strict]] [[1-category]] equipped with a sub-[[class]] of [[morphisms]] to be called the *[[weak equivalences]]*, closed under [[composition]] and containing all [[identity morphisms]], hence forming a [[wide subcategory]] (a [[relative category]]).

The authors [Dwyer, Hirschhorn, Kan & Smith (2004)](#DwyerHirschhornKanSmith04) require that the weak equivalences satisfy the *[[2-out-of-6-property]]* (this includes all [[model categories]], see [here](two-out-of-six+property#ModelCategoriesSatisfyTwoOutOfSix)) and give a detailed discussion. (Notice that --- with the assumption that all [[identity morphisms]] are among the weak equivalences --- [[2-out-of-6]] *[implies](two-out-of-six+property#2outof3)* the [[2-out-of-3 property]] required for [[categories with weak equivalences]].) 

This definition of "homotopical category" has found more followers, e.g. [Szumiło (2014)](#Szumiło14), [Hekking (2017)](#Hekking17).

But some authors &lbrack;[Bergner (2014)](#Bergner14), [Riehl (2019)](#Riehl19)&rbrack; use the term "homotopical category" more vaguely, apparently thinking at least of [[categories with weak equivalences]] but focusing on examples that do satisfy also the  [[two-out-of-six property]] (without mentioning this property).

On the other hand, [Arndt (2015)](#Arndt15) seems to use "homotopical categories" as a synonym for "[[relative categories]]" and [Szumiło (2019)](#Szumiło19) seems to use it as synonymous with "[[category with weak equivalences]]", see also [Bergner (2019)](#Bergner19).


\section{Related concepts}

* [[relative category]]

* [[category of fibrant objects]]

* [[cofibration category]]

* [[Waldhausen category]]

* [[model category]]

* [[calculus of fractions]]

* [[resolution]]

\section{References}

An early notion of "homotopical categories" as 1-categories equipped with [[homotopies]] subject to [[horizontal composition]] (hence [[extra structure]] mess than but in the direction of [[2-category]]-structure):

* {#Grandis92} [[Marco Grandis]], *On the categorical foundations of homological and homotopical algebra*, Cahiers de Topologie et Géométrie Différentielle Catégoriques **33** 2 (1992)  135-175 &lbrack;[numdam:CTGDC_1992__33_2_135_0](http://www.numdam.org/item/?id=CTGDC_1992__33_2_135_0)&rbrack;

* {#Grandis94} [[Marco Grandis]], *Homotopical algebra in homotopical categories*, Applied Categorical Structures **2** (1994) 351–406 &lbrack;[doi:10.1007/BF00873039](https://doi.org/10.1007/BF00873039)&rbrack;

The notion of "homotopical categories" as [[relative categories]] with the requirement that the weak equivalences satisfy the 2-out-of-6 property:

* {#DwyerHirschhornKanSmith04} [[William Dwyer]], [[Philip Hirschhorn]], [[Daniel Kan]], [[Jeff Smith]], p. 23 & pp. 96 of: *[[Homotopy Limit Functors on Model Categories and Homotopical Categories]]*, Mathematical Surveys and Monographs **113** AMS (2004) &lbrack;[ISBN: 978-1-4704-1340-8](https://bookstore.ams.org/surv-113-s), [pdf](http://dodo.pdmi.ras.ru/~topology/books/dhks.pdf)&rbrack;

Authors following this terminology:

* {#Szumiło14} [[Karol Szumiło]], *Two Models for the Homotopy Theory of Cocomplete Homotopy Theories*, Bonn (2014) &lbrack;[arXiv:1411.0303](https://arxiv.org/abs/1411.0303), [hdl:20.500.11811/6136](https://hdl.handle.net/20.500.11811/6136)&rbrack;

* {#Hekking17} [[Jeroen Hekking]], *Segal Objects in Homotopical Categories & K-theory of Proto-exact Categories*, Leiden (2017) &lbrack;[pdf](https://www.universiteitleiden.nl/binaries/content/assets/science/mi/scripties/master/hekking_master.pdf)&rbrack; 

* [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], *Homotopical inverse diagrams in categories with attributes*, Journal of Pure and Applied Algebra **225** 4 (2021) 106563 &lbrack;[doi:10.1016/j.jpaa.2020.106563](https://doi.org/10.1016/j.jpaa.2020.106563)&rbrack;

On the other hand, "homotopical categories" is used as synonymous with "[[category with weak equivalences]]" in:

* {#Szumiło19} [[Karol Szumiło]], [slide 10](https://hott.github.io/HoTT-2019/conf-slides/Szumilo.pdf#page=10) of: *Internal Languages of Higher Categories* (2019) &lbrack;[pdf](https://hott.github.io/HoTT-2019/conf-slides/Szumilo.pdf)&rbrack;

Usage of "homotopical categories" understood with more relaxed or unspecified axioms on the weak equivalences but focusing on examples which are homotopical in the [above](#DwyerHirschhornKanSmith04) sense: 

* {#Bergner14} [[Julie Bergner]], *An introduction to homotopical categories*, lecture at MSRI (2014) &lbrack;part 1:[YT](https://youtube.com/watch?v=OgbaZHpUeD0), 2:[YT](https://youtube.com/watch?v=SKZT7x_0i_Y)&rbrack;
 
* {#Riehl19} [[Emily Riehl]], *Homotopical categories: from model categories to (∞,1)-categories* &lbrack;[arXiv:1904.00886](https://arxiv.org/abs/1904.00886)&rbrack; in: [[Andrew J. Blumberg]], [[Teena Gerhardt]], [[Michael A. Hill]] (eds,) *[[Stable categories and structured ring spectra]]*,  MSRI Book Series, Cambridge University Press (2022) &lbrack;ISBN:9781009123297&rbrack;

Usage of "homotopical categories" as, apparently, synonymous with *[[relative categories]]*:

* {#Arndt15} [[Peter Arndt]], *Homotopical categories of logics*, in: *The Road to Universal Logic*, Studies in Universal Logic Birkhäuser (2015) &lbrack;[pdf](https://www.math.uni-duesseldorf.de/~arndt/research/HomotopicalCategoriesOfLogics.pdf), [doi:10.1007/978-3-319-10193-4_2](https://doi.org/10.1007/978-3-319-10193-4_2)&rbrack;

see also:

* {#Bergner19} [[Julie Bergner]], MAA review (2019) &lbrack;[web](https://www.maa.org/press/maa-reviews/higher-categories-and-homotopical-algebra)&rbrack; of: [[Denis-Charles Cisinski]]'s *[[Higher Categories and Homotopical Algebra]]*

  > "the two subjects &lbrack;[[homotopy theory]] and [[category theory]]&rbrack; have come together in a deep way in the development of what one might call higher homotopical categories. The idea is to consider something like a category, but whose morphisms from one object to another form a topological space, rather than simply a set, and for which composition might only be defined up to homotopy. Such a structure turns out to have several other interpretations: a certain kind of higher category for which various higher morphisms are invertible (often called an (∞,1)-category or simply ∞-category), or even as a category with weak equivalences in the sense of abstract homotopy theory."
 


[[!redirects homotopical categories]]
