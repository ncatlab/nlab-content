
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A **structural set theory** is a [[set theory]] which describes [[structuralism|structural]] mathematics, and *only* [[structuralism|structural]] mathematics: Sets are conceived as [[objects]] that may have [[functions]] between them, and that characterizes them. Or stated more formally: Sets are characterized by the [[category]] ("[[Set]]") which they form ([Lawvere 65](#Lawvere65)).
This is what essentially all the application of [[set theory]] in the practice of [[mathematics]] actually uses -- a point amplified by the approach of the introductory textbook [Lawvere-Rosebrugh 03](#LawvereRosebrugh03). 

This is in contrast to traditional [[ZFC|Zermolo-Fraenkel]]-style "[[material set theory]]"  where a global set-membership relation "$\in$" forces to think of all elements of sets as sets themselves, hence of sets-of-sets-of-sets-..., a feature that is almost never actually used or even considered in [[mathematics]], away from the study of [[material set theory]] itself.

As conceived by the [[structuralism|structuralist]], [[mathematics]] is the study of structures whose form is independent of the particular attributes of the things that make them up.  For instance, in [[ZF]] [[set theory]], "the set of natural numbers" can be defined as the von Neumann naturals $\omega_N = \{ \emptyset, \{\emptyset\}, \{\emptyset, \{\emptyset\}\}, \dots \}$ or alternately as the Zermelo naturals $\omega_Z = \{ \emptyset, \{\emptyset\}, \{\{\emptyset\}\}, \dots \}$, but either definition has all the necessary properties (namely, the properties making it a [[natural numbers object]] in [[Set|the category of sets]], when equipped with an appropriate successor operation).  See, for instance, [Benacerraf's paper](#WhatNumbersCouldNotBe).

The structuralist says, essentially, that the number "$3$" should denote "the third place in a [[natural numbers object]]" rather than some particular set such as $\{\emptyset, \{\emptyset\}, \{\emptyset, \{\emptyset\}\}\}$ as it does in any definition of "the set of natural numbers" in ZF.

*Structural set theory* provides a [[foundation of mathematics]] which is free of this "superfluous baggage" attendant on theories such as ZF, in which there is lots of information such as whether or not $3\in 17$ (yes, says von Neumann; no, says Zermelo) which is never used in mathematics.  In a structural set theory, the elements (such as $3$) of a set (such as $\mathbb{N}$) *have* no identity apart from their existence as elements of that set, and whatever structure is given to that set by the functions and relations placed upon it.  That is, sets (together with other attendant concepts such as [[elements]], [[functions]], and [[relations]]) are the "raw material" from which mathematical structures are built.  By contrast, theories such as ZF may be called [[material set theories]] or *membership-based set theories*.

Thus, somewhat paradoxically, it turns out that one of the primary attributes of a structural set theory is that the *elements* of a set have *no* "internal" structure; they are only given structure by means of functions and relations.  In particular, they are not themselves sets, and by default cannot be elements of any other set (not in the sense that it is false that they are, but in the sense that it is meaningless to ask whether they are), so that elements of different sets cannot be compared (unless and until extra structure is imposed).  Structural set theory thus looks very much like [[type theory]].  We contrast it with [[material set theory|material set theories]] such as ZF, in which the elements of sets can have internal structure, and are often (perhaps always) themselves sets.

It is hard to say precisely what makes a set theory "structural", but one attempt is the notion of a [[structurally presented set theory]].

## Examples

Among category theorists, it's popular to state the axioms of a structural set theory by specifying elementary properties of [[Set|the category of sets]].  For this reason structural set theory is often called **categorial set theory**.

* The original, and most commonly cited, categorially presented structural set theory is [[Bill Lawvere]]'s [[ETCS]].  It is weaker than ZFC and must be supplemented with an [[axiom of collection]] to handle some esoteric parts of modern mathematics, although it suffices for most everyday uses.  [McLarty's paper](#NumbersCanBe) argues that ETCS resolves the issues originally raised by Benacerraf.

* Another structural set theory, which is stronger than ETCS (since it includes the axiom of collection by default) and also less closely tied to category theory, is [[SEAR]].

* Set theory set up in [[extensional type theory|extensional]] [[intuitionistic type theory]] via [[setoids]] is structural.

* Local set theory avoids the use of any global universe but instead is formulated in a many-sorted language that has various forms of sorts including, for each sort a power-sort; see [Bell](#Bell) and [Aczel](#Aczel).

* Set theory set up via [[h-sets]] in [[homotopy type theory]] is structural ([Rijke-Spitters 13](#RijkeSpitter13)). 

## Related Pages

* [[material set theory]]

* [[structurally presented set theory]]

* [[material-structural adjunction]]

## References ##

An textbook that introduces the [[foundations of mathematics]] informally via structural set theory is

* {#LawvereRosebrugh03} [[William Lawvere]], [[Robert Rosebrugh]], _[[Sets for Mathematics]]_, Cambridge UP 2003.

The formal account of [[ETCS]] originates with


* {#Lawvere65} [[William Lawvere]], _An elementary theory of the category of sets_, Proceedings of the National Academy of Science of the U.S.A **52** pp.1506-1511 (1965). ([pdf](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC300477/pdf/pnas00186-0196.pdf))

Structural set theory found in [[homotopy type theory]] is discussed in

* {#RijkeSpitter13} [[Egbert Rijke]], [[Bas Spitters]], _Sets in homotopy type theory_ ([arXiv:1305.3835](http://arxiv.org/abs/1305.3835))

which became one chapter in 

* [[Univalent Foundations Project]], _[[Homotopy Type Theory – Univalent Foundations of Mathematics]]_

See also

* P. Benacerraf, _What numbers could not be_, The Philosophical Review Vol. 74, No. 1, Jan., 1965  {#WhatNumbersCouldNotBe}

* [[Colin McLarty]], _Numbers can be just what they have to_, No&#251;s, Vol 27, No. 4, 1993. {#NumbersCanBe}

* John Bell, _Notes on toposes and local set theories_ [PDF](http://publish.uwo.ca/~jbell/NOTES%20ON%20TOPOSES%20AND%20LOCAL%20SET%20THEORIES.pdf)

* Peter Aczel, _Local Constructive Set Theory and Inductive Definitions_, [PDF](http://www.cs.man.ac.uk/~petera/sommaruga-book-paper.pdf)

* [[Mike Shulman]], *Syntax, Semantics, and Structuralism II* [blog](https://golem.ph.utexas.edu/category/2009/12/syntax_semantics_and_structura_1.html)

* [[Tom Leinster]], *Rethinking set theory* [blog](https://golem.ph.utexas.edu/category/2012/12/rethinking_set_theory.html), [arXiv](http://arxiv.org/abs/1212.6543)

[[!redirects structural set theory]]
[[!redirects structural set theories]]
