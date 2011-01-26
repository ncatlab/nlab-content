Let $R$ be a (possibly noncommutative associative) ring ([[unital ring|unital]] or not). The collection of one sided (say right) ideals makes a [[partial order]] with respect to inclusions; a filter with respect to this partial order is a set of right ideals $F$ such that $R\in F$; if $I$,$J$ are right ideals, $I\in F$ and $I\subset J$ then $J\in F$; and if $I,J\in F$ then $I\cap J\in F$. 

A filter of ideals in $R$ is __topologizing__ if 

(i) it is [[uniform filter|uniform]], 
i.e. for any $I\in F$ and $r\in R$, the right ideal 

$$
(I:r) := \{s\in R \,|\, rs\in I\}
$$

is in $I$.

(ii) if $J\in F$ and $(I:r)\in I$ for all $r\in J$ then $I\in F$.

The term topologizing is explained by the following statement:

__Proposition.__ A topologizing set of right ideals in a ring $R$ is a basis of neighborhoods of $0$ for a topology on $R$. 

* Carl Faith, Algebra Vol. I, page 520

* Harold Simmons, _The semiring of topologizing filters of a ring_, [doi](http://dx.doi.org/10.1007/BF02772572)

[[!redirects topologizing filters]]