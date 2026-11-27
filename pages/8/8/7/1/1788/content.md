

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", there is no harm in breaking the lock, as it is just caused by bot traffic. When the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.


***


[[lax morphism|lax $T$-morphisms]]

$\beta^3$

\begin{tikzcd}
  X^{11}
  \ar[d]
  \ar[r]
  \ar[dr, phantom, "{ \lrcorner }"{pos=.1}]
  &
  L S^4
  \ar[d]
  \ar[r]
  \ar[dr, phantom, "{ \lrcorner }"{pos=.1}]
  &
  \ast
  \ar[d]
  \\
  X^{10}
  \ar[r]
  &
  \mathrm{Cyc} S^4
  \ar[r]
  & 
  B S^1
\end{tikzcd}


\begin{tikzcd}
  X'
  \ar[r]
  \ar[d, hook]
  \ar[dr, phantom, "{ \lrcorner }"{pos=.1}]
  & 
  (\ast \times \mathbb{R}^3)_+
  \ar[d, hook]
  \\
  X^{11}
  \ar[d]
  \ar[r]
  \ar[dr, phantom, "{ \lrcorner }"{pos=.1}]
  &
  (S^1 \times \mathbb{R}^3)_+
  \ar[r, hook]
  \ar[d]
  \ar[dr, phantom, "{ \lrcorner }"{pos=.1}]
  &
  L S^4
  \ar[d]
  \ar[r]
  \ar[dr, phantom, "{ \lrcorner }"{pos=.1}]
  &
  \ast
  \ar[d]
  \\
  X^{10}
  \ar[r]
  &
  B S^1
    \vee 
  S^3 
  \ar[r]
  &
  \mathrm{Cyc} S^4
  \ar[r]
  & 
  B S^1
\end{tikzcd}


\begin{tikzcd}
  S^2 
   \ar[r, "{ n }"]
   \ar[d, hook]
  &
  B S^1
  \ar[d]
  \\
  D^3
  \ar[r, hook]
  &
  \mathrm{MinCyc}_n S^4
\end{tikzcd}
...