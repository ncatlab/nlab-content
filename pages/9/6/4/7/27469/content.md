

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--

\tableofcontents


## Idea

In [[quantum information theory]] and [[quantum computing]], by the *T-gate* and the *S-gate* one refers to the [[quantum gates]] acting on single [[qbits]] that in the defining measurement-[[linear basis|basis]] $\big\{ {\vert 0 \rangle}, {\vert 1 \rangle} \big\}$ are given by the $2 \times 2$ [[complex numbers|complex]] [[matrices]]

$$
  T 
  \;=\;
  \left[
    \begin{array}{cc}
      1 & 0
      \\
      0 & e^{\pi \mathrm{i}/4}
    \end{array}
  \right]
$$

and

$$
  S 
  \;=\; 
  T^2
  \;=\;
  \left[
    \begin{array}{cc}
      1 & 0
      \\
      0 & \mathrm{i}
    \end{array}
  \right]
  \mathrlap{\,,}
$$

respectively, where "$\mathrm{i}$" denotes the [[imaginary unit]].

In particular, the [[Pauli Z-gate]] is decomposable into these gates as 

$$
  Z   
   \;=\; 
  S^2 
   \;=\; 
  T^4
  \,.
$$

\begin{remark}
Beware of these alternative names and their subtleties:

* The T-gate is also known as the "$\pi/8$-gate" (e.g. in [Nielsen & Chuang 2000 p xxx](#NielsenChuang00)), even though the phase rotation is by $\pi/4$ -- but differs by only a global phase from the $R_Z(\pi/8)$ [[rotation gate]].

* The S-gate is also known as the "phase gate", but that term is ambiguous.

\end{remark}

## Related gates

* [[Hadamard gate]]

* [[Pauli gates]]

* [[rotation gate]]

* [[CNOT gate]]

* [[Toffoli gate]]


## References

* {#NielsenChuang00} [[Michael A. Nielsen]], [[Isaac L. Chuang]], p xxx in: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

[[!redirects T gates]]

[[!redirects T-gate]]
[[!redirects T-gates]]

[[!redirects quantum T gate]]
[[!redirects quantum T gates]]

[[!redirects quantum T-gate]]
[[!redirects quantum T-gates]]


[[!redirects S gate]]
[[!redirects S gates]]
[[!redirects S-gate]]
[[!redirects S-gates]]

[[!redirects quantum S gate]]
[[!redirects quantum S gates]]
[[!redirects quantum S-gate]]
[[!redirects quantum S-gates]]

