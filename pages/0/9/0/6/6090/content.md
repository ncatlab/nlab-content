
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Qunantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Functorial Quantum Field Theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[quantum field theory]] a _[[scattering amplitude]]_ or _scattering matrix_  or _S-matrix_ encodes the [[probability amplitudes]] for scatterings processes of [[particles]] off each other.


Every [[perturbative quantum field theory]] has an S-matrix, usually thought of as a [[perturbation series]] over [[Feynman diagrams]] extracted from the [[action functional]].  The rigorous construction of this as an [[operator-valued distribution]] is the content of _[[causal perturbation theory]]_.

But there are also S-matrices not arising from a local field theory, for instance the [[string scattering amplitudes]].

The perception of the relevance of the S-matrix for the foundations of quantum field theory has a convoluted (and ongoing) history, see [below](#History).


## Details
 {#Formalization}


### In quantum mechanics
 {#InQuantumMechanics}

In [[quantum mechanics]], let $\mathcal{H}$ be some [[Hilbert space]] and let

$$
  H = H_{free} + V
$$

be Hermitian operator, thought of as a [[Hamiltonian]], decomposed as the [[sum]] of a free part ([[kinetic energy]]) and an interaction part ([[potential energy]]).

For example for a  [[non-relativistic particle]] of [[mass]] $m$ propagating on the [[line]] subject to a [[potential energy]] $V_{pot} \colon \mathbb{R} \to \mathbb{R}$, then $\mathcal{H} = L^2(X)$ is the Hilbert space space of [[square integrable functions]] and

$$
  H
   =
  \underset{H_{free}}{\underbrace{\tfrac{- \hbar^2}{2m} \frac{\partial^2}{\partial^2 x}}}
    +
  V
  \,,
$$

where $V = V_{pot}(x)$ is the operator of multiplying square integrable functions with the given potential energy function.

Now for

$$
  \array{
    \mathbb{R} &\overset{\vert \psi (-)\rangle }{\longrightarrow}& \mathcal{H}
   \\
   t &\mapsto& \vert \psi(t) \rangle
  }
$$

a one-parameter family of [[quantum states]], the [[Schrödinger equation]] for this state reads

$$
  \frac{d}{d t} \vert \psi(t) \rangle
  \;=\;
  \tfrac{1}{i \hbar} H \vert \psi\rangle
  \,.
$$

It is easy to solve this [[differential equation]] formally via its [[Green function]]: for $\vert \psi \rangle \in \mathcal{H}$ any state, then the unique solution $\vert \psi(-) \rangle$ to the Schr&#246;dinger equation subject to $\vert \psi(0) \rangle = \vert \psi \rangle$ is

$$
  \vert \psi(t)\rangle_S \coloneqq \exp( \tfrac{t}{i \hbar} H ) \vert \psi \rangle
  \,.
$$

(One says that this is the solution "in the [[Schrödinger picture]]", whence the subscript.)

However, if $H$ is sufficiently complicated, it may still be very hard to extract from this expression a more explicit formula for $\vert \psi(t) \rangle$, such as, in the example of the free particle on the line, its expression as a function ("[[wave function]]") of $x$ and $t$.

But assume that the analogous expression for $H_{free}$ alone is well understood, hence that the operator

$$
  U_{S,free}(t_1, t_2) \coloneqq \exp\left({\tfrac{t_2 - t_1}{i \hbar} H_{free}}\right)
$$

is sufficiently well understood. The "[[interaction picture]]" is a way to decompose the Schr&#246;dinger equation such that its dependence on $V$ gets separated from its dependence on $H_{free}$ in a way that admits to treat $H_{int}$ in [[perturbation theory]].

Namely define analogously

\[
  \label{StateInTheInteractionPicture}
  \begin{aligned}
    \vert \psi(t)\rangle_I
     &\coloneqq
     \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right) \vert \psi(t)\rangle_S
    \\
    & = \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right)
        \exp\left({ \tfrac{+ t}{i \hbar} H} \right)\vert \psi \rangle
    \\
    & = \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right)
        \exp\left({\tfrac{t}{i \hbar} H_{free} + \tfrac{t}{i \hbar} V} \right)\vert \psi \rangle   \end{aligned}
  \,.
\]

This is called the solution of the Schr&#246;dinger equation "in the [[interaction picture]]", whence the subscript. Its definition may be read as the result of propagating the actual solution $\vert \psi(-)\rangle_S$ at time $t$ back to time $t = 0$, but using just the free Hamiltonian, hence with "the interaction switched off".

