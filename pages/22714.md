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

Just as a [[groupoid]] is the [[oidification]] of a [[group]] and a [[ringoid]] is the oidification of a [[ring]], an flexible magmoid should be the oidification of a [[flexible magma]]. 

## Definition

A __flexible magmoid__ is a [[magmoid]] $Q$ such that for every two objects $a,b \in Ob(Q)$ and for every two morphisms $f:a \to b$ and $g:b \to a$, 

$$
  f \circ (g \circ f) = (f \circ g) \circ f
  \,.
$$

## Examples

* Every [[category]] is a flexible magmoid. 

* A one-object flexible magmoid is a [[flexible magma]]. 

* A [[Mod]]-enriched flexible magmoid is called a flexible [[linear magmoid]]. 

## Related concepts

[[!include oidification - table]]