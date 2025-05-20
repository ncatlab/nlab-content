

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Solid state physics
+-- {: .hide}
[[!include solid state physics -- contents]]
=--
#### Topological physics
+--{: .hide}
[[!include topological physics -- contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea
 {#Idea}

### General
 {#GeneralIdea}

In [[solid state physics]], a [[phase of matter]] (of a [[quantum material]]) is called *topological* (sometimes: a *topological state of matter*), within a given [[energy]] bound $\Delta$ (the "[[spectral gap|gap]]") if external deformations of the system that are gentle enough -- namely "[[adiabatic theorem|adiabatic]]" -- not to excite modes ([[quanta]]) $\gt \Delta$ above the [[ground state]] leave the main properties of the system [[invariant]]. This is vaguely reminiscent of how [[topology]] is concerned with properties of [[spaces]] that are invariant under "gentle" -- namely "[[continuous map|continuous]]" -- deformations. Indeed, it turns out or is expected that topological phases of matter may be characterized (classified) by certain [[homeomorphism classes]] or rather by [[homotopy classes]] of the kind studied in [[topology]], or rather in [[homotopy theory]] and [[generalized cohomology theory]] (e.g. the [[K-theory classification of topological phases of matter]]).

Such topological phases are fundamentally different from classical [[phases of matter]] in that they are *not* controlled by the [[Landau theory of phase transitions]].


### Topological insulators

For instance, a [[topological insulator]]-phase of a [[crystal|crystalline]] material (a prime example being [[graphene]], see also [below](#ExampleGraphene)) is one where the [[valence band]] of energies occupied by the crystal's [[electrons]] is separated by such an [[spectral gap|energy gap]] from the [[conduction band]], and where the [[valence bundle]] of the electron's occupied [[quantum states]], as a [[topological vector bundle]] over the material's [[Brillouin torus]], has (see also [[fiber bundles in physics]]):

1. a non-[[trivial bundle|trivial]] [[equivariant bundle|equivariant]] [[homeomorphism class]], in fact 

1. a non-trivial [[equivariant homotopy class|equivariant]] [[homotopy class]] of its [[classifying map]], in fact

1. a non-vanishing [[Whitehead-generalized cohomology|generalized]] [[cohomology class]] in [[twisted equivariant K-theory|twisted equivariant]] [[topological K-theory]].

This is part of the statement of the *[[K-theory classification of topological phases of matter]]* (for which there is some [[experiment|experimental]] and [[theoretical physics|theoretical]] support but which, one should admit, remains a [[conjecture]]). 

The idea is that no gentle/[[quantum adiabatic theorem|adiabatic]] deformation of such a [[topological insulator]]-phase (eg. by changing ambient [[pressure]], tension, [[electric fields]], etc.) can change the "topological" (rather: homotopy-theoretic) class of the [[valence bundle]], and all the material's properties implied by this non-trivial class (notably the nature of its "[[edge modes]]") remain unchanged under such deformation. 

Here the [[equivariance]] is with respect to any or all of: 

1. *spatial* [[crystallographic group|crystallographic point]] symmetries,

1. *non-spatial* symmetries, including:

   1. [[CPT theorem|CPT symmetries]] like [[time-reversal symmetry]],

   1. "[[internal symmetry|internal]]" or "on-site" symmetries 

         (such as [[spin]]-reversal symmetries in systems negligible [[magnetic field]] and [[spin-orbit coupling]])

which all [[group action|act]] on: 

1. the [[Brillouin torus]] and/or

1. the [[quantum observables|observables]] of the system 

   (eg. on the [[Hamiltonian]] by [[complex conjugation]], for the case of [[time-reversal symmetry]]).

If the class of a topological phase of matter crucially depends on its  [[equivariance]] under such [[symmetries]], hence if the phase could/would decay under deformations which (albeit remaining [[quantum adiabatic theorem|adiabatic]]) [[symmetry breaking|break]] some of the symmetry, then one speaks of a *[[symmetry protected topological phase]]*. The richness of topological phases all comes from this [[symmetry protected topological phase|symmetry protection]]. 

For instance, without any symmetry protection the [[valence bundles]] in a [[topological insulator]]-[[phase of matter|phase]] of a realistic crystalline material (necessarily of effective dimension $\leq 3$) are characterized entirely by their [[first Chern class]]; one speaks of a *[[Chern insulator]]*-phase. 

If a more fine-grained topological phase is "[[symmetry protected topological phase|protected]]" by [[crystallographic group|crystallographic symmetry]], then one speaks of a *[[topological crystalline insulator]]*-phase, etc.

### Topological semi-metals

More generally, there are topological phases where small [[quantum adiabatic theorem|adiabatic]] deformations have no effect, as before, but where the [[topological space]] *of possible deformations* has itself a non-trivial [[topological space|topology]], for instance a non-trivial [[fundamental group]], in which case the end result of a  *[[loop]] of deformations* may have the effect of having transformed the system's [[ground state]] by a [[unitary operator]] which depends on the [[homotopy class]] of this loop.

For example, if there is an [[energy gap]] *except* over a [[codimension]]$\geq 2$ [[submanifold]] of "band crossings" or "nodal loci" inside the [[Brillouin torus]], where the [[spectral gap|gap]] closes right at the [[chemical potential]], then one speaks of a *topological [[semi-metal]]*-phase. 
In this case the [[valence bundle]] is well-defined (only) on the [[complement]] of these "nodal" points, as before, and as such again invariant under gentle deformations, but now these external deformations (which will gently shift the [[energy bands]]) may move the position of the nodal band-crossing points through the [[Brillouin torus]]. 
If a loop of such deformations has the effect of [[braid group|braiding]] these nodal points around each other then it may in total have the effect of having transformed the [[ground state]] by an operation in a [[braid group representation]]. 

If this braiding is [[non-abelian group|non-abelian]], and/or if the [[holonomy]] of the [[Berry connection]] around the nodal points is [[non-abelian group|non-abelian]], it follows in particular that the ground state is "degenerate" ("has multiplicity") hence that there is a [[Hilbert space]] of states, all of the ground state energy at the chemical potential, whose [[dimension of a vector space|dimension]] is $\geq 2$. In this case one says that the topological phase in addition exhibits *[[topological order]]* or that its ground states exhibits "[[short-range entanglement|long-range entanglement]]" (at least "no [[short-range entanglement]]").

### Topological field theory
 {#TopologicalFieldTheory}

Therefore, in this case of [[topological order]], the [[quantum adiabatic theorem|adiabatic]] [[dynamics]] of the [[ground state]] of the topological material, say as the nodal points are [[braid group|braided]] around each other, is characterized by:

1. a [[finite-dimensional vector space|finite-dimensional]] [[Hilbert space]] [[space of quantum states]] 

   (the degenerate ground state),

1. a vanishing [[Hamiltonian]] 

   (being the restriction of the full Hamiltonian of the material to its energy=0 eigenstates),

1. global dynamics depending (only) on the "[[topology]]" (really: the [[homotopy type]]) of the trajectory

   (such as on the [[braid group|braid]] formed by the [[worldlines]] of the nodal points).

These are exactly the characteristics of a [[topological field theory]] of the type of [[Chern-Simons theory]], which here one may understand as the tiny but highly interesting subsector "below the gap" of the full non-topological [[quantum field theory]] that describes all the higher excitations of the given material (which is at least as rich as [[quantum electrodynamics]] in the [[background field|background]] of the [[electromagnetic field|Coulomb potential]] of the [[atomic nuclei]] on the crystal sites, see also [here](Dirac+field#FreeDiracFieldInCoulombBackground)).


### Anyons

Generally, it is expected that [[codimension]]=2 [[defects]] in a topological phase  of matter exhibit such a ([[symmetry protected topological order|symmetry protected]]) *[[topological order]]* in that the [[adiabatic theorem|adiabatic]] [[braid group|braiding]] of them around each other inside the topological host material is described by a [[topological quantum field theory]] and in particular constitutes a [[braid group representation]] on the systems [[ground state]]. 

In this case one refers to these defects also a *[[anyons]]*. 

The [[AdS3-CFT2 and CS-WZW correspondence|CS-WZW correspondence]] between [[Chern-Simons theory]] and the [[Wess-Zumino-Witten model]] then predicts that the [[wavefunctions]] that constitute these anyonic ground states in topological phases are given by [[conformal blocks]] of a [[2d CFT]], and it seems that this is indeed the case.

The idea to use the resulting monodromy [[braid representations]] constituted by the [[conformal blocks]] as [[quantum gates]] in a [[quantum computer]] underlies the subject of *[[topological quantum computation]]*.

The technical problem with implementing this and related ideas is that, in general, the [[energy gap]] of a topological phase of matter is small, so that it is first of all hard to detect and second it will be hard to *preserve* (hence hard to remain in the topological phase) as one tries to put the "topological properties" of a [[quantum material]] to use.




## Examples
 {#Examples}


### Quantum Hall effect

* [[quantum Hall effect]], [[quantum spin Hall effect]]


### Graphene
 {#ExampleGraphene}
 
The first and archetypical example of all these phenomena is seen in *[[graphene]]*, where a band gap *almost* closes over two nodal *[[Dirac points]]* (up to a tiny shift by the [[spin-orbit coupling]]).


The topological phase/order of graphene is "[[symmetry protected topological phase|symmetry protected]]": 

That this must be the case follows already from the fact that any plain [[complex vector bundle]] (such as the [[valence bundle]] may naively seem to be) is necessarily [[trivial bundle|trivial]] over the [[complement]] of two Dirac points inside the Brillouin [[2-torus]] (a punctured torus, see [[torus#AsAHomotopyType|here]]).
Indeed, the [[dynamics]] of the [[electrons]] in graphene is "$T I$"-symmetric, which forces the valence bundle to be a [[real vector bundle]] with a class not in [[KU-theory]] but in [[KO-theory]], which may be non-trivial over a punctured torus (see at *[[Möbius strip]]*). This non-triviality of the $T I$-symmetric valence bundles is exhibited by non-trivial [[Berry phases]] around the two nodal points.

### Haldane model

* [[Haldane model]]


## Related entries

* [[phase of matter]], [[quantum material]]

* [[gapped Hamiltonian]]

* [[topological field theory]]

* [[tensor network state]]

* [[quantum Hall effect]]

* [[topological insulator]]

* [[topological order]]

* [[quantum spin liquid]]

* [[strange metal]]

* [[Weyl semimetal]]

* in [[metamaterials]]:

  * [[topological photonics]]

  * [[topological phononics]]

* [[topological quantum computing]]

* [[quantum spin Hall effect]]

* [[entanglement]]


## References

### Reviews

Textbook accounts:

* Sanju Gupta, Avadh Saxena, *The Role of Topology in Materials*,  Springer Series in Solid-State Sciences **189**, 2018 ([doi:10.1007/978-3-319-76596-9](https://link.springer.com/book/10.1007/978-3-319-76596-9))

* {#Vanderbilt18} [[David Vanderbilt]],  *Berry Phases in Electronic Structure Theory -- Electric Polarization, Orbital Magnetization and Topological Insulators*, Cambridge University Press (2018) ([doi:10.1017/9781316662205](https://doi.org/10.1017/9781316662205))

* [[Bei Zeng]], [[Xie Chen]], [[Duan-Lu Zhou]], [[Xiao-Gang Wen]]: 

  *[[Quantum Information Meets Quantum Matter]] -- From Quantum Entanglement to Topological Phases of Many-Body Systems*, Quantum Science and Technology (QST), Springer (2019) $[$[arXiv:1508.02595](https://arxiv.org/abs/1508.02595), [doi:10.1007/978-1-4939-9084-9](https://doi.org/10.1007/978-1-4939-9084-9)$]$


* [[Tudor D. Stanescu]], Part II of: *Introduction to Topological Quantum Matter & Quantum Computation*, CRC Press 2020 ([ISBN:9780367574116](https://www.routledge.com/Introduction-to-Topological-Quantum-Matter--Quantum-Computation/Stanescu/p/book/9780367574116)) 

Review and survey:


* Shou-cheng Zhang, _Viewpoint: Topological states of quantum matter_,  APS Physics 1, 6 (2008) [doi:10.1103/Physics.1.6](http://dx.doi.org/10.1103/Physics.1.6)

* [[Ching-Kai Chiu]], [[Jeffrey C.Y. Teo]], [[Andreas P. Schnyder]] [[Shinsei Ryu]], *Classification of topological quantum matter with symmetries*, Rev. Mod. Phys. **88** 035005 (2016) $[$[arXiv:1505.03535](https://arxiv.org/abs/1505.03535), [doi:10.1103/RevModPhys.88.035005](https://doi.org/10.1103/RevModPhys.88.035005)$]$

* Vishal Bhardwaj, Ratnamala Chatterjee, *Topological Materials -- New Quantum Phases of Matter*, Resonance **25** (2020) 431–441  ([doi:10.1007/s12045-020-0955-5](https://doi.org/10.1007/s12045-020-0955-5), [pdf](https://www.ias.ac.in/article/fulltext/reso/025/03/0431-0441))

* [[Jérôme Cayssol]], [[Jean-Noël Fuchs]], *Topological and geometrical aspects of band theory*, J. Phys. Mater. **4** (2021) 034007 ([arXiv:2012.11941](https://arxiv.org/abs/2012.11941), [doi:10.1088/2515-7639/abf0b5](https://doi.org/10.1088/2515-7639/abf0b5))

* Delft Topology Course, *Online course on topology in condensed matter* (2015-) $[$[topocondmat.org](https://topocondmat.org)$]$


* [[Tanmoy Das]], *A pedagogic review on designing model topological insulators*, Journal of the Indian Institute of Science **96** 77-106 (2016) $[$[arXiv:1604.07546](https://arxiv.org/abs/1604.07546), [ISSN:0970-4140](http://journal.library.iisc.ernet.in/index.php/iisc/article/view/4606)$]$


* {#WangZhang17} Jing Wang, [[Shou-Cheng Zhang]], *Topological states of condensed matter*, Nature Materials **16** (2017) 1062–1067 &lbrack;[doi:10.1038/nmat5012](https://doi.org/10.1038/nmat5012)&rbrack;
   


* [[Charles Zhaoxi Xiong]], *Classification and Construction of Topological Phases of Quantum Matter* &lbrack;[arXiv:1906.02892](https://arxiv.org/abs/1906.02892)&rbrack;

* [[Muhammad Ilyas]], *Quantum Field Theories, Topological Materials, and Topological Quantum Computing* &lbrack;[arXiv:2208.09707](https://arxiv.org/abs/2208.09707)&rbrack;

In view of (fabrication of) [[quantum materials]]:

* Kang L. Wang, Yingying Wu, Christopher Eckberg, Gen Yin, Quanjun Pan: *Topological quantum materials*, MRS Bulletin **45** (2020) 373–379 &lbrack;[doi:10.1557/mrs.2020.122](https://doi.org/10.1557/mrs.2020.122)&rbrack;

* Nitesh Kumar, Satya N. Guin, Kaustuv, Manna, Chandra Shekhar, Claudia Felser: *Topological Quantum Materials from the Viewpoint of Chemistry*, Chemical Reviews **121** 5 (2020) &lbrack;[doi:10.1021/acs.chemrev.0c00732](https://pubs.acs.org/doi/full/10.1021/acs.chemrev.0c00732)&rbrack;


* Junjie Wu, Ying Zhang, Bin Xiang: *Synthesis, properties, and applications of topological quantum materials*, JUSTC **53** 10 (2023) 1002 &lbrack;[doi:10.52396/JUSTC-2023-0024](https://doi.org/10.52396/JUSTC-2023-0024)&rbrack;


Discussion with emphasis of the role of [[quantum anomalies]]:

* [[Jürg Fröhlich]], *Gauge Invariance and Anomalies in Condensed Matter Physics*, Journal of Mathematical Physics &lbrack;[arXiv:2303.14741](https://arxiv.org/abs/2303.14741)&rbrack;


See also:

* Wikipedia, *[Topological insulator](http://en.wikipedia.org/wiki/Topological_insulator)* 

* Wikipedia, *[Topological order](http://en.wikipedia.org/wiki/Topological_order)*

* [[Xiao-Gang Wen]], _Topological Orders and Edge Excitations in FQH States_, Advances in Physics 44, 405 (1995). [cond-mat/9506066](http://arxiv.org/abs/cond-mat/9506066). (for topological order)

* [[Chetan Nayak]], [[Steven H. Simon]], [[Ady Stern]], [[Michael Freedman|M. Freedman]], [[Sankar Das Sarma]], _Non-Abelian anyons and topological quantum computation_, Rev Mod Phys __80__:3 (Aug 2008) 1083&#8211;1159 [MR2009g:81041](http://www.ams.org/mathscinet-getitem?mr=2443722) [doi](http://dx.doi.org/10.1103/RevModPhys.80.1083) (for topological order)

* [M. Z. Hasan](http://www.princeton.edu/physics/people/display_person.xml?netid=mzhasan), C. L. Kane, _Topological insulators_, Reviews of Modern Physics __82__ (4): 3045 (2010) [arXiv:1002.3895](http://arxiv.org/abs/1002.3895) [doi](http://dx.doi.org/10.1103%2FRevModPhys.82.3045) (for topological insulator)

* C. L. Kane, _An insulator with a twist_, Nature physics __4__, May 2008, [pdf](http://www.physics.upenn.edu/~kane/pubs/p59.pdf) (for topological insulator)

* Class for Physics of the Royal Swedish Academy of Sciences, _Topological phase transitions and topological phases of matter_, Scientific Background on the Nobel Prize in Physics 2016, (2+)26 pages, [pdf](http://www.nobelprize.org/nobel_prizes/physics/laureates/2016/advanced-physicsprize2016.pdf)

In the context of [[topological quantum computation]]:

* [[Eric Rowell]], [[Zhenghan Wang]], Section 4 of: _Mathematics of Topological Quantum Computing_, Bull. Amer. Math. Soc. 55 (2018), 183-238 ([arXiv:1705.06206](https://arxiv.org/abs/1705.06206), [doi:10.1090/bull/1605](https://doi.org/10.1090/bull/1605))

In the context of [[chemistry]]:

* Bradlyn et al. *Topological quantum chemistry*, Nature **547** (2017) 298–305 &lbrack;[doi:10.1038/nature23268](https://doi.org/10.1038/nature23268)&rbrack;



### Early discovery articles

* [[Xiao-Gang Wen]], Qian Niu,  [_Ground state degeneracy of the FQH states in presence of random potential and on high genus Riemann surfaces_](http://dao.mit.edu/~wen/pub/topWN.pdf), Phys. Rev. B41, 9377 (1990) (for topological order described by [[TQFT]])
* E. Keski-Vakkuri, [[Xiao-Gang Wen]], [Ground state structure of hierarchical QH states on torus and modular transformation](http://dao.mit.edu/~wen/pub/kw.pdf)
Int. J. Mod. Phys. B7, 4227 (1993). (for topological order described by [[TQFT]]) 
* Liang Fu, C. L. Kane, _Topological insulators with inversion symmetry_, Physical Review B 76 (4): 045302. [arXiv:cond-mat/0611341](http://arxiv.org/abs/cond-mat/0611341) [doi](http://dx.doi.org/10.1103%2FPhysRevB.76.045302); _Superconducting proximity effect and Majorana fermions at the surface of a topological insulator_, Phys. Rev. Lett. __100__: 096407, [arXiv:0707.1692](http://arxiv.org/abs/0707.1692) [doi](http://dx.doi.org/10.1103%2FPhysRevLett.100.096407) (for topological insulator, a special case of SPT states)
* B. Andrei Bernevig, Taylor L. Hughes, Shou-Cheng Zhang, _Quantum spin Hall effect and topological phase transition in HgTe quantum wells_, Science 15 December 2006: __314__, n. 5806, pp. 1757-1761 [doi](http://dx.doi.org/10.1126/science.1133734) (for topological insulator, a special case of SPT states)
 
### Classification and symmetries

* [[Michael Levin]], [[Xiao-Gang Wen]], _String-net condensation: A physical mechanism for topological phases_, Phys. Rev. B, 71, 045110 (2005). (uses unitary [[fusion category]] to classify 2+1D topological order with gapped boundary)

* [[Alexei Kitaev]], _Periodic table for topological insulators and superconductors_, Proc. L.D.Landau Memorial Conf. "Advances in Theor. Physics", June 22-26, 2008, Chernogolovka, Russia, [arxiv/0901.2686](http://arxiv.org/abs/0901.2686) (uses [[K-homology]], [[Bott periodicity]] etc. to classify free fermion gapped phases with symmetry)

* Xie Chen, Zheng-Cheng Gu, Zheng-Xin Liu, Xiao-Gang Wen, _Symmetry protected topological orders and the group cohomology of their symmetry group_, [arXiv:1106.4772](http://arxiv.org/abs/1106.4772); A short version in Science __338__, 1604-1606 (2012) [pdf](http://dao.mit.edu/~wen/pub/dDSPTsht.pdf) (uses [[group cohomology]] of the symmetry group to classify gapped interacting bosonic states  with symmetry and trivial topological order)

* {#FreedMoore12} [[Daniel Freed]], [[Gregory Moore]], _Twisted equivariant matter_, [arxiv/1208.5055](http://arxiv.org/abs/1208.5055) (uses [[equivariant K-theory]] to classify free fermion gapped phases with symmetry)

* [[Juven Wang]], [[Zheng-Cheng Gu]], [[Xiao-Gang Wen]], _Field theory representation of gauge-gravity symmetry-protected topological invariants, group cohomology and beyond_, Phys. Rev. Lett. **114** (2015) 031601 &lbrack;[arxiv:1405.7689](https://arxiv.org/abs/1405.7689), [doi:10.1103/PhysRevLett.114.031601](http://journals.aps.org/prl/abstract/10.1103/PhysRevLett.114.031601)&rbrack;

* {#Freed14} [[Daniel Freed]], _Short-range entanglement and invertible field theories_ ([arXiv:1406.7278](http://arxiv.org/abs/1406.7278))

* [[Guo Chuan Thiang]], _On the K-theoretic classification of topological phases of matter_ &lbrack;[arXiv:1406.7366](http://arxiv.org/abs/1406.7366)&rbrack;

* [[Edward Witten]], _Fermion path integrals and topological phases_, [arxiv/1508.04715](http://arxiv.org/abs/1508.04715)

* Ping Ye, _(3+1)d anomalous twisted gauge theories with global symmetry_, [arxiv/1610.08645](https://arxiv.org/abs/1610.08645)

Classification of [[topological phases of matter]] via [[tensor network states]]:

* C. Wille, O. Buerschaper, [[Jens Eisert]], _Fermionic topological quantum states as tensor networks_, Phys. Rev. B 95, 245127 (2017) ([arXiv:1609.02574](https://arxiv.org/abs/1609.02574))

* Andreas Bauer, [[Jens Eisert]], Carolin Wille, _Towards a mathematical formalism for classifying phases of matter_ ([arXiv:1903.05413](https://arxiv.org/abs/1903.05413))


[[!include topological phases of matter via K-theory -- references]]


### Interacting topological phases
 {#ReferencesInteractingTopologicalPhases}

There is comparatively little discussion of the classification of topological phases of matter where the elementary excitations cannot be approximated as being non-interacting with each other.

Strong interaction is thought to be necessary for [[topological order]], see [there](topological+order#ReferencesLongRangeEntanglementRelationToStrongInteraction) for references on this point.

Discussion for the example of the [[Kitaev spin chain]]:

* [[Lukasz Fidkowski]], [[Alexei Kitaev]], *The effects of interactions on the topological classification of free fermion systems*, Phys. Rev. B **81** (2010) 134509  &lbrack;[arXiv:0904.2197](https://arxiv.org/abs/0904.2197), [doi:10.1103/PhysRevB.81.134509](https://doi.org/10.1103/PhysRevB.81.134509)&rbrack;

An overview:

* [[Jason Alicea]], [[Matthew Fisher]], [[Marcel Franz]], [[Yong-Baek Kim]],  *Strongly Interacting Topological Phases*, report on Banff workshop [15w5051](http://www.birs.ca/events/2015/5-day-workshops/15w5051) (2015) &lbrack;[pdf](https://www.birs.ca/workshops/2015/15w5051/report15w5051.pdf), [[AliceaEtAl-InteractingTopPhases.pdf:file]]&rbrack;

A proposal for the generalization of the [[K-theory classification of topological phases]] to interacting systems

* [Sati & Schreiber 2023](#SatiSchreiber23).



### Other articles

* N. Read, Subir Sachdev, _Large-N expansion for frustrated quantum antiferromagnets_, Phys. Rev. Lett. 66 1773 (1991)

* [[Xiao-Gang Wen]], _Mean Field Theory of Spin Liquid States with Finite Energy Gap and Topological orders_, Phys. Rev. B 44 2664 (1991).

* Alexei Yu. Kitaev, _Fault-tolerant quantum computation by anyons_, Annals of Physics __303__:1, January 2003; _Anyons in an exactly solved model and beyond_, Annals of Physics __321__:1, January 2006

* A. Kitaev, C. Laumann, _Topological phases and quantum computation_, [arXiv/0904.2771](http://arxiv.org/abs/0904.2771)

* Alexei Kitaev, John Preskill, _Topological entanglement entropy_, Phys. Rev. Lett. __96__, 110404 (2006)

* M. Levin, X-G. Wen, _Detecting topological order in a ground state wave function_, Phys. Rev. Letts.,96(11), 110405, (2006)

* Jan Carl Budich, Bj&#246;rn Trauzettel, _From the adiabatic theorem of quantum mechanics to topological states of matter_, physica status solidi (RRL) 7, 109 (2013) [arXiv:1210.6672](http://arxiv.org/abs/1210.6672)

* [[Kumar S. Gupta]], Amilcar Queiroz, _Anomalies and renormalization of impure states in quantum theories_, Modern Physics Letters __A29__ 13 (2014) &lbrack;[arxiv/1306.5570](http://arxiv.org/abs/1306.5570) [doi:10.1142/S0217732314500643](http://dx.doi.org/10.1142/S0217732314500643)&rbrack;

* Yosuke Kubota, _Controlled topological phases and bulk-edge correspondence_, [arxiv/1511.05314](http://arxiv.org/abs/1511.05314)
 
Speculations on topological phases relevant in the [[standard model of particle physics]]:

* {#Wang21} [[Juven Wang]], *Ultra Unification*, Phys. Rev. D **103**  (2021) 105024 &lbrack;[arXiv:2012.15860](https://arxiv.org/abs/2012.15860), [doi:10.1103/PhysRevD.103.105024](https://doi.org/10.1103/PhysRevD.103.105024)&rbrack;

Via [[higher gauge theory|higher]] [[lattice gauge theory]]:

* [[Joe Huxford]], *The higher lattice gauge theory model for topological phases of matter*, PhD thesis, Oxford (2022) &lbrack;[uuid:e789bf29-179b-4b79-9168-605bf8c035ba](https://ora.ox.ac.uk/objects/uuid:e789bf29-179b-4b79-9168-605bf8c035ba), [pdf](https://ora.ox.ac.uk/objects/uuid:e789bf29-179b-4b79-9168-605bf8c035ba/files/ddj52w5202)&rbrack;

* [[Joe Huxford]], [[Steven H. Simon]], *Excitations in the Higher Lattice Gauge Theory Model for Topological Phases I: Overview* &lbrack;[arXiv:2202.08294](https://arxiv.org/abs/2202.08294)&rbrack;



### Research groups

* Univ. of Maryland, [joint quantum institute](http://jqi.umd.edu/research/topological-matter)
* [Topology and correlation in condensed matter](http://tccm.pks.mpg.de) (Germany)
* [Center for topological matter](https://sites.google.com/site/ctmsrc) (Korea)
* [Microsoft Research Station Q](http://research.microsoft.com/en-us/labs/stationq) (KITP, Santa Barbara)

### Conference and seminar cycles

* Markus Garst, Achim Rosch, [[Simon Trebst]]: *[Topological states of matter](http://www.thp.uni-koeln.de/trebst/Lectures/2012-TopoSeminar.html)*

* Simons Center: *Topological Phases of Matter*, June 10-14, 2013 &lbrack;[scgp:3464](http://scgp.stonybrook.edu/archives/3464)&rbrack;

* [[Alexei Kitaev]], _On the classification of short-range entangled states_, [video](http://scgp.stonybrook.edu/archives/7874)

* CECAM 2013: *Topological Phases in Condensed Matter and Cold Atom Systems: towards quantum computations* &lbrack;[webpage](http://www.cecam.org/workshop-867.html)&rbrack;


[[!redirects topological phases of matter]]

[[!redirects topological phase]]
[[!redirects topological phases]]

[[!redirects topological state of matter]]
[[!redirects topological states of matter]]

[[!redirects topological matter]]

[[!redirects bulk-boundary correspondence]]
[[!redirects bulk-boundary correspondences]]