Notice that if the operator $V$ were to commute with $H_{free}$ (which it does not in all relevant examples) then we would simply have $\vert \psi(t)\rangle_I = \exp( \tfrac{t}{i \hbar } V ) \vert \psi\rangle$, hence then the solution (eq:StateInTheInteractionPicture) in the interaction picture would be the result of "propagating" the initial conditions using _only_ the interaction. Now since $V$ may not be assumed to commute with $H_{free}$, the actual form of $\vert \psi(-) \rangle_{I}$ is more complicated. But _infinitesimally_ it remains true that $\vert \psi(-)\rangle_I$ is propagated this way, not by the plain operator $V$, though, but by $V$ viewed in the [[Heisenberg picture]] of the free theory. This is the content of the differential equation (eq:DifferentialEquationInInteractionPicture) below.

But first notice that this will indeed be useful: If an explicit expression for the "state in the [[interaction picture]]" (eq:StateInTheInteractionPicture) is known, then the assumption that also the operator $\exp\left({\tfrac{t}{i \hbar} H_{free}}\right)$ is sufficiently well understood implies that the actual solution

$$
  \vert \psi(t) \rangle_S = \exp\left({\tfrac{t}{i \hbar} H_{free}}\right) \vert \psi(t) \rangle_I
$$

is under control. Hence the question now is how to find $\vert \psi(-)\rangle_I$ given its value at some time $t$. (It is conventional to consider this for $t \to \pm \infty$, see (eq:SMatrixInQuantumMechanics) below.)

Now it is clear from the construction and using the [[product law]] for [[differentiation]], that $\vert \psi(-)\rangle_S$ satisfies the following [[differential equation]]:

\[
  \label{DifferentialEquationInInteractionPicture}
  \frac{d}{d t} \vert \psi(t) \rangle
  \;=\;
  V_I(t) \vert \psi(t)\rangle_I
  \,,
\]

where

$$
  V_I(t)
    \coloneqq
  \exp\left( -\tfrac{t}{i \hbar} H_{free} \right)
    V
  \exp\left( +\tfrac{t}{i \hbar} H_{free} \right)
$$

is known as the [[interaction]] term $V$ "viewed in the interaction picture". But in fact this is just $V$ "viewed in the [[Heisenberg picture]]", but for the _free_ theory. By our running assumption that the free theory is well understood, also $V_I(t)$ is well understood, and hence all that remains now is to find a sufficiently concrete solution to equation (eq:DifferentialEquationInInteractionPicture). This is the heart of working in the interaction picture.

Solutions to equations of the "[[parallel transport]]"-type such as (eq:DifferentialEquationInInteractionPicture) are given by [[time-ordered product|time-ordering]] of Heisenberg picture operators, denoted $T$, applied to the naive exponential solution as above. This is known as the _[[Dyson formula]]_:

$$
  \vert \psi(t)\rangle_I
  \;=\;
  T\left(
    \exp\left(
      \int_{t_0}^t
        V_I(t)
        \tfrac{d t}{i \hbar}
    \right)
  \right)
  \vert \psi(t_0)\rangle
  \,.
$$

Here [[time-ordered product|time-ordering]] means

