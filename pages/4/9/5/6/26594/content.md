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

In [[probability theory]], *zero-one laws* are conditions for which a certain [[probability measure]] can only assume the values [[zero]] and [[one]] (i.e. it is a [[zero-one measure]]).

Very often they can be seen as conditions for which a probability measure, usually an [[iid measure|iid one]], is [[ergodic]] (that is, it is [[zero-one measure|zero-one]] on the [[invariant sets]] of some [[action]]). 


## Statements

### Hewitt-Savage zero-one law

Let $(X,p)$ be a [[probability space]]. Consider the infinite product $X^\mathbb{N}$, and form the [[iid measure]] $\tilde{p}$ on $X^\mathbb{N}$ whose [[marginals]] are given by $p$. 

Then for every [[exchangeable event]] $A\subseteq X^\mathbb{N}$ we have that either $\tilde{p}(A)=0$ or $\tilde{p}(A)=1$.
That is, $\tilde{p}$ restricted to the [[exchangeable sigma-algebra]] is a [[zero-one measure]]. 

(The equivalent characterizations of [[zero-one measures]] give equivalent formulations of this statement.)


### Kolmogorov's zero-one law

Let $(X,p)$ be a [[probability space]]. Consider the infinite product $X^\mathbb{N}$, and form the [[iid measure]] $\tilde{p}$ on $X^\mathbb{N}$ whose [[marginals]] are given by $p$. 

Then for every [[tail event]] $A\subseteq X^\mathbb{N}$ we have that either $\tilde{p}(A)=0$ or $\tilde{p}(A)=1$.
That is, $\tilde{p}$ restricted to the [[tail sigma-algebra]] is a [[zero-one measure]]. 

(The equivalent characterizations of [[zero-one measures]] give equivalent formulations of this statement.)


### Levy's zero-one law

See [[martingale convergence theorem]].


## In categorical probability

### Markov categories

(For now, see [Fritz-Rischel'20](#fritzrischel).)

### Dagger categories

(For now, see [Ensarguet-Perrone'23](#ergodic_dagger).)


## See also

* [[probability theory]], [[categorical probability]]

* [[zero-one measure]], [[zero-one kernel]], [[deterministic random variable]], [[Dirac measure]]

* [[ergodicity]], [[invariant measure]], [[invariant set]], [[ergodic decomposition theorem]]

* [[de Finetti's theorem]], [[exchangeability]], [[tail event]]

* [[law of large numbers]], [[ergodic theorem]]

* [[Markov category]], [[probability monad]]



## References

* {#fritzrischel} [[Tobias Fritz]] and Eigil Fjeldgren Rischel, _Infinite products and zero-one laws in categorical probability_, Compositionality 2(3) 2020. ([arXiv:1912.02769](http://arxiv.org/abs/1912.02769))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)


category: probability


[[!redirects zero-one laws]]
[[!redirects 0-1 law]]
[[!redirects 0-1 laws]]
[[!redirects Kolmogorov zero-one law]]
[[!redirects Hewitt-Savage zero-one law]]
[[!redirects Kolmogorov 0-1 law]]
[[!redirects Hewitt-Savage 0-1 law]]