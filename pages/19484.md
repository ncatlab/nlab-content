
## Cohesive toposes
  {#Cohesive}

We have seen roughly two different kinds of [[sheaf toposes]]:

* [[categories of sheaves on a topological space|categories of sheaves on a given space]] $X$ (Example \ref{SheafOnATopologicalSpace}), which, by [[localic reflection]] (Prop. \ref{LocalicReflection}), really are just a reflection of the space $X$ in the [[category]] of [[toposes]],

  these are called _[[petit toposes]]_;

* [[categories of sheaves]] whose [[objects]] are [[generalized spaces]] (Example \ref{SmoothSetAnnounced})

  these are called _[[gros toposes]]_.

+-- {: .num_remark #CohesiveGeneralizedSpacesAsFoundations}
###### Remark
**([[cohesion|cohesive]] [[generalized spaces]] as [[foundations|foundations]] of [[geometry]])**

If we aim to lay [[foundations]] for [[geometry]], then we are interested in isolating those kinds of [[generalized spaces]] which have foundational _a priori_ meaning independent of an otherwise pre-configured notion of space.
Hence we would like to first characterize suitable [[gros toposes]], extract concepts of [[space]] from these, and only then, possibly, consider the [[localic reflection|petit topos-reflections]] of these (Prop. \ref{LocalicReflection} below).

The [[gros toposes]] of such foundational [[generalized spaces]] ought to  have an _[[internal logic]]_ that knows about _[[modalities]] of [[geometry]]_ such as _[[discrete object|discreteness]]_ or _[[concrete object|concreteness]]_. Via the formalization of [[modalities]] in Def. \ref{ModalOperator} this leads to the definiton of [[cohesive toposes]] (Def. \ref{CohesiveTopos}, Prop. \ref{PiecesHavePoints} below, due to [[Some Thoughts on the Future of Category Theory|Lawvere 91]], [Lawvere 07](#cohesive+topos#LawvereAxiomatic)).

=--

There is a further progression of [[adjoint modalities]] (Def. \ref{AdjointModality}) of [[geometry]], including the _infinitesimal_ and the _&eacute;tale_, which are formalized by _[[differential cohesion]]_ (Def. \ref{DifferentialCohesion} below).

$\,$



+-- {: .num_defn #CohesiveTopos}
###### Definition
**([[cohesive topos]])**

A [[sheaf topos]] $\mathbf{H}$ (Def. \ref{Sheaf}) is called a _[[cohesive topos]]_ if there is a [[adjoint quadruple|quadruple]] (Remark \ref{AdjointTriples}) of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) to the [[category of sets]] (Example \ref{CategoryOfSets})

\[
  \label{CohesopmAdjointQuadruple}
  \Pi_0 \dashv Disc \dashv \Gamma \dashv coDisc
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{\phantom{AAA} \Pi_0 \phantom{AAA}}{\longrightarrow}
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

1. $\Pi_0$ [[preserved limit|preserves]] [[finite products]].

=--


+-- {: .num_example #PresheavesAdjointQuadrupleOnSiteWithTerminalObject}
###### Example
**([[adjoint quadruple]] of [[presheaves]] over [[site]] with [[terminal objects]])**

Let $\mathcal{C}$ be a [[small category]] (Def. \ref{SmallCategory}) with [[finite products]] (hence with a [[terminal object]] $\ast \in \mathcal{C}$ and for any two [[objects]] $X,Y \in \mathcal{C}$ their [[Cartesian product]] $X \times Y \in \mathcal{C}$).

Then there is an [[adjoint quadruple]] (Remark \ref{AdjointTriples}) of [[functors]] between the [[category of presheaves]] over $\mathcal{C}$ (Example \ref{CategoryOfPresheaves}), and the [[category of sets]] (Example \ref{CategoryOfSets})

\[
  \label{PreaheafAdjointQuadruple}
  [\mathcal{C}, Set]
    \array{
      \overset{\phantom{AAA} \Pi_0 \phantom{AAA}}{\longrightarrow}
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

1. $\Pi_0$ preserves [[finite products]]:

   for $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$, we have a [[natural bijection]]

   $$
     \Pi_0(\mathbf{X} \times \mathbf{Y})
     \;\simeq\;
     \Pi_0(\mathbf{X}) \times \Pi_0(\mathbf{Y})
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

Equivalently, $Disc \simeq p^\ast$ is the [[constant functor|constant]] [[diagram]]-assigning functor. By uniqueness of adjoints (Prop. \ref{UniquenessOfAdjoints}) implies that $\Pi_0$ is the functor that sends a presheaf, regarded as a [[functor]] $\mathbf{Y} \;\colon\; \mathcal{C}^{op} \to Set$, to its [[colimit]]

\[
  \label{Pi0IsColimit}
  \Pi_0(\mathbf{Y})
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
      \overset{\phantom{AAA} \Pi_0 \phantom{AAA}}{\longrightarrow}
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
  \Pi_0 \dashv Disc \dashv \Gamma \dashv coDisc
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{\phantom{AAA} \Pi_0 \phantom{AAA}}{\longrightarrow}
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
      \overset{ &#643; \;\coloneqq\; Disc \circ \Pi_0  }{\hookleftarrow}
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
|   $\phantom{A}$  $&#643; \;\coloneqq\; Disc \circ Pi_0$  $\phantom{A}$ | $\phantom{A}$ $\flat \;\coloneqq\; Disc \circ \Gamma$ $\phantom{A}$  | $\phantom{A}$ $\sharp \;\coloneqq\; coDisc \circ \Gamma $ $\phantom{A}$  |
{: style='margin:auto}


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

1. **[[pieces have points]]**: For every [[object]] $X \in \mathbf{H}$, the $\flat$-[[counit of an adjunction]] [[composition|composed]] with the &#643;-[[unit of an adjunction|unit]]

   $$
     \flat X
       \overset{ \phantom{AA} \epsilon^\flat_X \phantom{AA} }{\longrightarrow}
     X
       \overset{ \phantom{AA} \epsilon^&#643;_X \phantom{AA} }{\longrightarrow}
     &#643; X
   $$

   is an [[epimorphism]] (Def. \ref{Monomorphism})

1. For every [[object]] $X \in \mathbf{H}$, the $\flat$-[[counit of an adjunction]] [[composition|composed]] with the $\sharp$-[[unit of an adjunction|unit]]

   $$
     \flat X
       \overset{ \phantom{AA} \epsilon^\flat_X \phantom{AA} }{\longrightarrow}
     X
       \overset{ \phantom{AA} \epsilon^\sharp_X \phantom{AA} }{\longrightarrow}
     \sharp X
   $$

   is a [[monomorphism]] (Def. \ref{Monomorphism})


1. **[[discrete objects are concrete]]**: For every [[object]] $X \in \mathbf{H}$, we have that its [[discrete object]] $\flat X$ is a [[concrete object]] (Def. \ref{CohesiveModalities}).

1. **[[Aufhebung]] of [[bottom]] [[adjoint modality]]**

   The [[adjoint modality]] $\flat \dashv \sharp$ exhibits [[Aufhebung]] (Def. \ref{Aufhebung}) of the [[bottom]] [[adjoint modality]] (Example \ref{InitialAndFinalAdjointModality}), i.e. the [[initial object]] (Def. \ref{InitialObject}) is [[codiscrete object|codiscrete]] (Def. \ref{CohesiveModalities}):

   $$
     \sharp \emptyset \;\simeq\; \emptyset
     \,.
   $$

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
    \phantom{\overset{ \phantom{AA} \Pi_0 \phantom{AA} }{\longrightarrow}}
    \\
    \phantom{\overset{ \phantom{AA} Disc \phantom{AA} }{\hookleftarrow}}
    \\
    \overset{\phantom{AA} conc \phantom{AA}}{\longrightarrow}
    \\
    \overset{\phantom{AA} \iota_{conc} \phantom{AA}}{\hookleftarrow}
  }
  \mathbf{H}_{conc}
  \array{
    \overset{ \phantom{AA} \Pi_0 \phantom{AA} }{\longrightarrow}
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


+-- {: .num_defn #DifferentialCohesion}
###### Definition
**([[differentially cohesive topos]])**

Let $\mathbf{H}_{red}$ be a [[cohesive topos]] (Def. \ref{CohesiveTopos}). Then a [[differentially cohesive topos]] over $\mathbf{H}_{red}$ is another [[cohesive topos]] $\mathbf{H}$, equipped with an [[adjoint quadruple|quadrupe]] of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) of the form

$$
  \mathbf{H}
    \array{
      \overset{\phantom{AA} i_! \phantom{AA} }{\hookrightarrow}
      \\
      \overset{\phantom{AA} i^\ast \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AA} i_\ast \phantom{AA} }{\hookrightarrow}
      \\
      \overset{\phantom{AA} i^! \phantom{AA} }{\longleftarrow}
    }
  \mathbf{H}_{red}
$$

=--

+-- {: .num_defn #CohesiveModalities}
###### Definition
**([[adjoint triple]] of [[adjoint modality|adjoint]] [[modal operators]] on [[differentially cohesive topos]])**

Given a [[differentially cohesive topos]] $\mathbf{H}$ over $\mathbf{H}_{red}$ (Def. \ref{DifferentialCohesion}), its [[adjoint quadruple]] of functors to and from the [[cohesive topos]] $\mathbf{H}_{red}$ (Def. \ref{CohesiveTopos}) induce, by [[composition]] of functors, an [[adjoint triple]] (Remark \ref{AdjointTriples}) of [[adjoint modalities]] (Def. \ref{AdjointModality}):

$$
  \Re \dashv \Im \dashv \&
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{ \Re \;\coloneqq\; i_! \circ i^\ast  }{\hookleftarrow}
      \\
      \overset{\flat \;\coloneqq\; i_\ast \circ i^\ast  }{\longrightarrow}
      \\
      \overset{ \sharp \;\coloneqq\; i_\ast  \circ i^! }{\hookleftarrow}
    }
  \mathbf{H}
  \,.
$$

Since $i_!$ and $i\ast$ are [[fully faithful functors]] by assumption,
these are ([[comodal operator|co-]])[[modal operators]] (Def. \ref{ModalOperator}) on the [[cohesive topos]], by (Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}).

We pronounce these as follows:

| $\phantom{A}$ [[reduction modality]] $\phantom{A}$ | $\phantom{A}$ [[infinitesimal shape modality]] $\phantom{A}$ | $\phantom{A}$ [[infinitesimal flat modality]] $\phantom{A}$ |
|--------------------|-------------------|--------------------|
|   $\phantom{A}$  $\Re \;\coloneqq\; i_! \circ i^\ast$  $\phantom{A}$ | $\phantom{A}$ $\Im \;\coloneqq\; i_\ast \circ i^\ast$ $\phantom{A}$  | $\phantom{A}$ $ \& \;\coloneqq\; i_\ast \circ i^! $ $\phantom{A}$  |
{: style='margin:auto}

and we refer to the corressponding [[modal objects]] (Def. \ref{ModalObjects}) as follows:

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
