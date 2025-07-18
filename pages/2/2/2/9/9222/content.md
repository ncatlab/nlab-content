> This page is about densities on manifolds. For density in category theory, see [[dense functor]].

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _density_ on a [[manifold]] of [[dimension]] $n$ is a [[function]] that to each point assigns an [[infinitesimal object|infinitesimal]] [[volume]] (in general signed, and possibly degenerate), hence a volume  of $n$-[[hypercubes]] in the [[tangent space]] at that point.  A positive definite density is equivalently a _[[volume element]]_ (or a volume form on an [[orientation|oriented]] manifold).


## Definition

For $X$ a [[manifold]] its **1-density bundle** is the  real [[line bundle]] [[associated bundle|associated]] to the [[principal bundle]] underlying the [[tangent bundle]] by the 1-dimensional [[representation]] of the [[general linear group]]

$$
  \array{
  GL(n) &\to& GL(1) \simeq Aut_{Vect}(\mathbb{R}^1)
  \\
  A &\mapsto& |det(A)|^{-1}.
  }
$$

A [[section]] of the $1$-density bundle on $X$ is called a _$1$-density on $X$_. 

This is the general object against which one has [[integration]] of functions on $X$.

{#sDensities} More generally, for $s \in \mathbb{R} - \{0\}$ an **$s$-density** is a section of the [[line bundle]] which is [[associated bundle|associated]] to the principal bundle by the representation

$$
  \array{
  GL(n) &\to& GL(1) \simeq Aut_{Vect}(\mathbb{R}^1)
  \\
  A &\mapsto& |\det(A)|^{-s}.
  }
$$

The parameter $s$ is called the __weight__ of the density.  In particular for $s = 1/2$ one speaks of **half-densities**.

## Properties and applications

### Physical interpretation

We earlier spoke of a density (of weight $1$) $\rho$ as a measure of [[volume]], but in application to [[physics]] a density on [[spacetime]] (or space) might as easily be a measure of some other [[extensive quantity]] $Q$ (say, [[mass]]).  We then call $\rho$ the __$Q$-density__ (say, _mass density_); the [[integration of differential forms|integral]] of $\rho$ over a region $R$ is the amount of $Q$ in $R$.

Relative to a nondegenerate notion of volume given by another density $vol$, the ratio $\rho/vol$ is a [[scalar field]], an [[intensive quantity]] which is often also referred to as the _density_.  But $\rho$ itself is more fundamental in the [[geometry of physics]].

### Wave functions and canonical Hilbert spaces

In the context of [[geometric quantization]] one considers spaces of [[sections]] of [[line bundles]] ("[[prequantum line bundles]]") and tries to equip these with an [[inner product]] given by pointwise pairing followed by [[integration]] over the base such as to then [[completion|complete]] to a [[Hilbert space]]. 

One can define the [[integration]] against a fixed chosen [[measure]], but more canonical is to instead form the [[tensor product]] of the prequantum line bundle with the bundle of half-densities. The compactly supported sections of that tensor bundle can then naturally be integrated. This is sometimes called the "canonical Hilbert space" construction (e.g. ([Bates-Weinstein](#BatesWeinstein))).


## Related concepts

* [[volume form]]

* [[canonical bundle]], [[determinant line bundle]]

* [[pseudoscalar field]]

* [[canonical Hilbert-space of half-densities]]

* [[Verdier duality]]

[[!include square roots of line bundles - table]]


## References

A textbook account is for instance on p. 29 of 

* [[Nicole Berline]], [[Ezra Getzler]], [[Michele Vergne]], _Heat kernels and Dirac operators_, Springer (2004)

Discussion of half-densities in the context of [[geometric quantization]] is in 

* {#BatesWeinstein} Sean Bates, [[Alan Weinstein]], _Lectures on the geometry of quantization_, [pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf)
 


[[!redirects density]]
[[!redirects densities]]

[[!redirects density bundle]]
[[!redirects density bundles]]
[[!redirects density line bundle]]
[[!redirects density line bundles]]

[[!redirects half-density]]
[[!redirects half-densities]]

[[!redirects half-density bundle]]
[[!redirects half-density bundles]]
[[!redirects half-density line bundle]]
[[!redirects half-density line bundles]]
