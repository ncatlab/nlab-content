
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **hypergroup** is a [[algebra|algebraic]] structure similar to a [[group]], but where the composition operation does not just take two elements to a single product element in the group, but to a subset of elements of the group.

It is a [[hypermonoid]] with additional groupal [[stuff, structure, property|structure and property]].

## Definition

A **canonical hypergroup** is a [[set]], $H$, equipped with a commutative binary operation, 

$$
  + : H \times H \to P^*(H)
$$ 

taking values in [[non-empty subsets]] of $H$, and a zero element $0 \in H$, such that

1. $+$ is associative (extended to allow addition of subsets of $H$);
2. $0 + x = {\{x\}} = x + 0, \forall x \in H$;
3. $\forall x \in H, \exists ! y \in H$ such that $0 \in x + y$ (we denote this $y$ as $-x$);
4. $\forall x, y, z \in H, x \in y + z$ implies $z \in x - y$ (where $x - y$ means $x + (-y)$ as usual).


## Examples

The additive structure underlying a [[hyperring]] is a canonical hypergroup. See there for more examples.


[[!redirects hypergroup]]
[[!redirects hypergroups]]

category: algebra

[[!redirects canonical hypergroups]]