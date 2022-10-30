



Let $(E, \mathbf{L})$ be a [[Lagrangian field theory]]. Assume for simplicity of exposition that the [[field bundle]] 


$E \overset{fb}{\to}\Sigma$ is a [[trivial vector bundle]] over [[Minkowski spacetime]] and that $(\phi^a)_{a = 1}^s$ is a [[linear basis]] for its [[typical fiber]]. This means that the [[jet bundle]] $J^\infty_\Sigma(E)$ has canonical coordinates given by

$$
  \left(
    (x^\mu), (\phi^a), (\phi^a_{,\mu}), (\phi^a_{,\mu_1 \mu_2}), \cdots
  \right)
  \,.
$$

Here the $\phi^a$ are also called the _[[field (physics)|field]] [[coordinates]]_.


+-- {: .num_defn #EvolutionaryVectorField}
###### Definition
**([[evolutionary vector fields]] and [[antifields]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[fiber bundle]]. Then an [[evolutionary vector field]] $v$ is a smooth bundle morphism

$$
  \array{
    J^\infty_\Sigma(E)
    && \overset{v}{\longrightarrow} &&
    V_\Sigma E
    \\
    & {}_{\mathllap{jb_{\infty,0}}}\searrow && \swarrow_{\mathllap{}}
    \\
    && E
  }
  \,.
$$

We write

$$
  \Gamma_\Sigma^{ev}(T J^\infty_\Sigma(E))
  \;\in\;
  \Omega^{0,0}_\Sigma(E) Mod^{\mathbb{Z}}
$$

for the space of evolutionary vector fields, 
regarded as a [[graded module]] over the $\mathbb{R}$-[[associative algebra|algebra]]

$$
  \Omega^{0,0}_\Sigma(E)
  \;=\;
  C^\infty\left( J^\infty_\Sigma(E) \right)
$$

of [[smooth functions]] on the [[jet bundle]].

For the construction of the [[BV-BRST complex]] in the following, we will want to 
assign a _degree_ to evolutionary vector field, namely degree -1. 
The above module regarded as a [[graded module]] concentrated all in degree -1
is denoted by

$$
  \Gamma_\Sigma^{ev}(T J^\infty_\Sigma(E))[-1]
  \;\in\;
  \Omega^{0,0}_\Sigma(E) Mod^{\mathbb{Z}}^{\mathbb{Z}}
  \,.
$$


In the special case that $E \overset{fb}{\to} \Sigma$ is a [[trivial vector bundle]]
with [[field (physics)|field]] [[coordinates]] $(\phi^a)_{a = 1}^s$ as in example \ref{TrivialVectorBundleAsAFieldBundle}, then 
we write 

$$
  \overline \phi_a \;\coloneqq\; \partial_{\phi^a}[-1]
$$

for the induced basis elements of the space of those  [[vector fields]] on the [[jet bundle]] (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) which are dual to the field coordinates,
but regarded in degree -1. These then provide a [[linear basis]] for the space of evolutionary vector fields
in that the canonical linear map is an [[isomorphism]] of [[graded modules]]:

$$
  \label{AntifieldCoordinates}
  \Omega^{0,0}_\Sigma(E)
  \langle
     \overline{\phi}_a
  \rangle
    \overset{\simeq}{\longrightarrow}
  \Gamma_\Sigma^{ev}(V_\Sigma(E))[-1]
  \,.
$$

These generators $\overline{\phi}_a$ in degree -1 are called the _[[antifield]] coordinates_ 
corresponding to the [[field (physic)|field]] coordinates $\phi^a$.

=--


+-- {: .num_defn #ImplicitInfinitesimalGaugeSymmetry}
###### Definition
**(implicit [[infinitesimal gauge symmetry]])**

Given a [[Lagrangian field theory]] $(E, \mathbf{L})$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}),
then an _implicit [[infinitesimal gauge symmetry]]_ is an [[evolutionary vector field]] 
$\epsilon \in \Gamma_\Sigma^{ev}(V_\Sigma E)$
on which the [[Euler-Lagrange variational derivative]] (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) 
vanishes:

$$
  \iota_\epsilon \delta_{EL}\mathbf{L} = 0
  \,.
$$

In the special case that the [[field bundle]] $E \overset{fb}{\to} \Sigma$ is a [[trivial vector bundle]]
over [[Minkowski spacetime]] (example \ref{TrivialVectorBundleAsAFieldBundle}) 
with [[field (physics)|field]] coordinates $(\phi^a)$ and $(\overline{\phi}_a)$
and [[antifield]] coordinates $\overline{\phi}_a$ (eq:AntifieldCoordinates) an 
[[evolutionary vector field]] has an expansion of the form

$$
  \epsilon = R^a \partial_{\phi^a}
$$

where $(R^a \in \Omega^{0,0}_\Sigma(E))_{a = 1}^s$ are smooth functions on the jet bundle; and in terms
of these coordinates the condition on $\epsilon$ to be a gauge symmetryis equivalent to the condition

$$
  R^a \frac{\delta_{EL} L}{ \delta \phi^a} = 0 \phantom{AAA} \in \Omega^{0,0}_\Sigma(E)
  \,.
$$


=--


+-- {: .num_example #TrivialImplicialInfinitesimalGaugeTransformations}
###### Example
**(trivial implicial infinitesimal gauge transformations)**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

Then every [[evolutionary vector field]] (def. \ref{EvolutionaryVectorField}) of the special form

$$
  \epsilon 
  \coloneqq
  \frac{\delta_{EL} L }{\delta \phi^a} \kappa^{[a b]} \partial_{\phi^a}
  \;\in\;
  \Gamma_\Sigma^{ev}(V_\Sigma E)
$$

for a collection of smooth functions $(\kappa^{[a b]} \in \Omega^{0,0}_\Sigma(E))$ which is 
skew-symmetric in its indices ($\kappa^{[a b]} = - \kappa^{[b a]}$) is an 
implicit infinitesimal gauge symmetry (def. \ref{ImplicitInfinitesimalGaugeSymmetry}).

But since this is so for a "trivial reason" namely just that skew symmetry:

$$
  \iota_\epsilon \delta_{EL} \mathbf{L}
  =
  \undeerset{= 0}{
  \underbrace{
   \left( \frac{\delta_{EL} L }{\delta \phi^a} \right)
   \left( \frac{\delta_{EL} L }{\delta \phi^b} \right)
   \kappa^{[a b]}
  }
  }
  \, 
  dvol_\Sigma
$$

these are called the _trivial_ implicit infinitesimal gauge transformations.

=--


+-- {: .num_prop}
###### Proposition

For $(E, \mathbf{L})$ a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}), then 
every implicit [[infinitesimal gauge symmetry]] $\epsilon$ (def. \ref{ImplicitInfinitesimalGaugeSymmetry})
is in particular an [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents})
in that 

