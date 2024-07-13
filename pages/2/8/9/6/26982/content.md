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

*Zero-one measures* are [[measures]] whose only values are [[zero]] and [[one]]. 

In [[probability theory]], they model situations which "are not really random", where we are almost surely certain of which events take place and which do not. 
They are used in [[categorical probability]] to model situations of [[ergodicity]].

They also form a [[monad]], which is analogous to [[sober topological space|sobrification of topological spaces]].

The analogous concept for [[Markov kernels]] is a [[zero-one kernel]].


## Definition

A [[probability measure]] $p$ on a [[measurable space]] $X$ is said to be **zero-one**, **irreducible** or **extremal** if and only if any of the following equivalent conditions hold:

* For every event (measurable subset) $A$ of $X$, 
$$
p(A) \;=\; 0 \qquad or \qquad p(A) \;=\; 1 .
$$
* Every event (measurable subset) $A$ of $X$ is [[conditional independence|independent]] of itself:
$$
p(A) \;=\; p(A\cap A) \;=\; p(A)\,p(A) .
$$
* $p$ cannot be expressed as a nontrivial [[convex combination]] of other probability measures: if
$$
p \;=\; \lambda\,q_1 + (1-\lambda)\,q_2
$$
for $\lambda\in(0,1)$ and $q_1,q_2\in P X$, then $q_1=q_2=q$.
(This can be seen as analogous to [[irreducible closed sets]].)
* For every $f,g:X\to\mathbb{R}$ for which the integrals below exist, integration with $p$ preserves multiplication:
$$
\int_X f\cdot g\,dp \;=\; \left( \int_X f\,dp \right) \cdot \left( \int_X g\,dp \right) .
$$


## Examples

* Every [[Dirac measure|Dirac delta]] measure is zero-one: 
$$
\delta_x(A) \;=\; 1_A(x) \;=\; \begin{cases}
1 & x\in A ; \\
0 & x\notin A .
\end{cases}
$$
If $X$ is [[standard Borel]], or more more generally a [[sober measurable space]], every zero-one measure on $X$ is a Dirac delta.

* Every [[ergodic measure]] is zero-one when restricted to the [[invariant sigma-algebra]]. 


## Further properties

* Zero-one measures are exactly the [[law of a random variable|laws]] of those [[random variables]] which satisfy a [[zero-one law]].

* Zero-one kernels are exactly the [[Markov category#deterministic_morphisms|deterministic states]] of [[Stoch]], in the sense of [[Markov categories]].


## The monad of zero-one measures

(...)


## Related entries

* [[zero-one kernel]]
* [[Markov kernel]], [[Markov category]], [[Stoch]], [[Krn]]
* [[zero-one law]], [[ergodicity]], [[deterministic random variable]]
* [[thunk-force category]]
* [[sober measurable space]]
* [[point-free topology]], [[point of a locale]]


## References

* [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_. Adv. Math., 370:107239, 2020. [arXiv:1908.07021](https://arxiv.org/abs/1908.07021).

* {#det_submonad} Sean Moss, [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))

* {#markov_ergodic} Sean Moss, [[Paolo Perrone]], _A category-theoretic proof of the ergodic decomposition theorem_, Ergodic Theory and Dynamical Systems, 2023. ([arXiv:2207.07353](https://arxiv.org/abs/2207.07353))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)

* [[Paolo Perrone]], _When measurable spaces don't have enough points_, introductory talk. ([YouTube](https://www.youtube.com/watch?v=V4WzTgjbP3c))


category: probability


[[!redirects zero-one measure]]
[[!redirects zero-one measures]]
[[!redirects deterministic measure]]
[[!redirects deterministic measures]]
[[!redirects irreducible measure]]
[[!redirects irreducible measures]]