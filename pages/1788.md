

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
  \overline{\psi_1} \phi_2
  =
  (\xi_1)^a (\chi_1)_a + \chi
$$



$\,$

$\,$

$\,$


+-- {: .num_defn #DifferentialFormOnSuperCartesianSpaces}
###### Definition
**([[super differential forms]] on [[super Cartesian spaces]])


For $\mathbb{R}^{b\vert s}$ a [[super Cartesian space]] (def. \ref{SuperCartesianSpace}), hence the [[formal dual]]
of the [[supercommutative superalgebra]] of the form

$$
  C^\infty(\mathbb{R}^{b\vert s})
  \;=\;
  C^\infty(\mathbb{R}^b) \otimes_{\mathbb{R}} \wedge^\bullet \mathbb{R}^s
$$

with canonical even-graded [[coordinate function]] $(x^i)$ and odd-graded coordinate functions $(\theta^j)$,
then the [[de Rham complex]] of _[[super differential forms]]_ 

$$
  \Omega^\bullet(\mathbb{R}^{b|s})
$$

is the $\mathbb{Z} \times (\mathbb{Z}/2)$-[[graded commutative algebra]]

$$
  \Omega^\bullet(\mathbb{R}^{b|s})
  \;\coloneqq\;
  C^\infty(\mathbb{R}^{b|s})
    \otimes_{\mathbb{R}}
   \wedge^\bullet \langle
      d x^1, \cdots, d x^b,
      \;
      d \theta^1, \cdots, d\theta^s
   \rangle
$$

which is generated over $C^\infty(\mathbb{R}^{b\vert s})$ from new generators

$$
  \underset{
    \text{deg} = (1,even)
  }{\underbrace{ d x^i }}
  \phantom{AAAAA}
  \underset{
    \text{deg} = (1,odd)
  }{
  \underbrace{
    d \theta^j
  }
  }
$$

whose [[differential]] is defined in degree-0 by

$$
  d f 
    \;\coloneqq\; 
  \frac{\partial f}{\partial x^i} d x^i 
    +
  \frac{\partial f}{\partial \theta^j} d \theta^j 
$$

and extended from there as a bigraded [[derivation]] of bi-degree $(1,even)$.

| generator | bi-degree |
|--|--|
| $x^a$ | (0,even) |
| $\theta^\alpha$ | (0,odd) |
| $d$ | (1,even) |
| $dx^a$ | (1,even) |
| $d\theta^\alpha$ | (1,odd) |

This means that if $\alpha \in \Omega^\bullet(\mathbb{R}^{b\vert s})$ is in bidegree $(n_\alpha, \sigma_\alpha)$,
and $\beta \in \Omega^\bullet(\mathbb{R}^{b \vert \sigma})$ is in bidegree $(n_\beta, \signa_\beta)$, then

$$
  \alpha \wedge \beta
  \;
  =
  \;
  (- 1)^{n_\alpha n_\beta + \sigma_\alpha \sigma_\beta}
  \;
  \beta \wedge \alpha
  \,.
$$

Hence there are _two_ contributions to the sign picked up when exchanging two super-differential forms in the wedge product:

1. there is a "cohomological sign" which for commuting a $n_1$-forms past an $n_2$-form is $(-1)^{n_1 n_2}$;

1. in addition there is a "super-grading" sich which for commuting a $\sigma_1$-graded coordinate function past a $\sigma_2$-graded coordinate function (possibly under the de Rham differential) is $(-1)^{\sigma_1 \sigma_2}$.

For example:

$$
  x^{a_1} (dx^{a_2}) = + (dx^{a_2}) x^{a_1}
$$


$$
  \theta^\alpha (dx^a) = + (dx^a) \theta^\alpha
$$

$$
  \theta^{\alpha_1} (d\theta^{\alpha_2})
   =
  - (d\theta^{\alpha_2}) \theta^{\alpha_1}
$$

$$
  dx^{a_1}
  \wedge
  d x^{a_2}
  =
  -
  d x^{a_2}
  \wedge
  d x^{a_1}
$$


$$
  dx^a
  \wedge
  d \theta^{\alpha}
  =
  -
  d\theta^{\alpha}
  \wedge
  d x^a
$$

$$
  d\theta^{\alpha_1}
  \wedge
  d \theta^{\alpha_2}
  =
  +
  d\theta^{\alpha_2}
  \wedge
  d \theta^{\alpha_1}
$$


=--

(e.g. [Deligne-Freed 99](signs+in+supergeometry#DeligneFreed99); see at _[[signs in supergeometry]]_ for further discussion)
