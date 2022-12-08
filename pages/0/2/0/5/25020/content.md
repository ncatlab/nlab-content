
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

## Definition

An **reflexive symmetric relation** is a [[binary relation]] that is [[reflexive relation|reflexive]] and [[symmetric relation|symmetric]]. 

## Examples

* Every [[equivalence relation]] is an reflexive symmetric relation which is also a [[transitive relation]]. 

* The negation of a [[irreflexive symmetric relation]] is a reflexive symmetric relation. 

* The [[double negation]] of every [[equivalence relation]] is an irreflexive symmetric relation. In [[constructive mathematics]], this is not guaranteed to be transitive. 

## In constructive mathematics
 {#ConstructiveMathematics}

In constructive mathematics, the [[double negation]] of [[equality]] cannot in general be proven to be an [[equivalence relation]], because the [[denial inequality]] cannot be proved to be an [[apartness relation]]. Instead, the double negation of equality is only a stable reflexive symmetric relation. Indeed, since excluded middle cannot be proven, we could distinguish between the following reflexive symmetric relations in constructive mathematics:

* [[equality]]

* [[equivalence relations]], a transitive reflexive symmetric relation

* [[double negation]] of [[equality]]

* [[stable relation|stable]] reflexive symmetric relation, a reflexive symmetric relation $\approx$ which additionally satisfies $\neg \neg (a \approx b)$ implies $a \approx b$

* [[decidable relation|decidable]] reflexive symmetric relation, an reflexive symmetric relation $\approx$ which additionally satisfies $(a \approx b)$ or $\neg (a \approx b)$

## See also

* [[double negation]]
* [[irreflexive symmetric relation]]
* [[equivalence relation]]

[[!redirects reflexive symmetric relation]]
[[!redirects reflexive symmetric relations]]

[[!redirects stable reflexive symmetric relation]]
[[!redirects stable reflexive symmetric relations]]

[[!redirects decidable reflexive symmetric relation]]
[[!redirects decidable reflexive symmetric relations]]