
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

An _orthogonal matrix_ is a [[square matrix]] $A$ whose [[transpose matrix]]  equals its [[inverse matrix]] $A^T = A^{-1}$, hence such that $A^T A = 1$ under [[matrix multiplication]].
 
Orthogonal matrices form a [[subgroup]] of the [[general linear group]], namely the [[orthogonal group]].

For a generalization see _[[J-orthogonal matrix]]_. 

## Properties

Every real matrix $A$ can be factorized $A = Q R$ where $Q$ is orthogonal and $R$ is   a (say, upper) triangular matrix (wikipedia/[QR decomposition](https://en.wikipedia.org/wiki/QR_decomposition) which is a special case of [[Iwasawa decomposition]] for semisimple Lie groups). This is consequence of Gram-Schmidt orthogonalization. Similarly, every complex matrix can be factorized into a unitary and a complex upper triangular (complex) matrix.

Over the reals, the [[Cayley transform]] is a [[diffeomorphism]] between the linear space skewsymmetric matrices and an open subset of the Lie group of orthogonal matrices ($A$ such that $I+A$ is invertible) - a chart which is often having an advantage over using the exponential map. 

## Related concepts

* [[J-orthogonal matrix]]

* [[orthogonal group]], [[Gram-Schmidt orthogonalization]]


### References


* wikipedia/[orthogonal matrix](https://en.wikipedia.org/wiki/Orthogonal_matrix)

[[!redirects orthogonal matrices]]
