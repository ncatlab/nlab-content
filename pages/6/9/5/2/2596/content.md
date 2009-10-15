A smooth real valued function $f:M\to\mathbb{R}$ on a smooth [[manifold]] $M$ is called a **Morse function** if every critical point of $f$ is regular. 

$p\in M$ is a **critical point** of $f$ if for any curve $\gamma : (-\epsilon, \epsilon)\to M$ with $\gamma(0)=p$, the vector

$$
\frac{d(f\circ\gamma)}{dt} |_{t=0} = 0.
$$

The critical point is **regular** if for one (or equivalently any) chart $\phi : U^{\open}\to \mathbb{R}^n$, where $p\in U$ and $\phi(p) = 0\in \mathbb{R}^n$, the **Hessian matrix**

$$\left(\frac{\partial^2 (f\circ \phi^{-1})}{\partial x^i\partial x^j}(0)\right)_{i,j=1,\ldots, n} $$

is a nondegenerate (i.e. maximal rank) matrix. 

A choice of a Morse function on a compact manifold is often used to study topology of the manifold. This is called the Morse theory.  

Founders of Morse theory were M. Morse, R. Bott and A. Schwarz. 

One of the basic tools is [[Morse lemma]].

Cf. wikipedia: [Morse theory](http://en.wikipedia.org/wiki/Morse_theory)