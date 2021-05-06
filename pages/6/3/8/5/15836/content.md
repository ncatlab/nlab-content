
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Philosophy
+-- {: .hide}
[[!include philosophy - contents]]
=--
=--
=--

# The Bayesian interpretation of quantum physics
* table of contents
{: toc}

## Idea

[[mathematics|Mathematically]], [[quantum mechanics]], and in particular [[quantum statistical mechanics]], can be viewed as a generalization of [[probability theory]], that is as _[[quantum probability theory]]_.  The [[Bayesianism|Bayesian]] interpretation of probability can then be generalized to a Bayesian [[interpretation of quantum mechanics]], and thus (in principle) of all [[physics]].

The Bayesian interpretation is founded on these principles:

1. Quantum states (pure or mixed) are analogous to (indeed generalizations of) probability distributions, which are to be interpreted in a Bayesian way, as indicating knowledge, belief, etc.

2. Time evolution of pure quantum states by the time-dependent [[Schroedinger equation|Schrödinger's equation]] is analogous to evolution of classical statistical systems by [[Liouville's equation]] (and von Neumann has an equation for the evolution of [[density matrices]] that generalizes both).

3. [[wave function collapse|Collapse of the wave function]] (see also [[propositions as projections]]) is analogous to (indeed a generalization of) updating a probability distribution; [[Born rule|Born's Rule]] and [[Bayes rule|Bayes' Rule]] are analogues.

One should perhaps speak of *a* Bayesian interpretation of quantum mechanics, since there are different forms of Bayesianism.  (This article has been written by an objective Bayesian who naturally thinks of Bayesian probabilities as reflecting knowledge rather than belief, betting commitments, etc.  For other flavours of Bayesianism, substitute 'knowledge' below with a more appropriate term.)


## Formalism

There are various ways to formulate [[quantum mechanics]] mathematically, but the following elements are fairly common:

*  There is an algebra $A$ of [[observables]]; some or all of the elements of this algebra correspond to physically observable quantities.
*  There is a space $S$ of [[states]], by which we mean [[mixed states]] in general.
*  Given a state $\psi$ and an observable $O$, we obtain a [[probability distribution]] (a [[probability measure]] on the [[real line]] or something like it).

Roughly speaking, this probability distribution tells us the probability of observing the value of $O$ to take particular values given that the system has state $\psi$.  Let us write $O_*\psi(E)$ for the probability that the value of $O$ will be observed to belong to the event $E$ (which is a [[measurable set]] of real numbers when $\psi$ is a probability measure on the real line) for a system in state $\psi$.

So for example, we could actually be talking about a [[classical physics|classical]] system, in which we have a [[state space]] or [[phase space]] $X$, an observable is a function on $X$, a [[pure state]] is a point in $X$, and a general state is a probability measure on $X$.

Or we could be talking about a quantum system given by a [[Hilbert space]] $H$, in which an observable is a [[self-adjoint operator]] on $H$, a pure state is a $1$-dimensional subspace of $H$, and a general state is a [[density matrix]] on $H$.

Or we could use a more abstract formulation, such as those of [[AQFT]], [[FQFT]], and so forth; but all of these still have observables and states.

See also [[JBW-algebraic quantum mechanics]] for a mathematical formalism that may be motivated by treating the probability distributions $O_*\psi$ as fundamental (among other considerations).


## Interpretation

The point of the Bayesian interpretation is that the probabilities $O_*\psi(E)$ are to be interpreted as Bayesian probabilities.  That is, they are not objective features of reality (the territory) but rather an expression of what a rational observer might know about the world (a map).

Thus, a state $\psi$ represents a _state of knowledge_ about the world.  The algebra $A$ of observables may be objective (or fully known), but the particular state $\psi$ that the system is in depends on what is known about that particular system.  There is (except in the classical case) *no* possible complete specification of the actual values of all observables, only a probabilistic specification of what one might know about them.

