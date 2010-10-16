
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[groupoid]] is [[connected]] if it is [[inhabited set|inhabited]] and every object is connected by a morphism to every other object.

Every [[category]] $C$ induces a groupoid $G(C)$ by freely inverting all its [[morphism]]s. A category is connected if the groupoid $G(C)$ is.


## Definition

A [[category]] $C$ is **connected** if it is [[inhabited set|inhabited]] and the following equivalent conditions hold

* any two [[objects]] can be connected by a [[zigzag]] of [[morphisms]].

* the $\infty$-groupoidification of the category (the [[Kan fibrant replacement]] of its [[nerve]]) is a [[connected]] [[∞-groupoid]].

* the [[geometric realization]] of its [[nerve]] is a [[connected topological space]].

* the [[localization]] $C[C_1^{-1}]$ of $C$ at all its morphisms is a connected groupoid.

Note that the [[empty category]] is not connected.  For other purposes, one can argue about whether the [[empty set]] should be called "connected," but for the applications of connected categories, the empty category should definitely not be called connected.  In particular, a [[terminal object]] is not a [[connected limit]].

## Related concepts

A [[connected limit]] is a [[limit]] whose domain [[diagram]] category is connected.

[[!redirects connected categories]]
[[!redirects connected groupoid]]
[[!redirects connected groupoids]]
