
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

### For plain spectra
 {#ForPlainSpectra}

[[connective spectrum|Connective spectra]] form a [[coreflective sub-(∞,1)-category]] of the [[(∞,1)-category of spectra]]. The [[right adjoint|right]] [[adjoint (∞,1)-functor]] from spectra to connective spectra $E \mapsto E \langle 0 \rangle$ is called the _connective cover_ construction. This comes with the [[coreflective subcategory|coreflection]] morphism of spectra

\[
  \label{CoreflectionOfSpectrumFromItsConnectiveCover}
  E\langle 0 \rangle
  \overset{
    \epsilon_E
  }{\longrightarrow}
  E
\]

which induces an [[isomorphism]] on [[homotopy groups of a spectrum|homotopy groups of spectra]] in non-[[negative number|negative]] degrees: 

$$
  \pi_{\bullet \geq 0}\big( E\langle 0\rangle\big)  
  \underoverset
  {\simeq}
  {
    \pi_{\bullet \geq 0}
    (\epsilon_E)
  }{\longrightarrow} 
  \pi_{\bullet \geq 0}(E)
  \,.
$$




### For ring spectra
 {#ForRingSpectra}

The connective cover  [[(∞,1)-functor|functor]] extends from plain spectra to [[E-∞ ring spectra]] ([May 77, Prop. VII 4.3](#May77), [Lurie, Prop. 7.1.3.13](#Lurie)), such that the coreflection $E \langle0\rangle \longrightarrow E$ (eq:CoreflectionOfSpectrumFromItsConnectiveCover) is a [[homomorphism]] of [[E-∞ rings]].

Besides a canonically inherited ring structure, the connective cover may sometimes carry further ring structures, but in many examples of interest it is unique ([Baker-Richter 05](#BakerRichter05)). 


## Examples

* [[ku]] is the connective cover of [[KU]]

## Related concepts

* [[n-connected object of an (infinity,1)-topos]]

## References

For plain spectra:

* {#Schwede12} [[Stefan Schwede]], chapter II, section 8, and chapter III, section 7 of _[[Symmetric spectra]]_ (2012)

For [[ring spectra]]:

* {#May77} [[Peter May]], Prop. VII 4.3 in: _$E_\infty$-Ring spaces and $E_\infty$ ring spectra_, Lecture Notes in Mathematics 577, Springer 1977 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/e_infty.pdf), [cds:1690879](https://cds.cern.ch/record/1690879))


* {#BakerRichter05} [[Andrew Baker]], [[Birgit Richter]], _Uniqueness of $E_\infty$-structures for connective covers_,  Proc. Amer. Math. Soc. 136 (2008), 707-714  ([arXiv:math/0506422](http://arxiv.org/abs/math/0506422), [doi:10.1090/S0002-9939-07-08984-8](https://doi.org/10.1090/S0002-9939-07-08984-8))


* {#Lurie} [[Jacob Lurie]], 7.1.3.11-13 in: _[[Higher Algebra]]_


[[!redirects connective covers]]

