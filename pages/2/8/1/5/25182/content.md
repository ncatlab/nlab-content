
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

* The [[propositions as types]] interpretation, which says that all types are propositions. The term "propositional equality" is used as a synonym of typal equality in referring to [[identifications]] or [[identity types]]. In the presence of [[univalence]], all [[equivalences of types]] are equivalent to propositional equalities. 

* The [[propositions as some types]] interpretation, which says that only the [[subsingletons]] or [[h-propositions]] are propositions. The term "propositional equality" in this interpretation is not a synonym of typal equality in referring to [[identifications]] or [[identity types]]. Instead, "propositional equality" is used to refer to a [[unique]] [[identification]] or the [[proposition]] representing whether the [[identity type]] is [[contractible]], coinciding with the usual notion of [[propositional equality]] found elsewhere in mathematics, where equalities are unique (see e.g. [Buzzard 2024](#Buzzard24)). In the presence of [[univalence]], the [[unique]] [[equivalences of types]] are equivalent to propositional equalities. 

In this second sense, if all identifications in an [[identity type]] are unique (i.e. $\mathrm{Id}_A(x, y) \to \mathrm{isContr}(\mathrm{Id}_A(x, y)$), then the identity type is an [[h-proposition]], and if the identity type is an [[h-proposition]], then all identifications in the identity type are unique; hence the name *[[propositional equality]]* for unique identifications. 

If one assumes [[uniqueness of identity proofs]] or another [[axiom of set truncation]], then typal equality and propositional equality will coincide again regardless of which interpretation one uses, because then all identity types are propositions and all identifications are unique. 

However, propositional equality defined in the second sense is not necessarily a [[reflexive relation]]. The only such types with a reflexive propositional equality are [[h-sets]]: those that satisfy [[axiom K]] $\mathrm{isContr}(\mathrm{Id}_A(x, x))$ for all $x:A$. 

Most homotopy type theorists work in a dependent type theory without a separate prop judgment and use a mix of both interpretations of propositions, with the [[propositions as types]] interpretation of [[propositional equality]] as a synonym of [[typal equality]] being used by the vast majority of homotopy type theorists, even by those who use the [[propositions as some types]] interpretation for everything else. [[Kevin Buzzard]] in [Buzzard 2024](#Buzzard24) has used this fact and how that contradicts the interpretation of [[propositional equality]] elsewhere in mathematics as an argument for adopting a [[set-level type theory]] instead of [[homotopy type theory]]. 

By Buzzard's argument, homotopy type theorists should not be using the term "equality" to refer to arbitrary identifications or identity types, whether in its bare form or as "[[typal equality]]" or "[[propositional equality]]", instead restricting the use of equality / [[propositional equality]] for only the unique identifications, and using a suitable alternative for "typal equality", such as "[[identification]]" and "[[identified]]" and "[[identity type]]". On the other hand, the fact that [[propositional equality]] defined as having a unique identification is not a [[reflexive relation]] for non-set types means that perhaps it is not suitable for the bare term "equality", and perhaps the bare term "equality" and even the term "propositional equality" *should* refer to [[typal equality]] which is always reflexive. Either way, it seems that in the absence of [[uniqueness of identity proofs]], one has to give up either the notion of propositional equality as unique identification or the notion of propositional equality as a reflexive relation. 

### In logic over dependent type theory

In [[logic over dependent type theory]], the term *typal equality* is used to distinguish identity types from [[propositional equality]], which is the equality judged to be a proposition; i.e. $a =_A b \mathrm{prop}$. 

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