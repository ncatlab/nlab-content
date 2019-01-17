

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

_Statistical significance_ is a measure used in hypothesis testing. It is commonly defined in terms of the likelihood, under the assumption of some _null_ hypothesis, of results occurring with at least the significance as those that are measured. For instance, in a drug trial where those taking drug $A$ fare on average better than those on drug $B$, one might calculate the likelihood that such an effect would be found by chance given that the two drugs were in fact equally effective. Significance levels are often given as [[p-values]], where $p$ is the likelihood of the data under the null hypothesis. 

There have been a number of criticisms of the uses to which $p$-values have been put (e.g., [ZilMcCl 08](#ZilMcCl08)), especially by [[Bayesianism|Bayesian]] statisticians (see, e.g., [Jaynes 03, sec 9.1.1](#Jaynes03)). 

In experimental physics, researchers often require significance levels of $5 \sigma$ (5 [[standard deviations]]). Achievement of this level in an experiment should not be understood as meaning that the chance that this is not a real signal is 1 in 3.5 million, as an incorrect reading of the $p$-value might suggest. Instead, this level has been chosen from experience as making it sufficiently likely that the signal will not disappear as further evidence is collected. Bayesians are typically critical of this $\sigma$ language for its incoherence and argue that background knowledge should be employed to allow model comparison, see, for instance ([D'Agostini 03](#DAgostini03)).

## References 

* $n$Cafe: [Fetishizing p-Values](http://golem.ph.utexas.edu/category/2010/09/fetishizing_pvalues.html) by Tom Leinster

* Leland Wilkinson and Task Force on Statistical Inference, Statistical methods in psychology journals: guidelines and explanations, American Psychologist 54 (1999), 594&#8211;604, [pdf](http://www.apa.org/pubs/journals/releases/amp-54-8-594.pdf)

* {#ZilMcCl08} Stephen Ziliak and Deirdre McCloskey, _The Cult of Statistical Significance_, Michegan University Press, 2008, [book](https://www.press.umich.edu/186351/cult_of_statistical_significance).

* {#DAgostini03} Giulio D'Agostini, _Bayesian reasoning in data analysis: A critical introduction_, World Scientific Publishing, 2003.

* {#Jaynes03} Edwin Jaynes, _Probability theory: The logic of science_, Cambridge University Press, 2003.

See also

* Wikipedia, _[Statistical significance](https://en.wikipedia.org/wiki/Statistical_significance)_

[[!redirects statistical significances]]