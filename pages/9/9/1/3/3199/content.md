
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

### Heat kernel as a fundamental solution

One of the simplest linear partial differential equations of parabolic type is the heat (conductivity) equation. Recall that a [[fundamental solution]] of a linear partial differential operator $P$ is a solution of the PDE $P f = \delta$ where the inhomogeneous term $\delta$ is a [[delta function]] (in appropriate boundary conditions).

The fundamental solution of a heat equation is called the **heat kernel**. 

### Role in index theory

The study of heat kernel led to a new simpler proof of the [[index theorem]] by [[Michael Atiyah|Atiyah]], [[Raoul Bott|Bott]] and Patodi.

### Heat kernel for operators over Riemannian manifolds

Let $E\to X$ be a smooth vector bundle over a [[Riemannian manifold]] $X$, $\Gamma(E)$ the space of the smooth sections of $E$ and $P:\Gamma(E)\to\Gamma(E)$ a positive self-adjoint elliptic differential operator. The **heat operator** symbolically denoted by $e^{-tP}:\Gamma(E)\to\Gamma(E)$ is an infinitely smoothening operator characterized by the property that 

$$
\frac{d}{dt} (e^{-tP}u) = -Pe^{-tP}u
$$

for all $u\in\Gamma(E)$. The **heat kernel** $K$ for $P$ is then the kernel of an [[integral operator]] representing the heat operator:

$$
(e^{-tP}u)(x) = \int_X K_t(x,y) u(y) dy
$$ 

$K_t(x,y):E_y\to E_x$ is a linear map for all $x,y$ and $t$. Of course, one needs to justify this definition by the proof of the existence. 

### Heat kernel and path integrals

The [[Schrödinger equation]] without potential term is similar to the 
[[heat equation]] (there is an additional $\sqrt{-1}$); hence its fundamental solution is similar. The heat equation on the other hand can describe [[diffusion]]. Therefore also the similarity in the [[path integral]] description: the [[Wiener measure]] [[integral]] describes diffusion using [[Brownian motion]], similarly the Feynman path integral (for a finite-dimensional system) describes [[quantum mechanics]]; many points in the standard calculations are parallel. 

## Related concepts

* [[Laplace operator]]

* [[heat kernel]]

## References

A standard textbook account is

* [[Nicole Berline]], [[Ezra Getzler]], [[Michele Vergne]], _Heat kernels and Dirac operators_, Grundlehren __298__, Springer 1992, "Text Edition" 2003. 

For the relation to the [[index theorem]] see also

* [[Michael Atiyah]], [[Raoul Bott]], V. K. Patodi, On the heat equation and the index theorem, Invent. Math. 19 (1973), 279&#8211;330.

Discussion in the context of [[renormalization]] in [[quantum field theory]] is around section 6.5 of 

* [[Kevin Costello]], _Renormalisation and the Batalin-Vilkovisky formalism_ ([arXiv:0706.1533](http://arxiv.org/abs/0706.1533))

See also

* H. Blaine Lawson, Jr. , Marie-Louise Michelson, _Spin geometry_, Princeton Univ. Press 1989.

* Wikipedia, _[Heat kernel](http://en.wikipedia.org/wiki/Heat_kernel)_


[[!redirects heat kernels]]
