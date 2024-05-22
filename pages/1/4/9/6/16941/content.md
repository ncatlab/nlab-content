
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}



## Idea

$n\times n$ matrices with entries in a unital ring $R$ form a unital ring $Mat_{n \times n}(R)$ with unit $I_n$ (diagonal matrix whose each entry at the main diagonal is $1_R$). A matrix $A\in Mat_{n \times n}(R)$ is invertible (also said regular) if it has a two-sided inverse $A^{-1}$ in that unital ring, called the matrix inverse (or inverse matrix) of $A$. In other words, it is a matrix satisfying $A A^{-1} = I_n = A^{-1} A$.

## Variants

#### One-sided inverses

Sometimes one-sided inverses in $Mat_{n \times n}(R)$ are also useful as well as one-sided inverses of rectangular matrices.

#### Schur complement

Sometimes, an inverse matrix does not exist but formulas for some entries of inverse matrix make sense. Related  expressions include [[quasideterminant]]s and [[Schur complement]], see there.

#### Moore--Penrose inverse

A generalized inverse $A^{-1}$ satisfying weaker requirement $A A^{-1} A = I_n$ and $A^{-1} = A^{-1} A A^{-1}$ is sometimes useful, especially in applied mathematics and approximation theory. These identities play role also in [[inverse semigroup]]s.

In the case of matrices, such generalized inverse is known as Moore--Penrose inverse.

## Properties

+-- {: .num_prop #FundamentalTheoremOfLinearAlgebra}
###### Proposition
**(fundamental theorem of invertible matrices)**

If $R = k$ is a field, $n \in \mathbb{N}$ and $A \in Mat_{n \times n}(k)$ a [[square matrix]], the following are equivalent:

1. $A$ is an invertible matrix;

1. $A$ is the [[matrix product]] of [[elementary matrices]].

=--

## Related concepts

* [[quasideterminant]]

* [[Gaussian elimination]]

* [[rank of a matrix]]

* [[matrix group]]

* [[general linear group]]

* [[matrix equivalence]]

## References

* Wikipedia, _[Invertible matrix](https://en.wikipedia.org/wiki/Invertible_matrix)_, _[Moore--Penrose inverse](https://en.wikipedia.org/wiki/Moore%E2%80%93Penrose_inverse)_

* WolframMathWorld, _[Invertible Matrix Theorem](http://mathworld.wolfram.com/InvertibleMatrixTheorem.html)_

Formulas for inverses of [[block matrices]] see shortly at [[Schur complement]] and more at 

* D. Krob, B. Leclerc, Sec 2 in: _Minor identities for quasi-determinants and quantum determinants_, Comm. Math. Phys. **169** (1995) 1-23 &lbrack;[doi:10.1007/BF02101594](https://doi.org/10.1007/BF02101594), [arXiv:hep-th/9411194](https://arxiv.org/pdf/hep-th/9411194)&rbrack;đ

* Chapter 13 (e.g. 13.8), Block LU factorization, in: Nicholas J. Higham, _Accuracy and stability of numerical algorithms_, Society for Industrial and Applied Mathematics, Year: 2002

* Tzon-Tzer Lu, Sheng-Hua Shiou, *Inverses of $2 \times 2$ block matrices*, Computers & Mathematics with Applications **43** 1–2 (2002) 119-129 &lbrack;<a href="https://doi.org/10.1016/S0898-1221(01)00278-4">doi:10.1016/S0898-1221(01)00278-4</a>&rbrack;

* {#SD23} Müge Saadetoğlu, Şakir Mehmet Dinsev, *Inverses and determinants of $n \times n$ block matrices*, Mathematics **11** 17 (2023) 3784 &lbrack;[doi:10.3390/math11173784](https://doi.org/10.3390/math11173784)&rbrack;


[[!redirects inverse matrices]]

[[!redirects invertible matrix]]
[[!redirects invertible matrices]]

[[!redirects matrix inverse]]

[[!redirects fundamental theorem of invertible matrices]]