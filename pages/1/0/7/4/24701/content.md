+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A [[dependent type theory]] without [[definitional equality]]. 

This means that the computation rules ([[beta-reduction]] and [[eta-conversion]]) for each type in the type theory are all propositional computation rules using the [[identity type]], and in particular means that the identity type has to be introduced first before any other type is introduced. 

Objective type theory has [[decidable]] [[type checking]], and the type checking can be done in quadratic time. 

## Open problems

There are plenty of questions which are currently unresolved in objective type theory. Van der Berg and Besten in particular listed the following problems in their article:

* Does [[univalence]] imply [[function extensionality]] in [[objective type theory]]?

* Is [[Martin-Löf type theory]] conservative over [[objective type theory]]?

* How much of the [[HoTT book]] could be done in [[objective type theory]]?

* Does [[objective type theory]] have [[homotopy canonicity]] and [[normalization]]?

See also [[open problems in homotopy type theory]]

## Categorical semantics

Objective type theory can be interpreted in any [[path category]] with weak homotopy $\Pi$-types. 

## See also

* [[definitional equality]], [[identity type]]

* [[dependent type theory]], [[Martin-Löf type theory]], [[homotopy type theory]]

## References

* [[Benno van den Berg]], [[Martijn den Besten]], *Quadratic type checking for objective type theory* ([arXiv:2102.00905](https://arxiv.org/abs/2102.00905))