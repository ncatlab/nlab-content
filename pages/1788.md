+-- {: .num_prop #PrincipleOfExtremalAction}
###### Proposition
**([[principle of extremal action]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

The [[de Rham differential]] $d \mathcal{S}_{b\mathbf{L}}$ of the [[action functional]] (example \ref{VariationOfTheActionFunctional})
vanishes for all [[adiabatic switchings]] $b \in C^\infty_{cp}(\Sigma)$ constant on some
subset $\mathcal{O} \subset \Sigma$ (def. \ref{CutoffFunctions}) on those smooth collections of field histories

$$
  \Phi_{(-)} \;\colon\; U \longrightarrow \Gamma_\Sigma(E)
$$

which, as functions on $U$, are constant outside $\mathcal{O}$ (example \ref{DiffeologicalSpaceOfFieldHistories}, example \ref{SupergeometricSpaceOfFieldHistories})
precisely if $\Phi$ solves the [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]]
(def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}):

$$
  \left(
  \underset{ { {\mathcal{O} \subset \Sigma} \atop { b\vert_{\mathcal{O}} = const } } \atop { \Phi_{(-)}\vert_{\Sigma \setminus \mathcal{O}} = const }  }{\forall}
  \left(
     (\Phi_{(-)})^\ast d \mathcal{S}_{b \mathbf{L}}(\Phi) = 0
  \right)
  \right)
  \;\Leftrightarrow\;
  \left(
    j^\infty_\Sigma(\Phi(-))^\ast ( \delta_{EL} \mathbf{L} ) = 0
  \right)
  \,.
$$

=--


+-- {: .proof}
###### Proof

By prop. \ref{TransgressionOfVariationaldifferentialFormsCompatibleWithVariationalDerivative} we have

$$
  d \mathcal{S}_{b \mathbf{L}}(\Phi) 
  \;=\;
   \int_\Sigma
   j^\infty_\Sigma(\Phi_{(-)})^\ast (  \delta_{EL}  b \mathbf{L} )
   \,.
$$

By the assumption on $\Phi_{(-)}$ it follows that after pullback to $U$ the switching function $b$ is constant, so that
it commutes with the differentials:

$$
  (\Phi_{(-)})^\ast
  d \mathcal{S}_{b \mathbf{L}}(\Phi)
  \;=\;
  (\Phi_{(-)})^\ast
   \int_\Sigma
   b
   j^\infty_\Sigma(\Phi_{(-)})^\ast (  \delta_{EL}   \mathbf{L} )
   \,.
$$

This clearly vanishes for all $\Phi$ precisely if all components of $j^\infty_\Sigma(\Phi_{(-)})^\ast (  \delta_{EL}   \mathbf{L} )$
vanish, which is the statetement of the Euler-Lagrange equations of motion.

=--
