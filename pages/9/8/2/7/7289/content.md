+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}



## Idea 

The notion of _parity complex_, introduced by [[Ross Street]], is a notion of [[pasting diagram]] shape. It is based on some combinatorial axioms on subshapes of codimension at most 2 which permit the construction of a (strict) $\omega$-[[strict omega-category|category]] [[free construction|freely generated]] from the shape. 

## Definition 

+-- {: .num_defn}
###### Definition 
A **parity structure** is a [[graded set]] $\{C_n\}_{n \geq 0}$ together with, for each $n \geq 0$, functions 
$$\partial^+_n \colon C_{n+1} \to P(C_n), \qquad \partial^-_n \colon C_{n+1} \to P(C_n);$$
we assume throughout this article that $\partial^+_n(c)$, $\partial^-_n(c)$ are finite, nonempty, and disjoint. 
=-- 

Following Street, we abbreviate $\partial^+_n(c)$ to $c^+$, and $\partial^-_n(c)$ to $c^-$. The Greek letters $\varepsilon$, $\eta$ refer to values in the set $\{+, -\}$. 

+-- {: .num_defn}
###### Definition
A parity structure is a **parity complex** if it satisfies the following axioms: 

1. $c^{--} \cup c^{++} = c^{-+} \cup c^{+-}$ 

1. If $c \in C_1$, then $c^-$ and $c^+$ are both singletons. 

1. If $x, y \in c^\eta$ are distinct $n$-cells, then $x^+ \cap y^+ = \emptyset$ and $x^- \cap y^- = \emptyset$. 

1. Define a [[relation]] $\lt$ by $x \lt y$ whenever $x^+ \cap y^- \neq \emptyset$, and let $\prec$ be the reflexive transitive closure of $\lt$. Then $\prec$ is antisymmetric, and if $x \prec y$ for $x \in c^\varepsilon$ and $y \in c^\eta$, then $\varepsilon = \eta$. 
=--

## Examples 

* [[simplex|Simplexes]] 

* [[globe|Globes]] 

* [[cube|Cubes]]

* Products of parity complexes 

* [[polyhedron|Polyhedra]] 

## Basic results 

(...)

## Related notions 

* [[directed complex]]

* [[direct category]]

* [[test category]]

* [[oriental]]

* [[pasting scheme]]

## References 

* [[Ross Street]], _Parity complexes_, Cahiers Top. G&#233;om Diff. Cat&#233;goriques 32 (1991), 315-343. ([link](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1991__32_4/CTGDC_1991__32_4_315_0/CTGDC_1991__32_4_315_0.pdf)) Corrigenda, Cahiers Top. G&#233;om Diff. Cat&#233;goriques 35 (1994), 359-361. ([link](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1994__35_4/CTGDC_1994__35_4_359_0/CTGDC_1994__35_4_359_0.pdf))

[[!redirects parity complexes]]
