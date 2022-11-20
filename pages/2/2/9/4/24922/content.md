
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
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

In [[quantum information theory]], by the *bit flip channel*
one means the [[quantum channel]] on a [[quantum system]] represented by a single [[q-bit]] whose effect is to "flip" the [[linear basis|basis]] [[q-bit]]  [[quantum states]] $\left\vert 0 \right\rangle \leftrightarrow \left\vert 1 \right\rangle$ with some [[probability]] $p$ or else leave the system unchanged with probability $1 - p$.

(This would more properly be called the *q-bit flip channel*, but this is not commonly used terminology.)

The [[tensor product]] of $N$ bit flip channels model the analogous process on $N$ [[q-bits]], where every single one of them may flip with probability $p$, independently of all the others. In this form, the spin flip channel serves as a simple but important model for [[quantum noise]]. Basic examples of [[quantum error correction codes]] may be used to provide partial correction of such bit flip errors, see at *[[bit flip code]]*.

## Definition

Fix a [[real number]] $p \in [0,1]$ serving as a measure of the [[probability]] for a spin flip to occur when data is sent through the channel.

We write:

* $QBit \,\simeq\, \mathbb{C}\cdot \left\vert 0 \right\rangle \,\oplus\, \mathbb{C} \cdot \left\vert 1 \right\rangle$ for the [[space of quantum states]] of a [[q-bit]], regarded as a [[Hilbert space]] ([[Hermitian inner product space]]) with $\big\{\left\vert 0 \right\rangle, \left\vert 1 \right\rangle \big\}$ being an [[orthonormal linear basis]];

* $States(QBit) \subset Herm(QBit)$ for the space of [[density matrices]] on this Hilbert space, hence the subspace of [[positive semi-definite bilinear form|positive semi-definite]] [[Hermitian operators]] $QBit \multimap QBit$ of unit [[trace]];

* $X \;\colon\; QBit \multimap QBit$ for the "[[Pauli matrix|Pauli X]]" ("[[NOT]]") [[quantum logic gate]] given by $X \left\vert 0 \right\rangle \,=\, \left\vert 1 \right\rangle$, and $X \left\vert 1 \right\rangle \,=\, \left\vert 0 \right\rangle$.


Now, a common way to define the spin flip channel is by the following expression (e.g. [Chuang (2011), p. 296](#Chuang11)):

$$
  \begin{aligned}
    flip
    &\colon\;
    States(QBit)
    \longrightarrow
    States(QBit)
    \\
    flip(\rho) 
    &\equiv\;
    (1-p) \cdot \rho \,+\, p \cdot (X \rho X)
  \end{aligned}
$$

One readily checks that on [[pure states]] in the [[q-bit]]-[[linear basis|basis]] this acts as expected:

$$
  \begin{array}{ccl}
    States(QBit)
    &\longrightarrow&
    States(QBit)
    \\
    \vert 0 \rangle \langle 0 \rangle
      &\mapsto&
    \mathrlap{
      (1-p) \cdot 
      \left\vert 0 \right\rangle 
      \left\langle 0 \right\vert
      \;+\;
      \;\;\;\;\;\;\;\;\; 
      p \cdot
      \left\vert 1 \right\rangle 
      \left\langle 1 \right\vert
    }
    \\
    \vert 1 \rangle \langle 1 \rangle
      &\mapsto&
    \mathrlap{
      \;\;\;\;\;\;\;\;\; 
      p \cdot 
      \left\vert 0 \right\rangle 
      \left\langle 0 \right\vert
      \;+\;
      (1-p) \cdot
      \left\vert 1 \right\rangle 
      \left\langle 1 \right\vert
    }
  \end{array}
$$

Alternatively, one finds that a [[Kraus decomposition]] of this operator as a [[unitary operator]] followed by a [[quantum measurement]] is:

$$
  flip 
  \;\colon\;
  \rho
  \;\mapsto\;
  P_0 \, U_{flip} \, \rho \, U_{flip} \, P_0
  \;+\;
  P_1 \, U_{flip} \, \rho \, U_{flip} \, P_1
  \,,
$$

where the [[unitary operator]] $U_{flip}$ is:

$$
  U_{flip}
  \;=\;
  \left[
  \array{
    + \sqrt{1-p} & \sqrt{p}
    \\
    \sqrt{p} & - \sqrt{1-p}
  } 
  \right]
  \;\colon\;
  QBit \multimap QBit
$$

## Related concepts

* [[bit flip code]]
 
## References

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], §8.3.3 in: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

* {#Chuang11} [[Isaac L. Chuang]], *Quantum error correction*, Chapter 7 in: *Quantum Machines: Measurement and Control of Engineered Quantum Systems* Lecture Notes of the Les Houches Summer School **96** (2011) 273–320  &lbrack;[doi:10.1093/acprof:oso/9780199681181.003.0007](https://doi.org/10.1093/acprof:oso/9780199681181.003.0007)&rbrack;

[[!redirects bit flip channels]]

[[!redirects bit-flip channel]]
[[!redirects bit-flip channels]]

[[!redirects qbit flip channel]]
[[!redirects qbit flip channels]]
[[!redirects qbit-flip channel]]
[[!redirects qbit-flip channels]]

[[!redirects q-bit flip channel]]
[[!redirects q-bit flip channels]]
[[!redirects q-bit-flip channel]]
[[!redirects q-bit-flip channels]]

