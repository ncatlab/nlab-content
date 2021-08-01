
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _3-manifold_ is a [[manifold]] of [[dimension]] 3. (Our default meaning of "manifold" is [[topological manifold]], unless a qualifier is added, e.g., *smooth* manifold.) 

## Properties

### Triangulability and smoothing 

The following is taken from [Hatcher](#Hatcher): 

> A pleasant feature of 3-manifolds, in contrast to higher dimensions, is that there is no essential difference between smooth, piecewise linear, and topological manifolds. It was shown by Bing and [Moise](#Moise52) in the 1950s that [[triangulation theorem|every topological 3-manifold can be triangulated]] as a simplicial complex whose combinatorial type is unique up to subdivision. And every triangulation of a 3-manifold can be taken to be a smooth triangulation in some differential structure on the manifold, unique up to diffeomorphism.  Thus every topological  3-manifold has a unique smooth structure, and the classifications up to diffeomorphism and homeomorphism coincide. 

Thus it makes no essential difference if we consider 3-manifolds as mere topological manifolds, or as [[piecewise-linear manifolds]] or [[smooth manifolds]]. It's often technically convenient to work in the smooth category. 

### Poincar&#233; conjecture

+-- {: .num_theorem}
###### Theorem
**([[Poincaré conjecture]])**

Every [[simply connected]] [[compact space|compact]] 3-manifold without boundary is [[homeomorphism|homeomorphic]] to the 3-sphere.

=--

+-- {: .proof}
###### Proof


A proof strategy was given by [[Richard Hamilton]]: imagine the manifold is equipped with a [[metric]]. Follow the [[Ricci flow]] of that metric through the space of metrics. As the flow proceeds along parameter time, it will from time to time pass through metrics that describe singular geometries where the compact metric manifold pinches off into separate manifolds. Follow the flow through these singularities and then continue the flow on each of the resulting components. If this process terminates in finite parameter time with the metric on each component stabilizing to that of the round 3-sphere, then the original manifold was a 3-sphere.

The hard technical part of this program is to show that the passage through the  singularities can be controlled. This was finally shown by [[Grigori Perelman]].

=--

### Geometrization conjecture

The _[[geometrization conjecture]]_ says that every closed 3-manifold can be decomposed in a canonical way into pieces that each have one of eight types of geometric structure.

### Virtually fibered conjecture

The _[[virtually fibered conjecture]]_ says that every closed, irreducible, atoroidal 3-manifold with infinite fundamental group has a finite cover which is a surface bundle over the circle.

## Related concepts

* [[irreducible 3-manifold]]

* [[atoroidal 3-manifold]]

* [[Seifert 3-manifold]]

* [[hyperbolic 3-manifold]]

* [[Dehn surgery]]

* [[Kirby calculus]]

* [[low dimensional topology]]

* [[knot theory]]

* [[arithmetic topology]]

* [[Chern-Simons theory]]

* [[Atiyah 2-framing]]

* [[lens space]]

* [[associative submanifold]]

* [[2-manifold]], [[4-manifold]], [[8-manifold]]

## References

### General


Review:

* {#Thurston80} [[William Thurston]], _Geometry and topology of three-manifolds_ (1980), electronic version 1.1 (2002) available from MSRI ([web](http://library.msri.org/books/gt3m/))

* {#Hatcher}  [[Allen Hatcher]], _The classification of 3-manifolds -- a brief overview_, ([pdf](https://www.math.cornell.edu/~hatcher/Papers/3Msurvey.pdf)). 

* {#Martelli16} Bruno Martelli, _An Introduction to Geometric Topology_ ([arXiv:1610.02592](https://arxiv.org/abs/1610.02592))

The [[triangulation theorem]] for [[3-manifolds]]:

* {#Moise52} [[Edwin E. Moise]],  *Affine Structures in 3-Manifolds: V. The Triangulation Theorem and Hauptvermutung*, Annals of Mathematics Second Series, Vol. 56, No. 1 (Jul., 1952), pp. 96-114 ([doi:10.2307/1969769](https://doi.org/10.2307/1969769), [jstor:1969769](https://www.jstor.org/stable/1969769))


3-manifolds as [[branched covers]] of the [[3-sphere]]:

*  J. Montesinos, _A representation of closed orientable 3-manifolds as  3-fold branched coverings of $S^3$_, Bull. Amer. Math. Soc. 80 (1974), 845-846 ([Euclid:1183535815](https://projecteuclid.org/euclid.bams/1183535815))

See also

* {#BottCattaneo98} [[Raoul Bott]], [[Alberto Cattaneo]], _Integral Invariants of 3-Manifolds_, J. Diff. Geom., 48 (1998) 91-133 ([arXiv:dg-ga/9710001](https://arxiv.org/abs/dg-ga/9710001))

### Hyperbolic 3-manifolds

On [[hyperbolic 3-manifolds]]:

* [[William Thurston]], _Hyperbolic Structures on 3-manifolds, I: Deformation of acylindrical manifolds_, Annals of Math, 124 (1986), 203--246 ([jstor:1971277](https://www.jstor.org/stable/1971277), [arXiv:math/9801019](https://arxiv.org/abs/math/9801019))

* [[William Thurston]], _Hyperbolic Structures on 3-manifolds, II: Surface groups and 3-manifolds which fiber over the circle_ ([arXiv:math/9801045](https://arxiv.org/abs/math/9801045))

* [[William Thurston]], _Three dimensional manifolds, Kleinian groups and hyperbolic geometry_, Bull. Amer. Math. Soc. (N.S.) Volume 6, Number 3 (1982), 357-381 ([euclid.bams/1183548782](https://projecteuclid.org/euclid.bams/1183548782))



[[!redirects 3-manifolds]]
