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

*Zero-one measures* and *zero-one kernels* are [[measures]] and [[Markov kernels]] whose only values are [[zero]] and [[one]]. 

In [[probability theory]], they model situations which "are not really random", where we are almost surely certain of which events or which transitions take place. 

Zero-one kernels form a [[category]], which is used in [[categorical probability]] to model situations of determinism in a [[point-free topology|point-free]] way, as well as [[ergodicity]].


## Definition

A [[measure]] $p$ on a [[measurable space]] $X$ is said to be **zero-one** if and only if for every measurable subset $A$ of $X$, 
$$
p(A) \;=\; 0 \qquad or \qquad p(A) \;=\; 1 .
$$
Similarly, a [[Markov kernel]] $k:X\to Y$ is said to be **zero-one** if and only if for every $x\in X$ and every measurable subset $B$ of $Y$, 
$$
k(B|x) \;=\; 0 \qquad or \qquad k(B|x) \;=\; 1 .
$$


Equivalently, a [[measure]] is said to be *zero-one* exactly when it it makes each event [[conditional independence|independent]] of itself:
$$
p(A) \;=\; p(A\cap A) \;=\; p(A)\,p(A) \quad\Rightarrow\quad p(A)\in\{0,1\} .
$$
This is reflected exactly by the formulation in terms of [[Markov category#deterministic_morphisms|Markov categories]] (see below).
Similarly, a *zero-one kernel* is exactly a kernel whose output is [[conditional independence|conditionally independent]] of itself given the input.


## Examples

* Every [[Dirac delta]] measure is zero-one: 
$$
\delta_x(A) \;=\; 1_A(x) \;=\; \begin{cases}
1 & x\in A ; \\
0 & x\notin A .
\end{cases}
$$
If $X$ is [[standard Borel]], or more more generally a [[sober measurable space]], every zero-one measure on $X$ is a Dirac delta.

* More generally, every [[Markov kernel#kernels_from_deterministic_functions|kernel induced by a function]] is zero-one:
$$
\delta_f(A|x) \;=\; 1_A(f(x)) \;=\; \begin{cases}
1 & f(x)\in A ; \\
0 & f(x)\notin A .
\end{cases}
$$
Once again, if $Y$ is [[sober measurable space|sober]], every zero-one Markov kernel $X\to Y$ is in this form.

* Every [[ergodic measure]] is zero-one when restricted to the [[invariant sigma-algebra]] (which in general does not separate points). 


## The category of zero-one kernels

Zero-one Markov kernels are closed under composition, and hence they form a [[subcategory]] of [[Stoch]], sometimes denoted by $Stoch_det$.

This category is useful in [[categorical probability]] since it provides a [[point-free topology|point-free]] point of view on some probabilistic concepts.
Given [[measurable spaces]] $X$ and $Y$, denote their [[sigma-algebras]] by $\Sigma_X$ and $\Sigma_Y$. A zero-one kernel $k:X\to Y$ induces an assignment $k^*:\Sigma_Y\to\Sigma_X$ via 
$$
k^*B \;\coloneqq\; \{x\in X \,:\, k(B|x) = 1 \} .
$$ 
The map $k^*:\Sigma_Y\to\Sigma_X$ is a morphism of [[sigma-algebras]] (i.e. it preserves countable unions and complements), and every morphism of sigma-algebras $\Sigma_Y\to\Sigma_X$ is in this form for some kernel $k$. In other words, zero-one kernels are analogous to morphisms of [[locales]] in [[point-free topology]].


## Almost surely zero-one kernels

Given [[probability spaces]] $(X,p)$ and $(Y,q)$, a [[Markov kernel#measurepreserving_kernels|measure-preserving kernel]] $k:(X,p)\to(Y,q)$ is **[[almost surely]] zero-one** if for every measurable subset $B\subseteq Y$, 
$$
k(B|x) \;=\; 0 \qquad or \qquad k(B|x) \;=\; 1
$$
for $p$-almost sure all $X$. 
Almost surely zero-one kernels are closed under composition, and so are their almost sure equivalence classes.


## Further properties

* Zero-one measures are exactly the [[law of a random variable|laws]] of those [[random variables]] which satisfy a [[zero-one law]].

* Zero-one kernels are exactly the [[Markov category#deterministic_morphisms|deterministic morphisms]] of [[Stoch]], in the sense of [[Markov categories]].

* Zero-one kernels are exactly the [[thunk-force category#thunkable_morphisms|thunkable morphisms]] of [[Stoch]], seen as the [[Kleisli category]] of the [[Giry monad]] with its canonical [[thunk-force category|thunk-force structure]].

* Almost surely zero-one kernels are exactly the [[dagger epimorphisms]] (or *coisometries*) of [[Krn]].

* The [[invariant sigma-algebra]] is a [[colimit]] over an [[action]] in the category of zero-one kernels (and also in [[Stoch|the one of all kernels]]).


## Related entries

* [[Markov kernel]], [[Markov category]], [[Stoch]], [[Krn]]
* [[zero-one law]], [[ergodicity]]


## References

* [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_. Adv. Math., 370:107239, 2020. [arXiv:1908.07021](https://arxiv.org/abs/1908.07021).

* {#det_submonad} Sean Moss, [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))

* {#markov_ergodic} Sean Moss, [[Paolo Perrone]], _A category-theoretic proof of the ergodic decomposition theorem_, Ergodic Theory and Dynamical Systems, 2023. ([arXiv:2207.07353](https://arxiv.org/abs/2207.07353))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)

* [[Paolo Perrone]], _When measurable spaces don't have enough points_, introductory talk ([YouTube](https://www.youtube.com/watch?v=V4WzTgjbP3c))


category: probability

[[!redirects zero-one kernels]]
[[!redirects zero-one measure]]
[[!redirects zero-one measures]]
[[!redirects zero-one Markov kernel]]
[[!redirects zero-one Markov kernels]]
[[!redirects deterministic kernel]]
[[!redirects deterministic measure]]
[[!redirects deterministic Markov kernel]]
[[!redirects deterministic kernels]]
[[!redirects deterministic measures]]
[[!redirects deterministic Markov kernels]]