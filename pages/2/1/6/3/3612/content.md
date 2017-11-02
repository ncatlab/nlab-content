
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **Calculus of Constructions** (CoC) is a [[type theory]] [[formal system]] for [[constructive mathematics|constructive]] [[proof]] in [[natural deduction]] style.
This calculus goes back to [[Thierry Coquand]] and [[Gérard Huet]]

When supplemented by [[inductive types]], it become the __Calculus of Inductive Constructions__ (CIC).  Sometimes [[coinductive types]] are included as well and one speaks of the __Calculus of (co)inductive Constructions__. This is what the [[Coq]] software implements.

More in detail, the _Calculus of (co)Inductive Constructions_ is

1. a [[pure type system]], hence

   1. a system of [[natural deduction]] with [[dependent types]];

   1. with the natural-deduction rule for [[dependent product types]] specified;

1. with a rule for how to introduce new natural-deduction rules for arbitrary ([[coinductive type|co]])[[inductive types]].

1. and with [[universes]]:

   a cumulative hierarchy of [[predicative mathematics|predicative]] [[types of types]]

   and an impredicative [[type of propositions]].



All of the other standard [[type formation|type formations]] are subsumed by the existence of arbitrary inductive types, notably the _[[empty type]]_, _[[dependent sum types]]_ and _[[identity types]]_ are special inductive types. Specifying these hence makes the calculus of constructions be an [[intensional type theory|intensional]] [[dependent type theory]].

## Related concepts

* [[Coq]]

* [[computational type theory]]

## References

Original articles include

*  [[Thierry Coquand]], [[Gérard Huet]], _The Calculus of Constructions_ ([inria](http://hal.inria.fr/inria-00076024/en/), [pdf](http://hal.inria.fr/docs/00/07/60/24/PDF/RR-0530.pdf))

* M. Bunder, [[Jonathan Seldin]], _Variants of the basic calculus of constructions_ ([Cite Seer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.88.9497))

Surveys include

* Frade, _Calculus of inductive constructions_ ([pdf](http://www3.di.uminho.pt/~mjf/pub/SFV-CIC-2up.pdf))

* Wikipedia, _[Calculus of constructions](http://en.wikipedia.org/wiki/Calculus_of_constructions)_

A categorical semantics for CoC is discussed in

* [[Martin Hyland]], [[Andy Pitts]], _The Theory of Constructions: Categorical Semantics and Topos-theoretic Models_ , Cont. Math. **92** (1989) pp.137-199. ([draft](https://www.dpmms.cam.ac.uk/~martin/Research/Pub81-90/hp89.pdf))

For specifics of the implementation in [[Coq]] see

*  [[Coq]] manual, _[Calculus of Inductive Constructions](http://coq.inria.fr/doc/Reference-Manual006.html)_



[[!redirects calculus of inductive constructions]]
[[!redirects calculus of coinductive constructions]]
[[!redirects calculus of (co)inductive constructions]]
