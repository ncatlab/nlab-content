
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--


\tableofcontents


## Idea

Over [[ground rings]] which are not [[commutative ring|commutative]], the notion of *[[determinants]]* does not provide useful invariants of [[matrices]] (in fact, various classical formulas for determinants mutually disagree in this case). 

The notion of *quasideterminants* is meant to fix this: 
these are [[noncommutative rational functions]] of the given matrix entries rather than [[polynomials]].

Given an $n \times n$ matrix, its quasideterminants may be thought of as generalized ratios of an $n\times n$-determinant by an $(n-1)\times (n-1)$ [[minor]]. Since there are $n^2$ such [[minors]] -- one complementary to each entry -- there are $n^2$ quasideterminants. 

Ordinary [[determinants]], but also [[superdeterminants]], [[quantum determinants]] and [[Dieudonné determinants]] can be expressed as products of quasideterminants.


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
  \big( {|A|}_{ji}\big)^{-1} = (A^{-1})^i_j.
$$

Quasideterminants for a matrix with entries in a commutative ring $R$ are, up to a sign,
ratios of the determinant of the matrix and the determinant
of the appropriate $(n-1)\times (n-1)$ submatrix, as one can see by remembering the formula for matrix inverse in terms of the cofactor matrices. For systems of linear equations with coefficients (from one side) in a noncommutative ring, there are solution formulas involving quasideterminants and generalizing Cramer's rule (hence left and right Cramer's rule). Quasideterminants with generic entries (entries in a free skewfield) satisfy generalizations of many classical identities: Muir's law of extensionality, Silvester's law, etc., and a new "heredity" principle and so-called "homological identities". Furthermore, for polynomial equations over noncommutative rings, noncommutative Viete's formulas have been found and used in applications.


## References

The original articles:

* [[Israel M. Gel'fand]], [[Vladimir S. Retakh]]: _Determinants of matrices over noncommutative rings_, Funct. Anal. Appl. __25__ 2 (1991) 91--102 &lbrack;[doi:10.1007/BF01079588](https://doi.org/10.1007/BF01079588)&rbrack;

* [[Israel M. Gel'fand]], [[Vladimir S. Retakh]]: *A theory of noncommutative determinants and characteristic functions of graphs*, Funct. Anal. Appl. __26__ 4 (1992) 231--246 &lbrack;[doi:10.1007/BF01075044](https://doi.org/10.1007/BF01075044)&rbrack;

* [[Israel M. Gel'fand]], [[Vladimir S. Retakh]]: _Quasideterminants I_, Selecta Mathematica, N. S. **3** 4 (1997) 517--546 &lbrack;[doi:10.1007/s000290050019](https://doi.org/10.1007/s000290050019)&rbrack;

Review:

* [[Israel M. Gelfand]], [[Sergei Gelfand]], [[Vladimir S. Retakh]], [[Robert Lee Wilson]]: _Quasideterminants_, Advances in Mathematics **193** (2005) 56--141 &lbrack;[doi:10.1016/j.aim.2004.03.018](https://doi.org/10.1016/j.aim.2004.03.018)&rbrack;

* [[Vladimir S. Retakh]], [[Robert Lee Wilson]]: _Advanced course on quasideterminants and universal localization_, CRM Barcelona, (2007) &lbrack;[[RetakhWilson-Quasideterminants.pdf:file]]&rbrack;

See also: 

* Wikipedia: *[Quasideterminant](https://en.wikipedia.org/wiki/Quasideterminant)*

Further discussion:

* [[Israel Gelfand]], [[Daniel Krob]], Alain Lascoux, [[Bernard Leclerc]], [[Vladimir S. Retakh]], J.-Y. Thibon: _Noncommutative symmetric functions_, Adv. in Math. __112__ 2 (1995) 218--348 &lbrack;[arXiv:hep-th/9407124](https://arxiv.org/abs/hep-th/9407124), [doi:10.1006/aima.1995.1032](https://doi.org/10.1006/aima.1995.1032)&rbrack;

* [[Daniel Krob]], [[Bernard Leclerc]]: _Minor identities for quasi-determinants and quantum determinants_, Comm. Math. Phys. **169** (1995) 1-23 &lbrack;[doi:10.1007/BF02101594](https://doi.org/10.1007/BF02101594), [arXiv:hep-th/9411194](https://arxiv.org/pdf/hep-th/9411194)&rbrack;

* [[Zoran Škoda]]: *Quasideterminants and Cohn localization*, Chapter 16 in: _Noncommutative localization in noncommutative geometry_, London Math. Society Lecture Note Series **330** (2006) 220--310 &lbrack;[arXiv:math.QA/0403276](http://arxiv.org/abs/math/0403276), [doi:10.1017/CBO9780511526381.015](https://doi.org/10.1017/CBO9780511526381.015)&rbrack;


category: algebra

[[!redirects quasideterminants]]
[[!redirects quasi-determinant]]
[[!redirects quasi-determinants]]
