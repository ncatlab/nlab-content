
__$Quiv$__ or __$DiGraph$__ is the category of [[quivers]] or (as category theorists often call them) [[directed graph]].

We can define a quiver to be a functor $G\colon X^{op} \to Set$, where $X^{op}$ is the [[category]] with an [[object]] $0$, an object $1$ and two [[morphisms]] $s, t\colon 1 \to 0$, along with [[identity morphisms]].  This lets us efficiently define $Quiv$ as the category of [[presheaves]] on $X$, where:

* objects are [[functors]] $G\colon X^{op} \to C$,
* morphisms are [[natural transformations]] between such functors.

In other words, $Quiv$ is the [[functor category]] from this $X^{op}$ to [[Set]].


category: category

[[!redirects Quiv]]
[[!redirects DiGraph]]
[[!redirects Digraph]]
