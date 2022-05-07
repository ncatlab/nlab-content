
$$
  &#9025;
  \;\;
  &#x2341;
  \;\;
  &solb;
$$

$\esh$

\begin{tikzpicture}
  \draw (0,0) node {A};
\end{tikzpicture}

\begin{definition}\label{ShapeOfToposAsImageOfItsPointUnderProLeftAdjointToLConst}
**(shape of an $\infty$-topos -- [Hoyois 2013, p. 3](#Hoyois13))**
\linebreak
  For $(\Gamma \dashv LConst) \;\colon\; \mathbf{H} \to \infty Grpd$ an [[(infinity,1)-topos|$(\infty,1)$-topos]],
  write (with convenient overloading of notation)
  $$
    \array{
      Shp 
      \;\colon\; 
      &
      \mathbf{H} 
      &\longrightarrow&
      Pro(\infty Grpd)
      \\
      &
      X
      &\mapsto&
      \mathbf{H}  
      \big(
        \ast_{\mathbf{H}}
        ,\,
        LConst(-)
      \big)
    }
  $$
  for the [[pro-left adjoint]] to $LConst \,\colon\, \infty Grpd \to \mathbf{H},$ and say that the *shape of $\mathbf{H}$* is the image under this pro-left adjoint of its [[terminal object]] $\ast_{\mathbf{H}}$:
$$
  Shp(\mathbf{H})
  \;\coloneqq\;
  Shp(\ast_{\mathbf{H}})
  \,.
$$
\end{definition}

\begin{prop}
  Def. \ref{ShapeOfToposAsImageOfItsPointUnderProLeftAdjointToLConst}
  is equivalent to Def. \ref{LurieShapeOfAnInfinityTopos}
\end{prop}
\begin{proof}
Consider the following sequence of [[natural equivalence|natural]] [[equivalence in an (infinity,1)-category|equivalences]]:
$$
\begin{aligned}
  Shp(\mathbf{H})
  &
  \;\simeq\;
  \Gamma \circ LConst(-)
  \\
  &
  \;\simeq\;
  \infty Grpd
  \big(
    \ast
    ,\,
    \Gamma \circ LConst(-)
  \big)
  \\
  & 
  \;\simeq\;
  \mathbf{H}
  \big(
    LConst(\ast)
    ,\,
    LConst(-)
  \big)
  \\
  & \;\simeq\;
  \mathbf{H}
  \big(
    \ast_{\mathbf{H}}
    ,\,
    LConst(-)
  \big)
  \\
  & 
  \;\simeq\;
  Shp(\ast_{\mathbf{H}})
\end{aligned}
$$
Here the first equivalence is just Def. \ref{LurieShapeOfAnInfinityTopos} (alternatively: is Prop. \ref{ShapeIsGlobalSectionsOfLConst}), while all the following ones are the characteristic [hom-equivalences](adjoint+infinity1-functor#CharacterizationInTermsOfHomEquivalences) of the [[adjoint (infinity,1)-functor|adjoint $(\infty,1)$-functors]] involved. In the second but last step we use that $LConst$, being a [[left exact functor]], [[preserved limit|preserves]] [[terminal object in an (infinity,1)-category|terminal objects]].
\end{proof}



