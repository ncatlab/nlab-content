# Definition

A **lattice** is a [[partial order|poset]] which admits all finite [[meet]]s and finite [[join]]s (or all finite products and finite coproducts, regarding a poset as a category).

A **lattice** can also be defined as an algebraic structure, with the binary operations $\wedge$ and $\vee$ and the consants $\top$ and $\bot$. (These correspond, respectively, to binary and nullary meets and joins in the poset-theoretic definition; accordingly, they are read 'meet', 'join', 'top', and 'bottom'.) Here are the axioms for these operations:
* $\wedge$ and $\vee$ are each idempotent, commutative, and associative, with respective identities $\top$ and $\bot$;
* the _absorption laws_: $a \vee (a \wedge b) = a$, and $a \wedge (a \vee b) = a$.

You can recover the original poset from either the meet or the join; $a \leq b$ iff $a \wedge b = a$, and $a \geq b$ iff $a \vee b = a$. The absorption laws guarantee that these agree.

# Variations

Sometimes the requirement that a lattice have top and bottom (nullary meets and joins) is removed; then a lattice with these is called a **bounded lattice**.

A poset with only finite meets _or_ finite joins is a (meet- or join-) [[semilattice]].

A lattice which has *all* joins and meets (not just finitary ones) is a [[complete lattice]].
