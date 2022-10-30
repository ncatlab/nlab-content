
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[physics]], a __scalar field__ is a [[field (physics)|field]] on [[spacetime]]/[[worldvolume]] which is simply a [[function]] with values in the [[field of scalars]], typically the [[real numbers]] $\mathbb{R}$ or [[complex numbers]] $\mathbb{C}$, sometimes the [[quaternions]] $\mathbb{H}$. Hence it is a [[field (physics)|field]] encoded by a [[field bundle]] which is a [[trivial line bundle]].

One fundamental (complex, charged) scalar field is seen in [[experiment]], the _[[Higgs field]]_, which is one component of the [[standard model of particle physics]]. A widely hypothesized scalar field is the [[inflaton]] field in [[model (physics)|models]] of [[cosmic inflation]], which however remains speculative and might in any case be an effective compound of more fundamental fields.

But scalar fields also serve as a key toy example in theoretical studies of [[field theory]], such as in [[phi^4 theory]] or in the [[Ising model]]. The usefulness of the scalar field as a toy example of [[classical field theory]] and [[perturbative quantum field theory]] is due to
it already exhibiting much of the core structure of [[field theory]]. For instance the general formulas for [[propagators]]
and the [[S-matrix]] of general [[local field theories]] are structurally those of the
scalar field, just with some more fairly evident [[representation theory|representation theoretic]] structure thrown in.



## Definition

### Free scalar field

We discuss here the [[free field|free]] [[scalar field]] on general [[spacetimes]],
hence the scalar field subject to the [[force]] of a [[background field]] of [[gravity]], but
not [[interaction|interacting]] with itself. This means that its [[local Lagrangian density]]
is [[quadratic form|quadratic]] in the fields and its first derivatives (def. \ref{LocalLagrangianOfFreeScalarField})
and its [[equation of motion]] is the [[Klein-Gordon equation]] (hence the [[wave equation]] in the case of
vanishing [[mass]]) (prop. \ref{FreeScalarFieldEOM} below).

The [[Poisson bracket]] on the [[covariant phase space]] of this system (prop. \ref{FreeScalarFieldEOM} below) turns out
to have as [[integral kernel]] the [[causal propagator]] of the [[Klein-Gordon operator]]
(i.e. the [[Green function]] whose [[support of a distribution|support]] is inside the [[light cone]]).
Accordingly, the other associated [[Green functions]] of the [[Klein-Gordon operator]]
(the "[[propagators]]", such as the [[Feynman propagator]]) govern the
[[perturbative quantum field theory]] of the scalar field (see at _[[S-matrix]]_ for more).

#### Covariant phase space

Recall that a _[[classical field theory|classical]] [[local field theory]]_ is for some prescribed class of [[manifolds]] $\Sigma$ of given [[dimension]] $p+1 \in \mathbb{N}$ interpreted as [[spacetimes]]/[[worldvolumes]]:

1. a choice of [[fiber bundle]] $E \to\Sigma$, called the _[[field bundle]]_;

1. a choice $L \in \Omega^{p+1,0}(J^\infty(E))$ of [[horizontal differential form]] of degree $p+1$ on the [[jet bundle]] of the field bundle, called the _[[local Lagrangian density]]_.


Given a [[classical field theory|classical]] [[local field theory]] defined by a [[local Lagrangian density]] $L \in \Omega^{p+1,0}(J^\infty(E))$, then

1. the [[configuration space]] is the [[smooth space|smooth]] [[space of sections]]   $\Gamma_X(E)$ of the [[field bundle]];

1. the [[equations of motion]] is the [[partial differential equation]] on elements $\phi \in \Gamma_X(E)$ given by

   $$
     (\delta_{EL} L)(j^\infty \phi) = 0
     \,,
   $$

   where

   1. $\delta_{EL} \;\colon\; \Omega^{n,0}(J^\infty_X(E)) \to \mathcal{F}^1(J^\infty_X(E))$ denotes the _[[Euler-Lagrange operator]]_

   1. $j^\infty \;\colon\; \Gamma_X(E) \longrightarrow \Gamma_X(J^\infty_X(E))$ denotes [[jet prolongation]].

1. The [[covariant phase space]] $(Sol_{\delta_{EL}L = 0}, d\theta)$ is the subspace $Sol_{\delta_{EL} L = 0} \subset \Gamma_X(E)$ of solutions to the [[equations of motion]], equipped with the canonical [[presymplectic form]].


##### On Minkowski spacetime

We discuss the [[covariant phase space]] of the [[free field|free]] scalar field on [[Minkowski spacetime]].



