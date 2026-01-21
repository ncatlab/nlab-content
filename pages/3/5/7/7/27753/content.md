
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Topological physics
+--{: .hide}
[[!include topological physics -- contents]]
=--
=--
=--



\tableofcontents


## Idea

The *quantum anomalous Hall effect* (QAHE) is a joint variant of the [[quantum Hall effect]] and the [[anomalous Hall effect]]: Where a [[quantum Hall effect]] is induced by a strong *external* [[magnetic field]], in the "anomalous" version --- realized in [[crystal|crystalline]] [[topological phases of matter]] called *[[Chern insulators]]* --- the effect of the external magnetic field on the [[electrons]] is instead mimicked by the latter's [[spin-orbit coupling]] in the presence of magnetization, jointly reflected in a non-vanishing [[Berry curvature]] over the [[Brillouin torus]] which now plays the role of the external field's [[flux density]].

In analogy to how the ordinary [[quantum Hall effect]] has a [fractional version](quantum+Hall+effect#IdeaFQHE), there is even a fractional version of the QAHE: the *fractional quantum anomalous Hall effect* (FQAHE).


## Details

\begin{imagefromfile}
    "file_name": "ChangLiuMacDonald2023-Fig1.png",
    "float": "right",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -60,
        "bottom": 20,
        "right": 0, 
        "left": 30
    },
    "caption": "(from [Chang, Liu, MacDonald 2023](#ChangLiuMacDonald23))"
\end{imagefromfile}


