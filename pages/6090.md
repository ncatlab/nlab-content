
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

In [[quantum field theory]] a _[[scattering amplitude]]_ or _scattering matrix_, usually just _S-matrix_ for short, encodes the [[probability amplitudes]] for scatterings processes of [[particles]] off each other.

### General idea

Every [[Lagrangian field theory|Lagrangian]] [[perturbative quantum field theory]] has an S-matrix associated with its (after [[renormalization]]), usually thought of as a [[perturbation series]] over [[Feynman diagrams]] extracted from the [[Lagrangian density]]. The rigorous construction of this as an [[operator-valued distribution]] is the content of _[[causal perturbation theory]]_ ([Epstein-Glaser 73](#EpsteinGlaser73)).

But there are also S-matrices not arising from a local field theory, for instance the [[string scattering amplitudes]].

There have been attempts to _define_ [[perturbative quantum field theory]] by directly [[axiom|axiomatizing]] properties of the S-matrix, without requiring concepts of [[field (physics)|fields]] in [[spacetime]]. This perspective goes back to ([Heisenberg 43](#Heisenberg43)) and was vocally promoted in [[Geoffrey Chew]]'s "bootstrap program" (a textbook account is in [Eden-Ladshoff-Olive-Polkinhorne 66](#EdenLadshoffOlivePolkinhorne66)).

In the [[field theory]]-picture the crucial condition on the S-matrix is its [[causal additivity]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering} below) which reflects the [[microcausality]] of [[quantum observables]] (prop. \ref{PerturbativeQuantumObservablesIsLocalnet} below), whence the name "[[causal perturbation theory]]".

{#TheAnalyticSMatrix} This [[causality]] of the S-matrix, when understood in terms of underlying [[spacetime]] and [[field (physics)|fields]], is supposed to be detected more abstractly by the S-matrix being a suitable [[analytic function]] of the [[wave vectors]] of the scattering asymptotic states ([Newton 82, 10.3.3](#Newton82), [Arkani-Hamed et al. 06](#AAHDNR06)), often refereed to via "dispersion relations" (e.g. [Eden-Ladshoff-Olive-Polkinhorne 66 (1.1.1)-(1.1.5)](#EdenLadshoffOlivePolkinhorne66), [Gribov 69, 1.1.2](#Gribov69)). Since thereby analyticity is recognized as the crucial property of the S-matrix in the spacetime/field-independent axiomatization, this is often referred to as "the analytic S-matrix" (e.g. [Eden-Ladshoff-Olive-Polkinhorne 66](#EdenLadshoffOlivePolkinhorne66)). More specifically [[microcausality]] is what induces "crossing symmetry" of the S-matrix ([Weinberg 95, section 10.8](#Weinberg95)).

The perception of the nature of the S-matrix as a primary or derived concept in the foundations of quantum field theory has a convoluted (and ongoing) history, see [below](#History).

### The S-matrix bootstrap

From [this Phyics.SE comment](https://physics.stackexchange.com/a/17973/5603) by [[Ron Maimon]]:

The idea of the S-matrix "bootstrap" is that one may compute the S-matrix directly from suitable axioms without using a [[local field theory|local]] [[quantum field theory]] involving [[field (physics)|fields]] on [[spacetime]]. In order for the theory to be interesting, the S-matrix should obey certain properties abstracted away from field theory

* It should be unitary
* It should be Lorentz invariant
* It should be crossing invariant: this means that the antiparticle scattering
should be described by the analytic continuation of the particle scattering
* It should obey the Landau property--- that all singularities of scattering are poles and cuts corresponding to exchange of collections of real particles on shell.
* It should obey ([[Stanley Mandelstam|Mandelstam]]) analyticity: the amplitude should be writable as an integral over the imaginary part of the cut discontinuity from production of physical particles. Further, this cut discontinuity itself can be expanded in terms of another cut discontinuity (these are the mysterious then and still mysterious now double dispersion relations of Mandelstam).

This is a sketchy summary, because each of these conditions is involved. The unitarity condition in particular, is very difficult, because it is so nonlinear. The only practical way to solve it is in a perturbation series which starts with weakly interacting nearly stable particles (described by poles of the S-matrix) which exchange each other (the exchange picture is required by crossing, and the form of the scattering is fixed by the Landau and Mandelstam analyticity, once you know the spectrum).

The "Bootstrap property" is then the following heuristic idea, which is included in the above formal relations:

* The particles and interactions which emerge as the spectrum of the S-matrix from the scattering of states, including their binding together into bound states, should be the same spectrum of particles that come in as in-states.

This is a heuristic idea, because it is only saying that the S-matrix is consistent, and the formal consistency relations are those above. But the bootstrap was a slogan that implied that all the consistency conditions were not yet discovered, and there might be more.

This idea was very inspirational to many great people in the 1960s, because it was an approach to strong interactions that could accommodate non-field theories of infinitely many particle types of high spin, without postulating constituent particles (like quarks and gluons).

### Regge theory

Continuing with [this Phyics.SE comment](https://physics.stackexchange.com/a/17973/5603) by [[Ron Maimon]]:


The theory above doesn't get you anywhere without the following additional stuff. If you don't do this, you end up starting with a finite number of particles and interactions, and then you end up in effective field theory land. The finite-number-of-particles version of S-matrix theory is a dead end, or at least, it is equivalent to effective field theory, and this was understood in the late 1960s by Weinberg, and others, and this led S-matrix theory to die. This was the road the Chew travelled on, and the end of this road must be very personally painful to him.

But there is another road for S-matrix theory which is much more interesting, so that Chew should not be disheartened. You need to know that the scattering amplitude is analytic in the angular momentum of the exchanged particles, so that the particles lie on Regge trajectories, which give their angular momentum as a function of their mass squared, s.

Where the Regge trajectories hit an integer angular momentum, you see a particle. The trajectory interpolates the particle mass-squared vs. angular momentum graph, and it gives the asymptotic scattering caused by exchanging all these particles _together_. This scattering can be softer than the exchange of any one of these particles, because exchanging a particle of high spin necessarily has very singular scattering amplitudes at high energy. The Regge trajectory cancels out this growth with an infinite series of higher particles which soften the blowup, and lead to a power-law near-beam scattering at an angle which shrinks to zero as the energy goes to infinity in a way determined by the shape of the trajectory.

So the Regge bootstrap adds the following conditions

* All the particles in the theory lie on Regge trajectories, and the scattering of these particles is by Regge theory.

This condition is the most stringent, because you can't deform a pure Regge trajectory by adding a single particle--- you have to add new trajectories. The following restriction was suggested by experiment

* The Regge trajectories are linear in s

This was suggested by Chew and Frautschi from the resonances known in 1960! The straight lines mostly had two points. The next condition is also ad-hoc and experimental

* The Regge slope is universal (for mesons), it's the same for all the trajectories.

There are also "pomerons" in this approach which are not mesons, which have a different Regge slopem but ignore this for now.

Finally, there is the following condition, which was experimentally motivated, but has derivations by Mandelstam and others from more theoretical foundations (although this is S-matrix theory, it doesn't have axioms, so derivation is a loose word).

* The exchange of trajectories is via the s-channel or the t-channel, but not both. It is double counting to exchange the same trajectories in both channels.

These conditions essentially uniquely determine Veneziano's amplitude and bosonic string theory. Adding Fermion trajectories requires Ramond style supersymmetry, and then the road to string theory is to reinterpret all these conditions in the string picture which emerges.

String theory incorporates and gives concrete form to all the boostrap ideas, so much so that anyone doing bootstrap today is doing string theory, especially since AdS/CFT showed why the bootstrap is relevant to gauge theories like QCD in the first place.

The highlight of Regge theory is the Reggeon calculus, a full diagrammatic formalism, due to Gribov, for calculating the exchange of pomerons in a perturbation framework. This approach inspired a 2d parton picture of QCD which is studied heavily by several people, notably, Gribov, Lipatov, Feynman (as part of his parton program), and more recently Rajeev. Nearly every problem here is open and interesting.

For an example of a reasearch field which (partly) emerged from this, one of the major motivations for taking PT quantum mechanics seriously was the strange non-Hermitian form of the Reggeon field theory Hamiltonian.

### Pomerons and Reggeon Field theory

Further from [this Phyics.SE comment](https://physics.stackexchange.com/a/17973/5603) by [[Ron Maimon]]:

The main success of this picture is describing near-beam scattering, or diffractive scattering, at high energies. The idea here is that there is a Regge trajectory which is called the pomeron, which dominates high energy scattering, and which has no quantum numbers. This means that any particle will exchange the pomeron at high energies, so that p-pbar and p-p total cross sections will become equal.

This idea is spectacularly confirmed by mid 90's measurements of total p-p and p-pbar cross sections, and in a better political climate, this would have won some boostrap theorists a Nobel prize. Instead, it is never mentioned.

The pomeron in string theory becomes the closed string, which includes the graviton, which couples universally to stress energy. The relation between the closed string and the QCD pomeron is the subject of active research, associated with the names of Lipatov, Polchinski, Tan, and collaborators.

Regge scattering also predicts near beam scattering amplitudes from the sum of the appropriate trajectory function you can exchange. These predictions have been known to roughly work since the late 1960s.


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

Notice that if the operator $V$ were to commute with $H_{free}$ (which it does not in all relevant examples) then we would simply have $\vert \psi(t)\rangle_I = \exp( \tfrac{t}{i \hbar } V ) \vert \psi\rangle$, hence then the solution (eq:StateInTheInteractionPicture) in the [[interaction picture]] would be the result of "propagating" the initial conditions using _only_ the interaction. Now since $V$ may not be assumed to commute with $H_{free}$, the actual form of $\vert \psi(-) \rangle_{I}$ is more complicated. But _infinitesimally_ it remains true that $\vert \psi(-)\rangle_I$ is propagated this way, not by the plain operator $V$, though, but by $V$ viewed in the [[Heisenberg picture]] of the free theory. This is the content of the differential equation (eq:DifferentialEquationInInteractionPicture) below.

But first notice that this will indeed be useful: If an explicit expression for the "state in the [[interaction picture]]" (eq:StateInTheInteractionPicture) is known, then the assumption that also the operator $\exp\left({\tfrac{t}{i \hbar} H_{free}}\right)$ is sufficiently well understood implies that the actual solution

$$
  \vert \psi(t) \rangle_S = \exp\left({\tfrac{t}{i \hbar} H_{free}}\right) \vert \psi(t) \rangle_I
$$

is under control. Hence the question now is how to find $\vert \psi(-)\rangle_I$ given its value at some time $t$. (It is conventional to consider this for $t \to \pm \infty$, see (eq:SMatrixInQuantumMechanics) below.)

Now it is clear from the construction and using the [[product law]] for [[differentiation]], that $\vert \psi(-)\rangle_S$ satisfies the following [[differential equation]] ("[[Schrödinger equation]] in [[interaction picture]]"):

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

is known as the [[interaction]] term $V$ "viewed in the [[interaction picture]]". But in fact this is just $V$ "viewed in the [[Heisenberg picture]]", but for the _free_ theory. By our running assumption that the free theory is well understood, also $V_I(t)$ is well understood, and hence all that remains now is to find a sufficiently concrete solution to equation (eq:DifferentialEquationInInteractionPicture). This is the heart of working in the interaction picture.

Solutions to equations of the "[[parallel transport]]"-type such as (eq:DifferentialEquationInInteractionPicture) are given by [[time-ordered product|time-ordering]] of Heisenberg picture operators, denoted $T$, applied to the naive exponential solution as above. This is known as the _[[Dyson formula]]_:

$$
  \label{DysonFormula}
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

Beware the conventional abuse of notation here: Strictly speaking time ordering acts on the [[tensor algebra]] spanned by the $\{V_I(t)\}_{t \in \mathbb{R}}$ and has to be _followed_ by taking tensor products to actual products.

In applications to [[scattering]] processes one is interest in prescribing the [[quantum state]]/[[wave function]] far in the past, hence for $t \to - \infty$, and computing its form far in the future, hence for $t \to \infty$.

The operator that sends such "asymptotic ingoing-states" $\vert \psi(-\infty) \rangle_I$ to "asymptic outgoing states" $\vert \psi(+ \infty) \rangle_I$ is hence the [[limit of a sequence|limit]]

\[
  \label{SMatrixInQuantumMechanics}
  \mathcal{S}(V_I)
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

For example if $V_{I,1}$ and $V_{I,2}$ are two [[interactions]] such that the [[support]] in [[time]] of $V_{I,1}$
is _after_ the support of $V_{I,2}$:

$$
  \left\{
  \array{
    \left(t \gt t_0 \right) &\Rightarrow& V_{I,2} = 0
    \\
    \left(t \lt t_0 \right) &\Rightarrow& V_{I,1} = 0
  }
  \right.
$$

then, assuming the S-matrix for $V_{I,1}$, $V_{I,2}$ and $V_I \coloneqq V_{I,1} + V_{I,2}$ exists, the [[Dyson formula]] (eq:DysonFormula)
implies the "[[causal factorization]]"

$$
  \label{IntegralVersionSchroedingerEquationInInteractionPicture}
  \mathcal{S}(V_{I,1} + V_{I,2})
  \;=\;
  \mathcal{S}(V_{I,1}) \, \mathcal{S}(V_{I,2})
$$

Conversely, decomposing any $V_I(t)$ with the [[step function]] $\Theta$ as

$$
  V_I(t)
    \;=\;
  \underset{ \coloneqq V_{I,1}(t) }{\underbrace{V_I(t) \Theta(t-t_0)}}
   \;+\;
  \underset{ \coloneqq V_{I,2}(t) }{\underbrace{V_I(t)\Theta(t_0 - t)}}
$$

then this [[causal factorization]]-relation may be understood as the integral version of the
"[[Schrödinger equation]] in the [[interaction picture]]" (eq:DifferentialEquationInInteractionPicture).

It is this "integral-version of the [[Schrödinger equation]] in the [[interaction picture]]" (eq:IntegralVersionSchroedingerEquationInInteractionPicture) that has a fairly
evident generalization from [[quantum mechanics]] to [[relativistic field theory|relativistic]] [[perturbative quantum field theory]]
in the form of _[[causal perturbation theory]]_, def. \ref{LagrangianFieldTheoryPerturbativeScattering} below, see remark \ref{DysonCausalFactorization} below that.




### In perturbative relativistic Lagrangian QFT -- Causal perturbation theory
 {#InCausalPerturbationTheory}

> under construction

In [[perturbative algebraic quantum field theory]] the broad structure of the [[interaction picture]] in [[quantum mechanics]] ([above](#InQuantumMechanics)) remains a very good guide, but various technical details have to be generalized with due care:

1. The algebra of operators in the [[Heisenberg picture]] of the free theory becomes the _[[Wick algebra]]_ of the [[free field theory]] (taking into account "normal ordering" of field operators) defined on _[[microcausal functionals]]_ built from [[operator-valued distributions]] with constraints on their [[wave front set]].

1. The [[time-ordered products]] in the [[Dyson formula]] have to be refined to [[causal locality|causally ordered]] products and the resulting product at coincident points has to be defined by [[point-extension of distributions]] -- the freedom in making this choice is the [[renormalization]] freedom ("conter-terms").

1. The sharp interaction cutoff in the [[Dyson formula]] that is hidden in the integration over $[t_0,t]$ has to be smoothed out by [[adiabatic switching]] of the interaction (making the whole S-matrix an [[operator-valued distribution]]).

Together these three points are taken care of by the axiomatization of the "[[adiabatic switching|adiabatically switched]] [[S-matrix]]" according to **[[causal perturbation theory]]**.






#### Perturbative S-Matrices
 {#PerturbativeSMatrixAndTimeOrderedProducts}

We consider here the [[axioms]] for perturbative S-matrices relative to a fixed [[relativistic field theory|relativistic]] [[free field theory|free]] [[Lagrangian field theory|Lagrangian]] [[quantum field theory|quantum field]] [[vacuum]] (def. \ref{VacuumFree} below) according to _[[causal perturbation theory]]_ (def. \ref{LagrangianFieldTheoryPerturbativeScattering} below).
Since the first of these axioms requires the S-matrix to be a formal sum of [[multilinear map|multi-]][[linear continuous functionals]], it is convenient to impose axioms on these directly: this is the axiomatics for _[[time-ordered products]]_
in def. \ref{TimeOrderedProduct} below. That these latter axioms already imply the former
is the statement of prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix} below. Its proof
requires a close look at the "[[reverse-time ordered products]]" for the inverse S-matrix (def. \ref{ReverseTimeOrderedProduct} below)
and their induced reverse-causal factorization (prop. \ref{ReverseCausalFactorizationOfReverseTimeOrderedProducts} below).

$\,$

In considering [[perturbative QFT]], we are considering [[perturbation theory]] around a fixed [[free field theory|free]]
[[Lagrangian field theory|Lagrangian]] [[quantum field theory]] in a chosen [[Hadamard vacuum state]].
For convenient referencing we collect all the structure and notation that goes into this in the following definition:

+-- {: .num_defn #VacuumFree}
###### Definition
**([[free field theory|free]] [[relativistic field theory|relativistic]] [[Lagrangian field theory|Lagrangian]] [[quantum field theory|quantum field]] [[vacuum]])**

Let

1. $\Sigma$ be a [[spacetime]] (e.g. [[Minkowski spacetime]]);

1. $(E,\mathbf{L})$ a [[free field theory|free]] [[Lagrangian field theory]] ([this def.](A+first+idea+of+quantum+field+theory#FreeFieldTheory)), with [[field bundle]] $E \overset{fb}{\to} \Sigma$;

1. $\mathcal{G} \overset{fb}{\to} \Sigma$ a [[gauge parameter bundle]] for $(E,\mathbf{L})$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeParameters)), with induced [[BRST-complex|BRST]]-[[reduced phase space|reduced]] [[Lagrangian field theory]] $\left( E \times_\Sigma \mathcal{G}[1], \mathbf{L} - \mathbf{L}_{BRST}\right)$ ([this example](A+first+idea+of+quantum+field+theory#LocalOffShellBRSTComplex));

1. $(E_{\text{BV-BRST}}, \mathbf{L}' - \mathbf{L}'_{BRST})$ a [[gauge fixing]] ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) with [[graded manifold|graded]] [[BV-BRST formalism|BV-BRST]] [[field bundle]] $E_{\text{BV-BRST}} = T^\ast_{\Sigma}[-1]\left( E\times_\Sigma \mathcal{G}[1] \times_\Sigma A \times_\Sigma A[-1]\right)$ ([this remark](A+first+idea+of+quantum+field+theory#FieldBundleBVBRST));

1. $\Delta_H \in \Gamma'( E_{\text{BV-BRST}} \boxtimes E_{\text{BV-BRST}} )$ a [[Wightman propagator]] $\Delta_H = \tfrac{i}{2} \Delta + H$ compatible with the [[causal propagator]] $\Delta$ which corresponds to the [[Green hyperbolic partial differential equation|Green hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] induced by the [[gauge fixing|gauge-fixed]] [[Lagrangian density]] $\mathbf{L}'$.

Given this, we write

$$
  \left(
    {\, \atop \,}
    PolyObs(E_{\text{BV-BRST}})_{mc}[ [\hbar] ] \;,\;
   \star_H
   {\, \atop \,}
  \right)
$$

for the corresponding [[Wick algebra]]-[[structure]] on [[formal power series]] in $\hbar$ ([[Planck's constant]]) of [[microcausal polynomial observables]]. This is a [[star algebra]] with respect to ([[coefficient]]-wise) [[complex conjugation]]. Write

$$
  \label{HadamardVacuumStateForFreeFieldTheory}
  \array{
    PolyObs(E_{\text{BV-BRST}})_{mc}[ [\hbar] ]
     &\overset{\langle - \rangle}{\longrightarrow}&
    \mathbb{C}[ [\hbar] ]
    \\
    A &\mapsto& A(\Phi = 0)
  }
$$

for the induced [[Hadamard vacuum state]] ([this prop.](Wick+algebra#WickAlgebraCanonicalState)), hence the [[state on a star-algebra|state]] whose [[2-point function]] is the chosen [[Wightman propagator]]:

$$
  \left\langle \mathbf{\Phi}^a(x) \mathbf{\Phi}^b(y)\right\rangle
  \;=\;
  \hbar \, \Delta_H^{a b}(x,y)
  \,.
$$

Write

$$
  \label{NormalOrderingLocalObservables}
  \array{
    LocObs(E_{\text{BV-BRST}})
      &\overset{\phantom{A}:(-):\phantom{A}}{\hookrightarrow}&
    PolyObs(E_{\text{BV-BRST}})_{mc}
    \\
    A &\mapsto& :A:
  }
$$

for the inclusion of [[local observables]] into [[microcausal polynomial observables]] ([this example](A+first+idea+of+quantum+field+theory#PointwiseProductsOfFieldObservablesAdiabaticallySwitchedIsMicrocausal)), thought of as forming [[normal-ordered products]] in the [[Wick algebra]] (by [this def.](A+first+idea+of+quantum+field+theory#NormalOrderedProductNotation)).

We denote the [[Wick algebra]]-product (the [[star product]] $\star_H$ induced by the [[Wightman propagator]] $\Delta_H$) by juxtaposition ([this def.](A+first+idea+of+quantum+field+theory#NormalOrderedProductNotation))

$$
  A_1 A_2 \;\coloneqq\; A_1 \star_H A_2
  \,.
$$

If an element $A \in PolyObs(E_{\text{BV-BRST}})$ has an [[inverse]] with respect to this product, we denote that by
$A^{-1}$:

$$
  A^{-1} A = 1
  \,.
$$

For $A \in LocObs(E_{\text{BV-BRST}})$ we write $supp(A) \subset \Sigma$ for its spacetime support ([this def.](A+first+idea+of+quantum+field+theory#SpacetimeSupport)).
For $S_1, S_2 \subset \Sigma$ two [[subsets]] of [[spacetime]] we write $S_1 {\vee\!\!\!\wedge} S_2$ for the  [[causal ordering]]-[[relation]]
"$S_1$ does not intersect the [[past cone]] of $S_2$", equivalently "$S_2$ does not intersect the [[future cone]] of $S_1$".


=--

+-- {: .num_remark}
###### Remark

For the purposes of constructing or defining the Wick algebra, the conditions on $\Delta_H$ or $H$ could be relaxed. Requiring $\Delta_H$ to be an honest [[Wightman propagator]] means that it is a distribution satisfying the [[Hadamard distribution|Hadamard wavefront condition]], as well as addition positivity and normalization requirements. Dropping the positivity and some of the normalization requirements, $\Delta_H$ is then only a _Hadamard parametrix_ for the Wightman propagator. The construction of the Wick algebra with respect to $\Delta_H$ still makes sense, but $:(-):$ can no longer be interpreted as normal ordering with respect to a fixed vacuum state. In fact, in [[locally covariant pAQFT]], the property for $\Delta_H$ to be the Wightman propagator for a state is in conflict with local covariance. On the other hand, there is no problem with selecting a locally covariant Hadamard parametrix $\Delta_H$, which allows the construction or definition of the Wick algebra to be locally covariant.

=--

+-- {: .num_defn #LagrangianFieldTheoryPerturbativeScattering}
###### Definition
**([[S-matrix]] [[axioms]] -- [[causal perturbation theory]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

Then a _perturbative [[S-matrix]] scheme_ for [[perturbative QFT]] around this [[free field|free]] [[vacuum]] is a [[function]]

$$
  \mathcal{S}
    \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [\hbar , g, j] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g,j ] ]
$$

from [[local observables]] to [[microcausal polynomial observables]] of the free vacuum theory,  with formal parameters adjoined as indicated ([[Laurent series]] in [[Planck's constant]] $\hbar$ and [[formal power series]] in [[coupling constant]] $g$ and [[source field]] coupling $j$)
such that the following two conditions "perturbation" and "causal additivity (jointly: "[[causal perturbation theory]]") hold:

1. ([[perturbative quantum field theory|perturbation]])

   There exist [[multilinear map|multi-]][[linear continuous functionals]] (over $\mathbb{C}[ [\hbar, g, j] ]$) of the form

   $$
     T_k
       \;\colon\;
     \left(
       {\, \atop \,}
       PolyLocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]
       {\, \atop \,}
     \right)^{\otimes^k_{\mathbb{C}[ [\hbar, g, j] ]}}
       \longrightarrow
     PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g, j ] ]
   $$

   for all $k \in \mathbb{N}$, such that:

   1. The nullary map is [[constant function|constant]] on the [[neutral element|unit]] of the [[Wick algebra]]

      $$
        T_0(A) = 1
      $$

   1. The unary map is the inclusion of [[local observables]] as [[normal-ordered products]] (eq:NormalOrderingLocalObservables)

      $$
        T_1(A) = :A:
      $$

   1. The perturbative S-matrix is the [[exponential series]] of these maps in that for 
      all $S_{int}, A  \in LocObs(E_{\text{BV-BRST}})[ [\hbar] ] $

      $$
        \label{ExponentialSeriesScatteringMatrix}
        \begin{aligned}
          \mathcal{S}( g S_{int} + j A)
          & =
          T
          \left(
            \exp_{\otimes}
            \left(
              \tfrac{ 1 }{i \hbar}
              \left(
                g S_{int} + j A
              \right)
            \right)
          \right)
          \\
          & \coloneqq
          \underoverset{k = 0}{\infty}{\sum}
          \frac{1}{k!}
          \left( \frac{1}{i \hbar} \right)^k
          T_k
          \left(
            {\, \atop \,}
            \underset{k\,\text{arguments}}{\underbrace{ (g S_{int}  + jA) , \cdots,  (g S_{int} + j A)  }}
          {\, \atop \,}
          \right)
        \end{aligned}
      $$

1. ([[causal additivity]])

   For all [[local observables]] $S_{int}, A_1, A_2 \in LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]$ we have

   $$
     \label{CausalAdditivity}
     \left(
        {\, \atop \,}
        supp(A_1) {\vee\!\!\!\wedge} supp(A_2)
        {\, \atop \,}
     \right)
     \;\; \Rightarrow \;\;
     \left(
       {\, \atop \,}
       \mathcal{S}(g S_{int} + j A_1 + j A_2)
       =
       \mathcal{S}(g S_{int} + j A_1) \, \mathcal{S}(g S_{int})^{-1} \, \mathcal{S}(g S_{int} + j A_2)
       {\, \atop \,}
     \right)
     \,.
   $$

(The [[inverse]] $\mathcal{S}(g S_{int})^{-1}$ of $\mathcal{S}(g S_{int})$ with respect to the [[Wick algebra]]-[[structure]]
is implied to exist by axiom "perturbation", see remark \ref{PerturbativeSMatrixInverse} below.)

=--

Def. \ref{LagrangianFieldTheoryPerturbativeScattering} is due to ([Epstein-Glaser 73 (1)](#EpsteinGlaser73)),
in view of lemma \ref{CausalLocalityOfThePerturbativeSMatrix} below, following ([Stückelberg 49-53](causal+perturbation+theory#Stueckelberg49), [Bogoliubov-Shirkov 59](causal+perturbation+theory#BogoliubovShirkov59)).
That the [[domain]] of a S-matrix scheme is indeed the space of [[local observables]] was made explicit (in terms of axioms for the [[time-ordered products]], see def. \ref{TimeOrderedProduct} below), in ([Brunetti-Fredenhagen 99, section 3](#BrunettiFredenhagen99), [D&#252;tsch-Fredenhagen 04, appendix E](#DuetschFredenhagen04), [Hollands-Wald 04,  around (20)](#HollandsWald04)). Review includes ([Rejzner 16, around def. 6.7](#Rejzner16), [Dütsch 18, section 3.3](#Duetsch18)).

+-- {: .num_remark #PerturbativeSMatrixInverse}
###### Remark
**([[inverse|invertibility]] of the [[S-matrix]])**

The mutliplicative inverse $S(-)^{-1}$ of the perturbative S-matrix in def. \ref{LagrangianFieldTheoryPerturbativeScattering}
indeed exists, so that the list of axioms is indeed well defined: By the axiom "perturbation" this follows with the usual formula for the multiplicative inverse of [[formal power series]] that are non-vanishing in degree 0:

If we write

$$
  \mathcal{S}(g S_{int} + j A) = 1 + \mathcal{D}(g S_{int} + j A)
$$

then

$$
  \label{InfverseOfPerturbativeSMatrix}
  \begin{aligned}
    \left(
      {\, \atop \,}
      \mathcal{S}(g S_{int} + j A)
      {\, \atop \,}
    \right)^{-1}
    &=
    \left(
      {\, \atop \,}
      1 + \mathcal{D}(g S_{int} + j A)
      {\, \atop \,}
    \right)^{-1}
    \\
    & =
    \underoverset{r = 0}{\infty}{\sum}
    \left(
      {\, \atop \,}
      -\mathcal{D}(g S_{int} + j A)
      {\, \atop \,}
    \right)^r
  \end{aligned}
$$

where the sum does exist in $PolyObs(E_{\text{BV-BRST}})((\hbar))[ [[ g,j ] ]$, because (by
the axiom "perturbation")
$\mathcal{D}(g S_{int} + j A)$ has vanishing coefficient in zeroth order in the formal parameters $g$ and $j$, so that
only a finite sub-sum of the formal infinite sum contributes in each order in $g$ and $j$.

This expression for the inverse of S-matrix may usefully be re-ordganized in terms of "rever-time ordered products" (def. \ref{ReverseTimeOrderedProduct} below), see prop. \ref{ReverseTimOrderedProductsGiveReverseSMatrix} below.

=--

Given a perturbative [[S-matrix]] scheme (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) it immediately
induces a corresponding concept of [[observables]]:

+-- {: .num_defn #SchemeGeneratingFunction}
###### Definition
**([[generating function]] scheme for [[interacting field observables]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}.

Then corresponding _[[generating function]] scheme_
(for [[interacting field algebra|interacting field observables]], def. \ref{InteractingFieldObservables} below) is the functional

$$
  \mathcal{Z}_{(-)}(-)
    \;\colon\;
  \left(
    {\, \atop \,}
    LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]
    {\, \atop \,}
  \right)^2
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [g , j] ]
$$

given by

$$
  \label{GeneratingFunctionInducedFromSMatrix}
  \mathcal{Z}_{S_{int}}(A)
    \;\coloneqq\;
  \mathcal{S}(S_{int})^{-1} \mathcal{S}( S_{int} + A )
  \,.
$$

=--


+-- {: .num_prop #ZCausalAdditivity}
###### Proposition
**([[causal additivity]] in terms of [[generating functions]])**

In terms of the [[generating functions]] $\mathcal{Z}$ (def. \ref{SchemeGeneratingFunction}) the axiom "causal additivity" 
on the [[S-matrix]] scheme $\mathcal{S}$ (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) is equivalent to

* ([[causal additivity]] in terms of $\mathcal{Z}$)

  For all [[local observables]] $S_{int}, A_1, A_2 \in LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]$ we have

  $$
    \label{GeneratingFunctionCausalAdditivity}
    \begin{aligned}
    \left(
       {\, \atop \,}
       supp(A_1) {\vee\!\!\!\wedge} supp(A_2)
       {\, \atop \,}
    \right)
    & \;\; \Rightarrow \;\;
    \left(
      {\, \atop \,}
      \mathcal{Z}_{S_{int}}(A_1) \, \mathcal{Z}_{S_{int}}(A_2)
      =
      \mathcal{Z}_{S_{int}}(A_1 + A_2)
      {\, \atop \,}
    \right)
    \\
    & \;\; \Leftrightarrow \;\;
    \left(
      {\, \atop \,}
      \mathcal{Z}_{S_{int} + A_1}(A_2)
      =
      \mathcal{Z}_{S_{int}}(A_2)
      {\, \atop \,}
    \right)
    \end{aligned}
    \,.
  $$

(Whence "additivity".)

=--

+-- {: .proof}
###### Proof

This follows by elementary manipulations:

Multiplying both sides of (eq:CausalAdditivity) by $\mathcal{S}(g S_{int})^{-1}$ yields

$$
  \underset{
    \mathcal{Z}_{g S_{int}}(j A_1 + j A_2)
  }{
  \underbrace{
    \mathcal{S}(g S_{int})^{-1} 
    \mathcal{S}(g S_{int} + j A_1 + j A_2)
  }
  }
  \;=\;
  \underset{
    \mathcal{Z}_{g S_{int}}( j A_1 )
  }{
  \underbrace{
    \mathcal{S}(g S_{int})^{-1} \mathcal{S}(g S_{int} + j A_1)
  }
  }
  \underset{
    \mathcal{Z}_{g S_{int}}(j A_2)
  }{
  \underbrace{
    \mathcal{S}(g S_{int})^{-1} \mathcal{S}(g S_{int} + j A_2) 
  }
  }
$$

This is the first line of (eq:GeneratingFunctionCausalAdditivity).


Multiplying both sides of (eq:CausalAdditivity) by $\mathcal{S}(g S_{int} + j A_1)^{-1}$ yields

$$
  \underset{
    = \mathcal{Z}_{g S_{int} + j A_1}(j A_2)
  }{
  \underbrace{
    \mathcal{S}(g S_{int} + j A_1)^{-1}
    \mathcal{S}(g S_{int} + j A_1 + j A_2)
  }
  }
  \;=\;
  \underset{
    = \mathcal{Z}_{g S_{int}}(j A_2)
  }{
  \underbrace{
    \mathcal{S}(g S_{int})^{-1} \mathcal{S}(g S_{int} + j A_2)
  }
  }
  \,.
$$

This is the second line of (eq:GeneratingFunctionCausalAdditivity).


=--


+-- {: .num_defn #InteractingFieldObservables}
###### Definition
**([[interacting field observables]] -- [[Bogoliubov's formula]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}, and let $S_{int} \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ]$ be a [[local observable]] regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]]-[[action functional|functional]].

Then for $A \in LocObs(E_{\text{BV-BRST}})[ [\hbar] ]$ a [[local observable]] of the [[free field theory]], write

$$
  A_{int} \in PolyObs(E_{\text{BV-BRST}})_{mc}[ [\hbar, g] ]
$$

for the [[coefficient]] of $j^1$ in the [[generating function]] (eq:GeneratingFunctionInducedFromSMatrix):

$$
  \label{BogoliubovsFormula}
  \begin{aligned}
    A_{int}
    &\coloneqq
    i \hbar \frac{d}{d j}
    \left(
      {\, \atop \,}
      \mathcal{Z}_{S_{int}}( j A ) 
      {\, \atop \,}
    \right)_{\vert_{j = 0}}
    \\
    & \coloneqq
    i \hbar \frac{d}{d j} 
    \left(
      {\, \atop \,}
      \mathcal{S}^{-1}(S_{int}) \, \mathcal{S}( S_{int} + j A )
      {\, \atop \,}
    \right)_{\vert_{j = 0}}
  \end{aligned}
$$

This expression is called _[[Bogoliubov's formula]]_, due to ([Bogoliubov-Shirkov 59](#BogoliubovShirkov59)).
The assignment $A \mapsto A_{int}$ is also called the _[[quantum Møller operator]]_ ([Hawkins-Rejzner 16](perturbative+algebraic+quantum+field+theory#HawkinsRejzner16)).

One thinks of $A_{int}$ as the [[deformation]] of the observable $A$ as the [[interaction]] $S_{int}$ is turned on; and speaks of an element of the _[[interacting field algebra of observables]]_. Their value ("[[expectation value]]") in the given free [[Hadamard vacuum state]] 
$\langle  -\rangle$ (def. \ref{VacuumFree}) is a [[formal power series]] in [[Planck's constant]] $\hbar$ and in the [[coupling constant]] $g$, with [[coefficients]] in the [[complex numbers]]

$$
  \left\langle
    A_{int}
  \right\rangle
  \;\in\;
  \mathcal{C}[ [\hbar, g] ]
$$

which express the [[probability amplitudes]] that reflect the predictions of the [[perturbative QFT]], which may be compared to [[experiment]].

=--

([Epstein-Glaser 73, around (74)](#EpsteinGlaser73); review includes ([D&#252;tsch-Fredenhagen 00, around (17)](#DuetschFredenhagen00), [Dütsch 18, around (3.212)](pAQFR#Duetsch18)).

+-- {: .num_example #FormalPowerSeriesInteractingFieldObservables}
###### Remark
**([[interacting field observables]] are [[formal deformation quantization]])**

The [[interacting field observables]] in def. \ref{InteractingFieldObservables} are indeed [[formal power series]] in the formal parameter $\hbar$ ([[Planck's constant]]), as opposed to being more general [[Laurent series]], hence they involve no [[negative number|negative]] powers of $\hbar$ ([Dütsch-Fredenhagen 00, prop. 2 (ii)](interacting+field+observable#DuetschFredenhagen00), [Hawkins-Rejzner 16, cor. 5.2](interacting+field+observable#HawkinsRejzner16)).  This is not immediate, since by def. \ref{LagrangianFieldTheoryPerturbativeScattering} the [[S-matrix]] that they are defined from does involve negative powers of $\hbar$. 

It follows in particular that the [[interacting field observables]] have a [[classical limit]] $\hbar \to 0$. Indeed they constitute a [[formal deformation quantization]] of the interacting [[Peierls-Poisson bracket]] ([Collini 16](interacting+field+algebra+of+observables#Collini16), [Hawkins-Rejzner 16](interacting+field+algebra+of+observables#HawkinsRejzner16)).

=--


$\,$

#### Time-ordered products

Definition \ref{LagrangianFieldTheoryPerturbativeScattering} suggests to focus on the multilinear operations $T(...)$ which define the perturbative [[S-matrix]] order-by-order in $\hbar$. We impose [[axioms]] on these _[[time-ordered products]]_ directly (def. \ref{TimeOrderedProduct}) and then prove that these axioms imply the axioms for the corresponding [[S-matrix]] (prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix} below).


+-- {: .num_defn #TimeOrderedProduct}
###### Definition
**([[time-ordered product]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

A _[[time-ordered product]]_ is a sequence of [[multilinear map|multi-]][[linear continuous functionals]] for all $k \in \mathbb{N}$ of the form

$$
  T_k
    \;\colon\;
  \left(
    {\, \atop \,}
    LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]
    {\, \atop \,}
  \right)^{\otimes^k_{\mathcal{C}[ [\hbar, g, j] ]}}
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}((\hbar))[ [g , j] ]
$$

(from [[tensor products]] of [[local observables]] to [[microcausal polynomial observables]], with formal parameters adjoined as shown)
such that the following conditions hold for all possible arguments:

1. (normalization)

   $$
     T_0(A) = 1
   $$

1. (perturbation)

   $$
     T_1(A) =  :A:
   $$

1. (symmetry) each $T_k$ is graded-symmetric in its arguments, in that

   $$
     \left(
       {\, \atop \,}
       A_{\sigma(1)} \cdot A_{\sigma(2)} \cdots A_{\sigma(k-1)} \cdot  A_{\sigma(k)}
       = (-)^\epsilon A_1 \cdot A_2 \cdots A_{k-1} \cdot A_k
       {\, \atop \,}
     \right)
     \;\;\Rightarrow\;\;
     \left(
       {\, \atop \,}
       T_k(A_{\sigma(1)}, \ldots, A_{\sigma(k)})
       = (-)^\epsilon T_k(A_1, \ldots, A_k)
       {\, \atop \,}
     \right)
   $$

   for all [[tuples]] of [[local observables]] $A_1, \ldots, A_k \in LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]$ and any [[permutation]] $\sigma\in \Sigma(k)$

1. ([[causal factorization]]) If

   $$
     \left(
       {\, \atop \,}
       supp(A_1)
         \cup
         \cdots
         \cup
       supp(A_r)
       {\, \atop \,}
     \right)
       \;{\vee\!\!\!\wedge}\;
     \left(
       {\, \atop \,}
       supp(A_{r+1})
         \cup
         \cdots
         \cup
       supp(A_k)
       {\, \atop \,}
     \right)
   $$

   then

   $$
     T(A_1, \cdots, A_k)
     \; = \;
     T( A_1,   \cdots , A_r )
     \,
     T( A_{r+1},   \cdots , A_k )
     \,.
   $$

=--

+-- {: .num_remark #NotationForTimeOrderedProductsAsGeneralizedFunctions}
###### Remark
**([[time-ordered products]] as [[generalized functions]])**

It is convenient (as in [Epstein-Glaser 73](#EpsteinGlaser73)) to think of [[time-ordered products]] (def. \ref{TimeOrderedProduct}), being
[[Wick algebra]]-valued [[distributions]] (hence [[operator-valued distributions]] if we were to choose a [[representation]] of the
[[Wick algebra]] by [[linear operators]] on a [[Hilbert space]]), as [[generalized functions]] depending on spacetime points:

If

$$
  \left\{
    \alpha_ \in \Omega^{p+1,0}_\Sigma(E_{\text{BV-BRST}})\langle g \rangle
  \right\}
  \cup
  \left\{
    \beta_j \in \Omega^{p+1,0}_\Sigma(E_{\text{BV-BRST}})\langle j \rangle
  \right\}
$$

is a [[finite set]] of [[horizontal differential forms]], and

$$
  \left\{
    g_i, j_{j} \in C^\infty_{cp}(\Sigma)
  \right\}
$$

is a corresponding set of [[bump functions]] on [[spacetime]] ([[adiabatic switchings]]), so that

$$
  \left\{
    S_j
      \colon
    \Phi
      \mapsto
    \underset{\Sigma}{\int} g_i(x) \, \left(j^\infty_\Sigma(\Phi)^\ast \alpha_i\right)(x)\, dvol_\Sigma(x)
  \right\}
  \;\cup\;
  \left\{
    A_j
      \colon
    \Phi
      \mapsto
    \underset{\Sigma}{\int} j_i(x) \, \left(j^\infty_\Sigma(\Phi)^\ast \beta_i\right)(x)\, dvol_\Sigma(x)
  \right\}
$$

is the corresponding set of [[local observables]], then we may write the [[time-ordered product]]
of these observables as the [[integration]] of these [[bump functions]] against a [[generalized function]]
$T_{(\alpha_i)}$ with values in the [[Wick algebra]]:

$$
  \begin{aligned}
    &
    \underset{\Sigma^n}{\int}
      T_{(\alpha_i), (\beta_j)}(x_1, \cdots, x_{r}, x_{r+1}, \cdots x_{n})
      g_1(x_1) \cdots g_r(x_r)
      \,
      j_1(x_{r+1}) \cdots j_n(x_n)
    \, dvol_{\Sigma^n}(x_1, \cdots x_n)
    \\
    & \coloneqq
      T( S_1, \cdots, S_r, A_{r+1}, \cdots, A_n )
  \end{aligned}
  \,.
$$

Moreover, the subscripts on these [[generalized functions]] will always be
clear from the context, so that in computations we may notationally suppress these.

Finally, due to the "symmetry" axiom in def. \ref{TimeOrderedProduct}, a time-ordered product
depends, up to signs, only on its [[set]] of arguments, not on the order of the arguments. We will write
$\mathbf{X} \coloneqq \{x_1, \cdots, x_r\}$ and $\mathbf{Y} \coloneqq \{y_1, \cdots y_r\}$
for sets of spacetime points, and hence abbreviate the expression for the "value" of the
generalized function in the above as $T(\mathbf{X}, \mathbf{Y})$ etc.

In this condensed notation the above reads

$$
    \underset{\Sigma^{r+s}}{\int}
      T(\mathbf{X}, \mathbf{Y})
      \,
      g_1(x_1) \cdots g_r(x_r)
      j_{r+1}(x_{r+1}) \cdots j_n(x_n)
    \,
    dvol_{\Sigma^{r+s}}(\mathbf{X})
  \,.
$$

=--

This condensed notation turns out to be greatly simplify computations, as it absorbs all the "relative"
combinatorial prefactors:

+-- {: .num_example #ProductOfPerturbationSeriesInGenealizedFunctionNotation}
###### Example
**(product of perturbation series in [[generalized function]]-notation)**

Let

$$
  U(g)
  \coloneqq
  \underoverset{n = 0}{\infty}{\sum}
   \frac{1}{n!}
   \int U(x_1, \cdots, x_n)
   \,
   g(x_1) \cdots g(x_n) \, dvol
$$

and

$$
  V(g)
  \coloneqq
  \underoverset{n = 0}{\infty}{\sum}
   \frac{1}{n!}
   \int V(x_1, \cdots, x_n)
   \,
   g(x_1) \cdots g(x_n) \, dvol
$$

be power series of [[Wick algebra]]-valued [[distributions]] in the [[generalized function]]-notation of remark \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}.

Then their product $W(g) \coloneqq U(g) V(g)$ with [[generalized function]]-representation

$$
  W(g)
  \coloneqq
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

=--

([Epstein-Glaser 73 (5)](#EpsteinGlaser73))

+-- {: .proof}
###### Proof

For fixed [[cardinality]] ${\vert \mathbf{I} \vert} = n_1$
the sum over all subsets $\mathbf{I} \subset \mathbf{X}$ overcounts the sum over
[[partitions]] of the coordinates as $(x_1, \cdots x_{n_1}, x_{n_1 + 1}, \cdots x_n)$ precisely by the
[[binomial coefficient]] $\frac{n!}{n_1! (n - n_1) !}$. Here the factor of $n!$ cancels
against the "global" combinatorial prefactor in the above expansion of $W(g)$, while the remaining
factor $\frac{1}{n_1! (n - n_1) !}$ is just the "relative" combinatorial prefactor seen at total order $n$
when expanding the product $U(g)V(g)$.

=--




In order to prove that the axioms for [[time-ordered products]] do imply those for a perturbative [[S-matrix]]
(prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix} below) we need to consider
the corresponding reverse-time ordered products:


+-- {: .num_defn #ReverseTimeOrderedProduct}
###### Definition
**([[reverse-time ordered products]])**

Given a [[time-ordered product]] $T = \{T_k\}_{k \in \mathbb{N}}$ (def. \ref{TimeOrderedProduct}),
its _[[reverse-time ordered product]]_

$$
  \overline{T}_k
    \;\colon\;
  \left(
    {\, \atop \,}
    LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]
    {\, \atop \,}
  \right)
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})((\hbar))[ [g, j] ]
$$

for $k \in \mathbb{N}$ is defined by

$$
  \overline{T}( A_1 \cdots A_n )
  \;\coloneqq\;
  \left\{
    \array{
      \underoverset{r = 1}{n}{\sum}
      (-1)^r
      \underset{\sigma \in Unshuffl(n,r)}{\sum}
      T( A_{\sigma(1)} \cdots A_{\sigma(k_1)} )
      \,
      T( A_{\sigma(k_1 + 1)} \cdots A_{\sigma(k_2)} )
      \cdots
      T( A_{\sigma(k_{r-1}+1)} \cdots A_{\sigma_{k_r}}  )
      &\vert& k \geq 1
      \\
      1 &\vert& k = 0
    }
  \right.
  \,,
$$

where the sum is over all [[unshuffles]] $\sigma$ of $(1 \leq \cdots \leq n)$ into $r$ non-empty
ordered subsequences. Alternatively, in the [[generalized function]]-notation of remark \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}, this reads

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

([Epstein-Glaser 73, (11)](#EpsteinGlaser73))

+-- {: .num_prop #ReverseTimOrderedProductsGiveReverseSMatrix}
###### Proposition
**([[reverse-time ordered products]] express [[inverse]] [[S-matrix]])

Given [[time-ordered products]] $T(-)$ (def. \ref{TimeOrderedProduct}), then the
corresponding reverse time-ordered product $\overline{T}(-)$ (def. \ref{ReverseTimeOrderedProduct})
expresses the [[inverse]] $S(-)^{-1}$ (according to remark \ref{PerturbativeSMatrixInverse}) of the corresponding
perturbative [[S-matrix]] scheme $\mathcal{S}(S_{int}) \coloneqq \underset{k \in \mathbb{N}}{\sum} \tfrac{1}{k!} T(\underset{k\,\text{args}}{\underbrace{S_{int}, \cdots , S_{int}}})$ (def. \ref{LagrangianFieldTheoryPerturbativeScattering}):

$$
  \left(
    {\, \atop \,}
    \mathcal{S}(g S_{int} + j A )
    {\, \atop \,}
  \right)^{-1}
  \;=\;
  \underset{k \in \mathbb{N}}{\sum} 
    \frac{1}{k!}
    \left(
      \frac{1}{i \hbar}
    \right)^k
    \overline{T}( \underset{k \, \text{arguments}}{\underbrace{ (g S_{int} + j A), \cdots, (g S_{int} + j A)}} )
  \,.
$$

=--

+-- {: .proof}
###### Proof

For brevity we write just "$A$" for $\tfrac{1}{i \hbar}(g S_{int} + j A)$. 
(Hence we assume without restriction that $A$ is not independent of
powers of $g$ and $j$; this is just for making all sums in the following be order-wise finite sums.)
 
By definition we have

$$
  \begin{aligned}
  &
  \underset{k \in \mathbb{N}}{\sum}
    \frac{1}{k!}
    \overline{T}( \underset{k \, \text{args}}{\underbrace{A,  \cdots , A}} )
  \\
  & =
  \underset{ k \in \mathbb{N}}{\sum}
    \frac{1}{k!}
    \underoverset{r = 1}{k}{\sum}
    (-1)^r
    \!\!\!\underset{\sigma \in Unshuffl(k,r)}{\sum}\!\!\!
    T( A_{\sigma(1)} \cdots A_{\sigma(k_1)} )
    T( A_{\sigma(k_1 + 1)} \cdots A_{\sigma(k_2)} )
    \cdots
    T( A_{\sigma(k_{r-1}+1)} \cdots A_{\sigma_{k_r}} )
  \end{aligned}
$$

where all the $A_k$ happen to coincide: $A_k = A$.

If instead of [[unshuffles]] (i.e. [[partitions]] into non-empty subsequences preserving the original order) we took
partitions into arbitrarily ordered subsequences,
we would be overcounting by the [[factorial]] of the length of the subsequences, and hence the
above may be equivalently written as:

$$
  \cdots
  =
  \underset{k \in \mathbb{N}}{\sum}
    \tfrac{1}{k!}
    \underoverset{r = 1}{k}{\sum}
    (-1)^r
    \!\!\!
    \underset{ {\sigma \in \Sigma(k)} \atop { { k_1 + \cdots + k_r = k } \atop { \underset{i}{\forall} (k_i \geq 1) } } }{\sum}
    \!\!\!
    \tfrac{1}{k_1!} \cdots \tfrac{1}{k_r !}
    \,
    T( A_{\sigma(1)} \cdots A_{\sigma(k_1)} )
    \,
    T( A_{\sigma(k_1 + 1)} \cdots A_{\sigma(k_2)} )
    \cdots
    T( A_{\sigma(k_{r-1}+1)} \cdots A_{\sigma_{k_r}} )
    \,,
$$

where $\Sigma(k)$ denotes the [[symmetric group]] (the set of all [[permutations]] of $k$ elements).

Moreover, since all the $A_k$ are equal, the sum is in fact independent of $\sigma$, it only depends
on the length of the subsequences. Since there are $k!$ permutations of $k$ elements
the above reduces to

$$
  \begin{aligned}
    \cdots
    & =
    \underset{k \in \mathbb{N}}{\sum}
      \underoverset{r = 1}{k}{\sum}
      (-1)^r
      \!\!\!
      \underset{  k_1 + \cdots + k_r = k }{\sum}
      \tfrac{1}{k_1!} \cdots \tfrac{1}{k_r !}
      T( \underset{k_1 \, \text{factors}}{\underbrace{ A, \cdots , A  }}  )
      T( \underset{k_2 \, \text{factors}}{\underbrace{ A, \cdots , A }}  )
      \cdots
      T( \underset{k_r \, \text{factors}}{\underbrace{ A,  \cdots , A }}  )
    \\
    & =
      \underoverset{r = 0}{\infty}{\sum}
      \left(
        - \underoverset{k = 0}{\infty}{\sum} T ( \underset{k\,\text{factors}}{\underbrace{A,  \cdots , A}}   )
      \right)^r
    \\
    & =
      \mathcal{S}(A)^{-1}
      \,,
  \end{aligned}
$$

where in the last line we used (eq:InfverseOfPerturbativeSMatrix).


=--

In fact prop. \ref{ReverseTimOrderedProductsGiveReverseSMatrix} is a special case of the
following more general statement:

+-- {: .num_prop #InversionFormulaForTimeOrderedProducts}
###### Proposition
**(inversion relation for [[reverse-time ordered products]])

Let $\{T_k\}_{k \in \mathbb{N}}$ be [[time-ordered products]] according to def. \ref{TimeOrderedProduct}.
Then the [[reverse-time ordered products]] according to def. \ref{ReverseTimeOrderedProduct}
satisfies the following inversion relation for all $\mathbf{X} \neq \emptyset$
(in the condensed notation of remark \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}):

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
**(reverse [[causal factorization]] of [[reverse-time ordered products]])**

Let $\{T_k\}_{k \in \mathbb{N}}$ be [[time-ordered products]] according to def. \ref{TimeOrderedProduct}.
Then the reverse-time ordered products according to def. \ref{ReverseTimeOrderedProduct} satisfies
reverse-[[causal factorization]].

=--

([Epstein-Glaser 73, around (15)](#EpsteinGlaser73))

+-- {: .proof}
###### Proof

In the condensed notation of remark \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions},
we need to show that for $\mathbf{X} = \mathbf{P} \cup \mathbf{Q}$ with $\mathbf{P} \cap \mathbf{Q} = \emptyset$
then

$$
  \left(
    \mathbf{P} {\vee\!\!\!\wedge} \mathbf{Q}
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
     \!\!\!
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
[[causal factorization]] property of $T(-)$ (which holds by def. \ref{TimeOrderedProduct}) and that of $\overline{T}(-)$
(which holds by the induction assumption, using that $\mathbf{J} \neq \mathbf{X}$ hence that
${\vert \mathbf{J}\vert} \lt {\vert \mathbf{X}\vert}$).

1. in the third line we decomposed the sum over $\mathbf{J}, \mathbf{J}' \subset \mathbf{X}$
into two sums over subsets of $\mathbf{Q}$ and $\mathbf{P}$:

   1. The first summand in the third line is the contribution where $\mathbf{J}'$ has a non-empty intersection with $\mathbf{Q}$. This makes $\mathbf{K}$ range without constraint, and therefore the sum in the middle vanishes, as indicated, as it is the contribution at order ${\vert \mathbf{Q}\vert}$ of the inversion formula from prop. \ref{InversionFormulaForTimeOrderedProducts}.

   1. The second summand in the third line is the contribution where $\mathbf{J}'$ does not intersect $\mathbf{Q}$.
     Now the sum over $\mathbf{K}$ is the inversion formula from prop. \ref{InversionFormulaForTimeOrderedProducts} except for one term, and so it equals that term.

=--

Using these facts about the reverse-time ordered products,
we may finally prove that [[time-ordered products]] indeed do induced a perturbative S-matrix:

+-- {: .num_prop #TimeOrderedProductInducesPerturbativeSMatrix}
###### Proposition
**([[time-ordered products]] induce [[S-matrix]])**

Let $\{T_k\}_{k \in \mathbb{N}}$ be a system of [[time-ordered products]] according to def. \ref{TimeOrderedProduct}.
Then

$$
  \begin{aligned}
    \mathcal{S}(-)
    & \coloneqq
    T 
    \left( 
      \exp_\otimes
      \left(
        \tfrac{1}{i \hbar}(-)
      \right)
    \right)
    \\
    &
    \coloneqq 
    \underset{k \in \mathbb{N}}{\sum} 
    \tfrac{1}{k!}
    \tfrac{1}{(i \hbar)^k}  T( \underset{k \, \text{factors}}{\underbrace{-,  \cdots , -}} )
  \end{aligned}
$$

is indeed a perturbative S-matrix according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}.

=--

+-- {: .proof}
###### Proof

The axiom "perturbation" of the S-matrix is
immediate from the axioms "perturbation" and "normalization" of the time-ordered products.
What requires proof is that [[causal additivity]] of the S-matrix follows from
the [[causal factorization]] property of the time-ordered products.

Notice that also the weaker [[causal factorization]] property of the S-matrix (remark \ref{DysonCausalFactorization})
is immediate from the causal factorization condition on the time-ordered products.

But [[causal additivity]] is stronger. It is remarkable that this, too,
follows from just the time-ordering ([Epstein-Glaser 73, around (73)](#EpsteinGlaser73)):

To see this, first expand the
generating function $\mathcal{Z}$ (eq:GeneratingFunctionInducedFromSMatrix)  into
powers of $g$ and $j$

$$
  \mathcal{Z}_{g S_{int}}(j A)
  \;=\;
  \underoverset{n,m = 0}{\infty}{\sum}
   \frac{1}{n! m!}
   R\left(
      {\, \atop \,}  
      \underset{n\, \text{factors}}{\underbrace{g S_{int},  \cdots ,g S_{int}}},  
      ( \underset{m \, \text{factors}}{ \underbrace{ j A ,  \cdots , j A } }  ) 
      {\, \atop \,}
   \right)
$$

and then compare order-by-order with the given time-ordered product $T$ and
its induced reverse-time ordered product (def. \ref{ReverseTimeOrderedProduct}) via prop. \ref{ReverseTimOrderedProductsGiveReverseSMatrix}.
(These $R(-,-)$ are also called the "generating [[retarded products]], discussed in their own right around def. \ref{RetardedProductFromPerturbativeSMatrix} below.)

In the condensed notation of
remark \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}
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
  \left(supp(A_1) {\vee\!\!\!\wedge} supp(A_2)\right) 
  \Rightarrow 
  \left( Z_{(g S_{int}  + j A_1)}(j A_2) = Z_{S_{int}}(A_2) \right)
$$

and by prop. \ref{ZCausalAdditivity} this is equivalent to [[causal additivity]] of the S-matrix.

It remains to prove the claim:

Consider $\mathbf{X}, \mathbf{Y} \subset \Sigma$ such that the subset $\mathbf{P} \subset \mathbf{Y}$
of points not in the past of $\mathbf{X}$, hence the maximal subset with [[causal ordering]]

$$
  \mathbf{P} {\vee\!\!\!\wedge} \mathbf{X}
  \,,
$$

is non-empty. We need to show that in this case $R(\mathbf{Y}, \mathbf{X}) = 0$ (in the sense of generalized functions).

Write $\mathbf{Q} \coloneqq \mathbf{Y} \setminus \mathbf{P}$
for the complementary set of points, so that all points of $\mathbf{Q}$ are in the past of $\mathbf{X}$.
Notice that this implies that $\mathbf{P}$ is also not in the past of $\mathbf{Q}$:

$$
  \mathbf{P} {\vee\!\!\!\wedge} \mathbf{Q}
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


#### ("Re"-)Normalization
 {#ExistenceAndRenormalization}

So far we considered only the [[axioms]] on a consistent perturbative [[S-matrix]] scheme (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) or equivalently on [[time-ordered products]] (def. \ref{TimeOrderedProduct} prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix}). 
Now we discuss the process of the actual construction of [[time-ordered products]], hence of perturbative [[S-matrices]], by the process called _[[renormalization|("re"-)normalization]] 

We first discuss how [[time-ordered product]], and hence the perturbative S-matrix [above](#PerturbativeSMatrixAndTimeOrderedProducts),
is uniquely determined away from the locus where interaction points coincide (prop. \ref{TimeOrderedProductAwayFromDiagonal} below).
Moreover, we discuss how on that locus the time-ordered product is naturally expressed as a sum
of [[products of distributions]] of [[Feynman propagators]] that are labeled by [[Feynman diagrams]]: the _[[Feynman perturbation series]]_ (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints} below).

This means that the full  [[time-ordered product]] is an [[extension of distributions]] to the locus of coinciding vertices. The space of possible such extensions turns out to be finite-dimensional in each order of $g/\hbar, j/\hbar$, parameterizing the choice of
[[point-supported distributions]] at the interaction points whose [[degree of a distribution|scaling degree]]
is bounded by the given Feynman propagators.

+-- {: .num_defn #TuplesOfCompactlySupportedPolynomialLocalFunctionalsWithPairwiseDisjointSupport}
###### Definition
**([[tuples]] of [[local observables]] with pairwise disjoint spacetime support)**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

For $k \in \mathbb{N}$, write

$$
  \left(
    {\, \atop \,}
    LocPoly(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ] 
    {\, \atop \,}
  \right)^{\otimes^k_{\mathbb{C}[ [\hbar, g, j ] ]}}_{pds}
  \hookrightarrow
  \left(
    {\, \atop \,}
    LocPoly(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ] 
    {\, \atop \,}
  \right)^{\otimes^k_{\mathbb{C}[ [\hbar, g, j ] ]}}
$$

for the linear subspace of the $k$-fold [[tensor product]] of [[local observables]] (as in def. \ref{LagrangianFieldTheoryPerturbativeScattering}, def. \ref{TimeOrderedProduct}) on those tensor products $A_1 \otimes \cdots A_k$ of [[tuples]] with disjoint spacetime [[support]]:

$$
  supp(A_j) \cap supp(A_k) = \emptyset
  \phantom{AAA}
  \text{for} $i \neq j \in \{1, \cdots, k\}$
  \,.
$$

=--

+-- {: .num_prop #TimeOrderedProductAwayFromDiagonal}
###### Proposition
**([[time-ordered product]] away from coinciding interaction points)**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, and let $T = \{T_k\}_{k \in \mathbb{N}}$ be a sequence of [[time-ordered products]] (def. \ref{TimeOrderedProduct})

$$
  T_k
    \;\colon\;
  \left(
    {\, \atop \,}
    LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]
    {\, \atop \,}
  \right)^{\otimes^k_{\mathcal{C}[ [\hbar, g, j] ]}}
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}((\hbar))[ [g , j] ]
$$

Then their [[restriction]] to the subspace of [[tuples]] of [[local observables]] of pairwise disjoint spacetime support (def. \ref{TuplesOfCompactlySupportedPolynomialLocalFunctionalsWithPairwiseDisjointSupport}) is unique (independent of the [[renormalization|"re-"normalization]] freedom in choosing $T$) and is equal to the [[star product]] 

$$
  A_1 \star_{\star_F} A_2
  \;\coloneqq\;
  ((-)\cdot (-)) \circ
  \exp\left(
   \hbar
   \left(
     \underset{\Sigma \times \Sigma}{\int}
     \Delta_F^{a b}(x,y)
     \frac{\delta}{\delta \mathbf{\Phi}^a(x)}
     \otimes
     \frac{\delta}{\delta \mathbf{\Phi}^b(y)}
     \,
     dvol_\Sigma(x)\, dvol_\Sigma(y)
   \right)   
  \right)
  (A_1 \otimes A_2)
$$

that is induced ([this def.](star+product#PropagatorStarProduct)) by the [[Feynman propagator]] $\Delta_F \coloneqq \tfrac{i}{2}(\Delta_+ + \Delta_- + H)$ (corresponding to the [[Wightman propagator]] $\Delta_H = \tfrac{i}{2}(\Delta_+ - \Delta_-) + H$ which is given by the choice of [[free field|free]] [[vacuum]]), in that

$$
  T
  \left(
    {\, \atop \,}
    (g S_{int} + j A), \cdots, (g S_{int} + j A) 
    {\, \atop \,}
  \right)
  \;=\;
  (g S_{int} + j A) 
    \star_F 
    \cdots 
    \star_F 
  (g S_{int} + j A)
  \,.
$$

=--


+-- {: .proof}
###### Proof

First we need to see that the star product $\star_F$ is well defined on the given domain, in that [[Hörmander's criterion]] is met to guarantee that all [[products of distributions]] involved in expanding out the [[exponential]] in the definition of the star-product are well defined:

We proceed by [[induction]] over the number $k$ of arguments.

For $k = 1$ there is nothing to be shown. So assume that the $\Delta_F$-star product of $k$ local observables with pairwise disjoint spacetime support exists as a [[microcausal polynomial observable]] $A_{mc} = A_1 \star_F \cdots \star_F A_k$. We need to see that for $A_{k+1}$ any [[local observable]] whose spacetime support is disjoint from that of all of the $A_i$, hence disjoint from that of $A_{mc}$, the star product $A_{k+1} \star_F A_{mc}$ exists and is again microcausal.

Now since one of the two arguments of the [[star product]] is assumed to be a [[local observable]], the [[products of distributions]] that appear in the star product are of the form (written as [[generalized functions]])

$$
  \left(
    \underset{i}{\prod} D^{n_i}_x\Delta_H(x,y)
  \right)
  \alpha^{(n)}( \underset{k\,\text{args}}{\underbrace{y, y, \cdots, y}}, z_1, \cdots, z_m)
  \,,
$$

where $D^{n_1}$ denoted [[partial derivatives|partial]] [[derivatives of distributions]], and where $\alpha^{(n)}$ are the [[distribution|distributional]] [[coefficients]] of the [[polynomial observable]] $A_{mc}$, and where $x \neq y$, by assumption.

Since the [[derivative of distributions]] preserves or shrinks the [[wave front set]] (by [this prop.](derivative+of+a+distribution#DerivativeOfDistributionRetainsOrShrinksWaveFrontSet))it is sufficient to see that among these the expressions those of the simpler form

$$
  (\Delta_H(x,y))^{k}
  \alpha^{(n)}(y, y, \cdots, y, z_1, \cdots, z_m)
$$

exist as partial [[products of distributions|products of]] [[distributions of several variables]]. 

Now by [this prop.](Feynman+propagator#WaveFronSetsForKGPropagatorsOnMinkowski) the [[wave front set]] of the Feynman propagator $\Delta_H(x,y)$ with contains [[wave vectors]] along $x$ in the [[closed future cone]] of [[covectors]] based on the [[future]] [[light cone]] of $(x-y)$, as well as [[wave vectors]] in the [[closed past cone]] of [[covectors]] based on the [[past]] [[light cone]]:

<center>
<img src="https://ncatlab.org/nlab/files/FeynmanPropagator.png" width="60">
</center>

and similary but with opposite sign for $y$.

This implies first of all that [[Hörmander's criterion]] for the existence of the product $(\Delta_H(x,y))^k$ is satisfied (since the wave front wave vectors at $x$ and at $y$ are all in the [[closed future cone]] or all in the [[closed past cone]] at $x\neq y$, their sum never adds up to zero). Moreover, by [this prop.](product+of+distributions#WaveFrontSetOfProductOfDistributionsInsideFiberProductOfFactorWaveFrontSets) the resulting product has wave front set contained in the fiberwise sum of the wave front sets of the factors, hence is still of the same general form.

With this, finally [this prop.](product+of+distributions#PartialProductOfDistributionsOfSeveralVariables) implies, with the microcausal assumption on $\alpha^{(k)}$, that also the product $ (\Delta_H(x,y))^{k} \alpha^{(n)}(\underset{k\, \text{args}}{\underbrace{y, y, \cdots, y}}, z_1, \cdots, z_m)$ is defined, and a careful look at [this equation](product+of+distributions#eq:CompositionOfIntegralKernelsWaveFronConstraint) shows that its wave front set again satisfies the microcausality condition.

This proves that the star product exists as claimed.

Given that it exists, then by construction it is immediate that satisfies the axioms "perturbation" and "normalization" in def. \ref{TimeOrderedProduct}.

The only non-trivial point to check is that it indeed satisfies "[[causal factorization]]". In [this prop.](Wick+algebra#CausalOrderingTimeOrderedProductOnRegular) this is proven for $\star_F$ applied to [[regular polynomial observables]], but the proof manifestly applies whenever $\star_F$ is defined. The proof there also makes manifest that when defined, then $\star_F$ is in fact the _unique_ solution to causal factorization.

=--

+-- {: .num_defn #ExtensionOfTimeOrderedProoductsRenormalization}
###### Definition
**([[renormalization|("re"-)normalization]] of [[perturbative QFT]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

Prop. \ref{TimeOrderedProductAwayFromDiagonal} implies that the 
problem of constructing a sequence of [[time-ordered products]] (def. \ref{TimeOrderedProduct}), hence, by prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix}, an [[S-matrix]] scheme (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) for [[perturbative quantum field theory]] around the given [[free field]] [[vacuum]], is equivalently a problem of a sequence of compatible _[[extensions of distributions]]_ of the [[star products]] $\underset{k \; \text{arguments}}{\underbrace{(-)\star_F \cdots \star_F (-)}}$ of the [[Feynman propagator]] on $k$ arguments from the [[complement]] $\Sigma^k \setminus diag(\Sigma)$ of the [[diagonal]] of coinciding [[events]]

$$
  \array{
    diag(\Sigma) &\hookrightarrow& \Sigma^k
    \\
    x &\mapsto& (x, \cdots, x)
  }
$$

inside the [[Cartesian products]] $\Sigma^k$ of [[spacetime]] $\Sigma$, along the canonical inclusion

$$
  \Sigma^k \setminus diag(\Sigma)
    \overset{\phantom{AAA}}{\hookrightarrow}
  \Sigma^k
  \,.
$$

This choice of [[extension of distributions]] of the [[time-ordered product]] to coinciding interaction points deserves to be called a choice of _normalization_ of the [[time-ordered product]] (e.g. [Scharf 94, section 4.3](#Scharf95)) but for historical reasons it is known as _[[renormalization]]_ (see remark \ref{TheTraditionalErrorThatLeadsToTheNotoriouDivergencies} and remark \ref{CausalPerturbationTheoryAbsenceOfUVDivergences}).

=--

([Epstein-Glaser 73](#EpsteinGlaser73))


+-- {: .num_theorem #PerturbativeRenormalizationMainTheorem}
###### Theorem
**([[main theorem of perturbative renormalization]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

1. An [[S-matrix]] [[renormalization scheme]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) around this free vacuum exists, and its construction by choices of [[renormalization|("re"-)normalization]] according to def. \ref{ExtensionOfTimeOrderedProoductsRenormalization} involves precisely a [[finite-dimensional vector space]] of choices ("renormalization constants") at each order.

1. Every [[pair]] of choices of perturbative [[S-matrix]] [[renormalization schemes]] $\mathcal{S}$, $\widetilde{\mathcal{S}}$ (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) are related by a unique transformation of the space of [[local observables]] ("adding counterterms to interactions")

   $$
     Z
     \;\coloneqq\;
     LocObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ] 
       \longrightarrow
     LocObs(E_{\text{BV-BRST}})[ [ \hbar, h ] ]
   $$

   via [[precomposition]]

   $$
     \widetilde{\mathcal{S}} \;=\; \mathcal{S} \circ Z
     \,.
   $$

1. The [[group]] of transformations $Z$ arising this is the _[[Stückelberg-Petermann renormalization group]]_. 

> add assumption on Poincare invariance needed

=--

In summary this says that for each free field vacuum, the space of [[renormalization schemes]] for [[perturbative QFT]] around this vacuum is non-empty and is canonically a [[torsor]] over the [[Stückelberg-Petermann renormalization group]].


#### Feynman diagrams
 {#FeynmanDiagram}


By the nature of the exponential expression, this means in each order to
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
Assume it is true for $v {\vee\!\!\!\wedge} 1$ vertices. It follows that

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



$\,$

#### Conceptual remarks
 {#RemarksOnCausalPerturbationTheoryAxioms}

The simple axioms for [[S-matrices]] in [[causal perturbation theory]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) or equivalently (by prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix}) for [[time-ordered products]] (def. \ref{TimeOrderedProduct}), hence for [[interacting field observables]] (def. \ref{InteractingFieldObservables}) have a wealth of
implications and consequences. Before analyzing these formally, we make a few informal remarks meant to put these axioms into perspective:

+-- {: .num_remark #AsymptoticSeriesObservables}
###### Remark
**([[perturbative quantum field theory|perturbative QFT]] and [[asymptotic expansion]] of [[probability amplitudes]])**

Given a perturbative [[S-matrix]] scheme (def. \ref{LagrangianFieldTheoryPerturbativeScattering}), then by remark \ref{FormalPowerSeriesInteractingFieldObservables} the
[[expectation values]] of [[interacting field observables]] (def. \ref{InteractingFieldObservables}) are [[formal power series]]
in the formal parameters $\hbar$ and $g$ (which are interpreted as [[Planck's constant]], and as the [[coupling constant]], respectively):

$$
 \left\langle A_{int} \right\rangle
 \;\in\;
 \mathbb{C}[ [\hbar, g] ]
 \,.
$$

This means that there is _no_ guarantee that these series _[[convergence|converge]]_ for any [[positive real number|positive]]
value of $\hbar$ and/or $g$.
In terms of [[synthetic differential geometry]] this means that in [[perturbative QFT]] the [[deformation]] of the [[classical field theory|classical]] [[free field theory]] by quantum effects (measured by $\hbar$) and [[interactions]] (meaured by $g$) is so very tiny as to actually be [[infinitesimal]]: formal power series may be read as functions on the [[infinitesimal neighbourhood]] in a space of [[Lagrangian field theories]] at the point $\hbar = 0$, $g = 0$.

In fact, a simple argument (due to [Dyson 52](perturbative+quantum+field+theory#Dyson52))
suggests that in realistic field theories these series _never_ converge for _any_ [[positive real number|positive]] value of $\hbar$ and/or $g$. Namely convergence for $g$ would imply a [[positive real number|positive]] _[[radius of convergence]]_ around $g = 0$, which would imply convergence also for $-g$ and even for [[imaginary number|imaginary]] values of $g$, which would however correspond to unstable [[interactions]] for which no converging field theory is to be expected.

In physical practice one tries to interpret these [[formal power series]] as _[[asymptotic expansions]]_ of
actual but hypothetical functions in $\hbar, g$, which reflect the actual but hypothetical _[[non-perturbative quantum field theory]]_
that one imagines is being approximated by [[perturbative QFT]] methods.

For examples such as [[quantum electrodynamics]] and [[quantum chromodynamics]] as in the [[standard model of particle physics]], the truncation of these [[formal power series]] [[scattering amplitudes]] to the first handful of [[loop orders]] in $\hbar$ happens to agree with [[experiment]] (such as at the [[LHC]] collider) to high precision (for [[QED]]) or at least decent precision (for [[QCD]]), at least away from infrared phenomena (see remark \ref{AdiabaticLimit}).

In summary this says that [[perturbative QFT]] is an extremely _coarse_ approximation to what should be genuine [[non-perturbative quantum field theory]], while at the same time it happens to match certain experimental observations to remarkable degree, however only if some ad-hoc truncation of the resulting power series is considered.

This is strong motivation for going beyond [[perturbative QFT]] to understand and construct [[non-perturbative quantum field theory]]. Unfortunately, this is a wide-open problem, away from toy examples. Not a single [[interacting field theory]] in [[spacetime]] [[dimension]] $\geq 4$ has been non-perturbatively quantized. A single aspect of the non-perturbative [[quantization of Yang-Mills theory]] has famously been advertized as one of the _[Millenium Problems](http://www.claymath.org/millennium-problems/yang%E2%80%93mills-and-mass-gap)_ of our age, and speculation about non-perturbative [[quantum gravity]] is the subject of much activity.

Now as the name indicates, the axioms of _[[causal perturbation theory]]_ (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) do
_not_ address [[non-perturbative effect|non-perturbative aspects]] of [[non-perturbative field theory]]; the convergence or non-convergence of the [[formal power series]] that are axiomatized by [[Bogoliubov's formula]] (def. \ref{InteractingFieldObservables}) is _not_ addressed by the theory.
The point of the axioms of [[causal perturbation theory]] is to give rigorous mathematical meaning to _everything else_ in [[perturbative QFT]].

=--


+-- {: .num_remark #DysonCausalFactorization}
###### Remark
**([[Dyson series]] and [[Schrödinger equation]] in [[interaction picture]])**

The axiom "[[causal additivity]]" (eq:CausalAdditivity) on an [[S-matrix]] scheme (def. \ref{LagrangianFieldTheoryPerturbativeScattering})
implies immediately this weaker condition:

* ([[causal factorization]])

  For all [[local observables]] $A_1, A_2 \in LocObs(E_{\text{BV-BRST}})[ [\hbar, h, j] ]$ we have

  $$
    \left(
       {\, \atop \,}
       supp(A_1) {\vee\!\!\!\wedge} supp(A_2)
       {\, \atop \,}
    \right)
    \;\; \Rightarrow \;\;
    \left(
      {\, \atop \,}
      \mathcal{S}(A_1 + A_2)
      =
      \mathcal{S}(A_1) \, \mathcal{S}(A_2)
      {\, \atop \,}
   \right)
  $$

(This is the special case of "causal additivity" for $S_{int} = 0$, using that  by the axiom "perturbation" (eq:ExponentialSeriesScatteringMatrix) we have $\mathcal{S}(0) = 1$.)

If we now think of $A_1$ and $A_2$ themselves as [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functionals]],
then this reads equivalently but more suggestively

  $$
    \left(
       {\, \atop \,}
       supp(S_1) {\vee\!\!\!\wedge} supp(S_2)
       {\, \atop \,}
    \right)
    \;\; \Rightarrow \;\;
    \left(
      {\, \atop \,}
      \mathcal{S}(S_1 + S_2)
      =
      \mathcal{S}(S_1) \, \mathcal{S}(S_2)
      {\, \atop \,}
   \right)
  $$

This exhibits the [[S-matrix]]-scheme as a "[[causal ordering|causally ordered]] [[exponential]]"
or "[[Dyson series]]" of the [[interaction]], hence as a refinement to [[relativistic field theory]] of what in
[[quantum mechanics]] is the "integral version of the [[Schrödinger equation]] in the [[interaction picture]]" (eq:IntegralVersionSchroedingerEquationInInteractionPicture). (See also [Scharf 95, second half of 0.3](#Scharf95)).

While [[causal additivity]] is in fact stronger than [[causal factorization]], we find below that the
evident analogue of [[causal factorization]] imposed directly on the [[time-ordered products]] (def. \ref{TimeOrderedProduct} below)
does _imply_ [[causal additivity]] of the [[S-matrix]] (prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix} below).

The relevance of [[causal additivity]] of the [[S-matrix]], over just [[causal factorization]], is that it implies that
the induced [[interacting field algebra of observables]] (def. \ref{InteractingFieldObservables}) forms a [[causally local net]] (prop. \ref{PerturbativeQuantumObservablesIsLocalnet} below).

=--

+-- {: .num_remark #InterpretationOfPerturbativeSMatrix}
###### Remark
**([[path integral]]-intuition)**

In informal discussion of [[perturbative QFT]] going back to informal ideas of [[Schwinger-Tomonaga-Feynman-Dyson]], the
perturbative [[S-matrix]] is thought of in terms of a would-be _[[path integral]]_, symbolically written

$$
  \mathcal{S}\left(
    g S_{int} + j A
  \right)
  \;\overset{\text{not really!}}{=}\;
  \!\!\!\!\!
  \underset{\Phi \in \Gamma_\Sigma(E_{\text{BV-BRST}})_{asm}}{\int}
  \!\!\!\!\!\!
  \exp\left(
    \tfrac{1}{i \hbar}
    \int_\Sigma
    \left(
      g L_{int}(\Phi) + j A(\Phi)
    \right)
  \right)
  \,
  \exp\left(
    \tfrac{1}{i \hbar}\int_\Sigma L_{free}(\Phi)
  \right) D[\Phi]
  \,.
$$

Here the would-be [[integration]] is thought to be over the [[space of field histories]] $\Gamma_\Sigma(E_{\text{BV-BRST}})_{asm}$ (the [[space of sections]] of the given [[field bundle]]) for [[field histories]] which satisfy given asymptotic conditions at $x^0 \to \pm \infty$; and as these boundary conditions vary the above is regarded as a would-be [[integral kernel]] that defines the required operator in the [[Wick algebra]] (e.g. [Weinberg 95, around (9.3.10) and (9.4.1)](#Weinberg95)).

Beyond toy examples, it is not known how to define the would-be [[measure]] $D[\Phi]$ and it is not known how to make sense of this expression as an actual [[integral]].

The analogous path-integral intuition for [[Bogoliubov's formula]] for [[interacting field observables]] (def. \ref{InteractingFieldObservables}) symbolically reads

$$
  \begin{aligned}
  A_{int}
  & \overset{\text{not really!}}{=}
  \frac{d}{d j}
  \ln
  \left(
  \underset{\Phi \in \Gamma_\Sigma(E)_{asm}}{\int}
  \!\!\!\!
  \exp\left(
    \underset{\Sigma}{\int}
      g L_{int}(\Phi) + j A(\Phi)
  \right)
  \,
  \exp\left( \underset{\Sigma}{\int} L_{free}(\Phi) \right)
  D[\Phi]
  \right)
  \vert_{j = 0}
  \end{aligned}
$$

If here we were to regard the expression

$$
  \mu(\Phi)
  \;\overset{\text{not really!}}{\coloneqq}\;
  \frac{
    \exp\left( \underset{\Sigma}{\int} L_{free}(\Phi) \right)\, D[\Phi]
  }
  {
    \underset{\Phi \in \Gamma_\Sigma(E_{\text{BV-BRST}})_{asm}}{\int}
    \!\!\!\!
    \exp\left( \underset{\Sigma}{\int} L_{free}(\Phi) \right)\, D[\Phi]
  }
$$

as a would-be [[Gaussian measure]] on the [[space of field histories]], normalized to a would-be [[probability measure]], then this formula
would express interacting field observables as ordinary [[expectation values]]

$$
  A_{int}
   \overset{\text{not really!}}{=}
   \!\!\!
  \underset{\Phi \in \Gamma_\Sigma(E_{\text{BV-BRST}})_{asm}}{\int}
  \!\!\!\!\!\!
     A(\Phi)
  \,\mu(\Phi)
  \,.
$$

As before, beyond toy examples it is not known how to make sense of this as an actual [[integration]].

But we may think of the axioms for the [[S-matrix]] in [[causal perturbation theory]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) as rigorously _defining_ the [[path integral]], not analytically as an actual [[integration]], but _[[synthetic mathematics|synthetically]]_ by axiomatizing the properties of the desired _outcome_ of the would-be integration:

The analogy with a well-defined [[integral]] and the usual properties of an [[exponential]] vividly _suggest_
that the would-be [[path integral]] should obey [[causal factorization]]. Instead of trying to make sense of
[[path integral|path integration]] so that this factorization property could then be appealed to as a _consequence_ of general properties
of [[integration]] and [[exponentials]], the axioms of [[causal perturbation theory]] directly prescribe the
desired factorization property, without insisting that it derives from an actual integration.

The great success of [[path integral]]-intuition in the development of [[quantum field theory]], despite the dearth of
actual constructions, indicates that it is not the would-be integration process as such that actually matters in field
theory, but only the resulting properties that this _suggests_ the S-matrix should have; which is what
[[causal perturbation theory]] axiomatizes. Indeed, the simple [[axioms]] of [[causal perturbation theory]]
rigorously _imply_ finite (i.e. [[renormalization|("re"-)normalized]]) [[perturbative quantum field theory]] (see remark \ref{CausalPerturbationTheoryAbsenceOfUVDivergences}).

$$
  \array{
  \array{
    \text{would-be}
    \\
    \text{path integral}
    \\
    \text{intuition}
  }
  &
  \overset{
    \array{
      \text{informally}
      \\
      \text{suggests}
    }
  }{\longrightarrow}
  &
  \array{
    \text{causally additive}
    \\
    \text{scattering matrix}
  }
  &
  \overset{
    \array{
      \text{rigorously}
      \\
      \text{implies}
    }
  }{\longrightarrow}
  &
  \array{
    \text{UV-finite}
    \\
    \text{(i.e. (re-)normalized)}
    \\
    \text{perturbative QFT}
  }
  }
$$

=--



+-- {: .num_remark #FromAxiomaticSMatrixScatteringAmplitudes}
###### Remark
**([[scattering amplitudes]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}, and let

$$
  S_{int} \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ]
$$

be a [[local observable]], regarded
as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

Then for

$$
  A_{in}, A_{out} \in PolyObs(E_{\text{BV-BRST}})_{mc}[ [\hbar] ]
$$

two [[microcausal  polynomial observables]], the corresponding _[[scattering amplitude]]_ is the value (called "[[expectation value]]" when referring to $A^\ast_{out} \, \mathcal{S}(S_{int}) \, A_{in}$, or "matrix element" when freferring to $\mathcal{S}(S_{int})$, or "transition amplitude" when referring to $\left\langle A_{out} \right\vert$ and $\left\vert A_{in} \right\rangle$)

$$
  \left\langle
    A_{out}
    \,\vert\,
    \mathcal{S}(S_{int})
    \,\vert\,
    A_{in}
  \right\rangle
  \;\coloneqq\;
  \left\langle
    A^\ast_{out} \, \mathcal{S}(S_{int}) \, A_{in}
  \right\rangle
  \;\in\;
  \mathcal{C}[ [ \hbar, g ] ]
  \,.
$$

for the [[Wick algebra]]-product $A^\ast_{out} \, \mathcal{S}(S_{int})\, A_{in} \in PolyObs(E_{\text{BV-BRST}})[ [\hbar, g ] ]$
in the given [[Hadamard vacuum state]] $\langle -\rangle \colon PolyObs(E_{\text{BV-BRST}})[ [\hbar, g] ] \to \mathcal{C}[ [\hbar,g] ]$.

If here $A_{in}$ and $A_{out}$ are monomials in [[Wick algebra]]-products of the [[field observables]] $\mathbf{\Phi}^a(x) \in Obs(E_{\text{BV-BRST}})[ [\hbar] ]$,
then this [[scattering amplitude]] comes from the [[integral kernel]]

$$
  \begin{aligned}
  &
  \left\langle
    \mathbf{\Phi}^{a_{out,1}}(x_{out,1}) \cdots \mathbf{\Phi}^{a_{out,s}}(x_{out,s})
    \vert
    \,
    \mathcal{S}(S_{int})
    \,
    \vert
    \mathbf{\Phi}^{a_{in,1}}(x_{in,1})
    \cdots
    \mathbf{\Phi}^{a_{in,r}}(x_{in,r})
  \right\rangle
  \\
  & \coloneqq
  \left\langle
     \left(\mathbf{\Phi}^{a_{out,1}}(x_{out,1})\right)^\ast
      \cdots
      \left(\mathbf{\Phi}^{a_{out,s}}(x_{out,s})\right)^\ast
    \;\mathcal{S}(S_{int})\;
      \mathbf{\Phi}^{a_{in,1}}(x_{in,1})
      \cdots
      \mathbf{\Phi}^{a_{in,r}}(x_{in,r})
  \right\rangle
  \end{aligned}
$$

or similarly, under [[Fourier transform of distributions]],

$$
  \label{ScatteringPlaneWaves}
  \begin{aligned}
  &
  \left\langle
    \widehat{\mathbf{\Phi}}^{a_{out,1}}(k_{out,1}) \cdots \widehat{\mathbf{\Phi}}^{a_{out,s}}(k_{out,s})
    \vert
    \,
    \mathcal{S}(S_{int})
    \,
    \vert
    \widehat{\mathbf{\Phi}}^{a_{in,1}}(k_{in,1})
    \cdots
    \widehat{\mathbf{\Phi}}^{a_{in,r}}(k_{in,r})
  \right\rangle
  \\
  & \coloneqq
  \left\langle
     \left(\widehat{\mathbf{\Phi}}^{a_{out,1}}(k_{out,1})\right)^\ast
      \cdots
      \left(\widehat{\mathbf{\Phi}}^{a_{out,s}}(k_{out,s})\right)^\ast
    \;\mathcal{S}(S_{int})\;
      \widehat{\mathbf{\Phi}}^{a_{in,1}}(k_{in,1})
      \cdots
      \widehat{\mathbf{\Phi}}^{a_{in,r}}(k_{in,r})
  \right\rangle
  \end{aligned}
  \,.
$$

These are interpreted as the (distributional) _[[probability amplitudes]]_ for [[plane waves]] of field species $a_{in,\cdot}$
with [[wave vector]] $k_{in,\cdot}$ to come in from the far past, ineract with each other via $S_{int}$,
and emerge in the far future as [[plane waves]] of field species $a_{out,\cdot}$ with [[wave vectors]] $k_{out,\cdot}$.

=--

Or rather:

+-- {: .num_remark #AdiabaticLimit}
###### Remark
**([[adiabatic limit]], [[infrared divergences]] and [[interacting vacuum]])**

Since a [[local observable]] $S_{int} \in LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]$  by definition
has compact spacetime support, the [[scattering amplitudes]] in remark \ref{FromAxiomaticSMatrixScatteringAmplitudes}
describe [[scattering]] processes for [[interactions]] that vanish (are "[[adiabatic switching|adiabatically switched off]]") outside a compact subset of [[spacetime]]. This constraint is crucial for [[causal perturbation theory]] to work.

There are several aspects to this:

* ([[adiabatic limit]]) On the one hand, real physical interactions $\mathbf{L}_{int}$ (say the [[electron-photon interaction]])
are not _really_ supposed to vanish outside a compact region of spacetime. In order to reflect this mathematically, one may consider a [[sequence]] of [[adiabatic switchings]] $g_{sw} \in C^\infty_{cp}(\Sigma)\langle g \rangle$ (each of [[compact support]]) whose [[limit of a sequence|limit]] is the [[constant function]] $g \in C^\infty(\Sigma)\langle g\rangle$ (the actual [[coupling constant]]), then consider the corresponding [[sequence]] of [[interaction]] [[action functionals]] $S_{int,sw} \coloneqq \tau_\Sigma( g_{sw} \mathbf{L}_{int} )$ and finally consider:


   1. as the true [[scattering amplitude]] the corresponding [[limit of a sequence|limit]]

      $$
        \left\langle
          A_{out} \vert \mathcal{S}(S_{int}) \vert A_{int}
        \right\rangle
        \;\coloneqq\;
        \underset{g_{sw} \to 1}{\lim}
        \left\langle
          A_{out} \vert \mathcal{S}(S_{int,sw}) \vert A_{int}
        \right\rangle
      $$

      of adiabatically switched [[scattering amplitudes]] (remark \ref{FromAxiomaticSMatrixScatteringAmplitudes}) --  if it exists. This is called the _[[strong adiabatic limit]]_.

  1. as the true [[n-point functions]] the corresponding [[limit of a sequence|limit]]

     $$
       \begin{aligned}
       &
       \left\langle
         \mathbf{\Phi}^{a_1}_{int}(x_1)
         \mathbf{\Phi}^{a_2}_{int}(x_2)
           \cdots
         \mathbf{\Phi}^{a_{n-1}}_{int}(x_{n-1})
         \mathbf{\Phi}^{a_n}_{int,sw}(x_n)
       \right\rangle
       \\
       & =
       \underset{\underset{g_{sw} \to 1}{\longrightarrow}}{\lim}
       \left\langle
         \mathbf{\Phi}^{a_1}_{int,sw}(x_1)
         \mathbf{\Phi}^{a_2}_{int,sw}(x_2)
           \cdots
         \mathbf{\Phi}^{a_{n-1}}_{int,sw}(x_{n-1})
         \mathbf{\Phi}^{a_n}_{int,sw}(x_n)
       \right\rangle
       \end{aligned}
     $$

     of [[tempered distribution|tempered distributional]] [[expectation values]] of products of [[interacting field algebra|interacting]] [[field observables]] (def. \ref{InteractingFieldObservables}) -- if it exists. (Similarly for [[time-ordered products]].)  This is called the _[[weak adiabatic limit]]_.

  Beware that the left hand sides here are symbolic: Even if the limit exists in [[expectation values]], in general there is no actual observable whose expectation value is that limit.

  The strong and weak adiabatic limits have been shown to exist if all [[field (physics)|fields]] are [[mass|massive]] ([Epstein-Glaser 73](#EpsteinGlaser73)). The weak adiabatic limit has been shown to exists for [[quantum electrodynamics]] and for [[mass]]-less [[phi^4 theory]] ([Blanchard-Seneor 75](adiabatic+switching#BlanchardSeneor75)) and for larger classes of field theories in ([Duch 17, p. 113, 114](adiabatic+switching#Duch17)).

  If these limits do not exist, one says that the [[perturbative QFT]] has an _[[infrared divergence]]_. 
  
* ([[algebraic adiabatic limit]]) On the other hand, it is equally unrealistic that an actual [[experiment]] _detects_ phenomena outside a given compact subset of spacetime. Realistic scattering [[experiments]] (such as the [[LHC]]) do not really prepare or measure [[plane waves]] filling all of [[spacetime]] as described by the [[scattering amplitudes]] (eq:ScatteringPlaneWaves). Any [[observable]] that is realistically measurable must have compact spacetime support. We see below in prop. \ref{WellDefinedInteractingFieldAlgebra} that such [[interacting field observables]] with compact spacetime support may be computed without taking the [[adiabatic limit]]: It is sufficient to use any [[adiabatic switching]] which is constant on the support of the observable.

  This way one obtains for each [[causally closed subset]] $\mathcal{O}$ of spacetime an  algebra of observables $\mathcal{A}_{int}(\mathcal{O})$ whose support is in $\mathcal{O}$, and for each inclusion of subsets a corresponding inclusion of algebras of observables (prop. \ref{PerturbativeQuantumObservablesIsLocalnet} below). Of this system of observables one may form the [[category theory|category-theoretic]] [[inductive limit]] to obtain a single global algebra of observables.

  $$
    \mathcal{A}_{int}
      \;\coloneqq\;
    \underset{\underset{\mathcal{O}}{\longrightarrow}}{\lim}
      \mathcal{A}_{int}(\mathcal{O})
  $$

  This always exists. It is called the _[[algebraic adiabatic limit]]_ (going back to [Brunetti-Fredenhagen 00, section 8](perturbative+algebraic+quantum+field+theory#BrunettiFredenhagen00)).

  For [[quantum electrodynamics]] the [[algebraic adiabatic limit]] was worked out in ([Dütsch-Fredenhagen 98](quantum+electrodynamics#DuetschFredenhagen98), reviewed in [Dütsch 18, 5,3](QED+Duetsch18)).

* ([[interacting vacuum]]) While, via the above [[algebraic adiabatic limit]], [[causal perturbation theory]] yields the correct [[interacting field algebra of quantum observables]] independent of choices of [[adiabatic switching]], a theory of _[[quantum probability]]_ requires, on top of the [[algebra of observables]], also a _[[state on a star-algebra|state]]_

  $$
    \langle - \rangle_{int} \;\colon\; \mathcal{A}_{int} \longrightarrow \mathbb{C}[ [\hbar] ]
  $$

  Just as the [[interacting field algebra of observables]] $\mathcal{A}_{int}$ is a [[deformation]] of the free field algebra of observables ([[Wick algebra]]), there ought to be a corresponding deformation of the free [[Hadamard vacuum state]] $\langle- \rangle$ into an "[[interacting vacuum state]]" $\langle - \rangle_{int}$.

  Sometimes the [[weak adiabatic limit]] serves to define the [[interacting vacuum]] (see [Duch 17, p. 113-114](adiabatic+switching#Duch17)).

A stark example of these infrared issues is the phenomenon of _[[confinement]]_ of [[quarks]] to [[hadron]] [[bound states]] (notably to [[protons]] and [[neutrons]]) at large [[wavelengths]]. This is paramount in [[experiment|observation]] and reproduced in numerical [[lattice gauge theory]] simulation, but is invisible to [[perturbative QFT|perturbative]] [[quantum chromodynamics]] in its [[free field]] [[vacuum state]], due to [[infrared divergences]].
It is expected that this should be rectified by the proper [[interacting vacuum]] of [[QCD]] ([Rafelski 90, pages 12-16](confinement#Rafelski90)), which is possibly a "[[theta-vacuum]]" exhibiting [[superposition]] of [[instanton in QCD|QCD instantons]] ([Schäfer-Shuryak 98, section III.D](instanton+in+QCD#SchaeferShuryak98)). This remains open, closely related to the _[Millenium Problem](http://www.claymath.org/millennium-problems/yang%E2%80%93mills-and-mass-gap)_ of [[quantization of Yang-Mills theory]].

=--

In contrast to the above subtleties about the [[infrared divergences]], any would-be [[UV-divergences]] in [[perturbative QFT]] are 
dealt with by [[causal perturbation theory]]:


+-- {: .num_remark #TheTraditionalErrorThatLeadsToTheNotoriouDivergencies}
###### Remark
**(the traditional error leading to [[UV-divergences]])**

Naively it might seem that (say over [[Minkowski spacetime]], for simplicity) 
examples of [[time-ordered products]] according to def. \ref{TimeOrderedProduct}
might simply be obtained by multiplying [[Wick algebra]]-products with [[step functions]] $\Theta$ of the time coordinates, hence to write, in the notation as [[generalized functions]] (remark \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}):

$$
  T(x_1, x_2)
  \overset{\text{no!}}{=}
  \Theta(x_1^0 - x_2^0) \, T(x_1) \, T(x_2)
  +
  \Theta(x_2^0 - x_1^0) \, T(x_2) \, T(x_1)
$$

and analogously for time-ordered products of more arguments (for instance [Weinberg 95, p. 143, between (3.5.9) and (3.5.10)](#Weinberg95)).

This however is simply a mathematical error (as amplified in [Scharf 95, below (3.2.4), below (3.2.44) and in fig. 3](causal+perturbation+theory#Scharf95)): 

Both $T$ as well as $\Theta$ are [[distributions]] and their [[product of distributions]] is in general not defined ([[Hörmander's criterion]] may be violated). The notorious [[ultraviolet divergences]] which plagued ([Feynman 85](Schwinger-Tomonaga-Feynman-Dyson#Feynman85SuchABunchOfWords)) the original conception of [[perturbative QFT]] due to [[Schwinger-Tomonaga-Feynman-Dyson]] are the signature of this ill-defined product (see remark \ref{CausalPerturbationTheoryAbsenceOfUVDivergences}).

On the other hand, when both distributions are [[restriction of distributions|restricted]] to the [[complement]] of the [[diagonal]]
(i.e. restricted away from coinciding points $x_1 = x_2$), then the [[step function]] becomes a [[non-singular distribution]]
so that the above expression happens to be well defined and does solve the axioms for time-ordered products.

Hence what needs to be done to properly define the [[time-ordered product]] is to choose an [[extension of distributions]] of the above product expression back from the complement of the diagonal to the whole space of [[tuples]] of points. Any such extension will produce time-ordered products.

There are in general several different such [[extension of distributions|extensions]]. This freedom of choice is the freedom
of _[[renormalization|"re-"normalization]]_; or equivalently, by the [[main theorem of perturbative renormalization theory]] (theorem \ref{PerturbativeRenormalizationMainTheorem}),
this is the freedom of choosing "counter terms" for the [[local observable|local]] [[interactions]]. This we discuss below in
_[Feynman diagrams and (re-)normalization](#ExistenceAndRenormalization)_.


=--


+-- {: .num_remark #CausalPerturbationTheoryAbsenceOfUVDivergences}
###### Remark
**(absence of [[ultraviolet divergences]] and [[renormalization|re-normalization]])**

The simple axioms of [[causal perturbation theory]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering})
do fully capture [[perturbative quantum field theory]] "in the ultraviolet": A solution to these axioms
induces, by definition, well-defined [[perturbative QFT|perturbative]] [[scattering amplitudes]] (remark \ref{FromAxiomaticSMatrixScatteringAmplitudes})
and well-defined [[perturbative QFT|perturbative]] [[probability amplitudes]] of [[interacting field observables]] (def. \ref{InteractingFieldObservables}) induced by _[[local observables|local]]_ [[action functionals]] (describing point-interactions such as the [[electron-photon interaction]]). By the [[main theorem of perturbative renormalization]] (theorem \ref{PerturbativeRenormalizationMainTheorem}) such solutions exist. This means that, while these are necessarily [[formal power series]] in $\hbar$ and $g$ (remark \ref{AsymptoticSeriesObservables}), all the [[coefficients]] of these formal power series ("[[loop order]] contributions") are well defined.

This is in contrast to the original informal conception of [[perturbative QFT]] due to [[Schwinger-Tomonaga-Feynman-Dyson]],
which in a first stage produced ill-defined [[divergence|diverging]] expressions for the [[coefficients]] (due to the mathematical error discussed in remark \ref{TheTraditionalErrorThatLeadsToTheNotoriouDivergencies} below), which were then "[[renormalization|re-normalized]]" to finite values, by further informal arguments.

Here in [[causal perturbation theory]] no [[divergences]] in the [[coefficients]] of the [[formal power series]] are considered in the first place, all coefficients are well-defined, hence "finite". In this sense [[causal perturbation theory]] is about "finite" perturbative QFT, where instead of "re-normalization" of ill-defined expressions one just encounters "normalization" (prominently highlighted in [Scharf 95, see title, introduction, and section 4.3](causal+perturbation+theory#Scharf95)), namely compatible choices of these finite values, parameterized by the [[Stückelberg-pPetermann renormalization group]].

This refers to those [[divergences]] that are known as _[[UV-divergences]]_, namely short-distance effects,
which are mathematically reflected in the fact that the perturbative [[S-matrix]] scheme (def. \ref{LagrangianFieldTheoryPerturbativeScattering})
is defined on _[[local observables]]_, which, by their very locality, encode point-[[interactions]].
See also remark \ref{AdiabaticLimit} on _[[infrared divergences]]_.

=--

+-- {: .num_remark #calSFunctionIsRenormalizationScheme}
###### Remark
**([[renormalization scheme]])**

Beware the terminology in def. \ref{LagrangianFieldTheoryPerturbativeScattering}: A _single_ S-matrix is one single observable

$$
  \mathcal{S}(S_{int})
  \;\in\;
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [g,j] ]
$$

for a fixed ([[adiabatic switching|adiabatically switched]] [[local observable|local]]) [[interaction]] $S_{int}$, reflecting the [[scattering amplitudes]] (remark \ref{FromAxiomaticSMatrixScatteringAmplitudes}) with respect to that particular interaction.  Hence the function

$$
  \mathcal{S}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [\hbar, g,j] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})((\hbar))[ [g,j] ]
$$

axiomatized in def. \ref{LagrangianFieldTheoryPerturbativeScattering} is really a whole _scheme_ for constructing compatible S-matrices for _all_ possible (adiabatically switched, local) interactions at once.

Since the usual proof of the construction of such schemes of S-matrices involves _[[renormalization|("re"-)normalization]]_, the function $\mathcal{S}$ axiomatized by def. \ref{LagrangianFieldTheoryPerturbativeScattering} may also be referred to as a _[[renormalization scheme|("re"-)normalization scheme]]_.

This perspective on $\mathcal{S}$ as a [[renormalization scheme]] is amplified by the [[main theorem of perturbative renormalization]] (theorem \ref{PerturbativeRenormalizationMainTheorem})
wich states that the space of choices for $\mathcal{S}$ is a [[torsor]] over the [[Stückelberg-Petermann renormalization group]].

=--


+-- {: .num_remark}
###### Remark
**([[quantum anomalies]])**

The [[axioms]] for the [[S-matrix]] in def. \ref{LagrangianFieldTheoryPerturbativeScattering}
(and similarly that for the [[time-ordered products]] below in def. \ref{TimeOrderedProduct})
are sufficient to imply a [[causally local net]] of perturbative [[interacting field algebras of quantum observables]] (prop. \ref{PerturbativeQuantumObservablesIsLocalnet} below), and thus its [[algebraic adiabatic limit]] (remark \ref{AdiabaticLimit}).

It does not guarantee, however, that the [[BV-BRST differential]] passes to those
[[algebras of quantum observables]], hence it does not guarantee that the [[infinitesimal symmetries of the Lagrangian]]
are respected by the [[quantization]] process (there may be "[[quantum anomalies]]").
The extra condition that does ensure this is the _[[quantum master Ward identity]]_ or _[[quantum master equation]]_.
This we discuss elsewhere.

Apart from [[gauge symmetries]] one also wants to require that rigid symmetries  are preserved by the S-matrix, notably [[Poincare group]]-symmetry for scattering on [[Minkowski spacetime]]. This extra axiom is needed to imply the _[[main theorem of perturbative renormalization]]_ (theorem \ref{PerturbativeRenormalizationMainTheorem}).

=--






$\,$



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


Namely a key consequence of the "[[causal additivity]]" axiom on the S-matrix in def. \ref{LagrangianFieldTheoryPerturbativeScattering}
turns out to be that the perturbative [[quantum observables on interacting fields]] with compact spacetime support (def. \ref{GeneratingFunctionsForCorrelationFunctions})

1. depend on the [[adiabatic switching]] $g_{sw}$ of the [[interaction]] [[Lagrangian density]]
only up to _canonical_ unitary [[isomorphism]] (lemma \ref{CausalLocalityOfThePerturbativeSMatrix} below)

1. form a [[causal locality|causally]] [[local net of observables]] in the sense of the [[Haag-Kastler axioms]] as the spacetime localization varies (prop. \ref{PerturbativeQuantumObservablesIsLocalnet} below).

To the extent that a [[local net of observables]] may be regarded as _defining_ a [[quantum field theory]],
which is the claim of ([[perturbative AQFT|perturbative]]) [[AQFT]],
this proves that the perturbative S-matrices in [[causal perturbation theory]] as in def. \ref{LagrangianFieldTheoryPerturbativeScattering}
indeed make sense, despite the involvement of [[adiabatic switching]] of the [[interaction]] [[Lagrangian density]]
which does not make physical sense when interpreted naively: In reality the interaction is of course not (for realistic [[theory (physics)|theories]] at least) "switched off" outside some bounded region of spacetime; but the result here shows that if we pretend that it does
then first of all we get consistent mathematical formulas and moreover we can then nevertheless compute the correct [[quantum observables]] that are localized in this spacetime region. But the [[local net of observables]] as the spacetime localization varies
is supposed to encode the full quantum field theory. Certainly any given [[experiment]] in practice probes a bounded spacetime
region, and hence the algebra of observables localized in this region is sufficient to compare the theory to experiment.


$\,$



The power series coefficients of the [[quantum observables on interacting fields]]
are also called the _[[retarded products]]_. For the time being we mention these here
just for completeness:

+-- {: .num_defn #RetardedProductFromPerturbativeSMatrix}
###### Definition
**([[retarded products]] from [[S-matrix]])**

It follows from the perturbation axiom in def. \ref{LagrangianFieldTheoryPerturbativeScattering} that there is a system of [[continuous linear functionals]]

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

Let $S$ be a perturbative S-matrix according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}
with $Z$ the generating functional (eq:GeneratingFunctionInducedFromSMatrix) it induces

1. The following conditions are equivalent for all $L, J_1, J_2 \in \mathcal{F}_{loc}$:

   1. $Z_L(J_1 + J_2) = Z_L(J_1) Z_L(J_2)$

   1. $Z_{L + J_1}(J_2) = Z_L(J_2)$

   1. $S(L + J_1 + J_2) = S(L + J_1) \, S(L)^{-1} \, S(L + J_2)$

   Hence causal additivity in def. \ref{LagrangianFieldTheoryPerturbativeScattering}
implies that all these conditions hold if $supp(J_1) {\vee\!\!\!\wedge} supp(J_2)$.


1. If $supp(J_1)$ is [[spacelike]] separted from $supp(J_1)$, hence if the [[causal ordering]] is
   $supp(J_1) {\vee\!\!\!\wedge} supp(J_2)$ and $supp(J_2) {\vee\!\!\!\wedge} supp(J_1)$ then

   $$
     Z_{L_{int}}(J_1) Z_{L_{int}}(J_2) = Z_{L_{int}}(J_2) J_{L_{int}}(J_1)
     \,.
   $$


   Similarly, if $supp(L_1) {\vee\!\!\!\wedge} supp(L_2)$ and $supp(L_2) {\vee\!\!\!\wedge} supp(L_1)$ then

   $$
     S(L_1) \, S(L_2) = S(L_2) \, S(L_1)
     \,.
   $$



1. {#ChangeOfAdiabaticSwitchingAlgebraIso} If $L_1\vert_{O} = L_2\vert_{O}$ on a [[causally closed subset]] $O \subset \mathbb{R}^{d-1,1}$ then there exists an invertible $K \in \mathcal{W}[ [ g/\hbar] ]$ such that for all $J$ with $supp(J) \subset O$ it relates $Z_{L_1}(J)$ to $Z_{L_2}(J)$ by [[conjugation]]:

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
    supp(L_1) {\vee\!\!\!\wedge} supp(L_2)
  \right)
   \;\Rightarrow\;
  S(L_1 + L_2)
  =
  S(L_1)S(L_2)
  \,.
$$

Hence if $supp(L_1) {\vee\!\!\!\wedge} supp(L_2)$ and $supp(L_2) {\vee\!\!\!\wedge} supp(L_1)$ then

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

such that their [[causal order]] ([this def.](A+first+idea+of+quantum+field+theory#CausalOrdering)) is

$$
  supp(a) {\vee\!\!\!\wedge} supp(J) {\vee\!\!\!\wedge} supp(r)
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

We now use lemma \ref{CausalLocalityOfThePerturbativeSMatrix} to neatly organize the
system of localized [[quantum observables on interacting fields]]:

+-- {: .num_defn #PerturbativeGeneratingLocalNetOfObservables}
###### Definition
**(system of perturbative generating [[algebras of observables]])

Let $S$ be a perturbative S-matrix according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}
and let $L_{int} \in \Omega^{d,0}(E)$ be an [[interaction]] [[Lagrangian density]].


For $\mathcal{O} \subset \Sigma$ a [[causally closed subset]] of [[spacetime]]
([this def. ](A+first+idea+of+quantum+field+theory#CausalComplementOfSubsetOfLorentzianManifold))
and for $g_{sw} \in Cutoffs(\mathcal{O})$ an [[adiabatic switching]] function ([this def.](A+first+idea+of+quantum+field+theory#CutoffFunctions))
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

+-- {: .num_prop #WellDefinedInteractingFieldAlgebra}
###### Propsition
**([[interacting field algebra of observables]] well defined up to canonical [[isomorphism]])**

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

Given a perturbative S-matrix according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}
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
   which are [[spacelike]] separated, in that their [[causal ordering]] ([this def.](A+first+idea+of+quantum+field+theory#CausalOrdering)) satisfies

   $$
     \mathcal{O}_1 {\vee\!\!\!\wedge} \mathcal{O}_2
       \;\text{and}\;
     \mathcal{O}_2 {\vee\!\!\!\wedge} \mathcal{O}_1
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

Let $S$ be a perturbative S-matrix according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}
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
**(system of [[interacting field algebras of observables]] is [[local net of observables]])**


Given a perturbative S-matrix according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}
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
   which are [[spacelike]] separated, in that their [[causal ordering]] ([this def.](A+first+idea+of+quantum+field+theory#CausalOrdering)) satisfies

   $$
     \mathcal{O}_1 {\vee\!\!\!\wedge} \mathcal{O}_2
       \;\text{and}\;
     \mathcal{O}_2 {\vee\!\!\!\wedge} \mathcal{O}_1
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

for $supp(J_1) {\vee\!\!\!\wedge} supp(J_2)$ and $supp(J_2) {\vee\!\!\!\wedge} supp(J_1)$.

=--

$\,$





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


In the 1960s there was a prominent proposal, around [[Geoffrey Chew]], that ([[perturbative quantum field theory|perturbative]]) [[quantum field theory]] should be _defined_ by [[axiom|axiomatizing]] properties of the S-matrix _without_ explicit reference to [[field (physics)|fields]] on [[spacetime]].

Here _analycity_ (or more general the _crossing property_) of the S-matrix reflects its [[causal factorization]], and hence this is often referred to as the _analytic S-matrix_ (see [Eden-Ladshoff-Olive-Polkinhorne 66](#EdenLadshoffOlivePolkinhorne66)).

This is a radical perspective where no [[spacetime]] geometry and physical fields are made explicit, but where the entire physics is encoded by what quantum particles see that scatter through it.

Historically, this S-matrix "bootstrap" approach fell out of fashion with the success of the [[quark]] model in  [[quantum chromodynamics]], which is a [[local field theory|local]] [[Lagrangian field theory]] ([[Yang-Mills theory]]) defined in terms of [[field (physics)|fields]] on [[spacetime]].

See also the discussion in ([Chew 70](#Chew70), [Schroer 11](#Schroer11)).

But later [[perturbative string theory]] revived the axiomatic S-matrix perspective. In general, perturbative string theory is not defined by a geometric spacetime background. Instead the background is algebraically encoded by a [[2d SCFT]] ("[[2-spectral triple]]") and the [[string perturbation series]] is a formula that translates this into an S-matrix. Spacetime physics then is whatever is seen by string scattering processes (see also at _[string theory FAQ -- What are the equations of string theory?](string%20theory%20FAQ#WhatAreTheEquations)_).

More recently, the S-matrix perspective becomes fashionable also in [[Yang-Mills theory]], at least in [[super Yang-Mills theory]]: one observes that the theory enjoys good structures in its scattering amplitudes which are
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

This proposal was vocally promoted as the "bootstrap program" by [[Geoffrey Chew]] and [[Stanley Mandelstam]] (see [Chew 70](#Chew70)).

Textbooks account of this axiomatic approach to defining the S-matrix (i.e. not proceeding via [[Lagrangian field theory]] but via analyticity axioms) is

* {#EdenLadshoffOlivePolkinhorne66} Eden, Landshoff, [[David Olive]], [[John Polkinghorne]], _The Analytic S-matrix_, Cambridge 1966 ([pdf](http://assets.cambridge.org/97805210/48699/sample/9780521048699ws.pdf))

* {#Gribov69} [[Vladimir Gribov]], _The theory of complex angular momenta_, Lecture St. Petersburg 1996, publsihed.  Cambridge 2003 ([doi:10.1017/CBO9780511534959](https://doi.org/10.1017/CBO9780511534959))

Discussion of S-matrix analyticity as a constraint on global causality violation of locally Lorentz invariant theories is in

* {#AAHDNR06} Allan Adams, [[Nima Arkani-Hamed]], Sergei Dubovsky, Alberto Nicolis, Riccardo Rattazzi, _Causality, Analyticity and an IR Obstruction to UV Completion_, JHEP 0610:014, 2006 ([arXiv:hep-th/0602178](https://arxiv.org/abs/hep-th/0602178))

General discussion of scattering theory is in

* {#Newton82} Roger G. Newton, _Scattering Theory of Waves and Particles_, Springer 1982 ([TOC pdf](https://cds.cern.ch/record/1562608/files/0486425355_TOC.pdf))

* {#Iagolnitzer07} Daniel Iagolnitzer, _The Analyticity Program in Axiomatic Quantum Field Theory_, in  A.B. de Monvel, [[Detlev Buchholz]], Daniel Iagolnitzer, Moschella U. (eds.) _Rigorous Quantum Field Theory_, Progress in Mathematics, vol 251. Birkhäuser, Basel, 2007, ([web](https://link.springer.com/chapter/10.1007/978-3-7643-7434-1_11))

* {#Iagolnitzer14} Daniel Iagolnitzer, _Scattering in Quantum Field Theories, The Axiomatic and Constructive Approaches_, Princeton 2014 ([web](https://press.princeton.edu/titles/5157.html))

A textbook account of the traditional heuristic picture deriving the S-matrix in [[perturbative quantum field theory|perturbative]] [[Lagrangian field theory]] is in

* {#Weinberg95} [[Steven Weinberg]], chapter 3 of _The quantum theory of fields - Volume I: Foundations_, Cambridge 1995

The mathematically rigorous construction of the S-matrix in [[perturbative quantum field theory|perturbative]] [[Lagrangian field theory]] via _[[causal perturbation theory]]_ is due to

* {#EpsteinGlaser73} [[Henri Epstein]], [[Vladimir Glaser]], _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211 ([Numdam](http://www.numdam.org/item?id=AIHPA_1973__19_3_211_0 ))

based on ideas due to ([Stückelberg 49](causal+perturbation+theory#Stueckelberg49), [Stückelberg 51](causal+perturbation+theory#Stueckelberg49)) and

* {#BogoliubovShirkov59} [[Nikolay Bogoliubov]], [[Dmitry Shirkov]], _Introduction to the Theory of Quantized Fields_, New York (1959)

Comparative discussion of the two perspectives on the S-matrix includes:

* {#Chew70} [[Geoffrey Chew]], _Quark or Bootstrap: Triumph or Frustration for Hadron Physics_, Physics Today, May 1970 ([web](https://pubarchive.lbl.gov/islandora/object/ir%3A144169/datastream/PDF/view))

* {#Schroer11} [[Bert Schroer]], _Causality and dispersion relations and the role of the S-matrix in the ongoing research_ ([arXiv:1102.0168](https://arxiv.org/abs/1102.0168))


Brief introduction to the S-matrix in quantum mechanics and its rigorous construction in field theory via [[causal perturbation theory]] is in

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

* {#Duetsch18} [[Michael Dütsch]], _[[From classical field theory to perturbative quantum field theory]]_, 2018


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

* Wikipedia, _[Bootstrap model](https://en.wikipedia.org/wiki/Bootstrap_model)_

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
