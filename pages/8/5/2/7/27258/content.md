
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Definition

A **$\mathbb{Z}$-functor** or **integers functor** is a [[functor]] from the [[category]] of [[commutative rings]] [[CRing]] to the [[category of sets]] [[Set]]. The category of $\mathbb{Z}$-functors is thus the [[functor category]] $\mathrm{Set}^\mathrm{CRing}$. 

## Examples

* The [[forgetful functor]] $\mathbb{A}^1:\mathrm{CRing} \to \mathrm{Set}$ is a $\mathbb{Z}$-functor. 

* More generally, any [[affine scheme]] is a $\mathbb{Z}$-functor. 

## Properties

\begin{definition}
Let $X$ be a $\mathbb{Z}$-functor. Then the [[ring of fractions]] $\mathcal{O}(X)$ of $X$ is the [[set]] $X \Rightarrow \mathbb{A}^1$ of [[natural transformations]] from $X$ to the forgetful functor $\mathbb{A}^1$. 

The ring structure on $X \Rightarrow \mathbb{A}^1$ is defined pointwise by the following, for every commutative ring $R$ and element $x \in X(R)$:

$$0_R(x) \coloneqq 0 \qquad 1_R(x) \coloneqq 1$$

$$(a_R + b_R)(x) \coloneqq a_R(x) + b_R(x)$$

$$(- a_R)(x) \coloneqq - a_R(x)$$

$$(a_R \cdot b_R)(x) \coloneqq a_R(x) \cdot b_R(x)$$
\end{definition}

## Related concepts

* [[affine scheme]]

## References

* [[Max Zeuner]], *Univalent Foundations of Constructive Algebraic Geometry* ([arXiv:2407.17362](https://arxiv.org/abs/2407.17362))

[[!redirects Z-functor]]
[[!redirects Z-functors]]

[[!redirects integer functor]]
[[!redirects integer functors]]