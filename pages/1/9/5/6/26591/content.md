+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

One of the main tenets of [[probability theory]] is that in general [[stochastic dependence and independence|the probability of the product is not the product of the probabilities]], because of [[correlation]] and other [[statistical interactions]]. 
In particular, the probability of an [[infinite tensor product|infinite product]] is not the infinite product of the probabilities.

However, an infinite product is a [[cofiltered limit]] of finite products, and under some conditions, *the probability of an infinite product is the limit of the probability of the finite products*. 
One can interpret this fact as the absence of "infinitary correlations".

Statements of this kind are known collectively as the **Kolmogorov extension theorem**.
They are particularly important in the theory of [[stochastic processes]], since a stochastic process can be seen as a [[joint distribution]] over an [[infinite tensor product|infinite product]].


## In measure-theoretic probability

### Classical statement

(...)

### In terms of the Giry monad

(...)

### In the category of Markov kernels

(...)


## In Markov categories

In [[Markov categories]] the Kolmogorov extension theorem appears in the form of an [[axiom]] that the category can satisfy, an abstraction of the universal property in the [[category of Markov kernels]] given above.

\begin{definition}
Let $C$ be a Markov category, and let $(X_j)_{j\in J}$ be a family of objects. A **Kolmogorov product** of them is an [[infinite tensor product]] 
$$
X_J=\bigotimes_{j\in J} X_j
$$
such that all finite projections (marginalizations) $X_J\to X_F$, with $F\subseteq J$ finite, are deterministic morphisms.
\end{definition}

The category [[BorelStoch]], for example, has all countable Kolmogorov products. (The uncountable product of [[standard Borel spaces]], in general, is not standard Borel.)

See [[Markov category#kolmogorov_products|Markov category - Kolmogorov products]] for more on this, as well as [Fritz-Rischel'20](#fritzrischel).



## See also 

* [[probability theory]], [[categorical probability]]
* [[filtered category]], [[filtered limit]]
* [[probability monad]], [[Giry monad]]
* [[Markov category]], [[infinitary tensor product]]
* [[joint and marginal distributions]]
* [[stochastic dependence and independence]]


## References


* {#fritzrischel} [[Tobias Fritz]] and Eigil Fjeldgren Rischel, _Infinite products and zero-one laws in categorical probability_, Compositionality 2(3) 2020. ([arXiv:1912.02769](http://arxiv.org/abs/1912.02769))

* {#vb_martingales} Ruben Van Belle, _A categorical treatment of the Radon-Nikodym theorem and martingales_, 2023. ([arXiv](https://arxiv.org/abs/2305.03421))

[[!redirects Kolmogorov's extension theorem]]