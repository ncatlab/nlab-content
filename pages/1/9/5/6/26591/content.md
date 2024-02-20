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

One of the main tenets of [[probability theory]] is that in general [[joint and marginal probability|the probability of the product is not the product of the probabilities]], because of [[correlation]] and other [[statistical interactions]]. 
In particular, the probability of an [[infinite tensor product|infinite product]] is not the infinite product of the probabilities.

However, an infinite product is a [[cofiltered limit]] of finite products, and under some conditions, *the probability of an infinite product is the limit of the probability of the finite products*. 
One can interpret this fact as the absence of "infinitary correlations".

Statements of this kind are known collectively as the **Kolmogorov extension theorem**.
They are particularly important in the theory of [[stochastic processes]], since a stochastic process can be seen as a [[joint distribution]] over an [[infinite tensor product|infinite product]].


## In measure-theoretic probability

We look at the classical statement, and then give two (related) ways to express it category-theoretically.


### Classical statement

The classical statement is about [[probability measures]], and roughly says that under some conditions, a probability measure on an [[infinitary tensor product|infinite product]] is uniquely determined by its finite [[marginal distribution|marginals]].

\begin{theorem}\label{kolmogorov}
Let $\{(X_j,\mathcal{A}_j)\}_{j\in J}$ be a collection of [[standard Borel spaces]], indexed by a set $J$ of arbitrary cardinality. 

* Denote by $(X_J,\mathcal{A}_J)$ the [[product]] of the $X_j$, equipped with the product [[sigma-algebra]].
* Similarly, for every finite set $F\subseteq J$, denote $(X_F,\mathcal{A}_F)$ the product of the $(X_j,\mathcal{A}_j)$ for $j\in F$.

There is a [[bijection]] between

* probability measures on $(X_J,\mathcal{A}_J)$

and 

* families of probability measures $p_F$ on $(X_F,\mathcal{A}_F)$ for each finite subset $F\subseteq J$ such that for every inclusion $F\subseteq G$, the measure $p_F$ is the [[marginal distribution|marginal]] of $p_G$.

In particular, the $p_F$ can be obtained as marginal distributions of the measure $p_J$. 

\end{theorem}

Note that

* The same result holds more in general if each $(X_j,\mathcal{A}_j)$ is a [[Hausdorff space]] equipped with its [[Borel sigma-algebra]], and the measures $p_F$ are [[inner regular measure|inner regular]].

* The uncountable product of standard Borel spaces may fail to be standard Borel.

* The [[Borel sigma-algebra]] of an uncountable product of topological spaces is not the product of the Borel sigma-algebras of the factors.


### In the category of Markov kernels

We can restate Kolmogorov's extension theorem as a *limit*, as follows.

Let $\{(X_j,\mathcal{A}_j)\}_{j\in J}$ be a collection of [[standard Borel spaces]], indexed by a set $J$ of arbitrary cardinality. 

* Denote by $(X_J,\mathcal{A}_J)$ the categorical [[product]] of the $X_j$ in the [[Meas|category Meas of measurable spaces and measurable maps]].
* Similarly, for every finite set $F\subseteq J$, denote $(X_F,\mathcal{A}_F)$ the product of the $(X_j,\mathcal{A}_j)$ for $j\in F$.

Note that, since infinite products are [[cofiltered limits]] of finite products, $(X_J,\mathcal{A}_J)$ is the limit in [[Meas]] of the diagram formed by the $(X_F,\mathcal{A}_F)$ and their projections.

Now:

\begin{corollary}\label{kolmogorov_kernels}
The object $(X_J,\mathcal{A}_J)$ is the limit of the $(X_F,\mathcal{A}_F)$ also in the [[Stoch|category Stoch of measurable spaces and Markov kernels]]. 
\end{corollary}

Note that this does not say that $(X_J,\mathcal{A}_J)$ is the product of the $(X_j,\mathcal{A}_j)$ ([[joint and marginal distributions|that would be false even in the finite case]]).
It is just the "[[cofiltered limit|finite to infinite]]" part which is retained in the category of kernels.

