## Definition

An __ordered real vector space__ is a real [[vector space]] that has a compatible [[poset]] structure: if $x\le y$, then also $x+a\le y+a$ for all $a$ and $t x\le t y$ for all real $t\ge0$.

A __Riesz space__ is an ordered real vector space whose underlying [[poset]] is a [[lattice]].

A __morphism of Riesz spaces__ is a linear map that preserves finite [[infima]] and [[suprema]].

A __unital Riesz space__ is a Riesz space equipped with a unit: an element $u$ such that $u\ge0$ and for every $x$ there is an integer $n\ge0$ such that $|x|=\sup(x,-x) \le n u$.

A __morphism of unital Riesz spaces__ is a morphism of Riesz spaces that preserves the unit.

Any unit $u$ induces a [[seminorm]]: $\|x\|_u=\inf\{t\mid t\ge0 \land |x|\le t u\}$.

An _Archimedean Riesz space__ is a Riesz space such that any infinitesimal element $e$ is zero.  Here $e$ is __infinitesimal__ if there is $b$ such that $n e\le b$ for all integer $n$.

The seminorm induced by a unit on an Archimedean Riesz space is a [[norm]].

An Archimedean unital Riesz space is __uniformly complete__ if the norm induced by the unit (any unit, in fact) is [[complete]].

## Related concepts

* [[Yosida duality]]

## References

The original definition is in

* [[Frigyes Riesz]], _Sur la décomposition des opérations fonctionelles linéaires_, Atti congress. internaz. mathematici (Bologna, 1928), 3, Zanichelli (1930), 143–148.

[[!redirects Riesz spaces]]
[[!redirects vector lattice]]
[[!redirects vector lattices]]
[[!redirects lattice-ordered vector space]]
[[!redirects lattice-ordered vector spaces]]