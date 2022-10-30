


+-- {: .num_defn #EvolutionaryVectorField}
###### Definition
**([[evolutionary vector field]])**

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
$$

=--


Let $(E, \mathbf{L})$ be a [[Lagrangian field theory]]. Assume for simplicity of exposition that the [[field bundle]] $E \overset{fb}{\to}\Sigma$ is a [[trivial vector bundle]] over [[Minkowski spacetime]] and that $(\phi^a)_{a = 1}^s$ is a [[linear basis]] for its [[typical fiber]]. This means that the [[jet bundle]] $J^\infty_\Sigma(E)$ has canonical coordinates given by

$$
  \left(
    (x^\mu), (\phi^a), (\phi^a_{,\mu}), (\phi^a_{,\mu_1 \mu_2}), \cdots
  \right)
  \,.
$$

Here the $\phi^a$ are also called the _[[field (physics)|field]] [[coordinates]]_.

Consider then the space of [[evolutionary vector fields]] on the [[jet bundle]] (def. \ref{EvolutionaryVectorField})

$$
  \Gamma_\Sigma^{ev}(T J^\infty_\Sigma(E))[-1]
  \;\in\;
  \Omega^{0,0}_\Sigma(E) Mod^{\mathbb{Z}}
$$

regarded as a [[graded module]], concentrated in degree -1, over the $\mathbb{R}$-[[associative algebra|algebra]] 

$$
  \Omega^{0,0}_\Sigma(E)
  \;=\;
  C^\infty\left( J^\infty_\Sigma(E) \right)
$$ 

of [[smooth functions]] on the [[jet bundle]].


If 

$$
  \overline \phi_a \;\coloneqq\; \partial_{\phi^a}[-1] 
$$ 

denotes the canonical basis elements of the space of [[vector fields]] on the [[jet bundle]] which are dual to the field coordinates, and regarded in degree -1, then by (...) these span the space of [[evolutionary vector fields]] in that we have an [[isomorphism]] of [[graded modules]] of the form

$$
  \Gamma_\Sigma^{ev}(V_\Sigma(E))[-1]
    \;\simeq\;
  \Omega^{0,0}_\Sigma(E)
  \langle 
     \overline{\phi}_a
  \rangle
  \,.
$$

Evaluation of [[evolutionary vector fields]] in the [[Euler-Lagrange variational derivative]] $\delta_{EL} \mathbf{L} \in \Omega^{p,0}_\Sigma(E) \wedge \delta \Omega^{0,0}_\Sigma(E)$ yields a $\Omega^{0,0}_\Sigma(E)$-[[linear map]] of degree +1

$$
  \iota_{\delta_{EL}\mathbf{L}}
  \;\colon\;
  \Gamma_\Sigma^{ev}(V_\Sigma E)[-1]
    \longrightarrow
  \Omega^{p+1,0}_\Sigma(E)
  \,.
$$

If we use the [[volume form]] $dvol_\Sigma$ on [[spacetime]] $\Sigma$, regarded as an a horizontal $p+1$-form on the jet bundle, to induce an identification 

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


Moreover if we use the given canonical coordinates, in which the Euler-Lagrange form is expanded as


$$
  \delta_{EL}\mathbf{L}/dvol_\Sigma
  =
  \delta_{EL}L
  \;=\;
  \frac{\delta_{EL} L}{\delta \phi^a} \delta \phi^a
$$

then the components of this map are

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

The [[cochain cohomology]] of $\delta_{BV}$ has the following interpretation:


in degree 0:

$$
  im( \Gamma_\Sigma^{ev}(V_\Sigma(E)) \overset{\delta_{BV}}{\to} \Omega^{0,0}_\Sigma(E))
$$
 
is functions on the [[shell]].

in degree 1: 

$$
  im( \Gamma_\Sigma^{ev}(V_\Sigma(E)) \overset{\delta_{BV}}{\to} \Omega^{0,0}_\Sigma(E))
$$

is the [[gauge symmetries]]



