
A __Markov chain__ (named for [[Andrey Markov]]) is a sequence of random variable taking values in the state space of the chain, with the property that the probability of moving to the next state depends only upon the current state:

$$
Pr(X_{n + 1} = x | X_1 = x_1, X_2 = x_2,..., X_n = x_n) = Pr(X_{n + 1} = x | X_n = x_n).
$$ 

A Markov chain can also be described as a [[coalgebra for an endofunctor|coalgebra]] for the [[endofunctor]] on [[Set]] which maps a set $X$ to the set of [[probability distribution|probability distributions]] on $X$.

+--{: .query}
[[Ian Durham]]: I assume that a Markov chain can be represented as a directed graph in some way and thus can be used to generate a free category of some sort.  Is this a correct assumption?

[[Eric]]: I'm pretty sure that is the case for _finite_ Markov chains.

[[Ian Durham]]: Hmmm.  I'll have to think about that.
=--

## Literature

[Wikipedia](http://en.wikipedia.org/wiki/Markov_chain).

Baez and his students recently defined a generalization, open Markov chains:

* [[John C. Baez]], [[Brendan Fong]], [[Blake S. Pollard]], _A compositional framework for Markov processes_, [arxiv/1508.06448](http://arxiv.org/abs/1508.06448)


category: probability

[[!redirects Markov chain]]
[[!redirects Markov chains]]
