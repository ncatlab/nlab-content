

\begin{definition}\label{GershgorinDiscs}
**(Gershgorin discs)** \linebreak
 Let $A \in Mat_{n \times n}(\mathbb{C})$ be a [[square matrix]] with [[complex numbers|complex]] entries. For $j \in \{1, \cdots, n\}$ define 

* the $j$th *Gershgorin radius* of $A$ to be the [[sum]] of [[absolute values]] of off-diagonal entries in the $j$th row:

  $$
    r_j^A
    \;\coloneqq\;
    \underset{k \neq j}{\sum}
    \left\vert
      a_{j k}
    \right\vert
  $$

* the $j$th *Gershgorin disc* to be the [[closed disk]] in the [[complex plane]] centered at the $j$th diagonal entry with radius the above $j$th Gershgorin radius:

  $$
    D_j^A
    \;\coloneqq\;
    \Big\{
      z \in \mathbb{C}
      \,\Big\vert\,
      \left\vert
        z - a_{j j}
      \right\vert
      \,\leq\,
      r_j^A
    \Big\}
    \,.
  $$

\end{definition}
