+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The [[model category]] structures on [[functor category|functor categories]] are models for [[(∞,1)-category of (∞,1)-functors|(∞,1)-categories of (∞,1)-functors]].

For $C$ a [[model category]] and $D$ any [[small category]] there are two "obvious" ways to put a [[model category]] structure on the [[functor category]] $[D,C]$, called the _projective_ and the _injective_ model structures.  For completely general $C$, neither one need exist, but there are rather general conditions that ensure their existence.  In particular, the projective model structure exists as long as $C$ is [[cofibrantly generated model category|cofibrantly generated]], while both model structures exist if $C$ is [[accessible model category|accessible]] (and in particular if it is [[combinatorial model category|combinatorial]]).  In the case of [[enriched category|enriched]] diagrams, additional cofibrancy-type conditions are required on $D$.

A related kind of model structure is the [[Reedy model structure]]/[[generalized Reedy model structure]] on functor categories, which applies for *any* model category $C$, but requires $D$ to be a very special sort of category, namely a [[Reedy category]]/[[generalized Reedy category]].

In the special case that $C = $ [[sSet]] is the [[classical model structure on simplicial sets]] the projective and injective model structure on the functor categories $[D,SSet]$ are described in more detail at [[global model structure on simplicial presheaves]] and [[model structure on sSet-enriched presheaves]].

## Definition

Let $\mathbf{S}$ be a [[symmetric monoidal category]], let $C$ be an $\mathbf{S}$-[[model category]] that is an $\mathbf{S}$-[[enriched category]], and let $D$ be a [[small category|small]] $\mathbf{S}$-enriched category. Usually we have either $\mathbf{S}=Set$ or else $\mathbf{S}$ is a [[monoidal model category]] and $C$ an $\mathbf{S}$-[[enriched model category]].

Let $[D,C]$ denote the enriched [[functor category]], whose objects are $\mathbf{S}$-enriched functors $D\longrightarrow C$.

