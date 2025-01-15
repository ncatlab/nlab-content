
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

By *cohesive homotopy type theory* one will mean a [[modal type theory|modal]] [[homotopy type theory]] implementing [[cohesive homotopy theory]] via an [[adjoint triple]] of [[modal operators]]  ([[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]]), hence with [[relation between category theory and type theory|categorical semantics]] in [[cohesive (infinity,1)-topos|cohesive $\infty$-toposes]].

A first formulation of cohesive homotopy type theory &lbrack;[Schreiber & Shulman (2012)](#SchreiberShulman2012)&rbrack; added the required [[adjoint triple]] of [[modal operators]] as [[axioms]] to plain [[homotopy type theory]]. 

Another  approach &lbrack;[Shulman (2015)](#Shulman15)&rbrack; is to change the underlying rules of [[dependent type theory]] itself by adjoining [[syntax]] for [[flat modality|flat]]-[[modal type|modal]] [[contexts]] ("crisp contexts").

This second approach, via a modified type theory with crisp contexts (which has meanwhile be implemented in actual [[proof assistants]] such as *[[Agda-flat]]*), better lends itself to producing [[proofs]] internal to the theory and is what most authors now mean by (real-)cohesive homotopy type theory, see e.g. developments in: [Myers (2019)](#Myers19), [Myers (2021)](#Myers21), [Myers & Riley (2023)](#MyersRiley23).

In any case, *Cohesive homotopy type theory* is an [[axiom|axiomatic]] [[theory]] of the [[higher geometry]] of [[cohesive homotopy theory]], i.e. of the [[homotopy theory]] of [[differential topology]]:

In its [[categorical semantics]], the  [[types]] in cohesive HoTT are interpreted as _[[cohesive topos|cohesive]] [[homotopy types]]_, hence as [[cohesive ∞-groupoids]], such as for instance [[smooth ∞-groupoids]]. See also at _[[motivation for cohesive toposes]]_ for a non-technical discussion.

## The Axioms
  {#TheAxioms}

We discuss the formulation in [[homotopy type theory]] of the [internal axioms](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InternalDefinition) on a [[cohesive (∞,1)-topos]].

Cohesive homotopy type theory is a [[modal type theory]] which adds to [[homotopy type theory]] an [[adjoint triple]] of [[modalities]]

$$
  &#643; \dashv \flat \dashv \sharp
$$

called 

* [[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]],

where $&#643;$ and $\sharp$ are [[idempotent monad|idempotent]] [[monads (in computer science)|monads]] and where $\flat$ is an idempotent [[comonad]], subject to some compatibility condition.

### A) Codiscrete objects

**Axiom A.** _The ambient [[homotopy type theory]] has a 
[[geometric embedding|left-exact]] [[reflective sub-(∞,1)-category]],
to be called the [[base (∞,1)-topos]] "of [[codiscrete objects]]"._

Coq code at [Codiscrete.v](https://github.com/mikeshulman/HoTT/blob/master/Coq/Subcategories/Codiscrete.v)



We write

$$
  X \to \sharp X
$$

for the [[reflector]] into codiscrete objects. 

The homotopy type theory of the [[codiscrete objects]] we call the _external_ theory.


### B) Discrete objects

**Axiom B.** There is also a [[coreflective sub-(∞,1)-category]] of
_[[discrete objects]]_ such that with the codiscrete reflection
it makes the ambient theory that of a [[local (∞,1)-topos]].

[[Coq]] code at [LocalTopos.v](https://github.com/mikeshulman/HoTT/blob/master/Coq/Subcategories/LocalTopos.v).

The coreflector from discrete objects we write

$$
  \flat A \to A
  \,.
$$

### C) Cohesion

**Axiom C** The discrete objects are also reflective, the reflector is [[left adjoint]] to the coreflector and preserves [[product types]].

[[Coq]] code at [CohesiveTopos.v](https://github.com/mikeshulman/HoTT/blob/master/Coq/Subcategories/CohesiveTopos.v).

We write 

$$
  X \to \Pi X
$$

for the reflector into [[discrete objects]].

## As a multimodal type theory

There is another way to define cohesive homotopy type theory, as a [[multimodal type theory]]. Multimodal type theories were first introduced in [Gratzer, Kavvos, Nuyts, & Birkedal 2021](#GKNB21) and consists of a [[strict 2-category]] $\mathcal{M}$ called the *mode theory*, whose objects are called *modes* and whose 1-cells are called *modalities*. For each mode $m \in \mathcal{M}$, there is a type theory at mode $m$, and for each 1-cell between objects there is a type theoretic [[modality]] in the type theory, which comes with its associated [[context lock]]. 

### The mode theory of cohesion

The mode theory $\mathcal{M}$ of cohesive homotopy type theory consists of 

* two modes, the crisp or discrete mode $\mathcal{d} \in \mathcal{M}$ and the cohesive mode $\mathcal{c} \in \mathcal{M}$, 

* 1-cells $p_!, p_*:\mathcal{c} \to \mathcal{d}$ and $p^*, p^!:\mathcal{d} \to \mathcal{c}$, 

* 2-cells 

  * $\eta_{p_! \dashv p^*}: \mathrm{id}_\mathcal{c} \Rightarrow p^* \circ p_!$

  * $\epsilon_{p_! \dashv p^*}: p_! \circ p^* \Rightarrow \mathrm{id}_\mathcal{d}$

  * $\eta_{p^* \dashv p_*}: \mathrm{id}_\mathcal{d} \Rightarrow p_* \circ p^*$

  * $\epsilon_{p^* \dashv p_*}: p^* \circ p_* \Rightarrow \mathrm{id}_\mathcal{c}$

  * $\eta_{p_* \dashv p^!}: \mathrm{id}_\mathcal{c} \Rightarrow p^! \circ p_*$

  * $\epsilon_{p_* \dashv p^!}: p_* \circ p^! \Rightarrow \mathrm{id}_\mathcal{d}$

* which satisfy the following [[triangle identities]]:

  * $p^* \epsilon_{p_! \dashv p^*} \cdot \eta_{p_! \dashv p^*} p^* = \mathrm{id}_{p^*}$

  * $\epsilon_{p_! \dashv p^*} p_! \cdot p_! \eta_{p_! \dashv p^*} = \mathrm{id}_{p_!}$

  * $p_* \epsilon_{p^* \dashv p_*} \cdot \eta_{p^* \dashv p_*} p_* = \mathrm{id}_{p_*}$

  * $\epsilon_{p^* \dashv p_*} p^* \cdot p^* \eta_{p^* \dashv p_*} = \mathrm{id}_{p^*}$

  * $p^! \epsilon_{p_* \dashv p^!} \cdot \eta_{p_* \dashv p^!} p^! = \mathrm{id}_{p^!}$

  * $\epsilon_{p_* \dashv p^!} p_* \cdot p_* \eta_{p_* \dashv p^!} = \mathrm{id}_{p_*}$

which makes the 1-cells into an [[adjoint quadruple]]

$$p_! \dashv p^* \dashv p_* \dashv p^!$$

The notations for the adjoint quadruple are derived from the introduction of [Shulman 2015](#Shulman15), but are traditionally expressed as 

$$\Pi \dashv \mathrm{Disc} \dashv \Gamma \dashv \mathrm{Codisc}$$

(i.e. see [[cohesive infinity-topos]]). However, we do not use the above notations because $\Pi$ conflicts with the use of $\Pi$ for the [[dependent product type]] (i.e. $\Pi x:A.B(x)$) and $\Gamma$ conflicts with the use of $\Gamma$ to express arbitrary contexts in [[inference rules]] in [[dependent type theory]]. 

The [[sharp modality|sharp]], [[flat modality|flat]], and [[shape modality|shape]] endo-modalities on the cohesive mode can be defined as composites of the modalities above:

$$\sharp \coloneqq p_* \circ p^!:\mathcal{c} \to \mathcal{c} \qquad \flat \coloneqq p_* \circ p^*:\mathcal{c} \to \mathcal{c} \qquad \esh \coloneqq p_! \circ p^*:\mathcal{c} \to \mathcal{c}$$

yielding the [[adjoint triple]]

$$\esh \dashv \flat \dashv \sharp$$

### The modal type theory

In the multimodal type theory associated with cohesive homotopy type theory, there are two type judgments: 

* $A \; \mathrm{type} \; \mathrm{at} \; \mathcal{d}$ which says that $A$ is a type in the crisp mode;

* $A \; \mathrm{type} \; \mathrm{at} \; \mathcal{c}$ which says that $A$ is a type in the cohesive mode.

Similarly, there are two term judgments:

* $a:A \; \mathrm{at} \; \mathcal{d}$ which says that $a$ is a term of type $A$ in the crisp mode;

* $a:A \; \mathrm{at} \; \mathcal{c}$ which says that $a$ is a term of type $A$ in the cohesive mode. 

and two context judgments:

* $\Gamma \; \mathrm{ctx} \; \mathrm{at} \; \mathcal{d}$ which says that $\Gamma$ is a context in the crisp mode;

* $\Gamma \; \mathrm{ctx} \; \mathrm{at} \; \mathcal{c}$ which says that $\Gamma$ is a context in the cohesive mode.

as well as two separate judgments each for [[judgmental equality]] of types and terms:

* $A \equiv B \; \mathrm{type} \; \mathrm{at} \; \mathcal{d}$ which says that $A$ and $B$ are judgmentally equal types in the crisp mode;

* $A \equiv B \; \mathrm{type} \; \mathrm{at} \; \mathcal{c}$ which says that $A$ and $B$ are judgmentally equal types in the cohesive mode;

* $a \equiv b:A \; \mathrm{at} \; \mathcal{d}$ which says that $a$ and $b$ are judgmentally equal terms of type $A$ in the crisp mode;

* $a \equiv b:A \; \mathrm{at} \; \mathcal{c}$ which says that $a$ and $b$ are judgmentally equal terms of type $A$ in the cohesive mode. 

* $\Gamma \equiv \Delta \; \mathrm{ctx} \; \mathrm{at} \; \mathcal{d}$ which says that $\Gamma$ and $\Delta$ are judgmentally equal contexts in the crisp mode;

* $\Gamma \equiv \Delta \; \mathrm{ctx} \; \mathrm{at} \; \mathcal{c}$ which says that $\Gamma$ and $\Delta$ are judgmentally equal contexts in the cohesive mode;

The [original papers](#GKNB21) on [[multimodal type theory]] use the symbol @ instead of $\mathrm{at}$ but it doesn't seem to be possible to put @ inside of latex math mode on the nLab, whether directly or inside the mathrm command. 

Then we have the rules for the [[context locks]] of the [[modalities]] of cohesive homotopy type theory:

$$\frac{\Gamma \; \mathrm{ctx} \; \mathrm{at} \; \mathcal{d}}{\Gamma, \mathrm{lock}_{p_!} \; \mathrm{ctx} \; \mathrm{at} \; \mathcal{c}} \qquad \frac{\Gamma \; \mathrm{ctx} \; \mathrm{at} \; \mathcal{c}}{\Gamma, \mathrm{lock}_{p^*} \; \mathrm{ctx} \; \mathrm{at} \; \mathcal{d}} \qquad \frac{\Gamma \; \mathrm{ctx} \; \mathrm{at} \; \mathcal{d}}{\Gamma, \mathrm{lock}_{p_*} \; \mathrm{ctx} \; \mathrm{at} \; \mathcal{c}} \qquad \frac{\Gamma \; \mathrm{ctx} \; \mathrm{at} \; \mathcal{c}}{\Gamma, \mathrm{lock}_{p^!} \; \mathrm{ctx} \; \mathrm{at} \; \mathcal{d}}$$

The [original papers](#GKNB21) also used a lock symbol that the author does not know how to replicate on the nLab.

(...)

([Kolomatskaia & Shulman 2023](#KS23) might also be useful here in defining the type theory)

## Example phenomena

Before looking at the consequences of the axioms formally, 
we mention some example phenomena to illustrate the meaning of the axioms.

### Geometric spaces and their cohesive homotopy types
 {#GeometricSpacesAndTheirHomotopyTypes}

We indicate one central aspect of geometric homotopy theory that is not visible in plain [[homotopy type theory]], but is captured by its cohesive refinement.

The standard [[interval]] $I = [0,1]$ in [[Top|topological spaces]]
plays two rather different roles, depending on what kind of
equivalence between spaces is considered. To make this more vivid,
it serves to think of $[0,1]$ as equipped 
even with its canonical structure
of a [[smooth manifold]] ([[manifold with boundary|with boundary]]).

The canonical map $I \to *$ to the [[point]] is certainly not
a [[diffeomorphism]], and from the point of view of
[[differential geometry]] the interval carries non-trivial structure.
Notably its endpoints $0,1 : I$ are not equivalent points ([[terms]])
in differential geometry, but are distinct. From the point of view of differential
geometry the interval is a [[homotopy n-type|homotopy 0-type]]
(has [[h-level]] 2) -- but one that is in some way equipped with geometric
structure.

This geometric structure, however, induces also a notion of 
_[[path groupoid|geometric paths]]_ in the interval, such that 
any two of its points are connected by such a path, after all.
In other words, one can form the smooth [[fundamental ∞-groupoid]]
$\Pi(I)$ of the interval and regard _that_ as a [[homotopy type]]
_without_ further geometric structure (a [[discrete ∞-groupoid]]). This $\Pi(I)$ is an _[[interval type]]_, while $I$ itself is not.

As such, the canonical map $\Pi(I) \to *$ is an [[equivalence]]
after all, namely a [[weak homotopy equivalence]]. Therefore,
after application of $\Pi$, what used to be a geometric 0-type
becomes a [[(-1)-groupoid|(-1)-type]] and actually a
[[(-2)-groupoid|(-2)-type]] ([[h-level]] 0) --  up to equivalence the [[interval type]], but without any geometry.

This latter property is what makes the interval important in bare
[[homotopy theory]], where it serves to model notions
such as [[cylinder objects]], [[left homotopies]], etc. The former
property, however, is what makes the interval important in [[geometry]], where it serves to model [[Cartesian spaces]], [[manifolds]], etc.

In cohesive homotopy type theory these two roles of the interval
can both be seen, via the reflective embedding of [[discrete objects]], 
and the transition between them is present, via the 
[[fundamental infinity-groupoid in a locally infinity-connected (infinity,1)-topos|fundamental ∞-groupoid reflector]] $\mathbf{\Pi}$.

Specifically, there is a [[model]] for 
[[cohesive (∞,1)-topos|homotopy cohesion]], called 
[[Smooth∞Grpd]], in which [[smooth manifolds]] 
([[manifold with boundary|with boundary]]) are 
[[full and faithful functor|fully faithfully embedded]],
where hence $I = [0,1]$ exists as a [[type]]
that behaves as the interval in [[differential geometry]],
and where $\mathbf{\Pi}(I)$ is equivalent to the [[unit type]].

More generally, in this model every [[smooth manifold]]
$X$ is a [[homotopy n-type|homotopy 0-type]]/[[0-truncated]]
object, but the type $\mathbf{\Pi}(X)$ is a [[discrete ∞-groupoid]]
whose [[homotopy type]] is that of the topological space underlying
$X$, as regarded in the 
[[model structure on topological spaces|standard]] [[homotopy category]] 
of topological spaces.

In particular, the smooth [[circle]] $S^1$ in this model is a 
[[0-truncated|0-type]] such that $\mathbf{\Pi}(S^1)$ is the
[[1-truncated|1-type]] $\mathbf{B}\mathbb{Z}$ (the [[delooping]]
[[groupoid]] of the [[integers]]).

One can turn this around and axiomatize a [[continuum]] [[line object]]
in cohesive homotopy type theory as a [[ring object]] 
$\mathbb{Z} \hookrightarrow \mathbb{A}^1$ such that 
$\mathbf{\Pi}(\mathbb{A}^1) \simeq *$.



## Structures in cohesive homotopy type theory
 {#Structures} 

We discuss implications of the axioms of cohesive homotopy type theory and go through the discussion of the various [[structures in a cohesive (∞,1)-topos]].

### Cohomology

For $X$ and $A$ two [[types]], the externalization $\sharp(X \to A)$ of the [[function type]] $X \to A$ is the _type of [[cocycles]]_ on $X$ with coefficients in $A$. Its [[h-level]] 2 [[truncated|truncation]] $\tau_0 \sharp(X \to Y)$ is the [[cohomology]] of $X$ with coefficients in $A$.

### Flat cohomology and local systems

We give the [[Coq]]-formalization of [Flat cohomology and local systems](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#FlatDifferentialCohomology).

For $A$ a [[type]], we say that [[cohomology]] with coefficients in 
$\flat A$ is _flat cohomology_. A [[cocycle]] [[term]] $c : \sharp(X \to \flat A)$ is called a [[local system]] of coefficients $A$ on $X$.

(...)

### de Rham cohomology

We give the [[Coq]]-formalization of [intrinsic de Rham cohomology](http://ncatlab.org/nlab/show/cohesive+%28infinity,1%29-topos+--+structures#deRhamCohomology).

Let $A = \mathbf{B}G$ be a [[0-connected|connected]] [[type]].

The [[homotopy fiber]] type of the coreflection $\flat \mathbf{B}G \to \mathbf{B}G$ we call the _de Rham coefficient type_ of $G$, denoted $\flat_{dR} \mathbf{B}G$. So there is a [[fiber sequence]]

$$
  \flat_{dR} \mathbf{B}G \to \flat \mathbf{B}G \to \mathbf{B}G
  \,.
$$

[[Coq]]-code:

    Require Import Homotopy Subtopos Codiscrete LocalTopos CohesiveTopos.

    Hypothesis BG : Type.
    Hypothesis BG_is_0connected : is_contr (pi0 BG).
    Hypothesis pt : BG.

    Definition flat_dR : #Type
      := ipullback (<nowiki>[[fun _:unit => pt]]</nowiki>) (from_flat ([BG])).

### Differential cohomology

We give the [[Coq]]-formalization of [Differential cohomology](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#DifferentialCohomology).

(...)

## Related concepts

* [[real-cohesive homotopy type theory]]

* [[A1-homotopy type theory]]

* [[fractured homotopy type theory]]

* [[geometric homotopy type theory]]

* [[modal homotopy type theory]]

* [[stable homotopy type]]

* [[differential homotopy type theory]]

## References
 {#References}

First discussion of a ([[homotopy type theory|homotopy]]) [[type theory|type theoretic]] formulation of the [[modal type theory|modal]] [[cohesive homotopy theory]] (adopting terminology from [Lawvere 2007](cohesive+topos#LawvereAxiomatic) ) considered in

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))

was given in

* {#SchreiberShulman2012} [[Urs Schreiber]], [[Mike Shulman]], *[[schreiber:Quantum gauge field theory in Cohesive homotopy type theory]]*, EPTCS **158** (2014) 109-126 &lbrack;[arXiv:1408.0054](https://arxiv.org/abs/1408.0054), [doi:10.4204/EPTCS.158.8](https://doi.org/10.4204/EPTCS.158.8)&rbrack;

following

* {#ShulmanInternalizing} [[Mike Shulman]], _Internalizing the external, or The Joys of Codiscreteness_ ([blog post](http://golem.ph.utexas.edu/category/2011/11/internalizing_the_external_or.html))

by adding [[axioms]] for the [[adjoint triple]] of [[modal operators]] to plain [[homotopy type theory]].


See also broader discussion in:

* [[Urs Schreiber]], _[[schreiber:Modern Physics formalized in Modal Homotopy Type Theory ]]_ (2016)

* [[David Corfield]], Chap. 5 of *[[davidcorfield:Modal Homotopy Type Theory]]*, Oxford University Press (2020) &lbrack;[ISBN:9780198853404](https://global.oup.com/academic/product/modal-homotopy-type-theory-9780198853404)&rbrack;

Another type-theoretic formulation of [[cohesive homotopy theory]], now obtained by changing the rewrite rules of type theory itself -- adding a [[syntax|syntactic]] notion of [[flat modality|flat]]-[[modal type|modal]] ("crisp") [[contexts]]:

* {#Shulman15} [[Mike Shulman]], _Brouwer's fixed-point theorem in real-cohesive homotopy type theory_, Mathematical Structures in Computer Science **28** 6 (2018) 856-941 &lbrack;[arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147)&rbrack;

following a general pattern for [[modal type theory]] laid out in

* {#LicataShulman} [[Dan Licata]], [[Mike Shulman]], *Adjoint logic with a 2-category of modes*, in _[Logical Foundations of Computer Science 2016](http://lfcs.info/lfcs-2016/)_,  Lecture Notes in Computer Science **9537** (2016) &lbrack;[doi:10.1007/978-3-319-27683-0_16](https://doi.org/10.1007/978-3-319-27683-0_16), [pdf](http://dlicata.web.wesleyan.edu/pubs/ls15adjoint/ls15adjoint.pdf), [slides](http://dlicata.web.wesleyan.edu/pubs/ls15adjoint/ls15adjoint-lfcs-slides.pdf)&rbrack;

with exposition in:

* {#Shulman19} [[Mike Shulman]], _Comonadic modalities and cohesion_, talk at _[Geometry in Modal Homotopy Type Theory](http://felix-cherubini.de/modal-workshop.html)_, 2019 ([pdf slides](http://home.sandiego.edu/~shulman/papers/cmu2019a.pdf), [talk recording](https://youtu.be/GA93Hjh-Alk))


This approach (also "real cohesive type theory") is now what most people refer to when speaking of cohesive homotopy type theory. 

Notice that at this point there is no [[proof assistant]] that actually implements the [[shape modality]] this way, only the system consisting of [[flat modality]] $\dashv$ [[sharp modality]] (*[[spatial type theory]]*) runs on computers: eg. via *[[Agda-flat]]*.

Discussion of a fragment of [[differential cohesive (infinity,1)-topos|differential cohesive]] homotopy type theory with [[Agda-flat]]:

* {#Wellen18} [[Felix Wellen]], _[[schreiber:thesis Wellen|Cartan Geometry in Modal Homotopy Type Theory]]_ ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966), [thesis pdf](http://www.math.kit.edu/iag3/~wellen/media/diss.pdf))

* [[Felix Cherubini]]: *Synthetic $G$-jet-structures in modal homotopy type theory*, Mathematical Structures in Computer Science (2024) 1–35 &lbrack;[doi:10.1017/S0960129524000355](https://doi.org/10.1017/S0960129524000355), [arXiv:1806.05966](https://arxiv.org/abs/1806.05966)&rbrack;


Further development of (real-)cohesive homotopy type theory:

* {#Myers19} [[David Jaz Myers]], _Good Fibrations through the Modal Prism_, Higher Structures **6** 1 (2022) 212–255 &lbrack;[arXiv:1908.08034v2](https://arxiv.org/abs/1908.08034), [higher-structures:Vol6Iss1/Myers](https://higher-structures.math.cas.cz/api/files/issues/Vol6Iss1/Myers)&rbrack;

Formalization of the shape/flat-[[fracture square]] ([[differential cohomology hexagon]]):

* {#Myers21} [[David Jaz Myers]], _Modal Fracture of Higher Groups_ &lbrack;[arXiv:2106.15390](https://arxiv.org/abs/2106.15390)&rbrack;

  also: talk at *[CMU-HoTT Seminar](https://www.cmu.edu/dietrich/philosophy/hott/seminars/index.html)*, 2021 ([pdf](http://davidjaz.com/Talks/CMU_March_2021.pdf), [[MyersModalFracture2021.pdf:file]])

Discussion of pairs of commuting cohesive structures (such as the combination of real cohesion and equivariant relevant for [[differential cohomology|differential]] [[orbifold cohomology]]:

* {#MyersRiley23} [[David Jaz Myers]], [[Mitchell Riley]], *Commuting Cohesions* &lbrack;[arXiv:2301.13780](https://arxiv.org/abs/2301.13780)&rbrack;

Exposition in:

* [[David Jaz Myers]], *Simplicial, Differential, and Equivariant Homotopy Type Theory*, talk at [[CQTS]] (Jan 2023) &lbrack;video: [rec](https://nyu.zoom.us/rec/play/uk0LXy5ub2YUpJPhYq5p7GvpZ2I8_CZaWHSpWvZgwuUyHeWjXgUj2AQd21K1WSJo90V5DrE0BVhl7NuB.QbyHhtPHaJVQUj2A?continueMode=true&_x_zm_rtaid=Xyx9WZFLQzyRzu0Oh-2mNQ.1675318497581.13147cc7929a947e978b29124a207f98&_x_zm_rhtaid=938)&rbrack;


For [[parametricity]] in cohesive homotopy type theory:

* {#Aberle24} [[C.B. Aberlé]], *Parametricity via Cohesion* &lbrack;[arXiv:2404.03825](https://arxiv.org/abs/2404.03825)&rbrack; 

The development of cohesive homotopy type theory as a [[multimodal type theory]] uses material from 

* {#GKNB21} [[Daniel Gratzer]], [[G. Alex Kavvos]], [[Andreas Nuyts]], [[Lars Birkedal]]: _Multimodal Dependent Type Theory_, Logical Methods in Computer Science **17** 3 (2021) lmcs:7713 &lbrack;[arXiv:2011.15021](https://arxiv.org/abs/2011.15021), <a href="https://doi.org/10.46298/lmcs-17(3:11)2021">doi:10.46298/lmcs-17(3:11)2021</a>&rbrack;

* {#KS23} [[Astra Kolomatskaia]], [[Michael Shulman]], *Displayed Type Theory and Semi-Simplicial Types* &lbrack;[arXiv:2311.18781](https://arxiv.org/abs/2311.18781)&rbrack; 

[[!redirects cohesive type theory]]
[[!redirects cohesive type theories]]

[[!redirects cohesive homotopy type theory]]
[[!redirects cohesive homotopy type theories]]

[[!redirects cohesive homotopy type]]
[[!redirects cohesive homotopy types]]

[[!redirects cohesive HoTT]]
