
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

## Disambiguation

There are in general two ways to define a [[dependent type theory]]:

* One approach assumes a single separate type judgment and defines types via the single type judgment. 

* A second approach assumes an infinite number of universe levels $i$ and then defines an infinite number of [[type universes]] and, in the case for [[Coquand universes]], type judgments indexed by $i$, whereby types are then [[terms]] of the universes for [[Russell universes]] or identified with terms of the universes for [[Coquand universes]] via [[judgmental isomorphisms]]. 

These two ways to define a dependent type theory leads to many different ways to make a dependent type theory [[impredicative mathematics|impredicative]]. We assume throughout that there are some notion of [[dependent sum types]], [[dependent product types]], and [[identity types]]/[[path types]]. 

* For dependent type theories in the first sense, an **impredicative dependent type theory** is a dependent type theory with a [[type of all propositions]] defined via [[natural deduction]] [[inference rules]]. These dependent type theories are [[higher-order logics]] and are the [[internal logics]] of (the [[(infinity,1)-category theory|$(\infty, 1)$-categorical]] analogues of) [[elementary toposes]]. In general, (the [[(infinity,1)-category theory|$(\infty, 1)$-categorical]] analogues of) elementary toposes do not have any [[object classifiers]]. 

* For dependent type theories in the second sense, there are multiple notions of **impredicative dependent type theory**, including [[propositional resizing]] and [[impredicative polymorphism]]: 

  * For impredicative dependent type theory in the sense of a dependent type theory which has the [[propositional resizing axiom]]; these impredicative dependent type theories are stronger than the notion of impredicative dependent type theory using a single type judgment since these are the [[internal logics]] of [[(infinity, 1)-category|$(\infty, 1)$-categories]] with an infinite number of [[inaccessible cardinal|inaccessible]] [[object classifiers]]. 

  * For impredicative dependent type theory in the sense of a [[dependent type theory]] for which the base universe $U_0$ satisfies [[impredicative polymorphism]]; these impredicative type theories are also stronger than the notion of impredicative dependent type theory using a single type judgment since one can prove that [[excluded middle]] is [[false]]. 

category: disambiguation

[[!redirects impredicative type theory]]
[[!redirects impredicative type theories]]

[[!redirects impredicative dependent type theory]]
[[!redirects impredicative dependent type theories]]
