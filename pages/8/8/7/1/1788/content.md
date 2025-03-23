

> This page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](https://ncatlab.org/nlab/history/Sandbox).


***

**Extension of irreps of normal subgroups**

* [[I. Martin Isaacs]]: Thm. 11.7 in: *Character theory of finite groups*, Academic Press, New York (1976) &lbrack;[ISBN:978-0-8218-4229-4](https://bookstore.ams.org/view?ProductCode=CHEL/359.H)&rbrack;

* Peter Schmid: *Extending irreducible representations of normal subgroups*, Journal of Algebra **94** 1 (1985) 30-51 \[<a href="https://doi.org/10.1016/0021-8693(85)90203-0">doi:10.1016/0021-8693(85)90203-0</a>\]

* *Extending characters from normal subgroups*, in *Topics in Algebra*, Lecture Notes in Mathematics **697** (2006) 1–7 &lbrack;[doi:10.1007/BFb0103119](https://doi.org/10.1007/BFb0103119)&rbrack;

* G. Karpilovsky: *On extension of characters from normal subgroups*, Proceedings of the Edinburgh Mathematical Society **27** (1984) 7-9 &lbrack;[doi:10.1017/S0013091500022057](https://doi.org/10.1017/S0013091500022057), [pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/B051526AE20F219C468AFBF1D9546E43/S0013091500022057a.pdf/on_extension_of_characters_from_normal_subgroups.pdf)&rbrack;

* Qiang Huang: *Extension of irreducible characters from normal subgroups*, Linear and Multilinear Algebra **27** 2 (1990) &lbrack;[doi;10.1080/03081089008818001](https://doi.org/10.1080/03081089008818001)&rbrack;



\begin{tikzcd}[sep=5pt]
  _k \backslash ^q 
  \ar[-, rrrrrrrrrrrrrrr, shorten <=-40pt, shift right=4]
  \ar[-, ddddddddddddd, shorten <=-40pt, shift left=4]
  & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 & 9 & 10 & 11 & 12 & 13 & 14 & {}
  \\
  1 & 1 & 2 & \bullet &  \circ & \circ & \circ & \circ & \circ & \circ & \circ & \circ & \circ & \circ & \circ
  \\
  2 & \tfrac{1}{2} & \bullet & \tfrac{3}{2} & 2 & \circ & \circ & \circ & \circ  & \circ  & \circ  & \circ & \circ & \circ & \circ
  \\
  3 & \bullet & \tfrac{2}{3} & \bullet & \tfrac{4}{3} & \bullet & \bullet  & \circ  & \circ  & \circ  & \circ  & \circ & \circ & \circ & \circ
  \\ 
  4 & \tfrac{1}{4} & \tfrac{1}{2} & \tfrac{3}{4} & \bullet & \tfrac{5}{4} & \tfrac{3}{2} & \tfrac{7}{4} & 2 & \circ & \circ & \circ & \circ & \circ & \circ
  \\
  5 & \bullet & \tfrac{2}{5} & \bullet & \tfrac{4}{5} & \bullet & \tfrac{6}{5} & \bullet & \tfrac{8}{5} & \bullet & \bullet & \circ & \circ & \circ & \circ
  \\
  6 & \tfrac{1}{6} & \bullet & \tfrac{1}{2} & \tfrac{2}{3} & \tfrac{5}{6} & \bullet & \tfrac{7}{6} & \tfrac{4}{3} & \tfrac{3}{2} & \bullet & \tfrac{11}{6} & \bullet & \circ & \circ
  \\
  7 & \bullet & \tfrac{2}{7} & \bullet & \tfrac{4}{7} & \bullet & \tfrac{6}{7} & \bullet & \tfrac{8}{7} & \bullet & \tfrac{10}{7} & \bullet & \tfrac{12}{7} & \bullet & \bullet
  \\
  8 & \tfrac{1}{8} & \tfrac{1}{4} & \tfrac{3}{8} & ? & ? & ? & ? & ? & ? & ? & ? & ? & ? & ?
  \\
  9 & \bullet & \tfrac{2}{9} & \bullet & \tfrac{4}{9} & \bullet & \bullet & \bullet & \tfrac{8}{9} & \bullet & \tfrac{10}{9} & \bullet & \bullet  & \bullet & \tfrac{14}{9}
  \\
  10 & \tfrac{1}{10} & \bullet & ? & ? & ? & ? & ? & ? & ? & ? & ? & ? & ? & ? 
  \\
  11 & \bullet & \tfrac{2}{11} & \bullet & \tfrac{4}{11} & \bullet & \tfrac{6}{11} & \bullet & \tfrac{8}{11} & \bullet & \tfrac{10}{11} & \bullet & \tfrac{12}{11} & \bullet & \tfrac{14}{11}
  \\
  12 & \tfrac{1}{12} & \tfrac{1}{6} & \tfrac{1}{4} & \bullet & \tfrac{5}{12} & \tfrac{1}{2} & \tfrac{7}{12} & \tfrac{2}{3} & \tfrac{3}{4} & \tfrac{5}{6} & \tfrac{11}{12} & \bullet & \tfrac{13}{12} & \tfrac{7}{6}
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


   Since the Jacobi symbol $(r \vert k)$ vanishes iff $gcd(r,k) \neq 1$, this means that, at least for odd $k$, exactly only the reduced fractions appear.
