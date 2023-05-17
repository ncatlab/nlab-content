
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Given a [[topological group]] $G$, the _Borel model structure_ is a [[model category]] structure on the [[category]] of [[topological G-spaces]], hence of [[topological spaces]] [[group object|equipped with]] [[continuous function|continuous]] [[group actions]].

Analogously, given a [[simplicial group]] $G_\bullet$, the _Borel model structure_ is a [[model category]] structure on the [[category]] of [[simplicial group actions]], hence of [[simplicial sets]] equipped with $G$-[[action]] 

Both of these present the [[(∞,1)-category]] of [[∞-actions]] of the [[∞-group]] (see there) presented by $G$.

In the context of [[equivariant homotopy theory]] this is also called the "coarse model structure" (e.g. [Guillou 2006, section 5](#Guillou06)), since in general it has more weak equivalences than the [[fine model structure on topological G-spaces]] that enters [[Elmendorf's theorem]].


## Definition

### In topological spaces

Throughout, write [[Top]] for the [[category]] of [[compactly generated weak Hausdorff spaces]].

\begin{definition}
  For $G \,\in\, Grp(TopSp)$ a [[topological group]], write

\[
  \label{BGAsTopEnrichedCategory}
  \mathbf{B}G \;\in\; TopCat
\]

for the [[Top]]-[[enriched category]] with a single [[object]] and $G$ as its unique [[hom-object]].
\end{definition}

\begin{remark}
  There is an evident [[isomorphism]] of [[enriched categories]]
  \[
    \label{IdentifyingTopologicalGSpacesWithTopEnrichedFunctors}
    G Act(TopSp)
    \;\simeq\;
    TopFnctr\big( \mathbf{B}G,\, TopSp \big)
  \]
  between [[topological G-spaces]] and the [[Top]]-[[enriched functor category]] from $\mathbf{B}G$ (eq:BGAsTopEnrichedCategory) to [[Top]] (topological presheves).
\end{remark}

\begin{prop}\label{BorelModelStructureOnTopologicalSpaces}
For $G \in Grp(TopSp)$ a [[topological group]] there is a [[model category]]-structure 

$$
  G Act\big(TopSp\big)_{proj}
  \;\;\;
  \in
  \;
  MdlCat
$$ 

on the [[category]] of [[topological G-spaces]] whose [[weak equivalences]] and [[fibrations]] are those [[morphisms]] whose [[underlying]] [[continuous functions]] are so in the  [[classical model structure on topological spaces]].
\end{prop}

For [[discrete groups]] this may be argued as in  [Guillou 2006, Thm. 5.1](#Guillou06). 
For general topological groups this follows as a special case of the [[projective model structure on enriched functors|projective model structure on Top-enriched functor]] (see [this Thm.](Introduction+to+Homotopy+Theory#ProjectiveModelStructureOnTopologicalFunctors)), under the identification $G Act(TopSp) \,\simeq\, TopFun( \mathbf{B}G, TopSp )$ (eq:IdentifyingTopologicalGSpacesWithTopEnrichedFunctors).


### In simplicial sets

\begin{defn}\label{BorelModelStructure}

For $G_\bullet$ a [[simplicial group]] write 

* $\mathbf{B}G_\bullet$ for the one-object [[sSet-enriched category]] (here: a [[simplicial groupoid]]) whose [[hom-object]] is $G_\bullet$. 

* $G_\bullet Actions(sSet) \;\coloneqq\; sSetCat\big(\mathbf{B}G_\bullet, sSet\big)$ for the [[sSet]]-[[enriched functor category]] to [[SimplicialSets]].

* $G_\bullet Acts\big(sSet_{Qu}\big)_{proj} \coloneqq sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj}$ for the projective [[model structure on functors]] (projective [[model structure on simplicial presheaves]]). 

This is the $G_\bullet$ *Borel model structure*, naturally a [[simplicial model category]] ([DDK 80, Prop. 2.4](#DDK80), [Goerss & Jardine 09, Chapter V, Thm. 2.3](#GoerssJardine09)).
\end{defn}

### In combinatorial simplicial model categories
 {#DefinitionInCombSimpModCat}

More generally, if $\mathbf{C}$ is an [[sSet-enriched category]] which is also [[tensoring|tensored]] over [[sSet]], via an [[enriched functor]]
$$
  sSet \times \mathbf{C} \longrightarrow \mathbf{C}   
  \,,
$$
then for $\mathcal{G} \in Grp(sSet)$ the [enriched hom-isomorphism](enriched+adjoint+functor#ViaHomIsomorphism) of the [[tensoring]] 

$$
  Hom\big( 
    \mathcal{G}
    ,\,
    \mathbf{C}(\mathscr{V},\,\mathscr{V})
  \big) 
  \;\;\simeq\;\;
  Hom\big(
    \mathcal{G} \cdot \mathscr{V}
    ,\,
    \mathscr{V}
  \big)
$$
shows that [[sSet]]-[[enriched functors]]
$$
  F 
    \,\colon\,
  \mathbf{B}\mathcal{G} \longrightarrow \mathbf{C}
$$
may equivalently be thought of as [[simplicial group actions]] 
$$
  \mathcal{G} \cdot \mathscr{V}
  \overset{\rho}{\longrightarrow}
  \mathscr{V}
$$
of $\mathcal{G}$ acting on [[objects]] $\mathscr{V} \coloneqq F(\ast)$ via [[tensoring]].

If now $\mathbf{C}$ is in fact a [[combinatorial simplicial model category]], then the respective projective [[model structure on functors]] exists ([that Prop.](model+structure+on+functors#ExistenceOfProjectiveStructureOnEnrichedFunctors)), which we may hence think of as the Borel model structure on $\mathcal{G}$-actions on objects of $\mathbf{C}$:
\[
  \label{BorelModelStructureForCombinatoriaSimplicialModelCat}
  \mathcal{G}Act(\mathbf{C})_{Borel}
  \,\coloneqq\,
  sFunc(\mathbf{B}\mathcal{G},\,\mathbf{C})_{proj}
  \,.
\]




## Properties

### In topological spaces
 {#PropertiesInTopologicalSpaces}

#### Cofibrations and Cofibrant replacement

\begin{prop}\label{CofibrantObjectsInTopologicalBorelModelStructure}
The model category $G Act\big(TopSp_{Qu}\big)_{proj}$ from Prop. \ref{BorelModelStructureOnTopologicalSpaces} is [[cofibrantly generated model category|cofibrantly generated]] with [[generating cofibrations]] being (see [this Def.](Introduction+to+Homotopy+Theory#GeneratingCofibrationsForProjectiveStructureOnFunctors)) the [[product topological space|product]] with $G$ (regarded with its free left multiplication action) of the generating cofibrations of [[classical model structure on topological spaces|$TopSp_{Qu}$]].
\end{prop}
For [[discrete group|discrete]] $G$ a statement along these lines appears as   [Guillou 2006, Prop. 5.3](#Guillou06).
\begin{proof}
This is a special case of [this Thm.](Introduction+to+Homotopy+Theory#ProjectiveModelStructureOnTopologicalFunctors) about topological functor categories.

Alternatively, the statement is a special case of that for the [[fine model structure on topological G-spaces]] for the case of trivial family of closed subgroups (see [there](fine+model+structure+on+topological+G-spaces#SpecializationToBorelModelStructure)).
\end{proof}



\begin{example}\label{ProductWithUniversalPrincipalGSpaceIsCofibrantReplacement}
  Since the [[universal principal bundle|universal principal space]] $E G$ (the [[topological realization]] $E G \,=\, \big\vert W G\big\vert$ of the [[universal principal simplicial complex]]) is

* [[contractible homotopy type|contractible]]: $E G \simeq_{whe} \ast$;

* equipped with a [[free action]] by $G$,

Prop. \ref{CofibrantObjectsInTopologicalBorelModelStructure} implies that the [[product]] with $E G$ in G Act(TopSp) (i.e. the [[product topological space]] with the induced [[diagonal action]]) serves as [[cofibrant replacement]] in $G Act(TopSp)$:

$$
  \varnothing
    \underset{\;\in Cof\;}{\longrightarrow}
  X \times E G
    \underoverset{\;\in W \cap Fib\;}{pr_1}{\longrightarrow}
  X
  \;\;\;
  \in
  G Act\big(TopSp_{Qu}\big)_{proj}
  \,.
$$
\end{example}

> Hm, this is not a proper argument... 


#### Topological Borel construction

\begin{prop}\label{QuotentQuillenAdjunctionBetweenGSpacesToSpaces}
  There is a [[Quillen adjunction]]
  $$
    TopSp_{Qu}
    \underoverset
      {\underset{triv}{\longrightarrow}}
      {\overset{(-)/G}{\longleftarrow}}
      {\bot}
    G Act\big(TopSp_{Qu}\big)_{proj}   
  $$
  between the [[classical model structure on topological spaces]] and the projective Borel model structure from Prop. \ref{BorelModelStructureOnTopologicalSpaces}, whose

* [[right Quillen functor]], $triv$, assigns [[trivial actions]];

* [[left Quillen functor]], $(-)/G$, assigns [[topological quotient spaces]] by the [[relation]] $G \times X \underoverset{pr_2}{\mathclap{(-)\cdot(-)}}{\rightrightarrows} X$.

\end{prop}
([Guillou 2006, Ex. 5.5](#Guillou06))
\begin{proof}
  By definition of the weak equivalences and fibrations in Prop. \ref{BorelModelStructureOnTopologicalSpaces}, it is immediate that $triv$ preserves these classes of morphisms.
\end{proof}

\begin{prop}\label{BorelConstructionOfFreeActionEquivalentToPlainQuotient}
**([[Borel construction]] of [[free action]] is [[weak homotopy equivalence|weak hom. equivalent]] to plain [[quotient space]])**
\linebreak
  Let $G$ be a [[compact Lie group]] and 
  let $X$ be a [[G-CW complex]] whose $G$-action is [[free action|free]]. Then the comparison morphism between the [[Borel construction]] and the plain [[quotient space]] of $X$ is a [[weak homotopy equivalence]]:

$$
  (X \times E G)/G 
  \xrightarrow{ \; 
    (id_x \times (E G \to \ast))/G \, \in\, W 
  \; }
  X/G
  \,.
$$
\end{prop}
\begin{proof}
  Since $E G$ is a [[G-CW complex]], the product $X \times E G$ is cofibrant (by the analog of [this Prop.](fine+model+structure+on+topological+G-spaces#MonoidalModelCategoryStructure)) and $X$ is cofibrant by assumption and by Prop. \ref{CofibrantObjectsInTopologicalBorelModelStructure}.

Hence, by Prop. \ref{QuotentQuillenAdjunctionBetweenGSpacesToSpaces}, the morphism in question is the image under a [[left Quillen functor]], of a weak equivalence between cofibrant objects. Therefore the claim follows by [[Ken Brown's lemma]] ([here](Introduction+to+Homotopy+Theory#KenBrownLemma)).
\end{proof}



\begin{prop}
  The [[Borel construction]] exhibits the [[left derived functor]] of the [[quotient space]]-[[left Quillen functor]] in Prop. \ref{QuotentQuillenAdjunctionBetweenGSpacesToSpaces}:

$$
  X \,\in\, A Act(TopSp)
  \;\;\;\;
    \Rightarrow
  \;\;\;\;
  \big(\mathbb{L}(-)/G\big)(X)
  \;\simeq\;
  \frac{E G \times X}{G}
  \;\;\;
  \in
  \;
  Ho\Big( G Act\big( TopSp_{Qu} \big)_{proj}  \Big)
  \,.
$$ 
\end{prop}
\begin{proof}
  Since the [[left derived functor]] of a left Quillen functor is given by the application of the latter on any [[cofibrant replacement]], the claim follows by Ex. \ref{ProductWithUniversalPrincipalGSpaceIsCofibrantReplacement}.
\end{proof}

> or would follow, if that Example were argued properly


### In simplicial sets

#### Cofibrant replacement and homotopy quotients/fixed points
 {#CofibrantReplacementAndHomotopyQuotientsFixedPoints}

\begin{prop}\label{CofibrationsOfSimplicialActions}
**(cofibrations of simplicial actions)** \linebreak
The cofibrations $i \colon X \to Y$ in $sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj}$ (Def. \ref{BorelModelStructure}) are precisely those morphisms such that

1. the underlying morphism of [[simplicial sets]] is a [[monomorphism]];

1. the $G_\bullet$-[[action]] is a relatively [[free action]], i.e. [[free action|free]] on all [[simplices]] not in the [[image]] of $i$.

\end{prop}

This is ([DDK 80, Prop. 2.2. (ii)](#DDK80), [Guillou 2006, Prop. 5.3](#Guillou06), [Goerss & Jardine 09, V Lem. 2.4 & Cor. 2.10](#GoerssJardine09)).



\begin{remark}
In particular this means that an object is [[cofibrant object|cofibrant]] 
in $sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj}$ if the $G_\bullet$-[[action]] on it is [[free action|free]]. 

Hence [[cofibrant replacement]] is obtained by forming the [[Cartesian product|product]] with the model $W G_\bullet$ for the total space of the [[universal principal bundle]] over $G_\bullet$ (see at _[[simplicial group]]_ for notation and more details).
\end{remark}

\begin{remark}
It follows that for $X, A \in sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj}$ the [[derived hom space]]

$$
  R Hom_G(X,A)
$$

models the Borel $G$-[[equivariant cohomology]] of $X$ with [[coefficients]] in $A$. 

In particular, if $A$ is [[fibrant object|fibrant]] (the underlying simplicial set is a [[Kan complex]]) then:

1. if the $G_\bullet$-action on $A$ is trivial, then 

   $$
     R Hom_G(X,A) 
       \simeq 
     Hom_G(W G \times X , A) 
       \simeq 
     Hom(W G \times_G X, A)
   $$

   is equivalently maps of [[simplicial sets]] out of the [[Borel construction]] on $X$;

1. if $X = \ast $ is the [[point]] then 

   $$
     R Hom_G(X,A) 
       \simeq 
     Hom_G(W G, A) 
       \simeq 
     Hom(\overline{W} G , A)  
       \simeq 
     A^{h G}
   $$

   is the [[homotopy fixed points]] of $A$.

\end{remark}


#### Relation to the slice over the simplicial classifying space
 {#RelationToSliceOverSimplicialClassifyingSpace}

\begin{prop}\label{QuillenEquivalenceToSliceOverSimplicialClassifyingSpace}
  For $G$ a [[simplicial group]], there is a pair of [[adjoint functors]]
  \[
    \label{QuillenAdjunctionWithSliceOverSimplicialClassifyingSpace}
    G Act\big(sSet_{Qu}\big)_{proj}
      \underoverset
        {\underset{ \big((-) \times W G\big)/G }{\longrightarrow}}
        {\overset{ (-) \times_{\overline{W}G} W G  }{\longleftarrow}}
        {\bot}
    \big(sSet_{Qu}\big)_{/\overline{W}G}
  \]
  which constitute a [[simplicial Quillen adjunction|simplicial]] [[Quillen equivalence]] between the Borel model structure (Def. \ref{BorelModelStructure}) and the [[slice model structure]] of the [[classical model structure on simplicial sets]], sliced over the [[simplicial classifying space]] $\overline{W}G$.
  
\end{prop}

(this is essentially the statement of [DDK 80, Prop. 2.3, Prop. 2.4](#DDK80)) 

Here:

* the [[right adjoint]] is the [[Borel construction]] 

  understood as forming [[associated bundles]] to [[universal principal bundles]];

* the [[left adjoint]] forms [[homotopy fibers]].

(This may also be understood as an instance of the "[[fundamental theorem of (infinity,1)-topos theory|fundamental theorem of $\infty$-topos theory]]", see [there](slice+of+presheaves+is+presheaves+on+slice#InfinityActionsAsSlice).)

\begin{proof}\label{SimplicialProofOfEquivalenceToSliceModelStructure}
Consider any [[morphism]] in $sSet_{/\overline{W}G}$:

$$
  \array{
    X && \xrightarrow{\;\;f\;\;} && Y
    \mathrlap{\,.}
    \\
    & 
      {}_{\mathllap{c_X}}\searrow 
    && 
      \swarrow_{\mathrlap{c_Y}}
    \\
    && \overline{W}G
  }
$$

Its image under the left adjoint functor is, by definition, the top left arrow in the following [[commuting diagram]]:

\begin{tikzcd}
    c_X^\ast(W G)
    \ar[
      rr,
      "(f) \underset{\overline{W}G}{\times} W G"
    ]
    \ar[
      d,
      "p_X \,\in\, \mathrm{Fib}"
    ]
    &&
    c_Y^\ast(W G)
    \ar[
      d,
      "p_Y \,\in\, \mathrm{Fib}"
    ]
    \ar[rr]
    &&
    W G
    \ar[
      d,
      "\in \mathrm{Fib}"
    ]
    \\
    X
    \ar[
      rr,
      "f"{below}
    ]
    \ar[
      rrrr,
      rounded corners,
      to path={
         -- ([yshift=-7pt]\tikztostart.south)
         --node[below]{\scalebox{.7}{$
               c_Y
             $}} ([yshift=-7pt]\tikztotarget.south)
         -- (\tikztotarget.south)}
    ]
    &&
    Y
    \ar[
      rr,
      "c_Y"{below}
    ]
    &&
    \overline{W}G
\end{tikzcd}

Here the right square and the total rectangle are [[Cartesian squares]] ([[pullback squares]]), by defnition of the functor. It follows by the [[pasting law]] that also the square on the left is cartesian. Specifically, since [[fibrations]] are preserved under pullback, as shown, the top left morphism in question is the pullback of $f$ along a [[fibration]].

It follows that $(f) \underset{\overline{W}G}{\times} W G$ is:

1. a [[weak equivalence]] if $f$ is a weak equivalence, because the [[classical model structure on simplicial sets]] is a [[right proper model category]] (see [here](classical+model+structure+on+simplicial+sets#Properness));

1. a [[monomorphism]] if $f$ is a monomorphism, since monomorphisms are preserved by pullback (see [here](monomorphism#MonomorphismsArePreservedByPullback)).

   Moreover, since $W G \to \overline{W}G$ is the [[universal principal bundle]], it follows that $c_Y^\ast(W G) \to Y$ is a [[simplicial principal bundle]], so that, in particular, the action of $G$ on $c_Y^\ast(W G)$ is [[free action|free]]. 

   By Prop. \ref{CofibrationsOfSimplicialActions} this means that $(f) \underset{\overline{W}G}{\times} W G$ is a [[cofibration]] if $f$ is a cofibration.

In summary, the left adjoint functor in (eq:QuillenAdjunctionWithSliceOverSimplicialClassifyingSpace) preserves the classes of [[weak equivalences]] and of [[cofibrations]], hence also that of [[acyclic cofibrations]], and so it is a [[left Quillen functor]]. 

Next...
\end{proof}

In fact, these functors (eq:QuillenAdjunctionWithSliceOverSimplicialClassifyingSpace) are [[sSet]]-[[enriched functors]] which induce an [[equivalence of (infinity,1)-categories|equivalence of $(\infty,1)$-categories]] between the [[simplicial localizations]]  $L_W sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj} \simeq L_W sSet_{/\overline{W}H}$ ([DDK 80, Prop. 2.5](#DDK80)).

This kind of relation is discussed in more detail at _[[∞-action]]_.


\begin{remark}\label{sSetEnrichmentOfAdjunctionToSliceOverSimpClassSpace}
**(sSet-enrichement of the adjunction)** \linebreak
The statement that (eq:QuillenAdjunctionWithSliceOverSimplicialClassifyingSpace) is an [[sSet]]-*[[enriched adjunction]]* is not made explicit in [DDK 80](#DDK80); there it only says that the functors form a plain [[adjoint functors|adjunction]] ([DDK 80, Prop. 2.3](#DDK80)) and that they are each [[sSet]]-[[enriched functors]] ([DDK 80, Prop. 2.4](#DDK80)). 

The remaining observation that we have a [[natural isomorphism]] of [[sSet]]-[[hom-objects]]

$$
  \big[
    X \times_{\overline{W}G} W G,
    \,
    V
  \big]
  \;\simeq\;
  \big[
    X,
    \,
    (V \times W G)/G
  \big]
$$

hence

$$
  Hom
  \Big(
    \big( X \times_{\overline{W}G} W G \big) \times \Delta[\bullet],
    \,
    V
  \Big)
  \;\simeq\;
  Hom
  \big(
    X \times \Delta[\bullet],
    \,
    (V \times W G)/G
  \big)
$$

follows from the plain adjunction and the natural isomorphism

$$
  (X \times_{\overline{W}G} W G) \times \Delta[\bullet] 
  \;\simeq\;
  (X \times \Delta[\bullet]) \times_{\overline{W}G} W G  
  \,,
$$

which, in turn, follows, for instance, via the [[pasting law]]:

\begin{tikzcd}
  {
    { (X \times_{\overline{W}G} W G) \times \Delta[k] } 
    \atop
    { \mathllap{\simeq} (X \times \Delta[k]) \times_{\overline{W}G} W G  } 
  }
  \ar[r]
  \ar[d]
  \ar[dr,phantom,"\mbox{\tiny (pb)}"]
  & 
  X \times \Delta[k]
  \ar[
    d,
    "\mathrm{pr}_1"
  ]
  \\
  X \times_{\overline{W}G} W G
  \ar[r]
  \ar[d]
  \ar[dr,phantom,"\mbox{\tiny (pb)}"]
  & 
  X 
  \ar[
    d
  ]
  \\
  W G
  \ar[r]
  &
  \overline{W}G
  \,.
\end{tikzcd}

\end{remark}



#### Relation to the model structure on plain simplicial sets
 {#RelationToModelStructureOnPlainSimplicialSets}

For $\mathcal{G} \,\in\, Groups(sSets)$ a [[simplicial group]], write $\mathcal{G}Actions(sSets)$ for the [[category]] of $\mathcal{G}$-[[actions]] on [[simplicial sets]].

\begin{proposition}\label{CofreeAction}
**(underlying simplicial sets and cofree simplicial action)** \linebreak
  The [[forgetful functor]] $undrl$ from $\mathcal{G}Actions$ to underlying simplicial sets is a [[left Quillen functor]] from the Borel model structure (Def. \ref{BorelModelStructure}) to the [[classical model structure on simplicial sets]].

Its [[right adjoint]]

$$
  sSet
  \underoverset
    {\underset{ \;\;\; [\mathcal{G},-] \;\;\; }{\longrightarrow}}
    {\overset{ \;\;\; undrl \;\;\; }{\longleftarrow}}
    {\bot}
  \mathcal{G}Actions(sSet)
$$

sends $\mathcal{X} \in sSet$ to 

* the simplicial set 

  $$
    [\mathcal{G},\mathcal{X}] 
    \;\coloneqq\;
    Hom_{sSet}\big( \mathcal{G} \times \Delta[\bullet], \mathcal{X}\big) 
    \;\;\;
    \in
    sSet
  $$

* equipped with the $\mathcal{G}$-action

  $$
    \mathcal{G} \times [\mathcal{G},\mathcal{X}]
    \overset{ (-) \cdot (-) }{\longrightarrow}
    \mathcal{G}
  $$

  which in degree $n \in \mathbb{N}$ is the [[function]] 

  \[
    \label{CofreeSimplicialActionComponentFunctions}
    Hom(\Delta[n], \mathcal{G})
    \,\times\,
    Hom
    \big(
      \mathcal{G} \times \Delta[n],
      \,
      \mathcal{X}
    \big)
    \longrightarrow
    Hom
    \big(
      \mathcal{G} \times \Delta[n],
      \,
      \mathcal{X}
    \big)    
  \]

  that sends

  \[
  \label{CofreeSimplicialActionInComponents}
  \begin{aligned}
  &
  \Big(
    \Delta[n] \overset{g_n}{\to} \mathcal{G},
    \;
    \mathcal{G}\times \Delta[n]
    \overset{\phi}{\to}
    \mathcal{X},
  \Big)
  \\
  \;\;\mapsto\;\;
  &
  \Big(
  \mathcal{G} \times \Delta[n]
  \overset{id \times diag}{\longrightarrow}
  \mathcal{G} \times \Delta[n] \times \Delta[n]
  \overset{ id \times g_n \times id }{\longrightarrow}
  \mathcal{G} \times \mathcal{G} \times \Delta[n]
  \overset{(-)\cdot(-) \times id}{\to}
  \mathcal{G} \times \Delta[n]
  \overset{\phi}{\to}
  \mathcal{X}
  \Big)
  \end{aligned}
  \]

\end{proposition} 

Here and in the following proof we make free use of the [[Yoneda lemma]] [[natural bijection]]

$$
  Hom_{sSet}(\Delta[n], \mathcal{S}) \;\simeq\; \mathcal{S}_n
$$

for any [[simplicial set]] $S$ and for $\Delta[n] \in \Delta \overset{y}{\hookrightarrow} sSet$ the simplicial [[n-simplex]].

\begin{proof}

We already know from Def. \ref{BorelModelStructure} that $underl$ preserves all [[weak equivalences]] and from Prop. \ref{CofibrationsOfSimplicialActions} that it preserves all [[cofibrations]]. Therefore it is a [[left Quillen functor]] as soon as it is a [[left adjoint]] at all.

The idea of the existence of the [[cofree functor|cofree]] [[right adjoint]] to $undrl$ is familiar from [[topological G-spaces]] (see the section on [coinduced actions](topological+G-space#CoinducedActions) there), where it can be easily expressed point-wise in [[point-set topology]]. The formula (eq:CofreeSimplicialActionInComponents) adapts this idea to simplicial sets. Its form makes manifest that this gives a simplicial homomorphism, and with this the adjointness follows the usual logic by focusing on the image of the non-degenerate top-degree cell in $\Delta[n]$:

To check that (eq:CofreeSimplicialActionInComponents) really gives the right adjoint, it is sufficient to check the corresponding [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism), hence to check 
for $\mathcal{P} \in \mathcal{G}Actions(sSet)$, and $\mathcal{X} \in sSet$,
that we have a [[natural bijection]] of [[hom-sets]] of the form

$$
  \big\{
    \mathcal{P} 
       \overset{\;\;\phi_{(-)}\;\;}{\longrightarrow} 
    [\mathcal{G}, \mathcal{X}]
  \big\}
  \;\;\;\overset{ \;\; \widetilde{(-)} \;\; }{\leftrightarrow}\;\;\;
  \big\{
    undrl(\mathcal{P}) 
      \overset{\;\; {\widetilde \phi}_{(-)} \;\; }{\longrightarrow} 
    \mathcal{X}
  \big\}
  \,.
$$

So given 

$$
  \phi_{(-)}
  \;\colon\;
  p_n 
  \mapsto 
  \big(
    \phi_{p_n}
    \;\colon\;
    \mathcal{G} \times \Delta[n] \to \mathcal{X}
  \big)
$$

on the left, define

\[
  \label{AdjunctOfHomomorphismToCofreeSimplicialAction}
  \widetilde \phi_{(-)}
  \;\colon\;
  p_n 
  \mapsto
  \phi_{p_n}(e_n, \sigma_n)
  \;\in\;
  \mathcal{X}_n
  \,,
\]

where $e_n \in \mathcal{G}_n$ denotes the [[neutral element]] in degree $n \in \mathbb{N}$ and where $\sigma_n \in (\Delta[n])_n$ denotes the unique non-degenerate element $n$-cell in the [[n-simplex]]. 

It is clear that this is a [[natural transformation]] in $P$ and $X$. We need to show that ${\widetilde \phi}_{(-)} \colon undrl(P) \to X$ uniquely determines all of $\phi_{(-)}$.

To that end, observe for any $g_n \in \mathcal{G}_n$ the following sequence of identifications:

$$
  \begin{aligned} 
    \phi_{p_n}(g_n, \sigma_n)
    & \;=\;
    \phi_{p_n}( e_n \cdot g_n, \sigma_n )
    \\
    & \;=\;
    \big(
      g_n \cdot \phi_{p_n}
    \big)
    ( e_n, \sigma_n )
    \\
    & \;=\;
    \phi_{ g_n \cdot p_n }
    (e_n, \sigma_n)
    \\
    & \;=\;
    {\widetilde \phi}_{g_n \cdot p_n}
  \end{aligned}
$$

Here:

* the first step is the unit law in the component group $\mathcal{G}_n$;

* the second step uses the definition (eq:CofreeSimplicialActionInComponents) of the cofree action;

* the third step is the assumption that $\phi_{(-)}$ is a homomorphism of $\mathcal{G}$-actions ([[equivariant function|equivariance]]);

* the fourth step is the definition (eq:AdjunctOfHomomorphismToCofreeSimplicialAction).

These identifications show that $\phi_{(-)}$ is uniquely determined by ${\widetilde \phi_{(-)}}$, and vice versa.

\end{proof}



\begin{example}\label{BZActionOnInertiaGroupoid}
**($\mathbf{B}\mathbb{Z}$-[[infinity-action|2-action]] on [[inertia groupoid]])** \linebreak
  Let 

  * $G \in Groups(Sets)$ 

    be a [[discrete group]],

  * $X \in G Actions(Sets)$ 

    be a $G$-[[group action|action]],

  * $\mathcal{X} \;\coloneqq\; X \sslash G \;\coloneqq\; N( X \times G \rightrightarrows X ) \,=\, X \times G^{\times^\bullet} \in sSet$ 
 
    the [[simplicial set]] which is the [[nerve]] of its [[action groupoid]] (a model for its [[homotopy quotient]]),

  * $\mathcal{G} \,\coloneqq\, \mathbf{B}\mathbb{Z} \,\coloneqq\, N(\mathbb{Z} \rightrightarrows \ast)  \,\coloneqq\, \mathbb{Z}^{\times^\bullet} \,\in\, Groups(sSet)$ 

    the [[simplicial group]] which is the [[nerve]] of the [[2-group]] that is the [[delooping groupoid]] of the additive group of [[integers]].

Then the [[functor groupoid]]

\[
  \label{InertiaGroupoidAsFunctorGroupoidOutOfBZ}
  \begin{aligned}
    \Lambda(X \!\sslash\! G)
    & \;\coloneqq\;
    \big[
      \mathbf{B}\mathbb{Z}, X \!\sslash\! G
    \big]
    \\
    &
    \;\simeq\;
    Func
    \big(  
      (\mathbb{Z} \rightrightarrows \ast),
      \,
      (X \times G \rightrightarrows X)
    \big)
    \\
    & \;\underset{\in \mathrm{W}}{\leftarrow}\;
    \underset{
      [g] \in ConjCl(G)
    }{\coprod}
    \Big(
      X^{g} \!\sslash\! C_g
    \Big)
  \end{aligned}
\]

is known as the *[[inertia groupoid]]* of $X \!\sslash\! G$. Here

$$
  ConjCla(G)
  \;\coloneqq\;
  G/_{ad} G
  \,,
  \;\;\;\;\;\;\;\;\;\;\;
  C_g 
  \;\coloneqq\;
  \big\{
    h \in G
    \,\left\vert\,
    h \cdot g = g \cdot h
    \right.
  \big\}
$$

denotes, respectively, the set of [[conjugacy classes]] of elements of $G$, and the [[centralizer]] of $\{g\} \subset G$ -- this data serves to express the [[equivalence of categories|equivalent]] [[skeleton]] of the inertia groupoid in the last line of (eq:InertiaGroupoidAsFunctorGroupoidOutOfBZ).

Now, by Prop. \ref{CofreeAction} the inertia groupoid (eq:InertiaGroupoidAsFunctorGroupoidOutOfBZ) carries a canonical [[infinity-action|2-action]] of the [[2-group]] $\mathbf{B}\mathbb{Z}$:

By the formula (eq:CofreeSimplicialActionInComponents), for $n \in \mathbb{Z}$ the 2-group element in degree 1

$$
  {\color{purple}n}
  \;\colon\;
  \Delta[1]
  \longrightarrow
  \mathbf{B} \mathbb{Z}
$$

acts on the morphisms 

$$
  (x,g) \overset{h}{\longrightarrow} (h\cdot x, g)
  \;\;\;
  \in
  \;
  \Lambda(X \!\sslash\! G)
$$

of the inertia groupoid as follows (recall the nature of [[products of simplices]]):

<img src="https://ncatlab.org/nlab/files/BZActionOnInertiaGroupoid20210624.jpg" width="800" />

\end{example}


#### Relation to the fine model structure of equivariant homotopy theory

The [[identity functor]] gives a [[Quillen adjunction]] between the Borel model structure and the [[final model structure on topological G-spaces]] for [[equivariant homotopy theory]] ([Guillou 2006, section 5](#Guillou06)).

The left adjoint is

$$
  L = id 
    \;\colon\; 
  G_\bullet Act_{coarse} 
    \longrightarrow 
  G_\bullet Act_{fine}
$$

from the Borel model structure to the genuine [[equivariant homotopy theory]].

Because:

First of all, by ([Guillou 2006, theorem 3.12, example 4.2](#Guillou06)) $sSet^{\mathbf{B}G_\bullet}$ does carry a fine model structure. By ([Guillou 2006, last line of page 3](#Guillou06)) the fibrations and weak equivalences here are those maps which are ordinary fibrations and weak equivalences, respectively, on $H$-[[fixed point]] simplicial sets, for all subgroups $H$. This includes in particular the trivial subgroup and hence the identity functor

$$
  R = id \;\colon\; G_\bullet Act_{fine} \longrightarrow G_\bullet Act_{coarse}
$$

is right Quillen.





#### Generalization to simplicial presheaves
 {#GeneralizationToSimplicialPresheaves}

Since the [[simplicial classifying space|universal simplicial principal complex]]-construction is [[functor|functorial]]

$$
  SimplicialGroups
  \xrightarrow{\;\; W \;\;}
  SimplicialSets
$$

with [[natural transformations]]

$$
  \mathcal{G}
  \xrightarrow{\;\; i \;\;}
  W\mathcal{G}
  \xrightarrow{\;\; p \;\;}  
  \overline{W}\mathcal{G}
$$

the pair of [[adjoint functors]] (eq:QuillenAdjunctionWithSliceOverSimplicialClassifyingSpace) extends to [[presheaves]]:


\begin{prop}
For $\mathcal{C}$ a [[small category|small]] [[sSet-category]] with

$$
  sPSh(\mathcal{C})
  \;\coloneqq\;
  sSetCat( \mathcal{C}^{op}, \, sSet )
$$

denoting its category of [[simplicial presheaves]], and for

$$
  \underline{\mathcal{G}}
  \;\in\;
  Groups
  \big(
    sPSh(\mathcal{C})
  \big)
$$

a [[group object]] [[internalization|internal to]] [[SimplicialPresheaves]] with

$$
  \underline{\mathcal{G}}
  Acts
  \big(
    sPSh(\mathcal{C})
  \big)  
$$

denoting its category of [[action objects]] [[internalization|internal to]] [[SimplicialPresheaves]]

we have an [[adjoint functor|adjoint pair]]

$$
  \underline{\mathcal{G}}
  Acts
  \big(
    sPSh(\mathcal{C})
  \big)  
  \underoverset
    {
      \underset{ 
        \big(
          (-) \times W\underline{\mathcal{G}} 
        \big) 
        \big/
        \underline{\mathcal{G}}
      }
      {\longrightarrow}}
    {
      \overset{
        (-) 
          \times_{\overline{W}\underline{\mathcal{G}}}
        W\underline{\mathcal{G}}
      }{\longleftarrow}
    }
    {\bot}
    sPSh(\mathcal{C})_{/\overline{W}\underline{\mathcal{G}}}
$$

\end{prop}
\begin{proof}
The required [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) is the composite of the following sequence of [[natural bijections]]:

$$
  \begin{aligned}
    Hom
    \Big(
      (\underline{X},p),
      \,
      \big(
        \underline{Y} \times W\underline{\mathcal{G}}  
      \big) / \underline{\mathcal{G}}
    \Big)
    & 
    \;\simeq\;
    Hom
    \Big(
      \underline{X},
      \,
      \big(
        \underline{Y} \times W\underline{\mathcal{G}}  
      \big) / \underline{\mathcal{G}}
    \Big)
    \underset{
    Hom
    \Big(
      \underline{X},
      \,
      \overline{W} \underline{\mathcal{G}}
    \Big)
    }{\times}
    \{p\}
    \\
    & \;\simeq\;
    \int^c
    Hom
    \Big(
      \underline{X}(c),
      \,
      \big(
        \underline{Y}(c) \times W\underline{\mathcal{G}(c)}  
      \big) / \underline{\mathcal{G}}(c)
    \Big)
    \underset{
    \int^c
    Hom
    \Big(
      \underline{X}(c),
      \,
      \overline{W} \underline{\mathcal{G}}(c)
    \Big)
    }{\times}
    \{p\}
    \\
    & \;\simeq\;
    \int^c
    \left(
    Hom
    \Big(
      \underline{X}(c),
      \,
      \big(
        \underline{Y}(c) \times W\underline{\mathcal{G}}(c)  
      \big) / \underline{\mathcal{G}}(c)
    \Big)
    \underset{
    Hom
    \Big(
      \underline{X}(c),
      \,
      \overline{W} \underline{\mathcal{G}}(c)
    \Big)
    }{\times}
    \{p(c)\}
    \right)
    \\
    & \;\simeq\;
    \int^c 
    Hom_{/\overline{W}\underline{\mathcal{G}}(c)}
    \Big(
      \big( \underline{X}(c), p(c)\big),
      \,
      \big(
        \underline{Y}(c) \times \overline{W} \underline{\mathcal{G}}(c)
      \big)\big/ \mathcal{G}(c)
    \Big)
    \\ 
    & \;\simeq\;
    \int^c
    \left(
      \underline{\mathcal{G}}(c)
      Acts(sSet)
      \big(
        \underline{X}(c) 
          \underset{ \overline{W}\underline{\mathcal{G}}(c) }{\times}
        W \underline{\mathcal{G}}(c),
        \,
        \underline{Y}(c)
      \big)
    \right)
    \\
    & \;\simeq\;
    \mathcal{G}Acts(sPSh(\mathcal{C}))
    \big(
      \underline{X} 
        \underset{\overline{W}\underline{\mathcal{G}}}{\times}
      W \underline{\mathcal{G}},
      \,
      \underline{Y}
    \big)
  \end{aligned}
$$

Here:

* the first step is the characterization of hom-sets of a [[slice category]] as a [[fiber]] of the [[hom-sets]] of the underlying category;

* the second step is the description of the hom-set of a [[functor category]] as an [[end]] of object-wise hom-sets;

* the third step uses that [[ends]] are [[limits]] and [[limits commute with limits|hence commute]] with the [[fiber product]];

* the fourth step recognizes again, now object-wise, the hom-set in a [[slice category]];

* the fifth step is objectwise the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) of (eq:QuillenAdjunctionWithSliceOverSimplicialClassifyingSpace);

* the sixth step recognizes again the [[end]] as computing the hom-set in (a subcategory of) a functor category:

$$
  \array{
    \underline{\mathcal{G}}Acts
    \big(
      \underline{A}, \, \underline{B}
    \big)
    &\longrightarrow&
    \mathcal{G}(c_1)Acts
    \big(
       \underline{A}(c_1), \, \underline{B}(c_1)
    \big)
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    \mathcal{G}(c_2)Acts
    \big(
      \underline{A}(c_2), \, \underline{B}(c_2)
    \big)
    &\longrightarrow&
    Hom
    \big(
      \underline{A}(c_1), \, \underline{B}(c_2)
    \big)
  }
$$

\end{proof}


### In combinatorial simplicial model categories
 {#PropertiesInCombSimpModCats}

#### Base change

Given

* $\mathcal{G} \,\in\, Grp(sSet)$ a [[simplicial group]],

* $\mathbf{C}$ a [[combinatorial simplicial model category]] with 

  * [[sSet]]-[[tensoring]] denoted

    $$
      sSet \times \mathbf{C} 
        \overset{ (-) \cdot (-) }{\longrightarrow}
      \mathbf{C}
      \mathrlap{\,,}
    $$

  * [[classes]] of (acyclic) [[generating cofibrations]] denoted

    $I_{\mathbf{C}},J_{\mathbf{C}} \,\subset\, Mor(\mathbf{C})$, 

then its Borel model category
(eq:BorelModelStructureForCombinatoriaSimplicialModelCat)
$$
  \mathcal{G}Act(\mathbf{C})_{Borel}
  \,\coloneqq\,
  sFunc(\mathbf{B}\mathcal{G},\,\mathbf{C})_{proj}
$$
has, by [this Prop.](model+structure+on+functors#ExistenceOfProjectiveStructureOnEnrichedFunctors), (acyclic) [[generating cofibrations]] given by [[tensoring]] these with $\mathcal{G} = (\mathbf{B}\mathcal{G})(\ast, \ast)$ and understood as equipped with the $\mathcal{G}$-[[action]] induced by the [[regular action]] of $\mathcal{G}$ on itself:
\[
  \label{GeneratingCofibrationsForBorelInCombSimpCat}
  \array{
  I_{\mathcal{G}Act(\mathbf{C})}
  &\coloneqq&
  \mathcal{G}\cdot(I_{\mathbf{C}})
  \;\equiv\;
  \big\{
    \mathcal{G} \cdot i
    \,\big\vert\,
    i \in I
  \big\}
  \\
  J_{\mathcal{G}Act(\mathbf{C})}
  &\coloneqq&
  \mathcal{G}\cdot(J_{\mathbf{C}})
  \;\equiv\;
  \big\{
    \mathcal{G} \cdot j
    \,\big\vert\,
    j \in J
  \big\}
  \mathrlap{\,,}
  }
\]
where we noticed that these are just the [[images]] under the (acyclic) [[generating cofibrations]] of $\mathbf{C}$ under the left-[[induced action]]
\[
  \label{LeftQuillenInductionForBorelInCombSimpModCat}
  \mathbf{C}
  \underoverset
    {\underset{undrl}{\longleftarrow}}
    {\overset{\mathcal{G}\cdot(-)}{\longrightarrow}}
    {\;\; \bot \;\;}
  \mathcal{G}Act(\mathbf{C})
  \,.
\]


But since 

1. the [[underlying]] [[simplicial set]] of $\mathcal{G}$ is necessarily a [[cofibrant object]] of [[classical model structure on simplicial sets|$sSet_{Qu}$]]

1. $\mathbf{C}$ is an $sSet$-[[enriched model category]]

the [[pushout-product axiom]] satisfied by the [[tensoring]] implies that the [[underlying]] morphisms of these (acyclic) [[generating cofibration]] in the Borel structure, i.e. [[forgetful functor|forgetting]] their [[equivariant map|equivariance]] under the [[simplicial group action]], are still (acyclic) cofibrations in $\mathbf{C}$ itself, hence that we also have a [[Quillen adjunction]] of the form
\[
  \label{RightQuillenInductionForBorelInCombSimpModCat}
    \mathbf{C}   
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{undrl}{\longleftarrow}}
      {\;\;\; \bot_{{}_{Qu}} \;\;\;}
    \mathcal{G}Act(\mathbf{C})_{Borel}
\]
whose [[right adjoint]] may be thought of as the right [[induced action]] or equivalently as right [[Kan extension]] along the [[sSet]]-[[enriched functor]] $\ast \to \mathbf{B}\mathcal{G}$.


#### Monoidal model structure
 {#MonoidalModelStructure}

We discuss (Prop. \ref{ExistenceOfMonoidalModelStructure} below) induced [[monoidal model category]]-[[structure]] on the Borel model structure, in the generality of [[coefficients]] any (cofibrantly generated)  simplicial model structure (as [above](#DefinitionInCombSimpModCat)), which in addition carries compatible [[monoidal simplicial model structure]].



\begin{proposition}
\label{ExistenceOfMonoidalModelStructure}
  For $\mathcal{G} \in Grp(sSet)$ and $\mathbf{C}$ a [[combinatorial simplicial model category]] with compatible  [[closed monoidal category|closed]] [[monoidal enriched category]]-[[structure]], i.e. with an [[sSet]]-[[enriched functor]]  $(-)\otimes(-)$, the the objectwise [[tensor product]] 
$$
  \mathcal{G}Act(\mathbf{C})
  \times
  \mathcal{G}Act(\mathbf{C})
  \,\equiv\,
  sFunc(\mathbf{B}\mathcal{G},\,\mathbf{C})
  \times
  sFunc(\mathbf{B}\mathcal{G},\,\mathbf{C})
  \;\simeq\;
  sFunc(\mathbf{B}\mathcal{G},\,\mathbf{C} \times \mathbf{C})
  \overset
    {   
      sFunc(\mathbf{B}\mathcal{G},\, \otimes)
    }
    {\longrightarrow}
  sFunc(\mathbf{B}\mathcal{G},\,\mathbf{C})
$$
and the objectwise [[internal hom]]
$$
  \mathcal{G}Act(\mathbf{C})
  \times
  \mathcal{G}Act(\mathbf{C})
  \,\simeq\,
  sFunc\big(\mathbf{B}\mathcal{G},\,\mathbf{C}^{op})
  \times
  sFunc(\mathbf{B}\mathcal{G},\,\mathbf{C})
  \;\simeq\;
  sFunc(\mathbf{B}\mathcal{G},\,\mathbf{C} \times \mathbf{C})
  \overset
    {   
      sFunc(\mathbf{B}\mathcal{G},\, [-,-])
    }
    {\longrightarrow}
  sFunc(\mathbf{B}\mathcal{G},\,\mathbf{C})
$$
make the Borel model structure (eq:BorelModelStructureForCombinatoriaSimplicialModelCat)
$$
  \big(\mathcal{G}Act(\mathbf{C}), \otimes \big)
$$
a [[monoidal model category]], at least in that the [[pushout-product axiom]] holds.
A sufficient condition that also the [[unit axiom]] hold is that all objects of $\mathbf{C}$ are cofibrant.
\end{proposition}
The following argument for the pushout-product axiom follows [Berger & Moerdijk (2006), Lem. 2.5.2](#BergerMoerdijk2006).
\begin{proof}
It is sufficient to check the [[pushout-product axiom]] on (acyclic) [[generating cofibrations]] (by [this remark](pushout-product#PushoutProductAxiomInCofibrantlyGeneratedModelCategories)). To that end, given 

* [[generating cofibrations]]$\;A \to B$ and $X \to Y$ in $I_{\mathcal{G}Act(\mathbf{C})}$, we need to check that their [[pushout product]] is still a cofibration, which means that for any 

* [[acyclic fibration]]$\;Z \to W$ in $WFib_{\mathcal{G}Act(\mathbf{C})} = undrl^{-1} WFib_{\mathbf{C}}$

we need to find a [[lift]] in any [[commuting square]] of the form

$$
  \array{
    (A \otimes Y)
     \overset{A \otimes X}{\amalg}
    (B \otimes X)
    &\longrightarrow&
    Z
    \\
    \Big\downarrow
    &&
    \Big\downarrow
    \\
    B \otimes Y 
     &\longrightarrow&
    W
    \mathrlap{\,.}
  }
  \;\;\;\text{in}\;\; \mathcal{G}Act(\mathbf{C})
  \,.
$$
By [[Joyal-Tierney calculus]], this is equivalent to finding a [[lift]] in the [[internal hom]]-[[adjunct]] diagram:
$$
  \array{
    A 
      &\longrightarrow& 
    [X,Z]
    \\
    \Big\downarrow && \Big\downarrow
    \\
    B 
      &\longrightarrow&
    [Y,W] 
      \underset{[X,W]}{\times}
    [X,Z]
  }
  \;\;\;\text{in}\;\; \mathcal{G}Act(\mathbf{C})
  \,.
$$
Now observe that the (acyclic) Borel-cofibration on the left is, by (eq:GeneratingCofibrationsForBorelInCombSimpCat), in the image of the [[left adjoint]] functor $\mathcal{G}\cdot(-)$ whose [[right adjoint]] is the [[forgetful functor]] remembering just the [[underlying]] morphisms in $\mathbf{C}$. Therefore a lift in the above diagram is equivalently a lift of its [[adjunct]], which is just the [[underlying]] diagram in $\mathbf{C}$:
$$
  \array{
    A 
      &\longrightarrow& 
    [Y,Z]
    \\
    \Big\downarrow && \Big\downarrow
    \\
    B 
      &\longrightarrow&
    [Y,W] 
      \underset{[X,W]}{\times}
    [X,Z]
  }
  \;\;\;\text{in}\;\; \mathbf{C}
  \,.
$$
But now using

1. that the underlying map of the previous [[acyclic fibration]] is still an acyclic fibration in $\mathbf{C}$, by definition of the projective/Borel model strcuture,

1. that the underlying maps of the previous [[cofibrations]] are still cofibrations in $\mathbf{C}$, by (eq:RightQuillenInductionForBorelInCombSimpModCat)

1. the [[pullback-power axiom]] satisfied in the [[monoidal model category]] $\mathbf{C}$

it follows that the left map in this diagram is a cofibration and the right map is still an acyclic fibration, whence a lift exists by the model category axioms on $\mathbf{C}$.

A directly analogous argument applies in the cases where $A \to B$ or $X \to Y$ are in addition weak equivalences. Hence the [[pushout-product axiom]] is verified.

Finally, to verify the [[unit axiom]]: 

If $\mathbb{1} \,\in\, \mathbf{C}$ denotes the given [[tensor unit]], then the [[tensor unit]] in $\mathcal{G}Act(\mathbf{C})$ is the [[constant functor]] $\mathbf{B}\mathcal{G} \to \ast \overset{\mathbb{1}}{\longrightarrow} \mathbf{C}$, corresponding to the [[trivial action]] on $\mathbb{1}$. Writing $p_{const \mathbb{1}} \colon Q const(\mathbb{1}) \to const \mathbb{1}$ for a [[cofibrant resolution]], we need to see that given an [[object]] $X \in \mathcal{G}Act(\mathbf{C})$ the composite
$$
  (Q const \mathbb{1})
    \otimes
  X
  \overset{
    p_{const \mathbb{I}} \otimes id_X
  }{\longrightarrow}
  (const \mathbb{1}) \otimes X
  \underoverset{\sim}{l}{\longrightarrow}
  X
$$
is a [[weak equivalence]].

Since weak equivalence are just the underlying weak equivalences, for this it is sufficient (with the assumption that all objects in $\mathbf{C}$ are cofibrant), that 
$(-) \otimes X$ is a [[left Quillen functor]] on $\mathbf{C}$, since as such it preserves all weak equivalences between cofibrant objects, by [Ken Brown's lemma](Introduction+to+Homotopy+Theory#KenBrownLemma).

But the [[underlying]] object of $X$ is still cofibrant in $\mathbf{C}$, by (eq:RightQuillenInductionForBorelInCombSimpModCat), therefore $(-) \otimes X$ is left Quillen by the [[pushout-product axiom]] satisfied by the [[monoidal model category]] $\mathbf{C}$.
\end{proof}


## Related concepts

* [[fine model structure on topological G-spaces]]

* [[Borel-equivariant rational homotopy theory]]

## Literature

### In simplicial sets
 {#ReferencesInSimplicialSets}

The model structure, the characterization of its cofibrations, and its equivalence to the [[slice model structure]] of $sSet$ over $\bar W G$ is due to

* {#DDK80} [[Emmanuel Dror]], [[William Dwyer]], [[Daniel Kan]], _Equivariant maps which are self homotopy equivalences_, Proc. Amer. Math. Soc. 80 (1980), no. 4, 670&#8211;672 ([jstor:2043448](http://www.jstor.org/stable/2043448))

This Quillen equivalence also mentioned as:

* {#Dwyer2008} [[William Dwyer]], Exercise 4.2 in: _Homotopy theory of classifying spaces_, Lecture notes, Copenhagen 2008, ([pdf](http://www.math.ku.dk/~jg/homotopical2008/Dwyer.CopenhagenNotes.pdf), [[Dwyer_HomotopyTheoryOfClassifyingSpaces.pdf:file]])

Discussion in relation to the "fine" model structure of [[equivariant homotopy theory]] which appears in [[Elmendorf's theorem]] is in 

* {#Guillou06} [[Bert Guillou]], _A short note on models for equivariant homotopy theory_, 2006 ([pdf](http://www.math.uiuc.edu/~bertg/EquivModels.pdf), [[GuillouModelsForEquivariantHomotopyTheory.pdf:file]])

Textbook account of (just) the Borel model structure:

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], Section V.2 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) ([doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/))


Discussion with the model of [[∞-groups]] by [[simplicial groups]] replaced by groupal [[Segal spaces]] is in 

* [[Matan Prasma]], _Segal Group Actions_ ([arXiv:1311.4749](http://arxiv.org/abs/1311.4749))

Discussion of [[monoidal model category]]-enhancement on the Borel model structure:

* {#BergerMoerdijk2006} [[Clemens Berger]], [[Ieke Moerdijk]], §2.5 in: *The Boardman-Vogt resolution of operads in monoidal model categories*, Topology **45** (2006) 807-849 &lbrack;[arXiv:math/0502155](https://arxiv.org/abs/math/0502155), [doi:10.1016/j.top.2006.05.001](https://doi.org/10.1016/j.top.2006.05.001)&rbrack;

Discussion of a the [[integral model structure]] for actions of all simplicial groups:

* [[Yonatan Harpaz]], [[Matan Prasma]], section 6.2 of _The Grothendieck construction for model categories_ ([arXiv:1404.1852](http://arxiv.org/abs/1404.1852))



### In topological spaces
 {#ReferencesInTopologicalSpaces}

* [Guillou 2006, Section 5](#Guillou06)

* [[Steffen Sagave]], [[Christian Schlichtkrull]], Prop. 6.4 in: *Diagram spaces and symmetric spectra*, Advances in Mathematics, 231 (2012), 2116-2193 ([arXiv:1103.2764](https://arxiv.org/abs/1103.2764), [doi:10.1016/j.aim.2012.07.013](https://doi.org/10.1016/j.aim.2012.07.013))




[[!redirects Borel model structures]]

[[!redirects model structure on simplicial group actions]]
[[!redirects model structures on simplicial group actions]]


[[!redirects coarse model structure on topological G-spaces]]

