
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Solid abelian groups are objects which form the basis of non-archimedean analysis in certain approaches to mathematics, such as [[condensed mathematics]]. 

## Definition

### As a functor

A ***solid abelian group*** is an [[additive functor]] from the category of [[free abelian groups]] to the category of [[abelian groups]]. 

This definition is due to [[Dustin Clausen]] [here](https://golem.ph.utexas.edu/category/2020/03/pyknoticity_versus_cohesivenes.html#c057781). 

### In terms of condensed abelian groups

Let $S = \underset{\leftarrow}{\lim}_i S_i$ be a [[profinite set]], and define the [[condensed abelian group]] $\mathbb{Z}[S]^\square \coloneqq \underset{\leftarrow}{\lim}_i \mathbb{Z}[S_i]$, where $\mathbb{Z}[T]$ is the [[free abelian group]] on the set $T$. There is a natural map $m:S \to \mathbb{Z}[S]^\square$ which induces a map $\mathbb{Z}[S] \to \mathbb{Z}[S]^\square$. 

A **solid abelian group** is a condensed abelian group $A$ such that for all profinite sets $S$ and all maps $f:S \to A$, there is a unique map $g:\mathbb{Z}[S]^\square \to A$ such that $f = g \circ m$. 

## Properties

According to [[Peter Scholze]] in [this comment on the nCafé](https://golem.ph.utexas.edu/category/2020/03/pyknoticity_versus_cohesivenes.html#c057780) in the absense of the [[presentation axiom]], the category of solid abelian groups is not a condensed category. 

## See also

* [[condensed abelian group]]
* [[solidification functor]]
* [[solid spectrum]]

## References

* {#ScholzeLCM} [[Peter Scholze]], _Lectures on condensed mathematics_, [pdf](https://www.math.uni-bonn.de/people/scholze/Condensed.pdf)