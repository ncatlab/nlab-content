
...


+-- {: .num_example #LocalPoissonBracketForDiracField}
###### Example
**([[Poisson bracket Lie n-algebra|local Poisson bracket]] for [[free field theory|free]] [[Dirac field]])**

Consider the [[Lagrangian field theory]] of the [[free field theory|free]] [[Dirac field]] on [[Minkowski spacetime]] (example \ref{LagrangianDensityForDiracField}), whose [[presymplectic current]] is, according to example \ref{PresymplecticCurrentDiracField}, given by 

$$
  \label{RecallPresymplecticCurrentOfDiracField}
  \Omega_{BFV}
  \;=\;
  \overline{\delta \psi} \, \gamma^\mu \, \delta \psi \, \iota_{\partial_\mu} dvol_\Sigma
  \,.
$$

Consider this specifically in [[spacetime]] [[dimension]] $p + 1 = 4$ in which case the components $\psi_\alpha$ are [[complex number]]-valued (by prop./def. \ref{SpacetimeAsMatrices}), so that the [[tuple]] $(\psi_\alpha)$ amounts to 8 real-valued coordinate functions. By changing complex coordinates, we may equivalently consider $(\psi_\alpha)$ as four coordinate functions, and $(\overline{\psi}^\alpha)$ as another four independent coordinate functions.

Using this coordinate transformation, it is immediate to find the following [[pairs]] of [[Hamiltonian vector fields]] and their [[Hamiltonian differential forms]] from def. \ref{HamiltonianForms} applied to (eq:RecallPresymplecticCurrentOfDiracField)

| [[Hamiltonian vector field]] | [[Hamiltonian differential form]] |
|------------------------------|-----------------------------------|
|  $\phantom{AA} \partial_{\psi_\alpha}$      | $\phantom{AA}-\left(\overline{\delta \psi}\gamma^\mu\right)^\alpha\, \iota_{\partial_\mu} dvol_\Sigma$ |
| $\phantom{AA} \partial_{\overline{\psi}_\alpha}$ | $\phantom{AA}\phantom{-}\left( \gamma^\mu \psi  \right)_\alpha \, \iota_{\partial_\mu} dvol_\Sigma$ |

and to obtain the following non-trivial [[Poisson bracket Lie n-algebra|local Poisson brackets]] (prop. \ref{LocalPoissonBracket}) (the other possible brackets vanish):

$$
  \left\{
     \phantom{-}\left( \gamma^\mu \psi  \right)_\alpha \, \iota_{\partial_\mu} dvol_\Sigma
     \,,\,
     \left(\overline{\psi}\gamma^\mu\right)^\beta\, \iota_{\partial_\mu} dvol_\Sigma
  \right\}
  \;=\;
  \left(\gamma^\mu\right)_\alpha{}^{\beta} \, \iota_{\partial_\mu} dvol_\Sigma 
$$

=--
