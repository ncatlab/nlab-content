


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

The *contolled NOT* or *[[reversible computation|reversible]] [[XOR]]-gate* is the [[logic gate]] acting between [[pairs]] of [[bits]] which identically keeps the first bit in the pair and [[negation|negates]] the second IFF the first was set.

This may be understood equivalently as 

* the [[controlled quantum gate]]-version of the quantum [[NOT]]-gate

* the [[reversible computation|reversible]] version of the [[XOR]]-gate.

In [[quantum computing]]/[[quantum information theory]], by the *controlled NOT gate* or *CNOT gate* one means the [[quantum logic gate]] which acts on a [[pair]] of [[qbits]] by the [[linear map]] which is given in this way on the canonical [[linear basis]]-elements of a [[pair]] of [[qbits]]:

\begin{imagefromfile}
    "file_name": "CNOTGates-221026c.jpg",
    "width": "740",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


Similarly, by the *CCNOT*-gate (or *Toffoli gate*) one means the operation on triples of [[bits]]/[[qbit]] which keeps the first two and reverses the third iff the first two are both set.


## Related entries

* [[Hadamard gate]]

* [[reversible computation]]

## References

Textbook accounts:

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], p. 21 in: *Quantum computation and quantum information*, Cambridge University Press (2000) $[$[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]$]$

See also: 

* Wikipedia, *[Controlled NOT gate](https://en.wikipedia.org/wiki/Controlled_NOT_gate)*

* Wikipedia, *[Toffoli gate](https://en.wikipedia.org/wiki/Toffoli_gate)*


[[!redirects CNOT]]
[[!redirects CCNOT]]

[[!redirects Toffoli gate]]

[[!redirects controlled NOT gate]]
[[!redirects controlled-controlled NOT gate]]

[[!redirects quantum CNOT gate]]
[[!redirects quantum CNOT gates]]

[[!redirects controlled quantum NOT gate]]
[[!redirects controlled quantum NOT gates]]
