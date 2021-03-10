## Idea

[…]

## Definition

Suppose $U\colon A\to B$ is a [[functor]] that has a [[left multiadjoint]].

The __Diers spectrum__ of $U$ is the functor $B^{op}\to Set$
that sends an object $X\in B$ to the set $I$
that indexes the value
$(g_i\colon B\to U(A_i))_{i\in I}$
of the [[left multiadjoint]] of $U$ at $X$.
A morphism $f\colon X\to X'$ is sent to the induced map $I'\to I$
that assigns to $i'\in I'$ the unique $i\in I$
such that $g_{i'}\circ f\colon X\to U(A'_i)$ factors through $g_i$.

## Example

The category of [[integral domains]] and injective homomorphisms
is a [[multireflexive subcategory]] of the category of [[commutative rings]]
and ring homomorphisms.

The associated Diers spectrum functor is a functor
$$CRing^{op} \to Set$$
that sends a [[commutative ring]] to its [[prime spectrum]].

## Example

The category of [[reduced rings]] and injective homomorphisms
is a [[multireflexive subcategory]] of the category of [[commutative rings]]
and ring homomorphisms.

The associated Diers spectrum functor is a functor
$$CRing^{op} \to Set$$
that sends a [[commutative ring]] to its poset of [[radical ideals]].
This is precisely the underlying poset of the localic [[Zariski spectrum]].

## Reference

* [[Yves Diers]], _Some spectra relative to functors_.  Journal of Pure and Applied Algebra 22:1 (1981), 57–74.  [doi][1]

    [1]: https://doi.org/10.1016/0022-4049(81)90082-7
