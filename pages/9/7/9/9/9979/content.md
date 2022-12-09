
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Definition

An **irreflexive symmetric relation** is a [[binary relation]] that is [[irreflexive relation|irreflexive]] and [[symmetric relation|symmetric]]. 

## Examples

* Every [[apartness relation]] is an irreflexive symmetric relation which is also a [[comparison]]. 

* The negation of a [[reflexive symmetric relation]] is an irreflexive symmetric relation. 

* Every [[denial inequality]] is a [[weakly tight relation|weakly tight]] irreflexive symmetric relation. 

## In constructive mathematics
 {#ConstructiveMathematics}

In constructive mathematics, not ever tight irreflexive symmetric relation is a denial inequality, and not every denial inequality is tight. Instead, every [[denial inequality]] is only [[weakly tight]]. Indeed, since excluded middle cannot be proven, we could distinguish between the following irreflexive symmetric relations in constructive mathematics:

* [[denial inequality]], an irreflexive symmetric relation $\neq$ which additionally satisfies $\neg(a = b)$ implies $(a \neq b)$

* [[tight]] irreflexive symmetric relation, an irreflexive symmetric relation $\neq$ which additionally satisfies $\neg(a \neq b)$ implies $(a = b)$

* [[weakly tight relation|weakly tight]] irreflexive symmetric relation, an irreflexive symmetric relation $\neq$ which additionally satisfies $\neg(a \neq b)$ implies $\neg \neg (a = b)$

* [[stable relation|stable]] irreflexive symmetric relation, an irreflexive symmetric relation $\neq$ which additionally satisfies $\neg \neg (a \neq b)$ implies $(a \neq b)$

* [[decidable relation|decidable]] irreflexive symmetric relation, an irreflexive symmetric relation $\neq$ which additionally satisfies $(a \neq b)$ or $\neg (a \neq b)$

* [[apartness relation]], an irreflexive symmetric relation $\neq$ which additionally satisfies $a \neq b$ implies that $a \neq c$ or $c \neq b$

or any combination of the above, such as [[tight apartness relation]]. 

The notion of "[[inequality relation]]" in constructive mathematics usually refers to either the [[denial inequality]] or a [[tight apartness relation]]. On the other hand, some authors have used "inequality relation" to refere to general irreflexive symmetric relations. 

## See also

* [[apartness relation]]
* [[inequality relation]]
* [[reflexive symmetric relation]]

[[!redirects irreflexive symmetric relation]]
[[!redirects irreflexive symmetric relations]]

[[!redirects tight irreflexive symmetric relation]]
[[!redirects tight irreflexive symmetric relations]]

[[!redirects weakly tight irreflexive symmetric relation]]
[[!redirects weakly tight irreflexive symmetric relations]]

[[!redirects stable irreflexive symmetric relation]]
[[!redirects stable irreflexive symmetric relations]]

[[!redirects decidable irreflexive symmetric relation]]
[[!redirects decidable irreflexive symmetric relations]]
