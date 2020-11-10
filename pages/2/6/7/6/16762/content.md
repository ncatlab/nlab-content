
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

Given a [[space]] $X$ of sorts, in particular a [[scheme]] or [[variety]], with [[singularities]], i.e. with a subspace $S \subset X$ at which the [[geometry]] is non-regular (specifically: not [[smooth scheme|smooth]]), a _resolution_ of the singularity is a suitable regular (non-singular) space
$\widehat X$ equipped with a [[morphism]] back to the original space

$$
  p \;\colon\; \widehat X \longrightarrow X
$$

which is an [[isomorphism]] away from the singular locus.

Typical resolution of singularities is by "blow-up" of the singularity where the singular point is replaced by an [[n-sphere]]/[[projective space]] (and its neighbourhood by a [[tautological line bundle]]), then called the "exceptional [[divisor (algebraic geometry)|divisor]]" of the blow-up.

(quick review of the basic details includes [Berghoff 14, section 4.1](#Berghoff14))



## Examples

* the [[Fulton-MacPherson compactification]] of [[configuration spaces of points]] may be regarded as resolution of the [[fat diagonal]] inside an iterated [[Cartesian product]];

* this generalizes to  "[[wonderful compactifications]]" resolving singularities given by more general subspace arrangements

* [[Bridgeland stability]] over resolution of [[ADE-singularities]]: see [there](Bridgeland+stability+condition#OverResolutionsOfADESingularities)

## Related concept

* [[ADE singularity]]

  * [[M-theory lift of gauge enhancement on D6-branes]]

  * [[triple membrane junction]]

* [[tautological line bundle]]

  [[tautological equivariant line bundle]]

## References

The existence of resolutions of singularities by "blow-up" was established, for [[ground fields]] of [[characteristic zero]], in some generality in

* {#Hironaka64} [[Heisuke Hironaka]], _Resolution of Singularities of an Algebraic Variety Over a Field of Characteristic Zero: I_, Annals of Mathematics Second Series, Vol. 79, No. 1 (Jan., 1964), pp. 109-203 (95 pages) ([jstor:1970486](https://www.jstor.org/stable/1970486))

Basic review includes

* {#Berghoff14} [[Marko Berghoff]], section 4 of _Wonderful renormalization_, 2014 ([pdf](http://www2.mathematik.hu-berlin.de/%7Ekreimer/wp-content/uploads/Berghoff-Marko.pdf), [doi:10.18452/17160](https://doi.org/10.18452/17160))


The theorem of [Hironaka 64](#Hironaka64) was used to discuss singular [[distributions]] (in the sense of [[generalized functions]]) in

* {#Atiyah70} [[Michael Atiyah]], _Resolution of singularities and Division of Distributions_, Communications in Pure and Applied Mathematics, vol. XXIII, 145-150, 1970 ([doi:10.1002/cpa.3160230202](https://doi.org/10.1002/cpa.3160230202))

This method is closely related to the resolution of singularities of [[propagators]]/[[Feynman amplitudes]] by passage to [[Fulton-MacPherson compactification|compactified]] [[configuration spaces of points]], as disucussed at _[[Feynman amplitudes on compactified configuration spaces of points]]_.

See also

* Wikipedia, _[Resolution of singularities](https://en.wikipedia.org/wiki/Resolution_of_singularities)_

* Wikipedia, _[Blowing up](https://en.wikipedia.org/wiki/Blowing_up)_

* Wikipedia, _[Exceptional divisor](https://en.wikipedia.org/wiki/Exceptional_divisor)_

[[!redirects resolutions of singularities]]

[[!redirects crepant resolution]]
[[!redirects crepant resolutions]]

[[!redirects blowing up]]
[[!redirects blow up]]
[[!redirects blow-up]]
[[!redirects blowup]]

[[!redirects exceptional divisor]]
[[!redirects exceptional divisors]]
