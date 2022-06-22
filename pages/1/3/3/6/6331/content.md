

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A *Gauss-Manin connection* is a canonical [[flat connection]] on [[fiber bundles]] of [[relative cohomology|relative]] [[ordinary cohomology|ordinary]] (but possibly [[twisted cohomology|twisted]]) ([[cohomology groups|co]]-)[[homology groups]], hence a way of transforming (co-)homology classes as a *parameter* varies.

## Details

(...)

## For fiber bundles
 {#ForFiberBundles}

The existence of a flat connection on bundles of fiberwise-chomology groups is easy to understand in the case that the [[fibers]] form a [[locally trivial bundle|locally trivial]] [[fiber bundle]]: In this case the fiberwise cohomology of the local trivialization of this fiber bundle is a local trivialization of the bundle of its fiberwise cohomology groups.

Simple as this may appear, at least in the case of fiberwise [[twisted cohomology]] this case subsumes (for forgetful fibrations of [[configuration spaces of points]] in the plane) the profound example of solutions to the [[Knizhnik-Zamolodchikov equation]], identified as such via the  [hypergeometric integral construction](Knizhnik-Zamolodchikov+equation#BraidRepresentationsViaTwisteddRCohomologyOfConfigurationSpaces) -- this is highlighted as such in [Etingof, Frenkel & Kirillov 1998, §7.5](#EtingofFrenkelKirillov98), reproduced as Example \ref{ExampleOfHypergeometricKZEquations} below.

In the following we give a more abstract/formal ([[model category|model]] [[category theory|category theoretic]]/[[homotopy theory|homotopy theoretic]]) argument for the existence and construction of the Gauss-Manin connection for [[twisted cohomology]] on a class of [[fiber bundles]] which subsume the case that gives the [[KZ-equation]], namely projections of [[configuration spaces of points]] (Ex. \ref{ForgetfulMapBetweenConfigurationSpaces} below).

This following more abstract argument has the advantage that it applies at once to all [[generalized cohomology]]-theories for which [[classifying spaces]] exist ([[Whitehead-generalized cohomology theories]] and more general [[non-abelian cohomology]]-theories, such as unstable [[Cohomotopy]]), and that its structure is readily formulated in general [[(infinity,1)-topos|$(\infty,1)$-toposes]] and in [[homotopy type theory]]. In fact, in that formal language the following construction of the Gauss-Manin connection for twisted cohomology on fibers of a fiber bundle is so simple that it becomes essentially a tautology.


### For non-abelian cohomology
 {#ForNonAbelianCohomology}
 

The following is a (non-standard) general-abstract argument for the existence and construction of the structure of local systems on fiberwise cohomology groups, which applies in the generality of [[Whitehead-generalized cohomology theories]], and in fact of [[non-abelian cohomology|non-abelian cohomology theories]].

The simple idea -- using that all these notions of cohomology have [[classifying spaces]] -- is that the fiberwise 0-truncation of the *[fiberwise mapping space](parameterized+homotopy+theory#FiberwiseMappingSpaces)* to that classifying space provides at once the [[covering space]] which exhibits the local system.

The discussion below assumes that the base of the fibration is a [[homotopy 1-type]], which is the case in examples of interest (e.g. Ex. \ref{ForgetfulMapBetweenConfigurationSpaces} below). The construction in itself still works without this assumption, but then there is some kind of twist in the local system.

\linebreak


Let 

1. $B \in kHaus \hookrightarrow kTop$ be

   1. a [[compactly generated topological space|compactly generated]] [[Hausdorff space]],

   1. [[locally path-connected topological space|locally path-connected]] and [[semi-locally simply-connected topological space|semi-locally simply connected]],

   1. a [[homotopy 1-type]]

      \[
        \label{AssumptionThatBaseIsOneTruncated}
        \underset{b \in B}{\forall}\;\;\; \pi_{n \geq 2}(B,b) \;\simeq\; 0
        \,;
      \]

1. $(X \xrightarrow{p_X} B) \in kTop_{/B}$ be 

   1. a [[compactly generated topological space]] (i.e. a [[k-space]]),

   1. in the [[slice category]]  over $B$, via a [[Hurewicz fibration]] 

      \[
        \label{AssumingpXIsFibration}
        p_X \,\in\, hFib
        \,.
      \]

   1. which is [[fiber bundle|locally trivial]] over a [[numerable cover]] $\big\{ U_j \xhookrightarrow{\;\iota_j\;} B\big\}_{j \in J}$ for some [[typical fiber]] $X_0$:

      \[
        \label{LocalTrivialityOfFibration}
        \underset{j \in J}{\forall}\;\;\;\;
        \iota_j^\ast (X, p_X) \,\simeq\, p_B^\ast X_0
      \]

   1. what has the [[mathematical structure|structure]] of a [[CW-complex]]:

      \[
        \label{FiberIsCWComplex}
        X_0 \,\in\, CWCpl \to kTop
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
    B
  }
\]

\begin{example}\label{ForgetfulMapBetweenConfigurationSpaces}
**(forgetful map between configuration spaces of points)**
\linebreak
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

\begin{proposition}\label{FiberwiseNonAbelianCohomologySetsFormLocalSystem}
**(fiberwise non-abelian cohomology sets form local system)**
\linebreak
  For any [[k-space]] $A \,\in\, kTop$, the [[non-abelian cohomology]]-sets of the [[fibers]] $X_b$ (eq:FiberOfTheFibration) with [[coefficients]] in $A$:
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
constitute a [[local system]] over $B$, in that they arrange into a [[covering space]] over $B$ ([[fundamental theorem of covering spaces|equivalently]], they are the values of a [[functor]] from the [[fundamental groupoid]] of $B$ to [[Sets]]).

Moreover, if $\big\{U_j \xhookrightarrow{\iota_j} B\big\}_{j \in J}$ is an [[open cover]] over which $X \to B$ [[local trivialization|locally trivializes]] with [[typical fiber]] $X_0$, then the covering space of cohomology sets [[local trivialization|locally trivializes]] over the same cover, with [[typical fiber]] $H^0(X_0; A)$.
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
This is clearly a [[Hurewicz fibration]]. Since also $p_X$ is such by assumption (eq:AssumingpXIsFibration), it follows (by [this Prop.](parameterized+homotopy+theory#FiberwiseMappingSpacePreservesHFibrations)) that the [fiberwise mapping space](parameterized+homotopy+theory#FiberwiseMappingSpaces) between the two ([this Def.](parameterized+homotopy+theory#FiberwiseMappingSpace)) is also a [[Hurewicz fibration]], hence its [[fibers]] are [[homotopy fibers]] and as such coincide with the ordinary [[compact-open topology|mapping space]] between the fibers (by [this Example](parameterized+homotopy+theory#FiberOfFiberwiseMappingSpace)):
\[
  \label{HomotopyFiberOfFiberwiseMappingSpace}
  \array{
    Map
    \big(
      X_b 
      ,\,
      A
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
\]
Hence we may think of this diagram equivalently as representing the [[homotopy fiber product]] of $\{b\} \to B$ with the mapping fibration in the [[classical model structure on topological spaces]]. 

Noticing that 

1. this homotopy fiber product property is [[preserved limit|preserved]] by fiberwise [[0-truncation]] (for instance via [this Prop.](https://ncatlab.org/nlab/show/n-truncated+object+of+an+infinity1-category#nTruncationInToposPreservesFiniteProducts), using that [[classical model structure on topological spaces|$kTop_{Qu}$]] [[presentable (infinity,1)-category|presents]] the [[(infinity,1)-topos|$\infty$-topos]] of [[infinity-groupoids|$\infty$-groupoids]]);

1. the map $\{b\} \to B$ is already fiberwise 0-truncated, by assumption (eq:AssumptionThatBaseIsOneTruncated)

it follows that the fiberwise 0-truncation of the fiberwise mapping space fibration has as [[homotopy fibers]] the [[non-abelian cohomology]]-sets (eq:NonAbelianCohomologySets):

$$
  \array{
    \mathllap{
      H^0(X_b;\, A)
      \;=\;
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
Here by [[fibrant replacement]] we may assume that the right vertical map is again a [[Serre fibration]], as indicated, in which case it is a [[covering space]]-projection whose fibers are the desired cohomology groups. 
This proves the first statement. 

The second statement follows by the same argument, after using over any patch $U_j \xhookrightarrow{\iota_j} B$ of the given open cover the following [[natural isomorphism|natural]] identification:
$$
  \begin{array}{ll}
    \iota_j^\ast
    Map
    \big(
      (X, p_X)   
      ,\,
      p_B^\ast A
    \big)
    \\
    \;\simeq\;
    Map
    \big(
      \iota_j^\ast
      (X, p_X)   
      ,\,
      \iota_j^\ast
      p_B^\ast A
    \big)
    &
    \text{by (eq:PullbackOfFiberwiseMappingSpaces)}
    \\
    \;\simeq\;
    Map
    \big(
      p_{U_j}^\ast X_0
      ,\,
      p_{U_j}^\ast A
    \big)
    &
    \text{by (eq:LocalTrivialityOfFibration)}
    \\
    \;\simeq\;
    p_{U_j}^\ast
    Map
    \big(
      X_0
      ,\,
      A
    \big)
    &
    \text{by (eq:PullbackOfFiberwiseMappingSpaces)}
  \end{array}
$$ 
\end{proof}
Here we have used that [[pullback]] is a [[closed functor]] with respect to [[fiberwise mapping spaces]] (by [this Prop.](parameterized+homotopy+theory#PullbackOfFiberwiseMappingSpace)):
\[
  \label{PullbackOfFiberwiseMappingSpaces}
  f^\ast
  Map
  \big(
    (X,p_X)
    ,\,
    (Y,p_Y)
  \big)
  \;\simeq\;
  Map\big( f^\ast(X,p_X),\, f^\ast(Y,p_Y) \big)
  \,.
\]


### For twisted non-abelian cohomology
 {#ForTwistedNonabelianCohomology}

We generalize the [above](#ForNonAbelianCohomology) discussion to [[twisted cohomology|twisted]] [[non-abelian cohomology]] (Def. \ref{TwistedNonAbelianCohomology} below).

The argument is essentially the same as in the previous Prop. \ref{FiberwiseNonAbelianCohomologySetsFormLocalSystem}, only that now:

1. the base spaces starts out being the [[product space]] $B \times B G$ of the previous base space $B$ with the [[classifying space]] $B G$ for the twists, 

1. before passing to homotopy classes of fiberwise maps we form the right [[base change]] $(B \times p_{B G})_\ast$ ([[dependent product]]) along this classifying space. 

To see that the previous argument generalizes to this case one needs to 

1. observe that this right base change is right Quillen (Lem. \ref{RightBaseChangeAlongProjectionIsQuillen} below),

1. use a [[Beck-Chevalley relation]] (eq:BeckChevalleyRelationForProjection) to see that it is compatible with pullback along $\{b\} \to B$.

\linebreak

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
**(twisted non-abelian cohomology, as in [[schreiber:The Character Map in Twisted Non-Abelian Cohomology|FSS20, §2.2]])**
\linebreak
For 

* $G$ a [[discrete group]], 
  
* $A$ a [[G-space|$G$-space]], 

* $\tau_b \,\colon \,X_b \xrightarrow{\;\;} B G$ a map to the [[classifying space]] (eq:BGBeingCWCOmplex), 

the *$\tau_b$-[[twisted cohomology|twisted]] [[non-abelian cohomology]]* of $X_b$ with [[coefficients]] in $A$ is the [[connected components]] of the [[space of sections]] of the [[pullback bundle]] of $A \times_G E G$ along $\tau_b$:
\[
  \label{TwistedGeneralizedCohomologySets}
  \begin{aligned}
  A^\tau(X_b)
  \;\coloneqq\;
  H^\tau(X_b;\, A)
  &
  \;\coloneqq\;
  \pi_0
  \,
  \Gamma_{X_b}
  \big(
    \tau_b^\ast
    (A \times_G E G)
  \big)
  \\
  &
  \;\simeq\;
  \pi_0
  \bigg(
  (p_{B G})_\ast
  Map
  \Big(
    (X_b, \tau_b)
    ,\,
    \big(   
      A \times_G E G
      ,\,
      p_{A \times_G E G}
    \big)
  \Big)
  \bigg)
  \,,
  \end{aligned}
\]
where the [[codomain]] on the right is the [[Borel construction]]  (eq:BorelConstructionAsObjectInSliceOverBG) on $A$.
\end{definition}

\begin{remark}\label{SpaceOfSectionsByRightBaseChangeOfFiberwiseMapping}
To see that $(p_{B G})_\ast Map\big( (-,-),\, (-,-) \big)$ in the last line of (eq:TwistedGeneralizedCohomologySets) is really the same as the [[space of sections]], use the [[Yoneda lemma]] (for $kTop^{op}$) on the following sequence of [[natural isomorphisms]]:
$$
  \begin{array}{ll}
    kTop
    \Big(
      U
      ,\,
      (p_{B G})_\ast
      Map
      \big(
        (X_b, \tau_b)
        ,\,
        (A \times_G E G, p_{A \times_G E G})
      \big)
    \Big)
    \\
    \;\simeq\;
    kTop_{/ B G}
    \Big(
      (p_{B G})^\ast
      U
      ,\,
      Map
      \big(
        (X_b, \tau_b)
        ,\,
        (A \times_G E G, p_{A \times_G E G})
      \big)
    \Big)
    \\
    \;\simeq\; 
    kTop_{/ B G}
    \Big(
      \big(
        (p_{B G})^\ast U
      \big)
      \times
      (X_b, \tau_b)
      ,\,
      (A \times_G E G, p_{A \times_G E G})
    \Big)
    \\
    \;\simeq\; 
    kTop_{/ B G}
    \Big(
      (\tau_b)_!
      (U \times X_b, pr_{X_b})
      ,\,
      (A \times_G E G, p_{A \times_G E G})
    \Big)
    &
    \text{by (eq:APullback)}
    \\
    \;\simeq\; 
    kTop_{/ X_b}
    \Big(
      (U \times X_b, pr_{X_b})
      ,\,
      (\tau_b)^\ast
      (A \times_G E G, p_{A \times_G E G})
    \Big)
    \\
    \;\simeq\; 
    kTop
    \big(
      U \times X_b
      ,\,
      (\tau_b)^\ast (A \times_G E G)
    \big)
    \underset{
      kTop
      \big(
        U \times X_b
        ,\,
        X_b
      \big)
    }{\times}
    \big\{
      pr_{X_b}
    \big\}
    \\
    \;\simeq\; 
    kTop
    \Big(
    U 
    ,\,
    Map
    \big(
      X_b
      ,\,
      (\tau_b)^\ast (A \times_G E G)
    \big)
    \underset{
      Map
      \big(
        X_b
        ,\,
        X_b
      \big)
    }{\times}
    \big\{
      \mathrm{id}_{X_b}
    \big\}
    \Big)
    \\
    \;\simeq\;
    kTop
    \Big(
      U
      ,\,
      \Gamma_X
      \big(
        (\tau_b)^\ast
        ( A \times_G E G )
      \big)
    \Big)
  \end{array}
$$
Here each step is the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) of various [[adjoint functors]], except the marked one which is immediate from this [[pullback]] square:
\[
  \label{APullback}
  \array{
    U \times X_b
    &\overset{pr_{X_b}}{\longrightarrow}&
    X_b
    \\
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow\mathrlap{{}^{\tau_b}}
    \\
    U \times B G
    &\underset{pr_{B G}}{\longrightarrow}&
    B G
    \mathrlap{\,.}
  }
\]
and remembering that left [[base change]] $(\tau_b)_!$ is given simply by post-[[composition]] with $\tau_b$.
\end{remark}

Now we may state and prove the twisted-cohomology generalization of Prop. \ref{FiberwiseNonAbelianCohomologySetsFormLocalSystem}:

\begin{proposition}\label{FiberwiseTwistedNonAbelianCohomologySetsFormLocalSystem}
**(fiberwise twisted non-abelian cohomology sets form local system)**
\linebreak
  With $(X, p_X)$ a [[fiber bundle]] as [above](#ForNonAbelianCohomology), and 
  given a *global twist* on its total space
  $$
    \tau \,\colon\, X \xrightarrow{\;\;} B G
    \,,
  $$
  the $\tau_b$-twisted $A$-cohomology sets 
  (Def. \ref{TwistedNonAbelianCohomology})
of $X_b$,
for any $b \in B$, arrange into a [[covering space]] over $B$, generalizing the un-twisted statement from Prop. \ref{FiberwiseNonAbelianCohomologySetsFormLocalSystem}.
\end{proposition}
\begin{proof}
In the evident generalization of (eq:HomotopyFiberOfFiberwiseMappingSpace), we have the following [[homotopy pullback]] diagram:
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
Now by the [[Beck-Chevalley relation]] 
\[
  \label{BeckChevalleyRelationForProjection}
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
this gives the following pullback diagram:
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

From here we conclude as in the proof of Prop. \ref{FiberwiseNonAbelianCohomologySetsFormLocalSystem} that for all $b \in B$ we have:
$$
  \array{
    \phantom{---}
    \mathclap{
    \mathllap{
      H^{\tau_b}(X_b;\, A)
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
so that the fibration on the right is the covering space which exhibits the claimed local system.
\end{proof}

\begin{example}\label{ExampleOfHypergeometricKZEquations}
**(Hypergeometric Knizhnik-Zamologchikov equations)**
\linebreak
  Let 

1. $p_X \colon X \to B$ be the forgetful map of [[configuration spaces of points]] from Ex. \ref{ForgetfulMapBetweenConfigurationSpaces}

   $$
     Conf_{n + N}(\mathbb{R}^2)
     \xrightarrow{\;\;}
     Conf_{N}(\mathbb{R}^2)
     \,,
   $$

1. $A \,=\, K(\mathbb{C},n)$ the [[Eilenberg-MacLane space]] classifying [[ordinary cohomology|ordinary]] [[complex cohomology]];

1. $G \,\coloneqq\, \mathbb{Z}/k \,\subset\, U(1)$ be a [[cyclic group]], acting by multiplication by [[roots of unity]] on the [[complex numbers]] $\mathbb{C}$ and hence on $K(\mathbb{C},n)$.

Then Prop. \ref{FiberwiseTwistedNonAbelianCohomologySetsFormLocalSystem} constructs the Gauss-Manin connection
claimed in [Etingof, Frenkel & Kirillov 1998, §7.5](#EtingofFrenkelKirillov98).
\end{example}



## Examples

* [[Picard-Fuchs equation]]

## Related concepts

* [[flat connection]]

* [[flat vector bundle]]

* [[local system]]

* [[Knizhnik-Zamolodchikov equation]]

## References

Original articles:

* {#Manin58} [[Yuri Manin]], _Algebraic curves over fields with differentiation_, Izv. Akad. Nauk SSSR Ser. Mat. **22** 6 (1958) 737-756 $[$[mathnet:izv3998](http://mi.mathnet.ru/izv3998), [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=im&paperid=3998&volume=22&year=1958&issue=6&fpage=737&what=fullt&option_lang=eng)$]$ (in Russian)

* [[Nicholas M. Katz]], *On the differential equations satisfied by period matrices*, Publications Mathématiques de l'IHÉS, Tome **35** (1968) 71-106 $[$[numdamPMIHES_1968__35__71_0](http://www.numdam.org/item/PMIHES_1968__35__71_0)$]$

* {#Grothendieck66} [[Alexander Grothendieck]], *On the de Rham cohomology of algebraic varieties*, Publications Mathématiques de l'IHÉS, Tome **29** (1966) 95-103 $[$[numdam:PMIHES_1966__29__95_0](http://www.numdam.org/item/?id=PMIHES_1966__29__95_0)$]$ 

* [[Nicholas M. Katz]], [[Tadao Oda]], *On the differentiation of De Rham cohomology classes with respect to parameters*, J. Math. Kyoto Univ. **8** 2 (1968) 199-213 $[$[doi:10.1215/kjm/1250524135](https://projecteuclid.org/journals/kyoto-journal-of-mathematics/volume-8/issue-2/On-the-differentiation-of-De-Rham-cohomology-classes-with-respect/10.1215/kjm/1250524135.full)$]$

* [[Egbert Brieskorn]], *Die Monodromie der isolierten Singularit&auml;ten von Hyperfl&auml;chen*, Masucripta Math. **2** (1970) 103-161  $[$[doi:10.1007/BF01155695](https://doi.org/10.1007/BF01155695), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/brieskorn7.pdf)$]$

* [[Pierre Deligne]], *Equations différentielles à points singuliers réguliers*, Lecture Notes  Math. **163**, Springer (1970) $[$[publications.ias:355](https://publications.ias.edu/node/355)$]$


Textbook accounts:

* [[Pierre Deligne]], *Equations différentielles à points singuliers réguliers*, Lecture Notes  Math. **163**, Springer (1970) $[$[publications.ias:355](https://publications.ias.edu/node/355)$]$

* {#Kulikov98} [[Valentine S. Kulikov]], Part I of: *Mixed Hodge Structures and Singularities*, Cambridge University Press (1998) $[$[doi:10.1017/CBO9780511758928](https://doi.org/10.1017/CBO9780511758928)$]$

* {#Voisin02} [[Claire Voisin]] (translated by [[Leila Schneps]]), Section 9.2.1 (Def. 9.13) of: _[[Hodge theory and Complex algebraic geometry]] I_, Cambridge Stud. in Adv. Math. __76, 77__, 2002/3 ([doi:10.1017/CBO9780511615344](https://doi.org/10.1017/CBO9780511615344))

* [[Alexandru Dimca]], Theorem 2.5.14 in: *Sheaves in Topology*, Universitext, Springer (2004) $[$[doi:10.1007/978-3-642-18868-8](https://doi.org/10.1007/978-3-642-18868-8)$]$


Lecture notes:

* {#Bloch16} [[Spencer Bloch]], *Gauss-Manin connections* (2016) $[$[pdf](http://www.math.uchicago.edu/~bloch/Beijing_lectures_hypergeometric_161028.pdf), [[Bloch-GaussManinConnections.pdf:file]]$]$

Gauss-Manin connections over [[configuration spaces of points]]:

* [[Daniel C. Cohen]], [[Peter Orlik]], *Gauss-Manin Connections for Arrangements, I Eigenvalues*, Compositio Math. **136** (2003) 299-316 $[$[arXiiv:math/0105063](https://arxiv.org/abs/math/0105063), [doi:10.1023/A:1023262022279](https://doi.org/10.1023/A:1023262022279)$]$

* [[Daniel C. Cohen]], [[Peter Orlik]], *Gauss-Manin connections for arrangements, II Nonresonant weights*, Amer. J. Math. **127** (2005) 569-594 $[$[arXiv:math/0207114](https://arxiv.org/abs/math/0207114), [jstor:40067930](https://www.jstor.org/stable/40067930)$]$

* [[Daniel C. Cohen]], [[Peter Orlik]], *Gauss-Manin connections for arrangements, III Formal connections*, Trans. Amer. Math. Soc. **357** (2005) 3031-3050 $[$[arXiv:math/0307210](https://arxiv.org/abs/math/0307210), [doi:10.1090/S0002-9947-04-03621-9](https://doi.org/10.1090/S0002-9947-04-03621-9)$]$


and review in the context of [hypergeometric solutions](BraidRepresentationsViaTwisteddRCohomologyOfConfigurationSpaces) to the [[Knizhnik-Zamolodchikov equation]]:

* {#EtingofFrenkelKirillov98} [[Pavel Etingof]], [[Igor Frenkel]], [[Alexander Kirillov]], Section 7.5 in: *Lectures on Representation Theory and Knizhnik-Zamolodchikov Equations*, Mathematical surveys and monographs **58**, American Mathematical Society (1998) $[$[ISBN:978-1-4704-1285-2](https://bookstore.ams.org/surv-58), [review pdf](http://www.ams.org/journals/bull/2000-37-02/S0273-0979-00-00853-3/S0273-0979-00-00853-3.pdf)$]$



See also:

* [[eom]], *[Gauss-Manin connection](https://encyclopediaofmath.org/wiki/Gauss-Manin_connection)*

* Wikipedia, *[Gauss-Manin connection](http://en.wikipedia.org/wiki/Gauss%E2%80%93Manin_connection)*

* Allan Yashinski, _Smooth deformations and the Gauss-Manin connection_ ([arxiv/1410.0715](http://arxiv.org/abs/1410.0715))


Discussion in [[cyclic homology]]:

* [[Boris Tsygan]], _On the Gauss-Manin connection in cyclic homology_, Methods Funct. Anal. Topology __13__ (2007), no. 1, 8394.

* [[Ezra Getzler]], _Cartan homotopy formulas and the Gauss/Manin connection in cyclic homology_, [pdf](http://www.math.northwestern.edu/~getzler/Papers/barilan.pdf)


In [[noncommutative geometry]]:

* [[Vasily Dolgushev]], [[Dmitry Tamarkin]], [[Boris Tsygan]], _Noncommutative calculus and the Gauss-Manin connection_ ([arxiv/0902.2202](http://arxiv.org/abs/0902.2202))

[[!redirects Gauss-Manin connections]]

[[!redirects Picard-Fuchs equation]]
