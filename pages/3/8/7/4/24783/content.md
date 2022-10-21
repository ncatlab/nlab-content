
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

In [[quantum physics]] and especially in [[quantum information theory]], by *state preparation* one refers to a process (either in actual [[experiments]] or theoretically as a kind of [[quantum gate]]-operation) which, possibly conditioned on a classical parameter $b$, "produces" a predefined [[quantum state]] $\vert b \rangle \,\in\, \mathscr{H}$ in a given [[space of quantum states]] $\mathscr{H}$.

For example, for a [[qbit]] [[data type]] there are, by definition of qbits, two canonical basis states $\vert 0 \rangle, \vert 1 \rangle \,\in\, \mathbb{C}^2$ to be prepared, depending on a classical parameter which may be understood as of [[boolean]] [[type]] (where we set $Bool \,\coloneqq\, \{0, 1\}$). 

In the language[^1] of [modal quantum logic](necessity+and+possibility#ModalQuantumLogic) on [[dependent linear types]] (see at *[[quantum circuits via dependent linear types]]*), the conditional preparation of a [[qbit]]-state reads as follows:

[^1]: We follow *[[schreiber:Topological Quantum Programming in Linear Homotopy Type Theory]]*.

\begin{imagefromfile}
    "file_name": "QCwthLHT-QBitStatePreparationCondt-221021.jpg",
    "width": "500",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

and the unconditional state preparation is of this form:

\begin{imagefromfile}
    "file_name": "QCwthLHT-QBitStatePreparation-221021.jpg",
    "width": "500",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Other states may be prepared by first preparing a [[qbit]]-state and then sending it through some [[quantum gate]]. 

For instance, the [[Bell state]] on two [[qbits]] may be prepared by first preparing a [[tensor product]] of two $\vert 0 \rangle$-states and then sending one through a [[Hadamard gate]] and then the resulting two qbits through a [[CNOT gate]]:

\begin{imagefromfile}
    "file_name": "QCwthLHT-BellStatePreparation-221021.jpg",
    "width": "800",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

This is used in many common [[quantum circuits]], such as for instance in the [[quantum teleportation]]-protocol.

## References

Standard textbook accounts:


* [[Michael A. Nielsen]], [[Isaac L. Chuang]], §7.2 in: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;


[[!redirects quantum state preparations]]

[[!redirects state preparation]]
[[!redirects state preparations]]


