
+-- {: .num_example #dWCohomology}
###### Example
**([[Noether's theorem|Noether's theorems I and II]] in terms of [[local BV-cohomology]])**


Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) over [[Minkowski spacetime]] $\Sigma$ of [[dimension]] $ p + 1$, and let $\mathcal{G} \overset{gb}{\to} \Sigma$ be a [[gauge parameter bundle]] (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}) which is closed (def. \ref{GaugeParametersClosed}).  Assume that both are [[trivial vector bundles]] (example \ref{TrivialVectorBundleAsAFieldBundle}) with field coordinates as in prop. \ref{EulerLagrangeFormIsSectionOfLocalCotangentBundleOfJetBundleGaugeActionLieAlgebroid}.

Then in the [[local BV-complex]] (def. \ref{BVComplexOfOrdinaryLagrangianDensity}) we have:

The $(s_{BV} + d)$-closure of an element in total degree $p$ is characterizes as the [[direct sum]] of an [[evolutionary vector field]] which is an [[infinitesimal symmetry of the Lagrangian]] and the[[conserved current]] that corresponds to it under [[Noether's theorem|Noether's first theorem]] (prop. \ref{NoethersFirstTheorem}).

Moreover, such a pair is $(s_{BV} + d)$-exact precisely if the [[infinitesimal symmetry of the Lagrangian]] is in fact an [[infinitesimal gauge symmetry]] as witnessed by [[Noether's theorem|Noether's second theorem]] (prop. \ref{NoetherIdentities}).

=--


([Barnich-Brandt-Henneaux 94, top of p. 20](local+BRST+cohomology#BarnichBrandtHenneaux94))


+-- {: .proof}
###### Proof

An element of the [[local BV-complex]] in degee $p$ is the [[direct sum]] of a [[horizontal differential form]] of degree $p$ with the product of a horizontal form of degree $(p+1)$ times a function proportional to the [[antifields]]:

$$
  \array{
    \{J_v\} && 
    \\
    && 
    \\
    && \{ v^a \phi^\ddagger_a dvol_\Sigma\}  
  }
$$

Its closure means that

$$
  \array{
    \{J_v\} &\overset{d}{\longrightarrow}& \{ \overset{= 0}{\overbrace{ d J_v - \iota_v \delta_{EL}\mathbf{L} }} \}
    \\
    && \uparrow\mathrlap{s_{BV}}
    \\
    && \{ v^a \phi^\ddagger_a dvol_\Sigma\}
  }
$$

where the equality in the top right corner is euqation

It being exact means that

$$
  \array{
    \left\{ ... \right\}
    &
      \overset{d}{\longrightarrow}
    &
    \left\{
      J_R
      =
      K + d(...)
    \right\}
      &\overset{d}{\longrightarrow}&
    \left\{
      d J_R
    \right\}
    \\
    &&
    \uparrow
    \\
    &&
    \left\{
      K^{a \mu} \phi^\ddagger_a \iota_{\partial_\mu} dvol_\Sigma
    \right\}
  }
$$

where now the equality in the second term from the left is equation (eq:DecompositionOfGaugSymmetryConservedCurrent) for [[conserved currents]] corresponding to [[infinitesimal gauge symmetries]] (prop. \ref{ConservedChargeOfInfinitesimalGaugeSymmetryVanishes}).

=--

