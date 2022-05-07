

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

_Lattice gauge theory_ (introduced in [Wegner 71](#Wegner71), [Wilson 74](#Wilson74)) is [[gauge theory]] ([[Yang-Mills theory]], such as [[quantum chromodynamics]]) where [[continuum]] [[spacetime]] is replaced by a [[discrete group|discrete]] [[lattice (in a vector space, etc.)|lattice]], hence a [[lattice model]] for [[gauge field theory]].

Usually this is considered after [[Wick rotation]] from [[Minkowski spacetime]] $\mathbb{R}^{3,1}$ to [[Euclidean field theory]] on a [[lattice (in a vector space, etc.)|lattice]] inside $\mathbb{R}^3 \times S^1$, and typically one further identifies the spatial directions periodically to arrive at [[Euclidean]] [[gauge field theory]] on a [[lattice (in a vector space, etc.)|lattice]] inside the [[4-torus]] $T^4$.

This discretization and further [[KK-compactification|compactification]] has the effect that the would-be [[path integral]] of the theory becomes an ordinary [[finite number|finite]]- (albeit high-)[[dimension|dimensional]] [[integral]], hence well defined and in principle amenable to explicit computation. 

This allows to consider ([[Wick rotation|Wick-rotated]]) [[path integral quantization]] at fixed lattice spacing, this being, in principle, a [[non-perturbative field theory|non-perturbative]] [[quantization]], in contrast to [[perturbative quantum field theory]] in terms of a [[Feynman perturbation series]]. On the other hand, much of the subtlety of the latter now appears in issues of taking the continuum limit where the the lattice spacing is sent to zero. In particular, different choices of discretizing the [[path integral]] over the lattice correspond to the [[renormalization]]-freedom seen in [[perturbative quantum field theory]].

Hence lattice gauge theory lends itself to brute-force simulation of [[quantum field theory]] on electronic computers, and the term is often understood by default in this sense. See [Fodor-Hoelbling 12](#FodorHoelbling12) for a good account.


Since the explicit [[non-perturbative quantum field theory|non-perturbative]] formulation of [[Yang-Mills theories]] such as [[QCD]] is presently wide open (see the references at [[mass gap]] and at _[[quantization of Yang-Mills theory]]_) these numerical simulations provide, besides actual [[experiment]], key insights into the non-perturbative nature of the theory, such as its [[instanton sea]] ([Gruber 13](#Gruber13)) and notably the phenomenonon of [[confinement]]/[[mass gap]] and explicit computation of [[hadron]] [[masses]] ([Durr et al. 09](#Durr09), see [Fodor-Hoelbling 12, section V](#FodorHoelbling12))

Despite the word "theory", lattice gauge theory is more like "computer-simulated [[experiment]]". While it allows to see phenomena of QCD, it usually cannot provide a conceptual explanation, and of course not a mathematical derivation of problems such as [[confinement]]/[[mass gap]]. Lattice gauge theory is to the [[confinement]]/[[mass gap]]-problems as explicit computation of zeros of the [[Riemann zeta-function]] is to the [[Riemann hypothesis]] (see [there](#Riemann+hypothesis#ReferencesComputerChecks))).

## Properties

### Sign problem
 {#SignProblem}

See at *[[sign problem in lattice QCD]]*.


## Related concepts

* [[Symanzik effective field theory]]

* [[lattice model]]

* [[non-perturbative effect]]

* [[lattice renormalization]]

* Discussion of [[QCD instantons]] in LGT includes ([Moore 03, section 7](#Moore03), [Gruber 13](#Gruber13))

* [[QCD cosmology]]

* [[AdS/QCD correspondence]]

* [[Euclidean field theory]]

* [[string bit model]]

## References
 {#References}

### General

The concept was introduced in

* {#Wegner71} [[Franz Wegner]], _Duality in Generalized Ising Models and Phase Transitions without Local Order Parameters_, Journal of Mathematical Physics 12, 2259 (1971) ([doi:10.1063/1.1665530](https://doi.org/10.1063/1.1665530))

* {#Wilson74} [[Kenneth Wilson]],  _Confinement of quarks, Phys. Rev. D10, 2445, 1974 ([doi:10.1103/PhysRevD.10.2445](https://doi.org/10.1103/PhysRevD.10.2445))

Introduction and review:

* S. Gupta, _Introduction to lattice field theory_, March 2011, ([pdf](http://theory.tifr.res.in/~sgupta/talks/11aslft.pdf))

* G. M&#252;nster, M. Walzl, _Lattice Gauge Theory - A short Primer_ ([arXiv:hep-lat/0012005](http://arxiv.org/abs/hep-lat/0012005))

* [[Kenneth Wilson]], _The Origins of Lattice Gauge Theory_, ([arXiv:hep-lat/0412043](http://arxiv.org/abs/hep-lat/0412043))

* {#Moore03} Guy Moore, _Informal lectures on lattice gauge theory_, 2003 ([pdf](https://theorie.ikp.physik.tu-darmstadt.de/qcd/moore/latt_lectures.pdf))

* {#PeetersZamaklar09} [[Kasper Peeters]], [[Marija Zamaklar]], section 5 of _Euclidean Field Theory_, Lecture notes 2009-2011 ([web](http://maths.dur.ac.uk/users/kasper.peeters/eft.html), [pdf](http://maths.dur.ac.uk/users/kasper.peeters/pdf/eft.pdf))

* {#Brambilla14} Brambilla et al., Section 3.3.1 of: _[[QCD and strongly coupled gauge theories - challenges and perspectives]]_, Eur Phys J C Part Fields. 2014; 74(10): 2981  ([arXiv:1404.3723](https://arxiv.org/abs/1404.3723), [doi:10.1140/epjc/s10052-014-2981-5](https://link.springer.com/article/10.1140%2Fepjc%2Fs10052-014-2981-5))

* Mattia Dalla Brida, _Past, present, and future of precision determinations of the QCD parameters from lattice QCD_ ([arXiv:2012.01232](https://arxiv.org/abs/2012.01232))

Rigorous discussion in view of the [[mass gap problem]]:

* {#Chatterjee20} [[Sourav Chatterjee]], _A probabilistic mechanism for quark confinement_, Comm. Math. Phys. 2020 ([arXiv:2006.16229](https://arxiv.org/abs/2006.16229))



Visualization:

* James Biddle et al. _Publicising Lattice Field Theory through Visualisation_ ([arXiv:1903.08308](https://arxiv.org/abs/1903.08308))




Relation to [[string theory]]/[[M-theory]] (such as via [[BFSS matrix model]]) in view [[AdS-CFT duality]]:

* {#Hanada16} [[Masanori Hanada]], _What lattice theorists can do for superstring/M-theory_,  International Journal of Modern Physics A Vol. 31, No. 22, 1643006 (2016)  ([arXiv:1604.05421](https://arxiv.org/abs/1604.05421))


See also 

* Wikipedia, _[Lattice gauge theory](https://en.wikipedia.org/wiki/Lattice_gauge_theory)_

* Wikipedia, _[Lattice QCD](https://en.wikipedia.org/wiki/Lattice_QCD)_

### Computer simulations
 {#ReferencesMontoCarloSimulations}

Introduction:

* [[Masanori Hanada]], _Markov Chain Monte Carlo for Dummies_ ([arXiv:1808.08490](https://arxiv.org/abs/1808.08490))

* Anosh Joseph, _Markov Chain Monte Carlo Methods in Quantum Field Theories: A Modern Primer_, Springer Briefs in Physics 2020 ([arXiv:1912.10997](https://arxiv.org/abs/1912.10997))

Account of computer simulation results in lattice [[QCD]]:

* {#FodorHoelbling12} Zoltan Fodor, Christian Hoelbling, sections II-IV of _Light Hadron Masses from Lattice QCD_, Rev. Mod. Phys. 84, 449 (2012) ([arXiv:1203.4789](https://arxiv.org/abs/1203.4789))

See also

* [[Michael Creutz]], _Monte Carlo study of quantized SU(2) gauge theory_ Phys. Rev. D21 (1980) 2308-2315 ([journal](http://prd.aps.org/abstract/PRD/v21/i8/p2308_1), [pdf](http://thy.phy.bnl.gov/~creutz/mypubs/pub037.pdf))


* [[Michael Creutz]],  _Monte Carlo study of renormalization in lattice gauge theory_ Phys.Rev. D23 (1981) 1815  ([pdf](http://thy.phy.bnl.gov/~creutz/mypubs/pub045.pdf))


* [[Michael Creutz]], Laurence Jacobs, Claudio Rebbi, _Monte Carlo computations in lattice gauge theories_, Volume 95, Issue 4, April 1983, Pages 201&#8211;282 ([pdf](http://thy.phy.bnl.gov/~creutz/mypubs/pub068.pdf))

Specifically computation of [[hadron]]-[[masses]] (see [[mass gap problem]]) in lattice QCD is reported here:

* {#Durr09} S. Durr, Z. Fodor, J. Frison, C. Hoelbling, R. Hoffmann, S.D. Katz, S. Krieg, T. Kurth, L. Lellouch, T. Lippert, K.K. Szabo, G. Vulvert,

  _Ab-initio Determination of Light Hadron Masses_,

  Science 322:1224-1227, 2008 ([arXiv:0906.3599](https://arxiv.org/abs/0906.3599))

reviewed in 

* [Fodor-Hoelbling 12, section V of ](#FodorHoelbling12)


Discussion specifically of numerical computation of [[form factors]]:

* B.B. Brandt, S. Capitani, M. Della Morte, D. Djukanovic, J. Gegelia, G. von Hippel, A. Juttner, B. Knippschild, H.B. Meyer, H. Wittig, _Form factors in lattice QCD_, Eur. Phys. J. ST 198:79-94, 2011 ([arXiv:1106.1554](https://arxiv.org/abs/1106.1554))

Relation to [[tensor networks]]:

* [[Luca Tagliacozzo]], Alessio Celi, Maciej Lewenstein, _Tensor Networks for Lattice Gauge Theories with continuous groups_, Phys. Rev. X 4, 041024 (2014) ([arXiv:1405.4811](https://arxiv.org/abs/1405.4811))

* {#BBCCCDFJLMMRRTVV19} M.C. Bañuls, R. Blatt, J. Catani, A. Celi, J.I. Cirac, M. Dalmonte, L. Fallani, K. Jansen, M. Lewenstein, S. Montangero, C.A. Muschik, B. Reznik, E. Rico, [[Luca Tagliacozzo]], K. Van Acoleyen, [[Frank Verstraete]], U.-J. Wiese, M. Wingate, J. Zakrzewski, P. Zoller: 

  _Simulating Lattice Gauge Theories within Quantum Technologies_ 

  ([arXiv:1911.00003](https://arxiv.org/abs/1911.00003))


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

### For super Yang-Mills theories
  {#ForSuperYangMills}

Lattice simulation of [[torus]]-[[KK-compactifications]] of [[10d super Yang-Mills theory]] and numerical test of [[AdS/CFT]]:


#### General

* {#Joseph15} Anosh Joseph, _Review of Lattice Supersymmetry and Gauge-Gravity Duality_ ([arXiv:1509.01440](https://arxiv.org/abs/1509.01440))

* {#Hanada16} [[Masanori Hanada]], _What lattice theorists can do for superstring/M-theory_,  International Journal of Modern Physics AVol. 31, No. 22, 1643006 (2016)  ([arXiv:1604.05421](https://arxiv.org/abs/1604.05421))


#### Compactification to $D = 1$ 
 {#ReferencesBFSS}

The [[BFSS matrix model]]:

* Veselin G. Filev, Denjoe O'Connor, _The BFSS model on the lattice_, JHEP 1605 (2016) 167 ([arXiv:1506.01366](https://arxiv.org/abs/1506.01366))

* [[Masanori Hanada]], Paul Romatschke, _Lattice Simulations of 10d Yang-Mills toroidally compactified to 1d, 2d and 4d_ ([arXiv:1612.06395](https://arxiv.org/abs/1612.06395))

The [[BMN matrix model]]:

* Hrant Gharibyan, [[Masanori Hanada]], Masazumi Honda, Junyu Liu, _Toward simulating Superstring/M-theory on a quantum computer_ ([arXiv:2011.06573](https://arxiv.org/abs/2011.06573))



#### Compactification to $D= 0$  
 {#ReferencesIKKT}
 

The [[IKKT matrix model]] and claims that it predicts spontaneous [[KK-compactification]] of the $D = 10$ [[M-theory|non-perturbative]] [[type IIB string theory]]/[[F-theory]] to $D = 3+1$ macrocopic [[spacetime]] [[dimensions]]:

* {#KimNishimuraTsuchiya12} S.-W. Kim, J. Nishimura, and A. Tsuchiya, _Expanding (3+1)-dimensional universe from a Lorentzian matrix model for superstring theory in (9+1)-dimensions_, Phys. Rev. Lett. 108, 011601 (2012), ([arXiv:1108.1540](https://arxiv.org/abs/1108.1540)).

* S.-W. Kim, J. Nishimura, and A. Tsuchiya, _Late time behaviors of the expanding universe in the IIB matrix model_, JHEP 10, 147 (2012), ([arXiv:1208.0711](https://arxiv.org/abs/1208.0711)).

* Yuta Ito, Jun Nishimura, Asato Tsuchiya, _Large-scale computation of the exponentially expanding universe in a simplified Lorentzian type IIB matrix model_ ([arXiv:1512.01923](https://arxiv.org/abs/1512.01923))

* {#AHINT19} Toshihiro Aoki, Mitsuaki Hirasawa, Yuta Ito, Jun Nishimura, Asato Tsuchiya, _On the structure of the emergent 3d expanding space in the Lorentzian type IIB matrix model_ ([arXiv:1904.05914](https://arxiv.org/abs/1904.05914))


[[!redirects lattice gauge theories]]

[[!redirects lattice gauge field theory]]
[[!redirects lattice gauge field theorues]]

[[!redirects lattice field theory]]
[[!redirects lattice field theories]]


[[!redirects lattice QCD]]

[[!redirects lattice QFT]]


[[!redirects lattice quantum chromodynamics]]
