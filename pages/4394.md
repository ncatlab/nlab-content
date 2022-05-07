
# Bitopological space
* table of contents
{: toc}

## Definitions

Recall that a [[topological space]] is a [[set]] $X$ equipped with a [[topological structure]] $\mathcal{T}$.  Well, a __bitopological space__ is simply a set equipped with *two* topological structures $(X, \mathcal{T}, \mathcal{T}^*)$.  Unlike with [[bialgebras]], no compatibility condition is required between these structures.

A __bicontinous map__ is a [[function]] between bitopological spaces that is [[continuous map|continuous]] with respect to each topological structure.

Bitopological spaces and bicontinuous maps form a [[category]] $BiTop$.

## Separation axioms for topologies

Let $Cl$ denote the [[closure operator]] with respect to $\mathcal{T}$ and let $Cl^*$ denote the closure operator with respect to $\mathcal{T}^*$.

\begin{proposition}\label{implications}
Let $(X, \mathcal{T}, \mathcal{T}^*)$ be a bitopological space.
Consider the following properties of this space:

1. {#regular1} for each point $x$ there is a $\mathcal{T}$-[[neighborhood base]] consisting  of $\mathcal{T}^*$-closed sets; 

1. {#regular2} for all $x\in X$ and all $\mathcal{T}$-opens $U$ containing $x$ there is a $\mathcal{T}^*$-closed $\mathcal{T}$-neighborhood $V$ of $x$ such that $ V \subset U$;

1. {#coupled1} $Cl^*(O) \subset Cl(O)$ for each $\mathcal{T}^*$-open $O$; 

1. {#coupled2} for all $x\in X$ and all $\mathcal{T}$-neighborhoods $U$ of $x$ the closure $Cl^*(U)$ is a $\mathcal{T}^*$-neighborhood;

1. {#cotopology2} for each point $x$ and each $\mathcal{T}$-closed $\mathcal{T}$-neighborhood $V$ of $x$ in $X$ there exists a $\mathcal{T}^*$-closed $\mathcal{T}$-neighborhood $U$ of $x$ in $X$ such that $U$ is contained in $V$.

There are the following implications among these properties

\begin{centre}
  \begin{tikzcd}
	 & (2)	& (3) \\
	(5) & (1) & (4)
    \arrow[Rightarrow, from=2-1, to=1-2, "\text{if $\mathcal{T}$ regular}"] 
    \arrow[Leftrightarrow, from=1-2, to=2-2]
    \arrow[Leftrightarrow, from=1-3, to=2-3]
    \arrow[Rightarrow, from=2-2, to=2-1]
    \arrow[Rightarrow, from=1-3, to=1-2, "\text{if $\mathcal{T}$ regular}"]
    \arrow[Rightarrow, from=2-2, to=2-3]
\end{tikzcd}
\end{centre}

Especially, all properties are equivalent if $\mathcal{T}$ is [[regular space|regular]].
\end{proposition}

\begin{proof}
__[(1)](#regular1) $\iff$ [(2)](#regular2):__
Given a neighborhood base for a point $x$ as guaranteed by the first property. When you spell out the properties of this neighborhood base, you end up with the second property. For the reverse direction start with an arbitrary $\mathcal{T}$-neighborhood base of a point $x$ consisting of open. Apply the second property to every element of this neighborhood base to the desired neighborhood base.

__[(3)](#coupled1) $\iff$ [(4)](#coupled2):__
Suppose property [(3)](#coupled1), and let $U$ be a $\mathcal{T}$-neighborhood of an arbitrary point $x$. Then the [[complement]] $ \widetilde{Cl^*(U)} $ is in $\mathcal{T}^*$, so that $ Cl^*(\widetilde{Cl^*U}) \subset Cl(\widetilde{Cl^* U}) $ by the first property. Hence $ \widetilde{Cl(\widetilde{Cl^*U})} \subset \widetilde{Cl^*(\widetilde{Cl^* U})} $ for the complements.
Since $U$ is a $\mathcal{T}$-neighborhood of $x$, $x$ does not belong to $Cl(\widetilde{Cl^*U})$. 
Moreover, $\widetilde{Cl^*(\widetilde{Cl^*U})} $ is $\mathcal{T}^*$-open and a subset of $ Cl^*(U)$.
Hence $Cl^*(U)$ is a $\mathcal{T}^*$-neighborhood of $x$.

For the converse suppose property [(4)](#coupled2). Let $O$ be a nonempty $\mathcal{T}^*$-open set and $x$ an element of $Cl^*(O)$. Then if $U$ is any $\mathcal{T}$-neighborhood of $x$, some point $y \in O$ belongs to $Cl^*(U)$ due to the second property. Hence, as $O$ is a $\mathcal{T}^*$-neighborhood of $y$, some point of $U$ belongs to $O$. Thus $x \in Cl(O)$, and therefore $Cl^*(G) \subset Cl(O)$. 

__[(1)](#regular1) $\implies$ [(4)](#coupled2):__
Given $x\in X$ and a $\mathcal{T}$-neighborhood $U$ by property [(1)](#regular1) there is a $\mathcal{T}^*$-open $O \subset U$ containing $x$. Hence $O \subset Cl^*(U)$, and $Cl^*(U)$ is a $\mathcal{T}^*$-neighborhood. 

__[(3)](#coupled1) and $\mathcal{T}$ regular $\implies$ [(2)](#regular2):__
Let $x\in X$ and $U$ be a $\mathcal{T}$-open containing $x$. 
By regularity of $\mathcal{T}$ we can find disjoint $\mathcal{T}$-opens $V' \ni x$ and $U' \supset \tilde{U}$ ($\tilde{U}$ denotes the [[complement]]). Set $V \coloneqq Cl^*(V')$. This set is obviously a $\mathcal{T}^*$-closed $\mathcal{T}$-neighborhood of $x$. Due to property [(3)](#coupled1) $V \subset Cl(V')$. Since also $Cl(V') \subset \widetilde{U'}$, we have $V \subset U$. This is to say that $V$ is the $\mathcal{T}$-neighborhood we sought.

__[(5)](#cotopology2) and $\mathcal{T}$ regular $\implies$ [(2)](#regular2):__
Let $x\in X$ and $U$ be a $\mathcal{T}$-open containing $x$. By regularity of $\mathcal{T}$ we can find disjoint $\mathcal{T}$-opens $V' \ni x$ and $U' \supset \tilde{U}$ ($\tilde{U}$ denotes the [[complement]]). Due to property [(5)](#cotopology2) the closed set $\widetilde{U'}$ contains a $\mathcal{T}^*$-closed neighborhood of $x$. This is the neighborhood we sought. 

__[(1)](#regular1) $\implies$ [(5)](#cotopology2):__
Given some $\mathcal{T}$-closed $\mathcal{T}$-neighborhood $V$ of some point $x$ choose a neighborhood base according to property [(1)](#regular1) and take an element $U$ therein that is contained in $V$.
\end{proof}


\begin{definition}\label{regular}
Let $(X, \mathcal{T}, \mathcal{T}^*)$ be a bitopological space.
The topology $\mathcal{T}$ is __regular with respect to__ $\mathcal{T}^*$ if  one of the two equivalent conditions [(1)](#regular1) and [(2)](#regular2) from proposition \ref{implications} holds.
A bitopological space $(X, \mathcal{T}, \mathcal{T}^*)$ is called __pairwise regular__ if $\mathcal{T}$ is regular with respect to $\mathcal{T}^*$ and vise versa.
\end{definition}

\begin{definition}\label{coupled}
Let $(X, \mathcal{T}, \mathcal{T}^*)$ be a bitopological space.
The topology $\mathcal{T}^*$ is __coupled to__ $\mathcal{T}$ if one of the two equivalent conditions [(3)](#coupled1) and [(4)](#coupled2) from proposition \ref{implications} holds.
\end{definition}

Not that is if $\mathcal{T}^*$ is coupled to a finer topology $\mathcal{T} \supset \mathcal{T}^*$ then $\mathcal{T}^*$ is coupled to every topology coarser than $\mathcal{T}$ due to property [(3)](#coupled1). Moreover in this case also $\mathcal{T}$ is coupled to $\mathcal{T}^*$ (again a direct consequence of property [(3)](#coupled1)).

\begin{definition}\label{cotopology}
Let $(X, \mathcal{T}, \mathcal{T}^*)$ be a bitopological space.
The topology $\mathcal{T}^*$ is called a __[[cotopology]] of__ $\mathcal{T}$ if $\mathcal{T}^* \subseteq \mathcal{T}$ and property [(5)](#cotopology2) from proposition \ref{implications} holds.
The space $(X, \mathcal{T}^*)$ is also called a __cospace__ of $(X, \mathcal{T}$.
\end{definition}

## Remarks

It is interesting and perhaps surprising that many advanced topological notions can be described using bitopological spaces, even when you would not naively think that there are two topologies around.  (At least, that's my vague memory of what they were good for.  I think that this was in some article by Isbell.)

## Pointfree analogues

Expressed in the opposite category of [[frames]],
there are several pointfree analogues of bitopological spaces:
[[D-frames]], [[biframes]], and [[finitary biframes]].
The latter has the best properties of all three.
For an overview, see Suarez \cite{Suarez}.

## Related Articles

* [[cotopology]]
* [[topologically complete space]]


## References

* [Wikipedia entry](http://en.wikipedia.org/wiki/Bitopological_space)

* [[Jiri Adamek]], [[Horst Herrlich]], and [[George Strecker]], _Abstract and Concrete Categories: The Joy of Cats_, Dover New York 2009. ([pdf](http://katmat.math.uni-bremen.de/acc/acc.pdf)) pp. 59-60, 278

* B. Dvalishvili, _Bitopological Spaces: Theory, Relations with Generalized Algebraic Structures and Applications_, Elsevier Amsterdam 2005.

* [[Peter Johnstone]], _Collapsed Toposes as Bitopological Spaces_, pp. 19-35 in _Categorical Topology_, World Scientific Singapore 1989.

* O. K. Klinke, A. Jung, A. Moshier, _A bitopological point-free approach to compactications_ (2011). ([preprint](http://www.cs.bham.ac.uk/~axj/pub/papers/compactifications.pdf))

* R. Kopperman, _Asymmetry and duality in topology_, Topology Appl. **66** no. 1 (1995) pp. 1-39.

The idea naturally appeared first in the context of quasi-metric spaces

* Wallace Alvin Wilson, _On Quasi-Metric Spaces_, American Journal of Mathematics (1931), vol. 53, no. 3, pp. 675-684.

The notions of separation axioms were introduced in

* J. D. Weston, _On the comparison of topologies_ 1956, Journal of the London Mathematical Society, vol. s1-32 no. 3, pp. 342-354,

* J. C. Kelly, _Bitopological spaces_, Proc. London Math. Soc. **13** no.3 (1963) pp. 71-89.

Only Kelly introduced the concept in its nowadays formulation of a set equipped with two topologies. The Russian school contributed the following comprehensive overviews of this and related topics

* A. A. Ivanov, _Problems of the Theory of Bitopological Spaces_, 1990, Journal of Soviet Mathematics, vol. 52, Issue 1, pp. 2759-2790. Originally published as _Проблематика теории битопологических пространств_ in Zap. Nauchn. Sem. POMI, 1988, vol. 167 ([Russian version](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=znsl&paperid=5560&option_lang=en)).

* A. A. Ivanov, _Problems of the Theory of Bitopological Spaces 2_, 1996, Journal of Math. Sciences, vol. 81, Issue 2. Originally publishes as _Проблематика теории битопологических пространств. 2_ in Zap. Nauchn. Sem. POMI, 1993, Volume 208, pp. 5–67 ([Russian version](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=znsl&paperid=5828&option_lang=eng)).

* A. A. Ivanov, _Problems of the Theory of Bitopological Spaces 3_, 1998, Journal of Math. Sciences, vol. 91, Issue 6, pp 3339–3364. Originally published as _Проблематика теории битопологических пространств. 3_ in Zap. Nauchn. Sem. POMI, 1995, Volume 231, pp. 9–54 ([Russian version](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=znsl&paperid=3739&option_lang=eng)).

as well as a more introductory text book

* A. A. Ivanov, N. V. Khmylko, _Битопологические пространства_, 1997. Исследования по топологии. 9, Zap. Nauchn. Sem. POMI, 242, editor A. A. Ivanov ([Russian version](http://www.mathnet.ru/php/archive.phtml?jrnid=znsl&wshow=issue&bshow=contents&series=0&year=1997&volume=242&issue=&option_lang=rus&bookID=335)).

Stone duality for bitopological spaces with applications to domain theory is studied in 

* Achim Jung and M. Andrew Moshier: [On the bitopological nature of Stone duality](https://www.cs.bham.ac.uk/~axj/pub/papers/Jung-Moshier-2006-On-the-bitopological-nature-of-Stone-duality.pdf). Technical Report CSR-06-13. School of Computer Science, University of Birmingham, 2006.

The pointfree analogues of bitopoligal spaces are reviewed in

* Anna Laura Suarez,
_The category of finitary biframes as the category of pointfree bispaces_,
[arXiv:2010.04622](https://arxiv.org/abs/2010.04622).


[[!redirects bitopological space]]
[[!redirects bitopological spaces]]
[[!redirects Bitop]]
[[!redirects BiTop]]
[[!redirects Bi Top]]
