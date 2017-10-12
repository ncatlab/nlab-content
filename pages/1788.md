
+-- {: .num_example #LocalBVComplexOfVacuumElectromagnetismOnMinkowskiSpacetime}
###### Example
**([[local BV-complex]] of [[vacuum]] [[electromagnetism]] on [[Minkowski spacetime]])**

Consider the [[Lagrangian field theory]] of [[free field theory|free]] [[electromagnetism]]
on [[Minkowski spacetime]] (example \ref{ElectromagnetismLagrangianDensity})
with [[gauge parameter]] as in example \ref{InfinitesimalGaugeSymmetryElectromagnetism}.
With the [[field (physics)|field]] and [[gauge parameter]] coordinates as chosen in these examples

$$
  \left(
    (a_\mu), c
  \right)
$$

then the [[local BV-BRST complex]] (prop. \ref{LocalBVBRSTComplexIsDerivedCriticalLocusOfEulerLagrangeForm})
has generators

$$
  \array{
    & \overline{c} & \overline{a}^\mu & a_\mu & c
    \\
    deg =
    &
    -2 & -1 & 0 & 1
  }
$$

together with their [[total spacetime derivatives]],
and the local BV-BRST differential $s$ acts on these generators as follows:

$$
  s
  \;\colon\;
  \left\{
  \array{
    \overline{a}^\mu &\mapsto&  f^{\nu \mu}_{,\nu}  & \text{(equations of Motion -- vacuum Maxwell equations)}
    \\
    \overline{c} &\mapsto& \overline{a}^\mu_{,\mu} & \text{(Noether identity)}
    \\
    a_\mu &\mapsto& c_{,\mu} & \text{(infinitesimal gauge transformation)}
  }
  \right.
$$


=--


$\ddagger$