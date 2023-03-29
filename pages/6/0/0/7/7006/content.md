
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

What [[homotopy type theory]] is for [[homotopy theory]]/[[(∞,1)-category theory]], _directed homotopy type theory_ is (or should be) for [[directed homotopy theory]]/[[(∞,n)-category]] [[higher category theory|theory]].

More in detail: Where 

* the [[types]] of [[homotopy type theory]] have [[relation between category theory and type theory|interpretation]] as [[∞-groupoids]] aka [[(∞,0)-categories]]  (and more generally: as [[∞-stacks]]), so that [[homotopy type theory]] itself is an [[internal language]] for the [[(∞,1)-categories]] (specifically, for [[univalence axiom|univalent HoTT]]: [[(∞,1)-toposes]]) that these [[(∞,0)-categories]] form

so

* the [[types]] of directed homotopy type theory ought to have [[relation between type theory and category theory|interpretation]] as [[(∞,n)-categories]] for some $n \in \{1, 2, \cdots, \infty\}$ (and more generally: as [[(∞,n)-sheaves|(∞,n+1)-sheaves]]) so that directed homotopy type theory itself should be an [[internal language]] for the [[(∞,n)-category|(∞,n+1)-categories]] (and in the suitably directed [[univalence axiom|univalent]] case: [[(∞,n)-toposes|(∞,n+1)-toposes]]) that these (geometric) [[(∞,n)-categories]] form.

