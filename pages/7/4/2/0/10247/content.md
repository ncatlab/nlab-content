+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
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

*Ergodicity* is an idea which originated from [[statistical physics]], and which spread to [[probability theory]], [[representation theory]] and [[dynamical systems]], forming the basis of the entire mathematical field of [[ergodic theory]].

An *ergodic state* can be interpreted as a situation where we have a strong form of [[equilibrium]], where all the populated states of the system are connected and accessible to each other. 

For example, one can imagine a drop of ink completely dissolved in a glass of water which one is stirring. It is at [[equilibrium]] (i.e. the ink is completely dissolved), and each molecule of ink can swap places with any other molecule of ink under stirring (i.e. the glass of water is not divided into mutually inaccessible regions, unlike for example *two* glasses).

Sometimes the term *ergodic system* denotes a system which is *not yet* at equilibrium, but such that *if it transitions to equilibrium, it will reach an ergodic state*.


## Main definitions

Let $X$ be a [[measurable space]]. 
Let $M$ be a [[monoid]] (for example a [[group]]) with an [[action]] on $X$ via [[measurable functions]] $m:X\to X$ or via [[Markov kernels]] $k_m:X\to X$.

An [[invariant probability measure]] $p$ on $X$ is called **ergodic** if and only if for each [[invariant set]] $A$, 
$$
p(A) \;=\; 0 \qquad or \qquad p(A) \;=\; 1.
$$
Equivalently, $p$ is a [[zero-one measure]] on the [[invariant sigma-algebra]].

A (measure-preserving) [[dynamical system]] is called **ergodic** if its [[stationary measure]] is ergodic.

Similarly, a (stationary) [[stochastic process]], for example a stationary [[Markov chain]], is called **ergodic** if its [[stationary measure]] is ergodic.

Sometimes, more generally, a dynamical system or a stochastic process are called **ergodic** if any of the following equivalent conditions hold:

* There is a unique [[invariant probability measure]];
* There is a unique ergodic measure;
* All [[invariant measures]] are ergodic, and there exists at least one.

## Equivalent descriptions

(...)


## Examples

(...)


## In terms of category theory

(...)


## Properties

* The [[ergodic decomposition theorem]] says that, in some cases, every [[invariant probability measure]] is a [[convex mixture]] of ergodic ones.
* The [[ergodic theorem]] says that, in some cases, [[empirical means]] of [[random variables]] on an ergodic process tend to [[expectation value|expectations]] (and on more general [[stationary systems]], they tend to [[conditional expectations]] w.r.t. the [[invariant sigma-algebra]]). 


## Related entries

* [[probability theory]], [[categorical probability]]
* [[invariant measure]], [[invariant set]], [[stationary process]]
* [[ergodic decomposition theorem]], [[ergodic theorem]]
* [[de Finetti's theorem]], [[zero-one law]]
* [[Markov process]], [[Markov kernel]], [[Markov category]]
* [[shifts]], [[Bernoulli process]]


## References

* Wikipedia, _[Ergodic process](http://en.wikipedia.org/wiki/Ergodic_process)_

* [[Terence Tao]], [What's new? Lecture 9: Ergodicity](https://terrytao.wordpress.com/2008/02/04/254a-lecture-9-ergodicity/), blog entry.

* {#markov_ergodic} Sean Moss, [[Paolo Perrone]], _A category-theoretic proof of the ergodic decomposition theorem_, Ergodic Theory and Dynamical Systems, 2023. ([arXiv:2207.07353](https://arxiv.org/abs/2207.07353))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)


category: probability


[[!redirects ergodic]]
[[!redirects ergodic system]]
[[!redirects ergodic systems]]
[[!redirects ergodic dynamical system]]
[[!redirects ergodic dynamical systems]]
[[!redirects ergodic process]]
[[!redirects ergodic processes]]
[[!redirects ergodic stochastic process]]
[[!redirects ergodic stochastic processes]]
[[!redirects ergodic measure]]
[[!redirects ergodic measures]]
[[!redirects ergodic probability measure]]
[[!redirects ergodic probability measures]]
[[!redirects ergodic state]]
[[!redirects ergodic states]]