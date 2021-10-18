
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

> For the time being, the following speaks in [[(infinity,1)-topos theory|$\infty$-topos theory]], for definiteness; but all statements and proofs apply verbatim also to [[Grothendieck toposes]], since they just depend on general abstract category-theoretic properties.


## Idea

For $\mathbf{H}$ an [[(infinity,1)-topos|$\infty$-topos]] over the [[base (infinity,1)-topos|base $\infty$]]-[[Infinity-Grpd|$Grpd_\infty$]], it has an essentially unique [[(infinity,1)-geometric morphism|geometric morphism]] to [[Infinity-Grpd|$Grpd_\infty$]]

\[
  \label{TheGeometricMorphism}
  \mathbf{H}
  \underoverset
    {\underset{\Gamma}{\longrightarrow}}
    {\overset{LConst}{\longleftarrow}}
    {\;\;\;\;\bot\;\;\;\;}
  Grp_\infty
\]

where:

* the [[left adjoint]] has the interpretation of constructing [[locally constant infinity-stacks|locally constant $\infty$-stacks]],

* the [[right adjoint]] has the interpretation of forming [[global sections]].

In other words, [[Infinity-Grpd|$Grpd_\infty$]] is the [[terminal object in an (infinity,1)-category|terminal object]] in the [[(infinity,1)-category|$\infty$-category]] [[(infinity,1)Topos|$Topos_\infty$]] of [[infinity-stack (infinity,1)-toposes|$\infty$-stack $(\infty,1)$-toposes]] and [[(infinity,1)-geometric morphisms|$\infty$-geometric morphisms]] between these.

## Properties

\begin{proposition}
  The geometric morphism (eq:TheGeometricMorphism) exists essentially uniqyely.
\end{proposition}
(e.g. [Lurie 2009, HTT 6.3.4.1](#Lurie09))
\begin{proof}
  Since every [[infinity-groupoid|$\infty$-groupoid]] is an [[(infinity,1)-colimit|$\infty$-colimit]] (over itself) of the [[point]] (see [there](infinity1-limit#Tensoring)):

\[
  \label{InfinityGroupoidIsColimitOfPointOverItself}
  S \,\simeq\,
  \underset{\underset{S}{\longrightarrow}}{\lim} \,\ast
\]
and since the [[inverse image]] of a geometric morphism [[preserved limit|preserves]] [[finite limits]] (by definition), such as the [[terminal object]], and all [[(infinity,1)-colimits|$\infty$-colimits]] (since [[left adjoints preserve colimits]]), we have that $LConst$ must be given by forming the corresponding $\infty$-colimit of copies of the terminal object $\ast_{\mathbf{H}}$ in $\mathbf{H}$, which does exist:

$$
  \begin{aligned}
    LConst(S)
    &
    \;\simeq\;
    LConst
    \Big(
      \underset{
        \underset{S}{\longrightarrow}
      }{\lim}
      \,
      \ast
    \Big)
    \\
    &
    \;\simeq\;
    \underset{
      \underset{S}{\longrightarrow}
    }{\lim}
    \,
    LConst
    \big(
      \ast
    \big)
    \\
    &
    \;\simeq\;
    \underset{
      \underset{S}{\longrightarrow}
    }{\lim}
    \,
    \ast_{\mathbf{H}}
  \end{aligned}  
$$
\end{proof}


\begin{proposition}
\label{DirectImageOfTerminalGeometricMoprhismIsHomOutOfTerminalObject}
The [[direct image]] of the terminal geometric morphism (eq:TheGeometricMorphism) is given by the [[(infinity,1)-categorical hom-space|hom-space]] out of the [[terminal object]], in that 
for $X \,\in\, \mathbf{H}$ there is a [[natural equivalence]]
$$
  \Gamma (X)
  \;\simeq\;
  \mathbf{H}(\ast_{\mathbf{H}} ,\, X)
  \,,
$$
where $\ast_{\mathbf{H}} \,\in\, \mathbf{H}$ denotes the [[terminal object in an (infinity,1)-category|terminal object]].
\end{proposition}
\begin{proof}
For all $S \,\in\, Grpd_\infty$ we have the following sequence of [[natural equivalences]]:
$$
  \begin{array}{lll}
    Grpd_\infty
    \big(
      S
      ,\,
      \mathbf{H}(\ast_{\mathbf{H}} ,\, X)
    \big)
    & 
    \;\simeq\;
    Grpd_\infty
    \Big(
      \underset{\underset{S}{\longrightarrow}}{\lim} \ast
      ,\,
      \mathbf{H}(\ast_{\mathbf{H}} ,\, X)
    \Big)
    \\
    & 
    \;\simeq\;
    \underset{\underset{S}{\longleftarrow}}{\lim}
    \,
    Grpd_\infty
    \big(
      \ast
      ,\,
      \mathbf{H}(\ast_{\mathbf{H}} ,\, X)
    \big)
    \\
    & 
    \;\simeq\;
    \underset{\underset{S}{\longleftarrow}}{\lim}
    \,
    \mathbf{H}(\ast_{\mathbf{H}} ,\, X)
    \\
    & 
    \;\simeq\;
    \mathbf{H}
    \Big(
      \underset{\underset{S}{\longleftarrow}}{\lim}
      \ast_{\mathbf{H}} 
       ,\, 
       X
    \Big)
    \\
    & 
    \;\simeq\;
    \mathbf{H}
    \Big(
      \underset{\underset{S}{\longleftarrow}}{\lim}
      \,
      LConst(\ast) 
       ,\, 
       X
    \Big)
    \\
    & 
    \;\simeq\;
    \mathbf{H}
    \Big(
      LConst
      \big(
        \underset{\underset{S}{\longleftarrow}}{\lim}
        \ast
      \big)
      ,\, 
      X
    \Big)
    \\
    & 
    \;\simeq\;
    \mathbf{H}
    \big(
      LConst(S)
      ,\, 
      X
    \big)
  \end{array}
$$
(Here we used (eq:InfinityGroupoidIsColimitOfPointOverItself) and that [[hom-functor preserves limits]] and that [[left adjoints preserve colimits]] and that $LConst$ [[preserved limit|preserves]] [[finite limits]] such as the [[terminal object]], by definition.)

But this is a hom-equivalence which exhibits (see [here](adjoint+infinity1-functor#CharacterizationInTermsOfHomEquivalences)) $\mathbf{H}(\ast,-)$ as a [[right adjoint|right]] [[adjoint (infinity,1)-functor|adjoint $\infty$-functor]] to $LConst$. This implies the claim by essential uniqueness of adjoints.
\end{proof}

## Literature

For discussion in plain [[topos theory]] see any of the references listed there.

Discussion in [[(infinity,1)-topos theory|$\infty$-topos theory]] includes:


* {#Lurie09} [[Jacob Lurie]], Section 6.3.4 in: *[[Higher Topos Theory]]*, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))

[[!redirects terminal geometric morphisms]]

[[!redirects terminal (infinity,1)-geometric morphism]]
[[!redirects terminal (infinity,1)-geometric morphisms]]

