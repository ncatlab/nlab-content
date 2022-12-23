
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
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

Given a [[finitely generated group|finitely generated]] and [[dense subspace|dense]] [[subgroup]] $\langle g_1, g_1^{-1} \cdots, g_n, g_n^{-1} \rangle$ of the [[topological group]] [[SU(2)]], the *Solovay-Kitaev theorem* gives a bound on the length of sequences of [[elements]] from $\{g_1, \cdots, g_n\}$ which are needed in order to approximate any given element $g \,\in\, SU(2)$ to given accuracy.

In [[quantum computation]]-theory one interprets:

1. the set $\{g_0, \cdots, g_n\}$ as a given set of (operations of) [[quantum gates]] on [[qbits]]

   (that the subgroup these generate is [[dense subspace|dense]] in [[SU(2)]] is said to mean that this is a *universal set* of quantum gates);

1. the target element $g \,\in\, SU(2)$ as an intended operation on qbits (an intended quantum program);

1. the sequence of elements $g_i$ used to approximate $g$ as a [[quantum circuit]] realizing the quantum program,

and then the Solovay-Kitaev theorem guarantees that the maximum *depth* of the quantum circuit grows only slowly with its required accuracy.

(...)


## References

Original announcements:

* [[Robert Solovay]], *Lie Groups and Quantum Circuits*, talk at MSRI (2000) &lbrack;[webpage](https://www.msri.org/workshops/189/schedules/12826)&rbrack;


* [[Alexei Kitaev]],  *Quantum computations: algorithms and error correction*, Russian Mathematical Surveys, **52** 6 (1997) &lbrack;[doi:10.1070/RM1997v052n06ABEH002155](https://iopscience.iop.org/article/10.1070/RM1997v052n06ABEH002155), <a href="https://ochicken.top/Library/Physics/Quantum_Computation_and_Quantum_Information/1997.06%20A.Yu.Kitaev_%20Quantum%20computations_%20algorithms%20and%20error%20correction%20(kitaev1997).pdf">pdf</a>&rbrack;


Review:

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], *Solovay-Kitaev theorem*,  Appendix 3 of: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

* [[Christopher M. Dawson]], [[Michael A. Nielsen]], *The Solovay-Kitaev algorithm*, Quantum Information & Computation **6** 1 (2006) 81–95 &lbrack;[arXiv:quant-ph/0505030](https://arxiv.org/abs/quant-ph/0505030), [doi:10.5555/2011679.2011685](https://dl.acm.org/doi/10.5555/2011679.2011685)&rbrack;



See also:

* Wikipedia, *[Solovay-Kitaev theorem](https://en.wikipedia.org/wiki/Solovay%E2%80%93Kitaev_theorem)*


