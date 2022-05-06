
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The terminology  _(commutative) ring spectrum_ refers either to a ([[commutative monoid|commutative]]) [[monoid]] in the [[stable homotopy category]] regarded as [[monoidal category]] via the [[smash product of spectra]], or to the richer structure of a [[monoid]] in a [[model structure for spectra]] equipped with a [[symmetric smash product of spectra]]. 

In the first case a ring spectrum is a [[spectrum]] equipped with a unit and product operation, which is associative, unital  (and commutative) just up to unspecified [[homotopy]], such as in an [[H-space]] structure. Accordingly, these might be called "H-ring spectra", but it is traditional to just call them "ring spectra." (An _[[H-infinity ring spectrum]]_ ([Bruner-May-McClure-Steinberger 86](#BrunerMayMcLureSteinberger86)) is such an H-ring spectrum equipped with some extra structure modeling [[extended power]] operations.)

In the second case the structure is much richer; and in good cases, such as for [[highly structured spectra]], is equivalent to [[A-∞ ring]] structure ([[E-∞ ring]] structure).

To distinguish the two situations further qualification is being used. Sometimes one says **homotopy ring spectrum** to explicitly refer to the first case (e.g. [Schwede 12, chapter II 4.1](#Schwede12)) or one says "[[highly structured ring spectrum]]" to refer explicitly to the second case. For more on this see at _[[brave new algebra]]_ and _[[higher algebra]]_.

Since the concept of [[spectrum]] is the refinement of the concept of [[abelian group]] to [[homotopy theory]]/[[(∞,1)-category theory]]. The concept of **ring spectrum** is the corresponding generalization of the notion of ([[commutative ring|commutative]]) [[ring]].

[[!include homological and higher algebra -- table]]

## Definition

For details see _[[Introduction to Stable homotopy theory]]_, _[[Introduction to Stable homotopy theory -- 1-2|Part 1-2 -- Structured spectra]]_.

## Properties

### Relation to multiplicative generalized cohomology

Under the [[Brown representability theorem]], the [[generalized cohomology theory]] represented by a ring spectrum inherits the structure of a [[multiplicative cohomology theory]].

Conversely via the [[Brown representability theorem]] a spectrum representing a [[multiplicative cohomology theory]] inherits the structure of (at least) an H-ring spectrum. See [there](multiplicative+cohomology+theory#BrownRepresentabilityByRingSpectra).


## Related concepts

* [[ultracommutative ring spectrum]]

* [[symmetric ring spectrum]]

* [[symmetric algebra spectrum]]

* [[module spectrum]], [[algebra spectrum]]

* [[Gorenstein ring spectrum]]

* [[functor with smash products]]

* [[periodic ring spectrum]]

* [[Hopf ring spectrum]]

* [[model structure for ring spectra]]

* [[Boardman homomorphism]], [[Adams spectral sequence]]

* [[multiplicative spectral sequence]]



## Reference

The notion of (commutative) homotopy ring spectra, i.e. ([[commutative monoid|commutative]]) [[monoids]] in the [[stable homotopy category]] with respect to the [[smash product of spectra]]:

* {#Adams74} [[Frank Adams]], part III, section 10 of _[[Stable homotopy and generalised homology]]_, 1974 ([pdf](https://www.uio.no/studier/emner/matnat/math/MAT9580/v17/documents/adams-shgh.pdf))

  > (attributed there to [[George Whitehead]])

Review:

* [[John Michael Boardman]], Sections 3,7 of: _Stable Operations in Generalized Cohomology_ ([pdf](https://hopf.math.purdue.edu/Boardman/stabop.pdf)) in: [[Ioan Mackenzie James]] (ed.) _[[Handbook of Algebraic Topology]]_ Oxford 1995 ([doi:10.1016/B978-0-444-81779-2.X5000-7](https://doi.org/10.1016/B978-0-444-81779-2.X5000-7))

* {#TamakiKono06} [[Dai Tamaki]], [[Akira Kono]], Appendix C.2 of: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([[GeneralizedCohomology.pdf:file]], [ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))

* {#Malkiewich14} [[Cary Malkiewich]], section 1.3 of _The stable homotopy category_, 2014 ([pdf](http://math.stanford.edu/~carym/stable.pdf))

* [[Urs Schreiber]], _[[Introduction to Stable homotopy theory]] -- [Homotopy ring spectra](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyRingSpectra)_, 2016

* [[Birgit Richter]], _Commutative ring spectra_ ([arXiv:1710.02328](https://arxiv.org/abs/1710.02328))


On [[H-infinity ring spectra]]:

* {#BrunerMayMcLureSteinberger86} R. Bruner, [[Peter May]], [[James McClure]], M. Steinberger, _$H_\infty$-Ring Spectra and their Applications_, Lecture Notes in Mathematics 1176, Springer 1986 ([doi:10.1007/BFb0075405](https://link.springer.com/book/10.1007/BFb0075405),  [pdf](http://www.math.uchicago.edu/~may/BOOKS/h_infty.pdf))


Discussion of connective ring spectra as monoids with respect to a smash product on [[Gamma-spaces]]:

* {#Schwede99} [[Stefan Schwede]], _Stable homotopical algebra and $\Gamma$-spaces_, Math. Proc. Camb. Phil. Soc. (1999), 126, 329 ([pdf](http://www.math.uni-bonn.de/people/schwede/Gamma.pdf))

* {#Lawson09} [[Tyler Lawson]], _Commutative &#915;-rings do not model all commutative ring spectra_, Homology Homotopy Appl. Volume 11, Number 2 (2009), 189-194. ([Euclid](http://projecteuclid.org/euclid.hha/1296138517))

Discussion of ring spectra as rings with respect to the [[symmetric smash product of spectra]] on [[S-modules]] includes

* [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], sections 2 and 3 of _[[Modern foundations for stable homotopy theory]]_ ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

* {#EKMM} [[Anthony Elmendorf]], [[Igor Kriz]], [[Michael Mandell]], [[Peter May|P. May]], _[[Rings, modules and algebras in stable homotopy theory]]_, AMS Mathematical Surveys and Monographs Volume 47 (1997) ([pdf](http://www.math.uchicago.edu/~may/BOOKS/EKMM.pdf))

See also

* {#BakerRichter} [[Andrew Baker]], [[Birgit Richter]] _Structured ring spectra_, London Mathematical Society Lecture Notes Series 315, Springer 2004

A comprehensive account for [[symmetric spectra]] is in

* {#Schwede12} [[Stefan Schwede]], _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

and for [[orthogonal spectra]] in

* [[Stefan Schwede]], _[[Global homotopy theory]]_

An account in terms of [[(∞,1)-category theory]] is in section 7.1 of

* [[Jacob Lurie]], _[[Higher Algebra]]_

Discussion of [[simplicial ring|simplicial]] ring spectra is in

* {#GoerssHopkins99} [[Paul Goerss]], [[Michael Hopkins]], _Simplicial Structured Ring Spectra_ (1999) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.34.9216))


See also the references at [[stable homotopy theory]].

* Glossary for stable and chromatic homotopy theory ([[StableChromaticGlossary.pdf:file]])



[[!redirects ring spectra]]

[[!redirects commutative ring spectrum]]
[[!redirects commutative ring spectra]]

[[!redirects homotopy ring spectrum]]
[[!redirects homotopy ring spectra]]

[[!redirects homotopy commutative ring spectrum]]
[[!redirects homotopy commutative ring spectra]]
[[!redirects homotopy-commutative ring spectrum]]
[[!redirects homotopy-commutative ring spectra]]

[[!redirects H-ring spectrum]]
[[!redirects H-ring spectra]]

[[!redirects H ring spectrum]]
[[!redirects H ring spectra]]
