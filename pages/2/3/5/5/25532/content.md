# Supply in a monoidal category

* toc
{: toc}

## Idea

Suppose given some algebraic structure $P$ that there can be on an object of a [[symmetric monoidal category]], such as monoids, comonoids, etc.  We say that a symmetric monoidal category $C$ *supplies* $P$ if every object of $C$ is equipped with a $P$-structure, compatibly with the tensor product.  Importantly, the morphisms of $C$ are *not* all required to be $P$-homomorphisms.

## Definition

Let $P$ be a (single-sorted) [[prop]], and $C$ a symmetric monoidal category.  A **supply of $P$ in $C$** consists of

1. A $P$-algebra structure on every object of $C$, such that
2. The $P$-algebra structure on any tensor product $x\otimes y$ is that canonically induced from those on $x$ and $y$.

If there is a given supply of $P$ in $C$, we also say that $C$ **supplies** $P$-algebras.

## Remarks

The notion of "supply" does not satisfy the [[principle of equivalence]]: if $C\simeq D$ then a supply of $P$ in $C$ does not automatically transfer to a supply of $P$ in $D$.  Accordingly, a "symmetric monoidal category that supplies $P$" should be thought of as an atomic categorical structure, not as a [[category]] equipped with [[stuff, structure, property|structure]].

## Examples

* A [[hypergraph category]] is a symmetric monoidal category that supplies special commutative [[Frobenius algebras]].

* A [[Markov category]] is a [[semicartesian monoidal category|semicartesian]] symmetric monoidal category that supplies commutative comonoids.

## References

* Brendan Fong and David I, Spivak, _Supplying bells and whistles in symmetric monoidal categories_, [arxiv](https://arxiv.org/abs/1908.02633), 2019

[[!redirects supplies in a monoidal category]]
[[!redirects supply]]
[[!redirects supplies]]
