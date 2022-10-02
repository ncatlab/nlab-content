


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

In [[quantum computing]]/[[quantum information theory]], by the *controlled NOT gate* or *CNOT gate* one means the [[quantum gate]] which acts on a pair of [[qbits]] by the [[linear map]]

$$
  CNOT 
  \;\colon\;
  \mathbb{C}^2 \otimes \mathbb{C}^2
  \longrightarrow
  \mathbb{C}^2 \otimes \mathbb{C}^2
$$

which is given on the standard [[linear basis]]-elements by the operation which keeps the first bit and switches (NOTs) the second one iff the first has value 1:

$$
  CNOT
  \;\;\colon\;\;
  \left\{
  \;\;
  \begin{array}{ccc}
    \vert 0 \rangle \otimes \vert 0 \rangle   
    &\mapsto&
    \vert 0 \rangle \otimes \vert 0 \rangle
    \\
    \vert 0 \rangle \otimes \vert 1 \rangle   
    &\mapsto&
    \vert 0 \rangle \otimes \vert 1 \rangle
    \\
    \vert 1 \rangle \otimes \vert 0 \rangle   
    &\mapsto&
    \vert 1 \rangle \otimes \vert 1 \rangle
    \\
    \vert 1 \rangle \otimes \vert 1 \rangle   
    &\mapsto&
    \vert 1 \rangle \otimes \vert 0 \rangle
  \end{array}
  \right.
$$

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


