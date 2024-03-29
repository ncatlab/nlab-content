[[!redirects geometric quantization with KU-coefficients]]

> This entry is a chapter of _[[geometry of physics]]_. See there for context.

> previous chapters: _[[geometry of physics -- modules|modules]]_

***

#Contents#
* table of contents
{:toc}


## Introduction

In the section _[[prequantized Lagrangian correspondences]]_ we had seen how [[classical mechanics]] is captured by [[smooth groupoids]] slices over $\mathbf{B}U(1)$.

We consider this now as the [[boundary field theory]] of the [[2d Poisson-Chern-Simons theory]] in [[smooth infinity-groupoids]] over $\mathbf{B}^2 U(1)$ and discuss [[geometric quantization]] from the point of view of the holographic/[[motivic quantization]] of this system.

That is we consider the [[symplectic groupoid]] $SG(X,\pi)$ of a [[Poisson manifold]] $(X,\pi)$ as equipped with its [[prequantum line n-bundle|prequantum line 2-bundle]]. $SH(X,\pi) \to \mathbf{B}^2 U(1)$. We linearize this to an [[(infinity,1)-module bundle]] by composing with $\mathbf{B}^2 U(1)\to B GL_1(KU)$. Then we perform the boundary [[path integral quantization]] by [[fiber integration in K-theory]] and show how this reproduces, on the boundary, traditional [[geometric quantization]] such as in particular the [[orbit method]].

$$
  \array{
    && X
    \\
    & \swarrow && \searrow
    \\
    \ast && && SG(X,\pi)  && && pre-quantum
    \\
    & \searrow & \swArrow & \swarrow
    \\
    && \mathbf{B}^2 U(1)
    \\
    && \downarrow && && && \downarrow^{\mathrlap{quantization}}
    \\
    && B GL_1(KU)
    \\
    \\
    KU(\ast) &&\longrightarrow && KU(SG(X,\pi)) && && quantum
  }
$$

The abstract picture behind this cohomological [[motivic quantization]] is discussed at _[[dependent linear type theory]]_. Here we focus on explicit details for the case of [[KU]]-quantization.

## KU-theory

### Twisted KU-cohomology of manifolds

([Rosenberg 04](twisted+K-theory#Rosenberg89), [Atiyah-Segal 04](twisted+K-theory#AtiyahSegal04)), review is in ([Nuiten section 3.2.1](#Nuiten))

### Twisted KU-cohomology of smooth local quotient stacks

([FHT I](#FHT)), reviewed in ([Nuiten section 3.3.2](#Nuiten))

Write $H_0$ for the $\mathbb{Z}/2\mathbb{Z}$-graded [[separable Hilbert space]].

+-- {: .num_prop}
###### Proposition

For $X$ a [[smooth manifold]] and $G$ a [[compact Lie group]] with [[action]] on $X$, then the [[Hilbert bundle]]

$$
  E \coloneqq X \times H_0 \otimes L^2(G) \to X
$$ 

equipped with the $G$-action on the fibers given on $L^2(G)$ by pullback along the right $G$-action on itself is a universal equivariant Hilbert bundle, meaning that the space of equivariant sections of the associated Fredholm bundle is the $G$-[[equivariant K-theory]] of $X$

$$
  K^\bullet(X//G)
  \simeq
  \Gamma(X, Fred^\bullet(E))
  \,.
$$

=--

### Twisted integration with KU-coefficients




[[fiber integration in K-theory]]

along maps of [[manifolds]] ([CareyWang08](#CareyWang08))

along [[representable morphisms]] of [[local quotient stacks]] ([FHT I](#FHT))


review is in [Nuiten section 4.2](#Nuiten)


## Geometric quantization

[Bongers, section 2](#Bongers)


### Symplectic manifold with Hamiltonian $G$-action


([Nuiten, section 5.2.1](#Nuiten))


### Universal orbit quantization

([FHT II, section 1](#FHT)) ([Nuiten, section 5.2.2](#Nuiten))



## References

* {#Bongers} Stephan Bongers, _[[schreiber:master thesis Bongers|Geometric quantization of symplectic and Poisson manifolds]]_, 2014

* {#Nuiten} [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_, 2013

* {#CareyWang08} [[Alan Carey]], [[Bai-Ling Wang]], _Thom isomorphism and push-forward map in twisted K-theory_, J. K-Theory 1(2), 357-393 (2008) ([arXiv:0507414](http://arxiv.org/abs/math/0507414))

* {#FHT} [[Daniel Freed]], [[Mike Hopkins]], [[Constantin Teleman]], _[[Loop Groups and Twisted K-Theory]]_ I (2011) ([arXiv:0711.1906](http://arxiv.org/abs/0711.1906)), II (2013) ([arXiv:0511232](http://arxiv.org/abs/math/0511232))
