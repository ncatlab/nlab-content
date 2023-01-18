
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[two-level type theory]], there are also two different kinds of judgments, one for the types representing the metatheory, and one for the types representing the object theory. In [[typed predicate logic]], there are two different kinds of judgments, one for [[types]] and one for [[propositions]]. In [[type theory with shapes]], there are three different kinds of judgments, one for cubes, one for topes, and one for types, where the subtheory of cubes and topes together form a predicate logic over a type theory with finite product types. Examples of [[type theory with shapes]] include certain presentations of [[simplicial type theory]] and [[cubical type theory]]. Independently, [[cubical type theory]] could be considered as a type theory over a typed predicate logic with only one type, where the single type in the predicate logic is called the "interval" and the propositions in the predicate logic layer are called "face formulas". 

Thus, one could think of the different judgments as forming different **layers** of the type theory, and these type theories as **layered type theory**. 

Some layered type theories have [[split contexts]], in which the contexts (and associated judgments) sit in a sequential hierarchy: for example, in two-level type theory, the [[types]] in the object theory can depend upon [[variables]] in the metatheory, but the types in the metatheory cannot depend upon variables in the object theory. 

Layered type theories could be contrasted with theories like the usual presentations of [[Martin-Löf type theory]] and [[higher observational type theory]], which only have one layer and thus are considered to be **unlayered type theory**. 

## Examples

* [[typed predicate logic]]
* [[two-level type theory]]
* [[type theory with shapes]]
* [[simplicial type theory]]
* [[cubical type theory]]
* Any dependent type theory with an infinite sequential hierarchy of [[Russell universes]] but no separate type judgment. This includes [[book HoTT]], the theory presented in the [[HoTT book]]. The Russell universes are indexed by the [[natural numbers]], which have to be provided as a primitive in a separate layer specifically containing the natural numbers.

## References

The notion of layer of a type theory appears in

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

when defining [[type theory with shapes]] and [[simplicial type theory]]. 

The term "layered type theory" also appears in 

* César Bardomiano Martínez, *Limits and colimits of synthetic $\infty$-categories* $[$[arXiv:2202.12386](https://arxiv.org/abs/2202.12386)$]$

[[!redirects layer]]
[[!redirects layers]]