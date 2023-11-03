
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The **[[Jon Beck|Beck]]--[[Claude Chevalley|Chevalley]] condition**, also sometimes called just the *Beck condition* or the *Chevalley condition*, is a "commutation of [[adjoint functor|adjoint]]s" property that holds in many "[[base change|change of base]]" situations.

## Motivation

The Beck-Chevalley condition may be understood as a natural compatibility  condition for

**[(1)](#MotivationFromIntegralTransforms)** [[integral transforms]] in [[geometry]]

**[(2)](#MotivationFromLogicAndTypeTheory)** [[quantifiers]] in [[formal logic]]/[[type theory]]

### From integral transforms
 {#MotivationFromIntegralTransforms}

From the point of view of [[geometry]], in contexts such as of [[integral transforms]] one considers [[correspondences]] between [[spaces]] $A$, $B$ given by [[spans]] of [[maps]] between them:

\begin{tikzcd}[sep=20]
  & 
  X
  \ar[dl, "f"{swap}]
  \ar[dr, "g"]
  \\
  A && B
\end{tikzcd}


Via [[composition]] of such correspondences by [[fiber product]] of adjacent legs, they form the [[1-morphisms]] in a [[2-category]] *[[Span]]*.

Assuming some [[base change]] [[adjoint pair]] $f^\ast \vdash f_\ast$, thought of as

* *push-forward* $f_\ast \,\colon\, \mathcal{D}(X) \longrightarrow \mathcal{D}(A)$

and

* *pull-back* $f^\ast \,\colon\, \mathcal{D}(A) \longrightarrow \mathcal{D}(X)$

is [[functor|functorially]] associated with [[maps]] $f$ (i.e. such that there are [[natural isomorphisms]] $(f_2 f_1)_\ast \,\simeq\, (f_2)_\ast (f_1)_\ast$ and dually), the [[integral transform]] encoded by any span as above is the "pull-push" operation given by $g_* f^*$. 

Now the Beck-Chevalley condition (on such assignment of [[base change]] adjoints to maps) essentially says that this pull-push construction is ([[2-functor|2-]])[[functor|functorial]] under [[composition]] of [[spans]]:

Concretely, given a pair of composable spans:

\begin{tikzcd}[sep=20]
  & 
  X
  \ar[dl, "f"{swap}]
  \ar[dr, "g"]
  &&
  Y
  \ar[dl, "h"{swap}]
  \ar[dr, "k"]
  \\
  A && B && C
\end{tikzcd}

and their composite in [[Span]] formed by the [[fiber product]] of the adjacent legs

\begin{tikzcd}[sep=20]
  &&
  X \times_B Y
  \ar[dl, "q"{swap}]
  \ar[dr, "p"]
  \ar[dd, phantom, "{\lrcorner}"{rotate=-45, pos=.3}]
  \\
  & 
  X
  \ar[dl, "f"{swap}]
  \ar[dr, "g"]
  &&
  Y
  \ar[dl, "h"{swap}]
  \ar[dr, "k"]
  \\
  A && B && C
\end{tikzcd}

then functoriality of pull-push means that the
 *two* different ways to pull-push through the diagram coincide:

Pull-pushing through the spans separately results in

$$
  (k_\ast h^\ast)
  \circ
  (g_\ast f^\ast)
  \;=\;
  k_\ast 
  \,
  \underbrace{h^\ast \, g_\ast}
  \,
  f^\ast
  \,,
$$

while pull-pushing through the composite span results in

$$
  (k p)_* (f q)^* 
  = 
  k_* 
  \,
  \underbrace{p_* \, q^*}
  \,
  f^*
  \,.
$$

For these two operations to coincide, up to [[isomorphism]], hence for pull-push to respect composition of spans, we need an isomorphism between the operations shown over braces, hence of the form

\[
  \label{BCConditionInMotivationFromIntegralTransform}
  h^\ast \, g_\ast
  \;\simeq\;
  p_* \, q^*
\]

between the two ways of  push-pulling along the sides of any [[pullback square]]

\begin{tikzcd}[sep=20]
  &
  X \times_B Y
  \ar[dl, "q"{swap}]
  \ar[dr, "p"]
  \ar[dd, phantom, "{\lrcorner}"{rotate=-45, pos=.3}]
  \\
  X
  \ar[dr, "g"]
  &&
  Y
  \ar[dl, "h"{swap}]
  \\
  & B &
\end{tikzcd}

This (eq:BCConditionInMotivationFromIntegralTransform) is the Beck-Chevalley condition:  A natural necessary condition to ensure that [[integral transforms]] by pull-push [[base change]] through [[correspondences]] is functorial under [[composition]] of [[correspondences]] by [[fiber product]] of adjacent legs.

More motivation along these lines also be found at *[[dependent linear type theory]]*. As a formulation of propagation in cohomological [[quantum field theory]] this is [Sc14](dependent+linear+type+theory#Schreiber14) there.


### From logic and type theory
 {#MotivationFromLogicAndTypeTheory}

From the point of view of [[formal logic]] and [[dependent type theory]], the three items $f_! \dashv f^\ast \vdash f_\ast$ in a [[base change]] [[adjoint triple]] constitute the [[categorical semantics]] of [[quantification]] and [[context extension]] ([[existential quantification]]/[[dependent pair type]] $\dashv$ [[context extension]] $\dashv$ [[universal quantification]]/[[dependent product type]]), and so the Beck-Chevalley condition says that these are compatible with each other: concretely that [[substitution]] of [[free variables]] commutes with [[quantification]] --- a condition which [[syntax|syntactically]] is "self-evident", at least it is evidently desirable.

Original articles with this logical perspective on the BC condition: [Lawvere (1970), p. 8](#Lawvere70); [Seely (1983), p. 511](#Seely83); [Pavlović (1991), §1](#Pavlović91); [Pavlović (1996), p. 164](#Pavlović96).

For more on this logical aspect see [below](#InTypeTheory).



## Definition

Suppose given a [[commutative square]] (up to [[isomorphism]]) of [[functors]]:
$$\array{ & \overset{f^*}{\to} & \\
  ^{g^*}\downarrow && \downarrow^{k^*}\\
  & \underset{h^*}{\to} & }$$
in which $f^*$ and $h^*$ have [[left adjoint]]s $f_!$ and $h_!$, respectively. (The classical example is a [[Wirthmüller context]].)  Then the [[natural isomorphism]] that makes the square commute 

$$
  k^* f^* \to h^* g^*
$$

has a [[mate]]

$$ 
  h_! k^* \to g^* f_! 
$$

defined as the composite

$$ 
  h_! k^* \overset{\eta}{\to} h_! k^* f^* f_! \overset{\cong}{\to} h_! h^* g^* f_! \overset{\epsilon}{\to} g^* f_!   
  \,.
$$

We say the original square satisfies the **Beck--Chevalley condition** if this mate is an [[isomorphism]].

More generally, it is clear that for this to make sense, we only need a transformation $k^* f^* \to h^* g^*$; it doesn't need to be an isomorphism.  We also use the term *Beck--Chevalley condition* in this case,



### Left and right Beck--Chevalley condition

Of course, if $g^*$ and $k^*$ also have [[left adjoints]], there is also a Beck--Chevalley condition stating that the corresponding mate $k_! h^* \to f^* g_!$ is an isomorphism, and this is not equivalent in general.  Context is usually sufficient to disambiguate, although some people speak of the "left" and "right" Beck--Chevalley conditions.

Note that if $k^* f^* \to h^* g^*$ is not an isomorphism, then there is only one possible Beck-Chevalley condition.




### Dual Beck--Chevalley condition

If $f^*$ and $h^*$ have *right* adjoints $f_*$ and $h_*$, there is also a dual Beck--Chevalley condition saying that the mate $g^* f_* \to h_* k^*$ is an isomorphism.  By adjointness, if $f^*$ and $h^*$ have right adjoints and $g^*$ and $k^*$ have left adjoints, then $g^* f_* \to h_* k^*$ is an isomorphism if and only if $k_! h^* \to f^* g_!$ is.

### For bifibrations

Originally, the Beck-Chevalley condition was introduced in ([B&#233;nabou-Roubaud, 1970](#BenabouRoubaud70)) for [[bifibrations]] over a base category with pullbacks. In *loc.cit.* they call this condition **Chevalley condition** because he introduced it in his 1964 seminar. 


A [[bifibration]] $\mathbf{X} \to \mathbf{B}$ where $\mathbf{B}$ has pullbacks satisfies the **Chevalley condition** iff for every commuting square
$$\array{ & \overset{\psi^\prime}{\rightarrow} & \\
  \downarrow^{\varphi^\prime} && \downarrow^{\varphi}\\
  & \underset{\psi}{\rightarrow} & }$$
in $\mathbf{X}$ over a pullback square in the base $\mathbf{B}$ where $\varphi$ is [[cartesian morphism|cartesian]] and $\psi$ is cocartesian it holds that $\varphi^\prime$ is cartesian
iff $\psi^\prime$ is cocartesian. Actually, it suffices
to postulate one direction because the other one follows.
The nice thing about this formulation is that there is no
mention of "canonical" morphisms and no mention of [[cleavages]]. 

A fibration $P$ has products satisfying the Chevalley condition iff the opposite fibration $P^{op}$ is 
a bifibration satisfying the Chevalley condition in the above sense.

According to the [[Benabou–Roubaud theorem]], the Chevalley condition  is crucial for establishing the connection between the descent in the sense of fibered categories and the [[monadic descent]].



### "Local" Beck--Chevalley condition {#Local}

Suppose that $f^*$ and $h^*$ do not have entire left adjoints, but that for a particular object $x$ the left adjoint $f_!(x)$ exists.  This means that we have an object "$f_! x$" and a morphism $\eta_x\colon x \to f^* f_! x$ which is initial in the [[comma category]] $(x / f^*)$.  Then we have $k^*(\eta) \colon k^* x \to k^* f^* f_! x \to h^* g^* f_! x$, and we say that the square satisfies the *local Beck-Chevalley condition at $x$* if $k^*(\eta)$ is initial in the comma category $(k^* x / h^*)$, and hence exhibits $g^* f_! x$ as "$h_! k^* x$" (although we have not assumed that the entire functor $h_!$ exists).

If the functors $f_!$ and $h_!$ do exist, then the square satisfies the (global) Beck-Chevalley condition as defined above if and only if it satisfies the local one defined here at every object.

## In logic / type theory
 {#InTypeTheory}

If the functors in the formulation of the Beck-Chevalley condition are [[base change]] functors in the [[categorical semantics]] of some [[dependent type theory]] (or just of a [[hyperdoctrine]]) then the BC condition is equivalently stated in terms of logic as follows. 

A [[commuting diagram]]  

$$
  \array{
    D &\stackrel{h}{\to}& C 
    \\
    {}^{\mathllap{k}}\downarrow && \downarrow^{\mathrlap{g}}
    \\
    A &\stackrel{f}{\to}& B
  }
$$

is interpreted as a morphism of [[contexts]]. The [[pullback]] (of [[slice categories]] or of fibers in a [[hyperdoctrine]]) $h^*$ and $f^*$ is interpreted as the [[substitution]] of [[variables]] in these contexts. And the [[left adjoint]] $\sum_k \coloneqq k_! $ and $\sum_q \coloneqq g_!$, the [[dependent sum]] is interpreted (up to [[truncated|(-1)-truncation]], possibly) as [[existential quantifier|existential quantification]]. 

In terms of this the Beck-Chevalley condition says that if the above diagram is a [[pullback]], then **substitution commutes with existential quantification**

$$
  \sum_k h^* \phi \stackrel{\simeq}{\to} f^* \sum_g \phi
  \,.
$$

+-- {: .num_example}
###### Example

Consider the diagram of [[contexts]]

$$
  \array{
    [\Gamma, x : X] &\stackrel{}{\to}& [\Gamma, x : X, y : Y]
    \\
    \downarrow && \downarrow
    \\
    \Gamma &\to& [\Gamma, y : Y]
  }
  \;\;\;
  \simeq
  \;\;\;
  \array{
    \Gamma \times X &\stackrel{(p_1,p_2,t)}{\to}& \Gamma \times X \times Y
    \\
    {}^{\mathllap{p_1}}\downarrow && \downarrow^{\mathrlap{(p_1,p_3)}}
    \\
    \Gamma &\stackrel{(id,t)}{\to} & \Gamma \times Y
  }
  \,,
$$

with the horizontal morphism coming from a [[term]] $t : \Gamma \to Y$ in [[context]] $\Gamma$ and the vertical morphisms being the evident [[projection]], then the condition says that we may in a [[proposition]] $\phi$ substitute $t$ for $y$ before or after quantifying over $x$:

$$
 \sum_{x : X} \phi(x,t) \simeq (\sum_{x : X} \phi(x,y))[t/y]
 \,.
$$

=--

## Examples

### Various

* The [[codomain fibration]] of any [[category]] with [[pullbacks]] is a bifibration, and satisfies the Beck--Chevalley condition at every pullback square. In particular, [[locally cartesian closed categories]] always satisfy the Beck--Chevalley condition.

* If $C$ is a [[regular category]] (such as a [[topos]]), the bifibration $Sub(C) \to C$ of [[subobjects]] satisfies the Beck--Chevalley condition at every pullback square.

* The [[family fibration]] $Fam(C)\to Set$ of any category $C$ with small sums satisfies the Beck--Chevalley condition at every pullback square in $Set$.

* [Mackey's restriction formula](double+coset#MackeyFormula) for group representations.


### Images and pre-images


\begin{example}
\label{BeckChevalleyForPreImageBetweenPowerSets}
**(Beck-Chevalley for images and pre-images of sets)**
\linebreak
  Given a [[set]] $S \,\in\, Set$, write $\mathcal{P}(S)$ for its [[power set]] regarded as a [[poset]], meaning that

1. $\mathcal{P}(S)$ is the set of [[subsets]] $A \subset S$,

1. regarded as a [[category]] by declaring that there is a [[morphisms]] $A \to B$ precisely if $A \subset B$ as subsets of $S$.

Then for $f \,\colon\, S \longrightarrow T$ a [[function]] between sets, we obtain the followin three [[functors]] between their [[power sets]]:

1. $f_! \,\coloneqq\, f(-) \,\colon\, \mathcal{P}(S) \longrightarrow \mathcal{P}(T)$

   forms [[images]] under $f$

1. $f^\ast \,\coloneqq\, f^{-1} \,\colon\, \mathcal{P}(T) \longrightarrow \mathcal{P}(S)$

   forms [[preimages]] under $f$,

1. $f_ast \,\coloneqq\, T \setminus f\big(S \setminus (-)\big) \,\colon\, \mathcal{P}(S) \longrightarrow \mathcal{P}(T)$

   forms the [[complement]] of [[images]] of [[complements]].

These three functors constitute an [[adjoint triple]] 

$$
  f(-) \;\dashv\; f^{-1} \;\dashv\; f_\ast
$$

as is readily verified and also discussed at some length in the entry *[[interactions of images and pre-images with unions and intersections]]*.

In particular, the familiar/evident fact that forming [[images]] and [[preimages]] [[preserved colimit|preserves]] [[unions]] may be understood as a special case of the fact that [[left adjoints preserve colimits]].

Now given a [[pullback diagram]] in [[Set]]

   \[
     \label{PullbackOfSets}
     \array{
       D' 
         &\overset{\beta}{\longrightarrow}& 
       D
       \\
       \mathllap{{}^{\psi}}\big\downarrow 
       &{}^{{}_{(pb)}}& 
       \big\downarrow\mathrlap{{}^{\phi}}
       \\
       C' 
         &\underset{\alpha}{\longrightarrow}& 
       C
     }  
   \]

then these operations satisfy the left Beck-Chevalley condition in the sense that the following [[diagram]] of [[poset]]-[[homomorphisms]] ([[functors]]) [[commuting diagram|commutes]]:

   \[
     \label{RightBeckChevalleyDiagramForPreImages}
     \array{
       \mathcal{P}(D') 
         &\overset{\beta_!}{\longrightarrow}& 
       \mathcal{P}(D)
       \\
       \mathllap{{}^{\psi^{-1}}}\big\uparrow
       && 
       \big\uparrow\mathrlap{{}^{\phi^{-1}}}
       \\
       \mathcal{P}(C') 
         &\underset{\alpha_!}{\longrightarrow}& 
       \mathcal{P}(C)
     }  
   \]
To see this it is sufficient to check commutativity on [[singleton]]-[[subsets]] (because every other subset is a [[union]] of singletons and, as just remarked, [[interactions of images and pre-images with unions and intersections|images and preimages preserve unions]])
and given a [[singleton]] set $\{c'\} \subset C'$ on an element $c' \,\in\, C'$, we directly compute as follows: 
   \[
     \label{PreimagesInAPullbackDiagram}
     \begin{array}{l}
     \beta \circ \psi^{-1}\big(\{c'\}\big)
     \\
     \;\simeq\;
     \beta\Big(
       \big\{ 
         (c',d) 
         \,\big\vert\,
         d \,\in\, D
         \,,
         \phi(d) = \alpha(c')
       \big\}
     \Big)
     \\
     \;=\;
     \big\{ 
       d \,\in\, D
       \,\big\vert\,
       \phi(d) = \alpha(c')
     \big\}
     \\
     \;=\;
     \phi^{-1}\big(
      \{\alpha(c')\}
     \big)
     \\
     \;=\;
     \phi^{-1} \circ \alpha\big(\{c'\}\big)
     \,.
     \end{array}
   \]
Here it is the first two steps which make use of the assumption that (eq:PullbackOfSets) is a [[pullback square]], namely which means that $D'$ is compatibly [[bijection|bijective]] to the [[fiber product]] of $C'$ with $D$ over $C$:

$$
  \array{
  D' 
  &\simeq&
  \big\{  
    (c', d) \in C' \times D 
    \,\big\vert\,
    \phi(d) 
      \,=\, 
    \alpha(c') 
  \big\}
  \\
  \mathllap{{}^{\beta}}
  \big\downarrow 
    && 
  \!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
  \big\downarrow\mathrlap{{}^{ (c',d) \mapsto d }}
  \\
  D 
  &=& 
  \!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
  D
  }
$$
\end{example}

This elementary example \ref{BeckChevalleyForPreImageBetweenPowerSets} actually constitutes half of the proof of the archetypical example of Prop. \ref{BCForPresheavesOnPullbacksOfOpfibrations} below.

### Systems of functor categories
 {#PullbacksOfOpfibrations}


\begin{proposition}
\label{BCForPresheavesOnPullbacksOfOpfibrations}
Given 

1. $\phi \colon D \to C$ is an [[opfibration]] of [[small categories|small]] [[strict categories]] 

1. a [[pullback]] [[diagram]] in the _[[1-category]]_ [[Cat]] of [[small category|small]] [[strict categories]] and [[functors]] of the form

   \[
     \label{StrictPullbackOfOpfibration}
     \array{
       D' 
         &\overset{\beta}{\longrightarrow}& 
       D
       \\
       \mathllap{{}^{\psi}}\big\downarrow 
       &{}^{{}_{(pb)}}& 
       \big\downarrow\mathrlap{{}^{\phi}}
       \\
       C' 
         &\underset{\alpha}{\longrightarrow}& 
       C
     }  
   \]

   (hence presenting a [[2-pullback]]/[[homotopy pullback]], see Rem. \ref{PullbackOfOpfibrationModelsTwoPullback} below),

1. $\mathcal{C}$ any [[category]] with all [[small colimits]]



then the induced diagram of [[functor categories]]

$$
  \array{
    [D', \mathcal{C}] 
      &\overset{\beta^*}{\longleftarrow}& 
    [D, \mathcal{C}]
    \\
    \Big\downarrow\mathrlap{{}^{\psi_!}} 
      && 
    \Big\downarrow\mathrlap{{}^{\phi_!}}
    \\
    [C', \mathcal{C}] 
      &\underset{\alpha^*}{\longleftarrow}& 
    [C,\mathcal{C}]
  }
$$

(for $(-)^\ast$ denoting [[precomposition]] and $(-)_!$ denoting [[left Kan extension]]) 

satisfies the Beck-Chevalley condition, in that there is a [[natural isomorphism]]

$$
  \psi_! \circ \beta^* 
  \;\simeq\; \alpha^* \circ \phi_!
  \,.
$$
\end{proposition}
For this statement in the more general context of [[quasicategories]] see [Joyal (2008), prop. 11.6](#Joyal08).
\begin{proof}
The proof relies on two observations:

1. Since $\phi$ is [[opfibration|opfibered]], for every object $c \in C$ the embedding of the [[fiber]] $\phi^{-1}(c)$ into the [[comma category]] $\phi/c$ is a [[final functor]]. Therefore the [pointwise formula](Kan+extension#PointwiseByConicalLimits) for the [[left Kan extension]] $\phi_!$ is equivalently given by taking the [[colimit]] over the [[fiber]], instead of over the [[comma category]]:

  \[
    \label{PointwiseLeftKanExtensionInOpfiberedCase}
    \phi_!(X)_c 
    \;\simeq\; 
    \underset
      {\underset{\phi^{-1}\big(\{c\}\big)}{\longrightarrow}}
      {\lim} 
     \,
      X
    \,.
  \]

1. Since (eq:StrictPullbackOfOpfibration) is a (strict) pullback of (strict) categories (i.e. an ordinary pullback of [[sets]] of [[objects]] and of [[sets]] of [[morphisms]]), the operations of taking [[images]] and [[preimages]] $(-)^{-1}$ ([[fibers]]) of the [[object]]-[[functions]] of the given functors satisfy the [[poset|posetal]] Beck-Chevalley condition from Exp. \ref{BeckChevalleyForPreImageBetweenPowerSets}:

   \[
     \label{PreimagesInAPullbackDiagram}
     \begin{array}{l}
     \beta \circ \psi^{-1}\big(\{c'\}\big)
     \\
     \;\simeq\;
     \beta\Big(
       \big\{ 
         (c',d) 
         \,\big\vert\,
         d \,\in\, D
         \,,
         \phi(d) = \alpha(c')
       \big\}
     \Big)
     \\
     \;=\;
     \big\{ 
       d \,\in\, D
       \,\big\vert\,
       \phi(d) = \alpha(c')
     \big\}
     \\
     \;=\;
     \phi^{-1}\big(
      \{\alpha(c')\}
     \big)
     \\
     \;=\;
     \phi^{-1} \circ \alpha\big(\{c'\}\big)
     \,.
     \end{array}
   \]

   for all [[objects]] $c' \,\in\, Obj(C')$.

Now using first (eq:PointwiseLeftKanExtensionInOpfiberedCase) and then (eq:PreimagesInAPullbackDiagram) and then again (eq:PointwiseLeftKanExtensionInOpfiberedCase) yields the following sequence of [[isomorphisms]]

$$
  \begin{aligned}
    \big(\psi_! \beta^* (X)\big)(c')
    & 
    \;\simeq\;
    \underset
      {\underset{
        \beta \circ \psi^{-1}\big(\{c'\}\big)
      }{\longrightarrow}}
      {\lim} 
     \,
    X
    \\
    & 
    \;\simeq\;
    \underset
      {\underset{
        \phi^{-1} \circ \alpha\big(\{c'\}\big)
      }{\longrightarrow}}
      {\lim} 
    \,
    X
    \\
    & 
    \;\simeq\;
    \big(\alpha^* \phi_! (X)\big)(c')
    \,,
  \end{aligned}
$$

all of them [[natural isomorphism|natural]] in $c' \,\in\, Obj(C')$.
\end{proof}

\begin{remark}
As a [[counter-example]] showing that in Prop. \ref{BCForPresheavesOnPullbacksOfOpfibrations} the condition for $\phi \colon D \to C$ to be an [[opfibration]] is necessary for the statement to hold, consider 

* $C \coloneqq \{0\to 1\}$ the [[interval category]], 

* $D \coloneqq \ast,\;\;C' \coloneqq \ast$ the [[terminal category]], 

* $\phi\coloneqq const_0,\;\;\alpha \coloneqq const_1$.

Then the [[pullback]] $D' = \varnothing$ is the [[empty category]]. Therefore 

* $[D',\mathcal{C}] = [\varnothing, \mathcal{C}]$ is the [[terminal category]], so that $\psi_!\circ \beta^\ast$ is a [[constant functor]]

  (concretely, $\psi_! \colon \ast \simeq [\varnothing, \mathcal{C}] \to [C',\mathcal{C}]$ is [[left adjoint]] to the projection functor to the [[terminal category]] and [hence](initial+object#AdjointsToConstantFunctors) picks the [[initial object]] of $[C',\mathcal{C}]$),

* while $\alpha^* \circ \phi_!$ is the [[identity functor]]

  (to see this observe first that $[C,\mathcal{C}]$ now may be identified with the [[arrow category]] of $\mathcal{C}$, and second that, under this identification, $\phi_! \colon X \mapsto id_X$ sends any [[object]] of $\mathcal{C}$ to its [[identity morphism]], as is verified by observing that this is clearly [[left adjoint]] to the [[domain]]-restriction $\phi^\ast$).
   
\end{remark}

\begin{remark}
\label{PullbackOfOpfibrationModelsTwoPullback}
  In Prop. \ref{BCForPresheavesOnPullbacksOfOpfibrations},
  the [[pullback]] (eq:StrictPullbackOfOpfibration) of an [[opfibration]] of [[strict categories]] formed in the [[1-category]] of [[strict categories]] may be understood as modelling the [[2-pullback]] (cf. [there](2-pullback#StrictPullback)) of the corresponding [[cospan]] in the actual [[2-category]] [[Cat]].

In particular, if the [[strict categories]] involved in the pullback diagram (eq:StrictPullbackOfOpfibration) are all [[groupoids]], then a functor such as $\phi$ being a [[Kan fibration]] is equivalent to its [[nerve]] being a [[Kan fibration]] (see at *[[right Kan fibration]]*, [this and](right%2Fleft+Kan+fibration#FibrationInGroupoidsAsRightKanFibrations) [this Prop](right%2Fleft+Kan+fibration#OverKanComplex)), in which case the pullback diagram (eq:StrictPullbackOfOpfibration) models the [[homotopy pullback]] (by [this Prop.](homotopy+pullback#HomotopyPullbackByOrdinaryPullback)).
\end{remark}

### Enriched functor categories

Consider

* $(\mathbf{V}, \otimes, \mathbb{1})$ a [[cocomplete category|cocomplete]] [[symmetric monoidal category]], regarded as a [[cosmos for enrichment]],

* $\mathbf{C}$ a [[cocomplete category|cocomplete]] $\mathbf{V}$-[[enriched category]] which is also [[tensoring|tensored]] over $\mathbf{V}$, denoted:

  $$
    (-)\cdot(-)
    \;\colon\;
    \mathbf{V} \times \mathbf{C}
    \longrightarrow
    \mathbf{C} 
  $$

and write

* for any [[small category|small]] $\mathbf{V}$-[[enriched category]] $\mathcal{X} \,\in\, \mathbf{V}Cat^{small}$:

  $$
    \mathbf{V}Func(\mathcal{X},\,\mathbf{C})
    \;\in\;
    Cat
  $$ 
  
  for the $\mathbf{V}$-[[enriched-functor category]] from $\mathcal{X}$ to $\mathbf{C}$,

* for any $\mathbf{V}$-enriched functor $f \,\colon\, \mathcal{X} \longrightarrow \mathcal{Y}$:

  $$
    \mathbf{V}Func(\mathcal{X},\,\mathbf{C})
    \underoverset
      {\underset{f^\ast}{\longleftarrow}}
      {\overset{f_!}{\longrightarrow}}
      {\;\;\; \bot \;\;\;}
    \mathbf{V}Func(\mathcal{Y},\,\mathbf{C})
  $$

  for the [[pair]] of [[adjoint functors]] given by [[precomposition]] and by [[left Kan extension]], the latter being expressible by the following [[coend]]-formula (see [there](Kan+extension#eq:LeftKanExtensionViaCoendFormula)):

\[
  \label{CoendFormulaForLeftKanExtension}
  \mathscr{V}_{(-)}
  \;\in\; \mathbf{V}Func(\mathcal{X},\,\mathbf{C})
  \;\;\;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;\;\;
  (f_! \mathscr{V})_y
  \;\simeq\;
  \int^{x \in \mathcal{X}}
  \mathcal{X}\big(f(x),\,y\big)
  \cdot
  \mathscr{V}_{x}
  \,.
\]


The following is a rather simplistic but maybe instructive example:

\begin{example}
\label{ForPushPullofEnrichedPresheavesThroughProjectionDiagram}
In the case of a *[[cartesian closed category|cartesian closed]]* [[cosmos]] $(\mathbf{V}, \times, \ast)$
consider for $\mathcal{X}, \mathcal{Y}, \mathcal{X}' \,\in\, \mathbf{V}Cat^{small}$
a commuting diagram of $\mathbf{V}$-[[enriched functors]] of the following form:
$$
  \array{
    \mathcal{X} \times \mathcal{X}'
    &\overset{f \times id}{\longrightarrow}&
    \mathcal{Y} \times \mathcal{X}'
    \\
    \mathllap{{}^{pr_{\mathcal{X}}}}
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow
    \mathrlap{{}^{pr_{\mathcal{Y}}}}
    \\
    \mathcal{X}
    &\underset{\;\;\; f \;\;\;}{\longrightarrow}&
    \mathcal{Y}
  }
$$
(which is a [[pullback]] square in the [[1-category]] of [[strict category|strict]] $\mathbf{V}$-[[enriched categories]]).
 
Then the Beck-Chevalley condition on $\mathbf{C}$-valued $\mathbf{V}$-functors holds, in that the following [[commuting diagram|diagram commutes]]:
$$
  \array{
    \mathbf{V}Func(
      \mathcal{X} \times \mathcal{X}'
      ,\,
      \mathbf{C}
    \big)
    &\overset{(f \times id)_!}{\longrightarrow}&
    \mathbf{V}Func(
      \mathcal{Y} \times \mathcal{X}'
      ,\, 
      \mathbf{C}
    )
    \\
    \mathllap{{}^{(pr_{\mathcal{X}})^\ast}}
    \big\uparrow
    &&
    \big\uparrow
    \mathrlap{{}^{(pr_{\mathcal{Y}})^\ast}}
    \\
    \mathbf{V}Func(\mathcal{X},\,\mathbf{C})
    &\underset{\;\;\; f_! \;\;\;}{\longrightarrow}&
    \mathbf{V}Func(\mathcal{Y},\,\mathbf{C})
  }
$$

To see this, we may check object-wise as follows:
$$
  \begin{array}{l}
  \big(
    (f \times id)_! 
    (pr_{\mathcal{X}})^\ast
    \mathscr{V}
  \big)_{(y,x')}
  \\
  \;=\;
  \int^{(x,x'_0)}
  \mathcal{Y}\big(f(x),y\big)
  \times
  \mathcal{X}'\big(x'_0,x'\big)
  \cdot
  \big(
    (pr_{\mathcal{X}})^\ast\mathscr{V}_{x,x'_0}
  \big)
  \\
  \;=\;
  \int^{(x,x'_0)}
  \mathcal{Y}\big(f(x),y\big)
  \times
  \mathcal{X}'\big(x'_0,x'\big)
  \cdot
  \mathscr{V}_{x}
  \\
  \;=\;
  \int^{x'_0}
  \int^{x}
  \mathcal{Y}\big(f(x),y\big)
  \times
  \mathcal{X}'\big(x'_0,x'\big)
  \cdot
  \mathscr{V}_{x}
  \\
  \;\simeq\;
  \int^{x'_0}
  \mathcal{X}'\big(x'_0,x'\big)
  \cdot
  \int^{x}
  \mathcal{Y}\big(f(x),y\big)
  \cdot
  \mathscr{V}_{x}
  \\
  \;\simeq\;
  \int^{x}
  \mathcal{Y}\big(f(x), y\big)
  \cdot
  \mathscr{V}_{x}
  \\
  \;\simeq\;
  \big(
    f_!
    \mathscr{V}
  \big)_y
  \\
  \;\simeq\; 
  \big(
  (pr_{\mathcal{Y}})^\ast
  (
    f_!
    \mathscr{V}
  )
  \big)_{y,x'}
  \,,
  \end{array}
$$
where we used (apart from the definition of [[precomposition]]), in order of appearance: 

1. the [[coend]]-expression (eq:CoendFormulaForLeftKanExtension) for the [[left Kan extension]], 

1. the [[Fubini theorem]] for coends ([here](end#Fubini)),

1. the fact that the [[closed monoidal category|closed tensor]] $(-) \times (-)$ [[preserves colimits]] and hence [[coends]] in each variable,

1. the [[co-Yoneda lemma]] in the coend-form [here](co-Yoneda+lemma#coYonedaLemma) 

and finally the expression (eq:CoendFormulaForLeftKanExtension) again.
\end{example}

### Proper base change in &#233;tale cohomology

For [[coefficients]] of [[torsion group]], [[étale cohomology]]
satisfies Beck-Chevalley along [[proper morphisms]]. This is the statement of the  _[[proper base change theorem]]_. See there for more details.

### Grothendieck's yoga of six operations

A Beck-Chevalley condition is part of the [[axioms]] of  [[Grothendieck's yoga of six operations]], e.g. [Cisinski & Déglise (2009), §A.5](#CisinskiDéglise09), [Gallauer (2021), p. 16](#Gallauer21), [Scholze (2022), p. 11](#Scholze22).


## Related pages

* [[exact square]]
* [[Benabou-Roubaud theorem]]


## References
 {#References}

> The Beck-Chevalley condition has arisen in the theory of [[monadic descent|descent]] - as developed from [[Grothendieck]] 1959. [[Jon Beck]] and [[Claude Chevalley]] studied it independently from each another. &lbrack;...&rbrack; It is conspicuous that neither of them ever published anything on it. &lbrack;[Pavlović 1991, §14](#Pavlović91)&rbrack;

Original articles:

* {#BenabouRoubaud70} [[Jean Bénabou]], [[Jacques Roubaud]], _Monades et descente_, C. R. Acad. Sc. Paris, Ser. A **270**  (1970) 96-98 &lbrack;[gallica:12148/bpt6k480298g/f100](http://gallica.bnf.fr/ark:/12148/bpt6k480298g/f100), [[BenabouRoubaud-MonadesEtDescente.pdf:file]],   English translation (by [[Peter Heinig]]): [MO:q/279152](https://mathoverflow.net/q/279152)&rbrack;

  > (proving the [[Bénabou-Roubaud theorem]])

* {#Lawvere70} [[William Lawvere]], p. 8 of: *[[Equality in hyperdoctrines and comprehension schema as an adjoint functor]]*, Proceedings of the AMS Symposium on Pure Mathematics XVII (1970) 1-14 &lbrack;[pdf](https://ncatlab.org/nlab/files/LawvereComprehension.pdf)&rbrack;

  > (in terms of [[base change]] as the [[categorical semantics]] for [[universal quantification]]/[[dependent product]] and [[existential quantification]]/[[dependent sum]])

expanded on in 

* {#Seely83} [[Robert A. G. Seely]], *Hyperdoctrines, Natural Deduction and the Beck Condition*, Zeitschr. f. math. Logik und Grundlagen d. Math. **29** (1983) 505-542 &lbrack;[doi:10.1002/malq.19830291005]( https://doi.org/10.1002/malq.19830291005), [pdf](https://www.math.mcgill.ca/seely/ZML/ZML.PDF)&rbrack;

Review:

* {#Pavlovic1990} [[Duško Pavlović]], pp. 105 in: *Predicates and Fibrations*, PhD thesis, Utrecht (1990) &lbrack;[pdf](https://dusko.org/wp-content/uploads/2020/03/1990-proefschrift-dusko.pdf), [[Pavlovic-PredicatesAndFibrations.pdf:file]]&rbrack;

* {#Pavlović91} [[Duško Pavlović]], Section 1 of: *Categorical interpolation: Descent and the Beck-Chevalley condition without direct images*, in: *Category Theory*, Lecture Notes in Mathematics **1488** (1991) &lbrack;[doi:10.1007/BFb0084229](https://doi.org/10.1007/BFb0084229), [pdf](http://dusko.org/wp-content/uploads/2020/03/1990-Como-BCDE.pdf), [[Pavlovic-CategoricalInterpolation.pdf:file]]&rbrack;

* [[Simon John Ambler]], §5.5.1 in: *First Order Linear Logic in Symmetric Monoidal Closed Categories*, PhD thesis, Edinburgh (1991) &lbrack;[ECS-LFCS-92-194](https://www.lfcs.inf.ed.ac.uk/reports/92/ECS-LFCS-92-194), [pdf](http://www.lfcs.inf.ed.ac.uk/reports/92/ECS-LFCS-92-194/ECS-LFCS-92-194.pdf), [[Ambler-FOLL.pdf:file]]&rbrack;

> (in view of [[linear type theory]])


* {#Pavlović96} [[Duško Pavlović]], *Maps II: Chasing Diagrams in Categorical Proof Theory*, Logic Journal of the IGPL, **4** 2 (1996) 159–194 &lbrack;[doi:10.1093/jigpal/4.2.159](https://doi.org/10.1093/jigpal/4.2.159), [pdf](http://dusko.org/wp-content/uploads/2020/03/00-95-IGPL-mapsII.pdf)&rbrack;

* [[Paul Balmer]], around §7.5 of: *Stacks of group representations*, J. European Math. Soc. **17** 1 (2015) 189-228 &lbrack;[arXiv:1302.6290](https://arxiv.org/abs/1302.6290), [doi:10.4171/jems/501](https://doi.org/10.4171/jems/501)&rbrack;

Discussion for [[subobject lattices]]:

* [[Saunders MacLane]], [[Ieke Moerdijk]], chapter IV.9 (around p. 205) of: _[[Sheaves in Geometry and Logic]]_,   Springer (1992) &lbrack;[doi:10.1007/978-1-4612-0927-0](https://link.springer.com/book/10.1007/978-1-4612-0927-0)&rbrack;

Review in the context of [[Grothendieck's yoga of six operations]]:

* {#CisinskiDéglise09} [[Denis-Charles Cisinski]], [[Frédéric Déglise]], section A.5 of: *Triangulated categories of mixed motives*, Springer Monographs in Mathematics, Springer (2019) &lbrack;[arXiv:0912.2110](http://arxiv.org/abs/0912.2110), [doi:10.1007/978-3-030-33242-6](https://doi.org/10.1007/978-3-030-33242-6)&rbrack;
 

* {#Gallauer21} [[Martin Gallauer]], pp. 16 of: *An introduction to six-functor formalism*, lecture at *[The Six-Functor Formalism and Motivic Homotopy Theory](https://sites.google.com/view/summer-school-motivic/home)*, Università degli Studi di Milano (Sept. 2021) &lbrack;[arXiv:2112.10456](https://arxiv.org/abs/2112.10456), [pdf](https://homepages.warwick.ac.uk/staff/Martin.Gallauer/docs/m6ff.pdf)&rbrack;

* {#Scholze22} [[Peter Scholze]], p. 11 of: *Six Functor Formalisms*, [lecture notes ](https://people.mpim-bonn.mpg.de/scholze/Course%20Winter%202223.html) (2022) &lbrack;[pdf](https://people.mpim-bonn.mpg.de/scholze/SixFunctors.pdf), [[Scholze-SixOperations.pdf:file]]&rbrack;



Discussion for [[derived functors]] with focus on the example of [[base change]] of [[retractive spaces]] and [[homotopy categories]] of [[parameterized spectra]]:

* [[Michael Shulman]], *Comparing composites of left and right derived functors*, New York Journal of Mathematics **17** (2011) 75-125 &lbrack;[arXiv:0706.2868](https://arxiv.org/abs/0706.2868), [eudml:229181](https://eudml.org/doc/229181)&rbrack;

* [[Mike Shulman]], *Framed bicategories and monoidal fibrations*, Theory and Applications of Categories, **20** 18 (2008) 650–738 &lbrack;[tac:2018](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html), [arXiv:0706.1286](https://arxiv.org/abs/0706.1286)&rbrack;

Discussion in the generality of [[enriched category theory]]:

* [[Michael Shulman]], e.g. Thm. 9.3 in: *Enriched indexed categories*, Theory Appl. Categ. **28** (2013) 616-695 &lbrack;[doi:1212.3914](https://arxiv.org/abs/1212.3914), [tac:28-21](http://www.tac.mta.ca/tac/volumes/28/21/28-21abs.html)&rbrack;


Discussion in the generality of [[(infinity,1)-categories|$\infty$-categories]]:

* {#HopkinsLurie13} [[Michael Hopkins]], [[Jacob Lurie]], Prop. 4.3.3 in: *[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]* (2013) &lbrack;[pdf](http://www.math.harvard.edu/~lurie/papers/Ambidexterity.pdf)&rbrack;


* [[Urs Schreiber]], around Def. 5.5 of: *[[schreiber:Quantization via Linear homotopy types]]* &lbrack;[arXiv:1402.7041](https://arxiv.org/abs/1402.7041)&rbrack;

* {#GaitsgoryLurie} [[Dennis Gaitsgory]], [[Jacob Lurie]], Section 2.4.1 of: _Weil's conjecture for function fields_ (2014-2017) &lbrack;["first volume of expanded account" pdf](https://www.math.ias.edu/~lurie/papers/tamagawa-abridged.pdf)&rbrack;

for [[infinity-cosmos|$\infty$-cosmoi]]:

* [[Emily Riehl]], [[Dominic Verity]], Prop. 5.3.9 in: *Kan extensions and the calculus of modules for ∞-categories*, Algebr. Geom. Topol. **17** (2017) 189-271 &lbrack;[doi:10.2140/agt.2017.17.189](https://doi.org/10.2140/agt.2017.17.189), [arXiv:1507.01460](https://arxiv.org/abs/1507.01460)&rbrack;

Discussion for presheaf categories in the context of [[quasicategories]] ([[(infinity,1)-categories of (infinity,1)-presheaves|$\infty$-categories of $\infty$-presheaves]]):

* {#Joyal08} [[André Joyal]], [p. 175](https://ncatlab.org/nlab/files/JoyalTheoryOfQuasiCategories.pdf#page=27) of: *[[The Theory of Quasi-Categories and its Applications]]*, lectures at _[Advanced Course on Simplicial Methods in Higher Categories](https://lists.lehigh.edu/pipermail/algtop-l/2007q4/000017.html)_, CRM (2008) &lbrack;[pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf), [[JoyalTheoryOfQuasiCategories.pdf:file]]&rbrack;

Discussion for [[Goursat categories]]:

* [[Marino Gran]], [[Diana Rodelo]], *Beck-Chevalley condition and Goursat categories*, Journal of Pure and Applied Algebra **221** 10 (2017) 2445-2457 &lbrack;[arXiv:1512.04066](https://arxiv.org/abs/1512.04066), [doi:10.1016/j.jpaa.2016.12.031](https://doi.org/10.1016/j.jpaa.2016.12.031)&rbrack;


[[!redirects Beck-Chevalley conditions]]

[[!redirects Beck-Chevalley_Condition]]
[[!redirects Beck-Chevalley Condition]]
[[!redirects Beck–Chevalley condition]]
[[!redirects Beck--Chevalley condition]]
[[!redirects Beck condition]]
[[!redirects Chevalley condition]]
[[!redirects Beck-Chevalley property]]
[[!redirects Beck–Chevalley property]]
[[!redirects Beck--Chevalley property]]

[[!redirects Beck-Chevalley transformation]]
[[!redirects Beck-Chevalley transformations]]

[[!redirects Beck-Chevalley relation]]
[[!redirects Beck-Chevalley relations]]

[[!redirects Beck-Chevalley]]

