+-- {: .num_defn #CauchySurface}
###### Definition
**([[Cauchy surface]])**

Given a [[Lagrangian field theory]] $(E, \mathbf{L})$ on a [[spacetime]] $\Sigma$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}), then a
_[[Cauchy surface]]_ is a [[submanifold]] $\Sigma_p \hookrightarrow \Sigma$ such that the
restriction map from the [[on-shell]] [[space of field histories]] $\Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}$
(eq:OnShellFieldHistories) to the space $\Gamma_{\Sigma_p}(E)_{\delta_{EL}\mathbf{L} = 0}$ (eq:OnShellFieldHistoriesInHigherCodimension) of on-shell field histories
restricted to the [[infinitesimal neighbourhood]] of $\Sigma_p$ (example \ref{InfinitesimalNeighbourhood}) is an [[isomorphism]]:

$$
  \label{CauchySurfaceIsomorphismOnHistorySpace}
  \Gamma_\Sigma(E)_{\delta_{EL} \mathbf{L} = 0 }
    \underoverset{\simeq}{(-)\vert_{N_\Sigma \Sigma_p}}{\longrightarrow}
  \Gamma_{\Sigma_p}(E)_{\delta_{EL}\mathbf{L} = 0}
  \,.
$$

=--


+-- {: .num_defn #PhaseSpaceAssociatedWithCauchySurface}
###### Definition
**([[phase space]] associated with a [[Cauchy surface]])**

Given a [[Lagrangian field theory]] $(E, \mathbf{L})$ on a [[spacetime]] $\Sigma$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
and given a [[Cauchy surface]] $\Sigma_p \hookrightarrow \Sigma$ (def. \ref{CauchySurface})
then the corresponding _[[phase space]]_ is

1. the [[super smooth set]] $\Gamma_{\Sigma_p}(E)_{\delta_{EL}\mathbf{L} = 0}$ (eq:OnShellFieldHistoriesInHigherCodimension)
   of [[on-shell]] [[field histories]] restricted to the [[infinitesimal neighbourhood]] of $\Sigma_p$;

1. equipped with the [[differential 2-form]] (as in def. \ref{DifferentialFormsOnDiffeologicalSpaces})

   $$
     \label{TransgressionOfPresymplecticCurrentToCauchySurface}
     \omega_{\Sigma_p}
     \;\coloneqq\;
     \tau_{\Sigma_p}\left(\Omega_{BFV}\right)
     \;\in\;
     \Omega^2\left(
       \Gamma_{\Sigma_p}(E)_{\delta_{EL}\mathbf{L} = 0}
     \right)
   $$

   which is the [[transgression of variational differential forms|transgression]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces})
   of the [[presymplectic current]] $\Omega_{BFV}$ (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime})
   to $\Sigma_p$.

   This $\omega_{\Sigma_p}$ is a [[closed differential form]] in the sense of def. \ref{DifferentialFormsOnDiffeologicalSpaces},
   due to prop. \ref{TransgressionOfVariationaldifferentialFormsCompatibleWithVariationalDerivative}
   and using that $\Omega_{BFV} = \delta \Theta_{BFV}$ is closed by definition (eq:PresymplecticCurrent).
   As such this is called the _[[presymplectic form]]_ on the phase space.

=--


