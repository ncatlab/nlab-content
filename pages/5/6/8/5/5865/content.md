
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--


> This is a sub-section of the entry _[[cohesive (∞,1)-topos]]_ . See there for background and context

***


#Contents#
* table of contents
{:toc}

## Structure in a cohesive $(\infty,1)$-topos

A cohesive $(\infty,1)$-topos is a general context for [[higher geometry]] with good [[cohomology]] and [[homotopy]] properties. We list fundamental structures and constructions that exist in every cohesive $(\infty,1)$-topos.


### Concrete objects
 {#ConcreteObjects}


The cohesive structure on an object in a cohesive 
$(\infty,1)$-topos need not be supported by points. 
We discuss a general abstract characterization of objects that do have an interpretation as bare $n$-groupoids equipped with cohesive structure.

Compare with the section <a href="http://nlab.mathforge.org/nlab/show/cohesive%20topos#ConcreteObjects">Quasitoposes of concrete objects</a> at [[cohesive topos]].


+-- {: .num_prop #SubToposesOfDiscreteAndCodiscrete}
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

+-- {: .num_prop }
###### Proposition


The [[(∞,1)-topos]] [[∞Grpd]] is equivalent to 
the full [[sub-(∞,1)-category]] of $\mathbf{H}$ on 
those objects $X \in \mathbf{H}$ for which the 
[[unit of an adjunction|unit]]
 
$$
    X \to \mathrm{coDisc}\Gamma X
$$
  
is an [[equivalence in an (∞,1)-category|equivalence]].

=--

+-- {: .proof}
###### Proof

This follows by general facts discussed at [[reflective sub-(∞,1)-category]].

=--

+-- {: .num_defn}
###### Definition

We say an object $X$ is **$n$-concrete** if the canonical morphism 
$X \to coDisc \Gamma X$ is [[n-truncated|(n-1)-truncated]].

If a [[0-truncated]] object $X$ is $0$-concrete, we call it just **concrete**.


=--

See also _[[concrete (∞,1)-sheaf]]_.

+-- {: .num_prop}
###### Proposition

For $C$ an [[∞-cohesive site]], a 0-truncated object in the 
[[(∞,1)-topos]] over $C$ is concrete precisely if it is
a [[concrete sheaf]] in the traditional sense.

=--

+-- {: .num_defn #NConcretification}
###### Definition

For $X \in \mathbf{H}$ and $n \in \mathbb{N}$, the 
**$(n+1)$-concretification** of $X$ is the morphism

$$
  X \to conc_{n+1} X
$$

that is the left factor in the decomposition with respect to the 
[[n-connected/n-truncated factorization system]] of the 
$(\Gamma \dashv coDisc)$-[[unit of an adjunction|unit]]

$$
  \array{   
    && conc_{n+1} X
    \\
    & \nearrow && \searrow
    \\
    X &&\to&& coDisc \Gamma X
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

By that very [[n-connected/n-truncated factorization system]]
we have that $conc_{n+1} X$ is an $(n+1)$-concrete object.

=--



### Cohesive $\infty$-Groups 
  {#InfinGroups}

Every [[(∞,1)-topos]] $\mathbf{H}$ 
comes with a notion of [[group object in an (∞,1)-category|∞-group objects]] that generalizes the traditional notion of grouplike $A_\infty$ spaces in [[Top]] $\simeq$ [[∞Grpd]]. For more details on the following see also _[[looping and delooping]]_.



+-- {: .num_defn}
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


+-- {: .num_remark}
###### Remark

Notice that every [[0-connected]] object $A$ in the cohesive $(\infty,1)$-topos $\mathbf{H}$ does have a global point (then necessarily essentially unique) $* \to A$.

=--

This follows from the [above proposition](#PointLike) which says that $\mathbf{H}$ necessarily has [[homotopy dimension]] $\leq 0$.


+-- {: .num_prop}
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


+-- {: .num_prop}
###### Observation

 The delooping object $\mathbf{B}G \in \mathbf{H}$ is concrete precisely if $G$ is.

=--

We may therefore unambiguously speak of **concrete cohesive $\infty$-groups**.

+-- {: .num_defn}
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

+-- {: .num_remark}
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


+-- {: .num_prop}
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


### Cohomology and principal $\infty$-bundles 
 {#Cohomology}

There is an intrinsic notion of [[cohomology]] and 
of [[principal ∞-bundles]] in any [[(∞,1)-topos]] $\mathbf{H}$.

+-- {: .num_defn}
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


+-- {: .num_defn}
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

+-- {: .num_prop}
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


+-- {: .num_defn}
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


+-- {: .num_prop}
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


+-- {: .num_prop}
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

+-- {: .num_defn #GPrincipalInfinityBundle}
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

Of special interest are principal $\infty$-bundles of the form $P \to \mathbf{B}G$:

+-- {: .num_defn #InfinityGroupExtensions}
###### Definition

We say a sequence of [cohesive ∞-groups](#InfinGroups)

$$
  A \to \hat G \to G
$$

_exhibits $\hat G$ as an [[group extension|extension]] of $G$ by $A$_ if the corresponding [[delooping]] sequence

$$
  \mathbf{B}A \to \mathbf{B}\hat G \to \mathbf{B}G
$$

if a [[fiber sequence]]. If this fiber sequence extends one step further to the right to a morphism $\phi : \mathbf{B}G \to \mathbf{B}^2 A$, we have by def. \ref{GPrincipalInfinityBundle} that $\mathbf{B}\hat G \to \mathbf{B}G$ is the $\mathbf{B}A$-[[principal ∞-bundle]] classified by the [[cocycle]] $\phi$; and $\mathbf{B}A \to \mathbf{B}\hat G$ is its [[fiber]] over the unique point of $\mathbf{B}G$.

Given an extension and a  a $G$-[[principal ∞-bundle]] $P \to X$ in $\mathbf{H}$ we say a **lift** $\hat P$ of $P$ to a $\hat G$-principal $\infty$-bundle is a factorization of its classifying [[cocycle]] $g : X \to \mathbf{B}G$ through the extension

$$
  \array{
      && \mathbf{B}\hat G
     \\
     & {}^{\mathllap{\hat g}}\nearrow & \downarrow
    \\
    X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

=--

+-- {: .num_prop #ExtendedBundlesByBundlesOfExtensions}
###### Proposition

Let $A \to \hat G \to G$ be an extension of $\infty$-groups, 
def. \ref{InfinityGroupExtensions} in $\mathbf{H}$ and let $P \to X$ be a $G$-[[principal ∞-bundle]]. 

Then a $\hat G$-extension $\hat P \to X$ of $P$ is in particular also an $A$-principal $\infty$-bundle $\hat P \to P$ over $P$ with the property that its restriction to any [[fiber]] of $P$ is equivalent to $\hat G \to G$.

=--

We may summarize this as saying: 

> An extension of $\infty$-bundles is an $\infty$-bundle of extensions.

+-- {: .proof}
###### Proof

This follows from repeated application of the [[pasting law]] for [[(∞,1)-pullback]]s: consider the following diagram in $\mathbf{H}$

$$
  \array{
    \hat G &\to& \hat P &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    G &\to& P &\stackrel{q}{\to}& \mathbf{B}A &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow && \downarrow
    \\
    {*} &\stackrel{x}{\to}&
    X &\stackrel{\hat g}{\to}& \mathbf{B}\hat G
    &\stackrel{}{\to}& \mathbf{B}G
  }
  \,.
$$

The bottom composite $g : X \to \mathbf{B}G$ is a cocycle for the given $G$-principal $\infty$-bundle $P \to X$ and it factors through $\hat g : X \to \mathbf{B}\hat G$ by assumption of the existence of the extension $\hat P \to P$. 

Since also the bottom right square is an $\infty$-pullback by the given $\infty$-group extension, the [[pasting law]] asserts that the square over $\hat g$ is also a pullback, and then that so is the square over $q$. This exhibits $\hat P$ as an $A$-principal $\infty$-bundle over $P$.

Now choose any point $x : {*} \to X$ of the base space as on the left of the diagram. Pulling this back upwards through the diagram and using the pasting law and the definition of [[loop space object]]s $G \simeq \Omega \mathbf{B}G \simeq * \prod_{\mathbf{B}G} *$ the diagram completes by $(\infty,1)$-pullback squares on the left as indicated, which proves the claim.

=--

### $\infty$-Gerbes
  {#InftyGerbe}

For the moment see the discussion at _[[∞-gerbe]]_ . 

### Twisted cohomology and section
 {#TwistedCohomology}


A slight variant of [[cohomology]] is often relevant: [[twisted cohomology]].

+-- {: .num_defn #TwistedCohomologyInOvertopos}
###### Definition

For $\mathbf{H}$ an [[(∞,1)-topos]] let  $\mathbf{c} : B \to C$ a [[morphism]] representing a [[characteristic class]] $[\mathbf{c}] \in H(B,C)$. Let $C$ be [[pointed object|pointed]] and write  $A \to B$ for its [[homotopy fiber]].

We say that the **[[twisted cohomology]]** with coefficients in $A$ relative to $\mathbf{c}$ is the [[cohomology|intrinsic cohomology]] of the [[over-(∞,1)-topos]] $\mathbf{H}/C$ with coefficients in $f$.

If $\mathbf{c}$ is understood and $\phi : X \to B$ is any morphism, we write

$$
  \mathbf{H}_{\phi}(X, A)
   :=
  \mathbf{H}/C(\phi, \mathbf{c})
$$

and speak of the _[[cocycle]] [[∞-groupoid]] of twisted cohomology on $X$ with coefficients in $A$ and twisting cocycle $\phi$ relative to $[\mathbf{c}]$_ .

=--

For short we often say _twist_ for _twisting cocycle_ .

+-- {: .num_prop #DirectPropsOfTwistedCohomology}
###### Proposition

We have the following immediate properties of twisted cohomology:

* The $\phi$-twisted cohomology relative to $\mathbf{c}$ depends, up to [[equivalence in an (∞,1)-category|equivalence]], only on the [[characteristic class]] $[\mathbf{c}] \in H(B,C)$ represented by $\mathbf{c}$ and also only on the equivalence class $[\phi] \in H(X,C)$ of the twist.

* If the characteristic class is [[terminal object|terminal]], $\mathbf{c} : B \to *$ we have $A \simeq B$ and the corresponding twisted cohomology is ordinary cohomology with coefficients in $A$.


=--

+-- {: .num_prop #PullbackCharacterizationOfTwistedCohomology}
###### Proposition

Let the [[characteristic class]] $\mathbf{c} : B \to C$ and a twist $\phi : X \to C$ be given. Then the cocycle $\infty$-groupoid of twisted $A$-cohomology on $X$ is given by the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{\phi}(X,A) &\to& {*}
    \\
    \downarrow && \downarrow^{\mathrlap{\phi}}
    \\
    \mathbf{H}(X,B) &\stackrel{\mathbf{c}_*}{\to}& 
    \mathbf{H}(X,C)
  }
$$

in [[∞Grpd]].

=--

+-- {: .proof}
###### Proof

This is an application of the general pullback-formula for hom-spaces in
an [[over-(∞,1)-category]]. See there for details.

=--

+-- {: .num_prop #TrivialTwistYieldsOrdinaryCohomology}
###### Proposition

If the twist is trivial, $\phi = 0$ (meaning that it factors as $\phi : X \to * \to C$ through the point of the pointed object $C$), the corresponding twisted $A$-cohomology is equivalent to ordinary $A$-cohomology

$$
  \mathbf{H}_{\phi = 0}(X,A)
   \simeq  
  \mathbf{H}(X,A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

In this case we have that the characterizing $(\infty,1)$-pullback diagram from prop. \ref{PullbackCharacterizationOfTwistedCohomology} is the image under the [[hom-functor]] $\mathbf{H}(X,-) : \mathbf{H} \to \infty Grpd$ of the pullback diagram $B \stackrel{\mathbf{c}}{\to} C \leftarrow *$. By definition of $A$ as the [[homotopy fiber]] of $\mathbf{c}$,  its pullback is $A$. Since the [[hom-functor]] $\mathbf{H}(X,-)$ preserves [[(∞,1)-pullbacks]] the claim follows:

$$
  \begin{aligned}
    \mathbf{H}_{\phi = 0 }(X,A)
     & \simeq
    \mathbf{H}(X,B) \prod_{\mathbf{H}(X,C)} \mathbf{H}(X,*)
     \\
     & \simeq
      \mathbf{H}(X, B \prod_C *)
     \\
     & \simeq 
      \mathbf{H}(X,A)
  \end{aligned} 
  \,.
$$

=--

Often twisted cohomology is formulated in terms of homotopy classes of sections of a bundle. The following asserts that this is equivalent to the above definition.

By the discussion at [Cohomology and principal ∞-bundles](#Cohomology) we may understand the twist $\phi : X \to C$ as the cocycle for an $\Omega C$-[[principal ∞-bundle]] over $X$, being the [[(∞,1)-pullback]] of the point inclusion $* \to C$ along $\phi$, where the point is the homotopy-incarnation of the universal $\Omega C$-principal $\infty$-bundle. The [[characteristic class]] $B \to C$ in turn we may think of as an $\Omega A$-bundle [[associated bundle|associated]] to this universal bundle. Accordingly the pullback of $P_\phi := X \times_C B$ is the associated $\Omega A$-bundle over $X$ classified by $\phi$.

+-- {: .num_prop #TwistedCohomologyBySections}
###### Proposition

Let $P_\phi := X \times_C B$ be [[(∞,1)-pullback]] of the [[characteristic class]] $\mathbf{c}$ along the twisting cocycle $\phi$ 

$$
  \array{
     P_\phi &\to& B
     \\
     {}^{\mathllap{p}}\downarrow && \downarrow^{\mathrlap{\mathbf{c}}}
     \\
     X &\stackrel{\phi}{\to}& C
  }
  \,.
$$

Then the $\phi$-twisted $A$-cohomology of $X$ is equivalently the space of [[section]]s $\Gamma_X(P_\phi)$ of $P_\phi$ over $X$:

$$
  \mathbf{H}_{tw,\phi}(X,A)
  \simeq
  \Gamma_X(P_\phi)
  \,,
$$

where on the right we have the [[(∞,1)-pullback]]

$$
  \array{ 
     \Gamma_X(P_\phi) &\to& *
     \\
     \downarrow && \downarrow^{\mathrm{id}}
     \\
     \mathbf{H}(X,P_\phi) &\stackrel{p_*}{\to}& \mathbf{H}(X,X)
  }
  \,.
$$


=--

+-- {: .proof}
###### Proof

Consider the [[pasting diagram]]

$$
  \array{
     \mathbf{H}_{\phi}(X,A) \simeq & \Gamma_\phi(X)
     &\to& {*}
     \\
     & \downarrow && \downarrow^{\mathrlap{id}}
     \\
     & \mathbf{H}(X,P_{\phi}) &\stackrel{p_*}{\to}& \mathbf{H}(X,X)
     \\
     & \downarrow && \downarrow^{\mathrlap{\phi}_*}
     \\
     & \mathbf{H}(X,B) &\stackrel{\mathbf{c}_*}{\to}&
     \mathbf{H}(X,C)
  }
  \,.
$$

By the fact that the [[hom-functor]] $\mathbf{H}(X,-)$
preserves [[(∞,1)-limit]]s the bottom square is an [[(∞,1)-pullback]].
By the [[pasting law]] for [[(∞,1)-pullback]]s so is then the total outer
diagram. 
Noticing that the right vertical composite is 
$* \stackrel{\mathbf{\phi}}{\to} \mathbf{H}(X,C)$ the claim
follows with 
prop. \ref{PullbackCharacterizationOfTwistedCohomology}.


=--



+-- {: .num_note #CollectingTwistedCohomologyForDifferentTwists}
###### Note

In applications one is typically interested in situations where the [[characteristic class]] $[\mathbf{c}]$ and the domain $X$ is fixed and the twist $\phi$ varies. Since by prop. \ref{DirectPropsOfTwistedCohomology} only the equivalence class $[\phi] \in H(X,C)$ matters, it is sufficient to pick one representative $\phi$ in each equivalence class. Such as choice is equivalently a choice of [[section]]

$$
  H(X,C) := \pi_0 \mathbf{H}(X,C) \to \mathbf{H}(X,C)
$$

of the [[0-truncated|0-truncation]] projection $\mathbf{H}(X,C) \to H(X,C)$ from the cocycle $\infty$-groupoid to the set of cohomology classes. This justifies the following terminology.

=--


+-- {: .num_defn #TotalTwistedCohomology}
###### Definition

With a [[characteristic class]] $[\mathbf{c}] \in H(B,C)$ with [[homotopy fiber]] $A$ understood, we write

$$
  \mathbf{H}_{tw}(X,A) := \coprod_{[\phi] \in H(X,C)} \mathbf{H}_{tw, \phi}(X,A)
$$

for the union of all twisted cohomology cocycle $\infty$-groupoids.

=--

+-- {: .num_prop #TotalTwistedCohomologyByPullback}
###### Observation

We have that $\mathbf{H}_{tw}(X,A)$ is the [[(∞,1)-pullback]]


$$
  \array{
     \mathbf{H}_{tw}(X,A) &\stackrel{tw}{\to}& H(X,C)
     \\
     \downarrow && \downarrow
     \\
     \mathbf{H}(X,B)
       &\stackrel{\mathbf{c}_*}{\to}&
     \mathbf{H}(X,C)
  }
  \,,
$$

where the right vertical morphism in any section of the projection from $C$-cocycles to $C$-cohomology.

=--

+-- {: .num_note #NoteOnCopiesOfHomotopyFibersForTwistedCohomology}
###### Note

When the [[(∞,1)-topos]] $\mathbf{H}$ is [[presentable (∞,1)-category|presented]] by a [[model structure on simplicial presheaves]] and model for $X$ and $C$ is chosen, then the cocycle [[∞-groupoid]] $\mathbf{H}(X,C)$ is presented by an explicit [[simplicial presheaf]] $\mathbf{H}(X,C)_{simp} \in sSet$. Once these choices are made, there is therefore the inclusion of simplicial presheaves


$$
  const (\mathbf{H}(X,C)_{simp})_0 \to \mathbf{H}(X,C)_{simp}
  \,,
$$

where on the left we have the simplicially constant object on the vertices of $\mathbf{H}(X,C)_{simp}$. This morphism, in turn, presents a morphism in $\infty Grpd$ that in general contains a multitude of copies of the components of any $H(X,C) \to \mathbf{H}(X,C)$: a multitude of representatives of twists for each cohomology class of twists. Since by the above the twisted cohomology does not depend, up to equivalence, on the choice of representative, the coresponding $(\infty,1)$-pullback yields in general a larger coproduct of $\infty$-groupoids as the corresponding twisted cohomology. This however just contains copies of the [[homotopy type]]s already present in $\mathbf{H}_{tw}(X,A)$ as defined above.

=--


### $\infty$-Group representations and associated $\infty$-bundles
 {#GroupRepresentations}

The material to go here is at 
[[schreiber:differential cohomology in a cohesive topos|Schreiber, section 2.3.7]].

(...)
### Concordance 
  {#Concordance}

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



### Geometric homotopy  / &#233;tale homotopy
 {#Homotopy}

We discuss canonical internal realizations of the notions of [[étale homotopy]], [[geometric homotopy groups in an (infinity,1)-topos]] and [[local systems]] .


+-- {: .num_defn}
###### Definition

For $\mathbf{H}$ a [[locally ∞-connected (∞,1)-topos]] and $X \in \mathbf{H}$ an [[object]], we call $\Pi X \in $ [[∞Grpd]] the 
**[[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]** of $X$. 

The ([[categorical homotopy groups in an (∞,1)-topos|categorical]]) [[homotopy group]]s of $\Pi(X)$ we call the [[geometric homotopy groups in an (∞,1)-topos|geometric homotopy groups]] of $X$

$$
  \pi_\bullet^{geom}(X) := \pi_\bullet(\Pi (X))
  \,.
$$

=--

+-- {: .num_defn #GeometricRealization}
###### Definition


For $\vert - \vert : $ [[∞Grpd]] $\stackrel{\simeq}{\to}$ [[Top]] the [[homotopy hypothesis]]-[[equivalence of (∞,1)-categories|equivalence]] we write

$$
  \vert X \vert := \vert \Pi X \vert \in Top
$$

and call this the **topological [[geometric realization of cohesive ∞-groupoids]]** of $X$, or just the _geometric realization_ for short.

=--

+-- {: .num_note #GeometricRealizationInTheLiterature}
###### Note

In presentations of $\mathbf{H}$ by a [[model structure on simplicial presheaves]] -- as discussed at [[∞-cohesive site]] -- this abstract notion reproduces the notion of geometric realization of [[∞-stack]]s in ([Simpson](#Simpson)). See remark 2.22 in ([SimpsonTeleman](#SimpsonTeleman)).

=--

+-- {: .num_defn}
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

+-- {: .num_prop}
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

+-- {: .num_prop}
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

### Cohesive $\mathbb{A}^1$-homotopy / The Continuum
 {#A1HomotopyContinuum}

+-- {: .num_defn}
###### Definition

An object $\mathbb{A}^1 \in \mathbf{H}$ is called 
a **line object exhibiting the cohesion of $\mathbf{H}$**
if the [[shape modality]] $&#643;$ (hence the reflector $\Pi : \mathbf{H} \to \infty Grpd$)
exhibits the [[localization of an (∞,1)-category]] of $\mathbf{H}$
at the class of morphisms $\{ X \times \mathbb{A}^1 \to X \}_{X \in \mathbf{H}}$.

=--

+-- {: .num_example #RealLineIsTheContinuum}
###### Example

The cohesion of [[Smooth∞Grpd]] _is exhibited_ (in the sense defined [here](cohesive+%28infinity%2C1%29-topos#A1ExhibitingCohesion)) by the [[real line]]
(the standard [[continuum]]) under the canonical embedding
$\mathbb{R} \in $ [[SmoothMfd]] $\hookrightarrow $ [[Smooth∞Grpd]].

=--

This is ([dcct, 3.9.1](#dcct)). 

+-- {: .num_remark}
###### Remark

The analogous notion in [[infinitesimal cohesion]]
is discussed in [infinitesimal cohesion -- infinitesimal A1-homotopy](#cohesive+(infinity%2C1)-topos+--+infinitesimal+cohesion#InfinitesimalA1Homotopy).

=--


See also at 

* [[A1-homotopy theory]]

* [[continuum]]

### Galois theory
 {#GaloisTheory}

We discuss a canonical internal notion of
[[Galois theory]] in $\mathbf{H}$.


+-- {: .num_defn}
###### Definition

For $\kappa$ a [[regular cardinal]] write 

$$
  Core \infty Grpd_\kappa \in \infty Grpd
$$ 

for the [[∞-groupoid]] of $\kappa$-[[small (∞,1)-category|small ∞-groupoid]]s: the [[core]] of the full [[sub-(∞,1)-category]] of [[∞Grpd]] on the $\kappa$-small ones.

=--

+-- {: .num_remark}
###### Remark

We have 

$$
  Core \infty Grpd_\kappa \simeq
  \coprod_i \mathbf{B} Aut(F_i)
  \,,
$$

where the coproduct ranges over all $\kappa$-small [[homotopy type]]s $[F_i]$ and $Aut(F_i)$ is the [[automorphism ∞-group]] of any representative $F_i$ of $[F_i]$.

=--

+-- {: .num_defn}
###### Definition

For $X \in \mathbf{H}$ write

$$
  LConst(X) := \mathbf{H}(X, Disc Core \infty Grpd_\kappa)
  \,.
$$

We call this the $\infty$-groupoid of **[[locally constant ∞-stack]]s** on $X$.

=--

+-- {: .num_observation}
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

+-- {: .num_prop}
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

+-- {: .num_lemma}
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

+-- {: .num_prop}
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

+-- {: .num_defn}
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

+-- {: .num_lemma}
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

+-- {: .num_defn}
###### Proposition

Let $\mathbf{H}$ be a [[locally ∞-connected (∞,1)-topos]]. If $X \in \mathbf{H}$ is [[small-projective]] then the [[over-(∞,1)-topos]] $\mathbf{H}/X$ is 

1. [[locally ∞-connected (∞,1)-topos|locally ∞-connected]];

1. [[local (∞,1)-topos|local]].


=--

+-- {: .proof}
###### Proof

The first statement is proven at [[locally ∞-connected (∞,1)-topos]], the second at [[local (∞,1)-topos]].

=--

+-- {: .num_defn}
###### Proposition

In a cohesive $(\infty,1)$-topos $\mathbf{H}$, if $X$ is 
[[small-projective]] then so is its path ∞-groupoid $\mathbf{\Pi}(X)$.

=--

+-- {: .proof}
###### Proof

Because of the [[adjoint triple]] of [[adjoint (∞,1)-functor]]s 
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



+-- {: .num_defn}
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

+-- {: .num_defn}
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

+-- {: .num_prop}
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

+-- {: .num_prop}
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





### Flat $\infty$-connections and local systems 
  {#FlatDifferentialCohomology}

We describe for a [[locally ∞-connected (∞,1)-topos]] $\mathbf{H}$ a canonical intrinsic notion of _[[flat ∞-connections]]_, _flat_ [[higher parallel transport]] and higher [[local systems]].

Write $(\mathbf{\Pi} \dashv\mathbf{\flat}) := (Disc \Pi \dashv Disc \Gamma) : \mathbf{H} \to \mathbf{H}$ for the adjunction given by the [path ∞-groupoid](#Paths). Notice that this comes with the canonical $(\Pi \dashv Disc)$-[[unit of an adjunction|unit]] with components

$$
  X \to \mathbf{\Pi}(X)
$$

and the $(Disc \dashv \Gamma)$-counit with components

$$
  \mathbf{\flat} A \to A
  \,.
$$

+-- {: .num_defn}
###### Definition

For $X, A \in \mathbf{H}$ we write

$$
  \mathbf{H}_{flat}(X,A) := \mathbf{H}(\mathbf{\Pi}X, A)
$$

and call $H_{flat}(X,A) := \pi_0 \mathbf{H}_{flat}(X,A)$ the **flat (nonabelian) differential cohomology** of $X$ with coefficients in $A$.

We say a morphism $\nabla : \mathbf{\Pi}(X) \to A$ is a **flat [[connection on an ∞-bundle|∞-connnection]]** on the [[principal ∞-bundle]] corresponding to $X \to \mathbf{\Pi}(X) \stackrel{\nabla}{\to} A$, or an **$A$-[[local system]]** on $X$.

The induced morphism

$$
  \mathbf{H}_{flat}(X,A) \to \mathbf{H}(X,A)
$$

we say is the [[forgetful functor]] that forgets flat connections.


=--

+-- {: .num_remark}
###### Remark

The object $\mathbf{\Pi}(X)$ has the interpretation of the [path ∞-groupoid](#Paths) of $X$: it is a cohesive $\infty$-groupoid whose [[k-morphism]]s may be thought of as generated from the $k$-morphisms in $X$ and $k$-dimensional cohesive paths in $X$.

Accordingly a morphism $\mathbf{\Pi}(X) \to A$ may be thought of as assigning

* to each point $x \in X$ a fiber $P_x$ in $A$;

* to each path $\gamma : x_1 \to x_2$ in $X$ an [[equivalence in an (infinity,1)-category|equivalence]] $\nabla(\gamma) : P_{x_1} \to P_{x_2}$ between these fibers (the [[parallel transport]] along $\gamma$);


* to each disk $\Sigma$ in $X$ a [[2-morphism|2-equivalalence]] $\nabla(\Sigma)$ between these equivaleces associated to its boundary (the [[higher parallel transport]])

* and so on.

$$
  \array{
     &&
     && P_{x_2}
     \\
     A 
     &&
     & {}^{\mathllap{\nabla(\gamma_1)}}\nearrow  
     &
      \Downarrow^{\nabla(\Sigma)}
     & 
     \searrow^{\mathrlap{\nabla(\gamma_2)}}
     \\
     \uparrow^{\mathrlap{\nabla}} &&
     P_{x_1}
     &&\underset{\nabla(\gamma_3)}{\to}&&
     P_{x_3}
     \\
     &&
     && x_2
     \\
     \mathbf{\Pi}(X)
     &&
     & {}^{\mathllap{\gamma_1}}\nearrow &
       \Downarrow^{\Sigma}
     & \searrow^{\mathrlap{\gamma_2}}
     \\
     &&
     x_1
     &&\underset{\gamma_3}{\to}&&
     x_3
  }
$$


This we think of as encoding a flat [[higher parallel transport]] on $X$, coming from some flat $\infty$-connection and _defining_ this flat $\infty$-connection. 

For a _non-flat_ $\infty$-connection the parallel transport $\nabla(\gamma_3^{-1}\circ \gamma_2\circ \gamma_1)$ around a contractible loop as above need not be equivalent to the identity. We will obtain a formal notion of non-flat parallel transport [below](#ChernWeilTheory).

=--

+-- {: .num_lemma}
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

The following lists some basic properties of objects of the form $\mathbf{\flat}A$ and their interpretation in terms of flat $\infty$-connections.

+-- {: .num_prop}
###### Proposition


For $G := Disc G_0 \in \mathbf{H}$ a [[discrete ∞-groupoid|discrete ∞-group]] the canonical morphism $\mathbf{H}_{flat}(X,\mathbf{B}G) \to \mathbf{H}(X,\mathbf{B}G)$ is an [[equivalence in an (∞,1)-category|equivalence]].

=--

+-- {: .proof}
###### Proof

Since $Disc$ is a [[full and faithful (∞,1)-functor]] we have that the  [[unit of an adjunction|unit]] $Id \to \Gamma Disc $ is a natural equivalence. It follows that on $Disc G_0$ also the counit $Disc \Gamma Disc G_0 \to Disc G_0$ is a weak equivalence (since by the [[triangle identity]] we have that $Disc G_0 \stackrel{\simeq}{\to} Disc \Gamma Disc G_0 \to Disc G_0$ is the identity).

=--

+-- {: .num_remark}
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

+-- {: .num_remark #UnderlyingGroupoidOfFlat}
###### Remark

Since $(Disc \dashv \Gamma)$ is a [[reflective sub-(∞,1)-category|coreflection]], we have that for any cohesive $\infty$-groupoid $A$ the underlying [[discrete ∞-groupoid]] $\Gamma A$ coincides with the underlying $\infty$-groupoid $\Gamma \mathbf{\flat}A $ of $\mathbf{\flat}A$:

$$  
  \Gamma \mathbf{\flat} A \stackrel{\simeq}{\to} \Gamma A  
  \,.
$$

To interpret this it is useful to think of $A$ as a [[moduli stack]] for principal $\infty$-bundles. This is most familiar in the case that $A$ is [[0-connected|connected]], in which case by [the above](#InfinGroups) we write it $A = \mathbf{B}G$ for some cohesive [[∞-group]] $G$. 

In terms of this we may say that

1. $\mathbf{B}G$ is the [[moduli stack|moduli ∞-stack]] of $G$-[[principal ∞-bundles]];

1. $\mathbf{\flat} \mathbf{B}G$ is the moduli $\infty$-stack of $G$-principal $\infty$-bundles equipped with a flat $\infty$-connection.

Therefore 

$$
  \Gamma \mathbf{B}G \simeq \mathbf{H}(*, \mathbf{B}G)
$$ 

is the [[∞-groupoid]] of $G$-principal $\infty$-bundles _over the point_ (the [[terminal object]] in $\mathbf{H}$). Similarly

$$
  \Gamma \mathbf{\flat}\mathbf{B}G \simeq \mathbf{H}(*, \mathbf{\flat}\mathbf{B}G)
$$ 

is the $\infty$-groupoid of _flat_ $G$-principal $\infty$-bundles over the point.

So the equivalence $\Gamma \mathbf{\flat}\mathbf{B}G \simeq \Gamma \mathbf{B}G$ says that over the point every $G$-principal $\infty$-bundle carries an essentially unique flat $\infty$-connection. This is certainly what one expects, and certainly the case for ordinary [[connection on a bundle|connections]] on ordinary [[principal bundle]]s. 

Notice here that the axioms of cohesion imply in particular that the terminal object $* \in \mathbf{H}$ really behaves like a geometric point: it has underlying it a single point, $\Gamma * \simeq *$, and its [geometric homotopy type](#Homotopy) is that of the point, $\Pi(*) \simeq *$.

=--


### de Rham cohomology 
  {#deRhamCohomology}

In every [[locally ∞-connected (∞,1)-topos]] $\mathbf{H}$ there is an intrinsic notion of [[nonabelian cohomology|nonabelian]] [[de Rham cohomology]].

+-- {: .num_defn #drFlatAnddRShape}
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
$\mathbf{\flat}_{dR} A := * \prod_A \mathbf{\flat}A$ for the [[(∞,1)-pullback]]

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

We also say $\flat_{dR}$ is the _[[dR-flat modality]]_ and $\Pi_{dR}$ is the _[[dR-shape modality]]_.




+-- {: .num_prop #DeRhamAdjunction}
###### Proposition

The construction in def. \ref{drFlatAnddRShape} yields a pair of [[adjoint (∞,1)-functors]] 

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


+-- {: .num_prop #TripleOfDeRhamAdjunctions}
###### Proposition

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

+-- {: .num_defn}
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

A [[cocycle]] $\omega : X \to \mathbf{\flat}_{dR}A$ we call a **flat $A$-valued differential form** on $X$.

We say that $H_{dR}(X,A) {:=} \pi_0 \mathbf{H}_{dR}(X,A)$
is the **de Rham cohomology** of $X$ with coefficients in $A$.

=--

+-- {: .num_remark}
###### Observation

A [[cocycle]] in de Rham cohomology

$$
  \omega : \mathbf{\Pi}_{dR}X \to A
$$

is precisely a [flat ∞-connection](#FlatDifferentialCohomology) on a _trivializable_ $A$-principal $\infty$-bundle. More precisely, $\mathbf{H}_{dR}(X,A)$ is the [[homotopy fiber]] of the [[forgetful functor]] from $\infty$-bundles with flat $\infty$-connection to $\infty$-bundles: we have an [[(∞,1)-pullback]]

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

+-- {: .num_prop #deRhamWithDiscCoeffsIsTrivial}
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

+-- {: .num_prop}
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

+-- {: .num_remark}
###### Remark

In summary this means that in a cohesive $(\infty,1)$-topos the objects $\mathbf{\Pi}_{dR} X$ have the abstract properties of [[de Rham schematic homotopy type|pointed geometric de Rham homotopy types]].

In the [Examples](#Examples) we will see that, indeed, the intrinsic de Rham cohomology $H_{dR}(X, A) {:=} \pi_0 \mathbf{H}(\mathbf{\Pi}_{dR} X, A)$ reproduces ordinary de Rham cohomology in degree $d\gt 1$.

In degree 0 the intrinsic de Rham cohomology is necessarily trivial, while in degree 1 we find that it reproduces closed 1-forms, not divided out by exact forms. This difference to ordinary de Rham cohomology in the lowest two degrees may be interpreted in terms of the obstruction-theoretic meaning of de Rham cohomology by which we essentially characterized it above: we have that the intrinsic $H_{dR}^n(X,K)$ is the home for the obstructions to flatness of $\mathbf{B}^{n-2}K$-[[principal ∞-bundle]]s. For $n = 1$ this are groupoid-principal bundles over the _groupoid_ with $K$ as its space of objects. But the 1-form curvatures of groupoid bundles are not to be regarded modulo exact forms. More details on this are at [[circle n-bundle with connection]].

=--

### Integration of differential forms and Stokes lemma
 {#IntegrationOfDifferentialForms}

See at _[integration of differential forms -- In cohesive homotopy-type theory](integration%20of%20differential%20forms#InCohesiveHomotopyTypeTheory)_

### Exponentiated $\infty$-Lie algebras 
 {#LieAlgebras}

We now use the intrinsic non-abelian  de Rham cohomology in the cohesive $(\infty,1)$-topos
$\mathbf{H}$ discussed [above](#deRhamCohomology) to see that there is also an intrinsic notion of _exponentiated higher [[Lie algebra]] objects_ in $\mathbf{H}$. (The fact that for $\mathbf{H} = $ [[Smooth∞Grpd]] these abstractly defined objects are indeed presented by [[L-∞ algebras]] is discussed at _[[smooth ∞-groupoid -- structures]]_.)

The idea is that for $G \in Grp(\mathbf{H})$ an [[∞-group]], a $G$-valued differential form on some $X \in \mathbf{H}$, which by the above is given by a morphism

$$
  A : \mathbf{\Pi}_{dR}(X) \to \mathbf{B}G
$$ 

maps "infinitesimal paths" to elements of $G$, and hence only hits "infinitesimal elements" in $G$. Therefore the object that such forms universally factor through we write $\mathbf{B} \exp(\mathfrak{g})$ and think of as the formal [[Lie integration]] of the $\infty$-Lie algebra of $G$.

The reader should note here that all this is formulated without an explicit ("synthetic") notion of infinitesimals. Instead, it is infinitesimal in the same sense that $\mathbf{\Pi}_{dR}(X)$ is the _[[schematic homotopy type|schematic de Rham homotopy type]]_ of $X$, as discussed above. But if we add a bit more structure to the cohesive $(\infty,1)$-topos $\mathbf{H}$, then these infinitesimals can be realized also synthetically. That extra structure is that of _[[cohesive (infinity,1)-topos -- infinitesimal cohesion|infinitesimal cohesion]]_. See there for more details.


+-- {: .num_def #ExponentiatedLieAsGeometricallyContractible}
###### Definition


For a [[connected]] object $\mathbf{B}\exp(\mathfrak{g}) $ in $\mathbf{H}$ that is _geometrically contractible_

$$
  \Pi (\mathbf{B}\exp(\mathfrak{g})) \simeq *
$$

we call its [[loop space object]] 
$\exp(\mathfrak{g}) := \Omega_* \mathbf{B}\exp(\mathfrak{g})$ the  **[[Lie integration]] of an [[∞-Lie algebra]]** in $\mathbf{H}$. 

=--



+-- {: .num_defn}
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

+-- {: .num_prop #LieAsALeftAdjoint}
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

+-- {: .num_example}
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

where we used that in the [[∞-connected (∞,1)-topos|∞-connected]] $\mathbf{H}$ the functor $Disc$ is [[full and faithful (∞,1)-functor|full and faithful]].

=--

+-- {: .num_corollary}
###### Corollary

We have for every $\mathbf{B}G$ that $\exp Lie \mathbf{B}G$ is geometrically contractible.

=--


We shall write $\mathbf{B}\exp(\mathfrak{g})$ for $\exp Lie \mathbf{B}G$, when the context is clear. 


+-- {: .num_prop #LieValuesofDeRham}
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

By the <a href="http://ncatlab.org/nlab/show/adjoint+functor#UniversalArrows">universality of the counit</a> of $(\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR})$ we have that $\omega$ factors through the [[unit of an adjunction|counit]] 
$\exp Lie \mathbf{B}G \to \mathbf{B}G$. 

=--


Therefore instead of speaking of a $G$-valued de Rham cocycle, it is less  redundant to speak of an $\exp(\mathfrak{g})$-valued de Rham cocycle. In particular we have the following.


+-- {: .num_prop}
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


+-- {: .num_prop}
###### Proposition

If $\mathbf{H}$ is cohesive then we have 

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

+-- {: .num_defn #MaurerCartanForm}
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


+-- {: .num_remark}
###### Remark

By postcomposition the Maurer-Cartan form sends $G$-valued functions on $X$ to $\mathfrak{g}$-valued forms on $X$

$$
  \theta_* : \mathbf{H}(X,G) \to 
    \mathbf{H}^1_{dR}(X,G)
  \,.
$$

=--


+-- {: .num_remark #GActionOnGAndOndRFlatOfG}
###### Remark

For $G$ an [[∞-group]], there are canonical $G$-[[∞-actions]] on $G$ and on $\flat_{dR} \mathbf{B}G$. By the discussion at [[∞-action]] these are exhibited by the defining [[homotopy fiber sequences]]

$$
  \array{
     G &\longrightarrow& \ast
     \\
     && \downarrow
     \\
     && \mathbf{B}G
  }
$$

and

$$
  \array{
     \flat_{dR}\mathbf{B}G &\longrightarrow& \flat \mathbf{B}G
     \\
     && \downarrow
     \\
     && \mathbf{B}G
  }
  \,,
$$

respectively, and they identify the [[homotopy quotients]] of the action as

$$
  \ast \simeq G/G
$$

and

$$
  \flat \mathbf{B}G \simeq (\flat_{dR}\mathbf{B}G)/G
  \,,
$$

respectively.

=--

+-- {: .num_remark #MaurerCartanFormIsGEquivariant}
###### Proposition

For $G$ an [[∞-group]], then the [[Maurer-Cartan form]] $\theta_G \colon G \to \flat_{dR}\mathbf{BG}$ of def. \ref{MaurerCartanForm} naturally carries [[equivariance]] structure with respect to the $G$-[[∞-actions]] of remark \ref{GActionOnGAndOndRFlatOfG}, hence the structure of a [[homomorphism]]/[[intertwiner]] of these [[∞-actions]].

=--

+-- {: .proof}
###### Proof

By the discussion at _[[∞-action]]_ the equivariant structure in question is a morphism of the form

$$
  \array{
    G/G &&\stackrel{\theta/G}{\longrightarrow}&& (\flat_{dR}\mathbf{B}G)/G
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}G
  }
$$

such that it induces $\theta \colon G \to \flat_{dR}\mathbf{B}G$ on [[homotopy fibers]]. 

By remark \ref{GActionOnGAndOndRFlatOfG} the above diagram is equivalently

$$
  \array{
    \ast &&\stackrel{\theta/G}{\longrightarrow}&& \flat\mathbf{B}G
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}G
  }
  \,.
$$

There is an essentially unique horizontal morphism $\theta/G$ making this commute (up to homotopy). To see that this does induce the Maurer-Cartan form $\theta$ on homotopy fibers, notice that the morphism on homotopy fibers is the universal one from the total homotopy pullback diagram to the bottom homotopy pullback diagram labeled $\theta$ in

$$
  \array{
    G && \longrightarrow && \ast
    \\
    & \searrow^{\mathrlap{\theta}} && && \searrow^{\mathrlap{\theta/G}}
    \\
    \downarrow && \flat_{dR}\mathbf{B}G && \longrightarrow && \flat \mathbf{B}G
    \\
    & \swarrow && && \swarrow   
    \\
    \ast && \longrightarrow && \mathbf{B}G
  }
$$

The [[pasting law]] implies that also the top rectangle here, is a homotopy pullback, hence this identifies $\theta$ in this diagram indeed as the MC form.

=--


+-- {: .num_defn #UniversalCurvatureForms}
###### Definition


For $G = \mathbf{B}^n A$ an [[Eilenberg-MacLane object]], we also write 

$$
  curv : \mathbf{B}^n A \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} A
$$

for the intrinsic Maurer-Cartan form and call this the intrinsic **universal [[curvature characteristic form]]** on $\mathbf{B}^n A$.

=--

### Flat Ehresmann connections
 {#FlatEhresmannConnections}

We discuss now a general abstract notion of flat [[Ehresmann connections]] 
in a cohesive $(\infty,1)$-topos $\mathbf{H}$.

Let $G \in Grp(\mathbf{H})$ be an [[∞-group]]. 
For $g : X \to \mathbf{B}G$ a [[cocycle]] that modulates a $G$-[[principal ∞-bundle]] $P \to X$, we saw [above](#FlatDifferentialCohomology) that lifts

$$
  \array{
    && \flat \mathbf{B}G
    \\
    & {}^{\mathllap{\nabla}}\nearrow & \downarrow
    \\
    X &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

modulate flat $\infty$-connections $\nabla$ in $P \to X$. 

We can think of $\nabla : X \to \flat \mathbf{B}G$ as the cocycle datum for the connection on base space, in generalization of the discussion at _[[connection on a bundle]]_. On the other hand, there is the classical notion of an [[Ehresmann connection]], which instead encodes such connection data in terms of differential form data on the total space $P$.

We may now observe that such differential form data on $P$ is identified with the [[twisted ∞-bundle]] induced by the lift, with respect to the [[local coefficient ∞-bundle]] given by the [[fiber sequence]]

$$
  \array{
     \flat_{dR} \mathbf{B}G &\to& \flat \mathbf{B}G
     \\
     && \downarrow
     \\
     && \mathbf{B}G
  }
$$

that defines the de Rham coefficient object, discussed [above](#deRhamCohomology).

Notice also that the $\flat_{dR}\mathbf{B}G$-[[twisted cohomology]] defined by this local coefficient bundle says that: _flat $\infty$-connections are locally flat $Lie(G)$-valued forms that are globally twisted by by a $G$-principal $\infty$-bundle._


By the general discussion at [[twisted ∞-bundle]] we find that the flat connection $\nabla$ induces on $P$ the structure

$$
  \array{
    G &\to& P &\stackrel{A}{\to}& \flat_{dR} \mathbf{B}G
    \\
    \downarrow && \downarrow && \downarrow 
    \\
    * &\stackrel{x}{\to}& X &\stackrel{\nabla}{\to}& \flat \mathbf{B}G &\stackrel{}{\to}& \mathbf{B}G
  }
$$

consisting of

* a (flat) $Lie(G)$-valued form datum $A : P \to \flat_{dR}\mathbf{B}G$ on the total space $P$

* such that this intertwines the $G$-actions on $P$ and on $\flat_{dR}\mathbf{B}G$.

In the model $\mathbf{H}$ = [[Smooth∞Grpd]] one finds that the last condition reduces indeed to that of an [[Ehresmann connection]] for $A$ on $P$ (this is discussed [here](smooth+infinity-groupoid+--+structures#FlatEhresmannConnections)). One of the two Ehresmann conditions is manifest already abstractly: for every point $x : * \to X$ of base space, the restriction of $A$ to the fiber of $P$ over $X$ is the Maurer-Cartan form

$$
  \theta : G \to P \stackrel{A}{\to} \flat_{dR} \mathbf{B}G
$$

on the $\infty$-group $G$, discussed [above](#CurvatureCharacteristics).


### Differential cohomology 
 {#DifferentialCohomology}


#### Ordinary differential cohomology

In every [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] [[∞-connected (∞,1)-topos]] there is an intrinsic notion of [[ordinary differential cohomology]].

Fix a 0-[[truncated]] [[abelian group|abelian]] [[group object]] $A \in \tau_{\leq 0} \mathbf{H} \hookrightarrow \mathbf{H}$. For all $n \in \mathbf{N}$ we have then the [[Eilenberg-MacLane object]] $\mathbf{B}^n A$.

+-- {: .num_defn }
###### Definition 

For $X \in \mathbf{H}$ any object and $n \geq 1$ write

$$
  \mathbf{H}_{diff}(X,\mathbf{B}^n A) := 
    \mathbf{H}(X,\mathbf{B}^n A) \prod_{\mathbf{H}_{dR}(X,\mathbf{B}^n A)}
    H_{dR}^{n+1}(X,A)
$$ 

for the cocycle $\infty$-groupoid of [[twisted cohomology]], def. \ref{TwistedCohomologyInOvertopos}, of $X$ with coefficients in $A$ and with twist given by the canonical [curvature characteristic morphism](#CurvatureCharacteristics) 
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

+-- {: .num_prop #DiffCohIsWellDefined}
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

+-- {: .num_prop #DiffCohomologyRestrictedToVanishingCurvature}
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

By the <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-pullback#QuasiCatPastingLaw">pasting law for (∞,1)-pullbacks</a> the claim is equivalently that we have an $(\infty,1)$-pullback diagram

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

that [defines](#CurvatureCharacteristics) $curv$ (using that $\mathbf{\flat}$ preserves limits and hence looping and delooping).


=--

The following establishes the characteristic [[short exact sequences]] that characterizes intrinsic [[differential cohomology]] as an extension of curvature forms by flat $\infty$-bundles and of bare $\infty$-bundles by connection forms.

+-- {: .num_prop #CurvatureExactSequence}
###### Proposition

Let $im F \subset H_{dR}^{n+1}(X, A)$ be the [[image]] of the curvatures. Then the differential cohomology group $H_{diff}^n(X,A)$ fits into a [[short exact sequence]]

$$
  0 \to H^n_{flat}(X, A) \to H^n_{diff}(X,A) \to im F \to 0
$$

=--

+-- {: .proof}
###### Proof

Apply the [[long exact sequence of homotopy groups]] to the [[fiber sequence]] 

$$
  \mathbf{H}_{flat}(X, \mathbf{B}^n A)
    \to 
  \mathbf{H}_{diff}(X, \mathbf{B}^n A)
   \stackrel{[F]}{\to}
  H_{dR}^{n+1}(X,A)
$$

of prop. \ref{DiffCohomologyRestrictedToVanishingCurvature} and use that $H_{dR}^{n+1}(X,A)$ is, as a set, a [[homotopy n-type|homotopy 0-type]] to get the [[short exact sequence]]

$$
  \array{
    \pi_1(H_{dR}(X,A))  
     &\to& 
    \pi_0(\mathbf{H}_{flat}(X, \mathbf{B}^n A))
     &\to& 
    \pi_0(\mathbf{H}_{diff}(X, \mathbf{B}^n A))
     &\stackrel{[F]}{\to}&
    \pi_0(H_{dR}^{n+1}(X,A))
    \\
    = && = && = && \downarrow
    \\
    0 
      &\to& 
    H_{flat}^n(X, A) 
      &\to& 
    H_{diff}^n(X,A)
      &\to&
    im [F]
  }
  \,.
$$

=--

+-- {: .num_prop #CharacteristicClassExactSequence}
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


+-- {: .num_remark}
###### Remark

This is essentially the short exact sequence whose form is familiar from the traditional definition of [[ordinary differential cohomology]] only up to the following slight nuances in notation:

1.  The cohomology groups of the short exact sequence above denote the groups obtained in the given [[(∞,1)-topos]] $\mathbf{H}$, not in [[Top]]. Notably for $\mathbf{H} = $ [[∞LieGrpd]], $A = U(1) =\mathbb{R}/\mathbb{Z}$
the [[circle group]] and $|X| \in Top$ the [[geometric realization]] of a paracompact manifold $X$, we have that $H^n(X,\mathbb{R}/\mathbb{Z})$ above is $H^{n+1}_{sing}({|\Pi X|},\mathbb{Z})$. 

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

For a detailed discussion of the relation to [[ordinary differential cohomology]] see at _[[smooth ∞-groupoid]]_ the section <a href="http://nlab.mathforge.org/nlab/show/smooth infinity-groupoid#DiffCohomologyAbstractProperties">Abstract properties of differential cohomology</a>.

=--

In view of the second of these points one can make a _choice_ of cover in order to present the twisting cocycles functorially. To that end, let

$$
  \Omega^{n+1}_{cl}(-,A) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}A
$$

denote a choice of [[effective epimorphism in an (∞,1)-category|effective epimorphism]] out of a [[0-truncated]] object which we suggestively denote by $\Omega^{n+1}_{cl}(-,A)$.

+-- {: .num_defn }
###### Definition

With a choice $\Omega^{n+1}_{cl}(-,A) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}A$ 
fixed, we say an object $X \in \mathbf{H}$ is **dR-[[projective object|projective]]** if the induced morphism

$$
  \mathbf{H}(X, \Omega^{n+1}_{cl}(-,A))
  \to 
  \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B}^{n+1}A)
$$

is itself an [[effective epimorphism in an (∞,1)-category|effective epimorphism]] (of [[∞-groupoid]])s.

=--


+-- {: .num_remark }
###### Remark

A morphism of $\infty$-groupoids is an effective epimorphism precisely if it is surjective on $\pi_0$ (see [here](http://ncatlab.org/nlab/show/effective+epimorphism+in+an+%28infinity%2C1%29-category#EffectiveEpisOfInfinityGroupoids)). Since $\Omega^{n+1}_{cl}(-,A)$ is assumed to be [[0-truncated]], also 


$$
  \Omega^{n+1}_{cl}(X,A) := \mathbf{H}(X, \Omega^{n+1}_{cl}(-,A))
$$ 

is 0-truncated. Hence $X$ is dR-projective precisely if the set $\Omega^{n+1}_{cl}(X,A)$ contains representatives of all intrinsic de Rham cohomology classes of $X$.

In terms of [[hypercohomology]] this may be thought of as saying that $X$ is dR-projective if every de Rham hypercohomology class on $X$ has a representative by a globally defined differential form. In models of cohesion we typically have that [[manifolds]] are dR-projective, but nontrivial [[orbifold]]s are not.

=--

+-- {: .num_defn }
###### Definition

Write $\mathbf{B}^n A_{conn}$ for the $\infty$-pullback

$$
  \array{
  \mathbf{B}^n A_{conn}
  &
  \stackrel{}{\to}
  &
  \Omega^{n+1}_{cl}(-,A)
  \\ 
  \downarrow && \downarrow
  \\
  \mathbf{B}^n A
  &
  \stackrel{curv}{\to}
  &
  \mathbf{\flat}_{dR}\mathbf{B}^{n+1}A
  }
  \,.
$$

We say that this is the **differential coefficient object** of $\mathbf{B}^n A$.

=--

+-- {: .num_remark }
###### Remark

For every dR-projective $X \in \mathbf{H}$ there is a canonical 
[[monomorphism in an (∞,1)-category|monomorphism]]

$$
  \mathbf{H}_{diff}(X,\mathbf{B}^n A)
  \to 
  \mathbf{H}(X, \mathbf{B}^n A_{conn})
  \,,
$$



=--

+-- {: .proof}
###### Proof

Consider the diagram

$$
  \array{
    \mathbf{H}(X, \mathbf{B}^n A_{\mathrm{conn}})
    &
    \stackrel{}{\to}
    &
    \Omega^{n+1}_{cl}(-,A)
    \\ 
    \downarrow && \downarrow
    \\
    \mathbf{H}_{diff}(X,\mathbf{B}^n A)
    &
     \stackrel{}{\to}
    &
    H_{dR}^{n+1}(X,A)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X, \mathbf{B}^n A)   
    &
    \stackrel{}{\to}
    &
    \mathbf{H}(X, \mathbf{\flat}_{dR}\mathbf{B}^{n+1}A)
  }
  \,.
$$

The bottom square is an [[∞-pullback]] by definition. 
A morphism as in the top right exists by assumption that
$X$ is dR-prohective. Let also the
top square be an $\infty$-pullback. Then by the [[pasting law]]
so is the total rectangle, which identifies the top left object 
as indicated, since $\mathbf{H}(X,-)$ preserves $\infty$-pullbacks.

Since the top right morphism is in injection of sets, it is a 
monomorphism of $\infty$-groupoids. These are stable under $\infty$-pullback,
which proves the claim.

=--

#### Generalized differential cohomology

For cohesive [[stable homotopy types]] the above discussion may be refined and stream-lined considerably. For more on this see at _[[differential cohomology diagram]]_.


### Chern-Weil homomorphism and $\infty$-connections 
 {#ChernWeilTheory}

Induced by the [intrinsic differential cohomology](#DifferentialCohomology) in any [[∞-connected (∞,1)-topos|∞-connected]] and [[locally ∞-connected (∞,1)-topos]] is an intrinsic notion of [[Chern-Weil homomorphism]].

Let $A$ be the chosen abelian [[∞-group]] as [above](#DifferentialCohomology). Recall the [universal curvature characteristic class](#CurvatureCharacteristics)

$$
  curv : \mathbf{B}^n A \to \mathbf{\flat}_{dR}\mathbf{B}^{n+1}A
$$

for all $n \geq 1$.

+-- {: .num_defn}
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


+-- {: .num_defn}
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

+-- {: .num_prop}
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

As before for abelian coefficients, we introduce differential 
coefficient objects $\mathbf{B}G_{conn}$ that represent these differential cohomology classes 
over dR-projective objects

$$
  \array{
    \mathbf{\flat}\mathbf{B}G
    &
    \stackrel{\mathbf{\flat}\mathbf{c}}{\to}
    &
    \mathbf{\flat}\mathbf{B}^{n+1} A
    \\
    \downarrow 
    &&
    \downarrow
    \\
    \mathbf{B}G_{conn}
    &
    \stackrel{\hat {\mathbf{c}}}{\to}
    &
    \mathbf{B}^{n+1}A_{conn}
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G
    &\stackrel{\mathbf{c}}{\to}&
    \mathbf{B}^{n+1}A
  }
  \,.
$$

(...)

### Higher holonomy 
 {#HigherHolonomy}

The notion of [intrinsic ∞-connections](#ChernWeilTheory) in a 
cohesive $(\infty,1)$-topos induces a notion of [[higher parallel transport|higher holonomy]] 

+-- {: .num_defn #CohomologicalDimension}
###### Definition

We say an object $\Sigma \in \mathbf{H}$ has **[[cohomological dimension]]** $\leq n \in \mathbb{N}$ if for all $n$-[[connected]] and $(n+1)$-[[truncated]] objects $\mathbf{B}^{n+1}A$ the corresponding [[cohomology]] on $\Sigma$ is trivial

$$
  H(\Sigma, \mathbf{B}^{n+1}A ) \simeq *
  \,.
$$

Let $dim(\Sigma)$ be the maximum $n$ for which this is true.

=--





+-- {: .num_prop}
###### Observation

If $\Sigma \in \mathbf{H}$ has [cohomological dimension](#CohomologicalDimension) $\leq n$ then its  [intrinsic de Rham cohomology](#deRhamCohomology) vanishes in degree $k \gt n$

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




+-- {: .num_defn}
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


The **[[higher parallel transport|holonomy]]** of $\nabla$ over $\sigma$ is the flat holonomy of $\phi^* \nabla$

$$
  \int_\phi \nabla := \int_{\Sigma} \phi^* \nabla
  \,.
$$ 

=--

### Transgression in differential cohomology
 {#Transgression}

We discuss an intrinsic notion of 
[[transgression]]/[[fiber integration in ordinary differential cohomology]]
internal to any cohesive $(\infty,1)$-topos. This generalizes the notion
of [[higher holonomy]] discussed above.

Fix $A$ an abelian group object as above and $\mathbf{B}^n A_{conn}$
a corresponding differential coefficient object. Then for
$\Sigma \in \mathbf{H}$ of [[cohomological dimension]]
$k \leq n$ consider the map

$$
  [\Sigma, \mathbf{B}^n A_{conn}]
  \stackrel{conk_k \circ \tau_{n-k}}{\to}
  conk_{n-k} \tau_{n-k}
  [\Sigma, \mathbf{B}^n A_{conn}]
  \,.
$$


* $[-,-]$ denotes the <a href="http://nlab.mathforge.org/nlab/show/%28infinity,1%29-topos#ClosedMonoidalStructure">cartesian internal hom</a>;

* $\tau_{n-k}$ denotes [[truncated object in an (infinity,1)-category|truncation]] in degree $n-k$;

* $conk_{n-k}$ denotes [concretification](#ConcreteObjects) in degree $(n-k)$.


In typical models we have an equivalence

$$
  conk_k \tau_{n-k}
  [\Sigma, \mathbf{B}^n A_{conn}]
  \simeq
  \mathbf{B}^{n-1} A_{conn}
  \,.
$$

In this case we say that for 

$$
  \hat \mathbf{c} : \mathbf{B}G_{conn} \to \mathbf{B}^n A_{conn}
$$

a differential characteristic map, that the composite

$$
  \exp(i \int_{\Sigma}(-))
  : 
  [\Sigma, \mathbf{B} G_{conn}]
  \to 
  [\Sigma, \mathbf{B}^n A_{conn}]
  \to
  \mathbf{B}^{n-k}A_{conn}
$$

is the **transgression** of $\hat \mathbf{c}$ to the 
[[mapping space]] $[\Sigma, \mathbf{B} G_{conn}]$.

For $k = n$ the reproduces, on the underlying $\infty$-groupoids,
the [[higher holonomy]] discussed above.

(...)

### Chern-Simons functional 
  {#ChernSimonsTheory}


The notion of [intrinsic ∞-connections](#ChernWeilTheory) 
and their [higher holonomy](#HigherHolonomy) in a 
cohesive $(\infty,1)$-topos induces an intrinsic notion of
and [[schreiber:∞-Chern-Simons theory|higher Chern-Simons functionals]].


+-- {: .num_defn}
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

The cohesive refinement of this (...more discussion required...)

$$
  \int_\Sigma
    :
  [\Sigma, X] 
   \stackrel{}{\to}
  [\Sigma, \mathbf{B}^n A]_{diff}
   \stackrel{}{\to}
  conc_{n-dim \Sigma} [\Sigma, \mathbf{B}^n A]_{diff}
    \stackrel{\simeq}{\to}
  conc_{n-dim \Sigma} [\Sigma, \mathbf{\flat}\mathbf{B}^n A]
   \stackrel{}{\to}
  \tau_{n - \dim \Sigma} conc_{n-dim \Sigma} [\Sigma, \mathbf{\flat}\mathbf{B}^n A]
  \,,
$$

where

* $[-,-]$ denotes the <a href="http://nlab.mathforge.org/nlab/show/%28infinity,1%29-topos#ClosedMonoidalStructure">cartesian internal hom</a>;

* $[\Sigma, \mathbf{B}^n A]_{diff} \stackrel{}{\to} conc_{n-dim \Sigma} [\Sigma, \mathbf{B}^n A]_{diff}$ is the [concretification projection](#NConcretification) in degree $n - dim \Sigma$

* $conc_{n-dim \Sigma} [\Sigma, \mathbf{\flat}\mathbf{B}^n A] \stackrel{}{\to} \tau_{n - \dim \Sigma} conc_{n-dim \Sigma} [\Sigma, \mathbf{\flat} \mathbf{B}^n A]$ is the [[truncated|truncation projection]] in the same degree

we call the **smooth [[schreiber:∞-Chern-Simons theory|extended Chern-Simons functional]]**.

=--

+-- {: .num_defn}
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

## Related concepts

* [[!include cohesion - table]]
* [[concretification]]


## References

### General

For general references on [[cohesive (∞,1)-toposes]] see there.

The above list of structures in any cohesive $(\infty,1)$-topos is the topic of section 2.3 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_  
 {#dcct}

### Formulation in homotopy type theory

For formalizations of some structures in cohesive $(\infty,1)$-toposes in terms of [[homotopy type theory]] see _[[cohesive homotopy type theory]]_.




[[!redirects cohesive (∞,1)-topos -- structures]]

[[!redirects structures in a cohesive (∞,1)-topos]]

[[!redirects structures in a cohesive infinity-topos]]

[[!redirects cohesive topos -- structures]]
[[!redirects cohesive infinity-topos -- structures]]