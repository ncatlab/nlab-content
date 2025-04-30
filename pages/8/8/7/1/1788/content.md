

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](https://ncatlab.org/nlab/history/Sandbox).

\linebreak


***

Consider 

* $G$ a [[group]],

* $\mathbb{K}$ a [[ground field]] (or [[ground ring]]), 

* $\mathbb{K}[G] \,\coloneqq\, Span_{\mathbb{K}}\big( g \in G \big)$ the $\mathbb{K}$-[[linear span]] of the [[elements]] of $G$, equipped with the [[structure]] of the [[group algebra]] of $G$ [[associative algebra|over $\mathbb{K}$]], to be regarded canonically as a [[module]] ([[bimodule]]) over itself,

* $G Rep_{\mathbb{K}} \,\simeq\, \mathbb{K}[G]\text{-}Mod_{\mathbb{K}}$ the [[category of representations|category of]] $\mathbb{K}$-[[linear representations]] $G \curvearrowright V$ of $G$,

  $$
    \begin{array}{ccc}
      G \times V &\longrightarrow& V
      \\
      (g,v) &\mapsto& g \cdot v
      \mathrlap{\,,}
    \end{array}
  $$

  with [[intertwiners]] between them as [[morphisms]], 

  [[equivalence of categories|equivalently]] the [[category of modules|category of]] [[module|$\mathbb{K}[G]$-modules]], with [[hom-spaces]] to be denoted

  $$
    Hom_G(-,-) \,\equiv\, Hom_{\mathbb{K}[G]}(-,-)
    \mathrlap{\,,}
  $$

*  $H \xhookrightarrow{\iota} G$ a [[subgroup]] inclusion.

Write
\[
  \label{FunctorOfRestrictedRepresentation}
  \iota^\ast
  \;\colon\;
  G Rep_{\mathbb{K}}
  \xrightarrow{\;}
  H Rep_{\mathbb{K}}
\]
for the functor forming [[restricted representations]] along $\iota \colon H \hookrightarrow G$ (letting $H$ act on a given $G$-representation via its inclusion $\iota$ into $G$).

\begin{proposition}
**(left induced representation)**
  The functor $\iota^\ast$ (eq:FunctorOfRestrictedRepresentation) has a [[left adjoint]] $\iota_! \colon H Rep_{\mathbb{K}} \xrightarrow{\;} G Rep_{\mathbb{K}}$ given by
  $$
    V \in H Rep_{\mathbb{K}}
    \;\;\;\;\;\;
    \vdash
    \;\;\;\;\;\;
    \iota_{!} V
    \;\coloneqq\;
    \mathbb{K}[G]
      \otimes_{\mathbb{K}[H]}
    V
    \,,
  $$
  where on the right we have the $\mathbb{K}$-[[vector space]] (or [[module|$\mathbb{K}$-module]]) [[underlying]] the [[tensor product of modules|tensor product of]] (right-with-left) [[module|$\mathbb{K}[H]$-modules]] equipped with the $G$-[[group action]] given by
\[
  \label{ActionOnLeftInducedRep}
  \left.
  \begin{array}{l}
    [a,v] \,\in\, \mathbb{K}[G] \otimes_{\mathbb{K}[H]} V
    \\
    g \,\in\, G
  \end{array}
  \right\}
  \;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;
  g \cdot [a,v] \,\coloneqq\, [g \cdot a, v]
  \,.
\]
\end{proposition}
\begin{proof}
We claim that the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) is given by [[evaluation]] at the [[neutral element]] $\mathrm{e} \in G$:
$$
  \left.
  \begin{array}{l}
    V \,\in\, H Rep_{\mathbb{K}}
    \\
    W \,\in\, G Rep_{\mathbb{K}}
  \end{array}
  \right\}
  \;\;\;\;\;
  \vdash
  \;\;\;\;\;
  \frac{
    \overset{
      \iota_! V
    }{
      \overbrace{
        \mathbb{K}[G] \otimes_{\mathbb{K}[H]} V
      }
    }
    \xrightarrow{\;\; f \;\;}
    W
  }{
    V 
    \xrightarrow{ f([\mathrm{e},-]) }
    \iota^\ast W
  }
$$
To see this, just observe that 
$$
  \left.
  \begin{array}{l}
    f \,\in\, Hom_G\big(
      \mathbb{C}[G] \otimes_{\mathbb{C}[H]} V
      ,\,
      W
    \big)
    \\
    h \,\in\, H
    \\
    v \,\in\, V
  \end{array}
  \right\}
  \;\;\;\;\;
  \vdash
  \;\;\;\;\;
  \begin{array}{rcl}
  f\big(
    [\mathrm{e}, h \cdot v]
  \big)
  &=&
  f\big(
    [\mathrm{e} \cdot h, v]
  \big)  
  \;=\;
  f\big(
    [h, v]
  \big)  
  \\  
  &=&
  f\big(
    [h \cdot \mathrm{e}, v]
  \big)
  \;=\;
  f\big(
    h \cdot [\mathrm{e}, v]
  \big)  
  \;=\;
  h \cdot
  \Big(
    f\big(
      [\mathrm{e}, v]
    \big)  
  \Big)
  \,,
  \end{array}
