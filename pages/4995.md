
> This entry is about a refinement of the concept of [[cohesive topos]]. The definition here expresses an intuition not unrelated to that at [[cohesive (∞,1)-presheaf on E-∞ rings]] but the definitions are unrelated and apply in somewhat disjoint contexts.


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A _cohesive $(\infty,1)$-topos_ is a [[big topos|gros]] [[(∞,1)-topos]] $\mathbf{H}$ that provides a context of generalized [[spaces]] in which [[higher geometry]] makes sense, in particular [[higher differential geometry]]. See also at _[[motivation for cohesive toposes]]_ for a non-technical discussion.

Technically, it is an $(\infty,1)$-topos whose [[global section]] [[(∞,1)-geometric morphism]] $(Disc \dashv \Gamma): \mathbf{H} \stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\longrightarrow}} $ [[∞Grpd]] admits a further [[left adjoint|left]] [[adjoint (∞,1)-functor]] $\Pi$ and a further right adjoint $coDisc$: 

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv coDisc) : \mathbf{H} \to \infty Grpd
$$ 

with $Disc$ and $coDisc$ both [[full and faithful (∞,1)-functor]]s and such that $\Pi$ moreover preserves finite [[(∞,1)-limit|(∞,1)-product]]s. (For a notion of cohesion _relative_ to a general base, see Remark \ref{relative}.)

Here

1. the existence of $coDisc$ induces a sub-[[(∞,1)-quasitopos]] $Conc(\mathbf{H}) \hookrightarrow \mathbf{H}$ of _[[concrete (∞,1)-sheaf|concrete objects]]_ that behave like [[∞-groupoid]]s _equipped with extra cohesive structure_ , such as with [[topology|continuous structure]], [[smooth structure]], etc.

1. the existence of $\Pi$ induces a notion of [[geometric homotopy groups in an (∞,1)-topos|geometric]] [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|fundamental ∞-groupoid]], hence under $|-| : \infty Grpd \simeq $ [[Top]] of [[geometric realization]] $|\Pi(-)|$ of objects in $\mathbf{H}$.

The functor $\Gamma$ itself may be thought of as sending a cohesive [[∞-groupoid]] $X$ to its underlying bare $\infty$-groupoid $\Gamma(X)$. This is $X$ with all _cohesion forgotten_ (for instance with the continuous or the smooth structure forgotten).

Conversely, $Disc$ and $CoDisc$ send an $\infty$-groupoid $A$ either to the [[discrete space|discrete ∞-groupoid]] $Disc(A)$ with _discrete_ cohesive structure (for instance with [[discrete topology]]) or to the [[codiscrete space|codiscrete ∞-groupoid]] $Codisc(A)$ with the _codiscrete_ cohesive structure (for instance with [[codiscrete topology]]). 

This kind of [[adjoint quadruple]], directly analogous to the structure introduced by [[William Lawvere]] for [[cohesive toposes]], induces three [[adjoint modalities]] which in turn are adjoint to each other, to yield the adjoint string [[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]] $\int \dashv \flat \dashv \sharp$, which may be thought of as expressing "continuum" and "quantity" in the sense of [[Georg Hegel]]'s _[[Science of Logic]]_ (as explained in detail there.)

The existence of such an [[adjoint quadruple]] of adjoint $(\infty,1)$-functors alone implies a rich [[internalization|internal]] [[higher geometry]] in $\mathbf{H}$ that comes with its internal notion of [[Galois theory]], [[Lie theory]], [[differential cohomology]], [[Chern-Weil theory]]. 

Examples of cohesive $(\infty,1)$-toposes include

* the $(\infty,1)$-topos $\mathbf{H} = $[[Disc∞Grpd]] of [[discrete ∞-groupoid]]s; 

* the $(\infty,1)$-topos $\mathbf{H} = $ [[ETop∞Grpd]] of [[Euclidean-topological ∞-groupoids]];

* the $(\infty,1)$-topos $\mathbf{H} = $ [[Smooth∞Grpd]] of [[smooth ∞-groupoids]]; 

* the $(\infty,1)$-topos $\mathbf{H} = $ [[SynthDiff∞Grpd]] of [[formal smooth ∞-groupoids]];

* the $(\infty,1)$-topos $\mathbf{H} = $ [[Super∞Grpd]] of [[super ∞-groupoids]];

* the $(\infty,1)$-topos $\mathbf{H} = $ [[SmoothSuper∞Grpd]] of [[smooth super ∞-groupoids]].

In [[ETop∞Grpd]] and those contexts containing it, the internal notions of  [[geometric realization]], [[geometric homotopy groups in an (infinity,1)-topos|geometric homotopy]] and [[Galois theory]] subsume the usual ones (over well-behaved topological spaces). In [[Smooth∞Grpd]] also the notions of [[Lie theory]], [[differential cohomology]] and [[Chern-Weil theory]] subsume the usual ones. In [[SynthDiff∞Grpd]] the internal notion of [[Lie algebra]] and [[Lie algebroid]] subsumes the traditional one --- and generalizes them to higher smooth geometry.


## Definition


We state the definition in several equivalent ways.

