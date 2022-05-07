
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

## Definition

Given a [[square matrix]] $J$ (representing a [[bilinear form]]) over a [[commutative ring]] $k$, a _$J$-orthogonal matrix_ is any square matrix $A$ of the same size over $k$ such that

$$
  A^T J A = J
$$

where $A^T$ is the [[transpose matrix]] of $A$. 

Most often one considers a case when $J$ is diagonal. For $J = 1$ one recovers the notion of an [[orthogonal matrix]].

All J-orthogonal matrices over the [[ground field]] $k$ form an [[algebraic group]] denoted $SO_J(n, k)$ or $SO(n,k; J)$ or alike; in real or complex case a Lie group. The matrices in the Lie algebra are J-skew-symmetric, $A^T J + J A = 0$.

## Related concepts

* [[orthogonal matrix]]

## References

* [[M M Postnikov]], _Lectures on geometry, Semester V, Lie groups and Lie algebras_

* Nicholas J. Higham, _J-orthogonal matrices: properties and generation_, 
[doi](https://doi.org/10.1137/S0036144502414930)