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

This might follow from constructing it using double gluing and orthogonality (see discussion thread).

## Focused Orthogonality

Let $C$ be a [[star-autonomous]] category, and let $F\subseteq C(I,I^*)$ be any set: it is called a **focus**. One can then form a **focused tight orthogonality category** along similar lines. The first example is when $C$ is the category of relations, so a focus is just a set of cardinals $\leq 1$. But the construction works generally. 

Let $X$ be an object of $C$. Given $u\in C(I,X)$ and $v\in C(X,I^*)$, we write $u\perp v$ if $(v\circ u)\in F$.  This relation defines a [[Galois connection]] between $C(I,X)$ and $C(X,I^*)$ in the usual way: for $\mathcal{U}\subseteq C(I,X)$ we have $\mathcal{U}^\perp = \{ v \in C(X,I^*) \mid \forall u\in \mathcal{U}. u\perp v \}$, and likewise for $\mathcal{V}\subseteq C(X,I^*)$ we have $\mathcal{V}^\perp = \{ u \in C(I,X) \mid \forall v\in \mathcal{V}. u\perp v \}$.

We define a **$F$-tight-orthogonality space** to be an object $X\in C$ together with a $\mathcal{U}\subseteq C(I,X)$ that is a fixed point of this Galois connection, $\mathcal{U} = \mathcal{U}^{\perp\perp}$.  
A **morphism** between $F$-tight-orthogonality spaces $(X,\mathcal{U})\to (Y,\mathcal{V})$ is a morphism $f\in C(X,Y)$ such that

1. if $u\in \mathcal{U}$, then $f\circ u \in \mathcal{U}$;
2. if $v\in\mathcal{V}^\perp$ then $v\circ f\in \mathcal{U}^\perp$.

**Theorem:** (Hyland-Schalk): For any focus $F\subseteq C(I,I^*)$ on a star-autonomous category $C$, the $F$-tight-orthogonality spaces form a [[star-polycategory]].

More generally, we can consider an arbitrary family of subsets $\bot_X\subseteq C(I,X)\times C(X,I^*)$, which might or might not arise from a focus. We can define $\bot$-tight-orthogonality spaces in the same way. 

**Theorem:** (Hyland-Schalk): If an orthogonality $\bot_X\subseteq C(I,X)\times C(X,I^*)$ satisfies the four conditions for orthogonalities, a symmetry condition, and a precision condition, then the $\bot$-tight-orthogonality spaces form a [[star-polycategory]].

A typical example is $C=Rel$ and $u \bot v$ if $|u\cap v| \lt \omega$, which gives finiteness spaces.

**Conjecture:** any set of cardinal numbers induces a symmetric precise orthogonality on $Rel$. 

## References

The theory of focused orthogonality categories is developed in Section 5 of 

* [[Martin Hyland]] and Andrea Schalk, _Glueing and orthogonality for models of linear logic_, Theoretical Computer Science 294 (2003) 183–231 ([pdf](https://core.ac.uk/download/pdf/21173316.pdf))
 {#HylandSchalk}

[[!redirects arity spaces]]
