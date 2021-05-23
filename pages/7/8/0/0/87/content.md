
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Anafunctors
* automatic table of contents goes here
{:toc}

## Idea

An _anafunctor_ $F\colon C \to D$ is a generalized [[functor]].

A basic fact in ordinary [[category theory]] is that a [[functor]] $f\colon C \to D$ is an [[equivalence of categories]] -- in that there is a functor $g\colon D \to C$ and natural isomorphisms $f \circ g \simeq Id_D$ and $g \circ f \simeq Id_C$ -- if and only if it is a [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|fully faithful]].  However, the "if" part of this statement depends crucially on the [[axiom of choice]]: the functor $g$ is obtained by _choosing_  for each [[object]] $d \in D$ an object $c \in C$ such that $f(c) \simeq d$.  In fact, the statement that "every fully faithful and essentially surjective functor is an equivalence of categories" is equivalent to the axiom of choice.

The notion of *anafunctor* is a generalization of the usual notion of *functor*, which enables us to recover a version of this statement without the axiom of choice.  It was first studied in detail ([Makkai](#Makkai)) with [[foundations|foundational concerns]] in mind, although it also appears unnamed in ([Kelly](#Kelly)). Later, they were applied by [[Toby Bartels]] to [[internal category|internal categories]], where the axiom of choice is simply not an option.  These "internal anafunctors" actually turned out to be known already (at least up to equivalence) in some contexts, in particular as [[Hilsum-Skandalis morphism]]s between [[Lie groupoid]]s.

We present three motivations and applications of anafunctors: 

* [Anafunctors as a tool for handling foundational issues](#FoundationalMotivation)

* [Anafunctors as morphisms in internal categories](#InternalCatMotivation)

* [Anafunctors as morphisms in a homotopy category](#HomotopicalMotivation)


### Foundational motivation {#FoundationalMotivation}

There is a sense in which the construction of inverse equivalences is not a "real" use of the axiom of choice, because the choice of $d$ is determined up to unique isomorphism.  Note that in ordinary set theory, the axiom of choice is not necessary to make choices that are uniquely defined; this is sometimes called the "axiom of non-choice" or the "function comprehension principle."  Since in category theory, an object can only be expected to be determined up to unique isomorphism, it is natural to regard the above statement as really being a "functor comprehension principle" or an "axiom of non-choice for categories."  The fact that the full axiom of choice is required to make such choices is then an artifact of the usual [[foundation]]al choice to define categories as having a [[set]] of objects.

In fact, however, we can recover the functor comprehension principle while maintaining the definition of categories in set theory if we modify the notion of *functor*.  This results in the notion of _anafunctor_, which is essentially "a functor which determines its values on objects only up to isomorphism."  In particular, an anafunctor is an [[equivalence of categories]] (in the sense of having an inverse *anafunctor*) precisely if it is essentially surjective and full and faithful.  From this point of view, an anafunctor is not necessarily a fundamental notion, but rather an artifact that makes it possible to approximate the "natural" theory of categories, which doesn't need choice but has a functor comprehension principle, while still working in a set-theoretic foundation lacking choice.
   
Every functor may be interpreted as an anafunctor; that every anafunctor is equivalent to a functor is equivalent to the [[axiom of choice]], in which case the inclusion of functors into anafunctors is in fact an [[equivalence of categories]]. But if you ignore functors and deal only with anafunctors (or saturated anafunctors), then the theory becomes entirely [[constructive mathematics|constructive]] (without using the axiom of choice or even [[excluded middle]]).  Thus, anafunctors (or even saturated anafunctors) are the correct notion to use if you are doing [[constructive mathematics]] and you still want to [[foundations|found]] mathematics on some sort of [[set theory]].

  
### Motivation from internal categories {#InternalCatMotivation}

Since questions concerning the axiom of choice tend to look a bit esoteric to those not actively interested in questions of [[foundations]], it is helpful (and useful!) to think of this more generally in terms of [[internal category]] theory, where the concept is of independent use, and in fact well known by other names than "anafunctor".

Consider some ambient category $\mathcal{E}$ [[internalization|internal]] to which we want to do category theory. A good example to keep in mind is the category [[Top]] of [[topological space]]s.  We observe that "the axiom of choice fails in [[Top]]", but that this is a very non-esoteric and obvious statement: it just means that not every continuous [[epimorphism]] $P \to X$ between topological spaces has a _continuous_ [[section]].

Then it may easily happen that an internal functor $f\colon C \to D$ between [[internal category|internal categories]] in $\mathcal{E}$ (for instance between topological categories) is fully faithful, in the "internal" sense that
$$\array{C_1 & \overset{}{\to} & D_1\\
  \downarrow && \downarrow\\
  C_0 \times C_0 & \underset{}{\to} & D_0\times D_0}$$
is a [[pullback]], and essentially surjective, in the "internal" sense that $C_0 \times_{D_0} Iso(D) \to D_0$ is surjective (or even a quotient map, i.e. a [[regular epimorphism]]), but for which there still does not exist a weak inverse in $Cat(\mathcal{E})$.

For example, let $X$ be a topological space and consider the functor $C(U) \to X$, where $X$ is regarded as an internal category in $Top$ which is [[discrete category|discrete]] in the categorical sense, and $C(U)$ is the [[Cech nerve|Cech groupoid]] associated to an open [[cover]] $X = \bigcup_i U_i$ of $X$.  That means that the space of objects of $C(U)$ is $\coprod_i U_i$, and its space of morphisms is $\coprod_{i,j} (U_i\cap U_j)$.  Then the functor $C(U)\to X$ is fully faithful (essentially by definition of the morphisms in $C(U)$) and essentially surjective (since the $U_i$ are a cover of $X$) in the senses above.  However, in general it does not admit a weak inverse, since the continuous function $\coprod_i U_i \to X$ does not have a continuous section if $X$ is connected unless one of the $U_i$ is already equal to $X$.

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

where the left leg is a weak equivalence, hence for us: where the left leg is an internal functor that is $k$-surjective for all $k$.  (This is the beginning of the construction of the [[Dwyer-Kan localization]] at our chosen weak equivalences.)

For the case $\mathcal{E} = Top$ such a span is a morphism out of a _Cech cover_ . For instance for $C = X$ a topological space regarded as a topological category, for $G$ a [[topological group]] and $D = \mathbf{B}G$ its [[delooping]] one-object topological groupoid, such a span is a [[Cech cohomology|Cech cocycle]] on $X$ with values in $G$.

And finally: for the case that $\mathcal{E} = Set_{\not C}$ is the category of sets without the axiom of choice, such a span is an **anafunctor**: a functor $\hat C \to C$ that is surjective on objects and [[full and faithful functor|full and faithful]], together with a functor $\hat C \to D$ out of the "resolution" of $C$.

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

### Explicit set-theoretic definition {#SetDef}

In more explicit detail, an __anafunctor__ $F\colon C \to D$ consists of:

* a set ${|F|}$ of __specifications__ of $F$ (which corresponds to the set of objects of $\overline{F}$);
* maps $\sigma\colon {|F|} \to C$ and $\tau\colon {|F|} \to D$ (taking values in objects). Given $x\colon C$ and $y\colon D$, we say that $y$ is a __specified value__ of $F$ at $x$ if, for some $s\colon {|F|}$, $x = \sigma(s)$ and $y = \tau(s)$; in this case, $s$ __specifies__ $y$ as a value of $F$ at $x$, and we write $F_s(x) = y$.  That is,
  $$ F_s(x) \coloneqq \tau(s) .$$
  We say that $y$ is a __value__ of $F$ at $x$ if $y$ is isomorphic (in $D$) to some specified value of $F$ at $x$; we write $F(x) \cong y$. (There is no notion of *the* value of $F$ at $x$, except in the up-to-isomorphism sense of the [[generalised the]], and $F(x) = y$ is a meaningless statement.);
* for each $s, t\colon {|F|}$ and morphism $f\colon \sigma(s) \to \sigma(t)$ in $C$, a morphism
  $$ F_{s,t}(f)\colon F_s(x) \to F_t(y) $$
  in $D$, where $x \coloneqq \sigma(s)$ and $y \coloneqq \sigma(t)$. Similarly to the above, we can define whether a given morphism $g$ in $D$ is a __specified value__ of $F$ at a given morphism $f$ in $C$ or whether $g$ is (merely) a __value__ of $F$ at $f$. (Again, there is no notion of *the* value of $F$ at $f$.);
* $\sigma$ is a [[surjective function]]. Thus, $F$ has *some* value at any given object or morphism of $C$. (In the [[internalization|internalized]] case, this requirement can become quite complicated; for example, internal to [[Diff]], one requires a [[surjective submersion]].);
* $F$ preserves [[identity morphism|identities]]. That is, given $s\colon {|F|}$, the value of $F$ specified by $s$ and $s$ at the identity of $\sigma(s)$ is the identity of $\tau(s)$, or (in symbols) $F_{s,s}(\id_{\sigma(s)}) = \id_{\tau(s)}$, or (whenever this makes sense)
  $$ F_{s,s}(\id_x) = \id_{F_s(x)} ;$$
* $F$ preserves [[composition]]. That is, given $s, t, u\colon {|F|}$, $f\colon \sigma(s) \to \sigma(t)$, and $g\colon \sigma(t) \to \sigma(u)$,
  $$ F_{s,u}(f;g) = F_{s,t}(f);F_{t,u}(g) .$$
  (Here the semicolon indicates composition in the anti-Leibniz order.).

From the above explicit data, the category $\overline{F}$ is constructed as follows: the objects of $\overline{F}$ are the elements of ${|F|}$, while a morphism $s \to t$ in $\overline{F}$ is simply a morphism $\sigma(s) \to \sigma(t)$ in $C$.  Then $\sigma$ extends to a surjective faithful functor from $\overline{F}$ to $C$ (acting as the identity on morphisms), and $\tau$ extends to a functor from $\overline{F}$ to $D$ (mapping the morphism $f\colon s \to t$ in $\overline{F}$ to $F_{s,t}(f)\colon \tau(s) \to \tau(t)$ in $D$).

An anafunctor $F$ is __saturated__ if, whenever $F(x) \cong y$, $F_s(x) = y$ for some unique specification $s$, where the unicity of $s$ depends not only on $x$ and $y$ but also on how $y$ is a value of $F$ at $x$. To be precise: if $g\colon y' \to y$ is an isomorphism in $D$ and $F_{s'}(x) = y'$ for some specification $s'$, then there is a unique specification $s$ such that $F_{s',s}(\id_x) = g$ (where in particular, $\sigma(s) = x$ and $F_s(x) = y$). Every anafunctor $F\colon C \to D$ has a _saturation_ $\overline{F}$; $\overline{F}$ is a saturated anafunctor and $F \cong \overline{F}$ in the category of anafunctors from $C$ to $D$. In fact, the inclusion of the saturated anafunctors into the anafunctors (as a full subcategory) is an equivalence of categories (given fixed $C$ and $D$).

The usual notions of [[full functors]] and [[faithful functors]] can be generalized to anafunctors. An anafunctor $F$ is __full__ if the maps $F_{s, t}: Hom(\sigma(s), \sigma(t)) \to Hom(\tau(s), \tau(t))$ are all surjective, and it is __faithful__ if the maps are injective.

Anafunctors can be composed via pullback. Given anafunctors $F: C \to D$, $G: D \to E$, we can form the pullback
$$
\array{
  |GF|                & \to                 & |G|        & \overset{\tau_G}\to E\\
  \downarrow          &                     & \downarrow\mathrlap{\sigma_G}\\
  |F|                 & \underset{\tau_F}\to & D\\
  \mathllap{\sigma_F}\downarrow\\
  C
}
$$
More explicitly, the specifications are given by pairs $(s, t) \in |F| \times |G|$ such that $\tau_F(s) = \sigma_G(t)$, and $\sigma_{G F}(s, t) = \sigma_F(s)$, $\tau_{G F}(s, t) = \tau_G(t)$. For $(s, t), (s', t') \in |GF|$ and an arrow $f: \sigma_F(s) \to \sigma_F(s')$, we obtain an arrow $F_{s, s'}(f): \tau(s) \to \tau(s')$. This is also an arrow $\sigma_G(t) \to \sigma_G(t')$, so we can lift this map to $G_{t, t'}F_{s, s'}(f): \tau(t) \to \tau(t')$, and this completes the description of the anafunctor. The other axioms can be verified straightforwardly.

Categories, anafunctors, and a suitably defined notion of [[ananatural transformation]] between them form a [[bicategory]] $Cat_{ana}$; an internal [[equivalence]] in this 2-category is called an **anaequivalence**.  Every functor may be interpreted as an anafunctor, with ${|F|}$ always taken to be (the set of objects in) $C$ itself and $\sigma$ the [[identity functor]].  Indeed, there is a [[2-functor]] to $Cat_{ana}$ from the [[strict 2-category]] $Str Cat$ of categories, functors and natural transformations; this functor is an [[equivalence of categories|equivalence]] if and only if the [[axiom of choice]] holds.  Thus, most mathematicians will identify $Cat_{ana}$ and $Str Cat$ as simply [[Cat]], the $2$-category of categories; however, mathematicians who doubt the axiom of choice will distinguish them.  While anafunctors exist in any case, there is an ideological statement that may be implied by their use: that $Cat$ is *really* $Cat_{ana}$ rather than $Str Cat$.

In any case, (modulo "size issues" which one may want to impose) the inclusion of $Str Cat$ into $Cat_{ana}$ has a right adjoint, described using [[clique]]s. Accordingly, we can instead define anafunctors by means of clique categories, taking an anafunctor from $C$ into $D$ to be a genuine functor from $C$ into $Clique(D)$ (and the 2-category of anafunctors as the [[Kleisli category]] for the $Clique(-)$ 2-monad (in particular, natural transformations between anafunctors into $D$ are simply natural transformations of the corresponding genuine functors into $Clique(D)$)).

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

By the remarks above, if $S$ is [[Set]] and "cover" means "[[surjection]]" (an example where the covers are the regular epimorphisms), then we recover the original external notion of ([[small category|small]]) anafunctor.  An anafunctor, defined in this way, is saturated just when the map $core(F) \to core(C\times D)$ of [[cores]] is an [[isofibration]], so we need an internal notion of core to define saturated anafunctors internally.  An anafunctor is an anaequivalence when $F\to D$ is fully faithful and [[essentially surjective functor|essentially surjective]], meaning the canonical map $F_0\times_{C_0}C_1 \to C_0$ has splits over a cover of $C_0$. For [[Lie groupoids]], these are the [[Morita equivalences]].

If $C\leftarrow F \to D$ and $C\leftarrow G \to D$ are internal anafunctors, we define an __[[ananatural transformation]]__ between them (or simply a _natural transformation_, given the context) to be a [[natural transformation]] between the two induced internal functors $F\times_C G \to D$.  We can then prove that internal categories, anafunctors, and natural transformations form a [[bicategory]].  (Interestingly, you may need the axiom of choice in the [[metalogic]] to conclude this, depending on whether there is a natural way to choose the necessary pullbacks; else you get an [[anabicategory]], in which the composition functors are anafunctors.)

The role of the assumptions about covers is:

* Identity maps must be covers in order to have identity anafunctors (and more generally, for every functor to give rise to an anafunctor).
* To compose anafunctors by pullback, the pullbacks of covers must exist and be covers, and covers must be closed under composition.
* To define $F \times_C G$ and obtain a notion of natural transformation, we again need covers to have pullbacks.
* To define composition of natural transformations between anafunctors, we need covers to be effective; see diagram (118) in [HGT1](#HGT1).

Note: in Section 1.1.5 of [HGT1](#HGT1), the following additional axiom was assumed on the class of covers:

* every [[congruence]] involving a cover has a quotient object which is a cover.


This is not needed for anafunctors but is used to relate descent to bundles (and then to $2$-bundles).

### As an operation on 2-categories

_This section is work in progress by [[David Roberts|me]]_

While internal anafunctors seem to require a lot of baggage, they can be defined very elegantly by working with the 2-category $Cat(S)$ (or some sub-2-category thereof) as a 2-category. One first makes the observation:

* functors internal to $S$ which are fully faithful and whose object component belongs to a singleton Grothendieck pretopology themselves form a (strict) singleton pretopology on $Cat(S)$. Thus one can consider anafunctors as spans in a 2-category where the source leg belongs to a strict, subcanonical singleton Grothendieck pretopology, all of whose covers are [[ff morphism|ff]].

### Homotopy-theoretic interpretation

Observe that the surjective-on-objects equivalences are precisely the [[model category|acyclic fibrations]] for the [[canonical model structure]] on [[Cat]].  Therefore, anafunctors can be identified with the "one-step generalized morphisms" in $Cat$ whose first leg is not just a [[weak equivalence]] but an acyclic fibration.  However, it appears that the canonical model structure on Cat only exists (with its weak equivalences being the fully faithful and essentially surjective maps) under the assumption of some choice---though full AC is not needed, [[COSHEP]] suffices.

More generally, it is proven in [EKV](#EKV) that if $S$ has a Grothendieck coverage, then under suitable additional conditions on $S$ (and, of course, the axiom of choice assumed external to $S$), there is a [[model category|model structure]] on the category $Cat(S)$ of internal categories in $S$ relative to that coverage.  The internal anafunctors relative to the given coverage, as defined above, can then once again be identified with the spans whose first leg is an acyclic fibration.

Since all objects in the canonical model structure on Cat are fibrant, according to Kenneth Brown's theorem in [[homotopical cohomology theory]] it follows that one-step generalized morphisms already realize the full localization, i.e. they represent all morphisms in the [[homotopy category]] $Ho(Cat)$.

If we specialize to groupoids, with their canonical model structure by [[Ronnie Brown|Brown]]--[[Marek Golasiński|Golasiński]], then by the general idea of [[homotopical cohomology theory]]
this means that anafunctors between groupoids represent [[nonabelian cocycle]]s on groupoids with values in groupoids. By the notion of [[descent|codescent]] such homotopical cocycles are related to [[descent|descent data]] that enters the definition of [[sheaf|sheaves]] and [[stack]]s.


## Examples

We will use the [explicit set-theoretic definition](/nlab/show/anafunctor#SetDef) in this section.

### Product anafunctor
Given a category $C$ with [[cartesian product|binary products]], we can form a product functor $P: C \times C \to C$ that sends a pair of objects $(A, B)$ to a product of them. This requires picking a product for each pair, and hence requires the [[axiom of choice]].

However, we can form the product anafunctor without using choice. The specifications are given by $|P| = \text{product diagrams in }\;C$, and the maps $\sigma: |P| \to C \times C$ and $\tau: |P| \to C$ are given by
$$
  \sigma(A \leftarrow D \rightarrow B) = (A, B),\;\; \tau(A \leftarrow D \rightarrow B) = D.
$$
Given product diagrams $A \leftarrow D \rightarrow B$ and $A' \leftarrow D' \rightarrow B'$, and a map $(f, g): (A, B) \to (A', C')$ in $C \times C$, we obtain $P(f, g): D \to D'$ by the universal property of the product. The compatibility conditions are easy to check.

### Anafunctor from functor
Suppose we have a usual functor $F: C \to D$. Then we can obtain an anafunctor as the span
$$
\array{
  C & \overset{F}\to & D\\
  \mathllap{id_C} \downarrow \\
  C
}
$$
The composition of anafunctors agree with the composition of functors.

### Inverses of anafunctors
Given an anafunctor $F: C \to D$ with $\sigma: |F| \to C$ and $\tau: |F| \to D$, if $F$ (ie. $\tau$) is essentially surjective, then its saturation is strictly surjective.

Then given a saturated full and faithfull essentially surjective anafunctor, we can obtain an inverse anafunctor $F^{-1}: D \to C$ by swapping $\tau$ and $\sigma$ around. The conditions of being full and faithful and essentially surjective guarantees the axioms are still satisfied.

## Questions of size {#SizeQuestions}

Even if $C$ and $D$ are [[small categories]], then the category $Ana(C,D)$ of anafunctors from $C$ to $D$ is not necessarily even essentially small, and thus the 2-category $Cat_{ana}$ of categories and anafunctors is not [[cartesian closed category|cartesian closed]].  Some models in which this fails to be true are sketched in [this MO discussion](#HenryMO).

This is true, however, under the assumption of [[COSHEP]], since in that case (as above) anafunctors represent maps in $Ho(Cat)$, which is locally small by general model category theory.  More specifically, under COSHEP every anafunctor $C\leftarrow F \to D$ is equivalent to one where the set of objects of $F$ is $C_0'$, where $C_0'\to C_0$ is a projective cover of the set $C_0$ of objects of $C$.

COSHEP is actually stronger than necessary for this; all that is really needed is [[WISC]], i.e. for any set $X$, the full subcategory of $Set/X$ consisting of surjections has a [[weakly initial set]].  For in that case, any anafunctor $C\leftarrow F \to D$ is equivalent to one where the set of objects of $F$, equipped with its surjection to $C_0$, belongs to the weakly initial set.  Note that COSHEP implies WISC, as do the [[axiom of multiple choice]] and the axiom of [[small violations of choice]] (SVC).

In [Makkai's paper](#Makkai), he proves that $Ana(C,D)$ is essentially small under the assumption of his [[small cardinality selection axiom]] (SCSA), which also follows from SVC.  Although SCSA and WISC carry the same feel that "choice is violated only in a small way," Makkai's proof from SCSA is an "injective" approach, in that the set of possibilities for the objects of $F$ is constructed mainly from $D$, rather than purely from $C$ as in the "projective" approach above using COSHEP or WISC.

Another axiom ensuring that $Ana(C,D)$ is essentially small is the [[axiom of stack completions]] (ASC), since if $D\to \hat{D}$ is an intrinsic stack completion we have $Ana(C,D) \simeq Fun(C,\hat{D})$.

In particular, the bicategory of categories and anafunctors is locally essentially small and cartesian closed in the internal logic of any [[Grothendieck topos]], because the latter satisfies WISC, SCSA, and ASC.


##Anafunctors in homotopy type theory

Anafunctors are unnecessary when using "saturated/univalent" categories in [[homotopy type theory]] (see Def. 9.1.3 of [[the HoTT book]], and Chap. 9 notes), because of their [functor comprehension principle](https://ncatlab.org/michaelshulman/show/functor+comprehension+principle). An anafunctor is a span whose first leg is a surjective and fully faithful functor, but for saturated categories any such functor is an equivalence (in the strong sense of having an inverse), so any anafunctor is equivalent to a functor.


## Related concepts

### Anafunctors versus representable profunctors

A different way of describing "a functor whose values are determined only up to isomorphism" is with a representable [[profunctor]] (a.k.a. distributor).  A profunctor $A &#8696; B$ is a functor $F\colon A \to [B^{op},Set]$, and we call it *representable* if each [[presheaf]] $F(a)$ is [[representable functor|representable]].

In the presence of [[axiom of choice|AC]], one can then choose a representing object $F_a\in B$ for each $a$ and thereby define a functor $A\to B$, but without choice this is generally not possible.  However, one can define an anafunctor from $A$ to $B$, whose specifications at $a$ are "representations" of $F(a)$.

Conversely, given an anafunctor represented by a span $A \xleftarrow{g} P \xrightarrow{f} B$, one can define a profunctor $A &#8696; B$ as the composite $f_* \circ g^*$, where $f_*(p)(b) = B(b,f(p))$ and $g_*(a)(p) = A(g(p),a)$, and this profunctor will be representable.  This defines a bijective-on-objects [[equivalence of 2-categories]] between $Cat_{ana}$ and $Prof_{rep}$, the [[locally full sub-2-category]] of [[Prof]] determined by the representable profunctors.  (This appears to have been written down first [here](http://permalink.gmane.org/gmane.science.mathematics.categories/6485) by [[Jean Benabou]]).

Anafunctors and representable profunctors each have advantages.  For purposes which require only the 2-category $Cat_{ana}\simeq Prof_{rep}$, either one is of course sufficient.  For instance, a non-[[cleavage|cloven]] [[Grothendieck fibration]] can equally well be turned into a [[pseudofunctor]] valued in $Cat_{ana}$ or in $Prof_{rep}$.  However, in this case $Prof_{rep}$ is arguably more natural, since an arbitrary functor (not necessarily a fibration) $A \to B$ can be turned into a normal [[lax 2-functor]] $B^{op}\to Prof$, which is a pseudofunctor landing in $Prof_{rep}$ exactly when the given functor was a fibration.  (It is a pseudofunctor landing in $Prof_{corep}$ iff the functor was an opfibration, and it is a pseudofunctor iff the functor was [[exponentiable functor|exponentiable]].)  More generally, one good point about using representable profunctors is that they fit in immediately with the general notion of profunctor.

On the other hand, sometimes it requires a little contortion to put something in the form of a representable distributor.  For instance, if $A$ has binary [[products]], then there is obviously a product-assigning representable distributor $P\colon A \times A  &#8696; A$ defined by $P(a_1,a_2)(a) = Hom_A(a,a_1) \times Hom_A(a,a_2)$.  But if A has binary [[coproducts]], then in order to define a coproduct-assigning representable distributor $C\colon  A \times A  &#8696; A$, one needs to say something like

* $C(a_1,a_2)(a)=$ the set of triples $(a_3,p_1,p_2,f)$ where $p_i\colon a_i \to a_3$ are the injections into a coproduct and $f$ is a morphism $a \to a_3$, modulo an equivalence relation $(a_3,p_1,p_2,f) \sim (a_3',p_1',p_2',f')$ if there exists a (necessarily unique iso)morphism $g\colon a_3 \to a_3'$ commuting with all the structure maps.

(This is essentially making explicit the functor $Cat_{ana} \to Prof_{rep}$ defined above.)  Of course, $C$ is more easily defined as a *[[corepresentable functor|corepresentable]]* distributor.  But if we want to define a functor that involves both limits and colimits, like $(a,b,c) \mapsto a \times (b + c)$, then it is not "naturally" represented as either a representable or a corepresentable profunctor.  However, with anafunctors, all of these functors can be represented "naturally" in analogous ways.  In the first case, we consider the span $A\times A \leftarrow P \to A$, where $P$ is the category of binary product diagrams in $A$.  In the second case, we consider the span $A\times A \leftarrow C \to A$, where $C$ is the category of binary coproduct diagrams.  And in the third case, we consider the span $A\times A\times A \leftarrow D \to A$, where $D$ is the category of binary coproduct diagrams together with a product diagram one of whose factors is the vertex of the coproduct diagram.

Roughly speaking, anafunctors are formulated exactly in order to describe "functors defined up to isomorphism," while representable distributors describe "functors valued in representable presheaves."  "Objects defined up to isomorphism" and "representable presheaves" are *formally* equivalent (without invoking AC), but not every "naturally occurring" object-defined-up-to-isomorphism is "given in nature" by the presheaf it represents.  Some are given by the [[copresheaf]] they corepresent; others aren't given directly in either of those ways.  One can also think of an anafunctor as a particularly convenient "presentation" of a representable distributor.

A further reason that the notion of anafunctor is useful is that when working with [[internal categories]], the quotienting operations necessary to define the composite of internal profunctors may not exist, whereas internal anafunctors can always be composed.  Thus, when working with (for instance) [[smooth manifold|smooth]] categories or groupoids, profunctors are not so much an option, but anafunctors are well-behaved (see the papers by Bartels and Roberts referenced below).


## Generalizations

### Higher versions 

see [[infinity-anafunctor]]

### Lower version

see [[anafunction]]

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

The term "anafunctor" was introduced by Michael Makkai in

* {#Makkai} [[Michael Makkai]], _Avoiding the axiom of choice in general category theory_, Journal of Pure and Applied Algebra **108** isse 2 (1996) pp 109-173, doi:[10.1016/0022-4049(95)00029-1](https://doi.org/10.1016/0022-4049%2895%2900029-1), ([author's page](http://www.math.mcgill.ca/makkai/anafun/)) 

motivated in part to complete the analogy prophase:anaphase::profunctor:??.

The concept also appears, unnamed, in the article

[[Max Kelly]], _Complete functors in homology I_ (1963) 
{#Kelly}

on [[homological algebra]].  

The popularity of the term was notably pushed by [[Toby Bartels]], who considered [[internalization]]s of Makkai's definition in

* [[Toby Bartels]], _Higher Gauge Theory I: 2-Bundles_  ([arXiv:math.CT/0410328](http://arxiv.org/abs/math.CT/0410328))
{#HGT1}

A development and exposition of the general setup taking Makkai's and Bartels' motivations and the theory of [[homotopical category|homotopical categories]] into account is

* {#Roberts12} [[David Roberts]], _Internal categories, anafunctors and localisations_, [[Theory and Applications of Categories]], Vol. 26, 2012, No. 29, pp 788-829, [journal version](http://www.tac.mta.ca/tac/volumes/26/29/26-29abs.html), [arXiv:1101.2363](http://arxiv.org/abs/1101.2363)

and a purely formal construction using 2-categories appears in the notes

* {#Roberts18} [[David Roberts]], _The construction of formal anafunctors_ (2018) arXiv:[1808.04552](https://arxiv.org/abs/1808.04552), doi:[10.25909/5b6cfd1a73e55](https://doi.org/10.25909/5b6cfd1a73e55)

See also

* [[Erik Palmgren]], _Locally cartesian closed categories without chosen constructions_, [TAC](http://www.tac.mta.ca/tac/volumes/20/1/20-01abs.html).

Since anafunctors are a special case of a more general concept, they, or the general theory applying to them, has been considered under different terms elsewhere. 

The general question of [[model category]] structures on categories of [[internal category|internal categories]] is discussed in 

* T. Everaert, R.W. Kieboom and T. Van der Linden , _Model structures for homotopy of internal categories_  TAC,  Vol. 15, CT2004, No. 3, pp 66-94. ([web](http://www.tac.mta.ca/tac/volumes/15/3/15-03abs.html) ([pdf](http://www.tac.mta.ca/tac/volumes/15/3/15-03.pdf)))
{#EKV}

Closely related, still a bit more general, are the considerations in

* Jardine, _Cocycle categories_ K-theory 0782 ([web](http://www.math.uiuc.edu/K-theory/0782/)) ([pdf](http://www.math.uiuc.edu/K-theory/0782/coc-cat3.pdf))

Some models of set theory in which the bicategory of anafunctors fails to be small are sketched in the answers to

* {#HenryMO} Simon Henry, _Non smallness of the set of anafunctors without AC?_, URL (version: 2017-03-16): <https://mathoverflow.net/q/264585>


[[!redirects anafunctor]]
[[!redirects anafunctors]]
