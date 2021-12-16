

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contemts#
* table of contents
{:toc}

## Idea

In the formulation of ([[perturbative quantum field theory|perturbative]]) [[quantum field theory]] various naive mathematical constructions give rise to ill-defined "[[divergent series|divergent]]" expressions. 

Some of these occur in the [[limit of a sequence|limit]] that [[interaction]] points are taken _close_ to each other. Since the short distances involved in this limit translate, under [[Fourier transform]], to high [[frequencies]], these are called _[[ultraviolet divergences]]_. The correct way to deal with them is called _[[renormalization]]_.

Other divergences occur in the [[limit of a sequence|limit]] that the spacetime [[support]] of the [[interaction]] (the support of the "[[adiabatic switching]]") tends without bounds to all of spacetime, also called the [[adiabatic limit]]. Since the large distances involved in this limit translate, under [[Fourier transform]], to low [[frequencies]], these are called _infrared divergences_.

In [[perturbative AQFT]] the issue is dealt with by realizing that, despite superficial appearance, the [[adiabatic switching|adiabatically switched]] [[S-matrix]] already makes physical sense, namely, for the computation of those [[quantum observables]] whose [[spacetime]] [[support]] is such that its [[causal closure]] lies inside the support of the switched S-matrix ([this prop.](S-matrix#PerturbativeQuantumObservablesIsLocalnet)). This gives a well-defined meaning to [[causal perturbation theory]] _without_ having to consider the [[adiabatic limit]].

## Properties


> The [[Lee-Nauenberg theorem]] is a fundamental quantum mechanical result which provides the standard theoretical response to the problem of collinear and infrared divergences. Its argument, that the divergences due to massless charged particles can be removed by summing over degenerate states, has been successfully applied to systems with final state degeneracies such as LEP processes. If there are massless particles in both the initial and final states, as will be the case at the [[LHC]], the theorem requires the incorporation of disconnected [[Feynman diagrams|diagrams]] which produce connected interference effects at the level of the cross-section. However, this aspect of the theory has never been fully tested in the calculation of a cross-section. We show through explicit examples that in such cases the theorem introduces a divergent series of diagrams and hence fails to cancel the infrared divergences. It is also demonstrated that the widespread practice of treating soft infrared divergences by the [[Bloch-Nordsieck method]] and handling collinear divergences by the Lee-Nauenberg method is not consistent in such cases.

> ([Lavelle-McMullan 05](#LavelleMcMullan05))

## Related concepts

* [[infraparticle]]

* [[interacting vacuum]]

* [[ultraviolet divergence]]

* [[pAQFT]]


## References

Infrared divergences in [[QED]] were first observed in

* {#Mott31} N. F. Mott, _On the influence of radiative forces on the scattering of electrons_, Proc. Camb. Phil. Soc. 27, 255 (1931).

* {#BlockNordsiek37} [[Felix Bloch]] and [[Arnold Nordsieck]], _Note on the Radiation Field of the electron_, Phys. Rev. 52 , 54 (1937)

A famous approach to the problem is due to

* {#FadeevKulish70} [[Ludwig Faddeev]], P. P. Kulish, _Asymptotic conditions and infrared divergences in quantum electrodynamics_, Theoretical and Mathematical Physics June 1970, Volume 4, Issue 2, pp 745&#8211;757 ([mathnet.ru](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=tmf&paperid=4141&option_lang=eng), [springer](https://link.springer.com/article/10.1007%2FBF01066485))

But see

* Wojciech Dybalski, _From Faddeev-Kulish to LSZ. Towards a non-perturbative description of colliding electrons_ ([arXiv:1706.09057](https://arxiv.org/abs/1706.09057))

which says:

> the [Faddeev-Kulish approach](#FadeevKulish70) is justified at best by working out some test cases in perturbation theory. The question if the infrared finite [[S-matrix]] has any [[non-perturbative quantum field theory|non-perturbative]] meaning is left completely open. Secondly, the relation between the Faddeev-Kulish approach to the more standard [[LSZ scattering theory]] has never been clarified. While a naive application of the LSZ ideas clearly fails in the presence of infrared problems, a careful LSZ description of a bare electron accompanied by real and virtual photons is in fact possible.

> In the present work we outline a bridge from the Faddeev-Kulish formalism to this LSZ descriptionin the massless Nelson model.

On the [[Lee-Nauenberg theorem]]:

* {#LavelleMcMullan05} Martin Lavelle, David McMullan, _Collinearity, convergence and cancelling infrared divergences_, JHEP 0603 (2006) 026 ([arXiv:hep-ph/0511314](https://arxiv.org/abs/hep-ph/0511314))

Discussion from the point of view of [[causal perturbation theory]] / [[perturbative AQFT]]:

* {#AAS10} Andreas Aste, Cyrill von Arx, [[Günter Scharf]], section 4 of _Regularization in quantum field theory from the causal point of view_, Prog. Part. Nucl. Phys.64:61-119, 2010 ([arXiv:0906.1952](https://arxiv.org/abs/0906.1952))

* {#Duch17} [[Paweł Duch]], _Massless fields and adiabatic limit in quantum field theory_ ([arXiv:1709.09907](https://arxiv.org/abs/1709.09907))

* {#Duch19} [[Paweł Duch]], _Infrared problem in perturbative quantum field theory_ ([arXiv:1906.00940](https://arxiv.org/abs/1906.00940))


Further discussion in relation to the [[soft graviton theorem]]:

* Daniel Kapec, Malcolm Perry, Ana-Maria Raclariu, [[Andrew Strominger]], _Infrared Divergences in QED, Revisited_, Phys. Rev. D 96, 085002 (2017) ([arXiv:1705.04311](https://arxiv.org/abs/1705.04311))

* {#Strominger17} [[Andrew Strominger]], _Lectures on the Infrared Structure of Gravity and Gauge Theory_ ([arXiv:1703.05448](https://arxiv.org/abs/1703.05448))

* Neelima Agarwal, Lorenzo Magnea, Chiara Signorile-Signorile, Anurag Tripathi, *The Infrared Structure of Perturbative Gauge Theories* ([arXiv:2112.07099](https://arxiv.org/abs/2112.07099))


See also:

* Holmfridur Hannesdottir, Matthew D. Schwartz, _A Finite S-Matrix_ ([arXiv:1906.03271](https://arxiv.org/abs/1906.03271))

* Wikipedia, _[Infrared divergence](https://en.wikipedia.org/wiki/Infrared_divergence)_

[[!redirects infrared divergences]]

[[!redirects infrared divergency]]
[[!redirects infrared divergencies]]

[[!redirects IR divergency]]
[[!redirects IR divergencies]]

[[!redirects Lee-Nauenberg theorem]]
[[!redirects Lee-Nauenberg method]]

[[!redirects Bloch-Nordsieck theorem]]
[[!redirects Bloch-Nordsieck method]]

[[!redirects infrared cutoff]]
[[!redirects infrared cutoffs]]
