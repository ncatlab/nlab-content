
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Set theory
+-- {: .hide}
[[!include set theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

Covered marked extensional well-founded orders are important in constructing the [[sets]] of the [[cumulative hierarchy]] $V$ in a model of set theory, in the same way that [[well-orders]] or sets with [[transitive relation|transitive]] [[extensional relation|extensional]] [[well-founded relations]] are important in constructing the [[ordinals]] of $V$. These become important in [[constructive mathematics]] where one cannot in general show that the set of [[cardinals]] in $V$ and the set of ordinals in $V$ are in bijection with each other. 

## Definition

A **marked extensional well-founded order** or **mewo** is a set $S$ with an [[extensional relation|extensional]] [[well-founded relation]] $a \prec b$ on a set $S$ and a [[predicate]] $m(a)$ on $S$. 

An element $x \in S$ is **marked** if $m(x)$ is true. An element $x \in S$ is **covered** if there exists a marked element $y \in S$ such that $x \prec y$ is true. A marked extensional well-founded order is a **covered marked extensional well-founded order** if every element $x \in S$ is covered; i.e. 

$$\forall x \in S.\exists y \in S.m(y) \wedge (x \prec y)$$

## Related concepts

* [[well-order]]

* [[extensional relation]]

* [[well-founded relation]]

## References

* {#deJongEtAl23} [[Tom de Jong]], [[Nicolai Kraus]], [[Fredrik Nordvall Forsberg]], [[Chuangjie Xu]], *Set-Theoretic and Type-Theoretic Ordinals Coincide* ([arXiv:2301.10696](https://arxiv.org/abs/2301.10696))

[[!redirects marked extensional well-founded order]]
[[!redirects marked extensional well-founded orders]]

[[!redirects mewo]]
[[!redirects mewos]]

[[!redirects MEWO]]
[[!redirects MEWOs]]

[[!redirects covered marked extensional well-founded order]]
[[!redirects covered marked extensional well-founded orders]]

[[!redirects covered mewo]]
[[!redirects covered mewos]]

[[!redirects covered MEWO]]
[[!redirects covered MEWOs]]

[[!redirects marked extensional well-founded relation]]
[[!redirects marked extensional well-founded relations]]

[[!redirects covered marked extensional well-founded relation]]
[[!redirects covered marked extensional well-founded relations]]

[[!redirects marked element]]
[[!redirects marked elements]]

[[!redirects subset of marked elements]]
[[!redirects subsets of marked elements]]

[[!redirects covered element]]
[[!redirects covered elements]]