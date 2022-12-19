
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

Review with focus on optimization problems ([[quantum annealing]]):

* Catherine C. McGeoch, *Adiabatic Quantum Computation and Quantum Annealing: Theory and Practice* Synthesis Lectures on Quantum Computing &lbrack;[doi:10.2200/S00585ED1V01Y201407QMC008)](https://doi.org/10.2200/S00585ED1V01Y201407QMC008))&rbrack;

* Tameem Albash, Daniel A. Lidar,  *Adiabatic Quantum Computing*, Rev. Mod. Phys. **90** (2018) 015002 &lbrack;[arXiv:1611.04471](https://arxiv.org/abs/1611.04471), [doi:10.1103/RevModPhys.90.015002](https://doi.org/10.1103/RevModPhys.90.015002)&rbrack;

* Erica K. Grant and Travis S. Humble, *Adiabatic Quantum Computing and Quantum Annealing*, Oxford research Encyclopedia (20200) &lbrack;[doi:10.1093/acrefore/9780190871994.013.32](https://doi.org/10.1093/acrefore/9780190871994.013.32)&rbrack;

* Atanu Rajak, Sei Suzuki, Amit Dutta, Bikas K. Chakrabarti, *Quantum Annealing: An Overview* &lbrack;[arXiv:2207.01827](https://arxiv.org/abs/2207.01827)&rbrack;

    
See also:

* Wikipedia, *[Adiabatic quantum computation](https://en.wikipedia.org/wiki/Adiabatic_quantum_computation)*

* Minjae Jo, Michael Hanks, M. S. Kim, *Divide-and-conquer embedding for QUBO quantum annealing* &lbrack;[arXiv:2211.02184](https://arxiv.org/abs/2211.02184)&rbrack;

* Yusuke Kimura, Hidetoshi Nishimori, *Rigorous convergence condition for quantum annealing*, J. Phys. A: Math. Theor. **55** (2022) 435302 &lbrack;[arXiv:2207.12096](https://arxiv.org/abs/2207.12096), [doi:10.1088/1751-8121/ac9dce](https://doi.org/10.1088/1751-8121/ac9dce)&rbrack;


Proof that quantum annealing is universal for quantum computation:

* Dorit Aharonov, Wim van Dam, Julia Kempe, Zeph Landau, [[Seth Lloyd]], Oded Regev, *Adiabatic Quantum Computation is Equivalent to Standard Quantum Computation*, SIAM Review **50** 4 (2008) &lbrack;[arXiv:quant-ph/0405098](https://arxiv.org/abs/quant-ph/0405098), [doi:10.1137/080734479](https://doi.org/10.1137/080734479)&rbrack;

A more high-brow mathematical desription via "tangle machines":

* Avishy Y. Carmi, [[Daniel Moskovich]], §5 of: *Tangle Machines*, Proc. R. Soc. A **471** (2015) 20150111 &lbrack;[arXiv:1404.2862](https://arxiv.org/abs/1404.2862), [doi:10.1098/rspa.2015.0111](https://doi.org/10.1098/rspa.2015.0111)&rbrack;



### Geometric phase gates

References which consider quantum gates operating by (nonabelian) geometric Berry phases due to adiabatic parameter movement:

* Paolo Zanardi, Mario Rasetti, *Holonomic Quantum Computation*, Phys. Lett. A **264** (1999) 94-99 &lbrack;[doi:10.1016/S0375-9601%2899%2900803-8](https://doi.org/10.1016/S0375-9601%2899%2900803-8), [arXiv:quant-ph/9904011](https://arxiv.org/abs/quant-ph/9904011)
&rbrack;

* Jonathan A. Jones, Vlatko Vedral, Artur Ekert, Giuseppe Castagnoli, *Geometric quantum computation using nuclear magnetic resonance*, Nature **403** (2000) 869–871 &lbrack;[doi:10.1038/35002528](https://doi.org/10.1038/35002528)&rbrack;

* Giuseppe Falci, Rosario Fazio, G. Massimo Palma, Jens Siewert & Vlatko Vedral, *Detection of geometric phases in superconducting nanocircuits*, Nature **407** 355–358 (2000) &lbrack;[doi:10.1038/35030052](https://doi.org/10.1038/35030052)&rbrack;

* L. M. Duan, J. I. Cirac, P. Zoller, *Geometric Manipulation of Trapped Ions for Quantum Computation*, Science **292** (2001) 1695 &lbrack;[arXiv:quant-ph/0111086](https://arxiv.org/abs/quant-ph/0111086), [doi:10.1126/science.1058835](https://doi.org/10.1126/science.1058835)&rbrack;






### In topological quantum computation

References which make explicit that [[topological quantum computation]] by [[braiding]] of [[anyon]] [[worldlines]] is a form of adiabatic quantum computation:

* {#ArovasSchriefferWilczekZee85} [[Daniel P. Arovas]], [[Robert Schrieffer]], [[Frank Wilczek]], [[Anthony Zee]], *Statistical mechanics of anyons*, Nuclear Physics B **251** (1985) 117-126 (reprinted in [Wilczek 1990, p. 173-182](anyon#Wilczek90)) $[$<a href="https://doi.org/10.1016/0550-3213(85)90252-4">doi:10.1016/0550-3213(85)90252-4</a>$]$

* {#FreedmanKitaevLarsenWang03} [[Michael Freedman]], [[Alexei Kitaev]], [[Michael Larsen]], [[Zhenghan Wang]], pp. 6 of *Topological quantum computation*,  Bull. Amer. Math. Soc. __40__ (2003), 31-38 ([arXiv:quant-ph/0101025](https://arxiv.org/abs/quant-ph/0101025), [doi:10.1090/S0273-0979-02-00964-3](https://doi.org/10.1090/S0273-0979-02-00964-3), [pdf](http://www.ams.org/journals/bull/2003-40-01/S0273-0979-02-00964-3/S0273-0979-02-00964-3.pdf))

* {#NayakSimonSternFreedman08} [[Chetan Nayak]], [[Steven H. Simon]], [[Ady Stern]], [[Michael Freedman]], [[Sankar Das Sarma]], §II.A.2 (p. 6) of: _Non-Abelian Anyons and Topological Quantum Computation_, Rev. Mod. Phys. **80** 1083 (2008) &lbrack;[arXiv:0707.1888] (http://arxiv.org/abs/0707.1889), [doi:10.1103/RevModPhys.80.1083](https://doi.org/10.1103/RevModPhys.80.1083)&rbrack;

* {#ChengGalitskiDasSarma11} [[Meng Cheng]], [[Victor Galitski]], [[Sankar Das Sarma]], *Non-adiabatic Effects in the Braiding of Non-Abelian Anyons in Topological Superconductors*, Phys. Rev. B **84** (2011) 104529 &lbrack;[arXiv:1106.2549](https://arxiv.org/abs/1106.2549), [doi:10.1103/PhysRevB.84.104529](https://doi.org/10.1103/PhysRevB.84.104529)&rbrack;

* [[Jiannis K. Pachos]], *Introduction to Topological Quantum Computation*, Cambridge University Press (2012) &lbrack;[doi:10.1017/CBO9780511792908]( https://doi.org/10.1017/CBO9780511792908)&rbrack;

  > &lbrack;p. 50&rbrack;: "topological quantum computation resembles an adiabatic quantum computation with constant energy gap, where the quasiparticle coordinates provide the control parameters of the Hamiltonian."

  > &lbrack;p. 52&rbrack;: "Holonomic quantum computation resembles the adiabatic scheme &lbrack;...&rbrack; topological quantum computation can be considered as holonomic computation where the employed adiabatic evolutions have topological characteristics."


* {#CLBFN15} Chris Cesare, Andrew J. Landahl, Dave Bacon, Steven T. Flammia, Alice Neels, *Adiabatic topological quantum computing*, Phys. Rev. A **92** (2015) 012336  &lbrack;[arXiv:1406.2690](https://arxiv.org/abs/1406.2690), [doi:10.1103/PhysRevA.92.012336](https://doi.org/10.1103/PhysRevA.92.012336)&rbrack;

* {#LahtinenPachos17} [[Ville Lahtinen]], [[Jiannis K. Pachos]], p. 1 of: _A Short Introduction to Topological Quantum Computation_,  SciPost Phys. **3** 021 (2017) &lbrack;[arXiv:1705.04103](https://arxiv.org/abs/1705.04103), [doi:10.21468/SciPostPhys.3.3.021](https://scipost.org/SciPostPhys.3.3.021)&rbrack;

* E. Macaluso, T. Comparin, L. Mazza, and I. Carusotto, *Fusion Channels of Non-Abelian Anyons from Angular-Momentum and Density-Profile Measurements*, Phys. Rev. Lett. **123** 266801 (2019) &lbrack;[arXiv:1903.03011](https://arxiv.org/abs/1903.03011), [doi:10.1103/PhysRevLett.123.266801](https://doi.org/10.1103/PhysRevLett.123.266801)&rbrack;


* {#Stanescu20} [[Tudor D. Stanescu]], p. 321 of: *Introduction to Topological Quantum Matter & Quantum Computation*, CRC Press 2020 ([ISBN:9780367574116](https://www.routledge.com/Introduction-to-Topological-Quantum-Matter--Quantum-Computation/Stanescu/p/book/9780367574116)) 


* {#BarlasProdan20} Yafis Barlas, Emil Prodan, *Topological braiding of non-Abelian mid-gap defects in classical meta-materials*, Phys. Rev. Lett. **124** (2020) 146801 &lbrack;[arXiv:1903.00463](https://arxiv.org/abs/1903.00463), [doi:10.1103/PhysRevLett.124.146801](https://doi.org/10.1103/PhysRevLett.124.146801)&rbrack;





[[!redirects quantum annealing]]
