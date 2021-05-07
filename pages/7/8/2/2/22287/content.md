
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _two-valued type_ is an [[axiom|axiomatization]] of the [[two-valued object]] in the context of [[homotopy type theory]].

## Definition

As an [[inductive type]], the two-valued type is given by

    Inductive Two : Type
      | zero : Two
      | one : Two

This says that the type is inductively constructed from two [[terms]] in the type Two, whose [[semantics|interpretation]] is as the two points of the type; hence the name two-valued type.

## Boolean logic

The two-valued type is also called the type of [[boolean|booleans]]. One could recursively define the logical functions on $\mathbf{2}$ as follows

* For negation $\neg$
  * $\neg 0 := 1$
  * $\neg 1 := 0$
* For conjunction $\wedge$
  * $0 \wedge a := 0$
  * $1 \wedge a := a$
* For disjunction $\vee$
  * $0 \vee a := a$
  * $1 \vee a := 1$
* For implication $\implies$
  * $0 \implies a := 1$
  * $1 \implies a := a$

One could prove that $(\mathbf{2}, 0, 1, \neg, \wedge, \vee, \implies)$ form a [[Boolean algebra]]. The [[poset]] structure is given by implication.

A _boolean predicate_ valued in a type $T$ is a function $P: T \rightarrow \mathbf{2}$, and the type $T \to \mathbf{2}$ is a boolean [[function algebra]] for finite types $T$, and if [[path types]] exist, for all types $T$. Thus the [[functor]] $F: U \to BoolAlg$, $F(T) = T \to \mathbf{2}$ for a [[type universe]] $U$ is a [[Boolean hyperdoctrine]], and one could do [[classical logic|classical]] [[first-order logic]] inside $U$ if $\mathbf{2}$ and path types exist in $U$. 

In fact, just with [[dependent sum types]], [[dependent product types]], [[empty type]], [[unit type]], and the two-valued type in a type universe $U$, any [[two-valued logic]] could be done inside $U$. Furthermore, since binary [[disjoint coproducts]] exist when $\mathbf{2}$ exists, all finite types exist in $U$, and any [[finitely-valued logic]], such as the [[internal logic]] of a [[finite]] [[cartesian power]] of [[Set]], could be done inside $U$. 

## Properties

* A two-valued type is a [[suspension type]] of the [[empty type]], and the suspension of an two-valued type is a [[circle type]]. Geometrically, a two-valued type is a zero-dimensional sphere. 

## See also

* [[two-valued object]]
* [[two-valued logic]]