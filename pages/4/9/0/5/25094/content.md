
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

Given a [[finitely generated group|finitely generated]] and [[dense subspace|dense]] [[subgroup]] $\langle g_1, g_1^{-1} \cdots, g_n, g_n^{-1} \rangle$ of the [[topological group]] [[SU(2)]], the *Solovay-Kitaev theorem* &lbrack;[Kitaev (1997)](#Kitaev97), [Nielsen & Chuang (2000, §A3)](#NielsenChuang00)&rbrack; gives a strong bound on the length of sequences of [[elements]] from $\{g_1, \cdots, g_n\}$ which are needed in order to approximate any given element $g \,\in\, SU(2)$ to given accuracy.

In [[quantum computation]]-theory one interprets:

1. the set $\{g_0, \cdots, g_n\}$ as a given set of (operations of) [[quantum gates]] on [[qbits]]

   (that the subgroup these generate is [[dense subspace|dense]] in [[SU(2)]] is said to mean that this is a *universal set* of quantum gates);

1. the target element $g \,\in\, SU(2)$ as an intended operation on qbits (an intended quantum program);

1. the sequence of elements $g_i$ used to approximate $g$ as a [[quantum circuit]] realizing the quantum program ("quantum compilation"),

and then the Solovay-Kitaev theorem guarantees that the maximum *depth* of the quantum circuit grows only slowly with its required accuracy.

In fact, the theorem holds in the generality of [[SU(n)|$SU(d)$]], $d \in \mathbb{N}_{\geq 1}$, which in terms of [[quantum computation]] corresponds to working with *[[qdits]]* instead of just [[qbits]].

Regarding the practical relevance, it has been argued &lbrack;[MO:a/22197](https://quantumcomputing.stackexchange.com/a/22197/19363)&rbrack; that [[quantum computing]]-hardware such as based on [[superconductors]] will already allow to approximate any operation on a "physical qbit" by a single [[quantum gate]], but that for such hardware the Solovay-Kitaev theorem is still relevant on the level of "[[logical qbits]]", i.e. taking [[quantum error correction]] into account.

Similarly, in [[topological quantum computation]] the available set of basic [[anyon]] [[braiding|braid gates]] is highly constrained and the Solovay-Kitaev algorithm is used for "topological quantum compilation" (e.g. [Bonesteel, Hormozi, Zikos & Simon (2005)](#BonesteelHormoziZikosSimon05), [Hormozi, Zikos, Bonesteel & Simon (2007)](#HormoziZikosBonesteelSimon07), [Hormozi, Bonesteel & Simon (2009)](#HormoziBonesteelSimon09))



## References

### General

According to [Dawson & Nielsen (2006, p. 13)](#DawsonNielsen06) the first announcement of the theorem was 

* "by [[Robert Solovay|Solovay]] in 1995 on an email discussion list".

A proof was then outlined in:

* {#Kitaev97} [[Alexei Kitaev]],  *Quantum computations: algorithms and error correction*, Russian Mathematical Surveys, **52** 6 (1997) &lbrack;[doi:10.1070/RM1997v052n06ABEH002155](https://iopscience.iop.org/article/10.1070/RM1997v052n06ABEH002155), <a href="https://ochicken.top/Library/Physics/Quantum_Computation_and_Quantum_Information/1997.06%20A.Yu.Kitaev_%20Quantum%20computations_%20algorithms%20and%20error%20correction%20(kitaev1997).pdf">pdf</a>&rbrack;

followed by talk announcement:

* {#Solovay00} [[Robert Solovay]], *Lie Groups and Quantum Circuits*, talk at MSRI (2000) &lbrack;[webpage](https://www.msri.org/workshops/189/schedules/12826), [mp4](https://s3-us-west-1.amazonaws.com/msri-videos/paperclip/videos/data/000/049/315/original/189-12826-Lie_Groups_and_Quantum_Circuits-Robert_Solovay.mp4)&rbrack;


Following [Kitaev (1997)](#Kitaev97), a full proof was spelled out in:

* {#NielsenChuang00} [[Michael A. Nielsen]], [[Isaac L. Chuang]], *Solovay-Kitaev theorem*,  Appendix 3 of: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

Review:

* {#KitaevShenVyalyi02} [[Alexei Kitaev]], A. H. Shen, M. N. Vyalyi, §8.3 in: *Classical and Quantum Computation*, Graduate Studies in Mathematics **47**, Amer. Math. Soc. (2002) &lbrack;[doi:10.1090/gsm/047](http://dx.doi.org/10.1090/gsm/047)&rbrack;

* {#DawsonNielsen06} [[Christopher M. Dawson]], [[Michael A. Nielsen]], *The Solovay-Kitaev algorithm*, Quantum Information & Computation **6** 1 (2006) 81–95 &lbrack;[arXiv:quant-ph/0505030](https://arxiv.org/abs/quant-ph/0505030), [doi:10.5555/2011679.2011685](https://dl.acm.org/doi/10.5555/2011679.2011685)&rbrack;

See also:

* Wikipedia, *[Solovay-Kitaev theorem](https://en.wikipedia.org/wiki/Solovay%E2%80%93Kitaev_theorem)*

* Maris Ozols, *The Solovay-Kitaev theorem* &lbrack;[pdf](http://home.lu.lv/~sd20008/papers/essays/Solovay-Kitaev.pdf)&rbrack;

Further refinement of the algorithm:

* Attila B. Nagy, *On an implementation of the Solovay-Kitaev algorithm*, 10th Rhine Workshop on Computer Algebra &lbrack;[arXiv:quant-ph/0606077](https://arxiv.org/abs/quant-ph/0606077)&rbrack;


### In topological quantum computation
 {#ReferencesInTopologicalQuantumComputation}

Discussion of the Solovay-Kitaev theorem in the context of [[topological quantum computation]]:

* {#BonesteelHormoziZikosSimon05} [[Nicholas E. Bonesteel]], [[Layla Hormozi]], [[Georgios Zikos]], [[Steven H. Simon]], *Braid Topologies for Quantum Computation*, Phys. Rev. Lett. **95** 140503 (2005) $[$[arXiv:quant-ph/0505065](https://arxiv.org/abs/quant-ph/0505065), [doi:10.1103/PhysRevLett.95.140503](https://doi.org/10.1103/PhysRevLett.95.140503)$]$

* {#HormoziZikosBonesteelSimon07} [[Layla Hormozi]], [[Georgios Zikos]], [[Nicholas E. Bonesteel]], [[Steven H. Simon]], *Topological Quantum Compiling*, Phys. Rev. B **75** 165310 (2007) &lbrack;[arXiv:quant-ph/0610111](https://arxiv.org/abs/quant-ph/0610111), [doi:10.1103/PhysRevB.75.165310](https://doi.org/10.1103/PhysRevB.75.165310)&rbrack;

* {#HormoziBonesteelSimon09} [[Layla Hormozi]], [[Nicholas E. Bonesteel]], [[Steven H. Simon]], *Topological Quantum Computing with Read-Rezayi States*, Phys. Rev. Lett. **103** 160501 (2009) &lbrack;[doi:10.1103/PhysRevLett.103.160501](https://doi.org/10.1103/PhysRevLett.103.160501), [arXiv:0903.2239](https://arxiv.org/abs/0903.2239)&rbrack;


* [[Joren W. Brunekreef]], *Topological Quantum Computation and Quantum Compilation*, Utrecht (2014) &lbrack;[studenttheses.uu.nl:20.500.12932/17738](https://studenttheses.uu.nl/handle/20.500.12932/17738)&rbrack;

* Keisuke Fujii, *Quantum Computation with Topological Codes: from qubit to topological fault-tolerance*,  SpringerBriefs in Mathematical Physics **8** (2015) &lbrack;[arXiv:1504.01444](https://arxiv.org/abs/1504.01444), [doi:10.1007/978-981-287-996-7](https://doi.org/10.1007/978-981-287-996-7)&rbrack;




