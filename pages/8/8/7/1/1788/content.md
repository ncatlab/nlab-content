

> This page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](https://ncatlab.org/nlab/history/Sandbox).

\linebreak


***

$$
  \left[
  \begin{matrix}
    1 & a & c
    \\
    0 & 1 & b
    \\
    0 & 0 & 1
  \end{matrix}
  \right]
  \cdot
  \left[
  \begin{matrix}
    1 & a' & c'
    \\
    0 & 1 & b'
    \\
    0 & 0 & 1
  \end{matrix}
  \right]
  \;=\;
  \left[
  \begin{matrix}
    1 & a + a' & c + c' + a b'
    \\
    0 & 1 & b + b'
    \\
    0 & 0 & 1
  \end{matrix}
  \right]
$$




The subgroup of boundary Dehn twists is central &lbrack;[Farb & Margalit 2012 p 77](mapping+class+group#FarbMargalit12)&rbrack;

* Netanel H. Lindner, Erez Berg, Gil Refael, [[Ady Stern]]: *Fractionalizing Majorana Fermions: Non-Abelian Statistics on the Edges of Abelian Quantum Hall States*, Phys. Rev. X **2** (2012) 041002 &lbrack;[doi:10.1103/PhysRevX.2.041002](https://doi.org/10.1103/PhysRevX.2.041002), [doi:10.1103/PhysRevX.2.041002](https://doi.org/10.1103/PhysRevX.2.041002), [arXiv:1204.5733](https://arxiv.org/abs/1204.5733)&rbrack;

* [[Juven C. Wang]], [[Xiao-Gang Wen]]: *Boundary Degeneracy of Topological Order*, Phys. Rev. B **91** (2015) 125124 &lbrack;[doi:10.1103/PhysRevB.91.125124](https://doi.org/10.1103/PhysRevB.91.125124), [arXiv:1212.4863](https://arxiv.org/abs/1212.4863)&rbrack;

* *Symmetry breaking vs topological order: weak symmetry breaking* &lbrack;[pdf](https://mcgreevy.physics.ucsd.edu/s14/final-papers/2014S-239a-Kuczala-Alexander.pdf)&rbrack;



Particle-hole symmetry.

Original

* S. M. Girvin: *Particle-hole symmetry in the anomalous quantum Hall effect*, Phys. Rev. B **29** (1984) 6012(R) &lbrack;[doi:10.1103/PhysRevB.29.6012](https://doi.org/10.1103/PhysRevB.29.6012)&rbrack;





$\neq \gt 1$ may be understood as $\nu = 1$ for majority spin polarization with $\nu - 1$ for the minority polarization (Haldane 1983 [doi:10.1103/PhysRevLett.51.605](https://sci-hub.se/10.1103/PhysRevLett.51.605))



\begin{tikzcd}[sep=5pt]
  _k \backslash ^q 
  \ar[-, rrrrrrrrrrrrrrr, shorten <=-40pt, shift right=4]
  \ar[-, ddddddddddddd, shorten <=-40pt, shift left=4]
  & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 & 9 & 10 & 11 & 12 & 13 & 14 & {}
  \\
  \bullet & 1 & 2 & \bullet &  \circ & \circ & \circ & \circ & \circ & \circ & \circ & \circ & \circ & \circ & \circ
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


\begin{tikzpicture}

\draw[thick] (0,0)--(3,0);

\end{tikzpicture}


So: 

1. in the column of $q = 1$ all odd $k$ are excluded and all even $k$ are admissible,

1. in the column of $q = 2$ all odd $k$ are excluded and exactly every second even $k$ is admissible,

1. in rows of odd $k$ the odd $q$ are excluded, and for even $q = 2 r$ the result is admissible iff the Jacobi symbol $(r \vert k) \neq 0$.


   Since the Jacobi symbol $(r \vert k)$ vanishes iff $gcd(r,k) \neq 1$, this means that, at least for odd $k$, exactly only the reduced fractions appear.
