## Idea

A premodel category is a relaxation of the notion of a [[model category]].
[[Combinatorial]] premodel categories form a [[2-category]]
that has all (small) [[limits]] and [[colimits]]
and has representing objects for [[Quillen bifunctors]].

The [[2-category]] of combinatorial $V$-[[enriched]] premodel categories
is the category of modules over a monoid $V$ in this [[2-category]].
It inherits the same set of properties
and additionally admits a [[model 2-category]] structure.
In this model structure, a [[left Quillen functor]] is a [[weak equivalence]]
if and only if it is a [[Quillen equivalence]].

## Definition

A __premodel category__ is a [[bicomplete category]]
equipped with a pair of [[weak factorization systems]]
$(C,AF)$ and $(AC,F)$ such that $AC\subset C$ (equivalently, $AF\subset F$).

[[Model categories]] can be singled out of premodel categories
by imposing the additional requirement that the class
$W$ obtained by composing an element of $AC$ followed by an element of $AF$,
is closed under the [[2-out-of-3 property]].

## References

[[Reid William Barton]], _A model 2-category of enriched combinatorial premodel categories_, [arXiv:2004.12937](https://arxiv.org/abs/2004.12937).