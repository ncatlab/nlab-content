<div class="rightHandSide toc">
[[!include physicscontents]]
</div>

> under construction


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

[[quantum mechanics|Quantum mchanics]] and [[quantum field theory]] describe the dynamics of systems governed by [[quantum physics]]. In the _[[FQFT|Schrödinger picture]]_ of quantum mechanics this involves an assignment of a collection of _states_ of the system -- the **quantum states** -- to each _instant of time_ and a map from the collection of states at one instance to the collection of states at any other instance that encodes the time evolution of these states.

There are different proposals for how to formmlize quantum mechanics and quantum field theory, whose relations are understood (only) in parts. 
Accordingly, there are different ways to make the notion of _quantum state_ precise.

Broadly speaking, formalizations of quantum mechanics are of two main different types:

* in the _Schr&#246;dinger picture_ formalization of [[FQFT]] a quantum field theory is an [[n-functor]] 

  $$
    U : Cob_n^S \to \mathcal{C}
  $$

  on an [[(infinity,n)-category of cobordisms]] (with some extra structure $S$) to some target [[(infinity,n)-category]]. In this perspective an "instance of time" is an [[k-morphism|(n-1)-morphism]] $\Sigma$ in $Cob_n^S$, the **space of states** on this is the object $U(\Sigma) \in \mathcal{C}$ and a single quantum state is a [[generalized element]] $\psi \in U(\Sigma)$. 

  For instance for the category $Cob_1^{Riem}$ of 1-dimensional Riemannian cobordisms, a smooth functor $U : Cob_1^{Riem} \to$  [[Hilb]] may encode the quantum mechanics of a point particle propagating on some target space. The [[Hilbert space]] that it assigns to the single o-morphism ([[object]]) is the single space of states, and a quantum state is a ray in this Hilbert space.

* in the _Heisenberg picture_ formalization of [[AQFT]] quantum states are described more indirectly. Here the direct description is of the _local algebras of observables_ . In this formalization quantum states are revovered as linear functionals on these operator algebras, i.e. as [[state on an algebra|states on an algebra]] in the operator-theoretic sense.



+--{: .query}
[[Ian Durham]]: Please help make this a bit more clear, but please note there is some dispute concerning the nature of quantum states, including whether or not they even exist (see below).
=--


