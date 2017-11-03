

+-- {: .num_defn #PresymplecticCurrentDiracField}
###### Definition
**([[Euler-Lagrange form]] and [[presymplectic current]] of [[Dirac field]])**

Consider the [[Lagrangian field theory]] of the [[Dirac field]] (example \ref{LagrangianDensityForDiracField}).

* its [[Euler-Lagrange variational derivative]] is

  $$
    \delta_{EL} \mathbf{L}
    \;=\;
    2
    (\delta \overline \psi) 
    \left(
      i \gamma^\mu \psi_{,\mu} 
      +
      m \psi
    \right) 
    \wedge dvol_\Sigma
  $$

* its [[presymplectic current]] is

  $$
    \Omega_{BFV}
    \;=\;
    \overline{\psi}\gamma^\mu \psi \, \iota_{\partial_\mu} dvol_\Sigma
  $$

=--


+-- {: .proof}
###### Proof

The variation gives

$$
  \delta_{EL} L
  =
  (\overline{\delta \psi}) 
  \left(
    i \gamma^\mu \psi_{,\mu}
    +    
    m \psi
  \right)
  +
  m \overline{\psi} \delta \psi
  - 
    i \overline{\psi_{,\mu}} \gamma^\mu 
  (\delta \psi)
$$

The [[canonical momentum]] for the [[Dirac field]] is

$$
  \begin{aligned}
    p^\alpha_\mu
    & \coloneqq
    \frac{\partial }{\partial \psi^\alpha_{,\mu}}
    \left(
      i \overline {\psi} \gamma^\nu \psi_{,\nu}
      + 
      m \overline{\psi} \psi
    \right)
    \\
    & =
    \overline{\psi}^\beta (\gamma^\mu)_\beta{}^\alpha 
  \end{aligned}
$$

=--


$$
  \overline{\psi_1} \psi_2
  =
  (\xi_1)^a (\chi_2)_a + (\chi_1)^\dagger_{\dot a} (\xi_2)^{\dagger \dot a}
$$

$$
  \overline{\psi_2} \psi_1
  =
  (\xi_2)^a (\chi_1)_a + (\chi_2)^\dagger_{\dot a} (\xi_1)^{\dagger \dot a}
$$





