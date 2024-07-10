
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
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

A [[setoid]] whose [[quotient set]] is a [[monoid]]. Equivalently, a [[thin category|thin]] [[monoidal category|monoidal]] [[groupoid]], or in foundations where groupoids are [[univalent groupoid|univalent]] by default, a [[thin category|thin]] monoidal [[pregroupoid]]. 

“Monoidal setoid” is a placeholder name for a concept which may or may not have another name in the mathematics literature. 

## Definition

Here we assume that setoids are equipped with an [[equivalence relation]] (rather than a [[pseudo-equivalence relation]]). A **monoidal setoid** is a [[setoid]] $(A, \sim)$ with an element $e \in A$ and a function $m:A \times A \to A$ such that 

* $m$ preserves the [[equivalence relation]]: for all elements $a \in A$, $b \in A$, $c \in A$, and $d \in A$, if $a \sim c$ and $b \sim d$, then $m(a, b) \sim m(c, d)$. 

* $m$ is associative up to the equivalence relation: for all elements $a \in A$, $b \in A$, $c \in A$, $m(a, m(b, c)) \sim m(m(a, b), c)$

* $m$ is left and right unital up to the equivalence relation: for all elements $a \in A$, $m(a, e) \sim a$ and $m(e, a) \sim e$. 

$A$ is **[[commutative monoid|commutative monoidal]]** or **[[symmetric monoidal category|symmetric monoidal]]** or **[[braided monoidal category|braided monoidal]]** if additionally for all elements $a \in A$ and $b \in A$, $m(a, b) \sim m(b, a)$. 

## Examples

* Given any [[Archimedean ordered field]] $F$, the set of [[Cauchy sequences]] in $F$ is a [[monoidal setoid]] in two different ways, with respect to addition and with respect to multiplication. 

## Related concepts

* [[setoid]]

* [[groupal setoid]]

* [[ring setoid]]

* [[monoidal category]]

[[!redirects monoidal setoid]]
[[!redirects monoidal setoids]]

[[!redirects thin monoidal groupoid]]
[[!redirects thin monoidal groupoids]]

[[!redirects thin monoidal pregroupoid]]
[[!redirects thin monoidal pregroupoids]]

[[!redirects commutative monoidal setoid]]
[[!redirects commutative monoidal setoids]]

[[!redirects braided monoidal setoid]]
[[!redirects braided monoidal setoids]]

[[!redirects thin braided monoidal groupoid]]
[[!redirects thin braided monoidal groupoids]]

[[!redirects thin braided monoidal pregroupoid]]
[[!redirects thin braided monoidal pregroupoids]]

[[!redirects symmetric monoidal setoid]]
[[!redirects symmetric monoidal setoids]]

[[!redirects thin symmetric monoidal groupoid]]
[[!redirects thin symmetric monoidal groupoids]]

[[!redirects thin symmetric monoidal pregroupoid]]
[[!redirects thin symmetric monoidal pregroupoids]]