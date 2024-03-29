

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



The _statistical significance_ of a [[measurement]] outcome $x$ of some [[variable]] $X$ is a measure of how unlikely it is that this outcome would be observed if $X$ were a [[random variable]] under given default assumptions, the latter often called the "standard model" or the "[[null hypothesis]]" and denoted $H_0$. Hence 

1. a low statistical significance of the observed value $x$ _suggests_ that the default assumptions, hence the "standard model" or the "null hypothesis", is correct, whence $x$ is then also called a _[[null result]]_;

1. a high statistical significance of the observed value $x$ _suggests_ that the default assumptions, hence the "standard model" or the "null hypothesis", might be inaccurate and hence "to be rejected", or, rather, to be replaced by an improved assumption/model/hypothesis $H_1$ under which the observation $x$ becomes implied with higher probability.

<div style="float:right;margin:0 10px 10px 0;"><img src="https://ncatlab.org/nlab/files/StatisticalSignificance.jpg" width="270" /></div>

More precisely, in general statistical significance is given as the [[probability]] $P(X \geq x\vert H_0)$ that a [[random variable]] $X$ with values in the [[real numbers]] takes a value in the [[interval]] $w$ of values equal or greater the observed value $x$. This probability is known as the _[[p-value]]_. The lower this probability, the higher the statistical significance of observing $x$.

