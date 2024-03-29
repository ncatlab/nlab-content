
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The __spectral theorems__ form a cornerstone of [[functional analysis]]. They are a vast generalization to infinite-dimensional [[Hilbert spaces]] of a basic result in linear algebra: an $n \times n$ Hermitian matrix can be diagonalized or conjugated to a diagonal matrix with real entries along the diagonal. 

There is a caveat, though: if we consider a separable Hilbert space $\mathcal{H}$ then we can choose a countable orthonormal (Hilbert) basis $\{e_n\}$ of $\mathcal{H}$, a linear operator $A$ then has a matrix representation in this basis just as in finite dimensional linear algebra. The spectral theorem does _not_ say that for every selfadjoint $A$ there is a basis so that $A$ has a diagonal matrix with respect to it. The situation that comes closest to the analogy of finite dimensions is the spectral theorem for compact operators. 

There are several versions of the spectral theorem, or several spectral theorems, differing in the kind of operator considered (bounded or unbounded, selfadjoint or normal) and the phrasing of the statement (via spectral measures, multiplication operator norm), which is why this page does not consist of _one_ statement only. Plus there are several different strategies to prove e.g. the spectral theorem for bounded selfadjoint operators, so there is no _canonical_ way to prove it (none is particularly simple). 

## Versions of the theorem 

### Memory hook

This is a short description of a way to prove the spectral theorem for bounded, selfadjoint operators in the spectral measure form, it may serve as a memory hook:

Let $\mathcal{H}$ be a Hilbert space and A be an selfadjoint operator on $\mathcal{H}$. Then we can form the smallest [[von Neumann algebra]] $\mathcal{R}$ generated by both A and $\mathbb{1}$, the identity operator. This is an abelian algebra, that is, via the [[Gelfand representation]], the abelian version of the [[Gelfand-Naimark theorem]], isometric isomorph to the algebra of continuous complex valued functions of a compact Hausdorff space. The spectral integral of A now becomes the Lebesgue (or Riemann) integral of a continuous function. 

### Selfadjoint operators

* theorem: there is a one to one correspondence of (bounded or unbounded) selfadjoint operators $A$ and [[spectral measure]]s E such that 
$$
      A = \integral \lambda E(d\lambda)
$$
A is bounded iff E is bounded.

### Borel functional calculus

As stated on the [[spectral measure]] page, given a resolution of the identity $E$ one can make sense of $E(u)$ for any function $u$ that is Borel measurable. Since we have for a selfadjoint operator $A = E(u)$ for $u(\lambda) = \lambda$, one can define a bounded operator $u(A)$ for every _bounded_ Borel measurable function $u$.


### Compact operators

The special case of compact operators is mentioned here because it comes closest to the finite dimensional situation of diagonalizing Hermitian matrixes.

* theorem: let $A$ be a compact selfadjoint operator, then the spectrum of $A$ consists of eigenvalues only, and all eigenvalues $\neq 0$ have finite multiplicity. Therefore, the spectral theorem says in this case, that
$$ 
         A = \sum \lambda_k |x\rangle \langle x|
$$
where $\lambda_k$ is an eigenvalue (each eigenvalue appears n times if n is its multiplicity) and $x$ an eigenvector with eigenvalue $\lambda_k$. 

The converse statement is of course true, too, given a sequence $(\lambda_n)$ in $\mathbb{C}$ convergent to $0$, the sum above (with arbitrary $x \in \mathcal{H}, \|x\| = 1$) defines a normal compact operator, and a selfadjoint compact operator iff all $\lambda_n$ are real. 
It is possible to generalize the statement to compact operators on (not necessarily complete) normed spaces.

### Normal operators

(...) [[normal operator]] (...)

## Proofs

### ...

### By Lagrange multipliers

For the case of symmetric real matrices there is a
simple proof using [[Lagrange multiplier]] techniques.

See [Lagrange multiplier -- Applications -- To Spectral theory](http://ncatlab.org/nlab/show/Lagrange+multiplier#ApplicationToSpectralTheory).

## Related entries

* For [[unitary matrices]] the spectal theorem is equivalently [Cartan's theorem](maximal+torus#Properties) that every element in $U(n)$ is conjugate to an element in its [[maximal torus]]. 

[[!redirects spectral theorems]]