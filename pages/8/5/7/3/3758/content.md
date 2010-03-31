<div class="rightHandSide toc">
[[!include physicscontents]]
</div>

under construction

+--{: .query}
[[Ian Durham]]: Please help make this a bit more clear, but please note there is some dispute concerning the nature of quantum states.
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Every quantum particle or system has a certain number of intrinsic characteristics such as charge, mass, spin, etc.  In fact one could think of the complete list of such intrinsic characteristics of a single particle as _defining_ that particle (e.g. an electron is defined by it's set of characteristics).

Every quantum particle or system also has some associated _variable_ quantities usually called **observables** such as position, momentum, energy, spin orientation, etc.  Observables can often be grouped into subsets.  So, for example, $S_{x}, S_{y}$ and $S_{z}$ is the subset of observables of spin orientation while its position and momentum (including angular) observables form the spatial subset.

A quantum state is the state of a quantum particle or system at a given instant in time and is usually described by a normalized complex vector called the **state vector**.  In the context of a subset of observables, the state vector has as many components as there are possible values for any one of a subset's basic observables.  In other words, the state of a physical system in quantum mechanics with $n \in \mathbb{N}$ degrees of freedom is encoded by a a state vector with $n$ components.  The wavefunction for a system is encoded in its state vector.

Alternatively, the state may be thought of as being encoded by a complex [[hermitian matrix|hermitian]] $n \times n$ [[matrix]] $\rho \in Mat(n\times n, \mathbb{C})$ with non-negative [[eigenvalue]]s and unit [[trace]]. This is called a **[[density matrix]]**.  Note that this is less restrictive than the state vector representation of states since multiple state vectors can give a single density matrix.

## Definition

The full state of a quantum system with $n \in \mathbb{N}$ degrees of freedom is given by the set of observables, $Q(q)$.  We most often work with subsets of observables such as spatial $Q(x) \subset Q(q)$ or spin $Q(s) \subset Q(q)$.  Categorically, quantum states are always objects within a category and the morphisms of a category represent the transformations that the states can undergo.

### Categorical caveat

It pays to spend some time looking over the entry on [[2-vector space]] since the categorification of vector spaces is not entirely clear.

[[!redirects quantum states]]