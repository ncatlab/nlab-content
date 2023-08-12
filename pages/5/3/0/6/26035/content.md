
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

In [[dependent type theory]] ([[homotopy type theory]]), by *$\pi$-finite types* one means a kind of [[finite types]] which are not necessarily [[h-sets]] but have [[finite group|finite]] [[homotopy groups]] in each degree (what in [[homotopy theory]] are called a *[[pi-finite homotopy types]]* or similar).

## Definition
 {#Definition}

For given [[natural number]] $n$, a [[type]] is called *$\pi_n$-finite* if

1. it has a [[finite type]] of [[connected components]] ([[0-truncation]]), 

1. all its [[homotopy groups]] up to [[h-level]] $n$ at all base points are [[finite group|finite]].

A type is **$\pi$-finite type** if it is $\pi_n$-finite for all $n \colon \mathbb{N}$.


## Properties

Given two $\pi$-finite types $A$ and $B$, the types $A \times B$ and $A + B$ are both $\pi$-finite types. Similarly, given a family of $\pi$-finite types $B(x)$ indexed by a $\pi$-finite type $x:A$, the dependent sum type $\sum_{x:A} B(x)$ is a $\pi$-finite type.

## Examples

Given a [[univalent universe]] $U$ and a natural number $n:\mathbb{N}$, 

* the type of all $U$-small types with $n$ elements is a $\pi$-finite type. 

* The type of all $U$-small [[finite groups]] of [[order]] $n$ is a $\pi$-finite type. 

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