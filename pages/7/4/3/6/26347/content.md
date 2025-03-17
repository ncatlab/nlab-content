
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

By "quantum simulation" one broadly means the simulation *of* [[quantum systems]]. The term is used in two rather different ways:

1. Without further qualification, "quantum simulation" typically refers to the simulation of (complicated) quantum systems appearing in nature, such as (large) [[molecules]], *by* other (more controllable) quantum systems, notably by [[quantum computers]] (cf. *[[quantum chemistry]]*).

1. *Classical* quantum simulation refers to the simulation of [[quantum computers]] themselves by classical computers, such as for testing ([[software verification|verifying]]) [[quantum circuit]]-designs and more generally for testing [[quantum programming language|quantum programs]] and [[quantum computing]]-architectures.

## Related concepts

* [[quantum computing]]

* [[quantum sensing]]

* [[quantum communication]]

* [[quantum information]]


## References


### Quantum simulation by quantum systems

General discussion:

* Tomi H Johnson, Stephen R Clark, Dieter Jaksch, *What is a quantum simulator?*, EPJ Quantum Technol. **1** 10 (2014) &lbrack;[doi:10.1140/epjqt10](https://doi.org/10.1140/epjqt10)&rbrack;

* I. M. Georgescu, S. Ashhab, Franco Nori, *Quantum Simulation*, Rev. Mod. Phys. **86** 154 (2014) &lbrack;[arXiv:1308.6253](https://arxiv.org/abs/1308.6253), [doi:10.1103/RevModPhys.86.153](https://doi.org/10.1103/RevModPhys.86.153)&rbrack;

See also:

* Wikipedia, *[Quantum simulator](https://en.wikipedia.org/wiki/Quantum_simulator)*

Quantum simulation on [[trapped-ion quantum computing|trapped-ion quantum hardware]]:

* Michael Foss-Feig, Guido Pagano, Andrew C. Potter, Norman Y. Yao: *Progress in Trapped-Ion Quantum Simulation*, Annual Reviews of Condensed Matter Physics (2024) &lbrack;[arXiv:2409.02990](https://arxiv.org/abs/2409.02990)&rbrack;

On quantum simulation of the [[Dirac equation]]:

* L. Lamata, J. León, T. Schätz, [[Enrique Solano]]: *Dirac Equation and Quantum Relativistic Effects in a Single Trapped Ion*, Phys. Rev. Lett. **98** 253005 (2007) &lbrack;[doi:10.1103/PhysRevLett.98.253005](https://doi.org/10.1103/PhysRevLett.98.253005)&rbrack;

* R. Gerritsma, G. Kirchmair, F. Zähringer, [[Enrique Solano]], R. Blatt & C. F. Roos: *Quantum simulation of the Dirac equation*, Nature **463** 68–71 (2010) &lbrack;[doi:10.1038/nature08688](https://doi.org/10.1038/nature08688)&rbrack;


On quantum simulation of ([[lattice QFT|lattice]]) [[quantum field theory]]:

* [[John Preskill]], *Simulating quantum field theory with a quantum computer*, 36th Annual International Symposium on Lattice Field Theory, PoS **334** (2019) &lbrack;[doi:10.22323/1.334.0024](https://doi.org/10.22323/1.334.0024), 
[arXiv:1811.10085](https://arxiv.org/abs/1811.10085)&rbrack;

* Jad C. Halimeh, Masanori Hanada, Shunji Matsuura, Franco Nori, Enrico Rinaldi, Andreas Schäfer: *A universal framework for the quantum simulation of Yang-Mills theory* &lbrack;[arXiv:2411.13161](https://arxiv.org/abs/2411.13161)&rbrack;



specifically of  [[scattering amplitudes]] of [[bound states]]:

* Matteo Turco, Gonçalo M. Quinta, João Seixas, Yasser Omar, *Towards Quantum Simulation of Bound States Scattering* &lbrack;[arXiv:2305.07692](https://arxiv.org/abs/2305.07692)&rbrack;

{#OfAnyons} On quantum simulation of [[anyons]]:

* T. Andersen et al.: *Non-Abelian braiding of graph vertices in a superconducting processor*, Nature **618** (2023) 264–269 \[<a href="https://arxiv.org/abs/2210.10255">arXiv:2210.10255</a>, [doi:10.1038/s41586-023-05954-4](https://doi.org/10.1038/s41586-023-05954-4)\]

* Daniel Nigg, Markus Mueller, Esteban A. Martinez, Philipp Schindler, Markus Hennrich, Thomas Monz, Miguel A. Martin-Delgado, Rainer Blatt:
  *Experimental Quantum Computations on a Topologically Encoded Qubit*, Science **345** 6194 (2014) 302-305 &lbrack;[arXiv:1403.5426](https://arxiv.org/abs/1403.5426), [doi:10.1126/science.1253742](https://science.sciencemag.org/content/345/6194/302)&rbrack;

* [[Mohsin Iqbal]], [[Nathanan Tantivasadakarn]]: *Topological Order from Measurements and Feed-Forward on a Trapped Ion Quantum Computer*, Nature Communications Physics **7** (2024) 205 \[<a href="https://doi.org/10.1038/s42005-024-01698-3">doi:10.1038/s42005-024-01698-3</a>, [arXiv:2302.01917](https://arxiv.org/abs/2302.01917)\]

* [[Mohsin Iqbal]], [[Nathanan Tantivasadakarn]], R. Verresen et al., Figure 5 in : *Non-Abelian topological order and anyons on a trapped-ion processor*, Nature **626** (2024) 505–511 \[<a href="https://doi.org/10.1038/s41586-023-06934-4">doi:10.1038/s41586-023-06934-4</a>\]

  Nature research briefing: *Topological matter created on a quantum chip produces quasiparticles with computing power* \[<a href="https://doi.org/10.1038/d41586-023-04126-8">doi:10.1038/d41586-023-04126-8</a>\]
  
On [[quantum advantage]] for quantum simulation of the [[Schrödinger equation]]:

* Andrew D. King et al.: *Beyond-classical computation in quantum simulation*, Science
(Mar 2025) &lbrack;[doi:10.1126/science.ad6285](https://doi.org/10.1126/science.ado6285)&rbrack;


### Quantum simulation by classical systems

* Yongshan Ding, Frederic T. Chong, *Classical Simulation of Quantum Computation*, in: *Quantum Computer Systems*, Synthesis Lectures on Computer Architecture. Springer (2020) &lbrack;[doi:10.1007/978-3-031-01765-0_9](https://doi.org/10.1007/978-3-031-01765-0_9)&rbrack;

* Ya-Qian Zhao, Ren-Gang Li, Jin-Zhe Jiang, Chen Li, Hong-Zhen Li, En-Dong Wang, Wei-Feng Gong, Xin Zhang, Zhi-Qiang Wei, *Simulation of Quantum Computing on Classical Supercomputers*, Phys. Rev. A **104** 032603 (2021) &lbrack;[arXiv:2010.14962](https://arxiv.org/abs/2010.14962), [doi:10.1103/PhysRevA.104.032603](https://doi.org/10.1103/PhysRevA.104.032603)&rbrack;

* Robert Willie, *Classical simulation of quantum circuits* (2022) &lbrack;[pdf](https://www.cda.cit.tum.de/files/eda/2022_oag_classical_simulation_of_quantum_circuits.pdf)&rbrack;

* Xiaosi Xu, Simon Benjamin, Jinzhao Sun, Xiao Yuan, Pan Zhang, *A Herculean task: Classical simulation of quantum computers* &lbrack;[arXiv:2302.08880](https://arxiv.org/abs/2302.08880)&rbrack;

* Kieran Young, Marcus Scese, Ali Ebnenasir, *Simulating Quantum Computations on Classical Machines: A Survey* &lbrack;[arXiv:2311.16505](https://arxiv.org/abs/2311.16505)&rbrack;



See also:

* IONQ: *[The Value of Classical Quantum Simulators](https://ionq.com/resources/the-value-of-classical-quantum-simulators)*

[[!redirects quantum simulations]]

[[!redirects quantum simulator]]
[[!redirects quantum simulators]]
