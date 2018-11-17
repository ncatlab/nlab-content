+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _mass gap problem_ is an open conceptual problem in the [[quantization of Yang-Mills theory]], closely related to what in the [[phenomenology]] of [[quantum chromodynamics]] is called the _[[confinement]]_ of [[quarks]].

The [[Lagrangian]] for [[Yang-Mills theory]] coupled to [[fermion fields]] (such as for [[QCD]]) makes manifest the existence of [[mass]]-less [[quarks]] and [[gluons]]. Indeed at very higher [[temperature]] [[QCD]] is thought to exhibit a [[quark-gluon plasma]] well described by these degrees of freedoms.

But at comparatively smaller [[temperature]] it is observed in [[experiment]] as well as in [[lattice QCD]] computer experiment that QCD exhibits _[[confinement]]_, meaning that the low energy states of the theory are not free massless quarks and gluons anymore, but that these form [[bound states]] in the form of [[hadrons]] (including, notably, [[protons]] and [[neutrons]], and hence all the ordinary [[baryon|baryonic]] [[matter]] of the [[observable universe]]). 

The existence of massive [[hadron]]-[[bound states]] in low-energy [[QCD]] is thus well-established [[phenomenology|phenomenologically]], but it is as of yet lacking a conceptual theoretical explanation.

The _mass gap problem_ is the problem in [[mathematical physics]] to demonstrate theoretically (i.e. not just by [[lattice QCD|computer simulation]]) the existence of this mass gap/[[confinement]]-phenomenon in [[QCD]] and in [[Yang-Mills theory]] coupled to [[fermion fields]] in general.

