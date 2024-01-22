
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

\tableofcontents

## Idea

A __set theory__ is a theory of [[sets]].

## Na&#239;ve vs axiomatic set theory

__Na&#239;ve set theory__ is the basic algebra of the [[subsets]] of any given set $U$, together with a few levels of [[power sets]], say up to 
 $\mathcal{P}\mathcal{P}\mathcal{P}U$ and possibly no further.  Often students see this first for the set of [[real numbers]] as $U$ (although in fact one could start with the set of [[natural numbers]] and go one level further for an equivalent theory).  One could also use [[function sets]] instead of power sets as the basic set-forming operation (especially for a [[predicative mathematics|weakly predicative]] theory in [[constructive mathematics]]).

Once you start thinking very much about the nature of sets in general (rather than merely _using_ na&#239;ve set theory), it quickly becomes clear that one must be careful about how one can and cannot form sets.  [[Georg Cantor]] is credited with being the first to think about sets this deeply; although he did not propose a system of general rules for valid set-making operations, he recognised that some sets were 'inconsistent'.  An __axiomatic set theory__ is a set theory which carefully states the rules (or '[[axioms]]') which sets are assumed to obey.

[[Gottlob Frege]] has perhaps the first axiomatic set theory, but it was found (by [[Bertrand Russell]]) to be logically trivial; see [[Russell's paradox]]. [[Charles Sanders Peirce]] presented what could be regarded as the first consistent axiomatic set theory in [Peirce 1885](#Peirce1885) (see [Brady 2000](#Brady2000)). The more widely known consistent set theory is [[Ernst Zermelo]]'s set theory in 1905, which forms the basis for the axiomatic set theory used today.

## Foundational vs definitional set theory

There are two ways to go about doing axiomatic set theory.  The more ambitious is to develop a __foundational set theory__: set theory as [[foundations]] for all of mathematics.  This is what Frege proposed (although he failed through inconsistency) and which Zermelo achieved.

A variation of Zermelo\'s system (developed by Fraenkel and Skolem and called Zermelo--Fraenkel set theory or [[ZFC]]) is the orthodox foundations today, although it needs to be supplemented by [[Grothendieck universes]] (or something along those lines) to handle modern [[category theory]], and set theorists often consider further strengthenings of it through [[large cardinal]] [[axioms]] (of which the existence of Grothendieck universes is an example, just the tip of the iceberg). 

It is also possible to make a __definitional set theory__, in which one defines sets in terms of some more primitive concept. Examples include

* [[class theory]], where a set may be defined as a small [[class]].

* [[formal category theory]], where a set may be defined as a [[discrete category]]. 

* [[dependent type theory]], where a set may be defined as those [[types]] which are [[h-sets]]. 

* [[preset theory]], where a set may be defined as a preset equipped with an [[equivalence relation]]. 

In [[computer science]], a foundation based on the [[lambda-calculus]] is sometimes seen; in these terms, the concept of _[[list]]_ is more natural than set, with the difference being that sets have a coarser notion of equality.

## Constructive vs classical set thoery

There are also a difference in the set theory, depending on whether the set theory is built in [[classical logic]] or in [[constructive logic]]. In the latter, the set theory is called **[[constructive set theory]]**. In order to make sure that classical logic isn't implied by the axioms, certain axioms, such as the [[axiom of choice]], cannot be accepted in classical logic. 

## Material vs structural set theory
   {#MaterialSetTheory}

On the $n$Lab we like to distinguish between two types of set theory, especially in foundations:

*  In a __[[material set theory]]__ (also called a _membership-based set theory_), the elements of a set exist independently of that set.  As such, it makes sense to take two completely unrelated sets and ask if two of their members are [[equal]], and sometimes the answer will be Yes.  Frequently in material set theory one takes everything to be a [[pure set]], so that elements of sets are themselves sets.  Therefore, any two sets may be meaningfully compared to ask if they are equal or if one is a member of the other.

*  A __[[structural set theory]]__, on the other hand, looks more like [[type theory]].  Here, the elements of a set have no existence or structure apart from their identity as elements of that set.  In particular, they are not themselves sets, and cannot be elements of any *other* set, at least not without invoking some explicit [[type casting|type-casting]] operator (which here could simply be a [[function]] from one set to the other).  Similarly, elements of different sets cannot be compared to each other (without type-casting them to become elements of the same set).

Among category theorists, it\'s popular to state the axioms of a structural set theory by specifying elementary properties of [[Set|the category of sets]]; the orthodoxy here (to the extent that there is one) is probably [[Bill
Lawvere]]\'s [[ETCS]], which suffices for most everyday uses but must be supplemented to handle some esoteric parts of modern mathematics.  Another structural set theory, which is stronger than ETCS and less closely tied to category theory, is [[SEAR]].

In contrast, [[ZFC]] is an example of a material set theory.  From a model of either kind of set theory we can construct a model of the other, so the two are, broadly speaking, equivalent; for example, SEARC (SEAR with the [[axiom of choice]]) is equivalent in this way to ZFC, while ETCS is equivalent to a weak ('bounded') variation of ZFC.  A more precise statement is that the two kinds of theories form categories related by the [[material-structural adjunction]].


## Category theory on set theory

Category theory can provide a common [[model theory]] to compare various set theories.  Although only structural set theories like ETCS treat the elementary properties of the category $Set$ of sets as fundamental, one can ask for any set theory what properties $Set$ satisfies and compare them in those terms.  At the very least, $Set$ should be a [[pretopos]].

There is also [[algebraic set theory]], in which a material set theory is interpreted in the [[internal logic]] of some [[ambient category]], often called a "category of classes".  See also [[stack semantics]].


## Related concepts

* [[foundational axiom]]

* [[type theory]]

* [[constructive set theory]]

* [[algebraic set theory]]

* [[descriptive set theory]]

* [[internal logic of set theory]]

* [[set-theoretic multiverse]]

* [[foundations of mathematics]]

  * [[New Foundations]]

  * [[univalent foundations of mathematics]]


## Literature

### Historical

* {#Peirce1885} [[Charles Sanders Peirce]], *On the Algebra of Logic: A Contribution to the Philosophy of Notation*, American Journal of Mathematics **7** (1885)

* [[Felix Hausdorff]], *[[Grundzüge der Mengenlehre]]*, Leipzig: Veit (1914) &lbrack;:ISBN:978-0-8284-0061-9&rbrack; Reprinted by Chelsea Publishing Company (1944, 1949, 1965) &lbrack;[ark:/13960/t2891gn8g](https://archive.org/details/grundzgedermen00hausuoft/page/n5/mode/2up)&rbrack;


* {#Brady2000} Geraldine Brady (2000), From Peirce to Skolem: A Neglected Chapter in the History of Logic, North-Holland/Elsevier Science BV, Amsterdam, Netherlands.

### General

* [[Kenneth Kunen]], _Set theory,an introduction to independence proofs_, North-Holland.

* {#LawvereRosebrugh} [[William Lawvere]], [[Robert Rosebrugh]], _[[Sets for Mathematics]]_ , Cambridge UP  2003. ([web](http://books.google.de/books?id=h3_7aZz9ZMoC&pg=PP1&dq=sets+for+mathematics))

* [[Andreas Blass]], [[Yuri Gurevich]], *Why Sets?*, Bull. Europ. Assoc. Theoret. Comp. Sci. **84** (2004) 139-156.  &lbrack;[doi:10.1007/978-3-540-78127-1_11](https://doi.org/10.1007/978-3-540-78127-1_11), [pdf](https://web.eecs.umich.edu/~gurevich/Opera/172.pdf), [pdf](http://www.math.lsa.umich.edu/~ablass/set.pdf)&rbrack;

  > (with commentary on [[ETCC]])

* {#Shulman18} [[Michael Shulman]], _Comparing material and structural set theories_ ([arXiv:1808.05204](https://arxiv.org/abs/1808.05204))

### In homotopy type theory
 {#ReferencesInHomotopyTypeTheory}

Formalization of set theory in [[homotopy type theory]] (via [[h-sets]]) is discussed in 

* [[Egbert Rijke]], [[Bas Spitters]], _Sets in homotopy type theory_ ([arXiv:1305.3835](http://arxiv.org/abs/1305.3835))

* [[Univalent Foundations Project]], section 3 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

* J&#233;r&#233;my Ledent, _Modeling set theory in homotopy type theory_ (2014) ([pdf](http://perso.ens-lyon.fr/jeremy.ledent/internship_report.pdf))

* Håkon Robbestad Gylterud, Elisabeth Bonnevier, _Non-wellfounded sets in homotopy type theory_ ([arXiv:2001.06696](https://arxiv.org/abs/2001.06696))

See also at [[homotopy type theory FAQ]] _[What is HoTT? -- For set theorists](homotopy+type+theory+FAQ#WhatIsHoTTForSetTheorists)_.


[[!redirects set theory]]
[[!redirects set theories]]