$$
  \iota_\epsilon \delta \mathbf{L}
   \;=\;
  d \tilde J_\epsilon
$$

for some $\tilde J_\epsilon$. Moreover, the  [[conserved currents]] associated to 
such $\epsilon$ by [[Noether's theorem]] (prop. \ref{NoethersFirstTheorem}) vanish identically.


=--

+-- {: .proof}
###### Proof

This follows directly from the definitions: Using $\delta \mathbf{L} = \delta_{EL} \mathbf{L} + d \Theta$
(prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) and the defining property
$\iota_\epsilon \delta_{EL}\mathbf{L} = 0$ (def. \ref{ImplicitInfinitesimalGaugeSymmetry})
together with the verticality of $\epsilon$ ($\iota_{\epsilon} \circ d = - d \circ \iota_{\epsilon}$)
we have:

$$
  \begin{aligned}
    \iota_\epsilon \delta \mathbf{L}
      & =
    \iota_\epsilon
    \left(
      \delta_{EL} \mathbf{L}
       -
      d \Theta
    \right)
    \\
    & =
    \underset{
      = 0
    }{
    \underbrace{
      \iota_\epsilon \delta_{EL}\mathbf{L}
    }
    }
    -
    \underset{ = - d \iota_\epsilon \Theta}{
    \underbrace{
      \iota_\epsilon d \Theta
    }
    }
    \\
    & =
    d \underset{ = \tilde J_\epsilon }{\underbrace{ \iota_\epsilon \Theta }}
  \end{aligned}
$$


=--


+-- {: .num_defn}
###### Definition
**([[BV-complex]] of ordinary [[Lagrangian density]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})

Evaluation of [[evolutionary vector fields]] (def. \ref{EvolutionaryVectorField}) in the [[Euler-Lagrange variational derivative]] $\delta_{EL} \mathbf{L} \in \Omega^{p,0}_\Sigma(E) \wedge \delta \Omega^{0,0}_\Sigma(E)$ (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) yields a $\Omega^{0,0}_\Sigma(E)$-[[linear map]] 
(of degree +1 if we consider the evolutionary vector fields in degree -1)

$$
  \iota_{\delta_{EL}\mathbf{L}}
  \;\colon\;
  \Gamma_\Sigma^{ev}(V_\Sigma E)[-1]
    \longrightarrow
  \Omega^{p+1,0}_\Sigma(E)
  \,.
$$

If we use the [[volume form]] $dvol_\Sigma$ on [[spacetime]] $\Sigma$ to induce an identification

$$
  \Omega^{p+1,0}_\Sigma(E) \;\simeq\; C^\infty(J^\infty_\Sigma(E))\langle dvol_\sigma\rangle
$$

with respect to which the [[Lagrangian density]] decomposes as

$$
  \mathbf{L} = L dvol_\Sigma
$$

then this is a linear map of the form

$$
  \iota_{\delta_{EL} L}
  \;\colon\;
  \Gamma_\Sigma^{ev}(V_\Sigma E)[-1]
    \longrightarrow
  \Omega^{0,0}_\Sigma(E)
  \,.
$$

In the special case that the [[field bundle]] $E \overset{fb}{\to} \Sigma$ is a [[trrivial vector bundle]]
(example \ref{TrivialVectorBundleAsAFieldBundle}) with [[field (physics)|field]] coordinates $(\phi^a)$
so that the Euler-Lagrange variational derivative has the expansion 

$$
  \delta_{EL}L
  \;=\;
  \frac{\delta_{EL} L}{\delta \phi^a} \delta \phi^a
$$

then this map is given on the [[antifield]] basis elements (eq:AntifieldCoordinates) by

$$
  \iota_{\delta_{EL}L}
  \;\colon\;
  \overline{\phi}_a
  \;\mapsto\;
  \frac{\delta_{EL} L}{\delta \phi^a}
  \,.
$$

Consider then the [[symmetric algebra|graded symmetric algebra]]

$$
  Sym_{\Omega^{0,0}_\Sigma(E)}\left(
    \Gamma_\Sigma^{ev}(V_\Sigma E)[-1]
  \right)
$$

which is generated over $\Omega^{0,0}_\Sigma(E)$ from the [[evolutionary vector fields]] in degree -1, and let

$$
  \delta_{BV}
  \;\colon\;
    Sym_{\Omega^{0,0}_\Sigma(E)}\left(
    \Gamma_\Sigma^{ev}(V_\Sigma E)[-1]
  \right)
  \;\longrightarrow\;
  Sym_{\Omega^{0,0}_\Sigma(E)}\left(
    \Gamma_\Sigma^{ev}(V_\Sigma E)[-1]
  \right)
$$

be the unique extension of the linear map $\iota_{\delta_{EL}L}$ to a [[derivation]] of degree +1 on this algebra.

The resulting [[differential graded-commutative algebra]] 

$$
  \left(
    Sym_{\Omega^{0,0}_\Sigma(E)}\left(
      \Gamma_\Sigma^{ev}(V_\Sigma E)[-1]
    \right)
    \,,\,
    \delta_{BV}
  \right)
$$

is called the _[[BV-complex]]_ of the Lagrangian field theory.

=--

The [[cochain cohomology]] of the [[BV-comples]] has the following interpretation:


in degree 0:


$$
  im( \Gamma_\Sigma^{ev}(V_\Sigma(E)) \overset{\delta_{BV}}{\to} \Omega^{0,0}_\Sigma(E))
$$

is functions on the [[shell]].

in degree -1:

$$
  ker( \Gamma_\Sigma^{ev}(V_\Sigma(E)) \overset{\delta_{BV}}{\to} \Omega^{0,0}_\Sigma(E))
$$

is the implicit [[infinitesimal gauge symmetries]] (def. \ref{ImplicitInfinitesimalGaugeSymmetry})

and

$$
  im( 
    \Gamma_{\Sigma}^{ev}(V_\Sigma E) \wedge_{\Omega^{0,0}_\Sigma(E)} \Gamma_\Sigma^{ev}(V_\Sigma E)  
      \overset{\delta_{BV}}{\longrightarrow}
    \Gamma_{\Sigma}^{ev}(V_\Sigma E)
  )
$$

is the trivial implicit infinitesimal gauge transformations (example \ref{TrivialImplicialInfinitesimalGaugeTransformations}).
    

## References

* {#HennauxTeitelboim91} [[Marc Henneaux]], [[Claudio Teitelboim]], _Quantization of Gauge Systems_, Princeton University Press 1991



