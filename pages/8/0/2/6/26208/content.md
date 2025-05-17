
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

The notion of [[dependent type theory]] where all the [[computation rules]] and [[uniqueness rules]] for types use [[identity types]] instead of [[definitional equality]]. As a result, the results in the dependent type theory are more general than in models which use judgmental equality for computational and uniqueness rules, since judgmental equality implies typal equality, while the converse isn't necessarily the case. 

These dependent type theories come into two general versions:

* Dependent type theories which do not have judgmental [[definitional equality]]. Instead, [[definitions]] of [[types]] and [[terms]] are made using [[identifications]] or [[equivalences of types]]. This is called *[[objective type theory]]*, *[[propositional type theory]]*, or *[[weak type theory]]*. Any judgmental equality $\equiv$ in the theory represents [[alpha-equivalence|$\alpha$-equivalence]] or [[syntactic equality]], where the usual [[structural rules]] and [[congruence rules]] are [[admissible rules]].  

* Dependent type theories which do have judgmental [[definitional equality]], and thus definitions of [[types]] and [[terms]] are still made using [[judgmental equality]]. The [[structural rules]] and [[congruence rules]] for judgmental equality are no longer admissible, so have to be postulated explicitly in the theory like in the usual dependent type theories. In addition to the [[congruence rules]] for [[judgmental equality]] for the [[formation rules]], [[introduction rules]], and [[elimination rules]] of each type former, there are additional [[congruence rules]] for the computation and uniqueness rules, since the conversion rules are represented by the structure of an identification rather than judgmental equality, and thus this structure has to be preserved across judgmental equality. 

The latter includes versions of [[Martin-Löf type theory]], [[cubical type theory]], and [[observational type theory]] with only propositional computation rules, as well as extensions thereof such as [[type theory with shapes]] and [[simplicial type theory]]. 

## See also

* [[dependent type theory]]

* [[objective type theory]]

## References

* [[Matteo Spadetto]], *Relating homotopy equivalences to conservativity in dependendent type theories with propositional computation* ([arXiv:2303.05623](https://arxiv.org/abs/2303.05623))

[[!redirects dependent type theory with propositional computation]]
[[!redirects dependent type theories with propositional computation]]

[[!redirects dependent type theory with propositional computation rules]]
[[!redirects dependent type theories with propositional computation rules]]

[[!redirects dependent type theory with typal computation]]
[[!redirects dependent type theories with typal computation]]

[[!redirects dependent type theory with typal computation rules]]
[[!redirects dependent type theories with typal computation rules]]