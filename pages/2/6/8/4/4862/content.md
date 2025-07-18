
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The **circle** (the 1-[[dimensional|dimension]] [[sphere]]) is a fantastic thing with lots and lots of [[stuff, structure, property|properties and extra structures]].  It is a:

* [[topological space]]

* [[smooth manifold]]

* [[Lie group]] (the [[circle group]])

* [[co-H-group]]

and it is one of the basic building blocks for lots of areas of mathematics, including:

* [[homotopy theory]]

* [[loop spaces]]

* [[knots]] and [[links]]


## Definition

We consider the circle first as a [[topological space]], then as the [[homotopy type]] represented by that space.

### As a topological space

+-- {: .num_defn #circle}
###### Definition
The two most common definitions of the circle as a [[topological space]] are:

1. It is the [[topological subspace]] of $\mathbb{C}$ consisting of those numbers of [[norm]]/[[absolute value]] $1$:

   $$
     U(1) \coloneqq \{z \in \mathbb{C} : {|z|} = 1\}
   $$

   (of course, $\mathbb{C}$ can be identified with $\mathbb{R}^2$ and an equivalent formulation of this definition given; also, to emphasise the reason for the notation $U(1)$, $\mathbb{C}$ can be replaced by $\mathbb{C}^* = GL_1(\mathbb{C})$)

2. It is the quotient of $\mathbb{R}$ by the integers:

   $$
   S^1 \coloneqq \mathbb{R}/\mathbb{Z}
   $$
=--

The standard equivalence of the two definitions is given by the map $\mathbb{R} \to \mathbb{C}$, $t \mapsto e^{2 \pi i t}$.

In constructive mathematics, the notions of real numbers and complex numbers split into multiple notions. In general, if the metric space of the real numbers is not [[sequentially Cauchy complete]], such as in the [[modulated Cantor real numbers]], then the two definitions cannot be proven to be equivalent, since the [[exponential function]] is not well defined on $\mathbb{C}$. Only if the real numbers are [[sequentially Cauchy complete]] are the two definitions the same. 

### As a homotopy type

As the bare [[homotopy type]], the [[shape modality|shape]] $&#643; S^1 \simeq \mathbf{B}\mathbb{Z}$ of the [[cohesion|cohesive]] circle $S^1$ is equivalent to the [[homotopy pushout]]

$$
  &#643; S^1 \simeq * \coprod_{* \coprod * } * 
  \,.
$$

In [[homotopy type theory]], this can be formalized as a [[higher inductive type]] generated by a point `base` and a path from `base` to itself; see [[circle type]] for more.

## Properties

The topological circle is a [[compact space|compact]], [[connected space|connected]] [[topological space]].  It is a $1$-[[dimension|dimensional]] [[smooth manifold]] (indeed, it is the only $1$-dimensional compact, connected smooth manifold).  It is **not** [[simply connected space|simply connected]]. 

The circle is a model for the [[classifying space]] for the [[abelian group]] $\mathbb{Z}$, the [[integer|integers]]. Equivalently, the circle is the [[Eilenberg-Mac Lane space]] $K({\mathbb{Z}},1)$. Explicitly, the first [[homotopy group]] $\pi_1(S^1)$ is the [[integer|integers]] $\mathbb{Z}$. But the higher [[homotopy groups]] $\pi_n(S^1) \simeq *$, $n \gt 1$ all vanish (and so is a [[homotopy type|homotopy 1-type]]). This can be deduced from the result that the loop space $\Omega S^1$ of the circle is the group ${\mathbb{Z}}$ of integers and that $S^1$ is path-connected. Proofs of this in [[homotopy type theory]] are in the [references](#references).

The result that $S^1\simeq K({\mathbb{Z}},1)$ holds in a general [[Grothendieck (∞,1)-topos]]. In fact, more generally, for $X$ a pointed object of a [[Grothendieck (∞,1)-topos]] ${\mathcal{H}}$, there is a natural equivalence between the [[suspension object]] $\Sigma X$ and the classifying space $ B{\mathbb{Z}}\wedge X$. In particular, when $X$ is specifically the 0-truncated two-point space $S^0$, we get $S^1\simeq K({\mathbb{Z}},1)$.

 

The [[product]] of the circle with itself is the ($2$)-[[torus]]

$$
  T = S^1 \times S^1
  \,.
$$

Generally, the $n$-torus $T^n$ is $(S^1)^n$.

## Related concepts

* [[unit circle]]

* [[circle action]]

* [[minimal simplicial circle]]

* [[circle type]]

* [[sphere]]

* [[pseudocircle]]

* [[conic section]]

  * [[ellipse]], [[parabola]], [[hyperbola]]

* [[circumference of a circle]]

* [[area of a circle]]

## References

A formalization of the [[shape modality|shape]] [[homotopy type]] $&#643; S^1 \simeq \mathbf{B}\mathbb{Z}$ of the circle as a [[higher inductive type]] in [[homotopy type theory]], along with a proof that $\Omega &#643;S^1\simeq {\mathbb{Z}}$ (and hence $\pi_1(&#643;S^1) \simeq \mathbb{Z}$):

* {#LicataShulman13} [[Dan Licata]], [[Mike Shulman]], *Calculating the Fundamental Group of the Circle in Homotopy Type Theory*, LICS '13: Proceedings of the 2013 28th Annual ACM/IEEE Symposium on Logic in Computer Science June 2013 ([arXiv:1301.3443](http://arxiv.org/abs/1301.3443), [doi:10.1109/LICS.2013.28](https://doi.org/10.1109/LICS.2013.28))

  > blog announcement: [A formal proof that $\pi_1(S^1) = \mathbb{Z}$](https://homotopytypetheory.org/2011/04/29/a-formal-proof-that-pi1s1-is-z/)

* {#BezemBuchholtzGraysonShulman19} [[Marc Bezem]], [[Ulrik Buchholtz]], [[Daniel Grayson]], [[Michael Shulman]], _Construction of the Circle in UniMath_, Journal of Pure and Applied Algebra Volume 225, Issue 10, October 2021, 106687 ([arXiv:1910.01856](https://arxiv.org/abs/1910.01856))

The proof is formalized therein using the [[Agda]] [[proof assistant]].  See also

* The [[HoTT Book]], section 8.1

* The HoTT Coq-HoTT library: [theories/Spaces/Circle.v](https://github.com/HoTT/Coq-HoTT/blob/V8.18/theories/Spaces/Circle.v), [theories/Homotopy/Pi1S1.v](https://github.com/HoTT/Coq-HoTT/blob/V8.18/theories/Homotopy/Pi1S1.v)

* The HoTT Agda library: [homotopy/LoopSpaceCircle.agda](https://github.com/HoTT/HoTT-Agda/blob/2.0/homotopy/LoopSpaceCircle.agda)

[[!redirects circle]]
[[!redirects circles]]
[[!redirects Circle]]
[[!redirects Circles]]

[[!redirects 1-sphere]]
[[!redirects 1-spheres]]