> graphics grabbed from [Sinervo 02](#Sinervo02)

<div style="float:left;margin:0 10px 10px 0;"><img src="https://ncatlab.org/nlab/files/NormalDistribution.jpg" width="410" /></div>

In the special, but, by the [[central limit theorem]], generic situation that the [[probability distribution]] $p(X\vert H_0)$ of $X$ under hypothesis $H_0$ is a [[normal distribution]], 
it follows that the [[probability]] $P(X \geq x\vert H_0)$ is a [[monotone decreasing function]] of $x$, so that the value of $x$ itself is a measure of its statistical significance -- the larger $x$, the larger its statistical significance, in this case. It is natural then to express the magnitude $x \in \mathbb{R}$ in [[physical unit|units]] of [[standard deviations]] $\sigma$ of the given [[normal distribution]] $p(X\vert H_0)$. This expression of statistical significances in terms of [[standard deviations]] is common in [[particle physics]] (e.g. [Sinervo 02](#Sinervo02)), see [below](#ParticlePhysics).

As with much of [[statistics]], the concept of statistical significance is mostly used at the interface between [[theory (physics)|theory]] and [[experiment]], hence is part of the process of _[[coordination]]_, and as such subject to subtleties of real world activity that are not manifest in its clean mathematical definition. Often policy making and/or financial decisions depend on estimating and interpreting statistical significances. This has led to some lively debate about their use and misuse, see [below](#PossibleMisuse) for more. As a general rule of life, for a mathematical result to work well in applications, you need to understand what it says and what it does not say. There has also been considerable debate between [[Bayesianism|Bayesian]] and frequentist statisticians as to cogency of the use of statistical significance, see [below](#Bayes).

## Origin of significance threshold

The threshold $p\lt 0.05$ seems to date back to ([Fisher 1926](#Fisher26)) 

>… it is convenient to draw the line at about the level at which we can say: “Either there is something in the treatment, or a coincidence has occurred such as does not occur more than once in twenty trials.”…

>If one in twenty does not seem high enough odds, we may, if we prefer it, draw the line at one in fifty (the 2 per cent point), or one in a hundred (the 1 per cent point). Personally, the writer prefers to set a low standard of significance at the 5 per cent point, and ignore entirely all results which fail to reach this level. A scientific fact should be regarded as experimentally established only if a properly designed experiment rarely fails to give this level of significance.

This last sentence—implicitly about experimental replication—is often conveniently forgotten by researchers with only a rough working knowledge statistics, whereby a _single_ $p$-value under $0.05$ is seen as a discovery, rather than merely evidence.


## In particle physics
 {#ParticlePhysics}

In [[particle physics]], it has become customary to require statistical significance levels of $5 \sigma$ (5 [[standard deviations]]) in order to claim that a given observation is a real effect (e.g. [Sinervo 02, Section 5.3](#Sinervo02), [Dorigo 15, Section 3](#Dorigo15)). This corresponds to a probability ([[p-value]]) of about

$$
  5 \sigma
  \;\leftrightarrow\;
  p
  \;=\;
  2.8 \cdot 10^{-7}
  \;=\;
  0.00000028
$$ 

that the observation is a random fluctuation under the null hypothesis.

Notice that this is rather more stringent than the p-value of $p = 0.05$, corresponding to $\lt 2 \sigma$, which has been much used and much criticized in other areas of science, see [below](#PossibleMisuse).

Of course the $5 \sigma$-criterion for detectoin is a convention as any other. It has been argued in [Lyons 13b](#Lyons13b), [Dorigo 15](#Dorigo15) that different detection-thresholds should be used for different experiments. These suggestions are subjective and not generally agreed on either:

\begin{center}
<img src="https://ncatlab.org/nlab/files/LyonsThreshold.jpg" width="700">
\end{center}

> table taken from [Lyons 13b, p. 4](#Lyons13b)


\begin{center}
<img src="https://ncatlab.org/nlab/files/DorigoThresholds.jpg" width="700">
\end{center}

> table taken from [Dorigo 15, p. 16](#Dorigo15)

Regarding effects of current interest, notice that 

1. the significance $4 \sigma$ for anomalies in the [[anomalous magnetic moment]] $(g_\mu-2)$ of the [[muon]] required by [Lyons 13b, p. 4](#Lyons13b) has been reached by summer 2018, see [there](anomalous+magnetic+moment#Anomalies);

1. the significance $3 \sigma$ for [[flavour anomalies]] in [[B meson]] decays required both by [Lyons 13b, p. 4](#Lyons13b) and by [Dorigo 15, p. 16](#Dorigo15) has also been much exceeded by summer 2018, see [there](https://ncatlab.org/nlab/show/flavour+anomaly#Idea).

<br/>

## In other sciences

In pharmacology, for instance, hypothesis testing at some significance level is used in drug trials. Where those taking drug $A$ fare on average better than those on drug $B$, one might calculate the likelihood that such an effect would be found by chance given that the two drugs were in fact equally effective. 


## Possible misuse
 {#PossibleMisuse}

There have been a number of criticisms of the uses to which $p$-values have been put in scientific practice (e.g., [ZilMcCl 08](#ZilMcCl08), [GSRCPGA 16](#GSRCPGA16)). The American Statistical Association has published a statement on $p$-values ([WassLaz 16](#WassLaz16)), claiming that 

> the widespread use of 'statistical significance' (generally interpreted as '$p \leq 0.05$') as a license for making a claim of a scientific finding (or implied truth) leads to considerable distortion of the scientific process.

## Frequentist versus Bayesian statistics
 {#Bayes}

On a more fundamental level, [[Bayesianism|Bayesian]] statisticians have taken issue with the frequentist practice of hypothesis testing (see, e.g., [Jaynes 03, sec 9.1.1](#Jaynes03), [D'Agostini 03](#DAgostini03)), arguing that the value that should be sought is the probability of a proposed hypothesis conditional on the data, rather than the probability of the data under some null hypothesis. The frequentist concept of probability cannot allow for such a thing as a hypothesis having a probability. 

A useful comparison of the frequentist and Bayesian approaches as employed in particle physics, and a call for their reconciliation, is in ([Lyons 13a](#Lyons13a)):

> for physics analyses at the CERN’s LHC, the aim is, at least for determining parameters and setting upper limits in searches for various new phenomena, to use both approaches; similar answers would strengthen confidence in the results, while differences suggest the need to understand them in terms of the somewhat different questions that the two approaches are asking. It thus seems that the old war between the two methodologies is subsiding, and that they can hopefully live together in fruitful cooperation.

## Related concepts

* [[statistical inference]]

## References 

One early discussion is in

* {#Fisher26}  RA Fisher, _The Arrangement of Field Experiments_, Journal of the Ministry of Agriculture of Great Britain **33** (1926) pp 503–513.


Review includes

* {#Sinervo02} Pekka K. Sinervo, _Signal Significance in Particle Physics_, in Proceedings of _Advanced Statistical Techniques in Particle Physics_  Durham, UK, March 18-22, 2002 ([arXiv:hep-ex/0208005](https://arxiv.org/abs/hep-ex/0208005), [spire:601052](http://inspirehep.net/record/601052))

* {#Jaynes03} [[Edwin Jaynes]], _Probability theory: The logic of science_, Cambridge University Press, 2003.

* {#Lyons13a} [[Louis Lyons]], _Bayes and Frequentism: a Particle Physicist's perspective_,  Journal of Contemporary Physics Volume 54, 2013 - Issue 1
 ([arXiv:1301.1273](https://arxiv.org/abs/1301.1273), [doi:10.1080/00107514.2012.756312](https://doi.org/10.1080/00107514.2012.756312))

* {#Lyons13b} [[Louis Lyons]], _Discovering the Significance of 5 sigma_ ([arXiv:1310.1284](https://arxiv.org/abs/1310.1284))

* {#Dorigo15} [[Tommaso Dorigo]], _Extraordinary claims: the $0.000029\%$ solution_, EPJ Web of Conferences 95, 02003 (2015) ([doi:10.1051/epjconf/20159502003](https://doi.org/10.1051/epjconf/20159502003))

* {#Barlow19} Roger John Barlow, _Practical Statistics for Particle Physics_ ([arXiv:1905.12362](https://arxiv.org/abs/1905.12362))

See also

* Wikipedia, _[Statistical significance](https://en.wikipedia.org/wiki/Statistical_significance)_


* Leland Wilkinson and Task Force on Statistical Inference, Statistical methods in psychology journals: guidelines and explanations, American Psychologist 54 (1999), 594&#8211;604, [pdf](http://www.apa.org/pubs/journals/releases/amp-54-8-594.pdf)


Cautionary remarks on misuse of the concept include the following

* {#ZilMcCl08} Stephen Ziliak and Deirdre McCloskey, _The Cult of Statistical Significance_, Michegan University Press, 2008, [book](https://www.press.umich.edu/186351/cult_of_statistical_significance).



* {#DAgostini03} Giulio D'Agostini, _Bayesian reasoning in data analysis: A critical introduction_, World Scientific Publishing, 2003.

* $n$Cafe: [Fetishizing p-Values](http://golem.ph.utexas.edu/category/2010/09/fetishizing_pvalues.html) by Tom Leinster

* {#GSRCPGA16} Greenland, Senn, Rothman, Carlin, Poole, Goodman, Altman, _Statistical tests, P values, confidence intervals, and power: a guide to misinterpretations_, Eur J Epidemiol. 2016 Apr;31(4):337-50. ([doi:10.1007/s10654-016-0149-3](https://www.ncbi.nlm.nih.gov/pubmed/27209009))

* {#WassLaz16} Ronald Wasserstein, Nicole Lazar, _The ASA's Statement on $p$-Values: Context, Process, and Purpose_, The American Statistician 70(2), 2016, pp. 129-133 ([doi:10.1080/00031305.2016.1154108](https://doi.org/10.1080/00031305.2016.1154108))


[[!redirects statistical significances]]

[[!redirects p-value]]
[[!redirects p-values]]
