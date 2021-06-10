
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

A _homotopical category_ is a structure used in [[homotopy theory]], related to but more flexible than a [[model category]].

\section{Definition}

A _homotopical category_ is a category with a distinguished class of
morphisms (called 'weak equivalences') satisfying the following
conditions:

* Every identity map is a weak equivalence.

* It has the **[[2-out-of-6-property]]**: 
if morphisms $h \circ g$ and $g \circ f$ are weak equivalences, then so are $f$, $g$, $h$ and $h \circ g \circ f$.

\section{Remarks}

* If the first condition in Def. 2 holds, then the 2-out-of-6-property implies the [[2-out-of-3]] property, hence every homotopical category is a [[category with weak equivalences]].

* Every [[model category]] yields a homotopical category.

* A functor $F : C \to D$ between homotopical categories which preserves weak equivalences is a [[homotopical functor]].

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

This definition is in page 23 of

* [[William Dwyer]], [[Philip Hirschhorn]], [[Daniel Kan]] and [[Jeff Smith]], _[[Homotopy Limit Functors on Model Categories
and Homotopical Categories]]_, volume 113 of Mathematical Surveys and Monographs.  ([pdf](http://dodo.pdmi.ras.ru/~topology/books/dhks.pdf))

with the main development of the concept starting in subsection 33 on page 96.

Survey with an eye towards [[(∞,1)-categories]]:
 
* [[Emily Riehl]], _Homotopical categories: from model categories to (∞,1)-categories_, in: [[Andrew J. Blumberg]], [[Teena Gerhardt]], [[Michael A. Hill]] (eds,) *Stable categories and structured ring spectra*,  MSRI Book Series, Cambridge University Press ([arXiv:1904.00886](https://arxiv.org/abs/1904.00886))


[[!redirects homotopical categories]]
