
By def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime} a field history
$\Phi \in \Gamma_\Sigma(E)$ is [[on-shell]] precisely if its [[jet prolongation]] $j^\infty_\Sigma(E)$ (def. \ref{JetProlongation})
factors through the [[shell]] $\mathcal{E} \hookrightarrow J^\infty_\Sigma(E)$ (eq:ShellInJetBundle).
Hence by def. \ref{FlowOfFieldHistoriesAlongEvolutionaryVectorField} the statement is equivalently that
the ordinary flow (prop. \ref{CartanHomotopyFormula}) of $\hat v$ (def. \ref{EvolutionaryVectorFieldProlongation})
on the [[jet bundle]] $J^\infty_\Sigma(E)$ preserves the [[shell]]. This in turn means that it preserves the
vanishing locus of the [[Euler-Lagrange form]] $\delta_{EL} \mathbf{L}$. 

But by definition $\delta_{EL} \mathbf{L} = \mathbf{d} \mathbf{L} + d \Theta_{BFV}$ is the unique component of
the [[de Rham differential]] $\mathbf{d} \mathbf{L}$ proportional to the [[variational derivative]] of the fields
modulo a [[total spacetime derivative]] (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}).
Now by definition of [[infinitesimal symmetries of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents})
the infinitesimal change of $\mathbf{L}$ along the flow is horizontally exact
$\mathcal{L}_{\hat v} \mathbf{L} = d J_{\hat v}$, which implies that $\mathcal{L}_{\hat v} \delta_{EL} \mathbf{L} = 0$.
