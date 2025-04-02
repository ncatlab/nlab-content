

> This page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](https://ncatlab.org/nlab/history/Sandbox).


\linebreak

***




In [[representation theory]], the notion of *twisted intertwiners* is a generalization of that of *[[intertwiners]]*. 

References using the exact terminology "twisted intertwiner" include [Fuchs & Schweigert 2000a (7.2)](#FuchsSchweigert00), [2000b (2.2)](#FuchsSchweigert00b), [Felder, Fröhlich, Fuchs & Schweigert 2000 (4.7)](#FelderFröhlichFuchsSchweigert00), but the notion itself is older and may be known under other names.

## Definition

\begin{definition}
For $G$ a [[group]] and $\rho_1, \rho_2 \;\in\; Rep(G)$ a [[pair]] of [[linear representation]] on [[vector spaces]] $V_1$, $V_2$, respectively (all this generalizes straightforwardly to [[algebras]] and their [[modules]]), a *twisted intertwiner*

$$
  \rho_1 \Rightarrow \rho_2
$$

is 

1. an [[automorphism]] $\alpha \in Aut(G)$ of the group

1. a [[linear map]] $\eta \colon V_1 \longrightarrow V_2$

such that for all $g \in G$ we have

$$
  \eta \circ \rho_1(g)
    \;=\;
  \rho_2\big(\alpha(g)\big) \circ \eta
  \,.
$$

Given a pair of twisted intertwiners
$\rho_1 \overset{(\alpha,\eta)}{\Rightarrow} \rho_2 \overst{(\alpha',\eta')}{\Rightarrow} \rho_3$ their [[composition]] is given by composing their components separately.
\end{definition}

## Properties

### Category-theoretically

Writing $\mathbf{B}G$ for the [[delooping groupoid]] of $G$ and $Vec$ for the [[category of vector spaces]] (over a given [[ground field]]), the ordinary [[category]] [[Rep]] of $G$-[[representations]] and ordinary [[intertwiners]] $\eta \colon \rho_1 \Rightarrow \rho_2$ between these is [[equivalence of categories|equivalently]] the [[functor category]]

$$
  Rep(G) \;\;\simeq\;\;
  Func\big(
    \mathbf{B}G
    ,\,
    Vec
  \big)
  \,.
$$

\begin{tikzcd}
  \mathbf{B}G
  \ar[
    d, 
    bend right=40, 
    "{ \rho_1 }"{swap, pos=.53}, 
    "{\ }"{name=s}
  ]
  \ar[
    d, 
    bend left=40, 
    "{ \rho_2 }"{pos=.53}, 
    "{\ }"{name=t, swap}
  ]
  \ar[from=s, to=t, Rightarrow, "{ \eta }"]
  \\
  \mathrm{Vec}
\end{tikzcd}

In contrast, the category of $G$-representations with twisted intertwiners between them is the [[iso-comma category|iso-comma]] [[(2,1)-category]] between $\mathbf{B}G \colon \mathbf{B}Aut(G) \longrightarrow Grpd$ and $Vec \colon \ast \to Grpd$, whose [[1-morphisms]] are [[diagrams]] in [[Grpd]] of this form:

\begin{tikzcd}
  \mathbf{B}G
  \ar[
    rr,
    "{ \mathbf{B}\alpha }"
  ]
  \ar[
    dr,
    "{ \rho_1 }"{swap, pos=.4}, 
    "{\ }"{name=s}
  ]
  &[-40pt]&[-40]
  \mathbf{B}G
  \ar[
    dl,
    "{ \rho_2 }"{pos=.4}, 
    "{\ }"{name=t, swap}
  ]
  \ar[
    from=s, to=t, Rightarrow, "{ \eta }"
  ]
  \\
  &
  \mathrm{Vec}
\end{tikzcd}

and whose [[2-morphisms]] are the evident paper-cup pasting diagrams


\begin{tikzcd}
  \mathbf{B}G
  \ar[
    rr,
    bend left=20,
    "{ \mathbf{B}\alpha }"{description},
    "{\ }"{name=s2, swap}
  ]
  \ar[
    rr,
    bend right=20,
    "{ \mathbf{B}\alpha' }"{description},
    "{\ }"{name=t2}
  ]
  \ar[
    from=s2, to=t2,
    Rightarrow, 
    "{ \sim }"{sloped}
  ]
  \ar[
    dr,
    "{ \rho_1 }"{swap, pos=.4}, 
    "{\ }"{name=s}
  ]
  &[-40pt]&[-40]
  \mathbf{B}G
  \ar[
    dl,
    "{ \rho_2 }"{pos=.4}, 
    "{\ }"{name=t, swap}
  ]
  \ar[
    from=s, to=t, 
    Rightarrow, 
    bend right=10,
    shift right=5pt,
    "{ \eta }"{swap}
  ]
  \\
  &
  \mathrm{Vec}
\end{tikzcd}


## References

* {#FelderFröhlichFuchsSchweigert00} [[Giovanni Felder]], [[Jürg Fröhlich]], [[Jürgen Fuchs]], [[Christoph Schweigert]]: *The geometry of WZW branes*, J. Geom. Phys. **34** (2000) 162-190 \[<a href="https://doi.org/10.1016/S0393-0440(99)00061-3">doi:10.1016/S0393-0440(99)00061-3</a>, [arXiv:hep-th/9909030](https://arxiv.org/abs/hep-th/9909030)\]

* {#FuchsSchweigert00a} [[Jürgen Fuchs]], [[Christoph Schweigert]]: *Symmetry breaking boundaries II. More structures; examples*, Nucl. Phys. B **568** (2000) 543-593 &lbrack;[arXiv:hep-th/9908025](https://arxiv.org/abs/hep-th/9908025), <a href="https://doi.org/10.1016/S0550-3213(99)00669-0">doi:10.1016/S0550-3213(99)00669-0</a>&rbrack;

* {#FuchsSchweigert00b} [[Jürgen Fuchs]], [[Christoph Schweigert]]: *Lie algebra automorphisms in conformal field theory*, in *[Conference on Infinite Dimensional Lie Theory and Conformal Field Theory](https://inspirehep.net/conferences/972922)* (May 2000) &lbrack;[arXiv:math/0011160](https://arxiv.org/abs/math/0011160)&rbrack;


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
