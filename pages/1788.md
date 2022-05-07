


\begin{proposition}
For $n \in \mathbb{N}_+$ and
for $A \,\in\, Ab$ the [[integers]] or the [[circle group]],
the following [[composition|composite]] of is a [[simplicial weak equivalence]]
$$
  \begin{aligned}
    \big[
      S,
      \,
      B^n A
    \big]_\bullet   
    & \;=\;
    \big[
      S, 
      \,
      frgt \circ DK(A[n])
    \big]_\bullet
    \\
    &
    \;\simeq\;   
    sSet
    \big(
      S \times \Delta[\bullet],
      \,
      frgt \circ DK(A[n])
    \big)
    \\
    & \;\simeq\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(S \times \Delta[\bullet]),
      \,
      A[n]
    \big)    
    \\
    & \;\xrightarrow{EZ_S}\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(S) 
      \,\otimes\,
      N \circ \mathbb{Z}(\Delta[\bullet]),
      \,
      A[n]
    \big)    
    \\
    & \;\simeq\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(\Delta[\bullet]),
      \,
      [
        N \circ \mathbb{Z}(S),
        \,
        A[n]
      ]
    \big)    
    \\
    & \;\simeq\;
    \Big(
    frgt \circ DK
    \big(
      [
        \underset{
          \mathbb{Z} \oplus \mathbb{Z}[1]
        }{
        \underbrace{
          N \circ \mathbb{Z}(S)
        }
        },
        \,
        A[n]
      ]
    \big)
    \Big)_\bullet
    \\
    & \;\simeq\;
    \Big(
    frgt \circ DK
    \big(
      A[n] \oplus A[n-1]
    \big)
    \Big)_\bullet
    \\
    & 
    B^n A \times B^{n-1} A
  \end{aligned}
$$

\end{proposition}
Here all [[isomorphisms]] are [hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism) of the [above](#HomotopyCategories) [[adjoint functor|adjunctions]], the step denoted $EZ_S$ is pre-composition with the [[Eilenberg-Zilber map]], and under the brace we are using Prop. \ref{NormalizedChainComplexOfMinimalSimplicialCircle}.

\begin{proof}
  By the fact that the [[Eilenberg-Zilber map]] has a [[left inverse]] given by the [[Alexander-Whitney map]] $AW$ (see at *[[Eilenberg-Zilber/Alexander-Whitney deformation retraction]]*, the analogous composite with $AW_S$ instead of $EZ_S$ yields a left inverse morphism, which hence [[retraction|retracts]] the [[homotopy groups]] of $B^n A \times B^{n-1}A$ onto those of $\big[S, B^n A \big]$. 

But by [this Prop.](https://ncatlab.org/nlab/show/free+loop+space of classifying space#FreeLoopSpaceOfClassifyingSpaceOfSimplicialAbelianGroup) the latter is a product of [[Eilenberg-MacLane spaces]]
\[
  \big[
    S,
    \,
    B^n A
  \big]
  \;\simeq\;
  B^n A \times B^{n-1} A
  \;\;\;
  \in
  \;
  Ho(sSet)
  \,,
\]
hence with homotopy group $A$ in degrees $n$ and $n -1 $. By assumption on $A$ the only retractions of $A$ onto $A$ is the identity, so that $EZ_S$ must induces the identity morphism of homotopy groups. 
\end{proof}



$$
  \mathbb{Z}
  \colon
  sSet
  \rightleftarrows
  sAb
  \colon
  frgt
$$

$$
  N
  \colon
  sAb
  \rightleftarrows
  Ch_+
  \colon
  DK
$$

\linebreak

$$
  \begin{aligned}
    \big[
      S, 
      \,
      frgt \circ DK(V)
    \big]_\bullet
    &
    \;\simeq\;   
    sSet
    \big(
      S \times \Delta[\bullet],
      \,
      frgt \circ DK(V)
    \big)
    \\
    & \;\simeq\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(S \times \Delta[\bullet]),
      \,
      V
    \big)    
    \\
    & \;\xrightarrow{EZ_S}\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(S) 
      \,\otimes\,
      N \circ \mathbb{Z}(\Delta[\bullet]),
      \,
      V
    \big)    
    \\
    & \;\simeq\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(\Delta[\bullet]),
      \,
      [
        N \circ \mathbb{Z}(S),
        \,
        V
      ]
    \big)    
    \\
    & \;\simeq\;
    \Big(
    frgt \circ DK
    \big(
      [
        N \circ \mathbb{Z}(S),
        \,
        V
      ]
    \big)
    \Big)_\bullet
  \end{aligned}
$$


$$
  \begin{aligned}
    \Big(
      frgt \circ DK
      \big(
        [
          N \circ \mathbb{Z}(S),
          \,
          V
        ]
      \big)
    \Big)_\bullet
    & \;\simeq\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(\Delta[\bullet]),
      \,
      [
        N \circ \mathbb{Z}(S),
        \,
        V
      ]
    \big)    
    \\
    & \;\simeq\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(S) 
      \,\otimes\,
      N \circ \mathbb{Z}(\Delta[\bullet]),
      \,
      V
    \big)    
    \\
    & \xrightarrow{AW_S}
    Ch_+
    \big(
      N \circ \mathbb{Z}(S \times \Delta[\bullet]),
      \,
      V
    \big)    
    \\  
    & \;\simeq\;
    sSet
    \big(
      S \times \Delta[\bullet],
      \,
      frgt \circ DK(V)
    \big)
    \\
    & \;\simeq\;
    \big[
      S, 
      \,
      frgt \circ DK(V)
    \big]_\bullet
  \end{aligned}
$$

$$
    \big[
      S, 
      \,
      frgt \circ DK(V)
    \big]_\bullet
    \xrightarrow{\;EZ_S\;}
      \Big(
      frgt \circ DK
      \big(
        [
          N \circ \mathbb{Z}(S),
          \,
          V
        ]
      \big)
    \Big)_\bullet
    \xrightarrow{\;AW_S\;}
    \big[
      S, 
      \,
      frgt \circ DK(V)
    \big]_\bullet
$$



