
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

**[[Pauli gate]]**

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

The notion of quantum logic gates and [[quantum circuits]] originates with

* [[Richard Feynman]], *Quantum mechanical computers*, Foundations of Physics **16** (1986) 507–531 &lbrack;[doi:10.1007/BF01886518](https://doi.org/10.1007/BF01886518)&rbrack;

* [[David E. Deutsch]], *Quantum computational networks*, Proceedings of the Royal Society A, **425** 1868 (1989) 73-90 &lbrack;[doi:10.1098/rspa.1989.0099](https://doi.org/10.1098/rspa.1989.0099), [jstor:2398494](https://www.jstor.org/stable/2398494)&rbrack;

* {#BBCDMSSSW95} [[Adriano Barenco]], [[Charles H. Bennett]], [[Richard Cleve]], [[David P. DiVincenzo]], [[Norman Margolus]], [[Peter Shor]], [[Tycho Sleator]], [[John A. Smolin]], [[Harald Weinfurter]], *Elementary gates for quantum computation*, Phys. Rev. A**52** (1995) 3457 &lbrack;[arXiv:quant-ph/9503016](https://arxiv.org/abs/quant-ph/9503016), [doi:10.1103/PhysRevA.52.3457](https://doi.org/10.1103/PhysRevA.52.3457)&rbrack;

On experimental realizations:

* Chen, Church, Englert, Henkel, Rohwedder, Scully, Zubairy:  *Quantum Computing Devices -- Principles, Designs, and Analysis*, Routledge (2007) &lbrack;[ISBN:9780367390372](https://www.routledge.com/Quantum-Computing-Devices-Principles-Designs-and-Analysis/Chen-Church-Englert-Henkel-Rohwedder-Scully-Zubairy/p/book/9780367390372?srsltid=AfmBOooGiSmyK4mzxjmR1LBJz4zU9cgCpp_z4cPiCzEhM6SJo4b2GxRp)&rbrack;


See also:

* Wikipedia, *[Quantum logic gate](https://en.wikipedia.org/wiki/Quantum_logic_gate)*

Implementation of quantum logic gates on [[qbits]] realized via [[nucleon]]-[[spin]], via pulse protocols in [[nuclear magnetic resonance]]-technology:

* Price, Somaroo, Tseng, Gore, Fahmy,, Havel, Cory: *Construction and Implementation of NMR Quantum Logic Gates for Two Spin Systems*, Journal of Magnetic Resonance
**140** 2 (1999) 371-378 &lbrack;[doi;10.1006/jmre.1999.1851](https://doi.org/10.1006/jmre.1999.1851)&rbrack;

and analogously on [[electron]]-[[spin]]:

* M. Yu. Volkov and K. M. Salikhov, *Pulse Protocols for Quantum Computing with Electron Spins as Qubits*, Appl Magn Reson **41** (2011) 145–154 &lbrack;[doi:10.1007/s00723-011-0297-2](https://doi.org/10.1007/s00723-011-0297-2)&rbrack;

[[!redirects quantum logic gates]]

[[!redirects quantum gate]]
[[!redirects quantum gates]]

