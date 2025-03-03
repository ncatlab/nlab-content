
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Solid state physics
+-- {: .hide}
[[!include solid state physics -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In [[solid state physics]], the term "Majorana zero mode" (often abbreviated "MZM" or just "Majorana") has come to refer to (hypothetical and so far elusive) [[ground states]] of certain effectively 1-dimensional [[quantum materials]] (quantum/nano-wires) which are acted on by a "Majorana operator" (namely the [[Hermitian operator|Hermitian]] combination $c + c^\dagger$ of [[fermion]] [[canonical anti-commutation relations|annihilation/creation operators]], only vaguely related to [[special relativity|relativistic]] [[Majorana spinors]]) and which have been argued to potentially behave like [[Majorana anyons]], in some sense (beware that these modes, being stuck to wires, would not be mobile and hence would not admit [[adiabatic theorem|adiabatic]] [[braiding]] operations in the usual sense, see [here](https://quantumcomputing.stackexchange.com/q/25638/19363)).

These Majorana zero modes were theoretically introduced in a [[spin chain]] [[model (in theoretical physics)|model]] by [Kitaev 2001](#Kitaev01) ("Kitaev spin chain"), originally as a theoretical toy example for [[mass gap|gapped]] and degenerate [[ground states]] vaguely as expected for [[topological order]], but then argued to be realizable on interfaces of [[superconductors]] with certain [[topological insulators]] by [Fu & Kane 2008](#FuKane08); and their [[experiment|experimental]] realization in [[superconductor|super-]]/[[semiconductor|semi-conducting]] nano-wires has been proposed in [Lutchyn, Say & Das Sarma 2010](#LutchynSayDasSarma10), [Oreg, Refael, von Oppen 2010](#OregRefaelvonOppen10).



{#Following} Following these proposals --- and especially after [Microsoft Quantum](https://www.microsoft.com/en-us/research/research-area/quantum-computing) (with [QuTech](https://qutech.nl/) at TU Delft) declared ([Nov 2016](https://blogs.microsoft.com/ai/microsoft-doubles-quantum-computing-bet/)) the concrete aim of realizing [[topological quantum computation]] based on topological qbits given by such "Majorana zero modes" (following the plan laid out in [Das Sarma, Freedman & Nayak 15](#DasSarmaFreedmanNayak15)) --- the topic attracted [enormous attention](https://scholar.google.com/scholar?cites=12195292414684872731&as_sdt=2005&sciodt=0,5&hl=en) in [[solid state physics]].

## Claims and retractions
 {#ClaimsAndRetractions}

{#But} But prominent claims of experimental detection of (these kinds of) Majorana zero modes had to be retracted: 

* [by *Nature* in 2021](https://www.nature.com/articles/d41586-021-00612-z) 

  &lbrack;[doi:10.1038/s41586-021-03373-x](https://doi.org/10.1038/s41586-021-03373-x), [doi:10.5281/zenodo.4587841](https://doi.org/10.5281/zenodo.4587841), [doi:10.5281/zenodo.4545812](https://doi.org/10.5281/zenodo.4545812), [TU Delft press release](https://www.delta.tudelft.nl/article/majorana-not-fraud-confirmation-bias#)&rbrack; 

* [by *Nature* in 2022](http://retractionwatch.com/2022/04/24/authors-retract-second-majorana-paper-from-nature/) &lbrack;[doi:10.1038/s41586-022-04704-2](https://doi.org/10.1038/s41586-022-04704-2)&rbrack; 

* [by *Science* in 2022](https://retractionwatch.com/2022/11/17/another-majorana-particle-paper-retracted-this-time-from-science/) &lbrack;[doi:10.1126/science.adf7575](https://www.science.org/doi/10.1126/science.adf7575)&rbrack;, cf. further commentary by [[Sergey M. Frolov|S.M. Frolov]] [here](https://espressospin.org/2022/11/17/the-fallen-angel-particle/); 

* and a range of further claims are under similar criticism, see [Frolov & Mourik 2020](https://doi.org/10.5281/zenodo.6344447), [Das Sarma & Pan 2021](#DasSarmaPan21), [Frolov, Mourik & Zuo 2022](https://doi.org/10.5281/zenodo.6325378), [Mourik 2024](#Mourik24) and the extensive list [here](https://twitter.com/spinespresso/status/1503352928656138241) and [here](https://bsky.app/profile/spinespresso.bsky.social/post/3likchwf3p22d). 

While many researchers began to dismiss the whole approach of "Majorana zero modes" (e.g. [BSSA21](#BSSA21), [p. 3](https://arxiv.org/pdf/2106.11840v4.pdf#page=3)) a new claim of detection was made by [Nayak 22](#Nayak22) & [MicrosoftQuantum 23](#MicrosoftQuantum23) -- but see the [journal's editorial caveat](#MicrosoftQuantum23Caveat) and cautionary commentary by [Frolov & Mourik 22a](#FrolovMourik22a), [22b](#FrolovMourik22a), [Frolov 22](#Frolov22), [Das Sarma 22, p. 9](#DasSarma22), [Mourik 23](#Mourik23), [Legg 24](#Legg24), [Legg 25](#Legg25).

On [19 Feb 2025](https://azure.microsoft.com/en-us/blog/quantum/2025/02/19/microsoft-unveils-majorana-1-the-worlds-first-quantum-processor-powered-by-topological-qubits/)
a Microsoft Azure press release announced a quantum chip ("*Majorana 1*") suggested to host one topologically protected qbit. The accompanying Nature article [Microsoft Azure Quantum 2025](#AzureFeb25) states more carefully that:

> "*These measurements do not, by themselves, determine whether the low-energy states detected by interferometry are topological.*"

and again the journal issued a [caveat](#AzureFeb25Caveat).

Detailed commentary on these claims in [Legg 2025](#Legg25), [Frolov & Mourik 2025](#FrolovMourik25).


The accompanying company "roadmap" ([arXiv:2502.12252](https://arxiv.org/abs/2502.12252)) mentions the idea of Bonderson et al. 2008 (review [here](https://quantumcomputing.stackexchange.com/q/25638/19363)) of simulating braiding of these immovable states by a measurement-only protocol (a kind of [[quantum simulation]] of actual braiding, see [there](quantum+simulation#OfAnyons)).




## References

Named after *[[Ettore Majorana]]*.

### MZM in nanowires

The general strategy of realizing [[Majorana zero modes]] in supercondocuting/semiconducting nanowires is motivated by the [[Kitaev spin chain]]:

* {#Kitaev01} [[Alexei Kitaev]], *Unpaired Majorana fermions in quantum wires*,  Physics-Uspekhi, **44** 10S (2001) 131-136 &lbrack;[arXiv:cond-mat/0010440](https://arxiv.org/abs/cond-mat/0010440), [doi:10.1070/1063-7869/44/10S/S29](https://iopscience.iop.org/article/10.1070/1063-7869/44/10S/S29)&rbrack;

further developed in:

* {#FuKane08} [[Liang Fu]], [[Charles Kane]], *Superconducting Proximity Effect and Majorana Fermions at the Surface of a Topological Insulator*, Phys. Rev. Lett. **100** (2008) 096407 &lbrack;[doi:10.1103/PhysRevLett.100.096407](https://doi.org/10.1103/PhysRevLett.100.096407), [arXiv:0707.1692](https://arxiv.org/abs/0707.1692)&rbrack;

* {#LutchynSayDasSarma10} Roman M. Lutchyn, Jay D. Sau, [[Sankar Das Sarma]], *Majorana Fermions and a Topological Phase Transition in Semiconductor-Superconductor Heterostructures*, Phys. Rev. Lett. **105** (2010) 077001 &lbrack;[doi:10.1103/PhysRevLett.105.077001](https://doi.org/10.1103/PhysRevLett.105.077001)&rbrack;  

* {#OregRefaelvonOppen10} Yuval Oreg, Gil Refael, [[Felix von Oppen]], *Helical Liquids and Majorana Bound States in Quantum Wires*, Phys. Rev. Lett. **105** (2010) 177002 &lbrack;[doi:10.1103/PhysRevLett.105.177002](https://doi.org/10.1103/PhysRevLett.105.177002), [arXiv:1003.1145](https://arxiv.org/abs/1003.1145)&rbrack;

* [[Lukasz Fidkowski]], [[Alexei Kitaev]], *The effects of interactions on the topological classification of free fermion systems*, Phys. Rev. B **81** (2010) 134509  &lbrack;[arXiv:0904.2197](https://arxiv.org/abs/0904.2197), [doi:10.1103/PhysRevB.81.134509](https://doi.org/10.1103/PhysRevB.81.134509)&rbrack;

  > ([[interaction|interacting]] generalization)


reviewed in:

* Carlo W. J. Beenakker: *Search for non-Abelian Majorana braiding statistics in superconductors*, SciPost Phys. Lect. Notes **15** (2020) \[<a href="https://doi.org/10.21468/SciPostPhysLectNotes.15">doi:10.21468/SciPostPhysLectNotes.15</a>, [arXiv:1907.06497](https://arxiv.org/abs/1907.06497)\]

* [[Pasquale Marra]], *Majorana nanowires for topological quantum computation: A tutorial*, J. of Applied Physics **132** (2022) 231101   &lbrack;[arXiv:2206.14828](https://arxiv.org/abs/2206.14828), [doi:10.1063/5.0102999](https://doi.org/10.1063/5.0102999)&rbrack;

Discussion in the context of [[topological quantum computation]]:

* {#DasSarmaFreedmanNayak15} [[Sankar Das Sarma]], [[Michael Freedman]], [[Chetan Nayak]], *Majorana zero modes and topological quantum computation*, npj Quantum Inf **1** 15001 (2015) $[$[doi:10.1038/npjqi.2015.1](https://doi.org/10.1038/npjqi.2015.1)$]$

General review and experimental status:

* [[Sergey M. Frolov]], *How do we discover MAJORANA PARTICLES in NANOWIRES?*, talk via [ Instituto de Física, Universidade de São Paulo](http://portal.if.usp.br/ifusp/) (May 2021) &lbrack;[video](https://www.youtube.com/watch?v=7btnPqmSh_0)&rbrack;

  > [41:25](https://youtu.be/7btnPqmSh_0?t=2485): No, we have not discovered Majorana particles in nanowires. Yes, we should be able to do it.


* {#DasSarma22} [[Sankar Das Sarma]], *In search of Majorana*, Nature Physics **19** (2023) 165-170 &lbrack;[arXiv:2210.17365](https://arxiv.org/abs/2210.17365), [doi:10.1038/s41567-022-01900-9](https://doi.org/10.1038/s41567-022-01900-9)&rbrack;



See also:

* Wikipedia, *[Majorana bound states](https://en.wikipedia.org/wiki/Majorana_fermion#Majorana_bound_states)*

### Non-Detection 
  {#ReferencesNonDetection}


On the general problem of distinguishing the expected effect from noise:

* {#DasSarmaPan21} [[Sankar Das Sarma]], Haining Pan, *Disorder-induced zero-bias peaks in Majorana nanowires*, Phys. Rev. B **103** 195158 (2021) &lbrack;[arXiv:2103.05628](https://arxiv.org/abs/2103.05628), [doi:10.1103/PhysRevB.103.195158](https://doi.org/10.1103/PhysRevB.103.195158)&rbrack;
> we believe that similar confirmation bias applies to many other topological discovery claims in the literature during 2000–2020 where a precise knowledge of what one is looking for has been the key factor in the discovery claim, with the experimental quantization results themselves not being sufficiently compelling. &lbrack;...&rbrack; Our results certainly apply to most of the Majorana experiments during 2012–2021 in the literature.

* {#BSSA21} Koen Bertels, Tamara Sarac, Aritra Sarkar, Imran Ashraf, *Quantum Computing -- from NISQ to PISQ*, IEEE Micro **41** (2021) 24-32 &lbrack;[arXiv:2106.11840v4](https://arxiv.org/abs/2106.11840v4), [doi:10.1109/MM.2021.3099195](https://doi.ieeecomputersociety.org/10.1109/MM.2021.3099195)&rbrack;

> [p. 3](https://arxiv.org/pdf/2106.11840v4.pdf#page=3): The quantum physics community is sufficiently aware that when certain qubit technologies do not produce any reasonable result after several years of effort, they should be gently removed from the list of quantum candidates. After working with the physics colleagues in Delft, we saw that happening with the Majorana qubits that could not be confirmed in any follow-up experiment.

* {#FrolovMourik22a} [[Sergey M. Frolov]], [[Vincent Mourik]], *We cannot believe we overlooked these Majorana discoveries* &lbrack;[arXiv:2203.17060](https://arxiv.org/abs/2203.17060), [doi:10.5281/zenodo.6364928](https://doi.org/10.5281/zenodo.6364928), conclusion on: [p. 7](https://arxiv.org/ftp/arxiv/papers/2203/2203.17060.pdf#page=7)&rbrack;


Non-retracted claims of experimental realization of something in the direction of Majorana zero modes:

* {#MMBDRSC19} Gerbold C. Ménard, Andrej Mesaros, Christophe Brun, François Debontridder, Dimitri Roditchev, Pascal Simon, Tristan Cren, *Isolated pairs of Majorana zero modes in a disordered superconducting lead monolayer*,  Nat Commun **10** 2587 (2019) $[$[doi:10.1038/s41467-019-10397-5](https://doi.org/10.1038/s41467-019-10397-5)$]$

* {#Nayak22} [[Chetan Nayak]], *Microsoft has demonstrated the underlying physics required to create a new kind of qubit*, Microsoft Research Blog (March 2022)

* {#MicrosoftQuantum23} M. Aghaee et al. ([Microsoft Quantum](https://www.microsoft.com/en-us/research/research-area/quantum-computing)), *InAs-Al Hybrid Devices Passing the Topological Gap Protocol*, Phys. Rev. B **107** 245423 (2023) &lbrack;[doi:10.1103/PhysRevB.107.245423](https://doi.org/10.1103/PhysRevB.107.245423), [arXiv:2207.02472](https://arxiv.org/abs/2207.02472), [video presentation](https://www.microsoft.com/en-us/research/video/inas-al-hybrid-devices-passing-the-topological-gap-protocol/)&rbrack;

  \linebreak
  {#MicrosoftQuantum23Caveat} with an accompanying caveat editorial:

  Randall D. Kamien, Jessica Thomas, Stephen E. Nagler, Anthony M. Begley, and Sarma Kancharla, *Editorial: Transparency in Physical Review Articles*, Phys. Rev. B **107** 210001 (2023) &lbrack;[doi:10.1103/PhysRevB.107.210001](https://doi.org/10.1103/PhysRevB.107.210001)&rbrack;

  saying:

  > "In this issue of Physical Review B, Aghaee et al. &lbrack;[1](#MicrosoftQuantum23)&rbrack; report on an advancement towards the goal of topological quantum computing. While Physical Review readers are well aware that the many minutiæ of procedures, computations, and synthesis may be omitted in any particular dispatch, in this publication the intellectual property of the authors’ employer has prevented the release of some parameters of the studied devices that may be needed in order to reproduce them. As a reflection of the traditional values of the scholarly community, this is not in accordance with the usual norms of the Physical Review journals."

* {#AzureFeb25} Microsof Azure Quantum: *Interferometric single-shot parity measurement in InAs–Al hybrid devices*, Nature **638** (2025) 651–655 &lbrack;[doi:10.1038/s41586-024-08445-2](https://doi.org/10.1038/s41586-024-08445-2)&rbrack;

  {#AzureFeb25Caveat} again with an accompanying caveat editorial ("Peer Review File" &lbrack;[pdf](https://static-content.springer.com/esm/art%3A10.1038%2Fs41586-024-08445-2/MediaObjects/41586_2024_8445_MOESM2_ESM.pdf)&rbrack;):
  > "The editorial team wishes to point out that the results in this manuscript do not represent evidence for the presence of Majorana zero modes in the reported devices. The work is published for introducing a device architecture that might enable fusion experiments using future Majorana zero modes."


but see commentary in:

* [[Sergey Frolov]], *[Twitter:1671558089382957056](https://twitter.com/spinespresso/status/1671558089382957056) * (21 June 2023)

* Karmela Padavic-Callaghan, *Microsoft says its weird new particle could improve quantum computers --- Researchers at Microsoft say they have created elusive quasiparticles called Majorana zero modes -- but scientists outside the company are sceptical*, New Scientist (21 June 2023) &lbrack;[web](https://www.newscientist.com/article/2378782-microsoft-says-its-weird-new-particle-could-improve-quantum-computers)&rbrack;

* {#Mourik23} [[Vincent Mourik]]: correspondence with PRX editorial team on what later was published as [MS23](#MicrosoftQuantum23)  (2023) &lbrack;[pubpeer](https://pubpeer.com/publications/4C7F25D6DFE392856EF4171E379D67)&rbrack;

* {#Legg25} Henry F. Legg: *Comment on "InAs-Al hybrid devices passing the topological gap protocol", Microsoft Quantum, Phys. Rev. B 107, 245423 (2023)* &lbrack;[arXiv:2502.19560](https://arxiv.org/abs/2502.19560)&rbrack;

* {#FrolovMourik25} [[Sergey M. Frolov]], [[Vincent Mourik]]: *Majorana Fireside Chat: HOW CLOSE ARE WE TO A TOPOLOGICAL QUBIT?* (Feb 2025) &lbrack;[YT](https://youtu.be/9Ag-L3hZiXo)&rbrack;

and earlier:

* {#FrolovMourik22b} [[Sergey M. Frolov]], [[Vincent Mourik]]: *Majorana Fireside Podcast, Episode 1: The Microsoft TGP paper live review* &lbrack;[video](https://www.youtube.com/watch?v=RnYghkDaHH0), conclusion at: [1:01:31](https://www.youtube.com/watch?v=RnYghkDaHH0&t=3691s)&rbrack;

  > [1:01:52](https://youtu.be/RnYghkDaHH0?t=3712) The signal is fully consistent, from what we see, with *not* having discovered any Majorana or topological superconductivity here. At the same time, the amount of data is extremely narrow.

* {#Frolov22} [[Sergey M. Frolov]], *Superconductors and semiconductors, nanowires and majorana, research and integrity* &lbrack;[video](https://www.youtube.com/watch?v=FR7J4yH67GA), general caution: [55:34](https://youtu.be/FR7J4yH67GA?t=3334), concrete criticism: [1:01:41](https://youtu.be/FR7J4yH67GA?t=3701)&rbrack;
  > [1:01:50](https://youtu.be/FR7J4yH67GA?t=3710): The claims of the discovery of Majorana have been overblown and are false. Majorana has not been discovered in nanowires. I don't believe in any other system it has been discovered either.

On how this could happen:

* Elizabeth Gibney, *Inside Microsoft’s quest for a topological quantum computer* (Interview with Alex Bocharov), Nature (2016) &lbrack;[doi:10.1038/nature.2016.20774](https://doi.org/10.1038/nature.2016.20774)&rbrack;
  > &lbrack;Bocharov:&rbrack; We’re people-centric, rather than problem-centric.

See also:

* {#Frolov21} [[Sergey M. Frolov]], *So, You Think You Discovered a New State of Matter?*, Physics **14** 68 (2021) &lbrack;[physics.aps:v14/68](https://physics.aps.org/articles/v14/68)&rbrack;

* [[Sergey M. Frolov]], *Quantum computing’s reproducibility crisis: Majorana fermions*, Nature **592** (2021) 350-352 &lbrack;[doi:10.1038/d41586-021-00954-8](https://doi.org/10.1038/d41586-021-00954-8)&rbrack;

* {#Mourik24} [[Vincent Mourik]], *You uncovered unreliable research. What happens next?*, talk at *[International Conference on Reproducibility in Condensed Matter Physics](https://www.pqi.org/international-conference-reproducibility-condensed-matter-physics)*, Pittburgh Quantum Institute (2024) &lbrack;video:[YT](https://youtu.be/j6fQsTpU2-g?list=PLtTPtV8SRcxgDSzmQZ5X9WcHV2PMehPBj)&rbrack;

* Charles Gould, *Debunking the data behind the "Chiral Majorana fermion modes" claim*, talk at *[International Conference on Reproducibility in Condensed Matter Physics](https://www.pqi.org/international-conference-reproducibility-condensed-matter-physics)*, Pittburgh Quantum Institute (2024) &lbrack;video:[YT](https://youtu.be/fIIx8LL9r0c?list=PLtTPtV8SRcxgDSzmQZ5X9WcHV2PMehPBj)&rbrack;

* {#Legg24} Henry Legg, *Nonlocal conductance as a measure of topological superconducting phases*, talk at *[International Conference on Reproducibility in Condensed Matter Physics](https://www.pqi.org/international-conference-reproducibility-condensed-matter-physics)*, Pittburgh Quantum Institute (2024) &lbrack;video:[YT](https://youtu.be/OmUaLewy6Fs?list=PLtTPtV8SRcxgDSzmQZ5X9WcHV2PMehPBj)&rbrack;





\linebreak

[[!include anyons in topological superconductors -- references]]


[[!redirects Majorana zero modes]]

[[!redirects Kitaev spin chain]]
[[!redirects Kitaev spin chains]]
