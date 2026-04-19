> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.

***

\begin{lemma}
  The map
  $$
    \begin{array}{ccc}
      \pi_0\big(X \times_B Y\big) 
      &\longrightarrow&
      \pi_0(X) \times_{\pi_0(B)} \pi_0(Y)
      \\
      [(x,y,\gamma)] 
      &\mapsto&
      ([x],[y])
    \end{array}
  $$
  is surjective.
\end{lemma}
\begin{proof}
  As indicated, here we think of the homotopy fiber product $X \times_B Y$ as presented, via the [factorization lemma](Introduction+to+Homotopy+Theory#FactorizationLemma), as the space of triples consisting of a point $x \in X$, a point $y \in Y$ and a path $\gamma$ in $B$ from $f(x)$ to $g(y)$. But if $x$ and $y$ are given so $([x],[y]) \in \pi_0(X) \times_{\pi_0(B)} \pi_0(Y)$ this means exactly that $f(x)$ and $g(y)$ are path connected, hence that $\gamma$ as above exists, hence that $([x],[y])$ in in the image of the above map.
\end{proof}


\begin{xymatrix}
Q B \ar[d] \ar[r] & Q A \sqcup Q B \ar[d] \ar[r] & A \sqcup Q B \ar[d]\cr
  B        \ar[r] & Q A \sqcup   B        \ar[r] & A \sqcup   B       \cr
\end{xymatrix}