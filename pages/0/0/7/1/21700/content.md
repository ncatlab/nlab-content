

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea


The _initiality conjecture_ in [[type theory]] states that the [[term model]] of a [[type theory]] should be an [[initial object]] in the [[categorical semantics|category of models]] of that type theory. Initiality guarantees that the [[relation between type theory and category theory]] works as expected, hence that formal [[syntax|syntactical]] [[proofs]] in type theory  match theorems in [[categories]] that [[categorical semantics|interpret]] these type theories.

A careful proof of initiality for the special case of the [[calculus of constructions]] was given in [Streicher 91](#Streicher91).  Since then, initiality for more complex type theories (such as [[Martin-Löf dependent type theory]]) has often been treated as established, as a straightforward extension of Streicher’s result, but never written up carefully for a larger theory.

Around 2010, various researchers (notably [Voevodsky 15](#Voevodsky15), [16](#Voevodsky16), [17](#Voevodsky17)) raised the question of whether these extensions really were sufficiently straightforward to consider them established without further proof.  Since then, views on the status of initiality have varied within the field; but the issue has been, at least, a frustrating unresolved point.

A [[proof]] of the initiality conjecture for a full-featured [[Martin-Löf type theory]] is given/announced in [de Boer 20](#deBoer20), [Brunerie-Lumsdaine 20](#BrunerieLumsdaine20).  

> (text adapted from [Brunerie-Lumsdaine 20](#BrunerieLumsdaine20))


## Related concepts


* [[relation between type theory and category theory]]

* [[categorical model of dependent types]]

* [[syntax-semantics duality]]

* [[categorical semantics]]

* [[computational trinitarianism]]

* [[Awodey's conjecture]]



## References
  {#References}

Proof of the initiality conjecture for the [[calculus of constructions]] is due to:

* {#Streicher91} [[Thomas Streicher]], Chapter 4 of: _Semantics of type theory -- Correctness, completeness and independence results_, Progress in Theoretical Computer Science, Birkhäuser Boston, Inc., Boston, MA, 1991, xii+298 pp., (ISBN:0-8176-3594-7, [doi:10.1007/978-1-4612-0433-6](https://doi.org/10.1007/978-1-4612-0433-6))

Relevance of proof of more general versions of the conjecture was amplified in:

* {#Voevodsky15} [[Vladimir Voevodsky]], _[HoTT is not an interpretation of MLTT into abstract homotopy theory](https://homotopytypetheory.org/2015/01/11/hott-is-not-an-interpretation-of-mltt-into-abstract-homotopy-theory/)_, Jan 2015

  [[Peter Lumsdaine]] ([13 January 2015](https://homotopytypetheory.org/2015/01/11/hott-is-not-an-interpretation-of-mltt-into-abstract-homotopy-theory/#comment-35811)):

  > I am still confident that initiality (for MLTT, and other specific type theories) is a straightforward extension of Streicher’s proof. But I no longer feel that confidence justifies treating it as proven. We can’t be certain that it’s as straightforward as we think it is until someone has actually written it out — carefully, correctly, and publicly, so that multiple sets of eyes can check for errors.

* {#Voevodsky16} [[Vladimir Voevodsky]], _Mathematical theory of type theories and the initiality conjecture_, April 2016 ([pdf](https://www.math.ias.edu/Voevodsky/other/Voevodsky%20Templeton%20proposal.pdf), [[VoevodskyInitialityConjectureProposal.pdf:file]])

* {#Voevodsky17} [[Vladimir Voevodsky]], _Models, Interpretations and the Initiality Conjecture_, talk at _Special session on category theory and type theory_ in honor of Per Martin-Löf on his 75th birthday, August 17–19, 2017, during the [Logic Colloquium 2017](https://www.math-stockholm.se/konferenser-och-akti/logic-in-stockholm-2/logic-colloquium-201/logic-colloquium-2017-august-14-20-1.717648), [pdf](https://www.math.ias.edu/Voevodsky/files/files-annotated/Dropbox/Unfinished_papers/Type_systems/Notes_on_Type_Systems/2017_LC_Martin-Lof_special_session/BSL_extended_abstract.pdf))

Early status reports on the full proof appeared in:

* [[Andrej Bauer]] (with Philipp Haselwarter and [[Peter Lumsdaine]]), _Toward an initiality theorem for general type theories_, talk at _[Types, Homotopy Type theory, and Verification](https://www.him.uni-bonn.de/programs/past-programs/past-trimester-programs/types-sets-constructions/workshop-types-homotopy-type-theory-and-verification/schedule/)_, June 2018 ([abstract](https://www.him.uni-bonn.de/programs/past-programs/past-trimester-programs/types-sets-constructions/workshop-types-homotopy-type-theory-and-verification/schedule), [video recording](https://youtu.be/Bf2v448-3Qg))

* [[Peter LeFanu Lumsdaine]] (joint with Menno de Boer, [[Guillaume Brunerie]] , [[Anders Mörtberg]]), _Formalising the initiality conjecture in Coq_, Göteborg–Stockholm Joint Type Theory Seminar, December 2018 ([pdf](http://peterlefanulumsdaine.com/research/Lumsdaine-2018-Goteborg-Initiality.pdf))

A full [[proof]] of the [[initiality conjecture]] for full [[Martin-Löf type theory]], [[formal proof|formalized]] in [[Agda]], is given/announced in:

* [[Guillaume Brunerie]] (with Menno de Boer, [[Peter Lumsdaine]], [[Anders Mörtberg]]), _A formalization of the initiality conjecture in Agda_, talk at HoTT 2019, Pittsburgh ([pdf](https://guillaumebrunerie.github.io/pdf/initiality.pdf))

* {#deBoer20} Menno de Boer, _A Proof and Formalization of the Initiality Conjecture of Dependent Type Theory_, Stockholm 2020 ([diva2:1431287](https://su.diva-portal.org/smash/record.jsf?pid=diva2%3A1431287), [pdf](https://su.diva-portal.org/smash/get/diva2:1431287/FULLTEXT01.pdf))

* {#BrunerieLumsdaine20} [[Guillaume Brunerie]], [[Peter LeFanu Lumsdaine]] (joint with Menno de Boer, [[Anders Mörtberg]]), _Initiality for Martin-Löf type theory_, [Homotopy Type Theory Electronic Seminar Talks](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottest.html), Sept 10, 2020

[[!redirects initiality conjectures]]

[[!redirects initiality theorem]]
[[!redirects initiality theorems]]
