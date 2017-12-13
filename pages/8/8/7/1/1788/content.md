
+-- {: .num_example #dWCohomology}
###### Example
**([[Noether's theorem|Noether theorem I]] in terms of [[local BRST cohomology]])**

The $d-s$-closed elements in degree $(p,0)$ are precisely pairs $(v,J_v)$
consisting of an implicit infinitesimal local gauge symmetry $v$ and a conserved current $J_v$ for it.

The $d_W$-exact elements in this degree are sums of

1. $d$-exact currents;

1. on-shell vanishing implicit gauge transformations;

1. on-shell vanishing currents with their horizontally exact gauge transformations

(...)


=--

+-- {: .proof}
###### Proof


The $d_W$-closed element are
the implicit infinitesimal gauge symmetries $v$ regarded as an [[antifield]] $v^a \phi^\ddagger_a$
multiplied with the [[volume form]] $dvol_\Sigma$
together with their Noether current $J_v \in \Omega^{p,0}_\Sigma(E)$ (prop. \ref{NoethersFirstTheorem})


$$
  \array{
    \{J_v\} &\overset{d}{\longrightarrow}& \{ \overset{= 0}{\overbrace{ d J_v - \iota_v \delta_{EL}\mathbf{L} }} \}
    \\
    && \uparrow\mathrlap{s_{BV}}
    \\
    && \{ v^a \phi^\ddagger_a dvol_\Sigma\}
  }
$$



Such a pair is exact if

$$
  \array{
    \{K\}
     &\overset{d}{\longrightarrow}&
    \{ d K + v^{a \mu} \frac{\delta_{EL}L}{\delta \phi^a} \iota_{\partial_\mu} dvol_\Sigma   \} &\overset{d}{\longrightarrow}& \{ \overset{= 0}{\overbrace{ d J_v - \iota_v \delta_{EL}\mathbf{L} }} \}
    \\
    && \mathllap{s_{BV}}\uparrow && \uparrow\mathrlap{s_{BV}}
    \\
    && v^{a \mu} \phi^\ddagger_a \iota_{\partial_\mu} dvol_\Sigma
      &\underset{-d}{\longrightarrow}&
    \{ v^a \phi^\ddagger_a dvol_\Sigma\}
    \\
    && && \uparrow\mathrlap{s_{BV}}
    \\
    &&
    && \kappa^{a b } \phi^\ddagger_a \phi^\ddagger_b dvol_\Sigma
  }
$$

(...)

=--


+-- {: .num_example }
###### Example
**([[infinitesimal gauge symmetry]] via [[local BRST cohomology]])**

An  [[infinitesimal gauge symmetry]] $v_\epsilon$  of [[gauge parameter]] $(\epsilon^\alpha)$ is a vector field on the jet bundle with components of the form

$$
  \mathcal{L}_{v_\epsilon} \phi^a
   \;\coloneqq\;
  R^a_\alpha \epsilon^\alpha
    +
  R^{a \mu}_\alpha \frac{d \epsilon^\alpha}{d x^\mu}
$$

such that this is an [[infinitesimal symmetry of the Lagrangian]] in that

$$
  \begin{aligned}
    \iota_{v_\epsilon} \delta_{EL} \mathbf{L}
    & =
    v^a \frac{\delta_{EL} L}{\delta \phi^a} dvol_\Sigma
    \\
    & =
    \epsilon^\alpha
    \left(
       R^a_\alpha \frac{\delta_{EL} L}{ \delta \phi^a}
       -
       \frac{d}{d x^\mu}
       \left(
          R^{a \mu}_\alpha \frac{\delta_{EL} L}{\delta \phi^a}
       \right)
    \right)
    dvol_\Sigma
    +
    d\left(
       \epsilon^\alpha R^{a \mu}_\alpha \frac{\delta_{EL} L}{\delta \phi^a}
    \right)
    \iota_{\partial_\mu} dvol_\Sigma
    \\
    & =
    0 + d(...)
  \end{aligned}
$$

for all $(\epsilon^\alpha)$.

The corresponding [[antifield|anti]] [[ghost field]] $c^\ddagger_\alpha$ are taken by the BV-BRST differential to the antifield-preimage of the term on the left:

$$
  s\left(c^\ddagger_\alpha\right)
  \;=\;
  R^a_\alpha \phi^\ddagger_a
  -
  \frac{d}{d x^\mu}
  \left(
    R^{a \mu}_\alpha \phi^\ddagger_a
  \right)
  \,.
$$

Moreover, an [[on-shell]] vanishing [[infinitesimal symmetry of the Lagrangian]] is a vector field with components of the form

$$
  \kappa^{a b} \frac{\delta_{EL} L}{\delta \phi^a}
$$

for $\kappa^{a b} = - \kappa^{b a}$ a skew-symmetric system of smooth functions on the jet bundle.

The linear combination of such an infinitesimal gauge symmetry and an on-shell vanishing infinitesimal symmetry is $(s+d)$-exact:


$$
  \begin{aligned}
    v^a dvol_\Sigma
    & =
    \left(
      R^a_\alpha \epsilon^\alpha
      +
      R^{a \mu}_\alpha \frac{d \epsilon^\alpha}{d x^\mu}
      +
      \kappa^{a b} \frac{\delta_{EL} L }{ \delta \phi^a }
    \right)
    dvol_\Sigma
    \\
    & =
    s
    \left(
      \epsilon^\alpha c^\ddagger_\alpha
      -
      \tfrac{1}{2}\kappa^{a b} \phi^\ddagger_a \phi^\ddagger_b
    \right) dvol_\sigma
    +
    d\left(
      \epsilon^\alpha R^{a \mu}_\alpha
    \right)
    \iota_{\partial_\mu} dvol_\Sigma
  \end{aligned}
$$

([Barnich-Brandt-Henneaux 94, p. 20](local+BRST+cohomology#BarnichBrandtHenneaux94))


It may be useful to organize this expression into the $s+d$-[[bicomplex]] like so:

$$
  \array{
    \{K\}
     &\overset{d}{\longrightarrow}&
     \{ d K
       +
     \epsilon^\alpha R^{a \mu}_\alpha \frac{\delta_{EL}\mathbf{L}}{ \delta \phi^a}
     \}
     &\overset{d}{\longrightarrow}&
    \{ \overset{= 0}{\overbrace{ d J_v - \iota_v \delta_{EL}\mathbf{L} }} \}
    \\
    && \mathllap{s_{BV}}\uparrow && \uparrow\mathrlap{-s_{BV}}
    \\
    &&
    \epsilon^\alpha R^{a \mu}_\alpha \phi^\ddagger_a
    \iota_{\partial_\mu} dvol_\Sigma
      &\underset{d}{\longrightarrow}&
    \left\{
      d\left(
        \epsilon^\alpha R^{a \mu}_\alpha \phi^\ddagger_a
      \right)
      \iota_{\partial_\mu} dvol_\Sigma
      +
      \left(
        R^a_\alpha \epsilon^\alpha
        +
        R^{a \mu}_\alpha \frac{d \epsilon^\alpha}{d x^\mu}
        +
        \kappa^{a b} \frac{\delta_{EL} L }{ \delta \phi^a }
      \right)
      \phi^\ddagger_a
      \,
      dvol_\Sigma
    \right\}
    \\
    && && \uparrow\mathrlap{-s_{BV}}
    \\
    &&
    &&
    \left(
       - \epsilon^\alpha c^\ddagger_\alpha
       +
      \tfrac{1}{2}\kappa^{a b } \phi^\ddagger_a \phi^\ddagger_b
    \right)
    dvol_\Sigma
  }
$$


=--
