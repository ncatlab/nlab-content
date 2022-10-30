
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

A _state_ is a [[configuration space|configuration]] of a system in [[physics]], together with enough information about its [[time evolution]] (typically, the first derivative is sufficient) to allow one to propagate it arbitrarily.

In the Bayesian interpretation of physics, the state of a system is not a property of reality but instead indicates an observer\'s knowledge about the system.  A _[[pure state]]_ gives maximal information about the system (which amounts to complete information in [[classical mechanics]] but not generally in [[quantum mechanics]]), while a _[[mixed state]]_ is more general.  A mixed state can be decomposed into a [[probability distribution]] on the space of pure states, although this decomposition is unique only for classical systems.  In a frequentist interpretation of probability, a mixed state can describe only a statistical ensemble of systems; the real world is in one (generally unknown) pure state (possibly with additional hidden variables in the quantum case, depending on the interpretation of quantum physics).

States in the [[Schrödinger picture]] describe the state of the world at any given time and are subject to [[time evolution]], while in the [[Heisenberg picture]] a single state describes the entire history of the world.


## Definitions

The precise mathematical notion of _state_ depends on what mathematical formalization of mechanics is used.


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


## Related concepts

* **state**

  * [[classical state]], 

  * [[quantum state]]
   
    * [[superposition]]

    * [[space of states (in geometric quantization)]]

    * [[state in AQFT and operator algebra]]

* [[observable]]

  * [[algebra of observables]]

  * [[GNS construction]]

  * [[quantum operator (in geometric quantization)]]

[[!include Isbell duality - table]]


[[!redirects state]]
[[!redirects states]]
[[!redirects physical state]]
[[!redirects physical states]]

[[!redirects space of states]]
[[!redirects spaces of states]]

[[!redirects space of physical states]]
[[!redirects spaces of physicsal states]]
