
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What is called _Gaussian elimination_ is an [[algorithm]] for solving systems of [[linear equations]]. It proceeds by encoding the system as a [[matrix]] equation
$$
 A \, x = b
$$
where $b$ is a column matrix of free coefficients, $x$ is a column vector of unknowns, and $A$ is the matrix of coefficients. The entire system is therefore encoded by the matrix of the system which is in block form $(A | b)$. The algorithm consists of applying [[elementary row operations]] in a systematic way to bring it into [[upper triangular form]].

## Variants


### Over noncommutative rings

Coeffients may be in a noncommutative ring and we may search for a solution in that ring. However, all the coefficients are from the same, say left side of the unknowns. The algorithm is proceeding as in the commutative case, provided certain 
expressions are invertible along the way. 
Recursive nature of the algorithm is related to the 
hereditary property of [[quasideterminant]]s.

## Gauss decomposition

Performing the Gauss elimination procedure when $A$ is a square matrix to end with upper triangular matrix $U$ means that $A$ is written in the form
$$
A = w L U
$$
where $w$ is a permutation matrix, $L$ a lower triangular matrix with units of diagonal and $U$ an upper triangular
matrix. This is the [[Gauss decomposition]] with respect to the lower Borel subgroup of $GL(n,k)$. A noncommutative Gauss decomposition exists for matrices over noncommutative [[division ring]]s.

## Related concepts

* [[Gram-Schmidt process]]
* [[Gauss decomposition]]

## References

* Wikipedia, _[Gaussian elimination](https://en.wikipedia.org/wiki/Gaussian_elimination)_

An application of Gauss elimination to a particular system yields the [[Gram-Schmidt orthogonalization]]:

* Lyle Pursell, S. Y. Trimble, _Gram-Schmidt orthogonalization by Gauss elimination_, The American Mathematical Monthly  __98__:6 (1991) 544--549 [doi](https://doi.org/10.1080/00029890.1991.11995755)

[[!redirects Gaussian eliminations]]

[[!redirects Gauss elimination]]
[[!redirects Gauss eliminations]]

[[!redirects row reduction]]
[[!redirects row reductions]]

[[!redirects elementary row operation]]
[[!redirects elementary row operations]]

[[!redirects elementary column operation]]
[[!redirects elementary column operations]]

[[!redirects Gauss elimination procedure]]
[[!redirects Gauss elimination procedures]]

