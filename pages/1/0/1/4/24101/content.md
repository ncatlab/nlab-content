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

## Definition ##
In measure theory, a __content__ on a [[distributive lattice]] $(L, \leq, \bot, \vee, \top, \wedge)$ is a [[valuation (measure theory)|valuation]] $\mu:L \to [0, \infty]$ to the non-negative [[one-sided real number|lower reals]] such that the valuation of the bottom element is zero and additive if the pair of elements is disjoint.

$$\forall a\in L. \forall b \in L. \mu(\bot) = 0$$
$$\forall a\in L. \forall b \in L. (a \wedge b = \bot) \implies (\mu(a \vee b) = \mu(a) + \mu(b))$$

## See also ##

* [[valuation (measure theory)]]

* [[sigma-continuous valuation]]

* [[probability content]]

* [[measure]]

* [[Jordan content]]

## References ##

* Wikipedia, <a href="https://en.wikipedia.org/wiki/Content_(measure_theory)">*Content (measure theory)*</a>

[[!redirects contents]]