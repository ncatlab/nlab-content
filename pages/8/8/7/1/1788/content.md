


\begin{lemma}
\label{OneMorphismsInShapeOfMapsFromSphericalFormToBGammaParallelToOneComingFromShapeOfMapsFromBGToBGamma}
  If there exists any [[1-morphism]] in 
  $\esh \,Maps\big( S^{n+2}/G ,\, \mathbf{B}\Gamma \big)$
  (Exp. \ref{OneMorphismInShapeOfMappingStackFromSphericalSpaceFormToBGamma})
  between a [[pair]] of vertices in the image of
  $$
    TopFun
    \big(
      (G \rightrightarrows \ast)
      ,\,
      (\Gamma \rightrightarrows \ast)
    \big)_0
    \xrightarrow{\phantom{--} p^\ast \phantom{--}}
    TopFun
    \big(
      (S^{n+2} \times G \rightrightarrows S^{n+2})
      ,\,
      (\Gamma \rightrightarrows \ast)
    \big)_0
  $$  
  then there exists a morphism between them in the image of
  $$
    TopFun
    \big(
      (G \rightrightarrows \ast) \times \Delta^1
      ,\,
      (\Gamma \rightrightarrows \ast)
    \big)_1
    \xrightarrow{\phantom{--} p^\ast \phantom{--}}
    TopFun
    \big(
      (S^{n+2} \times G \rightrightarrows S^{n+2}) \times \Delta^1
      ,\,
      (\Gamma \rightrightarrows \ast)
    \big)_1    
  $$  
\end{lemma}
\begin{proof}
By Lemma
\ref{OneMorphismsInShapeOfMapsFromSphericalFormToBGammaEquivalentlyHaveConstantUnderlyingBundle}
we may assume without restriction that the underlying bundle is constant
along $\Delta^1$. The remaining data in the 1-morphism is a continuous function
$$
  \phi
  \,\colon\,
  \Delta^1 \times S^{n+2}
  \xrightarrow{\;\;}
  \Gamma
  \,.
$$
By the truncation assumption (eq:GammaIsNTruncated) this map has a continuous deformation to one that is constant along $S^{n+2}$ on $\phi(1,\ast)$.
\end{proof}

\begin{proposition}
  The comparison morphism (eq:ComparisonMorphismBetweenShapesOfMappingStacks) is an [[isomorphism]] on [[connected components]]:
$$
  \pi_0
  \big(
    \esh \, Map(p/\!\!/G,\,\mathbf{B}\Gamma)
  \big)
  \;\colon\;
  \pi_0
  \,
  \esh
  \,
  Map
  \big(
    \mathbf{B}G
    ,\,
    \mathbf{B}\Gamma
  \big)
  \xrightarrow{\phantom{--} \sim \phantom{--}}
  \pi_0
  \,
  \esh
  \,
  Map
  \big(
    S^{n+2}/G
    ,\,
    \mathbf{B}\Gamma
  \big)
$$
\end{proposition}
\begin{proof}
  It is [[surjective]] by Lem. \ref{ConjugacyClassesOfGroupHomomorphismsSurjectOnPrincipalBundlesOverSphericalSpaceForm}
and [[injective]] by Lemma \ref{OneMorphismsInShapeOfMapsFromSphericalFormToBGammaParallelToOneComingFromShapeOfMapsFromBGToBGamma}.
\end{proof}
