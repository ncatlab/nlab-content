
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In a [[locally ∞-connected (∞,1)-topos]] with [[full and faithful (∞,1)-functor|fully faithful]] [[inverse image]] (such as a [[cohesive (∞,1)-topos]]), the extra [[left adjoint]] $\Pi$ to the [[inverse image]] $Disc$ of the [[global sections]] [[geometric morphism]] $\Gamma$ induces a  [[higher modality]] $\esh \coloneqq Disc \circ \Pi$, which sends an [[object]] to something that may be regarded equivalently as its [[geometric realization]] or its [[fundamental ∞-groupoid]] (see at _[[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos]]_ and at _[[shape via cohesive path ∞-groupoid]]_). In either case $\esh X$ may be thought of as the _[[shape]]_ of $X$ and therefore one may call $\esh$ the _shape modality_.  It forms an [[adjoint modality]] with the [[flat modality]] $\flat \coloneqq Disc \circ \Gamma$.

## Definition

### In type theory

We assume a [[dependent type theory]] with crisp term judgments $a::A$ in addition to the usual (cohesive) type and term judgments $A \; \mathrm{type}$ and $a:A$, as well as context judgments $\Xi \vert \Gamma \; \mathrm{ctx}$ where $\Xi$ is a list of crisp term judgments, and $\Gamma$ is a list of cohesive term judgments. A crisp type is a type in the context $\Xi \vert ()$, where $()$ is the empty list of cohesive term judgments. In addition, we also assume the dependent type theory has [[typal equality]] and [[judgmental equality]], as well as the following [[axiom of cohesion]]:

*There is a crisp type $\Xi \vert () \vdash R \; \mathrm{type}$ such that given any crisp type $\Xi \vert () \vdash A \; \mathrm{type}$, $A$ is discrete if and only if the function $\mathrm{const}_{A, R}:A \to (R \to A)$ is an equivalence of types.*

From here, there are two different notions of the shape modality which could be defined in the type theory, the **strict shape modality**, which uses [[judgmental equality]] in the [[computation rule]] and [[uniqueness rule]], and the **weak shape modality**, which uses [[typal equality]] in the [[computation rule]] and [[uniqueness rule]]. When applied to a type they result in **strict shape types** and **weak shape types** respectively. The [[natural deduction]] rules for strict and weak shape types are provided as follows:

* Formation rules for weak and strict shape types:

$$\frac{\Xi \vert \Gamma \vdash A \; \mathrm{type}}{\Xi \vert \Gamma \vdash \esh A \; \mathrm{type}}\esh-\mathrm{form}$$

* Introduction rules for weak and strict shape types:

$$\frac{\Xi \vert \Gamma \vdash a:A}{\Xi \vert \Gamma \vdash \sigma_A(a):\esh A}\esh-\mathrm{intro}1$$

$$\frac{\Xi \vert \Gamma \vdash g:R \to \esh A \quad \Xi, \Gamma \vert () \vdash x:R}{\Xi \vert \Gamma \vdash k_A(g):\esh A}\esh-\mathrm{intro}2$$

$$\frac{\Xi \vert \Gamma \vdash g:R \to \esh A \quad \Xi, \Gamma \vert () \vdash x:R}{\Xi \vert \Gamma \vdash \iota_A(g, x):g(x) =_{\esh A} k_A(g)}\esh-\mathrm{intro}3$$

