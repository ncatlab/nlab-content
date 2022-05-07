For any monoidal category V with coequalisers, one can form a bicategory Bimod(V) of bimodules as follows. The objects of Bimod(V) are monoids R, S internal to V. The 1-cells are (R,S)-bimodules. That is, objects A in V with a compatible left action of R and right action of S. 1-cell composition is then a generalization of the usual notion of tensor product. For an (R,S)-bimodule A and an (S,T)-bimodule B, a new (R,T)-bimodule $A \otimes_S B$ is computed as the coequaliser of A's right action and B's left action of S.

\[
A \otimes S \otimes B
\begin{matrix}
  \overset{\rho \otimes B}{\rightarrow} \\
  \underset{A \otimes \lambda}{\rightarrow}
\end{matrix}\,\,
A \otimes B \rightarrow A \otimes_S B
\]

2-cells, as expected are just module homomorphisms. In the case where V = Ab, this recovers the usual notion of bimodules and tensor product.

More generally, profunctors over any monoidal category are referred to as [[bimodules|bimodule]]. Composition in this case replaces the colimit above with a coend.