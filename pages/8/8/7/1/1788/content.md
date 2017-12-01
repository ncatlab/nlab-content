+-- {: .num_prop #NoetherIdentities}
###### Proposition
**([[Noether's theorem|Noether's theorem II]] -- [[Noether identities]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

A [[gauge parameter|gauge parameterized]] [[evolutionary vector field]] (eq:CoordinateExpressionForGaugeParameterized)

$$
  v_\epsilon
  \;=\;
  \left(
    \epsilon^\alpha R^a_\alpha
    +
    \epsilon^\alpha_{,\mu} R^{a \mu}_\alpha
    +
    \epsilon^\alpha_{,\mu_1 \mu_2} R^{a \mu_1 \mu_2}_\alpha
    +
    \cdots
  \right)
  \partial_{\phi^a}
$$

is an [[infinitesimal symmetry of the Lagrangian]] for all [[gauge parameters]] $((\epsilon^\alpha), (\epsilon^\alpha_{,\mu}), \cdots)$ precisely if the [[Euler-Lagrange form]] $\delta_{EL}\mathbf{L}$ (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime})
satisfies the following relation:

$$
  \left(
    R^{a}_\alpha \frac{\delta_{EL}\mathbf{L}}{\delta \phi^a}
    -
    R^{a \mu}_\alpha \frac{d}{d x^\mu} \frac{\delta_{EL}\mathbf{L}}{\delta \phi^a}
    +
    R^{a \mu_1 \mu_2}_\alpha \frac{d^2}{d x^{\mu_1} d x^{\mu_2}} \frac{\delta_{EL}\mathbf{L}}{\delta \phi^a}
    -
    \cdots
  \right)
  \;=\;
  0
  \,.
$$

These relations are called the _[[Noether identities]]_ of the [[Euler-Lagrange equations|Euler-Lagrange]] [[equations of motion]] (def \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}).

=--

+-- {: .proof}
###### Proof

By [[Noether's theorem|Noether's theorem I]],
$v_\epsilon$ is an [[infinitesimal symmetry of the Lagrangian]] precisely if the contraction (def. \ref{ContractionOfFormsWithVectorFields})
of $v_\epsilon$ with the [[Euler-Lagrange form]] (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime})
is horizontally exact:

$$
  \iota_{v_\epsilon} \delta_{EL}\mathbf{L} = d J_{\hat v}
  \,.
$$

From (eq:CoordinateExpressionForGaugeParameterized) this means that

$$
  \begin{aligned}
    d J_{\hat v}
    & =
    \iota_{v_\epsilon} \delta_{EL} \mathbf{L}
    \\
    & =
    \underset{k \in \mathbb{N}}{\sum}
      \frac{d^k \epsilon^\alpha}{d x^{\mu_1} \cdot d x^{\mu_k}} R^{a \mu_1 \cdots \mu_k}_\alpha
      \frac{\delta_{EL} \mathbf{L}}{\delta \phi^a}
    \\
    & =
    \underset{A}{
    \underbrace{
    \epsilon^\alpha
    \underset{k \in \mathbb{N}}{\sum}
      (-1)^k  R^{a \mu_1 \cdots \mu_k}_\alpha
      \frac{d^k}{d x^{\mu_1} \cdots d x^{\mu_k}}
      \frac{\delta_{EL} \mathbf{L}}{\delta \phi^a}
    }
    }
    +
    d (...)
    \,,
  \end{aligned}
$$

where in the last step we used [[integration by parts]] to move the [[total spacetime derivatives]] off of $\epsilon^\alpha$, thereby picking up some horizontally exact correction term, as show.

This means that the term $A$ over the brace is horizontally exact:

$$
  \epsilon^\alpha
   \underset{k \in \mathbb{N}}{\sum}
     (-1)^k  R^{a \mu_1 \cdots \mu_k}_\alpha
      \frac{d^k}{d x^{\mu_1} \cdots d x^{\mu_k}}
      \frac{\delta_{EL} \mathbf{L}}{\delta \phi^a}
   \;=\;
   d(...)
$$

But now the term on the left is independent of the jet coordinates $\epsilon^\alpha_{,\mu_1 \cdots \mu_k}$
of positive order $k \geq 1$, while the horizontal derivative increases the dependency on the jet order by one.
Therefore the term on the left is horizontally exact precisely if it vanishes, which is the case precisely if the coefficients of $\epsilon^\alpha$ vanish, which is the statement of the Noether identities.

Alternatively we may reach this conclusion from (eq:NoetherIdentityTermIsHorizontallyExact) by applying to both sides of (eq:NoetherIdentityTermIsHorizontallyExact) the [[Euler-Lagrange derivative]] (eq:EulerLagrangeEquationGeneral) _with respect to $\epsilon^\alpha$_. On the left this yields again the coefficients of $\epsilon^\alpha$,
while by the argument from example \ref{TrivialLagrangianDensities} it makes the right hand side vanish.


=--



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


+-- {: .proof}
###### Proof

With the explicit form (eq:EulerLagrangeEquationGeneral) for the [[Euler-Lagrange derivative]] we compute as follows:

$$
  \begin{aligned}
    \delta_{EL}
    \left(
      \tfrac{1}{2}
      k_{\alpha \beta} f^\alpha_{\mu\nu} f^{\beta \mu \nu} 
    \right)
    & =
    \left(
    \left(
      \frac{\partial}{\partial a_{\mu'}^{\alpha'}}
      \left(
        a_{\mu,\nu}^\alpha
        +
        \tfrac{1}{2}
        \gamma^{\alpha}{}_{\alpha_2 \alpha_3}
        a_{\mu}^{\alpha_2} a_\nu^{\alpha_3}
      \right)
    \right)
    k_{\alpha \beta}
    f^{\beta \mu \nu}
    -
    \left(
      \frac{d}{d x^{\nu'}}
      \frac{\partial}{\partial a_{\mu',\nu'}^{\alpha'}}
      \left(
        a_{\mu,\nu}^\alpha
        +
        \tfrac{1}{2}
        \gamma^{\alpha}{}_{\alpha_2 \alpha_3}
        a_{\mu}^{\alpha_2} a_\nu^{\alpha_3}
      \right)
    \right)
    k_{\alpha \beta}
    f^{\beta \mu \nu}
    \right)
    \delta a_{\mu'}^{\alpha'}
    \\
    & =
    \gamma^{\alpha}{}_{\alpha' \alpha_3} a_\nu^{\alpha_3}
    f^{\beta \mu \nu}
    k_{\alpha \beta}
    \delta a_{\mu}^{\alpha'}
    -
    \left(
      \frac{d}{d x^{\nu}} f^{\beta \mu \nu}
    \right)
    k_{\alpha \beta}
    \delta a_{\mu}^{\alpha}
    \\
    &=
    \left(
      f^{\alpha \mu \nu}_{,\mu}
      +
      \underset{\tfrac{1}{2} ?}{\underbrace{1}}
      \gamma^\alpha{}_{\beta \gamma} a_\mu^\beta f^{\gamma \mu \nu}
    \right)
    k_{\alpha \beta}
    \delta a_\nu^\beta
  \end{aligned}  
$$

> relative factor of 2 wrong?

In the last step we used that $\gamma_{\alpha \beta \gamma} \coloneqq k_{\alpha \alpha'} \gamma^{\alpha'}{}_{\beta \gamma}$ is totally skew-symmetric in its indices.

=--
