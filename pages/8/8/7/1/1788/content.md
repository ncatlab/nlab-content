
...

Let $\widehat{G} \overset{p}{\twoheadrightarrow} G $ be a surjective homomorphism of discrete groups. For $H \subset G$ a subgroup, write $\widehat{H} \subset \widehat{G}$ for its pullback

\begin{tikzcd}
  \widehat{H}
  \ar[r, hook]
  \ar[d,->>]
  \ar[dr, phantom, "\mbox{\tiny(pb)}"]
  &
  \widehat{G}
  \ar[d,->>]
  \\
  H
  \ar[r, hook]
  &
  G
\end{tikzcd}


Then

\begin{tikzcd}
  \widehat{G}\mathrm{Orbt}
  \ar[from=r, hook', shift left=7pt, "R"]
  \ar[r, shift left=7pt, "L"]
  \ar[r, phantom, "\scalebox{.7}{$\bot$}"]
  &
  G\mathrm{Orbt}
\end{tikzcd}

where

* $R(G/H) \,=\, \widehat{G}/\widehat{H}$

* $L(\widehat{G}/K) \,=\, G/p(K)$.

A transparent way to see this is to identify $G$-orbits with the [[n-truncated object of an (infinity,1)-category|0-truncated objects]] in the $B G$-slice of $Singlrt \,\coloneqq\, Grpd_1^{cn} $: 

$$
  G Orbt \;\simeq\; \left( (Grpd_1^{cn})_{/ B G} \right)_0
  \,.
$$

Under this identification, the adjunction is the canonical left [[base change]] on slices composed with the [[n-truncated object of an (infinity,1)-category|0-truncation]] reflection ([here](n-truncated+object+of+an+infinity1-category#nTruncationReflection)):

\begin{tikzcd}
  (\mathrm{Grpd}_1^{\mathrm{cn}})_{/ B \widehat{G}}
  \ar[from=r, shift left=7pt, "(B p)^\ast"]
  \ar[r, shift left=7pt, "(B p)_!"]
  \ar[r, phantom, "\scalebox{.7}{$\bot$}"]
  &
  (\mathrm{Grpd}_1^{\mathrm{cn}})_{/ B G}
  \ar[from=r, hook', shift left=7pt]
  \ar[r, shift left=7pt, "\tau_0"]
  \ar[r, phantom, "\scalebox{.7}{$\bot$}"]
  &
  \left( (\mathrm{Grpd}_1^{\mathrm{cn}})_{/ B G} \right)_0
\end{tikzcd}

That the right adjoint $R$ is fully faithful is most readily seen by direct inspection: A function of $\widehat{G}$-sets on which $\widehat{G}$ acts only through $G$ is evidently $\widehat{G}$-equivariant if and only if it is $G$-equivariant.



$$
  Hom
  \big(
    \mathcal{X}
    ,\,
    \mathcal{Y}
  \big)
  \xrightarrow{\;\;\;}
  Hom
  \big(
    \mathcal{X} \times B N
    ,\,
    \mathcal{Y}
  \big)
$$



