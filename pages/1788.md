
\begin{definition}
**([[site]] of [[closed balls]])**
\linebreak
 Write $ClsdBalls \,\subset\, SmthMnfd_{bdry}$ for the [[full subcategory]] of the [[category]] of [[SmoothManifolds]] [[manifold with boundary|with boundary]] on the [[closed balls]] $\mathbb{B}_{cl}^n \,\coloneqq\, \big\{ \vec x \in \mathbb{R}^n \,\big\vert\, \sum_i x^i = 1 \big\}$, for $n \in \mathbb{N}$.

Regard this as a [[site]] by equipping it with the [[coverage]] whose [[covering families]] $\big\{ \overline{U_i} \to \mathbb{B}_{cl}^n \big\}_{i \in I}$ are the [[topological closures]] of [[good open covers]] 
$\big\{ U_i \to \mathbb{B}_{cl}^n \big\}_{i \in I}$.
\end{definition}

There is a functor
$$
  ClsdBalls
  \xrightarrow{\phantom{---}}
  OpenBalls
  \simeq
  CartSp
$$
given by restriction to interiors

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