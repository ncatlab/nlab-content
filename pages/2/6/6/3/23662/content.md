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

be the positive rational numbers. Let $S$ be a [[rational premetric space]], and let $x:I \to S$ be a [[net]] with index set $I$. A __$I$-modulus of convergence__ is a function $M \in {\mathbb{Q}_{+}} \to I$ such that for all positive rational numbers $\epsilon$ and all indices $i \in I$ and $j \in I$, if $i \geq M(\epsilon)$ and $j \geq M(\epsilon)$, then $x_i \sim_{\epsilon} x_j$. 

The composition $x \circ M$ of a net $x$ and a modulus of convergence $M$ is also a [[net]]. 

## See also ##

* [[limit of a net]]
* [[premetric space]]
* [[modulated Cauchy complete space]]
* [[Cauchy structure]]
* [[Cauchy approximation]]
* [[HoTT book real numbers]]

## References ##

* Auke B. Booij, Analysis in univalent type theory ([pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf))

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)