+-- {: .num_example #EvaluationOfTransgressedVariationalFormsOnTangentVectorsForFreeFieldTheory}
###### Example
**(evaluation of [[transgression of variational differential forms|transgressed variational form]] on [[tangent vectors]] for [[free field theory]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) which is [[free field theory|free]] (def. \ref{FreeFieldTheory}) hence
whose [[field bundle]] is a some [[smooth vector bundle|smooth]] [[super vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle})
and whose [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] is [[linear differential equation|linear]].
Then the [[synthetic differential geometry|synthetic]] [[tangent bundle]] (def. \ref{TangentBundleSynthetic}) of the [[on-shell]] [[space of field histories]] $\Gamma_{\Sigma}(E)_{\delta_{EL}\mathbf{L} = 0}$ (eq:OnShellFieldHistories)
with spacelike compact support (def \ref{CompactlySourceCausalSupport})
is canonically identified with the [[Cartesian product]] of this [[super smooth set]] with itself

$$
  T\left(
    \Gamma_{\Sigma,scp}(E)_{\delta_{EL} \mathbf{L} = 0}
  \right)
  \;\simeq\;
  \left(\Gamma_{\Sigma,scp}(E)_{\delta_{EL} \mathbf{L} = 0}\right)
  \times
  \left(\Gamma_{\Sigma,scp}(E)_{\delta_{EL} \mathbf{L} = 0}\right)
  \,.
$$

With field coordinates as in example \ref{TrivialVectorBundleAsAFieldBundle}, we may expand the
[[presymplectic current]] as

$$
  \Omega_{BFV}
  =
  \left(\Omega_{BFV}\right)^{\mu_1, \cdots, \mu_{k_1}, \nu_1, \cdots, \nu_{k_2}, \kappa}_{a_1 a_2}
  \delta \phi^{a_1}_{\mu_1 \cdots \mu_k} \wedge \delta \phi^{a_2}_{\nu_1 \cdots \nu_{k_2}}
  \wedge
  \iota_{\partial_\kappa} dvol_\Sigma
  \,,
$$

where the components $\Omega_{BFV}_{a_1 a_2}^{\mu_1, \cdots, \mu_{k_1}, \nu_1, \cdots, \nu_{k_2}, \kappa}$
are smooth functions on the [[jet bundle]].

Under these identifications the value of the [[presymplectic form]] $\omega_{\Sigma_p}$ (eq:TransgressionOfPresymplecticCurrentToCauchySurface)
on two [[tangent vectors]] $\vec \Phi_1, \vec \Phi_2 \in \Gamma_{\Sigma,scp}(E)$
at a point $\Phi_1, \Phi_2 \in \Gamma_{\Sigma,scp}(E)$ is

$$
  \omega_{\Sigma_p}(\vec \Phi_1, \vec \Phi_2)
  \;=\;
  \underset{\Sigma_p}{\int}
  \left(\Omega_{BFV}\right)^{\mu_1, \cdots, \mu_{k_1}, \nu_1, \cdots, \nu_{k_2}, \kappa}_{a_1 a_2}(\Phi_1(x), \Phi_2(x))
  \left(
  \frac{\partial}{\partial x^{\mu_1}}
  \cdots
  \frac{\partial}{\partial x^{\mu_{k_1}}}
  \vec \Phi_1(x)
  \right)
  \left(
  \frac{\partial}{\partial x^{\nu_1}}
  \cdots
  \frac{\partial}{\partial x^{\nu_{k_2}}}
  \vec \Phi_2(x)
  \right)
  \,
  \iota_{\partial_\kappa} dvol_\Sigma(x)
  \,.
$$

=--


+-- {: .num_example #PresymplecticFormForFreeRealScalarField}
###### Example
**([[presymplectic form]] for [[free field|free]] [[real scalar field]])**

Consider the [[Lagrangian field theory]] for the [[free field|free]] [[real scalar field]]
from example \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}.

Under the identification of example \ref{EvaluationOfTransgressedVariationalFormsOnTangentVectorsForFreeFieldTheory} the [[presymplectic form]] on the [[phase space]] (def. \ref{PhaseSpaceAssociatedWithCauchySurface})
associated with a [[Cauchy surface]] $\Sigma_p \hookrightarrow \Sigma$
is given by

$$
  \begin{aligned}
    \omega_{\Sigma_p}(\vec \Phi_1, \vec\Phi_2)
    & =
    \int_{\Sigma_{p}}
    \left(
      \frac{\partial \vec \Phi_1}{\partial x^\mu}(x) \vec \Phi_2(x)
      -
      \vec \Phi_1(x) \frac{\partial \vec \Phi_2}{\partial x^\mu}(x)
    \right)
    \eta^{\mu \nu}
    \iota_{\partial_\mu} dvol_{\Sigma_{p}}(x)
    \\
    & =
    \underset{\Sigma_p}{\int} K(\vec \Phi_1, \vec \Phi_2)
    \,.
  \end{aligned}
$$

Here the first equation follows via example \ref{EvaluationOfTransgressedVariationalFormsOnTangentVectorsForFreeFieldTheory} from the form of $\Omega_{BFV}$ from example \ref{FreeScalarFieldEOM},
while the second equation
identifies the integrand as the witness $K$ for the [[formally adjoint differential operator|formally self-adjointness]] of the [[Klein-Gordon equation]] from example \ref{FormallySelfAdjointKleinGordonOperator}.

=--


+-- {: .num_example #PresymplecticFormForFreeDiracField}
###### Example
**([[presymplectic form]] for [[free field theory|free]] [[Dirac field]])**

Consider the [[Lagrangian field theory]] of the [[free field theory|free]] [[Dirac field]] (example \ref{LagrangianDensityForDiracField}). 

Under the identification of example \ref{EvaluationOfTransgressedVariationalFormsOnTangentVectorsForFreeFieldTheory} the [[presymplectic form]] on the [[phase space]] (def. \ref{PhaseSpaceAssociatedWithCauchySurface}) associated with a [[Cauchy surface]] $\Sigma_p \hookrightarrow \Sigma$
is given by

$$
  \begin{aligned}
    \omega_{\Sigma_p}(\theta_1 \vec \Psi_1, \theta_2 \vec\Psi_2)
    & =
    \int_{\Sigma_{p}}
    \left(
      \overline{\theta_1 \vec \psi_1}\gamma^\mu \left( \theta_2 \vec \Psi_2 \right)
    \right)
    \iota_{\partial_\mu} dvol_{\Sigma_{p}}(x)
    \\
    & =
    \underset{\Sigma_p}{\int} K(\vec \Phi_1, \vec \Phi_2)
    \,.
  \end{aligned}
$$

Here the first equation follows via example \ref{EvaluationOfTransgressedVariationalFormsOnTangentVectorsForFreeFieldTheory} from the form of $\Omega_{BFV}$ from example \ref{PresymplecticCurrentDiracField},
while the second equation
identifies the integrand as the witness $K$ for the [[formally adjoint differential operator|formally self-adjointness]] of the [[Dirac equation]] from example \ref{DiracOperatorOnDiracSpinorsIsFormallySelfAdjointDifferentialOperator}.

=--


+-- {: .num_prop #CovariantPhaseSpace}
###### Proposition
**([[covariant phase space]])**

Consider $(E, \mathbf{L})$ a [[Lagrangian field theory]] on a [[spacetime]] $\Sigma$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

Let

$$
  \Sigma_{tra} \overset{tra}{\hookrightarrow} \Sigma
$$

be a [[submanifold]] [[manifold with boundary|with two boundary components]]
$\partial \Sigma_{tra} = \Sigma_{in} \sqcup \Sigma_{out}$ ,
both of which are [[Cauchy surfaces]] (def. \ref{CauchySurface}).

Then the corresponding inclusion diagram

$$
  \array{
    && \Sigma_{tra}
    \\
    & {}^{\mathllap{in}}\nearrow && \nwarrow^{\mathrm{out}}
    \\
    \Sigma_{in}
    && &&
    \Sigma_{out}
  }
$$

induces a [[Lagrangian correspondence]] between the associated [[phase spaces]] (def. \ref{PhaseSpaceAssociatedWithCauchySurface})

$$
  \array{
    && \Gamma_{\Sigma_{tra}}(E)_{\delta_{EL} \mathbf{L} = 0}
    \\
    & {}^{\mathllap{ (-)\vert_{in} }}\swarrow && \searrow^{\mathrlap{ (-)\vert_{out} }}
    \\
    \Gamma_{\Sigma^{(in)}}(E)_{\delta_{EL}\mathbf{L}= 0}
    && &&
    \Gamma_{\Sigma^{(out)}}(E)_{\delta_{EL}\mathbf{L}= 0}
    \\
    & {}_{\mathllap{\omega_{in}}}\searrow && \swarrow_{\mathrlap{\omega_{out}}}
    \\
    && \mathbf{\Omega}^{2}
  }
$$

in that the [[pullback of differential forms|pullback]] of the
two [[presymplectic forms]] (eq:TransgressionOfPresymplecticCurrentToCauchySurface) coincides on the
space of field histories:

$$
  \left( (-)\vert_{in}\right)^\ast\left( \omega_{in}\right)
  \;=\;
  \left( (-)\vert_{out} \right)^\ast \left( \omega_{out} \right)
  \phantom{AAAA}
  \in
  \Omega^2
  \left(
    \Gamma_{\Sigma_{tra}}(E)_{\delta_{EL} \mathbf{L} = 0}
  \right)
  \,.
$$

Hence there is a well defined [[presymplectic form]]

$$
  \omega \in \Omega^2\left(  \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L}} = 0 \right)
$$

on the genuine [[space of field histories]], given by $\omega \coloneqq i^\ast \omega_{\Sigma_p}$
for any Cauchy surface $\Sigma_p \overset{i}{\hookrightarrow} \Sigma$. This [[presymplectic smooth space]]

$$
  \left(
    \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L}}
    \,,\,
    \omega
  \right)
