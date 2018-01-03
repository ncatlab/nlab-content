# T-norms

* table of contents
{: toc}

## Definition

A **t-norm** is a [[semicartesian monoidal category|semicartesian]] [[symmetric monoidal category|commutative]] [[monoidal category|monoidal]] structure on the [[unit interval]] $[0,1]$ as a [[poset]].

That means it is a [[commutative monoid]] structure on the set $[0,1]$ that is order-preserving in each argument and with $1$ as the unit element.

## Related concepts

T-norms are used in [[fuzzy logic]].

## Examples

* $T(x,y) = \min(x,y)$.  This is the [[cartesian monoidal category|cartesian]] monoidal structure, also known as the *minimum t-norm* or the *Godel t-norm*.
* $T(x,y) = x y$, the *product t-norm*.
* $T(x,y) = \max(x+y-1,0)$, the *Lukasiewicz t-norm* (see [[Lukasiewicz logic]]).  This monoidal structure is moreover [[star-autonomous category|star-autonomous]] with the obvious involution $x^\ast = 1-x$.

[[!redirects t-norms]]
