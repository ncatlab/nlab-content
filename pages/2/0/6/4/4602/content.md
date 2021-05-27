[[!redirects epic sink]]
## Definition

Given an [[object]] $X$ in some [[category]], a family $(f_i\colon U_i \to X)_i$ of [[morphisms]] to $X$ is an __epic [[sink]]__, or a __jointly epic family__ if, given any two morphisms $g, h\colon X \to Y$ such that $ g \circ f_i= h\circ f_i$ for all $i$, it follows that $g = h$.

Dually, a family $(f_i\colon X \to U_i)_i$ of morphisms from $X$ is a __monic source__, or a __jointly monic family__ if, given any two morphisms $g, h\colon Y \to X$ such that $f_i \circ g = f_i \circ h$ for all $i$, it follows that $g = h$.

Sometimes we are interested only in [[small families]] of morphisms, but if so then it is best to say so explicitly.

A single morphism $U \to X$ is an [[epimorphism]] if and only it forms an epic sink by itself; conversely, a sink $(f_i\colon U_i \to X)_i$ is epic iff the induced map $\coprod_i U_i \to X$ is an epimorphism, assuming that the [[coproduct]] $\coprod_i U_i$ exists.  (Note, though, that for a large family of morphisms, this coproduct might not exist even if the category has all small coproducts.)  Dual results hold for [[monomorphisms]] and [[products]].

Finally, the [[empty family]] of morphisms with domain $X$ is a monic source iff $X$ is a [[subterminal object]] (and dually).

## Examples

If a functor $F \colon J \to C$ has a colimit $\mathrm{colim}F$, with maps $\iota_i \colon F i \to \mathrm{colim}F$ for $ i \in J$, then the family $(\iota_i)_{i \in J}$ is jointly epic. Similarly, the maps $(\pi_i \colon \mathrm{lim}F \to F i)_{i\in J}$ are jointly monic, when the limit exists.

## Related concepts

* [[cancellative category]]

[[!redirects epic sink]]
[[!redirects epimorphic sink]]
[[!redirects epic family]]
[[!redirects epimorphic family]]
[[!redirects jointly epic sink]]
[[!redirects jointly epimorphic sink]]
[[!redirects jointly epic family]]
[[!redirects jointly epimorphic family]]

[[!redirects monic source]]
[[!redirects monomorphic source]]
[[!redirects monic family]]
[[!redirects monomorphic family]]
[[!redirects jointly monic source]]
[[!redirects jointly monomorphic source]]
[[!redirects jointly monic family]]
[[!redirects jointly monomorphic family]]
