#Idea#

A (directed) graph is a collection of edges which may stretch between (ordered) pairs of "points", called _vertices_.

#Definition#

A **directed graph** $G = (G_0,G_1)$ is 

* a collection $G_0$, called the collection of _vertices_;

* a collection $G_1$, called the collection of _edges_;

* together with two maps $s,t : G_1 \to G_0$, called
the _source_ and _target_ maps.

A _loop_ is an edge $e\in G_1$ with $s(e) = t(e).$

More generally, a **directed graph [[internalization|internal to]] an ambient [[category]]** $C$ is

* an object $G_0 \in C$, called the object of _vertices_;

* an object $G_1 \in C$, called the object of _edges_;

* together with two morphisms $s,t : G_1 \to G_0$ in $C$, called the _source_ and _target_ morphisms.

##Examples##

* A directed graph internal to $Sets$ is a _small_ directed graph: one where the collections of edges and vertices form sets.



##Remarks##

* A directed graph is a [[globular set]] which is concentrated in the first two degrees.

* Note that this definition includes multigraphs, i.e. graphs with distinct edges $e,e'\in G_1$ such that $s(e) = s(e')$ and $t(e) = t(e')$, as well as loops, i.e. edges with $s(e) = t(e)$.

* A directed graph is like a [[category]] with units and composition forgotten. Indeed, a [[category]] is a directed graph with extra structure.

###See also###
***
* [[directed n-graph|Directed n-graph]]
