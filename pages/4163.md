

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

What is called _perturbative quantum field theory_ (pQFT) is [[quantum field theory]] where the [[interaction]] (between [[field (physics)|fields]]/[[particles]]) is treated as a tiny [[perturbation]] of the "[[free field theory]]" where no [[interaction]] is assumed to take place ("[[perturbation theory]]"). This is meant to be an approximation to the actual _[[non-perturbative quantum field theory]]_. However, the latter remains elusive except for toy examples of low spacetime dimension, vanishing [[interaction]] and/or [[topological field theory|topological invariance]] and most of the "quantum field theory" in the literature is tacitly understood to be perturbative.

Hence pQFT studies the _[[infinitesimal neighbourhood]]_ (also called the _[[formal neighbourhood]]_) of [[free quantum field theories]] in the space of all quantum field theories. Mathematically this means that the resulting [[quantum observables]] are [[formal power series]] in the [[coupling constant]]  $g$ which measures the strength of the [[interaction]] (as well as in _[[Planck's constant]]_, which measures the general strength of [[quantum physics|quantum]]). This distinguishes perturbative quantum field theory from [[non-perturbative quantum field theory]], where the algebras of [[quantum observables]] are supposed to be not formal power series algebras, but [[C*-algebras]].

The key object of perturbative QFT is the perturbative _[[scattering matrix]]_ which expresses, as a [[formal power series]] in the ratio of the [[coupling constant]] over [[Planck's constant]], the [[probability amplitude]] of [[scattering]] processes, namely of processes where [[free field theory|free fields]] in a certain [[quantum state|state]] come in from the far past, interact and hence scatter off each other, and then go off in some other [[quantum state]] into the far future. The [[scattering cross sections]] thus defined are the quantities which may be directly measured in scattering [[experiments]], such as the [[LHC]] accelerator.

The perturbative [[S-matrix]] turns out to have an expression as a sum over separate [[scattering amplitudes]] for elementary processes labeled by _[[Feynman diagrams]]_, each of which depicts one specific way for fields ([[particles]]) to interact with each other. That the full S-matrix is the sum over all amplitudes for all these possible scattering processes, the _[[Feynman perturbation series]]_, is an incarnation of the informal heuristic of the [[path integral]] and the [[superposition principle]] in [[quantum physics]], which says that the [[probability amplitude]] for a specific outcome is the sum over the probability amplitudes of all the possible processes that can contribute to this outcome. 

For all interesting [[interacting field theories]], such as [[quantum electrodynamics]] and [[quantum chromodynamics]], this [[scattering matrix]] [[formal power series]] necessarily has _vanishing_ [[radius of convergence]] ([Dyson 52](#Dyson52)). If it is assumed that the [[formal power series|formal]] [[Feynman perturbation series]] is the [[Taylor series]] of an actual [[smooth function]] given by the actual [[non-perturbative quantum field theory]] that is being approximated, then this means that it is at least an [[asymptotic series]] (by [this example](asymptotic+series#TaylorSeriesOfSmoothFunctionIsAsymptoticSeries)) whose first couple of terms could sum to a good approximation of the actual value to be computed. Indeed, the sum of the first few [[loop orders]] in the [[S-matrix]] for  [[QED]] and [[QCD]] in the [[standard model of particle physics]] turns out to be in agreement with [[experiment]] to good precision. 

(There are however known [[non-perturbative effects]] which are not captured in perturbation theory, such as [[confinement]] in [[QCD]], supposed related to [[instantons in QCD]]. In [[resurgence theory]] one tries to identify these from the [[asymptotic series|asymptotic]] nature of the [[Feynman perturbation series]].)

A key step in the construction of perturbative quantum field theory is the _[[renormalization]]_ of the point interactions. This comes about because given

1. a [[local Lagrangian density]] defining the nature of the [[field (physics)|fields]] and their [[interactions]], 

1. a [[vacuum state]] (generally: [[Hadamard state]]) that defines the [[free field theory|free]] [[quantum field theory]] to be perturbed about

it turns out that the construction of the perturbative [[S-matrix]] (the [[Feynman perturbation series]]) still involves at each order a finite-dimensional space of choices to be made. Physically, these are the specification of further high energy interactions not seen in the original [[local Lagrangian density]]; mathematically, this is the choice of extending the [[time-ordered product]] of the interaction, which is an [[operator-valued distribution]], to the locus of coinciding interaction points, in the sense of [[extensions of distributions]].

Historically, perturbative quantum field theory as originally conceived informally by [[Schwinger-Tomonaga-Feynman-Dyson]] in the 1940s, had been notorious for the mysterious conceptual nature of its mathematical principles ("divergences"). The mathematically rigorous formulation of [[renormalization]] ("removal of [[UV-divergences]]") in perturbative quantum field theory on [[Minkowski spacetime]] was established by [Epstein-Glaser 73](#EpsteinGlaser73), based on [Bogoliubov-Shirkov 59](#BogoliubovShirkov59) and [St&#252;ckelberg 51](#Stueckelberg51)), now known as **[[causal perturbation theory]]**; laid out in the seminal Erice summer school proceeding ([Velo-Wightman 76](#VeloWightman76)).

The correct definition of the [[adiabatic switching|adiabatic limit]] ("removal of IR divergencies") was understood in [Il'in-Slavnov 78](#IlinSlavnov78) and eventually developed by [D&#252;tsch-Fredenhagen 01](#DuetschFredenhagen01), [Brunetti-D&#252;tschFredenhagen 09](#BrunettiDuetschFredenhagen09), this is now called **[[perturbative algebraic quantum field theory]]**. 
The rigorous derivation of the previously informal [[Feynman rules]] and their [[dimensional regularization]] for computation of [[scattering amplitudes]] was achieved in [Keller 10 (IV.12)](#Keller10), [D&#252;tsch-Fredenhagen-Keller-Rejzner 14](#DuetschFredenhagenKellerRejzner14).
Quantization of [[gauge theories]] ([[Yang-Mills theory]]) in [[causal perturbation theory]]/[[perturbative AQFT]] was then discussed (for trivial [[principal bundles]] and restricted to [[gauge invariant observables]]) in the spirit of [[BRST-complex]]/[[BV-formalism]] in ([Fredenhagen-Rejzner 11b](#FredenhagenRejzner11b)).
The generalization of all these constructions from [[Minkowski spacetime]] to perturbative quantum fields on more general [[spacetimes]] (i.e. for more general [[gravity|gravitational]] [[background fields]] such as appearing in [[cosmology]] or [[black hole]] physics) was made possible due to the identification of the proper generalization of [[vacuum states]] and their [[Feynman propagators]] to [[Hadamard states]] on [[globally hyperbolic spacetimes]] in [Radzikowski 96](#Radzikowski96). The resulting rigorous perturbative [[QFT on curved spacetimes]] was developed in a long series of articles by [[Stefan Hollands|Hollands]], [[Robert Wald|Wald]], [[Romeo Brunetti|Brunetti]], [[Klaus Fredenhagen|Fredenhagen]] and others, now called _[[locally covariant perturbative AQFT]]_. 

While this establishes a rigorous construction of perturbative quantum field theory on general gravitational backgrounds, the construction principles had remained somewhat ad-hoc: The [[axioms]] for the perturbative [[S-matrix]] (equivalently for the [[time-ordered products]] or [[retarded products]] of field operators) were well motivated by comparison with the [[Dyson series]] in [[quantum mechanics]], by the heuristics of the [[path integral]] and not the least by their excellent confirmation by [[experiment]], but had not been derived from first principles of [[quantization]].  Then in [D&#252;tsch Fredenhagen 01](#DuetschFredenhagen01) it was observed that the [[Wick algebras]] of [[quantum observables]] in [[free quantum field theory]] are equivalently the [[Moyal deformation quantization]] of the canonical [[Poisson bracket]] (the _[[Peierls bracket]]_ or _[[causal propagator]]_) on the [[covariant phase space]] of the free field theory (or rather of a choice of [[Hadamard state]] for it) and [Collini 16](#Collini16) showed that under suitable conditions the perturbative [[interacting observable algebra]] is the [[Fedosov deformation quantization]] of [[covariant phase space]] of the interacting theory. A general argument to this extent was given in [Hawkins-Rejzner 16](#HawkinsRejzner16).

This suggests that the construction of the full [[non-perturbative quantum field theory]] ought to be given by a [[strict deformation quantization]] of the [[covariant phase space]]. But presently no example of such for non-trivial interaction in [[spacetime]] [[dimension]] $\geq 4$ is known.
In particular the [[phenomenology|phenomenologically]] interesting case of a complete construction of interacting field theories on 4-dimensional spacetimes is presently unknown. For the case of [[Yang-Mills theory]] this open problem to go beyond perturbative quantum field theory is one of the "Millennium Problems" (see at _[[quantization of Yang-Mills theory]]_). For the case of [[quantum gravity]] this is possibly the $10^4$-year problem that the field is facing. But observe that as a perturbative ([[effective quantum field theory|effective]]") quantum field theory, [[quantum gravity]] does fit into the framework of  perturbative QFT, is mathematically well-defined and makes predictions, see the references [there](quantum%20gravity#ReferencesAsAnEffectiveFieldTheory).

## Details

A comprehensive introduction is at _[[geometry of physics -- perturbative quantum field theory]]_.


## Properties

* [[main theorem of perturbative renormalization theory]]

## Related concepts

* [[renormalization]], [[radiative correction]]

* [[causal perturbation theory]], [[perturbative AQFT]]

[[!include products in pQFT -- table]]


* [[non-perturbative field theory]]

## References

### General

The original informal conception of perturbative QFT is due to [[Schwinger-Tomonaga-Feynman-Dyson]]:

* {#Dyson49} [[Freeman Dyson]], _The raditation theories of Tomonaga, Schwinger and Feynman_, Phys. Rev. 75, 486, 1949 ([pdf](http://web.ihep.su/dbserv/compas/src/dyson49b/eng.pdf))


The rigorous formulation of renormalized perturbative quantum field theory in terms of [[causal perturbation theory]] was first accomplished in 

* {#EpsteinGlaser73} [[Henri Epstein]], [[Vladimir Glaser]], _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211 ([Numdam](http://www.numdam.org/item?id=AIHPA_1973__19_3_211_0 ))

with precursors in

* {#Stueckelberg49} [[Ernst Stückelberg]], D. Rivier, Helv. Phys. Acta, 22 (1949) 215. 

* {#Stueckelberg51} [[Ernst Stückelberg]], J. Green, Helv. Phys. Acta, 24 (1951) 153.

* [[Ernst Stückelberg]], A. Peterman, , _La normalisation des constants dans la theorie des quanta_, Helv. Phys. Acta 26, 499 (1953); 

* {#BogoliubovShirkov59} [[Nikolay Bogoliubov]], [[Dmitry Shirkov]], _Introduction to the Theory of Quantized Fields_, New York (1959)

A seminal compilation of the resulting rigorous understanding of [[renormalization]] is

* {#VeloWightman76} G. Velo and [[Arthur Wightman]] (eds.) _Renormalization Theory_ Proceedings of the 1975 Erice summer school, NATO ASI Series C 23, D. Reidel, Dordrecht, 1976

Concrete computations in rigorous [[causal perturbation theory]] have been spelled out for [[quantum electrodynamics]] in

* {#Scharf95} [[Günter Scharf]], _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition

and for [[Yang-Mills theory]], [[quantum chromodynamics]] and [[perturbative quantum gravity]] in

* {#Scharf01} [[Günter Scharf]], _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

The treatment of the IR-divergencies by organizing the perturbative [[quantum observables]] into a [[local net of observables]] was first suggested in

* {#IlinSlavnov78} V. A. Il'in and D. S. Slavnov, _Observable algebras in the S-matrix approach_, Theor. Math. Phys. 36 (1978) 32 ([spire](http://inspirehep.net/record/135575), [doi](http://dx.doi.org/10.1007/BF01035870))

and then developed to _[[perturbative algebraic quantum field theory]]_ in

* {#DuetschFredenhagen01} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Algebraic Quantum Field Theory, Perturbation Theory, and the Loop Expansion_, Commun. Math. Phys. 219 (2001) 5-30 ([arXiv:hep-th/0001129](https://arxiv.org/abs/hep-th/0001129))

* {#BrunettiDuetschFredenhagen09} [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](http://arxiv.org/abs/0901.2038))

Quantization of [[gauge theories]] ([[Yang-Mills theory]]) in [[causal perturbation theory]]/[[perturbative AQFT]] is discussed (for trivial [[principal bundles]] and restricted to [[gauge invariant observables]]) in the spirit of [[BRST-complex]]/[[BV-formalism]] in

* {#FredenhagenRejzner11a} [[Klaus Fredenhagen]], [[Kasia Rejzner]], _Batalin-Vilkovisky formalism in the functional approach to classical field theory_, Commun. Math. Phys. 314(1), 93&#8211;127 (2012) ([arXiv:1101.5112](https://arxiv.org/abs/1101.5112))

* {#FredenhagenRejzner11b} [[Klaus Fredenhagen]], [[Kasia Rejzner]], _Batalin-Vilkovisky formalism in perturbative algebraic quantum field theory_, Commun. Math. Phys. 317(3), 697&#8211;725 (2012) ([arXiv:1110.5232](https://arxiv.org/abs/1110.5232))

and surveyed in:

* {#Rejzner16} [[Kasia Rejzner]], section 7 of _[[Perturbative Algebraic Quantum Field Theory]]_, Springer 2016

* [[Urs Schreiber]], _[[geometry of physics -- perturbative quantum field theory]]_, 2017

* {#Duetsch18} [[Michael Dütsch]], _[[From classical field theory to perturbative quantum field theory]]_, 2018





The generalization of all these constructions to quantum fields on general [[globally hyperbolic spacetimes]] (perturbative [[AQFT on curved spacetimes]]) was made possible by the results on [[Hadamard states]] and [[Feynman propagators]] in

* {#Radzikowski96} [[Marek Radzikowski]], _Micro-local approach to the Hadamard condition in quantum field theory on curved space-time_, Commun. Math. Phys. 179 (1996), 529&#8211;553 ([Euclid](http://projecteuclid.org/euclid.cmp/1104287114))

and then developed in a long series of articles by [[Stefan Hollands]], [[Robert Wald]], [[Romeo Brunetti]], [[Klaus Fredenhagen]] and others. For this see the references at _[[AQFT on curved spacetimes]]_.


The observation that perturbative quantum field theory is equivalently the [[formal deformation quantization]] of the defining [[local Lagrangian density]] is for [[free field theory]] due to

* {#DuetschFredenhagen01} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative algebraic quantum field theory and deformation quantization_, Proceedings of the Conference on Mathematical Physics in Mathematics and Physics, Siena June 20-25 (2000) ([arXiv:hep-th/0101079](http://xxx.uni-augsburg.de/abs/hep-th/0101079)) 

* {#HirschfeldHenselder02} A. C. Hirshfeld, P. Henselder, _Star Products and Perturbative Quantum Field Theory_, Annals Phys. 298 (2002) 382-393 ([arXiv:hep-th/0208194](https://arxiv.org/abs/hep-th/0208194))


and for interacting field theories ([[causal perturbation theory]]/[[perturbative AQFT]]) due

* {#Collini16} [[Giovanni Collini]], _Fedosov Quantization and Perturbative Quantum Field Theory_ ([arXiv:1603.09626](https://arxiv.org/abs/1603.09626))

* {#HawkinsRejzner16} [[Eli Hawkins]], [[Kasia Rejzner]], _The Star Product in Interacting Quantum Field Theory_ ([arXiv:1612.09157](https://arxiv.org/abs/1612.09157))


For more see the references at _[[perturbative algebraic quantum field theory]]_.

The relation of the construction via [[causal perturbation theory]] to the [[Feynman perturbation series]] in terms of [[Feynman diagrams]] was understood in 

* {#GarciaBondiaLazzarini00} [[Jose Gracia-Bondia]], S. Lazzarini, _Connes-Kreimer-Epstein-Glaser Renormalization_ ([arXiv:hep-th/0006106](https://arxiv.org/abs/hep-th/0006106))

* {#Keller10} [[Kai Keller]], chapter IV of _Dimensional Regularization in Position Space and a Forest Formula for Regularized Epstein-Glaser Renormalization_, PhD thesis ([arXxiv:1006.2148](https://arxiv.org/abs/1006.2148))

* {#DuetschFredenhagenKellerRejzner14} [[Michael Dütsch]], [[Klaus Fredenhagen]], [[Kai Keller]], [[Katarzyna Rejzner]], _Dimensional Regularization in Position Space, and a Forest Formula for Epstein-Glaser Renormalization_, J. Math. Phy.
55(12), 122303 (2014) ([arXiv:1311.5424](https://arxiv.org/abs/1311.5424))

Non-rigorous but widely used textbooks:

* [[Michael Peskin]], [[Daniel Schroeder]], _An Introduction to Quantum Field Theory_, 1995 ([spire:407703](https://inspirehep.net/literature/407703), [ISBN 9780201503975](https://www.routledge.com/An-Introduction-To-Quantum-Field-Theory/Peskin-Schroeder/p/book/9780201503975))

(...)


### Non-convergence of the perturbation series
 {#ReferencesNonConvergenceOfThePerturbationSeries}

The argument that the perturbation series of realistic pQFTs necessarily [[divergent series|diverges]], in fact has vanishing [[radius of convergence]] (is at best an [[asymptotic series]]) goes back to 

* {#Dyson52} [[Freeman Dyson]], _Divergence of perturbation theory in quantum electrodynamics_, Phys. Rev. 85, 631, 1952 ([spire](http://inspirehep.net/record/29799?ln=en))

and is made more precise in

* {#Lipatov77} [[Lev Lipatov]], _Divergence of the Perturbation Theory Series and the Quasiclassical Theory_, Sov.Phys.JETP 45 (1977) 216&#8211;223 ([pdf](http://jetp.ac.ru/cgi-bin/dn/e_045_02_0216.pdf))

recalled for instance in 

* {#Suslov05} [[Igor Suslov]], section 1 of _Divergent perturbation series_, Zh.Eksp.Teor.Fiz. 127 (2005) 1350; J.Exp.Theor.Phys. 100 (2005) 1188 ([arXiv:hep-ph/0510142](https://arxiv.org/abs/hep-ph/0510142))

* Justin Bond, last section of _Perturbative QFT is Asymptotic; is Divergent; is Problematic in Principle_ ([pdf](https://mcgreevy.physics.ucsd.edu/s13/final-papers/2013S-215C-Bond-Justin.pdf))

* {#FloryHellingSluka12} Mario Flory, [[Robert C. Helling]], Constantin Sluka, Section 2 of: *How I Learned to Stop Worrying and Love QFT* ([arXiv:1201.2714](https://arxiv.org/abs/1201.2714))

* {#HollandsWald14} [[Stefan Hollands]], [[Robert Wald]], section 4.1 of _Quantum fields in curved spacetime_, Physics Reports Volume 574, 16 April 2015, Pages 1-35 ([arXiv:1401.2026](https://arxiv.org/abs/1401.2026))

* Marco Serone, from 2:46 on in _A look at $\phi^4_2$ using perturbation theory_ ([recording](https://www.youtube.com/watch?v=J4nxvY1rOhI))

The argument that the perturbation series should be trustworthy for number of terms smaller than the inverse of the [[coupling constant]] is recalled in [Flory, Helling & Sluka 2012, p. 8 & eq. (34) & Sec. 2.5](#FloryHellingSluka12).

Exposition also in:

* [[Jakob Schwichtenberg]], *[divergence-perturbation-series-qft](http://jakobschwichtenberg.com/divergence-perturbation-series-qft)*


For the example of [[phi^4 theory|$\phi^4$-theory]] this non-convergence of the perturbation series is discussed in

* {#Helling} [[Robert C. Helling]], p. 4 of _Solving classical field equations_ ([pdf](http://homepages.physik.uni-muenchen.de/~helling/classical_fields.pdf), [[HellingClassicalQFT.pdf:file]])

* {#BakulevShirkov10} Alexander P. Bakulev, [[Dmitry Shirkov]], section 1.1 of _Inevitability and Importance of Non-Perturbative Elements in Quantum Field Theory_, Proceedings of the 6th Mathematical Physics Meeting, Sept. 14--23, 2010, Belgrade, Serbia (ISBN 978-86-82441-30-4), pp. 27--54 ([arXiv:1102.2380](https://arxiv.org/abs/1102.2380)) 

See also

* Carl M. Bender, Carlo Heissenberg, _Convergent and Divergent Series in Physics_ ([arXiv:1703.05164](https://arxiv.org/abs/1703.05164))

And see at _[[perturbation theory]] -- [On divergence/convergence](perturbation+theory#ReferencesDivergenceConvergence)_ 

{#ReferencesBreakdownAtLargeNumberOfInsertions} Discussion of further issues, even when [[resummation]] is thought to apply, arising for [[n-point functions]] at large $n$ (large number of external particles in a scattering process):

failure of unitarity (for [[phi^n interaction|$\phi^n$-theory]]):

* Sebastian Schenk, *The Breakdown of Resummed Perturbation Theory at High Energies* ([arXiv:2109.00549](https://arxiv.org/abs/2109.00549))

failure of [[locality]] (for [[perturbative quantum gravity]] and [[perturbative string theory]]):

* [[Sudip Ghosh]], [[Suvrat Raju]], *Loss of locality in gravitational correlators with a large number of insertions*, Phys. Rev. D 96, 066033 (2017) ([arXiv:1706.07424](https://arxiv.org/abs/1706.07424)) 

* [[Sudip Ghosh]], [[Suvrat Raju]], *The Breakdown of String Perturbation Theory for Many External Particles*, Phys. Rev. Lett. 118, 131602 (2017) ([arXiv:1611.08003](https://arxiv.org/abs/1611.08003))






### L-infinity algebra structure

Further identification of [[L-infinity algebra]]-[[structure]] in the [[Feynman amplitudes]]/[[S-matrix]] of [[Lagrangian field theory|Lagrangian]] [[perturbative quantum field theory]]:

* {#Froeb18} [[Markus Fröb]], _Anomalies in time-ordered products and applications to the BV-BRST formulation of quantum gauge theories_ ([arXiv:1803.10235](https://arxiv.org/abs/1803.10235))

* {#Arvanitakis19} [[Alex Arvanitakis]], _The $L_\infty$-algebra of the S-matrix_ ([arXiv:1903.05643](https://arxiv.org/abs/1903.05643))



[[!redirects perturbative quantum field theories]]


[[!redirects perturbative field theory]]
[[!redirects perturbative field theorys]]

[[!redirects perturbative QFT]]
[[!redirects perturbative QFTs]]


[[!redirects pQFT]]
[[!redirects pQFTs]]



