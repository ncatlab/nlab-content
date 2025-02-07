
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Analogously to how a [[classical physics|classical]] [[logic gate]] is a [[function]] between ([[finite set|finite]]) [[sets]] of [[tuples]] of [[bits]] ([[truth values]]), so a *quantum logic gate* is a ([[unitary operator|unitary]]) [[linear operator]] on ([[finite-dimensional vector space|finite-dimensional]]) [[Hilbert spaces]] of [[tensor product of vector spaces|tensor products]] of [[qbits]]:

\begin{imagefromfile}
    "file_name": "GenericLogicGate-221026.jpg",
    "width": "640",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Specifically, one calls such a linear map a *quantum gate* if it is thought of as potentially implemented as a basic operation performed by a [[quantum computing]] machine.

As such, typical quantum logic gates operate on a *small* number of [[qbits]], with more complicated such linear maps obtained by composing a given set of quantum logic gates into *[[quantum logic circuits]]*. Such compilation is hence one model of *[[quantum computation]]*.


## Examples
 {#Examples}

The first examples are linearizations of classical  [[logic gates]], or rather of their [[reversible computation|reversible]] versions:

\linebreak

**[[NOT]]** or **[[Pauli gate|X]]**:

\begin{imagefromfile}
    "file_name": "NOT_LogicGate-221025.jpg",
    "width": "600",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\linebreak

\linebreak

**[[XOR]]** and **[[CNOT]]:**

\begin{imagefromfile}
    "file_name": "CNOTGates-221026c.jpg",
    "width": "750",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


\linebreak

**[[AND]]**:

\begin{imagefromfile}
    "file_name": "ANDGates-221026b.jpg",
    "width": "770",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\linebreak

The following examples have no classical analog:

\linebreak

**[[Hadamard gate]]**:

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

\linebreak

**[[Pauli gates]]**

(...)

\linebreak

**[[T gate]]** and **[[S gate]]**

(...)

\linebreak

(...)


## Related concepts

* [[logic gate]]

* [[controlled quantum gate]]

* [[unitary quantum channel]]

* [[quantum circuit]]

* [[quantum logic]]

* [[qbit]], [[qtrit]], [[qdit]]


## References

### General

The notion of quantum logic gates and [[quantum circuits]] originates with

* [[Richard Feynman]], *Quantum mechanical computers*, Foundations of Physics **16** (1986) 507–531 &lbrack;[doi:10.1007/BF01886518](https://doi.org/10.1007/BF01886518)&rbrack;

* [[David E. Deutsch]], *Quantum computational networks*, Proceedings of the Royal Society A, **425** 1868 (1989) 73-90 &lbrack;[doi:10.1098/rspa.1989.0099](https://doi.org/10.1098/rspa.1989.0099), [jstor:2398494](https://www.jstor.org/stable/2398494)&rbrack;

* {#BBCDMSSSW95} [[Adriano Barenco]], [[Charles H. Bennett]], [[Richard Cleve]], [[David P. DiVincenzo]], [[Norman Margolus]], [[Peter Shor]], [[Tycho Sleator]], [[John A. Smolin]], [[Harald Weinfurter]], *Elementary gates for quantum computation*, Phys. Rev. A**52** (1995) 3457 &lbrack;[arXiv:quant-ph/9503016](https://arxiv.org/abs/quant-ph/9503016), [doi:10.1103/PhysRevA.52.3457](https://doi.org/10.1103/PhysRevA.52.3457)&rbrack;

Monograph:


* {#NielsenChuang00} [[Michael A. Nielsen]], [[Isaac L. Chuang]], §1.3.1-2 in: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

On experimental realizations:

* Chen, Church, Englert, Henkel, Rohwedder, Scully, Zubairy:  *Quantum Computing Devices -- Principles, Designs, and Analysis*, Routledge (2007) &lbrack;[ISBN:9780367390372](https://www.routledge.com/Quantum-Computing-Devices-Principles-Designs-and-Analysis/Chen-Church-Englert-Henkel-Rohwedder-Scully-Zubairy/p/book/9780367390372?srsltid=AfmBOooGiSmyK4mzxjmR1LBJz4zU9cgCpp_z4cPiCzEhM6SJo4b2GxRp)&rbrack;


See also:

* Wikipedia, *[Quantum logic gate](https://en.wikipedia.org/wiki/Quantum_logic_gate)*

Implementation of quantum logic gates on [[qbits]] realized via [[nucleon]]-[[spin]], via pulse protocols in [[nuclear magnetic resonance]]-technology:

* Price, Somaroo, Tseng, Gore, Fahmy,, Havel, Cory: *Construction and Implementation of NMR Quantum Logic Gates for Two Spin Systems*, Journal of Magnetic Resonance
**140** 2 (1999) 371-378 &lbrack;[doi;10.1006/jmre.1999.1851](https://doi.org/10.1006/jmre.1999.1851)&rbrack;

and analogously on [[electron]]-[[spin]]:

* M. Yu. Volkov and K. M. Salikhov, *Pulse Protocols for Quantum Computing with Electron Spins as Qubits*, Appl Magn Reson **41** (2011) 145–154 &lbrack;[doi:10.1007/s00723-011-0297-2](https://doi.org/10.1007/s00723-011-0297-2)&rbrack;

### Universal gate sets
 {#ReferencesUniversalGateSets}

Review:

* [Nielsen & Chuang 2000, §4.5](#NielsenChuang00)

* *Universal set of quantum gates*, ICTP-SAIFR presentation (2022) &lbrack;[pdf](https://www.ictp-saifr.org/wp-content/uploads/2022/11/ICTP_SAIFR_D1-L2.pdf)&rbrack;

Proof that [[CNOT]] + [[U(n)|U(2)]] is universal:

* [[Adriano Barenco]], [[Charles H. Bennett]], [[Richard Cleve]], [[David P. DiVincenzo]], [[Norman Margolus]], [[Peter Shor]], [[Tycho Sleator]], [[John A. Smolin]], [[Harald Weinfurter]]: *Elementary gates for quantum computation*, Phys. Rev. A **52** (1995) 3457 &lbrack;[doi:10.1103/PhysRevA.52.3457](https://doi.org/10.1103/PhysRevA.52.3457), [arXiv:quant-ph/9503016](https://arxiv.org/abs/quant-ph/9503016)&rbrack;

Proof that [[CNOT]] + [[Hadamard gate|Hadamard]] +  [[T gate]] is universal:

* P. Oscar Boykin, Tal Mor, Matthew Pulver, Vwani Roychowdhury, Farrokh Vatan: *A new universal and fault-tolerant quantum basis*, Information Processing Letters **75** 3 (2000) 101-107 \[<a href="https://doi.org/10.1016/S0020-0190(00)00084-3">doi:10.1016/S0020-0190(00)00084-3</a>, [arXiv:quant-ph/9906054](https://arxiv.org/abs/quant-ph/9906054)\]


Proof that [[CNOT]] + $R_y(\pi/4)$ +  [[S gate]] is universal:

* [[Alexei Kitaev]]: *Quantum computations: algorithms and error correction*,  Russ. Math. Surv. **52** (1997) 1191 &lbrack;[doi:10.1070/RM1997v052n06ABEH002155](https://iopscience.iop.org/article/10.1070/RM1997v052n06ABEH002155)&rbrack;


Proof that [[Toffoli gate]] + [[Hadamard gate]] is universal (and generally Toffoli + any real single-qbit gate not preserving the measurement basis):

* [[Yaoyun Shi]]: *Both Toffoli and Controlled-NOT need little help to do universal quantum computation*, Quantum Information & Computation **3** 1 (2003) 84-92 &lbrack;[doi:10.5555/2011508.2011515](https://dl.acm.org/doi/abs/10.5555/2011508.2011515), [arXiv:quant-ph/0205115](https://arxiv.org/abs/quant-ph/0205115)&rbrack;

* [[Dorit Aharonov]]: *A Simple Proof that Toffoli and Hadamard are Quantum Universal* &lbrack;[arXiv:quant-ph/0301040](https://arxiv.org/abs/quant-ph/0301040), [spire:2727250](https://inspirehep.net/literature/2727250)&rbrack;




[[!redirects quantum logic gates]]

[[!redirects quantum gate]]
[[!redirects quantum gates]]

