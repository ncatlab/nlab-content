# Idea

A **subsequential space** is a set equipped with a notion of _sequential convergence_, giving it a "topology" in an informal sense. Any [[topological space]] becomes a subsequential space with its standard notion of convergence, but only for a [[sequential space]] can the topology be recovered from sequential convergence.  In the other direction, not every subsequential space is induced by a topological one.

Despite these apparent drawbacks, subsequential spaces have a number of advantages.  Their definition is arguably more intuitive than that of a topological space.  Continuity of functions between subsequential spaces is likewise easy to define, by preservation of convergent sequences.  And since subsequential spaces include all sequential spaces, they include many spaces of interest to topologists, including all metrizable spaces and all CW complexes; thus they can be regarded as a sort of [[nice topological space]].  Furthermore, the category of subsequential spaces is _also_ a [[nice category of spaces]]: it is [[locally cartesian closed category|locally cartesian closed]] and in fact a [[quasitopos]], and the embedding of sequential spaces into subsequential ones preserves most important categorical structure: all [[limit]]s and many [[colimit]]s.  Since it is a "Grothendieck quasitopos," it is also [[locally presentable category|locally presentable]].


# Definition

A **subsequential space** is a set $X$ equipped with a relation between sequences and points, called "converges to," with the following properties.

1. For every $x\in X$, the constant sequence $(x)$ converges to $x$.

1. If a sequence $(x_n)$ converges to $x$, then so does any subsequence of $x$.

1. If, for some sequence $(x_n)$ and some point $x$, every subsequence of $(x_n)$ contains a further subsequence converging to $x$, then $(x_n)$ itself converges to $x$.

The final property can be stated less [[constructive mathematics|constructively]] as "if $(x_n)$ does not converge to $x$, then there is a subsequence $(x_{n_k})$ of $(x_n)$ such that no subsequence of $(x_{n_k})$ converges to $x$."



# References

* P. T. Johnstone, _On a topological topos_.  Proc. London Math. Soc. (3) 38 (1979) 237--271
