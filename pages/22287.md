[[!redirects booleans type]]
[[!redirects type of booleans]]
[[!redirects decidable subset classifier]]

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

The two-valued type is also called the __booleans type__ or the __type of [[boolean|booleans]]__. One could recursively define the logical functions on $\mathbf{2}$ as follows

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
* For the biconditional $\iff$
  * $0 \iff a := \neg a$
  * $1 \iff a := a$

One could prove that $(\mathbf{2}, 0, 1, \neg, \wedge, \vee, \implies)$ form a [[Boolean algebra]]. The [[poset]] structure is given by implication.

One could also inductively define [[observational equality]] on the booleans $\mathrm{Eq}_\mathbb{2}(x, y)$ as an indexed inductive type on the boolean type $\mathbb{2}$ with the following constructors

$$\mathrm{eq}_0: \mathrm{Eq}_\mathbb{2}(0, 0)$$
$$\mathrm{eq}_1: \mathrm{Eq}_\mathbb{2}(1, 1)$$

A _boolean predicate_ valued in a type $T$ is a function $P: T \rightarrow \mathbf{2}$, and the type $T \to \mathbf{2}$ is a boolean [[function algebra]] for finite types $T$, and if [[path types]] exist, for all types $T$. Thus the [[functor]] $F: U \to BoolAlg$, $F(T) = T \to \mathbf{2}$ for a [[type universe]] $U$ is a [[Boolean hyperdoctrine]], and one could do [[classical logic|classical]] [[first-order logic]] inside $U$ if $\mathbf{2}$ and path types exist in $U$. 

In fact, just with [[dependent sum types]], [[dependent product types]], [[empty type]], [[unit type]], and the two-valued type in a type universe $U$, any [[two-valued logic]] could be done inside $U$. Furthermore, since binary [[disjoint coproducts]] exist when $\mathbf{2}$ exists, all finite types exist in $U$, and any [[finitely-valued logic]], such as the [[internal logic]] of a [[finite]] [[cartesian power]] of [[Set]], could be done inside $U$. 

For finite types, one could also inductively define specific functions 

$$\forall a \in A.(-)(a):(A \to \mathbf{2}) \to \mathbf{2}$$

$$\exists a \in A.(-)(a):(A \to \mathbf{2}) \to \mathbf{2}$$

from the type of boolean predicates on $A$ and $\mathbf{2}$ such that they behave like [[existential quantification]] and [[universal quantification]]. 

## Bi-pointed types

A __bi-pointed type__ is a type $A$ with a function $\mathbf{2}\to A$. Examples include the [[interval type]] and the [[function type]] of the [[natural numbers type]]. 

## Properties

* The two-valued type is the [[suspension type]] of the [[empty type]], and the suspension of the two-valued type is the [[circle type]]. Geometrically, the two-valued type is a zero-dimensional sphere. 

* The two-valued type is [[homotopy equivalent]] to the type of [[decidable propositions]] in a universe $\mathcal{U}$. 

$$\mathbb{2} \cong \sum_{P:\mathcal{U}} isProp(P) \times isDecidable(P)$$

As a result, sometimes the two-valued type is called a __decidable subset classifier__. 

## See also

* [[two-valued object]]
* [[two-valued logic]]

## References ##

For discussion of booleans types in the context of [[homotopy type theory]]:

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

[[!redirects bi-pointed type]]