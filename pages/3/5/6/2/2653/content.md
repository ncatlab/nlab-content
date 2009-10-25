**Warning: Tentative.**

The _covering relation_ on a structure (generally already equipped with other relations) is a [[binary relation]] such that $x$ is related to $y$ if and only if $y$ is (in an appropriate sense) an *immediate* (and *only* immediate) successor of $x$.

## In a poset ##

A pair $(x,y)$ in a [[poset]] satsfies the __covering relation__ if $x \lt y$ but there is no $z$ such that $x \lt z$ and $z \lt y$. In other words, there are exactly two elements $z$ such that $x \leq z \leq y$: $z = x$ and $z = y$.  In this case, you would say that "$y$ covers $x$".

## In a directed graph ##

A pair $(x,y)$ of vertices in a [[directed graph]] satisfies the __covering relation__ if there is an edge $x \to y$ but there is no other path from $x$ to $y$.

## Common generalisation ##

Given any binary relation $\sim$ on a set $S$, a pair $(x,y)$ of elements of $S$ satisfies the __covering relation__ if the only sequence $x = z_0, \ldots, z_n = y$ such that $x_i \sim x_{i+1}$ satisfies $n = 1$ (so $x \sim y$).  Then the covering relation on a poset is the covering relation of $\leq$, and the covering relation in a directed graph is the covering relation of the adjacency relation of the graph.

## References ##

* [Wikipedia](http://en.wikipedia.org/wiki/Covering_relation)