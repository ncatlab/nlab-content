
> This entry is about the family of binary relations indexed by the positive rational numbers defined by Auke Booij in [Analysis in univalent type theory](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf). For the family of binary relations indexed by the non-negative rational numbers defined by Fred Richman in [Real numbers and other completions](http://math.fau.edu/richman/docs/RealNums.pdf), see [[Richman premetric space]]. 

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

A more general concept of [[metric space]] by Auke Booij. While Auke Booij simply called these structures "[[premetric spaces]]", there are multiple notions of premetric spaces in the mathematical literature, so we shall refer to these as Booij premetric spaces. 

## Definition ##

A __Booij premetric space__ is a [[set]] $S$ with a ternary [[relation]] $a \sim_\epsilon b$ for $a \in S$, $b \in S$, and $\epsilon \in \mathbb{Q}_+$, where $\mathbb{Q}_+$ represent the positive [[rational numbers]] in $\mathbb{Q}$. 

Booij premetric spaces are used as in the construction of the [[Cauchy real numbers]] and the [[HoTT book real numbers]]. 

## Generalizations

Booij premetric spaces could be generalized from the positive rational numbers $\mathbb{Q}_+$ to any set $T$. These are called $T$-premetric spaces, which are sets $S$ with a ternary [[relation]] $a \sim_\epsilon b$ for $a \in S$, $b \in S$, and $\epsilon \in T$. These could also be used to construct the [[HoTT book real numbers]], if one only has an integral subdomain $R \subseteq \mathbb{Q}$ such as the [[dyadic rational numbers]] or the [[decimal rational numbers]], where $T$ is $R_+$. 

## See also ##

* [[premetric space]]

* [[Richman premetric space]]

* [[Cauchy structure]]

* [[metric space]]

## References ##

* Auke B. Booij, Analysis in univalent type theory ([pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf))

[[!redirects Booij premetric]]
[[!redirects Booij premetrics]]
[[!redirects Booij premetric space]]
[[!redirects Booij premetric spaces]]