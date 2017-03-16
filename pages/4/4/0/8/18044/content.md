
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

One way to define this is as follows:


Observe that 

1. [[E-∞ geometry]] is _already in itself_ a [[higher geometry|higher geometric]] version of $\mathbb{Z}$-graded supergeometry (in the sense discussed at _[[geometry of physics -- superalgebra]]_). 

   At the level of [[homotopy groups]] this is the following fact:

   For $E$ a [[homotopy commutative ring spectrum]], then its [[stable homotopy groups]] $\pi_\bullet(E)$ inherits the structure of a $\mathbb{Z}$-graded super-commutative ring  (according to [this](geometry+of+physics+--+superalgebra#SupercommutativeSuperalgebraZGraded)). See at _[[Introduction to Stable homotopy theory]]_ in the section [1-2 Homotopy commutative ring spectra](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyRingSpectra) [this proposition](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum).

   But more is true: the $E_\infty$-analog of the [[integers]] $\mathbb{Z}$ is the [[sphere spectrum]] $\mathbb{S}$, and every [[E-infinity ring]] $E$ is canonically $\mathbb{S}$-graded ([Sagave-Schlichtkrull 11, theorem 1.7-18](#SagaveSchlichtkrull11)). 

   So [[E-∞ geometry]] in itself is already a [[categorification|categorified]]/homotopified version of [[supergeometry]], but of $\mathbb{Z}$-graded supergeometry, not of the proper $\mathbb{Z}/2$-graded supergeometry.

1. But ordinary $\mathbb{Z}/2$-graded [[supercommutative superalgebra]] is equivalently $\mathbb{Z}$-graded supercommutative superalgebra over the free even periodic $\mathbb{Z}$-graded supercommutative superalgebra ([this prop.](geometry+of+physics+--+superalgebra#ModulesOverRbeta)).


Here, in view of the first point, the second point has an evident analog in [[E-∞ geometry]]: The higher/derived analog of an even periodic $\mathbb{Z}$-graded commutative algebra is an [[E-infinity algebra]] over an [[even cohomology theory|even]] [[periodic ring spectrum]].

That [[E-infinity algebras]] over [[even cohomology theory|even]] [[periodic ring spectra]] are usefully regarded from the point of view of [[supercommutative superalgebra]] was highlighted in [Rezk 09, section 2](#Rezk09).

Hence it makes sense to define spectral/$E_\infty$ super-geometry simply to be [[E-∞ geometry]] over [[even cohomology theory|even]] [[periodic ring spectra]].

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
    R
    \wedge
    \left(
       \underset{n \in \mathbb{N}}{\coprod}
        B \Sigma(n)^{\mathbb{R}^n}
    \right)_+
    \\
    & \simeq
    R \wedge
    Sym_{\mathbb{S}}(\Sigma \mathbb{S})
  \end{aligned}
  \,.
$$




## References



* {#Rezk09} [[Charles Rezk]], section 2 of _The congruence criterion for power operations in Morava E-theory_, Homology, Homotopy and Applications, Vol. 11 (2009), No. 2, pp.327-379 ([arXiv:0902.2499](https://arxiv.org/abs/0902.2499))

* {#SagaveSchlichtkrull11} [[Steffen Sagave]], [[Christian Schlichtkrull]], _Diagram spaces and symmetric spectra_, Advances in Mathematics, Volume 231, Issues 3&#8211;4, October&#8211;November 2012, Pages 2116&#8211;2193 ([arXiv:1103.2764](https://arxiv.org/abs/1103.2764))



[[!redirects spectral super-schemes]]

[[!redirects spectral supergeometry]]
[[!redirects E-∞ supergeometry]]
[[!redirects E-infinity supergeometry]]

[[!redirects spectral super scheme]]
[[!redirects spectral super schemes]]
