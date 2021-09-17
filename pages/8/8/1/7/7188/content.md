

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


# Measurable functions
* table of contents
{: toc}

## Idea

The _measurable functions_ are those functions between [[measure spaces]] amenable to treatment in [[measure theory]], hence they are the evident _[[homomorphisms]]_ between [[measure spaces]].


## Definitions

Given [[measurable spaces]] $X$ and $Y$, a __measurable function__ from $X$ to $Y$ is a [[function]] $f\colon X \to Y$ such that the [[preimage]] $f^*(T)$ is [[measurable set|measurable]] in $X$ whenever $T$ is measurable in $Y$.

In classical measure theory, it is usually assumed that $Y$ is the [[real line]] (or a variation such as the extended real line or the complex plane) equipped with the [[Borel sets]].  Then $f$ is measurable if and only if $f^{-1}(I)$ is measurable whenever $I \subseteq Y$ is an interval.  More generally, if $Y$ is any [[topological space]] equipped with the Borel sets, then $f$ is measurable if and only if $f^{-1}(I)$ is measurable whenever $I \subseteq Y$ is [[open set|open]].

In some variations of measure theory based on $\delta$&#8209; or $\sigma$-rings instead of on $\sigma$-algebras, it is necessary to allow [[partial functions]] whose domain is a [[relatively measurable set]].  Classically (when $Y$ is the real line), one achieves (for purposes of [[integration]]) essentially the same result by requiring only that $f^{-1}(I)$ be measurable whenever $I \subseteq Y$ is an interval that does not contain $0$; in other words, one effectively assumes that $f$ is zero wherever it would otherwise be undefined.


## Modulo null sets

If (as in a [[measure space]], a [[Cheng space]], or a [[localisable measurable space]]), we have a notion of [[null sets]] (or [[full sets]]) in $X$ and $Y$, then we may allow a measurable function to be an __[[almost function]]__: a [[partial function]] whose domain is full.  Specifically, an almost function $f\colon X \to Y$ is __measurable__ if the [[preimage]] of every full set in $Y$ is full in $X$ and the preimage of every measurable set in $Y$ is, if not quite measurable in $X$, at least equal to a measurable set in $X$ up to a full set in $X$.  (To emphasise this last change, we may call such functions __almost measurable__.)  Additionally, we consider two measurable almost functions to be [[equal]] (or [[equivalent]] if one prefers) if they are __[[almost equality|almost equal]]__: their [[equaliser]] is full.

## Related concepts

* [[pushforward measure]]

## Literature

* Dave Applebaum, *Measurable Functions* ([pdf](http://www.applebaum.staff.shef.ac.uk/Ch2MeasFn.pdf))


category: analysis
[[!redirects measurable function]]
[[!redirects measurable functions]]
[[!redirects measurable map]]
[[!redirects measurable maps]]

[[!redirects measurable almost function]]
[[!redirects measurable almost functions]]
[[!redirects measurable almost measurable function]]
[[!redirects measurable almost measurable functions]]
[[!redirects measurable almost measurable almost function]]
[[!redirects measurable almost measurable almost functions]]
