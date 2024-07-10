
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

A [[setoid]] whose [[quotient set]] is a [[group]]. Equivalently, a [[thin category|thin]] [[2-group]], or in foundations where groupoids are [[univalent groupoid|univalent]] by default, a [[thin category|thin]] [[pregroupoid|pre]]-2-group. Also, equivalently, a [[monoidal setoid]] in which the monoidal product with any element has an [[inverse]] up to [[equivalence relation]]. 

“Groupal setoid” is a placeholder name for a concept which may or may not have another name in the mathematics literature. 

## Definition

Here we assume that setoids are equipped with an [[equivalence relation]] (rather than a [[pseudo-equivalence relation]]). A **groupal setoid** is a [[monoidal setoid]] $(A, \sim, e, m)$ with a function $i:A \to A$ such that 

* $i$ preserves the [[equivalence relation]]: for all elements $a \in A$ and $b \in A$, if $a \sim b$, then $i(a) \sim i(b)$. 

* $i$ satisfies the left and right inverse laws up to the equivalence relation: for all elements $a \in A$, $m(a, i(a)) \sim e$ and $m(i(a), a) \sim e$. 

$A$ is **[[abelian group|abelian groupal]]** or **[[symmetric 2-group|symmetric groupal]]** or **[[braided 2-group|braided groupal]]** if additionally for all elements $a \in A$ and $b \in A$, $m(a, b) \sim m(b, a)$. 

## Examples

* Given any [[Archimedean ordered field]] $F$, the set of [[Cauchy sequences]] in $F$ is a abelian groupal setoid. 

## Related concepts

* [[setoid]]

* [[group]], [[abelian group]]

* [[monoidal setoid]]

* [[ring setoid]]

* [[2-group]]

[[!redirects groupal setoid]]
[[!redirects groupal setoids]]

[[!redirects thin 2-group]]
[[!redirects thin 2-groups]]

[[!redirects thin pre-2-group]]
[[!redirects thin pre-2-groups]]

[[!redirects abelian groupal setoid]]
[[!redirects abelian groupal setoids]]

[[!redirects braided groupal setoid]]
[[!redirects braided groupal setoids]]

[[!redirects thin braided 2-group]]
[[!redirects thin braided 2-groups]]

[[!redirects thin braided pre-2-group]]
[[!redirects thin braided pre-2-groups]]

[[!redirects symmetric groupal setoid]]
[[!redirects symmetric groupal setoids]]

[[!redirects thin symmetric 2-group]]
[[!redirects thin symmetric 2-groups]]

[[!redirects thin symmetric pre-2-group]]
[[!redirects thin symmetric pre-2-groups]]