+-- {: .num_defn #ProjectiveAndInjectiveStructure}
###### Definition
We define the following classes of maps in $[D,C]$:

* the **projective weak equivalences** and **projective fibrations** are the [[natural transformations]] that are objectwise such morphisms in $C$.
* the **injective weak equivalences** and **injective cofibrations** are the [[natural transformations]] that are objectwise such morphisms in $C$.

If either of these choices defines a model structure on $[D,C]$, we call it the **projective model structure** $[D,C]_{proj}$ or **injective model structure** $[D,C]_{inj}$ respectively.  Of course, the projective cofibrations and injective fibrations can then be characterized by lifting properties.
=--


## Existence

### Projective case

The projective model structure can be regarded as a right-[[transferred model structure]].  This yields the following basic result on its existence.

\\begin{theorem}\label{ExistenceOfProjectiveStructureOnEnrichedFunctors}
**(existence and cofibrant generation of projective structure on enriched functors)**
\linebreak
Given

* $\mathbf{S}$ a [[cosmos for enrichment]],

* $D$, $C$ a pair of $\mathbf{S}$-enriched categories

where $C$ carries the [[structure]] of 

1. a [[cofibrantly generated model category]], 

2. which admits [[copowers]] by the [[hom-objects]] $D(x,y)\in \mathbf{S}$, which preserve [[acyclic cofibrations]].  

   (This is the case for instance if $\mathbf{S}=$ [[Set]], or if $\mathbf{S}$ is a [[monoidal model category]], $C$ is an [[enriched model category|$\mathbf{S}$-model category]], and the [[hom-objects]] $D(x,y)$ are cofibrant in $\mathbf{S}$.)

Then the projective model structure $[D,C]_{proj}$ on the [[enriched functor category]] exists, and is again cofibrantly generated.
\end{theorem}
(For $\mathbf{S} = $ [[Sets]] this is [Hirschhorn 2002, Thm. 11.6.1](#Hirschhorn02).).
\begin{proof}
Assuming the existence of such copowers, for any $x\in ob(D)$ the "[[evaluation]] at $x$" functor $ev_x \colon [D,C]\longrightarrow C$ has a [[left adjoint]] $F_x$ sending $A\in C$ to the functor $y\mapsto D(x,y)\odot A$, where $\odot$ denotes the [[copower]].  Now if $I$ and $J$ are generating sets of cofibrations and trivial cofibrations for $C$, let $I^D$ be the set of maps $F_x(i)$ in $[D,C]$, for all $i\in I$ and $x\in ob(D)$, and similarly for $J$.  Then the projective fibrations and trivial fibrations are characterized by having the right lifting property with respect to $J^D$ and $I^D$ respectively, while both $I^D$ and $J^D$ permit the [[small object argument]] since $I$ and $J$ do and colimits in $[D,C]$ are pointwise.  Since the trivial fibrations in $[D,C]$ clearly coincide with the fibrations that are weak equivalences, it remains only to show that all $J^D$-cell complexes are weak equivalences.  But a $J^D$-cell complex is objectwise a cell complex built from cells $D(x,y)\odot j$ for maps $j\in J$, and the assumption ensures that these are trivial cofibrations in $C$, hence so is any cell complex built from them.
\end{proof}

There do exist projective model structures that do not fall under this theorem, however, such as the following.

+-- {: .un_theorem}
###### Theorem
If $C$ is a [[locally presentable category|locally presentable]] [[2-category]] with its [[2-trivial model structure]] and $D$ is a small 2-category, then the projective model structure on $[D,C]$ exists.
=--
+-- {: .proof}
###### Proof
This follows from the result of [Lack](#Lack06) on [[transferred model structures]] for algebras over [[2-monads]], since $[D,C]$ is the category of algebras for an accessible 2-monad on $C^{ob(D)}$.
=--

Note that $C$ need not be cofibrantly generated (and the 2-trivial model structure often fails to be cofibrantly generated), so the generality of this result is not entirely included in the previous one.


### Accessible case

In the case when $C$ is an [[accessible model category]], i.e. it is a [[locally presentable category]] and its constituent [[weak factorization systems]] have [[accessible functor|accessible]] realizations as [[functorial factorizations]], we have the following general result from [Moser](#Moser) (the unenriched case appears in [HKRS15](#HKRS15) and [GKR18](#GKR18)).

\begin{theorem}\label{Accessible}
Let 

* $\mathbf{S}$ be a [[locally presentable category|locally presentable]] [[cosmos]]

* $C$ an $\mathbf{S}$-cocomplete locally $\mathbf{S}$-presentable $\mathbf{S}$-[[enriched category]] that is an [[accessible model category]], 

* $D$ a [[small category|small]] $\mathbf{S}$-category.  

Then:

1. If [[copowers]] by the [[hom-objects]] $D(x,y)$ preserve [[acyclic cofibrations]], then the projective model structure on $[D,C]$ exists and is accessible.

1. If [[copowers]] by the hom-objects $D(x,y)$ preserve [[cofibrations]], then the injective model structure on $[D,C]$ exists and is accessible

\end{theorem}


### Combinatorial case
 {#CombinatorialCase}

Every [[combinatorial model category]] (i.e. locally presentable and cofibrantly generated) is accessible, so Theorem \ref{Accessible} shows that both model structures exist, and Theorem \ref{CofGenProj} shows that the projective model structure is cofibrantly generated, hence (by [this Prop.](locally+presentable+category#PresheavesWithValuesInLocPresAreLocPres)) also [[combinatorial model category|combinatorial]].  

In fact the injective model structure is also combinatorial, although the proof is much more involved, because there is no explicit description of the generating cofibrations and acyclic cofibrations; they have to be produced by a cardinality argument.  This was first proven by in [[Higher Topos Theory|HTT, prop. A.2.8.2 and A.3.3.2]] under strong assumptions on the enriching category (in particular that all objects are cofibrant), and later generalized by [Makkai & Rosický 2014](#MakkaiRosický14) to essentially the following:

\begin{theorem}\label{Combinatorial}
Let $\mathbf{S}$ be a [[locally presentable category|locally presentable]] [[cosmos]], $C$ an $\mathbf{S}$-cocomplete locally $\mathbf{S}$-presentable $\mathbf{S}$-[[enriched category]] that is a [[combinatorial model category]], and $D$ a small $\mathbf{S}$-category.  Then:

1. If [[copowers]] by the hom-objects $D(x,y)$ preserve trivial cofibrations, then the projective model structure on $[D,C]$ exists and is combinatorial.

1. If [[copowers]] by the hom-objects $D(x,y)$ preserve cofibrations, then the injective model structure on $[D,C]$ exists and is combinatorial.

\end{theorem}
\begin{proof}
It suffices to construct the factorizations, which follows from [Makkai & Rosický 2014, Remark 3.8](#MakkaiRosický14) about left-lifting combinatorial weak factorization systems.
\end{proof}

## Properties

### General

+-- {: .num_prop}
###### Proposition

The projective and injective structures $[D,C]_{proj}$ and $[D,C]_{inj}$, def. \ref{ProjectiveAndInjectiveStructure}, are (insofar as they exist):

* right or left [[proper model categories]] if $C$ is right or left proper, respectively.

* $\mathbf{S}$-[[enriched model categories]] if $C$ is an $\mathbf{S}$-model category.

=--

The statement about properness appears as [[Higher Topos Theory|HTT, remark A.2.8.4]].

+-- {: .num_prop #PresentationOfInfinityFunctors}
###### Proposition

For $C$ a [[combinatorial simplicial model category]], the [[(∞,1)-category]] [[presentable (∞,1)-category|presented by]] $[D,C]_{proj}$ and $[D,C]_{inj}$ under the above assumptions is the [[(∞,1)-category of (∞,1)-functors]] $Func(D,C^\circ)$ from the ordinary category $D$ to the $(\infty,1)$-category presented by $C$.

=--

See at *[[(∞,1)-category of (∞,1)-functors]]* for more.


### Relation to other model structures

+-- {: .num_prop}
###### Proposition
If [[copowers]] by the hom-objects of $D$ preserve trivial cofibrations, then every every fibration in $[D,C]_{inj}$ is in particular a fibration in $[D,C]_{proj}$.  Similarly, if [[powers]] by the hom-objects of $D$ preserve trivial fibrations, then every cofibration in $[D,C]_{proj}$ is in particular a cofibration in $[D,C]_{inj}$.  The hypotheses are satisfied if $D$ is unenriched, or in the monoidal model category case if the hom-objects of $D$ are cofibrant.
=--

This is argued in the beginning of the proof of [[Higher Topos Theory|HTT, lemma A.2.8.3]].  For $Top$-enriched functors, this is ([Piacenza 91, section 5](#Piacenza91)). For details see at _[classical model structure on topological spaces -- Model structure on enriched functors](classical+model+structure+on+topological+spaces#ModelStructureOnTopEnrichedFunctors)_.

+-- {: .proof}
###### Proof
If $i:A\longrightarrow B$ is a trivial cofibration in $C$ and $x\in ob(D)$, then the first assumption implies that $F_x(i) : F_x(A) \longrightarrow F_x(B)$, for $F_x(A) (y) = D(x,y) \odot A$ the left adjoint of $ev_x : [D,C] \longrightarrow C$, is a trivial cofibration in $[D,C]_{inj}$.  Thus, any fibration $p$ in $[D,C]_{inj}$ has the right lifting property with respect to it, which is to say that $ev_x(p)$ has the right lifting property with respect to $i$.  Since this is true for any $i$, each $ev_x(p)$ is a fibration, i.e. $p$ is a fibration in $[D,C]_{inj}$.  The other half is dual.
=--

+-- {: .num_cor}
###### Corollary

The [[identity functors]]

$$
  [D,C]_{inj}
    \stackrel{\overset{Id}{\longleftarrow}}{\underset{Id}{\longrightarrow}}
  [D,C]_{proj}
$$

form a [[Quillen equivalence]] (with $Id : [D,C]_{proj} \longrightarrow [D,C]_{inj}$ being the left Quillen functor).

If $D$ is a [[Reedy category]] this factors through the [[Reedy model structure]]

$$
  [D,C]_{inj}
    \stackrel{\overset{Id}{\longleftarrow}}{\underset{Id}{\longrightarrow}}
  [D,C]_{Reedy}
    \stackrel{\overset{Id}{\longleftarrow}}{\underset{Id}{\longrightarrow}}
  [D,C]_{proj}
$$

=--

### Functoriality in domain and codomain

+-- {: .num_prop #QuillenFunctorialityInCodomain}
###### Proposition

The functor model structures depend [[Quillen adjunction|Quillen-functorially]] on their [[codomain]], in that for

$$
  D_1
  \stackrel
    {\overset{L}{\longleftarrow}}
    {\underset{R}{\longrightarrow}}
  D_2
$$

an $\mathbf{S}$-[[enriched Quillen adjunction]] between [[combinatorial model categories|combinatorial]] $\mathbf{S}$-[[enriched model categories]], postcomposition induces $\mathbf{S}$-[[enriched Quillen adjunctions]]

$$
  [C,D_1]_{proj}
    \stackrel
      {\overset{[C,L]}{\longleftarrow}}
      {\underset{[C,R]}{\longrightarrow}}
  [C,D_2]_{proj}
$$

and

$$
  [C,D_1]_{inj}
    \stackrel
      {\overset{[C,L]}{\longleftarrow}}
      {\underset{[C,R]}{\longrightarrow}}
  [C,D_2]_{inj}
  \,.
$$

Moreover, if $(L \dashv R)$ is a [[Quillen equivalence]], then so is $([C,L] \dashv [C,R])$.

=--

For the case that $C$ is a small category this is &lbrack;[Lurie, remark A.2.8.6](#Lurie)&rbrack;, for the enriched case this is &lbrack;[Lurie, prop. A.3.3.6](#Lurie)&rbrack;.



The Quillen-functoriality on the [[domain]] is more asymmetric.

\begin{proposition}
\label{QuillenFunctorialityInDomain}
**(Quillen functoriality in the domain category)**
\linebreak
For $p \colon C_1 \longrightarrow C_2$ a functor between small categories or an $\mathbf{S}$-[[enriched functor]] between $\mathbf{S}$-[[enriched categories]], let

$$
  (p_! \dashv p^* \dashv p_*)
  \;\colon\;
  [C_2,D]
  \stackrel{\overset{p_!}{\longleftarrow}}{\stackrel{\overset{p^*}{\longrightarrow}}{\underset{p_*}{\longleftarrow}}}
 [C_1,D]
$$

be the [[adjoint triple]] where $p^*$ is precomposition with $p$ and where $p_!$ and $p_*$ are left and right [[Kan extension]] along $p$, respectively.

Then we have [[Quillen adjunctions]]

$$
  (p_! \dashv p^*) 
  \;\colon\;
  [C_1,D]_{proj} \stackrel{\overset{p_!}{\longrightarrow}}{\underset{p^*}{\longleftarrow}}
  [C_2,D]_{proj}
$$

and

$$
  (p^* \dashv p_*)
  \;\colon\;
  [C_1,D]_{inj} \stackrel{\overset{p^*}{\longleftarrow}}{\underset{p_*}{\longrightarrow}}
  [C_2,D]_{inj}
  \,.
$$

\end{proposition}

For $C$ not enriched this appears as &lbrack;[Lurie, prop. A.2.8.7](#Lurie)&rbrack;, for the enriched case it appears as &lbrack;[Lurie, prop. A.3.3.7](#Lurie)&rbrack;.

+-- {: .num_remark }
###### Remark

In the $sSet$-enriched case, if $p : D_1 \longrightarrow D_2$ is a [[weak equivalence]] in the [[model structure on sSet-categories]], then these two Quillen adjunctions are both [[Quillen equivalence]]s.

=--



### Relation to homotopy Kan extensions/limits/colimits

Often functors $D \longrightarrow C$ are thought of as [[diagram]]s in the model category $C$, and one is interested in obtaining their [[homotopy limit]] or [[homotopy colimit]] or, generally, for $p : D \longrightarrow D'$ any functor, their left and right [[homotopy Kan extension]].

These are the left and right [[derived functor]]s $HoLan := \mathbb{L} p_1$ and $HoRan := \mathbb{R} p_*$ of

$$
  [D,C]_{proj} \stackrel{p_!}{\longrightarrow}  [D',C]_{proj}
$$

and

$$
  [D,C]_{inj} \stackrel{p_*}{\longrightarrow} [D',C]_{inj}
$$

respectively.

For more on this see [[homotopy Kan extension]]. For the case that $D' = *$ this reduces to [[homotopy limit]] and [[homotopy colimit]].


### Relation to $\infty$-functor categories
 {#RelationToInfinityFunctorCategories}

\begin{proposition}
  For 

  * $\mathbf{C}$ a [[combinatorial simplicial model category]]

  * $\mathbf{D}$ a [[small category|small]] [[sSet-enriched category]]

then both the projective and the injective model structure on the [[sSet]]-[[enriched functor category]] $sFunc(\mathbf{D}, \mathbf{C})$ (which exist by the above discussion) [[presentable (infinity,1)-category|present]] the corresponding [[(infinity,1)-category of (infinity,1)-functors|$\infty$-category of $\infty$-functors]]. Concretely: 

The [[homotopy coherent nerve]] of the [[full subcategory|full]] [[sSet-enriched category|sSet-enriched]] [[subcategory]] of the functor model category on its [[bifibrant objects]], $\big(\mathbf{sFunc}(\mathbf{D}, \mathbf{C})\big)^\circ$, is [[equivalence of quasi-categories|equivalent]] to the [[(infinity,1)-functor (infinity,1)-category|$\infty$-functor]] [[quasi-category]] between the [[homotopy coherent nerves]]
$$
  N \big( \mathbf{sFunc}(\mathbf{D}, \mathbf{C})^\circ \big)
  \;\;
  \underset{qCat}{\simeq}
  \;\;
  Func_\infty
  \Big(
    N(\mathbf{D})
    ,\,
    N\big( \mathbf{C}^\circ \big)
  \Big)
  \,.
$$
\end{proposition}
This is due to [Lurie (2009), Prop. 4.2.4.4](#Lurie). See also the discussion *[here](infinity1-category+of+infinity1-functors#ModelCategoryPresentation)* at *[[(infinity,1)-category of (infinity,1)-functors|$\infty$-category of $\infty$-functors]]*.


## Examples

Examples of cofibrant objects in the projective model structure are discussed at *[[projectively cofibrant diagram]]*.

\begin{example}
**([[model structure on simplicial presheaves]])**
\linebreak
  Model structures on [[sSet]]-valued [[functors]], hence on [[simplicial presheaves]], play a central role in the theory of [[combinatorial model categories]] and specifically in [[model topos]]-theory presenting [[(infinity,1)-topos|$\infty$-toposes]]. See at *[[model structure on simplicial presheaves]]* for more.
\end{example}

Specifically:

\begin{example}
\label{BorelModelStructureOnSimplicialGroupActions}
**([[Borel model structure]] on [[simplicial group actions]])**
\linebreak
For $\mathcal{G} \,\in\, Grp(sSet)$ a [[simplicial group]] with [[sSet]]-[[enriched groupoid|enriched]] [[delooping groupoid]] denoted $\mathbf{B}\mathcal{G} \in sSet\text{-}Grpd$, an [[sSet]]-[[enriched functor]] $\mathbf{B}\mathcal{G} \longrightarrow sSet$ is equivalently a [[simplicial group action]] of $\mathcal{G}$.

Under this identification, the projective model strcuture on [[simplicial functors]] (Prop. \ref{ExistenceOfProjectiveStructureOnEnrichedFunctors}) is equivalently the *[[Borel model structure]]* on [[simplicial group actions]], a context of Borel-[[equivariant homotopy theory]]:

$$
  sFunc\big(
    \mathbf{B}\mathcal{G}
    ,\,
    sSet
  \big)_{proj}
  \;\;
  =
  \;\;
  \mathcal{G}Act(sSet)_{Borel}
  \,.
$$

More generally, for $\mathcal{X} \in sSet\text{-}Grpd$ an [[sSet]]-[[enriched groupoid]] (Dwyer-Kan [[simplicial groupoid]]) with a single [[connected component]] $\pi_0(\mathcal{X}) \simeq \{[x]\}$, so that the inclusion
$$
  \iota 
    \,\colon\, 
  \mathbf{B}(\mathcal{X}(x,x))
  \xhookrightarrow{\phantom{---}}
  \mathcal{X}
$$
is an [[sSet]]-[[enriched adjoint equivalence]] (see discussion [there](simplicial+groupoid#RelationToSimplicialGroups)) the projective model structure on [[simplicial functors]] from Prop. \ref{ExistenceOfProjectiveStructureOnEnrichedFunctors} is [[transferred model structure|transferred]] under the induced [[adjoint equivalence]] of [[sSet]]-[[enriched functor categories]]
$$
  sFunc\big(
    \mathcal{X}
    ,\,
    sSet
  \big)_{proj}
  \underoverset
    {\underset{\iota^\ast}{\longrightarrow}}
    {\overset{\iota_!}{\longleftarrow}}
    {\;\; \bot_{\simeq} \;\;}
  sFunc\Big(
    \mathbf{B}\big(\mathcal{X}(x,x)\big)
    ,\,
    sSet
  \Big)_{proj}
  \;=\;
  \big(\mathcal{X}(x,x)\big) Act(sSet)_{Borel}
$$
By [this example](transferred+model+structure#RightTransferAlongAdjointEquivalence) it follows that morphisms in all three classes $(\mathrm{W}, Fib, Cof)$ in $sFunc(\mathcal{X}, \, sSet)_{proj}$ are those which restrict on $x \in Obj(\mathcal{X})$ to the respective class in $\big(\mathcal{X}(x,x)\big) Act(sSet)_{Borel}$.

It follows that for $\mathcal{X} \,\in\, sSet\text{-}Grpd$ a [[simplicial groupoid]] with any set $\pi_0(\mathcal{X})$ of [[connected components]], the projective model structure of simplicial functors over it is the [product model structure](model+category#ProductModelStructure) of the [[Borel model structures]] of [[simplicial group actions]], one for each connected component:
$$
  sFunc\big(
    \mathcal{X}
    ,\,
    sSet
  \big)_{proj}
  \underoverset
    {\underset{\iota^\ast}{\longrightarrow}}
    {\overset{\iota_!}{\longleftarrow}}
    {\;\; \bot_{\simeq} \;\;}
  \underset{i \in \pi_0(\mathcal{X})}{\prod}
  sFunc\Big(
    \mathbf{B}\big(\mathcal{X}(x_i,x_i)\big)
    ,\,
    sSet
  \Big)_{proj}
  \;=\;
  \underset{i \in \pi_0(\mathcal{X})}{\prod}
  \big(\mathcal{X}(x_i,x_i)\big) Act(sSet)_{Borel}
  \,.
$$
\end{example}



## Related concepts

* [[Reedy model structure]], [[generalized Reedy model structure]],

* [[model structure on sections]]

* [[lim^1 and Milnor sequences]]

* [[model structure on homotopical presheaves]], [[model structure on simplicial presheaves]]

* [[model structure for n-excisive functors]]

## References

The projective model structure on $Top_{Quillen}$-enriched functors is discussed in

* {#Piacenza91} [[Robert Piacenza]]  section 5 of _Homotopy theory of diagrams and CW-complexes over a category_, Can. J. Math. Vol 43 (4), 1991 ([[Piazenza91.pdf:file]])

  also chapter VI of [[Peter May]] et al., _Equivariant homotopy and cohomology theory_, 1996 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/alaska.pdf))

See also

* [[Alex Heller]], _Homotopy in functor categories_, Transactions of the AMS, vol 272, Number 1, July 1982 ([JSTOR](http://www.jstor.org/stable/1998955))

Textbook account of the projective model structure

* {#Hirschhorn02} [[Philip Hirschhorn]], §11.6 in: _[[Model Categories and Their Localizations]]_, AMS Math. Survey and Monographs **99** (2002) &lbrack;[ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/pshmain.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf)&rbrack;

The injective model structure for unenriched diagrams of simplicial sets was first constructed by

* [[Alex Heller]], _Homotopy theories_

Probably the first general construction of injective model structures for enriched diagrams in combinatorial model categories was in

* {#Lurie} [[Jacob Lurie]],  sections A.2.8 (unenriched) and section A.3.3 (enriched) of _[[Higher Topos Theory]]_, 2009

The projective model structure for functors to [[sSet]] on a _[[large category|large]]_ domain is discussed in

* [[Boris Chorny]], [[William Dwyer]], _Homotopy theory of small diagrams over large categories_, [arXiv:math/0607117](http://arxiv.org/abs/math/0607117)

The case of diagrams in a 2-category is a special case of

* {#Lack06} [[Steve Lack]], *Homotopy-theoretic aspects of 2-monads*, [arXiv](http://arxiv.org/abs/math.CT/0607646)

The use of accessible model structures to construct both projective and injective model structures on unenriched diagrams was introduced in

* Marzieh Bayeh, [[Kathryn Hess]], [[Varvara Karpova]], Magdalena K&#281;dziorek, [[Emily Riehl]], [[Brooke Shipley]], _Left-induced model structures and diagram categories_ ([arXiv:1401.3651](http://arxiv.org/abs/1401.3651))

* {#HKRS15} [[Kathryn Hess]], Magdalena K&#281;dziorek, [[Emily Riehl]], [[Brooke Shipley]], _A necessary and sufficient condition for induced model structures_ ([arXiv:1509.08154](http://arxiv.org/abs/1509.08154)).  This paper contains an error, corrected by:

* {#GKR18} [[Richard Garner]], Magdalena Kedziorek, [[Emily Riehl]], _Lifting accessible model structures_, [arXiv:1802.09889](https://arxiv.org/abs/1802.09889)

It was generalized to enriched diagrams in

* {#Moser} Lyne Moser, *Injective and Projective Model Structures on Enriched Diagram Categories*, [arXiv:1710.11388](https://arxiv.org/abs/1710.11388)

The more general result above on combinatoriality of injective model structures follows from Remark 3.8 of

* {#MakkaiRosický14} [[M. Makkai]], [[J. Rosický]], _Cellular categories_, J. Pure Appl. Alg. **218** (2014) 1652-1664 &lbrack;[arXiv:1304.7572](https://arxiv.org/abs/1304.7572), [doi:10.1016/j.jpaa.2014.01.005](https://doi.org/10.1016/j.jpaa.2014.01.005)&rbrack;

See also

* [[David White]], _Modified projective model structure_ ([MO comment](http://mathoverflow.net/questions/76160/acyclic-models-via-model-categories/104423#104423))

[[!redirects model structures on functors]]

[[!redirects injective model structure]]
[[!redirects injective model structures]]
[[!redirects injective model structure on functors]]
[[!redirects projective model structure]]
[[!redirects projective model structures]]
[[!redirects projective model structure on functors]]

[[!redirects global model structure on functor categories]]
[[!redirects global model structures on functor categories]]
[[!redirects global model structure on functors]]
[[!redirects global model structures on functors]]

[[!redirects model structure on enriched functors]]
[[!redirects model structures on enriched functors]]

[[!redirects projective model structure on enriched functors]]
[[!redirects projective model structures on enriched functors]]
[[!redirects injective model structure on enriched functors]]
[[!redirects injective model structures on enriched functors]]

[[!redirects model structure on simplicial functors]]
[[!redirects projective model structure on simplicial functors]]
[[!redirects injective model structure on simplicial functors]]

