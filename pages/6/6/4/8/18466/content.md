
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

What is called _causal perturbation theory_ is a mathematically rigorous construction of _[[perturbative quantum field theory|perturbative]]_ ([[gauge theory|gauge]]-) [[quantum field theory]], such as [[quantum electrodynamics]], based on a mathematical formulation of [[renormalization]] by St&#252;ckelberg-Bogoliubov-Epstein-Glaser ([Epstein-Glaser 73](#EpsteinGlaser73)).

Causal perturbation theory may be regarded as providing a well-defined consistent generalization from [[quantum mechanics]] to [[quantum field theory]] on [[Lorentzian manifold|Lorentzian]] [[spacetimes]] of the construction of the [[S-matrix]] via the [[Dyson formula]] ("[[time-ordered products]]") in the [[interaction picture]] .

A key idea of causal perturbation theory is that the [[interaction]] term $V$ is considered multiplied with some [[smooth function]] $g$ which has [[compact support]] on [[spacetime]]. This hence serves as a spacetime-dependent "[[coupling constant]]" which "switches off" the interaction outside a compact region, but not discontinuously as in many other schemes, but smoothly, hence "adiabatically" in terminology borrowed from [[thermodynamics]]. Therefore this is often called the "[[adiabatic switching]]" function, or similar.

The corresponding [[S-matrix]] would naively be given by the [[Dyson formula]]

$$
  S_g \coloneqq T \exp\left( \int_X g(x) V(x) dvol(x) \right)
$$

for $V$ the [[interaction]] term, and "$T$" indicating the [[time-ordered product]]. Causal perturbation theory proceeds by [[axiom|axiomatizing]] the key structural properties of this "[[adiabatic switching|adiabatically switched]]" [[S-matrix]], in particular its _[[causal additivity]]_, making sense of the "[[time-ordered product]]" by appropriate [[causal locality|causal ordering]] (whence the name of the approach) and then proving by [[induction]] that solutions to these axioms exist. 

