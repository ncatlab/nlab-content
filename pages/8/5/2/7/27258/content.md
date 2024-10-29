
> This page is about the concept in [[functorial geometry|functorial]] [[algebraic geometry]]. For functors between [[Z-categories]] see there.

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

The terminology is due to

* [[Michel Demazure]], [[Pierre Gabriel]], _Groupes algebriques_, tome 1,  avec un appendice _Corps de classes local_ par [[Michiel Hazewinkel|Hazewinkel M]], Mason and Cie, Paris (1970) 
  > (later volumes never appeared)

English translation:

* [[Michel Demazure]], [[Peter Gabriel]], *Introduction to algebraic geometry and algebraic groups*, North-Holland mathematics studies **39** (1980) &lbrack;[ISBN:9780080871509](https://shop.elsevier.com/books/introduction-to-algebraic-geometry-and-algebraic-groups/demazure/978-0-444-85443-8)&rbrack;


Formulation in [[univalence|univalent]] [[homotopy type theory]]:

* [[Max Zeuner]]: *Univalent Foundations of Constructive Algebraic Geometry* &lbrack;[arXiv:2407.17362](https://arxiv.org/abs/2407.17362)&rbrack;

[[!redirects Z-functor]]
[[!redirects Z-functors]]

[[!redirects integer functor]]
[[!redirects integer functors]]