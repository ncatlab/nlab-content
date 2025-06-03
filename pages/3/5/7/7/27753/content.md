
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

Experimental realization:

* Cui-Zu Chang et al.: *Experimental Observation of the Quantum Anomalous Hall Effect in a Magnetic Topological Insulator*, Science **340** (2013) 167 &lbrack;[doi:10.1126/science.1234414](https://doi.org/10.1126/science.1234414), [arXiv:1605.08829](https://arxiv.org/abs/1605.08829)&rbrack;

Review:

* Jing Wang, [[Biao Lian]], [[Shou-Cheng Zhang]]: *Quantum anomalous Hall effect in magnetic topological insulators*, Physica Scripta **2015** T164 (2015) 014003 &lbrack;[arXiv:1409.6715](https://arxiv.org/abs/1409.6715), [doi:10.1088/0031-8949/2015/T164/014003](https://doi.org/10.1088/0031-8949/2015/T164/014003)&rbrack;

*  [[Chao-Xing Liu]], [[Shou-Cheng Zhang]], Xiao-Liang Qi: *The Quantum Anomalous Hall Effect: Theory and Experiment*,  Annual Review of Condensed Matter Physics **7** (2016) &lbrack;[arXiv:1508.07106](https://arxiv.org/abs/1508.07106), [doi:10.1146/annurev-conmatphys-031115-011417](https://doi.org/10.1146/annurev-conmatphys-031115-011417)&rbrack;

* {#ChangLiuMacDonald23} Cui-Zu Chang, [[Chao-Xing Liu]], [[Allan H. MacDonald]]: *Colloquium: Quantum anomalous Hall effect*, Rev. Mod. Phys. **95** (2023) 011002  &lbrack;[arXiv:2202.13902](https://arxiv.org/abs/2202.13902), [doi:10.1103/RevModPhys.95.011002](https://doi.org/10.1103/RevModPhys.95.011002)&rbrack;


See also:

* Wikipedia: *[Quantum anomalous Hall effect](https://en.wikipedia.org/wiki/Quantum_anomalous_Hall_effect)*


### Fractional QAHE

Theoretical prediction:

* [[Titus Neupert]], [[Luiz Santos]], [[Claudio Chamon]], [[Christopher Mudry]]: *Fractional quantum Hall states at zero magnetic field*, Phys. Rev. Lett. **106** (2011) 236804  &lbrack;[arXiv:1012.4723](https://arxiv.org/abs/1012.4723), [doi:10.1103/PhysRevLett.106.236804](https://doi.org/10.1103/PhysRevLett.106.236804)&rbrack;

* S. A. Parameswaran, [[Rahul Roy]], S. L. Sondhi: *Fractional Quantum Hall Physics in Topological Flat Bands*, Comptes Rendus. Physique, Topological insulators / Isolants topologiques, **14** 9-10 (2013) 816-839 &lbrack;[arXiv:1302.6606](https://arxiv.org/abs/1302.6606), [doi:10.1016/j.crhy.2013.04.003](https://doi.org/10.1016/j.crhy.2013.04.003)&rbrack;

* [[Rahul Roy]]: *Band geometry of fractional topological insulators*, Phys. Rev. B **90** (2014) 165139 &lbrack;[arXiv:1208.2055](https://arxiv.org/abs/1208.2055), [doi:10.1103/PhysRevB.90.165139](https://doi.org/10.1103/PhysRevB.90.165139)&rbrack;




Experimental detection:

* Jiaqi Cai et al.: *Signatures of Fractional Quantum Anomalous Hall States in Twisted $MoTe_2$ Bilayer*, Nature **622** (2023) 63–68 &lbrack;[arXiv:2304.08470](https://arxiv.org/abs/2304.08470), [doi:10.1038/s41586-023-06289-w](https://doi.org/10.1038/s41586-023-06289-w)&rbrack;

* Yihang Zeng et al.: *Thermodynamic evidence of fractional Chern insulator in moiré $MoTe_2$*, Nature **622** (2023) 69–73 &lbrack;[doi:10.1038/s41586-023-06452-3](https://doi.org/10.1038/s41586-023-06452-3)&rbrack;

* Heonjoon Park et al.: *Observation of fractionally quantized anomalous Hall effect*, Nature **622** (2023) 74–79 &lbrack;[doi:10.1038/s41586-023-06536-0](https://doi.org/10.1038/s41586-023-06536-0)&rbrack;

* Zhengguang Lu et al.: *Fractional quantum anomalous Hall effect in multilayer graphene*, Nature **626** (2024) 759–764 &lbrack;[doi:10.1038/s41586-023-07010-7](https://doi.org/10.1038/s41586-023-07010-7)&rbrack;
     


Review:

* Long Yu et al., *The fractional quantum anomalous Hall effect*, Nature Reviews Materials **9** (2024) 455–459 &lbrack;[doi:10.1038/s41578-024-00694-x](https://doi.org/10.1038/s41578-024-00694-x)&rbrack;

* {#Morales-DuranShiMacDonald24} Nicolás Morales-Durán, Jingtian Shi, [[Allan H. MacDonald]]: *Fractionalized electrons in moiré materials*, Nature Reviews Physics **6** (2024) 349–351 &lbrack;[doi:10.1038/s42254-024-00718-z](https://doi.org/10.1038/s42254-024-00718-z)&rbrack;

* Jian Zhao et al.: *Exploring the Fractional Quantum Anomalous Hall Effect in Moiré Materials: Advances and Future Perspectives*, ACS Nano (2025) &lbrack;[doi:10.1021/acsnano.5c01598](https://doi.org/10.1021/acsnano.5c01598)&rbrack;

Further discussion:

* [[Nicolas Regnault]] et al.: *Fractional topological states in rhombohedral multilayer graphene modulated by kagome superlattice* &lbrack;[arXiv:2502.17320](https://arxiv.org/abs/2502.17320)&rbrack;

* Sen Niu, [[Jason Alicea]], D. N. Sheng, Yang Peng: *Quantum anomalous Hall effects and Hall crystals at fractional filling of helical trilayer graphene* &lbrack;[arXiv:2505.24146](https://arxiv.org/abs/2505.24146)&rbrack;



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






