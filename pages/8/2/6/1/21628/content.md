
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

This entry collects links related to the forthcoming book

* [[Egbert Rijke]]:

  \linebreak

  **Introduction to Homotopy Type Theory**

  \linebreak

  Cambridge Studies in Advanced Mathematics,

  Cambridge University Press 

  {#pdf} [arXiv:2212.11082](https://arxiv.org/abs/2212.11082) (359 pages)


which introduces [[homotopy type theory]] in general and in particular [[Martin-Löf's dependent type theory]], the [[Univalent Foundations for Mathematics]] and [[synthetic homotopy theory]]. 

The book is based on a course taught by the author at Carnegie Mellon University in the spring semester of 2018:

* [course webpage](http://www.andrew.cmu.edu/user/erijke/hott/)

The original writeup of these course notes

* [pdf (2018 course notes)](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [[Rijke-IntroductionHoTT-2018.pdf:file]] (221 pages, but smaller margins)

contains considerably more material than retained in the above arXiv version. 

Other versions:

* [pdf (2019 summer school notes)](https://hott.github.io/HoTT-2019/images/hott-intro-rijke.pdf) (134 pages)

* [GitHub repositories](https://github.com/HoTT-Intro)

* {#2022HoTTEST} [pdf (2022 HoTTEST summer school)] (https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf) (478 pages)


## Contents
 {#Contents}

**Chapter I** introduces the reader to [[Martin-Löf's dependent type theory]]. The fundamental concepts of [[type theory]] are explained without immediately jumping into the [[homotopy theory|homotopy]] [[relation between type theory and category theory|interpretation]] of type theory.

$\;\;\;1.$ [[dependent type theory|Dependent Type Theory]]

$\;\;\;2.$ [[Pi-types|Dependent function types]]

$\;\;\;3.$ The [[natural numbers]]

$\;\;\;4.$ More [[inductive types]]
   
$\;\;\;5.$ [[identity type|Identity types]]

$\;\;\;6.$ [[universe|Universes]]

$\;\;\;7.$ [[modular arithmetic|Modular arithmetic]] via the [[Curry-Howard isomorphism]]
   
$\;\;\;8.$ Decidability in elementary number theory

**Chapter II** is an exposition of the [[Univalent Foundations for Mathematics]]. This chapter gradually extends [[dependent type theory]] with [[function extensionality]], [[propositional truncation]], the [[univalence axiom]], and the type theoretic [[replacement axiom]].

$\;\;\;9.$  [[equivalence|Equivalences]]

$\;\;\;10.$ [[contractible type|Contractible types]]

$\;\;\;11.$ The fundamental theorem of [[identity types]]

$\;\;\;12.$ [[proposition|Propositions]], [[set|sets]], and the higher [[homotopy level|truncation levels]]

$\;\;\;13.$ [[function extensionality|Function extensionality]]

$\;\;\;14.$ [[propositional truncation|Propositional truncations]]

$\;\;\;15.$ [[image factorization|Image factorizations]]

$\;\;\;16.$ [[finite type|Finite types]]

$\;\;\;17.$ The [[univalence axiom]]

$\;\;\;18.$ [[quotient|Set quotients]]

$\;\;\;19.$ [[group|Groups]] in [[Univalent Foundations for Mathematics|univalent mathematics]]

$\;\;\;20.$ [[inductive type|General inductive types]]
  
**Chapter III** studies the [[circle]] as a [[higher inductive type]].

$\;\;\;21.$ The [[circle]]

$\;\;\;22.$ The [[universal cover]] of the [[circle]]

An [older version](#2022HoTTEST) of the book ended:

$\;\;\;22.$ [[homotopy pullback|Homotopy pullbacks]]

$\;\;\;23.$ [[homotopy pushout|Homotopy pushouts]]

$\;\;\;24.$ [[cubical set|Cubical]] [[diagrams]]

$\;\;\;25.$ [[pullback-stable colimit|Universality]] and [[descent]] for [[homotopy pushout|pushouts]]

$\;\;\;26.$ [[sequential colimit|Sequential colimits]]

$\;\;\;27.$ [[homotopy group|Homotopy groups]] of [[types]]

$\;\;\;28.$ The [[classifying space|classifying type]] of a [[group]]

$\;\;\;29.$ The [[Hopf fibration]]

$\;\;\;30.$ The [[real projective space|real projective spaces]]

$\;\;\;31.$ [[n-truncation modality|Truncations]]

$\;\;\;32.$ [[connected homotopy type|Connected types]] and maps

$\;\;\;33.$ The [[Blakers-Massey theorem]]

$\;\;\;34.$ [[infinity-group|Higher group theory]]

## Formalization

* The [main formalization](https://github.com/HoTT-Intro/Agda) of the book is in [[Agda]].

* Parts of the book have also been formalized in [Coq](https://github.com/HoTT-Intro/Coq).

category: reference