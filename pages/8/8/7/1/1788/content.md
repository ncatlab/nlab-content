Consider a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
without any non-trivial implicial [[infinitesimal gauge transformations]] (def. \ref{ImplicitInfinitesimalGaugeSymmetry});
for instance the [[real scalar field]] (def. \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}).

Inside its BV-complex (def. \ref{BVComplexOfOrdinaryLagrangianDensity}) we may form the linear combination of

1. the [[presymplectic current]] $\Omega_{BFV}$ (example \ref{FreeScalarFieldEOM})

1. the BF-presymplectic current $\Omega_{BV}$ (example \ref{BVPresymplecticCurrent}).

This yields a vertical 2-form

$$
  \Omega \;\coloneqq\; \Omega_{BV} + \Omega_{BFV} \;\; \in \Omega^{p,2}_\Sigma(E)\vert_{\mathcal{E}_{BV}}
$$

which is closed under the BV-horizontal derivative $d - s$:

$$
  \begin{aligned}
    (d - s) (\Omega_{BV} + \Omega_{BFV})
    & =
    \underset{= 0}{\underbrace{d \Omega_{BFV} - s \Omega_{BV}}} + d \Omega_{BV} - s \Omega_{BFV}
    \\
    & = 0
  \end{aligned}
$$

Here the first term vanishes via the local BV-BFV relation (prop. \ref{ResolutionOfCovariantPhaseSpaceCorrespondence})
while the other two terms vanish simply by degree reasons.

Of course we also have $\delta \Omega = 0$, and hence

$$
  (\delta + (d-s)) \Omega = 0
  \,.
$$

In fact we may also form the linear combination of

1. the presymplectic potential current $\Theta_{BFV}$ (eq:dLDecomposition)

1. the BF-presymplectic potential current $\Theta_{BV}$ (eq:BVPresymplecticPotential)

1. the [[Lagrangian density]] $\mathbf{L}$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})

hence

$$
  \Theta \;\coloneqq\; \Theta_{BV} + \underset{Lepage}{\underbrace{ \Theta_{BFV} + \mathbf{L} }}
$$

where the sum of the two terms on the right is the [[Lepage form]] (eq:TheLepage).

This is then a potential for the derived presymplectic current:

$$
  (\delta + (d-s))\Theta \;=\; \Omega
  \,.
$$

$$
  \begin{aligned}
    (\delta + (d - s) ) \Theta
    \\
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
$$
