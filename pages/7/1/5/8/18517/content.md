

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea


### Adiabatic switching

In [[perturbative quantum field theory]], the term _adiabatic switching_ refers to considering a smooth transition between vanishing and non-vanishing [[interaction]] [[coupling constant|coupling]]: the interactions is slowly, hence (borrowing a term from [[thermodynamics]]) "adiabatically", switched on or off. This is mostly a mathematical device, not meant to directly reflect a physical situation of changing coupling, but it does serve to construct physical quantities. This is closely related to the role of [[operator-valued distributions]] which are quantities that give well defined [[linear operators]] (hence [[quantum observables]]) only when evaluated on any [[bump function]].

Originally adiabatic switching was considered ([Lippmann-Schwinger 50](#LippmannSchwinger50)) only in the [[time]]-direction (for a fixed choice of time on [[Minkowski spacetime]]) by multiplying the [[interaction]] term of the [[Lagrangian density]]/[[Hamiltonian]] by the [[exponential]] $\exp(- \epsilon {\Vert t \Vert})$ (for $\epsilon \in (0,\infty)$ a [[positive number|positive]] [[real number]] and for ${\Vert t\Vert}$ the [[absolute value]] of the time [[coordinate]]). Review is for instance in ([Strocchi 13, section 6.3](#Strocchi13)).

Using this, the _Gell-Mann and Low formula_ ([Gell-Mann & Low 51](#GellMannLow51), see [Molinari 06](#Molinari06)) expresses the [[eigenstates]] $\vert \psi \rangle$ of an interacting [[Hamiltonian]] $H = H_{free} + H_{int}$ in terms of the eigenstates $\vert \Psi_{free} \rangle$ of the free Hamiltonian by the "adiabatic limit"
 
$$
  \vert \Psi^{\pm}_{int} \rangle 
  \;\propto\;
  \underset{\epsilon \to 0}{\lim}
  S_\epsilon(0, \pm \infty)
  \vert \Psi_{free} \rangle
$$

(if the [[limit of a sequence|limit]] exists) where $S_\epsilon$ denotes the [[S-matrix]] of the adiabatically switched Hamiltonian $H_\epsilon \coloneqq H_{free} + e^{- \epsilon {\Vert t\Vert}}H_{int}$.

More generally, one may consider adiabatic switching taking place not just in time, but in all of [[spacetime]]. This the basis of [[causal perturbation theory]] and [[locally covariant perturbative quantum field theory]]:

In the construction of [[perturbative quantum field theory]] via the method of [[causal perturbation theory]] the [[interaction]] terms $L_{int}$ used in the mathematical construction of the [[S-matrix]] are multiplied with a "[[coupling constant]]" $g$ which is in fact taken to be a [[smooth function]] of [[compact support]] on [[spacetime]], hence a [[bump function]]:

$$
  L_g = L_{free} + g L_{int}
  \,.
$$

This means that the the [[interaction]] as modeled by the [[S-matrix]]

$$
  S_g \coloneqq T \exp( \tfrac{i}{\hbar} \int_{X} g :L_{int}(x): )
$$

is non-trivial only on a [[compact topological space|compact]] [[subspace]] of [[spacetime]], towards its boundary it smoothly drops to zero. Hence outside this region the interaction is "switched off".

Since the actual interactions in [[physics]] are of course _not_ "switched off" anywhere, the use of an adiabatic switching is just an intermediate mathematical step.
Originally in ([Epstein-Glaser 73](#EpsteinGlaser73)) the idea was that after having constructed the [[S-matrix]] for any adiabatic switching $g$, the [[limit of a sequence|limit]] ("adiabatic limit") $g \to 1$ had to be taken to remove the switching in the end. Failure of this limit to exist is interpreted as "[[infrared divergency]]" of the [[perturbative quantum field theory]] (since the divergency comes from large scales, hence long [[wavelength]]).

But as observed in ([Il'in-Slavnov 78](#IlinSlavnov78)) and rediscovered in ([Brunetti-Fredenhagen 00](#BrunettiFredenhagen00)), an adiabatic switching map that is unity on a globally hyperbolic sub-spacetime $O \subset X$ is sufficient to compute the perturbative [[interacting field algebra]], hence the [[algebra of quantum observables]] $A(O)$ on that subspace, and the collection of all of these as $O$ ranges forms a [[causally local net of observables]] which fully captures the [[quantum field theory]] in the sense of the [[Haag-Kastler axioms]] ([this prop.](S-matrix#PerturbativeQuantumObservablesIsLocalnet)). This perspective is now known as _[[locally covariant algebraic quantum field theory]]_.

### Adiabatic limit

The [[limit of a sequence|limit]] of the [[perturbative S-matrix]] as the [[adiabatic switching]] is removed (if it exists) is called the _adiabatic limit_ or _strong adiabatic limit_.

If one just asks that the corresponding limit exists for the [[n-point functions]] one speaks of a _weak adiabatic limit_.

Even with the adiabatically switched S-matrix elements (not taking a limit) the [[local net of quantum observables]] is well defined ([this prop.](S-matrix#PerturbativeQuantumObservablesIsLocalnet)), this is hence a [[functor]]

$$
  \mathcal{O} \mapsto \mathcal{A}(\mathcal{O})
$$

that assigns [[algebras of observables]] to [[causally closed subsets]] of [[spacetime]]. The [[colimit]] algebra 

$$
  \mathcal{A} \coloneqq \underset{\underset{\mathcal{O}}{\longrightarrow}}{\lim} \mathcal{A}(\mathcal{O})
$$

over this [[functor]] (in the sense of [[category theory]]) always exists. This is also called the _algebraic adiabatic limit_.
 
(See around [Duch 17, section 4](#Duch17) for review of strong, weak and algebraic adiabaitc limit; and [Duch 17, chapter II](#Duch17) for results on the weak adiabatic limit)

Here 

1. the _algebraic adiabatic_ limit defines the _[[quantum observables]]_ in the limit;

1. the weak adiabatic limit may serve to define also the _[[state on a star-algebra|states]]_, hence the [[interacting vacuum]] ([Duch 17, p. 113-114](#Duch17)).

## References

The concept of adiabatic switching in the time direction was introduced in

* {#LippmannSchwinger50} B. A. Lippmann, [[Julian Schwinger]], *Variational Principles for Scattering Processes. I*,  Phys. Rev. 79, 469 (1950) ([doi:10.1103/PhysRev.79.469](https://doi.org/10.1103/PhysRev.79.469))

reviewed for instance in

* {#Strocchi13} [[Franco Strocchi]], section 6.3 of _An Introduction to Non-Perturbative Foundations of Quantum Field Theory_, Oxford University Press, 2013

and the corresponding formula for the interacting eigenstates in terms of the free ones is due to

* {#GellMannLow51} [[Murray Gell-Mann]], F. Low, _Bound states in quantum field theory_ Phys. Rev. 84, 350 (1951)

* [[Murray Gell-Mann]], M. L. Goldberger, Phys. Rev. 91 398 (1953)

see

* {#Molinari06} Luca Guido Molinari, _Another proof of Gell-Mann and Low's theorem_, Journal of Mathematical Physics 48, 052113, 2007 ([arXiv:math-ph/0612030](https://arxiv.org/abs/math-ph/0612030))

* Wikipedia, _[Gell-Mann and Low theorem](https://en.wikipedia.org/wiki/Gell-Mann_and_Low_theorem)_

The generalization to switching in all space-time directions was considered for the construction of [[causal perturbation theory]] in 

* {#EpsteinGlaser73} [[Henri Epstein]] and [[Vladimir Glaser]], _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211.

The observation that this in  fact makes causal perturbation theory a tool for constructing [[local nets of observables]] for [[locally covariant perturbative quantum field theory]] is due to

* {#IlinSlavnov78} V. A. Il'in and D. S. Slavnov, _Observable algebras in the S-matrix approach_, Theor. Math. Phys. 36 (1978) 32.

* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661,2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))

The term "algebraic adiabatic limit" for the resulting [[local net of observables]] (or its [[inductive limit]]) appears in

* {#FredenhagenLindner13} [[Klaus Fredenhagen]], [[Falk Lindner]], p. 7 of _Construction of KMS States in Perturbative QFT and Renormalized Hamiltonian Dynamics_, Communications in Mathematical Physics Volume 332, Issue 3, pp 895-932, 2014 ([arXiv:1306.6519](https://arxiv.org/abs/1306.6519))

The weak adiabatic limit in [[causal perturbation theory]] for massive fields was shown to exists in 

* [Epstein-Glaser 73](#EpsteinGlaser73)

Extension of this result to [[quantum electrodynamics]] and [[phi^4 theory]] was given in

* {#BlanchardSeneor75} P. Blanchard and R. Seneor, _Green’s functions for theories with massless particles (in perturbation theory)_, Ann. Inst. H. Poincaré Sec. A
23 (2), 147–209 (1975) ([Numdam](http://www.numdam.org/item?id=AIHPA_1975__23_2_147_0))

See also

* {#Scharf95} [[Günter Scharf]], section 3.11 of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition

Further extension of the result is due to

* {#Duch17} [[Paweł Duch]], _Massless fields and adiabatic limit in quantum field theory_ ([arXiv:1709.09907](https://arxiv.org/abs/1709.09907))

[[!redirects adiabatic switchings]]

[[!redirects Gell-Mann and Low formula]]

[[!redirects adiabatic limit]]
[[!redirects adiabatic limits]]

[[!redirects algebraic adiabatic limit]]
[[!redirects algebraic adiabatic limits]]

[[!redirects strong adiabatic limit]]
[[!redirects strong adiabatic limits]]

[[!redirects weak adiabatic limit]]
[[!redirects weak adiabatic limits]]
