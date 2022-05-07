+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

\tableofcontents

## Idea

We discuss a refinement of the traditional notion of _[[Atiyah Lie groupoids]]_ (the [[Lie groupoids]] which are the [[Lie integration]] of [[Atiyah Lie algebroids]] of $G$-[[principal bundles]]) from [[differential geometry]] to [[higher differential geometry]] and generally to [[higher geometry]].

* _[General idea](#GeneralIdea)_

* _[In higher prequantum geometry: motivation and survey](#InHigherPrequantumGeometryMotivationAndSurvey)_

### General idea
 {#GeneralIdea}

Briefly, for $G$ an [[∞-group]] in an [[(∞,1)-topos]] and $P \to X$ a $G$-[[principal ∞-bundle]], its _higher Atiyah groupoid_ is the [[groupoid object in an (∞,1)-category|groupoid object]] $At(P)$ such that the

* object of [[objects]] is $X$;

* object of [[morphisms]] is the collection of all $G$-equivariant maps between all pairs of [[fibers]] of $P$.

In these vague words this is precisely the same description as for the traditional Atiyah groupoid. Definition \ref{HigherAtiyahGroupoid} below makes precise what this means in [[higher geometry]].

Besides generalizing the traditional definition to [[homotopy theory]], the notion of higher Atiyah groupoids also generalizes from [[concrete objects]] such as [[Lie groups]] to general objects in an [[(∞,1)-topos]] (general [[∞-stacks]], not necessarily "supported on points"), notably to _[[moduli ∞-stacks]]_ for [[cocycles]] in [[differential cohomology]]. For instance if we assume that the ambient [[(∞,1)-topos]] $\mathbf{H}$ is [[cohesive (∞,1)-topos|cohesive]] and consider $\mathbb{G} \in \mathrm{Grp}(\mathbf{H})$  a _[[sylleptic ∞-group]]_, then there is the [[moduli ∞-stack]] $\mathbf{B}\mathbb{G}_{\mathrm{conn}}$ of _$\mathbb{G}$-[[principal ∞-connections]]_ and this is itself again a [[group object in an (∞,1)-category|group object]]. 
A $(\mathbf{B}\mathbb{G}_{\mathrm{conn}})$-[[principal ∞-bundle]] is equivalently a $(\mathbf{B}^2\mathbb{G})$-[[principal ∞-connection]] "without [[curving]]". For instance if $\mathbb{G} = U(1)$ is the [[circle group]] in [[smooth ∞-groupoids]], then 
$\mathbf{B}(\mathbf{B}\mathbb{G}_{\mathrm{conn}})$ classifies [[circle 2-bundle with connection]] without 2-form part: in parts of the literature this is known as "[[bundle gerbes]] with connective structure but without [[curving]]".

So the general definition considered here assigns a higher Atiyah groupoid to a "bundle gerbe with connective structure but no [[curving]]". It turns out that this is the _[[Courant 2-groupoid]]_ which [[Lie integration|Lie integrates]] the [[standard Courant Lie 2-algebroid]] traditionally induced by this data.

The  notion of higher Atiyah groupoids is more general still: the definition does not really require that the object fed into the construction is a plain [[principal ∞-bundle]]. It may notably also be a genuine [[principal ∞-connection]] (hence _with_ "[[curving]]"). We show below that the corresponding higher Atiyah groupoid is that groupoid object whose [[∞-group of bisections]] is the [[quantomorphism n-group]] of the principal $\infty$-connection regarded as a [[prequantum n-bundle]].

In summary, the [[higher geometry|higher geometric]] generalization of the notion of Atiyah groupoids unifies all three of the traditional notions of [[Atiyah groupoid]], of [[Courant 2-groupoid]] and of [[quantomorphism group]] and refines each of these to [[higher geometry]]:

[[!include higher Atiyah groupoid - table]]

At the same time the definition of higher Atiyah groupoids in [[(∞,1)-topos theory]], def. \ref{HigherAtiyahGroupoid} below, is very simple, almost tautological, identifying it as a very fundamental notion in [[(∞,1)-topos theory]]/[[homotopy type theory]].


### In higher prequantum geometry: motivation and survey
 {#InHigherPrequantumGeometryMotivationAndSurvey}


Higher Atiyah groupoids play a central role in [[higher prequantum geometry]]. 

> under construction

#### Ordinary prequantum geometry in terms of automorphisms in slices
 {#OrdinaryPrequantumGeometryInTermsofAutomorphismsInSlices}

A sequence of time-honored  traditional concepts in [[geometric quantization]]/[[prequantum geometry]] is

| [[Lie groups]]: | [[Heisenberg group]] | $\hookrightarrow$ | [[quantomorphism group]] | $\hookrightarrow$ |   [[gauge group]]  | 
|--|--|--|--|--|--|
| [[Lie algebras]]: | [[Heisenberg Lie algebra]] | $\hookrightarrow$ | [[Poisson Lie algebra]] | $\hookrightarrow$ | twisted [[vector fields]] |

For instance in the [[geometric quantization]] of the [[electromagnetic field|electrically]] [[charged particle|charted]] [[particle]] [[sigma-model]] we have a [[prequantum circle bundle]] $P$ with [[connection on a bundle]] $\nabla$ on a [[cotangent bundle]] $X = T^* Y$ which is essentially the [[pullback]] of the [[electromagnetic field]]-bundle on [[target space|target]] [[spacetime]] $Y$. Its _[[quantomorphism group]]_ is the group of [[diffeomorphisms]] $P \stackrel{\simeq}{\to} P$ of the total space of the prequantum bundle which preserve the connection (also called the _[[contactomorphism]]_ of $(P,\nabla)$ regarded as a [[regular contact manifold]]). For the following it is convenient to say this using the language of _[[moduli stacks]]_: we may regard $X$ as a [[representable functor|representable]] [[sheaf]] on the [[site]] of [[smooth manifolds]] (a "[[smooth space]]") and then moreover as a [[representable functor|representable]] [[stack]] on this site (a "[[smooth groupoid]]") and make use of the tautological existence of the [[moduli stack]] of $U(1)$-[[principal connections]], which we write $\mathbf{B}U(1)_{conn}$ (we don't need further details right now, but they can be found for instance at _[[circle n-bundle with connection]]_ for details). By definition this is such that for any $X$ a map $\nabla \colon X \to \mathbf{B}U(1)_{conn}$ is equivalently a $U(1)$-[[principal connection]] and such that a [[homotopy]] $\eta \colon \nabla_1 \to \nabla_2$ between two such maps is equivalently a [[gauge transformation]] between two such connections. With this formulation a [[quantomorphism]] of the [[prequantum bundle]] $\nabla$ is equivalently a diagram of the form as on the right of

$$
  \mathbf{QuantMorph}(\nabla)
  =
  \left\{
  \array{
    X &&\underoverset{\simeq}{\phi}{\to}&& X
    \\
    & \searrow &\swArrow_{\eta}& \swarrow
    \\
    && \mathbf{B}U(1)_{conn}
  }
  \right\}
$$

in the [[(2,1)-category]] of [[stacks]], namely a [[diffeomorphism]] $\phi \colon X \stackrel{\simeq}{\to} X$ of the base space of the bundle together with a [[gauge transformation]] of $U(1)$-[[principal connections]] $\eta \colon \phi^* \nabla \stackrel{\simeq}{\to} \nabla$.

The [[quantomorphism group]] is naturally an ([[infinite-dimensional Lie group|infinite dimensional]]) [[Lie group]]. Its [[Lie algebra]] is the [[Poisson bracket]] [[Lie algebra]]. If $X$ is equipped with the structure of a [[Lie group]] itself (notably if it is a [[vector space]]), then the sub-Lie algebra of that on the [[invariant differential form|invariant vectors]] is the [[Heisenberg Lie algebra]] and the Lie group corresponding to that is the [[Heisenberg group]].
 
One also says that a triangular diagram as above is an autoequivalence of the "modulating" map $\nabla \colon X \to \mathbf{B}U(1)_{conn}$ in the _[[slice (infinity,1)-category|slice (2,1)-category]]_ of [[stacks]]/[[smooth groupoids]] over $\mathbf{B}U(1)_{conn}$. 

Such autoequivalences in slices are familiar from basic concepts of [[Lie groupoid]] theory. For $\mathcal{G} = (\mathcal{G}_1 \stackrel{\to}{\to} \mathcal{G}_0)$ a [[Lie groupoid]], we may regard the inclusion of its manifold of objects as an [[atlas]] being a map $p_\mathcal{G} \colon\mathcal{G}_0 \to \mathcal{G}$. Regarding this atlas as an object in the [[slice (infinity,1)-category|slice (2,1)-category]] of [[stacks]]/[[smooth groupoids]] over $\mathcal{G}$, its autoequivalences are diagrams as on the right of

$$
  \mathbf{BiSect}(p_{\mathcal{G}})
  =
  \left\{
    \array{
      \mathcal{G}_0 &&\stackrel{\phi}{\to}&& \mathcal{G}_0
      \\
      & \searrow &\swArrow_\eta & \swarrow
      \\
      && \mathcal{G}
    }
  \right\}
  \,.
$$

This is a [[diffeomorphism]] $\phi \colon \mathcal{G}_0 \stackrel{\simeq}{\to} \mathcal{G}_0$ of the [[smooth manifold]] of [[objects]] equipped with a [[natural transformation]] $\eta$ whose component map is a [[smooth function]] that assigns to each point $q \in \mathcal{G}_0$ a [[morphism]] in $\mathcal{G}$ of the form $\eta_q \colon q \to \phi(q)$. This collection of data is known as a _[[bisection]]_ of a [[Lie groupoid]]. Bisections naturally form a group $\mathbf{BiSect}(p_{\mathcal{G}})$ , which is all the more manifest if we understand them as autoequivalences of the atlas in the slice, called the [[group of bisections]].

This perspective of regarding maps of [[smooth groupoids]] as objects in the slice over their codomain (an elementary step in [[higher category theory]]/[[(infinity,1)-topos theory|higher topos theory]], but not common in traditional differential geometry) turns out to be useful and drives all of the refinements, generalizations and theorems that we discuss in the following: we will see that higher [[prequantum geometry]] is essentially the geometry insice [[slice (infinity,1)-topos|higher slice categories]] of [[infinity-stack|higher stacks]] over [[moduli infinity-stack|higher moduli stacks]] of [[principal infinity-connection|higher principal connections]].

Before we get there, notice the following...

#### The need for higher prequantum bundles
 {#TheNeedForHigherPrequantumBundles}

The tools of [[geometric quantization]] mainly apply to [[quantum mechanics]] and only partially to [[quantum field theory]]. In particular in the context of _[[extended prequantum field theory]]_ in [[dimension]] $n$ a [[prequantum bundle]] over the ([[phase space|phase]]-)space of [[field (physics)|fields]] is to be refined (de-[[transgression|transgressed]]) to a _[[prequantum n-bundle]]_ over the [[moduli ∞-stack]] of [[field (physics)|fields]]. Therefore in order to apply [[geometric quantization]] to [[extended prequantum field theory]] to obtain [[extended quantum field theory]] we first need extended/higher prequantum geometry.

For instance the [[prequantum n-bundle|prequantum 3-bundle]] for standard [[3d Chern-Simons theory|3d]] [[Spin group]] [[Chern-Simons theory]] is modulated by the differential [[smooth first fractional Pontryagin class]]

$$
  \array{
    \mathbf{B}Spin_{conn} 
     &\stackrel{\tfrac{1}{2}\hat \mathbf{p}_1}{\to}&
    \mathbf{B}^3 U(1)_{conn}
    \\
    \downarrow && \downarrow & forget \; connections
    \\
    \mathbf{B}Spin 
     &\stackrel{\tfrac{1}{2}\mathbf{p}_1}{\to}&
    \mathbf{B}^3 U(1)
    \\
    \downarrow && \downarrow & geometric\;realization
    \\
    B Spin &\stackrel{\tfrac{1}{2}p_1}{\to}& K(\mathbb{Z},4)    
  }
  \,,
$$

modulating/clsasifying the universal _[[Chern-Simons circle 3-bundle with connection]]_ (also known as a _[[bundle 2-gerbe]]_) over the [[moduli stack]] of [[field (physics)|fields]] of $G$-Chern-Simons theory, which is the moduli stack $\mathbf{B}G_{conn}$ of $G$-[[principal connection]].

Similarly the [[prequantum n-bundle|prequantum 7-bundle]] for [[7d Chern-Simons theory]] on [[string 2-group]] [[principal infinity-connections|principal 2-connections]] is given by the differential [[smooth second fractional Pontryagin class]]

$$
  \array{
    \mathbf{B}String_{conn} 
     &\stackrel{\frac{1}{6}\hat \mathbf{p}_2}{\to}&
    \mathbf{B}^7 U(1)_{conn}
    \\
    \downarrow && \downarrow & forget\; connections
    \\
    \mathbf{B}String 
     &\stackrel{\frac{1}{6}\mathbf{p}_2}{\to}&
    \mathbf{B}^7 U(1)
    \\
    \downarrow && \downarrow & geometric\; realization
    \\
    B String &\stackrel{\frac{1}{6}p_2}{\to}& K(\mathbb{Z},8)
  }
  \,,
$$

modulating/classifying the universal _[[Chern-Simons circle 7-bundle with connection]]_ over the moduli 2-stack $\mathbf{B}String_{conn}$ of [[string 2-group]] [[principal infinity-connection|principal 2-connections]].



Therefore we want to lift the [above](#OrdinaryPrequantumGeometryInTermsofAutomorphismsInSlices) table of traditional notions to [[higher geometry]]...


#### Brief recollection: Higher geometry

In order to say this, clearly we need some basics of [[higher geometry]]...

$$
  \array{
     && Groupoids
     \\
     & \swarrow && \searrow^{\mathrlap{nerve}}
     \\
     Categories && &&  Kan complexes
     \\
     & \searrow && \swarrow
     \\
     && (\infty,1)-Categories
  }
  \,.
$$

Important construction principle for [[(∞,1)-categories]]: [[simplicial localization]]. For $\mathcal{C}$ a [[category]] with some subset of morphisms $W \hookrightarrow Mor(\mathcal{C})$ declared to be "[[weak equivalences]]", the [[simplicial localization]] 

$$
  L_W \mathcal{C} \in (\infty,1)Cat
$$

is the [[universal construction|universal]] $(\infty,1)$-category obtained from $\mathcal{C}$ by universally turning each weak equivalence into an actual [[homotopy equivalence]] in the sense of [[homotopy theory]].

In particular let $C$ be a [[site]], assumed for simplicity to have [[point of a topos|enough points]]. Declare then that in the [[functor category]] $Func(C^{op}, KanCplx)$, hence in [[Kan complex]]-valued presheaves, the weak equivalences are the [[stalk|stalkwise]] [[homotopy equivalences]] of Kan complexes. Then

$$
  \mathbf{H} \coloneqq Sh_{\infty}(C) \coloneqq L_{W} Func(C^{op}, KanCplx)
$$

is called the _[[(∞,1)-topos]]_ of [[(∞,1)-sheaves]]/[[∞-stacks]] on $C$.

An [[A-∞ algebra]]-object $G$ in such an $(\infty,1)$-topos such that $\pi_0(G)$ is a [[group]] is called an [[∞-group]] "with geometric structure as encoded by the test spaces $C$". The canonical source of $\infty$-groups are the [[homotopy fiber products]] of point inclusions $* \to X$ of any object X, the [[loop space object]]

$$
  \Omega X \coloneqq {*} \underset{X}{\times} {*}
  \,.
$$

In fact this are _all_ the [[∞-groups]] that there are, up to equivalence: forimg [[loop space objects]] is an [[equivalence of (∞,1)-categories]]

$$
  Grp(\mathbf{H})
   \stackrel{\overset{\Omega}{\leftarrow}}{\underoverset{\mathbf{B}}{\simeq}{\to}}
  \mathbf{H}^{*/}_{\geq 1}
$$

between [[∞-groups]] and [[pointed object|pointed]] [[connected object in an (∞,1)-topos|connected]] objects. The inverse equivalence $\mathbf{B}$ is the _[[delooping]]_ operation.

We say that such an $(\infty,1)$-topos $\mathbf{H}$ is _[[cohesive]]_ if it is equipped with an [[adjoint triple]] of [[idempotent monad|idempotent]] (co)/[[(∞,1)-monads]]

| [[shape modality]] | | [[flat modality]] | | [[sharp modality]]  |
|--|--|--|--|--
| idemp. monad | | idemp. comonad | | idemp. monad |
| $\Pi$ | $\dashv$ | $\flat$ | $\dashv$ | $\sharp$ |

This implies (strictly speaking we need [[differential cohesion]] for that, coming from another adjoint triple of (co)monads) that for every [[braided ∞-group]] $\mathbb{G} \in Grp(\mathbf{H})$ there is a canonical object $\mathbf{B}\mathbb{G}_{conn}$ which modulats $\mathbb{G}$-[[principal ∞-connections]].



#### Higher Atiyah groupoids

Looking at the [above](#OrdinaryPrequantumGeometryInTermsofAutomorphismsInSlices) table and noticing the [above](#TheNeedForHigherPrequantumBundles) need for higher prequantum bundles, we should try to find an analogous table of concepts in [[higher geometry]], something like this:

[[!include slice automorphism groups in higher prequantum geometry - table]]


(...)

The way all these notions and theorems work is by considering [[automorphism ∞-groups]] of the classifying (or rather: modulating) maps $\nabla \colon X \to \mathbf{B}\mathbb{G}_{conn}$ of a [[prequantum ∞-bundle]] in the [[slice (∞,1)-topos]] over the domain. For instance

$$
  \mathbf{QuantMorph}(\nabla)  
  =
  \left\{
    \array{
      X && \underoverset{\simeq}{\phi}{\to} && X
      \\
      & {}_{\mathllap{\nabla}}\searrow &\swArrow& \swarrow_{\mathrlap{\nabla}}
      \\
      && \mathbf{B}\mathbb{G}_{conn} 
    }
  \right\}
  \,.
$$

The others are obtained by succesively forgetting connection data. For instance

$$
  \BiSect(Cou(\nabla))  
  =
  \left\{
    \array{
      X && \underoverset{\simeq}{\phi}{\to} && X
      \\
      & {}_{\mathllap{\nabla_1}}\searrow &\swArrow& \swarrow_{\mathrlap{\nabla_1}}
      \\
      && \mathbf{B}(\mathbf{B}\mathbb{G}_{conn})
     }
   \right\}
   \,.
$$

and

$$
  \BiSect(At(\nabla))  
  =
  \left\{
    \array{
      X && \underoverset{\simeq}{\phi}{\to} && X
      \\
      & {}_{\mathllap{\nabla_0}}\searrow &\swArrow& \swarrow_{\mathrlap{\nabla_0}}
      \\
      && \mathbf{B}\mathbb{G}
    }
  \right\}
  \,.
$$

The extension sequence is then schematically simply the following

$$
  \left\{
    \array{
      && X
      \\
      & \swarrow &  & \searrow
      \\
      & \searrow &\swArrow& \swarrow
      \\
      && \mathbf{B}\mathbb{G}_{conn} 
    }
  \right\}
  \; \to \;
  \left\{
    \array{
      X &&\stackrel{\simeq}{\to}&& X
      \\
      & {}_{\mathllap{\nabla}}\searrow &\swArrow& \swarrow_{\mathrlap{\nabla}}
      \\
      && \mathbf{B}\mathbb{G}_{conn}
    }
  \right\}
  \;
  \to
  \;
  \left\{
    \array{
      X && \stackrel{\simeq}{\to} && X
    }
  \right\}
$$

in this generality this now includes various other notions, too:

[[!include higher Atiyah groupoid - table]]



#### The central theorem: Quantomorphism $\infty$-group extensions

+-- {: .num_theorem }
###### Theorem

For $\mathbb{G}$ a [[braided ∞-group]] and $\nabla \colon X \to \mathbf{B}\mathbb{G}_{conn}$ a higher prequantum geometry with respect to $\mathbb{G}$ there is a long [[homotopy fiber sequence]]

$$
  \left(\Omega \mathbb{G}\right)\mathbf{FlatConn}\left(\nabla\right)
  \to
  \mathbf{QuantMorph}(\nabla)
  \to 
  \mathbf{HamSympl}(\nabla)
  \stackrel{\nabla \circ (-)}{\to}
  \mathbf{B}\left(\left(\Omega \mathbb{G}\right)\mathbf{FlatConn}\left(\nabla\right) \right) 
  \,.
$$

Similarly there is the [[Heisenberg infinity-group]] extension

$$
  (\Omega \mathbb{G})\mathbf{FlatConn}(X)
   \to
  \mathbf{Heis}(\nabla)
   \to 
  G
$$

=--

+-- {: .num_theorem }
###### Theorem

The [[Lie differentiation]] of the [[∞-group extension]] sequence of prop. \ref{QuantomorphismExtension} is a [[homotopy fiber sequence]] of [[L-∞ algebras]] 

$$
  \mathbf{H}(X, \flat \mathbf{B}^{n-1}\mathbb{R})
  \to
  \mathfrak{Poisson}(X,\omega) \to \mathcal{X}_{Ham}(X,\omega)
  \stackrel{\iota_{(-)\omega}}{\to}
  \mathbf{B}\mathbf{H}(X, \flat \mathbf{B}^{n-1}\mathbb{R})
  \,,
$$

where

* $\mathfrak{Poisson}(X,\omega)$ is the [[Poisson Lie n-algebra]] as defined in ([Rogers 11](#Rogers11)).

* $\mathcal{X}_{Ham}$ is the Lie algebra of [[vector fields]] restricted to the [[Hamiltonian vector fields]];

* $\mathbf{H}(X, \flat (\mathbf{B}^{n-1})\mathbb{R})$ is the [[chain complex]] for flat [[de Rham cohomology]] in the given degree, regarded as an abelian [[L-∞ algebra]].

=--



The following table shows what this sequence reduces to when one chooses $\mathbb{G} = \mathbf{B}^{n-1}U(1)$.

[[!include geometric quantization extensions - table]]

#### Examples: $String$ and $Fivebrane$ as Heisenberg $\infty$-groups

+-- {: .num_example }
###### Example

For $G$ a simply connected semisimple compact Lie group such as the [[spin group]], let 

$$
  \nabla \coloneqq
   \exp\left(2 \pi i \int_{S^1} [S^1, \tfrac{1}{2}\hat \mathbf{p}_1]\right)
  \;\colon\; G \to \mathbf{B}^2 U(1)_{conn}
$$ 

be the canonical [[circle 2-bundle with connection]] over it. Then the [[Heisenberg infinity-group|Heisenberg 2-group]] [[infinity-group extension|extension]]

$$
  U(1)\mathbf{FlatConn}(G)
   \to
  \mathbf{Heis}(\nabla)
   \to
  G
$$

is the [[string 2-group]] extension

$$
  \mathbf{B}U(1) \to String(G) \to G
  \,.
$$

=--

(by classification of extensions by cohomology... by Lie 2-algebra computation...)

(and analogously for [[fivebrane 6-group]]...)

$$
 \mathbf{B}^6 U\left(1\right) 
   \to 
  \mathbf{Heis}\left(\exp\left(2 \pi i \int_{S^1} \left[S^1, \tfrac{1}{2}\hat \mathbf{p}_2\right] \right)\right) \to String
$$


## Definition
 {#Definition}

We now turn to the formal definition of higher Atiyah groupoids and the basic constructions on them.

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. Let $G \in Grp(\mathbf{H})$ be a [[group object in an (∞,1)-category|group object]] in $\mathbf{H}$, an [[∞-group]].

We define now for every $G$-[[principal ∞-bundle]] $P \to X$ in $\mathbf{H}$ a _[[groupoid object in an (∞,1)-category|groupoid object]]_ $At(P) \in Grpd(\mathbf{H})$ in $\mathbf{H}$. In order to do so we invoke two basic facts.

+-- {: .num_prop #EffectiveEpisAreEquivalentlyGroupoids}
###### Proposition

The construction of forming the [[Cech nerve]] of a [[morphism]] consitutes an [[equivalence of (∞,1)-categories]] from that of [[1-epimorphisms]] to that of [[groupoid objects in an (∞,1)-category|groupoid objects]] in $\mathbf{H}$:

$$
  (\mathbf{H}^{\Delta^1})_{1epi}
  \stackrel{\simeq}{\to}
  Grpd(\mathbf{H})
 \,.
$$

=--

This is a refined version of one of the [[Giraud-Rezk-Lurie axioms]] characterizing [[(∞,1)-topos]], discussed at _[[groupoid object in an (∞,1)-category]]_.

+-- {: .num_remark }
###### Remark

In terms of traditional terminology in the literature on [[topological stacks]]/[[differentiable stacks]] etc, this says that a groupoid object in $\mathbf{H}$ is equivalently an object $X \in \mathbf{H}$ which is equipped with an [[atlas]] $X_0 \to X$.

=--

Write $\mathbf{B}G \in \mathbf{H}$ for the [[delooping]] of $G$ in $\mathbf{H}$ (the [[moduli ∞-stack]] of $G$-[[principal ∞-bundles]], as the following proposition asserts:

+-- {: .num_prop #ClassificationOfGPrincipalBundles}
###### Proposition

The operation of forming [[(∞,1)-fibers]] ([[homotopy fibers]]) constitutes an [[equivalence of ∞-groupoids]]

$$
  fib 
  \;\colon\;
  \mathbf{H}(X, \mathbf{B}G)
  \to 
  G Bund(X)
  \,.
$$

=--

This is discussed at _[[principal ∞-bundle]]_.

Using these two facts we now set:

+-- {: .num_defn #HigherAtiyahGroupoid}
###### Definition

For $P \to X$ a $G$-[[principal ∞-bundle]] in $\mathbf{H}$, its **Atiyah groupoid** is the [[groupoid object in an (∞,1)-category|groupoid object]] $At \in \mathrm{Grpd}(\mathbf{H}) \simeq (\mathbf{H}^{\Delta^1})_{1epi}$ which is the [[1-image]] projection of the classifying map $g \colon X \to \mathbf{B}G$:

$$
  g 
  \;\colon\;
  X
   \stackrel{}{\to}
  At(P) \coloneqq im_1(g)
  \hookrightarrow
  \mathbf{B}G
  \,.
$$  

=--

+-- {: .num_remark #AtiyahGroupoidIsCechNerve}
###### Remark

By the discussion at _[[1-image]]_, the 1-image projection of any morphism $f \colon X \to Y$ in an [[(∞,1)-topos]] is equivalently given as the canonical map given by the [[(∞,1)-colimit]] over the [[Cech nerve]]

$$
  X \to im_1(f) \simeq \underset{\rightarrow}{\lim} (X^{\times^{\bullet+1}_Y})
  \,.
$$

This means that regarded as an object of $Grpd(\mathbf{H})$, the Atiyah groupoid $At(P)$ _is_ simply the [[Cech nerve]] of the classifying map. This means that the definition of Atiyah groupoids in [[higher geometry]] is much more fundamental than in traditional [[geometry]]. 

=--

## Properties

### Equivalence of Atiyah-groupoid bisections to slice automorphisms

We discuss how the [[∞-group of bisections]] of a higher Atiyah groupoid is canonically equivalent to the $\mathbf{H}$-valued [[automorphism ∞-group]] of the modulating map that gave rise to it, regarded as an object in the [[slice (∞,1)-topos]] over its [[codomain]]. 

To this end we need the following two definitions

+-- {: .num_defn #HValuedAutomorphismGroup}
###### Definition

For $f \colon X \to Y$ a [[morphism]] in an [[(∞,1)-topos]] $\mathbf{H}$, its **$\mathbf{H}$-valued [[automorphism ∞-group]]** $\mathbf{Aut}_{\mathbf{H}}(f)$ is the [[dependent product]] over $Y$ over the [[automorphism ∞-group]] of $f$ regarded as an object in the [[slice (∞,1)-topos]] $\mathbf{H}_{/Y}$:

$$
  \mathbf{Aut}_{\mathbf{H}}(f)
  \coloneqq
  \underset{Y}{\prod} \mathbf{Aut}_{/Y}(f)
  \,.
$$

=--

+-- {: .num_remark #Concretification}
###### Remark

For [[concrete object|non-concrete]] codomains $Y$ one is usually interested in the [[concretification]] of this group. To be discussed... For an example see at _[The quantomorphism $n$-group](#TheQuantomorphismNGroups)_ below.

=--

+-- {: .num_prop #HValuedAutomorphismAsFiber}
###### Proposition

For $f \colon X \to Y$ a morphism in $\mathbf{H}$, its $\mathbf{H}$-valued slice automorphism $\infty$-group according to prop. \ref{HValuedAutomorphismGroup} sits in an [[(∞,1)-pullback]] [[diagram]]

$$
  \array{
    \mathbf{Aut}_{\mathbf{H}}(f)
    &\to&
    \mathbf{Aut}(X)
    \\
      \downarrow^{\mathrlap{}} && \downarrow^{\mathrlap{f \circ (-)}}
    \\
    {*}
    &\stackrel{\vdash f}{\to}&
    [X,Y]
  }
  \,,
$$

where $\mathbf{Aut}(X) \hookrightarrow [X,X]$ is the ordinary [[automorphism ∞-group]] of $X$ in $\mathbf{H}$.

=--


+-- {: .num_defn}
###### Definition

For $\mathcal{G} \in Grpd(\mathbf{H})$ a [[groupoid object in an (∞,1)-category|groupoid object]] in an [[(∞,1)-topos]] $\mathbf{H}$, its **[[∞-group of bisections]]** $\mathbf{BiSect}(\mathcal{G}) \in Grpd(\mathbf{H})$ is the $\mathbf{H}$-valued automorphism $\infty$-group, def. \ref{HValuedAutomorphismGroup}, of the [[atlas]] $\phi_{\mathcal{G}} \colon \mathcal{G}_0 \to \mathcal{G}$ of $\mathcal{G}$ under prop. \ref{EffectiveEpisAreEquivalentlyGroupoids}:

$$
  \mathbf{BiSect}(\mathcal{G})
  \coloneqq
  \mathbf{Aut}_{\mathbf{H}}(\phi_{\mathcal{G}})
  \,.
$$

=--

With this the following proposition is immediate, but important for the interpretation of higher Atiyah groupoids:

+-- {: .num_prop}
###### Propostition

For $c \;\colon\; X \to \mathbf{F}$ a [[morphism]] in an [[(∞,1)-topos]] $\mathbf{H}$, modulating an [[fiber ∞-bundle]] $P \to X$, there is an canonical [[equivalence in an (infinity,1)-category|equivalence]] of [[∞-groups]] 

$$
  \mathbf{BiSect}(At(P))
  \simeq
  \mathbf{Aut}_{\mathbf{H}}(c)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

We may read this as saying that the higher Atiyah groupoid of an [[fiber ∞-bundle]] is the [[universal property|universal]] solution to the problem of finding a [[groupoid object in an (∞,1)-category|groupoid object]] whose [[∞-group of bisections]] reproduces a given slice [[automorphism ∞-group]]. In many applications, this is indeed the crucial property that drives the interest in higher Atiyah groupoids, see the _[Examples](#Examples)_ below.

=--


### Sequences of inclusions of Atiyah-bisection $\infty$-groups
 {#SequencesOfInclusionsOfGroupsOfBisections}

Let $\mathbf{H}$ be an [[(∞,1)-topos]] which is [[cohesive (∞,1)-topos|cohesive]]. As discussed there, this implies that there is an internal notion of [[differential cohomology]] and in particular of [[principal ∞-connections]] in $\mathbf{H}$. We note here how the canonical forgetful maps between [[moduli ∞-stacks]] of [[principal ∞-bundles]] equipped with differing degree of differential refinement induce canonical inclusions of the corresponding higher Atiyah groupoids. 

Let $\mathbb{G} \in Grp(\mathbf{H}) be a $[[braided ∞-group]]. Then there exists, by [[cohesion]], a canonical notion of $\mathbb{G}$-[[principal ∞-connections]], whose [[moduli ∞-stack]] we denote $\mathbf{B}\mathbb{G}_{\mathrm{conn}}$. This is equipped with a canonical map

$$
  \mathbf{B}\mathbb{G}_{conn} \to \mathbf{B}\mathbb{G}
$$

which "forgets the connection". Then for $\nabla \colon X \to \mathbf{B}\mathbb{G}_{conn}$ a $\mathbb{G}$-[[principal ∞-connection]] we write

$$
  \nabla_0 \;\colon\; X \stackrel{\nabla}{\to} 
   \mathbf{B}\mathbb{G}_{conn} \to \mathbf{B}\mathbb{G}
$$

for the corresponding underlying map.

+-- {: .num_prop #InclusionOfNableBisectionsIntoNable0Bisections}
###### Proposition

The [[dependent sum]] along this map induces a canonical map of [[∞-groups]] 

$$
  \mathbf{BiSect}(At(\nabla))
  \to   
  \mathbf{BiSect}(At(\nabla_0))
  \,.
$$

=--

If we regard $\nabla$ as a [[prequantum n-bundle]] then this is a canonical inclusion of the [[quantomorphism n-group]] into the $\infty$-group of "$\nabla_0$-twisted diffeomorphisms".


If $\mathbb{G}$ is even a [[sylleptic ∞-group]], then the above moduli $\infty$-stacks have a further [[delooping]] and we obtain a 2-step sequence of forgetful maps

$$
  \mathbf{B}^2 \mathbb{G}_{conn}
  \to 
  \mathbf{B}(\mathbf{B}\mathbb{G}_{conn})
  \to 
   \mathbf{B}^2 \mathbb{G}
  \,.
$$

Accordingly:

+-- {: .num_prop #InclusionOfNableBisectionsIntoNable1AndNabla0Bisections}
###### Proposition

The [[dependent sum]] along these maps induces inclusions of $\infty$-groups

$$
  \mathbf{BiSect}(At(\nabla))
  \to 
  \mathbf{BiSect}(At(\nabla_1))
  \to
  \mathbf{BiSect}(At(\nabla_0))  
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This now interprets as the inclusion 

1. of the [[quantomorphism n-group]] into the $\infty$-group of bisections of the [[higher Courant groupoid]];

1. $\infty$-group of bisections of the [[higher Courant groupoid]] into that of "$\nabla_0$-twisted diffeomorphisms".


=--

In summary we have the following table of inclusions

[[!include slice automorphism groups in higher prequantum geometry - table]]

See below at _[Examples-- The traditional Courant Lie 2-algebroid](#TheTraditionalCourantLie2Algebroid)_ for more on this.



## Examples
 {#Examples}

We first show how the general notion of _higher Atiyah groupoid_ reproduces various traditonal structures.

* _[The traditonal Atiyah Lie groupoid](#TheTraditionalAtiyagLieGroupoid)_

* _[The traditional Courant Lie 2-algebroid](#TheTraditionalCourantLie2Algebroid)_

* _[The traditional quantomorphism group](#TheTraditionalQuantomorphismGroup)_

* _[The quantomorphism n-groups](#TheQuantomorphismNGroups)_

* _[The traditional Heisenberg group](#TheTraditionalHeisenbergGroup)

* _[The Heisenberg n-group](#TheHeisenbergnGroup)



### The traditional Atiyah Lie groupoid
 {#TheTraditionalAtiyagLieGroupoid}

We discuss how the traditional notion of [[Atiyah Lie groupoids]] in traditional [[differential geometry]] is a special case of higher Atiyah groupoids of def. \ref{HigherAtiyahGroupoid}.

To set this up we take the ambient [[(∞,1)-topos]] to be 

$\mathbf{H} \coloneqq$ [[Smooth∞Grpd]] and make use of the canonical embeddings

[[SmthMfd]] $\hookrightarrow$ [[diffeological space|DiffeologicalSpace]] $\hookrightarrow$ [[smooth spaces|SmoothSpace]] $\hookrightarrow$ [[Smooth∞Grpd]],

and 

[[Lie groupoid|LieGrpd]] $\simeq$ [[differentiable stack]] $\hookrightarrow$ [[Smooth∞Grpd]]

which are understood in the following.

+-- {: .num_prop }
###### Proposition

For $G$ a [[Lie group]], $X$ a [[smooth manifold]] and $P \to X$ a $G$-[[principal bundle]], the traditional [[Atiyah Lie groupoid]] of $P$ is equivalent to that of def. \ref{HigherAtiyahGroupoid}.

=--

+-- {: .proof}
###### Proof

Write $g \colon X \to \mathbf{B}G$ for the classifying map of $P \to X$, by prop. \ref{ClassificationOfGPrincipalBundles}. 

By remark \ref{AtiyahGroupoidIsCechNerve} the higher Atiyah groupoid $At(P)$ is simply the [[Cech nerve]] of this map. Since $G$ and $X$ and hence $P$ are all [[truncated object in an (infinity,1)-category|0-truncated objects]], hence $\mathbf{B}G$ a [[1-truncated]] object, this Cech nerve is [[coskeleton|2-coskeletal]] and hence is sufficient to consider the first three degrees. By definition these are

$$
  At(P)
  \simeq
  \left(
    X \underset{\mathbf{B}G}{\times}X \underset{\mathbf{B}G}{\times}X 
      \stackrel{\to}{\stackrel{\to}{\to}} 
    X \underset{\mathbf{B}G}{\times}X
      \stackrel{\to}{\to}
    X 
  \right)
  \,,
$$ 

where $X \underset{\mathbf{B}G}{\times}X $ denotes the [[homotopy fiber product]] of $g$ with itself, and so forth. To see what this object is, pick any $U \in $ [[CartSp]], and observe that 

$$
  \mathbf{H}(U, X\underset{\mathbf{B}G}{\times}X )
  \simeq
  \mathbf{H}(U,X) \underset{\mathbf{H}(U,\mathbf{B}G)}{\times} \mathbf{H}(U,X)
$$

(using that the [[(∞,1)-categorical hom]]-[[(∞,1)-functor]] $\mathbf{H}(U,-)$ preserves [[(∞,1)-limits]]) is equivalently the [[set]] of [[triples]] consisting of two [[smooth functions]] $\phi_1, \phi_2 \colon X$ and a [[gauge transformation]] between the [[pullback|pulled-back bundles]] $\eta \colon \phi_1^* P \to \phi_2^* P$ on $U$.

Since $U$ is topologically [[contractible topological space|contractible]], and hence every $G$-[[principal bundle]] over $U$ admits a [[section]], every such triple induces a [[function]], in fact a [[bijection]], from the set of lifts $\hat \phi_1 \colon U \to P$ of $\phi_1$ to the set of lifts $\hat \phi_2 \colon U \to P$ which are $C^\infty(U,G)$-equivariant. By $G$-equivariant every pair consisting of a single lift $\hat \phi_1$ and its image $\eta(\hat \phi_1)$ already uniquely determes $\eta$. Therefore the above set of triples is [[natural isomorphism|naturally isomorphic]] to the set of [[smooth functions]] $U \to P \times_G P \coloneqq (P \times P)/_{diag} G$. This is precisely the [[smooth manifold]] of [[morphisms]] of the traditional [[Atiyah Lie groupoid]]. Since this is true for all $U \in $ [[CartSp]] and [[natural transformation|naturally]] so, and since [[CartSp]] is a [[site]] of definition of [[Smooth∞Grpd]] it follows by the [[(∞,1)-Yoneda lemma]] (which in the present cases reduces to the ordinary [[Yoneda lemma]]), we have a [[natural equivalence]]

$$
  X \underset{\mathbf{B}G}{\times} X 
  \simeq 
  P \times_G P
  \,.
$$

In this manner it is immediate to check that this identification respects all the structure maps, and hence the above Cech nerve is indeed identified as the [[simplicial manifold]] which is the [[nerve]] of the traditional [[Atiyah Lie groupoid]] $(P \times_G P \stackrel{\to}{\to} X)$.

=--

### The traditional Courant Lie 2-algebroid 
 {#TheTraditionalCourantLie2Algebroid}

There is a traditional construction which assigns to a [[bundle gerbe]] "with connective structure but without [[curving]]" a [[Courant Lie 2-algebroid]]. We discuss here how this is the [[Lie differentiation]] of the corresponding higher Atiyah groupoid.

In order to do so, we pick again, as [above](#TheTraditionalAtiyagLieGroupoid), as ambient context $\mathbf{H} = $ [[Smooth∞Grpd]].

+-- {: .num_prop }
###### Proposition

For $\mathbb{G} \coloneqq U(1) \in LieGrp \hookrightarrow Grp(\mathbf{H})$ the [[circle Lie group]] (which is in particular a [[sylleptic ∞-group]]), the sequence of maps of [[moduli ∞-stacks]]

$$
  \mathbf{B}^2 U(1)_{conn}
  \to 
  \mathbf{B}(\mathbf{B}U(1)_{conn})
  \to
  \mathbf{B}^2 U(1)
$$

of prop. \ref{InclusionOfNableBisectionsIntoNable1AndNabla0Bisections} is presented under the canonical equivalence [[Smooth∞Grpd]] $\simeq _{L_{lwhe}} Func(CartSp^{op}_{smooth}, sSet)$ by the image under the [[Dold-Kan correspondence]] of the evident sequence of [[chain maps]]

$$
  \array{
    U(1) &\stackrel{id}{\to}& U(1) &\stackrel{id}{\to}& U(1)
    \\
    \downarrow^{\mathrlap{d log}} && \downarrow^{\mathrlap{d log}} && \downarrow^{\mathrlap{0}}
    \\
    \Omega^1 &\stackrel{id}{\to}& \Omega^1 &\stackrel{\mathrlap{0}}{\to}& 0
    \\
    \downarrow^{\mathrlap{d}} && \downarrow^{\mathrlap{0}} && \downarrow^{\mathrlap{0}}    
    \\
    \Omega^2 &\to& 0 &\to& 0
  }
  \,,
$$

where on the left we have the [[Deligne complex]] for degree-3-[[ordinary differential cohomology]].

=--

+-- {: .proof}
###### Proof

This is a direct consequence of the discussion at _[[circle n-bundle with connection]]_.

=--

+-- {: .num_remark }
###### Remark

This makes precise how

* $\mathbf{B}^2 U(1)_{conn}$ is the [[moduli infinity-stack|moduli 2-stack]] of [[circle 2-bundles with connection]];

* $\mathbf{B}(\mathbf{B}U(1)_{conn})$ is the moduli 2-stack of circle 2-bundle "with connection but without [[curving]]";

* $\mathbf{B}^2 U(1)$ is the moduli 2-stack of [[circle 2-group]]-[[principal 2-bundles]].

=--

Let

$$
  \nabla_1 \colon X \to \mathbf{B}(\mathbf{B}U(1)_{conn})
$$

be the map modulating [[circle 2-bundle with connection]] but "without [[curving]]". Then then higher Atiyah groupoid of th $(\mathbf{B}U(1)_{conn})$-[[principal 2-bundle]] classified by this map has as higher Atiyah groupoid the corresponding _[[Courant Lie 2-groupoid]]_: the object which is the [[Lie integration]] of the traditional [[Courant Lie 2-algebroid]] associated with $\nabla_1$.

To see we observe that the corresponding [[∞-group of bisections|2-group of bisections]] is

$$
  \mathbf{Aut}_{\mathbf{H}}(\nabla_1)
  \coloneqq
  \underset{\mathbf{B}(\mathbf{B}U(1)_{conn})}{\prod}
  \mathbf{Aut}_{/\mathbf{B}(\mathbf{B}U(1)_{conn})}(\nabla_1)
  \,.
$$

This has as objects [[diagrams]] in $\mathbf{H}$ of the form

$$
  \array{
     X &&\underoverset{\simeq}{\phi}{\to}&& X
     \\
     & {}_{\mathllap{\nabla_1}}\searrow &\swArrow_\eta& \swarrow_{\mathrlap{\nabla_1}}
     \\
     && \mathbf{B}(\mathbf{B}U(1)_{conn})
  }
  \,,
$$

hece equivalently pairs consisting of a [[diffeomorphism]] $\phi \colon X \to X$ and a [[gauge transformation]] (of 2-connections without [[curving]])

$$
  \eta 
    \;\colon \;
  \phi^* \nabla_1 \to \nabla_1
  \,.
$$

The morphisms are accordingly the suitable [[natural transformations]] of these diagrams.

This is precisely the 2-group of "bundle gerbe symmetries" of $\nabla_1$ which is studient in ([Collier](#Collier)). With this identification the main result there is the above claim.

Moreover, the canonical inclusions of smooth 2-groups of prop. \ref{InclusionOfNableBisectionsIntoNable1AndNabla0Bisections} reproduces, under [[Lie differentiation]], the inclusion of the [[Poisson Lie 2-algebra]] into that [[Lie 2-algebra]] of sections of the corresponding [[Courant Lie 2-algebroid]] observed in ([Rogers 10](#Rogers10)).


### The traditional quantomorphism group
 {#TheTraditionalQuantomorphismGroup}

For $\nabla \colon X \to \mathbf{B}U(1)_{conn}$
the [[group of bisections]] of the corresponding Atiyah groupoid is the [[quantomorphism group]] of $\nabla$ regarded as a [[prequantum bundle]].

(...)


### The quantomorphism $n$-groups
 {#TheQuantomorphismNGroups}

In ([Rogers 11](#Rogers)) is a proposal for the generalization of the notion of [[Poisson bracket]] [[Lie algebra]] of a [[symplectic manifold]] to a notion of [[Poisson Lie n-algebra]] induced by an _[[n-plectic manifold]]_. Since the [[Lie integration]] of the [[Poisson bracket]] is traditionally known as the _[[quantomorphism group]]_, the Lie integration of these [[Poisson Lie n-algebras]] should be called an _[[quantomorphism n-group]]_.

We here discuss a general abstract theory of [[quantomorphism n-groups]] as [[∞-groups of bisections]] of a higher Atiyah groupoid associated with a [[principal ∞-connections]]. Then we show that under [[Lie differentiation]] this reproduces the construction in ([Rogers 11](#Rogers11)). 

[[!include geometric quantization extensions - table]]

For all of the following, let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] equipped with [[differential cohesion]]. Let $\mathbb{G} \on Grpd(\mathbf{H})$ be equipped with the structure of a [[braided ∞-group]]. Then there is a canonical object $\mathbf{B}\mathbb{G}_{conn} \in \mathbf{H}$ which is the [[moduli ∞-stack]] of $\mathbb{G}$-[[principal ∞-connections]].

Fox such a [[principal ∞-connection]] given by a map

$$
  \nabla \;\colon\; X \to \mathbf{B}\mathbb{G}_{conn}
  \,.
$$


+-- {: .num_remark }
###### Remark

By prop. \ref{HValuedAutomorphismAsFiber} the $\mathbf{H}$-valued automorphism $\infty$-group $\mathbf{Aut}_{\mathbf{H}}(\nabla)$ according to def. \ref{HValuedAutomorphismGroup} sits in an [[(∞,1)-pullback]] diagram of the form

$$
  \array{
    \mathbf{Aut}_{\mathbf{H}}(\nabla)
    &\to&
    \mathbf{Aut}(X)
    \\
    \downarrow && \downarrow^{\mathrlap{\nabla \circ (-)}}
    \\
    {*}
    &\stackrel{\vdash \nabla}{\to}& [X, \mathbf{B}\mathbb{G}_{conn}]
  }
  \,.
$$

By remark \ref{Concretification} we want to pass to its [[concretification]]. Indeed, in the above diagram the [[mapping ∞-stack]] $[X, \mathbf{B}\mathbb{G}_{conn}]$ is not quite yet the correct [[moduli ∞-stack]] for $\mathbb{G}$-[[principal ∞-connections]] on $X$, but instead its [[differential concretification]] $\mathbb{G}\mathbf{Conn}(X)$ is, as defined at _[concretification - Examples - Of differential moduli](concretification#ConcretificationOfDifferentialModuli)_. Therefore the following definition states the above pullback diagram with that replacement.

=--

+-- {: .num_defn }
###### Definition

Let $\mathbb{G}$ be a [[braided ∞-group]] as above and let $\nabla \;\colon\; X \to \mathbf{B}\mathbb{G}_{conn}$ be a $\mathbb{G}$-[[principal ∞-connection]].

The **[[quantomorphism ∞-group]]** $QuantMorph(\nabla) \in \mathrm{Grp}(\mathbf{H})$ of a $\nabla$ is the object fitting into the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{QuantMorph}(\nabla)
    &\to&
    \mathbf{Aut}(X)
    \\
    \downarrow && \downarrow^{\mathrlap{\nabla \circ (-)}}
    \\
    {*}
    &\stackrel{\vdash \nabla}{\to}& \mathbb{G}\mathbf{Conn}(X)
  }
  \,.
$$


=--

+-- {: .num_defn #HamiltonianSymplectomorphismInfinityGroup}
###### Definition

The [[Hamiltonian symplectomorphism ∞-group]] $\mathbf{HamSympl}(\nabla)$ is the [[1-image]] of the canonical map $\mathbf{QuantMorph}(\nabla) \to \mathbf{Aut}(X)$.


=--

+-- {: .num_prop #QuantomorphismExtension}
###### Proposition

The [[quantomorphism ∞-group]] $\mathbf{QuantMorph}(\nabla)$ in an [[∞-group extension]] of the Hamiltonian symplectomorphism $\infty$-group of def. \ref{HamiltonianSymplectomorphismInfinityGroup} by the [[∞-group]] $(\Omega\mathbb{G})\mathbf{FlatConn}(X)$ of [[concretification|concretified]] [[flat ∞-connections]] on $X$: we have a [[homotopy fiber sequence]]

$$
  (\Omega\mathbb{G})\mathbf{FlatConn}(X)
  \to 
  \mathbf{QuantMorph}(\nabla)
  \to 
  \mathbf{HamSympl}(\nabla)
  \,.
$$

Moreover, at least at the level of the underlying objects, this extension is classified by the [[cocycle]] $\mathbf{HamSympl}(\nabla) \stackrel{\nabla \circ (-)}{\to} \mathbf{B}((\Omega\mathbb{G})\mathbf{FlatConn}(X))$ in that we have a long [[homotopy fiber sequence]]

$$
  (\Omega\mathbb{G})\mathbf{FlatConn}(X)
  \to 
  \mathbf{QuantMorph}(\nabla)
  \to 
  \mathbf{HamSympl}(\nabla)
  \stackrel{\nabla \circ (-)}{\to}
  \mathbf{B}((\Omega \mathbb{G})\mathbf{FlatConn}(X))
  \,.
$$

=--

We now restrict this to a special case and describe it more in detail:

Let $\mathbf{H} = $ [[Smooth∞Grpd]], let $X \in $ [[SmthMfd]] $\hookrightarrow$ [[Smooth∞Grpd]] and let $\mathbb{G} \coloneqq \mathbf{B}^{n-1}U(1) \in \mathrm{Grp}(\mathbf{H})$ be the [[circle n-group]]. Finally let $\omega \colon X \to \Omega^{n+1}$ be an [[n-plectic form]] and $\nabla \;\colon\; X \to \mathbf{B}^n U(1)_{conn}$ a prequantization by a [[prequantum circle n-bundle]].

+-- {: .num_prop }
###### Proposition

The [[Lie differentiation]] of the [[∞-group extension]] sequence of prop. \ref{QuantomorphismExtension} is a [[homotopy fiber sequence]] of [[L-∞ algebras]] 

$$
  \mathbf{H}(X, \flat \mathbf{B}^{n-1}\mathbb{R})
  \to
  \mathfrak{Poisson}(X,\omega) \to \mathcal{X}_{Ham}(X,\omega)
  \stackrel{\iota_{(-)\omega}}{\to}
  \mathbf{B}\mathbf{H}(X, \flat \mathbf{B}^{n-1}\mathbb{R})
  \,,
$$

where

* $\mathfrak{Poisson}(X,\omega)$ is the [[Poisson Lie n-algebra]] as defined in ([Rogers 11](#Rogers11)).

* $\mathcal{X}_{Ham}$ is the Lie algebra of [[vector fields]] restricted to the [[Hamiltonian vector fields]];

* $\mathbf{H}(X, \flat (\mathbf{B}^{n-1})\mathbb{R})$ is the [[chain complex]] for flat [[de Rham cohomology]] in the given degree, regarded as an abelian [[L-∞ algebra]].

=--

### The traditional Heisenberg group
 {#TheTraditionalHeisenbergGroup}

(...) [[Heisenberg group]] (...)

### The Heisenberg $n$-group
 {#TheHeisenbergnGroup}


If $X = G \in \mathbf{H}$ has itself [[∞-group]] structure, then it is natural to restrict the [[quantomorphism ∞-group]] to that subgroup of the [[Hamiltonian symplectomorphism ∞-group]] whose elements come from the $G$-[[∞-action]] on itself. This is the corresponding _[[Heisenberg ∞-group]]_.

+-- {: .num_defn }
###### Definition

With all assumtions as [above](#TheQuantomorphismNGroups), let $G \in Grp(\mathbf{H})$ be an [[∞-group]] and let 

$$
  G \hookrightarrow \mathbf{Aut}(G)
$$

(where on the right we have the [[automorphism ∞-group]] of the underlying object $G \in \mathbf{H}$) the inclusion that exhibits the left $G$-[[∞-action]] on itself. 

The the **[[Heisenberg ∞-group]]** $\mathbf{Heis}(\nabla)$ is the [[(∞,1)-pullback]] in the [[diagram]]

$$
  \array{
    \mathbf{Heis}(\nabla)
    &\to&
    \mathbf{QuantMorph}(\nabla)
    \\
    \downarrow && \downarrow
    \\
    G &\to& \mathbf{Aut}(G)
  }
  \,.
$$

=--

The following is an immediate consequence of the definition

+-- {: .num_prop  #HeisenbergInfinityGroupExtension}
###### Proposition

The [[Heisenberg ∞-group]] $\mathbf{Heis}(\nabla)$ is an [[∞-group extension]] of $G$ by $(\Omega \mathbb{G})\mathbf{FlatConn}(G)$: we have a [[homotopy fiber sequence]] of [[∞-groups]]

$$
  (\Omega \mathbb{G})\mathbf{FlatConn}(G)
  \to 
  \mathbf{QuantMorph}(\nabla)
  \to 
  G
  \,.
$$

=--

+-- {: .num_example }
###### Example

In $\mathbf{H} = $ [[Smooth∞Grpd]] consider $G \in LieGrp \hookrightarrow Grp(\mathbf{H})$ a [[connected topological space|connected]], [[simply connected topological space|simply connected]] [[compact Lie group|compact]] [[semisimple Lie group]], say the [[Spin group]] $G = Spin$. Then the [[Killing form]] [[invariant polynomial]] is a pre-3-plectic form on the [[moduli stack]] of $G$-[[principal connections]]:

$$
  \langle -,-\rangle
  \;\colon\;
  \mathbf{B}G_{conn} \to \mathbf{\Omega}_{cl}^4
  \,.
$$

This has a [[higher geometric prequantization]] by the [[smooth first fractional Pontryagin class]], a map

$$
  \tfrac{1}{2}\hat\mathbf{p}_1
  \;\colon\;
  \mathbf{B}G_{conn} \to \mathbf{B}^3 U(1)_{conn}
  \,.
$$

The [[transgression]] of this to maps oout of the [[circle]] yields a [[circle 2-bundle with connection]]

$$
  \nabla 
   \;\colon\;
  G \to [S^1, G]
   \stackrel{[S^1, \frac{1}{2}\hat\mathbf{p}_1]}{\to}
  [S^1, \mathbf{B}^3 U(1)_{conn}]
   \stackrel{\exp(2 \pi i \int_{S^1}(-))}{\to}
  \mathbf{B}^2 U(1)
  \,.
$$

This is a [[prequantum circle 2-bundle]] which prequantizes the canonical [[differential 3-form]] on $G$, the one which is [[invariant differential form|left invariant]] and at the neutral element is $\langle -,[-,-]\rangle$.

Consider now the [[higher prequantum geometry]] of this 2-connection. So now $\mathbb{G} = \mathbf{B}U(1)$.

Observe that 

$$
  \begin{aligned}
    (\Omega \mathbb{G})\mathbf{FlatConn}(G)
    & \simeq
    U(1) \mathbf{FlatConn}(G)
    \\
    & =
    \mathbf{B}U(1)
  \end{aligned}
$$ 

because $G$ is assumed to be [[simply connected topological space|simply connected]]. (Notice that $\mathbf{B}U(1)$ does appear here with its canonical smooth structure: while a [[gauge transformation]] from the trivial $U(1)$-[[principal connection]] to itself is a constant function along $X$, the smooth structure in $U(1)\mathbf{FlatConn}(G)$ comes from how this may vary in parameterized collections ).

Therefore by prop. \ref{HeisenbergInfinityGroupExtension} we have an [[∞-group extension]]

$$
  \mathbf{B}U(1)
  \to
  \mathbf{Heis}(\nabla)
  \to
  G
  \,.
$$

This exhibits the Heisenberg 2-group here as the [[string 2-group]] $String(G)$:

$$
  \mathbf{Heis}(\nabla) \simeq String(G)
  \,.
$$

=--



## Related concepts

[[!include higher Atiyah groupoid - table]]

## References

The [above](#TheTraditionalCourantLie2Algebroid) identification of higher Atiyah groupoids of "bundle gerbes with connective structure but without [[curving]]" with those [[Lie integration|Lie integrating]] the corresponding [[standard Courant Lie 2-algebroid]] is directly implied (under the above translations) by the main result in 

* [[Braxton Collier]], _Infinitesimal Symmetries of Dixmier-Douady Gerbes_ ([arXiv:1108.1525](http://arxiv.org/abs/1108.1525))
 {#Collier}

The corresponding inclusion of the [[Poisson Lie 2-algebra]] into the [[Lie 2-algebra]] of bisections of the [[Courant Lie 2-algebroid]] was first observed in

* [[Chris Rogers]], _2-plectic geometry, Courant algebroids, and categorified prequantization_ ,  [arXiv:1009.2975](http://arxiv.org/abs/1009.2975).
 {#Rogers10}

in the context of _[[2-plectic geometry]]_ over [[smooth manifolds]].

The [[Poisson Lie n-algebra]] over an [[n-plectic manifold]], which by prop. \ref{spring} is the [[Lie differentiation]] of the [[quantomorphism n-group]] of any [[prequantum circle n-bundle]] prequantizing the $n$-plectic form, has been proposed in

* [[Chris Rogers]], _Higher symplectic geometry_ PhD thesis (2011) ([arXiv:1106.4068](http://arxiv.org/abs/1106.4068))
 {#Rogers11}


Most further statements here will appear in 

* [[Domenico Fiorenza]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_
 {#FiorenzaRogersSchreiber}


[[!redirects higher Atiyah groupoids]]

[[!redirects higher gauge groupoid]]
[[!redirects higher gauge groupoids]]
