
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

An $n \times n$-[[matrix]] $U \in Mat(n, \mathbb{C})$ with entries in the [[complex numbers]] (for $n$ a [[natural number]]) is **unitary** if the following equivalent conditions hold

* it preserves the canonical [[inner product]] on $\mathbb{C}^n$;

* the operation $(-)^\dagger$ of [[transpose matrix|transposing]] it and then applying [[complex conjugation]] to all its entries takes it to its inverse:

  $$
    U^\dagger \;=\; U^{-1}
    \,.
  $$

  hence equivalently:

  $$
    U \cdot U^\dagger \;=\; \mathrm{I}
  $$

For fixed $n$, the unitary matrices under [[matrix product]] form a [[Lie group]]: the _[[unitary group]]_ $\mathrm{U}(n)$ (or other notations).

## Related concepts

* [[quaternion unitary group]]

[[!redirects unitary matrix]]
[[!redirects unitary matrices]]
