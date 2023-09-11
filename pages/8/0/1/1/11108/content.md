
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Traditional notation in [[physics]] &lbrack;[Dirac 1939](#Dirac39)&rbrack; for writing down [[pure state|pure]] [[quantum states]] (elements of [[Hilbert spaces]]), their [[hermitian adjoints]] and [[Hermitian form|Hermtian]] [[inner products]]:

With the [[Hermitian form|Hermitian]] [[inner product]] on the [[underlying]] [[vector space]] of a [[Hilbert space]] $H$ denoted $\langle-\vert-\rangle$, element $\psi \,\in\, H$ are turned into elements of the [[linear dual space]] $H^\ast$ by $\langle \psi \vert -\rangle \,\in\, H^\ast$, whose [[evaluation]] on another $\phi \in H$ is the given [[Hermitian form]] $\langle \psi \vert \phi\rangle$. Hence if one declares notation such that

$$
  \array{
     \vert \phi \rangle \;\equiv\; \phi \,\in\, H
     \\
     \langle \psi \vert \;\equiv\; \langle \psi \vert -\rangle \,\in\, H^\ast
  }
$$

then the [[evaluation]]-pairing in the [[Hermitian form]] is essentially juxtaposition 

$$
  \array{
    H^\ast \otimes H &\longrightarrow& \mathbb{C}
    \\
    \langle \psi \vert 
    ,
    \vert \phi \rangle
    &\mapsto&
    \langle \psi \vert \phi \rangle
  }
$$

With the inner product $\langle-\vert-\rangle$ referred to as a *bracket* this suggest to refer to "$\langle \psi \vert$" as a "bra" and "$\vert \phi \rangle$" as a "ket" &lbrack;[Dirac 1939, last line](#Dirac39)&rbrack;.



## Related concepts

[[!include states and observables -- content]]


## References

Due to:

* {#Dirac39} [[Paul A. M. Dirac]], *A new notation for quantum mechanics*, Mathematical Proceedings of the Cambridge Philosophical Society **35** 3 (1939) 416-418 &lbrack;[doi:10.1017/S0305004100021162](https://doi.org/10.1017/S0305004100021162), [pdf](https://www.ifsc.usp.br/~lattice/wp-content/uploads/2014/02/Dirac_notation.pdf)&rbrack;

Textbook accounts:

* [[Jun John Sakurai]], Jim Napolitano, §1.2 in: *Modern Quantum Mechanics*, Cambridge University Press (1985, 1994, 2020) &lbrack;[doi:10.1017/9781108587280](https://doi.org/10.1017/9781108587280), [Wikipedia](https://en.wikipedia.org/wiki/Modern_Quantum_Mechanics)&rbrack;


See also:

* Wikipedia, _[Bra-ket notation](http://en.wikipedia.org/wiki/Bra&#8211;ket_notation)_

[[!redirects bra]]
[[!redirects ket]]
[[!redirects bras]]
[[!redirects kets]]

[[!redirects bra-ket notation]]
