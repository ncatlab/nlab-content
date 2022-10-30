
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

In [[solid state physics]], the term "Majorana zero mode" (often abbreviated "MZM" or just "Majorana") has come to refer to (hypothetical) [[ground states]] of certain effectively 1-dimensional [[quantum materials]] (quantum/nano-wires) which are acted on by a "Majorana operator" (namely the [[Hermitian operator|Hermitian]] combination $c + c^\dagger$ of [[fermion]] [[canonical anti-commutation relations|annihilation/creation operators]], only vaguely related to [[special relativity|relativistic]] [[Majorana spinors]]) and which have been argued to potentially behave like [[Majorana anyons]], in some sense (beware that these modes, being stuck to wires, would not be mobile and hence would not admit [[adiabatic theorem|adiabatic]] [[braiding]] operations in the usual sense, see [here](https://quantumcomputing.stackexchange.com/q/25638/19363)).

These Majorana zero modes were theoretically introduced in a [[spin chain]] [[model (in theoretical physics)|model]] by [Kitaev 2001](#Kitaev01) ("Kitaev spin chain"), argued to be realizable on interfaces of [[superconductors]] with certain [[topological insulators]] by [Fu & Kane 2008](#FuKane08); and their [[experiment|experimental]] realization in [[superconductor|super-]]/[[semiconductor|semi-conducting]] nanowires has been proposed in [Lutchyn, Say & Das Sarma 2010](#LutchynSayDasSarma10), [Oreg, Refael, von Oppen 2010](#OregRefaelvonOppen10).

Following these proposals and especially after [Microsoft Quantum](https://www.microsoft.com/en-us/research/research-area/quantum-computing) (with [QuTech](https://qutech.nl/) at TU Delft) declared ([Nov 2016](https://blogs.microsoft.com/ai/microsoft-doubles-quantum-computing-bet/)) the concrete aim of realizing [[topological quantum computation]] based on topological qbits given by such "Majorana zero modes" (following the plan laid out in [Das Sarma, Freedman & Nayak 15](#DasSarmaFreedmanNayak15)), the topic attracted [enormous attention](https://scholar.google.com/scholar?cites=12195292414684872731&as_sdt=2005&sciodt=0,5&hl=en) in [[solid state physics]].

But prominent claims of detection of Majorana zero modes had to be retracted [in 2021](https://www.nature.com/articles/d41586-021-00612-z) &lbrack;[doi:10.1038/s41586-021-03373-x](https://doi.org/10.1038/s41586-021-03373-x), [doi:10.5281/zenodo.4587841](https://doi.org/10.5281/zenodo.4587841), [doi:10.5281/zenodo.4545812](https://doi.org/10.5281/zenodo.4545812), [TU Delft press release](https://www.delta.tudelft.nl/article/majorana-not-fraud-confirmation-bias#)&rbrack; and again [in 2022](http://retractionwatch.com/2022/04/24/authors-retract-second-majorana-paper-from-nature/) &lbrack;[doi:10.1038/s41586-022-04704-2](https://doi.org/10.1038/s41586-022-04704-2)&rbrack;; and further claims are under criticism, see [Frolov & Mourik 2020](https://doi.org/10.5281/zenodo.6344447), [Das Sarma & Pan 2021](#DasSarmaPan21),[Frolov, Mourik & Zuo 2022](https://doi.org/10.5281/zenodo.6325378) and the extensive list [here](https://twitter.com/spinespresso/status/1503352928656138241). While some researchers now dismiss the whole approach (e.g. [BSSA21](#BSSA21), [p. 3](https://arxiv.org/pdf/2106.11840v4.pdf#page=3)) there is a new claim of detection by [Nayak 22](#Nayak22) & [MicrosoftQuantum 22](#MicrosoftQuantum22) -- but see [Frolov & Mourik 22a](#FrolovMourik22a), [22b](#FrolovMourik22a) and [Frolov 22](#Frolov22).

## References

### General

The general strategy of realizing [[Majorana zero modes]] in supercondocuting/semiconducting nanowires is due to

* {#Kitaev01} [[Alexei Kitaev]], *Unpaired Majorana fermions in quantum wires*,  Physics-Uspekhi, **44** 10S (2001) 131-136 &lbrack;[arXiv:cond-mat/0010440](https://arxiv.org/abs/cond-mat/0010440), [doi:10.1070/1063-7869/44/10S/S29](https://iopscience.iop.org/article/10.1070/1063-7869/44/10S/S29)&rbrack;

* {#FuKane08} [[Liang Fu]], [[Charles Kane]], *Superconducting Proximity Effect and Majorana Fermions at the Surface of a Topological Insulator*, Phys. Rev. Lett. **100** (2008) 096407 &lbrack;[doi:10.1103/PhysRevLett.100.096407](https://doi.org/10.1103/PhysRevLett.100.096407)&rbrack;

* {#LutchynSayDasSarma10} Roman M. Lutchyn, Jay D. Sau, [[Sankar Das Sarma]], *Majorana Fermions and a Topological Phase Transition in Semiconductor-Superconductor Heterostructures*, Phys. Rev. Lett. **105** (2010) 077001 &lbrack;[doi:10.1103/PhysRevLett.105.077001](https://doi.org/10.1103/PhysRevLett.105.077001)&rbrack;  

* {#OregRefaelvonOppen10} Yuval Oreg, Gil Refael, and Felix von Oppen, *Helical Liquids and Majorana Bound States in Quantum Wires*, Phys. Rev. Lett. **105** (2010) 177002 &lbrack;[doi:10.1103/PhysRevLett.105.177002](https://doi.org/10.1103/PhysRevLett.105.177002)&rbrack;

reviewed in:

* Pasquale Marra: *Majorana nanowires for topological quantum computation: A tutorial* &lbrack;[arXiv:2206.14828](https://arxiv.org/abs/2206.14828)&rbrack;

Discussion in the context of [[topological quantum computation]]:

* {#DasSarmaFreedmanNayak15} [[Sankar Das Sarma]], [[Michael Freedman]], [[Chetan Nayak]], *Majorana zero modes and topological quantum computation*, npj Quantum Inf **1** 15001 (2015) $[$[doi:10.1038/npjqi.2015.1](https://doi.org/10.1038/npjqi.2015.1)$]$

General review and experimental status:

* [[Sergey M. Frolov]], *How do we discover MAJORANA PARTICLES in NANOWIRES?*, talk via [ Instituto de Física, Universidade de São Paulo](http://portal.if.usp.br/ifusp/) (May 2021) &lbrack;[video](https://www.youtube.com/watch?v=7btnPqmSh_0)&rbrack;

  > [41:25](https://youtu.be/7btnPqmSh_0?t=2485): No, we have not discovered Majorana particles in nanowires. Yes, we should be able to do it.

See also:

* Wikipedia, *[Majorana bound states](https://en.wikipedia.org/wiki/Majorana_fermion#Majorana_bound_states)*

### Non-Detection 
  {#ReferencesNonDetection}


On the general problem of distinguishing the expected effect from noise:

* {#DasSarmaPan21} [[Sankar Das Sarma]], Haining Pan, *Disorder-induced zero-bias peaks in Majorana nanowires* Phys. Rev. B **103** 195158 (2021) &lbrack;[arXiv:2103.05628](https://arxiv.org/abs/2103.05628), [doi:10.1103/PhysRevB.103.195158](https://doi.org/10.1103/PhysRevB.103.195158)&rbrack;

> we believe that similar confirmation bias applies to many other topological discovery claims in the literature during 2000–2020 where a precise knowledge of what one is looking for has been the key factor in the discovery claim, with the experimental quantization results themselves not being sufficiently compelling. &lbrack;...&rbrack; Our results certainly apply to most of the Majorana experiments during 2012–2021 in the literature.

* {#BSSA21} Koen Bertels, Tamara Sarac, Aritra Sarkar, Imran Ashraf, *Quantum Computing -- from NISQ to PISQ*, IEEE Micro **41** (2021) 24-32 &lbrack;[arXiv:2106.11840v4](https://arxiv.org/abs/2106.11840v4), [doi:10.1109/MM.2021.3099195](https://doi.ieeecomputersociety.org/10.1109/MM.2021.3099195)&rbrack;

> [p. 3](https://arxiv.org/pdf/2106.11840v4.pdf#page=3): The quantum physics community is sufficiently aware that when certain qubit technologies do not produce any reasonable result after several years of effort, they should be gently removed from the list of quantum candidates. After working with the physics colleagues in Delft, we saw that happening with the Majorana qubits that could not be confirmed in any follow-up experiment.

* {#FrolovMourik22a} [[Sergey M. Frolov]], [[Vincent Mourik]], *We cannot believe we overlooked these Majorana discoveries* &lbrack;[arXiv:2203.17060](https://arxiv.org/abs/2203.17060), [doi:10.5281/zenodo.6364928](https://doi.org/10.5281/zenodo.6364928), conclusion on: [p. 7](https://arxiv.org/ftp/arxiv/papers/2203/2203.17060.pdf#page=7)&rbrack;


Non-retracted claims of experimental realization of something in the direction of Majorana zero modes:

* {#MMBDRSC19} Gerbold C. Ménard, Andrej Mesaros, Christophe Brun, François Debontridder, Dimitri Roditchev, Pascal Simon, Tristan Cren, *Isolated pairs of Majorana zero modes in a disordered superconducting lead monolayer*,  Nat Commun **10** 2587 (2019) $[$[doi:10.1038/s41467-019-10397-5](https://doi.org/10.1038/s41467-019-10397-5)$]$

* {#Nayak22} [[Chetan Nayak]], *Microsoft has demonstrated the underlying physics required to create a new kind of qubit*, Microsoft Research Blog (March 2022)

* {#MicrosoftQuantum22} [Microsoft Quantum](https://www.microsoft.com/en-us/research/research-area/quantum-computing), *InAs-Al Hybrid Devices Passing the Topological Gap Protocol* &lbrack;[arXiv:2207.02472](https://arxiv.org/abs/2207.02472), [video presentation](https://www.microsoft.com/en-us/research/video/inas-al-hybrid-devices-passing-the-topological-gap-protocol/)&rbrack;

but see commentary in:

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



[[!redirects Majorana zero modes]]

[[!redirects Kitaev spin chain]]
[[!redirects Kitaev spin chains]]
