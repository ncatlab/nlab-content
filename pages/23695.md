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
### In set theory ###
In measure theory, a __$\sigma$-continuous valuation__ on a [[sigma-complete lattice|$\sigma$-complete lattice]] $(L, \leq, \bot, \vee, \top, \wedge, \Vee)$ is a [[valuation (measure theory)|valuation]] $\mu:L \to [0, \infty]$ such that the $\sigma$-continuity condition is satisfied: for all sequences $s:\mathbb{N} \to L$, if $s(n) \leq s(n + 1)$ for all natural numbers $n \in\mathbb{N}$, then 
$$\mu(\Vee_{n:\mathbb{N}} s(n)) \leq \sup_{n:\mathbb{N}} \mu(s(n))$$

## See also ##

* [[valuation (measure theory)]]

* [[sigma-continuous probability valuation]]

* [[content]]

* [[measure]]

## References ##

* Alex Simpson, [Measure, randomness and sublocales](https://www.sciencedirect.com/science/article/pii/S0168007211001874). 