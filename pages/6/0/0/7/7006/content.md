
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Directed Type Theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
#### $(\infty,2)$-Topos theory
+--{: .hide}
[[!include (infinity,2)-topos theory - contents]]
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

## Appeal and practicality

One obvious reason for studying directed homotopy type theory (especially when $n = \infty$ in the above) is generality:  $(\infty,\infty)$-categories are among the most general higher categorical structures. Besides this reason, access to higher directed structure may offer, in particular, the following conceptual advantages.

* _Universe types can retain their higher directed structure._ [[type universe|Universe types]] are (small) 'internal' reflections of the category of all types of our type theory, but without sufficient higher structure in the theory, this reflection process must forget structure present in the external category (for instance, the [[category of sets]] can only contain a 'set of sets' as an object which does not remember functions; similarly, the universe type in [[homotopy type theory]] must forget about maps between types that are not equivalences).

* _Dependent function types become 'just' function types._ In the presence of higher directed structure, equipped with a universe type $\mathcal{U}$ and unit type $\mathbf{1}$, dependent function types $\Pi_{x : A} F(x)$, for $F$ a type family $F : A \to \mathcal{U}$, can be understood in terms of 'just' function types, namely, as $\mathsf{Fun}_{\mathsf{Fun}(A,\mathcal{U})}(\mathrm{const}_{\mathbf{1}}, F)$ (where $\mathrm{const}_{\mathbf{1}} : A \to \mathcal{U}$ is the constant functor with image $\mathbf{1}$).

* _Inductive types become substantially more expressive._ Inductive types with dependent constructors can also be expressed in terms of non-dependent constructors: for instance, for $F$ a type family $F : A \to \mathcal{U}$, the dependent pair type $\Sigma_{x : A} F(x)$ can be introduced with a single constructor $\mathrm{in} : F \to \mathrm{const}_{\Sigma_{x : A} F(x)}$ (which is a map in the function type $\mathsf{Fun}(A, \mathcal{U})$ and should thus be thought of as a natural transformation between functors). Moreover, there is the topic of [[higher inductive types]]; a useful example of a 'true' directed higher inductive type is the [[poset]] type $(\mathbb{N},\leq)$ with constructors
$$ 0 : \mathbf{1} \to \mathbb{N} $$
$$ \mathsf{succ} : \mathbb{N} \to \mathbb{N} $$
$$ \mathsf{less} : \id_{\mathbb{N}} \to \mathsf{succ} $$

