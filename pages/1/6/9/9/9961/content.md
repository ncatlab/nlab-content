

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Lattice gauge theory is a [[computation|computational]] model for [[gauge theory]] ([[Yang-Mills theory]]).

These are numerical simulation of [[Wick rotation|Wick rotated]] [[non-perturbative quantum field theory|non-perturbative QCD]] obtained by discretizing the [[Euclidean field theory|Euclidean spacetime]] to a _lattice_ [[graph]] of [[vertices]] and [[edges]] between them, regarding the [[gauge field]] as a function on the [[edges]] (assigning to an edge the [[holonomy]]/[[parallel transport]] of the gauge field) and then explicitly evaluating the would-be [[path integral]] of the [[Yang-Mills action]] over these field configurations as an approximate numerical sum. 

Specifically for [[QCD]] this is also called _lattice QCD_, etc.

Hence this yieds numerical values for [[correlation functions]] etc. which are non-perturbative in the [[coupling constant]] but nevertheless approximate, due to finite lattice spacing and numerical error. 

Since the explicit [[non-perturbative quantum field theory|non-perturbative]] formulation of [[Yang-Mills theories]] such as [[QCD]] is presently wide open (see also at _[[quantization of Yang-Mills theory]]_) these numerical simulation provide, besides [[experiment]] (e.g. of in particular of [[quark-gluon plasma]]), a key insight into the non-perturbative nature of the theory, such as its [[instanton sea]] ([Gruber 13](#Gruber13)) and the phenomenona of [[confinement]] and [[mass gap]].

Despite the word "theory", lattice gauge theory is more like "computer-simpulated [[experiment]]". While it allows to see phenomena of QCD, it usually cannot provide a conceptual explanation, and of course not a mathematical derivation.



## Related concepts

* [[non-perturbative effect]]

* [[lattice renormalization]]

* Discussion of [[QCD instantons]] in LGT includes ([Moore 03, section 7](#Moore03), [Gruber 13](#Gruber13))

* [[Euclidean field theory]]

* [[string bit model]]

## References

### General

* S. Gupta, _Introduction to lattice field theory_, March 2011, ([pdf](http://theory.tifr.res.in/~sgupta/talks/11aslft.pdf))

* G. M&#252;nster, M. Walzl, _Lattice Gauge Theory - A short Primer_ ([arXiv:hep-lat/0012005](http://arxiv.org/abs/hep-lat/0012005))

* [[Kenneth Wilson]], _The Origins of Lattice Gauge Theory_, ([arXiv:hep-lat/0412043](http://arxiv.org/abs/hep-lat/0412043))

* {#Moore03} Guy Moore, _Informal lectures on lattice gauge theory_, 2003 ([pdf](https://theorie.ikp.physik.tu-darmstadt.de/qcd/moore/latt_lectures.pdf))

* {#PeetersZamaklar09} [[Kasper Peeters]], [[Marija Zamaklar]], section 5 of _Euclidean Field Theory_, Lecture notes 2009-2011 ([web](http://maths.dur.ac.uk/users/kasper.peeters/eft.html), [pdf](http://maths.dur.ac.uk/users/kasper.peeters/pdf/eft.pdf))


See also 

* Wikipedia, _[Lattice gauge theory](https://en.wikipedia.org/wiki/Lattice_gauge_theory)_

* Wikipedia, _[Lattice QCD](https://en.wikipedia.org/wiki/Lattice_QCD)_

### Computer simulations
 {#ReferencesMontoCarloSimulations}

A good general account of computer simulation of lattice [[QCD]] is in 

* {#FodorHoelbling12} Zoltan Fodor, Christian Hoelbling, sections II-IV of _Light Hadron Masses from Lattice QCD_, Rev. Mod. Phys. 84, 449 (2012) ([arXiv:1203.4789](https://arxiv.org/abs/1203.4789))

See also

* [[Michael Creutz]], _Monte Carlo study of quantized SU(2) gauge theory_ Phys. Rev. D21 (1980) 2308-2315 ([journal](http://prd.aps.org/abstract/PRD/v21/i8/p2308_1), [pdf](http://thy.phy.bnl.gov/~creutz/mypubs/pub037.pdf))


* [[Michael Creutz]],  _Monte Carlo study of renormalization in lattice gauge theory_ Phys.Rev. D23 (1981) 1815  ([pdf](http://thy.phy.bnl.gov/~creutz/mypubs/pub045.pdf))


* [[Michael Creutz]], Laurence Jacobs, Claudio Rebbi, _Monte Carlo computations in lattice gauge theories_, Volume 95, Issue 4, April 1983, Pages 201&#8211;282 ([pdf](http://thy.phy.bnl.gov/~creutz/mypubs/pub068.pdf))

Specifically computation of [[hadron]]-[[masses]] (see [[mass gap problem]]) in lattice QCD is reported here:

* S. Durr, Z. Fodor, J. Frison, C. Hoelbling, R. Hoffmann, S.D. Katz, S. Krieg, T. Kurth, L. Lellouch, T. Lippert, K.K. Szabo, G. Vulvert,

  _Ab-initio Determination of Light Hadron Masses_,

  Science 322:1224-1227,2008 ([arXiv:0906.3599](https://arxiv.org/abs/0906.3599))

reviwed in 

* [Fodor-Hoelbling 12, section V of ](#FodorHoelbling12)


### Renormalization

A proposal for a rigorous formulation of [[renormalization]] in lattice gauge theory is due to 

* [[Tadeusz Balaban]], _Renormalization group approach to lattice gauge field theories: I. Generation of effective actions in a small field approximation and a coupling constant renormalization in four dimensions_, Communications in Mathematical Physics, Volume 109, Issue 2, pp.249-301 ([web](https://link.springer.com/article/10.1007%2FBF01215223))

* ...

reviewed in 


* [[Jonathan Dimock]], _The renormalization group according to Balaban, I. Small fields_, Rev. Math. Phys., 25, 1330010 (2013) ([doi:10.1142/S0129055X13300100](https://doi.org/10.1142/S0129055X13300100))

* ...

### Topological effects and instantons

Discussion of [[instantons]] in lattice QCd

* {#Gruber13} Florian Gruber, _Topology in dynamical Lattice QCD simulations_, 2013 ([web](http://epub.uni-regensburg.de/27631/), [pdf](http://epub.uni-regensburg.de/27631/1/dissertation.pdf))


[[!redirects lattice gauge field theory]]

[[!redirects lattice QCD]]
