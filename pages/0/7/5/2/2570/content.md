The Gram--Schmidt process is an algorithm which takes as input an ordered [[basis]] of an [[inner product space]] and produces as output an ordered [[orthonormal basis]]. 

In terms of [[matrix|matrices]], the Gram--Schmidt process is a procedure of factorization of a invertible matrix $M$ in the [[general linear group]] $GL_n(\mathbb{R})$ (or $GL_n(\mathbb{C})$) as a product $M = U T$ where $T$ is an upper triangular matrix and $U$ is an orthonormal (or unitary) matrix; as such it is a special case of the more general [[Iwasawa decomposition]] for a (connected) semisimple [[Lie group]]. Since the factorization depends smoothly on the parameters, the Gram--Schmidt procedure enables the reduction of the structure group of an inner product [[vector bundle|bundle]] (e.g., the [[tangent bundle]] of a [[Riemannian manifold]] or a [[Kähler manifold]]) from $GL_n$ to [[orthogonal group]] $O_n$ (or the [[unitary group]] $U_n$). 


## Gram--Schmidt process on Hilbert spaces 

In this section, "basis" is understood to signify an ordered independent set whose linear span is dense in a [[Hilbert space]] $H$ seen as a [[metric space]]. We will describe the Gram--Schmidt process as applied to a countable basis $v_1, v_2, \ldots$ of an infinite-dimensional separable Hilbert space, although it would apply just as well to a [[well-ordered set|well-ordered]] basis of any Hilbert space, separable or not. 

The orthonormal basis $u_1, u_2, \ldots$ produced as output is defined recursively as follows. We denote the normalization $v/\|v\|$ of a vector $v \in H$ by $N(v)$. Put 

$$u_n = N(v_n - \sum_{k \lt n} \langle v_n, u_k\rangle u_k)$$ 

where the sum on the right is understood to be empty (equal to $0$) in the case $n = 1$. A simple inductive argument shows that the $u_i$ are unit vectors orthogonal to each other, and that the span of $u_1, \ldots, u_n$ is equal to the span of $v_1, \ldots, v_n$. Therefore $u_1, u_2, \ldots$ is an orthonormal basis of $H$. 


## Example of Legendre polynomials 

A classic illustration of Gram--Schmidt is the production of the [[Legendre polynomials]]. 

Let $H$ be the Hilbert space $H = L^2([-1, 1])$, equipped with the standard inner product defined by 

$$\langle f, g\rangle = \int_{-1}^1 \bar{f(x)} g(x) d x$$ 

By the [[Stone-Weierstrass theorem]], the space of polynomials $\mathbb{C}[x]$ is dense in $H$ according to its standard inclusion, and so the polynomials $1, x, x^2, \ldots$ form an ordered basis of $H$. 

Applying the Gram--Schmidt process, one readily computes the first few orthonormal functions: 

$$u_1(x) = N(1) = 1/2$$ 

$$u_2(x) = N(x - 0) = \sqrt{3/2} x$$ 

$$u_3(x) = N(x^2 - \langle x^2, 1/2\rangle 1/2 - 0) = N(x^2 - 1/3) = 3\sqrt{5/2}/2(x^2 - 1/3)$$ 

The classical Legendre polynomials $P_n(x)$ are scalar multiplies of the functions $u_n$, adjusted so that $P_n(1) = 1$; they satisfy the orthogonality relations 

$$\langle P_n, P_m\rangle = \frac{2}{2n + 1}\delta_{m, n}$$ 

where $\delta_{m, n}$ is the [[Kronecker delta]]. 


## Application to non-bases

If we apply the Gram--Schmidt process to a well-ordered independent set whose closed linear span $S$ is *not* all of $H$, we still get an orthonormal basis of the subspace $S$.  If we apply the Gram--Schmidt process to a dependent set, then we will eventually run into a vector $v$ whose norm is zero, so we will not be able to take $N(v)$.  In that case, however, we can simply remove $v$ from the set and continue; then we will still get an orthonormal basis of the closed linear span.  (This conclusion is not generally valid in [[constructive mathematics]], since it relies on [[excluded middle]] applied to the statement that $\|v\| \neq 0$.  However, it does work to [[discrete fields]], such as the algebraic closure of the rationals, as seen in elementary undergraduate linear algebra.)


[[!redirects Gram–Schmidt process]]
[[!redirects Gram--Schmidt process]]
[[!redirects Gram-Schmidt]]
[[!redirects Gram–Schmidt]]
[[!redirects Gram--Schmidt]]
[[!redirects Gram-Schmidt procedure]]
[[!redirects Gram–Schmidt procedure]]
[[!redirects Gram--Schmidt procedure]]
[[!redirects Gram-Schmidt factorization]]
[[!redirects Gram–Schmidt factorization]]
[[!redirects Gram--Schmidt factorization]]
[[!redirects Gram-Schmidt factorisation]]
[[!redirects Gram–Schmidt factorisation]]
[[!redirects Gram--Schmidt factorisation]]