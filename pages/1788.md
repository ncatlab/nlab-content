
\begin{proposition}
  Let $\mathbf{H}$ be a [[cohesive (infinity,1)-topos|cohesive $\infty$-topos]], and consider $Y \,\in\, \mathbf{H}_{\sharp_1} \xhookrightarrow{\;} \mathbf{H}$ a [[concrete object]], in that its [[sharp modality]] [[unit of a monad|unit]] is a [[n-truncated object of an (infinity,1)-category|(-1)-truncated]]: $Y \xhookrightarrow{ \;\;\eta^\sharp_Y\;\; } \sharp Y$.  Then *cohesive maps to $X$ glue* (satisfy the respective sheaf property): 

For any $Y \,\in\, \mathbf{H}$ and any open cover, namely any [[n-connected object of an (infinity,1)-topos|(-1)-connected]]/[[effective epimorphism in an (infinity,1)-category|effective epi-morphism]] $U \twoheadrightarrow{\;\;} X$, cohesive maps $U \xrightarrow X$ whose maps of [[underlying]] $\infty$-groupoids descend/extend to $Y$, then they also descend/extend to $Y$ as cohesive maps, in an essentially unique way, in that all solid [[homotopy]]-[[commutative square]] as follows have essentially unique dashed lifts:

\begin{tikzcd}[row sep=20pt, column sep=20pt]
  U
  \ar[
    rr,
    "{ \forall }"{above}
  ]
  \ar[
    dd,
    ->>
  ]
  &&
  X
  \ar[
    dd,
    hook,
    "{ \eta^\sharp_X }"
  ]
  \\
  \\
  Y
  \ar[
    rr,
    "{ \forall }"{below}
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists ! }"{description}
  ]
  &&
  \sharp X
\end{tikzcd}

\end{proposition}
The point here is the given interpretation of this [[lifting problem]], but the proof of the latter is immediate:
\begin{proof}
  The essentially unique existence of the lift is an instance of the [[(n-connected, n-truncated) factorization system]] for $n = (-1)$.
\end{proof}