1. [externally](#ExternalDefinition) in the ambient context;

1. [internally](#InternalDefinition) to the cohesive $(\infty,1)$-topos itselfs;

1. internally and [formulated in homotopy type theory](#DefinitionInHomotopyTypeTheory)


### Externally
 {#ExternalDefinition}

The definition is the immediate analog of the definition of a [[cohesive topos]].


+-- {: .num_defn #CohesiveInfinTopos}
###### Definition

An [[(∞,1)-topos]] $\mathbf{H}$ is **cohesive** if

1. it is a [[strongly ∞-connected (∞,1)-topos]];

1. it is a [[local (∞,1)-topos]].


=--

+-- {: .num_remark #relative}
###### Remark


As always in [[topos theory]] and [[higher topos theory]], such definitions can be made sense of over any _base_ . Here: over any [[base (∞,1)-topos]]. For instance, it has been proposed that [[condensed mathematics]] be viewed with respect to cohesion over the base, $Sh_\infty(ProFinSet)$, $\infty$-sheaves over the [[pro-étale site]] of a point. Similarly [[differential algebraic K-theory]] may be understood via cohesion over a base of ∞-stacks over a site of arithmetic schemes (see there).

Over the canonical base [[∞Grpd]] of [[∞-groupoid]]s, the definition of a cohesive $(\infty,1)$-topos is equivalently the following:

the [[global section]] [[(∞,1)-geometric morphism]] $\Gamma : \mathbf{H} \to \infty Grpd$ lifts to an [[adjoint quadruple]] of [[adjoint (∞,1)-functor]]s
   
$$
  (\Pi \dashv Disc \dashv \Gamma \dashv coDisc) : 
  \mathbf{H}
   \stackrel{\stackrel{\overset{\Pi}{\longrightarrow}}{\overset{Disc}{\leftarrow}}}{\stackrel{\underset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}
  \infty Grpd
  \;
$$

where $\Pi$ preserves [[finite limit|finite]] [[(∞,1)-product]]s.

Often we will tacitly assume to work over [[∞Grpd]]. But most statements and constructions have straightforward generalizations to arbitrary bases.
In particular, below in the [internal definition](#InternalDefinition) of cohesion, it takes more to fix the base topos than to leave it arbitrary.

Every [[adjoint quadruple]] induces an [[adjoint triple]] of endofunctors. 

$$
  (
   \mathbf{\Pi}
   \dashv 
   \mathbf{\flat}
   \dashv 
   \mathbf{#}
  )
  :
  \mathbf{H}
    \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{\Disc}{\leftarrow}}{\underset{\Gamma}{\longrightarrow}}}
  \infty Grpd
   \stackrel{\overset{Disc}{\longrightarrow}}{\stackrel{\overset{\Gamma}{\leftarrow}}{\underset{coDisc}{\longrightarrow}}}
  \mathbf{H}
  \,.
$$

Here "$\mathbf{\flat}$" is meant to be pronounced "flat". The interpretation of these three functors is discussed in detail at _[[cohesive (∞,1)-topos -- structures]]_.

=--



Sometimes it is desireable to add further axioms, such as the following.

+-- {: .num_defn #PiecesHavePoints}
###### Definition

We say that **pieces have points** for an object
$X$ in a cohesive $(\infty,1)$-topos $\mathbf{H}$ 
if the [[points-to-pieces transform]]

$$
  \Gamma X \to \Gamma Disc \Pi X \simeq \Pi X
$$ 

is an [[effective epimorphism in an (∞,1)-category]], equivalently (as discussed there) such that this is an [[epimorphism]] on [[connected]] components.


=--

Here the first morphismism is the image under $\Gamma$ of the 
$(Disc \dashv \Gamma)$-[[unit of an adjunction|unit]] and the second is an inverse of the $(\Pi \dashv Disc)$-counit (which is invertible because $Disc$ is [[full and faithful (∞,1)-functor|full and faithful]] in a [[local (∞,1)-topos]].)

+-- {: .num_defn #DiscreteObjectsAreConcrete}
###### Definition

We say **discrete objects are concrete** in $\mathbf{H}$ if for all
$S \in $[[∞Grpd]] the morphism

$$
  Disc S \to coDisc \Gamma Disc S \stackrel{\simeq}{\longrightarrow} coDisc S
$$

induces [[monomorphism]]s on all [[categorical homotopy groups in an (infinity,1)-topos|homotopy sheaves]].

=--

The following extra condition ensures that the [[shape modality]] is explicitly given by a geometric [[path ∞-groupoid]] construction.

+-- {: .num_defn #A1ExhibitingCohesion}
###### Definition

Given a cohesive $\infty$-topos $\mathbf{H}$ and an object $\mathbb{A}^1 \in \mathbf{H}$, we say that $\mathbb{A}^1$ _exhibits the cohesion_  if the [[shape modality]] $\Pi$ is equivalent to "[[A1-homotopy theory|A1-localization]]" $L_{\mathbb{A}^1}$, hence to [[localization of an (∞,1)-category|localization]] of $\mathbf{H}$ at the class of [[projection]] morphisms of the form $(-)\times \mathbb{A}^1 \longrightarrow (-)$, i.e. if

$$
  \Pi \simeq L_{\mathbb{A}^1}
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

In the example of [[smooth ∞-groupoid|smooth cohesion]] and its variants such as [[Euclidean topological infinity-groupoid|Euclidean topological cohesion]], the standard [[real line]] $\mathbb{A}^1 = \mathbb{R}^1$ exhibits cohesion in the sense of def. \ref{A1ExhibitingCohesion} (by [this discussion](cohesive+%28infinity%2C1%29-topos+--+structures#RealLineIsTheContinuum)). Therefore one might also say that if an object $\mathbb{A}^1$ in a cohesive $\infty$-topos exhibits the cohesion, then it plays the role of _the [[continuum]]_ in analogy of the traditional use of this term in geometry. See also at _[continuum -- In cohesive homotopy theory](continuum#InCohesiveHomotopyTypeTheory)_.

=--

Another extra axiom is (see at _[[Aufhebung]]_ for more):

+-- {: .num_defn #AufhebungOfBecoming}
###### Definition

Say that a cohesive $\infty$-topos, def. \ref{CohesiveInfinTopos}, has _[[Aufhebung]] of [[becoming]]_ if the [[sharp modality]]  preserves the [[initial object]]

$$
  \sharp \emptyset \simeq \emptyset
  \,.
$$

=--



### Internally
 {#InternalDefinition}

We reformulate the [above axioms](#ExternalDefinition) for a cohesive $(\infty,1)$-topos without references to functors _on_ it, and instead entirely in terms of structures _in_ it.


+-- {: .num_lemma #ReflectiveEmbeddingInternally}
###### Lemma

A [[full sub-(∞,1)-category]] $\mathbf{B} \hookrightarrow \mathbf{H}$ is

* [[reflective sub-(∞,1)-category|reflectively embedded]] precisely if for every [[object]] $X \in \mathbf{H}$ there is a [[morphism]] 

  $$
    loc_X : X \to L X
  $$ 

  (the [[unit of an adjunction|unit]]) with $L X \in \mathbf{B} \hookrightarrow \mathbf{H}$, such that for all $Y \in \mathbf{B} \hookrightarrow \mathbf{H}$ the value of the [[(∞,1)-categorical hom-space]]-functor 

  $$
    \mathbf{H}(loc_X, Y) : 
    \mathbf{H}(L X, Y)
    \stackrel{\simeq}{\longrightarrow}
    \mathbf{H}(X, Y)
  $$

  is an [[equivalence in an (∞,1)-category|equivalence]] (of [[∞-groupoid]]s). 

* coreflectively embedded precisely if for every [[object]] $Y \in \mathbf{H}$ there is a [[morphism]] 

  $$
    coloc_Y : R Y \to Y
  $$ 

  (the [[unit of an adjunction|counit]]) with $R Y \in \mathbf{B} \hookrightarrow \mathbf{H}$ such that for all $X \in \mathbf{B} \hookrightarrow \mathbf{H}$ the value of the [[(∞,1)-categorical hom-space]]-functor 

  $$
    \mathbf{H}(X, coloc_Y) : 
    \mathbf{H}(X, R Y)
    \stackrel{\simeq}{\to}
    \mathbf{H}(X, Y)
  $$

  is an [[equivalence in an (∞,1)-category|equivalence]] (of [[∞-groupoid]]s). 


=--

This is proven [here](http://ncatlab.org/nlab/show/reflective+sub-%28infinity,1%29-category#CharacterizationOfReflectors).

+-- {: .num_lemma}
###### Lemma

A reflective embedding 

$$
  coDisc : \mathbf{B}_{cod} \stackrel{\overset{\tilde \Gamma}{\leftarrow}}{\underset{coDisc}{\hookrightarrow}} \mathbf{H}
$$

and a coreflective embedding 

$$
  Disc : \mathbf{B}_{disc} \stackrel{\overset{Disc}{\hookrightarrow}}{\underset{\Gamma}{\leftarrow}} \mathbf{H}
$$

fit into a single [[adjoint triple]]

$$
  \mathbf{H}
    \stackrel{
      \overset{Disc}{\hookleftarrow}
    }{
     \stackrel{  
       \overset{\Gamma}{\to}
     }{
       \underset{coDisc}{\hookleftarrow}
     }
   }
  \mathbf{B}
$$

(hence there is an equivalence $\mathbf{B}_{disc} \simeq \mathbf{B}_{cod}$ that moreover makes the coreflector $\tilde\Gamma$ of $Disc$ coincide with the reflector $\Gamma$ of $coDisc$) precisely if for the [[unit of an adjunction|unit]] and counit given by  lemma \ref{ReflectiveEmbeddingInternally} we have that the morphisms on the left of

\[
  \label{FirstNaturalEquivalence}
  coDisc \tilde \Gamma (Disc \Gamma X \to X)
  \;
  =:
  \;
  (coDisc \tilde \Gamma Disc \Gamma X

   \stackrel{\simeq}{\to}
  coDisc \tilde \Gamma X)
\]

\[ 
  \label{SecondNaturalEquivalence}
  Disc \Gamma (X \to coDisc \tilde \Gamma X)
  \;\;
   =:
  \;\;
  (
    Disc \Gamma X 
     \stackrel{\simeq}{\to}
    Disc \Gamma coDisc \tilde \Gamma
  )
\]

are (natural) [[equivalence in an (∞,1)-category|equivalences]] for all objects $X \in \mathbf{H}$, as indicated on the right.

=--

+-- {: .proof}
###### Proof

It is clear that if we have an [[adjoint triple]], then (eq:FirstNaturalEquivalence) and (eq:SecondNaturalEquivalence) are implied. We discuss now the converse.

First notice that the two embeddings always combine into an adjunction of the form

$$
  \mathbf{B}_{disc}
   \stackrel{\overset{Disc}{\hookrightarrow}}{\underset{\Gamma}{\leftarrow}}
  \mathbf{H}
   \stackrel{\overset{\tilde \Gamma}{\to}}{\underset{coDisc}{\hookleftarrow}}
  \mathbf{B}_{cod}    
  \,.
$$

The natural equivalence (eq:FirstNaturalEquivalence) applied to a codiscrete object $X := coDisc A$ gives that $coDisc$ of the counit of this composite adjunction is an equivalence 

$$
  coDisc \tilde \Gamma Disc \Gamma coDisc A
    \stackrel{\simeq}{\to}
  coDisc \tilde \Gamma coDisc A
    \stackrel{\simeq}{\to}
  coDisc A
$$

for all $A$, and since $coDisc$ is [[full and faithful (infinity,1)-functor|full and faithful]], so is the composite counit 

$$
  \tilde \Gamma Disc \Gamma coDisc A
    \stackrel{\simeq}{\to}
  \tilde \Gamma coDisc A
    \stackrel{\simeq}{\to}
  A  
$$

itself. Analogously, (eq:SecondNaturalEquivalence) implies that the unit of the composite adjunction is an equivalence. Therefore (eq:FirstNaturalEquivalence) and (eq:SecondNaturalEquivalence) together imply that the adjunction itself exhibits an [[equivalence of (∞,1)-categories|equivalence]] $\mathbf{B}_{disc} \simeq \mathbf{B}_{cod}$.

Using this we then find for each $X \in \mathbf{H}$ a composite natural equivalence

$$
  Disc \tilde \Gamma X
   \stackrel{\simeq}{\to}
  Disc \Gamma coDisc \tilde \Gamma X
   \stackrel{\simeq}{\to}
  Disc \Gamma X
$$

where the first morphism uses the above equivalence on the codiscrete object $\tilde \Gamma X$ and the second is a choice of natural inverse of (eq:SecondNaturalEquivalence).

Since $Disc$ is full and faithful, this mean that we have equivalences

$$
  \tilde \Gamma X 
   \simeq 
  \Gamma X
$$

natural in $X$, hence that $\tilde \Gamma \simeq \Gamma$.

=--

+-- {: .num_remark #AdjunctionIsoFromInternalReflectionCoreflection}
###### Remark

In the above situation, the defining [[adjoint (∞,1)-functor|adjunction equivalence]]

$$
  \mathbf{H}(\mathbf{\Pi} X , A)
    \simeq 
  \mathbf{H}(X, \flat A) 
$$

exhibiting $(\mathbf{\Pi} \dashv \flat)$
is given by the composite of natural equivalences


$$
    \mathbf{H}(\mathbf{\Pi}X, A)
     \underoverset{\simeq}{\mathbf{H}(\mathbf{\Pi}X, coloc_A)^{-1}}{\to}
     \mathbf{H}(\mathbf{\Pi} X, \flat A)
   \underoverset{\simeq}{\mathbf{H}(loc_X, \flat A)}{\to}
    \mathbf{H}(X, \flat A) 
$$

from lemma \ref{ReflectiveEmbeddingInternally}, using that both $\mathbf{\Pi} X$ as well as $\flat A$ are discrete.

=--


Using these lemmas we can now restate cohesiveness internally.

+-- {: .num_corollary}
###### Corollary

For $Disc : \mathbf{B} \hookrightarrow \mathbf{H}$ a [[sub-(∞,1)-category]], 
the inclusion extends to an [[adjoint quadruple]] of the form

$$
  \mathbf{H}
    \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{Disc}{\hookleftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{coDisc}{\hookleftarrow}}}}
  \mathbf{B}
$$

precisely if there exists for each object $X \in \mathbf{H}$

1. a morphism $X \to \mathbf{\Pi}(X)$ with $\mathbf{\Pi}(X) \in \mathbf{B} \stackrel{Disc}{\hookrightarrow} \mathbf{H}$;

1. a morphism $\mathbf{\flat} X \to X$ with $\mathbf{\flat} X \in \mathbf{B} \stackrel{Disc}{\hookrightarrow} \mathbf{H}$;

1. a morphism $X \to #X $ with $# X \in \mathbf{B} \stackrel{coDisc}{\hookrightarrow} \mathbf{H}$

such that for all $Y \in \mathbf{B} \stackrel{Disc}{\hookrightarrow} \mathbf{H}$ and $\tilde Y \in \mathbf{B} \stackrel{coDisc}{\hookrightarrow} \mathbf{H}$ the induced morphisms

1. $\mathbf{H}(\mathbf{\Pi}X , Y) \stackrel{\simeq}{\to} \mathbf{H}(X,Y)$;

1. $\mathbf{H}(Y, \mathbf{\flat}X) \stackrel{\simeq}{\to} \mathbf{H}(Y,X)$;

1. $\mathbf{H}(# X , \tilde Y) \stackrel{\simeq}{\to} \mathbf{H}(X,\tilde Y)$;

1. $# (\flat X \to X)$;

1. $\flat (X \to # X)$

are [[equivalence in an (infinity,1)-category|equivalences]] (the first three of [[∞-groupoids]] the last two in $\mathbf{H}$).

Moreover, if $\mathbf{H}$ is a [[cartesian closed category]], then $\Pi$ preserves finite products precisely if the $Disc$-inclusion is an [[exponential ideal]].

=--

The last statement follows from the $(\infty,1)$-category analog of the discussion [here](http://ncatlab.org/nlab/show/reflective+subcategory#ReflectiveSubcategoriesOfCartesianClosedCategotries).


### In homotopy type theory
  {#DefinitionInHomotopyTypeTheory}

The axioms for cohesion, in the [internal version](#InternalDefinition), can be formulated in [[homotopy type theory]], the [[internal language of an (∞,1)-topos]].

The corresponging [[Coq]]-[[HoTT]] code is in ([Shulman](#Shulman)).

For more see _[[cohesive homotopy type theory]]_.


## Properties

We discuss basic properties implied by the axioms for cohesive $(\infty,1)$-toposes in 

* [As a point-like space](#AsAPointLikeSpace);

* [General](#General).

* [Over arbitrary bases](#OverArbitraryBases)

Then we discuss presentations over special [[site]]s in  

* [Over an ∞-cohesive site](#OverAnInfinityCohesiveSite).

### As a point-like space
 {#AsAPointLikeSpace}


+-- {: .num_prop #PointLike}
###### Proposition

A nontrivial cohesive $(\infty,1)$-topos

1. has the [[shape of an (∞,1)-topos|shape]] of the point;

1. has [[homotopy dimension]] 0;

1. has [[cohomology dimension]] 0.
 

=--

+-- {: .proof}
###### Proof

The first holds for every [[∞-connected (∞,1)-topos]], see there.

The second holds for every [[local (∞,1)-topos]], see there.

The third follows from the second, see [[homotopy dimension]].

=--

+-- {: .num_remark #ThickenedPoint}
###### Remark

This says that a cohesive $(\infty,1)$-topos $\mathbf{H}$ is, when itself regarded as a [[little topos]], a generalized [[space]], a _thickened point_ . We may think of it as the standard [[point]] equipped with a _cohesive neighbourhood_ .

In this sense every space $X$ _modeled on_ the cohesive structure defined by $\mathbf{H}$ is an [[étale space]] over $X$: its [[petit topos|petit]] $(\infty,1)$-topos $\mathbf{H}/X$ sits by a [[locally homeomorphic geometric morphism]] over $\mathbf{H}$

$$
  \mathbf{H}/X \stackrel{local\;homeo}{\to} \mathbf{H}
  \,.
$$


=--


### Over an $\infty$-cohesive site
  {#OverAnInfinityCohesiveSite}

We discuss a [[presentable (∞,1)-category|presentation]] of classes of cohesive [[(∞,1)-topos]]es by a [[model structure on simplicial presheaves]] over a suitable [[site]].


+-- {: .num_prop #SimplicialPresheavesOverInfinityCohesviveSite}
###### Proposition

For $C$ an [[∞-cohesive site]] the [[(∞,1)-category of (∞,1)-sheaves]] $(\infty,1)Sh(C)$ over $C$ is a cohesive $(\infty,1)$-topos satisfying the two axioms _[pieces have points](#PiecesHavePoints)_ and _[discrete objects are concrete](#DiscreteObjectsAreConcrete)_ .

=--

The detailed discussion is at [[∞-cohesive site]].


### General
 {#General}

+-- {: .num_prop #HypercompleteProperty}
###### Proposition

Every cohesive $(\infty,1)$-topos over [[∞Grpd]] is a 
[[hypercomplete (∞,1)-topos]].

=--


+-- {: .proof}
###### Proof

By the [above proposition](#PointLike) it has finite 
[[homotopy dimension]]. This implies hypercompeteness. See there.

=--

+-- {: .num_prop #Cohesive1Topos}
###### Proposition

For $\mathbf{H}$ a cohesive $(\infty,1)$-topos, the [[(n,1)-topos|(1,1)-topos]] $\tau_{\leq 1-1} \mathbf{H}$ of 0-[[truncated]] objects is a [[cohesive topos]].

=--

+-- {: .num_prop #PiPreservesPullbacksOverDiscretes}
###### Proposition

For a cohesive $(\infty,1)$-topos $(\Pi \dashv Disc \dashv \Gamma \dashv coDisc) : \mathbf{H} \to \infty Grpd$ over an [[∞-cohesive site]], the functor $\Pi$ preserves [[(∞,1)-pullbacks]] over [[discrete objects]].

=--

We first consider a lemma. Notice that for $A \in \infty Grpd$ the [[(∞,1)-Grothendieck construction]] gives an [[equivalence of (∞,1)-categories]]

$$
  \infty Grpd_{/A} \simeq Func(A, \infty Grpd)
$$

from the [[over (∞,1)-category]] of $\infty Grpd$ over $A$ to the [[(∞,1)-functor (∞,1)-category]] from $A$ to $\infty Grpd$.


+-- {: .num_lemma #GrothendieckConstrInCohesivefinityTopos}
###### Lemma

For $\mathbf{H}$ a cohesive $(\infty,1)$-topos over
an [[∞-cohesive site]] and for $A \in \infty Grpd$, we
have an [[equivalence of (∞,1)-categories]]

$$
  \mathbf{H}_{/ Disc A} \simeq Func(A, \mathbf{H})
  \,.
$$

=--

+-- {: .proof}
###### Proof


We establish this via a [[presentable (infinity,1)-category|presentation]] of 
$\mathbf{H}$ by a [[model structure on simplicial presheaves]]. 

Let $C$ be an [[∞-cohesive site]] of definition for $\mathbf{H}$. Then by the discussion there we have

$$
  \mathbf{H} \simeq ([C^{op}, sSet]_{proj,loc})^\circ
  \,.
$$

Moreover, picking a [[Kan complex]] presentation for $A$, which we shall denote by the same symbol, we have that the constant simplicial presheaf $const A \in [C^{op}, sSet]_{proj, loc}$ is fibrant. Therefore by [this proposition](http://ncatlab.org/nlab/show/model+structure+on+an+over+category#PresentationOfSliceInfinityCat) the induced [[model structure on an overcategory]] on $[C^{op}, sSet]/const A$ presents the given [[over (∞,1)-category]]

$$
  \mathbf{H}_{/ Disc A}
  \simeq
  \left(
   \left([C^{op}, sSet]/const A\right)_{(proj,loc)/const A}
  \right)^\circ
  \,.
$$

Now observe that we have an ordinary [[equivalence of categories]]


$$
  [C^{op}, sSet]/const A 
   \simeq
  [C^op, sSet/A]
$$

under which the model structure becomes that of the local projective [[model structure on functors]] with values in the model structure $(sSet/A)_{Quillen/A}$ that presents $\infty Grpd_{/ A}$.

Let then $sSet^+/A$ denote the [[model structure for left fibrations]]. By the discussion there, this also presents $\infty Grpd_{/ A}$. Hence by [this proposition](http://ncatlab.org/nlab/show/model+structure+on+functors#PresentationOfInfinityFunctors) we have an [[equivalence of (∞,1)-categories]]

$$
  \begin{aligned}
   \mathbf{H}_{Disc A}
   & \simeq
  \left(
    [C^{op}, sSet/A]_{proj,loc}
  \right)^\circ
  \\
  & \simeq
  \left(
   [C^{op}, sSet^+/A]_{proj,loc}
  \right)^\circ
  \end{aligned}
  \,.
$$

This allows now to apply [this presentation](http://ncatlab.org/nlab/show/model%20structure%20for%20left%20fibrations#GrothendieckConstruction) of the [[(∞,1)-Grothendieck construction]] to find

$$
  \cdots \simeq
  \left(
   [C^{op}, [w(A), sSet_{Quillen}]_{proj}]_{proj,loc}
  \right)^\circ
  \,,  
$$

where $w(A)$ is the [[simplicially enriched category]] corresponding to $A$ (as discussed at _[[relation between quasi-categories and simplicial categories]]_ ) and $[w(A), sSet_{Quillen}]_{proj}$ is the global [[model structure on sSet-enriched presheaves]].

Then using the [[cartesian closed category|cartesian closure]] of the category of simplicial presheaves (which is a [[topos]]) inside the $(-)^\circ$ we have

$$
  \cdots
  \simeq
  \left(
   [w(A), [C^{op}, sSet_{Quillen}]_{proj,loc}]_{proj}
  \right)^\circ
  \,.
$$

Finally this implies the claim using [this proposition](http://ncatlab.org/nlab/show/%28infinity%2C1%29-category+of+%28infinity%2C1%29-functors#PresentationByModelStructuresOnFunctors).

=--


With this lemma we can now give the proof
of prop. \ref{PiPreservesPullbacksOverDiscretes}.

+-- {: .proof}
###### Proof

By the discussion at [adjoint (∞,1)-functors on slices](http://ncatlab.org/nlab/show/adjoint+%28infinity,1%29-functor#OnSlices) we have that $(\Pi \dashv Disc)$ induces an adjoint pair

$$
  (\Pi/Disc A \dashv Disc / Disc A)
  : 
  \mathbf{H}_{Disc A}
  \to 
  \infty Grpd_{/A}

  \,.
$$

Under the equivalence from lemma \ref{GrothendieckConstrInCohesivefinityTopos} the functor $\Pi/Disc A$ maps to

$$
  Func(A, \Pi) : 
  Func(A, \mathbf{H}) \to 
  Func(A, \infty Grpd)
  \,.
$$

Since [[products]] of $(\infty,1)$-functor $(\infty,1)$-categories are computed objectwise, and since $\Pi$ preserves finite products by the axioms of cohesion, also $Func(A, \Pi)$ preserves finite products, and hence so does $\Pi/Disc A$. But products in the slice over $Disc A$ are [[(∞,1)-pullbacks]] over $Disc A$. So this proves the claim.

=--

### Base of discrete and codiscrete objects
 {#OverArbitraryBases}

In the [internal definition](#InternalDefinition) the base of discrete/codiscrete objects is not explicitly axiomatized to be an [[(∞,1)-topos]] itself (the [[base (∞,1)-topos]]), but this is implied by the axioms. We deduce that and related properties in stages.

In the following, let $\mathbf{H}$ be an [[(∞,1)-topos]] equipped with an [[adjoint quadruple]] of functors to an [[(∞,1)-category]] $\mathbf{B}$ --  the _base of cohesion_, where $Disc$ and $coDisc$ are full and faithful.

+-- {: .num_prop #LimitsInBase}
###### Proposition

The base $\mathbf{B}$ of cohesion has all [[(∞,1)-limits]] and [[(∞,1)-colimits]].

=--

+-- {: .proof}

###### Proof

This is a general property of a reflectively and coreflectively embedded subcategory. The limits are computed by computing them in $\mathbf{H}$ and then applying $\Gamma$ and the colimits are computed by computing them in $\mathbf{H}$ and then applying $\Pi$. For $X : I \to \mathbf{B}$ any [[diagram]] we have

$$
  \begin{aligned}
    \Gamma \lim_{\leftarrow_i} Disc X_i
    & \simeq
    \lim_{\leftarrow_i} \Gamma Disc X_i 
    \\
    & \simeq 
    \lim_{\leftarrow_i}  X_i 
  \end{aligned}
$$

$$
  \begin{aligned}
    \Pi \lim_{\to_i} Disc X_i
    & \simeq
    \lim_{\leftarrow_i} \Pi Disc X_i 
    \\
    & \simeq 
    \lim_{\leftarrow_i}  X_i 
  \end{aligned}
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

Since $Disc$, being both a [[left adjoint]] as well as a [[right adjoint]] preserves limits and colimits, it follows that a (co)limit of discrete objects computed in $\mathbf{H}$ is itself again discrete and is the image under $Disc$ of the coresponding (co)limit computed in $\mathbf{B}$.

=--

+-- {: .num_example }
###### Example

Since [[loop space objects]] are [[(∞,1)-limits]] it follows that the loop space object of any discrete object is itself again a discrete object. 

=--

We have also the following stronger statement.

+-- {: .num_prop}
###### Proposition

The base of cohesion $\mathbf{B}$ is a [[presentable (∞,1)-category]] and in fact an [[(∞,1)-topos]] itself.

=--

+-- {: .proof}
###### Proof

By one of the equivalent characterizations of [[presentable (∞,1)-categories]] these are [[reflective sub-(∞,1)-categories]] of [[(∞,1)-categories of (∞,1)-presheaves]] where the embedding is by an [[accessible (∞,1)-functor]].

Since $\mathbf{H}$ is itself accessibly and reflectively embedded into the presheaves $PSh(C)$ on a [[(∞,1)-site]] of definition, we have a composite reflective inclusions

$$
  \mathbf{B}
  \stackrel{Disc}{\hookrightarrow}
  \mathbf{H}
  \hookrightarrow
  PSh(C)
  \,.
$$

Since $Disc$ even preserves all [[(∞,1)-colimits]], it is in particular an [[accessible (∞,1)-functor]], hence so is the above composite.

Finally, since $\Gamma$ preserves all [[(∞,1)-limits]], hence in particular the [[finite limits]], $(\Gamma, coDisc)$ is a [[geometric embedding]] that exhibits an sub-[[(∞,1)-topos]].

=--

Notice that the reflection $(\Pi \dashv Disc)$ does not in general constitute a [[geometric embedding]], since $\Pi$ is only required to preserve finite products (and in interesting examples rarely preserves more limits than that).

The following statement and its proof about [[cohesive topos|cohesive 1-toposes]] should hold verbatim also for cohesive $(\infty,1)$-toposes.

+-- {: .num_prop }
###### Proposition

The [[reflective subcategories]] of discrete objects and of codiscrete objects are both [[exponential ideals]].

=--

+-- {: .proof}
###### Proof

By the discussion at [[exponential ideal]] a reflective subcategories of a [[cartesian closed category]] is an exponential ideal precisely if the [[reflector]] preserves [[products]]. For the codiscrete objects the reflector $\Gamma$ preserves even all [[limits]] and for the discrete objects the reflector $\Pi$ does so by assumotion of strong connectedness.

=--

### Factorization systems associated to $\mathbf{\Pi}$
 {#FactorizationSystemsForPi}

We discuss [[orthogonal factorization system in an (infinity,1)-category|orthogonal factorization systems]] in a cohesive $(\infty,1)$-topos that characterize or are characterized by the [[reflective sub-(infinity,1)-category|reflective subcategory]] of dicrete objects, with reflector $\mathbf{\Pi} : \mathbf{H} \stackrel{\Pi}{\to} \infty Grpd \stackrel{Disc}{\hookrightarrow} \mathbf{H}$.


+-- {: .num_defn #PiClosure}
###### Definition

For $f : X \to Y$ a morphism in $\mathbf{H}$, write $c_{\mathbf{\Pi}} f \to Y$ for the [[(∞,1)-pullback]] in

$$
  \array{
    c_{\mathbf{\Pi}} f &\to & \mathbf{\Pi} X
    \\
    \downarrow && \downarrow^{\mathrlap{\mathbf{\Pi} f}}
    \\
    Y &\to& \mathbf{\Pi} Y
  }
  \,,
$$

where the bottom morphism is the $(\Pi \dashv Disc)$-[[unit of an adjunction|unit]]. We say that $c_{\mathbf{\Pi}} f$ is the **$\mathbf{\Pi}$-closure** of $f$, and that $f$ is **$\mathbf{\Pi}$[[Pi-closed morphism|-closed]]** if $X \simeq c_{\mathbf{\Pi}} f$.

=--

+-- {: .num_prop #FactorizationPiEquivalencePiClosed}
###### Proposition

If $\mathbf{H}$ has an [[∞-cohesive site]] of definition, then
every morphism $f : X \to Y$ in $\mathbf{H}$ factors as 

$$
  \array{
     X &&\stackrel{f}{\to}&& Y
     \\
     & \searrow && \nearrow
     \\
     && c_{\mathbf{\Pi}}f 
  }
  \,,
$$

such that $X \to c_{\mathbf{\Pi}} f$ is a _$\mathbf{\Pi}$-equivalence_ in that it is inverted by $\mathbf{\Pi}$.

=--

+-- {: .proof}
###### Proof

The factorization is given by the naturality of $\mathbf{\Pi}$
and the universal property of the $(\infty,1)$-pullback 
in def. \ref{PiClosure}.

$$
  \array{
    X &\to & c_{\mathbf{\Pi}} f &\to & \mathbf{\Pi} X
    \\
    &{}_{\mathllap{f}}\searrow & \downarrow && \downarrow^{\mathrlap{\mathbf{\Pi} f}}
    \\
    && Y &\to& \mathbf{\Pi} Y
  }
  \,.
$$

Then by prop. \ref{PiPreservesPullbacksOverDiscretes} the functor
$\mathbf{\Pi}$ preserves the $(\infty,1)$-pullback over the
discrete object $\mathbf{\Pi}Y$ and since $\mathbf{\Pi}(X \to \mathbf{\Pi}X)$
is an equivalence, it follows that $\mathbf{\Pi}(X \to c_{\mathbf{\Pi}f})$
is an equivalence.

=--

+-- {: .num_prop #PiEquivalencePiClosedFactorizationSystem}
###### Proposition

The pair of classes

$$
  (\mathbf{\Pi}-equivalences, \mathbf{\Pi}-closed morphisms)
$$

is an [[orthogonal factorization system in an (infinity,1)-category|orthogonal factorization system]] in $\mathbf{H}$.

=--

+-- {: .proof}
###### Proof

This follows by the general reasoning discussed at [[reflective factorization system]]:

By prop. \ref{FactorizationPiEquivalencePiClosed} we have the required factorization. It remains to check the orthogonality. 

So let 

$$
  \array{
     A &\to& X 
     \\
     \downarrow && \downarrow 
     \\
     B &\to& Y
  }
$$

be a square diagram in $\mathbf{H}$ where the left morphism is a $\mathbf{\Pi}$-equivalence and the right morphism is $\mathbf{\Pi}$-closed. Then by assumption there is a pullback square on the right in 

$$
  \array{
     A &\to& X &\to& \mathbf{\Pi}X 
     \\
     \downarrow && \downarrow  && \downarrow
     \\
     B &\to& Y &\to& \mathbf{\Pi}Y
     \,.
  }
  \,.
$$

By naturality of the [[unit of an adjunction|adjunction unit]], the total rectangle is equivalent to

$$
  \array{
    A &\to& \mathbf{\Pi} A &\to & \mathbf{\Pi} Y
    \\
    \downarrow && \downarrow^{\mathrlap{\simeq}} && \downarrow
    \\
    B &\to& \mathbf{\Pi} B &\to& \mathbf{\Pi}X
  }
  \,.
$$

Here by assumption the middle morphism is an equivalence.
Therefore there is an essentially unique lift in the square on the right and hence a lift in the total square. 
Again by the universality of the adjunction, any such lift factors through $\mathbf{\Pi} B$ and hence also this lift is essentially unique.

Finally by universality of the pullback, this induces an essentially unique lift $\sigma$ in

$$
  \array{
     A &\to& X &\to& \mathbf{\Pi}X 
     \\
     \downarrow &{}^{\mathllap{\sigma}}\nearrow& \downarrow  && \downarrow
     \\
     B &\to& Y &\to& \mathbf{\Pi}Y
     \,.
  }
  \,.
$$


=--

+-- {: .num_prop }
###### Observation

For $f : X \to Y$ a 
$\mathbf{\Pi}$-closed morphism and 
$y : * \to Y$ a [[global element]], the [[homotopy fiber]]
$X_y := y^* X$ is a discrete object.

=--

+-- {: .proof}
###### Proof

By the def. \ref{PiClosure} and the [[pasting law]] we have that $y^* X$ is equivalently the $\infty$-pullback in

$$
  \array{
    y^* X &\to& &\to& \mathbf{\Pi} X
    \\
    \downarrow && && \downarrow
    \\
    * &\stackrel{y}{\to}& Y &\stackrel{}{\to}& \mathbf{\Pi}Y
  }
  \,.
$$

Since the [[terminal object in an (infinity,1)-category|terminal object]] is discrete, and since the [[right adjoint]] $Disc$ preserves $\infty$-pullbacks, this exhibits $y^* X$ as the image under $Disc$ of an $\infty$-pullback of $\infty$-groupoids.

=--



## Structures in a cohesive $(\infty,1)$-topos 
  {#Structures}

A cohesive $(\infty,1)$-topos is a general context for [[higher geometry]] with good [[cohomology]] and [[homotopy]] properties. We list fundamental structures and constructions that exist in every cohesvive $(\infty,1)$-topos.

This section is at 

* [[cohesive (∞,1)-topos -- structures]]

## Types of cohesion

### Infinitesimal cohesion

* [[infinitesimal cohesion]]

###  Differential cohesion   
  {#DifferentialCohesion}

We discuss [[extra structure]] on a cohesive $(\infty,1)$-topos
that encodes a refinement of the corresponding notion of cohesion to 
_infinitesimal cohesion_ . More precisely, we consider inclusions
$\mathbf{H} \hookrightarrow \mathbf{H}_{th}$ of cohesive 
$(\infty,1)$-toposes that exhibit the objects of $\mathbf{H}_{th}$
as infinitesimal cohesive neighbourhoods of objects in 
$\mathbf{H}$.

This section is at

* [[differential cohesive (∞,1)-topos]]

### Locally ringed cohesion

Every cohesive $(\infty,1)$-topos $\mathbf{H}$ equipped with 
[differential cohesion](#DifferentialCohesion) comes canonically equipped with a notion of [[formally étale morphism]]s (as discussed there). Combined with the canonical interpretation of $\mathbf{H}$ as the [[classifying topos]] of a [[theory]] of [[local algebra|local T-algebra]]s, this canonically induces a notion of [[locally algebra-ed topos|locally algebra-ed (∞,1)-toposes]] with cohesive structure, generalizing the notion of [[locally ringed space]]s and [[locally ringed topos]]es.

This section is at 

* [[cohesive (∞,1)-topos -- structure ∞-sheaves]].


## Examples of cohesive $\infty$-toposes
 {#Examples}

We list examples of cohesive $(\infty,1)$-toposes,
both specific ones as well as classes of examples constructed in a certain way.

### Cohesive diagram $(\infty,1)$-toposes

#### Cohesive diagrams in a cohesive $(\infty,1)$-topos
 {#CohesiveDiagramToposes}

+-- {: .num_prop}
###### Proposition

Let $\mathbf{H}$ be an cohesive $(\infty,1)$-topos.

Let $D$ be a  [[small category]] ([[diagram]]) with [[initial object]] $\bottom$ and [[terminal object]] $\top$, or else a [[presentable (∞,1)-category]]. Write

$$
  (\bottom \dashv p \dashv \top)
  :
  D \stackrel{\overset{\bottom}{\hookleftarrow}}{\stackrel{\overset{p}{\to}}{\underset{\top}{\hookleftarrow}}}
  *
$$

for the [[adjoint triple|triple]] of [[adjoint (∞,1)-functors]] given by including $\bottom$ and $\top$.

Then the [[(∞,1)-category of (∞,1)-functors|(∞,1)-functor category]] $\mathbf{H}^D$ is again a cohesive $(\infty,1)$-topos, exhibited by the [[adjoint quadruple]] which is the composite

$$
  \mathbf{H}^D
   \stackrel{\overset{\top^*}{\to}}{\stackrel{\overset{p^*}{\hookleftarrow}}{\stackrel{\overset{\bottom^*}{\to}}{\underset{\bottom_*}{\hookleftarrow}}}}
  \mathbf{H}
   \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{Disc}{\hookleftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{coDisc}{\hookleftarrow}}}}
  \infty Grpd
  \,,
$$

where the [[adjoint quadruple]] on the left is that induced under [[(∞,1)-Kan extension]] from $(\bottom \dashv p \dashv \top)$.

=--

+-- {: .proof}
###### Proof

By the discussion at [[(∞,1)-Kan extension]] each of the original three functors induces [adjoint triples $(\bottom_! \dashv \bottom^* \dashv \bottom_*)$ etc, as indicated. In particular $\top^*$ is a [[right adjoint]] and therefore preserves finite products (and all small [[(∞,1)-limits]], even). 

By the original adjunctions one finds that $\bottom_! \simeq p^*$ and  $p_! \simeq \top^*$, which implies the adjoint quadruple as indicated above by essential uniqueness of adjoints. 

Finally it is clear that $\top^* p^* \simeq Id$, which implies that $p^*$ is a [[full and faithful (∞,1)-functor]] (and hence so is $\bottom_*$).

=--

In particular we have

+-- {: .num_cor}
###### Corollary

For $\mathbf{H}$ a cohesive $(\infty,1)$-topos, also its [[arrow category|arrow (∞,1)-category]] $\mathbf{H}^{\Delta[1]}$ is cohesive.

=--

+-- {: .num_example #SierpinskiTopos}
###### Example

For $\mathbf{H} = $ [[∞Grpd]] ("discrete cohesion", see [below](#DiscreteInfinityGroupoids)) the corresponding cohesive $(\infty,1)$-topos $\infty Grpd^{\Delta[1]}$ is known as the _[[Sierpinski (∞,1)-topos]]_.

=--

#### Simplicial objects in a cohesive $(\infty,1)$-topos
 {#SimplicialObjctsInACohesiveTopos}

For $\mathbf{H}$ a cohesive $(\infty,1)$-topos its [[category of simplicial objects|(∞,1)-category of simplicial objects]] $\mathbf{H}^{\Delta^{op}}$ is cohesive over $\mathbf{H}$

$$
  \mathbf{H}^{\Delta^{op}}
  \stackrel{\Pi_I}{\stackrel{\longrightarrow}{\stackrel{\overset{Disc_I}{\longleftarrow}}{\stackrel{\overset{\Gamma_I}{\longrightarrow}}{\underset{coDisc_I}{\longleftarrow}}}}}
  \mathbf{H}
  \,.
$$

Here

* $\Pi_I$ sends a [[simplicial object]] to the [[homotopy colimit]] over its components, hence to its "[[geometric realization]]" as seen in $\mathbf{H}$.

* $\Gamma_I$ evaluates on the 0-simplex;

* $Disc_I$ sends an object in $\mathbf{H}$ to the simplicial object which is simplicially constant on $A$.

Hence cohesion of $\mathbf{H}^{\Delta^{op}}$ relative to $\mathbf{H}$ expresses the existence of a discrete and directed notion of path. 

The simplicial interval $\Delta^1 \in \mathbf{H}^{\Delta^{op}}$ (regarded under [[(∞,1)-Yoneda embedding]]) _exhibits the cohesion_ of $\mathbf{H}^{\Delta^{op}}$ over $\mathbf{H}$ in the sense of def. \ref{A1ExhibitingCohesion}, in that the relative [[shape modality]] $\Pi_I$ is equivalent to the "[[A1-homotopy theory|A1-localization]]" at $\mathbb{A}^1 = \Delta^1$

$$
  \Pi_I \simeq L_{\Delta^1}
  \,.
$$



Notice that there is an inclusion

$$
  Grpd(\mathbf{H})
  \hookrightarrow
  Cat(\mathbf{H})
  \hookrightarrow
  \mathbf{H}^{\Delta^{op}}
$$

of the [[groupoid object in an (∞,1)-category|groupoid objects]] internal to $\mathbf{H}$ and of the [[category object in an (∞,1)-category|category objects]] internal to $\mathbf{H}$ inside $\mathbf{H}^{\Delta^{op}}$.

Here $\mathbf{H}^{\Delta^{op}}$ is also the [[classifying topos]] for [[linear intervals]]. Its [[homotopy type theory]] [[internal language]] is equipped with an interval [[type]]. 

For more see at _[[simplicial object in an (∞,1)-category]]_.


#### Bundles of cohesive spectra

The [[tangent (∞,1)-category]] $T\mathbf{H}$
to a cohesive $\infty$-topos is itself cohesive, 
(by the discussion at
_[tangent ∞-category -- Examples -- Of an ∞-topos](tangent+%28infinity%2C1%29-category#TangentTopos)_), the 
_[[tangent cohesive (∞,1)-topos]]_.

This $T \mathbf{H}$ the $\infty$-topos of [[parameterized spectra]] in $\mathbf{H}$, hence is context for cohesive [[stable homotopy theory]].

$$
  \array{
    Stab(\mathbf{H})
    &
    \stackrel{\overset{L\Pi^{seq}}{\longrightarrow}}{\stackrel{\overset{Disc^{seq}}{\leftarrow}}{\stackrel{\overset{\Gamma^{seq}}{\longrightarrow}}{\underset{coDisc^{seq}}{\leftarrow}}}}
    &
    Stab(\infty Grpd)
    \\
    \downarrow^{\mathrlap{incl}} && \downarrow^{\mathrlap{incl}}
    \\
    T \mathbf{H}
    &
    \stackrel{\overset{L\Pi^{seq}}{\longrightarrow}}{\stackrel{\overset{Disc^{seq}}{\leftarrow}}{\stackrel{\overset{\Gamma^{seq}}{\longrightarrow}}{\underset{coDisc^{seq}}{\leftarrow}}}}
  &
  T \infty Grpd
  \\
  {}^{\mathllap{base}}\downarrow {}^{\mathllap{0}}\uparrow \downarrow^{\mathrlap{base}} \uparrow^{\mathrlap{0}}
  && 
  {}^{\mathllap{base}}\downarrow {}^{\mathllap{0}}\uparrow \downarrow^{\mathrlap{base}} \uparrow^{\mathrlap{0}}
  \\
    \mathbf{H}
    &
    \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
  &
  \infty Grpd
  }
  \,.
$$

### Global equivariant homotopy theory

[[!include equivariant homotopy theory -- table]]


### From $\infty$-Cohesive sites of definition
 {#ExamplesFromCohesiveSitesOnfDefinition}

+-- {: .num_prop}
###### Proposition

Examples of [[∞-cohesive site]]s are

* any category with finite [[product]]s and equipped with the trivial [[coverage]].

* the [[full subcategory]] $CartSp_{top} \subset$ [[Top]] on [[open ball]]s with the [[good open cover]] [[coverage]];

* the site [[CartSp]] of [[Cartesian space]]s with [[smooth function]]s between them and [[good open cover]] [[coverage]].

* the [[Cahiers topos]]-site [[ThCartSp]] of infinitesimally thickened Cartesian spaces.

=--

From this one obtains the following list of examples of cohesive $(\infty,1)$-toposes.

#### Discrete $\infty$-groupoids
 {#DiscreteInfinityGroupoids}

* [[discrete ∞-groupoid]]


#### Topological $\infty$-groupoids

* [[Euclidean-topological ∞-groupoid]]

* [[locally contractible topological ∞-groupoid]]


#### Smooth $\infty$-groupoids

* [[smooth ∞-groupoid]]

#### Complex analytic $\infty$-groupoids

* [[complex analytic ∞-groupoid]]

#### Formal smooth $\infty$-groupoids

* [[formal smooth ∞-groupoid]]


#### Smooth Super $\infty$-groupoids

* [[super ∞-groupoid]]

* [[smooth super ∞-groupoid]]

* [[synthetic differential super ∞-groupoid]]


#### Smooth $\infty$-groupoids over algebraic $\infty$-stacks

One can consider the [[tangent (∞,1)-topos]] of the [[cohesive (∞,1)-topos]]

$$
  Sh_\infty\left(SmthMfd, Sh_\infty\left(Sch_{\mathbb{Z}}\right)\right)
  \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
  Sh_\infty(Sch_{\mathbb{Z}})
$$

of [[∞-stacks]] on the [[site]] of [[smooth manifolds]] with values in turn in [[∞-stack]] over a [[site]] of [[arithmetic schemes]], hence by [[smooth ∞-groupoids]] but over a [[base (∞,1)-topos]] of algebraic [[∞-stacks]].

This leads to [[differential algebraic K-theory]]. See there for details.

### $E_\infty$-Arithmetic $\infty$-groupoids

see _[[differential cohesion and idelic structure]]_

[[!include arithmetic cohesion -- table]]


### Smooth cohesion over arbitrary base $\infty$-toposes

The above examples relativize to [arbitrary bases](#OverArbitraryBases).

For instance [[smooth infinity-groupoid|smooth cohesion]] over an [[(∞,1)-topos]] over a suitable [[site]] of [[schemes]] is the natural context for [[differential algebraic K-theory]]. See there for more.

## Applications


As a context for geometric spaces and paths in geometric spaces, cohesive $(\infty,1)$-toposes are a natural context in which to formulate fundamental fundamental [[physics]]. See [[higher category theory and physics]] for more on this.

See also

* [[∞-Chern-Weil theory]]


* [[schreiber:∞-Chern-Simons theory]]


## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]]
  
  * [[Pi modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]]

* [[cohesive topos]] / **cohesive (∞,1)-topos**

* [[condensed cohesion]]

and

* [[locally connected site]], [[locally ∞-connected site]]

* [[connected site]]

* [[local site]]

* [[cohesive site]], [[(∞,1)-cohesive site]]

_unrelated_ is the notion of _[[cohesive ∞-prestack]]_

## References

### Precursors

The [[category theory|category-theoretic]] definition of [[cohesive topos]] was proposed by [[Bill Lawvere]]. See the references at _[[cohesive topos]]_.

The observation that the further left adjoint $\Pi$ in a [[locally ∞-connected (∞,1)-topos]] defines an intrinsic notion of paths and [[geometric homotopy groups in an (∞,1)-topos]] was suggested by [[Richard Williamson]].

The observation that the further right adjoint $coDisc$ in a [[local (∞,1)-topos]] serves to characterize [[concrete sheaf|concrete (∞,1)-sheaves]] was amplified by [[David Carchedi]].

Some aspects of the discussion here are, more or less explicitly, in 

* [[Carlos Simpson]], [[Constantin Teleman]], _deRham theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))
{#SimpsonTeleman}

For instance something similar to the notion of [[infinity-connected (infinity,1)-site|∞-connected site]] and the 
[[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] is the content of section 2.16.  The [infinitesimal path ∞-groupoid adjunction](#LieTheory) $(\mathbf{Red} \dashv \mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{inf})$ is essentially discussed in section 3. The notion of geometric realization (see <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos%20--%20structures#Homotopy">structures in a cohesive (∞,1)-topos -- geometric realization</a>), is touched on around remark 2.22, referring to

* [[Carlos Simpson]], _The topological realization of a simplicial presheaf_ , ([arXiv:q-alg/9609004](http://arxiv.org/abs/q-alg/9609004)).
 {#Simpson} 

But, more or less explicitly, the presentation of geometric realization of simplicial presheaves is much older, going back to Artin-Mazur. See [[geometric homotopy groups in an (∞,1)-topos]] for a detailed commented list of literature.

A characterization of infinitesimal extensions and formal smoothness by adjoint functors (discussed at [[infinitesimal cohesion]]) is considered in 

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative spaces_, preprint MPI-2004-35 ([ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2331), [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2303))
 {#KontsevichRosenbergSpaces}

in the context of _[[Q-categories]]_ .

### On cohesive $(\infty,1)$-toposes proper

On the material presented here:

* [[Urs Schreiber]], Section 3 of: _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))

* [[Hisham Sati]], [[Urs Schreiber]], Section 3.1.1 of: _[[schreiber:Proper Orbifold Cohomology]]_ ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))


### In homotopy type theory
  {#ReferencesInHoTT}

Expositions and discussion of the formalization of cohesion in [[homotopy type theory]] is in

* [[Mike Shulman]], _Axiomatic cohesion in HoTT_ ([blog post](http://homotopytypetheory.org/2011/11/02/axiomatic-cohesion-in-hott/))

The corresponding [[Coq]]-code is in 

* {#Shulman} [[Mike Shulman]], _[HoTT/Coq/Subcategories](https://github.com/mikeshulman/HoTT/tree/master/Coq/Subcategories)_
  

Exposition is at

* [[Mike Shulman]], _Internalizing the External, or The Joys of Codiscreteness_ ([blog post](http://golem.ph.utexas.edu/category/2011/11/internalizing_the_external_or.html))

[[!redirects cohesive (∞,1)-topos]]

[[!redirects cohesive (∞,1)-toposes]]
[[!redirects cohesive (infinity,1)-toposes]]

[[!redirects cohesive (∞,1)-topoi]]
[[!redirects cohesive (infinity,1)-topoi]]

[[!redirects cohesive ∞-topos]]
[[!redirects cohesive ∞-toposes]]

[[!redirects cohesive infinity-topos]]
[[!redirects cohesive infinity-toposes]]


[[!redirects cohesive ∞-groupoid]]
[[!redirects cohesive ∞-groupoids]]

[[!redirects cohesive infinity-groupoid]]
[[!redirects cohesive infinity-groupoids]]

[[!redirects cohesive homotopy theory]]
[[!redirects cohesive homotopy theories]]

[[!redirects cohesive model topos]]
[[!redirects cohesive model toposes]]
