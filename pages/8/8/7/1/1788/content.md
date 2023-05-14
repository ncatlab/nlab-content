
\begin{corollary}
In the above situation, let $f \,\colon\, C' \longrightarrow C$ be an [[sSet]]-[[enriched functor]] [[sSet-enriched categories]]. Then the two versions of [[base change]] along $f$

1. by [[precomposition]] $N(f)^\ast$ of [[(infinity,1)-functor categories|$\infty$-functor $\infty$-categories]] with $N(f)$,

1. by the [[derived functor]] $\mathbb{R} f^\ast$ of [[precomposition]] of [[sSet]]-[[enriched functor categories]] with $f$

are compatible under the equivalence of Prop. \ref{PresentationByModelStructuresOnFunctors}, in that they make a homotopy-[[commuting diagram]]
$$
  \array{
     N\big([C,A]^\circ\big) 
     &\xrightarrow{\phantom{-}\sim\phantom{-}}&
     Func\big(
       N(C)
       ,\,  
       N(A^\circ)
     \big)
     \\
     \mathllap{{}^{
       N\big(
        \mathbb{R}f^\ast
       \big)
     }}
     \Big\downarrow
     &\swArrow&
     \Big\downarrow\mathrlap{{}^{
       N(f)^\ast
     }}
     \\
     N\big([C',A]^\circ\big) 
     &\xrightarrow{\phantom{-}\sim\phantom{-}}&
     Func\big(
       N(C)
       ,\,  
       N(A^\circ)
     \big)
  }
$$
\end{corollary}


$$
  \array{
    N\big([C, A]^\circ\big)
    &\xhookrightarrow{\phantom{-}}&
    N\big([C, A]\big)
    &\longrightarrow&
    Func\big(
      N(C)
      ,\,
      N(A^\circ)
    \big)
    \\
    \Big\downarrow\mathrlap{{}^{
      N\big(\mathbb{R}f^\ast\big)
    }}
    &&
    \Big\downarrow\mathrlap{{}^{
      N\big(f^\ast\big)
    }}
    &&
    \Big\downarrow\mathrlap{{}^{
      N(f)^\ast
    }}
    \\
    N\big([C', A]^\circ\big)
    &\xleftarrow{ Q }&
    N\big([C', A]\big)
    &\longrightarrow&
    Func\big(
      N(C')
      ,\,
      N(A^\circ)
    \big)
    \\
    &
      \mathllap{{}_{id}}\nwarrow
    &
    \Big\uparrow
    &\nearrow
    \\
    &&
    N\big([C', A]^\circ\big)
  }
$$

\begin{tikzcd}[sep=30pt]
  N\big(
    [C,A]^\circ
  \big)
  \ar[dr, hook]
  \ar[drrr]
  \ar[ddd, "{ N(\mathbb{R}f^\ast) }"{description} ]
  &
  \\
  &
  N\big(
    [C,A]
  \big)
  \ar[rr]
  \ar[dd, "{ N(f^\ast) }"{description} ]
  &&
  \mathrm{Func}\big(
    N(C)
    ,\,
    N(A^\circ)
  \big)
  \ar[dd]
  \\
  \\
  N\big(
    [C',A]^\circ
  \big)
  \ar[d, hook]
  &
  N\big(
    [C',A]
  \big)
  \ar[rr]
  \ar[dl, "{ N(Q) }"{description}]
  \ar[d, "{\mathrm{id}}"{description}, "{\ }"{name=t, swap}]
  &&
  \mathrm{Func}\big(
    N(C')
    ,\,
    N(A^\circ)
  \big)
  \\
  N\big(
    [C',A]
  \big)
  \ar[r, hook]
  \ar[to=t, Rightarrow, shorten=20pt]
  &
  N\big(
    [C',A]
  \big) 
  \ar[urr]
\end{tikzcd}

\begin{tikzcd}[sep=30pt]
  N\big(
    [C,A]^\circ
  \big)
  \ar[d, "{ N\big( \mathbb{R}f^\ast \big) }"]
  &&
  \mathrm{Func}\big(
    N(C)
    ,\,
    N(A^\circ)
  \big)
  \ar[dd, "{ N(f)^\ast }"]
  \\ 
  N\big(
    [C',A]^\circ
  \big)  
  \ar[d, hook]
  \\
  N\big(
    [C',A]
  \big)
  \ar[uurr, Rightarrow, shorten=50pt, "{ \sim }"{sloped}]
  &&
  \mathrm{Func}\big(
    N(C')
    ,\,
    N(A^\circ)
  \big)
\end{tikzcd}


