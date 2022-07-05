This entry collects links related to the forthcoming book


* [[Egbert Rijke]], 

  _Introduction to Homotopy Type Theory_,

  Cambridge Studies in Advanced Mathematics,

  Cambridge University Press 

  {#pdf} [pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf) (478 pages)


which introduces [[homotopy type theory]] in general and [[Martin-Löf's dependent type theory]], the [[Univalent Foundations for Mathematics]] and [[synthetic homotopy theory]] in particular. 

The book is based on a course taught by the author at Carnegie Mellon University in the spring semester of 2018:

* [course webpage](http://www.andrew.cmu.edu/user/erijke/hott/)


Previous versions:

* [pdf (2018 course notes)](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf) (221 pages)

* [pdf (2019 summer school notes)](https://hott.github.io/HoTT-2019/images/hott-intro-rijke.pdf) (134 pages)

* [GitHub repositories](https://github.com/HoTT-Intro)


## Contents

The book contains three chapters:

* The first chapter introduces the reader to [[Martin-Löf's dependent type theory]]. The fundamental concepts of [[type theory]] are explained without immediately jumping into the [[homotopy theory|homotopy]] [[relation between type theory and category theory|interpretation]] of type theory.
  1. [[dependent type theory|Dependent Type Theory]]
  2. [[Pi-types|Dependent function types]]
  3. The [[natural numbers]]
  4. More [[inductive types]]
  5. [[identity type|Identity types]]
  6. [[universe|Universes]]
  7. [[modular arithmetic|Modular arithmetic]] in type theory

* The second chapter is an exposition of [[Vladimir Voevodsky|Voevodsky]]'s [[Univalent Foundations for Mathematics]]. In this chapter we gradually extend [[dependent type theory]] with [[function extensionality]], [[propositional truncation]], the [[univalence axiom]], and the type theoretic [[replacement axiom]].
  8. [[equivalence|Equivalences]]
  9. [[contractible type|Contractible types]]
  10. The [[fundamental theorem of identity types]]
  11. [[proposition|Propositions]], [[set|sets]], and the [[homotopy level|truncation levels]]
  12. [[function extensionality|Function extensionality]]
  13. [[propositional truncation|Propositional truncations]] and the [[image]] of a [[map]]
  14. The [[univalence axiom]]
  15. [[group|Groups]] in [[Univalent Foundations for Mathematics|univalent mathematics]]
  16. [[quotient|Set-quotients]]
  17. Elementary [[number theory]]
* The third chapter studies [[higher inductive types]], and develops [[homotopy theory]] and concepts from [[higher category theory]] in type theory.
  18. The [[circle]]
  19. The [[universal cover]] of the [[circle]]
  20. [[homotopy pullback|Homotopy pullbacks]]
  21. [[homotopy pushout|Homotopy pushouts]]
  22. [[Cubical diagrams]]
  23. [[pullback-stable colimit|Universality]] and [[descent]] for [[homotopy pushout|pushouts]]
  24. [[sequential colimit|Sequential colimits]]
  25. [[homotopy group|Homotopy groups]] of [[types]]
  26. The [[classifying space|classifying type]] of a [[group]]
  27. The [[Hopf fibration]]
  28. The [[real projective space|real projective spaces]]
  29. [[n-truncation modality|Truncations]]
  30. [[connected homotopy type|Connected types]] and maps
  31. The [[Blakers-Massey theorem]]
  32. [[infinity-group|Higher group theory]]

## Formalization

* The [main formalization](https://github.com/HoTT-Intro/Agda) of the book is in [[Agda]].

* Parts of the book have also been formalized in [Coq](https://github.com/HoTT-Intro/Coq).

category: reference