
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The *category of couplings*, sometimes denoted *Krn* or *ProbStoch*, is a [[category]] of [[probability spaces]] and [[transport plans]] between them. 

This category is naturally a [[dagger category]], as transport plans can be interpreted as going in either direction. (One can see that as an instance of [[Bayesian inversion]].)

This category is used in [[categorical probability]] to model, abstractly, properties which only hold *almost surely*, i.e. only up to an event of zero probability (zero measure).


## Construction

There are two equivalent definitions of the category of couplings, either in terms of [[coupling (probability)|couplings]], or in terms of [[equivalence classes]] of [[Markov kernels]].

### In terms of couplings

The [[category]] **Krn** has 

* As [[objects]], [[standard Borel]] [[probability spaces]], i.e. [[triples]] $(X,\mathcal{A},p)$ where $X$ is a [[set]] $\mathcal{A}$ is a [[sigma-algebra]] on $X$ making $(X,\mathcal{A})$ a [[standard Borel space]], and $p$ is a [[probability measure]] on $(X,\mathcal{A})$;

* as [[morphisms]], [[coupling (probability)|couplings]] between probability spaces. 

The identity and composition couplings are described [[transport plan#main_constructions|here]].


### In terms of Markov kernels

The [[category]] **Krn** has 

* As [[objects]], [[standard Borel]] [[probability spaces]] (see above);

* as [[morphisms]], [[equivalence classes]] of [[Markov kernel#measurepreserving_kernels|measure-preserving Markov kernels]] under [[Markov kernel#almost_sure_equality|almost sure equality]].

The [[identity morphisms|identity]] and [[composition]] are constructed as in [[Stoch]].


### Equivalence of the definitions

Given a [[Markov kernel#measurepreserving_kernels|measure-preserving Markov kernel]] $k:(X,\mathcal{A},p)\to(Y,\mathcal{B},q)$, one can define a coupling canonically as follows,
$$
r_k(A\times B) = \int_A k(B|x)\,p(dx) 
$$
for all $A\in\mathcal{A}$ and $B\in\mathcal{B}$.
(See also [[transport plan#couplings_induced_by_kernels|here]].) 

Conversely, whenever $(X,\mathcal{A},p)$ and $(Y,\mathcal{A},q)$ are [[standard Borel]], given a coupling $r$ on $(X\times Y,\mathcal{A}\otimes\mathcal{B})$ one can form the [[Markov kernel#regular_conditionals_from_a_joint_distribution|regular conditional distribution]] $r':(X,\mathcal{A},p)\to(Y,\mathcal{A},q)$, which is a measure-preserving kernel, defined up to [[Markov kernel#almost_sure_equality|almost sure equality]]. 

As one can check, these two assignment are mutually inverse, so that the two definitions of *Krn* give [[isomorphic categories]].


## Basic structures and properties

### Dagger structure

(...)

## Generalizations and extensions

### For non-standard-Borel measurable spaces

(...)

### For abstract Markov categories

(...)


## References

The category *Krn* was originally defined in

* Fredrik Dahlqvist, Vincent Danos, Ilias Garnier, and Alexandra Silva, _Borel kernels and
their approximation, categorically_. In MFPS 34: Proceedings of the Thirty-Fourth Conference on the Mathematical Foundations of Programming Semantics, volume 341, 91–119, 2018.  [arXiv](https://arxiv.org/abs/1803.02651).

It also appears in the following works:

* [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_. Adv. Math., 370:107239, 2020. [arXiv:1908.07021](https://arxiv.org/abs/1908.07021).

* Noé Ensarguet, [[Paolo Perrone]], _Categorical probability spaces, ergodic decompositions, and transitions to equilibrium_.  [arXiv](https://arxiv.org/abs/2310.04267).

* Dexter Kozen, Alexandra Silva, Erik Voogd, _Joint Distributions in Probabilistic Semantics_, MFPS 2023. ([arXiv](https://arxiv.org/abs/2309.06913))


## Related concepts

* [[Markov kernel]]
* [[coupling (probability)]]
* [[dagger category]]
* [[Stoch]]
* [[categorical probability]]


category: category


[[!redirects Krn]]
[[!redirects ProbStoch]]
[[!redirects categories of couplings]]