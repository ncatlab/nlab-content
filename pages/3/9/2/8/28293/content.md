

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

A [[category]] $C$ is **strongly connected** if it is [[inhabited set|inhabited]] and for any [[pair]] of [[objects]] $A,B$ there is a [[morphism]] $A \to B$. That is, each [[hom-set]] is inhabited.

This terminology is borrowed from [[graph|graph theory]]: a [[directed graph]] is called strongly connected when it is inhabited and for every two vertices $u,v$ there is a directed path from $u$ to $v$. Hence, a category is strongly connected precisely when its underlying directed graph is strongly connected.

If we merely require that for all objects $A,B$ there is a morphism $A \to B$ or a morphism $B \to A$, we call $C$ **semi-strongly connected**. This is no standard terminology, though, and in fact in Bunge's thesis (cited below) this property has been called *strongly connected*.

## Properties

* Every strongly connected category is semi-strongly connected.

* Every semi-strongly connected category is a [[connected category]].

* Every connected [[groupoid]] is strongly connected.

* Every inhabited category with [[zero morphisms]] is strongly connected.

## Examples

Among semi-strongly connected categories are:

* the [[Set|category of sets]],

* every [[inhabited set|inhabited]] [[linear order]], considered as a [[thin category]].

Among strongly connected categories are:

* the [[Ab|category of abelian groups]],

* the category of non-empty sets.
 
## Counterexamples

Not semi-strongly connected are:

* the [[CRing|category of commutative rings]],

* the [[empty category]],

* the [[product category]] $Set \times Set$.

## Related concepts

* [[connected category]]

## References

The terminology was introduced in:

* [[Marta Bunge]]: *Categories of set valued functors*, PhD thesis, University of Pennsylvania (1966) &lbrack;[[Bunge-CategoriesOfSetValuedFunctors.pdf:file]]&rbrack;

  Reprints in Theory and Applications of Categories **30** (2024) 1-84 &lbrack;[tac:tr39abs](http://www.tac.mta.ca/tac/reprints/articles/30/tr30abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/30/tr30.pdf)&rbrack;

[[!redirects strongly connected categories]]

[[!redirects strongly connected]]

[[!redirects semi-strongly connected]]

[[!redirects semi-strongly connected category]]

[[!redirects semi-strongly connected categories]]