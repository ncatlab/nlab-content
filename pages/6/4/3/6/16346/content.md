
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

While _[[Cartan geometry]]_ was originally conceived of in the context of [[differential geometry]], its principles and constructions make sense much more generally. In particular they make sense in the context of [[supergeometry]]. The implementation of Cartan geometry in supergeometry may well be called _super-Cartan geometry_ or _Cartan super-geometry_.

While this terminology has not been used traditionally, nevertheless key ingredients of super-Cartan geometry are well known in the literature, and all the more is it useful to make them explicit as what they are.

Essentially all of the [[supergravity]] literature in [[physics]] is about super-Cartan geometry for the inclusion of a [[Lorentz group]] inside a [[super Poincare group]], in direct analogy to how ordinary [[Einstein gravity]] ([[pseudo-Riemannian geometry]]) is the Cartan geometry of the inclusion of a Lorentz group inside a plain [[Poincare group]] -- this in fact being Cartan's original and motivating example for the whole theory. Where physicists speak of "locally gauging [[supersymmetry]]" the mathematical formulation of that is precisely this: the "[[supersymmetry]]" [[supergroup]] is the [[super Poincare group]] [[action|acting]] on [[super Minkowski spacetime]], and "locally gauging" it means exactly to consider [[spacetimes]] that are locally ([[tangent space]]-wise) modeled on [[super Minkowski space]], while globally varying according to a [[Lorentz group]]-[[G-structure]], hence the super-analog of a [[pseudo-Riemannian metric]].

Physics literature usually refers to the "superspace formulation" of supergravity when referring to the formulation of the theory in [[supergeometry]]. One physics references which moreover makes the super-Cartan-geometric picture of [[supergravity]] very explicit is ([D'Auria-Fre 82](#DAuriaFre82), [Castellani-D'Auria-Fre 91](#CastellaniDAuriaFre91)). (These authors in fact also make the [[higher Cartan geometry]] hidden here fairly explicit, see there for more.), even though these authors do not use this mathematical terminology. Similarly, discussion of super-[[Klein geometry]] in the context of [[supergravity]] is, even if not exactly in this terminology, rather explicit in ([Figueroa-O'Farrill 08](#FigueroaOFarrill08)). 

A reference that very clearly identifies the role of the mathematics of supergeometric [[G-structures]] (the relevant special class of super-Cartan geometry) in [[supergravity]] is ([Lott 01](#Lott01)). The followup ([Egeileh-Chami 13](#EgeilehChami13)) to that article finally makes the terminology "Cartan geometry" fully explicit in this supergeometric context. These authors observe for instance that from this perspective the traditional concept of _[[Killing spinor]]_ -- which involves an extra "weakening" parameter in addition to the plain concept of a _[[covariantly constant spinor]]_ -- is naturally understood as being in fact a covariantly constant spinor, but for a different model super-[[Klein geometry]] $G/H$.


This provides ample example and application of super-Cartan geometry for the case where $G/H$ is a [[super vector space]], hence for the case corresponding to [[G-structure]]. More general super-Cartan geometry apparently remains to be explored.

Notice however that a crucial difference to bosonic $G$-structure is that [[super Euclidean spaces]] and [[super-Minkowski spacetimes]], have nontrivial [[supergroup]] structure, which is crucially reflected in the fact that the [[left-invariant 1-forms]] ([[super differential forms]]) on these spaces are _not_ closed. This means that they carry natural intrinsic [[torsion of a G-structure]],. Due to this fact the super-Cartan geometry involved in [[supergravity]] is richer than its bosonic counterpart in a way that goes beyond the addition of "superpartners". For more on this see also at _[[torsion constraints of supergravity]]_.


## References

* {#DAuriaFre82}  [[Riccardo D'Auria]], [[Pietro Fré]] _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) 101-140 

* {#CastellaniDAuriaFre91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* {#Lott01} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_ Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

* {#FigueroaOFarrill08} [[José Miguel Figueroa-O'Farrill]], _The homogeneity conjecture for supergravity backgrounds_, J.Phys.Conf.Ser.175:012002, 2009 ([arXiv:0812.1258](http://arxiv.org/abs/0812.1258))

* {#EgeilehChami13} Michel Egeileh, Fida El Chami, _Some remarks on the geometry of superspace supergravity_, J.Geom.Phys. 62 (2012) 53-60 ([spire](http://inspirehep.net/record/1333125))
