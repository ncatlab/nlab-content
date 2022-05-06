

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



The _statistical significance_ of a [[measurement]] outcome $x$ of some [[variable]] $X$ is a measure of how unlikely it is that this outcome would be observed if $X$ were a [[random variable]] under given default assumptions, the latter often called the "standard model" or the "null hypothesis" and denoted $H_0$. Hence a high statistical significance of the observed value $x$ _suggests_ that the default assumptions, hence the "standard model" or the "null hypothesis", might be inaccurate and hence "to be rejected", or, rather, to be replaced by an improved assumption/model/hypothesis $H_1$ under which the observation $x$ becomes implied with higher probability.

<div style="float:right;margin:0 10px 10px 0;"><img src="https://ncatlab.org/nlab/files/StatisticalSignificance.jpg" width="270" /></div>

More precisely, in general statistical significance is given as the [[probability]] $P(X \geq x\vert H_0)$ that a [[random variable]] $X$ with values in the [[real numbers]] takes a value in the [[interval]] $w$ of values equal or greater the observed value $x$. This probability is known as the _[[p-value]]_. The lower this probability, the higher the statistical significance of observing $x$.

> graphics grabbed from [Sinervo 02](#Sinervo02)

<div style="float:left;margin:0 10px 10px 0;"><img src="https://ncatlab.org/nlab/files/NormalDistribution.jpg" width="410" /></div>

In the special, but, by the [[central limit theorem]], generic situation that the [[probability distribution]] $p(X\vert H_0)$ of $X$ under hypothesis $H_0$ is a [[normal distribution]], 
it follows that the [[probability]] $P(X \geq x\vert H_0)$ is a [[monotone decreasing function]] of $x$, so that the value of $x$ itself is a measure of its statistical significance -- the larger $x$, the larger its statistical significance, in this case. It is natural then to express the magnitude $x \in \mathbb{R}$ in [[physical unit|units]] of [[standard deviations]] $\sigma$ of the given [[normal distribution]] $p(X\vert H_0)$. This expression of statistical significances in terms of [[standard deviations]] is common in [[particle physics]] (e.g. [Sinervo 02](#Sinervo02)), see [below](#ParticlePhysics).

As with much of [[statistics]], the concept of statistical significance is mostly used at the interface between [[theory (physics)|theory]] and [[experiment]], hence is part of the process of _[[coordination]]_, and as such subject to subtleties of real world activity that are not manifest in its clean mathematical definition. Often policy making and/or financial decisions depend on estimating and interpreting statistical significances. This has led to some lively debate about their use and misuse, see [below](#PossibleMisuse) for more. As a general rule of life, for a mathematical result to work well in applications, you need to understand what it says and what it does not say. 


 



## In particle physics
 {#ParticlePhysics}

In [[particle physics]],it has become customary to require statistical significance levels of $5 \sigma$ (5 [[standard deviations]]) in order to claim that a given observation is a real effect (e.g. [Sinervo 02, Section 5.3](#Sinervo02)). This corresponds to a probability ([[p-value]]) of about $2.8 \cdot 10^{-7}$ that the observation is a random fluctuation under the null hypothesis.


## In other sciences

In pharmacology, for instance, hypothesis testing at some significance level is used in drug trials. Where those taking drug $A$ fare on average better than those on drug $B$, one might calculate the likelihood that such an effect would be found by chance given that the two drugs were in fact equally effective. 


## Possible misuse
 {#PossibleMisuse}

There have been a number of criticisms of the uses to which $p$-values have been put in scientific practice (e.g., [ZilMcCl 08](#ZilMcCl08)). The American Statistical Association has published a statement on $p$-values ([WassLaz 16](#WassLaz16)), claiming that 

> the widespread use of 'statistical significance' (generally interpreted as '$p \leq 0.05$') as a license for making a claim of a scientific finding (or implied truth) leads to considerable distortion of the scientific process.

## Frequentist versus Bayesian statistics

On a more fundamental level, [[Bayesianism|Bayesian]] statisticians have taken issue with the frequentist practice of hypothesis testing (see, e.g., [Jaynes 03, sec 9.1.1](#Jaynes03), [D'Agostini 03](#DAgostini03)). 

A useful comparison of the frequentist and Bayesian approaches as employed in particle physics, and a call for their reconciliation, is in ([Lyons 13](#Lyons13)):

> for physics analyses at the CERN’s LHC, the aim is, at least for determining parameters and setting upper limits in searches for various new phenomena, to use both approaches; similar answers would strengthen confidence in the results, while differences suggest the need to understand them in terms of the somewhat different questions that the two approaches are asking. It thus seems that the old war between the two methodologies is subsiding, and that they can hopefully live together in fruitful cooperation.

## References 

Review includes

* {#Sinervo02} Pekka K. Sinervo, _Signal Significance in Particle Physics_, in Proceedings of _Advanced Statistical Techniques in Particle Physics_  Durham, UK, March 18-22, 2002 ([arXiv:hep-ex/0208005](https://arxiv.org/abs/hep-ex/0208005), [spire:601052](http://inspirehep.net/record/601052))

* {#Lyons13} Louis Lyons, _Bayes and Frequentism: a Particle Physicist's perspective_, ([arXiv:1301.1273](https://arxiv.org/abs/1301.1273))

* {#Jaynes03} Edwin Jaynes, _Probability theory: The logic of science_, Cambridge University Press, 2003.

See also

* Wikipedia, _[Statistical significance](https://en.wikipedia.org/wiki/Statistical_significance)_

* {#WassLaz16} Ronald Wasserstein, Nicole Lazar, _The ASA's Statement on p-Values: Context, Process, and Purpose_, The American Statistician 70(2), 2016, pp. 129-133. 

* Leland Wilkinson and Task Force on Statistical Inference, Statistical methods in psychology journals: guidelines and explanations, American Psychologist 54 (1999), 594&#8211;604, [pdf](http://www.apa.org/pubs/journals/releases/amp-54-8-594.pdf)


Cautionary remarks on misuse of the concept include the following

* {#ZilMcCl08} Stephen Ziliak and Deirdre McCloskey, _The Cult of Statistical Significance_, Michegan University Press, 2008, [book](https://www.press.umich.edu/186351/cult_of_statistical_significance).

* {#DAgostini03} Giulio D'Agostini, _Bayesian reasoning in data analysis: A critical introduction_, World Scientific Publishing, 2003.

* $n$Cafe: [Fetishizing p-Values](http://golem.ph.utexas.edu/category/2010/09/fetishizing_pvalues.html) by Tom Leinster


[[!redirects statistical significances]]

[[!redirects p-value]]
[[!redirects p-values]]
