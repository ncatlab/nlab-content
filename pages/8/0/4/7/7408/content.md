
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

A _Boolean hyperdoctrine_ $P$ is a [[hyperdoctrine]] for [[lattices]] which are [[Boolean algebras]]

$$
  P \;\colon\; T^{op} \to BooleanAlgebra
  \,.
$$

## Definition

Let $C$ be a [[category]] with [[finite limits]]. A **[[classical logic|Boolean]] [[hyperdoctrine]]** over $C$ is a [[functor]]

$$
  P \;\colon\; C^{op} \to BoolAlg
$$

from the [[opposite category]] of $C$ to the category of [[Boolean algebras]], such that for every [[morphism]] $f : A \to B$ in $C$, the functor $P(A) \to P(B)$ has a [[left adjoint]] $\exists_f$ and a [[right adjoint]] $\forall_f$ satisfying

1. [[Frobenius reciprocity]];

1. [[Beck-Chevalley condition]].

## Examples

Every [[Boolean category]] $\mathcal{C}$ is a Boolean hyperdoctrine given by the [[subobject poset]] [[functor]] $\mathrm{sub}:\mathcal{C}^{op} \to BoolAlg$. 

## Related concepts

* [[first-order hyperdoctrine]]

* [[coherent hyperdoctrine]]

* [[regular hyperdoctrine]]


## References

A discussion of the free Boolean hyperdoctrine generated from a [[signature (in logic)|signature]] is in 

* [[Todd Trimble]], _[[toddtrimble:Notes on predicate logic]]_

[[!redirects Boolean hyperdoctrines]]

