
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

In [[quantum computing]]/[[quantum information theory]], by the *Hadamard gate* one means the [[quantum logic gate]] which acts on a single [[qbit]] by

$$
  q_0 \cdot \vert 0 \rangle 
  + 
  q_1 \cdot \vert 1\rangle 
  \;\;\;
  \mapsto
  \;\;\;
  \frac{1}{\sqrt{2}}
  \big(
    q_0 + q_1
  \big)
  \cdot 
  \vert 0 \rangle 
  +
  \frac{1}{\sqrt{2}}
  \big(
    q_0 - q_1
  \big)
  \cdot 
  \vert 1 \rangle 
  \,,
$$


hence which is the [[linear map]] $H \,\colon\, \mathbb{C}^2 \longrightarrow \mathbb{C}^2$ which in the standard [[linear basis]] is given by the [[matrix]]

$$
  \frac{1}{\sqrt{2}}
  \left(
  \array{
    +1 & +1
    \\
    +1 & -1
  }
  \right)
  \,.
$$

\begin{imagefromfile}
    "file_name": "HadamardGate-221026a.jpg",
    "width": "560",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


Simple as it is, the Hadamard gate plays a central role in theory and practice of [[quantum circuits]], notably where in its combination with the [[CNOT gate]] it is used to produce [[Bell states]] (such as in the [[quantum teleportation protocol]]).

## Related gates

* [[Pauli gates]]

* [[T gates]], [[S gate]]


## References

* {#Knill96} [[Emanuel Knill]], [p. 10](https://www.ncatlab.org/nlab/files/Knill-QuantumPseudocode.pdf#page=8) in: *Conventions for quantum pseudocode* Los Alamos Technical Report (1996) $[$[LA-UR-96-2724](https://www.osti.gov/biblio/366453-conventions-quantum-pseudocode), [doi:10.2172/366453](https://doi.org/10.2172/366453), [pdf](https://www.osti.gov/servlets/purl/366453), [[Knill-QuantumPseudocode.pdf:file]]$]$

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], [p. 28](https://ncatlab.org/nlab/files/NielsenChuangQuantumComputation.pdf#page=28) in: *Quantum computation and quantum information*, Cambridge University Press (2000) $[$[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]$]$

See also: 

* Wikipedia, *[Quantum logic -- Hadamard gate ](https://en.wikipedia.org/wiki/Quantum_logic_gate#Hadamard_gate)*

[[!redirects Hadamard gates]]