A proposal for the case $n = \infty$ (potentially describing [[(∞,∞)-categories]] aka [[omega-categories]]) is *[[opetopic type theory]]*, going back to [Finster (2012)](#opetopic+type+theory#Finster12).

A proposal for the case $n = 1$ with the directed analog of the [[univalence axiom]] included --- hence for a type theory whose types may be interpreted as [[(∞,1)-categories]]/[[(∞,2)-sheaves]] and which itself would be the [[internal language]] of the [[(∞,2)-category|$(\infty,2)$-categories]]/[[(∞,2)-topos|$(\infty,2)$-toposes]] that these form --- is announced in [Cisinski et al. (2023)](#CisinskiEtAl23).

## Related concepts

* [[directed type theory]], [[2-type theory]]

* [[opetopic type theory]]

* [[semi-simplicial type]]

* [[geometric homotopy type theory]]

* [[modal homotopy type theory]]

* [[fibered category theory]]

## References

* [[Robert Harper]], [[Dan Licata]], _Canonicity for 2-Dimensional Type Theory_ ([pdf](http://www.cs.cmu.edu/~drl/pubs/lh112tt/lh112tt.pdf))

* [[Robert Harper]], [[Dan Licata]], _2-Dimensional directed dependent type theory_ ([pdf](http://www.cs.cmu.edu/~drl/pubs/lh102dtt/lh102dtt.pdf) [slides](http://www.cs.cmu.edu/~drl/pubs/lh102dtt/lh102dtt-slides.pdf))

* [[Michael Warren]], _Directed Type Theory_ ([video lecture](https://video.ias.edu/univalent/1213/0410-MichaelWarren))

* [[Dan Licata]], Chapters 7 and 8 of _Dependently Typed Programming with Domain-Specific Logics_ PhD thesis, ([pdf](http://www.cs.cmu.edu/~drl/pubs/thesis/thesis.pdf))

* [[Andreas Nuyts]], _Towards a Directed Homotopy Type Theory based on 4 Kinds of Variance_, [PDF](https://anuyts.github.io/files/mathesis.pdf)

* [[Emily Riehl]], [[Mike Shulman]], *A type theory for synthetic ∞-categories*, Higher Structures **1** 1 (2017) &lbrack;[arxiv:1705.07442](https://arxiv.org/abs/1705.07442), [published article](https://higher-structures.math.cas.cz/api/files/issues/Vol1Iss1/RiehlShulman)&rbrack;

* [[Paige Randall North]], _Towards a directed homotopy type theory_ &lbrack;[arXiv:1807.10566](https://arxiv.org/abs/1807.10566)&rbrack;

* [[Alex Kavvos]], *A quantum of direction* (2019) &lbrack;[pdf](https://seis.bristol.ac.uk/~tz20861/papers/meio.pdf)&rbrack;


* {#CisinskiEtAl23} [[Denis-Charles Cisinski]], Hoang Kim Nguyen. Tashi Walde: *Univalent Directed Type Theory*, lecture series in the *[CMU Homotopy Type Theory Seminar](https://www.cmu.edu/dietrich/philosophy/hott/seminars/index.html)* (13, 20, 27 Mar 2023) &lbrack;[web](https://www.cmu.edu/dietrich/philosophy/hott/seminars/index.html#230313), video 1:[YT](https://www.youtube.com/watch?v=5YOltuTcBK8), 2:[YT](https://www.youtube.com/watch?v=xWmELBvHMPo), 3:[YT](https://www.youtube.com/watch?v=P0Cfb4eUJo4); slides 0:[pdf](https://www.cmu.edu/dietrich/philosophy/hott/seminars/slides/cisinski-nguyen-walde-intro_talk1.pdf), 1:[pdf](https://www.cmu.edu/dietrich/philosophy/hott/seminars/slides/cisinski-nguyen-walde-talk1.pdf), 2:[pdf](https://www.cmu.edu/dietrich/philosophy/hott/seminars/slides/cisinski-nguyen-walde-talk2.pdf), 3:[pdf](https://www.cmu.edu/dietrich/philosophy/hott/seminars/slides/cisinski-nguyen-walde-talk3.pdf)&rbrack;

  > **Abstract:** We will introduce a version of [[dependent type theory]] that is suitable to develop a [[synthetic mathematics|synthetic]] theory of [[1-categories]]. The [[axioms]] are both a [[fragment]] and an extension of ordinary [[dependent type theory]]. The [[axioms]] are chosen so that [[(∞,1)-category theory]] (in the form of [[quasi-categories]] or [[complete Segal spaces]]) gives a [[categorical semantics|semantic interpretation]], in a way which extends [[Vladimir Voevodsky|Voevodsky]]'s interpretation of [[univalence axiom|univalent]] [[dependent type theory]] in the [[homotopy theory]] of [[Kan complexes]]. More generally, using a slight generalization of [Shulman's methods](relation+between+type+theory+and+category+theory#Shulman19), we should be able to see that the theory of [[internal (∞,1)-category|(∞,1)‑categories internally]] in any [[(∞,1)-topos|∞‑topos]] (as [developed by Martini and Wolf](internal+infinity1-category#ReferencesInternalToInfinityTopos)) is a [[categorical semantics|semantic interpretation]] as well (hence so is [[Parametrized Higher Category Theory and Higher Algebra|parametrized higher category theory]] introduced by Barwick, Dotto, Glasman, Nardin and Shah). There are of course strong links with [[∞-cosmoi]] of Riehl and Verity as well as with [[cubical type theory|cubical HoTT]] (as strongly suggested by the work of Licata and Weaver), or [[simplicial type theory|simplicial HoTT]] (as in the work of Buchholtz and Weinberger). We will explain the axioms in detail and have a glimpse at basic theorems and constructions in this context ([[(∞,1)-Yoneda lemma|Yoneda Lemma]], [[(∞,1)-Kan extension|Kan extensions]], [[localization of an (∞,1)-category|Localizations]]). We will also discuss the perspective of reflexivity: since the theory speaks of itself (through directed [[univalence axiom|univalence]]), we can use it to justify new deduction rules that express the idea of working up to [[equivalence]] natively (e.g. we can produce a logic by rectifying the idea of having a locally cartesian type). In particular, this logic can be used to produce and study [[categorical semantics|semantic interpretations]] of [[HoTT]].

[[!redirects directed homotopy type theories]]

[[!redirects directed homotopy type]]
[[!redirects directed homotopy types]]
