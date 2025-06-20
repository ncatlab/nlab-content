[[!redirects Algebraic set theory]]

#Contents#
* table of contents
{:toc}

## Idea

The new insight taken as a starting point in _algebraic set theory_ (AST) is that [[models]] of [[set theory]] are in fact [[algebra over an algebraic theory|algebras]] for a suitably presented [[algebraic theory]], and that many familiar [[set theory|set-theoretic]] conditions (such as well-foundedness) are thereby related to familiar algebraic ones (such as [[free functor|freeness]]). ([Awodey](#Awodey))


##Description of the project##

Also sometimes called _categorical_ (meaning category-theoretic) _set theory_, _algebraic set theory_ started to be developed in 1988 by [[André Joyal]] and [[Ieke Moerdijk]] and was first presented in detail as a book in 1995 by them. AST is a robust framework based on [[category theory]] to study and organize [[set theory|set theories]] and to construct [[model of a set theory|models of set theories]]. The aim of AST is to provide a uniform categorical semantics or description of set theories of different kinds (classical or [[constructive mathematics|constructive]]; bounded, [[predicative mathematics|predicative]] or impredicative; [[well-founded set|well founded]] or ill founded, ...), the various constructions of the [[von Neumann hierarchy|cumulative hierarchy]] of [[pure set]]s, [[forcing]] models, [[sheaf]] models and [[realizability|realisability]] models.

Instead of focusing on categories of sets AST focuses on categories of [[class]]es. The basic tool of AST is the notion of a [[category with class structure]] (a category of classes equipped with a class of small maps (the intuition being that their fibres are small in some sense), powerclasses and a [[universe|universal object]]) which provides an axiomatic framework in which models of set theory can be constructed. The notion of a class category permits both the definition of [[Zermelo-Fraenkel algebra|ZF-algebras]] and related structures expressing the idea that the hierarchy of sets is an algebraic structure on the one hand and the interpretation of the first order logic of elementary set theory on the other. The subcategory of sets in a class category is an [[topos|elementary topos]] and every elementary topos occurs as the topos of sets in some class category.

The class category itself always embeds into the [[ideal completion]] of a topos. The interpretation of the logic is that in every class category the universe is a model of basic intuitionistic set theory $\mathbf{BIST}$ that is logically [[complete model|complete]] with respect to class category models. Therefore class categories generalize both topos theory and intuitionistic set theory. AST founds and formalizes set theory on the ZF-algebra with operations union and successor (singleton) instead of on the membership relation. The [[ZFC|ZF axioms]] are nothing but a description of the free ZF-algebra just as the [[natural numbers object|Peano axioms]] are a description of the free [[monoid]] on one generator. In this perspective the models of set theory are algebras for a suitably presented [[algebraic theory]]. Using an auxiliary notion of small map it is possible to extend the axioms of a topos and provide a general theory for uniformly constructing models of set theory out of toposes.


##Naming##

There are two reasons for referring to this research as "algebraic set theory": The first reason is that the models of set theory that are produced by these methods are algebras for an abstractly presented "theory", in a precise, technical sense known to category theorists as a [[monad]]. The notion of an algebra for a monad subsumes and generalizes that of a model for a conventional algebraic theory, such as groups, rings, modules, etc. Indeed, the first significant work in this style on the applications of [[category theory]] to the study of [[set theory]] was the monograph ([Joyal-Moerdijk 1995](#JoyalMoerdijk)) _Algebraic set theory_. 

The second reason is that we believe the locution "algebraic logic" should properly refer to categorical logic rather than just the logic of Boole and his modern proponents, since categorical logic subsumes such lattice theoretic methods and not the other way around. Hence the term "algebraic set theory" rather than "categorical set theory". This is in keeping with the use of "algebraic" to mean, essentially, "functorial" in modern algebraic topology, algebraic geometry, etc. (Awodey, [Why "algebraic set theory"?](http://www.phil.cmu.edu/projects/ast/whyast.html))

### Stack semantics
[[michaelshulman:stack semantics]] provides a structural and somewhat more uniform way of treating "classes" in [[topos]] theory.

## See also

* [[category of classes]]

* [[category with class structure]]

## References

Introductions and further pointers are at

* [Algebraic Set Theory Website](http://www.phil.cmu.edu/projects/ast/index.html)

Two introductions are: 

* [[Steve Awodey]], _An Outline of Algebraic Set Theory_ ([archived pdf](https://web.archive.org/web/20070614063821/https://caae.phil.cmu.edu/projects/ast/Papers/awodey_outline.pdf))

* [[Benno van den Berg]], [[Ieke Moerdijk]], _A Unified Approach to Algebraic Set Theory_ [arXiv](http://arxiv.org/abs/0710.3066)

A standard textbook is

* {#JoyalMoerdijk} [[André Joyal]], [[Ieke Moerdijk]]: _Algebraic set theory_, London Mathematical Society Lecture Note Series __220__, Cambridge University Press (1995) &lbrack;ISBN:0-521-55830-1, [doi:10.1017/CBO9780511752483](https://doi.org/10.1017/CBO9780511752483)&rbrack;
 

A reference for BIST is

* [[Steve Awodey]], [[Carsten Butz]], [[Alex Simpson]], [[Thomas Streicher]], ["Relating first-order set theories, toposes and categories of classes"](https://doi.org/10.1016/j.apal.2013.06.004), _Annals of Pure and Applied Logic_ 165 (2014)

[[!redirects algebraic set theories]]
[[!redirects small maps]]
[[!redirects small map]]

