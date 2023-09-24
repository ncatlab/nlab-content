
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

For $\mathscr{B}$ a [[finite-dimensional Hilbert space]], the operation of [[partial trace]] over $\mathscr{B}$ is a quantum channel

$$
  \array{
    \mathscr{H}
    \otimes
    \mathscr{B}
    \otimes
    \mathscr{B}^\ast
    \otimes
    \mathscr{H}^\ast
    &
    \xrightarrow{
      trace^{\mathscr{B}}
    }
    &
    \mathscr{H} \otimes \mathscr{H}^\ast
    \\
    \left\vert \psi, \beta \right\rangle
    \left\langle \beta', \psi' \right\vert
    &\mapsto&
    \left\vert \psi \right\rangle
    \left\langle \beta' \vert \beta \right\rangle
    \left\langle \psi' \right\vert
    \mathrlap{\,.}
  }  
$$

which represents the "operation" of averaging the [[mixed state|mixed]] [[quantum states]] of the [[composite system|composite]] [[quantum system]] $\mathscr{H} \otimes \mathscr{B}$ over the degrees of freedom of $\mathscr{B}$.


## Properties


[[!include quantum channels and decoherence -- section]]


## Related concepts

* [[decoherence]]

* [[quantum channel]]

  * [[quantum measurement channel]]

  * [[unitary quantum channel]]


[[!redirects partial trace quantum channels]]
