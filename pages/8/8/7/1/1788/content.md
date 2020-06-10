
+-- {: .num_prop #HodgeStarFollowedByHodgeStar}  
###### Proposition
**([[homotopy colimit]] over a [[representable functor]] is [[n-truncated object in an (∞,1)-category|contractible]])**

Let $\mathcal{C}$ be a [[small (∞,1)-category]] and consider an [[∞Groupoids|∞-groupoid]]-valued [[(∞,1)-functor]] $F \colon \mathcal{C} \to Groupoids_\infty$ which is representable, i.e. in the image of the [[(∞,1)-Yoneda embedding]] $F \simeq y C$: 

$$
  \array{
    \mathcal{C}
    &
    \overset{
      \phantom{AA}
      y
      \phantom{AA}
    }{\longrightarrow}
    &
    Func
    \big(
      \mathcal{C}^{op},
      Groupoids_\infty
    \big)
    \\
    C &\mapsto&
    y C
    \mathrlap{
      \coloneqq
       \mathcal{C}(-,C)
    }
  }
$$

Then the [[(∞,1)-colimit]] over this [[(∞,1)-functor]] is contractible, i.e. is the point, the [[terminal object in an (∞,1)-category|terminal object]] in [[∞Groupoids]]:

$$
  \underset{
    \underset{\mathcal{C}}{\longrightarrow}
  }{\lim}
   (y C)
   \;\simeq\;
   \ast
$$

=--

+-- {: .proof}
###### Proof

The terminal $\infty$-groupoid $\ast$ is characterized by the fact that for each $S \in Groupoids_\infty$ we have $Groupoids_\infty(\ast, S) \simeq S$.
Therefore it is suffucicient to show that $\underset{\longrightarrow}{\lim}\big(y C\big)$ has the same property:


$$
  \begin{aligned}
  Groupoids_\infty
  \left(
    \underset{\longrightarrow}{\lim}
    \big(
      y C
    \big)
    ,
    S
  \right)
  & \simeq\;
  Func(
    \mathcal{C}^{op}
    ,\,
    Groupoids_\infty
  )
  \left(
    y C
    ,
    const S
  \right)
  \\
  & \simeq\;
  (const S)(C)
  \\
  & \simeq\;
  S
  \end{aligned}
$$

Here the first step is the [[(∞,1)-adjunction]]

$$
  Func
  \big(
    \mathcal{C}^{op},
    Groupoids_\infty
  \big)
  \underoverset
    {
      \underset{const}{\longleftarrow}
    }
    {
      \overset{ \underset{\longrightarrow}{\lim} }{\longrightarrow}
    }
    {\phantom{AA}\bot\phantom{AA}}
  \Groupoids_\infty
$$

and the second step is the [[(∞,1)-Yoneda lemma]]

=--

\linebreak

\linebreak

\linebreak

\linebreak

\linebreak


\linebreak

\linebreak

\linebreak

\linebreak

\linebreak


$$
  \array{
     \mathcal{C}(D,C) && 
       \overset{
         (D \overset{f}{\to}C)^\ast
       }{\longleftarrow}
     && \mathcal{C}(C,C)
     \\
     & \searrow && \swarrow
     \\
     &&
     \{C \overset{id}{\to}C\}
  }
$$

