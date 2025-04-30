

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](https://ncatlab.org/nlab/history/Sandbox).

\linebreak


***

$Sym(T^\ast X \otimes T^\ast X)$

For $G$ a [[group]] and 
$$
  H \xhookrightarrow{\iota} G
$$
a [[subgroup]], write
\[
  \label{FunctorOfRestrictedRepresentation}
  \iota^\ast
  \;\colon\;
  G Rep_{\mathbb{C}}
  \xrightarrow{\;}
  H Rep_{\mathbb{C}}
\]
for the functor of [[restricted representations]].


\begin{proposition}
  The functor $\iota^\ast$ (eq:FunctorOfRestrictedRepresentation) has a [[right adjoint]] $\iota_\ast \colon H Rep_{\mathbb{C}} \xrightarrow{\;} G Rep_{\mathbb{C}}$ given by
  $$
    V \in H Rep_{\mathbb{C}}
    \;\;\;\;\;\;
    \vdash
    \;\;\;\;\;\;
    \iota_{\ast} V
    \;\coloneqq\;
    Hom_H\big(
      \mathbb{C}[H]
      ,\,
      V
    \big)
    \,,
  $$
  where on the right we have the [[vector space]] of $H$-[[equivariant map|equivariant]] [[linear maps]] equipped with the $G$-[[group action]] given by
$$
  \left.
  \begin{array}{l}
    f \,\colon\, \mathbb{C}[H] \xrightarrow{\;} V
    \\
    g \,\in\, G
  \end{array}
  \right\}
  \;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;
  g \cdot f \,\coloneqq\, f(- \cdot g)
  \,.
$$
\end{proposition}
\begin{proof}
We claim that the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) is given by [[evaluation]] at the [[neutral element]] $\mathrm{e} \in G$:
$$
  \left.
  \begin{array}{l}
    V \,\in\, H Rep
    \\
    W \,\in\, G Rep
  \end{array}
  \right\}
  \;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;
  \frac{
  W 
  \xrightarrow{\;\;\;\; f \;\;\;\;}
  \overset{\iota_\ast V}{
  \overbrace{
    Hom_{H}\big(
      \mathbb{C}[H]
      ,\,
      V
    \big)
  }
  }
  }{
    \iota^\ast W 
    \xrightarrow{\;\; f(-)(\mathrm{e}) \;\;} 
    V
  }
$$
To see this, just observe that 
$$
  \left.
  \begin{array}{l}
    f \,\in\, 
    Hom_G\Big(
      W
      ,\,
      Hom_H\big(
       \mathbb{C}[H]
       ,\,
       V
      \big)
    \Big)
    \\
    h \,\in\, H
  \end{array}
  \right\}
  \;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;
  f(h \cdot -)(\mathrm{e})
  \;=\;
  \big( h \cdot f(-)\big)(\mathrm{e})  
  \;=\;
  f(-)(\mathrm{e} \cdot h)
  \;=\;
  f(-)(h)
  \,,
$$
where the first equality is the $G$-[[equivariance]] of $f$, and the second is the $H$-[[equivariance]] of $f(-)$. This shows that $f(-)(\mathrm{e})$ is $H$-equivariant and that it uniquely determines $f$. 

\end{proof}



On electrodynamics via field strengths instead of gauge potentials:

* Joshua Newey, John Terning, Christopher B. Verhaaren: *Geometrizing the Anomaly* &lbrack;[arXiv:2504.16998](https://arxiv.org/abs/2504.16998)&rbrack;


