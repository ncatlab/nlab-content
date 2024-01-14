A *signed graph* is an undirected [[graph]] (e.g., a simple graph, which is a set $V$ of *vertices* together with a collection $E$ of two-element subsets of $V$ called *edges*) plus a function from $E$ to a two-element set of "signs", e.g., $\sigma: E \to \{+, -\}$. 

If $\binom{V}{2}$ denotes the set of two-element subsets of $V$, a signed *simple* graph could be equivalently defined to be a set $V$ together with a [[partial function]] $\binom{V}{2} \to \{+, -\}$. The domain of this partial function is declared to be $E$, so the data of a signed graph can be represented as $V$ together with a [[span]] of type 
$$\binom{V}{2} \hookleftarrow E \stackrel{\sigma}{\to} \{+, -\}.$$ 

Signed graphs are *not* *directed graphs*: signs on undirected edges are not the same as directional information. For example, if vertices represent people and edges represent being acquainted then the signs could indicate being allies or enemies.
If a [[linear order]] has been imposed on the vertex set, then the sign function can be interpreted as imparting directions to edges (say if $x \lt y$ in the order and an edge $e$ between $x$ and $y$ has sign $+$, then the direction is $x \to y$; if $e$ has sign $-$, then the direction is $y \to x$). However, such linear orders on vertices will not be preserved by morphisms of signed graphs, so this does not give a [[functor|functorial]] way to derive directed graphs from signed graphs. 

A fundamental property of a signed graph is the signs of its cycles.  The sign of a cycle is the product of the signs of its edges.

A *homomorphism* of signed graphs is a function between vertex sets which preserves signed-graph structure.  There are several kinds of homomorphism, depending on which signed-graph structure is preserved.  One type is *sign preserving*, i.e., the mapping preserves the signs of edges.  Another type, called a *switching homomorphism*, preserves the signs of cycles but not necessarily of edges.

Signed graphs (and the basic theorems of their theory) seem to be rediscovered again and again. See [Zaslavsky](#ZaslavskyBibliography) for an annotated bibliography on signed graphs and their various guises.  


## References 

* Thomas Zaslavsky: [ _A Mathematical Bibliography of Signed and Gain Graphs and Allied Areas_](http://www.combinatorics.org/ojs/index.php/eljc/article/view/DS8), Electronic Journal of Combinatorics, Dynamic Surveys in Combinatorics, #DS8.
{#ZaslavskyBibliography}
