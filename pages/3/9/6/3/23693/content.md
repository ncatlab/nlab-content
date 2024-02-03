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

* [[Rosolini dominance]]

* The [[intrinsic topology]] on a set $A$, which is the [[function set]] $\Sigma^A$

* Malcev topologies for set $A$, which are a $\sigma$-[[subobject|subframe]] of the intrinsic topology $\Sigma^A$. 

* Any [[frame]] is a $\sigma$-frame. In particular, the [[poset of truth values]] is a $\sigma$-frame. 

## See also ##

* [[sigma-complete lattice]]

* [[distributive lattice]]

* [[measure]]

* [[probability measure]]

* [[Dedekind cut]]

* [[Dedekind real numbers]]

* [[sigma-pretopos]]

* [[streak]]

* [[sigma-topological space]]

* [[sigma-locale]]

* [[limited principle of omniscience]]

## References ##

* Francesco Ciraulo, *$\sigma$-locales in Formal Topology*, Logical Methods in Computer Science, Volume 18, Issue 1 (January 12, 2022) ([doi:10.46298/lmcs-18%281%3A7%292022](https://doi.org/10.46298/lmcs-18%281%3A7%292022), [arXiv:1801.09644](https://arxiv.org/abs/1801.09644))

* [[Alex Simpson]], *Measure, randomness and sublocales*, Annals of Pure and Applied Logic, Volume 163, Issue 11, November 2012, Pages 1642-1659. ([doi:10.1016/j.apal.2011.12.014](https://doi.org/10.1016/j.apal.2011.12.014))

* [[Andrej Bauer]], *Spreen spaces and the synthetic Kreisel-Lacombe-Shoenfield-Tseitin theorem* ([arXiv:2307.07830](https://arxiv.org/abs/2307.07830))

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)