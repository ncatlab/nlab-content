[[!redirects homotopy coproducts]]
## Idea

__Homotopy coproducts__ are a special case of [[homotopy colimits]],
when the indexing diagram is a [[discrete category]].

Homotopy coproducts can be defined in any [[relative category]],
just like [[homotopy colimits]],
but practical computations are typically carried out
in presence of additional structures such as [[model structures]].

## Computation

In any [[model category]], the homotopy coproduct
of a family of objects $\{A_i\}_{i\in I}$
can be computed by [[cofibrantly replacing]] each $A_i$
and computing the (ordinary) [[coproduct]]
of the resulting family $\{QA_i\}_{i\in I}$ of [[cofibrant replacements]].

If [[weak equivalences]] are closed under small [[coproducts]],
then homotopy coproducts can be computed as ordinary coproducts,
because the map $$\coprod_{i\in I}QA_i\to \coprod_{i\in I}A_i$$
is a [[weak equivalence]].

## Examples

In [[simplicial sets]] with [[simplicial weak equivalences]],
[[topological spaces]] with [[weak homotopy equivalences]],
and [[chain complexes]] with [[quasi-isomorphisms]],
homotopy coproducts can be computed as ordinary coproducts
because [[weak equivalences]] are closed under small [[coproducts]]..

In [[commutative differential graded algebras]] with [[quasi-isomorphisms]] homotopy coproducts
can be computed by resolving each object by a [[cofibrant commutative differential graded algebra]], and then computing their ordinary [[tensor product]].

## Related notions

* [[coproduct]]

* [[homotopy colimit]]

* [[homotopy pushout]]

* [[homotopy coequalizer]]

* [[homotopy realization]]

[[!redirects homotopy coproducts]]