+-- {: .num_defn #LagrangianForFreeScalarFieldOnMinkowskiSpacetime}
###### Definition
**([[local Lagrangian density]] for [[free field|free]] [[scalar field]] on [[Minkowski spacetime]])**

For $p \in \mathbb{N}$, let [[spacetime]] $\Sigma \coloneqq \mathbb{R}^{p,1} = (\mathbb{R}^d, \eta)$ be [[Minkowski spacetime]] of [[dimension]] $p + 1$, where $\eta$ denotes the Minkowski [[metric tensor]] of [[signature of a quadratic form|signature]] $(-,+,\cdots, +)$. We write $\mathrm{dvol}_\Sigma \in \Omega^{p+1}(\Sigma)$ for the corresponding [[volume form]] and $\{x^\mu \colon \Sigma \to \mathbb{R}\}_{\mu = 0}^p$ for the canonical [[coordinate functions]].

Let the [[field bundle]] $E \to \Sigma$ be the [[trivial vector bundle|trivial]] [[real line bundle]] over $\Sigma$.

Then its [[jet bundle]] $J^\infty E$ has canonical coordinates

$$
  \{ \{x^\mu\}, \phi, \{\phi_{,\mu}\}, \{\phi_{,\mu \nu}\}, \cdots \}
  \,.
$$

In these coordinates, the [[local Lagrangian density]]

$$
  L \in \Omega^{p+1,0}(\Sigma)
$$

defining the [[free field|free]] [[scalar field]] of [[mass]] $m \in [0,\infty)$ on $\Sigma$ is

$$
  L
    \coloneqq
  \tfrac{1}{2}
  \left(
    \eta^{\mu \nu} \phi_{,\mu} \phi_{,\nu}
    +
    m^2 \phi^2
  \right)
  \mathrm{dvol}_\Sigma
  \,.
$$

=--



+-- {: .num_prop #FreeScalarFieldEOM}
###### Proposition
**([[covariant phase space]] of [[free field|free]] [[scalar field]])**

In the situation of def. \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}
for $\Phi : \Sigma \to \mathbb{R}$ the $\phi$-component of a [[section]] of the [[field bundle]], its [[equation of motion]] is the [[Klein-Gordon equation]]

$$
  \left(-\eta^{\mu \nu} \partial_\mu \partial_\nu + m^2 \right) \Phi = 0
  \,.
$$

Moreover, the induced [[pre-symplectic current]] $\omega \in \Omega^{p-1,2}(E)$ is, in local coordinates,

$$
  \omega
    =
  \left(g^{\mu \nu} d_V \phi_{,\mu} \wedge d_V \phi \right) \wedge \iota_{\partial_\nu} dvol_{\Sigma}
$$

and hence the induced [[symplectic form]] on the [[covariant phase space]] of the free scalar field
takes two [[smooth function]] $w_1,w_2 \in C^\infty(\Sigma)$, regarded as [[tangent vectors]] at zero to

$$
  \mathbf{\Omega}_{\Sigma_{p-1}}(w_1, w_2)
    \;=\;
    \int_{\Sigma_{p-1}}
    \left(
      (\partial_n w_1) w_2
      -
      w_1 \partial_n w_2
    \right)
    dvol_{\Sigma_{p-1}}
    \,,
$$

where $\Sigma_{p-1} \hookrightarrow \Sigma$ is any [[Cauchy surface]]
and where $n \in N \Sigma_{p-1}$ denotes its time-like normal vector field.

=--

+-- {: .proof}
###### Proof


We need to show that [[Euler-Lagrange operator]] $\delta_{EL} \colon \Omega^{p+1,0}(\Sigma) \to \Omega^{p+1,1}_S(\Sigma)$ takes the [[local Lagrangian density]] for the [[free field|free]] [[scalar field]] to

$$
  \delta_EL L
  \;=\;
  \left(
    \eta^{\mu \nu} \phi_{,\mu \nu}  + m^2 \phi
  \right)
  d_V \phi \wedge \mathrm{dvol}_\Sigma
  \,.
$$

First of all, the result of applying the [[variational bicomplex|vertical differential]] to the local Lagrangian density is

$$
  d_V L
    =
  \left(
    \eta^{\mu \nu} \phi_{,\mu} d_V \phi_{,\nu}
      +
    m^2 \phi d_V \phi
  \right)
  \wedge \mathrm{dvol}_\Sigma
  \,.
$$

By definition of the [[Euler-Lagrange operator]], in order to find $\mathrm{EL}$ and $\theta$, we need to exhibit this as the
sum of the form $(-) \wedge d_V \phi  - d_H \theta$.

The key to find $\theta$ is  to realize $d_V \phi_{,\nu}\wedge \mathrm{dvol}_\Sigma$ as a [[horizontal derivative]]. Since $d_H \phi = \phi_{,\mu} d x^\mu$ this is accomplished by

$$
  d_V \phi_{,\nu} \wedge \mathrm{dvol}_\Sigma
  =
  d_V d_H \phi \wedge \iota_{\partial_\nu} \mathrm{dvol}_\Sigma
$$

Hence we may set

$$
  \theta
    \coloneqq
  \eta^{\mu \nu} \phi_{,\mu} d_V \phi \wedge \iota_{\partial_\nu}
  \mathrm{dvol}_\Sigma
  \,,
$$

because with this we have

$$
  d_H \theta
  =
  \eta^{\mu \nu}
  \left(
    \phi_{,\mu \nu} d_V \phi
    -
    \eta^{\mu \nu} \phi_{,\mu} d_V \phi_{,\nu}
  \right) \wedge \mathrm{dvol}_\Sigma
  \,.
$$

In conclusion this yields the decomposition of the vertical differential of the Lagrangian density

$$
  d_V L
  =
  \underset{
    = \delta_{EL} L
  }{
  \underbrace{
    \left(
      \eta^{\mu \nu} \phi_{,\mu \nu}  + m^2 \phi
    \right)
    d_V \phi \wedge \mathrm{dvol}_\Sigma
  }
  }
  -
  d_H \theta
  \,,
$$

which shows that $\delta_{EL} L$ is as claimed, and that $\theta$ is a presymplectic potential current.
Hence the presymplectic current itself is

$$
  \begin{aligned}
    \omega &\coloneqq d_V \theta
    \\
    & =
    d_V \left( \eta^{\mu \nu} \phi_{,\mu} d_V \phi \wedge \iota_{\partial_\nu} \mathrm{dvol}_\Sigma \right)
    \\
    & =
    \left(\eta^{\mu \nu} d_V \phi_{,\mu} \wedge d_V \phi \right) \wedge \iota_{\partial_\nu} dvol_{\Sigma}
  \end{aligned}
  \,.
$$

For $\Sigma_p \hookrightarrow \Sigma$ a [[Cauchy surface]], the [[transgression]] of
this presymplectic current to the [[infinitesimal neighbourhood]] of $\Sigma$ is

$$
  \begin{aligned}
    \omega_{\Sigma_{p-1}}(w_1, w_2)
    & =
    \int_\Sigma
      \left(
        e^{\mu \nu} \mathbf{d} \partial_\mu \phi \wedge \mathbf{d} \phi
      \right)
      \iota_{\partial_\nu} dvol_\Sigma (\phi_1, \phi_2)
    \\
    & =
    \int_{\Sigma_{p-1}}
    \left(
      (\partial_n w_1) w_2
      -
      w_1 \partial_n w_2
    \right)
    dvol_{\Sigma_{p-1}}
  \end{aligned}
$$

=--


+-- {: .num_example #PoissonBracketsOverMinkowskiSpacetime}
###### Example
**([[Poisson brackets]] over [[Minkowski spacetime]])

Consider the covariant phase space over [[Minkowski spacetime]] of dimension $p+1$ as in def. \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime},
with [[pre-symplectic current]] according to prop. \ref{FreeScalarFieldEOM} given by

$$
  \omega
   =
  \eta^{\mu \nu} d_V \phi_{,\mu} \wedge d_V \phi \wedge \iota_{\partial_\mu} dvol_\Sigma
  \,
$$

The corresponding [[Poisson bracket Lie n-algebra|Poisson bracket Lie (p+1)-algebra]] has in degree 0
[[Hamiltonian forms]] such as

$$
  Q \coloneqq \phi \iota_{\partial_0} dvol_\Sigma \in \Omega^{p,0}(E)
$$

and

$$
  P \coloneqq \eta^{\mu \nu} \phi_{,\mu} \iota_{\partial_\nu} dvol_{\Sigma} \in \Omega^{p,0}(E)
  \,.
$$

The corresponding [[Hamiltonian vector fields]] are

$$
 v_P = \partial_{\phi_{,0}}
$$

and

$$
  v_Q = - \partial_{\phi}
  \,.
$$

Hence the corresponding bracket is

$$
  \{Q,P\} = \iota_{v_Q} \iota_{v_P} \omega = \iota_{\partial_0} dvol_\Sigma
  \,.
$$

More generally for $b_1, b_2 \in C^\infty_c(\Sigma)$ two [[bump functions]] then

$$
  \{ b_1 Q, b_2 P \} = \pm b_1 b_2 \iota_{\partial_0} dvol_\Sigma
  \,.
$$

Upon [[transgression]] to the [[Cauchy surface]] $\Sigma^t_{p} \coloneqq \{x \in  \Sigma \vert x^0 = t \}$ this yields the [[Poisson bracket]]

$$
  \left\{
    \int_{\Sigma_p} b_1(\vec x) \phi(t,\vec x) \iota_{\partial_0} dvol_\Sigma(x)
    d^p \vec x
    \;,\;
    \int_{\Sigma_p} b_2(\vec x) \partial_0 \phi(t,\vec x) \iota_{\partial_0} dvol_\Sigma(\vec x)
  \right\}
  \;=\;
  \int_{\Sigma_p} b_1(\vec x) b_2(\vec x) \iota_{\partial_0} dvol_\Sigma(\vec x)
  d^p \vec x
  \,.
$$

where now

$$
  \phi(x), \partial_0 \phi(x) : PhaseSpace(\Sigma_p^t) \to \mathbb{R}
$$

are the point-evaluation functions ([[functionals]]), which act on a field configuration $\Phi \in \Gamma_\Sigma(E) = C^\infty(\Sigma)$ as

$$
 \phi(x)(\Phi) \coloneqq \Phi(x)
 \phantom{AAAAAAAA}
 \partial_0 \phi(x) (\Phi) \coloneqq \partial_0 \Phi(x)
 \,.
$$

Notice that these point-evaluation functions themselves do not arise
as the transgression of elements in $\Omega^{p,0}(E)$, only their smearings such as $\int_{\Sigma_p} b_1 \phi dvol_{\Sigma_p}$ do.
Nevertheless we may express the above Poisson bracket conveniently via the [[integral kernel]]

$$
  \label{PoissonBracketOfScalarFieldPointEvaluationOnMinkowskiSpacetime}
  \{\phi(t,\vec x), \phi(t,\vec y) \}
  =
  \delta(\vec x - \vec y)
  \,.
$$


=--

More generally one may express the integral kernel for the Poisson bracket of evaluation functions for  different values of $t$.
Notice that for each time interval $[t_1, t_2]$ we have a [[Lagrangian correspondence]]

$$
  \array{
    && Trajectories([t_1,t_2])
    \\
    & {}^{\mathllap{ \Phi(-) \mapsto ( \Phi(t_1,-), \partial_0 \Phi(t_1,-) ) }}\swarrow
      &&
    \searrow^{\mathrlap{ \Phi(-) \mapsto ( \Phi(t_2,-), \partial_0 \Phi(t_2,-) ) }}
    \\
    PhaseSpace(\Sigma^{t_1}_p)
     && &&
    PhaseSpace(\Sigma^{t_2}_p)
    \\
    & {}_{\mathllap{\Omega^{t_1}}}\searrow && \swarrow_{\mathrlap{\Omega^{t_2}}}
    \\
    && \mathbf{\Omega}_{cl}^2
  }
  \,,
$$

where $Trajectories([t_1,t_2])$ is the space of solutions to the [[Klein-Gordon equation]]
on $[t_1,t_2] \times \mathbb{R}^p \subset \mathbb{R}^{p,1}$.





There is a unique function on $PhaseSpace(\Sigma^{t_1}_p)$ whose pullback to $Trajectories([t_1,t_2])$
is the evaluation function $\phi(x)$ for any $x^0 \in [t_1,t_2]$. By convenient abuse of notation,
we also call that function $\phi(x)$.


+-- {: .num_prop #IntegralKernelForPoissonBracketOfFreeScalarFieldOnMinkowskiSpacetime}
###### Proposition
**([[integral kernel]] for [[Poisson bracket]] on [[Minkowski spacetime]] is the [[causal propagator]])

The integral kernel on $\mathbb{R}^{p,1}$ for the Poisson bracket of the scalar field
over [[Minkowski spacetime]] (example \ref{PoissonBracketsOverMinkowskiSpacetime})
is the _[[causal propagator]]_

$$
  \Delta
    \;\in\;
  \mathcal{D}'(\Sigma \times \Sigma)
$$

(also known as the _[[Pauli-Jordan distribution]]_ or _[[Peierls bracket]]_)
on Minkowski spacetime:

$$
  \begin{aligned}
    \{ \phi(x), \phi(y) \}
    & =
    \Delta(x,y)
    \\
    & \coloneqq
    -i (2\pi)^{-p} \int \tfrac{1}{2 E(\vec k)}\left(
    e^{- i E(\vec k) (x-y)^0 - \vec k \cdot (\vec x - \vec y)}
    -
    e^{+ i E(\vec k) (x-y)^0 + \vec k \cdot (\vec x - \vec y)}
  \right) d^p \vec k
    \\
    & = 
   -i (2\pi)^{-p} \int \delta( k_\mu k^\mu + m^2 ) sgn( k_0 ) e^{ - i k_\mu (x-y)^\mu } d^{p+1} k
    \,.
  \end{aligned}
$$

=--

(e. g. [Scharf 01 (1.1.13)](#Scharf01))

+-- {: .proof}
###### Proof


By [[Fourier transform]] the general solution to the [[Klein-Gordon equation]] may be expressed in the form

$$
  \Phi(x)
    \;=\;
  (2\pi)^{-p} \int  Amp(k) e^{- i k_\mu x^\mu } \delta( k_\mu k^\mu + m^2 ) d^{p+1} k
  \,,
$$

where $Amp(k) \in \mathbb{C}$ is the _complex amplitude_ of the $k$th mode $(k \in \mathbb{R}^{p+1})$.

We may split this into the contributions with positive and those with negative [[energy]] $k_0$
by decomposing the integral over $k_0$ as

$$
  \begin{aligned}
    \Phi(x)
    & = \phantom{+}
    (2\pi)^{-p/2}
    \int_0^\infty  \int Amp(k_0, \vec k) e^{- i k_0 x^0 - i \vec k \cdot \vec x} \delta(- k_0^2 + \vec k + m^2) d^p \vec k \, d k_0
    \\
    & \phantom{=} +
    (2\pi)^{-p/2}
    \int_0^\infty  \int Amp(-k_0, \vec k) e^{+ i k_0 x^0 - i \vec k \cdot \vec x} \delta(-k_0^2 + \vec k^2 + m^2) d^p \vec k \, d k_0
    \,.
  \end{aligned}
$$

By [[changing integration variables]] via $k_0 = +\sqrt{ h }$ this yields

$$
  \begin{aligned}
    \Phi(x)
    & = \phantom{+}
    (2\pi)^{-p/2}
    \int_0^\infty  \int Amp(\sqrt{h}, \vec k) e^{- i \sqrt{h} x^0 - i \vec k \cdot \vec x} \delta(- h + \vec k + m^2) d^p \vec k \, \frac{d h}{2\sqrt{h}}
    \\
    & \phantom{=} +
    (2\pi)^{-p/2}
    \int_0^\infty  \int Amp(- \sqrt{h}, \vec k) e^{+ i \sqrt{h} x^0 - i \vec k \cdot \vec x} \delta(- h + \vec k^2 + m^2) d^p \vec k \, \frac{d h}{2 \sqrt{h}}
    \\
    & = \phantom{+}
    (2\pi)^{-p/2}
    \int Amp(E(\vec k), \vec k) e^{- i E(\vec k) x^0 - i \vec k \cdot \vec x} d^p \vec k
    \\
    & \phantom{=} +
    (2\pi)^{-p/2}
    \int Amp(-E(\vec k), \vec k) e^{+ i E(\vec k) x^0 - i \vec k \cdot \vec x} d^p \vec k
  \end{aligned}
$$

where we defined the _on-shell [[energy]]_

$$
  E(\vec k) \coloneqq + \sqrt{ \vec k^2 + m^2 }
  \,.
$$

It is convenient to also change variables $\vec k \mapsto - \vec k$ in the second integral. This yields

$$
  \begin{aligned}
    \Phi(x)
    &= \phantom{+}
      (2\pi)^{-p/2}
      \int Amp(E(\vec k), \vec k) e^{- i E(\vec k) x^0 - i \vec k \cdot \vec x} d^p \vec k
      \\
      & \phantom{=} +
      (-1)^p
      (2\pi)^{-p/2}
      \int Amp(-E(\vec k), \vec k) e^{+ i E(\vec k) x^0 + i \vec k \cdot \vec x} d^p \vec k
  \end{aligned}
    \,.
$$

Since $\Phi$ is real-valued, it follows that under [[complex conjugation]] $(-)^\ast$
the amplitudes are related by

$$
  Amp(E(\vec k), \vec k)^\ast = (-1)^p Amp(-E(\vec k), \vec k)
  \,.
$$

We abbreviate (cf. [Scharf 01 (1.1.18)](#Scharf01))

$$
  A(\vec k) \coloneqq E(\vec k) Amp(E(\vec k), \vec k)
  \,,
$$

where the prefactor just serves to make some of the following formulas come out conveniently.

With this the general solution to the Klein-Gordon equation is finally of the form

$$
  \label{FourierModeExpansionOfScalarFieldOnminkowskiSpacetime}
  \Phi(x)
  =
    (2\pi)^{-p/2}
    \int \frac{1}{\sqrt{2 E(\vec k)}}
      \left(
        A(\vec k) e^{- i E(\vec k) x^0 - i \vec k \cdot \vec x}
        +
        A(\vec k)^\ast e^{+ i E(\vec k) x^0 + i \vec k \cdot \vec x}
      \right)
    d^p \vec k
    \,.
$$

and hence its time derivative is

$$
  \partial_0 \Phi(x)
  =
    (2\pi)^{-p/2}
    \int -i \sqrt{E(k)/2}
      \left(
        A(\vec k) e^{- i E(\vec k) x^0 - i \vec k \cdot \vec x}
        -
        A(\vec k)^\ast e^{+ i E(\vec k) x^0 + i \vec k \cdot \vec x}
      \right)
    d^p \vec k
    \,.
$$

This allows to express the modes in terms of the value of the field and its time derivative at $t = 0$:

$$
  A(\vec k)
  =
   (2 \pi)^{-p/2}
   \int
     \left( \sqrt{E(k)/2}\Phi(0,\vec x) + i \frac{1}{2\sqrt{E(k)}} \partial_0 \Phi(0,\vec x)\right) \exp( i \vec k \cdot \vec x )
   d^p \vec x
   \,.
$$

As in example \ref{PoissonBracketsOverMinkowskiSpacetime} we denote the corresponding evaluation functional

$$
  a(\vec k) \;\colon\; C^\infty(\Sigma) \longrightarrow \mathbb{C}
$$

by the corresponding lower case symbol:

$$
  a(\vec k)
   \;\coloneqq\;
   (2 \pi)^{-p/2}
   \int
     \left( \sqrt{E(k)/2}\phi(\vec x) + i \frac{1}{\sqrt{2 E(k)}} \partial_0 \phi(\vec x)\right) \exp( i \vec k \cdot \vec x )
   d^p \vec x
   \,.
$$

With the Poisson bracket kernel $\{\phi(\vec x), \phi(\vec y)\} = \delta(\vec x - \vec y)$ from example \ref{PoissonBracketsOverMinkowskiSpacetime} (eq:PoissonBracketOfScalarFieldPointEvaluationOnMinkowskiSpacetime),
it follow that the  (integral kernel for the) Poisson bracket of these mode functionals is
that of the [[canonical commutation relations]]:

$$
  \begin{aligned}
    \label{CanonicalPoissonCommutationOfModesOfFreeScalarFieldOnMinkowskiSpacetime}
    \{ a(\vec k_1), a(\vec k_2)^\ast  \}
    & =
    -i
    (2\pi)^{-p}
    \int \delta(\vec x_1 - \vec x_2) e^{i  ( \vec k_1 \cdot \vec x_1 - \vec k_2 \cdot \vec x_2) } d \vec x_1 d\vec x_2
    \\
    & =
    -i
    (2\pi)^{-p}
    \int e^{i (\vec k_1 - \vec k_2) \cdot \vec x } d \vec x
    & =
    \\
    & =  -i \delta(\vec k_1 - \vec k_2)
    \,,
  \end{aligned}
$$

where in the last step we used the [[Fourier transform]] representation of the [[delta distribution]] ([this prop.](Dirac+distribution#FourierTransform)).

In order to finally compute $\{\phi(x), \phi(y)\}$, it is convenient to break this up into two contributions:
Write

$$
  \phi^{(+)}(x)
  \;\coloneqq\;
    (2\pi)^{-p/2}
    \int \frac{1}{\sqrt{2 E(\vec k)}}
        a(\vec k)^\ast e^{+ i E(\vec k) x^0 + i \vec k \cdot \vec x}
    d^p \vec k
  \phantom{AAAA}
  \phi^{(-)}(x)
  \;\coloneqq\;
    (2\pi)^{-p/2}
    \int \frac{1}{\sqrt{2 E(\vec k)}}
        a(\vec k) e^{- i E(\vec k) x^0 - i \vec k \cdot \vec x}
    d^p \vec k
$$

for the positive and negative energy contributions from the Fourier expansion in (eq:FourierModeExpansionOfScalarFieldOnminkowskiSpacetime), so that

$$
  \phi(x) = \phi^{(-)}(x)  + \phi^{(+)}(x)
  \,.
$$

Using the [[canonical commutation relation]] of the mode functions (eq:CanonicalPoissonCommutationOfModesOfFreeScalarFieldOnMinkowskiSpacetime), we find

$$
  \label{2PointFunctionFreeScalarFieldOnMinkowski}
  \begin{aligned}
    -i \omega(x,y)
     & \coloneqq
     \{ \phi^{(-)}(x), \phi^{(+)}(y) \}
    \\
    &=
    -i (2\pi)^{-p} \int \tfrac{1}{2 E(\vec k)} e^{- i E(\vec k) (x-y)^0 - \vec k \cdot (\vec x - \vec y)} d^{p} \vec k
    \\
    & =
    -i (2\pi)^{-p} \int \delta( k_\mu k^\mu + m^2 ) \Theta( k_0 ) e^{ - i k_\mu (x-y)^\mu } d^{p+1} k
    \,,
  \end{aligned}
$$

where in the last line we again applied [[change of integration variables]].
This $\omega$ is known as the _[[2-point function]]_ or _[[Hadamard propagator]]_ on Minkowski spacetime (see def. \ref{2PointFunctionOfScalarFieldOnMinkowskiSpacetime} below).

Similarly

$$
  \begin{aligned}
  \{ \phi^{(+)}(x), \phi^{(-)}(y) \}
  & =
  + i (2\pi)^{-p} \int \tfrac{1}{2 E(\vec k)} e^{i E(\vec k) (x-y)^0 + \vec k \cdot (\vec x - \vec y)} d^{p} \vec k
  \\
  & =
  + i (2\pi)^{-p} \int \delta( k_\mu k^\mu + m^2 ) \Theta( -k_0 ) e^{ - i k_\mu (x-y)^\mu } d^{p+1} k
  \\
  \end{aligned}
  \,.
$$

In particular this says that

$$
  \{ \phi^{(+)}(x), \phi^{(-)}(y) \}
  =
  - \omega(y,x)
  \coloneqq
  -
  \{ \phi^{(-)}(y), \phi^{(+)}(x) \}
  \,.
$$


With this we finally obtain the expression for the [[causal propagator]] as the skew-symmetrization
of the [[2-point function]]:

$$
  \begin{aligned}
  \{
    \phi(x),
    \phi(y)
  \}
  & =
  \{ \phi^{(-)}(x), \phi^{(+)}(y) \}
  +
  \{\phi^{(+)}(x), \phi^{(-)}(y)\}
  \\
  & =
  \omega(x,y) - \omega(y,x)
  \\
  & =
  -i (2\pi)^{-p} \int \tfrac{1}{2 E(\vec k)}\left(
    e^{- i E(\vec k) (x-y)^0 - \vec k \cdot (\vec x - \vec y)}
    -
    e^{+ i E(\vec k) (x-y)^0 + \vec k \cdot (\vec x - \vec y)}
  \right) d^p \vec k
  \\
  & =
  -i (2\pi)^{-p} \int \delta( k_\mu k^\mu + m^2 ) sgn( k_0 ) e^{ - i k_\mu (x-y)^\mu } d^{p+1} k
 \,.
  \end{aligned}
$$

=--

We record the 2-point function that appeared in this computation:

+-- {: .num_defn #2PointFunctionOfScalarFieldOnMinkowskiSpacetime}
###### Definition
**([[2-point function]] of [[scalar field]] on [[Minkowski spacetime]])**

The _[[2-point function]]_ or _[[Hadamard propagator]]_ of the scalar field on [[Minkowski spacetime]]

$$
  \omega \;\in\; \mathcal{D}'(\Sigma \times \Sigma)
$$

is  (eq:2PointFunctionFreeScalarFieldOnMinkowski)

$$
  \omega(x,y)
    \;\coloneqq\;
  i \{\phi^{(-)}(x), \phi^{(+)}(y)\}
  \,.
$$

=--





##### On general spacetimes

We discuss the [[covariant phase space]] of the [[free field|free]] scalar field on general [[spacetimes]].


+-- {: .num_defn #LocalLagrangianOfFreeScalarField}
###### Definition
**([[local Lagrangian density]] for [[free field|free]] [[scalar field]] on general [[spacetime]])**

As a [[classical field theory|classical]] [[local field theory|local field]] the _relativistic [[free field|free]] scalar field_ in [[dimension]] $p+1 \in \mathbb{N}$ of [[mass]] $m \in [0,\infty)$ is

* for each [[globally hyperbolic spacetime|globally hyperbolic]] [[orientation|oriented]] and [[time orientation|time-oriented]] [[spacetime]] $(\Sigma,e)$ ($\Sigma$ a [[smooth manifold]], $e$ a [[pseudo-orthogonal structure]]/[[vielbein]]  inducing a [[pseudo-Riemannian metric]] $g$)

1. the [[field bundle]] given by the [[trivial line bundle]] $X \times k \overset{pr_1}{\to} X$ over $X$;

1. the [[local Lagrangian density]] $L \in \Omega^{p+1,0}(J^\infty_X(X \times k))$ (a [[horizontal differential form]] on the [[jet bundle]] of the [[trivial line bundle]] over $X$) given by

   $$
     L \;\coloneqq\; \left( \vert \nabla \phi\vert^2 + m^2 \phi^2\right) dvol_ \Sigma
   $$

   where

   1. $\vert \nabla \phi\vert^2$ denotes the [[norm]] square of the first order jets with respect to the given [[metric]] $g$, hence in a local [[coordinate chart]] $J^\infty(E\vert_U) \coloneqq \left\{ \{x^\mu\}, \phi, \{\phi_{,\mu} \cdots\} \right\}$ of $J^\infty(X \times k)$ the function

      $$
        \vert \nabla \phi\vert^2\vert_{J^{\infty}(E\vert_U)}
          \;=\;
        g^{\mu \nu} \phi_{,\mu} \phi_{,\nu}
      $$

   1. $dvol$ denotes the [[volume form]] of $(\Sigma,e)$, canonically regarded as a [[horizontal differential form]] on $J^\infty(\Sigma \times k)$.

=--


The analogue of prop. \ref{IntegralKernelForPoissonBracketOfFreeScalarFieldOnMinkowskiSpacetime}
holds true for general spacetimes:

+-- {: .num_prop #FreeScalarFieldGreenFunctions}
###### Proposition
**([[advanced propagator]] and [[retarded propagator]])**

On a [[time orientation|time oriented]] [[globally hyperbolic spacetime]] the [[Klein-Gordon operator]] admits unique [[advanced propagator]] and [[retarded propagator]].

=--

(e.g. [B&#228;r-Ginoux-Pf&#228;ffle 07, corollary 3.4.3](BaerGinouxPfaeffle07))



+-- {: .num_prop }
###### Proposition

The induced [[Poisson bracket]] on the [[covariant phase space]] of the free scalar field (def. \ref{LocalLagrangianOfFreeScalarField}) is given by the [[Peierls bracket]]. (...)


=--

By [this prop.](Peierls+bracket#PeierlsPoissonBracket) (e.g. [Khavkine 14](Peierls+bracket#Khavkine14), [Collini 16, lemma 21](#Collini16)). See also [Fredenhagen-Rejzner 15, 3.3 Example](locally+covariant+perturbative+quantum+field+theory#FredenhagenRejzner15)


### Interacting scalar field

We discuss [[perturbative quantum field theory]] of the free scalar field perturbed by an [[interaction]] term
via [[locally covariant perturbative algebraic quantum field theory]].

#### On Minkowski spacetime

We disscuss the interacting scalar field on [[Minkowski spacetime]] via [[causal perturbation theory]].

By the discussion at _[[S-matrix]]_ we need to determine the [[Feynman propagator]], which
is a linear combination of the [[2-point function]] with the [[advanced propagator]]:

+-- {: .num_defn }
###### Definition

[[advanced propagator]]

$$
  \Delta_A(x.y) \coloneqq \theta((x-y)^0) \Delta(x,y)
$$

[[retarded propagator]]

$$
  \Delta_R(x.y) \coloneqq \theta((y-x)^0) \Delta(x,y)
$$




=--


## Related concepts

* [[wave equation]], [[Klein-Gordon equation]]

* [[causal propagator]], [[Feynman propagator]]

* [[Wick algebra]]

## References

For instance

* {#Scharf01} [[Günter Scharf]], section 1.1 of _[[Quantum Gauge Theories -- A True Ghost Story]], Wiley 2001

Most of the literatur on [[causal perturbation theory]] and [[perturbative AQFT]] focuses on the scalar field, for ease of exposition.
See the references there.

The standard [[perturbative quantum field theory]] (made rigorous via [[causal perturbation theory]]) of the [[interaction|interacting]] scalar field is shown to be [[Fedosov deformation quantization]] of the corresponding [[covariant phase space]] in

* {#Collini16} [[Giovanni Collini]], section 2.2 of _Fedosov Quantization and Perturbative Quantum Field Theory_ ([arXiv:1603.09626](https://arxiv.org/abs/1603.09626))


For references on the construction of [[perturbative quantum field theory|perturbative]] scalar field theory in [[causal perturbation theory]] see at _[[locally covariant perturbative quantum field theory]]_.

Discussion of scalar fields in [[cosmology]] includes

* J.W. van Holten, _On single scalar field cosmology_ ([arXiv:1301.1174](http://arxiv.org/abs/1301.1174))




[[!redirects scalar field]]
[[!redirects scalar fields]]

[[!redirects real scalar field]]
[[!redirects reak scalar fields]]


[[!redirects complex scalar field]]
[[!redirects complex scalar fields]]

[[!redirects scalar field theory]]
[[!redirects scalar field theories]]

[[!redirects scalar particle]]
[[!redirects scalar particles]]
