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

In measure theory, a __$\sigma$-continuous probability valuation__ on a [[sigma-complete lattice|$\sigma$-complete lattice]] $(L, \leq, \bot, \vee, \top, \wedge, \Vee)$ is a [[probability valuation]] $\mu:L \to [0, 1]$ such that the $\sigma$-continuity condition is satisfied: for all sequences $s:\mathbb{N} \to L$, if $s(n) \leq s(n + 1)$ for all natural numbers $n \in\mathbb{N}$, then 
$$\mu(\Vee_{n:\mathbb{N}} s(n)) \leq \sup_{n:\mathbb{N}} \mu(s(n))$$

## See also ##

* [[unit interval]]

* [[sigma-continuous valuation]]

* [[probability valuation]]

* [[probability measure]]

## References ##

* [[Alex Simpson]], *Measure, randomness and sublocales*, Annals of Pure and Applied Logic, Volume 163, Issue 11, November 2012, Pages 1642-1659. ([doi:10.1016/j.apal.2011.12.014](https://doi.org/10.1016/j.apal.2011.12.014))