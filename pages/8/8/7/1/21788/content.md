
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

In generalization of [[twisted ad-equivariant K-theory]] there is [[twisted ad-equivariant Tate K-theory]] (an [[equivariant elliptic cohomology]] theory) relating to the [[Verlinde ring]] of [[positive energy representation|positive energy]] [[loop group representations]] 
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

* {#Ganter13} [[Nora Ganter]], _Power operations in orbifold Tate K-theory_, Homology Homotopy Appl. Volume 15, Number 1 (2013), 313-342. ([arXiv:1301.2754](https://arxiv.org/abs/1301.2754), [euclid:hha/1383943680](https://projecteuclid.org/euclid.hha/1383943680))

On [[twisted ad-equivariant Tate K-theory]]:


For simply-connected [[compact Lie groups]]:

* {#Luecke19}  Kiran Luecke, _Completed K-theory and Equivariant Elliptic Cohomology_ ([arXiv:1904.00085](https://arxiv.org/abs/1904.00085))


For [[finite groups]]:

* {#Dove19} Thomas Dove, _Twisted Equivariant Tate K-Theory_ ([arXiv:1912.02374](https://arxiv.org/abs/1912.02374))

[[!redirects twisted ad-equivariant Tate K-theory]]






