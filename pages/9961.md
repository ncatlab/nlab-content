

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

_Lattice gauge theory_ (introduced in [Wilson 74](#Wilson74)) is [[gauge theory]] ([[Yang-Mills theory]], such as [[quantum chromodynamics]]) where [[continuum]] [[spacetime]] is replaced by a [[discrete group|discrete]] [[lattice (in a vector space, etc.)|lattice]].

Usually this is considered after [[Wick rotation]] from [[Minkowski spacetime]] $\mathbb{R}^{3,1}$ to [[Euclidean field theory]] on a [[lattice (in a vector space, etc.)|lattice]] inside $\mathbb{R}^3 \times S^1$, and typically one further identifies the spatial directions periodically to arrive at [[Euclidean]] [[gauge field theory]] on a [[lattice (in a vector space, etc.)|lattice]] inside the [[4-torus]] $T^4$.

This discretization and further [[KK-compactification|compactification]] has the effect that the would-be [[path integral]] of the theory becomes an ordinary [[finite number|finite]]- (albeit high-)[[dimension|dimensional]] [[integral]], hence well defined and in principle amenable to explicit computation. 

This allows to consider ([[Wick rotation|Wick-rotated]]) [[path integral quantization]] at fixed lattice spacing, this being, in principle, a [[non-perturbative field theory|non-perturbative]] [[quantization]], in contrast to [[perturbative quantum field theory]] in terms of a [[Feynman perturbation series]]. On the other hand, much of the subtlety of the latter now appears in issues of taking the continuum limit where the the lattice spacing is sent to zero. In particular, different choices of discretizing the [[path integral]] over the lattice correspond to the [[renormalization]]-freedom seen in [[perturbative quantum field theory]].

Hence lattice gauge theory lends itself to brute-force simulation of [[quantum field theory]] on electronic computers, and the term is often understood by default in this sense. See [Fodor-Hoelbling 12](#FodorHoelbling12) for a good account.


Since the explicit [[non-perturbative quantum field theory|non-perturbative]] formulation of [[Yang-Mills theories]] such as [[QCD]] is presently wide open (see the references at [[mass gap]] and at _[[quantization of Yang-Mills theory]]_) these numerical simulation provide, besides actual [[experiment]], key insight into the non-perturbative nature of the theory, such as its [[instanton sea]] ([Gruber 13](#Gruber13)) and notably the phenomenonon of [[confinement]]/[[mass gap]] and explicit computation of [[hadron]] [[masses]] ([Durr et al. 09](#Durr09), see [Fodor-Hoelbling 12, section V](#FodorHoelbling12))

Despite the word "theory", lattice gauge theory is more like "computer-simpulated [[experiment]]". While it allows to see phenomena of QCD, it usually cannot provide a conceptual explanation, and of course not a mathematical derivation of problems such as [[confinement]]/[[mass gap]]. Lattice gauge theory is to the [[confinement]]/[[mass gap]]-problems as explicit computation of zeros of the [[Riemann zeta-function]] is to the [[Riemann hypothesis]] (see [there](#Riemann+hypothesis#ReferencesComputerChecks))).



## Related concepts

* [[non-perturbative effect]]

* [[lattice renormalization]]

* Discussion of [[QCD instantons]] in LGT includes ([Moore 03, section 7](#Moore03), [Gruber 13](#Gruber13))

* [[Euclidean field theory]]

* [[string bit model]]

## References

The concept was introduced in

* {#Wilson74} [[Kenneth Wilson]],  _Confinement of quarks, Phys. Rev. D10, 2445, 1974 ([doi:10.1103/PhysRevD.10.2445](https://doi.org/10.1103/PhysRevD.10.2445))

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

* {#Durr09} S. Durr, Z. Fodor, J. Frison, C. Hoelbling, R. Hoffmann, S.D. Katz, S. Krieg, T. Kurth, L. Lellouch, T. Lippert, K.K. Szabo, G. Vulvert,

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
