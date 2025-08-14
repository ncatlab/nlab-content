#Contents#
* table of contents
{:toc}



##Idea 

Classic [[modalities]] are defined in absolute terms, so that, for instance, [[necessity and possibility]] are understood in terms of a state of affairs obtaining in all or some world. Some [philosophers](#philosophy) in the early 1970s looked to generalize these to graded versions so that a proposition may be said to be, say, quite likely, highly likely, and so on. Since then, linguists and computer scientists have developed these ideas, the latter expanding the topic to include those modalities relating to resources and [[side effects]].

A **graded modality** is an indexed family of [[modalities]] with some additional [[structure]] on the indices which mirrors the structure of the axioms/proof rules. A graded modality is a [[graded monad]] (or comonad) with idempotent components.

For example, the [[exponential modality]] of [[linear logic]] $!$ has a graded counterpart in [[bounded linear logic]], where $!$ is replaced with a family of modalities $!_n$ indexed by the natural numbers (the reuse bound).

More recent variations of [[linear logic]] which use graded modalities, where $!$ is replaced with a family of modalities $!_r$ indexed by a [[semi-ring]] could be designated by the name [[graded linear logic]].

[[Differential linear logic]] and [[graded linear logic]] seem to be mixable under the form of a [[graded differential linear logic]]. Such a logic would be a refinement of [[differential linear logic]] able to deal with differentiable functions which have a grade such as the degree of a polynomial or the number of times the function is differentiable. A more specific system would be a [[symmetric linear logic]] which deal specifically with [[symmetric powers]] and thus [[homogeneous polynomials]]. It seems possible to adapt the idea to an [[anticommutative]] setting giving an [[homological linear logic]]. Such a logic would be probably able to give a syntax for at least [[Koszul complexes]]. 


## References

* Brunel, Aloïs and Gaboardi, Marco and Mazza, Damiano and Zdancewic, Steve, _A Core Quantitative Coeffect Calculus_, ([doi](https://doi.org/10.1007/978-3-642-54833-8_19)) ([pdf](https://lipn.univ-paris13.fr/~mazza/papers/CoreQuantCoeff.pdf))

* Dan R. Ghica and Alex I. Smith, _Bounded Linear Types in a Resource Semiring
_, ([doi](https://doi.org/10.1007/978-3-642-54833-8_18)) ([pdf](https://www.cs.bham.ac.uk/~drg/papers/esop14.pdf))

* [[Dominic Orchard]], Vilem-Benjamin Liepelt, Harley Eades III, _Quantitative Program Reasoning with Graded Modal Types_, ([pdf](https://www.cs.kent.ac.uk/people/staff/dao7/publ/granule-icfp19.pdf))

* [[Dominic Orchard]], Vilem-Benjamin Liepelt, _Gram:  A linear functional language with graded modal types_, ([extended abstract](https://www.cs.ox.ac.uk/conferences/fscd2017/preproceedings_unprotected/TLLA_Orchard.pdf))

* Marco Gaboardi, [[Shin-ya Katsumata]], [[Dominic Orchard]], Flavien Breuvart, [[Tarmo Uustalu]], *Combining effects and coeffects via grading*, ICFP 2016: Proceedings of the 21st ACM SIGPLAN International Conference on Functional Programming (2016) 476–489 &lbrack;[doi:10.1145/2951913.2951939](https://doi.org/10.1145/2951913.2951939), [talk abstract](https://icfp16.sigplan.org/details/icfp-2016-papers/31/Combining-Effects-and-Coeffects-via-Grading), [video rec](https://www.youtube.com/watch?v=l1ZNMT3fQCo)&rbrack;

* Flavien Breuvart, Michele Pagani, _Modelling Coeffects in the Relational Semantics
of Linear Logic_, ([pdf](https://drops.dagstuhl.de/opus/volltexte/2015/5438/pdf/35.pdf))

* Shin-ya Katsumata, _A Double Category Theoretic Analysis of Graded Linear Exponential Comonads_, ([doi](https://doi.org/10.1007/978-3-319-89366-2_6))

* Soichiro Fujii, Shin-ya Katsumata, Paul-André Melliès, _Towards a Formal Theory of Graded Monads_, ([doi](https://doi.org/10.1007/978-3-662-49630-5_30)) ([pdf](https://www.irif.fr/~mellies/papers/fossacs2016-final-paper.pdf))

* [[J-B Vienney|Jean-Baptiste Vienney]], [[Jean-Simon Lemay|Jean-Simon Pacaud Lemay]], _Graded Differential Categories and Graded Differential Linear Logic_, 2023, [arXiv](https://arxiv.org/abs/2303.10586) 

A formal framework for type theories with a collection of modalities is in

* [[Daniel Licata]], [[Mike Shulman]], and [[Mitchell Riley]], _A Fibrational Framework for Substructural and Modal Logics (extended version)_, in Proceedings of 2nd International Conference on Formal Structures for Computation and Deduction (FSCD 2017) ([doi: 10.4230/LIPIcs.FSCD.2017.25](http://drops.dagstuhl.de/opus/volltexte/2017/7740/), [pdf](http://dlicata.web.wesleyan.edu/pubs/lsr17multi/lsr17multi-ex.pdf))

On [[dependent linear types]] and [[graded modalities]]:

* [[Benjamin Moon]], [[Harley Eades III]], [[Dominic Orchard]], *Graded Modal Dependent Type Theory*. In: N. Yoshida (ed.) *Programming Languages and Systems ESOP 2021*, Lecture Notes in Computer Science **12648**, Springer (2021) 462-490 &lbrack;[doi:10.1007/978-3-030-72019-3_17](https://doi.org/10.1007/978-3-030-72019-3_17), [arxiv:2010.13163](https://arxiv.org/abs/2010.13163)&rbrack;


For discussion in [[philosophy]] and linguistics, see

* Patrick Grosz, _Grading Modality: A New Approach to Modal Concord and its Relatives_, ([paper](https://www.univie.ac.at/sub14/proc/grosz.pdf))

* Daniel Lassiter, _Graded modality_, ([paper](https://web.stanford.edu/~danlass/Lassiter-graded-modality-draft.pdf)) 

* Daniel Lassiter, _Graded Modality: Qualitative and Quantitative Perspectives_, OUP, ([website](https://global.oup.com/academic/product/graded-modality-9780198701354?cc=us&lang=en&))

 {#philosophy} Earlier work in philosophy includes

* Lou Goble, 1970. _Grades Of Modality_. Logique Et Analyse 13, pp. 323-334, ([paper](http://virthost.vub.ac.be/lnaweb/ojs/index.php/LogiqueEtAnalyse/article/view/405)).
*  David Kaplan, _S5 with multiple possibility_, The Journal of Symbolic Logic, 35:355–356, 1970.

* Kit Fine, 1972. _In so many possible worlds_. Notre Dame Journal of Formal Logics 13: 516–520.

* David Lewis, 1973. _Counterfactuals_. Oxford: Blackwell

* M. Fattorosi-Barnaba  and  F. de Caro.  _Graded  modalities I_. Studia  Logica, 44:197–221,1985


[[!redirects graded modalities]]

