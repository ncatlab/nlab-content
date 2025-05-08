
> This entry is about *QRAM* in the sense of [Giovanetti et al. 2008](#GiovanettiLloydMaccone08). For the other sense of *[[classically controlled quantum computation]]* see there.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[quantum computing]] and [[quantum information theory]], the notion of *quantum random access memory* (QRAM, due to [Giovanetti, Lloyd & Maccone 2008](#GiovanettiLloydMaccone08)) is meant to be the [[quantum physics|quantum]]-analog of the [[classical physics|classical]] notion of [[random access memory]]; the key point being that QRAM may be addressed by *[[quantum superpositions]]* of address values and then reads/writes the corresponding [[quantum superposition]] of quantum data ([GLM08, (1)](#GiovanettiLloydMaccone08)).


## Circuit model
 {#CircuitModel}

The *circuit model* for QRAM essentially identifies a quantum program 

* of nominal type $\mathscr{H} \longrightarrow \mathscr{H}$ 

* but with access to a QRAM space $QMem$ 

with a  a [[quantum circuit]] of type

$$
  QMem \otimes \mathscr{H} 
    \longrightarrow
  QMem \otimes \mathscr{H}
  \,.
$$

In the existing literature this is typically stated in terms of concrete examples rather than in abstract generality, see for instance &lbrack;[Arunachalam et al 2015, Fig. 9](#ArunachalamEtAl15)&rbrack; or &lbrack;[Park, Petruccione & Rhee 2019, Fig 1](#ParkPetruccioneRhee19)&rbrack; with review in &lbrack;[Phalak, Chatterjee & Ghosh 2023, Fig 4](#PhalakChatterjeeGhosh23)&rbrack;. A nicely transparent example is given in by [quantumcomputinguk.org](#quantumcomputinguk):

<center>
<img src="https://ncatlab.org/nlab/files/CircuitQRAMExample-quantumcomputinguk.jpg" width="700">
</center>

(Here the block "Memory Cells" is our "$QMem$", the rest is our $\mathscr{H}$.)

This [[quantum circuit]] is such that (assuming $q_2 =\cdots = q_6 = 0$)

* if the Read/Write flag is 0 then

  it keeps all qbits (except for "Routing" and) except that the "Readout QBit" is set to one of the four "Memory values" depending on the four possible values of the "Addressing QBits"

* if the Read/Write flag is 1 then

  it keeps all qbits (except for "Routing" and) except that the "Memory QBit" addressed by the value of the "Addressing QBits" is set to the value of $q_{10}$.

* for a [[superposition]] of these inputs it yields the corresponding superposition of outputs.


## Via linear state-effects 

Recall that a classical random access memory of [[data type]] $Mem$ is modeled (in terms of [[monads in computer science]]) by the [[state monad]] induced from the *[[cartesian monoidal category|cartesian]]* [[internal hom]]-[[adjoint functor|adjunction]] 

* [[product]]$\;$ $Mem \times (-) \;\;\dashv\;\; Maps(Mem, -)$ $\;$[[function set]]

namely:

$$
  RAM(Mem,A)
  \;\coloneqq\;
  Maps
  \big(
    Mem
    ,\,
    Mem 
    \times 
    A
  \big)
  \,.
$$

(Notice that in concrete applications people often insist that  $Mem =$ [[Bool]]${}^{\times^n}$, but the conceptual nature of RAM is indifferent to this choice.)

Now, with classical data types (such as [[bits]]) replaced by quantum data types (such as [[qbits]]), namely by *[[linear types]]*, the analogous [[internal hom]]-[[adjoint functor|adjunction]] is 

* [[tensor product]]$\;$ $ QMem \otimes (-) \;\;\dashv\;\; LinMaps(QMem, - )$ $\;$[[linear space]]-of-[[linear maps]]

and the corresponding [[monad]] is

$$
  QRAM(Mem, \mathscr{H})
  \;\coloneqq\;
  LinMaps
  \big(
    QMem
    ,\,
    QMem 
    \otimes
    \mathscr{H}
  \big)
$$

and it seems clear that this does correspond to the intended behaviour of QRAM (where we are free to set $QMem \coloneqq $ [[QBit]]${}^{\otimes^n}$, if desired, which is typically the case in the literature).

In particular, the intended equivalence between the "QRAM model" and the "[[quantum circuit]]-model" of [[quantum computation]] is just the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) of the linear [[internal hom]]-[[adjunction]]

$$
  \Big\{
  In 
  \longrightarrow
  LinMaps
  \big(
    QMem
    ,\,
    QMem 
    \otimes
    Out
  \big)
  \Big\}
  \;\;\;\;\;\;\;
  \leftrightarrow
  \;\;\;\;\;\;\;  
  \Big\{
  In \otimes QMem
  \longrightarrow
  Out \otimes QMem
  \Big\}
  \,.
$$

## References

The terminology "quantum random access memory" is due to

* {#GiovanettiLloydMaccone08} [[Vittorio Giovannetti]], [[Seth Lloyd]], [[Lorenzo Maccone]], *Quantum random access memory*, Phys. Rev. Lett. **100** 160501 (2008) &lbrack;[doi:10.1103/PhysRevLett.100.160501](https://doi.org/10.1103/PhysRevLett.100.160501), [arXiv:0708.1879](https://arxiv.org/abs/0708.1879)&rbrack;

* {#GiovanettiLloydMaccone08b} [[Vittorio Giovannetti]], [[Seth Lloyd]], [[Lorenzo Maccone]], *Architectures for a quantum random access memory*, Phys. Rev. A **78** 052310 (2008) &lbrack;[doi:10.1103/PhysRevA.78.052310](https://doi.org/10.1103/PhysRevA.78.052310), [arXiv:0807.4994](https://arxiv.org/abs/0807.4994)&rbrack;

Further development:

* {#ArunachalamEtAl15} S. Arunachalam et al., *On the robustness of bucket brigade quantum RAM*, New Journal of Physics, **17** 12  (2015) 123010 &lbrack;[arXiv:1502.03450](https://arxiv.org/abs/1502.03450), [doi:10.1088/1367-2630/17/12/123010](https://doi.org/10.1088/1367-2630/17/12/123010)&rbrack;

* {#ParkPetruccioneRhee19} Park, Petruccione, Rhee, *Circuit-Based Quantum Random Access Memory for Classical Data*, Scientific Reports **9** 3949 (2019) &lbrack;[doi:10.1038/s41598-019-40439-3](https://doi.org/10.1038/s41598-019-40439-3)&rbrack;

Review:

* [[Alessandro Luongo]], *[The QRAM](https://quantumalgorithms.org/chap-classical-data-quantum-computers.html#the-qram)*, §3.1.1. in: *[Quantum algorithms for data analysis](https://quantumalgorithms.org/)*

* {#PhalakChatterjeeGhosh23} Koustubh Phalak, Avimita Chatterjee, Swaroop Ghosh, *Quantum Random Access Memory For Dummies* &lbrack;[arXiv:2305.01178](https://arxiv.org/abs/2305.01178)&rbrack;

* Samuel Jaques, Arthur G. Rattew, *QRAM: A Survey and Critique* &lbrack;[arXiv:2305.10310](https://arxiv.org/abs/2305.10310)&rbrack;

With emhasis on laboratory realization:

* Chenxu Liu, et al., III.C (pp. 18) of:  *Quantum Memory: A Missing Piece in Quantum Computing Units* &lbrack;[arXiv:2309.14432](https://arxiv.org/abs/2309.14432)&rbrack;

* Samuel Jaques, Arthur G. Rattew, *QRAM: A Survey and Critique* &lbrack;[arXiv:2305.10310](https://arxiv.org/abs/2305.10310)&rbrack;



With Qiskit:

* {#quantumcomputinguk} *[Implementing QRAM in Qiskit](https://quantumcomputinguk.org/tutorials/implementing-qram-in-qiskit-with-code)*

[[!redirects QRAMs]]

[[!redirects quantum RAM]]
[[!redirects quantum RAMs]]

[[!redirects quantum random access memory]]
[[!redirects quantum random access memories]]

[[!redirects quantum memory]]

[[!redirects quantum register]]
[[!redirects quantum registers]]


