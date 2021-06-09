
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The formulation of the [[sigma-model]] 2d [[CFT]]s that are used in (super) [[string theory]] had originally been of two types:

1. In the [[RNS-string]] forumlation the worldsheet is a [[supermanifold]], while the target space is an ordinary [[manifold]].

   The advantage of this formulation is that its [[quantization]] is comparatively tractable: it is a 2-dimensional superconformal field theory, coming with a super [[vertex operator algebra]].

   The disadvantage is that, as one says, "target space supersymmetry is not manifest": as described at [[string theory]], every 2d CFT gives rise to an effective background [[quantum field theory]] (that quantum field theory whose [[S-matrix]] approximates the [[S-matrix]] obtained by evaluating the given CFT correlators on all possible surfaces and summing over the conformal [[moduli space]] and all genera). One can identify explcitly in the [[vertex operator algebra]] of the 2d CFT those operators that correspond to the fields of this effective background field theory (the _vertex operators_). One finds that these fields are those of a theory of [[supergravity]] and [[super Yang-Mills theory]]. So in particular there is a [[super Lie algebra]] acting on them. But this "supersymmetry" of the effective target space theory appears like an accident if one unwraps all this: there is no structural one-line argument (known) that would guarantee that the effective background quantum field theory of a 2d super [[CFT]] is itself supersymmetric.

1. In the [[Green-Schwarz superstring]] [[sigma-model]] formulation, the [[worldsheet]] is an ordinary [[manifold]], but target space is a [[supermanifold]].

   This has the immediate advantage that target space supersymmetry is now "manifest": as described at [[supergravity]] it is just the super-[[diffeomorphism]] invariance of the theory, and the [[sigma-models]] in question all manifestly have this property.

The big disadvantage is, that it is not known how to [[quantization|quantize]] this system. The reason is that the standard procedure for quantization shows that the GS-type sigma models are [[constrained mechanics|constrained]] systems with second-class constraints. Little to nothing is known how to deal with that.

Berkovits was motivated by the desire to find a formulation of the superstring sigma model CFT that would combine the advantages of both the RNS formulation and the Green-Schwarz formulation. The goal was to have a CFT that looked like a free field theory (as the RNS string does for a flat Minkowski background, but as the GS string does not) if one just looked at a small part of the range of its fields, but which was globally constrained: the spinorial worldsheet fields here are maps into a space of [[pure spinor]]s that locally lools like a Euclidean space, but globally has a cone geometry (...details...).

Berkovits originally wrote down some more or less ad-hoc expressions. Later it was understood that what described is a _[[sheaf]] of vertex operator algebras_ (in general, not a [[sheaf]] but a [[stack]], in fact a [[gerbe]]) on target space: to each contractible open patch of target space is associate the [[vertex operator algebra]] of a free [[sigma-model]] CFT whose fields take values _just_ in that patch, such that on overlaps these vertex operator algebras glue in some way.

This at once made the previously mathemtically rather unjustified approach make close contact with the developing theory of [[chiral deRham complex]], which is one of the most-studied examples of sheaves of vertex operator algebras.

## Related concepts

* [[superstring]]

* [[string scattering amplitude]]

## References

### General

The original articles:

(...)

Relation to the [[RNS string]]:

* [[Nathan Berkovits]], *Manifest Spacetime Supersymmetry and the Superstring* ([arXiv:2106.04448](https://arxiv.org/abs/2106.04448))

### Sheaf ov VOAs

A good reference that explains the sheaf of vertex operator algebra perspective on the Berkovits superstring is

* Nikita Nekrasov, _Lectures on curved $\beta$-$\gamma$ systems, pure spinors, and anomalies_ ([arXiv](http://arxiv.org/abs/hep-th/0511008))

The standard reference on the closely related mathematical theory of the chiral deRham complex is

* [[Vassily Gorbounov]], Fyodor Malikov, [[Vadim Schechtman]], _Gerbes of chiral differential operators_  Math. Res. Lett. __7__ (2000),  no. 1, 55--66, [MR2002c:17040](http://www.ams.org/mathscinet-getitem?mr=2002c:17040), [math.AG/9906117](http://arxiv.org/abs/math/9906117); _Gerbes of chiral differential operators. II. Vertex algebroids_, Invent. Math. __155__ (2004), no. 3, 605--680, [MR2005e:17047](http://www.ams.org/mathscinet-getitem?mr=2005e:17047), [math.AG/0003170](http://arxiv.org/abs/math/0003170), [doi](http://dx.doi.org/10.1007/s00222-003-0333-4); _Gerbes of chiral differential operators. III_, in: The orbit method in geometry and physics (Marseille, 2000),  73--100, Progr. Math. __213__, Birkh&#228;user 2003, [MR2005a:17028](http://www.ams.org/mathscinet-getitem?mr=2005a:17028), [math.AG/0005201](http://arxiv.org/abs/math/0005201), _On chiral differential operators over homogeneous spaces_, Int. J. Math. Math. Sci. __26__ (2001), no. 2, 83--106, [MR2002g:14020](http://www.ams.org/mathscinet-getitem?mr=2002g:14020), [math.AG/0008154](http://arxiv.org/abs/math/0008154), [doi](http://dx.doi.org/10.1155/S0161171201020051)



Here is some blog discussion about this topic:

* [[Jacques Distler]]

  * _[CDO and pure spinors](http://golem.ph.utexas.edu/~distler/blog/archives/000664.html)_

  * _[Nekrasov on pure spinors](http://golem.ph.utexas.edu/~distler/blog/archives/000670.html)_


* [[Urs Schreiber]]

  * _[Nekrasov on pure spinor superstring](http://golem.ph.utexas.edu/string/archives/000661.html)_

    _[Sheaves of CDOs](http://golem.ph.utexas.edu/string/archives/000668.html)_