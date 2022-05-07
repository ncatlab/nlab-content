
For $V \simeq \mathbb{R}^n$ a [[real vector space]] of [[dimension]] $n$, an _orientation_ of $V$ is a choice of [[connected component]] of the [[complement]] of [[zero]] in its [[determinant line]]:

\[
  \label{OrientationOfARealVectorSpace}
  or_V
  \;\in\;
  \pi_0
  \big(
    \wedge^{dim(V)} V^\ast
    \setminus
    \{0\}
  \big)
  \,.
\]


For $X$ a [[differentiable manifold]] of [[dimension]] $n$, an _[[orientation]]_ of $X^n$ is smooth family of choices of orientations (eq:OrientationOfARealVectorSpace) for each [[cotangent space]] $T^\ast_x X^n$, $x \in X$, hence a choice of [[connected component]] of the [[complement]] of the [[zero-section]] in the [[space of smooth sections]] of the [[canonical line bundle]]:

$$
  or_X
  \;\in\;
  \pi_0
  \Big(
    \Gamma
    \big(
      \wedge_X^{dim(X)}
      T^\ast X
    \big)
    \setminus
    \{0_X\}
  \Big)
  \,.
$$

The representative [[smooth sections]] here are _[[volume forms]]_ on $X$.

If any such exist at all, $X$ is [[orientable]]. We now assume that this is the case.

If $X$ is moreover a [[closed manifold|closed]] then there are normalized such volume forms, in that their image, under the [[de Rham isomorphism]], in [[real cohomology]] is in the image of a generator of the [[integral cohomology]] of $X$:

\begin{xymatrix@C=16pt}
    &&
    H^n\big(X;\, \mathbb{Z} \big)
    \ar[d]
    \\
    \Gamma
    \big(
      \wedge_X^{\mathrm{dim}(X)}
      T^\ast X
    \big)  
    \ar[r]
    &
    H^n_{dR}(X)  
    \ar@{=}[r]
    &
    H^n_{dR}(X)      
\end{xymatrix}



