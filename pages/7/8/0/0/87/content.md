
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--
=--
=--


# Anafunctors
* automatic table of contents goes here
{:toc}


## Idea

An _anafunctor_ $F : C \to D$ is a generalized [[functor]].

A basic fact in ordinary [[category theory]] is that a [[functor]] $f\colon C \to D$ is an [[equivalence of categories]] -- in that there is a functor $g\colon D \to C$ and natural isomorphisms $f \circ g \simeq Id_D$ and $g \circ f \simeq Id_C$ -- if and only if it is a [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|fully faithful]].  However, the "if" part of this statement depends crucially on the [[axiom of choice]]: the functor $g$ is obtained by _choosing_  for each [[object]] $d \in D$ an object $c \in C$ such that $f(c) \simeq d$.  In fact, the statement that "every fully faithful and essentially surjective functor is an equivalence of categories" is equivalent to the axiom of choice.

The notion of *anafunctor* is a generalization of the usual notion of *functor*, which enables us to recover a version of this statement without the axiom of choice.  It was first studied in detail by [[Michael Makkai]] with foundational concerns in mind, although it also appears unnamed in an earlier paper of Kelly.  Later, they were applied by [[Toby Bartels]] to [[internal category|internal categories]], where the axiom of choice is simply not an option.  These "internal anafunctors" actually turned out to be known already (at least up to equivalence) in some contexts, in particular as [[Hilsum-Skandalis morphism]]s between [[Lie groupoid]]s.

We present three motivations and applications of anafunctors: 

