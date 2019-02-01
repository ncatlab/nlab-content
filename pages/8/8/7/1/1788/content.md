

#### At a $2 T$-orientifold singularity
  {#At2TSingularity}

For $G = 2 T$ the [[binary tetrahedral group]], the [[character of a linear representation|characters]]/[[D-brane charges]] of the [[virtual representation|virtual]] [[permutation representations]] are ([BSS 18, 4.8](#BurtonSatiSchreiber18))



| $[H] = $ | $\left[\langle e\rangle\right]$ | $\left[\langle g_1\rangle\right]$ |  $\left[\langle g_2\rangle\right]$ | $\left[\langle g_3\rangle\right]$ | $\left[\langle g_4\rangle\right]$ | $\left[\langle g_5\rangle\right]$ |  $\left[\langle g_6\rangle\right]$ |
|--|--|--|--|--|--|--|--|
| $\chi_{V_1} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ |$\phantom{-}1$ |
| $\chi_{V_2} =$ | $\phantom{-}2$ |  $\phantom{-}2$ |  $-1$ | $-1$ |  $\phantom{-}2$ | $-1$ | $-1$ |
| $\chi_{V_3} =$ | $\phantom{-}3$ |  $\phantom{-}3$ |  $\phantom{-}0$ | $\phantom{-}0$ |  $-1$ | $\phantom{-}0$ | $\phantom{-}0$ |
| $\chi_{V_4} =$ | $\phantom{-}4$ |  $-4$ |  $\phantom{-}1$ | $\phantom{-}1$ |  $\phantom{-}0$ | $-1$ | $-1$ |
| $\chi_{V_5} =$ | $\phantom{-}4$ |  $-4$ |  $-2$ | $-2$ |  $\phantom{-}0$ | $\phantom{-}2$ | $\phantom{-}2$ |


One sees by immediate inspection, that the general solution to the (homogenous part of the) tadpole cancellation condition (eq:VanishingOfCharacterValuesOnNontrivialSubgroups) for $G = 2T$ is

$$
  V 
  \;=\;
  n
  \Big(
    1 \cdot V_1
    + 
    1 \cdot V_2
    + 
    3 \cdot V_3
    + 
    2 \cdot V_4
    + 
    1 \cdot V_5 
  \Big)
  \,,
  \phantom{AAA}
  n \in \mathbb{Z}
$$


whose minimal [[mass]] (net brane number) is

$$
  \begin{aligned}
    dim(V) 
      & =
    \chi_V([\langle e\rangle]) 
    \\
      & =
        1 \cdot 1
        + 
        1 \cdot 2
        + 
        3 \cdot 3
        + 
        2 \cdot 4
        + 
        1 \cdot 4
      & 
      \\
      & 
      =
      24
  \end{aligned}
$$




***

Let 

\begin{tikzcd}
  R_{\mathbb{C}}(-)
  \arrow[r, phantom, "\colon" marking]
  &
  \mathrm{FinGrp}^{\mathrm{op}}
  \arrow[rr]
    &&
  \mathrm{CRing}
  \\
  &
  G
  \arrow[rr, phantom, "\mapsto" marking]
  \arrow[d, "\phi"]
  &&
  R_{\mathbb{C}}\big(G\big)
  \\
  &
  G'
  \arrow[rr, phantom, "\mapsto" marking]
  &&
  R_{\mathbb{C}}\big(G'\big)
  \arrow[u, "\phi^\ast"]
\end{tikzcd}

be the [[functor]] from the [[opposite category]] of the [[category]] [[FinGrp]] of [[finite groups]]] to the [[category]] [[CRing]] of [[commutative rings]], which sends a group to its [[representation ring]] and a [[group homomorphism]] to the corresponding [[restricted representation]]-assignment.

\begin{centre}

\begin{tikzpicture}

\fill (0,0) circle[radius=2em];

\end{tikzpicture}

\end{centre}

An XY-Matrix diagram:

\begin{centre}

\xymatrix{A \ar[r] \ar[dr] & B \ar[d] \\ & C}

\end{centre}