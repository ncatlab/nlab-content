
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
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

A [[setoid]] or [[Bishop set]] whose [[quotient set]] is an [[ordered field]]. 

“Ordered field setoid” and "Bishop ordered field" are placeholder names for a concept which may or may not have another name in the mathematics literature. 

## Definition

Classically: 

An **ordered field setoid** is a [[field setoid]] $(R, \sim)$ equipped with a [[strict weak order]] $\lt$ such that 

* for all $a \in R$ and $b \in R$, if $a \lt b$ is not true and $b \lt a$ is not true, then $a \sim b$

* $0 \lt 1$

* for all $a \in R$ and $b \in R$, $0 \lt a$ and $0 \lt b$ implies that $0 \lt a + b$; alternatively, $0 \lt a + b$ implies that $0 \lt a$ or $0 \lt b$. 

* for all $a \in R$ and $b \in R$, if $0 \lt a$ and $0 \lt b$, then $0 \lt a \cdot b$

One often sees the definition using a weak [[total order]] $\leq$ instead of the strict total order $\lt$. This makes no difference in [[classical mathematics]], but the definition of the strict total order is the one that generalizes to [[constructive mathematics]]. 

## Properties

* Given any ordered field setoid $S$, the [[rational numbers]] $\mathbb{Q}$ are a subset of $S$. In addition, there exists a [[ring setoid homomorphism]] from $\mathbb{Q} \to S$; however, this ring setoid homomorphism is not unique, unlike the case for [[ordered fields]] and [[ring homomorphisms]]. 

## Examples

* Given any [[Archimedean ordered field]] $F$, the set of [[Cauchy sequences]] in $F$ is an ordered field setoid. 

* Given any [[Archimedean ordered field]] $F$, the set of all [[locators]] of all elements of $F$ is an ordered field setoid. 

## Related concepts

* [[setoid]], [[Bishop set]]

* [[ordered field]]

* [[ring setoid]], [[field setoid]]

* [[Archimedean ordered field setoid]]

[[!redirects ordered field setoid]]
[[!redirects ordered field setoids]]

[[!redirects ordered Bishop field]]
[[!redirects ordered Bishop fields]]

[[!redirects Bishop ordered field]]
[[!redirects Bishop ordered fields]]