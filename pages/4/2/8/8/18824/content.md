## Phase space
  {#PhaseSpace}

It might seem that with the construction of the [[local observables]] (def. \ref{LocalObservables})
on the [[on-shell]] [[space of field histories]] (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime})
the [[field theory]] defined by a [[Lagrangian density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) has been completely analyzed:
This data specifies, in principle, which [[field histories]] are realized, and which [[observable]] properties these have.

In particular, if the [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime})
admit [[Cauchy surfaces]] (def. \ref{CauchySurface} below), i.e. spatial [[codimension]] 1 slices of [[spacetimes]]
such that a [[field history]] is uniquely specified already by its restriction to the [[infinitesimal neighbourhood]]
of that spatial slice, then a sufficiently complete collection of [[local observables]] whose spacetime support (def. \ref{SpacetimeSupport})
[[covering|covers]] that Cauchy surface allows to _predict_ the evolution of the field histories through time
from that Cauchy surface.

This is all what one might think a theory of physical fields should accomplish, and in fact this is essentially
all that was thought to be required of a theory of nature from about [[Isaac Newton]]'s time to about [[Max Planck]]'s time.

But we have seen that a remarkable aspect of [[Lagrangian field theory]] is that the [[de Rham differential]] of the [[local Lagrangian density]] $\mathbf{L}$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) decomposes into
_two_ kinds of [[variational differential forms]] (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}),
one of which is the [[Euler-Lagrange form]] which determines the [[equations of motion]] (eq:EulerLagrangeEquationGeneral).

However, there is a second contribution: The _[[presymplectic current]]_ $\Omega_{BFV} \in \Omega^{p,2}_{\Sigma}(E)$ (eq:PresymplecticCurrent).
Since this is of horizontal degree $p$,
its [[transgression of variational differential forms|transgression]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces}) implies a further structure on the [[space of field histories]]
 restricted to [[spacetime]] [[submanifolds]] of dimension $p$ (i.e. of spacetime "[[codimension]] 1").
There may be such submanifolds such that this restriction to their [[infinitesimal neighbourhood]] (example \ref{InfinitesimalNeighbourhood}) does not actually change the [[on-shell]] [[space of field histories]],
these are called the _[[Cauchy surfaces]]_ (def. \ref{CauchySurface} below).

By the [[Hamiltonian Noether theorem]] (prop. \ref{HamiltonianDifferentialForms}) the [[presymplectic current]] induces [[infinitesimal symmetries]] acting on [[field histories]] and [[local observables]], given by the [[Poisson bracket Lie n-algebra|local Poisson bracket]] (prop. \ref{LocalPoissonBracket}).
The [[transgression of variational differential forms|transgression]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces}) of the [[presymplectic current]]
to these [[Cauchy surfaces]] yields the corresponding [[infinitesimal symmetry]] group acting on the [[on-shell]] [[field histories]],
whose [[Lie bracket]] is the _[[Poisson bracket]]_ pairing on [[on-shell]] [[observables]] (example \ref{EvaluationOfTransgressedVariationalFormsOnTangentVectorsForFreeFieldTheory} below). This data, the [[on-shell]] [[space of field histories]] on the [[infinitesimal neighbourhood]] of a [[Cauchy surface]] equipped with [[infinitesimal symmetry]] exhibited by the [[Poisson bracket]] is called the _[[phase space]]_ of the theory (def. \ref{PhaseSpaceAssociatedWithCauchySurface}) below.

