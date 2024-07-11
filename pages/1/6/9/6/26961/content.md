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
They are a mathematical formalization of the idea of repeated, independent coin flips, or dice rolls: they are independent events, but the [[probability]] of each single variable (for example, each single coin flip) follows the same distribution.

Another name for the same process is *Bernoulli process*.


## Definition

Let $X$ be a [[measurable space]]. 
[[random variable|Random variables]] or [[random elements]] in a [[sequence]] $f_n \colon \Omega\to X$ on a [[probability space]] $(\Omega,\mu)$ are said to be **iid**, or **independent and identically distributed**, if their [[joint distribution]] $p$ is in the form 
$q\otimes q\otimes\dots\otimes q$ for some measure $q$ on $X$. Equivalently, if for all [[measurable subsets]] $A_1,\dots,A_n$ of $X$, 
$$
p(A_1\times\dots\times A_n) \;=\; q(A_1)\cdots q(A_n)\,.
$$

A similar definition can be given for [[infinite products]] as well, by means of the [[Kolmogorov extension theorem]].

Sometimes, especially when the space $X$ is [[finite set|finite]] (particularly when it has two elements, such as for coin flips), one calls the resulting [[stochastic process]] a **Bernoulli process**.


### In categorical probability

In [[categorical probability]], for example in [[Markov categories]], independence is simply encoded by taking the [[tensor product]] of [[morphisms]] (for example, from the [[monoidal unit]]). 

In case one considers independent identical copies of a measure depending on a (shared) parameter, in Markov categories one can model the situation using the *copy map* (see at [[Markov category]]).


## Properties

* [[De Finetti's theorem]] says that every [[exchangeable probability measure]] is a unique [[convex mixture]] of iid ones.
* The [[Hewitt-Savage zero-one law]] says that given iid random variables, the probability of each [[exchangeable event]] is either zero or one, i.e. it is a [[zero-one measure]]. 

* The [[Kolmogorov zero-one law]], similarly, says that given iid [[random variables]], the probability of each [[tail event event]] is a [[zero-one measure]]. 

* The [[law of large numbers]] says that given integrable iid random variables, the [[empirical mean]] tends to the [[expectation value]].


## See also 

* [[probability theory]], [[categorical probability]]

* [[de Finetti's theorem]], [[Hewitt-Savage zero-one law]], [[Kolmogorov zero-one law]], [[law of large numbers]]

* [[infinitary tensor product]], [[Kolmogorov extension theorem]]

* [[ergodic system]], [[Bernoulli shifts]]


category: probability


[[!redirects iid]]
[[!redirects IID]]
[[!redirects IID random variables]]
[[!redirects iid random elements]]
[[!redirects IID random elements]]
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