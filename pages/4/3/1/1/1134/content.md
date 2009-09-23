
<div class="rightHandSide toc">
[[!include supergeometry - contents]]
</div>



#Contents#

* automatic table of contents goes here
{:toc}

#Definition#

A **supermanifold** $X$ of dimension $p|q$ is a
[[ringed space]] $(|X|, O_X)$ where

* the [[topological space]] $|X|$ is [[second countable space]], [[Hausdorff space]]

* $O_X$ is a [[sheaf]] of commutative [[super algebra]]s that is locally on small enough open subsets $U \subset |X|$ isomorphic to one of the form $C^\infty(U) \otimes \wedge^\bullet \mathbb{R}^q$

Forgetting the graded part by projecting out the nilpotent ideal in $O_X$ yields the underlying ordinary smooth [[manifold]] $X_{red}$.

One just writes $C^\infty(X)$ for the [[super algebra]] $O_X(X)$ of global sections.


With the obvious morphisms of [[ringed space]] this forms the [[category]] [[SDiff]] of supermanifolds.

#Examples#

**example** For $E \to X$ a smooth finite-rank [[vector bundle]] the [[manifold]] $X$ equipped with the [[Grassmann algebra]] over $C^\infty(X)$ of the sections  of the dual bundle

$$
  O_X(U) := \Gamma (\wedge^\bullet(E^*))
$$

is a supermanifold. This is usually denoted by $\Pi E$

**exmaple** In particular, let $\mathbb{R}^{p+q} \to \mathbb{R}^p$ be the trivial rank $q$ [[vector bundle]] on $\mathbb{R}^p$ then one writes

$$
  \mathbb{R}^{p|q} := \Pi (\mathbb{R}^{p+q} \to \mathbb{R}^p)
$$

for the corresponding supermanifold.

**example** a [[super vector bundle]] on a supermanifold $X$ is a locally free [[sheaf]] of $O_X$-[[module]]s.

#Properties#

**Lemma** Every supermanifold is [[isomorphism|isomorphic]] to one of the form $\Pi E$ where $E$ is an ordinary smooth [[vector bundle]] and $\Pi E$ denotes the shifted .

**Warning** Still, the category of supermanifolds is far from being [[equivalence|equivalent]] to that of [[vector bundle]]s because a morphism of vector bundles translates to a morphism of supermanifolds that is strictly homogeneous in degrees, while a general morphism of supermanifolds need not be of this form.

But we have the following useful characterization of morphisms of supermanifolds_

**theorem**

* there is a natural bijection

  $$
    SDiff(X,Y) \simeq SAlgebras(C^\infty(Y), C^\infty(Y))
  $$

  so the contravariant embedding of supermanifolds into superalgebra is a [[full and faithful functor]]

* composition with the standard coordinate functions on $\mathbb{R}^{p|q}$ yields an [[isomorphism]]

  $$
    SDiff(X, \mathbb{R}^{p|q})
    \simeq
    (C^\infty(X)^{ev} \times \cdots p times \cdots 
    \times C^\infty(X)^{ev})
    \times
    (C^\infty(X)^{odd} \times \cdots q times \cdots 
    \times C^\infty(X)^{odd})
  $$

**Proof**

The first statement i a direct extension of the classical fact that the contravariant embedding of ordinary smooth [[manifold]]s into algebras $X \mapsto C^\infty(X)$ is a [[full and faithful functor]].



#Related entries#

* [[NQ-supermanifold]]

* [[integration over supermanifolds]]

* [[ringed site]]

* [[superconnection]]

* [[superdifferential form]]

#Some references#

* F. A. Berezin, D. A. Le&#301;tes, _Supermanifolds_, (Russian) Dokl. Akad. Nauk SSSR __224__ (1975), no. 3, 505--508; English transl.: Soviet Math. Dokl. __16__ (1975), no. 5, 1218--1222 (1976).

* I. L. Buchbinder, S. M. Kuzenko, _Ideas and methods of supersymmetry and supergravity; or A walk through superspace_

* Bryce de Witt, _Supermanifolds_, Cambridge Monographs on Mathematical Physics, 1984, 1992

* Yu. I. Manin, _Topics in noncommutative geometry_, Princeton Univ. Press 1991. 

* P. Deligne, P. Etingof, D.S. Freed, L. Jeffrey, D. Kazhdan, J. Morgan, D.R. Morrison and E. Witten, eds.  _Quantum fields and strings, A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

* V. S. Varadarajan, _Supersymmetry for mathematicians: an introduction_, AMS and Courant Institute, 2004.

There are many books in [[physics]] on [[supersymmetry]] (most well known is by Wess and Barger from 1992), but they emphasise more on the [[supersymmetry algebra]]s rather than on (the superspace and) _supermanifolds_. They should therefore rather be listed under entry [[supersymmetry]]. One should also note that there are two different definitions of a supermanifold which are not equivalent (some examples intersect but not all); they are sometimes  connected and even named according to the main proponents of the two approaches: Leites (via [[sheaf|sheaves]]) and de Witt (via [[supernumber]]s). 