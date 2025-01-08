[[!redirects modules over C^∞-rings]]
## Beck modules

The category of [[Beck modules]] over a [[C^∞-ring]] $A$ is equivalent to the category of ordinary [[modules]] over the underlying real [[algebra]] of $A$.

This is established using the proof given at [[Beck module]] for ordinary rings, using the fact that [[ideals]] of [[C^∞-rings]] coincide with ideals in the ordinary sense and the [[square zero extension]] construction used there can be promoted to a [[C^∞-ring]] using [[Taylor expansions]].

Furthermore, the resulting notion of a [[Beck derivation]] coincides with that of a [[C^∞-derivation]].

## Kainz–Kriegl–Michor modules

A different, nonequivalent definition was proposed by Kainz–Kriegl–Michor in 1987.

Suppose $k$ is a [[commutative ring]].
Denote by $Poly_k$ the following [[category]].
Objects are $k$-modules.
Morphisms $M\to N$ are polynomial maps $M\to N$, i.e., elements of $Sym M^*\otimes_k N$.

A [[commutative algebra]] $A$ can be identified with a product-preserving functor $FinPoly_k\to Set$, where $FinPoly_k$ is the full subcategory of $Poly_k$ on finitely generated free modules.
The value $A(X)$ for $X\in FinPoly_k$ can be thought of as the space of [[regular functions]] $Spec A\to X$, where $Spec A$ is the [[Zariski spectrum]] of $A$.

The starting observation is that a [[module]] $M$ over a  commutative $k$-algebra $A$ can be identified with a [[dinatural transformation]] (dinatural in $X\in CartPoly$)
$$\eta\colon Poly_k(X,M)\times A(X)\to M.$$
We require $\eta$ to be linear in the first argument.

That is to say, to specify an $A$-module $M$, we have to single out polynomial maps $k^n\to M$, together with a way to compose a polynomial map $k^n\to M$ with a [[regular function]] $Spec A\to k^n$, obtaining a regular map $Spec A\to M$.  Interpreting $M$ as the module of sections of a [[quasicoherent sheaf]] over $Spec A$, a regular map $Spec A\to M$ can be restricted to the diagonal $Spec A$, obtaining an element of $M$ as required.

The proposal of Kainz–Kriegl–Michor is then to replace polynomial maps with [[smooth maps]]:

A __C^∞-module__ over a [[C^∞-ring]] $A$ is a Hausdorff [[locally convex topological vector space]] $M$ together with a [[dinatural transformation]]
$$\eta\colon C^\infty(X,M)\times A(X)\to M$$
that is linear in the first argument.
If $\eta$ is also continuous in the first argument, we say that $M$ is a __continuous C^∞-module__.

Topological vector spaces in the above definition can be replaced by any notion of a vector space that allows for smooth maps, e.g., [[convenient vector space]] etc.

## Related concepts

* [[Beck module]], [[Beck derivation]]

## References

* G. Kainz, A. Kriegl, P. Michor, _$C^\infty$-algebras from the functional analytic view point_, Journal of Pure and Applied Algebra 46:1 (1987), 89-107.  [doi][KKM]

[KKM]: https://doi.org/10.1016/0022-4049(87)90045-4

