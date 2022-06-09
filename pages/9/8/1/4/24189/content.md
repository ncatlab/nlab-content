
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

This entry is about the formulation of [[sequential spectra]] [[spectrum object|in]] [[homotopy type theory]], specifically of sequential spectra that need not be genuine [[stable homotopy types]] in the sense of [[Omega-spectra]] and thus may be regarded as "[[pre-spectra]]" (they become genuine spectra under [[spectrification]]).

## Definition ##

In [[homotopy type theory]], a **prespectrum** or **sequential spectrum** is a [[dependent type|dependent]] [[bi-infinite sequence]] of [[types]] $n:\mathbb{Z} \vdash E_n\;\mathrm{type}$ with a dependent [[bi-infinite sequence]] of [[types]] $n \colon \mathbb{Z} \vdash *_n \colon E_n$ and a dependent bi-infinite sequence of [[functions]] $n \colon \mathbb{Z} \vdash e_n \colon E_n \to \Omega E_{n+1}$ which preserves the point, where $\Omega A$ is the [[loop space type]] of $A$. 

In [[Coq]] pseudocode, this becomes

    Definition prespectrum :=
      {X \colon int -> Type & 
       { pt \colon forall n, X n &
        { glue \colon forall n, X n -> pt (S n) == pt (S n) &
          forall n, glue n (pt n) == idpath (pt (S n)) }}}.

## See also ##

* [[pointed type]]

* [[Omega-spectrum type]]

* [[spectrum]]

* [[sequential spectrum]] (in contrast to an [[Omega-spectrum]])

* [[spectrification of a sequential spectrum type]]

## References ##

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* [[Floris van Doorn]] (2018), _On the Formalization of Higher Inductive Types and Synthetic Homotopy Theory_, ([arXiv:1808.10690](https://arxiv.org/abs/1808.10690), [web](http://florisvandoorn.com/papers/dissertation.pdf))

[[!redirects sequential spectrum types]]

[[!redirects prespectrum type]]
[[!redirects prespectrum types]]
[[!redirects pre-spectrum type]]
[[!redirects pre-spectrum types]]
