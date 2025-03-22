

> This page may be edited by anybody, anytime. (To recover edits, see the [page history](https://ncatlab.org/nlab/history/Sandbox).)


***

\begin{tikzcd}[sep=5pt]
  _k \backslash ^q 
  \ar[-, rrrrrrrrrrrr, shorten <=-40pt, shift right=4]
  \ar[-, ddddddddddddd, shorten <=-40pt, shift left=4]
  & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 & 9 & 10 & 11 & {}
  \\
  1 & 1 & 2 & \bullet &  \circ & \circ & \circ & \circ & \circ & \circ & \circ & \circ
  \\
  2 & \tfrac{1}{2} & \bullet & ? & ? & \circ & \circ & \circ & \circ  & \circ  & \circ  & \circ
  \\
  3 & \bullet & \tfrac{2}{3} & \bullet & \tfrac{4}{3} & \bullet & \bullet  & \circ  & \circ  & \circ  & \circ  & \circ
  \\ 
  4 & \tfrac{1}{4} & \tfrac{1}{2} & ? & ? & ? & ? & ? & ? & \circ & \circ & \circ
  \\
  5 & \bullet & \tfrac{2}{5} & \bullet & \tfrac{4}{5} & \bullet & \tfrac{6}{5} & \bullet & \tfrac{8}{5} & \bullet & \bullet & \circ
  \\
  6 & \tfrac{1}{6} & \bullet & ? & ? & ? & ? & ? & ? & ? & ? & ?
  \\
  7 & \bullet & \tfrac{2}{7} & \bullet & \tfrac{4}{7} & \bullet & \tfrac{6}{7} & \bullet & \tfrac{8}{7} & \bullet & \tfrac{10}{7} & \bullet
  \\
  8 & \tfrac{1}{8} & \tfrac{1}{4}
  \\
  9 & \bullet & \tfrac{2}{9} & \bullet & \tfrac{4}{9} & \bullet & \bullet & \bullet & \tfrac{8}{9} & \bullet & \tfrac{10}{9} & \bullet
  \\
  10 & \tfrac{1}{10} & \bullet
  \\
  11 & \bullet & \tfrac{2}{11} & \bullet & \tfrac{4}{1} & \bullet & \tfrac{6}{11} & \bullet & \tfrac{8}{11} & \bullet & \tfrac{10}{11} & \bullet
  \\
  12 & \tfrac{1}{12} & \tfrac{1}{6}
  \\
  {}
\end{tikzcd}

Here

* "$\bullet$" means that the corresponding combination of $(k,q)$ is not admissible, in that $k q$ is odd or the [[Gauss sum]] $\sum_{n=0}^{k-1} e^{ \tfrac{\pi \mathrm{i}}{k} q n^2 } = 0$.

* "$\circ$" means that $\tfrac{q}{k} \gt 2$


So: 

1. in the column of $q = 1$ all odd $k$ are excluded and all even $k$ are admissible,

1. in the column of $q = 2$ all odd $k$ are excluded and exactly every second even $k$ is admissible,

1. in rows of odd $k$ the odd $q$ are excluded, and for even $q = 2 r$ the result is admissible iff the Jacobi symbol $(r \vert k) \neq 0$.
