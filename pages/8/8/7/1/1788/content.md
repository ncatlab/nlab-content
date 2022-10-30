
in that the [[pullback of differential forms|pullback]] (def. \ref{PullbackOfDifferential1FormsOnCartesianSpaces})
along the [[shell]] inclusion $\mathcal{E} \overset{i_{\mathcal{E}}}{\hookrightarrow} J^\infty_\Sigma(E)$ (eq:ShellInJetBundle)
vanishes:

$$
  \begin{aligned}
    (i_{\mathcal{E}})^\ast
    \left(
     d \Omega_{BFV}
    \right)
    & =
    - (i_{\mathcal{E}})^\ast
    \left(
     \delta \delta_{EL} \mathcal{L}
    \right)
    \\
    & =
    - \delta
    \underset{
      ...
    }{
    \underbrace{
    (i_{\mathcal{E}})^\ast
    \left(
      \delta_{EL} \mathbf{L}
    \right)
    }
    }
    \\
    & = 0
  \end{aligned}
$$



+-- {: .num_defn #VerticalCotangentBundle}
###### Definition
**([[vertical cotangent bundle]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[fiber bundle]]. Its _[[vertical cotangent bundle]]_

$$
  \array{
    T^\ast_\Sigma E && \longrightarrow && E
    \\
    & \searrow && \swarrow
    \\
    && \Sigma
  }
$$

is the fiber bundle whose [[fiber]] over $x \in \Sigma$ is the [[cotangent bundle]] of the fiber of $E$ over $X$:

$$
  \left(
    T^\ast_\Sigma E
  \right)_x
  \;\coloneqq\;
  T^\ast E_x
  \,.
$$

In the case that $E \overset{fb}{\to} \Sigma$ is a [[vector bundle]], this is the [[fiber product]] of $E$ with its [[dual vector bundle]]

$$
  T^\ast_\Sigma E
  \;\simeq\;
  E \underset{\Sigma}{\times} E^\ast
  \,.
$$

In the case that $E = \Sigma \times F$ is a [[trivial bundle]], then 

$$
  T^\ast_\Sigma E
  \simeq
  \Sigma \times T^\ast F
  \,.
$$

Finally if $E = \Sigma \times V$ is both trivial and a vector bundle, then 

$$
  T^\ast_\Sigma E 
  \;\simeq\;
  \Sigma \times V \times V^\ast
  \,,
$$

where $V^\ast$ is the [[dual vector space]] of $V$.


=--
 
Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] which is 

1. a [[free field theory]],

1. admitting [[Cauchy surfaces]],

1. whose [[Lagrangian density]] depends at most on first order jets.

Write 

$$
  T^\ast_\Sigma E
  \;=\;
  E \underset{\Sigma}{\times} E^\ast
$$

for the [[vertical cotangent bundle]] (def. \ref{VerticalCotangentBundle}) of the [[field bundle]].

Then for $\Sigma_p \hookrightarrow \Sigma$ a choice of [[Cauchy surfaces]], the space 

$$
  LinHamObs_{\Sigma_p}(E,\mathbf{L})
  \hookrightarrow
  Obs(E,\mathbf{L})
$$


of on-shell [[observables]] which are

1. linear:

1. Hamiltonian local observables with respect to $\Sigma_p$

is 


$$
  \begin{aligned}
    \Gamma_{\Sigma,cp}(T^\ast_\Sigma E)
    & =
    \Gamma_{\Sigma,cp}( E \times_\Sigma E^\ast)
    \\
    &\simeq
    \Gamma_{\Sigma,cp}(E) \times \Gamma_{\Sigma,cp}(E^\ast)
  \end{aligned}
$$

where

$$
  ( \alpha^a ), (\beta_a)
  \mapsto
  \underset{\Sigma_p}{\int}
    \beta_a(x) \mathbf{\Phi}^a(x)
    \, 
    dvol_{\Sigma_p}(x)
   + 
   \underset{\Sigma_p}{\int}
     \alpha^a(x) 
     \mathbf{P}_a^\mu(x)
   \iota_{\partial_\mu} dvol_\Sigma(x)
$$

$$
  A(x) \mathbf{\Phi}^a(x)
  =
  \left(
    A(0,\vec x) + \epsilon \partial_0 A(0,\vec x)
  \right)
  \left(
    \Phi^a(0,\vec x) + \epsilon \partial_0 \mathbf{\Phi}^a(0,\vec x)
  \right)
  =
  A(0,\vec x) \mathbf{\Phi}^a(0,\vec x)
  +
  \epsilon\left(
    A(0,\vec x) \partial_0 \mathbf{\Phi}(0,\vec x)
    + 
    \partial_0 A(0,\vec x) \mathbf{\Phi}(0,\vec x)
  \right)
$$

