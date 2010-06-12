## Idea

A *monomorphism in a derivator* is the generalization to the context of a [[derivator]] of the notion of [[monomorphism]] in ordinary category theory.  Viewing a derivator as the "shadow" of an [[(∞,1)-category]], the notion of monomorphism therein coincides with the notion of [[monomorphism in an (∞,1)-category]].

## Definition

Let $\square$ denote the category
$$ \array{a & \to & b \\ \downarrow & & \downarrow \\ c & \to & d} $$
that is the "free-living [[commutative square]]", let $I$ be the [[interval category]] $(0\to 1)$, and let $p\colon \square \to I$ denote the functor collapsing $a,b,c$ to $0$ and sending $d$ to $1$.

Let $D$ be a [[prederivator]] and $f\colon X\to Y$ a morphism in $D(1)$.  By one of the axioms of a derivator, there exists an object $F\in D(I)$ representing $f$, which is unique up to non-unique isomorphism.  We say that $f$ is a **monomorphism** in $D$ if $p^*(F) \in D(\square)$ is a [[pullback in a derivator|pullback square]].

## Examples

* It is well-known and easy to verify that a morphism $f:A\to B$ in a 1-category is a [[monomorphism]] if and only if the square 
  $$ \array{ A & \overset{id}{\to} & A \\ ^{id}\downarrow & & \downarrow^f \\ A &\underset{f}{\to} & B } $$
  is a [[pullback]].  Therefore, in representable prederivators this definition reduces to the usual notion of monomorphism.

* In the homotopy derivator of an $(\infty,1)$-category, one can check that this reduces to the usual notion of [[monomorphism in an (∞,1)-category]].

[[!redirects monomorphisms in a derivator]]
[[!redirects monomorphisms in derivators]]
