**Warning: Tentative.**

The _covering relation_ on a structure (generally already equipped with other relations) is a [[binary relation]] such that $x$ is related to $y$ if and only if $y$ is (in an appropriate sense) an *immediate* successor of $x$.

## In a poset ##

A pair $(x,y)$ in a [[poset]] satsfies the __covering relation__ if $x \lt y$ but there is no $z$ such that $x \lt z$ and $z \lt y$. In other words, there are exactly two elements $z$ such that $x \leq z \leq y$: $z = x$ and $z = y$.  In this case, you would say that "$y$ covers $x$".

## In a directed graph ##

A pair $(x,y)$ of vertices in a [[directed graph]] satisfies the __covering relation__ if there is an edge $x \to y$ but there is no vertex $z$ with edges $x\to z$ and $z\to y$.

## Common generalisation ##

Given any binary relation $\sim$ on a set $S$, a pair $(x,y)$ of elements of $S$ satisfies the __covering relation__ if $x \sim y$ but there is no $z$ such that $x \sim z$ and $z \sim y$.  Then the covering relation on a poset is the covering relation of $\lt$, and the covering relation in a directed graph is the covering relation of the adjacency relation of the graph.

## References ##

* [Wikipedia](http://en.wikipedia.org/wiki/Covering_relation)