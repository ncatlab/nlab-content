

$$
  D_\mu f^{\alpha \mu \nu} = 0
$$

$$
  D_\mu f^{\alpha \mu \nu}
   \;\coloneqq\;
  f^{\alpha \mu \nu}_{,\mu}
  +
  \tfrac{1}{2}
    \gamma^{\alpha}{}_{\beta \gamma}
    a^\beta_{\mu} f^{\gamma \mu \nu}
$$

| [[field (physics)|field]] |  [[field bundle]] |  [[Lagrangian density]] | [[equation of motion]] |
|---------------------------|------------------|-------------------------|------------------------|
| [[real scalar field]] |  expl. \ref{RealScalarFieldBundle} |  expl. \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime} | expl. \ref{FreeScalarFieldEOM} |
| [[Dirac field]] | expl. \ref{DiracFieldBundle}  | expl. \ref{LagrangianDensityForDiracField}  |  expl. \ref{EquationOfMotionOfDiracFieldIsDiracEquation}  |
| [[electromagnetic field]] | expl. \ref{Electromagnetism} | expl. \ref{ElectromagnetismLagrangianDensity} | expl. \ref{ElectromagnetismEl}  |
| [[Yang-Mills field]] | expl. \ref{YangMillsFieldOverMinkowski}, <br/> expl. \ref{YangMillsFieldInInstantonSector} | expl. \ref{YangMillsLagrangian}  | expl. \ref{YangMillsOnMinkowskiEl} |
| [[B-field]] | expl. \ref{BField} | expl \ref{BFieldLagrangianDensity} | expl. \ref{EulerLagrangeFormBField} |

$\,$

$\,$

+-- {: .num_example #YangMillsOnMinkowskiEl}
###### Example
**([[Euler-Lagrange form]] for [[Yang-Mills theory]] on [[Minkowski spacetime]])**

Let $\mathfrak{g}$ be a [[Lie algebra]] equipped with a binary non-degenerate [[invariant polynomial]] $k$
and consider the [[Lagrangian field theory]] $(E,\mathbf{L})$ of $(\mathfrak{g},k)$-[[Yang-Mills theory]] from example \ref{YangMillsLagrangian}.

Its [[Euler-Lagrange form]] (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) is

$$
  \begin{aligned}
  \delta_{EL}\mathbf{L}
  & =
  D_\mu f^{\mu \nu \alpha}  k_{\alpha \beta}  \delta a_\nu^\beta \, dvol_\Sigma
  \\
  & \coloneqq
  \left(
    f^{\mu \nu \alpha}_{,\mu} + \tfrac{1}{2}\gamma^\alpha{}_{\beta \gamma} a_\mu^\beta f^{\mu \nu \gamma}
  \right)
  k_{\alpha \beta}
  \,\delta a_\mu^\beta
  \, dvol_\Sigma
  \,.
  \end{aligned}
$$

=--

