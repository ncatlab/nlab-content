The Gram-Schmidt process is an algorithm which takes as input an ordered [[basis]] of an [[inner product space]] and produces as output an ordered [[orthonormal basis]]. 

"Gram-Schmidt" is also used to refer to a factorization of a invertible matrix $M \in GL_n(\mathbb{R})$ ($M \in GL_n(\mathbb{C})$) as a product $M = U T$ where $T$ is an upper triangular matrix and $U$ is an orthonormal (unitary) matrix $U$, as such it is a special case of the more general [[Iwasawa decomposition]] for a (connected) semisimple Lie group. It may also refer to the reduction of the structure group of an inner product bundle (e.g., the tangent bundle of a Riemannian manifold) from $GL_n$ to $O_n$. 

## Gram-Schmidt process on Hilbert spaces 

In this section, "basis" is understood to signify an ordered independent set whose span is dense in a [[Hilbert space]] $H$ seen as a [[metric space]]. We will describe the Gram-Schmidt process as applied to a countable basis $v_1, v_2, \ldots$ of an infinite-dimensional separable Hilbert space, although it would apply just as well to a well-ordered basis of any Hilbert space, separable or not. 

The orthonormal basis $u_1, u_2, \ldots$ produced as output is defined recursively as follows. We denote the normalization $v/\|v\|$ of a vector $v \in H$ by $N(v)$. Put 

$$u_n = N(v_n - \sum_{k \lt n} \langle v_n, u_k\rangle u_k)$$ 

where the sum on the right is understood to be empty (equal to 0) in the case $n = 1$. A simple inductive argument shows that the $u_i$ are unit vectors orthogonal to each other, and that the span of $u_1, \ldots, u_n$ is equal to the span of $v_1, \ldots, v_n$. Therefore $u_1, u_2, \ldots$ is an orthonormal basis of $H$. 

## Example of Legendre polynomials 

A classic illustration of Gram-Schmidt is the production of the Legendre polynomials. 

Let $H$ be the Hilbert space $H = L^2([-1, 1])$, equipped with the standard inner product defined by 

$$\langle f, g\rangle = \int_{-1}^1 \bar{f(x)} g(x) d x$$ 

By the [[Stone-Weierstrass theorem]], the space of polynomials $\mathbb{C}[x]$ is dense in $H$ according to its standard inclusion, and so the polynomials $1, x, x^2, \ldots$ form an ordered basis of $H$. 

Applying the Gram-Schmidt process, one readily computes the first few orthonormal functions: 

$$u_1(x) = N(1) = 1/2$$ 

$$u_2(x) = N(x - 0) = \sqrt{3/2} x$$ 

$$u_3(x) = N(x^2 - \langle x^2, 1/2\rangle 1/2 - 0) = N(x^2 - 1/3) = 3\sqrt{5/2}/2(x^2 - 1/3)$$ 

The classical Legendre polynomials $P_n(x)$ are scalar multiplies of the functions $u_n$, adjusted so that $P_n(1) = 1$; they satisfy the orthogonality relations 

$$\langle P_n, P_m\rangle = \frac{2}{2n + 1}\delta_{m, n}$$ 

where $\delta_{m, n}$ is the Kronecker delta. 
