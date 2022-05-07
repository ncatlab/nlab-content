
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Algebra and Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The concept of _spectral super-scheme_ is supposed to be the refinement of the concept of [[super-scheme]] as one passes to [[spectral geometry]] in the sense of [[derived algebraic geometry]] over [[E-infinity rings]] ([[E-infinity geometry]]).


## Definition
 {#Definition}

The following is an argument for a good definition of spectral supergeometry. This was originally motivated from the observation in [Kapranov 13](#Kapranov13) and uses results due to [Rezk 09](#Rezk09) and [Sagave-Schlichtkrull 2011](#SagaveSchlichtkrull11).

Observe that 

1. {#EInfinityGeometryAlreadyZGraded} [[E-∞ geometry]] is _already in itself_ a [[higher geometry|higher geometric]] version of $\mathbb{Z}$-graded supergeometry (in the sense discussed at _[[geometry of physics -- superalgebra]]_). 

   $\,$

   At the level of [[homotopy groups]] this is the following basic fact:

   For $E$ a [[homotopy commutative ring spectrum]], its [[stable homotopy groups]] $\pi_\bullet(E)$ inherit the structure of a $\mathbb{Z}$-graded [[super-commutative ring]]  (according to [this](geometry+of+physics+--+superalgebra#SupercommutativeSuperalgebraZGraded)). See at _[[Introduction to Stable homotopy theory]]_ in the section [1-2 Homotopy commutative ring spectra](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyRingSpectra) [this proposition](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum).

   $\,$

   But more is true: the $E_\infty$-analog of the [[integers]] $\mathbb{Z}$ is the [[sphere spectrum]] $\mathbb{S} \,\simeq\, \Sigma^\infty S^0$, and every [[E-infinity ring]] $(E, \cdot)$ is canonically $\mathbb{S}$-graded, in that  ([Sagave-Schlichtkrull 11, theorem 1.7-1.8](#SagaveSchlichtkrull11)):

   on [underlying](Introduction+to+Stable+homotopy+theory+--+1-1#SigmaInfinityOmegaInfinity) [[E-infinity spaces|$E_\infty$-spaces]] $E_0 \,\coloneqq\, \Omega^\infty(E)$, at least, realized as $\Omega^{\mathcal{J}}(E)$ in [SaSc11 (4.4)](#SagaveSchlichtkrull11), they are canonically equipped with an [[commutative monoid in a symmetric monoidal (infinity,1)-category|$E_\infty$-monoid]] [[homomorphism]] 

   $$
     (E_0, \cdot) 
       \xrightarrow{\;} 
    (\mathbb{S}_0, +)
   $$

   to the *additive* $E_\infty$-space underlying the [[sphere spectrum]] ([traditionally](Bousfield-Friedlander+model+structure#Spectrification) denoted $Q S^0 $, which is notation for a construction that yields $\Omega^\infty \Sigma^\infty S^0$).

   The $E_\infty$-monoid homomorphisms of this form are the evident homotopy-theoretic generalization of morphisms of [[commutative monoids]] to the additive group $(\mathbb{Z}, +)$ of the [[integers]], and these are evidently equivalent to $\mathbb{Z}$-[[graded monoid|gradings]] on the [[domain]] monoid.

   $\,$

   So [[E-∞ geometry]] in itself is already a [[categorification|categorified]]/homotopified version of [[supergeometry]], but of $\mathbb{Z}$-graded supergeometry, not of the proper $\mathbb{Z}/2$-graded supergeometry.

   $\,$

   (That grading over the [[sphere spectrum]] is closely related to [[superalgebra]] had been highlighted in [Kapranov 13](#Kapranov13), but the issue of the difference between homotopified $\mathbb{Z}$-grading compared to homotopified $\mathbb{Z}/2$-grading had been left open.)

   $\,$

1. {#SuperGeometryAsPeriodifiedZGradedGeometry} But ordinary $\mathbb{Z}/2$-graded [[supercommutative superalgebra]] is equivalently $\mathbb{Z}$-graded [[supercommutative superalgebra]] over the free even periodic $\mathbb{Z}$-graded supercommutative superalgebra ([this prop.](geometry+of+physics+--+superalgebra#ModulesOverRbeta)).

   $\,$

1. {#PassageToAlgebraOverPeriodicRingSpectra} In view of the [first point](#EInfinityGeometryAlreadyZGraded), the [second point](#SuperGeometryAsPeriodifiedZGradedGeometry) has an evident analog in [[E-∞ geometry]]: 

   The higher/derived analog of an even periodic $\mathbb{Z}$-graded commutative algebra is an [[E-infinity algebra]] over an [[even cohomology theory|even]] [[periodic ring spectrum]].

   $\,$

   That [[E-infinity algebras]] over [[even cohomology theory|even]] [[periodic ring spectra]] are usefully regarded from the point of view of [[supercommutative superalgebra]] was highlighted in [Rezk 09, section 2](#Rezk09).

Hence it makes sense to say:

**Definition.** _Spectral/$E_\infty$ super-geometry_ is simply the [[E-∞ geometry]] over [[even cohomology theory|even]] [[periodic ring spectra]].

## Examples

### Spectral superpoint
  {#SpectralSuperpoint}

The ordinary [[superpoint]] over some [[field]] $k$ is the [[spectrum of a commutative ring]] of the graded [[symmetric algebra]] on a single odd generator ("graded [[ring of dual numbers]]")

$$
  \mathbb{A}_k^{0 \vert 1}
  \;\simeq\;
  Spec( \,Sym_k (k[1])\, )
$$ 

Accordingly, for $R$ an [[even cohomology theory|even]] [[periodic ring spectrum]], then the _spectral superpoint_ $R^{0 \vert 1}$ should be the [[spectral scheme]] given by the [[spectral symmetric algebra]] on the [[suspension spectrum]] of $R$:

$$
  \begin{aligned}
    R^{0 \vert 1}
     &\coloneqq
    Spec
    \left(
      Sym_R (\Sigma R)
    \right)
    \\
    & \simeq
    Spec\left(
    R
    \wedge
    \left(
       \underset{n \in \mathbb{N}}{\coprod}
        B \Sigma(n)^{\tau_n}
    \right)_+
    \right)
    \\
    & \simeq
    Spec\left(
    R \wedge
    Sym_{\mathbb{S}}(\Sigma \mathbb{S})
    \right)
  \end{aligned}
  \,.
$$

where on the right we have the [[Thom space]] of the [[vector bundle]] $\tau_n$ [[associated bundle|associated]] to the $\Sigma(n)$-[[universal principal bundle]] via the canonical [[action]] of $\Sigma(n)$ on $\mathbb{R}^n$ (see also at [symmetric group -- Classifying space and Thom space](permutation#ClassifyingSpaceAndThomSpace)).



## References

The proposal for spectral super-geometry [above](#Definition) invokes observations from

* {#Rezk09} [[Charles Rezk]], section 2 of _The congruence criterion for power operations in Morava E-theory_, Homology, Homotopy and Applications, Vol. 11 (2009), No. 2, pp.327-379 ([arXiv:0902.2499](https://arxiv.org/abs/0902.2499))

* {#SagaveSchlichtkrull11} [[Steffen Sagave]], [[Christian Schlichtkrull]], _Diagram spaces and symmetric spectra_, Advances in Mathematics, Volume 231, Issues 3&#8211;4, October&#8211;November 2012, Pages 2116&#8211;2193 ([arXiv:1103.2764](https://arxiv.org/abs/1103.2764))

The proposal [above](#Definition) was originally motivated from the discussion of the [[sphere spectrum]] in relation to [[super algebra]] highlighted in

* {#Kapranov13} [[Mikhail Kapranov]], _Categorification of supersymmetry and stable homotopy groups of spheres_, talk at _[Algebra, Combinatorics and Representation Theory: in memory of Andrei Zelevinsky (1953-2013)](http://mathserver.neu.edu/~bwebster/ACRT/)_ April 2013 ([abstract pdf](http://mathserver.neu.edu/~bwebster/ACRT/calendar-with-abstracts.pdf),  [video](https://youtu.be/StbRti1fV7A))

* {#Kapranov15} [[Mikhail Kapranov]], _Supergeometry in mathematics and physics_, in [[Gabriel Catren]], [[Mathieu Anel]], (eds.) _[[New Spaces for Mathematics and Physics]]_ ([arXiv:1512.07042](http://arxiv.org/abs/1512.07042))

* {#Kapranov15b} [[Mikhail Kapranov]], _Super-geometry_, talk at _[New Spaces for Mathematics & Physics](http://ercpqg-espace.sciencesconf.org/program)_, IHP Paris, Oct-Sept 2015 ([video recording](https://www.youtube.com/watch?v=bjsNwKYT8JE))

A closely related suggestion later appears in:

* MathOverflow comment  [MO:a/40327](https://mathoverflow.net/a/403274/381), Sep 2021



[[!redirects spectral super-schemes]]

[[!redirects spectral supergeometry]]
[[!redirects E-∞ supergeometry]]
[[!redirects E-infinity supergeometry]]

[[!redirects spectral super scheme]]
[[!redirects spectral super schemes]]

[[!redirects spectral superpoint]]
[[!redirects spectral superpoints]]
[[!redirects spectral super point]]
[[!redirects spectral super points]]
[[!redirects spectral super-point]]
[[!redirects spectral super-points]]

[[!redirects spectral superscheme]]
[[!redirects spectral superschemes]]
