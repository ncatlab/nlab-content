$x {\color{red}\le} y$



+-- {: .num_prop }
###### Proposition

Consider

1. $\Sigma$ a [[spacetime]] of [[dimension]] $p+1$, hence a [[Lorentzian manifold]] equipped with [[time orientation]];

1. $E \overset{fb}{\to} \Sigma$ a [[smooth vector bundle]]; 

   write $\tide E^\ast \coloneqq E^\ast \otimes_{\Sigma} \wedge^{p+1} T^\ast \Sigma$ for its [[density|densitized]] [[dual vector bundle]];

1. $P \colon \Gamma_\Sigma(E)\longrightarrow \Gamma_\Sigma(\tilde E^\ast)$ a [[Green hyperbolic differential operator]], hence a [[hyperbolic differential operator]] with unique [[advanced and retarded Green functions]]

   $G_\pm \;\colon\; \Gamma_{\pm}(\tilde E^\ast) \longrightarrow \Gamma_{\pm}(E)$.




=--


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






