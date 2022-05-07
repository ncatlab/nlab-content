
\begin{proposition}
Let 

* $\mathbf{H}$ be an [[(infinity,1)-topos|$\infty$-topos]];

* $G \,\in\, Groups(\mathbf{H})$ a [[group object in an (infinity,1)-category|group object]] ([[infinity-group|$\infty$-group]]);

* $G \curvearrowright X \,\in\, A Act(\mathbf{H})$ an [[infinity-action|$\infty$-action]] of $G$ on $X$.

If this is an $\infty$-[[free action]] in that all its higher [[shear maps]] are [[n-truncated object in an (infinity,1)-category|(-1)-truncated]]

\begin{tikzcd}
  X \times G^n
  \ar[r, hook]
  &
  X^{\times_{n+1}}
\end{tikzcd}

then the [[homotopy quotient]] is [[0-truncated]], in that for every $U \,\in\, \mathbf{H}$ and every $\infty$-group $K$ (sufficient to consider those in the image of $Grpd_\infty \xrightarrow{ LConst } \mathbf{H}$)
factors through the [[projection]] $U \times \mathbf{B}K \xrightarrow{ pr_2 } U$:

\begin{tikzcd}
  \mathbf{B}K
  \ar[rr]
  \ar[d]
  &&
  X /\!\!/ G
  \\
  \ast
  \ar[urr, dashed]
\end{tikzcd}
\end{proposition}
\begin{proof}
Given a morphism $\mathbf{B}K \to X \sslash G$, regard it as a morphism over the [[terminal object]] $\ast$ and then form the following diagram of [[atlas|atlases]] and their [[Cech nerves]] over it:
  \begin{tikzcd}
    K \times K
    \ar[dd, shift left=12pt]
    \ar[from=dd, shift left=6pt]
    \ar[dd]
    \ar[from=dd, shift right=6pt]
    \ar[dd, shift right=12pt]
    \ar[rr]
    \ar[dr, ->>]
    &&
    X \times G \times G
    \ar[dd, shift left=12pt]
    \ar[from=dd, shift left=6pt]
    \ar[dd]
    \ar[from=dd, shift right=6pt]
    \ar[dd, shift right=12pt]
    \ar[dr, hook]
    \\
    & 
    \ast
    \ar[rr, crossing over]
    \ar[ur, dashed]
    &&
    X \times X \times X
    \ar[dd, shift left=12pt]
    \ar[from=dd, shift left=6pt]
    \ar[dd]
    \ar[from=dd, shift right=6pt]
    \ar[dd, shift right=12pt]
    \\
    K
    \ar[rr]
    \ar[dr, ->>]
    \ar[dd, shift left=6pt]
    \ar[from=dd]
    \ar[dd, shift right=6pt]
    &&
    X \times G
    \ar[dr, hook]
    \ar[dd, shift left=6pt]
    \ar[from=dd]
    \ar[dd, shift right=6pt]
    \\
    & 
    \ast
    \ar[rr, crossing over]
    \ar[from=uu, shift left=12pt, crossing over, end anchor={[yshift=7pt]}]
    \ar[uu, shift left=6pt, crossing over, start anchor={[yshift=3pt]}]
    \ar[from=uu, crossing over]
    \ar[uu, shift right=6pt, crossing over, start anchor={[yshift=3pt]}]
    \ar[from=uu, shift right=12pt, crossing over, end anchor={[yshift=7pt]}]
    \ar[ur, dashed]
    &&
    X \times X
    \ar[dd, shift left=6pt]
    \ar[from=dd]
    \ar[dd, shift right=6pt]
    \\
    \ast
    \ar[rr]
    \ar[dd, ->>]
    \ar[dr, -, shift left=1pt]
    \ar[dr, -, shift right=1pt]
    &&
    X
    \ar[dd, ->>]
    \ar[dr, -, shift left=1pt]
    \ar[dr, -, shift right=1pt]
    \\
    &
    \ast 
    \ar[rr, crossing over]
    \ar[from=uu, shift left=6pt, crossing over]
    \ar[uu, crossing over]
    \ar[from=uu, shift right=6pt, crossing over]
    \ar[ur, dashed]
    &&
    X
    \ar[dd, ->>]
    \\
    \mathbf{B}K
    \ar[rr]
    \ar[dr]
    &&
    X /\!\!/ G
    \ar[dr]
    \\
    & 
    \ast
    \ar[rr]
    \ar[from=uu, ->>, crossing over]
    \ar[ur, dashed]
    &&
    \ast
  \end{tikzcd}  
By the assumptions on $K$ and on $G \curvearrowright X$ all the upper horizontal squares have a [[(-1)-connected]] morphism on the left and a [[(-1)-truncated]] morphism on the right. Since connected/truncated morphisms for [[(infinity,1)-categories of (infinity,1)-presheaves]] are detected objectwise,  this means that the entire square diagram of [[Cech nerve]] [[simplicial objects]] has a [[(-1)-connected]] morphism on the left and a [[(-1)-truncated]] morphism in the right. Therefore, the [[(n-connected, n-truncated) factorization system]] there exist compatible dashed [[lifts]] filling all the upper squares. But then passaged back to the [[(infinity,1)-colimits]] and using that [[groupoid objects in an (infinity,1)-topos are effective|groupoid objects in an $\infty$-topos are effective]], shows that there is a dashed [[lift]] in the bottom square. This is the claimed factorization through the point.
\end{proof}

