[[!redirects tau-smoothness]]

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **$\tau$-additive measure** (alias τ-regular, τ-smooth) is a [[measure]] on a [[topological space]] which interacts well with the topology. In particular, it has a well-defined and well-behaved [[support]].

$\tau$-additive measures can be thought of as a point of contact between [[measure theory]], and the theory of [[valuation (measure theory)|valuations]]. More on this in [[correspondence between measure and valuation theory]].

## Definition

Let $X$ be a [[topological space]]. A positive [[Borel subset|Borel measure]] $\mu$ on $X$ is called **$\tau$-additive**, or **$\tau$-smooth**, or **$\tau$-regular**, if for every directed [[net]] $\{U_\lambda\}_{\lambda\in\Lambda}$ of [[open subsets]] of $X$,
$$
  \mu \big( \sup_{\lambda} U_\lambda \big) 
  = 
  \sup_\lambda \mu(U_\lambda) .
$$

This property can be considered an instance of [[Scott topology|Scott continuity]], and is equivalent to continuity of the [[valuation (measure theory)|valuation]] defined by $\mu$ on the open sets.

## Examples

Every [[Radon measure]] on a [[Hausdorff space]] is $\tau$-additive. This includes most regular measures of common use, such as

* the [[Dirac measures]],
* the [[Lebesgue measure]] on the real line,
* the measure induced by the [[volume form]] of a Riemannian manifold,
* the [[Haar measure]] on a Lie group (or more generally a locally compact Hausdorff topological group).

## Properties

### Pushforward, products and marginals

* The [[pushforward measure]] of a $\tau$-additive measure along a [[continuous map]] is itself $\tau$-additive. In particular, the [[marginals]] of a $\tau$-additive measure are $\tau$-additive. This permits to construct a [[functor]], even a [[monad]] (see [below](#monad_structure)).

* The [[product measure|product]] of two $\tau$-additive measures on a product space can be extended to a $\tau$-additive measure. 

### Monad structure

One can form a [[measure monad]] analogous to the [[Giry monad]], whose functor part assigns to a topological space the space of $\tau$-additive measures over it. This monad is a submonad of the [[extended probabilistic powerdomain]]. See [[extended probabilistic powerdomain#the_measure_monad_on_top|the measure monad on Top]] for more details.


### Null sets and support 

Given a tau-additive measure $\mu$ on a topological space $X$, an open set $U\subseteq X$ is called **null** for $\mu$ if $\mu(U)=0$. A set has **full measure** if its complement is null.

By $\tau$-additivity, the union of all null open sets is null. Its [[complement]], which is a closed set, is called the **[[support]]** of $\mu$.
It can be seen as the smallest closed set of full measure. 

This definition can be extended to [[valuation (measure theory)#null_sets_and_support|continuous valuations]].

### Relationship with other measure-theoretical notions 

* Every [[Radon measure]] on a [[Hausdorff space]] is $\tau$-additive.
* Every $\tau$-additive measure on a [[compact Hausdorff space]] is [[Radon measure|Radon]].
* Every $\tau$-additive measure can be restricted to a [[continuous valuation]].
* Every [[continuous valuation]] on a [[regular space|regular]] [[Hausdorff space]] or on a [[locally compact space|locally compact]] [[sober space]] can be extended to a $\tau$-additive measure. 

See also: [[valuation (measure theory)#extending_valuations_to_measures|Extending valuations to measures]].

## Related notions

* [[Borel measure]]

* [[Radon measure]]

* [[continuous valuation]]

* [[extended probabilistic powerdomain]]

* [[correspondence between measure and valuation theory]]

## References

* V. Bogachev, _Measure Theory_, vol. 2 (2007).

[[!redirects tau-additive measures]]
[[!redirects tau-regular measure]]
[[!redirects tau-regular measures]]
[[!redirects tau-smooth measure]]
[[!redirects tau-smooth measures]]
[[!redirects τ-additive measure]]
[[!redirects τ-additive measures]]
[[!redirects τ-smooth measure]]
[[!redirects τ-smooth measures]]
[[!redirects τ-regular measure]]
[[!redirects τ-regular measures]]
[[!redirects tau-additive]]
[[!redirects tau-smooth]]
[[!redirects tau-regular]]
[[!redirects τ-additive]]
[[!redirects τ-smooth]]
[[!redirects τ-regular]]
[[!redirects $\tau$-additive measure]]
[[!redirects $\tau$-additive measures]]
[[!redirects $\tau$-additive]]
[[!redirects $\tau$-smooth measure]]
[[!redirects $\tau$-smooth measures]]
[[!redirects $\tau$-smooth]]
[[!redirects $\tau$-regular measure]]
[[!redirects $\tau$-regular measures]]
[[!redirects $\tau$-regular]]
[[!redirects tau-additivity]]
[[!redirects tau-smoothness]]
[[!redirects tau-regularity]]
[[!redirects τ-additivity]]
[[!redirects τ-smoothness]]
[[!redirects τ-regularity]]
[[!redirects $\tau$-additivity]]
[[!redirects $\tau$-smoothness]]
[[!redirects $\tau$-regularity]]