
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

In dependent type theories with a separate [[proposition]] [[judgment]] $\phi \mathrm{prop}$, the term *typal equality* is also used to distinguish identity types from [[propositional equality]], which is the equality judged to be a proposition; i.e. $a =_A b \mathrm{prop}$. On the other hand, in dependent type theory without a separate [[proposition]] [[judgment]], propositions are usually defined to be certain types, and the term "propositional equality" is used as a synonym of typal equality in referring to identity types.  (In fact, "propositional equality" is the older and arguably still more common term in this context.)

In [[dependent type theory with type variables]] and [[identity type#IdentityTypesBetweenTypes|identity types between types]], in the absence of the [[univalence axiom]], the term *typal equality* is also used for types to distinguish between when two types are typally equal via the identity type between the two types and when two types are equivalent to each other. 

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

## See also

* [[judgmental equality of terms]]
* [[propositional equality]]

[[!redirects typal equality]]
[[!redirects typally equal]]