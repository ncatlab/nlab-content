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

Let $[D,C]$ denote the enriched [[functor category]], whose objects are $\mathbf{S}$-enriched functors $D\to C$.

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

+-- {: .num_theorem #CofGenProj}
###### Theorem
Suppose that

1. $C$ is a [[cofibrantly generated model category]], and
2. $C$ admits [[copowers]] by the hom-objects $D(x,y)\in \mathbf{S}$, which preserve trivial cofibrations.  (For instance, this is the case if $\mathbf{S}=Set$, or if $\mathbf{S}$ is a monoidal model category, $C$ is an $\mathbf{S}$-model category, and the hom-objects $D(x,y)$ are cofibrant in $\mathbf{S}$.)

Then the projective model structure $[D,C]_{proj}$ exists, and is again cofibrantly generated.
=--
+-- {: .proof}
###### Proof
Assuming the existence of such copowers, for any $x\in ob(D)$ the "evaluation at $x$" functor $ev_x : [D,C]\to C$ has a left adjoint $F_x$ sending $A\in C$ to the functor $y\mapsto D(x,y)\odot A$, where $\odot$ denotes the [[copower]].  Now if $I$ and $J$ are generating sets of cofibrations and trivial cofibrations for $C$, let $I^D$ be the set of maps $F_x(i)$ in $[D,C]$, for all $i\in I$ and $x\in ob(D)$, and similarly for $J$.  Then the projective fibrations and trivial fibrations are characterized by having the right lifting property with respect to $J^D$ and $I^D$ respectively, while both $I^D$ and $J^D$ permit the [[small object argument]] since $I$ and $J$ do and colimits in $[D,C]$ are pointwise.  Since the trivial fibrations in $[D,C]$ clearly coincide with the fibrations that are weak equivalences, it remains only to show that all $J^D$-cell complexes are weak equivalences.  But a $J^D$-cell complex is objectwise a cell complex built from cells $D(x,y)\odot j$ for maps $j\in J$, and the assumption ensures that these are trivial cofibrations in $C$, hence so is any cell complex built from them.
=--

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
Let $\mathbf{S}$ be a [[locally presentable base]], $C$ an $\mathbf{S}$-cocomplete locally $\mathbf{S}$-presentable $\mathbf{S}$-enriched category that is an [[accessible model category]], and $D$ a small $\mathbf{S}$-category.  Then:

1. If [[copowers]] by the hom-objects $D(x,y)$ preserve trivial cofibrations, then the projective model structure on $[D,C]$ exists and is accessible.
1. If [[copowers]] by the hom-objects $D(x,y)$ preserve cofibrations, then the injective model structure on $[D,C]$ exists and is accessible

\end{theorem}


### Combinatorial case

Every [[combinatorial model category]] (i.e. locally presentable and cofibrantly generated) is accessible, so Theorem \ref{Accessible} shows that both model structures exist, and Theorem \ref{CofGenProj} shows that the projective model structure is cofibrantly generated, hence also combinatorial.  In fact the injective model structure is also combinatorial, although the proof is much more involved, because there is no explicit description of the generating cofibrations and acyclic cofibrations; they have to be produced by a cardinality argument.  This was first proven by in [[Higher Topos Theory|HTT, prop. A.2.8.2 and A.3.3.2]] under strong assumptions on the enriching category (in particular that all objects are cofibrant), and later generalized by [Makkai and Rosicky](#MR13) to essentially the following:

\begin{theorem}\label{Combinatorial}
Let $\mathbf{S}$ be a [[locally presentable base]], $C$ an $\mathbf{S}$-cocomplete locally $\mathbf{S}$-presentable $\mathbf{S}$-enriched category that is a [[combinatorial model category]], and $D$ a small $\mathbf{S}$-category.  Then:

1. If [[copowers]] by the hom-objects $D(x,y)$ preserve trivial cofibrations, then the projective model structure on $[D,C]$ exists and is combinatorial.
1. If [[copowers]] by the hom-objects $D(x,y)$ preserve cofibrations, then the injective model structure on $[D,C]$ exists and is combinatorial.

\end{theorem}
\begin{proof}
It suffices to construct the factorizations, which follows from [MR13, Remark 3.8](#MR13) about left-lifting combinatorial weak factorization systems.
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


### Relation to other model structures

+-- {: .num_prop}
###### Proposition
If [[copowers]] by the hom-objects of $D$ preserve trivial cofibrations, then every every fibration in $[D,C]_{inj}$ is in particular a fibration in $[D,C]_{proj}$.  Similarly, if [[powers]] by the hom-objects of $D$ preserve trivial fibrations, then every cofibration in $[D,C]_{proj}$ is in particular a cofibration in $[D,C]_{inj}$.  The hypotheses are satisfied if $D$ is unenriched, or in the monoidal model category case if the hom-objects of $D$ are cofibrant.
=--

This is argued in the beginning of the proof of [[Higher Topos Theory|HTT, lemma A.2.8.3]].  For $Top$-enriched functors, this is ([Piacenza 91, section 5](#Piacenza91)). For details see at _[classical model structure on topological spaces -- Model structure on enriched functors](classical+model+structure+on+topological+spaces#ModelStructureOnTopEnrichedFunctors)_.

+-- {: .proof}
###### Proof
If $i:A\to B$ is a trivial cofibration in $C$ and $x\in ob(D)$, then the first assumption implies that $F_x(i) : F_x(A) \to F_x(B)$, for $F_x(A) (y) = D(x,y) \odot A$ the left adjoint of $ev_x : [D,C] \to C$, is a trivial cofibration in $[D,C]_{inj}$.  Thus, any fibration $p$ in $[D,C]_{inj}$ has the right lifting property with respect to it, which is to say that $ev_x(p)$ has the right lifting property with respect to $i$.  Since this is true for any $i$, each $ev_x(p)$ is a fibration, i.e. $p$ is a fibration in $[D,C]_{inj}$.  The other half is dual.
=--

+-- {: .num_cor}
###### Corollary

The [[identity functors]]

$$
  [D,C]_{inj}   
    \stackrel{\overset{Id}{\leftarrow}}{\underset{Id}{\to}}
  [D,C]_{proj}
$$

form a [[Quillen equivalence]] (with $Id : [D,C]_{proj} \to [D,C]_{inj}$ being the left Quillen functor).

If $D$ is a [[Reedy category]] this factors through the [[Reedy model structure]]

$$
  [D,C]_{inj}   
    \stackrel{\overset{Id}{\leftarrow}}{\underset{Id}{\to}}
  [D,C]_{Reedy}
    \stackrel{\overset{Id}{\leftarrow}}{\underset{Id}{\to}}
  [D,C]_{proj}
$$

=--

### Functoriality in domain and codomain

+-- {: .num_prop #QuillenFunctorialityInCodomain}
###### Proposition

The functor model structures depend [[Quillen adjunction|Quillen-functorially]] on their [[codomain]], in that for

$$
  D_1 \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D_2
$$

a $\mathbf{S}$-[[enriched Quillen adjunction]] between [[combinatorial model categories|combinatorial]] $\mathbf{S}$-[[enriched model categories]], postcomposition induces $\mathbf{S}$-[[enriched Quillen adjunctions]]

$$
  [C,D_1]_{proj} \stackrel{\overset{[C,L]}{\leftarrow}}{\underset{[C,R]}{\to}} [C,D_2]_{proj}  
$$

and

$$
  [C,D_1]_{inj} \stackrel{\overset{[C,L]}{\leftarrow}}{\underset{[C,R]}{\to}} [C,D_2]_{inj}  
  \,.
$$

Moreover, if $(L \dashv R)$ is a [[Quillen equivalence]], then so is $([C,L] \dashv [C,R])$.

=--

For the case that $C$ is a small category this is ([Lurie, remark A.2.8.6](#Lurie)), for the enriched case this is ([Lurie, prop. A.3.3.6](#Lurie)).



The Quillen-functoriality on the domain is more asymmetric. 

+-- {: .num_prop}
###### Proposition

For $p : C_1 \to C_2$ a functor between small categories or an $\mathbf{S}$-[[enriched functor]] between $\mathbf{S}$-[[enriched categories]], let 

$$
  (p_! \dashv p^* \dashv p_*) :  [C_2,D] 
  \stackrel{\overset{p_!}{\leftarrow}}{\stackrel{\overset{p^*}{\to}}{\underset{p_*}{\leftarrow}}}
 [C_1,D]
$$ 

be the [[adjoint triple]] where $p^*$ is precomposition with $p$ and where $p_!$ and $p_*$ are left and right [[Kan extension]] along $p$, respectively.

Then we have [[Quillen adjunctions]]

$$
  (p_! \dashv p^*) :
  [C_1,D]_{proj} \stackrel{\overset{p_!}{\to}}{\underset{p^*}{\leftarrow}}
  [C_2,D]_{proj}
$$

and

$$
  (p^* \dashv p_*) :
  [C_1,D]_{inj} \stackrel{\overset{p^*}{\leftarrow}}{\underset{p_*}{\to}}
  [C_2,D]_{inj}
  \,.
$$


=--

For $C$ not enriched this appears as ([Lurie, prop. A.2.8.7](#Lurie)), for the enriched case it appears as ([Lurie, prop. A.3.3.7](#Lurie)).

+-- {: .num_remark } 
###### Remark

In the $sSet$-enriched case, if $p : D_1 \to D_2$ is an [[weak equivalence]] in the [[model structure on sSet-categories]], then these two Quillen adjunctions are both [[Quillen equivalence]]s.

=--

+-- {: .num_prop #PresentationOfInfinityFunctors} 
###### Proposition

For $C$ a [[combinatorial simplicial model category]], the [[(∞,1)-category]] [[presentable (∞,1)-category|presented by]] $[D,C]_{proj}$ and $[D,C]_{inj}$ under the above assumptions is the [[(∞,1)-category of (∞,1)-functors]] $Func(D,C^\circ)$ from the ordinary category $D$ to the $(\infty,1)$-category presented by $C$.

=--

See [[(∞,1)-category of (∞,1)-functors]] for details.


### Relation to homotopy Kan extensions/limits/colimits

Often functors $D \to C$ are thought of as [[diagram]]s in the model category $C$, and one is interested in obtaining their [[homotopy limit]] or [[homotopy colimit]] or, generally, for $p : D \to D'$ any functor, their left and right [[homotopy Kan extension]].

These are the left and right [[derived functor]]s $HoLan := \mathbb{L} p_1$ and $HoRan := \mathbb{R} p_*$ of

$$
  [D,C]_{proj} \stackrel{p_!}{\to}  [D',C]_{proj}
$$

and

$$
  [D,C]_{inj} \stackrel{p_*}{\to} [D',C]_{inj}
$$

respectively.

For more on this see [[homotopy Kan extension]]. For the case that $D' = *$ this reduces to [[homotopy limit]] and [[homotopy colimit]].

## Examples

Examples of cofibrant objects in the projective model structure are discussed at 

* [[projectively cofibrant diagram]].

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

General review and discussion includes

* [[Philip Hirschhorn]], section 11.6 in _Model categories and their localizations_, 2003 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))

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

* {#MR13} [[M. Makkai]], [[J. Rosický]], _Cellular categories_, 2013, [arXiv:1304.7572](https://arxiv.org/abs/1304.7572)

See also 

* [[David White]], _Modified projective model structure_ ([MO comment](http://mathoverflow.net/questions/76160/acyclic-models-via-model-categories/104423#104423))

[[!redirects model structures on functors]]

[[!redirects injective model structure]]
[[!redirects injective model structure on functors]]
[[!redirects projective model structure]]
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
