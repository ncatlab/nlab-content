\tableofcontents

\section{Introduction}

A semi-graph is like a _graph_ (more precisely, an undirected, simple graph, possibly with loops) but where certain edges may be 'open' or 'half-open': they may have a vertex at only one end, or at neither end. As usual, edges can only be joined at vertices. A vertex is typically indicated by a solid dot (possibly with a label), an end of edge without a vertex is typically indicated by a hollow dot (never with a label).

Here is a quick example, which has one edge without any vertices, and two edges with only one vertex.

\begin{centre}
  \begin{tikzpicture}
    \draw (0,0) -- (0,2) -- (2,2) -- (2,0) -- (0,0);
    \draw (2,2) -- (2,4);
    \draw (2,0) -- (4,0);
    \draw (0,-2) -- (2,-2);
    \fill (0,0) circle[radius=0.1];
    \fill (0,2) circle[radius=0.1];
    \fill (2,2) circle[radius=0.1];
    \fill (2,0) circle[radius=0.1];
    \draw (2,4) circle[radius=0.1]; 
    \draw (4,0) circle[radius=0.1];
    \draw (0,-2) circle[radius=0.1]; 
    \draw (2,-2) circle[radius=0.1];
  \end{tikzpicture}
\end{centre}   

\section{Preliminaries}

Throughout this page, we pick a set with exactly one element, and denote it $1$. 

\section{Details}

The following definition follows [Mochizuki2006](#Mochizuki2006).

\begin{defn} A _semi-graph_ consists of a set $V$, a set $E$ whose elements are sets with exactly two elements, and, for every element $e$ of $E$, a map $\zeta_{e}: e \rightarrow V \sqcup 1$.
 \end{defn}

\begin{terminology} Let $G$ be a semi-graph. A _vertex_ of $G$ is an element of $V$. An _edge_ of $G$ is an element of $E$. An edge $e$ of $G$ _abuts_ to a vertex $v$ of $G$ if $v$ belongs to the [[image]] of $\zeta_{e}$. We refer to an element of an edge $e$ of $G$ as a _branch_ of $e$.   \end{terminology}

\begin{rmk} In particular, every edge of a semi-graph has exactly two branches, but it is possible that neither, both, or only one of the branches abuts a vertex. Thus we think of an edge $e$ as subdivided into two branches $b_{1}$ and $b_{2}$, and do not think of the meeting point as a vertex of the graph; but always consider the other end of each branch as a vertex, either 'closed' (the branch maps to an actual vertex of $G$ under $\zeta_{e}$) or 'open' (the branch maps to $1$ under $\zeta_{e}$).   

\begin{centre}
  \begin{tikzpicture}
    \draw (0,0) to node[auto] {\large $b_{1}$} (2,0) to node[auto] {\large $b_{2}$} (4,0);
    \fill (0,0) circle[radius=0.1];
    \draw (4,0) circle[radius=0.1];
    \node[anchor=north] at (0,-0.2) {\large $v$};
  \end{tikzpicture}
\end{centre}

\end{rmk}


\section{References}

* _Semi-graphs of anabelioids_, [[Shinichi Mochizuki]], Publ. Res. Inst. Math. Sci., 42, No. 1, 221-322 (2006). [paper](http://www.kurims.kyoto-u.ac.jp/~motizuki/Semi-graphs%20of%20Anabelioids.pdf) [Zentralblatt review](https://zbmath.org/?q=an%3A1113.14025) {#Mochizuki2006}