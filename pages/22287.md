
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

The two-valued type is sometimes called the type of [[boolean|booleans]], but the word 'boolean' more often is a synonym of a [[truth value]] or [[proposition]], which has only two values in classical logic, and the type of truth values or the [[type of propositions]] has additional structure to it, such as that of a Heyting or Boolean algebra. 

## Properties

* A two-valued type is a [[suspension type]] of the [[empty type]], and the suspension of an two-valued type is a [[circle type]]. Geometrically, a two-valued type is a zero-dimensional sphere. 

## See also

* [[two-valued object]]