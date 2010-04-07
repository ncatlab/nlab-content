<div class="rightHandSide toc">
[[!include physicscontents]]
</div>


> under construction

#Contents#
* automatic table of contents goes here
{:toc}

## Quantum mechanics of point particles

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


## Quantum physics in general #

More generally, _quantum mechanics_ or _quantum physics_ may be taken to subsume [[quantum field theory]] and all of physics that is not [[classical mechanics]]. Another way to look at quantum processes is via [[quantum channels]] which are completely positive trace-preserving maps.


+--{.query}
Zoran: I slightly disagree with that opposite extremity either. The sentence is better suited to define quantum physics (though complement to [[classical physics]] includes relativity, while opposite to classical mechanics includes thermodynamics). Quantum physics is not the same as quantum mechanics. There are quantum phenomena which are not treated by quantum mechanics only. I mean it would be very unusual calling quantum statistical 
physics, part of quantum mechanics; it requires special limiting assumptions (thermodynamic limit, quantum ergodicity and so on lie outside) outside of scope of the things derivable from quantum mechanics.    

[[Ian Durham]]: J.J. Sakurai's book *Modern Quantum Mechanics* (not to be confused with his *Advanced Quantum Mechanics* which is a field theory book) discusses quantum statistical mechanics under the guise of quantum mechanics as does the forthcoming book *Q-PSI: Quantum processes, systems, and information* by Schumacher and Westmoreland.  While it may not be entirely accurate, "quantum physics" and "quantum mechanics" are usually treated as being synonymous.

Zoran: Quantum physics includes all quantum phenomena, including experimental reality. Quantum mechanics is just the theoretical description at the fundamental level, like mechanics is of the classical physics. 

[[Ian Durham]]: I agree, in principle, but I'm simply saying that not everyone interprets the term as such.

Zoran: not everybody cares about fine distinctions, but we should try to acknowledge the distinctions which are made at least by more careful treatises, not the least common denominator. 

Ian: The more I think about it, the more I strongly disagree.  I think you are correct in saying that quantum mechanics is the theoretical formalism for describing quantum phenomena in a non-field theoretic POV.  But what we're going on this site is describing the theory in terms of categories, not the phenomena.  If you want to strip it all down to the bear bones, rid quantum physics of the "mechanics," and then rebuild it entirely from an nPOV, be my guest.  But so far, that is not what has been done on this site.

Zoran: why non-field ?? Field is a continuous limiting case of mechanics when it becomes with infinitely many degrees of freedom. Classical mechanics of particles and fields. Quantum mechanics of particles and fields. These are standard expressions. After 52 courses of physics I attended in my life I am confident in basic terminology. Quantum physics is without a doubt more general notion. For example, Bohr was studying quantum physics, and de Broglie was and they did NOT do QM as they studied quantum physics at a incomplete level before QM proper was invented. Sometimes one intermediate phase, from 1913 with Bohr-Sommerfeld quantization conditions call "old quantum mechanics", though. The things you talk about categories and $n$POV have nothing to do with all of this and make no sense in this discussion. 
=--

## Quantum mechanics in terms of $\dagger$-compact categories

Many aspects of quantum mechanics and [[quantum computation]] depend only on the abstract properties of [[Hilb]] characterized by the fact that it is a [[†-compact category]]. 

For more on this see

* [[quantum mechanics in terms of †-compact categories]].


## References and related entries

* [[Hamilton operator]], [[semiclassical approximation]], [[quantization]]

* Glimm and Jaffe, [[Glimm-Jaffe|Quantum physics%3A a functional integral point of view]] (how to quote the link with : ??)

* Movshev's course has mathematically nice references: [link](http://www.math.sunysb.edu/~mmovshev/MAT570Spring2008/syllabusfinal.html); and [here](http://www.math.columbia.edu/~woit/qftnotes1.pdf) is a link to Woit's list of mroe physical tradition references. 

* P. Cartier, C. DeWitt-Morette, _Functional integration: action and symmetries_, Cambridge Monographs on Mathematical Physics, 2006.

* Leon Takhtajan, [[Quantum mechanics for mathematicians]], Amer. Math. Soc. 2008. 

[[!redirects quantum physics]]