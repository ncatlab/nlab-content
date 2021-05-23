+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Categorification
+-- {: .hide}
[[!include categorification - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

An __absorption category__ or __annihilation category__ $C$ is a [[category]] where for every two objects $a, b \in Ob(C)$ there is a morphism $0_{a\to b}: a \to b$, such that for any objects $a, b, c, d \in Ob(C)$, for any morphism $f:b \to c$, $f \circ 0_{a\to b} = 0_{a\to c}$, and for any morphism $g:d \to a$, $0_{a\to b} \circ g = 0_{d\to b}$. 

## Examples

* Every [[ringoid]] and [[algebroid]] is an absorption category. 

* An [[absorption monoid]] is an absorption category with only one object. 

## Related concepts

[[!include oidification - table]]

[[!redirects absorption categories]]
[[!redirects annihilation category]]
[[!redirects annihilation category]]