
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The phenomenon or principle called _vector meson dominance_ (VMD) is a tight relation between [[quantum hadrodynamics]] and [[quantum electrodynamics]], where the electrically neutral [[light meson|light]] [[vector meson]] [[field (physics)|fields]] $V_\mu$ (the neutral [[rho-meson]] $\rho^0_\mu$, the [[omega-meson]] $\omega_\mu$ and the [[phi-meson]]) are seen to be on par with, or even identified with, the [[electromagnetism|electromagnetic]] [[hadronic current]] $J^{hadr}$, at least to some approximation.

### Phenomenology
 {#Phenomenology}

In [[particle physics]] [[phenomenology]], _vector meson dominance_ is the observation that the [[interaction]] of [[hadrons]] with [[photons]] is dominated by [[interactions]] that procceed via excange of [[vector mesons]]. 

Specifically, the [[decay]] of [[electron]]/[[positron]]-[[pairs]] into [[hadrons]]  

$$
  e^+ + e^- \to H
$$

(reverse to the [[purely leptonic decay]] $H \to e^+ e^-$ of [[hadrons]]) is dominated by the [[light meson|light]] [[vector mesons]], in that the [[scattering cross section]] $\sigma(e^+ e^- \to H)$ is peaked at those [[energies]] corresponding to the [[rest masses]] of the vector mesons:

\begin{imagefromfile}
  "file_name": "VectorMesonDominanceInDileptonCrossSectionI.jpg",
  "width": 420,
  "caption": "[Piller-Weise 90, Fig. 1](#PillerWeise90)",
  "float": "right",
  "margin": {
    "top": 0,
    "right": 10,
    "bottom": 10,
    "left": 0,
    "unit": "px"
  } 
\end{imagefromfile}


The first graphics shows the measured cross section (in [[physical unit|units]] of that of the decay $e^+ e^- \to \mu^+ \mu_-$ of [[electron]] [[dileptons]] into [[muon]] [[dileptons]]): The [[light vector mesons]] [[rho-meson|ρ]]$^0$, [[omega-meson|ω]] and [[phi-meson|ϕ]] correspond to the the spikes below 1 [[GeV]], the further spikes correspond to [[heavy vector mesons]], with [[charmonium]] $J/\psi$ around 4 [[GeV]].

\begin{imagefromfile}
  "file_name": "VectorMesonDominanceInDileptonCrossSectionII.jpg",
  "width": 420,
  "caption": "[Piller-Weise 90, Fig. 2](#PillerWeise90)",  
  "float": "left",
  "margin": {
    "top": 0,
    "right": 10,
    "bottom": 10,
    "left": 0,
    "unit": "px"
  } 
\end{imagefromfile}


The second graphics shows the same data, now zoomed into the region of the [[light vector mesons]]. One sees clearly that in this region the [[graph of a function|graph]] of the [[scattering cross section]] is completely dominated first of all by the broad [[rho-meson|ρ]]$^0$ peak at a [[mass]] of $\sim 770$ [[MeV]] (see also [Murphy-Yount 71, Fig. 4](#MurphyYount71)), accompanied just by two sharp spikes, corresponding to the [[omega-meson|ω]] at $\sim 783$ [[MeV]] and the [[phi-meson|ϕ]] at $\sim 1020$ [[MeV]] (see also [Schildknecht 72, Table 1](#Schildknecht72)).



### Theory

In the [[effective field theory]] of [[quantum hadrodynamics]], _vector meson dominance_ refers to a proposal for how to formulate the [[theory (physics)|theory]] guided by the above [[phenomenology]]: 

Here the dominance is encoded by the _field-current identity_  ([Gell-Mann & Zachariasen 61](#GellMannZachariasen61), [Kroll, Lee & Zumino 76, (1.3)](#KrollLeeZumino76), [Sakurai 69, p. 54 onwards](#Sakurai69), review in [Piller-Weise 90, (4)](#PillerWeise90)):

$$
  J^{hadr}_\mu
  \;\sim\;
  V_\mu 
  \,,
$$ 

essentially identifying the electromagnetic [[hadron current]] with the joint neutral [[light meson|light]] [[vector meson]] [[field (physics)|field]].

This implies in particular that all [[coupling constants]] of [[interactions]] with an [[omega-meson]]/neutral [[rho-meson]] are proportional, by the same factor, to the corresponding electromagnetic coupling (reviewed in [Schildknecht 05, p. 3](#Schildknecht05)). 

In terms of a [[Lagrangian density]], this is encoded by meson/photon _mixed terms_ of the following form ([Kroll, Lee & Zumino 76, (2.7)](#KrollLeeZumino76),[Sakurai 69, p. 67](#Sakurai69)):

\[
  \label{VMD1Lagrangian}
  \mathbf{L}_{VMD1}
  \;\sim\;
  d V \wedge \star_4 d A
  \;+\;
  V \wedge \star_4 J^{hadr}
\]

obtained from the Lagrangian density $\mathbf{L}_{EM} \;\sim\; d A \wedge \star_{4} d A + A \wedge \star_4 J_{hadr}$ of [[Maxwell theory]] by exchanging a [[photon]] field variable $A$ with a [[vector meson]] [[field (physics)|field]] $V$ (reviewed in [OCPTW 95, p. 10](#OCPTW95), [Schildknecht 05, p. 4](#Schildknecht05)).

There is also an alternative, supposedly equivalent, Lagrangian formulation, less elegant but now in more widespread use. To distinguish the two one speaks of "VMD1" for the formulation (eq:VMD1Lagrangian) and of "VMD2" for the alternative formulation (reviewed in [OCPTW 95. (26)](#OCPTW95), [Schildknecht 05, (8)](#Schildknecht05)).


## Properties

### Derivation from holography

From [OCPTW 95](#OCPTW95):

> No direct translation between the [[standard model of particle physics|Standard Model]] and [[vector meson dominance|VMD]] has yet been made.

\linebreak

From [Rho et al. 16](AdS-QCD#RhoEtAl16):

> One can make $[$[[chiral perturbation theory]]$]$ consistent with [[QCD]] by suitably matching the [[correlators]] of the [[effective field theory|effective theory]] to those of [[QCD]] at a [[scale]] near $\Lambda$. Clearly this procedure is not limited to only one set of [[vector mesons]]; in fact, one can readily generalize it to an infinite number of hidden [[gauge fields]] in an [[effective field theory|effective]] [[Lagrangian density|Lagrangian]]. In so doing, it turns out that a fifth dimension is "deconstructed" in a (4+1)-dimensional (or 5D) [[Yang-Mills theory|Yang–Mills]] type form. We will see in Part III that such a structure arises, [[top-down model building|top-down]], in [[string theory]].

> $[...]$

> $[$this [[holographic QCD]]$]$ model comes out to describe — unexpectedly well — low-energy properties of both [[mesons]] and [[baryons]], in particular those properties reliably described in quenched [[lattice QCD]] simulations.

> $[...]$

> One of the most noticeable results of this [[AdS/QCD|holographic model]] is the first derivation of vector dominance (VD) that holds both for [[mesons]] and for [[baryons]]. It has been
somewhat of an oddity and a puzzle that [[Jun John Sakurai|Sakurai's]] [[vector meson dominance|vector dominance]] — with the lowest [[vector mesons]] [[rho meson|ρ]] and [[omega meson|ω]] — which held very well for [[pion|pionic]] [[form factors]] at low momentum transfers famously failed for [[nucleon]] [[form factors]]. In this [[AdS/QCD|holographic model]], the [[vector meson dominance|VD]] comes out automatically for both the [[pion]] and the [[nucleon]] provided that the infinite $[$[[Kaluza-Klein mechanism|KK-]]$]$tower is included. While the [[vector meson dominance|VD]] for the [[pion]] with the infinite tower is not surprising given the successful Sakurai VD, that the [[vector meson dominance|VD]] holds also for the [[nucleons]] is highly nontrivial. $[...]$ It turns out to be a consequence of a [[AdS/QCD|holographic]] [[Cheshire cat principle|Cheshire Cat phenomenon]]


## Related concepts

* [[vector meson]]

* [[form factor]]

* [[hadron current]]

[[!include effective field theories of nuclear physics -- contents]]



## References

### General

The original articles:

* {#GellMannZachariasen61} [[Murray Gell-Mann]], Fredrik Zachariasen, _Form Factors and Vector Mesons_, Phys. Rev. 124, 953 (1961) ([doi:10.1103/PhysRev.124.953](https://doi.org/10.1103/PhysRev.124.953))

* {#KrollLeeZumino76} Norman M. Kroll, T. D. Lee, [[Bruno Zumino]], _Neutral Vector Mesons and the Hadronic Electromagnetic Current_, Phys. Rev. 157, 1376 (1967) ([arXiv:10.1103/PhysRev.157.1376](https://doi.org/10.1103/PhysRev.157.1376))

* {#Sakurai69} [[Jun John Sakurai]], Chapter III of: _Currents and Mesons_, Chicago Lectures in Physics, based on notes by George Barry, University of Chicago Press (1969) ([ISBN: 9780226733838](https://www.press.uchicago.edu/ucp/books/book/chicago/C/bo3622598.html))


Review:

* {#MurphyYount71} Fred V. Murphy, David E. Yount, _Photons as hadrons_, Sci.Am. 225N1 (1971) 1, 94-104 ([spire:41546](https://inspirehep.net/literature/41546), [doi:10.1038/scientificamerican0771-94](https://doi.org/10.1038/scientificamerican0771-94))

* {#Schildknecht72} [[Dieter Schildknecht]], _Vector meson dominance, photo- and electroproduction from nucleons_,  in: _Photon-Hadron Interactions II_ Springer Tracts in Modern Physics, vol 63. Springer 1972 ([doi:10.1007/BFb0041507](https://doi.org/10.1007/BFb0041507))


* {#PillerWeise90} G. Piller, [[Wolfram Weise]], _Vector meson dominance: Selected topics_ 1990 ([spire310958](https://inspirehep.net/literature/310958), [[PillerWeiseVMD.pdf:file]])

* {#OCPTW95} H. B. O'Connell, B. C. Pearce, A. W. Thomas, A. G. Williams, _Rho-omega mixing, vector meson dominance and the pion form-factor_, Prog. Part. Nucl. Phys. 39:201-252, 1997 ([arXiv:hep-ph/9501251](https://arxiv.org/abs/hep-ph/9501251))

* {#Schildknecht05} [[Dieter Schildknecht]], _Vector Meson Dominance_, Acta Phys. Polon. B37:595-608, 2006 ([arXiv:hep-ph/0511090](https://arxiv.org/abs/hep-ph/0511090))


See also

* Wikipedia, _[Vector meson dominance](https://en.wikipedia.org/wiki/Vector_meson_dominance)_

More:

* H. B. O'Connell, A. G. Williams, M. Bracco, G. Krein, _Vector Meson Mixing and Charge Symmetry Violation_, Phys. Lett. B370:12-16, 1996 ([arXiv:hep-ph/9510425](https://arxiv.org/abs/hep-ph/9510425))

* A. G. Williams, _New results in vector meson dominance and rho meson physics_, Proceedings of the APCTP Workshop on Astro-Hadron Physics, "Properties of Hadrons in Matter", Seoul, 25-31 October, 1997 ([arXiv:hep-ph/9712405](https://arxiv.org/abs/hep-ph/9712405))

* {#BDDL09a}  M. Benayoun, P. David, L. DelBuono, O. Leitner, _A Global Treatment Of VMD Physics Up To The $\phi$: I. $e^+ e^-$ Annihilations, Anomalies And Vector Meson Partial Widths_, Eur. Phys. J. C65:211-245, 2010 ([arXiv:0907.4047](https://arxiv.org/abs/0907.4047))

* {#BDDL09a} M. Benayoun, P. David, L. DelBuono, O. Leitner, _A Global Treatment Of VMD Physics Up To The $\phi$: II. $\tau$ Decay and Hadronic Contributions To $g-2$_, Eur. Phys. J. C68:355-379, 2010 ([arXiv:0907.5603](https://arxiv.org/abs/0907.5603))

* Avner Karasik, _Vector dominance, one flavored baryons, and QCD domain walls from the "hidden" Wess-Zumino term_ ([arXiv:2010.10544](https://arxiv.org/abs/2010.10544))




### Via holographic QCD
 {#ReferencesViaHolographicQCD}

Derivation of vector meson dominance via [[holographic QCD]]:

* D.T. Son, M.A. Stephanov, _QCD and dimensional deconstruction_, Phys. Rev. D69 (2004) 065020 ([arXiv:hep-ph/0304182](https://arxiv.org/abs/hep-ph/0304182))

  (from the point of view of [[hidden local symmetry]])

* Sungho Hong, Sukjin Yoon, [[Matthew Strassler]], _On the Couplings of Vector Mesons in AdS/QCD_, JHEP 0604 (2006) 003 ([arXiv:hep-th/0409118](https://arxiv.org/abs/hep-th/0409118))

* Sungho Hong, Sukjin Yoon, [[Matthew Strassler]], _On the Couplings of the Rho Meson in AdS/QCD_ ([cds:816440](https://cds.cern.ch/record/816440), [arXiv:hep-ph/0501197](https://arxiv.org/abs/hep-ph/0501197))

* Leandro Da Rold, Alex Pomarol, _Chiral symmetry breaking from five dimensional spaces_, Nucl. Phys. B721:79-97, 2005 ([arXiv:hep-ph/0501218](https://arxiv.org/abs/hep-ph/0501218))

and specifically in the [[Witten-Sakai-Sugimoto model]]:

* {#SakaiSugimoto05} [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], p. 18 and Section 5 of: _More on a holographic dual of QCD_, Progr. Theor. Phys. 114: 1083-1118, 2005 ([arXiv:hep-th/0507073](https://arxiv.org/abs/hep-th/0507073))


[[!redirects current-field identity]]
[[!redirects current-field identities]]

[[!redirects field-current identity]]
[[!redirects field-current identities]]

[[!redirects VMD]]
[[!redirects VMD1]]
[[!redirects VMD2]]