This issue is well and widely known in the [[particle physics]]-community, see for instance [Kutschke 96, Section 3.1](#Kutschke96), [INFN 15](#INFN15). It gained more attention among the [[mathematics]]/[[mathematical physics]]-commutity when the [Clay Mathematics Institute](http://www.claymath.org/) declared the problem to be one in a list of "[Millenium Problems](http://www.claymath.org/millennium-problems)", see [Jaffe-Witten](#JaffeWitten), [Douglas 04](#Douglas04).



## Related pages

* [[confinement]]


## References

### Mathematics

A survey and problem description in [[mathematics]]/[[mathematical physics]] is in

* [Clay Mathematics Institute](http://www.claymath.org/), _[Yang-Mills and Mass Gap](http://www.claymath.org/millennium-problems/yang%E2%80%93mills-and-mass-gap)_

* {#JaffeWitten} [[Arthur Jaffe]], [[Edward Witten]], _Quantum Yang-Mills theory_ ([pdf](http://www.claymath.org/sites/default/files/yangmills.pdf))

and a report on the progress (essentially none) is in 

* {#Douglas04} [[Michael Douglas]], _Report on the Status of the Yang-Mills Millenium Prize Problem_, 2004 ([pdf](http://www.claymath.org/sites/default/files/ym2.pdf))

Further comments are in

* [[Ludvig Faddeev]], _Mass in Quantum Yang-Mills Theory_, [arXiv:0911.1013](https://arxiv.org/abs/0911.1013).

Notes reviewing more technical details of the problem are in 

* Jay Yablon, _The Origins of QCD Confinement in Yang-Mills Gauge Theory_, January 2008 ([pdf](http://jayryablon.files.wordpress.com/2008/01/qcd-confinement-handout-10.pdf))

See also

* Wikipedia, _[Mass gap](https://en.wikipedia.org/wiki/Mass_gap)_.

* Wikipedia, _[Yang-Mills existence and the mass gap](https://en.wikipedia.org/wiki/Yang%E2%80%93Mills_existence_and_mass_gap)_

### Phenomenology
 {#Phenomenology}

In the application of [[QCD]] to [[particle physics]] [[phenomenology]], the mass gap problem is incarnated in the open problem of demonstrating [[confinement]] of [[quarks]] at low energies to colour-neutral [[bound states]], hence to [[hadrons]]/[[baryons]] (hence the existence of ordinary [[matter]]!).  There does exist some qualitative understanding as well as computer simulations in [[lattice QCD]], but there remain fundamental issues with deriving basic properties of [[hadrons]] such as their [[mass]] (e.g. [Kutschke 96, Section 3.1](#Kutschke96)) and [[spin]] (the "[[proton spin crisis]]").

This is widely and well known, but particle physics does not quite share the mathematician's culture of succinctly highlighting open problems. Here are some sources that make this explicit:

* {#Kutschke96} Robert Kutschke, section 3.1 _Heavy flavour spectroscopy_, in D. Bugg (ed.), _Hadron Spectroscopy and the Confinement Problem_, Proceedings of a NATO Advanced Study Institute, Plenum Press 1996  ([doi:10.1007/978-1-4613-0375-6](https://www.springer.com/cn/book/9780306453038))

> While it is generally believed that QCD is the correct fundamental theory of the strong interactions there are, as yet, no practical means to produce full QCD calculations of hadron masses and their decay widths.

* J J Cobos-Martínez, _Non-perturbative QCD and hadron physics_ 2016  J. Phys.: Conf. Ser. 761 012036 ([doi:10.1088/1742-6596/761/1/012036](http://iopscience.iop.org/article/10.1088/1742-6596/761/1/012036))

> $[\cdots]$ the QCD Lagrangian does not by itself explain the data on strongly interacting matter, and it is not clear how the observed bound states, the hadrons, and their properties arise from QCD. Neither confinement  nor dynamical chiral symmetry breaking (DCSB) is apparent in QCD’s lagrangian, yet they play a dominant role in determining the observable characteristics of QCD. The physics of strongly interacting matter is governed by emergent phenomena such as these, which can only be elucidated through the use of non-perturbative methods in QCD [4, 5, 6, 7]

* {#INFN15} [Istituto Nazionale di Fisica Nucleare](https://web.infn.it/csn1/index.php/en/), _What Next: White Paper of the INFN-CSN1_ _Proposal for a long term strategy for accelerator based experiments_, Frascati Phys.Ser. 60 (2015) 1-302 (2015-05-29) ([spire:1374543](http://inspirehep.net/record/1374543/), [pdf](http://www.lnf.infn.it/sis/frascatiseries/Volume60/Volume60.pdf) ) chapter 7: _Hadron Physics and non-perturbative QCD
_  ([pdf](http://www.infn.it/csn1/White_paper_documents/NPQCD.pdf))

> Experimentally, there is a large number of facts that lack a detailed qualitative and quantitative explanation. The most spectacular manifestation of our lack of theoretical understanding of QCD is the failure to observe the elementary degrees of freedom, quarks and gluons, as free asymptotic states (color con- finement) and the occurrence, instead, of families of massive mesons and baryons (hadrons) that form approximately linear Regge trajectories in the mass squared. The internal, partonic structure of hadrons, and nucleons in particular, is still largely mysterious. Since protons and neutrons form almost all the visible matter of the Universe, it is of basic importance to explore their static and dynamical properties in terms of quarks and gluons interacting according to QCD dynamics. 


Of course various partial approaches exist, notably computer-[[experiment]] in [[lattice QCD]]. (Such computer-checks of the mass-gap problem are analogous to computer checks of the [[Riemann hypothesis]], see [there](Riemann+hypothesis#ReferencesComputerChecks))
High-accuracy computation of [[hadron]]-[[masses]] in [[lattice QCD]]-simulations are reported here:

* S. Durr, Z. Fodor, J. Frison, C. Hoelbling, R. Hoffmann, S.D. Katz, S. Krieg, T. Kurth, L. Lellouch, T. Lippert, K.K. Szabo, G. Vulvert,

  _Ab-initio Determination of Light Hadron Masses_,

  Science 322:1224-1227,2008 ([arXiv:0906.3599](https://arxiv.org/abs/0906.3599))


* Zoltan Fodor, Christian Hoelbling, section V of _Light Hadron Masses from Lattice QCD_, Rev. Mod. Phys. 84, 449, ([arXiv:1203.4789](https://arxiv.org/abs/1203.4789))

* S. Aoki et. al. _Review of lattice results concerning low-energy particle physics_ ([arXiv:1607.00299](https://arxiv.org/abs/1607.00299))

(...)

[[!redirects mass gap problem]]