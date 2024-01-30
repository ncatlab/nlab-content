
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

The [[category]] whose [[objects]] are [[finite sets]] and whose [[morphisms]] are [[stochastic maps]] (or [[stochastic matrices]]) is often denotes _FinStoch_, or similar.

It is an elementary but nontrivial example of a [[Markov category]], and together with its subcategory [[Stoch#borelstoch|BorelStoch]], one of the most important categories of [[categorical probability]].

## Definition

_FinStoch_ is the category whose 

* [[Objects]] are [[finite sets]];
* [[Morphisms]] are [[stochastic matrices]].

See at [[stochastic matrix]] for more details.

## Properties

* _FinStoch_ is closely related to the Kleisli category of the [[distribution monad]]: it is its [[full subcategory]] whose objects are finite sets.

* _FinStoch_ is a [[Cauchy-complete category]].

* As a [[Markov category]], it has [[Markov category#conditionals|conditionals]], and is hence [[Markov category#positivity_and_causality|positive and causal]].

## Related concepts

* [[Markov category]]
* [[Markov kernel]]
* [[category of couplings]]
* [[probability monad]]
* [[Giry monad]]
* [[Kleisli category]]
* [[categorical probability]]


## References:

* {#markov_support} Tobias Fritz, Tomáš Gonda, Antonio Lorenzin, Paolo Perrone, Dario Stein, _Absolute continuity, supports and idempotent splitting in categorical probability_, ([arXiv:2308.00651](https://arxiv.org/abs/2308.00651))

category: category

[[!redirects Finstoch]]