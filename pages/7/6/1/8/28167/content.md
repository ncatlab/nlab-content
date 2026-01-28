
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--



\tableofcontents


## Idea

In [[quantum physics]], the term *canonical quantization* refers, somewhat broadly, to [[quantization]] of (possibly [[constrained mechanics|constrained]]) [[classical mechanics|classical mechanical systems]] regarded in their [[Hamiltonian mechanics|Hamiltonian formulation]], via [[symplectic geometry]] of [[phase spaces]]. It proceeds, ideally, by construction of [[Hilbert spaces]] [[space of quantum states|of]] [[quantum states]] on which [[algebras of quantum observables]], [[Planck's constant|$\hbar$]]-[[deformation quantization|deforming]] the [[Poisson algebra]] of classical [[observables]], are [[linear representation|represented]] by [[linear operators]] (the [[Schrödinger picture of quantum mechanics]]). 

Beware that the use of "canonical" in "canonical quantization" is quite different from the use of the word in mathematics, where it refers to preferred choices. In contrast, [[deformation quantization]] of [[Poisson algebras]] is generally beset with *operator ordering* ambiguities and (beyond purely [[formal deformation quantization]]) with [[obstructions]] known as *[[quantum anomalies]]*, whence the saying that *...quantization is a mystery...* (cf. [here](Edward+Nelson#FirstQuantizationIsAMystery)).

Instead, "canonical" here refers to the older terminology of *[[canonical coordinates]]* $q$ and *[[canonical momenta]]* $p$ in [[classical mechanics|classical]] [[Hamiltonian mechanics]] (which of course are not really canonical, either), with their [[Poisson bracket]] $\{q,p\} = 1$ defined up to *[[canonical transformations]]*: In canonical quantization these are to be promoted to ([[multiplication]]) [[linear operator|operators]] $\widehat{q}$ and ([[differentiation]]) [[linear operator|operators]] $\widehat{p} (= -\mathrm{i}\hbar\partial/\partial q)$ satisfying the *[[canonical commutation relation]]* $[\widehat{q}, \widehat{p}] = \mathrm{i}\hbar$. 

But in particular when applied to [[classical field theory]], the existence of a [[Hamiltonian mechanics|Hamiltonian]] formulation crucially depends on a [[foliation]] of [[spacetime]] with [[spacelike]] leaves (or [[lightlike]] [[leaves]] for [[light cone quantization]]). While this exists at least on [[globally hyperbolic spacetimes]], such a choice breaks *manifest* local [[Lorentz group|Lorentz]]-[[symmetry]] and [[general covariance]]. Therefore canonical quantization is sometimes referred to in physics jargon as *non-covariant*. 

This is in contrast primarily to methods of quantization based on the [[Lagrangian density|Lagrangian]] formulation of [[classical mechanics]], such as notably [[path integral]] methods and their derivatives, like the construction of [[scattering amplitude]] [[S-matrices]] via [[Feynman perturbation series]] used traditionally in [[perturbative quantum field theory]].

Indeed, canonical quantization lends itself to the more elusive ambition of [[non-perturbative quantum field theory]]. 

The archetypical non-trivial example of non-perturbative canonical quantization of non-[[free field|free]] [[field theories]] is the [[quantization of Chern-Simons theory]] specifically by [[geometric quantization]] of its [[phase space]] of [[flat connections]], producing a [[modular functor]] worth of [[Hilbert spaces]] of states.


## References

### General

The origin of the idea of canonical quantization, [[deformation quantization|deforming]] [[Poisson brackets]] to [[linear operator|operator]] [[commutators]], is due to 

* [[P. A. M. Dirac]]: *The Fundamental Equations of Quantum Mechanics*, Proceedings of the Royal Society of London. Series A, Containing Papers of a Mathematical and Physical Character, Vol. 109, No. 752 (Dec. 1, 1925), pp. 642-653 &lbrack;[jstor:94441](https://www.jstor.org/stable/94441), [pdf](https://www.informationphilosopher.com/solutions/scientists/dirac/Fund_QM_1925.pdf)&rbrack;

as recalled in:

* {#Dirac1977} [[P. A. M. Dirac]]; around p. 124 of: *Recollections of an Exciting Era*, in: *Proceedings of the International School of Physics "Enrico Fermi", Course LVII, 1972--- History of Twentieth Century Physics*, Academic Press (1977) 109-146 &lbrack;[[Dirac-Recollections.pdf:file]]&rbrack;

For application in [[classical mechanics|classical]]/[[quantum mechanics]] see most references listed [there](quantum+mechanics#References).

For instance:

* Moo Youn-Han: *Canonical Quantization*, chapter 3 in: *From Photons to Higgs* (2014) 17-21 \[<a href="https://doi.org/10.1142/9789814579964_0004">doi:10.1142/9789814579964_0004</a>\]

See also:

* Wikipdia: *[Canonical quantization](https://en.wikipedia.org/wiki/Canonical_quantization)*




[[!include canonical quantization of gauge theories -- references]]







[[!redirects canonical quantizations]]

