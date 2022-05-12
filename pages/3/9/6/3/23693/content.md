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

A __$\sigma$-frame__ is a [[sigma-complete lattice|$\sigma$-complete lattice]] $(L, \leq, \bot, \vee, \top, \wedge, \Vee)$ such that for all elements $a \in L$ and sequences $s:\mathbb{N} \to L$, 
$$a \wedge \Vee_{n:\mathbb{N}} s(n) = \Vee_{n:\mathbb{N}} a \wedge s(n)$$

## Examples ##

* [[Sierpinski space]], denoted as $\Sigma$ or $1_\bot$, is the initial $\sigma$-frame. 

## See also ##

* [[sigma-complete lattice]]

* [[distributive lattice]]

* [[measure]]

* [[probability measure]]

* [[Dedekind cut]]

* [[Dedekind real numbers]]

* [[sigma-pretopos]]

* [[streak]]

## References ##

* Alex Simpson, [Measure, randomness and sublocales](https://www.sciencedirect.com/science/article/pii/S0168007211001874). 

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)