$$

is therefore called the _[[covariant phase space]]_ of the [[Lagrangian field theory]] $(E,\mathbf{L})$.

=--


+-- {: .proof}
###### Proof

By prop. \ref{HorizontalDerivativeOfPresymplecticCurrentVanishesOnShell} the
total spacetime derivative $d \Omega_{BFV}$ of the [[presymplectic current]] vanishes [[on-shell]]:

$$
  d \Omega_{BFV} = - \delta \delta_{EL} \mathbf{L}
$$

in that the [[pullback of differential forms|pullback]] (def. \ref{PullbackOfDifferential1FormsOnCartesianSpaces})
along the [[shell]] inclusion $\mathcal{E} \overset{i_{\mathcal{E}}}{\hookrightarrow} J^\infty_\Sigma(E)$ (eq:ShellInJetBundle)
vanishes:

$$
  \begin{aligned}
    (i_{\mathcal{E}})^\ast
    \left(
     d \Omega_{BFV}
    \right)
    & =
    - (i_{\mathcal{E}})^\ast
    \left(
     \delta \delta_{EL} \mathcal{L}
    \right)
    \\
    & =
    - \delta
    \underset{
      = 0
    }{
    \underbrace{
    (i_{\mathcal{E}})^\ast
    \left(
      \delta_{EL} \mathbf{L}
    \right)
    }
    }
    \\
    & = 0
  \end{aligned}
