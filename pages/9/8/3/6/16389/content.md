
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

### General
 {#General}

In [[Hamiltonian]] formulation of [[relativistic quantum field theory]] on [[Minkowski spacetime]] there are three essential choices of forms of [[hypersurfaces]] to [[foliation|foliate]] [[spacetime]] by &lbrack;[Dirac (1949)](#Dirac49)&rbrack;:

<center>
<img src="https://ncatlab.org/nlab/files/DiracFormsOfHamiltonianDynamics.jpg" width="600">
</center>

> (Fig. 1 from [Brodsky, Pauli & Pinsky (1998)](#BrodskyPauliPinsky98))

The "instant form" on the left [[foliation|foliates]] [[spacetime]] by [[spacelike]] [[hypersurfaces]] (cf. [[Cauchy surface]]). This is the form considered for [[Hamiltonian mechanics]] in most of the literature (certainly in the case of [[quantum mechanics]], cf. &lbrack;[Dirac (1949) §3](#Dirac49)&rbrack;).


In contrast, *light-cone quantization* corresponds to the choice of [[foliation]] by [[lightlike]] [[wavefronts]] &lbrack;[Dirac (1949) §5](#Dirac49)&rbrack;.

[Dirac (1949) §8](#Dirac49):

> The instant form has the advantage of being the one people are most familiar with, but I do not believe it is intrinsically any better for this reason. &lbrack;...&rbrack;

> The front form has the advantage that it requires only three Hamiltonians, instead of the four of the other forms. This makes it mathematically the most interesting form, and makes any problem of finding Hamiltonians substantially easier. 

> The front form has the further advantage that there is no square root in the Hamiltonians, which means that one can avoid negative energies for particles by suitably choosing the values of the dynamical variables in the front, without having to make a special convention about the sign
of a square root. 

(...)

### Discretized light-cone quantization
 {#DiscreteLightConeQuantization}

For [[nonperturbative quantum field theory|non-perturbative]] computations it turns out at least convenient (if not necessary) to in addition assume/impose periodic [[boundary conditions]] along the lightlike front, hence, in flat lightcone coordinates $x^{\pm}$, so that all fields $\phi$ satisfy

$$
  \phi\big(
    x^- + L,\, x^+
  \big)
  \;=\;
  \phi\big(
    x^-,\, x^+
  \big)
$$

for some $L \in \mathbb{R}_{\gt 0}$ giving the circumference of a lightlike [[circle]] (which some authors take to be literally [[lightlike]], of the kind shown eg. in [Bär 2004, Exp. 2.21 (2)](Lorentizan+geometry#Bär04), while others, like [Seiberg 1997](#Seiberg97), consider to be the [[limit of a sequence|limit]] of [[boosts]] of a [[spacelike]] [[circle]] [[fiber]]).

Since, [[Fourier transform|dually]], this means that the corresponding lightcone momentum $p^+$ becomes quantized in units of the inverse [[radius]] $R$ of this circle

\[
  \label{LightConeMomentumQuantization}
  p^+ \;\propto\; N/R
  \phantom{AAA}
  N \in \mathbb{Z}
  \,,
\]

hence one speaks of *discretized light-cone quantization*  or _DLCQ_, for short. This goes back to [Maskawa & Yamakawi 1976](#MaskawaYamakawi76); [Casher 1976](#Casher76); [Thorn 1977](#Thorn77), [1978](#Thorn78); [Pauli & Brodsky (1985b)](#PauliBrodsky85b), [(1985a)](#PauliBrodsky85a); [Tang, Brodsky & Pauli 1991 (2.6)](#TangBrodskyPauli91); see also [McCartor & Robertson 1994, §3](#McCartorRobertson94); for review see [Burkardt 1996, §5.1](#Burkardt96); [Heinzl 2001, §3.4](#Heinzl01).

Often it turns out that [[negative number|negative]] values of $N$ in (eq:LightConeMomentumQuantization) can be neglected or integrated out, so that 

$$
  N \in \mathbb{N}
$$

becomes a [[natural number]]-parameter akin to that considered in the [['t Hooft double line construction]] of [[gauge theories]], and then the [[large N limit]] of the discrete light cone quantization becomes of interest.


### For sigma-models

In [[quantization]] of [[sigma models]] whose [[target space]] has a [[lightlike]] [[Killing vector]], the strategy of light-cone gauge quantization is to [[gauge fixing|gauge fix]] the [[metric]] and [[diffeomorphisms]] of the [[worldvolume]] such that also the worldvolume has a [[lightlike]] [[Killing vector field]] and such that this is mapped to the given one on target space.

This typically fixes most of the available gauge freedom, and the strategy is then to apply [[quantization]] to what remains. For more on this general idea see at _[[quantization commutes with reduction]]_.

Often this is considered for [[target space]] being [[Minkowski spacetime]] $\mathbb{R}^{d-1,1}$ and with $X^+ \coloneqq X^0 - X^1$ denoting one of its canonical lightlike [[coordinates]]. If $\tau$ denotes similarly a lightlike coordinate function on the [[worldvolume]], then the condition of light-cone gauge reads

$$
  X^+ = p^+ \tau
$$

for some proportionality constant $p^+$, the *light cone momentum*.  This is how light cone gauge appears in much of the [[string theory]] literature.



## Applications

### Quantization of Green-Schwarz super $p$-brane sigma models

Light cone gauge quantization is the only method by which [[Green-Schwarz super p-brane sigma models]] have been quantized, to date. 

### BFSS matrix model

Specifically, applying light-cone gauge quantization to the [[Green-Schwarz sigma model]] for the  [[M2-brane]] on 11d [[Minkowski spacetime]], combined with a certain regularization of the remaining light-cone [[Hamiltonian]] yields the [[BFSS matrix model]].

### BMN matrix model 

Alternatively, applying the light cone gauge quantization of the [[Green-Schwarz sigma-model]] of the [[M2-brane]] not on [[Minkowski spacetime]] but, more generally, on 11d [[pp-wave spacetimes]] (which are [[Penrose limits]] of the [[near horizon geometry]] of the [[black brane|black]] [[M2-branes]]/[[M5-branes]]) yields the [[BMN matrix model]].


## Related concepts

* [[large N limit]]

* [[holographic light front QCD]]


## References

### General

The concept originates with

* {#Dirac49} [[Paul A. M. Dirac]], §5 in "The Front Form", in: *Forms of Relativistic Dynamics*, Rev. Mod. Phys. **21** (1949) 392-399 &lbrack;[doi:10.1103/RevModPhys.21.392](https://doi.org/10.1103/RevModPhys.21.392)&rbrack;

reviewed in

* K. K. Wan, J. J. Powis, *Quantum mechanics in Dirac's front form*,  Int J Theor Phys **33** (1994) 553–574 &lbrack;[doi:10.1007/BF00670516](https://doi.org/10.1007/BF00670516)&rbrack;

and was rediscovered several times, such as in the guise of "infinite momentum frame" field theory:

* [[Steven Weinberg]], *Dynamics at Infinite Momentum*, Phys. Rev. **150** (1966) 1313,  Erratum Phys. Rev. 158, 1638 (1967) &lbrack;[doi:10.1103/PhysRev.150.1313](https://doi.org/10.1103/PhysRev.150.1313)&rbrack;

see also [Chang & Ma 1969](#ChangMa69) and [Kogut & Soper 1970](#KogutSoper70)


Early review:

* Shau-Jin Chang, Robert G. Root, and Tung-Mow Yan, *Quantum Field Theories in the Infinite-Momentum Frame. I. Quantization of Scalar and Dirac Fields*, Phys. Rev. D **7**,  (1973) 1133 &lbrack;[doi:10.1103/PhysRevD.7.1133](https://doi.org/10.1103/PhysRevD.7.1133)&rbrack;

* [[Stanley J. Brodsky]], [[Gary McCartor]], [[Hans-Christian Pauli]], [[Stephen S. Pinsky]], *The challenge of light-cone quantization of gauge field theory*, Particle World **3** 3 (1993) 109-124  &lbrack;[cds:240388](http://cds.cern.ch/record/240388), [inspire:335247](https://inspirehep.net/literature/335247)&rbrack;

* Wei-Min Zhang, *Light-Front Dynamics and Light-Front QCD*, Chin. J. Phys. **32** (1994) 717-808 &lbrack;[arXiv:hep-ph/9412244](https://arxiv.org/abs/hep-ph/9412244)&rbrack;

* {#Burkardt96} [[Matthias Burkardt]], *Light Front Quantization*, Adv. Nucl. Phys. **23** (1996) 1-74 &lbrack;[arXiv:hep-ph/9505259](https://arxiv.org/abs/hep-ph/9505259), [doi:10.1007/0-306-47067-5_1](https://doi.org/10.1007/0-306-47067-5_1)&rbrack;

Further review:

* Guillaume Beuf, Meijian Li, Tolga Altinoluk, Fabio Dominguez, *Course on Light-Cone Techniques applied to QCD*  (2022) &lbrack;[indico:1203236](https://indico.cern.ch/event/1203236)&rbrack;

* [[Stanley Brodsky]], [[Thomas Heinzl]] et al. *Light-Front Quantum Chromodynamics: A framework for the analysis of hadron physics*, White Paper of International Light Cone Advisory Committee, Nuclear Physics B - Proceedings Supplements **251**, **252** (2014) 165-174 &lbrack;[doi:10.1016/j.nuclphysbps.2014.05.004](https://doi.org/10.1016/j.nuclphysbps.2014.05.004), [arXiv:1309.6333](https://arxiv.org/abs/1309.6333)&rbrack;

* J. Vary et al. *Basis Light-Front Quantization: Recent Progress and Future Prospects*, Few-Body Syst **57** (2016) 695–702 &lbrack;[doi:10.1007/s00601-016-1117-x](https://doi.org/10.1007/s00601-016-1117-x)&rbrack;
 
* Wikipedia, *[Light front quantization](https://en.wikipedia.org/wiki/Light_front_quantization)*

* Wikipedia, [Light-front computational methods](https://en.wikipedia.org/wiki/Light-front_computational_methods)

See also:

* A. Harindranath, *[Light Front Dynamics](https://www.saha.ac.in/theory/a.harindranath/light/light.html)* (web resources) 

The notion of lightlike circle compactification ("discretized light-cone quantization"):


* {#MaskawaYamakawi76} [[Toshihide Maskawa]], [[Koichi Yamakawi]], *The Problem of $P^+ = 0$ Mode in the Null-Plane Field Theory and Dirac's Method of Quantization*, Progress of Theoretical Physics **56** 1 (1976) 270–283 &lbrack;[doi:10.1143/PTP.56.270](https://doi.org/10.1143/PTP.56.270)&rbrack;

* {#Casher76} [[Aharon Casher]], *Gauge fields on the null plane*, Phys. Rev. D **14** (1976) 452 &lbrack;[doi:10.1103/PhysRevD.14.452](https://doi.org/10.1103/PhysRevD.14.452)&rbrack;

* {#Thorn77} [[Charles B. Thorn]], *On the derivation of dual models from field theory*, Physics Letters B **70** 1  (1977) 85-87 &lbrack;<a href="https://doi.org/10.1016/0370-2693(77)90351-3">doi:10.1016/0370-2693(77)90351-3</a>&rbrack;

* {#Thorn78} [[Charles B. Thorn]], *Derivation of dual models from field theory. II*, Phys. Rev. D **17** (1978) 1073 &lbrack;[doi:10.1103/PhysRevD.17.1073](https://doi.org/10.1103/PhysRevD.17.1073)&rbrack;

* {#PauliBrodsky85a} [[Hans-Christian Pauli]], [[Stanley J. Brodsky]], *Solving field theory in one space and one time dimension*, Phys. Rev. D **32** (1985) 1993 &lbrack;[doi:10.1103/PhysRevD.32.1993](https://journals.aps.org/prd/abstract/10.1103/PhysRevD.32.1993)&rbrack;

* {#Pauli99} [[Hans-Christian Pauli]], *Discretized light-cone quantization and the effective interaction in hadrons*, AIP Conf. Proc. **494** (1999) 80-139 &lbrack;[arXiv:hep-ph/9910203](https://arxiv.org/abs/hep-ph/9910203), [doi:10.1063/1.1301662](https://doi.org/10.1063/1.1301662)&rbrack;

and on the issue of excluding $p^+ = 0$:

* [[Joel S. Rozowsky]], [[Charles B. Thorn]], *Spontaneous Symmetry Breaking at Infinite Momentum without $P^+$ Zero-Modes*, Phys. Rev. Lett. **85** (2000) 1614-1617 &lbrack;[arXiv:hep-th/0003301](https://arxiv.org/abs/hep-th/0003301), [doi:10.1103/PhysRevLett.85.1614](https://doi.org/10.1103/PhysRevLett.85.1614)&rbrack;

See also:

* [[Glenn Barnich]], Sucheta Majumdar, [[Simone Speziale]], Wen-Di Tan, *Lessons from discrete light-cone quantization for physics at null infinity: Bosons in two dimensions* &lbrack;[arXiv:2401.14873](https://arxiv.org/abs/2401.14873)&rbrack;

* Philip D. Mannheim; *Physics on and off the light cone* &lbrack;[arXiv:2501.18068](https://arxiv.org/abs/2501.18068)&rbrack;

* S.S. Chabysheva, J.R. Hiller: *Zero Modes on the Light Front* &lbrack;[arXiv:2502.01775](https://arxiv.org/abs/2502.01775)&rbrack;




Lecture notes:

* {#Heinzl01} [[Thomas Heinzl]], *Light-Cone Quantization: Foundations and Applications*, in *Methods of Quantization*, Lecture Notes in Physics **572**, Springer (2001) &lbrack;[arXiv:hep-th/0008096](https://arxiv.org/abs/hep-th/0008096), [doi:10.1007/3-540-45114-5_2](https://doi.org/10.1007/3-540-45114-5_2)&rbrack;

More on the case of [[gauge fields]]:

* {#McCartorRobertson94} [[Gary McCartor]], David G. Robertson, *Light-cone quantization of gauge fields*, Zeitschrift für Physik C Particles and Fields **62** (1994) 349–355 &lbrack;[doi:10.1007/BF01560250](https://doi.org/10.1007/BF01560250)&rbrack;

In relation to [[spontaneous symmetry breaking]]:

* [[Stephen S. Pinsky]], *The Light-Cone Field Theory Paradigm for Spontaneous Symmetry Breaking*, in: *Proceedings, Hadron Structure 93 : Banská Štiavnica, September 5-10, 1993* &lbrack;[arXiv:hep-th/9405091](https://arxiv.org/abs/hep-th/9405091), [inspire:364380](https://inspirehep.net/literature/364380)&rbrack;


In relation to instant-time quantization:

* Philip D. Mannheim, _Light-front quantization is instant-time quantization_ &lbrack;[arXiv:1909.03548](https://arxiv.org/abs/1909.03548)&rbrack;

* Philip D. Mannheim, Peter Lowdon, [[Stanley Brodsky]], 
*Comparing light-front quantization with instant-time quantization*, Physics Reports **891** (2021) 1-65 &lbrack;[arXiv:2005.00109](https://arxiv.org/abs/2005.00109), [doi:10.1016/j.physrep.2020.09.001](https://doi.org/10.1016/j.physrep.2020.09.001)&rbrack;

Discussion of ([[reduced phase space|reduced]]) [[phase spaces]] in light-cone coordinates:

* Prem P. Srivastava, *Constraints and Hamiltonian in light-front quantized field theory*, Nuovo Cim. A **107** (1994) 549-558 &lbrack;[arXiv:hep-th/9308046](https://arxiv.org/abs/hep-th/9308046), [doi:10.1007/BF02768789](https://doi.org/10.1007/BF02768789)&rbrack;

* Kianoosh Kargar, Ahmad Shirzad, Majid Monemzadeh, *Dynamical structure of fields in light cone coordinates*, Phys. Rev. D **99** (2019) 045019 &lbrack;[arXiv:1608.03255](https://arxiv.org/abs/1608.03255), [doi:10.1103/PhysRevD.99.045019](https://doi.org/10.1103/PhysRevD.99.045019)&rbrack;

### Application to quantum electrodynamics

Application to [[quantum electrodynamics]]:

* {#ChangMa69} Shau-Jin Chang, Shang-Keng Ma, *Feynman Rules and Quantum Electrodynamics at Infinite Momentum*, Phys. Rev. **180** (1969) 1506 &lbrack;[doi:10.1103/PhysRev.180.1506](https://doi.org/10.1103/PhysRev.180.1506)&rbrack;

* {#KogutSoper70} John B. Kogut and Davison E. Soper, *Quantum Electrodynamics in the Infinite-Momentum Frame*, Phys. Rev. D **1** (1970) 2901 &lbrack;[doi:10.1103/PhysRevD.1.2901](https://doi.org/10.1103/PhysRevD.1.2901)&rbrack;

* [[Andrew C. Tang]], *Discretized light cone quantization: Application to quantum electrodynamics*, PhD thesis, Stanford (1990) &lbrack;[spire:296776](https://inspirehep.net/literature/296776), [pdf](https://inspirehep.net/files/5ef318e56c87e7561d36559f54895bd1), [[Tang-DLCQ.pdf:file]]&rbrack;


* {#TangBrodskyPauli91} [[Andrew C. Tang]], [[Stanley J. Brodsky]], [[Hans-Christian Pauli]], *Discretized light-cone quantization: Formalism for quantum electrodynamics*, Phys. Rev. D **44** (1991) 1842 &lbrack;[doi:10.1103/PhysRevD.44.1842](https://doi.org/10.1103/PhysRevD.44.1842)&rbrack;

and to pure [[electromagnetism]]:

* Martina M. Brisudova, *Electromagnetic duality and light-front coordinates*, Phys. Rev. D **59** (1999) 087702 &lbrack;[arXiv:hep-th/9806196](https://arxiv.org/abs/hep-th/9806196), [doi:10.1103/PhysRevD.59.087702](https://doi.org/10.1103/PhysRevD.59.087702)&rbrack;


* Sucheta Majumdar, *Residual gauge symmetry in light-cone electromagnetism*,  J. High Energ. Phys. **2023** 215 (2023) &lbrack;[arXiv:2212.10637](https://arxiv.org/abs/2212.10637), <a href="https://doi.org/10.1007/JHEP02(2023)215">doi:10.1007/JHEP02(2023)215</a>&rbrack;


### Application to quantum chromodynamics
 {#ReferencesApplicationToQCD}

Application of (discretized) light cone quantization to to [[QCD]]:

* [[G. Peter Lepage]], [[Stanley J. Brodsky]], *Exclusive processes in perturbative quantum chromodynamics*, Phys. Rev. D **22** (1980) 2157 &lbrack;[doi:10.1103/PhysRevD.22.2157](https://doi.org/10.1103/PhysRevD.22.2157)&rbrack;

* {#PauliBrodsky85b} [[Hans-Christian Pauli]], [[Stanley J. Brodsky]], *Discretized light-cone quantization: Solution to a field theory in one space and one time dimension*, Phys. Rev. D **32** (1985) 2001 &lbrack;[doi:10.1103/PhysRevD.32.2001](https://doi.org/10.1103/PhysRevD.32.2001)&rbrack;

* {#BrodskyPauliPinsky98} [[Stanley Brodsky]], [[Hans-Christian Pauli]], [[Stephen S. Pinsky]], *Quantum Chromodynamics and Other Field Theories on the Light Cone*, Phys. Rept. **301** (1998) 299-486 &lbrack;[arXiv:hep-ph/9705477](https://arxiv.org/abs/hep-ph/9705477), <a href="https://doi.org/10.1016/S0370-1573(97)00089-6">doi:10.1016/S0370-1573(97)00089-6</a>&rbrack;



Review in the broader context of [[non-perturbative quantum field theory]]:

* [[Yitzhak Frishman]], [[Jacob Sonnenschein]], §12 in: *Non-Perturbative Field Theory -- From Two Dimensional Conformal Field Theory to QCD in Four Dimensions*, Cambridge University Press (2010) &lbrack;[doi:10.1017/CBO9780511770838](https://doi.org/10.1017/CBO9780511770838), summary: [arXiv:1004.4859](https://arxiv.org/abs/1004.4859)&rbrack; open access (2023) &lbrack;[doi:10.1017/9781009401654](https://doi.org/10.1017/9781009401654)&rbrack;



A light-cone QCD-[[Lagrangian density]] adapted to [[MHV amplitudes]]:

* Hiren Kakkad, Piotr Kotko, Anna Stasto, *Quantum correction to a new Wilson line-based action for Gluodynamics* &lbrack;[arXiv:2311.04101](https://arxiv.org/abs/2311.04101)&rbrack;



### Application in string theory

Light cone quantization of the [[string]] [[sigma-model]] originates with 

* [[Peter Goddard]], [[Jeffrey Goldstone]], [[Claudio Rebbi]], [[Charles B. Thorn]],  §2.2 in: *Quantum dynamics of a massless relativistic string*, Nuclear Physics B **56** 1 (1973) 109-135 &lbrack;<a href="https://doi.org/10.1016/0550-3213(73)90223-X">doi:10.1016/0550-3213(73)90223-X</a>&rbrack;

see also

* [[Charles B. Thorn]], *Quantum Newtonian Dynamics on a Light Front*, Phys.Rev. D **59** (1999) 025005 &lbrack;[arXiv:hep-th/9807151](https://arxiv.org/abs/hep-th/9807151), [doi:10.1103/PhysRevD.59.025005](https://doi.org/10.1103/PhysRevD.59.025005)&rbrack;


All the standard introductory texts on [[string theory]] have sections devoted to light-cone quantization. For instance:

* {#GreenSchwarzWitten88} [[Michael Green]], [[John Schwarz]], [[Edward Witten]], section 5.2.1 of: _Superstring theory_, 3 vols. Cambridge Monographs on Mathematical Physics 1988 (Vol 1: [spire:250488](http://inspirehep.net/record/250488), [ISBN:9781107029118](https://www.cambridge.org/us/academic/subjects/physics/theoretical-physics-and-mathematical-physics/superstring-theory-25th-anniversary-edition-volume-1?format=HB&isbn=9781107029118))


In the context of the [[BFSS matrix model]] as a discrete light-cone formulation of [[M-theory]]:


* {#Seiberg97} [[Nathan Seiberg]], *Why is the Matrix Model Correct?*, Phys. Rev. Lett. **79** (1997) 3577-3580 &lbrack;[arXiv:hep-th/9710009](https://arxiv.org/abs/hep-th/9710009), [doi:10.1103/PhysRevLett.79.3577](https://doi.org/10.1103/PhysRevLett.79.3577)&rbrack;

* [[Adel Bilal]], *DLCQ of M-Theory as the Light-Like Limit*, Phys. Lett. B **435** (1998) 312-318 &lbrack;[arXiv:hep-th/9805070](https://arxiv.org/abs/hep-th/9805070), <a href="https://doi.org/10.1016/S0370-2693(98)00811-9">doi:10.1016/S0370-2693(98)00811-9</a>&rbrack;

Review:

* {#Ydri18} [[Badis Ydri]], Section 3.9 of: _Review of M(atrix)-Theory, Type IIB Matrix Model and Matrix String Theory_ &lbrack;[arXiv:1708.00734](https://arxiv.org/abs/1708.00734)&rbrack;, published as: _Matrix Models of String Theory_, IOP (2018) &lbrack;[ISBN:978-0-7503-1726-9](https://iopscience.iop.org/book/978-0-7503-1726-9)&rbrack;


[[!include quantization of M2-brane on Minkowski spacetime to BFSS matrix model -- references]]



[[!redirects light cone quantization]]

[[!redirects light-cone gauge quantization]]
[[!redirects light cone gauge quantization]]

[[!redirects discretized light-cone quantization]]
[[!redirects discretized light cone quantization]]

[[!redirects light-cone gauge]]
[[!redirects light cone gauge]]
[[!redirects lightcone gauge]]

[[!redirects light front quantization]]

[[!redirects discrete light front quantization]]

[[!redirects discrete light cone quantization]]
[[!redirects discrete light-cone quantization]]
[[!redirects discrete lightcone quantization]]
[[!redirects discrete light cone quantizations]]
[[!redirects discrete light-cone quantizations]]
[[!redirects discrete lightcone quantizations]]

[[!redirects DLCQ]]

[[!redirects light-front quantization]]

[[!redirects light cone momentum]]
[[!redirects light-cone momentum]]
[[!redirects lightcone momentum]]

[[!redirects light cone longitudal]]
[[!redirects light cone transversal]]
[[!redirects light-cone longitudal]]
[[!redirects light-cone transversal]]
[[!redirects lightcone longitudal]]
[[!redirects lightcone transversal]]

[[!redirects light-front formalism]]

