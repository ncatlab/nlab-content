

## Gros toposes
 {#GrosToposes}


We have seen roughly two different kinds of [[sheaf toposes]]:

* [[categories of sheaves on a topological space|categories of sheaves on a given space]] $X$ (Example \ref{SheafOnATopologicalSpace}), which, by [[localic reflection]] (Prop. \ref{LocalicReflection}), really are just a reflection of the space $X$ in the [[category]] of [[toposes]],

  these are called _[[petit toposes]]_;

* [[categories of sheaves]] whose [[objects]] are [[generalized spaces]] (Example \ref{SmoothSetAnnounced})

  these are called _[[gros toposes]]_.

+-- {: .num_remark #CohesiveGeneralizedSpacesAsFoundations}
###### Remark
**([[cohesion|cohesive]] [[generalized spaces]] as [[foundations|foundations]] of [[geometry]])**

If we aim to lay [[foundations]] for [[geometry]], then we are interested in isolating those kinds of [[generalized spaces]] which have foundational _a priori_ meaning, independent of an otherwise pre-configured notion of space.
Hence we would like to first characterize suitable [[gros toposes]], extract concepts of [[space]] from these, and only then, possibly, consider the [[localic reflection|petit topos-reflections]] of these (Prop. \ref{LocalicReflection} below).

The [[gros toposes]] of such foundational [[generalized spaces]] ought to  have an _[[internal logic]]_ that knows about _[[modalities]] of [[geometry]]_ such as _[[discrete object|discreteness]]_ or _[[concrete object|concreteness]]_. Via the formalization of [[modalities]] in Def. \ref{ModalOperator} this leads to the definiton of [[cohesive toposes]] (Def. \ref{CohesiveTopos}, Prop. \ref{PiecesHavePoints} below, due to [[Some Thoughts on the Future of Category Theory|Lawvere 91]], [Lawvere 07](#cohesive+topos#LawvereAxiomatic)).

=--

| $\phantom{A}$[[gros topos]]$\phantom{A}$ |  | $\phantom{A}$[[generalized spaces]] obey...$\phantom{A}$ | $\phantom{A}$example:$\phantom{A}$ |
|-----|---|-------|---|
| $\phantom{A}$[[cohesion]]$\phantom{A}$ |  Def. \ref{CohesiveTopos} |  $\phantom{A}$principles of [[differential topology]]$\phantom{A}$ | $\phantom{A}$[[geometry of physics -- smooth sets|SmoothSet]]$\phantom{A}$ |
| $\phantom{A}$[[elastic topos|elasticity]] | Def. \ref{DifferentialCohesion} |$\phantom{A}$principles of [[differential geometry]]$\phantom{A}$ | $\phantom{A}$[[geometry of physics -- manifolds and orbifolds|FormallSmoothset]]$\phantom{A}$ |
| $\phantom{A}$[[solid topos|solidity]]$\phantom{A}$ | Def. \ref{SuperDifferentialCohesion} | $\phantom{A}$principles of [[supergeometry]]$\phantom{A}$ | $\phantom{A}$[[geometry of physics -- supergeometry|SuperFormalSmoothSet]]$\phantom{A}$ |
{: style='margin:auto'}

$\,$


### Cohesive toposes
 {#Cohesive}

+-- {: .num_defn #CohesiveTopos}
###### Definition
**([[cohesive topos]])**

A [[sheaf topos]] $\mathbf{H}$ (Def. \ref{Sheaf}) is called a _[[cohesive topos]]_ if there is a [[adjoint quadruple|quadruple]] (Remark \ref{AdjointTriples}) of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) to the [[category of sets]] (Example \ref{CategoryOfSets})

\[
  \label{CohesopmAdjointQuadruple}
  \Pi \dashv Disc \dashv \Gamma \dashv coDisc
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{\phantom{AAA} \Pi \phantom{AAA}}{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookleftarrow}
    }
  Set
\]

such that:

1. $Disc$ and $coDisc$ are [[full and faithful functors]] (Def. \ref{FullyFaithfulFunctor})

1. $\Pi$ [[preserved limit|preserves]] [[finite products]].

=--


+-- {: .num_example #PresheavesAdjointQuadrupleOnSiteWithTerminalObject}
###### Example
**([[adjoint quadruple]] of [[presheaves]] over [[site]] with [[finite products]])**

Let $\mathcal{C}$ be a [[small category]] (Def. \ref{SmallCategory}) with [[finite products]] (hence with a [[terminal object]] $\ast \in \mathcal{C}$ and for any two [[objects]] $X,Y \in \mathcal{C}$ their [[Cartesian product]] $X \times Y \in \mathcal{C}$).

Then there is an [[adjoint quadruple]] (Remark \ref{AdjointTriples}) of [[functors]] between the [[category of presheaves]] over $\mathcal{C}$ (Example \ref{CategoryOfPresheaves}), and the [[category of sets]] (Example \ref{CategoryOfSets})

\[
  \label{PreaheafAdjointQuadruple}
  [\mathcal{C}^{op}, Set]
    \array{
      \overset{\phantom{AAA} \Pi \phantom{AAA}}{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookleftarrow}
    }
  Set
\]

such that:

1. the functor $\Gamma$ sends a [[presheaf]] $\mathbf{Y}$ to its set of [[global sections]], which here is its value on the [[terminal object]]:

   \[
     \label{CohesiveGlobalSectionsGivenByPointEvaluation}
     \begin{aligned}
       \Gamma \mathbf{Y}
       & =
       \underset{\underset{\mathcal{C}}{\longleftarrow}}{\lim}
       \mathbf{Y}
       \\
       & \simeq
       \mathbf{Y}(\ast)
     \end{aligned}
   \]

1. $Disc$ and $coDisc$ are [[full and faithful functors]] (Def. \ref{FullyFaithfulFunctor}).

1. $\Pi$ preserves [[finite products]]:

   for $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$, we have a [[natural bijection]]

   $$
     \Pi(\mathbf{X} \times \mathbf{Y})
     \;\simeq\;
     \Pi(\mathbf{X}) \times \Pi(\mathbf{Y})
     \,.
   $$

Hence the [[category of presheaves]] over a [[small category]] with [[finite products]], hence the [[category of sheaves]] for the [[trivial coverage]] (Example \ref{TrivialCoverage}) is a [[cohesive topos]] (Def. \ref{CohesiveTopos}).

=--

+-- {: .proof}
###### Proof

The existence of the [[terminal object]] in $\mathcal{C}$ means equivalently (by Example \ref{InitialCategoryAndTerminalCategory}) that there is an [[adjoint pair]] of [[functors]] between $\mathcal{C}$ and the [[terminal category]] (Example \ref{InitialCategoryAndTerminalCategory}):

$$
  \ast
    \underoverset
    {\underset{}{\hookrightarrow}}
    {\overset{p}{\longleftarrow}}
    {\bot}
   \mathcal{C}
$$

whose [[right adjoint]] takes the unique object of the terminal category to that terminal object.

From this it follows, by Example \ref{KanExtensionOfAdjointPairIsAdjointQuadruple}, that [[Kan extension]] produces an [[adjoint quadruple]] (Remark \ref{AdjointTriples}) of functors between the [[category of presheaves]] $[\mathcal{C}^{op}, Set]$ and $[\ast, Set] \simeq Set$, as shown, where

1. $\Gamma$ is the operation of pre-composition with the terminal object inclusion $\ast \hookrightarrow \mathcal{C}$

1. $Disc$ is the [[left Kan extension]] along the inclusion $\ast \hookrightarrow \mathcal{C}$ of the terminal object.

The former is manifestly the operation of evaluating on the terminal object.
Moreover, since the terminal object inclusion is manifestly a [[fully faithful functor]] (Def. \ref{FullyFaithfulFunctor}), it follows that also its [[left Kan extension]] $Disc$ is fully faithful  (Prop. \ref{LeftKanExtensionAlongFullyFaithfulFunctor}). This implies that also $coDisc$ is fully faithful, by (Prop. \ref{FullyFaithfulAdjointTriple}).

Equivalently, $Disc \simeq p^\ast$ is the [[constant functor|constant]] [[diagram]]-assigning functor. By uniqueness of adjoints (Prop. \ref{UniquenessOfAdjoints}) implies that $\Pi$ is the functor that sends a presheaf, regarded as a [[functor]] $\mathbf{Y} \;\colon\; \mathcal{C}^{op} \to Set$, to its [[colimit]]

\[
  \label{Pi0IsColimit}
  \Pi(\mathbf{Y})
  \;=\;
  \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim} \mathbf{Y}
  \,.
\]

The fact that this indeed preserves products follows from the assumption that $\mathcal{C}$ has [[finite products]], since [[categories with finite products are cosifted]] (Prop. \ref{CategoriesWithFiniteProductsAreCosifted})

=--


Example \ref{PresheavesAdjointQuadrupleOnSiteWithTerminalObject} suggests to  ask for [[coverages]] on categories with [[finite products]] which are such that the [[adjoint quadruple]]  (eq:PreaheafAdjointQuadruple) on the  [[category of presheaves]] ([[corestriction|co-]])[[restriction|restricts]] to the corresponding [[category of sheaves]]. The following Definition \ref{OneCohesiveSite} states a sufficient condition for this to be the case:

+-- {: .num_defn #OneCohesiveSite}
###### Definition
**([[cohesive site]])**

We call a [[site]] $\mathcal{C}$ (Def. \ref{Coverage}) _[[cohesive site|cohesive]]_ if the following conditions are satisfied:

1. The [[category]] $\mathcal{C}$ has [[finite products]] (as in Example \ref{PresheavesAdjointQuadrupleOnSiteWithTerminalObject}).

1. For every [[covering]] family $\{U_i \to X\}_i$ in the given [[coverage]] on  $\mathcal{C}$ the induced [[Cech groupoid]] $C(\{U_i\}_i) \in [C^{op}, Grpd]$ (Def. \ref{CechGroupoid}) satisfies the following two conditions:

   1. the set of [[connected components]] of the [[groupoid]] obtained as the [[colimit]] over the [[Cech groupoid]] is the [[singleton]]:

      $$
        \pi_0
        \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
         C(\{U_i\})
         \;\simeq\;
         \ast
      $$

   1. the set of [[connected components]] of the [[groupoid]] obtained as the [[limit]] of the [[Cech groupoid]] is [[equivalence of categories|equivalent]] to the set of points of $X$, regarded as a groupoid:

      $$
        \pi_0
        \underset{\underset{\mathcal{C}^{op}}{\longleftarrow}}{\lim} C(\{U_i\})
          \simeq
        Hom_{\mathcal{C}}(\ast,X)
        \,.
      $$

=--

This definition is designed to make the following true:

+-- {: .num_prop #CategoriesOfSheavesOnCohesiveSiteIsCohesive}
###### Proposition
**([[category of sheaves]] on a [[cohesive site]] is a [[cohesive topos]])**

Let $\mathcal{C}$ be a [[cohesive site]] (Def. \ref{OneCohesiveSite}). Then the [[adjoint quadruple]] on the [[category of presheaves]] over $\mathcal{C}$, from Example \ref{PresheavesAdjointQuadrupleOnSiteWithTerminalObject} (given that a [[cohesive site]] by definition has [[finite products]]) ([[corestriction|co-]])[[restriction|restricts]] from the [[category of presheaves]] over $\mathcal{C}$, to the [[category of sheaves]] (Def. \ref{Sheaf}) and hence exhibits $Sh(\mathcal{C})$ as a [[cohesive topos]] (Def. \ref{CohesiveTopos}):

\[
  \label{SheafToposAdjointQuadruple}
  Sh(\mathcal{C})
    \array{
      \overset{\phantom{AAA} \Pi \phantom{AAA}}{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookleftarrow}
    }
  Set
\]


=--

+-- {: .proof}
###### Proof

By example \ref{PresheavesAdjointQuadrupleOnSiteWithTerminalObject}  we alreaday have the analogous statement for the [[categories of presheaves]]. Hence it is sufficient to show that the functors $Disc$ and $coDisc$ from Example \ref{PresheavesAdjointQuadrupleOnSiteWithTerminalObject} factor through the definition inclusion of the [[category of sheaves]], hence that for each [[set]] $S$ the [[presheaves]] $Disc(S)$ and $coDisc(S)$ are indeed [[sheaves]] (Def. \ref{Sheaf}).

By the formulaton of the [[sheaf|sheaf condition]] via the [[Cech groupoid]] (Prop. \ref{CechGroupoidCoRepresents}), and using the [[adjunction]] hom-isomorphisms ([here](geometry+of+physics+--+categories+and+toposes#eq:HomIsomorphismForAdjointFunctors)) this is readily seen to be equivalent to the two further conditions on a cohesive site (Def. \ref{OneCohesiveSite}):

Let $\{U_i \to X\}$ be a [[covering]] family.

The sheaf condition (eq:SheafIsLocalObjectWithRespectToCechCovers) for $Disc(S)$ says that

$$
  \left[
    C(\{U_i\}) \overset{p_{\{U_i\}_i}}{\to} y(X)
    \,,\,
    Disc(S)
  \right]
$$

is an [[isomorphism]] of [[groupoids]], which by adjunction and using (eq:Pi0IsColimit) means equivalently that

$$
  \left[
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \left( C(\{U_i\}) \right) \to
    \ast
    \,,\,
    S
  \right]
$$

is an isomorphism of groupoids, where we used that colimits of representables are [[singletons]] (Lemma \ref{ColimitOfRepresentableIsSingleton}) to replace $\underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim} y(X) \simeq \ast$.

But now in this [[internal hom]] of [[groupoids]], the set $S$ is really a groupoid in the image of the [[reflective subcategory|reflective embedding]] of sets into groupoids, whose [[left adjoint]] is the [[connected components]]-functor $\pi_0$ (Example \ref{ReflectiveSubcategoryInclusionOfSetsIntoGroupoids}). Hence  by another adjunction isomoprhism this is equivalent to

$$
  \left[
    \pi_0
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \left( C(\{U_i\}) \right) \to
    \ast
    \,,\,
    S
  \right]
$$

being an isomorphism (a [[bijection]] of [[sets]], now). This is true for all $S \in Set$ precisely if (by the [[Yoneda lemma]], if you wish) the morphism

$$
    \pi_0
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \left( C(\{U_i\}) \right) \to
    \ast
$$

is already an isomorphism (here: [[bijection]]) itself.

Similarly,  the sheaf condition (eq:SheafIsLocalObjectWithRespectToCechCovers) for $coDisc(S)$ says that

$$
  \left[
    C(\{U_i\}) \overset{p_{\{U_i\}_i}}{\to} y(X)
    \,,\,
    coDisc(S)
  \right]
$$

is an [[isomorphism]], and hence by [[adjunction]] and using (eq:CohesiveGlobalSectionsGivenByPointEvaluation), this is equivalent to

$$
  \left[
    \pi_0
    \underset{\underset{\mathcal{C}^{op}}{\longleftarrow}}{\lim}
    C(\{U_i\})
    \overset{p_{\{U_i\}_i}}{\to}
    Hom_{\mathcal{C}}(\ast, X)
    \,,\,
    S
  \right]
$$

being an isomorphism. This holds for all $S \in Set$ if (by the [[Yoneda lemma]], if you wish)

$$
    \pi_0
    \underset{\underset{\mathcal{C}^{op}}{\longleftarrow}}{\lim}
    C(\{U_i\})
    \overset{p_{\{U_i\}_i}}{\to}
    Hom_{\mathcal{C}}(\ast, X)
$$

is an isomorphism.

=--


+-- {: .num_defn #CohesiveModalities}
###### Definition
**([[adjoint triple]] of [[adjoint modality|adjoint]] [[modal operators]] on [[cohesive topos]])**

Given a [[cohesive topos]] (Def. \ref{CohesiveTopos}), its [[adjoint quadruple]] (Remark \ref{AdjointTriples}) of functors to and from [[Set]]

$$
  \label{CohesopmAdjointQuadruple}
  \Pi \dashv Disc \dashv \Gamma \dashv coDisc
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{\phantom{AAA} \Pi \phantom{AAA}}{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookleftarrow}
    }
  Set
$$

induce, by [[composition]] of functors, an [[adjoint triple]] (Remark \ref{AdjointTriples}) of [[adjoint modalities]] (Def. \ref{AdjointModality}):

$$
  &#643; \dashv \flat \dashv \sharp
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{ &#643; \;\coloneqq\; Disc \circ \Pi  }{\hookleftarrow}
      \\
      \overset{\flat \;\coloneqq\; Disc \circ \Gamma  }{\longrightarrow}
      \\
      \overset{ \sharp \;\coloneqq\; coDisc\circ \Gamma }{\hookleftarrow}
    }
  \mathbf{H}
  \,.
$$

Since $Disc$ and $coDisc$ are [[fully faithful functors]] by assumption,
these are ([[comodal operator|co-]])[[modal operators]] (Def. \ref{ModalOperator}) on the [[cohesive topos]], by (Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}).

We pronounce these as follows:

| $\phantom{A}$ [[shape modality]] $\phantom{A}$ | $\phantom{A}$ [[flat modality]] $\phantom{A}$ | $\phantom{A}$ [[sharp modality]] $\phantom{A}$ |
|--------------------|-------------------|--------------------|
|   $\phantom{A}$  $&#643; \;\coloneqq\; Disc \circ \Pi$  $\phantom{A}$ | $\phantom{A}$ $\flat \;\coloneqq\; Disc \circ \Gamma$ $\phantom{A}$  | $\phantom{A}$ $\sharp \;\coloneqq\; coDisc \circ \Gamma $ $\phantom{A}$  |
{: style='margin:auto'}


and we refer to the corresponding [[modal objects]] (Def. \ref{ModalObjects}) as follows:

* a [[flat modality|flat]]-[[comodal object]]

  $$
    \flat X \underoverset{\simeq}{\phantom{A}\epsilon^\flat_X \phantom{A}}{\longrightarrow} X
  $$

  is called a _[[discrete object]]_;

* a [[sharp modality|sharp]]-[[modal object]]

  $$
    X \underoverset{\simeq}{\phantom{A}\eta^\sharp_X\phantom{A}}{\longrightarrow} \sharp X
  $$

  is called a _[[codiscrete object]]_;

* a [[sharp modality|sharp]]-[[modal objects|submodal object]]

  $$
    X \underoverset{mono}{\phantom{A}\eta^\sharp_X\phantom{A}}{\longrightarrow} \sharp X
  $$

  is a _[[concrete object]]_.

=--


+-- {: .num_prop #PiecesHavePoints}
###### Proposition
**([[pieces have points]] $\simeq$ [[discrete objects are concrete]] $\simeq$ [[Aufhebung]] of [[bottom]] [[adjoint modality]])**

Let $\mathbf{H}$ be a [[cohesive topos]] (Def. \ref{CohesiveTopos}). Then the following conditions are equivalent:

1. **[[pieces have points]]**: For every [[object]] $X \in \mathbf{H}$, _comparison of extremes_-transformation (eq:OppositeExtrmeComparison) for the $(&#643;, \dashv \flat)$-[[adjoint modality]] (eq:OppositeExtrmeComparison), hence the $\flat$-[[counit of an adjunction]] [[composition|composed]] with the &#643;-[[unit of an adjunction|unit]]

   $$
     \flat X
       \overset{ \phantom{AA} \epsilon^\flat_X \phantom{AA} }{\longrightarrow}
     X
       \overset{ \phantom{AA} \epsilon^&#643;_X \phantom{AA} }{\longrightarrow}
     &#643; X
   $$

   is an [[epimorphism]] (Def. \ref{Monomorphism})

1. **[[discrete objects are concrete]]**: For every [[object]] $X \in \mathbf{H}$, we have that its [[discrete object]] $\flat X$ is a [[concrete object]] (Def. \ref{CohesiveModalities}).

1. **[[Aufhebung]] of [[bottom]] [[adjoint modality]]**

   The [[adjoint modality]] $\flat \dashv \sharp$ exhibits [[Aufhebung]] (Def. \ref{Aufhebung}) of the [[bottom]] [[adjoint modality]] (Example \ref{InitialAndFinalAdjointModality}), i.e. the [[initial object]] (Def. \ref{InitialObject}) is [[codiscrete object|codiscrete]] (Def. \ref{CohesiveModalities}):

   $$
     \sharp \emptyset \;\simeq\; \emptyset
     \,.
   $$

=--

+-- {: .proof}
###### Proof

The comparison morphism $ptp_{\mathbf{H}}$ is a special case of that discussed in Prop. \ref{ComparisonMorphismBetweenOppositeExtremes}. First observe, in the notation there, that

$$
  ptp_{\mathbf{H}} \;\; \text{is epi}
  \phantom{AAA}
  \text{iff}
  \phantom{AAA}
  ptp_{\mathbf{B}} \;\; \text{is epi}
  \,.
$$

In one direction, assume that $ptp_{\mathbf{B}}$ is an epimorphism. By (eq:PiecesToPointsFromBase) we have $ptp_{\mathbf{H}} = Disc(ptp_{\mathbf{B}})$, but $Disc$ is a [[left adjoint]] and left adjoints preserve monomorphisms (Prop. \ref{LeftAdjointFunctorPreservesEpi}).

In the other direction, assume that $ptp_{\mathbf{H}}$ is an epimorphism. By (eq:PointsToPiecesInTheBase) and (eq:AdjunctOfptpH) we see that $ptp_{\mathbf{B}}$ is re-obtained from this by applying $\Gamma$ and then composition with isomorphisms. But $\Gamma$ is again a left adjoint, and hence preserves epimorphism by Prop. \ref{LeftAdjointFunctorPreservesEpi}, as does composition with isomorphisms.

By applying (eq:PointsToPiecesInTheBase) again, we find in particular that _[[pieces have points]]_ is also equivalent to $\Pi \epsilon^\flat_{Disc S}$ being an epimorphism, for all $S \in \mathbf{B}$. But this is equivalent to

$$
  Hom_{\mathbf{B}}(\Pi \epsilon^\flat_{\mathbf{X}}, S)
  =
  Hom_{\mathbf{\mathbf{H}}}(\epsilon^\flat_{\mathbf{X}}, Disc(S))
$$

being a [[monomorphism]] for all $S$ (by adjunction isomorphism (eq:HomIsomorphismForAdjointFunctors) and definition of [[epimorphism]], Def. \ref{Monomorphism}).

Now by Lemma \ref{ReExpressingMiddleFunctorInAdjointTriple}, this is equivalent to

$$
  Hom_{\mathbf{H}}( \mathbf{X}, \eta^\sharp_{Disc(S)} )
$$

being an injection for all $\mathbf{X}$, which, by Def. \ref{Monomorphism}, is equivalent to $\eta^\sharp_{Disc(S)}$ being a monomorphism, hence to _[[discrete objects are concrete]]_.

This establishes the equivalence between the first two items.

=--

+-- {: .num_prop #CohesiveSiteSuchThatDiscreteObjectsAreConcrete}
###### Proposition
**([[cohesive site]] such that [[pieces have points]]/[[discrete objects are concrete]])**

Let $\mathcal{C}$ be a [[cohesive site]] (Def. \ref{OneCohesiveSite}), such that

* for every [[object]] $X \in \mathcal{C}$, there is at least one [[morphism]] $\ast \overset{\exists}{\to} X$ from [[generalized the|the]] [[terminal object]] to $X$, hence such that the [[hom set]] $Hom_{\mathcal{C}}(\ast, X)$ is [[inhabited set|non-empty]].

Then the [[cohesive topos]] $Sh(\mathcal{C})$, according to Prop. \ref{CategoriesOfSheavesOnCohesiveSiteIsCohesive}, satisfies the equivalent conditions from Prop. \ref{PiecesHavePoints}:

1. [[pieces have points]],

1. [[discrete objects are concrete]].

=--


+-- {: .proof}
###### Proof

By Prop. \ref{PiecesHavePoints} it is sufficient to show the second condition, hence to check that for each [[set]] $S \in Set$, the canonical morphism

$$
  Disc(S) \longrightarrow coDisc(S)
$$

is a [[monomorphism]]. By Prop. \ref{RecognitionOfEpimorphisms} this means equivalently that for each [[object]] $X \in \mathcal{C}$ in the site, the component function

$$
  Disc(S)(X) \longrightarrow coDisc(S)(X)
$$

is an [[injective function]].

Now, by the proof of Prop. \ref{CategoriesOfSheavesOnCohesiveSiteIsCohesive}, this is the [[diagonal]] function

$$
  \array{
    S
     & \longrightarrow&
    Hom_{Set}\left( Hom_{\mathcal{C}}(\ast, X), S \right)
    \\
    s &\mapsto& const_s
  }
$$

This function is [[injective function|injective]] precisely if $Hom_{\mathcal{C}}(\ast, X)$ is [[inhabited set|non-empty]], which is true by assumption.


=--

+-- {: .num_prop #QuasitoposOfConcreteObjects}
###### Proposition
**([[quasitopos]] of [[concrete objects]] in a [[cohesive topos]])**

For $\mathbf{H}$ a [[cohesive topos]] (Def. \ref{CohesiveTopos}), write

$$
  \mathbf{H}_{conc}
  \overset{ \phantom{AAAA} }{\hookrightarrow}
  \mathbf{H}
$$

for its [[full subcategory]] (Example \ref{FullSubcategoryOnClassOfObjects}) of [[concrete objects]] (Def. \ref{CohesiveModalities}).

Then there is a sequence of [[reflective subcategory]]-inclusions (Def. \ref{ReflectiveSubcategory}) that factor the $(\Gamma \dashv coDisc)$-adjunction as

$$
  \Gamma \;\dashv\; coDisc
  \;\;\colon\;\;
  \mathbf{H}
  \array{
    \overset{\phantom{AA} conc \phantom{AA}}{\longrightarrow}
    \\
    \overset{\phantom{AA} \iota_{conc} \phantom{AA}}{\hookleftarrow}
  }
  \mathbf{H}_{conc}
  \array{
    \overset{\phantom{AA}\Gamma \phantom{AA}}{\longrightarrow}
    \\
    \overset{\phantom{AA}coDisc\phantom{AA}}{\hookleftarrow}
  }
  Set
$$

If in addition [[discrete objects are concrete]] (Prop. \ref{PiecesHavePoints}), then the full [[adjoint quadruple]] factors through the [[concrete objects]]:

$$
  \array{
     \\
     \phantom{a}
     \\
     \phantom{A}
     \\
     \Gamma \;\dashv\; coDisc
  }
  \;\;\colon\;\;
  \mathbf{H}
  \array{
    \phantom{\overset{ \phantom{AA} \Pi \phantom{AA} }{\longrightarrow}}
    \\
    \phantom{\overset{ \phantom{AA} Disc \phantom{AA} }{\hookleftarrow}}
    \\
    \overset{\phantom{AA} conc \phantom{AA}}{\longrightarrow}
    \\
    \overset{\phantom{AA} \iota_{conc} \phantom{AA}}{\hookleftarrow}
  }
  \mathbf{H}_{conc}
  \array{
    \overset{ \phantom{AA} \Pi \phantom{AA} }{\longrightarrow}
    \\
    \overset{ \phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
    \\
    \overset{\phantom{AA}\Gamma \phantom{AA}}{\longrightarrow}
    \\
    \overset{\phantom{AA}coDisc\phantom{AA}}{\hookleftarrow}
  }
  Set
$$


=--

+-- {: .proof}
###### Proof

For the adjunction on the right, we just need to observe that for every [[set]] $S \in Set$, the [[codiscrete object]] $coDisc(S)$ is [[concrete object|concrete]], which is immediate by [[idempotent monad|idempotency]] of $\sharp$ (Prop. \ref{ModalOpIdempotent}) and the fact that every [[isomorphism]] is also a [[monomorphism]]. Similarly, the assumption that [[discrete objects are concrete]] says exactly that also $Disc$ factors through $\mathbf{H}_{conc}$.

For the adjunction on the left we claim that the [[left adjoint]] $conc$, (to be called _[[concretification]]_), is given by sending each [[object]] to the [[image]] (Def. \ref{SheafToposEpiMonoFactorization}) of its $(\Gamma \dashv coDisc)$ [[adjunction unit]] $\eta^\sharp$:

$$
  conc \;\colon\; X \mapsto im(\eta^\sharp_X)
  \,,
$$

hence to the object which exhibits the [[(epi, mono) factorization system|epi/mono-factorization]] (Prop. \ref{SheafToposEpiMonoFactorization}) of $\eta^\sharp_X$

\[
  \label{ConcretificationUnitFromEpiMonoFactorization}
  \eta^\sharp_X
  \;\colon\;
  X
    \underoverset{epi}{ \eta^{conc}_X }{\longrightarrow}
  conc X
    \underoverset{mono}{}{\longrightarrow}
  \sharp X
  \,.
\]

First we need to show that $conc X$, thus defined, is indeed [[concrete object|concrete]], hence that $\eta^\sharp_{im(\eta^\sharp_X)}$ is a [[monomorphism]] (Def. \ref{Monomorphism}). For this, consider the following [[naturality square]] (eq:NaturalitySquareForAdjointnessOfFunctors) of the $\Gamma \dashv coDisc$-adjunction hom-isomorphism

\[
  \label{ConcNatur}
  \array{
    Hom_{Set}( \Gamma im(\eta^\sharp_X), \Gamma im(\eta^\sharp_X) )
    &\simeq&
    Hom_{\mathbf{H}}( im(\eta^\sharp_X), \sharp im(\eta^\sharp_X) )
    \\
    {}^{ \mathllap{ (-) \circ \Gamma(\eta^{conc}_X) } }\big\downarrow
      &&
    \big\downarrow^{
      \mathrlap{ (-) \circ \eta^{conc}_X }
    }
    \\
    Hom_{Set}( \Gamma X, \Gamma im(\eta^\sharp_X) )
    &\simeq&
    Hom_{\mathbf{H}}( X, \sharp im(\eta^\sharp_X) )
  }
  \phantom{AAAA}
  \array{
    \left\{ id_{\Gamma im(\eta^\sharp_X)} \right\}
      &\longrightarrow&
    \phantom{\sharp(\eta^{conc}_X) \circ \eta^\sharp_{ X }}
    \left\{ \eta^{\sharp}_{im(\eta^\sharp_X)} \right\}
    \\
    \big\downarrow
      &&
    \phantom{\sharp(\eta^{conc}_X) \circ \eta^\sharp_{ X }}
    \big\downarrow
    \\
    \left\{ \Gamma(\eta^{conc}_X) \right\}
      &\longrightarrow&
    \left\{
      \underset{
        iso
      }{
      \underbrace{
         \sharp(\eta^{conc}_X)
      }}
      \circ \eta^\sharp_{ X }
      \;=\;
    \eta^{\sharp}_{ im(\eta^\sharp_X) } \circ \eta^{conc}_X
    \right\}
  }
\]

By chasing the [[identity morphism]] on $\Gamma im(\eta^\sharp_X)$ through this diagram, as shown by the diagram on the right, we obtain the equality displayed in the bottom right entry, where we used the general formula for [[adjuncts]] (Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit})  and the definition $\sharp \coloneqq coDisc \circ \Gamma$ (Def. \ref{CohesiveModalities}).

But observe that $\Gamma (\eta^{conc}_X)$, and hence also $\sharp(\eta^{conc}_X)$, is an [[isomorphism]] (Def. \ref{Isomorphism}), as indicated above: Since $\Gamma$ is both a [[left adjoint]] as well as a [[right adjoint]], it preserves both [[epimorphisms]] as well as [[monomorphisms]] (Prop. \ref{LeftAdjointFunctorPreservesEpi}), hence it preserves [[image]] factorizations (Prop. \ref{SheafToposEpiMonoFactorization}). This implies that $\Gamma \eta^{conc}_X$ is the epimorphism onto the image of $\Gamma( \eta^\sharp_X )$. But by [[idempotent monad|idempotency]] of $\sharp$, the latter is an [[isomorphism]], and hence so is the epimorphism in its image factorization.

Therefore the equality in (eq:ConcNatur) says that

$$
  \begin{aligned}
    \eta^\sharp_{ X }
      & =
    \left(
      iso \circ \eta^{\sharp}_{ im(\eta^\sharp_X)}
    \right)
      \circ
    \eta^{conc}_X
    \\
    & =
    mono \circ \eta^{conc}_X
    \,,
  \end{aligned}
$$

where in the second line we remembered that $\eta^{conc}_X$ is, by definition, the epimorphism in the epi/mono-factorization of $\eta^\sharp_X$.

Now the defining property of epimorphisms (Def. \ref{Monomorphism}) allows to cancel this commmon factor on both sides, which yields

$$
  \eta^{\sharp}_{ im(\eta^\sharp_X) }
  \;=\;
  iso \circ mono
  \;=\;
  mono.
$$

This shows that $conc X \coloneqq im(\eta^\sharp_X)$ is indeed concret.

$\,$


It remains to show that this construction is [[left adjoint]] to the inclusion.
We claim that the [[adjunction unit]] (Def. \ref{AdjunctionUnitFromHomIsomorphism}) of $(conc \dashv \iota_{conc})$ is provided by $\eta^{conc}$ (eq:ConcretificationUnitFromEpiMonoFactorization).

To see this, first notice that, since the [[(epi, mono) factorization system|epi/mono-factorization]] (Prop. \ref{SheafToposEpiMonoFactorization}) is [[orthogonal factorization system|orthogonal]] and hence [[functorial factorization|functorial]], we have [[commuting diagrams]] of the form

\[
  \label{NaturalitySquareForConcretificationUnit}
  \array{
    X_1
      &\underoverset{epi}{\eta^{conc}_{X_1}}{\longrightarrow}&
    im(\eta^\sharp_{X_1})
      &\underset{mono}{\longrightarrow}&
    \sharp X_1
    \\
    \big\downarrow && \big\downarrow && \big\downarrow
    \\
    X_2
      &\underoverset{epi}{\eta^{conc}_{X_2}}{\longrightarrow}&
    im(\eta^\sharp_{X_2})
      &\underset{mono}{\longrightarrow}&
    \sharp X_2
  }
\]

Now to demonstrate the adjunction it is sufficient, by Prop. \ref{CollectionOfUniversalArrowsEquivalentToAdjointFunctor}, to show that $\eta^{conc}$ is a [[universal morphism]] in the sense of Def. \ref{UniversalArrow}. Hence consider any morphism $f \;\colon\; X_1 \to X_2$ with $X_2 \in \mathbf{H}_{conc} \hookrightarrow \mathbf{H}$. Then we need to show that there is a unique diagonal morphism as below, that makes the following _top left triangle_ [[commuting diagram|commute]]:

$$
  \array{
    X_1
      &\overset{\phantom{AA} f \phantom{AA}}{\longrightarrow}&
    X_2
    \\
    {}^{\mathllap{epi}}\big\downarrow^{\mathrlap{\eta^{conc}_{X_1}}}
      &{}^{\mathllap{\exists !}}\nearrow&
    \big\downarrow^{\mathrlap{mono}}
    \\
    im(\eta^\sharp_{X_1})
      &\underset{}{\longrightarrow}&
    \sharp X_2
  }
$$

Now, from (eq:NaturalitySquareForConcretificationUnit), we have a [[commuting square]] as shown. Here the left morphism is an [[epimorphism]] by construction, while the right morphism is a [[monomorphism]] by assumption on $X_2$. With this, the [[(epi, mono) factorization system|epi/mono-factorization]] in Prop. \ref{SheafToposEpiMonoFactorization} says that there is a diagonal [[lift]] which makes _both_ triangles [[commuting diagram|commute]].

It remains to see that the lift is unique with just the property of making the top left triangle commute. But this is equivalently the statement that the left morphism is an epimorphism, by Def. \ref{Monomorphism}.

=--



The equivalence of the first two follows with ([Johnstone, lemma 2.1, corollary 2.2](cohesive+topos#Johnstone)). The equivalence of the first and the last is due to [Lawvere-Menni 15, lemma 4.1, lemma 4.2](cohesive+topos#LawvereMenni15).


$\,$

### Elastic toposes
 {#ElasticToposes}

+-- {: .num_defn #DifferentialCohesion}
###### Definition
**([[elastic topos]])**

Let $\mathbf{H}_{red}$ be a [[cohesive topos]] (Def. \ref{CohesiveTopos}). Then an _[[elastic topos]]_ or _[[differentially cohesive topos]]_ over $\mathbf{H}_{red}$ is a [[sheaf topos]] $\mathbf{H}$ which is

1. a [[cohesive topos]] over [[Set]],

1. equipped with a [[adjoint quadruple|quadruple]] of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) to $\mathbf{H}_{red}$ of the form

   $$
     \mathbf{H}_{red}
       \array{
         \overset{\phantom{AA} \iota_{inf} \phantom{AA} }{\hookrightarrow}
         \\
         \overset{\phantom{AA} \Pi_{inf} \phantom{AA} }{\longleftarrow}
         \\
         \overset{\phantom{AA} Disc_{inf} \phantom{AA} }{\hookrightarrow}
         \\
         \overset{\phantom{AA} \Gamma_{inf} \phantom{AA} }{\longleftarrow}
       }
     \mathbf{H} 
   $$

=--


+-- {: .num_lemma #ProgressionOfSubcategoriesOfElasticTopos}
###### Lemma
**(progression of ([[coreflective subcategory|co-]])[[reflective subcategories]] of [[elastic topos]])**

Let $\mathbf{H}$ be an [[elastic topos]] (Def. \ref{DifferentialCohesion}) over a [[cohesive topos]] $\mathbf{H}_{red}$ (Def. \ref{CohesiveTopos}):

$$
  Set
    \array{
      \overset{\phantom{A} \Pi_{red} \phantom{A} }{\longleftarrow}
      \\
      \overset{\phantom{A} Disc_{red} \phantom{A} }{\hookrightarrow}
      \\
      \overset{\phantom{A} \Gamma_{red} \phantom{A} }{\longleftarrow}
      \\
      \overset{\phantom{A} coDisc_{red} \phantom{A} }{\hookrightarrow}
    }
  \mathbf{H}_{red}
    \array{
      \overset{\phantom{AA} \iota_{inf} \phantom{AA} }{\hookrightarrow}
      \\
      \overset{\phantom{AA} \Pi_{inf} \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AA} Disc_{inf} \phantom{AA} }{\hookrightarrow}
      \\
      \overset{\phantom{AA} \Gamma_{inf} \phantom{AA} }{\longleftarrow}
      \\
      \phantom{A}
      \\
      \phantom{a}
    }
  \mathbf{H}
$$

and write

$$
  Set
    \array{
      \overset{\phantom{AA} \Pi \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\hookrightarrow}
      \\
      \overset{\phantom{AA} \Gamma \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookrightarrow}
    }
  \mathbf{H}
$$

for the [[adjoint quadruple]] exhibiting the [[cohesion]] of $\mathbf{H}$ itself. Then these adjoint functors arrange and decompose as in the following [[diagram]]

<center>
<img src="https://ncatlab.org/nlab/files/ProgressionOfSubcategoriesDifferentialCohesion.jpg" width="400">
</center>

=--

+-- {: .proof}
###### Proof

The identification

$$
  (Disc \dashv \Gamma)
  \;\simeq\;
  ( Disc_{inf} \circ Disc_{red} \,\dashv\, \Gamma_{red} \circ \Gamma_{inf} )
$$


follows from the essential uniqueness of the [[global section]]-[[geometric morphism]] (Example \ref{GlobalSectionsGeometricMorphism}). This implies the identifications $\Pi \simeq \Pi_{red} \circ \Pi_{inf}$ by essential uniqueness of [[adjoints]] (Prop. \ref{UniquenessOfAdjoints}).

=--

+-- {: .num_defn #DiffCohesiveModalities}
###### Definition
**([[adjoint modalities]] on [[elastic topos]])**

Given an [[elastic topos]] ([[differentially cohesive topos]]) $\mathbf{H}$ over $\mathbf{H}_{red}$ (Def. \ref{DifferentialCohesion}), [[composition]] of the functors in Lemma \ref{ProgressionOfSubcategoriesOfElasticTopos} yields, via Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}, the following [[adjoint modalities]] (Def. \ref{AdjointModality})

$$
  \Re \dashv \Im \dashv \&
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{ \Re \;\coloneqq\; \iota_{inf} \circ \Pi_{inf}  }{\longleftarrow}
      \\
      \overset{\Im \;\coloneqq\; Disc_{inf} \circ \Pi_{inf}  }{\longrightarrow}
      \\
      \overset{ \& \;\coloneqq\; Disc_{inf}  \circ \Gamma_{inf} }{\longleftarrow}
    }
  \mathbf{H}
  \,.
$$

Since $\iota_{inf}$ and $Disc_{inf}$ are [[fully faithful functors]] by assumption, these are ([[comodal operator|co-]])[[modal operators]] (Def. \ref{ModalOperator}) on the [[cohesive topos]], by (Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}).

We pronounce these as follows:

| $\phantom{A}$ [[reduction modality]] $\phantom{A}$ | $\phantom{A}$ [[infinitesimal shape modality]] $\phantom{A}$ | $\phantom{A}$ [[infinitesimal flat modality]] $\phantom{A}$ |
|--------------------|-------------------|--------------------|
|   $\phantom{A}$  $\Re \;\coloneqq\; \iota_{inf} \circ \Pi_{inf}$  $\phantom{A}$ | $\phantom{A}$ $\Im \;\coloneqq\; Disc_{inf} \circ \Pi_{inf}$ $\phantom{A}$  | $\phantom{A}$ $ \& \;\coloneqq\; Disc_{inf} \circ \Gamma_{inf} $ $\phantom{A}$  |
{: style='margin:auto'}

and we refer to the corresponding [[modal objects]] (Def. \ref{ModalObjects}) as follows:

* a [[reduction modality|reduction]]-[[comodal object]]

  $$
    \Re X
      \underoverset{\simeq}{\epsilon^\Re_X}{\longrightarrow}
    X
  $$

  is called a _[[reduced object]]_;

* an [[infinitesimal shape modality|infinitesimal shape]]-[[modal object]]

  $$
    X \underoverset{\simeq}{\phantom{A}\eta^\Im_X\phantom{A}}{\longrightarrow} \Im X
  $$

  is called a _[[coreduced object]]_.


=--


+-- {: .num_prop #ProgressionOfModalitiesOnElasticTopos}
###### Proposition
**(progression of [[adjoint modalities]] on [[elastic topos]])**

Let $\mathbf{H}$ be an [[elastic topos]] (Def. \ref{DifferentialCohesion}) and consider the corresponding [[adjoint modalities]] which it inherits

1. for being a [[cohesive topos]], from Def. \ref{CohesiveModalities},

1. for being an [[elastic topos]], from Def. \ref{DiffCohesiveModalities}:


| $\phantom{A}$ [[shape modality]] $\phantom{A}$ | $\phantom{A}$ [[flat modality]] $\phantom{A}$ | $\phantom{A}$ [[sharp modality]] $\phantom{A}$ |
|--------------------|-------------------|--------------------|
|   $\phantom{A}$  $&#643; \;\coloneqq\; Disc \circ \Pi$  $\phantom{A}$ | $\phantom{A}$ $\flat \;\coloneqq\; Disc \circ \Gamma$ $\phantom{A}$  | $\phantom{A}$ $\sharp \;\coloneqq\; coDisc \circ \Gamma $ $\phantom{A}$  |
|   |    |   |
| $\phantom{A}$ [[reduction modality]] $\phantom{A}$ | $\phantom{A}$ [[infinitesimal shape modality]] $\phantom{A}$ | $\phantom{A}$ [[infinitesimal flat modality]] $\phantom{A}$ |
|   $\phantom{A}$  $\Re \;\coloneqq\; \iota_{inf} \circ \Pi_{inf}$  $\phantom{A}$ | $\phantom{A}$ $\Im \;\coloneqq\; Disc_{inf} \circ \Pi_{inf}$ $\phantom{A}$  | $\phantom{A}$ $ \& \;\coloneqq\; Disc_{inf} \circ \Gamma_{inf} $ $\phantom{A}$  |
{: style='margin:auto'}

Then these arrange into the following progression, via the [[preorder]] on modalities from Def. \ref{PreorderOnModalities}

$$
  \array{
    \Re &\dashv& \Im &\dashv& \&
    \\
    && \vee && \vee
    \\
    && &#643; &\dashv& \flat &\dashv& \sharp
    \\
    && && \vee && \vee
    \\
    && && \emptyset &\dashv& \ast
  }
$$

where we display also the [[bottom]] [[adjoint modality]] $\emptyset \dashv \ast$ (Example \ref{InitialAndFinalAdjointModality}), for completeness.

=--

+-- {: .proof}
###### Proof

We need to show, for all $X \in \mathbf{H}$, that

1. $\flat X$ is an $\&$-[[modal object]] (Def. \ref{ModalObjects}), hence that

   $$
     \& \flat X  \;\simeq\; X
   $$

1. $&#643; X$ is an $\Im$-[[modal object]] (Def. \ref{ModalObjects}), hence that

   $$
     \Im &#643; X  \;\simeq\; X
   $$

After unwinding the definitions of the modal operators Def. \ref{CohesiveModalities} and Def. \ref{CohesiveModalities}, and using their re-identification from Lemma \ref{ProgressionOfSubcategoriesOfElasticTopos}, this comes down to the fact that

$$
  \Pi_{inf} Disc_{inf} \;\simeq\; id
  \phantom{AAA}
  \text{and}
  \phantom{AAA}
  \Gamma_{inf} Disc_{inf} \;\simeq\; id
  \,,
$$

which holds by Prop. \ref{FullyFaithfulAndInvertibleAdjoints}, since $Disc_{inf}$ is a [[fully faithful functor]] and $\Pi_{inf}$, $Gamma_{inf}$ are ([[coreflective subcategory|co-]])[[reflective subcategory|reflectors]] for it, respectively:

$$
  \begin{aligned}
    \underset{Disc_{inf} \Gamma_{inf}}{\underbrace{\;\;\;\&\;\;\;}}
    \underset{Disc \Gamma }{\underbrace{\;\;\;\flat\;\;\;}}
    &
    =
     Disc_{inf} \Gamma_{inf}
    \underset{ Disc_{inf} Disc_{red} }{\underbrace{\;\;\;\Disc\;\;\;}} \Gamma
    \\
    & =
    \underset{
      \simeq Disc
    }{
    \underbrace{
      Disc_{inf} \underset{\simeq id}{\underbrace{\Gamma_{inf} Disc_{inf}}} Disc_{red}
    }}
    \; \Gamma
    \\
    & \simeq
    \underset{ Disc }{\underbrace{ Disc_{inf} Disc_{red} }} \Gamma \mathbf{X}
    \\
    & =
    Disc \Gamma
    \\
    & = \flat
  \end{aligned}
$$

and

$$
  \array{
    \underset{
      Disc_{inf} \Pi_{inf}
    }{
    \underbrace{
      \;\;\;\Im\;\;\;
    }}
    \underset{
      Disc \Pi
    }{
    \underbrace{
      \;\;\;&#643;\;\;\;
    }
    }
    & =
    Disc_{inf}
    \Pi_{inf}
    \underset{
      Disc_{inf} Disc_{red}
    }{
    \underbrace{
      \;\;\;Disc\;\;\;
   }
   }
   \Pi
   \\
   & =
   \underset{
     \simeq Disc
   }{
   \underbrace{
   Disc_{inf}
   \underset{
     \simeq id
   }{
   \underbrace{
     \Pi_{inf}
     Disc_{inf}
   }
   }
   Disc_{red}
   }
   }
   \Pi
   \\
   & \simeq
   Disc
   \Pi
   \\
   & =
   &#643;
  }
$$

=--

$\,$

### Solid toposes
  {#SolidToposes}

+-- {: .num_defn #SuperDifferentialCohesion}
###### Definition
**([[solid topos]])**

Let $\mathbf{H}_{bos}$ be an [[elastic topos]] (Def. \ref{DifferentialCohesion}) over a [[cohesive topos]] $\mathbf{H}_{red}$ (Def. \ref{CohesiveTopos}). Then a _[[solid topos]]_ or _[[super-differentially cohesive topos]]_ over $\mathbf{H}_{bos}$ is a [[sheaf topos]] $\mathbf{H}$, which is 

1. a [[cohesive topos]] over [[Set]] (Def. \ref{CohesiveTopos}),

1. an [[elastic topos]] over $\mathbf{H}_{red}$,

1. equipped with a [[adjoint quadruple|quadruple]] of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) to $\mathbf{H}_{bos}$ of the form

   $$
     \mathbf{H}_{bos}
       \array{
         \overset{\phantom{A} even \phantom{A} }{\longleftarrow}
         \\
         \overset{\phantom{AA} \iota_{sup} \phantom{AA} }{\hookrightarrow}
         \\
         \overset{\phantom{AA} \Pi_{sup} \phantom{AA} }{\longleftarrow}
         \\
         \overset{\phantom{AA} Disc_{sup} \phantom{AA} }{\hookrightarrow}
       }
     \mathbf{H}
   $$

   hence with $\iota_{sup}$ and $Disc_{sup}$ being [[fully faithful functors]] (Def. \ref{FullyFaithfulFunctor}).


=--



+-- {: .num_lemma #ProgressionOfSubcategoriesOfSolidTopos}
###### Lemma
**(progression of ([[coreflective subcategory|co-]])[[reflective subcategories]] of [[solid topos]])**

Let $\mathbf{H}$ be a [[solid topos]] (Def. \ref{SuperDifferentialCohesion}) over an [[elastic topos]] $\mathbf{H}_{red}$ (Def. \ref{DifferentialCohesion}):

$$
  Set
    \array{
      \overset{\phantom{A} \Pi_{red} \phantom{A} }{\longleftarrow}
      \\
      \overset{\phantom{A} Disc_{red} \phantom{A} }{\hookrightarrow}
      \\
      \overset{\phantom{A} \Gamma_{red} \phantom{A} }{\longleftarrow}
      \\
      \overset{\phantom{A} coDisc_{red} \phantom{A} }{\hookrightarrow}
    }
  \mathbf{H}_{red}
    \array{
      \overset{\phantom{AA} \iota_{inf} \phantom{AA} }{\hookrightarrow}
      \\
      \overset{\phantom{AA} \Pi_{inf} \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AA} Disc_{inf} \phantom{AA} }{\hookrightarrow}
      \\
      \overset{\phantom{AA} \Gamma_{inf} \phantom{AA} }{\longleftarrow}
      \\
      \phantom{A}
      \\
      \phantom{A \atop A}
    }
  \mathbf{H}_{bos}
    \array{
      \overset{\phantom{AA} even \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AA} \iota_{sup} \phantom{AA} }{\hookrightarrow}
      \\
      \overset{\phantom{AA} \Pi_{sup} \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AA} Disc_{sup} \phantom{AA} }{\hookrightarrow}
      \\
      \overset{\phantom{AA} \Gamma_{sup} \phantom{AA} }{\longleftarrow}
      \\
      \phantom{A}
      \\
      \phantom{A \atop A}
      \\
      \phantom{A \atop A}
    }
  \mathbf{H}
$$

Then these adjoint functors arrange and decompose as shown in the following [[diagram]]:

<center>
<img src="https://ncatlab.org/nlab/files/ProgressionSubcategoriesSuperCohesion.jpg" width="540">
</center>

Here the composite [[adjoint quadruple]]

$$
  Set
    \array{
      \overset{\Pi \simeq \Pi_{red}\Pi_{inf} \Pi_{sup} }{\longleftarrow}
      \\
      \overset{Disc = Disc_{sup} Disc_{inf} Disc_{red}}{\hookrightarrow}
      \\
      \overset{\Gamma = \Gamma_{sup} \Gamma_{inf} \Gamma_{red} }{\longleftarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookrightarrow}
    }
  \mathbf{H}
$$

exhibits the [[cohesion]] of $\mathbf{H}$ over [[Set]], and the composite adjoint quadruple

$$
  \mathbf{H}_{red}
    \array{
      \overset{\iota_{sup} \iota_{inf}}{\hookrightarrow}
      \\
      \overset{\Pi_{inf} \Pi_{sup} }{\longleftarrow}
      \\
      \overset{Disc_{inf} Disc_{red}}{\hookrightarrow}
      \\
      \overset{ \Gamma_{sup} }{\longleftarrow}
    }
  \mathbf{H}
$$

exhibits the [[elastic topos|elasticity]] of $\mathbf{H}$ over $\mathbf{H}_{red}$.


=--

+-- {: .proof}
###### Proof

As in the proof of Prop. \ref{ProgressionOfSubcategoriesOfElasticTopos},  this is immediate by the essential uniqueness of adjoints (Prop. \ref{UniquenessOfAdjoints}) and of the [[global section]]-[[geometric morphism]] (Example \ref{GlobalSectionsGeometricMorphism}).

=--

+-- {: .num_defn #SuperDiffCohesiveModalities}
###### Definition
**([[adjoint modalities]] on [[solid topos]])** 

Given a [[solid topos]] $\mathbf{H}$ over $\mathbf{H}_{bos}$ (Def. \ref{SuperDifferentialCohesion}), [[composition]] of the functors in Lemma \ref{ProgressionOfSubcategoriesOfSolidTopos} yields, via Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}, the following [[adjoint modalities]] (Def. \ref{AdjointModality})

$$
  \rightrightarrows
  \;\dashv\;
  \rightsquigarrow
  \;\dashv\;
  Rh
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{ \rightrightarrows \;\coloneqq\; \iota_{sup} \circ even  }{\longleftarrow}
      \\
      \overset{\rightsquigarrow \;\coloneqq\; \iota_{sup} \circ \Pi_{sup}  }{\longrightarrow}
      \\
      \overset{ Rh \;\coloneqq\; Disc_{sup}  \circ \Pi_{sup} }{\longleftarrow}
    }
  \mathbf{H}
  \,.
$$

Since $\iota_{sup}$ and $Disc_{sup}$ are [[fully faithful functors]] by assumption,
these are ([[comodal operator|co-]])[[modal operators]] (Def. \ref{ModalOperator}) on the [[cohesive topos]], by (Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}).

We pronounce these as follows:

| $\phantom{A}$ [[fermionic modality]] $\phantom{A}$ | $\phantom{A}$ [[bosonic modality]] $\phantom{A}$ | $\phantom{A}$ [[rheonomy modality]] $\phantom{A}$ |
|--------------------|-------------------|--------------------|
|   $\phantom{A}$  $\rightrightarrows \;\coloneqq\; \iota_{sup} \circ even$  $\phantom{A}$ | $\phantom{A}$ $\rightsquigarrow \;\coloneqq\; \iota_{sup} \circ \Pi_{sup}$ $\phantom{A}$  | $\phantom{A}$ $ Rh \;\coloneqq\; Disc_{sup} \circ \Pi_{sup} $ $\phantom{A}$  |
{: style='margin:auto'}

and we refer to the corresponding [[modal objects]] (Def. \ref{ModalObjects}) as follows:


* a $\rightsquigarrow$-[[comodal object]]

  $$
    \overset{\rightsquigarrow}{X}
      \underoverset{\simeq}{\epsilon^\rightsquigarrow_X}{\longrightarrow}
    X
  $$

  is called a _[[bosonic object]]_;

* a $Rh$-[[modal object]]

  $$
    X
      \underoverset{\simeq}{ \eta^{Rh}_X}{\longrightarrow}
    Rh X
  $$

  is called a _rheonomic object_;


=--


+-- {: .num_prop #ProgressionOfModalitiesOnSolidTopos}
###### Proposition
**(progression of [[adjoint modalities]] on [[solid topos]])**

Let $\mathbf{H}$ be a [[solid topos]] (Def. \ref{SuperDifferentialCohesion}) and consider the [[adjoint modalities]] which it inherits 

1. for being a [[cohesive topos]], from Def. \ref{CohesiveModalities}, 

1. for being an [[elastic topos]], from Def. \ref{DiffCohesiveModalities},

1. for being a [[solid topos]], from Def. \ref{SuperDiffCohesiveModalities}:


| $\phantom{A}$ [[shape modality]] $\phantom{A}$ | $\phantom{A}$ [[flat modality]] $\phantom{A}$ | $\phantom{A}$ [[sharp modality]] $\phantom{A}$ |
|--------------------|-------------------|--------------------|
|   $\phantom{A}$  $&#643; \;\coloneqq\; Disc \Pi$  $\phantom{A}$ | $\phantom{A}$ $\flat \;\coloneqq\; Disc \circ \Gamma$ $\phantom{A}$  | $\phantom{A}$ $\sharp \;\coloneqq\; coDisc \circ \Gamma $ $\phantom{A}$  |
|   |   |   |
| $\phantom{A}$ **[[reduction modality]]** $\phantom{A}$ | $\phantom{A}$ **[[infinitesimal shape modality]]** $\phantom{A}$ | $\phantom{A}$ **[[infinitesimal flat modality]]** $\phantom{A}$ |
|   $\phantom{A}$  $\Re \;\coloneqq\; \iota_{sup} \iota_{inf} \circ \Pi_{inf}\Pi_{sup}$  $\phantom{A}$ | $\phantom{A}$ $\Im \;\coloneqq\; Disc_{sup} Disc_{inf} \circ \Pi_{inf} \Pi_{sup}$ $\phantom{A}$  | $\phantom{A}$ $ \& \;\coloneqq\; Disc_{sup} Disc_{inf} \circ \Gamma_{inf}\Gamma_{sup} $ $\phantom{A}$  |
|   |    |    |
| $\phantom{A}$ **[[fermionic modality]]** $\phantom{A}$ | $\phantom{A}$ **[[bosonic modality]]** $\phantom{A}$ | $\phantom{A}$ **[[rheonomy modality]]** $\phantom{A}$ |
|   $\phantom{A}$  $\rightrightarrows \;\coloneqq\; \iota_{sup} \circ even$  $\phantom{A}$ | $\phantom{A}$ $\rightsquigarrow \;\coloneqq\; \iota_{sup} \circ \Pi_{sup}$ $\phantom{A}$  | $\phantom{A}$ $ Rh \;\coloneqq\; Disc_{sup} \circ \Pi_{sup} $ $\phantom{A}$  |
{: style='margin:auto'}

Then these arrange into the following progression, via the [[preorder]] on modalities from Def. \ref{PreorderOnModalities}:

$$
  \array{    
    id &\dashv& id
    \\
    \vee && \vee
    \\
    \rightrightarrows &\dashv& \rightsquigarrow &\dashv& Rh
    \\
    && \vee && \vee
    \\
    && \Re &\dashv& \Im &\dashv& \&
    \\
    && && \vee && \vee
    \\
    && && &#643; &\dashv& \flat &\dashv& \sharp
    \\
    && && && \vee && \vee
    \\
    && && && \emptyset &\dashv& \ast
  }
$$

where we are displaying, for completeness, also the [[adjoint modalities]]  at the [[bottom]] $\emptyset \dashv \ast$ and the [[top]] $id \dashv id$   (Example \ref{InitialAndFinalAdjointModality}).

=--

+-- {: .proof}
###### Proof

By Prop. \ref{ProgressionOfModalitiesOnElasticTopos}, it just remains to show that for all [[objects]] $X \in \mathbf{H}$

1. $\Im X$ is an $Rh$-[[modal object]], hence $Rh \Im X \simeq X$,

1. $\Re X$ is a [[bosonic object]], hence $\overset{\rightsquigarrow}{\Re X} \simeq \Re X$.

The proof is directly analogous to that of Prop. \ref{ProgressionOfModalitiesOnElasticTopos}, now using the decompositions from Lemma \ref{ProgressionOfSubcategoriesOfSolidTopos}:

$$
  \begin{aligned}
    Rh \Im 
    & =
    Disc_{sup} 
    \underset{
      \simeq id
    }{
    \underbrace{
      \Pi_{sup} \;\; Disc_{sup}
    } 
    }
    Disc_{inf} \Pi_{inf} \Pi_{sup}
    \\
    & \simeq 
    Disc_{sup} Disc_{inf} \Pi_{inf} \Pi_{sup}
    \\
    & = \Im
  \end{aligned}
$$

and

$$
  \begin{aligned}
    \rightsquigarrow \Re
    & =
    \iota_{sup} 
    \underset{\simeq id}{\underbrace{
    \Pi_{sup} \;\; \iota_{sup}}}
    \iota_{inf} \Pi_{inf}\Pi_{sub}
    \\
    & \simeq
    \iota_{sup} \iota_{inf} \Pi_{inf} \Pi_{sub}    
    \\
    & \simeq \Re
  \end{aligned}
$$

=--

(...)
