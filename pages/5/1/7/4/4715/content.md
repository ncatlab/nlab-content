
#Contents#
* table of contents
{:toc}

## Idea

A ribbon graph (also called fat graph) is a finite connected graph equipped with a cyclic ordering on the half edges incident to each vertex; it is
also required that the valence of each vertex is at least 3. To each ribbon graph, one can associate an oriented surface with boundary by replacing edges
by thin oriented rectangles (ribbons) and glueing them together at all vertices according to the chosen cyclic order.

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

For  a ribbon graph, the set of leaves of any tree inherits a cyclic order. Thus $\Gamma/F$ has a canonical structure a ribbon graph. This makes the following definition possible: A morphism of ribbon graphs is the morphism of underlying graphs which respects the ordering on the vertices; i.e.  $\Gamma_0/F\to\Gamma_1$ is an isomorphism of ribbon graphs. Every endomorphism of a ribbon graph is an automorphism and for any two ribbon graphs $\Gamma$ and $\Gamma'$, the set $Aut(\Gamma)$ acts freely on $Hom(\Gamma,\Gamma')$ on the right and $Aut(\Gamma')$ acts freely on $Hom(\Gamma,\Gamma')$ from the left. 

Let $\mathcal{Fat}$ denote the category of ribbon graphs and ribbon automorphisms. Strebel proved that the geometric realization $|\mathcal{Fat}|$ of the category of ribbon graphs decomposes into a direct sum of classifying spaces of all [[mapping class group]]s $M^s_g$ 

$$
|\mathcal{Fat}| = \coprod_{g,s} BM^s_g
$$

$M^s_g$ is a mapping class group of a surface of genus $g$ with $s$ punctures. Alternatively, one can instead of the geometric realization take a moduli space of ribbon graphs with metric. A **metric** on a ribbon graph is a positive real valued function on the set of edges. 

## Applications

...

## References

* K. Igusa, _Graph cohomology and Kontsevich cycles_, Topology __43__ (2004), n. 6, p. 1469-1510, [MR2005d:57028](http://www.ams.org/mathscinet-getitem?mr=2005d:57028), [doi](http://dx.doi.org/10.1016/j.top.2004.03.004)

* K. Strebel, _Quadratic Differentials_, Springer, Berlin, 1984, [MR86a:30072](http://www.ams.org/mathscinet-getitem?mr=86a:30072)

* R. C. Penner, _The decorated Teichm&#252;ller space of punctured surfaces_, Commun. Math. Phys. __113__ (2) (1987) 299--339. [MR89h:32044](http://www.ams.org/mathscinet-getitem?mr=89h:32044)

* John Harer, _The cohomology of the moduli space of curves_, Lec. Notes in Math. __1337__, p. 138&#8211;221. Springer, Berlin, 1988.

* M. Mulas, M. Penkava, _Ribbon graphs, quadratic differentials on Riemann surfaces, and algebraic curves defined over_ $\overline{\bold Q}$. Mikio Sato: a great Japanese mathematician of the twentieth century.  Asian J. Math. __2__ (1998),  no. 4, 875--919. 

* [[Maxim Kontsevich]], _Feynman diagrams and low-dimensional topology_, First European Congress of Mathematics, 1992, Paris, vol. II, Progress in Mathematics __120__, Birkh&#228;user (1994), 97&#8211;121, [pdf](http://193.51.104.7/~maxim/TEXTS/Feynman%20%20diagrams%20and%20low-dimensional%20topology.pdf)

* Ib Madsen, Michael Weiss, _The stable moduli space of Riemann surfaces: [[Mumford's conjecture]]_,  Ann. of Math. (2) __165__ (2007), no. 3, 843--941, [MR2009b:14051](http://www.ams.org/mathscinet-getitem?mr=2009b:14051), [doi](http://dx.doi.org/10.4007/annals.2007.165.843)

* J. Conant, K. Vogtmann, _On a theorem of Kontsevich_, [math.QA/0208169](http://arxiv.org/abs/math/0208169)

* Gabriele Mondello, _Riemann surfaces, ribbon graphs and combinatorial classes_, [pdf](http://www.mat.uniroma1.it/~mondello/me/papers/ober-definitive.pdf)

[[!redirects ribbon graphs]]