
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

