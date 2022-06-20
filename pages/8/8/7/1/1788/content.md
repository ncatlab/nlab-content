

Let 

1. $B \in kHaus \hookrightarrow kTop$ be

   1. a [[compactly generated topological space|compactly generated]] [[Hausdorff space]]

   1. a [[homotopy 1-type]]

      \[
        \label{AssumptionThatBaseIsOneTruncated}
        \underset{b \in B}{\forall}\;\;\; \pi_{n \geq 2}(B,b) \;\simeq\; 0
      \]

1. $(X \xrightarrow{p_X} B) \in kTop_{/B}$ be 

   1. a [[compactly generated topological space]] (i.e. a [[k-space]]) 

   1. in the [[slice category]]  over $B$, via a [[Hurewicz fibration]] 

      \[
        \label{AssumingpXIsFibration}
        p_X \,\in\, hFib
        \,.
      \]

For $b \in B$ we write $X_b$ for the [[fiber]] of $p_X$ over $b$:

\[
  \label{FiberOfTheFibration}
  \array{
    X_b &\xrightarrow{\phantom{----}}& X
    \\
    \big\downarrow 
    &{}_{{}^{(pb)}}& 
    \big\downarrow{}^{\mathrlap{p_X}}
    \\
    \{b\}
    &\underset{\phantom{----}}{\hookrightarrow}&
    X
  }
\]

\begin{example}
  For $n,N \,\in\, \mathbb{N}$, the map of [[configuration spaces of ordered points]] in the [[plane]] 
$$
  X 
    \;=\; 
  \underset{
    \{ 1, \cdots, n+N \}
  }{Conf}
  \big(
    \mathbb{R}^2
  \big)
  \xrightarrow{\;\;\;}
  \underset{
    \{1, \cdots, N\}
  }{Conf}
  \big(
    \mathbb{R}^2
  \big)
  \;=\;
  B
  \,
$$
(which forgets the position of the first $n$ among $n + N$ points)
satisfies the above assumption, by [this Prop.](configuration+space+of+points#ForgettingPointsIsAFibration) and [this Prop.](configuration+space+of+points#CnfSpaceOfPointsInPlaneIsEMSpace). 
\end{example}

\begin{proposition}
  For any [[k-space]] $A \,\in\, kTop$ the [[non-abelian cohomology]]-sets of the [[fibers]] $X_b$ (eq:FiberOfTheFibration) with [[coefficients]] in $A$:
\[
  \label{NonAbelianCohomologySets}
  A^0(X)
    \;\coloneqq\;
  H^0(X;\, A)
    \;\coloneqq\;
  \pi_0
  Map
  \big(
    X_b
    ,\,
    A
  \big)
\]
constitute a [[local system]] over $B$, in that they are the values of a [[functor]] from the [[fundamental groupoid]] of $B$ to [[Sets]].
\end{proposition}
\begin{proof}
  Write $p_B^\ast A \,\in\, kTop_{/B}$ for the [[base change]] of $A$ to the [[slice category|slice]] over $B$, i.e. for the trivial fibration 
\[
  \label{ATrivialFibration}
  p_B^\ast A
  \;\;\;\coloneqq\;\;\;
  B \times A \xrightarrow{\; pr_B \;} B
  \,.
\]
This is clearly a [[Hurewicz fibration]]. Since also $p_X$ is such by assumption (eq:AssumingpXIsFibration), it follows (by [this Prop.](parameterized+homotopy+theory#FiberwiseMappingSpacePreservesHFibrations)) that the [fiberwise mapping space](parameterized+homotopy+theory#FiberwiseMappingSpaces) between the two ([this Def.](parameterized+homotopy+theory#FiberwiseMappingSpace)) is also a [[Hurewicz fibration]], hence its [[fibers]] are [[homotopy fibers]] and as such coincide with the ordinary [[compact-open topology|mapping space]] between the fibers (by [this Prop.](parameterized+homotopy+theory#FiberOfFiberwiseMappingSpace)):
$$
  \array{
    Map
    \big(
      X_b 
      ,\,
      A_b
    \big)
    &
    \xrightarrow{\phantom{--}}
    \;\;\;\;\;
    &
    \phantom{---}
    \mathclap{
    Map
    \big(
      (X,p_X)
      ,\,
      p_B^\ast A
    \big)
    }
    \phantom{---}
    \\
    \big\downarrow
    &{}_{{}^{(pb)}}&
    \big\downarrow{}^{ \mathrlap{\in Fib}}
    \\
    \{b\}
    &\xrightarrow{\phantom{-----}}&
    B
    \mathrlap{\,.}
  }
$$
Hence we may think of this diagram equivalently as representing the [[homotopy fiber product]] of $\{b\} \to B$ with the mapping fibration in the [[classical model structure on topological spaces]]. 

Noticing that 

1. this homotopy fiber product property is [[preserved limit|preserved]] by fiberwise [[0-truncation]] (for instance via [this Prop.](https://ncatlab.org/nlab/show/n-truncated+object+of+an+infinity1-category#nTruncationInToposPreservesFiniteProducts), using that [[classical model structure on topological spaces|$kTop_{Qu}$]] [[presentable (infinity,1)-category|presents]] the [[(infinity,1)-topos]] of [[infinity-groupoids|$\infty$-groupoids]]);

1. the map $\{b\} \to B$ is already fiberwise 0-truncated, by assumption (eq:AssumptionThatBaseIsOneTruncated)

it follows that the fiberwise 0-truncation of the fiberwise mapping space fibration has as [[homotopy fibers]] the [[non-abelian cohomology]]-sets (eq:NonAbelianCohomologySets):

$$
  \array{
    \mathllap{
      H^0(X_b;\, A)
      \;\simeq\;
    }
    \pi_0
    Map
    \big(
      X_b
      ,\,
      A
    \big)
    &
    \xrightarrow{\phantom{--}}
    \;\;\;\;\;\;\;
    &
    \phantom{----}
    \mathclap{
    \pi_{0/B}
    \,
    Map
    \big(
      (X,p_X)
      ,\,
      p_B^\ast A
    \big)
    }
    \phantom{----}
    \\
    \big\downarrow
    &{}_{{}^{(pb)}}&
    \big\downarrow{}^{ \mathrlap{\in Fib} }
    \\
    \{b\}
    &\xrightarrow{\phantom{-----}}&
    B
    \mathrlap{\,.}
  }
$$
Here by [[fibrant replacement]] we may assume without restriction that the right vertical map is again a [[Serre fibration]], as indicated, in which case it is a [[covering space]]-projection whose fibers are the desired cohomology groups. This implies the claim by the *[fundamental theorem of covering space theory](covering+space#FundamentalTheoremOfCoveringSpaces)*.
\end{proof}

