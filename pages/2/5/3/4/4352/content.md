
#Cotents#
* automatic table of cotents goes here
{:toc}

## Idea

A **hypergroup** is a [[algebra|algebraic]] structure similar to a [[group]], but where the composition operation does ot just take two elements to a single product element in the group, but to a subset of elements of the group.

## Definition

A **canonical hypergroup** is a [[set]], $H$, equipped with a commutative binary operation, 

$$
  + : H \times H \to P^*(H)
$$ 

taking values in non-empty subsets of $H$, and a zero element $0 \in H$, such that

1. $+$ is associative (extended to allow addition of subsets of $H$);
1. $0 + x = x = x + 0, \forall x \in H$;
1. $\forall x \in H \exists ! y (= - x) \in H$ such that $0 \in x + y$;
1. $\forall x, y, z \in H, x \in y + z$ implies $z \in x - y$.

## Examples

The additive structure underlyig a [[hyperring]] is a canonical hypergroup. See there for more examples.