
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Bousfield localization of spectra_ refers generally to [[localization of an (∞,1)-category|localizations]] of the [[stable (∞,1)-category of spectra]] or else to its presentation by  [[Bousfield localization of model categories|Bousfield localization]] of the [[stable model category]] of [[spectra]]. 

Specifically, for $E \in Spec$ a [[spectrum]], the _Bousfield localization at $E$_ of another [[spectrum]] $X$ is the [[universal property|universal map]]

$$
  X \longrightarrow L_E X
$$

to the _$E$-local spectrum_ $L_E X$, with the property that for $Y$ any $E$-acyclic spectrum in that $Y \wedge E \simeq 0$, every morphism $Y \longrightarrow L_E X$ is null-homotopic (a [[zero morphism]] in the [[stable (∞,1)-category of spectra]]). (see for instance [Lurie 10, Example 4](#LurieLecture))

For $E = H \mathbb{Z}_p$ the [[Eilenberg-MacLane spectrum]] of the [[cyclic group]] $\mathbb{Z}_p \coloneqq \mathbb{Z}/p\mathbb{Z}$ for some [[prime number]] $p$, this $E$-localization is _[[p-localization]]_. (see for instance [Lurie 10, Examples 7 and 8](#LurieLecture))

## Examples

* [[p-localization]]

* [[telescopic localization]]

* [chromatic localization](Morava+E-theory#BousfieldLocalizationAndChromaticFiltration)

## Related concepts

* [[smashing localization]]

* [[chromatic filtration]], [[chromatic layer]]

## References

The original article is

* [[Aldridge Bousfield]], _The localization of spectra with respect to homology_ , Topology vol 18 (1979) ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))

Lecture notes include

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture notes (2010) ([web](http://www.math.harvard.edu/~lurie/252x.html)),  Lecture 20 _Bousfield localization_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture20.pdf))
 {#LurieLecture}

in section 2.4 of

* Holger Reeker, _On K(1)-local SU-bordism_ ([arXiv:0907.4299](http://arxiv.org/abs/0907.4299))
