
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

On the other hand, one can try to express certain aspects of [[probability]] and [[statistics]] [[analytic versus synthetic|synthetically]]. One looks for [[structures]] and [[axioms]] which can be thought of as "fundamental" in probability and statistics, and which one can use to prove theorems, without having to use [[measure theory]] directly. One then proves that the usual measure-theoretic treatment is a [[model]] (or [[semantics]]) of this theory. This approach is often called **[[synthetic probability theory]]**, in analogy for example with [[synthetic differential geometry]].
One of the most recent approaches to [[synthetic probability theory]] is given by [[Markov categories]].

The main end goals of categorical probability are

* To generalize existing results in probability theory to more general settings, for example with less stringent conditions on countability, separability, etc.;
* To find new results, which with the traditional methods would have been too complex to prove;
* To make probability and related fields more accessible to practitioners, thanks to the fact that the formalism incorporates measure theory without requiring the user to have any deep knowledge of it.


## Main structures of interest

[[category theory|Category theory]] was first developed to model particular structures in [[algebraic topology]], and subsequently [[algebraic geometry]], [[algebra]], [[logic]] and [[computer science]]. Each one of these intended applications shaped a piece of the theory, adding to category theory the relevant structures of interest for each application.

The applications of category theory to probability are among the most recent, and are both bringing new categorical structures into the theory (such as [[Markov categories]]), as well as repurposing and reinterpreting existing ideas (such as [[monads]]).

### Markov categories

[[Markov categories]] are a recent framework that models categories whose morphisms can be thought of as having randomness, such as [[stochastic maps]] and [[Markov kernels]]. 
It has a graphical formalism which keeps track of the stochastic dependencies, and which can be used to prove theorems in probability purely graphically.

For more details, see [[Markov category]].


### Probability monads

[[probability monads|Probability monads]] can be thought of as a way of adding a notion of "randomness" to an existing theory.
A [[monad]] often models the idea of "forming spaces of particular structures", and in probability theory, one is interested in forming spaces of [[probability measures]].
Monads are particularly useful when this construction needs to be iterated, for example, when in [[de Finetti theorem|de Finetti]] situations one needs to form _probability measures over probability measures_. 

For more details, see [[probability monad]].


### Dagger categories

[[dagger categories|Dagger categories]] can be thought of as "undirected" categories, where morphisms can be seen as going either way as in an undirected graph. 
In [[probability theory]], joint distributions, or [[transport plans]] exhibit such a behavior, sometimes called [[Bayesian inversion]].
Several probabilistic ideas can be modelled in terms of dagger-categorical concepts, for example, [[conditional expectation]].

For more details, see [[category of couplings]].


## Main results

Using category-theoretic methods, several results have been obtained in the past few years.

