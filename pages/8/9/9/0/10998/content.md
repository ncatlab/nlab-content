
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
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
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

The term _computational type theory_ has been used 

1. generally for [[intuitionistic type theory]] in view of its [[computation|computational]] content via the [[propositions-as-types]] and [[proofs-as-programs]] interpretation (e.g. [Constable 02](#Constable02), [Scholarpedia](#Scholarpedia)). 

1. more specifically for [[intuitionistic type theory]] with [[inductive types]] and here specifically for the dialect of the language which is implemented in the [[NuPRL]] software ([Constable et al. 86](#ConstableEtAl86), [NuPRL 05](#NuPRL05));

   > [Constable, p. 6](#Constable): $[$computational type theory$]$ considerably extended Per Martin-L&#246;f's Intuitionistic Type Theory (ITT) adding set types, quotient types, recursive types, partial object types (bar types)

1. for [[modal type theory]], specifically for [[type theory]] equipped with a [[monad (in computer science)]] that preserves [[finite products]], which exhibits a kind of computation ([Benton-Bierman-de Paiva 93](BentonBiermanDePaiva93), [Fairtlough-Mendler 02](#FairtloughMendler02)). 

   The [[internal logic]] of computational type theory in this sense is also called _propositional lax logic_ ([Fairtlough-Mendler 97](#FairtloughMendler97), [Crolard](#Crolard)) or _computational logic_.

## Related concepts

* [[computational trinitarianism]]


## References

Discussion of intuitionistic/constructive type theory (with inductive types) as such referred to as computational type theory is in 

* Scholarpedia, _[Computational type theory](http://www.scholarpedia.org/article/Computational_type_theory)_
 {#Scholarpedia}

* [[Robert Constable]], _Na&#239;ve Computational Type Theory_, Proof and System-Reliability NATO Science Series Volume 62, 2002, pp 213-259 {#Constable02}

Discussion specifically in the context of [[NuPRL]] is in

* [[Robert Constable]], Stuart F. Allen, H. M. Bromley, W. R. Cleaveland, J. F. Cremer, R. W. Harper, Douglas J. Howe, T. B. Knoblock, N. P. Mendler, P. Panangaden, James T. Sasaki, and Scott F. Smith. _Implementing Mathematics with the Nuprl Proof Development System_. Prentice-Hall, NJ, 1986.
 {#ConstableEtAl86}

* _Innovations in Computational Type Theory using Nuprl_ ([pdf](http://www.cs.uni-potsdam.de/ti/kreitz/PDF/05jal-nuprl.pdf))
 {#NuPRL05}

* [[Robert Constable]], _The Triumph of Types: Creating a Logic of Computational Reality_ ([[ConstableTriumphOfTypes.pdf:file]])
 {#Constable}

Discussion in the sense of [[modal type theory]] where computation is exhibited by a [[monad (in computer science)]] is in 

* Matt Fairtlough, [[Michael Mendler]], _Propositional Lax Logic_,  Volume 137, Issue 1, 25 August 1997, Pages 1&#8211;33 ([pdf](http://www.gdi.uni-bamberg.de/personnel/mendler/research/Papers/pll.pdf))
 {#FairtloughMendler97}

* {#BentonBiermanDePaiva93} [[Nick Benton]], [[Gavin Bierman]], [[Valeria de Paiva]], *Computational Types from a Logical Perspective*, Journal of Functional Programming **8** 2  (1998) 177-193 &lbrack;[doi:10.1017/S0956796898002998](https://doi.org/10.1017/S0956796898002998), [web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.5778)&rbrack;


* Matt Fairtlough, [[Michael Mendler]], _On the Logical Content of Computational Type Theory: A Solution to Curry's Problem_, Types for Proofs and Programs,
Lecture Notes in Computer Science Volume 2277, 2002, pp 63-78 ([[MendlerComputationalTypeTheory.pdf:file]])
 {#FairtloughMendler02}

*  Tristan Crolard, _Monadic reflection in lax logic_ [pdf](http://cedric.cnam.fr/cpr/crolard/publications/reflection.pdf)
 {#Crolard}

See also

* Fairouz Kamareddine, Twan Laan and [[Robert Constable]] (2012) 
_Russell's Orders in Kripke's Theory of Truth and Computational Type Theory_. In Dov. M Gabbay, Akihiro Kanamori and John Woods, (editors) _Sets and Extensions in the Twentieth Century_, 6, HHL, : San Diego: North Holland, 2012, pp. 801-845.


[[!redirects computational type theories]]

[[!redirects propositional lax logic]]

[[!redirects computational logic]]