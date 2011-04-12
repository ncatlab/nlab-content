
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

A _cohesive $(\infty,1)$-topos_ is a [[big topos|big]] [[(∞,1)-topos]] $\mathbf{H}$ that provides a context of generalized [[space]]s in which [[higher geometry]] makes sense. 

It is an $(\infty,1)$-topos whose [[global section]] [[(∞,1)-geometric morphism]] $(Disc \dashv \Gamma): \mathbf{H} \stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}} $ [[∞Grpd]] admits a further [[left adjoint|left]] [[adjoint (∞,1)-functor]] $\Pi$ and a further right adjoint $CoDisc$: 

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv Codisc) : \mathbf{H} \to \infty Grpd
$$ 

with $Disc$ and $Codisc$ both [[full and faithful (∞,1)-functor]]s and such that $\Pi$ moreover preserves finite [[(∞,1)-limit|(∞,1)-product]]s. Here

1. the existence of $CoDisc$ induces a sub-[[(∞,1)-quasitopos]] $Conc(\mathbf{H}) \hookrightarrow \mathbf{H}$ of _[[concrete (∞,1)-sheaf|concrete objects]]_ that behave like [[∞-groupoid]]s _equipped with extra cohesive structure_ , such as with [[topology|continuous structure]], [[smooth structure]], etc.

1. the existence of $\Pi$ induces a notion of [[geometric homotopy groups in an (∞,1)-topos|geometric]] [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|fundamental ∞-groupoid]], hence under $|-| : \infty Grpd \simeq $ [[Top]] of [[geometric realization]] $|\Pi(-)|$ of objects in $\mathbf{H}$.

The functor $\Gamma$ itself may be thought of as sending a cohesive [[∞-groupoid]] $X$ to its underlying bare $\infty$-groupoid $\Gamma(X)$. This is $X$ with all _cohesion forgotten_ (for instance with the continuous or the smooth structure forgotten).

Conversely, $Disc$ and $CoDisc$ send an $\infty$-groupoid $A$ either to the [[discrete space|discrete ∞-groupoid]] $Disc(A)$ with _discrete_ cohesive structure (for instance with [[discrete topology]]) or to the [[codiscrete space|codiscrete ∞-groupoid]] $Codisc(A)$ with the _codiscrete_ cohesive structure (for instance with [[codiscrete topology]]). 

The existence of such a quadruple of adjoint $(\infty,1)$-functors alone implies a rich [[internalization|internal]] [[higher geometry]] in $\mathbf{H}$ that comes with its internal notion of [[Galois theory]], [[Lie theory]], [[differential cohomology]], [[Chern-Weil theory]]. 

Examples of cohesive $(\infty,1)$-toposes include

* the $(\infty,1)$-topos $\mathbf{H} = $ [[ETop∞Grpd]] of [[Euclidean-topological ∞-groupoids]];

* the $(\infty,1)$-topos $\mathbf{H} = $ [[Smooth∞Grpd]] of [[smooth ∞-groupoids]] 

* the $(\infty,1)$-topos $\mathbf{H} = $ [[SynthDiff∞Grpd]] of [[synthetic differential ∞-groupoids]].

In the first the internal notion of [[Galois theory]] subsumes the usual one (over well-behaved topological spaces). In the latter also the notions of [[Lie theory]], [[differential cohomology]] and [[Chern-Weil theory]] subsume the uual ones --- and generalize them to higher smooth geoemtry.


## Definition

