+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

One source of cartesian [[differential category|differential categories]]
is [[tangent bundle categories]]:
in such a category, the [[full subcategory]] of [[objects]]
with a trivial (in the appropriate sense)
tangent bundle is a cartesian differential category.

## Definition

We present the revised definition of a cartesian differential category
due to Cruttwell \cite{Cruttwell}.

The adjective “cartesian” refers to the existence of finite products.

A prototypical example of a carteisan differential category
is the category whose objects are open subsets of finite-dimensional real vector (or affine) spaces
and morphisms are smooth maps.
Below, if $U\subset R^n$ is such an object, then $L_0(U)=R^n$ is the tangent space at any point of~$U$.

\begin{definition}
A __(generalized) cartesian differential category__
is a category $C$ with finite products
equipped with the following data:

* for any object $X\in C$ a commutative monoid
$$L(X)=(L_0(X),+_X\colon L_0(X)\times L_0(X)\to L_0(X),0_X\colon 1\to L_0(X))$$
(the tangent space at any point)
such that $L(L_0(X))=L(X)$ and $L(X\times Y)=L(X)\times L(Y)$;

* for any morphism $f\colon X\to Y$ in $C$, a morphism $D(f):L_0(X)\times X \to L_0(Y)$ (the derivative of $f$) such that

  * $D(+_X)=+_X\circ p_1$, $D(0_X)=0_X\circ p_1$ (where $p_1$ projects onto the first factor of a product);

  * (the derivative is a linear map)
$$D(f)\circ (a +_X b,c)=D(f)\circ (a,c) +_X D(f)\circ (b,c)$$
and
$$D(f)(0_X,a)=0_X$$
(where $a,b,c\colon A\to L_0(X)$ are morphisms in $C$);

  * (to be finished…)

\end{definition}

## Related concepts

* [[differential category]]


[[!redirects cartesian differential categories]]
