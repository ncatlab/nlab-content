\tableofcontents

## Idea

A [[Mahlo cardinal]] is a [[large cardinal]] in [[set theory]] needed to make the set theory equivalent to a [[type theory]], like [[Agda]], with [[type universes]] with [[inductive-recursive types]] inside of the universe. 

## Definition

The [[ordinal]] $\kappa$ is Mahlo iff for any function $F : \kappa \to \kappa$, there is an [[inaccessible cardinal]] $\lambda$ such that $\lambda \lt \kappa$ and $\lambda$ is closed under $F$.

We can phrase this more structurally as follows: $\kappa$ is Mahlo iff for any functor $F : Core(Set_{\lt\kappa}) \to Core(Set_{\lt\kappa})$ on the category of sets strictly smaller than $\kappa$ and bijections, there is a [[universe]] $U$ with $|U| \lt \kappa$ which is closed under $F$.

## See also

* [[large cardinal]]

## External links

* Wikipedia, [Mahlo cardinal](https://en.wikipedia.org/wiki/Mahlo_cardinal)