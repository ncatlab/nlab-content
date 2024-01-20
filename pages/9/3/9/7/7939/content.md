
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

In [[quantum information theory]] and [[quantum computing]], by a *q-bit* (or *qubit*) one means a [[quantum state]] in a 2-[[dimension of a vector space|dimensional]] [[complex vector space|complex]] [[Hilbert space]] [[space of quantum states|of states]].

Hence the quantum [[data type]] $QBit$ is the 2-[[dimension of a vector space|dimensional]] [[complex vector space]] equipped with its canonical [[quantum measurement]]-[[linear basis|basis]] 

$$
  \mathbb{C}^2 
  \,\simeq\, 
  \mathbb{C} \cdot \vert 0 \rangle \oplus \mathbb{C} \cdot \vert 1 \rangle
  \,.
$$

Analogous higher- but still finite- $d$-dimensional quantum data (types) are called *[[qudit|qdits]]* ("qtrits" for $d = 3$).

## Properties

### In terms of geometric quantization

In [[geometric quantization]] qbits are naturally understood as the states given by the [[geometric quantization of the 2-sphere]] for [[prequantum line bundle]] (plus [[metaplectic correction]]) being of unit [[first Chern class]]. See at _[geometric quantization of the 2-sphere -- The space of quantum states](geometric+quantization+of+the+2-sphere#TheSpaceOfQuantumStates)_.

## Related concepts

* [[data type]]

* [[spin resonance qbit]]

* [[one clean qbit]]

* [[Pauli gate]]

* [[bit]], [[truth value]]

* [[bit flip channel]], [[bit flip code]]

* [[quantum logic gate]], [[quantum circuit]]

* [[quantum logic]], [[quantum computing]], [[quantum error correction]]

* [[dimer]]

* [[quantum set]]

## References

### General

The term *q-bit* goes back to

* [[Benjamin Schumacher]], *Quantum coding*, Phys. Rev. A **51** (1995) 2738 $[$[doi:10.1103/PhysRevA.51.2738](https://doi.org/10.1103/PhysRevA.51.2738)$]$

and was popularized by early adoption such as in

* {#Shor95} [[Peter W. Shor]], *Scheme for reducing decoherence in quantum computer memory*, Phys. Rev. A 52, R2493(R) 1995 ([doi:10.1103/PhysRevA.52.R2493](https://doi.org/10.1103/PhysRevA.52.R2493))

Textbook account:

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], §1.2 in: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;



See also:

* Wikipedia, _[Qbit](http://en.wikipedia.org/wiki/Qubit)_

Laboratoy-realizations of qbits for use in [[quantum computers]]:

* *[Qubit Zoo](https://qubitzoo.org/qubitzoo/)*



[[!include spin resonance qbits -- references]]




[[!include superconducting qbits -- references]]





[[!redirects Qbit]]
[[!redirects qbits]]
[[!redirects Qbits]]
[[!redirects quantum bit]]
[[!redirects quantum bits]]

[[!redirects QBit]]

[[!redirects qubit]]
[[!redirects qubits]]

[[!redirects q-bit]]
[[!redirects q-bits]]

