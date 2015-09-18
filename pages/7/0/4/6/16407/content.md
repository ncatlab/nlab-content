#Contents#
* table of contents
{:toc}

## Definition

A **topological map** (or **embedded graph**) $M$ is a [[graph]] $G = (V,E,d)$ (loops and multiple edges allowed) equipped with an embedding $\theta$ of $G$ into a [[surface]] $X$ in such a way that:

1. vertices $x \in V$ are represented as distinct points $\theta(x) \in X$;

2. edges $e \in E$ are represented as curves $\theta(e)$ on the surface $X$ that intersect only at the vertices;

3. the complement $X \setminus \theta(G)$ of the graph on the surface is a disjoint union of connected components, called _faces_, each [[homeomorphic]] to an open [[disk]] (in other words, each face is [[simply connected]]).

These conditions can be summarized by saying that $\theta$ is a _cellular embedding_ (or "2-cell embedding").

A morphism of topological maps $(G,X,\theta) \to (G',X',\theta')$ is a continuous function between the underlying spaces $f : X \to X'$ whose restriction to $\theta(G)$ defines a homomorphism of graphs $f : G \to G'$.
Sometimes one may place additional conditions on the underlying surfaces and limit the morphisms between them accordingly.  For instance, typically one might assume that $X$ is [[compact space|compact]], [[connected space|connected]], [[oriented]] and without [[boundary]], and consider a map on $X$ as defined up to orientation-preserving homeomorphism.

Topological maps inherit various properties of their underlying surfaces: for instance, a graph embedded in a connected surface is itself necessarily a connected graph.  One also speaks of the _genus_ of a map $(G,X,\theta)$ as the [[genus of a surface|genus]] of the underlying surface $X$.

## Embedded graphs versus abstract graphs

It is important to distinguish topological maps, which are graphs equipped with an embedding, from graphs which may happen to have the property of being embeddable in different surfaces.  For example, a **planar map** is a graph equipped with a cellular embedding into the [[sphere]], while a **planar graph** is a graph which is _graph isomorphic_ to the underlying graph of a planar map.  Two planar graphs are considered equivalent if they are isomorphic as graphs $G_1 \cong G_2$, but two planar maps are only considered equivalent if this isomorphism of graphs can be realized on their embeddings $\theta_1(G_1) \cong \theta_2(G_2)$ by a homeomorphism of the sphere.  In particular, one planar graph might have multiple, inequivalent embeddings into the sphere.

To emphasize the distinction between embedded graphs and graphs which may happen to be embeddable, one sometimes refers to the latter as **abstract graphs**.[^Bartlett]

[^Bartlett]: For more on the distinction between embedded graphs and abstract graphs, see [[Bruce Bartlett]]'s n-Category Caf&#233; post on  [Feynman's Fabulous Formula](https://golem.ph.utexas.edu/category/2015/06/feynmans_fabulous_formula.html).


## Permutation representations

One of the remarkable properties of topological maps is that they can be given a purely algebraic representation as a collection of permutations satisfying a few properties.  For now, see the articles ([[cartographic group]]) and ([[combinatorial map]]).

## Related concepts

* [[combinatorial map]]

* [[ribbon graph]]

* [[child's drawing]]

* [[cartographic group]]

* [[branched cover of the Riemann sphere]]

## References

A formal treatment of topological maps (including the relationship to [[algebraic maps]] and the definition of several associated categories) is in

* [[Gareth A. Jones]] and [[David Singerman]], Theory of Maps on Orientable Surfaces. Proceedings of the London Mathematical Society, 37:273-307, 1978.

Fairly elementary sources for background material include:
 
* Arthur T. White: 1984 _Graphs, groups and surfaces_
  {#White1984}

This gives the Edmonds algorithm which given a graph and some permutations outputs an embedding. The original source for that is:

* J. Edmonds (1960), A combinatorial representation for polyhedral surfaces, Notices Amer. Math. Soc. 7, 646.

More recent treatments can be found in:

* Sergei K. Lando and Alexander K. Zvonkin, _Graphs on Surfaces and Their Applications_, Springer, 2004.

* Roman Nedela, _Maps, Hypermaps and Related Topics_, 2007. ([pdf](http://www.savbb.sk/~nedela/CMbook.pdf))

Wikipedia:

* [Graph embedding](https://en.wikipedia.org/wiki/Graph_embedding)

[[!redirects topological maps]]
[[!redirects embedded graph]]
[[!redirects embedded graphs]]
