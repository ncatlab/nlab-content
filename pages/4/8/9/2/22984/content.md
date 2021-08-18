
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--
#Contents#
* table of contents
{:toc}

## Idea

A **regular hyperdoctrine**, also called an **elementary existential doctrine**, is a version of a [[first-order hyperdoctrine]] that is appropriate for [[regular logic]].

## Definition

Let $C$ be a [[category]] with [[finite limits]]. A **[[regular logic|regular]] [[hyperdoctrine]]**, or **elementary existential doctrine**, over $C$ is a [[functor]]

$$
  P : C^{op} \to InfSemiLattice
$$

from the [[opposite category]] of $C$ to the category of inf-[[semilattices]], such that for every [[morphism]] $f : A \to B$ in $C$, the functor $P(A) \to P(B)$ has a [[left adjoint]] $\exists_f$ satisfying

1. [[Frobenius reciprocity]];

1. [[Beck-Chevalley condition]].

\begin{remark}
The original definition of Lawvere did not include the last two conditions and allowed the values of the functor to be arbitrary categories with finite products.  Other references sometimes require the adjoints $\exists_f$ to be defined only along projections (corresponding to ordinary [[existential quantification]] in logic) and diagonals (corresponding to [[equality]]); Lawvere showed that in the presence of Frobenius and Beck-Chevalley more general quantifiers can be constructed in terms of these.
\end{remark}

## Related concepts

* [[regular hyperdoctrine]]
* [[first-order hyperdoctrine]]

## References

* [[William Lawvere]], *Equality in hyperdoctrines and comprehension schema as an adjoint functor*

* Davide Trotta, *The existential completion*, 2021, [arxiv](https://arxiv.org/abs/2108.03416)

* Davide Trotta, *An algebraic approach to the completions of elementary doctrines*, 2021, [arxiv](https://arxiv.org/abs/2108.03415)

[[!redirects regular hyperdoctrines]]
[[!redirects elementary existential doctrine]]
[[!redirects elementary existential doctrines]]
[[!redirects elementary doctrine]]
[[!redirects elementary doctrines]]
[[!redirects existential doctrine]]
[[!redirects existential doctrines]]
