
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
=--
=--


# Bayesian reasoning
* table of contents
{: toc}

## Idea

Bayesian [[reasoning]] is an application of [[probability theory]] to [[inductive reasoning]] (and [[abductive reasoning]]).  It relies on an interpretation of probabilities as expressions of an agent's uncertainty about the world, rather than as concerning some notion of objective chance in the world. The perspective here is that, when done correctly, inductive reasoning is simply a generalisation of [[deductive reasoning]], where knowledge of the truth or falsity of a proposition  corresponds to adopting the extreme probabilities $1$ and $0$. 

Several advantages to this interpretation have been proposed. For one thing, it is possible to have (rational) degrees of belief about a wide range of propositions, including matters which are settled, yet unknown. For example, it is possible to speak of the probability of the value of a constant of nature falling within a given interval on the basis of various pieces of evidence, or of the outcome of a coin that has already been tossed. This interpretation of probability beyond limiting frequencies leads, so advocates such as [[Edwin Jaynes]] claim, to a more integrated treatment of probability theory and statistics.

## Dutch Book justification

It can be shown by so-called "Dutch Book" arguments, that a rational agent must set their degrees of belief in the outcomes of events in such a way that they satisfy the axioms of probability theory. The idea here is that to believe a proposition to degree $p$ is equivalent to being prepared to accept a wager at the corresponding odds. For instance, if I believe there is a 0.75 chance of rain today, then I should be prepared to accept a wager so that I receive $S$ units of currency if it does not rain, and pay out $S/3$ units if it does rain. Note that $S$ may be chosen to be negative by the bettor.

It can be shown then that such betting odds must satisfy the probability axioms, otherwise it will be possible for someone to place multiple bets which will cause the bookmaker to suffer a certain loss whatever the outcome. For example, in the case above, my degree of belief that it will _not_ rain today should be 0.25. Were I to offer, say, 0.5, someone could stake $(-3)$ units on the first bet and $(-2)$ units on the second bet, and will gain $1$ unit whether or not it rains.  Of course, real bookmakers have odds which sum to more than 1, but they suffer no guaranteed loss since clients are only allowed positive stakes.

##Cox's axioms

