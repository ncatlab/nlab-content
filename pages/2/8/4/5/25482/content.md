
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $L \dashv R$ be an [[adjunction]].
\begin{tikzcd}
	C & D
	\arrow[""{name=0, anchor=center, inner sep=0}, "L", bend left, from=1-1, to=1-2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "R", bend left, from=1-2, to=1-1]
	\arrow["\dashv"{anchor=center, rotate=-90}, draw=none, from=0, to=1]
\end{tikzcd}

The **envelope** of the adjunction, denoted $Env(L \dashv R)$, is the [[category]] whose [[objects]] are [[quadruples]]

$$
(c \in C, d \in D, f : L c \to d, g \colon c \to R d)
$$

such that $f$ and $g$ are each other's [[mate]], and whose [[morphisms]] are [[pairs]]

$$
(p \colon c \to c', q \colon d \to d')
$$

such that $(R q) \circ f = f' \circ p$ or equivalently $q \circ g = g' \circ (L p)$.

## Properties

* A [[functor]] $L \colon C \to D$ is [[left adjoint]] to a functor $R \colon D \to C$ if and only if there is an isomorphism of [[comma categories]] $L \downarrow D \cong C \downarrow R$ and this isomorphism commutes with the [[forgetful functors]] to the [[product category]] $C \times D$. In this case, the envelope $Env(L \dashv R)$ is also isomorphic to these comma categories over the evident forgetful functor to $C \times D$.

## Examples

* The envelope of the [[Isbell duality]] adjunction associated to a category $A$ is the [[Isbell envelope]] of $A$.

## Related concepts

* [[fixed point of an adjunction]]

## References

* [[Tom Avery]], [[Tom Leinster]]. _Isbell conjugacy and the reflexive completion_. Theory and Applications of Categories, **36** 12 (2021) 306-347 &lbrack;[tac:36-12](http://www.tac.mta.ca/tac/volumes/36/12/36-12abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/36/12/36-12.pdf)&rbrack;
