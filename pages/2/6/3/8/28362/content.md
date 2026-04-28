

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Differential cohomology
+-- {: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

\tableofcontents

## Idea

The *dual superconductor model*  ([Mandelstam 1975](#Mandelstam1975), [’t Hooft 1975](#tHooft1975), [1978](#tHooft1978)) is a proposal for how to conceptually understand the mechanism of [[confinement]] in non-abelian [[Yang-Mills theories]] such as [[quantum chromodynamics]] (the *[[Yang-Mills mass gap]]* problem).

The idea is to regard the theory in a "maximal abelian [[gauge fixing|gauge]]", where the [[SU(n)|$SU(n)$]] [[color charge|color]] [[gauge field]] is approximated by small nonabelian fluctuations around a [[Maxwell theory|Maxwell]]-like field with [[gauge group]] the [[maximal torus]] 

$$
  U(1)^{n-1} 
   \;\simeq\; 
  S\big(U(1)^n\big) 
   \;\subset\; 
  SU(n)
 \mathrlap{\,.}
$$ 
In such a [[gauge fixing|gauge]] one expects to see [[magnetic monopoles]] the way they are theoretically possible in [[Maxwell theory]] (cf. *[[Dirac charge quantization]]*), owing to the fact that the [[classifying space]] $B S\big(U(1)^n\big)$ (but not $B SU(n \geq 2)$) has nontrivial second [[homotopy group]], 

\[
  \pi_2\Big(
    B S\big(U(1)^{n}\big)
  \Big)
  \simeq
  \mathbb{Z}^{n-1}
  \,,\;\;\;\;\;\;
  \pi_2\big(B SU(n)\big) \simeq 0
  \,\;\;\;\;
  (n \geq 2)
  \mathrlap{\,.}
\]

The [[condensate|condensation]] of these [[magnetic monopoles]] is then imagined to be an [[electric-magnetic duality|electromagnetic dual]] to the (experimentally well-observed) condensation of [[Cooper pairs]] in [[superconductors]], whence one speaks of a *[[superinsulator]]* phase. 

But in [[superconductors]] it is well-known that the [[Meissner effect]] causes [[magnetic field|magnetic]] [[flux lines]] to (no longer spread out radially but) be bundled into [[flux tubes]] (through [[Abrikosov vortices]]). Hence by appeal to [[electric-magnetic duality]] one may expect that, dually, in such a [[magnetic monopole]] [[condensate]] [[superinsulator]] it is instead the [[color charge|color]]-*electric* flux lines which are bundled into [[flux tubes]]. But such [[color charge|color]]-*electric* [[flux tubes]] between [[quarks]] are exactly what, in turn, is expected (cf. *[[Polyakov gauge-string duality]]*) to conceptually explain the [[confinement]] of [[quarks]] inside [[mesons]] (and more generally inside [[baryons]], hence generally inside [[hadrons]]).


## Comparison to lattice simulation

The model compares favorably with [[lattice QCD]] simulations in suitable parameter ranges (cf. [Greensite 2003 §7.5](#Greensite2003), [CCCP 2017](#CCCP2017)).

### Successes

* **Abelian and Monopole Dominance:** In the maximally Abelian (MA) [[gauge fixing|gauge]], off-diagonal [[gluons]] acquire a large effective [[mass]] (around 1 [[GeV]]), which successfully reduces the infrared region of QCD into an Abelian-like theory ([Suganuma & Sakumichi 2018, p. 2](#SuganumaSakumichi2018)). Lattice simulations demonstrate "perfect Abelian dominance," where the Abelian part of the gauge field alone reproduces the full string tension for static quark-antiquark ($Q\bar{Q}$) systems on large physical-volume lattices ([Suganuma & Sakumichi 2014, p. 1](#SuganumaSakumichi2014); [Suganuma & Sakumichi 2018, p. 1](#SuganumaSakumichi2018)). This perfect Abelian dominance is also successfully verified for three-quark (3Q) systems ([Suganuma & Sakumichi 2018, p. 1](#SuganumaSakumichi2018)). 

* **Isolation of Confinement Dynamics:** The QCD vacuum in these simulations reveals a large clustering of the monopole-current network ([Suganuma & Sakumichi 2016, p. 1](#SuganumaSakumichi2016)). When the system is decomposed, the monopole part alone is found to be responsible for quark confinement, chiral symmetry breaking, and the presence of instantons, whereas the off-diagonal "photon" part contributes zero string tension ([Suganuma & Sakumichi 2014, p. 2](#SuganumaSakumichi2014)).

* **Flux Tube Profiles:** The transverse shape of the longitudinal chromoelectric field midway between static sources can be accurately described by the dual superconductivity picture ([Cea, Cosmai, Cuteri & Papa 2017, p. 1](#CCCP2017)). By fitting the lattice data to dual versions of superconductor vortex models, parameters can be extracted that indicate the $SU(3)$ pure gauge vacuum behaves as a type-I superconductor ([Cea, Cosmai, Cuteri & Papa 2017, p. 5](#CCCP2017)). In this pure gauge theory, the dual London penetration length ($\lambda$) and the mean width of the field profile remain fairly stable as the distance between sources varies ([Cea, Cosmai, Cuteri & Papa 2017, p. 5](#CCCP2017)).

* **Order Parameters:** Using a corrected definition of the order parameter for dual superconductivity, simulations show that the confined phase is superconducting while the deconfined phase behaves as a normal medium ([Di Giacomo 2001, p. 1](#DiGiacomo2001)). Similarly, suitably defined monopole creation operators acquire a non-zero expectation value strictly in the confinement phase ([Greensite 2003, Sec. 7.5](#Greensite2003)).

### Drawbacks and Limitations

* **Casimir Scaling and Representation Dependence:** The dual superconductor model predicts that the string tension should be strictly proportional to the $U(1)$ Abelian electric charge, which contradicts the intermediate-distance Casimir scaling observed in QCD ([Greensite 2003, Sec. 7.6.1](#Greensite2003)). Consequently, quarks in the adjoint representation, which have zero $U(1)$ electric charge, should not experience confinement under the monopole gas model, yet they are known to exhibit a linear confining potential up to the onset of color screening ([Greensite 2003, Sec. 7.6.1](#Greensite2003); [Del Debbio et al. 1997, p. 2](#DelDebbioEtAl1997)).

* **Asymptotic Distance Failures:** At asymptotic distances, QCD string tension depends only on N-ality, meaning the tension for double-charged Abelian Wilson loops should vanish due to screening by off-diagonal gluons ([Greensite 2003, Sec. 7.6.2](#Greensite2003)). However, the monopole dominance approximation fails to capture this; lattice data for double-charged Polyakov lines drastically disagree with the predictions of the monopole models, which incorrectly neglect the long-range effects of the off-diagonal gluons ([Greensite 2003, Sec. 7.6.2](#Greensite2003)).

* **Unobserved Flux Tubes:** The dual abelian Higgs models theoretically predict a multiplicity of different types of electric flux tubes that are not observed in actual QCD ([Greensite 2003, Sec. 7.6.1](#Greensite2003)).

* **Potential Gauge Artifacts:** There are concerns that the "Abelian dominance" observed on the lattice might be an artifact of the gauge-fixing procedure rather than a reflection of the underlying confinement mechanism, as alternative projections (like center projection) yield different dominant topological configurations ([Del Debbio et al. 1997, p. 2](#DelDebbioEtAl1997)).

* **Complications with Dynamical Quarks:** The dual superconductor picture is less robust when transitioning from pure gauge theories to (2+1)-flavor QCD with physical dynamical quarks ([Cea, Cosmai, Cuteri & Papa 2017, p. 5](#CCCP2017)). The presence of dynamical fermions introduces larger uncertainties and the possible onset of string breaking, which limits the explorable distance ranges and obscures clear trends in the flux tube parameters ([Cea, Cosmai, Cuteri & Papa 2017, p. 5](#CCCP2017)).

* **Theoretical Model Limitations:** The standard Abrikosov vortex ansatz diverges at the exact center of the flux tube, requiring alternative analytic functions to properly fit the lattice data ([Cea, Cosmai, Cuteri & Papa 2017, p. 4](#CCCP2017)). Furthermore, at very large distances between sources, the dual superconductivity hypothesis is expected to eventually fail and transition into an effective string theory description ([Cea, Cosmai, Cuteri & Papa 2017, p. 2](#CCCP2017)).
## Related concepts

* [[heterotic line bundle]]

## References


[[!include dual superconductor model -- references]]


[[!redirects dual superconductor model of confinement]]
[[!redirects dual superconductor model]]
[[!redirects dual superconductor]]
[[!redirects 't Hooft-Mandelstam model]]