It turns out that at each step in the [[induction]] (corresponding to each loop order) a [[distribution]] has to be [extended to a point](extension%20of%20distributions#SolutionSpaceOfPointExtensions), namely to the point at which the [[interaction]] takes place. A key theorem ([Epstein-Glaser 73, section 5](#EpsteinGlaser73), [this prop.](extension+of+distributions#SpaceOfPointExtensions)) states that this extension is parameterized by a finite-dimensional space of [[point-supported distributions]] at that point. One may organize the distributions that need to be extended into [[Feynman diagrams]] ([D&#252;tsch-Fredenhagen-Keller-Rejzner 14](#DuetschFredenhagenKellerRejzner14)). This way the freedom in [[extension of distributions]] is identified with the traditional [[renormalization]] freedom in [[perturbative quantum field theory]], see at _[[main theorem of perturbative renormalization]]_ for more on this point. 

(It may be argued, vividly so in [Scharf 95, p. 181-182](#Scharf95), that the notorious "infinities" that "plague" quantum field theory in other approaches are nothing but the result of incorrectly dealing with the issue of [[extension of distributions]].)

In fact the [[interacting field algebra]] induced by the [[S-matrix]] constructed via causal perturbation theory this way is a model for [[Fedosov's formal deformation quantization]] of the given [[local Lagrangian density]] ([Collini 16](#Collini16), [Hawkins-Rejzner 16](#HawkinsRejzner16)), thus justifying the method from first principles of (perturbative) [[quantization]].


The key axiom imposed on the [[S-matrix]] in causal perturbation theory is [[causal locality]], whence the name of the approach. This axiom asks that if adiabatic switching functions $g$ and $h$ have [[spacelike]] separated [[supports]] then the S-matrix _factors_

$$
  S_{g + h} = S_g S_h
  \,.
$$  

The [[time-ordered products]] $T(..)$ of [[field (physics)|fields]] are handled by splitting of [[distributions]] using tools from [[microlocal analysis]]. This is the mathematically rigorous step that takes care of what in other approaches are the "[[ultraviolet divergences]]".

Originally the idea was that in the end the [[limit of a sequence|limit]] $g \to 1$ had to be taken, removing the adiabatic switching of the the compact support of the interaction. In general this limit does not exist ("[[infrared divergences]]", e.g. [AAS 10, section 6](#AAS10)).

But in ([Il'in-Slavnov 78](#IlinSlavnov78)) it was observed that in fact the [[algebra of observables]] on any [[bounded subsets|bounded]] region may be computed with a $g$ whose [[compact support]] contains the [[causal closure]] of that region. Later in ([Brunetti-Fredenhagen 00](#BrunettiFredenhagen00)) it was pointed out that this means that causal perturbation theory in fact serves to construct the [[causally local net of observables]] of the [[perturbative quantum field theory]] (see [this prop](S-matrix#PerturbativeQuantumObservablesIsLocalnet) for details), as in the [[axioms]] for [[AQFT]] and in fact as in the axioms of [[AQFT on curved spacetimes]], but with values in [[formal power series algebras]] (as befits a [[perturbation theory]]) instead of [[C*-algebras]] (suitable for [[non-perturbative quantum field theory]]). 

(This takes care of the "[[algebraic adiabatic limit]]", which defines the [[quantum observables]]. It does not yet in itself define the "[[weak adiabatic limit]]" for the would-be [[vacuum]] [[quantum state]].)

This way causal perturbation theory leads to a unification of [[AQFT]] [[AQFT on curved spacetimes]] with [[perturbative quantum field theory]]. This unification is now known as **[[locally covariant perturbative quantum field theory]]**, see there for more.



## Properties

### Main theorem of renormalization
 {#MainTheoremOfRenormalization}

A central result in causal perturbation theory is called the _[[main theorem of perturbative renormalization theory]]_. This says that any two _renormalization schemes_, hence any two solutions to the inductive construction of the [[S-matrix]] $V \mapsto S(V)$,  as indicated above, for [[interaction]] terms $V$, are related by a unique natural transformation $Z \colon V \to V'$

$$
  S' = S \circ Z
  \,.
$$

The collection of these operations $Z$ forms a [[group]] called the _[[Stückelberg-Petermann renormalization group]]_. 

This is a mathematical reflection of the idea that renormalization is about regarding a [[perturbative quantum field theory]] with [[interaction]] $V$ as a [[effective field theory]] at some energy scale and then discovering that at higher energy there is a more fundamental interaction $Z(V)$ which effectively looks like $V$ at lower energy.



## Related concepts

* [[locally covariant perturbative quantum field theory]]

* [[Schwinger-Tomonaga-Feynman-Dyson]]

## References
 {#References}

Lecture notes in

* [[Urs Schreiber]], _[[geometry of physics -- perturbative quantum field theory]]_

The method is due to

* {#EpsteinGlaser73} [[Henri Epstein]], [[Vladimir Glaser]], _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211 ([Numdam](http://www.numdam.org/item?id=AIHPA_1973__19_3_211_0 ))

with precursors in 

* {#Stueckelberg49} [[Ernst Stückelberg]], D. Rivier, Helv. Phys. Acta, 22 (1949) 215. 

* {#Stueckelberg51} [[Ernst Stückelberg]], J. Green, Helv. Phys. Acta, 24 (1951) 153.

* [[Ernst Stückelberg]], A. Peterman, , _La normalisation des constants dans la theorie des quanta_, Helv. Phys. Acta 26, 499 (1953); 

* {#BogoliubovShirkov59} [[Nikolay Bogoliubov]], [[Dmitry Shirkov]], _Introduction to the Theory of Quantized Fields_, New York (1959)

whence sometimes called the _St&#252;ckelberg-Bogoliubov-Epstein-Glaser method_.

The expression of causal perturbation theory in terms of [[Feynman diagram]] techniques is due to

* {#DuetschFredenhagenKellerRejzner14} [[Michael Dütsch]], [[Klaus Fredenhagen]], Kai Keller, [[Katarzyna Rejzner]], _Dimensional Regularization in Position Space, and a Forest Formula for Epstein-Glaser Renormalization_, J. Math. Phy.
55(12), 122303 (2014) ([arXiv:1311.5424](https://arxiv.org/abs/1311.5424))

That causal perturbation theory (in the generality of curved spacetimes, see [below](#ReferencesOnCurvedSpacetimes)) is equivalently the ([[Fedosov deformation quantization|Fedosov]]-)[[formal deformation quantization]] of the interacting Lagrangian density was shown for the  [[scalar field]] [[phi^4 theory]] in

* {#Collini16} [[Giovanni Collini]], _Fedosov Quantization and Perturbative Quantum Field Theory_ ([arXiv:1603.09626](https://arxiv.org/abs/1603.09626))

and for the interacting scalar field in the toy example of regular non-local interactions in 

* {#HawkinsRejzner16} [[Eli Hawkins]], [[Kasia Rejzner]], _The Star Product in Interacting Quantum Field Theory_ ([arXiv:1612.09157](https://arxiv.org/abs/1612.09157))


### On Minkowski spacetime

Causal perturbation theory has been worked out in detail for the example of [[quantum electrodynamics]] on [[Minkowski spacetime]] in

* {#Scharf95} [[Günter Scharf]], _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition

and for  [[quantum chromodynamics]] and [[perturbative quantum gravity]] on [[Minkowski spacetime]] in 

* {#Scharf01} [[Günter Scharf]], _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

Non-technical exposition of this includes

* {#Neumaier15} [[Arnold Neumaier]], _[Causal Perturbation Theory](https://www.physicsforums.com/insights/causal-perturbation-theory/)_ (2015)

* [[Arnold Neumaier]], _[Action-based quantum field theory and causal perturbation theory](https://www.mat.univie.ac.at/~neum/physfaq/topics/causalQFT.html)_ (one section in _[A theoretical physics FAQ](http://www.mat.univie.ac.at/~neum/physfaq/physics-faq.html)_)

Technical review includes

* {#AAS10} Andreas Aste, Cyrill von Arx, [[Günter Scharf]], _Regularization in quantum field theory from the causal point of view_, Prog. Part. Nucl. Phys.64:61-119, 2010 ([arXiv:0906.1952](https://arxiv.org/abs/0906.1952))

* Christian P&#246;selt, _The method of Epstein and Glaser I_, 2002 ([pdf](http://wwwthep.physik.uni-mainz.de/~scheck/Poeselt.pdf))

### On curved spacetimes
 {#ReferencesOnCurvedSpacetimes}

The generalization of causal perturbation theory to [[quantum field theory on curved spacetimes]] is developed in

* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661, 2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))

* [[Stefan Hollands]], [[Robert Wald]], _Local Wick polynomials and time ordered products of quantum fields in curved spacetime_, Communications in Mathematical Physics, 223(2):289&#8211;326, 2001 ([arXiv:gr-qc/0103074](https://arxiv.org/abs/gr-qc/0103074))

* [[Stefan Hollands]], [[Robert Wald]], _Existence of local covariant time ordered products of quantum fields in curved spacetime_, Communications in Mathematical Physics, 231(2):309&#8211;345, 2002 ([arXiv:gr-qc/0111108](https://arxiv.org/abs/gr-qc/0111108))

* [[Stefan Hollands]], [[Robert Wald]], _On the renormalization group in curved spacetime_, Communications in Mathematical Physics, 237(1-2):123&#8211;160, 2003 ([arXiv:gr-qc/0209029](https://arxiv.org/abs/gr-qc/0209029))

* [[Stefan Hollands]], [[Robert Wald]], _Conservation of the stress tensor in perturbative interacting quantum field theory in curved spacetimes_, Reviews in Mathematical Physics, 17(03):227&#8211;311, 2005 ([arXi:gr-qc/0404074](https://arxiv.org/abs/gr-qc/0404074))

* [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](http://arxiv.org/abs/0901.2038))


Review is in

* {#HollandsWald14} [[Stefan Hollands]], [[Robert Wald]], _Quantum fields in curved spacetime_, Physics Reports Volume 574, 16 April 2015, Pages 1-35 ([arXiv:1401.2026](https://arxiv.org/abs/1401.2026))


### Local covariance

The observation that the method of causal perturbation theory naturally leads to [[locally covariant perturbative quantum field theory]] is due to 

* {#IlinSlavnov78} V. A. Il'in and D. S. Slavnov, _Observable algebras in the S-matrix approach_, Theor. Math. Phys. 36 (1978) 32 ([spire](http://inspirehep.net/record/135575), [doi](http://dx.doi.org/10.1007/BF01035870))

and was re-discovered and then popularized in

* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], section 8 of _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661,2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))

Review includes

* {#FredenhagenRejzner15} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], section 4.1 of _Perturbative Construction of Models of Algebraic Quantum Field Theory_ ([arXiv:1503.07814](https://arxiv.org/abs/1503.07814))

For more on this see the references at _[[locally covariant perturbative quantum field theory]]_.


[[!redirects causal perturbation theories]]