Firstly, some known concepts and results of probability theory have been given a category-theoretic description.
(For example: expressing [[Kolmogorov's extension theorem]] as a [[cofiltered limit]] condition.) This allows to incorporate the existing theory of probability into the categorical framework, and is the basic starting point for further results. 
(For example, every time in traditional probability Kolmogorov's extension theorem is invoked, one now knows that a certain [[universal property]] is being used.)

Secondly, some classical results of probability theory have been restated and reproven using category theory.
Often this adds new insight into the problem, and allows, for example, to drop further unnecessary assumptions (see the next point).
In addition, the category-theoretic formalism often trades higher complexity for higher abstraction. This way, while more abstract, the categorical proofs tend to be simpler than their measure-theoretic counterparts. (And so, they also allow to prove more difficult results more easily.) 

Thirdly, and most importantly, *new theorems* have been proven, as well as generalizations and extensions of old theorems, especially from the discrete to the continuous case. 

Here is a partial list, roughly in alphabetical order, roughly divided by subject.

(Work in progress, for more material see also the references below.)

### Probability and measure theory

* Aldous-Hoover theorem: proven using [[Markov categories]] in [CFGKL](#aldous_hoover).

* Approximations of Markov chains: [CDPP'09](#approx_markov), [DDGS'18](#krn).

* [[Carathéodory's extension theorem]]: proven using [[probability monads]] (as [[codensity monads]]) in [Van Belle'22](#vb_codensity).

* [[conditional expectation|Conditional expectations]]: first expressed categorically in [Panangaden](#panangaden_condexp)  and [CDPP'09](#approx_markov), then in terms of [[probability monads]] (as [[codensity monads]]) in [Van Belle'23](#vb_martingales) then using [[partial evaluations]] in [Perrone'18](#Perrone_thesis), [FP'20](#pev) and [FGPR'23](#fritz_representable), and finally in [[categories of couplings]] in [Ensarguet-Perrone'23](#ergodic_dagger) and [Perrone-Van Belle'24](#dagger_martingales).

* [[De Finetti's theorem]]: stated, interpreted and proven in terms of [[Markov categories]] with [[probability monads]]. Main results in [Fritz-Gonda-Perrone'21](#fritz_definetti), see also [Moss-Perrone'22](#det_submonad) and [CFGKL](#aldous_hoover) for further context. An analogous result was proven in the [[category of couplings]], [Ensarguet-Perrone'23](#ergodic_dagger). An additional, independent categorical approach is given in [Jacobs-Staton'20](#definetti_limit).

* [[ergodic decomposition|Ergodic decomposition theorem]]: proven for deterministic [[dynamical systems]] using [[Markov categories]] in [Moss-Perrone'23](#markov_ergodic), and extended to the stochastic case using [[Markov categories]] and [[categories of couplings]] in [Ensarguet-Perrone'23](#ergodic_dagger).

* Stochastic versions of [[Gelfand duality]]: [Furber-Jacobs'15](#gelfand_furber) and [Parzygnat'17](#stoch_gelfand_parzygnat).

* Probabilistic graphical models: a categorical study of Bayesian networks [Fong'12](#fong12), a d-separation criterion for Markov categories [Fritz-Klingler'22](#d-sep), a theory of Bayesian networks and Markov random fields [Lorenzin-Zanasi'25](#probabilistic_triangulation).

* [[idempotent completion|Idempotent completion]] of [[BorelStoch]]: a new measure-theoretic result, with several structural consequences, proven in [FGLPS'23](#markov_supports).

* [[imprecise probability|Imprecise probability]] in terms of graded monads and string diagrams: [LC-Staton'25](#imprecise_graded) and [Sarkis-Zanasi'25](#string_graded).

* [[Kantorovich duality]] in terms of [[probability monads]]: [Perrone'18](#Perrone_thesis), [Fritz-Perrone'19](#FPKant), [Fritz-Perrone'20](#orderedkantorovich).

* [[Kolmogorov extension theorem]]: described in terms of [[Markov categories]] in [Fritz-Rischel'20](#fritzrischel), and in terms of [[probability monads]] (as [[codensity monads]]) in [Van Belle'23](#vb_martingales). 

* The [[strong law of large numbers]] in terms of [[Markov categories]] in [FGLPSM'25](#lln).

* [[martingales|Martingales]]: Described in terms of [[probability monads]] (as [[codensity monads]]) in [Van Belle'23](#vb_martingales) and using [[partial evaluations]] in [Perrone'18](#Perrone_thesis). A version of their convergence theorem using the [[category of couplings]] is given in [Perrone-Van Belle'24](#dagger_martingales).

* Multinomial and hypergeometric distributions: described in terms of [[Markov categories]] in [Jacobs'21](#multinomial).

* [[Radon-Nikodym theorem]]: proven using [[probability monads]] (as [[codensity monads]]) in [Van Belle'23](#vb_martingales).

* [[support|Supports]] of [[probability measures]]: studied in terms of [[probability monads]] in [Fritz-Perrone-Rezagholi'21](#monads_supports) and in terms of [[Markov categories]] in [FGLPS'23](#markov_supports)

* Urn models, multinomials, and probability on sets, using category theory, including Markov categories: [Jacobs'21a](#multisets) [Jacobs'21b](#multinomial) [Jacobs'22](#urns_tubes), [Jacobs-Stein'23](#overdrawing), [Jacobs'24](#urn_isometric).

* Kolmogorov and Hewitt-savage's [[zero-one laws]]: proven in terms of [[Markov categories]] in [Fritz-Rischel'20](#fritzrischel), and in [[categories of couplings]] in [Ensarguet-Perrone'23](#ergodic_dagger).

(...)

### Statistics

* Bahadur's theorem on ancillary statistics: proven in terms of Markov categories in [Fritz'20](#fritzmarkov)

* Basu's theorem on minimal [[sufficient statistics]]: proven in terms of Markov categories in [Fritz'20](#fritzmarkov).

* [[Bayesian inverses]]: expressed categorically, with proofs about their core properties and their existence, in [DDGS'18](#krn), [Cho-Jacobs'19](#cd_categories), [Fritz'20](#fritzmarkov), [Parzygnat'24](#retrodiction), and others.

* [[Bayesian updating]]: categorically [Jacobs'23](#pearl_jeffrey), [Jacobs-Zanasi'18](#essential_bayes), and including using Markov categories, [Di Lavore-Román'23](#partial_markov) and [DLRS'25](#partial_markov_ext).

* Blackwell-Sherman-Stein theorem on statistical experiments: proven and generalized beyond the discrete case using [[Markov categories]] in [FGPR'23](#fritz_representable). Additional results in [BP'25](#bohinen).

* Causal inference: using string diagrams [JKZ'18](#causal_surgery), and using Markov categories [Yin'22](#markov_causal).

* Filtering and smoothing for hidden Markov models: described in terms of [[Markov categories]] in [Virgo'23](#filters_virgo), as well as in [FKMSW'24](#hidden_markov).

* Fisher-Neyman factorization theorem for [[sufficient statistics]]: proven in terms of Markov categories in [Fritz'20](#fritzmarkov).

* General results on [[sufficient statistics]]: in terms of Markov categories [Fritz'20](#fritzmarkov), and in terms of [[idempotents]] [Jacobs'23](#idemp_discrete).

* Improper priors for Gaussians, using [[Markov categories]]: [Stein-Samuelson'23](#gauss_nondet).

* [[machine learning|Machine learning]]: [[equivariance]] of [[neural networks]] using [[Markov categories]] in [Cornish'24](#cornish).

(...)

### Information theory

* Characterizations of [[relative entropy]] in the discrete case: [Baez-Fritz-Leinster'11](#entropy_infloss), [Baez-Fritz'14](#entropy_bayes), [Leinster'19](#entropy_short), [Fullwood-Parzygnat'21](#information_loss_stoch). (Quantum case in [Parzygnat'22](#von_neumann), see below.)

* Characterizations of [[relative entropy]] on [[standard Borel spaces]]: [Gagne-Panangaden'18](#entropy_borel).

* [[entropy|Entropy]] in terms of [[operads]]: [Bradley'21](#entropy_operads).

* [[entropy|Entropy]] from the point of view of [[topos theory]]: [Constantin-Döring'20](#entropy_topos).

* [[entropy|Entropy]], [[relative entropy]] and [[data processing inequalities]]: expressed in terms of [[enriched category|enriched]] [[Markov categories]] in [Perrone'24](#markov_entropy).

* A book on the relationship between [[metrics]], [[entropy]] and diversity in ecology, with a category-theoretic mindset: [Leinster'21](#entropy_diversity).

(...)

### Quantum probability and information theory

* Quantum versions of Bayesian inverses: [Coecke-Spekkens'12](#coecke_spekkens12), [Parzygnat-Russo'22](#noncommutative_bayes), [Parzygnat-Buscemi'23](#retrodiction), [Fullwood-Parzygnat'23](#quantum_bayes), [Parzygnat'24](#retrodiction).

* Quantum versions of conditioning and disintegrations:  [Parzygnat'21](#conditional_quantum), [Parzygnat-Russo'23](#noncomm_disintegrations).

* Quantum versions of [[de Finetti's theorem]]: [Staton-Summers'22](#definetti_ned) and [Fritz-Lorenzin'23](#quantum_definetti).

* Categorical descriptions of dilations: [Parzygnat'19](#stinespring) and [GHL'21](#gauguin_dilations).

* Categorical characterization of von Neumann entropy: [Parzygnat'22](#von_neumann).

* Quantum versions of Markov categories: [Parzygnat'20](#quantum_markov) and [Fritz-Lorenzin'23](#quantum_definetti).

(...)


### Probability in computer science

* Bayesian updating in probabilistic programming: [Jacobs'23](#pearl_jeffrey).

* A [[cartesian closed category]] with a [[probability monad]]: [HKSY'17](#QBS), [SSSW'21](#name_gen).

* Stochastic $\lambda$-calculus: [AKM'21](#stoch_lambda).

* Probability monads for probabilistic computation: [Jones-Plotkin'89](#jones_plotkin89), [Jacobs'18](#jacobs_pmonads), [DKPS'2023](#affine_lazy).

* Privacy of name generation: [HKSY'17](#QBS), [SSSW'21](#name_gen), [FGGPS'23](#dilations).

* [[probabilistic programming|Probabilistic programming]] and [[random graphs]]: [AFKKMRSY'24](#graphons).

* Stochastic memoization via monads: [Kaddar-Staton'23](#stoch_memo).

(...)


### Structural results of categorical probability

* Foundational results on [[Markov categories]]: [Golubtsov'99](#golubtsov99), [Cho-Jacobs'19](#cd_categories), [Fritz'20](#fritzmarkov).

* Constructions and analysis of [[categories]] of [[Markov kernels]] and of [[transport plans]]: [Lawvere'62](#Lawvere62), [Chentsov'65](#Chentsov65), [Giry'82](#giry'82), [Panangaden'99](#panangaden_cat_markov), [DDGS'18](#krn), [Perrone'21](#lifting), [Kozen-Silva-Voogd'23](#krn_ext).

* Constructions of free Markov and CD categories: [Fritz-Liang'23](#free_gs).

* Notions of [[conditional independence]] as [[universal properties]]: [Simpson'18](#independence), [Simpson'24](#atomic_sheaf), [Stein'25](#stein_RV).

* Study of joint and marginal distributions for [[probability monads]]: [Fritz-Perrone'18](#bimonoidal_monads).

* Markov categories for [[partial maps]]: [Di Lavore-Román'23](#partial_markov) and [DLRS'25](#partial_markov_ext).

* Connections between [[Markov categories]] and [[categories of couplings]]: [Fritz'20](#fritzmarkov), [Ensarguet-Perrone'23](#ergodic_dagger), [Stein'25](#stein_RV).

* Connections between [[Markov categories]] and [[probability monads]]: [Golubtsov'02](#golubtsov02), [FGPR'23](#fritz_representable), [Moss-Perrone'22](#det_submonad), [FGGPS'23](#dilations), [BP'25](#bohinen).

* Connections between [[Markov category#positivity_and_causality|positive Markov categories]] and [[semicartesian monoidal categories]]: [FGGPS'23](#dilations).

* Construction of [[locale|point-free]] [[probability monads]] (on [[locales]]): [Vickers'11](#vmonad).

* Results expressing [[probability monads]] as [[codensity monads]]: [Avery'16](#avery_giry) and more recently [Van Belle'22](#vb_codensity) with concrete applications to measure theory.

* Constructions of [[probability monads]] on [[metric spaces]], and connections with [[metric space|metric geometry]] and [[Banach spaces]]: [AJK'04](#jung), [Fritz-Perrone'19](#FPKant), [Fritz-Perrone'20](#orderedkantorovich).

* Constructions of [[probability monads]] on [[topological spaces]], and connections with [[functional analysis]]: [Swirszcz'74](#swirszcz), [Giry'82](#giry'82), [Jones-Plotkin'89](#jones_plotkin89), [Heckmann'96](#Heckmann96), [Keimel'08](#radonkeimel), [GLJ'19](#algebras), [Fritz-Perrone-Rezagholi'21](#monads_supports), [Kristel-Peterseim'24](#KP24).

* A monad encoding [[probabilistic point processes]] combining probability and nondeterminism: [Dash-Staton'20](#point_processes).

* [[random variables|Random variables]] in terms of [[sheaves]]: [Simpson'17](#probability_sheaves), [Simpson'24](#atomic_sheaf), [Stein'25](#stein_RV).

(...)




## Related entries

* [[Markov category]]

* [[probability monad]]

* [[synthetic probability theory]]

* [[probability theory]]


## References

(in alphabetical order by author)

* {#jung} Mauricio Alvarez-Manilla, Achim Jung, [[Klaus Keimel]], _The probabilistic powerdomain for stably compact spaces_, Theoretical Computer Science 328, 2004. [Link here](https://www.sciencedirect.com/science/article/pii/S0304397504004074).

* {#graphons} Nathanael L. Ackerman, Cameron E. Freer, Younesse Kaddar, Jacek Karwowski, Sean K. Moss, Daniel M. Roy, Sam Staton, Hongseok Yang, _Probabilistic programming interfaces for random graphs: Markov categories, graphons, and nominal sets_, Proceedings of POPL, 2024. ([arXiv](https://arxiv.org/abs/2312.17127))

* {#avery_giry} Tom Avery, _Codensity and the Giry monad_, Journal of Pure and Applied Algebra, 220(3), 2016.

* {#stoch_lambda} Pedro H. Azevedo de Amorim, Dexter Kozen, Radu Mardare, [[Prakash Panangaden]], Michael Roberts, _Universal semantics for the stochastic $\lambda$-calculus_, Proceedings of LICS, 2021. ([pdf](https://www.cs.mcgill.ca/~prakash/Pubs/lics-2021-1.pdf))

* {#algebraic_markov} Giorgio Bacci, Radu Mardare, [[Prakash Panangaden]], [[Gordon Plotkin]], _An algebraic theory of Markov processes_, Proceedings of LICS, 2018. ([pdf](https://www.cs.mcgill.ca/~prakash/Pubs/Markov-LICS.pdf))

* {#entropy_bayes} [[John Baez]] and [[Tobias Fritz]], _A Bayesian characterization of relative entropy_, Theory and Application of Categories, 29(16), 2014. ([arXiv](https://arxiv.org/abs/1402.3067))

* {#entropy_infloss} [[John Baez]], [[Tobias Fritz]] and [[Tom Leinster]], _A characterization of entropy in terms of information loss_, Entropy 13(2), 2011. ([arXiv](https://arxiv.org/abs/1106.1791))

* {#bohinen} Mika Bohinen and [[Paolo Perrone]], _Categorical algebra of conditional probability_, 2025. ([arXiv](https://arxiv.org/abs/2502.14941))

* {#entropy_operads} Tai-Danae Bradley, _Entropy as a topological operad derivation_, Entropy 23(9), 2021. ([arXiv](https://arxiv.org/abs/2107.09581))

* {#vanbreugel} Franck van Breugel, _The metric monad for probabilistic nondeterminism_, unpublished, 2005. ([pdf](http://www.cse.yorku.ca/~franck/research/drafts/monad.pdf))

* {#approx_markov} Philippe Chaput, Vincent Danos, [[Prakash Panangaden]] and [[Gordon Plotkin]], _Approximating Markov processes by averaging_, Proceedings of ICALP 2009. ([pdf](https://www.cs.mcgill.ca/~prakash/Pubs/new_plain.pdf))

* {#aldous_hoover} Leihao Chen, [[Tobias Fritz]], Tomáš Gonda, Andreas Klingler, Antonio Lorenzin, _The Aldous-Hoover Theorem in Categorical Probability_, ([arXiv:2411.12840](https://arxiv.org/abs/2411.12840))

* {#Chentsov65} N. N. Chentsov, _The categories of mathematical statistics_, Dokl. Akad. SSSR 164, 1965.

* {#cd_categories} Kenta Cho, [[Bart Jacobs]], _Disintegration and Bayesian Inversion via String Diagrams_, Mathematical Structures of Computer Science 29, 2019. ([arXiv:1709.00322](https://arxiv.org/abs/1709.00322))

* {#structuralism} [[Bob Coecke]], Eric Oliver Paquette, Dusko Pavlovic, _Classical and quantum structuralism_, ([arXiv:0904.1997](https://arxiv.org/abs/0904.1997))

* {#coecke_spekkens12} [[Bob Coecke]] and Robert W. Spekkens, _Picturing classical and quantum Bayesian inference_, Synthese, 186(3), 2012. ([arXiv](https://arxiv.org/abs/1102.2368))

* {#entropy_topos} Carmen Constantin and Andreas Döring, _A topos-theoretic notion of entropy_, 2020. ([arXiv](https://arxiv.org/abs/2006.03139))

* {#cornish} Rob Cornish, _Stochastic Neural Network Symmetrization in Markov Categories_, 2024. ([arXiv](https://arxiv.org/abs/2406.11814))

* {#krn} Fredrik Dahlqvist, Vincent Danos, Ilias Garnier, and Alexandra Silva, _Borel kernels and
their approximation, categorically_. In MFPS 34: Proceedings of the Thirty-Fourth Conference on the Mathematical Foundations of Programming Semantics, volume 341, 91–119, 2018.  [arXiv](https://arxiv.org/abs/1803.02651).

* {#affine_lazy} Swaraj Dash, Younesse Kaddar, Hugo Paquet and Sam Staton, _Affine monads and lazy structures for Bayesian programming_, Proceedings of POPL, 2023. ([pdf](https://www.cs.ox.ac.uk/people/hugo.paquet/lazyppl.pdf))

* {#point_processes} Swaraj Dash and Sam Staton, _A monad for probabilistic point processes_, Proceedings of Applied Category Theory, 2020. ([pdf](https://cgi.cse.unsw.edu.au/~eptcs/paper.cgi?ACT2020:61.pdf))

* {#partial_markov} Elena Di Lavore and Mario Román, _Evidential Decision Theory via Partial Markov Categories_, Proceedings of LICS, 2023. ([arXiv](https://arxiv.org/abs/2301.12989))

* {#partial_markov_ext} Elena Di Lavore, Mario Román and Paweł Sobociński, _Partial Markov Categories_, 2025. ([arXiv](https://arxiv.org/abs/2502.03477))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)

* {#fong12} [[Brendan Fong]], _Causal theories: A categorical perspective on Bayesian networks_, master thesis, University of Oxford, 2012. ([arXiv](https://arxiv.org/abs/1301.6201))

* {#2-entropy} James Fullwood, _On a 2-relative entropy_, Entropy 24(1), 2022. ([arXiv](https://arxiv.org/abs/2112.03582))

* {#retrodiction} [[Arthur J. Parzygnat]], _Reversing information flow: retrodiction in semicartesian categories_, 2024. ([arXiv](https://arxiv.org/abs/2401.17447))

* {#quantum_bayes} James Fullwood and [[Arthur J. Parzygnat]], _From time-reversal symmetry to quantum Bayes rules_, PRX Quantum 4, 2023. ([arXiv](https://arxiv.org/abs/2212.08088))

* {#quantum_states_time} James Fullwood and [[Arthur J. Parzygnat]], _On quantum states over time_, Proceedings of the Royal Society A 478, 2022. ([arXiv](https://arxiv.org/abs/2202.03607))

* {#information_loss_stoch} James Fullwood and [[Arthur J. Parzygnat]], _The information loss of a stochastic map_, Entropy 2021, 23(8), 2021. ([arXiv](https://arxiv.org/abs/2107.01975))

* {#gelfand_furber} Robert W. J. Furber and [[Bart Jacobs]]: _From Kleisli Categories to Commutative C*-algebras: Probabilistic Gelfand Duality_, LMCS 11(2), 2015. ([arXiv](https://arxiv.org/abs/1303.1115))

* {#fritzmarkov} [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_, Advances of Mathematics 370, 2020. ([arXiv:1908.07021](http://arxiv.org/abs/1908.07021))

* {#weaklymarkov} [[Tobias Fritz]], [[Fabio Gadducci]], [[Paolo Perrone]] and Davide Trotta, _Weakly Markov categories and weakly affine monads_, Proceedings of CALCO, LIPIcs 10, 2023. ([arXiv](https://arxiv.org/abs/2303.14049))

* {#oplax_cartesian} [[Tobias Fritz]], [[Fabio Gadducci]], Davide Trotta, Andrea Corradini, _From gs-monoidal to oplax-cartesian categories: constructions and functorial completeness_, Applied Categorical Structures 31, 42, 2023. ([arXiv](https://arxiv.org/abs/2205.06892))

* {#dilations} [[Tobias Fritz]], Tomáš Gonda, Nicholas Gauguin Houghton-Larsen, [[Paolo Perrone]] and Dario Stein, _Dilations and information flow axioms in categorical probability_. Mathematical Structures in Computer Science, 2023. ([arXiv:2211.02507](https://arxiv.org/abs/2211.02507)).

* {#markov_supports} [[Tobias Fritz]], Tomáš Gonda, Antonio Lorenzin, [[Paolo Perrone]], Dario Stein, _Absolute continuity, supports and idempotent splitting in categorical probability_, ([arXiv:2308.00651](https://arxiv.org/abs/2308.00651))

* {#fritz_definetti} [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], _De Finetti's theorem in categorical probability_. Journal of Stochastic Analysis, 2021. ([arXiv:2105.02639](https://arxiv.org/abs/2105.02639))

* {#fritz_representable} [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], Eigil Fjeldgren Rischel, _Representable Markov categories and comparison of statistical experiments in categorical probability_, Theoretical Computer Science 961, 2023. ([arXiv:2010.07416](https://arxiv.org/abs/2010.07416))

* {#lln} Tobias Fritz, Tomáš Gonda, Antonio Lorenzin, Paolo Perrone and Areeb Shah Mohammed, _Empirical Measures and Strong Laws of Large Numbers in Categorical Probability_, 2025 ([arXiv:2503.21576](https://arxiv.org/abs/2503.21576))

* {#d-sep} [[Tobias Fritz]] and Andreas Klingler, _The d-separation criterion in Categorical Probability_, Journal of Machine Learning Research 24(46), 2023. ([arXiv](https://arxiv.org/abs/2207.05740))

* {#hidden_markov} [[Tobias Fritz]], Andreas Klingler, Drew McNeely, Areeb Shah-Mohammed and Yuwen Wang, _Hidden Markov models and the Bayes filter in categorical probability_, 2024. ([arXiv](https://arxiv.org/abs/2401.14669))

* {#free_gs} [[Tobias Fritz]], [[Wendong Liang]], _Free gs-monoidal categories and free Markov categories_, Applied Categorical Structures 31, 21, 2023. ([arXiv:2204.02284](https://arxiv.org/abs/2204.02284))

* {#quantum_definetti} [[Tobias Fritz]] and Antonio Lorenzin, _Involutive Markov categories and the quantum de Finetti theorem_, 2023. ([arXiv](https://arxiv.org/abs/2312.09666))

* {#orderedkantorovich} [[Tobias Fritz]] and [[Paolo Perrone]], _Stochastic order on metric spaces and the ordered Kantorovich monad_, Advances in Mathematics 366, 2020. ([arXiv:1808.09898](https://arxiv.org/abs/1808.09898))

* {#pev} [[Tobias Fritz]] and [[Paolo Perrone]], _Monads, partial evaluations, and rewriting_, Proceedings of MFPS, 2020. ([arXiv](https://arxiv.org/abs/1810.06037))

* {#FPKant} [[Tobias Fritz]] and [[Paolo Perrone]], _A Probability Monad as the Colimit of Spaces of Finite Samples_, Theory and Applications of Categories 34, 2019. ([arXiv:1712.05363](https://arxiv.org/abs/1712.05363))

* {#bimonoidal_monads} [[Tobias Fritz]], [[Paolo Perrone]], _Bimonoidal Structure of Probability Monads_, Proceedings of MFPS, 2018, ([arXiv:1804.03527](https://arxiv.org/abs/1804.03527))

* {#monads_supports} [[Tobias Fritz]], [[Paolo Perrone]], Sharwin Rezagholi, _Probability, valuations, hyperspace: Three monads on Top and the support as a morphism_, Mathematical Structures in Computer Science 31(8), 2021. ([arXiv:1910.03752](https://arxiv.org/abs/1910.03752))

* {#fritzrischel} [[Tobias Fritz]] and Eigil Fjeldgren Rischel, _Infinite products and zero-one laws in categorical probability_, Compositionality 2(3) 2020. ([arXiv:1912.02769](http://arxiv.org/abs/1912.02769))

* {#entropy_borel} Nicolas Gagne and [[Prakash Panangaden]], _A categorical characterization of relative entropy on standard Borel spaces_, ENTCS 336, 2018. ([arXiv](https://arxiv.org/abs/1703.08853))

* {#gauguin_dilations} Nicholas Gauguin Houghton-Larsen, _A Mathematical Framework for Causally Structured Dilations and its Relation to Quantum Self-Testing_, PhD thesis, University of Copenhagen, 2021. ([arXiv](https://arxiv.org/abs/2103.02302))

* {#giry82} Michèle Giry, _A categorical approach to probability theory_, Categorical aspects of topology and analysis, Lecture notes in Mathematics 915, Springer, 1982.

* {#golubtsov99} Peter V. Golubtsov, _Axiomatic description of categories of information converters_, Problemy Peredachi Informatsii (Problems in Information Transmission) 35(3), 1999. 

* {#golubtsov02} Peter V. Golubtsov, _Monoidal Kleisli category as a background for information transformers theory_. Information Theory and Information Processing 2, 2002.

* {#golubtsov04} Peter V. Golubtsov, _Information transformers: category-theoretical structure, informativeness, decision-making problems_, Hadronic Journal Supplements 19(3), 2004.

* {#golubtsov_mosaliuk02} Peter V. Golubtsov and Stepan S. Moskaliuk, _Method of additional structures on the objects of a monoidal Kleisli category as a background for information transformers theory_, Hadronic Journal 25(2), 2002.

* {#algebras} [[Jean Goubault-Larrecq]] and Xiaodong Jia, _Algebras of the extended probabilistic powerdomain monad_, ENTCS 345, 2019
([doi:10.1016/j.entcs.2019.07.015](https://doi.org/10.1016/j.entcs.2019.07.015))

* {#Heckmann96} Reinhold Heckmann, _Spaces of valuations_, Papers on General Topology and Ap-plications, 1996 ([doi:10.1111/j.1749-6632.1996.tb49168.x](https://doi.org/10.1111/j.1749-6632.1996.tb49168.x),[pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.45.5845&rep=rep1&type=pdf))

* {#stoch_memo} Younesse Kaddar and Sam Staton, _A model of stochastic memoization and name generation in probabilistic programming: categorical semantics via monads on presheaf categories_, Proceedings of MFPS, 2023. ([arXiv](https://arxiv.org/abs/2309.09467))

* {#QBS} [[Chris Heunen]], Ohad Kammar, [[Sam Staton]] and Hongseok Yang, _A convenient category for higher-order probability theory_, Proceedings of LICS 2017. ([arXiv](https://arxiv.org/abs/1701.02547))

* {#urn_isometric} [[Bart Jacobs]], _Drawing from an Urn is Isometric_, Proceedings of FoSSaCS, 2024. ([pdf](http://www.cs.ru.nl/B.Jacobs/PAPERS/draw-isometries.pdf))

* {#pearl_jeffrey} [[Bart Jacobs]], _Pearl's and Jeffrey's Update as Modes of Learning in Probabilistic Programming_ ([arXiv:2309.07053](https://arxiv.org/abs/2309.07053))

* {#urns_tubes} [[Bart Jacobs]], _Urns & Tubes_, Compositionality 4(4), 2022. ([arXiv](https://arxiv.org/abs/2110.02155))

* {#idemp_discrete} [[Bart Jacobs]], _Sufficient statistics and split idempotents in discrete probability theory_, Proceedings of MFPS, 2023. ([arXiv](https://arxiv.org/abs/2212.09191))

* {#multinomial} [[Bart Jacobs]], _Multinomial and Hypergeometric Distributions in Markov Categories_, Proceedings of MFPS 2021. ([arXiv](https://arxiv.org/abs/2112.14044))

* {#multisets} [[Bart Jacobs]], _From Multisets over Distributions to Distributions over Multisets_, Proceedings of LICS, 2021. ([arXiv](https://arxiv.org/abs/2105.06908))

* {#jacobs_pmonads} [[Bart Jacobs]], _From probability monads to commutative effectuses_, Journal of Logical and Algebraic Methods in Programming 94, 2018. 
([doi:10.1016/j.jlamp.2016.11.006](https://doi.org/10.1016/j.jlamp.2016.11.006))

* {#parameter_learning} [[Bart Jacobs]], _Categorical aspects of parameter learning_, 2018. ([arXiv](https://arxiv.org/abs/1810.05814))

* {#exact_inference} [[Bart Jacobs]], _A Channel-based Exact Inference Algorithm for Bayesian Networks_, 2018. ([arXiv](https://arxiv.org/abs/1804.08032))

* {#conj_priors} [[Bart Jacobs]], _A Channel-Based Perspective on Conjugate Priors_, 2017. ([arXiv:1707.00269](https://arxiv.org/abs/1707.00269))

* {#hypernormalization} [[Bart Jacobs]], _Hyper Normalisation and Conditioning for Discrete Probability Distributions_, LMCS 13, 2017. ([arXiv](https://arxiv.org/abs/1607.02790))

* {#causal_surgery} [[Bart Jacobs]], [[Aleks Kissinger]], [[Fabio Zanasi]], _Causal Inference by String Diagram Surgery_, ([arXiv:1811.08338](https://arxiv.org/abs/1811.08338))

* {#definetti_limit} [[Bart Jacobs]], [[Sam Staton]], _De Finetti's construction as a categorical limit_, Proceedings of CMCS, 2021. ([arXiv:2003.01964](https://arxiv.org/abs/2003.01964))

* {#overdrawing} [[Bart Jacobs]] and [[Dario Stein]], _Overdrawing Urns using Categories of Signed Probabilities_, Proceedings of Applied Category Theory, EPTCS 397, 2023. ([arXiv](https://arxiv.org/abs/2312.12453))

* {#essential_bayes} [[Bart Jacobs]], [[Fabio Zanasi]], _The Logical Essentials of Bayesian Reasoning_, ([arXiv:1804.01193](https://arxiv.org/abs/1804.01193))

* {#bayes_adjoint} [[Bart Jacobs]], [[Fabio Zanasi]], and Octavio Zapata, _Bayesian Factorisation as Adjoint, [abstract](http://wadt18.cs.rhul.ac.uk/submissions/WADT18A33.pdf)

* {#jones_plotkin89} Claire Jones and [[Gordon Plotkin]], _A probabilistic powerdomain of evaluations_, Procedings of LICS, 1989. ([doi](https://doi.org/10.1109/LICS.1989.39173))

* {#radonkeimel} [[Klaus Keimel]], _The monad of probability measures over compact ordered spaces and its Eilenberg-Moore algebras_, Topology and its Applications, 2008 ([doi:10.1016/j.topol.2008.07.002](https://doi.org/10.1016/j.topol.2008.07.002))

* {#stone_markov} Dexter Kozen, Kim G. Larsen, Radu Mardare, [[Prakash Panangaden]], _Stone duality for Markov processes_, Proceedings of LICS, 2013. ([pdf](https://www.cs.mcgill.ca/~prakash/Pubs/mfcs2013.pdf))

* {#markov_logid} Dexter Kozen, Radu Mardare, [[Prakash Panangaden]], _Stone duality for Markov processes_, Proceedings of MFCS, 2013. ([pdf](https://www.cs.mcgill.ca/~prakash/Pubs/lics2013.pdf))

* {#krn_ext} Dexter Kozen, Alexandra Silva, Erik Voogd, _Joint Distributions in Probabilistic Semantics_, MFPS 2023. ([arXiv](https://arxiv.org/abs/2309.06913))

* {#KP24} Peter Kristel, Benedikt Peterseim, _A topologically enriched probability monad on the cartesian closed category of CGWH spaces_. ([arXiv](https://arxiv.org/abs/2404.08430))

* {#Lawvere62} [[Bill Lawvere]], _The category of probabilistic mappings_, ms. 12 pages, 1962 
([[lawvereprobability1962.pdf:file]])

* {#entropy_short} Tom Leinster, _A short characterization of relative entropy_, Journal of Mathematical Physics 60, 2019. ([arXiv](https://arxiv.org/abs/1712.04903))

* {#entropy_diversity} Tom Leinster, _Entropy and Diversity_, Cambridge University Press, 2021. 

* {#imprecise_graded} Jack Liell-Cock and [[Sam Staton]], _Compositional imprecise probability_, POPL 2025. ([arXiv](https://arxiv.org/abs/2405.09391))

* {#probabilistic_triangulation} Antonio Lorenzin and [[Fabio Zanasi]], _An Algebraic Approach to Moralisation and Triangulation of Probabilistic Graphical Models_, 2025. ([arXiv](https://arxiv.org/abs/2503.11820))

* {#wasserstein_algebras} Radu Mardare, [[Prakash Panangaden]], [[Gordon Plotkin]], _Free complete Wasserstein algebras_, LMCS 14, 2018. ([pdf](https://www.cs.mcgill.ca/~prakash/Pubs/fcwa.pdf))

* {#quantitative_reasoning} Radu Mardare, [[Prakash Panangaden]], [[Gordon Plotkin]], _Quantitative algebraic reasoning_, Proceedings of LICS, 2016. ([pdf](https://www.cs.mcgill.ca/~prakash/Pubs/lics2016.pdf))

* Cristina Matache, Sean Moss, Sam Staton, Ariadne Si Suo, _Denotational semantics for languages for inference: semirings, monads, and tensors_, Proceedings of LAFI, 2023. ([arXiv](https://arxiv.org/abs/2312.16694))

* {#moggi89} [[Eugenio Moggi]], *Computational lambda-calculus and monads*, Proceedings of LICS, 1989. ([doi](https://doi.org/10.1109/LICS.1989.39155))

* {#markov_ergodic} Sean Moss and [[Paolo Perrone]], _A category-theoretic proof of the ergodic decomposition theorem_, Ergodic Theory and Dynamical Systems, 2023. ([arXiv:2207.07353](https://arxiv.org/abs/2207.07353))

* {#det_submonad} Sean Moss, [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))

* {#panangaden_cat_markov} [[Prakash Panangaden]], _The category of Markov kernels_, ENTCS, 1999. ([full text](https://www.sciencedirect.com/science/article/pii/S1571066105806024))

* {#panangaden_markov} [[Prakash Panangaden]], _Labelled Markov processes_, Imperial College Press, 2009.

* {#panangaden_condexp} [[Prakash Panangaden]], _A categorical view of conditional expectation_, ([slides](http://math.ucr.edu/home/baez/mathematical/ACTUCR/Panagaden_Conditional_Expectation.pdf))

* {#von_neumann} [[Arthur J. Parzygnat]], _A functorial characterization of von Neumann entropy_, Cahiers de Topologie et de Géométrie Différentielle Catégorique LXIII(1), 2022. ([arXiv](https://arxiv.org/abs/2009.07125))

* {#conditional_quantum} [[Arthur J. Parzygnat]], _Conditional distributions for quantum systems_, EPTCS 343, 2021. ([arXiv](https://arxiv.org/abs/2102.01529))

* {#quantum_markov} [[Arthur J. Parzygnat]], _Inverses, disintegrations, and Bayesian inversion in quantum Markov categories_, 2020. ([arXiv](https://arxiv.org/abs/2001.08375))

* {#stinespring} [[Arthur J. Parzygnat]], _Stinespring's construction as an adjunction_, Compositionality 1(2), 2019. ([arXiv](https://arxiv.org/abs/1807.02533))

* {#stoch_gelfand_parzygnat} [[Arthur J. Parzygnat]], _Discrete probabilistic and algebraic dynamics: a stochastic commutative Gelfand-Naimark Theorem_, 2017. ([arXiv](https://arxiv.org/abs/1708.00091))

* {#retrodiction} [[Arthur J. Parzygnat]], Francesco Buscemi, _Axioms for retrodiction: achieving time-reversal symmetry with a prior_, Quantum 7(1013), 2023. [arXiv](https://arxiv.org/abs/2210.13531)

* {#noncomm_disintegrations} [[Arthur J. Parzygnat]], Benjamin P. Russo, _Non-commutative disintegrations: existence and uniqueness in finite dimensions_, Journal of Noncommutative Geometry 17(3), 2023. ([arXiv](https://arxiv.org/abs/1907.09689))

* {#noncommutative_bayes} [[Arthur J. Parzygnat]] and Benjamin P. Russo, _A noncommutative Bayes theorem_, Linear Algebra Applications 644, 2022. ([arXiv](https://arxiv.org/abs/2005.03886))

* {#markov_entropy} [[Paolo Perrone]], _Markov Categories and Entropy_, IEEE Transactions on Information Theory 70(3), 2024. ([arXiv](https://arxiv.org/abs/2212.11719))

* {#dagger_martingales} [[Paolo Perrone]] and Ruben Van Belle, _Convergence of martingales via enriched dagger categories_, 2024. ([arXiv](https://arxiv.org/abs/2404.15191))

* {#lifting} [[Paolo Perrone]], _Lifting couplings in Wasserstein spaces_, 2021. ([arXiv](https://arxiv.org/abs/2110.06591))

* {#Perrone_thesis} [[Paolo Perrone]], _Categorical Probability and Stochastic Dominance in Metric Spaces_, 2018 ([thesis](http://www.paoloperrone.org/phdthesis.pdf))

* {#name_gen} Marcin Sabok, Sam Staton, Dario Stein, Michael Wolman, _Probabilistic Programming Semantics for Name Generation_, Proceedings of POPL, 2021. ([arXiv](https://arxiv.org/abs/2007.08638))

* {#probability_sheaves} [[Alex Simpson]], _Probability Sheaves and the Giry Monad_, 2017 ([pdf](https://coalg.org/mfps-calco2017/calco-papers/calco2017-1.pdf))

* {#independence} [[Alex Simpson]], _Category-theoretic structure for independence and conditional independence_, ENTCS, 2018. ([link](https://www.sciencedirect.com/science/article/pii/S1571066118300318))

* {#atomic_sheaf} [[Alex Simpson]], _Equivalence and Conditional Independence in Atomic Sheaf Logid_, Proceedings of LICS, 2024. ([arXiv](https://arxiv.org/abs/2405.11073))

* {#string_graded} Ralph Sarkis and [[Fabio Zanasi]], _String Diagram for Graded Monoidal Theories with an Application to Imprecise Probability_, 2025. ([arXiv](https://arxiv.org/abs/2501.18404))

* {#definetti_ned} Sam Staton and Ned Summers, _Quantum de Finetti Theorems as Categorical Limits, and Limits of State Spaces of C*-algebras_, Proceedings of Quantum Physics and Logic, 2022. ([arXiv](https://arxiv.org/abs/2207.05832))

* {#stein_RV} Dario Stein, _Random Variables, Conditional Independence and Categories of Abstract Sample Spaces_, 2025. ([arXiv](https://arxiv.org/abs/2503.02477))

* {#gauss_nondet} Dario Stein and Richard Samuelson, _A Category for unifying Gaussian Probability and Nondeterminism_, Proceedings of CALCO, LIPIcs 10, 2023. ([arXiv](https://arxiv.org/abs/2204.14024))

* {#exact_cond} Dario Stein and [[Sam Staton]], _Probabilistic Programming with Exact Conditions_, JACM, 2023. ([arXiv](https://arxiv.org/abs/2312.17141))

* {#swirszcz} T. Swirszcz, _Monadic functors and convexity_, Bulletin de l'Academie Polonaise des Sciences 22, 1974 ([pdf](https://www.fuw.edu.pl/~kostecki/scans/swirszcz1974.pdf))

* {#vb_martingales} Ruben Van Belle, _A categorical treatment of the Radon-Nikodym theorem and martingales_, 2023. ([arXiv](https://arxiv.org/abs/2305.03421))

* {#vb_caratheodory} Ruben Van Belle, _A categorical proof of the Carathéodory extension theorem_, 2022. ([arXiv](https://arxiv.org/abs/2210.01720))

* {#vb_codensity} Ruben Van Belle, _Probability monads as codensity monads_, Theory and Applications of Categories, 38(21), 2022. ([arXiv](https://arxiv.org/abs/2111.01250))

* {#vmonad} [[Steve Vickers]], _A monad of valuation locales_, 2011. [Link here](https://www.cs.bham.ac.uk/~sjv/Riesz.pdf).

* {#filters_virgo} Nathaniel Virgo, _Unifilar Machines and the Adjoint Structure of Bayesian Filtering_, Proceedings of ACT, 2023. ([arXiv](https://arxiv.org/abs/2305.02826))

* {#markov_causal} Yimu Yin, Jiji Zhang, _Markov categories, causal theories, and the do-calculus_, 2022. ([arXiv](https://arxiv.org/abs/2204.04821))





(...more to add...)


category: probability

[[!redirects category-theoretic probability]]
[[!redirects category-theoretic approach to probability theory]]
[[!redirects categorical approach to probability theory]]
[[!redirects categorical approaches to probability theory]]
[[!redirects categorical probability]]
[[!redirects categorical probability theory]]
[[!redirects categorical probability and statistics]]
[[!redirects synthetic probability]]
[[!redirects synthetic probability theory]]



