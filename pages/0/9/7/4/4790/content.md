
> See also _[[quaternionic unitary group]]_ for the compact form.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition 

For $n \in \mathbb{N}$, the **symplectic group** $Sp(2n, \mathbb{R})$ is one of the [[classical Lie groups]].

It is the subgroup of the [[general linear group]] $GL(2n, \mathbb{R})$ of elements preserving the canonical [[symplectic form]] $\Omega$ on the [[Cartesian space]] $\mathbb{R}^{2n}$, that is: the group consisting of those [[matrices]] $A$ such that

$$
  A^T \Omega A = \Omega
  \,.
$$

The real symplectic group $Sp(2n,\mathbb{R})$ should not be confused with the *[[compact symplectic group]]* $Sp(n)$, which is the [[maximal compact subgroup]] of the _complex_ symplectic group $Sp(2n,\mathbb{C})$.

## Properties

### Maximal compact subgroup
 {#MaximalCompactSubgroup}

The [[maximal compact subgroup]] of the symplectic group $Sp(2n, \mathbb{R})$ is the [[unitary group]] $U(n)$.

### Homotopy groups
 {#HomotopyGroups}

By the [above](#MaximalCompactSubgroup) the [[homotopy groups]] of the symplectic group are those of the corresponding [[unitary group]].

In particular the first [[homotopy group]] of the symplectic group is the [[integers]]

$$
  \pi_1(Sp(2n,\mathbb{R})) \simeq \mathbb{Z}
  \,.
$$

The unique connected [[double cover]] obtained from this is the [[metaplectic group]] [[group extension|extension]] $Mp(2n) \to Sp(2n, \mathbb{R})$.

## Related concepts

* [[conformal symplectic group]]

* [[affine symplectic group]]

* [[metaplectic group]]

* [[extended affine symplectic group]]

* [[orthosymplectic supergroup]]

* A higher analog of the symplectic group in [[2-plectic geometry]] is the [[exceptional Lie group]] [[G₂]] (see there for more details).

* [[quaternionic unitary group]]


## References
	

The term "symplectic group" was suggested in 

* [[Hermann Weyl]], _The Classical Groups: their invariants and representations_ (1939, p. 165) 

by

> The name "complex group" formerly advocated by me in allusion to line complexes, as these are defined by the vanishing of antisymmetric bilinear forms, has become more and more embarrassing through collision with the word "complex" in the connotation of complex number. I therefore propose to replace it by the corresponding Greek adjective "symplectic." Dickson calls the group the "Abelian linear group" in homage to Abel who first studied it.

On [[homotopy groups]]:

* {#MimuraToda63} Mamoru Mimura, Hiroshi Toda, _Homotopy groups of symplectic groups_, J. Math. Kyoto Univ. Volume 3, Number 2 (1963), 251-273 ([Euclid:1250524819](https://projecteuclid.org/euclid.kjm/1250524819))

O. Meara's book studies symplectic group of a finite dimensional symplectic or even alternating space (space with an alternating form, not necessarily nondegenerate) over an arbitrary field

* O. T. Meara, _Symplectic groups_, Math. Surveys __16__, Amer. Math. Soc. 1978

A generalization, a symplectic group over a noncommutative algebra with involution is studied in 

* D. Alessandrini, A. Berenstein, [[V. Retakh]], E. Rogozinnikov,  A. Wienhard, _Symplectic groups over noncommutative algebras_ Sel. Math. New Ser. __28__, 82 (2022) [doi](https://doi.org/10.1007/s00029-022-00787-x)

[[!redirects symplectic group]]
[[!redirects symplectic groups]]
