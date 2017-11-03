

+-- {: .num_defn #PresymplecticCurrentDiracField}
###### Definition
**([[Euler-Lagrange form]] and [[presymplectic current]] of [[Dirac field]])**

Consider the [[Lagrangian field theory]] of the [[Dirac field]] on [[Minkowski spacetime]] of [[dimension]] $p + 1 \in \{3,4,6,10\}$ (example \ref{LagrangianDensityForDiracField}).

Then

* the [[Euler-Lagrange variational derivative]] in the case of vanishing [[mass]] $m$ is 

  $$
    \delta_{EL} \mathbf{L}
    \;=\;
    2 i\,
    \overline{\delta \psi}
    \,\gamma^\mu\, \psi_{,\mu}
    \,  
    \wedge dvol_\Sigma
  $$

  and in the case that [[spacetime]] [[dimension]] is $p +1 = 4$ and arbitrary [[mass]] $m\in \mathbb{R}$, it is

  $$
    \delta_{EL} \mathbf{L}
     \;=\;
     \left( 
       \overline{\delta \psi}
       \left(
          i \gamma^\mu \psi_{,\mu} + m \psi
       \right)
       +
       \left(
         - i \gamma^\mu\overline{\psi_{,\mu}} + m \overline{\psi}
       \right)
       (\delta \psi)
     \right)
     \,
     dvol_\Sigma
  $$
  

* its [[presymplectic current]] is

  $$
    \Omega_{BFV}
    \;=\;
    \overline{\psi}\,\gamma^\mu \,\psi \, \iota_{\partial_\mu} dvol_\Sigma
  $$


=--


+-- {: .proof}
###### Proof

In any case the [[canonical momentum]] of the [[Dirac field]] according to example \ref{CanonicalMomentum} is

$$
  \begin{aligned}
    p^\alpha_\mu
    & \coloneqq
    \frac{\partial }{\partial \psi^\alpha_{,\mu}}
    \left(
      i \overline {\psi} \, \gamma^\nu \, \psi_{,\nu}
      + 
      m \overline{\psi} \psi
    \right)
    \\
    & =
    \overline{\psi}^\beta (\gamma^\mu)_\beta{}^\alpha 
  \end{aligned}
$$

This yields the [[presymplectic current]] as claimed, by example \ref{CanonicalMomentum}.

Now regarding the [[Euler-Lagrange form]], first consider the massless case in spacetime dimension $p+1 \in \{3,4,6,10\}$, where

$$
  L
  \;=\;
  i \overline{\psi} \, \gamma^\mu \, \psi_{,\mu}
  \,.
$$

Then we compute as follows:

$$
  \begin{aligned}
    \delta_{EL} L
    & =
    i \,\overline{\delta \psi} \, \gamma^\mu \, \psi_{,\mu}
    \underset{
      = +
      i \,\overline{\delta \psi} \, \gamma^\mu \, \psi_{,\mu}
    }{
    \underbrace{
    -
    i \overline{\psi_{,\mu}} \, \gamma^\mu \, \delta \psi
    }
    }
    \\
    & =
    2 i \, \overline{\delta \psi} \, \gamma^\mu \, \psi_{,\mu}
  \end{aligned}
$$

Here the first equation is the general formula (eq:EulerLagrangeEquationGeneral) for the Euler-Lagrange variation, while the identity under the braces combines two facts:

1. the [[bilinear form]] $\overline{(-)}\gamma^\mu(-)$ is symmetric (...)

1. the spinor field coordinate functions anti-commute according to (eq:DiracFieldJetCoordinatesAnticommute).

Finally in the special case of the massive Dirac field in spacetime dimension $p+1 = 4$ the Lagrangian function is

$$
  L
  \;=\;
  i \, \overline{\psi} \gamma^\mu \psi_{,\mu} + m \overline{\psi}\psi
$$

where now $\psi_\alpha$ takes values in the [[complex numbers]] $\mathbb{C}$ (as opposed to in $\mathbb{R}$, $\mathbb{H}$ or $\mathbb{O}$). Therefore we may now form the [[derivative]] equivalently by treeating $\psi$ and $\overline{\psi}$ as independent components of the field. This immediately yields the claim.


=--


