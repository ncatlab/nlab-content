

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
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[condensed matter physics]], a *semi-metal* is a [[crystal|crystalline]] material whose [[electronic band structure]] is such that there is a sizeable gap between the [[valence band]] and the [[conduction band]] (as for an [[insulator]]) *except* over a [[submanifold]] of "nodal loci" inside the [[Brillouin torus]] which is of [[positive number|positive]] [[codimension]] $\geq 2$. 

This terminology, which was established in the early 2000s, is meant to follow the  older terminology *[[semiconductor]]*, which refers to the case where there is globally a gap between valence and conduction band, but just a small one. Notice that a global and large gap corresponds to an [[insulator]], while the absence of a gap, hence the broad overlap of valence and conductions band, corresponds to a [[metal]]. Therefore a semi-metal behaves like an [[insulator]] for the bulk of its excitation modes, like a [[semiconductor]] for excitations close to the nodal loci, and almost like a [[metal]] for excitations right at the nodal loci; whence the terminology.

<center>
<img src="https://ncatlab.org/nlab/files/SemiMetalBandStructure-20220405.jpg" width="400">
(graphics from [[schreiber:Topological Quantum Computation in TED-K|SS 22]])
</center>

If the gap closure happens over an isolated point, one speaks of a *nodal point* proper, or more specifically of a *Dirac point* or *Weyl point*, indicating the "degeneracy" (multiplicity) of the [[energy]] [[eigenstates]] at the point (2 for Weyl, 4 for Dirac, see [below](#MassTerms)). If the gap closes over a 1-dimensional manifold (a [[curve]] or a [[circle]]) one speaks of a *nodal line*. 

Due to the gap on (a [[neighbourhood retract]] of) the [[complement]] of the nodal points/lines inside the [[Brillouin torus]], the [[Berry connection]] is well-defined away from the nodal loci, and it tends to be [[flat connection|flat]] in suitable hyperplanes there. It's [[holonomy]] around [[codimension]]=2 nodal loci (ie. around nodal lines in 3d materials and nodal points in effectively 2d materials such as [[graphene]], see also at *[[defect brane]]*) -- known as a *[[Berry phase]]* -- is then a property of the nodal locus alone, and to be interpreted as a measure for the "topological protection" of the gap over the nodal loci (e.g. [FWDF 16, II.B](#FWDF16), [Vanderbilt 18, 5.5.2](#Vanderbilt18)): Under [[quantum adiabatic theorem|adiabatic]] deformations of the material that do not excite modes above the gap, these nodal points may move and merge or split, but their total topological charge cannot change.

Therefore semi-metals with such non-trivial Berry phases are examples of [[topological phases of matter]], and are sometimes called *topological semi-metals*, for emphasis. In fact, if the topological charges of the nodal loci in a semi-metal do happen to be trivial, then it is (in the deformation class of) a fully gapped [[insulator]] and may then be a *[[topological insulator]]* (if the [[twisted equivariant K-theory|twisted equivariant]] [[topological K-theory]] class of its [[valence bundle]] is non-trivial).


## Properties

### Phase decay via mass terms
 {#MassTerms}

Near nodal points in the Brillouin torus of a semi-metal, the [[dispersion 
relation]] $k \mapsto E(
k)$ exhibited by the [[energy bands]] is thought to be approximated by that of a massless [[Dirac equation|Dirac equation]]/[[Weyl spinor|Weyl equation]], whence the terminology *Dirac point* or *Weyl point*.

When the material's parameters can be and are [[quantum adiabatic theorem|adiabatically]] tuned such that this [[dispersion relation]] turns into a *massive* [[Dirac equation]], then the band gap at the former nodal crossing will "open up" in proportion to the [[coefficient]] $m$ of the effective *[[mass term]]* $m \gamma_0$ in the Dirac equation. If this happens to all nodal points (while keeping the band gap open everywhere else), one expects that the topological semi-metal phase decays into a [[topological insulator]]-phase.


A necessary condition for such a *[[mass term]]* to exist at all is that a further [[Clifford algebra|Clifford generator]] $\gamma_0$ is represented on the Bloch-Hilbert space of electrons such that it skew-commutes with all [[Feynman slash notation|Clifford momenta]] $k\!\!\!/$ (e.g. [Schnyder 18, Sec. II.A](#Schnyder18), [Schnyder 20, Sec. 2.1](#Schnyder20), see also [Freed & Hopkins 21, around Lem. 9.55](#FreedHopkins21)). 

\begin{imagefromfile}
    "file_name": "MassTermsForSemiMetalNodalPoints-220517.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(graphics from [SS22](#SS22))"
\end{imagefromfile}

By [[Karoubi K-theory|Karoubi/Atiyah-Singer-type theorems]], such gap-opening mass terms are expected to again be classified by topological K-theory groups ([Chiu & Schnyder 14, Sec. A.2](#ChiuSchnyder14), reviewed in [Schnyder 18, Sec. II.A](#Schnyder18), [Schnyder 20, Sec. 2.1](#Schnyder20), following [Morimoto & Furusaki 13, Sec. V](#MorimotoFurusaki13), [CTSR 15, Sec. III.C](#CTSR15)).


Beware: 

1. This means that the topological *semi-metal*-phase must be classified in a group *modulo* the group of [[mass terms]] (cf. [Freed & Hopkins 21, Thm. 9.63](#FreedHopkins21)). The K-group of mass terms itself at best classifies aspects of the [[topological insulator]]-phase that the semi-metal phase may decay to.

1. The argument about single [[mass terms]] in a K-theory group of a point ignores the global topology of the valence bundle.

   This is manifest already in the canonical example of the [[Haldane model]], where for *constant* mass terms (as usually understood) the total topological charge of all nodal points combined is constrained to vanish.


## Examples

The archetypical and original example of a semi-metal is *[[graphene]]*, where the gap closes over two [[Dirac points]]. (Or almost: a tiny [[spin-orbit coupling]] in graphene actually produces a tiny gap even at the would-be Dirac points, which however tends to be too small to be visible in practice. But if one will or would analyze graphene with an accuracy that does resolve this tiny gap-opening, then graphene will or would appear as a [[topological insulator]] instead of a semi-metal.)

After the synthesis of graphene, which is an effectively 2-dimensional material (an atomic mono-layer) much attention has shifted to the synthesis and understanding of 3-dimensional semi-metals.

## Related concepts

* [[topological insulator]]

* [[photonic semimetal]], [[phononic semimetal]]




## References

### General

Review:

* [[Anton A. Burkov]], *Topological semimetals*, Nature Materials **15** (2016) 1145–1148 &lbrack;[doi:10.1038/nmat4788](https://doi.org/10.1038/nmat4788), [arXiv:1610.07866](https://arxiv.org/abs/1610.07866)&rbrack;

* Jinyu Zou, Zhuoran He, Gang Xu: *The study of magnetic topological semimetals by first principles calculations*, npj Computational Materials **5** 96 (2019) &lbrack;[doi:10.1038/s41524-019-0237-5](https://doi.org/10.1038/s41524-019-0237-5)&rbrack;

* [[Alexander S. Sergeev]], section 10 of: *Topological insulators and geometry of vector bundles*, SciPost Physics Lecture Notes **67** (2023) &lbrack;[arXiv:2011.05004](https://arxiv.org/abs/2011.05004), [doi:10.21468/SciPostPhysLectNotes.67](https://doi.org/10.21468/SciPostPhysLectNotes.67)&rbrack;


* [[Guo Chuan Thiang]]: *Topological Semimetals*, [[Encyclopedia of Mathematical Physics 2nd ed]] (2024) &lbrack;[arXiv:2407.12692](https://arxiv.org/abs/2407.12692)&rbrack;


General monographs:

* [[Tomáš Bzdušek]], *Symmetry and topology of nodal semimetals*, ETH (2017) &lbrack;[doi:10.3929/ethz-b-000216959](https://doi.org/10.3929/ethz-b-000216959)&rbrack;

* {#Vanderbilt18} [[David Vanderbilt]],  Section 5 of: *Berry Phases in Electronic Structure Theory -- Electric Polarization, Orbital Magnetization and Topological Insulators*, Cambridge University Press (2018) ([doi:10.1017/9781316662205](https://doi.org/10.1017/9781316662205))

Review with emphasis on [mass terms](#MassTerms):

* {#Schnyder18} [[Andreas P. Schnyder]], *Accidental and symmetry-enforced band crossings in topological semimetals*, lecture notes (2018) &lbrack;[pdf](https://www.fkf.mpg.de/6431357/topo_lecture_notes_schnyder_TMS18.pdf), [[Schnyder-Semimetals-2018.pdf:file]]&rbrack;

* {#Schnyder20} [[Andreas P. Schnyder]], *Topological semimetals*, lecture notes (2020) &lbrack;[pdf](https://www.fkf.mpg.de/7143520/topological_semimetals.pdf), [[Schnyder-Semimetals-2020.pdf:file]]&rbrack;


For references on *[[graphene]]* see also there.

Discussion focusing on 3-dimensional semi-metals with nodal lines:

* [[Junyeong Ahn]], Dongwook Kim, Youngkuk Kim, Bohm-Jung Yang: *Band Topology and Linking Structure of Nodal Line Semimetals with $\mathbb{Z}_2$ Monopole Charges*, Phys. Rev. Lett. **121**  (2018) 106403 &lbrack;[arXiv:1803.11416](https://arxiv.org/abs/1803.11416), [doi:10.1103/PhysRevLett.121.106403](https://doi.org/10.1103/PhysRevLett.121.106403)&rbrack;

* [[Anton A. Burkov]], M. D. Hook, Leon Balents:  *Topological nodal semimetals*, Phys. Rev. B **84** (2011) 235126 &lbrack;[arXiv:1110.1089](https://arxiv.org/abs/1110.1089), [doi:10.1103/PhysRevB.84.235126](https://doi.org/10.1103/PhysRevB.84.235126)&rbrack;

* [[Ari M. Turner]], [[Ashvin Vishwanath]], Part I of: *Beyond Band Insulators: Topology of Semi-metals and Interacting Phases*, in: *Topological Insulators*, Contemporary Concepts of Condensed Matter Science **6** (2013) 293-324 &lbrack;[arXiv:1301.0330](https://arxiv.org/abs/1301.0330), [ISBN:978-0-444-63314-9](https://www.sciencedirect.com/bookseries/contemporary-concepts-of-condensed-matter-science/vol/6/suppl/C)&rbrack;

* Bohm-Jung Yang, Naoto Nagaosa, *Classification of stable three-dimensional Dirac semimetals with nontrivial topology*, Nature Communications **5** (2014) 4898  &lbrack;[doi:10.1038/ncomms5898](https://doi.org/10.1038/ncomms5898)&rbrack;)

* Da-Shuai Ma, Jianhui Zhou, Botao Fu, Zhi-Ming Yu, Cheng-Cheng Liu, Yugui Yao: *Mirror Protected Multiple Nodal Line Semimetals and Material Realization*, Phys. Rev. B **98** 201104 (2018) &lbrack;[arXiv:1804.06960](https://arxiv.org/abs/1804.06960), [doi:10.1103/PhysRevB.98.201104](https://doi.org/10.1103/PhysRevB.98.201104)&rbrack;

* N. P. Armitage, [[Eugene Mele]], [[Ashvin Vishwanath]], *Weyl and Dirac semimetals in three-dimensional solids*, Rev. Mod. Phys. **90** 015001 (2018) &lbrack;[doi:10.1103/RevModPhys.90.015001](https://doi.org/10.1103/RevModPhys.90.015001)&rbrack;

* Jiaheng Li, Zetao Zhang, Chong Wang, Huaqing Huang, Bing-Lin Gu, Wenhui Duan,  *Topological semimetals from the perspective of first-principles calculations*, Journal of Applied Physics **128** 191101 (2020) ([doi:10.1063/5.0025396]( https://doi.org/10.1063/5.0025396))

* Faruk Abdulla, Ganpathy Murthy, Ankur Das, *Stable nodal line semimetals in the chiral classes in three dimensions*  &lbrack;[arXiv:2401.02966](https://arxiv.org/abs/2401.02966)&rbrack;

Discussion of the $\mathbb{Z}/2$-valued [[Berry phases]] around [[codimension]]=2 nodal loci in $P I$-symmetric (time-reversal +  inversion invariant)  semi-metals:

* Dan-Wei Zhang, Y. X. Zhao, Rui-Bin Liu, Zheng-Yuan Xue, Shi-Liang Zhu, Z. D. Wang, *Quantum simulation of exotic PT-invariant topological nodal loop bands with ultracold atoms in an optical lattice*, Phys. Rev. A **93** (2016) 043617  ([arXiv:1601.00371](https://arxiv.org/abs/1601.00371), [doi:10.1103/PhysRevA.93.043617](https://doi.org/10.1103/PhysRevA.93.043617))
  > (see sec II.A, these authors stand out as mentioning the relevant [[KO-theory]])

* {#FWDF16} Chen Fang, Hongming Weng, Xi Dai, Zhong Fang, *Topological nodal line semimetals*, Chinese Phys. B **25** (2016) 117106 &lbrack;[arXiv:1609.05414](https://arxiv.org/abs/1609.05414), [doi:10.1088/1674-1056/25/11/117106](https://doi.org/10.1088/1674-1056/25/11/117106)&rbrack;
  > (see sec II.B)

* [Vanderbilt 18, 5.5.2](#Vanderbilt18)


More mathematical discussion of the case of [[Chern semi-metals]]:

* {#MathaiThiang17a} [[Varghese Mathai]], [[Guo Chuan Thiang]], *Global topology of Weyl semimetals and Fermi arcs*, J. Phys. A: Math. Theor. **50** (2017) 11LT01 &lbrack;[arXiv:1607.02242](https://arxiv.org/abs/1607.02242),  [doi:10.1088/1751-8121/aa59b2](https://doi.org/10.1088/1751-8121/aa59b2)&rbrack;

* {#MathaiThiang17b} [[Varghese Mathai]], [[Guo Chuan Thiang]], *Differential Topology of Semimetals*, Commun. Math. Phys. **355** (2017) 561–602 &lbrack;[arXiv:1611.08961](https://arxiv.org/abs/1611.08961), [doi:10.1007/s00220-017-2965-z](https://doi.org/10.1007/s00220-017-2965-z)&rbrack;


Discussion of (classification of) Dirac/Weyl mass terms:

* {#ChiuSchnyder14} [[Ching-Kai Chiu]], [[Andreas P. Schnyder]], Section A.2 of: *Classification of reflection-symmetry-protected topological semimetals and nodal superconductors*, Phys. Rev. B **90** 205136 (2014) $[$[doi:10.1103/PhysRevB.90.205136](https://doi.org/10.1103/PhysRevB.90.205136)$]$

following:

* {#MorimotoFurusaki13} Takahiro Morimoto and Akira Furusaki, Sec. V of: *Topological classification with additional symmetries from Clifford algebras*, Phys. Rev. B **88** (2013) 125129 ([arXiv:1306.2505](https://arxiv.org/abs/1306.2505),  [doi:10.1103/PhysRevB.88.125129](https://doi.org/10.1103/PhysRevB.88.125129))

* {#CTSR15} [[Ching-Kai Chiu]], [[Jeffrey C.Y. Teo]], [[Andreas P. Schnyder]], [[Shinsei Ryu]], Section III.C of *Classification of topological quantum matter with symmetries*, Rev. Mod. Phys. **88** (2016) 035005 ([arXiv:1505.03535](https://arxiv.org/abs/1505.03535), [doi:10.1103/RevModPhys.88.035005](https://doi.org/10.1103/RevModPhys.88.035005))

Pedagogical example:

* {#DelftTopologyCourse} Delft Topology Course team, *[Haldane model, Berry curvature, and Chern number](https://topocondmat.org/w4_haldane/haldane_model.html#first-try)* - [First try](https://topocondmat.org/w4_haldane/haldane_model.html#first-try), [Second try](https://topocondmat.org/w4_haldane/haldane_model.html#second-try)


Related discussion of Dirac mass terms is in:

* {#FreedHopkins21} [[Daniel S. Freed]], [[Michael J. Hopkins]], *Reflection positivity and invertible topological phases*, Geom. Topol. **25** (2021) 1165-1330 &lbrack;[arXiv:1604.06527](https://arxiv.org/abs/1604.06527), [doi:10.2140/gt.2021.25.1165](https://doi.org/10.2140/gt.2021.25.1165)&rbrack;


Lists of actual semi-metals:

* Md. Rakibul Karim Akand. *Catalog of magnetic topological semimetals*, AIP Advances **10** 095222 (2020) &lbrack;[doi:10.1063/5.0020096](https://doi.org/10.1063/5.0020096)&rbrack;

Simulation of Dirac semimetals with [[lattice field theory]]:

* *Lattice field theory simulations of Dirac semimetals*, Annals of Physics **391** (2018) 278-292 &lbrack;[doi:10.1016/j.aop.2018.02.016](https://doi.org/10.1016/j.aop.2018.02.016)&rbrack;

and other numerical calculuations:

* *The study of magnetic topological semimetals by first principles calculations*, npj Computational Materials **5** 96 (2019) &lbrack;[doi:10.1038/s41524-019-0237-5](https://doi.org/10.1038/s41524-019-0237-5)&rbrack;

* *Topological semimetals from the perspective of first-principles calculations*, Journal of Applied Physics **128** (2020) 191101 &lbrack;[doi:10.1063/5.0025396](https://doi.org/10.1063/5.0025396)&rbrack;

{#ReferencesStronglyCoupled} On strongly-coupled topological semimetals:

* [[Koji Hashimoto]], Shunichiro Kinoshita, Keiju Murata, [[Takashi Oka]], *Holographic Floquet states: (I) A strongly coupled Weyl semimetal*, J. High Energ. Phys. **2017** 127 (2017)  &lbrack;[arXiv:1611.03702](https://arxiv.org/abs/1611.03702), <a href="https://doi.org/10.1007/JHEP05(2017)127">doi:10.1007/JHEP05(2017)127</a>&rbrack;

* Diana M Kirschbaum, Monika Lužnik, Gwenvredig Le Roy,  Silke Paschen, *How to identify and characterize strongly correlated topological semimetals*, J. Phys. Mater. **7** (2024) 012003 &lbrack;[doi:10.1088/2515-7639/ad0f30a](https://iopscience.iop.org/article/10.1088/2515-7639/ad0f30), [arXiv:2308.11318](https://arxiv.org/abs/2308.11318)&rbrack;

* Yongjun Ahn, Matteo Baggioli, Yan Liu, Xin-Meng Wu, *Chiral magnetic waves in strongly coupled Weyl semimetals*, J. High Energ. Phys. **2024** 124 (2024) &lbrack;[arXiv:2401.07772](https://arxiv.org/abs/2401.07772), <a href="https://doi.org/10.1007/JHEP03(2024)124">doi:10.1007/JHEP03(2024)124</a>&rbrack;

and relation to [[topological order]]:

* Chong Wang, Lei Gioia, [[Anton A. Burkov]], *Fractional Quantum Hall Effect in Weyl Semimetals*, Phys. Rev. Lett. **124** 096603 (2020) &lbrack;[doi:10.1103/PhysRevLett.124.096603](https://doi.org/10.1103/PhysRevLett.124.096603)&rbrack;

* Manisha Thakurathi, [[Anton A. Burkov]], *Theory of the fractional quantum Hall effect in Weyl semimetals*, Phys. Rev. B **101** 235168 (2020) &lbrack;[doi:10.1103/PhysRevB.101.235168](https://doi.org/10.1103/PhysRevB.101.235168), [arXiv:2005.13545](https://arxiv.org/abs/2005.13545), [arXiv:2005.13545](https://arxiv.org/abs/2005.13545)&rbrack;

  > "while we focused on fully gapped states \[...\] it also makes sense to consider gapless strongly correlated states with the same property. Such states may be accessed easily within the formalism, presented above

* Dan Sehayek, Manisha Thakurathi, [[Anton A. Burkov]], *Charge density waves in Weyl semimetals*, Phys. Rev. B **102** 115159 (2020) &lbrack;[doi:10.1103/PhysRevB.102.115159](https://doi.org/10.1103/PhysRevB.102.115159)&rbrack;

* Jinmin Yi, Xuzhe Ying, Lei Gioia, [[Anton A. Burkov]], *Topological order in interacting semimetals*, Phys. Rev. B **107** 115147 (2023) &lbrack;[arXi:2301.03628](https://arxiv.org/abs/2301.03628), [doi:10.1103/PhysRevB.107.115147](https://doi.org/10.1103/PhysRevB.107.115147)&rbrack;

* Hongshuang Liu, Jiashuo Liang, Taiyu Sun, Liying Wang: *Recent progress in topological semimetal and its realization in Heusler compounds*, Materials Today Physics
**41** (2024) 101343 &lbrack;[doi:10.1016/j.mtphys.2024.101343](https://doi.org/10.1016/j.mtphys.2024.101343)&rbrack;


On Weyl-Kondo semimetals:

* Hsin-Hua Lai, Sarah E. Grefe, Silke Paschen, Qimiao Si, *Weyl–Kondo semimetal in heavy-fermion systems*, PNAS **115** 1 (2017) 93-97 &lbrack;[doi:10.1073/pnas.1715851115](https://doi.org/10.1073/pnas.1715851115)&rbrack;


* Lei Chen, C. Setty, H. Hu et al.: *Topological Semimetal driven by Strong Correlations and Crystalline Symmetry*,  
Nat. Phys. **18** 1341–1346 (2022) &lbrack;[arXiv:2107.10837](https://arxiv.org/abs/2107.10837), [doi:10.1038/s41567-022-01743-4](https://doi.org/10.1038/s41567-022-01743-4)&rbrack

and background on "heavy fermions":

* Norbert Grewe, Frank Steglich, *Heavy fermions*, Chapter 97 in: *Handbook on the Physics and Chemistry of Rare Earths*
**14** (1991) 343-474 \[<a href="https://doi.org/10.1016/S0168-1273(05)80103-5">doi:10.1016/S0168-1273(05)80103-5</a>\]



### Holographic description 

On holographic descriptions of [[topological semimetals]] via the [[AdS-CMT correspondence]]:

* [[Karl Landsteiner]], [[Yan Liu]], *The holographic Weyl semi-metal*, Physics Letters B **753** (2016) 453-457 &lbrack;[arXiv:1505.04772](https://arxiv.org/abs/1505.04772), [doi:10.1016/j.physletb.2015.12.052](https://doi.org/10.1016/j.physletb.2015.12.052)&rbrack;

* [[Karl Landsteiner]], [[Yan Liu]], [[Ya-Wen Sun]], *Quantum phase transition between a topological and a trivial semimetal from holography*, Phys. Rev. Lett. **116** 081602 (2016) &lbrack;[arXiv:1511.05505](https://arxiv.org/abs/1511.05505), [doi:10.1103/PhysRevLett.116.081602](https://doi.org/10.1103/PhysRevLett.116.081602)&rbrack;

* Ling-Long Gao, [[Yan Liu]], Hong-Da Lyu, *Black hole interiors in holographic topological semimetals* &lbrack;[arXiv:2301.01468](https://arxiv.org/abs/2301.01468)&rbrack;

* Masataka Matsumoto, Mirmani Mirjalali, Ali Vahedi, *Non-Linear Dynamics and Critical Phenomena in the Holographic Landscape of Weyl Semimetals* &lbrack;[arXiv:2405.06484](https://arxiv.org/abs/2405.06484)&rbrack;

* Nishal Rai, Karl Landsteiner: *Hydrodynamic Modes of Holographic Weyl Semimetals* &lbrack;[arXiv:2408.06192](https://arxiv.org/abs/2408.06192)&rbrack;

Review:

* [[Karl Landsteiner]], [[Yan Liu]], [[Ya-Wen Sun]], *Holographic Topological Semimetals*,  Sci. China Phys. Mech. Astron. **63** 250001 (2020) &lbrack;[arXiv:1911.07978](https://arxiv.org/abs/1911.07978), [doi:10.1007/s11433-019-1477-7](https://doi.org/10.1007/s11433-019-1477-7)&rbrack;


Some of the above material is taken from 

* {#SS22} [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Topological Quantum Computation in TED-K]]*, [PlanQC **2022**](https://icfp22.sigplan.org/home/planqc-2022) [**33**](https://planqc2022.hotcrp.com/paper/33), (15 Sep 2022) &lbrack;[arXiv:2209.08331](https://arxiv.org/abs/2209.08331), slides: [pdf](/schreiber/files/TQCinTEDK-PlanQC-220905b.pdf), video: [YT](https://www.youtube.com/watch?v=hDwXQVcloB8&feature=emb_logo)&rbrack;




[[!include anyonic braiding in momentum space -- references]]








[[!redirects semi-metals]]


[[!redirects semimetal]]
[[!redirects semimetals]]

[[!redirects topological semi-metal]]
[[!redirects topological semi-metals]]

[[!redirects topological semimetal]]
[[!redirects topological semimetals]]


[[!redirects Dirac point]]
[[!redirects Dirac points]]

[[!redirects Weyl point]]
[[!redirects Weyl points]]

[[!redirects band node]]
[[!redirects band nodes]]

[[!redirects nodal point]]
[[!redirects nodal points]]

[[!redirects nodal line]]
[[!redirects nodal lines]]



