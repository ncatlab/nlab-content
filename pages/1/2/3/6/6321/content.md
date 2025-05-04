
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
#### Qunantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

_Quantum electrodynamics_ ("QED") is the [[perturbative quantum field theory]] of the [[electromagnetic field]] coupled to a [[Dirac field]] via the [[electron-photon interaction]]: it describes the [[quantum theory]] of [[photons]] and [[electrons]].

## Definition

The [[Lagrangian density]] defining QED is the [[sum]] of 

1. the [[free field]] contribution of the [[electromagnetic field]];

1. the [[free field]] contribution of a [[Dirac field]];

1. the [[electron-photon interaction]] term with [[coupling constant]] given by the [[fine structure constant]].

See at _[[A first idea of quantum field theory]]_ [this example](A+first+idea+of+quantum+field+theory#LagrangianQED).

The underlying [[free field theory]] admits a [[quantization]] via the corresponding [[Wick algebra]]. QED is, by definition, the [[perturbative quantum field theory]] obtained from this by finding a perturbative [[S-matrix]] for the [[electron-photon interaction]]. 

As a result, [[scattering amplitudes]] for [[electron-photon interactions]] in QED are then expressed in terms of [[Feynman amplitudes]]:

[[!include Feynman diagrams in causal perturbation theory -- summary]]


## Properties

* [[anomalous magnetic moment of the electron]]

* [[Lamb shift]]

* [[Casimir effect]]

* [[axial anomaly]]

## Related concepts

* [[fine structure constant]]

* [[photon propagator]]

* [[Schwinger effect]]

* [[quantum field theory]]

  * [[scalar field]]

  * [[gauge theory]]

    * **QED**

    * [[QCD]], [[quantization of Yang-Mills theory]]



## References

### Original articles

The term "quantum electrodynamics" is due to 

* [[Paul Dirac]]: _The quantum theory of emission and absorption of radiation_, Proc. Roy. Soc. London A **114** (1927) 243 &lbrack;[spire](http://inspirehep.net/record/42586?ln=en), [pdf](http://wwwhome.lorentz.leidenuniv.nl/~boyarsky/media/Proc.R.Soc.Lond.-1927-Dirac-243-65.pdf)&rbrack;

This left some issues with the quantization of the radiation field. These were addressed, and the [[causal propagator]] for the [[electromagnetic field]] was first found in 

* [[Pascual Jordan]], [[Wolfgang Pauli]], _Zur Quantenelektrodynamik ladungsfreier Felder_, Zeitschrift f&#252;r Physik 47, 151 (1928)

A comprehensive, albeit informal, theory of QED and of [[perturbative quantum field theory]] in general was eventually developed by

* [[Schwinger-Tomonaga-Feynman-Dyson]], 1940s

For more on the history see

* [[Rudolf Haag]], _Early papers on quantum field theory (1992-1930)_ ([pdf](https://link.springer.com/content/pdf/bfm%3A978-3-642-70078-1%2F1%2F1.pdf))

and ([Scharf 95, section 0.0](#Scharf95)).

On [[quantum electrodynamics]] via [[discretized light-cone quantization]]:

* [[Andrew C. Tang]], *Discretized light cone quantization: Application to quantum electrodynamics*, PhD thesis, Stanford (1990) &lbrack;[spire:296776](https://inspirehep.net/literature/296776), [pdf](https://inspirehep.net/files/5ef318e56c87e7561d36559f54895bd1), [[Tang-DLCQ.pdf:file]]&rbrack;

* {#TangBrodskyPauli91} [[Andrew C. Tang]], [[Stanley J. Brodsky]], [[Hans-Christian Pauli]], *Discretized light-cone quantization: Formalism for quantum electrodynamics*, Phys. Rev. D **44** (1991) 1842 &lbrack;[doi:10.1103/PhysRevD.44.1842](https://doi.org/10.1103/PhysRevD.44.1842)&rbrack;


Discussion of [[vacuum stability]] in [[QED]]:

* {#Scharf96} [[Günter Scharf]], _Vacuum stability in quantum field theory_, Nuovo Cim. A109 (1996) 1605-1607 ([spire:432208](http://inspirehep.net/record/432208/))

* {#Nikolic01} [[Hrvoje Nikolić]], _Physical stability of the QED vacuum_, 2001 ([arXiv:hep-ph/0105176](https://arxiv.org/abs/hep-ph/0105176))


The rigorous construction of [[perturbative QFT|perturbative]] QED in [[causal perturbation theory]] is worked out in 

* [Scharf 95](#Scharf95)

and refined to [[perturbative AQFT]] in

* {#DuetschFredenhagen98} [[Michael Dütsch]], [[Klaus Fredenhagen]], _A local (perturbative) construction of observables in gauge theores: the example of QED_ , Commun. Math. Phys. 203 (1999), no.1, 71-105,  ([arXiv:hep-th/9807078](http://xxx.uni-augsburg.de/abs/hep-th/9807078)). 

and generalized to possibly non-abelian [[Yang-Mills theory]] in

* {#Hollands07} [[Stefan Hollands]], _Renormalized Quantum Yang-Mills Fields in Curved Spacetime_, Rev. Math. Phys. 20:1033-1172, 2008 ([arXiv:0705.3340](https://arxiv.org/abs/0705.3340))

The [[weak adiabatic limit]] of QED was established in 

* {#BlanchardSeneor75} P. Blanchard and R. Seneor, _Green’s functions for theories with massless particles (in perturbation theory)_, Ann. Inst. H. Poincaré Sec. A
23 (2), 147–209 (1975) ([Numdam](http://www.numdam.org/item?id=AIHPA_1975__23_2_147_0))

* {#Duch17} [[Paweł Duch]], _Massless fields and adiabatic limit in quantum field theory_ ([arXiv:1709.09907](https://arxiv.org/abs/1709.09907))

The [[local net of algebras of observables]] and hence the [[algebraic adiabatic limit]] was worked out in

* [Dütsch-Fredenhagen 98](#DuetschFredenhagen98)

Further discussion of the [[adiabatic limit]] and [[infrared divergences]] includes

* Daniel Kapec, Malcolm Perry, Ana-Maria Raclariu, [[Andrew Strominger]], _Infrared Divergences in QED, Revisited_, Phys. Rev. D 96, 085002 (2017) ([arXiv:1705.04311](https://arxiv.org/abs/1705.04311))

On the *field strength formalism*, expressing [[scattering amplitudes]] of electrodynamics in terms of non-local expressions in the [[field strengths]]/[[flux densities]] instead of in the [[gauge potentials]]:

* Joshua Newey, John Terning, Christopher B. Verhaaren: *Schwinger vs Coleman: Magnetic Charge Renormalization*, Journal of High Energy Physics **2024** 75 (2024) &lbrack;[arXiv:2407.13823](https://arxiv.org/abs/2407.13823), <a href="https://doi.org/10.1007/JHEP11(2024)075">doi:10.1007/JHEP11(2024)075</a>&rbrack;

* Joshua Newey, John Terning, Christopher B. Verhaaren: *Geometrizing the Anomaly* &lbrack;[arXiv:2504.16998](https://arxiv.org/abs/2504.16998)&rbrack;



### Review

Traditional discussion includes

* [[Radovan Dermisek]], _Quantum Electrodynamics (QED)_ ([pdf](http://www.physics.indiana.edu/~dermisek/QFT_09/qft-II-5-4p.pdf), [[DermisekQED.pdf:file]])

* [[Hitoshi Murayama]], _Quantum Electrodynamics_ ([pdf](http://hitoshi.berkeley.edu/221B-S02/QED.pdf))

* {#Zeidler} [[Eberhard Zeidler]], _Quantum field theory II: Quantum electrodynamics --  A bridge between mathematicians and physicists_, Springer (2009)

* Einan Gardi, lectures 19, 20 of _[Modern Quantum Field Theory](https://www2.ph.ed.ac.uk/~egardi/MQFT/)_, 2015 ([pdf](https://www2.ph.ed.ac.uk/~egardi/MQFT/MQFT_2015_lecture_19_20.pdf))
  
Mathematically rigorous discussion in [[causal perturbation theory]]/[[perturbative AQFT]] is in

* {#Scharf95} [[Günter Scharf]], _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition

* {#Duetsch18} [[Michael Dütsch]], chapter 5 of _[[From classical field theory to perturbative quantum field theory]]_, 2018

  following ([Dütsch-Fredenhagen 98](#DuetschFredenhagen98))


### Phenomenology

Comparison to [[experiment]] is reviewed in

* _Tests of QED_ ([pdf](http://edu.itp.phys.ethz.ch/hs10/ppp1/PPP1_6.pdf))

Specifically via the [[Lamb shift]]:

* Savely G. Karshenboim, D. I. Mendeleev, _The Lamb Shift of Hydrogen and Low-Energy Tests of QED_ ([arXiv:hep-ph/9411356](https://arxiv.org/abs/hep-ph/9411356))


[[!redirects quantum electrodynamics]]
[[!redirects quantum electro dynamics]]
[[!redirects QED]]
