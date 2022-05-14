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

A **loop digraph object** [[internalization|internal to]] a [[category]] is an [[object]] that behaves in that category like loop [[digraphs]] do in [[Set]].

## Definition 

### In a category with finite products

A **loop digraph object** in a [[category]] $\mathcal{C}$ with [[finite products]] is

* a [[object]] $V$ in $\mathcal{C}$ 

* an object $E$ in $\mathcal{C}$

* a [[morphism]] $R:E \to V \times V$

such that $R$ is [[monic]]: for every object $A$ in $\mathcal{C}$ and morphisms $f: A \to E$ and $g: A \to E$, $R \circ f = R \circ g$ implies that $f = g$. 

### In general categories

A **loop digraph object** in a category $\mathcal{C}$ is

* a [[object]] $V$ in $\mathcal{C}$ 

* an object $E$ in $\mathcal{C}$

* a [[morphism]] $s:E \to V$

* a morphism $t:E \to V$

such that $s$ and $t$ are [[jointly monic]]: for every object $A$ in $\mathcal{C}$ and morphisms $f: A \to E$ and $g: A \to E$, $s \circ f = s \circ g$ and $t \circ f = t \circ g$ imply that $f = g$. 

## Properties

A loop digraph object is equivalently an object with an [[internal relation|internal binary endorelation]]. 

## Related concepts

* [[graph]]

* [[digraph]]

* [[relation]]

* [[loop graph object]]

* [[internal relation]]

[[!redirects loop digraph objects]]