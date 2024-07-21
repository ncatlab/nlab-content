+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}


## Idea

In [[probability theory]], a [[sigma-algebra]] can be interpreted as a system of possible "distinctions" that can be made in a [[measurable space|measurable]] or [[probability space]] $X$. 

A *filtration* on a probability space is an increasing system of [[sigma-algebras]], for example indexed by time, which one can interpret as "being able to make more and more distinctions", or "learning more and more as time progresses".

As the intuition may suggest, it is an instantiation of the categorical notion of [[filtration]], in the context of [[probability theory]].


## Definition

A **filtered probability space** consists of a [[probability space]] $(X,\mathcal{A},p)$, equipped with a [[filtration]] of sub-[[sigma-algebras]] of $\mathcal{A}$, i.e. a collection $(\mathcal{F}_i)_{i\in I}$ where:

* $I$ is a [[partially ordered set]] (often totally ordered), with finitary [[upper bounds]];
* For each $i\in I$, $\mathcal{F}_i$ is a sub-sigma-algebra of $\mathcal{A}$;
* For each $i\le j\in I$, $\mathcal{F}_i\subseteq \mathcal{F}_j$.

Note that a filtration $(\mathcal{F}_i)_{i\in I}$  as defined above is a [[filtered object]] in the category of [[sigma-algebras]], but a [[cofiltered object]] in the category of measurable or probability spaces. Indeed, if $\mathcal{F}_i\subseteq \mathcal{F}_j$, the set-theoretic identity map $X\to X$ is measurable as a function $(X,\mathcal{F}_j)\to(X,\mathcal{F}_i)$, but not the other way around.


## Limits and colimits

(...)


## Related concepts

* [[probability space]], [[random variable]], [[stochastic process]]
* [[martingale]]

[[!include filtered objects -- contents]]


## References

* {#vb_martingales} Ruben Van Belle, _A categorical treatment of the Radon-Nikodym theorem and martingales_, 2023. ([arXiv](https://arxiv.org/abs/2305.03421))

* {#dagger_martingales} [[Paolo Perrone]] and Ruben Van Belle, _Convergence of martingales via enriched dagger categories_, 2024. ([arXiv](https://arxiv.org/abs/2404.15191))

### Introductory material

* [[Paolo Perrone]], _Starting Category Theory_, World Scientific, 2024, Section 3.2.7. ([website](https://www.worldscientific.com/worldscibooks/10.1142/13670))

* [[Paolo Perrone]], _Convergence of martingales via enriched dagger categories_, video talk, 2024. ([YouTube](https://www.youtube.com/watch?v=awr4RBrhh1g))


category: probability

[[!redirects filtered probability spaces]]