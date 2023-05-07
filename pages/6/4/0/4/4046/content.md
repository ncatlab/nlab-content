
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **pivotal category** is an [[autonomous category]] equipped with a [[monoidal natural transformation|monoidal natural isomorphism]] $A \to (A^*)^*$.  Pivotal categories have also been called "sovereign categories."  This is a kind of [[category with duals]].

A right autonomous category with such an isomorphism is automatically left autonomous too, so the right/left distinction does not apply to pivotal categories.

## Intuition

In an autonomous category $\mathscr{C}$, left duals and right duals have no reason to agree. That is, given an object $A\in\mathscr{C}$ we may not necessarily have $A\cong A^{**}$ (See [this MO post](https://mathoverflow.net/questions/303245/the-dual-of-a-dual-in-a-rigid-tensor-category) for a discussion). Even if we do (like in semisimple categories and braided monoidal categories) there is no a-priori reason for this isomorphism to be natural.

For this isomorphism to be natural we need a pivotal structure. Interestingly enough, if a pivotal structure exists then it will be unique up to precomposing with an element of the group $\text{Aut}^{\otimes}(\text{id}_{\mathscr{C}})$ of monoidal natural automorphisms of the identity [Bartlett, Prop. 5.7, Lemma 6.2](#Bartlett2009).

In the case of fusion categories, we have that $\text{Aut}^{\otimes}(\text{id}_{\mathscr{C}})\cong \text{Hom}(U_{\mathscr{C}},\mathbb{C}^{\times})$ where $U_{\mathscr{C}}$ is the universal grading group. Hence, there will be only finitely many choices of pivotal structures [Gelaki](#Gelaki2006).

## Related concepts

* {#Gelaki2006} [[Shlomo Gelaki]], _Nilpotent fusion categories_, Advances in Mathematics, [arXiv](https://arxiv.org/abs/math/0610726)

* {#Bartlett2009} [[Bruce Bartlett]], _On unitary 2-representations of finite groups and topological quantum field theory_, PhD thesis, [arXiv](https://arxiv.org/abs/0901.3975)

* [[fusion category]]

* **pivotal category

* [[spherical category]]


[[!redirects pivotal category]]
[[!redirects pivotal categories]]
[[!redirects sovereign category]]
[[!redirects sovereign categories]]
[[!redirects pivotal structure]]
[[!redirects pivotal structures]]
