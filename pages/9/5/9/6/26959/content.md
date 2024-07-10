
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
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[constructive mathematics|constructive]] [[real analysis]], there have been many different proposals to define a well-behaved notion of the [[real numbers]], such as the [[Dedekind real numbers]]. However, there is one definition of real numbers classically which is not well behaved in constructive mathematics: The [[Cauchy real numbers]], whether defined with or without [[moduli of continuity]]. While the set of Cauchy sequences of the [[rational numbers]] is [[sequentially Cauchy complete]], the Cauchy real numbers as defined as a quotient set of Cauchy sequences of the [[rational numbers]] is not [[sequentially Cauchy complete]], because quotient sets do not preserve sequential Cauchy completeness. In addition, some [[foundations of mathematics]], such as the original [[predicative mathematics|predicative]] [[Martin-Loef type theory]] with [[canonicity]], are sufficiently weak that they do not have [[quotient sets]]. As a result, for a more well-behaved notion of real numbers, they instead use directly the set of Cauchy sequences of the [[rational numbers]] with [[modulus of continuity]] as an [[Archimedean ordered field setoid]], which happen to be [[sequentially Cauchy complete]]

The notion of *sequentially Cauchy complete Archimedean ordered field setoid* is to unify the different approaches to the well-behaved real numbers in real analysis. 

Sequential cauchy completeness is important in real analysis because it is used in various approaches to [[real analysis]] to define certain functions on the real numbers and prove many properties of the real numbers, such as the [[analytic functions]] and the [[fundamental theorem of calculus]] - which are not definable or provable without sequential Cauchy completeness of the real numbers. 

## Properties

* Every [[sequentially Cauchy complete]] [[Archimedean ordered field setoid]] is a [[sequentially Cauchy complete]] [[pseudometric space]]. 

## Examples

There are many examples of a sequentially Cauchy complete Archimedean ordered field setoid. These include: 

* Any [[sequentially Cauchy complete]] [[Archimedean ordered field]]: 

  * the [[Dedekind real numbers]], 

  * the [[multivalued Cauchy real numbers]], 

  * the [[generalised Cauchy real numbers]] using [[Cauchy filters]] or [[Cauchy nets]], 

  * the real numbers as a [[terminal object]] in some suitable category, such as [[Archimedean ordered fields]]. 

  * subsets of the Dedekind real numbers consisting of Dedekind cuts valued in a [[subobject|sub]]-[[sigma-frame|$\sigma$-frame]] of the [[frame of truth values]]

  * the [[Escardo-Simpson real numbers]]

  * the [[HoTT book real numbers]]

* Given any [[Archimedean ordered field]] $F$, the set of [[Cauchy sequences]] in $F$ with [[modulus of continuity]] is a sequentially Cauchy complete Archimedean ordered field setoid

  * In particular, the usual set of [[Cauchy sequences]] of [[rational numbers]] with [[modulus of continuity]] is a sequentially Cauchy complete Archimedean ordered field setoid. 

* Given any [[Archimedean ordered field]] $F$, the set of [[Cauchy filters]], [[Cauchy nets]], or [[multivalued Cauchy sequences]] in $F$ with [[modulus of continuity]] is a sequentially Cauchy complete Archimedean ordered field setoid

* Given any [[Archimedean ordered field|Archimedean ordered]] [[field extension]] $F$ of the [[Cauchy real numbers]] $\mathbb{R}_C$, the set of all [[locators]] of all elements of $F$ is a sequentially Cauchy complete Archimedean ordered field setoid. 

## Related concepts

* [[pseudometric space]]

* [[sequentially Cauchy complete space]]

* [[Archimedean ordered field setoid]]

[[!redirects sequentially Cauchy complete Archimedean ordered field setoid]]
[[!redirects sequentially Cauchy complete Archimedean ordered field setoids]]