
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

This entry is about the formulation of [[Omega-spectra]] [[spectrum object|in]] [[homotopy type theory]], i.e. sequential spectra that are [[stable homotopy types]].

## Definition ##

In [[homotopy type theory]], a **spectrum** or $\Omega$-**spectrum** is a [[sequential spectrum type]] $E$ in which each pointed map $e_n$ is an equivalence.

$$\Spectrum \equiv \sum_{E : \PreSpectrum} \prod_{n : \mathbb{Z}} \IsEquiv (e_n)$$

## See also ##

* [[pointed type]]

* [[sequential spectrum type]]

* [[spectrum]]

* [[Omega-spectrum]] (in contrast to an [[sequential spectrum]])

* [[spectrification of a sequential spectrum type]]

## References ##

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* [[Floris van Doorn]] (2018), _On the Formalization of Higher Inductive Types and Synthetic Homotopy Theory_, ([arXiv:1808.10690](https://arxiv.org/abs/1808.10690), [web](http://florisvandoorn.com/papers/dissertation.pdf))

[[!redirects Omega-spectrum types]]

[[!redirects spectrum type]]
[[!redirects spectrum types]]
