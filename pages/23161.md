


### Powering of $\infty$-toposes over $\infty$-groupoids
  {#PoweringOfInfinityToposesOverInfinityGroupoids}

We discuss how the [[powering]] of [[(infinity,1)-toposes|$\infty$-toposes]] over [[Infinity-Grpd|$Grpd_\infty$]] is given by forming [[mapping stacks]] out of [[locally constant infinity-stacks|locally constant $\infty$-stacks]]. All of the following formulas and their proogfs hold verbatim also for [[Grothendieck toposes]], as they just use general abstract properties.

\linebreak

Let $\mathbf{H}$ be an [[(infinity,1)-topos|$\infty$-topos]] 

* with terminal [[(infinity,1)-geometric morphism|geometric morphism]] denoted


  \[
    \label{TerminalGeometricMorphismAdjunction}
    \mathbf{H}
    \underoverset
      {\underset{\Gamma}{\longrightarrow}}
      {\overset{LConst}{\longleftarrow}}
      {\;\;\;\;\bot\;\;\;\;}
    Grp_\infty
    \,,
  \]

  where the [[inverse image]] constructs [[locally constant infinity-stacks|locally constant $\infty$-stacks]],

* and with its [[internal hom]] ([[mapping stack]]) [[adjoint (infinity,1)-functor|adjunction]] denoted

  \[
    \label{MappingStackAdjunction}
    \mathbf{H}
      \underoverset
        {\underset{Maps(X,-)}{\longrightarrow}}  
        { \overset{ (-) \times X }{\longleftarrow} }
        {\;\;\;\; \bot \;\;\;\;}
    \mathbf{H}
  \]

  for $X \,\in\, \mathbf{H}$. 

  Notice that this construction is also [[(infinity,1)-functor|$\infty$-functorial]] in the first argument: 
$Maps\big( X \xrightarrow{f} Y ,\, A \big)$ is the morphism which under the [[(infinity,1)-Yoneda lemma|$\infty$-Yoneda lemma]] over $\mathbf{H}$ (which is large but locally small, so that the lemma does apply)  corresponds to

$$
  \mathbf{H}
  \big(
    (-)
    ,\,
    Maps(X,A)
  \big)
  \;\simeq\;
  \mathbf{H}
  \big(
    (-) \times X
    ,\,
    A
  \big)
  \xrightarrow{
    \mathbf{H}
    \big(
      (-) \times f
      ,\,
      A
    \big)   
  }
  \mathbf{H}
  \big(
    (-) \times Y
    ,\,
    A
  \big)
  \;\simeq\;
  \mathbf{H}
  \big(
    (-)
    ,\,
    Maps(X,A)
  \big)
  \,.
$$



By definition, for any $S \in Grpd_\infty$ and $X \in \mathbf{H}$ the [[powering]]] is the [[(∞,1)-limit]] over the [[diagram]] constant on $X$

$$
  X^K \,=\, {\lim_\leftarrow}_K X
$$

while the [[tensoring]] is the [[(∞,1)-colimit]] over the diagram constant on $X$

$$
  K \cdot X \,=\, {\lim_{\to}}_K X
  \,.
$$

\begin{remark}
  Under [[Isbell duality]], the powering operations on homotopy types $X$ corresponds to higher order [[Hochschild cohomology]] of suitable algebras of functions on  $X$, as discussed there.
\end{remark}



\begin{proposition}
The *powering* of $\mathbf{H}$ over [[Infinity-Grpd|$Grpd_\infty$]] is given by the [[mapping stack]] out of the [[locally constant infinity-stack|locally constant $\infty$-stacks]]:

$$
  \array{
    Grpd_\infty^{op}
    \times
    \mathbf{H}
    &
    \overset{ LConst^{op} \times \mathrm{id} }{\longrightarrow}
    &
    \mathbf{H}^{op}
    \times 
    \mathbf{H}
    &
    \overset{Maps(-,-)}{\longrightarrow}
    &
    \mathbf{H}
  }
