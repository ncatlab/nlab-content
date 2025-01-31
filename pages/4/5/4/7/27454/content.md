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

*Detailed balance* is a strong form of [[equilibrium]] for [[Markov processes]] and [[dynamical systems]], stronger than [[stationary process|stationarity]] and independent from [[ergodicity]]. 

It can be roughly interpreted as a situation where for every two regions (of the state space, etc.) $A$ and $B$, the amount of mass (or probability, etc.) flowing from $A$ to $B$ equals the amount of mass flowing from $B$ to $A$. 


## Definition

### For discrete Markov chains

A finite-state [[stationary Markov chain]] on $X$ with [[stationary measure]] $p$ and [[transition matrix]] $k$ is said to satisfy **detailed balance** if and only if 
$$
p(x)\,k(y|x) \;=\; p(y)\,k(x|y) .
$$
Equivalently, if for each $x,y\in X$, the probability of the following two-state trajectories are equal:
$$
P(x,y) \;=\; P(y,x) .
$$

Note that this is strictly stronger than [[stationary process|stationarity]]. For example, consider a cyclic permutation $k$ on the set $\{a,b,c,d\}$ given by $a\mapsto b, b\mapsto c$, etc. This admits the uniform measure as stationary measure (call it $p$), however we have that 
$$
p(a)\cdot k(b|a) \;=\; \frac{1}{4} \cdot 1 \;=\; \frac{1}{4}
$$
and 
$$
p(b)\cdot k(a|b) \;=\; \frac{1}{4} \cdot 0 \;=\; 0 .
$$
Indeed, the "mass" flows in the direction $a\to b$, but not $b\to a$ (at least, not in a single step).
Still, the system is stationary: the amount of mass that leaves $a$ (and goes to $b$) is equal to the amount of mass that enters $a$. It just does not come from $b$.


### General case

More generally, given a [[measure-preserving Markov kernel]] $k:(X,p)\to(X,p)$, we say that the resulting process satisfies **detailed balance** if and only if for all [[measurable subsets]] $A$ and $B$ of $X$, 
$$
\int_A k(B|x)\,p(d x) \;=\; \int_B k(A|x)\,p(d x) .
$$
In other words, $k$ is its own [[Bayesian inverse]].

The same definition can be given for a class ("semigroup") of measure-preserving Markov kernels indexed by an arbitrary [[monoid]].

## Properties

* A Markov process satisfies detailed balance if and only if it is [[time-reversible stochastic process|time-reversible]].


## Examples

* Every [[idempotent Markov chain]] satisfies detailed balance.

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


[[!redirects time-reversible Markov process]]
[[!redirects time-reversible Markov processes]]
