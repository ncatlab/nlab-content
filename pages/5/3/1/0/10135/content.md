
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



#Contents#
* table of contents
{:toc}


## Idea

Since the crucial extra [[structures]] carried by an [[orbifold]] are

1. geometric structure (e.g. [[topology|topological]], [[algebraic geometry|algebro-geometric]], [[differential geometry|differential-geometric]], [[supergeometry|super-geometric]], etc.)

1. [[singularities]]

the [[cohomology]] of orbifolds should be such as to provide [[invariants]] which are sensitive not just to the underlying plain [[homotopy type]] of an orbifold (its [[shape modality|shape]]) but also to this extra structure. This means that _orbifold cohomology_ should, respectively, unify

1. geometric cohomology (e.g. [[sheaf cohomology|sheaf]] [[hypercohomology]], [[differential cohomology]], etc.)

1. [[equivariant cohomology]] in its fine form of [[Bredon cohomology]]
 
in the sense that [[differential cohomology|geometric cohomology]] is recovered away from the orbifold [[singularities]] and [[equivariant cohomology]] is recovered right at the [[singularities]], while globally orbifold cohomology provides a unification of these two aspects.

Since any concept of [[cohomology]] (as discussed there) is effectively equivalent to the choice of ambient [[(∞,1)-topos]], the question of defining orbifold cohomology is closely related to the question of how exactly to define the [[(∞,1)-category]] of orbifolds (usually a [[(2,1)-category]]) in the first place. This question is notoriously more subtle than the simple intuitive idea of orbifolds might suggest, as witnessed by the convoluted history of the concept (see e.g. [Lerman 08, Introduction](orbifold#Lerman08)).

$\,$

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
  \mathbf{H}_{/\mathbf{G}}
$$

in the [[slice (∞,1)-topos]] over the [[delooping]] $\mathbf{B}G = \ast \sslash G$ of $G$, which is still a [[0-truncated object]], reflecting that as a [[functor]] of [[groupoids]] the morphism $\mathcal{X} \to \mathbf{B}G$ is a [[faithful functor]].

Accordingly, if this is to be the formalization of the nature of the [[orbifold]] $\mathcal{X}$, then its corresponding orbifold cohomology has [[coefficients]] given by objects $\mathcal{A} \in \mathbf{H}_{/\mathbf{B}G}$ and cohomology sets being the [[connected components]] of the [[(∞,1)-categorical hom-spaces]]

$$
  H_{\mathbf{B}G}\big( \mathcal{X}, \mathcal{A}\big)
  \;\coloneqq\;
  \pi_0 \mathbf{H}_{/\mathbf{B}G}\big( \mathcal{X}, \mathcal{A}\big)
  \,.
$$

This concept of orbifold cohomology does fully reflect the geometric nature of orbifolds. It also reflects _some_ equivariance aspect. For example if $\mathcal{X} = \ast \sslash G$ is the one-point orbifold with singularity given by a finite group $G$, and if $V \in G Representations$ is a [[linear representation]], with $K(V,n)\sslash G \in \infty Groupoids \overset{Disc}{\hookrightarrow}$ its [[Eilenberg-MacLane space]], then 

$$
  H_{\mathbf{B}G}\big( 
    \mathbf{B}G, K(V,n)\sslash G
  \big)
  \;\simeq\;
  H^n_{grp}(G,V)
$$

is the [[group cohomology]] of $G$ with [[coefficients]] in $V$.

However, this definition does _not_ reflect [[Bredon cohomology|Bredon]]-[[equivariant cohomology]] around the orbifold singularities. Instead, it really given (geometric/stacky refinement) of _[[cohomology with local fcoefficients]]_.


$\,$

### Lift of orbifolds to geometric global homotopy theory

Hence the proposal of [Moerdijk-Pronk 97](orbifold#MoerdijkPronk97) that an [[orbifold]] should be regarded as a certain [[geometric stack]] is missing something. It was briefly suggested in [Schwede 17, Introduction](#Schwede17), [Schwede 18, p. ix-x](#Schwede18) that the missing aspect is provided by [[global equivariant homotopy theory]], but details seem to have been left open. 

Here we discuss how to define the required orbifold cohomology in detail and in general. We combine the [[differential cohesion]] for the geometric aspect with the cohesion of [[global equivariant homotopy theory]] that was observed and highlighted in [Rezk 14](#Rezk14).

The following may serve as intuition for the issue with the nature of orbifolds:

Envision the picture of an orbifold singularity and hold a mathemagical magnifying glass over the singular point. Inside the magnifying we you see resolved the singular point as a fuzzy fattened point, to be called $\mathbb{B}G$.

Removing the magnifying glass, what one sees with the bare eye depends on how one squints:

1. The physicist says that what he sees is a singular point, but a point after all. This is the plain [[quotient]]  $\ast = \ast / G$. 

1. The Lie geometer says that what he sees is a point transforming under the $G$-[[action]] that fixes it, hence [[homotopy quotient]] [[groupoid]] $\mathbf{B}G =\ast \sslash G$.

These two aspects are two [[adjoint modality|opposite extreme aspects]] of the orbifold singularity $\mathbb{B}G$, but the orbifold singularity is more than both of these aspects. The real nature of an orbifold singularity is really a point, not a big [[classifying space]] $B G$ (recall that already $\mathbf{B}\mathbb{Z}_2$ = \mathbb{R}P^\infty), but it also does remember the group [[action]], for that characterizes how the singularity is being singular.

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


### Globally equivariant cohesive toposes

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

to distinguish them from their image as [[delooping]] groupoids $B G \in $ [[∞Grpd]]. (As we consider [[(∞,1)-presheaves]] on $Singularities$ with values in [[∞Groupoids]], in Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory} below, these two objects become crucially different, albeit closely related.)

=--

+-- {: .num_remark}
###### Remark

The category $Singularities$ in Def. \ref{CategoryOfSingularities} is called

* "$Orb$ version 1" in [Henriques-Gepner 07](orbispace#HenriquesGepner07)

* "$Glob$" in [Rezk 14, 2.2](#Rezk14)

* "$Orb$" in [Körschgen 16](orbispace#Koerschgen16), [Schwede 17](orbispace#Schwede17), [Schwede 18](global+equivariant+homotopy+theory#Schwede18).

=--

+-- {: .num_prop #CohesionOfGlobalEquivariantHomotopyTheory}
###### Proposition
**([[global equivariant homotopy theory]] [[cohesive (∞,1)-topos|cohesive]] over [[base (∞,1)-topos]])**

Let $\mathbf{H}$ be any [[(∞,1)-topos]] and consider the [[(∞,1)-category of (∞,1)-presheaves]] on the category of singularities (Def. \ref{CategoryOfSingularities}) over the [[base (∞,1)-topos]] \mathbf{H}, hence the [[(∞,1)-functor (∞,1)-category]]

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
  Sh_\infty\left( Singularities, \infty \mathbf{H}\right)
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
         \simeq \mathbf{B}G
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
       B K, BG
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

By the [[(n-connected, n-truncated) factorization system]], a [[1-morphism]] in an [[(∞,1)-topos]] is [[n-truncated object in an (infinity,1)-category|0-truncated]] precisely if it has the [[right lifting property]] again every morphism that is [[n-connected object of an (infinity,1)-topos|0-connected]].

+-- {: .num_example}
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

$$
  \array{
     B G'
     \\
     \downarrow^{\mathrlap{B p}}
     \\
     B G
  }
$$

is 0-connected precisely if the corresponding [[group homomorphism]] $p \colon G' \to G$ is [[surjective function|surjective]].

=--

Therefore one might say "[[faithful morphism]]" for every [[n-truncated object in an (infinity,1)-category|0-truncated]] morphism in an [[(∞,1)-topos]]. But the terminology "faithful" is used with other meanings, too, and we need to refer to these variants

+-- {: .num_defn #SingularitiesFaithful}
###### Definition
**($Singularities$-faithful morphisms)**

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] with $\mathbf{H}_{sing} \coloneqq Sh_\infty\left( Singularities, \mathbf{H}\right)$ its [[globally equivariant homotopy theory]] according to Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory}. We say that a morphism
$\mathcal{X} \overset{f}{\to} \mathcal{Y}$ in $\mathbf{H}_{sing}$ is _$Singularities$-faithful_ if its has the [[right lifting property]] against morphisms of the form

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

For the case $\math{H} =$ [[∞Groupoids]] this is the definition of _faithful maps_ in [Rezk 14. Prop. 3.4.1](#Rezk14).

> It seems that the morphisms (eq:Singularities0Connected) are not 0-connected in $Sh_\infty(Singularities, \infty Groupoids)$. Them being 0-connected should come down to the statement that for $p \colon G' \to G$ a surjective group homomorphism and $H \subset G$ any subgroup, there always is a lift of $H$ to $G'$ and that any two such lifts are conjugate to each other, in $G'$. But already the first condition fails in general, since not every epimorphism of groups is a split epimorphism.

> Nevertheless and in any case we have the following, which is all we will need:

+-- {: .num_example}
###### Example

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] with $\mathbf{H}_{sing}$ its [[globally equivariant homotopy theory]] according to Prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory}. 

If a morphism $X \overset{f}{\to} Y$ in $\mathbf{H}$ is [[n-truncated object in an (infinity,1)-category|0-truncated]], then its image under $coDisc_{sing} \;\colon\; \mathbf{H} \hookrightarrow \mathbf{H}_{sing}$ is $Singularities$-faithful (Def. \ref{SingularitiesFaithful}).

This follows directly by the adjunctions (eq:SingularitiesAdjointQuadruple), the relations (eq:ShapeOfOrbifoldSingularity) and the fact spring


=--



### Orbifolds

+-- {: .num_defn #Orbifold}
###### Definition
**([[orbifold]]**, improved definition)

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

If $\mathbf{H}$ is moreover [[differential cohesion|differentially cohesive]] and $V \in Grp(\mathbf{H})$ is a [[∞-group|group object]], then an orbifold $\mathcal{X}$ is called a _$V$-orbifold_ if is underlying [[geometric stack|geometric groupoid]] $\flat_{sing}\left( \mathcal{X}\right)$ (eq:OrbifoldUnderlyingGroupoid) is a [[V-manifold]].

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




## Related concepts

* [[orbifold]]

* [[Gromov-Witten theory]]


History

According to [Abramovich 05, p. 42](#Abramovich05):

> On December 7, 1995 [[Maxim Kontsevich]] delivered a history-making lecture at Orsay, titled _String Cohomology_. This is what is now know, after [Chen-Ruan 00](#ChenRuan00), as _orbifold cohomology_, Kontsevich's lecture notes described the orbifold and  [[quantum cohomology]] of a global quotient [[orbifold]]. Twisted sectors, the age grading, and a version of orbifold stable maps for global quotients are all there.

The same lecture also introduced _[[motivic integration]]_.

## References
 
Discussion of orbifold cohomology in the context of [[Bredon cohomology|Bredon]]/[[global equivariant homotopy theory|global]] [[equivariant cohomology]] includes

* {#PronkScull07} [[Dorette Pronk]], [[Laura Scull]], _Translation Groupoids and Orbifold Bredon Cohomology_, Canad. J. Math. 62(2010), 614-645 ([arXiv:0705.3249](https://arxiv.org/abs/0705.3249), [doi:10.4153/CJM-2010-024-1](https://doi.org/10.4153/CJM-2010-024-1))


* {#Schwede17} [[Stefan Schwede]], _Orbispaces, orthogonal spaces, and the universal compact Lie group_ ([arXiv:1711.06019](https://arxiv.org/abs/1711.06019))

* {#Schwede18} [[Stefan Schwede]], _[[Global homotopy theory]]_, New Mathematical Monographs, 34 Cambridge University Press, 2018 ([arXiv:1802.09382](https://arxiv.org/abs/1802.09382))

related to results of

* {#HenriquesGepner07} [[André Henriques]], [[David Gepner]], _Homotopy Theory of Orbispaces_ ([arXiv:math/0701916](http://arxiv.org/abs/math/0701916))

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_, 2014



See also

* {#ChenRuan00} Weimin Chen, [[Yongbin Ruan]], _A New Cohomology Theory for Orbifold_, Commun. Math. Phys. 248 (2004) 1-31 ([arXiv:math/0004129](http://arxiv.org/abs/math/0004129))
 
* {#Abramovich05} [[Dan Abramovich]], _Lectures on Gromov-Witten invariants of orbifolds_ ([arXiv:math/0512372](http://arxiv.org/abs/math/0512372))


[[!redirects orbifold cohomologies]]

[[!redirects orbifold cohomology group]]
[[!redirects orbifold cohomology groups]]

[[!redirects orbispace cohomology]]
[[!redirects orbispace cohomologies]]

[[!redirects orbispace cohomology group]]
[[!redirects orbispace cohomology groups]]

