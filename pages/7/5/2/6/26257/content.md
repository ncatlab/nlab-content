
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Fibred category theory
+-- {: .hide}
[[!include fibred category theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
**Fibred functors** are morphisms between [[fibred categories]].
They are 1-cells in the [[2-category]] $\mathbf{Fib}$.

## Definition
A **fibred functor** between [[fibred categories]] $p:\mathcal{E} \to \mathcal{B}$ and $p':\mathcal{E}' \to \mathcal{B}'$ is a pair of functors $F_0:\mathcal{B} \to \mathcal{B}'$ and $F_1:\mathcal{E} \to \mathcal{E}'$ such that the following commutes:
\begin{tikzcd}
\mathcal{E} \arrow[swap]{d}{p} \arrow{r}{F_1} & \mathcal{E}' \arrow{d}{p'}\\
\mathcal{B} \arrow{r}{F_0} & \mathcal{B}',
\end{tikzcd}
and such that $F_1$ preserve [[cartesian morphisms]].

Symbolically, preserving cartesian morphisms means that for each $E:\mathcal{E}$ and $f:B \to p(E)$ morphism in the base, we have $F_0(f)^*E \cong F_1(f^*E)$, where $(-)^*$ denotes reindexing.

\begin{remark}
When $F_0$ is the identity we recover the notion of morphism between fibrations over the same base (which are the 1-cells in $\mathbf{Fib}(\mathcal{B})$).
In that case, $F_1$ induces a family of functors between fibers over the same object in the base.
\end{remark}

## For cloven fibrations
If $p$ and $p'$ are assumed to be [[cloven fibrations]], then a **(cloven) fibred functor** between them is assumed to preserve the cleavage, i.e. the choice of cartesian lifts.

## Properties
The total category of a fibration supports a [[factorization system]] whose left class is comprised of vertical maps (those projecting to an isomorphism) and whose right class are [[cartesian morphism|cartesian maps]].
Fibred functors, by definition, only support the latter, because vertical maps are supported by square of functors in general:

\begin{proposition}
Consider a [[commutative square]] of [[functors]]:
\begin{tikzcd}
\mathcal{E} \arrow[swap]{d}{p} \arrow{r}{F_1} & \mathcal{E}' \arrow{d}{p'}\\
\mathcal{B} \arrow{r}{F_0} & \mathcal{B}',
\end{tikzcd}
Then $F_1$ sends $p$-vertical maps to $p'$-vertical maps.
\end{proposition}
\begin{proof}
Let $\varphi:D \to E$ be a vertical map in $\mathcal{E}$, meaning $p(\varphi) = 1_{B}$, where $B=p(D)=p(E)$. Then $F_1(\varphi) : F_1(D) \to F_1(E)$ is a 1-cell over $p'(F_1\varphi) = F_0(p(\varphi)) = 1_{F_0B}$.
\end{proof}

Thus fibred functors preserve the vertical-cartesian factorization of maps.

## See also
* [[fibred category]], [[fibred natural transformation]]

[[!redirects morphism of fibrations]]
[[!redirects morphisms of fibrations]]
[[!redirects fibered functor]]
[[!redirects fibered functors]]
[[!redirects fibred functors]]