
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


> This entry is about the notion in [[quantum information theory]]. For subgroups of a [[Clifford algebra]] see instead there.


\tableofcontents


## Idea


In [[quantum information theory]], by the *Clifford group* on $n$-[[qbits]] (for $n \in \mathbb{N}_{\geq 1}$) one means the [[normalizer subgroup]], inside the [[unitary group]] $U(2n)$, of the group of $n$fold $\mathbb{C}$-[[tensor products]] of [[linear operators]] from the [[Pauli group]].

An [[element]] of the Clifford group, understood as a [[unitary operator]] on the [[finite-dimensional Hilbert space]] $\mathbb{C}^{2n}$, is also called a *Clifford [[quantum gate]]* or just *Clifford gate*, for short.

The [[Gottesman-Knill theorem]] states that [[quantum circuits]] which are built only from Clifford gates ("stabilizer circuits") may be efficiently [[quantum simulation|simulated]] on [[classical computers]]. Conversely this means that for a [[quantum computer]] to exhibit [[quantum advantage]] it must realize [[quantum gates]] which are non-Clifford gates.


## References

### General

The origin of the attention paid to the [[normalizer subgroup]] of the [[Pauli group]] inside the [[unitary group]] is (p 5 of):

* {#Gottesman98} [[Daniel Gottesman]]: *A Theory of Fault-Tolerant Quantum Computation*, Phys. Rev. A **57** (1998) 127 &lbrack;[arXiv:quant-ph/9702029](https://arxiv.org/abs/quant-ph/9702029), [doi:10.1103/PhysRevA.57.127](https://doi.org/10.1103/PhysRevA.57.127)&rbrack;

Contrary to common claims, the term "Clifford group" for this normalizer subgroup seems to have emerged only in the following years.

Review:

* Jiri Tolar: *On Clifford groups in quantum computing*, J. Phys.: Conf. Series **1071** (2018) 012022 &lbrack;[arXiv:1810.10259](https://arxiv.org/abs/1810.10259), [doi:10.1088/1742-6596/1071/1/012022](https://doi.org/10.1088/1742-6596/1071/1/012022)&rbrack;

* Kieran Mastel: *The Clifford theory of the $n$-qubit Clifford group* &lbrack;[arXiv:2307.05810](https://arxiv.org/abs/2307.05810)&rbrack;

See also: 

* Wikipedia: *[Clifford group](https://en.wikipedia.org/wiki/Clifford_group)*

* Wikipedia: *[Gottesman-Knill theorem](https://en.wikipedia.org/wiki/Gottesman%E2%80%93Knill_theorem)*

* Daniel Grier, Luke Schaeffer: *The Classification of Clifford Gates over Qubits*, Quantum **6** (2022) 734 &lbrack;[arXiv:1603.03999](https://arxiv.org/abs/1603.03999), [doi:10.22331/q-2022-06-13-734](https://doi.org/10.22331/q-2022-06-13-734)&rbrack;

* George Biswas: *Exploring Classical Simulation of Quantum Circuits of Clifford Gates through Simple Examples and Intuitive Insights* &lbrack;[arXiv:2405.13590](https://arxiv.org/abs/2405.13590)&rbrack;


### Realizing protected non-Clifford gates
 {#RealizingNonCliffordGates}

The practical issue of realizing fault-tolerant non-Clifford gates (either via [[quantum error correction]] or via [[topological quantum computing|topological error protection]]):

* Marek Narożniak et al.: *Quantum gates for Majoranas zero modes in topological superconductors in one-dimensional geometry*, Phys. Rev. B **103** (2021) 205429 &lbrack;[doi:10.1103/PhysRevB.103.205429](https://doi.org/10.1103/PhysRevB.103.205429)&rbrack;

* Ali Hamed Safwan, Raditya Weda Bomantara: *Generating non-Clifford gate operations through exact mapping between Majorana fermions and $\mathbb{Z}_4$ parafermions* &lbrack;[arXiv:2411.18736](https://arxiv.org/abs/2411.18736)&rbrack;

* Wang Yifei et al.: *Efficient fault-tolerant implementations of non-Clifford gates with reconfigurable atom arrays*, npj Quantum Information **10** 136 (2024) &lbrack;[doi:10.1038/s41534-024-00945-3](https://doi.org/10.1038/s41534-024-00945-3)&rbrack;

* Louis Golowich: *Improved Fault-Tolerant Non-Clifford Gates (or: How to Multiply Quantumly)*, talk at IAS (March 03, 2025) &lbrack;[ias.edu](https://www.ias.edu/video/improved-fault-tolerant-non-clifford-gates-or-how-multiply-quantumly), [youtu.be](https://youtu.be/0laX71DNUrg)&rbrack;

* Margarita Davydova et al.: *Universal fault tolerant quantum computation in 2D without getting tied in knots* &lbrack;[arXiv:2503.15751](https://arxiv.org/abs/2503.15751)&rbrack;  

* Microsoft Quantum: *Non-Clifford operations*, appendix D of: *Roadmap to fault tolerant quantum computation using topological qubit arrays* &lbrack;[arXiv:2502.12252](https://arxiv.org/abs/2502.12252), [inSpire:2890977](https://inspirehep.net/literature/2890977)&rbrack;



[[!redirects Clifford groups]]

[[!redirects Gottesman-Knill theorem]]

[[!redirects Clifford gate]]
[[!redirects Clifford gates]]
