
#Contents#
* table of contents
{:toc}


## Idea  

Given a group action on a graph $Y$ (with involution on the edges), one gets a quotient graph $X=Y/G$ together the family of the stabilisers on the vertices and on the edges. Abstracting this gives a graph of groups.


## Definition

A graph of groups $\Gamma(G,X)$ consists of

* a connected graph, $X$;

*  a function, $G$, which, for every vertex, $v\in V(X)$ assigns a group, $G_v$, and for each edge, $e\in E(X)$ assigns a group, $G_e$ such that $G_e= G_\overline{e}$

* For each edge, $e\in E(X)$, there exists a monomorphism, $\sigma::G_e\to G_{i(e)}$, where $i(e)$ is the initial vertex of the edge, $e$.

##References

* [[J.-P. Serre]], 1977, _Arbres, amalgames, SL2_, volume 46 of Astérisque, Société mathématique de France.

* [[J.-P. Serre]], 2003, _Trees_, Springer Monographs in Mathematics, Springer- Verlag Berlin

* [[H. Bass]], _Covering theory for graphs of groups_, Journal of Pure and Applied Algebra, 89, (1993), 3–47.