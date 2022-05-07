
> under construction


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

> This entry follows [Sati-Schreiber 20](#SatiSchreiber20). See there for full details, until this entry here gets cleaned up.



#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

Since the crucial extra [[structures]] carried by an [[orbifold]] are

1. geometric structure (e.g. [[topology|topological]], [[algebraic geometry|algebro-geometric]], [[differential geometry|differential-geometric]], [[supergeometry|super-geometric]], etc.)

1. [[singularities]]

the [[cohomology]] of orbifolds should be such as to provide [[invariants]] which are sensitive not just to the underlying plain [[homotopy type]] of an orbifold (its [[shape modality|shape]]) but also to this extra structure. This means that _orbifold cohomology_ should, respectively, unify

1. geometric cohomology (e.g. [[sheaf cohomology|sheaf]] [[hypercohomology]], [[differential cohomology]], etc.)

1. [[equivariant cohomology]] in its fine form of [[Bredon cohomology]]
 
in the sense that [[differential cohomology|geometric cohomology]] is recovered away from the orbifold [[singularities]] and [[equivariant cohomology]] is recovered right at the [[singularities]], while globally orbifold cohomology provides a unification of these two aspects.

Since any concept of [[cohomology]] (as discussed there) is effectively equivalent to the choice of ambient [[(∞,1)-topos]], the question of defining orbifold cohomology is closely related to the question of how exactly to define the [[(∞,1)-category]] of orbifolds (usually a [[(2,1)-category]]) in the first place. This question is notoriously more subtle than the simple intuitive idea of orbifolds might suggest, as witnessed by the convoluted history of the concept (see e.g. [Lerman 08, Introduction](orbifold#Lerman08)).

\linebreak

### Deficiency of orbifolds as geometric groupoids

A proposal popular among [[Lie theory|Lie theorists]] ([Moerdijk-Pronk 97](orbifold#MoerdijkPronk97)) is to regard an orbifold with local charts $U_i \in G_i Actions$ ([[actions]] of some [[group]] on some local model [[space]]) as the [[geometric stack]] obtained by gluing the corresponding [[homotopy quotients]]/[[quotient stacks]] $U_i \!\sslash \!G_i$. If $\mathbf{H}$ is the ambient [[cohesive (∞,1)-topos]] in which this takes place (for instance $\mathbf{H} = $ [[Smooth∞Groupoids]], [[SuperFormalSmooth∞Groupoids]], etc.) and if $G \in Grp \overset{Disc}{\hookrightarrow} Grp(\mathbf{H})$ is a [[discrete group]] in which all the [[isotropy groups]] of the orbifold are contained, this gives an object 

$$
  \left(
  \array{
    \mathcal{X}
    \\
    \downarrow^{\mathrlap{faith}}
    \\
    \mathbf{B}G
  }
  \phantom{{}^{faith}}
  \right)
  \;\in\;
  \left( 
    \mathbf{H}_{/\mathbf{B}G}
  \right)_{\leq 0}
  \hookrightarrow
  \mathbf{H}_{/\mathbf{B}G}
$$

in the [[slice (∞,1)-topos]] over the [[delooping]] $\mathbf{B}G = \ast \sslash G$ of $G$, which is still a [[0-truncated object]], reflecting that as a [[functor]] of [[groupoids]] the morphism $\mathcal{X} \to \mathbf{B}G$ is a [[faithful functor]].

Accordingly, if this is -- or were -- the correct formalization of the nature of [[orbifolds]] $\mathcal{X}$, then the corresponding orbifold cohomology has [[coefficients]] given by objects $\mathcal{A} \in \mathbf{H}_{/\mathbf{B}G}$ and cohomology sets being the [[connected components]] of the [[(∞,1)-categorical hom-spaces]]

$$
  H_{\mathbf{B}G}\big( \mathcal{X}, \mathcal{A}\big)
  \;\coloneqq\;
  \pi_0 \mathbf{H}_{/\mathbf{B}G}\big( \mathcal{X}, \mathcal{A}\big)
  \,.
$$

This concept of orbifold cohomology does fully reflect the geometric nature of orbifolds. It also reflects _some_ equivariance aspect. For example if $\mathcal{X} = \ast \sslash G$ is the one-point orbifold with singularity given by a finite group $G$, and if $V \in G Representations$ is a [[linear representation]], with $K(V,n)\sslash G \in \infty Groupoids_{/\mathbf{B}G} \overset{Disc}{\hookrightarrow} \mathbf{H}_{/\mathbf{B}G}$ its [[Eilenberg-MacLane space]], then 

$$
  H_{\mathbf{B}G}\big( 
    \mathbf{B}G, K(V,n)\sslash G
  \big)
  \;\simeq\;
  H^n_{grp}(G,V)
$$

is the [[group cohomology]] of $G$ with [[coefficients]] in $V$.

However, this definition does _not_ reflect [[Bredon cohomology|Bredon]]-[[equivariant cohomology]] around the orbifold singularities. Instead, it really given (geometric/stacky refinement) of _[[cohomology with local coefficients]]_.


$\,$

### Lift of orbifolds to geometric global homotopy theory

Hence the proposal of [Moerdijk-Pronk 97](orbifold#MoerdijkPronk97), that an [[orbifold]] should be regarded as a certain [[geometric stack]], is missing something. It was briefly suggested in [Schwede 17, Introduction](#Schwede17), [Schwede 18, p. ix-x](#Schwede18) that the missing aspect is provided by [[global equivariant homotopy theory]], but details seem to have been left open. 

Here we discuss how to define the required orbifold cohomology in detail and in general. We combine the [[differential cohesion]] for the geometric aspect with the cohesion of [[global equivariant homotopy theory]] that was observed and highlighted in [Rezk 14](#Rezk14).

The following may serve as intuition for the issue with the nature of orbifolds:

Envision the picture of an orbifold singularity and hold a mathemagical magnifying glass over the singular point. Under this magnification you can see resolved the singular point as a fuzzy fattened point, to be called $\mathbb{B}G$.

Removing the magnifying glass, what one sees with the bare eye depends on how one squints:

* The physicist says that what he sees is a singular point, but a point after all. This is the plain [[quotient]]  $\ast = \ast / G$. 

* The Lie geometer says that what she sees is a point transforming under the $G$-[[action]] that fixes it, hence the [[homotopy quotient]] [[groupoid]] $\mathbf{B}G =\ast \sslash G$.

These are two [[adjoint modality|opposite extreme aspects]] of the orbifold singularity $\mathbb{B}G$, but the orbifold singularity itself is more than both of these aspects. The real nature of an orbifold singularity is in fact a point, not a big [[classifying space]] $\mathbf{B} G$ (recall that already $\mathbf{B}\mathbb{Z}_2 = \mathbb{R}P^\infty$), but it is a point that also remembers the group [[action]], for that characterizes how the singularity is being singular.

$$
   \array{
       && 
       { \text{orbifold singularity} \atop {\mathbb{B}G} }
      \\
      & {}^{\mathllap{&#643;_{sing}}}\swarrow & {{\phantom{A}} \atop {  \text{opposite extreme} \atop \text{aspects of orbifold singularity} }} & \searrow^{\mathrlap{ \flat_{sing} }}
     \\
     { \text{plain quotient} \atop {\ast = \ast/G} }
     &&
     &&
     { \text{homotopy quotient} \atop { \mathbf{B}G = \ast \sslash G } }
   }
$$

## Definition
  {#Definition}

The definition of orbifold cohomology below in Def. \ref{OrbifoldCohomology} is the canonical [[cohomology]] in a [[slice (infinity,1)-topos|slice]] of the [[globally equivariant homotopy theory]] $\mathbf{H}_{sing}$ of the given ambient [[cohesive (∞,1)-topos]] $\mathbf{H}$. 

For completeness, we first introduce/recall $\mathbf{H}_{sing}$ in Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory} below, as well as its slices to $G$-[[equivariant homotopy theory]] $\mathbf{H}_G$ (Def. \ref{GEquivariantHomotopyTheoryOfCohesiveInfinityTopos} below), following [Rezk 14](#Rezk14).

The key point in the following is the identification of [[orbifolds]] as the [[n-truncated object in an (∞,1)-category|0-truncated]] "$Singularities$-[[codiscrete objects]]" in $\mathbf{H}_{sing}$ (Def. \ref{Orbifold} below), which is consistent in that under passage to [[shape modality|shapes]], i.e. the underlying bare [[globally equivariant homotopy theory|globally equivariant]] [[homotopy types]], it reproduces the standard embedding of [[G-spaces]] into [[globally equivariant homotopy theory]] (Example \ref{GlobalHomotopyQuotientsOfSmoothManifolds} below.)

$\,$

### Globally equivariant cohesive toposes
  {#GloballyEquivariantCohesiveToposes}

We consider here the evident refinement to _geometric cohomology_ hence to _[[differential cohomology]]_ ([[cohesion|cohesive]] [[infinity-stack|∞-stacky]] [[sheaf cohomology]]) of [[globally equivariant homotopy theory]], in Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory} below.

In order to bring out the conceptual appearance of [[orbifolds]] further [below](#OnOrbifolds), we take the liberty of referring to what otherwise is known as the "[[global orbit category]]" instead as the _categories of singularities_ (Def. \ref{CategoryOfSingularities} below).

$\,$


+-- {: .num_defn #CategoryOfSingularities}
###### Definition
**(category of singularities)**

Write

$$
  Singularities
  \;\coloneqq\;
  Groupoids^{cn}_{1,fin}
  \hookrightarrow
  Groupoids_\infty
$$

for the [[(2,1)-category]] of [[connected object|connected]] [[homotopy type with finite homotopy groups|finite groupoids]]. A [[skeleton]] has [[objects]] labeled by [[finite groups]] $G$, and we will denote these objects

$$
  \mathbb{B}G
  \;\in\;
  Singularities
$$

to distinguish them from their image as [[delooping]] groupoids $\mathbf{B} G \in $ [[∞Grpd]]. (As we consider [[(∞,1)-presheaves]] on $Singularities$ with values in [[∞Groupoids]], in Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory} below, these two objects become crucially different, albeit closely related.)

=--

+-- {: .num_remark #SingularitiesInTheLiterature}
###### Remark

The category $Singularities$ in Def. \ref{CategoryOfSingularities}, when generalized from [[finite groups]] to [[compact Lie groups]], is called

* "$Orb$ version 1" in [Henriques-Gepner 07](orbispace#HenriquesGepner07)

* "$Glo$" in [Rezk 14, 2.2](#Rezk14)

* "$Orb$" in [Körschgen 16, 2.1](orbispace#Koerschgen16), [Juran 20, 3.2](#Juran20)

* "$\mathbf{O}_{gl}$" in [Schwede 17](orbispace#Schwede17), [Körschgen 16, 2.2](orbispace#Koerschgen16) 

=--

+-- {: .num_prop #CohesionOfGlobalEquivariantHomotopyTheory}
###### Proposition
**([[global equivariant homotopy theory]] [[cohesive (∞,1)-topos|cohesive]] over [[base (∞,1)-topos]])**

Let $\mathbf{H}$ be any [[(∞,1)-topos]] and consider the [[(∞,1)-category of (∞,1)-presheaves]] on the category of singularities (Def. \ref{CategoryOfSingularities}) over the [[base (∞,1)-topos]] $\mathbf{H}$, hence the [[(∞,1)-functor (∞,1)-category]]

$$
  \mathbf{H}_{sing}
  \;\coloneqq\;
  Sh_\infty\big( Singularities, \mathbf{H}\big)
  \;=\;
  Funct\big( \Singularities^{op}, \mathbf{H}\big)
  \,.
$$

This is a [[cohesive (∞,1)-topos]] over the [[base (∞,1)-topos]] $\mathbf{H}$ in that the [[global section]]-[[geometric morphisms]] enhances to an [[adjoint quadruple]] of [[adjoint (∞,1)-functors]]

\[
  \label{SingularitiesAdjointQuadruple}
  \big(
    \Pi_{sing}
    \dashv
    Disc_{sing}
    \dashv
    \Gamma_{sing}
    \dashv
    coDisc_{sing}
  \big)
  \;\colon\;
  \mathbf{H}_{sing}
    \leftrightarrow
  \mathbf{H}
\]

such that

1. $Disc_{sing}, coDisc_{sing} \;\colon\; \mathbf{H} \to \mathbf{H}_{sing}$ are [[fully faithful (∞,1)-functors]];

1. $\Pi_{sing}$ preserves [[finite products]].

hence inducing an [[adjoint triple]] of [[adjoint modalities]]

$$
  &#643;_{sing}
  \dashv 
  \flat_{sing}
  \dashv
  \sharp_{sing}
  \;\colon\;
  \mathbf{H}_{sing} \to \mathbf{H}_{sing}
$$

("[[shape modality|shape]]", "[[flat modality|flat]]", "[[sharp modality|sharp]]" for singularities).

Moreover, for $G$ a [[finite group]] regarded under the inclusion

$$
  G \in Grp \overset{Disc}\hookrightarrow Grp(\mathbf{H}) \overset{Disc_{sing}}{\hookrightarrow} Grp\left(\mathbf{H}_{sing}\right)
$$

and writing 

$$
  \mathbf{B}G \in \mathbf{H}_{sing}
$$

for its [[delooping]] under $Grp\left( \mathbf{H}_{sing} \right) \underoverset{\simeq}{\mathbf{B}}{\longrightarrow} \mathbf{H}^{\ast/}_{cn}$,

in constrast to the [[(∞,1)-Yoneda embedding]]

$$
  \mathbb{B}G 
  \overset{y}{\longrightarrow}
  Sh_\infty\left( Singularities, \infty \mathrm{Grpd}\right)
  \overset{Disc}{\longrightarrow}
  Sh_\infty\left( Singularities, \mathbf{H}\right)
$$ 

we have

\[
  \label{ShapeOfOrbifoldSingularity}
  \begin{aligned}
     &#643;_{sing} \mathbb{B}G 
     & \simeq\; \ast/G = \ast
     \\
     \flat_{sing} \mathbb{B}G 
     &\simeq\; \ast \sslash G = \mathbf{B}G
  \end{aligned}
\]


=--

+-- {: .proof}
###### Proof

This is immediate by general properties of left/right [[(∞,1)-Kan extension]], using the evident fact that $Singularities$ has [[finite products]] (the [[terminal object in an (∞,1)-category|terminal object]] is $\mathbb{B}1$ and the binary [[Cartesian product]] is give by forming [[direct product groups]]: $\left(\mathbb{B}G_1\right) \times \left( \mathbb{B}G_2\right) \simeq \mathbb{B}\left( G_1 \times G_2\right)$ ). The directly analogous 1-categorical argument is at _[[infinity-cohesive site]]_.

=--

+-- {: .num_example}
###### Example

For $\mathbf{H} =$  [[∞Groupoids]] the [[cohesion]] of Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory} is that of plain [[globally equivariant homotopy theory]] ([Rezk 14, 4.1](#Rezk14)), i.e. without any geometric determination ([[geometrically discrete ∞-groupoids]]).

=--


Conversely we have:

+-- {: .num_prop #SingularitiesAsCoDisc}
###### Proposition
**([[orbifold]] [[singularities]] are the [[codiscrete object|codiscrete]] aspect of [[homotopy quotients]]**)

Let $\mathbf{H}$ itself be a [[cohesive (∞,1)-topos]] over [[∞Groupoids]]

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv coDisc)
  \;\colon\;
  \mathbf{H} \leftrightarrow \infty Groupoids
  \,.
$$


Then in the situation of Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory}

$$
  coDisc_{sing} \mathbf{B}G
  \;\simeq\;
  \mathbb{B}G
  \,.
$$

=--

+-- {: .proof}
###### Proof

Let $\mathcal{S}$ be a cohesive [[(∞,1)-site]] of definition for $\mathbf{H}$, so that 

$$
  \mathbf{H}_{sing}
  \;\simeq\;
  Sh_\infty
  \left(
    \mathcal{S} \times Singularities
    \;,\;
    \infty Groupoids
  \right)
$$

and $\Pi(S) \simeq \ast$ for $S \in \mathcal{S} \overset{y}{\hookrightarrow} \mathbf{H}$.

Then as [[(∞,1)-presheaves]] regarded this way we have

$$
  \begin{aligned}
    coDisc_{sing} \mathbf{B}G
    \;\colon\;
    S \times \mathbb{B}K 
    & \mapsto
    \mathbf{H}_{sing}\left( S \times \mathbb{B}K, coDisc_{sing} Disc \mathbf{B}G \right)
    \\
    & \simeq
    \mathbf{H}\big( 
       S 
         \times 
       \underset{
         \simeq \mathbf{B}K
       }{
       \underbrace{
         \Gamma_{sing}\left( \mathbb{B}K\right)
       }}
       , 
       Disc \mathbf{B}G 
    \big)    
    \\
    & \simeq
    \infty Groupoids\big( 
       \underset{
         \simeq \mathbf{B}K
       }{
       \underbrace{
         \Pi(S \times \mathbf{B}K)
       }}
       \,,
       \mathbf{B}G 
    \big)        
    \\
    & \simeq
    \infty Groupoids\left(
       \mathbf{B} K, \mathbf{B}G
    \right)
    \\
    & \simeq
    \mathbf{H}_{sing}\big(
       \mathbb{B}K, 
       \mathbb{B}G
    \big)
    \\
    & \simeq
    \mathbf{H}_{sing}\big(
       S \times \mathbb{B}K, 
       \mathbb{B}G
    \big)
  \end{aligned}
$$

Here we used the various [[(∞,1)-adjunctions]] and the [[(∞,1)-Yoneda lemma]], and the claim in turn follows by the [[(∞,1)-Yoneda lemma]].

=--


$\,$

### $G$-Equivariant cohesive toposes
  {#EquivariantCohesiveToposes}

In order to speak of $G$-[[equivariant homotopy theory]] (Def. \ref{GEquivariantHomotopyTheoryOfCohesiveInfinityTopos} below) inside [[globally equivariant homotopy theory]] (Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory} above) we need a certain concept of faithfulness (Def. \ref{SingularitiesFaithful} below).

For that purpose, recall that in an [[(∞,1)-topos]] the [[pair]] of [[classes]] of [[n-connected object in an (∞,1)-topos|n-connected morphisms]] and [[n-truncated object in an (∞,1)-category|n-truncated morphisms]] for an [[orthogonal factorization system in an (∞,1)-category|orthogonal factorization system]] for all $n \in \{-2,-1\} \sqcup \mathbb{N} \sqcup \{\infty\}$.

In particular this says that a [[1-morphism]] in an [[(∞,1)-topos]] is [[n-truncated object in an (infinity,1)-category|0-truncated]] precisely if it has the [[right lifting property]] against every morphism that is [[n-connected object of an (infinity,1)-topos|0-connected]].

$\,$

Just for the record: 

+-- {: .num_lemma #GammaPreservesnTruncatedMorphisms}
###### Lemma
**($\Gamma_{sing}$ preserves [[n-truncated object in an (∞,1)-category|n-truncated morphisms]])**

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] with $\mathbf{H}_{sing}$ its [[globally equivariant homotopy theory]] from Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory}.

Then in particular the functor (eq:SingularitiesAdjointQuadruple)

$$
  \Gamma_{sing}
  \;\colon\;
  \mathbf{H}_{sing}
  \longrightarrow
  \mathbf{H}
$$

preserves [[n-truncated object in an (∞,1)-category|n-truncated morphisms]] for all $n$.

=--

+-- {: .proof}
###### Proof

By the [[(n-connected, n-truncated) factorization system]] and the [[adjunctions]] in (eq:SingularitiesAdjointQuadruple) the statement is equivalent to 

$$
  Disc_{sing}
  \;\colon\;
  \mathbf{H}
  \longrightarrow
  \mathbf{H}_{sing}
$$

preserving [[n-connected object in an (∞,1)-topos|n-connected morphisms]]. These are [[effective epimorphisms in an (∞,1)-category]] satisfying an extra condition. Both the definition of effective epimorphisms as well as that extra conditions are entirely formulated in terms of [[(∞,1)-limits]] and [[(∞,1)-colimits]] ([this Prop.](n-connected+object+of+an+infinity-topos#CharacterizationByDiagonal)). Since $Disc_{sing}$ is both a left and a right [[adjoint (∞,1)-functor]] by (eq:SingularitiesAdjointQuadruple) it preserves all these.


=--

+-- {: .num_example #EsoAndFullToFaithfulFactoriazation}
###### Example
**(on [[groupoids]] [[(n-connected, n-truncated) factorization system|(0-connected, 0-truncated)]] is [[(eso and full, faithful) factorization system|(eso and full, faithful)]])**

In the [[(∞,1)-topos]] [[∞Groupoids]] the [[n-truncated object in an (infinity,1)-category|1-truncated objects]] are equivalently [[groupoids]] in the sense of [[small categories]] with all [[morphisms]] [[invertible morphism|invertible]]

$$
  Groupoids \simeq \infty Groupoids_{\leq 1} \hookrightarrow \infty Groupoids
$$

Under this identification the [[1-morphisms]] between 1-truncated objects correspond equivalently [[functors]], and we have that these [[1-morphisms]] are

1. [[n-truncated object in an (infinity,1)-category|0-truncated]] precisely if they correspond to [[faithful functors]];

1. [[n-connected object of an (infinity,1)-topos|0-connected]] precisely if they correspond to [[essentially surjective functor|essentially surjective]] and [[full functors]].

In particular a morphism of [[delooping]] groupoids

\[
  \label{BGPrimeToBG}
  \array{
     \mathbf{B} G'
     \\
     \downarrow^{\mathrlap{\mathbf{B} p}}
     \\
     \mathbf{B} G
  }
\]

is a 0-connected morphism in $\infty Groupoids$ precisely if the corresponding [[group homomorphism]] $p \colon G' \to G$ is [[surjective function|surjective]].

=--

Therefore one might say "[[faithful morphism]]" for every [[n-truncated object in an (infinity,1)-category|0-truncated]] morphism in an [[(∞,1)-topos]]. But the terminology "faithful" is used with other meanings, too, and we need to refer to these variants

+-- {: .num_defn #SingularitiesFaithful}
###### Definition
**($Singularities$-faithful morphisms)**

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] with $\mathbf{H}_{sing} \coloneqq Sh_\infty\left( Singularities, \mathbf{H}\right)$ its [[globally equivariant homotopy theory]] according to Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory}. We say that a morphism
$\mathcal{X} \overset{f}{\to} \mathcal{Y}$ in $\mathbf{H}_{sing}$ is _$Singularities$-faithful_ if it has the [[right lifting property]] against morphisms of the form

\[
  \label{Singularities0Connected}
  \left(
    \array{
      \mathbb{B}G'
      \\
      \downarrow^{\mathrlap{\mathbb{B}p}}
      \\
      \mathbb{B}G
    }
    \phantom{{}^{\mathbb{B}^p}}
  \right)
  \;\in\;
  Singularities \overset{Yoneda}{\hookrightarrow} 
  Sh_\infty\left(
    Singularities,
    \infty Groupoids
  \right)
  \overset{Disc}{\hookrightarrow}
  Sh_\infty\left(
    Singularities,
    \mathbf{H}
  \right)
  \;=\;
  \mathbf{H}_{sing}
\]

where $p \;\colon\; G' \to G$ is a _[[surjective function|surjective]]_ [[group homomorphism]].

=--

For the case $\mathbf{H} =$ [[∞Groupoids]] this is the definition of _faithful maps_ in [Rezk 14. Prop. 3.4.1](#Rezk14).

> It seems that the morphisms (eq:Singularities0Connected) are not in general 0-connected in $Sh_\infty(Singularities, \infty Groupoids)$. Them being 0-connected should come down to the statement that for $p \colon G' \to G$ a surjective group homomorphism and $H \subset G$ any subgroup, there always is a lift of $H$ to $G'$ and that any two such lifts are conjugate to each other, in $G'$. But already the first condition fails in general, since not every epimorphism of groups is a [[split epimorphism]].

> Nevertheless and in any case we have the following, which is all we will need:

+-- {: .num_prop #coDiscSingOf0TruncatedMorphismsIsSingularitiesFaithful}
###### Proposition
**($coDisc_{sing}$ of a 0-truncated morphism is $Singularities$-faithful)**

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] with $\mathbf{H}_{sing}$ its [[globally equivariant homotopy theory]] according to Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory}. 

If a morphism $X \overset{f}{\to} Y$ in $\mathbf{H}$ is [[n-truncated object in an (infinity,1)-category|0-truncated]], then its image under $coDisc_{sing} \;\colon\; \mathbf{H} \hookrightarrow \mathbf{H}_{sing}$ is $Singularities$-faithful (Def. \ref{SingularitiesFaithful}).

=--

+-- {: .proof}
###### Proof

This follows by the adjunctions (eq:SingularitiesAdjointQuadruple), the relations (eq:ShapeOfOrbifoldSingularity) and the fact (eq:BGPrimeToBG):

$$
  \phantom{{}^{\mathbb{B}p}}
  \array{
    \mathbb{B}G' &\longrightarrow& coDisc_{sing}(X)
    \\ 
    {}^{\mathllap{\mathbb{B}p}}\big\downarrow 
      &\nearrow&   
    \big \downarrow^{\mathrlap{ coDisc_{sing}(f) }}
    \\
    \mathbb{B}G
    &\longrightarrow&
    coDisc_{sing}(Y) 
  }
  \phantom{AAAA}  
  \;\Leftrightarrow\;\;
  \phantom{A}
  \phantom{{}^{\mathbb{B}p}}
  \array{
    \Gamma_{sing}\left(\mathbb{B}G'\right) 
      &\longrightarrow& 
    X
    \\ 
    {}^{\mathllap{\Gamma_{sing}\left(\mathbb{B}p\right)}}\big\downarrow 
      &\nearrow&   
    \big \downarrow^{\mathrlap{ f }}
    \\
    \Gamma_{sing}\left(\mathbb{B}G\right)
    &\longrightarrow&
    Y
  }
  \phantom{AA}
  \;\;\simeq\;\;
  \phantom{A}
  \array{
    \mathbf{B} G'
      &\longrightarrow& 
    X
    \\ 
    {}^{\mathllap{\mathbf{B}p}}\big\downarrow 
      &\nearrow&   
    \big \downarrow^{\mathrlap{ f }}
    \\
    \mathbf{B} G
    &\longrightarrow&
    Y
  }
$$

=--


+-- {: .num_defn #GlobalOrbitCategory}
###### Definition
**([[global orbit category]])**

Write

$$
  GlobalOrbits
  \;\coloneqq\;
  Singularities^{faith}
$$

for the wide non-[[full sub-(infinity,1)-category]] of $Singularities$ (Def. \ref{CategoryOfSingularities}) with the same [[objects]] $\mathbb{B}G$ but the [[1-morphisms]] required to be 0-truncated as morphisms of $\infty$-groupods, hence to be faithful functors of groupoids (Example \ref{EsoAndFullToFaithfulFactoriazation}), hence to come from _[[injective function|injective]]_ [[group homomorphisms]].

=--


+-- {: .num_remark}
###### Remark

The category $GlobalOrbits$ in Def. \ref{GlobalOrbitCategory}, when generalized from [[finite groups]] to [[compact Lie groups]], is called

* "$Orb$ version 2" in [Henriques-Gepner 07](orbispace#HenriquesGepner07)

* "$Orb$" in [Rezk 14, 4.5](#Rezk14)

and is _not_ the category called "$Orb$" in [Körschgen 16](orbispace#Koerschgen16), [Schwede 17](orbispace#Schwede17), [Schwede 18](global+equivariant+homotopy+theory#Schwede18) (see Remark \ref{SingularitiesInTheLiterature}).

=--

+-- {: .num_prop #GorbitCategory} 
###### Proposition/Definition
**([[slice (∞,1)-category|slice]] of [[global orbit category|global orbits]] is $G$-[[orbit category|orbits]])**

For $G$ a [[finite group]], the [[slice (∞,1)-category|slice]] of the [[global orbit category]] from Def. \ref{GlobalOrbitCategory} over the object $\mathbb{B}G$ is [[equivalence of (∞,1)-categories|equivalent]] to the $G$-[[orbit category]]

$$
  GlobalOrbits_{/\mathbb{B}G}
  \;\simeq\;
  G Orbits
$$

=--

+-- {: .num_defn #GEquivariantHomotopyTheoryOfCohesiveInfinityTopos}
###### Definition
**($G$-[[equivariant homotopy theory]] of a [[cohesive (∞,1)-topos]])**


For $\mathbf{H}$ a [[cohesive (∞,1)-topos]] and $G$ a [[finite group]] we say that the _$G$-[[equivariant homotopy theory]] of $\mathbf{H}$_ is the [[(∞,1)-presheaf (∞,1)-topos]] on the $G$-[[orbit category]] (Def. \ref{GorbitCategory}) over $\mathbf{H}$:

$$
  \begin{aligned}
    \mathbf{H}_G  
    &\coloneqq\;
    Sh_\infty\big( G Orbits , \mathbf{H} \big)
    \\
    & \simeq
    Sh_\infty\big( GlobalOrbits_{/\mathbb{B}G} , \mathbf{H} \big)
    \\
    & \simeq
    Sh_\infty\big( GlobalOrbits , \mathbf{H} \big)_{/\mathbb{B}G}
  \end{aligned}
$$

On the right we are displaying immediate [[equivalence of (∞,1)-categories|equivalences]], the first by Prop. \ref{GorbitCategory}, the second by the general slicing behaviour of $\infty$-toposes ([this Prop.](slice+homotopy-topos#SlicingCommutesWithPassingToPresheaves)).

=--

The relation between the [[global homotopy theory]] $\mathbf{H}_{sing}$ (Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory}) and the $G$-[[equivariant homotopy theory]] $\mathbf{H}_G$ (Def. \ref{GEquivariantHomotopyTheoryOfCohesiveInfinityTopos}) is the topic of [Rezk 14](#Rezk14):

+-- {: .num_defn #NormalSubgroupClassifier}
###### Definition
**([[normal subgroup]] classifier, [Rezk 14, 4.1](#Rezk14))**

For $\mathbf{H}$ a [[cohesive (∞,1)-topos]], let

$$
  \mathcal{N}
  \;\in\;
  Sh\big(Singularities, Sets \big)
  \hookrightarrow
  Sh_\infty\big(Singularities, \infty Groupoids \big)
  \overset{}{\hookrightarrow}
  Sh_\infty\big( 
    Singularities, \mathbf{H}
  \big)
$$

be the presheaf which to any [[finite group]] $\mathbb{B}G$ assigns the [[set]] (i.e. [[0-groupoid]]) of [[normal subgroups]] of $G$.

=--

+-- {: .num_prop #SingularitiesFaithfulSliceOverNormalSubgroupClassifier}
###### Proposition
**([Rezk 14](#Rezk14))**

For $\mathbf{H}$ an [[(∞,1)-topos]], with $\mathbf{H}_{sing} \coloneqq Sh_\infty\big( Singularities, \mathbf{H}\big)$ its [[global equivariant homotopy theory]] according to Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory}, there is an [[equivalence of (∞,1)-categories]]

$$
  \array{
    Sh_\infty\big( GlobalOrbits, \mathbf{H}\big)
    &\overset{\simeq}{\longrightarrow}&
    \left(
      Sh_\infty\big( Singularities, \mathbf{H}\big)_{/\mathcal{N}}
    \right)_{\text{singfaith}}
    \;=\;
    \left(
    \left( 
      \mathbf{H}_{sing}
    \right)_{/\mathcal{N}}
    \right)_{singfaith}
  }
$$

between the [[(∞,1)-presheaf (∞,1)-category]] on the [[global orbit category]] according to Def. \ref{GlobalOrbitCategory} and the [[full sub-(∞,1)-category]] of the [[slice (∞,1)-topos]] of $\mathbf{H}_{sing}$ over the normal subgroup classifier $\mathcal{N}$ (Def. \ref{NormalSubgroupClassifier}) on those morphisms to $\mathcal{N}$ which are $Singularities$-faithful according to Def. \ref{SingularitiesFaithful}.

Moreover, if $G$ is a [[finite group]] then slicing over $\mathbb{B}G$ this yields an equivalence

$$
  \array{
    \mathbf{H}_G
    \;\simeq\;
    \left(
      \left( 
        \mathbf{H}_{sing}
      \right)_{/\mathbb{B}G}
    \right)_{singfaith}
  }
$$

between the $G$-[[equivariant homotopy theory]] $\mathbf{H}_G$ (Def. \ref{GEquivariantHomotopyTheoryOfCohesiveInfinityTopos})  and the [[full sub-(∞,1)-category]] on the $Singularities$-faithful objects of the [[slice (∞,1)-category|slice]] of the [[global homotopy theory]] $\mathbf{H}_{sing}$ (Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory}) over $\mathbb{B}G$.

=--


### Orbifolds
 {#OnOrbifolds}

With [[cohesion|cohesive]] [[globally equivariant homotopy theory]] in place, there is now an elegant definition of [[orbifolds]] (Def. \ref{Orbifold} below) which, being fully _[[synthetic mathematics|synthetic]]_ makes manifest good defining properties of the [[category]] of [[orbifolds]] (Remark \ref{OrbifoldsInGloballyEquivariantStillEquivalentToGeometricGroupoids} below).

Not directly evident is that under passing to [[shape modality|shapes]] (underlying [[globally equivariant homotopy theory|globally equivariant]] [[geometrically discrete ∞-groupoids]]) this definition is compatible with the standard embedding of [[G-spaces]] into [[globally equivariant homotopy theory]]. That this indeed is the case is confirmed in Example \ref{GlobalHomotopyQuotientsOfSmoothManifolds} below.

$\,$

+-- {: .num_defn #Orbifold}
###### Definition
**([[orbifold]]**)

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] with $\mathbf{H}_{sing}$ its corresponding [[globally equivariant homotopy theory]] according to Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory}.

For $G \in Grp(\mathbf{H})$ a [[finite group]] we say that an _orbifold with singularities ([[isotropy groups]]) in $G$_ is an [[object]] of the [[slice (∞,1)-topos]] 

$$
  \mathcal{X}
  \;\in\;
  \left(\mathbf{H}_{sing}\right)_{/\mathbb{B}G}
$$

which  is

1. [[n-truncated object in an (infinity,1)-category|0-truncated]] (as an object of the [[slice (infinity,1)-topos|slice]]);

1.  $\sharp_{sing}$-[[modal object|modal]] (hence "$Singularity$-[[codiscrete object|codiscrete]]").

Given such an orbifold, we say that its _underlying [[geometric stack|geometric groupoid]]_ is its $Singularities$-[[flat modality|flat]] aspect:

\[
  \label{OrbifoldUnderlyingGroupoid}
  \flat_{sing}\left( \mathcal{X}\right)
  \;\in\;
  \mathbf{H}_{/\mathbf{B}G}
  \overset{Disc_{sing}}{\hookrightarrow}
  \left(
    \mathbf{H}_{sing}
  \right)_{/\mathbb{B}G}
\]

where on the right we used (eq:ShapeOfOrbifoldSingularity).

If $\mathbf{H}$ is moreover [[differential cohesion|differentially cohesive]] and $V \in Grp(\mathbf{H})$ is a [[∞-group|group object]], then an orbifold $\mathcal{X}$ is called a _$V$-orbifold_ if its underlying [[geometric stack|geometric groupoid]] $\flat_{sing}\left( \mathcal{X}\right)$ (eq:OrbifoldUnderlyingGroupoid) is a [[V-manifold]].

=--

+-- {: .num_example #GlobalHomotopyQuotientOrbifold}
###### Example
**(global [[homotopy quotient]]-[[orbifolds]])**

Let $X \in \mathbf{H}$ be [[n-truncated object in an (infinity,1)-category|0-truncated]] and equipped with a $G$-[[∞-action|action]], with [[homotopy quotient]] $(X \sslash \mathbf{B}G \to \mathbf{B}G) \in \mathbf{H}_{/\mathbf{B}G}$. Then

$$
  \mathcal{X}
  \;\coloneqq\;
  coDisc_{sing}
  \left(
    \array{
      X \sslash G
      \\
      \downarrow
      \\
      \mathbf{B}G
    }
  \right)
  \;\simeq\;
  \left(
    \array{
      coDisc_{sing}\left( X\sslash G\right)
      \\
      \downarrow
      \\
      \mathbb{B}G
    }
  \right)
$$

is an [[orbifold]] with isotropy groups in $G$, according to Def. \ref{Orbifold}.  Here on the right we identified the slice using Prop. \ref{SingularitiesAsCoDisc}.

=--

As a further special case:

+-- {: .num_example #GlobalHomotopyQuotientsOfSmoothManifolds}
###### Example
**(global [[homotopy quotient]]-[[orbifolds]] of [[smooth manifolds]])**

Let $\mathbf{H} \coloneqq$ [[Smooth∞Groupoids]]. For $G$ a [[finite group]], let $X$ be a [[smooth manifold]] equipped with a smooth $G$-[[action]]. Under the canonical embedding into $\mathbf{H}$ the corresponding [[action groupoid]] is a 0-truncated object 

$$
  \left(
  \array{
    X \sslash G
    \\
    \downarrow
    \\
    \mathbf{B}G
  }
  \right)
  \;\in\;
  Smooth\infty Groupoids_{/\mathbf{B}G}
$$

as in Example \ref{GlobalHomotopyQuotientOrbifold}, and hence its $Singularities$-[[codiscrete object|codiscrete]] image is a [[orbifold]] in the sense of Def. \ref{Orbifold}:

$$
  \mathcal{X}
  \;\coloneqq\;
  \left(
  \array{
    coDisc_{sing}\big(X \sslash G \big)
    \\
    \downarrow
    \\
    \mathbb{B}G
  }
  \right)
  \;\in\;
  \left( 
    Smooth\infty Groupoids_{sing}
  \right)_{/\mathbb{B}G}
  \,.
$$

We claim that the [[shape modality|shape]] of this orbifold in plain [[global equivariant homotopy theory]] coincides with the global equivariant homotopy type associated with the [[G-space]] underlying $X$

$$
  &#643; coDisc_{sing}\left( 
   X \sslash G
  \right)
  \;\simeq\;
  \Delta_G\big( X \big)
  \;\in\;
  Sh_\infty\big( 
    Singularities, \infty Groupoids
  \big)
  \,,
$$

where on the right $\Delta_G$ is as in [Rezk 14, 3.2](#Rezk14)

=--

+-- {: .proof}
###### Proof

The key point is that the assumption of 0-truncation of $\mathcal{X}$ and the restriction to [[finite groups|finite]] (hence [[discrete groups|discrete]]) groups ensures that $coDisc_{sing}$ forms the correct [[fixed point]] [[sheaves]], whose separate [[shape modality|shape]]/[[geometric realization]] then coincides with the relevant fixed point spaces of $X$.

In detail, as $\infty$-groupoid-valued presheaves on the product site [[CartSp]] $\times Singularities$ we have

$$
  \begin{aligned}
    coDisc_{sing}\big( X\sslash G\big)
    \;\colon\;
    \mathbb{R}^n \times \mathbb{B}K
    & \mapsto\;
    \infty Groupoids\big(
      \mathbf{B}K,
      \underset{
        \in 1Groupoid
      }{
        \underbrace{  
          \underset{\in Set}{
            \underbrace{C^\infty(\mathbb{R}^n, X)}
          } 
        }
      }
      \sslash G
    \big)  
    \\
    & \simeq \;
    \underset{
      \simeq Grpd(Set)
    }{
    \underbrace{
      1 Groupoids
     }
     }
     \big(
      \mathbf{B}K, 
      C^\infty(\mathbb{R}^n, X) \sslash G
    \big)
    \\
    & \simeq \;
    \underset{\phi \in Groups(K,G)}{\bigsqcup} 
      C^\infty(\mathbb{R}^n, X^{\phi(K)}) \sslash G
  \end{aligned}
$$

where in the first step we used the [[adjunction]] $(\Gamma_{sing} \dashv coDisc_{sing})$ as in Prop. \ref{SingularitiesAsCoDisc}. Hence as smooth $\infty$-groupoid valued presheaves on just $Singularities$ this is

$$
  \Big(
  coDisc_{sing}\big( 
    X \sslash G
  \big)
  \;\colon\;
  \mathbb{B}K
  \;\mapsto\;
    \underset{\phi \in Groups(K,G)}{\bigsqcup} 
    X^{\phi(K)} \sslash G  
  \Big)
  \;\in\;
  Sh_\infty\big( Singularities, Smooth\infty Groupoids \big)
  \,.
$$

Now [[shape modality|shape]] &#643; is [[left adjoint]], hence preserves the [[coproducts]] and the [[homotopy quotient]] by $G$ and finally also $G$ itself ($G$ being [[discrete group|discrete]], and &#643; preserving the point (the [[terminal object]]), by [[cohesion]]), so that in conclusion

$$
  \Big(
  &#643;
  coDisc_{sing}\big( 
    X \sslash G
  \big)
  \;\colon\;
  \mathbb{B}K
  \;\mapsto\;
    \underset{\phi \in Groups(K,G)}{\bigsqcup} 
     &#643; \left(X^{\phi(K)}\right) \sslash G  
  \Big)
  \;\in\;
  Sh_\infty\big( Singularities, \infty Groupoids \big)
  \,.
$$

But this is exactly the formula for $\Delta_G (X)$, as in [Rezk 14, 3.2](#Rezk14).

=--


+-- {: .num_prop #OrbifoldsInEquivariantHomotopyTheory}
###### Proposition
**([[orbifolds]] are in [[cohesion|cohesive]] [[equivariant homotopy theory]])**

An [[orbifold]] $\mathcal{X}$ with isotropy groups in $G$, according to Def. \ref{Orbifold} is $Singularities$-faithful over $\mathbb{B}G$ (Def. \ref{SingularitiesFaithful}) and hence inside the inclusion (from Prop. \ref{SingularitiesFaithfulSliceOverNormalSubgroupClassifier}) of the $G$-[[equivariant homotopy theory]] of $\mathbf{H}$ (Def. \ref{GEquivariantHomotopyTheoryOfCohesiveInfinityTopos}) into the [[globally equivariant homotopy theory]] of $\mathbf{H}$:

$$
  \mathcal{X}
  \;\in\;
  \mathbf{H}_G
  \;\hookrightarrow\;
  \left(
    \mathbf{H}_{sing}
  \right)_{/\mathbb{B}G}
$$

=--

+-- {: .proof}
###### Proof

By Prop. \ref{SingularitiesFaithfulSliceOverNormalSubgroupClassifier} we need to check that $\mathcal{X} \to \mathbb{B}G$ is $Singularities$-faithful.

Now, by the first defining assumption on $\mathcal{X}$ (Def. \ref{Orbifold}) and by Lemma \ref{GammaPreservesnTruncatedMorphisms}, we have that $\Gamma_{sing}(\mathcal{X} \to \mathbb{B}G)$ is [[n-truncated object in an (infinity,1)-category|0-truncated]]. By [[cohesion]] (eq:SingularitiesAdjointQuadruple) we have $coDisc_{sing} \circ \Gamma_{sing} \;\simeq\; Id$ and hence  $\mathcal{X} \to \mathbb{B}G$ is the image under $coDisc_{sing}$ of a 0-truncated morphism.
With this the statement follows by Prop. \ref{coDiscSingOf0TruncatedMorphismsIsSingularitiesFaithful}.

=--

+-- {: .num_remark #OrbifoldsInGloballyEquivariantStillEquivalentToGeometricGroupoids}
###### Remark
**([[orbifolds]] inside [[globally equivariant homotopy theory]] are still [[equivalence of (infinity,1)-categories|equivalent]] to [[cohesive (infinity,1)-topos|cohesive groupoids]])**

Since $coDisc_{sing} \;\colon\; \mathbf{H} \hookrightarrow \mathbf{H}_{sing}$ is a [[full sub-(∞,1)-category]]-inclusion, the [[(2,1)-category]] of $V$-[[orbifolds]] inside $\mathbf{H}_{sing}$ according to Def. \ref{Orbifold} is equivalent to its pre-image in $\mathbf{H}$, hence will coincide, for suitable choices of $\mathbf{H}$ and $V \in Grp(\mathbf{H})$, with traditional definition of [[(2,1)-categories]] of orbifolds regarded as certain [[geometric stacks|geometric groupoids]]. But by embedding this into the larger [[global homotopy theory]] $\mathbf{H}_{sing}$ of $\mathbf{H}$ more general [[coefficient]]-objects for orbifold cohomology become available, and this brings in the previously missing [[Bredon cohomology|Bredon]]-[[equivariant cohomology]]-aspect of orbifold cohomology.

=--


$\,$

### Orbifold cohomology

With [[orbifolds]] properly realized in [[cohesion|cohesive]] [[globally equivariant homotopy theory]] by the [above](#OnOrbifolds), the proper definition of _orbifold cohomology_ is now immediate, by the general logic of [[cohomology]] in [[(∞,1)-toposes]], this is Def. \ref{OrbifoldCohomology} below.

What needs checking is that this definition, in the special case that the [[coefficient]] object is [[geometrically discrete infinity-groupoid|geometrically discrete]] reproduces [[Bredon cohomology|Bredon]] [[equivariant cohomology]] of the underlying bare [[homotopy type]] of the orbifold. But this follows readily with the general considerations above, this is Example \ref{OrbifoldCohomologyWithGeometricallyDiscreteCoefficients} below.

$\,$

+-- {: .num_defn #OrbifoldCohomology}
###### Definition
**(orbifold cohomology)**

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] and write $\mathbf{H}_{sing}$ for its [[globally equivariant homotopy theory]] as in Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory}.

Let $G$ be a [[finite group]] and consider an [[orbifold]] with [[isotropy groups]]/[[singularities]] in $G$, according to Def. \ref{Orbifold}:

$$
  \mathcal{X} \;\in\; \left( \mathbf{H}_{sing} \right)
  \,.
$$

Then for 

$$
  \mathcal{A} \;\in\; \left( \mathbf{H}_{sing} \right)
$$

any other object (*not* necessarily itself an orbifold, and typically far from being so) the _orbifold cohomology_ of $\mathcal{X}$ with [[coefficients]] in $\mathcal{A}$ is the [[cohomology]] as given by the ambient [[(∞,1)-topos]], hence

$$
  H\big(
    \mathcal{X},
    \mathcal{A}
  \big)
  \;\coloneqq\;
  \left(
    \mathbf{H}_{sing}
  \right)_{/\mathbb{B}G}
  \big( \mathcal{X}, \mathcal{A}\big)
  \,.
$$

=--

We check the two desiderata for a good definition of orbifold cohomology discussed [above](#Idea):

1. It is clear that on objects in the inclusion $Disc_{sing} \;\colon\; \mathbf{H} \hookrightarrow \mathbf{H}_{sing}$ orbifold cohomology reduces to geometric cohomology on $\mathbf{H}$.

1. In the other extreme, for orbifold cohomology with geometrically discrete coefficients, we check that we re-obtain [[Bredon cohomology|Bredon]] [[equivariant cohomology]] of the underlying [[G-spaces]]:

+-- {: .num_example #OrbifoldCohomologyWithGeometricallyDiscreteCoefficients}
###### Example
**([[orbifold cohomology]] with [[geometrically discrete infinity-groupoid|geometrically discrete]] [[coefficients]] is $G$-[[equivariant cohomology]])**

Let $\mathbf{H} = $ [[Smooth∞Groupoids]] and consider a [[smooth manifold]] $X$ equipped with smooth [[action]] by a [[finite group]] $G$, regarded as an [[orbifold]] as in Example \ref{GlobalHomotopyQuotientsOfSmoothManifolds}: 
$$
  \mathcal{X}
  \;\coloneqq\;
  \left(
  \array{
    coDisc_{sing}\big( X \sslash G \big)
    \\
    \downarrow
    \\
    \mathbb{B}G
  }
  \right)
  \;\in\;
  \Big( 
    Smooth \infty Groupoids_{sing}
  \Big)_{/\mathbb{B}G}
  \,.
$$


Let moreover

$$
  \mathcal{A}
  \;\in\;
  \Big( 
    \infty Groupoids
  \Big)_{G}
  \overset{Disc}{\hookrightarrow}
  \Big( 
    Smooth \infty Groupoids
  \Big)_{G}
  \hookrightarrow
  \Big( 
    Smooth \infty Groupoids_{sing}
  \Big)_{/\mathbb{B}G}
$$

be any [[geometrically discrete infinity-groupoid|geometrically discrete]] [[coefficient]] object in $G$-[[equivariant homotopy theory]], included into the [[slice (infinity,1)-topos|slice]] of the [[global equivariant homotopy theory]] via Prop. \ref{GorbitCategory}.

Then the [[orbifold cohomology]] of $\mathcal{X}$ with [[coefficients]] in $\mathcal{A}$, according to Def. \ref{OrbifoldCohomology}, coincides with the [[Bredon cohomology|Bredon]] $G$-[[equivariant cohomology]] of the [[G-space]] underlying $X$:

$$
  H\big(
   \mathcal{X}, Disc(\mathcal{A})
  \big)
  \;\simeq\;
  H_G\big( 
    X, \mathcal{A}
  \big)
  \,.
$$

=--

+-- {: .proof}
###### Proof

We compute

$$  
  \begin{aligned}
    \left(Smooth \infty Groupoids_{sing}\right)_{/\mathbb{B}G}
    \left(
      \mathcal{X}, Disc(\mathcal{A})
    \right)
    & \simeq
    Smooth \infty Groupoids_G
    \left(
      \mathcal{X}, Disc(\mathcal{A})
    \right)    
    \\
    & \simeq
    \infty Groupoids_G
    \left(
      &#643;_{sing}\mathcal{X}, \mathcal{A}
    \right)    
  \end{aligned}
$$

where the first step is by Prop. \ref{OrbifoldsInEquivariantHomotopyTheory}, while the second is by the [[cohesion]] [[adjunction]] $&#643; \dashv Disc$ for [[Smooth∞Groupoids]]. By Example \ref{GlobalHomotopyQuotientsOfSmoothManifolds} we have that $&#643; \mathcal{X} \in \infty Groupoids_G$ is indeed the [[G-space]] $X$ regarded in $G$-[[equivariant homotopy theory]].
 
=--


## Related concepts

* [[orbifold]]

* [[Gromov-Witten theory]]

* [[orbifold K-theory]], [[equivariant K-theory]]

* [[twisted ad-equivariant Tate K-theory]]

* [[equivariant elliptic cohomology]]

History

According to [Abramovich 05, p. 42](#Abramovich05):

> On December 7, 1995 [[Maxim Kontsevich]] delivered a history-making lecture at Orsay, titled _String Cohomology_. This is what is now know, after [Chen-Ruan 00](#ChenRuan00), as _orbifold cohomology_, Kontsevich's lecture notes described the orbifold and  [[quantum cohomology]] of a global quotient [[orbifold]]. Twisted sectors, the age grading, and a version of orbifold stable maps for global quotients are all there.

The same lecture also introduced _[[motivic integration]]_.

## References


[[!include traditional orbifold cohomology -- references]]



### Proper orbifold cohomology
 
Discussion of orbifold cohomology in the context of [[Bredon cohomology]]:

* {#PronkScull07} [[Dorette Pronk]], [[Laura Scull]], _Translation Groupoids and Orbifold Bredon Cohomology_, Canad. J. Math. 62(2010), 614-645 ([arXiv:0705.3249](https://arxiv.org/abs/0705.3249), [doi:10.4153/CJM-2010-024-1](https://doi.org/10.4153/CJM-2010-024-1))

The suggestion to regard orbifold cohomology in [[global equivariant homotopy theory]]:

* {#Schwede17} [[Stefan Schwede]], Introduction of: _Orbispaces, orthogonal spaces, and the universal compact Lie group_, Mathematische Zeitschrift 294 (2020), 71-107 ([arXiv:1711.06019](https://arxiv.org/abs/1711.06019))

* {#Schwede18} [[Stefan Schwede]], p. ix-x of: _[[Global homotopy theory]]_, New Mathematical Monographs, 34 Cambridge University Press, 2018 ([arXiv:1802.09382](https://arxiv.org/abs/1802.09382))

Spelling out this suggestion of [Schwede 17, Intro](#Schwede17), [Schwede 1, p. ix-x8](#Schwede18):

* {#Juran20} [[Branko Juran]], _Orbifolds, Orbispaces and Global Homotopy Theory_ ([arXiv:2006.12374](https://arxiv.org/abs/2006.12374))

Based on results of or related to:

* {#HenriquesGepner07} [[André Henriques]], [[David Gepner]], _Homotopy Theory of Orbispaces_ ([arXiv:math/0701916](http://arxiv.org/abs/math/0701916))

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_, 2014

The above text follows:

* {#SatiSchreiber20} [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Proper Orbifold Cohomology]]_ ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))






[[!redirects orbifold cohomologies]]

[[!redirects orbifold cohomology group]]
[[!redirects orbifold cohomology groups]]

[[!redirects orbispace cohomology]]
[[!redirects orbispace cohomologies]]

[[!redirects orbispace cohomology group]]
[[!redirects orbispace cohomology groups]]