$$
in that this operation has the following properties:

1. For all $X,\,A \,\in\, \mathbf{H}$ and $S \,\in\, Grpd_\infty$ we have a [[natural equivalence]]

   \[
     \mathbf{H}
     \Big(
       X
       ,\,
       Maps
       \big(
         LConst(S)
         ,\,
         A
       \big)
     \Big)
     \;\;
     \simeq
     \;\;
     Grpd_\infty
     \Big(
       S
       ,\,
       \mathbf{H}
       \big(
         X
         ,\,
         A
       \big)
     \Big)
   \]

1. In its first argument the operation 

   1. sends the [[terminal object]] (the [[point]]) to the identity:

      \[
        \label{MappingStackOutOfLocallyConstantPreservesLimitsInFirstArg}
        Maps
        \big(
          LConst(\ast)
          ,\,
          X
        \big)
        \;\;
        \simeq
        \;\;
         X
      \]

   1. sends [[(infinity,1)-colimits|$\infty$-colimits]] to [[(infinity,1)-limits|$\infty$-limits]]:

      \[
        \label{MappingStackOutOfLConstStacksPreservesColimitInFirstArgument}
        Maps
        \Big(
          \underset{
            \longrightarrow
          }{\lim}
          \,
          LConst\big(S_\bullet\big)
          ,\,
          X
        \Big)
        \;\;
        \simeq
        \;\;
        \underset{
          \longleftarrow
        }{\lim}
        \,
        Maps
        \Big(
          LConst\big(S_\bullet\big)
          ,\,
          X
        \Big)
        \,,
      \]

   where all [[equivalence in an (infinity,1)-category|equivalences]] shown are [[natural equivalence|natural]].

\end{proposition}



\begin{proof}

For the first statement to be proven, consider the following sequence of [[natural equivalences]]:
$$
  \begin{array}{lll}
     \mathbf{H}
     \Big(
       X
       ,\,
       Maps
       \big(
         LConst(S)
         ,\,
         A
       \big)
     \Big)
     &
     \;\simeq\;   
     \mathbf{H}
     \big(
       X 
       \times
       LConst(S)
       ,\,
       A
     \big)
     &
     \text{(eq:MappingStackAdjunction)}
     \\
     & \;\simeq\;
     \mathbf{H}
     \Big(
       LConst(S)
       ,\,
       Maps
       \big(
         X
         ,\,
         A
       \big)
     \Big)
     &
     \text{(eq:MappingStackAdjunction)}
     \\
     & \;\simeq\;
     Grpd_\infty
     \Big(
       S
       ,\,
       \Gamma
       \,
       Maps
       \big(
         X
         ,\,
         A
       \big)
     \Big)
     &
     \text{ (eq:TerminalGeometricMorphismAdjunction) }
     \\
     & \;\simeq\;
     Grpd_\infty
     \bigg(
       S
       ,\,
       \mathbf{H}
       \Big(
         \ast_{\mathbf{H}}
         ,\,
         Maps
         \big(
           X
           ,\,
           A
         \big)
       \Big)
     \bigg)
     &
     \text{by}\;\text{<a href="https://ncatlab.org/nlab/show/terminal+geometric+morphism#DirectImageOfTerminalGeometricMoprhismIsHomOutOfTerminalObject">this Prop.</a>}
     \\
     & \;\simeq\;
     Grpd_\infty
     \Big(
       S
       ,\,
       \mathbf{H}
       \big(
         \ast_{\mathbf{H}}
         \times
         X
         ,\,
         A
       \big)
     \Big)
     &
     \text{(eq:MappingStackAdjunction)}
     \\
     & \;\simeq\;
     Grpd_\infty
     \Big(
       S
       ,\,
       \mathbf{H}
       \big(
         X
         ,\,
         A
       \big)
     \Big)
  \end{array}
$$

For the second statement, recall that
[[hom-functors preserve limits]] in that there are [[natural equivalences|natural]] [[equivalences in an (infinity,1)-category|equivalences]] of the form

