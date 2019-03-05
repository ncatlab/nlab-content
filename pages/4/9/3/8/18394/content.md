## Idea

Formally, a cotopology of a topological space $X$ is a coarser topological space $^*X$ on the same set $X$ that does not forget too many sets.
The approach was introduced by J. D. Weston.
It can be used to generalize the [[Baire category theorem]] and to characterize [[topologically complete space|topological completeness]]. The pair of both topologies, the original and the coarser one, constitute an example of a [[bitopological space]].


## Definitions

+-- {: .num_defn}
###### Definition
Let $X$ be a topological space and set $\mathcal{O} = Op(X)$.
A topology $^*\mathcal{O}$ on $X$ is called a **cotopology** of $\mathcal{O}$---and $^*X = (X, ^*\mathcal{O})$ is called a **cospace** of $X$---if

1. $^*\mathcal{O}$ is coarser than $\mathcal{O}$, i.e., $^*\mathcal{O} \subseteq \mathcal{O}$; 
1. for each point $x$ and each $\mathcal{O}$-closed neighborhood $V$ of $x$ in $X$ there exists a $^*\mathcal{O}$-closed $\mathcal{O}$-neighborhood $U$ of $x$ in $X$ such that $U$ is contained in $V$.
=--

The last condition is equivalent to

* Each point $x$ has a neighborhood base in $X$ the elements of which are closed in $^*X$.


+-- {: .num_defn}
###### Definition
A topological space $X$ is called **cocompact** if there is a cospace $^*X$ of $X$ which is [[compact space|compact]].

=--

## Properties

Every cocompact [[regular space]] is a [[Baire space]]. A [[metrisable topological space|metrisable space]] is [[topologically complete space|topologically complete]] if and only if it is cocompact.

A space that admits only Hausdorff cospaces is equivalently an H-closed space, i.e. it (is Hausdorff and) is not a proper dense subspace of another space.

## References

The concept first appeared in

* J. D. Weston, _On the comparison of topologies_ 1956, 

de Groot used it to give a unifying and generalizing version of the [[Baire category theorem]]

* de Groot, _Subcompactness and the Baire category theorem_ 1963, Nederl. Akad. Wetensch. Proc., Ser. A66 = Indag. Math., vol. 25, pp. 761-767,

further developments include

* Aarts, de Groot, McDowell, _Cotopology for metrizable spaces_ 1970, Duke Mathematical Journal vol. 37.

* [[George Strecker]] and G. Viglino, _Cotopology and Minimal Hausdorff Spaces_ 1969, Proceedings of the American Mathematical Society
Vol. 21 No. 3.


[[!redirects cocompact space]]