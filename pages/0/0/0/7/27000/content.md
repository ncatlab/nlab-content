+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In [[probability theory]], a *tail event* is an event which, intuitively, does not depend on the initial terms of a sequence. 
(For example, think of the truth value of the statement "The sequence $(x_n)$ has a limit": it does not depend on the first terms, but only on the "tail" of the sequence.)

Sometimes, in fields such as [[economics]], *tail event* refers to the mostly unrelated notion of *rare event*. (Think of a point very far right or very far left of a [[Gaussian distribution]], i.e. on the "tail".)


## Definition

Let $(X,\mathcal{A})$ be a [[measurable space]]. Consider the countably infinite product $X^\mathbb{N}$, and recall that the product sigma-algebra is given by
$$
\sigma \left( \bigcup_{i\in\mathbb{N}} \pi_i^{-1}(\mathcal{A}) \right) ,
$$
where $\pi_i:X^\mathbb{N}\to X$ is the $i$-th product projection.

The **tail sigma-algebra** on $X^\mathbb{N}$ is the sub-sigma-algebra of the product one, given by 
$$
\bigcap_{n\in\mathbb{N}} \sigma \left( \bigcup_{i=0}^n \pi_n^{-1}(\mathcal{A}) \right) .
$$

Similarly, if we have a sequence of [[random variables]] $f_n:\Omega\to X$, the **tail sigma-algebra** on $\Omega$ is the one induced by the tail sigma-algebra on $X^\mathbb{N}$ via the map $(f_n):\Omega\to X^\mathbb{N}$.

An event (measurable subset) of the tail sigma-algebra is called a **tail event**.

(Similar definitions can be given for other cardinalities than $\mathbb{N}$.)


## Properties

* Every [[shift]]-[[invariant event]] is a tail event. 
* The converse is not true. For example, consider a sequence $(x_n)\in X^\mathbb{N}$ where the $x_n$ are distinct. The event of "having the same tail as $(x_n)$", i.e. the set
$$
\{ (y_n) \,:\, \exists N, \forall n\ge N, y_n = x_n \} \;\subseteq\; X^\mathbb{N}
$$
is a tail event, but is not shift-invariant (if the $x_n$ are distinct).

* The [[Kolmogorov zero-one law]] says that for [[iid random variables]], every tail event has [[zero-one measure|probability zero or one]].


## See also

* [[probability theory]], [[categorical probability]]
* [[zero-one law]], [[exchangeability]]
* [[ergodicity]], [[invariant measure]], [[invariant set]], [[ergodic decomposition theorem]]
* [[law of large numbers]], [[ergodic theorem]]


## References

* {#fritzrischel} [[Tobias Fritz]] and Eigil Fjeldgren Rischel, _Infinite products and zero-one laws in categorical probability_, Compositionality 2(3) 2020. ([arXiv:1912.02769](http://arxiv.org/abs/1912.02769))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)




category: probability


[[!redirects tail events]]
[[!redirects tail subset]]
[[!redirects tail subsets]]
[[!redirects tail random variable]]
[[!redirects tail random variables]]
[[!redirects tail sigma-algebra]]
[[!redirects tail sigma-algebras]]
[[!redirects tail sigma algebra]]
[[!redirects tail sigma algebras]]
[[!redirects tail σ-algebra]]
[[!redirects tail σ-algebras]]