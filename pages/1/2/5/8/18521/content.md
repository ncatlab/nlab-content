+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

In [[graph theory]], an **orientation** of an undirected [[graph]] is a choice of one of two possible directions for every [[edge]]. An **oriented graph** is an undirected graph equipped with an orientation.

Since the precise definition of "undirected graph" can vary depending on context (notably, whether one allows loops or multiple edges), the precise definition of "oriented graph" is likewise context dependent.

## Definitions

### Oriented simple graphs

In [[combinatorics]], the most common sense of "oriented graph" is "simple graph equipped with an orientation".

More formally: let $\binom{V}{2}$ denote the set of two-element subsets of $V$, 
and $\Delta \hookrightarrow V^2 = V \times V$ the diagonal $\{(v, v): v \in V\}$. Then there is a quotient map $q: V^2 \setminus \Delta \to \binom{V}{2}$, realizing $\binom{V}{2}$ as the set of orbits of the fixed-point free involution $(x, y) \mapsto (y, x)$ on $V^2 \setminus \Delta$. Then an oriented graph consists of a graph $(V, E \hookrightarrow \binom{V}{2}$ together with a section of the quotient $p$ identified in the pullback diagram 

$$\array{
F & \to & V^2 \setminus \Delta \\ 
\mathllap{p} \downarrow & & \downarrow \mathrlap{q} \\ 
E & \hookrightarrow & \binom{V}{2}.
}$$

Equivalently, an oriented graph consists of a set $V$ and a subset $E \hookrightarrow V^2$ such that $(x, y) \in E$ implies $(y, x) \notin E$. We may depict a pair $(x, y)$ in $E$ as an arrow from $x$ to $y$. Of course the condition rules out loops (arrows from a vertex to itself), and evidently the notion of oriented graph is very different from the notion of [[digraph]] where 2-cycles are allowed (an arrow from $x$ to $y$ and another back from $y$ to $x$). 

### More general graph orientations

If the underlying undirected graph is allowed to have loops and multiple edges, then an oriented graph is essentially the same thing as a [[directed graph]] (i.e., [[quiver]]).

Formally, let an undirected graph $G$ be given by a quiver $s,t : E \rightrightarrows V$ together with a [[fixed point]] free [[involution]] $i : E \to E$ such that $s\circ i = t$ and $t \circ i = s$ (in the style of [Serre 1977](#Serre1977)).
Then an orientation of $G$ consists of a subset $E^+ \subseteq E$ such that $E$ is the [[disjoint union]] $E = E^+ \uplus i(E^+)$.

Any such orientation induces a corresponding quiver $G^+ = E^+ \rightrightarrows V$.
Conversely, any quiver $E \rightrightarrows V$ can be seen as an orientation of the undirected Serre graph defined by adding a formal inverse to each edge.

Although the terms "oriented graph" and "directed graph" become essentially equivalent under this reading, in many situations it is useful to consider an oriented graph as one of the many possible orientations of a given undirected graph.
For example, various [[graph invariants]] (such as the [[flow polynomial]], or [[W. T. Tutte|Tutte]]'s original definition of the [[Tutte polynomial]]) can be defined relative to an arbitrary orientation of a graph, but are independent of the choice of orientation.

## References

* [[W. T. Tutte]], A contribution to the theory of chromatic polynomials. Canad. J. Math. 6:80&#8211;91, 1954. [(doi)](http://dx.doi.org/10.4153/CJM-1954-010-9)

* Frank Harary (1969), _Graph Theory_, Addison-Wesley.
* {#Serre1977} [[Jean-Pierre Serre]] (1977), _Trees_, Springer.
* [[W. T. Tutte]] (1984), _Graph Theory_, Addison-Wesley.
