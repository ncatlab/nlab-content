## Idea

A ribbon graph (also called fat graph) is a finite connected graph equipped with a cyclic ordering on the half edges incident to each vertex; it is
also required that the valence of each vertex is at least 3. 

## Definition

Set theoretically, a __ribbon graph__ is given by a finite set of half edges, equipped with two (unordered) [[partitions]]:

(i) into subsets which we call *vertices*; each with cardinality at least 3

(ii) into *pairs of half-edges* called *edges*

and with a cyclic ordering of ("on") each vertex. Without a cyclic ordering, 
we will just say graph. 

The half-edges belonging to the same vertex are said to be *incident*. An edge is a *loop* if its constituent half-edges are incident. 

## Further constructions

Given any edge $e$ in a graph $\Gamma$, 
we can collapse it to a new graph $\Gamma/e$ by merging the two vertices
containing the edge and removing both half edges.  

A forest $F$ (disjoint union of trees) spans a graph $\Gamma$ if it contains all of its vertices. One can collapse $\Gamma$ to $\Gamma/F$ by collapsing each tree to a separate vertex. Then the edges in $\Gamma/F$ are the edges of $\Gamma$ which do not lie in any tree in $F$; the vertices of $\Gamma/F$ correspond to the sets of leaves of the component trees of $F$.  

A morphism of graphs $\Gamma_0\to\Gamma_1$ is defined as an isomorphism $\Gamma_0/F\to\Gamma_1$ where $F$ is a spanning forest of $\Gamma_0$. Morphisms of such graphs are both epi and mono. 

For  a ribbon graph, the set of leaves of any tree inherits a cyclic order. Thus $\Gamma/F$ has a canonical structure a ribbon graph. This makes the following definition possible: A morphism of ribbon graphs is the morphism of underlying graphs which respects the ordering on the vertices; i.e.  $\Gamma_0/F\to\Gamma_1$ is an isomorphism of ribbon graphs. Every endomorphism of a ribbon graph is an automorphism and for any two ribbon graphs $\Gamma$ and $\Gamma'$, the set $Aut(\Gamma)$ acts freely on $Hom(\Gamma,\Gamma')$ on the right and $Aut(\Gamma')$ acts freely on it from the left. 

Let $\mathcal{Fat}$ denote the category of ribbon graphs and ribbon automorphisms. Strebel proved that the geometric realization $|\mathcal{Fat}|$ of the category of ribbon graphs decmposes into a direct sum of classifying spaces of all [[mapping class group]]s $M^s_g$ 

$$
|\mathcal{Fat}| = \coprod_{g,s} BM^s_g
$$

$M^s_g$ is a mapping class group of a surface of genus $g$ with $s$ punctures. 

## Applications

...

## References

* K. Igusa, _Graph cohomology and Kontsevich cycles_, Topology __43__ (2004), n. 6, p. 1469-1510, [MR2005d:57028](http://www.ams.org/mathscinet-getitem?mr=2005d:57028), [doi](http://dx.doi.org/10.1016/j.top.2004.03.004)

[[!redirects ribbon graphs]]