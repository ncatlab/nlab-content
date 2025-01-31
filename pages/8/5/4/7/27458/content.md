+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
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

A [[stochastic process]] is called *stationary* if the probability of each trajectory is invariant under (rigid) [[time translation]]. 

It is a way to encode mathematically a system which might exhibit [[randomness]] as well as [[memory]], but which does not explicitly depend on time. 


## Definition

A [[stochastic process]] $(X_t)_{t\in T}$ (for $T=\mathbb{N},\mathbb{R}$, etc.) is called **stationary** if and only if for every finite [[joint and marginal distributions|marginal]] $(X_{t_1},\dots,X_{t_n})$ and each $s\in T$, the tuples 
$$
(X_{t_1},\dots,X_{t_n}) \qquad and \qquad (X_{t_1+s},\dots,X_{t_n+s})
$$
have the same [[joint distribution]]. 

Note that this condition is stronger than requiring that the distributions of the single $X_t$ are time-invariant: *also the correlations*, of any order, are time-invariant, as long as all the times are translated "rigidly", by the same amount $s$. 

Equivalently, it is stationary if the complete [[joint distribution]] on $X^T$ is [[shift-invariant]], i.e. it is a [[measure-preserving dynamical system]]. 


## Examples

* A [[Markov chain]] is stationary if and only if its [[transition kernel]] is a time-independent [[measure-preserving Markov kernel]].
* [[white noise|White noise]] is a continuous-time stationary process.
* Every [[exchangeable process]] is stationary, in particular, [[Bernoulli processes]].
* Every [[ergodic process]] is stationary.
* Every [[time-reversible process]] is stationary.


## Related entries

* [[probability theory]], [[categorical probability]]
* [[invariant measure]], [[invariant set]], [[equilibrium]]
* [[ergodic decomposition theorem]], [[ergodic theorem]]
* [[de Finetti's theorem]], [[zero-one law]]
* [[Markov process]], [[Markov kernel]], [[Markov category]]
* [[shifts]], [[Bernoulli process]]


## References

* Wikipedia, [Stationary process](https://en.wikipedia.org/wiki/Stationary_process)

category: probability

[[!redirects stationary stochastic processes]]
[[!redirects stationary measure]]
[[!redirects stationary measures]]
[[!redirects stationary system]]
[[!redirects stationary systems]]
[[!redirects stationary state]]
[[!redirects stationary states]]
[[!redirects stationary process]]
[[!redirects stationary processes]]