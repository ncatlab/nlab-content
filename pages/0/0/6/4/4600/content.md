
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Ordinary differential cohomology is the [[differential cohomology]]-refinement of [[ordinary cohomology]], for instance realized as [[singular cohomology]].

Every [[generalized (Eilenberg-Steenrod) cohomology]]-theory has a refinement to [[differential cohomology]]. By _ordinary differential cohomology_ one refers, for emphasis, to the differential refinement of _ordinary [[integral cohomology]]_ , hence of the [[cohomology theory]] represented by the [[Eilenberg-MacLane spectrum]] $K(-,\mathbb{Z})$. To the extent that [[integral cohomology]] is often just called _cohomology_ when the context is clear, _ordinary differential cohomology_ is often called just _differential cohomology_ .

Ordinary differential cohomology classifies [[circle n-bundles with connection]]. In low degree these are ordinary [[circle bundle]]s with [[connection on a bundle|connection]]. In the next degree they are [[circle 2-group]] [[principal 2-bundles]] / [[bundle gerbes]] with [[connection on a 2-bundle|2-connection]].




## Properties

Here we write $H_{diff}^\bullet(X)$ for the ordinary differential cohomology groups of a [[smooth manifold]] $X$. 


### Curvature and characteristic class
 {#CurvatureAndCharClass}
 {#AbstractProperties}

There are two [[natural transformation|natural]] morphisms:

1. The underlying [[characteristic class]] 

   $$
     c : H_{diff}^\bullet(X) \to H^\bullet(X,\mathbb{Z})
   $$ 

   produces the class in [[integral cohomology]] that underlies a differential cocycle;

   * for $H^2_{diff}(X)$ this is called the first [[Chern class]] of a [[line bundle]];

   * for $H^3_{diff}(X)$ this is called the [[Dixmier-Douady class]] of the corresponding [[bundle gerbe]].

1. The [[curvature]] 

   $$
    F : H_{diff}^\bullet(X) \to \Omega^\bullet_{cl}(X)
   $$ 

   produces a closed [[differential form]] of degree $n$. This happens to land in closed differential forms with integral [[period]]s (see [below](#AbstractProperties)).



The following is either a definition, if regarded as an axiomatic characterization of ordinary differential cohomology, or it is a proposition, if regarded as a property of one of the [models](#Models).

Let $X$ be a [[smooth manifold]] and $n \in \mathbb{N}$ with $n \geq 1$ Write

* $H_{diff}^n(X)$ for the ordinary differential cohomology of $X$ in degree $n$;

* $\Omega^{n-1}(X)$ for the collection of [[differential form]]s of degree $n-1$;

* $\Omega^{n-1}_{int}(X)$ for the collection of [[differential form]]s $\omega$ of degree $n-1$ that are closed and whose [[period]]s are integral: for every $\gamma : S^{n-1} \to X$ we have the [[integral]] $\int_{S^{n-1}} \gamma^* \omega \in \mathbb{Z} \hookrightarrow \mathbb{R}$. Similarly for $\Omega^n_{int}(X)$.

* $H^n(X, \mathbb{Z})$ and $H^n(X, U(1))$ for the ordinary cohomology (for instance modeled as [[singular cohomology]]) of $X$ with coefficients in the [[integer]]s or the [[circle group]] (regarded as a [[discrete group]]), respectively.

All of these sets are [[abelian group]]s: the forms under addition of forms, and the differential cohomology classes are defined or proven (depending on the approach, see above) to have abelian group structure such that  the maps to curvatures and characteristic classes, from [above](#CurvatureAndCharClass) are [[homomorphism]]s of [[abelian group]]s.

+-- {: .num_prop #ExactSequencesForOrdDiffCohomology}
###### Proposition

The differential cohomology $H_{diff}^n(X)$ of $X$ fits into [[short exact sequence]]s of abelian groups

1. **curvature exact sequence**

   \[
     \label{CurvatureSequence}
     0 \to H^{n-1}(X, U(1)) \to H^n_{diff}(X) \stackrel{F}{\to} \Omega_{int}^n(X) \to 0
   \]

1. **characteristic class exact sequence**

   \[
      \label{CharacteristicClassSequence}
      0 
       \to 
      \Omega^{n-1}(X)/\Omega^{n-1}_{int}(X)
       \to
      H_{diff}^n(X)
       \stackrel{c}{\to} 
      H^n(X, \mathbb{Z})
       \to
      0 
      \,.
   \]

=--

The first sequence (eq:CurvatureSequence) says in words: two circle $(n-1)$-bundles $n$ whose [[curvature]] coincides differ by a _flat_ circle (n-1)-bundle.

The second sequence (eq:CharacteristicClassSequence) says in words: two connections on the same circle $(n-1)$-bundle differ by a globally defined connection $(n-1)$-form, well defined up to addition of a form with integral periods. 

More is true: both these sequences interlock to form the hexagonal _[[differential cohomology diagram]]_ of ordinary differential cohomology. For more see at _[differential cohomology diagram -- Examples -- Deligne coefficients](differential+cohomology+diagram#DeligneCoefficients)_.

### Models
  {#Models}

There are various equivalent [[cocycle]]-models for ordinary differential cohomology. They include

* [[Cheeger-Simons differential character]]s;

* [[Deligne cohomology]];

* [[circle n-bundles with connection]].

The last of these are often known as $U(1)$-[[gerbe]]s or [[bundle gerbe]]s with connection.

Cocycles $\nabla \in H_{diff}^2(X)$ in degree 2 ordinary differential cohomology are represented by ordinary [[circle group]]-[[principal bundle]]s with [[connection on a bundle|connection]] on $X$.  The class $c(\nabla) \in H^2(X,\mathbb{Z})$ is the [[Chern class]] of the underlying circle bundle and the form $F_\nabla \in \Omega^2_{cl}(X)$ is the [[curvature]] 2-form of the connection $\nabla$.

## Fiber integration

see

* [[fiber integration in ordinary differential cohomology]]


## Applications

### In Chern-Weil theory

For $X$ a [[smooth manifold]], $G$ a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ and [[invariant polynomial]] $\langle -\rangle$ of degree $2n$, the [[Chern-Weil homomorphism]] may be refined to a morphism

$$
  H^1(X,G) \to H_{diff}^{2n}(X)
$$

from the first [[nonabelian cohomology]] of $X$ classifying $G$-[[principal bundle]]s to degree $2n$ ordinary differential cohomology.

The projection

$$
  H^1(X,G) \to H_{diff}^{2n}(X) \stackrel{c}{\to} H^{2n}(X,\mathbb{Z})
$$

is the integral [[characteristic class]] corresponding to the invariant polynomial and the projection

$$
  H^1(X,G) \to H_{diff}^{2n}(X) \stackrel{F}{\to} \Omega^{2n}_{cl}(X)
$$

is a differential form which represents the image of this class under $H^{2n}(X,\mathbb{Z}) \to H^{2n}(X,\mathbb{R})$ in [[de Rham cohomology]] (under the [[de Rham theorem]]).

### In physics

In [[physics]]

* the [[electromagnetic field]] is a cocycle in degree 2 ordinary differential cohomology 

* the [[Kalb-Ramond field]] is a cocycle in degree 3;

* the [[supergravity C-field]] is a cocycle in degree 4.

In abelian [[higher dimensional Chern-Simons theory]] in dimension $(4k+3)$ a field configuration is a cocycle in ordinary differential geometry of degree $(2k+2)$, for $k \in \mathbb{N}$.

## In a general abstract context

Ordinary differential cohomology (and indeed a [[cocycle]] model thereof) is defined generally [[internalization|internal]] to any [[cohesive (∞,1)-topos]] $\mathbf{H}$. This is discussed at 

* [cohesive (∞,1)-topos -- structures -- differential cohomology](http://ncatlab.org/nlab/show/cohesive%20%28infinity,1%29-topos%20--%20structures#DifferentialCohomology).

For the case $\mathbf{H} = $ [[Smooth∞Grpd]] this intrinsic definition reproduces the [[Deligne complex]] model. This is discussed at

* [Smooth∞Grpd -- structures -- differential cohomology](http://ncatlab.org/nlab/show/smooth%20infinity-groupoid%20--%20structures#StrucDifferentialCohomology)

## Related concepts

* [[twisted ordinary differential cohomology]]

* [[equivariant ordinary differential cohomology]]

* [[arithmetic Chow group]]

## References

For more and more original references see:

* _[[Deligne cohomology]]_

* _[[Cheeger-Simons differential characters]]_

* *[[differential cohomology]]*

Lecture notes:

* [[Byungdo Park]], *Differential cohomology and gerbes: An introduction to higher differential geometry*, lecture notes (2023) &lbrack;[pdf](https://byungdo.github.io/seminars/IMSRS.pdf), [[Park-DifferentialCohomology.pdf:file]]&rbrack;

  > (emphasis on relation to [[bundle gerbes]] [[connection on a bundle gerbe|with connection]])


For discussion in the broader context of generalized [[differential cohomology]] see

* [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_ ([arXiv](http://arxiv.org/abs/math.AT/0211216))

  * A pedestrian introduction of ordinary differential cocycles is in section 2.3 there. 

  * The systematic construction and definition via a [[homotopy pullback]] is in section 3.2.

  * The relation to Chern-Weil theory is in section 3.3.

A characterization by the two characteristic exact sequences is discussed in 

* [[James Simons]], [[Dennis Sullivan]], _Axiomatic characterization of ordinary differential cohomology_,  J Topology (2008) 1 (1): 45-56 ([arXiv:math/0701077](https://arxiv.org/abs/math/0701077), [doi:10.1112/jtopol/jtm006]( https://doi.org/10.1112/jtopol/jtm006) [web pdf](http://jtopol.oxfordjournals.org/content/1/1/45.full.pdf+html))


Discussion of [[equivariant ordinary differential cohomology]]

* [[Ernesto Lupercio]], [[Bernardo Uribe]], _Deligne Cohomology for Orbifolds, discrete torsion and B-fields_, in: _Geometric and topological methods for quantum field theory_ Proceedings, Summer School, Villa de Leyva, Colombia, July 9-27, 2001 ([arXiv:hep-th/0201184](https://arxiv.org/abs/hep-th/0201184), [spire:582101](https://inspirehep.net/literature/582101))

* [[Kiyonori Gomi]], _Equivariant smooth Deligne cohomology_, Osaka J. Math. Volume 42, Number 2 (2005), 309-337 ([euclid:ojm/1153494380](https://projecteuclid.org/euclid.ojm/1153494380))

* Andreas Kübel, [[Andreas Thom]], _Equivariant Differential Cohomology_, Transactions of the American Mathematical Society (2018) ([doi:10.1090/tran/7315](https://doi.org/10.1090/tran/7315), [arXiv:1510.06392](https://arxiv.org/abs/1510.06392))

* [[Corbett Redden]], _Differential Borel equivariant cohomology via connections_, New York Journal of Mathematics, Volume 23 (2017) 441-487 ([nyjm:23-20](http://nyjm.albany.edu/j/2017/23-20.html), [arXiv:1602.06921](https://arxiv.org/abs/1602.06921))

* [[Corbett Redden]], _An alternate description of equivariant connections_, Differential Geometry and its Applications Volume 56, February 2018, Pages 81-94 ([doi:10.1016/j.difgeo.2017.11.003](https://doi.org/10.1016/j.difgeo.2017.11.003) [arXiv:1608.01297](https://arxiv.org/abs/1608.01297))

* [[Byungdo Park]], [[Corbett Redden]], _A classification of equivariant gerbe connections_, Communications in Contemporary Mathematics **21** 02 1850001 (2019) &lbrack;[doi:10.1142/S0219199718500013](https://doi.org/10.1142/S0219199718500013)&rbrack;

* Cheng-Yong Du Xiaojuan Zhao, _Spark and Deligne-Beilinson cohomology on orbifolds_, Journal of Geometry and Physics Volume 104, June 2016, Pages 277-290 ([doi:10.1016/j.geomphys.2016.02.011](https://doi.org/10.1016/j.geomphys.2016.02.011))

* Cheng-Yong Du, Lili Shen, Xiaojuan Zhao, _Spark complexes on good effective orbifold atlases categorically_, Theory and Applications of Categories, 33(26):784-812, 2018 ([tac:33-26](http://www.tac.mta.ca/tac/volumes/33/26/33-26abs.html), [arXiv:1708.07551](https://arxiv.org/abs/1708.07551))

Discussion of variants of [[differential concretification|differentially concretified]] [[infinity-stack|higher]] [[moduli stacks]] of [[ordinary differential cohomology]] (higher [[bundle gerbes with connection]]) with application to [[higher gauge theory]]:

* [[Severin Bunk]], [[Carlos S. Shahbazi]], *Higher Geometric Structures on Manifolds and the Gauge Theory of Deligne Cohomology* &lbrack;[arXiv:2304.06633](https://arxiv.org/abs/2304.06633)&rbrack;

