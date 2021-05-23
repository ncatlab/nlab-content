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

Just as a [[groupoid]] is the [[oidification]] of a [[group]] and a [[ringoid]] is the oidification of a [[ring]], an alternative magmoid should be the oidification of a [[alternative magma]]. 

## Definition

An __alternative magmoid__ is a [[magmoid]] $Q$ such that for every two objects $a,b \in Ob(Q)$ and for every morphism $f:a \to b$ and endomorphisms $g:a \to a$ and $h:b \to b$,

$$
  f \circ (g \circ g) = (f \circ g) \circ g
  \,
$$

and

$$
  h \circ (h \circ f) = (h \circ h) \circ f
  \,
$$

## Examples

* Every [[category]] is an alternative magmoid. 

* A one-object alternative magmoid is a [[alternative magma]]. 

* A [[Mod]]-enriched alternative magmoid is called a alternative algebroid. 

## Related concepts

[[!include oidification - table]]