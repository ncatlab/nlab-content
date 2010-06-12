## Idea

A *pullback in a derivator* is the generalization to the context of a [[derivator]] of the notion of [[pullback]] in ordinary category theory.  Viewing a derivator as the "shadow" of an [[(∞,1)-category]], the notion of monomorphism therein coincides with the notion of [[homotopy pullback]] in an $(\infty,1)$-category.

## Definition

Let $\square$ denote the category
$$ \array{a & \to & b \\ \downarrow & & \downarrow \\ c & \to & d} $$
that is the "free-living [[commutative square]]", and let $L$ be the full subcategory of $\square$ on $b,c,d$, with inclusion $u\colon L\to \square$.

Let $D$ be a [[derivator]] and let $X\in D(\square)$ be a commutative square in $D$.  We say that $X$ is a **pullback square** if the unit $X\to u_* u^* X$ of the [[adjunction]] $u^*\dashv u_*$ is an isomorphism.  Since $u$ is [[fully faithful]], so is $u_*$, so this is equivalent to saying that there exists some $Y\in D(L)$ such that $X\cong u_* Y$.

If $D$ is merely a prederivator, then we can phrase the same definition by saying that $X$ has the universal property that $u_* u^* X$ would, if the whole functor $u_*$ existed.

[[!redirects pullbacks in a derivator]]
[[!redirects pullbacks in derivators]]
[[!redirects cartesian square in a derivator]]
[[!redirects cartesian squares in a derivator]]
[[!redirects cartesian squares in derivators]]
[[!redirects fiber product in a derivator]]
[[!redirects fiber products in a derivator]]
[[!redirects fiber products in derivators]]
