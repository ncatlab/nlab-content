

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebraic Qunantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In [[perturbative quantum field theory]], the [[magnetic moment]] of [[particles]] as predicted by [[classical field theory]] may receive corrections due to [[quantum physics|quantum effects]]. Such corrections are also called _[[quantum anomalies]]_, and hence one speaks of the _anomalous magnetic moments_, traditionally denoted by "$g-2$".

The archetypical example is the anomalous magnetic moment of the [[electron]] in [[quantum electrodynamics]], which is famous as the [[pQFT]]-prediction that matches [[experiment]] to an accuracy of about $10^{-12}$ (e.g.[Scharf 95, (3.10.20)](#Scharf95)).

Similarly there is the anomalous magenetic moment $g_\mu - 2$ of the [[muon]] and the  other [[leptons]].

## Anomalies
 {#Anomalies}

In fact, the anomalous magnetic moment of the [[muon]] $g_\mu - 2$ has become notorious for apparently showing a noticeable _discrepancy_ between [[theory (physics)|theoretic prediction]] from the [[standard model of particle physics]] and its value as determined in [[experiment]]. The discrepancy is now found to have [[statistical significance]] around 3.5[[standard deviation|σ]] ([DHMZ 17](#DHMZ17)) or 4[[standard deviation|σ]] ([Jegerlehner 18a](#Jegerlehner18a)). 

In April 2021, after re-doing the Brookhaven experiment, Fermilab confirms these findings and states a statistical significance of the deviation of 4.2 sigma ([Abi et al. 21](#AbiEtAl21)).


Recent measurements may even show a possible deviation around 2.5 [[standard deviation|σ]] for the electron's anomalous magnetic moment (see [Falkowski 18](#Falkowski18)). Details depend on understanding of [[non-perturbative effects]] ([Jegerlehner 18b, section 2](#Jegerlehner18b)).

In particular, there seems to be inconsistencies in the theoretical understanding of the relevant [[lattice QCD]]-computations:

\begin{imagefromfile}
    "file_name": "LehnerMeyermug2Lattice.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -50,
        "right": 10,
        "bottom": -40,
        "left": 20
    }
\end{imagefromfile}

> graphics from [Lehner-Meyer 20, Fig 14](#LehnerMeyer20)

If these experimental "anomalies" (in the sense of [[phenomenology]]) in the anomalous magnetic moment $g_\mu - 2$ (and possibly even in $g_e -2$) are real (the established rule of thumb is that deviations are established once their [[statistical significance]] reaches 5[[standard deviation|σ]], see [here](statistical+significance#ParticlePhysics)), they point to "new physics" beyond the [[standard model of particle physics]]. 

In fact [Lyons 13b](#Lyons13b) argued that the detection-threshold of the [[statistical significance]] of anomalies here should be just 4[[standard deviation|σ]], which would mean that they should already count as being detected:

\begin{center}
<img src="https://ncatlab.org/nlab/files/LyonsGMinus2DetectionThreshold.jpg" width="600">
\end{center}

> table taken from [Lyons 13b, p. 4](#Lyons13b)

Together with the [[flavour anomalies]], these anomalies relate to the [[flavour problem]] in the [[standard model of particle physics]]:

<center>
<img src="https://ncatlab.org/nlab/files/CrivellinRandAHints.jpg" width="300">
</center>

> graphics from [Crivellin-Hoferichter 20](flavour+anomaly#CrivellinHoferichter20) 

> (here "$R$" refers to [[flavour anomalies]] in various channels, "$a$" refers to anomalies in the the [[anomalous magnetic moments]] of the [[electron]] and the [[muon]], "LFUV" is shoft for "Lepton Flavor Universality Violation", and the numbers are the [[statistical significances]] of the effects seen)





Possible explanations for the anomomalies in the anomalous magnetic moments is the existence of [[leptoquarks]] ([Bauer-Neubert 15](#BauerNeubert15), [CCDM 16](#CCDM16), [Falkowski 17](#Falkowski17), [Müller 18](#Mueller18)), which at the same time are a candidate for explaining the [[flavour anomalies]] (see also [Chiang-Okada 17](#ChiangOkada17)).


## Contributions

### QED contributions

(...)  for the [[electron]] see e.g. [Scharf 95, section 3.10](#Scharf95) (...)

### Quantum gravity contributions
 {#QuantumGravityCorrection}

The further corrections of [[loop order|1-loop]] [[perturbative quantum gravity]] to the anomalous magnetic moment of the [[electron]] and the [[muon]] have been computed in ([Berends-Gastman 75](#BerendsGastman75)) and found to be finite without need for [[renormalization]]. These [[Feynman diagrams]] contribute:

<img src="https://ncatlab.org/nlab/files/GravityVertexCorrectionsForQED.png" width="750">

### Axion contributions

Possible contributions to and xconstraints on $g_{lep}-2$ from hypothetical [[axions]] are discussed in [ACGM 08](#ACGM08), [MMPP 16](#MMPP16), [BNT 17](#BNT17)...

## Related concepts

* [[electric dipole moment]]

## References

### General

Basic discussion:

* {#Steinmann02} [[Othmar Steinmann]], _What is the Magnetic Moment of the Electron?_, Commun.Math.Phys. 237 (2003) 181-201 ([arXiv:hep-ph/0211187](https://arxiv.org/abs/hep-ph/0211187))

* Kirill Melnikov, [[Arkady Vainshtein]], _Theory of the Muon Anomalous Magnetic Moment_, Springer Tracts in Modern Physics 216, 2006

* [[Friedrich Jegerlehner]], _The Anomalous Magnetic Moment of the Muon_, Springer Tracts in Modern Physics 226, Springer-Verlag Berlin Heidelberg, 2008

Discussion of detection-threshold for the [[statistical significance]] of anomalies:


* {#Lyons13b} [[Louis Lyons]], _Discovering the Significance of 5 sigma_ ([arXiv:1310.1284](https://arxiv.org/abs/1310.1284))


See also

* Wikipedia, _[Anomalous magnetic dipole moment](https://en.wikipedia.org/wiki/Anomalous_magnetic_dipole_moment)_

Comprehensive discussion for the [[muon]]:

* T. Aoyama et al., _The anomalous magnetic moment of the muon in the Standard Model_ ([arXiv:2006.04822](https://arxiv.org/abs/2006.04822))


### Experiment and deviation

Discussion of precision experiment and possible deviation from theory:

* {#DHMZ17} Michel Davier, Andreas Hoecker, Bogdan Malaescu, Zhiqing Zhang, _Reevaluation of the hadronic vacuum polarisation contributions to the Standard Model predictions of the muon g-2 and alpha(mZ) using newest hadronic cross-section data_, Eur. Phys. J. C (2017) 77: 827 ([arXiv:1706.09436](https://arxiv.org/abs/1706.09436))

* J. L. Holzbauer on behalf of the Muon g-2 collaboration, _The Muon g-2 Experiment Overview and Status_, Proceedings for The 19th International Workshop on Neutrinos from Accelerators (NUFACT 2017) ([arXiv:1712.05980](https://arxiv.org/abs/1712.05980))

* {#Jegerlehner18a} [[Fred Jegerlehner]], _The Muon g-2 in Progress_, Acta Physica Polonica 2018 ([doi:10.5506/APhysPolB.49.1157](https://arxiv.org/ct?url=https%3A%2F%2Fdx.doi.org%2F10.5506%252FAPhysPolB.49.1157&v=01073571), [arXiv:1804.07409](https://arxiv.org/abs/1804.07409))

* {#Jegerlehner18b} [[Fred Jegerlehner]], _The Role of Mesons in Muon $g-2$_ ([arXiv:1809.07413](https://arxiv.org/abs/1809.07413))

* {#Falkowski18} [[Adam Falkowski]], _[Both $g-2$ anomalies](http://resonaances.blogspot.com/2018/06/alpha-and-g-minus-two.html)_, June 2018


* {#AbiEtAl21} B. Abi et al. (Muon g−2 Collaboration), _Measurement of the Positive Muon Anomalous Magnetic Moment to 0.46 ppm_, Phys. Rev. Lett. 126, 141801 2021 ([doi:10.1103/PhysRevLett.126.141801](https://doi.org/10.1103/PhysRevLett.126.141801))

  $\,$

  Exposition:

  Priscilla Cushman, _Muon’s Escalating Challenge to the Standard Model_,  Physics 14, 54, April 2021 ([web](https://physics.aps.org/articles/v14/54))

### Relation to flavour anomalies

Possible explanation of the anomaly in the anomalous magnetic moments in terms of [[leptoquarks]]:

* {#BauerNeubert15} Martin Bauer, Matthias Neubert, _One Leptoquark to Rule Them All: A Minimal Explanation for $R_{D^{(\ast)}}$, $R_K$ and $(g-2)_\mu$_, Phys. Rev. Lett. 116, 141802 (2016) ([arXiv:1511.01900](https://arxiv.org/abs/1511.01900))

* {#CCDM16} Estefania Coluccio Leskow, Andreas Crivellin, Giancarlo D'Ambrosio, Dario Müller, _$(g-2)_\mu$, Lepton Flavour Violation and Z Decays with Leptoquarks: Correlations and Future Prospects_, Phys. Rev. D 95, 055018 (2017) ([arXiv:1612.06858](https://arxiv.org/abs/1612.06858))

* {#BiswasShaw19} Anirban Biswas, Avirup Shaw, _Reconciling dark matter, $R_{K^{(\ast)}}$ anomalies and $(g-2)_\mu$ in an $L_\mu-L_\tau$ scenario_ ([arXiv:1903.08745](https://arxiv.org/abs/1903.08745))


* {#Falkowski17} [[Adam Falkowski]], _[Leptoquarks strike back](http://resonaances.blogspot.com/2015/11/leptoquarks-strike-back.html)_, November 2017

* {#ChiangOkada17} Cheng-Wei Chiang, Hiroshi Okada, _A simple model for explaining muon-related anomalies and dark matter_ ([arXiv:1711.07365](https://arxiv.org/abs/1711.07365))


* {#Mueller18} Dario Müller, _Leptoquarks in Flavour Physics_, EPJ Web of Conferences 179, 01015 (2018) ([arXiv:1801.03380](https://arxiv.org/abs/1801.03380))

* Junichiro Kawamura, Stuart Raby, Andreas Trautner, _Complete Vector-like Fourth Family and new $U(1)'$ for Muon Anomalies_ ([arXiv:1906.11297](https://arxiv.org/abs/1906.11297))

Further possible joint explanation of the [anomalies](anomalous+magnetic+moment#Anomalies) observed in the [[muon]] [[anomalous magnetic moment]] and the [[flavour anomalies]]:

* Geneviève Bélanger, Cédric Delaunay, Susanne Westhoff, _A Dark Matter Relic From Muon Anomalies_,  Phys. Rev. D 92, 055021 (2015) ([arXiv:1507.06660](https://arxiv.org/abs/1507.06660))

* {#ChiangOkada17} Cheng-Wei Chiang, Hiroshi Okada, _A simple model for explaining muon-related anomalies and dark matter_ ([arXiv:1711.07365](https://arxiv.org/abs/1711.07365))

* Junichiro Kawamura, Stuart Raby, Andreas Trautner, _Complete Vector-like Fourth Family and new $U(1)'$ for Muon Anomalies_ ([arXiv:1906.11297](https://arxiv.org/abs/1906.11297))

* Lorenzo Calibbi, M.L. López-Ibáñez, Aurora Melis, Oscar Vives, _Muon and electron $g-2$ and lepton masses in flavor models_ ([arXiv:2003.06633](https://arxiv.org/abs/2003.06633))

* A. S. de Jesus, S. Kovalenko, F. S. Queiroz, K. Sinha, C. Siqueira, _Vector-Like Leptons and Inert Scalar Triplet: Lepton Flavor Violation, $g-2$ and Collider Searches_ ([arXiv:2004.01200](https://arxiv.org/abs/2004.01200))

* Shaikh Saad, _Combined explanations of $(g-2)_\mu$, $R_{D^\ast}$, $R_{K^\ast}$ anomalies in a two-loop radiative neutrino mass model_ ([arXiv:2005.04352](https://arxiv.org/abs/2005.04352))

* Da Huang, António P. Morais, Rui Santos, _Anomalies in $B$ Decays and Muon $g-2$ from Dark Loops_ ([arXiv:2007.05082](https://arxiv.org/abs/2007.05082))

* K.S. Babu, P.S. Bhupal Dev, Sudip Jana, Anil Thapa, _Unified Framework for $B$-Anomalies, Muon $g-2$, and Neutrino Masses_ ([arXiv:2009.01771](https://arxiv.org/abs/2009.01771))

* Sang Quang Dinh, Hieu Minh Tran, _Muon $g-2$ and semileptonic $B$ decays in BDW model with gauge kinetic mixing_ ([arXiv:2011.07182](https://arxiv.org/abs/2011.07182))


Realization in [[F-theory]] of [[GUT]]-models with [[Z'-bosons]] and/or [leptoquarks]] addressing the [[flavour anomalies]] and the [(g-2) anomalies](anomalous+magnetic+moment#Anomalies):

* Miguel Crispim Romao, Stephen F. King, George K. Leontaris, _Non-universal $Z'$ from Fluxed GUTs_, Physics Letters B Volume 782, 10 July 2018, Pages 353-361 ([arXiv:1710.02349](https://arxiv.org/abs/1710.02349))

* A. Karozas, G. K. Leontaris, I. Tavellaris, N. D. Vlachos, _On the LHC signatures of $SU(5) \times U(1)'$ F-theory motivated models_ ([arXiv:2007.05936](https://arxiv.org/abs/2007.05936))



### QED contributions

The computation of the anomalous magnetic dipole moment of the [[electron]] in [[QED]] is spelled out (via [[causal perturbation theory]]) in 

* {#Scharf95} [[Günter Scharf]], section 3.10, culminating in (3.10.20), of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition

### QCD contribution

#### General

Discussion of [[QCD]] contributions via [[lattice QCD]]:

* {#LehnerMeyer20} Christoph Lehner, Aaron S. Meyer, _Consistency of hadronic vacuum polarization between lattice QCD and the R-ratio_ ([arXiv:2003.04177](https://arxiv.org/abs/2003.04177))

#### Via holographic QCD

Application of [[holographic QCD]] to [[anomalous magnetic moment]] of the [[muon]]:

* Luigi Cappiello, _What does Holographic QCD predict for anomalous $(g-2)_\mu$?_, 2015 ([pdf](https://agenda.infn.it/getFile.py/access?contribId=19&sessionId=5&resId=0&materialId=paper&confId=9430))


* Josef Leutgeb, Anton Rebhan, _Axial vector transition form factors in holographic QCD and their contribution to the anomalous magnetic moment of the muon_ ([arXiv:1912.01596](https://arxiv.org/abs/1912.01596))

* Josef Leutgeb, Anton Rebhan, _Axial vector transition form factors in holographic QCD and their contribution to the muon $g-2$_ ([arXiv:2012.06514](https://arxiv.org/abs/2012.06514))


### Gravity contributions

Corrections at [[loop order|1-loop]] from [[quantum gravity]] are discussed in

* {#BerendsGastman75} F. A. Berends, R. Gastmans, _Quantum gravity and the electron and muon anomalous magnetic moment_, Phys. Lett. B55 Issue 3 Feb 1975 311-312 (<a href="https://doi.org/10.1016/0370-2693(75)90608-5">doi:10.1016/0370-2693(75)90608-5</a>)

This discussion is adapted to [[supergravity]] in

* F. del Aguila, A. Culatti, R. Munoz-Tapia, M. Perez-Victoria, _Supergravity corrections to $(g-2)_l$ in differential renormalization_, Nuclear Physics  B  504  (1997)  532-550 ([arXiv:hep-ph/9702342](https://arxiv.org/abs/hep-ph/9702342))



### Axion contributions
 {#ReferencesAxionContributions}

Contribution of hypothetical [[axions]] to the [[anomalous magnetic moment]] 
of the [[electron]] and [[muon]] in [[QED]]:

* Yannis Semertzidis, _Magnetic and Electric Dipole Moments in Storage Rings_, chapter 6 of Markus Kuster, Georg Raffelt, Berta Beltrán (eds.), _Axions: Theory, cosmology, and Experimental Searches_, Lect.
Notes Phys. 741 (Springer, Berlin Heidelberg 2008) (<a href="https://doi.org/10.1007/978-3-540-73518-2_2">doi:10.1007/978-3-540-73518-2_2</a>) 

* {#ACGM08} Roberta Armillis, Claudio Coriano, Marco Guzzi, Simone Morelli, _Axions and Anomaly-Mediated Interactions: The Green-Schwarz and Wess-Zumino Vertices at Higher Orders and g-2 of the muon_, JHEP 0810:034,2008 ([arXiv:0808.1882](https://arxiv.org/abs/0808.1882))


* {#MMPP16} W.J. Marciano, A. Masiero, P. Paradisi, M. Passera, _Contributions of axion-like particles to lepton dipole moments_, Phys. Rev. D 94, 115033 (2016) ([arXiv:1607.01022](https://arxiv.org/abs/1607.01022))

* {#BNT17} Martin Bauer, Matthias Neubert, Andrea Thamm, _Collider Probes of Axion-Like Particles_, J. High Energ. Phys. (2017) 2017: 44. ([arXiv:1708.00443](https://arxiv.org/abs/1708.00443), <a href="https://doi.org/10.1007/JHEP12(2017)044">doi:10.1007/JHEP12(2017)044</a>)

The basic relevant [[Feynman diagrams]] are worked out here:

* [pdf](http://www-personal.umich.edu/~jbourj/peskin/6-3.pdf)



[[!redirects anomalous magnetic moments]]

[[!redirects anomalous magnetic dipole moment]]
[[!redirects anomalous magnetic dipole moments]]

[[!redirects electron anomalous magnetic moment]]
[[!redirects muon anomalous magnetic moment]]

[[!redirects anomalous magnetic moment of the electron]]
[[!redirects anomalous magnetic dipole moment of the electron]]

[[!redirects g-2]]