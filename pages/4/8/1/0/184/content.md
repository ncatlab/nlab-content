##Idea##

A directed $n$-graph is a higher dimensional generalization of a [[directed graph]] with $r$-dimensional _edges_ spanning $(r-1)$-dimensional _vertices_.

##Definition##

A **directed $n$-graph** $G = \prod_{r=0}^n G_r$ is 

* a collection $G_r$ of $r$-dimensional edges (or **$r$-edges**) for $0 \le r \le n$;

* together with two maps $s,t : G_r \to G_{r-1}$, called
the **source** and **target** maps, where $G_{-1}$ is the empty set.

An $r$-edge $e\in G_r$ is called an **identity** (or **$r$-loop**) if

$$s(e) = t(e).$$

An **identity assigning map** is a map $i:G_r\to G_{r+1}$ satisfying

$$s\circ i = \mathrm{Id}$$
$$t\circ i = \mathrm{Id}$$

when defined. When identity assignment maps are defined for all $r\ge 0$, the directed $\infty$-graph is referred to as a **directed $\infty$-graph with identities**.

##Remarks##

* A directed 1-graph is a [[directed graph]].

* A directed $n$-graph is not required to contain identities.

* A directed $n$-graph is like an [[n-category]] with units and composition forgotten. Indeed, an [[n-category]] is a directed $n$-graph with extra structure.

* One can defined a (globular) _directed $\omega$-graph_ (or _directed $\infty$-graph) in a [[coalgebra|coalgebraic]] fashion as follows: A directed $\omega$-graph $G$ consists of a collection $G_0$ of vertices and, for each pair of vertices $x$ and $y$, a directed $\omega$-graph $\Hom(x,y)$. (This is a definition by [[structural coinduction]].) Can this be continued to a corecursive definition of $\omega$-[[omega-category|category]] (or $\infty$-[[infinity-category|category]])?

##See also##
***
* $\omega$-[[omega-graph|graph]]