> &lbrack;[Chang, Liu & MacDonald 2023  §II.A](#ChangLiuMacDonald23):&rbrack; A common feature of all the QAH systems that are established as of this writing --- magnetically doped [[topological insulator|TI]] films, films of the intrinsic magnetic TI $Mn Bi_2 Te_4$, magic-angle TBG, ABC trilayer [[graphene]] on $h\text{-}BN$, and TMD moir&eacute;s --- is adiabatic connection to a limit in which the band states
close to the Fermi level can be described by 2D massive [[Dirac equations]]. \[...\] The 2D Dirac model is not periodic in momentum and is therefore not a crystal Hamiltonian. When applied to crystalline electronic degrees of freedom, it is intended to apply only in small isolated portions of the Brillouin zone (BZ) with large Berry curvatures \[...\]  the Berry curvature in the 2D Dirac equation is concentrated within a momentum-space area proportional to $(m/\hbar v_D)^2$  (where $v_D \sim v_{D,x} \sim v_{D,y}$), and that it decays as ${\vert \mathbf{k} \vert}^{-3}$ for large ${\vert \mathbf{k} \vert}$. \[...\] Each 2D Dirac Hamiltonian therefore contributes $\pm (e^2/2 h)$ to the Hall conductivity


{#FQAHDetails} Moreover, for fractional quantum Hall systems the [[valence band]]:

* is "almost flat", meaning that its energy gradient with respect to momentum is small, so that the [[kinetic energy]] of electrons is small ("quenched") and the electron-interaction/correlation is dominant

* overlaps the Fermi energy, so that it is only partially (fractionally) filled, with holes at the peaks of the Dirac domes:

\begin{imagefromfile}
    "file_name": "FQAH-BandStructure.png",
    "width": 640,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}



## Related entries

**Types of Hall effects**

* [[Hall effect]], [[anomalous Hall effect]]

* [[quantum Hall effect]], [[quantum anomalous Hall effect]]

* [[quantum spin Hall effect|quantum]]$\;$[[spin Hall effect]]



## References

### Integer QAHE

The theoretical prediction of Hall conductance proportional to the [[first Chern number]] ([[integral|integrated]] [[Berry curvature]]) of the [[valence band]] in a [[topological insulator]]:

* D. J. Thouless, M. Kohmoto, M. P. Nightingale, M. den Nijs: *Quantized Hall Conductance in a Two-Dimensional Periodic Potential*, Phys. Rev. Lett. **49** (1982) 405 &lbrack;[doi:10.1103/PhysRevLett.49.405](https://doi.org/10.1103/PhysRevLett.49.405)&rbrack;


The first theoretical lattice model, which came to be called the *[[Haldane model]]*:

* [[Duncan Haldane]]: *Model for a Quantum Hall Effect without Landau Levels: Condensed-Matter Realization of the "Parity Anomaly"*, Phys. Rev. Lett. **61** (1988) 2015 &lbrack;[doi:10.1103/PhysRevLett.61.2015](https://doi.org/10.1103/PhysRevLett.61.2015)&rbrack;

Experimental realization of QAH systems:

* Cui-Zu Chang et al.: *Experimental Observation of the Quantum Anomalous Hall Effect in a Magnetic Topological Insulator*, Science **340** (2013) 167 &lbrack;[doi:10.1126/science.1234414](https://doi.org/10.1126/science.1234414), [arXiv:1605.08829](https://arxiv.org/abs/1605.08829)&rbrack;

Review:

* Jing Wang, [[Biao Lian]], [[Shou-Cheng Zhang]]: *Quantum anomalous Hall effect in magnetic topological insulators*, Physica Scripta **2015** T164 (2015) 014003 &lbrack;[arXiv:1409.6715](https://arxiv.org/abs/1409.6715), [doi:10.1088/0031-8949/2015/T164/014003](https://doi.org/10.1088/0031-8949/2015/T164/014003)&rbrack;

*  [[Chao-Xing Liu]], [[Shou-Cheng Zhang]], Xiao-Liang Qi: *The Quantum Anomalous Hall Effect: Theory and Experiment*,  Annual Review of Condensed Matter Physics **7** (2016) &lbrack;[arXiv:1508.07106](https://arxiv.org/abs/1508.07106), [doi:10.1146/annurev-conmatphys-031115-011417](https://doi.org/10.1146/annurev-conmatphys-031115-011417)&rbrack;

* {#ChangLiuMacDonald23} Cui-Zu Chang, [[Chao-Xing Liu]], [[Allan H. MacDonald]]: *Colloquium: Quantum anomalous Hall effect*, Rev. Mod. Phys. **95** (2023) 011002  &lbrack;[arXiv:2202.13902](https://arxiv.org/abs/2202.13902), [doi:10.1103/RevModPhys.95.011002](https://doi.org/10.1103/RevModPhys.95.011002)&rbrack;




See also:

* Wikipedia: *[Quantum anomalous Hall effect](https://en.wikipedia.org/wiki/Quantum_anomalous_Hall_effect)*


### Fractional QAHE

#### General

The original theoretical prediction (published back-to-back in the same volume) of the fractional quantum anomalous Hall in fractional Chern insulators:

* {#TangMeiWen11} Evelyn Tang, Jia-Wei Mei, [[Xiao-Gang Wen]]: _High-Temperature Fractional Quantum Hall States_, Phys. Rev. Lett. **106** (2011) 236802 &lbrack;[arXiv:1101.1942](https://arxiv.org/abs/1101.1942), [doi:10.1103/PhysRevLett.106.236802](https://doi.org/10.1103/PhysRevLett.106.236802)&rbrack;

* {#SunGuKatsuraDasSarma11} Kai Sun, [[Zheng-Cheng Gu]], Hosho Katsura, [[Sankar Das Sarma]]: _Nearly Flatbands with Nontrivial Topology_, Phys. Rev. Lett. **106** (2011) 236803 &lbrack;[arXiv:1012.5864](https://arxiv.org/abs/1012.5864), [doi:10.1103/PhysRevLett.106.236803](https://doi.org/10.1103/PhysRevLett.106.236803)&rbrack;

* [[Titus Neupert]], [[Luiz Santos]], [[Claudio Chamon]], [[Christopher Mudry]]: *Fractional quantum Hall states at zero magnetic field*, Phys. Rev. Lett. **106** (2011) 236804  &lbrack;[arXiv:1012.4723](https://arxiv.org/abs/1012.4723), [doi:10.1103/PhysRevLett.106.236804](https://doi.org/10.1103/PhysRevLett.106.236804)&rbrack;

and further early theoretical development:

* [[Siddharth A. Parameswaran]], [[Rahul Roy]], [[Shivaji L. Sondhi]]: *Fractional Quantum Hall Physics in Topological Flat Bands*, Comptes Rendus. Physique, Topological insulators / Isolants topologiques, **14** 9-10 (2013) 816-839 &lbrack;[arXiv:1302.6606](https://arxiv.org/abs/1302.6606), [doi:10.1016/j.crhy.2013.04.003](https://doi.org/10.1016/j.crhy.2013.04.003)&rbrack;
  > "The possibility of stabilizing exotic topological phases outside of a dilution fridge and without a superconducting magnet, and the avenues it opens for further experimental
probes of these phases, is among the primary motivations of the activity in this field"

* [[Rahul Roy]]: *Band geometry of fractional topological insulators*, Phys. Rev. B **90** (2014) 165139 &lbrack;[arXiv:1208.2055](https://arxiv.org/abs/1208.2055), [doi:10.1103/PhysRevB.90.165139](https://doi.org/10.1103/PhysRevB.90.165139)&rbrack;

* [[Nicolas Regnault]], [[B. Andrei Bernevig]]: *Fractional Chern Insulator*, Phys. Rev. X **1** (2011) 021014  &lbrack;[arXiv:1105.4867](https://arxiv.org/abs/1105.4867), [doi:10.1103/PhysRevX.1.021014](https://doi.org/10.1103/PhysRevX.1.021014)&rbrack;

Relation to [[W-infinity algebra]]:

* [[Siddharth A. Parameswaran]], [[Rahul Roy]], [[Shivaji L. Sondhi]]: *Fractional Chern Insulators and the W-Infinity Algebra*, Phys. Rev. B **85**  (2012) 241308(R) &lbrack;[arXiv:1106.4025](https://arxiv.org/abs/1106.4025), [doi:10.1103/PhysRevB.85.241308](https://doi.org/10.1103/PhysRevB.85.241308)&rbrack;

See also:

* Peleg Emanuel, Anna Keselman, Yuval Oreg: *A Unifying Framework for Fractional Chern Insulator Stabilization*, Phys. Rev. B **112** (2025) 235133  &lbrack;[arXiv:2505.07950](https://arxiv.org/abs/2505.07950), [doi:10.1103/9hpw-kz7g](https://doi.org/10.1103/9hpw-kz7g)&rbrack;



Experimental realization of FQAH systems:

* Jiaqi Cai et al.: *Signatures of Fractional Quantum Anomalous Hall States in Twisted $MoTe_2$ Bilayer*, Nature **622** (2023) 63–68 &lbrack;[arXiv:2304.08470](https://arxiv.org/abs/2304.08470), [doi:10.1038/s41586-023-06289-w](https://doi.org/10.1038/s41586-023-06289-w)&rbrack;
  > (in twisted bilayer [molybdenum ditelluride](https://en.wikipedia.org/wiki/Molybdenum_ditelluride), $Mo Te_2$)

* Yihang Zeng et al.: *Thermodynamic evidence of fractional Chern insulator in moiré $MoTe_2$*, Nature **622** (2023) 69–73 &lbrack;[doi:10.1038/s41586-023-06452-3](https://doi.org/10.1038/s41586-023-06452-3)&rbrack;

* Heonjoon Park et al.: *Observation of fractionally quantized anomalous Hall effect*, Nature **622** (2023) 74–79 &lbrack;[doi:10.1038/s41586-023-06536-0](https://doi.org/10.1038/s41586-023-06536-0)&rbrack;

* Boran Zhou, Hui Yang, and Ya-Hui Zhang: *Fractional Quantum Anomalous Hall Effect in Rhombohedral Multilayer Graphene in the Moiréless Limit*, Phys. Rev. Lett. **133** (2024) 206504 &lbrack;[doi:10.1103/PhysRevLett.133.206504](https://doi.org/10.1103/PhysRevLett.133.206504), [arXiv:2311.04217](https://arxiv.org/abs/2311.04217)&rbrack;

* Zhengguang Lu et al.: *Fractional quantum anomalous Hall effect in multilayer graphene*, Nature **626** (2024) 759–764 &lbrack;[doi:10.1038/s41586-023-07010-7](https://doi.org/10.1038/s41586-023-07010-7), [arXiv:2309.17436](https://arxiv.org/abs/2309.17436)&rbrack;

* Jingwei Dong, et al.: *Observation of Integer and Fractional Chern insulators in high Chern number flatbands* &lbrack;[arXiv:2507.09908](https://arxiv.org/abs/2507.09908)&rbrack;

* Naitian Liu et al.: *Diverse high-Chern-number quantum anomalous Hall insulators in twisted rhombohedral graphene* &lbrack;[arXiv:2507.11347](https://arxiv.org/abs/2507.11347)&rbrack;

* Hongyun Zhang et al.: *Moiré enhanced flat band in rhombohedral graphene*, Nat. Mater. (2025) &lbrack;[arXiv:2504.06251](https://arxiv.org/abs/2504.06251), [doi:10.1038/s41563-025-02416-2](https://doi.org/10.1038/s41563-025-02416-2)&rbrack;
     


Review:

* [[Rahul Roy]], [[Shivaji L. Sondhi]]: *Fractional quantum Hall effect without Landau levels*, Physics **4**46  (June 2011) &lbrack;[physics.aps:v4/46](https://physics.aps.org/articles/v4/46)&rbrack;

* {#BergholtzLiu2013} Emil J. Bergholtz, Zhao Liu: *Topological Flat Band Models and Fractional Chern Insulators*, Int. J. Mod. Phys. B **27** (2013) 1330017 &lbrack;[doi:10.1142/S021797921330017X](https://doi.org/10.1142/S021797921330017X), [arXiv:1308.0343](https://arxiv.org/abs/1308.0343)&rbrack;

* [[Titus Neupert]], [[Claudio Chamon]], [[Thomas Iadecola]], [[Luiz H. Santos]], [[Christopher Mudry]]: *Fractional (Chern and topological) insulators* Physica Scripta **2015** (2015) 014005 &lbrack;[arXiv:1410.5828](https://arxiv.org/abs/1410.5828), [doi:10.1088/0031-8949/2015/T164/014005](https://doi.org/10.1088/0031-8949/2015/T164/014005)&rbrack;

* Long Yu et al., *The fractional quantum anomalous Hall effect*, Nature Reviews Materials **9** (2024) 455–459 &lbrack;[doi:10.1038/s41578-024-00694-x](https://doi.org/10.1038/s41578-024-00694-x)&rbrack;

* {#Morales-DuranShiMacDonald24} Nicolás Morales-Durán, Jingtian Shi, [[Allan H. MacDonald]]: *Fractionalized electrons in moiré materials*, Nature Reviews Physics **6** (2024) 349–351 &lbrack;[doi:10.1038/s42254-024-00718-z](https://doi.org/10.1038/s42254-024-00718-z)&rbrack;

* Jian Zhao et al.: *Exploring the Fractional Quantum Anomalous Hall Effect in Moiré Materials: Advances and Future Perspectives*, ACS Nano (2025) &lbrack;[doi:10.1021/acsnano.5c01598](https://doi.org/10.1021/acsnano.5c01598)&rbrack;

See also:

* Wikipedia: *[Fractional Chern insulator](https://en.wikipedia.org/wiki/Fractional_Chern_insulator)*

Further discussion:

* Valentin Crépel, Liang Fu: *Anomalous Hall metal and fractional Chern insulator in twisted transition metal dichalcogenides*, Phys. Rev. B **107** (2023) L201109 &lbrack;[arXiv:2207.08895](https://arxiv.org/abs/2207.08895), [doi:10.1103/PhysRevB.107.L201109](https://doi.org/10.1103/PhysRevB.107.L201109)&rbrack;

* Gal Shavit, Yuval Oreg: *Quantum Geometry and Stabilization of Fractional Chern Insulators Far from the Ideal Limit*, Phys. Rev. Lett. **133** (2024) 156504 &lbrack;[doi:10.1103/PhysRevLett.133.156504](https://doi.org/10.1103/PhysRevLett.133.156504), [arXiv:2405.09627](https://arxiv.org/abs/2405.09627)&rbrack;

* [[Nicolas Regnault]] et al.: *Fractional topological states in rhombohedral multilayer graphene modulated by kagome superlattice* &lbrack;[arXiv:2502.17320](https://arxiv.org/abs/2502.17320)&rbrack;

* Sen Niu, [[Jason Alicea]], D. N. Sheng, Yang Peng: *Quantum anomalous Hall effects and Hall crystals at fractional filling of helical trilayer graphene* &lbrack;[arXiv:2505.24146](https://arxiv.org/abs/2505.24146)&rbrack;

* Hongyu Lu, Han-Qing Wu, Bin-Bin Chen, Wang Yao, Zi Yang Meng: *Generic (fractional) quantum anomalous Hall crystals from interaction-driven band folding* &lbrack;[arXiv:2505.04138](https://arxiv.org/abs/2505.04138)&rbrack;

* Raul Perea-Causin, Hui Liu, Emil J. Bergholtz: *Quantum anomalous Hall crystals in moiré bands with higher Chern number*, Nature Communications **16** 6875 (2025) &lbrack;[doi:10.1038/s41467-025-62224-9](https://doi.org/10.1038/s41467-025-62224-9)&rbrack;

* Zhengyan Darius Shi, T. Senthil: *Doping a fractional quantum anomalous Hall insulator* &lbrack;[arXiv:2409.20567](https://arxiv.org/abs/2409.20567)&rbrack;

    

The case of [[crystalline topological insulators]] and [[symmetry protected topological order]]:

* Yuan-Ming Lu, Ying Ran: *Symmetry protected fractional Chern insulators and fractional topological insulators*, Phys. Rev. B **85** (2012)  165134 &lbrack;[arXiv:1109.0226](https://arxiv.org/abs/1109.0226), [doi:10.1103/PhysRevB.85.165134](https://doi.org/10.1103/PhysRevB.85.165134)&rbrack;
  > "In fact, the recently discovered FCI states preserve all the lattice point group symmetry as well as translational symmetry. Here in this paper, we point out that as a consequence of the lattice symmetry, there exist many different quantum FCI phases, all respecting the full lattice symmetry, even at the same filling fraction with the same quantum Hall conductance \[...\] These distinct FCI phases cannot be adiabatically connected with each other without a phase transition while the lattice symmetry is respected"

* Chao-Ming Jian, Xiao-Liang Qi: *Crystal-symmetry preserving Wannier states for fractional chern insulators*, Phys. Rev. B **88** (2013) 165134 &lbrack;[arXiv:1303.1787](https://arxiv.org/abs/1303.1787), [doi:10.1103/PhysRevB.88.165134](https://doi.org/10.1103/PhysRevB.88.165134)&rbrack;

* Ke Huang, Xiao Li, [[Sankar Das Sarma]], Fan Zhang: *Self-consistent theory of fractional quantum anomalous Hall states in rhombohedral graphene* Phys. Rev. B **110** (2024) 115146 &lbrack;[doi:10.1103/PhysRevB.110.115146](https://doi.org/10.1103/PhysRevB.110.115146), [arXiv:2407.08661](https://arxiv.org/abs/2407.08661)&rbrack;

* Yuxuan Zhang, [[Maissam Barkeshli]]: *Fractionally Quantized Electric Polarization and Discrete Shift of Crystalline Fractional Chern Insulators*, Phys. Rev. B
&lbrack;[arXiv:2411.04171](https://arxiv.org/abs/2411.04171), [doi:10.1103/qslx-ybf6](https://doi.org/10.1103/qslx-ybf6)&rbrack;

* Naren Manjunath: *Crystalline invariants of integer
and fractional Chern insulators*, talk at *[Recent Developments and Challenges in Topological Phases](https://www2.yukawa.kyoto-u.ac.jp/~yitpmolecule-topology-2024/)*, Kyoto University (2024) &lbrack;[pdf](https://www2.yukawa.kyoto-u.ac.jp/~yitpmolecule-topology-2024/slide/Naren.pdf), [[Manjunath-CrystallineInvariantsofFCI.pdf:file]]&rbrack;

See also:

* Kryštof Kolář, Kang Yang, [[Felix von Oppen]], Christophe Mora: *Robustness of real-space topology in moiré systems* &lbrack;[arXiv:2507.00130](https://arxiv.org/abs/2507.00130)&rbrack;

Relation to [[superconductors]]:

* Taige Wang, Michael P. Zaletel: *Chiral superconductivity near a fractional Chern insulator* &lbrack;[arXiv:2507.07921](https://arxiv.org/abs/2507.07921)&rbrack;

#### Anyonic states
  {#ReferencesFQAHAnyons}

On [[anyons]] in FQAH systems:

* Aidan P. Reddy, Nisarga Paul, Ahmed Abouelkomsan, Liang Fu: *Non-Abelian fractionalization in topological minibands*, Phys. Rev. Lett. **133** (2024) 166503 &lbrack;[arXiv:2403.00059](https://arxiv.org/abs/2403.00059), [doi:10.1103/PhysRevLett.133.166503](https://doi.org/10.1103/PhysRevLett.133.166503)
&rbrack;

* Hui Liu, Zhao Liu, Emil J. Bergholtz: *Non-Abelian Fractional Chern Insulators and Competing States in Flat Moiré Bands*, Phys. Rev. Lett. **135** (2025) 106604 &lbrack;[arXiv:2405.08887](https://arxiv.org/abs/2405.08887), [doi:10.1103/43nq-ntqm](https://doi.org/10.1103/43nq-ntqm)&rbrack;

* Ryohei Kobayashi, Yuxuan Zhang, Naren Manjunath, [[Maissam Barkeshli]]: *Crystalline invariants of fractional Chern insulators*, Phys. Rev. B (2025) &lbrack;[arXiv:2405.17431](https://arxiv.org/abs/2405.17431), [doi:10.1103/8bpm-qbzp](https://doi.org/10.1103/8bpm-qbzp)&rbrack;

* Hui Liu, Raul Perea-Causin & Emil J. Bergholtz: *Parafermions in moiré minibands*, Nature Communications **16** (2025) 1770 &lbrack;[doi:10.1038/s41467-025-57035-x](https://doi.org/10.1038/s41467-025-57035-x)&rbrack;

* Zhengyan Darius Shi, T. Senthil: *Anyon delocalization transitions out of a disordered FQAH insulator*, PNAS **122**  51 (2025) e2520608122 &lbrack;[arXiv:2506.02128](https://arxiv.org/abs/2506.02128), [doi:10.1073/pnas.2520608122](https://doi.org/10.1073/pnas.2520608122)&rbrack;

* [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:FQAH Anyons|Identifying Anyonic Topological Order in Fractional Quantum Anomalous Hall Systems]]*, Applied Physics Letters (2025) &lbrack;[arXiv:2507.00138](https://arxiv.org/abs/2507.00138)&rbrack;

* Felix A. Palm, Nader Mostaan, Nathan Goldman, Fabian Grusdt: *Interferometric Braiding of Anyons in Chern insulators* &lbrack;[arXiv:2511.09445](https://arxiv.org/abs/2511.09445)&rbrack;

* Chuyi Tuo, Ming-Rui Li, Hong Yao: *Fractional quantum anomalous Hall and anyon density-wave halo in a minimal interacting lattice model of twisted bilayer $MoTe_2$* &lbrack;[arXiv:2512.23608](https://arxiv.org/abs/2512.23608)&rbrack;  


* [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Crystalline Chern Order|Fragile Topological Phases and Topological Order of 2D Crystalline Chern Insulators]]* &lbrack;[arXiv:2512.24709](https://arxiv.org/abs/2512.24709)&rbrack;

#### In view of TQC

In view of potential [[topological quantum computing]] hardware:

* James Urton: *[Researchers make a quantum computing leap with a magnetic twist](https://www.washington.edu/news/2023/06/27/fqah-states/)*, UW News (June 2023)


#### Collective excitations

On the chiral graviton mode in FCIs:

* Min Long, Zeno Bacciconi, Hongyu Lu, Hernan B. Xavier, Zi Yang Meng, Marcello Dalmonte: *Chiral Graviton Modes in Fermionic Fractional Chern Insulators* &lbrack;[arXiv:2601.05196](https://arxiv.org/abs/2601.05196)&rbrack;





[[!redirects quantum anomalous Hall effects]]

[[!redirects quantum anomalous Hall system]]
[[!redirects quantum anomalous Hall systems]]

[[!redirects anomalous quantum Hall effect]]
[[!redirects anomalous quantum Hall effects]]

[[!redirects anomalous quantum  Hall system]]
[[!redirects anomalous quantum  Hall systems]]

[[!redirects fractional quantum anomalous Hall effect]]
[[!redirects fractional quantum anomalous Hall effects]]

[[!redirects fractional quantum anomalous Hall system]]
[[!redirects fractional quantum anomalous Hall systems]]

[[!redirects fractional anomalous quantum Hall effect]]
[[!redirects fractional anomalous quantum Hall effects]]

[[!redirects fractional anomalous quantum Hall system]]
[[!redirects fractional anomalous quantum Hall systems]]

[[!redirects QAH effect]]
[[!redirects QAH effects]]

[[!redirects QAH system]]
[[!redirects QAH systems]]

[[!redirects FQAH effect]]
[[!redirects FQAH effects]]

[[!redirects FQAH system]]
[[!redirects FQAH systems]]

[[!redirects fractional Chern insulator]]
[[!redirects fractional Chern insulators]]




