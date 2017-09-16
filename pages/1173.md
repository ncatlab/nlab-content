A **meet-semilattice** is a [[poset]] which admits all [[finite set|finite]] [[meet|meets]], or equivalently which admits a top element $\top$ and binary meets $a\wedge b$.

In a meet-semilattice the binary meet $\wedge$ is commutative, associative, has $\top$ as a unit, and is *idempotent*: $a\wedge a =a$.  And in fact, given any commutative and idempotent [[monoid]] $(A,\wedge,\top)$, we can define $a\le b$ to mean $a \wedge b = a$ to make it into a poset with finite meets; thus we have an equivalent algebraic definition of a meet-semilattice.

Dually, a **join-semilattice** is a poset which admits all finite joins, including a bottom element $\bot$ and binary joins $\vee$.  Once again $\vee$ is commutative, associative, unital for $\bot$, and idempotent, and we can recover the order from it.

Note that the algebraic definition of both types of semilattice is the same: a commutative idempotent monoid.  The difference comes in how we define the order, or if we work purely algebraically, in the notation we use (just as we distinguish additive and multiplicative groups notationally).