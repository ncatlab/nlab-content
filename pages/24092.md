
> This entry is about the family of binary relations indexed by the non-negative rational numbers defined by Fred Richman in [Real numbers and other completions](http://math.fau.edu/richman/docs/RealNums.pdf), see [[Richman premetric space]]. For the family of binary relations indexed by the positive rational numbers defined by Auke Booij in [Analysis in univalent type theory](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf). 

***

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

## Idea ##

A more general concept of [[metric space]] by Fred Richman. While Fred Richman simply called these structures "[[premetric spaces]]", there are multiple notions of premetric spaces in the mathematical literature, so we shall refer to these as Richman premetric spaces. 

## Definition ##

A __Richman premetric space__ is a [[set]] $S$ with a ternary [[relation]] $(-)\sim_{(-)}(-)\colon S \times \mathbb{Q}_{\geq 0} \times S \to \Omega$, where $\mathbb{Q}_{\geq 0}$ represent the non-negative [[rational numbers]] in $\mathbb{Q}$ and $\Omega$ is the set of [[truth values]], such that 

* for all $x \in S$ and $y \in S$, $(x = y) \iff (x \sim_0 y)$

* for all $x \in S$ and $y \in S$, there exists $q \in \mathbb{Q}_{\geq 0}$ such that $x \sim_q y$

* for all $x \in S$, $y \in S$, $q \in \mathbb{Q}_{\geq 0}$, and $r \in (q, \infty)$, where $(q, \infty)$ is the set of all non-negative rational numbers strictly greater than $q$, then $(x \sim_r y) \iff (x \sim_q y)$

* for all $x \in S$, $y \in S$, $z \in S$, $q \in \mathbb{Q}_{\geq 0}$, and $r \in \mathbb{Q}_{\geq 0}$, if $x \sim_q y$ and $y \sim_r z$, then $x \sim_{q + r} z$. 

## Properties ##

Assuming [[excluded middle]], every Richman premetric space is a [[metric space]]. Without excluded middle, however, every Richman premetric space is a "metric space" which is valued in the lower Dedekind real numbers, rather than the two-sided Dedekind real numbers. 

## See also ##

* [[premetric space]]

* [[Booij premetric space]]

* [[metric space]]

## References ##

* [[Fred Richman]], Real numbers and other completions ([pdf](http://math.fau.edu/richman/docs/RealNums.pdf))

[[!redirects Richman premetric]]
[[!redirects Richman premetrics]]
[[!redirects Richman premetric space]]
[[!redirects Richman premetric spaces]]