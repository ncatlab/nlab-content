#Contents#
* automatic table of contents goes here
{:toc}

#Point particle quantum mechanics#

 _Quantum mechanics_ is usually understood to be the part of [[quantum field theory]] that studies the quantum analog of the [[classical mechanics]] of point particles. 

+--{.query}
Zoran: While this has some merit for this particular direction/subfield, it is other way around: quantum field theory is a special kind of a quantum mechanical system (with infinitely many degrees of freedom). You are here taking very special point of view and identifying quantum mechanics with quantum mechanics of a system with finitely many degrees of freedom. One teaches thus other way around: there are quantum mechanical systems, then there are some special kinds including QFTs. Quantum mechanics of the point particles on the other hand is not subsumed by the formalism below either. For example, the time-dependent Hamiltonians and quantum mechanics for finite state systems do not seem to be included. I personally do not understand how do you put a concrete potential in the game below either but I suppose it is a way. I mean which space-dependent and other parameters are allowed for $H$ and how it works (note that while the usual forces are related to the curvature, I do not see there is a mechanism for all kind of potentials and more general hamiltonians to be just derived from general rule and be invariant under isomorphism in Riemannian category) ?

_Toby_:  It looks like Urs understands 'mechanics' in much the same way that I did at [[classical mechanics]].  I do agree that that the term includes time-dependent Hamiltonians and similar generalisiations, however.
=--

One may usefully think of the quantum mechanics of a point particle propagating on a [[manifold]] $X$ as being $(0+1)$-dimensional [[quantum field theory]]:

the fields of this system are maps $\Sigma \to X$ where $\Sigma \in Riem Bord_1$ are 1-dimensional [[Riemannian manifold]] [[cobordism]]s. These are the _trajectories_ of the particle. 

After [[quantization]] this yields a 1-dimensional [[FQFT]] given by a [[functor]]

$$
  U(-) : Riem Bord_1 \to Hilb
$$

from [[cobordism]]s to [[Hilbert space]]s (or some other flavor of [[vector space]]s) that assigns

* to the point the _space of states_ $\mathcal{H}$, typically the space of $L_2$-sections (with respect to a [[Riemannian metric]] on $X$) of the background [[gauge field]] on $X$ under which the particle in question is charged 

* to the cobordism of Riemannian length $t$ the operator

  $$
    U(t) := \exp\left(\frac{t}{i \hbar } H \right)
    : \mathcal{H} \to \mathcal{H}
    \,,
  $$

  where $H$ is the [[Hamiltonian operator]], typically of the form $H = \nabla^\dagger \circ \nabla $ for $\nabla$ the [[covariant derivative]] of the given background [[gauge field]].

Such a setup describes the quantum mechanics of a particle that feels forces of backgound [[gravity]] encoded in the [[Riemannian metric]] on $X$ and forces of background gauge fields (such as the [[electromagnetic field]]) encoded in the covariant derivative $\nabla$.

#Quantum mechanics in general #

More generally, _quantum mechanics_ may be used as a term that subsumes [[quantum field theory]] and all of physics that is not [[classical mechanics]]. 

Zoran: I slightly disagree with that opposite extremity either. The sentence is better suited to define quantum physics (though complement to [[classical physics]] includes relativity, while opposite to classical mechanics includes thermodynamics). Quantum physics is not the same as quantum mechanics. There are quantum phenomena which are not treated by quantum mechanics only. I mean it would be very unusual calling quantum statistical 
physics, part of quantum mechanics; it requires special limiting assumptions (thermodynamic limit, quantum ergodicity and so on lie outside) outside of scope of the things derivable from quantum mechanics.    

