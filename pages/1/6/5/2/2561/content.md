# Idea

Copairing is [[opposite category|dual]] to [[pairing]].


# Definition

Let $X$ and $Y$ be [[objects]] of some [[category]] $C$, and suppose that [[the]] [[coproduct]] $X \amalg Y$ exists in $C$.

Let $T$ be some object of $C$, and let $a\colon X \to T$ and $b\colon Y \to T$ be [[morphisms]] of $C$.  Then, by definition of [[coproduct]], there exists a unique morphism $[a,b]\colon X \amalg Y \to T$ such that the obvious diagrams commute.

This $[a,b]$ is the __copairing__ of $a$ and $b$.


# Notation

When convenient, it is nice to write it vertically; all of the following are seen:
$$ \left({a \atop b}\right) ,\quad \left[{a \atop b}\right] ,\quad \left\{{a \atop b}\right\} .$$
The vertical notation can be combined with [[pairing]] to create a [[matrix]] notation for morphisms from a coproduct to a product.  This works best when products and coproducts are the same, as described at [[matrix calculus]].


# Examples

One often sees a [[function]] defined by cases as follows:
$$ f(x) = \left\{\array{ g(x) & \text {if}\; \phi(x) \\ h(x) & \text {if}\; \psi(x) .}\right. $$
Such a definition is valid in general iff the [[domain]] of $f$ is the (internal) [[disjoint union]] of its [[subsets]] $\{x : \phi(x)\}$ and $\{x : \psi(x)\}$.  In that case, let $X$ be the first subset, let $Y$ be the second, and let $T$ be the [[target]] of $f$; let $a\colon X \to T$ and $b\colon Y \to T$ be [[restriction]]s of $g$ and $h$.  Then we have $X \amalg Y$ as the domain of $f$, and $f$ itself is the copairing $[a,b]$.