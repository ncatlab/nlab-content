

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A __hyperstonean space__ (French: *espace hyperstonien*)
is a [[Stonean space]] such that the [[union]] of supports of all normal measures is [[everywhere dense]].

Here a __normal measure__ is a [[Radon measure]] that vanishes on [[nowhere dense]] subsets.

## Properties

The support of a normal measure is a [[clopen]] subset.

In a hyperstonean space, all [[meager subsets]] are [[nowhere dense]] and the support of any normal measure is a [[clopen subset]].

Every [[Stonean space]] decomposes as a [[coproduct]] of three [[clopen subsets]] $E_1$, $E_2$, and $E_3$ with the following properties:

* $E_1$ has an [[everywhere dense]] [[meager subset]].  The only normal measure on $E_1$ is the zero measure.

* $E_2$ is a hyperstonean space.

* Every [[meager subset]] of $E_3$ is [[nowhere dense]] and every [[Radon measure]] has a [[nowhere dense]] support.  The only normal measure on $E_3$ is the zero measure.

## Hyperstonean duality

By [[Gelfand-type duality for commutative von Neumann algebras]], the category of hyperstonean spaces and open continuous maps is equivalent to the opposite category of [[localizable Boolean algebras]], the category of [[measurable locales]], and the opposite category of commutative [[von Neumann algebras]].

## Hyperstonean locales

Hyperstonean locales can be defined as [[Stonean locales]] that admit sufficiently many [[normal valuation]]s.

Assuming the [[axiom of choice]], [[Stonean locales]] are [[spatial locale|spatial]], so the category of hyperstonean locales
is equivalent to the category of hyperstonean spaces.

## Hyperstonean cover

Given a [[compact Hausdorff space]] $X$, its __hyperstonean cover__ is defined as a continuous map of [[compact Hausdorff spaces]]
$$h X \to X$$
that under the [[Gelfand duality]] for commutative unital [[C*-algebras]] corresponds to the canonical inclusion $C(X)\to C(X)^{**}$ into the double dual.

## References

Hyperstonean spaces were introduced and studied by [[Jacques Dixmier]]:

* [[Jacques Dixmier]], _Sur certains espaces considérés par M. H. Stone_. Summa Brasiliensis Mathematicae 2, (1951), 151–182.  [PDF](https://dmitripavlov.org/scans/dixmier.pdf)

An expository account is given by [[Masamichi Takesaki]] in

* [[Masamichi Takesaki]], _Theory of Operator Algebras_, Chapter III, Section 1.

The hyperstonean cover of a [[compact Hausdorff space]] is introduced in

* J. Flachsmeyer, _Topologization of Boolean algebras_, General Topology and Its Relations to Modern Analysis and Algebra IV, Lecture Notes in Mathematics 609 (1977), 81–97.  [doi](http://dx.doi.org/10.1007/bfb0068674).

A bibliography of hyperstonean covers can be found in

* V. K. Zaharov, _Hyperstonean cover and second dual extension_, Acta Mathematica Hungarica 51:1-2 (1988), 125-149.  [doi](http://dx.doi.org/10.1007/bf01903626).

[[!redirects hyperstonean spaces]]
[[!redirects hyperstonean topological space]]
[[!redirects hyperstonean topological spaces]]
[[!redirects normal measure]]
[[!redirects normal measures]]
[[!redirects hyperstonean locale]]
[[!redirects hyperstonean locales]]
[[!redirects hyperstonean cover]]
[[!redirects hyperstonean covers]]
[[!redirects hyperstonean duality]]