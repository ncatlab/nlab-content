

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

## As a functor

The construction of pushforward measures is how one can make the [[Giry monad]], or other [[monads of measures]], functorial. Given a measurable (or continuous, etc.) map $f:X\to Y$, the pushforward gives a well-defined, measurable map $P X\to P Y$ (where $P$ denotes the [[Giry monad]]), making $P$ into a [[functor]].

## Properties

* The pushforward of a [[τ-additive measure]] along a [[continuous map]] is again τ-additive.

* If a [[continuous valuation]] $\nu$ on a topological space $X$ is [[valuation (measure theory)#extending_valuations_to_measures|extendable to a measure]] $\nu$, its [[valuation (measure theory)#pushforward|pushforward (as a valuation)]] $f_*\mu$ along a [[continuous map]] $f:X\to Y$ is again extendable, and it extends to $f_*\nu$.

## Related concepts

* [[Borel measure]], [[Radon measure]], [[τ-additive measure]]
* [[monads of probability, measures, and valuations]]
* [[Giry monad]]

* [[conditional expectation]]








## References

See also

* Wikipedia, _[Pushforward measure](https://en.wikipedia.org/wiki/Pushforward_measure)_

[[!redirects pushforward measures]]
[[!redirects push-forward measure]]
[[!redirects push-forward measures]]
[[!redirects image measure]]
[[!redirects image measures]]
