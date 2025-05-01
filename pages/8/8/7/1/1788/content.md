

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak


***

[[CategoriesAndToposes-20250501.pdf:file]]

\begin{corollary}
The [[unit of an adjunction|counit]] $\eta^{L}$ of the left [[adjoint functor|adjunction]] $\iota_! \dashv \iota^\ast$ (Prop. \ref{LeftInductionAdjunction}) is given by inserting the [[neutral element]]:
$$
  \begin{array}{rcc}
    V
    &\xrightarrow{\phantom{--} \epsilon^L_V \phantom{--}}&
    \mathbb{K}[G]
      \otimes_{\mathbb{K}[H]}
    V
    \\
    v &\mapsto& [\mathrm{e},v]
  \end{array}
$$
\end{corollary}
\begin{proof}
  The [[adjunction unit]] is (see [there](adjoint+functor#AdjunctionUnitFromHomIsomorphism)) the [[adjunct]] $\widetilde{(-)}$ of the [[identity map]]:
  $$
  \begin{array}{rcl}
    \mathbb{K}[G]
      \otimes_{\mathbb{K}[H]}
    V
    &\xrightarrow{\phantom{--} id \phantom{--}}&
    \mathbb{K}[G]
      \otimes_{\mathbb{K}[H]}
    V
    \mathrlap{\,,}
  \end{array}
  $$
  hence is its image $\widetilde{id}$ under the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) (eq:LeftHomIso). From that formula (eq:LeftHomIso) we have indeed
  $$
    \widetilde{id}(\phi)(v)
    \;=\;
    id([\mathrm{e},v])
    \;=\;
    [\mathrm{e},v]
    \,.
  $$
\end{proof}


The passage of [[group]] [[inverse elements]] $(-)^{-1}$ on $G$ extends to an [[anti-involution]] $\overline{(-)}$ on $\mathbb{K}[G]$, 

$$
  \overline{
    \textstyle{\sum_g} c_g \, g
  }
  \;=\;
  \textstyle{\sum_g} \overline{c_g} \, g^{-1}  
  \,.
$$ 

\begin{lemma}
\label{ComparisonBetweenLeftAndRightInducedRepresentations}
**(comparison map between left and right induced representations)**
\linebreak
For $H \xhookrightarrow{\;} G$ a [[subgroup]] inclusion and
$V \in H Rep$,
we have a $G$-[[equivariant]] [[linear map|linear]] [[injection]] from the left into the right induced representation
$$
  \mathbb{K}[G] \otimes_{\mathbb{K}[H]} V
  \xhookrightarrow{\phantom{--}\phi\phantom{--}}
  hom_H\big(
    \mathbb{K}[G]
    ,\,
    V
  \big)
  \mathrlap{\,,}
$$
[[natural transformation|natural]] in $V$, which is an [[isomorphism]] if the subgroup inclusion $H \hookrightarrow G$ has [[finite number|finite]] [[index of a subgroup|index]]. 
\end{lemma}
\begin{proof}
Define $\phi$ to take homogeneous elements of the form $[g,v]$, for $g \in G$, to the linear map $\phi[g,v] \,\colon\, \mathbb{K}[G] \to V$ which, in turn, is given on basis elements $g' \in G \subset \mathbb{C}[G]$ by
$$
  \phi[g,v]
  \;\colon\;
  g'
    \;\mapsto\;
  \left\{
  \begin{array}{lll}
    h \cdot v &\vert& g' = h \cdot g^{-1}
    \\
    0 &\vert& \text{otherwise}
  \end{array}
  \right.
$$
First to observe that this construction is well defined, 
in that 

1. $\phi[g,v]$ is $H$-equivariant, 

   which is immediate from the form of the above formula;

1. $\phi$ is independent of the choice of representative $[g,v] = [g \cdot k, k^{-1}\cdot v]$, 

   which is seen from
   $$
     \phi[g \cdot k, k^{-1} \cdot v]
     \;\colon\;
     g' 
       \;\mapsto\;
     \left\{
     \begin{array}{lll}
       h \cdot k^{-1} \cdot v 
          &\vert& 
           g' 
            = 
           h \cdot (g \cdot k)^{-1} 
            = 
           h \cdot k^{-1} \cdot g^{-1}
       \\
       0 &\vert& \text{otherwise}
     \end{array}
     \right.
   $$
   whence indeed
   $
     \phi[g \cdot k, k^{-1} \cdot v]
     \;=\;
     \phi[g,v]
     \,;
   $

1. $\phi$ is $G$-equivariant,

   which is seen by computing for $q \in G$ as follows:
   $$
     \begin{array}{rcl}
     \phi\big(
       q \cdot [g,v]
     \big)(g')
     &\equiv&
     \phi\big(
       [q \cdot g,v]
     \big)(g')
     \\
     &=&
     \left\{
     \begin{array}{rcl}
       h \cdot v &\vert& g' = h \cdot (q\cdot g)^{-1}
       \\
       0 &\vert& \text{otherwise}
     \end{array}
     \right.
     \\
     &=&
     \left\{
     \begin{array}{rcl}
       h \cdot v &\vert& g' \cdot q = h \cdot g^{-1}
       \\
       0 &\vert& \text{otherwise}
     \end{array}
     \right.
     \\
     &=&
     (\phi[g,v])(g' \cdot q)
     \\
     &\equiv&
     \big( q \cdot \phi[g,v] \big)(g')
     \mathrlap{\,.}
     \end{array}
   $$

It is also immediate that the construction is natural in $V$.

Now the $H$-equivariance implies that for any choice of [[section]] $[g] \mapsto g$ of the [[coset]] [[quotient]] [[coprojection]] $ G \twoheadrightarrow G/H$ (in [[Sets]]) the [[range]] of $\phi$ is [[linear span|spanned]] by the combinations $\sum_{[g] \in G/H} \phi[g,v_g]$.

For this to vanish on all $g'$ clearly all the $v_g$ must vanish separately, which shows that the kernel of $\phi$ is $0$, hence that we have an injection. 

At the same time, if $H$ has finite index in $G$ then both this range as well as the [[codomain]] 
$
  hom_H\big(
    \mathbb{K}[G]
    ,\,
    V
  \big)
$
have [[finite dimensional vector space|finite dimension]], equal to the number ${\vert G \colon H\vert}$ of $H$-[[cosets]] of elements of $G$. 
This means (by the *[[rank-nullity theorem]]*, if you wish) that in the case of finite index the injection $\phi$ is moreover surjective and hence an [[isomorphism]], as claimed.
\end{proof}

\begin{proposition}
  When the subgroup inclusion $H \xhookrightarrow{\iota} G$ has [[finite number|finite]] [[index of a subgroup|index]] then the left and right induced representation functors are [[natural isomorphism|naturally isomorphic]] $\iota_! \simeq \iota_{\ast}$, constituting with $\iota^\ast$ an [[ambidextrous adjunction]].
\end{proposition}
\begin{proof}
  By Lem. \ref{ComparisonBetweenLeftAndRightInducedRepresentations}.
\end{proof}

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