* _Formalization of (higher) categorical semantics._ On a more practical side, access to higher directed structure could allow us to formalize the categorical semantics of other types theories, such as [[homotopy type theory]], as discussed in [Cisinki et al 2023](https://ncatlab.org/nlab/show/directed+homotopy+type+theory#CisinskiEtAl23).

On the other hand, working directed higher type theory may not be very practical. 

* While it is clear that one eventually wants to speak about higher categorical concepts with type theory, it is not a priori clear that this motivates the dedicated formulation of new rules for directed higher type theory: it might still be more convenient to instead work internal to ordinary [[homotopy type theory]].

* More generally, it has been argued that directed higher type theories may not aid the practical usability of proof assistants due to the potential complexity of the rules involved.

## Related concepts

* [[directed univalence axiom]]

* [[directed type theory]], [[2-type theory]]

* [[opetopic type theory]]

* [[semi-simplicial type]]

* [[geometric homotopy type theory]]

* [[modal homotopy type theory]]

* [[fibered category theory]]

## References

### General

* [[Robert Harper]], [[Dan Licata]], _Canonicity for 2-Dimensional Type Theory_ ([pdf](http://www.cs.cmu.edu/~drl/pubs/lh112tt/lh112tt.pdf))

* [[Robert Harper]], [[Dan Licata]], _2-Dimensional directed dependent type theory_ ([pdf](http://www.cs.cmu.edu/~drl/pubs/lh102dtt/lh102dtt.pdf) [slides](http://www.cs.cmu.edu/~drl/pubs/lh102dtt/lh102dtt-slides.pdf))

* [[Michael Warren]], _Directed Type Theory_ ([video lecture](https://video.ias.edu/univalent/1213/0410-MichaelWarren))

* [[Dan Licata]], Chapters 7 and 8 of _Dependently Typed Programming with Domain-Specific Logics_ PhD thesis, ([pdf](http://www.cs.cmu.edu/~drl/pubs/thesis/thesis.pdf))

* [[Emily Riehl]], [[Mike Shulman]], *A type theory for synthetic ∞-categories*, Higher Structures **1** 1 (2017) &lbrack;[arxiv:1705.07442](https://arxiv.org/abs/1705.07442), [published article](https://higher-structures.math.cas.cz/api/files/issues/Vol1Iss1/RiehlShulman)&rbrack;

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

* [[Paige Randall North]], _Towards a directed homotopy type theory_ &lbrack;[arXiv:1807.10566](https://arxiv.org/abs/1807.10566)&rbrack;

* [[Alex Kavvos]], *A quantum of direction* (2019) &lbrack;[pdf](https://seis.bristol.ac.uk/~tz20861/papers/meio.pdf)&rbrack;

* {#Nuyts24} [[Andreas Nuyts]], _Higher Pro-arrows: Towards a Model for Naturality Pretype Theory_, HoTTEST seminar, May 2, 2024, [Slides](https://anuyts.github.io/files/2024/natpt-hottest-pres.pdf), [Video](https://youtu.be/jcaG18oicP8)

* {#Nuyts23} [[Andreas Nuyts]], _Higher Pro-arrows: Towards a Model for Naturality Pretype Theory_, HoTT/UF 2023, [PDF](https://hott-uf.github.io/2023/HoTTUF_2023_paper_1410.pdf), [Slides](https://anuyts.github.io/files/2023/natpt-hott-uf-pres.pdf), [Video](https://youtu.be/kw82hW-FlBc)

* [[Andreas Nuyts]], _Towards a Directed Homotopy Type Theory based on 4 Kinds of Variance_, 2015, [PDF](https://anuyts.github.io/files/mathesis.pdf)

### Cisinski et al.
 {#ReferencesCisinskiEtAl}

* {#CisinskiEtAl23} [[Denis-Charles Cisinski]], [[Hoang Kim Nguyen]], Tashi Walde: *Univalent Directed Type Theory*, lecture series in the *[CMU Homotopy Type Theory Seminar](https://www.cmu.edu/dietrich/philosophy/hott/seminars/index.html)* (13, 20, 27 Mar 2023) &lbrack;[web](https://www.cmu.edu/dietrich/philosophy/hott/seminars/index.html#230313), video 1:[YT](https://www.youtube.com/watch?v=5YOltuTcBK8), 2:[YT](https://www.youtube.com/watch?v=xWmELBvHMPo), 3:[YT](https://www.youtube.com/watch?v=P0Cfb4eUJo4); slides 0:[pdf](https://www.cmu.edu/dietrich/philosophy/hott/seminars/slides/cisinski-nguyen-walde-intro_talk1.pdf), 1:[pdf](https://www.cmu.edu/dietrich/philosophy/hott/seminars/slides/cisinski-nguyen-walde-talk1.pdf), 2:[pdf](https://www.cmu.edu/dietrich/philosophy/hott/seminars/slides/cisinski-nguyen-walde-talk2.pdf), 3:[pdf](https://www.cmu.edu/dietrich/philosophy/hott/seminars/slides/cisinski-nguyen-walde-talk3.pdf)&rbrack;

  > **Abstract:** We will introduce a version of [[dependent type theory]] that is suitable to develop a [[synthetic mathematics|synthetic]] theory of [[1-categories]]. The [[axioms]] are both a [[fragment]] and an extension of ordinary [[dependent type theory]]. The [[axioms]] are chosen so that [[(∞,1)-category theory]] (in the form of [[quasi-categories]] or [[complete Segal spaces]]) gives a [[categorical semantics|semantic interpretation]], in a way which extends [[Vladimir Voevodsky|Voevodsky]]'s interpretation of [[univalence axiom|univalent]] [[dependent type theory]] in the [[homotopy theory]] of [[Kan complexes]]. More generally, using a slight generalization of [Shulman's methods](relation+between+type+theory+and+category+theory#Shulman19), we should be able to see that the theory of [[internal (∞,1)-category|(∞,1)‑categories internally]] in any [[(∞,1)-topos|∞‑topos]] (as [developed by Martini and Wolf](internal+infinity1-category#ReferencesInternalToInfinityTopos)) is a [[categorical semantics|semantic interpretation]] as well (hence so is [[Parametrized Higher Category Theory and Higher Algebra|parametrized higher category theory]] introduced by Barwick, Dotto, Glasman, Nardin and Shah). There are of course strong links with [[∞-cosmoi]] of Riehl and Verity as well as with [[cubical type theory|cubical HoTT]] (as strongly suggested by the work of Licata and Weaver), or [[simplicial type theory|simplicial HoTT]] (as in the work of Buchholtz and Weinberger). We will explain the axioms in detail and have a glimpse at basic theorems and constructions in this context ([[(∞,1)-Yoneda lemma|Yoneda Lemma]], [[(∞,1)-Kan extension|Kan extensions]], [[localization of an (∞,1)-category|Localizations]]). We will also discuss the perspective of reflexivity: since the theory speaks of itself (through directed [[univalence axiom|univalence]]), we can use it to justify new deduction rules that express the idea of working up to [[equivalence]] natively (e.g. we can produce a logic by rectifying the idea of having a locally cartesian type). In particular, this logic can be used to produce and study [[categorical semantics|semantic interpretations]] of [[HoTT]].

This is based on the discussion of [[straightening and unstraightening]] entirely within the context of [[quasi-categories]] from

* [[Denis-Charles Cisinski]], [[Hoang Kim Nguyen]], *The universal coCartesian fibration* &lbrack;[arXiv:2210.08945](https://arxiv.org/abs/2210.08945)&rbrack;

which (along the lines of the discussion of the universal left fibration from [Cisinski 2019](universal+left+fibration#Cisinski19)) allows to understand the [[universal coCartesian fibration]] as [[categorical semantics]] for the [[univalence axiom|univalent]] [[type universe]] in [[directed homotopy type theory]] (see [video 3 at 1:16:58](https://youtu.be/P0Cfb4eUJo4?t=4618) and [slide 3.33](https://www.cmu.edu/dietrich/philosophy/hott/seminars/slides/cisinski-nguyen-walde-talk3.pdf#page=33)).

{#CisinskiOnSyntax} But the actual type-theoretic syntax ([[inference rules]]) for this intended semantics remains to be given:

> &lbrack;[[Denis-Charles Cisinski|Cisinski]] in [video 3 at 1:27:43](https://youtu.be/P0Cfb4eUJo4?t=5263)&rbrack;: I won't provide the full [[syntax]] yet and actually I would be very happy to discuss that, because we don't know yet and I have questions myself, actually.

> &lbrack;[[Steve Awodey|Awodey]] in [video 3 at 1:46:23](https://youtu.be/P0Cfb4eUJo4?t=6383)&rbrack;: Maybe I'll suggest something, you tell me if you agree: What we have is a kind of axiomatization of the semantics of a system for type theory, so that we know what exactly we want formalize in the type theory, and what depends on what, and it articulates and structures the intended interpretation of the type theory in a very useful way. Maybe in the way that the axiomatic description of a cartesian closed category was very good to have for formulating the [[lambda-calculus]]. But I think that what we have is more on the side of the axiomatic description of the semantics, like the cartesian closed category, that it is on the side of the lambda-calculus itself. So, maybe I would suggest the term "abstract type theory" to describe this system as an intermediate in between an actual formally implemented system of type theory and the big unclear world of possible semantics and all the different structures that one could try to capture with a type theory, in between is this abstract type theory which specifies a particular structure that we want to capture in our type theory, which is a very very useful methodological step. &lbrack;...&rbrack; I am trying to maybe reconcile:

> Some people would prefer to call a type theory only something which can immediately be implemented in a computer. So that's different than an abstract description of a structure that we would want to describe in such a type theory.


> &lbrack;[[Denis-Charles Cisinski|Cisinski]] in [video 3 at 1:49:28](https://youtu.be/P0Cfb4eUJo4?t=6568)&rbrack;: I agree with what you say but I still have the hope to be able to produce an actual syntax &lbrack;...&rbrack; that's really the goal.

More on the [[directed univalence axiom]] in this context:

* [[Hoang Kim Nguyen]], *Directed univalence in simplicial sets*, talk in *[Homotopy Type Theory Electronic Seminar Talks](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottest.html)* (March 2023) &lbrack;[video](https://www.youtube.com/watch?v=GgcJqzGvq80), [slides](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Nguyen-2023-03-09-HoTTEST.pdf)&rbrack;





[[!redirects directed homotopy type theories]]

[[!redirects directed homotopy type]]
[[!redirects directed homotopy types]]
