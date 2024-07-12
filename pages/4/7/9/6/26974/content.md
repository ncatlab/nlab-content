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
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

An *invariant measure* is a measure which is [[invariant]] under the [[action]] of a [[group]] or [[monoid]].

It is an important concept in [[probability theory]], [[dynamical systems]], [[statistical physics]], and [[representation theory]].

## Definitions

Let $X$ be a [[measurable space]], and let $M$ be a [[monoid]] with an [[action]] on $X$ via [[measurable functions]]. 
For each $m\in M$, denote the action on $X$ again by $m:X\to X$. 

A [[measure]] $p$ on $X$ is called **invariant** or **stationary** under the action of $M$ if and only if for all $m\in M$, the pushforward $m_*p$ is equal to $p$. That is, for each [[measurable subset]] $A\subseteq X$,
$$
p(m^{-1}(A)) \;=\; p(A) .
$$

### Examples

* The [[Haar integral|Haar measure]] on a [[compact]] [[topological group]] $G$ is invariant for the action of $G$ on itself, given by left multiplication.

* An [[exchangeable measure]] on a [[product]] space $X^\mathbb{N}$ is invariant under the action of finite [[permutations]].


### Actions via Markov kernels

A monoid $(M,e,\cdot)$ can also act on a measurable space $X$ via [[Markov kernels]]. That is, to each $m\in M$ we can assign a kernel $k_m:X\to X$ such that 
$$
k_e(A|x) \;=\; 1_A(x)
$$
and
$$
k_{m\cdot n}(A|x) \;=\; \int_X k_m(A|x')\,k_n(d x'|x) .
$$

In this case, a measure $p$ on $X$ is **invariant** or **stationary** if and only if for all $m\in M$, and for all measurable $A\subseteq X$,
$$
\int_X k_m(A|x) \, p(d x) \;=\; p(A) .
$$


## In terms of category theory

(...)


## Properties

* The [[ergodic decomposition theorem]] says that, under some condition, an invariant measure is a [[mixture]] of [[ergodic measure|ergodic ones]]. 


## References


* {#fritz_definetti} [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], _De Finetti's theorem in categorical probability_. Journal of Stochastic Analysis, 2021. ([arXiv:2105.02639](https://arxiv.org/abs/2105.02639))

* {#markov_ergodic} Sean Moss, [[Paolo Perrone]], _A category-theoretic proof of the ergodic decomposition theorem_, Ergodic Theory and Dynamical Systems, 2023. ([arXiv:2207.07353](https://arxiv.org/abs/2207.07353))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)


category: probability


[[!redirects invariant measures]]
[[!redirects invariant probability measure]]
[[!redirects invariant probability measures]]
[[!redirects stationary measure]]
[[!redirects stationary measures]]
[[!redirects invariant state]]
[[!redirects invariant states]]
[[!redirects stationary state]]
[[!redirects stationary states]]