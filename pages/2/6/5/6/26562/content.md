[[!redirects categorical approaches to probability theory]]

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

There are a number of approaches to apply [[category theory]] to [[probability]] and related fields, such as [[statistics]], [[information theory]] and [[dynamical systems]].

On one hand, one can study the existing structures in traditional probability theory (such as [[probability spaces]], [[integration]], and so on) using a categorical lens. For instance, the [[Giry monad]] models the formation of spaces of [[probability measures]] and its iterations, used for example in the context of [[de Finetti's theorem]].

On the other hand, one can try to express certain aspects of [[probability]] and [[statistics]] [[analytic versus synthetic|synthetically]]. One looks for [[structures]] and [[axioms]] which can be thought of as "fundamental" in probability and statistics, and which one can use to prove theorems, without having to use [[measure theory]] directly. One then proves that the usual measure-theoretic treatment is a [[model]] (or [[semantics]]) of this theory. This approach is often called **synthetic probability theory**, in analogy for example with [[synthetic differential geometry]].
One of the most recent approaches to synthetic probability theory is given by [[Markov categories]].

The main end goals of categorical probability are

* To generalize existing results in probability theory to more general settings, for example with less stringent conditions on countability, separability, etc.;
* To find new results, which with the traditional methods would have been too complex to prove;
* To make probability and related fields more accessible to practitioners, thanks to the fact that the formalism incorporates measure theory without requiring any deep knowledge of it.


## Main structures of interest


### Markov categories

For now, see [[Markov category]].

(...)


### Probability monads

For now, see [[probability monad]].

(...)


### Dagger categories

For now, see [[dagger category]].

(...)


## Main results

Using category-theoretic methods, several results have been obtained in the past few years.

Firstly, some known concepts and results of probability theory have been given a category-theoretic description.
(For example: expressing [[Kolmogorov's extension theorem]] as a [[cofiltered limit]] condition.) This allows to incorporate the existing theory of probability into the categorical framework, and is the basic starting point for further results. 
(For example, every time in traditional probability Kolmogorov's extension theorem is invoked, one now knows that a certain universal property is being used.)

Secondly, some classical results of probability theory have been restated and reproven using category theory.
Often this adds new insight into the problem, and allows, for example, to drop further unnecessary assumptions (see the next point).
In addition, the category-theoretic formalism often trades higher complexity for higher abstraction. This way, while more abstract, the categorical proofs tend to be simpler than their measure-theoretic counterparts. (And so, they also allow to prove more difficult results more easily.) 

Thirdly, and most importantly, *new theorems* have been proven, as well as generalizations and extensions of old theorems, especially from the discrete to the continuous case. 

Here is a partial list, in alphabetical order.

(Work in progress, especially adding the relevant references.)

* [[Bayesian inverses]] (...)

* Blackwell-Sherman-Stein theorem on statistical experiments (...)

* [[conditional expectations]] (...)

* [[de Finetti's theorem]], stated, interpreted and proven in terms of Markov categories as well as in dagger categories. Main results in [Fritz-Gonda-Perrone'21](#fritz_definetti), see also [Moss-Perrone'22](#det_submonad) and [Ensarguet-Perrone'23](#ergodic_dagger) for further context. An additional categorical approach is given in [Jacobs-Staton'20](#definetti_limit).

* [[disintegrations]] (...) 

* [[d-separation]] (...)

* [[entropy]] and [[data processing inequalities]] (...)

* [[ergodic decomposition theorem]] (...)

* [[Kolmogorov extension theorem]] (...)

* joint and marginal distributions (...)

* [[martingales]] (...)

* multinomial and hypergeometric distributions (...)

* privacy in name generation (...)

* [[sufficient statistics]] (...)

* Kolmogorov and Hewitt-savage's [[zero-one laws]] (...)

(also missing: quantum probability)


## See also

* [[Markov category]]

* [[probability monad]]

* [[probability theory]]


## References

The first work on categorical probability seems to be due to Lawvere, and it is unpublished:

*{#Lawvere62} [[W. Lawvere]], _The category of probabilistic mappings_, ms. 12 pages, 1962 
([[lawvereprobability1962.pdf:file]])


Here are other references:


* {#fritz_definetti} [[Tobias Fritz]], [[Tomáš Gonda]], [[Paolo Perrone]], _De Finetti's theorem in categorical probability_. Journal of Stochastic Analysis, 2021. ([arXiv:2105.02639](https://arxiv.org/abs/2105.02639))

* Bart Jacobs, Fabio Zanasi, and Octavio Zapata, _Bayesian Factorisation as Adjoint, [abstract](http://wadt18.cs.rhul.ac.uk/submissions/WADT18A33.pdf)
Adjunction between Bayesian nets and distributions. How can one net be assigned? 

* Bart Jacobs, _Structured Probabilistic Reasoning_, [pdf](http://www.cs.ru.nl/B.Jacobs/PAPERS/ProbabilisticReasoning.pdf)

* Bart Jacobs, _Categorical Aspects of Parameter Learning_, [slides](http://www.cs.ru.nl/B.Jacobs/TALKS/learning.pdf)

* {#cd_categories} Kenta Cho, Bart Jacobs, _Disintegration and Bayesian Inversion via String Diagrams_, ([arXiv:1709.00322](https://arxiv.org/abs/1709.00322))

* {#definetti_limit} Bart Jacobs, Sam Staton, _De Finetti's construction as a categorical limit_, ([arXiv:2003.01964](https://arxiv.org/abs/2003.01964))

* Bob Coecke, Eric Oliver Paquette, Dusko Pavlovic, _Classical and quantum structuralism_, ([arXiv:0904.1997](https://arxiv.org/abs/0904.1997))

* Bob Coecke, Robert W. Spekkens, _Picturing classical and quantum Bayesian inference_, ([arXiv:1102.2368](https://arxiv.org/abs/1102.2368))

* Bart Jacobs, Fabio Zanasi, _The Logical Essentials of Bayesian Reasoning_, ([arXiv:1804.01193](https://arxiv.org/abs/1804.01193))

* Bart Jacobs, Aleks Kissinger, Fabio Zanasi, _Causal Inference by String Diagram Surgery_, ([arXiv:1811.08338](https://arxiv.org/abs/1811.08338))

* {#bimonoidal_monads} Tobias Fritz, Paolo Perrone, _Bimonoidal Structure of Probability Monads_, ([arXiv:1804.03527](https://arxiv.org/abs/1804.03527))

* {#Perrone_thesis} Paolo Perrone, _Categorical Probability and Stochastic Dominance in Metric Spaces_, ([thesis](http://www.paoloperrone.org/phdthesis.pdf))

* {#FPKant} [[Tobias Fritz]] and Paolo Perrone, _A Probability Monad as the Colimit of Spaces of Finite Samples_, ([arXiv:1712.05363](https://arxiv.org/abs/1712.05363)).

* {#fritz_markov} Tobias Fritz, _A synthetic approach to Markov kernels, conditional independence, and theorems on sufficient statistics_, ([arXiv:1908.07021](https://arxiv.org/abs/1908.07021))

* {#monads_supports} Tobias Fritz, Paolo Perrone, Sharwin Rezagholi, _Probability, valuations, hyperspace: Three monads on Top and the support as a morphism_, ([arXiv:1910.03752](https://arxiv.org/abs/1910.03752))

* Alex Simpson, _Probability Sheaves and the Giry Monad_, ([pdf](https://coalg.org/mfps-calco2017/calco-papers/calco2017-1.pdf))

* Chris Heunen, Ohad Kammar, Sam Staton, Hongseok Yang, _A Convenient Category for Higher-Order Probability Theory_, ([arXiv:1701.02547](https://arxiv.org/abs/1701.02547))

* {#panangaden_condexp} Prakash Panangaden, _A categorical view of conditional expectation_, ([slides](http://math.ucr.edu/home/baez/mathematical/ACTUCR/Panagaden_Conditional_Expectation.pdf))

* Dario Stein, Sam Staton, _Compositional Semantics for Probabilistic Programs with Exact Conditioning_, ([arXiv:2101.11351](https://arxiv.org/abs/2101.11351))

* Bart Jacobs, _A Channel-Based Perspective on Conjugate Priors_, ([arXiv:1707.00269](https://arxiv.org/abs/1707.00269))

* {#pearl_jeffrey} Bart Jacobs, _Pearl's and Jeffrey's Update as Modes of Learning in Probabilistic Programming_ ([arXiv:2309.07053](https://arxiv.org/abs/2309.07053))

* {#ergodic_dagger} Noé Ensarguet, Paolo Perrone, Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)

* {#markov_supports} Tobias Fritz, Tomáš Gonda, Antonio Lorenzin, Paolo Perrone, Dario Stein, _Absolute continuity, supports and idempotent splitting in categorical probability_, ([arXiv:2308.00651](https://arxiv.org/abs/2308.00651))

* {#markov_dilations} Tobias Fritz, Tomáš Gonda, Nicholas Gauguin Houghton-Larsen, Antonio Lorenzin, Paolo Perrone, Dario Stein, _Dilations and information flow axioms in categorical probability_, ([arXiv:2211.02507](https://arxiv.org/abs/2211.02507))

* {#det_submonad} [[Sean Moss]], [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))


(...more to add...)



[[!redirects category-theoretic approach to probability theory]]
[[!redirects categorical approach to probability theory]]
[[!redirects categorical approaches to probability theory]]
[[!redirects categorical probability]]
[[!redirects categorical probability theory]]
[[!redirects categorical probability and statistics]]
[[!redirects synthetic probability]]
[[!redirects synthetic probability theory]]