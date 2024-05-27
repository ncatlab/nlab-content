

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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


#Contents#
* table of contents
{:toc}

## Idea

In [[solid state physics]], many or all [[anyon]]-species of (potential) practical interest (such as for [[topological quantum computation]]) are thought to be characterized by [[affine Lie algebras]] $\widehat{\mathfrak{g}}^k$ (at some [[level (Chern-Simons theory)|level]] $k$), in that their [[wavefunctions]] are, essentially, $\widehat{g}$-[[conformal blocks]] and their [[braid group representation|braiding]] is described by $G$-[[Chern-Simons theory]] at [[level (Chern-Simons theory)|level]] $k$ (possibly fractional, see at *[[logarithmic CFT]]* [here](logarithmic+CFT#FractionalLevelWZWModelReferences)).

If here $\mathfrak{g} = $ [[su(2)|$\mathfrak{su}(2)$]], then one also speaks of "SU(2)-anyons" (with varying conventions on capitalization, etc.). 
With "Majorana anyons" ($k = 2$) and "Fibonacci anyons" ($k = 3$) this class subsumes most or all anyon species which seem to have a realistic chance of existing in nature. 

{#NonRealizationOfMZZInNanowires} Notably [[Majorana anyons]] (in the guise of "[[Majorana zero modes]]" in super/semi-conducting nanowires) are (or were until recently, see [arXiv:2106.11840v4](https://arxiv.org/abs/2106.11840v4), [p. 3](https://arxiv.org/pdf/2106.11840v4.pdf#page=3)) at the focus of attention of an intense effort to finally provide a practical proof of principle for the old idea of [[topological quantum computation]] (following the plan laid out in [Das Sarma, Freedman & Nayak 15](#DasSarmaFreedmanNayak15)). After initial claims had to be retracted [in 2021](https://www.nature.com/articles/d41586-021-00612-z) &lbrack;[doi:10.1038/s41586-021-03373-x](https://doi.org/10.1038/s41586-021-03373-x), [doi:10.5281/zenodo.4587841](https://doi.org/10.5281/zenodo.4587841), [doi:10.5281/zenodo.4545812](https://doi.org/10.5281/zenodo.4545812), [TU Delft press release](https://www.delta.tudelft.nl/article/majorana-not-fraud-confirmation-bias#)&rbrack; and again [in 2022](http://retractionwatch.com/2022/04/24/authors-retract-second-majorana-paper-from-nature/) &lbrack;[doi:10.1038/s41586-022-04704-2](https://doi.org/10.1038/s41586-022-04704-2)&rbrack; (further claims are under criticism, see e.g. [doi:10.5281/zenodo.6344447](https://doi.org/10.5281/zenodo.6344447), [doi:10.5281/zenodo.6325378](https://doi.org/10.5281/zenodo.6325378) and the list [here](https://twitter.com/spinespresso/status/1503352928656138241)) there is a new claim of detection by [Nayak 22](#Nayak22) & [MicrosoftQuantum 22](#MicrosoftQuantum22), but see [Frolov & Mourik 22a](#FrolovMourik22a), [22b](#FrolovMourik22a) and [Frolov 22](#Frolov22).

In any case, Majorana anyons are known not to be universal (not all [[quantum gates]] may be approximated with Majorana braiding). The simplest universal $\mathfrak{su}(2)$-anyon species are the Fibonacci anyons at [[level (Chern-Simons theory)|level]] $k = 3$ (e.g. [Simeon 2021](#Simeon21), also [Kolganov, Mironov & Morozon (2023)](#KolganovMironovMorozon23)).

## Related concepts

* [[parafermion]]

* [[Majorana dimer]]

## References

### General

Early consideration of $\mathfrak{su}(2)$-anyons is *implicit*  in the context of [[Laughlin wavefunctions]] due to

* {#ReadRezayi99} [[Nicholas Read]], [[Edward Rezayi]], *Beyond paired quantum Hall states: Parafermions and incompressible states in the first excited Landau level*, Phys. Rev. B **59** (1999) 8084 $[$[doi:10.1103/PhysRevB.59.8084](https://doi.org/10.1103/PhysRevB.59.8084)$]$

Early discussion of [[topological quantum computation]] in $SU(2)$-[[Chern-Simons theory]]:

* {#FreedmanKitaevLarsenWang03} [[Michael Freedman]], [[Alexei Kitaev]], [[Michael Larsen]], [[Zhenghan Wang]], *Topological quantum computation*,  Bull. Amer. Math. Soc. __40__ (2003), 31-38 ([arXiv:quant-ph/0101025](https://arxiv.org/abs/quant-ph/0101025), [doi:10.1090/S0273-0979-02-00964-3](https://doi.org/10.1090/S0273-0979-02-00964-3), [pdf](http://www.ams.org/journals/bull/2003-40-01/S0273-0979-02-00964-3/S0273-0979-02-00964-3.pdf))

* [[Michael Freedman]], [[Michael Larsen]], [[Zhenghan Wang]], _A modular functor which is universal for quantum computation_, Communications in Mathematical Physics. 2002, Vol 227, Num 3, pp 605-622  ([arXiv:quant-ph/0001108](http://arxiv.org/abs/quant-ph/0001108))

More concrete discussion of these phenomena in terms of [[anyons]]:

* [[Simon Trebst]], [[Matthias Troyer]], [[Zhenghan Wang]], A. W. W. Ludwig, *A short introduction to Fibonacci anyon models*, Prog. Theor. Phys. Supp. **176** 384 (2008) &lbrack;[arXiv:0902.3275](https://arxiv.org/abs/0902.3275), [doi:10.1143/PTPS.176.384](https://doi.org/10.1143/PTPS.176.384)&rbrack;

* C. Gils, E. Ardonne, [[Simon Trebst]], D. A. Huse, A. W. W. Ludwig, [[Matthias Troyer]], [[Zhenghan Wang]],  *Anyonic quantum spin chains: Spin-1 generalizations and topological stability*, Phys. Rev. B **87** (2013), 235120
&lbrack;[doi:10.1103/PhysRevB.87.235120](https://doi.org/10.1103/PhysRevB.87.235120), [arXiv:1303.4290](https://arxiv.org/abs/1303.4290)&rbrack;

* {#DasSarmaFreedmanNayak15} [[Sankar Das Sarma]], [[Michael Freedman]], [[Chetan Nayak]], *Majorana zero modes and topological quantum computation*, npj Quantum Inf **1** 15001 (2015) &lbrack;[doi:10.1038/npjqi.2015.1](https://doi.org/10.1038/npjqi.2015.1)&rbrack;

*  [[Emil Génetay-Johansen]], [[Tapio Simula]], *Fibonacci anyons versus Majorana fermions -- A Monte Carlo Approach to the Compilation of Braid Circuits in $SU(2)_k$ Anyon Models*, PRX Quantum **2** 010334 (2021) &lbrack;[arXiv:2008.10790](https://arxiv.org/abs/2008.10790), [doi:10.1103/PRXQuantum.2.010334](https://doi.org/10.1103/PRXQuantum.2.010334)&rbrack;

Discussion of Fibonacci anyons:

* {#Simeon21} Ryan Simeon, *Universality of Fibonacci anyons in topological quantum computing* (2021) &lbrack;[pdf](https://homes.psd.uchicago.edu/~sethi/Teaching/P243-W2021/Final%20Papers/Simeon-PHYS243_final.pdf), [[Simeon-UniversalityOfFibonacciAnyons.pdf:file]]&rbrack;

Discussion of universality at higher [[Chern-Simons level|level]] $k$ (and also for $SU(N)$-anyons with $N \gt 2$):

* {#KolganovMironovMorozon23} [[Nikita Kolganov]], [[Sergey Mironov]], [[Andrey Morozov]], *Large $k$ topological quantum computer*, Nuclear Physics B
**987** (2023) 116072 &lbrack;[arXiv:2105.03980](https://arxiv.org/abs/2105.03980), [doi:10.1016/j.nuclphysb.2023.116072](https://doi.org/10.1016/j.nuclphysb.2023.116072)&rbrack;



### Experimental realization


#### (Non-)Observation of Majorana zero modes

The general strategy of realizing [[Majorana zero modes]] in supercondocuting/semiconducting nanowires is due to

* [[Alexei Kitaev]], *Unpaired Majorana fermions in quantum wires*,  Physics-Uspekhi, **44** 10S (2001) 131-136 &lbrack;[doi:10.1070/1063-7869/44/10S/S29](https://iopscience.iop.org/article/10.1070/1063-7869/44/10S/S29)&rbrack;

* Roman M. Lutchyn, Jay D. Sau, [[Sankar Das Sarma]], *Majorana Fermions and a Topological Phase Transition in Semiconductor-Superconductor Heterostructures*, Phys. Rev. Lett. **105** (2010) 077001 &lbrack;[doi:10.1103/PhysRevLett.105.077001](https://doi.org/10.1103/PhysRevLett.105.077001)&rbrack;  

* Yuval Oreg, Gil Refael, and Felix von Oppen, *Helical Liquids and Majorana Bound States in Quantum Wires*, Phys. Rev. Lett. **105** (2010) 177002 &lbrack;[doi:10.1103/PhysRevLett.105.177002](https://doi.org/10.1103/PhysRevLett.105.177002)&rbrack;

reviewed in:

* Pasquale Marra: *Majorana nanowires for topological quantum computation: A tutorial* &lbrack;[arXiv:2206.14828](https://arxiv.org/abs/2206.14828)&rbrack;


On the general problem of distinguishing the expected effect from noise:

* [[Sankar Das Sarma]], Haining Pan, *Disorder-induced zero-bias peaks in Majorana nanowires* Phys. Rev. B **103** 195158 (2021) &lbrack;[arXiv:2103.05628](https://arxiv.org/abs/2103.05628), [doi:10.1103/PhysRevB.103.195158](https://doi.org/10.1103/PhysRevB.103.195158)&rbrack;

> we believe that similar confirmation bias applies to many other topological discovery claims in the literature during 2000–2020 where a precise knowledge of what one is looking for has been the key factor in the discovery claim, with the experimental quantization results themselves not being sufficiently compelling. &lbrack;...&rbrack; Our results certainly apply to most of the Majorana experiments during 2012–2021 in the literature.


Non-retracted claims of experimental realization of something in the direction of Majorana zero modes:

* {#MMBDRSC19} Gerbold C. Ménard, Andrej Mesaros, Christophe Brun, François Debontridder, Dimitri Roditchev, Pascal Simon, Tristan Cren, *Isolated pairs of Majorana zero modes in a disordered superconducting lead monolayer*,  Nat Commun **10** 2587 (2019) $[$[doi:10.1038/s41467-019-10397-5](https://doi.org/10.1038/s41467-019-10397-5)$]$

* {#Nayak22} [[Chetan Nayak]], *Microsoft has demonstrated the underlying physics required to create a new kind of qubit*, Microsoft Research Blog (March 2022)

* {#MicrosoftQuantum22} Microsoft Quantum, *InAs-Al Hybrid Devices Passing the Topological Gap Protocol* &lbrack;[arXiv:2207.02472](https://arxiv.org/abs/2207.02472)&rbrack;

but see commentary in:

* {#FrolovMourik22a} [[Sergey M. Frolov]], [[Vincent Mourik]], *We cannot believe we overlooked these Majorana discoveries* &lbrack;[arXiv:2203.17060](https://arxiv.org/abs/2203.17060), [doi:10.5281/zenodo.6364928](https://doi.org/10.5281/zenodo.6364928), conclusion on: [p. 7](https://arxiv.org/ftp/arxiv/papers/2203/2203.17060.pdf#page=7)&rbrack;

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

#### Other

Proposal to realize [[Fibonacci anyons]] on [[quasicrystal]]-states:

* Marcelo Amaral, [[David Chester]], Fang Fang, Klee Irwin, *Exploiting Anyonic Behavior of Quasicrystals for Topological Quantum Computing*, Symmetry **14** 9 (2022) 1780 &lbrack;[arXiv:2207.08928](https://arxiv.org/abs/2207.08928), [doi:10.3390/sym14091780](https://doi.org/10.3390/sym14091780)&rbrack;


\linebreak




[[!include Laughlin wavefunctions as conformal blocks -- references]]





[[!redirects su(2)-anyons]]

[[!redirects SU(2)-anyon]]
[[!redirects SU(2)-anyons]]

[[!redirects su2-anyon]]
[[!redirects su2-anyons]]

[[!redirects Majorana anyon]]
[[!redirects Majorana anyons]]


[[!redirects Fibonacci anyon]]
[[!redirects Fibonacci anyons]]


[[!redirects Ising anyon]]
[[!redirects Ising anyons]]

