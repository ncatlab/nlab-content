# Arity spaces

* table of contents
{: toc}

## Idea

An **arity space** is a common generalization of [[coherence spaces]], [[finiteness spaces]], and [[totality spaces]] to an arbitrary set of "arities".

+--{: .standout}
This is an original and tentative definition.  In particular, it's not clear whether the allowed sets of arities should be restricted in some way.  Should they be an [[arity class]]?  The only previously studied examples appear to be the cases $\{0,1\}$ (coherence spaces), $\{0,1,2,3,\dots\}$ (finiteness spaces), and $\{1\}$ (totality spaces), which are all arity classes.
=--

## Definition

Let $\kappa$ be a set of [[cardinal numbers]].  Given two [[subsets]] $u,v\subseteq X$ of the same [[set]] $X$, we write $u\perp v$ if $|u\cap v|\in \kappa$.  This relation defines a [[Galois connection]] in the usual way: for $\mathcal{U}\subseteq P(X)$ we have $\mathcal{U}^\perp = \{ v \mid \forall u\in \mathcal{U}. u\perp v \}$.  Since $\perp$ is symmetric, $(-)^\perp$ is self-adjoint on the right.

We define a **$\kappa$-arity space** to be a set $X$ together with a $\mathcal{U}\subseteq P(X)$ that is a fixed point of this Galois connection, $\mathcal{U} = \mathcal{U}^{\perp\perp}$.  We call the sets in $\mathcal{U}$ **$\kappa$-ary** and the sets in $\mathcal{U}^{\perp}$ **co-$\kappa$-ary**.

A **morphism** or **relation** between $\kappa$-arity spaces is a [[relation]] $R: X &#8696; Y$ such that

1. If $u\subseteq X$ is $\kappa$-ary, then $R[u] = \{ y \mid \exists x\in u, R(x,y) \}$ is $\kappa$-ary.
1. If $v\subseteq Y$ is co-$\kappa$-ary, then $R^{-1}[v] = \{ x \mid \exists y\in v, R(x,y) \}$ is co-$\kappa$-ary.

## Examples

* If $\kappa=\{0,1\}$, then a $\kappa$-arity space is precisely a [[coherence space]].

* If $\kappa = \omega = \{0,1,2,3,\dots\}$, then a $\kappa$-arity space is precisely a [[finiteness space]].

* If $\kappa=\{1\}$, then a $\kappa$-arity space is (almost?) precisely a [[totality space]].

## Properties

**Conjecture:** For any $\kappa$, the category of $\kappa$-arity spaces is [[star-autonomous]].

This might follow from constructing it using [[double gluing]] and orthogonality.

## Construction as a Comma Double Category

We can define arity spaces by a variation on the [[double gluing]] construction.

Define a double category $Orth$ of orthogonalities 
1. Objects are relations $\bot \subseteq X \times Y$
2. A vertical morphism from $(X_1,Y_1,\perp_1)$ to $(X_2, Y_2, \perp_2)$ exists when $X_1$ and $Y_1$ are orthogonal subsets of $X_2$ and $Y_2$ respectively.
3. A horizontal morphism from $(X_1,Y_1,\perp_1)$ to $(X_2,Y_2,\perp_2)$ is a pair of a function $f_* : X_1 \to X_2$ and $f^* : Y_2 \to Y_1$
4. A square from $f$ to $g$ exists when $f_*$ is the restriction of $g_*$ and similarly for $f^*$ and $g^*$.

Then the (2-)category of arity spaces can be defined as the comma double category (where $Rel$ and $Set$ are viewed as vertically discrete double categories:

\begin{tikzcd}
  Arity(\kappa) \ar[d] \ar[r] \ar[dr,phantom,"\Downarrow"] & Set \times Set^o \ar[d] \\
  Rel \ar[r,"L_\kappa"'] & Orth
\end{tikzcd}

Where $L_\kappa$ maps a set $X$ to the orthogonality $|U \cap V| \leq \kappa$ on $Subset(X) \times Subset(X)$ and a pair of sets $X, Y$ is given the trivial orthogonality $x \perp y = \bot$

[[!redirects arity spaces]]
