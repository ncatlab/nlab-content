\tableofcontents

\section{Idea}

A _cyclic permutation_ is, roughly speaking, a [[permutation]] in which, if we view the elements of a finite set as people standing in a circle, everybody shifts one step to the right, or everybody shifts one step to the left. 

\section{Formal definition}

Recall that a [[permutation]] of a [[finite set]] $X$ can formally be defined to be a [[bijection]] $X \rightarrow X$.

\begin{defn} Let $X$ be a finite set with $n$ elements. Fix an isomorphism $i : X \rightarrow \{ 1, \ldots, n \}$. A _cyclic permutation_ of $X$ is a permutation $p: X \rightarrow X$ of $X$ such that either the following diagram commutes where $\sigma$ is the permutation of $\{ 1, \ldots, n \}$ given by $i \mapsto i+1$ for $1 \leq i \leq n-1$ and by $n \mapsto 1$

\begin{centre}

\begin{tikzcd}
X \arrow[r, "i"] \arrow[d, swap, "p"] & \{ 1, \ldots, n \} \arrow[d, "\sigma"] \\
X \arrow[r, swap, "i"] & \{ 1, \ldots, n \}
\end{tikzcd}

\end{centre}

or it commutes where $\sigma$ is given by $i \mapsto i-1$ for $2 \leq i \leq n$ and $1 \mapsto n$. 

\end{defn}

\begin{rmk} There are a number of equivalent definitions. \end{rmk} 