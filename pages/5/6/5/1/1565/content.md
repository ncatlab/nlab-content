[[!redirects semiring]]
[[!redirects rigs]]
[[!redirects semirings]]


A __rig__ is a [[ring]] 'without negatives' (hence the missing 'n' in the name, get it?).  Similarly, a __semiring__ has neither negatives nor even zero.

Specifically, it a [[set]] $R$ with operations of addition and multiplication, such that
*  $R$ is a [[monoid]] under multiplication;
*  $R$ is an [[abelian monoid]] (for a rig) or an abelian semigroup (for a semiring) under addition;
*  multiplication distributes over addition.

More sophisticatedly, we can say that, just as a ring is a [[monoid object]] in [[abelian group]]s, so a rig is a monoid object in abelian monoids and a semiring is a monoid object in abelian semigroups.

As with rings, one sometimes considers non-associative or non-unital versions (where multiplication may not be associative or may have no identity).  It is rarer to remove requirements from addition as we have done here.  But notice that while $R$ can be proved (from the other axioms) to be an [[abelian group]] under addition (and therefore a ring) as long as it is a [[group]], this argument does not go through if it is only a monoid.

Many rigs are either [[ring]]s or [[distributive lattice]]s.  Indeed, a ring is precisely a rig that forms a group under addition, while a distributive lattice is precisely a commutative rig in which the operations are idempotent.  Note that a [[Boolean algebra]] is a rig in both ways: as a lattice and as a [[Boolean ring]].

Some rigs which are neither rings nor distributive lattices include:

* The [[natural numbers]].
* The nonnegative [[rational number]]s and the nonnegative [[real numbers]].
* Polynomials with coefficients in any rig.
* The set of isomorphism classes of objects in any [[distributive category]], or more generally in any [[rig category]].
* The [[tropical rig]], which is $\mathbb{R}\cup \{\infty\}$ with addition $x\oplus y = min(x,y)$  and multiplication $x\otimes y = x+y$.

Any rig can be completed to a ring by adding negatives, in the same way that the natural numbers are completed to the integers.  When applied to the set of isomorphism classes of objects in a rig category, the result is part of [[algebraic K-theory]].


[[!redirects semiring]]