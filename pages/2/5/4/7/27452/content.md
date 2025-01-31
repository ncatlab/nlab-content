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

A [[stochastic process]] is *time-reversible* if it is symmetric under [[time-reversal symmetry|time reversal]]. 

This symmetry is meant in a _stochastic_ sense: it says that *given any trajectory, its reverse trajectory has the same probability of happening*. 


## Definition

A [[stationary stochastic process]] $(X_t)_{t\in T}$ is called **time-reversible** if and only if for all finite $t_1 \lt \dots \lt t_n$, we have that the finite [[joint and marginal distribution|marginals]]
$$
(X_{t_1},\dots,X_{t_n}) \qquad and \qquad (X_{t_n},\dots,X_{t_1})
$$
have the same [[joint distribution]].

(The definition outside the stationary case does not seem to appear in the literature.)


## Examples

* A [[Markov process]] or [[Markov chain]] is time-reversible if and only if it satisfies [[detailed balance]]. In particular, every [[idempotent Markov chain]] is time-reversible.
* Every [[exchangeable process]] is time-reversible, in particular [[Bernoulli processes]] are.


## Related entries

* [[probability theory]], [[categorical probability]]
* [[invariant measure]], [[invariant set]]
* [[equilibrium]], [[detailed balance]]
* [[Markov process]], [[Markov kernel]], [[Markov category]]
* [[time-reversal symmetry]]


## References

* Wikipedia, _[Time reversibility](http://en.wikipedia.org/wiki/Time_reversibility)_

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)


category: probability


[[!redirects time-reversible stochastic processes]]
[[!redirects time reversible stochastic process]]
[[!redirects time reversible stochastic processes]]
[[!redirects time-reversible process]]
[[!redirects time-reversible processes]]
[[!redirects time reversible process]]
[[!redirects time reversible processes]]