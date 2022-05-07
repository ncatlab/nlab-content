

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

## Definition

In [[measure theory]], the _pushforward_ $f_\ast \mu$ of a [[measure]] $\mu$ on a [[measurable space]] $X$ along a [[measurable function]] $f \colon X \to Y$ to another [[measure space]] $Y$ assigns to a subset the original measure of the [[preimage]] under $f$ of that subset:

$$
  (f_\ast\mu)( - ) \coloneqq \mu(f^{-1}(-))
  \,.
$$




## Properties

### General 

* The pushforward of a [[τ-additive measure]] along a [[continuous map]] is again τ-additive.

* If a [[continuous valuation]] $\nu$ on a topological space $X$ is [[valuation (measure theory)#extending_valuations_to_measures|extendable to a measure]] $\nu$, its [[valuation (measure theory)#pushforward|pushforward (as a valuation)]] $f_*\mu$ along a [[continuous map]] $f:X\to Y$ is again extendable, and it extends to $f_*\nu$.

* The pushforward measure along a [[product]] projection is called a [[marginal measure]].

### Relation to entropy

\begin{prop}\label{EntropyDoesNotIncreaseUnderPushforward}
  **([[entropy]] does not increase under [[pushforward measure|pushforward]])**
  Let $f \colon X \longrightarrow Y$ be a [[measurable function]] between [[measure spaces]], and let $\mu$ be a [[probability distribution]] on $X$. Then the [[entropy]] of $\mu$ is larger or equal to that of its [[pushforward measure|pushforward]] distribution $f_\ast \mu$:

$$
  S(\mu) 
  \;\geq\;
  S
  \big(
    f_\ast(\mu)
  \big)
  \,.
$$

\end{prop}

(e.g. [Austin, Prop. 2.7](#Austin))

### Relation to the Giry monad

The construction of pushforward measures is how one can make the [[Giry monad]], or other [[measure monads]], [[functor|functorial]]. Given a measurable (or continuous, etc.) map $f \colon X\to Y$, the pushforward gives a well-defined, measurable map $P X\to P Y$ (where $P$ denotes the [[Giry monad]]), making $P$ into a [[functor]].


## Related concepts

* [[Borel measure]], [[Radon measure]], [[τ-additive measure]]

* [[monads of probability, measures, and valuations]]

* [[Giry monad]]

* [[conditional expectation]]

* [[pullback of a function]]

* [[pullback in cohomology]]






## References

See also

* Wikipedia, _[Pushforward measure](https://en.wikipedia.org/wiki/Pushforward_measure)_

In relation to [[entropy]]:

* {#Austin} Tim D. Austin, *Entropy and Sinai’s Theorem* ([pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.135.8492&rep=rep1&type=pdf), [[AustinEntropyAndSinaiTheorem.pdf:file]])


[[!redirects pushforward measures]]
[[!redirects push-forward measure]]
[[!redirects push-forward measures]]
[[!redirects pushforward of a measure]]
[[!redirects pushforward of measures]]
[[!redirects push-forward of a measure]]
[[!redirects push-forward of measures]]
[[!redirects image measure]]
[[!redirects image measures]]
