A __rig__, or __semiring__, is a [[ring]] 'without negatives' (hence the missing 'n' in the name, get it?).

Specifically, it a [[set]] $R$ with operations of addition and multiplication, such that
*  $R$ is a [[monoid]] under multiplication;
*  $R$ is an [[abelian monoid]] under addition;
*  multiplication distributes over addition.

As with rings, one sometimes considers non-associative or non-unital versions (where multiplication may not be associative or may have no identity).  It is rarer to remove requirements from addition.  But notice that while $R$ can be proved (from the other axioms) to be an [[abelian group]] under addition (and therefore a ring) as long as it is a [[group]], this argument does not go through if it is only a monoid.

Most examples of rigs are either [[ring]]s or [[distributive lattice]]s.  Indeed, a ring is precisely a rig that forms a group under addition, while a distributive lattice is precisely a commutative rig in which the operations are idempotent.  Note that a [[Boolean algebra]] is a rig in both ways: as a lattice and as a [[Boolean ring]].

Just as a ring is a [[monoid object]] in the category [[Ab]] of abelian groups, so a rig is a monoid object in the category of abelian monoids.