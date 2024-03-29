
#Contents#
* table of contents
{:toc}

## Definition

In [[non-archimedean analytic geometry]], one considers:

Given a [[topological space]], a _quasinet_ in $X$ is a [[set]] $\tau = \{V_i\}$ of [[subsets]] of $X$ such that for each point $x\in X$ there exists a finite number of such subsets $V_{i_1}, \cdots, V_{i_n} \in \tau$ such that

1. $x\in V_{i_1} \cap V_{i_2} \cap \cdots \cap V_{i_n}$ (the point is in their [[intersection]]);

1. $V_{i_1} \cup \cdots \cup V_{i_n}$ is a [[neighbourhood]] of $x$.

(e.g. [Berkovich 09, def. 3.1.1.](#Berkovich09))

A quasinet $\tau$ is called a _net_ if for all $U,V \in \tau$ then the restriction $\tau|_{U \cap V}$ is a quasinet of $U \cap V$.

## Examples

* A [[Berkovich analytic space]] is a [[locally Hausdorff topological space|locally Hausdorff]] [[topological space]] equipped with an [[atlas]] by [[affinoid domains]] such that the underlying [[analytic spectrum]] [[topological spaces]] of these form a net of [[compact subsets]] on $X$.



## References



* {#Berkovich09} [[Vladimir Berkovich]], _Non-archimedean analytic spaces_, lectures at the _Advanced School on $p$-adic Analysis and Applications_, ICTP, Trieste, 31 August - 11 September 2009 ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Trieste_2009.pdf))

[[!redirects quasi-nets]]

[[!redirects quasinet]]
[[!redirects quasinets]]
