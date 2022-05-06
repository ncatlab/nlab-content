## Idea

Formally, a cotopology of a topological space $(X, \mathcal{T})$ is a coarser topology $\mathcal{T}^*$ on the same set $X$ that does not forget too many sets.
It can be used to generalize the [[Baire category theorem]] and to characterize [[topologically complete space|topological completeness]]. The pair of both topologies, the original and the coarser one, constitute an example of a [[bitopological space]].


## Definitions

\begin{definition}
Let $(X, \mathcal{T})$ be a topological space.
A topology $\mathcal{T}^*$ on $X$ is called a __cotopology__ of $\mathcal{T}$---and $(X, \mathcal{T}^*)$ is called a __cospace__ of $(X, \mathcal{T}$---if

1. $\mathcal{T}^*$ is coarser than $\mathcal{T}$, i.e., $\mathcal{T}^* \subseteq \mathcal{T}$; 

1. for each point $x$ and each $\mathcal{T}$-closed $\mathcal{T}$-neighborhood $V$ of $x$ in $X$ there exists a $\mathcal{T}^*$-closed $\mathcal{T}$-neighborhood $U$ of $x$ in $X$ such that $U$ is contained in $V$.

\end{definition}

If $\mathcal{T}$ is [[regular space|regular]], the last condition can be replaced by other conditions, see [[bitopological space#implications|this proposition]].

\begin{definition}
A topological space $X$ is called __cocompact__ if there is a cotopology $\mathcal{T}^*$ on $X$ which is [[compact space|compact]].
\end{definition}

## Properties

Every cocompact [[regular space]] is a [[Baire space]]. A [[metrisable topological space|metrisable space]] is [[topologically complete space|topologically complete]] if and only if it is cocompact.

A space that admits only Hausdorff cospaces is equivalently an H-closed space, i.e. it (is Hausdorff and) is not a proper dense subspace of another space.


## Related Concepts

* [[bitopological space]]

## References

The concept principally appeared in

* J. D. Weston, _On the comparison of topologies_ 1956, Journal of the London Mathematical Society, vol. s1-32 no. 3, pp. 342-354.

De Groot made cotopologies popular by giving a unifying and generalizing version of the [[Baire category theorem]]

* de Groot, _Subcompactness and the Baire category theorem_ 1963, Nederl. Akad. Wetensch. Proc., Ser. A66 = Indag. Math., vol. 25, pp. 761-767.

In this context some 

* _Colloquium co-topologie_ at the _Mathematisch Centrum_, today _[Centrum Wiskunde & Informatica](https://www.cwi.nl/)_, in Amsterdam in 1964 

is mentioned.
Further developments include

* Aarts, de Groot, McDowell, _Cotopology for metrizable spaces_ 1970, Duke Mathematical Journal vol. 37.

* [[George Strecker]] and G. Viglino, _Cotopology and Minimal Hausdorff Spaces_ 1969, Proceedings of the American Mathematical Society Vol. 21 No. 3.


[[!redirects cocompact space]]