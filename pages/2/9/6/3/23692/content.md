+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##

A __$\sigma$-complete lattice__ is a [[lattice]] $(L, \leq, \bot, \vee, \top, \wedge)$ with a function

$$\Vee_{n:\mathbb{N}} (-)(n): (\mathbb{N} \to L) \to L$$

such that 

* for all natural numbers $n \in \mathbb{N}$ and sequences $s: \mathbb{N} \to L$
$$ s(n) \leq \Vee_{n:\mathbb{N}} s(n)$$

* for all elements $x \in L$ and sequences $s: \mathbb{N} \to L$ if $s(n) \leq x)$ for all natural numbers $n \in \mathbb{N}$, then 
$$\Vee_{n:\mathbb{N}} s(n) \leq x$$

## See also ##

* [[lattice]]

* [[sigma-frame]]

* [[sigma-continuous valuation]]

* [[sigma-continuous probability valuation]]

## References ##

* Alex Simpson, [Measure, randomness and sublocales](https://www.sciencedirect.com/science/article/pii/S0168007211001874). 