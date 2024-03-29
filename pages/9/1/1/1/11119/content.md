## Idea

A _symmetric endofunctor_ is an [[endofunctor]] together with [[actions]] of the [[symmetric groups]] on its [[automorphism groups]].

## Definition

Let $\Phi$ be a [[graded monoid]] in the [[category]] of [[groups]], e.g. the [[graded monoid]] $\Sigma = (\Sigma_n)_{n \ge 0}$ of [[symmetric groups]].

A **symmetric endofunctor** $F : C \to C$ is an [[endofunctor]] together with the data of, for each $n \in \mathbf{N}$, a [[group homomorphism]]
  $$ \Phi_n \to \Aut(F^{\circ n}) $$
where $F^{\circ n}$ is the $n$-fold [[composite]] of $F$.