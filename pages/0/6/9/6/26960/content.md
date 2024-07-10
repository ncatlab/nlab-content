+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[probability theory]], a (usually infinite) sequence is called *exchangeable*, or sometimes *symmetric*, if it is invariant under finite [[permutations]]. 
In particular:

* An *exchangeable probability measure* is a [[measure]] on a [[product]] space which is invariant under finite [[permutations]] of the coordinates;
* An *exchangeable event* is an [[event]] ([[measurable subset]]) of a product space which is invariant under finite permutations.

(See below for more details.)

Exchangeable random variables and events play a prominent role in [[de Finetti's theorem]] and in the [[Hewitt-Savage zero-one law]]. 


## Exchangeable measures and random variables

Let $X$ be a [[measurable space]], and consider the [[infinite product]] $X^{\mathbb{N}}$. 
A **finite permutation** is an isomorphism $\sigma:X^{\mathbb{N}}\to X^{\mathbb{N}}$ which is a permutation of finitely many components of $X^{\mathbb{N}}$. (Equivalently, it is induced by finitely many applications of the [[braiding]].)

A [[probability measure]] $p$ on $X^{\mathbb{N}}$ is called **exchangeable** or **symmetric** if and only if it is [[invariant measure|invariant]] under all finite permutations. 
In other words, if for all finite permutations $\sigma:X^{\mathbb{N}}\to X^{\mathbb{N}}$, the [[pushforward measure]] $\sigma_*p$ is equal to $p$. Even more explicitly, for every [[measurable subset]] $A$ of $X^{\mathbb{N}}$, we have 
$$
p(\sigma^{-1}(A)) \;=\; p(A) .
$$

(Note that such a probability measure is often specified by its finite [[marginals]], by the [[Kolmogorov extension theorem]].)

A sequence of [[random variables]] or [[random elements]] $f_n:\Omega\to X$ on a [[probability space]] $(\Omega,\mu)$ is said to be **exchangeable**, or to form an **exchangeable process**, if the resulting [[joint distribution]] on $X^{\mathbb{N}}$ is an exchangeable measure. 

Similar definitions can be given for a finite product $X^n$. 


### In categorical probability

In a [[Markov category]], and more generally in any [[symmetric monoidal category]], one can similarly define an **exchangeable state** to be a morphism $I\to X^\mathbb{N}$ from the [[monoidal unit]] to an [[infinite tensor product]] which is invariant under the action of the [[braiding]]. 

In other words, finite permutations form a [[group]] acting on $X^{\mathbb{N}}$, and exchangeable states form a [[cone]] over the resulting [[diagram]]. 
[[De Finetti's theorem]] can be interpreted as saying that the [[limit]] cone is given by a space of probability measure (such as given by [[probability monad]]). 


### Examples

* A sequence of [[iid random variables]] is exchangeable.

* Somewhat on the other extreme, perfectly [[correlated]] [[random variables]] are also exchangeable, but in general far from independent. Their joint distribution is in the form 
$$ p(A_1\times A_2\times\dots) \;=\; q(A_1\cap A_2\cap\dots) $$
for some distribution $q$ on $X$. 


## Exchangeable events and the exchangeable sigma-algebra

Similarly to measures, an [[event]] ([[measurable subset]]) $A$ of the infinite product $X^{\mathbb{N}}$ is called an **exchangeable** or **symmetric event** if for all finite permutations $\sigma:X^{\mathbb{N}}\to X^{\mathbb{N}}$,
$$
\sigma^{-1}(A) \;=\; A ,
$$
i.e. if it is [[invariant set|invariant]] under finite permutations.

The exchangeable events of $X^{\mathbb{N}}$ form a [[sigma-algebra]], called the **exchangeable sigma-algebra**. It is the [[invariant sigma-algebra]] for the [[group action|action]] of finite permutations on $X^{\mathbb{N}}$.

In some contexts one is, instead, interested in events which are invariant only [[almost surely]], that is, those events $A$ such that  for all finite permutations $\sigma$,
$$
p(A \setminus \sigma^{-1}(A)) \;=\; p(\sigma^{-1}(A)\setminus A) \;=\; 0 .
$$
These events are sometimes called **almost exchangeable**, **almost surely exchangeable**, or even just **exchangeable**.  
They also form a sigma-algebra, also often called the **exchangeable sigma-algebra**. 

In probability theory, very often, this ambiguity in terminology does not cause problems, since, at least for countably many random variables, it is customary to only look at processes up to almost sure equality. 


### In categorical probability

In [[categorical probability]], often the exchangeable sigma-algebra can be encoded as a [[colimit]] of the action of permutations.
(The same can be said about [[invariant sigma-algebras]] of more general actions.)

In [[Stoch]] and in [[Markov categories]], the sigma-algebra of strictly (not just almost surely) invariant sets can be seen as a colimit, both in the category of [[Markov kernels]] and of [[Meas|measurable functions]] ([Moss-Perrone'23](#markov_ergodic)). 

Similarly, in [[Krn]] and in [[categories of couplings]], the sigma-algebra of almost surely invariant sets can be seen as a colimit compatible with the [[dagger category|dagger structure]] ([Ensarguet-Perrone'23](#ergodic_dagger)). For [[standard Borel spaces]], one can, up to isomorphism, also consider strictly invariant sets.


## Properties

* [[De Finetti's theorem]] says that every exchangeable probability measure is a unique [[convex mixture]] of [[iid]] ones. 
* Another way of stating de Finetti's theorem is that an infinite sequence of exchangeable random variables are [[conditionally independent]] given the exchangeable sigma-algebra.

* The [[Hewitt-Savage zero-one law]] says that given [[iid random variables]], the probability of each exchangeable event is either zero or one, i.e. it is a [[zero-one measure]]. 


## See also 

* [[probability theory]], [[categorical probability]]
* [[de Finetti's theorem]], [[Hewitt-Savage zero-one law]]
* [[infinitary tensor product]], [[Kolmogorov extension theorem]]
* [[limit]], [[permutation]], 
* [[invariant measure]], [[invariant sigma-algebra]]
* [[iid random variables]]

* Wikipedia, [Exchangeable random variables](https://en.wikipedia.org/wiki/Exchangeable_random_variables)

## References

* {#definetti_limit} [[Bart Jacobs]], [[Sam Staton]], _De Finetti's construction as a categorical limit_, Proceedings of CMCS, 2021. ([arXiv:2003.01964](https://arxiv.org/abs/2003.01964))

* {#fritz_definetti} [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], _De Finetti's theorem in categorical probability_. Journal of Stochastic Analysis, 2021. ([arXiv:2105.02639](https://arxiv.org/abs/2105.02639))

* {#markov_ergodic} Sean Moss, [[Paolo Perrone]], _A category-theoretic proof of the ergodic decomposition theorem_, Ergodic Theory and Dynamical Systems, 2023. ([arXiv:2207.07353](https://arxiv.org/abs/2207.07353))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)


category: probability


[[!redirects exchangeable]]
[[!redirects exchangeable sequence]]
[[!redirects exchangeable random variables]]
[[!redirects exchangeable random elements]]
[[!redirects exchangeable process]]
[[!redirects exchangeable stochastic process]]
[[!redirects symmetric measure]]
[[!redirects exchangeable measure]]
[[!redirects exchangeable probability measure]]
[[!redirects symmetric event]]
[[!redirects exchangeable event]]
[[!redirects exchangeable events]]
[[!redirects exchangeable sigma-algebra]]