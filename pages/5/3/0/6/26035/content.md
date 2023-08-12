
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[dependent type theory]], a notion of [[finite type]] for [[types]] which are not just [[h-sets]]. 

## Definition

A type is a **$\pi$-finite type** if if it has finitely many connected components and there exists a [[natural number]] $n$ such that all its [[homotopy groups]] up to [[h-level]] $n$ at all base points are finite. 

For given [[natural number]] $n$, a type is a **$\pi_n$-finite type** if it has finitely many connected components and all its [[homotopy groups]] up to [[h-level]] $n$ at all base points are finite. 

## Properties

Given two $\pi$-finite types $A$ and $B$, the types $A \times B$ and $A + B$ are both $\pi$-finite types. Similarly, given a family of $\pi$-finite types $B(x)$ indexed by a $\pi$-finite type $x:A$, the dependent sum type $\sum_{x:A} B(x)$ is a $\pi$-finite type. 

## See also

* [[finite type]]

* [[locally finite type]]

* [[pi-finite homotopy type]]

* [[combinatorics]]

## References

* [[UniMath project]], *π-finite types* ([web](https://unimath.github.io/agda-unimath/univalent-combinatorics.pi-finite-types.html))

* [[UniMath project]], *Univalent combinatorics* ([web](https://unimath.github.io/agda-unimath/univalent-combinatorics.html))

[[!redirects π-finite type]]
[[!redirects π-finite types]]

[[!redirects pi-finite type]]
[[!redirects pi-finite types]]