
## Idea

Given a semigroup, we'd like to identify it with the semigroup of its left/right translations. Those are the left/right weakly reductive semigroups. 

## Definition

We only define left weakly reductive semigroups, right weakly reductive semigroups are defined similarly.

Let $S_l$ be the set of left translations of $S$. That is, this is the set of maps $x_l:S\to S$ defined by $x_l(y) := x\cdot y$. The semigroup $(S_l, \circ)$, where $\circ$ denotes composition of maps, is called the semigroup of left translations of $S$.

The map $f:x\mapsto x_l$ is then a morphism in the category of semigroups. We call $(S, \cdot)$ _left weakly reductive_, if $f$ is an isomorphism.

Explicitly, and this is where the name comes from, if $a, b\in S$, and $x\cdot a = x\cdot b$ for all $x\in S$, then $a = b$.

A _weakly reductive semigroup_ is a semigroup that is both right and left weakly reductive.



## In terms of varieties

A left weakly reductive semigroup can be thought of as a class of structures $(S, \cdot , w, r)$, where $\cdot, w$ are binary operations, and $r$ is a ternary operation, satisfying the following axioms for all $x, y, z$: $ x\cdot (y\cdot z) = (x\cdot y)\cdot z, r(x, y, w(x, y)\cdot x) = x, r(x, y, w(x, y)\cdot y) = y $.

## Examples

Any _left monoid_, a semigroup with a left identity element, is a left weakly reductive semigroup. In particular, any monoid is weakly reductive.

Any left weakly reductive commutative semigroup is weakly reductive.

A monogenic semigroup that isn't a group is not weakly reductive.

There exists unique smallest left weakly reductive semigroup which isn't a left monoid. It can be defined as the idempotent semigroup $(\{x, y, z\}, \cdot)$ such that $a\cdot b = z$ for $a\neq b$.

## References

* A. H. Preston and G. B. Clifford, _The algebraic theory of semigroups: Volume I_, American Mathematical Society (1961)


