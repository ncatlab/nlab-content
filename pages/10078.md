

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

Traditionally the [[Feynman perturbation series]]/[[scattering amplitudes]] in [[perturbative quantum field theory]] are defined, given a [[free field theory|free field]] [[vacuum]] and an [[local observable|local]] [[interaction]] [[action functional]], by applying the _[[Feynman rules]]_ ([this prop.](A+first+idea+of+quantum+field+theory#FeynmanPerturbationSeriesAwayFromCoincidingPoints)) to the monomial terms in the [[interaction]] [[Lagrangian density]] and deriving from that a rule for how to weight each [[Feynman diagram]] by a [[probability amplitude]], its _[[Feynman amplitude]]_, subject to [[renormalization]] choices.

In contrast, in what is called the _worldline formalism_ of [[perturbative quantum field theory]] this assignment is obtained instead more conceptually as the [[correlators]]/[[n-point functions]] of a 1-dimensional QFT that lives _on_ the Feynman graphs, namely the [[worldline]] theory (usually a [[sigma-model]] in the given [[target|target]] [[spacetime]]) of the [[particles]] that are the quanta of the [[field (physics)|fields]] in the field theory.

One may think of this as making explicit the [[edges]] in a [[Feynman diagram]] as corresponding to [[virtual particles]]].

Mathematically the key step here is a [[Mellin transform]] -- introducing a "[[Schwinger parameter]]" -- which realizes the [[Feynman propagator]] $\Delta_F(x,y)$ as a [[path integral]] for a [[relativistic particle]] travelling from $y$ to $x$.

This worldline formalism is equivalent to the traditional formulation. It has the conceptual advantage that it expresses the [[Feynman perturbation series]] of [[perturbative  quantum field theory]] manifestly as a [[second quantization]] of its particle content given explicitly as the [[superposition]] of all 1-particle processes.

The worldline formulation of QFT has an evident generalization to higher dimensional [[worldvolumes]]: in direct analogy one can consider summing the [[correlators]]/[[n-point functions]] over [[worldvolume]] [[theory (physics)|theories]] of "higher dimensional particles" ("[[branes]]") over all possible worldvolume geometries. Indeed, for 2-[[dimensional]] branes this is precisely the way in which [[perturbative string theory]] is defined: the [[string scattering amplitudes]] are given by the analogous "worldsheet formalism" known as the [[string perturbation series]] as the sum over all surfaces of the [[correlators]]/[[n-point functions]] of of a 2d [[SCFT]] of central charge 15.

[[!include second quantization -- table]]


Indeed, after decades of [[Feynman rules]], the worldline formalism for QFT was found only _via_ [[string theory]] in ([Bern-Kosower 91](#BernKosower91)), by looking at the point particle limit of [[string scattering amplitudes]]. 


<img src="https://ncatlab.org/nlab/files/StringFeynmanDiagrams.png" width="300">

> graphics grabbed from [Jurke 10](https://benjaminjurke.com/content/articles/2010/string-theory/)

<img src="https://ncatlab.org/nlab/files/PointParticleLimitOfStringDiagram.png" width="300">

> graphics grabbed from [Schubert 96](#Schubert96)



Then ([Strassler 92](#Strassler92), [Strassler 93](#Strassler93)) observed that generally the worldline formlism is obtained from the correlators of the 1d QFT of [[relativistic particles]] on their [[worldline]]. 

<img src="http://ncatlab.org/nlab/files/worldlineformalismoverview.jpg">

> graphics grabbed from ([Schmidt-Schubert 94](#SchmidtSchubert94))

The first calculuation along these lines was actually done earlier in ([Metsaev-Tseytlin 88](#MetsaevTseytlin88)) where the [[1-loop]] [[beta function]] for pure [[Yang-Mills theory]] was obtained as the point-particle limit of the [[partition function]] of a [[bosonic string|bosonic]] [[open string]] in a Yang-Mills [[background field]]. This provided a theoretical explanation for the observation, made earlier in ([Nepomechie 83](#Nepomechie83)) that when computed via [[dimensional regularization]] then this [[beta function]] coefficient of [[Yang-Mills theory]] vanishes in [[spacetime]] [[dimension]] 26. This of course is the critical dimension of the [[bosonic string]].


## Related entries

* [[virtual particle]]

* [string theory FAQ -- What is the relationship between quantum field theory and string theory?](string+theory+FAQ#RelationshipBetweenQuantumFieldTheoryAndStringTheory)

## References

Precursor observations include

* {#Nepomechie83} R.I. Nepomechie, _Remarks on quantized Yang-Mills theory in 26 dimensions_, Physics Letters B Volume 128, Issues 3–4, 25 August 1983, Pages 177-178 Phys. Lett. B128 (1983) 177 (<a href="https://doi.org/10.1016/0370-2693(83)90385-4">doi:10.1016/0370-2693(83)90385-4</a>)

* {#MetsaevTseytlin88} [[Ruslan Metsaev]], [[Arkady Tseytlin]], _On loop corrections to string theory effective actions_, Nuclear Physics B Volume 298, Issue 1, 29 February 1988, Pages 109-132 (<a href="https://doi.org/10.1016/0550-3213(88)90306-9">doi:10.1016/0550-3213(88)90306-9</a>)

The worldline formalism as such was first derived from the point-particle limit of [[string scattering amplitudes]] in 

* {#BernKosower91} [[Zvi Bern]], D. Kosower, _Efficient calculation of one-loop QCD amplitudes_ Phys. Rev. D 66 (1991),([journal](http://prl.aps.org/abstract/PRL/v66/i13/p1669_1))
 
* {#BernKosower92} [[Zvi Bern]], D. Kosower, _The computation of loop amplitudes in gauge theories_, Nucl. Phys. B379 (1992)  ([journal](http://ccdb4fs.kek.jp/cgi-bin/img_index?9108076))

Then it was related to actual worldline quantum field theory in 

* {#Strassler92} [[Matthew Strassler]], _Field Theory Without Feynman Diagrams: One-Loop Effective Actions_, Nucl. Phys. B385:145-184,1992 ([arXiv:hep-ph/9205205](http://arxiv.org/abs/hep-ph/9205205))
 


* {#Strassler93} [[Matthew Strassler]], _The Bern-Kosower Rules and Their Relation to Quantum Field Theory_, PhD thesis, Stanford 1993 ([spires](http://inspirehep.net/record/364079?ln=de))
 
Reviews include

* {#SchmidtSchubert94} M. G. Schmidt, [[Christian Schubert]], _The Worldline Path Integral Approach to Feynman Graphs_ ([arXiv:hep-ph/9412358](http://arxiv.org/abs/hep-ph/9412358))

* {#Schubert96} [[Christian Schubert]], _An Introduction to the Worldline Technique for Quantum Field Theory Calculations_, Acta Phys. Polon.B27:3965-4001, 1996 ([arXiv:hep-th/9610108](https://arxiv.org/abs/hep-th/9610108))

* [[Christian Schubert]], _Perturbative Quantum Field Theory in the String-Inspired Formalism_, Phys.Rept. 355 (2001) 73-234 ([arXiv:hep-th/0101036](https://arxiv.org/abs/hep-th/0101036))

* James P. Edwards, C. Moctezuma Mata, U. Müller, [[Christian Schubert]], *New techniques for worldline integration*, SIGMA 17 (2021), 065, 19 pages ([arXiv:2106.12071](https://arxiv.org/abs/2106.12071))

New techniques for worldline integration

Exposition with an eye towards [[quantum gravity]] is in

* {#Witten11} [[Edward Witten]], from 30:40 on in _Quantum Gravity_, Solomon Lefschetz Memorial Lecture Series, November 2011 ([video](https://www.youtube.com/watch?v=uRdCJMYc2Ds#t=15))

* {#Witten15} [[Edward Witten]], _What every physicist should know about string theory_, talk at [Strings2015](https://strings2015.icts.res.in)  ([pdf](https://strings2015.icts.res.in/talkDocuments/26-06-2015-Edward-Witten.pdf), [[WittenWorldlineFormalism.pdf:file]], [video recording](https://www.youtube.com/watch?v=H0jLD0PphTY))

See also:

* [[Thanu Padmanabhan]], *World-line Path integral for the Propagator expressed as an ordinary integral: Concept and Applications*, Found Phys., 51 35 (2021) ([arXiv:2104.07041](https://arxiv.org/abs/2104.07041), [doi:10.1007/s10701-021-00447-8]( https://doi.org/10.1007/s10701-021-00447-8))


Discussion of the [[Schwinger effect]] via [[worldline formalism]]:

* [[Gerald Dunne]], [[Christian Schubert]], _Worldline Instantons and Pair Production in Inhomogeneous Fields_, Phys. Rev. D72 (2005) 105004 ([arXiv:hep-th/0507174](https://arxiv.org/abs/hep-th/0507174))

Discussion for [[QCD]] with emphasis of [[2d QCD]] and [[AdS/QCD]]:

* Adi Armoni, Oded Mintakevich, _Comments on Mesonic Correlators in the Worldline Formalism_, 
 Nuclear Physics B, Volume 852, Issue 1, 1 November 2011, Pages 61-70 ([arxiv:1102.5318](https://arxiv.org/abs/1102.5318))



Further development includes

* M. G. Schmidt, [[Christian Schubert]], _Worldline Green Functions for Multiloop Diagrams_, Phys.Lett. B331 (1994) 69-76 ([arXiv:hep-th/9403158](https://arxiv.org/abs/hep-th/9403158))

* [[Eric D'Hoker]], Darius G. Gagne, _Worldline Path Integrals for Fermions with General Couplings_, Nucl.Phys. B467 (1996) 297-312 ([arXiv:hep-th/9512080](https://arxiv.org/abs/hep-th/9512080))


* C. Alexandrou, R. Rosenfelder, A. W. Schreiber, _Worldline path integral for the massive Dirac propagator: A four-dimensional approach_, Phys. Rev. A59 (1999) 1762-1776 ([arXiv:hep-th/9809101](http://arxiv.org/abs/hep-th/9809101))


* Fiorenzo Bastianelli, Olindo Corradini, Andrea Zirotti, _BRST treatment of zero modes for the worldline formalism in curved space_, JHEP 0401 (2004) 023 ([arXiv:hep-th/0312064](https://arxiv.org/abs/hep-th/0312064))

* Peng Dai, [[Warren Siegel]], _Worldline Green Functions for Arbitrary Feynman Diagrams_, Nucl.Phys.B770:107-122,2007 ([arXiv:hep-th/0608062](https://arxiv.org/abs/hep-th/0608062))

* S. A. Franchino-Viñas, S. Mignemi, _Worldline Formalism in Snyder Spaces_ ([arXiv:1806.11467](https://arxiv.org/abs/1806.11467))

* Olindo Corradini, Maurizio Muratori, _String-inspired Methods and the Worldline Formalism in Curved Space_ ([arXiv:1808.05401](https://arxiv.org/abs/1808.05401))

* Olindo Corradini, Maurizio Muratori, _A Monte Carlo Approach to the Worldline Formalism in Curved Space_ ([arXiv:2006.02911](https://arxiv.org/abs/2006.02911))



As a means of constructing [[UV-completions]]:

* Steven Abel, Nicola Andrea Dondi, _UV Completion on the Worldline_ ([arXiv:1905.04258](https://arxiv.org/abs/1905.04258))

For [[black hole]] [[scattering]]:

* Gustav Mogull, [[Jan Plefka]], Jan Steinhoff, _Classical black hole scattering from a worldline quantum field theory_ ([arXiv:2010.02865](https://arxiv.org/abs/2010.02865))


A list of more literature is at

* The Tangent Bundle, _[QFT Worldline formalism](http://www.physics.thetangentbundle.net/wiki/Quantum_field_theory/worldline_formalism)_


[[!redirects worldline formalisms]]

[[!redirects worldline theory]]
[[!redirects worldline theories]]

[[!redirects worldline method]]
[[!redirects worldline methods]]