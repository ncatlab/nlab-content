
...



$$
  [\delta, ]
$$

$$  
  s_{BV}
  \;=\;
  \frac{\delta_{EL}L}{\delta \phi^a}
  \frac{\partial}{\partial \overline{\phi}^a}
$$


$$ 
  \begin{aligned}
    \left[
      \tfrac{1}{2}\int \int \Delta^{a b}_F(x,y) \frac{\delta}{\delta \Phi^a(x)} \frac{\delta}{\delta \Phi^b(y)}
      \, dvol(x)\, dvol(y)
      \;,\;
      \int
        P\Phi^a(z)\frac{\delta}{\delta \overline{\Phi}^a(z)}
       dvol(z)
    \right]
    & =
    \int \int \int
     \underset{= \delta(x-y)}{
       \underbrace{\Delta^{a b}_F(x,y) P_y}
     } \delta(y-z)
     \frac{\delta}{\delta \Phi^a(x)}
     \frac{\delta}{\delta \overline{\Phi}^b(z)}
     \,dvol(x)\, dvol(y) \, dvol(z)
    \\
    & =
    \int 
      \frac{\delta}{\delta \Phi^a(x)}
      \frac{\delta}{\delta \overline{\Phi}^a(x)}
      \, dvol(x) 
 \end{aligned}
$$

$\,$

$\,$

$\,$

+-- {: .num_example #BField}
###### Example
**([[field bundle]] for [[B-field]])**

On [[Minkowski spacetime]] $\Sigma$ (def. \ref{MinkowskiSpacetime}), let the [[field bundle]] (def. \ref{FieldsAndFieldBundles}) be given by the
skew-symmetrized [[tensor product of vector bundles]] of the [[cotangent bundle]] with itself

$$
  E \coloneqq \wedge^2_\Sigma T^\ast \Sigma
  \,.
$$

This is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) with canonical [[field (physics)|field]] coordinates $(b_{\mu \nu})$ subject to 

$$
  b_{\mu \nu} \;=\; - b_{\nu \mu}
  \,.
$$

A [[section]] of this bundle, hence a [[field history]], is a [[differential 2-form]] (def. \ref{DifferentialnForms})

$$
  B \in \Gamma_\Sigma(\wedge^2_\Sigma T^\ast \Sigma) = \Omega^2(\Sigma)
$$

on [[spacetime]]. 

=--

+-- {: .num_example #BFieldJetFaraday}
###### Example
**(universal [[B-field|B-]][[field strength]] on [[jet bundle]])**

Consider the [[field bundle]] (def. \ref{FieldsAndFieldBundles}) of the [[B-field]] (example \ref{BField})
over [[Minkowski spacetime]] $\Sigma$ (def. \ref{MinkowskiSpacetime}) with jet coordinates
$((x^\mu), (b_{\mu \nu}), (b_{\mu \nu,\rho}), \cdots )$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}). Consider the functions on the [[jet bundle]] given by the linear combinations

$$
  \label{BFieldFaradayTensorJet}
  \begin{aligned}
    h_{\mu_1 \mu_2 \mu_3}
      & \coloneqq
    \tfrac{1}{2}
      b_{[\mu_1 \mu_2, \mu_3]}
    \\
    & \coloneqq
     \tfrac{1}{6}
    \left(
      \underset{ \sigma \atop  \text{permutation} }{\sum}
      (-1)^{ {\vert \sigma \vert} }
      b_{\mu_{\sigma_1} \mu_{\sigma_2}, \mu_{\sigma_3}}
    \right)
    \\
    & =
    b_{\mu_1 \mu_2, \mu_3}
    +
    b_{\mu_2 \mu_3, \mu_1}
    +
    b_{\mu_3 \mu_1, \mu_2}
    \,,
  \end{aligned}
$$

where in the last step we used that $b_{\mu \nu} = - b_{\nu \mu}$.

=--



+-- {: .num_example #ElectromagnetismEl}
###### Example
**([[Euler-Lagrange form]] for [[free field|free]] [[B-field]])**

Consider the [[Lagrangian field theory]] of the [[free field|free]] [[B-field]] from example \ref{spring}.

The [[Euler-Lagrange variational derivative]] is

$$
  \delta_{EL} \mathbf{L}
  \;=\;
  h^{\mu \nu \rho}{}_{,\rho} \delta b_{\mu \nu}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By (eq:EulerLagrangeEquationGeneral) we have

$$
  \begin{aligned}
    \frac{\delta_{EL} L}{\delta b_{\mu \nu}} \delta b_{\mu \nu}
    & =
    \left(
      \underset{
        = 0
      }{
      \underbrace{
        \frac{\partial}{\partial b_{\mu \nu}}
        \tfrac{1}{2} b_{[\mu_1 \mu_2, \mu_3]} b^{[\mu_1 \mu_2, \mu_3]}
      }
      }
      -
      \frac{d}{d x^\rho}
      \frac{\partial}{\partial b_{\mu \nu, \rho}}
        \tfrac{1}{2} b_{[\mu_1 \mu_2, \mu_3]} b^{[\mu_1 \mu_2, \mu_3]}
    \right)
    \delta b_{\mu \nu}
    \\
    & =
    -
    \left(
      \frac{d}{d x^\rho}
      \frac{\partial}{\partial b_{\mu \nu, \rho}}
        \tfrac{1}{2} b_{\mu_1 \mu_2, \mu_3} b^{[\mu_1 \mu_2, \mu_3]}
    \right)
    \delta b_{\mu \nu}
    \\
    & =
    -
    \left(
      \frac{d}{d x^\rho}
      b^{[\mu \nu, \rho]}
    \right)
    \delta b_{\mu \nu}
    \\
    & =
    -
    h^{\mu \nu \rho}{}_{,\rho} \delta b_{\mu \nu}
    \,.
  \end{aligned}
$$


=--


$\,$

$$
  \{b_{\mu \nu}, (b_{\mu \nu, \mu_1}), (b_{\mu \nu, \mu_1 \mu_2}), \cdots\}
$$

$$
  h_{\mu \nu \rho}
  \coloneqq
  b_{[\mu \nu, \rho]}
$$

$$
  L 
   \coloneqq
  \tfrac{1}{2} h_{\mu \nu \rho} h^{\mu \nu \rho}
$$

$$
  \frac{\delta_{EL} L}{\delta b_{\mu \nu}}
  =
 
$$