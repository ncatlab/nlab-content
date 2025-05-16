
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
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

#Contents#
* table of contents
{:toc}

## Definition ##


Traditionally, there are two different ways to present [[dependent type theory]]:

* One can present dependent type theory with a [[hierarchy of type universes]] such that every type is a term of a universe of the hierarchy. Examples of such dependent type theories include the one found in the [[HoTT book]] and the proof assistants [[Agda]], [[Coq]], [[Lean]], and its variants like [[Cubical Agda]]. 

* Alternatively, one can present dependent type theory with a separate type [[judgment]] and no [[type universes]] at all. Examples of such dependent type theories include the one found in [[Egbert Rijke]]'s [[Introduction to Homotopy Type Theory]]. 

From these two notions of dependent type theory, there are two notions of a *univalent type theory*:

* In the first case, a **univalent type theory** is a [[dependent type theory]] with [[identity types]], [[dependent product types]], and [[dependent sum types]] such that all universes in the universe hierarchy satisfy the [[univalence axiom]]. 

* In the second case, a **univalent type theory** is a [[dependent type theory with type variables]] and with [[identity types]], [[dependent product types]], [[dependent sum types]], and [[identity type#IdentityTypesBetweenTypes|identity types between types]] such that the [[univalence axiom]] holds in the type theory. 

These univalent type theories usually have additional types such as the [[empty type]], the [[unit type]], the [[booleans]], and the [[natural numbers type]], making it into a [[Martin-Löf dependent type theory]]. 

## See also ##

* [[Martin-Löf dependent type theory]]

* [[proof theoretic strength of univalent type theory plus HITs]]

* [[homotopy type theory]]

* [[univalent foundations]]

* [[UniMath]]

## References ##

* Auke Booij, _Analysis in Univalent Type Theory_, ([slides](https://www.cs.bham.ac.uk/~abb538/slides/2018-02-darmstadt.pdf)) ([thesis](https://www.cs.bham.ac.uk/~abb538/thesis-first_submission.pdf))

* [[Martín Hötzel Escardó]] and [Cory Knapp](https://github.com/cmknapp), _Partial Elements and Recursion via Dominances in Univalent Type Theory_, ([LIPIcs:2017:7682](https://drops.dagstuhl.de/opus/volltexte/2017/7682/))

Univalent type theory is discussed in chapter 5 of:

* {#AngiuliGratzer} [[Carlo Angiuli]], [[Daniel Gratzer]], *Principles of Dependent Type Theory* ([pdf](https://www.danielgratzer.com/papers/type-theory-book.pdf))

[[!redirects univalent type theories]]

[[!redirects univalent type universe]]
[[!redirects univalent type universes]]
