+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

De Finetti's theorem is one of the central results of [[probability theory]], and usually refers to any of the following related statements:

* Every [[exchangeable probability measure]] on an [[infinite product]] is a unique [[mixture]] of [[iid]] ones. 
* Every infinite sequence of [[exchangeable random variables]] exhibits [[conditional independence]] given the [[empirical distribution]].
* Every infinite sequence of [[exchangeable random variables]] exhibits [[conditional independence]] given the [[exchangeable sigma-algebra]]. 

The statement involves [[mixtures]] of [[probability measures]], and so probability measures *over* probability measures. This recursive construction is one of the main motivations for introducing [[probability monad|monads in probability theory]].
Indeed, [[category-theoretic approaches to probability theory|categorically]], the theorem can equivalently be expressed as follows:

* The [[Giry monad]] is the [[limit]] of an [[exchangeable]] process in the category of [[Markov kernels]].


## Motivation

There are several ways of motivating de Finetti's theorem. 
Here is one, which is very close to de Finetti's original motivation, as explained in his original paper ([de Finetti'29](#definetti_og)).

Consider a repeated experiment where we are uncertain about the distribution. For the simplest possible example, imagine repeatedly flipping a coin, but without knowing in advance the bias of the coin.
One may be tempted to assume that the coin flips are [[stochastic independence|independent]], since "a coin has no memory". However, this is not quite the case:

* What we can say is that the coin flips are [[exchangeable]], since the coin is always the same, and so every flip, and each subsequence of flips, follows the same distribution.
* However, in general [[stochastic independence|independence]] fails: *there is* hidden information in past flips about future flips: by flipping the coin repeatedly, we can get more and more certain about the coin's bias. (For example, if we keep getting "heads", we may start suspecting that the coin is not fair.)
* If we instead *know exactly* the bias of the coin, there is no more hidden information that past flips have about future ones. Therefore, *given the bias of the coin*, the flips are [[conditionally independent]].

De Finetti's theorem says precisely that for every [[exchangeable]] process we have [[conditional independence]] of the variables given their [[empirical distribution|distribution]].


## In measure-theoretic probability

(...)

## In Markov categories

(...)

## In dagger categories

(For now, see [here](#ergodic_dagger).)

## Quantum versions

(For now, see the references.)


## See also 

* [[probability theory]], [[categorical probability]]
* [[infinitary tensor product]], [[Kolmogorov extension theorem]]
* [[Giry monad]], [[probability monad]], [[Markov category]]
* [[Hewitt-Savage zero-one law]], [[law of large numbers]]
* [[exchangeability]], [[limit]], [[permutation]]
* [[ergodicity]], [[ergodic decomposition theorem]]

* Wikipedia, [de Finetti's theorem](https://en.wikipedia.org/wiki/De_Finetti%27s_theorem)


## References

The original paper by de Finetti:

* {#definetti_og} [[Bruno de Finetti]], _Funzione caratteristica di un fenomeno aleatorio_ (*The characteristic function of a random phenomenon*), Atti del Congresso Internazionale dei Matematici: Bologna, 3-10 settembre 1928 (1929), pages 179-290. ([Full text in Italian](https://docplayer.it/24159-Funzione-caratteristica-di-un-fenomeno-aleatorio.html), [English translation](https://arxiv.org/abs/1512.01229))

Category-theoretic accounts:

* {#definetti_limit} [[Bart Jacobs]], [[Sam Staton]], _De Finetti's construction as a categorical limit_, Proceedings of CMCS, 2021. ([arXiv:2003.01964](https://arxiv.org/abs/2003.01964))

* {#fritz_definetti} [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], _De Finetti's theorem in categorical probability_. Journal of Stochastic Analysis, 2021. ([arXiv:2105.02639](https://arxiv.org/abs/2105.02639))

* {#det_submonad} Sean Moss, [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))

* {#fritz_representable} [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], Eigil Fjeldgren Rischel, _Representable Markov categories and comparison of statistical experiments in categorical probability_, Theoretical Computer Science 961, 2023. ([arXiv:2010.07416](https://arxiv.org/abs/2010.07416))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)


For the quantum case:

* {#definetti_ned} [[Sam Staton]] and Ned Summers, _Quantum de Finetti Theorems as Categorical Limits, and Limits of State Spaces of $C^\ast$-algebras_, Proceedings of Quantum Physics and Logic, 2022. ([arXiv](https://arxiv.org/abs/2207.05832))

* {#quantum_definetti} [[Tobias Fritz]] and Antonio Lorenzin, _Involutive Markov categories and the quantum de Finetti theorem_, 2023. ([arXiv](https://arxiv.org/abs/2312.09666))


Introductory videos:

* [[Tobias Fritz]], _Categorical Probability and the de Finetti theorem_, New York Category Seminar, 2021. ([YouTube](https://www.youtube.com/watch?v=vqyYDHGnDqE))

* [[Paolo Perrone]], _Markov categories: a tutorial_. Applied Category Theory (ACT) 2023, tutorial video. De Finetti's theorem starting at time 1:16:30. ([YouTube](https://youtu.be/9U5w3EMHio8?feature=shared&t=4590))

* [[Paolo Perrone]], _Universal Properties in Probability Theory_. Keynote talk, Category Theory (CT) 2023. De Finetti theorem starting at time 39:25 ([YouTube](https://youtu.be/gmSlbgmLyVQ?feature=shared&t=2364))

* [[Antonio Lorenzin]], _Involutive Markov categories and the quantum de Finetti theorem_, Oxford Advanced Seminar on Informatic Structures (OASIS), 2023. ([YouTube](https://www.youtube.com/watch?v=OaGzf3KUkTY))


category: probability


[[!redirects de Finetti theorem]]
[[!redirects De Finetti's theorem]]
[[!redirects De Finetti theorem]]
[[!redirects deFinetti's theorem]]
[[!redirects deFinetti theorem]]
[[!redirects DeFinetti's theorem]]
[[!redirects DeFinetti theorem]]