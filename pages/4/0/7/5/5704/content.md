## Idea

A *quotient space* is a [[quotient object]] in the [[category]] [[Top]] of [[topological spaces]].

## Definition

Let $X$ be a [[topological space]] and $\sim$ an [[equivalence relation]] on (the underlying set of) $X$.  (Since [[monomorphisms]] in [[Top]] are just [[injection|injective]] [[continuous maps]], to give an equivalence relation on the underlying set of a topological space is the same as to give a [[congruence]] on that space in $Top$.)  Let $Y = X/\sim$ be the [[quotient set]] and $q\colon X\to Y$ the quotient map.

The **quotient topology**, or **identification topology**, induced on $Y$ from $X$ says that a subset $U\subseteq Y$ is [[open subset|open]] if and only if $q^{-1}(U)\subseteq X$ is open.  With this topology $Y$ is a **quotient space** or **identification space** of $X$.

Obviously, up to [[homeomorphism]], all that matters is the surjective function $X\to Y$.  For the above definition, we don't even need it to be surjective, and we could generalize to a [[sink]] instead of a single map; in such a case one generally says *final topology* or *strong topology*.  See [[topological concrete category]].

## Related pages

* [[image]]

* [[subspace]]

* [[subframe]]

[[!redirects quotient topology]]
[[!redirects quotient spaces]]
[[!redirects quotient topologies]]
[[!redirects identification space]]
[[!redirects identification topology]]
[[!redirects identification spaces]]
[[!redirects identification topologies]]
