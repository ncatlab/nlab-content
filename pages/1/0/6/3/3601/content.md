<div class="rightHandSide toc">
[[!include physicscontents]]
</div>



> under construction

_Quantum information_ refers to data that can be physically stored in a [[quantum mechanics|quantum system]]. 

_Quantum information theory_ is the study of how such information can be encoded, measured, and manipulated. A notable sub-field is _quantum computation_, a term often used synonymously with quantum information theory, which studies protocols and algorithms that use quantum systems to perform computations.

_Categorical quantum information_ refers to a program in which the cogent aspects of [[Hilbert space]]-based quantum information theory are abstracted to the level of [[symmetric monoidal categories]].

#Contents#
* automatic table of contents goes here
{:toc}

## Quantum information and quantum computation

In pure state quantum mechanics, physical states are encoded as vectors in a [[Hilbert space]]. Often Dirac "bra-ket" notation is used to represent such vectors, where $|\psi\rangle$ represents a state and $\langle \psi |$ represents its linear adjoint. State evolutions are expressed as unitary maps. Self-adjoint operators represent physical quantities such such as position and [[momentum]] and are called observables. Measurements are expressed as sets of projectors onto the eigenvectors of an observable.

In mixed state quantum mechanics, physical states are represented as density operators $\rho$, state evolution as maps of the form $\rho \mapsto U^\dagger \rho U$ for unitary maps $U$, and measurements are positive operator-valued measures (POVM's). There is a natural embedding of pure state quantum mechanics into the mixed state picture. Another way to approach this is through the use of [[quantum channels]] which can be used to describe the exchange of [[information]]. (TODO: show this)


### Entanglement

### Quantum protocols and algorithms

Brief synopsis of teleportation, entanglement swapping, BB84, E91, Deutsch-Jozsa, Shor.

+--{: .query}
[[Ian Durham]]: Should we maybe somehow link the quantum mechanics section to this?  Teleportation and entanglement, to me, are quantum phenomena that transcend their use in quantum information theory (the others, I agree, are purely information-theoretical).
=--

## $\dagger$-symmetric monoidal categories

* [[†-category]]

## Diagrammatic notation

## Extensions

CPM, classical structures, ...

[[!redirects quantum information theory]]
[[!redirects quantum computing]]
[[!redirects quantum computation]]