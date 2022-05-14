
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

A (binary) [[relation]] $\sim$ on a set $A$ is __reflexive__ if every element of $A$ is related to itself:
$$\forall (x: A),\; x \sim x$$

In the language of the $2$-poset [[Rel]] of sets and relations, a relation $R: A \to A$ is __reflexive__ if it contains the identity relation on $A$:
$$\id_A \subseteq R$$

## Relation to graphs

A set with a reflexive relation is the same as a [[loop digraph object|loop]] [[digraph]] $(V, E, s:E \to V, t:E \to V)$ with function $refl:V \to E$ such that 

* for every $a \in V$, $s(refl(a)) =_E a$
* for every $a \in V$, $t(refl(a)) =_E a$

## Related concepts

* [[relation]]

  * **reflexive relation**, [[irreflexive relation]]

  * [[symmetric relation]]

* [[first law of thought]]

* [[setoid]]

[[!redirects reflexive relation]]
[[!redirects reflexive relations]]

[[!redirects reflexivity]]
