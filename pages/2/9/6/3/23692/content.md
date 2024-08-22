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

$$\Vee_{i:\mathbb{N}} (-)(i): (\mathbb{N} \to L) \to L$$

such that 

* for all natural numbers $n \in \mathbb{N}$ and sequences $s: \mathbb{N} \to L$
$$ s(n) \leq \Vee_{i:\mathbb{N}} s(i)$$

* for all elements $x \in L$ and sequences $s: \mathbb{N} \to L$, if $s(n) \leq x$ for all natural numbers $n \in \mathbb{N}$, then 
$$\Vee_{i:\mathbb{N}} s(i) \leq x$$

## See also ##

* [[lattice]]

* [[sigma-frame]]

* [[sigma-complete Heyting algebra]]

* [[sigma-continuous valuation]]

* [[sigma-continuous probability valuation]]

## References ##

* [[Alex Simpson]], *Measure, randomness and sublocales*, Annals of Pure and Applied Logic, Volume 163, Issue 11, November 2012, Pages 1642-1659. ([doi:10.1016/j.apal.2011.12.014](https://doi.org/10.1016/j.apal.2011.12.014))