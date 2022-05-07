
$\box$


$\perp$

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
\end{prop}
\begin{proof}
  We may [[presentable (infinity,1)-category]] the sequence in the [[classical model structure on topological spaces]] or the [[classical model structure on simplicial sets]], in the latter case we may assume that $A$  is presented by a [[Kan complex]].

Then the respective canonical model for the [[iterated loop space]] is evidently the ordinary [[1-category]]-theoretic [[fiber]] of the [[evaluation map]] out of the [[internal hom]]:
$$
  \Omega^n A
  \xrightarrow{ ev_\ast }
  Maps( S^d ,\, A )
  \xrightarrow{ ev_\ast }
  A
  \,.
$$
Moreover, the evaluation map is equivalently the image of the point inclusion under the [[internal hom]]-functor
$$
  ev_\ast 
  \;=\;
  Maps( \ast \to S^d ,\, A )
  \,.
$$
Since either model category is a [[Cartesian closed monoidal category|Cartesian closed]] [[monoidal model category|monoidal model]], hence an [[enriched model category]] over itself
and since $\ast \to S^d$ is a [[cofibration]] in either case, 


\end{proof}
Hence the [[homotopy groups]] of the mapping space form a [[long exact sequence]] with thos of $A$, of the following form:
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


