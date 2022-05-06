
#### At a $2 I$-orientifold singularity
  {#At2ISingularity}

For $G = 2 I$ the [[binary icosahedral group]] (whose [[order of a group|order]] is ${\vert 2I \vert} = 120$), the [[character of a linear representation|characters]]/[[D-brane charges]] of the elementary [[virtual representation|virtual]] [[permutation representations]]/[[fractional D-branes]] are ([BSS 18, 4.10](#BurtonSatiSchreiber18)):

| $[H] = $ | $\left[\langle e\rangle\right]$ | $\left[\langle g_1\rangle\right]$ |  $\left[\langle g_2\rangle\right]$ | $\left[\langle g_3\rangle\right]$ | $\left[\langle g_4\rangle\right]$ | $\left[\langle g_5\rangle\right]$ |  $\left[\langle g_6\rangle\right]$ | $\left[\langle g_7\rangle\right]$ | $\left[\langle g_78\rangle\right]$ |
|--|--|--|--|--|--|--|--|--|--|
| $\chi_{V_1} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_2} =$ | $\phantom{-}4$ |  $\phantom{-}4$ |  $\phantom{-}1$ | $\phantom{-}0$ |  $-1$ | $-1$ | $\phantom{-}1$ | $-1$ | $-1$ |
| $\chi_{V_3} =$ | $\phantom{-}5$ |  $\phantom{-}5$ |  $-1$ | $\phantom{-}1$ |  $\phantom{-}0$ | $\phantom{-}0$ | $-1$ | $\phantom{-}0$ | $\phantom{-}0$ |
| $\chi_{V_4} =$ | $\phantom{-}6$ |  $\phantom{-}6$ |  $\phantom{-}0$ | $-2$ |  $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}0$ | $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_5} =$ | $\phantom{-1}\mathllap{12}$ |  $\phantom{-1}\mathllap{-12}$ |  $\phantom{-}0$ | $\phantom{-}0$ |  $\phantom{-}2$ | $\phantom{-}2$ | $\phantom{-}0$ | $-2$ | $-2$ |
| $\chi_{V_6} =$ | $\phantom{-}8$ |  $-8$ |  $\phantom{-}2$ | $\phantom{-}0$ |  $-2$ | $-2$ | $-2$ | $\phantom{-}2$ | $\phantom{-}2$ |
| $\chi_{V_7} =$ | $\phantom{-}8$ |  $-8$ |  $-4$ | $\phantom{-}0$ |  $-2$ | $-2$ | $\phantom{-}4$ | $\phantom{-}2$ | $\phantom{-}2$ |


One sees by not so immediate inspection, that the general solution to the (homogenous part of the) tadpole cancellation condition (eq:VanishingOfCharacterValuesOnNontrivialSubgroups) for $G = 2I$ is

$$
  V 
  \;=\;
  n
  \Big(
    1 \cdot V_1
    + 
    4 \cdot V_2
    + 
    5 \cdot V_3
    + 
    3 \cdot V_4
    + 
    3 \cdot V_5 
    + 
    2 \cdot V_6 
    + 
    1 \cdot V_7 
  \Big)
  \,,
  \phantom{AAA}
  n \in \mathbb{Z}
$$


whose minimal [[positive number|positive]] [[mass]] (net brane number) is

$$
  \begin{aligned}
    M_{2I}
      & =
    dim(V) 
    \\
      & =
    \chi_V([\langle e\rangle]) 
    \\
      & =
      1 \cdot 1
      + 
      4 \cdot 4
      + 
      5 \cdot 5
      + 
      3 \cdot 6
      + 
      3 \cdot 12
      + 
      2 \cdot 8
      + 
      1 \cdot 8
      \\
      & 
      =
      120
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

be the [[functor]] from the [[opposite category]] of the [[category]] [[FinGrp]] of [[finite groups]] to the [[category]] [[CRing]] of [[commutative rings]], which sends a group to its [[representation ring]] and a [[group homomorphism]] to the corresponding [[restricted representation]]-assignment.

\begin{centre}

\begin{tikzpicture}

\fill (0,0) circle[radius=2em];

\end{tikzpicture}

\end{centre}

An XY-Matrix diagram:

\begin{centre}

\begin{xymatrix}

A \ar[r] \ar[dr] & B^{2} \ar[d] \\ & C

\end{xymatrix}

\end{centre}

\begin{centre}

\begin{xymatrix[font = \large]@C+2pc}

A \rtwocell^f_g{\alpha} & B

\end{xymatrix}

\end{centre}

\begin{centre}

\begin{xymatrix[border = 2pc]}

A \ar@/^2.0pc/[r] \ar@/_2.0pc/[r] & B

\end{xymatrix}

\end{centre}
