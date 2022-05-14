[[!redirects directed loop graph object]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

A **loop graph object** [[internalization|internal to]] a [[category]] with [[finite products]] is an [[object]] that behaves in that category like loop [[graphs]] do in [[Set]].

## Definition 

### In a category with finite products

A **loop graph object** in a category $\mathcal{C}$ with [[finite products]] is a [[loop digraph object]] $(V, E, R:E \to V \times V)$ with a morphism $i:E \to E$ such that 

* $p_1 \circ R = p_2 \circ R \circ sym$
* $p_2 \circ R = p_1 \circ R \circ sym$
* $i \circ i = id_E$

where $p_1, p_2:V \times V \to V$ are the unique projection morphisms of the binary product. 

### In a general category

A **loop graph object** in a category $\mathcal{C}$ is a [[loop digraph object]] $(V, E, s:E \to V, t:E \to V)$ with a morphism $i:E \to E$ such that 

* $s \circ R = t \circ sym$
* $t \circ R = s \circ sym$
* $i \circ i = id_E$

## Properties

A loop graph object is equivalently an object with an [[internal relation|internal symmetric binary endorelation]]. 

## Related concepts

* [[graph]]

* [[symmetric relation]]

* [[loop digraph object]]

* [[internal relation]]

[[!redirects loop graph objects]]