Some consider the reliance on the idea of the undesirability of certain financial loss to be unbefitting for a justification of what is supposed to be an extension of ordinary deductive logic ([Jaynes 2003](#Jaynes)). Axiomatisations in terms of the properties one should expect of degrees of plausibility have been given, and it can be shown from such axioms that these degrees satisfy the axioms of probability. Richard Cox is responsible for one such axiomatisation (for the moment see [Wikipedia: Cox's theorem](http://en.wikipedia.org/wiki/Cox's_theorem)).

##Conditionalizing

Using [[Bayes' Rule]], degrees of belief can be updated on receipt of new evidence.

$$
P(h|e) = P(e|h) \cdot \frac{P(h)}{P(e)},
$$

where $h$ is a hypothesis and $e$ is evidence.

The idea here is that when $e$ is observed, your degree of belief in $h$ should be changed from $P(h)$ to $P(h|e)$. This is known as **conditionalizing**. If $P(h|e) \gt P(h)$, we say that $e$ has provided **confirmation** for $h$.

Typically, situations will involve a range of possible hypotheses, $h_1, h_2, \ldots$, and applying Bayes' Rule will allow us to compare how these fare as new observations are made. For example, comparing the fate of two hypotheses,

$$
\frac{P(h_1|e)}{P(h_2|e)} = \frac{P(e|h_1)}{P(e|h_2)}\cdot \frac{P(h_1)}{P(h_2)}.
$$

How to assign prior probabilities to hypotheses when you don't think you have an exhaustive set of rivals is not obvious. When astronomers in the nineteenth century tried to account for the anomalies in the position of Mercury's perihelion, they tried out all manner of explanations: maybe there was a planet inside Mercury's orbit, maybe there was a cloud of dust surrounding the sun, maybe the power in the inverse square law ought to be (2 - $\epsilon$),... Assigning priors and changing these as evidence comes in is one thing, but it would have been wise to have reserved some of the prior for 'none of the above'.

Interestingly, one of the first people to give a qualitative sketch of how such an approach would work was [[George Polya]] in 'Mathematics and Plausible Reasoning' ([Polya](#Polya)), where examples from mathematics are widely used. The idea of a Bayesian account of plausible reasoning in mathematics surprises many, it being assumed that mathematicians rely solely on [[deductive reasoning|deduction]]. (See also Chap. 4 of [Corfield03](#Corfield).)

##Objective Bayesianism

For some Bayesians, degrees of belief must satisfy further restrictions. One extreme form of this view holds that given a particular state of knowledge, there is a single best set of degrees of belief that should be adopted for any proposition. 

Some such restrictions are generally accepted. If, for example, all I know of an event is that it has $n$ possible outcomes, the objective Bayesian will apply the principle of indifference to set their degrees of belief to $1/n$ for each outcome. On the other hand, if there is background knowledge concerning differences between the outcomes, indifference need not hold. This principle of indifference can be generalized to other kinds of invariance, such as the Jeffreys prior ([wiki](http://en.wikipedia.org/wiki/Jeffreys_prior)). 

Other objective Bayesian principles include maximum entropy (see [Jaynes 2003](#Jaynes)). For instance, Jaynes argues that if all that is known of a die is that the mean value of throws is equal to, say, 4, then a prior distribution over $\{1, 2, 3, 4, 5, 6\}$ should be chosen which maximizes [[entropy]], subject to the constraint that the mean is 4. Many familiar distributions are maximum entropy distributions, subject to moment constraints. For instance, the Normal distribution, $N(\mu, \sigma^2)$, is the distribution over the reals which maximises entropy subject to having mean $\mu$ and variance $\sigma^2$.

##Exchangeability

Frequentist statistics makes much use of independent and identically distributed (iid) random variables, for example in sampling situations. If, say, we were to toss a coin repeatedly and record the outcomes, the frequentist would typically understand this as sampling from a Bernoulli distribution for some fixed value $p$ of the coin showing heads. From the sample one could then calculate an estimate and confidence interval for the true value of $p$.

Many Bayesians, in particular [[Bruno de Finetti]], argue that this makes no sense since probability is not in the world, but rather it represents the strengths of our beliefs in different outcomes. Their formulation in such repeated sampling cases is to say that if our degrees of belief are such that, for all $n$, the probability we assign to any sequence of $n$ tosses is invariant under any permutation of $n$ elements, then we can represent our degrees of belief for all sequences as arising from a mixture of Bernoulli distributions for some prior distribution over the value of $p$. 

More formally, given a sequence of random variables $\{X_i\}^\infty_{i = 1}$ each taking the values $0$ and $1$, de Finetti's Representation Theorem says that the sequence is exchangeable if and only if there is a random variable $\Theta: \Omega \to [0, 1]$, with distribution $\mu_{\Theta}$, such that

$$
P\{X_1=x_1,\ldots,X_n=x_n\}=\int_{[0,1]} \theta^s (1 - \theta)^{n - s} d \mu_{\Theta}(\theta),
$$

in which $s = \sum^n_{i=1} x_i$. 

Often, for ease of calculation, Beta distributions are chosen as priors on $p$, which can be taken as representing one's confidence as though one had already seen a certain number of heads and tails. Bayesians are sometimes criticized for the subjectivity inherent in the choice of a prior, but in many cases, such as this one, prior distributions will eventually be 'washed out' by the weight of the evidence.  The de Finetti theorem has a generalization for multivariate distributions ([BBF](#BBF)).

Of course, exchangeability may not represent the strength of one's prior beliefs accurately. For example, in the case of coin tossing, I may have a suspicion of there being something in the tossing mechanism which would make the result of one toss depend on its predecessor. Then it would be quite reasonable for me, say, to have accorded a higher prior probability to the sequence of one hundred heads followed by one hundred tails than to some of its permutations. There are, however, generalizations of de Finetti's representation theorem to Markov chain situations ([Diaconis and Freedman](#DF80)).

## Related entries

* [[conditional expectation]]

* [[Bayesian interpretation of quantum mechanics]]



## References

### General


* {#Jaynes} [[Edwin Jaynes]], _Probability Theory: The Logic of Science_, Cambridge University Press, 2003.

* {#Polya} [[George Polya]], _Mathematics and Plausible Reasoning: Vol. II: Patterns of Plausible Inference_, Princeton University Press, 1954.

* {#Corfield} [[David Corfield]], _Towards a Philosophy of Real Mathematics_, Cambridge University Press, 2003, Chap. 4.




See also 

* Wikipedia, _[Bayesian inference](https://en.wikipedia.org/wiki/Bayesian_inference)_

### Category-theoretic treatment

Placing Bayesian inference in a category theoretic setting occurs in

* [[Kirk Sturtz]], _Bayesian Inference using the Symmetric Monoidal Closed Category Structure_, ([ arXiv:1601.02593](https://arxiv.org/abs/1601.02593))

* [[Jared Culbertson]], [[Kirk Sturtz]] _Bayesian machine learning via category theory_, ([arXiv:1312.1445](https://arxiv.org/abs/1312.1445))

### Exchangeability

* {#DF80} [[Persi Diaconis]] and David Freedman, "De Finetti's theorem for Markov chains." Annals of Probability, 8(1), 115-130, 1980.

* {#BBF} A. Bach, H. Blank, H. Francke, _Bose-Einstein statistics derived from the statistics of classical particles_, Lettere Al Nuovo Cimento Series 2, Volume 43, Issue 4, pp 195-198.

* {#FGP21} [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], _De Finetti's Theorem in Categorical Probability_, ([arXiv:2105.02639](https://arxiv.org/abs/2105.02639))



### Bayesian inference in physics

Discussion of applications in [[astronomy]], [[cosmology]] and [[particle physics]] includes

* [[Jörg Rachen]], _Bayesian Classification of Astronomical Objects -- and what is behind it_ ([arXiv:1302.2429](http://arxiv.org/abs/1302.2429))

* [[Roberto Trotta]], _Bayesian Methods in Cosmology_, ([arXiv:1701.01467](https://arxiv.org/abs/1701.01467))

* {#Lyons13} Louis Lyons, _Bayes and Frequentism: a Particle Physicist's perspective_, ([arXiv:1301.1273](https://arxiv.org/abs/1301.1273))

* Joshua Landon, Frank X. Lee, Nozer D. Singpurwalla, _A Problem in Particle Physics and Its Bayesian Analysis_, ([arXiv:1201.1141](https://arxiv.org/abs/1201.1141))




 




[[!redirects Bayesian reasoning]]
[[!redirects Bayesian induction]]
[[!redirects Bayesian probability]]
[[!redirects Bayesianism]]


[[!redirects Bayesian inference]]
[[!redirects Bayesian inferences]]
