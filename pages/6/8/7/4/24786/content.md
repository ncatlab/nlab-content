+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--
# Contents
* table of contents
{:toc}

## Definition

An **absolutely dense functor** $F \colon A \to B$ is a [[functor]] which is equivalently characterised by the following conditions:

1. $F^* = [F^{op}, Set] \colon [B^{op}, Set] \to [A^{op}, Set]$ is [[fully faithful]].

1. The [[counit]] of the adjunction $F_* \dashv F^* : [B^{op}, Set] \to [A^{op}, Set]$ is invertible.

1. $F$ is [[co-fully faithful]] (also called a [[lax epimorphism]]) in [[Cat]].

1. For every functor $G : B^{op} \times B \to C$, there is a canonical isomorphism ([MathOverflow answer](https://mathoverflow.net/a/354097))
$$ \int_{b \in B} G(b, b) \cong \int_{a \in A} G(F a, F a) $$
(This is a notion of [[final functor|initiality]] for [[ends]].)

More generally, an **absolutely dense morphism** in a [[proarrow equipment]] $K \to M$ is a 1-cell $f : a \to b$ in $K$ for which the counit $f_* \circ f^* \cong 1_b$.

## References

- [[Jiri Adamek]], [[Robert El Bashir]], [[Manuela Sobral]], [[Jiri Velebil]]. _On functors which are lax epimorphisms_. TAC. (2001)

- [[Fernando Lucatelli Nunes]] and [[Sousa Lurdes]]. _On lax epimorphisms and the associated factorization_. Journal of Pure and Applied Algebra 226.12 (2022)


[[!redirects absolutely dense]]
[[!redirects absolutely dense functors]]
[[!redirects absolutely dense morphism]]
[[!redirects absolutely dense morphisms]]