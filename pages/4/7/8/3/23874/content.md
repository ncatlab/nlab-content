[[!redirects directed loop graph object]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
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

Recall that a [[topos]] is a [[category]] that behaves likes the category [[Set]] of [[set|sets]].  

A **loop digraph object** [[internalization|internal to]] a topos is an [[object]] that behaves in that topos like loop [[digraphs]] do in [[Set]].

## Definition 

### In a topos

A **loop digraph object** in a [[topos]] $\mathcal{E}$ with [[terminal object]] $1$ is 

* a [[object]] $V$ in $\mathcal{E}$ 

* an object $E$ in $\mathcal{E}$

* a [[morphism]] $s:E \to V$

* a morphism $t:E \to V$

such that $s$ and $t$ are [[jointly injective]]: for every [[global element]] $f: 1 \to E$ and $g: 1 \to E$, $s \circ f = s \circ g$ and $t \circ f = t \circ g$ imply that $f = g$. 

## Related concepts

* [[graph]]

* [[digraph]]

* [[relation]]

[[!redirects loop digraph objects]]