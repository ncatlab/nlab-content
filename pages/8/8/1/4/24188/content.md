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

The _James construction type_ is an [[axiom|axiomatization]] of the [[James construction]] in the context of [[homotopy type theory]].

## Definition

As a [[higher inductive type]], the James construction type $J A$ of a [[pointed type]] $(A, a)$ is given by the following constructors

* $\epsilon_{J A} : J A$
* $\alpha_{J A} : A \to J A \to J A$
* $\delta_{J A} : \prod_{x : J A} x = \alpha_{J A}(a)(x)$

In [[Coq]] pseudocode this becomes

    Inductive JamesConstruction (A : PointedType) : Type
      | epsilon : JamesConstruction A
      | alpha : A -> JamesConstruction A -> JamesConstruction A
      | delta : forall (x : JamesConstruction A) x = alpha point x

We can see that $J A$ is simply the [[free monoid]] on $A$. The higher inductive type is recursive which can make it difficult to study. This however can be remedied by defining a sequence of types $(J_n A)_{n: \mathbb{N}}$ together with maps $(i_n : J_n A \to J_{n+1} A)_{n:\mathbb{N}}$ such that the type $J_\infty A$ defined as the [[sequential colimit]] of $(J_n A)_{n:\mathbb{N}}$ is equivalent to $J A$.

## Properties ##

There is an equivalence of types $J A \simeq \Omega \Sigma A$ if $A$ is [[0-connected]].

## Related concepts

* [[higher inductive type]]

* [[pointed type]]

* [[free monoid]]

* [[James construction]]

## References

* {#Brunerie16} [[Guillaume Brunerie]], _On the homotopy groups of spheres in homotopy type theory_ ([arxiv:1606.05916](https://arxiv.org/abs/1606.05916))

* {#LumsdaineShulman17} [[Peter LeFanu Lumsdaine]], [[Mike Shulman]], _Semantics of higher inductive types_ ([arXiv:1705.07088](https://arxiv.org/abs/1705.07088))

* {#Brunerie17} [[Guillaume Brunerie]], _The James construction and $\pi_4(S^3)$ in homotopy type theory_ ([arXiv:1710.10307](https://arxiv.org/abs/1710.10307))

[[!redirects James construction types]]