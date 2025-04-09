
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

In [[qbit]]-based [[quantum computation]], by the *Pauli gates* one means the [[linear basis]] of [[quantum gates]] on single [[qbits]], hence on the 2-dimensional [[Hilbert spaces]] $QBit \simeq \mathbb{C}^2$, which, in terms of the canonical [[quantum measurement]]-[[linear basis|basis]] $\mathbb{C}^2 \simeq Span\big( \{ {\vert 0 \rangle} ,\, {\vert 1 \rangle} \} \big)$, are given by the [[Pauli matrices]].

Explicitly this means that (in the conentional normalization) the:

1. *Pauli-X gate* (or quantum [[NOT]] gate) is given by the [[matrix]]

   $$
     X \;\;\coloneqq\;\; 
     \left[
       \begin{array}{cc}
         0 & 1 
         \\
         1 & 0
       \end{array}
     \right]
   $$

1. *Pauli-Y gate* is given by the [[matrix]]

   $$
     Y \;\;\coloneqq\;\; 
     \left[
       \begin{array}{cc}
         0 & - \mathrm{i} 
         \\
         \mathrm{i} & 0
       \end{array}
     \right]
   $$

1. *Pauli-Z gate* is given by the [[matrix]]

   $$
     Z \;\;\coloneqq\;\; 
     \left[
       \begin{array}{cc}
         1 & 0 
         \\
         0 & -1
       \end{array}
     \right]
   $$


## Properties

### Relation to Hadamard gates and the ZX-calculus

The [[Hadamard gate]] transforms the [[eigenstates]] $\vert 0 \rangle$, $\vert 1 \rangle$ of the Pauli Z-gate into those $\propto {\vert 0 \rangle} \pm {\vert 1 \rangle}$ of the Pauli-X gate, a relation that is elaborated on by the correspondingly named *[[ZX-calculus]]*.

## Related concepts

* [[Hadamard gate]], [[T gate]], [[S gate]]

* [[quantum computation]]

* [[quantum gate]], [[quantum circuit]]

* [[Hadamard gate]]

* [[XOR]], [[CNOT]]

* [[Solovay-Kitaev theorem]]


## References

Monograph:

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], p. xxx in: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

[[!redirects Pauli gates]]

[[!redirects Pauli quantum gate]]
[[!redirects Pauli quantum gates]]

[[!redirects Pauli-X gate]]
[[!redirects Pauli-X gates]]
[[!redirects Pauli-Y gate]]
[[!redirects Pauli-Y gates]]
[[!redirects Pauli-Z gate]]
[[!redirects Pauli-Z gates]]

[[!redirects Pauli X-gate]]
[[!redirects Pauli X-gates]]
[[!redirects Pauli Y-gate]]
[[!redirects Pauli Y-gates]]
[[!redirects Pauli Z-gate]]
[[!redirects Pauli Z-gates]]


[[!redirects Pauli-X]]
[[!redirects Pauli-Y]]
[[!redirects Pauli-Z]]
