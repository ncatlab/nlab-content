
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

This entry is about the formulation of [[Omega-spectra]] [[spectrum object|in]] [[homotopy type theory]], i.e. [[sequential spectrum types]] that are [[stable homotopy types]].

## Definition ##

In [[homotopy type theory]], a **spectrum** or $\Omega$-**spectrum** is a [[sequential spectrum type]] $E$ in which each pointed map $e_n$ is an [[equivalence in homotopy type theory|equivalence]].

$$\Spectrum \equiv \sum_{E : \PreSpectrum} \prod_{n : \mathbb{Z}} \IsEquiv (e_n)$$

## See also ##

* [[pointed type]]

* [[sequential spectrum type]]

* [[spectrum]]

* [[Omega-spectrum]] (in contrast to an [[sequential spectrum]])

* [[spectrification of a sequential spectrum type]]

* [[cohomology in homotopy type theory]]

## References ##

* [[Evan Cavallo]], §3.2 of: *Synthetic Cohomology in Homotopy Type Theory* (2015) &lbrack;[pdf](https://staff.math.su.se/evan.cavallo/works/thesis15.pdf), [[Cavallo-CohomologyInHoTT.pdf:file]]&rbrack;

* [[Floris van Doorn]], §5.3 in: _On the Formalization of Higher Inductive Types and Synthetic Homotopy Theory_ (2018) &lbrack;[arXiv:1808.10690](https://arxiv.org/abs/1808.10690), [web](http://florisvandoorn.com/papers/dissertation.pdf)&rbrack;

[[!redirects Omega-spectrum types]]

[[!redirects spectrum type]]
[[!redirects spectrum types]]
