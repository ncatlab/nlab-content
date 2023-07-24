
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

By a *homotopical category* authors tend to mean something like a [[relative category]] or a [[category with weak equivalences]] or something stronger, but in any case a [[1-category]] equipped with a [[class]] of morphisms to be called *[[weak equivalences]]* and satisfying some extra [[axioms]]. The terminology is that of a [[concept with an attitude]]: One is interested in the [[localization]]/[[homotopy category]] with respect to the weak equivalences, or rather in the [[simplicial localization]], hence in the [[(infinity,1)-category|$(\infty,1)$-category]] and hence "the [[homotopy theory]]" presented by this data.

Accordingly, a [[functor]] between the underlying categories of homotopical categories which preserves the weak equivalences is called a *[[homotopical functor]]*.

\section{Definition}

Most authors will agree that a *homotopical category* is at least a [[strict category|strict]] [[1-category]] equipped with a sub-[[class]] of [[morphisms]] to be called the *[[weak equivalences]]*, closed under [[composition]] and containing all [[identity morphisms]], hence forming a [[wide subcategory]].

The authors [Dwyer, Hirschhorn, Kan & Smith (2004)](#DwyerHirschhornKanSmith04) -- who seem to introduce the terminology "homotopical category" -- require that the weak equivalences satisfy the *[[2-out-of-6-property]]* (this includes all [[model categories]]).  Notice that (with the assumption that all [[identity morphisms]] are among the weak equivalences) this *implies* the [[2-out-of-3 property]].

Later authors (eg. [Arndt (2015)](#Arndt15), [Riehl (2019)](#Riehl19)) seem to use the term "homotopical category" nominally as in *[[relative category]]*, but the examples discussed are [[categories with weak equivalences]] and the [[two-out-of-six property]] (even when satisfied) is not mentioned.


\section{Simplicial localization}

Every homotopical category $C$ "presents" or "models" an [[(infinity,1)-category]] $L C$, a [[simplicially enriched category]] called the [[simplicial localization]] of $C$, which is in some sense the universal solution to inverting the weak equivalence up to [[higher category theory|higher categorical]] morphisms.

\section{Related concepts}

* [[relative category]]

* [[category of fibrant objects]]

* [[cofibration category]]

* [[Waldhausen category]]

* [[model category]]

* category with a [[calculus of fractions]]

* [[resolution]]

\section{References}

The notion with the requirement that the weak equivalences satisfy the 2-out-of-6 property:

* {#DwyerHirschhornKanSmith04} [[William Dwyer]], [[Philip Hirschhorn]], [[Daniel Kan]], [[Jeff Smith]], p. 23 & pp. 96 of: *[[Homotopy Limit Functors on Model Categories and Homotopical Categories]]*, Mathematical Surveys and Monographs **113** AMS (2004) &lbrack;[ISBN: 978-1-4704-1340-8](https://bookstore.ams.org/surv-113-s), [pdf](http://dodo.pdmi.ras.ru/~topology/books/dhks.pdf)&rbrack;

The notion with more relaxed/unspecified axioms on the weak equivalences:

* {#Arndt15} [[Peter Arndt]], *Homotopical categories of logics*, in: *The Road to Universal Logic*, Studies in Universal Logic Birkhäuser (2015) &lbrack;[pdf](https://www.math.uni-duesseldorf.de/~arndt/research/HomotopicalCategoriesOfLogics.pdf), [doi:10.1007/978-3-319-10193-4_2](https://doi.org/10.1007/978-3-319-10193-4_2)&rbrack;
 
* {#Riehl19} [[Emily Riehl]], *Homotopical categories: from model categories to (∞,1)-categories* &lbrack;[arXiv:1904.00886](https://arxiv.org/abs/1904.00886)&rbrack; in: [[Andrew J. Blumberg]], [[Teena Gerhardt]], [[Michael A. Hill]] (eds,) *[[Stable categories and structured ring spectra]]*,  MSRI Book Series, Cambridge University Press (2022) &lbrack;ISBN:9781009123297&rbrack;


[[!redirects homotopical categories]]
