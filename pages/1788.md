

\begin{prop}
 For $A$ a [[pointed homotopy type]], hence an [[∞-groupoid]] equipped with a base point $\ast \xrightarrow{ pt_A } A$,
then for $n \,\in\, \mathbb{N}$, the [[iterated loop space|n-fold loop space]] of $A$ is the [[homotopy fiber]] of basepoint-[[evaluation map]] on the [[mapping space]] from the [[homotopy type]] of the [[n-sphere]]:
$$
  \Omega^n A
  \xrightarrow{ hofib(ev_{\ast}) }
  Maps
  \big( 
    &#643; S^d 
    ,\,
    A
  \big)
  \xrightarrow{ ev_\ast }
  A
$$

\begin{tikzcd}[column sep=10pt]
    \cdots
    \ar[r]
    &
    \pi_{\bullet + 1}(A)
    \ar[rr]
    &&
    \pi_{\bullet+d}(A)
    \ar[
      rr
    ]
    &&
    \pi_{ \bullet }
    \big(
      \mathrm{Maps}
      ( 
        S^d 
        \,
         A 
      )
    \big)
    \ar[
      rr
    ]
    &&
    \pi_{\bullet}(A)
    \ar[
      rr
    ]
    &&
    \pi_{\bullet + d-1}(A)
    \ar[r]
    &
    \cdots
\end{tikzcd}


\end{prop}


