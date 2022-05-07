
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

>  This is a subsection of the entry [[cohesive (∞,1)-topos]]. See there for background and context.

***

#Contents#
* table of contents
{:toc}

## Idea

A [[cohesive (∞,1)-topos]] is a context of [[∞-groupoid]]s that are equipped with a [[geometry|geometric]] notion of _cohesion_ on their collections of [[object]]s and [[k-morphism]]s, for instance [[Euclidean-topological ∞-groupoid|topological cohesion]] or [[smooth ∞-groupoid|smooth cohesion]].

While the axioms of cohesion do imply the intrinsic existence of _exponentiated_ [[infinitesimal spaces]], they do not admit access to an explicit [[synthetic differential geometry|synthetic]] notion of infinitesimal extension.

Here we consider one extra axiom on a [[cohesive (∞,1)-topos]] that does imply a good intrinsic notion of synthetic differential extension, compatible with the given notion of cohesion. We speak of *differential cohesion*.

In a cohesive $(\infty,1)$-topos with differential cohesion there are for instance good intrinsic notions of [[formally smooth morphism|formal smoothness]] and of [[de Rham space]]s of objects.

## Differential cohesion

We discuss [[extra structure]] on a [[cohesive (∞,1)-topos]]
that encodes a refinement of the corresponding notion of cohesion to
_[[infinitesimal object|infinitesimal]] cohesion_ . More precisely, we consider inclusions
$\mathbf{H} \hookrightarrow \mathbf{H}_{th}$ of cohesive

$(\infty,1)$-toposes that exhibit the objects of $\mathbf{H}_{th}$
as infinitesimal cohesive neighbourhoods of objects in
$\mathbf{H}$.