+-- {: .un_defn #CohesiveInfinTopos}
###### Definition

An [[(∞,1)-topos]] $\mathbf{H}$ is **cohesive** if

1. it is a [[strongly ∞-connected (∞,1)-topos]];

1. it is a [[local (∞,1)-topos]].

This means equivalently: the [[global section]] [[(∞,1)-geometric morphism]] lifts to a quadruple of [[adjoint (∞,1)-functor]]s
   
$$
  (f_! \dashv f^* \dashv f_* \dashv f^!) : 
  \mathbf{H}
   \stackrel{\stackrel{\overset{f_!}{\to}}{\overset{f^*}{\leftarrow}}}{\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}
  \infty Grpd
  \;
$$

where $f_!$ preserves [[finite limit|finite]] [[(∞,1)-product]].

=--

+-- {: .un_defn #PiecesHavePoints}
###### Definition

We say that **pieces have points** for an object
$X$ in a cohesive $(\infty,1)$-topos $\mathbf{H}$ 
if the morphism

$$
  \Gamma X \to \Gamma Disc \Pi X \simeq \Pi X
$$ 

is an [[effective epimorphism in an (∞,1)-category]], equivalently (as discussed there) such that this is an [[epimorphism]] on [[connected]] components.


=--

Here the first morphismism is the image under $\Gamma$ of the 
$(Disc \dashv \Gamma)$-[[unit of an adjunction|unit]] and the second is an inverse of the $(\Pi \dashv Disc)$-counit (which is invertible because $Disc$ is [[full and faithful (∞,1)-functor|full and faithful]] in a [[local (∞,1)-topos]].)

+-- {: .un_defn #DiscreteObjectsAreConcrete}
###### Definition

We say **discrete objects are concrete** in $\mathbf{H}$ if for all
$S \in $[[∞Grpd]] the morphism

$$
  Disc S \to coDisc \Gamma Disc S \stackrel{\simeq}{\to} coDisc S
$$

induces [[monomorphism]]s on all [[categorical homotopy groups in an (infinity,1)-topos|homotopy sheaves]].

=--

## Properties


### As a point-like space



+-- {: .un_prop #PointLike}
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

+-- {: .un_remark}
###### Remark

This says that a cohesive $(\infty,1)$-topos $\mathbf{H}$ is, when itself regarded as a [[little topos]], a generalized [[space]], a _thickened point_ . We may think of it as the standard [[point]] equipped with a _cohesive neighbourhood_ .

In this sense every space $X$ _modeled on_ the cohesive structure defined by $\mathbf{H}$ is an [[étale space]] over $X$: its [[petit topos|petit]] $(\infty,1)$-topos $\mathbf{H}/X$ sits by a [[locally homeomorphic geometric morphism]] over $\mathbf{H}$

$$
  \mathbf{H}/X \stackrel{local\;homeo}{\to} \mathbf{H}
  \,.
$$


=--


### General

+-- {: .un_prop}
###### Proposition

Every cohesive $(\infty,1)$-topos is a 
[[hypercomplete (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof


By the [above proposition](#PointLike) it has finite 
[[homotopy dimension]]. This implies hypercompeteness. See there.

=--

+-- {: .un_prop}
###### Proposition

For $\mathbf{H}$ a cohesive $(\infty,1)$-topos, the [[(n,1)-topos|(1,1)-topos]] $\tau_{\leq 1-1} \mathbf{H}$ of 0-[[truncated]] objects is a [[cohesive topos]].

=--


### Over an $\infty$-cohesive site


+-- {: .un_prop}
###### Proposition

For $C$ an [[∞-cohesive site] the [[(∞,1)-category of (∞,1)-sheaves]] $(\infty,1)Sh(C)$ over $C$ is a cohesive $(\infty,1)$-topos satisfying the two axioms _[pieces have points](#PiecesHavePoints)_ and _[discrete objects are concrete](#DiscreteObjectsAreConcrete)_ .

=--

See [[∞-cohesive site]].

## Structures in a cohesive $(\infty,1)$-topos {#Structures}

A cohesive $(\infty,1)$-topos is a general context for [[higher geometry]] with good [[cohomology]] and [[homotopy]] properties. We list fundamental structures and constructions that exist in every cohesvive $(\infty,1)$-topos.


### Concrete objects{#ConcreteObjects}


The cohesive structure on an object in a cohesive 
$(\infty,1)$-topos need not be supported by points. 
We discuss a general abstract characterization of  
objects that do have an interpretation as bare $n$-groupoids 
equipped with cohesive structure.

Compare with the section <a href="http://nlab.mathforge.org/nlab/show/cohesive%20topos#ConcreteObjects">Quasitoposes of concrete objects</a> at [[cohesive topos]].


+-- {: .un_prop}
###### Proposition

On a cohesive $(\infty,1)$-topos $\mathbf{H}$ 
both $\mathrm{Disc}$ and $\mathrm{coDisc}$ 
are [[full and faithful (∞,1)-functor]]s and $\mathrm{coDisc}$ exhibits [[∞Grpd]]  as a sub-$(\infty,1)$-topos of $\mathbf{H}$ by an  
[[(∞,1)-geometric embedding]]

$$
  \infty Grpd
    \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{coDisc}{\hookrightarrow}}
  \mathbf{H}
  \,.
$$

=--

+-- {: .proof}
###### Proof

The full and faithfulness of $Disc$ and $coDisc$ follows as
in the discussion at [[∞-connected (∞,1)-topos]],
Since $\Gamma$ is also a right adjoint it preserves 
in particular [[finite limit|finite]] [[(∞,1)-limit]]s, so that
$(\Gamma \dashv \mathrm{coDisc})$ is indeed an 
[[(∞,1)-geometric morphism]]. 
(See the general discussion at [[local (∞,1)-topos]].)



=--

+-- {: .un_prop}
###### Proposition


The [[(∞,1)-topos]] [[∞Grpd]] is equivalent to 
the full [[sub-(∞,1)-category]] of $\mathbf{H}$ on 
those objects $X \in \mathbf{H}$ for which the 
[[unit of an adjunction|counit]]
 
$$
    X \to \mathrm{coDisc}\Gamma X
$$
  
is an [[equivalence in an (∞,1)-category|equivalence]].

=--

+-- {: .proof}
###### Proof

This follows by general facts discussed at [[reflective sub-(∞,1)-category]].

=--

+-- {: .un_def}
###### Definition

We say a 0-[[truncated]] object $X \in \mathbf{H}$ is 
is **concrete** if the [[unit of an adjunction|counit]]

$$
  X \to \mathrm{coDisc} \Gamma X
$$

is a [[monomorphism]]. We say a general object $X$ is 
concrete if all its 
[[categorical homotopy groups in an (∞,1)-topos|categorical homotopy sheaves]] are concrete.

=--

+-- {: .un_prop}
###### Proposition

For $C$ an [[∞-cohesive site]], a 0-truncated object in the 
[[(∞,1)-topos]] over $C$ is concrete prescisely if it is
a [[concrete sheaf]] in the traditional sense.

=--




### Geometry and structure sheaves {#GeometryAndStructureSheaves}

+-- {: .un_def}
###### Definition

Fix an uncountable [[regular cardinal]] $\kappa$. Let 

$$
  \mathcal{G} \hookrightarrow Conc(\mathbf{H}) \hookrightarrow \mathbf{H}
$$ 

be the full [[sub-(∞,1)-category]] of [concrete objects](#ConcreteObjects) whose underlying $\infty$-groupoid is a $\kappa$-[[small (infinity,1)-category|small ∞-groupoid]]. 

=--

+-- {: .un_def}
###### Definition

We equip $\mathcal{G}$ with the canonical structure of a [[geometry (for structured (infinity,1)-toposes)|geometry]]:

* the _admissible morphisms_ are the [[monomorphism in an (infinity,1)-category|monomorphisms]];

* a family $\{U_i \to U\}$ of monomorphisms is a [[covering]] if the induced morphism out of the coproduct

  $$
    \coprod_i U_i \to U
  $$

  is an [[effective epimorphism]] in $\mathbf{H}$;


=--

+-- {: .un_lemma}
###### Observation

This definition indeed makes $\mathcal{G}$ a [[geometry (for structured (infinity,1)-toposes)|geometry]].

=--

+-- {: .proof}
###### Proof

By the $\kappa$-bound $\mathcal{G}$ is a [[small (∞,1)-category]].

Monomorphisms are stable under pullbacks and satisfy 2-out-of-3 (See [[monomorphism in an (∞,1)-category]].)

The quasi-$(\infty,1)$-topos $Conc(\mathbf{H})$ has all finite $(\infty,1)$-limits and these are preserved by the right adjoint inclusion $Conc(\mathbf{H}) \hookrightarrow \mathbf{H}$.

It also has all $\kappa$-bounded $(\infty,1)$-colimits (computed in $\mathbf{H}$ and reflected back into $\mathcal{G}$), hence is an [[idempotent complete (∞,1)-category]].

A covering family in $\mathcal{G}$ goes to an effective epimorphism by definition. Effective epimorphisms are stable under pullback in $\mathcal{G}$ because that pullback coincides with the pullback in $\mathbf{H}$ where the statement holds due to [[universal colimits]] of the $(\infty,1)$-topos.

=--

+-- {: .un_def}
###### Definition


For every object $X \in \mathbf{H}$ define the functor

$$
  \mathcal{O}_X : \mathcal{G} \hookrightarrow \mathbf{H}
   \stackrel{X^*}{\to} \mathbf{H}/X
$$

from $\mathcal{G}$ to the [[over-(∞,1)-topos]] over $X$, where $X^*$ is the [[inverse image]] functor of the corresponding [[étale geometric morphism]].

=--

+-- {: .un_lemma}
###### Observation

This makes $\mathbf{H}/X$ a $\mathcal{G}$-[[structured (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

Since $X^*$, being an inverse image, preserves finite limits and since it preserves effective epimorphisms, by [[universal colimits]].

=--


### Cohesive $\infty$-Groups 
  {#InfinGroups}

Every [[(∞,1)-topos]] $\mathbf{H}$ 
comes with a notion of [[group object in an (∞,1)-category|∞-group objects]] that generalizes the traditional notion of grouplike $A_\infty$ spaces in [[Top]] $\simeq$ [[∞Grpd]].



+-- {: .un_def}
###### Definition

  For $X \in \mathbf{H}$ an object and $x : * \to X$ a point, the 
  **[[loop space object]]** of $X$ is the [[(∞,1)-pullback]]
  $\Omega_x X := * \times_X *$:

  $$
    \array{
       \Omega_x X & \to & {*} 
       \\
       \downarrow && \downarrow^{\mathrlap{x}}
       \\
       {*} & \stackrel{x}{\to} & X
    }
    \,.
  $$

=--

This object $\Omega_x X$ is canonically equipped with the structure of an [[∞-group]] obect.


+-- {: .un_remark}
###### Remark

Notice that every [[0-connected]] object $A$ in the cohesive $(\infty,1)$-topos $\mathbf{H}$ does have a global point (then necessarily essentially unique) $* \to A$.

=--

This follows from the [above proposition](#PointLike) which says that $\mathbf{H}$ necessarily has [[homotopy dimension]] $\leq 0$.


+-- {: .un_prop}
###### Proposition

The operation of forming [[loop space object]]s in $\mathbf{H}$ establishes an [[equivalence of (∞,1)-categories]]

$$
  \Omega : PointedConnected(\mathbf{H}) \stackrel{\simeq}{\to} Grp(\mathbf{H})  
$$

between the [[(∞,1)-category]] of [[group object in an (∞,1)-category|group object]]s in $\mathbf{H}$ and the full [[sub-(∞,1)-category]] of [[pointed object]]s $*/\mathbf{H}$ on those that are [[0-connected]].

=--

+-- {: .proof}
###### Proof

By the discussion at <a href="http://ncatlab.org/nlab/show/groupoid+object+in+an+(infinity%2C1)-category#Delooping">delooping</a>. 

=--

We write

$$
  \mathbf{B} : Grpd(\mathbf{H}) \to  PointedConnected(\mathbf{H})
$$

for the inverse to $\Omega$. For $G \in Grp(\mathbf{H})$ we call 
$\mathbf{B}G \in PointedConnected(\mathbf{H}) \hookrightarrow \mathbf{H}$ the 
**[[delooping]]** of $G$.

Notice that since the cohesive $(\infty,1)$-topos $\mathbf{H}$ has [[homotopy dimension]] $0$ by the [above proposition](#PointLike) every 0-connected object has an essentially unique point, but nevertheless the [[homotopy type]] of $*/\mathbf{H}(\mathbf{B}G, \mathbf{B}H)$ may differ from that of $\mathbf{H}(\mathbf{B}G, \mathbf{B}H)$.


+-- {: .un_prop}
###### Observation

 The delooping object $\mathbf{B}G \in \mathbf{H}$ is concrete preciely if $G$ is.

=--

We may therefore unambiguously speak of **concrete cohesive $\infty$-groups**.

+-- {: .un_def}
###### Definition

  For $f : Y \to Z$ any morhism in $\mathbf{H}$
  and $z : * \to Z$ a point, the [[homotopy fiber|∞-fiber]] or
  of $f$ over this point is the [[(∞,1)-pullback]] 
  $ X := {*} \times_Z Y$

  $$
    \array{
        X & \to & {*} 
        \\
        \downarrow && \downarrow^{\mathrlap{z}}
        \\
        Y & \stackrel{f}{\to} & Z
    }
    \,.
  $$

=--

+-- {: .un_remark}
###### Observation

  Suppose that also $Y$ is pointed and $f$ is a morphism of pointed objects.
  Then the $\infty$-fiber of an $\infty$-fiber is the 
  [[loop space object]] of the base.

=--

This means that we have a diagram

$$
  \array{
      \Omega_z Z  & \to& X & \to & {*} 
      \\
      \downarrow && \downarrow && \downarrow
      \\
      {*} & \to & Y & \stackrel{f}{\to} & Z
  }
  \,,
$$

where the outer rectangle is an [[(∞,1)-pullback]] if the left square is an 
[[(∞,1)-pullback]]. 
This follows from the pasting law for $(\infty,1)$-pullbacks in any
[[(∞,1)-category]].


+-- {: .un_prop}
###### Proposition

If the cohesive $(\infty,1)$-topos $\mathbf{H}$ has an [[∞-cohesive site]] of definition $C$, then 

* every [[∞-group]] object has a presentation by a presheaf of [[simplicial group]]s 

  $$
    G \in [C^{op}, sGrp] \stackrel{U}{\to} [C^{op}, sSet]
  $$
 
  which is fibrant in $[C^{op}, sSet]_{proj}$;

* the corresponding [[delooping]] object is presented by the presheaf 

  $$
    \bar W G \in [C^{op}, sSet_0] \hookrightarrow [C^{op}, sSet]
  $$

  which is given over each $U \in C$ by $\bar W (G(U))$ (see [[simplicial group]] for the notation).

=--

+-- {: .proof}
###### Proof

Let $* \to X \in [C^{op}, sSet]_{proj,loc}$ be a locally fibrant representative of $* \to \mathbf{B}G$. Since the [[terminal object]] $*$ is indeed presented by the presheaf constant on the point we have functorial choices of basepoints in all the $X(U)$ for all $U \in C$ and by assumption that $X$ is [[connected]] all the $X(U)$ are connected. Hence without loss of generality we may assume that $X$ is presented by a presheaf of reduced simplicial sets
$X \in [C^{op}, sSet_0] \hookrightarrow X \in [C^{op}, sSet]$.

Then notice the [[Quillen equivalence]] between the [[model structure on reduced simplicial sets]] and the [[model structure on simplicial groups]]

$$
  (\Omega \dashv \bar W) : sGrp \stackrel{\overset{\Omega}{\leftarrow}}{\underset{\bar W}{\to}}
   sSet_0
  \,.
$$

In particular its [[unit of an adjunction|unit]] is a weak equivalence

$$
  \bar W \Omega Y \stackrel{\simeq}{\to} Y
$$

for every $Y \in sSet_0 \hookrightarrow sSet_{Quillen}$ and $\bar W \Omega Y$ is always a [[Kan complex]]. Therefore 

$$
  \bar W \Omega X \in [C^{op}, sSet]_{proj}
$$

is an equivalent representative for $X$, fibrant at least in the global model structure. Since the finite [[(∞,1)-limit]] involved in forming [[loop space object]]s is equivalently computed in the global model structure, it is sufficient to observe that

$$
  \array{
    \Omega X &\to& W \Omega X
    \\
    \downarrow && \downarrow
    \\
    * &\to& \bar W \Omega X
  }
$$

is

* a [[pullback]] diagram in $[C^{op}, sSet]$ (because it is so over each $U \in C$ by the general discussion at [[simplicial group]]);

* a [[homotopy pullback]] of the point along itself (since $W G \to \bar W G$ is objectwise a fibration [[resolution]] of the point inclusion).


=--

### Cohomology and principal $\infty$-bundles {#Cohomology}

There is an intrinsic notion of [[cohomology]] and 
of [[principal ∞-bundles]] in any [[(∞,1)-topos]] $\mathbf{H}$.

+-- {: .un_def}
###### Definition

For $X,A \in \mathbf{H}$ two [[object]]s, we say that

$$
  H(X,A) := \pi_0 \mathbf{H}(X,A)
$$

is the **[[cohomology]] set** of $X$ with coefficients in $A$. If $A = G$ is an  [[∞-group]] we write

$$
  H^1(X,G) := \pi_0 \mathbf{H}(X, \mathbf{B}G)
$$

for cohomology with coefficients in its [[delooping]]. Generally, if  $K \in \mathbf{H}$ has a $p$-fold [[delooping]], we write

$$
  H^p(X,K) := \pi_0 \mathbf{H}(X, \mathbf{B}^p K)
  \,.
$$

=--

In the context of cohomology on $X$ with coefficients in $A$ we we say that

* the hom-space $\mathbf{H}(X,A)$ is the **cocycle $\infty$-groupoid**;

* a [[morphism]] $g : X \to A$ is a [[cocycle]];

* a [[2-morphism]] : $g \Rightarrow h$ is a [[coboundary]] between cocycles.

* a morphism $c : A \to B$ represents the [[characteristic class]]

  $$
    [c] : H(-,A) \to H(-,B)
    \,.
  $$


+-- {: .un_def}
###### Definition


For every morphism $c : \mathbf{B}G \to \mathbf{B}H \in \mathbf{H}$ define the **long [[fiber sequence]] to the left**

$$
   \cdots 
   \to 
   \Omega G
  \to 
  \Omega H 
   \to 
   F
    \to 
   G 
     \to  
   H 
     \to 
    \mathbf{B} F 
     \to 
    \mathbf{B}G
      \stackrel{c}{\to} 
   \mathbf{B}H
$$

to be the given by the consecutive [[pasting]] diagrams of [[(∞,1)-pullback]]s

$$
  \array{
      \vdots && \vdots
      \\
      \Omega H &\to& G &\to& *
      \\
      \downarrow &&\downarrow && \downarrow 
      \\
     * &\to& H &\to& \mathbf{B}F &\to& *
      \\
     &&\downarrow && \downarrow && \downarrow
     \\
     && * &\to& \mathbf{B}G & \stackrel{c}{\to} & \mathbf{B}H
  }
  \,.
$$

=--

+-- {: .un_prop}
###### Proposition

* The long fiber sequence to the left of $c : \mathbf{B}G \to \mathbf{B}H$ becomes constant on the point after $n$ iterations if $H$ is $n$-[[truncated]]. 


* For every object $X \in \mathbf{H}$ we have a long [[exact sequence]] of [[pointed set]]s


  $$  
    \cdots \to H^0(X,G) \to H^0(X,H) \to H^1(X,F) \to H^1(X,G) \to H^1(X,H)
   \,.
  $$

=--

+-- {: .proof}
###### Proof

The first statement follows from the observation that a 
[[loop space object]] $\Omega_x A$ is a fiber of the [[free loop space object]] $\mathcal{L} A$
and that this may equivalently be computed by the 
[[(∞,1)-powering]] $A^{S^1}$, where $S^1 \in Top \simeq \infty Grpd$ is the [[circle]]. (See [[Hochschild cohomology]] for details.)

The second statement follows by observing that the 
$\infty$-hom-functor $\mathbf{H}(X,-)$ preserves all 
[[(∞,1)-limit]]s, so that we have [[(∞,1)-pullback]]s

$$ 
  \array{
    \mathbf{H}(X,F) &\to &*
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,G) &\to& \mathbf{H}(X,H)
  }
$$

etc. in [[∞Grpd]] at each stage of the fiber sequence. The statement then follows with the familiar [[long exact sequence]] for [[homotopy group]]s in [[Top]] $\simeq$ [[∞Grpd]].

=--

To every cocycle $g : X \to \mathbf{B}G$ is canonically associated its [[homotopy fiber]] $P \to X$, the [[(∞,1)-pullback]]

$$
  \array{
    P &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{g}{\to}& \mathbf{B}G
    \,.
  }
  \,.
$$

We discuss now that $P$ canonically has the structure of a $G$-[[principal ∞-bundle]] and that $\mathbf{B}G$ is the [[fine moduli space]] for $G$-principal $\infty$-bundles.


+-- {: .un_defn}
###### Definition
**(principal $G$-action)**

Let $G$ be a [[groupoid object in an (∞,1)-category|group object in the (∞,1)-topos]] $\mathbf{H}$. A **principal [[action]]** of $G$ on an object $P \in \mathbf{H}$ is 
a [[groupoid object in an (∞,1)-category|groupoid object in the (∞,1)-topos]] $P//G$ that sits over $*//G$ in that we have a 
  morphism of [[simplicial object|simplicial diagram]]s $\Delta^{op} \to \mathbf{H}$

$$
  \array{
    \vdots && \vdots
    \\
    P \times G \times G
    &\stackrel{(p_2, p_3)}{\to}& G \times G
    \\
   \downarrow\downarrow\downarrow 
    && \downarrow\downarrow\downarrow
    \\
    P \times G
    &\stackrel{p_2}{\to}& G
    \\
    \downarrow\downarrow && \downarrow\downarrow
    \\
    P &\stackrel{}{\to}& {*}
  }
$$

in $\mathbf{H}$.

We say that the [[(∞,1)-colimit]]

$$
  X : \lim_\to (P//G : \Delta^{op} \to \mathbf{H})
$$

is the **base space** defined by this action.

=--

We may think of $P//G$ as the **[[action groupoid]]** of the $G$-action on $P$. For us it _defines_ this $G$-action.


+-- {: .un_prop}
###### Proposition

The $G$-principal action as defined above satisfies the 
**principality condition** in that we have an equivalence of
groupoid objects

 $$
   \array{
     \vdots && \vdots
     \\
     P \times_X P \times_X P
     &\stackrel{\simeq}{\to}& 
     P \times G \times G
     \\
    \downarrow\downarrow\downarrow 
     && \downarrow\downarrow\downarrow
     \\
     P \times_X P
     &\stackrel{\simeq}{\to}& 
     P \times G
     \\
     \downarrow\downarrow && \downarrow\downarrow
     \\
     P &\stackrel{\simeq}{\to}& P
   }
   \,.
 $$

=--

+-- {: .proof}
###### Proof

This principality condition asserts that the groupoid object $P//G$ is [[groupoid object in an (infinity,1)-category|effective]]. By [[(∞,1)-topos|Giraud's axioms characterizing (∞,1)-toposes]], every groupoid object in $\mathbf{H}$ is effective.

=--


+-- {: .un_prop}
###### Proposition

For $X \to \mathbf{B}G$ any morphism, its [[homotopy fiber]] $P \to X$
is canonically equipped with a principal $G$-action with base space $X$.

=--

+-- {: .proof}
###### Proof

By the above we need to show that we have a morphism of simplicial diagrams

$$
  \array{
    \vdots && \vdots && \vdots
    \\
    P \times_X P \times_X P 
    &\stackrel{\simeq}{\to}& P \times G \times G
    &\to& G \times G
    \\
    \downarrow\downarrow\downarrow
    && 
   \downarrow\downarrow\downarrow 
    && \downarrow\downarrow\downarrow
    \\
    P \times_X P &\stackrel{\simeq}{\to}& P \times G
    &\stackrel{p_2}{\to}& G
    \\
    \downarrow\downarrow
    && \downarrow\downarrow && \downarrow\downarrow
    \\
    P &\stackrel{=}{\to}& P &\stackrel{}{\to}& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X &\stackrel{=}{\to}& X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,,
$$

where the left horizontal morphisms are equivalences, as indicated. We proceed by induction through on the height of this diagram.

The defining [[(∞,1)-pullback]] square for $P \times_X P$ is 

$$
  \array{
    P \times_X P &\to& P
    \\
    \downarrow && \downarrow
    \\
    P &\to& X
  }
$$

To compute this, we may attach the defining $(\infty,1)$-pullback square of $P$ to obtain the [[pasting]] diagram

$$
  \array{
    P \times_X P &\to& P &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    P &\to& X &\to& \mathbf{B}G
    \,.
  }
$$

and use the [pasting law for pullbacks](http://ncatlab.org/nlab/show/pullback#Pasting), to conclude that $P \times_X P$ is the pullback

$$
  \array{
    P \times_X P &\to& &\to& {*}
    \\
    \downarrow && && \downarrow
    \\
    P &\to& X &\to& \mathbf{B}G
    \,.
  }
$$

By defnition of $P$ as the homotopy fiber of $X \to \mathbf{B}G$, the lower horizontal morphism is equivalent to $P \to {*} \to \mathbf{B}G$, so that $P \times_X P$ is equivalent to the pullback

$$
  \array{
    P \times_X P &\to& &\to& {*}
    \\
    \downarrow && && \downarrow
    \\
    P &\to& {*} &\to& \mathbf{B}G
    \,.
  }
$$

This finally may be computed as the pasting of two pullbacks

$$
  \array{
    P \times_X P &\simeq& P \times G &\to& G &\to& {*}
    \\
    &&\downarrow && \downarrow && \downarrow
    \\
    &&P &\to& {*} &\to& \mathbf{B}G
    \,.
  }
$$

of which the one on the right is the defining one for $G$ and the remaining one on the left is just an [[(∞,1)-product]].  

Proceeding by induction from this case we find analogousy that $P^{\times_X^{n+1}} \simeq P \times G^{\times_n}$: suppose this has been shown for $(n-1)$, then the defining pullback square for $P^{\times_X^{n+1}}$ is

$$
  \array{
    P \times_X P^{\times_X^n}
    &\to&
    P
    \\
    \downarrow && \downarrow
    \\
    P^{\times_X^n}&\to& X
  }
  \,.
$$

We may again paste this to obtain

$$
  \array{
    P \times_X P^{\times_X^n}
    &\to&
    P
    &\to&
    *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    P^{\times_X^n}&\to& X &\to& \mathbf{B}G
  }
$$

and use from the previous induction step that

$$
  (P^{\times_X^n} \to X \to \mathbf{B}G) 
  \simeq
  (P^{\times_X^n} \to * \to \mathbf{B}G)
$$

to conclude the induction step with the same arguments as before.


=--

+-- {: .un_defn}
###### Definition

We say a $G$-principal action of $G$ on $P$ over $X$ is a 
$G$-[[principal ∞-bundle]] if the colimit over $P//G \to *//G$
produces a pullback square: the bottom square in 


$$
  \array{
    \vdots && \vdots
    \\
    P \times G \times G
    &\to& G \times G
    \\
   \downarrow\downarrow\downarrow 
    && \downarrow\downarrow\downarrow
    \\
    P \times G
    &\stackrel{p_2}{\to}& G
    \\
    \downarrow\downarrow && \downarrow\downarrow
    \\
    P &\stackrel{}{\to}& {*}
    \\
    \downarrow && \downarrow
    \\
    X = \lim_\to (P \times G^\bullet) &\stackrel{g}{\to}& 
   \mathbf{B}G = \lim_\to( G^\bullet)
  }
  \,.
$$


=--




### Concordance {#Concordance}

Since $\mathbf{H}$ is an [[(∞,1)-topos]] it carries canonically
the structure of a [[cartesian closed (∞,1)-category]]. For  
$X, Y \in \mathbf{H}$, write $Y^X \in \mathbf{H}$ for the corresponding
[[internal hom]].

Since $\Pi : \mathbf{H} \to $ [[∞Grpd]] preserves products, we have 
for all $X,Y, Z \in \mathbf{H}$ canonically induced a morphism

$$
  \Pi(Y^X) \times \Pi(Z^Y)
   \stackrel{\simeq}{\to}
  \Pi(Y^X \times Z^Y)
  \stackrel{\Pi(comp_{X,Y,Z})}{\to}
  \Pi(Z^X)
  \,.
$$

This should yield an [[(∞,1)-category]] $\tilde \mathbf{H}$
with the same objects as $\mathbf{H}$ and hom-$\infty$-groupoids defined by

$$
  \tilde \mathbf{H}(X,Y) := \Pi(Y^X)
  \,.
$$

We have that

$$
  \tilde \mathbf{H}(X,\mathbf{B}G) = \Pi(\mathbf{B}G^X) 
$$

is the $\infty$-groupoid whose objects are $G$-[[principal ∞-bundle]]s on $X$ and whose morphisms have the interpretaton of $G$-principal bundles on the cylinder $X \times I$. These are _[[concordance]]s of $\infty$-bundles._



### Geometric homotopy and Galois theory {#Homotopy}

We discuss canonical internal realizations of the notions of [[homotopy group]], [[local system]] and [[Galois theory]] in $\mathbf{H}$.


+-- {: .un_defn}
###### Definition

For $\mathbf{H}$ a [[locally ∞-connected (∞,1)-topos]] and $X \in \mathbf{H}$ an [[object]], we call $\Pi X \in $ [[∞Grpd]] the 
[[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] of $X$. The ([[categorical homotopy groups in an (∞,1)-topos|categorical]]) [[homotopy group]]s of $\Pi(X)$ we call the [[geometric homotopy groups in an (∞,1)-topos|geometric homotopy groups]] of $X$

$$
  \pi_\bullet^{geom}(X) := \pi_\bullet(\Pi (X))
  \,.
$$

=--

+-- {: .un_def}
###### Definition

We say a **geometric [[homotopy]]** between two morphism $f,g : X \to Y$
in $\mathbf{H}$ is a diagram

$$
  \array{
    X 
    \\
    \downarrow^{\mathrlap{(Id,i)}} & \searrow^{\mathrlap{f}}
    \\
    X \times I &\stackrel{\eta}{\to}& Y
    \\
    \uparrow^{\mathrlap{(Id,o)}} & \nearrow_{\mathrlap{g}}
    \\
    X
  }
$$

such that $I$ is geometrically connected, $\pi_0^{geom}(I) = *$.

=--

+-- {: .un_prop}
###### Proposition

If $f,g : X\to Y$ are geometrically homotopic in $\mathbf{H}$, then their images $\Pi(f), \Pi(g)$ are 
equivalent in $\infty Grpd$.

=--

+-- {: .proof}
###### Proof

By the condition that $\Pi$ preserves products
in a cohesive $(\infty,1)$-topos we have that the image of the
geometric homotopy in $\infty Grpd$ is a diagram of the form

$$
  \array{
    \Pi(X) 
    \\
    \downarrow^{\mathrlap{(Id,\Pi(i))}} & \searrow^{\mathrlap{\Pi(f)}}
    \\
    \Pi(X) \times \Pi(I) &\stackrel{\Pi(\eta)}{\to}& \Pi(Y)
    \\
    \uparrow^{\mathrlap{(Id,\Pi(o))}} & \nearrow_{\mathrlap{\Pi(g)}}
    \\
    \Pi(X)
  }
  \,.
$$

Now since $\Pi(I)$ is connected by assumption, there is a diagram

$$
  \array{
     && *
     \\
     & {}^{\mathllap{Id}}\nearrow & \downarrow^{\mathrlap{\Pi(i)}}
     \\
     * &\to& \Pi(I)
     \\
     & {}_{\mathllap{Id}}\searrow & \uparrow^{\mathrlap{\Pi(o)}}
     \\
     && *
  }
$$

in [[∞Grpd]].

Taking the product of this diagram with $\Pi(X)$ and pasting the result
to the above image $\Pi(\eta)$ of the geometric homotopy constructs
the equivalence $\Pi(f) \Rightarrow \Pi(g)$ in $\infty Grpd$.

=--

+-- {: .un_prop}
###### Proposition

For $\mathbf{H}$ a [[locally ∞-connected (∞,1)-topos]], also all its objects $X \in \mathbf{H}$ are locally $\infty$-connected, in the sense  their [[petit topos|petit]] [[over-(∞,1)-toposes]] $\mathbf{H}/X$ are locally $\infty$-connected.

The two notions of fundamental $\infty$-groupoids of $X$ induced this way do agree, in that there is a natural equivalence

$$
  \Pi_X(X \in \mathbf{H}/X) \simeq \Pi(X \in \mathbf{H})
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the general facts recalled at [[étale geometric morphism]] we have a composite [[essential geometric morphism]]

$$
  (\Pi_X \dashv \Delta_X \dashv \Gamma_X) : 
  \mathbf{H}_{/X}
   \stackrel{\overset{X_!}{\to}}{\stackrel{\overset{X^*}{\leftarrow}}{\underset{\X_*}{\to}}}
  \mathbf{H}
   \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\to}}}  
   \infty Grpd
$$

and $X_!$ is given by sending $(Y \to X) \in \mathbf{H}/X$ to $Y \in \mathbf{H}$.

=--


+-- {: .un_def}
###### Definition

For $\kappa$ a [[regular cardinal]] write 

$$
  Core \infty Grpd_\kappa \in \infty Grpd
$$ 

for the [[∞-groupoid]] of $\kappa$-[[small (∞,1)-category|small ∞-groupoid]]s: the [[core]] of the full [[sub-(∞,1)-category]] of [[∞Grpd]] on the $\kappa$-small ones.

=--

+-- {: .un_remark}
###### Remark

We have 

$$
  Core \infty Grpd_\kappa \simeq
  \coprod_i \mathbf{B} Aut(F_i)
  \,,
$$

where the coproduct ranges over all $\kappa$-small [[homotopy type]]s $[F_i]$ and $Aut(F_i)$ is the [[automorphism ∞-group]] of any representative $F_i$ of $[F_i]$.

=--

+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ write

$$
  LConst(X) := \mathbf{H}(X, Disc Core \infty Grpd_\kappa)
  \,.
$$

We call this the $\infty$-groupoid of **[[locally constant ∞-stack]]s** on $X$.

=--

+-- {: .un_observation}
###### Observation

Since $Disc$ is [[left adjoint]] and [[right adjoint]] it commutes with [[coproduct]]s and with [[delooping]] and therefore

$$
  Disc Core \infty Grpd_\kappa 
    \simeq 
  \coprod_i \mathbf{B} Disc Aut(F_i)
  \,.
$$

Therefore a cocycle $P \in LConst(X)$ may be identified on each geometric connected component of $X$ as a  $Disc Aut(F_i)$-[[principal ∞-bundle]] $P \to X$ over $X$ for the [[∞-group]] object  $Disc Aut(F_i) \in \mathbf{H}$. We may think of this as an object $P \in \mathbf{H}/X$ in the [[little topos]] over $X$. This way the objects of $LConst(X)$ are  indeed identified $\infty$-stacks over $X$.

=--


The following proposition says that the central statements of [[Galois theory]] hold for these canonical notions of geometric homotopy groups and locally constant $\infty$-stacks.

+-- {: .un_prop}
###### Proposition

For $\mathbf{H}$ [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] and [[∞-connected (∞,1)-topos|∞-connected]], we have

* a natural equivalence 

  $$
    LConst(X) \simeq \infty \mathrm{Grpd}(\Pi(X), \infty Grpd_\kappa)
  $$

  of locally constant $\infty$-stacks on $X$ with $\infty$-[[permutation representation]]s of the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|fundamental ∞-groupoid]] of $X$ ([[local system]]s on $X$);

* for every point $x : * \to X$ a natural equivalence of the endomorphisms of the fiber functor $x^*$ and the [[loop space]] of $\Pi(X)$ at $x$

  $$
    End( x^* : LConst(X) \to \infty Grpd ) \simeq \Omega_x \Pi(X)
    \,.
  $$

=--

+-- {: .proof}
###### Proof

The first statement is just the adjunction $(\Pi \dashv Disc)$.

$$
  \begin{aligned}
     LConst(X) & := \mathbf{H}(X, Disc Core \infty Grpd_\kappa)
     \\
     &  \simeq \infty Grpd(\Pi(X), Core \infty Grpd_\kappa)
     \\
     &  \simeq \infty Grpd(\Pi(X), \infty Grpd_\kappa)     
  \end{aligned}
  \,.
$$


Using this and that $\Pi$ preserves the 
[[terminal object in an (∞,1)-category|terminal object]], so that the [[adjunct]] of
$(* \to X \to Disc Core \infty Grpd_\kappa)$ is
$(* \to \Pi(X) \to \infty Grpd_\kappa)$
the second statement follows with an iterated application of the [[(∞,1)-Yoneda lemma]] (this is pure [[Tannaka duality]] as discussed there):

The fiber functor $x^* : Func(\Pi(X), \infty Grpd) \to \infty Grpd$ evaluates an $(\infty,1)$-presheaf on $\Pi(X)^{op}$ at $x \in \Pi(X)$. By the [[(∞,1)-Yoneda lemma]] this is the same as homming out of $j(x)$, where $j : \Pi(X)^{op} \to Func(\Pi(X), \infty Grpd)$ is the [[(∞,1)-Yoneda embedding]]:

$$
  x^* \simeq Hom_{PSh(\Pi(X)^{op})}(j(x), -)
  \,.
$$

This means that $x^*$ itself is a representable object in $PSh(PSh(\Pi(X)^{op})^{op})$. If we denote by $\tilde j : PSh(\Pi(X)^{op})^{op} \to PSh(PSh(\Pi(X)^{op})^{op})$ the corresponding Yoneda embedding, then 

$$
  x^* \simeq \tilde j (j (x))
  \,.
$$

With this, we compute the endomorphisms of $x^*$ by applying the [[(∞,1)-Yoneda lemma]] two more times:

$$
  \begin{aligned}
    End x^*
     & \simeq
    End_{PSh(PSh(\Pi(X)^{op})^{op})} (\tilde j(j (x)))
     \\
     & \simeq
     End(PSh(\Pi(X))^{op}) (j(x))
     \\
     & \simeq
     End_{\Pi(X)^{op}}(x,x)
    \\
     & \simeq
     Aut_x \Pi(X)
    \\
     & =: \Omega_x \Pi(X)
  \end{aligned}
   \,.
$$

=--



### van Kampen theorem {#vanKampenTheorem}

A [[higher homotopy van Kampen theorem|higher]] [[van Kampen theorem]] asserts that passing to [[fundamental ∞-groupoid]]s preserves certain colimits. 

On a cohesive $(\infty,1)$-topos $\mathbf{H}$ the fundamental $\infty$-groupoid functor $\Pi : \mathbf{H} \to \infty Grpd$ is a [[left adjoint]] [[(∞,1)-functor]] and hence preserves all [[(∞,1)-colimit]]s.

More interesting is the question which $(\infty,1)$-colimits of [concrete spaces](#ConcreteObjects) in  

$$
  Conc(\mathbf{H}) 
    \stackrel{\overset{conc}{\leftarrow}}{\underset{inj}{\hookrightarrow}} 
  \mathbf{H}
$$ 

are preserved by $\Pi \circ inj : Conc(\mathbf{H}) \to \infty Grpd$. These colimits are computed by first computing them in $\mathbf{H}$ and then applying the concretization functor. So we have

+-- {: .un_lemma}
###### Observation

Let $U_\bullet : K \to Conc(\mathbf{H})$ be a [[diagram]] such that
the [[(∞,1)-colimit]]
$\lim_\to inj \circ U_\bullet$ is concrete, $\cdots \simeq inj(X)$.

Then the [[fundamental ∞-groupoid]] of $X$ is computed as the $(\infty,1)$-colimit

$$
  \Pi(X) \simeq {\lim_\to} \Pi(U_\bullet)
  \,.
$$


=--


In the [Examples](#Examples) we discuss the cohesive $(\infty,1)$-topos $\mathbf{H} = (\infty,1)Sh(TopBall)$ of [[topological ∞-groupoid]]s For that case we recover the ordinary [[higher van Kampen theorem]]:

+-- {: .un_prop}
###### Proposition

Let $X$ be a [[paracompact space|paracompact]] or [[locally contractible space|locally contractible]] [[topological space]]s and $U_1 \hookrightarrow X$, $U_2 \hookrightarrow X$ a [[covering]] by two [[open subsets]].

Then under the [[singular simplicial complex]] functor $Sing : Top \to $ [[sSet]] we have a [[homotopy pushout]]

$$
  \array{
    Sing(U_1) \cap Sing(U_2) &\to& Sing(U_2)
    \\
    \downarrow && \downarrow
    \\
    Sing(U_1) &\to& Sing(X)
  }
  \,.
$$


=--

+-- {: .proof}
###### Proof

We inject the topological space via the external [[Yoneda embedding]]

$$
  Top \hookrightarrow Sh(TopBalls) \hookrightarrow
  \mathbf{H} := (\infty,1)Sh(OpenBalls)
$$

as a 0-[[truncated]] [[topological ∞-groupoid]] in the cohesive 
$(\infty,1)$-topos $\mathbf{H}$. Being an [[(∞,1)-category of (∞,1)-sheaves]] this is [[locally presentable (∞,1)-category|presented]] by the [[Bousfield localization of model categories|left Bousfield localization]] $Sh(TopBalls, sSet)_{inj,loc}$ of the injective [[model structure on simplicial sheaves]] on $TopBalls$ (as described at [[models for ∞-stack (∞,1)-toposes]]). 

Notice that the injection $Top \hookrightarrow Sh(TopBalls)$ of topological spaces as [[concrete sheaves]] on the site of open balls preserves the pushout $X = U_1 \coprod_{U_1 \cap U_2} U_2$. (This is effectively the statement that $X$ as a [[representable functor|representable]] on [[Diff]] is a [[sheaf]].) Accordingly so does the further inclusion into $Sh(TopBall,sSet) \simeq Sh(TopBalls)^{\Delta^{op}}$ as simplicially constant simplicial sheaves.

Since cofibrations in that model structure are objectwise and degreewise injective maps, it follows that the ordinary [[pushout]] diagram

$$
  \array{
    U_1 \cap U_2 &\to& U_2
    \\
    \downarrow && \downarrow
    \\
    U_1 &\to& X
  }
$$

in $Sh(TopBalls, sSet)_{inj,loc}$ has all objects cofibrant and is the pushout along a cofibration, hence is a [[homotopy pushout]] (as described there). By the general theorem at [[(∞,1)-colimit]] homotopy pushouts model $(\infty,1)$-pushouts, so that indeed $X$ is the $(\infty,1)$-pushout

$$
  X \simeq U_1 \coprod_{U_1 \cap U_2} U_2 \in \mathbf{H}
  \,.
$$

The proposition now follows with the above observation that $\Pi$ preserves all $(\infty,1)$-colimits and with the statement (from [[topological ∞-groupoid]]) that for a topological space (locally contractible or paracompact) we have $\Pi X \simeq Sing X$.

=--




### Paths and geometric Postnikov towers {#Paths}

The [above](#Homotopy) construction of the 
[[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|fundamental ∞-groupoid]] of objects in $\mathbf{H}$ as an object in  [[∞Grpd]] may be reflected back into $\mathbf{H}$, where it gives a notion of homotopy [[path n-groupoid]]s and a geometric notion of [[Postnikov tower]]s of objects in $\mathbf{H}$.

+-- {: .un_def}
###### Definition

For $\mathbf{H}$ a [[locally ∞-connected (∞,1)-topos]]
define the composite [[adjoint (∞,1)-functor]]s

$$
  (\mathbf{\Pi} \dashv \mathbf{\flat}) 
  :=
  (Disc \Pi \dashv Disc \Gamma)
  : 
  \mathbf{H}
   \to 
  \mathbf{H}
  \,.
$$

=--


We say

* $\mathbf{\Pi}(X)$ is the **path $\infty$-groupoid** of $X$ -- the reflection of the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] back into the cohesive context of $\mathbf{H}$;

* $\mathbf{\flat} A$ ("flat $A$") is the coefficient object for 
  **[flat differential A-cohomology](#FlatDifferentialCohomology)** 
  or for $A$-[[local system]]s

Write

$$
  (\tau_n \dashv i_n)
  :
  \mathbf{H}_{\leq n}
  \stackrel{\overset{\tau_{n}}{\leftarrow}}{\underset{i}{\hookrightarrow}}
  \mathbf{H}
$$

for the [[reflective sub-(∞,1)-category]] of [[truncated|n-truncated object]]s and 

$$
  \mathbf{\tau}_n : 
    \mathbf{H} \stackrel{\tau_n}{\to} \mathbf{H}_{\leq n}
  \hookrightarrow
  \mathbf{H}
$$

for the truncation-[[localization of an (∞,1)-category|localization]] funtor. 

We say

$$
  \mathbf{\Pi}_n : \mathbf{H} \stackrel{\mathbf{\Pi}_n}{\to}
   \mathbf{H} \stackrel{\mathbf{\tau}_n}{\to}
  \mathbf{H}
$$

is the **homotopy [[path n-groupoid]]** functor. 

We say that the (truncated) components of the $(\Pi \dashv Disc)$-[[unit of an adjunction|unit]] 

$$
  X \to \mathbf{\Pi}(X)
$$

are the **constant path inclusions**. Dually we have canonical morphism

$$
  \mathbf{\flat}A \to A
  \,.
$$

+-- {: .un_lemma}
###### Observation

If $\mathbf{H}$ is cohesive, then $\mathbf{\flat}$ has a [[right adjoint]] $\mathbf{\Gamma}$

$$
  (\mathbf{\Pi} \dashv \mathbf{\flat} \dashv \mathbf{\Gamma}) 
  :=
  (Disc \Pi \dashv Disc \Gamma \dashv coDisc \Gamma)
  : 
  \mathbf{H}
     \stackrel{\overset{\mathbf{\Pi}}{\to}}{\stackrel{\overset{\mathbf{\flat}}{\leftarrow}}{\underset{\mathbf{\Gamma}}{\to}}}
  \mathbf{H}
  \,.
$$

and this makes $\mathbf{H}$ be $\infty$-connected and locally $\infty$-connected over itself.

=--

+-- {: .un_def}
###### Proposition

Let $\mathbf{H}$ be a [[locally ∞-connected (∞,1)-topos]]. If $X \in \mathbf{H}$ is [[small-projective]] then the [[over-(∞,1)-topos]] $\mathbf{H}/X$ is 

1. [[locally ∞-connected (∞,1)-topos|locally ∞-connected]];

1. [[local (∞,1)-topos|local]].


=--

+-- {: .proof}
###### Proof

The first statement is proven at [[locally ∞-connected (∞,1)-topos]], the second at [[local (∞,1)-topos]].

=--

+-- {: .un_def}
###### Proposition

In a cohesive $(\infty,1)$-topos $\mathbf{H}$, if $X$ is 
[[small-projective]] then so is its path ∞-groupoid $\mathbf{\Pi}(X)$.

=--

+-- {: .proof}
###### Proof

Because of the triple of [[adjoint (∞,1)-functor]]s 
$(\mathbf{\Pi} \dashv \mathbf{\flat} \dashv \mathbf{\Gamma})$ we have for [[diagram]] $A : I \to \mathbf{H}$ that

$$
  \begin{aligned}
     \mathbf{H}(\mathbf{\Pi}(X), {\lim_\to}_i A_i)
     & \simeq 
     \mathbf{H}(X, \mathbf{\flat}{\lim_\to}_i A_i)
    \\
     & \simeq 
     \mathbf{H}(X, {\lim_\to}_i \mathbf{\flat} A_i)
     \\
     & \simeq 
     {\lim_\to}_i \mathbf{H}(X,  \mathbf{\flat} A_i)
  \end{aligned}
  \,,
$$ 

where in the last step we used that $X$ is [[small-projective]] by assumption.

=--



+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ we say that the **geometric Postnikov tower**
of $X$ is the [[Postnikov tower in an (∞,1)-category]] of $\mathbf{\Pi}(X)$:

$$
  \mathbf{\Pi}(X) \to \cdots
   \to 
   \mathbf{\Pi}_2(X) \to \mathbf{\Pi}_1(X) \to \mathbf{\Pi}_0(X)
  \,.
$$

=--


### Universal coverings and geometric Whitehead towers {#Coverings}

We discuss an intrinsic notion of [[Whitehead tower]]s in a [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] [[∞-connected (∞,1)-topos]] $\mathbf{H}$.

+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ a [[pointed object]], the **[[Whitehead tower in an (∞,1)-topos|geometric Whitehead tower]]** of $X$ is the sequence of objects 

$$
  X^{\mathbf{(\infty)}} \to \cdots \to X^{\mathbf{(2)}} \to X^{\mathbf{(1)}} \to X^{\mathbf{(0)}} \simeq X
$$

in $\mathbf{H}$, where for each $n \in \mathbb{N}$ the object $X^{(n+1)}$ is the [[homotopy fiber]] of the canonical morphism $X \to \mathbf{\Pi}_{n+1} X$ to the [path n+1-groupoid](#Paths) of $X$. 

We call $X^{\mathbf{(n+1)}}$ the $(n+1)$-fold 
**[[universal covering space]]** of $X$.

We write $X^{\mathbf{(\infty)}}$ for the homotopy fiber of the untruncated constant path inclusion.

$$
  X^{\mathbf{(\infty)}} \to X \to \mathbf{\Pi}(X)
  \,.
$$

Here the morphisms $X^{\mathbf{(n+1)}} \to X^{\mathbf{n}}$ are those induced from this <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#PushoutPasting">pasting diagram of (∞,1)-pullbacks</a>

$$
  \array{
    X^{\mathbf{(n)}} &\to& *
    \\
    \downarrow && \downarrow
    \\
    X^{\mathbf{(n-1)}} & \to & \mathbf{B}^n \mathbf{\pi}_n(X) &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X &\to& \mathbf{\Pi}_n(X) &\to& \mathbf{\Pi}_{(n-1)}(X)
  }
  \,,
$$

where the object $\mathbf{B}^n \mathbf{\pi}_n(X)$ is defined as the [[homotopy fiber]] of the bottom right morphism.

=--

+-- {: .un_prop}
###### Proposition

Every object $X \in \mathbf{H}$ is covered by objects of the form $X^{\mathbf{(\infty)}}$ for different choices of base points in $X$, in the sense that every $X$ is the [[(∞,1)-colimit]] over a [[diagram]] whose vertices are of this form.

=--

+-- {: .proof}
###### Proof

Consider the diagram

$$
  \array{
    {\lim_\to}_{s \in \Pi(X)} (i^* *)
      &\to& {\lim_\to}_{s \in \Pi(X)} *
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    X &\stackrel{i}{\to}& \mathbf{\Pi}(X)
  }
  \,.
$$

The bottom morphism is the constant path inclusion, the $(\Pi \dashv Disc)$-[[unit of an adjunction|unit]]. The right morphism is the [[equivalence in an (∞,1)-category]] that is the image under $Disc$ of the decomposition ${\lim_\to}_S * \stackrel{\simeq}{\to} S$ of every [[∞-groupoid]] as the [[(∞,1)-colimit]] (see there) over itself of the [[(∞,1)-functor]] constant on the point.

The left morphism is the [[(∞,1)-pullback]] along $i$ of this equivalence, hence itself an equivalence. By [[universal colimits]] in the [[(∞,1)-topos]] $\mathbf{H}$ the top left object is the [[(∞,1)-colimit]] over the single [[homotopy fiber]]s $i^* *_s$  of the form $X^{\mathbf{(\infty)}}$ as indicated. 


=--

+-- {: .un_prop}
###### Proposition

The inclusion $\Pi(i^* *) \to \Pi(X)$ of the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|fundamental ∞-groupoid]] $\Pi(i^* *)$ of each of these objects into $\Pi(X)$ is homotopic to the point.

=--

+-- {: .proof}
###### Proof

We apply $\Pi(-)$ to the above diagram over a single vertex $s$ and attach the $(\Pi \dashv Disc)$-[[unit of an adjunction|counit]] to get

$$
  \array{
    \Pi(i^* *)
      &\to& 
      &\to&
      *
    \\
    \downarrow && && \downarrow 
    \\
    \Pi X &\stackrel{\Pi(i)}{\to}& \Pi Disc \Pi(X)
     &\to& \Pi(X)
  }
  \,.
$$

Then the bottom morphism is an equivalence by the $(\Pi \dashv Disc)$-[[zig-zag-identity]].

=--





### Flat $\infty$-connections and local systems {#FlatDifferentialCohomology}

We describe for a [[locally ∞-connected (∞,1)-topos]] $\mathbf{H}$ a canonical intrinsic notion of _flat_ [[connections on ∞-bundles]], _flat_ [[higher parallel transport]] and higher [[local system]]s.

Write $(\mathbf{\Pi} \dashv\mathbf{\flat}) := (Disc \Pi \dashv Disc \Gamma) : \mathbf{H} \to \mathbf{H}$ for the adjunction given by the [path ∞-groupoid](#Paths). Notice that this comes with the canonical $(\Pi \dashv Disc)$-[[unit of an adjunction|unit]] with components

$$
  X \to \mathbf{\Pi}(X)
$$

and the $(Disc \dashv \Gamma)$-counit with components

$$
  \mathbf{\flat} A \to A
  \,.
$$

+-- {: .un_def}
###### Definition

For $X, A \in \mathbf{H}$ we write

$$
  \mathbf{H}_{flat}(X,A) := \mathbf{H}(\mathbf{\Pi}X, A)
$$

and call $H_{flat}(X,A) := \pi_0 \mathbf{H}_{flat}(X,A)$ the **flat (nonabelian) differential cohomology** of $X$ with coefficients in $A$.

We say a morphism $\nabla : \mathbf{\Pi}(X) \to A$ is a **flat [[connection on an ∞-bundle|∞-connnection]] on the [[principal ∞-bundle]] corresponding to $X \to \mathbf{\Pi}(X) \stackrel{\nabla}{\to} A$, or an **$A$-[[local system]]** on $X$.

The induced morphism

$$
  \mathbf{H}_{flat}(X,A) \to \mathbf{H}(X,A)
$$

we say is the [[forgetful functor]] that forgets flat connections.


=--

+-- {: .un_remark}
###### Remark

The object $\mathbf{\Pi}(X)$ has the interpretation of the [path ∞-groupoid](#Paths) of $X$: it is a cohesive $\infty$-groupoid whose [[k-morphism]]s may be thought of as generated from the $k$-morphisms in $X$ and $k$-dimensional cohesive paths in $X$.

Accordingly a mophism $\mathbf{Pi}(X) \to A$ may be thought of as assigning

* to each point of $X$ a fiber in $A$;

* to each path in $X$ an equivalence between these fibers;

* to each disk in $X$ a  2-equivalalence between these equivaleces associated to its boundary

* and so on.

This we think of as encoding a flat [[higher parallel transport]] on $X$, coming from some flat $\infty$-connection and _defining_ this flat $\infty$-connection.

=--

+-- {: .un_lemma}
###### Observation


By the $(\mathbf{\Pi} \dashv \mathbf{\flat})$-adjunction we have a [[natural transformation|natural]] equivalence

$$
  \mathbf{H}_{flat}(X,A) \simeq \mathbf{H}(X,\mathbf{\flat}A)
  \,.
$$

A [[cocycle]] $g : X \to A$ for a [[principal ∞-bundle]] on $X$ is in the image of 

$$
  \mathbf{H}_{flat}(X,A) \to \mathbf{H}(X,A)
$$

precisely if there is a lift $\nabla$ in the [[diagram]]

$$
  \array{
     && \mathbf{\flat}A 
     \\
     & {}^{\nabla}\nearrow& \downarrow
    \\
    X &\stackrel{g}{\to}& A
  }
  \,.
$$

=--

We call $\mathbf{\flat}A$ the **coefficient object for flat $A$-connections**. 

+-- {: .un_prop}
###### Proposition

For $G := Disc G_0 \in \mathbf{H}$ a [[discrete ∞-groupoid|discrete ∞-group]] the canonical morphism $\mathbf{H}_{flat}(X,\mathbf{B}G) \to \mathbf{H}(X,\mathbf{B}G)$ is an [[equivalence in an (∞,1)-category|equivalence]].

=--

+-- {: .proof}
###### Proof

Since $Disc$ is a [[full and faithful (∞,1)-functor]] we have that the  [[unit of an adjunction|unit]] $Id \to \Gamma Disc $ is a natural equivalence. It follows that on $Disc G_0$ also the counit $Disc \Gamma Disc G_0 \to Disc G_0$ is a weak equivalence (since by the [[triangle identity]] we have that $Disc G_0 \stackrel{\simeq}{\to} Disc \Gamma Disc G_0 \to Disc G_0$ is the identity).

=--

+-- {: .un_remark}
###### Remark

This says that for discrete structure [[∞-group]]s $G$ there is an essentially unique flat $\infty$-connection on any $G$-[[principal ∞-bundle]]. Moreover, the further equivalence

$$
  \mathbf{H}(\mathbf{\Pi}(X), \mathbf{B}G)
  \simeq
  \mathbf{H}_{flat}(X, \mathbf{B}G)
  \simeq
  \mathbf{H}(X, \mathbf{B}G)
$$

may be read as saying that the $G$-principal $\infty$-bundle
is entirely characterized by the flat [[higher parallel transport]]
of this unique $\infty$-connection.

=--


### de Rham cohomology 
  {#deRhamCohomology}

In every [[locally ∞-connected (∞,1)-topos]] $\mathbf{H}$ there is an intrinsic notion of [[nonabelian cohomology|nonabelian]] [[de Rham cohomology]].

+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ an object, write $\mathbf{\Pi}_{dR}X := * \coprod_X \mathbf{\Pi} X$
for the [[(∞,1)-colimit|(∞,1)-pushout]]

$$
  \array{
    X &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}(X) &\to& \mathbf{\Pi}_{dR}X
  }
  \,.
$$

For $* \to A$ any [[pointed object]] in $\mathbf{H}$, write 
$\mathbf{\flat}_{dR} A : * \prod_A \mathbf{\flat}A$ for the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{\flat}_{dR} A &\to& \mathbf{\flat} A 
    \\
    \downarrow && \downarrow
    \\
    * &\to& A
  }
  \,.
$$


=--

+-- {: .un_prop #DeRhamAdjunction}
###### Proposition

This construction yields a pair of [[adjoint (∞,1)-functor]]s 

$$
  (\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR} )
  : 
  */\mathbf{H}
  \stackrel{
     \overset{\mathbf{\Pi}_{dR}}{\leftarrow}
   }{
     \underset{\mathbf{\flat}_{dR}}{\to}
   }
  \mathbf{H}
  \,.
$$


=--

+-- {: .proof}
###### Proof

We check the defining natural hom-equivalence

$$
  {*}/\mathbf{H}(\mathbf{\Pi}_{dR}X,A)
  \simeq
  \mathbf{H}(X, \mathbf{\flat}_{dR}A)
  \,.
$$

The hom-space in the [[over-(∞,1)-category|under-(∞,1)-category]] $*/\mathbf{H}$ is (as discussed there), computed by the [[(∞,1)-pullback]]

$$
  \array{
     */\mathbf{H}(\mathbf{\Pi}_{dR}X, A)
      &\to&
     \mathbf{H}(\mathbf{\Pi}_{dR}X, A)
     \\
     \downarrow && \downarrow
     \\
     * &\stackrel{pt_A}{\to}& \mathbf{H}(*,A)
  }
  \,.
$$

By the fact that the [[hom-functor]]  $\mathbf{H}(-,-) : \mathbf{H}^{op} \times \mathbf{H} \to \infty Grpd $ preserves limits in both arguments we have a natural equivalence

$$
  \begin{aligned}
     \mathbf{H}(\mathbf{\Pi}_{dR} X, A)
     & :=
     \mathbf{H}( *\coprod_{X} \mathbf{\Pi}(X), A  )     
     \\
     & \simeq 
     \mathbf{H}(*,A) \prod_{\mathbf{H}(X,A)} 
      \mathbf{H}(\mathbf{\Pi}(X),A)
  \end{aligned}
  \,.
$$

We paste this pullback to the above pullback diagram to obtain

$$
  \array{
     */\mathbf{H}(\mathbf{\Pi}_{dR}X, A)
      &\to&
     \mathbf{H}(\mathbf{\Pi}_{dR}X, A) &\to&
      \mathbf{H}(\mathbf{\Pi}(X),A)
     \\
     \downarrow && \downarrow  && \downarrow
     \\
     * &\stackrel{pt_A}{\to}& \mathbf{H}(*,A)
     &\to& 
      \mathbf{H}(X,A)
  }
  \,.
$$

By the pasting law for [[(∞,1)-pullback]]s the outer diagram is still a pullback. We may evidently rewrite the bottom composite as in

$$
  \array{
     */\mathbf{H}(\mathbf{\Pi}_{dR}X, A)
      &\to&
      &\to&
      \mathbf{H}(\mathbf{\Pi}(X),A)
     \\
     \downarrow && && \downarrow
     \\
     * &\stackrel{\simeq}{\to}& \mathbf{H}(X,*)
     &\stackrel{(pt_A)_*}{\to}& 
      \mathbf{H}(X,A)
  }
  \,.
$$

This exhibits the hom-space as the pullback

$$
  \begin{aligned}
    */\mathbf{H}(\mathbf{\Pi}_{dR}(X),A)
    \simeq
     \mathbf{H}(X,*) \prod_{\mathbf{H}(X,A)} \mathbf{H}(X,\mathbf{\flat} A)
   \end{aligned}
  \,,
$$

where we used the $(\mathbf{\Pi} \dashv \mathbf{\flat})$-adjunction. Now using again that $\mathbf{H}(X,-)$ preserves pullbacks, this is

$$
  \cdots \simeq \mathbf{H}(X, * \prod_A \mathbf{\flat}A )
  \simeq \mathbf{H}(X , \mathbf{\flat}_{dR}A)
  \,.
$$


=--

+-- {: .un_prop #TripleOfDeRhamAdjunctions}
###### Observation

If $\mathbf{H}$ is also [[local (∞,1)-topos|local]], then there is a further [[right adjoint]] $\mathbf{\Gamma}_{dR}$

$$
  (\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR} \dashv \mathbf{\Gamma}_{dR})
  :
  \mathbf{H}
    \stackrel{\overset{\mathbf{\Pi}_{dR}}{\to}}{\stackrel{\stackrel{\mathbf{\flat}_{dR}}{\leftarrow}}{\underset{\mathbf{\Gamma}_{dR}}{\to}}}
  */\mathbf{H}
$$

given by

$$
  \mathbf{\Gamma}_{dR} X {:=}
    * \coprod_{X} \mathbf{\Gamma}(X)
  \,,
$$

where $(\mathbf{\Pi} \dashv \mathbf{\flat} \dashv \mathbf{\Gamma}) : \mathbf{H} \to \mathbf{H}$ is the triple of adjunctions discussed at [Paths](#Paths).

=--

+-- {: .proof}
###### Proof

This follows by the same kind of argument as above.

=--

+-- {: .un_def}
###### Definition

For $X, A \in \mathbf{H}$ we write

$$
  \mathbf{H}_{dR}(X,A)
  :=
  \mathbf{H}(\mathbf{\Pi}_{dR}X, A)
  \simeq
  \mathbf{H}(X, \mathbf{\flat}_{dR} A)
  \,.
$$

A [[cocycle]] $\omega : X \to \mathbf{\flat}_{dR}A$ we call an **flat $A$-valued differential form** on $X$.

We say that $H_{dR}(X,A) {:=} \pi_0 \mathbf{H}_{dR}(X,A)$
is the **de Rham cohomology** of $X$ with coefficients in $A$.

=--

+-- {: .un_remark}
###### Observation

A [[cocycle]] in de Rham cohomology

$$
  \omega : \mathbf{\Pi}_{dR}X \to A
$$

is precisely a [flat ∞-connetion](#FlatDifferentialCohomology) on a _trivializable_ $A$-principal $\infty$-bundle. More precisely, $\mathbf{H}_{dR}(X,A)$ is the [[homotopy fiber]] of the [[forgetful functor]] from $\infty$-bundles with flat $\infty$-connection to $\infty$-bundles: we have an [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{dR}(X,A) &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}_{flat}(X,A) &\to& \mathbf{H}(X,A)
  }  
  \,.
$$

=--

+-- {: .proof}
###### Proof

This follows by the fact that the [[hom-functor]] $\mathbf{H}(X,-)$ preserves the defining [[(∞,1)-pullback]] for $\mathbf{\flat}_{dR} A$.

=--

Just for emphasis, notice the dual description of this situation: by the [[universal property]] of the [[(∞,1)-colimit]] that defines $\mathbf{\Pi}_{dR} X$ we have that $\omega$ corresponds to a diagram

$$
  \array{
    X &\to& *
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    \mathbf{\Pi}(X) &\stackrel{\omega}{\to}& A
  }
  \,.
$$

The bottom horizontal morphism is a flat connection on the 
$\infty$-bundle given by the cocycle $X \to \mathbf{\Pi}(X) \stackrel{\omega}{\to} A$. The diagram says that this is equivalent to the trivial bundle given by the trivial cocycle $X \to * \to A$.

+-- {: .un_prop #deRhamWithDiscCoeffsIsTrivial}
###### Proposition

The de Rham cohomology with coefficients in discrete objects is trivial: for all $S \in \infty Grpd$ we have

$$
  \mathbf{\flat}_{dR} Disc S \simeq *
  \,.
$$


=--

+-- {: .proof}
###### Proof

Using that in a [[∞-connected (∞,1)-topos]] the functor $Disc$ is a [[full and faithful (∞,1)-functor]] so that the [[unit of an adjunction|unit]] $Id \to \Gamma Disc $ is an [[equivalence in an (∞,1)-category|equivalence]] and using that by the [[zig-zag identity]]  we have then that the [[unit of an adjunction|counit]] component
$\mathbf{\flat} Disc S := Disc \Gamma Disc S \to Disc S$ is also an equivalence, we have


$$
  \begin{aligned}
     \mathbf{\flat}_{dR} Disc S 
     & {:=}
     * \prod_{Disc S} \mathbf{\flat} Disc S
     \\
     & \simeq * \prod_{Disc S} Disc S
     \\
     & \simeq *
  \end{aligned}
  \,,
$$

since the pullback of an equivalence is an equivalence.

=--

+-- {: .un_prop}
###### Proposition

In a cohesive $\mathbf{H}$  _[pieces have points](#PiecesHavePoints)_ precisely if for all $X \in \mathbf{H}$, the de Rham coefficient object $\mathbf{\Pi}_{dR} X $ is
_globally [[connected]]_ in that $\pi_0 \mathbf{H}(*, \mathbf{\Pi}_{dR}X) = *$.

If $X$ has at least one point ($\pi_0(\Gamma X) \neq \emptyset $) 
and is geometrically connected ($\pi_0 (\Pi X) = {*}$) then 
$\mathbf{\Pi}_{\mathrm{dR}}(X)$ is also locally connected: 
$\tau_0 \mathbf{\Pi}_{\mathrm{dR}}X \simeq {*} \in \mathbf{H}$.

=--

+-- {: .proof}
###### Proof

Since $\Gamma$ preserves [[(∞,1)-colimit]]s in a cohesive $(\infty,1)$-topos we have

$$
  \begin{aligned}
    \mathbf{H}(*, \mathbf{\Pi}_{dR}X)
    & \simeq
    \Gamma \mathbf{\Pi}_{dR} X
    \\  
    & \simeq
    * \coprod_{\Gamma X} \Gamma \mathbf{\Pi}X  
    \\
    & \simeq
    * \coprod_{\Gamma X} \Pi X  
  \end{aligned}
  \,,
$$

where in the last step we used that $Disc$ is a [[full and faithful (∞,1)-functor|full and faithful]], so that there is an equivalence $\Gamma \mathbf{\Pi}X := \Gamma Disc \Pi X \simeq \Pi X$.

To analyse this [[(∞,1)-colimit|(∞,1)pushout]] 
we present it by a  [[homotopy pushout]] in 
the standard [[model structure on simplicial sets]] $\mathrm{sSet}_{\mathrm{Quillen}}$. 
Denoting by $\Gamma X$ and $\Pi X$ any representatives in $\mathrm{sSet}_{\mathrm{Quillen}}$ of the objects of the same name in 
$\infty \mathrm{Grpd}$, this may be computed by the ordinary [[pushout]] in [[sSet]]

$$
  \array{
    \Gamma X  &\to& (\Gamma X) \times \Delta[1] \coprod_{\Gamma X} {*}
    \\
    \downarrow && \downarrow
    \\
    \Pi X &\to & Q
  }
  \,,
$$

where on the right we have inserted the [[cone]] on $\Gamma X$ in order to turn the top morphism into a cofibration. From this ordinary pushout it is clear that the connected components of $Q$ are obtained from those of 
$\Pi X$ by identifying all those
in the image of a connected component of $\Gamma X$. So if the left morphism is surjective on
$\pi_0$ then $\pi_0(Q) = *$. This is precisely the condition that 
[pieces have points](#PiecesHavePoints) in $\mathbf{H}$.

For the local analysis we consider the same setup objectwise in the injective [[model structure on simplicial presheaves]]
$[C^{\mathrm{op}}, \mathrm{sSet}]_{\mathrm{inj},\mathrm{loc}}$. 
For any $U \in C$
we then have the pushout $Q_U$ in

$$
  \array{
    X(U) &\to & (X(U)) \times \Delta[1] \coprod_{X(U)} {*}
    \\
    \downarrow && \downarrow
    \\
    \mathrm{sSet}(\Gamma(U), \Pi X) & \to & Q_U
  }
  \,,
$$

as a model for the value of the simplicial presheaf presenting $\mathbf{\Pi}_{\mathrm{dR}}(X)$.
If $X$ is geometrically connected then $\pi_0 \mathrm{sSet}(\Gamma(U), \Pi(X)) = *$
and hence for the left morphism to be surjective on $\pi_0$ it suffices that the top left
object is not empty. Since the simplicial set $X(U)$ contains at least the vertices 
$U \to * \to X$ of which there is by assumption at least one, this is the case.

=--

+-- {: .un_remark}
###### Remark

In summary this means that in a cohesive $(\infty,1)$-topos the objects $\mathbf{\Pi}_{dR} X$ have the abstract properties of [[de Rham schematic homotopy type|pointed geometric de Rham homotopy types]].

In the [Examples](#Examples) we will see that, indeed, the intrinsic de Rham cohomology $H_{dR}(X, A) {:=} \pi_0 \mathbf{H}(\mathbf{\Pi}_{dR} X, A)$ reproduces ordinary de Rham cohomology in degree $d\gt 1$.

In degree 0 the intrinsic de Rham cohomology is necessrily trivial, while in degree 1 we find that it reproduces closed 1-forms, not divided out by exact forms. This difference to ordinary de Rham cohomology in the lowest two degrees may be interpreted in terms of the obstruction-theoretic meaning of de Rham cohomology by which we essentially characterized it above: we have that the intrinsic $H_{dR}^n(X,K)$ is the home for the obstructions to flatness of $\mathbf{B}^{n-2}K$-[[principal ∞-bundle]]s. For $n = 1$ this are groupoid-principal bundles over the _groupoid_ with $K$ as its space of objects. But the 1-form curvatures of groupoid bundles are not to be regarded modulo exact forms. More details on this are at [[circle n-bundle with connection]].

=--


### Exponentiated $\infty$-Lie algebras {#LieAlgebras}


+-- {: .un_def #ExponentiatedLieAsGeometricallyContractible}
###### Definition


For a [[connected]] object $\mathbf{B}\exp(\mathfrak{g}) $ in $\mathbf{H}$ that is _geometrically contractible_

$$
  \Pi (\mathbf{B}\exp(\mathfrak{g})) \simeq *
$$

we call its [[loop space object]] 
$\exp(\mathfrak{g}) := \Omega_* \mathbf{B}\exp(\mathfrak{g})$ the  **[[Lie integration]] of an [[∞-Lie algebra]]** in $\mathbf{H}$. 

=--



+-- {: .un_def}
###### Definition

Set

$$
  \exp Lie
  := 
  \mathbf{\Pi}_{dR} \circ \mathbf{\flat}_{dR} 
  : */\mathbf{H} \to */\mathbf{H}
  \,.
$$

=--

+-- {: .un_prop #LieAsALeftAdjoint}
###### Observation


If $\mathbf{H}$ is cohesive, then $\exp Lie$ is a [[left adjoint]].


=--

+-- {: .proof}
###### Proof

When $\mathbf{H}$ is cohesive we have the [de Rham triple of adjunction](#TripleOfDeRhamAdjunctions) 
$(\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR} \dashv \mathbf{\Gamma}_{dR})$. Accordingly then $Lie$ is part of an [[adjunction]]

$$
  (\exp Lie \dashv \mathbf{\Gamma}_{dR}\mathbf{\flat}_{dR})
  \,.
$$

=--

+-- {: .un_example}
###### Proposition/Example

For all $X$ the object $\mathbf{\Pi}_{dR}(X)$ is geometrically contractible.

=--

+-- {: .proof}
###### Proof

Since on the [[locally ∞-connected (∞,1)-topos]] and [[∞-connected (∞,1)-topos|∞-connected]] $\mathbf{H}$ the functor $\Pi$ preserves [[(∞,1)-colimit]]s and the [[terminal object in an (∞,1)-category|terminal object]], we have

$$
  \begin{aligned}
    \Pi \mathbf{\Pi}_{dR} X
    & {:=}
     \Pi (*) \coprod_{\Pi X} \Pi \mathbf{\Pi} X
    \\
    & \simeq
      * \coprod_{\Pi X} \Pi Disc \Pi X   
    \\
    & \simeq 
      * \coprod_{\Pi X} \Pi X
    & \simeq
      *
  \end{aligned}
  \,,
$$

where we used that in the [[∞-connected (∞,1)-topos|∞-connected]] $\mathbf{H}$ the functor $Disc$ is[[full and faithful (∞,1)-functor|full and faithful]].

=--

+-- {: .un_corollary}
###### Corollary

We have for every $\mathbf{B}G$ that $\exp Lie \mathbf{B}G$ is geometrically contractible.

=--


We shall write $\mathbf{B}\exp(\mathfrak{g})$ for $\exp Lie \mathbf{B}G$, when the context is clear. 


+-- {: .un_prop #LieValuesofDeRham}
###### Proposition


Every [de Rham cocycle](#deRhamCohomology) $\omega : \mathbf{\Pi}_{dR} X \to \mathbf{B}G$ factors through the ∞-Lie algebra of $G$

$$
  \array{
     && \mathbf{B}\exp(\mathfrak{g})
     \\
     & \nearrow & \downarrow
     \\
     \mathbf{\Pi}_{dR}X 
     &\stackrel{\omega}{\to}&
     \mathbf{B}G
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the <a href="http://ncatlab.org/nlab/show/adjoint+functor#UniversalArrows">universality of the counit</a> of $(\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR})$ we have that $\omega$ factors through the [[unit of an adjunction|counit]9 
$\exp Lie \mathbf{B}G \to \mathbf{B}G$. 

=--


Therefore instead of speaking of a $G$-valued de Rham cocycle, it is less  redundant to speak of an $\exp(\mathfrak{g})$-valued de Rham cocycle. In particular we have the following.


+-- {: .un_prop}
###### Corollary

Every morphism $\exp Lie \mathbf{B}H \to \mathbf{B}G$ from an exponentiated $\infty$-Lie algebra to an $\infty$-group factors through the exponentiated $\infty$-Lie algebra of that $\infty$-group

$$
  \array{
    \mathbf{B}\exp(\mathfrak{h}) &\to& \mathbf{B}\exp(\mathfrak{g})
    \\
    & \searrow& \downarrow
    \\
    && \mathbf{B}G
  }
  \,.
$$

=--


+-- {: .un_prop}
###### Proposition

If $\mathbf{H}$ is cohesivem then we have 

$$
  \exp Lie \circ \exp Lie \simeq \exp Lie \circ \Sigma \circ \Omega
  \,.
$$

=--

+-- {: .proof}
###### Proof

First observe that for all $A \in */\mathbf{H}$ we have

$$
  \mathbf{\flat} \mathbf{\flat}_{dR} A \simeq *
$$

This follows using

* $\mathbf{\flat}$ is a [[right adjoint]] and hence preserves [[(∞,1)-pullback]]s;

* $\mathbf{\flat} \mathbf{\flat} := Disc \Gamma Disc \Gamma \simeq Disc \Gamma =: \mathbf{\flat}$ by the fact that $Disc$ is a 
  [[full and faithful (∞,1)-functor]]; 

* the counit $\mathbf{\flat} \mathbf{\flat} A \to \mathbf{\flat} A$ is equivalent to the identity, by the [[zig-zag-identity]] of the [[adjunction]] and using that equivalences satisfy [[category with weak equivalences|2-out-of-3]].

by computing

$$
  \begin{aligned}
    \mathbf{\flat} \mathbf{\flat}_{dR} A
    & 
    * \times_{\mathbf{\flat}A} \mathbf{\flat}\mathbf{\flat}A
    \\
    & \simeq 
    * \times_{\mathbf{\flat}A} \mathbf{\flat}A
    \\
    & \simeq *
 \end{aligned} 
 \,,
$$

using that the [[(∞,1)-pullback]] of an [[equivalence in an (∞,1)-category|equivalence]] is an equivalence.


From this we deduce that

$$
  \mathbf{\flat}_{dR} \circ \mathbf{\flat}_{dR} 
  \simeq \mathbf{\flat}_{dR} \circ \Omega
  \,.
$$

by computing for all $A \in \mathbf{H}$

$$
  \begin{aligned}
    \mathbf{\flat}_{dR} \circ \mathbf{\flat}_{dR} A
    & \simeq 
    * \times_{\mathbf{\flat}_{dR} A} \mathbf{\flat}\mathbf{\flat}_{dR} A
    \\
    & \simeq
    * \times_{\mathbf{\flat}_{dR} A} *
    \\
    & \simeq
    \mathbf{\flat}_{dR}( * \times_A * )
    \\
    & \simeq \mathbf{\flat}_{dR} \Omega A
  \end{aligned}
  \,.
$$

Also observe that by a [proposition above](#deRhamWithDiscCoeffsIsTrivial) we have

$$
  \mathbf{\flat}_{dR} \mathbf{\Pi} X \simeq *
$$

for all $X \in \mathbf{H}$.


Finally to obtain $\exp Lie \circ \exp Lie$ we do one more computation of this sort, using that 

* $\exp Lie := \mathbf{\Pi}_{dR} \mathbf{\flat}_{dR}$ preserves the terminal object (since $\mathbf{H}$ is [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] and [[∞-connected (∞,1)-topos|∞-connected]]) 

* and that it is a [[left adjoint]] by [the above](#LieAsALeftAdjoint), since $\mathbf{H}$ is assumed to be cohesive.

We compute:

$$
  \begin{aligned}
    \exp Lie \exp Lie A 
    & \simeq 
    \exp Lie \mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} A
    \\
    & \simeq
      * 
        \coprod_{\exp Lie \mathbf{\flat}_{dR} A} 
      \exp Lie \mathbf{\Pi} \mathbf{\flat}_{dR} A
    \\
    & \simeq
      * 
        \coprod_{\exp Lie \mathbf{\flat}_{dR} A} 
      \mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} \mathbf{\Pi} \mathbf{\flat}_{dR} A
    \\
    & \simeq 
    * \coprod_{\exp Lie \mathbf{\flat}_{dR} A} *    
    \\
    & \simeq 
    * \coprod_{\mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} \mathbf{\flat}_{dR} A} *
    \\
    & \simeq 
    * \coprod_{\mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} \Omega A} *   
    \\
    & \simeq
    * \coprod_{\exp Lie \Omega A} *   
    \\
    & \simeq
    \exp Lie ( * \coprod_{\Omega A} * )
    \\
    & \simeq
    \exp Lie \Sigma \Omega A  
  \end{aligned} 
  \,.
$$

=--



### Maurer-Cartan forms and curvature characteristic forms      
  {#CurvatureCharacteristics}

In the [intrinsic de Rham cohomology](#deRhamCohomology) of a [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] [[∞-connected (∞,1)-topos|∞-connected]] there exist canonical cocycles that we may identify with [[Maurer-Cartan form]]s and with universal [[curvature characteristic form]]s.

+-- {: .un_def}
###### Definition

For $G \in \mathbf{H}$ an [[∞-group]], write

$$
  \theta : G \to \mathbf{\flat}_{dR} \mathbf{B}G
$$

for the $\mathfrak{g}$-[valued](#LieAlgebras) 
de Rham cocycle on $G$ which is induced by the <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#PushoutPasting">(∞,1)-pullback pasting</a>

$$
  \array{
     G &\to& *
     \\
     {}^{\mathllap{\theta}}\downarrow && \downarrow
     \\
     \mathbf{\flat}_{dR} \mathbf{B}G &\to& \mathbf{\flat}\mathbf{B}G
     \\
     \downarrow && \downarrow
     \\
     * &\to& \mathbf{B}G 
  }
$$

and the [above proposition](#LieValuesofDeRham).

We call $\theta$ the **[[Maurer-Cartan form]]** on $G$.

=--

+-- {: .un_remark}
###### Remark

By postcomposition the Maurer-Cartan form sends $G$-valued functions on $X$ to $\mathfrak{g}$-valued forms on $X$

$$
  \theta_* : \mathbf{H}(X,G) \to 
    \mathbf{H}^1_{dR}(X,G)
  \,.
$$

=--


+-- {: .un_defn #UniversalCurvatureForms}
###### Definition


For $G = \mathbf{B}^n A$ an [[Eilenberg-MacLane object]], we also write 

$$
  curv : \mathbf{B}^n A \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} A
$$

for the intrinsic Maurer-Cartan form and call this the intrinsic **universal [[curvature characteristic form]]** on $\mathbf{B}^n A$.

=--



### Differential cohomology {#DifferentialCohomology}

In every [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] [[∞-connected (∞,1)-topos]] there is an intrinsic notion of [[ordinary differential cohomology]].

Fix a 0-[[truncated]] [[abelian group|abelian]] [[group object]] $A \in \tau_{\leq 0} \mathbf{H} \hookrightarrow \mathbf{H}$. For all $n \in \mathbf{N}$ we have then the [[Eilenberg-MacLane object]] $\mathbf{B}^n A$.

+-- {: .un_def }
###### Definition 

For $X \in \mathbf{H}$ any object and $n \geq 1$ write

$$
  \mathbf{H}_{diff}(X,\mathbf{B}^n A) := 
    \mathbf{H}(X,\mathbf{B}^n A) \prod_{\mathbf{H}_{dR}(X,\mathbf{B}^n A)}
    H_{dR}^{n+1}(X,A)
$$ 

for the cocycle $\infty$-groupoid of [[twisted cohomology]] of $X$ with coefficients in $A$ and with twist given by the canonical [curvature characteristic morphism](#CurvatureCharacteristics) 
$curv : \mathbf{B}^n A \to \mathbf{\flat}_{dR}\mathbf{B}^{n+1} A$. This is the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{diff}(X,\mathbf{B}^n A) 
      &\stackrel{[F]}{\to}& 
     H_{dR}^{n+1}(X,A)
    \\
    {}^{\mathllap{\eta}}\downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}^n A) 
        &\stackrel{curv_*}{\to}& 
     \mathbf{H}_{dR}(X,\mathbf{B}^{n+1} A)
  }
  \,,
$$

where the right vertical morphism $H^{n+1}_{dR}(X) = \pi_0 \mathbf{H}_{dR}(X,\mathbf{B}^{n+1}A)
 \to \mathbf{H}_{dR}(X,\mathbf{B}^{n+1}A)$ is any choice of cocycle representative for each cohomology class: a choice of point in every connected component.

We call

$$
  H_{diff}^n(X,A) {:=} \pi_0 \mathbf{H}_{diff}(X, \mathbf{B}^{n} A)
$$

the degree-$n$ **[[differential cohomology]]** of $X$ with coefficient in $A$.

For $\nabla \in \mathbf{H}_{diff}(X,\mathbf{B}^n A)$ a [[cocycle]], we call

* $[\eta(\nabla)] \in H^n(X,A)$ the class of the **underlying 
   $\mathbf{B}^{n-1} A$-[[principal ∞-bundle]]**;

* $F(\nabla) \in H_{dR}^{n+1}(X,A)$ the **[[curvature]]** class of $c$.


We also say $\nabla$ is an **$\infty$-connection** on $\eta(\nabla)$ (see [below](#ChernWeilTheory)).

=--

+-- {: .un_prop #DiffCohIsWellDefined}
###### Observation

The differential cohomology $H_{diff}^n(X,A)$ does not depend on the choice of morphism $H_{dR}^{n+1}(X,A) \to \mathbf{H}_{dR}(X, \mathbf{B}^{n+1}A)$ (as long as it is an isomorphism on $\pi_0$, as required).
In fact, for different choices the corresponding cocycle [[∞-groupoid]]s $\mathbf{H}_{diff}(X,\mathbf{B}^n A)$ are equivalent.

=--

+-- {: .proof}
###### Proof

The set  

$$
  H_{dR}^{n+1}(X,A) = \coprod_{H_{dR}^{n+1}(X,A)} {*} 
$$ 

is, as a 0-[[truncated]] [[∞-groupoid]], an [[(∞,1)-coproduct]] of the [[terminal object in an (∞,1)-category|terminal object]] in [[∞Grpd]]. By [[universal colimits]] in this [[(∞,1)-topos]] we have that [[(∞,1)-colimit]]s are preserved by [[(∞,1)-pullback]]s, so that $\mathbf{H}_{diff}(X, \mathbf{B}^n A)$ is the coproduct 

$$
  \mathbf{H}_{diff}(X,\mathbf{B}^n A) \simeq
  \coprod_{H_{dR}^{n+1}(X,A)} 
   \left(
   \mathbf{H}(X,\mathbf{B}^n A) 
      \prod_{\mathbf{H}_{dR}(X,\mathbf{B}^{n+1}A)} 
    {*}
  \right)
$$

of the [[homotopy fiber]]s of $curv_*$ over each of the chosen points $* \to \mathbf{H}_{dR}(X,\mathbf{B}^{n+1}A)$. These homotopy fibers only  depend, up to equivalence, on the connected component over which they are taken.

=--

+-- {: .un_prop #DiffCohomologyRestrictedToVanishingCurvature}
###### Proposition

When restricted to vanishing curvature, differential cohomology coincides with [flat differential cohomology](#FlatDifferentialCohomology):

$$
  H_{diff}^n (X,A)|_{[F] = 0} \simeq H_{flat}(X,\mathbf{B}^n A)
  \,.
$$

Moreover this is true at the level of [[cocycle]] [[∞-groupoid]]s

$$
 \left(
  \mathbf{H}_{diff}(X, \mathbf{B}^n A) 
    \prod_{H_{dR}^{n+1}(X,A)} \{[F] = 0\}
  \right)
  \simeq
  \mathbf{H}_{flat}(X,\mathbf{B}^n A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-pullback#QuasiCatPastingLaw">pasting law for (∞,1)-pullbacks</a> the claim is equivalently that we have a an $(\infty,1)$-pullback diagram

$$
  \array{
    \mathbf{H}_{flat}(X, \mathbf{B}^n A) &\to& {*}
    \\
    \downarrow && \downarrow^{\mathrlap{\{[F] = 0\}}}
    \\
    \mathbf{H}_{diff}(X,\mathbf{B}^n A) &\stackrel{[F]}{\to}& 
     H_{dR}^{n+1}(X,A)
    \\
    {}^{\mathllap{\eta}}\downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}^n A) 
        &\stackrel{curv_*}{\to}& 
     \mathbf{H}_{dR}(X,\mathbf{B}^{n+1} A)
  }
  \,.
$$

By definition of flat cohomology and of intrinsic de Rham cohomology
in $\mathbf{H}$, the outer rectangle is 

$$
  \array{
    \mathbf{H}(X,\mathbf{\flat}\mathbf{B}^n A) &\to& {*}
    \\ 
    \downarrow && \downarrow 
    \\
    \mathbf{H}(X, \mathbf{B}^n A) 
      &\stackrel{curv_*}{\to}&
    \mathbf{H}(X, \mathbf{\flat}_{dR}\mathbf{B}^{n+1} A)
  }
  \,.
$$

Since the [[hom-functor]] $\mathbf{H}(X,-)$ preserves [[(∞,1)-limit]]s this is a pullback if

$$
  \array{
    \mathbf{\flat} \mathbf{B}^n A &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}^n A 
      &\stackrel{curv}{\to}& 
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1} A
  }
$$

is. Indeed, this is one step in the [[fiber sequence]] 

$$
   \cdots
   \to 
   \mathbf{\flat} \mathbf{B}^n A
   \to
   \mathbf{B}^n A
   \stackrel{curv}{\to}
   \mathbf{\flat}_{dR} \mathbf{B}^{n+1}A
  \to
  \mathbf{\flat} \mathbf{B}^{n+1} A
   \to
  \mathbf{B}^{n+1} A
$$

that [defines](#CurvatureCharacteristics) $curv$ (using that $\mathbf{\flat}$ preserves limits and hence looping and delooping)


=--

+-- {: .un_prop}
###### Proposition

The differential cohomology group $H_{diff}^n(X,A)$ fits into a [[short exact sequence]] of [[abelian group]]s

$$
  0 
   \to 
  H_{dR}^n(X,A)/H^{n-1}(X,A) 
   \to 
  H_{diff}^n(X,A) 
   \to 
  H^n(X,A)
   \to 
  0
  \,.
$$

=--


+-- {: .proof}
###### Proof

This is a general statement about the definition of [[twisted cohomology]].
We claim that for all $n \geq 1$ we have a [[fiber sequence]]

$$
  \mathbf{H}(X, \mathbf{B}^{n-1}A)
  \to 
  \mathbf{H}_{dR}(X, \mathbf{B}^n A)
  \to 
  \mathbf{H}_{diff}(X, \mathbf{B}^n A)
  \to
  \mathbf{H}(X, \mathbf{B}^n A)
$$

in [[∞Grpd]]. This implies the [[short exact sequence]] using that 
by construction the last morphism is surjective on connected components (because in the defining $(\infty,1)$-pullback for $\mathbf{H}_{diff}$ the right vertical morphism is by assumption surjective on connected components).

To see that we do have the fiber sequence as claimed consider the 
pasting composite of [[(∞,1)-pullback]]s

$$
  \array{
    \mathbf{H}_{dR}(X,\mathbf{B}^{n-1} A) 
    &\to& 
      \mathbf{H}_{diff}(X,\mathbf{B}^n A)  
    &\to& 
     H_{dR}(X, \mathbf{B}^{n+1} A)
    \\
    \downarrow && \downarrow && \downarrow
    \\
    {*} 
      &\to& 
    \mathbf{H}(X, \mathbf{B}^n A) 
      &\stackrel{curv}{\to}&
    \mathbf{H}_{dR}(X, \mathbf{B}^{n+1} A)
  }
  \,.
$$

The square on the right is a pullback by the above definition.
Since also the square on the left is assumed to be an $(\infty,1)$-pullback
it follows by the <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-pullback#QuasiCatPastingLaw">pasting law for (∞,1)-pullbacks</a> that the top left object is
the $(\infty,1)$-pullback of the total rectangle diagram. 
That total diagram is 

$$
  \array{
    \Omega \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B}^{n+1}A) 
    &\to& 
     H(X,\mathbf{\flat}_{dR} \mathbf{B}^{n+1} A)
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{H}(X,\mathbf{\flat}_{dR} \mathbf{B}^{n+1} A)
  }
  \,,
$$

because, as before, this $(\infty,1)$-pullback is the coproduct of the 
homotopy fibers, and they are empty over the connected components not
in the image of the bottom morphism and are the [[loop space object]]
over the single connected component that is in the image. 

Finally using that (as discussed at [[cohomology]] and at [[fiber sequence]]) 
$$
  \Omega \mathbf{H}(X,\mathbf{\flat}_{dR} \mathbf{B}^{n+1}A) 
    \simeq 
   \mathbf{H}(X,\Omega \mathbf{\flat}_{dR} \mathbf{B}^{n+1}A)
$$ 

and

$$ 
  \Omega \mathbf{\flat}_{dR} \mathbf{B}^{n+1}A 
    \simeq 
   \mathbf{\flat}_{dR} \Omega \mathbf{B}^{n+1}A
$$

since both $\mathbf{H}(X,-)$ as well as $\mathbf{\flat}_{dR}$
preserve [[(∞,1)-limit]]s and hence formation of [[loop space object]]s,
the claim follows.


=--


+-- {: .un_remark}
###### Remark

This is essentially the short exact sequence whose form is familiar from the traditional definition of [[ordinary differential cohomology]] only up to the following slight nuances in notation:

1.  The cohomology groups of the short exact sequence above denote the groups obtained in the given [[(∞,1)-topos]] $\mathbf{H}$, not in [[Top]]. Notably for $\mathbf{H} = $ [[?LieGrpd]], $A = U(1) =\mathbb{R}/\mathbb{Z}$
the [[circle group]] and $|X| \in Top$ the geometric realization of a paracompact manifold $X$, we have that $H^n(X,\mathbb{R}/\mathbb{Z})$ above is $H^{n+1}_{sing}({|\Pi X|},\mathbb{Z})$. 

1. The fact that on the left  of the short exact sequence for differential cohomology we have the de Rham cohomology set $H_{dR}^n(X,A)$ instead of 
something like the set of all flat forms as familiar from 
[[ordinary differential cohomology]] is because the latter has no
intrinsic meaning but depends on a choice of model. 
After fixing a specific
[[presentable (∞,1)-category|presentation]] of $\mathbf{H}$ 
by a [[model category]] $C$ we can
consider instead of 
$H_{dR}^{n+1}(X,A) \to \mathbf{H}_{dR}(X, \mathbf{B}^{n+1}A)$ 
the inclusion of the set of objects 
$\Omega_{cl}^{n+1}(X,A) {:=} \mathbb{R}Hom_C(X, \mathbf{B}^{n+1}A )_0
\hookrightarrow \mathbb{R}Hom_C(X, \mathbf{B}^{n+1}A )$. However,
by the [above observation](#DiffCohIsWellDefined) this 
only adds multiple copies of the homotopy types of the connected 
components of $\mathbf{H}_{diff}(X, \mathbf{B}^n A)$.

=--




### Chern-Weil homomorphism and $\infty$-connections {#ChernWeilTheory}

Induced by the [intrinsic differential cohomology](#DifferentialCohomology) in any [[∞-connected (∞,1)-topos|∞-connected]] and [[locally ∞-connected (∞,1)-topos]] is an intrinsic notion of [[Chern-Weil homomorphism]].

Let $A$ be the chosen abelian [[∞-group]] as [above](#DifferentialCohomology). Recall the [universal curvature characteristic class](#CurvatureCharacteristics)

$$
  curv : \mathbf{B}^n A \to \mathbf{\flat}_{dR}\mathbf{B}^{n+1}A
$$

for all $n \geq 1$.

+-- {: .un_def}
###### Definition


For $G$ an [[∞-group]] and 

$$
  \mathbf{c} : \mathbf{B}G \to \mathbf{B}^n A
$$

a representative of a [[characteristic class]] $[\mathbf{c}] \in H^n(\mathbf{B}G, A)$ we say that the composite

$$
  \mathbf{c}_{dR} : \mathbf{B}G \stackrel{\mathbf{c}}{\to}
    \mathbf{B}^n A 
     \stackrel{curv}{\to}
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1} A
$$

represents the corresponding [[differential characteristic class]] or **[[curvature characteristic class]]** 
$[\mathbf{c}_{dR}] \in H_{dR}^{n+1}(\mathbf{B}G, A)$.

The induced map on cohomology

$$
  (\mathbf{c}_{dR})_* 
   : 
  H^1(-,G)
  \to
  H^{n+1}_{dR}(-,A)
$$

we call the (unrefined) **[[∞-Chern-Weil homomorphism]]** induced by $\mathbf{c}$.

=--

The following construction universally lifts the 
$\infty$-Chern-Weil homomorphism from taking values in 
[intrinsic de Rham cohomology](#deRhamCohomology) 
to values in [intrinsic differential cohomology](#DifferentialCohomology).


+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ any object, define the [[∞-groupoid]] $\mathbf{H}_{conn}(X,\mathbf{B}G)$ as the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{conn}(X, \mathbf{B}G) 
     &\stackrel{(\hat \mathbf{c}_i)_i}{\to}& 
     \prod_{[\mathbf{c}_i] \in H^{n_i}(\mathbf{B}G,A); i \geq 1} 
     \mathbf{H}_{diff}(X,\mathbf{B}^{n_i} A)
   \\
   {}^{\mathllap{\eta}}\downarrow && \downarrow
   \\
   \mathbf{H}(X, \mathbf{B}G) 
     &\stackrel{( \mathbf{c}_i)_i}{\to}& 
     \prod_{[\mathbf{c}_i] \in H^{n_i}(\mathbf{B}G,A); i \geq 1} 
   \mathbf{H}(X,\mathbf{B}^{n_i} A)
  }
 \,.
$$

We say 

* a cocycle in $\nabla \in \mathbf{H}_{conn}(X, \mathbf{B}G)$ is an [[connection on an ∞-bundle|∞-connection]] 

* on the [[principal ∞-bundle]] $\eta(\nabla)$;

* a morphism in $\mathbf{H}_{conn}(X, \mathbf{B}G)$ is a [[gauge transformation]] of connections;

* for each $[\mathbf{c}] \n H^n(\mathbf{B}G, A)$ the morphism

  $$
    [\hat \mathbf{c}] :  H_{conn}(X,\mathbf{B}G) \to H_{diff}^n(X, A)
  $$

  is the (full/refined) **[[∞-Chern-Weil homomorphism]]** induced
  by the [[characteristic class]] $[\mathbf{c}]$.

=--

+-- {: .un_prop}
###### Observation

Under the [[curvature]] projection $[F] : H_{diff}^n (X,A) \to H_{dR}^{n+1}(X,A)$ the refined Chern-Weil homomorphism for $\mathbf{c}$ projects to the unrefined Chern-Weil homomorphism.

=--

+-- {: .proof}
###### Proof

This is due to the existence of the pasting composite

$$
  \array{
    \mathbf{H}_{conn}(X, \mathbf{B}G) 
     &\stackrel{(\hat \mathbf{c}_i)_i}{\to}& 
     \prod_{[\mathbf{c}_i] \in H^{n_i}(\mathbf{B}G,A); i \geq 1} 
     \mathbf{H}_{diff}(X,\mathbf{B}^{n_i} A)
    &\stackrel{[F]}{\to}&
     \prod_{[\mathbf{c}_i] \in H^{n_i}(\mathbf{B}G,A); i \geq 1} 
     H_{dR}^{n_i+1}(X,A)
   \\
   {}^{\mathllap{\eta}}\downarrow && \downarrow && \downarrow
   \\
   \mathbf{H}(X, \mathbf{B}G) 
     &\stackrel{(\mathbf{c}_i)_i}{\to}& 
     \prod_{[\mathbf{c}_i] \in H^{n_i}(\mathbf{B}G,A); i \geq 1} 
   \mathbf{H}(X,\mathbf{B}^{n_i} A)
    &\stackrel{curv_*}{\to}&
     \prod_{[\mathbf{c}_i] \in H^{n_i}(\mathbf{B}G,A); i \geq 1} 
    \mathbf{H}_{dR}(X, \mathbf{B}^{n_i+1},A)
  }
$$

of the defining $(\infty,1)$-pullback for $\mathbf{H}_{conn}(X,\mathbf{B}G)$ with the products of the defining
$(\infty,1)$-pullbacks for the $\mathbf{H}_{diff}(X, \mathbf{B}^{n_i}A)$.

=--


### Higher holonomy and Chern-Simons functional 
  {#ChernSimonsTheory}

The notion of [intrinsic ∞-connections](#ChernWeilTheory) in a 
cohesive $(\infty,1)$-topos induces a notion of [[higher parallel transport|higher holonomy]] and [[Chern-Simons theory|Chern-Simons functionals]].


+-- {: .un_prop}
###### Definition

We say an object $\Sigma \in \mathbf{H}$ has **[[cohomological dimension]]** $\leq n \in \mathbb{N}$ if for all $n$-[[connected]] coefficient objects  and $(n++1)$-[[truncated]] objects $\mathbf{B}^{n+1}A$ the corresponding cohomology on $\Sigma$ is trivial

$$
  H(\Sigma, \mathbf{B}^{n+1}A ) \simeq *
  \,.
$$

Let $dim(\Sigma)$ be the maximum $n$ for which this is true.

=--



+-- {: .un_prop}
###### Observation

If $\Sigma$ has [[cohomological dimension]] $\leq n$ then its  [intrinsic de Rham cohomology](#deRhamCohomology) vanishes in degree $k \gt n$

$$
  H_{dR}^{k \gt n}(\Sigma, A) \simeq *
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since $\mathbf{\flat}$ is a [[right adjoint]] it preserves [[delooping]] and hence $\mathbf{\flat} \mathbf{B}^k A \simeq \mathbf{B}^k \mathbf{\flat}A$. It follows that 

$$
  \begin{aligned}
     H_{dR}^{k}(\Sigma,A)
     & :=
     \pi_0 \mathbf{H}(\Sigma, \mathbf{\flat}_{dR} \mathbf{B}^k A)
    \\
    & \simeq
     \pi_0 \mathbf{H}(\Sigma, * \prod_{\mathbf{B}^k A} \mathbf{B}^k \mathbf{\flat}A)
    \\
    & \simeq
    \pi_0
     \left( 
     \mathbf{H}(\Sigma,*) \prod_{\mathbf{H}(\Sigma, \mathbf{B}^k A)}
      \mathbf{H}(\Sigma, \mathbf{B}^k \mathbf{\flat}A)
     \right)
   \\
   & \simeq
    \pi_0 (*)
  \end{aligned}
  \,.
$$

=--

Let now again $A$ be fixed as [above](#DifferentialCohomology).

+-- {: .un_def}
###### Definition

Let $\Sigma \in \mathbf{H}$, $n \in \mathbf{N}$ with
$dim \Sigma \leq n$. 
  
We say that the composite

$$
  \int_\Sigma 
  : 
  \mathbf{H}_{flat}(\Sigma, \mathbf{B}^n A)
   \stackrel{\simeq}{\to}
  \infty Gprd(\Pi(\Sigma), \Pi(\mathbf{B}^n A))
   \stackrel{\tau_{\leq n-dim(\Sigma)}}{\to}
  \tau_{n-dim(\Sigma)}
    \infty Gprd(\Pi(\Sigma), \Pi(\mathbf{B}^n A))
$$ 

of the [[adjunction]] equivalence followed by [[truncated|truncation]] is the **flat holonomy** operation on flat $\infty$-connections.

More generally, let

* $\nabla \in \mathbf{H}_{diff}(X, \mathbf{B}^n A)$ be a differential coycle on some $X \in \mathbf{H}$

* $\phi : \Sigma \to X$ a morphism.

Write

$$
  \phi^* : \mathbf{H}_{diff}(X, \mathbf{B}^{n+1} A) 
    \to 
  \mathbf{H}_{diff}(\Sigma, \mathbf{B}^n A)
   \simeq
  \mathbf{H}_{flat}(\Sigma, \mathbf{B}^n A)
$$

(using the [above proposition](#DiffCohomologyRestrictedToVanishingCurvature)) 
for the morphism on $(\infty,1)$-pullbacks induced by the morphism of diagrams

$$
  \array{  
     \mathbf{H}(X, \mathbf{B}^n A) &\to&
     \mathbf{H}_{dR}(X, \mathbf{B}^{n+1} A)
     &\leftarrow&
     H_{dR}^{n+1}(X, A)
     \\
     \downarrow^{\mathrlap{\phi^*}}
     &&
     \downarrow^{\mathrlap{\phi^*}}
     &&
     \downarrow
     \\
     \mathbf{H}(\Sigma, \mathbf{B}^n A) &\to&
     \mathbf{H}_{dR}(X, \mathbf{B}^{n+1} A)
     &\leftarrow&
     *     
  }
$$


The **[[higher parallel transport|holonomomy]]** of $\nabla$ over $\sigma$ is the flat holonomy of $\phi^* \nabla$

$$
  \int_\phi \nabla := \int_{\Sigma} \phi^* \nabla
  \,.
$$ 

=--

+-- {: .un_def}
###### Definition

Let $\Sigma \in \mathbf{H}$ be of [[cohomological dimension]] $dim\Sigma = n \in \mathbb{N}$ and let $\mathbf{c} : X \to \mathbf{B}^n A$ a representative of a [[characteristic class]] $[\mathbf{c}] \in H^n(X, A)$ for some object $X$. We say that the composite

$$
  \exp(S_{\mathbf{c}}(-))
  : 
  \mathbf{H}(\Sigma, X)
   \stackrel{\hat \mathbf{c}}{\to}
  \mathbf{H}_{diff}(\Sigma, \mathbf{B}^n A)
   \stackrel{\simeq}{\to}
  \mathbf{H}_{flat}(\Sigma, \mathbf{B}^n A)
   \stackrel{\int_\Sigma}{\to}
  \tau_{\leq 0}
    \infty Grpd(\Pi(\Sigma), \Pi \mathbf{B}^n A)
$$

where $\hat \mathbf{c}$ denotes the [refined Chern-Weil homomorphism](#ChernWeilTheory) induced by $\mathbf{c}$,
is the **[[schreiber:∞-Chern-Simons theory|extended Chern-Simons functional]]** induced by $\mathbf{c}$ on $\Sigma$.

=--

+-- {: .un_def}
###### Remark

In the language of [[sigma-model]] [[quantum field theory]] the ingredients of this definition have the following interpretation

* $\Sigma$ is the _worldvolume of a fundamental $(dim\Sigma-1)$-[[brane]]_ ;

* $X$ is the target space;

* $\hat \mathbf{c}$ is the background [[gauge field]] on $X$;

* $\mathbf{H}_{conn}(\Sigma,X)$ is the space of _worldvolume field configurations_ $\phi : \Sigma \to X$ or _trajectories_ of the brane in $X$;

* $\exp(S_{\mathbf{c}}(\phi)) =  \int_\Sigma \phi^* \hat \mathbf{c}$ is the value of the [[action functional]] on the field configuration $\phi$.

=--

In suitable situations this construction refines to an internal construction.

Assume that $\mathbf{H}$ has a canonical [[line object]] $\mathbb{A}^1$ and a [[natural numbers object]] $\mathbb{Z}$. Then the [[action functional]] $\exp(i S(-))$ may lift to the [[internal hom]] with respect to the canonical <a href="http://ncatlab.org/nlab/show/(infinity,1)-topos#ClosedMonoidalStructure">cartesian closed monoidal structure</a> on any [[(∞,1)-topos]] to a morphism of the form

$$
  \exp(i S_{\mathbf{c}}(-)) : [\Sigma,\mathbf{B}G_{conn}] \to 
  \mathbf{B}^{n-dim \Sigma}\mathbb{A}^1/\mathbb{Z}
  \,.
$$

We call $[\Sigma, \mathbf{B}G_{conn}]$ the [[configuration space]] of the [[schreiber:∞-Chern-Simons theory]] defined by $\mathbf{c}$ and $\exp(i S_\mathbf{c}(-))$ the [[action functional]] in [[codimension]] 
$(n-dim\Sigma)$ defined on it. 

See [[schreiber:∞-Chern-Simons theory]] for more discussion.


##  Infinitesimal cohesion   
  {#InfinitesimalCohesion}

We discuss [[extra structure]] on a cohesive $(\infty,1)$-topos
that encodes a refinement of the corresponding notion of cohesion to 
_infinitesimal cohesion_ . More precisely, we consider inclusions
$\mathbf{H} \hookrightarrow \mathbf{H}_{th}$ of cohesive 
$(\infty,1)$-toposes that exhibit the objects of $\mathbf{H}_{th}$
as infinitesimal cohesive neighbourhoods of objects in 
$\mathbf{H}$.


+-- {: .un_defn #InfinitesimalCohesiveInfTopos}
###### Definition

Given a cohesive $(\infty,1)$-topos $\mathbf{H}$ we say that 
an **infinitesimal cohesive neighbourhood** of $\mathbf{H}$
is another cohesive $(\infty,1)$-topos $\mathbf{H}_{th}$
equipped with a quadruple of [[adjoint (∞,1)-functor]]s

$$
  (i_! \dashv i^* \dashv i_* \dashv i^!) : 
  \mathbf{H}
    \stackrel{\overset{i_!}{\hookrightarrow}}{\stackrel{\overset{i^*}{\leftarrow}}{\stackrel{\overset{i_*}{\hookrightarrow}}{\underset{i^!}{\leftarrow}}}}
  \mathbf{H}_{th}
$$

where $i_!$ is 

* a [[full and faithful (∞,1)-functor]] 

* that preserves the [[terminal object in an (∞,1)-category|terminal object]].

=--

This definition is an abstraction of similar situations considered in ([SimpsonTeleman](#SimpsonTeleman)) and in [Kontsevich-Rosenberg](#KontsevichRosenbergSpaces). See also the section <a href="http://nlab.mathforge.org/nlab/show/Q-category#InfinitesimalThickening">Infinitesimal thickenings</a> at [[Q-category]].

+-- {: .un_prop #InfinitesimalInclusionIfFullAndFaithful}
###### Observation

This implies that also $i_*$ is a [[full and faithful (∞,1)-functor]].

=--

+-- {: .proof}
###### Proof

By the characterizaton of full and faithful [[adjoint (∞,1)-functor]]s 
the condition on $i_!$ is equivalent to $i^* i_! \simeq Id$. Since $(i^* i_! \dashv i^* i_*)$ it follows by essential uniqueness of [[adjoint (∞,1)-functor]]s that also $i^* i_* \simeq Id$.

=--

+-- {: .un_remark}
###### Remark

This definition captures the characterization of an [[infinitesimal object]] as having a single [[global element|global point]] surrounded by an infinitesimal neighbourhood: as we shall see in more detail [below](#InfinitesimalPathsAndReduction), the [[(∞,1)-functor]] $i^*$ may be thought of as contracting away any infinitesimal extension of an object. Thus $X$ being an [infinitesimal object](#InfinitesimalObject) amounts to  $i^* X \simeq *$, and the [[adjoint (∞,1)-functor|(∞,1)-adjunction]] $(i_! \dashv i^*)$ then indeed guarantees that $X$ has only a single global point, since 

$$
  \begin{aligned}
    \mathbf{H}_{th}(*, X) 
      & \simeq \mathbf{H}_{th}(i_! *, X) 
      \\
      & \simeq \mathbf{H}(*, i^* X)
      \\
      & \simeq \mathbf{H}(*, *)
      \\
      & \simeq *
 \end{aligned}
  \,.
$$

=--

+-- {: .un_prop #InfinitesimalNeighbourhoodIsOverInfGroupoid}
###### Observation

The inclusion into the infinitesimal neighbourhood is necessarily
a morphism of [[(∞,1)-topos]]es over [[∞Grpd]].

$$
  \array{
     \mathbf{H} && \stackrel{(i^* \dashv i_*)}{\to} && \mathbf{H}_{th}
     \\
     & {}_{\mathllap{\Gamma}}\searrow && \swarrow_{\mathrlap{\Gamma}}
     \\
     && \infty Grpd 
  }
$$

as is the induced geometric morphism
$(i_* \dashv i^!) : \mathbf{H}_{th} \to \mathbf{H}$

$$
  \array{
     \mathbf{H}_{th} && \stackrel{(i_* \dashv i^!)}{\to} 
      && \mathbf{H}
     \\
     & {}_{\mathllap{\Gamma}}\searrow && \swarrow_{\mathrlap{\Gamma}}
     \\
     && \infty Grpd 
  }
  \,.
$$

Moreover $i_*$ is necessarily a [[full and faithful (∞,1)-functor]].

=--

+-- {: .proof}
###### Proof

By essential uniqueness of th [[global section]] [[geometric morphism]]:
In both cases the [[direct image]] functor has as [[left adjoint]]
that preserves the [[terminal object]]. Therefore

$$
  \begin{aligned}
    \Gamma_{\mathbf{H}_{th}}( i_* X )
    & 
    \simeq
    \mathbf{H}_{th}(*, i_* X)
    \\
    & \simeq \mathbf{H}(i^* *, X)
    \\
    & 
    \simeq \mathbf{H}(*, X)
    \\
    & \simeq \Gamma_{\mathbf{H}}(X)
  \end{aligned}
  \,.
$$

Analogously in the second case.

=--


We shall write 

$$
  (\Pi_{inf} \dashv Disc_{inf} \dashv \Gamma_{inf})
  := 
  (i^* \dashv i_* \dashv i^!)
$$

so that the [[global section]] geometric moprhism of $\mathbf{H}_{th}$ factors as

$$
  (\Pi_{\mathbf{H}_{th}} \dashv Disc_{\mathbf{H}_{th}} \dashv \Gamma_{\mathbf{H}_{th}})
  :
  \mathbf{H}_{th}
  \stackrel{\overset{\Pi_{inf}}{\to}}{\stackrel{\overset{Disc_{inf}}{\leftarrow}}{\underset{\Gamma_{inf}}{\to}}}
  \mathbf{H}
  \stackrel{\overset{\Pi_{\mathbf{H}}}{\to}}{\stackrel{\overset{Disc_{\mathbf{H}}}{\leftarrow}}{\underset{\Gamma_{\mathbf{H}}}{\to}}}
  \infty Grpd
  \,.
$$


Let for the remainder of this section an infinitesimal neighbourhood $\mathbf{H} \hookrightarrow \mathbf{H}_{th}$ be fixed.


### Properties

+-- {: .un_def #InfinitesimalNeighBourhoodSite}
###### Definition

Let $C$ be an [[∞-cohesive site]]. We say a [[site]] $C_{th}$ 

* equipped with a [[coreflective subcategory|coreflective embedding]]

  $$
    (i \dashv p) : 
     C \stackrel{\overset{i}{\hookrightarrow}}{\underset{p}{\leftarrow}}
    C_{th}
  $$

* such that 

  * $i$ preserves [[pullback]]s along morphisms in [[covering]] families;

  * both $i$ and $p$ send [[covering]] families to covering families;

  * for all $\mathbf{U}$ in $C_{th}$ and covering families $\{U_i \to p(\mathbf{U})\}$ there is a lift through $p$ to a covering family $\{\mathbf{U}_i \to \mathbf{U}\}$

is an **infinitesimal neighbourhood site** of $C$.

=--


+-- {: .un_prop #InfinitesimalNeighbourhoodFromInfinitesimalSite}
###### Proposition

Let $C$ be an [[∞-cohesive site]] and  $(i \dashv p) : C \stackrel{\overset{i}{\hookrightarrow}}{\underset{p}{\leftarrow}} C_{th}$ an [infinitesimal neighbourhood site](#InfinitesimalNeighBourhoodSite). 

Then the [[(∞,1)-category of (∞,1)-sheaves]] on $C_{th}$ is a cohesive $(\infty,1)$-topos and the restriction $i^*$ along $i$ exhibits it as an [infinitesimal neighbourhood](#InfinitesimalNeighbourhoodIsOverInfGroupoid) of the cohesive $(\infty,1)$-topos over $C$.

$$
 ( i_! \dashv i^* \dashv i_* \dashv i^! )
  :
  Sh_{(\infty,1)}(C)
  \stackrel{\overset{i_!}{\hookrightarrow}}{\stackrel{\overset{i^*}{\leftarrow}}{\stackrel{\overset{i_*}{\to}}{\stackrel{i^!}{\leftarrow}}}}
  Sh_{(\infty,1)}(C^{th})
  \,.
$$

Moreover, $i_!$ restricts on representables to the [[(∞,1)-Yoneda embedding]] factoring through $i$:

$$
  \array{
    C &\hookrightarrow& Sh_{(\infty,1)}(C)
    \\
    \downarrow^{\mathrlap{i}} && \downarrow^{\mathrlap{i_!}}
    \\
    C_{th} &\hookrightarrow& Sh_{(\infty,1)}(C_{th})
  }
  \,.
$$


=--

+-- {: .proof}
###### Proof

We [[presentable (∞,1)-category|present]] the [[(∞,1)-sheaf (∞,1)-category]] $Sh_{(\infty,1)}(C_{th})$ by the projective [[model structure on simplicial presheaves]] [[Bousfield localization of model categories|left Bousfield localized]] at the [[covering]] [[sieve]] inclusions 

$$
  Sh_{(\infty,1)}(C_{th}) \simeq
  ([C_{th}^{op}, sSet]_{loc})^\circ
$$

(as discussed at [[models for ∞-stack (∞,1)-toposes|models for (∞,1)-sheaf (∞,1)-toposes]]).


Consider the right [[Kan extension]] $Ran_i : [C^{op}, sSet] \to [C_{th}^{op},sSet]$ of [[simplicial presheaves]] along the functor $i$. On an object $K \times D \in C_{th}$ it is given by the [[end]]-expression

$$
  \begin{aligned}
    \mathrm{Ran}_{i} F : \mathbf{K} 
    & \mapsto 
    \int_{U \in C} \mathrm{sSet}( C_{\mathrm{th}}(i(U), \mathbf{K})  , F(U))
    \\
    & \simeq 
    \int_{U \in C} \mathrm{sSet}( C(U, p(\mathbf{K}))  , F(U))
    \\
    & \simeq 
    F(p(\mathbf{K}))
    \\
    & =: (p^* F)(\mathbf{K})
   \end{aligned}
  \,,
$$

where in the last step we use the [[Yoneda reduction]]-form of the [[Yoneda lemma]]. 

This shows that the [[right adjoint]] to $(-)\circ i$ is itself given by precomposition with a functor, and hence has itself a further right adjoint, which gives us a total of four [[adjoint functor]]s

$$
  [C^{op}, sSet]  
    \stackrel{\overset{Lan_i}{\to}}{\stackrel{\overset{(-)\circ i}{\leftarrow}}{\stackrel{\overset{(-)\circ p}{\to}}{\underset{Ran_p}{\leftarrow}}}}
  [C_{th}^{op}, sSet]
  \,.
$$

From this are directly induced the corresponding [[simplicial Quillen adjunction]]s on the global projective and injective [[model structure on simplicial presheaves]]

$$
  (Lan_i \dashv (-) \circ i) : 
  [C^{op}, sSet]_{proj}
   \stackrel{\overset{Lan_i}{\to}}{\underset{(-)\circ i}{\leftarrow}}
  [C_{th}^{op}, sSet]_{proj}
  \,;
$$

$$
  ((-)\circ i \dashv (-) \circ p) : 
  [C^{op}, sSet]_{proj}
   \stackrel{\overset{(-)\circ i}{\leftarrow}}
    {\underset{(-)\circ p}{\to}}
  [C_{th}^{op}, sSet]_{proj}
  \,;
$$

$$
  ((-) \circ p \dashv Ran_p) : 
  [C^{op}, sSet]_{inj}
   \stackrel{\overset{(-)\circ p}{\to}}{\underset{Ran_p}{\leftarrow}}
  [C_{th}^{op}, sSet]_{inj}
  \,.
$$

Observe that $Lan_i$, being a left [[Kan extension]], sends representables to representables: we have

$$
  Lan_i C(-,T) :
  \mathbf{K}
  \mapsto
  \int^{U \in C} C_{th}(\mathbf{K}, i(U))
   \cdot C(U,T)
$$

and by [[Yoneda reduction]] (more explicitly: observing that this is equivalently the formula for left [[Kan extension]] of the non-corepresentable $C_{th}(K \times D, i(-)) : C \to sSet$ along the identity functor) this is

$$
  \cdots \simeq C_{th}(\mathbf{K}, i(T))
  \,.
$$

By the discussion at [[simplicial Quillen adjunction]] for the above Quillen adjunctions to descend to the Cech-local [[model structure on simplicial presheaves]] it suffices that the [[right adjoint]]s preserve locally fibrant objects. 

We first check that $(-) \circ i$ sends locally fibrant objects to locally fibrant objects.  

To that end, let $\{U_i \to U\}$ be a [[covering family]] in $C$. Write $\int^{[k] \in \Delta} \Delta[k] \cdot \coprod_{i_0, \cdots, i_k} (j(U_{i_0}) \times_{j(U)} j(U_{i_1}) \times_{j(U)} \cdots \times_{j(U)} j(U_k))$ for its [[Cech nerve]], where $j$ denotes the [[Yoneda embedding]]. Recall by the definition of the [[∞-cohesive site]] $C$ that all the [[fiber product]]s of representable presheaves here are again themselves representable, hence $\cdots = \int^{[k] \in \Delta} \Delta[k] \cdot \coprod_{i_0, \cdots, i_k} (j(U_{i_0} \times_U U_{i_1} \times_U \cdots \times_U U_k))$. This means that the [[left adjoint]] $Lan_i$ preserves not only the [[coend]] and [[tensoring]], but by the remark in the previous paragraph and the assumption that $i$ preserves [[pullback]]s along covers we have that

$$
  \begin{aligned}
    Lan_i 
    C(\{U_i \to U\})
    & \simeq 
     \int^{[k] \in \Delta} \Delta[k] \cdot \coprod_{i_0, \cdots, i_k} Lan_i (j(U_{i_0} \times_U U_{i_1} \times_U \cdots \times_U U_k))    
     \\
     & \simeq
     \int^{[k] \in \Delta} \Delta[k] \cdot \coprod_{i_0, \cdots, i_k} 
  j i (U_{i_0} \times_U U_{i_1} \times_U \cdots \times_U U_k)    
    \\
    & \simeq
     \int^{[k] \in \Delta} \Delta[k] \cdot \coprod_{i_0, \cdots, i_k} 
  j (i(U_{i_0}) \times_{i(U)} i(U_{i_1}) \times_{i(U)} \cdots \times_{i(U)} i(U_k))      
  \end{aligned}
   \,.
$$ 

By the assumption that $i$ preserves covers, this is the [[Cech nerve]] of a [[covering family]] in $C_{th}$. Therefore for $F \in [C_{th}^{op}, sSet]_{proj,loc}$ fibrant we have for all [[covering]]s $\{U_i \to U\}$ in $C$ that the [[descent]] morphism

$$
  (i^* F)(U) = F(i(U))
   \stackrel{}{\to}
  [C_{th}^{op}, sSet](C(\{i(U_i)\}), F)
  =
  [C^{op}, sSet](C(\{U_i\}), i^* F)
$$

is a weak equivalence, hence that $i^* F$ is locally fibrant.

To see that $(-) \circ p$ preserves locally fibrant objects, we apply the analogous reasoning after observing that its [[left adjoint]] $(-)\circ i$ preserves all [[limit]]s and [[colimit]]s of [[simplicial presheaves]] (as these are computed objectwise) and by observing that for 
$\{\mathbf{U}_i \stackrel{p_i}{\to} \mathbf{U}\}$ 
a covering family in $C_{th}$ we have that its image under $(-) \circ i$ is its image under $p$, by the [[Yoneda lemma]]:

$$
  \begin{aligned}
     [C^{op}, sSet](K, ((-)\circ i) (\mathbf{U}))
     & \simeq
     C_{th}(i(K), \mathbf{U})
     \\
     & \simeq
      C(K, p(\mathbf{U}))
  \end{aligned}
$$

and using that $p$ preserves covers by assumption.

Therefore $(-) \circ i$ is a left and right local [[Quillen adjunction|Quillen functor]] with left local Quillen adjoint $Lan_i$ and right local Quillen adjoint $(-)\circ p$.

It follows that $i^* : Sh_{(\infty,1)}(C_{th}) \to Sh_{(\infty,1)}(C)$ is given by the left [[derived functor]] of restriction along $i$, and 
$i_* : Sh_{(\infty,1)}(C) \to Sh_{(\infty,1)}(C_{th})$ is given by the right [[derived functor]] of restriction along $p$. 

Finally to see that also $Ran_p$ preserves locally fibrant objects by the same reasoning as above, notice that for every [[covering]] family $\{U_i \to U\}$ in $C$ and every morphism $\mathbf{K} \to p^* U$ in $C_{th}$ we may find a covering $\{\mathbf{K}_j  \to \mathbf{K}\}$ of $\mathbf{K}$ such that we find commuting diagrams on the left of

$$
  \array{
    \mathbf{K}_j &\to& p^* U_{i(j)}
    \\
    \downarrow && \downarrow
    \\
    \mathbf{K} &\to& p^* U
  }
  \;\;\;
  \leftrightarrow
  \;\;\;
  \array{
    p(\mathbf{K}_j) & =&  i^*(\mathbf{K}_j) &\to&  U_{i(j)}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    p(\mathbf{K}) &= & i^*(\mathbf{K})  &\to&  U
  }
  \,,
$$

because by adjunction these correspond to commuting diagrams as indicated on the right, which exist by definition of [[coverage]] on $C$ and lift through $p$ by assumption on $C_{th}$.

This implies that $\{p^* U_i \to p^* U\}$ is a _generalized cover_ in the terminology at [[model structure on simplicial presheaves]], which by the discussion there implies that the corresponding [[Cech nerve]] equivalent to the [[sieve]] inclusion is a weak equivalence.

This establishes the quadruple of [[adjoint (∞,1)-functor]]s as claimed.

It remains to see that $i_!$ is full and faithful.

For that notice the general fact that left 
[[Kan extension]] (see the propeties discussed there) along a [[full and faithful functor]] $i$ satisfies $Lan_i \circ i \simeq id$. It remains to observe that since $(-)\circ i$ is not only right but also left Quillen by the above, we have that $i^* Lan_i$ applied to a cofibrant object is already the [[derived functor]] of the composite.

=--


+-- {: .un_remark}
###### Remark

Conversely this implies that $Sh_{(\infty,1)}(C_{th})$ is an [[∞-connected (∞,1)-topos]] over [[Smooth∞Grpd]], exhibited by the triple of adjunctions

$$
  (i^* \dashv i_* \dashv i^!) : 
  SynthDiff \infty Grpd \to Smooth \infty Grpd
  \,.
$$


=--


### Structures in the presence of infinitesimal cohesion

We discuss structures that are canonically present in 
a cohesive $(\infty,1)$-topos equipped with infinitesimal cohesion. These structures parallel the [structures in a general cohesive (∞,1)-topos](#Structures).




#### Infinitesimal paths and de Rham spaces
  {#InfinitesimalPaths}
 
In the presence of [infinitesimal cohesion](#InfinitesimalCohesiveInfTopos) there is an infinitesimal analog of the [geometric paths ∞-groupoids](#Paths).


+-- {: .un_def #InfinitesimalPathsAndReduction}
###### Definition

Define the triple of [[adjoint (∞,1)-functor]]s 

$$
 (\mathbf{Red} \dashv \mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{dR})
 : 
 (i_! i^* \dashv i_* i^* \dashv i_* i^! ) 
  :
 \mathbf{H}_{th} 
  \to 
 \mathbf{H}_{th}
  \,.
$$

For $X\in \mathbf{H}_{th}$ we say that

* $\mathbf{\Pi}_{inf}(X)$ is the **infinitesimal path $\infty$-groupoid** 
  of $X$;

  The $(i^* \dashv i_*)$-[[unit of an adjunction|unit]] 

  $$
    X \to \mathbf{\Pi}_{inf}(X)
  $$

  we call the **constant infinitesimal path inclusion**.

* $\mathbf{Red}(X)$ is the **reduced cohesive $\infty$-groupoid** underlying
  $X$.

  The $(i_* \dashv i^*)$-[[unit of an adjunction|counit]] 

  $$
    \mathbf{Red} X \to X
  $$

  we call the **inclusion of the reduced part** of $X$.

=-- 

+-- {: .num_defn #FormalSmoothness}
###### Definition

We say an object $X \in \mathbf{H}_{th}$ is **formally smooth** if the constant infinitesimal path inclusion

$$
  X \to \mathbf{\Pi}(X)
$$

is an [[effective epimorphism in an (∞,1)-category|effective epimorphism]].

=--

In this form this is the evident $(\infty,1)$-categorical analog of the conditions as they appear for instance in [SimpsonTeleman, page 7](#SimpsonTeleman).

+-- {: .un_note #FormalSmoothnessByCanonicalMorphism}
###### Note

An object $X \in \mathbf{H}$ is formally smooth according to def. \ref{FormalSmoothness} precisely if the canonical morphism

$$
  i_! X \to i_* X
$$

is an [[effective epimorphism in an (∞,1)-category|effective epimorphism]].

=--

+-- {: .proof}
###### Proof

The canonical morphism is the composite

$$
  (i_! \to i_*)
  :=
  i_!
   \stackrel{\eta i_!}{\to}
  \mathbf{\Pi}_{inf} i_! := i_* i^* i_!
   \stackrel{\simeq}{\to}
  i_*  
  \,.
$$

By the condition that $i_!$ is a [[full and faithful (∞,1)-functor]] the second morphism here in an [[equivalence in an (∞,1)-category|equivalence]] and hence the component of the composite on $X$ being an effective epimorphism is equivalent to the component $i_! X \to \mathbf{\Pi} i_! X$ being an effective epimorphism.

=--

In this form this characterization of formal smoothness is the evident generalization of the condition given in [Kontsevich-Rosenberg, section 4.1](#KontsevichRosenbergSpaces). See the section <a href="http://nlab.mathforge.org/nlab/show/Q-category#FormalSmoothness">Formal smoothness</a> at [[Q-category]].



+-- {: .un_prop #RedIsIdempotent}
###### Observation

The operation $\mathbf{Red}$ is an [[idempotent]] projection of
$\mathbf{H}_{th}$ onto the image of $\mathbf{H}$

$$
  \mathbf{Red} \mathbf{Red} \simeq \mathbf{Red}
  \,.
$$

Accordingly also

$$
  \mathbf{\Pi}_{inf} \mathbf{\Pi}_{inf} \simeq \mathbf{\Pi}_{inf}
$$

and

$$
  \mathbf{\flat}_{inf} \mathbf{\flat}_{inf} \simeq 
  \mathbf{\flat}_{inf}
  \,.
$$


=--

+-- {: .proof}
###### Proof

By definition of infinitesimal neighbourhood we have that
$i_!$ is a [[full and faithful (∞,1)-functor]]. It follows that 
$i^* i_! \simeq Id$ and hence

$$
  \begin{aligned}
    \mathbf{Red} \mathbf{Red}
    & \simeq
    i_! i^* i_! i^* 
    \\
    & \simeq i_! i^*
    \\
    & \simeq \mathbf{Red}
  \end{aligned}
  \,.
$$

=--

+-- {: .un_prop #InclusionOfConstantIntoInfinitesimalIntoAllPaths}
###### Observation

There is a canonical [[natural transformation]]

$$
  \mathbf{\Pi}_{inf}(X) \to \mathbf{\Pi}(X)
$$

that factors the finite path inclusion through the infinitesimal one

$$
  \array{
    && \mathbf{\Pi}_{inf}(X)
    \\
    & \nearrow && \searrow
    \\
    X &&\to&& \mathbf{\Pi}(X)
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is the formula for the unit of the composite adjunction
$\mathbf{H}_{th} \stackrel{\overset{\Pi_{inf}}{\to}}{\underset{Disc_{inf}}{\leftarrow}} \mathbf{H} \stackrel{\overset{\Pi}{\to}}{\underset{Disc}{\leftarrow}} \infty Grpd$:

$$
  X \stackrel{i_{inf}X}{\to} Disc_{inf}\Pi_{inf} X
  \stackrel{Disc_{inf}(i_{\mathbf{H}}\Pi_{inf}X)}{\to}
  Disc_{\mathbf{H}} Disc_{inf} \Pi_{\mathbf{H}} \Pi_{inf} X
  =
  Disc_{\mathbf{H}_{th}} \Pi_{\mathbf{H}_{th}}
  \,.
$$


=--


#### Flat $\infty$-connections and infinitesimal local systems
  {#StrucInfinitesimalLocalSystem}


We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#FlatDifferentialCohomology">intrinsic flat cohomology</a> in an infinitesimal neighbourhood.

+-- {: .un_def}
###### Definition

For $X, A \in \mathbf{H}_{th}$ we say that

$$
  H_{infflat}(X,A) := \pi_0 \mathbf{H}(\mathbf{\Pi}_{inf}(X), A)
   \simeq
   \pi_0 \mathbf{H}(X, \mathbf{\flat}_{inf}A)
$$

is the **infinitesimal flat cohomology** of $X$ with coefficient in $A$.

=--

By the [above observation](#InclusionOfConstantIntoInfinitesimalIntoAllPaths) 
we have canonical morphisms

$$
  \mathbf{H}_{flat}(X,A) 
    \to  
  \mathbf{H}_{infflat}(X,A)
    \to
  \mathbf{H}(X,A)
$$

The objects on the left are [[principal ∞-bundle]]s equipped with flat [[connection on an ∞-bundle|∞-connection]]. The first morphism forgets their [[higher parallel transport]] along finite volumes and just remembers the parallel transport along infinitesimal volumes. The last morphism finally forgets also this connection information.


#### $\infty$-Lie algebras and $\infty$-Lie algebroids
 {#LieAlgebroids}

The infinitesimal analog of [exponentiated ∞-Lie algebra](#LieAlgebras) are genuine [[∞-Lie algebra]]s.

+-- {: .un_def #InfinitesimalObject}
###### Definition

An object $X \in \mathbf{H}_{th}$ is an 
**infinitesimal cohesive $\infty$-groupoid** if 
$\mathbf{\Pi}_{inf} X \simeq *$.

An [[∞-group]] object $\mathfrak{g} \in \mathbf{H}_{th}$ that is infinitesimal we call an **[[∞-Lie algebra]]** . 

For $X \in \mathbf{H}$ any object, we say 
$\mathfrak{a} \in \mathbf{H}_{th}$ is an 
**[[∞-Lie algebroid]] over $X$** if $\mathbf{\Pi}_{inf}(\mathfrak{a}) \simeq \mathbf{\Pi}_{inf}(X)$; equivalently: if there is a morphism

$$
  \mathfrak{a} \to \mathbf{\Pi}_{inf}(X)
$$

that serves as [[generalized the|the]] $(i^* \dashv i_*)$-[[unit of an adjunction|unit]] on $\mathfrak{a}$, hence as the [infinitesimal path inclusion](#InfinitesimalPathsAndReduction) for $\mathfrak{a}$.

=--

+-- {: .un_prop}
###### Proposition

An infinitesimal cohesive $\infty$-groupoid
is both geometrically contractible and has as underlying discrete $\infty$-groupoid the point:

* $\Pi X \simeq *$

* $\Gamma X \simeq {*}$.

=--

+-- {: .proof}
###### Proof

The first statement is implied by the fact that 
both $i_!$ as well as $i_*$ are full and faithful. This means that
if $\mathbf{\Pi}_{\mathrm{inf}}(X) \simeq *$ then already $i^* X = \Pi_{\mathrm{inf}}(X) \simeq *$.
Since $\Pi_{\mathbf{H}_{\mathrm{th}}} \simeq \Pi_{\mathbf{H}} \Pi_{\mathrm{inf}}$ and 
$\Pi_{\mathbf{H}}$ preserves the terminal object by cohesiveness, this implies the first claim.
 
The second statement follows by 
$$
  \begin{aligned}
    \Gamma X & \simeq \mathbf{H}_{\mathrm{th}}(*,X)
     \\
     & \simeq \mathbf{H}_{\mathrm{th}}(\mathbf{Red}*, X)
     \\
     & \simeq \mathbf{H}_{\mathrm{th}}(*, \mathbf{\Pi}_{\mathrm{inf}}(X))
     \\
     & \simeq \mathbf{H}_{\mathrm{th}}(*,*)
     \\
     & \simeq *
  \end{aligned}
  \,.
$$

=--



+-- {: .un_prop}
###### Observation

For all $X \in \mathbf{H}$, we have that $X$ and $\mathbf{\Pi}_{inf}(X)$ are [∞-Lie algebroids](#InfinitesimalObject) over $X$, the first by the constant infinitesmal path inclusion, the second by the identity.

=--

+-- {: .proof}
###### Proof

For $X$ this is tautological, for $\mathbf{\Pi}(X)$ it follows from the [idempotency of Red](#RedIsIdempotent) and the $(i^* \dashv i_*)$-[[zig-zag identity]].

=--

+-- {: .un_def}
###### Definition

If we think of $\mathbf{\Pi}_{inf}(X)$ as an $\infty$-Lie algebroid we shall equivalently write

$$
  T X := \mathbf{\Pi}_{inf}(X)
$$

and call this the [[tangent Lie algebroid]] of $X$.

In this notation any other $\infty$-Lie algebroid $\mathfrak{a}$ over $X$ is characterized by a morphism

$$
  \mathfrak{a} \to T X
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

In other contexts the object $\mathbf{\Pi}_{inf}(X)$ is also called the **[[de Rham space]] of $X$**.

Here we avoid this terminology, since by the [above discussion](#deRhamCohomology) we have a good notion of intrinsic [[de Rham cohomology]] in a cohesive $(\infty,1)$-topos already without introducing infinitesimal cohesion. From this point of view the object $\mathbf{\Pi}_{inf}(X)$ is not primarily characterized by the fact that (in some models, see [below](#Examples)) it does co-represents de Rham cohomology -- because the object $\mathbf{\Pi}_{dR}(X)$ from [above](#deRhamCohomology) does, too -- but by the fact that it does so in an explicitly infinitesimal way.

=--

+-- {: .un_prop}
###### Proposition

The [[delooping]] $\mathbf{B}\mathfrak{g}$ of an [∞-Lie algebra](#InfinitesimalObject) $\mathfrak{g}$ is an [[∞-Lie algebroid]] over the point.

=--

+-- {: .proof}
###### Proof

Since both $i^*$ and $i_*$ are [[right adjoint]], the [infinitesimal path ∞-groupoid functor](#InfinitesimalPathsAndReduction) commutes with [[delooping]]. Therefore 

$$
  \begin{aligned}
    \mathbf{\Pi}_{inf} \mathbf{B}\mathfrak{g}
    & \simeq
    \mathbf{B} \mathbf{\Pi}_{inf} \mathfrak{g}
    \\
    & \simeq \mathbf{B} *
    \\
    & \simeq *
    \\
    & \simeq \mathbf{\Pi}_{inf} *
  \end{aligned}
  \,.
$$

=--


+-- {: .un_prop}
###### Proposition

An [infinitesimal cohesive ∞-groupoid](#InfinitesimalObject) 
$X \in \mathbf{H}_{th}$ is both [geometrically contractible](#ExponentiatedLieAsGeometricallyContractible) and has as underlying [[discrete ∞-groupoid]] the point:

* $\Pi X \simeq *$

* $\Gamma X \simeq *$.

=--

+-- {: .proof}
###### Proof

This follows with using the [above observation](#InfinitesimalInclusionIfFullAndFaithful) from the full and faithfulness of $i_!$ and $i_*$.

The former implies that with $\mathbf{\Pi}_{inf}(X) \simeq *$ already $i^*X  = \Pi_{inf}X = *$. Since $\Pi_{\mathbf{H}_{th}} \simeq \Pi_{\mathbf{H}} \Pi_{inf}$ and since $\Pi_{\mathbf{H}}$ preserves the point by cohesiveness, this implies the first claim.

For the latter we compute

$$
  \begin{aligned}
    \Gamma X & \simeq \mathbf{H}_{th}(*,X)
     \\
     & \simeq \mathbf{H}_{th}(\mathbf{Red}*, X)
     \\
     & \simeq \mathbf{H}_{th}(*, \mathbf{\Pi}_{inf}(X))
     \\
     & \simeq \mathbf{H}_{th}(*,*)
     \\
     & \simeq *
  \end{aligned}
  \,.
$$

=--


#### Lie theory {#LieTheory} 

(...)


#### Deformation theory {#StrucDeformationTheory}

(...)


## Examples {#Examples}

+-- {: .un_prop}
###### Proposition

Examples of [[∞-cohesive site]]s are

* any category with finite [[product]]s and equipped with the trivial [[coverage]].

* the [[full subcategory]] $CartSp_{top} \subset$ [[Top]] on [[open ball]]s with the [[good open cover]] [[coverage]];

* the site [[CartSp]] of [[Cartesian space]]s with [[smooth function]]s between them and [[good open cover]] [[coverage]].

* the [[Cahiers topos]]-site [[ThCartSp]] of infinitesimally thickened Cartesian spaces.

=--


### Discrete $\infty$-groupoids

* [[discrete ∞-groupoid]]


### Topological $\infty$-groupoids

* [[Euclidean-topological ∞-groupoid]]

* [[locally contractible topological ∞-groupoid]]


### Smooth $\infty$-groupoids

* [[smooth ∞-groupoid]]

* [[synthetic differential ∞-groupoid]]

* [[super smooth ∞-groupoid]]

### Super $\infty$-groupoids

* [[super ∞-groupoid]]

* [[smooth super ∞-groupoid]]


## Applications


As a context for geometric spaces and paths in geometric spaces, cohesive $(\infty,1)$-toposes are a natural context in which to formulate fundamental fundamental [[physics]]. See [[higher category theory and physics]] for more on this.


## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / **cohesive (∞,1)-topos**

and

* [[locally connected site]], [[locally ∞-connected site]]

* [[connected site]]

* [[local site]]

* [[cohesive site]], [[(∞,1)-cohesive site]]


## References

The [[category theory|category-theoretic]] definition of [[cohesive topos]] was proposed by [[Bill Lawvere]]. See the references at [[cohesive topos]].

The observation that the further left adjoint $\Pi$ in a [[locally ∞-connected (∞,1)-topos]] defines an intrinsic notion of paths and [[geometric homotopy groups in an (∞,1)-topos]] was suggested by [[Richard Williamson]].

The observation that the further right adjoint $coDisc$ in a [[local (∞,1)-topos]] serves to characterize [[concrete sheaf|concrete (∞,1)-sheaves]] was amplified by [[David Carchedi]].

The [infinitesimal path ∞-groupoid adjunction](#LieTheory) $(\mathbf{Red} \dashv \mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{inf})$ is essentially discussed in section 3 of 

* [[Carlos Simpson]], [[Constantin Teleman]], _deRham theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))
{#SimpsonTeleman}

The characterization of infinitesimal extensions and formal smoothness by adjoint functors is considered in 

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative spaces_, preprint MPI-2004-35 ([ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2331), [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2303))
 {#KontsevichRosenbergSpaces}

in the context of _[[Q-categories]]_ .

Some of the material discussed here is in section 2 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ 

A commented list of related references is at

* [[schreiber:differential cohomology in an (∞,1)-topos -- references
  |differential cohomology in a cohesive topos -- references]]



[[!redirects cohesive (∞,1)-topos]]

[[!redirects cohesive (∞,1)-toposes]]
[[!redirects cohesive (infinity,1)-toposes]]

[[!redirects cohesive (∞,1)-topoi]]
[[!redirects cohesive (infinity,1)-topoi]]


[[!redirects cohesive ∞-groupoid]]
[[!redirects cohesive ∞-groupoids]]
[[!redirects cohesive infinity-groupoid]]
[[!redirects cohesive infinity-groupoids]]