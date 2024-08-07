
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

A **random variable**, or _stochastic variable_, is  a quantity that is subject to 'random' variation.

Some authors in [[probability theory]] distinguish between random variables and **random elements**: a *random element* is a generic entity (such as a [[point]] of a [[set]] or [[space]]) subject to random variation, while a *random variable* is specifically a [[number]] subject to random variation. 


## Definition

The formalization of this idea in modern [[probability theory]] ([Kolmogorov 33, III](#Kolmogorov33)) is to take a random variable to be a [[measurable function]] $f$ on a [[probability space]] $(X,\mathcal{F},\mu)$ (e.g. [Grigoryan 08, 3.2](#Grigoryan08), [Dembo 12, 1.2.1](#Dembo12)). 

One thinks of $X$ as the space of all possible configurations (all the "[[possible worlds]]" with respect to the idealized situation under consideration), thinks of the measure $\mu(U)$ of any [[subset]] of it as the [[probability]] that one of the configurations $x \in U \subset X$ is _randomly_ realized, and thinks of $f(x)$ as the value of the given random variable in the situation of that configuration.

Often, a *random element* is a [[measurable function]] $X\to Y$, where $Y$ is a generic [[measurable space]], while the term *random variable* is reserved for the case where $Y$ is $\mathbb{R}$, $\mathbb{R}^n$, or a more general [[vector space]].
One speaks for example of *random elements of a set*, and of *real-valued* or *vector-valued random variables*.

In particular, the term *random variable* tends to be used for those situation where there is a notion of [[expectation value]].
For example the [[expectation value]] of a (real-valued) random variable $f$ is the [[integral]]

$$
  \langle f \rangle \coloneqq \int_X f \cdot \mu
$$

of $f$ against the [[probability measure]] $\mu$, i.e. the average value of the random variable over all possible configuration, weighted by their [[probability]].


## Properties

### Relation to type theoretic constructions

There is at least some similarity of the concept of random variables to usage of the [[function monad]] ("[[reader monad]]") in the context of [[monad (in computer science)|monads in computer science]]. 

In [Verdier 14](#Verdier14) it says:

> The intuition behind the Reader monad, for a mathematician, is perhaps stochastic variables. A stochastic variable is a function from a probability space to some other space. So we see a stochastic variable as a monadic value.

and in [Toronto-McCarthy 10b, slide 35](#TorontoMcCarthy10b):

> you could interpret this by regarding random variables as reader monad computations. 

See also ([Toronto-McCarthy 10b, slide 24](#TorontoMcCarthy10b)). [Toronto-McCarthy 10a, 2.2](#TorontoMcCarthy10a), [Toronto 14](#Toronto14) call the [[function monad]] the _random variable idiom_.

### Random variables and Dedekind reals

Given a measure space $(X,\Sigma,\mu)$, a _random variable_ is also often  defined as an _equivalence class_ of measurable _real_-valued functions on $X$ where two such functions are identified when they differ only on a subset of measure zero.

In this context, it has been observed by [[Pierre Deligne|P. Deligne]][^Del] that the po-set of measurable subsets $\Sigma$ can be equipped with a suitable [[Grothendieck topology]].

[^Del]:  [[SGA4]].I, p.412.

In the resulting [[Grothendieck topos]] $Meas(X,\Sigma,\mu)$ the object of [[Dedekind real numbers]] $R_D$ corresponds to the _sheaf of random variables_ on $X$ in this sense.

A Dedekind real in a topos $Sh(X)$ of sheaves on a _topological space_ is just a continuous real-valued function on $X$. This suggests the view that the sheaf-theoretic perspective on $(X,\Sigma,\mu)$ sweeps the measure-theoretic details under the rug and brings out the conceptual essence of a random variable as simply a real-valued 'function' or 'variable real number' on $X$ and goes in the same direction as the connection to the function monad mentioned in the previous section.

The details of this example, due to [[Dana Scott|D. Scott]], are described in ([Johnstone 1977](#Johnstone77), p.213).

## Related concepts

* [[iid random variables]]

* [[probability theory]]

* [[probability monad]]

## References

* Wikipedia, _[Random variable](http://en.wikipedia.org/wiki/Random_variable)_

The modern formal concept originates around

* {#Kolmogorov33} [[Andrey Kolmogorov]], _Grundbegriffe der Wahrscheinlichkeitsrechnung_, Ergebnisse der Mathematik und Ihrer Grenzgebiete, Springer Berlin Heidelberg 1933.

Surveys and lecture notes include

* {#Grigoryan08} Alexander Grigoryan, _Measure theory and probability_, 2008. ([pdf](https://www.math.uni-bielefeld.de/~grigor/mwlect.pdf))

* {#Dembo12} [[Amir Dembo]], _Probability theory_, 2012. ([pdf](http://statweb.stanford.edu/~adembo/stat-310a/lnotes.pdf))

For more information on the above topos-theoretic example consult

* {#Johnstone77} [[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977. (Dover reprint 2014)

Discussion from a point of view of [[type theory]]/[[computer science]] includes

* {#TorontoMcCarthy10a} [[Neil Toronto]], [[Jay McCarthy]], _From Bayesian notation to pure Racket, via measure-theoretic probability_, in _Implementation and Application of Functional Languages_, 2010. ([article](https://link.springer.com/chapter/10.1007/978-3-642-24276-2_6))

* {#TorontoMcCarthy10b} [[Neil Toronto]], [[Jay McCarthy]], _From Bayesian Notation to Pure Racket_, talk notes 2010. ([pdf](http://jeapostrophe.github.io/home/static/toronto-2010ifl-slides.pdf))

* {#Toronto14} [[Neil Toronto]], _Useful Languages for Probabilistic Modeling and Inference_, PhD Thesis, 2014. ([pdf](http://cs.umd.edu/~ntoronto/papers/toronto-2014diss.pdf), [slides](http://cs.umd.edu/~ntoronto/papers/toronto-2014diss-slides.pdf))

* {#Verdier14} [[Olivier Verdier]], _[The Reader and Writer Monads and Comonads](http://www.olivierverdier.com/posts/2014/12/31/reader-writer-monad-comonad/)_, 2014.


category: probability

[[!redirects random variables]]

[[!redirects random element]]
[[!redirects random elements]]

[[!redirects stochastic variable]]
[[!redirects stochastic variables]]