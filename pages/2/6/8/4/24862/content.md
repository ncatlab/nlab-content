
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

In [[typed predicate logic]], there are two different kinds of judgments and contexts, one for [[types]] and one for [[propositions]]. In [[two-level type theory]], there are also two different kinds of judgments and contexts, one for the types representing the metatheory, and one for the types representing the object theory. In [[type theory with shapes]], there are three different kinds of judgments and contexts, one for cubes, one for topes, and one for types, where the subtheory of cubes and topes together form a predicate logic over a type theory with finite product types. Examples of [[type theory with shapes]] include certain presentations of [[simplicial type theory]] and [[cubical type theory]]. Independently, [[cubical type theory]] could be considered as a type theory over a typed predicate logic with only one type, where the single type in the predicate logic is called the "interval" and the propositions in the predicate logic layer are called "face formulas". 

Furthermore, each of these judgments and contexts sit in a sequential hierarchy: for example, in two-level type theory, the [[types]] in the object theory can depend upon [[variables]] in the metatheory, but the types in the metatheory cannot depend upon variables in the object theory. Similarly, while propositions in typed predicate logic can depend upon variables in a type, traditionally, there is no such notion of variable in a proposition. Thus, one could think of the different judgments and contexts as sitting in different **layers** of the type theory, and these type theories as **layered type theory**. 

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

[[!redirects layer]]
[[!redirects layers]]