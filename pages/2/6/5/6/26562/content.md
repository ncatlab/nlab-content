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

* [[de Finetti's theorem]], stated, interpreted and proven in terms of [[Markov categories]] with [[probability monads]]. Main results in [Fritz-Gonda-Perrone'21](#fritz_definetti), see also [Moss-Perrone'22](#det_submonad) for further context. An analogous result was proven in the [[category of couplings]], [Ensarguet-Perrone'23](#ergodic_dagger). An additional, independent categorical approach is given in [Jacobs-Staton'20](#definetti_limit).

* [[disintegrations]] (...) 

* [[d-separation]] (...)

* [[entropy]] and [[data processing inequalities]] (...)

* [[ergodic decomposition theorem]] (...)

* filtering (...)

* [[idempotent completion]] of [[BorelStoch]] (...)

* joint and marginal distributions (...)

* [[Kolmogorov extension theorem]] (...)

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

* {#Lawvere62} [[W. Lawvere]], _The category of probabilistic mappings_, ms. 12 pages, 1962 
([[lawvereprobability1962.pdf:file]])


Here are other references:


* {#fritzmarkov} [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_, Advances of Mathematics 370, 2020. ([arXiv:1908.07021](http://arxiv.org/abs/1908.07021))

* {#fritz_definetti} [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], _De Finetti's theorem in categorical probability_. Journal of Stochastic Analysis, 2021. ([arXiv:2105.02639](https://arxiv.org/abs/2105.02639))

* {#cd_categories} Kenta Cho, [[Bart Jacobs]], _Disintegration and Bayesian Inversion via String Diagrams_, Mathematical Structures of Computer Science 29, 2019. ([arXiv:1709.00322](https://arxiv.org/abs/1709.00322))

* {#definetti_limit} [[Bart Jacobs]], [[Sam Staton]], _De Finetti's construction as a categorical limit_, Proceedings of CMCS, 2021. ([arXiv:2003.01964](https://arxiv.org/abs/2003.01964))

* {#coecke_spekkens11} [[Bob Coecke]] and Robert W. Spekkens, _Picturing classical and quantum Bayesian inference_, Synthese, 186(3), 2012. ([arXiv](https://arxiv.org/abs/1102.2368))

* {#Perrone_thesis} [[Paolo Perrone]], _Categorical Probability and Stochastic Dominance in Metric Spaces_, ([thesis](http://www.paoloperrone.org/phdthesis.pdf))

* {#FPKant} [[Tobias Fritz]] and [[Paolo Perrone]], _A Probability Monad as the Colimit of Spaces of Finite Samples_, Theory and Applications of Categories 34, 2019. ([arXiv:1712.05363](https://arxiv.org/abs/1712.05363))

* {#monads_supports} [[Tobias Fritz]], [[Paolo Perrone]], Sharwin Rezagholi, _Probability, valuations, hyperspace: Three monads on Top and the support as a morphism_, Mathematical Structures in Computer Science 31(8), 2021. ([arXiv:1910.03752](https://arxiv.org/abs/1910.03752))

* {#pearl_jeffrey} [[Bart Jacobs]], _Pearl's and Jeffrey's Update as Modes of Learning in Probabilistic Programming_ ([arXiv:2309.07053](https://arxiv.org/abs/2309.07053))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)

* {#markov_supports} [[Tobias Fritz]], Tomáš Gonda, Antonio Lorenzin, [[Paolo Perrone]], Dario Stein, _Absolute continuity, supports and idempotent splitting in categorical probability_, ([arXiv:2308.00651](https://arxiv.org/abs/2308.00651))

* {#dilations} [[Tobias Fritz]], Tomáš Gonda, Nicholas Gauguin Houghton-Larsen, [[Paolo Perrone]] and Dario Stein, _Dilations and information flow axioms in categorical probability_. Mathematical Structures in Computer Science, 2023. ([arXiv:2211.02507](https://arxiv.org/abs/2211.02507)).

* {#det_submonad} Sean Moss, [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))

* {#d-sep} [[Tobias Fritz]] and Andreas Klingler, _The d-separation criterion in Categorical Probability_, Journal of Machine Learning Research 24(46), 2023. ([arXiv](https://arxiv.org/abs/2207.05740))

* [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], Eigil Fjeldgren Rischel, _Representable Markov categories and comparison of statistical experiments in categorical probability_, Theoretical Computer Science 961, 2023. ([arXiv:2010.07416](https://arxiv.org/abs/2010.07416))

* {#fritzrischel} [[Tobias Fritz]] and Eigil Fjeldgren Rischel, _Infinite products and zero-one laws in categorical probability_, Compositionality 2(3) 2020. ([arXiv:1912.02769](http://arxiv.org/abs/1912.02769))

* {#markov_entropy} [[Paolo Perrone]], _Markov Categories and Entropy_, IEEE Transactions on Information Theory, 2023. ([arXiv](https://arxiv.org/abs/2212.11719))

* {#Chentsov65} N. N. Chentsov, _The categories of mathematical statistics_, Dokl. Akad. SSSR 164, 1965.

* {#giry82} Michèle Giry, _A categorical approach to probability theory_, Categorical aspects of topology and analysis, Lecture notes in Mathematics 915, Springer, 1982.

* {#moggi89} [[Eugenio Moggi]], *Computational lambda-calculus and monads*, Proceedings of LICS, 1989. ([doi](https://doi.org/10.1109/LICS.1989.39155))

* {#jones_plotkin89} Claire Jones and [[Gordon Plotkin]], _A probabilistic powerdomain of evaluations_, Procedings of LICS, 1989. ([doi](https://doi.org/10.1109/LICS.1989.39173))

* {#golubtsov99} Peter V. Golubtsov, _Axiomatic description of categories of information converters_, Problemy Peredachi Informatsii (Problems in Information Transmission) 35(3), 1999. 

* {#golubtsov02} Peter V. Golubtsov, _Monoidal Kleisli category as a background for information transformers theory_. Information Theory and Information Processing 2, 2002.

* {#golubtsov_mosaliuk02} Peter V. Golubtsov and Stepan S. Moskaliuk, _Method of additional structures on the objects of a monoidal Kleisli category as a background for information transformers theory_, Hadronic Journal 25(2), 2002.

* {#golubtsov04} Peter V. Golubtsov, _Information transformers: category-theoretical structure, informativeness, decision-making problems_, Hadronic Journal Supplements 19(3), 2004.

* {#coecke_spekkens11} [[Bob Coecke]] and Robert W. Spekkens, _Picturing classical and quantum Bayesian inference_, Synthese, 186(3), 2012. ([arXiv](https://arxiv.org/abs/1102.2368))

* {#fong12} [[Brendan Fong]], _Causal theories: A categorical prespective on Bayesian networks_, master thesis, University of Oxford, 2012. ([arXiv](https://arxiv.org/abs/1609.05382))

* [[Tobias Fritz]], [[Wendong Liang]], _Free gs-monoidal categories and free Markov categories_, Applied Categorical Structures 31, 21, 2023. ([arXiv:2204.02284](https://arxiv.org/abs/2204.02284))

* Sean Moss and [[Paolo Perrone]], _A category-theoretic proof of the ergodic decomposition theorem_, Ergodic Theory and Dynamical Systems, 2023. ([arXiv:2207.07353](https://arxiv.org/abs/2207.07353))

* [[Bart Jacobs]], _Multinomial and Hypergeometric Distributions in Markov Categories_, Proceedings of MFPS 2021. ([arXiv](https://arxiv.org/abs/2112.14044))

* [[Tobias Fritz]], [[Fabio Gadducci]], Davide Trotta, Andrea Corradini, _From gs-monoidal to oplax-cartesian categories: constructions and functorial completeness_, Applied Categorical Structures 31, 42, 2023. ([arXiv](https://arxiv.org/abs/2205.06892))

* [[Tobias Fritz]], [[Fabio Gadducci]], [[Paolo Perrone]] and Davide Trotta, _Weakly Markov categories and weakly affine monads_, Proceedings of CALCO, LIPIcs 10, 2023. ([arXiv](https://arxiv.org/abs/2303.14049))

* Dario Stein and Richard Samuelson, _A Category for unifying Gaussian Probability and Nondeterminism_, Proceedings of CALCO, LIPIcs 10, 2023. ([arXiv](https://arxiv.org/abs/2204.14024))

* [[Tobias Fritz]] and Antonio Lorenzin, _Involutive Markov categories and the quantum de Finetti theorem_, 2023. ([arXiv](https://arxiv.org/abs/2312.09666))

* [[Bart Jacobs]], Fabio Zanasi, and Octavio Zapata, _Bayesian Factorisation as Adjoint, [abstract](http://wadt18.cs.rhul.ac.uk/submissions/WADT18A33.pdf)
Adjunction between Bayesian nets and distributions. How can one net be assigned? 

* [[Bart Jacobs]], _Structured Probabilistic Reasoning_, [pdf](http://www.cs.ru.nl/B.Jacobs/PAPERS/ProbabilisticReasoning.pdf)

* [[Bart Jacobs]], _Categorical Aspects of Parameter Learning_, [slides](http://www.cs.ru.nl/B.Jacobs/TALKS/learning.pdf)

* [[Bob Coecke]], Eric Oliver Paquette, Dusko Pavlovic, _Classical and quantum structuralism_, ([arXiv:0904.1997](https://arxiv.org/abs/0904.1997))

* [[Bart Jacobs]], Fabio Zanasi, _The Logical Essentials of Bayesian Reasoning_, ([arXiv:1804.01193](https://arxiv.org/abs/1804.01193))

* [[Bart Jacobs]], Aleks Kissinger, Fabio Zanasi, _Causal Inference by String Diagram Surgery_, ([arXiv:1811.08338](https://arxiv.org/abs/1811.08338))

* {#bimonoidal_monads} [[Tobias Fritz]], [[Paolo Perrone]], _Bimonoidal Structure of Probability Monads_, Proceedings of MFPS, 2018, ([arXiv:1804.03527](https://arxiv.org/abs/1804.03527))

* Alex Simpson, _Probability Sheaves and the Giry Monad_, ([pdf](https://coalg.org/mfps-calco2017/calco-papers/calco2017-1.pdf))

* Nathaniel Virgo, _Unifilar Machines and the Adjoint Structure of Bayesian Filtering_, Proceedings of ACT, 2023. ([arXiv](https://arxiv.org/abs/2305.02826))

* Chris Heunen, Ohad Kammar, Sam Staton, Hongseok Yang, _A Convenient Category for Higher-Order Probability Theory_, ([arXiv:1701.02547](https://arxiv.org/abs/1701.02547))

* {#panangaden_markov} Prakash Panangaden, _Labelled Markov processes_, Imperial College Press, 2009.

* {#panangaden_condexp} Prakash Panangaden, _A categorical view of conditional expectation_, ([slides](http://math.ucr.edu/home/baez/mathematical/ACTUCR/Panagaden_Conditional_Expectation.pdf))

* Dario Stein and [[Sam Staton]], _Probabilistic Programming with Exact Conditions_, JACM, 2023. ([arXiv](https://arxiv.org/abs/2312.17141))

* [[Bart Jacobs]], _A Channel-Based Perspective on Conjugate Priors_, ([arXiv:1707.00269](https://arxiv.org/abs/1707.00269))


* [[Tobias Fritz]], Andreas Klingler, Drew McNeely, Areeb Shah-Mohammed and Yuwen Wang, _Hidden Markov models and the Bayes filter in categorical probability_, 2024. ([arXiv](https://arxiv.org/abs/2401.14669))

(...more to add...)



[[!redirects category-theoretic approach to probability theory]]
[[!redirects categorical approach to probability theory]]
[[!redirects categorical approaches to probability theory]]
[[!redirects categorical probability]]
[[!redirects categorical probability theory]]
[[!redirects categorical probability and statistics]]
[[!redirects synthetic probability]]
[[!redirects synthetic probability theory]]