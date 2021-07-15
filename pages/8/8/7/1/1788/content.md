
Recall that ([this Prop.](adjoint+functor#GeneralAdjunctsInTermsOfAdjunctionUnitCounit)) the hom-isomorphism that defines an adjunction of functors ([this Def.](adjoint+functor#AdjointFunctorsInTermsOfNaturalBijectionOfHomSets)) is equivalently given in terms of [[composition]] with 

* the [[adjunction unit]] $eta_c \colon c \xrightarrow{\;} R \circ L(c)$ 

* the [[adjunction counit]] $\epsilon_d \colon L \circ R(d) \xrightarrow{\;} d$ 

as follows:

\begin{tikzcd}[column sep={between origins, 33}]
    L(c)
    \ar[rr, "f"]
    &&
    d
    &{\phantom{AAA}}\leftrightarrow{\phantom{AAA}}&
    c 
    \ar[rr, "\eta_c"]
    \ar[
      rrrr,
      rounded corners,
      to path={
           -- ([yshift=+12pt]\tikztostart.north)
           --node[above]{
               \scalebox{.7}{$
                 \widetilde{f}
               $}
             } ([yshift=+8.5pt]\tikztotarget.north)
           -- (\tikztotarget.north)}
    ]
    &&
    R \circ L(c)
    \ar[rr, "R(f)"]
    &&
    R(d)
\end{tikzcd}

\begin{tikzcd}[column sep={between origins, 33}]
    c
    \ar[rr, "\widetilde f"]
    &&
    R(d)
    &{\phantom{AAA}}\leftrightarrow{\phantom{AAA}}&
    L(c)
    \ar[rr, "L(\widetilde{f})"]
    \ar[
      rrrr,
      rounded corners,
      to path={
           -- ([yshift=+8pt]\tikztostart.north)
           --node[above]{
               \scalebox{.7}{$
                 f
               $}
             } ([yshift=+8.5pt]\tikztotarget.north)
           -- (\tikztotarget.north)}
    ]
    &&
    L \circ R(d)
    \ar[
      rr,
      "\epsilon_d"
    ]
    &&
    d
\end{tikzcd}

Using this, consider the following transformations of morphisms in sliced categories:

**(1a)**

\begin{tikzcd}[column sep={between origins, 33}, row sep=4]
    L(c) 
    \ar[rr, "f", dashed]
    \ar[dr]
      && 
    d
    \ar[dl, "p"]
    \\
    & 
    L(b)
\end{tikzcd}

**(2a)**

\begin{tikzcd}[column sep={between origins, 33}, row sep=4]
    c 
    \ar[
      rr,
      "{\eta_c}"
    ]
    \ar[dr]
    \ar[
      rrrr,
      rounded corners,
      to path={
           -- ([yshift=+12pt]\tikztostart.north)
           --node[above]{
               \scalebox{.7}{$
                 \widetilde{f}
               $}
             } ([yshift=+8pt]\tikztotarget.north)
           -- (\tikztotarget.north)}
    ]
    &&
    R \circ L(c)
    \ar[rr, "{R(f)}", dashed]
    \ar[dr]
      &&
    R(d)
    \ar[dl, "R(p)"]
    \\
    &
    b
    \ar[
      rr,
      "\eta_b"{below}
    ]
    &
    &
    R \circ L(b)
\end{tikzcd}

**(2b)**

\begin{tikzcd}[column sep={between origins, 33}, row sep=4]
    c
    \ar[
      rr,
      dashed
    ]
    \ar[dr]
      \ar[
      rrrr,
      rounded corners,
      to path={
           -- ([yshift=+12pt]\tikztostart.north)
           --node[above]{
               \scalebox{.7}{$
                 \widetilde{f}
               $}
             } ([yshift=+8pt]\tikztotarget.north)
           -- (\tikztotarget.north)}
      ]
    &&
    \eta_b^\ast\big(R(d)\big)
    \ar[rr]
    \ar[dl]
    \ar[
      dr,
      phantom,
      "\mbox{\tiny\rm(pb)}"
    ]
      &&
    R(d)
    \ar[dl, "R(p)"]
    \\
    &
    b
    \ar[
      rr,
      "\eta_b"{below}
    ]
    &
    &
    R \circ L(b)
\end{tikzcd}

**(1b)**

\begin{tikzcd}[column sep={between origins, 33}, row sep=4]
    L(c)
    \ar[dr]
    \ar[rrrr, "\widetilde{f}"]
    \ar[
      rrrrrr,
      rounded corners,
      to path={
           -- ([yshift=+8pt]\tikztostart.north)
           --node[above]{
               \scalebox{.7}{$
                 f
               $}
             } ([yshift=+8pt]\tikztotarget.north)
           -- (\tikztotarget.north)}
    ]
    &&
    &&
    L \circ R(d)
    \ar[rr, "{\epsilon_d}"]
    \ar[dl]
    &&
    d
    \ar[dl, "p"]
    \\
    &
    L(b)
    \ar[
      rr,
      "L(\eta_b)"{below}
    ]
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
    &
    &
    L \circ R \circ L(b)
    \ar[rr, "\epsilon_{L(b)}"{below}]
    &&
    L(b)
\end{tikzcd}

Here 

* (2a) and (2b) are equivalent expression of the same morphism $\tilde f$ in $\mathcal{C}_{/b}$, by the [[universal property]] of the [[pullbackk]];

* (1a) and (1b) are equivalent expressions of the same morphism $f$ in $\mathcal{D}_{/L(b)}$, by the above expression of [[adjuncts]] between $\mathcal{C}$ and $\mathcal{D}$.

Hence 

* starting with a morphism as in (1a) and transforming it to $(2)$ and then to (1b) is the identity operation;

* starting with a morphism as in (2b) and transforming it to (1) and then to (2a) is the identity operation.

In conclusion, the transformations (1) $\leftrightarrow$ (2) consitute a hom-isomorphism that witnesses the adjunction $L_{/c} \dashv R_{/c}$.


