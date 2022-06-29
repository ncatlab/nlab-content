
$$
  \array{
    Sh(CartSp, GoodOpen)
    &\array{\phantom{----}}{\hookrightarrow}&
    Sh(CartSp, FiniteGoodOpen)
    \\
    X
    &\mapsto&
    \big(
     n
     \mapsto
     im\big(X(D^n \hookrightarrow\mathbb{R}^n)\big) 
    \big)
  }
$$


\begin{tikzcd}
  g^\ast X
  \ar[r]
  \ar[d]
  \ar[dr, phantom, "{\mbox{\tiny(pb)}}"]
  \ar[
    dd,
    bend right=50,
    "{g^\ast f}"{swap}
  ]
  &
  X
  \ar[d]
  \ar[
    dd,
    bend left=50,
    "{f}"
  ]
  \\
  \mathrm{im}_n(g^\ast f)
  \ar[r]
  \ar[d]
  \ar[dr, phantom, "{\mbox{\tiny(pb)}}"]
  &
  \mathrm{im}_n(f)
  \ar[d]
  \\
  Y'
  \ar[
    r,
    "g"{swap} 
  ]
  &
  Y
\end{tikzcd}



$$\tilde f \;\colon\; C \underoverset{\simeq}{\ell_C}{\longrightarrow} 1 \otimes C \overset{e\otimes id}{\longrightarrow} A \otimes C \overset{f}{\longrightarrow}
N,$$