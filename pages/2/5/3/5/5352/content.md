
> This entry is about the concept in [[differential geometry]]. For the concept of [[Jacobian variety]] see there.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

If $f : \mathbb{R}^n \to \mathbb{R}^m$ is a $C^1$-[[differentiable map]], between [[Cartesian space]]s, its **Jacobian matrix** is the $(m \times n)$ [[matrix]]

$$
  J(f) \in Mat_{m \times n}(C^0(\mathbb{R}, \mathbb{R}))
$$

of [[partial derivative]]s

$$
  J(f)^i_j := \frac{\partial f^i}{\partial x^j},\,\,\,\,\,\,\,i=1,\ldots,m; j = 1,\ldots,n,
$$
where $x = (x^1,\ldots,x^n)$. Here the convention is that the upper index is a row index and the lower index is the column index; in particular $\mathbf{R}^n$ is the space of real column vectors of length $n$.

In more general situation, if $f = (f^1(x),\ldots,f^m(x))$ is differentiable at a point $x$ (and possibly defined only in a [[neighborhood]] of $x$), we define the Jacobian $J_p f$ of map $f$ at point $x$ as a matrix with real values $(J_p f)^i_j = \frac{\partial f^i}{\partial x^j}|_x$. 

That is, the Jacobian is the matrix which describes the [[total derivative]]. 

If $n=m$ the Jacobian matrix is a square matrix, hence its [[determinant]] $det(J(f))$ is defined and called __the Jacobian of $f$__ (possibly only at a point). Sometimes one refers to Jacobian matrix rather ambigously by Jacobian as well. 


## Properties

The [[chain rule]] may be phrased by saying that the Jacobian matrix of the composition $\mathbf{R}^n\stackrel{f}\to\mathbf{R}^m\stackrel{g}\to\mathbf{R}^r$ is the [[matrix product]] of the Jacobian matrices of $g$ and of $f$ (at appropriate points).  


If $g:M\to N$ is a $C^1$-map of $C^1$-manifolds, then the [[tangent bundle|tangent map]] $T g: T M\to T N$ defined point by point abstractly by $(T_p g)(X_p)(f) = X_p(f\circ g)$, for $p\in M$, can in local [[coordinates]] be represented by a Jacobian matrix. Namely, if $(U,\phi)\ni p$ and $(V,\psi)\ni g(p)$ are [[charts]] and $X_p = \sum X^i\frac{\partial}{\partial x^i}|_p$ (i.e. $X_p(f)  = \sum_i X^i_p \frac{\partial (f\circ \phi^{-1})}{\partial x^i}|_{\phi(p)}$ for all germs $f\in \mathcal{F}_p$), then 
$$
(T_p g)(X_p) = \sum_{i,j} J_p(\psi \circ g\circ\phi^{-1})_i^j X^i_p \frac{\partial}{\partial y^j}|_{g(p)}
$$ 

## Related concepts

* [[differentiation]], [[Hessian matrix]], [[extremum]]

* [[pullback of a distribution]]

[[!redirects Jacobians]]

[[!redirects Jacobian matrix]]
[[!redirects Jacobian determinant]]

[[!redirects Jacobian matrices]]
[[!redirects Jacobian determinants]]
