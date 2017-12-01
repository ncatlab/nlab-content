
+-- {: .num_prop #NoethersFirstTheorem}
###### Proposition
**([[Noether's theorem]] I)**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

If $v$ is an [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents})
with $\mathcal{L}_{\hat v} \mathbf{L} = d \tilde J_{\hat v}$, then

$$
  \label{NoetherCurrent}
  J_{\hat v} \coloneqq \tilde J_{\hat v} - \iota_{\hat v} \Theta_{BFV}
$$

is an [[on-shell]] [[conserved current]] (def. \ref{SymmetriesAndConservedCurrents}), for $\Theta_{BFV}$
a presymplectic potential (eq:PresymplecticPotential) from def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}.

=--

+-- {: .proof}
###### Proof

By [[Cartan's homotopy formula]] for the [[Lie derivative]] (prop. \ref{CartanHomotopyFormula})
and the decomposition of the variational derivative $\delta \mathbf{L}$ (eq:dLDecomposition)
and the fact that contraction $\iota_{\hat v}$ with the prolongtion of an evolutionary vector field vanishes on horizontal differential forms
(eq:GenericComponentsForProlongationOfEvolutionaryVectorField) and anti-commutes with the horizontal differential (eq:ProlongedEvolutionaryVectorFieldContractionAnticommutedWithHorizontalDerivative), by def. \ref{EvolutionaryVectorField},
we may re-express the defining equation for the symmetry as follows:

$$
  \begin{aligned}
    d \tilde J_{\hat v}
    & =
    \mathcal{L}_{\hat v} \mathbf{L}
    \\
    & =
    \iota_{\hat v} \underset{= \delta_{EL}\mathbf{L} - d \Theta_{BFV}}{\underbrace{\mathbf{d} \mathbf{L}}}
    +
    \mathbf{d} \underset{= 0}{\underbrace{\iota_v \mathbf{L}}}
    \\
    & =
    \iota_{\hat v} \delta_{EL} \mathbf{L}
    + d \iota_{\hat v} \Theta_{BFV}
  \end{aligned}
$$

which is equivalent to

$$
  d(\underset{= J_{\hat v}}{\underbrace{\tilde J_{\hat v} - \iota_{\hat v} \Theta_{BFV}}}) = \iota_{\hat v} \delta_{EL}\mathbf{L}
$$

Since, by definition of the [[prolonged shell]] $\mathcal{E}^\infty$, the differential form on the right 
vanishes on $\mathcal{E}$ this yields the claim.

=--
