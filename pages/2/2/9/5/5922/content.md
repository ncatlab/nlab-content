
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

An _axiom_ is a [[proposition]] in [[logic]] that a given [[theory]] requires to be [[true]]: every [[model]] of the theory is required to make the axiom hold true. The sense however is that an axiom is a _basic_ true proposition, used to prove other true propositions (the [[theorems]]) in the theory. 


## Definition

Given a [[language]] $L$ (perhaps specified by a [[signature (in logic)|signature]]: a collection of [[types]], [[function symbols]] and [[relation symbols]]), a [[theory]] is the collection of assertions which are derivable (using the rules of [[deduction]] of the ambient [[logic]] or [[deductive system]]) from a given set of assertions, called **axioms** of the theory.  In other words, a theory is generated from a set of axioms, by starting with those axioms and applying [[rule of inference|rules of deduction]], much as terms in an algebraic system may be generated from a set of basic terms by applying operations. Axioms should therefore be considered as _presenting_ a theory; different axiom sets may well give the same theory. 

In terms of a [[deductive system]], axioms can be regarded as "rules with zero hypotheses".  The form of such axioms depends on the details of the deductive system used: it could be [[natural deduction]], [[sequent calculus]], a [[Hilbert system]], etc.  If we take sequent calculus, for instance, then any collection of [[sequents]] written in the given language $L$

$$
  \vec{\phi} \vdash_{\vec x} \vec{\psi}
$$

(asserting that "If every [[proposition]] $\phi_i$ is [[true]] in [[context]] $\vec{x}$ then also some $\psi_i$ is/has to be true") can be taken as a collection of axioms for some theory. [[model|Models]] of the theory will then be those [[structure in model theory|structures]] of the language in which the axioms are interpreted as true statements. For example, a model of [[group theory]] is a structure in the language of groups for which the group theory axioms hold, which is (of course) a [[group]]. 

Assuming the deductive system is [[soundness theorem|sound]], every sequent which is the conclusion of a valid sequent deduction, starting from the axioms, will also be true in every model. And if the deductive system is also [[completeness theorem|complete]], then every sequent of the language which is true in every model will in fact be provable from the axioms. 

## Examples
 {#Examples}

* In [[polymorphic dependent type theory]], many axioms are represented by a type-indexed family of terms. 

[[!include foundational axiom - contents]]


(...)

* [[pushout-product axiom]]

(...)

* [[Hilbert's sixth problem]] asks for an axiomatization of [[physics]].

## Related concepts

* [[axiom schema]]


[[!include mathematical statements --- contents]]




## References

For instance def. D1.1.6 in 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_


[[!redirects axiom]]
[[!redirects axioms]]

[[!redirects axiomatization]]
[[!redirects axiomatizations]]


category: logic