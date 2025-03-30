## Idea

A (proper) **vertex coloring** of a [[graph]] is a labelling of its vertices with the property that no two vertices sharing an edge have the same label, while an **$n$-coloring** is a vertex coloring using at most $n$ distinct labels. The **chromatic number** $\chi(G)$ of a graph $G$ is the least $n$ such that $G$ has an $n$-coloring.

Vertex coloring may also be expressed in terms of graph homomorphisms: a $n$-coloring of $G$ is the same thing as a graph homomorphism $G \to K_n$ into the complete graph on $n$ vertices.
This formulation makes clear the duality between colorings and _cliques_: an $n$-[[clique]] in $G$ is the same thing as a homomorphism $K_n \to G$.

## Definitions

Vertex coloring is functorial; a homomorphism $f : G \rightarrow H$ of graphs existing means that $\chi(G) \le \chi(H)$, since any n-coloring $c : H \to K_n$ of $H$ can be extended to $G$ by $f \circ c$. There are many categories of graphs, but to be general, given some cardinal $\kappa$ (almost always assumed to be $|\mathbb{N}|$) let

$\mathbf{Grph}_+$ be the category of sets smaller than $\kappa$ with a symmetric relation

* $\mathbf{Grph}$ be the subcategory of $\mathbf{Grph}_+$ spanned by the irreflexive relations

* $\kappa_+$ be the poset of cardinalities less than or equal to $\kappa$

* $\kappa$ be the poset of cardinalities less than $\kappa$

* $\chi(G) := min\{n | Hom(G, K_n) \ne \emptyset\}$ keeping in mind that $min$ is the product in a poset

Then $\chi : \mathbf{Grph}_+ \to \kappa_+$ and $\mathbf{Grph} \to \kappa$. $\mathbf{Grph}_+$ is a nicer category to work in, since it has a terminal object, but it means that not all graphs can technically be colored, so we can identify the chromatic number of a graph with a loop to $\kappa$, since no graph of size < $\kappa$ could actually have a $\kappa$-coloring.

It [[hom-functor preserves limits|makes sense]] from the definition that $\chi$ preserves coproducts (disjoint unions), and it preserves the terminal object (graph with one object and loop), so it's easy to assume it preserves products too, but this question has actually been open since 1966 under the name [[Hedetniemi's conjecture]]. 

## Related concepts

* [[knot coloring]]

## References

* Chris Godsil and Gordon Royle (2001), _Algebraic Graph Theory_, Springer.

* Pavol Hell and Jaroslav Nešetřil (2001), _Graphs and Homomorphisms_, Oxford University Press.

Two posts by [[Tom Leinster]] at the n-Category Caf&#233; on vertex-coloring and a categorical formulation of _Hedetniemi's conjecture_:

* [[Tom Leinster]], ["Colouring a Graph"](https://golem.ph.utexas.edu/category/2013/04/colouring_a_graph.html), n-Category Caf&#233; post of April 12, 2013.

* [[Tom Leinster]], ["Graph Colouring and Cartesian Closed Categories"](https://golem.ph.utexas.edu/category/2014/12/graph_colouring_and_cartesian.html), n-Category Caf&#233; post of December 5, 2014.

Other references:

* Wikipedia: [Graph coloring](https://en.wikipedia.org/wiki/Graph_coloring)