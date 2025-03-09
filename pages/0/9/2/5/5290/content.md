

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Gerstenhaber algebra_ is a [[Poisson n-algebra|Poisson 2-algebra]], hence a graded [[Poisson algebra]] (i.e. [[internalization|internal to]] [[graded vector spaces]]) with [[Poisson bracket]] of degree -1 (cf. [Cattaneo, Fiorenza & Longoni 2006, Def. 1.1](#CattaneoFiorenzaLongoni06)).

Since the signs in the [[Jacobi identity]] depend only on the degree of the bracket [[modulo]] 2, some authors speak more generally of Gerstenhaber algebras in the case of graded Poisson algebras with bracket of any odd degree (e.g. [Kontsevich 1999, Thm. 3](#Kontsevich99)).




## Definition

+-- {: .num_defn}
###### Definition


A **Gerstenhaber algebra** is a [[chain complex]] $A$ equipped with

1. a graded symmetric product $(-)\cdot(-) \colon A \otimes A \to A$,

1. a graded skew-symmetric bracket $[-,-] \;\colon\; A \otimes A \to A[1]$,

such that 

* $(-) \cdot (-)$ is [[associativity|associative]] 

* $[-,-]$ satisfies the [[Jacobi identity]] 

* $[a,-]$ is a [[derivation]] of $(-)\cdot(-)$ for all $a \in A$.

=--

## Properties

+-- {: .num_theorem}
###### Theorem

The [[homology]] of the  [[operad]] for Gerstenhaber algebras in [[chain complexes]] is the operad for Gerstenhaber algebras.

Accordingly the [[homology]] of an [[E2-algebra]] is a Gerstenhaber algebra.

=--

This is due to [Cohen (1976)](#Cohen).

+-- {: .num_remark}
###### Remark

A Gerstenhaber algebra equipped in addition with a certain morphism $\Delta : A \to A$ is a **[[BV-algebra]]**. This is the homology of an algebra over the [[framed little 2-disk operad]].

=--

## Related concepts

* [[Poisson n-algebra]]

* [[BV-algebra]]

## References

* {#Cohen} [[Fred Cohen]], *The homology of $C_{n+1}$-Spaces, $n\geq0$*, In: The Homology of Iterated Loop Spaces. Lecture Notes in Mathematics, vol. **533**. Springer, Berlin, Heidelberg. (1976) &lbrack;[doi:10.1007/BFb0080467](https://doi.org/10.1007/BFb0080467)&rbrack;
 
* [[Murray Gerstenhaber]], *The cohomology structure of an associative ring*, Ann. of Math. **78** (1963) 267-288 &lbrack;[doi:10.2307/1970343](https://doi.org/10.2307/1970343), [jstor:1970343](https://www.jstor.org/stable/1970343) [MR28:5102](http://www.ams.org/mathscinet-getitem?mr=28:5102)&rbrack;

* [[Ping Xu]], *Gerstenhaber algebras and BV-algebras in Poisson geometry*, Commun. Math. Phys. **200** 3 (1999) 545-560 &lbrack;[arXiv:dg-ga/9703001](https://arxiv.org/abs/dg-ga/9703001), [doi:10.1007/s002200050540](https://doi.org/10.1007/s002200050540)&rbrack;

* {#Kontsevich99} [[Maxim Kontsevich]], *Operads and Motives in Deformation Quantization*, Lett. Math. Phys. **48** (1999) 35-72 &lbrack;[arXiv:math/9904055](https://arxiv.org/abs/math/9904055), [doi:10.1023/A:1007555725247](https://doi.org/10.1023/A:1007555725247)&rbrack;


* {#CattaneoFiorenzaLongoni06} [[Alberto S. Cattaneo]], [[Domenico Fiorenza]], Riccardo Longoni, *Graded Poisson Algebras*, in: *Encyclopedia of Mathematical Physics*, Elsevier (2006) 560-567 &lbrack;[arXiv:1811.07395](https://arxiv.org/abs/1811.07395), [doi:10.1016/B0-12-512666-2/00434-X](https://doi.org/10.1016/B0-12-512666-2/00434-X)&rbrack;


[[!redirects Gerstenhaber algebras]]

[[!redirects Poisson 2-algebra]]
[[!redirects Poisson 2-algebras]]

[[!redirects Gerstenhaber bracket]]
[[!redirects Gerstenhaber brackets]]

