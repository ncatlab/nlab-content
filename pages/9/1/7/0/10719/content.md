

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

If a  [[Bousfield localization of spectra]] $L_E$ at a [[spectrum]] $E$ preserves all [[direct sums]], then it is given by [[smash product]] with the $E$-localization of the [[sphere spectrum]]

$$
  L_E X \simeq X \wedge L_E S
$$

and is hence called a _smashing localization_.

Smashing localizations hence in particular

1. preserve [[(∞,1)-colimits]];

1. are [[monoidal (∞,1)-functors]] except possibly for preservation of the [[tensor unit]].

see e.g. ([GGN 13, p. 8](#GGN13)) for discussion.

## Examples

* [[rationalization]] is smashing: $L_{\mathbb{Q}} \simeq (-) \wedge H \mathbb{Q}$ (e.g [Bauer 11, example 1.7 (4)](#Bauer11))

* For $G$ a [[group]] without [[torsion subgroup|torsion]], then localization at the [[Moore spectrum]] $E = S G$ (in particular [[p-localization]]) is smashing (see at _[[Bousfield localization of spectra]]_ [here](Bousfield+localization+of+spectra#pLocalizationIsSmashing)).

* Localization with respect to [[Morava E-theory]] is smashing (Hopkins-Ravenel).

* "finite localizations" are smashing ([Miller 92](#Miller92))

## Counter-examples

* [[p-completion]] is _not_ smashing

## Related concepts

* [[smash product theorem]]

## References

* {#LurieLect22} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ Lecture notes, Lecture 22 _Morava E-theory and Morava K-theory_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture22.pdf))

* {#Miller92} Miller, _Finite localizations_, Boletin de la Sociedad Matematica Mexicana 37 (1992), 383&#8211;390 ([HopfArchive](http://hopf.math.purdue.edu/cgi-bin/generate?/MillerH/finite-localization))
 
* {#GGN13} [[David Gepner]], Moritz Groth, [[Thomas Nikolaus]], _Universality of multiplicative infinite loop space machines_ ([arXiv:1305.4550](http://arxiv.org/abs/1305.4550))

* {#Bauer11} [[Tilman Bauer]], _Bousfield localization and the Hasse square_ (2011) ([pdf](https://math.mit.edu/events/talbot/2007/tmfproc/Chapter09/Bousfield.pdf), [[Bauer_BousfieldLocalization.pdf:file]]), chapter 6 in:  [[Christopher Douglas]], [[John Francis]], [[André Henriques]], [[Michael Hill]] (eds.), _Topological Modular Forms_, Mathematical Surveys and Monographs Volume 201, AMS 2014  ([ISBN:978-1-4704-1884-7](https://bookstore.ams.org/surv-201))


* {#Nardin12} [[Denis Nardin]], section 3.2 of _Stability and distributivity over orbital ∞-categories_, 2012 ([pdf](https://www.math.univ-paris13.fr/~nardin/thesis.pdf))

[[!redirects smashing localizations]]

[[!redirects smashing localization of spectra]]
[[!redirects smashing localizations of spectra]]