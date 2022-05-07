

\begin{prop}
  For $n \geq 1$, the [[homotopy groups]] of [[complex projective space]] $\mathbb{C}P^n$ are the [[integers]] in degree 2, the [[homotopy groups of spheres|homotopy groups of]] the [[n-sphere|2n+1-sphere]] in degrees $\geq 2n+1$ and [[trivial group|trivial]] otherwise:
\[
  \label{ListOfHomotopyGroupsOfComplexProjectiveSpace}
    \pi_k
    \big(
      \mathbb{C}P^n
    \big)
    \;=\;
    \left\{
    \array{
      \ast &\vert& k = 0
      \\
      1 &\vert& k = 1
      \\
      \mathbb{Z} &\vert& k = 2
      \\
      \mathbb{Z} &\vert& k = 2n + 1
      \\
      \pi_k
      \big(
        S^{2n+1}
      \big)
      &\vert&
      k \geq 2n+1
      \\
      0 &\vert& otherwise
    }
    \right.
\]
\end{prop}

\begin{proof}
  Essentially by definition, $\mathbb{C}P^n$ is the [[quotient space]] of the [[circle group]]-[[action]] on the unit sphere  $S^{2n+1} \simeq S\big(\mathbb{C}^{2n+2}\big)$. 

First of all, this implies that $\mathbb{C}P^n$ is [[connected topological space|connected]], since $S^{2n+1}$ is, hence $\pi_0\big( \mathbb{C}P^n\big) = \ast$.

Moreover, since this is a [[free action]], we have a [[circle principal bundle]] and hence a [[fiber sequence]] of the form

\begin{xymatrix@C=20pt@R=20pt}
  S^1 
  \ar[r]
  &
  S^{2n+1}
  \ar[d]
  \\
  &
  \mathbb{C}P^n
  \,.
\end{xymatrix}

Therefore the homotopy groups of $\mathbb{C}P^n$ sit in the corresponding [[long exact sequence of homotopy groups]], hence a [[long exact sequence]] of the this form:

\begin{xymatrix@C=20pt@R=20pt}
  \cdots
  \ar[r]
  &
  \pi_{k+1}
  \big(
    \mathbb{C}P^k
  \big)
  \ar[r]
  &
  \pi_k
  \big(
    S^1
  \big)
  \ar[r]
  &
  \pi_k
  \big(
    S^{2n+1}
  \big)
  \ar[r]
  &
  \pi_k
  \big(
    \mathbb{C}P^n
  \big)
  \ar[r]
  &
  \pi_{k-1}
  \big(
    S^1
  \big)
  \ar[r]
  &
  \cdots
\end{xymatrix}

By the following two basic facts about the [[homotopy groups of spheres]]

$$
  \pi_{k \geq 2}
  \big(
    S^1
  \big)
  \;=\;
  0
  \,,
  \phantom{AAAA}
  \pi_{k \leq 2n}
  \big(
    S^{2n+1}
  \big)
  \;=\;
  0
$$

this long exact sequence contains this part 

\begin{xymatrix@C=20pt@R=20pt}
  \pi_1
  \big(
    S^{2n+1}
  \big)
  \ar@{=}[d]
  \ar[r]
  & 
  \pi_1
  \big(
    \mathbb{C}P^n
  \big)
  \ar@{=}[d]
  \ar[r]
  &
  \pi_0
  \big(
    S^1
  \big)
  \ar@{=}[d]
  \\
  1
  \ar@{=}[r]
  &
  \pi_1
  \big(
    \mathbb{C}P^n
  \big)
  \ar[r]
  &
  \ast
\end{xymatrix}



and this part (using now the assumption that $n \geq 1$):

\begin{xymatrix@C=20pt@R=20pt}
  \pi_2
  \big(
    S^{2n+1}
  \big)
  \ar@{=}[d]
  \ar[r]
  & 
  \pi_2
  \big(
    \mathbb{C}P^n
  \big)
  \ar@{=}[d]
  \ar[r]
  &
  \pi_1
  \big(
    S^1
  \big)
  \ar@{=}[d]
  \ar[r]
  &
  \pi_1
  \big(
    S^{2n+1}
  \big)
  \ar@{=}[d]
  \\
  0
  \ar[r]
  &
  \pi_2
  \big(
    \mathbb{C}P^n
  \big)
  \ar@{=}[r]
  &
  \mathbb{Z}
  \ar[r]
  &
  0
\end{xymatrix}

and these parts, for all $k \geq 3$:

\begin{xymatrix@C=20pt@R=20pt}
  \pi_{k}
  \big(
    S^1
  \big)
  \ar@{=}[d]
  \ar[r]
  &
  \pi_k
  \big(
    S^{2n+1}
  \big)
  \ar[r]
  \ar@{=}[d]
  &
  \pi_k
  \big(
    \mathbb{C}P^n
  \big)
  \ar[r]
  \ar@{=}[d]
  &
  \pi_{k-1}
  \big(
    S^1
  \big)
  \ar@{=}[d]
  \\
  0
  \ar[r]
  &
  \pi_k
  \big(
    S^{2n+1}
  \big)
  \ar@{=}[r]
  &
  \pi_k
  \big(
    \mathbb{C}P^n
  \big)
  \ar[r]
  &
  0
\end{xymatrix}

In both cases the identification in the bottom line follows from [[exact sequence|exactness]], given that the two outer items are [[trivial group|trivial]].

This gives the list (eq:ListOfHomotopyGroupsOfComplexProjectiveSpace), where we just made explicit that $\pi_{2n+1}(S^{2n+1}) = \mathbb{Z}$ (the [[Hopf degree theorem]], if you wish).
\end{proof}


