
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

* toc
{: toc}

## Idea

Consider a type $P$ of [[algebra|algebraic]] [[structure]] (such as [[monoid]]-structure, [[comonoid]]-structure, etc.)
that may be put on an [[object]] of a [[symmetric monoidal category]].  We say that a symmetric monoidal category $C$ *supplies* $P$ if every object of $C$ can be equipped with such $P$-structure, compatibly with the given [[tensor product]].  Importantly, the morphisms of $C$ are *not* all required to be $P$-homomorphisms.

## Definition

Let $P$ be a (single-sorted) [[prop]], and $C$ a symmetric monoidal category.  A **supply of $P$ in $C$** consists of

1. A $P$-algebra structure on every object of $C$, such that
2. The $P$-algebra structure on any tensor product $x\otimes y$ is that canonically induced from those on $x$ and $y$.

If there is a given supply of $P$ in $C$, we also say that $C$ **supplies** $P$-algebras.

## Remarks

The notion of "supply" does not satisfy the [[principle of equivalence]]: if $C\simeq D$ then a supply of $P$ in $C$ does not automatically transfer to a supply of $P$ in $D$.  Accordingly, a "symmetric monoidal category that supplies $P$" should be thought of as an atomic categorical structure, not as a [[category]] equipped with [[stuff, structure, property|structure]].

## Examples

* A [[hypergraph category]] is a symmetric monoidal category that supplies special commutative [[Frobenius algebras]].

* A [[Markov category]] is a [[semicartesian monoidal category|semicartesian]] symmetric monoidal category that supplies cocommutative comonoids.

* A [[gs-monoidal category]] is a symmetric monoidal category that supplies cocommutative comonoids.

## References

* [[Brendan Fong]], [[David Spivak]], _Supplying bells and whistles in symmetric monoidal categories_, &lbrack;[arxiv:1908.02633](https://arxiv.org/abs/1908.02633)&rbrack;

[[!redirects supplies in a monoidal category]]
[[!redirects supply]]
[[!redirects supplies]]
