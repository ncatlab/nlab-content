[[!redirects CCZ gate]]

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


\tableofcontents

## Idea

In [[quantum computing]] and [[quantum information theory]], the *controlled Z gates* are [[controlled quantum gate]] versions of the [[Z gate]].

Where the [[Z gate]] acts on a single [[qbit]], being the [[unitary operator]]

\[
\begin{array}{ccc}
  \mathbb{C} 
   &\overset{Z}{\longrightarrow}&
   \mathbb{C}
   \\
   \vert b \rangle &\mapsto& (-1)^b \vert b \rangle
   \mathrlap{\,,}
\end{array}
\]
the $(N-1)$-*controlled* Z gates for $N \in \mathbb{N}_{\geq 1}$ are the [[unitary operators]] on the [[tensor product of Hilbert spaces|tensor product]] of $N$ [[qbits]] given by
\[
\label{BitCodeFormula}
\begin{array}{ccc}
  \mathbb{C}^N
   &\overset{C^{N-1} Z}{\longrightarrow}&
   \mathbb{C}^N
   \\
   \vert b_1,\cdots, b_N \rangle 
     &\mapsto& 
    (-1)^{b_1 \cdots b_N} 
   \vert b_1, \cdots, b_N \rangle
   \mathrlap{\,,}
\end{array}
\]
where $b_i \in \{0,1\}$.

(cf. [Beverland, Campbell, Howard & Kliuchnikov 2020](#BeverlandCampbellHowardKliuchnikov2020)).

Since the [[exponential]] expression in (eq:BitCodeFormula) is 
\[
  (-1)^{b_1 \cdots b_N}
  =
  \begin{cases}
    -1 & \text{ if }\; \forall_i \colon b_i\!=\!1
    \\
    +1 & \text{ otherwise }
   \end{cases}
\]
we equivalently have:
\[
  C^{N-1}Z
  \,=\,
  id 
    - 
  2{\vert 1, \cdots, 1\rangle}{\langle 1, \cdots, 1 \vert}
  \mathrlap{\,.}
\]
(cf. [Gühne et al. 2014 (1)](#GühneEtAl2014)).


## Examples

The *CCZ* [[quantum gate]] is the doubly-[[controlled quantum gate|controlled]] form of the [[Pauli gate|Pauli $Z$-gate]], which plays a role as a [non-Clifford gate](Clifford+group#NonCliffordMagic) alternative to the [[T-gate]] in the discussion of [Takagi, Yoder & Chuang 2017](#TakagiYoderChuang2017).

## Related concepts

* [[T-gate]]

## References

* {#GühneEtAl2014} O. Gühne, M. Cuquet, F.E.S. Steinhoff, T. Moroder, M. Rossi, D. Bruß, B. Kraus, C. Macchiavello; eq (1) in: *Entanglement and nonclassical properties of hypergraph states*, J. Phys. A: Math. Theor. **47** (2014) 335303 \[<a href="https://doi.org/10.1088/1751-8113/47/33/335303">doi:10.1088/1751-8113/47/33/335303</a>, [arXiv:1404.6492](https://arxiv.org/abs/1404.6492)\]


* {#TakagiYoderChuang2017} Ryuji Takagi, Theodore J. Yoder, [[Isaac L. Chuang]]: *Error rates and resource overheads of encoded three-qubit gates*, Phys. Rev. A **96** (2017) 042302 \[<a href="https://doi.org/10.1103/PhysRevA.96.042302">arXiv:10.1103/PhysRevA.96.042302</a>, [arXiv:1707.00012](https://arxiv.org/abs/1707.00012)\]

* {#BeverlandCampbellHowardKliuchnikov2020} Michael Beverland, Earl Campbell, Mark Howard, Vadym Kliuchnikov; §4.1 of: *Lower bounds on the non-Clifford resources for quantum computations*, Quantum Sci. Technol. **5** (2020) 035009 \[<a href="https://doi.org/10.1088/2058-9565/ab8963">doi:10.1088/2058-9565/ab8963</a>, [arXiv:1904.01124](https://arxiv.org/abs/1904.01124)\]

[[!redirects controlled Z-gates]]

[[!redirects CCZ-gate]]
[[!redirects CCZ-gates]]

[[!redirects CCZ gate]]
[[!redirects CCZ gates]]

[[!redirects controlled-controlled Z-gate]]
[[!redirects controlled-controlled Z-gates]]
