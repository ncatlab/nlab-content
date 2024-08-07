
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A degree-$p$ _calibration_ of an oriented [[Riemannian manifold]] $(X,g)$ is a [[differential p-form]] $\omega \in \Omega^p(X)$ with the property that 

1. it is [[closed differential form|closed]] $d \omega = 0$;

1. evaluated on any oriented $p$-dimensional subspace of any [[tangent space]] of $X$, it is less than or equal to the induced degree-$p$ [[volume form]], with [[equality]] for at least one choice of subspace.

A Riemannian manifold equipped with such a calibration is also called a _calibrated geometry_ ([Harvey-Lawson 82](#HarveyLawson82)) or similar.

A _calibrated submanifold_ of a manifold with calibration is an oriented [[submanifold]] such that restricted to each of its tangent spaces $\omega$ _equals_ the induced volume form of the submanifold there.

## Properties

### Minimal volume submanifolds

Any calibrated submanifold $\Sigma \hookrightarrow X$ minimizes [[volume]] in its [[homology]] class.

For Let $\tilde \Sigma \hookrightarrow X$ be a homologous [[submanifold]]. Then [[Stokes theorem]] together with the condition that $d \phi = 0$ implies that the [[integration of differential forms]] of $\phi$ over $\Sigma$ equals that over $\tilde \Sigma$. The defining conditions on calibrations and on calibrated submanifolds then imply the [[inequality]]

$$
  vol(\Sigma)
  \stackrel{cal\,subm}{=}
  \int_\Sigma \phi
  \stackrel{Stokes}{=} 
  \int_{\tilde \Sigma} \phi
  \stackrel{calib}{\leq}
  \int_{\tilde \Sigma} d vol
  =
  vol(\tilde \Sigma)
  \,.
$$

### Calibrations from spinors
 {#CalibrationsFromSpinors}

> under construction

For suitable $n$ and $p$, and given a real [[spin representation]] of $Spin(n)$, 
then the [[Cartesian space]] $\mathbb{R}^n$ with its canonical Riemannian structure
becomes $p$-calibrated with the calibration form being 

$$
  \omega_{\epsilon}
  \coloneqq 
  (\overline{\epsilon} \Gamma_{a_1 a_2 \cdots a_p} \epsilon) \, e^{a_1} \wedge \cdots \wedge e^{a_p}
$$

where 

1. $\{e^a\}$ denotes the canonical [[linear basis]] of [[differential 1-forms]];

1. $\epsilon$ is a non-vanishing [[spinor]];

1. $\overline{\epsilon} \Gamma_{a_1 a_2 \cdots a_p} \epsilon$ is the [canonical bilinear pairing](spin+representation#SpinorBilinearForms) which in components is given by evaluating $\epsilon$ in the [[quadratic form]] given by multiplying the skew-symmetrized product of $p$ of the representation matrices $\Gamma^a$ of the [[Clifford algebra]] with the [[charge conjugation matrix]] $C$.

(e.g. [Dadok-Harvey 93](#DadokHarvey93)).

For instance for $n = 7$ and $p = 3$ then this gives the [[associative 3-form]] calibration.

More generally for $X$ an $n$-dimensional [[Riemannian manifold]] with a [[covariantly constant spinor]] $\epsilon$, then under suitable conditions applying this construction in each [[tangent space]] gives a calibration.

## Examples

* The globalization of the [[associative 3-form]] of a [[G₂-manifold]] is a calibration. A calibrated submanifold in this case is also called an [[associative submanifold]].

* The [[Cayley 4-form]] on [[Spin(7)-manifolds]].

## References

### General

The original articles are


* {#HarveyLawson82} [[Reese Harvey]], [[H. Blaine Lawson]], _Calibrated geometries_, Acta Mathematica July 1982, Volume 148, Issue 1, pp 47-157

* [[Reese Harvey]], _Calibrated geometries_, Proceeding of the ICM 1983 ([pdf](http://www.mathunion.org/ICM/ICM1983.1/Main/icm1983.1.0797.0808.ocr.pdf))

The relation to [[Killing spinors]] goes back to

* [[Reese Harvey]], _Spinors and Calibrations_, Academic Press, 1990 ([publisher](http://www.elsevier.com/books/spinors-and-calibrations/harvey/978-0-12-329650-4))

* {#DadokHarvey93} [[Jiri Dadok]], [[Reese Harvey]], _Calibrations and spinors_, Acta Mathematica 1993, Volume 170, Issue 1, pp 83-120

See also


* Wikipedia, _[Calibrated geometry](https://en.wikipedia.org/wiki/Calibrated_geometry)_

* Jason Dean Lotay, _Calibrated submanifolds and the Exceptional geometries_, 2005 ([pdf](https://people.maths.ox.ac.uk/joyce/theses/LotayDPhil.pdf))

### Application in string theory

Discussion in [[string theory]]/[[M-theory]] includes the following.


* [[Gary Gibbons]], [[George Papadopoulos]], _Calibrations and Intersecting Branes_ ([arXiv:hep-th/9803163](http://arxiv.org/abs/hep-th/9803163))

* [[Jerome Gauntlett]], [[Neil Lambert]], [[Peter West]], _Branes and Calibrated Geometries_, Commun.Math.Phys. 202 (1999) 571-592 ([arXiv:hep-th/9803216](http://arxiv.org/abs/hep-th/9803216))

* [[George Papadopoulos]], [[Jan Gutowski]], _AdS Calibrations_, Phys.Lett.B462:81-88,1999 ([arXiv:hep-th/9902034](http://arxiv.org/abs/hep-th/9902034))

* [[Jan Gutowski]], [[George Papadopoulos]], [[Paul Townsend]], _Supersymmetry and generalized calibrations_, Phys.Rev.D60:106006, 1999 ([arXiv:hep-th/9905156](http://arxiv.org/abs/hep-th/9905156))

* [[Jan Gutowski]], S. Ivanov, [[George Papadopoulos]], _Deformations of generalized calibrations and compact non-Kahler manifolds with vanishing first Chern class_, Asian Journal of Mathematics 7 (2003), 39-80 ([arXiv:0205012](http://arxiv.org/abs/math/0205012))

[[!redirects calibrations]]

[[!redirects calibrated geometry]]
[[!redirects calibrated geometries]]

[[!redirects calibrated manifold]]
[[!redirects calibrated manifolds]]

[[!redirects calibrated submanifold]]
[[!redirects calibrated submanifolds]]

[[!redirects manifold with calibration]]
[[!redirects manifolds with calibration]]
[[!redirects manifold with calibrations]]
[[!redirects manifolds with calibrations]]