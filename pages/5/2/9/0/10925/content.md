
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

Broadly, a *logic gate* is a [[function]] 

$$
  Bool^{n_{in}}
  \xrightarrow{\phantom{---}}
  Bool^{n_{out}}
$$

of [[tuples]] of [[truth values]], hence a
[[map]]
between [[cartesian products]] $\mathrm{Bool}^n$ of [[Booleans]] $Bool \,\coloneqq\, \{false, true\} \;\simeq\; \{0,1\}$.

Specifically, one calls such a function a *logic gate* if it is thought of as potentially implemented as a basic operation performed by a [[computing]] machine -- in which case the [[truth values]] are also called *[[bits]]*. 

As such, typical logic gates are Boolean functions between a *small* number of [[bits]], with more complicated such functions thought as obtained by composing a given set of logic gates into  [[logic circuits]].


## Examples

A list of some basic logic and gates and their [[reversible computation|reversible]] and [[quantum logic gate]] versions:

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
    "file_name": "CNOTGates-221026a.jpg",
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

\linebreak

**[[AND]]**:

\begin{imagefromfile}
    "file_name": "ANDGates-221026.jpg",
    "width": "770",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


(...)


## Related concepts

* [[formal logic]]

* [[quantum logic gate]]

## References

Textbook accounts:

*  Jan Friso Groote, Rolf Morel, Julien Schmaltz, Adam Watkins, *Logic Gates, Circuits, Processors, Compilers and Computers*, Springer (2021) &lbrack;[doi:10.1007/978-3-030-68553-9](https://doi.org/10.1007/978-3-030-68553-9)&rbrack;

* John Bird, Chapter 7 of: *Bird's Higher Engineering Mathematics*, Routledge (2021) &lbrack;[ISBN:9781003124221](https://www.taylorfrancis.com/chapters/mono/10.1201/9781003124221-7/boolean-algebra-logic-circuits-john-bird)&rbrack;

See also:

* Wikipedia, _[Logic gate](http://en.wikipedia.org/wiki/Logic_gate)_

[[!redirects logic gates]]

[[!redirects logic circuit]]
[[!redirects logic circuits]]
