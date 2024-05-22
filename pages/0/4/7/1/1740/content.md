
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Over non-[[commutative ring|commutative]] [[rings]] [[determinants]] are not useful invariants of [[matrix|matrices]] (in fact, various classical formulas for determinants mutually disagree in this case) and other [[polynomial]] suggestions were not of much success (in some cases the [[superdeterminant]] and [[Dieudonné determinant]] are of use, but they can be easily expressed in terms of quasideterminants anyway). Quasideterminants will be [[noncommutative rational function]]s, rather than polynomial, expressions. 

A quasideterminant generalizes a ratio of $n\times n$-determinant and a $(n-1)\times(n-1)$ minor. Regarding that there are $n^2$ such minors -- complementary to each entry-- there are $n^2$ quasideterminants, indexed by labels of the complementary entry. Special cases when useful polynomial determinants are defined like the usual determinant, superdeterminant, quantum determinant and Dieudonné determinant can be obtained as products of quasideterminants.

## Definition

Let $A = (a^i_j)\in M_n(R)$ be an $n\times n$ matrix
over an arbitrary noncommutative (but unital and associative) [[ring]] $R$. In fact it makes sense to work with many objects (see [[horizontal categorification]]): having, say, an [[abelian category]] where $a^i_j$ is a morphism from the object $i$ to the object $j$. 
Let us choose a row label $i$ and a column label $j$.
By $A^{\hat{i}}_{\hat{j}}$ we'll denote the $(n-1)\times(n-1)$ matrix obtained
from $A$ by removing the $i$-th row and the $j$-th column.
The $(i,j)$-th **quasideterminant** $|A|_{ij}$ is
\[ |A|_{ij} = a^i_j -
\sum_{k \neq i, l\neq j} a^i_l  (A^{\hat{i}}_{\hat{j}})^{-1}_{lk} a^k_j
\]
provided the right-hand side is defined (the corresponding inverses exist).


## Properties

Up to $n^2$ quasideterminants of a given $A \in M_n(R)$
may be defined. If all the $n^2$ quasideterminants $|A|_{ij}$ exist and are invertible then the [[inverse matrix]] $A^{-1}$ of $A$ exists in $M_n(R)$ and

$$
(|A|_{ji})^{-1} = (A^{-1})^i_j.
$$

Quasideterminants for a matrix with entries in a commutative ring $R$ are, up to a sign,
ratios of the determinant of the matrix and the determinant
of the appropriate $(n-1)\times (n-1)$ submatrix, as one can see by remembering the formula for matrix inverse in terms of the cofactor matrices. For systems of linear equations with coefficients (from one side) in a noncommutative ring, there are solution formulas involving quasideterminants and generalizing Cramer's rule (hence left and right Cramer's rule). Quasideterminants with generic entries (entries in a free skewfield) satisfy generalizations of many classical identities: Muir's law of extensionality, Silvester's law, etc., and a new "heredity" principle and so-called "homological identities". Furthermore, for polynomial equations over noncommutative rings, noncommutative Viete's formulas have been found and used in applications.

## References

Quasideterminants were introduced by I. Gel'fand and V. Retakh around 1990. 

* [[I. M. Gel'fand]], [[V. Retakh|V. S. Retakh]], _Determinants of matrices over noncommutative rings_, Funct.Anal.Appl. __25__ (1991), no.2, pp. 91--102.
engl. transl. __21__ (1991), pp. 51--58. 

* I.M. Gel'fand, V.S. Retakh, A theory of noncommutative determinants and characteristic functions of graphs, Funct.Anal.Appl. __26__ (1992), no.4, pp. 231--246.

* I.M. Gel'fand, V.S. Retakh, _Quasideterminants I_, Selecta Mathematica, N. S. 3 (1997) no.4, pp. 517--546; [doi](https://doi.org/10.1007/s000290050019)

* D.Krob, B.Leclerc, _Minor identities for quasi-determinants and quantum determinants_, Comm. Math. Phys. 169 (1995) 1--23 [doi](https://doi.org/10.1007/BF02101594)
arXiv:[hep-th/9411194](https://arxiv.org/pdf/hep-th/9411194)

* Chapter 16: Quasideterminants and Cohn localization in [[Z. Škoda]], _Noncommutative localization in noncommutative geometry_, London Math. Society Lecture Note Series 330, ed.  A. Ranicki; pp. 220--313, [arXiv:math.QA/0403276](http://arxiv.org/abs/math/0403276))

* [[V. Retakh]], R. Wilson, _Advanced course on quasideterminants and universal localization_ (2007) &lbrack;[[RetakhWilson-Quasideterminants.pdf:file]]&rbrack; 

category: algebra

[[!redirects quasideterminants]]