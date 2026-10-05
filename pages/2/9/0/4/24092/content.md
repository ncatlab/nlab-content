
> This article is about premetric spaces as defined by Fred Richman. For other notions of premetric spaces, see [[premetric space]].

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

A more general concept of [[metric space]] by Fred Richman. While Fred Richman simply called these structures "[[premetric spaces]]", there are multiple notions of premetric spaces in the mathematical literature. 

## Definition ##

A __premetric space__ is a [[set]] $S$ with a ternary [[relation]] $(-)\sim_{(-)}(-)\colon S \times \mathbb{Q}_{\geq 0} \times S \to \Omega$, where $\mathbb{Q}_{\geq 0}$ represent the non-negative [[rational numbers]] in $\mathbb{Q}$ and $\Omega$ is the set of [[truth values]], such that 

* for all $x \in S$ and $y \in S$, $(x = y) \iff (x \sim_0 y)$

* for all $x \in S$ and $y \in S$, there exists $q \in \mathbb{Q}_{\geq 0}$ such that $x \sim_q y$

* for all $x \in S$, $y \in S$, $q \in \mathbb{Q}_{\geq 0}$, and $r \in (q, \infty)$, where $(q, \infty)$ is the set of all non-negative rational numbers strictly greater than $q$, then $(x \sim_r y) \iff (x \sim_q y)$

* for all $x \in S$, $y \in S$, $z \in S$, $q \in \mathbb{Q}_{\geq 0}$, and $r \in \mathbb{Q}_{\geq 0}$, if $x \sim_q y$ and $y \sim_r z$, then $x \sim_{q + r} z$. 

## Properties ##

Assuming [[excluded middle]], every premetric space is a [[metric space]]. Without excluded middle, however, every premetric space is a "metric space" which is valued in the lower Dedekind real numbers, rather than the two-sided Dedekind real numbers. 

## See also ##

* [[premetric space]]

* [[premetric space (Booij)]]

* [[metric space]]

## References ##

* [[Fred Richman]], *Real numbers and other completions*, Mathematical Logic Quarterly **54** 1 (2008) 98-108 &lbrack;[doi:10.1002/malq.200710024](https://onlinelibrary.wiley.com/doi/10.1002/malq.200710024)&rbrack;

[[!redirects premetric (Richman)]]
[[!redirects premetrics (Richman)]]
[[!redirects premetric space (Richman)]]
[[!redirects premetric spaces (Richman)]]

[[!redirects Richman premetric]]
[[!redirects Richman premetrics]]
[[!redirects Richman premetric space]]
[[!redirects Richman premetric spaces]]