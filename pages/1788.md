
For $G$ a [[discrete group]], we write $B G \,\coloneqq\, \vert N (G \rightrightarrows \ast)\vert$ for the [[topological realization]] of the [[nerve]] of the [[delooping groupoid]] of $G$, hence for the usual [[classifying space]] (which, by discreteness of $G$, is an [[Eilenberg-MacLane space]] $K(G,1)$) in its usual realization as a [[CW-complex]]:
\[
  \label{BGBeingCWCOmplex}
  B G \,\in\, CWCpx \hookrightarrow kTop^{cof}
  \,.
\] 

For $A \,\in\, G Act(kTop)$ a [[topological G-space|topological $G$-space]] (a space equipped with a [[continuous map]] $G$-[[group action|action]]), its *[[Borel construction]]* is -- regarded as the $A$-[[fiber bundle]] [[associated bundle|associated]] to the [[universal principal bundle|universal $G$-principal bundle]] -- an object in the [[slice category]] over the [[classifying space]] $B G$ (eq:BGBeingCWCOmplex)

\[
  \label{BorelConstructionAsObjectInSliceOverBG}
  \big(
    A \times_G E G
    ,\,
    p_{A \times_G E G }
  \big)
  \;\;
  \in
  \;
  kTop_{/B G}
\]

\begin{lemma}\label{RightBaseChangeAlongProjectionIsQuillen}
  For $B \in kTop$, the right [[base change]] along the [[projection]] $pr_B \,\colon\, B \times B G \to B $
  $$
    kTop_{B \times B G}
     \underoverset
       {
         \underset{ (pr_B)^\ast }{\longrightarrow}
       }
       {
         \overset{ (pr_B)^\ast }{\longleftarrow}
       }
       {\bot_{{}_{\mathrlap{Qu}}}}
    kTop_{B}
  $$
  is a [[Quillen adjunction]] between the respective [[slice model categories]] of the [[classical model structure on topological spaces]].
\end{lemma}
\begin{proof}
  Since $pr_B \,\colon\, B \times B G \to B$ is just [[projection]] out of a [[Cartesian product]], the [[pullback]] $(pr_B)^\ast$ acts by forming the [[product topological space]] with the space $B G$. But since $B G$ is [[cofibrant object|cofibrant]] (eq:BGBeingCWCOmplex) this operation preserves [[cofibrations]] and [[acyclic cofibrations]] of $kTop_{Qu}$ (by [this Prop.](classical+model+structure+on+topological+spaces#HomProductAdjunctionForCofibrantObjectInTopCGIsQuillen)) and hence also those of its [[slice model structure]].
\end{proof}

\begin{definition}\label{TwistedNonAbelianCohomology}
**(twisted non-abelian cohomology)**
\linebreak
For 

* $G$ a [[discrete group]], 
  
* $A$ a [[G-space|$G$-space]], 

* $\tau_b \,\colon \,X_b \xrightarrow{\;\;} B G$ a map to the [[classifying space]] (eq:BGBeingCWCOmplex), 

the *$\tau$-[[twisted cohomology|twisted]] [[non-abelian cohomology]]* of $X_b$ with [[coefficients]] in $A$ is
$$
  A^\tau(X_b)
  \;\coloneqq\;
  H^\tau(X_b;\, A)
  \;\coloneqq\;
  \pi_0
  \bigg(
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
  \bigg)
  \,,
$$
where the [[codomain]] on the right is the [[Borel construction]]  (eq:BorelConstructionAsObjectInSliceOverBG) on $A$.
\end{definition}

\begin{proposition}\label{FiberwiseTwistedNonAbelianCohomologySetsFormLocalSystem}
**(fiberwise twisted non-abelian cohomology sets form local system)**
\linebreak
  With $(X, p_X)$ a [[fiber bundle]] as above, and 
  given a *global twist* on its total space
  $$
    \tau \,\colon\, X \xrightarrow{\;\;} B G
    \,,
  $$
  the $\tau_b$-twisted $A$-cohomology sets 
  (Def. \ref{TwistedNonAbelianCohomology})
of $X_b$,
as $b \in B$, arrange into a covering space over $B$, generalizing the un-twisted statement from Prop. \ref{FiberwiseNonAbelianCohomologySetsFormLocalSystem}.
\end{proposition}
\begin{proof}
start with

$$
  \array{
    \phantom{---}
    \mathclap{
    Map
    \Big(
      \big(
        (X_b, \tau_b)
      \big)
      ,\,
      \big(
        A \times_G E G, p_{A \times_G E G}
      \big)
    \Big)
    }
    \phantom{-------}
    &
    \!\!\!\!\!\!\!\!\!\!\!\!
    \xrightarrow{\phantom{---}}
    \;\;\;\;\;\;\;\;\;\;
    &
    \phantom{-----}
    \mathclap{
    Map
    \Big(
      \big(
        X, (p_X, \tau)
      \big)
      ,\,
      p_B^\ast
      \big(
        A \times_G E G, p_{A \times_G E G}
      \big)
    \Big)
    }
    \phantom{-----}
    \\
    \big\downarrow
    &{}_{{}^{(pb)}}&
    \big\downarrow{}^{ \mathrlap{\in Fib}}
    \\
    \{b\} \times B G
    &\xrightarrow{\phantom{-----}}&
    B \times B G
    \mathrlap{\,.}
  }
$$

By the [[Beck-Chevalley relation]] 
\[
  \big(
    b_{(-)}
  \big)^\ast
    \circ
  \big(
    B
    \times
    p_{B G}
  \big)_\ast
  \;\;
  \simeq
  \;\;
  \big(
    p_{B G}
  \big)_\ast
  \circ
  \big(
    b_{(-)} \times B G
  \big)^\ast

\]
\begin{tikzcd}[
    column sep={between origins, 36pt}
  ]
    & 
    B G
    \ar[
      dr,
      "{
        b_{(-)}
        \times
        B G
      }"
    ]
    \ar[
      dl,
      "{
        \mathrm{p}_{B G}
      }"{swap}
    ]
    \\
    \ast
    \ar[
      dr,
      "{
        b_{(-)}
      }"{swap}
    ]
    &&
    B
    \times
    B G
    \ar[
      dl,
      "{
        B
        \times
        p_{B G}
      }"
    ]
    \\
    &
    B
  \end{tikzcd}
