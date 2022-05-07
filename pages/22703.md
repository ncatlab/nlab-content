+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Categorification
+-- {: .hide}
[[!include categorification - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Just as a [[groupoid]] is the [[oidification]] of a [[group]] and a [[ringoid]] is the oidification of a [[ring]], a [[unital magmoid]] should be the oidification of a [[unital magma]]. 

## Definition

A __unital magmoid__ $Q$ is a [[magmoid]] where every object $a \in Ob(Q)$ has an [[identity morphism]] $id_a: a \to a$, such that for any morphism $f:a \to b$, $f \circ id_a = f$, and for any morphism $g:c \to a$, $id_a \circ g = g$. 

A unital magmoid is __invertible__ if for every pair of objects $a,b \in Ob(Q)$ and for every morphism $f:a \to b$, there exists an [[inverse morphism]] $g:b \to a$ such that $f \circ g = id_b$ and $g \circ f = id_a$. 

## Examples

* A [[groupoid]] is a unital magmoid. 

* A [[category]] and a [[loopoid]] are unital magmoids. 

* A unital magmoid with only one object is called a [[unital magma]]. 

## Related concepts

[[!include oidification - table]]

[[!redirects unital magmoids]]