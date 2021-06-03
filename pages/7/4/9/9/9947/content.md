
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
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

A _proof assistant_ or _proof management system_ is a kind of software designed to help with [[proofs]] in formalized [[mathematics]]. Many proof assistants resemble and/or include a [[programming language]].

There are arguably two threads of current development in proof systems, which may be called "foundational" and "coverage".

The "foundational" work tries to find the best foundational theory to formalize mathematics (see also at _[[foundations of mathematics]]_). Out of that work first came [[dependent type theory|dependent types]] ([[Automath]], in the late 60s), then the [[calculus of constructions]] (early [[Coq]]), and the [[calculus of inductive constructions]] (current [[Coq]]). More recently a new wave of such work is being done in [[homotopy type theory]] as another step in this direction. Coq's library is not that large, except in the area of [[group theory]] where the results of the work on [[Feit-Thompson theorem]] has produced something larger.

The "coverage" work tries to formalize as much as possible of mathematics in existing theories.  For instance, for decades people have been building [[Mizar]]'s library (Mizar is based on [[Tarski–Grothendieck set theory]] rather than [[type theory]]). Its library is a couple of orders of magnitude larger than anyone else's. On the other hand, despite this quantity, it remains an issue to attack problems of contemporary research interest in these systems, see also at _[Mizar -- problem of pertinence](Mizar#ProblemOfPertinence)_.

Similar to Mizar is [[NuPRL]], [[HOL light]] and [[Isabelle]], which all have decently sized libraries.  (Isabelle can be used with either [[material set theory]], like Mizar, or [[higher-order type theory]], like the others.)


## Examples

[[!include proof assistants and formalization projects -- list]]


## References

* Wikipedia, _[Proof assistant](https://en.wikipedia.org/wiki/Proof_assistant)_

* Oscar Lanford III., _Computer assisted proofs in analysis_, Proceedings of the International Congress of Mathematicians, 1986 ([pdf](http://www.mathunion.org/ICM/ICM1986.2/Main/icm1986.2.1385.1394.ocr.pdf))


* [[Freek Wiedijk]], _Digital math by alphabet_ ([web](http://www.cs.ru.nl/~freek/digimath/index.html))

* [[Carlos Simpson]], _[Verification and creation of proofs by computer](http://math.unice.fr/~carlos/themes/verif.html)_


* {#Avigad12} [[Jeremy Avigad]], _Interactive Theorem Proving,
Automated Reasoning, and Mathematical Computation_, 2012 [pdf slides](http://www.andrew.cmu.edu/user/avigad/Talks/icerm.pdf)


* _[Conference Series on Intelligent Computer Mathematics](http://www.cicm-conference.org/)_

  ([2014](http://cicm-conference.org/2014/cicm.php))

* Conference series on Interactive theorem proving

  ([2014](http://www.cs.uwyo.edu/~ruben/itp-2014/))

Parts of the above text are taken from [this MO comment](http://mathoverflow.net/questions/133572/at-which-level-is-it-currently-possible-to-write-formal-proofs/134009#134009) by [[Jacques Carette]].

Proof assistants specifically for [[homotopy type theory]]:

* [HoTT wiki](https://ncatlab.org/homotopytypetheory/show/HomePage), *[[homotopytypetheory:Proof Assistants]]*

See also 

* [[Kevin Buzzard]], _[Xena project](https://xenaproject.wordpress.com/2018/10/07/what-is-the-xena-project/)_

  on [[formal proof]] and proof assistants in undergraduate mathematics.

[[!redirects proof assistant]]
[[!redirects proof assistants]]

[[!redirects proof management system]]
[[!redirects proof management systems]]

[[!redirects computer proof assistant]]
[[!redirects computer proof assistants]]

[[!redirects theorem prover]]