### Definition
 {#Definition}


+-- {: .num_defn #InfinitesimalCohesiveInfTopos}

###### Definition

Given a cohesive $(\infty,1)$-topos $\mathbf{H}$ we say that
an **infinitesimal cohesive neighbourhood** of $\mathbf{H}$
is another cohesive $(\infty,1)$-topos $\mathbf{H}_{th}$
equipped with an  [[adjoint quadruple]] of [[adjoint (∞,1)-functors]] of the form

$$
  (i_! \dashv i^* \dashv i_* \dashv i^!) :
  \mathbf{H}
    \stackrel{\overset{i_!}{\hookrightarrow}}{\stackrel{\overset{i^*}{\leftarrow}}{\stackrel{\overset{i_*}{\hookrightarrow}}{\underset{i^!}{\leftarrow}}}}
  \mathbf{H}_{th}
$$

where $i_!$ is  a [[full and faithful (∞,1)-functor|full and faithful]] and preserves [[finite products]].

Conversely we will say that data as in def. \ref{InfinitesimalCohesiveInfTopos} equips the cohesive $\infty$-topos $\mathbf{H}$ with **differential cohesion**.

=--




+-- {: .num_remark}
###### Remark

This definition is an abstraction of similar situations considered in ([SimpsonTeleman](#SimpsonTeleman)) and in [Kontsevich-Rosenberg](#KontsevichRosenbergSpaces). See also the section [Infinitesimal thickening](Q-category#InfinitesimalThickening) at [[Q-category]].

=--

+-- {: .num_remark #InfinitesimalInclusionIfFullAndFaithful}
###### Remark

This implies that also $i_*$ is a [[full and faithful (∞,1)-functor]].

=--

+-- {: .proof}
###### Proof

By the characterizaton of full and faithful [[adjoint (∞,1)-functor]]s
the condition on $i_!$ is equivalent to $i^* i_! \simeq Id$. Since $(i^* i_! \dashv i^* i_*)$ it follows by essential uniqueness of [[adjoint (∞,1)-functor]]s that also $i^* i_* \simeq Id$.

=--

+-- {: .num_remark}
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

+-- {: .num_prop #InfinitesimalNeighbourhoodIsOverInfGroupoid}
###### Proposition

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
  \stackrel{\overset{\Pi_{inf}}{\longrightarrow}}{\stackrel{\overset{Disc_{inf}}{\leftarrow}}{\underset{\Gamma_{inf}}{\longrightarrow}}}
  \mathbf{H}
  \stackrel{\overset{\Pi_{\mathbf{H}}}{\longrightarrow}}{\stackrel{\overset{Disc_{\mathbf{H}}}{\longleftarrow}}{\underset{\Gamma_{\mathbf{H}}}{\longrightarrow}}}
  \infty Grpd
  \,.
$$

We also consider the [[(∞,1)-monads]]/comonads induced from these reflections:

1. the [[reduction modality]] $\Re \coloneqq i_! i^\ast$ ;

1. the [[infinitesimal shape modality]] $\Im \coloneqq i_\ast i^\ast$;

1. the [[infinitesimal flat modality]] ${\&}  \coloneqq i_* i^!$.

The above says that these interact with the modalities of the ambient cohesion, i.e.

1. the [[shape modality]] $&#643;$;

1. the [[flat modality]] $\flat$;

1. the [[sharp modality]] $\sharp$

as follows:

$$
   \array{
      && && \Re
      \\
     && && \bot
      \\
      && &#643; & \subset & \Im
      \\
      && \bot && \bot
      \\
      \emptyset &\subset& \flat & \subset & {\&}
      \\
      \bot & & \bot &&
      \\
      \ast & \subset& \sharp
   }
$$

Here the inclusion sign $\subset$ is to mean that the [[modal types]] of the modality on the left are included in the modal types of the modality on the right.

For more details on this, see at _[[geometry of physics -- categories and toposes]]_ the section _[Elastic toposes](geometry+of+physics+--+categories+and+toposes#ElasticToposes)_.

Let for the remainder of this section an infinitesimal neighbourhood $\mathbf{H} \hookrightarrow \mathbf{H}_{th}$ be fixed.

+-- {: .num_remark #SequenceOfOrdersOfInfinitesimals}
###### Remark

More generally we may ask for a sequence of differential inclusions of $\infty$-toposes as above, reflecting ever higher orders of infinitesimals, hence notably a progression 

$$
  &#643;
  \lt
  \Im
  =
  \Im_{(\infty)}
  \lt
  \cdots
  \lt
  \Im_{(3)}
  \lt
  \Im_{(2)}
  \lt
  \Im_{(1)}
  \lt
  id
$$

of [[infinitesimal shape modalities]] of various order, yielding a further factorization of the shape unit as

$$
  X \to \Im_{(1)}X \to \Im_{(2)}X 
   \to \Im_{(3)} X  \to \cdots \to \Im X \to &#643; X
  \,.
$$



=--


### Properties
 {#Properties}

#### From $\infty$-sheaves over infinitesimal neighbourhood sites
 {#PresentationOnInfinitesimalNeighbourhoodSites}

We give a presentation of classes of infinitesimal neighbourhoods by [[simplicial presheaves]] on suitable [[sites]].

+-- {: .num_defn #InfinitesimalNeighBourhoodSite}
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


+-- {: .num_prop #InfinitesimalNeighbourhoodFromInfinitesimalSite}
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
    \stackrel{\overset{Lan_i}{\longrightarrow}}{\stackrel{\overset{(-)\circ i}{\longleftarrow}}{\stackrel{\overset{(-)\circ p}{\longrightarrow}}{\underset{Ran_p}{\longleftarrow}}}}

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
   \stackrel{\overset{(-)\circ i}{\longleftarrow}}
    {\underset{(-)\circ p}{\longrightarrow}}
  [C_{th}^{op}, sSet]_{proj}
  \,;
$$

$$
  ((-) \circ p \dashv Ran_p) :
  [C^{op}, sSet]_{inj}
   \stackrel{\overset{(-)\circ p}{\longrightarrow}}{\underset{Ran_p}{\longleftarrow}}
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
[[Kan extension]] (see the properties discussed there) along a [[full and faithful functor]] $i$ satisfies $Lan_i \circ i \simeq id$. It remains to observe that since $(-)\circ i$ is not only right but also left Quillen by the above, we have that $i^* Lan_i$ applied to a cofibrant object is already the [[derived functor]] of the composite.


=--


+-- {: .num_remark}
###### Remark

Conversely this implies that $Sh_{(\infty,1)}(C_{th})$ is an [[∞-connected (∞,1)-topos]] over [[Smooth∞Grpd]], exhibited by the triple of adjunctions

$$
  (i^* \dashv i_* \dashv i^!) :
  SynthDiff \infty Grpd \to Smooth \infty Grpd
  \,.
$$


=--



#### Relation to infinitesimal cohesion
 {#RelationToInfinitesimalCohesion}

We discuss how differential cohesion in the sense of def. \ref{InfinitesimalCohesiveInfTopos} relates to [[infinitesimal cohesion]].

> under construction

+-- {: .num_defn #InducedRelativeShapeAndFlat}
###### Definition

Given differential cohesion, def. \ref{InfinitesimalCohesiveInfTopos},

$$
  \array{
     \Re &\dashv& \Im &\dashv& {\&}
     \\
     && \vee && \vee
     \\
     && &#643; &\dashv& \flat &\dashv& \sharp
  }
$$

define operations $&#643;^{rel}$ and $\flat^{rel}$ by

$$
  &#643;^{rel} X \coloneqq (&#643; X) \underset{\Re X}{\coprod} X
$$

$$
  \flat^{rel} X \coloneqq (\flat X) \underset{\Im}{\times} X
  \,.
$$

Hence $&#643;^{rel} X$ makes a [[homotopy pushout]] square

$$
  \array{
    \Re X &\longrightarrow& X
    \\
    \downarrow && \downarrow
    \\
    &#643; X &\longrightarrow& &#643;^{rel} X
  }
$$

and $\flat^{rel}$  makes a [[homotopy pullback]] square

$$
  \array{
    \flat^{rel} X &\longrightarrow& X
    \\
    \downarrow && \downarrow
    \\
    \flat X &\longrightarrow& \Im X
  }
  \,.
$$

We call $&#643;^{rel}$ the _[[relative shape modality]]_ and $\flat^{rel}$ the _[[relative flat modality]]_.

=--

+-- {: .num_prop}
###### Proposition

The relative shape and flat modalities of def. \ref{InducedRelativeShapeAndFlat}

1. form an [[adjoint pair]] $(&#643;^{rel} \dashv \flat^{rel})$;

1. whose (co-)[[modal types]] are precisely the properly infinitesimal types, hence those for which $\flat \to \Im$ is an [[equivalence]];

1. $&#643;^{rel}$ preserves the [[terminal object]].

=--

It follows that when $\flat^{rel}$ has a further [[right adjoint]] $\sharp^{rel}$ with equivalent [[modal types]] containing the [[codiscrete object|codiscrete types]], then this defines a [[level of a topos|level]]

$$
  \array{
     \flat^{rel} &\dashv& \sharp^{rel}
     \\
     \vee && \vee
     \\
     \flat &\dashv& \sharp
     \\
     \vee && \vee
     \\
     \emptyset &\dashv& \ast
  }
$$

hence an intermediate subtopos
$\infty Grpd \hookrightarrow \mathbf{H}_{infinitesimal}\hookrightarrow \mathbf{H}_{th}$ which is [[infinitesimal cohesion|infinitesimally cohesive]].

This happens notably for the model of [[formal smooth ∞-groupoids]] and all its variants such as formal [[complex analytic ∞-groupoids]] etc. But in this case $(\flat^{rel} \dashv \sharp^{rel})$ does not provide  [[Aufhebung]] for $(\flat \dashv \sharp)$.

(...)

+-- {: .num_prop #CounitOfFlatRelIsFormallyEtale}
###### Proposition

The [[counit of a comonad|counit]] of the relative flat modality is a [[formally étale morphism]].


=--

+-- {: .proof}
###### Proof

From the fact that the [[infinitesimal shape modality]] is [[idempotent monad|idempotent]] and preserves [[homotopy pullbacks]].

=--



### Structures in a differential cohesive $(\infty,1)$-topos
 {#StructuresInDifferentialCohesion}

We discuss structures that are canonically present in
a cohesive $(\infty,1)$-topos equipped with differential cohesion. These structures parallel the [structures in a general cohesive (∞,1)-topos](#Structures).




#### Infinitesimal paths and de Rham spaces
  {#InfinitesimalPaths}

In the presence of [differential cohesion](#InfinitesimalCohesiveInfTopos) there is an infinitesimal analog of the [geometric paths ∞-groupoids](#Paths).

##### Infinitesimal path $\infty$-groupoid

+-- {: .num_defn #InfinitesimalPathsAndReduction}
###### Definition

Define the [[adjoint triple]] of [[adjoint (∞,1)-functor]]s corresponding to the [[adjoint quadruple]] $(i_! \dashv i^* \dashv i_* \dashv i^!)$:

$$
 (\Re \dashv \Im \dashv \& )
 :
 (i_! i^* \dashv i_* i^* \dashv i_* i^! )
  :
 \mathbf{H}_{th}
  \to
 \mathbf{H}_{th}
  \,.
$$

We say that

* $\Re$ is the **[[reduction modality]]**.

* $\Im$ is the **[[infinitesimal shape modality]]**.

* $\& $ is the **[[infinitesimal flat modality]]**.

An object in the full sub-$\infty$-category

* of $\Re$ we call a **[[reduced object]]**

* of $\Im$ we call a **[[coreduced object]]**.

For $X\in \mathbf{H}_{th}$ we say that

* $\Im(X)$ is the **[[infinitesimal path ∞-groupoid]]**
  of $X$;


  The $(i^* \dashv i_*)$-[[unit of an adjunction|unit]]

  $$
    X \to \Im(X)
  $$




  we call the **constant infinitesimal path inclusion**.

* $\Re(X)$ is the **[[reduced cohesive ∞-groupoid]]** underlying
  $X$.

  The $(i_* \dashv i^*)$-[[unit of an adjunction|counit]]

  $$
    \Re X \to X
  $$


  we call the **inclusion of the reduced part** of $X$.

=--

+-- {: .num_remark #TerminologyDeRhamspace}
###### Remark


In traditional contexts see ([SimpsonTeleman, p. 7](#SimpsonTeleman)) the object $\Im(X)$ is called the **[[de Rham space]] of $X$** or the **de Rham stack of $X$** .
Here we may tend to avoid this terminology, since by the discussion at <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#deRhamCohomology">cohesive (∞,1)-topos -- de Rham cohomology</a> we have a good notion of intrinsic [[de Rham cohomology]] in any [[cohesive (∞,1)-topos]] already without equipping it with differential cohesion. From this point of view the object $\Im(X)$ is not primarily characterized by the fact that (in some models, see [below](#Examples)) it does co-represent de Rham cohomology -- because the object $\mathbf{\Pi}_{dR}(X)$ from [above](#deRhamCohomology) does, too -- but by the fact that it does so in an explicitly ([[synthetic differential geometry|synthetic]]) infinitesimal way.

=--

+-- {: .num_prop #InclusionOfConstantIntoInfinitesimalIntoAllPaths}

###### Observation

There is a canonical [[natural transformation]]

$$
  \Im(X) \to \int(X)
$$

that factors the finite path inclusion through the infinitesimal one

$$
  \array{
    && \Im(X)
    \\
    & \nearrow && \searrow
    \\
    X &&\to&& \int(X)
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is the formula for the [[unit of an adjunction|unit]] of the composite adjunction
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



##### Jet $\infty$-bundles
 {#JetBundleObjects}

Notice that for $f : X \to Y$ any [[morphism]] in any [[(∞,1)-topos]] $\mathbf{H}$, there is the corresponding [[base change geometric morphism]] between the [[over-(∞,1)-toposes]]

$$
  (f^* \dashv f_*) : \mathbf{H}/X \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}} \mathbf{H}/Y
  \,.
$$


+-- {: .num_defn }
###### Definition

For any object $X \in \mathbf{H}$ write

$$
  Jet : \mathbf{H}/X \stackrel{\overset{i^*}{\leftarrow}}{\underset{i_*}{\to}}
  \mathbf{H}/\Im(X)
$$

for the [[base change geometric morphism]] induced by the constant infinitesimal path inclusion $i : X \to \Im(X)$, def. \ref{InfinitesimalPathsAndReduction}.

For $(E \to X) \in \mathbf{H}/X$ we call $Jet(E) \to \Im(X)$ as well as its pullback $i^* Jet(E) \to X$ (depending on context) the **[[jet bundle]]** of $E \to X$.

=--


##### Formally smooth/&#233;tale/unramified morphisms

 {#FormallySmoothEtaleUnramified}

+-- {: .num_defn #FormalSmoothness}
###### Definition

We say an object $X \in \mathbf{H}_{th}$ is **formally smooth** if the constant infinitesimal path inclusion, $X \to \Im(X)$, def. \ref{InfinitesimalPathsAndReduction},

is an [[effective epimorphism in an (∞,1)-category|effective epimorphism]].


=--

In this form this is the evident $(\infty,1)$-categorical analog of the conditions as they appear for instance in ([SimpsonTeleman, page 7](#SimpsonTeleman)).

+-- {: .num_remark #FormalSmoothnessByCanonicalMorphism}
###### Remark

An object $X \in \mathbf{H}_{th}$ is formally smooth according to def. \ref{FormalSmoothness} precisely if the canonical morphism

$$
  i_! X \to i_* X
$$

(induced from the [[adjoint quadruple]] $(i_! \dashv i^* \dashv i_* \dashv i^!)$, see there) is an [[effective epimorphism in an (∞,1)-category|effective epimorphism]].

=--

+-- {: .proof}

###### Proof


The canonical morphism is the composite

$$
  (i_! \to i_*)
  :=
  i_!

   \stackrel{\eta i_!}{\to}
  \Im i_! := i_* i^* i_!
   \stackrel{\simeq}{\to}
  i_*
  \,.
$$

By the condition that $i_!$ is a [[full and faithful (∞,1)-functor]] the second morphism here in an [[equivalence in an (∞,1)-category|equivalence]], as indicated, and hence the component of the composite on $X$ being an effective epimorphism is equivalent to the component $i_! X \to \mathbf{\Pi} i_! X$ being an effective epimorphism.

=--



+-- {: .num_remark #RelationToRK}
###### Remark


In this form this characterization of formal smoothness is the evident generalization of the condition given in ([Kontsevich-Rosenberg, section 4.1](#KontsevichRosenbergSpaces)). See the section _<a href="http://nlab.mathforge.org/nlab/show/Q-category#FormalSmoothness">Formal smoothness</a>_ at _[[Q-category]]_ for more discussion. Notice that by <a href="http://nlab.mathforge.org/nlab/show/Q-category#DiscussionOfTheInfinitesimalThickeningFormalization">this remark</a> the notation there is related to the one used here by $u^* = i_!$, $u_* = i^*$ and $u^! = i_*$.

=--

Therefore we have the following more general definition.

+-- {: .num_defn #FormalRelativeSmoothnessByCanonicalMorphism}
###### Definition

For $f : X \to Y$ a morphism in $\mathbf{H}$, we say that

1. $f$ is a **[[formally smooth morphism]]** if the canonical morphism

   $$
     i_! X
      \to
     i_! Y \prod_{i_* Y} i_* Y
   $$

   is an [[effective epimorphism in an (∞,1)-category|effective epimorphism]].

1. $f$ is a **[[formally unramified morphism]]** if this is a [[(-1)-truncated]] morphism. More generally,  $f$ is an _order-$k$ formally unramified morphisms_ for $(-2) \leq k \leq \infty$ if this is a [[k-truncated]] morphism.

1. $f$ is a **[[formally étale morphism]]** if this morphism is an [[equivalence in an (∞,1)-category|equivalence]], hence if

   $$
     \array{
        i_! X &\stackrel{i_! f}{\to}& i_! Y
        \\
        \downarrow && \downarrow
        \\
        i_* X &\stackrel{i_* f}{\to}& i_* Y
     }
   $$

   is an [[(∞,1)-pullback]] square.


=--

+-- {: .num_remark #MeaningOfFormallyUnramified}
###### Remark

An order-(-2) formally unramified morphism is equivalently a [[formally étale morphism]].

Only for [[0-truncated]] $X$ does formal smoothness together with formal unramifiedness imply formal &#233;taleness.

=--

Even more generally we can formulate formal smoothness in $\mathbf{H}_{th}$:

+-- {: .num_defn #FormallyEtaleInHTh}
###### Definition

A morphism $f \colon X \to Y$ in $\mathbf{H}_{th}$ is **[[formally etale morphism|formally étale]]** if it is $\Im$-[[Pi-closed morphism|closed]], hence if its $\Im$-unit naturality square

$$
  \array{
    X &\to& \Im(X)
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{\Im(f)}}
    \\
    Y &\to& \Im(y)
  }
$$

is an [[(∞,1)-pullback]].

=--

+-- {: .num_remark}
###### Remark

A morphism $f$ in $\mathbf{H}$ is formally etale in the sense of def. \ref{FormalRelativeSmoothnessByCanonicalMorphism} precisely if its image $i_!(f)$ in $\mathbf{H}_{th}$ is formally etale in the sense of def. \ref{FormallyEtaleInHTh}.

=--

+-- {: .proof}
###### Proof

This is again given by the fact that $\Im = i_* i^*$ by definition and that $i_!$ is fully faithful, so that

$$
  \array{
    i_! X &\to& \Im(i_! X) \simeq i_* i^* i_! X &\stackrel{\simeq}{\to}& i_* X
    \\
    \downarrow^{\mathrlap{i_! f}} && \downarrow^{\mathrlap{i_* i^* i_! f}} && \downarrow^{\mathrlap{i_* f}}
    \\
    i_! Y &\to& \Im(i_! Y) \simeq i_* i^* i_! Y &\stackrel{\simeq}{\to}& i_* Y
  }
  \,.
$$

=--

+-- {: .num_prop #PropertiesOfFormallyEtaleMorphisms}
###### Proposition

The collection of [[formally étale morphisms]] in $\mathbf{H}$, def. \ref{FormalRelativeSmoothnessByCanonicalMorphism}, is closed under the following operations.

1. Every [[equivalence in an (∞,1)-category|equivalence]] is formally &#233;tale.

1. The composite of two formally &#233;tale morphisms is itself formally &#233;tale.

1. If


   $$
     \array{
       && Y
       \\
       & {}^{\mathllap{f}}\nearrow &\swArrow_{\simeq}& \searrow^{\mathrlap{g}}
       \\
       X &&\stackrel{h}{\to}&& Z
     }
   $$

   is a [[diagram]] such that $g$ and $h$ are formally &#233;tale, then also $f$ is formally &#233;tale.

1. Any [[retract]] of a formally &#233;tale morphisms is itself formally &#233;tale.

1. The [[(∞,1)-pullback]] of a formally &#233;tale morphisms is formally &#233;tale if the pullback is preserved by $i_!$.

=--

The statements about closure under composition and pullback appears as([KontsevichRosenberg, prop. 5.4, prop. 5.6](#KontsevichRosenbergSpaces)). Notice that the extra assumption that $i_!$ preserves the pullback is implicit in their setup, by remark \ref{RelationToRK}.

+-- {: .proof}
###### Proof

The first statement follows since $\infty$-pullbacks are well defined up to quivalence.

The second two statements follow by the [[pasting law]] for [[(∞,1)-pullback]]s: let $f : X \to Y$ and $g : Y \to Z$ be two
morphisms and consider the [[pasting diagram]]

$$
  \array{
    i_! X &\stackrel{i_! f }{\to}& i_! Y &\stackrel{i_! g}{\to}&  Z
    \\
    \downarrow && \downarrow && \downarrow
    \\
    i_* X &\stackrel{i_* f }{\to}& i_* Y &\stackrel{i_* g}{\to}& i_* Z
  }
  \,.
$$

If $f$ and $g$ are formally &#233;tale then both small squares are pullback squares. Then the pasting law says that so is the outer rectangle and hence $g \circ f$ is formally &#233;tale. Similarly, if $g$ and $g \circ f$ are formally &#233;tale then the right square and the total reactangle are pullbacks, so the pasting law says that also the left square is a pullback and so also $f$ is formally &#233;tale.

For the fourth claim, let $Id \simeq (g \to f \to g)$ be a [[retract]] in the [[arrow category|arrow (∞,1)-category]] $\mathbf{H}^I$. By applying the natural transformation $\phi : i_! \to I_*$ we obtain a retract

$$
  Id \simeq ((i_! g \to i_*g) \to  (i_! f \to i_*f) \to (i_! g \to i_*g))
$$

in the category of squares $\mathbf{H}^{\Box}$. We claim that generally, if the middle piece in a retract in $\mathbf{H}^\Box$ is an [[(∞,1)-pullback]] square, then so is its retract sqare. This implies the fourth claim.

To see this, we use that

1. [[(∞,1)-limit]]s are computed by [[homotopy limit]]s in any [[presentable (∞,1)-category]] $C$ presenting $\mathbf{H}$;

1. homotopy limits in $C$ may be computed by the left and right adjoints provided by the [[derivator]] $Ho(C)$ associated to $C$.

From this the claim follows as described in detail at _[[retract]]_ in the section _<a href="http://nlab.mathforge.org/nlab/show/retract#RetractsOfDiagrams">retracts of diagrams</a>_ .

For the last claim, consider an [[(∞,1)-pullback]] diagram

$$
  \array{
    A \times_Y X &\to& X
    \\
    {}^{\mathllap{p}}\downarrow && \downarrow^{\mathrlap{f}}
    \\
    A &\to& Y
  }
$$

where $f$ is formally &#233;tale.

Applying the [[natural transformation]] $\phi : i_! \to i_*$ to this yields a square of squares. Two sides of this are the [[pasting]] composite


$$
  \array{
    i_! A \times_Y X &\to& i_! X &\stackrel{\phi_X}{\to}&  i_* X
    \\
    \downarrow^{\mathrlap{i_! p}} && \downarrow^{\mathrlap{i_! f}}
                        && \downarrow^{\mathrlap{i_* f}}
    \\
    i_! A &\to& i_! Y &\stackrel{\phi_Y}{\to}& i_* Y
  }
$$

and the other two sides are the pasting composite

$$
  \array{
     i_! A \times_Y X &\stackrel{\phi_{A \times_Y X}}{\to}& i_* A \times_Y A
     &\stackrel{}{\to}& i_* X
     \\
     \downarrow^{\mathrlap{i_! p}} && \downarrow^{\mathrlap{i_* p}} && \downarrow^{\mathrlap{i_* f}}
     \\
     i_! A &\stackrel{\phi_A}{\to}& i_* A &\to& i_* Y
  }
  \,.
$$

Counting left to right and top to bottom, we have that

* the first square is a pullback by assumption that $i_!$ preserves the given pullback;

* the second square is a pullback, since $f$ is formally &#233;tale.

* the total top rectangle is therefore a pullback, by the [[pasting law]];

* the fourth square is a pullback since $i_*$ is [[right adjoint]] and so also preserves pullbacks;

* also the total bottom rectangle is a pullback, since it is equal to the top  total rectangle;

* therefore finally the third square is a pullback, by the other clause of the [[pasting law]]. Hence  $p$ is formally &#233;tale.

=--

+-- {: .num_remark #AsOpenMaps}
###### Remark

The properties listed in prop. \ref{PropertiesOfFormallyEtaleMorphisms} correspond to the axioms on the _[[open map]]s_ ("admissible maps") in a [[geometry (for structured (∞,1)-toposes)]]  ([Lurie, def. 1.2.1](#LurieStSp)). This means that a notion of formally &#233;tale morphisms induces a notion of [[locally algebra-ed topos|locally algebra-ed (∞,1)toposes]]/[[structured (∞,1)-toposes]] in a cohesive context. This is discuss in

* [[cohesive (∞,1)-topos -- structure ∞-sheaves]].

=--

In order to interpret the notion of formal smoothness, we turn now to the discussion of infinitesimal reduction.

+-- {: .num_prop #RedIsIdempotent}
###### Proposition

The operation $\Re$ is an [[idempotent]] projection of
$\mathbf{H}_{th}$ onto the image of $\mathbf{H}$

$$
  \Re \Re \simeq \Re
  \,.
$$

Accordingly also

$$
  \Im \Im \simeq \Im
$$


=--

+-- {: .proof}
###### Proof

By definition of infinitesimal neighbourhood we have that
$i_!$ is a [[full and faithful (∞,1)-functor]]. It follows that
$i^* i_! \simeq Id$ and hence

$$
  \begin{aligned}
    \Re \Re
    & \simeq
    i_! i^* i_! i^*
    \\
    & \simeq i_! i^*
    \\
    & \simeq \Re
  \end{aligned}
  \,.
$$

=--

+-- {: .num_cor #PiInfXIsFormallySmooth}
###### Observation

For every $X \in \mathbf{H}_{th}$, we have that $\Im(X)$ is formally smooth according to def. \ref{FormalSmoothness}.

=--

+-- {: .proof}
###### Proof

By prop. \ref{RedIsIdempotent} we have that

$$
  \Im(X) \to \Im \Im X

$$

is an [[equivalence in an (∞,1)-category|equivalence]]. As such it is in particular an [[effective epimorphism in an (∞,1)-category|effective epimorphism]].

=--

#### Infinitesimal $\mathbb{A}^1$-homotopy
 {#InfinitesimalA1Homotopy}

+-- {: .num_defn }
###### Definition

A set of objects $\{D_\alpha \in \mathbf{H}_{th}\}_\alpha$
is said to **exhibit the differential structure** or

**exhibit the infinitesimal thickening** if the
[[localization of an (∞,1)-category|localization]]

$$
  L_{\{D_\alpha\}_\alpha} \mathbf{H}_{th}

  \stackrel{\leftarrow}{\hookrightarrow}
  \mathbf{H}_{th}
$$

of $\mathbf{H}_{th}$
at the morphisms of the form $D_\alpha \times X \to X$
is exhibited by the [[infinitesimal shape modality]] $\Im$.

=--

+-- {: .num_Remark }
###### Remark

This is the [[infinitesimal cohesion|infinitesimal]]
analog of the notion of objects exhibiting [[cohesion]],
see at [structures in cohesion -- A1-homotopy and the continuum](#cohesive+%28infinity,1%29-topos+--+structures#A1HomotopyContinuum).



=--

For more see at _[[Lie differentiation]]_.

#### Structure sheaves
 {#StructureSheaves}
 {#CotangentBundles}

We discuss how in differential cohesion $\mathbf{H}_{th}$ every object $X$ canonically induces its [[étale (∞,1)-topos]] $Sh_{\mathbf{H}_{th}}(X)$.


For $X \in \mathbf{H}_{th}$ any object in a differential cohesive $\infty$-topos, we formulate

1. the [[(∞,1)-topos]] denoted $\mathcal{X}$ or $Sh_\infty(X)$ of [[(∞,1)-sheaves]] over $X$, or rather of formally &#233;tale maps into $X$;

1. the [[structure (∞,1)-sheaf]] $\mathcal{O}_{X}$ of $X$.

The resulting structure is essentially that discussed ([Lurie, Structured Spaces](#Lurie)) if we regard $\mathbf{H}_{th}$ equipped with its formally &#233;tale morphisms, def. \ref{FormallyEtaleInHTh}, as a ([[large category|large]]) [[geometry for structured (∞,1)-toposes]].

One way to motivate this is to consider structure sheaves of flat differential forms. To that end, let $G \in Grp(\mathbf{H}_{th})$ a differential cohesive [[∞-group]] with [de Rham coefficient object](cohesive+%28infinity,1%29-topos+--+structures#deRhamCohomology) $\flat_{dR}\mathbf{B}G$ and for $X \in \mathbf{H}_{th}$ any differential homotopy type, the product projection


$$
  X \times \flat_{dR} \mathbf{B}G \to X
$$

regarded as an object of the [[slice (∞,1)-topos]] $(\mathbf{H}_{th})_{/X}$ _almost_ qualifies as a "bundle of flat $\mathfrak{g}$-valued differential forms" over $X$: for $U \to X$ an cover (a [[1-epimorphism]]) regarded in $(\mathbf{H}_{th})_{/X}$, a $U$-plot of this product projection is a $U$-plot of $X$ together with a flat $\mathfrak{g}$-valued de Rham cocycle on $X$.

This is indeed what the sections of a corresponding bundle of differential forms over $X$ are supposed to look like -- but only _if_ $U \to X$ is sufficiently _spread out_ over $X$, hence sufficiently [[étale map|étale]]. Because, on the extreme, if $X$ is the point (the [[terminal object]]), then there should be no non-trivial section of differential forms relative to $U$ over $X$, but the above product projection instead reproduces all the sections of $\flat_{dR} \mathbf{B}G$.

In order to obtain the correct cotangent-like bundle from the product with the de Rham coefficient object, it needs to be _restricted_ to plots out of suficiently &#233;tale maps into $X$. In order to correctly test differential form data, "suitable" here should be "formally", namely infinitesimally. Hence the restriction should be along the full inclusion

$$
  (\mathbf{H}_{th})_{/X}^{fet} \hookrightarrow (\mathbf{H}_{th})_{/X}
$$

of the formally &#233;tale maps of def. \ref{FormallyEtaleInHTh} into $X$. Since on formally &#233;tale covers the sections should be those given by $\flat_{dR}\mathbf{B}G$, one finds that the corresponding "cotangent bundle" must be the [[coreflective subcategory|coreflection]] along this inclusion. The following proposition establishes that this coreflection indeed exists.



+-- {: .num_defn #EtaleSlice}
###### Definition

For $X \in \mathbf{H}_{th}$ any object, write

$$
  (\mathbf{H}_{th})^{fet}_{/X} \hookrightarrow (\mathbf{H}_{th})_{/X}
$$

for the full [[sub-(∞,1)-category]] of the [[slice (∞,1)-topos]] over $X$ on those maps into $X$ which are formally &#233;tale, def. \ref{FormallyEtaleInHTh}.

We also write $FEt_{\mathbf{X}}$ or $Sh_{\mathbf{H}}(X)$ for $(\mathbf{H}_{th})_{/X}^{fet}$.


=--

+-- {: .num_prop #EtalificationIsCoreflection}
###### Proposition

The inclusion $\iota$ of def. \ref{EtaleSlice} is both [[reflective sub-(∞,1)-category|reflective]] as well as [[coreflective subcategory|coreflective]], hence it fits into an [[adjoint triple]] of the form

$$
  (\mathbf{H}_{th})_{/X}^{fet}
  \stackrel{\overset{L}{\leftarrow}}{\stackrel{\overset{\iota}{\hookrightarrow}}{\underset{Et}{\leftarrow}}}
  (\mathbf{H}_{th})_{/X}
  \,.
$$

=--

+-- {: .proof}
###### Proof


By the general discussion at _[[reflective factorization system]]_, the reflection is given by sending a morphism $f \colon Y \to X$ to
$X \times_{\Im(X)} \Im(Y) \to Y$ and the reflection [[unit of an adjunction|unit]] is the left horizontal morphism in

$$
  \array{
    Y &\to& X \times_{\Im(Y)} \Im(Y) &\to& \Im(Y)
   \\
    & \searrow & \downarrow^{} && \downarrow^{\mathrlap{\Im(f)}}
   \\
   && X &\to& \Im(X)
  }
  \,.
$$

Therefore $(\mathbf{H}_{th})_{/X}^{fet}$, being a reflective subcategory of a [[locally presentable (∞,1)-category]], is (as discussed there) itself locally presentable. Hence by the [[adjoint (∞,1)-functor theorem]] it is now sufficient to show that the inclusion preserves all small [[(∞,1)-colimits]] in order to conclude that it also has a right [[adjoint (∞,1)-functor]].

So consider any [[diagram]] [[(∞,1)-functor]] $I \to (\mathbf{H}_{th})_{/X}^{fet}$ out of a [[small (∞,1)-category]]. Since the inclusion of $(\mathbf{H}_{th})_{/X}^{fet}$ is full, it is sufficient to show that the $(\infty,1)$-colimit over this diagram taken in $(\mathbf{H}_{th})_{/X}$ lands again in $(\mathbf{H}_{th})_{/X}^{fet}$ in order to have that $(\infty,1)$-colimits are preserved by the inclusion. Moreover, colimits in a slice of $\mathbf{H}_{th}$ are computed in $\mathbf{H}_{th}$ itself (this is discussed at _[slice category - Colimits](overcategory#LimitsAndColimits)_).

Therefore we are reduced to showing that the square

$$
  \array{
    \underset{\to_i}{\lim} Y_i &\to& \Im \underset{\to_i}{\lim} Y_i
    \\
    \downarrow && \downarrow
    \\
    X &\to& \Im(X)
  }
$$

is an [[(∞,1)-pullback]] square. But since $\Im$ is a [[left adjoint]] it commutes with the $(\infty,1)$-colimit on objects and hence this diagram is equivalent to

$$
  \array{
    \underset{\to_i}{\lim} Y_i &\to& \underset{\to_i}{\lim} \Im Y_i
    \\
    \downarrow && \downarrow
    \\
    X &\to& \Im(X)
  }
  \,.
$$

This diagram is now indeed an [[(∞,1)-pullback]] by the fact that we have [[universal colimits]] in the [[(∞,1)-topos]] $\mathbf{H}_{th}$, hence that on the left the component $Y_i$ for each $i \in I$ is the [[(∞,1)-pullback]] of $\Im(Y_i) \to \Im(X)$, by assumption that we are taking an $(\infty,1)$-colimit over formally &#233;tale morphisms.

=--

+-- {: .num_example #EtalificationOverThePoint}
###### Example

For the case that $X \simeq \ast$ in prop. \ref{EtalificationIsCoreflection}, then the proof there shows that the &#233;talification operation over the point is just ${\&} $:

$$
  {\&}  \simeq Et_{/\ast}
  \,.
$$

Indeed, for any $X$ then ${\&} X \to \ast$ is a [[formally étale morphism]] since

$$
  \array{
    {\&} X &\longrightarrow& \Im{\&}  X
     \\
     \downarrow && \downarrow
     \\
     \ast &\longrightarrow& \Im \ast
  }
  \;\;\;
  \simeq
  \;\;\;
  \array{
    {\&} X &\stackrel{\simeq}{\longrightarrow}& {\&}  X
     \\
     \downarrow && \downarrow
     \\
     \ast &\stackrel{\simeq}{\longrightarrow}& \ast
  }
$$

is a [[homotopy pullback]].

=--


+-- {: .num_prop }
###### Proposition

The $\infty$-category $(\mathbf{H}_{th})_{/X}^{fet}$ is an [[(∞,1)-topos]] and the canonical inclusion into $(\mathbf{H}_{th})_{/X}$ is a [[geometric embedding]].

=--

+-- {: .proof}
###### Proof

By prop. \ref{EtalificationIsCoreflection} the inclusion $(\mathbf{H}_{th})_{/X}^{fet} \hookrightarrow (\mathbf{H}_{th})_{/X}$ is [[reflective sub-(infinity,1)-category|reflective]] with reflector given by the $(\Im-equivalences , \Im-closed)$ factorization system. Since $\Im$ is a [[right adjoint]] and hence in particular preserves [[(∞,1)-pullbacks]], the $\Im$-equivalences are stable under pullbacks. By the discussion at _[[stable factorization system]]_ this is the case precisely if the corresponding reflector preserves [[finite (∞,1)-limits]]. Hence the embedding is a [[geometric embedding]] which exhibits a [[sub-(∞,1)-topos]] inclusion.

=--

+-- {: .num_defn #TheStructureSheafOfX}
###### Definition

For $X \in \mathbf{H}_{th}$ we speak of

$$
  \mathcal{X} \coloneqq Sh_{\mathbf{H}_{th}}(X)
  \coloneqq
  (\mathbf{H}_{th})_{/X}^{fet}
$$

also as the ([[petit (∞,1)-topos|petit]]) [[(∞,1)-topos]] of $X$
or the _[[étale (∞,1)-topos]]_ of $X$.

Write

$$
  \mathcal{O}_X
    \colon
  \mathbf{H}_{th}
    \stackrel{(-) \times X}{\to}
  (\mathbf{H}_{th})_{/X}
    \stackrel{Et}{\to}
  (\mathbf{H}_{th})_{/X}^{fet}
  =
  Sh_{\mathbf{H}_{th}}(X)
$$

for the composite [[(∞,1)-functor]] that sends any $A \in \mathbf{H}_{th}$ to the etalification, prop. \ref{EtalificationIsCoreflection}, of the projection $A \times X \to X$.

We call $\mathcal{O}_X$ the **[[structure sheaf]]** of $X$.

=--



+-- {: .num_remark }
###### Remark

For $X, A \in \mathbf{H}_{th}$ and for $U \to X$ a [[formally étale morphism]] in $\mathbf{H}_{th}$ (hence like an [[open subset]] of $X$), we have that

$$
  \begin{aligned}
    \mathcal{O}_{X}(A)(U)
    & \coloneqq
    Sh_{\mathbf{H}_{th}}(X)( U , \mathcal{O}_{X}(A) )
    \\
    & \coloneqq
    Sh_{\mathbf{H}_{th}}(X)( U , Et(X \times A) )
    \\
    & \simeq
    (\mathbf{H}_{th})_{/X}(U, X \times A)
    \\
    & \simeq
    \mathbf{H}_{th}(U,A)
    \\
    & \simeq
    A(U)
  \end{aligned}
  \,,
$$

where we used the [[adjoint (∞,1)-functor|∞-adjunction]] $(\iota \dashv Et)$ of prop. \ref{EtalificationIsCoreflection} and the [[(∞,1)-Yoneda lemma]].

This means that $\mathcal{O}_{X}(A)$ behaves as the _sheaf of $A$-valued functions over $X$_.


=--

+-- {: .num_prop #StructureSheafIsIndeedStructureSheaf}
###### Proposition

The functor $\mathcal{O}_X$ of def. \ref{StructureSheafRestrictedToH} is
indeed an $\mathbf{H}_{th}$-[[structure sheaf]] in the sense of [[structured (∞,1)-toposes]], for $\mathbf{H}_{th}$ regarded as a (large) [[geometry (for structured (∞,1)-toposes)]] with the [[formally étale morphisms]] being the "admissible morphisms".

=--

This is the analog of ([[Structured Spaces|Lurie, Structured Spaces, prop. 2.2.11]]).

+-- {: .proof}
###### Proof

We need to check that $\mathcal{O}_{X}$ preserves [[finite (∞,1)-limits]] and [[formally étale morphism|formally étale]] [[covers]] (where covers here in the [[canonical topology]] on the given toposes are [[1-epimorphisms]]). The first statement follows since $\mathcal{O}_{X}$ is [[right adjoint]] to the forgetful functor

$$
  Sh_{\mathbf{H}}(X)
    \simeq
  (\mathbf{H}_{th})_{/X}^{fet}
    \hookrightarrow
  (\mathbf{H}_{th})_{/X}
    \stackrel{\underset{X}{\sum}}{\to}
  \mathbf{H}_{th}
$$

For the second statement, let $p \colon \widehat Y \longrightarrow Y$ be any [[1-epimorphism]] which is also a [[formally étale morphism|formally étale]]. We need to show that also $Et(X \times p)$ is a [[1-epimorphism]].  By the discussion at [[effective epimorphism in an (∞,1)-category]] for this it is sufficient that the [[0-truncated|0-truncation]] $\tau_0 Et(X \times p)$ is an [[epimorphism]] in the underlying [[sheaf topos]], hence that every [[generalized element]] of $Et(X \times Y)$ has a lift to $Et(X \times \widehat{Y})$ after refinement along a cover.

By the fact that $Et$ is [[right adjoint]] to the inclusion, by construction, this means that it is sufficient to show that given a [[diagram]] in $\mathbf{H}_{th}$ of the form


$$
  \array{
    && && X \times \widehat{Y}
    \\
    && && \downarrow
    \\
    U && \longrightarrow && X \times Y
    \\
    & \searrow && \swarrow
    \\
    && X
  }
$$

with $U \to X$ formally &#233;tale, this can be completed to a diagram of the form

$$
  \array{
    \widehat{U} && \longrightarrow && X \times \widehat{Y}
    \\
    \downarrow && && \downarrow
    \\
    U && \longrightarrow && X \times Y
    \\
    & \searrow && \swarrow
    \\
    && X
  }
$$

with $\widehat{U} \to U$ a formally &#233;tale 1-epimorphism. But since both [[1-epimorphisms]] as well as [[formally étale morphisms]] are stable under [[(∞,1)-pullback]] we can take $\widehat U \coloneqq \widehat{Y} \times_Y U$.

=--

+-- {: .num_remark}
###### Remark

In the case that $\mathbf{H}_{th}$ happens to have an [[(∞,1)-site]] of definition whose [[covers]] are ([[Grothendieck pretopology|generated]]) from [[formally étale morphisms]] (a small [[geometry (for structured (∞,1)-toposes)]]), then $\mathbf{H}_{th}$ is the [[classifying topos|classifying (∞,1)-topos]] for [[structure sheaves]] and $\mathcal{O}_X$ in prop. \ref{StructureSheafIsIndeedStructureSheaf} may be regarded as the [[inverse image]] of the classifying [[geometric morphism]]

$$
  Sh_{\mathbf{H}_{th}}(X)
  \stackrel{\overset{\mathcal{O}_X}{\leftarrow}}{\underset{}{\longrightarrow}}
  \mathbf{H}_{th}
  \,.
$$

=--
+-- {: .num_example #CotangentBundle}
###### Example

Let $G \in Grp(\mathbf{H}_{th})$ be an [[∞-group]] and write $\flat_{dR} \mathbf{B}G \in \mathbf{H}_{th}$ for the corresponding de Rham coefficient object.
Then

$$
  \mathcal{O}_X(\flat_{dR}\mathbf{B}G)
  \in
  Sh_{\mathbf{H}}(X)
$$

we may call the **$G$-valued flat cotangent sheaf** of $X$.

=--

+-- {: .num_remark }
###### Remark

For $U \in \mathbf{H}_{th}$ a test object (say an object in a [[(∞,1)-site]] of definition, under the [[Yoneda embedding]]) a formally &#233;tale morphism $U \to X$ is like an [[open map]]/open embedding. Regarded as an object in $(\mathbf{H}_{th})_{/X}^{fet}$ we may consider the sections over $U$ of the cotangent bundle as defined above, which in $\mathbf{H}_{th}$ are diagrams

$$
  \array{
    U &&\to&& \mathcal{O}_X(\flat_{dR}\mathbf{B}G)
    \\
    & \searrow && \swarrow
    \\
    && X
  }
  \,.
$$

By the fact that $Et(-)$ is [[right adjoint]], such diagrams are in bijection to diagrams

$$
  \array{
    U &&\to&& X \times \flat_{dR} \mathbf{B}G
    \\
    & \searrow && \swarrow
    \\
    && X
  }
$$

where we are now simply including on the left the formally &#233;tale map $(U \to X)$ along $(\mathbf{H}_{th})^{fet}_{/X} \hookrightarrow (\mathbf{H}_{th})_{/X}$.

In other words, the sections of the $G$-valued flat cotangent sheaf $\mathcal{O}_X(\flat_{dR}\mathbf{B}G)$ are just the sections of $X \times \flat_{dR}\mathbf{B}G \to X$ itself, only that the _domain_ of the section is constrained to be a formally &#233;tale patch of $X$.

But then by the very nature of $\flat_{dR}\mathbf{B}G$ it follows that the flat sections of the $G$-valued cotangent bundle of $X$ are indeed nothing but the flat $G$-valued differential forms on $X$.

=--

+-- {: .num_prop #StructuredPetitToposesAreLocallyContractible}
###### Proposition

For $X \in \mathbf{H}_{th}$ an object in a differentially cohesive
$\infty$-topos, then its petit structured $\infty$-topos
$Sh_{\mathbf{H}_{th}}(X)$, according to def. \ref{TheStructureSheafOfX},
is [[locally ∞-connected (∞,1)-topos|locally ∞-connected]].

=--

+-- {: .proof}
###### Proof

We need to check that the composite

$$
  \infty Grpd \stackrel{Disc}{\longrightarrow} \mathbf{H}_{th}
   \stackrel{(-) \times X}{\longrightarrow}
   (\mathbf{H}_{th})_{/X}
  \stackrel{L}{\longrightarrow}
  Sh_{\mathbf{H}}(X)
$$

preserves [[(∞,1)-limits]], so that it has a further
[[left adjoint]]. Here $L$ is the
reflector from prop. \ref{EtalificationIsCoreflection}.
Inspection shows that this composite sends an object $A \in \infty Grpd$ to
$\Im(Disc(A)) \times X \to X$:

$$

  \array{
    \Im(Disc(A)) \times X
     &\longrightarrow&
    \Im(Disc(A) \times X) & \simeq \Im(Disc(A)) \times \Im(X)
    \\
    \downarrow &{}^{(pb)}& \downarrow
    \\
    X &\longrightarrow& \Im(X)
  }
  \,.
$$


By the discussion at [slice (∞,1)-category -- Limits and colimits](slice+infinity-category#LimitsAndColimits) an [[(∞,1)-limit]] in the slice $(\mathbf{H}_{th})_{/X}$ is computed as an [[(∞,1)-limit]] in $\mathbf{H}$ of the [[diagram]] with the slice [[cocone]] adjoined. By [[right adjoint|right adjointness]] of the inclusion $Sh_{\mathbf{H}}(X) \hookrightarrow (\mathbf{H}_{th})_{/X}$ the same is then true for $Sh_{\mathbf{H}}(X) \coloneqq (\mathbf{H}_{th})_{/X}^{et}$.

Now for $A \colon J \to \infty Grpd$ a [[diagram]], it is taken to the diagram $j \mapsto \Im(Disc(A_j)) \times X \to X$ in $Sh_{\mathbf{H}}(X)$ and so its $\infty$-limit is computed in $\mathbf{H}$ over the diagram locally of the form

$$
  \array{
     X \times \Im(Disc(A_{j}))
     &&\longrightarrow&&
     X \times \Im(Disc(A_{j'}))
     \\
     & \searrow && \swarrow
     \\
     && X
  }
  \simeq
  \array{
     X \times \Im(Disc(A_{j}))
     &&\longrightarrow&&
     X \times \Im(Disc(A_{j'}))
     \\
     & \searrow && \swarrow
     \\
     && X \times \ast
  }
  \,.
$$

Since $\infty$-limits commute with each other this limit is the product of

1.  $\underset{\leftarrow}{\lim}_j \Im(Disc(A_j))$

1. $\underset{\leftarrow}{\lim}_{J \star \Delta^0} X$ (over the co-coned diagram constant on $X$).

For the first of these, since the [[infinitesimal shape modality]] $\Im$
is in particular a [[right adjoint]] (with [[left adjoint]] the
[[reduction modality]]), and since $Disc$ is also [[right adjoint]] by [[cohesion]], we have a [[natural equivalence]]

$$
  \underset{\leftarrow}{\lim}_j \Im(Disc(A_j))
  \simeq
   \Im(Disc(\underset{\leftarrow}{\lim}_j(A_j)))
  \,.
$$

For the second, the $\infty$-limit over an $\infty$-category $J \star \Delta^0$ of a functor constant on $X$ is

$$
  \begin{aligned}
     \underset{\leftarrow}{\lim}_{J \star \Delta^0} X
     & \simeq
     \underset{\leftarrow}{\lim}_{J \star \Delta^0} [\ast, X]
     \\
     & \simeq
     [\underset{\rightarrow}{\lim}_{J \star \Delta^0} \ast, X]
     \\
     & \simeq
     [{\vert {J \star \Delta^0}\vert}, X]
     \\
     & \simeq
     [\ast, X] \simeq X
  \end{aligned}
  \,,
$$

where the last line follows since ${J \star \Delta^0}$
has a terminal object and hence contractible geometric realization.

In conclusion this shows that $\infty$-limits are preserved by $L \circ (-)\times X\circ Disc$.

=--

+-- {: .num_prop #FormallyEtaleMorphismInducesEtaleMorphismOfStructuredToposes}
###### Proposition

Let $f \;\colon\; Y \longrightarrow X$ be a [[formally étale morphism]] in a differentially cohesive $\infty$-topos $\mathbf{H}$. Then pullback $f^\ast$ is the [[inverse image]] of an [[étale morphism]] of [[structured (∞,1)-toposes]] between the corresponding [[étale toposes]], def. \ref{TheStructureSheafOfX}, hence
there is an [[étale geometric morphism]]

$$
  Sh_{\mathbf{H}}(Y)
  \simeq
  Sh_{\mathbf{H}}(X)/_{f}
   \stackrel{\overset{f_!}{\longrightarrow}}{\stackrel{\overset{f^\ast}{\leftarrow}}{\underset{f_\ast}{\longrightarrow}}}
  Sh_{\mathbf{H}}(X)
$$

and an equivalence of [[structure sheaves]]

$$
  \mathcal{O}_Y \simeq f^\ast \mathcal{O}_X
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since the inclusion of the point into the interval is an op-[[final (∞,1)-functor]] we have (by [this proposition](over-%28infinity%2C1%29-category#FinalFunctorsInduceEquivalentSlices)) an [[equivalence]] of [[over-(∞,1)-categories]]

$$

  \mathbf{H}/_{Y} \simeq \mathbf{H}/_{f} \simeq (\mathbf{H}/_{X})/_f
  \,.
$$

Since $f$ is formally &#233;tale by assumption and since [[formally étale morphisms]] are closed under [[composition]], this restricts to an [[equivalence]]
$Sh_{\mathbf{H}}(Y) \simeq (Sh_{\mathbf{H}}(X))/_f$.

For the equivalence of structure sheaves it is sufficient to show for each
[[coefficient]] $A \in \mathbf{H}_{th}$  an equivalence

$$
  \mathcal{O}_Y(A) \simeq (f^\ast \mathcal{O}_X(A))
$$

in $Sh_{\mathbf{H}}(Y)$. But by definition (\ref{TheStructureSheafOfX}) $\mathcal{O}_Y(A) \coloneqq Et(A \times Y)$ and similarly for $\mathcal{O}_X$ and since $Et$ is [[right adjoint]] to the inclusion $Sh_{\mathbf{H}}(Y) \hookrightarrow \mathbf{H}_{Y}$ we have

$$
  f^\ast \mathcal{O}_X(A)
  =
  f^\ast Et(A \times X)
  \simeq
  Et(f^\ast(A \times X))
  \simeq
  Et(A \times Y)
  =
  \mathcal{O}_Y(A)
  \,.
$$



=--



#### Sheaves of (quasi-coherent) modules
 {#SheavesOfModules}

We discuss the abstract formulation of sheaves of [[modules]] and of [[quasicoherent sheaves]] on petit $\infty$-toposes in differential cohesion.

> under construction -- check

+-- {: .num_defn}
###### Definition

For $X \in \mathbf{H}_{th}$ an object and $(Sh_{\mathbf{H}}(X), \mathcal{O}_X)$ its $\mathbf{H}_{th}$-[[structured (infinity,1)-topos]], according to def. \ref{TheStructureSheafOfX}, consider the composite functor

$$
  \mathcal{O}_X^{\mathbf{H}} \;\colon\; \mathbf{H} \stackrel{i_!}{\hookrightarrow} \mathbf{H}_{th} \stackrel{Et X^\ast}{\longrightarrow} Sh_{\mathbf{H}}(X)
  \,,
$$

then an **$\mathcal{O}_X$-module** $\mathcal{F}$ on $X$ is an extension of $\mathcal{O}_X^{\mathbf{H}}$ by a limit-preserving functor through $i_!$

$$
  \array{
    \mathbf{H} &\stackrel{\mathcal{O}_X^{\mathbf{H}}}{\longrightarrow}& Sh_{\mathbf{H}}(X)
    \\
     {}^{\mathllap{i_!}}\downarrow & \nearrow_{\mathrlap{\mathcal{F}}}
    \\
    \mathbf{H}_{th}
  }
  \,.
$$

=--

+-- {: .num_example}
###### Example

In particular $\mathcal{O}_X$ is canonically a module over itself by setting $\mathcal{F} = \mathcal{O}_X$.

=--


This is a slight abstraction of the definition in ([Lurie QC,  section 2.3](quasicoherent+sheaf#LurieQC)). See at _[quasicoherent sheaf -- In higher geometry -- As extension of the structure sheaf](quasicoherent+sheaf#HigherGeometryAsExtensionsOfStructureSheaf)_.


#### Liouville-Poincar&#233; cocycle
 {#PoincareCocycle}

+-- {: .num_defn #TheLiouvillePoincareCocycle}
###### Definition

For $X,A \in \mathbf{H}_{th}$ and with $\mathcal{O}_X(A) \in Sh_{\mathbf{H}}(X)$ as in def. \ref{TheStructureSheafOfX}, write

$$
  \theta_X(A)
  \;\colon\;
  \underset{X}{\sum}
  \iota \mathcal{O}_X(A)
  \to
  A
$$

for the [[morphism]] in $\mathbf{H}$ which is the $(\underset{X}{\sum} \dashv X^*)$-adjunct $\underset{X}{\sum}\iota Et(X^* A) \to A$ of the [[counit of a comonad|counit]] $\iota Et(X^* A) \to X^* A$ of the $(\iota \dashv Et)$-coreflection of def. \ref{TheStructureSheafOfX}.

This $\theta_X(A)$ we call the **Liouville-Poincar&#233; $A$-cocycle** on $\underset{X}{\sum} \iota \mathcal{O}_X(A)$.

=--

+-- {: .num_example }
###### Example

Consider the model of differential cohesion given by $\mathbf{H}_{th} =$ [[SynthDiff∞Grpd]]. Write $\Omega^1 \in \mathbf{H }\stackrel{i_!}{\hookrightarrow} \mathbf{H}_{th}$ for the abstract [[sheaf]] of [[differential 1-forms]].

Then for $X \in SmthMfd \hookrightarrow \mathbf{H}$ a [[smooth manifold]], we have that

$$

  \underset{X}{\sum} \iota \mathcal{O}_X(\Omega^1) \to X
$$

is the [[cotangent bundle]]

$$
  T^* X \to X
$$

of the manifold: because for $i_U \colon U \to X$ an open subset of the manifold regarded as an object of $Sh_{\mathbf{H}}(X)$, a section $\iota(\sigma_U)$ of $T^* X|_U \to U$ is equivalently a map $\sigma \colon i_U \to \mathcal{O}_X(\Omega^1)$ in $Sh_{\mathbf{H}_{th}}(X)$, which by the $(\iota \dashv Et)$-[[adjunction]] is a map $\iota(i_U) \to X \times \Omega^1$ in $(\mathbf{H}_{th})_{/X}$ which finally is equivalently a map $U \to \Omega^1$ in $\mathbf{H}_{th}$ hence an element in $\Omega^1(U)$.


So the Liouville-Poincar&#233; $\Omega^1$-cocycle according to \ref{TheLiouvillePoincareCocycle} is a [[differential 1-form]]

$$
  \theta
  \;\colon\;
  \underset{X}{\sum}\iota \mathcal{O}_X(\Omega^1)
  \to
  \Omega^1
$$

on the total space of the cotangent bundle. For

$$
  \sigma \;\colon\; X \to \mathcal{O}_X(\Omega^1)
  \;\;\;
  \in Sh_{\mathbf{H}}(X)
$$

a [[section]] of the [[cotangent bundle]], the [[pullback of a differential form|pullback form]] $\sigma^* \theta$ on $X$ is the composite

$$
  \underset{X}{\sum}\iota X \stackrel{\underset{X}{\sum}\iota(\sigma)}{\to} \underset{X}{\sum}\iota \mathcal{O}_X(\Omega^1) \stackrel{\theta}{\to} \Omega^1
 \,,
$$

hence the [[adjunct]]

$$
  \iota X \stackrel{\iota(\sigma)}{\to} \iota \mathcal{O}_X(\Omega^1) \stackrel{}{\to} X^* \Omega^1
  \,,
$$

hence by definition

$$
  \iota(X) \stackrel{\iota(\sigma)}{\to} \iota(Et(X \times \Omega^1)) \stackrel{}{\to} X^*\Omega^1
  \,,
$$

hence the adjunct

$$
  X \stackrel{\sigma}{\to} Et(X \times \Omega^1) \stackrel{id}{\to} Et(X \times \Omega^1)
$$

hence the original $\sigma$. This is the defining property which identifies $\that$ as the traditional [[Liouville-Poincaré 1-form]].


=--


#### Manifolds and &#233;tale groupoids
 {#EtaleObjects}
 {#CohesivemanifoldsSeparated}

An ordinary [[topological groupoid|topological]]/[[Lie groupoid|Lie]] [[étale groupoid]] is one whose source/target map is an
[[étale map]]. We consider now a notion that can be formulated in the presence of infinitesimal cohesion which generalizes this.

+-- {: .num_defn #FormalEtaleGroupoid}
###### Definition

A [[groupoid object in an (∞,1)-category|groupoid object]] $\mathcal{G}_\bullet$ is an  **[[étale ∞-groupoid]]** if the equivalent (via the higher [[Giraud theorem]]) [[effective epimorphism]] (the [[atlas]]) $\mathcal{G}_0 \longrightarrow \mathcal{G}$ is a [[formally étale morphism]].

=--

Let now $V$ be any object


(For instance let $\mathbb{A}^1 \in \mathbf{H}$ be a canonical line object that exhibits the cohesion of $\mathbf{H}$ in the sense of _[structures in a differential infinity-topos -- A1 homotopy / The continuum](cohesive+%28infinity%2C1%29-topos+--+structures#A1HomotopyContinuum)_ and take $V = \coprod_n \mathbb{A}^n$.)

+-- {: .num_defn #Manifold}
###### Definition

A **$V$-manifold** is an object $X$ such that there exists a **$V$-cover** $U$, namely a  [[correspondence]] from $V$ to $X$

$$
  \array{
     && U
     \\
     & \swarrow && \searrow
     \\
     V && && X
  }
$$

such that both morphisms are [[formally étale morphisms]] and such that $U \to X$ is in addition an [[effective epimorphism]].

=--

See also at _[smooth manifold -- general abstract geometric formulation](smooth%20manifold#GeneralAbstractCharacterization)_

#### Frame bundles
 {#GLnTangentBundles}

We discuss how each manifold $X$ in differential cohesion as in def. \ref{Manifold} is associated a canonical [[frame bundle]] classified by a morphism $X \to \mathbf{B}GL(V)$.


+-- {: .num_defn #FormalDiskBundle}
###### Definition


For $X$ any object in differential cohesion, its _[[infinitesimal disk bundle]]_ $T_{inf} X \to X$ is the [[homotopy pullback]]

$$
  \array{
    T_{inf} X &\stackrel{ev}{\longrightarrow}& X
    \\
    \downarrow^{\mathrlap{p}} && \downarrow
    \\
    X &\longrightarrow& \Im X
  }
$$

of the [[unit of a monad|unit]] of its [[infinitesimal shape modality]] along itself.

More generally, given a filtration of differential cohesion by orders of infinitesimals, remark \ref{SequenceOfOrdersOfInfinitesimals}, then the order-$k$ [[infinitesimal disk bundle]] is the [[homotopy pullback]] in

$$
  \array{
    T_{inf} X &\stackrel{ev}{\longrightarrow}& \Im_{(k)}X
    \\
    \downarrow^{\mathrlap{p}} && \downarrow
    \\
    X &\longrightarrow& \Im X
  }
  \,.
$$


=--

+-- {: .num_remark}
###### Remark

The [[Atiyah groupoid]] of $T_{inf} X$ is the [[jet groupoid]] of $X$

=--

+-- {: .num_remark #RelationOfInfinitesimalDiskBundleToJetBundle}
###### Remark

With respect to the [[base change]] [[geometric morphism]]

$$
  \mathbf{H}_{/X}
    \stackrel{\overset{p_!}{\longrightarrow}}{\stackrel{\overset{p^\ast}{\longleftarrow}}{\underset{p_\ast}{\longrightarrow}}}
  \mathbf{H}_{/\Im X}
$$

then then [[infinitesimal disk bundle]] of $X$ is

$$
  T_{inf} X \simeq p^\ast p_! X
  \,,
$$

where on the right $X$ is regarded as sitting by the identity morphism over itself.

Written in this form it follows from the [[adjoint triple]] above that bundle morphisms 

$$
  \array{
    T_{inf}X && \longrightarrow && E
    \\
    & \searrow && \swarrow
    \\
    && X
  }
$$

are equivalently [[sections]] of $p^\ast p_\ast E$. But such bundle morphisms are equivalently [[jets]] of $E$ and hence $p^\ast p_\ast E$ is the [[jet bundle]] of $E$. See there for more.

=--

+-- {: .num_lemma #EtalePullbackOfFormalDiskBundleIsFormalDiskBundle}
###### Lemma

If $\iota \colon U \to X$ is a [[formally étale morphism]], def. \ref{FormallyEtaleInHTh}, then

$$
  \iota^\ast T_{inf} X \simeq T_{inf}U
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the definition of formal &#233;taleness and using the [[pasting law]] we have an equivalence of [[pasting diagrams]] of [[homotopy pullbacks]] of the following form:

$$
  \array{
     \iota^\ast T_{inf} X &\longrightarrow& T_{inf} X &\longrightarrow& X
     \\
     \downarrow && \downarrow && \downarrow
     \\
     U &\longrightarrow& X &\longrightarrow& \Im X
  }
  \;\;\;\;
  \simeq
  \;\;\;\;
  \array{
      T_{inf} U &\longrightarrow& U &\longrightarrow& X
       \\
       \downarrow && \downarrow && \downarrow
       \\
       U &\longrightarrow& \Im U &\longrightarrow& \Im X
  }
$$


=--

+-- {: .num_defn #Framing}
###### Definition

For $V$ an object, a **[[framing]]** on $V$ is a trivialization of its infinitesimal disk bundle, def. \ref{FormalDiskBundle}, i.e. an object $\mathbb{D}^V$ -- the typical [[infinitesimal disk]] or [[formal disk]] -- and a (chosen) [[equivalence]]

$$
  \array{
    T_{inf} V && \stackrel{\simeq}{\longrightarrow} && V \times \mathbb{D}^n
    \\
    & \searrow && \swarrow_{\mathrlap{p_1}}
    \\
    && V
  }
  \,.
$$



=--

+-- {: .num_defn #GeneralLinearGroup}
###### Definition

For $V$ a framed object, def. \ref{Framing}, we write

$$
  GL(V) \coloneqq \mathbf{Aut}(\mathbb{D}^V)
$$

for the [[automorphism ∞-group]] of its typical [[infinitesimal disk]]/[[formal disk]].

=--

+-- {: .num_remark #OrderOfInfinitesimalDisks}
###### Remark

When the [[infinitesimal shape modality]] exhibits first-order infinitesimals, such that $\mathbb{D}(V)$ is the first order [[infinitesimal neighbourhood]] of a point, then $\mathbf{Aut}(\mathbb{D}(V))$ indeed plays the role of the [[general linear group]]. When $\mathbb{D}^n$ is instead a higher order or even the whole [[formal neighbourhood]], then $GL(n)$ is rather a [[jet group]]. For order $k$-jets this is sometimes written $GL^k(V)$ We nevertheless stick with the notation "$GL(V)$" here, consistent with the fact that we have no index on the [[infinitesimal shape modality]]. More generally one may wish to keep track of a whole tower of infinitesimal shape modalities and their induced towers of concepts discussed here.

=--


This class of examples of framings is important:

+-- {: .num_prop #DifferentialCohesiveInfinityGroupIsCanonicallyFramed}
###### Proposition

Every differentially cohesive [[∞-group]] $G$ is canonically framed (def. \ref{Framing}) such that the horizontal map in def. \ref{FormalDiskBundle} is given by the left action of $G$ on its [[infinitesimal disk]] at the neutral element:

$$
  ev \colon T_{inf}G \simeq G \times \mathbb{D}^G_e \stackrel{\cdot}{\longrightarrow} G
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the discussion at _[[Mayer-Vietoris sequence]]_ in the section _[Over an ∞-group](Mayer-Vietoris%20sequence#OverAGroupObject)_ and using that the [[infinitesimal shape modality]] preserves group structure, the defining [[homotopy pullback]] of $T_{inf} G$ is equivalent to the pasting of pullback diagrams of the form

$$
  \array{
    T_{inf} G &\stackrel{}{\longrightarrow}&
    \mathbb{D}^G_e
    &\stackrel{}{\longrightarrow}& \ast
    \\
    \downarrow &&  \downarrow && \downarrow
    \\
    G \times G &\stackrel{(-)\cdot (-)^{-1}}{\longrightarrow}& G
    &\stackrel{}{\longrightarrow}&
    \Im G
  }
  \,,
$$

where the right square is the defining pullback for the [[infinitesimal disk]] $\mathbb{D}^G$. For the left square we find by [this proposition](Mayer-Vietoris%20sequence#HTTArgumentForPullback) that $T_{inf} G \simeq G\times \mathbb{D}^G$ and that the top horizontal morphism is as claimed.

=--




By lemma \ref{EtalePullbackOfFormalDiskBundleIsFormalDiskBundle} it follows that:

+-- {: .num_prop #FormalDiskBundleOfRegularManifoldsTrivializesOverCover}
###### Proposition

For $V$ a framed object, def. \ref{Framing}, let $X$ be a $V$-manifold, def. \ref{Manifold}. Then the infinitesimal disk bundle, def. \ref{FormalDiskBundle}, of $X$ canonically trivializes over any $V$-cover $V \leftarrow U \rightarrow X$ , i.e. there is a [[homotopy pullback]] of the form

$$
  \array{
     U \times \mathbb{D}^V &\longrightarrow& T_{inf} X
     \\
     \downarrow && \downarrow
     \\
     U &\longrightarrow& X
  }
  \,.
$$

This exhibits $T_{inf} X\to X$ as a $\mathbb{D}^V$-[[fiber ∞-bundle]].

=--

+-- {: .num_prop #ModulatingMapOfFormalDiskBundle}
###### Remark

By [this discussion](fiber+infinity-bundle#Properties) this fiber [[fiber ∞-bundle]] is the [[associated ∞-bundle]] of an essentially uniquely determined $\mathbf{Aut}(\mathbb{D}^V)$-[[principal ∞-bundle]].

=--

+-- {: .num_defn #FrameBundleMap}
###### Definition

Given a $V$-manifold $X$, def. \ref{Manifold}, for framed $V$, def. \ref{Framing}, then its _[[frame bundle]]_ $Fr(X)$ is the $GL(V)$-[[principal ∞-bundle]] given by prop. \ref{FormalDiskBundleOfRegularManifoldsTrivializesOverCover} via remark \ref{ModulatingMapOfFormalDiskBundle}.

=--

+-- {: .num_remark }
###### Remark

As in remark \ref{OrderOfInfinitesimalDisks}, this really axiomatizes in general [[higher order frame bundles]] with the order implicit in the nature of the [[infinitesimal shape modality]].

=--

+-- {: .num_remark #FrameBundlesFunctorial}
###### Remark

By prop. \ref{EtalePullbackOfFormalDiskBundleIsFormalDiskBundle} the construction of frame bundles in def. \ref{FrameBundleMap} is functorial in [[formally étale maps]] between $V$-manifolds.

=--

#### $G$-Structures
 {#structures}

We discuss the formalization of [[G-structures]] and [[integrability of G-structures]] in differential cohesion

Let $V$ be framed, def. \ref{Framing}, let $G$ be an [[∞-group]] and $G \to GL(V)$ a homomorphism to the general linear group of $V$, def. \ref{GeneralLinearGroup}, hence

$$
  G\mathbf{Struc}\colon \mathbf{B}G \longrightarrow \mathbf{B}GL(V)
$$

a morphism between the [[deloopings]].

+-- {: .num_defn #GStructure}
###### Definition

For $X$ a $V$-manifold, def. \ref{Manifold}, a **[[G-structure]]** on $X$ is a lift of the structure group of its [[frame bundle]], def. \ref{FrameBundleMap}, to $G$, hence a diagram

$$
  \array{
     X && \longrightarrow&&  \mathbf{B}G
     \\
     & {}_{\mathllap{\tau_X}}\searrow && \swarrow_{\mathrlap{G\mathbf{Struc}}}
     \\
     && \mathbf{B}GL(V)
  }
$$

hence a morphism

$$
  \mathbf{c} \colon \tau_X \longrightarrow G\mathbf{Struc}
$$

in the [[slice (∞,1)-topos]].

=--

In fact $G\mathbf{Struc}\in \mathbf{H}_{/\mathbf{B}GL(n)}$ is the [[moduli ∞-stack]] of such $G$-structures.

The double [[slice (∞,1)-topos|slice]] $(\mathbf{H}_{/\mathbf{B}GL(n)})_{/G\mathbf{Struc}}$ is the [[(∞,1)-category]] of such $G$-structures.

+-- {: .num_example #TrivialGStructure}
###### Example


If $V$ is framed, def. \ref{Framing}, then it carries the trivial $G$-structure, which we denote by

$$
  \mathbf{c}_0 \colon \tau_{V} \longrightarrow G\mathbf{Struc}
  \,.
$$

=--

+-- {: .num_defn #IntegrableGStructure}
###### Definition

For $V$ framed, def. \ref{Framing}, and $X$ a $V$-manifold, def. \ref{Manifold}, then  a $G$-structure $\mathbf{c}$ on $X$, def. \ref{GStructure}, is _[[integrability of G-structures|integrable]]_ (or _locally flat_) if there exists a $V$-cover

$$
  \array{
     && U
     \\
     & \swarrow && \searrow
     \\
     V && && X
  }
$$

such that the [[correspondence]] of [[frame bundles]] induced via remark \ref{FrameBundlesFunctorial}

$$
  \array{
     && \tau_U
     \\
     & \swarrow && \searrow
     \\
     \tau_V && && \tau_X
  }
$$

(a diagram in $\mathbf{H}_{/\mathbf{B}GL(V)}$) extends to a sliced correspondence between $\mathbf{c}$ and the trivial $G$-structure $\mathbf{c}_0$ on $V$, example \ref{TrivialGStructure}, hence to a diagram in $\mathbf{H}_{/\mathbf{B}GL(V)}$ of the form

$$
  \array{
     && \tau_U
     \\
     & \swarrow && \searrow
     \\
     \tau_V && \swArrow_{\mathrlap{\simeq}}  && \tau_X
     \\
     & {}_{\mathllap{\mathbf{c}_0}}\searrow && \swarrow_{\mathrlap{\mathbf{c}}}
     \\
     && G\mathbf{Struct}
  }
$$

On the other hand, $\mathbf{c}$ is called _infinitesimally integrable_ (or _torsion-free_) if such an extension exists (only) after restriction to all [[infinitesimal disks]] in $X$ and $U$, hence after composition with the [[counit of a comonad|counit]]

$$
  \flat^{rel} U \longrightarrow U
$$

of the [[relative flat modality]], def. \ref{InducedRelativeShapeAndFlat} (using that by prop. \ref{CounitOfFlatRelIsFormallyEtale} this is also formally &#233;tale and hence induces map of frame bundles):

$$
  \array{
     && \tau_{\flat^{rel} U}
     \\
     & \swarrow && \searrow
     \\
     \tau_V && \swArrow_{\mathrlap{\simeq}}  && \tau_X
     \\
     & {}_{\mathllap{\mathbf{c}_0}}\searrow && \swarrow_{\mathrlap{\mathbf{c}}}
     \\
     && G\mathbf{Struct}
  }
 \,.
$$


=--

+-- {: .num_remark}
###### Remark

As before, if the given [[reduction modality]] encodes order-$k$ infinitesimals, then the infinitesimal integrability in def. \ref{IntegrableGStructure} is order-$k$ integrability. For $k = 1$ this is [[torsion of a G-structure|torsion-freeness]].

=--



#### Flat $\infty$-connections and infinitesimal local systems
  {#StrucInfinitesimalLocalSystem}


We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#FlatDifferentialCohomology">intrinsic flat cohomology</a> in an infinitesimal neighbourhood.


+-- {: .num_defn #InfinitesimalFlatCohomology}
###### Definition

For $X, A \in \mathbf{H}_{th}$ we say that

$$
  H_{infflat}(X,A) := \pi_0 \mathbf{H}(\Im(X), A)
   \simeq
   \pi_0 \mathbf{H}(X, \mathbf{\flat}_{inf}A)
$$

(where $(\Im \dashv \mathbf{\flat}_{inf})$ is given by def. \ref{InfinitesimalPathsAndReduction}) is the **infinitesimal flat cohomology** of $X$ with coefficient in $A$.

=--


+-- {: .num_note #CrystallineCohomology}
###### Note

In traditional contexts this is also called _[[crystalline cohomology]]_ or just _[[de Rham cohomology]]_ . Since we already have an <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#deRhamCohomology">intrinsic notion of de Rham cohomology</a> in any [[cohesive (∞,1)-topos]], which is similar to but may slightly differ from infinitesimal flat differential cohomology, we shall say **[[synthetic differential geometry|synthetic]] de Rham cohomology** for the notion of def. \ref{InfinitesimalFlatCohomology} if we wish to honor traditional terminology. In this case we shall write

$$
  H_{dR,synth}(X,A)
   :=
  \pi_0 \mathbf{H}_{th}(\Im(X), A)
  \,.

$$

=--

+-- {: .num_note #FiniteAndInfinitesimalFlatConnections}
###### Note


By the [above observation](#InclusionOfConstantIntoInfinitesimalIntoAllPaths)
we have canonical morphisms

$$
  \mathbf{H}_{flat}(X,A)
    \to
  \mathbf{H}_{infflat}(X,A)
    \to
  \mathbf{H}(X,A)
$$


The objects on the left are **[[principal ∞-bundle]]s equipped with flat [[connection on an ∞-bundle|∞-connection]]** . The first morphism forgets their [[higher parallel transport]] along finite volumes and just remembers the parallel transport along infinitesimal volumes. The last morphism finally forgets also this connection information.

=--

+-- {: .num_defn #deRhamTheorem}
###### Definition

For $A \in \mathbf{H}_{th}$ an abelian [[∞-group]] object we say that the **[[de Rham theorem]]** for $A$-coefficients holds in $\mathbf{H}_{th}$ if for all $X \in \mathbf{H}_{th}$ the
[infinitesimal path inclusion](#InclusionOfConstantIntoInfinitesimalIntoAllPaths)


$$
  \Im(X) \to \mathbf{\Pi}(X)
$$

is an equivalence in $A$-[[cohomology]], hence if for all $n \in \mathbb{N}$ we have that

$$
  \pi_0 \mathbf{H}_{th}(\mathbf{\Pi}(X), \mathbf{B}^n A)
  \to

  \pi_0 \mathbf{H}_{th}(\Im(X), \mathbf{B}^n A)
$$

is an [[isomorphism]].

=--

If we follow the notation of note \ref{CrystallineCohomology} and moreover write $\vert X \vert = \vert \Pi X \vert$ for the <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#GeometricRealization">intrinsic geometric realization</a>, then this becomes

$$
  H^{\bullet}_{dR, synth}(X,A) \simeq H^\bullet(|X|, A_{disc})
  \,,
$$

where on the right we have ordinary cohomology in [[Top]] (for instance realized as [[singular cohomology]]) with coefficients in the [[discrete group]] $A_{disc} := \Gamma A$ underlying the cohesive group $A$.

In certain contexts of infinitesimal neighbourhoods of cohesive $\infty$-toposes the de Rham theorem in this form has been considered in ([SimpsonTeleman](#SimpsonTeleman)).



#### Formal cohesive $\infty$-groupoids
 {#FormalInfinityGroupoids}


Recall that a [[groupoid object in an (infinity,1)-category]] is equivalently an [[1-epimorphism]] $X \longrightarrow \mathcal{G}$, thought of as exhibiting an [[atlas]] $X$ for the groupoid $\mathcal{G}$.

Now an $\infty$-Lie algebroid is supposed to be an $\infty$-groupoid which is only infinitesimally extended over its base space $X$. Hence: 

A groupoid object $p \colon X \longrightarrow \mathcal{G}$ is _infinitesimal_ if under the [[reduction modality]] $\Re$ (equivalently under the [[infinitesimal shape modality]] $\Im$) the [[atlas]] becomes an [[equivalence in an (infinity,1)-category|equivalence]]: $\Re(p), \Im(p) \in Equiv$.

For example the tangent $\infty$-Lie algebroid $T X$ of any $X$ is the [[unit of a monad|unit]] of the [[infinitesimal shape modality]].

$$
  \eta^{\Im}_X \;\colon\; X \stackrel{}{\longrightarrow} \Im X
  \,.
$$

It follows that every such $\infty$-Lie algebroid $X \to \mathcal{G}$ canonically maps to the tangent $\infty$-Lie algebroid of $X$ -- the _anchor map_. The naturality square of the unit $\eta^{\Im}_{p}$ exhibits the morphism:

$$
  \array{
     X & \stackrel{id}{\longrightarrow} & X
     \\
     \downarrow^{\mathrlap{p}} && \downarrow^{\mathrlap{\eta^\Im_X}}
     \\
      &&  \Im X
     \\
     \downarrow && \downarrow^{\mathrlap{\Im p}}_\simeq
     \\
     \mathcal{G}
     &\stackrel{\eta^{\Im}_{\mathcal{G}}}{\longrightarrow}& \Im \mathcal{G}
  }
$$


#### Lie theory {#LieTheory}

(...)

The discussion at _[synthetic differential ∞-groupoid -- Lie differentiation](synthetic+differential+infinity-groupoid#LieDifferentiation)_ immediately generalizes to produce a concept of Lie differentiation in any differentially cohesive context. This Lie differentiation is just the flat modality of the differential cohesion but regarded as cohesive over its induced [[infinitesimal cohesion]]. As such, there is a left adjoint to Lie differentiation, given by the corresponding shape modality. However, the substance of Lie theory here will be to restrict this adjunction to [[geometric ∞-stacks]]. On the geometric $\infty$-stacks the Lie differentiation via passage to inffinitesimal cohesion will yield actual $L_\infty$-algebras, but some structure is required to make the formal [[Lie integration]] of these lang indeed in [[geometric ∞-stacks]].


(...)



#### Deformation theory
 {#StrucDeformationTheory}

For $C^{op}$ any [[(∞,1)-site]] the construction of the
[[tangent (∞,1)-category]] $T_{C} \to C$ provides a canonical infinitesimal thickening of $C$:


$$
  C
  \stackrel{\overset{cod}{\leftarrow}}{\stackrel{\overset{\Delta}{\to}}{\underset{dom}{\leftarrow}}}
  C^{\Delta[1]}
  \stackrel{\overset{L}{\to}}{\underset{\Omega^\infty}{\leftarrow}}
  \,,
$$

where the $\infty$-functor pair on the right forms a
$cod$-[[relative (∞,1)-adjunction]]. The composite $L \circ i$ is the [[cotangent complex]] functor for $C$ and $\Omega^\infty$ is fiberwise the canonical map out of the [[stabilization]].

The image of $i$ is contained in that of $\Omega^\infty$. Therefore we may restrict the $(cod \dashv i)$-adjunction on the right to the [[full sub-(∞,1)-category]] $\tilde T_C$ of $C^{\Delta[1]}$ on thise objects in the image of $\Omega^\infty$. This yields an infinitesimal neighbourhood of [[(∞,1)-sites]]

$$
  C^{op}
  \stackrel{\overset{i}{\hookrightarrow}}{\underset{cod}{\leftarrow}}
  (\tilde T_C)^{op}
  \,.
$$

(...)

#### Idelic structure


See at _[[differential cohesion and idelic structure]]_.




## Examples

* [[formal smooth ∞-groupoid]]
* [[infinitesimally thickened Sierpinski topos]]


## Related concepts

* [[infinitesimal cohesive (infinity,1)-topos]]

* [[differential homotopy type theory]]

[[!include cohesion - table]]


## References


The material discussed here corresponds to the most part to sections 3.5 and 3.10 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

Exposition:

* {#Loregian19} [[Fosco Loregian]], *Cohesion in Rome*, talk notes, Dec. 2019  ([pdf](https://tetrapharmakon.github.io/stuff/cohesive_rome.pdf), [[LoregianCohesion.pdf:file]])


For references on the general notion of _[[cohesive (∞,1)-topos]]_, see there.

The following literature is related to or subsumes by the discussion here.

Something analogous to the notion of [[infinity-connected (infinity,1)-site|∞-connected site]] and the
[[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] is the content of section 2.16.  of

* {#SimpsonTeleman} [[Carlos Simpson]], [[Constantin Teleman]], _deRham theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))


The [infinitesimal path ∞-groupoid adjunction](#LieTheory) $(\Re \dashv \Im \dashv \&)$ is essentially discussed in section 3 there.

The characterization of infinitesimal extensions and formal smoothness by adjoint functors (in 1-[[category theory]]) is considered in

* {#KontsevichRosenbergSpaces} [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative spaces_, preprint MPI-2004-35 ([pdf](http://nlab.mathforge.org/nlab/files/KontsevichRosenbergNCSpaces.pdf), [ps](http://www.mpim-bonn.mpg.de/preblob/2331), [dvi](http://www.mpim-bonn.mpg.de/preblob/2303))
 

in the context of _[[Q-categories]]_ .

The notion of forming [[petit topos|petit]] $(\infty,1)$-toposes of &#233;tale objects over a given object appears in

* {#Lurie} [[Jacob Lurie]], _[[Structured Spaces]]_
 

* {#Carchedi} [[David Carchedi]], _The Meaning of &#201;tale Stacks_ ([arXiv:1212.2282](http://arxiv.org/abs/1212.2282))
 



[[!redirects differential cohesion]]
[[!redirects differential cohesive (∞,1)-topos]]
[[!redirects differential cohesive ∞-topos]]
[[!redirects differential cohesive (∞,1)-toposes]]
[[!redirects differential cohesive ∞-toposes]]

[[!redirects differential cohesive (infinity,1)-topos]]
[[!redirects differential cohesive infinity-topos]]
[[!redirects differential cohesive (infinity,1)-toposes]]
[[!redirects differential cohesive infinity-toposes]]

[[!redirects cohesive (infinity,1)-topos -- infinitesimal cohesion]] 

[[!redirects differentially cohesive topos]]

[[!redirects elastic topos]]
[[!redirects elastic toposes]]
[[!redirects elastic topoi]]

[[!redirects elastic (∞,1)-topos]]
[[!redirects elastic (∞,1)-toposes]]

[[!redirects elastic (infinity,1)-topos]]
[[!redirects elastic (infinity,1)-toposes]]


[[!redirects ∞-elastic site]]
[[!redirects ∞-elastic sites]]

[[!redirects elastic model topos]]
[[!redirects elastic model toposes]]




