##Idea##

A (directed) graph is a collection of edges which may stretch between (ordered) pairs of "points", called _vertices_.

A directed graph is like a [[category]] with units and composition forgotten. Indeed, a [[category]] is a directed graph with extra structure.  To formalize this idea, we say there is a [[forgetful functor]] 

$$U : Cat \to DiGraph$$

where [[DiGraph]] is the category of directed graphs and [[Cat]] is the category of small categories.  Moreover, this forgetful functor has a [[left adjoint]] 

$$F : DiGraph \to Cat $$

sending each directed graph to the [[free functor|free]] category on that graph.  A free category on a graph is called a [[quiver]].

##Definition##

An **abstract directed graph** $X$ is a [[category]] with

* one object $X_0$, called the object of _vertices_;

* one object $X_1$, called the object of _edges_;

* two morphisms $s,t : X_1 \to X_0$, called
the _source_ and _target_;

* together with identity morphisms.

A **directed graph** is a [[functor]] $G: X\to$ [[Set]].

More generally, a **directed graph [[internalization|in]] a category $C$** is a [[functor]] $G : X \to C$.

The category of directed graphs in $C$, [[DiGraph]], is the [[functor category]] $C^{X}$, where:

* objects are functors $G: X \to C$,

* morphisms are [[natural transformation|natural transformations]] between such functors.

In the basic case $C = Set$, we call this category the category of [[presheaf|presheaves]] on $X^{op}$.  So: the category of directed graphs, [[DiGraph]], is the category of presheaves on the category $X^{op}$.

##Remarks##

Let $G_0 = G(X_0)$ and $G_1 = G(X_1)$.

* A directed graph in $C$ is a [[presheaf]] on $X^{op}$ with values in $C$.

* A directed graph is a [[globular set]] which is concentrated in the first two degrees.

* Directed graphs includes multigraphs, i.e. graphs with distinct edges $e,e'\in G_1$ such that $s(e) = s(e')$ and $t(e) = t(e')$, as well as loops, i.e. edges with $s(e) = t(e)$.

##See also##
***
* [[directed n-graph|Directed n-graph]]
