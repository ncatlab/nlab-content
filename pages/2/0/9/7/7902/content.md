
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

A _Wilson loop_ or _Wilson line_ is an [[observable]] in (both classical and quantum) [[gauge theory]] obtained from the [[holonomy]] of the [[gauge field|gauge]] [[connection on a bundle|connection]]. 

Hence if the gauge connection is given by a globally defined 1-form $A$, then the __Wilson loop__ along a closed [[loop]] $C$ is the trace of the [[path-ordered exponential]]
$$
W_C = Tr(\mathcal{P}exp(i\oint_C A_\mu d x^\mu))
$$
where $\mathcal{P}$ is the "path-ordering operator" and $A_\mu$ are the components of the connection. 

## Properties

### Relation to 1d Chern-Simons theory

For $G$ a suitable [[Lie group]] (compact, semi-simple and simply connected) the Wilson loops of $G$-[[principal connections]] are equivalently the [[partition functions]] of a [[1-dimensional Chern-Simons theory]].

This appears famously in the formulation of [[Chern-Simons theory]] [with Wilson lines](Chern-Simons+theory#WithWilsonLineObservables). More detailes are at _[[orbit method]]_.

### Relation to defects

Wilson loop insertions may be thought of or at least related to _defects_ in the sense of  _[[QFT with defects]]_.

### Duality with 't Hooft operators under S-duality and geometric Langlands

[[S-duality]] of 4d [[super Yang-Mills theory]] may exchange Wilson loop operators with [['t Hooft operators]], in an incarnation of the [[geometric Langlands correspondence]] ([Kapustin-Witten 06](#KapustinWitten06))

[[!include geometric Langlands QFT -- table]]

## Examples

### In Chern-Simons theory

In $SU(2)$-[[Chern-Simons theory]] the Wilson line observables compute the [[Jones polynomial]] of the given curve. See there for more details.


## Related entries

* [['t Hooft operator]]

* [[Wilson surface]]

## References

### General

* [[Kenneth Wilson]], _Confinement of quarks_, Physical Review __D 10__ (8): 2445. [doi](http://dx.doi.org/10.1103/PhysRevD.10.2445) (1974)

* Yuri Makeenko, _Methods of contemporary gauge theory_, Cambridge Monographs on Math. Physics, [gBooks](http://books.google.com/books?id=9W-W2w75ulAC)

* Wikipedia [Wilson loop](http://en.wikipedia.org/wiki/Wilson_loop)

* R. Giles, _Reconstruction of gauge potentials from Wilson loops_, Physical Review __D 24__ (8): 2160, [doi](http://dx.doi.org/10.1103/PhysRevD.24.2160)

* A. Andrasi, J. C. Taylor, _Renormalization of Wilson operators in Minkowski space_, Nucl. Phys. B516 (1998) 417, [hep-th/9601122](http://arxiv.org/abs/hep-th/9601122)

* Amit Sever, Pedro Vieira, Luis F. Alday, Juan Maldacena, [[Davide Gaiotto]], _An Operator product expansion for polygonal null Wilson loops_, [arxiv.org/abs/1006.2788](http://arxiv.org/abs/1006.2788)

### In Chern-Simons theory

Relation between [[Dehn surgery]] and [[Wilson loop observables]] in [[Chern-Simons theory]]:

* E. Guadagnini, _Surgery rules in quantum Chern-Simons field theory_, Nuclear Physics B
Volume 375, Issue 2, 18 May 1992, Pages 381-398 (<a href="https://doi.org/10.1016/0550-3213(92)90037-C">doi:10.1016/0550-3213(92)90037-C</a>)

* Boguslaw Broda, _Chern-Simons theory on an arbitrary manifold via surgery_ ([arXiv:hep-th/9305051](https://arxiv.org/abs/hep-th/9305051))


The [[Poisson bracket]] of Wilson line observables in [[3d Chern-Simons theory]] was obtained in 

* W. Goldman, _Invariant functions on Lie groups and Hamiltonian flow of surface
group representations_, Inventiones Math., 85 (1986), 263&#8211;302.

For more see 

* {#GelcaUribe10b} [[Razvan Gelca]], [[Alejandro Uribe]], section 4 of _Quantum mechanics and non-abelian theta functions for the gauge group $SU(2)$_ ([arXiv:1007.2010](http://arxiv.org/abs/1007.2010))


Discussion of [[BTZ black hole|BTZ]] [[black hole entropy]] and more generally of [[holographic entanglement entropy]] in [[3d quantum gravity]]/[[AdS3/CFT2]] via [[Wilson line observables]] in [[Chern-Simons theory]]:

* Martin Ammon, Alejandra Castro, Nabil Iqbal, _Wilson Lines and Entanglement Entropy in Higher Spin Gravity_, JHEP 10 (2013) 110 ([arXiv:1306.4338](https://arxiv.org/abs/1306.4338))

* [[Jan de Boer]], Juan I. Jottar, _Entanglement Entropy and Higher Spin Holography in $AdS_3$_, 	JHEP 1404:089, 2014 ([arXiv:1306.4347](https://arxiv.org/abs/1306.4347))


* Alejandra Castro, Stephane Detournay, Nabil Iqbal, [[Eric Perlmutter]], _Holographic entanglement entropy and gravitational anomalies_, JHEP 07 (2014) 114 ([arXiv:1405.2792](https://arxiv.org/abs/1405.2792))


* Mert Besken, Ashwin Hegde, Eliot Hijano, [[Per Kraus]], _Holographic conformal blocks from interacting Wilson lines_, JHEP 08 (2016) 099 ([arXiv:1603.07317](https://arxiv.org/abs/1603.07317))


* Andreas Blommaert, Thomas G. Mertens, Henri Verschelde, _The Schwarzian Theory - A Wilson Line Perspective_, JHEP 1812 (2018) 022 ([arXiv:1806.07765](https://arxiv.org/abs/1806.07765))

* [[Eric D'Hoker]], [[Per Kraus]], _Gravitational Wilson lines in $AdS_3$_ ([arXiv:1912.02750](https://arxiv.org/abs/1912.02750))



* Ashwin Dushyantha Hegde, _Role of Wilson Lines in 3D Quantum Gravity_, 2019 ([spire:1763572](http://inspirehep.net/record/1763572))

* Xing Huang, Chen-Te Ma, Hongfei Shu, _Quantum Correction of the Wilson Line and Entanglement Entropy in the $AdS_3$ Chern-Simons Gravity Theory_ ([arXiv:1911.03841](https://arxiv.org/abs/1911.03841))

and similarly for 3d flat-space holography:

* Arjun Bagchi, Rudranil Basu, Daniel Grumiller, Max Riegler, _Entanglement entropy in Galilean conformal field theories and flat holography_, Phys. Rev. Lett. 114, 111602 (2015) ([arXiv 1410.4089](https://arxiv.org/abs/1410.4089))

* Rudranil Basu, Max Riegler, _Wilson Lines and Holographic Entanglement Entropy in Galilean Conformal Field Theories_, Phys. Rev. D 93, 045003 (2016) ([arXiv:1511.08662](https://arxiv.org/abs/1511.08662))



* Wout Merbis, Max Riegler, _Geometric actions and flat space holography_ ([arXiv:1912.08207](https://arxiv.org/abs/1912.08207))


### In QFT with defects

Relation to [[QFT with defects]] is discussed in

slide 17 of 

* [[Constantin Bachas]], _Conformal defects in/and String theory_ ([pdf](http://www.ggi.fi.infn.it/talks/talk106.pdf))

slide 5 of 

* [[Constantin Bachas]], _Conformal defects in gauged WZW models_ ([pdf](http://hep.physics.uoc.gr/conf09/TALKS/Bachas.pdf))



### As partition functions of 1d Chern-Simons theory

Expression of Wilson loops as [[partition functions]] of [[1-dimensional Chern-Simons theories]]  by the [[orbit method]] (as used notably in [[Chern-Simons theory]]) is in section 4 of 

* [[Chris Beasley]], _Localization for Wilson Loops in Chern-Simons Theory_, in J. Andersen, H. Boden, A. Hahn, and B. Himpel (eds.) _Chern-Simons Gauge Theory: 20 Years After_, AMS/IP Studies in Adv. Math., Vol. 50, AMS, Providence, RI, 2011. ([arXiv:0911.2687](http://arxiv.org/abs/0911.2687))

referring to 

* S. Elitzur, [[Greg Moore]], A. Schwimmer, and [[Nathan Seiberg]], _Remarks on the Canonical Quantization of the Chern-Simons-Witten Theory_, Nucl. Phys. B 326 (1989) 108&#8211;134.

in the context of [[Chern-Simons theory]] and in more general gauge theory to

* A. P. Balachandran, S. Borchardt, and A. Stern, _Lagrangian And Hamiltonian Descriptions of Yang-Mills Particles_, Phys. Rev. D 17 (1978) 3247&#8211;3256

### In S-duality and relation to t Hoofts operators

* {#KapustinWitten06} [[Anton Kapustin]], [[Edward Witten]], _Electric-Magnetic Duality And The Geometric Langlands Program_, Communications in Number Theory and Physics Volume 1 (2007) Number 1 ([arXiv:hep-th/0604151](http://arxiv.org/abs/hep-th/0604151))


[[!redirects Wilson loop]]
[[!redirects Wilson loops]]
[[!redirects Wilson-loop]]
[[!redirects Wilson-loops]]

[[!redirects Wilson line]]
[[!redirects Wilson-line]]
[[!redirects Wilson lines]]
[[!redirects Wilson-lines]]

[[!redirects Wilson operator]]
[[!redirects Wilson operators]]

[[!redirects Wilson loop observable]]
[[!redirects Wilson loop observables]]

[[!redirects Wilson line observable]]
[[!redirects Wilson line observables]]
