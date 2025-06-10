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

*Zero-one kernels* are [[Markov kernels]] whose only values are [[zero]] and [[one]]. 

In [[probability theory]], they model situations which "are not really random", where we are almost surely certain of which transitions take place and which do not.

They are the [[Markov kernel|kernel]] version of a [[zero-one measure]]. 

Zero-one kernels form a [[category]], which is used in [[categorical probability]] to model situations of determinism in a [[point-free topology|point-free]] way.


## Definition

A [[Markov kernel]] $k:X\to Y$ is said to be **zero-one** if and only if for every $x\in X$ and every measurable subset $B$ of $Y$, 
$$
k(B|x) \;=\; 0 \qquad or \qquad k(B|x) \;=\; 1 .
$$


## Examples

* Every [[Dirac measure|Dirac delta]] measure is a zero-one kernel from the one-point spae: 
$$
\delta_x(A) \;=\; 1_A(x) \;=\; \begin{cases}
1 & x\in A ; \\
0 & x\notin A .
\end{cases}
$$
If $X$ is [[standard Borel]], or more more generally [[sober measurable space|if it has enough points]], every zero-one measure on $X$ is a Dirac delta.

* More generally, every [[Markov kernel#kernels_from_deterministic_functions|kernel induced by a function]] is zero-one:
$$
\delta_f(A|x) \;=\; 1_A(f(x)) \;=\; \begin{cases}
1 & f(x)\in A ; \\
0 & f(x)\notin A .
\end{cases}
$$
Once again, if $Y$ is [[sober measurable space|sober]], every zero-one Markov kernel $X\to Y$ is in this form.

(See also at [[zero-one measure#examples|zero-one measure]].)


## The category of zero-one kernels

Zero-one Markov kernels are closed under composition, and hence they form a [[subcategory]] of [[Stoch]], sometimes denoted by $Stoch_det$.

This category is useful in [[categorical probability]] since it provides a [[point-free topology|point-free]] point of view on some probabilistic concepts.
Given [[measurable spaces]] $X$ and $Y$, denote their [[sigma-algebras]] by $\Sigma_X$ and $\Sigma_Y$. A zero-one kernel $k:X\to Y$ induces an assignment $k^*:\Sigma_Y\to\Sigma_X$ via 
$$
k^*B \;\coloneqq\; \{x\in X \,:\, k(B|x) = 1 \} .
$$ 
The map $k^*:\Sigma_Y\to\Sigma_X$ is a morphism of [[sigma-algebras]] (i.e. it preserves countable unions and complements), and every morphism of sigma-algebras $\Sigma_Y\to\Sigma_X$ is in this form for some kernel $k$. In other words, zero-one kernels are analogous to morphisms of [[locales]] in [[point-free topology]].

In particular, similar to the case of [[sober topological spaces]], $Stoch_det$ is equivalent to the category of [[sober measurable spaces]].
Equivalently, it can also be seen as the [[Kleisli category]] of the [[zero-one measure#the_monad_of_zeroone_measures|zero-one measure monad]] (equivalently, the [[sober measurable space|sobrification monad of measurable spaces]]).


## Almost surely zero-one kernels

Given [[probability spaces]] $(X,p)$ and $(Y,q)$, a [[Markov kernel#measurepreserving_kernels|measure-preserving kernel]] $k:(X,p)\to(Y,q)$ is **[[almost surely]] zero-one** if for every measurable subset $B\subseteq Y$, 
$$
k(B|x) \;=\; 0 \qquad or \qquad k(B|x) \;=\; 1
$$
for $p$-almost sure all $X$. 
Almost surely zero-one kernels are closed under composition, and so are their almost sure equivalence classes.


## Further properties

* Zero-one kernels are exactly the [[Markov category#deterministic_morphisms|deterministic morphisms]] of [[Stoch]], in the sense of [[Markov categories]].

* Zero-one kernels are exactly the [[thunk-force category#thunkable_morphisms|thunkable morphisms]] of [[Stoch]], seen as the [[Kleisli category]] of the [[Giry monad]] with its canonical [[thunk-force category|thunk-force structure]].

* Almost surely zero-one kernels are exactly the [[dagger epimorphisms]] (or *coisometries*) of [[Krn]].

* The [[invariant sigma-algebra]] is a [[colimit]] over an [[action]] in the category of zero-one kernels (and also in [[Stoch|the one of all kernels]]).


## Related entries

* [[zero-one measure]]
* [[Markov kernel]], [[Markov category]], [[Stoch]], [[Krn]]
* [[thunk-force category]]
* [[sober measurable space]], [[Loomis-Sikorski duality]]
* [[point-free topology]], [[point of a locale]]


## References

* [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_. Adv. Math., 370:107239, 2020. [arXiv:1908.07021](https://arxiv.org/abs/1908.07021).

* {#det_submonad} Sean Moss, [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))

* {#markov_ergodic} Sean Moss, [[Paolo Perrone]], _A category-theoretic proof of the ergodic decomposition theorem_, Ergodic Theory and Dynamical Systems, 2023. ([arXiv:2207.07353](https://arxiv.org/abs/2207.07353))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)

### Introductory material

* [[Paolo Perrone]], _When measurable spaces don't have enough points_, introductory talk. ([YouTube](https://www.youtube.com/watch?v=V4WzTgjbP3c))


category: probability

[[!redirects zero-one kernels]]
[[!redirects zero-one Markov kernel]]
[[!redirects zero-one Markov kernels]]
[[!redirects deterministic kernel]]
[[!redirects deterministic Markov kernel]]
[[!redirects deterministic kernels]]
[[!redirects deterministic Markov kernels]]