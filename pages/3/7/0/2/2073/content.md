# Idea #

Marked simplicial sets are [[simplicial set]]s with a little bit of extra [[stuff, structure, property|structure]] that allows to model [[Cartesian fibration]]s of [[simplicial set]]s precisely as the fibrations with respect to a certain [[model category]] structure on marked simplicial sets.

# Definition #

A **marked simplicial set** is 

* a pair $(S,E)$ consisting of 

  * a [[simplicial set]] $S$ 

  * and a subset $E \subset S_1$ of edges of $S$, called the _marked edges_, 

* such that

  * all degenerate edges are marked.

A morphism $(S,E) \to (S',E')$ of marked simplicial sets is a morphism $f : S \to S'$ of [[simplicial set]]s that carries marked edges to marked edges in that $f(E) \subset E'$.

# References #

Section 3.1 of

* [[Jacob Lurie]], [[Higher Topos Theory]]