In the [[Schroedinger picture]] (assuming a notion of [[time]]), states [[time evolution|evolve]] deterministically, unitarily, and with conservation of [[entropy]].  (Or in the [[Heisenberg picture]], they don\'t evolve at all, with the observables evolving instead.)  But a state may change otherwise, if one\'s knowledge changes.  If this is an increase in knowledge as a result of a [[measurement]], then this change in the state may be called the 'collapse of the wavefunction'.  But this collapse takes place in the map, not the territory; unlike time evolution, it is not a physical process.

Given a specification of $S$ and $A$, it may be that there exist certain states $\psi$ in $S$ such that $O_*\psi$ is a [[delta measure]] (giving a probability of $1$ for one value and $0$ for all others) for every $O$ in $A$.  Then the system is classical.  Depending on the mathematical formalism used, such states may not actually belong to $S$ (which might, for example, own only the [[absolutely continuous measure|absolutely continuous]] probability measures in some sense, as is natural in the [[JBW-algebraic quantum mechanics|W*-algebraic approach]]); so in general, we may say that the system is __classical__ if there exists a [[net]] $(\psi_n)_n$ of states such that, for each observable $O$, the net $(O_*\psi_n)_n$ of measures on the real line [[convergence in measure|converges in measure]] to a delta measure.  (Or so I imagine; this definition might not really be general enough.)


## History

People have implied (for example at the beginning of [Caves, Fuchs, & Schack, 2001](#CFS2001)) that this is what [[Niels Bohr]] meant all along when he put forth the [[Copenhagen interpretation]] (for more on this suggestion see also at _[[Bohr topos]]_), and people have implied (in the first paper at [Fuchs, n.d.](#Fuchs)) that it is what [[Albert Einstein]] was groping towards when he attacked Bohr, and still others ([[Ray Streater]] as cited in [Wikimedia Foundation, n.d.](#Wikimedia)) have implied that it is what [[John von Neumann]] was doing when he eschewed interpretation for mathematical axioms.  Any time that somebody has described a quantum state as containing information, or being given by an experimenter\'s knowledge, or being different for one observer than for another, the Bayesian interpretation is implicit.  Arguably, it is implicit in any statement that the wavefunction describes probabilities, if [[probability]] is treated as Bayesian.  However, the *explicit* exposition of this interpretation seems to have come rather late.

The earliest linking of Bayesianism to quantum states as states of knowledge, as far as I have seen, is Usenet discussion in 1994 ([Baez et al, 2003](#Baez2003)).  [[John Baez]] was promoting similar ideas the previous year ([Baez, 1993](#Baez1993)) (and this is not the origin of these ideas either), but this still allows other interpretations.  The idea of a 'Bayesian interpretation' came to prominence in 2001, drawing out of work on [[quantum information theory]] ([Caves, Fuchs, & Schack, 2001](#CFS2001)).  Further work has been done principally by [[Christopher Fuchs]] ([Fuchs, n.d.](#Fuchs)).


## Related interpretations

The Bayesian interpretation fits into a broader family of [[interpretations of quantum mechanics]] known as _epistemic_ (or _$\psi$-epistemic_ to be more precise).  Although 'epistemic' literally refers to knowledge (suggesting objective Bayesianism in particular), the term may be used more broadly to distinguish from _ontic_ interpretations, in which the state $\psi$ is an objective feature of reality.  In contrast, an epistemic interpretation is one in which the state is subjective in some way (whether relative to one\'s knowledge or otherwise).  Much of what is written above applies more broadly to any epistemic interpretation, although I\'m not sure how much; at least some epistemic interpretations go on to posit a more fundamental reality (involving [[hidden-variable theory|hidden variables]]), while the Bayesian interpretation does not require this.

In the other direction, 'Quantum Bayesianism' or 'QBism' is used specifically to refer to the position advanced over the course of last decade principally by [[Christopher Fuchs]].  Although Fuchs\'s first papers on the subject (starting with [Caves, Fuchs, & Schack, 2001](#CFS2001)) referred explicitly to 'states of knowledge', Fuchs has since adopted an increasingly subjective approach, drawing many philosophical conclusions that go beyond mere Bayesianism.  These ideas should be attributed to QBism specifically rather than to the Bayesian interpretation generally.

## Related entries

* [[interpretation of quantum mechanics]]

* [[quantum probability]]

* [[collapse of the wave function]]

## References

* {#Baez1993} [[John Baez]] (1993). This Week's Finds in Mathematical Physics (Week 27). [Web](http://math.ucr.edu/home/baez/week27.html).
 

* {#Baez2003} John Baez et al (2003). Bayesian Probability Theory and Quantum Mechanics. Collection of Usenet posts from 1994, with commentary. [Web](http://www.math.ucr.edu/home/baez/bayes.html)
  

* {#CFS2001} Carlton Caves, [[Christopher Fuchs]], Ruediger Schack (2001). Unknown Quantum States: The Quantum de Finetti Representation. [arXiv](http://arxiv.org/abs/quant-ph/0104088).
  

* {#Fuchs} [[Christopher Fuchs]] (n.d.). Quantum Dreams Page. Collection of preprints, epistles, and lecture notes. [Web](http://www.physics.umb.edu/Research/QBism/chris.html).

* [[Christopher Fuchs]], [[David Mermin]], Ruediger Schack, _An Introduction to QBism with an Application to the Locality of Quantum Mechanics_, Am. J. Phys., Vol. 82, No. 8, August 2014, 749-754 ([arXiv:1311.5253](https://arxiv.org/abs/1311.5253))

* {#Mermin18} [[David Mermin]], _Making better sense of quantum mechanics_ ([arXiv:1809.01639](https://arxiv.org/abs/1809.01639))

See also

* {#Wikimedia}Wikimedia Foundation (n.d.). Quantum Bayesianism. [English Wikipedia](https://en.wikipedia.org/wiki/Quantum_Bayesianism).
  


[[!redirects Bayesian interpretation of quantum mechanics]]
[[!redirects Bayesian interpretations of quantum mechanics]]
[[!redirects Bayesian interpretation of quantum physics]]
[[!redirects Bayesian interpretations of quantum physics]]
[[!redirects Bayesian interpretation of physics]]
[[!redirects Bayesian interpretations of physics]]

[[!redirects quantum Bayesianism]]
[[!redirects Quantum Bayesianism]]
[[!redirects QBism]]
