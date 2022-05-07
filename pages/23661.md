[[!redirects Cauchy approximations]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##

Let $\mathbb{Q}$ be the [[rational numbers]] and let 

$$\mathbb{Q}_{+} \coloneqq \{x \in \mathbb{Q} \vert 0 \lt x\}$$ 

be the set of positive rational numbers. Let $(S, \sim)$ be a [[premetric space]]. A __Cauchy approximation__ is a function $x: \mathbb{Q}_{+} \to S$ such that for all positive rational numbers $\delta$ and $\eta$, $x(\delta) \sim_{\delta + \eta} x(\eta)$. 

The set of all Cauchy approximations is defined as

$$C(S) \coloneqq \{x \in S^{\mathbb{Q}_{+}} \vert \forall \delta \in \mathbb{Q}_{+}.\forall \eta \in \mathbb{Q}_{+}.x(\delta) \sim_{\delta + \eta} x(\eta)\}$$ 

## Properties ##

Every Cauchy approximation is a [[Cauchy net]] indexed by the positive rational numbers $\mathbb{Q}_{+}$. 

A Cauchy approximation is the composition $x \circ M$ of a [[net]] $x$ and an [[modulus of convergence]] $M$. 

## See also ##

* [[premetric space]]
* [[Cauchy structure]]
* [[modulus of convergence]]
* [[Cauchy real numbers]]
* [[HoTT book real numbers]]

## References ##

* Auke B. Booij, Analysis in univalent type theory ([pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf))

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)