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
can be computed by [[cofibrant replacement|cofibrantly replacing]] each $A_i$
and computing the (ordinary) [[coproduct]]
of the resulting family $\{QA_i\}_{i\in I}$ of [[cofibrant replacements]].

If [[weak equivalences]] are closed under small [[coproducts]],
then homotopy coproducts can be computed as ordinary coproducts,
because the map $\coprod_{i\in I}QA_i\to \coprod_{i\in I}A_i$ is a [[weak equivalence]].

In general, [[cofibrant replacement]] cannot be avoided, even in the case of a [[proper model category]].  For example, the model structure on [[simplicial commutative rings]] transferred along the forgetful functor to [[simplicial sets]] is proper, but the canonical map
$$Q A \sqcup Q B \to A \sqcup B$$
from the homotopy coproduct to the coproduct is not a weak equivalence if $A=B=\mathbf{Z}/2$, since the left side computes $Tor(A,B)$, which has nontrivial higher homotopy groups.

## Examples

In [[simplicial sets]] with [[simplicial weak equivalences]],
[[topological spaces]] with [[weak homotopy equivalences]],
and [[chain complexes]] with [[quasi-isomorphisms]],
homotopy coproducts can be computed as ordinary coproducts
because [[weak equivalences]] are closed under small [[coproducts]].

In [[commutative differential graded algebras]] with [[quasi-isomorphisms]] homotopy coproducts
can be computed by resolving each object by a [[cofibrant commutative differential graded algebra]], and then computing their ordinary [[tensor product]].

## Related notions

* [[coproduct]]

* [[homotopy colimit]]

* [[homotopy pushout]]

* [[homotopy coequalizer]]

* [[homotopy realization]]

[[!redirects homotopy coproducts]]