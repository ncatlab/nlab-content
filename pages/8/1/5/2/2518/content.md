
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

A **structural set theory** is a [[set theory]] which describes [[structuralism|structural]] mathematics, and *only* [[structuralism|structural]] mathematics: Sets are conceived as [[objects]] that have [[elements]], and are related to each other by [[functions]] or [[relations]].  In the most common structural set theories such as [[ETCS]], sets are characterized by the functions between them, i.e. by the [[category]] ("[[Set]]") which they form ([Lawvere 65](#Lawvere65)).  This is what essentially all the application of [[set theory]] in the practice of [[mathematics]] actually uses -- a point amplified by the approach of the introductory textbook [Lawvere-Rosebrugh 03](#LawvereRosebrugh03). 

This is in contrast to traditional [[ZFC|Zermelo-Fraenkel]]-style "[[material set theory]]"  where a global set-membership relation "$\in$" forces one to think of all elements of sets as sets themselves, hence of sets-of-sets-of-sets-..., a feature that is almost never actually used or even considered in [[mathematics]], away from the study of [[material set theory]] itself.

As conceived by the [[structuralism|structuralist]], [[mathematics]] is the study of structures whose form is independent of the particular attributes of the things that make them up.  For instance, in [[ZF]] [[set theory]], "the set of natural numbers" can be defined as the von Neumann naturals $\omega_N = \{ \emptyset, \{\emptyset\}, \{\emptyset, \{\emptyset\}\}, \dots \}$ or alternately as the Zermelo naturals $\omega_Z = \{ \emptyset, \{\emptyset\}, \{\{\emptyset\}\}, \dots \}$, but either definition has all the necessary properties (namely, the properties making it a [[natural numbers object]] in [[Set|the category of sets]], when equipped with an appropriate successor operation).  See, for instance, [Benacerraf's paper](#WhatNumbersCouldNotBe).

The structuralist says, essentially, that the number "$3$" should denote "the third place in a [[natural numbers object]]" rather than some particular set such as $\{\emptyset, \{\emptyset\}, \{\emptyset, \{\emptyset\}\}\}$ as it does in any definition of "the set of natural numbers" in ZF.

*Structural set theory* provides a [[foundation of mathematics]] which is free of this "superfluous baggage" attendant on theories such as ZF, in which there is lots of information such as whether or not $3\in 17$ (yes, says von Neumann; no, says Zermelo) which is never used in mathematics.  In a structural set theory, the elements (such as $3$) of a set (such as $\mathbb{N}$) *have* no identity apart from their existence as elements of that set, and whatever structure is given to that set by the functions and relations placed upon it.  That is, sets (together with other attendant concepts such as [[elements]], [[functions]], and [[relations]]) are the "raw material" from which mathematical structures are built.  By contrast, theories such as ZF may be called [[material set theories]] or *membership-based set theories*.

Thus, somewhat paradoxically, it turns out that one of the primary attributes of a structural set theory is that the *elements* of a set have *no* "internal" structure; they are only given structure by means of functions and relations.  In particular, they are not themselves sets, and by default cannot be elements of any other set (not in the sense that it is false that they are, but in the sense that it is meaningless to ask whether they are), so that elements of different sets cannot be compared (unless and until extra structure is imposed).  Structural set theory thus looks very much like [[type theory]].  We contrast it with [[material set theory|material set theories]] such as ZF, in which the elements of sets can have internal structure, and are often (perhaps always) themselves sets.

Structural set theories can be distinguished by whether they include a formal notion of [[family]] of [[sets]]. Those that do are known as [[first-order set theory|first-order set theories]], while those that do not are known as [[zeroth-order set theory|seroth-order set theories]]. [[higher-order set theory|Higher-order set theories]] have a notion of families of families in addition to families of sets. This parallels [[logic]], where the role of [[proposition]]s is played by sets and the role of [[predicate]]s is played by families. Many structural set theories are only zeroth-order set theories, but the hSets and functions from hSets to the type hSet in [[homotopy type theory]] form a higher-order set theory. 

It is hard to say precisely what makes a set theory "structural", but one attempt is the notion of a [[structurally presented set theory]].

## Examples
 {#Examples}

### Elementary theory of the category of sets (ETCS)
 {#ETCS}

The original, and most commonly cited, categorially presented structural set theory is the _[[elementary theory of the category of sets]]_, or _[[ETCS]]_ for short ([Lawvere 65](#Lawvere65)).  


Therefore structural set theory is also called **categorial set theory**.

[[ETCS]] axiomatizes the [[category]] [[Set]] of [[sets]] as a [[well-pointed topos]] and thus lends itself to [[foundations of mathematics]] in [[topos theory]]. As such this is similar to the [[h-set]]-theory found in [[homotopy type theory]] ([below](#InHomotopyTypeTheory)), which forms a [[ΠW-pretopos]].

[[ETCS]] is weaker than [[ZFC]]. To handle some esoteric parts of modern mathematics (such as?) it must be supplemented with an [[axiom of collection]], although it suffices for most everyday uses.  

[McLarty 93](#McLarty93) argues that ETCS resolves the issues originally raised by [Benacerraf 65](#Benacerraf65).

### Sets, Elements and Relations (SEAR)

Another structural set theory, which is stronger than ETCS (since it includes the axiom of collection by default) and also less closely tied to category theory, is [[SEAR]].

### Setoids

Set theory set up in [[extensional type theory|extensional]] [[intuitionistic type theory]] via [[setoids]] is structural.

### Local set theory

Local set theory avoids the use of any global universe but instead is formulated in a many-sorted language that has various forms of sorts including, for each sort a power-sort; see [Bell](#Bell) and [Aczel](#Aczel).

### Homotopy-sets in homotopy type theory
  {#InHomotopyTypeTheory}

The collection of  [[h-sets]] in [[homotopy type theory]] constitute a [[ΠW-pretopos]], hence a structural set theory ([Rijke-Spitters 13](#RijkeSpitter13)). 

## Related Pages

* [[material set theory]]

* [[structurally presented set theory]]

* [[material-structural adjunction]]

## References ##

A textbook that introduces the [[foundations of mathematics]] informally via structural set theory is

* {#LawvereRosebrugh03} [[William Lawvere]], [[Robert Rosebrugh]], _[[Sets for Mathematics]]_, Cambridge UP 2003.

The formal account of [[ETCS]] originates with


* {#Lawvere65} [[William Lawvere]], _An elementary theory of the category of sets_, Proceedings of the National Academy of Science of the U.S.A **52** pp.1506-1511 (1965). ([pdf](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC300477/pdf/pnas00186-0196.pdf))

Structural set theory found in [[homotopy type theory]] is discussed in

* {#RijkeSpitters13} [[Egbert Rijke]], [[Bas Spitters]], _Sets in homotopy type theory_, Mathematical Structures in Computer Science, Volume 25, Issue 5 (From type theory and homotopy theory to Univalent Foundations of Mathematics)  ([arXiv:1305.3835](http://arxiv.org/abs/1305.3835))

which became one chapter in 

* [[Univalent Foundations Project]], _[[Homotopy Type Theory – Univalent Foundations of Mathematics]]_

Relation to [[material set theory]] is discussed in

* {#Shulman18} [[Michael Shulman]], _Comparing material and structural set theories_ ([arXiv:1808.05204](https://arxiv.org/abs/1808.05204))


See also

* {#Benacerraf65} P. Benacerraf, _What numbers could not be_, The Philosophical Review Vol. 74, No. 1, Jan., 1965  {#WhatNumbersCouldNotBe}

* {#McLarty93} [[Colin McLarty]], _Numbers can be just what they have to_, No&#251;s, Vol 27, No. 4, 1993. 

* John Bell, _Notes on toposes and local set theories_ [PDF](http://publish.uwo.ca/~jbell/topnotes.pdf)

* Peter Aczel, _Local Constructive Set Theory and Inductive Definitions_, [PDF](http://www.cs.man.ac.uk/~petera/sommaruga-book-paper.pdf)

* [[Mike Shulman]], *Syntax, Semantics, and Structuralism II* [blog](https://golem.ph.utexas.edu/category/2009/12/syntax_semantics_and_structura_1.html)

* [[Tom Leinster]], *Rethinking set theory* [blog](https://golem.ph.utexas.edu/category/2012/12/rethinking_set_theory.html), [arXiv](http://arxiv.org/abs/1212.6543)

[[!redirects structural set theory]]
[[!redirects structural set theories]]