In fact if enough [[Cauchy surfaces]] exist, then the [[presymplectic forms]] associated with
any one choice turn out do agree after [[pullback of differential forms|pullback]] to the full [[on-shell]] [[space of field histories]], exhibiting this as the _[[covariant phase space]]_ of the theory (prop. \ref{CovariantPhaseSpace} below) which is hence manifestly independent of aa choice of space/time splitting. Accordingly, also the [[Poisson bracket]] on [[on-shell]] [[observables]] exists in a covariant form; for [[free field theories]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations of motion]] (def. \ref{GreenHyperbolicDifferentialOperator}) this is called the _[[Peierls-Poisson bracket]]_ (theorem \ref{PPeierlsBracket} below). The [[integral kernel]] for this [[Peierls-Poisson bracket]] is called the _[[causal propagator]]_ (prop. \ref{GreenFunctionsAreContinuous}).
Its "[[normal ordered product|normal ordered]]" or "[[positive real number|positive]] [[frequency]] component", called the _[[Hadamard propagator]]_ (def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime} below) as well as the corresponding [[time-ordered product|time-ordered]] variant, called the _[[Feynman propagator]]_ (def. \ref{FeynmanPropagatorForKleinGordonEquationOnMinkowskiSpacetime} below), which we discuss in detail in _[Propagators](#Propagators)_ below,
control the [[causal perturbation theory]] for constructing [[perturbative quantum field theory]] by [[deformation quantization|deforming]]
the commutative pointwise product of [[on-shell]] [[observables]] to a [[non-commutative algebra|non-commutative product]] governed to first order by the [[Peierls-Poisson bracket]].

To see how such a [[deformation quantization]] comes about conceptually from the [[phase space]] strucure,
notice from the basic principles of [[homotopy theory]] that given any [[structure]] on a [[space]]
which is [[invariant]] with respect to a [[symmetry group]] [[action|acting]] on the space
(here: the [[presymplectic current]])
then the true structure at hand is the [[homotopy quotient]] of that [[space]] by that [[symmetry group]].
We will explain this further below. This here just to point out that the [[homotopy quotient]] of the
[[phase space]] by the [[Hamiltonian vector field|infinitesimal symmetries of the presymplectic current]]
is called the _[[symplectic groupoid]]_ and that the _true_ [[algebra of observables]] is hence
the ([[polarization|polarized]]) [[groupoid convolution algebra|convolution algebra of functions]]
on this groupoid. This turns out to the "[[algebra of quantum observables]]" and the passage from the
naive [[local observables]] on [[presymplectic manifold|presymplectic]] [[phase space]] to
this non-commutative algebra of functions on its [[homotopy quotient]] to the [[symplectic groupoid]]
is called _[[quantization]]_. This we discuss in much detail [below](#Quantization); for the
moment this is just to motivate why the [[covariant phase space]] is the crucial construction to be
extracted from a [[Lagrangian field theory]].

$\,$

$$
  \array{
  \left\{
    \array{
      \text{on-shell space}
      \\
      \text{ of field histories}
      \\
      \text{restricted to}
      \\
      \text{Cauchy surface}
    }
  \right\}
   &\overset{\array{ \text{homotopy} \\ \text{quotient} \\ \text{by} \\ \text{infinitesimal} \\ \text{symmetries} }}{\longrightarrow}
   &
   \left\{
       \array{
         \text{covariant}
         \\
         \text{phase space}
       }
   \right\}
   &\overset{ \array{\text{Lie algebra} \\ \text{of functions} } }{\longrightarrow}&
   \left\{
      \array{
        \text{Poisson algebra}
        \\
        \text{of observables}
      }
   \right\}
   \\
   &
     \searrow
   &
     \Big\downarrow{}^\mathrlap{{\text{Lie integration}}}
   &&
     {}^{\mathllap{quantization}}\Big\downarrow
   \\
   && \left\{
      \array{
        \text{symplectic}
        \\
        \text{groupoid}
      }
   \right\}
   &
   \overset{
      \array{
         \text{polarized}
         \\
         \text{convolution}
         \\
         \text{algebra}
      }
   }{\longrightarrow}&
   \left\{
      \array{
         \text{quantum algebra}
         \\
         \text{of observables}
      }
   \right\}
   }
$$

$\,$

We now discuss these topics:

$\,$

* _[Covariant phase space](#PreymplecticPhaseSpace)_

* _[BV-Resolution of the covariant phase space](#BVResolutionOfTheCovariantPhaseSpace)_

* _[Hamiltonian local observables](#HamiltonianLocalObservablesOnACauchySurface)_

$\,$

**Covariant phase space**
 {#PreymplecticPhaseSpace}

+-- {: .num_defn #CauchySurface}
###### Definition
**([[Cauchy surface]])**

Given a [[Lagrangian field theory]] $(E, \mathbf{L})$ on a [[spacetime]] $\Sigma$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}), then a
_[[Cauchy surface]]_ is a [[submanifold]] $\Sigma_p \hookrightarrow \Sigma$ (def. \ref{SmoothManifoldInsideDiffeologicalSpaces}) such that the
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

   which is the distributional [[transgression of variational differential forms|transgression]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces})
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

where the components $(\Omega_{BFV})_{a_1 a_2}^{\mu_1, \cdots, \mu_{k_1}, \nu_1, \cdots, \nu_{k_2}, \kappa}$
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

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) such that

1. it is a [[free field theory]] (def. \ref{FreeFieldTheory})

1. whose [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] $P \Phi = 0$ (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}) is

   1. [[formally adjoint differential operator|formally self-adjoint]] or [[formally adjoint differential operator|formally anti self-adjoint]] (def. \ref{FormallyAdjointDifferentialOperators}) such that

      * the integral over the witness $K$ (eq:FormallyAdjointDifferentialOperatorWitness) is the
      [[presymplectic form]] (eq:TransgressionOfPresymplecticCurrentToCauchySurface): $\omega_{\Sigma_p} = \underset{\Sigma_p}{\int} K$;

   1. [[Green hyperbolic differential operator|Green hyperbolic]] (def. \ref{GreenHyperbolicDifferentialOperator}).

Write

$$
  \mathrm{G}_P
    \;\colon\;
    LinObs(E_{scp},\mathbf{L})^{reg}
        \overset{\mathrm{G}_P}{\longrightarrow}
    \Gamma_{\Sigma,scp}(E)_{\delta_{EL}\mathbf{L} = 0}
$$

for the linear map
from regular linear field observables (def. \ref{RegularLinearFieldObservables}) to on-shell [[field histories]] with spatially compact support (def. \ref{CompactlySourceCausalSupport}) given under the identification (eq:RegularLinearObservablesAreCompactlySupportedSectionsModuloImageOfP)
by the [[causal Green function]] $\mathrm{G}_P$ (def. \ref{AdvancedAndRetardedGreenFunctions}).

Then for every [[Cauchy surface]] $\Sigma_p \hookrightarrow \Sigma$ (def. \ref{CauchySurface}) this map is an inverse to the
[[presymplectic form]] $\omega_{\Sigma_p}$ (def. \ref{PhaseSpaceAssociatedWithCauchySurface})
in that, under the identification of tangent vectors to field histories from example \ref{EvaluationOfTransgressedVariationalFormsOnTangentVectorsForFreeFieldTheory}, we have that the composite

$$
  \label{ForGreenHyperbolicFreeFieldTheoryCausalGreenFunctionIsInverseToPresymplecticFormOnRegularLinearObservables}
  \array{
    \omega_{\Sigma_p}(\mathrm{G}_P(-),(-))
    \;=\;
    ev
    &\colon&
    LinObs(E_{scp},\mathbf{L})^{reg} &\otimes& \Gamma_{\Sigma,scp}(E)
      &\longrightarrow&
    \mathbb{C}
    \\
    && (A &,& \Phi) &\mapsto& A(\Phi)
  }
$$

equals the [[evaluation map]] of observables on field histories.

This means that for every [[Cauchy surface]] $\Sigma_p$ the [[presymplectic form]] $\omega_{\Sigma_p}$ restricts to a _[[symplectic form]]_
on regular linear observables. The corresponding _[[Poisson bracket]]_ is

$$
  \left\{
    -,-
  \right\}_{\Sigma_p}
  \;\coloneqq\;
  \omega_{\Sigma_p}(\mathrm{G}_P(-), \mathrm{G}_P(-))
  \;\;\colon\;\;
  LinObs(E_{scp},\mathbf{L})^{reg} \otimes LinObs(E_{scp},\mathbf{L})^{reg}
    \longrightarrow
  \mathbb{R}
  \,.
$$

Moreover, equation (eq:ForGreenHyperbolicFreeFieldTheoryCausalGreenFunctionIsInverseToPresymplecticFormOnRegularLinearObservables)
implies that this is the _covariant [[Poisson bracket]]_ in the sense of the [[covariant phase space]] (def. \ref{CovariantPhaseSpace})
in that it does not actually depend on the choice of [[Cauchy surface]].

An equivalent expression for the Poisson bracket that makes its independence from the choice of Cauchy surface
manifest is the _$P$-[[Peierls bracket]]_ given by

$$
  \label{ThePPeierlsBracket}
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

where on the left $\alpha^\ast, \beta^\ast \in \Gamma_{\Sigma,cp}(E^\ast) \simeq LinObs(E_{scp},\mathbf{L})^{reg}$

Hence under the given assumptions, for every Cauchy surface the [[Poisson bracket]]
associated with that Cauchy surface equals the invariantly ("covariantly") defined [[Peierls bracket]]

$$
  \{-,-\}_{\Sigma_p} = \{-,-\}
  \,.
$$

Finally this means that in terms of the [[causal propagator]] $\Delta$ (eq:CausalPropagator) the
covariant [[Peierls-Poisson bracket]] is given in [[generalized function]]-notation by

$$
  \label{CausalPropagatorPPeierlsBracket}
  \{\alpha^\ast, \beta^\ast\}
  \;=\;
  \underset{\Sigma}{\int} \underset{\Sigma}{\int}
    \alpha^\ast(x) \cdot \Delta(x,y) \cdot \beta^\ast(y)
  \, dvol_\Sigma(x)\, dvol_\Sigma(y)
$$

Therefore, while the point-evaluation field observables $\mathbf{\Phi}^a(x)$ (def. \ref{PointEvaluationObservables}) are not themselves regular observables (def. \ref{RegularLinearFieldObservables}),
the [[Peierls-Poisson bracket]] (eq:CausalPropagatorPPeierlsBracket) is induced from the
following distributional bracket between them

$$
  \left\{
    \mathbf{\Phi}^a(x)
    ,
    \mathbf{\Phi}^b(y)
  \right\}
  \;=\;
  \Delta^{a b}(x,y)
$$

with the [[causal propagator]] (eq:CausalPropagator) on the right, in that with the identification (eq:AverageOfFieldObservableIsRegularLinearObservables) the [[Peierls-Poisson bracket]] on
regular linear observables arises as follows:

$$
  \begin{aligned}
    \left\{
      \underset{\Sigma}{\int} \alpha^\ast_a(x) \mathbf{\Phi}^a(x) \, dvol_\Sigma(x)
      \,,\,
      \underset{\Sigma}{\int} \beta^\ast_b(y) \mathbf{\Phi}^b(y) \, dvol_\Sigma(y)
    \right\}
    & =
    \underset{\Sigma}{\int} \underset{\Sigma}{\int}
      \alpha^\ast_a(x)
      \underset{= \Delta^{a b}(x,y)}{
      \underbrace{
      \left\{
        \mathbf{\Phi}^a(x),
        \mathbf{\Phi}^b(y)
      \right\}
      }
      }
      \beta^\ast_b(y)
      \, dvol_\Sigma(x)\, dvol_\Sigma(y)
    \\
    & =
    \underset{\Sigma}{\int} \underset{\Sigma}{\int}
      \alpha^\ast_a(x)
      \Delta^{a b}(x,y)
      \beta^\ast_b(y)
      \, dvol_\Sigma(x)\, dvol_\Sigma(y)
  \end{aligned}
$$


=--

([Khavkine 14, lemma 2.5](Green+hyperbolic+partial+differential+equation#Khavkine14))



+-- {: .proof}
###### Proof

Consider two more Cauchy surfaces $\Sigma_p^\pm \hookrightarrow I^\pm(\Sigma) \hookrightarrow \Sigma$, in the [[future]] $I^+$ and in the [[past]] $I^-$ of $\Sigma$, respectively. Choose a [[partition of unity]] on $\Sigma$ consisting of two elements $\chi^\pm \in C^\infty(\Sigma)$ with [[support]] bounded by these Cauchy surfaces: $supp(\chi_\pm) \subset I^\pm(\Sigma^{\mp})$.

Then define

$$
  \label{SplittingOfGreenExactSequenceType}
  P_\chi
    \;\colon\;
  \Gamma_{\Sigma,scp}(E)
    \longrightarrow
  \Gamma_{\Sigma,cp}(E^\ast)
$$

by

$$
  \label{SplittingOfGreenExactSequence}
  \begin{aligned}
    P_\chi(\Phi)
      & \coloneqq
    \phantom{-} P(\chi_+ \Phi)
    \\
    & =
    -
    P(\chi_- \Phi)
    \,.
  \end{aligned}
$$

Notice that the [[support]] of the partitioned field history is in the compactly sourced future/past cone

$$
  \label{ChipmPhiIsSupportedInPastFuture}
  \chi_\pm  \Phi
  \;\in\;
  \Gamma_{\Sigma,\pm cp}(E)
$$

since $\Phi$ is supported in the compactly sourced causal cone, but that
$P(\chi_\pm \Phi)$ indeed has [[compact support]] as required by (eq:SplittingOfGreenExactSequenceType): Since $P(\Phi) = 0$, by assumption, the support is the intersection of that of $\Phi$ with that of $d \chi_\pm$, and the first is spacelike compact by assumption, while the latter is timelike compact, by definition of partition of unity.

Similarly, the equality in (eq:SplittingOfGreenExactSequence) holds because by [[partition of unity]] $P(\chi_+ \Phi) + P(\chi_-\Phi) = P((\chi_+ + \chi_-)\Phi ) = P(\Phi) = 0$.

It follows that

$$
  \label{PchiIsRightInverseToGP}
  \begin{aligned}
    \mathrm{G}_P \circ P_\chi (\Phi)
    & =
    \left(
      \mathrm{G}_{P,+} - \mathrm{G}_{P,-}
    \right) P_\chi (\Phi)
    \\
    & =
    \underset{ = \chi_+ \Phi}{\underbrace{\mathrm{G}_{P,+} P(\chi_+ \Phi)}}
    +
    \underset{ = \chi_- \Phi }{\underbrace{\mathrm{G}_{P,-} P(\chi_- \Phi)}}
    \\
    & =
    (\chi_+ + \chi_-)\Phi
    \\
    & =
    \Phi
    \,,
  \end{aligned}
$$

where in the second line we chose from the two equivalent expressions (eq:SplittingOfGreenExactSequence) such that via (eq:ChipmPhiIsSupportedInPastFuture) the defining property of the [[advanced and retarded Green functions|advanced or retarded Green function]], respectively, may be applied, as shown under the braces.

([Khavkine 14, lemma 2.1](Green+hyperbolic+differential+equation#Khavkine14))

Now we apply this to the computation of $\omega_{\Sigma_p}(\mathrm{G}_P(-),-)$:

$$
  \begin{aligned}
    \omega_{\Sigma_P}(\mathrm{G}_P(\alpha^\ast),\vec \Phi)
    & =
    \underset{\Sigma_P}{\int}  K(\mathrm{G}_P(\alpha^\ast), \vec \Phi)
    \\
    & =
    \underset{\Sigma_P}{\int}  K(\mathrm{G}_P(\alpha^\ast), \chi_+\vec \Phi)
     +
    \underset{\Sigma_P}{\int}  K(\mathrm{G}_P(\alpha^\ast), \chi_-\vec \Phi)
    \\
    & =
    \underset{I^-(\Sigma_P)}{\int}  d K(\mathrm{G}_P(\alpha^\ast), \chi_+\vec \Phi)
     -
    \underset{I^+(\Sigma_P)}{\int}  d K(\mathrm{G}_P(\alpha^\ast), \chi_-\vec \Phi)
    \\
    & =
    \underset{I^-(\Sigma_P)}{\int}
    \left(
       \underset{= 0}{
       \underbrace{
       P(\mathrm{G}_P(\alpha^\ast))}} \cdot \chi_+\vec \Phi
       \mp
       \mathrm{G}_P(\alpha^\ast) \cdot P(\chi_+ \vec \Phi)
    \right)
    dvol_\Sigma
    -
    \underset{I^+(\Sigma_P)}{\int}
    \left(
       \underset{= 0}{
       \underbrace{
       P(\mathrm{G}_P(\alpha^\ast))}} \cdot \chi_-\vec \Phi
       \mp
       \mathrm{G}_P(\alpha^\ast) \cdot P(\chi_- \vec \Phi)
    \right)
    dvol_\Sigma
    \\
    & =
    \mp
    \left(
    \underset{I^-(\Sigma_P)}{\int}
       \mathrm{G}_P(\alpha^\ast) \cdot P(\chi_+ \vec \Phi)
    dvol_\Sigma
    +
    \underset{I^+(\Sigma_P)}{\int}
       \mathrm{G}_P(\alpha^\ast) \cdot P(\chi_+ \vec \Phi)
     dvol_\Sigma
    \right)
    \\
    & =
    \underset{\Sigma}{\int} \mathrm{G}_P(\alpha^\ast) \cdot P(\chi_+ \vec \Phi) dvol_\Sigma
    \\
    & =
    \underset{\Sigma}{\int} \alpha^\ast \cdot \mathrm{G}_{P} (P (\chi_+ \vec \Phi))
    \\
    & =
    \underset{\Sigma}{\int} \alpha^\ast \cdot \vec \Phi
   \end{aligned}
$$

Here we computed as follows:

1. applied the assumption that $\omega_{\Sigma_p}(-,-) = \underset{\Sigma_p}{\int} K(-,-)$;

1. applied the above partition of unity;

1. used the [[Stokes theorem]] (prop. \ref{StokesTheorem}) for the past and the future of $\Sigma_p$, respectively;

1. applied the definition of $d K$ as the witness  of the formal (anti-) self-adjointness of $P$ (def. \ref{FormallyAdjointDifferentialOperators});

1. used $P\circ \mathrm{G}_p = 0$ on $\Gamma_{\Sigma,cp}(E^\ast)$ (def. \ref{AdvancedAndRetardedGreenFunctions}) and used (eq:SplittingOfGreenExactSequence);

1. unified the two integration domains, now that the integrands are the same;

1. used the formally (anti-)self adjointness of the Green functions (example \ref{CausalGreenFunctionOfFormallyAdjointDifferentialOperatorAreFormallyAdjoint});


1. used (eq:PchiIsRightInverseToGP).


=--

+-- {: .num_example #PeierlsBracketEistsForScalarFieldAndDiracField}
###### Example
**([[scalar field]] and [[Dirac field]] have [[covariant phase space|covariant]] [[Peierls-Poisson bracket]])**

Examples of [[free field theory|free]] [[Lagrangian field theories]] for which the assumptions of theorem
\ref{PPeierlsBracket} are satisfied,  so that the covariant [[Poisson bracket]] exists in the form
of the [[Peierls bracket]] include

* the [[free field theory|free]] [[real scalar field]] (example \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime});

* the [[free field theory|free]] [[Dirac field]] (example \ref{LagrangianDensityForDiracField}).

For the [[free field theory|free]] [[scalar field]] this is the statement of example \ref{GreenHyperbolicKleinGordonEquation}
with example \ref{PresymplecticFormForFreeRealScalarField}, while for the [[Dirac field]] this is the
statement of example \ref{GreenHyperbolicDiracOperator} with example \ref{PresymplecticFormForFreeDiracField}.

=--

For the [[free field theory|free]] [[electromagnetic field]] (example \ref{ElectromagnetismLagrangianDensity})
the assumptions of theorem \ref{PPeierlsBracket} are violated, the [[covariant phase space]] does not exist.
But in the discuss of _[Gauge fixing](#GaugeFixing)_, below,
we will find that for an equivalent re-incarnation of the electromagnetic field, they are met after all.



$\,$

**BV-resolution of the covariant phase space**
 {#BVResolutionOfTheCovariantPhaseSpace}

So far we have discussed the [[covariant phase space]] (prop. \ref{CovariantPhaseSpace}) in terms of
explicit restriction to the [[shell]].  We now turn to the more flexible perspective where
a [[homological resolution]] of the [[shell]] in terms of  "[[antifields]]" is used (def. \ref{BVComplexOfOrdinaryLagrangianDensity}).

+-- {: .num_example #BVPresymplecticCurrent}
###### Example
**(BV-presymplectic current)**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
whose [[field bundle]] $E$ is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) and whose [[Lagrangian density]] $\mathbf{L}$ is spacetime-independent (example \ref{ShellForSpacetimeIndependentLagrangians}).
Let $\Sigma \times \{\varphi\} \hookrightarrow \mathcal{E}$ be a constant section of the shell (eq:ConstantSectionOfTrivialShellBundle).

Then in the BV-variational bicomplex (eq:ComparisonMorphismFromOrdinaryBVComplexToLocalObservables)
there exists the _BV-presymplectic potential_

$$
  \label{BVPresymplecticPotential}
  \Theta_{BV}
    \;\coloneqq\;
  \phi^{\ddagger}_a \delta \phi^a \, dvol_\Sigma
  \;\in\;
  \Omega^{p,1}_\Sigma(E,\varphi)\vert_{\mathcal{E}_{BV}}
$$

and the corresponding _BV-presymplectic current_

$$
  \Omega_{BV}
  ;\in\;
  \Omega^{p,2}_\Sigma(E,\varphi)\vert_{\mathcal{E}_{BV}}
$$

defined by

$$
  \begin{aligned}
    \Omega_{BV}
      & \coloneqq
    \delta \Theta_{BV}
     \\
     & =
     \delta \phi^{\ddagger}_a \wedge \delta \phi^a \wedge dvol_{\Sigma}
  \end{aligned}
  \,,
$$

where $(\phi^a)$ are the given [[field (physics)|field]]
[[coordinates]], $\phi^{\ddagger}_a$ the corresponding [[antifield]] coordinates (eq:AntifieldCoordinates)
and $\frac{\delta_{EL} \mathbf{L}}{\delta \phi^a}$ the corresponding components of the [[Euler-Lagrange form]]
(prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}).

=--



+-- {: .num_prop #ResolutionOfCovariantPhaseSpaceCorrespondence}
###### Proposition
**(local BV-BFV relation)**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
whose [[field bundle]] $E$ is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) and whose [[Lagrangian density]] $\mathbf{L}$ is spacetime-independent (example \ref{ShellForSpacetimeIndependentLagrangians}).
Let $\Sigma \times \{\varphi\} \hookrightarrow \mathcal{E}$ be a constant section of the shell (eq:ConstantSectionOfTrivialShellBundle).

Then the BV-presymplectic current $\Omega_{BV}$ (def. \ref{BVPresymplecticCurrent})
witnesses the [[on-shell]] vanishing (prop. \ref{HorizontalDerivativeOfPresymplecticCurrentVanishesOnShell}) of the [[total derivative|total spacetime derivative]] of the genuine [[presymplectic current]] $\Omega_{BFV}$ (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) in that the [[total derivative|total spacetime derivative]]
of $\Omega_{BFV}$ equals the BV-differential $s_{BV}$  of $\Omega_{BV}$:

$$
  d \Omega_{BFV} = s \Omega_{BV}
  \,.
$$

Hence if $\Sigma_{tra} \hookrightarrow \Sigma$ is a [[submanifold]] of [[spacetime]] of full dimension $p+1$
[[manifold with boundary|with boundary]] $\partial \Sigma_{tra} = \Sigma_{in} \sqcup \Sigma_{out}$

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

then the [[pullback of differential forms|pullback]] of the
two [[presymplectic forms]] (eq:TransgressionOfPresymplecticCurrentToCauchySurface)
on the incoming and outgoing [[spaces of field histories]], respectively, differ by the
BV-differential of the transgression of the BV-presymplectic current:

$$
  \left( (-)\vert_{in}\right)^\ast\left( \omega_{in}\right)
  \;-\;
  \left( (-)\vert_{out} \right)^\ast \left( \omega_{out} \right)
  =
  \tau_{\mathbb{D} \times \Sigma_{tra}} ( s \Omega_{BV} )
  \phantom{AAAA}
  \in
  \Omega^2
  \left(
    \Gamma_{\Sigma_{tra}}(E)_{\delta_{EL} \mathbf{L} = 0}
  \right)
  \,.
$$

This [[homological resolution]] of the [[Lagrangian correspondence]] that exhibits the "covariance" of the
[[covariant phase space]] (prop. \ref{CovariantPhaseSpace}) is known as the _BV-BFV relation_
([Cattaneo-Mnev-Reshetikhin 12 (9)](BV-BRST+formalism#CattaneoMnevReshetikhin12)).

=--


+-- {: .proof}
###### Proof

For the first statement we compute as follows:

$$
  \begin{aligned}
   s \Omega_{BV}
    & =
  - \delta (s \phi^{\ddagger}_a) \delta \phi^a \wedge dvol_{\Sigma}
  \\
    & =
  - \delta \frac{\delta_{EL}L }{\delta \phi^a}  \delta \phi^a dvol_{\Sigma}
  \\
  & =
  - \delta \delta_{EL}\mathbf{L}
  \\
  & =
  d \Omega_{BFV}
  \,,
  \end{aligned}
$$

where the first steps simply unwind the definitions, and where the last step is prop. \ref{HorizontalDerivativeOfPresymplecticCurrentVanishesOnShell}.

With this the second statement follows by immediate generalization of
the proof of prop. \ref{CovariantPhaseSpace}.

=--



+-- {: .num_example #DerivedPresymplecticCurrentOfRealScalarField}
###### Example
**(derived [[presymplectic current]] of [[real scalar field]])**

Consider a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
without any non-trivial implicit [[infinitesimal gauge transformations]] (def. \ref{ImplicitInfinitesimalGaugeSymmetry});
for instance the [[real scalar field]] from example \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}.

Inside its [[local BV-complex]] (def. \ref{BVComplexOfOrdinaryLagrangianDensity}) we may form the linear combination of

1. the [[presymplectic current]] $\Omega_{BFV}$ (example \ref{FreeScalarFieldEOM})

1. the BF-presymplectic current $\Omega_{BV}$ (example \ref{BVPresymplecticCurrent}).

This yields a vertical 2-form

$$
  \Omega \;\coloneqq\; \Omega_{BV} + \Omega_{BFV} \;\; \in \Omega^{p,2}_\Sigma(E)\vert_{\mathcal{E}_{BV}}
$$

which might be called the _derived presymplectic current_.

Similarly we may form the linear combination of
1. the presymplectic potential current $\Theta_{BFV}$ (eq:dLDecomposition)

1. the BF-presymplectic potential current $\Theta_{BV}$ (eq:BVPresymplecticPotential)

1. the [[Lagrangian density]] $\mathbf{L}$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})

hence

$$
  \Theta \;\coloneqq\; \Theta_{BV} + \underset{Lepage}{\underbrace{ \Theta_{BFV} + \mathbf{L} }}
$$

(where the sum of the two terms on the right is the [[Lepage form]] (eq:TheLepage)).
This might be called the _derived presymplectic potental current_.

We then have that

$$
  (\delta + (d-s))\Omega \;=\; 0
$$

and in fact

$$
  (\delta + (d-s))\Theta \;=\; \Omega
  \,.
$$


=--


+-- {: .proof}
###### Proof

Of course the first statement follows from the second, but in fact the two contributions of the first statement
even vanish separately:

$$
  \delta \Omega = 0
  \,,
  \phantom{AAAA}
  (d-s)\Omega = 0
  \,.
$$

The statement on the left is immediate from the definitions, since $\Omega = \delta \Theta$.
For the statement on the right we compute

$$
  \begin{aligned}
    (d - s) (\Omega_{BV} + \Omega_{BFV})
    & =
    \underset{= 0}{\underbrace{d \Omega_{BFV}
      -
    \underset{ = 0 }{\underbrace{ s \Omega_{BV}}}  }}
     +
    \underset{ = 0}{\underbrace{ d \Omega_{BV} - s \Omega_{BFV} }}
    \\
    & = 0
  \end{aligned}
$$

Here the first term vanishes via the local BV-BFV relation (prop. \ref{ResolutionOfCovariantPhaseSpaceCorrespondence})
while the other two terms vanish simply by degree reasons.

Similarly for the second statement we compute as follows:

$$
  \begin{aligned}
    (\delta + (d - s) ) \Theta
    & =
    \underset{ = \Omega_{BV}  + \Omega_{BFV}}{\underbrace{ \delta (\Theta_{BV} + \Theta_{BFV}) }}
    +
    \underset{ = \delta \mathbf{L}}{\underbrace{\mathbf{d} \mathbf{L}}}
    +
    \underset{ = 0 }{\underbrace{  (d-s) \mathbf{L}  }}
    +
    (d-s)(\Theta_{BV} + \Theta_{BFV})
    \\
    & =
    \Omega_{BV} +  \Omega_{BFV}
    +
    \delta \mathbf{L}
    +
    \underset{ = 0}{\underbrace{d \Theta_{BV}}}
    -
    \underset{ = \delta_{EL} \mathbf{L} }{\underbrace{ s \Theta_{BV}}}
    +
    \underset{ = \delta_{EL}\mathbf{L} - \delta \mathbf{L} }{\underbrace{ d \Theta_{BFV} } }
    -
    \underset{ = 0 }{\underbrace{ s \Theta_{BFV} }}
    \\
    & =
    \Omega_{BV} + \Omega_{BFV}
  \end{aligned}
  \,.
$$

Here the direct vanishing of various terms is again by simple degree reasons, and
otherwise we used the definition of $\Omega$ and, crucially, the variational identity
$\delta \mathbf{L} = \delta_{EL}\mathbf{L} - d \Theta_{BFV}$ (eq:dLDecomposition).

=--



$\,$

**Hamiltonian local observables**
 {#HamiltonianLocalObservablesOnACauchySurface}

We have defined the _[[local observables]]_ (def. \ref{LocalObservables}) as
the [[transgression of variational differential forms|transgressions]] of horizontal $p+1$-forms
(with compact spacetime support) to the [[on-shell]] [[space of field histories]] $\Gamma_{\Sigma}(E)_{\delta_{EL}\mathbf{L} = 0}$ over
all of [[spacetime]] $\Sigma$. More
explicitly, these could be called the _spacetime local observables_.

But with every choice of [[Cauchy surface]] $\Sigma_p \hookrightarrow \Sigma$ (def. \ref{CauchySurface}) comes another notion
of local observables: those that are [[transgression of variational differential forms|transgressions]]
of horizontal $p$-forms (instead of $p+1$-forms) to the [[on-shell]]
[[space of field histories]] restricted to the [[infinitesimal neighbourhood]] of that Cauchy surface (def. \ref{FieldHistoriesOnInfinitesimalNeighbourhoodOfSubmanifoldOfSpacetime}): $\Gamma_{\Sigma_p}(E)_{\delta_{EL} \mathbf{L} = 0}$.
These are _spatially local observables_, with respect to the given choice of [[Cauchy surface]].

Among these spatially local observables are the _Hamiltonian local observables_ (def. \ref{HamiltonianLocalObservables} below)
which are [[transgression of variational differential forms|transgressions]] specifically of the
[[Hamiltonian differential forms|Hamiltonian forms]] (def. \ref{HamiltonianForms}).
These inherit a transgression of the [[Poisson bracket Lie n-algebra|local Poisson bracket]] (prop. \ref{LocalPoissonBracket})
to a [[Poisson bracket]] on Hamiltonian local observables (def. \ref{PoissonBracketOnHamiltonianLocalObservables} below).
This is known as the _[[Peierls bracket]]_ (example \ref{PoissonBracketForRealScalarField} below).




+-- {: .num_defn #HamiltonianLocalObservables}
###### Definition
**(Hamiltonian local observables)**

Let $(E, \mathbf{L})$ be a [[Lagrangian field theory]]  (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

Consider a [[local observable]] (def. \ref{LocalObservables})

$$
  \tau_\Sigma(A)
    \;\colon\;
  \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}
    \longrightarrow
  \mathbb{C}
  \,,
$$

hence the [[transgression of variational differential forms|transgression]] of a variational horizontal
$p+1$-form $A \in \Omega^{p+1,0}_{\Sigma,cp}(E)$ of compact spacetime support.

Given a [[Cauchy surface]] $\Sigma_p \hookrightarrow \Sigma$ (def. \ref{CauchySurface})
we say that $\tau_\Sigma (A)$ is _[[Hamiltonian]]_ if it is also the transgression of a
[[Hamiltonian differential form]] (def. \ref{HamiltonianForms}), hence if there exists

$$
  (H,v) \in \Omega^{p,0}_{\Sigma, Ham}(E)
$$

whose transgression over the Cauchy surface $\Sigma_p$ equals the transgression of $A$ over all of
spacetime $\Sigma$, under the isomorphism (eq:CauchySurfaceIsomorphismOnHistorySpace)

$$
  \array{
    \Gamma_\Sigma(E)_{\delta_{EL} \mathbf{L} = 0 }
      && \underoverset{\simeq}{(-)\vert_{N_\Sigma \Sigma_p}}{\longrightarrow} &&
    \Gamma_{\Sigma_p}(E)_{\delta_{EL}\mathbf{L} = 0}
    \\
    & {}_{\mathllap{\tau_\Sigma}(A)}\searrow && \swarrow_{\mathrlap{ \tau_{\Sigma_p}(H) }}
    \\
    && \mathbf{\Omega}^2
  }
$$

=--

Beware that the [[local observable]] $\tau_{\Sigma_p}(H)$ defined by a [[Hamiltonian differential form]]
$H \in \Omega^{p,0}_{\Sigma,Ham}(E)$ as in def. \ref{HamiltonianLocalObservables}  does in general depend
not just on the choice of $H$, but also on the choice $\Sigma_p$ of the Cauchy surface.
The exception are those Hamiltonian forms which are _[[conserved currents]]_:


+-- {: .num_prop #ConservedCharge}
###### Proposition
**([[conserved charges]] -- [[transgression of variational differential forms|transgression]] of [[conserved currents]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

If a [[Hamiltonian differential form]] $J \in \Omega^{p,0}_{\Sigma,Ham}(E)$ (def. \ref{HamiltonianForms}) happens to be a
[[conserved current]] (def. \ref{SymmetriesAndConservedCurrents}) in that its [[total derivative|total spacetime derivative]]
vanishes [[on-shell]]

$$
  d J \vert_{\mathcal{E}} \;= \; 0
$$

then the induced Hamiltonian [[local observable]] $\tau_{\Sigma_p}(J)$ (def. \ref{HamiltonianLocalObservables})
is independent of the choice of [[Cauchy surface]] $\Sigma_p$ (def \ref{CauchySurface})
in that for $\Sigma_p, \Sigma'_p \hookrightarrow \Sigma$ any two Cauchy surfaces which are [[cobordism|cobordant]],
then

$$
  \tau_{\Sigma_p}(J) = \tau_{\Sigma'_p}(J)
  \,.
$$

The resulting [[constant function|constant]] is called the
_[[conserved charge]]_ of the conserved current, traditionally denoted

$$
  Q \;\coloneqq\; \tau_{\Sigma_p}(J)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition the [[transgression of variational differential forms|transgression]] of $d J$
vanishes on the [[on-shell]] [[space of field histories]]. Therefore the result
is given by [[Stokes' theorem]] (prop. \ref{StokesTheorem}).

=--


+-- {: .num_defn #PoissonBracketOnHamiltonianLocalObservables}
###### Definition
**([[Poisson bracket]] of [[Hamiltonian differential form|Hamiltonian]] [[local observables]] on  [[covariant phase space]])**

Let $(E, \mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) where the [[field bundle]] $E \overset{fb}{\to} \Sigma$ is a [[trivial vector bundle]] over [[Minkowski spacetime]] (example \ref{TrivialVectorBundleAsAFieldBundle}).

We say that the _[[Poisson bracket]]_ on Hamiltonian local observables (def. \ref{HamiltonianLocalObservables})
is the [[transgression of variational differential forms|transgression]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces})
of the [[Poisson bracket Lie n-algebra|local Poisson bracket]] (def. \ref{LocalPoissonBracket})
of the corresponding [[Hamiltonian differential forms]] (def. \ref{LocalPoissonBracket})
to the [[covariant phase space]] (def. \ref{CovariantPhaseSpace}).

Explicitly: for $\Sigma_p \hookrightarrow \Sigma$ a choice of [[Cauchy surface]] (def. \ref{CauchySurface})
then the Poisson bracket between two local Hamiltonian observables
$\tau_{\Sigma_p}((H_i, v_i))$ is

$$
  \label{PoissonBracketTransgressedToCauchySurface}
  \left\{
    \tau_{\Sigma_p}((H_1, v_1))
    \,,\,
    \tau_{\Sigma_p}( (H_2, v_2) )
  \right\}
  \;\coloneqq\;
  \tau_{\Sigma_p}( \, \{ (H_1, v_1), (H_2, v_2) \} \, )
  \,,
$$

where on the right we have the transgression of the [[Poisson bracket Lie n-algebra|local Poisson bracket]]
$\{(H_1, v_1), (H_2, v_2)\}$ of [[Hamiltonian differential forms]] on the [[jet bundle]] from prop. \ref{LocalPoissonBracket}.

=--


+-- {: .proof}
###### Proof

We need to see that equation (eq:PoissonBracketTransgressedToCauchySurface) is well defined,
in that it does not depend on the choice of Hamiltonian form $(H_i, v_i)$
representing the local Hamiltonian observable $\tau_{\Sigma_p}(H_i)$.

It is clear that all the transgressions involved depend only on the restriction
of the Hamiltonian forms to the pullback of the jet bundle to
the [[infinitesimal neighbourhood]] $N_\Sigma \Sigma_p$.
Moreover, the Poisson bracket on the jet bundle (eq:LocalPoissonLieBracket)
clearly respects this restriction.

If a Hamiltonian differential form $H$ is in the [[kernel]] of the transgression map
relative to $\Sigma_p$, in that for every smooth collection $\Phi_{(-)} \colon U \to \Gamma_{\Sigma_p}(E)_{\delta_{EL}\mathbf{L} = 0}$ of field histories (according to def. \ref{DifferentialFormsOnDiffeologicalSpaces}) we have (by def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces})

$$
  \int_{\Sigma_p} j^\infty_\Sigma(\Phi_{(-)})^\ast H  \;= \;0
  \;\;\;
  \in \Omega^p(U)
$$

then the fact that the _[[kernel of integration is the exact differential forms]]_ says that
$j^\infty_\Sigma(\Phi_{(-)})^\ast H \in \Omega^p(U \times \Sigma)$ is $d_\Sigma$-[[exact differential form|exact]] and hence in particular
$d_\Sigma$-[[closed differential form|closed]] for all $\Phi_{(-)}$:

$$
  d_\Sigma j^\infty(\Phi_{(-)})^\ast H \;=\; 0
  \,.
$$

By prop. \ref{PullbackAlongJetProlongationIntertwinesHorizontalDerivative} this means that

$$
  j^\infty(\Phi_{(-)})^\ast ( d H ) \;= \; 0
$$

for all $\Phi_{(-)}$. Since $H \in \Omega^{p,0}_\Sigma(E)$ is horizontal, the same
proposition (see also example \ref{BasicFactsAboutVarationalCalculusOnJetBundleOfTrivialVectorBundle}) implies that
in fact $H$ is horizontally closed:

$$
  d H \;=\; 0
  \,.
$$

Now since the field bundle $E \overset{fb}{\to} \Sigma$ is [[trivial bundle|trivial]] by assumption, prop. \ref{HorizontalVariationalComplexOfTrivialFieldBundleIsExact}
applies and says that this horizontally closed form on the jet bundle is in fact horizontally exact.

In conclusion this shows that the [[kernel]] of the [[transgression of variational differential forms|transgression]]
map $\tau_{\Sigma_p} \;\colon\; \Omega^{p,0}_\Sigma(E) \to C^\infty\left( \Gamma_{\Sigma_p}(E)\right)$
is precisely the space of horizontally exact horizontal $p$-forms.

Therefore the claim
now follows with the statement that horizontally exact [[Hamiltonian differential forms]] constitute a
[[Lie ideal]] for the local Poisson bracket on the jet bundle; this is lemma \ref{HorizontallyExactFormsDropOutOfLocalLieBracket}.

=--




+-- {: .num_example #PoissonBracketForRealScalarField}
###### Example
**([[Poisson bracket]] of the  [[real scalar field]])**

Consider the [[Lagrangian field theory]] of the [[free field|free]] [[scalar field]]
(example \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}),
and consider the [[Cauchy surface]] defined by $x^0 = 0$.

By example \ref{LocalPoissonBracketForRealScalarField} the [[Poisson bracket Lie n-algebra|local Poisson bracket]]
of the [[Hamiltonian forms]]

$$
  Q \coloneqq \phi \iota_{\partial_0} dvol_\Sigma \in \Omega^{p,0}(E)
$$

and

$$
  P \coloneqq \eta^{\mu \nu} \phi_{,\mu} \iota_{\partial_\nu} dvol_{\Sigma} \in \Omega^{p,0}(E)
  \,.
$$

is

$$
  \{Q,P\} = \iota_{v_Q} \iota_{v_P} \omega = \iota_{\partial_0} dvol_\Sigma
  \,.
$$


Upon [[transgression of variational differential forms|transgression]] according to def. \ref{PoissonBracketOnHamiltonianLocalObservables}
this yields the following [[Poisson bracket]]

$$
  \left\{
    \int_{\Sigma_p} b_1(\vec x) \phi(t,\vec x) \iota_{\partial_0} dvol_\Sigma(x)
    d^p \vec x
    \;,\;
    \int_{\Sigma_p} b_2(\vec x) \partial_0 \phi(t,\vec x) \iota_{\partial_0} dvol_\Sigma(\vec x)
  \right\}
  \;=\;
  \int_{\Sigma_p} b_1(\vec x) b_2(\vec x) \iota_{\partial_0} dvol_\Sigma(\vec x)
  d^p \vec x
  \,,
$$

where

$$
  \mathbf{\Phi}(x), \partial_0 \mathbf{\Phi}(x)
    \;:\;
  PhaseSpace(\Sigma_p^t) \to \mathbb{R}
$$

denote the point-evaluation observables (example \ref{PointEvaluationObservables}), which act on a field history $\Phi \in \Gamma_\Sigma(E) = C^\infty(\Sigma)$ as

$$
 \mathbf{\Phi}(x) \;\colon\; \Phi \mapsto \Phi(x)
 \phantom{AAAAAAAA}
 \partial_0 \mathbf{\Phi}(x) \;\colon\; \Phi \mapsto \partial_0 \Phi(x)
 \,.
$$

Notice that these point-evaluation functions themselves do not arise
as the transgression of elements in $\Omega^{p,0}(E)$; only their smearings such as $\int_{\Sigma_p} b_1 \phi dvol_{\Sigma_p}$ do.
Nevertheless we may express the above Poisson bracket conveniently via the [[integral kernel]]

$$
  \label{PoissonBracketOfScalarFieldPointEvaluationOnMinkowskiSpacetime}
  \left\{
    \mathbf{\Phi}(t,\vec x), \partial_0\mathbf{\Phi}(t,\vec y)
  \right\}
  \;=\;
  \delta(\vec x - \vec y)
  \,.
$$

=---




+-- {: .num_prop #PoissonBracketForDiracField}
###### Proposition
**([[super Lie algebra|super]]-[[Poisson bracket]] of the [[Dirac field]])**

Consider the [[Lagrangian field theory]] of the [[free field theory|free]] [[Dirac field]] on [[Minkowski spacetime]] (example \ref{LagrangianDensityForDiracField}) with [[field bundle]] the odd-shifted [[spinor bundle]] $E = \Sigma \times S_{odd}$ (example \ref{DiracFieldBundle}) and with

$$
  \theta \Psi_\alpha(x)
  \;\colon\;
  \mathbb{R}^{0\vert 1}
     \longrightarrow
  \left[
    \Gamma_\Sigma(\Sigma \times S_{odd})_{\delta_{EL}\mathbf{L} = 0},
    \mathbb{C}
  \right]
$$

the corresponding odd-graded point-evaluation observable (example \ref{PointEvaluationObservables}).

Then consider the [[Cauchy surfaces]] in [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime}) given by $x^0 = t$ for $t \in \mathbb{R}$. Under [[transgression of variational differential forms|transgression]] to this Cauchy surface via def. \ref{PoissonBracketOnHamiltonianLocalObservables},
the [[Poisson bracket Lie n-algebra|local Poisson bracket]], which by example \ref{LocalPoissonBracketForDiracField} is given by the [[super Lie algebra|super Lie bracket]]

$$
  \left\{
     \left( \gamma^\mu \psi  \right)_\alpha \, \iota_{\partial_\mu} dvol_\Sigma
     \,,\,
     \left(\overline{\psi}\gamma^\mu\right)^\beta\, \iota_{\partial_\mu} dvol_\Sigma
  \right\}
  \;=\;
  \left(\gamma^\mu\right)_\alpha{}^{\beta} \, \iota_{\partial_\mu} dvol_\Sigma
  \,,
$$

has [[integral kernel]]

$$
  \left\{
    \psi_\alpha(t,\vec x)
    ,
    \overline{\psi}^\beta(t,\vec y)
  \right\}
  \;=\;
  (\gamma^0)_{\alpha}{}^\beta \delta(\vec y - \vec x)
  \,.
$$


=--



$\,$

This concludes our discussion of the [[phase space]] and the [[Poisson-Peierls bracket]] for well behaved [[Lagrangian field theories]].
In the [next chapter](#Propagators) we discuss in detail the [[integral kernels]] corresponding to the [[Poisson-Peierls bracket]]
for key classes of examples. These are the _[[propagators]]_ of the theory.
