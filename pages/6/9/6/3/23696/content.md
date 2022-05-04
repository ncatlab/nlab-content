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

In measure theory, a __probability valuation__ on a [[lattice]] $(L, \leq, \bot, \vee, \top, \wedge)$ is a [[monotonic function]] $\mu:L \to [0, 1]$ such that $\mu(\bot) = 0$, $\mu(\top) = 1$, and the modularity condition is satisfied: for all elements $a, b \in L$, 
$$\mu(a) + \mu(b) = \mu(a \wedge b) + \mu(a \vee b)$$

## See also ##

* [[unit interval]]

* [[valuation (measure theory)]]

* [[sigma-continuous probability valuation]]

## References ##

* Alex Simpson, [Measure, randomness and sublocales](https://www.sciencedirect.com/science/article/pii/S0168007211001874). 