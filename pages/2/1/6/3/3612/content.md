
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

When supplemented by [[inductive types]], it become the __Calculus of Inductive Constructions__ (CIC).  Sometimes [[coinductive types]] are included as well and one speaks of the __Calculus of (co)inductive Constructions__. This is what the [[Rocq]] software implements.

More in detail, the _Calculus of (co)Inductive Constructions_ is

1. a [[pure type system]], hence

   1. a system of [[natural deduction]] with [[dependent types]];

   1. with the natural-deduction rule for [[dependent product types]] specified;

1. with a rule for how to introduce new [[natural deduction]] [[inference rules]] for arbitrary ([[coinductive type|co]])[[inductive types]].

1. and with [[type universes]]:

   a cumulative hierarchy of [[predicative mathematics|predicative]] [[types of types]]

   and an impredicative [[type of propositions]].



All of the other standard [[type formation|type formations]] are subsumed by the existence of arbitrary inductive types, notably the _[[empty type]]_, _[[dependent sum types]]_ and _[[identity types]]_ are special inductive types. Specifying these hence makes the calculus of constructions be an [[intensional type theory|intensional]] [[dependent type theory]].

## Related concepts

* [[initiality conjecture]]

* [[Rocq]]

* [[computational type theory]]

## References

### General

Original articles:

*  [[Thierry Coquand]], [[Gérard Huet]], _The Calculus of Constructions_, INRIA Rapport **530** (1986) &lbrack;[inria:00076024](http://hal.inria.fr/inria-00076024/en/), [pdf](http://hal.inria.fr/docs/00/07/60/24/PDF/RR-0530.pdf)&rbrack;

* [[Christine Paulin-Mohring]], *Inductive definitions in the system Coq -- Rules and Properties*, in: *Typed Lambda Calculi and Applications* TLCA 1993, Lecture Notes in Computer Science **664** Springer (1993) &lbrack;[doi:10.1007/BFb0037116](https://doi.org/10.1007/BFb0037116)&rbrack;

  > (adding [[inductive types]])


Review and surveys:

* [[Zhaohui Luo]], *Computation and Reasoning -- A Type Theory for Computer Science*, Clarendon Press (1994) $[$[ISBN:9780198538356](https://global.oup.com/academic/product/computation-and-reasoning-9780198538356), [pdf](https://www.researchgate.net/profile/Zhaohui-Luo-4/publication/243770570_Computation_and_Reasoning_A_Type_Theory_for_Computer_Science/links/54d0dc6b0cf29ca81103f26a/Computation-and-Reasoning-A-Type-Theory-for-Computer-Science.pdf)$]$

* M. Bunder, [[Jonathan Seldin]], *Variants of the basic calculus of constructions*, Journal of Applied Logic
**2** 2 (2004) 191-217 &lbrack;[doi:10.1016/j.jal.2004.02.004](https://doi.org/10.1016/j.jal.2004.02.004)&rbrack;

* [[Christine Paulin-Mohring]], *Introduction to the Calculus of Inductive Constructions*, contribution to: *Vienna Summer of Logic* (2014) &lbrack;[hal:01094195](https://hal.inria.fr/hal-01094195), [pdf](https://hal.inria.fr/hal-01094195/document), [pdf slides](https://easychair.org/smart-program/VSL2014/APPA-invited-slides-6.pdf)&rbrack;


* Frade, _Calculus of inductive constructions_ ([pdf](http://www3.di.uminho.pt/~mjf/pub/SFV-CIC-2up.pdf))

* Wikipedia, _[Calculus of constructions](http://en.wikipedia.org/wiki/Calculus_of_constructions)_

A [[categorical semantics]] for CoC is discussed in

* [[Martin Hyland]], [[Andy Pitts]], _The Theory of Constructions: Categorical Semantics and Topos-theoretic Models_ , Cont. Math. **92** (1989) pp.137-199. ([draft](https://www.dpmms.cam.ac.uk/~jmeh1/Research/Pub81-90/hp89.pdf))

For specifics of the implementation in [[Coq]] see

*  [[Coq]] manual, _[Calculus of Inductive Constructions](http://coq.inria.fr/doc/Reference-Manual006.html)_



[[!include history of inductive types -- references]]









[[!redirects calculus of inductive constructions]]
[[!redirects calculus of coinductive constructions]]
[[!redirects calculus of (co)inductive constructions]]
