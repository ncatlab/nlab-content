[[!redirects commutative monoidal categories]]
[[!redirects commutative monoidal categories]]
[[!redirects commutative monoidal categories]]
[[!redirects commutative monoidal categories]]
## Idea

Commutative monoidal categories are [[symmetric monoidal categories]] whose whose monoidal product is strictly [[associative]], [[unital]], and commutative. Furthermore, the associators, unitors, and symmetries are given by the identity (although this is not necessary for categories of this sort). Commutative monoidal categories are normally seen as going too far as the [[coherence theorem for symmetric monoidal categories]] says that symmetric monoidal categories are symmetric monoidally equivalent to [[monoidal categories|strict monoidal categories]] whose symmetries may not be given by the identity. Nevertheless, commutative monoidal categories are the natural type of category that [[Petri nets]] freely generate.

## Definition

A commutative monoidal category is a [[commutative monoid]] object in [[Cat]]  with [[cartesian product]].  Explicitly, the data of a commutative monoidal category is:
* A commutative monoid of objects $C_1$,

* a commutative monoid of morphisms $C_0$,

* source and target [[monoid homomorphisms]] $s,t \colon C_1 \to C_0$,

* an identity assigning monoid homomorphism $i \colon C_0 \to C_1$ and,

* a homomorphism $\circ \colon C_1 \times_C_0 C_1 \to C_1$ representing composition.

These homorphisms are required to satisfy the axioms of a [[category]]. In particular, because composition is a commutative monoid homomorphism, it satisfies the [[interchange law]]

$$ (g \circ f) + (h \circ k) = (g + h) \circ (f + k) $$

whenever all composites are defined.

[[!redirects commutative monoidal categories]]
[[!redirects Commutative monoidal categories]]