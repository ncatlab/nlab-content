If $x$ and $y$ are elements of a [[partial order|poset]], then their **join**, or **supremum**, is an element $x \vee y$ of the poset such that:
* $x \leq x \vee y$ and $y \leq x \vee y$;
* if $x \leq a$ and $y \leq a$, then $x \vee y \leq a$.
Such a join may not exist; if it does, then it is unique.

In a [[preorder|proset]], a join may be defined similarly, but it need not be unique.  (However, it is still unique up the natural [[equivalence]] in the proset.)

The above definition is for the join of two elements of a poset, but it can easily be generalised to any number of elements.  It may be more common to use 'join' for a join of finitely many elements and 'supremum' for a join of (possibly) infinitely many elements, but they are the same concept.  The join may also be called the **maximum** if it equals one of the original elements.

Special cases:  A join of zero elements is a [[bottom]] element.  Any element $a$ is a join of that one element.

A poset that has all finite joins is a **join-[[semilattice]]**.  A poset that has all suprema is a **[[complete lattice|complete]] join-semilattice**.

As a poset is a special kind of [[category]], a join is simply a [[coproduct]] in that category.

A join of [[subset]]s or [[subobject]]s is called a [[union]].