
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Every [[generalized (Eilenberg-Steenrod) cohomology]]-theory has a refinement to [[differential cohomology]]. By _ordinary differential cohomology_ one refers, for emphasis, to the differential refinement of _ordinary [[integral cohomology]]_ , hence of the [[cohomology theory]] represented by the [[Eilenberg-MacLane spectrum]] $K(-,\mathbb{Z})$. To the extent that [[integral cohomology]] is often just called _cohomology_ if the context is clear, _ordinary differential cohomology_ is often called just _differential cohomology_ .

Here we write $H_{diff}^\bullet(X)$ for the ordinary differential cohomology groups of a [[smooth manifold]] $X$. 

## Properties

There are two [[natural transformation|natural]] morphism

1. underlying cocycle $c : H_{diff}^\bullet(X) \to H^\bullet(X,\mathbb{Z})$ produces the cocycle in [[integral cohomology]] that underlies a differential cocycle;

1. [[curvature]] $F : H_{diff}^\bullet(X) \to \Omega^\bullet_{cl}(X)$ produces a closed [[differential form]] of degree $n$.

There are various equivalent [[cocycle]]-models for ordinary differential cohomology. They include

* [[Cheeger-Simons differential character]]s;

* [[Deligne cohomology]];

* [[circle n-bundles with connection]].

The last of these are often known as $U(1)$-[[gerbe]]s or [[bundle gerbe]]s with connection.

Cocycles $\nabla \in H_{diff}^2(X)$ in degree 2 ordinary differential cohomology are represented by ordinary [[circle group]]-[[principal bundle]]s with [[connection on a bundle|connection]] on $X$.  The class $c(\nabla) \in H^2(X,\mathbb{Z})$ is the [[Chern class]] of the underlying circle bundle and the form $F_\nabla \in \Omega^2_{cl}(X)$ is the [[curvature]] 2-form of the connection $\nabla$.


## Applications

### In Chern-Weil theory

For $X$ a [[smooth manifold]], $G$ a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ and [[invariant polynomial]] $\langle -\rangle$ of degree $2n$, the [[Chern-Weil homomorphism]] may b refined to a morphism

$$
  H^1(X,G) \to H_{diff}^{2n}(X)
$$

from the first [[nonabelian cohomology]] of $X$ classifying $G$-[[principal bundle]]s to degree $2n$ ordinary differential cohomology.

The projection

$$
  H^1(X,G) \to H_{diff}^{2n}(X) \stackrel{c}{\to} H^{2n}(X,\mathbb{Z})
$$

is the integral [[characteristic class]] corresponding to the invariant polynomial and the projection

$$
  H^1(X,G) \to H_{diff}^{2n}(X) \stackrel{F}{\to} \Omega^{2n}_{cl}(X)
$$

is a differential form which represents the image of this class under $H^{2n}(X,\mathbb{Z}) \to H^{2n}(X,\mathbb{R})$ in [[de Rham cohomology]] (under the [[de Rham theorem]]).

### In physics

In [[physics]]

* the [[electromagnetic field]] is a cocycle in degree 2 ordinary differential cohomology 

* the [[Kalb-Ramond field]] is a cocycle in degree 3;

* the [[supergravity C-field]] is a cocyce in degree 4.


## References

A good discussion is in 

* [[Mike Hopkins]], I. Singer, [[Quadratic Functions in Geometry, Topology,and M-Theory]] ([arXiv](http://arxiv.org/abs/math.AT/0211216))

  * A pedestrian introduction of ordinary differential cocycles is in section 2.3 there. 

  * The systematic construction and definition via a [[homotopy pullback]] is in section 3.2.

  * The relation to Chern-Weil theory is in section 3.3.
