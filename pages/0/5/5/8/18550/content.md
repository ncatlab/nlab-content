+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A _tempered (or Schwartz) distribution_ is a [[distribution]] $u\in\mathcal{D}'(\mathbb{R}^n)$ that does not "grow too fast" -- at most polynomial (or moderate/tempered) growth -- at infinity (in all directions); in particular it is only defined on $\mathbb{R}^n$, not on any open subset. Formally, a tempered distribution is a [[continuous linear functional]] on the [[Schwartz space]] $\mathcal{S}(\mathbb{R}^n)$ of [[smooth functions with rapidly decreasing derivatives]]. The space of tempered distributions (with its natural topology) is denoted $\mathcal{S}'(\mathbb{R}^n)$. The main property is that its Fourier transform $\mathcal{F}u$ is well-defined, and is itself a tempered distribution; and that it naturally extends the standard Fourier transform $\mathcal{F}: L^2(\mathbb{R}^n) \to L^2(\mathbb{R}^n)$. This makes tempered distributions the natural setting for solving (linear) partial differential equations.

## Definition

+-- {: .num_defn #TemperedDistribution}
###### Definition
**(tempered distributions)**

For $n \in \mathbb{N}$, a _[[tempered distribution]]_ on the [[Euclidean space]] $\mathbb{R}^n$ is a [[continuous linear functional]] on the [[Schwartz space]] $\mathcal{S}(\mathbb{R}^n)$ ([this def.](Schwartz+space#SchwartzSpaceOfFunctionsWithRapidlyDecreasingDerivatives)) of [[smooth functions with rapidly decreasing derivatives]].

The [[topological vector space]] of tempered distributions is denoted $\mathcal{S}'(\mathbb{R}^n)$.

=--


(e.g. [H&#246;rmander 90, def. 7.1.7](#Hoermander90))

## Related concepts

* [[Fourier transform of distributions]]


## References

* {#Hoermander90} [[Lars Hörmander]], section 7.1 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990


* {#Melrose03} [[Richard Melrose]], chapter 1 of _Introduction to microlocal analysis_, 2003 ([pdf](http://www-math.mit.edu/~rbm/iml90.pdf))


[[!redirects tempered distributions]]

category: functional analysis