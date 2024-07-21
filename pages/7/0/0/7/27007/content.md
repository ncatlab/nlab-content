+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## Idea

(...)


## Definition

Let $(X,\mathcal{A},p,(\mathcal{F}_n))$ be a [[filtered probability space]].

A **martingale** on $(X,\mathcal{A},p,(\mathcal{F}_n))$ is a [[stochastic process]] (collection of [[random variables]]) $f_n:X\to\mathbb{R}$ such that 

* For every $n$, the function $f_n$ is $\mathcal{F}_n$-measurable (i.e. the process is *adapted* to the [[filtered probability space|filtration]]:);
* For each $n\le m$, the function $f_n$ is a [[conditional expectation]] of $f_m$ given $\mathcal{F}_n$:
$$
f_n \;=\; \mathbb{E}(f_m|\mathcal{F}_n) .
$$

Similar definitions can be given for [[random variables]] with values in other spaces, for example, [[Banach spaces]].


### Variations 

A **submartingale** on a [[filtered probability space]] $(X,\mathcal{A},p,(\mathcal{F}_n))$ is an adapted stochastic process $(f_n)$ satisfying 
$$
f_n \;\le\; \mathbb{E}(f_m|\mathcal{F}_n) 
$$
for each $n\le m$.

Similarly, a **supermartingale** on $(X,\mathcal{A},p,(\mathcal{F}_n))$ is an adapted stochastic process $(f_n)$ satisfying 
$$
f_n \;\ge\; \mathbb{E}(f_m|\mathcal{F}_n) 
$$
for each $n\le m$.

A **backward martingale** or **inverse martingale** can be seen as a martingale in reverse time. 
Explicitly, given a [[probability space]] $(X,\mathcal{A},p)$ with a *decreasing* [[filtration]] $(\mathcal{F}_n)$ of [[sigma-algebras]] (i.e. $\mathcal{F}_n\supseteq\mathcal{F}_m$ for $n\le m$), a backward martingale is an adapted process $(f_n)$ satisfying
$$
f_m \;=\; \mathbb{E}(f_n|\mathcal{F}_m) 
$$
for each $n\le m$.



## Properties

(...)


## See also

* [[probability theory]], [[categorical probability]]

* [[random variable]], [[expectation value]], [[conditional expectation]]

* [[stochastic process]], [[random walk]], [[white noise]]

* [[martingale convergence theorem]]

* [[probability monad]], [[mixture]], [[empirical mean]]


## References

* {#vb_martingales} Ruben Van Belle, _A categorical treatment of the Radon-Nikodym theorem and martingales_, 2023. ([arXiv](https://arxiv.org/abs/2305.03421))

* {#dagger_martingales} [[Paolo Perrone]] and Ruben Van Belle, _Convergence of martingales via enriched dagger categories_, 2024. ([arXiv](https://arxiv.org/abs/2404.15191))

### Introductory material

* [[Paolo Perrone]], _Convergence of martingales via enriched dagger categories_, video talk, 2024. ([YouTube](https://www.youtube.com/watch?v=awr4RBrhh1g))


category: probability


[[!redirects martingales]]
[[!redirects Martingale]]
[[!redirects Martingales]]