+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _sampling map_ is an assignment that takes a [[probability distribution]] $p$ on a space $X$, and returns a random sample from $X$ distributed according to $p$.

It is a mathematical abstraction of the idea of flipping a coin, or of rolling a die (which are fair, or for which we know the bias): the outcome is random, but we know exactly the distribution it follows.


## In measure-theoretic probability

Let $X$ be a [[measurable space]]. Denote by $P X$ the set of [[probability measures]] over $X$. The **sampling map** is the [[Markov kernel]] $samp:P X\to X$ defined for every $p\in P X$ and every measurable $A\subseteq X$ by
$$
samp(A|p) \;\coloneqq\; p(A) .
$$

We can interpret this kernel as of "taking a sample from the distribution $p$".


### Example

Given a number $b\in[0,1]$, a **Bernoulli random variable** with bias $b$, denoted by $Bern(b)$, is a [[random variable]] which is $1$ with probability $b$, and $0$ with probability $1-b$. (Intuitively, we are "flipping a coin with bias $b$".)

We can view the set $[0,1]$ as parametrizing all the possible probability distributions on $\{0,1\}$, i.e. $[0,1]\cong P\{0,1\}$. Therefore, the assignment $Bern$ induces a Markov kernel $P\{0,1\}\to\{0,1\}$, which is exactly the sampling map given above. 


### In terms of the Giry monad

The sampling map is the [[counit]] of the [[adjunction]] induced by the [[Giry monad]] between the [[Stoch|category of Markov kernels]] and the [[Meas|category of measurable spaces]]. 

As the counit of an adjunction, it satisfies the following [[universal property]]: every Markov kernel $X\to Y$ can be written as a composition $X\to P Y\to Y$, where the map $X\to P Y$ is deterministic (it is the [[Markov kernel#kernels_from_deterministic_functions|kernel induced by a measurable function]]), and the map $P Y\to Y$ is the sampling map.

A probabilistic interpretation of this universal property is that sampling *generates* all the randomness. In other words, a process is *random* if and only if, at some point, it involves *sampling*, for example flipping a coin, or something analogous.

This is particularly important in probabilistic programming (see below).


## In Markov categories

(For now, see [[Markov category#representable_markov_categories|representable Markov category]].)


## In computer science

### In terms of thunk-force categories

As the counit of a Kleisli adjunction, the sampling map can be interpreted as the *forcing map* of a [[thunk-force category]].

One can view a probability distribution as a *thunk*, from which one can sample (or *force*) at a later time (for example, in lazy programming languages). 

Part of the correspondence between the Markov category formalism and the thunk-force formalism is studied in [Moss-Perrone'22](#det_submonad). 


### In probabilistic programming

In [[probabilistic programming]], the sampling map is the function, usually denoted by _samp_, _sample_, or sometimes _random_, which returns a (pseudo)random sample from a specified distribution. (Often, the uniform distribution on the unit interval, or an approximation thereof.)

The sampling map, by its universal property, can be seen as "generating" the randomness of probabilistic computations. For this reason, categorical probability can be interpreted as a form of probabilistic programming [[semantics]]. 
(Another central aspect of categorical probability and of probabilistic programming, besides sampling, is [[conditional probability|conditioning]].)


## See also

* [[Giry monad]], [[probability monad]], [[monad in computer science]], [[observational monad]]
* [[Markov category]], [[thunk-force category]], [[Kleisli category]]
* [[Markov kernel]], [[iid samples]]


## References

* {#fritz_representable} [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], Eigil Fjeldgren Rischel, _Representable Markov categories and comparison of statistical experiments in categorical probability_, Theoretical Computer Science 961, 2023. ([arXiv:2010.07416](https://arxiv.org/abs/2010.07416))

* {#det_submonad} Sean Moss, [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))


category: probability


[[!redirects samp]]
[[!redirects sample]]
[[!redirects sampling]]