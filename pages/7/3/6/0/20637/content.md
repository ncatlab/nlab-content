
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Dwyer-Wilkerson space_ $G_3$ ([Dwyer-Wilkerson 93](#DwyerWilkerson93)) is a [[p-adic completion|2-complete]] [[H-space]], in fact a finite [[loop space]]/[[infinity-group]], such that the mod 2 [[cohomology ring]] of its [[classifying space]]/[[delooping]] is the mod 2 [[Dickson invariants]] of rank 4. As such, it is the fourth and last space (see [below](#Cohomology)) in a series of [[infinity-groups]] that starts with 3 [[compact Lie groups]], namely with [automorphism groups of real normed division algebras](normed+division+algebra#Automorphisms):

| $n=$ | 1 | 2 | 3 | 4 | 
|--|--|--|--|--|
| $DI(n)=$ | [[Z/2]] | [[SO(3)]] | [[G2]] | [[G3]] |
|          | [= Aut(C)](complex+number#AutomorphismsOfComplexNumbersIsZ2)        | [= Aut(H)](quaternion#AutomorphismsOfQUatrnionsAlgebraIsSO3)       |  [= Aut(O)](octonion#AutomorphismsOfOctonionAlgebraIsG2)  |   |

whence the notation $G_3$ (suggested by [[Jack Morava]]).


## Properties

### Cohomology
 {#Cohomology}

The [[ordinary cohomology]] of the [[classifying space]]/[[delooping]] $B G_3$ with [[coefficients]] in the [[prime field]] $\mathbb{F}_2$ is, as an [[associative algebra]] over the [[Steenrod algebra]], the ring of mod 2 [[Dickson invariants]] of rank 4.

([Dwyer-Wilkerson 93, Theorem 1.1](#DwyerWilkerson93))

As such $G_3$ is the last in a series of [[infinity-groups]] whose [[classifying spaces]]/[[deloopings]] have as mod 2 [[cohomology ring]] the mod 2 [[Dickson invariants]] for rank $n$, which starts with three ordinary [[compact Lie groups]]:

| $n=$ | 1 | 2 | 3 | 4 | 
|--|--|--|--|--|
| $DI(n)=$ | [[Z/2]] | [[SO(3)]] | [[G2]] | [[G3]] |

([Dwyer-Wilkerson 93, top of p. 38 (2 of 28)](#DwyerWilkerson93))




This means in particular that the cohomology is an [[exterior algebra]] on generators of degree 7, 11, 13, 14 so it's (2-locally) a [[Poincare duality space]] of dimension 45.

(...)




### Weyl group

The analog of the [[Weyl group]] for $G_3$ is $\mathbb{Z}/2 \times GL(3,\mathbb{F}_2)$.

([Dwyer-Wilkerson 93, middle of p. 38 (2 of 28)](#DwyerWilkerson93))


### Homotopy coset space $G_3/Spin(7)$

$G_3$ receives a homomorphism from [[Spin(7)]]. The [[homotopy fiber]] of the corresponding [[delooping]] map is a homotopy-[[coset space]] 

$$
  G_3/Spin(7)
$$

The [[ordinary cohomology]] with [[coefficients]] in the [[prime field]] $\mathbb{F}_2$ of this space

1. is concentrated in even degrees,

1. has [[Euler characteristic]] 24.

([Dwyer-Wilkerson 93, Theorem 1.8](#DwyerWilkerson93))

## Related concepts

[[!include coset space structure on n-spheres -- table]]

## References

Due to 

*  {#DwyerWilkerson93} [[William Dwyer]], [[Clarence Wilkerson]], _A new finite loop space at the prime two_, J. Amer. Math. Soc. 6 (1993), 37-64  ([doi:10.1090/S0894-0347-1993-1161306-9](https://doi.org/10.1090/S0894-0347-1993-1161306-9))

See also

* Martin Bendersky, Donald M. Davis, _$v_1$-periodic homotopy groups of the Dwyer-Wilkerson space_ ([arXiv:0706.0993](https://arxiv.org/abs/0706.0993))

* [[Andrew Baker]], [[Tilman Bauer]], _The realizability of some finite-length modules over the Steenrod algebra by spaces_ ([arXiv:1903.10288](https://arxiv.org/abs/1903.10288))


[[!redirects Dwyer-Wilkerson H-sapces]]

[[!redirects Dwyer-Wilkerson space]]
[[!redirects Dwyer-Wilkerson spaces]]

[[!redirects G3]]



