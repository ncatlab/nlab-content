
#Contents#
* table of contents
{:toc}


## Idea

_Semi-topological K-theory_ $K_*^{st}$ is a [[homology theory|homological invariant]] of complex [[noncommutative spaces]] that interpolates between [[algebraic K-theory]] and [[topological K-theory]]. It is defined by starting with the presheaf defined by [[nonconnective algebraic K-theory]], taking the associated [[etale topology|etale]] [[infinity-sheaf|sheaf]], making it $\mathbf{A}^1$-[[homotopy invariant]], and finally taking the topological realization of the resulting presheaf. One recovers [[topological K-theory]] from this by inverting the [[Bott element]].

Semi-topological K-theory of [[complex varieties]] is related to [[morphic cohomology]] in the same way that [[algebraic K-theory]] is related to [[motivic cohomology]] and [[topological K-theory]] is related to [[singular cohomology]]. In fact there is an analogue of the [[Atiyah-Hirzebruch spectral sequence]].

Some [examples](#Examples) suggest that semi-topological K-theory may be a better suited invariant for complex varieties than either algebraic or topological K-theory.

## Definition

+-- {: .num_defn}
###### Definition
**(topological realization of presheaves)**.
Taking underlying [[topological spaces]] of complex points induces a functor of [[infinity-categories]]
  $$ |-| : Aff_C \longrightarrow Spc $$
from complex [[affine schemes]] to [[homotopy types]]. By [[left Kan extension]] it extends to a [[colimit]]-preserving functor
  $$ |-| : P(Aff_\mathbf{C}) \longrightarrow Spc $$
on the [[infinity-category of infinity-presheaves]].
This further extends to a [[colimit]]-preserving functor
  $$ |-| : P^{Spt}(Aff_\mathbf{C}) \longrightarrow Spt $$
on the [[infinity-category]] of [[infinity-presheaf|presheaves]] of [[spectra]], by taking the [[left Kan extension]] of the composite
  $$ P(Aff_\mathbf{C}) \stackrel{|-|}{\longrightarrow} Spc \stackrel{\Sigma^{\infty}}{\longrightarrow} Spt $$
along the canonical functor $P(Aff_\mathbf{C}) \to P^{Spt}(Aff_\mathbf{C})$ induced by taking [[suspension spectra]] objectwise.
=--

Let $T$ be a [[dg-category]] over $\mathbf{C}$. Let $K(T)$ denote the [[non-connective algebraic K-theory|nonconnective]] [[Waldhausen K-theory of a dg-category|Waldhausen K-theory]] of $T$. This defines a [[infinity-presheaf|presheaf]] of [[spectra]]
  $$ K(T \otimes_{\mathbf{C}} -) : Aff_C^{op} \longrightarrow Spt $$
which sends $Spec(A)$ to $K(T \otimes_{\mathbf{C}} A)$.

+-- {: .num_defn}
###### Definition
The **semi-topological K-theory** of $T$ is the [[spectrum]] defined by the formula
  $$ K^{st}(T) = |L^{A^1}(L^{et}(K(T \otimes_{\mathbf{C}} -)))| $$
where $L^{et}$ and $L^{A^1}$ are the [[etale topology|etale]] and $\mathbf{A}^1$-[[homotopy invariant]] [[localization of an (infinity,1)-category|localization]] endofunctors, respectively.
=--

+-- {: .num_defn}
###### Definition
The **semi-topological K-theory** of a complex [[scheme]] $X$ is the [[spectrum]]
  $$ K^{st}(T) = K^{st}(Perf(X)) $$
where $Perf(X)$ is the [[dg-category]] of [[perfect complexes]] on $X$.
=--

## Properties

Let $T$ be a [[dg-category]] over $\mathbf{C}$ and $\mathcal{M}_T$ the [[derived moduli stack of objects in a dg-category|moduli space of pseudo-perfect dg-modules]] over $T$. This is a [[derived stack]], hence an [[infinity-stack]] on the [[infinity-category]] of [[simplicial commutative rings]]. Applying the topological realization (which extends to presheaves on [[simplicial commutative rings]] in the obvious way), one gets a spectrum $|\mathcal{M}_T|$.

+-- {: .num_prop}
###### Proposition
$|\mathcal{M}_T|$ is an [[infinite loop space]], and there is a canonical identification
  $$ \tilde{K}^{st}(T) \simeq |\mathcal{M}_T| $$
where the left hand side is a [[connective spectrum|connective]] version of semi-topological K-theory.
=--

See ([Blanc 13](#Blanc13), 4.3), ([Toen 10](#Toen10)), ([Kaledin 10](#Kaledin10), section 8).

## Conjectures

+-- {: .num_conjecture}
###### Conjecture
**(lattice conjecture)**.
For every smooth proper [[dg-category]] $T$ over $\mathbf{C}$, the canonical morphism
  $$ ch^{top} \wedge_{\mathbf{S}} H \mathbf{C}
       : K^{top}(T) \wedge_{\mathbf{S}} H\mathbf{C}
       \longrightarrow HP(T) $$
induced by the noncommutative [[Chern character]] is an equivalence of [[spectra]].
=--

(move this to [[topological K-theory of a dg-category]]...)

## Examples
 {#Examples}

* On a [[point]], semi-topological K-theory coincides with [[topological K-theory]]:
  $$ K^{st}(\Spec(\mathbf{C})) \simeq K^{top}(\Spec(\mathbf{C})), $$
while the [[homotopy groups]] of [[algebraic K-theory]] are uncountable in degree $i \gt 0$.

* With finite [[coefficients]], semi-topological K-theory coincides with [[algebraic K-theory]]:
  $$ K_*^{st}(X, \mathbf{Z}/n) \simeq K_*^{alg}(X, \mathbf{Z}/n) $$
while the [[topological K-theory]] only sees the [[homotopy type]] of the variety and not the finer algebraic structure.

* Rationally, semi-topological K-theory contains information about the cycles on $X$, and conjecturally, the rational [[Hodge filtration]] on [[singular cohomology]].

* $K_0^{st}(X)$ coincides with the [[Grothendieck group]] of [[vector bundles]] up to [[algebraic equivalence]]. Rationally, an analogue of the [[Chern character]] map induces canonical isomorphisms
  $$ K_0^{st}(X, \mathbf{Q}) \stackrel{\sim}{\longrightarrow} CH^*_alg(X, \mathbf{Q}), $$
where on the right hand side is the group of [[algebraic cycles]] modulo [[algebraic equivalence]].

## References

A first definition of semi-topological K-theory for [[complex varieties]] was given in

* [[Eric M. Friedlander]] and [[Mark E. Walker]], _Semi-topological K-theory using function complexes_, Topology, 41(3):591&#8211;644, 2002.

An analogue of the [[Atiyah-Hirzebruch spectral sequence]], and computations of semi-topological K-theory for a large class of varieties, are in

* [[Eric M. Friedlander]], [[Christian Haesemeyer]], and [[Mark E. Walker]]. _Techniques, computations, and conjectures for semi-topological K-theory_, Math. Ann., 330(4):759&#8211;807, 2004, [web](http://www.math.uiuc.edu/K-theory/0621/).

A survey is

* [[Eric M. Friedlander]], [[Mark E. Walker]], _Semi-topological K-theory_, in [[Handbook of K-theory]], Springer, 2005, [web](http://www.math.illinois.edu/K-theory/handbook/).

Semi-topological K-theory for [[dg-categories]] was introduced by [[Bertrand Toen]] in lecture III of

* {#Toen10} [[Bertrand Toen]], _Saturated dg-categories_, lectures at Workshop on Homological Mirror Symmetry and Related Topics, January 2010, University of Miami, [notes](https://math.berkeley.edu/~auroux/frg/miami10-notes/).

Some discussion and interesting conjectures are in the last section of

* {#Kaledin10} [[D. Kaledin]], _Motivic structures in non-commutative geometry_, [arXiv:1003.3210](http://arxiv.org/abs/1003.3210).

A state of the art treatment via [[dg-categories]], from the point of view of [[derived noncommutative algebraic geometry]], is in

* {#Blanc13} [[Anthony Blanc]], _Topological K-theory of complex noncommutative spaces_, Ph.D. thesis, 2013, [arXiv:1211.7360](http://arxiv.org/abs/1211.7360).

[[!redirects semitopological K-theory]]

[[!redirects semi-topological K-theory of a dg-category]]
[[!redirects semitopological K-theory of a dg-category]]