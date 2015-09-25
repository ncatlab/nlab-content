
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

## Idea

In an ordinary undirected [[graph]], each edge $e$ links an [[unordered pair]] of vertices $x$ and $y$ (perhaps allowing for the possibility that $x = y$, as in the case of a loop).  Hypergraphs generalize this, allowing a "hyperedge" to link any set of "hypervertices" (or any [[non-empty set]] in some formulations).

## As 2-colored graphs

Any hypergraph $H$ induces a [[vertex coloring|2-colored]] (hence necessarily [[bipartite graph|bipartite]]) graph $G(H)$, called its _incidence graph_.  The hypervertices $v$ and hyperedges $e$ of $H$ are represented respectively as black vertices $b_v$ and white vertices $w_e$ of $G(H)$, with an edge $b_v \sim w_e$ in $G(H)$ if and only if $v \in e$.   Conversely, any 2-colored graph $G$ determines a hypergraph $H(G)$, where each white vertex $w$ is interpreted as a hyperedge $e_w = \{v_b \mid b \sim w\}$ connecting all of the hypervertices associated to its (black vertex) neighbors.  (Note this could result in empty hyperedges, in the case that $G$ contained isolated white vertices.)

## Related concepts

* [[hypermap]]
* [[hyperstructure]]

## References

* T. R. S. Walsh, _Hypermaps Versus Bipartite Maps_, Journal of Combinatorial Theory (B) 18, 155-163 (1975).

* W. D&#246;rfler and D. A. Waller, _A category-theoretical approach to hypergraphs_, Archiv der Mathematik, Volume 34, Number 1, (1980) 185-192, DOI: 10.1007/BF01224952

[[!redirects hypergraphs]]

