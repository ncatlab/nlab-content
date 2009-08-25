An __affine space__ is a [[vector space]] that has forgotten its origin.

This can be understood in various ways:
*  An affine space is simply a vector space, but we accept as [[morphisms]] of affine spaces any function which is the difference between a linear map (a morphism of vector spaces) and a [[constant function]].
*  An affine space is a [[set]] equipped with an equivalence class of vector space structures, where two vector space structures are considered equivalent if the [[identity function]] is the difference between a linear map and a constant function.
*  An affine space is a set $A$ together with a vector space $V$ and an [[action]] of (the additive group of) $V$ on $A$ that makes $A$ into a $V$-[[torsor]]. For this point of view, see also [[zoranskoda:affine space]].
*  An affine space is a set $A$ together with a vector space $V$ and a function $A \times A \to V$ (thought of as subtraction) that satisfies some equations.
* An affine space is a [[heap]] whose automorphism group is the additive group of a vector space. Slightly rephrased and repacked, an affine space over a field $k$ is an [[inhabited set]] $A$ together with functions $A \times A \times A \to A$ (thought of as $x,y,z \mapsto x - y + z$) and $k \times A \times A \to A$ (thought of as $r,x,y \mapsto r x - r y + y$) that satsify some equations.

+--{: .query}
[[Mike Shulman]]: That last definition can't be right, since it doesn't mention the [[base field]].  Did you mean $k\times A\times A\to A$ taking $(r,x,y)$ to "$r x + (1-r) y$"?

_Toby_:  Whoops, sorry, the function $A \times A \times A \to A$ only gives the affine $\mathbb{Z}$-module structure.  We do need both, however, analogously to needing both addition and scalar multiplication for a vector space.  (Although, just as the addition in a topological vector space may be recovered from the scalar multiplication by continuity, so we only need your function for a topological affine space.)  It also occurs to me that my function is a peculiarly weighted average, so I changed its explanation.

[[Mike Shulman]]: Are you sure we need both?  Seems to me that
$$ x - y + z = 2 (\frac{1}{2} x + \frac{1}{2} z) + (-1)y $$
means you can recover the first from the second (at least, if $k$ has characteristic $\neq 2$).
=--

Sometimes one allows the [[empty set]] to be an affine space (of dimension $-1$).  This is most natural using the last definition; it amounts to simply removing the requirement that $A$ be inhabited and allows affine spaces to be given by a [[variety of algebras]].
