
#Contents#
* table of contents
{:toc}

## Idea following Loomis-Sternberg

$X$ -- finite dimensional real vector space

$U\subset X$ open 

$F: U\to \mathbf{R}$ differentiable function

$S\subset U$ a smooth submanifold, which can be represented as a zero set of a differentiable map $G: U\to Y$, whre $Y$ is a real vector space and such that $d G_x$ is surjective for each $x\in S$. 

We want to minimize $F(x)$ for $x\in S$. It won't work to set $d F_x = 0$ and solving for $x$ as $x$ will not be a critical point of $F$ in general. The Lagrange multipliers are used to define another function $L$ such that solving $d L_x = 0$ gives extrema of the constrained extremization problem. 

__Theorem__ (Loomis-Sternberg 3.12.2) Suppose $F$ has a maximum on $S$ at $x$. Then there is a function(al) $l$ in $Y^*$ such that $x$ is a critical point of the function $F - l\circ G$.

The proof uses implicit function theorem and the usual extremization arguments. 

To get to a more familiar form of Lagrange multipliers, one uses the local coordinates $(x_1,\ldots,x_n)$ on $U$ and sets $Y = \mathbf{R}^m$, so that $G = (g^1,\ldots, g^n)$. Now $l: Y\to\mathbf{R}$ will be of the form $l(y_1,\ldots,y_m) = \sum_{i = 1}^m \lambda_i y_i$ and $F - l\circ G = F - \sum_{i = 1}^m \lambda_i g^i$ and $d (F - l\circ G) = 0$ gives 

$$
\frac{\partial F}{\partial x_j} - \sum_{i = 1}^m\lambda_i\frac{\partial g^i}{\partial x_j} = 0,\,\,\,\,\,\,\,\,j = 1,\ldots, n.
$$

This is $n$ equations, which together with $m$ equations $G = (g^1,\ldots, g^n) = 0$ for $S$ give $m+n$ equations for $m+n$ unknowns $x_1,\ldots, x_n, \lambda_1,\ldots,\lambda_m$. The last $m$ variables here are the Lagrange multipliers. 

## Applications 

### To spectral theory 
 {#ApplicationToSpectralTheory}

The method of Lagrange multipliers affords an elementary proof of the [[spectral theorem]] for finite-dimensional real [[vector spaces]], one which does not involve passage to the [[complex numbers]] and the [[fundamental theorem of algebra]]. 

+-- {: .un_prop}
######Proposition 
Let $A$ be a real symmetric $n \times n$ matrix. Then $A$ is diagonalizable over the real numbers. 
=-- 

+-- {: .proof} 
######Proof 
Consider the problem of maximizing the function $f(x) = \langle x \vert A \vert x \rangle$ where $x \in \mathbb{R}^n$ is subject to the constraint $\langle x \vert x \rangle = 1$. (Such an extreme point exists, say by compactness.) By the symmetry of $A$, the [[gradient]] of $f$ is easily calculated to be $\nabla f (x) = 2 A x$, whereas the gradient of the [[Euclidean norm]] $\langle x \vert x \rangle$ is $2 x$. At a point $x$ where a maximum is attained, we have $\nabla f(x) = 2 A x = \lambda (2 x)$ for some Lagrange multiplier $\lambda$. Thus $x$ is an eigenvector of $A$ with eigenvalue $\lambda$. The usual arguments show that $A$ restricts to a [[self-adjoint operator]] on the hyperplane orthogonal to $x$; by picking an orthonormal basis of this hyperplane, we may represent this restriction of $A$ by a real symmetric matrix of size $(n-1) \times (n-1)$, and the argument repeats. 

=-- 

## Related concepts

* [[auxiliary field]]

* [[gauge fixing]]

## References

Named after [[Joseph-Louis Lagrange]].

* wikipedia [Lagrange multiplier](http://en.wikipedia.org/wiki/Lagrange_multiplier)

* Springer eom: [Lagrange multipliers](http://eom.springer.de/L/l057190.htm), [Pontrjagin maximum principle](http://eom.springer.de/p/p073780.htm)

* Lynn H. Loomis, [[S. Sternberg]], _Advanced calculus_, section 3.12 

"Submanifolds and Lagrange multipliers" [[LoomisSternberg13s2.djvu:file]]

* Robert Hermann, _Some differential-geometric aspects of the Lagrange variational problem_, Illinois J. Math. __6__, 1962, 634&#8211;673, [MR145457](http://www.ams.org/mathscinet-getitem?mr=145457),[euclid](http://projecteuclid.org/euclid.ijm/1255632711)
* Juan Carlos Marrero, David Mart&#237;n de Diego, Ari Stern, _Lagrangian submanifolds and discrete constrained mechanics_, slides, [pdf](http://ccom.ucsd.edu/~astern/pdfs/dspde20100601.pdf)
* Manuel de Le&#243;n, David Mart&#237;n Diego, _Solving non-holonomic Lagrangian dynamics in terms of almost product structures_, Extracta Math. 11 (1996), no. 2, 325&#8211;347, [pdf](http://digital.csic.es/bitstream/10261/2232/1/solving.pdf) [MR97m:58079](http://www.ams.org/mathscinet-getitem?mr=1437457)

[[!redirects Lagrange multipliers]]