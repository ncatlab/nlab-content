
### Slicing of adjoint functors
 {#OnSlices}

\begin{proposition}\label{SliceAdjoints}
**(sliced adjoints)** \linebreak
Let

$$
   \mathcal{D} 
   \underoverset
    {\underset{\;\;\;\;R\;\;\;\;}{\longrightarrow}}
    {\overset{\;\;\;\;L\;\;\;\;}{\longleftarrow}}
    {\bot}
  \mathcal{C}
$$

be a pair of [[adjoint functors]] ([[adjoint (∞,1)-functors|adjoint ∞-functors]]), where the [[category]] ([[(∞,1)-category|∞-category]]) $\mathcal{C}$ has all [[pullbacks]] ([[homotopy pullbacks]]). 

Then: 

1. For every [[object]] $b \in \mathcal{C}$ there is induced a pair of [[adjoint functors]] between the [[slice categories]] ([[slice (∞,1)-categories|slice ∞-categories]]) of the form

   \[
     \label{SlicedAdjointFunctorsOverLb}
     \mathcal{D}_{/L(b)}
     \underoverset
       {\underset{\;\;\;\;R_{/b}\;\;\;\;}{\longrightarrow}}
       {\overset{\;\;\;\;L_{/b}\;\;\;\;}{\longleftarrow}}
       {\bot}
     \mathcal{C}_{/b}
     \mathrlap{\,,} 
   \]

   where:

   * $L_{/b}$ is the evident induced functor (applying $L$ to the entire triangle [[diagrams]] in $\mathcal{C}$ which represent the morphisms in $\mathcal{C}_{/b}$);

   * $R_{/b}$ is the [[composition|composite]]

     $$
       R_{/b} 
         \;\colon\; 
       \mathcal{D}_{/{L(b)}} 
         \overset{\;\;R\;\;}{\longrightarrow} 
       \mathcal{C}_{/{(R \circ L(b))}} 
         \overset{\;\;(\eta_{b})^*\;\;}{\longrightarrow}
       \mathcal{C}_{/b}
     $$

     of 

     1. the evident functor induced by $R$;

     1. the ([[homotopy pullback|homotopy]]) [[pullback]] along the $(L \dashv R)$-[[unit of an adjunction|unit]] at $b$ (i.e. the [[base change]] along $\eta_b$).

1. For every [[object]] $b \in \mathcal{D}$ there is induced a pair of [[adjoint functors]] between the [[slice categories]] of the form

   \[
     \label{SlicedAdjointFunctorsOverRb}
     \mathcal{D}_{/b}
     \underoverset
       {\underset{\;\;\;\;R_{/b}\;\;\;\;}{\longrightarrow}}
       {\overset{\;\;\;\;L_{/b}\;\;\;\;}{\longleftarrow}}
       {\bot}
     \mathcal{C}_{/R(b)}
     \mathrlap{\,,} 
   \]

   where:

   * $R_{/b}$ is the evident induced functor (applying $R$ to the entire triangle [[diagrams]] in $\mathcal{D}$ which represent the morphisms in $\mathcal{D}_{/b}$);

   * $L_{/b}$ is the [[composition|composite]]

     $$
       L_{/b} 
         \;\colon\; 
       \mathcal{D}_{/{R(b)}} 
         \overset{\;\;L\;\;}{\longrightarrow} 
       \mathcal{C}_{/{(L \circ R(b))}} 
         \overset{\;\;(\epsilon_{b})_!\;\;}{\longrightarrow}
       \mathcal{C}_{/b}
     $$

     of 

     1. the evident functor induced by $L$;

     1. the [[composition]] with the $(L \dashv R)$-[[counit of an adjunction|counit]] at $b$ (i.e. the left [[base change]] along $\epsilon_b$).

\end{proposition}
The first statement appears, in the generality of [[(∞,1)-category theory]], as [[Higher Topos Theory|HTT, prop. 5.2.5.1]]. For discussion in [[model category|model category theory]] see at *[sliced Quillen adjunctions](slice+model+structure#SlicedQuillenAdjunction)*.
\begin{proof}
(in [[1-category|1-]][[category theory]])

Recall that ([this Prop.](adjoint+functor#GeneralAdjunctsInTermsOfAdjunctionUnitCounit)) the hom-isomorphism that defines an adjunction of functors ([this Def.](adjoint+functor#AdjointFunctorsInTermsOfNaturalBijectionOfHomSets)) is equivalently given in terms of [[composition]] with 

* the [[adjunction unit]] $\;\;\eta_c \colon c \xrightarrow{\;} R \circ L(c)$ 

* the [[adjunction counit]] $\;\;\epsilon_d \colon L \circ R(d) \xrightarrow{\;} d$ 

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

Using this, consider the following transformations of morphisms in slice categories, for the **first case**:

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
    \ar[rrrr, "L(\widetilde{f})"]
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

Here:

* (1a) and (1b) are equivalent expressions of the same morphism $f$ in $\mathcal{D}_{/L(b)}$, by (at the top of the diagrams) the above expression of [[adjuncts]] between $\mathcal{C}$ and $\mathcal{D}$ and (at the bottom) by the [[triangle identity]].

* (2a) and (2b) are equivalent expression of the same morphism $\tilde f$ in $\mathcal{C}_{/b}$, by the [[universal property]] of the [[pullback]].

Hence:

* starting with a morphism as in (1a) and transforming it to $(2)$ and then to (1b) is the identity operation;

* starting with a morphism as in (2b) and transforming it to (1) and then to (2a) is the identity operation.

In conclusion, the transformations (1) $\leftrightarrow$ (2) consitute a [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) that witnesses an adjunction of the first claimed form (eq:SlicedAdjointFunctorsOverLb).

\linebreak

The **second case** follows analogously, but a little more directly since no pullback is involved:

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

In conclusion, the transformations (1) $\leftrightarrow$ (2) consitute a [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) that witnesses an adjunction of the second claimed form (eq:SlicedAdjointFunctorsOverRb).
\end{proof}


\begin{remark}
  \label{LeftAdjointOfSlicedAdjunctionFormsAdjuncts}
**(left adjoint of sliced adjunction forms adjuncts)** \linebreak
  The sliced adjunction (Prop. \ref{SliceAdjoints}) in the second form (eq:SlicedAdjointFunctorsOverRb) is such that the sliced [[left adjoint]]  sends slicing morphism $\tau$ to their [[adjuncts]] $\widetilde{\tau}$, in that (again by [this Prop.](adjoint+functor#GeneralAdjunctsInTermsOfAdjunctionUnitCounit)):

$$
  L_{/d}
  \,
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
  \left(
  \array{
    L(c)
    \\
    \big\downarrow {}^{\mathrlap{\widetilde{\tau}}}
    \\
    b
  }
  \right)
  \;\;\;
  \in
  \;
  \mathcal{D}_{/b}
$$
\end{remark}



