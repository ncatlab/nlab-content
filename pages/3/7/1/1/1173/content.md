A **meet-semilattice** is a [[poset]] which admits all [[finite set|finite]] [[meet|meets]], or equivalently which admits a top element $\top$ and binary meets $a\wedge b$.

In a meet-semilattice the binary meet $\wedge$ is commutative, associative, has $\top$ as a unit, and is *idempotent*: $a\wedge a =a$.  And in fact, given any commutative and idempotent [[monoid]] $(A,\wedge,\top)$, we can define $a\le b$ to mean $a \wedge b = a$ to make it into a poset with finite meets; thus we have an equivalent algebraic definition of a meet-semilattice.

Dually, a **join-semilattice** is a poset which admits all finite joins, including a bottom element $\bot$ and binary joins $\vee$.  Once again $\vee$ is commutative, associative, unital for $\bot$, and idempotent, and we can recover the order from it.

Note that the algebraic definition of both types of semilattice is the same: a commutative idempotent monoid.  The difference comes in how we define the order, or if we work purely algebraically, in the notation we use (just as we distinguish additive and multiplicative groups notationally).  It would also be possible to take one as standard and call the other a _cosemilattice_ (compare [[direction|directed]] and [[codirection|codirected]] sets), but this may not have ever been done.

If a poset is both a meet- *and* a join-semilattice, then we call it a [[lattice]].


## Bounded semilattices and semipseudolattices

Traditionally, a semilattice need have only finite [[inhabited set|inhabited]] meets/joins; that is, it need not have a top/bottom element.  Algebraically, this means that a semilattice need not be a monoid, but is any commutative idempotent [[semigroup]].

One might call a semilattice that does have a top/bottom element a __bounded semilattice__; the problem with this is that a [[bounded poset]] already means a poset that has both top *and* bottom elements, whereas here we really only want to require one.

Another approach is to define a semilattice, as above, to require a top/bottom element and then use the term __pseudosemilattice__ or __semipseudolattice__ to allow for the possibility that it might not.

See [[lattice]] for more discussion of this issue.


## Semilattice homomorphisms

A semilattice homomorphism $f$ from a semilattice $A$ to a semilattice $B$ is a [[function]] from $A$ to $B$ (seen as sets) that preserves $\vee$ (and $\bot$, if this is required):
$$ f(x \vee y) = f(x) \vee f(y),\; f(\bot) = \bot .$$
Note that such a homomorphism is necessarily a [[monotone function]], but the converse fails.

Thus, a semilattice is a poset with [[property-like structure]].


[[!redirects meet-semilattice]]
[[!redirects join-semilattice]]
[[!redirects meet semilattice]]
[[!redirects join semilattice]]
[[!redirects cosemilattice]]
[[!redirects bounded semilattice]]
[[!redirects pseudosemilattice]]
[[!redirects semipseudolattice]]
[[!redirects semilattices]]
[[!redirects meet-semilattices]]
[[!redirects join-semilattices]]
[[!redirects meet semilattices]]
[[!redirects join semilattices]]
[[!redirects cosemilattices]]
[[!redirects bounded semilattices]]
[[!redirects pseudosemilattices]]
[[!redirects semipseudolattices]]