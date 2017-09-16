An __affine space__ is a [[vector space]] that has forgotten its origin.

This can be understood in various ways:
*  An affine space is simply a vector space, but we accept as [[morphisms]] of affine spaces any function which is the difference between a linear map (a morphism of vector spaces) and a [[constant function]].
*  An affine space is a [[set]] equipped with an equivalence class of vector space structures, where two vector space structures are considered equivalent if the [[identity function]] is the difference between a linear map and a constant function.
*  An affine space is a set $A$ together with a vector space $V$ and an [[action]] of (the additive group of) $V$ on $A$ that makes $A$ into a $V$-[[torsor]].
*  An affine space is a set $A$ together with a vector space $V$ and a function $A \times A \to V$ (thought of as subtraction) that satisfies some equations.
*  An affine space is an [[inhabited set]] $A$ together with a function $A \times A \times A \to A$ (thought of as averaging) that satsifies some equations.

+--{: .query}
[[Mike Shulman]]: That last definition can't be right, since it doesn't mention the [[base field]].  Did you mean $k\times A\times A\to A$ taking $(r,x,y)$ to "$r x + (1-r) y$"?
=--

Sometimes one allows the [[empty set]] to be an affine space (of dimension $-1$).  This is most natural using the last definition; it amounts to simply removing the requirement that $A$ be inhabited and allows affine spaces to be given by a [[variety of algebras]].