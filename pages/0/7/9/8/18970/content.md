

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[perturbative quantum field theory]] the construction of the [[scattering matrix]] $\mathcal{S}$, hence of the [[interacting field algebra of observables]] for a given [[interaction]] $g S_{int}$ [[perturbation theory|perturbing]] around a given [[free field theory|free field]] [[vacuum]], involves choices of _normalization_ of [[time-ordered products]]/[[Feynman diagrams]] (traditionally called _[[renormalization|"re"-normalizations]]_) encoding new [[interactions]] that appear where several of the original interaction vertices defined by $g S_{int}$ coincide.

Whenever a [[group]] $RG$ [[action|acts]] on the space of [[observables]] of the theory such that [[conjugation]] by this action takes [[renormalization scheme|("re"-)normalization schemes]] into each other, then these  choices of [[renormalization|("re"-)normalization]]  are parameterized by -- or "flow with" -- the elements of $RG$.  This is called _renormalization group flow_  (prop.
\ref{FlowRenormalizationGroup} below); often called _RG flow_, for short.

The archetypical example here is the [[group]] $RG$ of [[scaling transformations]] on [[Minkowski spacetime]] (def. \ref{ScalingTransformations} below), which induces a [[renormalization group flow]] (prop. \ref{RGFlowScalingTransformations} below) due to the particular nature of the [[Wightman propagator]] resp. [[Feynman propagator]] on [[Minkowski spacetime]] (example \ref{ScalarFieldMassDimensionOnMinkowskiSpacetime} below). In this case the choice of [[renormalization|("re"-)normalization]] hence "flows with scale".

Now the _[[main theorem of perturbative renormalization]] states that (if only the basic [[renormalization condition]] called "field independence" is satisfied) any two choices of [[renormalization scheme|("re"-)normalization schemes]] $\mathcal{S}$ and $\mathcal{S}'$ are related by a unique [[interaction vertex redefinition]] $\mathcal{Z}$, as

$$
  \mathcal{S}' = \mathcal{S} \circ \mathcal{Z}
  \,.
$$

Applied to a parameterization/flow of renormalization choices by a group $RG$ this hence induces an [[interaction vertex redefinition]] as a function of $RG$. One may think of the shape of the interaction vertices as fixed and only their ([[adiabatic switching|adiabatically switched]]) [[coupling constants]] as changing under such an [[interaction vertex redefinition]], and hence then one has [[coupling constants]] $g_j$ that are parameterized by elements $\rho$ of $RG$:

$$
  \mathcal{Z}_{\rho_{vac}}^\rho
  \;\colon\;
  \{g_j\}
    \mapsto
  \{g_j(\rho)\}
$$

This dependendence is called _running of the coupling constants_ under the renormalization group flow (def. \ref{CouplingRunning} below).

