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
  7. [[modular arithmetic|Modular arithmetic]] via the [[Curry-Howard isomorphism]]
  8. Decidability in elementary number theory

* The second chapter is an exposition of [[Vladimir Voevodsky|Voevodsky]]'s [[Univalent Foundations for Mathematics]]. In this chapter we gradually extend [[dependent type theory]] with [[function extensionality]], [[propositional truncation]], the [[univalence axiom]], and the type theoretic [[replacement axiom]].
  9.  [[equivalence|Equivalences]]
  10. [[contractible type|Contractible types]]
  11. The [[fundamental theorem of identity types]]
  12. [[proposition|Propositions]], [[set|sets]], and the higher [[homotopy level|truncation levels]]
  13. [[function extensionality|Function extensionality]]
  14. [[propositional truncation|Propositional truncations]]
  15. [[image factorization|Image factorizations]]
  16. [[finite type|Finite types]]
  17. The [[univalence axiom]]
  18. [[quotient|Set-quotients]]
  19. [[group|Groups]] in [[Univalent Foundations for Mathematics|univalent mathematics]]
  
* The third chapter studies [[higher inductive types]], and develops [[homotopy theory]] and concepts from [[higher category theory]] in type theory.
  20. The [[circle]]
  21. The [[universal cover]] of the [[circle]]
  22. [[homotopy pullback|Homotopy pullbacks]]
  23. [[homotopy pushout|Homotopy pushouts]]
  24. [[Cubical diagrams]]
  25. [[pullback-stable colimit|Universality]] and [[descent]] for [[homotopy pushout|pushouts]]
  26. [[sequential colimit|Sequential colimits]]
  27. [[homotopy group|Homotopy groups]] of [[types]]
  28. The [[classifying space|classifying type]] of a [[group]]
  29. The [[Hopf fibration]]
  30. The [[real projective space|real projective spaces]]
  31. [[n-truncation modality|Truncations]]
  32. [[connected homotopy type|Connected types]] and maps
  33. The [[Blakers-Massey theorem]]
  34. [[infinity-group|Higher group theory]]

## Formalization

* The [main formalization](https://github.com/HoTT-Intro/Agda) of the book is in [[Agda]].

* Parts of the book have also been formalized in [Coq](https://github.com/HoTT-Intro/Coq).

category: reference