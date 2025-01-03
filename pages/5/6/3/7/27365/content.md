

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

A [[partial order]] in the [[antithesis interpretation]] of [[constructive mathematics]] in [[intuitionistic logic]]. 

## Definition

An **antithesis partial order** is a [[partial order]] $(A, \leq)$ equipped with an [[irreflexive relation|irreflexive]] and [[symmetric relation]] $\nsim$ and a relation $\lt$ such that for all $x \in A$, $y \in A$, and $z \in A$,

* $x \leq y$ and $y \lt z$ implies that $x \lt z$

* $x \lt y$ and $y \leq z$ implies that $x \lt z$

* $x \lt y$ implies that $x \nsim y$

* $x \nsim y$ implies that $x \lt y$ or $y \lt x$

In addition, we have the following concepts:

* An antithesis partial order $A$ is **strong** if $\lt$ is a [[cotransitive relation]]. 

* An antithesis partial order $A$ is **linear** if for all $x \in A$ and $y \in A$, $x \lt y$ implies $x \leq y$. 

* An antithesis partial order $A$ is **total** if $\leq$ is a [[total relation]]. 

* An antithesis partial order $A$ is **affirmative** if $\nsim$ is a [[denial inequality]]. 

* An antithesis partial order $A$ is **refutative** if $\nsim$ is a [[tight relation]]. 

## Examples

* The order in an [[ordered Kock field]] is a strong linear affirmative antithesis partial order. 

## Related concepts

* [[partial order]]

* [[pseudo-order]]

* [[total order]]

* [[antithesis interpretation]]

## References

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

[[!redirects antithesis partial order]]
[[!redirects antithesis partial orders]]

[[!redirects antithesis poset]]
[[!redirects antithesis posets]]

[[!redirects strong antithesis partial order]]
[[!redirects strong antithesis partial orders]]

[[!redirects strong antithesis poset]]
[[!redirects strong antithesis posets]]

[[!redirects linear antithesis partial order]]
[[!redirects linear antithesis partial orders]]

[[!redirects linear antithesis poset]]
[[!redirects linear antithesis posets]]

[[!redirects total antithesis partial order]]
[[!redirects total antithesis partial orders]]

[[!redirects total antithesis poset]]
[[!redirects total antithesis posets]]

[[!redirects affirmative antithesis partial order]]
[[!redirects affirmative antithesis partial orders]]

[[!redirects affirmative antithesis poset]]
[[!redirects affirmative antithesis posets]]

[[!redirects refutative antithesis partial order]]
[[!redirects refutative antithesis partial orders]]

[[!redirects refutative antithesis poset]]
[[!redirects refutative antithesis posets]]