One example of [[renormalization group flow]] is that induced by [[scaling transformations]] (prop. \ref{RGFlowScalingTransformations} below). This is the original and main example of the concept ([Gell-Mann & Low 54](#GellMannLow54))

In this case the [[running of the coupling constants]] may be understood as expressing how "more" [[interactions]] (at higher energy/shorter [[wavelength]]) become visible (say to [[experiment]]) as the scale resolution is increased. In this case the dependence of the coupling $g_j(\rho)$ on the parameter $\rho$ happens to be [[differentiable function|differentiable]]; its [[logarithm|logarithmic]] [[derivative]] (denoted "$\psi$" in [Gell-Mann & Low 54](#GellMannLow54)) is known as the _[[beta function]]_ ([Callan 70](#Callan70), [Symanzik 70](#Symanzik70)):

$$
  \beta(g) \coloneqq \rho \frac{\partial g_j}{\partial \rho}
  \,.
$$

Notice that this is related to, but conceptually different from, _[[Polchinski's flow equation]]_ in the context of [[Wilsonian RG]].


The [[running of the coupling constants]] is not quite a [[representation]] of the [[renormalization group flow]],
but it is a "twisted" representation, namely a [[group cocycle|group 1-cocycle]] (prop. \ref{CocycleRunningCoupling} below). For the case of [[scaling transformations]] this may be called the _[[Gell-Mann-Low renormalization cocycle]]_ ([Brunetti-Dütsch-Fredenhagen 09](#BrunettiDuetschFredenhagen09)).

For more see at 

* [[geometry of physics -- A first idea of quantum field theory]] the section _[Renormalization](geometry+of+physics+--+A+first+idea+of+quantum+field+theory#Renormalization)_

## Definition


+-- {: .num_prop #FlowRenormalizationGroup}
###### Proposition
**([[renormalization group flow]])**

Let

$$
  vac
    \;\coloneqq\;
  (E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )
$$

be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) around which we consider [[interacting field theory|interacting]] [[perturbative QFT]].

Consider a [[group]] $RG$ equipped with an [[action]] on the [[Wick algebra]] of [[off-shell]] [[microcausal polynomial observables]] with formal parameters adjoined (as in [this def.](S-matrix#FormalParameters))

$$
  rg_{(-)}
  \;\colon\;
  RG \times PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g, j ] ]
  \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ \hbar, g, j ] ]
  \,,
$$

hence for each $\rho \in RG$ a [[continuous linear map]] $rg_\rho$ which has an [[inverse]] $rg_\rho^{-1} \in RG$ and is a [[homomorphism]] of the [[Wick algebra]]-product (the [[star product]] $\star_H$ induced by the [[Wightman propagator]] of the given vauum $vac$)

$$
  rg_\rho( A_1 \star_H A_2 )
  \;=\;
  rg_\rho(A_1) \star_H rg_\rho(A_2)
$$

such that the following conditions hold:

1. the action preserves the subspace of [[off-shell]] polynomial [[local observables]], hence it [[restriction|restricts]] as

   $$
     rg_{(-)}
     \;\colon\;
     RG \times LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]\langle g,j\rangle
     \longrightarrow
     LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]\langle g,j\rangle
   $$

1. the action respects the [[causal order]] of the spacetime support ([this def.](A+first+idea+of+quantum+field+theory#SpacetimeSupport)) of local observables, in that for $O_1, O_2 \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]$ we have

   $$
     \left(
       supp(O_1)
       \,{\vee\!\!\!\wedge}\,
       supp(O_2)
     \right)
     \phantom{A}
       \Rightarrow
     \phantom{A}
     \left(
       supp(rg_\rho(O_1))
       \,{\vee\!\!\!\wedge}\,
       supp(rg_\rho(O_2))
     \right)
   $$

   for all $\rho \in RG$.

Then:

The operation of [[conjugation]] by this action on [[observables]] induces an [[action]] on the [[set]] of [[S-matrix]] [[renormalization schemes]] ([this def.](S-matrix#LagrangianFieldTheoryPerturbativeScattering), [this remark](S-matrix#calSFunctionIsRenormalizationScheme)),
in that for

$$
  \mathcal{S}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar , g, j] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})( (\hbar) )[ [ g, j] ]
$$

a perturbative [[S-matrix scheme]] around the given [[free field theory|free field]] [[vacuum]] $vac$, also the [[composition|composite]]

$$
  \mathcal{S}^\rho
  \;\coloneqq\;
  rg_\rho \circ \mathcal{S} \circ rg_{\rho}^{-1}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar , g, j] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})( (\hbar) )[ [ g, j] ]
$$

is an [[S-matrix]] scheme, for all $\rho \in RG$.

More generally, let

$$
  vac_\rho
    \;\coloneqq\;
  (E_{\text{BV-BRST}}, \mathbf{L}'_\rho, \Delta_{H,\rho} )
$$

be a collection of [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacua]] parameterized by elements $\rho \in RG$,
all with the same underlying [[field bundle]]; and
consider $rg_\rho$ as above, except that it is not an [[automorphism]] of any [[Wick algebra]],
but an [[isomorphism]] between the [[Wick algebra]]-structures on various vacua, in that

$$
  \label{IntertwiningWickProductsActionRG}
  rg_{\rho}( A_1 \star_{H, \rho^{-1} \rho_{vac}} A_2 )
  \;=\;
  rg_{\rho}(A_1) \star_{H, \rho_{vac}} rg_{\rho}(A_2)
$$

for all $\rho, \rho_{vac} \in RG$

Then if

$$
  \{ \mathcal{S}_{\rho} \}_{\rho \in RG}
$$

is a collection of [[S-matrix schemes]], one around each of the [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacua]]
$vac_\rho$, it follows that for all pairs of group elements $\rho_{vac}, \rho \in RG$ the [[composition|composite]]

$$
  \label{RGConjugateSmatrix}
  \mathcal{S}_{\rho_{vac}}^\rho
  \;\coloneqq\;
  rg_\rho \circ \mathcal{S}_{\rho^{-1}\rho_{vac}} \circ rg_\rho^{-1}
$$

is an [[S-matrix scheme]] around the vacuum labeled by $\rho_{vac}$.


Since therefore each element $\rho \in RG$ in the [[group]] $RG$ picks a different choice of [[renormalization|normalization]]
of the [[S-matrix]] scheme around a given vacuum at $\rho_{vac}$, we call the assignment $\rho \mapsto \mathcal{S}_{\rho_{vac}}^{\rho}$
a _[[renormalization group flow|re-normalization group flow]]_.



=--

([Brunetti-Dütsch-Fredenhagen 09, sections 4.2, 5.1](#BrunettiDuetschFredenhagen09), [Dütsch 18, section 3.5.3](#Duetsch18))

+-- {: .proof}
###### Proof

It is clear from the definition that each $\mathcal{S}^{\rho}_{\rho_{vac}}$ satisfies the axiom "perturbation" (in [this def.](S-matrix#LagrangianFieldTheoryPerturbativeScattering)).

In order to verify the axiom "[[causal additivity]]",
observe, for convenience, that by [this prop.](S-matrix#CausalFactorizationAlreadyImpliesSMatrix) it is sufficient to check [[causal factorization]].

So consider $O_1, O_2 \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g,j\rangle$
two local observables whose spacetime support is in [[causal order]].

$$
  supp(O_1)
  \;{\vee\!\!\!\wedge}\;
  supp(O_2)
  \,.
$$

We need to show that the

$$
  \mathcal{S}_{\rho_{vac}}^{\rho}(O_1 + O_2)
  =
  \mathcal{S}_{\rho_{vac}}^\rho(O_1)
    \star_{H,\rho_{vac}}
  \mathcal{S}_{vac_e}^\rho(O_2)
$$

for all $\rho, \rho_{vac} \in RG$.

Using the defining properties of $rg_{(-)}$ and the [[causal factorization]] of $\mathcal{S}_{\rho^{-1}\rho_{vac}}$ we directly compute as follows:


$$
  \begin{aligned}
    \mathcal{S}_{\rho_{vac}}^\rho(O_1 + O_2)
    & =
    rg_\rho
      \circ
    \mathcal{S}_{\rho^{-1} \rho_{vac}}
      \circ
    rg_\rho^{-1}( O_1 + O_2 )
    \\
    & =
    rg_\rho
    \left(
      {\, \atop \,}
      \mathcal{S}_{\rho^{-1}\rho_{vac}}
      \left(
        rg_\rho^{-1}(O_1) + rg_\rho^{-1}(O_2)
      \right)
      {\, \atop \,}
    \right)
    \\
    & =
    rg_\rho
    \left(
      {\, \atop \,}
      \left(
        \mathcal{S}_{\rho^{-1}\rho_{vac}}\left(rg_\rho^{-1}(O_1)\right)
      \right)
        \star_{H, \rho^{-1} \rho_{vac}}
      \left(
        \mathcal{S}_{ \rho^{-1} \rho_{vac} }\left(rg_\rho^{-1}(O_2)\right)
      \right)
      {\, \atop \,}
    \right)
    \\
    & =
    rg_\rho
    \left(
      {\, \atop \,}
      \mathcal{S}_{\rho^{-1} \rho_{vac}}\left(rg_{\rho^{-1}}(O_1)\right)
      {\, \atop \,}
    \right)
    \star_{H, \rho_{vac}}
    rg_\rho
    \left(
      {\, \atop \,}
      \mathcal{S}_{\rho^{-1} \rho_{vac}}\left( rg_\rho^{-1}(O_2)\right)
      {\, \atop \,}
    \right)
    \\
    & =
    \mathcal{S}^\rho_{\rho_{vac}}( O_1 )
      \,
      \star_{H, \rho_{vac}}
      \,
     \mathcal{S}_{\rho_{vac}}^\rho(O_2)
    \,.
  \end{aligned}
$$

=--

+-- {: .num_defn #CouplingRunning}
###### Definition
**([[running coupling constants]])**

Let

$$
  vac
  \coloneqq
  vac_e
    \;\coloneqq\;
  (E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )
$$

be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) around which we consider [[interacting field theory|interacting]] [[perturbative QFT]], let $\mathcal{S}$ be an [[S-matrix]] scheme
around this vacuum and let $rg_{(-)}$ be a [[renormalization group flow]] according to prop. \ref{FlowRenormalizationGroup}, such that each re-normalized [[S-matrix scheme]] $\mathcal{S}_{vac}^\rho$ satisfies the [[renormalization condition]] "field independence".

Then by the [[main theorem of perturbative renormalization]] ([this prop.](Stückelberg-Petermann+renormalization+group#AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition)) there is for every [[pair]] $\rho_1, \rho_2 \in RG$ a unique [[interaction vertex redefinition]]

$$
  \mathcal{Z}_{\rho_{vac}}^{\rho}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]
    \longrightarrow
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]
$$

which relates the corresponding two [[S-matrix]] schemes via

$$
  \label{SMatrixScemesRelatedByRunningFunction}
  \mathcal{S}_{\rho_{vac}}^{\rho}
  \;=\;
  \mathcal{S}_{\rho_{vac}}
    \circ
  \mathcal{Z}_{\rho_{vac}}^\rho
  \,.
$$

If one thinks of an [[interaction]] vertex, hence a [[local observable]] $g S_{int}+ j A$, as specified by the ([[adiabatic switching|adiabatically switched]]) [[coupling constants]] $g_j \in C^\infty_{cp}(\Sigma)\langle g \rangle$ multiplying the corresponding [[interaction]] [[Lagrangian densities]] $\mathbf{L}_{int,j} \in \Omega^{p+1,0}_\Sigma(E_{\text{BV-BRST}})$ as

$$
  g S_{int}
  \;=\;
  \underset{j}{\sum} \tau_\Sigma \left( g_j \mathbf{L}_{int,j} \right)
$$

(where $\tau_\Sigma$ denotes [[transgression of variational differential forms]]) then $\mathcal{Z}_{\rho_1}^{\rho_2}$ exhibits a dependency of the ([[adiabatic switching|adiabatically switched]]) [[coupling constants]] $g_j$ of the [[renormalization group flow]] parameterized by $\rho$. The corresponding functions

$$
  \mathcal{Z}_{\rho_{vac}}^{\rho}(g S_{int})
    \;\colon\;
   (g_j)
     \mapsto
   (g_j(\rho))
$$

are then called _[[running coupling constants]]_.

=--

([Brunetti-Dütsch-Fredenhagen 09, sections 4.2, 5.1](#BrunettiDuetschFredenhagen09), [Dütsch 18, section 3.5.3](#Duetsch18))

## Properties

+-- {: .num_prop #CocycleRunningCoupling}
###### Proposition
**([[running coupling constants]] are  [[group cocycle]] over [[renormalization group flow]])**

Consider [[running coupling constants]]

$$
   \mathcal{Z}_{\rho_{vac}}^{\rho}
   \;\colon\;
   (g_j)
     \mapsto
   (g_j(\rho))
$$

as in def. \ref{CouplingRunning}. Then for all $\rho_{vac}, \rho_1, \rho_2 \in RG$ the following equality is satisfied
by the "running functions" (eq:SMatrixScemesRelatedByRunningFunction):

$$
  \mathcal{Z}_{\rho_{vac}}^{\rho_1 \rho_2}
  \;=\;
  \mathcal{Z}_{\rho_{vac}}^{\rho_1}
    \circ
  \left(
    \sigma_{\rho_1}
      \circ
    \mathcal{Z}_{\rho^{-1} \rho_{vac}}^{\rho_2}
      \circ
    \sigma_{\rho_1}^{-1}
  \right)
  \,.
$$

=--

([Brunetti-Dütsch-Fredenhagen 09 (69)](#BrunettiDuetschFredenhagen09), [Dütsch 18, (3.325)](#Duetsch18))

+-- {: .proof}
###### Proof

Directly using the definitions, we compute as follows:

$$
  \begin{aligned}
    \mathcal{S}_{\rho_{vac}}
      \circ
    \mathcal{Z}_{\rho_{vac}}^{\rho_1 \rho_2}
    & =
    \mathcal{S}_{\rho_{vac}}^{\rho_1 \rho_2 }
    \\
    & =
    \sigma_{\rho_1}
      \circ
    \underset{
      =
      \mathcal{S}_{\rho_1^{-1} \rho_{vac}}^{\rho_2}
        =
      \mathcal{S}_{\rho_1^{-1} \rho_{vac}}
        \circ
      \mathcal{Z}_{\rho_1^{-1} \rho_vac}^{\rho_2}
    }{
    \underbrace{
      \sigma_{\rho_2}
        \circ
      \mathcal{S}_{\rho_2^{-1}\rho_1^{-1}\rho_{vac}}
        \circ
      \sigma_{\rho_2}^{-1}
    }}
      \circ
    \sigma_{\rho_1}^{-1}
    \\
    & =
    \underset{
      =
      \mathcal{S}_{\rho_{vac}}
        \circ
      \mathcal{Z}_{\rho_{vac}}^{\rho_1}
        \circ
      \sigma_{\rho_1}
    }{
    \underbrace{
      \sigma_{\rho_1}
        \circ
      \mathcal{S}_{\rho_1^{-1} \rho_{vac}}
        \circ
      \overset{ = id }{
        \overbrace{
          \sigma_{\rho_1}^{-1}
            \circ
          \sigma_{\rho_1}
        }
    }
    }}
      \circ
      \mathcal{Z}_{\rho_1^{-1} \rho_{vac}}^{\rho_2}
      \circ
      \sigma_{\rho_1}^{-1}
    \\
    & =
    \mathcal{S}_{\rho_{vac}}
      \circ
    \mathcal{Z}_{\rho_{vac}}^{\rho_1}
      \circ
    \underbrace{
      \sigma_{\rho_1}
        \circ
      \mathcal{Z}_{\rho_1^{-1} \rho_{vac}}^{\rho_2}
        \circ
      \sigma_{\rho_1}^{-1}
    }
  \end{aligned}
$$

This demonstrates the equation between vertex redefinitions to be shown after [[composition]] with an S-matrix scheme. But by the uniqueness-clause in the [[main theorem of perturbative renormalization]] the composition operation $\mathcal{S}_{\rho_{vac}} \circ (-)$ as a function from [[vertex redefinitions]] to S-matrix schemes is [[injective function|injective]]. This implies the equation itself.

=--

## Examples

### Scaling transformations
 {#ScalingTransformationsRGFlow}

We discuss (prop. \ref{RGFlowScalingTransformations} below) that, if the field species involved have well-defined [[mass dimension]] (example \ref{ScalarFieldMassDimensionOnMinkowskiSpacetime} below) then [[scaling transformations]] on [[Minkowski spacetime]] (example \ref{ScalingTransformations} below) induce a [[renormalization group flow]] (def. \ref{FlowRenormalizationGroup}). This is the original and main example of [[renormalization group flows]] ([Gell-Mann& Low 54](#GellMannLow54)).



+-- {: .num_example #ScalingTransformations}
###### Example
**([[scaling transformations]] and [[mass dimension]])**

Let

$$
  E \overset{fb}{\longrightarrow} \Sigma
$$

be a [[field bundle]] which is a [[trivial vector bundle]] over [[Minkowski spacetime]] $\Sigma = \mathbb{R}^{p,1} \simeq_{\mathbb{R}} \mathbb{R}^{p+1}$.

For $\rho \in (0,\infty) \subset \mathbb{R}$ a [[positive real number]],
write

$$
  \array{
    \Sigma
      &\overset{\rho}{\longrightarrow}&
    \Sigma
    \\
    x &\mapsto& \rho x
  }
$$

for the operation of multiplication by $\rho$ using the [[real vector space]]-[[structure]] of the [[Cartesian space]] $\mathbb{R}^{p+1}$ underlying [[Minkowski spacetime]].

By [[pullback of differential forms|pullback]] this acts on [[field histories]] ([[sections]] of the [[field bundle]]) via

$$
  \array{
    \Gamma_\Sigma(E)
      &\overset{\rho^\ast}{\longrightarrow}&
    \Gamma_\Sigma(E)
    \\
    \Phi &\mapsto& \Phi(\rho(-))
  }
  \,.
$$

Let then

$$
  \rho
    \mapsto
  vac_\rho
    \;\coloneqq\;
  (E_{\text{BV-BRST}}, \mathbf{L}'_{\rho}, \Delta_{H,\rho} )
$$

be a 1-parameter collection of [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacua]] on that field bundle, according to [this def.](S-matrix#VacuumFree), and consider a decomposition into a set $Spec$ of field species ([this def.](S-matrix#VerticesAndFieldSpecies)) such that for each $sp \in Spec$ the collection of [[Feynman propagators]] $\Delta_{F,\rho,sp}$ for that species _scales homogeneously_ in that there exists

$$
  dim(sp) \in \mathbb{R}
$$

such that for all $\rho$ we have (using [[generalized functions]]-notation)

$$
  \label{FeynmanPropagatorScalingBehaviour}
  \rho^{ 2 dim(sp) }  \Delta_{F, 1/\rho, sp}( \rho x )
  \;=\;
  \Delta_{F,sp, \rho = 1}(x)
  \,.
$$

Typically $\rho$ rescales a [[mass]] parameter, in which case $dim(sp)$ is also called the _[[mass dimension]]_ of the field species $sp$.

Let finally

$$
  \array{
    PolyObs(E)
    &
      \overset{
        \sigma_\rho
      }{\longrightarrow}
    &
    PolyObs(E)
    \\
    \mathbf{\Phi}_{sp}^a(x)
      &\mapsto&
    \rho^{- dim(sp)} \mathbf{\Phi}^a( \rho^{-1} x )
  }
$$

be the [[function]] on [[off-shell]] [[polynomial observables]] given on [[field observables]] $\mathbf{Phi}^a(x)$ by [[pullback of differential forms|pullback]] along $\rho^{-1}$ followed by multiplication by $\rho$ taken to the negative power of the [[mass dimension]], and extended from there to all [[polynomial observables]] as an [[associative algebra|algebra]] [[homomorphism]].

This constitutes an [[action]] of the [[group]]

$$
  RG
    \coloneqq
  \left(
    \mathbb{R}_+, \cdot
  \right)
$$

of [[positive real numbers]] (under [[multiplication]]) on [[polynomial observables]], called the group of _[[scaling transformations]]_ for the given choice of field species and [[mass]] parameters.

=--

([Dütsch 18, def. 3.19](#Duetsch18))


+-- {: .num_example #ScalarFieldMassDimensionOnMinkowskiSpacetime}
###### Example
**([[mass dimension]] of [[scalar field]])**

Consider the [[Feynman propagator]] $\Delta_{F,m}$ of the [[free field theory|free]] [[real scalar field]] on [[Minkowski spacetime]] $\Sigma = \mathbb{R}^{p,1}$  for [[mass]] parameter $m \in (0,\infty)$; a [[Green function]] for the [[Klein-Gordon equation]].

Let the group $RG \coloneqq (\mathbb{R}_+, \cdots)$ of [[scaling transformations]] $\rho \in \mathbb{R}_+$ on [[Minkowski spacetime]] (def. \ref{ScalingTransformations}) act on the mass parameter by inverse multiplication

$$
  (\rho , \Delta_{F,m})
    \mapsto
  \Delta_{F,\rho^{-1}m}(\rho (-))
  \,.
$$

Then we have

$$
  \Delta_{F,\rho^{-1}m}(\rho (-))
  \;=\;
  \rho^{-(p+1) + 2}
  \Delta_{F,1}(x)
$$

and hence the corresponding [[mass dimension]] (def. \ref{ScalingTransformations}) of the [[real scalar field]] on $\mathbb{R}^{p,1}$ is

$$
  dim(\text{scalar field})
  =
  (p+1)/2 - 1
  \,.
$$

=--

+-- {: .proof}
###### Proof

By  ([this prop.](Feynman+propagator#FeynmanPropagatorAsACauchyPrincipalvalue)) the [[Feynman propagator]] in question is given by the [[Cauchy principal value]]-formula (in [[generalized function]]-notation)

$$
  \begin{aligned}
  \Delta_{F,m}(x)
  & =
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{+i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu x^\mu}
  }{
    - k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 \pm i \epsilon
  }
  \, d k_0 \, d^p \vec k
  \,.
  \end{aligned}
$$

By applying [[change of integration variables]] $k \mapsto \rho^{-1} k$ in the [[Fourier transform of distributions|Fourier transform]] this becomes

$$
  \begin{aligned}
  \Delta_{F,\rho^{-1}m}(\rho x)
  & =
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{+i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu \rho x^\mu}
  }{
    - k_\mu k^\mu - \left( \rho^{-1} \tfrac{m c}{\hbar} \right)^2 \pm i \epsilon
  }
  \, d k_0 \, d^p \vec k
  \\
  & =
  \rho^{-(p+1)}
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{+i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu x^\mu}
  }{
    - \rho^{-2} k_\mu k^\mu - \rho^{-2} \left( \tfrac{m c}{\hbar} \right)^2 \pm i \epsilon
  }
  \, d k_0 \, d^p \vec k
  \\
  & =
  \rho^{-(p+1)+2}
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{+i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu x^\mu}
  }{
    - k_\mu k^\mu -  \left( \tfrac{m c}{\hbar} \right)^2 \pm i \epsilon
  }
  \, d k_0 \, d^p \vec k
  \\
  & =
  \rho^{-(p+1) + 2}
  \Delta_{F,m}(x)
  \end{aligned}
$$

=--

+-- {: .num_prop #RGFlowScalingTransformations}
###### Proposition
**([[scaling transformations]] are [[renormalization group flow]])**

Let

$$
  vac \coloneqq vac_m
  \coloneqq (E_{\text{BV-BRST}}, \mathbf{L}', \Delta_{H,m})
$$

be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacua]] on that field bundle, according to [this def.](S-matrix#VacuumFree) equipped with a decomposition into a set $Spec$ of field species ([this def.](S-matrix#VerticesAndFieldSpecies)) such that for each $sp \in Spec$ the collection of [[Feynman propagators]] the corresponding field species has a well-defined [[mass dimension]] $dim(sp)$ (def. \ref{ScalingTransformations})

Then the [[action]] of the [[group]] $RG \coloneqq (\mathbb{R}_+, \cdot)$ of [[scaling transformations]] (def. \ref{ScalingTransformations}) is a [[renormalization group flow]] in the sense of [this prop.](renormalization+group+flow#FlowRenormalizationGroup).

=--

([Dütsch 18, exercise 3.20](#Duetsch18))


+-- {: .proof}
###### Proof

It is clear that rescaling preserves [[causal order]] and the [[renormalization condition]] of "field indepencen".

The condition we need to check is that for $A_1, A_2 \in PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]$ two [[microcausal polynomial observables]]  we have for any $\rho, \rho_{vac} \in \mathbb{R}_+$ that

$$
  \sigma_\rho
  \left(
    A_1 \star_{H, \rho^{-1} \rho_{vac} c} A_2
  \right)
  \;=\;
  \sigma_\rho(A_1)
    \star_{H,\rho_{vac}}
  \sigma_\rho(A_2)
  \,.
$$

By the assumption of decomposition into free field species $sp \in Spec$, it is sufficient to check this for each species $\Delta_{H,sp}$.
Moreover, by the nature of the [[star product]] on [[polynomial observables]], which is given by iterated contractions with the [[Wightman propagator]], it is sufficient to check this for one such contraction.

Observe that the scaling behaviour of the [[Wightman propagator]] $\Delta_{H,m}$ is the same as the behaviour (eq:FeynmanPropagatorScalingBehaviour) of the correspponding [[Feynman propagator]]. With this we directly compute as follows:

$$
  \begin{aligned}
    \sigma_\rho (\mathbf{\Phi}(x))
     \star_{F, \rho_{vac} m}
    \sigma_\rho (\mathbf{\Phi}(y)
    & =
    \rho^{-2 dim }
    \mathbf{\Phi}(\rho^{-1} x)
      \star_{F, \rho_{vac} m}
    \mathbf{\Phi}(\rho^{-1} y)
    \\
    & =
    \rho^{-2 dim }
    \Delta_{F, \rho_{vac} m}(\rho^{-1}(x-y))
    \\
    & =
    \Delta_{F, \rho^{-1}\rho_{vac}m }(x,y) \mathbf{1}
    \\
    & =
    rg_{\rho}\left(
     \Delta_{F, \rho^{-1}\rho_{vac}m }(x,y) \mathbf{1}
    \right)
    \\
    & =
    rg_{\rho}
    \left(
      \mathbf{\Phi}(x)
        \star_{F, \rho^{-1} \rho_{vac} m}
      \mathbf{\Phi}(y)
    \right)
  \end{aligned}
  \,.
$$

=--

## Related concepts

* [[Wilsonian RG]]

* [[gauge coupling unification]]

* [[threshold correction]]

## References

The original informal discussion for RG-flow along [[scaling transformations]] is due to

* {#GellMannLow54} [[Murray Gell-Mann]] and F. E. Low, _Quantum Electrodynamics at Small Distances_, Phys. Rev. 95 (5) (1954), 1300–1312 ([pdf](http://www.fafnir.phyast.pitt.edu/py3765/GellManLow.pdf))

* {#Callan70} [[Curtis Callan]], _Broken Scale Invariance in Scalar Field Theory_, Phys. Rev. D 2, 1541, 1970 ([doi:10.1103/PhysRevD.2.1541](https://doi.org/10.1103/PhysRevD.2.1541))

* {#Symanzik70} [[Kurt Symanzik]],  _Small distance behaviour in field theory and power counting_, Communications in Mathematical Physics. 18 (3): 227–246 ([doi:10.1007/BF01649434](https://doi.org/10.1007/BF01649434))

Formulation in the rigorous context of [[causal perturbation theory]]/[[pAQFT]], via the [[main theorem of perturbative renormalization]], is due to

* {#BrunettiDuetschFredenhagen09} [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](https://arxiv.org/abs/0901.2038))

reviewed in

* {#Duetsch18} [[Michael Dütsch]], section 3.5.3 of _[[From classical field theory
to perturbative quantum field theory]]_, 2018

[[!redirects renormalization group flows]]

[[!redirects rg-flow]]
[[!redirects rg-flows]]

[[!redirects rg flow]]
[[!redirects rg flows]]

[[!redirects RG-flow]]
[[!redirects RG-flows]]

[[!redirects RG flow]]
[[!redirects RG flows]]


[[!redirects Gell-Mann-Low renormalization cocycle]]
[[!redirects Gell-Mann-Low renormalization cocycles]]

[[!redirects Gell-Mann-Low cocycle]]
[[!redirects Gell-Mann-Low cocycles]]

[[!redirects Gell-Mann-Low renormalization group]]
[[!redirects Gell-Mann-Low renormalization groups]]

[[!redirects mass dimension]]
[[!redirects mass dimensions]]


[[!redirects running coupling constant]]
[[!redirects running coupling constants]]

[[!redirects running of the coupling constant]]
[[!redirects running of the coupling constants]]

