> This article is about maps of [[topological spaces]].  For morphisms of [[schemes]], see [[quasiseparated morphism]] and [[separated morphism of schemes]].  For morphisms of [[toposes]], see [[separated geometric morphisms]].

## Idea

A family version of the notion of a [[Hausdorff space]].

## Definition

A [[continuous map]] $f\colon X\to Y$ of [[topological spaces]] is __separated__ if the relative diagonal
$$\Delta\colon X\to X\times_Y X$$
is a [[closed map]].

Equivalent formulations:

* The image of the relative diagonal map is a closed subset of $X\times_Y X$.

* Two distinct points of $X$ mapping to the same point of $Y$ have disjoint [[neighborhoods]] in $X$.

## Properties

Taking $Y$ to be a point, we recover the definition of a [[Hausdorff space]] as a space with a closed diagonal map.

Separated maps are closed under [[base changes]].

The point-set formulation of separated maps implies that every fiber of a separated map is a [[Hausdorff space]].  The converse is false, since disjoint neighborhoods in a fiber need not come from disjoint neighborhoods in $X$.

## Related concepts

* [[quasiseparated morphism]], [[separated morphism of schemes]], [[separated geometric morphisms]]

## References

* [[Stacks Project]], Tag 0CY0, <https://stacks.math.columbia.edu/tag/0CY0>.

[[!redirects separated maps]]
[[!redirects separated]]