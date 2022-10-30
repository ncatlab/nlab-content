

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Variational calculus
+--{: .hide}
[[!include variational calculus - contents]]
=--
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _extended Lagrangian_ is the notion of [[Lagrangian]] refined to [[extended quantum field theory]] (or "localized" or "multi-tiered" quantum field theory). At the same time is is the [[prequantum n-bundle]] of the theory in its [[higher geometric quantization]] in top codimension, hence over the point.

## Motivation and Survey
 {#MotivationAndSurvey}


1. [Ingredients of fundamental physics](#IngredientsOfFundamentalPhysics)

1. [Topological local Lagrangian gauge field theory](#TopologicalLocalLagrangianGaugeFieldTheory)

1. [Chern-Simons field theory as a toy example](#ChernSimonsTheoryAsAToyExample)

1. [Topological local field theory in higher category theory](#TopologicalLocalFieldTheoryInHigherGeometry)

1. [Intermezzo: Elements of higher cohesive geometry](#IntermezzoElementsOfHigherCohesiveGeometry)

1. [Chern-Simons theory as the archetypical example](#CSAsArchetypicalExample)

1. [Topological local Lagrangian field theory in higher geometry](#TopologcalLocalLagrangianFieldTheoryInHigherGeometry)

1. [7-dimensional Chern-Simons theory as the next example](#7dCSTheoryAsExample)

1. [∞-Chern-Simons theory as the general example](#InfinityChern-SimonsTheoryAsTheGeneralExample)

### Ingredients of fundamental physics
 {#IngredientsOfFundamentalPhysics}

Ever since [[Issac Newton]], [[theories of physics]] are formulated in the language of [[mathematics]]. Modern physics is formulated in terms of modern mathematics in the most intimate way.
We aim to give here a account at least of central parts of modern physics naturally formulated in the mathematics of _[[higher geometry]]_ that we discussed in _[geometry of physics - Geometry](geomery+of+physics#GEOMETRY)_. 

The physics that we are concerned with is _fundamental_ physics,
that part of the large subject of physics which is concerned with elementary  processes and phenomena of physics from which all others are thoght to _emerge_ as approximations to collective effects of complex configurations of the elementary 
entities.

The best [[theory (physics)|theory]] of fundamental physics as presently understood is known as _[[Einstein-Yang-Mills-Dirac-Higgs theory]]_. 
While fundamental, this theory has _free parameters_. These index different flavors of the same general mechanism. Notably the species and the masses of the fundamental [[fermion]] [[particles]] are such parameters, as 
is their coupling to the [[force fields]].

Specifying these parameters is called constructing a 
_[[model (in theoretical physics)|model]]_ in physics  and specifically a [[phenomenology|phenomenological model]] of fundamental physics, 
if aimed at making the observations that are predicted by the theory to closely match those that are being made in experiments. The global choice of these parameters that make the predictions  match all available data to the currently best possible degree is called the _standard model_, specifically the  _[[standard model of particle physics]]_ for the sector in which the large-scale description of the 
force of [[gravity]] is approximately negligible, and the 
_[[standard model of cosmology]]_
which focuses on that large scale structure.

The following table list some key ingredients of the standard theory of fundamental physics, all of which we discuss in detail further below.

[[!include standard model of fundamental physics - table]]

### Topological local Lagrangian gauge field theory
 {#TopologicalLocalLagrangianGaugeFieldTheory}

While the [[standard model of fundamental physics - table|standard model of fundamental physics]] is a specification of the general  framework of [[Einstein-Yang-Mills-Dirac-Higgs theory]], that theory itself is a particular realization of several deep general principles  of theoretical physics: it is 

1. a **[[field (physics)|field]]** theory;
1. a **[[gauge theory|gauge]]** theory;
1. a **[[Lagrangian]]** theory;
1. a **[[local quantum field theory|local]]** theory;
1. a **[[topological field theory|topological]] theory.

We briefly indicate what this means, a formal discussion of these notions will be given in the  main part below.

* A **[[field (physics)|field]]** theory identifies the basic configurations of a physical system with generalized functions on spacetime, such as [[tensor fields]], and more generally with [[sections]] $\phi$ of some [[fiber bundle]] over spacetime

  $$
    \array{ 
      && E 
      \\
      & {}^{\mathllap{\phi}}{\nearrow} & \downarrow^{\mathrlap{field\;bundle}}   
      \\
      X &\stackrel{id}{\to}& X
     }
   $$

* A **[[gauge theory|gauge]]** theory in the broad sense has not just a [[set]] or [[smooth space]] of field configurations but has a [[groupoid]] or [[stack]]/[[smooth groupoid]] of field configurations: there are equivalences between nominally different field configurations 

  $$
    \phi \stackrel{\simeq}{\to} \phi'
  $$

  called _[[gauge transformations]]_.

   A gauge theory in the original sense specifically has a groupoid of [[principal connections]] as its configurations. (Notice that gauge transformations are not in general just a redundancy of the description of the theory, but are genuine data: there are in general non-trivial gauge [[automorphisms]] of a field and the stack of gauge field configurations is not in general equivalent to a plain [[sheaf]].)

* A **[[Lagrangian]]** theory is one which is specified by a function on the space of all its configurations, called the (exponentiated) _[[action functional]]_ $\exp(i S)$. This function is assumed to be the [[integration of differential forms|integral]] of a [[differential form]] $L$ on [[spacetime]] that itself is a function of the field configurations and called the [[Lagrangian]] of the theory. 

  $$
    \exp(i S(\phi)) = \exp\left(i \int_X L\left(\phi\right)\left(x\right) \right) 
  $$

  The [[critical locus]]

  $$
    \left\{
	 \phi \in \mathbf{Fields}(\Sigma)		|
		d_{\mathrm{var}} S_\phi \simeq 0
	  \right\}
  $$

  of the action functional is called the _[[phase space]]_ of the theory, a point of this is said to be a solution to the _[[equations of motion]]_ of the theory.

* A **[[local quantum field theory|local]]** theory has a Lagrangian form which at each point of spacetime only depends on the values of the fields at that point, and of finitely many derivatives of the fields at that point.

  $$
    \exp(i S(\phi)) = \exp\left(i \int_X L\left(\phi\left(x\right), \nabla \phi\left(x\right)\right)\right) 
  $$

  This means that a _[[local Lagrangian]]_ is a horizontal form on the [[jet bundle]] of the field bundle of which the fields are sections.

* A **[[topological field theory|topological]]** theory finally is one where the field bundle is naturally associated to every smooth manifold, typically of some fixed dimension and possibly equipped with  topological [[G-structure]] such as an orientation, but not equipped with any further geometric structure: all geometric structure such as metrics on spacetime are themselves regarded as parts of the field content in a topological theory.


### Chern-Simons field theory as a toy example

Most of this was fairly well understood decades ago, by the 1960s. But even with all this conceptual understanding of the structure of fundamental physics available, there were and are a lot of implications of 
_[[topological field theory|topological]] [[local  Lagrangian]] [[gauge field theory]]_ which remained elusive.


In the 1980s attention turned to _other_ topological local Lagrangian gauge field theories than that governing the standard model: it turns out that there are many such  [[theories of physics]] that share crucial properties with the standard model but which  otherwise predict, if considered as phenomenological models, physics  radically different from that
which we actually observe experimentally. For instance there are respectable theories of fundamental 
pyhsics which describe physics in dimensions other than the three spatial and one time dimension which we clearly observe, theories that contain no force of gravity, others that contain only the force of gravity, theories that contain mirror partners of every species of matter or contain no matter at all, etc.

In short, it was gradually realized, and realized to be important, that, in the platonic world of mathematics and of theoretical physics, there is a whole space of field theories, in which the one underlying the standard model of observed physics is only one single point, even if regarded with its free parameters.

A crucial step forward happened when around 1989 [[Edward Witten]], in this vein,  introduced the study of what is now called _[[Chern-Simons theory]]_ a topological local Lagrangian gauge field theory which, as such, shares
some crucial principles with Einstein-Maxwell-Yang-Mills theory, while at the  same time being  radically different and most importantly: 
much simpler to analyze. 

The dimension of Chern-Simons theory is 3 instead of 4, but 
Chern-Simons theory has a [[gauge field]] just as [[Yang-Mills theory]] does. For $G$ a [[connected topological space|connected]] [[simply connected topological space|simply connected]] [[gauge group]], this is mathematically represented by a [[Lie algebra-valued differential 1-form]] $A$.

The [[Lagrangian]] of [[Chern-Simons theory]] is the [[Chern-Simons 3-form]]

$$
  L(A)
  \coloneqq
  \mathrm{CS}_3(A)
  \coloneqq
  \langle A \wedge F_A\rangle
  + 
  c
  \langle A \wedge [A \wedge A]\rangle
  \,,
$$

whence the name of the theory, and hence the Chern-Simons [[action functional]] is

$$
  \exp(i S(A)) 
  =
   \exp\left(
     2 \pi i \int_{\Sigma_X} \mathrm{CS}_3(A)
	\right)
$$


At the same time Chern-Simons theory is still being rich in phenomena, 
in fact so rich in phenomena that for instance it helped illuminate deep mathematical problems that had not otherwise been understood as much before (properties called _[[knot invariants]]_).


### Topological local field theory in higher category theory
 {#TopologicalLocalFieldTheoryInHigherGeometry}

Another pleasant effect of the introduction of the Chern-Simons "toy model"  for topological field theory was that, 
due to its conceptual simplicity, its basic structure could be appreciated also by mathematicians not trained in theoretical physics, who would otherwise fail to see through all the  physics jargon involved in the available discussion of realistic models. Accordingly, immediately after the realization of Chern-Simons field theory,  the first mathematically precise axiomatizations of an $n$-dimensional _[[topological field theory]]_ was proposed, by [[Michael Atiyah]]: "[[functorial quantum field theory]]"

This axiomatization demands in particular that to each [[closed manifold]] of [[dimension]] $(n-1)$ is assigned a [[vector space]]

$$
  Z 
   \;\colon\; 
  \Sigma_{n-1} \mapsto Z(\Sigma_{n-1}) \in \mathrm{Vect}
$$

thought of as the _[[space of physical states]]_ of the theory on the
spatial slice $\Sigma_{n-1}$ of spacetime. 

However, This original axiomatization did not capture the full _[[local quantum field theory|locality]]_ property: the spaces of states are assigned globally to a space $\Sigma_{n-1}$ and are not required to be obtainable by "integrating up local data" over $\Sigma_{n-1}$. 

In order to refine this, one needs an axiomatization of field theory that assigns data also to manifolds $\Sigma_{k}$ of [[dimension]] $0 \leq k \leq n$. This should be such that the data assigned to a torus $\Sigma_{k} \times S^1$ is the [[trace]] in a suitable sense, of the data assigned to $\Sigma_{k}$ itself. It turns out that the way to capture this is to think of $Z(\Sigma_k)$ as being a vector space in [[higher category theory]]/[[directed homotopy type theory]]: an [[n-vector space|(n-k)-vector space]].

$$
  \Sigma_k \mapsto Z(\Sigma_k) \in (n-k)\mathrm{Vect}
$$

That something like this should work was hypothetized by [[Dan Freed]] (in _[[Higher Algebraic Structures and Quantization]]_), the precise formulation was later given by [[Jacob Lurie]] (in _[[On the Classification of Topological Field Theories]]_). In the literature the resulting axiomatization is called _[[extended topological field theory]]_ (with "extended" referring to extending the axioms from [[codimension]] 1 to higher codimension) or _[[multi-tiered field theory]]_ (thinking of the data in higher [[codimension]] as being higher "tieres" of the theory). 

But in the [[physics]]-community, at least in the [[algebraic quantum field theory]]-community, there is also the well-established term of _[[local quantum field theory]]_ which refers broadly to what the axioms of "extended TQFT" capture. Hence we should think of this as formalizing _topological local field theory_.


### Topological local *Lagrangian* field theory in higher geometry
 {#TopologcalLocalLagrangianFieldTheoryInHigherGeometry}

The formalization of [[extended topological field theory]] thus captures the _[[local quantum field theory|local]]_ aspect of [[field (physics)|field]] [[theory (physics)|theory]]. But we saw [above](#TopologicalLocalLagrangianGaugeFieldTheory) that the theories of fundamental physics have one more crucial property: they are _[[Lagrangian]]_. Here we indicate how to formulate Lagrangian theories that are also local in the sense of [[extended field theory]].

The step of passing from a [[Lagrangian]] to the corresponding 
[[quantum field theory]] is called _[[quantization]]_. There are two broad approaches to formalization of what this means, called _[[deformation quantization|algebraic deformation quantization]]_ and _[[geometric quantization]]_.  The first of these deals explicitly with producing [[algebras of quantum observables]], while the second describes explicitly how to construct the [[spaces of states]] that we considered above. Both are at least roughly dual to each other, in the spirit of [[Isbell duality|the general duality]] between [[algebra]] and [[geometry]]. 
For the following discussion we follow the ideas of [[geometric quantization]], which naturally fit a discussion of _[[geometry of physics]]_.
The following table surveys some keywords in this context which we will discuss in detail further below.

[[!include Isbell duality - table]]


In its traditional formulation, one considers the [[symplectic form]] $\omega$ which is naturally induced by a [[local Lagrangian]] on its (reduced) [[covariant phase space]] and says that a _[[geometric prequantization]]_ of this form is the choice of a $U(1)$-[[principal connection]] $\nabla$ on the phase space whose [[curvature]] $F_\nabla$ is $\omega$, hence a lift in

$$
  \array{
    &&& \mathbf{B}U(1)_{conn}
    \\
    {{prequantum} \atop {circle\;bundle}} && {}^{\mathllap{\nabla}}\nearrow & \downarrow^{\mathrlap{F_{(-)}}} & curvature
    \\
    &PhaseSpace
    &\stackrel{\omega}{\to}&
    \Omega^2_{cl}
    \\
    &&
    sympl.\;form
  }
  \,.
$$

A [[section]] of the [[associated bundle|associated]] [[complex line bundle]]

$$
  \array{
    && P \times_{U(1)}\mathbb{C}
    \\
    & {}^{\mathllap{\Psi}}\nearrow & \downarrow
    \\
    X &\stackrel{id}{\to}& X
  }
$$

is called a _[[wave function]]_ on phase space. One is to choose a [[polarization]] of phase space, equipping it locally with "[[canonical coordinates]]" and "[[canonical momenta]]". Then a _[[quantum state]]_ in geometric quantization is a [[wave function]] $\Psi$ which only depends on the [[canonical coordinates]].


$$
  Z(\Sigma_{n-1}) 
  \coloneqq
  \{wave\; functions\;of\;canonical\;coordinates\}
  \coloneqq
  \left\{
    polarized\;sections\;of\;prequantum\;line\;bundle
  \right\}
  \,.
$$

From this it is clear that in order to refine this to local (extended, multi-tiered)  [[prequantum field theory]] we are to assign _[[circle n-bundle with connection|higher line bundles]]_ in higher codimension, namely a [[prequantum n-bundle|prequantum (n-k)-bundle]] in [[codimension]] $k$.

As a first indication that this makes good sense, notice that the natural assignment to a field in codimension 0, hence to a field configuration on [[spacetime]], is its [[action functional]]. Being a $U(1)$-valued function, this is naturally thought of as a 0-bundle, the _[[prequantum 0-bundle]]_.

So we are after a picture as indicated in the following table. 

| | | [[extended prequantum field theory|local/extended Lagrangian field theory]] |  | [[extended quantum field theory|local/extended quantum field theory]]  |
|--|--|--|--|--|
| closed piece of [[spacetime]] of [[dimension]] $0 \leq k \leq n$ |  [[prequantum field theory]] | [[prequantum n-bundle|prequantum (n-k)-bundle]] | [[geometric quantization]] | [[space of states|space of]] $(n-k)$-[[wave functions]] |
| [[closed manifold]] of [[dimension]] $0 \leq k \leq n$ | $\stackrel{local\;prequantum\;field\;theory}{\mapsto}$ | [[circle n-bundle with connection|circle (n-k)-bundle with connection]] on [[moduli stack]] of [[field (physics)|field configurations]] | $\stackrel{polarized\; sections}{\mapsto}$ | [[n-vector space|(n-k)-vector space of states]] | 
| $\Sigma_k$ | $\mapsto$ | $\exp(2 \pi i \int_{\Sigma_k}[\Sigma_k,\mathbf{L}]) : [\Sigma_k, \mathbf{Fields}] \to \mathbf{B}^{n-k} U(1)_{conn}$ | $\mapsto$ | $Z(\Sigma_{n-k})$ |


### Intermezzo: Recalling elements of higher cohesive geometry  
 {#IntermezzoElementsOfHigherCohesiveGeometry}

The idea of _[[extended prequantum field theory]]_ indicated [above](#TopologcalLocalLagrangianFieldTheoryInHigherGeometry)  is best illustrated by the example of [[Chern-Simons field theory]]. We talk about this in a moment [below](#CSAsArchetypicalExample), but since in order to do so we need now at least some basic notions from [[cohesion|cohesive]] [[higher geometry]], we briefly recall these first.

(...)

For $\mathcal{C}$ a [[site]] with [[point of a topos|enough points]] the [[(2,1)-category]] of [[(2,1)-sheaves]] ([[stacks]]) on $\mathcal{C}$ is the [[simplicial localization]]

$$
  Sh_{(2,1)}(\mathcal{C})
  \simeq
  L_{le} Func(\mathcal{C}^{op}, Grpd)
  \,.
$$

$L_{le}$: formally turn [[stalk]]-wise ("local") [[equivalence of groupoids|equivalence of groupoids]] into actual [[equivalences]].

(...)

$$
  \infty Grpd \simeq L_{whe} sSet \simeq L_{whe} Top
$$

$L_{w}$: formally turn [[weak homotopy equivalences]] into actual [[homotopy equivalences]].

(...)



$$
  \array{
    \mathbf{H} \coloneqq
    & Sh_\infty(\mathcal{C})
    &
    \stackrel{
      \overset{\infty-stackif.}{\leftarrow}
    }{
      \hookrightarrow
    }
  &
  PSh_\infty(\mathcal{C})
  \\
  & \uparrow^{\mathrlap{\simeq}} && \uparrow^{\mathrlap{\simeq}}
  \\
  & L_{lwhe} Func(\mathcal{C}^{op}, sSet)
  &
  \stackrel{
    \overset{\mathbb{L} id}{\leftarrow}
   }{
     \underset{\mathbb{R} id}{\rightarrow}
  }&
  L_{whe} Func(\mathcal{C}^{op}, sSet)
  }
$$


$L_{lwhe}$: universally turn [[stalk]]-wise ("local") [[weak homotopy equivalences]] into actual [[homotopy equivalences]]

(...)

[[cohesion]]

$\mathcal{C}$ an [[infinity-cohesive site]] 

$$
  \array{
   \mathbf{H}
    &
   \stackrel{\overset{\Pi}{\to}}{\stackrel{}{\stackrel{\overset{coDisc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{coDisc}{\leftarrow}}}}} 
   &
  \infty Grpd
  \\
  \uparrow^{\mathrlap{\simeq}}
  &&
  \uparrow^{\mathrlap{\simeq}}
  \\
  L_{lwhe} Func(\mathcal{C}^{op}, sSet)
  &\stackrel{\overset{hocolim_{\mathcal{C}}}{\to}}{\stackrel{\overset{const}{\leftarrow}}{\stackrel{X \mapsto X(*)}{\stackrel{\overset{}{\to}}{\underset{}{\leftarrow}}}}}&
  L_{whe} sSet
  }
$$

(...)

the [[adjoint quadruple]] of [[(∞,1)-functors]] induces an [[adjoint triple]] of [[comonad|co]][[(∞,1)-monads]]:

| [[shape modality]] | $\dashv$ | [[flat modality]] | $\dashv$ |[[sharp modality]] |
|--|--|--|--|--|
| $\mathbf{\Pi} \coloneqq Disc \circ \Pi$ | | $flat \coloneqq Disc \circ \Gamma$ |   | $\sharp \coloneqq coDisc \circ \Gamma$  |

for $G \in Grp(\mathbf{H})$ we have a [[pasting diagram]] of [[(∞,1)-pullbacks]]

$$
  \array{
    G &\to& * 
    \\
    \downarrow^{\mathrlap{\theta_G}} && \downarrow
    \\
    \flat_{dR} \mathbf{B}G
    &\to&
    \flat \mathbf{B}G
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}G
  }
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \array{
    \infty-group &\to& *
    \\
    {}^{\mathllap{MC\;form}}\downarrow && \downarrow
    \\
    deRham\, coefficients &\to& flat\;coefficients
    \\
    \downarrow && \downarrow
    \\
    * &\to& principal\,coefficients
  }
$$

for $\mathbb{G}$ a [[braided ∞-group]] set 

$$
  curv_{\mathbb{G}}
  \;\colon\;
  \mathbf{B}\mathbb{G}
  \stackrel{\theta_{\mathbf{B}\mathbb{G}}}{\to}
  \flat_{dR}\mathbf{B}^2 \mathbb{G}
$$

then $\mathbb{G}$-[[differential cohomology]] is $curv_{\mathbf{B}\mathbb{G}}$-[[twisted cohomology]]

In particular, if we consider globally defined curvature forms

$$
  \Omega_{cl}(-,\mathbb{G}) \to \flat_{dR}\mathbf{B}^2\mathbb{G}
$$

then the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{B}\mathbb{G}_{conn}
    &\to&
    \Omega(-,\mathbb{G})
    \\
    \downarrow && \downarrow^{\mathrlap{F_{(-)}}}
    \\
    \mathbf{B}\mathbb{G}
    &\stackrel{curv_{\mathbf{B}\mathbb{G}}}{\to}&
    \flat_{dR}\mathbf{B}^2 \mathbb{G}
  }
$$

is the mopduli for [[principal ∞-connections]].

Now for 

$$
  \mathbf{c}
  \;\colon\;
  \mathbf{B}G
  \to 
  \mathbf{B}\mathbb{G}
$$

a [[universal characteristic map]] we say that a _differential refinement_ is a choice of $\mathbf{B}G_{conn}$ and $\hat \mathbf{c}$ in

$$
  \array{
    \flat \mathbf{B}G 
    &\stackrel{\flat \mathbf{c}}{\to}&
    \mathbf{B}\mathbb{G}
    \\
    \downarrow && \downarrow^{}
    \\
    \mathbf{B}G_{conn} &\stackrel{\hat \mathbf{c}}{\to}&
    \mathbf{B}\mathbb{G}_{conn}
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G
    &\stackrel{\mathbf{c}}{\to}&
    \mathbf{B}\mathbb{G}
  }
  \,.
$$

These are the [[extended Lagrangians]] here.

### Chern-Simons theory as the archetypical example
 {#CSAsArchetypicalExample}

For illustration purposes, we survey how the [[Chern-Simons field theory]] considered as a toy model for topological local Lagrangian gauge field theory considered [above](#ChernSimonsTheoryAsAToyExample) has in [[higher geometry]] a [[prequantum n-bundle|prequantum (n-k)-bundle]] associated in [[codimension]] $k$.

First consider again $G$ to be a [[connected topological space|connected]] and [[simply connected topological space|simply connected]] [[simple Lie group]]. Then the [[integral cohomology]] of the [[classifying space]] of $G$ is

$$
  H^4(BG , \mathbb{Z}) \simeq \mathbb{Z}
  \,.
$$

An element in here is a [[universal characteristic class]] of $G$-[[principal bundles]]. In Chern-Simons theory this is going to be what traditionally is called the [[level (Chern-Simons theory)|level]] of the theory.

We writ

$$
  c : B G \to  B^3 U(1) \simeq K(\mathbb{Z},4)
$$

for a represenative [[universal characteristic map]] of the corresponding degree-4 [[universal characteristic class]]. 


Under [[geometric realization of cohesive ∞-groupoids|geoetric realization]] as just [recalled](#IntermezzoElementsOfHigherCohesiveGeometry) this has an essentially unique lift to _smooth cohomology_, hence to a morphism of [[moduli ∞-stacks]]

$$
  \mathbf{c}
  \;\colon\;
  \mathbf{B}G
  \to 
  \mathbf{B}^3 U(1)
$$

which, in a precise sense, is the [[Lie integration]] of the canonical 3-[[cocycle]] 

$$
  \langle -, [-,-]\rangle \;\colon\; \mathfrak{g} \to \mathbf{B}^2 \mathbb{R}
$$

in the [[Lie algebra cohomology]] of the [[Lie algebra]] $\mathfrak{g}$ of $G$ in that

$$
  \mathbf{c} \simeq \tau_1 \exp(\mu)
  \,.
$$


Moreover, this smooth universal characteristic map  has a further lift to [[differential cohomology]]

$$
  \hat \mathbf{c}
  \;\colon\;
  \mathbf{B}G_{conn}
  \to 
  \mathbf{B}^3 U(1)_{conn}
  \,.
$$

This modulates a [[circle n-bundle with connection|circle 3-bundle with connection]] -- the "[[Chern-Simons circle 3-bundle with connection]]" -- on the [[smooth infinity-groupoid|smooth]] [[moduli stack]] of smooth $G$-[[principal connections]]. 

$$
  \array{
    \mathbf{B}G_{conn}
    &\stackrel{\hat \mathbf{c}}{\to}&
    \mathbf{B}^3 U(1)_{conn} 
    \\
    \downarrow && \downarrow &&& \mathbf{H}
    \\
    \mathbf{B}G
    &\stackrel{\mathbf{c}}{\to}&
    \mathbf{B}^3 U(1)
    \\
    && &&& \downarrow^{\mathrlap{{\vert \Pi(-)\vert}}}
    \\
    B G &\stackrel{c}{\to}& B^3 U(1) &&& L_{whe} Top
  }
$$

One finds that the [[transgression]] of this to codimension 0 is the Chern-Simons action functional discussed above. The other transgressions are

| [[dimension]] |  | [[prequantum n-bundle|prequantum (3-k)-bundle]] |  |
|---------------|--|-------------------------------------------------|--|
| $k = 0$ | [[twisted differential string structure|differential fractional first Pontryagin class]] | $\hat \mathbf{c} \;\colon\; \mathbf{B}G_{conn} \to \mathbf{B}^3 U(1)_{conn}$ |  ([FSS](#FSS))  |
| $k = 1$ | [[WZW model]] [[background gauge field|background]] [[B-field]] | $G \to [S^1, \mathbf{B}G_{conn}] \stackrel{[S^1, \hat \mathbf{c}]}{\to} [S^1, \mathbf{B}^3 U(1)_{conn}] \stackrel{\exp(2 \pi i \int_{S^1} (-))}{\to} \mathbf{B}^2 U(1)_{conn}$ |  |
| $k = 2$ | off-sheff [[prequantum bundle]] | $[\Sigma_2, \mathbf{B}G_{conn}] \stackrel{[\Sigma_2, \hat \mathbf{c}]}{\to} [\Sigma_2, \mathbf{B}^3 U(1)_{conn}] \stackrel{\exp(2 \pi i \int_{\Sigma_2} (-))}{\to} \mathbf{B} U(1)_{conn}$ | | 
| $k = 3$ | [[action functional]] | $[\Sigma_3, \mathbf{B}G_{conn}] \stackrel{[\Sigma_3, \hat \mathbf{c}]}{\to} [\Sigma_3, \mathbf{B}^3 U(1)_{conn}] \stackrel{\exp(2 \pi i \int_{\Sigma_3} (-))}{\to} U(1)$

Here the [[WZW model|WZW]] [[B-field]] is the topological part of a 2-dimensional local Lagrangian field theory called the _[[Wess-Zumino-Witten model]]_. One says that the WZW model is related by the [[holographic principle]] with [[3d Chern-Simons theory]].

If the [[gauge group]] $G$ is not simple and simply connected, then there are other canonical [[universal characteristic classes]] in $H^4(B G, \mathbb{Z})$. If these have a differential refinement, they give rise to the corresponding Chern-Simons theory.

Notably in the case that $G = U(1)$ is the [[circle group]] (hence not [[simply connected topological space|simply connected]]) there is the [[cup product]] of the universal [[first Chern class]] with itself

$$
  c_1 \cup c_1 \;\colon\; B U(1) \to B^3 U(1)
  \,.
$$

The smooth and differential refinement of the [[first Chern class]] itself $c_1 \;\colon\; B U(1) \to B U(1) K(\mathbb{Z},2) $ is tautological: this is simply the identity 

$$
  \widehat \mathbf{c}_1 \coloneqq id 
  \;\colon\;
  \mathbf{B}U(1)_{conn}
  \to 
  \mathbf{B}U(1)_{conn}
  \,.
$$

The nontrivial part is that, as one can see, the  [[cup product]] on [[differential cohomology]] refines to [[moduli ∞-stacks]] of [[circle n-bundle with connection]] as the [[∞-stackification]] of what is called the [[Beilinson-Deligne cup product]], and so we have 

$$
  \widehat \mathbf{c}_1 \cup \widehat \mathbf{c}_1
  \;\colon\;
  \mathbf{B}U(1)_{conn}
  \to
  \mathbf{B}^3 U(1)_{conn}
  \,.
$$

This is the [[extended Lagrangian]] for abelian Chern-Simons theory. On field configuration which happens to be given by a globally defined 1-form $A$ its value is 

$$
  \exp\left(
    2\pi i \int_{\Sigma_3} A \wedge d A
  \right)
  \in 
  U(1)
  \,.
$$

But now not every field configuration is necessarily given by a globally defined 1-form anymore, and more generally the action functional has a more sophisticated expression.

### 7-dimensional Chern-Simons theory as the next example
 {#7dCSTheoryAsExample}


So far we have considered general motivation for [[extended prequantum field theory]], and indication how its application to the well-known case of [[3d Chern-Simons theory]] naturally captures the characteristics of the theory. Now we consider further examples whose higher geometry has not necessarily been considered traditionally.

An immediate class of further examples is obtained by abelian [[higher Chern-Simons theory]] induced by the [[cup product]] of the [[first Chern class]] with itself

$$
  [DD_{2k} \cup DD_{2k}] \in H^{4(k+1)}(B^{2k+1} U(1), \mathbb{Z})
  \,.
$$

This has a refinement ([FSS cup](#FSSCup)) to a [[differential characteristic class]] by the 
_[[Beilinson-Deligne cup product]]_ of the [[differential characteristic class|differential refinement]] of the higher [[Dixmier-Douady class]] with itself:

$$
  \widehat \mathbf{DD}_{2k}
  \cup
  \widehat \mathbf{DD}_{2k}
  \;\colon\;
  \mathbf{B}^{2k+1} U(1)_{conn}
  \to 
  \mathbf{B}^{4k+3} U(1)_{conn}
  \,.
$$

In particular there is the abelian [[7d Chern-Simons theory]]

$$
  \widehat \mathbf{DD}_2
  \cup
  \widehat \mathbf{DD}_2
  \;\colon\;
  \mathbf{B}^3 U(1)_{conn}
  \to 
  \mathbf{B}^7 U(1)_{conn}
  \,.
$$

An argument in ([Witten 98](#AdS-CFT#Witten98)) says that this abelian 
[[7d Chern-Simons theory]] (or more precisely a [[quadratic refinement]] of it) is related to the _[[self-dual higher gauge theory]]_ sector of the [[6d (2,0)-supersymmetric QFT]] on the [[worldvolume]] of a single [[M5-brane]]_  in analogy to how [[3d Chern-Simons theory]] is related to the [[WZW model]]:

| [[schreiber:∞-Chern-Simons theory]] | $\leftarrow$[[holographic principle]] $\rightarrow$| [[schreiber:∞-Wess-Zumino-Witten theory ]] | [[Kaluza-Klein reduction]] $\to$ |   |
|--|--|--|--|--|
| [[3d Chern-Simons theory]]  | [3dCS-2dCFT](holographic+principle#3dCS-2dCFT) | [[WZW model]] | | |
| [[7d Chern-Simons theory]]  | [AdS7/CFT6 duality](AdS-CFT#AdS7CFT6) | [[6d (2,0)-supersymmetric QFT]] | | [[N=4 D=4 super Yang-Mills theory]] | 

The argument in ([Witten 98](#AdS-CFT#Witten98)) also says that in view of [AdS7/CFT6 duality](AdS-CFT#AdS7CFT6) the [[field (physics)|field]] of the 7d theory here is to be identified withe the _[[supergravity C-field]]_ in [[11-dimensional supergravity]]/[[M-theory]]. 

But the [[supergravity C-field]] is known to have moduli that are in general more complicated than just $\mathbf{B}^3 U(1)_{conn}$ (due to a [[Green-Schwarz anomaly cancellation]] mechanism in [[11-dimensional supergravity]] and a "flux quantization" condition). In ([FSS 7dCD](#FSS7dCS)) the corrected moduli are dicussed and found to involve a coupling of the abelian 7d theory with a nonabelian 7d Chern-Simons theory whose [[field (physics)|fields]] are twisted higher spin connections: "[[twisted differential string structures]]".

To see what this is, recall that [above](#CSAsArchetypicalExample) we interpreted the [[extended Lagrangian]] of [[3d Chern-Simons theory]] for a simply connected compact simple gauge group $G$ as the smooth and moreover differential refinement of the canonical [[universal characteristic class]] in $H^4(B G, \mathbb{Z})$. Specifically for $G$ the [[spin group]] this is the [[first fractional Pontryagin class]], represented by a [[characteristic map]]  

$$
  \tfrac{1}{2}p_1 \;\colon\; B Spin \to B^3 U(1)
  \,.
$$ 

This can be understood as a higher analog of the [[second Stiefel-Whitney class]] $w_2 \;\colon\; B SO \to B^2 \mathbb{Z}$ which is the universal [[obstruction]] to [[spin structure]]. We say that $\tfrac{1}{2}p_1$ is the universal [[obstruction]] to a _[[higher spin structure]]_ called _[[string structure]]_ (this and the motivation for this terminology is discussed in detail in _[geometry of physics - Fields - Examples - Fields of gravity and G-structure](geometry+pf+physics##FieldsOfGravityAndGeneralizedGeometry)_). These higher obstructions are the (dual) [[k-invariants]] of the [[Whitehead tower]] of $B O$:

[[!include higher spin structure - table]]

From the point of view of [[extended prequantum field theory]] we are to regard each horizontal map in this tower as classifying the potential underlying [[instanton sector]] of an [[extended Lagrangian]]/[[prequantum n-bundle]], and we may ask if these lift to actual extended Lagrangian.

The next step up the ladder is the universal [[second fractional Pontryagin class]]. Its [[twisted differential string structure|differential refinement]] as been constructed in ([FSS diff coc](#FiorenzaSchreiberStasheff)).

$$
  \array{
    \mathbf{B}String_{conn}
    &\stackrel{\widehat {\tfrac{1}{6}\mathbf{p}_2}}{\to}&
    \mathbf{B}^7 U(1)_{conn} 
    \\
    \downarrow && \downarrow &&& \mathbf{H}
    \\
    \mathbf{B}G
    &\stackrel{ \tfrac{1}{6}\mathbf{p}_2 }{\to}&
    \mathbf{B}^7 U(1)
    \\
    && &&& \downarrow^{\mathrlap{{\vert \Pi(-)\vert}}}
    \\
    B String &\stackrel{\tfrac{1}{6}p_2}{\to}& B^7 U(1) &&& L_{whe} Top
  }
  \,.
$$

This now defines an [[extended Lagrangian]] for a  [[7d Chern-Simons theory]] on [[String 2-group]]-[[2-connections]].  

Coming back to the above arguments about the relation of the 7d theory to a 6d theory, these suggest that the 6d theory involves  [[prequantum n-bundle|prequantum 6-bundle]]-analog of the [[WZW model|WZW 2-bundle]]. 

Indeed, the assignment of a higher Wess-Zumino-Witten-type [[prequantum n-bundle|prequantum (n-1)-bundle]] to an extended prequantum Lagrangian works very generally: the _prequantum $(n-1)$-bundle_ is the WZW-type $(n-1)$-bundle of the theory.
Its underlying $(n-1)$-bundle is simply the [[looping]] of the $n$-bundle underlying the [[extended Lagrangian]]. Specifically, the [[string 2-group]]-[[7d Chern-Simons theory]] has a WZW- prequantum 6-bundle on the [[string 2-group]] which is modulated by the map

$$
  \array{
    \mathbf{B}String
    && &\stackrel{\Omega \left( \tfrac{1}{6}\mathbf{p_2}\right)}{\to}& &&
    \mathbf{B}^6 U(1)
    \\
    {}^{\mathllap{\simeq}}\downarrow
    && && && \uparrow
    \\
    String //_{Ad} String
    &
    \stackrel{\simeq}{\to}
    &
    [\mathbf{\Pi}(S^1), \mathbf{B}String]
    &
    \stackrel{[\mathbf{\Pi}(S^1), \tfrac{1}{2}\mathbf{p}_2]}{\to}
    &
    [\mathbf{\Pi}(S^1), \mathbf{B}^7 U(1)]
    &\simeq&
    \mathbf{B}^6 U(1) // \mathbf{B}^6 U(1)
  }
  \,.
$$

Therefore in summary we find the following identifications of [[extended prequantum field theory]] with (semi-)traditional notions:

[[!include extended prequantum field theory - table]]


### $\infty$-Chern-Simons theory as the general example
 {#InfinityCSAsGeneralExample}

(...)


## Definition

Let $\mathbf{H}$ be an ambient [[(∞,1)-topos]], typically a [[cohesive (∞,1)-topos]] such as [[Smooth∞Grpd]] or one of its [[slice (∞,1)-topos|slices]]. For $n \in \mathbb{N}$ let $\mathbf{B}^n U(1)_{conn} \in \mathbf{H}$ be the [[moduli ∞-stack]] of [[circle n-bundles with connection]]. Let moreover $\mathbf{Fields} \in \mathbf{H}$ be the given [[moduli ∞-stack]] of [[field (physics)|field configurations]], so that for $\Sigma$ some [[worldvolume]] [[manifold]] a [[field (physics)|field]] configuration on $\Sigma$ is a map in $\mathbf{H}$ of the form

$$
  \phi \colon \Sigma \to \mathbf{Fields}
$$

a [[gauge transformation]] $\phi \Rightarrow \phi'$ is a [[homotopy]] between two such maps, and a [[higher gauge transformation]] is a higher homotopy.

Then an **extended Lagrangian** or [[prequantum n-bundle]] for an $n$-dimensional [[quantum field theory]] with fields classified by $\mathbf{Fields}$ is a map in $\mathbf{H}$ of the form

$$
  \mathbf{L}
  \;\colon\;
  \mathbf{Fields}
  \to 
  \mathbf{B}^n U(1)_{conn}
  \,.
$$

By post-[[composition]] this sends a field $\pho \colon \Sigma_n \to \mathbf{Fields}$ to the [[circle n-bundle with connection]] on $\Sigma_n$ modulated by

$$
  \mathbf{L}(\phi)
  \;\colon\;
  \Sigma_n 
  \stackrel{\phi}{\to}
  \mathbf{Fields}
  \stackrel{\mathbf{L}}{\to}
  \mathbf{B}^n U(1)_{conn}
  \,.
$$

This is locally  -- restricted to some [[good cover]] $U \to \Sigma_n$ of $\Sigma_b$) given by a [[differential n-form]] 

$$
  L(\phi) \omega \in \Omega^n(U)
  \,,
$$

where $L(\phi) \in C^\infty(U)$ is a [[smooth function]] and where $\omega \in \Omega^n(U)$ is some [[volume form]] or some other prespecified [[measure]]. This function $L(\phi)$ is the ordinary [[Lagrangian]]. 

Over an [[orientation|oriented]] [[closed manifold]] $\Sigma_n$ of [[dimension]] $n$ the corresponding [[action functional]] is the [[transgression]] of $\mathbf{L}$ to the mapping stack/[[internal hom]] out of $\Sigma_n$, hence the composite

$$
  \exp\left(
    2\pi i \int_{\Sigma_n} [\Sigma_n, \mathbf{L}]
  \right)
  \;\colon\;
  [\Sigma_n, \mathbf{Fields}]
  \stackrel{[\Sigma_n, \mathbf{L}]}{\to}
  [\Sigma_n, \mathbf{B}^n U(1)_{conn}]
  \stackrel{\exp(2 \pi in \int_{\Sigma_n})(-) }{\to}
  U(1)
  \,,
$$

where the first map is the [[internal hom]] on morphisms and the second is the [[higher holonomy]] map of a [[circle n-bundle with connection]] over $\Sigma_n$, hence the [[fiber integration in ordinary differential cohomology]]. 

For $\phi : \Sigma_n \to \mathbf{Fields}$ a field such that the [[circle n-group|circle (n-1)-group]] [[principal ∞-bundle]] underlying $\mathbf{L}(\phi)$ is trivializable and trivialized, the differential form $L(\phi)\omega$ discussed above descends to $X$ itself and the [[action functional]] is simply the [[integration of differential forms]]

$$
  \phi \mapsto \exp\left(2 \pi i \int_{\Sigma_n} L(\phi) \omega \right)
  \,.
$$

This special case is the relation between [[Lagrangians]] and [[action functionals]] as traditionally considered.

Generally, for $0 \leq k \leq n$ and $\Sigma_{k}$ an oriented [[closed manifold]] of [[dimension]] $k$, transgression as above yields a map in $\mathbf{H}$ of the form

$$
  \exp\left(
    2\pi i \int_{\Sigma_k} [\Sigma_n, \mathbf{L}]
  \right)
  \;\colon\;
  [\Sigma_k, \mathbf{Fields}]
  \stackrel{[\Sigma_n, \mathbf{L}]}{\to}
  [\Sigma_l, \mathbf{B}^n U(1)_{conn}]
  \stackrel{\exp(2 \pi in \int_{\Sigma_k})(-) }{\to}
  \mathbf{B}^{n-k}U(1)_{conn}
$$

which modulates a [[circle n-bundle with connection|circle (n-k)-bundle with connection]] on the [[moduli infinity-stack]] of fields on $\Sigma_k$. At least for large classes of theories, this is the (off-shell) [[prequantum n-bundle|prequantum (n-k)-bundle]] of the theory.

## Properties

### Relation to universal characteristic classes

By the discussion at _[[field (physics)]]_ in the section _[Properties - Relation to twisted cohomology](field%20%28physics%29#RelationToTwistedCohomology)_ a field configuration in any [[theory of physics]] may equivalently be thought of as a [[cocycle]] in [[twisted cohomology|twisted]] general [[cohomology]]. Here we discuss that evaluating an extended Lagrangian on such a field configuration is equivalently producing a [[characteristic class]]. In other words, under this identification with [[cohomology]] an extended Lagrangian is equivalently a [[universal characteristic map]] and its [[equivalence class]] is the corresponding [[universal characteristic map]].

[[!include gauge field - table]]

## Examples

### For discrete higher gauge groups: $\infty$-Dijkgraaf-Witten theory

$G$ a [[discrete ∞-group]]

extended Lagrangians are cocycles in [[group cohomology]]:

$$
  \pi_0 \mathbf{H}(\mathbf{B}G, \mathbf{B}^n U(1))
  \simeq
  \pi_0 Top(B G, B^n U(1)_{disc})
  \simeq
  H_{Grp}^n(G,U(1))
$$

these are the extendd Lagrangians of [[infinity-Dijkgraaf-Witten theory]].

### For ordinary gauge theory with

We consider $G$ a [[Lie group]], to be regarded as the [[gauge group]] of a [[gauge theory]]. We write $\mathbf{B}G_{conn} \in \mathbf{H}$ for the [[smooth infinity-groupoid|smooth]] [[moduli stack]] of $G$-[[principal connections]].  

Setting $\mathbf{Fields} \coloneqq \mathbf{B}G_{conn}$ this is the [[moduli stack]] for [[field (physics)|fields]] in a pure $G$-gauge theory. An extended Lagrangian is hence to be a map

$$
  \mathbf{L} 
    \;\colon\;
  \mathbf{B}G_{conn}
   \stackrel{}{\to}
  \mathbf{B}^n U(1)_{conn}
  \,.
$$

+-- {: .prop_defn}
###### Proposition

For $G \in \mathbf{H} \coloneqq $ [[Smooth∞Grpd]] a [[compact Lie group]] and $n \in \mathbb{N}$, then [[geometric realization of cohesive ∞-groupoids]] ${\vert - \vert} \colon \mathbf{H} \to \infty Grpd \simeq L_{whe} Top$ induces a [[natural isomorphism]]

$$ 
  {\vert- \vert}
  \;\colon\;
  \pi_0 \mathbf{H}(\mathbf{B}G, \mathbf{B}^n U(1))
  \stackrel{\simeq}{\to}
  \pi_0 L_{whe} Top(B G, B^n U(1))
  \simeq
  H^{n+1}(B G, \mathbb{Z})
  \,.
$$ 

=--

This is discussed at _[[Lie group cohomology]]_. The proof is in ([dcct](#dcct)).

+-- {: .prop_defn}
###### Proposition

This means that the [[instanton sectors]] of extended Lagrangians for pure ordinary gauge theory are labeled precisely by the [[integral cohomology]] of the [[classifying space]] $B G$ of the [[gauge group]]. In ordinary [[Chern-Simons theory]] this is called the **level** of the theory.

=--

### Higher gauge theory

If $G \in Grp(\mathbf{H})$ is an [[∞-group]] (a [[smooth ∞-group]] if $\mathbf{H}$ is [[Smooth∞Grpd]]) and 

$$
  \mathbf{Fields}  
  \simeq
  \mathbf{B}G_{conn}
$$

is a [[moduli ∞-stack]] of $G$-[[principal ∞-bundle|principal]] [[connection on an ∞-bundle|∞-connections]], then the theory in question is a ([[higher gauge theory|higher]]) [[gauge theory]]. In this case the map

$$
  \mathbf{c} \;\colon\; \mathbf{B}G \to \mathbf{B}^n U(1)
$$

underlying the extended Lagrangian is a [[cocycle]] that induces an [[extension of ∞-groups]], fitting a [[homotopy fiber sequence]]

$$
  \mathbf{B}^{n-1}U(1) \to \mathbf{B}\hat G
\stackrel{}{\to} \mathbf{B}G \stackrel{\mathbf{c}}{\to} \mathbf{B}^n U(1)
  \,.
$$

In this case the extended Lagrangian also plays the role as the universal differential refinement of the [[obstruction]] class to [[lift of structure groups]] through $\hat G \to G$. More generally, its [[homotopy fiber products]] are [[moduli ∞-stacks]] of [[twisted differential c-structures]]. See there for more examples.

### Construction of extended Lagrangians by Lie integration
 {#ByLieIntegration}

[[Lie integration]]:

for $\mathbb{g}$ an [[L-∞ algebra]] and

$$
  \mu \;\colon\; \mathfrak{g} \to b^{n-1}\mathbb{R}
$$ 

a [[homomorphism]] of $L_\infty$-algebras into the [[line Lie n-algebra]], hence a [[cocycle]] in [[L-∞ algebra cohomology]], the operation of differentially refined [[Lie integration]] ([FSS diff coc](#FiorenzaSchreiberStasheff)) produces a morphism of [[moduli ∞-stacks]]

$$
  \widehat {\exp(\mu)}
  \;\colon\;
  \exp(\mathfrak{g})_{conn}
  \to 
  \mathbf{B}^n \mathbb{R}_{conn}
$$

Under [[truncated object in an (∞,1)-category|truncation]] this yields

$$
  \mathbf{B}G_{conn}
  \to 
  \mathbf{B}^n (\mathbb{R}/\Gamma)
  \,,
$$

where $G \coloneqq \Omega \tau_n \exp(\mathfrak{g})$ and where $\mathbf{B}G_{conn}$ is the moduli of $G$-[[connections on an ∞-bundle|∞-connections]]. ([FSS](#FiorenzaSchreiberStasheff))

### Higher Chern-Simons theory

Various examples are discussed at 

* [[schreiber:∞-Chern-Simons theory]]

* [[higher dimensional Chern-Simons theory]]

  * [[1d Chern-Simons theory]]

  * [[Chern-Simons theory]]

  * [[5d Chern-Simons theory]]

  * [[7d Chern-Simons theory]]

  * [[AKSZ sigma-models]]

  * [[string field theory]]

  * [[infinite-dimensional Chern-Simons theory]]

## Related concepts

[[!include extended prequantum field theory - table]]
  

## References

Expositions, examples and further pointers are in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Extended higher cup-product Chern-Simons theories]]_

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_

Lecture notes are in _[[geometry of physics]]_, and section 1.2 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_
 {#dcct}

A general abstract discussion is in section 3 there, further discussion of examples in section 5.

The construction of extended Lagrangian by [[Lie integration]] of [[L-∞ algebra cocycles]] is due to

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech Cocycles for Differential characteristic Classes]]_
 {#FiorenzaSchreiberStasheff}

Construction of differential cup-product theories is in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Extended higher cup-product Chern-Simons theories]]_
 {#FSSCup}


The discussion of the abelian [[7d Chern-Simons theory]] involved in [AdS7/CFT6 duality](AdS-CFT#AdS7CFT6) is due to ([Witten 98](#AdS-CFT#Witten98)). The discussion of the non-abelian quantum-corrected version is due to

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:7d Chern-Simons theory and the 5-brane]]_
 {#FSS7dCS}

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The moduli 3-stack of the C-field]]_


[[!redirects extended Lagrangians]]




