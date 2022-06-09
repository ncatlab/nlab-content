
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _probability distribution_ is a [[measure]] used in [[probability theory]] whose [[integral]] over some subspace of a [[measurable space]] is regarded as assigning a _probability_ for some event to take values in this subset.

Often a _[[probability density]]_.

## Definition

### On measurable spaces

A __probability distribution__ is a [[measure]] $\rho$ on a [[measurable space]] $X$ such that

* it is positive: $\forall U \subset X : \int_U d\rho \geq 0$;

* it is normalized: $\int_X d\rho = 1$.

### On $\sigma$-frames

In measure theory, a __probability measure__ or __probability distribution__ on a [[sigma-frame|$\sigma$-frame]] or more generally a [[sigma-complete lattice |$\sigma$-complete]] [[distributive lattice]] $(L, \leq, \bot, \vee, \top, \wedge, \Vee)$ is a [[probability valuation]] $\mu:L \to [0, 1]$ such that the elements are mutually disjoint and the probability valuation is denumerably/countably additive
$$\forall s\in L^\mathbb{N}. \forall m \in \mathbb{N}. \forall n \in \mathbb{N}. (m \neq n) \wedge (s(m) \wedge s(n) = \bot)$$
$$\forall s\in L^\mathbb{N}. \mu(\Vee_{n:\mathbb{N}} s(n)) = \sum_{n:\mathbb{N}} \mu(s(n))$$

## Properties

The collection of all probability distributions on a measurable space carries various [[metric]] structures that are studied in [[information geometry]]:

* [[information metric]]

* [[Wasserstein metric]]

## Examples

* [[Gaussian probability distribution]]


## Related concept

* [[probability space]]

* [[expectation value]]

* [[moment]]

* [[entropy]]

* [[positive-operator valued probability measure]]

* [[density of a subset]]

* [[unit interval]]

* [[sigma-frame]]

* [[sigma-complete lattice]]

* [[distributive lattice]]

* [[probability valuation]]

* [[sigma-continuous probability valuation]]

## References ##

* Alex Simpson, [Measure, randomness and sublocales](https://www.sciencedirect.com/science/article/pii/S0168007211001874). 

[[!redirects probability distribution]]
[[!redirects probability distributions]]
[[!redirects probability measure]]
[[!redirects probability measures]]
