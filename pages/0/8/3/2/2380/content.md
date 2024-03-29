
> This entry is about the notion in [[type theory]]. For the unrelated notion of the same name in [[model theory]] see at _[[type (in model theory)]]_.


***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In modern [[logic]], we understand that every [[variable]] should have a _type_, or _domain of discourse_ or be of some _sort_.  For instance we say that if a variable $n$ is constrained to be an [[integer]] then "$n$ is of integer type" or "of type $\mathbb{Z}$". The usual formal expression from [[set theory]] for this -- $n \in \mathbb{Z}$ -- is then often written $n \colon \mathbb{Z}$

We speak of _typed logic_ if this typing of variables is enforced by the [[metalanguage]]. In formulations of a [[theory]] the types are often called _sorts_. More generally, _[[type theory]]_ formalizes reasoning with such typed variables. See there for more

(Untyped logic may be seen as simply a special case, in which there is only a single unique type.  Thus, untyped logic has *one* type, not *no* type.)

## Definition

Reasoning with types is formalized in [[natural deduction]] (which in turn is formalized in a [[logical framework]] such as [[Elf]]).

Behaviour of types is specified by a 4-step set of rules

1. [[type formation]]

1. [[term introduction]]

1. [[term elimination]]

1. [[computation rules]]

## Properties

Deep relations between [[type theory]], [[category theory]] and [[computer science]] relate types to other notions, such as [[objects]] in a [[category]]. See at _[[computational trinitarianism]]_ for more on this.

## Related concepts

* [[category (philosophy)]]

* [[fibrant type]]

[[!include notions of type]]


[[!redirects types]]

[[!redirects domain of discourse]]
[[!redirects domains of discourse]]
[[!redirects universe of discourse]]
[[!redirects universes of discourse]]

[[!redirects sort]]
[[!redirects sorts]]

