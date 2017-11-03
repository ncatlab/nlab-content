

+-- {: .num_prop #CanonicalMomentum}
###### Proposition
**([[canonical momentum]])**


Consider a [[Lagrangian field theory]] $(E, \mathbf{L})$ whose [[Lagrangian density]] $\mathbf{L}$

1. does not depend on the [[spacetime]]-[[coordinates]] 

1. depends on spacetime derivatives of [[field (physics)|field]] coordinates (hence on [[jet bundle]] coordinates) at most to first order.  

Hence if the [[field bundle]] $E \overset{fb}{\to} \Sigma$ is a [[trivial vector bundle]] over [[Minkowski spacetime]] (example \ref{TrivialVectorBundleAsAFieldBundle}) this means to consider the case that

$$
  \mathbf{L} 
    \;=\; 
   L\left( 
     (\phi^a), (\phi^a_{,\mu}) 
   \right) \wedge dvol_\Sigma
  \,.
$$

Then the [[presymplectic current]] (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) is (up to possible a horizontally exact part) of the form

$$
  \Omega_{BFV}
   \;=\;
  \delta p_a^\mu 
  \wedge 
  \delta \phi^a
  \wedge 
  \iota_{\partial_\mu} dvol_\Sigma
$$

where

$$
  p_a^\mu 
    \;\coloneqq\;
  \frac{\partial L}{ \partial \phi^a_{,\mu}}
$$

denotes the [[partial derivative]] of the [[Lagrangian density|Lagrangian function]] with respect to the spacetime-[[derivatives]] of the [[field (physics)|field]] [[coordinates]].

Here 

$$
  \begin{aligned}
    p_a 
      & \coloneqq 
    p_a^0
    \\
      & =
    \frac{\partial L}{\partial \phi^a_{,0}}
  \end{aligned}
$$ 

is called the _[[canonical momentum]]_ corresponding to the "[[canonical coordinate|canonical field coordinate]]" $\phi^a$.

In the language of [[multisymplectic geometry]] the full expression

$$
  p_a^\mu \wedge \iota_{\partial_\mu} dvol_\Sigma
  \;\in\; 
  \Omega^{p,1}_\Sigma(E)
$$

is also called the "canonical multi-momentum", or similar.

=--

+-- {: .proof}
###### Proof

We compute as before:

$$
  \begin{aligned}
    \mathbf{d} \mathbf{L}
    & =
    \left(
      \frac{\partial L}{\partial \phi^a} \delta \phi^a
      + 
      \frac{\partial L}{\partial \phi^a_{,\mu}} \delta \phi^a_{,\mu}
    \right)
    \wedge
    dvol_\Sigma
    \\
    & =
    \left(
      \frac{\partial L}{\partial \phi^a}
      -
      \frac{d}{d x^\mu} \frac{\partial L}{\partial \phi^a_{,\mu}}
    \right)
    \wedge
    dvol_\Sigma
    -
    d
    \underset{
      \Theta_{BFV}
    }{ 
    \underbrace{
      \left(
        \frac{\partial L}{\partial \phi^a_{,\mu}} \delta \phi^a
      \right)
      \wedge
      \iota_{\partial_\mu} dvol_\Sigma
    }
    }
  \end{aligned}
  \,.
$$

Hence 

$$
  \begin{aligned}
    \Omega_{BFV}
    & \coloneqq
    \delta \Theta_{BFV}
    \\
    & =
    \delta
    \left(
      \frac{\partial L}{\partial \phi^a_{,\mu}}
      \delta \phi^a_{,\mu}
      \wedge \iota_{\partial_\mu} dvol_\Sigma
    \right)
    \\
    & =
     \delta
      \frac{\partial L}{\partial \phi^a_{,\mu}}
     \wedge
      \delta \phi^a_{,\mu}
      \wedge 
      \iota_{\partial_\mu} dvol_\Sigma
    \\
    & =
    \delta p_a^\mu \wedge \delta \phi^a \wedge \iota_{\partial_\mu} dvol_\Sigma
  \end{aligned}
$$

=--