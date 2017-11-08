$x {\color{red}\le} y$


For $E \overset{fb}{\to} \Sigma$ a [[field bundle]] (def. \ref{Fields})
and $\mathbf{L} \in \Omega^{p+1}_\Sigma(E)$ a [[Lagrangian density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
then of course for every [[real number]] $r \in \mathcal{R}$ of course also the multiple

$$
  r \mathbf{L} \in \Omega^{p+1}_\Sigma(E)
$$

is a Lagrangian density. Moreover, by prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}
this rescaled Lagrangian induces correspondingly rescaled [[Euler-Lagrange forms]] and [[presymplectic currents]].

But the [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] (eq:EulerLagrangeEquationGeneral)
for the rescaled Lagrangian is clearly equivalent to that of the original Lagrangian: they have the same solutions.
Similarly, later we see that the rescaled [[presymplectic current]] induced the same [[quantizations]]
as the original presymlectic current does (the difference may be absorbed in a redefinition of [[Planck's constant]]).

Therefore for [[quantum field theory]] globally defined Lagrangian densities matter only
up to rescaling of the Lagrangian (for [[locally variational field theories]], remark \ref{LocallyVariationalFieldTheory},
the situation is more subtle).

But consider the case of a [[field bundle]] $E \overset{fb}{\to} \Sigma$ over [[Minkowski spacetime]] $\Sigma = \mathbb{R}^{p+1}$ (def. \ref{MinkowskiSpacetime}). Then rescaling of _[[spacetime]] [[coordinates]]_ 

$$
  \array{
    \mathbb{R}^\times \times \mathbb{R}^{p+1} \longrightarrow  \mathbb{R}^{p,1}
  }
$$

extends to an [[action]] of the multiplicative [[group]] $\mathbb{R}^\times$ of non-zero [[real numbers]] to the total space of the [[jet bundle]]

$$
  sc 
    \;\colon\;   
  \mathbb{R}^\times \times J^\infty_\Sigma(E) 
    \longrightarrow
  J^\infty_\Sigma(E)
$$

given on induced jet coordinates by

$$
  \begin{aligned}
    x^\mu & \mapsto r x^\mu
    \\
    \phi^a & \mapsto \phi^a
    \\
    \phi^a_{,\mu_1, \cdots \mu_k} & \mapsto r^{-k} \phi^a_{,\mu_1 \cdots \mu_k}
  \end{aligned}
  \,.
$$

Let then

$$
  \mathbf{L}_{(-)}
   \;\colon\;
  \mathbb{R}^1 \longrightarrow \mathbf{\Omega}^{p+1}(J^\infty_\Sigma(E))
$$

be a smooth collection of [[Lagrangian densities]] depending on one parameter,
and consider the $R^\times$-[[action]] on the parameter given by

$$
  \array{
    \mathbb{R}^\times \times \mathbb{R}^1 &\longrightarrow& \mathbb{R}^1
    \\
    (r, m) &\mapsto& r^{w} m
  }
$$

for some $w \in \mathbb{Z}$.

If this is such that the _combined_ rescaling changes the Lagrangian only up to a multiple, in that

$$
  sc^\ast_r \mathbf{L}_{sc_r(-)} = f(r) \mathbf{L}_{(-)}
$$

then we say that this parameter is _proportional to a [[physical unit]] of $length^{w}$_.


+-- {: .num_example #DiracCurrent}
###### Example
**([[Dirac current]])**

Consider the [[Lagrangian field theory]] of the [[free field theory|free]] [[Dirac field]] on [[Minkowski spacetime]] in spacetime dimension $p + 1 = 3+1$ (example \ref{LagrangianDensityForDiracField}) 

$$
  \mathbf{L} = i \overline{\psi} \gamma^\mu \psi_{,\mu} \, dvol_\Sigma
  \,.
$$

Then the prolongation (prop. \ref{EvolutionaryVectorFieldProlongation}) of the [[evolutionary vector field]] (def. \ref{EvolutionaryVectorField})

$$
  v \;\coloneqq\; i \psi_\alpha \partial_{\psi_\alpha}
$$

is an [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents}). The [[conserved current]] that corresponds to this under [[Noether's theorem|Noether's theorem I]] (prop. \ref{NoethersFirstTheorem}) is 

$$
  \overline{\psi} \gamma^\mu \psi \, \iota_{\partial_\mu} dvol_\Sigma
  \;\in\;
  \Omega^{p,0}_{\Sigma(E)}
  \,.
$$

This is called the _[[Dirac current]]_.

In fact, due to the [[supergeometry|supergeometric]] nature of the [[Dirac field]], the [[Dirac current]] is conserved even [[off-shell]], as discussed in remark \ref{LagrangianDensityOfDiracFieldSupergeometricNature}.

=--


+-- {: .proof}
###### Proof


The prolongation (eq:ProlongationOfEvolutionaryVectorFieldExplicit) of $v$ is 

$$
  \hat v 
    = 
  i \psi_\alpha \partial_{\psi_\alpha}
    +
  i \psi_{\alpha,\mu} \partial_{\psi_{\alpha,\mu}}
    + 
   \cdots
  \,.
$$

Therefore

$$
  \begin{aligned}
    \mathcal{L}_v \left( 
      i \overline{\psi} \gamma^\mu \psi_{,\mu}
    \right) 
    dvol_\Sigma
    & =
    \underset{
      = i \cdot (-i) \overline{\psi} \gamma^\mu \psi_{,\mu}
    }{
    \underbrace{
      i \overline{i \psi} \gamma^\mu \psi_{,\mu}
    }
    }
    dvol_\Sigma
    +  
    \underset{
      i \cdot i \overline{\psi} \gamma^\mu \psi_{,\mu}
    }{   
    \underbrace{
      i \overline{\psi} \gamma^\mu (i \psi_{,\mu})
    }
    }
    dvol_\Sigma
    \\ & =
    0
  \end{aligned}
$$

=--

Let 

$$
  \mathbf{L}_{(-)}
  \;\colon\;
  \mathbb{R}^k \longrightarrow \mathbf{\Omega}^{p+1}(J^\infty_\Sigma(E))
$$

be a $k$-parameter collection of Lagrangian densities



Let $\Sigma$ be a [[Euclidean space]] equipped with 

1. a [[Riemannian metric]] $g$;

1. a [[real number]] $m \in \mathbb{R}$.

Using this [[structure]] $(g,m)$ we may formulate the [[Klein-Gordon equation]] $(\Box - m^2) \Phi = 0$ on $\Sigma$.

Now let $X$ be another Euclidean space, thought of as the actual observed spacetime. To say that $(\Sigma,g)$ is a model for our spacetime is to choose a diffeomorphism

$$
  \kappa \;\colon\; X \overset{\simeq}{\longrightarrow} \Sigma
$$

such that the length measured on $X$ is that given by the pullback metric $\kappa^\ast g$.

We might then think that we can equip $X$ with Klein-Gordon structure as above

$$
  (X, \kappa^\ast g, m)
$$

But this would be wrong: If $\Phi$ is a solution to the Klein-Gordon equation $KG(g,m)$ on $\Sigma$, then $\kappa^\ast \Phi$ is _not_ in general a solution to $KG(\kappa^\ast g,m)$.




+-- {: .num_prop}
###### Proposition

The general linear observable on the [[on-shell]] [[space of field histories]] of the [[free field theory|free]] [[real scalar field]] of [[mass]] $m \in \mathbb{R}_{\geq 0}$ is, under the identification ... the [[compactly supported distribution]]


$$
  \label{FourierModeExpansionOfScalarFieldOnminkowskiSpacetime}
  \mathbf{\Phi}(x)
  =
  \underset{\vec k \in \mathbb{R}^p}{\int}
      \left(
        a(\vec k) e^{- i \omega(\vec k) x^0 - 2 \pi i \vec k \cdot \vec x}
        +
        a(\vec k)^\ast e^{+ i \omega (\vec k) x^0 + 2 \pi i \vec k \cdot \vec x}
      \right)
    \frac{d^p \vec k}{
      (2\pi)^n \sqrt{ 2\omega(\vec k)/c }
    }
$$

which is the [[Fourier transform of distributions|Fourier transform]] of any 

=--

Under [[Fourier transform of distributions]] (def. \ref{EquationOfMotionOfFreeRealScalarField})
the [[Klein-Gordon equation]]

$$
  -\eta^{\mu \nu}\frac{\partial^2 }{\partial x^\mu \partial x^\nu} \Phi(x) + m^2 \Phi(x) \;=\; 0
  \phantom{AAAA}
  \text{for all} \, x \in \mathbb{R}^n
$$

becomes, using the relation (eq:FourierTransformInterchangesCoordinateProductWithDerivative) from example \ref{BasicPropertiesOfFourierTransformOverCartesianSpaces}):

$$
  2 \pi k_\mu 2 \pi k^\mu \widehat{\phi}(k) + m^2 \widehat{\Phi}(k) \;=\; 0
  \phantom{AAAA}
  \text{for all} \, k \in \mathbb{R}^n
  \,.
$$

The general solution of this equation are the multiples of the [[delta distribution]] (def. \ref{DiracDeltaDistribution})
applied to the "[[mass shell]]" $2 \pi k_\mu 2\pi k^\mu + m^2$:

$$
  \widehat{\Phi}(k)
    \;=\;
  A(k)\,
  \delta\left(
    2 \pi k_\mu 2 \pi k^\mu + m^2
  \right)
  \,.
$$

Hence by the [[Fourier inversion theorem]] (prop. \ref{FourierInversionTheoremForDistributions}),
the general solution of the original [[Klein-Gordon equation]] is a [[superposition]] of [[plane waves]] of the form

$$
  \Phi(x)
    \;=\;
  \int  A(k) e^{- 2\pi i k_\mu x^\mu }
  \delta\left( 2 \pi k_\mu 2 \pi k^\mu + m^2 \right)
  d^{p+1} k
  \,,
$$

where $a(k) \in \mathbb{C}$ is the _complex [[amplitude]]_ of the _mode_ with _[[wave vector]]_ $k \in \mathbb{R}^{p+1}$.

We may split this into the contributions with positive and those with negative _[[frequency]]_

$$
  \nu \coloneqq k_0
$$

by decomposing the integral over $k_0$ as

$$
  \begin{aligned}
    \Phi(x)
    & = \phantom{+}
    \int_0^\infty
    \left(
    \int A(k_0, \vec k) e^{- 2 \pi i k_0 x^0 - 2 \pi i \vec k \cdot \vec x}
      \,
      \delta\left(
        - (2 \pi k_0)^2 +  (2 \pi \vec k)^2 + m^2
      \right) d^p \vec k
    \right)
    d k_0
    \\
    & \phantom{=} +
    \int_0^\infty
    \left(
      \int A(-k_0, \vec k) e^{+ 2 \pi i k_0 x^0 - 2\pi i \vec k \cdot \vec x}
      \,
      \delta\left(
        - (2 \pi k_0)^2 + (2 \pi \vec k)^2 + m^2
      \right) d^p \vec k
    \right) d k_0
    \,.
  \end{aligned}
$$

By [[changing integration variables]] via $k_0 = +\sqrt{ h }/2 \pi$ this yields

$$
  \begin{aligned}
    \Phi(x)
    & = \phantom{+}
    \int
    \int_0^\infty
      A(\sqrt{h}/2\pi, \vec k)
      e^{- i \sqrt{h} x^0 - 2 \pi i \vec k \cdot \vec x}
      \delta\left(
        - h + (2 \pi \vec k)^2 + m^2
      \right)
      \, \frac{d h}{4 \pi \sqrt{h}}
      \,d^p \vec k
    \\
    & \phantom{=} +
    \int
    \int_0^\infty
      A(- \sqrt{h}/2\pi, \vec k)
      e^{+ i \sqrt{h} x^0 - 2 \pi i \vec k \cdot \vec x}
      \delta\left( - h + (2 \pi \vec k)^2 + m^2 \right)
     \, \frac{d h}{4 \pi\sqrt{h}}
     \, d^p \vec k
    \\
    & = \phantom{+}
    \int A(\nu(\vec k),\vec k) e^{- i \omega(\vec k) x^0 - 2 \pi i \vec k \cdot \vec x} \frac{d^p \vec k}{ 4 \pi \omega(\vec k) }
    \\
    & \phantom{=} +
    \int A(-\nu(\vec k),\vec k) e^{+ i \omega(\vec k) x^0 - 2 \pi i \vec k \cdot \vec x} \frac{d^p \vec k}{ 4 \pi \omega(\vec k) }
   \,,
  \end{aligned}
$$

where in the last line we defined the _on-shell [[positive number|positive]] [[angular frequency]]_

$$
  \omega (\vec k) \coloneqq + \sqrt{ (2 \pi \vec k)^2 + m^2 }
  \;\in \;
  \mathbb{R}_{\geq 0}
$$

It is convenient to also change variables $\vec k \mapsto - \vec k$ in the second integral. This yields

$$
  \begin{aligned}
    \Phi(x)
    & = \phantom{+}
    \int A(\nu(\vec k),\vec k) e^{- i \omega(\vec k) x^0 - 2 \pi i \vec k \cdot \vec x} \frac{d^p \vec k}{ 4 \pi \omega(\vec k) }
    \\
    & \phantom{=} + (-1)^p
    \int A(-\nu(\vec k),-\vec k) e^{+ i \omega(\vec k) x^0 + 2 \pi i \vec k \cdot \vec x} \frac{d^p \vec k}{ 4 \pi \omega(\vec k) }
   \,,
  \end{aligned}
$$

Since $\Phi$ is real-valued, it follows that under [[complex conjugation]] $(-)^\ast$ the amplitudes are related by

$$
  A(\nu(\vec k), \vec k)^\ast = (-1)^p A(-\omega(\vec k),-\vec k)
  \,.
$$

With this the general solution to the Klein-Gordon equation is finally of the form

$$
  \label{FourierModeExpansionOfScalarFieldOnminkowskiSpacetime}
  \Phi(x)
  =
    \int \frac{1}{\sqrt{ 2 \omega(\vec k)}}
      \left(
        a(\vec k) e^{- i \omega(\vec k) x^0 - 2 \pi i \vec k \cdot \vec x}
        +
        a(\vec k)^\ast e^{+ i \omega (\vec k) x^0 + 2 \pi i \vec k \cdot \vec x}
      \right)
    d^p \vec k
    \,.
$$

=--

and hence its time derivative is

$$
  \partial_0 \Phi(x)
  =
    \int -i \sqrt{\omega(\vec k)/2}
      \left(
        a(\vec k) e^{- i \omega (\vec k) x^0 - 2 \pi i \vec k \cdot \vec x}
        -
        a(\vec k)^\ast e^{+ i \omega(\vec k) x^0 + 2 \pi i \vec k \cdot \vec x}
      \right)
    d^p \vec k
    \,.
$$

This allows to express the field mode amplitudes in terms of the value of the field and its time derivative at $t = 0$:

$$
  a(\vec k)
  \;=\;
   \tfrac{1}{2}
   \int
     \left( \sqrt{\omega(\vec k)} \Phi(0,\vec x)
     + i \frac{1}{\sqrt{ \omega \vec k}} \partial_0 \Phi(0,\vec x)\right) \exp( i \vec k \cdot \vec x )
   d^p \vec x
   \,.
$$

Write

$$
  \mathbf{a}(\vec k) \;\colon\; C^\infty(\Sigma) \longrightarrow \mathbb{C}
$$

for the corresponding evaluation observable (example \ref{PointEvaluationObservables})

$$
  \mathbf{a}(\vec k)
   \;\colon\;
   \Phi
   \;\mapsto\;
   \tfrac{1}{2}
   \int
     \left( \sqrt{\omega(\vec k)}  \mathbf{\Phi}(\vec x) + i \frac{1}{\sqrt{ \omega(\vec k)}} \partial_0 \mathbf{\Phi}(\vec x)\right) \exp( i \vec k \cdot \vec x )
   d^p \vec x
   \,.
$$

With the Poisson bracket kernel $\{\phi(\vec x), \partial_0 \phi(\vec y)\} = \delta(\vec x - \vec y)$ (eq:PoissonBracketOfScalarFieldPointEvaluationOnMinkowskiSpacetime),
it follow that the  (integral kernel for the) Poisson bracket of these mode observables is
that of the [[canonical commutation relations]]:

$$
  \begin{aligned}
    \label{CanonicalPoissonCommutationOfModesOfFreeScalarFieldOnMinkowskiSpacetime}
    \left\{
      \mathbf{a}(\vec k_1), \mathbf{a}(\vec k_2)^\ast
    \right\}
    & =
    -i
    \int \delta(\vec x_1 - \vec x_2) e^{2 \pi i  ( \vec k_1 \cdot \vec x_1 - \vec k_2 \cdot \vec x_2) } d \vec x_1 d\vec x_2
    \\
    & =
    -i
    \int e^{2 \pi i (\vec k_1 - \vec k_2) \cdot \vec x } d \vec x
    & =
    \\
    & =  -i \delta(\vec k_1 - \vec k_2)
    \,,
  \end{aligned}
$$

where in the last step we used the [[Fourier transform]] representation of the [[delta distribution]] ([this prop.](Dirac+distribution#FourierTransform)).

In order to finally compute $\{\mathbf{\Phi}(x), \mathbf{\Phi}(y)\}$, it is convenient to break this up into two contributions:
Write

$$
  \mathbf{\Phi}^{(+)}(x)
  \;\coloneqq\;
    \int \frac{1}{\sqrt{2 \omega(\vec k)}}
        \mathbf{a}(\vec k)^\ast e^{+ i \omega(\vec k) x^0 + i \vec k \cdot \vec x}
    d^p \vec k
  \phantom{AAAA}
  \mathbf{\Phi}^{(-)}(x)
  \;\coloneqq\;
    \int \frac{1}{\sqrt{2 \omega(\vec k)}}
        \mathbf{a}(\vec k) e^{- i \omega(\vec k) x^0 - i \vec k \cdot \vec x}
    d^p \vec k
$$

for the positive and negative energy contributions from the Fourier expansion in (eq:FourierModeExpansionOfScalarFieldOnminkowskiSpacetime), so that

$$
  \mathbf{\Phi}(x)
    \;=\;
  \mathbf{\Phi}^{(-)}(x)  + \mathbf{\Phi}^{(+)}(x)
  \,.
$$

Using the [[canonical commutation relation]] of the mode functions (eq:CanonicalPoissonCommutationOfModesOfFreeScalarFieldOnMinkowskiSpacetime), we find

$$
  \label{2PointFunctionFreeScalarFieldOnMinkowski}
  \begin{aligned}
    -i \omega(x,y)
     & \coloneqq
     \left\{ \mathbf{\phi}^{(-)}(x), \mathbf{\phi}^{(+)}(y) \right\}
    \\
    &=
    -i
   \int \tfrac{1}{2 \omega(\vec k)} e^{- i \omega(\vec k) (x-y)^0 - \vec k \cdot (\vec x - \vec y)} d^{p} \vec k
    \\
    & =
    -i
    \int \delta\left( 2\pi k_\mu 2 \pi k^\mu + m^2 \right) \Theta( k_0 ) e^{ - i k_\mu (x-y)^\mu } d^{p+1} k
    \,,
  \end{aligned}
$$

where in the last line we again applied [[change of integration variables]].
This $\omega$ is known as the _[[2-point function]]_ or _[[Hadamard propagator]]_ on Minkowski spacetime.
Similarly

$$
  \begin{aligned}
  \left\{ \mathbf{\Phi}^{(+)}(x), \mathbf{\Phi}^{(-)}(y) \right\}
  & =
  + i
  \int \tfrac{1}{2 \omega(\vec k)} e^{i \omega(\vec k) (x-y)^0 + 2\pi i\vec k \cdot (\vec x - \vec y)} d^{p} \vec k
  \\
  & =
  + i
  \int \delta\left( 2\pi k_\mu 2\pi k^\mu + m^2 \right) \Theta( -k_0 ) e^{ - i 2\pi i k_\mu (x-y)^\mu } d^{p+1} k
  \\
  \end{aligned}
  \,.
$$

With this we finally obtain the expression for the [[causal propagator]] as the skew-symmetrization
of the [[2-point function]]:

$$
  \begin{aligned}
  \{
    \mathbf{\Phi}(x),
    \mathbf{\Phi}(y)
  \}
  & =
  \{ \mathbf{\Phi}^{(-)}(x), \mathbf{\Phi}^{(+)}(y) \}
  +
  \{\mathbf{\Phi}^{(+)}(x), \mathbf{\Phi}^{(-)}(y)\}
  \\
  & =
  -i \left(
    \omega(x,y) - \omega(y,x)
  \right)
  \\
  & =
  -i
  \int \tfrac{1}{2 E(\vec k)}\left(
    e^{- i \omega(\vec k) (x-y)^0 - 2\pi i\vec k \cdot (\vec x - \vec y)}
    -
    e^{+ i \omega(\vec k) (x-y)^0 + 2\pi i\vec k \cdot (\vec x - \vec y)}
  \right) d^p \vec k
  \\
  & =
  -i
  \int \delta\left( 2\pi k_\mu 2\pi k^\mu + m^2 \right) sgn( k_0 ) e^{ - 2\pi i k_\mu (x-y)^\mu } d^{p+1} k
 \,.
  \end{aligned}
$$
