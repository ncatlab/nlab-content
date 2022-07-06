
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

By *adiabatic quantum computation* one means models of [[quantum computation]] on [[parameterized quantum systems]] where the [[quantum gates]] are [[unitary transformations]] on a [[topological phase of matter|gapped]] (and possibly [[topological order|topologically ordered]]) [[ground state]] which are induced, via the [[quantum adiabatic theorem]], by sufficiently slow movement of external [[dependent linear type theory|parameters]].

Often the term *adiabatic quantum computation* is used by default for [[optimization theory|optimization]] problems ("[[quantum annealing]]", see the references [below](#QuantumAnnealingReferences)).

On the other hand, the possibly most prominent example of adiabatic quantum computation is often not advertized as such (but see [CLBFN 2015](#CLBFN15)), namely [[topological quantum computation]] by adiabatic [[braid group|braiding]] of [defect anyons](braid+group+statistics#AsBraidingOfDefects) (whose positions is the external parameter, varying in a [[configuration space of points]]). This is made explicit in [Freedman, Kitaev, Larsen & Wang 2003, pp. 6](#FreedmanKitaevLarsenWang03); [Nayak, Simon, Stern & Freedman 2008, §II.A.2 (p. 6)](#NayakSimonSternFreedman08); and [Cheng, Galitski & Das Sarma 2011, p. 1](#ChengGalitskiDasSarma11); see also [Arovas, Schrieffer, Wilczek & Zee 1985, p. 1](#ArovasSchriefferWilczekZee85) and [Stanescu 2020, p. 321](#Stanescu20); [Barlas & Prodan 2020](#BarlasProdan20).

The following graphics shows this with labelling indicative of [momentum-space anyons](braid+group+statistics#ReferencesAnyonicBraidingInMomentumSpace):

\begin{imagefromfile}
    "file_name": "AdiabaticBraidingOfBandNodes-220604.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

> (graphics from [[schreiber:Topological Quantum Computation in TED-K|SS22]]) 


## References
 {#References}

### In optimization -- quantum annealing
 {#QuantumAnnealingReferences}

Discussion with focus on optimization problems ([[quantum annealing]]):

* Catherine C. McGeoch, *Adiabatic Quantum Computation and Quantum Annealing: Theory and Practice* Synthesis Lectures on Quantum Computing $[$[doi:10.2200/S00585ED1V01Y201407QMC008)](https://doi.org/10.2200/S00585ED1V01Y201407QMC008))$]$

* Tameem Albash, Daniel A. Lidar,  *Adiabatic Quantum Computing*, Rev. Mod. Phys. **90** (2018) 015002 $[$[arXiv:1611.04471](https://arxiv.org/abs/1611.04471), [doi:10.1103/RevModPhys.90.015002](https://doi.org/10.1103/RevModPhys.90.015002)$]$

* Erica K. Grant and Travis S. Humble, *Adiabatic Quantum Computing and Quantum Annealing* $[$[doi:10.1093/acrefore/9780190871994.013.32](https://doi.org/10.1093/acrefore/9780190871994.013.32)$]$

* Atanu Rajak, Sei Suzuki, Amit Dutta, Bikas K. Chakrabarti, *Quantum Annealing: An Overview* &lbrack;[arXiv:2207.01827](https://arxiv.org/abs/2207.01827)&rbrack;

    
See also:

* Wikipedia, *[Adiabatic quantum computation](https://en.wikipedia.org/wiki/Adiabatic_quantum_computation)*

### In topological quantum computation

References which make explicit that [[topological quantum computation]] with [[anyons]] is a form of adiabatic quantum computation:

* {#ArovasSchriefferWilczekZee85} [[Daniel P. Arovas]], [[Robert Schrieffer]], [[Frank Wilczek]], [[Anthony Zee]], *Statistical mechanics of anyons*, Nuclear Physics B **251** (1985) 117-126 (reprinted in [Wilczek 1990, p. 173-182](anyon#Wilczek90)) $[$<a href="https://doi.org/10.1016/0550-3213(85)90252-4">doi:10.1016/0550-3213(85)90252-4</a>$]$

* {#FreedmanKitaevLarsenWang03} [[Michael Freedman]], [[Alexei Kitaev]], [[Michael Larsen]], [[Zhenghan Wang]], pp. 6 of *Topological quantum computation*,  Bull. Amer. Math. Soc. __40__ (2003), 31-38 ([arXiv:quant-ph/0101025](https://arxiv.org/abs/quant-ph/0101025), [doi:10.1090/S0273-0979-02-00964-3](https://doi.org/10.1090/S0273-0979-02-00964-3), [pdf](http://www.ams.org/journals/bull/2003-40-01/S0273-0979-02-00964-3/S0273-0979-02-00964-3.pdf))

* {#NayakSimonSternFreedman08} [[Chetan Nayak]], [[Steven H. Simon]], [[Ady Stern]], [[Michael Freedman]], [[Sankar Das Sarma]], §II.A.2 (p. 6) of: _Non-Abelian Anyons and Topological Quantum Computation_, Rev. Mod. Phys. **80** 1083 (2008) $[$[arXiv:0707.1888] (http://arxiv.org/abs/0707.1889), [doi:10.1103/RevModPhys.80.1083](https://doi.org/10.1103/RevModPhys.80.1083)$]$

* {#ChengGalitskiDasSarma11} [[Meng Cheng]], [[Victor Galitski]], [[Sankar Das Sarma]], *Non-adiabatic Effects in the Braiding of Non-Abelian Anyons in Topological Superconductors*, Phys. Rev. B **84** (2011) 104529 $[$[arXiv:1106.2549](https://arxiv.org/abs/1106.2549), [doi:10.1103/PhysRevB.84.104529](https://doi.org/10.1103/PhysRevB.84.104529)$]$


* {#CLBFN15} Chris Cesare, Andrew J. Landahl, Dave Bacon, Steven T. Flammia, Alice Neels, *Adiabatic topological quantum computing*, Phys. Rev. A **92** (2015) 012336  $[$[arXiv:1406.2690](https://arxiv.org/abs/1406.2690), [doi:10.1103/PhysRevA.92.012336](https://doi.org/10.1103/PhysRevA.92.012336)$]$

* {#Stanescu20} [[Tudor D. Stanescu]], p. 321 of: *Introduction to Topological Quantum Matter & Quantum Computation*, CRC Press 2020 ([ISBN:9780367574116](https://www.routledge.com/Introduction-to-Topological-Quantum-Matter--Quantum-Computation/Stanescu/p/book/9780367574116)) 


* {#BarlasProdan20} Yafis Barlas, Emil Prodan, *Topological braiding of non-Abelian mid-gap defects in classical meta-materials*, Phys. Rev. Lett. **124** (2020) 146801 $[$[arXiv:1903.00463](https://arxiv.org/abs/1903.00463), [doi:10.1103/PhysRevLett.124.146801](https://doi.org/10.1103/PhysRevLett.124.146801)$]$ 





[[!redirects quantum annealing]]
