+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _circle type_ is an [[axiom|axiomatization]] of the [[homotopy type]] of the ([[shape modality|shape]] of) the [[circle]] in the context of [[homotopy type theory]].

## Definition

As a [[higher inductive type]], the circle is given by

    Inductive Circle : Type
      | base : Circle
      | loop : Id Circle base base

This says that the type is inductive constructed from a [[terms]] in the circle, whose [[semantics|interpretation]] is as the base point of the circle, together with a term in the [[identity type]] of paths between these two terms, which interprets as the 1-cell of the circle

$$
  base \stackrel{loop}{\to} base
  \,
$$

a non-constant path from the base point to itself.

### As a suspension

The circle type could also be defined as the [[suspension type]] $\Sigma \mathbf{2}$ of the type of booleans $\mathbf{2}$. 

## See also

* [[circle]], [[unit circle]], [[circle group]]

* [[minimal simplicial circle]]

* [[suspension type]]

## References

A formalization of the [[shape modality|shape]] [[homotopy type]] $&#643; S^1 \simeq \mathbf{B}\mathbb{Z}$ of the circle as a [[higher inductive type]] in [[homotopy type theory]], along with a proof that $\Omega &#643;S^1\simeq {\mathbb{Z}}$ (and hence $\pi_1(&#643;S^1) \simeq \mathbb{Z}$):

* {#LicataShulman13} [[Dan Licata]], [[Mike Shulman]], *Calculating the Fundamental Group of the Circle in Homotopy Type Theory*, LICS '13: Proceedings of the 2013 28th Annual ACM/IEEE Symposium on Logic in Computer Science June 2013 ([arXiv:1301.3443](http://arxiv.org/abs/1301.3443), [doi:10.1109/LICS.2013.28](https://doi.org/10.1109/LICS.2013.28))

  > blog announcement: [A formal proof that $\pi_1(S^1) = \mathbb{Z}$](https://homotopytypetheory.org/2011/04/29/a-formal-proof-that-pi1s1-is-z/)

* {#BezemBuchholtzGraysonShulman19} [[Marc Bezem]], [[Ulrik Buchholtz]], [[Daniel Grayson]], [[Michael Shulman]], _Construction of the Circle in UniMath_, Journal of Pure and Applied Algebra Volume 225, Issue 10, October 2021, 106687 ([arXiv:1910.01856](https://arxiv.org/abs/1910.01856))


The proof is formalized therein using the [[Agda]] [[proof assistant]].  See also

* The [[HoTT Book]], section 8.1

* The HoTT Coq library: [theories/hit/Circle.v](https://github.com/HoTT/HoTT/blob/master/theories/hit/Circle.v)

* The HoTT Agda library: [homotopy/LoopSpaceCircle.agda](https://github.com/HoTT/HoTT-Agda/blob/2.0/homotopy/LoopSpaceCircle.agda)

[[!redirects circle types]]