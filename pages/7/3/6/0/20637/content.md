
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

The _Dwyer-Wilkerson space_ $G_3$ ([Dwyer-Wilkerson 93](#DwyerWilkerson93)) is a [[p-adic completion|2-complete]] [[H-space]], in fact a finite [[loop space]]/[[∞-group]], such that the mod 2 [[cohomology ring]] of its [[classifying space]]/[[delooping]] is the mod 2 [[Dickson invariants]] of rank 4. As such, it is the fifth and last space (see [below](#Cohomology)) in a series of [[∞-groups]] that starts with 4 [[compact Lie groups]], namely with the [automorphism groups of real normed division algebras](normed+division+algebra#Automorphisms):

| $n=$ | 0 | 1 | 2 | 3 | 4 | 
|--|--|--|--|--|--|
| $DI(n)=$ | [[trivial group|1]] |  [[Z/2]] | [[SO(3)]] | [[G2]] | [[G3]] |
|          | = Aut(R) | [= Aut(C)](complex+number#AutomorphismsOfComplexNumbersIsZ2)        | [= Aut(H)](quaternion#AutomorphismsOfQUatrnionsAlgebraIsSO3)       |  [= Aut(O)](octonion#AutomorphismsOfOctonionAlgebraIsG2)  |   |

whence the notation $G_3$ (suggested in [Møller 95, p. 5](#Moller95)).

While $G_3$ is not a [[compact Lie group]], it is a [[p-compact group|2-compact group]], hence a "[[homotopy Lie group]]" (see [below](#AsA2CompactGroup)).



## Properties

### Cohomology
 {#Cohomology}

The [[ordinary cohomology]] of the [[classifying space]]/[[delooping]] $B G_3$ with [[coefficients]] in the [[prime field]] $\mathbb{F}_2$ is, as an [[associative algebra]] over the [[Steenrod algebra]], the ring of mod 2 [[Dickson invariants]] of rank 4. This is the ring of invariants of the natural action of $GL(4, \mathbf{F}_2)$ on the rank 4 polynomial algebra $H^{\ast}((B \mathbf{Z}/2)^4, \mathbf{F}_2)$, a polynomial algebra on classes $c_8$, $c_12$, $c_14$, and $c_15$ with $Sq^4 c_8 = c_{12}$, $Sq^2 c_{12} = c_{14}$, and $Sq^1 c_{14} = c_{15}$.

([Dwyer-Wilkerson 93, Theorem 1.1](#DwyerWilkerson93))



As such, $G_3$ is the last in a series of [[∞-groups]] whose [[classifying spaces]]/[[deloopings]] have as mod 2 [[cohomology ring]] the mod 2 [[Dickson invariants]] for rank $n$, which starts with three ordinary [[compact Lie groups]]:

| $n=$ | 1 | 2 | 3 | 4 | 
|--|--|--|--|--|
| $DI(n)=$ | [[Z/2]] | [[SO(3)]] | [[G2]] | [[G3]] |

([Dwyer-Wilkerson 93, top of p. 38 (2 of 28)](#DwyerWilkerson93))




This means in particular that the cohomology is an [[exterior algebra]] on generators of degree 7, 11, 13, 14 so it's (2-locally) a [[Poincare duality space]] of dimension 45.

(...)

### Construction as a homotopy colimit

The space $B G_3$ is the 2-completion of the homotopy colimit of a diagram ([Notbohm 03, Sec. 2](#Notbohm), [Ziemianski, 0.2.3](#Ziemianski)).


### As a 2-compact group
 {#AsA2CompactGroup}

$G_3$ is the only exotic 2-group, or, in other words, the only simple 
[[p-compact group|2-compact group]] not arising as the 2-completion of a compact connected Lie group ([Andersen-Grodal 06](#AndersenGrodal06)).


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

### Relation to the Conway group, $Co_3$

$B G_3$ receives a map from $B Co_3$, the [[delooping]] of the [[Conway group]], $Co_3$. This map has the property that it injects the mod two cohomology of $B G_3$ as a subring over which the mod two cohomology of $B Co_3$ is finitely generated as a module (see [Benson 94](#Benson94)). This continues a pattern from $B A_5 \to B SO(3)$ and $B M_{12} \to B G_2$, where $M_{12}$ is a [[Mathieu group]].

## Related concepts

[[!include coset space structure on n-spheres -- table]]

## References

Due to 

*  {#DwyerWilkerson93} [[William Dwyer]], [[Clarence Wilkerson]], _A new finite loop space at the prime two_, J. Amer. Math. Soc. 6 (1993), 37-64  ([doi:10.1090/S0894-0347-1993-1161306-9](https://doi.org/10.1090/S0894-0347-1993-1161306-9))

Review:

* {#Moller95} [[Jesper Møller]], _Homotopy Lie groups_, Bull. Amer. Math. Soc. (N.S.) 32 (1995) 413-428 ([arXiv:math/9510218](https://arxiv.org/abs/math/9510218))

* {#Grodal10} [[Jesper Grodal]], _The Classification of $p$–Compact Groups and Homotopical Group Theory_, Proceedings of the International Congress of Mathematicians, Hyderabad 2010 ([arXiv:1003.4010](https://arxiv.org/abs/1003.4010), [pdf](http://web.math.ku.dk/~jg/papers/icm.pdf), [[GrodalpCompactGroups2010.pdf:file]])

* {#Notbohm} Dietrich Notbohm, _On the compact 2-group $D I(4)$_,  Journal für die reine und angewandte Mathematik (Crelles Journal), Volume 2003, Issue 555, Pages 163–185, ([pdf](https://pdfs.semanticscholar.org/76ee/dfae66955e452fc20e7ab4a19bd1f6284af4.pdf))



See also

* {#BenderskyDavis07} Martin Bendersky, Donald M. Davis, _$v_1$-periodic homotopy groups of the Dwyer-Wilkerson space_ ([arXiv:0706.0993](https://arxiv.org/abs/0706.0993))

* [[Andrew Baker]], [[Tilman Bauer]], _The realizability of some finite-length modules over the Steenrod algebra by spaces_ ([arXiv:1903.10288](https://arxiv.org/abs/1903.10288))

* {#AndersenGrodal06} Kasper Andersen, [[Jesper Grodal]], _The classification of 2-compact groups_, J. Amer. Math. Soc. 22 (2009), 387-436 ([arXiv:math/0611437](https://arxiv.org/abs/math/0611437))

* {#Ziemianski} Krzysztof Ziemia&nacute;ski, _A faithful complex representation of the 2-compact group DI(4)_, ([thesis](https://www.mimuw.edu.pl/~ziemians/pap/Thesis.pdf))

* {#Benson94} David Benson, _Conway’s group $Co_3$ and the Dickson invariants_, Manuscripta Math (1994) 85: 177.

Speculation on possible geometric roles of $G_3$:

* {#Wilson09} [[Robert Wilson]], Slide 94 of: _A new approach to the Leech lattice_, talk at University of Cambridge, 21st October 2009 ([slides pdf](http://www.maths.qmul.ac.uk/~raw/talks_files/Cambridge09.pdf))

  (on an [[octonions|octonionic]] construction of the [[Leech lattice]])


[[!redirects Dwyer-Wilkerson H-spaces]]

[[!redirects Dwyer-Wilkerson space]]
[[!redirects Dwyer-Wilkerson spaces]]

[[!redirects G3]]



