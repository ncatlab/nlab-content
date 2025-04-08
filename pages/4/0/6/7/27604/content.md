
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

The origin of the attention paid to the [[normalizer subgroup]] of the [[Pauli group]] inside the [[unitary group]] is (p 5 of):

* {#Gottesman98} [[Daniel Gottesman]]: *A Theory of Fault-Tolerant Quantum Computation*, Phys. Rev. A **57** (1998) 127 &lbrack;[arXiv:quant-ph/9702029](https://arxiv.org/abs/quant-ph/9702029), [doi:10.1103/PhysRevA.57.127](https://doi.org/10.1103/PhysRevA.57.127)&rbrack;

Contrary to common claims, the term "Clifford group" for this normalizer subgroup seems to have emerged only in the following years.

Review:

* J. Tolar: *On Clifford groups in quantum computing*, J. Phys.: Conf. Series **1071** (2018) 012022 &lbrack;[arXiv:1810.10259](https://arxiv.org/abs/1810.10259), [doi:10.1088/1742-6596/1071/1/012022](https://doi.org/10.1088/1742-6596/1071/1/012022)&rbrack;

* Kieran Mastel: *The Clifford theory of the $n$-qubit Clifford group* &lbrack;[arXiv:2307.05810](https://arxiv.org/abs/2307.05810)&rbrack;

See also: 

* Wikipedia: *[Clifford group](https://en.wikipedia.org/wiki/Clifford_group)*

* Wikipedia: *[Gottesman-Knill theorem](https://en.wikipedia.org/wiki/Gottesman%E2%80%93Knill_theorem)*

* Daniel Grier, Luke Schaeffer: *The Classification of Clifford Gates over Qubits*, Quantum **6** (2022) 734 &lbrack;[arXiv:1603.03999](https://arxiv.org/abs/1603.03999), [doi:10.22331/q-2022-06-13-734](https://doi.org/10.22331/q-2022-06-13-734)&rbrack;

* George Biswas: *Exploring Classical Simulation of Quantum Circuits of Clifford Gates through Simple Examples and Intuitive Insights* &lbrack;[arXiv:2405.13590](https://arxiv.org/abs/2405.13590)&rbrack;


[[!redirects Clifford groups]]

[[!redirects Gottesman-Knill theorem]]
