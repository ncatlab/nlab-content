
$\mathfrak{osp}(1{|}2)$

  $\mathbf{V}Func(\mathcal{X},\,\mathbf{C})$ for the $\mathbf{V}$-[[enriched functor category]] from $\mathcal{X}$ to $\mathbf{C}$,

* for any $\mathbf{V}$-enriched functor $f \,\colon\, \mathcal{X} \longrightarrow \mathcal{Y}$:


   \[
     \label{PreimagesInAPullbackDiagram}
     \begin{array}{l}
     \beta \circ \psi^{-1}\big(\{c'\})\big
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
       \,,
       \phi(d) = \alpha(c')
     \big\}
     \end{array}
   \]


$$
  f_! f^\ast (X)
  \;\simeq\;
  f_!( f^\ast X \otimes f^\ast \mathbb{1} )
  \;\simeq\;
  X \times f_! f^\ast \mathbb{1}
$$


$$
  L^\ast \big( P(-,a) \cdot j \big)
  \;\simeq\;
  P\big(L(-),a\big) \cdot j
  \;\simeq\;
  P\big(-,R(a)\big) \cdot j
$$




$$
  f_!\big( 
    X \otimes f^\ast 1  \to f^\ast f_! X \otimes f^\ast 1
  \big)
  =
  f_!(X) \otimes (1 \to f_! f^\ast 1)
$$

$$
  \epsilon_{f_! X} \colon
  (f_! f^\ast 1 \to id) \otimes (f_! X)
  =
  f_! (f^\ast(1 \otimes f^\ast f_! X) \to f_! X
$$


## Examples

### Parameterized objects
 {#ParameterizedObjects}

We discuss a class of examples of integral model structures on categories of "$sSet$-parameterized objects in a category $\mathbf{C}$", namely of the [[Grothendieck constructions]] on [[indexed category|indexed]] [[enriched functor categories]] from the $\mathbf{V}$-[[enriched category]]-incarnation of a given simplicial set into a given $\mathbf{V}$-[[enriched category]] $\mathbf{C}$.

> under construction --- handle with care

Since we of course assume $\mathbf{C}$ to be a [[model category]] and hence in particular [[complete category|complete]] and [[cocomplete category|cocomplete]], these [[indexed categories]] have [[base change]] (along maps $f$ of base objects) by [[adjoint triples]] $f_! \dashv f^\ast \dashv f_\ast$ given by precomposition and left/right [[Kan extension]], respectively.
Depending on whether we equip the stage-wise [[enriched functor categories]] with the [[projective model structure on functors]] or the [[injective model structure on functors]], this yields two constructions of an integral model structure on the Grothendieck construction, which we discuss, respectively, as:

* the [projective version](#ParameterizedObjectsProjectiveVersion) using $f_! \dashv f^\ast$,

* the [injective version](#ParameterizedObjectsInjectiveVersion) using $(f_\ast)^{op} \dashv (f^\ast)^{op}$.

If $\mathbf{C}$ is in addition a [[monoidal enriched category|*monoidal* enriched category]] then the injective version of the integral model structure becomes itself a [[monoidal model category]] under the respective "[[external tensor product]], see

* the [monoidal version](#MonoidalModelStructureOnParameterizedObjects).


\begin{definition}\label{SetupAndNotationForParameterizedObjects}
**(Setup and notation)**
We consider:

* $\mathbf{C}$ a [[combinatorial simplicial model category]]

  * all whose objects are cofibrant, and

  * whose [[sSet]]-[[tensoring]] comes from it being a category of [[simplicial objects]] in some [[cocomplete category]].

For

* $X \in sSet$ a [[simplicial set]]

with

* $\mathcal{G}(X) \in sGrpd$ denoting its [[Dwyer-Kan simplicial path groupoid]],

  (an [[sSet]]-[[enriched groupoid]] to be regarded as a [[small category|small]] [[sSet-enriched category]])

we write

$$
  \mathbf{C}^{\mathcal{G}(X)}
  \;\;
  \coloneqq
  sFunc
  \big(
    \mathcal{G}(X)
    ,\,
    \mathbf{C}
  \big)
$$
for the [[sSet]]-[[enriched functor category]] from $\mathcal{G}(X)$ to $\mathbf{C}$.

In general we denote the objects of these categories, which are [[dependent pairs]] $(\mathcal{X}, \mathscr{V})$, as

$$
  \mathscr{V}_{\mathcal{X}}
  \,\equiv\,
  \big(
    x \colon \mathcal{X} \,\mapsto\, \mathscr{V}_x
  \big)
  \;\in\;
  \mathbf{C}^{\mathcal{X}}
  \,.
$$

We denote the [[initial objects]]

* of $sSet$ or of $sGrpd$ by $\varnothing$

* of $\mathbf{C}$ by $0$;

* of $\mathbf{C}^{\mathcal{G}(X)}$ as $0_{\mathcal{G}(X)}$;

and so that

* of $\mathbf{C}_{sSet}$ by $0_{\varnothing} \,\in\, \underset{\simeq \{0_{\varnothing}\}}{\underbrace{\mathbf{C}^{\varnothing}}} \,\in\, \mathbf{C}_{sSet}$.


Now by

* [[precomposition]]$\;\mathcal{G}(f)^\ast \,\coloneqq\, (-) \circ \mathcal{G}(f)$

these categories arrange into an [[indexed category]], constituted by a [[contravariant functor|contravariant]] [[pseudofunctor]]
$$
  \array{
    \mathllap{
      \mathbf{C}^{\mathcal{G}(-)}
      \;\colon\;
    }
    sSet &\longrightarrow& Cat
    \\
    X
      &\mapsto&
    \mathbf{C}^{\mathcal{G}(X)}
    \\
    \Big\downarrow\mathrlap{{}^f}
    &&
    \Big\uparrow\mathrlap{
       {}^{\mathcal{G}(f)^\ast}
    }
    \\
    Y
    &\mapsto&
    \mathbf{C}^{\mathcal{G}(Y)}
  }
$$
whose [[Grothendieck construction]] we abbreviate by
\[
  \label{CategoryOfParameterizedObjects}
  \mathbf{C}_{sSet}
  \;\;
    \coloneqq
  \;\;
  \underset{X \in sSet}{\int}
  \mathbf{C}^{\mathcal{G}(X)}
  \,.
\]

We may think of this as the category of *objects of $\mathbf{C}$ parameterized over [[infinity-groupoids|$\infty$-groupoids]]*.


We will denote the components of morphisms in $\mathbf{C}_{sSet}$ as follows:
$$
  \begin{array}{ll}
  \text{i.e.}
  \;\;\;
  \phi_f
  \;\;\colon\;\;
  \mathscr{V}_{\mathcal{G}(X)}
  \longrightarrow
  \mathscr{V}_{\mathcal{G}(Y)}
  &
  \text{means that}
  \;\;\;
  \begin{array}{cccc}
    \phi
    &\colon&
    \mathscr{V}_{\mathcal{G}(X)}
    &\overset{}{\longrightarrow}&
    \mathcal{G}(f)^\ast
    \big(
      \mathscr{W}_{\mathcal{G}(Y)}
    \big)
    \\
    f
    &\colon&
    \mathcal{X}
    &\overset{}{\longrightarrow}&
    \mathcal{Y}
    \mathrlap{\,,}
  \end{array}
  \end{array}
$$
the point being that the component $\phi$ is a map into the pullback functor, as opposed to one of its [[adjuncts]], which instead we will denote "$\widetilde{\phi}$".
\end{definition}

\begin{remark}
  The [[sSet]]-[[enriched functor category]] over any [[sSet]]-[[enriched groupoid]] $\mathcal{X}$ is [[adjoint equivalence of categories|adjoint equivalent]] to a [[cartesian product]] of [[enriched functor categories]] on the [[simplicial group actions]] of the [[connected components]], each of which may be identified with a category of [[simplicial group actions]] on objects in $\mathbf{C}$, by the discusison [here](simplicial+groupoid#RelationToSimplicialGroups):
$$
  \mathbf{C}^{\mathcal{G}(X)}
  \;\simeq\;
  \underset{i \in \pi_0(X)}{\prod}
  \big(
    \mathcal{G}(X)(x_i,x_i)
  \big)Act(\mathbf{C})
  \,.
$$
\end{remark}

The assumption in Def. \ref{SetupAndNotationForParameterizedObjects} that all objects in $\mathbf{C}$ are [[cofibrant object|cofibrant]] is quite strong (we need this in the analysis of the pushout (eq:PushoutExpressionForLeftInducedAction) below) but it is satisfied in a couple of interesting examples:

\begin{example}
\label{ExamplesOfModelStructureOnsSgrpdParametrizedObjects}
Situations in which the assumptions of Def. \ref{SetupAndNotationForParameterizedObjects} are verified and the homotopy theories which result by the discussion below include the following:

1. The choice

   * $\mathbf{C} \,\equiv\, sSet_{Qu}$

   yields (another proof of) [Harpaz & Prasma (2015), Prop. 6.2.1](#HarpazPrasma15) generalized from [[delooping groupoids]] of [[simplicial groups]] to all [[simplicial groupoids]] (i.e. away from just connected base types --- which is a mild generalization in itself but crucial for equipping the resulting Grothendieck construction with [[closed monoidal category|closed monoidal]]-structure, see [below](#MonoidalModelStructureOnParameterizedObjects)).


1. The choice

   * $\mathbf{C} \,\equiv\, sCh_\bullet(k)$ 

   being the local model structure on the simplicial enhancement of the projective model structure on chain complexes over a field $k$ (from [this Prop.](model+structure+on+chain+complexes#LocalizedReedyModelStructureOnSimplicialUnboundedChainComplexes))

     (all whose objects are cofibrant, by [this Prop](model+structure+on+chain+complexes#OverGroundFieldAllObjectsInSimplicialStructureOnUnboundedComplexesAreCofibrant))

   yields a [[model category]]-structure for [[flat infinity-vector bundles|flat $\infty$-vector bundles]] ([[infinity-local systems|$\infty$-local systems]] or, [[stable Dold-Kan correspondence|equivalently]], [[parameterized spectrum|parameterized]] [[Eilenberg-MacLane spectrum|$H k$]]-[[module spectra]]) over varying base spaces.

\end{example}



#### Plain model structure

We establish integral model structures on parameterized objects under the above assumptions (Def. \ref{SetupAndNotationForParameterizedObjects}).


##### Projective version
 {#ParameterizedObjectsProjectiveVersion}

\begin{definition}
  For $X \in sSet$, we write
  $$
    \mathbf{C}^{\mathcal{G}(X)}_{proj}
    \;\coloneqq\;
    sFunc\big(
      \mathcal{G}
      ,\,
      \mathbf{C}
    \big)_{proj}
  $$
  for the [[projective model structure on functors]] which exists (and is [[combinatorial model category|combinatorial]]) by [this Prop.](model+structure+on+functors#Combinatorial).
\end{definition}

On the projective structure the pre-composition [[base change]]-functors $f^\ast$ are clearly [[right Quillen functors]] (cf. [this Prop.](model+structure+on+functors#QuillenFunctorialityInDomain)) so that their [[left adjoint]] [[left Kan extensions]] $f_!$ are [[left Quillen functors]]:

\begin{proposition}
  \label{ProjectiveModelStructureOnParameterizedObjects}
**(projective integral model structure on parameterized objects)**
\linebreak
In the situation of Def. \ref{SetupAndNotationForParameterizedObjects}, the [[pseudofunctor]]
$$
  \array{
    sSet &\longrightarrow& ModCat
    \\
    \mathcal{X}
      &\mapsto&
    \mathbf{C}^{\mathcal{G}(X)}_{proj}
    \\
    \Big\downarrow\mathrlap{{}^f}
    &&
   \Big\downarrow\mathrlap{{}^{\mathcal{G}(f)_!}}
    \\
    \mathcal{Y}
    &\mapsto&
    \mathbf{C}^{\mathcal{G}(Y)}_{proj}
  }
$$
is relative and proper (in the sense [above](#Definition)), hence the integral model structure (Prop. \ref{ExistenceStatement}) on the category of *parameterized $\mathbf{C}$ objects* (eq:CategoryOfParameterizedObjects)
$$
  \mathbf{C}_{sSet, proj}
  \;\;\coloneqq\;\;
  \underset{X \in sSet}{\int}
  \mathbf{C}^{\mathcal{G}(X)}_{proj}
$$
exists.
\end{proposition}
\begin{proof}
First to prove that the pseudofunctor is relative, here is a lazy argument (to be improved):
By general results in [[Higher Topos Theory]], the given pseudofunctor presents the [[(infinity,1)-functor|$\infty$-functor]]
$$
  \array{
    Grpd_\infty &\longrightarrow& Cat_\infty
    \\
    \mathcal{X}
      &\mapsto&
    Func_\infty\big(
     \mathcal{X}
     ,\,
     L^W \mathbf{C}
    \big)
    \mathrlap{\,.}
  }
$$
By passage to [[homotopy category of an (infinity,1)-category|homotopy categories]] and using functoriality it follows that for $f$ an [[equivalence in an (infinity,1)-category|equivalence]], so is the [[derived functor]] of $f_!$, whence $f_!$ is a left [[Quillen equivalence]]. This shows that the pseudofunctor is relative.

Right properness is immediate: Since the weak equivalences in the projective [[model structure on functors]] are objectwise, the precomposition functor $f^\ast$ preserves weak equivalences for all $f$.

It remains to argue left-properness. So given $f \colon X \to Y$ an acyclic cofibration of simplicial sets, we need to show that $\mathcal{G}(f)_!$ preserves all [[weak equivalences]].

We claim that that it is sufficent to check the statement over [[reduced simplicial sets]], hence the case where $\mathcal{G}(f)$ is a map of [[simplicial groupoid|simplicial]] [[delooping groupoids]] of the form
$$
  \mathcal{G}(f)
  \;=\;
  \mathbf{B}\phi
  \;\colon\;
  \mathbf{B}H
    \longrightarrow
  \mathbf{B}G
$$
with a single comonent map
$$
  \phi \,\coloneqq\, \mathcal{G}(f)_{x,x}
$$
being a [[homomorphism]] of [[simplicial groups]].

Namely, first of all it is clearly sufficient to check on connected components, and then for $\mathcal{G}(f) \,\colon\, \mathcal{G}(X) \to \mathcal{G}(Y)$ a morphism of connected [[sSet-enriched categories]], any choice of object $x \in Obj\big(\mathcal{G}(X)\big)$ (i.e. a [[vertex]] in $X$) gives a [[pullback square]]
$$
  \array{
    && \mathbf{B}\mathcal{G}(X)
    \\
    &
    \mathllap{{}^{\iota_x}}\swarrow
    &&
    \searrow\mathrlap{{}^{\mathcal{G}(f)_{x,x}}}
    \\
    \mathcal{G}(X)
      && &&
    \mathbf{B}\mathcal{G}(Y)_{f(x),f(x)}
    \\
    &
    \mathllap{{}_{ \mathcal{G}(f) }}\searrow
    &&
    \swarrow\mathrlap{{}_{\iota_{f(x)}}}
    \\
    && \mathcal{G}(Y)
  }
$$
whose associated [[Beck-Chevalley condition]] says that
$$
  (\iota_{f(x)})^\ast \circ f_!
  \;=\;
  (f_x)_! (\iota_{x})^\ast
  \,.
$$
But since the pullback operations preserve all weak equivalences (as already remarked above) and the weak equivalences over a connected simplicial groupoid are detected over any object (by discussion [here](simplicial+groupoid#BorelModelStructureOnSimplicialGroupActions))
this says that $f_!$ preserves weak equivalences at $x$ iff $(f_x)_!$ does.


Now in the case of a single-object simplicial groupoids, the [[sSet]]-[[enriched functors]] $\mathbf{B}H \to \mathbf{C}$ are equivalently $H$-[[simplicial group actions]] in $\mathbf{C}$. On such an [[action object]] $\rho \,\colon\, H \cdot X \longrightarrow X$ the functor $f_!$ is given, on [[underlying]] [[objects]], by 

##### Injective version
 {#ParameterizedObjectsInjectiveVersion}

\begin{definition}
  For $X \in sSet$, we write
  $$
    \mathbf{C}^{\mathcal{G}(X)}_{inj}
    \;\coloneqq\;
    sFunc\big(
      \mathcal{G}
      ,\,
      \mathbf{C}
    \big)_{inj}
  $$
  for the [[injective model structure on functors]] which exists (and is [[combinatorial model category|combinatorial]]) by [this Prop.](model+structure+on+functors#Combinatorial).
\end{definition}

On the injective structure the pre-composition [[base change]]-functors $f^\ast$ are clearly [[left Quillen functors]] (cf. [this Prop.](model+structure+on+functors#QuillenFunctorialityInDomain)) so that their [[right adjoint]] [[right Kan extensions]] $f_\ast$ are [[right Quillen functors]].

Just in order to be able to appeal to the existence statement of Prop. \ref{ExistenceStatement} we consider the corresponding [[opposite model structures]] since this reverses the handed-ness of the [[base change]]-[[Quillen adjunction|Quillen adjoints]] to

\begin{proposition}
  \label{InjectiveModelStructureOnParameterizedObjects}
**(injective integral model structure on parameterized objects)**
\linebreak
In the situation of Def. \ref{SetupAndNotationForParameterizedObjects}, the [[pseudofunctor]]
$$
  \array{
    sSet &\longrightarrow& ModCat
    \\
    \mathcal{X}
      &\mapsto&
    \big(\mathbf{C}^{\mathcal{G}(X)}_{inj}\big)^{op}
    \\
    \Big\downarrow\mathrlap{{}^f}
    &&
    \Big\downarrow\mathrlap{{}^{
      \mathcal{G}(f)^{op}_\ast}
    }
    \\
    \mathcal{Y}
    &\mapsto&
    \big(\mathbf{C}^{\mathcal{G}(Y)}_{inj}\big)^{op}
  }
$$
is relative and proper (in the sense [above](#Definition)), hence the integral model structure (Prop. \ref{ExistenceStatement}) on the category of *parameterized $\mathbf{C}$ objects* (eq:CategoryOfParameterizedObjects)
$$
  \mathbf{C}_{sSet, inj}
  \;\;\coloneqq\;\;
  \underset{X \in sSet}{\int}
  \mathbf{C}^{\mathcal{G}(X)}^{op}_{inj}
$$
exists.
\end{proposition}
\begin{proof}
  The proof of Prop.\ref{ProjectiveModelStructureOnParameterizedObjects} applies verbatim. Notice that the pushout (eq:PushoutExpressionForLeftInducedAction) now formed in an [[opposite category]] $\big(\mathbf{C}^{\mathcal{G}(X)}\big)$ corresponds to the corresponding [[pullback]] of [[powerings]] which expresses right [[induced actions]].
\end{proof}


\linebreak

#### Monoidal version
 {#MonoidalModelStructureOnParameterizedObjects}

> still incomplete and currently also incoherent... 

Now assume in addition that

1. $\mathbf{C}$ is in addition a [[symmetric monoidal category|symmetric]] [[monoidal simplicial model category]] with

  * [[tensor product]] denoted $(-) \otimes (-) \,\colon\, \mathbf{C} \times \mathbf{C} \to \mathbf{C}$

  * [[internal hom]] denoted $[-,-] \,\colon\, \mathbf{C}^{op} \times \mathbf{C} \to \mathbf{C}$

Then the injective model structures $\mathbf{C}^{\mathcal{G}(X)}_{inj}$ inherit [[monoidal model structure]] from the objectwise-tensor product in $\mathbf{C}$.

Since also the corresponding [[internal hom]] is formed objectwise, the pre-composition functors

$$
  \array{
    X &\overset{f}{\longrightarrow}& Y
    \\
    sFunc\big(
      \mathcal{G}(X)
      ,\,
      \mathbf{C}
    \big)
    &\overset{
     \big(
       \mathcal{G}(f)
     \big)^\ast
    }{\longleftarrow}&
    sFunc\big(
      \mathcal{G}(Y)
      ,\,
      \mathbf{C}
    \big)
  }
$$

are both [[strong monoidal functor|strong monoidal]] and [[strong closed functors]]. This should imply that

\begin{lemma}
\label{BeckChevalleyCondition}
  Our [[indexed monoidal category]]
  $$
    \array{
    sSet &\longrightarrow& MonCat
    \\
    X
      &\mapsto&
    \big(
      \mathbf{C}^{\mathcal{G}(X)}
      ,\,
      \otimes_{\mathcal{G}(X)}
      ,\,
      1_{\mathcal{G}(X)}
    \big)
    }
  $$
satisfies the [[Beck-Chevalley condition]].
\end{lemma}

\begin{definition}\label{ExternalTensorProduct}
**(external tensor product)**
\linebreak
  The *[[external tensor product]]* on $\mathbf{C}_{sSet}$ (eq:CategoryOfParameterizedObjects)

$$
  \boxtimes
  \;\colon\;
  \mathbf{C}_{sSet}
  \times
  \mathbf{C}_{sSet}
  \longrightarrow
  \mathbf{C}_{sSet}
$$

is defined first on morphisms covering [[identity morphisms]] over [[reduced simplicial sets]] by

$$
  \boxtimes
  \;\colon\;
  \mathbf{C}^{\mathcal{G}(X)}
  \times
  \mathbf{C}^{\mathcal{G}(Y)}
  \overset{
    \big(\mathcal{G}(pr_{X})\big)^\ast
    \times
    \big(\mathcal{G}(pr_{Y})\big)^\ast
  }{\longrightarrow}
  \mathbf{C}^{\mathcal{G}(X \times Y)}
  \times
  \mathbf{C}^{\mathcal{G}(X \times Y)}
  \overset{
    \Big(
      W\big(\mathcal{G}(Y)(\ast,\ast)\big)
      \cdot (-)
    \Big)
    \times
    \Big(
      W\big(\mathcal{G}(X)(\ast,\ast)\big)
      \cdot (-)
    \Big)
  }{\longrightarrow}
  \mathbf{C}^{\mathcal{G}(X \times Y)}
  \times
  \mathbf{C}^{\mathcal{G}(X \times Y)}
  \overset{
    \otimes
  }{\longrightarrow}
  \mathbf{C}^{\mathcal{G}(X \times Y)}
$$

and then in general by

$$
  \left[
  \array{
    \mathscr{V}_{\mathcal{G}(X)}
    \\
    \Big\downarrow\mathrlap{^{\phi_f}}
    \\
    \mathscr{W}_{\mathcal{G}(Y)}
  }
  \;\;\,
  \right]
  \boxtimes
  \left[
  \array{
    \mathscr{V}'_{\mathcal{G}(X')}
    \\
    \Big\downarrow\mathrlap{^{\phi'_{f'}}}
    \\
    \mathscr{W}'_{\mathcal{G}(Y')}
  }
  \;\;\;
  \right]
  \;\;
  \coloneqq
  \;\;
  \left[
  \array{
    \mathscr{V}_{\mathcal{G}(X)}
    \boxtimes
    \mathscr{V}'_{\mathcal{G}(X')}
    \\
    \Big\downarrow\mathrlap{{}^{\phi_f \boxtimes \phi'_{f'}}}
    \\
    \mathscr{W}_{\mathcal{G}(Y)}
    \boxtimes
    \mathscr{W}'_{\mathcal{G}(Y')}
  }
  \;\;\;\;
  \right]
$$
\end{definition}

\begin{lemma}
  The functor forming the [[external tensor product]] (Def. \ref{ExternalTensorProduct}) with a fixed object $\mathscr{V}'_{\mathcal{X}'} \,\in\, \mathbf{C}_{sSet}$
$$
  (-) \boxtimes \mathscr{V}'_{\mathcal{G}(X')}
  \;\colon\;
  \mathbf{C}_{sSet}
  \longrightarrow
  \mathbf{C}_{sSet}
$$
is a [[left Quillen functor]] on the injective integral model structure of Prop \ref{InjectiveModelStructureOnParameterizedObjects}.
\end{lemma}
The following proof notationally suppresses the tensorings $W\big(\mathcal{G}(X)(\ast,\ast)\big)\cdot(-)$. They just run along.
\begin{proof}
First to see that it is a [[left adjoint]]: By [this Prop.](external+tensor+product#CocontinuityAndAdjoints) it [[preserves colimits]] and by [this Prop.](locally+presentable+category#LocallyPresentableGrothendieckConstruction) our [[Grothendieck construction]]-category is [[locally presentable]], whence the existence of a [[right adjoint]] follows by the [[adjoint functor theorem]] ([this Prop.](adjoint+functor+theorem#AdjFuncTheoremForLocallyPresentableCats)).

The bulk of the work is to see that the external tensor preserves (acyclic) cofibrations:

For $\phi_f \;\colon\; \mathscr{V}_{\mathcal{X}} \to \mathscr{W}_{\mathcal{Y}}$ an (acyclic) integral cofibration,
we need to show that the adjunct of the component map

$$
  \big(
    (\mathrm{pr}_{\mathcal{X}})^\ast
    \phi
  \big)
  \otimes
  (f \times id)^\ast
  (pr_{\mathcal{X}'})^\ast
  id_{\mathscr{V}'}
$$

is an (acyclic) cofibration in $\mathbf{C}$. Here on the right we have inserted the operation $(f \times id)^\ast$ --- which we may since it equals the identity in its postcomposition with $(pr_{\mathcal{X}'})^\ast$. But with that term inserted, we may apply [[Frobenius reciprocity]] when computing the [[adjunct]] of this map as its image under $(f \times id)_!$ composed with the counit.

This formula for the adjunct is the total left morphism in the following commuting diagram. Here:

* the top left square is the [[naturality square]] of the [[projection formula]],

* the bottom left square is from [this Remark](Wirthmüller+context#ProjectionComposedWithCounitInRemainingVariable),

* the top right square is a [[Beck-Chevalley condition|Beck-Chevalley]] [[naturality square]] associated with the evident [[pullback]] square

  $$
    \array{
      & &
      X \times X'
      \\
      &
      \mathllap{{}^{pr_{X}}}\swarrow
      &&
      \searrow\mathrlap{^{f \times id}}
      \\
      X && && Y \times X'
      \\
      &
      \mathllap{{}_{f}}\searrow
     &&
       \swarrow\mathrlap{{}_{pr_{Y}}}
      \\
      &&
      Y
      \mathrlap{\,,}
    }
  $$


* the bottom right square expresses the equality of two ways of moving the zig-zag morphism through the [[pasting diagram]] further below to the top right, one direct and the other by first moving it to the bottom left, using that the pasting of the left two squares and that of the bottom three squares are isomorphisms.

<img src="/nlab/files/LemmaDiagram-230424b.jpg" width="800">

The upshot is that the adjunct morphism on the left of the big diagram above is isomorphic to the composite on the right. That composite on the right, however, is the adjunct of $\phi$ pulled back to a product space and tensored with the pullback of a object of $\mathbf{C}^{\mathcal{X}'}$.

Thus it remains to see that pullback along product projections preserves cofibrations... but actually this fails, one needs instead to pullback and then cofibrantly replace... am adjusting it...
\end{proof}
