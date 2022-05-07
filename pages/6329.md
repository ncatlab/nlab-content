
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### AQFT
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

[[dynamics|Dynamics]] affects both [[observables]] and, [[duality between space and quantity|dually]], [[states]]; this is most well known in [[quantum mechanics]] but applies equally well to [[classical mechanics]]. The different "pictures" of mechanics differ in how the dynamics is explicitly formalized:

* In the __Heisenberg picture__, the dependence of observables on [[time]] (or more generally [[spacetime]]) is encoded, while the state is held fixed; the axiomatic formalization of this is given by the [[Haag–Kastler axioms]] of [[AQFT]].

* In the __Schr&#246;dinger picture__, states are [[propagator|propagated]] through [[time]], while observables are held fixed; the axiomatic formalization of this is given by [[cobordism category]] [[representations]] in [[FQFT]].

* The __[[Dirac (interaction) picture]]__ is a mixture of these two approaches: dynamics is split into a [[free system|free]] (or otherwise [[solvable system|solvable]]) part and an [[perturbation theory|interaction or perturbation]]; one of these is take to affect the states, the other the observables.

The pictures are named after those physicists ([[Werner Heisenberg]], [[Erwin Schrödinger]], and [[Paul Dirac]]) who first used or popularised these approaches to quantum physics.


## Formulation

### With global time

Let us assume a global notion of [[time]], say a [[background field|fixed background]] [[spacetime]] which is [[globally hyperbolic spacetime|globally hyperbolic]], so that it admits a [[foliation]] into [[Cauchy surfaces]], and choose a [[time coordinate]] for this foliation.  The upshot of this is that each [[event]] occurs at a time $t$, and conversely we can speak of [[space]] at any time $t$ (at least within certain bounds).  Thus we may speak sensibly of either the state of the world at time $t$ or the value of some observable quantity at time $t$.

