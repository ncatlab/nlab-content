
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

A (binary) [[relation]] $\sim$ on a set $A$ is __symmetric__ if any two elements that are related in one order are also related in the other order:
$$\forall (x, y: A),\; x \sim y \;\Rightarrow\; y \sim x$$

In the language of the $2$-poset-with-duals [[Rel]] of sets and relations, a relation $R: A \to A$ is __symmetric__ if it is contained in its reverse:
$$R \subseteq R^{op}$$
In that case, this containment is in fact an equality.

## Relation to graphs

A set with a symmetric relation is the same as a [[loop digraph object|loop]] [[digraph]] $(V, E, s:E \to V, t:E \to V)$ with a function $sym:E \to E$ such that 

* for every $f \in E$, $s(f) =_V t(sym(f))$
* for every $f \in E$, $t(f) =_V s(sym(f))$
* for every $f \in E$, $sym(sym(f)) =_E f$
* for every $a \in V$, $sym(refl(a)) =_E refl(a)$

## Related concepts

* [[relation]]

  * [[reflexive relation]]

  * **symmetric relation**

* [[setoid]]
