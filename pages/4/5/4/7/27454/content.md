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

(...)

## Definition

A finite-state [[stationary Markov chain]] on $X$ with [[stationary measure]] $p$ and [[transition matrix]] $k$ is said to satisfy **detailed balance** if and only if 
$$
p(x)\,k(y|x) \;=\; p(y)\,k(x|y) .
$$
Equivalently, if for each $x,y\in X$, the probability of the following two-state trajectories are equal:
$$
P(x,y) \;=\; P(y,x) .
$$

More generally, given a [[measure-preserving Markov kernel]] $k:(X,p)\to(X,p)$, we say that the resulting process satisfies **detailed balance** if and only if for all [[measurable subsets]] $A$ and $B$ of $X$, 
$$
\int_A k(B|x)\,p(d x) \;=\; \int_B k(A|x)\,p(d x) .
$$
In other words, $k$ is its own [[Bayesian inverse]].


## Properties

* A Markov process satisfies detailed balance if and only if it is [[time-reversible stochastic process|time-reversible]].


## Examples


(...)

## Related entries

* [[probability theory]], [[categorical probability]]
* [[invariant measure]], [[invariant set]]
* [[equilibrium]], [[ergodicity]], 
* [[Markov process]], [[Markov kernel]], [[Markov category]]
* [[time-reversal symmetry]], [[time-reversible stochastic process]]


## References

* Wikipedia, _[Ergodic process](http://en.wikipedia.org/wiki/Time_reversibility)_

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)


category: probability


[[!redirects time-reversible stochastic processes]]
[[!redirects time reversible stochastic process]]
[[!redirects time reversible stochastic processes]]
[[!redirects time-reversible process]]
[[!redirects time-reversible processes]]
[[!redirects time reversible process]]
[[!redirects time reversible processes]]