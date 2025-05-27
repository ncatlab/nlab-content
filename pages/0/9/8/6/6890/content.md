
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The computer software _Rocq_ (previously called _Coq_) "runs" the formal [[foundations]]-language _[[dependent type theory|dependent]] [[type theory]]_ and serves in particular as a formal [[proof management system]]. It provides a formal language to write mathematical [[definitions]], executable [[programs]] and [[theorems]] together with an environment for semi-interactive development of machine-checked [[proofs]], i.e. for [[certified programming]]. 

The old name, _Coq_, originates from [[Thierry Coquand]], with a reference as well to Coquand's [[calculus of constructions|Calculus of Constructions]] (CoC). The new name _Rocq_ originates from [Inria Rocquencourt](https://www.inria.fr/en), the institute in which the language was originally developed at, and is a reference to the mythological bird Roc. Both names follow a tradition of naming languages after animals (compare OCaml). 

## Applications

Computer systems such as Rocq and [[Agda]] have been used to give machine-assisted and machine-verified proofs of extraordinary length, such as of the [[four-colour theorem]] and the [[Kepler conjecture]]. 

More generally, they are being used to formalise and machine-verify large parts of mathematics as such, see the section _[Formalization of set-based mathematics](#FormalizationOfSetBasedMathematics)_ below. 

One striking insight by [[Vladimir Voevodsky]] was that Rocq naturally lends itself also to a formalization of higher mathematics that is founded not on sets, but on [[higher category theory]] and [[homotopy theory]]. For this see below the section _[Homotopy type theory](#HomotopyTypeTheory)_.



### Formalization of set-based mathematics
  {#FormalizationOfSetBasedMathematics}

Projects include

* [ForMath](#ForMath)

* [MathClasses](#MathClasses)

### Formalized proofs

Major [[theorems]] whose [[proofs]] have been fully formalized in Rocq include

* [[Feit-Thompson theorem]]

### Homotopy type theory
  {#HomotopyTypeTheory}

For Rocq-projects in [[homotopy type theory]] see the section [Code](homotopy+type+theory#Code).



## Related entries
 {#RelatedEntries}

* Rocq uses the _[[Gallina specification language]]_ for specifying [[theories]].

* and it uses a version of the *[[calculus of constructions]]* to implement [[natural deduction]].

* *[[CoqQ]]* is a [[quantum programming language]] [[domain specific embedded programming language|embedded]] in Coq.

\linebreak

[[!include proof assistants and formalization projects -- list]]



## References

### General
 {#ReferencesGeneral}

* [Rocq home page](https://rocq-prover.org/)

* {#jsCoq} [JsCoq](https://x80.org/rhino-coq/), a ready-to-use online Coq environment

* {#jsHoTTCoq} [JsHoTTCoq](https://x80.org/rhino-hott/), a ready-to-use online [[HoTT]] Coq environment

* {#CoqWiki} [Cocorico](http://coq.inria.fr/cocorico), the Coq wiki

* [HoTT Coq wiki](https://github.com/HoTT/HoTT/wiki)

* [history of Coq](https://github.com/coq/coq/blob/beedccef9ddc8633c705d7c5ee2f1bbbb3ec8a47/dev/doc/README-V1-V5)

* Russell O’Connor, _[Believing In-Consistency](http://r6.ca/blog/20091101T231201Z.html)_

  (On whether the consistency of Coq is believable, given that [[ordinal analysis]] techniques are nowhere near able to handle such strong systems.)

### Learning Coq

To get an idea how to use Coq from Emacs, there are [[Andrej Bauer]]'s _Video tutorials for the Coq proof assistant_ ([web](http://math.andrej.com/2011/02/22/video-tutorials-for-the-coq-proof-assistant/)).

Yet properly learning Coq can be quite daunting, luckily the right material can help a lot:

1. [[Benjamin Pierce]]'s [Software Foundations](http://www.cis.upenn.edu/~bcpierce/sf/) is probably the most elementary introduction to Coq and functional progamming. The book is written in Coq so you can directly open the source files in CoqIDE and step through them to see what is going on and solve the exercises.

1. In a similar style, [[Andrej Bauer]] and [[Peter LeFanu Lumsdaine]] wrote a nice [Coq tutorial](https://github.com/andrejbauer/Homotopy/tree/master/OberwolfachTutorial) ([pdf](https://github.com/andrejbauer/Homotopy/blob/master/OberwolfachTutorial/univalence.pdf)) on [homotopy type theory](#HomotopyTypeTheory). See also _[[Oberwolfach HoTT-Coq tutorial]]_.

1. [[Adam Chlipala]]'s trimmed down version of [Certified Programming with Dependent Types](http://adam.chlipala.net/papers/CpdtJFR/) explains more advanced Coq techniques.

 
### Applications to formal mathematics

*  {#MahboubiTassi21} Assia Mahboubi, Enrico Tassi, *Mathematical Components* (2021) &lbrack;[doi:10.5281/zenodo.3999478](https://doi.org/10.5281/zenodo.3999478)&rbrack;

On [[ForMath]]:

* {#ForMath} [[Thierry Coquand]], _ForMath: Formalisation of Mathematics_ research project ([web](http://wiki.portal.chalmers.se/cse/pmwiki.php/ForMath/ForMath))
  

* {#MathClasses} Eelis van der Weegen, [[Bas Spitters]], Robbert Krebbers, Matthieu Sozeau, Tom Prince, [[Jelle Herold]], 

  _Math Classes_, Coq Library for basic mathematical structures ([web](http://math-classes.org/))
 
Formalization of [[synthetic geometry|synthetic]] [[Euclidean geometry]]:

* [[Gabriel Braun]], [[Pierre Boutry]], [[Julien Narboux]], _[GeoCoq](http://geocoq.github.io/GeoCoq/)_, _[La g&#233;om&#233;trie de Tarski en Coq](http://gabrielbraun.free.fr/Geometry/Tarski/)_

Formalization of [[internal categories in homotopy type theory]]:

* [[Jason Gross]], [[Adam Chlipala]], [[David Spivak]], _Experience Implementing a Performant Category-Theory Library in Coq_ ([arXiv:1401.7694](http://arxiv.org/abs/1401.7694))
  

category: software

[[!redirects Coq]]
[[!redirects coq]]

[[!redirects Rocq]]
[[!redirects rocq]]