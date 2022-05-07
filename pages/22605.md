+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of [[localization]] of a monoid, the [[localization]] of a [[category]] with a single object. Could be generalized to localization of [[monoid objects]] in a [[cartesian monoidal category]] $C$. The localization of a ring is a localization of a monoid object in [[Ab]].

## Definition

### For commutative monoids

Let $(M,1,*)$ be a commutative [[monoid object]] in $Set$ and let $S$ be a commutative [[subobject|submonoid]] of $M$. Then the __localization__ of $M$ __away from__ $S$, $S^{-1}M$, is the set of equivalences on $M \times S$, $(m_1,s_1) \sim (m_2,s_2)$ such that there is an element $u:S$ where $m_1 \cdot s_2 \cdot u = m_2 \cdot s_1 \cdot u$. 

Write $m s^{-1}$ for the [[equivalence class]] of $(m,s)$. On this set, the product is defined by

$$
  (m_1 s_1^{-1}) \cdot (m_2 s_2^{-1}) \coloneqq (m_1 \cdot m_2) (s_1 \cdot s_2)^{-1}
  \,.
$$

### For non-commutative monoids

Analogue of [[noncommutative localization]] for noncommutative monoid objects in $Set$ instead of $Ab$. 

...

## Group completion

The [[group completion]] of a monoid $M$ is the localization of $M$ away from $M$. 

## Related concepts

* [[localization]]

* [[localization of a ring]]