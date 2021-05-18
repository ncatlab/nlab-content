
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


### Algebraically

A _spectral triple_ ([Connes-Moscovici 95](#ConnesMoscovici95)) is [[operator algebra|operator algebraic]] data that mimics the geometric data provided by a [[smooth manifold|smooth]] [[Riemannian manifold]] $X$ with [[spin structure]] ([Connes 08](#Connes08)) and generalizes it to [[noncommutative geometry]]. It is effectively a [[Fredholm module]] with possibly unbounded [[Fredholm operator]] and refined by the specification of a [[dense subalgebra]] of the [[C-star-algebra]] of bounded operators on that module. As such, spectral triples have close ties to [[algebraic K-theory]] and so also to the [[physics]] described by these (see also at _[[spectral action]]_).

In a little more detail, a spectral triple consists of

1. a $\mathbb{Z}_2$-graded [[Hilbert space]] $\mathcal{H}$, to be thought of as the space of (square integrable) [[sections]] of the [[spinor bundle]] of $X$;

1. An [[associative algebra]] $A$ with a [[dense subalgebra|dense embedding]] $A \hookrightarrow B(H)$ into the [[C-star-algebra]] of [[bounded operators]] on $H$, to be thought of as the algebra of [[smooth functions]] on $X$;

   These two items encode the [[topology]] and [[smooth structure]].

1. A [[Fredholm operator]] $D$ acting on $\mathcal{H}$ and satisfying some conditions, to be thought of as the [[Dirac operator]] acting on the spinors.

   This item encodes the [[Riemannian metric]] and possibly a [[connection on a bundle|connection]].


(This is, or is a slight variant of, the concept of an unbounded [[Fredholm modules]] (e.g. [Carey-Philips 98](#CareyPhilips98)))

Below we discuss how one may think  of a spectral triple as being precisely the algebraic data of [[supersymmetric quantum mechanics]] defining the worldvolume [[QFT]] of the quantum [[relativistic particle|super particle]] propagating on a Riemannian target space (a [[sigma-model]].) Accordingly this is just the beginning of a pattern. One degree up a [[2-spectral triple]] is algebraic data encoding a Riemannian manifold with [[string structure]].

### As 1-dimensional FQFTs
 {#As1DimensionalFQFTs}

Here is an **unorthodox way** to state the idea of spectral triple in terms of [[FQFT]], which is in part just the reformulation of the [[quantum mechanics]] motivation that [[Alain Connes]] derived his definition from in the modern light of [[FQFT]], but which more concretely follows work by [[Maxim Kontsevich|Kontsevich]]-[[Yan Soibelman|Soibelman]], see  ([Soibelman 11](#Soibelman11)) and see the references at _[[2-spectral triple]]_. 

> (but maybe eventually we should have a traditional idea section and move this here to a subsection on further interpretations)

Let $R Cob_{1|1}^{Feyn}$ be the [[cobordism category]] of [[Feynman graph]]s for the [[superparticle]] with a single type of interaction along the lines of [[(1,1)-dimensional Euclidean field theories and K-theory]]. So its morphisms are generated from $(1|1)$-dimensional super-Riemannian manifolds (i.e. super-intervals) and from a single interaction vertex

$$
  \array{
    \bullet
    \\
    & \searrow
    \\
    && \bullet & \to
    \\
    & \nearrow
    \\
    \bullet
  }
$$

subject to the obvious associativity condition.

Then a spectral triple $(A,H,D)$ is the data encoding a sufficiently nice smooth [[functor]] 

$$
  Z_{(A,H,D)} : R Cob_{1|1}^{Feyn}  \to sVect
$$

to the [[category]] of [[super vector space]]s.

Here

* $A = Z_{(A,H,D)}(\bullet)_0$ is the even part of the [[super vector space]] assigned by the functor to the point, equipped with the structure of a [[algebra]] whose product is given by the image of the interaction vertex

  $$
    Z_{(A,H,D)}
    \left(
  \array{
    \bullet
    \\
    & \searrow
    \\
    && \bullet & \to
    \\
    & \nearrow
    \\
    \bullet
  }
    \right)
  $$

* $H$ is some completion of $Z_{(A,H,D)}(\bullet)$  to a [[super Hilbert space]]

* and $D \in End(H)$ is an odd self-adjoint operator on $H$, which gives the value of the functor on the super-interval $(t,\theta)$ by

  $$
    (t,\theta) \mapsto \exp( - t D^2 + \theta D )
    \,.
  $$ 

(For technical details that I am glossing over see the field theory link above).

So this is the [[quantum mechanics]] of a [[superparticle]]. In the simplest case this comes from a spinor particle propagating on a [[spin structure]] [[Riemannian manifold]] $X$in which case

* $H = L^2(S)$ is the space of square integrable spinor sections;

* $D$ is the [[Dirac operator]]

* $A = C^\infty(X)$ is the space of smooth functions on $X$.

One point of a spectral triple is to take the view of world-line [[quantum mechanics]] as basic and _characterize_ the spin Riemannian geometry of $X$ entirely by this algebraic data. In particular the [[Riemannian metric]] on $X$ is encoded in the [[operator spectrum]] of $D$, which is where the notion "spectral triple" gets its name from.

Then with all the ordinary geoemtry re-encoded algebraically this way, in terms of the 1-dimensional [[quantum field theory]] that _probes_ this geometry, one can then use the same formulas to interpret spectral triple geometrically that do _not_ come from an ordinary geometry as in the above example.

## Properties


### Metric dimension and KO-dimension

For a space described by a spectral triple there are several notions of [[dimension]] which all coincide when the space is a classical [[smooth manifold]] but which may differ on more general spectral spaces.

Notably there is the [[metric dimension]], which determines the growth of the [[eigenvalues]] of the [[Dirac operator]] ([Connes95, p. 6](#Connes95)).

And then there is the [[KO-dimension]].


## Related concepts

* [[spectral geometry]]

* [[hearing the shape of a drum]]

* [[KK-theory]]

* [[spectral action]]

* [[Connes-Lott-Chamseddine model]]

* [[higher category theory and physics]]: _[Spectral standard model and gravity](higher+category+theory+and+physics#SpecStandModAndGravity)_

* [[(1,1)-dimensional Euclidean field theories and K-theory]]
  
* [[2-spectral triple]]


## References

### General

The standard textbook is

* [[Alain Connes]], _Noncommutative Geometry_ , Academic Press (1994)

See also 

* [[Alain Connes]], [[Matilde Marcolli]], chapter I, section 10 of _[[Noncommutative Geometry, Quantum Fields and Motives]]_


The terminology  of spectral triples was introduced in

* {#ConnesMoscovici95} [[Alain Connes]], [[Henri Moscovici]],  _The Local Index Formula in Noncommutative Geometry_, Geometry and Funct. Analysis 5 (1995) 174-243.

* {#Connes95} [[Alain Connes]], _Noncommutative geometry and reality_, J. Math. Phys. 36 (11), 1995 ([doi:10.1063/1.531241](https://doi.org/10.1063/1.531241))

and that of [[spectral action]] in

* [[Alain Connes]], _Gravity coupled with matter and foundation of non-commutative geometry_ ([arXiv:hep-th/9603053](http://arxiv.org/abs/hep-th/9603053))

The characterization of ordinary [[compact space|compact]] [[smooth manifolds]] with [[spin structure]] in terms of spectral triples is in 

* {#Connes08} [[Alain Connes]], _On the spectral characterization of manifolds_ ([arXiv:0810.2088](http://arxiv.org/abs/0810.2088))

See also

* {#CareyPhilips98} [[Alan Carey]], John Phillips, _Fredholm modules and spectral flow_  J. Canadian Math. Soc. **50** (1998) 673-718. ([publisher](https://cms.math.ca/10.4153/CJM-1998-038-x))

* R. da Rocha, A. A. Tomaz, _Hearing the shape of inequivalent spin structures and exotic Dirac operators_ ([arXiv:2003.03619](https://arxiv.org/abs/2003.03619))

Traditionally spectral triples are discussed without specifying their [[homomorphisms]]. Proposals to remedy this such as to obtain a sensible [[category]] of spectral triples include the following

* {#BCL05} [[Paolo Bertozzini]], [[Roberto Conti]], Wicharn Lewkeeratiyutkul, _A Category of Spectral Triples and Discrete Groups with Length Function_, Osaka Journal of Mathematics, 43 n. 2, 327-350 (2006) ([arXiv:math/0502583](http://arxiv.org/abs/math/0502583))

* {#BCL08} [[Paolo Bertozzini]], [[Roberto Conti]], Wicharn Lewkeeratiyutkul, _Non-Commutative Geometry, Categories and Quantum Physics_, East-West Journal of Mathematics "Contributions in Mathematics and Applications II" Special Volume 2007, 213-259 (2008) ([arXiv:0801.2826](http://arxiv.org/abs/0801.2826))



(See also the pointers concerning the relation to [[KK-theory]] [below](#ReferencesRelationToKKTheory)).

Spectral triples over [[Jordan algebras]]:

* Latham Boyle, Shane Farnsworth,
_The standard model, the Pati-Salam model, and "Jordan geometry"_ ([arxiv:1910.11888](https://arxiv.org/abs/1910.11888))

See also


* Ludwik Dabrowski, Andrzej Sitarz, _Multiwisted real spectral triples_ ([arXiv:1911.12873](https://arxiv.org/abs/1911.12873))


### Relation to quantum physics 

A discussion of spectral triples as [[FQFT]] data encoding a [[representation]] of a category of 1-dimensional [[cobordisms]] with [[Riemannian manifold|Riemannian]] structure and vertices is in section 1.4 of 

* {#Soibelman11} [[Yan Soibelman]], _Collapsing Conformal Field Theories, spaces with non-negative Ricci curvature and non-commutative geometry_, in [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_, Proceedings of Symposia in Pure Mathematics, AMS 2011

A brief indication of some of the central ideas going into this is at

* [[Urs Schreiber]],  _[Spectral triples and graph field theory](http://golem.ph.utexas.edu/category/2007/06/had_the_pleasure_of_talking.html)_


A general introduction to and discussion of spectral triples with an eye on [[quantum mechanics]], [[quantum field theory]] and [[string theory]] is in

* [[Jürg Fröhlich]], Oiver Grandjean, [[Andreas Recknagel]], _Supersymmetric quantum theory, non-commutative geometry, and gravitation_  Lecture Notes Les Houches (1995) ([arXiv:hep-th/9706132](http://arxiv.org/abs/hep-th/9706132))

In section 7.2 of this an outlokk on how to regard the [[string theory|string's]] worldvolume [[CFT]] as a [[2-spectral triple]] is given.

A detailed derivation for how spectral triples arise as point particle limits of [[vertex operator algebra]]s for 2d [[CFT]]s:

* [[Daniel Roggenkamp]], [[Katrin Wendland]], _Limits and Degenerations of Unitary Conformal Field Theories_ ([arXiv:hep-th/0308143](http://arxiv.org/abs/hep-th/0308143))

A summary of this is in

* [[Daniel Roggenkamp]], [[Katrin Wendland]], _Decoding the geometry of conformal field theories_ ([arXiv:0803.0657](http://arxiv.org/abs/0803.0657))

Also

* [[Sebastiano Carpi]], Robin Hillier, [[Yasuyuki Kawahigashi]], [[Roberto Longo]], _Spectral Triples and the Super-Virasoro Algebra_ Communications in Mathematical Physics, Volume 295, Number 1 / April 2010 ([Springer pdf](http://www.springerlink.com/content/316wx4r4x885172w/fulltext.pdf))


Discussion in the context of [[D-brane]] [[matrix models]] is in

* T. Asakawa, S. Sugimoto, S. Terashima, _D-branes, Matrix Theory and K-homology_, JHEP 0203 (2002) 034 ([arXiv:hep-th/0108085](http://arxiv.org/abs/hep-th/0108085))

### von Neumann spectral triples 

One variation uses [[von Neumann algebras]] instead of [[C-star algebras]].

This goes back to ([Carey-Philips 98](#CareyPhilips98)) and 

* Alan L Carey, John Phillips, Fyodor Sukochev, _On unbounded $p$-summable Fredholm modules_ ([arXiv:math/9908091](http://arxiv.org/abs/math/9908091))

See also

* M-T. Benameur, T. Fack,, _Type II non-commutative geometry. I. Dixmier trace in von Neumann algebras_, Advances in Mathematics 199: 29-87, 2006.

* [[Alain Connes]], [[Henri Moscovici]], _Type III and spectral triples_ ([arXiv:math/0609703](http://arxiv.org/abs/math/0609703))


### Relation to K-theory
 {#ReferencesRelationToKKTheory}

Relation to [[K-theory]] and [[KK-theory]] is discussed in

* ([pdf](http://www.math.sc.chula.ac.th/cimpa/sites/default/file/bangkoknotes.pdf&#8206;))

* [[Bram Mesland]], _Spectral triples and KK-theory: A survey_ ([arXiv:1304.3802](http://arxiv.org/abs/1304.3802))

* [[Alan Carey]], John Philips, Adam Rennie, _Spectral triples: examples and index theory_, in Alan Carey (ed.) _Noncommutative geometry and physics, Renormalization, Motives, Index theory_ (2011)

### Examples

On the [[spectral triple|spectral]] [[Riemannian geometry]] of the [[fuzzy 2-sphere]]:

* [[Francesco D'Andrea]], [[Fedele Lizzi]], [[Joseph Várilly]], _Metric Properties of the Fuzzy Sphere_, Lett. Math. Phys.103 (2013), 183-205 ([arXiv:1209.0108](https://arxiv.org/abs/1209.0108))




[[!redirects spectral triples]]
[[!redirects graph field theory]]

[[!redirects unbounded Fredholm module]]
[[!redirects unbounded Fredholm modules]]