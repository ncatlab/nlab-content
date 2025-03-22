

> This page may be edited by anybody, anytime.


***

\begin{tikzcd}[sep=5pt]
  _k \backslash ^q 
  \ar[-, rrrrrr, shorten <=-40pt, shift right=4]
  \ar[-, dddddd, shorten <=-40pt, shift left=4]
  & 1 & 2 & 3 & 4 & 5 & {}
  \\
  1 & \times & 2 & \times &  \circ & \circ
  \\
  2 & \tfrac{1}{2} & \times & ? & 2 & \circ
  \\
  3 & \times & \tfrac{2}{3} & \times & \tfrac{4}{3} & ? 
  \\ 
  4 & \tfrac{1}{4} & \tfrac{1}{2} & ? & ?
  \\
  5 & \times & \tfrac{2}{5} & ? & \tfrac{4}{5}
  \\
  {}
\end{tikzcd}

Here

* "$\times$" means that the corresponding combination of $(k,q)$ is not admissible, in that $k q$ is odd or $\sum_{n=0}^{k-1} e^{ \tfrac{\pi \mathrm{i}}{k} q n^2 } = 0$.

* "$\circ$" means that $\tfrac{q}{k} \gt 2$