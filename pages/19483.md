

## Basic notions of Topos theory
  {#BasicNotionsOfToposTheory}

We have explained in Remark \ref{PresaheavesAsGeneralizedSpaces} how [[presheaves]] on a [[category]] $\mathcal{C}$ may be thought of as _[[generalized spaces]] probe-able by the objects of $\mathcal{C}$_, and that two consistency conditions on this interpretation are provided by the [[Yoneda lemma]] (Prop. \ref{YonedaLemma}) and the resulting [[Yoneda embedding]] (Prop. \ref{YonedaEmbedding}). Here we turn to a third consistency condition that one will want to impose, namely a _locality_ or _gluing condition_ (Remark \ref{SheafConditionAsLocality} below), to be called the _[[sheaf]]_ condition (Def. \ref{SheafConditionAsLocality} below).

More in detail, we had seen that any [[category of presheaves]] $[\mathcal{C}^{op}, Set]$ is the [[free cocompletion]] of the given [[small category]] $\mathcal{C}$ (Prop. \ref{FreeCocompletion}) and hence exhibits [[generalized spaces]] $\mathbf{X} \in [\mathcal{C}^{op}, Set]$ as being glued or _[[generators and relations|generated]]_ form the "ordinary spaces" $X \in \mathcal{C}$. Further conditions to be imposed now will impose _[[generators and relations|relations]]_ among these generators, such as the locality relation embodied by the [[sheaf]]-condition.

It turns out that these relations are reflected by special properties of an [[adjunction]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) that relates [[generalized spaces]] to ordinary [[spaces]]:

**[[generalized spaces]] via [[generators and relations]]:**

| $\phantom{A}$[[free cocompletion]]$\phantom{A}$ <br/> $\phantom{A}=$[[category of presheaves|presheaves]]$\phantom{A}$  | $\phantom{A}$[[locally presentable category|loc. presentable category]]$\phantom{A}$ | $\phantom{A}$[[sheaf topos]]$\phantom{AAAA}$ |  
|-----|--|------|
| $\phantom{A}\mathbf{H} \underoverset{\underset{\phantom{AAA}}{\longrightarrow}}{\overset{}{\longleftarrow}}{\simeq} [\mathcal{C}^{op},Set]$ |  $\phantom{A}\mathbf{H} \underoverset{\underset{\text{accessible}}{\hookrightarrow}}{\overset{}{\longleftarrow}}{\bot} [\mathcal{C}^{op}, Set]$ | $\phantom{A}\mathbf{H} \underoverset{\underset{\text{accessible}}{\hookrightarrow}}{\overset{\text{left exact}}{\longleftarrow}}{\bot} [\mathcal{C}^{op}, Set]$ |
| $\phantom{A}$Prop. \ref{FreeCocompletion}$\phantom{A}$ | $\phantom{A}$Def. \ref{LocallyPresentableCategory}$\phantom{A}$ | $\phantom{A}$Prop. \ref{SheafToposViaLexReflection}$\phantom{A}$ |
|  |   |    |
| $\phantom{A}$**[[simplicial presheaves]]$\phantom{A}$** |  **$\phantom{A}$[[combinatorial model category]]$\phantom{A}$** |   **$\phantom{A}$[[model topos]]$\phantom{A}$** | 
| $\phantom{A}\mathbf{H} \underoverset{\underset{\phantom{AAA}}{\longrightarrow}}{\overset{}{\longleftarrow}}{\simeq_{Qu}} [\mathcal{C}^{op},sSet_{Qu}]_{proj}$ |  $\phantom{A}\mathbf{H} \underoverset{\underset{\text{accessible}}{\hookrightarrow}}{\overset{}{\longleftarrow}}{\bot_{Qu}} [\mathcal{C}^{op}, sSet_{Qu}]_{proj}$ | $\phantom{A}\mathbf{H} \underoverset{\underset{\text{accessible}}{\hookrightarrow}}{\overset{\text{left exact}}{\longleftarrow}}{\bot_{Qu}} [\mathcal{C}^{op}, sSet_{Qu}]_{proj}$ |
| $\phantom{A}$Example \ref{CategoriesOfSimplicialPresheaves} | $\phantom{A}$Def. \ref{BousfieldLocalizationOfModelCategories} |  $\phantom{A}$Def. \ref{ModelTopos} |   
 
$\,$

+-- {: .num_remark #SheafConditionAsLocality}
###### Remark
**([[sheaf|sheaf condition]] as [[local-to-global principle]] for [[generalized spaces]])**

If the [[objects]] of $\mathcal{C}$ are thought of as [[spaces]] of sorts, as in Remark \ref{PresaheavesAsGeneralizedSpaces}, then there is typically a notion of _locality_ in these spaces, reflected by a notion of what it means to _[[cover]]_ a given space by ("smaller") spaces (a _[[coverage]]_, Def. \ref{Coverage} below).

But if a space $X \in \mathcal{C}$ is covered, say by two other spaces $U_1, U_2 \in \mathcal{C}$, via morphisms

$$
  \array{
    U_1 && && U_2
    \\
    & {}_{\mathllap{i_1}}\searrow && \swarrow_{\mathrlap{i_2}}
    \\
    && X
  }
$$

then this must be reflected in the behaviour of the probes of any generalized space $\mathbf{Y}$ (in the sense of Remark \ref{PresaheavesAsGeneralizedSpaces}) by these test spaces:

For ease of discussion, suppose that there is a sense in which these two patches above [[intersection|intersect]] in $X$ to form a space $U_1 \cap_X U_2 \in \mathcal{C}$. Then locality of probes should imply that the ways of mapping $U_1$ and $U_2$ into $\mathbf{Y}$ such that these maps agree on the intersection $U_1 \cap_X U_2$, should be equivalent to the ways of mapping all of $X$ into $\mathbf{Y}$.

$$
  \text{locality}
  \;:\;
  \left\{
    \array{
       \text{maps from}\,U_1\,\text{and}\,U_2\,\text{to}\,\mathbf{Y}
       \\
       \text{that coincide on}\,U_1 \cap_X U_2
    }
  \right\}
  \;\simeq\;
  \left\{
    \text{maps from}\,X\,\text{into}\,\mathbf{Y}
  \right\}
$$

One could call this the condition of _locality of probes of generalized spaces probeable by objects of $\mathcal{C}$_. But the established terminology is that this is the _[[sheaf|sheaf condition]] (eq:SheafCondition) on [[presheaves]] over $\mathcal{C}$_. Those presheaves which satisfy this condition are called the _[[sheaves]]_ (Def. \ref{Sheaf} below).

=--


+-- {: .num_remark}
###### Remark
**Warning**

Most (if not all) introductions to [[sheaf theory]] insist on motivating the concept from the special case of [[sheaves on topological spaces]] (Example \ref{SheafOnATopologicalSpace} below). This is good motivation for what Grothendieck called "[[petit topos]]"-theory. The motivation above, instead, naturally leads to the "[[gros topos]]"-perspective, as in Example \ref{SmoothSetAnnounced} below, which is more useful for discussing the [[synthetic differential geometry|synthetic]] [[higher differential geometry|higher]] [[geometry of physics -- supergeometry|supergeometry]] of [[physics]]. In fact, this is the perspective of _[[functorial geometry]]_ that has been highlighted since [Grothendieck 65](functorial+geometry#Grothendieck65), but which has maybe remained underappreciated.

=--

$\,$

We now first introduce the [[sheaf]]-condition (Def. \ref{Sheaf}) below in its traditional form via "[[matching families]]" (Def. \ref{CompatibleElements} below). Then we show (Prop. \ref{CechGroupoidCoRepresents} below) how this is equivalently expressed in terms of _[[Cech groupoids]]_ (Example \ref{CechGroupoid} below). This second formulation is convenient for understanding and handling various constructions in ordinary [[topos theory]] (for instance the definition of [[cohesive sites]]) and it makes immediate the generalization to [[higher topos theory]].

$\,$

### Descent

Here we introduce the [[sheaf]]-condition (Def. \ref{Sheaf} below) in its component-description via [[matching families]] (Def. \ref{CompatibleElements} below). Then we consider some of the general key properties of the resulting [[categories of sheaves]], such as notably their "convenience", in the technical sense of Prop. \ref{PropertiesOfSheafToposes} below.

$\,$

+-- {: .num_defn #Coverage}
###### Definition
**([[coverage]] and [[site]])**

Let $\mathcal{C}$ be a [[small category]] (Def. \ref{SmallCategory}). Then a _[[coverage]]_ on $\mathcal{C}$ is

* for each [[object]] $X \in \mathcal{C}$ a [[set]] of [[indexed sets]] of [[morphisms]] into $X$

  $$
    \left\{ U_i \overset{\iota_i}{\to} X \right\}_{i \in I}
  $$

  called the _[[coverings]]_ of $X$,

such that

* for every [[covering]] $\left\{ U_i \overset{\iota_i}{\to} X \right\}_{i \in I}$ of $X$ and every [[morphism]] $Y \overset{f}{\longrightarrow} X$ there exists a _refining covering_ $\left\{ V_j \overset{\iota_j}{\to} Y \right\}_{j \in J}$ of $Y$, meaning that for each $j \in J$ there exists $i \in I$ and a morphism $V_j \overset{\iota_{j,i}}{\to} U_i$ such that

  \[
    \label{ConditionOnCoverage}
    f \circ \iota_j
     \;=\;
    \iota_i \circ \iota_{j,i}
    \phantom{AAAAAAA}
    \array{
      V_j
        &\overset{\iota_{j,i}}{\longrightarrow}&
      U_i
      \\
      {}^{\mathllap{ \iota_j }}\big\downarrow
        &&
      \big\downarrow{}^{\mathrlap{ \iota_i}}
      \\
      Y &\underset{f}{\longrightarrow}& X
    }
  \]

A [[small category]] $\mathcal{C}$ equipped with a [[coverage]] is called a _[[site]]_.
=--

+-- {: .num_example #CanonicalCoverageOnTopologicalSpaces}
###### Example
**(canonical [[coverage]] on [[topological spaces]])**

The [[category]] [[Top]] of (small) [[topological spaces]] (Example \ref{ExamplesOfConcreteCategories}) carries a [[coverage]] (Def. \ref{Coverage}) whose [[coverings]] are the usal [[open covers]] of topological spaces.

The condition (eq:ConditionOnCoverage) on a coverage is met, since the [[preimages]] of [[open subsets]] under a [[continuous function]] $f$ are again [[open subsets]], so that the preimages of an open cover consistitute an open cover of the [[domain]], such that the [[commuting diagram]]-condition (eq:ConditionOnCoverage) is immediage.

Similarly, for $X \in Top$ a fixed topological space, there is the [[site]] $Op(X)$ whose underlying [[category]] is the _[[category of opens]]_ of $X$, which is the [[thin category]] (Example \ref{PartiallyOrderedSetsAsSmallCategories}) of [[open subsets]] of $X$ and subset inclusions, and whose [[coverings]] are again the [[open covers]].


=--


+-- {: .num_example #DifferentiablyGoodOpenCoversOfSmoothManifolds}
###### Example
**(differentiably [[good open covers]] of [[smooth manifolds]])**

The [[category]] [[SmthMfd]] of [[smooth manifold]] (Example \ref{ExamplesOfConcreteCategories}) carries a [[coverage]] (Def. \ref{Coverage}), where for $X \in SmthMfd$ any [[smooth manifold]] of [[dimension]] $D \in \mathbb{N}$, its [[coverings]] are collections of [[smooth functions]] from the [[Cartesian space]] $\mathbb{R}^D$ to $X$ whose [[image]] is the inclusion of an [[open ball]].

Hence these are the usual _[[open covers]]_ of $X$, but with the extra condition that every patch is [[diffeomorphism|diffeomorphic]] to a Cartesian space (hence to a smooth [[open ball]]).

One may further constrain this and ask that also all the non-empty finite [[intersections]] of these open balls are [[diffeomorphism|diffeomorphic]] to open balls. These are the _differentiably [[good open covers]]_.

To see that these coverings satisfy the condition (eq:ConditionOnCoverage): The plain pullback of an [[open cover]] along any continuous function is again an open cover, just not necessarily by patches diffeomorphic to open balls. But every open cover may be _refined_ by one that is (see at _[[good open cover]]_), and this is sufficient for (eq:ConditionOnCoverage).

=--

Example \ref{DifferentiablyGoodOpenCoversOfSmoothManifolds} is further developed in the chapters _[[geometry of physics -- smooth sets|smooth sets]]_ and _[[geometry of physics -- smooth homotopy types|on smooth homotopy types]]_.


+-- {: .num_defn #CompatibleElements}
###### Definition
**([[matching family]] -- [[descent object]])**

Let $\mathcal{C}$ be a [[small category]] equipped with a [[coverage]], hence a [[site]] (Def. \ref{Coverage}) and consider a [[presheaf]] $\mathbf{Y} \in [\mathcal{C}^{op}, Set]$ (Example \ref{CategoryOfPresheaves}) over $\mathcal{C}$.

Given an [[object]] $X \in \mathcal{C}$ and a [[covering]] $\left\{ U_i \overset{\iota_i}{\to} X \right\}_{i \in I}$ of it (Def. \ref{Coverage}) we say that a _[[matching family]]_ (of probes of $\mathbf{Y}$) is a [[tuple]] $(\phi_i \in \mathbf{Y}(U_i))_{i \in I}$ such that for all $i,j \in I$ and [[pairs]] of [[morphisms]] $U_i \overset{\kappa_i}{\leftarrow} V \overset{\kappa_j}{\to} U_j$ satisfying

\[
  \label{MatchingCondition}
  \iota_i \circ \kappa_i
  \;=\;
  \iota_j \circ \kappa_j
  \phantom{AAAAAAAA}
  \array{
    && V
    \\
    & {}^{\mathllap{\kappa_i}}\swarrow && \searrow^{\mathrlap{\kappa_j}}
    \\
    U_i && && U_j
    \\
    & {}_{\mathllap{\iota_i}}\searrow && \swarrow_{\mathrlap{\iota_j}}
    \\
    && X
  }
\]

we have

\[
  \label{GluingCondition}
  \mathbf{Y}(\kappa_i)(\phi_i)
  \;=\;
  \mathbf{Y}(\kappa_j)(\phi_j)
  \,.
\]

We write

\[
  \label{SetOfMatching}
  Match\big(
    \{U_i\}_{i \in I}
    \,,\,
    \mathbf{Y}
  \big)
  \subset
  \underset{i}{\prod} \mathbf{Y}(U_i)
  \;\in\;
  Set
\]

for the set of [[matching families]] for the given presheaf and covering.

This is also called the _[[descent object]]_ of $\mathbf{Y}$ for _[[descent]]_ along the [[covering]] $\{U_i \overset{\iota_i}{\to}X\}$.

=--

+-- {: .num_example #MatchingFamiliesThatGlue}
###### Example
**([[matching families]] that glue)**

Let $\mathcal{C}$ be a [[small category]] equipped with a [[coverage]], hence a [[site]] (Def. \ref{Coverage}) and consider a [[presheaf]] $\mathbf{Y} \in [\mathcal{C}^{op}, Set]$ (Example \ref{CategoryOfPresheaves}) over $\mathcal{C}$.

Given an [[object]] $X \in \mathcal{C}$ and a [[covering]] $\left\{ U_i \overset{\iota_i}{\to} X \right\}_{i \in I}$ of it (Def. \ref{Coverage}), then every element

$$
  \phi \;\in\; \mathbf{Y}(X)
$$

induces a [[matching family]] (Def. \ref{CompatibleElements}) by

$$
  \big( \mathbf{Y}(\iota_i)(\phi)  \big)_{i \in I}
  \,.
$$

(That this indeed satisfies the matching condition follows immediately by the [[functor|functoriality]] of $\mathbf{Y}$.)

This construction provides a [[function]] of the form

\[
  \label{SheafComparison}
  \mathbf{Y}(X)
    \longrightarrow
  Match\big(
    \{U_i\}_{i \in I}
    \,,\,
    \mathbf{Y}
  \big)
\]

The matching families in the image of this function are hence those [[tuples]] of probes of $\mathbf{Y}$ by the patches $U_i$ of $X$ which _glue_ to a global probe out of $X$.

=--



+-- {: .num_defn #Sheaf}
###### Definition
**([[sheaves]] and [[sheaf toposes]])**

Let $\mathcal{C}$ be a [[small category]] equipped with a [[coverage]], hence a [[site]] (Def. \ref{Coverage}) and consider a [[presheaf]] $\mathbf{Y} \in [\mathcal{C}^{op}, Set]$ (Example \ref{CategoryOfPresheaves}) over $\mathcal{C}$.

The presheaf $\mathbf{Y}$ is called a _[[sheaf]]_ if for every [[object]] $X \in \mathcal{C}$ and every [[covering]] $\left\{ U_i \overset{\iota_i}{\to} X \right\}_{i \in I}$ of $X$ _all [[matching families]] glue uniquely_, hence if the comparison morphism (eq:SheafComparison) is a [[bijection]]

\[
  \label{SheafCondition}
  \mathbf{Y}(X)
    \overset{\simeq}{\longrightarrow}
  Match\big(
    \{U_i\}_{i \in I}
    \,,\,
    \mathbf{Y}
  \big)
  \,.
\]

The [[full subcategory]] (Example \ref{FullSubcategoryOnClassOfObjects}) of the [[category of presheaves]] over a given [[site]] $\mathcal{C}$, on those that are sheaves is the _[[category of sheaves]]_, denoted

\[
  \label{FullSubcategoryOfSheaves}
  Sh(\mathcal{C})
    \overset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}
  [\mathcal{C}^{op}, Set]
  \,.
\]

A [[category]] which is [[equivalence of categories|equivalent]] (Def. \ref{EquivalenceOfCategories}) to a [[category of sheaves]] is called a _[[sheaf topos]]_, or often just _[[topos]]_, for short.

For $\mathbf{H}_1$ and $\mathbf{H}_2$ two such sheaf toposes, a [[homomorphism]] $f \;\colon\; \mathbf{H}_1 \to \mathbf{H}_2$ between them, called a _[[geometric morphism]]_ is an [[adjoint pair]] of [[functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets})

\[
  \label{GeometricMorphism}
  \mathbf{H}_1
    \underoverset
      {\underset{ \phantom{AA} f_\ast \phantom{AA} }{\longrightarrow}}
      \overset{ \phantom{AA} f^\ast \phantom{AA} }{\longleftarrow}
      {}
  \mathbf{H}_2
\]

such that

* the [[left adjoint]] $f^\ast$, called the _[[inverse image]]_, [[preserved limit|preserves]] [[finite products]].

Hence there is a [[category]] _[[Topos]]_, whose [[objects]] are [[sheaf toposes]] and whose [[morphisms]] are [[geometric morphisms]].

=--

+-- {: .num_example #GlobalSectionsGeometricMorphism}
###### Example
**([[global sections]] [[geometric morphism]])**

Let $\mathbf{H}$ be a [[sheaf topos]] (Def. \ref{Sheaf}). Then there is a [[geometric morphism]] (eq:GeometricMorphism) to the [[category of sets]] (Example \ref{CategoryOfSets}), unique up to [[natural isomorphism]] (Def. \ref{NaturalTransformations}):

$$
  \mathbf{H}
    \underoverset
      {\underset{\phantom{AA}\Gamma\phantom{AA}}{\longrightarrow}}
      {\overset{L}{\hookleftarrow}}
      {\bot}
  Set
  \,.
$$

Here $\Gamma$ is called [[generalized the|the]] _[[global sections]]-[[functor]]_.


=--

+-- {: .proof}
###### Proof

Notice that every [[set]] $S \in Set$ is the [[coproduct]], indexed by itself, of the [[terminal object]] $\ast \in Set$ ([[generalized the|the]] [[singleton]]):

$$
  S \;\simeq\; \underset{s \in S}{\coprod} \ast
  \,.
$$

Since $L$ is a [[left adjoint]], it [[preserved limit|preserves]] this [[coproduct]] (Prop. \ref{AdjointsPreserveCoLimits}). Moreover, since $L$ is assumed to preserve [[finite products]], and since the [[terminal object]] is the empty [[product]] (Example \ref{TerminalObjectIsEmptyLimit}), it also preserves the terminal object. Therefore $L$ is fixed, up to [[natural isomorphism]], to act as

$$
  \array{
    L(S)
    & \simeq
    L \left( \underset{s \in S}{\coprod} \ast  \right)
    \\
    & \simeq
    \underset{s \in S}{\coprod} L(\ast)
    \\
    & \simeq
    \underset{s \in S}{\coprod} \ast
  }
  \,.
$$

This shows that $L$ exists and uniquely so, up to natural isomorphism. This implies the essential uniqueness of $\Gamma$ by uniqueness of adjoints (Prop. \ref{UniquenessOfAdjoints}).

=--


+-- {: .num_example #TrivialCoverage}
###### Example
**([[trivial coverage]])**

For $\mathcal{C}$ a [[small category]] (Def. \ref{SmallCategory}), the _trivial coverage_ on it is the [[coverage]] (Def. \ref{Coverage}) with no [[covering]] families at all, meaning that the [[sheaf|sheaf condition]] (Def. \ref{Sheaf}) over the resulting [[site]] is empty, in that _every_ [[presheaf]] is a [[sheaf]] for this coverage.

Hence the [[category of presheaves]] $[\mathcal{C}^{op},Set]$ (Example \ref{CategoryOfPresheaves}) over a site $\mathcal{C}_{triv}$ with trivial coverage is already the corresponding [[category of sheaves]], hence the corresponding [[sheaf topos]]:

$$
  Sh\left( \mathcal{C}_{triv}\right)
  \;\simeq\;
  [\mathcal{C}^{op}, Set]
  \,.
$$

=--

+-- {: .num_example }
###### Example
**([[sheaves]] on the [[terminal category]] are plain [[sets]])**

Consider the [[terminal category]] $\ast$ (Example \ref{InitialCategoryAndTerminalCategory}) equipped with its [[trivial coverage]] (Example \ref{TrivialCoverage}). Then there is a canonical [[equivalence of categories]] (Def. \ref{EquivalenceOfCategories}) between the [[category of sheaves]] on this [[site]] (Def. \ref{Sheaf}) and the [[category of sets]] (Example \ref{CategoryOfSets}):

$$
  Sh(\ast) \;\simeq\; Set
  \,.
$$

Hence the [[category of sets]] is a [[sheaf topos]].

=--

+-- {: .num_example #SheafOnATopologicalSpace}
###### Example
**([[sheaves on a topological space]] -- [[spatial topos|spatial]] [[petit toposes]])**

In the literature, the concept of (pre-)sheaf (Def. \ref{Sheaf}) is sometimes not defined relative to a [[site]], but relative to a [[topological space]]. But the latter is a special case: For $X$ a [[topological space]], consider its [[category of open subsets]] $Op(X)$ from Example \ref{CanonicalCoverageOnTopologicalSpaces}, with [[coverage]] given by the usual [[open covers]]. Then a "[[sheaf on a topological space|sheaf on this topological space]]" is a sheaf, in the sense of Def. \ref{Sheaf}, on this site of opens. One writes

$$
  Sh(X)
    \;\coloneqq\;
  Sh(Op(X))
   \overset{\phantom{AA}}{\hookrightarrow}
  [Op(X)^{op}, Set]
  \,,
$$

for short.  The [[sheaf toposes]] arising this way are also called _[[spatial toposes]]_.

=--

+-- {: .num_prop #LocalicReflection}
###### Proposition
**([[localic reflection]])**

The construction of [[categories of sheaves on a topological space]] (Example \ref{SheafOnATopologicalSpace}) extends to a [[functor]] from the [[category]] _[[Top]]_ of [[topological spaces]] and [[continuous functions]] between them (Example \ref{ExamplesOfConcreteCategories}) to the [[category]] _[[Topos]]_ of [[sheaf toposes]] and [[geometric morphisms]] between them (Example \ref{SheafOnATopologicalSpace}).

$$
  Sh(-)
  \;\colon\;
  Top \longrightarrow Topos
  \,.
$$

Moreover, when restricted to [[sober topological spaces]], this becomes a [[fully faithful functor]], hence a [[full subcategory]]-inclusion (Def. \ref{FullyFaithfulFunctor})

$$
  Sh(-)
  \;\colon\;
  SoberTop \overset{\phantom{AAA}}{\hookrightarrow} Topos
  \,.
$$

More generally, this holds for _[[locales]]_ (i.e. for "[[sober topological spaces]] not necessarily supported on points"), in which case it becomes a [[reflective subcategory]]-inclusion (Def. \ref{ReflectiveSubcategory})

$$
  Locale
    \underoverset
      {\underset{\phantom{AA} Sh(-) \phantom{AA} }{\hookrightarrow}}
      {\overset{\phantom{AAAA}}{\longleftarrow}}
      {\bot}
  Topos
$$

This says that [[categories of sheaves on topological spaces]] are but a reflection of soper topological spaces (generally: locales) and nothing more, whence they are also called _[[petit toposes]]_.

=--


+-- {: .num_example #AbelianSheaves}
###### Example
**([[abelian sheaves]])**

In the literature, sometimes sheaves are understood by default as taking values not in the [[category of sets]], but in the category of [[abelian groups]]. Combined with Example \ref{SheafOnATopologicalSpace} this means that some authors really mean "sheaf of abelian groups of the site of opens of a topological space", when they write just "sheaf".

But for $\mathcal{S}$ any [[mathematical structure]], a sheaf of $\mathcal{S}$-structured sets is equivalently an $\mathcal{S}$-structure [[internalization|internal]] to the [[category of sheaves]] according to Def. \ref{Sheaf}. In particular [[sheaves of abelian groups]] are equivalently abelian [[group objects]] in the category of sheaves of sets as discussed here.

=--

+-- {: .num_example #SmoothSetAnnounced}
###### Example
**([[smooth sets]])**

Consider the [[site]] [[SmthMfd]] of _all_ [[smooth manifolds]], from Example \ref{DifferentiablyGoodOpenCoversOfSmoothManifolds}. The [[category of sheaves]] over this (Def. \ref{Sheaf}) is [[equivalence of categories|equivalent]] to the category of _[[smooth sets]]_, discussed in the chapter _[[geometry of physics -- smooth sets]]_:

$$
  Sh(SmthMfd) \;\simeq\; SmoothSet
  \,.
$$

This is a _[[gros topos]]_, in a sense made precise by Def. \ref{CohesiveTopos} below (a _[[cohesive topos]]_).

=--

+-- {: .num_remark #OrdinarySpacesAreGeneratorsAndRelationsForGeneralizedSpaces}
###### Remark
**(ordinary [[spaces]] and their [[coverings]] are [[generators and relations]] for [[generalized spaces]])**

Given a [[site]] $\mathcal{C}$ (Def. \ref{Coverage}), then its [[presheaf topos]] $[\mathcal{C}^{op}, Set]$ (Example \ref{TrivialCoverage}) is the [[free cocompletion]] of the [[category]] $\mathcal{C}$ (Prop. \ref{FreeCocompletion}), hence the category obtained by [[free construction|freely]] forming [[colimits]] ("gluing") of objects of $\mathcal{C}$.

In contrast, the [[full subcategory]] inclusion $Sh(\mathcal{C}) \hookrightarrow [\mathcal{C}^{op}, Set]$ enforces _relations_ between these free colimits.

Therefore in total we may think of a [[sheaf topos]] $Sh(\mathcal{C})$ as obtained by [[generators and relations]] from the [[objects]] of its [[site]] $\mathcal{C}$:

* the objects of $\mathcal{C}$ are the generators;

* the [[coverings]] of $\mathcal{C}$ are the relations.



=--



+-- {: .num_prop #Sheafification}
###### Proposition
**([[sheafification]] and [[plus construction]])**

Let $\mathcal{C}$ be a [[site]] (Def. \ref{Coverage}). Then the [[full subcategory]]-inclusion (eq:FullSubcategoryOfSheaves) of the [[category of sheaves]] over $\mathcal{C}$ (Def. \ref{Sheaf}) into the [[category of presheaves]] (Example \ref{CategoryOfPresheaves}) has a [[left adjoint]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) called _[[sheafification]]_

\[
  Sh(\mathcal{C})
   \underoverset
     {\underset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}}
     {\overset{ L }{\longleftarrow}}
     {\bot}
  [\mathcal{C}^{op}, Set]
  \,.
\]


An explicit formula for [[sheafification]] is given by applying the following "[[plus construction]]" _twice_:

$$
  L(\mathbf{Y}) \simeq (\mathbf{Y}^+)^+
  \,.
$$

Here the [[plus construction]]

$$
  (-)^+
  \;\colon\;
  [\mathcal{C}^{op}, Set]
    \longrightarrow
  [\mathcal{C}^{op}, Set]
$$

is given by forming [[equivalence classes]] of sets of [[matching families]] (Def. \ref{CompatibleElements}) for all possible [[covers]] (Def. \ref{Coverage})

$$
  \mathbf{Y}^+(X)
  \;\coloneqq\;
  \left\{
    \{U_i \overset{\iota_i}{\to} X\}
    \; \text{covering}
    \;,
    \phi \in Match\left( \{U_i\}, \mathbf{Y}  \right)
  \right\}/\sim
$$

under the [[equivalence relation]] which identifies two such [[pairs]] if the two covers have a joint refinement such that the restriction of the two matching families to that joint refinement coincide.


=--




$\,$


+-- {: .num_example #InducedCoverage}
###### Example
**([[induced coverage]])

Let $\mathcal{C}$ be a [[site]] (Def. \ref{Coverage}). Then a [[full subcategory]] (Def. \ref{FullyFaithfulFunctor})

$$
  \mathcal{D}
    \hookrightarrow
  \mathcal{C}
$$

becomes a [[site]] itself, whose [[coverage]] consists of those [[coverings]] $\{U_i \overset{\iota_i}{\to} Y\}$ in $\mathcal{C}$ that happen to be in $\mathcal{D} \hookrightarrow \mathcal{C}$.


=--


+-- {: .num_defn #DenseSubsite}
###### Definition
**([[dense subsite]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be [[sites]] (Def. \ref{Coverage}) with a a [[full subcategory]]-inclusion (Def. \ref{FullyFaithfulFunctor})

$$
  \mathcal{D}
    \hookrightarrow
  \mathcal{C}
$$

and regard $\mathcal{D}$ as equipped with the [[induced coverage]] (Def. \ref{InducedCoverage}).

This is called a _[[dense subsite]]-inclusion_ if every [[object]] $X \in \mathcal{C}$ has a [[covering]] $\{U_i \overset{\iota_i}{\to} X\}_i$ such that for all $i$ the patches are in the subcategory:

$$
  U_i \;\in\; \mathcal{D} \hookrightarrow \mathcal{C}
  \,.
$$

=--



+-- {: .num_prop #ComparisonLemma}
###### Proposition
**([[comparison lemma]])**

Let $\mathcal{D} \overset{\iota}{\hookrightarrow} \mathcal{C}$ be a [[dense subsite]] inclusion (def. \ref{DenseSubsite}). Then [[precomposition]] with $\iota$ induces an [[equivalence of categories]] (Def. \ref{EquivalenceOfCategories}) between their [[categories of sheaves]] (Def. \ref{Sheaf}):

$$
  \iota^\ast
    \;\colon\;
  Sh(\mathcal{C})
    \overset{\simeq}{\longrightarrow}
  Sh(\mathcal{D})
$$

=--




+-- {: .num_prop #RecognitionOfEpimorphisms}
###### Proposition
**(recognition of [[epimorphism|epi-]]/[[monomorphism|mono-]]/[[isomorphisms]] of [[sheaves]])**

Let $\mathcal{C}$ be a [[site]] (Def. \ref{Coverage}) with $Sh(\mathcal{C})$ its [[category of sheaves]] (Def. \ref{Sheaf}).

Then a [[morphisms]] $f \;\colon\; \mathbf{X} \to \mathbf{Y}$ in $Sh(\mathcal{C})$ is

1. a [[monomorphism]] (Def. \ref{Monomorphism}) or [[isomorphism]] (Def. \ref{Isomorphism}) precisely if it is so _globally_ in that for each object $U \in \mathcal{C}$ in the site, then the component $f_U \colon \mathbf{X}(U) \to \mathbf{Y}(U)$ is an [[injection]] or [[bijection]] of [[sets]], respectively.

1.  an [[epimorphism]] (Def. \ref{Monomorphism}) precisely if it is so _locally_, in that: for all $U \in C$ there is a [[covering]] $\{p_i : U_i \to U\}_{i \in I}$ such that for all $i \in I$ and every element $y \in \mathbf{Y}(U)$ the element $f(p_i)(y)$ is in the image of $f(U_i) : \mathbf{X}(U_i) \to \mathbf{Y}(U_i)$.

=--

+-- {: .num_prop #SheafToposEpiMonoFactorization}
###### Proposition
**([[(epi, mono) factorization system|epi/mono-factorization]] through [[image]])**

Let $Sh(\mathcal{C})$ be a [[category of sheaves]] (Def. \ref{Sheaf}). Then every [[morphism]] $f \;\colon\; \mathbf{X} \to \mathbf{Y}$ factors as an [[epimorphism]] followed by a [[monomorphism]] (Def. \ref{Monomorphism}) uniquely up to unique [[isomorphism]]:

$$
  f
  \;\colon\;
  \mathbf{X}
    \overset{epi}{\longrightarrow}
  im(f)
    \overset{mono}{\longrightarrow}
  \mathbf{Y}
  \,.
$$

[[generalized the|The]] [[object]] $im(f)$, as a [[subobject]] of $\mathbf{Y}$, is called the _[[image]]_ of $f$.

In fact this is an [[orthogonal factorization system]], in that for every [[commuting square]] where the left morphism is an [[epimorphism]], and the right one a [[monomorphism]], there exists a unique [[lift]]:

\[
  \label{EpiMonoOrthogonalLifting}
  \array{
    A &\overset{\phantom{AAA}}{\longrightarrow}& B
    \\
    {}^{\mathllap{epi}}\big\downarrow
      &{}^{\exists!}\nearrow&
    \big\downarrow^{\mathrlap{mono}}
    \\
    C &\underset{\phantom{AAA}}{\longrightarrow}& D
  }
\]

This implies that this is a [[functorial factorization]], in that for every [[commuting square]]

$$
  \array{
    \mathbf{X}_1 &\overset{f_1}{\longrightarrow}& \mathbf{Y}_1
    \\
    \big\downarrow && \big\downarrow
    \\
    \mathbf{X}_2 &\underset{f_2}{\longrightarrow}& \mathbf{Y}_2
  }
$$

there is an induced morphism of [[images]] such that the resulting rectangular [[commuting diagram|diagram commutes]]:

$$
  \array{
    \mathbf{X}_1 &\overset{epi}{\longrightarrow}& im(f_1) &\overset{mono}{\longrightarrow}& \mathbf{Y}_1
    \\
    \big\downarrow && \big\downarrow && \big\downarrow
    \\
    \mathbf{X}_2 &\overset{epi}{\longrightarrow}& im(f_2) &\overset{mono}{\longrightarrow}& \mathbf{Y}_2
  }
$$


=--

$\,$

We discuss some of the key properties of [[sheaf toposes]]:

+-- {: .num_prop #PropertiesOfSheafToposes}
###### Proposition
**([[sheaf toposes]] are [[cosmoi]])**

Let $\mathcal{C}$ be a [[site]] (Def. \ref{Coverage}) and  $Sh(\mathcal{C})$ its [[sheaf topos]] (Def. \ref{Sheaf}). Then:

1. All [[limits]] exist in $Sh(\mathcal{C})$ (Def. \ref{Limits}), and they are computed as limits of presheaves, via Example \ref{LimitsOfPresheavesAreComputedObjectwise}:

   $$
     \iota\left(
       \underset{\underset{d}{\longleftarrow}}{\lim} \mathbf{X}_d
     \right)
     \;\simeq\;
       \underset{\underset{d}{\longleftarrow}}{\lim} \iota(\mathbf{X}_d)
   $$

1. All [[colimits]] exist in $Sh(\mathcal{C})$ (Def. \ref{Limits}) and they are given by the [[sheafification]] (Def. \ref{Sheafification}) of the same colimits computed in the [[category of presheaves]], via Example \ref{LimitsOfPresheavesAreComputedObjectwise}:

   $$
     \underset{\underset{d}{\longrightarrow}}{\lim} \mathbf{X}_d
     \;\simeq\;
     L\left(
       \underset{\underset{d}{\longleftarrow}}{\lim} \iota(\mathbf{X}_d)
     \right)
   $$

1. The [[cartesian monoidal category|cartesian]] (Example \ref{CartesianMonoidalCategory}) [[closed monoidal category]]-structure (Def. \ref{ClosedMonoidalCategory}) on the [[category of presheaves]] $[\mathcal{C}^{op}, Set]$ from Example \ref{CartesianClosedMonoidalnessOfCategoriesOfPresheaves} restricts to sheaves:

   $$
     Sh(\mathcal{C})
       \underoverset
         {\underset{[\mathbf{X}, -]}{\longrightarrow}}
         {\overset{\mathbf{X} \times (-)}{\longleftarrow}}
         {}
     Sh(\mathcal{C})
   $$

   In particular, for $\mathbf{X}, \mathbf{Y} \in Sh(\mathcal{C})$ two [[sheaves]], their [[internal hom]] $[\mathbf{X}, \mathbf{Y}] \in Sh(\mathcal{C})$ is a [[sheaf]] given by

   $$
     [\mathbf{X}, \mathbf{Y}]
     \;\colon\;
     U
     \;\mapsto\;
     Hom_{Sh(\mathcal{C})}( y(U) \mathbf{X}, \mathbf{Y} )
     \,,
   $$

   where $y(U)$ is the [[representable presheaf|presheaf represented]] by $U \in \mathcal{C}$ (Example \ref{RepresentablePresheaves}).

This may be summarized by saying that every [[sheaf topos]] (in particular every [[category of presheaves]], by Example \ref{TrivialCoverage}) is a [[cosmos]] for [[enriched category theory]] (Def. \ref{Cosmos}).

=--


+-- {: .num_defn #LocalEpimorphism}
###### Definition
**([[local epimorphism]])**

Let $\mathcal{C}$ be a [[site]] (Def. \ref{Coverage}). Then a [[morphism]] of [[presheaves]] over $\mathcal{C}$ (Example \ref{CategoryOfPresheaves})

$$
  \mathbf{Y} \overset{\phantom{AA}f\phantom{AA}}{\longrightarrow} \mathbf{X}
  \;\;\;
  \in [\mathcal{S}^{op}, Set]
$$

is called a  _[[local epimorphism]]_ if for every [[object]] $U \in \mathcal{C}$, every [[morphism]] $y(U) \longrightarrow \mathbf{X}$
out of its [[representable presheaf|represented presheaf]] (Example \ref{RepresentablePresheaves}) has the _local [[lifting property]]_ through $f$ in that there is a [[covering]] $\big\{ U_i \overset{\iota_i}{\to} U \big\}$ (Def. \ref{Coverage}) and a [[commuting diagram]] of the form

$$
  \array{ 
    y(U_i) 
      &\overset{\phantom{AA}\exists\phantom{AA}}{\longrightarrow}& 
    \mathbf{Y}
    \\
    {}^{\mathllap{y(\iota_i)}} \Big\downarrow 
      && 
    \Big\downarrow{}^{\mathrlap{ f }}
    \\
    y(U) &\underset{\phantom{AAAA}}{\longrightarrow}& \mathbf{X}
  }
$$

=--

$\,$


### Codescent

In order to understand the sheaf condition (eq:SheafCondition) better, it is useful to consider [[Cech groupoids]] (Def. \ref{CechGroupoid} below). These are really _[[presheaves of groupoids]]_ (Def. \ref{PresheafOfGroupoids} below), a special case of the general concept of [[enriched presheaves]]. The key property of the [[Cech groupoid]] is that it co-represents the [[sheaf|sheaf condition]] (Prop. \ref{CechGroupoidCoRepresents} below). It is in this incarnation that the concept of sheaf seamlessly generalizes to [[homotopy theory]] via "[[higher stacks]]".

$\,$


+-- {: .num_defn #PresheafOfGroupoids}
###### Definition
**([[presheaves of groupoids]])**

For $\mathcal{C}$ a [[small category]] (Def. \ref{SmallCategory}) consider the [[functor category]] (Example \ref{FunctorCategory})
from the [[opposite category]] of $\mathcal{C}$ (Example \ref{OppositeCategory}) to the category [[Grpd]] of [[small groupoid|small]] [[groupoids]] (Example \ref{CategoriesOfSmallCategories})

\[
  [\mathcal{C}^{op}, Grpd]
  \,.
\]

By Example \ref{ExamplesOfCosmoi} we may regard [[Grpd]] as a [[cosmos]] for [[enriched category theory]]. Since the inclusion $Set \hookrightarrow Grpd$ (Example \ref{ReflectiveSubcategoryInclusionOfSetsIntoGroupoids}) is a [[strong monoidal functor]] (Def. \ref{LaxMonoidalFunctor}) of [[cosmoi]] (Example \ref{ExamplesOfCosmoi}), the plain category $\mathcal{C}$ may be thought of as a [[Grpd]]-[[enriched category]] (Def. \ref{TopEnrichedCategory}) and hence a functor $\mathcal{C}^{op} \to Grpd$ is equivalently a [[Grpd]]-[[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor}).

This means that the plain [[category of functors]] $[\mathcal{C}^{op}, Grpd]$ enriches to [[Grpd]]-[[enriched category]] of [[Grpd]]-[[enriched presheaves]] (Example \ref{EnrichedPresheaf}).

Hence we may speak of _[[presheaves of groupoids]]_.

=--

+-- {: .num_remark #PresheavesOfGroupoidsAsInternalGroupoidsInPresheaves}
###### Remark
**([[presheaves of groupoids]] as [[internal groupoids]] in [[presheaves]])**

From every [[presheaf of groupoids]] $\mathbf{Y} \in [\mathcal{C}^{op}, Grpd]$ (Def. \ref{PresheafOfGroupoids}), we obtain two ordinary [[presheaves]] of sets (Def. \ref{CategoryOfPresheaves}) called the

* _presheaf of objects_

  $$
    Obj_{\mathbf{Y}(-)}
    \in
    [\mathcal{C}^{op}, Set]
  $$

* the _presheaf of morphisms_

  $$
    Mor_{\mathbf{Y}(-)}
    \;\coloneqq\;
     \underset{x,y \in Obj_{\mathbf{Y}(-)}}{\coprod}
      Hom_{{\mathbf{Y}(-)}}
    \;\colon\;
    [\mathcal{C}^{op}, Set]
  $$

In more abstract language this assignment constitutes an [[equivalence of categories]]

\[
  \label{InternalGroupoidsPresheavesOfGroupoids}
  \array{
    [\mathcal{C}^{op}, Grpd]
      &\overset{\simeq}{\longrightarrow}&
    Grpd\left( [\mathcal{C}^{op}, Grpd]\right)
    \\
    \mathbf{Y}
      &\mapsto&
    \left(
      \phantom{AAA}
      \array{
       \underset{
          Mor_{\mathbf{Y}(-)}
        }{
        \underbrace{
          \underset{x,y \in Obj_{\mathbf{Y}(-)}}{\coprod}
          Hom_{{\mathbf{Y}(-)}}
        }}
        \\
        {}^{\mathllap{
          \array{(x \overset{f}{\to}y) \\ \mapsto\\  x}
         }
        }\Big\downarrow
        \;\;\;\;
        \Big\uparrow^{\mathrlap{
          \array{ x \\ \mapsto \\ x \overset{id_x}{\to} x }
        }}
        \phantom{x \overset{id_x}{\to} }
        \Big\downarrow^{ \mathrlap{
          \array{ (x \overset{f}{\to} y) \\ \mapsto \\ y }
        } }
        \\
        Obj_{\mathbf{Y}(-)}
      }
      \phantom{AAA}
    \right)
  }
  \,.
\]

from [[presheaves of groupoids]] to _[[internal groupoids]]- in the [[category of presheaves]] over $\mathcal{C}$ (Def. \ref{CategoryOfPresheaves}).


=--

+-- {: .num_example #PresaheavesOfSetsReflectiveInPresheavesOfGroupoids}
###### Example
**([[presheaves]] of [[sets]] form [[reflective subcategory]] of [[presheaves of groupoids]])**

Let $\mathcal{C}$ be a [[small category]] (Def. \ref{SmallCategory}). There is the [[reflective subcategory]]-inclusion (Def. \ref{ReflectiveSubcategory}) of the [[category of presheaves]] over $\mathcal{C}$ (Example \ref{CategoryOfPresheaves}) into the category of [[presheaves of groupoids]] over $\mathcal{C}$ (Def. \ref{PresheafOfGroupoids})

$$
  [\mathcal{C}^{op}, Set]
    \underoverset
      {\underset{\phantom{AAAA}}{\hookrightarrow}}
      {\overset{\pi_0}{\longleftarrow}}
      {\bot}
  [\mathcal{C}^{op}, Grpd]
$$

which is given over each object of $\mathcal{C}$ by the reflective inclusion of [[sets]] into [[groupoids]] (Example \ref{ReflectiveSubcategoryInclusionOfSetsIntoGroupoids}).

=--

+-- {: .num_example #CechGroupoid}
###### Example
**([[Cech groupoid]])**

Let $\mathcal{C}$ be a [[site]] (Def. \ref{Coverage}), and $X \in \mathcal{C}$ an [[object]] of that site. For each [[covering]] family $\{ U_i \overset{\iota_i}{\to} X\}$ of $X$ in the given [[coverage]], the _[[Cech groupoid]]_ is the [[presheaf of groupoids]] (Def. \ref{PresheafOfGroupoids})

$$
  C(\{U_i\})
    \;\in\;
  [\mathcal{C}^{op}, Grpd]
  \;\simeq\;
  Grpd\left( [\mathcal{C}^{op}, Set]  \right)
$$

which, regarded as an [[internal groupoid]] in the [[category of presheaves]] over $\mathcal{C}$, via (eq:InternalGroupoidsPresheavesOfGroupoids), has as [[presheaf]] of [[objects]] the [[coproduct]]

$$
  Obj_{C(\{U_i\})} \;\coloneqq\; \underset{i}{\coprod}  y(U_i)
$$

of the [[representable presheaf|presheaves represented]] (under the [[Yoneda embedding]], Prop. \ref{YonedaEmbedding}) by the [[covering]] objects $U_i$, and as [[presheaf]] of [[morphisms]] the [[coproduct]] over all [[fiber products]] of these:

$$
  Mor_{C(\{U_i\})}
    \;\coloneqq\;
  \underset{i,j}{\coprod}  y(U_i) \times_{y(X)} y(U_j)
  \,.
$$

This means equivalently that for any $V \in \mathcal{C}$ the [[groupoid]] assigned by $C(\{U_i\})$ has as set of objects [[pairs]] consisting of an index $i$ and a morphism $V \overset{\kappa_i}{\to} U_i$ in $\mathcal{C}$, and there is a unique morphism between two such objects

$$
  \kappa_i \longrightarrow \kappa_j
$$

precisely if

\[
  \label{CechMatchingCondition}
  \iota_i \circ \kappa_i
  \;=\;
  \iota_j \circ \kappa_j
  \phantom{AAAAAAAA}
  \array{
    && V
    \\
    & {}^{\mathllap{\kappa_i}}\swarrow && \searrow^{\mathrlap{\kappa_j}}
    \\
    U_i && && U_j
    \\
    & {}_{\mathllap{\iota_i}}\searrow && \swarrow_{\mathrlap{\iota_j}}
    \\
    && X
  }
\]


=--

Condition (eq:CechMatchingCondition) for [[morphisms]] in the [[Cech groupoid]] to be well-defined is verbatim the condition (eq:MatchingCondition) in the definition of [[matching families]]. Indeed, [[Cech groupoids]] serve to conveniently summarize (and then generalize) the [[sheaf|sheaf condition]] (Def. \ref{Sheaf}):

+-- {: .num_prop #CechGroupoidCoRepresents}
###### Proposition
**([[Cech groupoid]] co-represents [[matching families]] -- [[codescent]])**

For [[Grpd]] regarded as a [[cosmos]] (Example \ref{ExamplesOfCosmoi}), and $\mathcal{C}$ a [[site]] (Def. \ref{Coverage}), let

$$
  \mathbf{Y} \in [\mathcal{C}^{op}, Set] \hookrightarrow [\mathcal{C}^{op}, Grpd]
$$

be a [[presheaf]] on $\mathcal{C}$ (Example \ref{CategoryOfPresheaves}), regarded as a [[Grpd]]-[[enriched presheaf]] via Example \ref{PresaheavesOfSetsReflectiveInPresheavesOfGroupoids}, let $X \in \mathcal{C}$ be any [[object]] and $\{U_i \overset{\iota_i}{\to} X\}_i$ a [[covering]] family (Def. \ref{Coverage}) with induced [[Cech groupoid]] $C(\{U_i\}_i)$ (Example \ref{CechGroupoid}).

Then there is an [[isomorphism]]

$$
  [\mathcal{C}^{op},Grpd]
  \left(
    C\left(\{U_i\}_i\right), \, \mathbf{Y}
  \right)
  \;\simeq\;
  Match\left( \{U_i\}_i, \, \mathbf{Y} \right)
$$

between the [[hom-object|hom-groupoid]] of [[Grpd]]-[[enriched presheaves]] (Def. \ref{PointedTopologicalFunctorCategory}) and the set of [[matching families]] (Def. \ref{CompatibleElements}).

Since hence the Cech-groupoid co-represents the [[descent object]], it is sometimes called the _[[codescent object]]_ along the given covering.

Moreover, under this identification the canonical morphism

\[
  \label{CechResolution}
  C\left( \{U_i\}_i \right)
    \overset{p_{\{U_i\}_i}}{\longrightarrow}
  y(X)
\]

induces the comparison morphism (eq:SheafComparison)

$$
  \array{
    [\mathcal{C}^{op}, Grpd]\left( y(X), \, \mathbf{Y} \right)
    & \simeq &
    \mathbf{Y}(X)
    \\
    {}^{
      \mathllap{
        [\mathcal{C}^{op}, Grpd](p_{\{U_i\}_i}, \mathbf{Y})
      }
    }\downarrow && \downarrow
    \\
    [\mathcal{C}^{op},Grpd]
    \left(
      C\left(\{U_i\}_i\right), \, \mathbf{Y}
    \right)
    &\simeq&
    Match\left( \{U_i\}_i, \, \mathbf{Y} \right)
  }
  \,.
$$

In conclusion, this means that the [[presheaf]] $\mathbf{Y}$ is a [[sheaf]] (Def. \ref{Sheaf}) precisely if homming Cech groupoid projections into it produces an isomorphism:

\[
  \label{SheafIsLocalObjectWithRespectToCechCovers}
  \mathbf{Y}
  \,\text{is a sheaf}
  \phantom{AAAA}
  \Leftrightarrow
  \phantom{AAAA}
  \left[
    C\left( \{U_i\}_i \right)
    \overset{p_{\{U_i\}I}}{\to}
     y(X)
    \;,\;
    \mathbf{Y}
  \right]
  \, \text{is iso, for all covering families} \, \{U_i \to X\}
\]

One also says in this case that $\mathbf{Y}$ is a _[[local object]]
with respect to [[Cech covers]]_/

=--

+-- {: .proof}
###### Proof

By (eq:HomObjectOfEnrichedFunctorCategoryViaEnd) the hom-groupoid is computed as the [[end]]

$$
  [\mathcal{C}^{op},Grpd]
  \left(
    C\left(\{U_i\}_i\right), \, \mathbf{Y}
  \right)
  \;=\;
  \int_{V \in \mathcal{C}}
  \left[
    C\left(\{U_i\}_i\right)(V), \, \mathbf{Y}(V)
  \right]
  \,,
$$

where, by Example \ref{ExamplesOfCosmoi}, the "integrand" is the [[functor category]] (here: a [[groupoid]]) from the [[Cech groupoid]] at a given $V$ to the set (regarded as a groupoid) assigned by $\mathbf{Y}$ to $V$.

Since $\mathbf{Y}(V)$ is just a set, that functor groupoid, too, is just a set, regarded as a groupoid. Its elements are the [[functors]] $C\left(\{U_i\}_i\right)(V) \longrightarrow \mathbf{Y}(V)$, which are equivalently those  [[functions]] on sets of objects

$$
  \underset{i}{\coprod} y(U_i)(V)
  =
  Obj_{C\left(\{U_i\}_i\right)(V)}
    \longrightarrow
  Obj_{\mathbf{Y}(V)}
  =
  \mathbf{Y}(V)
$$

which respect the [[equivalence relation]] induced by the morphisms in the Cech groupoid at $V$.

Hence the hom-groupoid is a subset of the [[end]] of these [[function sets]]:

$$
  \begin{aligned}
    \int_{V \in \mathcal{C}}
    \left[
      C\left(\{U_i\}_i\right)(V), \, \mathbf{Y}(V)
    \right]
    & \hookrightarrow
    \int_{V \in \mathcal{C}}
    \left[
      \underset{i}{\coprod} y(U_i)(V), \, \mathbf{Y}(V)
    \right]
    \\
    & \simeq
    \int_{V \in \mathcal{C}}
    \underset{i}{\prod}
    \left[
       y(U_i)(V), \, \mathbf{Y}(V)
    \right]
    \\
    & \simeq
    \underset{i}{\prod}
    \int_{V \in \mathcal{C}}
    \left[
       y(U_i)(V), \, \mathbf{Y}(V)
    \right]
    \\
    & \simeq
    \underset{i}{\prod}
    \mathbf{Y}(U_i)
  \end{aligned}
$$

Here we used: first that the [[internal hom]]-functor turns colimits in its first argument into limits (Prop. \ref{InternalHomPreservesLimits}), then that [[limits commute with limits]] (Prop. \ref{LimitsCommuteWithLimits}), hence that in particular [[ends]] commute with [[products]] , and finally the [[enriched Yoneda lemma]] (Prop. \ref{YonedaReductionTopological}), which here is, via Example \ref{NaturalTransformationsViaEnds}, just the plain [[Yoneda lemma]] (Prop. \ref{YonedaLemma}). The end result is hence the same [[Cartesian product]] set that also the set of matching families is defined to be a subset of, in (eq:SetOfMatching).

This shows that an element in
$ \int_{V \in \mathcal{C}}
    \left[
      C\left(\{U_i\}_i\right)(V), \, \mathbf{Y}(V)
    \right]
$ is a [[tuple]] $(\phi_i \in \mathbf{Y}(U_i))_i$, subject to some condition. This condition is that for each $V \in \mathcal{C}$ the assignment

$$
  \array{
    C\left(\{U_i\}_i\right)(V)
      & \longrightarrow &
    \mathbf{Y}(V)
    \\
    (V \overset{\kappa_i}{\to} U_i)
    &\mapsto&
    \kappa_i^\ast \phi_i
    =
    \mathbf{Y}(\kappa_i)(\phi_i)
  }
$$

constitutes a [[functor]] of [[groupoids]].

By definition of the [[Cech groupoid]], and since the [[codomain]] is a just [[set]] regarded as a [[groupoid]], this is the case precisely if

$$
  \mathbf{Y}(\kappa_i)(\phi_i)
  \;=\;
  \mathbf{Y}(\kappa_j)(\phi_j)
  \phantom{AAAA}
  \text{for all}\, i,j
  \,,
$$

which is exactly the condition (eq:GluingCondition) that makes $(\phi_i)_i$ a matching family.

=--

$\,$

### Local presentation

We now discuss a more abstract characterization of [[sheaf toposes]], in terms of properties enjoyed by the [[adjunction]] that relates them to the corresponding [[categories of presheaves]].

+-- {: .num_defn #LocallyPresentableCategory}
###### Definition
**([[locally presentable category]])**

A [[category]] $\mathbf{H}$ (Def. \ref{Categories}) is called _[[locally presentable category|locally presentable]]_ if there exists a [[small category]] $\mathcal{C}$ (Def. \ref{SmallCategory}) and a [[reflective subcategory]]-inclusion of $\mathcal{C}$ into its [[category of presheaves]] (Example \ref{CategoryOfPresheaves})

$$
  \mathbf{H}
    \underoverset
      {\underset{\text{acc}}{\hookrightarrow}}
      {\overset{\phantom{AA}L\phantom{AA}}{\longleftarrow}}
      {\bot}
  [\mathcal{C}^{op}, Set]
$$

such that the inclusion functor is an _[[accessible functor|accessible functor]]_ in that it [[preserved limit|preserves]] $\kappa$-[[filtered colimits]] for some [[regular cardinal]] $\kappa$.

=--


+-- {: .num_prop #GiraudTheorem}
###### Proposition
**([[Giraud's theorem]])**

A [[sheaf topos]] (Def. \ref{Sheaf}) is equivalently a [[locally presentable category]] (Def. \ref{LocallyPresentableCategory}) with

1. [[universal colimits]],

1. [[effective quotients]],

1. [[disjoint coproducts]].

=--


+-- {: .num_prop #SheafToposViaLexReflection}
###### Proposition
**([[sheaf toposes are equivalently the left exact reflective subcategories of presheaf toposes]])**

Let $(\mathcal{C}, \tau)$ be a [[site]] (Def. \ref{Coverage}). 
Then the [[full subcategory]] inclusion $i \colon Sh(\mathcal{C},\tau) \hookrightarrow PSh(\mathcal{C})$ of its [[sheaf topos]] (Def. \ref{Sheaf}) into its [[category of presheaves]] is a [[reflective subcategory]] inclusion (Def. \ref{ReflectiveSubcategory}) 

$$
  Sh(\mathcal{C},\tau)
   \underoverset
     {\underset{\iota}{\hookrightarrow}}
     {\overset{\phantom{AA}L\phantom{AA}}{\longleftarrow}}
     {\bot}
  PSh(\mathcal{C})
$$

such that:

1. the inclusion $\iota$ is an [[accessible functor]], thus exhibiting $Sh(\mathcal{C},\tau)$ as a [[locally presentable category]] (Def. \ref{LocallyPresentableCategory})

1. the reflector $L \colon PSh(\mathcal{C})  \to Sh(\mathcal{C})$ (which is [[sheafification]], Prop. \ref{Sheafification}) is [[left exact functor|left exact]] ("lex") in that it [[preserved limit|preserves]] [[finite limits]].

Conversely, every [[sheaf topos]] arises this way. Hence [[sheaf toposes]] $\mathbf{H}$ are equivalently the [[left exact functor|left exact]]-[[reflective subcategory|reflectively]] [[full subcategories]] of [[presheaf toposes]] over some [[small category]] $\mathcal{C}$:

\[
  \label{SheafToposAsLexReflection}
  \mathbf{H}
   \underoverset
     {\underset{\phantom{AA}acc\phantom{AA}}{\hookrightarrow}}
     {\overset{\phantom{AA}lex\phantom{AA}}{\longleftarrow}}
     {\bot}
  PSh(\mathcal{C})
\]
 
=--

(e.g. [Borceux 94, prop. 3.5.4, cor. 3.5.5](sheaf+toposes+are+equivalently+the+left+exact+reflective+subcategories+of+presheaf+toposes#Borceux94), [Johnstone, C.2.1.11](sheaf+toposes+are+equivalently+the+left+exact+reflective+subcategories+of+presheaf+toposes#Johnstone))


+-- {: .num_example}
###### Remark
**(left exact reflections of [[categories of presheaves]] are [[locally presentable categories]])**

In the characterization of [[sheaf toposes are equivalently the left exact reflective subcategories of presheaf toposes|sheaf toposes as left exact reflections of categories of presheaves]] in Prop. \ref{SheafToposViaLexReflection}, the [[accessible functor|accessibility]] of the inclusion, equivalently the [[locally presentable category|local presentability]] (Def. \ref{LocallyPresentableCategory}) is automatically implied (using the [[adjoint functor theorem]]), as indicated in (eq:SheafToposAsLexReflection). 

=--
