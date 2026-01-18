
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

The [[equivariant cohomology|equivariant]] version of Tate K-theory is a form of [[equivariant elliptic cohomology]]. For $G$ a [[finite group]] and $X$ a [[topological G-space]] it comes down ([Ganter 07, Def. 3.1](#Ganter07), [Ganter 13, Def. 2.6](#Ganter13), review in [Dove 19, Def. 6.16](#Dove19)) to the sub-ring

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

**{#RotationCondition}Rotation condition**. _The $C_g$-[[equivariant vector bundles]] $V_j$ which form the coefficient of $q^{j/\left\vert g \right\vert }$ are such that $g$ acts on them by multiplication with $\exp\big( 2 \pi i \frac{j}{\left\vert g \right\vert}  \big)$_.

{#RotationConditionImpliedByHuanInertiaEquivariance} This rotation condition may be understood more intrinsically 
(this is made explicit on [p. 63](https://arxiv.org/pdf/1912.02374.pdf#page=69) of [Dove 19](#Dove19))
as that in implied by the [[orbifold K-theory]] on [[Huan's inertia orbifold]] ([Huan 18](#Huan18)), induced by the nature of the quotient groups
$$
  \Lambda_g \;\coloneqq\; \frac{C_g \times \mathbb{R}}{ \langle (g^{-1},1) \rangle }
$$
appearing [there](Huan's+inertia+orbifold#HuanCentralizer). This quotient exactly equates the action of $g \in G$ with that of a rotation of $S^1$.

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

* {#AHS01}  [[Matthew Ando]], [[Michael Hopkins]], [[Neil Strickland]], Section 2.7 of: _Elliptic spectra, the Witten genus and the theorem of the cube_, Invent. math. 146, 595–687 (2001) &lbrack;[doi:10.1007/s002220100175](https://doi.org/10.1007/s002220100175)&rbrack;


* {#Lurie09} [[Jacob Lurie]], _[[A Survey of Elliptic Cohomology]]_, in: _Algebraic Topology_ Abel Symposia **4** (2009) 219-277 &lbrack;[pdf](http://www.math.harvard.edu/~lurie/papers/survey.pdf), [doi:10.1007/978-3-642-01200-6_9](https://doi.org/10.1007/978-3-642-01200-6_9)&rbrack;

As completed $S^1$-[[equivariant K-theory]] of [[free loop space]]

* {#KM04}  [[Nitu Kitchloo]], [[Jack Morava]], Section 5 of: _Thom Prospectra for Loopgroup representations_ &lbrack;[arXiv:math/0404541](https://arxiv.org/abs/math/0404541)&rbrack;


As a form of [[equivariant elliptic cohomology]] ([[twisted ad-equivariant Tate K-theory]]):


* {#Ganter07} [[Nora Ganter]], Section 3.1 in: _Stringy power operations in Tate K-theory_ &lbrack;[arXiv:math/0701565](https://arxiv.org/abs/math/0701565)&rbrack;

* {#Ganter13} [[Nora Ganter]]: *Power operations in orbifold Tate K-theory*,  Homology Homotopy Appl. **15** 1 (2013) 313-342  &lbrack;[arXiv:1301.2754](https://arxiv.org/abs/1301.2754), [euclid:hha/1383943680](https://projecteuclid.org/journals/homology-homotopy-and-applications/volume-15/issue-1/Power-operations-in-orbifold-Tate-K-theory/hha/1383943680.full)&rbrack;
  > (cf. *[[orbifold K-theory]]*)

* {#Rezk14} [[Charles Rezk]], *Quasi-Elliptic Cohomology* (2014) &lbrack;[[Rezk-QuasiEllipticCohomology.pdf:file]]&rbrack;


* [[Zhen Huan]], _Quasi-elliptic cohomology_ (2017) &lbrack;[hdl:2142/97268](http://hdl.handle.net/2142/97268)&rbrack;

* [[Zhen Huan]], *Quasi-Elliptic Cohomology and its Power Operations*, J. Homotopy and Related Structures **13** (2018) 715–767 &lbrack;[arXiv:1612.00930](https://arxiv.org/abs/1612.00930), [doi:10.1007/s40062-018-0201-y](https://doi.org/10.1007/s40062-018-0201-y)&rbrack;

* [[Zhen Huan]], *Quasi-elliptic cohomology and its Spectrum* &lbrack;[arXiv:1703.06562](https://arxiv.org/abs/1703.06562)&rbrack;

* {#Huan18} [[Zhen Huan]], _Quasi-Elliptic Cohomology I_, Advances in Mathematics, **337** (2018) 107-138 &lbrack;[arXiv:1805.06305](https://arxiv.org/abs/1805.06305), [doi:10.1016/j.aim.2018.08.007](https://doi.org/10.1016/j.aim.2018.08.007)&rbrack;

with a streamlined account in 

* [[Zhen Huan]], *Quasi-theories* &lbrack;[arXiv:1809.06651](https://arxiv.org/abs/1809.06651)&rbrack;

* [[Zhen Huan]], *Quasi-theories and their equivariant orthogonal spectra* &lbrack;[arXiv:1809.07622](https://arxiv.org/abs/1809.07622)&rbrack;

and some general abstract clarification on [[Huan's inertia orbifold]] in:

* [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Cyclification of Orbifolds]]*, Comm. Math. Phys. (2023) &lbrack;[arXiv:2212.13836](https://arxiv.org/abs/2212.13836), [[schreiber:cyclic loop spaces 2022|talk]]&rbrack;

Review:

* [[Zhen Huan]], *Quasi-elliptic cohomology theory and the twisted, twisted Real theories*, talk at Perimeter Institute (2020) &lbrack;video: [doi:10.48660/20050059](https://doi.org/10.48660/20050059)&rbrack;

For [[simply-connected topological space|simply-connected]] [[compact Lie groups]]:

* {#Luecke19}  [[Kiran Luecke]], *Completed K-theory and Equivariant Elliptic Cohomology*, Advances in Mathematics **410** B (2022) 108754 &lbrack;[arXiv:1904.00085](https://arxiv.org/abs/1904.00085), [doi:10.1016/j.aim.2022.108754](https://doi.org/10.1016/j.aim.2022.108754)&rbrack;


For [[finite groups]]:

* {#Dove19} [[Thomas Dove]], _Twisted Equivariant Tate K-Theory_ &lbrack;[arXiv:1912.02374](https://arxiv.org/abs/1912.02374)&rbrack;

Generalization to [[twisted equivariant K-theory]] 

* [[Zhen Huan]], [[Matthew Spong]], *Twisted Quasi-elliptic cohomology and twisted equivariant elliptic cohomology* ([arXiv:2006.00554](https://arxiv.org/abs/2006.00554))

and further to [[KR-theory]]:

* [[Zhen Huan]], [[Matthew B. Young]], *Twisted Real quasi-elliptic cohomology* &lbrack;[arXiv:2210.07511](https://arxiv.org/abs/2210.07511)&rbrack;

  [[Zhen Huan]], *Twisted Real quasi-elliptic cohomology*, talk at [[CQTS]] (Nov 2022) &lbrack;[video](https://zoom.us/rec/play/_2MIenxSff2vBZeFPO8lV6g_lyLgrUEBDP5Au7tySNyeJpeLeXfZ96ZBkgKs7wNYAnBDauB4atzVJAt-.McANEtFgQHFACmbr?_x_zm_rhtaid=966&_x_zm_rtaid=F4VKJYOLRDu8ouQdfmDz3w.1668757869896.554b5189e89fa9af0846d97599b6bf49&autoplay=true&continueMode=true&iet=6_ddkV5u8UGa9M9U4dDvH2SN55OyZgmZiCrQZ6wbo4E.AG.Gp56JL6y5Z3naAtSVPOGAHkLGEPMDtxPB370GxyQz_EIJOEq1ylk0bXAowqSDnPSYr62xiX92tLdNLdbchq-w5Vhavx5UCPbjfaCIIObE183OI8.142oNpQmC8JiJOzcA4eIXw.O0nEkHAMvD5awvgi&startTime=1667999236000)&rbrack;

On quasi-elliptic cohomology of [[representation spheres]] as an approximation to [[equivariant Cohomotopy]]:

* [[Zhen Huan]]: *Twisted Quasi-elliptic cohomology and twisted equivariant elliptic cohomology*, Advances in Theoretical and Mathematical Physics **29** 7 (2025) 1857-1904 &lbrack;[arXiv:2006.00554](https://arxiv.org/abs/2006.00554), [doi:10.4310/ATMP.251120035411](https://doi.org/10.4310/ATMP.251120035411)&rbrack;

* [[Zhen Huan]]: *Quasi-elliptic cohomology of 4-spheres*,     Axioms **14** 4 (2025) 267 &lbrack;[arXiv:2408.02278](https://arxiv.org/abs/2408.02278), [doi:10.3390/axioms14040267](https://doi.org/10.3390/axioms14040267)&rbrack;



[[!redirects twisted ad-equivariant Tate K-theory]]

[[!redirects quasi-elliptic cohomology]]





