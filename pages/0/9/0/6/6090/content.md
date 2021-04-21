
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
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

In [[quantum field theory]] a _[[scattering amplitude]]_ or _scattering matrix_, usually just _S-matrix_ for short, encodes the [[probability amplitudes]] for scattering processes of [[particles]] off each other.

### General idea

Every [[Lagrangian field theory|Lagrangian]] [[perturbative quantum field theory]] has an S-matrix associated with it (after [[renormalization]]), usually thought of as a [[perturbation series]] over [[Feynman diagrams]] extracted from the [[Lagrangian density]]. The rigorous construction of this as an [[operator-valued distribution]] is the content of _[[causal perturbation theory]]_ ([Epstein-Glaser 73](#EpsteinGlaser73)).

But there are also S-matrices not fundamentally arising from a [[local field theory]], notably the [[string scattering amplitudes]].

There have been attempts to _define_ [[perturbative quantum field theory]] by directly [[axiom|axiomatizing]] properties of the S-matrix, without requiring concepts of [[field (physics)|fields]] in [[spacetime]]. This perspective goes back to ([Heisenberg 43](#Heisenberg43)) and was vocally promoted in [[Geoffrey Chew]]'s "bootstrap program" (a textbook account is in [Eden-Ladshoff-Olive-Polkinhorne 66](#EdenLadshoffOlivePolkinhorne66)).

In the [[field theory]]-picture the crucial condition on the S-matrix is its [[causal additivity]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering} below) which reflects the [[microcausality]] of [[quantum observables]] (prop. \ref{PerturbativeQuantumObservablesIsLocalnet} below), whence the name "[[causal perturbation theory]]".

{#TheAnalyticSMatrix} This [[causality]] of the S-matrix, when understood in terms of underlying [[spacetime]] and [[field (physics)|fields]], is supposed to be detected more abstractly by the S-matrix being a suitable [[analytic function]] of the [[wave vectors]] of the scattering asymptotic states ([Newton 82, 10.3.3](#Newton82), [Arkani-Hamed et al. 06](#AAHDNR06)), often referred to via "dispersion relations" (e.g. [Eden-Ladshoff-Olive-Polkinhorne 66 (1.1.1)-(1.1.5)](#EdenLadshoffOlivePolkinhorne66), [Gribov 69, 1.1.2](#Gribov69)). Since thereby analyticity is recognized as the crucial property of the S-matrix in the spacetime/field-independent axiomatization, this is often referred to as "the analytic S-matrix" (e.g. [Eden-Ladshoff-Olive-Polkinhorne 66](#EdenLadshoffOlivePolkinhorne66)). More specifically [[microcausality]] is what induces "crossing symmetry" of the S-matrix ([Weinberg 95, section 10.8](#Weinberg95)).

The perception of the nature of the S-matrix as a primary or derived concept in the foundations of quantum field theory has a convoluted (and ongoing) history, see [below](#History).

### The S-matrix bootstrap
  {#IdeaSMatrixBootstrap}

From [this Physics.SE comment](https://physics.stackexchange.com/a/17973/5603) by [[Ron Maimon]]:

The idea of the S-matrix "bootstrap" is that one may compute the S-matrix directly from suitable axioms without using a [[local field theory|local]] [[quantum field theory]] involving [[field (physics)|fields]] on [[spacetime]]. In order for the theory to be interesting, the S-matrix should obey certain properties abstracted away from field theory

* It should be unitary
* It should be Lorentz invariant
* It should be crossing invariant: this means that the antiparticle scattering
should be described by the analytic continuation of the particle scattering
* It should obey the Landau property--- that all singularities of scattering are poles and cuts corresponding to exchange of collections of real particles on shell.
* It should obey ([[Stanley Mandelstam|Mandelstam]]) analyticity: the amplitude should be writable as an integral over the imaginary part of the cut discontinuity from production of physical particles. Further, this cut discontinuity itself can be expanded in terms of another cut discontinuity (these are the mysterious then and still mysterious now double dispersion relations of Mandelstam).

This is a sketchy summary, because each of these conditions is involved. The unitarity condition in particular, is very difficult, because it is so nonlinear. The only practical way to solve it is in a perturbation series which starts with weakly interacting nearly stable particles (described by poles of the S-matrix) which exchange each other (the exchange picture is required by crossing, and the form of the scattering is fixed by the Landau and Mandelstam analyticity, once you know the spectrum).

The "Bootstrap property" is then the following heuristic idea, which is included in the above formal relations:

* The particles and interactions which emerge as the spectrum of the S-matrix from the scattering of states, including their binding together into bound states, should be the same spectrum of particles that come in ias in-states.

This is a heuristic idea, because it is only saying that the S-matrix is consistent, and the formal consistency relations are those above. But the bootstrap was a slogan that implied that all the consistency conditions were not yet discovered, and there might be more.

This idea was very inspirational to many great people in the 1960s, because it was an approach to strong interactions that could accommodate non-field theories of infinitely many particle types of high spin, without postulating constituent particles (like quarks and gluons).

### Regge theory

Continuing with [this Physics.SE comment](https://physics.stackexchange.com/a/17973/5603) by [[Ron Maimon]]:


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

We first discuss the simple situation of S-matrices in [[quantum mechanics]]:

* _[In Quantum Mechanics](#InQuantumMechanics)_

Then we give a detailed account of S-matrix theory for [[perturbative quantum field theory]] induced from [[interaction]] [[action functionals]] on [[spacetime]]: 

* _[In perturbative relativistic Lagrangian QFT – Causal perturbation theory](#InCausalPerturbationTheory)_.

This is essentially chapter 15. in _[[A first idea of quantum field theory]]_.

(We should eventually also discuss the abstract S-matrix bootstrap here in detail.)

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
    & =
        \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right)
        \exp\left({\tfrac{t}{i \hbar} H_{free} + \tfrac{t}{i \hbar} V} \right)
        \vert \psi \rangle
    \end{aligned}
  \,.
\]

This is called the solution of the Schr&#246;dinger equation "in the [[interaction picture]]", whence the subscript. Its definition may be read as the result of propagating the actual solution $\vert \psi(-)\rangle_S$ at time $t$ back to time $t = 0$, but using just the free Hamiltonian, hence with "the interaction switched off".

Notice that if the operator $V$ were to commute with $H_{free}$ (which it does not in all relevant examples) then we would simply have $\vert \psi(t)\rangle_I = \exp( \tfrac{t}{i \hbar } V ) \vert \psi\rangle$, hence then the solution (eq:StateInTheInteractionPicture) in the [[interaction picture]] would be the result of "propagating" the initial conditions using _only_ the interaction. Now since $V$ may not be assumed to commute with $H_{free}$, the actual form of $\vert \psi(-) \rangle_{I}$ is more complicated. But _infinitesimally_ it remains true that $\vert \psi(-)\rangle_I$ is propagated this way, not by the plain operator $V$, though, but by $V$ viewed in the [[Heisenberg picture]] of the free theory. This is the content of the differential equation (eq:DifferentialEquationInInteractionPicture) below.

But first notice that this will indeed be useful: If an explicit expression for the "state in the [[interaction picture]]" (eq:StateInTheInteractionPicture) is known, then the assumption that also the operator $\exp\left({\tfrac{t}{i \hbar} H_{free}}\right)$ is sufficiently well understood implies that the actual solution

$$
  \vert \psi(t) \rangle_S
  \;=\;
  \exp\left({\tfrac{t}{i \hbar} H_{free}}\right) \vert \psi(t) \rangle_I
$$

is under control. Hence the question now is how to find $\vert \psi(-)\rangle_I$ given its value at some time $t$. (It is conventional to consider this for $t \to \pm \infty$, see (eq:SMatrixInQuantumMechanics) below.)

Now observe that $\vert \psi(-)\rangle_i$ satisfies the following [[differential equation]] ("[[Schrödinger equation]] in [[interaction picture]]"):

\[
  \label{DifferentialEquationInInteractionPicture}
  \frac{d}{d t} \vert \psi(t) \rangle_I
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

is known as the [[interaction]] term $V$ "viewed in the [[interaction picture]]".

Here is the derivation of (eq:DifferentialEquationInInteractionPicture), where we use the [[product law]] for [[differentiation]]:

$$
  \begin{aligned}
    \frac{d}{d t}
    \vert \psi(r) \rangle_I
    & =
    \frac{d}{d t}
    \left(
      \exp\left( \tfrac{- t}{i \hbar} H_{free}\right)
      \exp\left({\tfrac{t}{i \hbar} H_{free} + \tfrac{t}{i \hbar} V} \right)
    \right)
    \vert \psi \rangle
    \\
    & =
    \left(
      \left(
        \frac{d}{d t}
        \exp\left( \tfrac{- t}{i \hbar} H_{free} \right)
      \right)
      \exp\left({\tfrac{t}{i \hbar} H_{free} + \tfrac{t}{i \hbar} V} \right)
      +
      \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right)
      \left(
        \frac{d}{d t}
        \exp\left({\tfrac{t}{i \hbar} H_{free} + \tfrac{t}{i \hbar} V} \right)
      \right)
    \right)
    \vert \psi \rangle
    \\
    & =
    \left(
      \exp\left( \tfrac{- t}{i \hbar} H_{free} \right)
      \left( \tfrac{- 1}{i \hbar} H_{free} \right)
      \exp\left( \tfrac{t}{i \hbar} H_{free} + \tfrac{t}{i \hbar} V  \right)
      +
      \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right)
      \left( \tfrac{1}{i \hbar} H_{free} + \tfrac{1}{i \hbar} V \right)
      \exp\left( \tfrac{t}{i \hbar} H_{free} + \tfrac{t}{i \hbar} V \right)
    \right)
    \vert \psi \rangle
    \\
    & =
      \tfrac{1}{i \hbar}
      \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right)
      V
      \exp\left( \tfrac{t}{i \hbar} H_{free} + \tfrac{t}{i \hbar} V \right)
    \vert \psi \rangle
    \\
    & =
      \tfrac{1}{i \hbar}
      \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right)
      V
      \exp\left({\tfrac{+ t}{i \hbar} H_{free}}\right)
      \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right)
      \exp\left( \tfrac{t}{i \hbar} H_{free} + \tfrac{t}{i \hbar} V \right)
    \vert \psi \rangle
    \\
    & =
      \tfrac{1}{i \hbar}
      \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right)
      V
      \exp\left({\tfrac{+ t}{i \hbar} H_{free}}\right)
      \vert \psi(t) \rangle_I
    \\
    & =
      \tfrac{1}{i \hbar}
      V_I(t)
      \vert \psi(t) \rangle_I
  \end{aligned}
$$


Now in fact $V_I$ is just $V$ "viewed in the [[Heisenberg picture]]", but for the _free_ theory. By our running assumption that the free theory is well understood, also $V_I(t)$ is well understood, and hence all that remains now is to find a sufficiently concrete solution to equation (eq:DifferentialEquationInInteractionPicture). This is the heart of working in the interaction picture.

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


In [[perturbative algebraic quantum field theory]] the broad structure of the [[interaction picture]] in [[quantum mechanics]] ([above](#InQuantumMechanics)) remains a very good guide, but various technical details have to be generalized with due care:

1. The algebra of operators in the [[Heisenberg picture]] of the free theory becomes the _[[Wick algebra]]_ of the [[free field theory]] (taking into account "normal ordering" of field operators) defined on _[[microcausal functionals]]_ built from [[operator-valued distributions]] with constraints on their [[wave front set]].

1. The [[time-ordered products]] in the [[Dyson formula]] have to be refined to [[causal locality|causally ordered]] products and the resulting product at coincident points has to be defined by [[point-extension of distributions]] -- the freedom in making this choice is the [[renormalization]] freedom ("conter-terms").

1. The sharp interaction cutoff in the [[Dyson formula]] that is hidden in the integration over $[t_0,t]$ has to be smoothed out by [[adiabatic switching]] of the interaction (making the whole S-matrix an [[operator-valued distribution]]).

Together these three points are taken care of by the axiomatization of the "[[adiabatic switching|adiabatically switched]] [[S-matrix]]" according to **[[causal perturbation theory]]** (def. \ref{LagrangianFieldTheoryPerturbativeScattering} below)



$\,$

#### Free field vacua
 {#FreeFieldVacua}


In considering [[perturbative QFT]], we are considering [[perturbation theory]] in formal [[deformation]] parameters around a fixed [[free field theory|free]]
[[Lagrangian field theory|Lagrangian]] [[quantum field theory]] in a chosen [[Hadamard vacuum state]].

For convenient referencing we collect all the structure and notation that goes into this in the following definitions:

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

for the corresponding [[Wick algebra]]-[[structure]] on [[formal power series]] in $\hbar$ ([[Planck's constant]]) of [[microcausal polynomial observables]]. This is a [[star algebra]] with respect to ([[coefficient]]-wise) [[complex conjugation]].

Write

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

for the induced [[Hadamard vacuum state]] ([this prop.](Wick+algebra#WickAlgebraCanonicalState)), hence the [[state on a star-algebra|state]] whose [[distribution|distributional]] [[2-point function]] is the chosen [[Wightman propagator]]:

$$
  \left\langle \mathbf{\Phi}^a(x) \mathbf{\Phi}^b(y)\right\rangle
  \;=\;
  \hbar \, \Delta_H^{a b}(x,y)
  \,.
$$

Given any [[microcausal polynomial observable]] $A \in PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]$ then its value in this state is called its _free [[vacuum expectation value]]_

$$
  \left\langle
    A
  \right\rangle
  \;\in\;
  \mathbb{C}[ [ \hbar, g, j] ]
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

Finally, for $A \in LocObs(E_{\text{BV-BRST}})$ we write $supp(A) \subset \Sigma$ for its spacetime support ([this def.](A+first+idea+of+quantum+field+theory#SpacetimeSupport)).
For $S_1, S_2 \subset \Sigma$ two [[subsets]] of [[spacetime]] we write

$$
  S_1 {\vee\!\!\!\wedge} S_2
  \phantom{AAA}
  \left\{
    \array{
      \text{"}S_1 \, \text{does not intersect the past of} \, S_2\text{"}
      \\
      \Updownarrow
      \\
      \text{"}S_2 \, \text{does not intersect the future of} \, S_1\text{"}
    }
  \right.
$$

for the  [[causal ordering]]-[[relation]] and


$$
  S_1 {\gt\!\!\!\!\lt} S_2
  \phantom{AAA}
  \text{for}
  \phantom{AAA}
  \array{
    S_1 {\vee\!\!\!\wedge} S_2
    \\
    \text{and}
    \\
    S_2 {\vee\!\!\!\wedge} A_1
  }
$$

for _[[spacelike]] separation_.

=--

+-- {: .num_remark}
###### Remark

For the purposes of constructing or defining the Wick algebra, the conditions on $\Delta_H$ or $H$ could be relaxed. Requiring $\Delta_H$ to be an honest [[Wightman propagator]] means that it is a distribution satisfying the [[Hadamard distribution|Hadamard wavefront condition]], as well as addition positivity and normalization requirements. Dropping the positivity and some of the normalization requirements, $\Delta_H$ is then only a _Hadamard parametrix_ for the Wightman propagator. The construction of the Wick algebra with respect to $\Delta_H$ still makes sense, but $:(-):$ can no longer be interpreted as normal ordering with respect to a fixed vacuum state. In fact, in [[locally covariant pAQFT]], the property for $\Delta_H$ to be the Wightman propagator for a state is in conflict with local covariance. On the other hand, there is no problem with selecting a locally covariant Hadamard parametrix $\Delta_H$, which allows the construction or definition of the Wick algebra to be locally covariant.

=--

Being concerned with [[perturbative QFT|perturbation theory]] means mathematically that we consider _[[formal power series]]_
in [[deformation]] parameters $\hbar$ ("[[Planck's constant]]") and $g$ ("[[coupling constant]]"), also in $j$ ("[[source field]]"),
see also remark \ref{AsymptoticSeriesObservables}. The following collects our notational conventions for these matters:

+-- {: .num_defn #FormalParameters}
###### Definition
**([[formal power series]] of [[observables]] for [[perturbative QFT]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

Write

$$
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]
  \;\coloneqq\;
  \underset{ k_1, k_2, k_3 \in \mathbb{N}}{\prod}
  LocObs(E_{\text{BV-BRST}})\langle \hbar^{k_1} g^{k_2} j^{k^3}\rangle
$$

for the space of [[formal power series]] in three formal [[variables]]

1. $\hbar$ ("[[Planck's constant]]"),

1. $g$ ("[[coupling constant]]")

1. $j$ ("[[source field]]")

with  [[coefficients]] in the [[topological vector spaces]] of the [[off-shell]] polynomial [[local observables]] of the [[free field]] theory; similarly for the [[off-shell]] [[microcausal polynomial observables]]:

$$
  PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j ] ]
  \;\coloneqq\;
  \underset{ k_1, k_2, k_3 \in \mathbb{N}}{\prod}
  PolyObs(E_{\text{BV-BRST}})_{mc}\langle \hbar^{k_1} g^{k_2} j^{k^3}\rangle
  \,.
$$

Similary

$$
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g  ] ]
  \,,
   \phantom{AAA}
  PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g  ] ]
$$

denotes the subspace for which no powers of $j$ appear, etc.

Accordingly

$$
  C^\infty_{cp}(\Sigma) \langle g \rangle
$$

denotes the vector space of [[bump functions]] on [[spacetime]] tensored with the vector space spanned by a single copy of $g$.
The elements

$$
  g_{sw} \in C^\infty_{cp}(\Sigma)\langle g \rangle
$$

may be regarded as [[spacetime]]-dependent "[[coupling constants]]" with compact support,
called _[[adiabatic switching|adiabatically switched]] couplings_.

Similarly then

$$
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]\langle g , j \rangle
$$

is the subspace of those formal power series that are at least linear in $g$ or $j$ (hence those that vanish if one sets $g,j = 0$ ).
Hence every element of this space may be written in the form

$$
  O
    =
  g S_{int} + j A
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]\langle g , j \rangle
  \,,
$$

where the notation is to suggest that we will think of the coefficient of $g$ as an ([[adiabatic switching|adiabatically switched]])
[[interaction]] [[action functional]].

In particular for

$$
  \mathbf{L}_{int}
  \;\in\;
  \Omega^{p+1,0}_\Sigma(E_{\text{BV-BRST}})[ [ \hbar , g] ]
$$

a [[formal power series]] in $\hbar$ and $g$ of [[local Lagrangian densities]], thought of as a local [[interaction]] Lagrangian, and if

$$
  g_{sw}
  \;\in\;
  C^\infty_{cp}(\Sigma) \langle g \rangle
$$

is an [[adiabatic switching|adiabatically switched]] coupling as before, then the [[transgression of variational differential forms|transgression]] of the product

$$
  g_{sw} \mathbf{L}_{int}
  \;\in\;
  \Omega^{p+1,0}_{\Sigma,cp}(E_{\text{BV-BRST}})[ [ \hbar ,g ] ]\langle g \rangle
$$

is such an [[adiabatic switching|adiabatically switched]] [[interaction]]

$$
  g S_{int}
  \;=\;
  \tau_\Sigma( g_{sw} \mathbf{L}_{int} )
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g] ]\langle g \rangle
  \,.
$$

We also consider the space of [[off-shell]] [[microcausal polynomial observables]] of the [[free field theory]] with formal parameters adjoined

$$
  PolyObs(E_{\text{BV-BRST}})_{mc} ((\hbar)) [ [ g , j] ]
  \,,
$$

which, in its $\hbar$-dependent, is the space of _[[Laurent series]]_ in $\hbar$, hence the space exhibiting also negative formal powers of $\hbar$.

=--

$\,$

#### Perturbative S-Matrices
 {#PerturbativeSMatrixAndTimeOrderedProducts}

We introduce now the [[axioms]] for perturbative [[scattering matrices]] relative to a fixed [[relativistic field theory|relativistic]] [[free field theory|free]] [[Lagrangian field theory|Lagrangian]] [[quantum field theory|quantum field]] [[vacuum]] (def. \ref{VacuumFree} below) according to _[[causal perturbation theory]]_ (def. \ref{LagrangianFieldTheoryPerturbativeScattering} below).
Since the first of these axioms requires the S-matrix to be a formal sum of [[multilinear map|multi-]][[linear continuous functionals]], it is convenient to impose axioms on these directly: this is the axiomatics for _[[time-ordered products]]_
in def. \ref{TimeOrderedProduct} below. That these latter axioms already imply the former
is the statement of prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix} below. Its proof
requires a close look at the "[[reverse-time ordered products]]" for the inverse S-matrix (def. \ref{ReverseTimeOrderedProduct} below)
and their induced reverse-causal factorization (prop. \ref{ReverseCausalFactorizationOfReverseTimeOrderedProducts} below).


+-- {: .num_defn #LagrangianFieldTheoryPerturbativeScattering}
###### Definition
**([[S-matrix]] [[axioms]] -- [[causal perturbation theory]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

Then a _perturbative [[S-matrix]] scheme_ for [[perturbative QFT]] around this [[free field|free]] [[vacuum]] is a [[function]]

$$
  \mathcal{S}
    \;\;\colon\;\;
  LocObs(E_{\text{BV-BRST}})[ [\hbar , g, j] ]\langle g, j \rangle
    \overset{\phantom{AAA}}{\longrightarrow}
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g, j ] ]
$$

from [[local observables]] to [[microcausal polynomial observables]] of the free vacuum theory,
with formal parameters adjoined as indicated (def. \ref{FormalParameters}),
such that the following two conditions "perturbation" and "causal additivity (jointly: "[[causal perturbation theory]]") hold:

1. ([[perturbative quantum field theory|perturbation]])

   There exist [[multilinear map|multi-]][[linear continuous functionals]] (over $\mathbb{C}[ [\hbar, g, j] ]$) of the form

   $$
     \label{TimeOrderedProductsInSMatrix}
     T_k
       \;\colon\;
     \left(
       {\, \atop \,}
       LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]\langle g, j \rangle
       {\, \atop \,}
     \right)^{\otimes^k_{\mathbb{C}[ [\hbar, g, j] ]}}
       \longrightarrow
     PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g, j ] ]
   $$

   for all $k \in \mathbb{N}$, such that:

   1. The nullary map is [[constant function|constant]] on the [[neutral element|unit]] of the [[Wick algebra]]

      $$
        T_0( g S_{int} + j A) = 1
      $$

   1. The unary map is the inclusion of [[local observables]] as [[normal-ordered products]] (eq:NormalOrderingLocalObservables)

      $$
        T_1(g S_{int} + j A) = g :S_{int}: + j :A:
      $$

   1. The perturbative S-matrix is the [[exponential series]] of these maps in that for
      all $g S_{int} + j A  \in LocObs(E_{\text{BV-BRST}})[ [\hbar , g, j] ]\langle g,j\rangle $

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

   For all perturbative [[local observables]] $ O_0, O_1, O_2 \in LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]$ we have

   \[
     \label{CausalAdditivity}
     \left(
        {\, \atop \,}
        supp( O_1 ) {\vee\!\!\!\wedge} supp( O_2 )
        {\, \atop \,}
     \right)
     \;\; \Rightarrow \;\;
     \left(
       {\, \atop \,}
       \mathcal{S}( O_0 + O_1 + O_2 )
       \;\,
       \mathcal{S}( O_0 + O_1 )
       \,
       \mathcal{S}( O_0 )^{-1}
       \,
       \mathcal{S}(O_0 + O_2)
       {\, \atop \,}
     \right)
     \,.
   \]

(The [[inverse]] $\mathcal{S}(O)^{-1}$ of $\mathcal{S}(O)$ with respect to the [[Wick algebra]]-[[structure]]
is implied to exist by axiom "perturbation", see remark \ref{PerturbativeSMatrixInverse} below.)

=--

Def. \ref{LagrangianFieldTheoryPerturbativeScattering} is due to ([Epstein-Glaser 73 (1)](#EpsteinGlaser73)),
following ([Stückelberg 49-53](causal+perturbation+theory#Stueckelberg49), [Bogoliubov-Shirkov 59](causal+perturbation+theory#BogoliubovShirkov59)).
That the [[domain]] of an S-matrix scheme is indeed the space of [[local observables]] was made explicit (in terms of axioms for the [[time-ordered products]], see def. \ref{TimeOrderedProduct} below), in ([Brunetti-Fredenhagen 99, section 3](#BrunettiFredenhagen99), [D&#252;tsch-Fredenhagen 04, appendix E](#DuetschFredenhagen04), [Hollands-Wald 04,  around (20)](#HollandsWald04)). Review includes ([Rejzner 16, around def. 6.7](#Rejzner16), [Dütsch 18, section 3.3](#Duetsch18)).

+-- {: .num_remark #PerturbativeSMatrixInverse}
###### Remark
**([[inverse|invertibility]] of the [[S-matrix]])**

The mutliplicative inverse $S(-)^{-1}$ of the perturbative [[S-matrix]] in def. \ref{LagrangianFieldTheoryPerturbativeScattering}
with respect to the [[Wick algebra]]-product indeed exists, so that the list of axioms is indeed well defined: By the axiom "perturbation" this follows with the usual formula for the multiplicative inverse of [[formal power series]] that are non-vanishing in degree 0:

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

This expression for the inverse of S-matrix may usefully be re-organized in terms of "rever-time ordered products" (def. \ref{ReverseTimeOrderedProduct} below), see prop. \ref{ReverseTimOrderedProductsGiveReverseSMatrix} below.

Notice that $\mathcal{S}(-g S_{int} - j A )$ is instead the inverse with respect to the [[time-ordered products]] (eq:TimeOrderedProductsInSMatrix) in that

$$
  T( \mathcal{S}(-g S_{int} -  j A ) \,,\, \mathcal{S}(g S_{int} + j A)  )
  \;=\;
  1
  \;=\;
  T( \mathcal{S}(g S_{int} + j A )  \,,\,  \mathcal{S}(-g S_{in} - j A ) )
  \,.
$$

(Since the time-ordered product is, by definition, symmetric in its arguments, the usual formula for the multiplicative inverse of
an [[exponential series]] applies).

=--

+-- {: .num_remark #MoreDeformationParameters}
###### Remark
**(adjoining further [[deformation]] parameters)

The definition of [[S-matrix]] schemes in def. \ref{LagrangianFieldTheoryPerturbativeScattering} has immediate variants where arbitrary countable sets $\{g_n\}$ and $\{j_m\}$ of formal [[deformation]] parameters are considered, instead of just a single [[coupling constant]] $g$ and a single [[source field]] $j$. The more such constants are considered, the "more perturbative" the theory becomes and the stronger the implications.

=--

Given a perturbative [[S-matrix]] scheme (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) it immediately
induces a corresponding concept of [[observables]]:

+-- {: .num_defn #SchemeGeneratingFunction}
###### Definition
**([[generating function]] scheme for [[interacting field observables]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}.

The corresponding _[[generating function]] scheme_
(for [[interacting field observables]], def. \ref{InteractingFieldObservables} below) is the functional

$$
  \mathcal{Z}_{(-)}(-)
    \;\colon\;
    LocObs(E_{\text{BV-BRST}})[ [\hbar, g] ]\langle g \rangle
    \;\times\;
    LocObs(E_{\text{BV-BRST}})[ [\hbar, j] ]\langle j \rangle
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [g , j] ]
$$

given by

$$
  \label{GeneratingFunctionInducedFromSMatrix}
  \mathcal{Z}_{g S_{int}}(j A)
    \;\coloneqq\;
  \mathcal{S}(g S_{int})^{-1} \mathcal{S}( g S_{int} + j A )
  \,.
$$

=--


+-- {: .num_prop #ZCausalAdditivity}
###### Proposition
**([[causal additivity]] in terms of [[generating functions]])**

In terms of the [[generating functions]] $\mathcal{Z}$ (def. \ref{SchemeGeneratingFunction}) the axiom "[[causal additivity]]"
on the [[S-matrix]] scheme $\mathcal{S}$ (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) is equivalent to:

* ([[causal additivity]] in terms of $\mathcal{Z}$)

  For all [[local observables]] $O_0, O_1, O_2 \in LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]\otimes\mathbb{C}\langle g,j\rangle$ we have

  $$
    \label{GeneratingFunctionCausalAdditivity}
    \begin{aligned}
    \left(
       {\, \atop \,}
       supp(O_1) {\vee\!\!\!\wedge} supp(O_2)
       {\, \atop \,}
    \right)
    & \;\; \Rightarrow \;\;
    \left(
      {\, \atop \,}
      \mathcal{Z}_{O_0}( O_1 ) \, \mathcal{Z}_{O_0}( O_2)
      =
      \mathcal{Z}_{  O_0 }( O_1 + O_2 )
      {\, \atop \,}
    \right)
    \\
    & \;\; \Leftrightarrow \;\;
    \left(
      {\, \atop \,}
      \mathcal{Z}_{ O_0 + O_1 }( O_2 )
      =
      \mathcal{Z}_{ O_0 }( O_2 )
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

Multiplying both sides of (eq:CausalAdditivity) by $\mathcal{S}(O_0)^{-1}$ yields

$$
  \underset{
    \mathcal{Z}_{ O_0 }( O_1 + O_2 )
  }{
  \underbrace{
    \mathcal{S}( O_0 )^{-1}
    \mathcal{S}( O_0 + O_1 + O_2 )
  }
  }
  \;=\;
  \underset{
    \mathcal{Z}_{ O_0 }( O_1 )
  }{
  \underbrace{
    \mathcal{S}( O_0 )^{-1} \mathcal{S}( O_0 + O_1 )
  }
  }
  \underset{
    \mathcal{Z}_{ O_0 }( O_2 )
  }{
  \underbrace{
    \mathcal{S}( O_0 )^{-1} \mathcal{S}( O_0 + O_2 )
  }
  }
$$

This is the first line of (eq:GeneratingFunctionCausalAdditivity).

Multiplying both sides of (eq:CausalAdditivity) by $\mathcal{S}( O_0 + O_1 )^{-1}$ yields

$$
  \underset{
    = \mathcal{Z}_{ O_0 + O_1 }(  O_2 )
  }{
  \underbrace{
    \mathcal{S}( O_0 + O_1 )^{-1}
    \mathcal{S}( O_0 + O_1 + O_2 )
  }
  }
  \;=\;
  \underset{
    = \mathcal{Z}_{ O_0 }( O_2 )
  }{
  \underbrace{
    \mathcal{S}( O_0 )^{-1} \mathcal{S}( O_0 + O_2 )
  }
  }
  \,.
$$

This is the second line of (eq:GeneratingFunctionCausalAdditivity).


=--


+-- {: .num_defn #InteractingFieldObservables}
###### Definition
**([[interacting field observables]] -- [[Bogoliubov's formula]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}, and let $g S_{int} \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ]\langle g \rangle$ be a [[local observable]] regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]]-[[action functional|functional]].

Then for $A \in LocObs(E_{\text{BV-BRST}})[ [\hbar , g] ]$ a [[local observable]] of the [[free field theory]],
we say that the corresponding [[local interacting field observable]]

$$
  A_{int} \in PolyObs(E_{\text{BV-BRST}})_{mc}[ [\hbar, g] ]
$$

is the [[coefficient]] of $j^1$ in the [[generating function]] (eq:GeneratingFunctionInducedFromSMatrix):

$$
  \label{BogoliubovsFormula}
  \begin{aligned}
    A_{int}
    &\coloneqq
    i \hbar \frac{d}{d j}
    \left(
      {\, \atop \,}
      \mathcal{Z}_{ g S_{int} }( j A )
      {\, \atop \,}
    \right)_{\vert_{j = 0}}
    \\
    & \coloneqq
    i \hbar \frac{d}{d j}
    \left(
      {\, \atop \,}
      \mathcal{S}(g S_{int})^{-1} \, \mathcal{S}( g S_{int} + j A )
      {\, \atop \,}
    \right)_{\vert_{j = 0}}
    \\
    & =
    \mathcal{S}(g S_{int})^{-1}
    T\left(
      \mathcal{S}(g S_{int}), A
    \right)
    \,.
  \end{aligned}
$$

This expression is called _[[Bogoliubov's formula]]_, due to ([Bogoliubov-Shirkov 59](#BogoliubovShirkov59)).

One thinks of $A_{int}$ as the [[deformation]] of the [[local observable]] $A$ as the [[interaction]] $S_{int}$ is turned on; and speaks of an element of the _[[interacting field algebra of observables]]_. Their value ("[[expectation value]]") in the given free [[Hadamard vacuum state]]
$\langle  -\rangle$ (def. \ref{VacuumFree}) is a [[formal power series]] in [[Planck's constant]] $\hbar$ and in the [[coupling constant]] $g$, with [[coefficients]] in the [[complex numbers]]

$$
  \left\langle
    A_{int}
  \right\rangle
  \;\in\;
  \mathbb{C}[ [\hbar, g] ]
$$

which express the [[probability amplitudes]] that reflect the predictions of the [[perturbative QFT]], which may be compared to [[experiment]].

=--

([Epstein-Glaser 73, around (74)](#EpsteinGlaser73); review includes ([D&#252;tsch-Fredenhagen 00, around (17)](#DuetschFredenhagen00), [Dütsch 18, around (3.212)](pAQFT#Duetsch18)).


+-- {: .num_example #FormalPowerSeriesInteractingFieldObservables}
###### Remark
**([[interacting field observables]] are [[formal deformation quantization]])**

The [[interacting field observables]] in def. \ref{InteractingFieldObservables} are indeed [[formal power series]] in the formal parameter $\hbar$ ([[Planck's constant]]), as opposed to being more general [[Laurent series]], hence they involve no [[negative number|negative]] powers of $\hbar$ ([Dütsch-Fredenhagen 00, prop. 2 (ii)](interacting+field+observable#DuetschFredenhagen00), [Hawkins-Rejzner 16, cor. 5.2](interacting+field+observable#HawkinsRejzner16)).  This is not immediate, since by def. \ref{LagrangianFieldTheoryPerturbativeScattering} the [[S-matrix]] that they are defined from does involve negative powers of $\hbar$.

It follows in particular that the [[interacting field observables]] have a [[classical limit]] $\hbar \to 0$, which
is not the case for the [[S-matrix]] itself (due to it involving negative powers of $\hbar$).
Indeed the [[interacting field observables]] constitute a _[[formal deformation quantization]]_ of the [[covariant phase space]]
of the [[interacting field theory]] (prop. \ref{InteractingFieldAlgebraOfObservablesIsFormalDeformationQuantization} below)
and are thus the more fundamental concept.

=--

As the name suggests, the [[S-matrices]] in def. \ref{LagrangianFieldTheoryPerturbativeScattering} serve to express [[scattering amplitudes]] (example \ref{ScatteringAmplitudeFromInteractingFieldObservables} below). But by remark \ref{FormalPowerSeriesInteractingFieldObservables}
the more fundamental concept is that of the [[interacting field observables]]. Their perspective reveals that
consistent interpretation of [[scattering amplitudes]] requires the following condition on the relation between the
[[vacuum state]] and the [[interaction]] term:

+-- {: .num_defn #VacuumStability}
###### Definition
**([[vacuum stability]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}, and let $g S_{int} \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g] ]\langle g \rangle$ be a [[local observable]], regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

We say that the given [[Hadamard vacuum state|Hadamard]] [[vacuum state]] ([this prop.](Wick+algebra#WickAlgebraCanonicalState))

$$
  \langle - \rangle
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar , g, j ] ]
  \longrightarrow
  \mathbb{C}[ [ \hbar, g, j ] ]
$$

is _[[vacuum stability|stable]]_ with respect to the [[interaction]] $S_{int}$, if for all elements of the [[Wick algebra]]

$$
  A \in PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g] ]
$$

we have

$$
  \left\langle
    A \mathcal{S}(g S_{int})
  \right\rangle
  \;=\;
  \left\langle
     \mathcal{S}(g S_{int})
  \right\rangle
  \,
  \left\langle
    A
  \right\rangle
  \phantom{AA}
  \text{and}
  \phantom{AA}
  \left\langle
    \mathcal{S}(g S_{int})^{-1}
    A
  \right\rangle
  \;=\;
  \frac{1}
  {
    \left\langle
      \mathcal{S}(g S_{int})
    \right\rangle
   }
   \left\langle
     A
   \right\rangle
$$

=--


+-- {: .num_example #InteractinFieldTimeOrderedProduct}
###### Example
**([[time-ordered product]] of [[interacting field observables]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}, and let $g S_{int} \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ]\langle g \rangle$ be a [[local observable]] regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]]-[[action functional|functional]].

Consider two [[local observables]]

$$
  A_1, A_2
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar , g] ]
$$

with [[causal ordering|causally ordered]] spacetime support

$$
  supp(A_1) {\vee\!\!\!\!\wedge} supp(A_2)
$$

Then [[causal additivity]] according to prop. \ref{ZCausalAdditivity} implies that the
[[Wick algebra]]-product of the corresponding [[interacting field observables]]
$(A_1)_{int}, (A_2)_{int} \in PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ] $ (def. \ref{InteractingFieldObservables})
is

$$
  \begin{aligned}
    (A_1)_{int}
    (A_2)_{int}
    & =
    \left(
      \frac{\partial}{\partial j} \mathcal{Z}(j A_1 )
    \right)_{\vert j = 0}
    \left(
      \frac{\partial}{\partial j} \mathcal{Z}( j A_2 )
    \right)_{\vert j = 0}
    \\
    & =
    \frac{\partial^2}{\partial j_1 \partial j_2}
    \left(
      {\, \atop \,}
      \mathcal{Z}( j_1 A_1 )
      \mathcal{Z}( j_2 A_2 )
      {\, \atop \,}
    \right)_{
       \left\vert { {j_1 = 0}, \atop {j_2 = 0} } \right.
    }
    \\
    & =
    \frac{\partial^2}{\partial j_1 \partial j_2}
    \left(
      {\, \atop \,}
      \mathcal{Z}( j_1 A_1 + j_2 A_2 )
      {\, \atop \,}
    \right)_{
       \left\vert { {j_1 = 0}, \atop {j_2 = 0} } \right.
    }
  \end{aligned}
$$

Here the last line makes sense if one extends the axioms on the [[S-matrix]] in prop. \ref{LagrangianFieldTheoryPerturbativeScattering}
from formal power series in $\hbar, g, j$ to formal power series in $\hbar, g, j_1, j_2, \cdots$ (remark \ref{MoreDeformationParameters}).
Hence in this generalization, the [[generating functions]] $\mathcal{Z}$ are not just generating functions
for [[interacting field observables]] themselves, but in fact for _[[time-ordered products]]_ of interacting field observables.

=--

An important special case of [[time-ordered products]] of [[interacting field observables]] as in example \ref{InteractinFieldTimeOrderedProduct}
is the following special case of _[[scattering amplitudes]]_, which is the example that gives the _[[scattering matrix]]_ in def. \ref{LagrangianFieldTheoryPerturbativeScattering} its name:

+-- {: .num_example #ScatteringAmplitudeFromInteractingFieldObservables}
###### Example
**([[scattering amplitudes]] as [[vacuum expectation values]] of [[interacting field observables]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}, and let $g S_{int} \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ]\langle g \rangle$ be a [[local observable]] regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]]-[[action functional|functional]],
such that the [[vacuum state]] is [[vacuum stability|stable]] with respect to $g S_{int}$ (def. \ref{VacuumStability}).

Consider [[local observables]]

$$
  \array{
    A_{in,1}, \cdots, A_{in , n_{in}},
    \\
    A_{out,1}, \cdots, A_{out, n_{out}}
  }
  \;\;\in\;\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g] ]
$$

whose spacetime support satisfies the following [[causal ordering]]:

$$
  A_{out, i_{out} }
  {\gt\!\!\!\!\lt}
  A_{out, j_{out}}
  \phantom{AAA}
  A_{out, i_{out} }
    {\vee\!\!\!\wedge}
  S_{int}
    {\vee\!\!\!\wedge}
  A_{in, i_{in}}
  \phantom{AAA}
  A_{in, i_{in} }
  {\gt\!\!\!\!\lt}
  A_{in, j_{in}}
$$

for all $1 \leq i_{out} \lt j_{out} \leq n_{out}$ and $1 \leq  i_{in} \lt j_{in} \leq n_{in}$.

Then the [[vacuum expectation value]] of the [[Wick algebra]]-product of the corresponding [[interacting field observables]] (def. \ref{InteractingFieldObservables})
is

$$
  \begin{aligned}
   &
   \left\langle
     {\, \atop \,}
     (A_{out, 1})_{int}
     \cdots
     (A_{out,n_{out}})_{int}
     \,
     (A_{in, 1})_{int}
     \cdots
     (A_{in,n_{in}})_{int}
     {\, \atop \,}
   \right\rangle
   \\
   & =
   \left\langle
     {\, \atop \,}
       A_{out,1}
       \cdots
       A_{out,n_{out}}
    \right|
       \;
       \mathcal{S}(g S_{int})
       \;
    \left|
       A_{in,1}
       \cdots
       A_{in, n_{in}}
     {\, \atop \,}
   \right\rangle
   \\
   & \coloneqq
   \frac{1}{
     \left\langle \mathcal{S}(g S_{int}) \right\rangle
   }
   \left\langle
     {\, \atop \,}
       A_{out,1}
       \cdots
       A_{out,n_{out}}
       \;
       \mathcal{S}(g S_{int})
       \;
       A_{in,1}
       \cdots
       A_{in, n_{in}}
     {\, \atop \,}
   \right\rangle
   \,.
  \end{aligned}
$$

These [[vacuum expectation values]] are interpreted, in the [[adiabatic limit]] where $g_{sw} \to 1$, as _[[scattering amplitudes]]_ (remark \ref{FromAxiomaticSMatrixScatteringAmplitudes} below).

=--

+-- {: .proof}
###### Proof

For notational convenience, we spell out the argument for $n_{in} =  1 = n_{out}$. The general case
is directly analogous.

So assuming the [[causal order]]

$$
  supp(A_{out})
   {\vee\!\!\!\wedge}
  supp(S_{int})
   {\vee\!\!\!\wedge}
  supp(A_{in})
$$

we compute with [[causal additivity]] via prop. \ref{ZCausalAdditivity} as follows:


$$
  \begin{aligned}
    (A_{out})_{int} (A_{in})_{int}
    & =
    \frac{d^2 }{\partial j_{out} \partial j_{in}}
    \left(
       \mathcal{Z}( j_{out} A_{out} )
       \mathcal{Z}( j_{in} A_{in} )
    \right)_{\left\vert { { j_{out} = 0 } \atop { j_{in} = 0 } }  \right.}
    \\
    & =
    \frac{\partial^2 }{\partial j_{out} \partial j_{in}}
    \left(
       \mathcal{S}(g S_{int})^{-1}
       \underset{
         =
         \mathcal{S}(j_{out} A_{out})
         \mathcal{S}(g S_{int})
       }{
       \underbrace{
         \mathcal{S}(g S_{int} + j_{out} A_{out})
       }
       }
       \mathcal{S}(g S_{int})^{-1}
       \underset{
         = \mathcal{S}(g S_{int}) \mathcal{S}(j_{in} A_{in})
       }{
       \underbrace{
         \mathcal{S}(g S_{int} + j_{in}A_{in})
       }
       }
    \right)_{\left\vert { { j_{out} = 0 } \atop { j_{in} = 0 } }  \right.}
    \\
    & =
    \frac{\partial^2 }{\partial j_{out} \partial j_{in}}
    \left(
       \mathcal{S}(g S_{int})^{-1}
       \mathcal{S}(j_{out} A_{out})
       \underset{
         = \mathcal{S}(g S_{int})
       }{
       \underbrace{
         \mathcal{S}(g S_{int})
         \mathcal{S}(g S_{int})^{-1}
         \mathcal{S}(g S_{int})
       }
       }
       \mathcal{S}(j_{in} A_{in})
    \right)_{\left\vert { { j_{out} = 0 } \atop { j_{in} = 0 } }  \right.}
    \\
    & =
    \mathcal{S}(g S_{int})^{-1}
    \,
    \left(
      {\, \atop \,}
      A_{out}
      \mathcal{S}(g S_{int})
      A_{in}
      {\, \atop \,}
    \right)
    \,.
  \end{aligned}
$$

With this the statement follows by the definition of [[vacuum stability]] (def. \ref{VacuumStability}).

=--


+-- {: .num_remark}
###### Remark
**(computing [[S-matrices]] via [[Feynman perturbation series]])**

For practical computation of [[vacuum expectation values]] of [[interacting field observables]] (example \ref{InteractinFieldTimeOrderedProduct})
and hence in particular, via example \ref{ScatteringAmplitudeFromInteractingFieldObservables}, of [[scattering amplitudes]],
one needs some method for collecting all the contributions to the [[formal power series]] in increasing order in $\hbar$ and $g$.

Such a method is provided by the [[Feynman perturbation series]] (example \ref{FeynmanPerturbationSeries} below)
and the [[effective action]] (def. \ref{InPerturbationTheoryActionEffective}), see example \ref{SMatrixVacuumContribution} below.

=--



$\,$

#### Conceptual remarks
 {#RemarksOnCausalPerturbationTheoryAxioms}

The simple axioms for [[S-matrices]] in [[causal perturbation theory]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) and hence for [[interacting field observables]] (def. \ref{InteractingFieldObservables}) have a wealth of
implications and consequences. Before discussing these formally below, we here make a few informal remarks meant to put various relevant concepts into perspective:

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
suggests that in realistic field theories these series _never_ converge for _any_ [[positive real number|positive]] value of $\hbar$ and/or $g$. Namely convergence for $g$ would imply a [[positive real number|positive]] _[[radius of convergence]]_ around $g = 0$, which would imply convergence also for $-g$ and even for [[imaginary number|imaginary]] values of $g$, which would however correspond to unstable [[interactions]] for which no converging field theory is to be expected. (See [Helling, p. 4](perturbative+quantum+field+theory#Helling) for the example of [[phi^4 theory]].)

In physical practice one tries to interpret these non-converging [[formal power series]] as _[[asymptotic expansions]]_ of
actual but hypothetical functions in $\hbar, g$, which reflect the actual but hypothetical _[[non-perturbative quantum field theory]]_
that one imagines is being approximated by [[perturbative QFT]] methods. An _[[asymptotic expansion]]_ of a function is a [[power series]] which may not converge, but which has for every $n \in \mathbb{N}$ an estimate for how far the [[sum]] of the first $n$ terms in the series may differ from the function being approximated.

For examples such as [[quantum electrodynamics]] and [[quantum chromodynamics]], as in the [[standard model of particle physics]], the truncation of these [[formal power series]] [[scattering amplitudes]] to the first handful of [[loop orders]] in $\hbar$ happens to agree with [[experiment]] (such as at the [[LHC]] collider) to high precision (for [[QED]]) or at least decent precision (for [[QCD]]), at least away from infrared phenomena (see remark \ref{AdiabaticLimit}).

In summary this says that [[perturbative QFT]] is an extremely _coarse_ and restrictive approximation to what should be genuine [[non-perturbative quantum field theory]], while at the same time it happens to match certain experimental observations to remarkable degree, albeit only if some ad-hoc truncation of the resulting power series is considered.

This is strong motivation for going beyond [[perturbative QFT]] to understand and construct genuine [[non-perturbative quantum field theory]]. Unfortunately, this is a wide-open problem, away from toy examples. Not a single [[interacting field theory]] in [[spacetime]] [[dimension]] $\geq 4$ has been non-perturbatively quantized. Already a single aspect of the [[non-perturbative quantum field theory|non-perturbative]] [[quantization of Yang-Mills theory]] (as in [[QCD]]) has famously been advertized as one of the _[Millennium Problems](http://www.claymath.org/millennium-problems/yang%E2%80%93mills-and-mass-gap)_ of our age; and speculation about [[non-perturbative quantum field theory|non-perturbative]] [[quantum gravity]] is the subject of much activity.

Now, as the name indicates, the [[axioms]] of _[[causal perturbation theory]]_ (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) do
_not_ address [[non-perturbative effect|non-perturbative aspects]] of [[non-perturbative field theory]]; the convergence or non-convergence of the [[formal power series]] that are axiomatized by [[Bogoliubov's formula]] (def. \ref{InteractingFieldObservables}) is _not_ addressed by the theory.
The point of the axioms of [[causal perturbation theory]] is to give rigorous mathematical meaning to _everything else_ in [[perturbative QFT]].

=--


+-- {: .num_remark #DysonCausalFactorization}
###### Remark
**([[Dyson series]] and [[Schrödinger equation]] in [[interaction picture]])**

The axiom "[[causal additivity]]" (eq:CausalAdditivity) on an [[S-matrix]] scheme (def. \ref{LagrangianFieldTheoryPerturbativeScattering})
implies immediately this seemingly weaker condition (which turns out to be equivalent, this is prop. \ref{CausalFactorizationAlreadyImpliesSMatrix} below):

* ([[causal factorization]])

  For all [[local observables]] $O_1, O_2 \in LocObs(E_{\text{BV-BRST}})[ [\hbar, h, j] ]\langle g , j\rangle $ we have

  $$
    \left(
       {\, \atop \,}
       supp(O_1) {\vee\!\!\!\wedge} supp(O_2)
       {\, \atop \,}
    \right)
    \;\; \Rightarrow \;\;
    \left(
      {\, \atop \,}
      \mathcal{S}( O_1 + O_2 )
      =
      \mathcal{S}( O_1 ) \, \mathcal{S}( O_2 )
      {\, \atop \,}
   \right)
  $$

(This is the special case of "causal additivity" for $O_0 = 0$, using that  by the axiom "perturbation" (eq:ExponentialSeriesScatteringMatrix) we have $\mathcal{S}(0) = 1$.)

If we now think of $O_1 = g S_{1}$ and $O_2 = g S_2$ themselves as [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functionals]], then this becomes

  $$
    \left(
       {\, \atop \,}
       supp(S_1) {\vee\!\!\!\wedge} supp(S_2)
       {\, \atop \,}
    \right)
    \;\; \Rightarrow \;\;
    \left(
      {\, \atop \,}
      \mathcal{S}( g S_1 + g S_2 )
      =
      \mathcal{S}( g S_1) \, \mathcal{S}( g sS_2)
      {\, \atop \,}
   \right)
  $$

This exhibits the [[S-matrix]]-scheme as a "[[causal ordering|causally ordered]] [[exponential]]"
or "[[Dyson series]]" of the [[interaction]], hence as a refinement to [[relativistic field theory]] of what in
[[quantum mechanics]] is the "integral version of the [[Schrödinger equation]] in the [[interaction picture]]" (eq:IntegralVersionSchroedingerEquationInInteractionPicture). (See also [Scharf 95, second half of 0.3](#Scharf95)).

The relevance of manifest [[causal additivity]] of the [[S-matrix]], over just [[causal factorization]] (even though both conditions happen to be equivalent, see prop. \ref{CausalFactorizationAlreadyImpliesSMatrix} below), is that it directly implies that
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

Here the would-be [[integration]] is thought to be over the [[space of field histories]] $\Gamma_\Sigma(E_{\text{BV-BRST}})_{asm}$ (the [[space of sections]] of the given [[field bundle]]) for [[field histories]] which satisfy given asymptotic conditions at $x^0 \to \pm \infty$; and as these boundary conditions vary the above is regarded as a would-be [[integral kernel]] that defines the required operator in the [[Wick algebra]] (e.g. [Weinberg 95, around (9.3.10) and (9.4.1)](#Weinberg95)). This is related to the intuitive picture of the [[Feynman perturbation series]] expressing a sum over all possible interactions of [[virtual particles]] (remark \ref{WorldlineFormalism}).

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

two [[microcausal  polynomial observables]], with [[causal ordering]]

$$
  supp(A_{out}) {\vee\!\!\!\wedge} supp(A_{int})
$$

the corresponding _[[scattering amplitude]]_ (as in example \ref{ScatteringAmplitudeFromInteractingFieldObservables}) is the value (called "[[expectation value]]" when referring to $A^\ast_{out} \, \mathcal{S}(S_{int}) \, A_{in}$, or "matrix element" when referring to $\mathcal{S}(S_{int})$, or "transition amplitude" when referring to $\left\langle A_{out} \right\vert$ and $\left\vert A_{in} \right\rangle$)

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
  \mathbb{C}[ [ \hbar, g ] ]
  \,.
$$

for the [[Wick algebra]]-product $A^\ast_{out} \, \mathcal{S}(S_{int})\, A_{in} \in PolyObs(E_{\text{BV-BRST}})[ [\hbar, g ] ]$
in the given [[Hadamard vacuum state]] $\langle -\rangle \colon PolyObs(E_{\text{BV-BRST}})[ [\hbar, g] ] \to \mathbb{C}[ [\hbar,g] ]$.

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

* ([[algebraic adiabatic limit]]) On the other hand, it is equally unrealistic that an actual [[experiment]] _detects_ phenomena outside a given compact subset of spacetime. Realistic scattering [[experiments]] (such as the [[LHC]]) do not really prepare or measure [[plane waves]] filling all of [[spacetime]] as described by the [[scattering amplitudes]] (eq:ScatteringPlaneWaves). Any [[observable]] that is realistically measurable must have compact spacetime support. We see below in prop. \ref{IsomorphismFromChangeOfAdiabaticSwitching} that such [[interacting field observables]] with compact spacetime support may be computed without taking the [[adiabatic limit]]: It is sufficient to use any [[adiabatic switching]] which is constant on the support of the observable.

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
It is expected that this should be rectified by the proper [[interacting vacuum]] of [[QCD]] ([Rafelski 90, pages 12-16](confinement#Rafelski90)), which is possibly a "[[theta-vacuum]]" exhibiting [[superposition]] of [[instanton in QCD|QCD instantons]] ([Schäfer-Shuryak 98, section III.D](instanton+in+QCD#SchaeferShuryak98)). This remains open, closely related to the _[Millennium Problem](http://www.claymath.org/millennium-problems/yang%E2%80%93mills-and-mass-gap)_ of [[quantization of Yang-Mills theory]].

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

Here in [[causal perturbation theory]] no [[divergences]] in the [[coefficients]] of the [[formal power series]] are considered in the first place, all coefficients are well-defined, hence "finite". In this sense [[causal perturbation theory]] is about "finite" perturbative QFT, where instead of "re-normalization" of ill-defined expressions one just encounters "normalization" (prominently highlighted in [Scharf 95, see title, introduction, and section 4.3](causal+perturbation+theoryscatt#Scharf95)), namely compatible choices of these finite values. The actual "re-normalization" in the sense of "change of normalization" is expressed by the [[Stückelberg-Petermann renormalization group]].

This refers to those [[divergences]] that are known as _[[UV-divergences]]_, namely short-distance effects,
which are mathematically reflected in the fact that the perturbative [[S-matrix]] scheme (def. \ref{LagrangianFieldTheoryPerturbativeScattering})
is defined on _[[local observables]]_, which, by their very locality, encode point-[[interactions]].
See also remark \ref{AdiabaticLimit} on _[[infrared divergences]]_.

=--


+-- {: .num_remark #WorldlineFormalism}
###### Remark
**([[virtual particles]], [[worldline formalism]] and [[perturbative string theory]])**

It is suggestive to think of the [[edges]] in the [[Feynman diagrams]] (def. \ref{FeynmanDiagram}) as [[worldlines]] of "[[virtual particles]]" and of the [[vertices]] as the points where they collide and transmute. (Care must be exercised not to confuse this with concepts of real [[particles]].) With this interpretation prop. \ref{FeynmanDiagramAmplitude} may be read as saying that the [[scattering amplitude]] for given external [[source fields]] (remark \ref{FromAxiomaticSMatrixScatteringAmplitudes}) is the [[superposition]] of the [[Feynman amplitudes]] of all possible ways that these may interact; which is closely related to the intuition for the [[path integral]] (remark \ref{InterpretationOfPerturbativeSMatrix}).

This intuition is made precise by the _[[worldline formalism]]_ of [[perturbative quantum field theory]] ([Strassler 92](worldline+formalism#Strassler92)). This is the perspective on [[perturbative QFT]] which directly relates [[perturbative QFT]] to [[perturbative string theory]] ([Schmidt-Schubert 94](worldline+formalism#SchmidtSchubert94)). In fact the [[worldline formalism]] for [[perturbative QFT]] was originally found by taking thre point-particle limit of [[string scattering amplitudes]] ([Bern-Kosower 91](worldline+formalism#BernKosower91), [Bern-Kosower 92](worldline+formalism#BernKosower92)).

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
  LocObs(E_{\text{BV-BRST}})[ [\hbar, g,j] ]\langle g, j
  \rangle
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

#### Interacting field observables
 {#QuantumObservables}

We have seen that via [[Bogoliubov's formula]] (def. \ref{InteractingFieldObservables}) every perturbative [[S-matrix]] scheme (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) induces for every choice of [[adiabatic switching|adiabatically switched]]
[[interaction]] [[action functional]] $S_{int,sw} \coloneqq \tau_\Sigma( g_{sw} \mathbf{L}_{int} )$ a notion of [[perturbative QFT|perturbative]] [[interacting field observables]] (def. \ref{InteractingFieldObservables}). These generate an algebra (def. \ref{QuntumMollerOperator} below).
By [[Bogoliubov's formula]], in general this algebra depends on the choice of [[adiabatic switching]];
which however is not meant to be part of the [[physics]], but just a mathematical device for grasping global field structures locally.

But this spurious dependence  goes away (prop. \ref{IsomorphismFromChangeOfAdiabaticSwitching} below) when restricting attention to
observables whose spacetime support is inside a compact [[causally closed subsets]] $\mathcal{O}$ of spacetime (def. \ref{PerturbativeGeneratingLocalNetOfObservables} below). This is a sensible condition for an [[observable]] in [[physics]],
where any realistic [[experiment]] nessecarily probes only a compact subset of spacetime, see also remark \ref{AdiabaticLimit}.

The resulting system (a "[[co-presheaf]]") of well-defined perturbative [[interacting field algebras of observables]] (def. \ref{SystemOfAlgebrasOfQuantumObservables} below)

$$
  \mathcal{O} \mapsto IntObs(E_{\text{BV-BRST}}, \mathbf{L}_{int})(\mathcal{O})
$$

is in fact [[causal locality|causally local]] (prop. \ref{PerturbativeQuantumObservablesIsLocalnet} below).
This fact was presupposed without proof already in [Il'in-Slavnov 78](perturbative+algebraic+quantum+field+theory#IlinSlavnov78);
because this is one of two key properties that the [[Haag-Kastler axioms]] ([Haag-Kastler 64](Haag-Kastler+axioms#HaagKastler64)) demand of an intrinsically defined [[quantum field theory]]
(i.e. defined without necessarily making recourse to the geometric backdrop of [[Lagrangian field theory]]). The only other key property demanded by the [[Haag-Kastler axioms]]
is that the [[algebras of observables]] be [[C*-algebras]]; this however must be regarded as the axiom encoding
[[non-perturbative quantum field theory]] and hence is necessarily violated in the present context of [[perturbative QFT]].

Since quantum field theory following the full [[Haag-Kastler axioms]] is commonly known as _[[AQFT]]_, this perturbative version,
with [[causally local nets of observables]] but without the [[C*-algebra]]-condition on them, has come to be called
_[[perturbative AQFT]]_ ([Dütsch-Fredenhagen 01](perturbative+algebraic+quantum+field+theory#DuetschFredenhagen01),
[Fredenhagen-Rejzner 12](perturbative+algebraic+quantum+field+theory#FredenhagenRejzner12)).

In this terminology the content of prop. \ref{PerturbativeQuantumObservablesIsLocalnet} below is that
_while the input of [[causal perturbation theory]] is a [[gauge fixing|gauge fixed]] [[Lagrangian field theory]],
the output is a [[perturbative algebraic quantum field theory]]_:


$$
  \array{
    \array{
      \text{gauge-fixed}
      \\
      \text{Lagrangian}
      \\
      \text{field theory}
    }
    &
    \overset{
      \array{
        \text{causal}
        \\
        \text{perturbation theory}
        \\
      }
    }{\longrightarrow}&
    \array{
      \text{perturbative}
      \\
      \text{algebraic}
      \\
      \text{quantum}
      \\
      \text{field theory}
    }
    \\
    \underset{
      \array{
        \text{(Becchi-Rouet-Stora 76,}
        \\
        \text{Batalin-Vilkovisky 80s)}
      }
    }{\,}
    &
    \underset{
      \array{
        \text{(Bogoliubov-Shirkov 59,}
        \\
        \text{Epstein-Glaser 73)}
      }
    }{\,}
    &
    \underset{
    \array{
      \text{ (Il'in-Slavnov 78,  }
      \\
      \text{Brunetti-Fredenhagen 99,}
      \\
      \text{Dütsch-Fredenhagen 01)}
    }
    }{\,}
  }
$$


The independence of the [[causally local net]] of localized [[interacting field algebras of observables]]
$IntObs(E_{\text{BV-BRST}}, \mathbf{L}_{int} )(\mathcal{O})$ from the choice of [[adiabatic switching]]
implies a well-defined spacetime-global [[algebra of observables]] by forming the [[inductive limit]]

$$
  IntObs(E_{\text{BV-BRST}}, \mathbf{L}_{int})
    \;\coloneqq\;
  \underset{\underset{\mathcal{O}}{\longrightarrow}}{\lim}
  \left(
    {\, \atop \,}
    IntObs(E_{\text{BV-BRST}}, \mathbf{L}_{int})(\mathcal{O})
    {\, \atop \,}
  \right)
  \,.
$$

This is also called the _[[algebraic adiabatic limit]]_, defining the [[algebras of observables]] of [[perturbative QFT]]
"in the infrared". The only remaining step in the construction of a [[perturbative QFT]] that remains is then
to find an [[interacting vacuum state]]

$$
  \left\langle
    -
  \right\rangle_{int}
  \;\colon\;
  IntObs(E_{\text{BV-BRST}}, \mathbf{L}_{int})
   \longrightarrow
  \mathbb{C}[ [ \hbar, g] ]
$$

on the global [[interacting field algebra]] $Obs_{\mathbf{L}_{int}}$.
This is related to the actual _[[adiabatic limit]]_, and it is by and large an open problem, see remark \ref{AdiabaticLimit}.


$\,$


+-- {: .num_defn #QuntumMollerOperator}
###### Definition
**([[interacting field algebra of observables]] -- [[quantum Møller operator]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}, and let $g S_{int} \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ]$ be a [[local observable]] regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]]-[[action functional|functional]].


We write

$$
  LocIntObs_{\mathcal{S}}(E_{\text{BV-BRST}}, g S_{int})
  \;\coloneqq\;
  \left\{
    {\, \atop \,}
    A_{int} \;\vert\; A \in LocObs(E_{BV-BRST})[ [ \hbar, g ] ]
    {\, \atop \,}
  \right\}
    \hookrightarrow
  PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g] ]
$$

for the subspace of [[interacting field observables]] $A_{int}$ (def. \ref{InteractingFieldObservables}) corresponding to [[local observables]] $A$,
the _[[local interacting field observables]]_.

Furthermore we write

$$
  \array{
    LocObs(E_{\text{BV-BRST}})[ [ \hbar , g] ]
    &
    \underoverset
    {\simeq}
    {
      \phantom{A}\mathcal{R}^{-1}\phantom{A}
    }{\longrightarrow}
    &
    IntLocObs(E_{\text{BV-BRST}}, g S_{int})[ [ \hbar , g ] ]
    \\
    A
      &\mapsto&
    A_{int}
      \coloneqq
    \mathcal{S}(g S_{int})^{-1} T( \mathcal{S}(g S_{int}), A )
  }
$$

for the factorization of the function $A \mapsto A_{int}$ through its image, which, by remark \ref{PerturbativeSMatrixInverse},
is a [[linear isomorphism]] with [[inverse]]

$$
  \array{
    IntLocObs(E_{\text{BV-BRST}}, g S_{int})[ [ \hbar , g ] ]
    &
    \underoverset
    {\simeq}
    {
      \phantom{A}\mathcal{R}\phantom{A  }
    }{\longrightarrow}
    &
    LocObs(E_{\text{BV-BRST}})[ [ \hbar , g] ]
    \\
    A_{int}
      &\mapsto&
    A
      \coloneqq
    T\left(
      \mathcal{S}(-g S_{int})
      ,
      \left( \mathcal{S}(g S_{int}) A_{int} \right)
    \right)
  }
$$

This may be called the _[[quantum Møller operator]]_ ([Hawkins-Rejzner 16, (33)](perturbative+algebraic+quantum+field+theory#HawkinsRejzner16)).

Finally we write

$$
  \begin{aligned}
    IntObs(E_{\text{BV-BRST}}, S_{int})
    & \coloneqq
    \left\langle
    {\, \atop \,}
      IntLocObs(E_{\text{BV-BRST}})[ [ \hbar, g] ]
    {\, \atop \,}
    \right\rangle
    \\
    &
     \phantom{\coloneqq}
     \hookrightarrow
    PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ]
  \end{aligned}
$$

for the smallest subalgebra of the [[Wick algebra]] containing the [[interacting local observables]].
This is the _perturbative [[interacting field algebra of observables]]_.

=--

The definition of the [[interacting field algebra of observables]] from the data of a [[scattering matrix]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) via [[Bogoliubov's formula]] (def. \ref{InteractingFieldObservables}) is physically well-motivated, but is not immediately recognizable as the result of applying a systematic concept of [[quantization]] (such as [[formal deformation quantization]]) to the given [[Lagrangian field theory]]. The following
proposition \ref{InteractingFieldAlgebraOfObservablesIsFormalDeformationQuantization} says that this is nevertheless the case.
(The special case of this statement for [[free field theory]] is discussed at _[[Wick algebra]]_, see [this remark](Wick+algebra#WickAlgebraIsFormalDeformationQuantization)).

+-- {: .num_prop #InteractingFieldAlgebraOfObservablesIsFormalDeformationQuantization}
###### Proposition
**([[interacting field algebra of observables]] is [[formal deformation quantization]] of [[interacting field theory|interacting]] [[Lagrangian field theory]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, and let $g_{sw} \mathbf{L}_{int} \in \Omega^{p+1,0}_{\Sigma,cp}(E_{\text{BV-BRST}})[ [\hbar, g ] ]\langle g\rangle$ be an [[adiabatic switching|adiabatically switched]] [[interaction]] [[Lagrangian density]] with corresponding
[[action functional]] $g S_{int} \coloneqq \tau_\Sigma( g_{sw} \mathbf{L}_{int} )$.

Then, at least on [[regular polynomial observables]], the construction of perturbative [[interacting field algebras of observables]] in def. \ref{QuntumMollerOperator} is a [[formal deformation quantization]] of the [[interacting field theory|interacting]] [[Lagrangian field theory]]
$(E_{\text{BV-BRST}}, \mathbf{L}'  + g_{sw} \mathbf{L}_{int})$.

=--

([Hawkins-Rejzner 16, prop. 5.4](perturbative+algebraic+quantum+field+theory#HawkinsRejzner16), [Collini 16](#Collini16))


The following definition collects the system (a [[co-presheaf]]) of [[generating functions]] for [[interacting field observables]]
which are localized in spacetime as the spacetime localization region varies:

+-- {: .num_defn #PerturbativeGeneratingLocalNetOfObservables}
###### Definition
**(system of spacetime-localized [[generating functions]] for [[interacting field observables]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}, and let

$$
  \mathbf{L}_{int}
  \;\in\;
  \Omega^{p+1,0}_\Sigma(E_{\text{BV-BRST}})[ [ \hbar , g  ] ]
$$

be a [[Lagrangian density]], to be thought of as an [[interaction]], so that for $g_{sw} \in C^\infty_{sp}(\Sigma)\langle g \rangle$
an [[adiabatic switching]] the [[transgression of variational differential forms|transgression]]

$$
  S_{int,sw}
    \;\coloneqq\;
  \tau_\Sigma(g_{sw} \mathbf{L}_{int})
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]
$$

is a [[local observable]], to be thought of as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

For $\mathcal{O} \subset \Sigma$ a [[causally closed subset]] of [[spacetime]]
([this def.](A+first+idea+of+quantum+field+theory#CausalComplementOfSubsetOfLorentzianManifold))
and for $g_{sw} \in Cutoffs(\mathcal{O})$ an [[adiabatic switching]] function ([this def.](A+first+idea+of+quantum+field+theory#CutoffFunctions))
which is constant on a [[neighbourhood]] of $\mathcal{O}$, write

$$
  Gen(E_{\text{BV-BRST}}, S_{int,sw} )(\mathcal{O})
   \;\coloneqq\;
  \left\langle
    \mathcal{Z}_{S_{int,sw}}(j A)
    \;\vert\;
    A \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g] ]
    \,\text{with}\,
    supp(A) \subset \mathcal{O}
  \right\rangle
   \;\subset\;
  PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]
$$

for the smallest subalgebra of the [[Wick algebra]] which contains the
[[generating functions]] (def. \ref{SchemeGeneratingFunction})
with respect to $S_{int,sw}$ for all those [[local observables]] $A$ whose spacetime support is in $\mathcal{O}$.

Moreover, write

$$
  Gen(E_{\text{BV-BRST}}, \mathbf{L}_{int})(\mathcal{O})
    \;\subset\;
  \underset{g_{sw} \in Cutoffs(\mathcal{O})}{\prod}
  Gen(E_{\text{BV-BRST}}, S_{int,sw})(\mathcal{O})
$$

be the subalgebra of the [[Cartesian product]] of all these algebras as $g_{sw}$ ranges over cutoffs, which is generated by the
[[tuples]]

$$
  \mathcal{Z}_{\mathbf{L}_{int}}(A)
    \;\coloneqq\;
  \left(
    \mathcal{Z}_{S_{int,sw}}(j A)
  \right)_{g_{sw} \in Cutoffs(\mathcal{O})}
$$

for $A$ with $supp(A) \subset \mathcal{O}$.

We call $Gen(E_{\text{BV-BRST}}, \mathbf{L}_{int} )(\mathcal{O})$ the _algebra of [[generating functions]] for [[interacting field observables]] localized in $\mathcal{O}$_.

Finally, for $\mathcal{O}_1 \subset \mathcal{O}_2$ an inclusion of two [[causally closed subsets]], let

$$
  i_{\mathcal{O}_1, \mathcal{O}_2}
  \;\colon\;
  Gen(E_{\text{BV-BRST}}, \mathbf{L}_{int})(\mathcal{O}_1)
    \longrightarrow
  Gen(E_{\text{BV-BRST}}, \mathbf{L}_{int})(\mathcal{O}_2)
$$

be the algebra [[homomorphism]] which is given simply by restricting the index set of [[tuples]].

This construction defines a [[functor]]

$$
  Gen(E_{\text{BV-BRST}}, \mathbf{L}_{int})
    \;\colon\;
  CausClsdSubsets(\Sigma)
    \longrightarrow
  Algebras
$$

from the [[poset]] of [[causally closed subsets]] of [[spacetime]] to the [[category]] of [[algebras]].

> (extends to [[star algebras]] if scattering matrices are chosen unitary...)

=--

([Brunetti-Fredenhagen 99, (65)-(67)](#BrunettiFredenhagen99))

The key technical fact is the following:

+-- {: .num_prop #IsomorphismFromChangeOfAdiabaticSwitching}
###### Proposition
**(localized [[interacting field observables]] independent of [[adiabatic switching]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}, and let

$$
  \mathbf{L}_{int}
  \;\in\;
  \Omega^{p+1,0}_\Sigma(E_{\text{BV-BRST}})[ [ \hbar , g  ] ]
$$

be a [[Lagrangian density]], to be thought of as an [[interaction]], so that for $g_{sw} \in C^\infty_{sp}(\Sigma)\langle g \rangle$
an [[adiabatic switching]] the [[transgression of variational differential forms|transgression]]

$$
  g S_{int,sw} \;\coloneqq\; \tau_\Sigma(g_{sw} \mathbf{L}_{int})
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]
$$

is a [[local observable]], to be thought of as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

If two such [[adiabatic switchings]] $g_{sw,1}, g_{sw,2} \in C^\infty_{cp}(\Sigma)$ agree on a
[[causally closed subset]]

$$
  \mathcal{O} \;\subset\; \Sigma
$$

in that

$$
  g_{sw,1}\vert_{\mathcal{O}} = g_{sw,2}\vert_{\mathcal{O}}
$$

then there exists a [[microcausal polynomial observable]]

$$
  K \;\in\; PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j ] ]
$$

such that for every [[local observable]]

$$
  A \;\in\; LocObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ]
$$

with spacetime support in $\mathcal{O}$

$$
  supp(A) \;\subset\; \mathcal{O}
$$

the corresponding two [[generating functions]] (eq:GeneratingFunctionInducedFromSMatrix)
are related via [[conjugation]] by $K$:

$$
  \label{AdiabaticSwitchingRelationGeneratingFunctions}
  \mathcal{Z}_{S_{int,sw_2}}
  \left(
    j A
  \right)
  \;=\;
  K^{-1}
  \,
  \left(
    \mathcal{Z}_{S_{int,sw_1}}
    \left(
      j A
    \right)
  \right)
  \,
  K
  \,.
$$

In particular this means that for every choice of [[adiabatic switching]] $g_{sw} \in Cutoffs(\mathcal{O})$
the algebra $Gen_{S_{int,sw}}(\mathcal{O})$ of [[generating functions]] for [[interacting field observables]]
computed with $g_{sw}$ is canonically [[isomorphism|isomorphic]] to the
abstract algebra $Gen_{\mathbf{L}_{int}}(\mathcal{O})$  (def. \ref{PerturbativeGeneratingLocalNetOfObservables}),
by the evident map on generators:

$$
  \label{AbstractGeneratingFunctionAlgebraIsomorphicToAnyAdiabaticSwitching}
  \array{
    Gen(E_{\text{BV-BRST}}, \mathbf{L}_{int})(\mathcal{o})
      &\overset{\simeq}{\longrightarrow}&
    Gen(E_{\text{BV-BRST}}, S_{int,sw})(\mathcal{O})
    \\
    \left(
      \mathcal{Z}_{S_{int,sw'}}
    \right)_{g_{sw'} \in Cutoffs(\mathcal{O})}
    &\mapsto&
    \mathcal{Z}_{S_{int,sw}}
  }
  \,.
$$

=--

([Brunetti-Fredenhagen 99, prop. 8.1](#BrunettiFredenhagen99))

+-- {: .proof}
###### Proof

By causal closure of $\mathcal{O}$, [this lemma](A+first+idea+of+quantum+field+theory#CausalPartition)
says that there are [[bump functions]]

$$
  a, r \in C^\infty_{cp}(\Sigma)\langle g \rangle
$$

which decompose the difference of [[adiabatic switchings]]

$$
  g_{sw,2} - g_{sw,1} = a + r
$$

subject to the [[causal ordering]]

$$
  supp(a) \,{\vee\!\!\!\wedge}\, \mathcal{O} \,{\vee\!\!\!\wedge}\, supp(r)
  \,.
$$

With this the result follows from repeated use of [[causal additivity]] in its various equivalent
incarnations from prop. \ref{ZCausalAdditivity}:

$$
  \begin{aligned}
    & \mathcal{Z}_{g S_{int,sw_2}}(j A)
    \\
    & =
    \mathcal{Z}_{
      \left(
        \tau_\Sigma
        \left(
          g_{sw,2}
          \mathbf{L}_{int}
        \right)
      \right)
    }
    \left(
      j A
    \right)
    \\
    & =
    \mathcal{Z}_{
      \left(
        \tau_\Sigma
        \left(
          (g_{sw,1} + a + r)\mathbf{L}_{int}
        \right)
      \right)
    }
    \left(
      j A
    \right)
    \\
    & =
    \mathcal{Z}_{
      \left(
        g S_{int,sw_1}
        +
        \tau_\Sigma
        \left(
          r \mathbf{L}_{int}
        \right)
        +
        \tau_\Sigma
        \left(
          a \mathbf{L}_{int}
        \right)
      \right)
    }
    \left(
      j A
    \right)
    \\
    & =
    \mathcal{Z}_{
      \left(
        g S_{int,sw_1}
        +
        \tau_\Sigma
        \left(
          r \mathbf{L}_{int}
        \right)
      \right)
    }
    \left(
      j A
    \right)
    \\
    & =
    \mathcal{S}
    \left(
      g S_{int,sw_1}
      +
      \tau_\Sigma
      \left(
        r \mathbf{L}_{int}
      \right)
    \right)^{-1}
    \,
    \mathcal{S}
    \left(
      g S_{int,sw_1}
      +
      j A
      +
      \tau_\Sigma
      \left(
        r \mathbf{L}_{int}
      \right)
    \right)
    \\
    & =
    \mathcal{S}
    \left(
      g S_{int,sw_1}
      +
      \tau_\Sigma
      \left(
        r \mathbf{L}_{int}
      \right)
    \right)^{-1}
    \,
    \mathcal{S}
    \left(
      g S_{int,sw_1}
      +
      j A
    \right)
    \,
    \mathcal{S}
    \left(
      g S_{int,sw_1}
    \right)^{-1}
    \,
    \mathcal{S}
    \left(
      j A
      +
      \tau_\Sigma
      \left(
        r \mathbf{L}_{int}
      \right)
    \right)
    \\
    & =
    \mathcal{S}
    \left(
      g S_{int,sw_1}
      +
      \tau_\Sigma
      \left(
        r\mathbf{L}_{int}
      \right)
    \right)^{-1}
    \,
    \underset{
      = id
    }{
    \underbrace{
    \mathcal{S}
    \left(
      g S_{int,sw_1}
    \right)
    \,
    \mathcal{S}
    \left(
      g S_{int,sw_1}
    \right)^{-1}
    }
    }
    \,
    \mathcal{S}
    \left(
      g S_{int,sw_1}
      +
      j A
    \right)
    \,
    \mathcal{S}
    \left(
      g S_{int , sw_1}
    \right)^{-1}
    \,
    \mathcal{S}
    \left(
      j A
      +
      \tau_\Sigma
      \left(
        r \mathbf{L}_{int}
      \right)
    \right)
    \\
    & =
    \underset{
      K^{-1}
    }{
      \underbrace{
        \left(
          \mathcal{Z}_{
            g S_{int,sw_1}
          }
          \left(
            \tau_\Sigma
            \left(
              r \mathbf{L}_{int}
            \right)
          \right)
        \right)^{-1}
      }
    }
    \,

    \mathcal{Z}_{
      g S_{int,sw_1}
    }
    \left(
      j A
    \right)
    \,\,
    \underset{
      K
    }{
    \underbrace{
    \mathcal{Z}_{
      g S_{int,sw_1}
    }
    \left(
      \tau_\Sigma
      \left(
        r \mathbf{L}_{int}
      \right)
    \right)
    }}
  \end{aligned}
$$


This proves the existence of elements $K$ as claimed.

It is clear that conjugation induces an algebra homomorphism,
and since the map is a linear isomorphism on the space of generators,
it is an algebra isomorphism on the algebras being generated (eq:AbstractGeneratingFunctionAlgebraIsomorphicToAnyAdiabaticSwitching).

(While the elements $K$ in (eq:AdiabaticSwitchingRelationGeneratingFunctions) are far from being unique themselves,
equation (eq:AdiabaticSwitchingRelationGeneratingFunctions) says that the map on generators induced
by conjugation with $K$ is independent of this choice.)


=--


+-- {: .num_prop #GeneratingAlgebrasIsLocalNet}
###### Proposition
**(system of generating algebras is [[causally local net]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}, and let

$$
  \mathbf{L}_{int}
  \;\in\;
  \Omega^{p+1,0}_\Sigma(E_{\text{BV-BRST}})[ [ \hbar , g  ] ]
$$

be a [[Lagrangian density]], to be thought of as an [[interaction]].

Then the system

$$
  Gen(E_{\text{BV-BRST}}, \mathbf{L}_{int})
  \;\colon\;
  CausCldSubsets(\Sigma)
    \longrightarrow
  Algebra
$$

of localized [[generating functions]] for [[interacting field observables]] (def. \ref{PerturbativeGeneratingLocalNetOfObservables})
is a _[[causally local net]]_ in that it satisfies the following conditions:

1. (isotony) For every inclusion $\mathcal{O}_1 \subset \mathcal{O}_2$ of [[causally closed subsets]] of [[spacetime]]
   the corresponding algebra homomorphism is a [[monomorphism]]

   $$
     i_{\mathcal{O}_1, \mathcal{O}_2}
     \;\colon\;
     Gen(E_{\text{BV-BRST}}, \mathbf{L}_{int})(\mathcal{O}_1) \hookrightarrow Gen(E_{\text{BV-BRST}},\mathbf{L}_{int})(\mathcal{O}_2)
   $$

1. ([[causal locality]]) For $\mathcal{O}_1, \mathcal{O}_2 \subset X$ two [[causally closed subsets]]
   which are [[spacelike]] separated, in that their [[causal ordering]] ([this def.](A+first+idea+of+quantum+field+theory#CausalOrdering)) satisfies

   $$
     \mathcal{O}_1 {\vee\!\!\!\wedge} \mathcal{O}_2
       \;\text{and}\;
     \mathcal{O}_2 {\vee\!\!\!\wedge} \mathcal{O}_1
   $$

   and for $\mathcal{O} \subset \Sigma$ any further [[causally closed subset]] which contains both

   $$
     \mathcal{O}_1 , \mathcal{O}_2 \subset \mathcal{O}
   $$

   then the corresponding images of the generating function algebras of interacting field observables
   localized in  $\mathcal{O}_1$ and in $\mathcal{O}_2$,
   respectively, commute with each other as subalgebras of the generating function algebras of interacting
   field observables localized in $\mathcal{O}$:

   $$
     \left[
       i_{\mathcal{O}_1,\mathcal{O}}(Gen_{L_{int}}(\mathcal{O}_1))
       \;,\;
       i_{\mathcal{O}_2,\mathcal{O}}(Gen_{L_{int}}(\mathcal{O}_2))
     \right]
     \;=\;
     0
     \;\;\;
     \in Gen(E_{\text{BV-BRST}}, \mathbf{L}_{int})(\mathcal{O})
     \,.
   $$


=--

([D&#252;tsch-Fredenhagen 00, section 3](#DuetschFredenhagen00), following [Brunetti-Fredenhagen 99, section 8](#BrunettiFredenhagen99),
[Il'in-Slavnov 78](#IlinSlavnov78))

+-- {: .proof}
###### Proof

Isotony is immediate from the definition of the algebra homomorphisms in def. \ref{PerturbativeGeneratingLocalNetOfObservables}.

By the isomorphism (eq:AbstractGeneratingFunctionAlgebraIsomorphicToAnyAdiabaticSwitching) we may check causal localizy with respect to any
choice of [[adiabatic switching]] $g_{sw} \in Cautoff(\mathcal{O})$ constant over $\mathcal{O}$. For this
the statement follows, with the assumption of spacelike separation, by [[causal additivity]] (prop. \ref{ZCausalAdditivity}):

For $supp(A_1) \subset \mathcal{O}_1$ and $supp(A_2) \subset \mathcal{O}_2$ we have:

$$
  \begin{aligned}
    \mathcal{Z}_{g S_{int,sw}}( j A_1 )
    \mathcal{Z}_{g S_{int,sw}}( j A_2 )
    & =
    \mathcal{S}_{g S_{int,sw}}( j A_1 + j A_2)
    \\
    & =
    \mathcal{S}_{g S_{int,sw}}( j A_2 + j A_1)
    \\
    & =
    \mathcal{Z}_{g S_{int,sw}}( j A_2 )
    \mathcal{Z}_{g S_{int,sw}}( j A_1 )
  \end{aligned}
$$

=--

With the [[causally local net]] of localized [[generating functions]] for
[[interacting field observables]] in hand, it is now immediate to get the

+-- {: .num_defn #SystemOfAlgebrasOfQuantumObservables}
###### Definition
**(system of [[interacting field algebras of observables]])

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}, and let

$$
  \mathbf{L}_{int}
  \;\in\;
  \Omega^{p+1,0}_\Sigma(E_{\text{BV-BRST}})[ [ \hbar , g  ] ]
$$

be a [[Lagrangian density]], to be thought of as an [[interaction]], so that for $g_{sw} \in C^\infty_{sp}(\Sigma)\langle g \rangle$
an [[adiabatic switching]] the [[transgression of variational differential forms|transgression]]

$$
  g S_{int,sw} \;\coloneqq\; g \tau_\Sigma(g_{sw} \mathbf{L}_{int})
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ]\langle g \rangle
$$

is a [[local observable]], to be thought of as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

For $\mathcal{O} \subset \Sigma$ a [[causally closed subset]]
of [[spacetime]] ([this def.](A+first+idea+of+quantum+field+theory#CausalComplementOfSubsetOfLorentzianManifold))
and for $g_{sw} \in Cutoffs(\mathcal{O})$ an compatible [[adiabatic switching]] function (def. \ref{CutoffFunctions}) write

$$
  IntObs(E_{\text{BV-BRST}}, S_{int,sw})(\mathcal{O})
   \coloneqq
  \left\langle
     i \hbar \frac{d}{d j}
     \mathcal{Z}_{S_{int}}(j A)\vert_{j = 0} \;\vert\; supp(A) \subset \mathcal{O}
  \right\rangle
   \;\subset\;
  PolyObs((\hbar))[ [ g ] ]
$$

for the [[interacting field algebra of observables]] (def. \ref{QuntumMollerOperator}) with spacetime support in $\mathcal{O}$.

Let then

$$
  IntObs(E_{\text{BV-BRST}}, \mathbf{L}_{int})(\mathcal{O})
    \subset
  \underset{g_{sw} \in Cutoffs(\mathcal{O})}{\prod} IntObs(E_{\text{BV-BRST}}, S_{int,sw})(\mathcal{O})
$$

be the subalgebra of the [[Cartesian product]] of all these algebras as $g_{sw}$ ranges, which is generated by the
[[tuples]]

$$
   i \hbar
   \frac{d}{d j } \mathcal{Z}_{\mathbf{L}_{int}}\vert_{j = 0}
    \;\coloneqq\;
  \left(
      i \hbar
      \frac{d}{d j } \mathcal{Z}_{S_{int,sw}} (j A)\vert_{j  = 0}
  \right)_{g_{sw} \in Cutoffs(\mathcal{O})}
$$

for $supp(A) \subset \mathcal{O}$.

Finally, for $\mathcal{O}_1 \subset \mathcal{O}_2$ an inclusion of two [[causally closed subsets]], let

$$
  i_{\mathcal{O}_1, \mathcal{O}_2}
  \;\colon\;
  IntObs(E_{\text{BV-BRST}}, \mathbf{L}_{int})(\mathcal{O}_1)
    \longrightarrow
  IntObs(E_{\text{BV-BRST}}, \mathbf{L}_{int})(\mathcal{O}_2)
$$

be the algebra [[homomorphism]] which is given simply by restricting the index set of [[tuples]].

This construction defines a [[functor]]

$$
  IntObs(E_{\text{BV-BRST}}, \mathbf{L}_{int}) \;\colon\; CausClsdSubsets(\Sigma) \longrightarrow Algebras
$$

from the [[poset]] of [[causally closed subsets]] in the [[spacetime]] $\Sigma$ to the [[category]] of [[star algebras]].

=--

Finally, as a direct corollary of prop. \ref{GeneratingAlgebrasIsLocalNet}, we obtain the key result:

+-- {: .num_prop #PerturbativeQuantumObservablesIsLocalnet}
###### Proposition
**(system of [[interacting field algebras of observables]] is [[causally local net|causally local]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}, and let

$$
  \mathbf{L}_{int}
  \;\in\;
  \Omega^{p+1,0}_\Sigma(E_{\text{BV-BRST}})[ [ \hbar , g ] ]
  \,.
$$

be a [[Lagrangian density]], to be thought of as an [[interaction]],
then the system of [[algebras of observables]] $Obs_{L_{int}}$ (def. \ref{SystemOfAlgebrasOfQuantumObservables})
is a [[local net of observables]] in that

1. (isotony) For every inclusion $\mathcal{O}_1 \subset \mathcal{O}_2$ of [[causally closed subsets]]
   the corresponding algebra homomorphism is a [[monomorphism]]

   $$
     i_{\mathcal{O}_1, \mathcal{O}_2}
     \;\colon\;
     IntObs(E_{\text{BV-BRST}}, \mathbf{L}_{int})(\mathcal{O}_1) \hookrightarrow IntObs(E_{\text{BV-BRST}}, \mathbf{L}_{int})(\mathcal{O}_2)
   $$

1. ([[causal locality]]) For $\mathcal{O}_1, \mathcal{O}_2 \subset X$ two [[causally closed subsets]]
   which are [[spacelike]] separated, in that their [[causal ordering]] ([this def.](A+first+idea+of+quantum+field+theory#CausalOrdering)) satisfies

   $$
     \mathcal{O}_1 {\vee\!\!\!\wedge} \mathcal{O}_2
       \;\text{and}\;
     \mathcal{O}_2 {\vee\!\!\!\wedge} \mathcal{O}_1
   $$

   and for $\mathcal{O} \subset \Sigma$ any further causally closed subset which contains both

   $$
     \mathcal{O}_1 , \mathcal{O}_2 \subset \mathcal{O}
   $$

   then the corresponding images of the generating algebras of $\mathcal{O}_1$ and $\mathcal{O}_2$,
   respectively, commute with each other as subalgebras of the generating algebra of $\mathcal{O}$:

   $$
     \left[
       i_{\mathcal{O}_1,\mathcal{O}}(Obs_{\mathbf{L}_{int}}(\mathcal{O}_1))
       \;,\;
       i_{\mathcal{O}_2,\mathcal{O}}(Obs_{\mathbf{L}_{int}}(\mathcal{O}_2))
     \right]
     \;=\;
     0
     \;\;\;
     \in IntObs(E_{\text{BV-BRST}}, \mathbf{L}_{int})(\mathcal{O})
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
    & \left[
      i \hbar \frac{d}{d j} \mathcal{Z}_{S_{int,sw}}(j A_1)\vert_{j = 0}
      \;,\;
      i \hbar  \frac{d}{d j} \mathcal{Z}_{S_{int,sw}}(j J_2)\vert_{j = 0}
    \right]
    \\
    & =
     (i \hbar)^2
     \frac{
       \partial^2
     }{
       \partial j_1 \partial j_2
     }
     \underset{ = 0}{
     \underbrace{
    \left[
       \mathcal{Z}_{S_{int,sw}}(j_1 A_1)
      \;,\;
       \mathcal{Z}_{S_{int,sw}}(j_1 A_2)
    \right]}}_{ \left\vert  { {j_1 = 0} \atop {j_2 = 0} } \right. }
    \\
    & = 0
  \end{aligned}
$$

=--


$\,$


#### Time-ordered products
 {#TimeOrderedProducts}

Definition \ref{LagrangianFieldTheoryPerturbativeScattering} suggests to focus on the multilinear operations $T(...)$ which define the perturbative [[S-matrix]] order-by-order in $\hbar$. We impose [[axioms]] on these _[[time-ordered products]]_ directly (def. \ref{TimeOrderedProduct}) and then prove that these axioms imply the axioms for the corresponding [[S-matrix]] (prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix} below).


+-- {: .num_defn #TimeOrderedProduct}
###### Definition
**([[time-ordered products]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

A _[[time-ordered product]]_ is a sequence of [[multilinear map|multi-]][[linear continuous functionals]] for all $k \in \mathbb{N}$ of the form

$$
  T_k
    \;\colon\;
  \left(
    {\, \atop \,}
    LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]\langle g,j \rangle
    {\, \atop \,}
  \right)^{\otimes^k_{\mathbb{C}[ [\hbar, g, j] ]}}
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}((\hbar))[ [g , j] ]
$$

(from [[tensor products]] of [[local observables]] to [[microcausal polynomial observables]], with formal parameters adjoined
according to def. \ref{FormalParameters})
such that the following conditions hold for all possible arguments:

1. (normalization)

   $$
     T_0(O) = 1
   $$

1. (perturbation)

   $$
     T_1(O) =  :O:
   $$

1. (symmetry) each $T_k$ is symmetric in its arguments, in that for every [[permutation]]
   $\sigma \in \Sigma(k)$ of $k$ elements

   $$
     T_k(O_{\sigma(1)}, O_{\sigma(2)}, \cdots, O_{\sigma(k)})
     \;=\;
     T_k(O_1, O_2, \cdots, O_k)
   $$

1. ([[causal factorization]]) If the spacetime support ([this def.](A+first+idea+of+quantum+field+theory#SpacetimeSupport))
   of [[local observables]] satisfies the [[causal ordering]]

   $$
     \left(
       {\, \atop \,}
       supp(O_1)
         \cup
         \cdots
         \cup
       supp(O_r)
       {\, \atop \,}
     \right)
       \;{\vee\!\!\!\wedge}\;
     \left(
       {\, \atop \,}
       supp(O_{r+1})
         \cup
         \cdots
         \cup
       supp(O_k)
       {\, \atop \,}
     \right)
   $$

   then the time-ordered product of these $k$ arguments factors as
   the [[Wick algebra]]-product of the time-ordered product of the first $r$ and that of the second $k-r$ arguments:

   $$
     T(O_1, \cdots, O_k)
     \; = \;
     T( O_1,   \cdots , O_r )
     \,
     T( O_{r+1},   \cdots , O_k )
     \,.
   $$

=--

+-- {: .num_example #TimeOrderedProductsFromSMatrixScheme}
###### Example
**([[S-matrix]] scheme implies [[time-ordered products]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree} and let

$$
  \mathcal{S}
  \;=\;
  \underset{k \in \mathbb{N}}{\sum}
  \frac{1}{k!}\frac{1}{(i \hbar)^k}
  T_k
$$

be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}.

Then the $\{T_k\}_{k \in \mathbb{N}}$ are [[time-ordered products]] in the sense of def. \ref{TimeOrderedProduct}.

=--

+-- {: .proof}
###### Proof

We need to show that the $\{T_k\}_{k \in \mathbb{N}}$ satisfy [[causal factorization]].

For

$$
  O_j\;\in\; LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g,j\rangle
$$

a local observable, consider the continuous linear function that muliplies this by any [[real number]]

$$
  \array{
    \mathbb{R}
      &\longrightarrow&
    LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g,j\rangle
    \\
    \kappa_j &\mapsto& \kappa_j O_j
  }
  \,.
$$

Since the $T_k$ by definition are [[continuous linear functionals]], they are in particular
[[differentiable maps]], and hence so is the S-matrix $\mathcal{S}$. We may extract $T_k$ from
$\mathcal{S}$ by [[differentiation]] with respect to the parameters $\kappa_j$ at $\kappa_j = 0$:

$$
  T_k(O_1, \cdots, O_k)
  \;=\;
  (i \hbar)^k
  \frac{\partial^k}{
    \partial \kappa_1
    \cdots
    \partial \kappa_k
  }
  \mathcal{S}\left( \kappa_1 O_1 + \cdots + \kappa_k O_k \right)\vert_{\kappa_1, \cdots, \kappa_k = 0}
$$

for all $k \in \mathbb{N}$.

Now the [[causal additivity]] of the S-matrix $\mathcal{S}$ implies its [[causal factorization]] (remark \ref{DysonCausalFactorization})
and this implies the causal factorization of the $\{T_k\}$ by the [[product law]] of [[differentiation]]:

$$
  \begin{aligned}
    T_k(O_1, \cdots, O_k)
    & =
    (i \hbar)^k
    \frac{\partial^k}{
      \partial \kappa_1
      \cdots
      \partial \kappa_k
    }
    \mathcal{S}\left( \kappa_1 O_1 + \cdots + \kappa_k O_k \right)\vert_{\kappa_1, \cdots, \kappa_k = 0}
    \\
    & =
    (i \hbar)^k
    \frac{\partial^k}{
      \partial \kappa_1
      \cdots
      \partial \kappa_k
    }
    \left(
      {\, \atop \,}
      \mathcal{S}(\kappa_1 O_1 + \cdots + \kappa_r O_r)
      \,
      \mathcal{S}(\kappa_{r+1} O_{r+1} + \cdots + \kappa_k O_k)
      {\, \atop \,}
    \right)
    \vert_{\kappa_1, \cdots, \kappa_k = 0}
    \\
    & =
    (i \hbar)^r
    \frac{\partial^r}{
      \partial \kappa_1
      \cdots
      \partial \kappa_r
    }
    \mathcal{S}(\kappa_1 O_1 + \cdots + \kappa_r O_r)
    \vert_{\kappa_1, \cdots, \kappa_r = 0}
    \;
    (i \hbar)^{k-r}
    \frac{\partial^{k-r}}{
      \partial \kappa_{r+1}
      \cdots
      \partial \kappa_k
    }
    \mathcal{S}(\kappa_{r+1} O_{r+1} + \cdots + \kappa_k O_k)
    \vert_{\kappa_{r+1}, \cdots, \kappa_k = 0}
    \\
    & =
    T_{r}( O_1, \cdots, O_{r} )
    \,
    T_{k-r}( O_{r+1}, \cdots, O_{k} )
  \end{aligned}
  \,.
$$

=--

The converse implication, that [[time-ordered products]] induce an [[S-matrix]] scheme involves
more work (prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix} below).

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

In conclusion:

+-- {: .num_prop #CausalFactorizationAlreadyImpliesSMatrix}
###### Proposition
**([[S-matrix]] scheme via [[causal factorization]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree} and consider a function

$$
  \mathcal{S}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g,j \rangle
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g, j] ]
$$

from [[local observables]] to [[microcausal polynomial observables]] which satisfies the condition "perturbation"
from def. \ref{LagrangianFieldTheoryPerturbativeScattering}. Then the following two conditions
on $\mathcal{S}$ are equivalent

1. [[causal additivity]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering})

1. [[causal factorization]] (remark \ref{DysonCausalFactorization})

and hence either of them is necessary and sufficient for $\mathcal{S}$ to be a perturbative [[S-matrix]] scheme
according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}.

=--


+-- {: .proof}
###### Proof

That causal factorization follows from causal additivity is immediate (remark \ref{DysonCausalFactorization}).

Conversely, causal factorization of $\mathcal{S}$ implies that its expansion coefficients $\{T_k\}_{k \in \mathbb{N}}$
are [[time-ordered products]] (def. \ref{TimeOrderedProduct}), via the proof of example \ref{TimeOrderedProductsFromSMatrixScheme},
and this implies causal additivity by prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix}.

=--


#### ("Re"-)Normalization
 {#ExistenceAndRenormalization}

We discuss now that [[time-ordered products]] as in def. \ref{TimeOrderedProduct}, hence, by prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix}, perturbative [[S-matrix]] schemes (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) exist in fact uniquely away from coinciding interaction points (prop. \ref{TimeOrderedProductAwayFromDiagonal} below).

This means that the construction of full [[time-ordered products]]/[[S-matrix]] schemes may be phrased as an [[extension of distributions]] of time-ordered products to the [[diagonal]] locus of coinciding spacetime arguments (prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal} below).
This choice in their definition is called the choice of _[[renormalization|("re"-)normalization]]_ of the [[time-ordered products]] (remark \ref{CausalPerturbationTheoryAbsenceOfUVDivergences}), and hence of the [[interacting field theory|interacting]] [[pQFT]] that these define (def. \ref{ExtensionOfTimeOrderedProoductsRenormalization} below).

The space of these choices may be accurately characterized, it is a [[torsor]] over a [[group]] of re-definitions of the
[[interaction]]-terms, called the "[[Stückelberg-Petermann renormalization group]]". This is called the
_[[main theorem of perturbative renormalization]]_, theorem \ref{PerturbativeRenormalizationMainTheorem} below.

Here we discuss just enough of the ingredients needed to _state_ this theorem. For proof of theorem and
discussion of the various methods of picking [[renormalization|("re"-)normalizations]] see [[renormalization|there]].

$\,$

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
  \text{for} \, i \neq j \in \{1, \cdots, k\}
  \,.
$$

=--

+-- {: .num_prop #TimeOrderedProductAwayFromDiagonal}
###### Proposition
**([[time-ordered product]] unique away from coinciding spacetime arguments)**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, and let $T = \{T_k\}_{k \in \mathbb{N}}$ be a sequence of [[time-ordered products]] (def. \ref{TimeOrderedProduct})

$$
  \array{
    \left(
      {\, \atop \,}
      LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]
      {\, \atop \,}
    \right)^{\otimes^k_{\mathbb{C}[ [\hbar, g, j] ]}}
      & \longrightarrow &
    PolyObs(E_{\text{BV-BRST}})_{reg}((\hbar))[ [g , j] ]
    \\
    \uparrow & \nearrow_{(-) \star_F \cdots \star_F (-)}
    \\
    \left(
      {\, \atop \,}
      LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]
      {\, \atop \,}
    \right)^{\otimes^k_{\mathbb{C}[ [\hbar, g, j] ]}}_{pds}
  }
$$

Then their [[restriction]] to the subspace of [[tuples]] of [[local observables]] of pairwise disjoint spacetime support (def. \ref{TuplesOfCompactlySupportedPolynomialLocalFunctionalsWithPairwiseDisjointSupport}) is unique (independent of the [[renormalization|"re-"normalization]] freedom in choosing $T$) and is given by the [[star product]]

$$
  A_1 \star_{F} A_2
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
    A_1 , \cdots, A_k
    {\, \atop \,}
  \right)
  \;=\;
  A_1
    \star_F
    \cdots
    \star_F
  A_k
  \,.
$$

In particular the time-ordered product extends from the restricted domain of tensor products of local observables to a restricted domain of [[microcausal polynomial observables]], where it becomes an [[associativity|associative]] product:

$$
  \label{RestrictedTimeOrderedProductAssociative}
  \begin{aligned}
    T(A_1, \cdots, A_{k_n})
    & =
    T(A_1, \cdots, A_{k_1})
      \star_F
    T(A_{k_1 + 1}, \cdots, A_{k_2})
      \star_F
      \cdots
      \star_F
    T(A_{k_{n-1} + 1}, \cdots, A_{k_n})
    \\
    & =
    A_1 \star_F \cdots \star_F A_{k_n}
  \end{aligned}
$$

for all tuples of local observables $A_1, \cdots, A_{k_1}, A_{k_1+1}, \cdots, A_{k_2}, \cdots, \cdots A_{k_n}$ with pairwise disjoint spacetime support.

=--

The idea of this statement goes back at least to [Epstein-Glaser 73](#EpsteinGlaser73), as in remark \ref{TheTraditionalErrorThatLeadsToTheNotoriouDivergencies}. One formulation appears as ([Brunetti-Fredenhagen 00, theorem 4.3](perturbative+algebraic+quantum+field+theory#BrunettiFredenhagen00)). The above formulation in terms of the [[star product]] is stated in ([Fredenhagen-Rejzner 12, p. 27](perturbative+algebraic+quantum+field+theory#FredenhagenRejzner12), [Dütsch 18, lemma 3.63 (b)](perturbative+algebraic+quantum+field+theory#Duetsch18)).

+-- {: .proof}
###### Proof

By [[induction]] over the number of arguments, it is sufficient to see that, more generally, for $A_1, A_2 \in PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]$ two [[microcausal polynomial observables]] with disjoint spacetime support the star product $A_1 \star_F A_2$ is well-defined and satisfies causal factorization.

Consider two [[partitions of unity]]

$$
  (\chi_{1,i} \in C^\infty_{cp}(\Sigma))_{i}
  \phantom{AAA}
  (\chi_{1,j} \in C^\infty_{cp}(\Sigma))_{j}
$$

and write $(A_{1,i})_i$ and $(A_{2,j})_{j}$ for the collection of [[microcausal polynomial observables]] obtained by multiplying all the [[distribution|distributional]] [[coefficients]] of $A_1$ and of $A_2$ with $\chi_{1,i}$ and with $\chi_{2,j}$, respectively, for all $i$ and $j$, hence such that

$$
  A_1 \;=\; \underset{i}{\sum} A_{1,i}
  \phantom{AAA}
  A_2 \;=\; \underset{j}{\sum} A_{1,j}
  \,.
$$

By linearity, it is sufficient to prove that $A_{1,i} \star_F A_{2,j}$ is well defined for all $i,j$ and satisfies causal factorization.

Since the spacetime supports of $A_1$ and $A_2$ are assumed to be disjoint

$$
  supp(A_1) \cap supp(A_2) \;=\; \emptyset
$$

we may find partitions such that each resulting pair of smaller supports is in fact in [[causal order]]-relation:

$$
  \array{
    \left(
      supp(A_1) \cap supp(\chi_{1,i})
    \right)
       {\vee\!\!\!\wedge}
    \left(
      supp(A_2) \cap supp(\chi_{2,j})
    \right)
    \\
    \text{or}
    \\
    \left(
      supp(A_2) \cap supp(\chi_{2,j})
    \right)
       {\vee\!\!\!\wedge}
    \left(
      supp(A_1) \cap supp(\chi_{1,u})
    \right)
  }
  \phantom{AAAAA}
  \text{for all}\,\, i,j
  \,.
$$

But now it follows as in the proof of [this prop.](Wick+algebra#CausalOrderingTimeOrderedProductOnRegular) (via [this equation](Wick+algebra#eq:CausallyOrderedWickProductViaFeynmanPropagator)) that

$$
  A_{1,i}
   \star_F
  A_{2,j}
  \;=\;
  \left\{
    \array{
      A_{1,i} \star_H A_{2,j} &\vert& supp(A_{1,i}) {\vee\!\!\!\wedge} supp(A_{2,j})
      \\
      A_{2,j} \star_H A_{1,i} &\vert& supp(A_{2,j}) {\vee\!\!\!\wedge} supp(A_{1,i})
  }
  \right.
$$


Finally the [[associativity]]-statement follows as in [this prop.](star+product#AssociativeAndUnitalStarProduct).


=--

Before using the unqueness of the [[time-ordered products]] away from coinciding spacetime arguments (prop. \ref{TimeOrderedProductAwayFromDiagonal}) to characterize the freedom in [[renormalization|("re"-)normalizing]] [[time-ordered products]], we pause to observe that in the same vein the [[time-ordered products]] have a unique extension of their domain also to [[regular polynomial observables]]. This is in itself a trivial statement (since all [[star products]] are defined on [[regular polynomial observables]], [this def.](star+product#PropagatorStarProduct)) but for understanding the behaviour under [[renormalization|("re"-)normalization]] of other structures, such as the interacting [[BV-differential]] (def. \ref{BVDifferentialInteractingQuantum} below) it is useful to understand renormalization as a process that starts extending awa from [[regular polynomial observables]].




By prop. \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}, on [[regular polynomial observables]] the
[[S-matrix]] is given as follows:

+-- {: .num_defn #OnRegularObservablesPerturbativeSMatrix}
###### Definition
**([[perturbative S-matrix]] on [[regular polynomial observables]])**


Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

Recall that the _[[time-ordered product]] on [[regular polynomial observables]]_
is the [[star product]] $\star_F$ induced by the [[Feynman propagator]] ([this. def.](Wick+algebra#OnRegularPolynomialObservablesTimeOrderedProduct)) and that, due to the [[non-singular distribution|non-singular]]
nature of [[regular polynomial observables]], this is given by [[conjugation]] of the pointwise product ([this equation](A+first+idea+of+quantum+field+theory#eq:ObservablesPointwiseProduct)) with $\mathcal{T}$ ([this equation](Wick+algebra#eq:OnRegularPolynomialObservablesPointwiseTimeOrderedIsomorphism)) as

$$
  T(A_1, A_2)
  \;=\;
  A_1 \star_F A_2
  \;=\;
  \mathcal{T}( \mathcal{T}^{-1}(A_1) \cdot \mathcal{T}^{-1}(A_2))
$$

([this prop.](Wick+algebra#IsomorphismOnRegularPolynomialObservablesTimeOrderedandPointwise)).

We say that the _[[perturbative S-matrix]] scheme_ on [[regular polynomial observables]]
is the [[exponential]] with respect to $\star_F$:

$$
  \mathcal{S}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar, g , j] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}((\hbar))[ [ g, j] ]
$$

given by

$$
  \mathcal{S}(S_{int})
  =
  \exp_{\star_F}
  \left(
    \tfrac{1}{i \hbar} S_{int})
  \right)
  \coloneqq
  1
    +
  \tfrac{1}{\i \hbar} S_{int}
    +
  \tfrac{1}{2}
  \tfrac{1}{(i \hbar)^2}
  S_{int} \star_F S_{int}
  +
  \cdots
  \,.
$$

We think of $S_{int}$ here as an [[adiabatic switching|adiabatically switched]] non-point-[[interaction]] [[action functional]].

We write $\mathcal{S}(S_{int})^{-1}$ for the [[inverse]] with respect to the [[Wick algebra|Wick product]] (which exists by [this remark](S-matrix#PerturbativeSMatrixInverse))

$$
  \mathcal{S}(S_{int})^{-1} \star_H \mathcal{S}(S_{int})
  =
  1
  \,.
$$

Notice that this is in general different form the inverse with respect to the [[time-ordered product]] $\star_F$, which is $\mathcal{S}(-S_{int})$:

$$
  \mathcal{S}(-S_{int})
    \star_F
  \mathcal{S}(S_{int})
  =
  1
  \,.
$$

=--

Similarly, by def. \ref{QuntumMollerOperator}, on [[regular polynomial observables]] the [[quantum Møller operator]] is given as follows:

+-- {: .num_defn #MollerOperatorOnRegularPolynomialObservables}
###### Definition
**([[quantum Møller operator]] on [[regular polynomial observables]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.
Given an [[adiabatic switching|adiabatically switched]] non-point-[[interaction]] [[action functional]] in the form of a [[regular polynomial observable]] of degree 0

$$
  S_{int}
  \;\in\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar , g, j] ]
$$

then the corresponding _[[quantum Møller operator]]_ on [[regular polynomial observables]]

$$
  \mathcal{R}^{-1}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar , g, j] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar, g, j] ]
$$

is given by the [[derivative]] of [[Bogoliubov's formula]]

$$
  \mathcal{R}^{-1}
    \;\coloneqq\;
  \mathcal{S}(S_{int})^{-1}
    \star_H
  (\mathcal{S}(S_{int}) \star_F (-))
  \,,
$$

where $\mathcal{S}(S_{int}) = \exp_{\mathcal{T}}\left( \tfrac{-1}{i \hbar} S_{int} \right)$ is the [[perturbative S-matrix]] from  def. \ref{OnRegularObservablesPerturbativeSMatrix}.

This indeed lands in [[formal power series]] in [[Planck's constant]] $\hbar$ (by [this remark](Bogoliubov's+formula#PowersInPlancksConstant)),  instead of in more general [[Laurent series]] as the [[perturbative S-matrix]] does (def. \ref{OnRegularObservablesPerturbativeSMatrix}).

Hence the inverse map is

$$
  \mathcal{R}
   \;=\;
  \mathcal{S}(-S_{int}) \star_F ( \mathcal{S}(S_{int}) \star(-) )
  \,.
$$

=--

([Bogoliubov-Shirkov 59](Bogoliubov's+formula#BogoliubovShirkov59); the above terminology follows [Hawkins-Rejzner 16, below def. 5.1](Møller+operator#HawkinsRejzner16))

(Beware that compared to Fredenhagen, Rejzner et. al. we change notation conventions $\mathcal{R} \leftrightarrow \mathcal{R}^{-1}$ in order to bring out the analogy to (the conventions for the) [[time-ordered product]]  $A_1 \star_F A_2 = \mathcal{T}(\mathcal{T}^{-1}(A_1) \cdot \mathcal{T}^{-1}(A_2))$ on regular polynomial observables.)

Still by def. \ref{QuntumMollerOperator}, on [[regular polynomial observables]] the [[interacting field algebra of observables]] is given as follows:


+-- {: .num_defn #FieldAlgebraObservablesInteracting}
###### Definition
**([[interacting field algebra]] [[structure]] on [[regular polynomial observables]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}. Given an [[adiabatic switching|adiabatically switched]] non-point-[[interaction]] [[action functional]] in the form of a [[regular polynomial observable]] in degree 0

$$
  S_{int}
  \;\in\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar, g, j] ]
  \,,
$$

then the _[[interacting field algebra]]_ [[structure]] on [[regular polynomial observables]]

$$
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar, g, j] ]
    \otimes
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar, g, h] ]
    \overset{ \star_{int} }{\longrightarrow}
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar, g, j] ]
$$

is the [[conjugation]] of the [[Wick algebra]]-[[structure]] by the [[quantum Møller operator]] (def. \ref{MollerOperatorOnRegularPolynomialObservables}):

$$
  A_1 \star_{int} A_2
  \;\coloneqq\;
  \mathcal{R}
  \left(
    \mathcal{R}^{-1}(A_1)
     \star_H
    \mathcal{R}^{-1}(A_2)
  \right)
$$

=--

(e.g. [Fredenhagen-Rejzner 11b, (19)](quantum+master+equation#FredenhagenRejzner11b))


Notice the following dependencies of these defnitions, which we leave notationally implicit:

| [[endomorphism]] of <br/> [[regular polynomial observables]] | meaning | depends on choice of |
|--------|---------|----------------------|
| $\phantom{AA}\mathcal{T}$ | [[time-ordered product|time-ordering]] | [[free field theory|free]] [[Lagrangian density]] and [[Wightman propagator]] |
| $\phantom{AA}\mathcal{S}$ | [[S-matrix]] | [[free field theory|free]] [[Lagrangian density]] and [[Wightman propagator]] |
| $\phantom{AA}\mathcal{R}$ | [[quantum Møller operator]] | [[free field theory|free]] [[Lagrangian density]] and [[Wightman propagator]] and [[interaction]] |


$\,$

After having discussed the uniqueness of the [[time-ordered products]] away from coinciding spacetime arguments (prop. \ref{TimeOrderedProductAwayFromDiagonal}) we now phrase and then discuss the freedom in defining these products at coinciding arguments, thus [[renormalization|("re"-)normalizing]] them.

+-- {: .num_defn #ExtensionOfTimeOrderedProoductsRenormalization}
###### Definition
**([[Epstein-Glaser renormalization|Epstein-Glaser ("re"-)normalization]] of [[perturbative QFT]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

Prop. \ref{TimeOrderedProductAwayFromDiagonal} implies that the
problem of constructing a sequence of [[time-ordered products]] (def. \ref{TimeOrderedProduct}), hence, by prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix}, an [[S-matrix]] scheme (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) for [[perturbative quantum field theory]] around the given [[free field]] [[vacuum]], is equivalently a problem of a sequence of compatible _[[extensions of distributions]]_ of the [[star products]] $\underset{k \; \text{arguments}}{\underbrace{(-)\star_F \cdots \star_F (-)}}$ of the [[Feynman propagator]] on $k$ arguments from the [[complement]] of coinciding [[events]] inside the [[Cartesian products]] $\Sigma^k$ of [[spacetime]] $\Sigma$, along the canonical inclusion

$$
  \Sigma^k \setminus \left\{ (x_i) \,\vert\, \underset{i \neq j}{\exists} (x_i = x_j) \right\}
    \overset{\phantom{AAA}}{\hookrightarrow}
  \Sigma^k
  \,.
$$

Via the [[associativity]] (eq:RestrictedTimeOrderedProductAssociative) of the restricted [[time-ordered product]] thesese choices are naturally made by [[induction]] over $k$, choosing the $(k+1)$-ary [[time-ordered product]] $T_{k+1}$ as an [[extension of distributions]] of $T_k(\underset{k \, \text{args}}{\underbrace{-, \cdots, -}}) \star_F (-)$.

This [[induction|inductive]] choice of [[extension of distributions]] of the [[time-ordered product]] to coinciding interaction points deserves to be called a choice of _normalization_ of the [[time-ordered product]] (e.g. [Scharf 94, section 4.3](#Scharf95)), but for historical reasons (see remark \ref{TheTraditionalErrorThatLeadsToTheNotoriouDivergencies} and remark \ref{CausalPerturbationTheoryAbsenceOfUVDivergences}) it is known as _[[renormalization|re-normalization]]_. Specifically the inductive construction by extension to coinciding interaction points is known as _[[Epstein-Glaser renormalization]]_.

=--

In ([Epstein-Glaser 73](#EpsteinGlaser73)) this is phrased in terms of splitting of distributions. In ([Brunetti-Fredenhagen 00, sections 4 and 7](perturbative+algebraic+quantum+field+theory#BrunettiFredenhagen00)) the perspective via [[extension of distributions]] is introduced, following ([Stora 93](perturbative+algebraic+quantum+field+theory#Stora93)). Review is in ([Dütsch 18, section 3.3.2](perturbative+algebraic+quantum+field+theory#Duetsch18)).

Proposition \ref{TimeOrderedProductAwayFromDiagonal} already shows that the freedom in choosing the [[renormalization|("re"-)normalization]] of [[time-ordered products]] is at most that of [[extensions of distributions|extending]] them to the "fat diagonal", where at least one pair of interaction points coincides. The following proposition \ref{RenormalizationIsInductivelyExtensionToDiagonal} says that when making these choices [[induction|inductively]] in the arity of the [[time-ordered products]] as in def. \ref{ExtensionOfTimeOrderedProoductsRenormalization} then the available choice of [[renormalization|("re"-)normalization)]] at each stage is in fact only that of extension to the actual [[diagonal]], where _all_ interaction points coincide:


+-- {: .num_prop #RenormalizationIsInductivelyExtensionToDiagonal}
###### Proposition
**([[renormalization|("re"-)normalization]] is [[induction|inductive]] [[extension of distributions|extension]] of [[time-ordered products]] to [[diagonal]])**


Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

Assume that for $n \in \mathbb{N}$, [[time-ordered products]]
$\{T_{k}\}_{k \leq n}$ of arity $k \leq n$ have been constructed
in the sense of def. \ref{TimeOrderedProduct}.
Then the time-ordered product $T_{n+1}$ of arity $n+1$ is uniquely fixed on the [[complement]]

$$
  \Sigma^{n+1} \setminus diag(n)
  \;=\;
  \left\{
     (x_i \in \Sigma)_{i = 1}^n
     \;\vert\;
     \underset{i,j}{\exists} (x_i \neq x_j)
  \right\}
$$

of the [[image]] of the [[diagonal]] inclusion $\Sigma \overset{diag}{\longrightarrow} \Sigma^{n}$
(where we regarded $T_{n+1}$ as a [[generalized function]] on $\Sigma^{n+1}$ according to remark \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}).

=--

This statement appears in ([Popineau-Stora 82](renormalization#PopineauStora82)), with (unpublished) details in ([Stora 93](renormalization#Stora93)), following personal communication by [[Henri Epstein]] (according to [Dütsch 18, footnote 57](#Duetsch18)). Following this, statement and detailed proof appeared in ([Brunetti-Fredenhagen 99](#BrunettiFredenhagen99)).


+-- {: .proof}
###### Proof

We will construct an [[open cover]] of $\Sigma^{n+1} \setminus \Sigma$ by subsets $\mathcal{C}_I \subset \Sigma^{n+1}$ which are [[disjoint unions]]
of [[inhabited set|non-empty]] sets that are in [[causal order]], so that by [[causal factorization]] the
time-ordered products $T_{n+1}$ on these subsets are uniquely given by $T_{k}(-) \star_H T_{n-k}(-)$.
Then we show that these unique products on these special subsets do coincide on [[intersections]].
This yields the claim by a [[partition of unity]].

We now say this in detail:

For $I \subset \{1, \cdots, n+1\}$  write $\overline{I} \coloneqq \{1, \cdots, n+1\} \setminus I$.
For $I, \overline{I} \neq \emptyset$, define the subset

$$
  \mathcal{C}_I
  \;\coloneqq\;
  \left\{
    (x_i)_{i \in \{1, \cdots, n+1\}} \in \Sigma^{n+1}
    \;\vert\;
    \{x_i\}_{i \in I} {\vee\!\!\!\wedge} \{x_j\}_{j \in \{1, \cdots, n+1\} \setminus I}
  \right\}
  \;\subset\;
  \Sigma^{n+1}
  \,.
$$

Since the [[causal order]]-relation involves the [[closed future cones]]/[[closed past cones]], respectively, it is clear that these are [[open subsets]]. Moreover it is immediate that they form an [[open cover]] of the [[complement]] of the [[diagonal]]:

$$
  \underset{ { I \subset \{1, \cdots, n+1\} \atop { I, \overline{I} \neq \emptyset } }   }{\cup}
  \mathcal{C}_I
  \;=\;
  \Sigma^{n+1} \setminus diag(\Sigma)
  \,.
$$

(Because any two distinct points in the [[globally hyperbolic spacetime]] $\Sigma$ may be causally separated by a [[Cauchy surface]],
and any such may be deformed a little such as not to intersect any of a given finite set of points. )

Hence the condition of [[causal factorization]] on $T_{n+1}$ implies that
[[restriction of distributions|restricted]] to any $\mathcal{C}_{I}$ these have to be given (in the condensed [[generalized function]]-notation from remark \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions} on
any unordered tuple $\mathbf{X} = \{x_1, \cdots, x_{n+1}\} \in \mathcal{C}_I$ with corresponding induced tuples
$\mathbf{I} \coloneqq \{x_i\}_{i \in I}$ and $\overline{\mathbf{I}} \coloneqq \{x_i\}_{i \in \overline{I}}$ by

$$
  \label{InductiveIdentificationOfTimeOrderedProductAwayFromDiagonal}
  T_{n+1}( \mathbf{X} )
  \;=\;
  T(\mathbf{I}) T(\overline{\mathbf{I}})
  \phantom{AA}
  \text{for}
  \phantom{A}
  \mathcal{X} \in \mathcal{C}_I
  \,.
$$

This shows that $T_{n+1}$ is unique on $\Sigma^{n+1} \setminus diag(\Sigma)$ if it exists at all,
hence if these local identifications glue to a global definition of $T_{n+1}$. To see that this is the case,
we have to consider any two such subsets

$$
  I_1, I_2
  \subset
  \{1, \cdots, n+1\}
  \,,
  \phantom{AA}
  I_1, I_2, \overline{I_1}, \overline{I_2} \neq \emptyset
  \,.
$$

By definition this implies that for

$$
  \mathbf{X} \in \mathcal{C}_{I_1} \cap \mathcal{C}_{I_2}
$$

a tuple of spacetime points which decomposes into causal order with respect to both these subsets,
the corresponding mixed intersections of tuples  are spacelike separated:

$$
  \mathbf{I}_1 \cap \overline{\mathbf{I}_2}
    \;
    {\gt\!\!\!\!\lt}
    \;
  \overline{\mathbf{I}_1} \cap \mathbf{I}_2
  \,.
$$

By the assumption that the $\{T_k\}_{k \neq n}$ satisfy causal factorization, this implies that the corresponding
time-ordered products commute:

$$
  \label{TimeOrderedProductsOfMixedIntersectionsCommute}
  T(\mathbf{I}_1 \cap \overline{\mathbf{I}_2})
  \,
  T(\overline{\mathbf{I}_1} \cap \mathbf{I}_2)
  \;=\;
  T(\overline{\mathbf{I}_1} \cap \mathbf{I}_2)
  \,
  T(\mathbf{I}_1 \cap \overline{\mathbf{I}_2})
  \,.
$$

Using this we find that the identifications of $T_{n+1}$
on $\mathcal{C}_{I_1}$ and on $\mathcal{C}_{I_2}$, accrding to (eq:InductiveIdentificationOfTimeOrderedProductAwayFromDiagonal),
agree on the intersection: in that for $  \mathbf{X}  \in \mathcal{C}_{I_1} \cap \mathcal{C}_{I_2}$ we have

$$
  \begin{aligned}
    T( \mathbf{I}_1 ) T( \overline{\mathbf{I}_1} )
    & =
    T( \mathbf{I}_1 \cap \mathbf{I}_2 )
    T( \mathbf{I}_1 \cap \overline{\mathbf{I}_2} )
    \,
    T( \overline{\mathbf{I}_1} \cap \mathbf{I}_2 )
    T( \overline{\mathbf{I}_1} \cap \overline{\mathbf{I}_2} )
    \\
    & =
    T( \mathbf{I}_1 \cap \mathbf{I}_2 )
    \underbrace{
    T( \overline{\mathbf{I}_1} \cap \mathbf{I}_2 )
    T( \mathbf{I}_1 \cap \overline{\mathbf{I}_2} )
    }
    T( \overline{\mathbf{I}_1} \cap \overline{\mathbf{I}_2} )
    \\
    & =
    T( \mathbf{I}_2 )
    T( \overline{\mathbf{I}_2} )
  \end{aligned}
$$

Here in the first step we expanded out the two factors using (eq:InductiveIdentificationOfTimeOrderedProductAwayFromDiagonal) for $I_2$,
then under the brace we used (eq:TimeOrderedProductsOfMixedIntersectionsCommute) and in the last step we used again
(eq:InductiveIdentificationOfTimeOrderedProductAwayFromDiagonal), but now for $I_1$.

To conclude, let

$$
  \left(
    \chi_I
    \in
    C^\infty_{cp}(\Sigma^{n+1})
  \right)_{ { I \subset \{1, \cdots, n+1\} } \atop { I, \overline{I} \neq \emptyset } }
$$

be a [[partition of unity]] subordinate to the [[open cover]] formed by the $\mathcal{C}_I$. Then the above implies that
setting for any $\mathbf{X} \in \Sigma^{n+1} \setminus diag(\Sigma)$

$$
  T_{n+1}(\mathbf{X})
  \;\coloneqq\;
  \underset{
    { I \in \{1, \cdots, n+1\} }
    \atop
    { I, \overline{I} \neq \emptyset }
  }{\sum}
  \chi_i(\mathbf{X}) T( \mathbf{I} ) T( \overline{\mathbf{I}} )
$$

is well defined and satisfies causal factorization.

=--

Since [[renormalization|("re"-)normalization]] involves making choices, there is the freedom to impose
further conditions that one may want to have satisfied. These are called _[[renormalization conditions]]_.

+-- {: .num_defn #RenormalizationConditions}
###### Definition
**([[renormalization conditions]], [[protection from quantum corrections]] and [[quantum anomalies]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

Then a condition $P$ on $k$-ary functions of the form

$$
  T_k
    \;\colon\;
  \left(
    {\, \atop \,}
    LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]
    {\, \atop \,}
  \right)^{\otimes^k_{\mathbb{C}[ [\hbar, g, j] ]}}
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}((\hbar))[ [g , j] ]
$$

is called a _renormalization condition_ if

1. it holds for the unique [[time-ordered products]] away from coinciding spacetime arguments (according to prop. \ref{TimeOrderedProductAwayFromDiagonal});

1. whenever it holds for all unrestricted $T_{k \leq n}$ for some $n \in \mathbb{N}$, then it also holds
   for $T_{n+1}$ restricted away from the diagonal:

   $$
     P(T_k)_{k \leq n}
     \;\Rightarrow\;
     P\left(
       T_{n+1}\vert_{\Sigma^{n+1} \setminus diag(\Sigma)}
     \right)
     \,.
   $$

This means that a renormalization condition is a condition that may consistently be imposed degreewise
in an [[induction|inductive]] construction of [[time-ordered products]] by degreewise [[extension of distributions|extension]]
to the [[diagonal]], according to prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal}.

If specified renormalization conditions $\{P_i\}$ completely remove any freedom in the choice of time-ordered products for a given [[quantum observable]], one says that the renormalization conditions _[[protection from quantum corrections|protects the observable against quantum corrections]]_. 

If for specified renormalization conditions $\{P_i\}$ there is _no_ choice of [[time-ordered products]] $\{T_k\}_{k \in \mathbb{N}}$
(def. \ref{TimeOrderedProduct}) that satisfies all these conditions, then one says that an
[[interacting field theory|interacting]] [[perturbative QFT]] satisfying $\{P_i\}$ fails to exist due to a _[[quantum anomaly]]_.

=--


+-- {: .num_prop #BasicConditionsRenormalization}
###### Proposition
**(basic [[renormalization conditions]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

Then the following conditions are [[renormalization conditions]] (def. \ref{RenormalizationConditions}):

1. (field independence) The [[functional derivative]] of a [[polynomial observable]] arising as a [[time-ordered product]] takes contributions only from the arguments, not from the product operation itself; in [[generalized function]]-notation:

   $$
     \label{FieldIndependenceRenormalizationCondition}
     \frac{\delta}{\delta \mathbf{\Phi}^a(x)}
     T(A_1, \cdots, A_n)
     \;=\;
     \underset{1 \leq k \leq n}{\sum}
     T\left(
       A_1, \cdots, A_{k-1}, \frac{\delta}{\delta \mathbf{\Phi}^a(x)}A_k, A_{k+1}, \cdots, A_n
     \right)
   $$

1. ([[translation group|translation]] equivariance) If the underlying [[spacetime]] is [[Minkowski spacetime]], $\Sigma = \mathbb{R}^{p,1}$,
   with the induced [[action]] of the [[translation group]] on [[polynomial observables]]

   $$
     \rho
       \;\colon\;
     \mathbb{R}^{p,1} \times PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]
       \longrightarrow
     PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]
   $$

   then

   $$
     \rho_v \left( {\, \atop \,} T(A_1, \cdots, A_n) {\, \atop \,}\right)
     \;=\;
     T(\rho_{v}(A_1), \cdots, \rho_v(A_n))
   $$

1. ([[quantum master equation]], [[master Ward identity]]) see prop. \ref{QuantumMasterEquation}

   (if this condition fails, the corresponding [[quantum anomaly]] (def. \ref{RenormalizationConditions}) is called a _[[gauge anomaly]]_)


=--

([Duetsch 18, p. 150 and section 4.2](#Duetsch18))

+-- {: .proof}
###### Proof

For the first two statements this is obvious from prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal} and prop. \ref{TimeOrderedProductAwayFromDiagonal}, which imply that $T_{n+1}\vert_{\Sigma^{n+1} \setminus diag(\Sigma)}$ is
uniquely specified from $\{T_k\}_{k \leq n}$ via the [[star product]] induced by the [[Feynman propagator]],
and the fact that, on [[Minkowski  spacetime]], this is manifestly translation invariant and independent of the fields
(e.q. [this prop.](Feynman+propagator#FeynmanPropagatorAsACauchyPrincipalvalue)).

The third statement requires work. That the [[quantum master equation]]/([[master Ward identity]]
always holds on [[regular polynomial observables]] is prop. \ref{QuantumMasterEquation} below.
That it holds for $T_{n+1}\vert_{\Sigma^{n+1} \setminus diag(\Sigma)}$ if it holds for $\{T_k\}_{k \leq n}$
is shown in ([Duetsch 18, section 4.2.2](#Duetsch18)).

=--

+-- {: .num_theorem #PerturbativeRenormalizationMainTheorem}
###### Theorem
**([[main theorem of perturbative renormalization]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

1. An [[S-matrix]] [[renormalization scheme]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) around this free vacuum,
   satisfying the [[renormalization conditions]] (def. \ref{RenormalizationConditions}) "field independence" (prop. \ref{BasicConditionsRenormalization}),
   exists, and its construction by choices of [[renormalization|("re"-)normalization]] of [[time-ordered products]] $\{T_k\}_{k \in \mathbb{N}}$ according to def. \ref{ExtensionOfTimeOrderedProoductsRenormalization} involves precisely a [[finite-dimensional vector space]] of choices ("renormalization constants") at each order $k \in \mathbb{N}$.

1. Every [[pair]] $\mathcal{S}$, $\widetilde{\mathcal{S}}$ of such choices is related by a unique _[[interaction vertex redefinition]]_

   $$
     \mathcal{Z}
     \;\colon\;
     LocObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ]
       \longrightarrow
     LocObs(E_{\text{BV-BRST}})[ [ \hbar, h ] ]
   $$

   via [[precomposition]]

   $$
     \widetilde{\mathcal{S}} \;=\; \mathcal{S} \circ Z
     \,.
   $$

1. The [[group]] of transformations $\mathcal{Z}$ arising this way is the _[[Stückelberg-Petermann renormalization group]]_.

=--

In summary this says that for each free field vacuum, the space of [[renormalization schemes]] for [[perturbative QFT]] around this vacuum is non-empty and is canonically a [[torsor]] over the [[Stückelberg-Petermann renormalization group]].

Notice that the [[Stückelberg-Petermann renormalization group]] involves neither [[scaling transformations]] as in [[Gell-Mann-Low renormalization cocycles]], nor cutoffs as in Wilsonian [[effective field theory]]. But these alternative perspectives may be extracted as specia cases ([Brunetti-Dütsch-Fredenhagen 09](renormalization+group#BrunettiDuetschFredenhagen09)).

$\,$

#### Feynman perturbation series
 {#FeynmanDiagrams}


By def \ref{ExtensionOfTimeOrderedProoductsRenormalization} and the [[main theorem of perturbative renormalization]] (theorem \ref{PerturbativeRenormalizationMainTheorem}), the construction of perturbative [[S-matrix]] schemes/[[time-ordered products]] may be phrased as [[renormalization|("re-")normalization]] of the [[star product]] induced by the [[Feynman propagator]], namely as a choice of [[extension of distributions]] of the this star-product to the locus of coinciding interaction points.

Since the [[star product]] is the [[exponential]] of the binary contraction with the [[Feynman propagator]], it is naturally expanded as a [[sum]] of [[products of distributions]] labeled by [[finite multigraphs]] (def. \ref{Graphs} below),
where each [[vertex]] corresponds to an [[interaction]] or [[source field]] insertion, and where each [[edge]]
corresponds to one contractions of two of these with the [[Feynman propagator]]. The [[products of distributions]]
arising this way are the _[[Feynman amplitudes]]_ (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints} below).

If the [[free field]] [[vacuum]] is decomposed as a [[direct sum]] of distinct [[free field]] [[types]]/species (def. \ref{VerticesAndFieldSpecies} below), then
in addition to the [[vertices]] also the edges in these [[graphs]] receive labels, now by the field species whose particular [[Feynman propagator]] is being used in the contraction at that edges.
These labeled graphs are now called _[[Feynman diagrams]]_ (def. \ref{FeynmanDiagram} below) and the [[products of distributions]] which they encode are their _[[Feynman amplitudes]]_ built by the _[[Feynman rules]]_ (prop. \ref{FeynmanDiagramAmplitude} below).

The choice of [[renormalization|("re"-)normalization]] of the [[time-ordered products]]/[[S-matrix]] is thus equivalently a choice of [[renormalization|("re"-)normalization]] of the [[Feynman amplitudes]] for all possible [[Feynman diagrams]].
These are usefully organized in powers of $\hbar$ by their _[[loop order]]_ (prop. \ref{FeynmanDiagramLoopOrder} below).

In conclusion, the [[Feynman rules]] make the perturbative [[S-matrix]] be equal to a [[formal power series]]
of [[Feynman amplitudes]] labeled by [[Feynman graphs]]. As such it is known as the _[[Feynman perturbation series]]_ (example \ref{FeynmanPerturbationSeries} below).

Notice how it is therefore the [[combinatorics]] of [[star products]] that governs both [[Wick's lemma]] in [[free field theory]] as well as [[Feynman diagram|Feynman diagrammatics]] in [[interacting field theory]]:

[[!include Wick algebra -- table]]


$\,$

{#FeynmanDiagramInTwoStages} We now discuss [[Feynman diagrams]] and their [[Feynman amplitudes]] in two stages:
First we consider plain [[finite multigraphs]] with [[linear order|linearly ordered]] vertices
but no other labels (def. \ref{Graphs} below) and discuss how these generally organize an expansion
of the [[time-ordered products]] as a sum of [[products of distributions|distributional products]]
of the given [[Feynman propagator]] (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints} below).
These summands (or their [[vacuum expectation values]]) are called the _[[Feynman amplitudes]]_ if
one thinks of the underlying [[free field]] [[vacuum]] as having a single "field species"
and of the chosen [[interaction]] to be a single "interaction vertex".

But often it is possible and useful to identify different field species and different interaction vertices.
In fact in applications this choice is typically evident and not highlighted as a choice. We
make it explicit below as def. \ref{VerticesAndFieldSpecies}.  Such a choice makes
both the [[interaction]] term as well as the [[Feynman propagator]] decompose as sums (remark \ref{FeynmanPropagatorFieldSpecies} below).
Accordingly then, after "multiplying out" the products of these sums that appear in the Feynman amplitudes, these, too, decompose
further as as sums indexed by multigraphs whose edges are labeled by field species, and whose vertices are labeled
by interactions. These labeled multigraphs are the _[[Feynman diagrams]]_ (def. \ref{FeynmanDiagram} below) and the
corresponding summands are the [[Feynman amplitudes]] proper (prop. \ref{FeynmanDiagramAmplitude} below).

+-- {: .num_defn #Graphs}
###### Definition
**([[finite graph|finite]] [[multigraphs]])**

A _[[finite graph|finite]] [[multigraph]]_ is

1. a [[finite set]] $V$ ("of [[vertices]]");

1. a [[finite set]] $E$ ("of [[edges]]");

1. a [[function]] $E \overset{p}{\to} \left\{ {\,\atop \,} \{v_1, v_2\} = \{v_2, v_1\} \;\vert\; v_1, v_2 \in V \,,\; v_1 \neq v_2 {\, \atop \,} \right\}$

   (sending any [[edge]] to the unordered pair of distinct [[vertices]] that it goes between).

A choice of [[linear order]] on the set of vertices of a finite multigraph is a choice of [[bijection]] of the form

$$
  V \simeq \{1, 2, \cdots, \nu\}
  \,.
$$

Hence the [[isomorphism classes]] of a [[finite graph|finite]] [[multigraphs]] with [[linear order|linearly ordered]]
[[vertices]] are characterized by

1. a [[natural number]]

   $$
     \nu \coloneqq {\vert V\vert} \in \mathbb{N}
   $$

   (the number of [[vertices]]);

1. for each $i \lt j \in \{1, \cdots, \nu\}$ a natural number

   $$
     e_{i,j} \coloneqq {\vert p^{-1}(\{v_i,v_j\})\vert} \in \mathbb{N}
   $$

   (the number of [[edges]] between the $i$th and the $j$th vertex).

We write $\mathcal{G}_\nu$ for the set of such [[isomorphism classes]] of finite multigraphs with linearly ordered vertices
identified with $\{1, 2, \cdots, \nu\}$; and we write

$$
  \mathcal{G} \;\coloneqq\; \underset{\nu \in \mathbb{N}}{\sqcup} \mathcal{G}_\nu
$$

for the set of [[isomorphism classes]] of finite multigraphs with linearly ordered vertices of any number.

=--

+-- {: .num_prop #FeynmanPerturbationSeriesAwayFromCoincidingPoints}
###### Proposition
**([[Feynman amplitudes]] of [[finite multigraphs]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

For $\nu \in \mathbb{N}$, the $\nu$-fold [[time-ordered product]] away from coinciding interaction points, given by prop. \ref{TimeOrderedProductAwayFromDiagonal}

$$
  T_\nu
    \;\colon\;
  \left(
    {\, \atop \,}
    LocObs(E_{\text{BV-BRST}})[ [\hbar, g, j] ]
    {\, \atop \,}
  \right)^{\otimes^\nu_{\mathbb{C}[ [\hbar, g, j] ]}}_{pds}
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}((\hbar))[ [g , j] ]
$$

is equal to the following [[formal power series]] labeled by [[isomorphism classes]] of [[finite multigraphs]] with $\nu$ [[linear order|linearly ordered]] [[vertices]], $\Gamma \in \mathcal{G}_\nu$ (def. \ref{Graphs}):

$$
  \label{FeynmanAmplitudeExpansionOfTimeOrderedProductAwayFromDiagonal}
  \begin{aligned}
    & T_\nu(O_1, \cdots , O_\nu)
    \\
    & =
    \underset{\Gamma \in \mathcal{G}_\nu}{\sum}
     \Gamma\left(O_i)_{i = 1}^\nu\right)
    \\
    & \coloneqq
    \underset{ \Gamma \in \mathcal{G}_\nu }{\sum}
    prod
    \circ
    \underset{ r \lt s \in \{1, \cdots, \nu\} }{\prod}
    \frac{\hbar^{e_{r,s}}}{e_{r,s}!}
    \left\langle
      (\Delta_{F})^{e_{r,s}}
      ,
      \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_r^{e_{r,s}}}
      \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_s^{e_{r,s}}}
    \right\rangle
    \left(
      O_1 \otimes \cdots \otimes O_{\nu}
    \right)
    \\
    & \coloneqq
    \underset{ \Gamma \in \mathcal{G}_\nu  }{\sum}
    ((-) \cdot \cdots \cdot (-))
    \circ
    \underset{ r \lt s \in \{1, \cdots,\nu\} }{\prod}
    \frac{\hbar^{e_{r,s}}}{e_{r,s}!}
    \\
    &
    \phantom{AAA}
      \underset{i = 1, \cdots e_{r,s}}{\prod}
        \underset{\Sigma \times \Sigma}{\int}
         dvol_\Sigma(x_i)
         dvol_\Sigma(y_i)
         \,
         \Delta_F^{a_i b_i}(x_i,y_i)
     \\
     & \phantom{AAAAAA}
    \left(
      O_1
        \otimes
        \cdots
        \otimes
      O_{r-1}
        \otimes
       \frac{
         \delta^{e_{r,s}} O_r
       }{
         \delta \mathbf{\Phi}^{a_1}(x_1)
         \cdots
         \delta \mathbf{\Phi}^{a_{e_{r,s}}}(x_{e_{r,s}})
       }
        \otimes
      O_{r+1}
        \otimes
        \cdots
        \otimes
      O_{s-1}
        \otimes
      \frac{
          \delta^{e_{r,s}} O_s
       }{
         \delta \mathbf{\Phi}^{b_1}(y_1)
         \cdots
         \delta \mathbf{\Phi}^{b_{e_{r,s}}}(y_{e_{r,s}})
       }
        \otimes
       O_{s+1}
        \otimes
        \cdots
        \otimes
      O_\nu
    \right)
    \,,
  \end{aligned}
$$

where $e_{r,s} \coloneqq e_{r,s}(\Gamma)$ is, for short, the number of [[edges]] between vertex $r$ and vertex $s$ in the
[[finite multigraph]] $\Gamma$ of the outer sum, according to def. \ref{Graphs}.

Here the summands of the expansion (eq:FeynmanAmplitudeExpansionOfTimeOrderedProductAwayFromDiagonal)

$$
  \label{FeynmanAmplitude}
  \Gamma\left( (O_i)_{i = 1}^\nu\right)
  \;\coloneqq\;
    prod
    \circ
    \underset{ r \lt s \in \{1, \cdots,\nu\} }{\prod}
    \frac{\hbar^{e_{r,s}}}{e_{r,s}!}
    \left\langle
      (\Delta_{F})^{e_{r,s}}
      ,
      \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_r^{e_{r,s}}}
      \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_s^{e_{r,s}}}
    \right\rangle
    \left(
      O_1 \otimes \cdots \otimes O_{\nu}
    \right)
  \;\in\;
  PolyObs(E_{\text{BV-BRT}})((\hbar))[ [g,j ] ]
$$

and/or their [[vacuum expectation values]]

$$
  \left\langle
    \Gamma\left((V_i)_{i = 1}^v\right)
  \right\rangle
  \;\in\;
  \mathbb{C}((\hbar))[ [ h, j] ]
$$

are called the _[[Feynman amplitudes]]_ for scattering processes in the given [[free field]] [[vacuum]] of shape $\Gamma$  with [[interaction]] [[vertices]] $O_i$. Their expression as [[products of distributions]] via algebraic expression on the right hand side of (eq:FeynmanAmplitude) is also called the _[[Feynman rules]]_.

=--

([Keller 10, IV.1](#Keller10))

+-- {: .proof}
###### Proof

We proceed by [[induction]] over the number $v$ of [[vertices]].
The statement is trivially true for a single vertex.
So assume that it is true for $v \geq 1$ vertices. It follows that

$$
  \begin{aligned}
    & T(O_1, \cdots, O_\nu, O_{\nu+1})
    \\
    & =
    T( T(O_1, \cdots ,O_\nu),  O_{\nu+1} )
    \\
    &=
    prod
      \circ
    \exp\left(
      \left\langle
        \hbar \Delta_F,
        \frac{\delta}{\delta \mathbf{\Phi}}
          \otimes
        \frac{\delta}{\delta \mathbf{\Phi}}
      \right\rangle
    \right)
    \left(
    \left(
      prod
        \circ
      \!\!\!\!
      \underset{\Gamma \in \mathcal{G}_\nu }{\sum}
      \underset{ { r \lt s } \atop { \in \{1, \cdots, \nu\} }  }{\prod}
      \frac{1}{e_{r,s}!}
      \left\langle
          (\hbar \Delta_F)^{e_{r,s}}
          \,,\,
          \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_r^{e_{r,s}}}
          \frac{\delta^{e_{r,s}}}{ \delta \mathbf{\Phi}_s^{e_{r,s}} }
      \right\rangle
      (O_1 \otimes \cdots \otimes O_\nu)
    \right)
      \,\otimes\,
    O_{\nu+1}
    \right)
    \\
    & =
    prod
      \circ
    \underset{\Gamma \in \mathcal{G}_\nu }{\sum}
    \\
    & \phantom{=}
      \underset{ {  r \lt s } \atop {  \in \{1,\cdots, \nu\}}  }{\prod}
      \frac{1}{e_{r,s}!}
    \left\langle
        (\hbar \Delta_F)^{e_{r,s}}
        \,,\,
        \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_r^{e_{r,s}}}
        \frac{\delta^{e_{r,s}}}{ \delta \mathbf{\Phi}_s^{e_{r,s}} }
    \right\rangle
    \\
    & \phantom{=}
    \underset{
       { e_{\nu+1} =}
       \atop
       { e_{1,{\nu+1}} + \cdots + e_{\nu,\nu + 1} }
    }{\sum}
      \underset{
        = (e_{1,\nu + 1}) \cdots (e_{\nu,\nu+1}))
      }{
      \underbrace{
      \frac{
        \left(
          { e_{\nu + 1} }
          \atop
          { (e_{1, \nu + 1}), \cdots, (e_{\nu , \nu+1}) }
        \right)
      }{
        ( e_{\nu+1} ) !
      }
      }
      }
    \left\langle
      (\hbar \Delta_F)^{e_{\nu+1}}
    \left(
      \frac{\delta^{e_{1,\nu+1}} O_1 }{\delta \mathbf{\Phi}^{e_{1,\nu+1}}}
        \otimes
        \cdots
        \otimes
      \frac{
        \delta^{e_{\nu,\nu+1}} O_\nu
      }{
        \delta \mathbf{\Phi}^{e_{\nu,\nu+1}}
      }
    \;\otimes\;
    \frac{
      \delta^{ e_{\nu + 1} } O_{\nu+1}
    }{
      \delta \mathbf{\Phi}^{e_{1,\nu+1} + \cdots + e_{\nu,\nu+1}}
    }
    \right\rangle
    \right)
    \\
    &=
    prod
      \circ
    \underset{\Gamma \in \mathcal{G}_{\nu+1} }{\sum}
    \underset{ { r \lt s } \atop { \in \{1, \cdots, \nu+1\} } }{\prod}
    \tfrac{1}{e_{r,s}!}
    \left\langle
        (\hbar \Delta_F)^{e_{r,s}}
        \,,\,
        \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_r^{e_{r,s}}}
        \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_s^{e_{r,s}}}
    \right\rangle
    (O_1 \otimes \cdots \otimes O_{\nu+1})
  \end{aligned}
$$

The combinatorial factor over the brace is the [[multinomial coefficient]] expressing the number of ways of distributing $e_{\nu+1}$-many functional derivatives to $v$ factors, via the [[product rule]], and quotiented by the [[factorial]] that comes from the [[exponential]] in the definition of the [[star product]].

Here in the first step we used the [[associativity]] (eq:RestrictedTimeOrderedProductAssociative) of the restricted time-ordered product, in the second step we used the induction assumption,
in the third we passed the outer functional derivatives through the pointwise product using the [[product rule]], and in the fourth step we recognized that this amounts to summing
in addition over all possible choices of sets of edges from the first $v$ vertices to the new $\nu+1$st vertex,
which yield in total the sum over all diagrams with $\nu+1$ vertices.

=--

If the [[free field theory]] is decomposed as a [[direct sum]] of free field theories, we obtain a more
fine-grained concept of [[Feynman amplitudes]]:

+-- {: .num_defn #VerticesAndFieldSpecies}
###### Definition
**(field species and interaction vertices)**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, and let $g S_{int} + j A \;\in\; LocObs(E_{\text{BV-BRST}})[ [ \hbar , g , j] ]\langle g,j \rangle$
be a [[local observable]] regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

Then

1. a choice of _field species_ is a choice of decomposition of the  [[BV-BRST formalism|BV-BRST]] [[field bundle]] $E_{\text{BV-BRST}}$
as a [[fiber product]] over [[finite set]] $Spec = \{sp_1, sp_2, \cdots, sp_n\}$ of ([[graded manifold|graded]] [[supermanifold|super-]]) [[field bundles]]

   $$
     E_{\text{BV-BRST}}
     \;\simeq\;
     E_{sp_1} \times_{\Sigma} \cdots \times_\Sigma E_{sp_n}
     \,,
   $$

   such that the [[gauge fixing|gauge fixed]] [[free field|free]] [[Lagrangian density]] $\mathbf{L}'$ is the [[sum]]

   $$
     \mathbf{L}' \;=\; \mathbf{L}'_{sp_1} + \cdots + \mathbf{L}'_{sp_n}
   $$

   of [[free field theory|free]] [[Lagrangian densities]]

   $$
     \mathbf{L}'_{sp_i} \in \Omega^{p+1,0}_\Sigma(E_i)
   $$

  on these separate field bundles.

1. a choice of _interaction vertices and external vertices_ is a choice of sum decomposition

   $$
     g S_{int} + j A
     \;=\;
     \underset{i \in Ext}{\sum} g S_{int,i}
     +
     \underset{j \in Int}{\sum} j A_j
   $$

   parameterized by [[finite sets]] $Int$ and $Ext$, to be called the sets of _internal vertex labels_ and _external vertex labels_,
respectively.

=--

+-- {: .num_remark #FeynmanPropagatorFieldSpecies}
###### Remark
**(Feynman propagator for separate field species)**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

Then a choice of field species as in def. \ref{VerticesAndFieldSpecies}
induces a corresponding decomposition of the [[Feynman propagator]] of the gauge fixed free field theory

$$
  \Delta_F
  \;\in\;
  \Gamma'_{\Sigma \times \Sigma}( E_{\text{BV-BRST}} \boxtimes E_{\text{BV-BRST}} )
$$

as the sum of Feynman propagators for each of the chosen field species:

$$
  \Delta_F
  \;=\;
  \Delta_{F,1} + \cdots + \Delta_{F,n}
  \;\in\;
  \underoverset{i = 1}{n}{\oplus}
  \Gamma'_{\Sigma \times \Sigma}( E_{sp_i} \boxtimes E_{sp_i} )
    \;\subset\;
  \Gamma'_{\Sigma \times \Sigma}( E_{\text{BV-BRST}} \boxtimes E_{\text{BV-BRST}} )
$$

hence in components, with $(\phi^A$ the collective field coordinates on $E_{\text{BV-BRST}}$,
this decomposition is of the form

$$
  \left(
    \Delta_F^{A, B}
  \right)
  \;=\;
  \left(
    \array{
      (\Delta_{F,1}^{a b}) & 0 & 0 &  \cdots & 0
      \\
      0 & (\Delta_{F,2}^{\alpha \beta}) & 0 & \cdots & 0
      \\
      \vdots & & & & \vdots
      \\
      0 & \cdots & \cdots & 0 & (\Delta_{F,n}^{i j})
    }
  \right)
$$

=--


+-- {: .num_example #FieldSpeciesQED}
###### Example
**(field species in [[quantum electrodynamics]])**

The [[field bundle]] for [[Gaussian-averaged Lorenz gauge|Lorenz]] [[gauge fixing|gauge fixed]] [[quantum electrodynamics]]
on [[Minkowski spacetime]] $\Sigma$ admits a decomposition into field species, according to def. \ref{VerticesAndFieldSpecies}, as


$$
  E_{\text{BV-BRST}}
  \;=\;
   \underset{
      \text{Dirac}
      \atop
      \text{field}
    }{
    \underbrace{
    (S_{odd} \times \Sigma)
    }}
    \times_\Sigma
   \underset{
     {\text{electromagnetic field &amp;}}
     \atop
     {\text{Nakanishi-Lautrup field}}
    }{
    \underbrace{
      T^\ast\Sigma
       \times_\Sigma
      (\mathbb{R} \times \Sigma)
    }}
   \times_\Sigma
   \underset{
     \text{ghost field}
   }{
   \underbrace{
     (\mathbb{R}[1] \times \Sigma)
   }
   }
   \times_\Sigma
   \underset{
     \text{antighost field}
   }{
   \underbrace{
     (\mathbb{R}[-1] \times \Sigma)
   }
   }
$$

(by [this example](A+first+idea+of+quantum+field+theory#LagrangianQED) and [this example](A+first+idea+of+quantum+field+theory#NLGaugeFixingOfElectromagnetism)).

The corresponding sum decomposition of the Feynman propagator, according to remark \ref{FeynmanPropagatorFieldSpecies},
is

$$
  \Delta_F
    \;=\;
  \underset{
    \text{Dirac}
    \atop
    \text{field}
  }{
  \underbrace{
    \Delta_F^{\text{electron}}
  }
  }
  +
  \underset{
    \text{electromagnetic field &amp;}
    \atop
    \text{Nakanishi-Lautrup field}
  }{
  \underbrace{
    \left(
      \array{
        \Delta_F^{photon} & *
        \\
        * & *
      }
    \right)
  }
  }
  +
  \Delta_F^{ghost}
  +
  \Delta_F^{\text{antighost}}
  \,,
$$

where

1. $\Delta_F^{\text{electron}}$ is the [[electron propagator]] ([this def.](Feynman+propagator#FeynmanPropagatorForDiracOperatorOnMinkowskiSpacetime))

1. $\Delta_F^{photon}$ is the [[photon propagator]] in [[Gaussian-averaged Lorenz gauge]] ([this prop.](A+first+idea+of+quantum+field+theory#PhotonPropagatorInGaussianAveragedLorenzGauge))

1. the [[ghost field]] and [[antighost field]] [[Feynman propagators]] $\Delta_F^{ghost}$, and $\Delta_F^{antighost}$ are each one copy of the [[Feynman propagator]] of the [[real scalar field]] ([this prop.](Feynman+propagator#FeynmanPropagatorAsACauchyPrincipalvalue)), while the [[Nakanishi-Lautrup field]] contributes a mixing with the [[photon propagator]], notationally suppressed behind the star-symbols above.

=--


+-- {: .num_defn #FeynmanDiagram}
###### Definition
**([[Feynman diagrams]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, and let $g S_{int} + j A \;\in\; LocObs(E_{\text{BV-BRST}})[ [ \hbar , g , j] ]\langle g,j \rangle$
be a [[local observable]] regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

Let moreover

$$
  E_{\text{BV-BRST}}
  \;\simeq\;
  \underset{sp \in Spec}{\times} E_{sp}
  \,,
$$

be a choice of field species, according to def \ref{VerticesAndFieldSpecies},

$$
  g S_{int} + j A
  \;=\;
  \underset{i \in Ext}{\sum} g S_{int,i}
  +
  \underset{j \in Int}{\Sum} j A_j
$$

a choice of internal and external interaction vertices according to def. \ref{VerticesAndFieldSpecies}.

With these choices, we say that a _[[Feynman diagram]]_ $(\Gamma, vertlab, edgelab)$ is

1. a [[finite multigraph]] with [[linear order|linearly ordered]] vertices (def. \ref{Graphs})

   $$
     \Gamma \in \mathcal{G}
     \,,
   $$

1. a [[function]] from its [[vertices]]

   $$
     vertlab \;\colon\; V_{\Gamma} \longrightarrow Int \sqcup Ext
   $$

   to the [[disjoint union]] of the chosen sets of internal and external vertex labels;

1. a [[function]] from its [[edges]]

   $$
     edgelab \;\colon\; E_{\Gamma} \to Spec
   $$

   to the chosen set of field species.

We write

$$
  \array{
    \mathcal{G}^{Feyn}
      &\overset{\text{forget} \atop \text{labels}}{\longrightarrow}&
    \mathcal{G}
    \\
    (\Gamma,vertlab, edgelab) &\mapsto& \Gamma
  }
$$

for the set of [[isomorphism classes]] of Feynman diagrams with labels in $Sp$, refining the set of
isomorphisms of plain [[finite multigraphs]] with [[linear order|linearly ordered]] [[vertices]] from def. \ref{Graphs}.

=--


+-- {: .num_prop #FeynmanDiagramAmplitude}
###### Proposition
**([[Feynman amplitudes]] for [[Feynman diagrams]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, and let $g S_{int} + j A \;\in\; LocObs(E_{\text{BV-BRST}})[ [ \hbar , g , j] ]\langle g,j \rangle$
be a [[local observable]] regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

Let moreover

$$
  E_{\text{BV-BRST}}
  \;\simeq\;
  \underset{sp \in Spec}{\times} E_{sp}
  \,,
$$

be a choice of field species, according to def \ref{VerticesAndFieldSpecies}, hence inducing, by remark \ref{FeynmanPropagatorFieldSpecies},
a sum decomposition of the [[Feynman propagator]]

$$
  \label{FeynmanPropagatorSumOverFieldSpecies}
  \Delta_F
  \;=\;
  \underset{sp \in Spec}{\sum}\Delta_{F,sp}
  \,,
$$

and let

$$
  \label{VertexDecompositionFeynmanAmplitude}
  g S_{int} + j A
  \;=\;
  \underset{i \in Ext}{\sum} g S_{int,i}
  +
  \underset{j \in Int}{\Sum} j A_j
$$

be a choice of internal and external interaction vertices according to def. \ref{VerticesAndFieldSpecies}.

Then by "multiplying out" the products of the sums (eq:FeynmanPropagatorSumOverFieldSpecies) and (eq:VertexDecompositionFeynmanAmplitude) in the
formula (eq:FeynmanAmplitude) for the [[Feynman amplitude]] $\Gamma\left( (g S_{int} + j A))_{i = 1}^\nu \right)$ (def. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}) this decomposes as a sum of the form

$$
  \Gamma\left(
    (g S_{int} + j A)_{i = 1}^\nu
  \right)
  \;=\;
  \underset{
    { V_\Gamma \overset{vertlab}{\longrightarrow} Int \sqcup Ext}
    \atop
    { E_\Gamma \overset{edgelab}{\longrightarrow}  Spec }
  }{\sum}
    \left(
      \Gamma,
      edgelab, vertlab
    \right)
    (g S_{int} + j A)
$$

over all ways of labeling the [[vertices]] $v$ of $\Gamma$ by the internal or external vertex labels,
and  the [[edges]] $e$ of $\Gamma$ by field species. The corresponding summands

$$
   \left(
     \Gamma,
     edgelab,
     vertlab
   \right)
   (g S_{int} + j A)
   \;\in\;
   PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]
$$

or rather their [[vacuum expectation value]]

$$
  \left\langle
   \left(
     \Gamma,
     edgelab, vertlab
   \right)
   (g S_{int} + j A)
  \right\rangle
  \;\in\;
  \mathbb{C}[ [ \hbar, g, j ] ]
$$

are called the _[[Feynman amplitude]] associated with these [[Feynman diagrams]].

=--


[[!include Feynman diagrams in causal perturbation theory -- summary]]


+-- {: .num_example #FeynmanPerturbationSeries}
###### Example
**([[Feynman perturbation series]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, and let

$$
  g S_{int} + j A
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, h ] ]\langle g , j\rangle
$$

be a [[local observable]], regarded as a [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

By prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints} every choice of perturbative [[S-matrix]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering})

$$
  \mathcal{S}(g S_{int} + j A)
  \;\in\;
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g, j ] ] +
$$

has an expansion as a [[formal power series]] of the form

$$
  \mathcal{S}(g S_{int} + j A)
  \;=\;
  \underset{\Gamma \in \mathcal{G}}{\sum}
  \Gamma\left( (g S_{int} + j A)_{i = 1}^{\nu(\Gamma)}\right)
  \,,
$$

where the series is over all [[finite multigraphs]] with [[linear order|linearly ordered]] [[vertices]] $\Gamma$ (def. \ref{Graphs}), and the summands are the corresponding [[renormalization|("re"-)normalized]] (def. \ref{ExtensionOfTimeOrderedProoductsRenormalization}) [[Feynman amplitudes]] (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}).

If moreover a choice of field species and of internal and external interaction vertices is made, according to def. \ref{VerticesAndFieldSpecies},
then this series expansion refines to an expansion over all [[Feynman diagrams]] $(\Gamma,edgelab, vertlab)$ (def. \ref{FeynmanDiagram})
of [[Feynman amplitudes]] $(\Gamma, edgelab,vertlab)(g S_{int} + j A)$ (def. \ref{FeynmanDiagramAmplitude}):

$$
  \mathcal{S}(g S_{int} + j A)
  \;=\;
  \underset{(\Gamma,edgelab, vertlab) \in \mathcal{G}^{Feyn}}{\sum}
    (\Gamma, edgelab,vertlab)(g S_{int} + j A)
  \,,
$$


Expressed in this form the S-matrix is known as the _[[Feynman perturbation series]]_.

=--


+-- {: .num_remark #Tadpoles}
###### Remark
**(no [[tadpole]] [[Feynman diagrams]])**

In the definition of [[finite multigraphs]] in def. \ref{Graphs} there are _no_ edges considered that go from any [[vertex]] to _itself_. Accordingly, there are _no_ such labeled edges in [[Feynman diagrams]] (def. \ref{FeynmanDiagram}):

<center>
  <img src="https://ncatlab.org/nlab/files/tadpole.png" width="70">
</center>

In [[pQFT]] these diagrams are called _[[tadpoles]]_, and their non-appearance is considered part of the _[[Feynman rules]]_ (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}).
Via prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints} this condition reflects the nature of the [[star product]] ([this def.](star+product#PropagatorStarProduct)) which always contracts _different_ [[tensor product]] factors with the [[Feynman propagator]] before taking their pointwise product.

Beware that in [[graph theory]] these [[tadpoles]] are called "[[loops]]", while here in [[pQFT]] a "loop" in a [[planar graph]] refers instead to what in [[graph theory]] is called a _[[face]]_ of the graph, see the discussion of _[[loop order]]_ in prop. \ref{FeynmanDiagramLoopOrder} below.

=--

([Keller 10, remark II.8 and proof of prop. II.7](#Keller10))





$\,$

#### Effective action
 {#EffectiveAction}

We have seen that the [[Feynman perturbation series]] expresses the [[S-matrix]] as a [[formal power series]] of _[[Feynman amplitudes]]_ labeled by _[[Feynman diagrams]]_. Now the [[Feynman amplitude]] associated with a [[disjoint union]] of [[connected graph|connected]] [[Feynman diagrams]] (def. \ref{ConnectedGraphs} below) is just the product of the amplitudes of the [[connected components]] (prop. \ref{LogarithmEffectiveAction} below). This allows to re-organize the [[Feynman perturbation series]] as the ordinary [[exponential]] of the Feynman perturbation series restricted to just [[connected graph|connected]] Feynman diagrams. The latter is called the _[[effective action]]_ (def. \ref{InPerturbationTheoryActionEffective} below) because it allows to express [[vacuum expectation values]] of the [[S-matrix]] as an ordinary exponential (equation (eq:ExponentialSeffVEVOfSMatrix) below).

+-- {: .num_defn #ConnectedGraphs}
###### Definition
**([[connected graphs]])**

Given two [[finite multigraphs]] $\Gamma_1, \Gamma_2 \in \mathcal{G}$ (def. \ref{Graphs}), their [[disjoint union]]

$$
  \Gamma_1 \sqcup \Gamma_2
  \;\in\;
  \mathcal{G}
$$

is the finite multigraph whose set of [[vertices]] and set of [[edges]] are the [[disjoint unions]] of the corresponding sets of $\Gamma_1$ and $\Gamma_2$

$$
  V_{\Gamma_1 \sqcup \Gamma_2}
    \;\coloneqq\;
  V_{\Gamma_1} \sqcup V_{\Gamma_2}
$$

$$
  E_{\Gamma_1 \sqcup \Gamma_2}
    \;\coloneqq\;
  E_{\Gamma_1} \sqcup E_{\Gamma_2}
$$

and whose vertex-assigning function $p$ is the corresponding function on disjoint unions

$$
  p_{\Gamma_1 \sqcup \Gamma_2}
  \;\coloneqq\;
  p_{\Gamma_1} \sqcup p_{\Gamma_2}
  \,.
$$

The operation induces a pairing on the set $\mathcal{G}$ of [[isomorphism classes]] of [[finite multigraphs]]

$$
  (-) \sqcup (-)
  \;\colon\;
  \mathcal{G} \times \mathcal{G}
    \longrightarrow
  \mathcal{G}
  \,.
$$

A [[finite multigraph]] $\Gamma \in \mathcal{G}$ (def. \ref{Graphs}) is called _[[connected graph|connected]]_ if it is not the [[disjoint union]] of two [[inhabited|non-empty]] finite multigraphs.

We write

$$
  \mathcal{G}_{conn}
  \subset
  \mathcal{G}
$$

for the subset of [[isomorphism classes]] of [[connected graph|connected]] [[finite multigraphs]].


=--

+-- {: .num_lemma #MultiplicativeFeynmanAmplitudes}
###### Lemma
**([[Feynman amplitudes]] multiply under [[disjoint union]] of [[graphs]])**

Let

$$
  \Gamma
    \;=\;
  \Gamma_1
    \sqcup
  \Gamma_2
    \sqcup
    \cdots
    \sqcup
  \Gamma_n
  \;\in\; \mathcal{G}
$$

be [[disjoint union]] of graphs (def. \ref{ConnectedGraphs}). then then corresponding [[Feynman amplitudes]] (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints})
multiply by the pointwise product ([this def.](A+first+idea+of+quantum+field+theory#Observable)):

$$
  \Gamma\left( g S_{int} + j A)_{i = 1}^{\nu(\Gamma)} \right)
  \;=\;
  \Gamma_1\left( (g S_{int} + j A)_{i = 1}^{\nu(\Gamma_1)}\right)
   \cdot
  \Gamma_2\left( (g S_{int} + j A)_{i = 1}^{\nu(\Gamma_2)} \right)
    \cdot
    \cdots
    \cdot
  \Gamma_n\left( (g S_{int} + j A)_{i = 1}^{\nu(\Gamma_n)} \right)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{TimeOrderedProductAwayFromDiagonal} the contributions to the S-matrix away from coinciding interaction points are given by the [[star product]] induced by the [[Feynman propagator]], and specifically, by prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}, the [[Feynman amplitudes]] are given this way.
Moreover the [[star product]] ([this def.](star+product#PropagatorStarProduct)) is given by first contracting with powers of the [[Feynman propagator]] and then multiplying all resulting terms with the pointwise product of observables.
This implies the claim by the nature of the combinatorial factor in the definition of the [[Feynman amplitudes]] (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}).

=--

+-- {: .num_defn #InPerturbationTheoryActionEffective}
###### Definition
**([[effective action]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be an [[S-matrix]] scheme for [[perturbative QFT]] around this vacuum (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) and let

$$
  g S_{int} + j A
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, h ] ]
$$

be a [[local observable]].

Recall that for each [[finite multigraph]] $\Gamma \in \mathcal{G}$ (def. \ref{Graphs}) the [[Feynman perturbation series]] for $\mathcal{S}(g S_{int} + j A)$ (example \ref{FeynmanPerturbationSeries})

$$
  \mathcal{S}(g S_{int} + j A)
  \;=\;
  \underset{\Gamma \in \mathcal{G}}{\sum}
    \Gamma\left( (g S_{int} + j A)_{i = 1}^{v(\Gamma)} \right)
$$

contributes with a [[renormalization|("re"-)nromalized]] [[Feynman amplitude]] $\Gamma\left( (g S_{int} + j A)_{i = 1}^v\right) \in PolyObs(E_{\text{BV-BRST}})((\hbar))[ [ g, j ] ]$.

We say that the corresponding _[[effective action]]_ is $i \hbar$ times the sub-series

$$
  \label{ExpansionEffectiveAction}
  S_{eff}(g,j)
  \;\coloneqq\;
  i \hbar
  \underset{\Gamma \in \mathcal{G}_{conn}}{\sum}
  \Gamma\left( (g S_{int} + j A)_{i = 1}^{\nu(\Gamma)} \right)
  \;\in\;
  PolyObs(E_{\text{BV-BRST}})[ [\hbar,  g, j ] ]
$$

of [[Feynman amplitudes]] that are labeled only by the _[[connected graphs]]_  $\Gamma \in \mathcal{G}_{conn} \subset \mathcal{G}$ (def. \ref{ConnectedGraphs}).

(A priori $S_{eff}(g,j)$ could contain negative powers of $\hbar$, but it turns out that it does not; this is prop. \ref{FeynmanDiagramLoopOrder} below.)

=--

+-- {: .num_remark #TerminologyForEffectiveAction}
###### Remark
**(terminology for "effective action")**

Beware differing conventions of terminology:

1. In [[effective quantum field theory]], the [[effective action]] in def. \ref{InPerturbationTheoryActionEffective} is sometimes called the _effective potential_ at scale $\Lambda = 0$ (see [this prop.](InPerturbationTheoryActionEffective)). 

   This terminology originates in restriction to the special example of the [[scalar field]], where the typical non-derivative [[Phi^n interactions]] $g S_{int} = \underset{n}{\sum} \underset{\Sigma}{\int} g_{sw}^{(n)}(x) (\mathbf{\Phi}(x))^n \, dvol_\Sigma(x)$ are naturally thought of as [[potential energy]]-terms.

   From this perspective the [[effective action]] in def. \ref{InPerturbationTheoryActionEffective} is a special case of _[[relative effective actions]]_ $S_{eff,\Lambda}$ ("relative effective potentials", in the case of [[Phi^n interactions]]) relative to an arbitrary [[UV cutoff]]-scales $\Lambda$ ([this def.](effective+quantum+field+theory#EffectiveActionRelative)).

1. For the special case that 

   $$
     j A 
       \coloneqq 
     \underset{\Sigma}{\int} j_{sw,a}(x) \mathbf{\Phi}^a(x)\, dvol_{\Sigma}(x)
   $$
  
   is a [[regular polynomial observable|regular]] [[linear observable]] ([this def.](A+first+idea+of+quantum+field+theory#RegularLinearFieldObservables)) the [[effective action]] according to def. \ref{InPerturbationTheoryActionEffective} is often denoted $W(j)$ or $E(j)$, and then its _functional [[Legendre transform]]_ (if that makes sense) is instead called the effective action, instead.

   This is because the latter encodes the [[equations of motion]] for the [[vacuum expectation values]] $\langle \mathbf{\Phi}(x)_int\rangle$ of the [[interacting field observables|interacting]] [[field observables]]; we discuss this as example \ref{EquationsOfMotionForVacuumExpectationValues} below.

Notice the different meaning of "effective" in both cases: In the first case it refers to what is effectively seen of the full [[pQFT]] _at some [[UV-cutoff scale]]_, while in the second case it refers to what is effectively seen when restricting attention only to the [[vacuum expectation values]] of [[regular polynomial observable|regular]] [[linear observables]].

=--


+-- {: .num_prop #LogarithmEffectiveAction}
###### Proposition
**([[effective action]] is [[logarithm]] of [[S-matrix]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be an [[S-matrix]] scheme for [[perturbative QFT]] around this vacuum (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) and let

$$
  g S_{int} + j A
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, h ] ]
$$

be a [[local observable]] and let

$$
  S_{eff}(g,j) \;\in\; PolyObs(E_{\text{BV-BRST}})((\hbar))[ [ g, j] ]
$$

be the corresponding [[effective action]] (def. \ref{InPerturbationTheoryActionEffective}).

Then then [[S-matrix]] for $g S_{int} + j A$ is the [[exponential]] of the [[effective action]] with respect to the pointwise product $(-)\cdot (-)$ of observables ([this def.](A+first+idea+of+quantum+field+theory#Observable)):

$$
  \begin{aligned}
    \mathcal{S}(g S_{int} + j A)
    & =
    \exp_\cdot\left( \tfrac{1}{i \hbar} S_{eff}(g,j)  \right)
    \\
    & \coloneqq
    1
      +
    \frac{1}{i \hbar} S_{eff}(g,j)
      +
    \frac{1}{(i \hbar)^2} S_{eff}(g,j) \cdot S_{eff}(g,j)
      +
    \frac{1}{(i \hbar)^3} S_{eff}(g,j) \cdot S_{eff}(g,j) \cdot S_{eff}(g,j)
      +
    \cdots
  \end{aligned}
$$

Moreover, this relation passes to the [[vacuum expectation values]]:

$$
  \label{ExponentialSeffVEVOfSMatrix}
  \begin{aligned}
    \left\langle
      {\, \atop \,}
      \mathcal{S}(g S_{int} + j A)
      {\, \atop \,}
    \right\rangle
    & =
    \left\langle
      {\, \atop \,}
      \exp\left(
        \tfrac{1}{i \hbar} S_{eff}(g,j)
      \right)
      {\, \atop \,}
    \right\rangle
    \\
    & =
    e^{\tfrac{1}{i \hbar} \langle S_{eff}(g,j) \rangle}
  \end{aligned}
  \,.
$$

Conversely the [[vacuum expectation value]] of the [[effective action]] is to the [[logarithm]] of that of the S-matrix:

$$
  \left\langle
    S_{eff}(g,j)
  \right\rangle
  \;=\;
  i \hbar
  \,
  \ln
  \left\langle
    \mathcal{S}(g S_{int} + j A)
  \right\rangle
  \,.
$$

=--


+-- {: .proof}
###### Proof

By lemma \ref{MultiplicativeFeynmanAmplitudes} the summands in the $n$th pointwise power of $\frac{1}{i \hbar}$ times the effective action are precisely the Feynman amplitudes $\Gamma\left((g S_{int} + j A)_{i = 1}^{\nu(\Gamma)}\right)$ of [[finite multigraphs]] $\Gamma$ with $n$ [[connected components]], where each such appears with multiplicity given by the [[factorial]] of $n$:

$$
  \frac{1}{n!}
  \left(
    \frac{1}{i \hbar}
    S_{eff}(g,j)
  \right)^n
  \;=\;
  \underset{
     { \Gamma = \underoverset{j = 1}{n}{\sqcup} \Gamma_j }
     \atop
     { \Gamma_j \in \mathcal{G}_{conn} }
  }{\sum}
  \Gamma\left( (g S_{int} + j A)_{i = 1}^{\nu(\Gamma)} \right)
  \,.
$$

It follows that

$$
  \begin{aligned}
    \exp_\cdot\left(
      \frac{1}{i \hbar} S_{int}
    \right)
    & =
    \underset{n \in \mathbb{N}}{\sum}
    \underset{
       { \Gamma = \underoverset{j = 1}{n}{\sqcup} \Gamma_j }
       \atop
       { \Gamma_j \in \mathcal{G}_{conn} }
    }{\sum}
    \Gamma\left( (g S_{int} + j A)_{i = 1}^{v(\Gamma)} \right)
    \\
    & =
    \underset{\Gamma \in \mathcal{G}}{\sum}
    \Gamma\left( (g S_{int} + j A)_{i = 1}^{v(\Gamma)} \right)
  \end{aligned}
$$

yields the [[Feynman perturbation series]] by expressing it as a series (re-)organized by number of [[connected components]] of the [[Feynman diagrams]].

To conclude the proof it is now sufficient to observe that taking [[vacuum expectation values]] of [[polynomial observables]] respects the pointwise product of observables

$$
  \left\langle A_1 \cdot A_2 \right\rangle
  \;=\;
  \left\langle
    A_1
  \right\rangle
  \,
  \left\langle
    A_2
  \right\rangle
  \,.
$$

This is because the [[Hadamard vacuum state]] $\langle -\rangle \colon PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]  \to \mathbb{C}[ [\hbar, g, j ] ]$ simply picks the zero-order monomial term, by [this prop.](Wick+algebra#WickAlgebraCanonicalState),
and under multiplication of polynomials the zero-order terms are multiplied.

=--

This immediately implies the following important fact:

+-- {: .num_prop #EffectiveActionIsGeneratingFunction}
###### Proposition
**(in [[vacuum stability|stable vacuum]] the [[effective action]] is [[generating function]] for [[vacuum expectation values]] of [[interacting field observables]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, and let $g S_{int} + j A \;\in\; LocObs(E_{\text{BV-BRST}})[ [ \hbar , g , j] ]\langle g,j \rangle$
be a [[local observable]] regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

If the given [[vacuum state]] is [[vacuum stability|stable]] (def. \ref{VacuumStability}) then the [[vacuum expectation value]] $\langle S_{eff}(g,j)\rangle$ of the [[effective action]] (def. \ref{InPerturbationTheoryActionEffective}) is the generating function for the [[vacuum expectation value]] of the [[interacting field observable]] $A_{int}$ (def. \ref{InteractingFieldObservables}) in that 

$$
  \left\langle
    A_{int}
  \right\rangle
  \;=\;
  \frac{d}{d j}
  S_{eff}(g,j)\vert_{j = 0}
  \,.
$$

=--

+-- {: .proof}
###### Proof

We compute as follows:

$$
  \begin{aligned}
    \frac{d}{d j}
    S_{eff}(g,j)
    & =
    i \hbar
    \frac{d}{d j}
    \ln
    \left\langle
      \mathcal{S}(g S_{int} + j A)
    \right\rangle
    \vert_{j = 0}
    \\
    & =
    i \hbar    
    \left\langle
      \mathcal{S}(g S_{int})
    \right\rangle^{-1}
    \frac{d}{d j}
    \left\langle
      \mathcal{S}(g S_{int} + j A)
    \right\rangle
    \vert_{j = 0}
    \\
    & =
    \left\langle
      \frac{d}{d j}
      \underset{ \mathcal{Z}(j A) }{
      \underbrace{\mathcal{S}(g S_{int})^{-1}
      \mathcal{S}(g S_{int} + j A)
      }}
      \vert_{j = 0}
    \right\rangle
    \\
    & =
    \left\langle 
      A_{int}
    \right\rangle
    \,.
  \end{aligned}
$$

Here in the first step we used prop \ref{LogarithmEffectiveAction}, in the second step we applied the [[chain rule]] of [[differentiation]], in the third step we used the definition of [[vacuum stability]] (def. \ref{VacuumStability}) and in the fourth step we recognized the definition of the [[interacting field observables]] (def. \ref{InteractingFieldObservables}).

=--

+-- {: .num_example #EquationsOfMotionForVacuumExpectationValues}
###### Example
**([[equations of motion]] for [[vacuum expectation values]] of [[interacting field observables]])**

Consider the [[effective action]] (def. \ref{InPerturbationTheoryActionEffective}) for the case that 

$$
  \begin{aligned}
    j A 
    & = 
    \tau{\Sigma}( j_{sw} \phi)
    \\
    & =
    \underset{\Sigma}{\int}  
      j_{sw}(x) \mathbf{\Phi}(x) 
    \, dvol_\Sigma(x)
  \end{aligned}
$$ 

is a [[regular polynomial observable|regular]] [[linear observable]] ([this def.](A+first+idea+of+quantum+field+theory#RegularLinearFieldObservables)), hence the smearing of a [[field observable]] ([this def.](A+first+idea+of+quantum+field+theory#PointEvaluationObservables)) by an [[adiabatic switching]] of the [[source field]]

$$
  j_{sw} \;\in\; C^\infty_{cp}(\Sigma) \langle j\rangle
  \,.
$$

(Here we are notationally suppressing internal field indices, for convenience.)

In this case the [[vacuum expectation value]] of the corresponding [[effective action]] is often denoted 

$$
  W(j_{sw})
$$ 

and regarded as a functional of the [[adiabatic switching]] $j_{sw}$ of the [[source field]].

In this case prop. \ref{EffectiveActionIsGeneratingFunction} says that if the [[vacuum state]] is [[vacuum stability|stable]], then  $W$ is the [[generating functional]] for [[interacting field observables|interacting]] (def. \ref{InteractingFieldObservables}) [[field observables]] ([this def.](A+first+idea+of+quantum+field+theory#PointEvaluationObservables)) in that

$$
  \label{WFunctionalDerivative}
  \left\langle 
    \mathbf{\Phi}(x)_{int} 
  \right\rangle
  \;=\;
  \frac{\delta}{\delta j_{sw}(x)}
  W(j_{sw} = 0)
  \,.
$$

Assume then that there exists a corresponding functional of the [[field histories]] $\Gamma(\Phi)$, which behaves like a functional [[Legendre transform]] of $W$ in that it satisfies the functional version of the defining equation of Legendre transforms (first derivatives are [[inverse functions]] of each other, see [this equation](Legendre+transformation#eq:DerivativesOfLegendreTransformsAreInverseFunctions)), in that

$$
 \frac{\delta }{\delta \Phi(x)}
 \Gamma
  \left(
      \frac{\delta}{\delta j_{sw}(y)} W
  \right)
  \;=\;
  \delta(x,y) j_{sw}(x)
  \,.
$$

By (eq:WFunctionalDerivative) this implies that

$$
 \frac{\delta }{\delta \Phi(x)}
 \Gamma
  \left(
    \left\langle \mathbf{\Phi}(x)_{int} \right\rangle  \right)
  \;=\;
  0
  \,.
$$  

This may be read as a quantum version of the [[principle of extremal action]] ([this prop.](A+first+idea+of+quantum+field+theory#PrincipleOfExtremalAction))
formulated now not for the [[field histories]] $\Phi(x)$, but for the [[vacuum expectation values]] $\langle \mathbf{\Phi}(x)_{int}\rangle$ of their corresponding [[interacting quantum field observables]].

Beware, (as in remark \ref{TerminologyForEffectiveAction}) that many texts refer to $\Gamma(\Phi)$ as the _effective action_, instead of its [[Legendre transform]], the generating functional $W(j_{sw})$. 

=--


The perspective of the [[effective action]] also gives a transparent picture of the order of quantum effects involved in the
[[S-matrix]], this is prop. \ref{FeynmanDiagramLoopOrder} below. In order to state this conveniently, we invoke
two basic concepts from [[graph theory]]:

+-- {: .num_defn #GraphPlanar}
###### Definition
**([[planar graphs]] and [[trees]])**

A [[finite multigraph]] (def. \ref{Graphs}) is called a _[[planar graph]]_ if it
admits an [[embedding]] into the [[plane]], hence if it may be "drawn into the plane" without intersections, in the evident way.

A [[finite multigraph]] is called a _[[tree]]_ if for any two of its [[vertices]]
there is at most one [[path]] of [[edges]] connecting them, these are examples of planar graphs. We write

$$
  \mathcal{G}_{tree}
    \subset
  \mathcal{G}
$$

for the [[subset]] of [[isomorphism classes]] of [[finite multigraphs]] with [[linear order|linearly orrdered]] [[vertices]] (def. \ref{Graphs})
on those which are [[trees]].

=--


+-- {: .num_prop #FeynmanDiagramLoopOrder}
###### Proposition
**([[loop order]] and [[tree level]] of [[Feynman perturbation series]])**

The [[effective action]] (def. \ref{InPerturbationTheoryActionEffective}) contains no negative powers of $\hbar$, hence is indeed
a [[formal power series]] also in $\hbar$:

$$
  S_{eff}(g,j)
  \;\in\;
  PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]
  \,.
$$

and in particular

$$
  \left\langle
    S_{eff}(g,j)
  \right\rangle
  \;\in\;
  \mathbb{C}[ [ \hbar, g, j] ]
  \,.
$$

Moreover, the contribution to the effective action in the [[classical limit]] $\hbar \to 0$
is precisely that of [[Feynman amplitudes]] of those [[finite multigraphs]] (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}) which are [[trees]] (def. \ref{GraphPlanar}); thus called the _[[tree level]]_-contribution:

$$
  S_{eff}(g,j)\vert_{\hbar = 0}
  \;=\;
  i \hbar
  \underset{\Gamma \in \mathcal{G}_{conn} \cap \mathcal{G}_{tree}}{\sum}
  \Gamma\left( (g S_{int} + j A)_{i = 1}^{\nu(\Gamma)} \right)
  \,.
$$

Finally, a [[finite multigraph]] $\Gamma$ (def. \ref{Graphs}) which is [[planar graph|planar]] (def. \ref{GraphPlanar}) and [[connected graph|connected]] (def. \ref{ConnectedGraphs}) contributes to the effective action
precisely at order

$$
  \hbar^{L(\Gamma)}
  \,,
$$

where $L(\Gamma) \in \mathbb{N}$ is the number of _[[faces]]_ of $\Gamma$, here called the _number of loops_ of the diagram;
here usually called the _[[loop order]]_ of $\Gamma$.

(Beware the terminology clash with [[graph theory]], see the discussion of [[tadpoles]] in remark \ref{Tadpoles}.)

=--

+-- {: .proof}
###### Proof


By def. \ref{LagrangianFieldTheoryPerturbativeScattering} the explicit $\hbar$-dependence of the [[S-matrix]] is

$$
  \mathcal{S}
  \left(
    S_{int}
  \right)
  \;=\;
  \underset{k \in \mathbb{N}}{\sum}
    \frac{1}{k!}
    \frac{1}{(i \hbar)^k}
    T( \underset{k \, \text{factors}}{\underbrace{S_{int}, \cdots,  S_{int}}} )
$$

and by prop. \ref{TimeOrderedProductAwayFromDiagonal} the further $\hbar$-dependence of the [[time-ordered product]] $T(\cdots)$ is

$$
  T(S_{int}, S_{int})
  \;=\;
  prod \circ
  \exp\left(
    \hbar
    \left\langle
      \Delta_F,
      \frac{\delta}{\delta \mathbf{\Phi}}
        \otimes
      \frac{\delta}{\delta \mathbf{\Phi}}
    \right\rangle
  \right)
 ( S_{int} \otimes S_{int} )
  \,,
$$

By the [[Feynman rules]] (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}) this means that

1. each [[vertex]] of a Feynman diagram contributes a power $\hbar^{-1}$ to its Feynman amplitude;

1. each [[edge]] of a Feynman diagram contributes a power $\hbar^{+1}$ to its Feynman amplitude.

If we write

$$
  E(\Gamma), V(\Gamma) \;\in\; \mathbb{N}
$$

for the total number of [[vertices]] and [[edges]], respectively, in $\Gamma$, this means that a Feynman amplitude
corresponding to some $\Gamma \in \mathcal{G}$ contributes precisely at order

$$
  \label{GeneralFeynmanDiagramhbarContribution}
  \hbar^{E(\Gamma) - V(\Gamma)}
  \,.
$$

So far this holds for arbitrary $\Gamma$. If however $\Gamma$ is [[connected graph|connected]] (def. \ref{ConnectedGraphs}) and [[planar graph|planar]] (def. \ref{GraphPlanar}), then _[[Euler's formula]]_ asserts that

$$
  \label{ConnectedPlanarGraphEulerCharacteristic}
  E(\Gamma) - V(\Gamma)
  \;=\;
  L(\Gamma) - 1
  \,.
$$

Hence $\hbar^{L(\Gamma)- 1}$ is the order of $\hbar$ at which $\Gamma$ contributes to the [[scattering matrix]] expressed as the [[Feynman perturbation series]].

But the [[effective action]], by definition (eq:ExpansionEffectiveAction), has the same contributions
of Feynman amplitudes, but multiplied by another power of $\hbar^1$, hence it contributes at order

$$
  \hbar^{E(\Gamma) - V(\Gamma) + 1} = \hbar^{L(\Gamma)}
  \,.
$$

This proves the second claim on [[loop order]].

The first claim, due to the extra factor of $\hbar$ in the definition of the effective action, is equivalent to saying
that the Feynman amplitude of every [[connected graph|connected]] [[finite multigraph]]
contributes powers in $\hbar$ of order $\geq -1$ and contributes at order $\hbar^{-1}$ precisely if the graph is a tree.

Observe that a [[connected graph|connected]] [[finite multigraph]] $\Gamma$ with $\nu \in \mathbb{N}$ vertices (necessarily $\nu \geq 1$) has at least $\nu-1$ edges and precisely $\nu - 1$ edges if it is a tree.

To see this, consecutively remove edges from $\Gamma$ as long as possible while retaining connectivity. When this process stops, the result must be a connected tree $\Gamma'$, hence a [[connected graph|connected]] [[planar graph]] with $L(\Gamma') = 0$. Therefore [[Euler's formula]] (eq:ConnectedPlanarGraphEulerCharacteristic) implies that that $E(\Gamma') = V(\Gamma') -1$.

This means that the connected multigraph $\Gamma$ in general has a Feynman amplitude of order

$$
  \hbar^{E(\Gamma) - V(\Gamma)}
  =
  \hbar^{ \overset{\geq 0}{\overbrace{E(\Gamma) - E(\Gamma')}} + \overset{= -1}{\overbrace{E(\Gamma') - V(\Gamma)}}  }
$$

and precisely if it is a tree its Feynman amplitude is of order $\hbar^{-1}$.

=--

$\,$


#### Vacuum diagrams
 {#VacuumDiagrams}

With the [[Feynman perturbation series]] and the [[effective action]] in hand, it is now immediate to see that there
is a general contribution by [[vacuum diagrams]] (def. \ref{VacuumDiagram} below) in the [[scattering matrix]] which,
in a [[vacuum stability|stable vacuum state]],
cancels out against the prefactor $\mathcal{S}(g S_{int})$ in [[Bogoliubov's formula]] for [[interacting field observables]].


+-- {: .num_defn #VacuumDiagram}
###### Definition
**([[vacuum diagrams]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, and let $g S_{int} + j A \;\in\; LocObs(E_{\text{BV-BRST}})[ [ \hbar , g , j] ]\langle g,j \rangle$
be a [[local observable]] regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]],
and consider a choice of decomposition for field species and interaction vertices according to def. \ref{VerticesAndFieldSpecies}.

Then a [[Feynman diagram]] all whose vertices are internal vertices (def. \ref{FeynmanDiagram})
is called a _[[vacuum diagram]]_.

Write

$$
  \mathcal{G}^{Feyn}_{vac}
   \subset
  \mathcal{G}^{Feyn}
$$

for the subset of [[isomorphism classes]] of vacuum diagrams among the set of isomorphism classes of all Feynman diagrams, def. \ref{FeynmanDiagram}. Similarly write

$$
  \mathcal{G}^{Feyn}_{conn,vac}
  \;\coloneqq\;
  \mathcal{G}^{Feyn}_{conn}
    \cap
  \mathcal{G}^{Feyn}_{vac}
  \;\subset\;
  \mathcal{G}^{Feyn}
$$

for the subset of [[isomorphism classes]] of Feynman diagrams which are both vacuum diagrams as well as [[connected graphs]] (def. \ref{ConnectedGraphs}).

Finally write

$$
  S_{eff,vac}(g)
  \;\coloneqq\;
  \underset{ { (\Gamma,vertlab,edgelab) } \atop { \in \mathcal{G}_{conn,vac} } }{\sum}
  (\Gamma,vertlab, edgelab)(g S_{int})
  \;\in\;
  PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar , g ] ]
$$

for the sub-series of that for the [[effective action]] (def. \ref{InPerturbationTheoryActionEffective}) given
only by those connected diagrams which are also vacuum diagrams.

=--

+-- {: .num_example}
###### Example
**(2-vertex [[vacuum diagram]] in [[QED]])**

The [[vacuum diagram]] (def. \ref{VacuumDiagram}) with two [[electron-photon interaction]]-vertices in [[quantum electrodynamics]] ([this example.](A+first+idea+of+quantum+field+theory#LagrangianQED)) is:

<center>
<img src="https://ncatlab.org/nlab/files/QEDVacuumDiagram.png" width="200">
</center>

=--

+-- {: .num_example #SMatrixVacuumContribution}
###### Example
**([[vacuum diagram]]-contribution to [[S-matrices]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, and let $g S_{int} + j A \;\in\; LocObs(E_{\text{BV-BRST}})[ [ \hbar , g , j] ]\langle g,j \rangle$
be a [[local observable]] regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]],
and consider a choice of decomposition for field species and interaction vertices according to def. \ref{VerticesAndFieldSpecies}.

Then the [[Feynman perturbation series]]-expansion of the [[S-matrix]] (example \ref{FeynmanPerturbationSeries})
of the [[interaction]]-term $g S_{int}$ alone (no [[source field]]-contribution) is the series of [[Feynman amplitudes]] that are labeled by [[vacuum diagrams]] (def. \ref{VacuumDiagram}), hence (by prop. \ref{LogarithmEffectiveAction}) the exponential of the
vacuum [[effective action]] $S_{eff,vac}$ (def. \ref{VacuumDiagram}):

$$
  \begin{aligned}
    \mathcal{S}(g S_{int})
    & =
    \exp_\cdot\left( \tfrac{1}{i \hbar} S_{eff,vac}(g,j) \right)
    \\
    & =
    \underset{\Gamma \in \mathcal{G}_{vac}}{\sum}
      \Gamma\left(g S_{int}\right)
  \end{aligned}
  \,.
$$

More generally, the S-matrix with [[source field]]-contribution $j A$ included always splits as a
_pointwise_ product of the vacuum S_matrix with the [[Feynman perturbation series]] over all [[Feynman graphs]] with at least
one external vertex:

$$
  \begin{aligned}
  \mathcal{S}(g S_{int} + j A)
  \;=\;
  \mathcal{S}(g S_{int})
  \cdot
  \underset{
    \text{Feynman perturbation series}
    \atop
    \text{over diagrams with at least one external vertex}
  }{
   \underbrace{
     \exp_\cdot
     \left(
       \tfrac{1}{i \hbar} \left( S_{eff}(g,j) - S_{eff,vac}(g) \right)
     \right)
   }
  }
  \,,
  \end{aligned}
$$

Hence if the [[free field]] [[vacuum state]] is stable with respect to the interaction $g S_{int}$, according to def. \ref{VacuumStability}, then the [[vacuum expectation value]] of a [[time-ordered product]] of [[interacting field observables]] $j (A_i)_{int}$ (example \ref{InteractinFieldTimeOrderedProduct}) and hence in particular of [[scattering amplitudes]] (example \ref{ScatteringAmplitudeFromInteractingFieldObservables}) is
given by the [[Feynman perturbation series]] (example \ref{FeynmanPerturbationSeries}) over
just the non-vacuum [[Feynman diagrams]], hence over all those diagram that have at least one one external vertex

$$
  \begin{aligned}
  &
  \left(
    {\, \atop \,}
    supp(A_1)
      {\vee\!\!\!\wedge}
    supp(A_2)
      {\vee\!\!\!\wedge}
      \cdots
      {\vee\!\!\!\wedge}
    supp(A_n)
    {\, \atop \,}
  \right)
  \\
  & \Rightarrow
  \left\langle
    {\, \atop \,}
    (A_1)_int
    (A_2)_{int}
      \cdots
    (A_n)_{int}
    {\, \atop \,}
  \right\rangle
  \;=\;
  \frac{d^n}{ d j_1 \cdots d j_n}
  \left(
    \underset{\Gamma \in \mathcal{G} \setminus \mathcal{G}_{vac}   }{\sum}
    \Gamma(g S_{int} + \sum_i j_i A_i)
  \right)_{
    \vert j_1, \cdots, j_n = 0
  }
  \,.
  \end{aligned}
$$

This is the way in which the [[Feynman perturbation series]] is used in practice for computing [[scattering amplitudes]].

=--

$\,$

#### Interacting quantum BV-Differential
 {#InteractingQantumBVDifferential}

So far we have discussed, starting with a [[BV-BRST formalism|BV-BRST]] [[gauge fixing|gauge fixed]] [[free field]] [[vacuum]],
the perturbative construction of [[interacting field algebras of observables]] (def. \ref{QuntumMollerOperator}) and their organization
in increasing powers of $\hbar$ and $g$ ([[loop order]], prop. \ref{FeynmanDiagramLoopOrder}) via the [[Feynman perturbation series]] (example \ref{FeynmanPerturbationSeries}, example \ref{SMatrixVacuumContribution}).

But this [[interacting field algebra of observables]] still involves all the [[auxiliary fields]] of the [[BV-BRST formalism|BV-BRST]] [[gauge fixing|gauge fixed]] [[free field]] [[vacuum]] (as in example \ref{FieldSpeciesQED} for QED), while the
actual physical [[gauge invariance|gauge invariant]] [[on-shell]] observables should be (just) the [[cochain cohomology]] of the
[[BV-BRST differential]] on this enlarged space of observables. Hence for the construction of [[perturbative QFT]] to conclude,
it remains to pass the [[BV-BRST differential]] of the [[free field]] [[Wick algebra]] of observables to
a [[differential]] on the [[interacting field algebra]], such that its [[cochain cohomology]] is well defined.

Since the [[time-ordered products]] away from coinciding interaction points and as well as on [[regular polynomial observables]] are uniquely fixed
(prop. \ref{TimeOrderedProductAwayFromDiagonal}), one finds that also this _interacting quantum BV-differential_
is uniquely fixed, on [[regular polynomial observables]], by [[conjugation]] with the [[quantum Møller operators]] (def. \ref{BVDifferentialInteractingQuantum}).
The formula that characterizes it there is called the _[[quantum master equation]]_ or equivalently the _[[quantum master Ward identity]]_ (prop. \ref{QuantumMasterEquation} below).

When [[extension of distributions|extending]] to coinciding interaction points via [[renormalization|("re"-)normalization]] (def. \ref{ExtensionOfTimeOrderedProoductsRenormalization}) these identities are not guaranteed to hold anymore, but may
be imposed as [[renormalization conditions]] (def. \ref{RenormalizationConditions}, prop. \ref{BasicConditionsRenormalization}).
Quantum correction to the [[master Ward identity]] then imply corrections to [[Noether's theorem|Noether current]] [[conserved current|conservation laws]]; this we discuss [below](#WardIdentities).



$\,$


Recall how the global BV-differential

$$
  \{S',-\}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
$$

on [[regular polynomial observables]] ([this def.](A+first+idea+of+quantum+field+theory#BVDifferentialGlobal)) is conjugated into the [[time-ordered product]] via the time ordering operator
$\mathcal{T} \circ \{-S',-\} \circ \mathcal{T}^{-}$ ([this prop.](BV-operator#GaugeFixedActionFunctionalTimeOrderedAntibracket)).

In the same way we may use the [[quantum Møller operators]] to conjugate the BV-differential into the regular part of the [[interacting field algebra of observables]]:

+-- {: .num_defn #BVDifferentialInteractingQuantum}
###### Definition
**(interacting quantum [[BV-differential]])**

Given an [[adiabatic switching|adiabatically switched]] non-point-[[interaction]] [[action functional]] in the form of a [[regular polynomial observable]] $S_{int}$,
then the _interacting quantum BV-differential_ on the [[interacting field algebra]] (def. \ref{FieldAlgebraObservablesInteracting})
on [[regular polynomial observables]] is the [[conjugation]] of the plain [[BV-differential]] $\{-S',-\}$ by the [[quantum Møller operator]] induced by $S_{int}$ (def. \ref{MollerOperatorOnRegularPolynomialObservables}):

$$
  \mathcal{R} \circ \{-S', (-)\} \circ \mathcal{R}^{-1}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
  \,.
$$

=--

([Rejzner 11, (5.38)](quantum+master+equation#Rejzner11))


+-- {: .num_prop #QuantumMasterEquation}
###### Proposition
**([[quantum master equation]] and [[quantum master Ward identity]] on [[regular polynomial observables]])**

Consider an [[adiabatic switching|adiabatically switched]] non-point-[[interaction]] [[action functional]] in the form of a [[regular polynomial observable]] in degree 0

$$
  S_{int}
  \;\in\;
  PolyObs(E_{\text{BV-BRST}})_{{reg} \atop {deg = 0}}[ [\hbar] ]
  \,,
$$

Then the following are equivalent:

1. The _[[quantum master equation]]_ (QME)

   $$
     \label{OnRegularObservablesQuantumMasterEquation}
      \tfrac{1}{2} \{ S' + S_{int}, S' + S_{int} \}_{\mathcal{T}}
      +
      i \hbar  \Delta_{BV}( S' + S_{int} )
     \;=\;
     0
     \,.
   $$


1. The  [[perturbative S-matrix]] (def. \ref{OnRegularObservablesPerturbativeSMatrix}) is $BV$-closed

   $$
     \{-S', \mathcal{S}(S_{int})\} = 0
     \,.
   $$

1. The quantum _[[master Ward identity]]_ (MWI) on [[regular polynomial observables]] _in terms of [[retarded products]]_:

   $$
     \label{OnRegularObservablesQuantumMasterWardIdentity}
     \mathcal{R} \circ \{-S',(-)\} \circ \mathcal{R}^{-1}
     \;=\;
     -
     \left(
       \left\{ S' + S_{int} \,,\, (-) \right\}_{\mathcal{T}}
       + i \hbar   \Delta_{BV}
     \right)
   $$

   ([Dütsch 18, (4.2)](Ward+identity#Duetsch18))

   expressing the interacting quantum [[BV-differential]] (def. \ref{BVDifferentialInteractingQuantum}) as the sum of the [[time-ordered product|time-ordered]] [[antibracket]] ([this def.](BV-operator#AntibracketTimeOrdered)) with the _total_ [[action functional]] $S' + S_{int}$ and $i \hbar$ times the [[BV-operator]] ([BV-operator](BV-operator#ForGaugeFixedFreeLagrangianFieldTheoryBVOperator)).

1. The quantum _[[master Ward identity]]_ (MWI) on [[regular polynomial observables]] _in terms of [[time-ordered products]]_:

   $$
     \label{OnRegularObservablesQuantumMasterWardIdentityViaTimeOrdered}
     \mathcal{S}(-S_{int})
       \star_F
     \{-S', \mathcal{S}(S_{int}) \star_F  (-)\}
     \;=\;
     -
     \left(
       \left\{ S' + S_{int} \,,\, (-) \right\}_{\mathcal{T}}
       + i \hbar   \Delta_{BV}
     \right)
   $$

   ([Dütsch 18, (4.8)](Ward+identity#Duetsch18))

=--

([Rejzner 11, (5.35) - (5.38)](quantum+master+equation#Rejzner11), following [Hollands 07, (342)-(345)](Ward+identity#Hollands07))


+-- {: .proof}
###### Proof

To see that the first two conditions are equivalent, we compute as follows

$$
  \label{QuantumMasterOnRegularObservablesBVDifferentialOfSMatrixInTerms}
  \begin{aligned}
    \left\{
      -S',  \mathcal{S}(S_{int})
    \right\}
    & =
    \left\{
      -S'
      ,
      \exp_{\mathcal{T}}
      \left(
        \tfrac{1}{i \hbar} S_{int}
      \right)
    \right\}
    \\
    & =
    \underset{
      {
        \tfrac{-1}{i \hbar} \{S',S\}_{\mathcal{T}}
      }
      \atop
      {
        \star_F
        \exp_{\mathcal{T}}
        \left(
          \tfrac{1}{i \hbar} S_{int}
        \right)
      }
    }{
    \underbrace{
    \left\{
      -S'
      ,
      \exp_{\mathcal{T}}
      \left(
        \tfrac{1}{i \hbar} S_{int}
      \right)
    \right\}_{\mathcal{T}}
    }
    }
    -
    i \hbar
    \underset{
      {
        \left(
          \tfrac{1}{i \hbar}
          \Delta_{BV}(S_{int})
          +
          \tfrac{1}{2 (i \hbar)^2}
          \left\{
            S_{int}, S_{int}
          \right\}_{\mathcal{T}}
        \right)
      }
      \atop
      {
        \star_{F}
        \exp_{\mathcal{T}}
        \left(
          \tfrac{1}{i \hbar}
          S_{int}
        \right)
      }
    }{
    \underbrace{
    \Delta_{BV}
    \left(
      \exp_{\mathcal{T}}
      \left(
        \tfrac{1}{i \hbar} S_{int}
      \right)
    \right)
    }
    }
    \\
    & =
    \tfrac{-1}{i \hbar}
    \underset{ \text{QME} }{
    \underbrace{
    \left(
      \{S',S_{int}\}
      +
      \tfrac{1}{2}\{S_{int}, S_{int}\}
      +
      i \hbar \Delta_{BV}(S_{int})
    \right)
    }
    }
      \star_F
    \exp_{\mathcal{T}}
    \left(
      \tfrac{1}{i \hbar}
      S_{int}
    \right)
  \end{aligned}
$$

Here in the first step we used the definition of the [[BV-operator]] ([this def.](A+first+idea+of+quantum+field+theory#ForGaugeFixedFreeLagrangianFieldTheoryBVOperator)) to rewrite the plain antibracket in terms of the time-ordered antibracket ([this def.](BV-operator#AntibracketTimeOrdered)), then under the second brace we used that the time-ordered antibracket is the failure of the BV-operator to be a derivation ([this prop](BV-operator#AntibracketBVOperatorRelation)) and under the first brace the consequence of this statement for application to exponentials ([this example](BV-operator#TimeOrderedExponentialBVOperator)). Finally we collected terms, and to "complete the square" we added the terms on the left of

$$
  \frac{1}{2} \underset{= 0}{\underbrace{\{S', S'\}_{\mathcal{T}}}}
  -
  i \hbar \underset{ = 0}{\underbrace{ \Delta_{BV}(S')}} = 0
$$

which vanish because, by definition of [[gauge fixing]] ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)), the free gauge-fixed action functional $S'$ is independent of [[antifields]].

But since the operation $(-) \star_F \exp_{\mathcal{T}}\left( \tfrac{1}{i \hbar} S_{int} \right)$ has the [[inverse]] $(-) \star_F \exp_{\mathcal{T}}\left( \tfrac{-1}{i \hbar}  S_{int} \right)$, this implies the claim.

Next we show that the [[quantum master equation]] implies the [[quantum master Ward identities]].

We use that the BV-differential $\{-S',-\}$ is a [[derivation]] of the [[Wick algebra]] product $\star_H$ (lemma \ref{DerivationBVDifferentialForWickAlgebra}).

First of all this implies that with $\{-S', \mathcal{S}(S_{int})\} = 0$ also
$\{-S', \mathcal{S}(S_{int})^{-1}\} = 0$.

Thus we compute as follows:

$$
  \begin{aligned}
    \{-S', -\} \circ \mathcal{R}^{-1}(A)
    & =
    \{-S', \mathcal{R}^{-1}(A)\}
    \\
    & =
    \left\{
      { \, \atop \, }
      -S',
      \mathcal{S}(S_{int})^{-1}
        \star_H
      \left( \mathcal{S}(S_{int}) \star_F a \right)
      {\, \atop \,}
    \right\}
    \\
    & = \phantom{+}
    \underset{
      = 0
    }{
    \underbrace{
    \left\{
      -S', \mathcal{S}(S_{int})^{-1}
    \right\}
    }
    }
      \star_H
    \left(
      \mathcal{S}(S_{int}) \star_F A
    \right)
    \\
    & \phantom{=}
    +
    \mathcal{S}(S_{int})^{-1}
      \star_H
    \left\{
      -S',
      \mathcal{S}(S_{int}) \star_F A
    \right\}
    \\
    & =
    \mathcal{S}(S_{int})^{-1}
      \star_H
    \left(
      \underset{
        = 1
      }{
      \underbrace{
        \mathcal{S}(+ S_{int})
          \star_F
        \mathcal{S}(- S_{int})
      }
      }
        \star_F
      \left\{
        -S',
        \mathcal{S}(S_{int}) \star_F A
      \right\}
   \right)
   \\
   & =
    \mathcal{S}(S_{int})^{-1}
      \star_H
    \left(
      \mathcal{S}(+ S_{int})
        \star_F
      \underset{ (\ast) }{
      \underbrace{
        \mathcal{S}(- S_{int})
          \star_F
        \left\{
          -S',
          \mathcal{S}(S_{int}) \star_F A
        \right\}
     }
     }
   \right)
   \\
   & =
   \mathcal{R}^{-1}
   \left(
     \underset{ (\ast) }{
     \underbrace{
       \phantom{\, \atop \,}
       \mathcal{S}(-S_{int})
         \star_F
       \left\{
         -S',
         \mathcal{S}(S_{int}) \star_F A
       \right\}
       }
       }
   \right)
  \end{aligned}
$$

By applying $\mathcal{R}$ to both sides of this equation, this means
first of all that the interacting quantum BV-differential
is equivalently given by

$$
  \mathcal{R} \circ \{-S', (-)\} \circ \mathcal{R}^{-1}
  \;=\;
  \mathcal{S}(-S_{int}) \star_F \{-S', \mathcal{S}(S_{int}) \star_F  (-)\}
  \,,
$$

hence that if either version (eq:OnRegularObservablesQuantumMasterWardIdentity) or (eq:OnRegularObservablesQuantumMasterWardIdentityViaTimeOrdered)  of the [[master Ward identity]] holds, it implies the other.

Now expanding out the definition of $\mathcal{S}$ (def. \ref{OnRegularObservablesPerturbativeSMatrix}) and expressing $\{-S',-\}$ via the [[time-ordered product|time-ordered]] [[antibracket]] ([this def.](BV-operator#AntibracketTimeOrdered)) and the [[BV-operator]] $\Delta_{BV}$ ([this prop.](BV-operator#ForGaugeFixedFreeLagrangianFieldTheoryBVOperator)) as

$$
  \{-S',-\}
  \;=\;
  \{-S',-\}_{\mathcal{T}} - i \hbar \Delta_{BV}
$$

(on [[regular polynomial observables]]), we continue computing as follows:

$$
  \label{QMESecondStep}
  \begin{aligned}
    & \mathcal{R} \circ \{-S', (-)\} \circ \mathcal{R}^{-1}( A )
    \\
    & =
   \exp_{\mathcal{T}}
    \left(
      \tfrac{-1}{i \hbar} S_{int}
    \right)
      \star_F
    \left\{
      -S',
      \exp_{\mathcal{T}}
      \left(
         \tfrac{1}{i \hbar} S_{int}
      \right)
        \star_F
      A
    \right\}
    \\
    & =
    \exp_{\mathcal{T}}
    \left(
      \tfrac{-1}{i \hbar}
        S_{int}
    \right)
      \star_F
    \left(
      \left\{
        -S',
        \exp_{\mathcal{T}}
        \left(
          \tfrac{ 1 }{i \hbar} S_{int}
        \right)
          \star_F
        A
      \right\}_{\mathcal{T}}
      -
      i \hbar
      \Delta_{BV}
      \left(
        \exp_{\mathcal{T}}
        \left(
           \tfrac{ 1 }{i \hbar} S_{int}
        \right)
          \star_F
        A
      \right)
    \right)
    \\
    &
    \phantom{+}
    =
    \tfrac{1}{i \hbar} \{ -S', S_{int}  \}_{\mathcal{T}} \star_F   A
    +
    \{-S', A\}_{\mathcal{T}}
    \\
    &
    \phantom{=}
    -
    i \hbar
    \exp_{\mathcal{T}}\left( \tfrac{-1}{i \hbar} S_{int}\right)
    \star_F
    \left(
      \underset{
        {
          \left(
          \tfrac{1}{i \hbar}\Delta_{BV}(S_{int})
          +
          \tfrac{1}{2 (i \hbar)^2} \left\{ S_{int}, S_{int} \right\}
          \right)
        }
        \atop
        {
          \star_F \exp_{\mathcal{T}}\left( \tfrac{ 1 }{i \hbar} S_{int} \right)
        }
      }{
      \underbrace{
        \Delta_{BV}
        \left(
          \exp_{\mathcal{T}}
          \left(
            \tfrac{ 1}{i \hbar} S_{int}
          \right)
        \right)
      }
      }
      \star_F A
      \,+\,
       \exp_{\mathcal{T}}
       \left(
         \tfrac{ 1}{i \hbar} S_{int}
       \right)
       \star_F
       \Delta_{BV}(A)
       \,+\,
       \underset{
         {
           \exp_{\mathcal{T}}\left( \tfrac{1}{i \hbar} S_{int} \right)
         }
         \atop
         {
           \star_F
           \tfrac{ 1}{i \hbar}
           \{S_{int}, A\}
         }
       }{
       \underbrace{
         \left\{
           \exp_{\mathcal{T}}
           \left(
             \tfrac{ 1}{i \hbar} S_{int}
           \right)
           \,,\,
           A
         \right\}_{\mathcal{T}}
      }
      }
    \right)
    \\
    & =
    -
    \left(
      \{ S' + S_{int}\,,\, A\}_{\mathcal{T}}
        +
      i \hbar \Delta_{BV}(A)
    \right)
    \\
    & \phantom{=}
    -
    \tfrac{1}{i \hbar}
    \underset{ \text{QME} }{
    \underbrace{
    \left(
      \tfrac{1}{2} \{ S' + S_{int}, S' + S_{int} \}_{\mathcal{T}}
      +
      i \hbar  \Delta_{BV}( S' + S_{int} )
    \right)
    }}
      \star_F A
    \\
    & =
    -
    \left(
      \{ S' + S_{int}\,,\, A\}_{\mathcal{T}}
        +
      i \hbar \Delta_{BV}(A)
    \right)
  \end{aligned}
$$

Here in the line with the braces we used that the [[BV-operator]] is a [[derivation]] of the [[time-ordered product]] up to correction by the time-ordered [[antibracket]] ([this prop.](BV-operator#AntibracketBVOperatorRelation)), and under the first brace we used the effect of that property on time-ordered exponentials ([this example](BV-operator#TimeOrderedExponentialBVOperator)), while under the second brace we used that $\{(-),A\}_{\mathcal{T}}$ is a derivation of the time-ordered product. Finally we have collected terms, added $0 = \{S',S'\} + i \hbar \Delta_{BV}(S')$ as before, and then used the QME.

This shows that the quantum [[master Ward identities]] follow from the [[quantum master equation]]. To conclude, it is now sufficient to show that, conversely, the MWI in terms of, say, retarded products implies the QME.

To see this, observe that with the BV-differential being nilpotent, also its conjugation by $\mathcal{R}$ is, so that with the above we have:

$$
  \begin{aligned}
  & \left( \{-S',-\}\right)^2 = 0
  \\
  \Leftrightarrow
  \;
  &
  \left( \mathcal{R} \circ \{-S',(-)\} \circ \mathcal{R}^{-1} \right)^2 = 0
  \\
  \Leftrightarrow
  \;
  &
  \underset{
    \left\{
      {\, \atop \,}
      \tfrac{1}{2}\{S' + S_{int}, S' + S_{int}\}_{\mathcal{T}}
      +
      i \hbar \Delta_{BV}(S' + S_{int})
      \,,\,
      (-)
    \right\}
  }{
  \underbrace{
    \left(
      \{S' + S_{int}, (-)\}_{\mathcal{T}} + i \hbar \Delta_{BV}
    \right)^2
  }
  } = 0
  \end{aligned}
$$

Here under the brace we computed as follows:

$$
  \begin{aligned}
  \left(
    \{S' + S_{int}, (-)\}_{\mathcal{T}} + i \hbar \Delta_{BV}
  \right)^2
  & =
  \phantom{+}
  \underset{
    \tfrac{1}{2} \{ \{S' + S, S'+ S\}_{\mathcal{T}}, (-) \}_{\mathcal{T}}
  }{
  \underbrace{
    \{S' + S_{int}, \{S' + S_{int}\}_{\mathcal{T}}, (-) \}_{\mathcal{T}}
  }}
  \\
  &
  \phantom{=}
  +
  i \hbar
  \underset{
    \{  \Delta_{BV}(S'+ S)\,,\, (-)  \}_{\mathcal{T}}
  }{
  \underbrace{
  \left(
    \{S' + S_{int}, (-)\}_{\mathcal{T}} \circ \Delta_{BV}
    +
    \Delta_{BV} \circ \{S' + S_{int}, (-)\}_{\mathcal{T}}
  \right)
  }}
  \\
  &
  \phantom{=}
  +
  (i \hbar)^2
   \underset{= 0}
   {
     \underbrace{
       \Delta_{BV} \circ \Delta_{BV}
      }
    }
  \end{aligned}
  \,.
$$

where, in turn, the term under the first brace follows by the graded [[Jacobi identity]], the one under the second brace by Henneaux-Teitelboim (15.105c) and the one under the third brace by Henneaux-Teitelboim (15.105b).

=--

$\,$

#### Ward identities
  {#WardIdentities}

The _[[quantum master Ward identity]]_ (prop. \ref{QuantumMasterEquation}) expresses the relation between the [[quantum field theory|quantum]] (measured by [[Planck's constant]] $\hbar$) [[interacting field theory|interacting]] (measured by the [[coupling constant]] $g$) [[equations of motion]] to the [[classical field theory|classical]] [[free field]] [[equations of motion]] at $\hbar, g\to 0$ (remark \ref{QuantumMasterEuqationRelatesQuantumInteractingELEquationsToClassicalFreeELEquations} below). As such it generalizes the [[Schwinger-Dyson equation]] ([this prop.](A+first+idea+of+quantum+field+theory#DysonSchwinger)), to which it reduces for $g = 0$ (example \ref{QuantumMasterEuqationRelatesQuantumInteractingELEquationsToClassicalFreeELEquations} below) as well as the _classical master Ward identity_, which is the case for $\hbar = 0$ (example \ref{MasterWardIdentityClassical} below).

Applied to products of the [[equations of motion]] with any given [[observable]], the master Ward identity becomes a particular _Ward identity_.

This is of interest notably in view of [[Noether's theorem]] ([this prop.](A+first+idea+of+quantum+field+theory#NoethersFirstTheorem)), which says that every [[infinitesimal symmetry of the Lagrangian]] of, in particular, the given [[free field theory]], corresponds to a [[conserved current]] ([this def.](A+first+idea+of+quantum+field+theory#SymmetriesAndConservedCurrents)), hence a [[horizontal differential form]] whose [[total spacetime derivative]] vanishes up to a term proportional to the [[equations of motion]]. Under [[transgression of variational differential forms|transgression]] to [[local observables]] this is a relation of the form

$$
  div \mathbf{J} = 0 \phantom{AAA} \text{on-shell}
  \,,
$$

where "on shell" means up to the ideal generated by the [[classical field theory|classical]] [[free field theory|free]] [[equations of motion]]. Hence for the case of [[local observables]] of the form $div \mathbf{J}$, the quantum Ward identity expresses the possible failure of the original [[conserved current]] to actually be conserved, due to both quantum effects ($\hbar$) and interactions ($g$). This is the form in which Ward identities are usually understood (example \ref{NoetherCurrentConservationQuantumCorrection} below).

As one [[extension of distributions|extends]] the [[time-ordered products]] to coinciding interaction points in [[renormalization|("re"-)normalization]]
of the [[perturbative QFT]] (def. \ref{ExtensionOfTimeOrderedProoductsRenormalization}), the [[quantum master equation]]/[[master Ward identity]] becomes a _[[renormalization condition]]_ (def. \ref{RenormalizationConditions}, prop. \ref{BasicConditionsRenormalization}). If this condition fails, one speaks of a _[[quantum anomaly]]_. Specifically if the Ward identity for an [[infinitesimal gauge symmetry]] is violated, one speaks of a _[[gauge anomaly]]_.

$\,$


+-- {: .num_defn #OnRegularPolynomialObservablesMasterWardIdentity}
###### Definition

Consider a [[free field theory|free]] [[gauge fixing|gauge fixed]] [[Lagrangian field theory]] $(E_{\text{BV-BRST}}, \mathbf{L}')$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) with global [[BV-differential]] on [[regular polynomial observables]]

$$
  \{-S',(-)\}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
$$

([this def.](A+first+idea+of+quantum+field+theory#ComplexBVBRSTGlobal)).

Let moreover

$$
  g S_{int}
   \;\in\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [ \hbar , g  ] ]
$$

be a [[regular polynomial observable]] (regarded as an [[adiabatic switching|adiabatically switched]] non-point-[[interaction]] [[action functional]]) such that the total action $S' + g S_{int}$ satisfies the [[quantum master equation]] ([this prop.](quantum+master+equation#QuantumMasterEquation)); and write

$$
  \mathcal{R}^{-1}(-)
  \;\coloneqq\;
  \mathcal{S}(g S_{int})^{-1}
    \star_H
  (\mathcal{S}(g S_{int}) \star_F (-))
$$

for the corresponding [[quantum Møller operator]] ([this def.](quantum+master+equation#MollerOperatorOnRegularPolynomialObservables)).

Then by [this prop.](quantum+master+equation#QuantumMasterEquation) we have

$$
  \label{OnRegularObservablesQuantumMasterWardIdentityViaTimeOrdered}
  \{-S',(-)\} \circ \mathcal{R}^{-1}
  \;=\;
  \mathcal{R}^{-1}
  \left(
    \left\{ -(S' + g S_{int}) \,,\, (-) \right\}_{\mathcal{T}}
    -
    i \hbar   \Delta_{BV}
  \right)
$$

This is the _quantum master Ward identity_ on [[regular polynomial observables]], i.e. before [[renormalization]].

=--

([Rejzner 13, (37)](Ward+identity#Rejzner13))

+-- {: .num_remark #QuantumMasterEuqationRelatesQuantumInteractingELEquationsToClassicalFreeELEquations}
###### Remark
**([[quantum master Ward identity]] relates [[quantum field theory|quantum]] [[interacting field theory|interacting field]] [[equation of motion|EOMs]] to [[classical field theory|classical]] [[free field]] [[equation of motion|EOMs]])**

For $A \in PolyObs(E_{\text{BV-BRST}})_{reg}[ [ \hbar, g] ] $ the [[quantum master Ward identity]] on [[regular polynomial observables]] (eq:OnRegularObservablesQuantumMasterWardIdentityViaTimeOrdered) reads

$$
  \label{RearrangedMasterQuantumWard}
  \mathcal{R}^{-1}
  \left(
    \left\{ -(S' + g S_{int}) \,,\, A \right\}_{\mathcal{T}}
    -
    i \hbar   \Delta_{BV}(A)
  \right)
  \;=\;
  \{-S', \mathcal{R}^{-1}(A) \}
$$

The term on the right is manifestly in the [[image]] of the global [[BV-differential]] $\{-S',-\}$ of the [[free field theory]] ([this def.](A+first+idea+of+quantum+field+theory#ComplexBVBRSTGlobal)) and hence vanishes when passing to [[on-shell]] observables along the [[isomorphism]] ([this equation](A+first+idea+of+quantum+field+theory#eq:OnShellPolynomialObservablesAsBVCohomology))

$$
  \underset{
    \text{on-shell}
  }{
  \underbrace{
    PolyObs(E_{\text{BV-BRST}}, \mathbf{L}')
  }}
  \;\simeq\;
  \underset{
    \text{off-shell}
  }{
  \underbrace{
    PolyObs(E_{\text{BV-BRST}})_{def(af = 0)}
  }}/im(\{-S',-\})
$$

(by [this example](A+first+idea+of+quantum+field+theory#BVDifferentialGlobal)).

Hence

$$
  \mathcal{R}^{-1}
  \left(
    \left\{ -(S' + g S_{int}) \,,\, A \right\}_{\mathcal{T}}
    -
    i \hbar   \Delta_{BV}(A)
  \right)
  \;=\;
  0
  \phantom{AAA}
  \text{on-shell}
$$

In contrast, the left hand side is the [[interacting field observable]] (via [this def.](S-matrix#MollerOperatorOnRegularPolynomialObservables)) of the sum of the [[time-ordered product|time-ordered]] [[antibracket]] with the [[action functional]] of the [[interacting field theory]] and a quantum correction given by the [[BV-operator]]. If we use the definition of the [[BV-operator]] $\Delta_{BV}$ ([this def.](BV-operator#RearrangedMasterWardWithOnShell)) we may equivalently re-write this as


$$
  \label{RearrangedMasterWardWithOnShell}
  \mathcal{R}^{-1}
  \left(
    \left\{ -S'  \,,\, A \right\}
    +
    \left\{ -g S_{int} \,,\, A  \right\}_{\mathcal{T}}
  \right)
  \;=\;
  0
  \phantom{AAA}
  \text{on-shell}
$$


Hence the [[quantum master Ward identity]] expresses a relation between the ideal spanned by the [[classical field theory|classical]] [[free field theory|free field]] [[equations of motion]] and the [[quantum field theory|quantum]] [[interacting field theory|interacting field]] equations of motion.



=--

+-- {: .num_example #SchwingerDysonReductionOfQuantumMasterWardIdentity}
###### Example
**([[free field]]-limit of [[master Ward identity]] is [[Schwinger-Dyson equation]])**

In the [[free field]]-limit $g \to 0$ (noticing that in this limit $\mathcal{R}^{-1} = id$) the [[quantum master Ward identity]] (eq:OnRegularObservablesQuantumMasterWardIdentityViaTimeOrdered) reduces to

$$
  \left\{ -S'  \,,\, A \right\}_{\mathcal{T}}
  -
  i \hbar   \Delta_{BV}(A)
  \;=\;
  \{-S', A  \}
$$

which is the defining equation for the [[BV-operator]] ([this equation](BV-operator#eq:BVOperatorDefiningRelation)), hence is isomorphic (under $\mathcal{T}$) to the [[Schwinger-Dyson equation]] ([this prop.](BV-operator#DysonSchwinger))

=--

+-- {: .num_example #MasterWardIdentityClassical}
###### Example
**([[classical limit]] of [[quantum master Ward identity]])**

In the [[classical limit]] $\hbar \to 0$ (noticing that the classical limit of $\{-,-\}_{\mathcal{T}}$ is $\{-,-\}$) the [[quantum master Ward identity]] (eq:OnRegularObservablesQuantumMasterWardIdentityViaTimeOrdered) reduces to

$$
  \mathcal{R}^{1}
  \left(
    \left\{ -(S' + g S_{int}) \,,\, A \right\}
  \right)
  \;=\;
  \{-S', \mathcal{R}^{-1}(A) \}
$$

This says that the [[interacting field observable]] corresponding to the global [[antibracket]] with the action functional of the [[interacting field theory]] vanishes on-shell, classically.

Applied to an observable which is [[linear map|linear]] in the [[antifields]]

$$
  A
    \;=\;
  \underset{\Sigma}{\int}
    A^a(x)
    \mathbf{\Phi}^\ddagger_a(x)
  \,
  dvol_\Sigma(x)
$$

this yields

$$
  \begin{aligned}
    0
    & =
    \{-S', \mathcal{R}^{-1}(A)\}
    +
    \mathcal{R}^{-1}
    \left(
      \left\{ -(S' + S_{int}) \,,\, A \right\}_{\mathcal{T}}
    \right)
    \\
    & =
    \underset{\Sigma}{\int}
      \frac{\delta S'}{\delta \mathbf{\Phi}^a(x)} \mathcal{R}^{-1}(A^a(x))
    \, dvol_\Sigma(x)
    +
    \mathcal{R}^{-1}
    \left(
      \underset{\Sigma}{\int}
          A^a(x) \frac{\delta (S' + S_{int})}{\delta \mathbf{\Phi}^a(x)}
        \, dvol_\Sigma(x)
    \right)
  \end{aligned}
$$

This is the _classical master Ward identity_ according to ([Dütsch-Fredenhagen 02](Ward+identity#DuetschFredenhagen02), [Brennecke-Dütsch 07, (5.5)](Ward+identity#BrennecketDuetsch07)), following ([Dütsch-Boas 02](Ward+identity#DuetschBoas02)).

=--

+-- {: .num_example #NoetherCurrentConservationQuantumCorrection}
###### Example
**(quantum correction to [[Noether's theorem|Noether current]] [[conserved current|conservation]])**

Let $v \in \Gamma^{ev}_\Sigma(T_\Sigma(E_{\text{BRST}}))$ be an [[evolutionary vector field]], which is an [[infinitesimal symmetry of the Lagrangian]] $\mathbf{L}'$, and let $J_{\hat v} \in \Omega^{p,0}_\Sigma(E_{\text{BV-BRST}})$ the corresponding [[conserved current]], by [[Noether's theorem|Noether's theorem I]] ([this prop.](A+first+idea+of+quantum+field+theory#NoethersFirstTheorem)), so that

$$
  \begin{aligned}
    d J_{\hat v}
    & =
    \iota_{\hat v}  \delta \mathbf{L}'
    \\
    & =
    (v^a dvol_\Sigma) \frac{\delta_{EL} L'}{\delta \phi^a}
    \phantom{AAA}
    \in
    \Omega^{p+1,0}_\Sigma(E_{\text{BV-BRST}})
  \end{aligned}
$$

(by [this equation](A+first+idea+of+quantum+field+theory#eq:CurrentNoetherConservation)), where in the second line we just rewrote the expression in components (using [this equation](A+first+idea+of+quantum+field+theory#eq:EulerLagrangeEquationGeneral))

$$
  v^a
  \,,
  \frac{\delta_{EL} L'}{\delta \phi^a}
  \;\in \Omega^{0,0}_\Sigma(E_{\text{BV-BRST}})
$$

and re-arranged suggestively.

Then for $a_{sw} \in C^\infty_{cp}(\Sigma)$ any choice of [[bump function]], we obtain the [[local observables]]

$$
  \begin{aligned}
    A_{sw}
    & \coloneqq
    \underset{\Sigma}{\int}
      \underset{
        A^a(x)
      }{
      \underbrace{
        a_{sw}(x)
        v^a( \mathbf{\Phi}(x), D\mathbf{\Phi}(x), \cdots )
      }
      }
      \mathbf{\Phi}^\ddagger_a(x)
      \,
      dvol_\Sigma(x)
    \\
    & \coloneqq
    \tau_\Sigma( a_{sw}  v^a \phi^{\ddagger}_a \, dvol_\Sigma)
  \end{aligned}
$$

and


$$
  \begin{aligned}
    (div \mathbf{J})_{sw}
    & \coloneqq
    \underset{\Sigma}{\int}
      \underset{
        A^a(x)
      }{
      \underbrace{
        a_{sw}(x)
        v^a( \mathbf{\Phi}(x), D\mathbf{\Phi}(x), \cdots )
      }
      }
      \frac{\delta S'}{\delta \mathbf{\Phi}^a(x)}
      \,
      dvol_\Sigma(x)
    \\
    & \coloneqq
    \tau_\Sigma
    \left(
      a_{sw}  v^a \frac{\delta_{EL} \mathbf{L}'}{\delta \phi^a}
      \, dvol_\Sigma
    \right)
  \end{aligned}
$$

by [[transgression of variational differential forms]].

This is such that

$$
  \left\{
    -S' , A_{sw}
  \right\}
  =
  (div \mathbf{J})_{sw}
  \,.
$$

Hence applied to this choice of local observable $A$, the quantum master Ward identity (eq:RearrangedMasterWardWithOnShell) now says that

$$
  \mathcal{R}^{-1}
  \left(
    {\, \atop \,}
    (div \mathbf{J})_{sw}
  \right)
  \;=\;
  \mathcal{R}^{-1}
  \left(
      \{g S_{int}, A_{sw} \}_{\mathcal{T}}

    {\, \atop \,}
  \right)
    \phantom{AAA}
  \text{on-shell}
$$

Hence the [[interacting field observable]]-version $\mathcal{R}^{-1}(div\mathbf{J})$ of $div \mathbf{J}$ need not vanish itself on-shell, instead there may be a correction as shown on the right.

=--


$\,$


$\,$

#### Retarded products

We have seen that the [[exponential series]]-expansion of the [[perturbative S-matrix]] $\mathcal{S}(g S_{int})$ is given by "[[time-ordered products]]". Similarly there is an [[exponential series]]-expansion of the [[quantum Møller operator]] $\mathcal{S}(g S_{int})^{-1} T(\mathcal{S}(g S_{int}), (-))$ (def. \ref{QuntumMollerOperator}); its coefficients are called the _[[retarded products]]_ (def. \ref{RetardedProductFromPerturbativeSMatrix}) below.

Hence where the [[time-ordered products]] directly relate to [[scattering amplitudes]] (example \ref{ScatteringAmplitudeFromInteractingFieldObservables}) the [[retarded products]] directly relate to more general [[interacting field observables]] (def. \ref{InteractingFieldObservables}).

The formulation of [[interacting field theory]] via [[time-ordered products]] or [[retarded products]] is essentially equivalent; in any given situation either one may be more conenient than the other.

+-- {: .num_defn #RetardedProductFromPerturbativeSMatrix}
###### Definition
**([[retarded products]] from [[S-matrix]])**

It follows from the perturbation axiom in def. \ref{LagrangianFieldTheoryPerturbativeScattering} that there is a system of [[continuous linear functionals]]

$$
  R
    \;\colon\;
  \left(
    LocObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ]
    \langle g\rangle\right)^{\otimes^k}
    \otimes
  (LocObs(E_{\text{BV-BRST}})[ [ \hbar,g, j] ] )^{\otimes^l}
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]
$$

for all $k,l \in \mathbb{N}$ such that

$$
  \mathcal{Z}_{S_{int}}(j A)
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

(...)


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


## Examples

### Chern-Simons theory

The [[Feynman amplitudes]] of [[higher Chern-Simons theory]], such as [[AKSZ sigma-models]], regarded in their incarnation as [[Feynman amplitudes on compactified configuration spaces of points]], serve to exhibit a [[graph complex]]-model for the [[de Rham complex]] of [[Fulton-MacPherson compactifications]] of [[configuration spaces of points]] by the construction recalled [there](Fulton-MacPherson+operad#RelationToGraphComplexes). See the pointers at _[[Chern-Simons theory]]_ [here](Chern-Simons+theory#FeynmanPerturbationSeries).


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

> In the 1970s, S-matrix theory just plain died. All practitioners jumped ship rapidly in 1974, with the triple-whammy of [[effective field theory|Wilsonian field theory]], the discovery of the Charm [[quark]], and [[asymptotic freedom]]. These results killed S-matrix theory for thirty years. Those that jumped ship include all the original [[string theory|string theorists]] who stayed employed: notably [[Gabriele Veneziano|Veneziano]], who was convinced that [[gauge theory]] was right when [[Gerard 't Hooft|t'Hooft]] showed that [[AdS-CFT|large-N gauge fields]] give the string topological expansion, and [[Leonard Susskind|Susskind]], who didn't mention Regge theory after the early 1970s. Everybody stopped studying [[string theory]] except [[Joël Scherk|Scherk]] and [[John Schwarz|Schwarz]], and Schwarz was protected by [[Murray Gell-Mann|Gell-Mann]], or else he would never have been tenured and funded.

> This sorry history means that not a single S-matrix theory course is taught in the curriculum today, nobody studies it except a few theorists of advanced age hidden away in particle accelerators, and the main S-matrix theory, [[string theory]], is not properly explained and remains completely enigmatic even to most physicists. There were some good reasons for this --- some S-matrix people said silly things about the consistency of quantum field theory --- but to be fair, [[quantum field theory]] people said equally silly things about S-matrix theory.

> [[Steven Weinberg|Weinberg]] came up with these heuristic arguments in the 1960s, which convinced him that S-matrix theory was a dead end, or rather, to show that it was a tautological synonym for quantum field theory. Weinberg was motivated by models of pion-nucleon interactions, which was a hot S-matrix topic in the early 1960s. The solution to the problem is the [[chiral symmetry breaking]] models of the pion condensate, and these are [[effective field theories]].

> Building on this result, Weinberg became convinced that the only real solution to the S-matrix was a field theory of some particles with spin. He still says this every once in a while, but it is dead wrong. The most charitable interpretation is that every S-matrix has a field theory limit, where all but a finite number of particles decouple, but this is not true either (consider [[little string theory]]). String theory exists, and there are non-field theoretic S-matrices, namely all the ones in [[string theory]], including [[little string theory]] in (5+1)d, which is non-gravitational.

From ([Weinberg 09, p. 11](#Weinberg09)):

> I offered this in my 1979 paper as what [[Arthur Wightman]] would call a [[folk theorem]]: "if one writes down the most general possible [[Lagrangian]], including all terms consistent with assumed [[symmetry]] principles, and then calculates [[scattering amplitudes|matrix elements]] with this Lagrangian to any given order of [[perturbation theory]], the result will simply be the most general possible S-matrix consistent with perturbative unitarity, analyticity, [[cluster decomposition]], and the assumed symmetry properties."

> There was an interesting irony in this. I had been at Berkeley from 1959 to 1966, when [[Geoffrey Chew]] and his collaborators were elaborating a program for calculating S-matrix elements for [[strong nuclear force|strong interaction]] processes by the use of unitarity, analyticity, and Lorentz invariance, without reference to [[quantum field theory]]. I found it an attractive philosophy, because it relied only on a minimum of principles, all well established. Unfortunately, the S-matrix theorists were never able to develop a reliable method of calculation, so I worked instead on other things, including [[current algebra]]. Now in 1979 I realized that the assumptions of S-matrix theory, supplemented by chiral invariance, were indeed all that are needed at low energy, but the most convenient way of implementing these assumptions in actual calculations was by good old quantum field theory, which the S-matrix theorists had hoped to supplant.


## Related entries

* [[Haag-Ruelle scattering theory]]

* [[LSZ reduction formula]]

* [[Coleman theorem]], [[Haag–Łopuszański–Sohnius theorem]]

* [[scattering amplitude]], [[Feynman diagram]], [[string scattering amplitude]],

* [[crossing symmetry]]

* [[AdS-CFT]]

* [string theory FAQ -- What are the equations of string theory?](string%20theory%20FAQ#WhatAreTheEquations)


See also at _[[sigma model]]_ the section _<a href="http://ncatlab.org/nlab/show/sigma-model#SecondQuantization">Exposition of second quantization of sigma-models</a>_


[[!include products in pQFT -- table]]


## References

### General

Early work basing [[perturbative quantum field theory]] on the concept of the S-matrix is

* {#Heisenberg43} [[Werner Heisenberg]], _Die "beobachtbaren Größen" in der Theorie der Elementarteilchen_, Zeitschrift für Physik 120, 513, 1943 ([doi:10.1007/978-3-642-70078-1_44](https://doi.org/10.1007/978-3-642-70078-1_44))

recalled in

* Alexander S. Blum, _The state is not abolished, it withers away: how quantum field theory became a theory of scattering_ ([arXiv:2011.05908](https://arxiv.org/abs/2011.05908))



This proposal was vocally promoted as the "bootstrap program" by [[Geoffrey Chew]] and [[Stanley Mandelstam]] (see [Chew 70](#Chew70)).

An account of the history of the contributions by [[Tullio Regge]] is in

* {#Bottino18} Alessandro Bottino, _A retrospective look at Regge poles_ ([arXiv:1807.02456](https://arxiv.org/abs/1807.02456))

Textbook accounts of this axiomatic approach to defining the S-matrix (i.e. not proceeding via [[Lagrangian field theory]] but via analyticity axioms):

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

* {#Chew70} [[Geoffrey Chew]], _Quark or Bootstrap: Triumph or Frustration for Hadron Physics_, Physics Today, May 1970 ([web](https://pubarchive.lbl.gov/islandora/object/ir%3A144169/datastream/PDF/view), [[Chew70.pdf:file]])

* {#Schroer11} [[Bert Schroer]], _Causality and dispersion relations and the role of the S-matrix in the ongoing research_ ([arXiv:1102.0168](https://arxiv.org/abs/1102.0168))

Discussion with emphasis on [[gravitational waves]] and [[perturbative quantum gravity]]:

* [[Pierre Vanhove]], *S-matrix approach to general gravity and beyond* ([arXiv:2104.10148](https://arxiv.org/abs/2104.10148))


See also

* Wikipedia, _[S-matrix](http://en.wikipedia.org/wiki/S-matrix#History)_

* Wikipedia, _[S-matrix theory](http://en.wikipedia.org/wiki/S-matrix_theory)_

* Wikipedia, _[Bootstrap model](https://en.wikipedia.org/wiki/Bootstrap_model)_


The S-matrix for [[mesons]] in [[chiral perturbation theory]]:

* Andrea Guerrieri, Joao Penedones, Pedro Vieira, _S-matrix Bootstrap for Effective Field Theories: Massless Pions_ ([arXiv:2011.02802](https://arxiv.org/abs/2011.02802))

* Eef van Beveren, George Rupp, _Modern meson spectroscopy: the fundamental role of unitarity_ ([arXiv:2012.03693](https://arxiv.org/abs/2012.03693))


Brief introduction to the S-matrix in quantum mechanics and its rigorous construction in field theory via [[causal perturbation theory]] is in

* {#Scharf95} [[Günter Scharf]], sections 0.3 and 3.1 of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, awSpringer 1995

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

* Piotr Tourkine, Alexander Zhiboedov, _Scattering from production in 2d_ ([arXiv:2101.05211](https://arxiv.org/abs/2101.05211))

Talk notes:

* Gabriele Travaglini, _The return of the analytic S-matrix_, 2013 ([pdf](http://pyweb.swan.ac.uk/sfsh/sewmweb/sfshtalks/gabriele.pdf))

* Rutger Boels, _The Ultimate Revenge of the Analytic S-matrix_ ([pdf](http://thep.housing.rug.nl/sites/default/files/talks/The%20revenge%20of%20the%20analytic%20S-matrix.pdf))

On the S-matrix bootstrap in relation to [[string scattering amplitudes]]:

* Andrea Guerrieri, Joao Penedones, Pedro Vieira, _Where is String Theory?_ ([arXiv:2102.02847](https://arxiv.org/abs/2102.02847))

An entertaining account of some of the history and the sociology of S-matrix theory is on the first pages of

* {#Shankar99} [[Ramamurti Shankar]], _Effective Field Theory in Condensed Matter Physics_ in _Conceptual Foundations of Quantum Field Theory_, 1999 ([arXiv:cond-mat/9703210](http://arxiv.org/abs/cond-mat/9703210))


[[!include classification of long-range forces -- references]]





[[!redirects S-matrices]]


[[!redirects scattering matrix]]
[[!redirects scattering matrices]]

[[!redirects S-matrix theory]]
[[!redirects S-matrix theories]]

[[!redirects S-matrix scheme]]
[[!redirects S-matrix schemes]]

[[!redirects perturbative S-matrix]]
[[!redirects perturbative S-matrices]]

[[!redirects Feynman perturbation series]]

[[!redirects S-matrix bootstrap]]


