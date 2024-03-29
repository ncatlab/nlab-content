Let $M$ be a smooth manifold and $f: M\to \mathbb{R}$ a real valued function.

$p\in M$ is a **critical point** of $f$ if for any curve $\gamma : (-\epsilon, \epsilon)\to M$ with $\gamma(0)=p$, the vector

$$
\frac{d(f\circ\gamma)}{dt} |_{t=0} = 0.
$$

The critical point is **regular** if for one (or equivalently any) chart $\phi : U^{\open}\to \mathbb{R}^n$, where $p\in U$ and $\phi(p) = 0\in \mathbb{R}^n$, the Hessian matrix

$$\left(\frac{\partial^2 (f\circ \phi^{-1})}{\partial x^i\partial x^j}|_{0}\right)_{ij} $$

is a nondegenerate (i.e. maximal rank) matrix.  

The **Morse lemma** states that for any regular critical point $p$ of $f$ there is a chart $\phi: U\to \mathbb{R}^n$ around $p$ such that the function in these coordinates is quadratic:

$$(f\circ\phi^{-1})(x^1,\ldots,x^n) = f(p) +\sum_{i=1}^k x_i^2 - \sum_{j=k+1}^n x_j^2$$

and the number $k$ is determined by the Hessian matrix. While the Morse lemma is proved by Morse, the modern proof is by Moser's deformation method.  The Morse lemma can be generalized to smooth functions on a Hilbert manifold, in which case there is a linear operator $A$ such that in suitable local coordinates, the quadratic functional $f\circ\phi^{-1}$ can be written as $f(p)+$&lt;$A x,x$>.

* V. Guillemin, S. Sternberg, _Geometric asymptotics_, [Appendix 1](http://www.ams.org/online_bks/surv14/surv14-appI.pdf)