* [Anafunctors as a tool for handling foundational issues](#FoundationalMotivation)

* [Anafunctors as morphisms in internal categories](#InternalCatMotivation)

* [Anafunctors as morphisms in a homotopy category](#HomotopicalMotivation)


### Foundational motivation {#FoundationalMotivation}

There is a sense in which the construction of inverse equivalences is not a "real" use of the axiom of choice, because the choice of $d$ is determined up to unique isomorphism.  Note that in ordinary set theory, the axiom of choice is not necessary to make choices that are uniquely defined; this is sometimes called the "axiom of non-choice" or the "function comprehension principle."  Since in category theory, an object can only be expected to be determined up to unique isomorphism, it is natural to regard the above statement as really being a "functor comprehension principle" or an "axiom of non-choice for categories."  The fact that the full axiom of choice is required to make such choices is then an artifact of the usual [[foundation]]al choice to define categories as having a [[set]] of objects.

In fact, however, we can recover the functor comprehension principle while maintaining the definition of categories in set theory if we modify the notion of *functor*.  This results in the notion of _anafunctor_, which is essentially "a functor which determines its values on objects only up to isomorphism."  In particular, an anafunctor is an [[equivalence of categories]] (in the sense of having an inverse *anafunctor*) precisely if it is essentially surjective and full and faithful.  From this point of view, an anafunctor is not necessarily a fundamental notion, but rather an artifact that makes it possible to approximate the "natural" theory of categories, which doesn't need choice but has a functor comprehension principle, while still working in a set-theoretic foundation lacking choice.
   
Every functor may be interpreted as an anafunctor; that every anafunctor is equivalent to a functor is equivalent to the [[axiom of choice]], in which case the inclusion of functors into anafunctors is in fact an [[equivalence of categories]]. But if you ignore functors and deal only with anafunctors (or saturated anafunctors), then the theory becomes entirely [[constructive mathematics|constructive]] (without using the axiom of choice or even [[excluded middle]]).  Thus, anafunctors (or even saturated anafunctors) are the correct notion to use if you are doing [[constructive mathematics]] and you still want to [[foundations|found]] mathematics on some sort of [[set theory]].

  
### Motivation from internal categories {#InternalCatMotivation}

Since questions concerning the axiom of choice tend to look a bit esoteric to those not actively interested in questions of [[foundations]], it is helpful (and useful!) to think of this more generally in terms of [[internal category]] theory, where the concept is of independent use, and in fact well known by other names than "anafunctor".  Consider some ambient category $\mathcal{E}$ [[internalization|internal]] to which we want to do category theory. A good example to keep in mind is the category [[Top]] of [[topological space]]s.  We observe that "the axiom of choice fails in [[Top]]", but that this is a very non-esoteric and obvious statement: it just means that not every continous [[epimorphism]] $P \to X$ between topological spaces has a _continuous_ [[section]].

Then it may easily happen that an internal functor $f\colon C \to D$ between [[internal category|internal categories]] in $\mathcal{E}$ (for instance between topological categories) is fully faithful, in the "internal" sense that
$$\array{C_1 & \overset{}{\to} & D_1\\
  \downarrow && \downarrow\\
  C_0 \times C_0 & \underset{}{\to} & D_0\times D_0}$$
is a [[pullback]], and essentially surjective, in the "internal" sense that $C_0 \times_{D_0} Iso(D) \to D_0$ is surjective (or even a quotient map, i.e. a [[regular epimorphism]]), but for which there still does not exist a weak inverse in $Cat(\mathcal{E})$.

For example, let $X$ be a topological space and consider the functor $C(U) \to X$, where $X$ is regarded as an internal category in $Top$ which is [[discrete category|discrete]] in the categorical sense, and $C(U)$ is the [[Cech nerve|Cech groupoid]] associated to an open [[cover]] $X = \bigcup_i U_i$ of $X$.  That means that the space of objects of $C(U)$ is $\coprod_i U_i$, and its space of morphisms is $\coprod_{i,j} (U_i\cap U_j)$.  Then the functor $C(U)\to X$ is fully faithful (essentially by definition of the morphisms in $C(U)$) and essentially surjective (since the $U_i$ are a cover of $X$) in the senses above.  However, in general it does not admit a weak inverse, since the continuous function $\coprod_i U_i \to X$ does not have a continuous section unless one of the $U_i$ is already equal to $X$.

Note that the foundational point of view also fits in this picture; we can simply take $\mathcal{E} = Set_{\not AC}$ to be the category [[Set]] of [[set]]s in a model of set theory that need not satisfy the [[axiom of choice]].  Here the same thing may happen: not every fully faithful and essentially surjective functor has a weak inverse.

### Homotopical motivation {#HomotopicalMotivation}

There is a standard way to deal with such situations where we are faced with a category -- here the category $Cat(\mathcal{E})$ of categories internal to $\mathcal{E}$ -- some of whose morphisms look like they ought to have inverses, but do not: we call these would-be invertible morphisms _weak equivalences_ such that our category becomes a [[category with weak equivalences]] or a [[homotopical category]]. Then we pass to the corresponding [[homotopy category]]: the universal "improvement" of our category such that all the would-be invertible morphism do become invertible.

Here we take the weak equivalences in $Cat(\mathcal{E})$ to be the internal functors that are internally fully faithful and essentially surjective. It turns out that this choice of weak equivalences is particularly well-behaved in that it actually forms a [[calculus of fractions]]. Due to the early work on abstract [[homotopy theory]] by Gabriel and Zisman, there is simple explicit construction of the corresponding [[homotopy category]] $Ho(Cat(\mathcal{E}))$ in this case: the objects are the same as those of $Cat(E)$ -- hence [[internal category|categories internal to]] $\mathcal{E}$ for us -- and the morphisms $f\colon C \to D$ are [[span]]s of morphism in $Cat(\mathcal{E})$

$$
  \array{
    \hat C &\stackrel{\hat f}{\to}& D
    \\
    \downarrow^{\mathrlap{\in W}}
    \\
    C
  }
  \,,
$$

where the left leg is a weak equivalence., hence for us: where the left leg is an internal functor that is $k$-surjective for all $k$.  (This is the beginning of the construction of the [[Dwyer-Kan localization]] at our chosen weak equivalences.)

For the case $\mathcal{E} = Top$ such a span is a morphism out of a _Cech cover_ . For instance for $C = X$ a topological space regarded as a topological category, for $G$ a [[topological group]] and $D = \mathbf{B}G$ its [[delooping]] one-object topological groupoid, such a span is a [[Cech cohomology|Cech cocycle]] on $X$ with values in $G$.

And finally: for the case that $\mathcal{E} = Set_{\not C}$ is the category of sets without the axiom of choice, such a span is an **anafunctor**: a functor $\hat C \to C$ that is is surjective on objects and [[full and faithful functor|full and faithful]], together with a functor $\hat C \to D$ out of the "resolution" of $C$.

So one can understand ordinary anafunctors as follows:

1. first we consider that the [[axiom of choice]] may fail, 
   which makes previously invertible functors  non-invertible;
   
1. then we universally _force_ the now non-invertible functors 
   to become invertible after all,
   by throwing in formal inverses for them.

More generally, in any [[category of fibrant objects]] the morphisms in the [[homotopy category]] are represented by [[span]]s of the form

$$
  \array{
    \hat X &\to & Y
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X 
  }
$$

with the left leg being an acyclic fibration. (This is a special case of the general statements of [[simplicial localization]]). 


## Definitions

Given categories $C$ and $D$, an __anafunctor__ $F\colon C \to D$ may be rather slickly defined as a [[span]] of ordinary ([[strict functor|strict]]) [[functors]] $C \overset{\sigma}\leftarrow \overline{F} \overset{\tau}\rightarrow D$ (where $\overline{F}$ is some category), with the property that the functor $\sigma\colon {\overline{F}} \to C$ is both [[faithful functor|faithful]] and (strictly!) surjective on both objects and morphisms (therefore both [[full functor|full]] and [[essentially surjective functor|essentially surjective on objects]]).  It is also possible to define an anafunctor as a span in which $\sigma$ is merely a [[equivalence of categories|weak equivalence]] (that is, faithful, full, and essentially surjective on objects), although that is slightly more complicated to work with.

### Explicit set-theoretic definition

In more explicit detail, an __anafunctor__ $F\colon C \to D$ consists of:
* a set $|F|$ of __specifications__ of $F$ (which corresponds to the set of objects of $\overline{F}$);
* maps $\sigma\colon |F| \to C$ and $\tau\colon |F| \to D$ (taking values in objects). Given $x\colon C$ and $y\colon D$, we say that $y$ is a __specified value__ of $F$ at $x$ if, for some $s\colon |F|$, $x = \sigma(s)$ and $y = \tau(s)$; in this case, $s$ __specifies__ $y$ as a value of $F$ at $x$, and we write $F_s(x) = y$.  That is,
  $$ F_s(x) \coloneqq \tau(s) .$$
  We say that $y$ is a __value__ of $F$ at $x$ if $y$ is isomorphic (in $D$) to some specified value of $F$ at $x$; we write $F(x) \cong y$. (There is no notion of *the* value of $F$ at $x$, except in the up-to-isomorphism sense of the [[generalised the]], and $F(x) = y$ is a meaningless statement.);
* for each $s, t\colon |F|$ and morphism $f\colon \sigma(s) \to \sigma(t)$ in $C$, a morphism
  $$ F_{s,t}(f)\colon F_s(x) \to F_t(y) $$
  in $D$, where $x \coloneqq \sigma(s)$ and $y \coloneqq \tau(s)$. Similarly to the above, we can define whether a given morphism $g$ in $D$ is a __specified value__ of $F$ at a given morphism $f$ in $C$ or whether $g$ is (merely) a __value__ of $F$ at $f$. (Again, there is no notion of *the* value of $F$ at $f$.);
* $\sigma$ is a [[surjective function]]. Thus, $F$ has *some* value at any given object or morphism of $C$. (In the [[internalization|internalized]] case, this requirement can become quite complicated; for example, internal to [[Diff]], one requires a [[surjective submersion]].);
* $F$ preserves [[identity morphism|identities]]. That is, given $s\colon |F|$, the value of $F$ specified by $s$ and $s$ at the identity of $\sigma(s)$ is the identity of $\tau(s)$, or (in symbols) $F_{s,s}(\id_{\sigma(s)}) = \id_{\tau(s)}$, or (whenever this makes sense)
  $$ F_{s,s}(\id_x) = \id_{F_s(x)} ;$$
* $F$ preserves [[composition]]. That is, given $s, t, u\colon |F|$, $f\colon \sigma(s) \to \sigma(t)$, and $g\colon \sigma(t) \to \sigma(u)$,
  $$ F_{s,u}(f;g) = F_{s,t}(f);F_{t,u}(g) .$$
  (Here the semicolon indicates composition in the anti-Leibniz order.).

From the above explicit data, the category $\overline{F}$ is constructed as follows: the objects of $\overline{F}$ are the elements of $|F|$, while a morphism $s \to t$ in $\overline{F}$ is simply a morphism $\sigma(s) \to \sigma(t)$ in $C$.  Then $\sigma$ extends to a surjective faithful functor from $\overline{F}$ to $C$ (acting as the identity on morphisms), and $\tau$ extends to a functor from $\overline{F}$ to $D$ (mapping the morphism $f\colon s \to t$ in $\overline{F}$ to $F_{s,t}(f)\colon \tau(s) \to \tau(t)$ in $D$).

An anafunctor $F$ is __saturated__ if, whenever $F(x) \cong y$, $F_s(x) = y$ for some unique specification $s$, where the unicity of $s$ depends not only on $x$ and $y$ but also on how $y$ is a value of $F$ at $x$. To be precise: if $g\colon y' \to y$ is an isomorphism in $D$ and $F_{s'}(x) = y'$ for some specification $s'$, then there is a unique specification $s$ such that $F_{s',s}(\id_x) = g$ (where in particular, $\sigma(s) = x$ and $F_s(x) = y$). Every anafunctor $F\colon C \to D$ has a _saturation_ $\overline{F}$; $\overline{F}$ is a saturated anafunctor and $F \cong \overline{F}$ in the category of anafunctors from $C$ to $D$. In fact, the inclusion of the saturated anafunctors into the anafunctors (as a full subcategory) is an equivalence of categories (given fixed $C$ and $D$).

Categories, anafunctors, and a suitably defined notion of [[ananatural transformation]] between them form a [[bicategory]] $Cat_{ana}$; an internal [[equivalence]] in this 2-category is called an **anaequivalence**.  Every functor may be interpreted as an anafunctor, with $|F|$ always taken to be (the set of objects in) $C$ itself and $\sigma$ the [[identity functor]].  Indeed, there is a [[2-functor]] to $Cat_{ana}$ from the [[strict 2-category]] $Str Cat$ of categories, functors and natural transformations; this functor is an [[equivalence of categories|equivalence]] if and only if the [[axiom of choice]] holds.  Thus, most mathematicians will identify $Cat_{ana}$ and $Str Cat$ as simply [[Cat]], the $2$-category of categories; however, mathematicians who doubt the axiom of choice will distinguish them.  While anafunctors exist in any case, there is an ideological statement that may be implied by their use: that $Cat$ is *really* $Cat_{ana}$ rather than $Str Cat$.

In any case, (modulo "size issues" which one may want to impose) the inclusion of $Str Cat$ into $Cat_{ana}$ has a right adjoint, described using [[clique]]s. Accordingly, we can instead define anafunctors by means of clique categories, taking an anafunctor from $C$ into $D$ to be a genuine functor from $C$ into $Clique(D)$ (and the 2-category of anafunctors as the Kleisli category for the $Clique(-)$ 2-monad (in particular, natural transformations between anafunctors into $D$ are simply natural transformations of the corresponding genuine functors into $Clique(D)$)).

### Internal definition using covers

We generalise the slick definition of anafunctors as spans rather than the detailed definition involving specified values.

Let $S$ be a category containing a collection of morphisms called "covers" such that

* every [[isomorphism]] is a cover,
* covers are closed under composition,
* any [[pullback]] of a cover exists and is a cover ([[pullback stability]]),
* every cover is the [[quotient object]] of its [[kernel pair]], i.e. is an [[effective epimorphism]].  (Since all pullbacks of covers exist, this is equivalent to saying that every cover is a [[regular epimorphism]].)

Note that these are precisely the axioms saying that the singleton families $\{p\colon V\to U\}$ where $p$ is a cover form a [[subcanonical coverage|subcanonical]] [[Grothendieck pretopology]].  One important class of examples is when $S$ is a [[regular category]] and the covers are the [[regular epimorphisms]].  Another is when $S$ is the category of smooth manifolds and the covers are the surjective submersions.

In such a situation, if $C$ and $D$ are [[internal category|internal categories]] in $S$, we define an __anafunctor__ $C\to D$ to consist of a span $C\leftarrow F \to D$ of internal functors such that:

1. $F_0\to C_0$ (the map of objects) is a cover.

2. $F\to C$ is [[ff morphism|fully-faithful]], in the internal sense that the following is a pullback square:
$$\array{F_1 & \to & C_1 \\ \downarrow && \downarrow \\ F_0\times F_0&   \to & C_0\times C_0}$$

Note that assuming $F_0\to C_0$ is a cover, so is $F_0\times F_0\to C_0\times C_0$ (it is a composition of pullbacks of $F_0\to C_0$); thus the above pullback always exists.

By the remarks above, if $S$ is [[Set]] and "cover" means "[[surjection]]" (an example where the covers are the regular epimorphisms), then we recover the original external notion of ([[small category|small]]) anafunctor.  An anafunctor, defined in this way, is saturated just when the map $core(F) \to core(C\times D)$ of [[cores]] is an [[isofibration]], so we need an internal notion of core to define saturated anafunctors internally.  An anafunctor is an anaequivalence when $F\to D$ is fully faithful and a cover on objects; for [[Lie groupoids]], these are the [[Morita equivalences]].

If $C\leftarrow F \to D$ and $C\leftarrow G \to D$ are internal anafunctors, we define an __[[ananatural transformation]]__ between them (or simply a _natural transformation_, given the context) to be a [[natural transformation]] between the two induced internal natural transformations $F\times_C G \to D$.  We can then prove that internal categories, anafunctors, and natural transformations form a [[bicategory]].  (Interestingly, you may need the axiom of choice in the [[metalogic]] to conclude this, depending on whether there is a natural way to choose the necessary pullbacks; else you get an [[anabicategory]], in which the composition functors are anafunctors.)

The role of the assumptions about covers is:

* Identity maps must be covers in order to have identity anafunctors (and more generally, for every functor to give rise to an anafunctor).
* To compose anafunctors by pullback, the pullbacks of covers must exist and be covers, and covers must be closed under composition.
* To define $F \times_C G$ and obtain a notion of natural transformation, we again need covers to have pullbacks.
* To define composition of natural transformations between anafunctors, we need covers to be effective; see diagram (118) in [HGT1](#HGT1).

Note: in Section 1.1.5 of [HGT1](#HGT1), the following additional axiom was assumed on the class of covers:

* every [[congruence]] involving a cover has a quotient object which is a cover.

This is not needed for anafunctors but is used to relate descent to bundles (and then to $2$-bundles).


### Homotopy-theoretic interpretation

Observe that the surjective-on-objects equivalences are precisely the [[model category|acyclic fibrations]] for the [[canonical model structure]] on [[Cat]].  Therefore, anafunctors can be identified with the "one-step generalized morphisms" in $Cat$ whose first leg is not just a [[weak equivalence]] but an acyclic fibration.  However, it appears that the canonical model structure on Cat only exists (with its weak equivalences being the fully faithful and essentially surjective maps) under the assumption of some choice---though full AC is not needed, [[COSHEP]] suffices.

More generally, it is proven in [EKV](#EKV) that if $S$ has a Grothendieck coverage, then under suitable additional conditions on $S$ (and, of course, the axiom of choice assumed external to $S$), there is a [[model category|model structure]] on the category $Cat(S)$ of internal categories in $S$ relative to that coverage.  The internal anafunctors relative to the given coverage, as defined above, can then once again be identified with the spans whose first leg is an acyclic fibration.

Since all objects in the canonical model structure on Cat are fibrant, according to Kenneth Brown's theorem in [[homotopical cohomology theory]] it follows that one-step generalized morphisms already realize the full localization, i.e. they represent all morphisms in the [[homotopy category]] $Ho(Cat)$.

If we specialize to groupoids, with their canonical model structure by Brown-Golasinski, then by the general idea of [[homotopical cohomology theory]]
this means that anafunctors between groupoids represent [[nonabelian cocycle]]s on groupoids with values in groupoids. By the notion of [[descent|codescent]] such homotopical cocycles are related to [[descent|descent data]] that enters the definition of [[sheaf|sheaves]] and [[stack]]s.


## Questions of size {#SizeQuestions}

In general, it seems that even if $C$ and $D$ are [[small categories]], then the category $Ana(C,D)$ of anafunctors from $C$ to $D$ is not necessarily even essentially small, and thus the 2-category $Cat_{ana}$ of categories and anafunctors is not [[cartesian closed category|cartesian closed]].

This is true, however, under the assumption of COSHEP, since in that case (as above) anafunctors represent maps in $Ho(Cat)$, which is locally small by general model category theory.  More specifically, under COSHEP every anafunctor $C\leftarrow F \to D$ is equivalent to one where the set of objects of $F$ is $C_0'$, where $C_0'\to C_0$ is a projective cover of the set $C_0$ of objects of $C$.

COSHEP is actually stronger than necessary for this; all that is really needed is [[WISC]], i.e. for any set $X$, the full subcategory of $Set/X$ consisting of surjections has a [[weakly initial set]].  For in that case, any anafunctor $C\leftarrow F \to D$ is equivalent to one where the set of objects of $F$, equipped with its surjection to $C_0$, belongs to the weakly initial set.  Note that COSHEP implies WISC, as do the [[axiom of multiple choice]] and the axiom of [[small violations of choice]].

In Makkai's paper referenced below, he proves that $Ana(C,D)$ is small under the assumption of his [[small cardinality selection axiom]], which also follows from SVC.  It is not obvious, however, what the [[structural set theory|structural]] counterparts of these two axioms might be.  Although they carry the same feel that "choice is violated only in a small way," Makkai's proof from SCSA is an "injective" approach, in that the set of possibilities for the objects of $F$ is constructed mainly from $D$, rather than purely from $C$ as in the "projective" approach above using COSHEP or WISC.


## Generalizations

### Higher versions 

see [[infinity-anafunctor]]

### Additive version

The notion of abelian [[butterfly]] introduced by Behrang Noohi [Weak maps of 2-groups](http://arxiv.org/abs/math.CT/0506313) is the additive version of the notion of (saturated) anafunctor: the equivalence between, on the one hand, internal groupoids and internal functors and, on the other hand, arrows and commutative squares in an abelian category extends to an equivalence between saturated anafunctors and butterflies.

+-- {: .query}

_Urs says:_ Why do you restrict this to the abelian case? From 
[page  16](http://arxiv.org/PS_cache/math/pdf/0506/0506313v3.pdf#page=16)  of Noohi's article I got the impression that he is precisely describing the ana-2-functors between one-object 2-groupoids in terms of the corresponding (possibly nonabelian) crossed modules. 

_Mathieu says:_ I don't see that (or something like that) on that page, but saturated anafunctors should correspond to butterflies also in the semi-abelian case (using the notion of internal crossed module in a semi-abelian category introduced by Janelidze), but I have not checked it.  The special case of groups is probably easy to check: saturated anafunctors between two internal groupoids in the category of groups should correspond to butterflies between the corresponding crossed modules.

_Urs says:_ I haven't checked the details. But he is looking at derived homs of crossed complexes. By general nonsense these derived hom should be given by homs out of cofibrant replacements. This is another way of talking about the anafunctor picture. Somebody should check the details.

[[Tim Porter|Tim]]: Noohi has pointed out to me a slip in his HHA article in which he gives an 'algebraic' description of weak map (and thus of anafunctor) between the crossed modules corresponding to the 2-groups.  He has posted a corrected version on the archive (&lt;http://arxiv.org/abs/math/0506313v3>, but make sure you get version 3).
=--

## References

The term "anafunctor" was intrroduced by Michael Makkai in


* Makkai, [Avoiding the axiom of choice in general category theory](http://www.math.mcgill.ca/makkai/anafun/) 

The popularity of the term was notably pushed by [[Toby Bartels]], who considered [[internalization]]s of Makkai's definition in

* [[Toby Bartels]], _Higher Gauge Theory I: 2-Bundles_  ([arXiv:math.CT/0410328](http://arxiv.org/abs/math.CT/0410328))
{#HGT1}

A development and exposition of the general setup taking Makkai's and Bartels' motivations and the theory of [[homotopical category|homotopical categories]] into account is

* [[David Roberts]], _Internal categories and anafunctors_ (PhD thesis, chapter I) ([pdf](http://ncatlab.org/davidroberts/files/internal_cats_and_anafunctors.pdf))

Since anafunctors are a special case of a more general concept, they, or the general theory applying to them, has been considered under different terms elsewhere. 

The general question of [[model category]] structures on categories of [[internal category|internal categories]] is discussed in 

* T. Everaert, R.W. Kieboom and T. Van der Linden , _Model structures for homotopy of internal categories_  TAC,  Vol. 15, CT2004, No. 3, pp 66-94. ([web](http://www.tac.mta.ca/tac/volumes/15/3/15-03abs.html) ([pdf](http://www.tac.mta.ca/tac/volumes/15/3/15-03.pdf)))
{#EKV}

Closely related, still a bit more general, are the considerations in

* Jardine, _Cocycle categories_ K-theory 0782 ([web](http://www.math.uiuc.edu/K-theory/0782/)) ([pdf](http://www.math.uiuc.edu/K-theory/0782/coc-cat3.pdf))


## Discussion

The following discussion was about the effect of different notions of [[coverage]] on the definition of and operations on anafunctors.

+-- {: .query}

[[David Roberts]] says: If one uses a coverage, then composing anafunctors means a choice has to be made in the filler of $U \to D_0 \leftarrow V$ with the right map a cover. Presumably the resulting bicategory of anafunctors is independent, up to biequivalence, of the choices made. Also, at the very least the identity map has to be a cover, so as to define the identity anafunctor. 

DR says: Well I suppose we could follow Makkai's philosophy twice and have a composition anafunctor (in the original sense) for composing anafunctors (in the internal sense) and end up with an anabicategory.

_Mike_: Yes, presumably it won't depend on the fillers chosen; I haven't checked the details, though.  "Grothendieck coverage" means the same as "Grothendieck topology" and thus includes closure under lots of things, including composition and containing identities.

_David R_: I noticed the adjective Grothendieck in the preceeding sentence half-way through asking the question, but I think my point still holds for general coverages, without the closure properties.

_Mike_: Well, as you pointed out, you need at least identity maps to be covers to have identity anafunctors, and you need covers to be stable under composition, as well as pullback, in order to define composition of anafunctors.  An arbitrary coverage might not satisfy those, although pretty much any coverage arising in practice does.  The other point that a choice has to be made unless you have honest pullback-stability is certainly true.  So probably the most natural-feeling context in which to work is a (possibly singleton) [[Grothendieck pretopology]].  I would be happy for this page to ignore the case where covers don't have pullbacks; I did some rewriting above to reflect this discussion.  I think this discussion could now be deleted; feel free to do so if you agree.

_David R_: After some thought, one could do without _the_ identity anafunctor, and be satisfied with a anafunctor (of the external variety) giving the identity: $1 \to Ana(X,X)$. I think I should move this discussion to a section of its own, and develop these ideas there. As an aside, I think I saw an example of a non-Grothendieck coverage in John and Alex's [[generalized smooth space|smooth spaces]] paper.

_Toby_: You only get an anabicategory anyway, because of the choice of pullbacks (unless the structure of the coverage fixes these, as can be done in $Set$).

Anafunctors really should make sense in any [[site]] whatsoever (as long as we can compose ananatural transformations, which I guess we can if the site is subcanonical).  The trick of getting away with single maps (as one can do, for example, in a superextensive site) is not really necessary.  In fact, using a coverage makes the definitions, while more complicated, really look more natural in topological categories.

=--


[[!redirects anafunctors]]