this gives

$$
  \array{
    \phantom{---}
    \mathclap{
    (p_{B G})_\ast
    Map
    \Big(
      \big(
        (X_b, \tau_b)
      \big)
      ,\,
      \big(
        A \times_G E G, p_{A \times_G E G}
      \big)
    \Big)
    }
    \phantom{---------}
    &
    \!\!\!\!\!\!\!\!\!\!\!\!
    \xrightarrow{\phantom{---}}
    \;\;\;\;\;\;\;\;\;\;
    &
    \phantom{--------}
    \mathclap{
    (B \times p_{B G})_\ast
    Map
    \Big(
      \big(
        X, (p_X, \tau)
      \big)
      ,\,
      p_B^\ast
      \big(
        A \times_G E G, p_{A \times_G E G}
      \big)
    \Big)
    }
    \phantom{-----}
    \\
    \big\downarrow
    &{}_{{}^{(pb)}}&
    \big\downarrow{}^{ \mathrlap{\in Fib}}
    \\
    \{b\}
    &\xrightarrow{\phantom{----------}}&
    B 
    \mathrlap{\,,}
  }
$$
where the vertical map on the right is still a fibration, by Lem. \ref{RightBaseChangeAlongProjectionIsQuillen}.

Therefore we conclude as in the proof of ... that 

$$
  \array{
    \phantom{---}
    \mathclap{
    \mathllap{
      H^\tau(X_b;\, A)
      \,=\,
    }
    \pi_0
    (p_{B G})_\ast
    Map
    \Big(
      \big(
        (X_b, \tau_b)
      \big)
      ,\,
      \big(
        A \times_G E G, p_{A \times_G E G}
      \big)
    \Big)
    }
    \phantom{---------}
    &
    \!\!\!\!\!\!\!\!\!\!\!\!
    \xrightarrow{\phantom{---}}
    \;\;\;\;\;\;\;\;\;\;
    &
    \phantom{---------}
    \mathclap{
    \pi_{0/B}
    (B \times p_{B G})_\ast
    Map
    \Big(
      \big(
        X, (p_X, \tau)
      \big)
      ,\,
      p_B^\ast
      \big(
        A \times_G E G, p_{A \times_G E G}
      \big)
    \Big)
    }
    \phantom{-----}
    \\
    \big\downarrow
    &{}_{{}^{(pb)}}&
    \big\downarrow{}^{ \mathrlap{\in Fib}}
    \\
    \{b\}
    &\xrightarrow{\phantom{----------}}&
    B 
    \mathrlap{\,,}
  }
$$


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