Because this is a picture of [[dynamics]], states or observables (as appropriate to the picture) will vary through time.  We therefore have a [[time evolution]] operator $U(t,t')$ between any two times $t,t'$; actually, we need consider only $U(t) \coloneqq U(t,0)$, since $U(t,t') = U(t) \circ U(t')^{-1}$.

In the Heisenberg picture, for each observable $A$, we speak of $A$ only at some time $t$, so our actual observables are of the form $A(t)$.  We write abstractly
$$ A(t) = A(0) \cdot U(t) $$
to show the evolution of the observable through time.  However, when it comes to the state of the world, we speak of a single state $\psi$ that describes the world at all times.

In the Schr&#246;dinger picture, we instead speak of $\psi(t)$, the state of the world at time $t$.  We write abstractly
$$ \psi(t) = U(t) \ast \psi(0) $$
(the [[Schrödinger equation]]) to show the evolution of the state through time.  However, when it comes to observables, we use only the observable $A$ across all times.

To see the connection between the two pictures, recall that an observable $A$ and a state $\psi$ together produce a [[probability distribution]] giving the probability that any given value of $A$ will be observed, given that the world is in state $\psi$.  (This is true throughout mechanics, although it is obscured in non-statistical classical mechanics, since the probability distributions produced by classical [[pure states]] are all [[delta measure]]s.)  Assuming that $A$ belongs to an appropriate [[algebra of observables]] and the probability measures are sufficiently nice, we may restrict attention to the [[expectation value]]s $\langle{A}\rangle_\psi$ of these distributions, since the entire distribution can be recovered from $\langle{A^n}\rangle_\psi$ as $n$ varies over [[natural numbers]].

The connection between the two pictures is then given by
$$ \langle{A \cdot U(t)}\rangle_\psi = \langle{A}\rangle_{U(t) \ast \psi} .$$

It remains to say exactly what $U(t)$ is and what the operations $\cdot$ and $\ast$ are.  Let us use the [[density matrix]] formulation of [[quantum statistical mechanics]], since classical and non-statistical mechanics may be recovered as special cases, by restricting (respectively) the allowed observables or states.  In this case, both states and observables are given by [[linear operators]] on a [[Hilbert space]] $H$, and we have
$$ \langle{A}\rangle_\psi = \tr(A \psi) $$
(using the [[trace]] operation).
Each $U(t)$ is a [[unitary operator]] on $H$ (since time evolution between Cauchy surfaces is a symmetry), and we have
$$ A \cdot U(t) = U(t)^{-1} A U(t) $$
(a [[right action]]) and
$$ U(t) \ast \psi = U(t) \psi U(t)^{-1} $$
(a [[left action]]).
We then have
$$ \langle{A \cdot U(t)}\rangle_\psi
 = tr(U(t)^{-1} A U(t) \psi)
 = tr(A U(t) \psi U(t)^{-1})
 = \langle{A}\rangle_{U(t) \ast \psi} ,$$
as desired, using the [[cyclic property of the trace]].

The time evolution operator $U(t)$ is often derived from a [[Hamiltonian]] and the formula for $A(t)$ or $\psi(t)$ is further derived from a [[differential equation]] involving this Hamiltonian.  However, this is unnecessary for the connection between the two pictures.


### Without time

If spacetime is not [[globally hyperbolic spacetime|globally hyperbolic]], then there is no time coordinate $t$, and none of the discussion above makes sense; or if we choose a coordinate $t$ and call it time regardless, then time evolution is not a symmetry and we do not have the operators $U(t)$.

In this case, the Heisenberg picture still makes sense, even though we cannot expect to calculate $A(t)$ from $A(0)$ (if it even makes sense to discuss such things).  This is easily seen in [[field theory]], where the operators called $A$ above are really of the form $A(x,y,z)$.  Then the Heisenberg picture\'s $A(t)$ is really $A(x,y,z,t)$, or simply $A(p)$ where $p$ indicates an [[event]] (a [[point]] in [[spacetime]]).  So even if the coordinates $x,y,z,t$ do not make sense, still $A(p)$ does; and even if the equations of physics cannot be thought of as describing evolution through time, still they can be thought of as describing the relationships between observables at different places in spacetime.

In contrast, the Schr&#246;dinger picture cannot be so treated.  One may be led to the contrary impression by the quantum mechanics of a single particle without any internal structure (not even [[spin]]), in which case the Hilbert space of (pure quantum-mechanical) states is naturally identified with $L^2(\mathbb{R}^3)$ and the state $\psi$ is really $\psi(x,y,z)$.  In this case, the Schr&#246;dinger picture\'s $\psi(t)$ is really $\psi(x,y,z,t)$, that is $\psi(p)$.  However, this fails in classical or statistical mechanics; and even in non-statistical quantum mechanics, it breaks down if the particle has internal structure or there is more than one particle in the world.  Then we see that the spacial coordinates $x,y,z$ generalise to the arbitrary coordinates of [[configuration space]], while $t$ remains only $t$, and there is no way to subsume it into a spacetime coordinate.

### In local field theory

from [Torre-Varadarajan 98 p.2](#TorreVaradarajan98):

The idea of evolving a quantum field from any [[Cauchy surface]] to any other seems to have originated in the mid 1940's with the work of Tomonaga [1] and
Schwinger [2] on relativisticquantum field theory. Tomonaga and Schwinger wanted an invariant generalization of the Schr&#246;dinger equation, which describes time evolution of the state of a quantum field relative to a fixed inertial reference frame. By allowing for all possible Cauchy surfaces in the
description of dynamical evolution one easily accommodates all possible notions of time for all possible inertial observers. Thus a dynamical formalism incorporating arbitrary Cauchy surfaces does allow for an invariant generalization of the Schr&#246;dinger equation. Since, the space of Cauchy surfaces is infinite-dimensional, it is impossible to describe time evolution along arbitrary surfaces by using a single time parameter.  In essence, one needs a distinct time parameter for every possible foliation of spacet
ime. As shown by Tomonaga and Schwinger, if one formulates dynamics in terms of general Cauchy surfaces, the resulting dynamical evolution equation is, formally, a functional differential equation, which is usually called the "[[Tomonaga-Schwinger equation]]. Following [3], we use the term
functional evolution to refer to the formulation of dynamical evolution in which one evolves quantities along arbitrary Cauchy surfaces.

Thus the Tomonaga-Schwinger equation appears as the analog of the Schr &#776;odinger equation, when describing functional evolution. It was (and stillis) tacitly assumed that the Tomonaga-Schwinger equation defines the infinitesimal form of unitary evolution of states from one Cauchy surface to another, just as the more familiar (and mathematically more tractable) sCHR&#214;DINGER equation describes the infinitesimal form of unitary evolution between two hyperplanes of constant Minkowskian time. One of our principal goals in this paper is to show that this assumption is untenable.



from [[Arnold Neumaier]], [PO comment 2016](http://www.physicsoverflow.org/36936/what-picture-the-haag-ruelle-scattering-theory-formulated?show=36953#a36953).

The [[Heisenberg picture]] is the only one where relativistic quantum field theory can be rigorously defined, e.g., through the Wightman axioms. The latter imply the existence of a 4-dimensional group of translations generated by the 4-momentum vector $p$. Once one select a future-like direction to determine time, one gets from $p$ the Hamiltonian $H=p_0$, and can use it to define time-dependent states $\psi(t)$ in the usual way. Together with the spatial part of the momentum, this gives a conventional, frame-dependent Schroedinger representation of the states.

Thus the Schr&#246;dinger picture exists but is frame dependent. You can regard any operator $A$ on the Hilbert space as a Schroedinger observable and find its expectation as time changes in the usual Schroedinger way, and translate it to the Heisenberg picture in the usual way such that $A$ becomes explicitly time-dependent and the state is fixed.

However, in 4-dimensional relativistic interacting quantum field theories, fields must be smeared in space and in time in order to produce densely defined operators (rather than distributions). Thus, unlike in the nonrelativistic case, the fixed-time spatial fields $\phi(x)=\Phi(t,x)|_{t=0}$, where $x$ is 3-dimensional, are not well-defined objects. 

Thus although the Schroedinger picture exists it does not represent local fields at a fixed time. The attempt to pretend it did leads to the problems mentioned in Dirac's paper. In this sense, the relativistic field theory cannot be made well-defined without transcending the Schroedinger picture. 

The above is completely independent of scattering theory. In scattering theory one has to construct the asymptotic Hilbert space. Unlike the interacting Hilbert space, the asymptotic Hilbert space is a Fock space and must therefore be defined by a limiting procedure. This is what is done in the Haag-Ruelle theory. Note that because of the Lorentz invariance of the future cone, the resulting asymptotic space does not depend on the choice of the time direction, as long as it points into the future cone. 

There are presentations of the Haag-Ruelle theory that are a little more in the spirit of the Heisenberg picture; see the comments at the end of p.379 of Volume 3 of Reed and Simon. One can probably work almost completely in the Heisenberg picture if one works out the algebra of asymptotic constants (in analogy with the nonrelativistic case treated in Section 3.4 of Volume 3 of Thirring), but to show that the corresponding asymptotic operators have a Fock representation one apparently needs to go through some Schroedinger-like computations.

## History

Historically, the terms 'Schr&#246;dinger picture' and 'Heisenberg picture' (at least) referred to *more* than what we discuss above; they referred to the entirety of the differences between Schr&#246;dinger\'s and Heisenberg\'s approaches to quantum mechanics.

For example, these terms included also Schr&#246;dinger\'s use of typically [[wave]]-like functions as pure states (and correspondingly [[operators]] in the higher-type-theoretic sense as observables) vs Heisenberg\'s use of infinite-dimensional [[matrix|matrices]] as observables (and correspondingly [[infinite sequences]] as pure states).  This difference was rectified by [[John von Neumann|von Neumann]]\'s application of [[Hilbert space]] to the problem, showing that (if one suitably restricts the allowed functions and sequences and also identifies equivalent functions a bit) both approaches used Hilbert space (what we would now call the infinite-dimensional  iseparable Hilbert space) as the space of pure states.

This is entirely separate from the question of whether states or observables are taken to evolve with time.  Still, there is this connection: Schr&#246;dinger evolved states, and his approach was called 'wave mechanics' after his representation for states, while Heisenberg evolved observables, and his approach was called 'matrix mechanics' after his representation for observables.

## Examples

* The [[quantization]] of the [[hydrogen atom]] in the various pictures is reviewed in [Nanni 15](#hydrogen+atom#Nanni15), chpapter 6 for the Schr&#246;dinger picture and chapter 12 for the Heisenberg picture.

## Related concepts

* [[Tomonaga-Schwinger equation]]

[[!include Isbell duality - table]]


## References

See for instance 

* [[Eberhard Zeidler]], sections 7.19.1--3 in _Quantum field theory. A bridge between mathematicians and physicists -- volume I_ Springer (2009) ([web](http://www.mis.mpg.de/zeidler/qft.html)).

To check conventions at least, see Wikipedia:

* [Heisenberg picture](http://en.wikipedia.org/wiki/Heisenberg_picture),
* [Schr&#246;dinger picture](http://en.wikipedia.org/wiki/Schr%C3%B6dinger_picture).

Subtleties with the Schr&#246;dinger picture for [[field theory]] in [[spacetime]] dimension $\geq 3$ is discussed in

* {#TorreVaradarajan98} [[Charles Torre]], M. Varadarajan, _Functional Evolution of Free Quantum Fields_, Class.Quant.Grav. 16 (1999) 2651-2668 ([arXiv:hep-th/9811222](https://arxiv.org/abs/hep-th/9811222))

A note on how the Schr&#246;dinger picture in the form of [[extended quantum field theory|extended]] [[FQFT]] on [[Lorentzian manifold]]s is related to the Heisenberg picture in the form of [[AQFT]] is in 

* [[Urs Schreiber]], _[[schreiber:AQFTfromFQFT.pdf:file]]_, Communications in Mathematical Physics, Volume 291, Issue 2 (2009), pp.357-401 

[[operator algebra|Operator algebraic]] formulation of [[quantum error correction]] in the Heisenberg picture:

* Cédric Bény, Achim Kempf, David W. Kribs, _Generalization of Quantum Error Correction via the Heisenberg Picture_, Phys. Rev. Lett. 98, 100502 – Published 7 March 2007 ([doi:10.1103/PhysRevLett.98.100502](https://doi.org/10.1103/PhysRevLett.98.100502), [arXiv:quant-ph/0608071](https://arxiv.org/abs/quant-ph/0608071))

* Cédric Bény, Achim Kempf, David W. Kribs, _Quantum Error Correction of Observables_, Phys. Rev. A 76, 042303 (2007) ([arXiv:0705.1574](https://arxiv.org/abs/0705.1574))


[[!redirects dynamical picture]]
[[!redirects picture of dynamics]]
[[!redirects mechanical picture]]
[[!redirects picture of mechanics]]
[[!redirects quantum mechanical picture]]
[[!redirects picture of quantum mechanics]]

[[!redirects Heisenberg picture]]
[[!redirects Schrödinger picture]]
[[!redirects Schroedinger picture]]
[[!redirects Schrodinger picture]]