$$
  T( V_I(t_1) V_I(t_2) )
  \;\coloneqq\;
  \left\{
    \array{
      V_I(t_1) V_I(t_2) &\vert& t_1 \geq t_2
      \\
      V_I(t_2) V_I(t_1) &\vert& t_2 \geq t_2
    }
  \right.
  \,.
$$

(This is abuse of notation: Strictly speaking time ordering acts on the [[tensor algebra]] spanned by the $\{V_I(t)\}_{t \in \mathbb{R}}$ and has to be _folllowed_ by taking tensor products to actual products. )

In applications to [[scattering]] processes one is interest in prescribing the [[quantum state]]/[[wave function]] far in the past, hence for $t \to - \infty$, and computing its form far in the future, hence for $t \to \infty$.

The operator that sends such "asymptotic ingoing-states" $\vert \psi(-\infty) \rangle_I$ to "asymptic outgoing states" $\vert \psi(+ \infty) \rangle_I$ is hence the [[limit of a sequence|limit]]

\[
  \label{SMatrixInQuantumMechanics}
  S
  \;\coloneqq\;
  \underset{t \to \infty}{\lim}
  T\left(
    \exp\left(
      \int_{-t}^t
        V_I(t)
        \tfrac{d t}{i \hbar}
    \right)
  \right)
  \,.
\]

This limit (if it exists) is called the _scattering matrix_ or _S-matrix_, for short.


### In perturbative quantum field theory


In [[perturbative quantum field theory]] the broad structure of the interaction picture in quantum mechanics ([above](#InQuantumMechanics)) remains a very good guide, but various technical details have to be generalized with due care:

1. The algebra of operators in the [[Heisenberg picture]] of the free theory becomes the _[[Wick algebra]]_ of the [[free field theory]] (taking into account "normal ordering" of field operators) defined on _[[microcausal functionals]]_ built from [[operator-valued distributions]] with constraints on their [[wave front set]].

1. The [[time-ordered products]] in the [[Dyson formula]] have to be refined to [[causal locality|causally ordered]] products and the resulting product at coincident points has to be defined by [[point-extension of distributions]] -- the freedom in making this choice is the [[renormalization]] freedom ("conter-terms").

1. The sharp interaction cutoff in the [[Dyson formula]] that is hidden in the integration over $[t_0,t]$ has to be smoothed out by [[adiabatic switching]] of the interaction (making the whole S-matrix an [[operator-valued distribution]]).

Together these three point are taken care of by the axiomatization of the "[[adiabatic switching|adiabatically switched]] [[S-matrix]]" according to **[[causal perturbation theory]]**.


The analogue of the limit $t \to \infty$ in the construction of the [[S-matrix]] (now: [[adiabatic limit]]) in general does not exist in field theory ("infrared divergencies"). But in fact it need not be taken: The field algebra in a bounded region of [[spacetime]] may be computed with any adiabatic switching that is constant on this region. Moreover, the algebras assigned to regions of spacetime this way satisfy [[causal locality]] by the causal ordering in the construction of the S-matrix. Therefore, even without taking the adiabtic limit in [[causal perturbation theory]] one obtains a field theory in the form of a _[[local net of observables]]_. This is the topic of **[[locally covariant perturbative quantum field theory]]**.


$\,$

> under construction


#### Preliminaries


In all of the following, let

$$
  d \in \mathbb{N}
$$

the [[spacetime]] [[dimension]].

Write

$$
  \mathbb{R}^{d-1,1} \coloneqq (\mathbb{R}^{d}, \eta)
$$

for [[Minkowski spacetime]] of dimension $d$, hence for the [[pseudo-Riemannian manifold]] whose underlying
[[smooth manifold]] is the [[Cartesian space]] $\mathbb{R}^d$ and whose [[metric tensor]] is

$$
  \eta = - d x^0 \otimes d x^0 + d x^1 \otimes d x^1 + \cdots + d x^{d-1} \otimes d x^{d-1}
 \,,
$$

where $x^\mu \;\colon\; \mathbb{R}^d \longrightarrow \mathbb{R}$ with $\mu \in \{0, \cdots, d-1\}$ denote the canonical [[coordinate]] functions.

For $x \in \mathbb{R}^{d-1,1}$ a point in spacetime, we write


For $x \in \mathbb{R}^{d-1,1}$ a point in spacetime, we write

$$
  V^+(x), V^-(x) \subset \mathbb{R}^{d-1,1}
$$

for its [[open future cone]] and [[open past cone]], respectively, and

$$
  \overline{V}^+(x), \overline{V}^-(x) \subset \mathbb{R}^{d-1,1}
$$

for the corresponding closed cones.

For $S \subset \mathbb{R}^{d-1,1}$ a [[subset]] we write

$$
  \overline{V}^\pm(S)
  \;\coloneqq\;
  \underset{x \in S}{\cup} \overline{V}^{\pm}(x)
$$

for the union of the future/past closed cones of all its points.


Consider the [[relation]] on the set $P(\mathbb{R}^{d})$ of [[subsets]] of spacetime given by

$$
  \begin{aligned}
    (S_1 \geq S_2)
    & \coloneqq
    S_1 \cap \overline{V}^-(S_2) = \emptyset
    \\
    \Leftrightarrow & S_2 \cap \overline{V}^+(S_1) = \emptyset
   \end{aligned}
   \,.
$$



If $S_1 \geq S_2$ and $S_2 \geq S_1$ we say that the two subsets are _[[spacelike]] separated_.



#### The axioms

Write $\Sigma \coloneqq \mathbb{R}^{d-1,1}$.

Let $E \to \Sigma$ be a [[field bundle]], write $\Gamma_\Sigma(E)$ for its space of [[smooth sections]].

+-- {: .num_defn #CompactlySupportedPolynomialLocalDensities}
###### Definition
**(compactly supported polynomial local densities)**

Write

$$
  \Omega_{poly}^{h,v}(E)
$$

for the space of differential forms on the [[jet bundle]] of $E$ which locally are [[polynomials]]
in the field variables.

$$
  \mathcal{F}_{loc}
    \; \subset \;
  C^\infty_c(\Sigma) \underset{\Omega_{poly}^{0,0}(E)}{\otimes} \Omega_{poly}^{d,0}(E)
$$

for the subspace of [[horizontal differential forms]] of degree $d$ on the [[jet bundle]] ([[local Lagrangian densities]])
of those which are [[compact support|compactly supported]] with respect to $\Sigma$ and [[polynomial]] with respect to the 
field variables.

Every $L \in \mathcal{F}_{loc}$ induces a functional

$$
   \Gamma_\Sigma(E) \longrightarrow \mathbb{R}
$$

by [[integration of differential forms|integration]] of the [[pullback of differential forms|pullback]]
of $L$ along the [[jet prolongation]] of a given [[section]]:

$$
  \phi \mapsto \int_{\Sigma} j^\infty(\phi)^\ast L 
  \,.
$$

These functionals happen to be [[microcausal functional|microcausal]], so that there is an inclusion

$$
  \mathcal{F}_{loc} \hookrightarrow \mathcal{F}_{mc}
$$

into the space of [[microcausal functionals]]. (See [this example](microcausal+functional#CompactlySupportedPolynomialLocalDensities) at _[[microcausal functional]]_).

=--



By construction, an element of $\mathcal{F}_{loc}$ may be presented as

$$
  g_{sw} L_{int} + \underset{n}{\sum} j_{sw,n} J_n
$$

where $L_{int}, J_n \in \Omega_{poly}^{d,0}(E)$ are polynomial local densities, to be regarded
as [[interaction]] [[Lagrangian density]] and [[source field]], respectively, and where
$g_{sw}, j_{sw,n} \in C^\infty_c(\Sigma)$ are [[compact support|compactly supported]] [[smooth functions]]
(a [[bump functions]]) on spacetime $\Sigma$, to be regarded as [[adiabatic switching]] functions.




Let $\mathcal{W}$ be a [[Wick algebra]] on $\mathbb{R}^{d-1,1}$ 
on $\Gamma(E)$), equipped with an [[action]]

$$
  \rho \;\colon\; \mathbb{R}^d \times \mathcal{W} \longrightarrow \mathcal{W}
$$

of the [[translation group]], encoding the quantization of [[free fields]].


+-- {: .num_defn #PerturbativeSMatrixOnMinkowskiSpacetime}
###### Definition
**(perturbative S-matrix on Minkowski spacetime)**

A _perturbative scattering matrix for fields $E$_, is a [[function]]

$$
  S
    \;\colon\;
  \mathcal{F}_{loc} \longrightarrow \mathcal{W}[ [ g/\hbar ] ]
$$

on compactly supported polynomial local densities (def. \ref{CompactlySupportedPolynomialLocalDensities}) 
with values in the algebra of [[formal power series]] in a formal variable $g/\hbar$ with [[coefficients]]
in the given [[Wick algebra]],
such that the following conditions hold for fixed $L_{int}, \{ J_n\}_{n = 1}^N$:

1. (perturbation)

   There exist [[distributions]] ([[multilinear map|multi-]] [[linear continuous functionals]]) of the form

   $$
     T^k \;\colon\; C^\infty_c(\Sigma)^{\otimes^{k(N+1)}} \longrightarrow \mathcal{W}[ [ g/\hbar ] ]
   $$

   for $k \in \mathbb{N}$, called the $k$-ary [[time-ordered products]], such that:
   
   1. The unary time-ordered product is the image of the given local functional in the [[Wick algebra]] $\mathcal{W} = (\mathcal{F}_{mc}, \star)$ under the inclusion $\mathcal{F}_{loc} \hookrightarrow \mathcal{F}_{mc}$ form def. \ref{CompactlySupportedPolynomialLocalDensities}:
   
      $T^1(g_{sw}L_{int},j_{sw}J) = :g_{sw}L_{int}: + :j_{sw}J:$
      
   1. The S-matrix is the [[exponential]] of the time-ordered products:

      $$ 
        S( g_{sw} L_{int} )
        \;=\;
        \underoverset{k = 0}{\infty}{\sum} \tfrac{1}{k!}
        \left(\tfrac{-1}{i \hbar}\right)^k
        \langle    T^k, (g_{sw}L_{int}, \cdots, g_{sw} L_{int}, j_{sw,1}J_1, \cdots , j_{sw,1} J_1, \cdots)   \rangle
      $$

1. (normalization)

   $$
     S(0) = 1
   $$

1. (unitarity)

   $$
     S(-)^\ast = S(-)^{-1}
   $$

1. (translation invariance)

1. (causal additivity)

   $$
     \left( supp(J_1) \geq supp(J_2) \right)
     \;\; \Rightarrow \;\;
     S(g_{sw}L_{int} + J_1 + J_2)
     =
     S(g_{sw}L_{int} + J_1) S(g_{sw}L_{int})^{-1} S(g_{sw}L_{int} + J_2)
     \,.
   $$

=--

For fixed $L_{int}, J_n$ this is [Epstein-Glaser 73 (1)](#EpsteinGlaser73) (in view of lemma \ref{CausalLocalityOfThePerturbativeSMatrix} below).

+-- {: .num_remark}
###### Remark

In def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime} $g/\hbar$ has the interpretation of the
[[coupling constant]] divided by [[Planck's constant]]. One obtains a [[formal power series]]
with the expected non-negative powers of $\hbar$ after passing to the [[interacting field algebra]]
induced by the S-matrix.

The local density $g_{sw}L_{int}$ has the interpretation 
[[interaction]] [[Lagrangian density]] $L_{int}$ [[adiabatic switching|adiabatically switched]] by a compactly supported
function $g_{sw}$,  and $J$ has the interpretation of a [[source field]]. 

=--

#### Causal locality

+-- {: .num_defn #GeneratingFunctionsForCorrelationFunctions}
###### Definition
**([[generating functions]] for [[correlation functions]])**

For $S$ a perturbative S-matrix as in def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime},
its _[[generating function]] for [[correlation functions]]_ is

$$
  V(g_{sw}L_{int}, J)
    \;\coloneqq\;
  S(g_{sw}L_{int})^{-1} S(g_{sw}L_{int} + J)
  \,.
$$

=--


+-- {: .num_lemma #CausalLocalityOfThePerturbativeSMatrix}
###### Lemma
**(causal locality of the perturbative S-matrix)**

Let $S$ be a perturbative S-matrix according to def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}
with $V$ its generating function for correlation functions
according to def. \ref{GeneratingFunctionsForCorrelationFunctions}. 

1. The following conditions are equivalent for all $L, J_1, J_2 \in \mathcal{F}_{loc}$:

   1. $V(L, J_1 + J_2) = V(L, J_1) V(L, J_2)$

   1. $V(L + J_1 , J_2) = V(L, J_2)$

   1. $S(L + J_1 + J_2) = S(L, J_1) S(L)^{-1} S(L + J_2)$

   Hence causal additivity in def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}
implies that all these conditions hold if $supp(J_1) \geq supp(J_2)$.


1. If $supp(L_1) \geq supp(L_2)$ and $supp(L_2) \geq supp(L_1)$ then


   $$
     S(L_1) S(L_2) = S(L_2) S(L_1)
     \,.
   $$

1. If $L_1\vert_{O} = L_2\vert_{O}$ on a [[causally closed subset]] $O \subset \mathbb{R}^{d-1,1}$
then there exists an invertible $K \in \mathcal{W}[ [ g/\hbar] ]$ such that for all $J$ with $supp(J) \subset O$

   $$
     V(L_2, J) = K^{-1} V(L_1, J) K
     \,.
   $$

=--

+-- {: .proof}
###### Proof

The equivalence of the three conditions in the first statement is immediate from the definitions:

Expanding out the definition of $V$, the first expression is equivalent to

$$
  S(L)^{-1} S(L + J_1 + J_2) 
    = 
  S(L)^{-1} S(L +  J_1 ) S(L)^{-1} S(L + J_2)
  \,.
$$

Multiplying both sides of this equation by $S(L)$, shows that it is equivalent to the third clause.

Multiplying once more with $S(L + J_1)^{-1}$ this third equation is seen to be equivalent to

$$
  S(L + J_1)^{-1} S(L + J_1 + J_2) = S(L)^{-1} S(L + J_2)
$$

which is equivalently the second clause, by definition of $V$.

Now setting $L = 0$ and $J_1 = L_1$ and $J_2 = L_2$ in the third clause it
reduces to 

$$
  \left(
    supp(L_1) \geq supp(L_2)
  \right)
   \;\Rightarrow\;
  S(L_1 + L_2)
  =
  S(L_1)S(L_2)
  \,.
$$

Hence if $supp(L_1) \geq supp(L_2)$ and $supp(L_2) \geq supp(L_1)$ then 

$$
  S(L_1) S(L_2) = S(L_1 + L_2) = S(L_2 + L_1) = S(L_2) S(L_1)
  \,,
$$

which is the second statement to be shown.


For the last statement, notice that by causal closure of
$O$ the difference $L_2 - L_2$, which by assumption has
$supp(L_2 - L_1) \in \mathbb{R}^{d-1,1} \setminus O$,
may be written as

$$
  L_2 - L_1 = a + r
$$

such that

$$
  supp(a) \geq supp(J) \geq supp(r)
$$

It follows with causal additivity and its equivalent formulations above that

$$
  \begin{aligned}
    V(L_2, J)
      & =
    V(L_1 + a + r, J)
    \\
      & =
    V(L_1 + r , J)
    \\
      & =
    S(L_1 + r)^{-1} S(L_1 + r + J)
    \\
      & =
    S(L_1 + r)^{-1} S(J + L_1) S(L_1)^{-1} S(L_1 + r)
    \\
      & =
    S(L_1 + r)^{-1} \underset{= id}{\underbrace{S(L_1) S(L_1)^{-1}}} S(L_1 + J) S(L_1)^{-1} S(L_1 + r)
    \\
      & =
    V(L_1, r)^{-1} V(L_1, J) V(L_1,r)
  \end{aligned}
$$

and hence the last statement holds for $K \coloneqq V(g_1,r)$.

=--



### In functorial quantum field theory

At least the _idea_ of the S-matrix is very explicit in the Atiyah-Segal picture of _functorial QFT_ ([[FQFT]]).

Here a quantum field theory is given by a [[functor]]

$$
 Z \colon Bord_d^S \longrightarrow Vect
$$

from a suitable [[category of cobordisms]] to a suitable [[category]] of [[vector spaces]].

* To a codimension-1 slice $M_{d-1}$ of space this assigns a vector space $Z(M_{d-1})$ -- the (Hilbert) [[space of quantum states]] over $M_{d-1}$;

* to a [[spacetime]]/[[worldvolume]] manifold $M$ with [[boundaries]] $\partial M$ one assigns the quantum propagator which is the linear map $Z(M) : Z(\partial_{in} M) \to Z(\partial_{out} M)$ that takes incoming states to outgoing states via propagation along the spacetime/worldvolume $M$. This $Z(M)$ is alternatively known as the  the _[[scattering amplitude]]_ or _S-matrix_ for propagation from $\partial_{in}M$ to $\partial_{out}M$ along a process of shape $M$.

Now for genuine [[topological field theories]] all spaces of quantum states are [[finite number|finite]] [[dimension|dimensional]] and hence we can equivalently consider the [[dual vector space]] (using that finite dimensional vector spaces form a [[compact closed category]]). Doing so the propagator map

$$
  Z(M) : Z(\partial_{in}M) \to Z(\partial_{out}M)
$$

equivalently becomes a linear map of the form

$$
  \mathbb{C} \to Z(\partial_{out}M) \otimes Z(\partial_{in}M)^\ast = Z(\partial M)
  \,.
$$

Notice that such a linear map from the canonical 1-dimensional complex vector space $\mathbb{C}$ to some other vector space is equivalently just a choice of element in that vector space. It is in this sense that $Z(M)$ is equivalently a vector in $Z(\partial_{out}M) \otimes Z(\partial_{in}M)^\ast = Z(\partial M)$.

In this form in physics the propagator is usually called the _[[correlator]]_ or _[[n-point function]]_ .

Segal's axioms for [[FQFT]] ([[CFT]] in his case) were originally explicitly about the propagators/S-matrices, while Atiyah formulated it in terms of the correlators this way. Both perspectives go over into each other under duality as above.

Notice that this kind of discussion is not restricted to topological field theory. For instance already plain quantum mechanics is usefully formulated this way, that's the point of [[finite quantum mechanics in terms of dagger-compact categories]].

## Properties

### Possible symmetries

see at _[[Haag–Lopuszanski–Sohnius theorem]]_


## History
 {#History}


In the 1960s there was a prominent proposal, around [[Geoffrey Chew]], that ([[perturbative quantum field theory|perturbative]]) [[quantum field theory]] should be _defined_ by [[axiom|axiomatizing]] properties of the S-matrix. This is a radical perspective where no [[spacetime]] geometry and physical fields are made explicit, but where the entire physics is encoded by what quantum particles see that scatter through it.

Historically, the S-matrix "bootstrap" approach fell out of fashion with the success of the [[quark]] model and of [[QCD]], which is a [[local field theory]] governed by an [[action functional]] ([[Yang-Mills theory]]).

But later [[perturbative string theory]] revived the S-matrix approach. In general, perturbative string theory is not defined by a geometric background. Instead the background is algebraically encoded by a [[2d SCFT]] ("[[2-spectral triple]]") and the [[string perturbation series]] is a formula that translates this into an S-matrix. Spacetime physics then is whatever is seen by string scattering processes (see also at _[string theory FAQ -- What are the equations of string theory?](string%20theory%20FAQ#WhatAreTheEquations)_)

More recently, the S-matrix perspective becomes fashionable also in [[Yang-Mills theory]], at least in [[super Yang-Mills theory]]: one observes that the theory enjoyes good structures in its scattering amplitudes which are
essentially invisible in the vast summation of [[Feynman diagrams]] that extract the S-matrix from the [[action functional]]. Instead there are entirely different mathematical structures that encode at least some sub-class of scattering amplitudes (see at _[[amplituhedron]]_).

From [this physics.SE comment](http://physics.stackexchange.com/a/15164/5603) by Ron Maimon:

> The history of [[physics]] cannot be well understood without appreciating the unbelievable antagonism between the [[Geoffrey Chew|Chew]]/[[Stanley Mandelstam|Mandelstam]]/[[Vladimir Gribov|Gribov]] S-matrix camp, and the [[Steven Weinberg|Weinberg]]/[[Sheldon Glashow|Glashow]]/[[Alexander Polyakov|Polyakov]] [[quantum field theory|Field theory]] camp. The two sides hated each other, did not hire each other, and did not read each other, at least not in the west. The only people that straddled both camps were older folks and Russians--- [[Murray Gell-Mann|Gell-Mann]] more than [[Lev Landau|Landau]] (who believed the [[Landau pole]] implied S-matrix), Gribov and Migdal more than anyone else in the west other than [[Murray Gell-Mann|Gell-Mann]] and [[Kenneth Wilson|Wilson]]. Wilson did his PhD in S-matrix theory, for example, as did [[David Gross]] (under Chew).

> In the 1970s, S-matrix theory just plain died. All practitioners jumped ship rapidly in 1974, with the triple-whammy of [[effective field theory|Wilsonian field theory]], the discovery of the Charm [[quark]], and [[asymptotic freedom]]. These results killed S-matrix theory for thirty years. Those that jumped ship include all the original [[string theory|string theorists]] who stayed employed: notably [[Gabriele Veneziano|Veneziano]], who was convinced that [[gauge theory]] was right when [[Gerard 't Hooft|t'Hooft]] showed that [[AdS-CFT|large-N gauge fields]] give the string topological expansion, and [[Leonard Susskind|Susskind]], who didn't mention Regge theory after the early 1970s. Everybody stopped studying [[string theory]] except [[Joël Scherk|Scherk]] and [[John Schwarz|Schwarz]], and Schwarz was protected by Gell-Mann, or else he would never have been tenured and funded.

> This sorry history means that not a single S-matrix theory course is taught in the curriculum today, nobody studies it except a few theorists of advanced age hidden away in particle accelerators, and the main S-matrix theory, [[string theory]], is not properly explained and remains completely enigmatic even to most physicists. There were some good reasons for this--- some S-matrix people said silly things about the consistency of quantum field theory--- but to be fair, [[quantum field theory]] people said equally silly things about S-matrix theory.

> Weinberg came up with these heuristic arguments in the 1960s, which convinced him that S-matrix theory was a dead end, or rather, to show that it was a tautological synonym for quantum field theory. Weinberg was motivated by models of pion-nucleon interactions, which was a hot S-matrix topic in the early 1960s. The solution to the problem is the chiral symmetry breaking models of the pion condensate, and these are effective field theories.

> Building on this result, Weinberg became convinced that the only real solution to the S-matrix was a field theory of some particles with spin. He still says this every once in a while, but it is dead wrong. The most charitable interpretation is that every S-matrix has a field theory limit, where all but a finite number of particles decouple, but this is not true either (consider little string theory). String theory exists, and there are non-field theoretic S-matrices, namely all the ones in string theory, including little string theory in (5+1)d, which is non-gravitational.

From ([Weinberg 09, p. 11](#Weinberg09)):

> I offered this in my 1979 paper as what Arthur Wightman would call a [[folk theorem]]: "if one writes down the most general possible [[Lagrangian]], including all terms consistent with assumed [[symmetry]] principles, and then calculates [[scattering amplitudes|matrix elements]] with this Lagrangian to any given order of [[perturbation theory]], the result will simply be the most general possible S-matrix consistent with perturbative unitarity, analyticity, [[cluster decomposition]], and the assumed symmetry properties."

> There was an interesting irony in this. I had been at Berkeley from 1959 to 1966, when [[Geoffrey Chew]] and his collaborators were elaborating a program for calculating S-matrix elements for strong interaction processes by the use of unitarity, analyticity, and Lorentz invariance, without reference to [[quantum field theory]]. I found it an attractive philosophy, because it relied only on a minimum of principles, all well established. Unfortunately, the S-matrix theorists were never able to develop a reliable method of calculation, so I worked instead on other things, including [[current algebra]]. Now in 1979 I realized that the assumptions of S-matrix theory, supplemented by chiral invariance, were indeed all that are needed at low energy, but the most convenient way of implementing these assumptions in actual calculations was by good old quantum field theory, which the S-matrix theorists had hoped to supplant.



## Related entries

See also at _[[sigma model]]_ the section _<a href="http://ncatlab.org/nlab/show/sigma-model#SecondQuantization">Exposition of second quantization of sigma-models</a>_

* [[Coleman theorem]], [[Haag–Łopuszański–Sohnius theorem]]

* [[scattering amplitude]], [[Feynman diagram]], [[string scattering amplitude]],

* [[AdS-CFT]]

* [string theory FAQ -- What are the equations of string theory?](string%20theory%20FAQ#WhatAreTheEquations)

## References

Early work basing [[perturbative quantum field theory]] on the concept of the S-matrix is

* {#Heisenberg43} [[Werner Heisenberg]], Zeitschrift f&#252;r Physik 120, 513, 1943

The mathematically rigorous construction in field theory via [[causal perturbation theory]] is due to

* {#EpsteinGlaser73} [[Henri Epstein]], [[Vladimir Glaser]], _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211 ([Numdam](http://www.numdam.org/item?id=AIHPA_1973__19_3_211_0 ))

Brief introuction to the S-matrix in quantum mechanics and its rigorous construction in field theory via [[causal perturbation theory]]

* {#Scharf95} [[Günter Scharf]], sections 0.3 and 3.1 of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Springer 1995

* [[Günter Scharf]], section 2 of _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

See also

* Alan. R. White, _The Past and Future of S-Matrix Theory_ ([arXiv:hep-ph/0002303](https://arxiv.org/abs/hep-ph/0002303))

* {#Weinberg09} [[Steven Weinberg]], _Effective Field Theory, Past and Future_ ([arXiv:0908.1964](http://arxiv.org/abs/0908.1964))

* Jacob Bourjaily, _Quantum Field Theory and the Analytic S-Matrix_, 2011 ([pdf](https://www.princeton.edu/physics/graduate-program/theses/theses-from-2011-1/bourjaily_princeton_thesis.pdf))

Talk notes:

* Gabriele Travaglini, _The return of the analytic S-matrix_, 2013 ([pdf](http://pyweb.swan.ac.uk/sfsh/sewmweb/sfshtalks/gabriele.pdf))

* Rutger Boels, _The Ultimate Revenge of the Analytic S-matrix_ ([pdf](http://thep.housing.rug.nl/sites/default/files/talks/The%20revenge%20of%20the%20analytic%20S-matrix.pdf))

See also

* Wikipedia, _[S-matrix](http://en.wikipedia.org/wiki/S-matrix#History)_

* Wikipedia, _[S-matrix theory](http://en.wikipedia.org/wiki/S-matrix_theory)_


An entertaining account of some of the history and the sociology of S-matrix theory is on the first pages of

* {#Shankar99} [[Ramamurti Shankar]], _Effective Field Theory in Condensed Matter Physics_ in _Conceptual Foundations of Quantum Field Theory_, 1999 ([arXiv:cond-mat/9703210](http://arxiv.org/abs/cond-mat/9703210))

[[!redirects S-matrices]]


[[!redirects scattering matrix]]
[[!redirects scattering matrices]]

[[!redirects S-matrix theory]]
[[!redirects S-matrix theories]] 