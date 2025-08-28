[[!redirects absolute dense functor]]
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

1. $F$ is [[dense]] and $Lan_F F$ is an [[absolute Kan extension]].

1. $F^* = [F^{op}, Set] \colon [B^{op}, Set] \to [A^{op}, Set]$ is [[fully faithful]].

1. The [[counit]] of the adjunction $F_* \dashv F^* : [B^{op}, Set] \to [A^{op}, Set]$ is invertible.

1. $F$ is [[corepresentably fully faithful]] (also called a [[lax epimorphism]]) in [[Cat]].

1. For every functor $G : B^{op} \times B \to C$, there is a canonical isomorphism ([MathOverflow answer](https://mathoverflow.net/a/354097))
$$ \int_{b \in B} G(b, b) \cong \int_{a \in A} G(F a, F a) $$
(This is a notion of [[final functor|initiality]] for [[ends]].)

1. For every morphism $f : b \to b'$ in $B$, the category of $F$-factorisations of $f$ (which has objects triples $(a \in A, f_1 : b \to f a, f_2 : f a \to b')$ such that $f_2 f_1 = f$) is [[connected]]. ([MathOverflow answer](https://mathoverflow.net/a/354097))

More generally, an **absolutely dense morphism** in a [[proarrow equipment]] $K \to M$ is a 1-cell $f : a \to b$ in $K$ for which the counit $f_* \circ f^* \cong 1_b$.

## Properties

Every simultaneously reflective and coreflective subcategory of a presheaf category is itself a presheaf category and is induced by precomposition along an absolutely dense functor: this is the main result of the paper of El Bashir--Velebil below.

## References

(Absolutely dense functors are called **Cauchy dense** in the following paper of [[Brian Day]].)

- [[Brian Day]]. _Density presentations of functors_. Bulletin of the Australian Mathematical Society 16.3 (1977): 427-448.

- [[Jiri Adamek]], [[Robert El Bashir]], [[Manuela Sobral]], [[Jiri Velebil]]. _On functors which are lax epimorphisms_. TAC. (2001)

- Robert El Bashir and [[Jiri Velebil]]. _Simultaneously reflective and coreflective subcategories of presheaves_. Theory and Applications of Categories 10.16 (2002): 410-423.

- [[Fernando Lucatelli Nunes]] and [[Sousa Lurdes]]. _On lax epimorphisms and the associated factorization_. Journal of Pure and Applied Algebra 226.12 (2022)

- Adrián Doña Mateo, _Cauchy density_, [arXiv:2507.07869](https://arxiv.org/abs/2507.07869) (2025).


[[!redirects absolutely dense]]
[[!redirects absolutely dense functors]]
[[!redirects absolutely dense morphism]]
[[!redirects absolutely dense morphisms]]
