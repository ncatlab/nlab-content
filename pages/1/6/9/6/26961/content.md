+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

In [[probability theory]], *iid* is shorthand for *independent and identically distributed*, and it's mostly used for [[random variables]].

The notion of such random variables formalizes the idea of repeated independent coin flips or dice rolls: they are [[stochastic independence|independent events]], and the [[probability]] of each event (for example, each single coin flip) follows the same distribution.

Another name for the same process is *Bernoulli process*.


## Definition

Let $X$ be a [[measurable space]]. 
[[random variable|Random variables]] or [[random elements]] in a [[sequence]] $f_n \colon \Omega\to X$ on a [[probability space]] $(\Omega,\mu)$ are said to be **iid**, or **independent and identically distributed**, if their [[joint distribution]] $p$ is in the form 
$q\otimes q\otimes\dots\otimes q$ for some measure $q$ on $X$. Equivalently, if for all [[measurable subsets]] $A_1,\dots,A_n$ of $X$, 
$$
  p(A_1\times\dots\times A_n) 
   \;=\; 
  q(A_1)\cdots q(A_n)
  \,.
$$

A similar definition can be given for [[infinite products]] as well, by means of the [[Kolmogorov extension theorem]].

Sometimes, especially when the space $X$ is [[finite set|finite]] (particularly when it has two elements, such as for coin flips), one calls the resulting [[stochastic process]] a **Bernoulli process**.


### iid samples

Given a probability distribution $p$ on $X$, one can take **iid samples**. This can be described as a [[Markov kernel]] $samp_\mathbb{N}:P X\to (P X)^\mathbb{N}\to X^\mathbb{N}$ where:

* The kernel $P X\to (P X)^\mathbb{N}$ is the [[Markov kernel#kernels_from_deterministic_functions|kernel induced by]] the function $p\mapsto (p,p,\dots)$;
* The kernel $(P X)^\mathbb{N}\to X^\mathbb{N}$ is induced by taking many tensor copies of the [[sampling map]]. (One can take infinitely many copies by means of the [[Kolmogorov extension theorem]].)

Explicitly, the kernel $samp_\mathbb{N}:P X\to X^\mathbb{N}$ is given as follows:
$$
samp_\mathbb{N}(A_1\times\dots\times A_n|p) \;=\; p(A_1)\cdots p(A_n) ,
$$
where again we make use of the [[Kolmogorov extension theorem]] to define the kernel in terms of its finite [[marginal distribution|marginals]].


One way of stating [[de Finetti's theorem]] is by saying that the map $samp_\mathbb{N}:P X\to X^\mathbb{N}$ is a [[limit]] cone over an [[exchangeable process]].


### In categorical probability

In [[categorical probability]], for example in [[Markov categories]], independence is simply encoded by taking the [[tensor product]] of [[morphisms]] (for example, from the [[monoidal unit]]). 

In Markov categories, one can model iid samples using the *copy map* (see at [[Markov category]]), together with [[Markov category#kolmogorov_products|Kolmogorov products]].


## Properties

* An iid process is always [[exchangeable]]. (The converse is not true.)

* [[De Finetti's theorem]] says that every [[exchangeable probability measure]] is a unique [[convex mixture]] of iid ones.
* The [[Hewitt-Savage zero-one law]] says that given iid random variables, the probability of each [[exchangeable event]] is either zero or one, i.e. it is a [[zero-one measure]]. 

* The [[Kolmogorov zero-one law]], similarly, says that given iid [[random variables]], the probability of each [[tail event]] is a [[zero-one measure]]. 

* The [[law of large numbers]] says that given integrable iid random variables, the [[empirical mean]] tends to the [[expectation value]].


## See also 

* [[probability theory]], [[categorical probability]]

* [[observational monad]], [[sampling map]]

* [[de Finetti's theorem]], [[Hewitt-Savage zero-one law]], [[Kolmogorov zero-one law]], [[law of large numbers]]

* [[infinitary tensor product]], [[Kolmogorov extension theorem]]

* [[Markov category]], [[sampling map]]

* [[ergodic system]], [[Bernoulli shifts]]


## References

See also:

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Independence_(probability_theory)">Independence (probability theory)</a>*

* ProofWiki: *[Definition:Independent Random Variables](https://proofwiki.org/wiki/Definition:Independent_Random_Variables)*

* ProofWiki: *[Condition for Independence from Product of Expectations](https://proofwiki.org/wiki/Condition_for_Independence_from_Product_of_Expectations)*

category: probability


[[!redirects iid]]
[[!redirects IID]]
[[!redirects IID random variables]]
[[!redirects iid random elements]]
[[!redirects IID random elements]]
[[!redirects iid measure]]
[[!redirects IID measure]]
[[!redirects iid measures]]
[[!redirects IID measures]]
[[!redirects iid sequence]]
[[!redirects IID sequence]]
[[!redirects iid process]]
[[!redirects IID process]]
[[!redirects independent and identically distributed random variables]]
[[!redirects independent and identically distributed random elements]]
[[!redirects independent and identically distributed sequence]]
[[!redirects independent and identically distributed process]]
[[!redirects iid samples]]
[[!redirects IID samples]]
[[!redirects independent and identically distributed samples]]
[[!redirects Bernoulli random variables]]
[[!redirects Bernoulli random elements]]
[[!redirects Bernoulli sequence]]
[[!redirects Bernoulli process]]