Every quantum particle or system has a certain number of intrinsic characteristics such as charge, mass, spin, etc.  In fact one could think of the complete list of such intrinsic characteristics of a single particle as _defining_ that particle (e.g. an electron is defined by it's set of characteristics).

Every quantum particle or system also has some associated _variable_ quantities usually called **observables** such as position, momentum, energy, spin orientation, etc.  Observables can often be grouped into subsets.  So, for example, $S_{x}, S_{y}$ and $S_{z}$ is the subset of observables of spin orientation while its position and momentum (including angular) observables form the spatial subset.

+--{: .query}
[[Tim van Beek]]: That looks like the idea of [[superselection sector]]s.
Again starting from [[AQFT]]: The Hilbert space of all states is a direct sum of subspaces, called superselection sectors or coherent subspaces. Within each one has an unrestricted superposition principle, while phase relations between state vectors belonging to different sectors are meaningless.
Example: If you got two states, x and y, x has integer spin and y has half integer spin, the relative phase of both cannot have any physical relevance. The algebra of observables transforms each sector into itself. So, if there are no charge carrying fields, a given state in one sector cannot be transformed into a state in a different sector by any "physical process". That's the essential difference between e.g. momentum and spin. Spin is constant on each superselection sector, momentum is not.
=--

A quantum state is the state of a quantum particle or system at a given instant in time and is usually described by a normalized complex vector called the **state vector**.  In the context of a subset of observables, the state vector has as many components as there are possible values for any one of a subset's basic observables.  In other words, the state of a physical system in quantum mechanics with $n \in \mathbb{N}$ degrees of freedom is encoded by a a state vector with $n$ components.  The wavefunction for a system is encoded in its state vector.

Alternatively, the state may be thought of as being encoded by a complex [[hermitian matrix|hermitian]] $n \times n$ [[matrix]] $\rho \in Mat(n\times n, \mathbb{C})$ with non-negative [[eigenvalue]]s and unit [[trace]]. This is called a **[[density matrix]]**.  Note that this is less restrictive than the state vector representation of states since multiple state vectors can give a single density matrix.

The full state of a quantum system with $n \in \mathbb{N}$ degrees of freedom is given by the set of observables, $Q(q)$.  We most often work with subsets of observables such as spatial $Q(x) \subset Q(q)$ or spin $Q(s) \subset Q(q)$.  Categorically, quantum states are always objects within a category and the morphisms of a category represent the transformations that the states can undergo.

## Definition

### In plain quantum mechanics
In QM, the state of a quantum system is a normalized vector of a given complex (separable) Hilbert space. Observables are represented by selfadjoint (not necessarily bounded) operators on that Hilbert space. The value of an observable A in a state x is given by $\langle x, Ax \rangle$.

#### $L^2$ standard representation

### aspects of quantum information theory
TODO
(please mention [Gleason's theorem] (/nlab/show/von+Neumann+algebra#GleasonsTheorem))

### In FQFT

#### States as rays in Hilbert spaces

#### States in higher dimensional extended QFTs

### In AQFT
The starting point of [[AQFT]] is either with fields, see [[Wightman axioms]], or directly with an (abstract) $C*-$algebra of observables, see [[Haag-Kastler axioms]]. Roughly the Wightman fields generate the operator algebras of observables. 

#### Linear functionals on operator algebras
A (quantum) state in the sense of physics is a state of the algebra of observables in the sense of mathematics, see [states of operator algebras](/nlab/show/operator+algebra#statesOfOperatorAlgebras).
Note that the concept of a particle has not entered the scene yet, so that the concept of a state if more fundamental from the current viewpoint than that of a particle. 

To get to the Hilbert space picture of quantum mechanics one needs to employ the GNS construction ([[Gelfand-Naimark-Segal construction]]) to obtain both a Hilbert space from the algebra of observables and a given state, and a representation of the observables in the algebra of bounded operators on that Hilbert space.

## QBism and category theory

In the quantum Bayesian view, there is really no such thing as a quantum state.  More correctly, a so-called quantum state is "not something out there, in the external world, but instead [is an expression] of information." (Ref. 1, p.2).  Ultimately, in QBism, it is the _relations between_ states that is of interest anyway.  This could be said of physics as a whole, in a way, since one view of the universe holds that it consists of particles and their interactions and that without the interactions (which are nothing more than relations), the universe would be a boring place (Ref. 4).  The underlying theme here is that relativity was right: everything is relative (related) to something else.

Taken in this context, physics is really a relational theory which is why category theory is ideally suited to describe it: the richest part of category theory is the morphisms (arrows).  Without them you're essentially reduced to a very limited (and uninteresting) set theory.  The internal morphisms of categories as well as functors between categories are the "meat" of category theory and this is precisely the same idea QBism attempts to capture in the context of quantum theory.  Category theory may prove to be the ideal tool for a fuller and richer development of QBism.

## References

* C.A. Fuchs, _QBism, the Perimeter of Quantum Bayesianism_ ([pdf](http://arxiv.org/abs/1003.5209)), gives a nice summary of the quantum Bayesian view and also provides a treasure trove of references on discussions (going all the way back to the beginning of quantum theory) on quantum states.

* G. Brida, M. Bondani, I. P. Degiovanni, M. Genovese, M. G. A. Paris, I. Ruo Berchera, V. Schettini, _On the discrimination between classical and quantum states_, ([pdf](http://arxiv.org/abs/0909.5288)), discusses the relation between quantum and classical states.

* D.N. Page, _Do Our Observations Depend upon the Quantum State of the Universe?_, ([pdf](http://arxiv.org/abs/0907.4751)), includes discussion concerning the nature of quantum states.

* I.T. Durham, _Unification and Emergence in Physics: the Problem of Articulation_, ([pdf](http://arxiv.org/abs/1001.4304)), discusses the adequacy of language and mathematics in describing the physical world.

[[!redirects quantum states]]