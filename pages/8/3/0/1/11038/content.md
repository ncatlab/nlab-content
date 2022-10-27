[[!redirects quantum gate]]


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

The first examples are linearizations of classical  [[logic gates]], or rather of their [[reversible computation|reversible]] versions:

\linebreak

**[[NOT]]:**

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

(...)


## Related concepts

* [[logic gate]]

* [[quantum circuit]]

* [[quantum logic]]

## References

The notion of quantum logic gates and [[quantum circuits]] originates with

* [[David E. Deutsch]], *Quantum computational networks*, Proceedings of the Royal Society A, **425** 1868 (1989) 73-90 &lbrack;[doi:10.1098/rspa.1989.0099](https://doi.org/10.1098/rspa.1989.0099), [jstor:2398494](https://www.jstor.org/stable/2398494)&rbrack;

See also:

* Wikipedia, *[Quantum logic gate](https://en.wikipedia.org/wiki/Quantum_logic_gate)*

[[!redirects quantum logic gate]]
[[!redirects quantum logic gates]]

[[!redirects quantum gates]]

[[!redirects controlled quantum gate]]
[[!redirects controlled quantum gates]]
[[!redirects controlled quantum logic gate]]
[[!redirects controlled quantum logic gates]]
