##Idea##

A directed $n$-graph, or $n$-digraph, is a higher dimensional generalization of a [[directed graph]] with $r$-dimensional _edges_ spanning $(r-1)$-dimensional _vertices_.

A directed $n$-graph is like an [[n-category]] with units and composition forgotten. Indeed, an $n$-category is a directed $n$-graph with extra structure.  To formalize this idea, we say there is a [[forgetful functor]] 

$$U : n\Cat \to n\DiGraph$$

where $n\DiGraph$ is the category of directed $n$-graphs and $n\Cat$ is the category of small $n$-categories.  Moreover, this forgetful functor has a [[adjoint functor|left adjoint]] 

$$F : n\DiGraph \to n\Cat $$

sending each directed $n$-graph to the free $n$-category on that $n$-graph.  A free $n$-category on an $n$-graph is called an $n$-[[quiver]].


##Definition##

An **abstract directed $n$-graph** $X$ is a [[category]] with

* objects $X_r$ of $r$-dimensional edges (or **$r$-edges**) for $0 \le r \le n$;

* morphisms $s_r,t_r : X_{r+1} \to X_r$, called
**sources** and **targets** for $0\le r \lt n$;

* together with identity morphisms $\mathrm{Id}_r:X_r\to X_r$ for $0\le r\le n$.

A **directed $n$-graph** is a [[functor]] $G:X\to$ [[Set]].

A **directed $n$-graph in a category $C$** is a [[functor]] $G:X\to C$.

An $r$-edge $e\in G_r$ is called an **identity** (or **$r$-loop**) if

$$s(e) = t(e).$$

A morphism $i_r: X_r\to X_{r+1}$ sending an $r$-edge to its respective $(r+1)$-loop, when defined, is called an **identity assigning map**. Identity assigning maps satisfy

$$s_r\circ i_r = \mathrm{Id}_r$$
$$t_r\circ i_r = \mathrm{Id}_r.$$

When identity assignment maps are defined for all $0\le r\lt n$, the directed $n$-graph is referred to as a **directed $n$-graph with identities**.

##Remarks##

* A directed $n$-graph is not required to contain identities.

Let $G_r = G(X_r)$, $s_r = G(s_r)$, $t_r = G(t_r)$.

* Any two consecutive objects $G_r,G_{r+1}$ together with morphism $s_r,t_r,\mathrm{Id}_r,\mathrm{Id}_{r+1}$ constitute a [[directed graph]]. In particular, a directed 1-graph is a [[directed graph]].

* One can define a (globular) _directed $\omega$-graph_ (or _directed $\infty$-graph_) in a [[coalgebra|coalgebraic]] fashion as follows: A directed $\omega$-graph $G$ consists of a collection $G_0$ of vertices and, for each pair of vertices $x$ and $y$, a directed $\omega$-graph $\Hom(x,y)$. (This is a definition by [[structural coinduction]].) Can this be continued to a corecursive definition of $\infty$-[[infinity-category|category]]?

##See also##
***
* $\omega$-[[omega-graph|graph]]


[[!redirects n-digraph]]