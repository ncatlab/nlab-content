
For $G$ a [[discrete group]], we write $B G \,\coloneqq\, \vert N (G \rightrightarrows \ast)\vert$ for the [[topological realization]] of the [[nerve]] of the [[delooping groupoid]] of $G$, hence for the usual [[classifying space]] (which, by discreteness of $G$, is an [[Eilenberg-MacLane space]] $K(G,1)$) in its usual realization as a [[CW-complex]]:
\[
  \label{BGBeingCWCOmplex}
  B G \,\in\, CWCpx \hookrightarrow kTop^{cof}
  \,.
\] 

\begin{lemma}
  For $B \in kTop$, the right [[base change]]
  $$
    kTop_{B \times B G}
     \underoverset
       {
         \underset{ (pr_B)^\ast }{\longrightarrow}
       }
       {
         \overset{ (pr_B)^\ast }{\longleftarrow}
       }
       {\bot_{{}_{Qu}}}
    kTop_{B}
  $$
  is a [[Quillen adjunction]] between the respective [[slice model categories]] of the [[classical model structure on topological spaces]].
\end{lemma}
\begin{proof}
  Since $pr_B \,\colon\, B \times B G \to B$ is just [[projection]] out of a [[Cartesian product]], the [[pullback]] $(pr_B)^\ast$ acts by forming the [[product topological space]] with the space $B G$. But since $B G$ is [[cofibrant object|cofibrant]] (eq:BGBeingCWCOmplex) this operation preserves [[cofibrations]] and [[acyclic cofibrations]] of $kTop_{Qu}$ (by [this Prop.](classical+model+structure+on +topological spaces#HomProductAdjunctionForCofibrantObjectInTopCGIsQuillen)) and hence also those of its [[slice model structure]].
\end{proof}

\begin{definition}
  For $G$ a [[discrete group]] and $A$ a [[G-space|$G$-space]], and $\tau_b \,\colon \,X_b \xrightarrow{\;\;} B G$ a map, the $\tau$-[[twisted cohomology|twisted]] [[non-abelian cohomology]] of $X_b$ with [[coefficients]] in $A$ is
$$
  A^\tau(X_b)
  \;\coloneqq\;
  H^\tau(X_b;\, A)
  \;\coloneqq\;
  \pi_0
  (p_{B G})_\ast
  Map
  \Big(
    (X_b, \tau_b)
    ,\,
    p_{B}^\ast
    \big(   
      A \times_G E G
      ,\,
      p_{A \times_G E G}
    \big)
  \Big)
  \,,
$$
where the [[codomain]] on the right is the [[Borel construction]] of the $G$-[[group action|action]] on $A$.
\end{definition}

\begin{proposition}
  Given a global twist
  $$
    \tau \,\colon\, X \xrightarrow{\;\;} B G
    \,,
  $$
  the $\tau_b$-twisted $A$-cohomology sets of $X_b$,
as $b \in B$, arrange into a covering space of $B$.
\end{proposition}
\begin{proof}
  now we need that $(p_{B G})_\ast$ is right Quillen... 
\end{proof}


$$
  \begin{aligned}
    kTop_{/B'}
    \Big(
      (U,p_U)
      ,\,
      f^\ast 
      Map
      \big(
        (X,p_X)
        ,\,
        (A,p_A)
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \Big(
      f_! (U,p_U)
      ,\,
      Map
      \big(
        (X,p_X)
        ,\,
        (A,p_A)
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \Big(
      (U,f \circ p_U)
      ,\,
      Map
      \big(
        (X,p_X)
        ,\,
        (A,p_A)
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \big(
      (U,f \circ p_U)
      \times
      (X, p_X)
      ,\,
      (A,p_A)
    \big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \Big(
      f_!
      \big(
        (U, p_U)
        \times
        f^\ast (X, p_X)
      \big)
      ,\,
      (A,p_A)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B'}
    \Big(
        (U, p_U)
        \times
        f^\ast (X, p_X)
      ,\,
      f^\ast
      (A,p_A)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B'}
    \Big(
      (U, p_U)
      ,\,
      Map
      \big(
        f^\ast (X, p_X)
        ,\,
        f^\ast (A,p_A)
      \big)
    \Big)
  \end{aligned}
$$

\linebreak

$$
  \begin{aligned}
    kTop_{/B}
    \Big(
      (U, p_U)
      ,\,
      \Map
      \big(
        p_B^\ast X_0
        ,\,
        p_B^\ast A_0
      \big)
    \Big)
    &
    \;\simeq\;
    kTop_{/B}
    \big(
      (U, p_U) \times (B \times X_0, pr_{B})
      ,\,
      p_B^\ast A_0
    \big)
    \\
    & 
    \;\simeq\;
    kTop_{/B}
    \big(
      (U \times X_0, p_U \circ pr_U)
      ,\,
      p_B^\ast A_0
    \big)
    \\
    &
    \;\simeq\;
    kTop
    \Big(
      U \times X_0
      ,\,
      A_0
    \big)
    \\
    &
    \;\simeq\;
    kTop
    \Big(
      U 
      ,\,
      Map
      \big(
        X_0
        ,\,
        A_0
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop
    \Big(
      (p_B)_!
      (U,p_U)
      ,\,
      Map
      \big(
        X_0
        ,\,
        A_0
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \Big(
      (U,p_U)
      ,\,
      p_B^\ast
      Map
      \big(
        X_0
        ,\,
        A_0
      \big)
    \Big)
  \end{aligned}
$$

...