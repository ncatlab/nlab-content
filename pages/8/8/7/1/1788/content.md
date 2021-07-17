
$$
  r_1 \,\otimes\, r_2
  \;=\;
  \big( r_1 \,\otimes\, 1 \big) \cdot \big( 1 \otimes r_2 \big)
  \;=\;
  1 \,\otimes\, r_1 \cdot 1 \otimes r_2
  \;=\;
  1 \,\otimes\, r_1 \cdot r_2
$$

\begin{prop}
  If $f$ is an [[isomorphism]] with [[inverse morphism]] $f^{-1}$, then any [[left inverse]] or [[right inverse]] is already an actual [[inverse morphism]] and in fact is [[equality|equal]] to $f^{-1}$.
\end{prop}
In particular, [[inverse morphisms]] are unique when they exist.
\begin{proof}
  Let $g$ be a [left inverse]], hence such that $g \circ f \,=\, id$. 
  Write $f^{-1}$ for the actual inverse, hence such that
  $f^{-1} \circ f \,=\, id$ and $f \circ f^{-1} \,=\, id$.  
  Then the following sequence of equalities implies that
  $g = f^{-1}$:
$$
  \begin{aligned}
    g 
    & \;=\;
    g \circ id
    \\
    & \;=\;
    g \circ ( f \circ f^{-1} )
    \\
    & \;=\;
    (g \circ f) \circ f^{-1}
    \\
    & \;=\;
    id \circ f^{-1}
    \\
    & \;=\;
    f^{-1}
    \,.
  \end{aligned}
$$
Here essentially all steps use just the definitions of the various morphisms, except the third, which uses [[associativity]] of [[composition]] in any [[category]].

An analogous argument applies to right inverses; and, of course, either argument applies to actual inverses.
\end{proof}

\begin{remark}
  The sliced adjunction (Prop. \ref{SliceAdjoints}) in the second form (eq:SlicedAdjointFunctorsOverRb) is such that the sliced [[left adjoint]] form [[adjuncts]] of slicing morphisms, in that (again by [this Prop.](adjoint+functor#GeneralAdjunctsInTermsOfAdjunctionUnitCounit)):

$$
  L_{/d}
  \left(
    \array{
      c
      \\
      \big\downarrow {}^{\mathrlap{\tau}}
      \\
      R(b)
    }
  \right)
  \;\;
  =
  \;\;
  \array{
    L(c)
    \\
    \big\downarrow {}^{\mathrlap{\widetilde{\tau}}}
    \\
    b
  }
$$
\end{remark}


**(1a)**

\begin{tikzcd}[column sep={between origins, 33}, row sep=4]
  c
  \ar[rr, dashed, "f"]
  \ar[dr]
  &&
  R(d)
  \ar[dl]
  \\
  & 
  R(b)
\end{tikzcd}

**(2)**

\begin{tikzcd}[column sep={between origins, 33}, row sep=4]
  L(c)
  \ar[rr, dashed, "L(f)"]
  \ar[dr]
  \ar[
      rrrr,
      rounded corners,
      to path={
           -- ([yshift=+8pt]\tikztostart.north)
           --node[above]{
               \scalebox{.7}{$
                 \widetilde{f}
               $}
             } ([yshift=+8pt]\tikztotarget.north)
           -- (\tikztotarget.north)}
  ]
  &&
  L \circ R(d)
  \ar[rr, "\epsilon_d"{above}]
  \ar[dl]
  &&
  d
  \ar[dl]
  \\
  &
  L \circ R(b)
  \ar[rr, "\epsilon_b"{below}]
  &&
  b
\end{tikzcd}

**(1b)**

\begin{tikzcd}[column sep={between origins, 33}, row sep=4]
  c
  \ar[rr, "\eta_c"{above}]
  \ar[dr]
  \ar[
      rrrrrr,
      rounded corners,
      to path={
           -- ([yshift=+12pt]\tikztostart.north)
           --node[above]{
               \scalebox{.7}{$
                 f
               $}
             } ([yshift=+8pt]\tikztotarget.north)
           -- (\tikztotarget.north)}
  ]
  &&
  R \circ L(c)
  \ar[rrrr,"R(\widetilde{f})"]
  \ar[dr]
  &&
  %R \circ L \circ R(d)
  %\ar[rr, "R(\epsilon_d)"{above}]
  %\ar[dl]
  &&
  R(d)
  \ar[dl]
  \\
  &
  R(b)
  \ar[rr, "\eta_{R(b)}"{below}]
    \ar[
      rrrr,
      rounded corners,
      to path={
           -- ([yshift=-8pt]\tikztostart.south)
           --node[below]{
               \scalebox{.7}{$
                 \mathrm{id}
               $}
             } ([yshift=-8pt]\tikztotarget.south)
           -- (\tikztotarget.south)}
    ]
  &&
  R \circ L \circ R(b)
  \ar[rr, "R(\epsilon_b)"{below}]
  &&
  R(b)
\end{tikzcd}