$$
where the first equality is by definition of the [[tensor product of bimodules|tensor product]], the second-but-last is (eq:ActionOnLeftInducedRep) and the last one is by the $G$-[[equivariance]] of $f$.
This shows that $f\big([\mathrm{e},-]\big)$ is $H$-[[equivariant]] and that it uniquely determines $f$, hence that we have a [[bijection]] of [[hom-sets]]

$$
  Hom_G\Big(
    \mathbb{K}[G] \otimes_{\mathbb{K}[H]} V
    ,\,
    W
  \Big)
  \;\;\simeq\;\;
  Hom_H\Big(
    V
    ,\,
    \iota^\ast W
  \Big)
  \,.  
$$

Finally, it is manifest that this bijection $f \mapsto f([\mathrm{e},-])$ is [[natural transformation|natural]] in $V$ and $W$, and so this establishes a [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) exhibiting the claimed [[adjoint functor|adjunction]] $\iota_! \dashv \iota^\ast$.
\end{proof}


\begin{proposition}
**(right induced representation)**
  The functor $\iota^\ast$ (eq:FunctorOfRestrictedRepresentation) has a [[right adjoint]] $\iota_\ast \colon H Rep_{\mathbb{K}} \xrightarrow{\;} G Rep_{\mathbb{K}}$ given by
  $$
    V \in H Rep_{\mathbb{K}}
    \;\;\;\;\;\;
    \vdash
    \;\;\;\;\;\;
    \iota_{\ast} V
    \;\coloneqq\;
    hom_H\big(
      \mathbb{K}[G]
      ,\,
      V
    \big)
    \,,
  $$
  where on the right we have the $\mathbb{K}$-[[vector space]] (or [[module|$\mathbb{K}$-module]]) of $H$-[[equivariant map|equivariant]] $\mathbb{K}$-[[linear maps]] equipped with the $G$-[[group action]] given by
\[
  \label{ActionOnRightInducedRep}
  \left.
  \begin{array}{l}
    f \,\colon\, \mathbb{K}[G] \xrightarrow{\;} V
    \\
    g \,\in\, G
    \\
    a \,\in\, \mathbb{K}[G]
  \end{array}
  \right\}
  \;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;
  (g \cdot f)(a) \,\coloneqq\, f(a \cdot g)
  \,.
\]
\end{proposition}
\begin{proof}
We claim that the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) is given by [[evaluation]] at the [[neutral element]] $\mathrm{e} \in G$:
$$
  \left.
  \begin{array}{l}
    V \,\in\, H Rep_{\mathbb{K}}
    \\
    W \,\in\, G Rep_{\mathbb{K}}
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
    hom_{H}\big(
      \mathbb{K}[G]
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
      hom_H\big(
       \mathbb{K}[G]
       ,\,
       V
      \big)
    \Big)
    \\
    h \,\in\, H
    \\
    w \,\in\, W
  \end{array}
  \right\}
  \;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;
  \begin{array}{rcl}
  f(h \cdot w)(\mathrm{e})
  &=&
  \big( h \cdot f(w) \big)(\mathrm{e})  
  \;=\;
  f(w)(\mathrm{e} \cdot h)
  \;=\;
  f(w)(h)
  \\
  &=&
  f(w)(h \cdot \mathrm{e})
  \;=\;
  h\cdot\big(f(w)(\mathrm{e})\big)
  \end{array}
  \,,
$$
where the first equality is the $G$-[[equivariance]] of $f$, the second is (eq:ActionOnRightInducedRep) and the last one is the $H$-[[equivariance]] of $f(w)$. This shows that $f(-)(\mathrm{e})$ is $H$-equivariant and that it uniquely determines $f$, hence that we have a [[bijection]] of [[hom-sets]]:
$$
  Hom_G\Big(
    W 
    ,\,
    hom_H\big(
      \mathbb{K}[G]
      ,\,
      V
    \big)
  \Big)
  \;\;\simeq\;\;
  Hom_H\big(
    \iota^\ast W 
    ,\,
    V
  \big)
$$

Finally, it is manifest that this bijection $f \mapsto f([\mathrm{e},-])$ is [[natural transformation|natural]], and so this establishes a [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) exhibiting the claimed [[adjoint functor|adjunction]] $\iota^\ast \dashv \iota_{\ast}$.
\end{proof}



On electrodynamics via field strengths instead of gauge potentials:

* Joshua Newey, John Terning, Christopher B. Verhaaren: *Geometrizing the Anomaly* &lbrack;[arXiv:2504.16998](https://arxiv.org/abs/2504.16998)&rbrack;