$$\frac{\Xi \vert \Gamma \vdash g:R \to \esh A \quad \Xi, \Gamma \vert () \vdash x:R}{\Xi \vert \Gamma \vdash k_A'(g):\esh A}\esh-\mathrm{intro}4$$

$$\frac{\Xi \vert \Gamma \vdash x:R}{\Xi \vert \Gamma \vdash \iota_A'(x):x =_{\esh A} k_A'(\mathrm{const}_{\esh A, R}(x))}\esh-\mathrm{intro}5$$

* Elimination rules for weak and strict shape types:

$$\frac{\Xi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi \vert \Gamma, w:\esh A \vdash Q \; \mathrm{type} \quad \Xi \vert \Gamma \vdash x:A}{\Xi \vert \Gamma \vdash d_{\sigma_A}(x):Q[\sigma_A(x)/w]}\esh-\mathrm{elim}1$$

$$\frac{\Xi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi \vert \Gamma, w:\esh A \vdash Q \; \mathrm{type} \quad \Xi \vert \Gamma \vdash g:R \to \esh A \quad \Xi \vert \Gamma \vdash x:R \quad \Xi \vert \Gamma \vdash h:Q[g(x)/w]}{\Xi \vert \Gamma \vdash d_{\kappa_A}(g, h):Q[\kappa_A(g)/w]}\esh-\mathrm{elim}2$$

$$\frac{\Xi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi \vert \Gamma, w:\esh A \vdash Q \; \mathrm{type} \quad \Xi \vert \Gamma \vdash g:R \to \esh A \quad \Xi \vert \Gamma \vdash x:R \quad \Xi \vert \Gamma \vdash h:Q[g(x)/w]}{\Xi \vert \Gamma \vdash d_{\iota_A}(g, x.h):h =_{Q[\kappa_A(g)/w]} d_{\kappa_A}(g, h)}\esh-\mathrm{elim}3$$

$$\frac{\Xi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi \vert \Gamma, w:\esh A \vdash Q \; \mathrm{type} \quad \Xi \vert \Gamma \vdash g:R \to \esh A \quad \Xi \vert \Gamma \vdash x:R \quad \Xi \vert \Gamma \vdash h:Q[g(x)/w]}{\Xi \vert \Gamma \vdash d_{\kappa_A'}(g, h):Q[\kappa_A'(g)/w]}\esh-\mathrm{elim}4$$

$$\frac{\Xi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi \vert \Gamma, w:\esh A \vdash Q \; \mathrm{type} \quad \Xi \vert \Gamma \vdash x:\esh A \quad \Xi \vert \Gamma \vdash y:Q[x/w]}{\Xi \vert \Gamma \vdash d_{\iota_A'}(y, x):y =_{Q[\kappa_A'(\mathrm{const}_{\esh A, R}(x))/w]} d_{\kappa_A'}(\mathrm{const}_{\esh A, R}(x), \mathrm{const}_{\esh A, R}(y))}\esh-\mathrm{elim}5$$

* Computation rules for weak and strict shape types:

$$\frac{\Xi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi \vert \Gamma, w:\esh A \vdash Q \; \mathrm{type} \quad \Xi \vert \Gamma \vdash x:A \quad \Xi \vert \Gamma, y:\esh A \vdash f:Q}{\Xi \vert \Gamma \vdash f[\sigma_A(x)/y] \equiv d_{\sigma_A}(x):Q[\sigma_A(x)/w]}\esh-\mathrm{comp}\mathrm{strict}1$$

$$\frac{\Xi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi \vert \Gamma, w:\esh A \vdash Q \; \mathrm{type} \quad \Xi \vert \Gamma \vdash x:A \quad \Xi \vert \Gamma, y:\esh A \vdash f:Q}{\Xi \vert \Gamma \vdash \beta_\esh^1(x):f[\sigma_A(x)/y] =_{Q[\sigma_A(x)/w]} d_{\sigma_A}(x)}\esh-\mathrm{comp}\mathrm{weak}1$$

...

The shape modality is an example of a [[higher inductive type]] which states that the [[shape modality]] of a type $A$ $\esh(A)$ is the [[localization of a type|localization]] $L_{R^1}(A)$ of $A$ at the function $\mathrm{const}:A \to (R \to A)$, equivalent to $\mathrm{const}':(1 \to A) \to (R \to A)$. Weak shape modalities are primarily used in cohesive [[objective type theories]], while strict shape modalities are typically used in cohesive type theories with [[judgmental equality]], such as cohesive [[Martin-Löf type theory]] ([[cohesive homotopy type theory]] or cohesive [[higher observational type theory]]. 

## Properties

### Preservation of some $\infty$-fiber products
 {#PreservationOfSomeHomotopyFiberProducts}

The shape operation is defined to [[preserved limit|preserve]] [[finite products|finite]] [[homotopy products]] and small [[(infinity,1)-colimits|homotopy colimits]] (being a [[left adjoint]]) but it does not preserve general [[(infinity,1)-limits|homotopy limits]], not even all [[homotopy pullbacks]]:

\begin{example}
**(shape does not preserve homotopy fibers of points over positive-dimensional smooth spheres)**
\linebreak
  For $n \in \mathbb{N}_+$ consider the [[n-sphere|$n$-sphere]] in its standard incarnation as a [[smooth manifold]] (or just as a [[D-topological space]]) and as such as a [[0-truncated]] [[smooth infinity-groupoid|smooth $\infty$-groupoid]]
$$
  S^n_{smth} \,\in\, SmthMfd \hookrightarrow SmthGrpd_\infty
  \,.
$$ 
This is such that the shape is the $n$-sphere as a geometrically [[discrete object|discrete]] higher [[homotopy type]]
$$
  \esh S^n_{smth} \,\simeq\, S^n \,\in\,
  Grpd_\infty 
  \xhookrightarrow{Disc} 
  SmthGrpd_{\infty}.
$$

Now for $x \colon \ast \to S^n_{smth}$ any point (and using that $\esh \ast \,=\, \ast$ by the condition that $\esh$ preserves [[finite products]]):

1. its [[fiber product]] over $S^n_{smth}$ may be computed in [[SmthMfd]] and hence is that same point:

1. its [[homotopy fiber product]] over $S^n = \esh S^n_{smth}$ is the [[loop space]] $\Omega S^n$, which (under our assumption that $n$ is a [[positive number]]) is far from equivalent to the point (for example: $\Omega S^1 \,\simeq\, \mathbb{Z}$).

Hence

$$
  n \in \mathbb{N}_+
  \;\;\;\;
  \vdash
  \;\;\;\;
  \ast
  \;\simeq\;
  \esh
  \big(
    \ast 
     \underset
       {S^n_{smth}}
       {\times}
    \ast
  \big)
  \;\neq\;
  \big(
    (\esh\ast) 
     \underset
       {\esh S^n_{smth}}
       {\times}
    (\esh\ast) 
  \big)
  \;\simeq\;
  \Omega S^{n}
  \,.
$$
\end{example}

However, the shape modality does preserve some useful classes of homotopy fiber products after all:

#### General

\begin{prop}\label{CohesiveShapePreservesLoopingOfDeloopings}
**(cohesive shape preserves looping and delooping)** 
\linebreak  
For $\mathbf{H}$ a [[cohesive (infinity,1)-topos|cohesive $\infty$-topos]]
and $\mathbf{B}\mathcal{G} \,\in\, \mathbf{H}$ a pointed connected object, [[May recognition theorem|hence]] the [[delooping]] of an [[infinity-group|$\infty$-group]] $\mathcal{G} \,\in\, Grp(\mathbf{H})$, the cohesive shape modality preserves the [[looping]] homotopy fiber product:
$$
  \esh
  \big(
    \ast 
    \underset
     {\mathbf{B}\mathcal{G}}{\times}
    \ast
  \big)
  \;\;
  \simeq
  \;\;
    \ast 
    \underset
     {\esh \mathbf{B}\mathcal{G}}{\times}
    \ast
  \,.
$$
\end{prop}
\begin{proof}
  Since [[groupoid objects in an (∞,1)-topos are effective]], the [[delooping]] of an [[infinity-group|$\infty$-group]] is the simplicial [[(infinity,1)-colimit|$\infty$-colimit]] of the [[simplicial object]] $\mathcal{G}^{\times^\bullet}$ of [[finite products]] of $\mathcal{G}$. Since the shape operation [[preserved limit|preserves]] finite products and general colimits, it preserves the delooping:
$$
  \esh
  \mathbf{B}\mathcal{G}
  \;\simeq\;
  \esh
  \underset{\underset{n \in \mathbb{N}}{\longrightarrow}}
  {\lim}
  \mathcal{G}^{\times^n}
  \;\simeq\;
  \underset{\underset{n \in \mathbb{N}}{\longrightarrow}}
  {\lim}
  \big(
    \esh
    \mathcal{G}
  \big)^{\times^n}
  \;\simeq\;
  \mathbf{B} \esh \mathcal{G}
  \,.
$$
Finally, using again that [[groupoid objects in an (∞,1)-topos are effective]], the claim follows:
$$
  \esh
  \big(
    \ast
     \underset{\mathbf{B}\mathcal{G}}{\times}
    \ast
  \big)
  \;\simeq\;
  \esh
   \mathcal{G}
  \;\simeq\;
  \esh
  \big(
    \ast
     \underset{\esh\mathbf{B}\mathcal{G}}{\times}
    \ast
  \big)
  \,.
$$
\end{proof}

\begin{prop}\label{ShapePreservesHomotopyFibersOverDiscreteObjects}
**(cohesive shape preserves homotopy fiber products over discrete objects)**
\linebreak
  If $\mathbf{H}$ is a [[cohesive (infinity,1)-topos|cohesive $\infty$-topos]] [[base (infinity,1)-topos|
over]] [[Infinity-Grpd|$Grpd_\infty$]], then its [[shape modality]] [[preserved limit|preserves]] [[homotopy fiber products]] over [[discrete objects]].
\end{prop}
The following argument follows [[schreiber:differential cohomology in a cohesive topos|dcct, Thm. 3.8.19]], which in turn follows discussion with [[Mike Shulman]]. The diagram is taken from the writeup of the proof given in [[schreiber:Equivariant principal infinity-bundles|SS21, Prop. 3.38]].
\begin{proof}
By a version of the [[(infinity,1)-Grothendieck construction|$\infty$-Grothendieck construction]] ([Beardsley & Péroux 2022, Lem. 3.10](infinity1-Grothendieck+construction#BeardsleyPéroux22)), a [[slice (infinity,1)-topos|slice $\infty$-topos]] over the [[inverse image]] of a plain [[infinity-groupoid|$\infty$-groupoid]] $B$ is [[equivalence of (infinity,1)-categories|equivalent]] to the [[(infinity,1)-category of (infinity,1)-functors|$\infty$-category of $\infty$-functors]] $B \to \mathbf{H}$. This way, the [$B$-sliced adjunction](adjoint+infinity1-functor#OnSlices) $Shp \dashv Dscr$ is seen to be of the following form:
\begin{tikzcd}[column sep=20pt]
    \mathrm{Fnctr}
    \big(
      B
      ,\,
      \mathbf{H}
    \big)
    \ar[
      from=rrrrrr,
      rounded corners,
      to path={
           ([yshift=0pt]\tikztostart.south)
        -- ([yshift=-12pt]\tikztostart.south)
        -- node[yshift=-6.8pt]{ \scalebox{.8}{$
               \mathrm{Fnctr}
                 (B, \mathrm{Dscr})
           $} }
           ([yshift=-12pt]\tikztotarget.south)
        -- ([yshift=-00pt]\tikztotarget.south)
      }
    ]
    \ar[
      rrrrrr,
      rounded corners,
      to path={
           ([yshift=0pt]\tikztostart.north)
        -- ([yshift=+12pt]\tikztostart.north)
        -- node[yshift=+6.8pt]{ \scalebox{.8}{$
             \mathrm{Fnctr}
               (B,\mathrm{Shp})
           $} }
           ([yshift=+12pt]\tikztotarget.north)
        -- ([yshift=-00pt]\tikztotarget.north)
      }
    ]
    &[-24pt]
    \simeq
    &[-24pt]
    \mathbf{H}_{/\mathrm{Dscr}(B)}
    \ar[
      rr,
      shift left=7pt,
      "\mathrm{Shp}_{/B}"
    ]
    \ar[
      from=rr,
      shift left=7pt,
      "{\mathrm{Dscr}_{/B}}"
    ]
    \ar[
      rr,
      "{\scalebox{.8}{$\bot$}}",
      phantom
    ]
    &&
    \big(
      \mathrm{Grpd}_{\infty}
    \big)_{/B}
    &[-24pt]\simeq&[-24pt]
    \mathrm{Fnctr}
    \big(
      S
      ,\,
      \mathrm{Grpd}_\infty
    \big)
    \,.
\end{tikzcd}

Now $Fnctr(B,Shp)$ preserves [[binary products]] as soon as $Shp$ does (because products of presheaves are computed objectwise). But binary products in the equivalent slice category $\mathbf{H}_{/B}$ are the homotopy fiber products in question, and hence the claim follows.
\end{proof}

\begin{prop}\label{ShapePreservesHomotopyFibersOfMapsFromDiscreteToDeloopedObjects}
**(shape preserves homotopy fibers of maps from discrete to delooped objects)**
\linebreak
  For $\mathbf{H}$ is a [[cohesive (infinity,1)-topos|cohesive $\infty$-topos]] [[base (infinity,1)-topos|
over]] [[Infinity-Grpd|$Grpd_\infty$]] the shape modality preserves the [[homotopy fibers]] of morphisms 

$$
  f \,\colon\, X \longrightarrow \mathbf{B}\mathcal{G}
$$

* from any [[discrete object]] $X \,\in\, Grpd_\infty \xhookrightarrow{Dscr} \mathbf{H}$ 

* to any [[delooping|delooped]] object $\mathbf{B}\mathcal{G} \,\in\, \mathbf{H}$

in that

$$
  \esh
  fib(f)
  \;\simeq\;
  fib\big( \esh f \big)
  \,.
$$

\end{prop}
\begin{proof}
Since a discrete $\infty$-groupoid $X$ is the [[coproduct]] of its [[connected components]], and since coproducts are [[preserved colimit|preserved]] by [[homotopy pullback]] (due to [[universal colimits]] in an [[(infinity,1)-topos|$\infty$-topos]]) and by the shape modality (being a [[left adjoint]]), we may assume without restriction of generaliity that also $X$ is connected, hence $X \,\simeq\,B \mathcal{K}$ with $\ast \twoheadrightarrow B\mathcal{K}$ an [[effective epimorphism in an (infinity,1)-category|effective epimorphism]].

First, observe that the [[pasting law for homotopy pullbacks]] gives the pasting diagram of [[homotopy pullbacks]] shown on the left below:

$$
  \array{
    \mathcal{G}
    &\longrightarrow&
    fib(f)
    &\longrightarrow&
    \ast
    \\
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow
    \\
    \ast
    &\twoheadrightarrow&
    B\mathcal{K}
    &\underset{f}{\longrightarrow}&
    \mathbf{B}\mathcal{G}
  }
  \;\;\;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;\;\;
  \array{
    \esh \mathcal{G}
    &\longrightarrow&
    \esh fib(f)
    &\longrightarrow&
    \ast
    \\
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow
    \\
    \ast
    &\twoheadrightarrow&
    B\mathcal{K}
    &\underset{\esh f}{\longrightarrow}&
    B\mathcal{G}
    \mathrlap{\,.}
  }
$$

Now, as shown on the right, the shape modality

1. preserves the left pullback square and its bottom effective epimorphism, by Prop. \ref{CohesiveShapePreservesLoopingOfDeloopings};

1. preserves the outer pullback rectangle by Prop. \ref{ShapePreservesHomotopyFibersOverDiscreteObjects}.

Therefore also the square on the far right is homotopy Cartesian, by the "reverse pasting law" ([this Prop.](pasting+law+for+pullbacks#ReversePastingLawForInfinityGroupoids)). But this is equivalently the claim to be shown.
\end{proof}

\linebreak


#### More specific cases
 {#MoreSpecificCases}

The following discussion is about the topological/smooth shape modality commuting with [[looping]] ([[homotopy fiber products]] of points) of [[mapping stacks]] between [[delooping]] stacks of certain [[topological groups]]. This is a technical point of crucial importance in the construction and discussion of [[equivariant classifying spaces]] for [[equivariant principal bundles]] -- though not traditionally presented as being about behaviour under a shape modality. The following perspective is from [[schreiber:Equivariant principal infinity-bundles|SS21]], though the hard results themselves are either classical (essentially [Conner & Floyd 1964, Lemma 31.8](nearby+homomorphisms+from+compact+Lie+groups+are+conjugate#ConnerFloyd64) for the case of compact $\Gamma$) or, in more generality, due to [Uribe & Lück 2014](equivariant+bundle#UribeLück14). (Beware that the following differs from their notation by the exchange "$G$" $\leftrightarrow$ "$\Gamma$"! For us here, $G$ denotes the [[equivariance group]] and $\Gamma$ the [[structure group]].)

\linebreak

\begin{defn}\label{ConditionHOnFamiliesOfGroupHomomorphisms}
**(Condition H on families of topological group homomorphisms)**
\linebreak
  Let $G, \Gamma \,\in\, Grp(kTop)$ be [[topological groups]] and let 
$$
  \mathcal{R} 
    \,\subset\, 
  \underset{
    H \subset G
  }{\coprod}
  Hom(H,\Gamma)
$$ 
be a [[set]] of [[pairs]] $(H,\rho)$ consisting of a topological [[subgroup]] $H$ of $G$ and a [[continuous map|continuous]] [[homomorphism]] $H \to \Gamma$ such that 
([Uribe & Lück 2014, Def. 3.4](equivariant+bundle#UribeLück14)) $\mathcal{R}$ is closed under:

1. [[fiber products]], i.e. under products in $Grp(kTop)_{/\Gamma}$,

1. [[conjugation]] by $\Gamma$ (under postcomposition),

1. [[conjugation]] by $G$ (under precomposition).

We say (with [Uribe & Lück 2014, Def. 6.1](equivariant+bundle#UribeLück14)) that such data satisfies *Condition H* if for all $(H,
\rho) \,\in\, \mathcal{R}$ we have:

1. the [[path component]] of $\rho$ in $HomMap(H,\Gamma)$ is contained in its [[orbit]] under the $\Gamma$-[[conjugation action]]:

   $$
     HomMap(H,\Gamma)_{\rho}
     \;\;
     \subset
     \;\; 
     \Gamma(\rho)
     \;\coloneqq\;
     \big\{
       Ad_\gamma \circ \rho
       \;\big\vert\;
       \gamma \in \Gamma
     \big\}
   $$

1. the [[coset space]]-[[coprojections]]

   1. $G \longrightarrow G/H$

   1. $\Gamma \longrightarrow \Gamma/Stab_\Gamma(\rho)$

      (by the the [[stabilizer subgroup]] $Stab_{\Gamma}(\rho) \subset \Gamma$ under the [[conjugation action]])

   [[coset space coprojection admitting local sections|admit local sections]].

1. the map

   $$
     \array{
       \Gamma/Stab_\Gamma(\rho) 
       &\longrightarrow&
       HomMap(H,\Gamma)
       \\
       [\gamma] &\mapsto& Ad_\gamma \circ \rho 
     }
   $$ 
  
   is a [[homeomorphism]] onto its [[image]].

\end{defn}
\begin{example}
 \label{ExamplesOfCollectionsOfTopologicalGroupHomsSatisfyingConditionH}
  Examples of families of topological group homomorphisms satsifying *Condition H* (Def. \ref{ConditionHOnFamiliesOfGroupHomomorphisms}) include the following:

1. $\Gamma$ and $G$ any [[Lie groups]] with $\Gamma$ [[almost connected topological group|almost connected]]

   with $\mathcal{R}$ consisting of all [[compact topological group|compact]] subsgroups $H \subset G$ and all their homomorphisms $H \to \Gamma$

   (established in [Uribe & Lück 2014, Thm. 6.3](equivariant+bundle#UribeLück14))

1. $\Gamma =$ [[PU(ℋ)]] and $G$ any [[finite group]]

   with $\mathcal{R}$ consisting of all subgroups $H \subset G$ and all their homomorphisms $H \to 
PU(\mathcal{H})$

   (established in [Uribe & Lück 2014, Sec. 15](equivariant+bundle#UribeLück14))

\end{example}

For the following formulation of the main result of [Uribe & Lück 2014](equivariant+bundle#UribeLück14) in terms of cohesive homotopy theory we use the [[continuous diffeology]]
$$
  kTop
  \xrightarrow{CDfflg}
  DiffSp
  \hookrightarrow
  SmthGrp_\infty
$$
and the fact that this preserves shapes and shapes of [[mapping spaces]] (see the introduction of [[schreiber:Equivariant principal infinity-bundles|SS21]]).
 
\begin{proposition}
**(shape commutes with looping of mapping stacks between delooping stacks of certain pairs of topological groups)**
\linebreak
For 

* $G$ a [[finite group]] 

* $\Gamma$ a [[compact Lie group]] or [[PU(ℋ)]], 

we have for all [[homomorphisms]] $\rho \,\colon\, H \to \Gamma$ from [[subgroups]] $H \subset G$ that the shape modality commutes with the [[looping]]-operation on the [[mapping stack]] between the [[deloopings]] of $H$ and $\Gamma$ in [[smooth infinity-groupoids|$SmoothGrpd_{\infty}$]]:
$$
  \esh
  \Omega_\rho 
  Map
  \big( 
    \mathbf{B}H
    ,\,
    \mathbf{B}\Gamma
  \big)
  \;\;
  \simeq
  \;\;
  \Omega_\rho 
  \esh
  Map
  \big( 
    \mathbf{B}H
    ,\,
    \mathbf{B}\Gamma
  \big)
  \,.
$$
\end{proposition}
\begin{proof}
First notice (e.g. from the discussion at *[[stabilizer subgroup]]*, [here](stabilizer+group#GeneralAbstract)) that
\[
  \label{ConjugationStabilizerSubgroupAsLoopingOfMappingStack}
  Stab_\Gamma(\rho)
  \;\simeq\;
  \Omega_\rho 
  Map
  \big(
    \mathbf{B}H
    ,\,
    \mathbf{B}\Gamma
  \big)
\]

From the discussion at *[[equivariant principal bundles]]* we have, under the given assumptions, that
$$
  B_G \Gamma
  \;\;\;
  \colon
  \;\;\;
  G/H 
  \;\mapsto\;
  \esh
  \,
  Map
  \big(
    \mathbf{B}H
    ,\,
    \mathbf{B}\Gamma
  \big)
$$
is the $G$-[[equivariant homotopy type]] of the $G$-[[equivariant classifying space]] of $\Gamma$. 

(For $\Gamma$ compact Lie this is the [Murayama-Shimakawa result](equivariant+bundle#UniversalEquivariantPrincipalBundles) as reviewed in [Guillou, May & Merling 2017, Thm. 3.1](equivariant+bundle#GuillouMayMerling17), while for $\Gamma = PU(\mathcal{H})$ this is due to [Bárcenas, Espinoza, Joachim & Uribe 2012](equivariant+bundle#BEJU14), with a re-derivation in a more explicitly cohesive context in [[schreiber:Equivariant principal infinity-bundles|SS21]]).

Moreover, by Exp. \ref{ExamplesOfCollectionsOfTopologicalGroupHomsSatisfyingConditionH} both cases satisfy *Condition H* (Def. \ref{ConditionHOnFamiliesOfGroupHomomorphisms}), whence the main result [Uribe & Lück 2014, Sec. 13](equivariant+bundle#UribeLück14) applies, which, using the above identification of the equivariant classifying space, gives a [[weak homotopy equivalence]] of the form

$$
  \underset{
     { [\rho] \in }
     \atop
     { Hom(H,\Gamma)/\Gamma }
  }{\coprod}
  B Stab_\Gamma(\rho)
  \;\;\;
  \simeq
  \;\;\;
  \esh 
  Map
  \big(
    \mathbf{B}H
    ,\,
    \mathbf{B}\Gamma
  \big)
  \,.
$$

(For $\Gamma$ a [[Lie group]] this is the classical fact that [[nearby homomorphisms from compact Lie groups are conjugate]].)

Observing that $B Stab_\Gamma(\rho) \,\simeq\, \mathbf{B} \esh Stab_\Gamma(\rho)$, the looping of this equivalence at the basepoint given by $\rho$ yields the claim.
\end{proof}


\linebreak











### Relative shape and factorization system

Generally, given an [[(∞,1)-topos]] $\mathbf{H}$ (or just a 1-[[topos]]) equipped with an [[idempotent monad]] $\esh \colon \mathbf{H} \to \mathbf{H}$ (a [[modal type theory|(higher) modality]]/[[closure operator]]) which preserves [[(∞,1)-pullbacks]] over objects in its [[essential image]], one may call a [[morphism]] $f \colon X \to Y$ in $\mathbf{H}$ _$\esh$-closed_ if the [[unit of an adjunction|unit]]-diagram

$$
  \array{
    X 
    &\overset{\eta_X}{\longrightarrow}& \esh(X)
    \\
    \big\downarrow {\mathrlap{{}^f}} 
    && 
    \big\downarrow{\mathrlap{{}^{\esh(f)}}}
    \\
    Y 
    &
    \overset{\eta_Y}{\longrightarrow}
    & 
    \esh(Y)
  }
$$

is an [[(∞,1)-pullback]] diagram. These $\esh$-closed morphisms form the right half of an [[orthogonal factorization system]], the left half being the morphisms that are sent to [[equivalence in an (∞,1)-category|equivalences]] in $\mathbf{H}$.




+-- {: .num_defn}
###### Definition

Let $(\Pi\dashv \Disc\dashv \Gamma):H\to\infty\Grpd$ be an [[infinity-connected (infinity,1)-topos]], let $\esh:=\Disc \Pi$ be the geometric path functor / geometric homotopy functor, let $f:X\to Y$ be a $H$-morphism, let $c_{\esh} f$ denote the ∞-pullback


$$
  \array{
    c_{\esh} f
    &\longrightarrow& 
    {\esh} X
    \\
    \big\downarrow
    &&
    \big\downarrow^{\mathrlap{{\esh}_f}}   
    \\
    Y
    &\xrightarrow{1_{(\Pi\dashv \Disc)}}
    &
    {\esh}Y
  }
$$

$c_{\esh} f$ is called $\esh$**-closure of** $f$.

$f$ is called $\esh$**-closed** if $X\simeq c_{\esh}f$.
=--

If a morphism $f:X\to Y$ factors into $f=g\circ h$ and $h$ is a $\esh$-equivalence then $g$ is $\esh$-closed; this is seen by using that $\esh$ is idempotent.



$\Pi$-closed morphisms are a right class of an [[orthogonal factorization system]] ([[orthogonal factorization system in an (∞,1)-category|in an (∞,1)-category]]) and hence, as discussed there, are closed under [[limits]], [[composition]], [[retracts]] and satisfy the left cancellation property.

\begin{remark}
**(shape-modal maps as open maps)**
\linebreak
A consequence of the previous property is that the class of $\esh$-closed morphisms gives rise to an admissible structure in the sense of [[structured (infinity,1)-topos|structured spaces]] on an (∞,1)-connected (∞,1)-topos, hence they serve as a class of a kind of *[[open maps]]*.
\end{remark}

### Shape via cohesive path ∞-groupoid

See at _[[shape via cohesive path ∞-groupoid]]_.




## Examples

### Internal locally constant $\infty$-stacks
 {#LocallyConstantStacks}

In a [[cohesive (∞,1)-topos]] $\mathbf{H}$ with an [[∞-cohesive site]] of definition, the [[fundamental ∞-groupoid]]-functor $\esh$ satisfies the above assumptions (this is the example gives this entry its name). The $\esh$-closed morphisms into some $X \in \mathbf{H}$ are canonically identified with the [[locally constant ∞-stacks]] over $X$. The correspondence is effectively what is called [[categorical Galois theory]].

+-- {: .num_prop}
###### Proposition

Let $H$ be a [[cohesive (∞,1)-topos]] possessing a [[∞-cohesive site]] of definition.
Then for $X\in H$ the locally constant ∞-stacks $E\in \L\Const(X)$, regarded as ∞-bundle morphisms $p:E\to X$ are precisely the $\esh$-closed morphisms into $X$

=--


### Formally &#233;tale morphisms
 {#EtaleMorphisms}

In a [[differential cohesive (∞,1)-topos]] $\mathbf{H}_{th}$, the [[de Rham space]] functor $\Im$ satisfies the above assumptions. The $\Im$-closed morphisms are precisely the [[formally étale morphisms]].

## Related entries

* [[shape]], [[shape of an (∞,1)-topos]]

* [[shape via cohesive path ∞-groupoid]]

* [[reflective subuniverse]]

[[!include cohesion - table]]

* [differential cohesion - cotangent bundles](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+infinitesimal+cohesion#CotangentBundles)


## References

### General

Original discussion:

* [[Urs Schreiber]], [[Zoran Škoda]]: [§7.4.2](https://arxiv.org/pdf/1004.2472.pdf#page=31) of: *Categorified symmetries* &lbrack;[arXiv:1004.2472](https://arxiv.org/abs/1004.2472)&rbrack;

* [[Urs Schreiber]], Sec. 3.4.5 in: _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](https://arxiv.org/abs/1310.7930))

* {#Shulman15} [[Mike Shulman]], Sec. 9.7 in: _Brouwer's fixed-point theorem in real-cohesive homotopy type theory_, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

### In Smooth∞Grpd

For the case of [[Smooth∞Grpd]]:

On [[shape via cohesive path ∞-groupoids]]:

* {#Pavlov14} [[Dmitri Pavlov]], _Structured Brown representability via concordance_, 2014 ([pdf](https://dmitripavlov.org/concordance.pdf), [[Pavlov_Concordance.pdf:file]])

* {#BEBP19} [[Daniel Berwick-Evans]], [[Pedro Boavida de Brito]], [[Dmitri Pavlov]], _Classifying spaces of infinity-sheaves_ ([arXiv:1912.10544](https://arxiv.org/abs/1912.10544))

Discussion for [[orbifolds]], [[étale groupoids]] and, generally, [[étale ∞-groupoids]]:

* {#Carchedi15} [[David Carchedi]], _On The Homotopy Type of Higher Orbifolds and Haefliger Classifying Spaces_ ([arXiv:1504.02394](http://arxiv.org/abs/1504.02394))





[[!redirects Pi-closed morphisms]]

[[!redirects cohesive shape]]
[[!redirects cohesive shapes]]

[[!redirects Pi modality]]
[[!redirects Pi-closed morphism]]

