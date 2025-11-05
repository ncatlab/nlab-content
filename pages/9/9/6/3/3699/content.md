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
A __Markov chain__ (named for [[Andrey Markov]]) is a [[sequence]] of [[random variables]] taking values in the state space of the chain, with the property that the [[probability]] of moving to the next state depends only upon the current state.  For the case of a finite state space this is just the statement that

$$
Pr(X_{n + 1} = x | X_1 = x_1, X_2 = x_2,..., X_n = x_n) = Pr(X_{n + 1} = x | X_n = x_n).
$$ 

## Definition

A Markov chain is a special case of a [[stochastic process]] in which the dynamical laws at each stage of the process are a Markov dynamic law (which is defined on the page [[stochastic process]]) and the states at every stage of the process are identical.

## Related concepts

* [[stochastic process]]


## Literature

[Wikipedia](http://en.wikipedia.org/wiki/Markov_chain).

Baez and his students recently defined a generalization, open Markov chains:

* [[John C. Baez]], [[Brendan Fong]], Blake S. Pollard: _A compositional framework for Markov processes_, [arxiv/1508.06448](http://arxiv.org/abs/1508.06448)


category: probability

[[!redirects Markov chain]]
[[!redirects Markov chains]]

[[!redirects Markov process]]
[[!redirects Markov processes]]


