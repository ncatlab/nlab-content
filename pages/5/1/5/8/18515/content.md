
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Vacua
+-- {: .hide}
[[!include vacua -- contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea


In [[perturbative quantum field theory]] [[AQFT on curved spacetimes|on curved spacetimes]], _Hadamard states_ are certain [[quantum states]] of [[free fields]] (whose [[2-point function]] is the corresponding _Hadamard distribution_ on [[spacetime]]) that play the role that the _[[vacuum state]]_ plays on [[Minkowski spacetime]].

Here a _[[vacuum state]]_ is supposed to be a [[quantum state]] that expresses the absence of any [[particle]] excitations of the fields.
On [[Minkowski spacetime]] the _vacuum state_ for a [[free field theory]] is the standard Hadamard state (def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime} below). On general [[globally hyperbolic spacetimes]] there are always Hadamard states ([Radzikowski 96](#Radzikowski96), see def. \ref{HadamardDistribution} below),  and they do play the role of the vacuum state in  the construction of [[AQFT on curved spacetimes]], see at _[[locally covariant perturbative AQFT]]_. Notably the choice of such a Hadamard state fixes the _[[Feynman propagator]]_, hence the [[time-ordered product]] of [[quantum observables]] and thus the [[perturbative quantum field theory|perturbative]] [[S-matrix]] away from coinciding interaction points (the [[extension of distributions|extension of these distributions]] to coinciding interaction points is the process of [[renormalization]]).

However, since on a general [[globally hyperbolic spacetime]] there is no globally well-defined concept of [[particles]], there is in general no concept of vacuum state. But under good conditions (such as existence of suitable [[timelike]] [[Killing vectors]]) one may identify Hadamard states which deserve to be thought of as vacuum states ([Brum-Fredenhagen 13](#BrumFredenhagen13)).


Hadamard states are mathematically characterized as follows:

Given a [[globally hyperbolic spacetime]], the [[causal propagator]] defines a [[symplectic form]] on the [[covariant phase space]] of the [[free field|free]] [[scalar field]]. However its [[wave front set]] is too large for the would-be induced [[Moyal star product]] to exist on but a very small subalgebra of smooth functionals, due to the failure of the relevant [[products of distributions]] to exist. However the Moyal star product makes sense more generally for [[almost Kähler structures]] with a symmetric contribution added to the skew-symmetric symplectic form.

A _Hadamard distribution_ is such a modification of the [[causal propagator]] by a symmetric component such that the resulting [[wave front set]] is just one causal half of that of the [[causal propagator]]. This is usually called a _Wightman propagator_. (Unfortunately the term "Hadamard propagator" is used for something else.)

This allows to define the corresponding [[Moyal star product]] on the larger algebra of [[microcausal functionals]] which is large enough to contain the [[adiabatic switching|adiabatically switched]] point [[interaction]] terms $g \phi(x)^n$ (as in [[phi^4 theory]] etc.). The resulting [[algebra of observables]] is the _[[Wick algebra]]_ of the free scalar field.

The Hadamard distribution may also be thought of as the [[2-point function]] of a [[quasi-free quantum state]]. These states are therefore called _Hadamard states_.

[[!include propagators - table]]


## Definition

Recall the following general facts about the [[wave equation]]/[[Klein-Gordon equation]]

+-- {: .num_prop #PropertiesOfTheCausalPropagator}
###### Proposition
**(the [[causal propagator]])**

Let $(X,g)$ be a [[time orientation|time-oriented]] [[globally hyperbolic spacetime]] and let $m \in \mathbb{R}_{\geq 0}$ (the "[[mass]]"). Then the [[Klein-Gordon equation]]

$$
  (\Box_g - m^2) \phi = 0
$$

(a [[partial differential equation]] on [[smooth functions]] $f \in C^\infty(X,\mathbb{R})$ ) has unique advanced and retarded [[Green functions]] $E^{R/A}$, namely [[continuous linear functionals]]

$$
  E^{A/R}
   \;\colon\;
  C^\infty_c(X)
   \longrightarrow
  C^\infty(X)
$$

(from [[bump functions]] to general [[smooth functions]]) which are [[fundamental solutions]] in that

$$
  (\Box_g - m^2) \circ E^{A/R} = \delta
  \phantom{AAAA}
  E^{A/R} \circ (\Box_g - m^2) = \delta
$$

and which have advanced/retarded [[support of a distribution]] when viewed (via the [[Schwartz kernel theorem]]) as [[distributions]] on the [[Cartesian product]] manifold $X \times X$

$$
  supp( E^{A/R}) \subset \{ (x_1, x_2) \in X \times X  \;\vert\; x_1 \in J^{\mp} (x_2) \}
 \,.
$$

In fact these two fundamental solutions are related by switching their arguments

$$
  E^{A/R}(x_1, x_2) = E^{R/A}(x_2, x_1)
  \,.
$$

Finally their [[wave front set]] is

$$
  WF(E^{A/R})
  \;=\;
  \left\{
   ((x_1, x_2), (k_1, -k_2))
   \;\vert\;
   x_1 \in J^{\mp}(x_2)
   \;\text{and}\;
   \left(
     (x_1, k_1) \sim (x_2, k_2)
   \right)
   \;\text{or}\;
   \left(
     (x_1 = x_2)
     \,\text{and}\,
     k_1 = -k_2
   \right)
  \right\}
  \,.
$$

Here the [[relation]] $(x_1, k_1) \sim (x_2, k_2)$ means that there exists a [[lightlike]] [[geodesic]] from $x_1$ to $x_2$ with cotangent vector $k_1$ at $x_1$ and $k_2$ at $x_2$.

It follows that the [[wave front set]] of their difference (the [[causal propagator]])

$$
  E \;\coloneqq\; E^A - E^R
$$

is

$$
  WF(E)
  \;=\;
  \left\{
    ((x_1 x_2), (k_1, -k_2))
    \;\vert\;
    (x_1, k_1) \sim (x_2, k_2)
  \right\}
  \,.
$$


=--

+-- {: .num_defn #HadamardDistribution}
###### Definition
**(Hadamard distribution)

Let $(X,g)$ be a [[time orientation|time oriented]] [[globally hyperbolic spacetime]].

A _Hadamard 2-point function_ or _Hadamard distribution_ for the [[free field|free]] [[scalar field]] on $(X,g)$ is a [[distribution of two variables]]

$$
  \omega \in \mathcal{D}'(X \times X)
$$

on the [[Cartesian product]] manifold such that


1. the anti-symmetric part of $\omega$ is the [[causal propagator]] $E$ (from prop. \ref{PropertiesOfTheCausalPropagator})

   $$
     \omega(x_1, x_2) - \omega(x_2, x_1)
     \;=\;
     i E(x_1, x_2)
   $$

1. (wave front set spectral condition ([Radzikowski 96, def. 6.1](#Radzikowski96)))

   the [[wave front set]] is one causal half that of the causal propagator:

   $$
     WF(\omega)
     \;=\;
     \left\{
       ((x_1, x_2), (k_1, -k_2))
       \;\vert\;
       (x_1, k_1) \simeq (x_2, k_2)
       \;\;\text{and}\;\;
       k_1 \in V_{x_1}^+
     \right\}
   $$



1. (Klein-Gordon bi-solution) $(\Box_g - m^2) \omega(-,x) = 0$ and $(\Box_g - m^2)\omega(x,-) = 0$, for all $x \in X$;


1. {#PositiveSemiDefiniteness} (positive semi-definiteness) For any complex-valued [[bump function]] $b$ we have that

   $$
     \int_{X \times X} b^\ast(x) \omega(x,y) b(y) \, dvol(x) dvol(y)
     \;\coloneqq\;
     \langle \omega, b^\ast \otimes b \rangle
     \;\geq\; 0
   $$

=--

+-- {: .num_remark}
###### Remark

Before ([Radzikowski 96](#Radzikowski96)), Hadamard distributions were characterized by their singularity structure (see ... below). In ([Kay-Wald 91](#KayWald91)) the spectrum condition in def. \ref{HadamardDistribution} was formulated, and ([Radzikowski 96](#Radzikowski96)) proved that this is equivalent to the original definition via singularity structure.

=--


## Properties

### Existence

+-- {: .num_prop #ExistenceOfHadamardDistributions}
###### Proposition
**(existence of Hadamard distributions)

Let $(X,g)$ be a [[globally hyperbolic spacetime]]. Then a [[Hadamard distribution]] $\omega$ according to def. \ref{HadamardDistribution} does exist.

It is given, up to addition by a smooth function, as the difference between the [[advanced propagator]] and the [[Feynman propagator]]

=--

([Radzikowski 96, above theorem 6.3 with theorem 5.1](#Radzikowski96))

In fact there exist infinitely many Hadamard distributions on any globally hyperbolic spacetime ([Junker-Schrohe 02](#JunkerSchrohe02), [Fulling-Narcowich-Wald 81](#FullingNarcowichWald81)).

## Examples

### For Klein-Gordon operator on Minkowski spacetime
{#ForKleinGordonOperatorOnMinkowskiSpacetime}

On [[Minkowski spacetime]] $\mathbb{R}^{p,1}$ consider the [[Klein-Gordon operator]]

$$
\eta^{\mu \nu} \frac{\partial}{\partial x^\mu} \frac{\partial}{\partial x^\nu} \Phi -  \left( \tfrac{m c}{\hbar} \right)^2 \Phi \;=\; 0 \,.
$$

Its [[Fourier transform]] is

$$
- k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2
\;=\;
(k_0)^2 - {\vert \vec k\vert}^2 - \left( \tfrac{m c}{\hbar} \right)^2
\,.
$$

The [[dispersion relation]] of this equation we write

$$
\label{DispersionRelationForKleinGordonooeratorObMinkowskiSpacetime}
\omega(\vec k)
\;\coloneqq\;
+ c \sqrt{ {\vert \vec k \vert}^2 + \left( \tfrac{m c}{\hbar}\right)^2 }
\,,
$$

where on the right we choose the [[non-negative real number|non-negative]] [[square root]].


$\,$

We now discuss

1. _[Advanced and regarded propagators](#AdvancedAndRetardedPropagatorsForKleinGordonEquationOnMinkowskiSpacetime)_

1. _[Causal propagator](#CausalPropagatorForKleinGordonEquationOnMinkowskiSpacetime)_

1. _[Wightman propagator](#HadamardPropagatorForKleinGordonOnMinkowskiSpacetime)_

1. _[Wave front sets](#WaveFrontSetsOfPropagatorsForKleinGordonOperatorOnMinkowskiSpacetime)_

$\,$



**[[advanced and retarded propagators]] for [[Klein-Gordon equation]] on [[Minkowski spacetime]]**
{#AdvancedAndRetardedPropagatorsForKleinGordonEquationOnMinkowskiSpacetime}

+-- {: .num_prop #AdvancedRetardedPropafatorsForKleinGordonOnMinkowskiSpacetime}
###### Proposition
**(mode expansion of [[advanced and retarded propagators]] for [[Klein-Gordon operator]] on [[Minkowski spacetime]])**

The [[advanced and retarded Green functions]] $G_\pm$ of the [[Klein-Gordon operator]] on [[Minkowski spacetime]] are given by [[integral kernels]] ("[[propagators]]")

$$
\Delta_\pm \in \mathcal{D}'(\mathbb{R}^{p,1}\times \mathbb{R}^{p,1})
$$

by (in [[generalized function]]-notation)

$$
G_\pm(\Phi)
\;=\;
\underset{\mathbb{R}^{p,1}}{\int}
\Delta_{\pm}(x,y) \Phi(y) \, dvol(y)
$$

where the [[advanced and retarded propagators]] $\Delta_{\pm}(x,y)$ have the following equivalent expressions:

$$
\label{ModeExpansionForMinkowskiAdvancedRetardedPropagator}
\begin{aligned}
\Delta_\pm(x-y)
& =
\frac{1}{(2\pi)^{p+1}}
\underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
\int \int
\frac{
e^{i k_0 (x^0 - y^0)} e^{i \vec k \cdot (\vec x - \vec y)}
}{
(k_0 \mp i\epsilon)^2 - {\vert \vec k\vert}^2  -\left( \tfrac{m c}{\hbar}\right)^2
}
\, d k_0 \, d^p \vec k
\\
& =
\left\{
\array{
\frac{\pm i}{(2\pi)^{p}}
\int
\frac{1}{2\omega(\vec k)/c}
\left(
e^{+i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
-
e^{-i \omega(\vec k)(x^0 - y^0)/c  + i \vec k \cdot (\vec x - \vec  y) }
\right)
d^p \vec k
& \vert & \text{if} \,  \pm (x^0 - y^0) \gt 0
\\
0 & \vert & \text{otherwise}
}
\right.
\end{aligned}
$$

Here $\omega(\vec k)$ denotes the [[dispersion relation]] (eq:DispersionRelationForKleinGordonooeratorObMinkowskiSpacetime) of the [[Klein-Gordon equation]].

=--

+-- {: .proof}
###### Proof

The [[Klein-Gordon operator]] is a [[Green hyperbolic differential operator]] ([this example](Green+hyperbolic+partial+differential+equation#GreenHyperbolicKleinGordonOperator)) therefore its advanced and retarded Green functions exist uniquely (prop. \ref{AdvancedAndRetardedGreenFunctionsForGreenHyperbolicOperatorAreUnique}).
Moreover,  prop. \ref{GreenFunctionsAreContinuous} says that they are [[continuous linear functionals]] with respect to the [[topological vector space]] [[structures]] on [[spaces of smooth sections]] (def. \ref{TVSStructureOnSpacesOfSmoothSections}). In the case of the [[Klein-Gordon operator]] this just means that

$$
G_{\pm}
\;\colon\;
C^\infty_{cp}(\mathbb{R}^{p,1})
\longrightarrow
C^\infty_{\pm cp}(\mathbb{R}^{p,1})
$$

are [[continuous linear functionals]] in the standard sense of [[distributions]]. Therefore the
[[Schwartz kernel theorem]]  implies the existence of [[integral kernels]] being [[distributions in two variables]]

$$
\Delta_{\pm} \in \mathcal{D}(\mathbb{R}^{p,1} \times \mathbb{R}^{p,1})
$$

such that, in the notation of [[generalized functions]],

$$
(G_\pm \alpha)(x)
\;=\;
\underset{\mathbb{R}^{p,1}}{\int} \Delta_{\pm}(x,y) \alpha(y) \, dvol(y)
\,.
$$

These integral kernels are the advanced/retarded "[[propagators]]". We now compute
these [[integral kernels]] by making an Ansatz and showing that it has the defining properties,
which identifies them by the uniqueness statement of prop. \ref{AdvancedAndRetardedGreenFunctionsForGreenHyperbolicOperatorAreUnique}.

We make use of the fact that the [[Klein-Gordon equation]] is [[invariant]] under the defnining [[action]]
of the [[Poincaré group]] on [[Minkowski spacetime]], which is a [[semidirect product group]] of the [[translation group]]
and the [[Lorentz group]].

Since the [[Klein-Gordon operator]] is invariant, in particular, under [[translations]] in $\mathbb{R}^{p,1}$ it is clear that the propagators, as a [[distribution in two variables]], depend only on the difference of its two arguments

$$
\Delta_{\pm}(x,y) = \Delta_{\pm}(x-y)
\,.
$$

Since moreover the [[Klein-Gordon operator]] is [[formally adjoint differential operator|formally self-adjoint]] ([this prop.](Klein-Gordon+equation#FormallySelfAdjointKleinGordonOperator)) this implies that for $P$ the Klein the equation (eq:AdvancedRetardedGreenFunctionIsRightInverseToDiffOperator)

$$
P \circ G_\pm  = id
$$

is equivalent to the equation (eq:AdvancedRetardedGreenFunctionIsLeftInverseToDiffOperator)

$$
G_\pm \circ P = id
\,.
$$

Therefore it is sufficient to solve for the first of these two equation, subject to
the defining support conditions. In terms of the [[propagator]] [[integral kernels]] this means that we have to solve the [[distribution|distributional]] equation

$$
\label{KleinGordonEquationOnAdvacedRetardedPropagator}
\left(
\eta^{\mu \nu}
\frac{\partial}{\partial x^\mu}
\frac{\partial}{\partial x^\nu}
-
\left( \tfrac{m c}{\hbar} \right)^2
\right)
\Delta_\pm(x-y)
\;=\;
\delta(x-y)
$$

subject to the condition that the [[support of a distribution|distributional support]] is

$$
supp\left( \Delta_{\pm}(x-y) \right)
\subset
\left\{
{\vert x-y\vert^2_\eta}\lt 0
\;\,,\;
\pm(x^0 - y^ 0) \gt 0
\right\}
\,.
$$


We make the _Ansatz_ that we assume that $\Delta_{\pm}$, as a distribution in a single variable $x-y$, is a [[tempered distribution]]

$$
\Delta_\pm \in \mathcal{S}'(\mathbb{R}^{p,1})
\,,
$$

hence amenable to [[Fourier transform of distributions]]. If we do find a solution this way, it is guaranteed to be the unique solution by prop. \ref{AdvancedAndRetardedGreenFunctionsForGreenHyperbolicOperatorAreUnique}.

By [this prop.](Fourier+transform#BasicPropertiesOfFourierTransformOverCartesianSpaces)
the [[Fourier transform of distributions|distributional Fourier transform]] of equation (eq:KleinGordonEquationOnAdvacedRetardedPropagator) is

$$
\begin{aligned}
\label{FourierVersionOfPDEForKleinGordonAdvancedRetardedPropagator}
\left(
- \eta^{\mu \nu} k_\mu k_\nu - \left( \tfrac{m c}{\hbar} \right)^2
\right)
\widehat{\Delta_{\pm}}(k)
& =
\widehat{\delta}(k)
\\
& =
1
\end{aligned}
\,,
$$

where in the second line we used the [[Fourier transform of distributions|Fourier transform]] of the [[delta distribution]]
from [this example](Dirac+distribution#FourierTransformOfDeltaDistribution).

Notice that this implies that the [[Fourier transform]] of the [[causal propagator]]

$$
  \Delta_S \coloneqq \Delta_+ - \Delta_-
$$

satisfies the homogeneous equation:

$$
\label{FourierVersionOfPDEForKleinGordonCausalPropagator}
\left(
- \eta^{\mu \nu} k_\mu k_\nu - \left( \tfrac{m c}{\hbar} \right)^2
\right)
\widehat{\Delta_S}(k)
\;=\;
0
\,,
$$


Hence we are now reduced to finding solutions $\widehat{\Delta_\pm} \in \mathcal{S}'(\mathbb{R}^{p,1})$ to (eq:FourierVersionOfPDEForKleinGordonAdvancedRetardedPropagator) such that their [[Fourier inversion theorem|Fourier inverse]] $\Delta_\pm$ has the required [[support of a distribution|support]] properties.

We discuss this by a variant of the [[Cauchy principal value]]:

Suppose the following [[limit of a sequence|limit]] of [[non-singular distributions]] in the [[variable]] $k \in \mathbb{R}^{p,1}$
exists in the space of [[distributions]]

$$
\label{LimitOverImaginaryOffsetForFourierTransformedAdvancedRetardedPropagator}
\underset{ {\epsilon \in (0,\infty)} \atop { \epsilon \to 0 } }{\lim}
\frac{1}{ (k_0 \mp i \epsilon)^2  - {\vert \vec k\vert^2} - \left( \tfrac{m c}{\hbar} \right)^2 }
\;\in\;
\mathcal{D}'(\mathbb{R}^{p,1})
$$

meaning that for each [[bump function]] $b \in C^\infty_{cp}(\mathbb{R}^{p,1})$ the [[limit of a sequence|limit]] in $\mathbb{C}$

$$
\underset{ {\epsilon \in (0,\infty)} \atop { \epsilon \to 0 }   }{\lim}
\underset{\mathbb{R}^{p,1}}{\int} \frac{b(k)}{ (k_0\mp i \epsilon)^2 - {\vert \vec k\vert}^2 - \left( \tfrac{m c}{\hbar} \right)^2  }
d^{p+1}k
\;\in\;
\mathbb{C}
$$

exists. Then this limit is clearly a solution to the distributional equation (eq:FourierVersionOfPDEForKleinGordonAdvancedRetardedPropagator)
because on those bump functions $b(k)$ which happen to be products with $\left(-\eta^{\mu \nu}k_\mu k^\nu - \left( \tfrac{m c}{\hbar}\right)^2\right)$
we clearly have

$$
\begin{aligned}
\underset{ {\epsilon \in (0,\infty)} \atop { \epsilon \to 0 }   }{\lim}
\underset{\mathbb{R}^{p,1}}{\int}
\frac{
\left( -\eta^{\mu \nu} k_\mu k_\nu - \left( \tfrac{m c}{\hbar} \right)^2 \right) b(k)
}{
(k_0\mp i \epsilon)^2 - {\vert \vec k\vert}^2 - \left( \tfrac{m c}{\hbar} \right)^2
}
d^{p+1}k
& =
\underset{\mathbb{R}^{p,1}}{\int}
\underset{= 1}{
\underbrace{
\underset{ {\epsilon \in (0,\infty)} \atop { \epsilon \to 0 }   }{\lim}
\frac{
\left( -\eta^{\mu \nu} k_\mu k_\nu - \left( \tfrac{m c}{\hbar} \right)^2 \right) }{
(k_0\mp i \epsilon)^2 - {\vert \vec k\vert}^2 - \left( \tfrac{m c}{\hbar} \right)^2  }
}
}
b(k)\, d^{p+1}k
\\
& =
\langle 1, b\rangle
\,.
\end{aligned}
$$

Moreover, if the limiting distribution (eq:LimitOverImaginaryOffsetForFourierTransformedAdvancedRetardedPropagator)
exists, then it is clearly a [[tempered distribution]], hence we may apply [[Fourier inversion theorem|Fourier inversion]]
to  obtain [[Green functions]]

$$
\label{AdvancedRetardedPropagatorViaFourierTransformOfLLimitOverImaginaryOffsets}
\Delta_{\pm}(x,y)
\;\coloneqq\;
\underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
\frac{1}{(2\pi)^{p+1}}
\underset{\mathbb{R}^{p,1}}{\int}
\frac{e^{i k_\mu (x-y)^\mu}}{
(k_0 \mp i \epsilon  )^2 - {\vert \vec k\vert}^2  - \left(\tfrac{m c}{\hbar}\right)^2
}
d k_0 d^p \vec k
\,.
$$

To see that this is the correct answer, we need to check the defining support property.

Finally, by the [[Fourier inversion theorem]], to show that the [[limit of a sequence|limit]] (eq:LimitOverImaginaryOffsetForFourierTransformedAdvancedRetardedPropagator) indeed exists it is sufficient to show that the
limit in (eq:AdvancedRetardedPropagatorViaFourierTransformOfLLimitOverImaginaryOffsets) exists.

We compute as follows

$$
\label{TheSupportOfTheCandidateAdvancedRetardedPropagatorIsinTheFutureOrPastRespectively}
\begin{aligned}
\Delta_\pm(x-y)
& =
\frac{1}{(2\pi)^{p+1}}
\underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
\int \int
\frac{
e^{i k_0 (x^0 - y^0)} e^{i \vec k \cdot (\vec x - \vec y)}
}{
(k_0 \mp i\epsilon)^2 - {\vert \vec k\vert}^2  -\left( \tfrac{m c}{\hbar}\right)^2
}
\, d k_0 \, d^p \vec k
\\
& =
\frac{1}{(2\pi)^{p+1}}
\underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
\int \int
\frac{
e^{i k_0 (x^0 - y^0)} e^{i \vec k \cdot (\vec x - \vec y)}
}{
(k_0 \mp i \epsilon)^2 - \left(\omega(\vec k)/c\right)^2
}
\, d k_0 \, d^p \vec k
\\
&=
\frac{1}{(2\pi)^{p+1}}
\underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
\int \int
\frac{
e^{i k_0 (x^0 - y^0)} e^{i \vec k \cdot (\vec x - \vec y)}
}{
\left(
(k_0 \mp i\epsilon) - \omega(\vec  k)/c
\right)
\left(
(k_0 \mp i \epsilon) + \omega(\vec k)/c
\right)
}
\, d k_0 \, d^p \vec k
\\
& =
\left\{
\array{
\frac{\pm i}{(2\pi)^{p}}
\int
\frac{1}{2\omega(\vec k)/c}
\left(
e^{i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
-
e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec  y)}
\right)
d^p \vec k
& \vert & \text{if} \,  \pm (x^0 - y^0) \gt 0
\\
0 & \vert & \text{otherwise}
}
\right.
\end{aligned}
$$

where $\omega(\vec k)$ denotes the [[dispersion relation]] (eq:DispersionRelationForKleinGordonooeratorObMinkowskiSpacetime) of the [[Klein-Gordon equation]].

Here the key step is the application of [[Cauchy's integral formula]] in the fourth step. We spell this out now for $\Delta_+$, the discussion for $\Delta_-$ is the same, just with the appropriate signs reversed.

1. If  $(x^0 - y^0) \gt 0$ thn the expression $e^{ik_0 (x^0 - y^0)}$ decays with _[[positive number|positive]] [[imaginary part]]_ of $k_0$, so that we may expand the [[integration]] [[domain]] into the [[upper half plane]] as

$$
\begin{aligned}
\int_{-\infty}^\infty d k_0
& = \phantom{+}
\int_{-\infty}^0 d k_0 + \int_{0}^{+ i \infty} d k_0
\\
& = + \int_{+i \infty}^0 d k_0  + \int_0^\infty d k_0
\,;
\end{aligned}
$$

Conversely, if $(x^0 - y^0) \lt 0$ then we may analogously expand into the [[lower half plane]].

1. This integration domain may then further be completed to two [[contour integrations]]. For the expansion into the [[upper half plane]] these encircle counter-clockwise the [[poles]] at $\pm \omega(\vec k)+ i\epsilon \in \mathbb{C}$, while for expansion into the [[lower half plane]] no poles are being encircled.

<img src="https://ncatlab.org/nlab/files/ContourForAdvancedPropagator.png" height="280">


1. Apply [[Cauchy's integral formula]] to find in the case $(x^0 - y^0)\gt 0$ the sum of the [[residues]] at these two [[poles]] times $2\pi i$, zero in the other case. (For the retarded propagator we get $- 2 \pi i$ times the residues, because now the contours encircling non-trivial poles go clockwise).

1. The result does not depend on $\epsilon$ anymore, therefore the [[limit of a sequence|limit]] $\epsilon \to 0$ is now computed trivially.

This computation shows a) that the limiting distribution indeed exists, and b) that the [[support of a distribution|support]]
of $\Delta_+$ is in the future, and that of $\Delta_-$ is in the past.

Hence it only remains to see now that the support of $\Delta_\pm$ is inside the [[causal cone]].
But this follows from the previous argument, by using that the [[Klein-Gordon equation]] is invariant under
[[Lorentz transformations]]: This implies that the support is in fact in the [[future]] of _every_ spacelike
slice through the origin in $\mathbb{R}^{p,1}$, hence in the [[closed future cone]] of the origin.


=--


+-- {: .num_cor #CausalPropagatorIsSkewSymmetric}
###### Corollary
**([[causal propagator]] is skew-symmetric)**

Under reversal of arguments the [[advanced and retarded causal propagators]] are related by

$$
\Delta_{\pm}(y-x) = \Delta_\mp(x-y)
\,.
$$

It follows that the [[causal propagator]] $\Delta \coloneqq \Delta_+ - \Delta_-$ is skew-symmetric in its arguments:

$$
\Delta_S(x-y) = - \Delta_S(y-x)
\,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{AdvancedRetardedPropafatorsForKleinGordonOnMinkowskiSpacetime} we have with (eq:ModeExpansionForMinkowskiAdvancedRetardedPropagator)


$$
\begin{aligned}
\Delta_\pm(y-x)
& =
\left\{
\array{
\frac{\pm i}{(2\pi)^{p}}
\int
\frac{1}{2\omega(\vec k)/c}
\left(
e^{-i \omega(\vec k)(x^0 - y^0)/c -  i \vec k \cdot (\vec x -\vec y)}
-
e^{+i \omega(\vec k)(x^0 - y^0)/c  - i \vec k \cdot (\vec x - \vec  y) }
\right)
d^p \vec k
& \vert & \text{if} \,  \mp (x^0 - y^0) \gt 0
\\
0 & \vert & \text{otherwise}
}
\right.
\\
& =
\left\{
\array{
\frac{\pm i}{(2\pi)^{p}}
\int
\frac{1}{2\omega(\vec k)/c}
\left(
e^{-i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
-
e^{+i \omega(\vec k)(x^0 - y^0)/c  - i \vec k \cdot (\vec x - \vec  y) }
\right)
d^p \vec k
& \vert & \text{if} \,  \mp (x^0 - y^0) \gt 0
\\
0 & \vert & \text{otherwise}
}
\right.
\\
& =
\left\{
\array{
\frac{\mp i}{(2\pi)^{p}}
\int
\frac{1}{2\omega(\vec k)/c}
\left(
e^{+i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
-
e^{-i \omega(\vec k)(x^0 - y^0)/c  - i \vec k \cdot (\vec x - \vec  y) }
\right)
d^p \vec k
& \vert & \text{if} \,  \mp (x^0 - y^0) \gt 0
\\
0 & \vert & \text{otherwise}
}
\right.
\\
& =
\Delta_\mp(x-y)
\end{aligned}
$$

Here in the second step we applied [[change of integration variables]] $\vec k \mapsto - \vec k$ (which introduces _no_ sign because in addition to $d \vec k \mapsto - d \vec k$ the integration domain reverses [[orientation]]).

=--

$\,$

**[[causal propagator]]**
{#CausalPropagatorForKleinGordonEquationOnMinkowskiSpacetime}

+-- {: .num_prop #ModeExpansionOfCausalPropagatorForKleinGordonOnMinkowski}
###### Proposition
**(mode expansion of [[causal propagator]] for [[Klein-Gordon equation]] on [[Minkowski spacetime]])**

The [[causal propagator]] (eq:CausalPropagator) for the [[Klein-Gordon equation]] for [[mass]] $m$ on [[Minkowski spacetime]] $\mathbb{R}^{p,1}$ is given, in [[generalized function]] notation, by


$$
\label{CausalPropagatorModeExpansionForKleinGordonOnMinkowskiSpacetime}
\begin{aligned}
\Delta_S(x,y)
& =
\frac{+ i}{(2\pi)^{p}}
\int
\frac{1}{2\omega(\vec k)/c}
\left(
e^{i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
-
e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec  y)}
\right)
d^p \vec k
\\
& =
\frac{-1}{(2\pi)^p}
\int
\frac{1}{\omega(\vec k)/c}
\sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
e^{i \vec k \cdot (\vec x -\vec y)}
d^p \vec k
\,,
\end{aligned}
$$

where in the second line we used [[Euler's formula]] $sin(\alpha)= \tfrac{1}{2i}\left( e^{i \alpha} - e^{-i \alpha} \right)$.

In particular this shows that the [[causal propagator]] is [[real part|real]], in that it is equal to its [[complex conjugation|complex conjugate]]

$$
  \label{CausalPropagatorForKleinGordonEquationOnMinkowskiSpacetimeIsReal}
  \left(\Delta_S(x,y)\right)^\ast = \Delta_S(x,y)
  \,.
$$

=--


+-- {: .proof}
###### Proof

By definition and using the expression from prop. \ref{AdvancedRetardedPropafatorsForKleinGordonOnMinkowskiSpacetime} for the [[advanced and retarded causal propagators]] we have

$$
\begin{aligned}
\Delta_S(x,y)
& \coloneqq
\Delta_+(x,y) - \Delta_-(x,y)
\\
& =
\left\{
\array{
\frac{+ i}{(2\pi)^{p}}
\int
\frac{1}{2\omega(\vec k)/c}
\left(
e^{i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
-
e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec  y)}
\right)
d^p \vec k
& \vert & \text{if} \,  + (x^0 - y^0) \gt 0
\\
\frac{(-1) (-1) i}{(2\pi)^{p}}
\int
\frac{1}{2\omega(\vec k)/c}
\left(
e^{i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
-
e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec  y)}
\right)
d^p \vec k
& \vert & \text{if} \,  - (x^0 - y^0) \gt 0
}
\right.
\\
& =
\frac{+ i}{(2\pi)^{p}}
\int
\frac{1}{2\omega(\vec k)/c}
\left(
e^{i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
-
e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec  y)}
\right)
d^p \vec k
\\
& =
\frac{-1}{(2\pi)^p}
\int
\frac{1}{\omega(\vec k)/c}
\sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
e^{i \vec k \cdot (\vec x -\vec y)}
d^p \vec k
\end{aligned}
$$

For the reality, notice from the last line that

$$
  \begin{aligned}
    \left(\Delta_S(x,y)\right)^\ast
    & =
    \frac{-1}{(2\pi)^p}
    \int
    \frac{1}{\omega(\vec k)/c}
    \sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
     e^{-i \vec k \cdot (\vec x -\vec y)}
    d^p \vec k
    \\
    & =
    \frac{-1}{(2\pi)^p}
    \int
    \frac{1}{\omega(\vec k)/c}
    \sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
     e^{+i \vec k \cdot (\vec x -\vec y)}
    d^p \vec k
    \\
    & =
    \Delta_S(x,y)
    \,,
   \end{aligned}
$$

where in the last step we used the [[change of integration variables]] $\vec k \mapsto - \vec k$
(whih introduces no sign, since on top of $d \vec k \mapsto - d \vec k$ the [[orientation]] of the integration [[domain]] changes).

=--

We consider a couple of equivalent expressions for the causal propagator:

+-- {: .num_prop #CausalPropagatorForKleinGordonOnMinkowskiAsContourIntegral}
###### Proposition
**([[causal propagator]] for [[Klein-Gordon operator]] on [[Minkowski spacetime]] as a [[contour integral]])**


The [[causal propagator]] for the [[Klein-Gordon equation]] at [[mass]] $m$ on [[Minkowski spacetime]] has the following equivalent expression, as a [[generalized function]], given as a [[contour integral]] along a curve $C(\vec k)$ going counter-clockwise around the two [[poles]] at $k_0 = \pm \omega(\vec k)/c$:


$$
\Delta_S(x,y)
\;=\;
(2\pi)^{-(p+1)}
\int
\underset{C(\vec k)}{\oint}
\frac{e^{i k_\mu (x-y)^\mu}}{ -k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2g  }
\,d k_0
\,d^{p} k
\,.
$$

=--


<img src="https://ncatlab.org/nlab/files/ContourForCausalPropagator.png" height="160">

> graphics grabbed from [Kocic 16](#Kocic16)


+-- {: .proof}
###### Proof


By [[Cauchy's integral formula]] we compute as follows:

$$
\begin{aligned}
(2\pi)^{-(p+1)}
\int
\underset{C(\vec k)}{\oint}
\frac{e^{i k_\mu (x^\mu - y^\mu)}}{ -k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 }
\,d k_0
\,d^{p} k
& =
(2\pi)^{-(p+1)}
\int
\underset{C(\vec k)}{\oint}
\frac{
e^{i k_0 x^0} e^{ i \vec k \cdot (\vec x - \vec y)}
}{
k_0^2 - \omega(\vec k)^2/c^2
}
\,d k_0
\,d^p \vec k
\\
& =
(2\pi)^{-(p+1)}
\int
\underset{C(\vec k)}{\oint}
\frac{
e^{i k_0 (x^0 - y^0)} e^{i \vec k \cdot (\vec x - \vec y)}
}{
( k_0 + \omega(\vec k)/c )
( k_0 - \omega(\vec k)/c )
}
\,d k_0
\,d^p \vec k
\\
& =
(2\pi)^{-(p+1)}
2\pi i
\int
\left(
\frac{
e^{i \omega(\vec k) (x^0 - y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
}
{
2 \omega(\vec k)/c
}
-
\frac{
e^{ - i \omega(\vec k) (x^0 - y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
}{
2 \omega(\vec k)/c
}
\right)
\,d^p \vec k
\\
& =
i
(2\pi)^{-p}
\int
\frac{1}{\omega(\vec k)/c}
sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
e^{i \vec k \cdot (\vec x - \vec y)}
\,d^p \vec k
\,.
\end{aligned}
$$

The last line is the expression for the causal propagator from prop. \ref{ModeExpansionOfCausalPropagatorForKleinGordonOnMinkowski}

=--



+-- {: .num_prop #CausalPropagatorAsFourierTransformOfDeltaDistributionOnTransformedKGOperator}
###### Proposition
**([[causal propagator]] as [[Fourier transform]] of [[delta distribution]]  on the [[Fourier transform|Fourier transformed]] [[Klein-Gordon operator]])**


The [[causal propagator]] for the [[Klein-Gordon equation]] at [[mass]] $m$ on [[Minkowski spacetime]] has the following equivalent expression, as a [[generalized function]]:


$$
\Delta_S(x,y)
\;=\;
i (2\pi)^{-p} \int \delta\left( k_\mu k^\mu + \left( \tfrac{m c}{\hbar}\right)^2 \right) sgn( k_0 ) e^{ i k_\mu (x-y)^\mu } d^{p+1} k
\,,
$$

where the [[integrand]] is the product of the [[sign function]] of $k_0$ with the [[delta distribution]] of the [[Fourier transform]] of the [[Klein-Gordon operator]] and a [[plane wave]] factor.

=--

+-- {: .proof}
###### Proof

By decomposing the integral over $k_0$ into its negative and its positive half, and applying the [[change of integration variables]] $k_0 = \pm\sqrt{h}$ we get

$$
\begin{aligned}
i (2\pi)^{-p} \int \delta\left( k_\mu k^\mu + \left( \tfrac{m c}{\hbar}\right)^2 \right) sgn( k_0 ) e^{ i k_\mu (x-y)^\mu } d^{p+1} k
& =
+ i (2\pi)^{-p} \int \int_0^\infty \delta\left( -k_0^2 + \vec k^2 + \left( \tfrac{m c}{\hbar}\right)^2 \right) e^{ i k_0 (x^0 - y^0) + i \vec k \cdot (\vec x - \vec y)}  d k_0 \, d^p \vec k
\\
& \phantom{=}
- i (2\pi)^{-p} \int \int_{-\infty}^0 \delta\left( -k_0^2 + \vec k^2 + \left(\tfrac{m c}{\hbar}\right)^2 \right)  e^{ i k_0 (x^0 - y^0)+ i \vec k \cdot (\vec x - \vec y) } d k_0 \, d^{p} \vec k
\\
& =
+i (2\pi)^{-p} \int \int_0^\infty \frac{1}{2 \sqrt{h}} \delta\left( -h + \omega(\vec k)^2/c^2  \right) e^{ + i \sqrt{h} (x^0 - y^0) + i \vec k \cdot \vec x } d h \, d^{p} \vec k
\\
& \phantom{=}
- i (2\pi)^{-p} \int \int_0^\infty  \frac{1}{2 \sqrt{h}} \delta\left( - h + \omega(\vec k)^2/c^2 \right) e^{ - i \sqrt{h} (x^0 - y^0) + i \vec k \cdot \vec x }  d h \, d^{p} \vec k
\\
& =
+i (2\pi)^{-p} \int \frac{1}{2 \omega(\vec k)/c} e^{ i \omega(\vec k) (x-y)^0/c + i \vec k \cdot \vec x}  d^{p} \vec k
\\
& \phantom{=}
- i (2\pi)^{-p} \int \frac{1}{2 \omega(\vec k)/c} e^{ - i \omega(\vec k) (x-y)^0/c + i \vec k \cdot \vec x }  d^{p} \vec k
\\
& = -(2 \pi)^{-p} \int \frac{1}{\omega(\vec k)/c}
sin\left( \omega(\vec k)(x-y)^0/c \right)
e^{i \vec k \cdot (\vec x - \vec y)}
\end{aligned}
$$

The last line is the expression for the causal propagator from prop. \ref{ModeExpansionOfCausalPropagatorForKleinGordonOnMinkowski}.


=--



+-- {: .num_prop #SingularSupportOfCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetimeIsTheLightCone}
###### Proposition
**([[singular support]] of the [[causal propagator]] of the [[Klein-Gordon equation]] on [[Minkowski spacetime]] is the [[light cone]])**

The [[singular support]] of the [[causal propagator]] for the [[Klein-Gordon equation]] on [[Minkowski spacetime]]
is the [[light cone]] of the origin:

$$
\Delta_S(x,y)
\;\propto\;
sgn(x^0 - y^0)
\delta\left(
-{\vert x-y\vert}^2_\eta
\right)
-
\Theta\left(
-{\vert x-y\vert}^2_\eta
\right)
\left(
\text{non-singular}
\right)
\,.
$$

=--

(e.g. [Scharf 95 (2.3.18)](causal+perturbation+theory#Scharf95))


+-- {: .proof}
###### Proof



Consider the formula for the [[causal propagator]] in terms of the mode expansion (eq:CausalPropagatorModeExpansionForKleinGordonOnMinkowskiSpacetime). Since the [[integrand]] here depends on the [[wave vector]] $\vec k$ only via its [[norm]] ${\vert \vec k\vert}$ and the [[angle]] $\theta$ it makes with the given [[spacetime]] [[vector]] via

$$
\vec k \cdot (\vec x - \vec y)
\;=\;
{\vert \vec k\vert} \, {\vert \vec x\vert} \, \cos(\theta)
$$


we may express the [[integration]] in terms of [[polar coordinates]] as follws:


$$
\begin{aligned}
\Delta_S(x - y)
& =
\frac{-1}{(2\pi)^p}
\int \frac{1}{2 \omega(\vec k)/c}
\sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
e^{i \vec k \cdot (\vec x - \vec y)}
\, d^p \vec k
\\
& =
\frac{- vol_{S^{p-2}}}{(2\pi)^p}
\underset{{\vert \vec k\vert} \in \mathbb{R}_{\geq 0}}{\int}
\underset{ \theta \in [0,\pi] }{\int}
\frac{ 1 }{ \omega(\vec k)/c }
\sin\left( \omega(\vec k) (x^0 - y^0) /c \right)
e^{ i {\vert \vec k\vert} {\vert \vec x - \vec y\vert} \cos(\theta) }
{\vert \vec k\vert} ({\vert \vec k\vert} \sin(\theta))^{p-2}
\,
d \theta
\wedge
d {\vert \vec k\vert}
\end{aligned}
$$

We specialize further computation now to the case that the [[spacetime]] [[dimension]] is $p + 1 = 3 + 1$, in which case the above becomes

$$
\begin{aligned}
\Delta_S(x - y)
& =
\frac{- 2\pi}{(2\pi)^{3}}
\underset{{\vert \vec k\vert} \in \mathbb{R}_{\geq 0}}{\int}
\frac{ {\vert \vec k \vert}^2 }{ \omega(\vec k)/c }
\sin\left( \omega(\vec k) (x^0 - y^0) /c \right)
\underset{
=
\tfrac{1}{i {\vert \vec k\vert}\, {\vert \vec x - \vec y\vert} }
\left(
e^{i {\vert \vec k\vert}\, {\vert \vec x - \vec y\vert}}
-
e^{-i {\vert \vec k\vert}\, {\vert \vec x - \vec y\vert}}
\right)
}{
\underbrace{
\underset{ \cos(\theta) \in [-1,1] }{\int}
e^{ i {\vert \vec k\vert} {\vert \vec x - \vec y\vert} \cos(\theta) }
d \cos(\theta)
}
}
\wedge
d {\vert \vec k \vert}
\\
& =
\frac{- 2}{(2\pi)^{2} {\vert \vec x - \vec y\vert}}
\underset{{\vert \vec k\vert} \in \mathbb{R}_{\geq 0}}{\int}
\frac{ {\vert \vec k \vert} }{ \omega(\vec k)/c }
\sin\left( \omega(\vec k) (x^0 - y^0) /c \right)
\sin\left( {\vert \vec k\vert}\, {\vert \vec x - \vec y\vert} \right)
\\
& =
\frac{- 2}{(2\pi)^{2} {\vert \vec x - \vec y\vert}}
\frac{d}{d {\vert \vec x - \vec y \vert } }
\underset{{\vert \vec k\vert} \in \mathbb{R}_{\geq 0}}{\int}
\frac{ 1 }{ \omega(\vec k)/c }
\sin\left( \omega(\vec k) (x^0 - y^0) /c \right)
\cos\left( {\vert \vec k\vert}\, {\vert \vec x - \vec y\vert} \right)
\, d {\vert \vec k\vert}
\\
& =
\frac{- 1}{(2\pi)^{2} {\vert \vec x - \vec y\vert}}
\frac{d}{d {\vert \vec x - \vec y \vert } }
\underset{  \kappa \in \mathbb{R}  }{\int}
\frac{ 1 }{ \omega(\kappa)/c }
\sin\left( \omega(\kappa) (x^0 - y^0) /c \right)
\cos\left( \kappa\, {\vert \vec x - \vec y\vert} \right)
\, d \kappa
\\
& =
\frac{- 1}{2(2\pi)^{2} {\vert \vec x - \vec y\vert}}
\frac{d}{d {\vert \vec x - \vec y} \vert }
\left(
\underset{\coloneqq I_+}{
\underbrace{
\underset{ \kappa \in \mathbb{R}  }{\int}
\frac{ 1 }{ \omega(\kappa)/c }
\sin\left(
\omega(\kappa) (x^0 - y^0) /c
+
\kappa\, {\vert \vec x - \vec y\vert}
\right)
d\kappa
}
}
+
\underset{ \coloneqq I_- }{
\underbrace{
\underset{ \kappa \in \mathbb{R}  }{\int}
\frac{ 1 }{ \omega(\kappa)/c }
\sin\left(
\omega(\kappa) (x^0 - y^0) /c
-
\kappa\, {\vert \vec x - \vec y\vert}
\right)
\,
d \kappa
}
}
\right)
\,,
\end{aligned}
$$

where in the last step we used one of the [[trigonometric identities]].

In order to further evaluate this, we parameterize the remaining components $(\omega/c, \kappa)$ of the [[wave vector]]
by the dual [[rapidity]] $z$, via

$$
  \left(\cosh(z)\right)^2 - \left( \sinh(z)\right)^2 = 1
$$

as

$$
  \omega(\kappa)/c
  \;=\;
  \left(
    \tfrac{m c}{\hbar}
  \right)
  \cosh(z)
  \phantom{AA}
  \,,
  \phantom{AA}
  \kappa
  \;=\;
  \left(
    \tfrac{m c}{\hbar}
  \right)
  \sinh(z)
  \,,
$$

which makes use of the fact that $\omega(\kappa)$ is non-negative, by construction.
This [[change of integration variables]] makes the integrals under the braces above become

$$
  I_\pm
  \;=\;
  \int_{-\infty}^\infty
   \sin\left(
     \tfrac{m c}{\hbar}
     \left(
       (x^0 - y^0) \cosh(z)
       \pm
       {\vert \vec x - \vec y\vert}
       \sinh(z)
     \right)
   \right)
   \, d z
   \,.
$$

Next we similarly parameterize the vector $x-y$ by its [[rapidity]] $\tau$. That parameterization depends on whether
$x-y$ is spacelike or not, and if not, whether it is future or past directed.

First, if $x-y$ is [[spacelike]] in that ${\vert x-y\vert}^2_\eta \gt 0$
then we may parameterize as

$$
  (x^0 - y^0)
  =
  \sqrt{{\vert x-y\vert}^2_\eta} \sinh(\tau)
  \phantom{AA}
  \,,
  \phantom{AA}
  {\vert \vec x - \vec y\vert}
  =
  \sqrt{ {\vert x-y\vert}^2_\eta} \cosh(\tau)
$$

which yields

$$
  \begin{aligned}
    I_{\pm}
    & =
    \int_{-\infty}^\infty
     \sin\left(
       \tfrac{m c}{\hbar}
       \sqrt{ {\vert x-y\vert}^2_\eta }
       \left(
         \sinh(\tau) \cosh(z)
         \pm
         \cosh(\tau)
         \sinh(z)
       \right)
     \right)
     \, d z
     \\
     & =
    \int_{-\infty}^\infty
     \sin\left(
       \tfrac{m c}{\hbar}
       \sqrt{ {\vert x-y\vert}^2_\eta}
       \left(
          \sinh\left( \tau \pm z\right)
       \right)
     \right)
     \, d z
     \\
     & =
    \int_{-\infty}^\infty
     \sin\left(
       \tfrac{m c}{\hbar}
       \sqrt{ {\vert x-y\vert}^2_\eta }
       \left(
          \sinh\left( z \right)
       \right)
     \right)
     \, d z
     \\
     & = 0
     \,,
  \end{aligned}
$$

where in the last line we observe that the integrand is a skew-symmetric function of $z$.

Second, if $x-y$ is [[timelike]] with $(x^0 - y^0) \gt 0$ then we may parameterize as

$$
  (x^0 - y^0)
  =
  \sqrt{ -{\vert x-y\vert}^2_\eta} \cosh(\tau)
  \phantom{AA}
  \,,
  \phantom{AA}
  {\vert \vec x - \vec y\vert}
  =
  \sqrt{ -{\vert x - y\vert}^2_\eta }
  \sinh(\tau)
$$

which yields

$$
  \begin{aligned}
    I_\pm
    & =
    \int_{-\infty}^\infty
     \sin\left(
       \tfrac{m c}{\hbar}
       \left(
         (x^0 - y^0) \cosh(z)
         \pm
         {\vert \vec x - \vec y\vert}
         \sinh(z)
       \right)
     \right)
     \, d z
     \\
     & =
    \int_{-\infty}^\infty
     \sin\left(
       \sqrt{ - {\vert x-y\vert}^2_\eta }
       \tfrac{m c}{\hbar}
       \left(
         \cosh(\tau)\cosh(z)
         \pm
         \cosh(\tau)
         \sinh(z)
       \right)
     \right)
     \, d z
     \\
     & =
    \int_{-\infty}^\infty
     \sin\left(
       \sqrt{ - {\vert x-y\vert}^2_\eta }
       \tfrac{m c}{\hbar}
       \left(
         \cosh(z \pm \tau)
       \right)
     \right)
     \, d z
     \\
     & =
     \pi J_0\left( \sqrt{ - {\vert x-y\vert}^2_\eta} \tfrac{m c}{\hbar} \right)
   \end{aligned}
   \,.
$$

Here $J_0$ denotes the [[Bessel function]] of order 0. The important point here is that this is a smooth function.

Similarly, if $x-y$ is [[timelike]] with $(x^0 - y^0) \lt 0$ then the same argument yields

$$
  I_\pm = -  \pi J_0\left( \sqrt{ - {\vert x-y\vert}^2_\eta} \tfrac{m c}{\hbar} \right)
$$

In conclusion, the general form of $I_\pm$ is

$$
  I_\pm
  =
  \pi
  sgn(x^0 - y^0)
  \Theta\left( -{\vert x-y\vert}^2_\eta \right)
  J_0\left( \sqrt{ - {\vert x-y\vert}^2_\eta } \tfrac{m c}{\hbar} \right)
  \,.
$$

Therefore we end up with

$$
\begin{aligned}
\Delta_S(x,y)
& =
\frac{1}{4 \pi {\vert \vec x - \vec y\vert}}
\frac{d}{d {\vert \vec x - \vec y\vert}}
sgn(x^0) \Theta\left( -{\vert x-y\vert}^2_\eta \right)
J_0\left(
  \sqrt{ -{\vert x-y\vert}^2_\eta }
  \tfrac{m c}{\hbar}
\right)
\\
& =
\frac{-1}{2 \pi }
\frac{d}{d (-{\vert x-y\vert}^2_\eta)}
sgn(x^0) \Theta\left( -{\vert x-y\vert}^2_\eta \right)
J_0\left(
  \sqrt{-{\vert x-y \vert}^2_\eta} \tfrac{m c}{\hbar}
\right)
\\
& =
-\frac{1}{2 \pi }
\frac{d}{d (- \vert x-y\vert^2_{\eta})}
sgn(x^0) \Theta\left( - {\vert x - y\vert}^2_\eta \right)
J_0\left(
\tfrac{m c}{\hbar}  \sqrt{ -{\vert x-y\vert}^2_\eta }
\right)
\\
& =
\frac{-1}{2\pi}
sgn(x^0)
\left(
\delta\left(
-{\vert x-y\vert}^2_\eta
\right)
\;-\;
\Theta\left( -{\vert x-y\vert}^2_\eta  \right)
\frac{d}{d \left({-\vert x-y\vert}^2_\eta\right) }
J_0\left(
\tfrac{m c}{\hbar}  \sqrt{ -{\vert x-y\vert}^2_\eta }
\right)
\right)
\end{aligned}
$$

=--



$\,$

**[[Wightman propagator]]**
{#HadamardPropagatorForKleinGordonOnMinkowskiSpacetime}

Prop. \ref{CausalPropagatorAsFourierTransformOfDeltaDistributionOnTransformedKGOperator} exhibits the [[causal propagator]] of the [[Klein-Gordon operator]] on [[Minkowski spacetime]] as the difference of a contribution for [[positive real number|positive]] temporal [[angular frequency]] $k_0 \propto \omega(\vec k)$ (hence positive [[energy]] $\hbar \omega(\vec k)$ and a contribution of negative temporal [[angular frequency]].

The [[positive real number|positive]] [[frequency]] contribution to the [[causal propagator]] is called the _[[Wightman propagator]]_ (def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime} below), also known as the the _[[vacuum state]] [[2-point function]] of the [[free field|free]] [[real scalar field]] on [[Minkowski spacetime]]_. Notice that the temporal component
of the [[wave vector]] is proportional to the _negative_ [[angular frequency]]

$$
k_0 = -\omega/c
$$

(see at _[[plane wave]]_), therefore the appearance of the [[step function]] $\Theta(-k_0)$ in (eq:HadamardPropagatorForKleinGordonOperatorOnMinkowskiSpacetime) below:

+-- {: .num_defn #StandardHadamardDistributionOnMinkowskiSpacetime}
###### Definition
**([[Wightman propagator]] or [[vacuum state]] [[2-point function]] for [[Klein-Gordon operator]] on [[Minkowski spacetime]])**

The _[[Wightman propagator]]_ for the [[Klein-Gordon operator]] at [[mass]] $m$ on [[Minkowski spacetime]] is the [[tempered distribution|tempered]] [[distribution in two variables]] $\Delta_H \in \mathcal{S}'(\mathbb{R}^{p,1})$ which as a [[generalized function]] is given by the expression

$$
\label{HadamardPropagatorForKleinGordonOperatorOnMinkowskiSpacetime}
\begin{aligned}
\Delta_H(x,y)
& \coloneqq
\frac{1}{(2\pi)^p} \int \delta\left( k_\mu k^\mu + m^2 \right) \Theta( -k_0 ) e^{i k_\mu (x^\mu-y^\mu) } \, d^{p+1} k
\\
& =
\frac{1}{(2\pi)^p}
\int \frac{1}{2 \omega(\vec k)/c}
e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec y) }
\, d^p \vec k
\,,
\end{aligned}
$$

Here in the first line we have in the [[integrand]] the [[delta distribution]] of the [[Fourier transform]] of the [[Klein-Gordon operator]]  times a [[plane wave]] and times the [[step function]] $\Theta$ of the temporal component of the [[wave vector]]. In the second line we used the [[change of integration variables]] $k_0 = \sqrt{h}$, then the definition of the [[delta distribution]] and the fact that $\omega(\vec k)$ is by definition the [[non-negative real number|non-negative]] solution to the Klein-Gordon [[dispersion relation]].

=--

(e.g. [Khavkine-Moretti 14, equation (38) and section 3.4](#KhavkineMoretti14))

It is immediate but important that:

+-- {: .num_prop #OnMinkowskiWightmanIsDistributionalSolutionToKleinGordon}
###### Proposition
**([[Wightman propagator]] on [[Minkowski spacetime]] is [[distributional solution to a PDE|distributional solution]] to [[Klein-Gordon equation]])**

The [[Wightman propagator]] $\Delta_H$ (def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime}) is a [[distributional solution to a PDE|distributional solution]] to the [[Klein-Gordon equation]]

$$
  (\Box_x - m^2)\Delta_H(x,y) = 0
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition \ref{StandardHadamardDistributionOnMinkowskiSpacetime} the Wightman propagator is the [[Fourier transform of distributions]] of the [[product of distributions]]

$$
  \delta(k_\mu k^\mu + m^2) \Theta(-k_0)
  \,,
$$

where in turn the argument of the [[delta distribution]] is just $-1$ times the Fourier transform of the [Klein-Gordon operator]] itsel. This is clearly a solution to the equation

$$
  (-k_\mu k^\mu - m^2) \, \delta(k_\mu k^\mu + m^2) \Theta(-k_0)
  \;=\;
  0
  \,.
$$

Under [[Fourier inversion theorem|Fourier inversion]], this is the equation $(\Box_x - m^2)\Delta_H(x,y) = 0$, as in the proof of prop. \ref{AdvancedRetardedPropafatorsForKleinGordonOnMinkowskiSpacetime}.

=--



+-- {: .num_prop #ContourIntegralForStandardHadamardPropagatorOnMinkowskiSpacetime}
###### Proposition
**([[contour integral]] representation of the [[Wightman propagator]] for the [[Klein-Gordon operator]] on [[Minkowski spacetime]])

The [[Wightman propagator]] from
def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime} is
equivalently given by the [[contour integral]]

$$
\label{StandardHadamardPropagatorOnMinkowskiSpacetimeInTermsOfContourIntegral}
\Delta_H(x,y)
\;=\;
-i(2\pi)^{-(p+1)}
\int
\underset{C_+(\vec k)}{\oint}
\frac{e^{-i k_\mu (x-y)^\mu}}{ -k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 }
d k_0
d^{p} k
\,,
$$

where the [[Jordan curve]] $C_+(\vec k) \subset \mathbb{C}$ runs counter-clockwise, enclosing the point $+ \omega(\vec k)/c \in \mathbb{R} \subset \mathbb{C}$, but not enclosing the point $- \omega(\vec k)/c \in \mathbb{R} \subset \mathbb{C}$.


<img src="https://ncatlab.org/nlab/files/ContourForHadamardPropagator.png" height="200">

> graphics grabbed from [Kocic 16](#Kocic16)

=--

+-- {: .proof}
###### Proof

We compute as follows:

$$
\begin{aligned}
-i(2\pi)^{-(p+1)}
\int
\underset{C_+(\vec k)}{\oint}
\frac{e^{ - i k_\mu (x-y)^\mu}}{ -k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 }
d k_0
d^{p} k
& =
-i(2\pi)^{-(p+1)}
\int
\oint_{C_+(\vec k)}
\frac{
e^{ -i k_0 x^0} e^{i \vec k \cdot (\vec x - \vec y)}
}{
k_0^2 - \omega(\vec k)^2/c^2
}
d k_0
d^p \vec k
\\
& =
-i(2\pi)^{-(p+1)}
\int
\underset{C_+(\vec k)}{\oint}
\frac{
e^{ - i k_0 (x^0-y^0)} e^{i \vec k \cdot (\vec x - \vec y)}
}{
( k_0 - \omega_\epsilon(\vec k)  )
( k_0 + \omega_\epsilon(\vec k) )
}
d k_0
d^p \vec k
\\
& =
(2\pi)^{-p}
\int
\frac{1}{2 \omega(\vec k)}
e^{-i \omega(\vec k) (x^0-y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
d^p \vec k
\,.
\end{aligned}
$$

The last step is application of [[Cauchy's integral formula]], which says that the [[contour integral]] picks up the [[residue]] of the [[pole]] of the [[integrand]] at $+ \omega(\vec k)/c \in \mathbb{R} \subset \mathbb{C}$. The last line is $\Delta_H(x,y)$, by definition \ref{StandardHadamardDistributionOnMinkowskiSpacetime}.



=--



+-- {: .num_prop #SkewSymmetricPartOfHadmrdPropagatorIsCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetime}
###### Proposition
**(skew-symmetric part of [[Wightman propagator]] is the [[causal propagator]])**

The [[Wightman propagator]] for the [[Klein-Gordon equation]] on [[Minkowski spacetime]] (def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime}) is of the form

$$
  \label{DeompositionOfHadamardPropagatorOnMinkowkski}
  \begin{aligned}
    \Delta_H
    & =
    \tfrac{i}{2} \Delta_S
    +
    H
    \\
    & =
    \tfrac{i}{2}
    \left(
      \Delta_+ - \Delta_-
    \right)
    +
    H
  \end{aligned}
  \,,
$$

where

1. $\Delta_S$ is the [[causal propagator]] (prop. \ref{AdvancedRetardedPropagatorsForKleinGordonOnMinkowskiSpacetime}),
   which is real (eq:CausalPropagatorForKleinGordonEquationOnMinkowskiSpacetimeIsReal) and skew-symmetric (prop. \ref{CausalPropagatorIsSkewSymmetric})

   $$
     (\Delta_S(x,y))^\ast = \Delta_S(x,y)
     \phantom{AA}
     \,,
     \phantom{AA}
     \Delta_S(y,x) = - \Delta_S(x,y)
   $$

1. $H$ is real and symmetric

   $$
     (H(x,y))^\ast = H(x,y)
     \phantom{AA}
     \,,
     \phantom{AA}
     H(y,x) = H(x,y)
   $$

=--


+-- {: .proof}
###### Proof


By applying [[Euler's formula]] to (eq:HadamardPropagatorForKleinGordonOperatorOnMinkowskiSpacetime) we obtain

$$
  \label{SymmetricPartOfHadamardPropagatorForKleinGordonOnMinkowskiSpacetime}
  \begin{aligned}
  \Delta_H(x,y)
  & =
  \frac{1}{(2\pi)^p}
   \int \frac{1}{2 \omega(\vec k)/c}
   e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec y) }
   \, d^p \vec k
  \\
  & =
   \tfrac{i}{2}
   \underset{= \Delta_S(x,y)}{
   \underbrace{
     \frac{-1}{(2\pi)^p}
     \int
     \frac{1}{\omega(\vec k)/c}
     \sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
     e^{i \vec k \cdot (\vec x - \vec y) }
     \, d^p \vec k
   }}
   \;+\;
   \underset{
     \coloneqq H(x,y)
   }{
   \underbrace{
    \frac{1}{(2\pi)^p}
     \int \frac{1}{2 \omega(\vec k)/c}
     \cos\left( \omega(\vec k)(x^0 - y^0)/c  \right)
     e^{i \vec k \cdot (\vec x - \vec y) }
     \, d^p \vec k
   }}
  \end{aligned}
$$

On the left this identifies the [[causal propagator]] by (eq:CausalPropagatorModeExpansionForKleinGordonOnMinkowskiSpacetime), prop. \ref{ModeExpansionOfCausalPropagatorForKleinGordonOnMinkowski}.

The second summand changes, both under complex conjugation as well as under $(x-y) \mapsto (y-x)$,
via [[change of integration variables]] $\vec k \mapsto - \vec k$ (because the [[cosine]] is an even function).
This does not change the integral, and hence $H$ is symmetric.

=--




$\,$

**[[Feynman propagator]]**
 {#FeynmanPropagator}

We have seen that the [[positive real number|positive]] [[frequency]] component of the [[causal propagator]] $\Delta_S$ for the [[Klein-Gordon equation]] on [[Minkowski spacetime]] (prop. \ref{AdvancedRetardedPropagatorsForKleinGordonOnMinkowskiSpacetime}) is the [[Wightman propagator]] $\Delta_H$ (def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime}) given, according to prop. \ref{SkewSymmetricPartOfHadmrdPropagatorIsCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetime}, by (eq:DeompositionOfHadamardPropagatorOnMinkowkski)

$$
  \begin{aligned}
    \Delta_H
    & =
    \tfrac{i}{2} \Delta_S
    +
    H
    \\
    & =
    \tfrac{i}{2}
    \left(
      \Delta_+ - \Delta_-
    \right)
    +
    H
  \end{aligned}
  \,.
$$

There is an evident variant of this combination, which will be of interest:


+-- {: .num_defn #FeynmanPropagatorForKleinGordonEquationOnMinkowskiSpacetime}
###### Definition
**([[Feynman propagator]] for [[Klein-Gordon equation]] on [[Minkowski spacetime]])**

The _[[Feynman propagator]]_ for the [[Klein-Gordon equation]] on [[Minkowski spacetime]] is the [[linear combination]]

$$
  \Delta_F
  \coloneqq
    \tfrac{i}{2}
    \left(
      \Delta_+ + \Delta_-
    \right)
    +
    H
$$

where the first term is proportional to the sum of the [[advanced and retarded propagators]] (prop. \ref{AdvancedRetardedPropagatorsForKleinGordonOnMinkowskiSpacetime}) and the second is the symmetric part of the [[Wightman propagator]] according to prop. \ref{SkewSymmetricPartOfHadmrdPropagatorIsCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetime}.

Similarly the _[[anti-Feynman propagator]]_ is

$$
  \Delta_{\overline{F}}
  \coloneqq
    \tfrac{i}{2}
    \left(
      \Delta_+ + \Delta_-
    \right)
    -
    H
  \,.
$$

=--


+-- {: .num_prop #ModeExpansionForFeynmanPropagatorOfKleinGordonEquationOnMinkowskiSpacetime}
###### Proposition
**(mode expansion for [[Feynman propagator]] of [[Klein-Gordon equation]] on [[Minkowski spacetime]])**

The [[Feynman propagator]] (def. \ref{FeynmanPropagatorForKleinGordonEquationOnMinkowskiSpacetime}) for the [[Klein-Gordon equation]] on [[Minkowski spacetime]] is given by the following equivalent expressions

$$
  \begin{aligned}
  \Delta_F(x,y)
  & =
  \left\{
    \array{
    \frac{1}{(2\pi)^p}
    \int
    \frac{1}{\omega(\vec k)c}
    e^{-i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \gt 0
    \\
    \frac{1}{(2\pi)^p}
    \int
    \frac{1}{2\omega(\vec k)c}
    e^{+i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \lt 0
    }
  \right.
  \\
  & =
  \left\{
    \array{
      \Delta_H(x,y) &\vert& (x^0 - y^0) \gt 0
      \\
      \Delta_H(y,x) &\vert& (x^0 - y^0) \lt 0
    }
  \right.
  \end{aligned}
$$

Similarly the [[anti-Feynman propagator]] is equivalently given by

$$
  \begin{aligned}
  \Delta_{\overline{F}}(x,y)
  & =
  \left\{
    \array{
    \frac{-}{(2\pi)^p}
    \int
    \frac{1}{\omega(\vec k)c}
    e^{+i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \gt 0
    \\
    \frac{-}{(2\pi)^p}
    \int
    \frac{1}{2\omega(\vec k)c}
    e^{-i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \lt 0
    }
  \right.
  \\
  & =
  \left\{
    \array{
      -\Delta_H(y,x) &\vert& (x^0 - y^0) \gt 0
      \\
      -\Delta_H(x,y) &\vert& (x^0 - y^0) \lt 0
    }
  \right.
  \end{aligned}
$$


=--

+-- {: .proof}
###### Proof


By the mode expansion of $\Delta_{\pm}$ from (eq:ModeExpansionForMinkowskiAdvancedRetardedPropagator) and the mode expansion of $H$ from (eq:SymmetricPartOfHadamardPropagatorForKleinGordonOnMinkowskiSpacetime) we have

$$
  \begin{aligned}
   \Delta_F(x,y)
   & =
  \left\{
    \array{
      \underset{
        = \tfrac{i}{2} \Delta_+(x,y) + 0 \;\text{for}\; (x^0 - y^0) \gt 0
      }{
      \underbrace{
      \frac{- i}{(2\pi)^{p}}
      \int
      \frac{1}{2 \omega(\vec k)/c}
      \sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
      e^{i \vec k \cdot (\vec x - \vec  y) }
      \, d^p \vec k
      }
      }
      +
      \underset{
        = H(x,y)
      }{
      \underbrace{
      \frac{1}{(2\pi)^p}
      \int \frac{1}{2 \omega(\vec k)/c}
      \cos\left( \omega(\vec k)(x^0 - y^0)/c  \right)
      e^{i \vec k \cdot (\vec x - \vec y) }
      \, d^p \vec k
      }
      }
      &\vert&
      (x^0 - y^0) \gt 0
      \\
      \underset{
         = 0 + \tfrac{i}{2}\Delta_-(x,y) \;\text{for}\; (x^0 - y^0) \lt 0
      }{
      \underbrace{
      \frac{+ i}{(2\pi)^{p}}
      \int
      \frac{1}{2 \omega(\vec k)/c}
      \sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
      e^{i \vec k \cdot (\vec x - \vec  y) }
      \, d^p \vec k
      }
      }
      +
      \underset{ = H(x,y) }{
      \underbrace{
      \frac{1}{(2\pi)^p}
      \int \frac{1}{2 \omega(\vec k)/c}
      \cos\left( \omega(\vec k)(x^0 - y^0)/c  \right)
      e^{i \vec k \cdot (\vec x - \vec y) }
      \, d^p \vec k
      }
      }
      &\vert&
      (x^0 - y^0) \lt 0
    }
  \right.
  \\
  & =
  \left\{
    \array{
    \frac{1}{(2\pi)^p}
    \int
    \frac{1}{2\omega(\vec k)c}
    e^{-i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \gt 0
    \\
    \frac{1}{(2\pi)^p}
    \int
    \frac{1}{2\omega(\vec k)c}
    e^{+i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \lt 0
    }
  \right.
  \\
  & =
  \left\{
    \array{
      \Delta_H(x,y) &\vert& (x^0 - y^0) \gt 0
      \\
      \Delta_H(y,x) &\vert& (x^0 - y^0) \lt 0
    }
  \right.
  \end{aligned}
$$

where in the second line we used [[Euler's formula]]. The last line follows by comparison with (eq:HadamardPropagatorForKleinGordonOperatorOnMinkowskiSpacetime) and using that the integral over $\vec k$
is invariant under $\vec k \mapsto - \vec k$.

The computation for $\Delta_{\overline{F}}$ is the same, only now with a minus sign in front of the [[cosine]]:

$$
  \begin{aligned}
   \Delta_{\overline{F}}(x,y)
   & =
  \left\{
    \array{
      \underset{
        = \tfrac{i}{2} \Delta_+(x,y) + 0 \;\text{for}\; (x^0 - y^0) \gt 0
      }{
      \underbrace{
      \frac{- i}{(2\pi)^{p}}
      \int
      \frac{1}{2 \omega(\vec k)/c}
      \sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
      e^{i \vec k \cdot (\vec x - \vec  y) }
      \, d^p \vec k
      }
      }
      -
      \underset{
        = H(x,y)
      }{
      \underbrace{
      \frac{1}{(2\pi)^p}
      \int \frac{1}{2 \omega(\vec k)/c}
      \cos\left( \omega(\vec k)(x^0 - y^0)/c  \right)
      e^{i \vec k \cdot (\vec x - \vec y) }
      \, d^p \vec k
      }
      }
      &\vert&
      (x^0 - y^0) \gt 0
      \\
      \underset{
         = 0 + \tfrac{i}{2}\Delta_-(x,y) \;\text{for}\; (x^0 - y^0) \lt 0
      }{
      \underbrace{
      \frac{+ i}{(2\pi)^{p}}
      \int
      \frac{1}{2 \omega(\vec k)/c}
      \sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
      e^{i \vec k \cdot (\vec x - \vec  y) }
      \, d^p \vec k
      }
      }
      -
      \underset{ = H(x,y) }{
      \underbrace{
      \frac{1}{(2\pi)^p}
      \int \frac{1}{2 \omega(\vec k)/c}
      \cos\left( \omega(\vec k)(x^0 - y^0)/c  \right)
      e^{i \vec k \cdot (\vec x - \vec y) }
      \, d^p \vec k
      }
      }
      &\vert&
      (x^0 - y^0) \lt 0
    }
  \right.
  \\
  & =
  \left\{
    \array{
    \frac{-1}{(2\pi)^p}
    \int
    \frac{1}{2\omega(\vec k)c}
    e^{+i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \gt 0
    \\
    \frac{-1}{(2\pi)^p}
    \int
    \frac{1}{2\omega(\vec k)c}
    e^{-1i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \lt 0
    }
  \right.
  \\
  & =
  \left\{
    \array{
      - \Delta_H(y,x) &\vert& (x^0 - y^0) \gt 0
      \\
      - \Delta_H(x,y) &\vert& (x^0 - y^0) \lt 0
    }
  \right.
  \end{aligned}
$$


=--

As before for the [[causal propagator]], there are equivalent reformulations of the [[Feynman propagator]], which are useful for computations:

+-- {: .num_prop #FeynmanPropagatorAsACauchyPrincipalvalue}
###### Proposition
**([[Feynman propagator]] as a [[Cauchy principal value]])**

The [[Feynman propagator]] and [[anti-Feynman propagator]] (def. \ref{FeynmanPropagatorForKleinGordonEquationOnMinkowskiSpacetime}) for the [[Klein-Gordon equation]] on [[Minkowski spacetime]] is equivalently given by the following expressions, respectively:

$$
  \begin{aligned}
  \left.
  \array{
    \Delta_F(x,y)
    \\
    \Delta_{\overline{F}}(x,y)
  }
  \right\}
  & =
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{-i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu (x^\mu - y^\mu)}
  }{
    - k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 \pm i \epsilon
  }
  \, d k_0 \, d^p \vec k
  \end{aligned}
$$

where we have a [[limit of a sequence|limit]] of [[distributions]] as for the [[Cauchy principal value]] ([this prop](Cauchy+principal+vlue#CauchyPrincipalValueEqualsIntegrationWithImaginaryOffsetPlusDelta)).

=--

+-- {: .proof}
###### Proof

We compute as follows:

$$
  \begin{aligned}
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{-i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu (x^\mu - y^\mu)}
  }{
    - k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 \pm i \epsilon
  }
  \, d k_0 \, d^p \vec k
  & =
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{-i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu (x^\mu - y^\mu)}
  }{
    (k_0)^2
      -
    \underset{
      \coloneqq \omega_{\pm\epsilon}(\vec k)^2/c^2
    }{\underbrace{ \left( \omega(\vec k)^2/c^2 \mp i \epsilon \right) }}
  }
  \, d k_0 \, d^p \vec k
  \\
  & =
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{-i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu (x^\mu - y^\mu)}
  }{
     \left(
       k_0 - \omega_{\pm \epsilon}(\vec k)/c
     \right)
     \left(
       k_0 + \omega_{\pm \epsilon}(\vec k)/c
     \right)
  }
  \, d k_0 \, d^p \vec k
  \\
  & =
  \left\{
    \array{
    \frac{\pm 1}{(2\pi)^p}
    \int
    \frac{1}{2\omega(\vec k)c}
    e^{\mp i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \gt 0
    \\
    \frac{\pm 1}{(2\pi)^p}
    \int
    \frac{1}{2\omega(\vec k)c}
    e^{\pm i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \lt 0
    }
  \right.
  \\
  & =
  \left\{
    \array{
      \Delta_F(x,y)
      \\
      \Delta_{\overline{F}}(x,y)
    }
  \right.
  \end{aligned}
$$

Here

1. In the first step we introduced the [[complex number|complex]] [[square root]] $\omega_{\pm \epsilon}(\vec k)$. For this to be compatible with the choice of _non-negative_ square root for $\epsilon = 0$ in (eq:DispersionRelationForKleinGordonooeratorObMinkowskiSpacetime) we need to choose that complex square root whose [[complex phase]] is one half that of $\omega(\vec k)^2 - i \epsilon$ (instead of that plus [[π]]). This means that $\omega_{+ \epsilon}(\vec k)$ is in the _[[lower half plane]]_ and $\omega_-(\vec k)$ is in the [[upper half plane]].

1. In the third step we observe that

   1. for $(x^0 - y^0) \gt 0$ the [[integrand]] decays for [[positive real number|positive]] [[imaginary part]] and hence the integration over $k_0$ may be deformed to a [[Jordan curve|contour]] which encircles the [[pole]] in the [[upper half plane]];


   1. for $(x^0 - y^0) \lt 0$ the integrand decays for [[negative real number|negative]] [[imaginary part]]  and hence the integration over $k_0$ may be deformed to a [[Jordan curve|contour]] which encircles the [[pole]] in the [[lower half plane]]

   and then apply [[Cauchy's integral formula]] which picks out $2\pi i$ times the [[residue]] a these poles.

   <img src="https://ncatlab.org/nlab/files/ContourForFeynmanPropagator.png" height="300">

   Notice that when completing to a contour in the [[lower half plane]] we pick up a minus signs from the fact that now the contour runs clockwise.

1. In the fourth step we used prop. \ref{ModeExpansionForFeynmanPropagatorOfKleinGordonEquationOnMinkowskiSpacetime}.

=--


$\,$

$\,$

**[[singular support]] and [[wave front sets]]**
{#WaveFrontSetsOfPropagatorsForKleinGordonOperatorOnMinkowskiSpacetime}

We now discuss the [[singular support]] and the [[wave front sets]] of the various [[propagators]] for the [[Klein-Gordon equation]] on [[Minkowski spacetime]].


+-- {: .num_prop #SingularSupportOfCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetimeIsTheLightCone}
###### Proposition
**([[singular support]] of the [[causal propagator]] of the [[Klein-Gordon equation]] on [[Minkowski spacetime]] is the [[light cone]])**

The [[singular support]] of the [[causal propagator]] $\Delta_S$ for the [[Klein-Gordon equation]] on [[Minkowski spacetime]],
regarded via [[translation]] [[invariant|invariance]] as a [[generalized function]] in a single variable (eq:TranslationInvariantKleinGordonPropagatorsOnMinkowskiSpacetime)
is the [[light cone]] of the origin:

$$
  supp_{sing}(\Delta_S)
  \;=\;
  \left\{
    x \in \mathbb{R}^{p,1}
    \,\vert\,
    {\vert x\vert}^2_\eta = 0
  \right\}
  \,.
$$

=--


+-- {: .proof}
###### Proof

The statement follows immediately from the result
([Gel'fand-Shilov 66, III 2.11 (7), p 294](#GelfandShilov66)), see [this prop.](Cauchy+principal+value#FourierTransformOfDeltaDistributionappliedToMassShell)

We make this fully explicit now in the special case of [[spacetime]] [[dimension]]

$$
  p + 1 = 3 + 1
$$

by computing an explicit form for the [[causal propagator]] in terms of the [[delta distribution]],
the [[Heaviside distribution]] and [[smooth function|smooth]] [[Bessel functions]].

We follow ([Scharf 95 (2.3.18)](causal+perturbation+theory#Scharf95)).


Consider the formula for the [[causal propagator]] in terms of the mode expansion (eq:CausalPropagatorModeExpansionForKleinGordonOnMinkowskiSpacetime). Since the [[integrand]] here depends on the [[wave vector]] $\vec k$ only via its [[norm]] ${\vert \vec k\vert}$ and the [[angle]] $\theta$ it makes with the given [[spacetime]] [[vector]] via

$$
\vec k \cdot (\vec x - \vec y)
\;=\;
{\vert \vec k\vert} \, {\vert \vec x\vert} \, \cos(\theta)
$$


we may express the [[integration]] in terms of [[polar coordinates]] as follws:


$$
\begin{aligned}
\Delta_S(x - y)
& =
\frac{-1}{(2\pi)^p}
\int \frac{1}{2 \omega(\vec k)/c}
\sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
e^{i \vec k \cdot (\vec x - \vec y)}
\, d^p \vec k
\\
& =
\frac{- vol_{S^{p-2}}}{(2\pi)^p}
\underset{{\vert \vec k\vert} \in \mathbb{R}_{\geq 0}}{\int}
\underset{ \theta \in [0,\pi] }{\int}
\frac{ 1 }{ \omega(\vec k)/c }
\sin\left( \omega(\vec k) (x^0 - y^0) /c \right)
e^{ i {\vert \vec k\vert} {\vert \vec x - \vec y\vert} \cos(\theta) }
{\vert \vec k\vert} ({\vert \vec k\vert} \sin(\theta))^{p-2}
\,
d \theta
\wedge
d {\vert \vec k\vert}
\end{aligned}
$$


In the special case of [[spacetime]] [[dimension]] $p + 1 = 3 + 1$ this becomes

$$
\label{StepsInComputingCausalPropagatorIn3plus1Dimension}
\begin{aligned}
\Delta_S(x - y)
& =
\frac{- 2\pi}{(2\pi)^{3}}
\underset{{\vert \vec k\vert} \in \mathbb{R}_{\geq 0}}{\int}
\frac{ {\vert \vec k \vert}^2 }{ \omega(\vec k)/c }
\sin\left( \omega(\vec k) (x^0 - y^0) /c \right)
\underset{
=
\tfrac{1}{i {\vert \vec k\vert}\, {\vert \vec x - \vec y\vert} }
\left(
e^{i {\vert \vec k\vert}\, {\vert \vec x - \vec y\vert}}
-
e^{-i {\vert \vec k\vert}\, {\vert \vec x - \vec y\vert}}
\right)
}{
\underbrace{
\underset{ \cos(\theta) \in [-1,1] }{\int}
e^{ i {\vert \vec k\vert} {\vert \vec x - \vec y\vert} \cos(\theta) }
d \cos(\theta)
}
}
\wedge
d {\vert \vec k \vert}
\\
& =
\frac{- 2}{(2\pi)^{2} {\vert \vec x - \vec y\vert}}
\underset{{\vert \vec k\vert} \in \mathbb{R}_{\geq 0}}{\int}
\frac{ {\vert \vec k \vert} }{ \omega(\vec k)/c }
\sin\left( \omega(\vec k) (x^0 - y^0) /c \right)
\sin\left( {\vert \vec k\vert}\, {\vert \vec x - \vec y\vert} \right)
\, d {\vert \vec k\vert}
\\
& =
\frac{- 2}{(2\pi)^{2} {\vert \vec x - \vec y\vert}}
\frac{d}{d {\vert \vec x - \vec y \vert } }
\underset{{\vert \vec k\vert} \in \mathbb{R}_{\geq 0}}{\int}
\frac{ 1 }{ \omega(\vec k)/c }
\sin\left( \omega(\vec k) (x^0 - y^0) /c \right)
\cos\left( {\vert \vec k\vert}\, {\vert \vec x - \vec y\vert} \right)
\, d {\vert \vec k\vert}
\\
& =
\frac{- 1}{(2\pi)^{2} {\vert \vec x - \vec y\vert}}
\frac{d}{d {\vert \vec x - \vec y \vert } }
\underset{  \kappa \in \mathbb{R}  }{\int}
\frac{ 1 }{ \omega(\kappa)/c }
\sin\left( \omega(\kappa) (x^0 - y^0) /c \right)
\cos\left( \kappa\, {\vert \vec x - \vec y\vert} \right)
\, d \kappa
\\
& =
\frac{- 1}{2(2\pi)^{2} {\vert \vec x - \vec y\vert}}
\frac{d}{d {\vert \vec x - \vec y} \vert }
\left(
\underset{\coloneqq I_+}{
\underbrace{
\underset{ \kappa \in \mathbb{R}  }{\int}
\frac{ 1 }{ \omega(\kappa)/c }
\sin\left(
\omega(\kappa) (x^0 - y^0) /c
+
\kappa\, {\vert \vec x - \vec y\vert}
\right)
d\kappa
}
}
+
\underset{ \coloneqq I_- }{
\underbrace{
\underset{ \kappa \in \mathbb{R}  }{\int}
\frac{ 1 }{ \omega(\kappa)/c }
\sin\left(
\omega(\kappa) (x^0 - y^0) /c
-
\kappa\, {\vert \vec x - \vec y\vert}
\right)
\,
d \kappa
}
}
\right)
\,.
\end{aligned}
$$

Here in the second but last step we renamed $\kappa \coloneqq {\vert \vec k\vert}$ and
doubled the integration domain for  convenience,
and in the last step we used the [[trigonometric identity]] $\sin(\alpha) \cos(\beta)\;=\; \tfrac{1}{2} \left( \sin(\alpha + \beta) + \sin(\alpha - \beta) \right)$.


In order to further evaluate this, we parameterize the remaining components $(\omega/c, \kappa)$ of the [[wave vector]]
by the dual [[rapidity]] $z$, via

$$
  \left(\cosh(z)\right)^2 - \left( \sinh(z)\right)^2 = 1
$$

as

$$
  \omega(\kappa)/c
  \;=\;
  \left(
    \tfrac{m c}{\hbar}
  \right)
  \cosh(z)
  \phantom{AA}
  \,,
  \phantom{AA}
  \kappa
  \;=\;
  \left(
    \tfrac{m c}{\hbar}
  \right)
  \sinh(z)
  \,,
$$

which makes use of the fact that $\omega(\kappa)$ is non-negative, by construction.
This [[change of integration variables]] makes the integrals under the braces above become

$$
  \label{TheTwoSpecialFunctionIntegralsInTheComputationOfTheCausalPropagatorIn3Plus1DOnMinkowski}
  I_\pm
  \;=\;
  \int_{-\infty}^\infty
   \sin\left(
     \tfrac{m c}{\hbar}
     \left(
       (x^0 - y^0) \cosh(z)
       \pm
       {\vert \vec x - \vec y\vert}
       \sinh(z)
     \right)
   \right)
   \, d z
   \,.
$$

Next we similarly parameterize the vector $x-y$ by its [[rapidity]] $\tau$. That parameterization depends on whether
$x-y$ is spacelike or not, and if not, whether it is future or past directed.

First, if $x-y$ is [[spacelike]] in that ${\vert x-y\vert}^2_\eta \gt 0$
then we may parameterize as

$$
  (x^0 - y^0)
  =
  \sqrt{{\vert x-y\vert}^2_\eta} \sinh(\tau)
  \phantom{AA}
  \,,
  \phantom{AA}
  {\vert \vec x - \vec y\vert}
  =
  \sqrt{ {\vert x-y\vert}^2_\eta} \cosh(\tau)
$$

which yields

$$
  \begin{aligned}
    I_{\pm}
    & =
    \int_{-\infty}^\infty
     \sin\left(
       \tfrac{m c}{\hbar}
       \sqrt{ {\vert x-y\vert}^2_\eta }
       \left(
         \sinh(\tau) \cosh(z)
         \pm
         \cosh(\tau)
         \sinh(z)
       \right)
     \right)
     \, d z
     \\
     & =
    \int_{-\infty}^\infty
     \sin\left(
       \tfrac{m c}{\hbar}
       \sqrt{ {\vert x-y\vert}^2_\eta}
       \left(
          \sinh\left( \tau \pm z\right)
       \right)
     \right)
     \, d z
     \\
     & =
    \int_{-\infty}^\infty
     \sin\left(
       \tfrac{m c}{\hbar}
       \sqrt{ {\vert x-y\vert}^2_\eta }
       \left(
          \sinh\left( z \right)
       \right)
     \right)
     \, d z
     \\
     & = 0
     \,,
  \end{aligned}
$$

where in the last line we observe that the integrand is a skew-symmetric function of $z$.

Second, if $x-y$ is [[timelike]] with $(x^0 - y^0) \gt 0$ then we may parameterize as

$$
  (x^0 - y^0)
  =
  \sqrt{ -{\vert x-y\vert}^2_\eta} \cosh(\tau)
  \phantom{AA}
  \,,
  \phantom{AA}
  {\vert \vec x - \vec y\vert}
  =
  \sqrt{ -{\vert x - y\vert}^2_\eta }
  \sinh(\tau)
$$

which yields

$$
  \label{IdentifyingTheBesselFunctionInComputationOfCausalPropagatorIn3Plus1DOnMinkowski}
  \begin{aligned}
    I_\pm
    & =
    \int_{-\infty}^\infty
     \sin\left(
       \tfrac{m c}{\hbar}
       \left(
         (x^0 - y^0) \cosh(z)
         \pm
         {\vert \vec x - \vec y\vert}
         \sinh(z)
       \right)
     \right)
     \, d z
     \\
     & =
    \int_{-\infty}^\infty
     \sin\left(
       \sqrt{ - {\vert x-y\vert}^2_\eta }
       \tfrac{m c}{\hbar}
       \left(
         \cosh(\tau)\cosh(z)
         \pm
         \cosh(\tau)
         \sinh(z)
       \right)
     \right)
     \, d z
     \\
     & =
    \int_{-\infty}^\infty
     \sin\left(
       \sqrt{ - {\vert x-y\vert}^2_\eta }
       \tfrac{m c}{\hbar}
       \left(
         \cosh(z \pm \tau)
       \right)
     \right)
     \, d z
     \\
     & =
     \pi J_0\left( \sqrt{ - {\vert x-y\vert}^2_\eta} \tfrac{m c}{\hbar} \right)
   \end{aligned}
   \,.
$$

Here in the last line we identified the integral representation of the [[Bessel function]] $J_0$ of order 0 (see [here](Bessel+function#eq:J0AsIntSinOfxCoshtdt)). The important point here is that this is a smooth function.

Similarly, if $x-y$ is [[timelike]] with $(x^0 - y^0) \lt 0$ then the same argument yields

$$
  I_\pm = -  \pi J_0\left( \sqrt{ - {\vert x-y\vert}^2_\eta} \tfrac{m c}{\hbar} \right)
$$

In conclusion, the general form of $I_\pm$ is

$$
  I_\pm
  =
  \pi
  sgn(x^0 - y^0)
  \Theta\left( -{\vert x-y\vert}^2_\eta \right)
  J_0\left( \sqrt{ - {\vert x-y\vert}^2_\eta } \tfrac{m c}{\hbar} \right)
  \,.
$$

Therefore we end up with

$$
\label{FinalResultOfComputationOf3Plus1dCausalPropagator}
\begin{aligned}
\Delta_S(x,y)
& =
\frac{1}{4 \pi {\vert \vec x - \vec y\vert}}
\frac{d}{d {\vert \vec x - \vec y\vert}}
sgn(x^0) \Theta\left( -{\vert x-y\vert}^2_\eta \right)
J_0\left(
  \sqrt{ -{\vert x-y\vert}^2_\eta }
  \tfrac{m c}{\hbar}
\right)
\\
& =
\frac{-1}{2 \pi }
\frac{d}{d (-{\vert x-y\vert}^2_\eta)}
sgn(x^0) \Theta\left( -{\vert x-y\vert}^2_\eta \right)
J_0\left(
  \sqrt{-{\vert x-y \vert}^2_\eta} \tfrac{m c}{\hbar}
\right)
\\
& =
-\frac{1}{2 \pi }
\frac{d}{d (- \vert x-y\vert^2_{\eta})}
sgn(x^0) \Theta\left( - {\vert x - y\vert}^2_\eta \right)
J_0\left(
\tfrac{m c}{\hbar}  \sqrt{ -{\vert x-y\vert}^2_\eta }
\right)
\\
& =
\frac{-1}{2\pi}
sgn(x^0)
\left(
\delta\left(
-{\vert x-y\vert}^2_\eta
\right)
\;-\;
\Theta\left( -{\vert x-y\vert}^2_\eta  \right)
\frac{d}{d \left({-\vert x-y\vert}^2_\eta\right) }
J_0\left(
\tfrac{m c}{\hbar}  \sqrt{ -{\vert x-y\vert}^2_\eta }
\right)
\right)
\end{aligned}
$$

=--


+-- {: .num_prop #SingularSupportOfHadamardPropagatorForKleinGordonEquationOnMinkowskiSpacetimeIsTheLightCone}
###### Proposition
**([[singular support]] of the [[Wightman propagator]] of the [[Klein-Gordon equation]] on [[Minkowski spacetime]] is the [[light cone]])**

The [[singular support]] of the [[Wightman propagator]] $\Delta_H$ (def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime}) for the [[Klein-Gordon equation]] on [[Minkowski spacetime]], regarded via [[translation]] [[invariant|invariance]] as a [[distribution]]
in a single variable, is the [[light cone]] of the origin:

$$
  supp_{sing}(\Delta_H)
  =
  \left\{
    x \in \mathbb{R}^{p,1}
    \;\vert\;
    {\vert x\vert}^2_\eta = 0
  \right\}
  \,.
$$

=--

+-- {: .proof}
###### Proof

The statement follows immediately from the result
([Gel'fand-Shilov 66, III 2.11 (7), p 294](#GelfandShilov66)), see [this prop.](Cauchy+principal+value#FourierTransformOfDeltaDistributionappliedToMassShell).

We make this fully explicit now in the special case of [[spacetime]] [[dimension]]

$$
  p + 1 = 3 + 1
$$

by computing an explicit form for the [[causal propagator]] in terms of the [[delta distribution]],
the [[Heaviside distribution]] and [[smooth function|smooth]] [[Bessel functions]].

We follow ([Scharf 95 (2.3.36)](causal+perturbation+theory#Scharf95)).


By (eq:SymmetricPartOfHadamardPropagatorForKleinGordonOnMinkowskiSpacetime) we have

$$
  \begin{aligned}
  \Delta_H(x,y)
   & =
   \tfrac{i}{2}
   \underset{= \Delta_S(x,y)}{
   \underbrace{
     \frac{-1}{(2\pi)^p}
     \int
     \frac{1}{\omega(\vec k)/c}
     \sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
     e^{i \vec k \cdot (\vec x - \vec y) }
     \, d^p \vec k
   }}
   \;+\;
   \underset{
     \coloneqq H(x,y)
   }{
   \underbrace{
    \frac{1}{(2\pi)^p}
     \int \frac{1}{2 \omega(\vec k)/c}
     \cos\left( \omega(\vec k)(x^0 - y^0)/c  \right)
     e^{i \vec k \cdot (\vec x - \vec y) }
     \, d^p \vec k
   }}
  \end{aligned}
$$

The first summand, proportional to the [[causal propagator]], which we computed as (eq:FinalResultOfComputationOf3Plus1dCausalPropagator)
in prop. \ref{SingularSupportOfCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetimeIsTheLightCone} to be

$$
  \tfrac{i}{2}\Delta_S(x,y)
  \;=\;
  \frac{-i}{4\pi}
  sgn(x^0)
  \left(
  \delta\left(
  -{\vert x-y\vert}^2_\eta
  \right)
  \;-\;
  \Theta\left( -{\vert x-y\vert}^2_\eta  \right)
  \frac{d}{d \left({-\vert x-y\vert}^2_\eta\right) }
  J_0\left(
  \tfrac{m c}{\hbar}  \sqrt{ -{\vert x-y\vert}^2_\eta }
  \right)
  \right)
  \,.
$$

The second term is computed in a directly analogous fashion: The integrals $I_\pm$ from
(eq:TheTwoSpecialFunctionIntegralsInTheComputationOfTheCausalPropagatorIn3Plus1DOnMinkowski) are now

$$
  I_\pm
  \coloneqq
  \int_{-\infty}^\infty
   \cos\left(
     \tfrac{m c}{\hbar}
     \left(
       (x^0 - y^0) \cosh(z)
       \pm
       {\vert \vec x - \vec y\vert}
       \sinh(z)
     \right)
   \right)
   \, d z
$$

Parameterizing by [[rapidity]], as in the proof of prop. \ref{SingularSupportOfCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetimeIsTheLightCone}, one finds that for [[timelike]] $x-y$ this is

$$
  \begin{aligned}
  I_\pm
  & =
    \int_{-\infty}^\infty
     \cos\left(
       \tfrac{m c}{\hbar}
       \sqrt{ {\vert x-y\vert}^2_\eta }
       \left(
          \cosh\left( z \right)
       \right)
     \right)
     \, d z
  \\
  & =
  - \pi N_0
  \left(
    \tfrac{m c}{\hbar}
    \sqrt{ {\vert x-y\vert}^2_\eta }
  \right)
  \end{aligned}
$$

while for [[spacelike]] $x-y$ it is

$$
  \begin{aligned}
    I_\pm
    & =
    \int_{-\infty}^\infty
     \cos\left(
       \tfrac{m c}{\hbar}
       \sqrt{ {\vert x-y\vert}^2_\eta }
       \left(
          \sinh\left( z \right)
       \right)
     \right)
     \, d z
     \\
    & =
    2 K_0
   \left(
     \tfrac{m c}{\hbar}
     \sqrt{ {\vert x-y\vert}^2_\eta }
   \right)
   \,,
  \end{aligned}
$$

where we identified the integral representations of the [[Neumann function]] $N_0$ (see [here](Bessel+function#N0AsIntSinOfxCoshtdt))
and of the [[modified Bessel function]] $K_0$ (see [here](Bessel+function#eq:K0AsIntSinOfxCoshtdt)).

As for the [[Bessel function]] $J_0$ in (eq:IdentifyingTheBesselFunctionInComputationOfCausalPropagatorIn3Plus1DOnMinkowski) the key point is that these are [[smooth functions]]. Hence we conclude that

$$
  H(x,y)
  \;\propto\;
  \frac{d}{d \left( {\vert x-y\vert}^2_\eta \right)}
  \left(
    -\Theta\left( -{\vert x-y\vert}^2_\eta \right)
    N_0
    \left(
      \tfrac{m c}{\hbar}
      \sqrt{ {\vert x-y\vert}^2_\eta }
    \right)
    +
    \Theta\left( {\vert x-y\vert}^2_\eta  \right)
    \tfrac{2}{\pi}
    K_0
   \left(
     \tfrac{m c}{\hbar}
     \sqrt{ {\vert x-y\vert}^2_\eta }
   \right)
  \right)
  \,.
$$

This expression has singularities on the [[light cone]] due to the [[step functions]].
In fact the expression being differentiated is continuous at the light cone
([Scharf 95 (2.3.34)](#Scharf95)), so that the singularity on the light cone is not a [[delta distribution]]
singularity from the derivative of the step functions. Accordingly it does not cancel the singularity
of $\tfrac{i}{2}\Delta_S(x,y)$ as above, and hence the singular support of $\Delta_H$ is still the whole
light cone.

=--


+-- {: .num_prop #SingularSupportOfFeynmanPropagatorForKleinGordonEquationOnMinkowskiSpacetime}
###### Proposition
**([[singular support]] of [[Feynman propagator]] for [[Klein-Gordon equation]] on [[Minkowski spacetime]])**

The [[singular support]] of the [[Feynman propagator]] $\Delta_H$ and of the [[anti-Feynman propagator]] $\Delta_{\overline{F}}$ (def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime}) for the [[Klein-Gordon equation]] on [[Minkowski spacetime]], regarded via [[translation]] [[invariant|invariance]] as a [[distribution]]
in a single variable, is the [[light cone]] of the origin:

$$
  \left.
  \array{
    supp_{sing}(\Delta_F)
    \\
    supp_{sing}(\Delta_{\overline{F}})
  }
  \right\}
  =
  \left\{
    x \in \mathbb{R}^{p,1}
    \;\vert\;
    {\vert x\vert}^2_\eta = 0
  \right\}
  \,.
$$

=--


+-- {: .proof}
###### Proof

The statement follows immediately from the result
([Gel'fand-Shilov 66, III 2.8 (8) and (9), p 289](#GelfandShilov66)), see [this prop.](Cauchy+principal+value#FourierTransformOfPrincipalValueOfPowerOfQuadraticForm).

=--


+-- {: .num_prop #WaveFronSetsForKGPropagatorsOnMinkowski}
###### Proposition
**([[wave front sets]] of [[propagators]] of [[Klein-Gordon equation]] on [[Minkowski spacetime]])**

The [[wave front set]] of the various [[propagators]] for the [[Klein-Gordon equation]] on [[Minkowski spacetime]], regarded, via [[translation]] [[invariant|invariance]], as [[distributions]] in a single variable, are as follows:

* the [[causal propagator]] $\Delta_S$ (prop. \ref{ModeExpansionOfCausalPropagatorForKleinGordonOnMinkowski}) has wave front set all pairs $(x,k)$ with $x$ and $k$ both on the lightcone:

$$
WF(\Delta_S) = \left\{ (x,k) \,\vert\, {\vert x\vert}^2_\eta = 0 \;\text{and} \; {\vert k\vert}^2_\eta = 0 \; \text{and} \, k \neq 0  \right\}
$$

<center>
<img src="https://ncatlab.org/nlab/files/RetGreenFunction.png" width="60"> <br/> - <br/> <img src="https://ncatlab.org/nlab/files/AdvancedGreenFunction.png" width="60">
</center>

* the [[Wightman propagator]] $\Delta_H$ (def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime}) has wave front set all pairs $(x,k)$ with $x$ and $k$ both on the light cone and $k^0 \gt 0$:

$$
WF(\Delta_H) = \left\{ (x,k) \,\vert\, {\vert x\vert}^2_\eta = 0 \;\text{and} \; {\vert k\vert}^2_\eta = 0 \; \text{and} \; k^0 \gt 0   \right\}
$$

<center>
<img src="https://ncatlab.org/nlab/files/HadamardPropagator.png" width="60">
</center>


* the [[Feynman propagator]] $\Delta_S$ (def. \ref{FeynmanPropagatorForKleinGordonEquationOnMinkowskiSpacetime}) has wave front set all pairs $(x,k)$ with $x$ and $k$ both on the light cone and $\pm k_0 \gt 0 \;\Leftrightarrow\; \pm x^0 \gt 0$

$$
  WF(\Delta_H) = \left\{ (x,k) \,\vert\, {\vert x\vert}^2_\eta = 0 \;\text{and} \; {\vert k\vert}^2_\eta = 0 \; \text{and} \;
    \left(
       \pm k_0 \gt 0 \;\Leftrightarrow\; \pm x^0 \gt 0
    \right)
  \right\}
$$

<center>
<img src="https://ncatlab.org/nlab/files/FeynmanPropagator.png" width="60">
</center>

=--

([Radzikowski 96, (16)](Hadamard+distribution#Radzikowski96))

+-- {: .proof}
###### Proof

First regarding the causal propagator:

By prop. \ref{SingularSupportOfCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetimeIsTheLightCone} the [[singular support]] of $\Delta_S$ is the [[light cone]].

Since the causal propagator is a solution to the homogeneous Klein-Gordon equation, the
[[propagation of singularities theorem]] says that also all [[wave vectors]] in the wave front set are lightlike.
Hence it just remains to show that all non-vanishing lightlike wave vectors based on the lightcone in spacetime
indeed do appear in the wave front set.

To that end, let $b \in C^\infty_{cp}(\mathbb{R}^{p,1})$ be a [[bump function]] whose [[compact support]] includes the origin.

For $a \in \mathbb{R}^{p,1}$ a point on the light cone, we need to determine the decay property of the Fourier transform of $x \mapsto b(x-a)\Delta_S(x)$. This is the [[convolution of distributions]] of $\hat b(k)e^{i k_\mu a^\mu}$ with $\widehat \Delta_S(k)$. By prop. \ref{CausalPropagatorAsFourierTransformOfDeltaDistributionOnTransformedKGOperator} we have

$$
\widehat \Delta_{S}(k)
\;\propto\;
\delta\left( -k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 \right)
sgn(k_0)
\,.
$$

This means that the convolution product is the smearing of the mass shell by $\widehat b(k)e^{i k_\u a^\mu}$.

Since the mass shell asymptotes to the light cone, and since $e^{i k_\mu a^\mu} = 1$ for $k$ on the light cone (given that $a$ is on the light cone), this implies the claim.


Now for the [[Wightman propagator]]:

By def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime} its Fourier transform is of the form

$$
\widehat \Delta_H(k)
\;\propto\;
\delta\left( k_\mu k^\mu + m^2 \right) \Theta( -k_0 )
$$

Moreover, its [[singular support]] is also the light cone (prop. \ref{SingularSupportOfHadamardPropagatorForKleinGordonEquationOnMinkowskiSpacetimeIsTheLightCone}).

Therefore now same argument as before says that the wave front set consists of wave vectors $k$ on the light cone, but now due to the [[step function]] factor $\Theta(-k_0)$ it must satisfy $0 \leq - k_0 = k^0$.

Finally regarding the [[Feynman propagator]]:

by prop. \ref{ModeExpansionForFeynmanPropagatorOfKleinGordonEquationOnMinkowskiSpacetime} the Feynman propagator
coincides with the positive frequency Wightman propagator for $x^0 \gt 0$ and with the "negative frequency Hadamard operator"
for $x^0 \lt 0$. Therefore the form of $WF(\Delta_F)$ now follows directly with that of $WF(\Delta_H)$ above.

=--











### For Dirac operator on Minkowski spacetime
 {#ExampleForDiracOperatorOnMinkowskiSpacetime}

Finally we observe that the [[propagators]] for the [[Dirac field]] on [[Minkowski spacetime]]
follow immediately from the propagators for the [[scalar field]]:

+-- {: .num_prop #DiracEquationOnMinkowskiSpacetimeAdvancedAndRetardedPropagators}
###### Proposition
**([[advanced and retarded propagator]] for [[Dirac equation]] on [[Minkowski spacetime]])**

Consider the [[Dirac operator]] on [[Minkowski spacetime]], which in [[Feynman slash notation]] reads

$$
  \begin{aligned}
    D
      & \coloneqq
    -i {\partial\!\!\!/\,}
     + \tfrac{m c}{\hbar}
    \\
    & =
    -i \gamma^\mu \frac{\partial}{\partial x^\mu} + \tfrac{m c}{\hbar}
  \end{aligned}
  \,.
$$

Its [[advanced and retarded propagators]] (def. \ref{AdvancedAndRetardedGreenFunctions})
are the [[derivatives of distributions]] of the advanced and retarded propagators $\Delta_\pm$ for the [[Klein-Gordon equation]] (prop. \ref{AdvancedRetardedPropagatorsForKleinGordonOnMinkowskiSpacetime}) by ${\partial\!\!\!/\,} + m$:

$$
  \Delta_{D, \pm}
  \;=\;
  \left(
    -i{\partial\!\!\!/\,} - \tfrac{m c}{\hbar}
  \right)
  \Delta_{\pm}
  \,.
$$

Hence the same is true for the [[causal propagator]]:

$$
  \Delta_{D, S}
  \;=\;
  \left(
    -i{\partial\!\!\!/\,} - \tfrac{m c}{\hbar}
  \right)
  \Delta_{S}
  \,.
$$


=--

+-- {: .proof}
###### Proof

Applying a [[differential operator]] does not change the [[support]] of a [[smooth function]], hence also not the [[support of a distribution]]. Therefore the uniqueness of the advanced and retarded propagators (prop. \ref{AdvancedAndRetardedGreenFunctionsForGreenHyperbolicOperatorAreUnique})
together with the translation-invariance and the anti-[[formally self-adjoint differential operator|formally self-adjointness]] of the [[Dirac operator]] (as for the [[Klein-Gordon operator]] (eq:TranslationInvariantKleinGordonPropagatorsOnMinkowskiSpacetime)
implies that it is sufficent to check that applying the [[Dirac operator]] to the $\Delta_{D, \pm}$
yields the [[delta distribution]]. This follows since the Dirac operator squares to the Klein-Gordon operator:


$$
  \begin{aligned}
    \left(
      -i{\partial\!\!\!/\,} + \tfrac{m c}{\hbar}
    \right)
    \Delta_{D, \pm}
    & =
    \underset{ = \Box - \left(\tfrac{m c}{\hbar}\right)^2}{
    \underbrace{
    \left(
      -i{\partial\!\!\!/\,} + \tfrac{m c}{\hbar}
    \right)
    \left(
      -i{\partial\!\!\!/\,} - \tfrac{m c}{\hbar}
    \right)
    }
    }
    \Delta_{\pm}
    \\
    & =
    \delta
  \end{aligned}
  \,.
$$

=--

Similarly we obtain the other [[propagators]] for the [[Dirac field]] from those of the [[real scalar field]]:

+-- {: .num_defn #HadamardPropagatorForDiracOperatorOnMinkowskiSpacetime}
###### Definition
**([[Wightman propagator]] for [[Dirac operator]] on [[Minkowski spacetime]])**

The _[[Wightman propagator]]_ for the [[Dirac operator]] on [[Minkowski spacetime]] is the [[positive real number|positive]] [[frequency]] part of the [[causal propagator]] (prop. \ref{DiracEquationOnMinkowskiSpacetimeAdvancedAndRetardedPropagators}),
hence the [[derivative of distributions]] of the Wightman propagator for the Klein-Gordon field (def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime}) by the [[Dirac operator]]:

$$
  \begin{aligned}
  \left(
     -i{\partial\!\!\!/\,} + \tfrac{m c}{\hbar}
  \right)\Delta_{H}(x,y)
  & =
  \frac{1}{(2\pi)^p} \int \delta\left( k_\mu k^\mu + m^2 \right) \Theta( -k_0 ) ( {k\!\!\!/\,} + \tfrac{m c}{\hbar}) e^{i k_\mu (x^\mu-y^\mu) } \, d^{p+1} k
  \\
  & =
  \frac{1}{(2\pi)^p}
  \int \frac{ \gamma^0 \omega(\vec k)/c + \vec \gamma \cdot \vec k + \tfrac{m c}{\hbar}   }{2 \omega(\vec k)/c}
  e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec y) }
  \, d^p \vec k
  \,.
  \end{aligned}
$$

Here we used the expression (eq:StandardHadamardDistributionOnMinkowskiSpacetime) for the Wightman propagator of the Klein-Gordon equation.

=--

+-- {: .num_defn #FeynmanPropagatorForDiracOperatorOnMinkowskiSpacetime}
###### Definition
**([[Feynman propagator]] for [[Dirac operator]] on [[Minkowski spacetime]])**

The _[[Feynman propagator]]_ for the [[Dirac operator]] on [[Minkowski spacetime]] is the linear combination

$$
  \Delta_{D, F}
  \;\coloneqq\;
  \Delta_{D,H}
  +
  i \Delta_{D, -}
$$

of the [[Wightman propagator]] (def. \ref{HadamardPropagatorForDiracOperatorOnMinkowskiSpacetime}) and the retarded propagator (prop. \ref{DiracEquationOnMinkowskiSpacetimeAdvancedAndRetardedPropagators}). By prop. \ref{FeynmanPropagatorAsACauchyPrincipalvalue}
this means that it is the
[[derivative of distributions]] of the [[Feynman propagator]] of the [[Klein-Gordon equation]] (def. \ref{FeynmanPropagatorForKleinGordonEquationOnMinkowskiSpacetime}) by the [[Dirac operator]]

$$
  \begin{aligned}
  \Delta_{D, F}
   & =
  \left(
     -i{\partial\!\!\!/\,} + \tfrac{m c}{\hbar}
  \right)\Delta_{F}(x,y)
  & =
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{-i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     \left( {k\!\!\!/\,} + \tfrac{m c}{\hbar} \right) e^{i k_\mu (x^\mu - y^\mu)}
  }{
    - k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 + i \epsilon
  }
  \, d k_0 \, d^p \vec k
  \,.
  \end{aligned}
$$


=--


## Related concepts

* [[causal propagator]]

* [[Feynman propagator]]

[[!include states and observables -- content]]



## References

Textbook discussion of the Hadamard distribution for [[free fields]] in [[Minkowski spacetime]] is in

* {#Scharf95} [[Günter Scharf]],  section 2.3 of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Springer 1995

* [[Günter Scharf]], section 1 of  _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

(there the Hadamard distribution is denoted "$-i D^+_m(x-y)$").

* {#Duetsch18} [[Michael Dütsch]], section 2.2. of _[[From classical field theory to perturbative quantum field theory]]_, 2018

A concise overview of the standard [[Wightman propagator]] on [[Minkowski spacetime]] and its relation to the other pertinent propagors is given in

* {#Kocic16} [[Mikica Kocic]], _Invariant Commutation and Propagation Functions Invariant Commutation and Propagation Functions_, 2016 ([[KGPropagatorsOnMinkowskiTable.pdf:file]])


On general [[globally hyperbolic spacetimes]] Hadamard spectrum condition was first rigorously defined in

* {#KayWald91} B. S. Kay, [[Robert Wald]], _Theorems on the uniqueness and thermal properties of stationary, nonsingular, quasifree states on spacetimes  with a bifurcate  Killing  horizon_, Phys.  Rep. 207(2), 49-136 (1991)

and shown to be equivalent to the definition in terms of singular structure in

* {#Radzikowski96} [[Marek Radzikowski]], _Micro-local approach to the Hadamard condition in quantum field theory on curved space-time_, Commun. Math. Phys. 179 (1996), 529&#8211;553 ([Euclid](http://projecteuclid.org/euclid.cmp/1104287114))

A gap in the Kay-Wald definition of Hadamard states and in the equivalence with Radzikowski's formulation has been discussed, by partially changing original Kay-Wald's definition,  and closed in 

* {#Moretti121} [[Valter Moretti]], _On the global Hadamard parametrix in QFT and the signed squared geodesic distance defined in domains larger than convex normal neighbourhoods_, Lett. Math. Phys. 2021 ([arXiv:2107.04903](https://arxiv.org/abs/2107.04903))

Hadamard states with [[smooth function|smooth]] dependence on the [[mass]] square (needed for [[dimensional regularization]] methods in [[causal perturbation theory]]/[[perturbative AQFT]]) are constructed in

* {#Keller10} [[Kai Keller]], chapter III of _Dimensional Regularization in Position Space and a Forest Formula for Regularized Epstein-Glaser Renormalization_, PhD thesis ([arXxiv:1006.2148](https://arxiv.org/abs/1006.2148))

Discussion of [[vacuum state]]-like Hadamard states is in

* {#BrumFredenhagen13} Marcos Brum, [[Klaus Fredenhagen]], _"Vacuum-like" Hadamard states for quantum fields on curved spacetimes_ ([arXiv:1307.0482](https://arxiv.org/abs/1307.0482))


Review and further developments are in

* {#Hollands07} [[Stefan Hollands]], appendix D of _Renormalized Quantum Yang-Mills Fields in Curved Spacetime_, Rev. Math. Phys. 20:1033-1172, 2008 ([arXiv:0705.3340](https://arxiv.org/abs/0705.3340))

* {#KhavkineMoretti14} [[Igor Khavkine]], [[Valter Moretti]], _Algebraic QFT in Curved Spacetime and quasifree Hadamard states: an introduction_, Chapter 5 in [[Romeo Brunetti]] et al. (eds.) _Advances in Algebraic Quantum Field Theory_, Springer, 2015 ([arXiv:1412.5945](https://arxiv.org/abs/1412.5945))

Discussion for [[electromagnetism]] is in

* [[Claudio Dappiaggi]], D. Siemssen, _Hadamard states for the vector potential on asymptotically flat spacetimes_, Rev. Math. Phys. 25, 1 (2013)


See also

* {#JunkerSchrohe02} W. Junker and E. Schrohe: _Adiabatic vacuum states on general spacetime manifolds: Definition, construction, and physical properties_, Annales Poincare Phys. Theor. 3, 1113
(2002)

* S. A. Fulling, M. Sweeny, [[Robert Wald]], _Singularity Structure Of The Two Point Function In Quantum Field Theory In Curved Space-Time_, Commun. Math.
Phys. 63, 257 (1978).

* {#FullingNarcowichWald81} S. A. Fulling, F. J. Narcowich, [[Robert Wald]], _Singularity Structure Of The Two Point Function In Quantum Field Theory In Curved Space-Time_, Annals Phys. 136, 243 (1981),


* Marcos Brum, [[Klaus Fredenhagen]], _"Vacuum-like" Hadamard states for quantum fields on curved spacetimes_, Classical and Quantum Gravity, Volume 31, Number 2 ([arXiv:1307.0482](https://arxiv.org/abs/1307.0482))

[[!redirects Hadamard distributions]]

[[!redirects quasi-free Hadamard state]]
[[!redirects quasi-free Hadamard states]]

[[!redirects Hadamard state]]
[[!redirects Hadamard states]]

[[!redirects Hadamard vacuum state]]
[[!redirects Hadamard vacuum states]]

[[!redirects Wightman propagator]]
[[!redirects Wightman propagators]]


[[!redirects Hadamard 2-point function]]
[[!redirects Hadamard 2-point functions]]

[[!redirects Wightman 2-point function]]
[[!redirects Wightman 2-point functions]]

[[!redirects Wightman propagator]]
[[!redirects Wightman propagators]]



