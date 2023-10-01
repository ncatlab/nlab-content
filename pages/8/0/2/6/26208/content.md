
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

**Weak type theory** or **propositional type theory** is a [[dependent type theory]] without judgmental conversion; all the [[computation rules]]/[[beta-conversion|$\beta$-conversion rules]] and [[uniqueness rules]]/[[eta-conversion|$\eta$-conversion rules]] for types use [[identity types]] instead of [[judgmental equality]]. As a result, the results in weak type theory are more general than in models which use judgmental equality for computational and uniqueness rules, since judgmental equality implies typal equality, while the converse isn't necessarily the case. 

In formal presentations of weak type theories, the [[identity type]] has to be introduced at the same time the [[dependent function type]] is introduced, since the computation rules for one relies on the existence of the other. 

Formally, weak type theories come into two general versions:

* Dependent type theories which do not have judgmental equality and its [[structural rules]]. Instead, [[definitions]] of [[types]] and [[terms]] are made using [[identifications]] or [[equivalences of types]]. See [[objective type theory]] for more details on this. 

* Dependent type theories which do have judgmental equality and its [[structural rules]], and thus definitions of [[types]] and [[terms]] are still made using [[judgmental equality]]. However, in addition to the [[congruence rules]] for [[judgmental equality]] for the [[formation rules]], [[introduction rules]], and [[elimination rules]] of each type former, there are additional [[congruence rules]] for the computation and uniqueness rules, since the conversion rules are represented by the structure of an identification rather than judgmental equality, and thus this structure has to be preserved across judgmental equality. 

The latter includes weak versions of [[Martin-Löf type theory]], [[cubical type theory]], and [[observational type theory]], as well as extensions thereof such as [[type theory with shapes]] and [[simplicial type theory]]. Hypothetically, the latter would also be seen in [[proof assistants]], where the base [[programming language]] used to implement the weak type theory, such as [[Coq]] or [[Agda]], already has a judgmental equality. 

A hybrid of weak and non-weak type theories can occur in [[two-level type theory]] and variants thereof like [[Homotopy Type System]], where one level has weak types and the other one has strict types. 

## Open problems

There are plenty of questions which are currently unresolved in weak type theory. Van der Berg and Besten listed the following problems in the context of [[objective type theory]], but equally this applies to any weak type theory:

* Does [[univalence]] imply [[function extensionality]] for types in the universe in [[weak type theory]]?

* Is (the [[homotopy type theory]] based upon) [[Martin-Löf type theory]] conservative over (the [[homotopy type theory]] based upon) [[weak type theory|weak]] Martin-Löf type theory?

* How much of the [[HoTT book]] could be done in [[weak type theory]]?

* Does [[weak type theory]] have [[homotopy canonicity]] and [[normalization]]?

Other problems include

* What is the [[categorical semantics]] of the [[homotopy type theory]] based upon [[weak type theory]], with all [[higher inductive types]] and [[weakly Tarski]] [[univalent universes]]? 

* Is [[weak function extensionality]] equivalent to [[function extensionality]] in [[weak type theory]]?

* Does [[product extensionality]] hold in [[weak type theory]]? Namely, given types $A$ and $B$ and elements $a:A \times B$ and $b:A \times B$, is the canonical function $\mathrm{idtoprojectionids}:(a =_{A \times B} b) \to (\pi_1(a) \simeq \pi_1(b)) \times (\pi_2(a) \simeq \pi_2(b))$ an [[equivalence of types]]?

* Is [[function extensionality]] still provable in weak [[cubical type theory]]?

See also [[open problems in homotopy type theory]]

## See also

* [[dependent type theory]]

## References

The original paper on weak type theory, in the context of [[objective type theory]]:

* {#BB21} [[Benno van den Berg]], [[Martijn den Besten]], *Quadratic type checking for objective type theory* ([arXiv:2102.00905](https://arxiv.org/abs/2102.00905))

Talks at Strength of Weak Type Theory, hosted by [[DutchCATS]]:

* [[Daniël Otten]], *Models for Propositional Type Theory*, 11 May 2023. ([slides](https://dutchcats.github.io/Weak_type_theories/slides_otten.pdf))

* [[Théo Winterhalter]], *A conservative and constructive translation from extensional type theory to weak type theory*, 11 May 2023. ([slides](https://dutchcats.github.io/Weak_type_theories/slides_winterhalter.pdf))

* [[Sam Speight]], *Higher-Dimensional Realizability for Intensional Type Theory*, 11 May 2023. ([slides](https://dutchcats.github.io/Weak_type_theories/slides_speight.pdf))

* [[Matteo Spadetto]], *Weak type theories: a conservativity result for homotopy elementary types*, 12 May 2023. ([slides](https://dutchcats.github.io/Weak_type_theories/slides_spadetto.pdf))

* [[Benno van den Berg]], *Towards homotopy canonicity for propositional type theory*, 12 May 2023. ([slides](https://dutchcats.github.io/Weak_type_theories/slides_van_den_berg.pdf))

* [[Rafaël Bocquet]], *Towards coherence theorems for equational extensions of type theories*, 12 May 2023. ([slides](https://dutchcats.github.io/Weak_type_theories/slides_bocquet.pdf))

Project to convert [[extensional type theory]] to [[weak type theory]]:

* Github, [ett-to-wtt](https://github.com/TheoWinterhalter/ett-to-wtt)

[[!redirects propositional type theory]]
[[!redirects propositional type theories]]
[[!redirects weak type theory]]
[[!redirects weak type theories]]