\begin{proof}
For finite sets $F\subseteq G\subseteq J$, denote by $\pi_{J,F}:(X_J,\mathcal{A}_J)\to(X_F,\mathcal{A}_F)$ and $\pi_{G,F}:(X_G,\mathcal{A}_H)\to(X_F,\mathcal{A}_F)$ the product projections. 
With a slight abuse, denote the [[Markov kernel#kernels_from_deterministic_functions|Markov kernel induced by the functions]] $\pi_{J,F}$ and $\pi_{G,F}$ again by $\pi_{J,F}$ and $\pi_{G,F}$.

Given a measurable space $(Y,\mathcal{B})$, we have to show that there is a bijection between [[Markov kernels]] $k_J:Y\to X_J$ and families of Markov kernels $k_F:Y\to X_F$ such that for each inclusion $F\subseteq G$, the outer triangle in the following diagram of [[Stoch]] commutes.
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
] 
& & & (X_G,\mathcal{A}_G) \ar{dd}{\pi_{G,F}} \\
(Y,\mathcal{B}) \ar{urrr}{k_G} \ar[dashed]{rr}[near end]{k_J} \ar{drrr}[swap]{k_F} && (X_J,\mathcal{A}_J) \ar{ur}[swap]{\pi_{J,G}} \ar{dr}{\pi_{J,F}} \\
& & & (X_F,\mathcal{A}_F)
\end{tikzcd}

Now for each $y\in Y$, the Markov kernels $k_J(-|y)$ and $k_F(-|y)$ are just [[probability measures]], so that Theorem \ref{kolmogorov} applies. We only need to show that $k_J$ is measurable in $y$ if and only if the $k_F$ are. Now if $k_J$ is measurable, so is $k_F$, since the composition of measurable functions is measurable. The converse is true as well, since measurability of Markov kernels can be equivalently tested on a [[pi-system]].
\end{proof}


### In terms of the Giry monad

The result in terms of [[Markov kernels]] can be restated in terms of the [[Giry monad]] as follows.

Once again, recall that $(X_J,\mathcal{A}_J)$ is the [[cofiltered limit]] in [[Meas]] of the diagram formed by the $(X_F,\mathcal{A}_F)$ and their projections.

Now, if the $X_j$ are [[standard Borel]]:

\begin{corollary}\label{kolmogorov_giry}
The Giry monad preserves this limit. 
\end{corollary}

\begin{proof}
We have to show that given a measurable space $Y$, there is a bijection between [[measurable functions]] $f_J:Y\to X_J$ and families of measurable functions $f_F:Y\to X_F$ such that for each inclusion $F\subseteq G$, the outer triangle in the following diagram of [[Meas]] commutes.
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
] 
& & & P(X_G) \ar{dd}{P\pi_{G,F}} \\
Y \ar{urrr}{f_G} \ar[dashed]{rr}[near end]{f_J} \ar{drrr}[swap]{f_F} && P(X_J) \ar{ur}[swap]{P\pi_{J,G}} \ar{dr}{P\pi_{J,F}} \\
& & & P(X_F)
\end{tikzcd}
Now since [[Stoch]] is the [[Kleisli category]] of the [[Giry monad]], notice that there is a bijection 
$$
Stoch(Y,X) \cong Meas(Y,PX)
$$
natural in $X$, so that the universal property that we want to prove is just a restatement of the proof of Corollary \ref{kolmogorov_kernels}.
\end{proof}



## In Markov categories

In [[Markov categories]] the Kolmogorov extension theorem appears in the form of an [[axiom]] that the category can satisfy, an abstraction of the universal property in the [[category of Markov kernels]] given above.

\begin{definition}
Let $C$ be a Markov category, and let $(X_j)_{j\in J}$ be a family of objects. A **Kolmogorov product** of them is an [[infinite tensor product]] 
$$
X_J=\bigotimes_{j\in J} X_j
$$
such that all finite projections (marginalizations) $X_J\to X_F$, with $F\subseteq J$ finite, are [[Markov category#deterministic_morphisms|deterministic morphisms]].
\end{definition}

The category [[BorelStoch]], for example, has all countable Kolmogorov products. (The uncountable product of [[standard Borel spaces]], in general, is not standard Borel.)

See [[Markov category#kolmogorov_products|Markov category - Kolmogorov products]] for more on this, as well as [Fritz-Rischel'20](#fritzrischel).



## See also 

* [[probability theory]], [[categorical probability]]
* [[filtered category]], [[filtered limit]]
* [[infinitary tensor product]]
* [[probability monad]], [[Giry monad]]
* [[Markov category]], [[infinitary tensor product]]
* [[joint and marginal distributions]]
* [[stochastic dependence and independence]]


## References


* {#fritzrischel} [[Tobias Fritz]] and Eigil Fjeldgren Rischel, _Infinite products and zero-one laws in categorical probability_, Compositionality 2(3) 2020. ([arXiv:1912.02769](http://arxiv.org/abs/1912.02769))

* {#vb_martingales} Ruben Van Belle, _A categorical treatment of the Radon-Nikodym theorem and martingales_, 2023. ([arXiv](https://arxiv.org/abs/2305.03421))


category: probability

[[!redirects Kolmogorov's extension theorem]]