
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

## Idea

A _universally closed morphism_ is a [[closed morphism]] all whose [[pullback]]s are also closed.

## Definition

Let $C$ be a [[category]] with [[pullback]]s and with a notion of [[closed morphism]] which is stable under [[composition]] and contains all the [[isomorphisms]]. 

A morphism $f:X\to Y$ in $C$ is __universally closed__ if for every
$h: Z\to Y$ the [[pullback]] $h^*(f): Z\times_Y X\to Z$ is a [[closed morphism]]. 

In particular, for $h=id_Y$ we see that a universally closed morphism is itself closed. 

## Examples

* The assumptions are satisfied in the category of [[scheme]]s. See [[valuative criterion of properness]] for a characterization of universally closed morphisms of schemes via valuation rings. 

[[!redirects universally closed morphisms]]