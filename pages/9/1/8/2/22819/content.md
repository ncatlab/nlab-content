
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

Then for every [[object]] $c \in \mathcal{C}$ there is induced a pair of adjoint functors between the [[slice categories]] ([[slice (∞,1)-categories|slice ∞-categories]])

$$
  \mathcal{D}_{/L(c)}
  \underoverset
    {\underset{\;\;\;\;R_{/c}\;\;\;\;}{\longrightarrow}}
    {\overset{\;\;\;\;L_{/c}\;\;\;\;}{\longleftarrow}}
    {\bot}
  \mathcal{C}_{/c}
  \mathrlap{\,,}
$$

where:

* $L_{/c}$ is the evident induced functor (applying $L$ to the entire triangle [[diagrams]] in $\mathcal{C}$ which represent the morphisms in $\mathcal{C}_{/c}$);

* $R_{/c}$ is the [[composition|composite]]

  $$
    R_{/c} 
      \;\colon\; 
    \mathcal{D}_{/{L(c)}} 
      \overset{\;\;R\;\;}{\longrightarrow} 
    \mathcal{C}_{/{(R \circ L(c))}} 
      \overset{\;\;\eta_{c}^*\;\;}{\longrightarrow}
    \mathcal{C}_{/c}
  $$

  of 

  1. the evident functor induced by $R$;

  1. the ([[homotopy pullback|homotopy]]) [[pullback]] along the $(L \dashv R)$-[[unit of an adjunction|unit]] at $c$.

\end{proposition}
In the generality of [[(∞,1)-category theory]] this appears as [[Higher Topos Theory|HTT, prop. 5.2.5.1]]. For discussion in [[model category|model category theory]] see at *[sliced Quillen adjunctions](slice+model+structure#SlicedQuillenAdjunction)*.
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

Using this, consider the following transformations of morphisms in slice categories:

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

Here:

* (1a) and (1b) are equivalent expressions of the same morphism $f$ in $\mathcal{D}_{/L(b)}$, by (at the top of the diagrams) the above expression of [[adjuncts]] between $\mathcal{C}$ and $\mathcal{D}$ and (at the bottom) by the [[triangle identity]].

* (2a) and (2b) are equivalent expression of the same morphism $\tilde f$ in $\mathcal{C}_{/b}$, by the [[universal property]] of the [[pullback]].

Hence:

* starting with a morphism as in (1a) and transforming it to $(2)$ and then to (1b) is the identity operation;

* starting with a morphism as in (2b) and transforming it to (1) and then to (2a) is the identity operation.

In conclusion, the transformations (1) $\leftrightarrow$ (2) consitute a [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) that witnesses an adjunction of the claimed form $L_{/c} \dashv R_{/c}$.
\end{proof}




