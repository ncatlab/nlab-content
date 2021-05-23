+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Enriched category theory
+-- {: .hide}
[[!include enriched category theory contents]]
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

# Contents
* table of contents
{: toc}


## Idea

A differential algebroid is an [[oidification]] of the concept of [[differential algebra]].

## Definitions

Let $K$ be a [[commutative ring]] and $C$ be a $K$-[[linear category]]. Then $C$ is a __$K$-differential algebroid__ if for every hom-$K$-module $Mor(a,b)$ there is a $K$-linear morphism $d_{Mor(a,b)}:Mor(a,b) \to Mor(a,b)$ such that for all objects $a,b,c\in Ob(C)$, morphisms $f:Mor(a,b)$ and $g:Mor(b,c)$, and $K$-linear morphisms $d_{Mor(a,b)}:Mor(a,b) \to Mor(a,b)$, $d_{Mor(b,c)}:Mor(b,c) \to Mor(b,c)$, and $d_{Mor(a,c)}:Mor(a,c) \to Mor(a,c)$
$$
  d_{Mor(a,c)}(g \circ f) = d_{Mor(b,c)}(g) \circ f + g \circ d_{Mor(a,b)}(f)
  \,.
$$

## Examples

* A [[differential algebra]] is a differential algebroid with only one object. 

## Related concepts

[[!include oidification - table]]

[[!redirects differential algebroid]]
[[!redirects differential algebroids]]