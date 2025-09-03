> This entry is about the notion of state in [[physics]] For use in [[computer science]], see at _[[state monad]]_. 


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

A _state_ of a system in [[physics]] is a description of everything that is true (or known, or relevant, depending on the circumstances) about the [[physical system]].

In the [[Bayesian interpretation of physics]], the state of a system is not a property of reality but instead indicates an observer\'s knowledge about the system.  A _[[pure state]]_ gives maximal information about the system (which amounts to complete information in [[classical mechanics]] but not generally in [[quantum mechanics]]), while a _[[mixed state]]_ is more general.  A mixed state can be decomposed into a [[probability distribution]] on the space of pure states, although this decomposition is unique only for classical systems.  In a frequentist interpretation of probability, a mixed state can describe only a statistical ensemble of systems; the real world is in one (generally unknown) pure state (possibly with additional hidden variables in the quantum case, depending on the interpretation of quantum physics).

States in the [[Schrödinger picture]] describe the state of the system at any given time and are subject to [[time evolution]], while in the [[Heisenberg picture]] a single state describes the entire history of the system (with time evolution applying to the [[observables]] instead).

In [[statistical physics]], a [[microstate]] is a complete description of all of the particles in a system, while a [[macrostate]] considers only the macroscopic properties known to [[thermodynamics]].


## Definitions

The precise mathematical notion of _state_ depends on what mathematical formalization of mechanics is used.


### Algebraic definition
 {#AlgebraicDefinition}

Quite generally, both in [[classical physics]] as well as in [[quantum physics]], one may define states as assignments of [[expectation values]] to [[observables]] in an [[algebra of observables]]. This is the definition used in _[[quantum probability theory]]_ (which subsumes ordinary [[probability theory]]). See at 

* _[[state in AQFT and operator algebra]]_

for details.


### In classical mechanics

In classical [[Lagrangian mechanics]], a pure state is a [[global element|point]] in the [[state space]] of the system, giving all of the (generalised) [[generalized position|positions]] and [[velocity|velocities]].  In classical [[Hamiltonian mechanics]], a pure state is a point in the [[phase space]] of the system, giving the positions and [[momentum|momenta]].  In either case, a mixed state is a [[probability distribution]] on the space of pure states.

More generally, a _[[classical state]]_ is a [[linear function]] $\rho\colon A \to \mathbb{R}$ on the [[Poisson algebra]] $A$ underlying the [[classical mechanical system]] which satisfies _positivity_ and _normalization_.


### In geometric quantization

* [[space of states (in geometric quantization)]]


### In Hilbert-space quantum mechanics

In [[quantum mechanics]] given by a [[Hilbert space]] $H$, a [[pure state]] is a ray in $H$, which we often call the Hilbert space of states.  Strictly speaking, the space of states is not $H$ but $(H \setminus \{0\})/\mathbb{C}$, or equivalently $S(H)/\mathrm{U}(1)$.  A mixed state is then a [[density matrix]] on $H$.


### In AQFT

In [[AQFT]], a [[quantum mechanical system]] is given by a $C^*$-[[C-star-algebra|algebra]] $A$, and a [[quantum state]] is usually defined as a linear function $\rho\colon A \to \mathbb{C}$ which satisfies _positivity_ and _normalization_; see [[states in AQFT and operator algebra]].

Arguably, the correct notion of state to use is that of [[quasi-state]]; every state gives rise to a unique quasi-state, but not conversely.  However, when either classical mechanics or Hilbert-space quantum mechanics is formulated in AQFT, every quasi-state *is* a state (at least if the Hilbert space is not of very low dimension, by [[Gleason's theorem]]).  See also the Idea-section at [[Bohr topos]] for a discussion of this point.


### In FQFT

In the [[FQFT]] formulation of [[quantum field theory]], a physical system is given by a [[cobordism]] [[representation]]

$$
  Bord_n^S \to \mathcal{C}
  \,.
$$

In this formulation the [[k-morphism|(n-1)-morphism]] in $\mathcal{C}$ assigned to an $(n-1)$-dimensional [[manifold]] $\Sigma_{n-1}$ is the _space of states_ over that manifold. A state is accordingly a [[generalized element]] of this object.


## Pure and mixed states

In [[statistical physics]], a [[pure state]] is a state of maximal information, while a [[mixed state]] is a state with less than maximal information.  In the classical case, we may say that a pure state is a state of *complete* information, but this does not work in the quantum case; from the perspective of the information-theoretic or Bayesian interpretation of quantum physics, this inability to have complete information, even when having maximal information, is the key feature of [[quantum physics]] that distinguishes it from [[classical physics]].

See [[pure state]].


## Examples

Here are some toy examples of spaces of states.

For an impossible system, the space of states is [[empty space|empty]]; for a trivial system (with a unique way to be), the space of states is the [[point]].  This unique state is pure.

For a classical [[bit]], a system with two distinct ways to be, the space of states is a [[line segment]]; a state is given by a real number $t$ with $0 \leq t \leq 1$.  This $t$ is the probability that the system is in the first state, with $1 - t$ the probability that it is in the second; the two pure states correspond to $t = 0$ and $t = 1$.  This space naturally comes equipped with a metric structure in which its length is actually $2$; it's the line segment from $(0,1)$ to $(1,0)$ in the [[Lebesgue space]] $l^1(2)$.

For a quantum bit, a [[qubit]], a state is given by a self-adjoint $2$-by-$2$ complex matrix
$$ \begin{pmatrix} a & b - \mathrm{i} c \\ b + \mathrm{i} c & d \end{pmatrix} $$
with unit trace (so $d = 1 - a$) and nonnegative determinant (so $a^2 + b^2 + c^2 \leq a$).
However, the metric structure from viewing this as a subset of $\mathbb{R}^3$ is misleading, so we use $w \coloneqq a - d = 2 a - 1$ instead, along with $u \coloneqq 2 b$ and $v \coloneqq 2 c$ to keep the same normalization.  Then the density matrix may be written
$$ \frac 1 2 \begin{pmatrix} 1 + w & u - \mathrm{i} v \\ u + \mathrm{i} v & 1 - w \end{pmatrix} = \frac 1 2 (\mathrm{I} + u \sigma_x + v \sigma_y + w \sigma_z) ,$$
where the $\sigma$s are the [[Pauli matrices]].  This already has unit trace; the inequality for the determinant is
$$ u^2 + v^2 + w^2 \leq 1 .$$
The pure states are those satisfying $u^2 + v^2 + w^2 = 1$, forming a unit [[sphere]], known in this context as the [[Bloch sphere]] (so the full space of all states is the Bloch ball).


## Related concepts

[[!include states and observables -- content]]

\linebreak

[[!include Isbell duality - table]]


[[!redirects state]]
[[!redirects states]]
[[!redirects physical state]]
[[!redirects physical states]]

[[!redirects space of states]]
[[!redirects spaces of states]]

[[!redirects space of physical states]]
[[!redirects spaces of physicsal states]]
