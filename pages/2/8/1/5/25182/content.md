
> This article is about the notion of [[equality]] as a [[type]]. For [[equality]] as a [[proposition]] or [[predicate]], see [[propositional equality]]. For [[equality]] as a [[judgment]], see [[judgmental equality]]. For other notions of equality, see [[equality]]. 

---

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


\tableofcontents

## Idea

In [[dependent type theory]], the term *typal equality* is used to describe the use of the [[identity type]] to represent the notion of equality of terms, and is primarily used to distinguish from the notion of [[judgmental equality of terms]]. 

In [[dependent type theory with type variables]] and [[identity type#IdentityTypesBetweenTypes|identity types between types]], in the absence of the [[univalence axiom]], the term *typal equality* is also used for types to distinguish between when two types are typally equal via the identity type between the two types and when two types are equivalent to each other. 

## Relation to propositional equality

### In dependent type theory

In [[dependent type theory]] without a separate [[proposition]] [[judgment]], there are two different interpretations of [[propositions]] and thus [[propositional equality]]: 

* The [[propositions as types]] interpretation, which says that all types are propositions. The term *propositional equality* is used as a synonym of typal equality in referring to [[identifications]] or [[identity types]]. In the presence of [[univalence]], all [[equivalences of types]] are equivalent to propositional equalities. 

* The [[propositions as some types]] interpretation, which says that only the [[subsingletons]] or [[h-propositions]] are propositions. The term *propositional equality* in this interpretation is not a synonym of typal equality and only refers to the [[contractible type|unique]] [[identifications]] or the [[h-proposition]] valued [[identity types]]. 

Most homotopy type theorists work in a dependent type theory without a separate prop judgment and use a mix of both interpretations of propositions, with the [[propositions as types]] interpretation of [[propositional equality]] as a synonym of [[typal equality]] being used by the vast majority of homotopy type theorists, even by those who use the [[propositions as some types]] interpretation for everything else. [[Kevin Buzzard]] in [Buzzard 2024](#Buzzard24) has used this fact and how that contradicts the interpretation of [[propositional equality]] elsewhere in mathematics as an argument for adopting a [[set-level type theory]] instead of [[homotopy type theory]]. 

By Buzzard's argument, homotopy type theorists should not be using the term "equality" to refer to arbitrary identifications or identity types, whether in its bare form or as "[[typal equality]]" or "[[propositional equality]]", instead restricting the use of equality / [[propositional equality]] for only the [[contractible type|unique]] [[identifications]] and the [[h-proposition]] valued [[identity types]], and using a suitable alternative for "typal equality", such as "[[identification]]" and "[[identified]]" and "[[identity type]]". 

### In logic over dependent type theory

In [[logic over dependent type theory]], the term *typal equality* is also used to distinguish identity types from the external notion of [[propositional equality]], which is the equality judged to be a proposition; i.e. $a =_A b \mathrm{prop}$, in addition to the usual internal notion of propositional equality as a [[mere proposition]] valued [[identity type]]. 

## Parallels between judgmental equality and typal equality

The parallels between the structural rules for judgmental equality and typal equality in [[dependent type theory with type variables]] are shown below:

| judgmental equality | typal equality |
|---------------------|----------------|
| judgmental equality of terms | identification between terms |
| reflexivity of judgmental equality of terms | identity identification between terms |
| symmetry of judgmental equality of terms | inverse identification between terms |
| transitivity of judgmental equality of terms | concatenation of identifications between terms |
| judgmental equality of types | identification between types |
| reflexivity of judgmental equality of types | identity identification between types |
| symmetry of judgmental equality of types | inverse identification between types |
| transitivity of judgmental equality of types | concatenation of identification between types |
| principle of substitution | action on identifications |

## Related concepts

* [[judgmental equality of terms]]
* [[propositional equality]]

## References

* {#Buzzard24} [[Kevin Buzzard]], *Grothendieck's use of equality* ([arXiv:2405.10387](https://arxiv.org/abs/2405.10387))

[[!redirects typal equality]]
[[!redirects typally equal]]