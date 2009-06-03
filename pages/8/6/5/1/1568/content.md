Ideals show up both in [[ring]] theory and in [[lattice]] theory.  Actually, both of these can be slightly generalised:

## In rings and other rigs

A __left ideal__ in a [[ring]] (or even [[rig]]) $R$ is a [[subset]] $I$ of (the underlying set of) $R$ such that:
*  $0 \in I$;
*  $x + y \in I$ whenever $x, y \in I$;
*  $x y \in I$ whenever $y \in I$, regardless of whether $x \in I$.

A __right ideal__ in $R$ is a subset $I$ such that:
*  $0 \in I$;
*  $x + y \in I$ whenever $x, y \in I$;
*  $x y \in I$ whenever $x \in I$.

A __two-sided ideal__ in $R$ is a subset $I$ that is both a left and right ideal; that is:
*  $0 \in I$;
*  $x + y \in I$ whenever $x \in I$ and $y \in I$;
*  $x y \in I$ whenever $x \in I$ or $y \in I$.

This generalises to:
*  $x_1 + \cdots + x_n \in I$ whenever $x_k \in I$ for every $k$;
*  $x_1 \cdots x_n \in I$ whenever $x_k \in I$ for some $k$.

Notice that all three kinds of ideal are equivalent for a commutative ring.

## In lattices and other prosets

An __ideal__ in a [[lattice]] (or even [[preorder|proset]]) $L$ is a [[subset]] $I$ of (the underlying set of) $L$ such that:
*  There is an element of $I$ (so that $I$ is [[inhabited set|inhabited]]);
*  if $x, y \in I$, then $x, y \leq z$ for some $z \in I$;
*  if $x \in I$ and $y \leq x$, then $y \in I$ too.

We can make this look more algebraic if $L$ is a (bounded) join-[[semilattice]]:
*  $\bot \in I$;
*  $x \vee y \in I$ if $x, y \in I$;
*  $y \in I$ whenever $x \vee y \in I$.

If $L$ is indeed a lattice, then we can make this look just like the ring version:
*  $\bot \in I$;
*  $x \vee y \in I$ whenever $x, y \in I$;
*  $x \wedge y \in I$ whenever $x \in I$.

The concept of ideal is dual to that of [[filter]].  A subset of $L$ that satisfies the first two of the three axioms for an ideal in a proset is precisely a [[direction|directed subset]] of $L$; notice that this is weaker than being a sub-join-semilattice even if $L$ is a lattice.

## In both at once

A [[distributive lattice]] is both a lattice and a commutative rig; the two concepts of ideal are the same, as can be seen by comparing the definition for rigs to the last definition for lattices.

A [[Boolean algebra]] is a rig in two different ways: as a distributive lattice and as a [[Boolean ring]].  Fortunately, these actually give the same concept of ideal.

## Kinds of ideals

An ideal $I$ is __proper__ if there exists an element $x$ such that $x \notin I$.  In a rig, $I$ is proper iff $1 \notin I$; in a lattice, $I$ is proper iff $\top \notin I$.

An ideal $I$ is __prime__ if it is proper and it satsfies a binary condition corresponding to the nullary condition that is properness:
*  In a rig, $x \in I$ or $y \in I$ if $x y \in I$;
*  In a proset, $x \in I$ or $y \in I$ if, for all $z$, $z \in I$ if $z \leq x$ or $z \leq y$.
*  In a lattice (simplifying the proset version to look like the rig verison), $x \in I$ or $y \in I$ if $x \wedge y \in I$.

An ideal is __maximal__ if it is maximal among proper ideals; note that a maximal ideal is necessarily proper.