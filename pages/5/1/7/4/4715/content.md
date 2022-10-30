
#Contents#
* table of contents
{:toc}

## Idea

A _ribbon graph_ (also called _fat graph_ ) is a finite connected [[graph]] equipped with a cyclic ordering on the half edges incident to each vertex; it is
also required that the valence of each vertex is at least 3. 

To each ribbon graph, one can associate an [[orientation|oriented]] [[surface]] with [[boundary]] by replacing edges
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


## Properties

For the following we represent a fat graph by

* a set $V$ of vertices;

* a set $H$ of half-edges;

* a source map $s : H \to V$;

* an involution $i :  H \to H$ which sends each half-edge to its partner half-edge;

* an permutation $\sigma : H \to H$ which gives the cyclic order on the edges.


### Geometric realization

For $\Gamma$ a fat graph, write $\Sigma_\Gamma$ for the [[surface]] that it defines.


+-- {: .num_prop}
###### Proposition

The [[boundary]] components of $\Sigma_\Gamma$ are naturally identified with the [[cycle]]s of $\sigma \circ i : H \to H$, as well as with the cycles of $i \circ \sigma$.

=--

+-- {: .num_prop}
###### Proposition

The [[genus]] of $\Sigma_\Gamma$ is

$$
  g = \frac{1}{2}
   \left(
     - \vert V\vert - \vert E\vert - \vert bounary components\vert + 2
   \right)
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

For every surface $S$ with boundary, there is a fat graph $\Gamma$ and a [[homeomorphism]]

$$
  S \stackrel{\simeq}{\to}  \Sigma_\Gamma
  \,.
$$

=--

### Moduli space of surfaces

Write $FatGraph^c_3$ for the [[full subcategory]] of fat graphs on the connected fat graphs for which every vertex has valence at leat 3. Write $\vert FatGraph^c_3 \vert \in $ [[Top]] for the [[geometric realization]] of this [[category]]. For $\Sigma$ a [[surface]], write $\Gamma_Sigma$ for its [[mapping class group]] and $B \Gamma_\Sigma$ for the corresponding [[classifying space]].

+-- {: .num_theorem}
###### Theorem

There is a [[weak homotopy equivalence]]

$$
  \vert FatGraph^c_3 \vert \simeq
  \coprod_{[\Sigma]} B \Gamma_\Sigma
  \,,
$$

where on the right thr coproduct ranges over isomorphism classes of orientable, closed 2-dimensional manifolds with $n \geq 1$ marked points, except those for which $(g,n) = (0,1)$ or  $(g, n) = (0,2)$.

=--

In various guises this theorem has been proven by [Costello](#Costello), [Kontsevich92](#Kontsevich92), [Igusa02](#Igusa02), [Penner](#Penner), [Strebel](#Strebel).

The restriction to valence $\geq 3$ can be dropped:

+-- {: .num_theorem}
###### Theorem

There is a [[weak homotopy equivalence]]

$$
  \vert FatGraph^c \vert \simeq
  B U(1) \coprod B U(1) \coprod_{[\Sigma]} B \Gamma_\Sigma
  \,,
$$

where again on the right thr coproduct ranges over isomorphism classes of orientable, closed 2-dimensional manifolds with $n \geq 1$ marked points, except those for which $(g,n) = (0,1)$ or  $(g, n) = (0,2)$. The two extra copies of $B U(1)$ corespond to these two exceptional cases.

=--

This has been shown in ([Godin](#Godin)). One of the $B U(1)$-summands is also produced in ([Igusa02](#Igusa02)). A detailed complete proof appears as ([Kuipers, theorem 3.59](#Kuipers)).


## Related concepts

* [[graph]]

* [[directed graph]]

  * [[directed n-graph]]

* **ribbon graph**

## References

Original references include

* [[Maxim Kontsevich]], _Intersection theory on the moduli space of curves and the matrix Airy function_ , Commun.
Math. Phys. (1992), no. 147, 1-23.
 {#Kontsevich92}
 
* [[Kiyoshi Igusa]], _Higher franz-reidemeister torsion_ , IP Studies in Advanced Mathematics, American Mathematical
Society, 2002.
 {#Igusa02}

* [[Kiyoshi Igusa]], _Graph cohomology and Kontsevich cycles_, Topology __43__ (2004), n. 6, p. 1469-1510, [MR2005d:57028](http://www.ams.org/mathscinet-getitem?mr=2005d:57028), [doi](http://dx.doi.org/10.1016/j.top.2004.03.004)
 {#Igusa04}

* K. Strebel, _Quadratic Differentials_, Springer, Berlin, 1984, [MR86a:30072](http://www.ams.org/mathscinet-getitem?mr=86a:30072)

* R. C. Penner, _The decorated Teichm&#252;ller space of punctured surfaces_, Commun. Math. Phys. __113__ (2) (1987) 299--339. [MR89h:32044](http://www.ams.org/mathscinet-getitem?mr=89h:32044)

* John Harer, _The cohomology of the moduli space of curves_, Lec. Notes in Math. __1337__, p. 138&#8211;221. Springer, Berlin, 1988.

* M. Mulas, M. Penkava, _Ribbon graphs, quadratic differentials on Riemann surfaces, and algebraic curves defined over_ $\overline{\bold Q}$. Mikio Sato: a great Japanese mathematician of the twentieth century.  Asian J. Math. __2__ (1998),  no. 4, 875--919. 

* [[Maxim Kontsevich]], _Feynman diagrams and low-dimensional topology_, First European Congress of Mathematics, 1992, Paris, vol. II, Progress in Mathematics __120__, Birkh&#228;user (1994), 97&#8211;121, [pdf](http://193.51.104.7/~maxim/TEXTS/Feynman%20%20diagrams%20and%20low-dimensional%20topology.pdf)

* Ib Madsen, Michael Weiss, _The stable moduli space of Riemann surfaces: [[Mumford's conjecture]]_,  Ann. of Math. (2) __165__ (2007), no. 3, 843--941, [MR2009b:14051](http://www.ams.org/mathscinet-getitem?mr=2009b:14051), [doi](http://dx.doi.org/10.4007/annals.2007.165.843)

* J. Conant, K. Vogtmann, _On a theorem of Kontsevich_, [math.QA/0208169](http://arxiv.org/abs/math/0208169)

* Gabriele Mondello, _Riemann surfaces, ribbon graphs and combinatorial classes_, [pdf](http://www.mat.uniroma1.it/~mondello/me/papers/ober-definitive.pdf)

* [[Veronique Godin]], _Higher string topology operations_ (2007)([arXiv:0711.4859](http://arxiv.org/abs/0711.4859))
 {#Godin}

A survey is in chapter 3 of 

* [[Sander Kuipers]], _String topology operations_ MSc thesis (2011)

Some discussion is at

* MathOverflow: [why does ribbon graph cohomology compute cohomology of mapping class group](http://mathoverflow.net/questions/51978/why-does-ribbon-graph-cohomology-compute-cohomology-of-mcg)

[[!redirects ribbon graphs]]

[[!redirects fat graph]]
[[!redirects fat graphs]]