
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Tate K-theory is the [[elliptic cohomology theory]] associated with the [[Tate curve]] (the Tate [[elliptic curve]] over the [[Laurent series]] ring $\mathbb{Z}((q))$ )  ([AHS 01, 2.7](#AHS01), [Lurie 09, 4.3](#Lurie09))

The corresponding [[elliptic genus]] is the [[Witten genus]] ([AHS 01, Sec. 2.7](#AHS01)).

### Plain version

The underlying [[generalized (Eilenberg-Steenrod) cohomology|cohomology theory]] is given by [[Laurent series]] in [[topological K-theory]], and equivalently by completion of [[circle group]]-[[equivariant K-theory]] of [[free loop spaces]] $\mathcal{L}(-)$ ([KM 04, Section 5](#KM04), see also [Lurie 09, Section 5.2](#Lurie09)):

$$
  \begin{aligned}
  Ell_{Tate}(X)
  &
  \simeq
  \;
  K(X)((q))
  \\
  &
  \simeq
  \;
  K_{S^1}(\mathcal{L}X)
  \otimes_{K_{S^1}(\ast)}
  \mathbb{Z}((q))
  \,.
  \end{aligned}
$$

(For more exposition see also [Dove 19, Sec. 6.2](#Dove19)).

### Equivariant version
 {#IdeaEquivariantVersion}

The [[equivariant cohomology|equivariant]] version of Tate K-theory is a form of [[equivariant elliptic cohomology]]. For $G$ a [[finite group]] and $X$ a [[topological G-space]] it comes down ([Ganter 07, Def. 3.1](#Ganter07), [Ganter 13, Def. 2.6](#Ganter13), [Dove 19, Def. 6.16](#Dove19)) to the sub-ring

$$
  Ell_{Tate}
  \big(
    \prec (X \sslash G)
  \big)
  \;\subset\;
  \underset{[g]}{\bigoplus}
  K_{C_g}(X^g)(( q^{1/\left\vert g\right\vert} ))
$$

of the [[direct sum]], over [[conjugacy classes]] of group elements $g$, of [[Laurent polynomials]] with [[coefficients]] in [[equivariant K-theory]]-groups on the $g$-[[fixed loci]] for equivariance group the [[centralizer]] of $g$ 

on those elements which satisfy the _rotation condition_:

**Rotation condition**. _The $C_g$-[[equivariant vector bundles]] $V_j$ which form the coefficient of $q^{j/\left\vert g \right\vert }$ are such that $g$ acts on them by multiplication with $\exp\big( 2 \pi i \frac{j}{\left\vert g \right\vert}  \big)$_

Hence, in generalization of [[twisted ad-equivariant K-theory]] there is [[twisted ad-equivariant Tate K-theory]] (an [[equivariant elliptic cohomology]] theory) relating to the [[Verlinde ring]] of [[positive energy representation|positive energy]] [[loop group representations]] 
([Lurie 09, Sec. 5.2](#Lurie09), 
[Luecke 19, Cor. 3.2.5](#Luecke19), [Dove 19](#Dove19)).

## Properties

### Relation to elliptic genus

The [[Ochanine genus]] lifts to a homomorphism of [[ring spectra]] $M Spin \to KO((q))$ from [[spin structure]] [[cobordism cohomology theory]] to [[Tate K-theory]] ([Kreck-Stolz 93, lemma 5.8, lemma 5.4](spin-orientation+of+elliptic+cohomology#KreckStolz93)). This is the _[[spin-orientation of elliptic cohomology]]_

## Related concepts

* [[elliptic genus]]

  * [[Ochanine genus]]

  * [[Witten genus]]

* [[elliptic Chern character]]

* [[topological K-theory]]

* [[twisted ad-equivariant K-theory]]



## References

As [[elliptic cohomology]] over the [[Tate sphere]]:

* {#AHS01}  [[Matthew Ando]], [[Michael Hopkins]], [[Neil Strickland]], Section 2.7 of: _Elliptic spectra, the Witten genus and the theorem of the cube_, Invent. math. 146, 595–687 (2001) ([doi:10.1007/s002220100175](https://doi.org/10.1007/s002220100175))


* {#Lurie09} [[Jacob Lurie]], _[[A Survey of Elliptic Cohomology]]_, in: _Algebraic Topology_ Abel Symposia Volume 4, 2009, pp 219-277 ([pdf](http://www.math.harvard.edu/~lurie/papers/survey.pdf), [doi:10.1007/978-3-642-01200-6_9](https://doi.org/10.1007/978-3-642-01200-6_9))

As completed $S^1$-[[equivariant K-theory]] of [[free loop space]]

* {#KM04}  [[Nitu Kitchloo]], [[Jack Morava]], Section 5 of: _Thom Prospectra for Loopgroup representations_ ([arXiv:math/0404541](https://arxiv.org/abs/math/0404541))


As a form of [[equivariant elliptic cohomology]] ([[twisted ad-equivariant Tate K-theory]]):


* {#Ganter07} [[Nora Ganter]], Section 3.1 in: _Stringy power operations in Tate K-theory_ ([arXiv:math/0701565](https://arxiv.org/abs/math/0701565))

* {#Ganter13} [[Nora Ganter]], _Power operations in orbifold Tate K-theory_, Homology Homotopy Appl. Volume 15, Number 1 (2013), 313-342. ([arXiv:1301.2754](https://arxiv.org/abs/1301.2754), [euclid:hha/1383943680](https://projecteuclid.org/euclid.hha/1383943680))

* [[Zhen Huan]], _Quasi-elliptic cohomology_, 2017 ([hdl](http://hdl.handle.net/2142/97268))

* [[Zhen Huan]], *Quasi-elliptic cohomology and its Spectrum* ([arXiv:1703.06562](https://arxiv.org/abs/1703.06562))


* {#Huan18} [[Zhen Huan]], _Quasi-Elliptic Cohomology I_, Advances in Mathematics, Volume 337, 15 October 2018, Pages 107-138 ([arXiv:1805.06305](https://arxiv.org/abs/1805.06305), [doi:10.1016/j.aim.2018.08.007](https://doi.org/10.1016/j.aim.2018.08.007))

For simply-connected [[compact Lie groups]]:

* {#Luecke19}  Kiran Luecke, _Completed K-theory and Equivariant Elliptic Cohomology_ ([arXiv:1904.00085](https://arxiv.org/abs/1904.00085))


For [[finite groups]]:

* {#Dove19} Thomas Dove, _Twisted Equivariant Tate K-Theory_ ([arXiv:1912.02374](https://arxiv.org/abs/1912.02374))

[[!redirects twisted ad-equivariant Tate K-theory]]






