
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

\begin{definition}
A *signed graph* is an undirected [[graph]] (e.g., a [[simple graph]], which is a [[set]] $V$ of *[[vertices]]* together with a collection $E$ of two-element subsets of $V$ called *[[edges]]*) together with a function from $E$ to a two-element set of "signs", e.g., $\sigma: E \to \{+, -\}$. 
not necessarily of edges.

One says that the sign of a cycle in a signed graph is the product of the signs of its edges.
\end{definition}

There are several notions of *[[homomorphisms]]* of signed graphs. They are all homomorphisms of the underlying graphs, by differ by how strictly they preserve the extra sign structure:

1. *sign preserving homomorphisms* preserve the signs of individual edges, 

1. *switching homomorphisms* are only required to preserve the signs of cycles but not necessarily of individual edges.

\begin{definition}
Let $\binom{V}{2}$ denotes the set of two-element [[subsets]] of $V$. A signed *simple* graph is equivalently a set $V$ together with a [[partial function]] $\binom{V}{2} \to \{+, -\}$. The [[domain]] of this partial function is declared to be $E$, so the data of a signed graph can be represented as $V$ together with a [[span]] of type 
$$
  \binom{V}{2} 
    \hookleftarrow 
  E 
    \overset{\sigma}{\longrightarrow} 
  \{+, -\}
  \,.
$$ 
\end{definition}

Signed graphs (and the basic theorems of their theory) seem to be rediscovered again and again. See [Zaslavsky 2018](#Zaslavsky18) for an annotated bibliography on signed graphs and their various guises.  


\begin{remark}
Signed graphs are *not* *directed graphs*: signs on undirected edges are not the same as directional information. For example, if vertices represent people and edges represent being acquainted then the signs could indicate being allies or enemies.

If a [[linear order]] has been imposed on the vertex set, then the sign function can be interpreted as imparting directions to edges (say if $x \lt y$ in the order and an edge $e$ between $x$ and $y$ has sign $+$, then the direction is $x \to y$; if $e$ has sign $-$, then the direction is $y \to x$). However, such linear orders on vertices will not be preserved by morphisms of signed graphs, so this does not give a [[functor|functorial]] way to derive directed graphs from signed graphs. 
\end{remark}



## References 

* {#Zaslavsky18} Thomas Zaslavsky, *A Mathematical Bibliography of Signed and Gain Graphs and Allied Areas*, Electronic Journal of Combinatorics, Dynamic Surveys in Combinatorics, DS8 (2018) &lbrack;[doi:10.37236/29](https://doi.org/10.37236/29)&rbrack;

[[!redirects signed graphs]]


