## Idea

A weak inverse is like an inverse, but weakened to work in situations where being an inverse on the nose would be [[evil]].


## Definitions

Given a [[functor]] $F: C \to D$, a __weak inverse__ of $F$ is a functor $G: D \to C$ with [[natural isomorphism]]s
$$ \iota: id_C \to G \circ F,\; \epsilon: F \circ G \to id_D .$$

If it exists, a weak inverse is unique up to natural isomorphism, and furthermore can be improved to form an [[adjoint equivalence]], where $\iota$ and $\epsilon$ sastisfy the [[triangle identities]].

More generally, given a $2$-[[2-category|category]] $\mathcal{B}$ and a morphisms $F: C \to D$ in $\mathcal{B}$, a __weak inverse__ of $F$ is a morphism $G: D \to C$ with $2$-isomorphisms
$$ \iota: id_C \to G \circ F,\; \epsilon: F \circ G \to id_D .$$

Weak inverses give the proper notion of [[equivalence of categories]] and [[equivalence]] in a $2$-category.