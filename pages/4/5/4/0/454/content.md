A **lattice** is a [[poset]] which admits all finite [[meet]]s and finite [[join]]s (or all finite products and finite coproducts, regarding a poset as a category).

A **lattice** can also be defined as an algebraic structure, with the binary operations $\wedge$ and $\vee$ and the consants $\top$ and $\bot$. (These correspond, respectively, to binary and nullary meets and joins in the poset-theoretic definition; accordingly, they are read 'meet', 'join', 'top', and 'bottom'.) Here are the axioms for these operations:
* $\wedge$ and $\vee$ are each idempotent, commutative, and associative, with respective identities $\top$ and $\bot$;
* the _absorption laws_: $a \vee (a \wedge b) = a$, and $a \wedge (a \vee b) = a$.

You can recover the original poset from either the meet or the join; $a \leq b$ iff $a \wedge b = a$, and $a \geq b$ iff $a \vee b = a$. The absorption laws guarantee that these agree.

Sometimes the requirement that a lattice have top and bottom (nullary meets and joins) is removed; then a lattice with these is called a **bounded lattice**.

A **meet-semilattice** is a poset which admits all finite meets; a **join-semilattice** is a poset which admits all finite joins. The algebraic definition of **semilattice** is the same either way, but you can still distinguish meet- and join- semilattices for their notation (much as you do additive and multiplicative groups).