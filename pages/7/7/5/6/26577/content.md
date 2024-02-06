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

In elementary [[probability theory]], [[Bayes' formula]] refers to a version of the formula 
$$
   P(A)\,P(B|A) \,=\, P(B)\,P(A|B)
   \,,
$$
and relates the [[conditional probability]] of $B$ given $A$ to the one of $A$ given $B$.

From the [[category-theoretic probability|category-theoretic point of view]], this formula expresses a duality, sometimes called **Bayesian inversion**, which often gives rise to a [[dagger category|dagger structure]].


## Intuition

In logical reasoning, implications in general cannot be reversed: $A \to B$, alone, does not imply $B\to A$. 

In [[probability theory]], instead, conditional statements exhibit a [[duality]] which is absent in pure logical reasoning.

Consider for example a city in which *all taxis are yellow*. (The implication is $taxi\to yellow$.)
If we see a yellow car, of course we can't be sure it's a taxi. However, it's *more likely* that it's a taxi compared to a randomly colored car. This increase in likelihood is larger if the fraction of yellow cars is small. Indeed, [[Bayes' rule]] says that 
$$
P(taxi|yellow) = \frac{P(yellow\,taxi)}{P(yellow)} = \frac{P(taxi)}{P(yellow)} .
$$

More generally, in a city where *most* taxis are yellow, there is a high conditional probability that a given taxi is yellow,
$$
P(yellow|taxi) .
$$
The higher this probability is, the higher is the probability that a given yellow car is a taxi, again according to [[Bayes' rule]]:
$$
P(taxi|yellow) = \frac{P(yellow\,taxi)}{P(yellow)} = \frac{P(taxi)\,P(yellow|taxi)}{P(yellow)}
$$

In [[categorical probability]], this phenomenon can be modeled by saying that to each "conditional" morphism in the form $\{taxi, not\,taxi\}\to\{colors\,of\,cars\}$ there corresponds a canonical morphism $\{colors\,of\,cars\}\to\{taxi, not\,taxi\}$, called the *Bayesian inverse*.

In some cases, this symmetry gives rise to a [[dagger category]].

## In traditional probability theory

(...)

### Discrete case

(...)

### Measure-theoretic case

For now see [[Markov kernel#bayesian_inversion]].

(...)


## In categorical probability

(...)

### In Markov categories

For now see [[Markov category#conditionals]].

(...)

### In dagger categories

For now see [[category of couplings]].

(...)


## Quantum versions

(...)


## See also

* [[categorical probability]], [[Markov category]]

* [[transport plan]], [[category of couplings]]

* [[Markov kernel]], [[stochastic map]], [[Stoch]]

* [[conditional probability]], [[conditional expectation]]

* [[probability theory]], [[statistics]], [[Bayesian statistics]]

* [[dagger category]]



## References

For categorical probability:

* {#fritzmarkov} [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_, Advances of Mathematics 370, 2020. ([arXiv:1908.07021](http://arxiv.org/abs/1908.07021))

* {#cd_categories} Kenta Cho, Bart Jacobs, _Disintegration and Bayesian Inversion via String Diagrams_, Mathematical Structures of Computer Science 29, 2019. ([arXiv:1709.00322](https://arxiv.org/abs/1709.00322))

* Dario Stein and [[Sam Staton]], _Probabilistic Programming with Exact Conditions_, JACM, 2023. ([arXiv](https://arxiv.org/abs/2312.17141))

* Noé Ensarguet and [[Paolo Perrone]], _Categorical probability spaces, ergodic decompositions_, and transitions to equilibrium, 2023. ([arXiv:2310.04267](https://arxiv.org/abs/2310.04267))


For the quantum case:

* {#coecke_spekkens12} [[Bob Coecke]] and Robert W. Spekkens, _Picturing classical and quantum Bayesian inference_, Synthese, 186(3), 2012. ([arXiv](https://arxiv.org/abs/1102.2368))

* {#quantum_markov} [[Arthur J. Parzygnat]], _Inverses, disintegrations, and Bayesian inversion in quantum Markov categories_, 2020. ([arXiv](https://arxiv.org/abs/2001.08375))

* {#noncommutative_bayes} [[Arthur J. Parzygnat]] and Benjamin P. Russo, _A noncommutative Bayes theorem_, Linear Algebra Applications 644, 2022. ([arXiv](https://arxiv.org/abs/2005.03886))

* {#conditional_quantum} [[Arthur J. Parzygnat]], _Conditional distributions for quantum systems_, EPTCS 343, 2021. ([arXiv](https://arxiv.org/abs/2102.01529))

* {#retrodiction} [[Arthur J. Parzygnat]], Francesco Buscemi, _Axioms for retrodiction: achieving time-reversal symmetry with a prior_, Quantum 7(1013), 2023. [arXiv](https://arxiv.org/abs/2210.13531)

* {#quantum_bayes} James Fullwood and [[Arthur J. Parzygnat]], _From time-reversal symmetry to quantum Bayes rules_, PRX Quantum 4, 2023. ([arXiv](https://arxiv.org/abs/2212.08088))

* {#noncomm_disintegrations} [[Arthur J. Parzygnat]], Benjamin P. Russo, _Non-commutative disintegrations: existence and uniqueness in finite dimensions_, Journal of Noncommutative Geometry 17(3), 2023. ([arXiv](https://arxiv.org/abs/1907.09689))


[[!redirects Bayesian inversions]]
[[!redirects Bayesian inverse]]
[[!redirects Bayesian inverses]]
[[!redirects bayesian inversion]]
[[!redirects bayesian inversions]]
[[!redirects bayesian inverse]]
[[!redirects bayesian inverses]]

