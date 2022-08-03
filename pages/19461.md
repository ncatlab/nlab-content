+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In a [[rewriting system]], a term is said to be of **normal form** if it does not admit any further rewrites.

In [[type theory]], a [[canonical form]] is a normal form, but the converse need not hold.

A term is weakly normalizing if there exists at least one particular sequence of rewrites that eventually yields a normal form. A rewrite has weak normalization if every term has this property.

A term is strongly normalizing if every sequence of rewrites eventually terminates with a normal form. If every term has this property, the rewrite system has strong normalization.

In the [[untyped lambda calculus]] the term $(\lambda x . x x x) (\lambda x . x x x)$ is neither strongly nor weakly normalizing.

## Related concepts

* [[canonical form]]

[[!redirects normal forms]]