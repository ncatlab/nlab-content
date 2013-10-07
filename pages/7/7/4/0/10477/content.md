
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **Reedy category with fibrant constants** is a [[Reedy category]] $R$ such that for every [[model category]] $M$ and every [[fibrant object]] $X \in M$ the constant $R$-[[diagram]] at $X$ is Reedy fibrant.

## Properties

+-- {: .num_theorem}
###### Theorem

For a Reedy category $R$ the following are equivalent.

1. $R$ has fibrant constants.
1. For any model category $M$ the [[colimit]] functor $\colim_R \colon M^R \to M$ is a [[Quillen adjunction|left Quillen functor]].
1. All matching categories of $R$ are [[connected category|connected]] or empty.

=--

This theorem is proven in [Hirschhorn,Proposition 15.10.2 and Theorem 15.10.8](#Hirshhorn).

+-- {: .num_theorem}
###### Proposition

1. The product of two Reedy categories with fibrant constants is a Reedy category with fibrant constants.
1. If $R$ is an [[elegant Reedy category]] and $X$ is a presheaf on $R$, then the [[category of elements]] of $X$ is a Reedy category with fibrant constants.

=--

+-- {: .proof}
###### Proof

1. This follows by combining point 3. of the theorem above with the fact that the matching categories satisfy the "Leibniz rule", see [Riehl, Verity, Observation 4.2](#RiehlVerity).
1. This is proven in [Hirschhorn, Proposition 15.10.4](#Hirschhorn) in the case of $R = \Delta$, but the argument given there applies to any elegant Reedy category.

=--

## Examples

* The [[simplex category]] $\Delta$ is a Reedy category with fibrant constants.

* More generally, Joyal's [[Theta category|disk categories]] $\Theta_n$ are Reedy categories with fibrant constants.

* Every [[direct category]] is a Reedy category with fibrant constants.


## References

* [[Philip Hirschhorn]],  _Model categories and their localizations_, volume 99 of Mathematical Surveys and Monographs, American Mathematical Society, 2009, {#Hirschhorn}

* [[Emily Riehl]], [[Dominic Verity]] _The theory and practice of Reedy categories_ [arXiv](http://arxiv.org/abs/1304.6871v1) {#RiehlVerity}