\[
  \label{HomFunctorPreservesLimits}
  \mathbf{H}
  \Big(
    \underset{\underset{i}{\longrightarrow}}{\lim}
    \,,
    X_i
    ,\,
    \underset{\underset{j}{\longleftarrow}}{\lim}
    \,,
    A_j
  \Big)
  \;\;
  \simeq
  \;\;
  \underset{\underset{i}{\longleftarrow}}{\lim}
  \,
  \underset{\underset{j}{\longleftarrow}}{\lim}
  \,
  \mathbf{H}
  \Big(
    X_i
    ,\,
    A_j
  \Big)
  \,,
\]


and that $\infty$-toposes have [[universal colimits]], in particular that the [[product]] operation is a [[left adjoint]] (eq:MappingStackAdjunction) and [[left adjoints preserve colimits|hence preserves colimits]]:

\[
  \label{ProductsPreserveColimits}
  (-)
  \,\times\,
  \underset{{\longrightarrow}}{\lim} \, S_\bullet
  \;\;
  \simeq
  \;\;
  \underset{{\longrightarrow}}{\lim} \, 
  \big(
    (-)
    \,\times\,
    S_\bullet
  \big)
  \,.
\]

With this, we get the following sequences of [[natural equivalences]]:

$$
  \begin{array}{lll}
    &
    \mathbf{H}
    \bigg(
      (-)
      ,\,
      Maps
      \Big(
        \underset{\longrightarrow}{\lim}
        \,
        LConst(S_\bullet)
        ,\,
        X
      \Big)
    \bigg)
    \\
    & \;\simeq\;
    \mathbf{H}
    \Big(
      (-)
      \times
      \underset{\longrightarrow}{\lim}
      \,
      LConst(S_\bullet)
      ,\,
      X
    \Big)
    &
    \text{ (eq:MappingStackAdjunction) }
    \\
    & \;\simeq\;
    \mathbf{H}
    \Big(
      \underset{\longrightarrow}{\lim}
      \big(
        (-)
        \times
        LConst(S_\bullet)
      \big)
      ,\,
      X
    \Big)
    &
    \text{ (eq:ProductsPreserveColimits) }
    \\
    & \;\simeq\;
    \underset{\longleftarrow}{\lim}
    \,
    \mathbf{H}
    \big(
      (-)
      \times
      LConst(S_\bullet)
      ,\,
      X
    \big)
    & 
    \text{ (eq:HomFunctorPreservesLimits) }
    \\
    & \;\simeq\;
    \underset{\longleftarrow}{\lim}
    \,
    \mathbf{H}
    \Big(
      (-)
      ,\,
      Maps
      \big(
        LConst(S_\bullet)
        ,\,
        X
      \big)
    \Big)
    &
    \text{ (eq:MappingStackAdjunction) }
    \\
    & \;\simeq\;
    \mathbf{H}
    \Big(
      (-)
      ,\,
      \underset{\longleftarrow}{\lim}
      \,
      Maps
      \big(
        LConst(S_\bullet)
        ,\,
        X
      \big)
    \Big)
    &
    \text{ (eq:HomFunctorPreservesLimits) }
    \,.
  \end{array}
$$
This implies (eq:MappingStackOutOfLConstStacksPreservesColimitInFirstArgument) by the [[(infinity,1)-Yoneda lemma|$\infty$-Yoneda lemma]] over $\mathbf{H}$ (which is large but locally small, so that the lemma does apply). 

Finally (eq:MappingStackOutOfLocallyConstantPreservesLimitsInFirstArg) is immediate from the fact that $LConst$ preserves the terminal object, by definition:
$$
    Maps
    \big(
      LConst(\ast)
      ,\,
      X
    \big)
    \;\simeq\;
    Maps
    \big(
      \ast_{\mathbf{H}}
      ,\,
      X
    \big)
    \;\simeq\;
    X
    \,.
$$
\end{proof}



