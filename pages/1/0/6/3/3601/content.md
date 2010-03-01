<div class="rightHandSide toc">
[[!include physicscontents]]
</div>



> under construction

Quantum information refers to data that can be physically stored in a [[quantum mechanics|quantum system]]. 

Quantum information theory is the study of how such information can be encoded, measured, and manipulated. A notable sub-field is _quantum computation_, a term often used synonymously with quantum information theory, which studies protocols and algorithms that use quantum systems to perform computations.

Categorical quantum information refers to a program in which the cogent aspects of [[Hilbert space]]-based quantum information theory are abstracted to the level of [[symmetric monoidal categories]].

#Contents#
* automatic table of contents goes here
{:toc}

## Hilbert space quantum mechanics

+--{: .query}
TODO: decide whether to shift this section to [[quantum mechanics]].
=--

In pure state quantum mechanics, physical states are encoded as vectors in a [[Hilbert space]]. Often Dirac "bra-ket" notation is used to represent such vectors, where $|\psi\rangle$ represents a state and $\langle\psi|$ represents its linear adjoint. State evolutions are expressed as unitary maps. Self-adjoint operators represent physical quantities such such as position and [[momentum]] and are called observables. Measurements are expressed as sets of projectors onto the eigenvectors of an observable.

In mixed state quantum mechanics, physical states are represented as density operators $\rho$, state evolution as maps of the form $\rho \mapsto U^\dagger \rho U$ for unitary maps $U$, and measurements are positive operator-valued measures (POVM's). There is a natural embedding of pure states into the space of density matrices: $|\psi\rangle \mapsto |\psi\rangle\langle\psi|$. So, one way to think of mixed states is a probabilistic mixture of pure states.

\[ \rho = \sum_i a_i |\psi_i\rangle\langle\psi_i| \]

Composite systems are formed by taking the tensor product of Hilbert spaces. If a pure state $|\Psi\rangle \in H_1 \otimes H_2$ can be written as $|\psi_1\rangle \otimes |\psi_2\rangle$ for $|\psi_i\rangle \in H_i$ it is said to be _separable_. If no such $|\psi_i\rangle$ exist, $|\Psi\rangle$ is said to be _entangled_. If a mixed state is separable if it is the sum of separable pure states. Otherwise, it is entangled.

States, state evolutions, and observables are all special cases of [[quantum channels]] which can be used to describe the exchange of classical and quantum [[information]].

### Quantum protocols and algorithms

Brief synopsis of teleportation, entanglement swapping, BB84, E91, Deutsch-Jozsa, Shor.

+--{: .query}
[[Ian Durham]]: Should we maybe somehow link the quantum mechanics section to this?  Teleportation and entanglement, to me, are quantum phenomena that transcend their use in quantum information theory (the others, I agree, are purely information-theoretical).

[[Aleks Kissinger]]: Entanglement I agree with, though the description of teleportation as a protocol (as opposed to a phenomenon) probably belongs here.

[[Ian Durham]]: Yes, I'd agree with that.  It's description is usually in terms of a protocol.  Actually, I suppose it's status as a "phenomenon" is somewhat debatable.
=--

## Categorical formulation

The linear adjoint $(-)^\dagger$ gives Hilbert spaces the structure of a [[†-category]]. The category of Hilb of Hilbert spaces forms a **&#8224;-symmetric monoidal category**, that is, a [[symmetric monoidal category]] equipped with a symmetric monoidal functor $(-)^\dagger$ from $Hilb^{op}$ to $Hilb$. Furthermore, the category FHilb of _finite dimensional_ Hilbert spaces forms a **&#8224;-compact closed category**, or a [[compact closed category]] such that $A_*$ := $(A^*)^\dagger = (A^\dagger)^*$ and $(\eta_A)^\dagger = \epsilon_{A^*}$.

## Diagrammatic notation

<svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 width="60px" height="109px" viewBox="0 0 60 109" enable-background="new 0 0 60 109" xml:space="preserve">
<line fill="none" stroke="#000000" stroke-width="2" x1="30.5" y1="0" x2="30.5" y2="109"/>
<rect x="1" y="23.5" fill="#ccccee" stroke="#000000" stroke-width="2" width="58" height="58"/>
<text transform="matrix(1 0 0 1 26 60.5)" font-family="'MyriadPro-Regular'" font-size="24">f</text>
<polyline fill="none" stroke="#000000" stroke-width="2" points="26,8.752 30.438,13.25 34.875,8.752 "/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="26.333,91.752 30.771,96.25 35.208,91.752 "/>
</svg>

## Extensions

CPM, classical structures, ...

[[!redirects quantum information theory]]
[[!redirects quantum computing]]
[[!redirects quantum computation]]