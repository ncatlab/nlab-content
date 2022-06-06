A list of (believed to be) open problems in homotopy type theory.  To add more detail about a problem (such as why it is hard or interesting, or what ideas have been tried), make a link to a new page.

# Contents
* table of contents
{: toc}

## Semantics

* Construct a [[model of type theory in an (infinity,1)-topos]]. What remains open is the issue of weak Tarski universes.

* Construct an [[(infinity,1)-topos]], or precisely an [[elementary (infinity,1)-topos]], out of (the syntactic category of) a system of type theory. Kapulkin [1507.02648](http://arxiv.org/abs/1507.02648) has shown that we obtain a locally cartesean closed quasicategory. [[Urs Schreiber]] proposed the following question:
"Given an (infinity-)functor from (any flavor of) homotopy type theories to infinity-categories as above, characterize its essential image."

* Define a notion of [[elementary (infinity,1)-topos]] and show that any such admits a model of homotopy type theory.

* [[Semantics]] for strict [[resizing rules]]. Probably refers to the rules introduced in Voevodsky's [Bergen lecture](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations_files/2011_Bergen.pdf), as opposed to the ones in the book.

* Construct (higher) [[inductive-recursive type|inductive-recursive types]] in univalent models, or show that they don't exist.

* Connect [[univalence]] and [[parametricity]] as suggested [here](http://bentnib.org/dtt-parametricity.pdf). One answer is [here](https://arxiv.org/abs/1909.05027).

* Show that when the construction of the [[cumulative hierarchy]] in chapter 10 of the book is interpreted in the [[simplicial set model]], it reproduces (up to equivalence) the usual cumulative hierarchy of the ambient ZFC.  Conclude that if HoTT+AC proves that the cumulative hierarchy satisfies some statement of set theory, then that statement follows from ZFC; see also [this comment](http://math.andrej.com/2014/01/13/univalent-foundations-subsume-classical-mathematics/comment-page-1/#comment-34342) and surrounding discussion.

* The [[model invariance problem]]: show that the interpretation of type theory is independent of the [[model category]] chosen to present an [[(infinity,1)-category]].

* Treat co-inductive types in HoTT. Part of the problem is that general co-inductive types are not fully understood in ordinary type theory.
Using extensionality, we obtain [[M-types]] from W-types.

## Metatheory

* "Writing all inductive definitions in terms of Sigma-types and W-types is theoretically possible, but extremely tedious ... it’s unknown whether any similar reduction for HITs is possible." ([source](http://homotopytypetheory.org/2014/06/08/hiru-tdd/))

* Give a [[computational interpretation]] of univalence and HITs. The cubical set model makes progress on this. [PDF](http://www.cse.chalmers.se/~coquand/mod1.pdf)

* Is there a [[cubical type theory]] that describes more exactly what happens in the [[model of type theory in cubical sets]]? Partial solutions: the [cubical language](https://github.com/simhu/cubical), [this](http://dlicata.web.wesleyan.edu/pubs/lb14cubical/lb14cubes-oxford.pdf) and [this](http://www.cs.nott.ac.uk/~txa/publ/ctt.pdf)

* Show in HoTT that the $n^{th}$ universe is a model of HoTT with $(n-1)$ universes. Part of this question is: what is an [internal model of HoTT](http://homotopytypetheory.org/2014/03/03/hott-should-eat-itself/).

* What is the [[proof theoretic strength of univalent type theory plus HITs]]? In particular, can they be predicatively justified? One could start by considering simple classes of HITs; e.g. [here](http://reports-archive.adm.cs.cmu.edu/anon/2014/CMU-CS-14-101R.pdf) before continuing to, say, pushouts, the cumulative sets, the Cauchy reals and the surreals.

* Is univalence consistent with Induction-Recusion? This would allow us to build a non-univalent universe inside a univalent one. Related to this, higher inductive types [can](http://homotopytypetheory.org/2014/06/08/hiru-tdd/) be used to define a univalent universe.

* Consider the type theory with a sequence of universes plus for each $n\gt 0$, an axiom asserting that there are [[n-type|n-types]] that are not $(n-1)$-types; see [here](http://arxiv.org/abs/1311.4002). Does adding axioms asserting that each universe is [[univalence|univalent]] increase the logical strength? Of course, univalence gives funext.

* Prove or disprove the conjecture that every fibrant type in [[HTS]] is equivalent to one definable in [[Martin-Löf Type Theory|MLTT]].  A potential method of disproof would be to solve the [[model invariance problem]] positively for MLTT but negatively for fibrant types in HTS.

## Homotopy theory and algebraic topology

* [[Homotopy theory in HoTT]]

* Similarly to the torus, consider the projective plane, Klein bottle, ... as discussed in the book (sec 6.6). Show that the Klein bottle is not orientable.  (This requires defining "orientable".)
    * This also requires defining what a surface is.

* What is the [[loop space of a wedge of circles]] indexed by a set without decidable equality?

* Calculate more [[homotopy groups of spheres]].

* Show that the [[homotopy groups of spheres]] are all finitely generated, and are finite with the same exceptions as classically.

    * The classical proof requires Hurewicz, and now that spectral sequences are around should be possible.

* Define the Hurewicz map and prove the Hurewicz theorem

* Define the Toda bracket.

* Prove that $n$-spheres are $\infty$-truncated.

* Prove that $S^2$ is not an $n$-type.

* Define the/a delooping of $S^3$.

* Can we verify [computational algebraic topology](http://www-fourier.ujf-grenoble.fr/~sergerar/Kenzo/) using HoTT?

* Bott periodicity

* Develop synthetic stable homotopy theory

## Higher algebra and higher category theory

* Define [[semi-simplicial type|semi-simplicial types]] in type theory, or show that this is not possible. Define [[Segal space]] [[complete Segal space]].

* Define a [[weak omega-category in type theory]].

* Is it possible to have limits be judgmentally the same as opposite colimits, and simultaneously have (co)limits be judgmentally the same as particular Kan extensions.  As partially detailed [on an issue on the HoTT/HoTT repo](https://github.com/HoTT/HoTT/issues/284), part of the problem is that the functor ᵒᵖ : (D → C)ᵒᵖ → (Dᵒᵖ → Cᵒᵖ) has a judgmental inverse (the composition is judgmentally the identity functor on objects and morphisms), and, assuming univalence, the precategories (D → C)ᵒᵖ and (Dᵒᵖ → Cᵒᵖ) are propositionally but not judgmentally equal.

* [[Eric Finster, Towards Higher Universal Algebra in Type Theory]]

* Construct the first 8 $\mathbb{N}$-indexed families of $\infty$-groups in the [[Whitehead tower]] of the [[orthogonal group]]s. 

## Other mathematics

* What axioms of set theory are satisfied by the [[HIT model of ZFC]] constructed in chapter 10 of the book?  For instance, does it satisfy collection or REA?

* Are any of the stronger forms of the [[axiom of choice]] mentioned in the book (ex 7.8) consistent with univalence?

* Do the higher inductive-inductive [[real numbers]] from the book coincide with the Escardo-Simpson reals, [here](http://www.cs.bham.ac.uk/~mhe/papers/lics2001-revised.pdf) and [here](http://www.cs.bham.ac.uk/~mhe/papers/realadt.pdf)? [Solved](https://arxiv.org/abs/1706.05956) by Auke Booij using resizing/impredicativity. Can a predicative treatment be obtained from hSets as a predicative topos (by [Rijke/Spitters](http://arxiv.org/abs/1305.3835)) and the predicative [formalization](https://arxiv.org/abs/1610.05072) of Cauchy reals by Gilbert.

* Can multiplication be defined for the higher inductive-inductive [[surreal numbers]] from the book?

* Can Rezk complete categories remove the non-constructivity from the applications of the Freyd Adjoint Functor theorem? ([[faft.txt:file]])

* Is there a predicative and constructive abstract definition of the category of real Hilbert spaces, in a similar fashion as what Chris Heunen and Andre Kornell did in classical mathematics in their article ([Axioms for the category of Hilbert spaces](https://arxiv.org/abs/2109.07418))? Solér's theorem, which is used in their proof, is only valid in classical mathematics.

## In cohesive homotopy type theory

* Assuming [[axiom R-flat]], is the [[shape]] of every [[subset]] of the [[Dedekind real numbers]] a [[set]]? 

* Assuming [[axiom R-flat]] and [[excluded middle]], prove that the [[analytic Markov's principle]] is true. 

* What is the $(\infty,1)$-topos theoretic interpretation of [[axiom R-flat]]?

* Prove the approximate [[intermediate value theorem]] in [[Mike Shulman]]'s  [model of cohesive homotopy type theory](https://arxiv.org/abs/1509.07584) without resorting to crispness. 

* Formalize $\infty$-[[Chern-Weil theory]] internally in cohesive homotopy type theory. (See [arxiv:1310.7930](https://arxiv.org/abs/1310.7930) for an external presentation in $(\infinity,1)$-category theory)

* Construct a model of the 3+1 dimensional [[quantum gauge field theory]] of [[quantum electrodynamics]] in cohesive homotopy type theory. 

## Formalization

* Formalize the construction of models of type theory using contextual categories.

* Formalize [[semi-simplicial types]].

* Formalize $\infty$-groupoids, $\infty$-categories within HoTT.

* Formalize what remains to be done from chapters 8, 10, and 11 of the book.
  In particular, develop the Higher Inductive-Inductive real numbers in some language, such as Coq (the basics of the surreal numbers have been done).

  In general, [this file](https://github.com/HoTT/HoTT/blob/master/contrib/HoTTBook.v) contains a Coq outline of the book. Instructions for how to contribute are [here](https://github.com/HoTT/HoTT/blob/master/README.markdown).

## Other lists of open problems

* Coquand's five open problems:
Coquand listed five open problems [here](https://eutypes.cs.ru.nl/eutypes_pmwiki/uploads/Meetings/Coquand.pdf)

* Open problems stated at the HoTT2019 Summer School [[HoTT2019 Summer School open problems list]]

* [Interpretation of Coq in higher toposes](https://cstheory.stackexchange.com/questions/44403/model-of-coq-pcuic-in-higher-toposes).

## Closed problems

+-- {: .query}
How about keeping a running list of solutions like this:?

Maybe only things not in the HoTT book?  Else the list of solved problems gets very long!

OK, here's the rule: if it was stated here (or on the UF-wiki) as an open problem, then it gets recorded here once it's solved.
=--

* There is a [[nlab:model structure on semi-simplicial sets]].

* Prove that the [[torus]] (with the HIT definition involving a 2-dimensional path) is equivalent to a product of two circles. See Sojakova's proof: [[torus.pdf:file]]. A shorter formalized proof is [here](http://homotopytypetheory.org/2015/01/20/ts1s1-cubically/)

* Construct the Hopf fibration. (Lumsdaine gave the construction in 2012 and Brunerie proved it was correct in 2013.)

* Construct the "super [[Hopf fibration]]" (AKA [[nlab:quaternionic Hopf fibration]]) $S^3 \to S^7 \to S^4$. (Buchholtz and Rijke solved this early 2016 through a [homotopy version of the Cayley-Dickson construction](https://arxiv.org/abs/1610.01134).)

*  Prove the [[Seifert-van Kampen theorem]]. (Shulman did it in 2013.)

* Construct Eilenberg--MacLane spaces and use them to define cohomology. (Licata and Finster did it in 2013, written up in [this paper](http://dlicata.web.wesleyan.edu/pubs/lf14em/lf14em.pdf) (pdf).)


* Define the Whitehead product.
Guillaume Brunerie did this in 2017, written up in [this paper](https://arxiv.org/abs/1710.10307). He also gives a constructive proof of $\pi_4( S^3)= Z/n Z$ for some $n$ and a construction of the [reduced James product](https://ncatlab.org/nlab/show/EHP+spectral+sequence#via_the_james_model) as a HIT and a homotopy colimit. It is also proven that $\Omega \Sigma X \simeq J(X)$ for some pointed connected type $X$. All of these constructions can be found in detail in [his thesis](https://arxiv.org/abs/1606.05916).