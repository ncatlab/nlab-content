
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

be an Hermitian operator, thought of as a [[Hamiltonian]], decomposed as the [[sum]] of a free part ([[kinetic energy]]) and an interaction part ([[potential energy]]).

For example for a  [[non-relativistic particle]] of [[mass]] $m$ propagating on the [[line]] subject to a [[potential energy]] $V_{pot} \colon \mathbb{R} \to \mathbb{R}$, then $\mathcal{H} = L^2(\mathbb{R})$ is the Hilbert space space of [[square integrable functions]] and

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
      V_I(t_2) V_I(t_1) &\vert& t_2 \geq t_1
    }
  \right.
  \,.
$$

(This is abuse of notation: Strictly speaking time ordering acts on the [[tensor algebra]] spanned by the $\{V_I(t)\}_{t \in \mathbb{R}}$ and has to be _followed_ by taking tensor products to actual products. )

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


### In perturbative algebraic quantum field theory


In [[perturbative algebraic quantum field theory]] the broad structure of the [[interaction picture]] in [[quantum mechanics]] ([above](#InQuantumMechanics)) remains a very good guide, but various technical details have to be generalized with due care:

1. The algebra of operators in the [[Heisenberg picture]] of the free theory becomes the _[[Wick algebra]]_ of the [[free field theory]] (taking into account "normal ordering" of field operators) defined on _[[microcausal functionals]]_ built from [[operator-valued distributions]] with constraints on their [[wave front set]].

1. The [[time-ordered products]] in the [[Dyson formula]] have to be refined to [[causal locality|causally ordered]] products and the resulting product at coincident points has to be defined by [[point-extension of distributions]] -- the freedom in making this choice is the [[renormalization]] freedom ("conter-terms").

1. The sharp interaction cutoff in the [[Dyson formula]] that is hidden in the integration over $[t_0,t]$ has to be smoothed out by [[adiabatic switching]] of the interaction (making the whole S-matrix an [[operator-valued distribution]]).

Together these three point are taken care of by the axiomatization of the "[[adiabatic switching|adiabatically switched]] [[S-matrix]]" according to **[[causal perturbation theory]]**.


The analogue of the limit $t \to \infty$ in the construction of the [[S-matrix]] (now: [[adiabatic limit]]) in general does not exist in field theory ("infrared divergencies"). But in fact it need not be taken: The field algebra in a bounded region of [[spacetime]] may be computed with any adiabatic switching that is constant on this region. Moreover, the algebras assigned to regions of spacetime this way satisfy [[causal locality]] by the causal ordering in the construction of the S-matrix. Therefore, even without taking the adiabatic limit in [[causal perturbation theory]] one obtains a field theory in the form of a _[[local net of observables]]_. This is the topic of **[[locally covariant perturbative quantum field theory]]**.


$\,$


#### Spacetime and Causality
 {#SpacetimeAndCausality}



Throughout, let
$\Sigma$ be a [[time orientation|time-oriented]] [[globally hyperbolic Lorentzian manifold]] of [[dimension]]

$$
  p + 1 \in \mathbb{N}
$$

This is to model the [[spacetime]] over which we consider [[field theory]]. Hence we will often refer to $\Sigma$
just as _[[spacetime]]_, for short.

We need to consider the following concepts and constructions related to the [[causal structure]] of $\Sigma$.

+-- {: .num_defn #CausalPastAndFuture}
###### Definition
**(causal [[past]] and [[future]])**

For $x \in \Sigma$ a point in spacetime, we write

$$
  V^+(x), V^-(x) \subset \Sigma
$$

for its [[open future cone]] and [[open past cone]], respectively, and

$$
  \overline{V}^+(x), \overline{V}^-(x) \subset \Sigma
$$

for the corresponding closed cones. We write

$$
  J(x) \coloneqq \overline{V}^+(x) \cup \overline{V}^-(x)
$$

for the full [[causal cone]].

For $S \subset \Sigma$ a [[subset]] we write

$$
  \overline{V}^\pm(S)
  \;\coloneqq\;
  \underset{x \in S}{\cup} \overline{V}^{\pm}(x)
$$

for the union of the future/past closed cones of all its points.

=--



+-- {: .num_defn #CausalOrdering}
###### Definition
**(causal order)**

Consider the [[relation]] on the set $P(\Sigma)$ of [[subsets]] of spacetime
which says a [[subset]] $S_1 \subset \Sigma$ is _not prior_ to a subset $S_2 \subset \Sigma$,
denoted $S_1 \geq S_2$, if $S_1$ does not [[intersection|intersect]] the [[causal past]] of $S_2$ (def. \ref{CausalPastAndFuture}),
or equivalently that $S_2$ does not intersect the [[causal future]] of $S_1$:

$$
  \begin{aligned}
    (S_1 \geq S_2)
    & \coloneqq
    S_1 \cap \overline{V}^-(S_2) = \emptyset
    \\
    & \Leftrightarrow S_2 \cap \overline{V}^+(S_1) = \emptyset
   \end{aligned}
   \,.
$$

If $S_1 \geq S_2$ and $S_2 \geq S_1$ we say that the two subsets are _[[spacelike]] separated_.

=--

+-- {: .num_example #CausalComplementOfSubsetOfLorentzianManifold}
###### Definition
**([[causal complement]] and [[causal closure]] of subset of [[spacetime]])**

For $S \subset X$ a [[subset]] of [[spacetime]], its _[[causal complement]]_ $S^\perp$ is the [[complement]] of the [[causal cone]]:

$$
  S^\perp \;\coloneqq\; S \setminus J_X(S)
  \,.
$$

The causal complement $S^{\perp \perp}$ of the causal complement $S^\perp$ is called the _[[causal closure]]_. If

$$
  S = S^{\perp \perp}
$$

then the subset $S$ is called a _[[causally closed subset]]_.

Given a [[spacetime]] $\Sigma$, we write

$$
  CausClsdSubsets(\Sigma) \;\in\; Cat
$$

for the [[partially ordered set]] of causally closed subsets, partially ordered by
inclusion $\mathcal{O}_1 \subset \mathcal{O}_2$.

=--


+-- {: .num_defn #CutoffFunctions}
###### Definition
**([[adiabatic switching]])**

For a [[causally closed subset]] $\mathcal{O} \subset \Sigma$ of [[spacetime]] (def. \ref{CausalComplementOfSubsetOfLorentzianManifold}) say that an
_[[adiabatic switching]] function_ or  _cutoff function_ for $\mathcal{O}$
is a [[smooth function]] $g_{sw}$ of [[compact support]] (a [[bump function]]) whose
restriction to some [[neighbourhood]] of $\mathcal{O}$ is the [[constant function]]
with value $1$:

$$
  Cutoffs(\mathcal{O})
  \;\coloneqq\;
  \left\{
    g_{sw} \in \mathcal{C}^\infty_c(\Sigma)
    \;\vert\;
    \underset{ {U \supset \mathcal{O}} \atop { \text{neighbourhood} } }{\exists}
    \left(
      g_{sw}\vert_S = const_1
    \right)
  \right\}
  \,.
$$

Often we consider the vctor space space $C^\infty(\Sigma)\langle g \rangle $ spanned by a formal
variable $g$ under multiplication with smooth functions, and consider as adiabatic switching functions
the corresponding images in this space, which are hence bump functions constant on $g$ over
a neighbourhood of $\mathcal{O}$.


=--

+-- {: .num_lemma #CausalPartition}
###### Lemma
**(causal partition)**

Let $\mathcal{O} \subset \Sigma$ be a [[causally closed subset]] (def. \ref{CausalComplementOfSubsetOfLorentzianManifold})
and let $f \in C^\infty_{cp}(\Sigma)$ be a [[compact support|compactly supported]] [[smooth function]] which vanishes
on a [[neighbourhood]] $U \supset \mathcal{O}$, i.e. $f\vert_U = 0$.

Then there exists a _causal partition_ of $f$ in that there
exist compactly supported smooth functions $a,r \in C^\infty_{cp}(\Sigma)$
such that

1. they sum up to $f$:

   $$
     f = a + r
   $$

1. their [[support]] satisfies the following causal ordering (def. \ref{CausalOrdering})

   $$
     supp(a) \geq \mathcal{O} \geq supp(r)
     \,.
   $$

=--

+-- {: .proof}
###### Proof idea

By assumption $\mathcal{O}$ has a [[Cauchy surface]]. This may be
extended to a Cauchy surface $\Sigma_p$ of $\Sigma$, such that this is one [[leaf]]
of a [[foliation]] of $\Sigma$ by Cauchy surfaces, given by a [[diffeomorphism]]
$\Sigma \simeq (-1,1) \times \Sigma_p$ with the original $\Sigma_p$ at zero.
There exists then $\epsilon \in (0,1)$ such that
the restriction of $supp(f)$ to the interval $(-\epsilon, \epsilon)$ is
in the [[causal complement]] $\overline{\mathcal{O}}$ of the given region (def. \ref{CausalComplementOfSubsetOfLorentzianManifold}):

$$
  supp(f) \cap (-\epsilon, \epsilon) \times \Sigma_p
  \;\subset\;
  \overline{\mathcal{O}}
  \,.
$$

Let then $\chi \colon \Sigma \to \mathbb{R}$ be any [[smooth function]] with

1. $\chi\vert_{(-1,0] \times \Sigma_p} = 1$

1. $\chi\vert_{(\epsilon,1) \times \Sigma_p} = 0$.

Then

$$
  r \coloneqq \chi \cdot f
  \phantom{AAA}
  \text{and}
  \phantom{AAA}
  a \coloneqq (1-\chi) \cdot f
$$

are smooth functions as required.

=--



#### Free fields and Propagators

The definition and construction of a perturbative S-matrix below proceeds on the backdrop of a
[[formal deformation quantization|formal]] of the underlying [[free field theory]],
in particular a corresponding perturbative [[algebra of observables]], the _[[Wick algebra]]_ $\mathcal{W}$.
Here we briefly recall relevant bckground from [[free field theory]].

But just stating the [[axioms]] for the perturbative Lagrangian S-matrix ([below](#PerturbativeSMatrixAndTimeOrderedProducts))
and deducing from these axioms the [[causally local net of quantum observables]] ([further below](#CausalLocality))
only requires knowing that there is a
[[continuous linear functional]]

$$
  :(-):
    \;\colon\;
  \mathcal{F}_{loc} \longrightarrow \mathcal{W}
$$

from [[local observables]] to the coresponding [[quantum observables]], being elements of the [[Wick algebra]].

The actual construction of the S-matrix ([further below](#ExistenceAndRenormalization)) and the proof of the
[[main theorem of perturbative renormalization]] requires more details, which we briefly summarize here.



+-- {: .num_defn #CompactlySupportedPolynomialLocalDensities}
###### Definition
**([[local observables]])**

Let $\Sigma$ be a [[globally hyperbolic spacetime]], let

$$
  \array{
    E
    \\
    \downarrow^{\mathrlap{fb}}
    \\
    \Sigma
  }
$$

be a smooth [[fiber bundle]] regarded as a [[field bundle]] and let

$$
  \mathbf{L} \in \Omega^{p+1,0}_\Sigma(E)
$$

be a [[local Lagrangian density]]. We write

$$
  \Omega \in \Omega^{p,2}_\Sigma(E)
$$

for the corresponding [[pre-symplectic current]] and

$$
  \Omega^{p,0}_{\Sigma, Ham}(E)
$$

for the induced space of [[Hamiltonian differential forms]]. We write

$$
  \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0} \hookrightarrow \Gamma_\Sigma(E)
$$

for the subspace of solutions to the [[Euler-Lagrange equations]] inside the full field [[configuration space]] (the [[shell]]).

If the [[Euler-Lagrange operator]] $j^\infty_\Sigma(-)^\ast \delta_{EL}\mathbf{L}$ is a _linear [[normally hyperbolic differential operator]]_ on $\Gamma_\Sigma(E)$ we say that the field theory is a _[[free field theory]]_.

Since $\Sigma$ is assumed to be [[time orientation|time-oriented]] [[globally hyperbolic spacetime|globally hyperbolic]], there
exists a 1-form $e^0$ which represents the [[time orientation]]. The space $\mathcal{F}_{loc}$ of _[[local observables]]_
is the [[image]] of the [[Hamiltonian differential forms]] with compact spacetime support in the smooth functions on the [[on-shell]] under the
operations of forming the wedge product with $e^0$ followed by [[transgression]]


$$
  \mathcal{F}_{loc}
   \;\coloneqq\;
  im\left(
    \Omega^{p+1,0}_{\Sigma,Ham,cp}(E)
      \overset{e^0 \wedge (-)}{\longrightarrow}
    \Omega^{p2,0}_{\Sigma, cp}(E)
      \overset{\tau_{\Sigma}}{\longrightarrow}
    C^\infty\left( \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0} \right)
  \right)
  \,.
$$

Since the [[kernel]] of the transgression map is the space of forms in the image of the
[[total derivative|total horizontal derivative]] ([[horizontal derivative]]), this is equivalently

$$
  \mathcal{F}_{loc}
    \simeq
  im\left(
    \Omega^{p+1,0}_{\Sigma,Ham, cp}(E)
      \overset{e^0 \wedge (-)}{\longrightarrow}
    \Omega^{p2,0}_{\Sigma, cp}(E)
  \right)
  /im(d)
  \,.
$$

Due to the restriction to [[Hamiltonian differential forms]] in the construction of $\mathcal{F}_{loc}$,
the [[presymplectic current]] $\Omega$ induces a [[Poisson bracket]] on the space of local observables

$$
  \{-,-\}
  \;\colon\;
  \mathcal{F}_{loc} \otimes \mathcal{F}_{loc}
    \longrightarrow
  \mathcal{F}_{loc}
  \,.
$$

Given a [[formal deformation quantization]] $\mathcal{W}$ of this Poisson bracket, then we write

$$
  \mathcal{F}_{loc}
    \overset{:(-):}{\longrightarrow}
  \mathcal{W}
$$

for the corresponding quantization map.

=--

In the case of _[[free field theories]]_ such $\mathcal{W}$ is given by the _[[Wick algebra]]_.
See there for more.


In the following we need to keep track of powers of the [[coupling constant]] and the [[source field]].
To that end, we write $\langle g,j\rangle$ be the vector space spanned by the elements $g$ and $j$ and

$$
  \mathcal{F}_{loc} \langle g,j\rangle
  \;\coloneqq\;
  \mathcal{F}_{loc} \otimes \langle g,j\rangle
$$

Then every element of $\mathcal{F}_{loc}\langle g,j \rangle$ may be presented as

$$
  \underset{n_1}{\sum} g_{sw,n_1} L_{n_1} + \underset{n_2}{\sum} j_{sw,n_2} A_{n_2}
$$

where $L_{n_1}, L_{n_2} \in \Omega_{\Sigma,poly}^{p+1,0}(E)$ are polynomial local observables, to be regarded
as [[interaction]] [[Lagrangian densities]] and [[observables]], respectively, and where

$$
  g_{sw, n_1} \in C^\infty_{cp}(\Sigma) \langle g\rangle
$$

and

$$
  j_{sw,n_2} \in C^\infty_{cp}(\Sigma) \langle j \rangle
$$

are [[compact support|compactly supported]] [[smooth functions]]
([[bump functions]]) on spacetime $\Sigma$ times the [[coupling constant]] or source strength, respectively,
 to be regarded as [[adiabatic switching|adiabatically switched]]
[[coupling constant]] and [[source field]], respectively.


We will be considering [[formal power series]] in $g/\hbar$ and $j/\hbar$ with coefficients in the
[[Wick algebra]] $\mathcal{W}$. Since the vector space underlying the Wick algebra
$\mathcal{W} = (\mathcal{F}_{mc}[ [ \hbar ] ],  \cdot_H  )$
is itself that of a formal power series in $\hbar$, we have

$$
  \mathcal{W}[ [ g/\hbar, j/\hbar] ] \subset  ( \mathcal{F}_{mc}((\hbar)) [ [ g, j ] ], \cdot_H )
  \,.
$$



#### Perturbative S-Matrix and Time-ordered products
 {#PerturbativeSMatrixAndTimeOrderedProducts}

We consider now the [[axioms]] for a perturbative S-matrix of a [[Lagrangian field theory]]
as used in  [[causal perturbation theory]] (def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime} below).
Since, by definition, the S-matrix is a formal sum of multi-[[linear continuous functionals]],
it is convenient to impose axioms on these directly: this is the axiomatics for _[[time-ordered products]]_
in def. \ref{TimeOrderedProduct} below. That these latter axioms already imply the former
is the statement of prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix} below. Its proof
requires a close look at the "reverse-time ordered products" for the inverse S-matrix (def. \ref{ReverseTimeOrderedProduct} below)
and their induced reverse-causal factorization (prop. \ref{ReverseCausalFactorizationOfReverseTimeOrderedProducts} below).

The axioms we consider here are just the bare minimum of [[causal perturbation theory]], sufficient to
imply that the induced perturbative [[quantum observables]]
organize into a [[causally local net of quantum observables]] (discussed [below](#CausalLocality)).

In applications one considers further axioms, in particular compatibility of the S-matrix with
[[spacetime]] [[symmetry]]. This is needed for the proof of the [[main theorem of perturbative renormalization]]
(see [below](#ExistenceAndRenormalization)).


+-- {: .num_defn #PerturbativeSMatrixOnMinkowskiSpacetime}
###### Definition
**(perturbative Lagrangian S-matrix)**

Let $\mathcal{W}$ be a [[Wick algebra]]
encoding the quantization of [[free fields]] in $E$, with

$$
  \mathcal{F}_{loc} \overset{:(-):}{\longrightarrow} \mathcal{W}
$$

the quantization map (def. \ref{CompactlySupportedPolynomialLocalDensities}).

Then a _Lagrangian S-matrix for fields of type $E$ perturbing the free fields encoded by $\mathcal{W}$_, is a [[functional]]

$$
  S
    \;\colon\;
  \mathcal{F}_{loc}\otimes ( \langle g,j\rangle  ) \longrightarrow \mathcal{W}[ [ g/\hbar, j/\hbar ] ]
$$

(on [[local observables]] (def. \ref{CompactlySupportedPolynomialLocalDensities})
times the coupling constant $g$ or source strength $j$
with values in the algebra of [[formal power series]] in the formal variables $g/\hbar$
and $j/\hbar$  in the given [[Wick algebra]])
such that the following conditions hold for fixed $L_{int}, \{ J_n\}_{n = 1}^N$:

1. (perturbation)

   There exist [[distributions]] ([[multilinear map|multi-]] [[linear continuous functionals]]) of the form

   $$
     T \;\colon\; (\mathcal{F}_{loc} \otimes ( \langle g,j \rangle ) )^{\otimes^k} \longrightarrow \mathcal{W}[ [ g/\hbar, j/\hbar ] ]
   $$

   for all $k \in \mathbb{N}$, such that:

   1. The unary operation is the quantization map

      $$
        T(L + A) = :L: + :A:
      $$

   1. The S-matrix is the [[exponential]] of "time-ordered products" in that  for $L, A  \in \mathcal{F}_{loc}$

      $$
        \begin{aligned}
          S( g L + j A )
          & =
          T\left( \exp_{\otimes}\left( \tfrac{1}{i \hbar} \left( g L + j A\right) \right) \right)
          \\
          & \coloneqq
          \underoverset{k = 0}{\infty}{\sum} \tfrac{1}{k!}
          \frac{1}{(i \hbar)^k}
          T(\underset{k\, \text{arguments}}{\underbrace{ (g L + j A) \cdots (g L + j A) }})
        \end{aligned}
      $$

1. (normalization)

   $$
     S(0) = 1
   $$

1. ([[causal additivity]])

  For all $J_1, J_2, L \in \mathcal{F}_{loc}$ we have

   $$
     \left( supp(J_1) \geq supp(J_2) \right)
     \;\; \Rightarrow \;\;
     \left(
       \underset{L \in \mathcal{F}_{loc}}{\forall}
       \left(
         S(L + J_1 + J_2)
         =
         S(L + J_1) S(L)^{-1} S(L + J_2)
       \right)
     \right)
     \,.
   $$

Given such perturbative $S$-matrix, then we say that the _[[generating function]]_
(for [[quantum observables]], see def. \ref{GeneratingFunctionsForCorrelationFunctions} below) that it induces is the functional

$$
  \label{GeneratingFunctionInducedFromSMatrix}
  Z
    \;\colon\;
  \mathcal{F}_{loc} \langle g \rangle
    \times
  \mathcal{F}_{loc} \langle j \rangle
    \longrightarrow
  \mathcal{W}[ [ g/\hbar] ][ [ j/\hbar ] ]
$$

given by

$$
  Z_{g_{sw}L_{int}}(j_{sw}A)
  \;\coloneqq\;
  S(g_{sw}L_{int})^{-1} S( g_{sw}L_{int} + j_{sw}A )
  \,.
$$


=--

Def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime} is due to ([Epstein-Glaser 73 (1)](#EpsteinGlaser73))
(in view of lemma \ref{CausalLocalityOfThePerturbativeSMatrix} below), except that these authors
remain a little vague on the nature of the domain.
The domain $\mathcal{F}_{loc}$ is made explicit (in terms of axioms
for the [[time-ordered products]], see def. \ref{TimeOrderedProduct} below),
in ([Brunetti-Fredenhagen 99, section 3](#BrunettiFredenhagen99), [D&#252;tschFredenhagen 04, appendix E](#DuetschFredenhagen04),
[Hollands-Wald 04,  around (20)](#HollandsWald04)); for review see ([Rejzner 16, around def. 6.7](#Rejzner16)).

+-- {: .num_remark}
###### Remark
**(further axioms)**

The list of axioms in def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime},
similarly those for the [[time-ordered products]] below in def. \ref{TimeOrderedProduct}, is just the bare
minimum which implies that the corresponding [[quantum observables]]
organize into a [[causally local net]] (discussed [below](#CausalLocality)).
In applications such as in discussion of [[renormalization]] ([below](#ExistenceAndRenormalization))
one considers further axioms, such a unitarity and compatibility with spacetime symmetry.

=--


+-- {: .num_remark #PerturbativeSMatrixInverse}
###### Remark
**(invertibility of the perturbative S-matrix)**

The mutliplicative inverse $S(-)^{-1}$ of the perturbative S-matrix in def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}
always exists: By the axioms "perturbation" and "normalization" this follows with the usual formula
for the multiplicative inverse of [[formal power series]] that are non-vanishing in degree 0:

If we write

$$
  S(g L +  j A) \coloneqq 1 + D(g L + j A)
$$

then

$$
  \label{InfverseOfPerturbativeSMatrix}
  \begin{aligned}
    S(g L + j A)^{-1} &= (1 + D(j L + j A))^{-1}
    \\
    & =
    \underoverset{r = 0}{\infty}{\sum} (-D(g L + j A))^r
    \\
    & =
    \underoverset{r = 0}{\infty}{\sum} (1 - S(g L + j A))^r
    \,,
  \end{aligned}
$$

where the last sum does exist in $\mathcal{W}[ [ g/\hbar, j/\hbar] ]$ because by
the axiom "normalization"
$D(L)$ has vanishing coefficient in zeroth order, so that
only a finite sub-sum of the formal infinite sum contributes in each order.

=--


+-- {: .num_remark #InterpretationOfPerturbativeSMatrix}
###### Remark
**(interpretation of the perturbative S-matrix as a [[path integral]])**

In def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime} $g/\hbar$ has the interpretation of the
[[coupling constant]] divided by [[Planck's constant]]. One obtains a [[formal power series]]
with the expected non-negative powers of $\hbar$ after passing to the [[quantum observables]]
induced by the S-matrix, see def. \ref{GeneratingFunctionsForCorrelationFunctions} below.

The local density $g_{sw}L_{int}$ has the interpretation
[[interaction]] [[Lagrangian density]] $L_{int}$ [[adiabatic switching|adiabatically switched]] by a compactly supported
function $g_{sw}$,  and $j_{sw}$ has the interpretation of a [[source field]].

In informal heuristic discussion of [[perturbative quantum field theory]] the S-matrix is thought of as a [[path integral]],
written

$$
  S\left(
    \tfrac{g}{\hbar} L_{int} + j
  \right)
  \;\overset{\text{not really!}}{=}\;
  \underset{\Phi \in \Gamma_\Sigma(E)_{asmpt}}{\int}
  \exp\left(
    \int_X
    \left(
      \tfrac{g}{i \hbar} L_{int}(\Phi) + j A(\Phi)
    \right)
  \right)  e^{\tfrac{1}{i \hbar}\int_X L_{free}(\Phi) }D[\Phi]
$$

where the integration is thought to be over the [[configuration space]] $\Gamma_\Sigma(E)_{asmpt}$ of [[field (physics)|fields]] $\Phi$
(the [[space of sections]] of the given [[field bundle]])
which satisfy given asymptotic conditions at $x^0 \to \pm \infty$; and as these boundary conditions
vary the above is regarded as an integral kernel that defines the required operator in $\mathcal{W}$
(e.g. [Weinberg 95, around (9.3.10) and (9.4.1)](#Weinberg95)).

We may think of the axioms in def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime} as rigorously _defining_
the [[path integral]], not as an actual [[integration]], but "[[synthetic mathematics|synthetically]]"
by defining the expected causal behaviour of the would-be integration.

=--

Definition \ref{PerturbativeSMatrixOnMinkowskiSpacetime} suggests to focus on the
multilinear operations $T(...)$ which define the perturbative S-matix order-by-order:


+-- {: .num_defn #TimeOrderedProduct}
###### Definition
**([[time-ordered product]])**

Let $\mathcal{W}$ be a [[Wick algebra]]
encoding the quantization of [[free fields]] in $E$ (def. \ref{CompactlySupportedPolynomialLocalDensities}).

A _[[time-ordered product]]_ is a sequence of [[distributions]] ([[multilinear map|multi-]] [[linear continuous functionals]]) of the form

$$
  T_k \;\colon\; \mathcal{F}_{loc}^{\otimes^k} \longrightarrow \mathcal{W}[ [ g/\hbar ] ]
$$

for all $k \in \mathbb{N}$, such that:

1. (perturbation) $T_1(g L + j A) =  :g L: +  :j A:$

1. (normalization) $T_0 = 1$

1. (symmetry) each $T_k$ is symmetric in its arguments

1. ([[causal factorization]]) If $supp(L_1) \cup \cdots \cup supp(L_r) \;\geq\; supp(L_{r+1}) \cup \cdots \cup supp(L_k)$ then

   $$
     T((g L_1 + j A_1)  \cdots (g L_k + j A_k) )
       =
     T( (g L_1 + j A_1)  \cdots (g L_r + j A_r) )
     T( (g L_{r+1} + j A_{r+1})  \cdots ( g L_k + j A_{k} ) )
     \,.
   $$

=--

+-- {: .num_defn #NotationForTimeOrderedProductsAsGeneralizedFunctions}
###### Definition
**(notation for time-ordered products as [[generalized functions]])**

It will be convenient (as in [Epstein-Glaser 73](#EpsteinGlaser73)) to think of the time-ordered products, being [[operator-valued distributions]], as [[generalized functions]] with dependence on spacetime points:

$$
  \begin{aligned}
    & \int_{\Sigma^{r+s}}
      T_{L_1, \cdots, L_r, A_1, \cdots, A_s}(x_1, \cdots, x_{r}, y_1, \cdots, y_s)
      g_{sw,1}(x_1) \cdots g_{sw, r}(x_r)
      j_{sw,1}(y_1) \cdots j_{sw,s}(y_s)
    dvol_\Sigma(x_1, \cdots, x_r, y_1, \cdots, y_s)
    \\
    & \coloneqq
    T( g_{sw,1} L_1 \cdots g_{sw,k} L \cdot j_{sw,1} A_1 \cdots j_{sw,s}A_s )
  \end{aligned}
  \,.
$$

Moreover, the subscripts on these [[generalized functions]] will always be
clear from the context, so that in computations we will notationally suppress these.

Finally, due to the "symmetry" axiom in def. \ref{TimeOrderedProduct}, a time-ordered product
depends only on its [[set]] of arguments, not on the order of the arguments. We will write
$\mathbf{X} \coloneqq \{x_1, \cdots, x_r\}$ and $\mathbf{Y} \coloneqq \{y_1, \cdots y_r\}$
for sets of spacetime points, and hence abbreviate the expression for the "value" of the
generalized function in the above as $T(\mathbf{X}, \mathbf{Y})$ etc.

In this condensed notation the above reads

$$
    \int_{\Sigma^{r+s}}
      T(\mathbf{X}, \mathbf{Y})
      \,
      g_{sw,1}(x_1) \cdots g_{sw, r}(x_r)
      \,
      j_{sw,1}(y_1) \cdots j_{sw,s}(y_s)
    dvol_\Sigma(\mathbf{X},\mathbf{Y})
  \,.
$$

=--

This condensed notation turns out to be greatly simplify computations, as it absorbs all the "relative"
combinatorial prefactors:

+-- {: .num_example #ProductOfPerturbationSeriesInGenealizedFunctionNotation}
###### Example
**(product of perturbation series in generalized function notation)**

Let

$$
  U(g)
  =
  \underoverset{n = 0}{\infty}{\sum}
   \frac{1}{n!}
   \int U(x_1, \cdots, x_n)
   \,
   g(x_1) \cdots g(x_n) \, dvol
$$

and

$$
  V(g)
  =
  \underoverset{n = 0}{\infty}{\sum}
   \frac{1}{n!}
   \int V(x_1, \cdots, x_n)
   \,
   g(x_1) \cdots g(x_n) \, dvol
$$

be power series of distributions in formal power series in $g/\hbar$ as in def. \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}.
Then the product $W(g) \coloneqq U(g) V(g)$ with expansion

$$
  W(g)
  =
  \underoverset{n = 0}{\infty}{\sum}
   \frac{1}{n!}
   \int W(x_1, \cdots, x_n)
   \,
   g(x_1) \cdots g(x_n) \, dvol
$$

is given simply by

$$
  W(\mathbf{X})
    \;=\;
  \underset{\mathbf{I} \subset \mathbf{X}}{\sum} U(\mathbf{I}) V(\mathbf{X} \setminus \mathbf{I})
  \,.
$$

([Epstein-Glaser 73 (5)](#EpsteinGlaser73))

This is because for fixed cardinality ${\vert \mathbf{I} \vert} = n_1$
this sum over all subsets $\mathbf{I} \subset \mathbf{X}$ overcounts the sum over
partitions of the coordinates as $(x_1, \cdots x_{n_1}, x_{n_1 + 1}, \cdots x_n)$ precisely by the
[[binomial coefficient]] $\frac{n!}{n_1! (n - n_1) !}$. Here the factor of $n!$ cancels
against the "global" combinatorial prefactor in the above expansion of $W(g)$, while the remaining
factor $\frac{1}{n_1! (n - n_1) !}$ is just the "relative" combinatorial prefactor seen at total order $n$
when expanding the product $U(g)V(g)$.


=--



+-- {: .num_remark #TheTraditionalErrorThatLeadsToTheNotoriouDivergencies}
###### Remark
**(the traditional error that leads to the notorious divergencies)**

Naively it might seem that the time-ordered products of def. \ref{TimeOrderedProduct}
are given simply by multiplication with [[step functions]], in the notation as
generalized functions (def. \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}):

$$
  T(x_1, x_2)
  \overset{\text{no!}}{=}
  \theta(x_1^0 - x_2^0) T(x_1) T(x_2)
  +
  \theta(x_2^0 - x_1^0) T(x_2) T(x_1)
$$

etc. (for instance [Weinberg 95, p. 143, between (3.5.9) and (3.5.10)](#Weinberg95)).

This however is simply a mathematical error, in general: Both $T(-,-)$ as well as $\theta$
are [[distributions]] and their [[product of distributions]] is in general not defined.
The notorious "divergencies which plague quantum field theory" are the signature
of this ill defined operation.

On the other hand, when both distributions are restricted to the [[complement]] of the [[diagonal]]
(i.e. restricted away from $x_1 = x_2$) then the above expression happens to be well defined and does
solve the axioms for time-ordered products.

Hence what needs to be done to properly define the time-ordered product is to
choose an [[extension of distributions]] of the above expression from the complement of the
diagonal to the diagonal. Any such extension will produce time-ordered products.
There are in general several different such extensions. This freedom of choice is the freedom
of [[renormalization]]; or equivalently, by the [[main theorem of perturbative renormalization theory]],
this is the freedom of choosing "counter terms" for the local interaction. This we discuss below in
_[Feynman diagrams and (re-)normalization](#ExistenceAndRenormalization)_.


=--

In order to prove that the axioms for time-ordered products do imply those for a perturbative S-matrix
(prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix} below) we need to consider
the corresponding reverse-time ordere products:


+-- {: .num_defn #ReverseTimeOrderedProduct}
###### Definition
**(reverse-time ordered product)**

Given a time-ordered product $T = \{T_k\}_{k \in \mathbb{N}}$ (def. \ref{TimeOrderedProduct}),
its _reverse-time ordered product_

$$
  \overline{T}_k \;\colon\; \mathcal{F}_{loc}^{\otimes^k} \longrightarrow \mathcal{W}[ [ g/\hbar ] ]
$$

for $k \in \mathbb{N}$ is defined by

$$
  \overline{T}( L_1 \cdots L_n )
  \;\coloneqq\;
  \left\{
    \array{
      \underoverset{r = 1}{n}{\sum}
      (-1)^r
      \underset{\sigma \in Unshuffl(n,r)}{\sum}
      T( L_{\sigma(1)} \cdots L_{\sigma(k_1)} )
      \,
      T( L_{\sigma(k_1 + 1)} \cdots L_{\sigma(k_2)} )
      \cdots
      T( L_{\sigma(k_{r-1}+1)} \cdots L_{\sigma_{k_r}}  )
      &\vert& k \geq 1
      \\
      1 &\vert& k = 0
    }
  \right.
  \,,
$$

where the sum is over all [[unshuffles]] $\sigma$ of $(1 \leq \cdots \leq n)$ into $r$ non-empty
ordered subsequences. Alternatively, as a generalized function as in def. \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}, this reads

$$
  \overline{T}( \mathbf{X} )
  =
  \underoverset{r = 1}{{\vert \mathbf{X} \vert}}{\sum}
  (-1)^r
  \underset{ \array{
    \mathbf{I}_1, \cdots, \mathbf{I}_r \neq \emptyset
    \\
    \underset{j \neq k}{\forall}\left( \mathbf{I}_j \cap \mathbf{I}_k = \emptyset  \right)
    \\
    \mathbf{I}_1 \cup \cdots \cup \mathbf{I}_r = \mathbf{X}
  } }{\sum}  T( \mathbf{I}_1 ) \cdots T(\mathbf{I}_r)
$$

=--

(e.g. [Epstein-Glaser 73 (11)](#EpsteinGlaser73))

+-- {: .num_prop #ReverseTimOrderedProductsGiveReverseSMatrix}
###### Proposition
**(reverse-time ordered products express inverse S-matrix)

Given a time-ordered products $T(-)$ (def. \ref{TimeOrderedProduct}), then the
corresponding reverse time-ordered product $\overline{T}(-)$ (def. \ref{ReverseTimeOrderedProduct})
expresses the [[inverse]] $S(-)^{-1}$ (according to remark \ref{PerturbativeSMatrixInverse}) of the corresponding
perturbative S-matrix $S(L) \coloneqq \underset{k \in \mathbb{N}}{\sum} \tfrac{1}{k!} T(\underset{k\,\text{args}}{\underbrace{L \cdots L}})$:

$$
  S(L)^{-1}
  =
  \underset{k \in \mathbb{N}}{\sum} \tfrac{1}{k!} \overline{T}( \underset{k \, \text{args}}{\underbrace{L \cdots L}} )
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition we have

$$
  \underset{k \in \mathbb{N}}{\sum}
    \tfrac{1}{k!}
    \overline{T}( \underset{k \, \text{args}}{\underbrace{L \cdots L}} )
  =
  \underset{ k \in \mathbb{N}}{\sum}
    \tfrac{1}{k!}
    \underoverset{r = 1}{k}{\sum}
    (-1)^r
    \underset{\sigma \in Unshuffl(k,r)}{\sum}
    T( L_{\sigma(1)} \cdots L_{\sigma(k_1)} )
    T( L_{\sigma(k_1 + 1)} \cdots L_{\sigma(k_2)} )
    \cdots
    T( L_{\sigma(k_{r-1}+1)} \cdots L_{\sigma_{k_r}} )
$$

where $\underset{k \in \{1 , \cdots, n\}}{\forall} L_k \coloneqq L$.

If instead of unshuffles (i.e. partitions into non-empty subsequences preserving the original order) we took
partitions into arbitrarily ordered subsequences,
we would be overcounting by the factorial of the length of the subsequences, and hence the
above may be equivalently written as:

$$
  \cdots
  =
  \underset{k \in \mathbb{N}}{\sum}
    \tfrac{1}{k!}
    \underoverset{r = 1}{k}{\sum}
    (-1)^r
    \underset{ {\sigma \in \Sigma(k)} \atop { { k_1 + \cdots + k_r = k } \atop { \underset{i}{\forall} (k_i \geq 1) } } }{\sum}
    \tfrac{1}{k_1!} \cdots \tfrac{1}{k_r !}
    \,
    T( L_{\sigma(1)} \cdots L_{\sigma(k_1)} )
    \,
    T( L_{\sigma(k_1 + 1)} \cdots L_{\sigma(k_2)} )
    \cdots
    T( L_{\sigma(k_{r-1}+1)} \cdots L_{\sigma_{k_r}} )
    \,,
$$

where $\Sigma(k)$ denotes the [[symmetric group]] (the collection of all [[permutations]] of $k$ elements).

Moreover, since all the $L_k$ are equal, the sum is in fact independent of $\sigma$, it only depends
on the length of the subsequences. Since there are $k!$ permutations of $k$ elements
the above reduces to

$$
  \begin{aligned}
    \cdots
    & =
    \underset{k \in \mathbb{N}}{\sum}
      \underoverset{r = 1}{k}{\sum}
      (-1)^r
      \underset{  k_1 + \cdots + k_r = k }{\sum}
      \tfrac{1}{k_1!} \cdots \tfrac{1}{k_r !}
      T( \underset{k_1 \, \text{factors}}{\underbrace{ L \cdots L }}  )
      T( \underset{k_2 \, \text{factors}}{\underbrace{ L \cdots L }}  )
      \cdots
      T( \underset{k_r \, \text{factors}}{\underbrace{ L \cdots L }}  )
    \\
    & =
      \underoverset{\infty}{r = 0}{\sum}
      \left(
        - \underoverset{k = 0}{\infty}{\sum} T ( \underset{k\,\text{factors}}{\underbrace{L \cdots L}}   )
      \right)^r
    \\
    & =
      S(L)^{-1}
      \,,
  \end{aligned}
$$

where in the last line we used (eq:InfverseOfPerturbativeSMatrix).


=--

In fact prop. \ref{ReverseTimOrderedProductsGiveReverseSMatrix} is a special case of the
following more general statement:

+-- {: .num_prop #InversionFormulaForTimeOrderedProducts}
###### Proposition
**(inversion relation for reverse-time ordered products)

Let $\{T_k\}_{k \in \mathbb{N}}$ be [[time-ordered products]] according to def. \ref{TimeOrderedProduct}.
Then the reverse-time ordered products according to def. \ref{ReverseTimeOrderedProduct}
satisfies the following inversion relation for all $\mathbf{X} \neq \emptyset$
(in the condensed notation of def. \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions})

$$
  \underset{\mathbf{J} \subset \mathbf{X}}{\sum}
    T(\mathbf{J}) \overline{T}(\mathbf{X} \setminus \mathbf{J})
  \;=\;
  0
$$

and

$$
  \underset{\mathbf{J} \subset \mathbf{X}}{\sum}
    \overline{T}(\mathbf{X} \setminus \mathbf{J})  T(\mathbf{J})
  \;=\;
  0
$$

=--

+-- {: .proof}
###### Proof

This is immediate from unwinding the definitions.


=--

+-- {: .num_prop #ReverseCausalFactorizationOfReverseTimeOrderedProducts}
###### Proposition
**(reverse [[causal factorization]] of reverse-time ordered products)**

Let $\{T_k\}_{k \in \mathbb{N}}$ be [[time-ordered products]] according to def. \ref{TimeOrderedProduct}.
Then the reverse-time ordered products according to def. \ref{ReverseTimeOrderedProduct} satisfies
reverse-[[causal factorization]].

=--

([Epstein-Glaser 73, around (15)](#EpsteinGlaser73))

+-- {: .proof}
###### Proof

In the condensed notation of def. \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions},
we need to show that for $\mathbf{X} = \mathbf{P} \cup \mathbf{Q}$ with $\mathbf{P} \cap \mathbf{Q} = \emptyset$
then

$$
  \left(
    \mathbf{P} \geq \mathbf{Q}
  \right)
  \;\Rightarrow\;
  \left(
    \overline{T}(\mathbf{X})
     =
    \overline{T}(\mathbf{Q}) \overline{T}(\mathbf{P})
  \right)
  \,.
$$

We proceed by [[induction]]. If ${\vert \mathbf{X}\vert} = 1$ the statement is immediate.
So assume that the statement is true for sets of [[cardinality]] $n \geq 1$ and consider
$\mathbf{X}$ with ${\vert \mathbf{X}\vert} = n+1$.

We make free use of the condensed notation as in example \ref{ProductOfPerturbationSeriesInGenealizedFunctionNotation}.

From the formal inversion

$$
  \underset{\mathbf{J} \subset \mathbf{X}}{\sum} \overline{T}(\mathbf{J}) T(\mathbf{X}\setminus \mathbf{J})
  = 0
$$

(which uses the induction assumption that ${\vert \mathbf{X}\vert} \geq 1$) it follows that

$$
  \begin{aligned}
    \overline{T}(\mathbf{X})
      & =
    - \underset{ { \mathbf{J} \subset \mathbf{X} } \atop { \mathbf{J} \neq \mathbf{X} }  }{\sum}
     \overline{T}(\mathbf{J}) T( \mathbf{X} \setminus \mathbf{J} )
     \\
     & =
    - \underset{
        { \mathbf{J} \cup \mathbf{J}' = \mathbf{X} }
        \atop
        {
          { \mathbf{J} \cap \mathbf{J}' = \emptyset }
          \atop
          { \mathbf{J}' \neq \emptyset }
        }
     }{\sum}
     \overline{T}( \mathbf{Q} \cap \mathbf{J} )
     \overline{T}( \mathbf{P} \cap \mathbf{J} )
               T ( \mathbf{P} \cap ( \mathbf{J}' ) )
               T ( \mathbf{Q} \cap ( \mathbf{J}' ) )
     \\
     & =
    - \underset{
      { \mathbf{L} \cup \mathbf{L}' = \mathbf{Q} \,,\, \mathbf{L} \cap \mathbf{L}' = \emptyset }
      \atop
      { \mathbf{L}' \neq \emptyset }
    }{\sum}
     \overline{T}( \mathbf{L} )
     \underset{ = 0}{
       \underbrace{
         \left(
          \underset{
              \mathbf{K} \subset \mathbf{P}
           }{\sum}
           \overline{T}( \mathbf{K} ) T( \mathbf{P} \setminus \mathbf{K})
         \right)
       }
     }
     T(\mathbf{L'})
    -
    \overline{T}(\mathbf{Q})
    \underset{
      = - \overline{T}(\mathbf{P})
    }{
    \underbrace{
      \underset{
        {\mathbf{K} \subset \mathbf{P}}
        \atop
        { \mathbf{K} \neq \emptyset }
      }{\sum}
      \overline{T}(\mathbf{K})
                T (\mathbf{P} \setminus \mathbf{K} )
    }}
    \\
    & =
    \overline{T}(\mathbf{Q}) \overline{T}(\mathbf{P})
  \end{aligned}
   \,.
$$

Here

1. in the second line we used that $\mathbf{X} = \mathbf{Q} \sqcup \mathbf{P}$, together with the
causal factorization property of $T(-)$ (which holds by general assumption) and that of $\overline{T}(-)$
(which holds by the induction assumption, using that $\mathbf{J} \neq \mathbf{X}$ hence that
${\vert \mathbf{J}\vert} \lt {\vert \mathbf{X}\vert}$).

1. in the third line we decomposed the sum over $\mathbf{J}, \mathbf{J}' \subset \mathbf{X}$
into two sums over subsets of $\mathbf{Q}$ and $\mathbf{P}$:

   1. The first summand in the third line is the contribution where $\mathbf{J}'$ has a non-empty intersection with $\mathbf{Q}$. This makes $\mathbf{K}$ range without constraint, and therefore the sum in the middle vanishes, as indicated, as it is the contribution at order ${\vert \mathbf{Q}\vert}$ of the inversion formula from prop. \ref{InversionFormulaForTimeOrderedProducts}

   1. The second summand in the third line is the contribution where $\mathbf{J}'$ does not intersect $\mathbf{Q}$.
     Now the sum over $\mathbf{K}$ is the inversion formula from prop. \ref{InversionFormulaForTimeOrderedProducts} except for one term, and so it equals that term.

=--

Using these facts about the reverse-time ordered products,
we may finally prove that [[time-ordered products]] indeed do induced a perturbative S-matrix:

+-- {: .num_prop #TimeOrderedProductInducesPerturbativeSMatrix}
###### Proposition
**([[time-ordered products]] induce perturbative S-matrix)**

Let $\{T_k\}_{k \in \mathbb{N}}$ be a system of [[time-ordered products]] according to def. \ref{TimeOrderedProduct}.
Then

$$
  \begin{aligned}
    S(-)
    & \coloneqq
    T \exp\left(
      \tfrac{1}{i \hbar}(-)
      \right)
    \\
    &
    \coloneqq \underset{k \in \mathbb{N}}{\sum} \tfrac{1}{(i \hbar)^k} \tfrac{1}{k!} T( \underset{k \, \text{factors}}{\underbrace{- \cdots -}} )
  \end{aligned}
$$

is indeed a perturbative S-matrix according to def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}.

=--

+-- {: .proof}
###### Proof

The axiom "perturbation" and "normalization" for the S-matrix are
immediate from the corresponding axioms of the time-ordered products.
What requires proof is that [[causal additivity]] of the S-matrix follows from
the causal factorization property of the time-ordered products.

Notice that also the simple causal factorization property of the S-matrix

$$
  (supp(g_{sw_1}L_1) \geq supp(g_{sw,}L_2))
    \;\Rightarrow\;
  \left(
    S(g_{sw,1}L_1 + g_{sw,2}L_2)
    =
    S(g_{sw,1}L_1) S(g_{sw,2}L_2)
  \right)
$$

is immediate from the time-ordering axiom of the time-ordered products.

But [[causal additivity]] is stronger. It is remarkable that this, too,
follows from just the time-ordering ([Epstein-Glaser 73, around (73)](#EpsteinGlaser73)):

To see this, first expand the
generating functional $Z$ (eq:GeneratingFunctionInducedFromSMatrix)  into
powers of $(g/\hbar)$ and $(j/\hbar)$

$$
  Z_{L}(L + A)
  \;=\;
  \underoverset{n,m = 0}{\infty}{\sum}
   \frac{1}{n! m!}
   R(  \underset{n\, \text{factors}}{\underbrace{L \cdots L}},  ( \underset{m \, \text{factors}}{ \underbrace{ A \cdots A } }  ) )
$$

and then compare order-by-order with the given time-ordered product $T$ and
its induced reverse-time ordered product (def. \ref{ReverseTimeOrderedProduct}) via prop. \ref{ReverseTimOrderedProductsGiveReverseSMatrix}.
(These $R(-,-)$ are also called the "generating [[retarded products]], discussed in their own right around def. \ref{RetardedProductFromPerturbativeSMatrix} below.)

In the condensed notation of
def. \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}
and its way of absorbing combinatorial prefactors as in example \ref{ProductOfPerturbationSeriesInGenealizedFunctionNotation}
this
yields at order $(g/\hbar)^{\vert \mathbf{Y}\vert} (j/\hbar)^{\vert \mathbf{X}\vert}$ the coefficient

$$
  \label{CoefficientOfgeneratingRetardedProduct}
  R(\mathbf{Y}, \mathbf{X})
   \;=\;
  \underset{\mathbf{I} \subset \mathbf{Y}}{\sum}
    \overline{T}(\mathbf{I})
    T( (\mathbf{Y} \setminus \mathbf{I}) , \mathbf{X} )
  \,.
$$

We claim now that the [[support of a distribution|support]] of $R$ is inside the subset for which
$\mathbf{Y}$ is in the [[causal past]] of $\mathbf{X}$. This will imply the claim, because by
multi-linearity of $R(-,-)$ it then follows that

$$
  \left(J_1 \geq J_2\right) \Rightarrow \left( Z_{L + J_1}(J_2) = Z_L(J_2) \right)
$$

and by lemma \ref{CausalLocalityOfThePerturbativeSMatrix} this is equivalent to [[causal additivity]] of the S-matrix.

It remains to prove the claim:

Consider $\mathbf{X}, \mathbf{Y} \subset \Sigma$ such that the subset $\mathbf{P} \subset \mathbf{Y}$
of points not in the past of $\mathbf{X}$ (def. \ref{CausalOrdering}), hence the maximal subset with

$$
  \mathbf{P} \geq \mathbf{X}
  \,,
$$

is non-empty. We need to show that in this case $R(\mathbf{Y}, \mathbf{X}) = 0$ (in the sense of generalized functions).

Write $\mathbf{Q} \coloneqq \mathbf{Y} \setminus \mathbf{P}$
for the complementary set of points, so that all points of $\mathbf{Q}$ are in the past of $\mathbf{X}$.
Notice that this implies that $\mathbf{P}$ is also not in the past of $\mathbf{Q}$:

$$
  \mathbf{P} \geq \mathbf{Q}
  \,.
$$

With this decomposition of $\mathbf{Y}$, the sum in (eq:CoefficientOfgeneratingRetardedProduct)
over subsets $\mathbf{I}$ of $\mathbf{Y}$ may be decomposed into a sum over
subsets $\mathbf{J}$ of $\mathbf{P}$ and $\mathbf{K}$ of $\mathbf{Q}$, respectively.
These subsets inherit the above causal ordering, so that by the causal factorization property of
$T(-)$ (def. \ref{TimeOrderedProduct}) and $\overline{T}(-)$ (prop. \ref{ReverseCausalFactorizationOfReverseTimeOrderedProducts})
the time-ordered and reverse time-ordered products
factor on these arguments:

$$
  \begin{aligned}
    R(\mathbf{Y}, \mathbf{X})
    & =
    \underset{ {\mathbf{J} \subset \mathbf{P}} \atop { \mathbf{K} \subset \mathbf{Q} } }{\sum}
     \,
     \overline{T}( \mathbf{J} \cup \mathbf{K} )
     T( (\mathbf{P} \setminus \mathbf{J}) \cup (\mathbf{Q} \setminus \mathbf{K}), \mathbf{X} )
     \\
     & =
     \underset{ {\mathbf{J} \subset \mathbf{P}} \atop { \mathbf{K} \subset \mathbf{Q} } }{\sum}
     \,
     \overline{T}( \mathbf{K} )
     \overline{T}( \mathbf{J} )
     T( \mathbf{P} \setminus \mathbf{J} )
     T( \mathbf{Q} \setminus \mathbf{K}, \mathbf{X} )
     \\
     & =
     \underset{ \mathbf{K} \subset \mathbf{Q} }{\sum}
     \overline{T}(\mathbf{K})
     \underset{= 0}{
     \underbrace{
     \left(
       \underset{\mathbf{J} \subset \mathbf{P}}{\sum}
       \overline{T}(\mathbf{J})
       T( \mathbf{P} \setminus \mathbf{J} )
     \right)
     }}
     T(\mathbf{Q} \setminus \mathbf{K}, \mathbf{X})
  \end{aligned}
  \,.
$$

Here the sub-sum in brackets vanishes by the inversion formula, prop. \ref{InversionFormulaForTimeOrderedProducts}.

=--

$\,$

#### Quantum observables and Retarded products
 {#QuantumObservables}

A genuine local [[observable]] should depend on the values of the [[fields]] on some [[compact subset]]
of spacetime. Moreover, a perturbative [[quantum observable]] should be a [[power series]] in [[Planck's constant]] $\hbar$,
reducing to the corresponding classical observable at $\hbar = 0$. The perturbative S-matrix axiomatized [above](#PerturbativeSMatrixAndTimeOrderedProducts)
is neither localized in spacetime this way, nor is it a power series in $\hbar$ (it is a [[Laurent series]] in $\hbar$).
So it is not a local observable. But the actual [[quantum observables on interacting fields]] may be expressed in terms of the S-matrix
by [[Bogoliubov's formula]] (def. \ref{GeneratingFunctionsForCorrelationFunctions} below).

This formula is consistent in that it implies that local observables form a [[causally local net]]
as their spacetime support varies (this is prop. \ref{PerturbativeQuantumObservablesIsLocalnet} below).
(On deeper grounds, this formula
turns out to yield the [[formal deformation quantization|formal]] [[Fedosov deformation quantization]] of
the interacting field theory ([Collini 16](#Collini16)).)


Namely a key consequence of the "[[causal additivity]]" axiom on the S-matrix in def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}
turns out to be that the perturbative [[quantum observables on interacting fields]] with compact spacetime support (def. \ref{GeneratingFunctionsForCorrelationFunctions})

1. depend on the [[adiabatic switching]] $g_{sw}$ of the [[interaction]] [[Lagrangian density]]
only up to _canonical_ unitary [[isomorphism]] (lemma \ref{CausalLocalityOfThePerturbativeSMatrix} below)

1. form a [[causal locality|causally]] [[local net of observables]] in the sense of the [[Haag-Kastler axioms]] as the spacetime localization varies (prop. \ref{PerturbativeQuantumObservablesIsLocalnet} below).

To the extent that a [[local net of observables]] may be regarded as _defining_ a [[quantum field theory]],
which is the claim of ([[perturbative AQFT|perturbative]]) [[AQFT]],
this proves that the perturbative S-matrices in [[causal perturbation theory]] as in def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}
indeed make sense, despite the involvement of [[adiabatic switching]] of the [[interaction]] [[Lagrangian density]]
which does not make physical sense when interpreted naively: In reality the interaction is of course not (for realistic [[theory (physics)|theories]] at least) "switched off" outside some bounded region of spacetime; but the result here shows that if we pretend that it does
then first of all we get consistent mathematical formulas and moreover we can then nevertheless compute the correct [[quantum observables]] that are localized in this spacetime region. But the [[local net of observables]] as the spacetime localization varies
is supposed to encode the full quantum field theory. Certainly any given [[experiment]] in practice probes a bounded spacetime
region, and hence the algebra of observables localized in this region is sufficient to compare the theory to experiment.


$\,$


+-- {: .num_defn #GeneratingFunctionsForCorrelationFunctions}
###### Definition
**(perturbative [[quantum observables on interacting fields]] via [[Bogoliubov's formula]])**

Let $S$ be a perturbative S-matrix as in def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime},
and $g_{sw} L_{int} \in \mathcal{F}_{loc}\langle g\rangle$ an [[adiabatic switching|adiabatically switched]]
[[interaction]] [[Lagrangian density]].

Then for $A \in \mathcal{F}_{loc}$ a [[local observable]], the perturbative
[[quantum observable]] $\widehat{A}$ corresponding to $A$ is the [[operator-valued distribution]]

$$
  \widehat{A}
  \;\colon\;
  C^\infty_{cp}(\Sigma)
    \longrightarrow
  \mathcal{W}[ [ g ] ][ [ \hbar ] ]
$$

which is the [[derivative]] of the generating functional $Z$ ((eq:GeneratingFunctionInducedFromSMatrix) in def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}) at vanishing [[source field]]:

$$
  \widehat{A}(j)
    \;\coloneqq\;
  - i \hbar \frac{d}{d \epsilon} Z_{g_{sw} L_{int}}( \epsilon j  A)\vert_{\epsilon = 0}
  \,.
$$


=--

This definition of $\widehat{A}$ without the [[adiabatic switching]] $g_{sw}$ is originally due to [Bogoliubov-Shirkov 59](#BogoliubovShirkov59), nowadays sometimes called _[[Bogoliubov's formula]]_ (e.g. [Rejzner 16 (6.12)](#Rejzner16)).
The version with adiabatic switching is due to ([Epstein-Glaser 73 around (74)](#EpsteinGlaser73)).
Review includes ([D&#252;tsch-Fredenhagen 00, around (17)](#DuetschFredenhagen00)).


+-- {: .num_remark }
###### Remark
**(interpretation of Bogoliubov's formula in terms of the path integral

With the perturbative S-matrix informally thought of as a path integral as in
remark \ref{InterpretationOfPerturbativeSMatrix}

$$
  S(\tfrac{g}{\hbar} L_{int} + j A)
    \;\overset{\text{not really!}}{=}\;
  \int
  \exp\left(
    \int_X
    \left(
      \tfrac{g}{i \hbar} L_{int}(\Phi) + j A(\Phi)
    \right)
  \right)  e^{\tfrac{1}{i \hbar}\int_X L_{free}(\Phi) }D[\Phi]
$$

the [[Bogoliubov formula]] in def. \ref{GeneratingFunctionsForCorrelationFunctions}
simimlarly would have the following interpretation:


$$
  \widehat A(j)
  \;\overset{\text{not really!}}{=}\;
  \frac{
    \int
    j A(\Phi)
    \exp\left(
      \int_X
      \left(
        \tfrac{g}{i \hbar} L_{int}(\Phi)
      \right)
    \right)  e^{\tfrac{1}{i \hbar}\int_X L_{free}(\Phi) }D[\Phi]
  }
  {
    \int
    \exp\left(
      \int_X
      \left(
        \tfrac{g}{i \hbar} L_{int}(\Phi)
      \right)
    \right)  e^{\tfrac{1}{i \hbar}\int_X L_{free}(\Phi) }D[\Phi]
  }
$$

If here we were to regard the expression

$$
  \mu(\Phi)
  \;\overset{\text{not really}}{\coloneqq}\;
  \frac{
    \exp\left(
      \int_X
      \left(
        \tfrac{g}{i \hbar} L_{int}(\Phi)
      \right)
    \right)  e^{\tfrac{1}{i \hbar}\int_X L_{free}(\Phi) }D[\Phi]
  }
  {
    \int
    \exp\left(
      \int_X
      \left(
        \tfrac{g}{i \hbar} L_{int}(\Phi)
      \right)
    \right)  e^{\tfrac{1}{i \hbar}\int_X L_{free}(\phi) }D[\phi]
  }
$$

as a "complex probability measure" on the the configuration space of fields, then this formula
would express the [[expectation value]] of the functional $A$ under this measure:

$$
  \widehat{A}(j) \overset{\text{not really!}}{=} [j A]_{\mu} = \int j A(\Phi) \mu(\Phi)
  \,.
$$

=--

The power series coefficients of the [[quantum observables on interacting fields]]
are also called the _[[retarded products]]_. For the time being we mention these here
just for completeness:

+-- {: .num_defn #RetardedProductFromPerturbativeSMatrix}
###### Definition
**([[retarded products]] induced from perturbative S-matrix)

It follows from the perturbation axiom in def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime} that there is a system of [[continuous linear functionals]]

$$
  R
    \;\colon\;
  \left(\mathcal{F}_{loc}\langle g\rangle\right)^{\otimes^k}
    \otimes
  (\mathcal{F}_{loc})^{\otimes^l}
    \longrightarrow
  \mathcal{W}[ [ g/\hbar] ] [ [ j/\hbar] ]
$$

for all $k,l \in \mathbb{N}$ such that

$$
  Z_{g_{sw} L}(j_{sw} A)
  =
  \underset{k,l \in \mathbb{N}}{\sum} \frac{1}{k! l!}
  R(
    \underset{k \,\text{arguments}}{\underbrace{ g_{sw} L \cdots g_{sw} L } },
    \underset{l \; \text{arguments}}{\underbrace{ j_{sw} A \cdots j_{sw} A }}
  )
  \,.
$$

Similarly there is

$$
  R
    \;\colon\;
  \left(\mathcal{F}_{loc}\langle g \rangle\right)^{\otimes^k}
    \otimes
  \left(\mathcal{F}_{loc}\langle j \rangle\right)
    \longrightarrow
  \mathcal{W}[ [ g ] ] [ [ \hbar ] ]
$$

such that

$$
  \widehat{A}(h)
  =
  \underset{k \in \mathbb{N}}{\sum} \frac{1}{k!}
  r( \underset{k \,\text{arguments}}{\underbrace{g_{sw}L_{int} \cdots g_{sw}L_{int}}}, h A )
  \,.
$$

These are called the (generating) _[[retarded products]]_ ([Glaser-Lehmann-Zimmermann 57](#GlaserLehmannZimmermann57), [Epstein-Glaser 73, section 8.1](#EpsteinGlaser73)).

=--

Direct axiomatization of the [[retarded products]] is due to ([D&#252;tsch-Fredenhagen 04](#DuetschFredenhagen04)),
see ([Collini 16, section 2.2](#Collini16)).

$\,$

It is useful now to reformulate the [[causal additivity]]-property of the perturbative S-matrix
in terms of the generating functions / [[retarded products]]:

+-- {: .num_lemma #CausalLocalityOfThePerturbativeSMatrix}
###### Lemma
**(causal locality of the perturbative S-matrix)**

Let $S$ be a perturbative S-matrix according to def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}
with $Z$ the generating functional (eq:GeneratingFunctionInducedFromSMatrix) it induces

1. The following conditions are equivalent for all $L, J_1, J_2 \in \mathcal{F}_{loc}$:

   1. $Z_L(J_1 + J_2) = Z_L(J_1) Z_L(J_2)$

   1. $Z_{L + J_1}(J_2) = Z_L(J_2)$

   1. $S(L + J_1 + J_2) = S(L + J_1) \, S(L)^{-1} \, S(L + J_2)$

   Hence causal additivity in def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}
implies that all these conditions hold if $supp(J_1) \geq supp(J_2)$.


1. If $supp(J_1)$ is [[spacelike]] separted from $supp(J_1)$, hence if the causal ordering (def \ref{CausalOrdering}) is
   $supp(J_1) \geq supp(J_2)$ and $supp(J_2) \geq supp(J_1)$ then

   $$
     Z_{L_{int}}(J_1) Z_{L_{int}}(J_2) = Z_{L_{int}}(J_2) J_{L_{int}}(J_1)
     \,.
   $$


   Similarly, if $supp(L_1) \geq supp(L_2)$ and $supp(L_2) \geq supp(L_1)$ then

   $$
     S(L_1) \, S(L_2) = S(L_2) \, S(L_1)
     \,.
   $$



1. If $L_1\vert_{O} = L_2\vert_{O}$ on a [[causally closed subset]] $O \subset \mathbb{R}^{d-1,1}$
then there exists an invertible $K \in \mathcal{W}[ [ g/\hbar] ]$ such that for all $J$ with $supp(J) \subset O$
   it relates $Z_{L_1}(J)$ to $Z_{L_2}(J)$ by [[conjugation]]:

   $$
     Z_{L_2}(J) = K^{-1} \, Z_{L_1}(J) \, K
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

Now the first clause of the first item immediately implies the first clause of the second item.

Similarly, setting $L = 0$ and $J_1 = L_1$ and $J_2 = L_2$ in the third clause of the first item it
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

which is the second clause of the second statement to be shown.


For the last statement, notice that by causal closure of
$O$ the difference $L_2 - L_2$, which by assumption has
$supp(L_2 - L_1) \in X \setminus O$,
may, according to lemma \ref{CausalPartition}, be written as

$$
  L_2 - L_1 = a + r
$$

such that their causal order (def. \ref{CausalOrdering}) is

$$
  supp(a) \geq supp(J) \geq supp(r)
$$

It follows with causal additivity and its equivalent formulations above that

$$
  \begin{aligned}
    Z_{L_2}(J)
      & =
    Z_{L_1 + a + r}(J)
    \\
      & =
    Z_{L_1 + r}(J)
    \\
      & =
    S(L_1 + r)^{-1} \, S(L_1 + r + J)
    \\
      & =
    S(L_1 + r)^{-1} \, S(J + L_1) \, S(L_1)^{-1} \, S(L_1 + r)
    \\
      & =
    S(L_1 + r)^{-1} \underset{= id}{\underbrace{S(L_1) S(L_1)^{-1}}} S(L_1 + J) \, S(L_1)^{-1} \, S(L_1 + r)
    \\
      & =
    Z_{L_1}(r)^{-1} \, Z_{L_1}(J) \, Z_{L_1}(r)
  \end{aligned}
$$

and hence the last statement holds for $K \coloneqq Z_{L_1}(r)$.

=--

We now use this fact (lemma \ref{CausalLocalityOfThePerturbativeSMatrix}) to neatly organize the
system of localized [[quantum observables on interacting fields]]:

+-- {: .num_defn #PerturbativeGeneratingLocalNetOfObservables}
###### Definition
**(system of perturbative generating [[algebras of observables]])

Let $S$ be a perturbative S-matrix according to def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}
and let $L_{int} \in \Omega^{d,0}(E)$ be an [[interaction]] [[Lagrangian density]].


For $\mathcal{O} \subset \Sigma$ a [[causally closed subset]] of [[spacetime]]
(def. \ref{CausalComplementOfSubsetOfLorentzianManifold})
and for $g_{sw} \in Cutoffs(\mathcal{O})$ an [[adiabatic switching]] function (def. \ref{CutoffFunctions})
which is constant on a [[neighbourhood]] of $\mathcal{O}$, write

$$
  Gen_{g_{sw} L_{int}}(\mathcal{O})
   \coloneqq
  \left\langle
    Z_{g_{sw}L_{int}}(J) \;\vert\; supp(J) \subset \mathcal{O}
  \right\rangle
   \;\subset\;
  \mathcal{W}[ [ g/\hbar] ]
$$

for the smallest subalgebra of the [[Wick algebra]] which contains the
generating functions for correlation functions  (def. \ref{GeneratingFunctionsForCorrelationFunctions})
of the form $Z_{g_{sw}L_{int}}(J)$, for all those [[local observables]] $J \in \mathcal{F}_{loc}$ with $supp(J) \subset \mathcal{O}$.

Moreover, write

$$
  Gen_{L_{int}}(\mathcal{O})
    \;\subset\;
  \underset{g_{sw} \in Cutoffs(\mathcal{O})}{\prod} Gen_{g_{sw}L_{int}}(\mathcal{O})
$$

be the subalgebra of the [[Cartesian product]] of all these algebras as $g_{sw}$ ranges, which is generated by the
[[tuples]]

$$
  Z_{L_{int}}(J)
    \;\coloneqq\;
  \left(
     Z_{g_{sw}L_{int}} (J)
  \right)_{g_{sw} \in Cutoffs(\mathcal{O})}
$$

for $J$ with $supp(J) \subset \mathcal{O}$.

Finally, for $\mathcal{O}_1 \subset \mathcal{O}_2$ an inclusion of two [[causally closed subsets]], let

$$
  i_{\mathcal{O}_1, \mathcal{O}_2}
  \;\colon\;
  Gen_{L_{int}}(\mathcal{O}_1)
    \longrightarrow
  Gen_{L_{int}}(\mathcal{O}_2)
$$

be the algebra [[homomorphism]] which is given simply by restricting the index set of [[tuples]].

This construction defines a [[functor]]

$$
  Gen_{L_{int}} \;\colon\; CausClsdSubsets(\Sigma) \longrightarrow StarAlgebras
$$

from the [[poset]] of [[causally closed subsets]] of [[spacetime]] to the [[category]] of [[star algebras]].


=--

([Brunetti-Fredenhagen 99, (65)-(67)](#BrunettiFredenhagen99))

+-- {: .num_remark}
###### Remark
**([[algebra of observables]] well defined up to canonical [[isomorphism]])**

By lemma \ref{CausalLocalityOfThePerturbativeSMatrix},
for every causally closed $\mathcal{O} \subset X$ and every $g_{sw} \in Cutoffs(\mathcal{O})$
the abstract algebra $Gen_{L_{int}}(\mathcal{O})$ from def. \ref{CausalLocalityOfThePerturbativeSMatrix}
is _canonically_ isomorphic to the subalgebra $Gen_{g_{sw}L_{int}}(\mathcal{O}) \subset \mathcal{W}[ [ g/\hbar ] ] $
of formal power series in the [[Wick algebra]].

Beware the slight subtlety in this statement:

The unitary elements $K$ in $\mathcal{W}[ [ g/\hbar] ]$ which exhibit the isomorphisms by [[conjugation]] are not
unique, since there are many choices of splittings $g_2 - g_1 = a + r$ in the proof of prop. \ref{CausalLocalityOfThePerturbativeSMatrix}.
But the induced isomorphisms between the algebras generated by the $Z_{L_{int}}(J)$ is independent
of this ambiguity, since, again by the proof of prop. \ref{CausalLocalityOfThePerturbativeSMatrix},
conjugation by each such $K$ gives the same result on the given generators: $Z_{g_1 L_{int}}(J) \mapsto Z_{g_2 L_{int}}(J)$.

=--

+-- {: .num_prop #GeneratingAlgebrasIsLocalNet}
###### Proposition
**(system of perturbative generating algebras is [[causally local net of observables]])**

Given a perturbative S-matrix according to def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}
and an interaction [[Lagrangian density]] $L_{int}$, then the system of generating algebras of observables $Gen_{L_{int}}$ (def. \ref{PerturbativeGeneratingLocalNetOfObservables})
is a [[causally local net of observables]] in that

1. (isotony) For every inclusion $\mathcal{O}_1 \subset \mathcal{O}_2$ of [[causally closed subsets]]
   the corresponding
   algebra homomorphism is a [[monomorphism]]

   $$
     i_{\mathcal{O}_1, \mathcal{O}_2}
     \;\colon\;
     Gen_{L_{int}}(\mathcal{O}_1) \hookrightarrow Gen_{L_{int}}(\mathcal{O}_2)
   $$

1. ([[causal locality]]) For $\mathcal{O}_1, \mathcal{O}_2 \subset X$ two [[causally closed subsets]]
   which are [[spacelike]] separated, in that their causal ordering (def. \ref{CausalOrdering}) satisfies

   $$
     \mathcal{O}_1 \geq \mathcal{O}_2
       \;\text{and}\;
     \mathcal{O}_2 \geq \mathcal{O}_1
   $$

   then for $\mathcal{O} \subset X$ any further causally closed subset which contains both

   $$
     \mathcal{O}_1 , \mathcal{O}_2 \subset \mathcal{O}
   $$

   then the corresponding images of the generating algebras of $\mathcal{O}_1$ and $\mathcal{O}_2$,
   respectively, commute with each other as subalgebras of the generating algebra of $\mathcal{O}$:

   $$
     \left[
       i_{\mathcal{O}_1,\mathcal{O}}(Gen_{L_{int}}(\mathcal{O}_1))
       \;,\;
       i_{\mathcal{O}_2,\mathcal{O}}(Gen_{L_{int}}(\mathcal{O}_2))
     \right]
     \;=\;
     0
     \;\;\;
     \in Gen_{L_{int}}(\mathcal{O})
     \,.
   $$


=--

([D&#252;tsch-Fredenhagen 00, section 3](#DuetschFredenhagen00), following [Brunetti-Fredenhagen 99, section 8](#BrunettiFredenhagen99),
[Il'in-Slavnov 78](#IlinSlavnov78))

+-- {: .proof}
###### Proof

Isotony is immediate from the definition of the algebra homomorphisms in def. \ref{PerturbativeGeneratingLocalNetOfObservables}.

Causal locality of the system of observables follows from the causal additivity of the S-matrix,
by the first clause in the second statement of lemma \ref{CausalLocalityOfThePerturbativeSMatrix}.

=--

In the same kind of way as def. \ref{PerturbativeGeneratingLocalNetOfObservables} the actual net of algebra
of perturbative [[quantum observables]] (def. \ref{GeneratingFunctionsForCorrelationFunctions}) is defined:

+-- {: .num_defn #SystemOfAlgebrasOfQuantumObservables}
###### Definition
**(system of [[algebras of quantum observables]])

Let $S$ be a perturbative S-matrix according to def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}
and let $L_{int} \in \Omega^{d,0}(E)$ be an [[interaction]] [[Lagrangian density]].


For $\mathcal{O} \subset \Sigma$ a [[causally closed subset]]
of [[spacetime]] (def. \ref{CausalComplementOfSubsetOfLorentzianManifold})
and for $g_{sw} \in Cutoffs(\mathcal{O})$ an compatible [[adiabatic switching]] function (def. \ref{CutoffFunctions}) write

$$
  Obs_{g_{sw} L_{int}}(\mathcal{O})
   \coloneqq
  \left\langle
     -i \frac{d}{d \epsilon} Z_{g_{sw}L_{int}}(\epsilon J)\vert_{\epsilon = 0} \;\vert\; supp(J) \subset \mathcal{O}
  \right\rangle
   \;\subset\;
  \mathcal{W}[ [ g ] ] [ [ \hbar ]  ]
$$

for the smallest subalgebra of the [[Wick algebra]] which contains the
perturbative [[quantum observables on interacting fields]]  (def. \ref{GeneratingFunctionsForCorrelationFunctions}) supported in $\mathcal{O}$.

Moreover, let

$$
  Obs_{L_{int}}(\mathcal{O})
    \subset
  \underset{g_{sw} \in Cutoffs(\mathcal{O})}{\prod} Obs_{g_{sw}L_{int}}(\mathcal{O})
$$

be the subalgebra of the [[Cartesian product]] of all these algebras as $g_{sw}$ ranges, which is generated by the
[[tuples]]

$$
  -i \hbar \frac{d}{d \epsilon} Z_{L_{int}}(\epsilon J)\vert_{\epsilon = 0}
    \;\coloneqq\;
  \left(
      - i \hbar \frac{d}{d \epsilon} Z_{g_{sw}L_{int}} (\epsilon J)\vert_{\epsilon = 0}
  \right)_{g_{sw} \in Cutoffs(\mathcal{O})}
$$

for $J$ with $supp(J) \subset \mathcal{O}$.

Finally, for $\mathcal{O}_1 \subset \mathcal{O}_2$ an inclusion of two [[causally closed subsets]], let

$$
  i_{\mathcal{O}_1, \mathcal{O}_2}
  \;\colon\;
  Obs_{L_{int}}(\mathcal{O}_1)
    \longrightarrow
  Obs_{L_{int}}(\mathcal{O}_2)
$$

be the algebra [[homomorphism]] which is given simply by restricting the index set of [[tuples]].

This construction defines a [[functor]]

$$
  Obs_{L_{int}} \;\colon\; CausClsdSubsets(\Sigma) \longrightarrow StarAlgebras
$$

from the [[poset]] of [[causally closed subsets]] in the [[spacetime]] $\Sigma$ to the [[category]] of [[star algebras]].

=--

As a corollary of prop. \ref{GeneratingAlgebrasIsLocalNet} we then have the key result:

+-- {: .num_prop #PerturbativeQuantumObservablesIsLocalnet}
###### Proposition
**(system of algebras of perturbative quantum observables is [[local net of observables]])**


Given a perturbative S-matrix according to def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}
and an interaction [[Lagrangian density]] $L_{int}$, then the system of [[algebras of observables]] $Obs_{L_{int}}$ (def. \ref{SystemOfAlgebrasOfQuantumObservables})
is a [[local net of observables]] in that

1. (isotony) For every inclusion $\mathcal{O}_1 \subset \mathcal{O}_2$ of [[causally closed subsets]]
   the corresponding algebra homomorphism is a [[monomorphism]]

   $$
     i_{\mathcal{O}_1, \mathcal{O}_2}
     \;\colon\;
     Obs_{L_{int}}(\mathcal{O}_1) \hookrightarrow Obs_{L_{int}}(\mathcal{O}_2)
   $$

1. ([[causal locality]]) For $\mathcal{O}_1, \mathcal{O}_2 \subset X$ two [[causally closed subsets]]
   which are [[spacelike]] separated, in that their causal ordering (def. \ref{CausalOrdering}) satisfies

   $$
     \mathcal{O}_1 \geq \mathcal{O}_2
       \;\text{and}\;
     \mathcal{O}_2 \geq \mathcal{O}_1
   $$

   then for $\mathcal{O} \subset X$ any further causally closed subset which contains both

   $$
     \mathcal{O}_1 , \mathcal{O}_2 \subset \mathcal{O}
   $$

   then the corresponding images of the generating algebras of $\mathcal{O}_1$ and $\mathcal{O}_2$,
   respectively, commute with each other as subalgebras of the generating algebra of $\mathcal{O}$:

   $$
     \left[
       i_{\mathcal{O}_1,\mathcal{O}}(Obs_{L_{int}}(\mathcal{O}_1))
       \;,\;
       i_{\mathcal{O}_2,\mathcal{O}}(Obs_{L_{int}}(\mathcal{O}_2))
     \right]
     \;=\;
     0
     \;\;\;
     \in Obs_{L_{int}}(\mathcal{O})
     \,.
   $$

=--

([D&#252;tsch-Fredenhagen 00, below (17)](#DuetschFredenhagen00), following [Brunetti-Fredenhagen 99, section 8](#BrunettiFredenhagen99),
[Il'in-Slavnov 78](#IlinSlavnov78))

+-- {: .proof}
###### Proof

The first point is again immediate from the definition (def. \ref{SystemOfAlgebrasOfQuantumObservables}).

For the second point it is sufficient to check the commutativity relation on generators. For these
the statement follows with prop. \ref{GeneratingAlgebrasIsLocalNet}:

$$
  \begin{aligned}
    \left[
      -i \frac{d}{d \epsilon_1} Z_{g_{sw}L_{int}}(\epsilon_1 J_1)\vert_{\epsilon_1 = 0}
      \;,\;
      -i  \frac{d}{d \epsilon_2} Z_{g_{sw}L_{int}}(\epsilon_2 J_2)\vert_{\epsilon_2 = 0}
    \right]
    &
    =
     -
     \frac{d}{d \epsilon_1}
     \frac{d}{d \epsilon_2}
     \underset{ = 0}{
     \underbrace{
    \left[
       Z_{g_{sw}L_{int}}(\epsilon_1 J_1)
      \;,\;
       Z_{g_{sw}L_{int}}(\epsilon_2 J_2)
    \right]}} \vert_{ {\epsilon_1 = 0} \atop {\epsilon_2 = 0}}
    \\
    & = 0
  \end{aligned}
$$

for $supp(J_1) \geq supp(J_2)$ and $supp(J_2) \geq supp(J_1)$.

=--

$\,$

#### Feynman diagrams and Renormalization
 {#ExistenceAndRenormalization}


So far we considered only the [[axioms]] on a consistent perturbative S-matrix /[[time-ordered products]]
and its formal consequences. Now we discuss the actual construction of [[time-ordered products]],
hence of perturbative S-matrices, by the process called _[[renormalization]] of [[Feynman diagrams]]_.

We first discuss how [[time-ordered product]], and hence the perturbative S-matrix [above](#PerturbativeSMatrixAndTimeOrderedProducts),
is uniquely determined away from the locus where interaction points coincide (prop. \ref{TimeOrderedProductAwayFromDiagonal} below).
Moreover, we discuss how on that locus the time-ordered product is naturally expressed as a sum
of [[products of distributions]] of [[Feynman propagators]] that are labeled by [[Feynman diagrams]]: the _[[Feynman perturbation series]]_ (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints} below).

This means that the full  [[time-ordered product]] is an [[extension of distributions]] of these
_[[scattering amplitudes]]- to the locus of coinciding vertices. The space of possible such
extensions turns out to be finite-dimensional in each order of $g/\hbar, j/\hbar$, parameterizing the choice of
[[point-supported distributions]] at the interaction points whose [[degree of a distribution|scaling degree]]
is bounded by the given Feynman propagators.

+-- {: .num_defn #TuplesOfCompactlySupportedPolynomialLocalFunctionalsWithPairwiseDisjointSupport}
###### Definition

For $k \in \mathbb{N}$, write

$$
  \left(\mathcal{F}_{loc}\langle g,j\rangle\right)^{\otimes^k}_{pds}
  \hookrightarrow
  \left(\mathcal{F}_{loc}\langle g,j\rangle\right)^{\otimes^k}
$$

for the subspace of the $k$-fold [[tensor product]] of the space of compactly supported polynomial
local densities (def. \ref{CompactlySupportedPolynomialLocalDensities}) on those [[tuples]]
which have pairwise disjoint spacetime [[support]].

=--

+-- {: .num_prop #TimeOrderedProductAwayFromDiagonal}
###### Proposition
**([[time-ordered product]] away from the diagonal)**

Restricted to $\left(\mathcal{F}_{loc}\langle g,j\rangle\right)^{\otimes^k}_{pds}$
(def. \ref{TuplesOfCompactlySupportedPolynomialLocalFunctionalsWithPairwiseDisjointSupport})
there is a unique [[time-ordered product]] (def. \ref{TimeOrderedProduct}),
given by the [[star product]] that is induced by the [[Feynman propagator]] $\omega_F$

$$
  F \star_{\omega_F} G
  \;\coloneqq\;
  prod \circ
  \exp\left(
   \hbar
   \left\langle
     \omega_F , \frac{\delta}{\delta \phi} \otimes \frac{\delta}{\delta \phi}
   \right\rangle
  \right)
  (F \otimes G)
$$

in that

$$
  T( L_1 \cdots L_k )
  =
  L_1 \star_{\omega_F} L_2 \star_{\omega_F} \cdots \star_{\omega_F} L_k
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since the [[singular support]] of the [[Feynman propagator]] is on the [[diagonal]],
and since the support of elements in $\left(\mathcal{F}_{loc}\langle g,j\rangle\right)^{\otimes^k}_{pds}$
is by definition in the complement of the diagonal, the star product $\star_{\omega_F}$ is well defined.
By construction it satisfies the axioms "peturbation" and "normalization" in def. \ref{TimeOrderedProduct}.
The only non-trivial point to check is that it indeed satisfies "[[causal factorization]]":

Unwinding the definition of the [[Hadamard state]] $\omega$ and the [[Feynman propagator]] $\omega_F$, we have

$$
  \begin{aligned}
    \omega & = \tfrac{i}{2}( \Delta_R - \Delta_A ) + H
    \\
    \omega_F & = \tfrac{i}{2}( \Delta_R + \Delta_A ) + H
  \end{aligned}
$$

where the propagators on the right have, in particular, the following properties:

1. the [[advanced propagator]] vanishes when its first argument is not in the causal past of its second argument:

   $$
     (supp(F) \geq supp(G))
     \;\Rightarrow\;
     \left(
       \left\langle \Delta_A , \frac{\delta F}{\delta \phi} \otimes \frac{\delta G}{\delta \phi}  \right\rangle = 0
     \right)
     \,.
   $$

1. the [[retarded propagator]] equals the [[advanced propagator]] with arguments switched:

   $$
     \left\langle \Delta_R , \frac{\delta F}{\delta \phi} \otimes \frac{\delta G}{\delta \phi} \right\rangle
       =
     \left\langle \Delta_A , \frac{\delta G}{\delta \phi} \otimes \frac{\delta F}{\delta \phi} \right\rangle
   $$

1. $H$ is symmetric:

   $$
     \left\langle H, \frac{\delta F}{\delta \phi} \otimes \frac{\delta G}{\delta \phi} \right\rangle
     =
     \left\langle H, \frac{\delta G}{\delta \phi} \otimes \frac{\delta F}{\delta \phi} \right\rangle
   $$

It follows for causal ordering $supp(F) \geq supp(G)$ (def. \ref{CausalOrdering}) that

$$
  \begin{aligned}
    F \star_{\omega_F} G
    & =
    prod \circ \exp\left(
      \hbar
      \left\langle  \omega_F , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    prod \circ
    \exp\left(
      \hbar
      \left\langle  \tfrac{i}{2}( \Delta_R + \Delta_A ) + H  , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    prod \circ
    \exp\left(
      \hbar
      \left\langle  \tfrac{i}{2}\Delta_R + H  , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    prod \circ
    \exp\left(
      \hbar
      \left\langle  \tfrac{i}{2}( \Delta_R - \Delta_A ) + H  , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    prod \circ
    \exp\left(
      \hbar
      \left\langle  \omega , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    F \star_{\omega} G
  \end{aligned}
$$

and for $supp(G) \geq supp(F)$ that

$$
  \begin{aligned}
    F \star_{\omega_F} G
    & =
    prod \circ \exp\left(   
      \hbar
      \left\langle  \omega_F , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    prod \circ \exp\left(
      \hbar
      \left\langle  \tfrac{i}{2}( \Delta_R + \Delta_A ) + H  , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    prod \circ \exp\left(
      \hbar
      \left\langle  \tfrac{i}{2} \Delta_A + H  , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    prod \circ \exp\left(
      \hbar
      \left\langle  \tfrac{i}{2} \Delta_R + H  , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( G \otimes F )
    \\
    & =
    prod \circ \exp\left(
      \hbar
      \left\langle  \tfrac{i}{2} (\Delta_R - \Delta_A) + H  , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( G \otimes F )
    \\
    & =
    G \star_{\omega} F
    \,.
  \end{aligned}
$$

This shows that $\star_F$ is a consistent time-ordered product on the subspace of functionals
with disjoint support. It is immediate from the above that it is the unique solution on this subspace.

=--

+-- {: .num_remark #TimeOrderedProductAssociative}
###### Remark
**([[time-ordered product]] is [[associativity|assocativative]])**

Prop. \ref{TimeOrderedProductAwayFromDiagonal} implies in particular that the
time-ordered product is [[associativity|associative]], in that

$$
  T( T(V_1 \cdots V_{k_1}) \cdots T(V_{k_{n-1}+1} \cdots V_{k_n} ) )
  =
  T( V_1 \cdots V_{k_1} \cdots V_{k_{n-1}+1} \cdots V_{n_n} )
  \,.
$$

=--

It follows that the problem of constructing time-ordered products, and hence (by prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix}) the
perturbative S-matrix, consists of finding compatible [[extension of distributions|extension]]
of the distribution
$ prod \circ \exp\left( \left\langle  \omega_F , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle \right)$ to the diagonal.

Moreover, by the nature of the exponential expression, this means in each order to
extend [[product of distributions|products]] of Feynman propagators labeled by
[[graphs]] whose [[vertices]] correspond to the polynomial factors in $F$ and $G$ and whose
[[edges]] indicate over which variables the Feynman propagators are to be multiplied.


+-- {: .num_defn #ScalarFieldFeynmanDiagram}
###### Definition
**([[scalar field]] [[Feynman diagram]])**

A _[[scalar field]] [[Feynman diagram]]_ $\Gamma$ is

1. a [[natural number]] $v \in \mathcal{N}$ (number of [[vertices]]);

1. a $v$-[[tuple]] of elements $(V_r \in \mathcal{F}_{loc} \langle g,j\rangle)_{r \in \{1, \cdots, v\}}$ (the interaction and external field vertices)

1. for each $a \lt b \in \{1, \cdots, v\}$ a natural number $e_{a,b} \in \mathbb{N}$ ("of [[edges]] from the $a$th to the $b$th vertex").

For a given [[tuple]] $(V_j)$ of interaction vertices we write

$$
  FDiag_{(V_j)}
$$

for set of scalar field Feynman diagrams with that tuple of vertices.

=--

+-- {: .num_prop #FeynmanPerturbationSeriesAwayFromCoincidingPoints}
###### Proposition
**([[Feynman perturbation series]] away from coinciding vertices)


For $v \in \mathbb{N}$ the $v$-fold
[[time-ordered product]] away from the diagonal,
given by prop. \ref{TimeOrderedProductAwayFromDiagonal}

$$
  T_v
    \;\colon\;
  \left(\mathcal{F}_{loc}\langle g,j\rangle\right)_{pds}^{\otimes^{v}}
    \longrightarrow
  \mathcal{W}[ [ g/\hbar, j/\hbar] ]
$$

is equal to

$$
  T_k(V_1 \cdots V_v)
    \;=\;
  prod
    \circ
  \underset{\Gamma \in \mathcal{G}_{(V_j)_{j = 1}^{v}}}{\sum}
  \underset{ r \lt s \in \{1, \cdots, v\} }{\prod}
  \tfrac{1}{e_{r,s}!}
  \left\langle
      \hbar \omega_F
      \,,\,
      \frac{\delta^{e_{r,s}}}{\delta \phi_r^{e_{r,s}}}
      \frac{\delta^{e_{r,s}}}{ \delta \phi_s^{e_{r,s}} }
  \right\rangle
  (V_1 \otimes \cdots \otimes V_v)
  \,,
$$

where the edge numbers $e_{r,s} = e_{r,s}(\Gamma)$ are those of the given Feynman diagram $\Gamma$.

=--

([Keller 10, IV.1](#Keller10))

+-- {: .proof}
###### Proof

We proceed by [[induction]] over the number of [[vertices]].
The statement is trivially true for a single vertex.
Assume it is true for $v \geq 1$ vertices. It follows that

$$
  \begin{aligned}
    T(V_1 \cdots V_v V_{v+1})
    & =
    T( T(V_1 \cdots V_v) V_{v+1} )
    \\
    &=
    prod \circ
    \exp\left(
      \left\langle
         \hbar \omega_F, \frac{\delta}{\delta \phi} \otimes \frac{\delta}{\delta \phi}
      \right\rangle
    \right)
    \left(
      prod
        \circ
      \underset{\Gamma \in \mathcal{G}_{(V_j)_{j = 1}^{v}}}{\sum}
      \underset{ r \gt s \in \{1, \cdots, v\} }{\prod}
      \frac{1}{e_{r,s}!}
      \left\langle
          \hbar \omega_F
          \,,\,
          \frac{\delta^{e_{r,s}}}{\delta \phi_r^{e_{r,s}}}
          \frac{\delta^{e_{r,s}}}{ \delta \phi_s^{e_{r,s}} }
      \right\rangle
      (V_1 \otimes \cdots \otimes V_v)
    \right)
    \;\otimes\;
    V_{v+1}
    \\
    & =
    prod
      \circ
    \underset{\Gamma \in \mathcal{G}_{(V_j)_{j = 1}^{v}}}{\sum}
      \underset{ r \gt s \in \{1, \cdots, v\} }{\prod}
      \tfrac{1}{e_{r,s}!}
    \left\langle
        \hbar \omega_F
        \,,\,
        \frac{\delta^{e_{r,s}}}{\delta \phi_r^{e_{r,s}}}
        \frac{\delta^{e_{r,s}}}{ \delta \phi_s^{e_{r,s}} }
    \right\rangle
    \left(
    \underset{e_{1,{v+1}}, \cdots e_{v,v+1} \in \mathbb{N}}{\sum}
      \underset{t \in \{1, \cdots v\}}{\prod}
      \tfrac{1}{e_{t,v+1} !}
    \left(
      \frac{\delta^{e_{1,v+1}} V_1 }{\delta \phi_{1}^{e_{1,v+1}}}
        \otimes
        \cdots
        \otimes
      \frac{ \delta^{e_{v,v+1}} V_v}{ \delta \phi_{v}^{e_{v,v+1}} }
    \right)
    \;\otimes\;
    \frac{\delta^{e_{1,v+1} + \cdots + e_{v,v+1}} V_{v+1}}{\delta \phi_{v-1}^{e_{1,v+1} + \cdots + e_{v,v+1}}}
    \right)
    \\
    &=
    prod
      \circ
    \underset{\Gamma \in \mathcal{G}_{(V_j)_{j = 1}^{v+1}}}{\sum}
    \underset{ r \lt s \in \{1, \cdots, v+1\} }{\prod}
    \tfrac{1}{e_{r,s}!}
    \left\langle
        \hbar \omega_F
        \,,\,
        \frac{\delta^{e_{r,s}}}{\delta \phi_r^{e_{r,s}}}
        \frac{\delta^{e_{r,s}}}{ \delta \phi_s^{e_{r,s}} }
    \right\rangle
    (V_1 \otimes \cdots \otimes V_{v+1})
  \end{aligned}
$$

Here in the first step we use the [[associativity]] of the time-ordered product
(remark \ref{TimeOrderedProductAssociative}), in the second step we use the induction assumption,
in the third we pass the outer functional derivatives through the pointwise product
using the [[product rule]], and in the fourth step we recognize that this amounts to summing
in addition over all possible choices of sets of edges from the first $v$ vertices to the new $v+1$st vertex,
which yield in total the sum over all diagrams with $v+1$ vertices.

=--

[[!include Feynman diagrams in causal perturbation theory -- summary]]


+-- {: .num_remark}
###### Remark
**([[loop order]] and powers of [[Planck's constant]])

From prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints} one deduces that the
order in [[Planck's constant]] that a ([[planar graph|planar]]) [[Feynman diagram]] contributes to the 
S-matrix is given (up to a possible offset due to external vertices) by the "number of loops" in the diagram.
See at _[[loop order]]_ the section _[Relation to powers in Planck's constant](loop+order#RelationToPowersInPlancksConstant)_ for details.

=--

(...)

The [[main theorem of perturbative renormalization]] states that

1. For fixed $L_{int}$ the extension of these time-ordered products to the diagonal exists, and in each order there is a finite dimensional space of possible choices.

1. There is a way to make these choices coherently, so that
   one obtains the $S$-matrix indeed as a function in $L_{int}$. (a "renormalization scheme").

1. The perturbative S-matrices $S$ and $\tilde S$ for two different such renormalization schemes are
   related by a transformation $Z \;\colon\; \mathcal{F}_{loc} \longrightarrow \mathcal{F}_{loc}$ as

   $$
     \tilde S = S \circ Z
     \,.
   $$

   here $Z(L_{int})$ is $L_{int}$ with "counterterms added".

1. The transformations $Z \colon \mathcal{T}_{loc} \to \mathcal{T}_{loc}$ form a [[group]], called the
   _[[Stückelberg-Peterson renormalization group]]_. Hence the renormalization schemes / coherent perturbative
   S-matrices form a [[torsor]] over this group.





$\,$

$\,$

$\,$

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


In the 1960s there was a prominent proposal, around [[Geoffrey Chew]], that ([[perturbative quantum field theory|perturbative]]) [[quantum field theory]] should be _defined_ by [[axiom|axiomatizing]] properties of the S-matrix _without_ explicit reference to [[spacetime]]. 
This is a radical perspective where no [[spacetime]] geometry and physical fields are made explicit, but where the entire physics is encoded by what quantum particles see that scatter through it.

Historically, this S-matrix "bootstrap" approach fell out of fashion with the success of the [[quark]] model and of [[QCD]], which is a [[local field theory|local]] [[Lagrangian field theory]] ([[Yang-Mills theory]]) defined in terms of [[field (physics)|fields]] on [[spacetime]].

But later [[perturbative string theory]] revived the S-matrix approach. In general, perturbative string theory is not defined by a geometric spacetime background. Instead the background is algebraically encoded by a [[2d SCFT]] ("[[2-spectral triple]]") and the [[string perturbation series]] is a formula that translates this into an S-matrix. Spacetime physics then is whatever is seen by string scattering processes (see also at _[string theory FAQ -- What are the equations of string theory?](string%20theory%20FAQ#WhatAreTheEquations)_). 

More recently, the S-matrix perspective becomes fashionable also in [[Yang-Mills theory]], at least in [[super Yang-Mills theory]]: one observes that the theory enjoyes good structures in its scattering amplitudes which are
essentially invisible in the vast summation of [[Feynman diagrams]] that extract the S-matrix from the [[action functional]]. Instead there are entirely different mathematical structures that encode at least some sub-class of scattering amplitudes (see at _[[amplituhedron]]_).

{#RonMaimonOnHistory} From [this physics.SE comment](http://physics.stackexchange.com/a/15164/5603) by [[Ron Maimon]]:

> The history of [[physics]] cannot be well understood without appreciating the unbelievable antagonism between the [[Geoffrey Chew|Chew]]/[[Stanley Mandelstam|Mandelstam]]/[[Vladimir Gribov|Gribov]] S-matrix camp, and the [[Steven Weinberg|Weinberg]]/[[Sheldon Glashow|Glashow]]/[[Alexander Polyakov|Polyakov]] [[quantum field theory|Field theory]] camp. The two sides hated each other, did not hire each other, and did not read each other, at least not in the west. The only people that straddled both camps were older folks and Russians--- [[Murray Gell-Mann|Gell-Mann]] more than [[Lev Landau|Landau]] (who believed the [[Landau pole]] implied the S-matrix), Gribov and Migdal more than anyone else in the west other than [[Murray Gell-Mann|Gell-Mann]] and [[Kenneth Wilson|Wilson]]. Wilson did his PhD in S-matrix theory, for example, as did [[David Gross]] (under Chew).

> In the 1970s, S-matrix theory just plain died. All practitioners jumped ship rapidly in 1974, with the triple-whammy of [[effective field theory|Wilsonian field theory]], the discovery of the Charm [[quark]], and [[asymptotic freedom]]. These results killed S-matrix theory for thirty years. Those that jumped ship include all the original [[string theory|string theorists]] who stayed employed: notably [[Gabriele Veneziano|Veneziano]], who was convinced that [[gauge theory]] was right when [[Gerard 't Hooft|t'Hooft]] showed that [[AdS-CFT|large-N gauge fields]] give the string topological expansion, and [[Leonard Susskind|Susskind]], who didn't mention Regge theory after the early 1970s. Everybody stopped studying [[string theory]] except [[Joël Scherk|Scherk]] and [[John Schwarz|Schwarz]], and Schwarz was protected by
[[Murray Gell-Mann|Gell-Mann]], or else he would never have been tenured and funded.

> This sorry history means that not a single S-matrix theory course is taught in the curriculum today, nobody studies it except a few theorists of advanced age hidden away in particle accelerators, and the main S-matrix theory, [[string theory]], is not properly explained and remains completely enigmatic even to most physicists. There were some good reasons for this --- some S-matrix people said silly things about the consistency of quantum field theory --- but to be fair, [[quantum field theory]] people said equally silly things about S-matrix theory.

> [[Steven Weinberg|Weinberg]] came up with these heuristic arguments in the 1960s, which convinced him that S-matrix theory was a dead end, or rather, to show that it was a tautological synonym for quantum field theory. Weinberg was motivated by models of pion-nucleon interactions, which was a hot S-matrix topic in the early 1960s. The solution to the problem is the [[chiral symmetry breaking]] models of the pion condensate, and these are [[effective field theories]].

> Building on this result, Weinberg became convinced that the only real solution to the S-matrix was a field theory of some particles with spin. He still says this every once in a while, but it is dead wrong. The most charitable interpretation is that every S-matrix has a field theory limit, where all but a finite number of particles decouple, but this is not true either (consider [[little string theory]]). String theory exists, and there are non-field theoretic S-matrices, namely all the ones in [[string theory]], including [[little string theory]] in (5+1)d, which is non-gravitational.

From ([Weinberg 09, p. 11](#Weinberg09)):

> I offered this in my 1979 paper as what [[Arthur Wightman]] would call a [[folk theorem]]: "if one writes down the most general possible [[Lagrangian]], including all terms consistent with assumed [[symmetry]] principles, and then calculates [[scattering amplitudes|matrix elements]] with this Lagrangian to any given order of [[perturbation theory]], the result will simply be the most general possible S-matrix consistent with perturbative unitarity, analyticity, [[cluster decomposition]], and the assumed symmetry properties."

> There was an interesting irony in this. I had been at Berkeley from 1959 to 1966, when [[Geoffrey Chew]] and his collaborators were elaborating a program for calculating S-matrix elements for [[strong nuclear force|strong interaction]] processes by the use of unitarity, analyticity, and Lorentz invariance, without reference to [[quantum field theory]]. I found it an attractive philosophy, because it relied only on a minimum of principles, all well established. Unfortunately, the S-matrix theorists were never able to develop a reliable method of calculation, so I worked instead on other things, including [[current algebra]]. Now in 1979 I realized that the assumptions of S-matrix theory, supplemented by chiral invariance, were indeed all that are needed at low energy, but the most convenient way of implementing these assumptions in actual calculations was by good old quantum field theory, which the S-matrix theorists had hoped to supplant.



## Related entries

See also at _[[sigma model]]_ the section _<a href="http://ncatlab.org/nlab/show/sigma-model#SecondQuantization">Exposition of second quantization of sigma-models</a>_

* [[Coleman theorem]], [[Haag–Łopuszański–Sohnius theorem]]

* [[scattering amplitude]], [[Feynman diagram]], [[string scattering amplitude]],

* [[AdS-CFT]]

* [string theory FAQ -- What are the equations of string theory?](string%20theory%20FAQ#WhatAreTheEquations)

[[!include products in pQFT -- table]]


## References

Early work basing [[perturbative quantum field theory]] on the concept of the S-matrix is

* {#Heisenberg43} [[Werner Heisenberg]], Zeitschrift für Physik 120, 513, 1943

A textbook account of the axiomatic approach is 

* Eden, Landshoff, Olive, Polkinghorne, _The Analytic S-matrix_, Cambridge 1966 ([pdf](http://assets.cambridge.org/97805210/48699/sample/9780521048699ws.pdf))

A textbook account of the traditional heuristic picture is in

* {#Weinberg95} [[Steven Weinberg]], chapter 3 of _The quantum theory of fields - Volume I: Foundations_, Cambridge 1995

The mathematically rigorous construction in field theory via [[causal perturbation theory]] is due to

* {#EpsteinGlaser73} [[Henri Epstein]], [[Vladimir Glaser]], _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211 ([Numdam](http://www.numdam.org/item?id=AIHPA_1973__19_3_211_0 ))

based on ideas due to ([St&#252;ckelberg 49](causal+perturbation+theory#Stueckelberg49), [St&#252;ckelberg 51](causal+perturbation+theory#Stueckelberg49)) and

* {#BogoliubovShirkov59} [[Nikolay Bogoliubov]], [[Dmitry Shirkov]], _Introduction to the Theory of Quantized Fields_, New York (1959)

Brief introduction to the S-matrix in quantum mechanics and its rigorous construction in field theory via [[causal perturbation theory]]

* {#Scharf95} [[Günter Scharf]], sections 0.3 and 3.1 of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Springer 1995

* [[Günter Scharf]], section 2 of _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

The formulation of [[causal perturbation theory]] in terms of [[Feynman diagrams]] is due to

* {#Keller10} [[Kai Keller]], chapter IV of _Dimensional Regularization in Position Space and a Forest Formula for Regularized Epstein-Glaser Renormalization_, PhD thesis ([arXxiv:1006.2148](https://arxiv.org/abs/1006.2148))

see also

* {#DuetschFredenhagenKellerRejzner14} [[Michael Dütsch]], [[Klaus Fredenhagen]], [[Kai Keller]], [[Katarzyna Rejzner]], _Dimensional Regularization in Position Space, and a Forest Formula for Epstein-Glaser Renormalization_, J. Math. Phy.
55(12), 122303 (2014) ([arXiv:1311.5424](https://arxiv.org/abs/1311.5424))


Construction of the [[local net of quantum observables]] from [[causal perturbation theory]] was hinted at in

* {#IlinSlavnov78} V. A. Il'in and D. S. Slavnov, _Observable algebras in the S-matrix approach_, Theor. Math. Phys. 36 (1978) 32. ([spire](http://inspirehep.net/record/135575), [doi](http://dx.doi.org/10.1007/BF01035870))

then rediscovered in

* {#BrunettiFredenhagen99} [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661, 2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))

and made more explicit in

* {#DuetschFredenhagen00} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Algebraic Quantum Field Theory, Perturbation Theory, and the Loop Expansion_, Commun.Math.Phys. 219 (2001) 5-30 ([arXiv:hep-th/0001129](https://arxiv.org/abs/hep-th/0001129))

The axiomatization in terms of [[retarded products]], which as such were maybe introduced in

* {#GlaserLehmannZimmermann57} [[Vladimir Glaser]], H. Lehmann, W. Zimmermann, _Field operators and retarded functions_, Il Nuovo Cimento 6, 1122-1128 (1957) ([doi:10.1007/bf02747395](http://dx.doi.org/10.1007/bf02747395))

* O. Steinmann, _Perturbation Expansions in Axiomatic Field Theory_, Lecture Notes in Physics, vol. 11, Springer, Berlin and Heidelberg, 1971.

goes back to

* {#DuetschFredenhagen04} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Causal perturbation theory in terms of retarded products, and a proof of the Action Ward Identity_, Rev. Math. Phys. 16, 1291 (2004) ([arXiv:hep-th/0403213](https://arxiv.org/abs/hep-th/0403213))

A detailed discussion is in

* {#Collini16} [[Giovanni Collini]], section 2.2 of _Fedosov Quantization and Perturbative Quantum Field Theory_ ([arXiv:1603.09626](https://arxiv.org/abs/1603.09626))

following

* {#HollandsWald04} [[Stefan Hollands]], [[Robert Wald]], _Conservation of the stress tensor in perturbative interacting quantum field theory in curved spacetimes_, Rev. Math. Phys. 17 (2005) 227-312 ([arXiv:gr-qc/0404074](https://arxiv.org/abs/gr-qc/0404074))


For review and further development in the context of [[perturbative AQFT]] see the references there, such as


* {#Rejzner16} [[Katarzyna Rejzner]], _Perturbative Algebraic Quantum Field Theory_, Mathematical Physics Studies, Springer 2016 ([pdf](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))


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

[[!redirects perturbative S-matrix]]
[[!redirects perturbative S-matrices]]

[[!redirects Feynman perturbation series]]