$$

This implies that the transgression of $d \Omega_{BFV}$ to
the [[on-shell]] [[space of field histories]] $\Gamma_{\Sigma_{tra}}(E)_{\delta_{EL}\mathbf{L} = 0}$ vanishes
(since by definition (eq:EquationOfMotionEL) that involves pulling back through the shell inclusion)

$$
  \tau_{\Sigma_{tra}}(d \Omega_{BFV}) = 0
  \,.
$$

But then the claim follows with prop. \ref{TransgressionOfVariationaldifferentialFormsCompatibleWithVariationalDerivative}:

$$
  \begin{aligned}
    0
    & =   \tau_{\Sigma_{tra}}(d \Omega_{BFV})
    \\
    & = ((-)\vert_{\Sigma_{tra}})^\ast \tau_{\partial \Sigma_{tra}} \Omega_{BFV}
    \,.
  \end{aligned}
$$

=--


+-- {: .num_theorem #PPeierlsBracket}
###### Theorem
**([[polynomial Poisson algebra|polynomial Poisson bracket]] on [[covariant phase space]] -- the [[Peierls bracket]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) which is

1. a [[free field theory|free]] (def. \ref{FreeFieldTheory})

1. whose [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] $P \Phi = 0$ (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}) is

   1. [[formally adjoint differential operator|formally self-adjoint]] or anti self-adjoint (def. \ref{FormallyAdjointDifferentialOperators})
      such that the integral over the witness $K$ (eq:FormallyAdjointDifferentialOperatorWitness) is the
      [[presymplectic form]] (eq:TransgressionOfPresymplecticCurrentToCauchySurface): $\omega_{\Sigma_p} = \underset{\Sigma_p}{\int} K$

   1. [[Green hyperbolic differential operator|Green hyperbolic]] (def. \ref{GreenHyperbolicDifferentialOperator}).

Then the map

$$
  \array{
    LinObs(E_{scp},\mathbf{L})^{reg}
     &\coloneqq&
    \Gamma_{\Sigma,cp}(\tilde E)
     &\overset{\phantom{AAA}}{\hookrightarrow}&
    LinObs(E_{scp},\mathbf{L})
    \\
    && \alpha^\ast &\mapsto& \left( \Phi \mapsto \underset{\Sigma}{\int} \alpha^\ast \cdot \Phi , dvol_\Sigma \right)
  }
$$

from compactly supported sections of the [[dual vector bundle]] of the [[field bundle]] (def. \ref{CompactlySourceCausalSupport}) to linear observables on spatially compactly supported on-shell field histories (eq:LinearObservablesOnSpatiallyCompactlySupportedOnShellFieldHistories) is an injection. We call the subspace of linear observables defined thereby that of _regular_ linear observables.

In particular then the [[causal Green function]] $\mathrm{G}_P$ (def. \ref{AdvancedAndRetardedGreenFunctions}) defines
a linear map

$$
  \mathrm{G}_P
  \;\colon\;
  LinObs(E_{scp},\mathbf{L})^{reg}
      \overset{}{\longrightarrow}
  \Gamma_{\Sigma,scp}(E)_{\delta_{EL}\mathbf{L} = 0}
$$

from regular linear observables of on-shell field histories with spatially compact support.

For every [[Cauchy surface]] $\Sigma_p \hookrightarrow \Sigma$ this is an inverse to the
[[presymplectic form]] $\omega_{\Sigma_p}$ (def. \ref{PhaseSpaceAssociatedWithCauchySurface})
in that, under the identification of tangent vectors to field histories from example \ref{EvaluationOfTransgressedVariationalFormsOnTangentVectorsForFreeFieldTheory}, we have that the composite

$$
  \label{ForGreenHyperbolicFreeFieldTheoryCausalGreenFunctionIsInverseToPresymplecticFormOnRegularLinearObservables}
  \array{
    \omega_{\Sigma_p}(\mathrm{G}(-),(-))
    \;=\;
    ev
    &\colon&
    LinObs(E_{scp},\mathbf{L})^{reg} \otimes \Gamma_{\Sigma,scp}(E)
      &\longrightarrow&
    \mathbb{C}
    \\
    && (A, \Phi) &\mapsto& A(\Phi)
  }
$$

equals the [[evaluation map]] of observables on field histories.

This means that for every [[Cauchy surface]] $\Sigma_p$ the [[presymplectic form]] $\omega_{\Sigma_p}$ restricts to a _[[symplectic form]]_
on regular linear observables. The corresponding _[[Poisson bracket]]_ is defined to be

$$
  \left\{
    -,-
  \right\}_{\Sigma_p}
  \;\coloneqq\;
  \omega_{\Sigma_p}(\mathrm{G}(-), \mathrm{G}(-))
  \;\colon\;
  LinObs(E_{scp},\mathbf{L})^{reg} \otimes LinObs(E_{scp},\mathbf{L})^{reg}
    \longrightarrow
  \mathbb{R}
  \,.
$$

Moreover, equation (eq:ForGreenHyperbolicFreeFieldTheoryCausalGreenFunctionIsInverseToPresymplecticFormOnRegularLinearObservables)
implies that this is the _covariant [[Poisson bracket]]_ in the sense of the [[covariant phase space]] (def. \ref{CovariantPhaseSpace})
in that it does not actually depend on the choice of [[Cauchy surface]].

Finally, an equivalent expression for the Poisson bracket that makes its independence from the choice of Cauchy surface
manifest is the _$P$-[[Peierls bracket]]_ given by

$$
  \array{
    LinObs(E_{scp},\mathbf{L})^{reg} \otimes LinObs(E_{scp},\mathbf{L})^{reg}
      &\overset{\{-,-\}}{\longrightarrow}&
    \mathbb{R}
    \\
    (\alpha^\ast, \beta^\ast)
      &\mapsto&
    \underset{\Sigma}{\int}
    \mathrm{G}(\alpha^\ast) \cdot \beta^\ast
      \,
    dvol_\Sigma
  }
$$

where on the left

$$
  \alpha^\ast, \beta^\ast \in \Gamma_{\Sigma,cp}(E^\ast) \simeq LinObs(E_{scp},\mathbf{L})^{reg}
  \,.
$$

Hence under the given assumptions, for every Cauchy surface the [[Poisson bracket]]
associated with that Cauchy surface equals the invariantly ("covariantly") defined [[Peierls bracket]]

$$
  \{-,-\}_{\Sigma_p} = \{-,-\}
  \,.
$$

=--

([Khavkine 14, lemma 2.5](Green+hyperbolic+partial+differential+equation#Khavkine14))



+-- {: .num_example #PeierlsBracketEistsForScalarFieldAndDiracField}
###### Example
**([[scalar field]] and [[Dirac field]] have [[covariant phase space|covariant]] [[Peierls-Poisson bracket]])**

Examples of [[free field theor|free]] [[Lagrangian field theories]] for which the assumptions of theorem
\ref{PPeierlsBracket} are satisfied,  so that the covariant [[Poisson bracket]] exists in the form
of the [[Peierls bracket]] include

* the [[free field theory|free]] [[real scalar field]] (example \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime});

* the [[free field theory|free]] [[Dirac field]] (example \ref{LagrangianDensityForDiracField}).

For the [[free field theory|free]] [[scalar field]] this is the statement of example \ref{GreenHyperbolicKleinGordonEquation} 
with example \ref{PresymplecticFormForFreeRealScalarField}, while for the [[Dirac field]] this is the
statement of example \ref{GreenHyperbolicDiracOperator} with example \ref{PresymplecticFormForFreeDiracField}.

=--

For the [[free field theory|free]] [[electromagnetic field]] (example \ref{ElectromagnetismLagrangianDensity})
the assumptions are violated. But in the discuussion of _[Gauge fixing](#GaugeFixing)_, below,
we wil find that for an equivalent re-incarnation of the electromagnetic field, they are met after all.
