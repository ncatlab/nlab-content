
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Recall that an [[undirected graph]] $G$ consists of a set $V$ of _vertices_ and a set $E$ of unordered pairs of vertices. A **path** in $G$ is a finite sequence of vertices $x_0, \ldots, x_n$ such that each pair $x_i x_{i+1}$ belongs to $E$. If $x_n = x_0$, then the path is called a **cycle**. A graph is **connected** if it is nonempty and if for every distinct pair of vertices $x, y$, there is a path for which $x_0 = x$ and $x_n = y$. A graph is **acyclic** if the only cycles are paths 

$$x_0, \ldots, x_{n-1}, x_n, x_{n-1}, \ldots, x_0$$ 

where steps are retraced; an [[acyclic graph]] is also called a _[[forest]]_. A *[[tree]]* is a connected forest. 

Each forest is a [[disjoint union|disjoint sum]] (a [[coproduct]] in the category of graphs) of trees. Removal of a vertex of a tree (and any edges incident to it) results in a forest. 


## References

See also:

* Wikipedia, *[Polytree](https://en.wikipedia.org/wiki/Polytree)*

[[!redirects acyclic graphs]]

[[!redirects forest]]
[[!redirects forests]]

[[!redirects rooted forest]]
[[!redirects rooted forests]]


