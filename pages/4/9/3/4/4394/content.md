
# Bitopological space
* table of contents
{: toc}

## Definitions

Recall that a [[topological space]] is a [[set]] $X$ equipped with a [[topological structure]] $\mathcal{T}$.  Well, a __bitopological space__ is simply a set equipped with *two* topological structures $(X, \mathcal{T}, \mathcal{T}^*)$.  Unlike with [[bialgebras]], no compatibility condition is required between these structures.

A __bicontinous map__ is a [[function]] between bitopological spaces that is [[continuous map|continuous]] with respect to each topological structure.

Bitopological spaces and bicontinuous maps form a [[category]] $BiTop$.

## Compatibility conditions for topologies


\begin{definition}\label{regular}
Let $(X, \mathcal{T}, \mathcal{T}^*)$ be a bitopological space.
The topology $\mathcal{T}$ is __regular with respect to__ $\mathcal{T}^*$ if  one of the following two equivalent conditions holds

1. For each point $x$ there is a $\mathcal{T}$-[[neighborhood base]] consisting  of $\mathcal{T}^*$-closed sets; 
1. for all $x\in X$ and all $\mathcal{T}$-opens containing $x$ there is a $\mathcal{T}^*$-closed $\mathcal{T}$-neighborhood $V$ of $x$ such that $ V \subset U$.

A bitopological space $(X, \mathcal{T}, \mathcal{T}^*)$ is called __pairwise regular__ if $\mathcal{T}$ is regular with respect to $\mathcal{T}^*$ and wise versa.
\end{definition}

\begin{proof}
Given a neighborhood base for a point $x$ as guaranteed by the first property. When you spell out the properties of this neighborhood base, you end up with the second property. For the reverse direction start with an arbitrary $\mathcal{T}$-neighborhood base of a point $x$ consisting of open. Apply the second property to every element of this neighborhood base to the desired neighborhood base.
\end{proof}

Let $Cl$ denote the [[closure operator]] with respect to $\mathcal{T}$ and let $Cl^*$ denote the closure operator with respect to $\mathcal{T}^*$.

\begin{definition}\label{coupled}
Let $(X, \mathcal{T}, \mathcal{T}^*)$ be a bitopological space.
The topology $\mathcal{T}^*$ is __coupled to__ $\mathcal{T}^*$ if one of the following two equivalent conditions holds

1. $Cl^*(O) \subset Cl(O)$ for each $\mathcal{T}^*$-open $O$; 

1. for all $x\in X$ and all $\mathcal{T}$-neighborhoods $U$ of $x$ the closure $Cl^*(U)$ is a $\mathcal{T}$-neighborhood.

\end{definition}

\begin{proof}
Suppose the first property, and let $U$ be a $\mathcal{T}$-neighborhood of an arbitrary point $x$. Then the [[complement]] $ \widetilde{Cl^*(U)} $ is in $\mathcal{T}^*$, so that $ Cl^*(\widetilde{Cl^*U}) \subset Cl(\widetilde{Cl^* U}) $ by the first property. Hence $ \widetilde{Cl(\widetilde{Cl^*U})} \subset \widetilde{Cl^*(\widetilde{Cl^* U})} $ for the complements.
Since $U$ is a $\mathcal{T}$-neighborhood of $x$, $x$ does not belong to $Cl(\widetilde{Cl^*U})$. 
Moreover, $\widetilde{Cl^*(\widetilde{Cl^*U})} $ is $\mathcal{T}^*$-open and a subset of $ Cl^*(U)$.
Hence $Cl^*(U)$ is a $\mathcal{T}^*$-neighborhood of $x$.

For the converse suppose the second property. Let $O$ be a nonempty $\mathcal{T}^*$-open set and $x$ an element of $Cl^*(O)$. Then if $U$ is any $\mathcal{T}$-neighborhood of $x$, some point $y \in O$ belongs to $Cl^*(U)$ due to the second property. Hence, as $O$ is a $\mathcal{T}^*$-neighborhood of $y$, some point of $U$ belongs to $O$. Thus $x \in Cl(O)$, and therefore $Cl^*(G) \subset Cl(O)$. 
\end{proof}

\begin{proposition}
There are the following implications between the properties from definitions \ref{regular} and \ref{coupled} as well as the property

* for each point $x$ and each $\mathcal{T}$-closed $\mathcal{T}$-neighborhood $V$ of $x$ in $X$ there exists a $\mathcal{T}^*$-closed $\mathcal{T}$-neighborhood $U$ of $x$ in $X$ such that $U$ is contained in $V$.



Especially, all properties are equivalent if $$ is [[regular space|regular]].
\end{proposition}

\begin{centre}
\begin{tikzpicture}
	\usetikzlibrary{arrows.meta}
	\usetikzlibrary{matrix}
  \matrix (m) [matrix of nodes,row sep=3em,column sep=5em,minimum width=2em]
{
	 & (R2)	& (C1) \\
	(*) & (R1) & (C1) \\};
\path[-stealth] 
	(m-2-1) edge[double] node[above left] {\scriptsize if $\mathcal{T}$ regular} (m-1-2)
	(m-1-2) edge[stealth-stealth, double] (m-2-2)
	(m-1-3) edge[stealth-stealth, double] (m-2-3)
	(m-2-2) edge[double] (m-2-1)
	(m-1-3) edge[double] node[above] {\scriptsize if $\mathcal{T}$ regular} (m-1-2)
	(m-2-2) edge[double] (m-2-3)
	(m-2-2) edge[double, bend right] node[below] {\scriptsize if $\mathcal{T}^*\subset \mathcal{T}$} (m-2-3);
\end{tikzpicture}
\end{centre}

## Remarks

It is interesting and perhaps surprising that many advanced topological notions can be described using bitopological spaces, even when you would not na&#239;vely think that there are two topologies around.  (At least, that\'s my vague memory of what they were good for.  I think that this was in some article by Isbell.)

## Related Articles

* [[cotopology]]
* [[topologically complete space]]


## References

* [Wikipedia entry](http://en.wikipedia.org/wiki/Bitopological_space)

* [[Jiri Adamek]], [[Horst Herrlich]], and [[George Strecker]], _Abstract and Concrete Categories: The Joy of Cats_ , Dover New York 2009. ([pdf](http://katmat.math.uni-bremen.de/acc/acc.pdf)) pp.59-60,278

* B. Dvalishvili, _Bitopological Spaces: Theory, Relations with Generalized Algebraic Structures and Applications_ , Elsevier Amsterdam 2005.

* [[Peter Johnstone]], _Collapsed Toposes as Bitopological Spaces_ , pp.19-35 in _Categorical Topology_ , World Scientific Singapore 1989.

* O. K. Klinke, A. Jung, A. Moshier, _A bitopological point-free approach to compactications_ (2011). ([preprint](http://www.cs.bham.ac.uk/~axj/pub/papers/compactifications.pdf))

* R. Kopperman, _Asymmetry and duality in topology_ , Topology Appl. **66** no.1 (1995) pp.1-39.

The notions of respective regularity, being coupled, etc. were introduced in

* J. D. Weston, _On the comparison of topologies_ 1956, Journal of the London Mathematical Society, vol. s1-32 no. 3, pp. 342-354,

* J. C. Kelly, _Bitopological spaces_ , Proc. London Math. Soc. **13** no.3 (1963) pp.71-89.

[[!redirects bitopological space]]
[[!redirects bitopological spaces]]
[[!redirects Bitop]]
[[!redirects BiTop]]
[[!redirects Bi Top]]
