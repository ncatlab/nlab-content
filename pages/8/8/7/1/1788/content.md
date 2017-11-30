
For

$$
  E \overset{fb}{\longrightarrow} \Sigma
$$

a [[fiber bundle]], regarded as a [[field bundle]], and for 

$$
  E' \overset{fb'}{\longrightarrow} \Sigma
$$

any other [[fiber bundle]] over the same base, we write

$$
  \Gamma_{J^\infty_\Sigma(E)}(E')
  \;\coloneqq\;
  \Gamma_{J^\infty_\Sigma(E)}( jb^\ast E' )
  \;=\;
  Hom_\Sigma(J^\infty_\Sigma(E), E')
  \;\simeq\; 
  DiffOp(E,E')
$$

for the [[space of sections]] of the [[pullback of bundles]] of $E'$ to the [[jet bundle]] $J^\infty_\Sigma(E) \overset{jb}{\longrightarrow} \Sigma$ along $jb$.

We write $T_\Sigma E$ for the [[vertical tangent bundle]], etc.

For example 

* $\Gamma_{J^\infty_\Sigma(E)}(T_\Sigma E)$ is the space of [[evolutionary vector fields]];

* $\Gamma_{J^\infty_\Sigma(E)}( T^\ast_\Sigma E) \otimes \wedge^{p+1}_\Sigma(T^\ast \Sigma)$ is the space of source forms

+-- {: .num_defn #FrechetDerivativeOfDifferentialOperator}
###### Definition

Let 

$$
  E \overset{fb}{\to} \Sigma
$$ 

be a [[field bundle]] and let

$$
  V \overset{vb}{\to} \Sigma
$$

be a [[vector bundle]] 

Then for

$$
  P \in \Gamma_{J^\infty_\Sigma(E)}(V)
$$

its _[[Fréchet derivative]]_ is the map

$$
  \array{
    \Gamma_{J^\infty_\Sigma(E)}(E)
      & \overset{  \mathrm{D}P }{\longrightarrow} &
    \Gamma_{J^\infty_\Sigma(E)}(V)
    \\
    v &\mapsto& \hat v(P) 
  }
$$

where $\hat v$ is the prolongation of $v$.

In the case that $E$ and $V$ are [[trivial vector bundles]] over [[Minkowski spacetime]] with coordinates $((x^\mu), (\phi^a))$ and $((x^\mu), (\rho^b))$, respectively, then this is given by

$$
  ((\mathrm{D}P)(v))^b
   \;=\;
  \left(
     v^a \frac{\partial P^b}{\partial \phi^a}
     +
     \frac{d v^a}{d x^\mu}  
     \frac{\partial P^b}{\partial \phi^a_{,\mu}}
     +
      \frac{d v^a}{d x^\mu d x^\nu}
      \frac{\partial  P^b}{\partial \phi^a_{,\mu \nu}}
      +
     \cdots
  \right)
$$

This shows that $\mathrm{D}P$ may equivalently be regarded as a $J^\infty_\Sigma(E)$-dependent differential operator from $T_\Sigma E$ to $V$

$$
  \mathrm{D}_P
  \;\colon\;
  J^\infty_\Sigma(E) \times_\Sigma J^\infty_\Sigma T_\Sigma E
  \longrightarrow
  V   
$$

in that

$$
  \label{FrechetDerivativeAsDifferentialOperatorEquality}
  \mathrm{D}_P(-,v)
  =
  \mathrm{D}P(v)
  = 
  \hat v (P)
  \,.
$$

=--


+-- {: .num_example}
###### Example

Over [[Minkowski spacetime]] $\Sigma$, let $\mathbf{L} = L dvol \in \Omega^{p,0}_\Sigma(E)$ be a [[Lagrangian density]], with coefficient function regarded as

$$
  L \;\in \; \Gamma_{J^\infty_\Sigma}(E)(\Sigma \times \mathbb{R})
  \,,
$$

Then the [[formally adjoint differential operator|formal adjoint]]  

$$
  (\mathrm{D}_L)^\ast
    \;\colon\;
  J^\infty_\Sigma(E)\times_\Sigma (\Sigma \times \mathbb{R})^\ast
  \longrightarrow
  T_\Sigma^\ast E
$$


of its Frechet derivative def. \ref{FrechetDerivativeOfDifferentialOperator}, regarded as a $J^\infty_\Sigma(E)$-dependent differential operator $\mathrm{D}_P$ from $T_\Sigma$ to $V$ and applied to the constant section 

$$
  1 \in \Gamma_\Sigma(\Sigma \times \mathbb{R}^\ast)
$$

is the [[Euler-Lagrange derivative]]

$$
  \delta_{EL}\mathbf{L}
  \;=\;
  \left(\mathrm{D}_{L}\right)^\ast(1)
  \;\in\;
  \Gamma_{J^\infty_\Sigma(E)}(T_\Sigma^\ast)
   \simeq
   \Omega^{p+1,1}_\Sigma(E)_{source}
$$

=--

+-- {: .num_prop #EulerLagrangeDerivativeIsDerivationViaAdjointFrechetDerivatives}
###### Proposition

Let $V \overset{vb}{\to} \Sigma$ be a [[vector bundle]] and write $V^\ast \overset{}{\to} \Sigma$ for its [[dual vector bundle]]. 

For $\alpha \in \Gamma_\Sigma(V)$ and $\beta^\ast \in \Gamma_\Sigma(E^\ast)$ we have

$$
  \delta_{EL}( \alpha \cdot \beta^\ast )
  \;=\;
  (\mathrm{D}_\alpha)^\ast(\beta^\ast)
  + 
  (\mathrm{D}_{\beta^\ast})^\ast(\alpha)
$$

=--


+-- {: .proof}
###### Proof

By the [[product law]]

$$
  \begin{aligned}
    \frac{
      \delta_{EL} \left(\alpha \cdot \beta^\ast \right)
    }
    {
      \delta \phi^a
    }
    & =
    \frac{\partial \left(\alpha \cdot \beta^\ast \right)}{\partial \phi^a}
    -
    \frac{d}{d x^\mu}
    \left(
       \frac{\partial \left( \alpha \cdot \beta^\ast \right)}{\partial \phi^a_{,\mu}}
    \right)
    +
    \frac{d}{d x^\mu d x^\nu}
    \left(
       \frac{\partial \left( \alpha \cdot \beta^\ast \right) }{\partial \phi^a_{,\mu \nu}}
    \right)  
    -
    \cdots
    \\
    & =
    \phantom{+}
    \frac{\partial \alpha }{\partial \phi^a}
    \cdot \beta^\ast
    -
    \frac{d}{d x^\mu}
    \left(
       \frac{\partial \alpha }{\partial \phi^a_{,\mu}}
       \cdot 
       \beta^\ast
    \right)
    +
    \frac{d}{d x^\mu d x^\nu}
    \left(
       \frac{\partial \alpha  }{\partial \phi^a_{,\mu \nu}}
       \cdot 
       \beta^\ast
    \right)  
    -
    \cdots
    \\
    & \phantom{=}
    +
    \frac{\partial \beta^\ast }{\partial \phi^a}
    \cdot \alpha
    -
    \frac{d}{d x^\mu}
    \left(
       \frac{\partial \beta^\ast }{\partial \phi^a_{,\mu}}
       \cdot 
       \alpha
    \right)
    +
    \frac{d}{d x^\mu d x^\nu}
    \left(
       \frac{\partial \beta^\ast  }{\partial \phi^a_{,\mu \nu}}
       \cdot 
       \alpha
    \right)  
    -
    \cdots
    \\
    & =
    (\mathrm{D}_\alpha)^\ast(\beta^\ast)
    + 
    (\mathrm{D}_{\beta^\ast})^\ast(\alpha)
  \end{aligned}
$$

=--

+-- {: .num_prop }
###### Proposition

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]]. If an [[evolutionary vector field]] $v$ is an [[infinitesimal symmetry of the Lagrangian]] then the [[flow]] along its prolongation $\hat v$ preserves the [[prolonged shell]] $\mathcal{E}^\infty \hookrightarrow J^\infty_\Sigma(E)$ in that the [[Lie derivative]] of the [[Euler-Lagrange form]] $\delta_{EL}\mathbf{L}$ along $\hat v$ vanishes on $\mathcal{E}^\infty$:

$$
  \mathcal{L}_{\hat v}\mathbf{L} = 0 \, mod\, im(d)
  \phantom{AAA}
  \Rightarrow
  \phantom{AAA}
  \mathcal{L}_{\hat v} \delta_{EL}\mathbf{L}\vert_{\mathcal{E}^\infty} = 0 
  \,.
$$ 

=--

+-- {: .proof}
###### Proof

Notice that for any vector field $\hat v$ the [[Lie derivative]] $\mathcal{L}_{\hat v}$ of the [[Euler-Lagrange form]] $\delta_{EL}\mathbf{L} = \frac{\delta_{EL}\mathbf{L}}{\delta \phi^a} \delta \phi^a dvol_\Sigma$ differs from that of its component functions $\frac{\delta_{EL}\mathbf{L}}{\delta \phi^a} dvol_\Sigma$ by a term proportional to these component functions, which by definition vanishes on-shell. But the Lie derivative of the component functions is just their plain derivative. So it is sufficient to show that 

$$
  \hat v
  \left(
    \frac{\delta_{EL} L}{\delta \phi^a}
  \right)
  \vert_{\mathcal{E}^\infty}
  \;=\;
  0
  \,.
$$ 

Now by [[Noether's theorem]] the condition $\mathcal{L}_{\hat v} = d \tilde J_{\hat v}$ implies that 

$$
  \iota_{\hat v} \delta_{EL}\mathbf{L}
  \;=\;
  d J_{\hat v}
  \,.
$$

Since the right hand side is horizontally exact, the [[Euler-Lagrange derivative]] applied to the right hand vanishes, hence

$$
  \begin{aligned}
    0 
    & =
    \frac{\delta_{EL} \left( v \cdot \delta_{EL} L\right) }{ \delta \phi^a }
    \\
    & =
    (\mathrm{D}_{v})^\ast( \delta_{EL}L )
    +
    (\mathrm{D}_{\delta_{EL}L})^\ast(v)
    \\
    & =
    (\mathrm{D}_{v})^\ast( \delta_{EL}L )
    +
    (\mathrm{D}_{\delta_{EL}L})(v)
    \\
    & =
    (\mathrm{D}_{v})^\ast( \delta_{EL}L )
    +
    \hat v(\delta_{EL}L)
    \,.
  \end{aligned}
$$

Here the first step is by prop. \ref{EulerLagrangeDerivativeIsDerivationViaAdjointFrechetDerivatives}, the second step is by ... and the third step is
(eq:FrechetDerivativeAsDifferentialOperatorEquality).

Hence

$$
  \begin{aligned}
    \hat v(\delta_{EL}L) \vert_{\mathcal{E}^\infty}
    & =
    -
    (\mathrm{D}_{v})^\ast( \delta_{EL}L ) \vert_{\mathcal{E}^\infty}
    \\
    & = 
    0
  \end{aligned}
  \,,
$$

where in the last line we used that on the [[prolonged shell]] $\delta_{EL}L$ and all its horizontal derivatives vanish, by definition.


=--

