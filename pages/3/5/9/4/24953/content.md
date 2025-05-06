
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

In [[quantum computing]] (but the idea applies generally to [[nondeterministic computation]]), *repeat-until-success* &lbrack;[Shah & Oi (2013)](#ShahOi13), [Lim, Beige & Kwek (2005)](#LimBeigeKwek05)&rbrack; is a computation scheme with [[postselection]], where a given non-deterministic [[logic gate]] is re-applied to its given input data until a failure syndrome vanishes to indicate that the desired kind of gate operation has been performed.

Concretely, in [[quantum computation]] this means that a [[quantum logic gate]] is executed followed by [[quantum measurement]] of parts of its output data, and depending on this measurement either the remaining quantum state output is accepted and forwarded to the next [[logic gate]] in the [[quantum circuit]], or else the result is [[uncomputation|uncomputed]] and the procedure repeated.

While it has been shown &lbrack;[Lim, Beige & Kwek (2005)](#LimBeigeKwek05)&rbrack; that such repeat-until-success gates may be efficient (as they can avoid use of gate elements which yield guaranteed outcomes but at a high resource cost), they fall out of the plain [[quantum logic circuit]] scheme in that the nature and even the number of [[quantum gates]] being executed depends on [[classically controlled quantum gate|classical control]] measurement results known only at runtime  (i.e. on "[[dynamic lifting]]" of measurement results back into the classical context).

Phrased differently, repeat-until-success algorithms do have a generalized [[quantum circuit]]-description, but involving an infinite number of "wires"  (since it may take arbitrarily long until the failure syndrome vanishes).


## Related concepts

* [[postselection]]

* [[classically controlled quantum gate]]

* [[dynamic lifting]]

* [[non-deterministic computation]]

## References

* {#ShahOi13} Kerem Halil Shah, Daniel Kuan Li Oi, *Ancilla Driven Quantum Computation with arbitrary entangling strength*, Theory of Quantum Computation **22** (2013) &lbrack;[arXiv:1303.2066](https://arxiv.org/abs/1303.2066), [doi:10.4230/LIPIcs.TQC.2013.1](https://doi.org/10.4230/LIPIcs.TQC.2013.1)&rbrack;


* {#LimBeigeKwek05} Yuan Liang Lim, Almut Beige, Leong Chuan Kwek, *Repeat-Until-Success Quantum Computing*, Phys. Rev. Lett. **95** (2005)  030505 &lbrack;[doi:10.1103/PhysRevLett.95.030505](https://doi.org/10.1103/PhysRevLett.95.030505), [arXiv:quant-ph/0408043](https://arxiv.org/abs/quant-ph/0408043)&rbrack;

* Yuan Liang Lim, Sean D. Barrett, Almut Beige, Pieter Kok, Leong Chuan Kwek, *Repeat-Until-Success quantum computing using stationary and flying qubits*, Phys. Rev. A **73** (2006) 012304 &lbrack;[arXiv:quant-ph/0508218](https://arxiv.org/abs/quant-ph/0508218), [doi:10.1103/PhysRevA.73.012304](https://doi.org/10.1103/PhysRevA.73.012304)&rbrack;


* Adam Paetznick, Krysta M. Svore, *Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*, Quantum Information & Computation **14** 15-16 (2014) 1277-1301 &lbrack;[arXiv:1311.1074](https://arxiv.org/abs/1311.1074), [doi:10.5555/2685179.2685181](https://dl.acm.org/doi/10.5555/2685179.2685181)&rbrack;

* Alex Bocharov, Martin Roetteler, Krysta M. Svore: *Efficient synthesis of universal Repeat-Until-Success circuits*, Phys. Rev. Lett. **114** (2015) 080502 &lbrack;[arXiv:1404.5320](https://arxiv.org/abs/1404.5320), [doi:10.1103/PhysRevLett.114.080502](https://doi.org/10.1103/PhysRevLett.114.080502)&rbrack;

* Nathan Wiebe, Martin Roetteler: *Quantum arithmetic and numerical analysis using Repeat-Until-Success circuits* QIC *16** (2016) 134-178 &lbrack;[arXiv:1406.2040](https://arxiv.org/abs/1406.2040)&rbrack;


Discussion of the situation where "fail" (non-success) is guaranteed to act as the [[identity]] on the input [[quantum states]] ("success or draw")

* Qingxiuxiong Dong, Marco Túlio Quintino, Akihito Soeda, Mio Murao, *Success-or-Draw: A Strategy Allowing Repeat-Until-Success in Quantum Computation*, Phys. Rev. Lett. **126** (2021) 150504 &lbrack;[arXiv:2011.01055](https://arxiv.org/abs/2011.01055), [doi:10.1103/PhysRevLett.126.150504](https://doi.org/10.1103/PhysRevLett.126.150504)&rbrack;

On repeat-until-success algorithms for creating "quantum imaginary time evolution":

* {#AolitaEtAl21} Thais de Lima Silva, Márcio M. Taddei, Stefano Carrazza, [[Leandro Aolita]], *Fragmented imaginary-time evolution for early-stage quantum signal processors* &lbrack;[arXiv:2110.13180](https://arxiv.org/abs/2110.13180), [spire:1952417](https://inspirehep.net/literature/1952417)&rbrack;

Review:

* [[Leandro Aolita]], *Imaginary-time evolution algorithms for intermediate-scale quantum signal processors*, talk at *[Atomtronics@AbuDhabi2021](https://qrcseminar.tii.ae)* (2021) &lbrack;[video](https://youtu.be/G2eigbPiMKU)&rbrack;

[[!redirects repeat-until-success]]

[[!redirects repeat-until-success quantum gate]]
[[!redirects repeat-until-success quantum gates]]


[[!redirects repeat-until-success gate]]
[[!redirects repeat-until-success gates]]

