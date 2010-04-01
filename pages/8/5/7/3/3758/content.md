<div class="rightHandSide toc">
[[!include physicscontents]]
</div>

under construction

+--{: .query}
[[Ian Durham]]: Please help make this a bit more clear, but please note there is some dispute concerning the nature of quantum states, including whether or not they even exist (see below).

[[Tim van Beek]]: I tried to insert a few ideas of mine...I guess we would have to narrow this page to a certain interpretation of quantum physics, like "what is a quantum state in the traditional sense of quantum mechanics" or "what is a quantum state in the sense of the xy picture of QFT".
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Every quantum particle or system has a certain number of intrinsic characteristics such as charge, mass, spin, etc.  In fact one could think of the complete list of such intrinsic characteristics of a single particle as _defining_ that particle (e.g. an electron is defined by it's set of characteristics).

+--{: .query}
[[Tim van Beek]]: In AQFT you would start with the observables, and say that the values (let's call them quantum numbers for now) of a complete set of observables unambiguously identify a state of a system. If you have an ensemble of states with identical quantum numbers and get one of them today, and another one tomorrow, there is no way to tell if it is the same or a "different" one. 
BTW: An "electron" in this picture is a state with the appropriate quantum numbers, so from the viewpoint of [[QFT]] one should not treat "states" and "particles" as complementary concepts, the concept of state is more fundamental. 
=--

Every quantum particle or system also has some associated _variable_ quantities usually called **observables** such as position, momentum, energy, spin orientation, etc.  Observables can often be grouped into subsets.  So, for example, $S_{x}, S_{y}$ and $S_{z}$ is the subset of observables of spin orientation while its position and momentum (including angular) observables form the spatial subset.

+--{: .query}
[[Tim van Beek]]: That looks like the idea of [[superselection sector]]s.
Again starting from [[AQFT]]: The Hilbert space of all states is a direct sum of subspaces, called superselection sectors or coherent subspaces. Within each one has an unrestricted superposition principle, while phase relations between state vectors belonging to different sectors are meaningless.
Example: If you got two states, x and y, x has integer spin and y has half integer spin, the relative phase of both cannot have any physical relevance. The algebra of observables transforms each sector into itself. So, if there are no charge carrying fields, a given state in one sector cannot be transformed into a state in a different sector by any "physical process". That's the essential difference between e.g. momentum and spin. Spin is constant on each superselection sector, momentum is not.
=--

A quantum state is the state of a quantum particle or system at a given instant in time and is usually described by a normalized complex vector called the **state vector**.  In the context of a subset of observables, the state vector has as many components as there are possible values for any one of a subset's basic observables.  In other words, the state of a physical system in quantum mechanics with $n \in \mathbb{N}$ degrees of freedom is encoded by a a state vector with $n$ components.  The wavefunction for a system is encoded in its state vector.

Alternatively, the state may be thought of as being encoded by a complex [[hermitian matrix|hermitian]] $n \times n$ [[matrix]] $\rho \in Mat(n\times n, \mathbb{C})$ with non-negative [[eigenvalue]]s and unit [[trace]]. This is called a **[[density matrix]]**.  Note that this is less restrictive than the state vector representation of states since multiple state vectors can give a single density matrix.

## Definition

The full state of a quantum system with $n \in \mathbb{N}$ degrees of freedom is given by the set of observables, $Q(q)$.  We most often work with subsets of observables such as spatial $Q(x) \subset Q(q)$ or spin $Q(s) \subset Q(q)$.  Categorically, quantum states are always objects within a category and the morphisms of a category represent the transformations that the states can undergo.

+--{: .query}
[[Tim van Beek]]: In QM, the state of a quantum system is a normalized vector in a complex (separable) Hilbert space. Observables are represented by selfadjoint (not necessarily bounded) operators on that Hilbert space. The value of an observable A in a state x is given by $\langle x, Ax \rangle$.

Again, from the viewpoint of AQFT you start with the $C*$-algebra of observables, the state of a system is given by a state of the algebra in a mathematical sense, and the Hilbert space enters through the GNS construction with respect to that state.
=--

### Categorical caveat

It pays to spend some time looking over the entry on [[2-vector space]] since the categorification of vector spaces is not entirely clear.

## References

+--{: .query}
[[Tim van Beek]]: One (short) remark per reference what it's about would be nice.
=--

* C.A. Fuchs, _QBism, the Perimeter of Quantum Bayesianism_ ([pdf](http://arxiv.org/abs/1003.5209)).

* G. Brida, M. Bondani, I. P. Degiovanni, M. Genovese, M. G. A. Paris, I. Ruo Berchera, V. Schettini, _On the discrimination between classical and quantum states_, ([pdf](http://arxiv.org/abs/0909.5288))

* D.N. Page, _Do Our Observations Depend upon the Quantum State of the Universe?_, ([pdf](http://arxiv.org/abs/0907.4751))

[[!redirects quantum states]]