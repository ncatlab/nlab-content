

## Basic notions of higher topos theory

We have discussed basic notions of [[topos theory]] [above](#BasicNotionsOfToposTheory) and of [[homotopy theory]] ([above](#BasicNotionsOfHomotopyTheory)). The combination of the two is _[[(infinity,1)-topos theory|higher topos theory]]_ which we discuss here. 

We had explained how [[toposes]] may be thought of as [[categories]] of [[generalized spaces]] and how [[homotopy theory]] is about relaxing the concept of [[equality]] to that of [[gauge transformation]]/[[homotopy]] and [[higher gauge transformation]]/[[higher homotopy]]. Accordingly, [[(infinity,1)-topos|higher toposes]] may be thought of as [[(infinity,1)-category|higher categories]] of [[generalized spaces]] whose probe are defined only up to [[gauge transformation]]/[[homotopy]]. Examples of such include [[orbifolds]] and [[Lie groupoids]].

(...)


### Locally presentable $\infty$-Categories
 {#LocallyPresentbableInfinityCategories}

The analog of the notion of [[locally presentable categories]] (Def. \ref{LocallyPresentableCategory}) for [[model categories]] (Def. \ref{ModelCategory}) are _[[combinatorial model categories]]_ (Def. \ref{CombinatorialModelCategory}) below. In addition to the ordinary condition of presentability of the underlying category, these are required to be _[[cofibrantly generated model category|cofibrant generation]]_ (Def. \ref{CofibrantlyGeneratedModelCategory} below) in that all [[cofibrations]] are [[retracts]] of [[relative cell complex]]-inclusions.

That this is indeed the correct [[model category]]-analog of [[locally presentable categories]] is the statement of [[Dugger's theorem]] (Def. \ref{DuggerTheorem} below). 

Hence as we pass to the [[localization of a category|localization]] of the [[very large category]] of [[combinatorial model categories]] at the [[Quillen equivalences]], we obtain a [[homotopy theory|homotopy-theoretic]] refinement of the [[very large category]] [[PrCat]] of [[locally presentable categories]]: [[Ho(CombModCat)]] (Def. \ref{HoCombModCat}). An [[object]] in [[Ho(CombModCat)]] we also refer to as a _[[locally presentable (∞,1)-category]]_, and a [[morphism]] in [[Ho(CombModCat)]] we also refer to as the [[equivalence class]] of an _[[(∞,1)-colimit]]-[[preserved limit|preserving]] [[(∞,1)-functor]]_.



$\,$

+-- {: .num_defn #CofibrantlyGeneratedModelCategory}
###### Definition
**([[cofibrantly generated model category]])**

A [[model category]] $\mathcal{C}$ (def. \ref{ModelCategory}) is called **cofibrantly generated** if there exists two [[small set|small]] [[subsets]]

$$
  I, J \subset Mor(\mathcal{C})
$$

of its class of [[morphisms]], such that

1. $I$ and $J$ have small domains according to def. \ref{ClassOfMorphismsWithSmallDomains},

1.  the (acyclic) cofibrations of $\mathcal{C}$ are precisely the [[retracts]], of $I$-[[relative cell complexes]] ($J$-relative cell complexes), def. \ref{TopologicalCCellComplex}.

=--

+-- {: .num_prop #CofibrantlyGeneratedModelCategoryLifting}
###### Proposition

For $\mathcal{C}$ a [[cofibrantly generated model category]], def. \ref{CofibrantlyGeneratedModelCategory}, with generating (acylic) cofibrations $I$ ($J$), then its classes $W, Fib, Cof$ of weak equivalences, fibrations and cofibrations are equivalently expressed as [[injective or projective morphisms]] (def. \ref{LiftingAndExtension}) this way:


1. $Cof = (I Inj) Proj$

1. $W \cap Fib = I Inj$;

1. $W \cap Cof = (J Inj) Proj$;

1. $Fib = J Inj$;


=--

+-- {: .proof}
###### Proof

It is clear from the definition that $I \subset (I Inj) Proj$, so that the closure property of prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms} gives an inclusion

$$
  Cof \subset (I Inj) Proj
  \,.
$$

For the converse inclusion, let $f \in (I Inj) Proj$. By the [[small object argument]], prop. \ref{SmallObjectArgument}, there is a factorization $f\colon \overset{\in I Cell}{\longrightarrow}\overset{I Inj}{\longrightarrow}$. Hence by assumption and by the [[retract argument]] lemma \ref{RetractArgument}, $f$ is a retract of an $I$-relative cell complex, hence is in $Cof$.

This proves the first statement. Together with the closure properties of prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}, this implies the second claim.

The proof of the third and fourth item is directly analogous, just with $J$ replaced for $I$.

=--

+-- {: .num_defn #CombinatorialModelCategory}
###### Definition
**([[combinatorial model category]])**

A _[[combinatorial model category]]_ is a [[model category]] (Def. \ref{ModelCategory}) which is 

1. [[locally presentable category|locally presentable]] (Def. \ref{LocallyPresentableCategory})

1. [[cofibrantly generated model category]] (Def. \ref{CofibrantlyGeneratedModelCategory})

=--

+-- {: .num_prop #ClassicalModelStructureOnSimplicialSetsIsCombinatorial}
###### Example
**([[classical model structure on simplicial sets]] is [[combinatorial model category]])**

The [[classical model structure on simplicial sets]] (Def. \ref{ClassesOfMorphismsOnsSetQuillen}) $sSet_{Qu}$ is a [[combinatorial model category]] (Def. \ref{CombinatorialModelCategory}).

=--

+-- {: .num_example #CategoriesOfSimplicialPresheaves}
###### Example
**([[category of simplicial presheaves]])**

Let $\mathcal{C}$ be a [[small category|small]] (Def. \ref{SmallCategory}) [[sSet]]-[[enriched category]] (Def. \ref{TopEnrichedCategory} with Example \ref{ExamplesOfCosmoi}) and consider the [[enriched presheaf category]] (Example \ref{EnrichedPresheaf})

$$
  sPSh(\mathcal{C})
  \;\coloneqq\;
  [\mathcal{C}^{op}, sSet]
$$  

This is called the _[[category of simplicial presheaves]]_ on $\mathcal{C}$.

By Prop. \ref{SimplicialSetsAsPresheavesOnTheSimplexCategory} this is [[equivalence of categories|equivalent]] (Def. \ref{AdjointEquivalenceOfCategories}) to the category of [[simplicial objects]] in the [[category of presheaves]] over $\mathcal{C}$ (Example \ref{CategoryOfPresheaves}):

\[
  \label{SimplicialObjectsInPresheavesAreSimplicialPresheaves}
  [\mathcal{C}^{op}, sSet]
  \;\simeq\;
  [\Delta^{op}, \mathcal{C}^{op}, Set]
\]

This implies for instance that if 

$$
  \mathcal{D} 
    \overset{F}{\longrightarrow} 
  \mathcal{D}
$$

a [[functor]], the induced [[adjoint triple]] (Remark \ref{AdjointTriples}) of [[sSet]]-[[enriched functor]] [[Kan extensions]] (Prop. \ref{TopologicalLeftKanExtensionBCoend})

$$
  [\mathcal{C}^{op}, sSet]
     \;
     \array{
       \underoverset{\phantom{AA}\bot\phantom{AA}}{Lan_F}{\longrightarrow}
       \\
       \underoverset{\phantom{AA}\bot\phantom{AA}}{F^\ast}{\longleftarrow}
       \\
       \underoverset{\phantom{AA}\phantom{\bot}\phantom{AA}}{Ran_F}{\longrightarrow}
     }
     \;
  [\mathcal{D}^{op}, sSet]
$$

is given simplicial-degreewise by the corresponding [[Set]]-enriched Kan extensions.

=--




+-- {: .num_prop #ModelCategoriesOfSimplicialPresheaves}
###### Proposition
**([[model categories of simplicial presheaves]])**

Let $\mathcal{C}$ be a [[small category|small]] (Def. \ref{SmallCategory}) [[sSet]]-[[enriched category]] (Def. \ref{TopEnrichedCategory} with Example \ref{ExamplesOfCosmoi}). Then the [[category of simplicial presheaves]] $[\mathcal{C}^{op}, sSet]$ (Example \ref{CategoriesOfSimplicialPresheaves}) carries the following two [[structures]] of a [[model category]] (Def. \ref{ModelCategory})

1. the _[[projective model structure on simplicial presheaves]]_

   $$
     [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
   $$

   has as [[weak equivalences]] and [[fibrations]] those [[natural transformations]] $\eta$ whose component on every [[object]] $c \in \mathcal{C}$ is a weak equivalences or fibration, respectively, in the [[classical model structure on simplicial sets]] (Def. \ref{ClassesOfMorphismsOnsSetQuillen});

1. the _[[injective model structure on simplicial presheaves]]_

   $$
     [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
   $$

   has as [[weak equivalences]] and [[cofibrations]] those [[natural transformations]] $\eta$ whose component on every [[object]] $c \in \mathcal{C}$ is a weak equivalences or cofibration, respectively, in the [[classical model structure on simplicial sets]] (Def. \ref{ClassesOfMorphismsOnsSetQuillen});

Moreover, the [[identity functors]] constitute a [[Quillen equivalence]] (Def. \ref{QuillenEquivalence}) between these two model structures

\[
  \label{QuillenEquivalenceBetweenInjectiveAndProjective}
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\overset{\phantom{AA}id\phantom{AA}}{\longleftarrow}}
      {\simeq_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
\]

=--

+-- {: .num_remark #ProjectiveCofibrationIsObjectwiseCofibration}
###### Remark

The [[Quillen adjunction]] (eq:QuillenEquivalenceBetweenInjectiveAndProjective) in Prop. \ref{ModelCategoriesOfSimplicialPresheaves}
implies in particular that

1. every projective cofibration is in particular an objectwise cofibration;

1. every injective fibration is in particular an objectwise fibration;

=--





+-- {: .num_prop #SomeProjectivelyCofibrantSimplicialPresheaves}
###### Proposition
**(some [[projective model structure on simplicial presheaves|projectively]] [[cofibrant object|cofibrant]] [[simplicial presheaves]])**

Let $\mathcal{C}$ be a [[small category|small]] (Def. \ref{SmallCategory}). Then a sufficient condition for a [[simplicial presheaf]] over $\mathcal{C}$ (Def. \ref{sSet}) 

$$
  \mathbf{X} 
  \;\in\;
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
$$

to be a [[cofibrant object]] with respect to the _projective_ [[model structure on simplicial presheaves]] (Prop. \ref{ModelCategoriesOfSimplicialPresheaves}) is that

1. $\mathbf{X}$ is degreewise a [[coproduct]] of [[representable presheaves]]

   $$
     \mathbf{X}_k \;\simeq\; \underset{i_k}{\coprod} y(X_{i_k})
   $$

1. the [[degeneracy maps]] are inclusions of [[direct summands]].

In particular every [[representable presheaf]], regarded as a simplicially constant simplicial presheaf, is projectively cofibrant.

=--

([[Universal Homotopy Theories|Dugger 00, section 9, lemma 2.7]])

The following concept of [[left Bousfield localization]] is the analog for [[model categories]] of the concept of reflection onto [[local objects]] (Def. \ref{LocalizationAtACollectionOfMorphisms}):


+-- {: .num_defn #BousfieldLocalizationOfModelCategories}
###### Definition
**([[left Bousfield localization]])**

A **[[left Bousfield localization of model categories|left Bousfield localization]]** $\mathcal{C}_{loc}$ of a [[model category]] $\mathcal{C}$ (Def. \ref{ModelCategory}) is another model category structure on the same underlying category with the same [[cofibrations]],

$$
  Cof_{loc} = Cof
$$

but more [[weak equivalences]]

$$
  W_{loc} \supset W
  \,.
$$

We say that this is localization _at $W_{loc}$_.

=--

Notice that:

+-- {: .num_prop #BasicPropertiesOfLectBousfieldLocalizations}
###### Proposition
**([[left Bousfield localization]] is [[Quillen reflection]])**

Given a [[left Bousfield localization of model categories|left Bousfield localization]] $\mathcal{C}_{loc}$ of $\mathcal{C}$ as in def. \ref{BousfieldLocalizationOfModelCategories}, then the [[identity functor]] exhibits a [[Quillen reflection]] (Def. \ref{QuillenReflection})

$$
  \mathcal{C}_{loc}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
   \mathcal{C}
   \,.
 $$

In particular, by Prop. \ref{QuillenReflectionViaReflectionOfHomotopyCategories}, the induced adjunction of [[derived functors]] (Prop. \ref{QuillenAdjunctionInducesAdjunctionOnHomotopyCategories}) exhibits a [[reflective subcategory]] inclusion of [[homotopy category of a model category|homotopy categories]] (Def. \ref{HomotopyCategoryOfAModelCategory})

   $$
     Ho(\mathcal{C}_{loc})
       \underoverset
         {\underset{\phantom{AA}\mathbb{R} id \phantom{AA}}{\hookrightarrow}}
         {\overset{\mathbb{L}id}{\longleftarrow}}
         {\bot}
     Ho(\mathcal{C})
     \,.
   $$

=--

+-- {: .proof}
###### Proof

We claim that

1. $Fib_{loc} \subset Fib$;

1. $W_{loc} \cap Fib_{loc} = W \cap Fib$;


Using the properties of the [[weak factorization systems]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#WeakFactorizationSystem)) of (acyclic cofibrations, fibrations) and (cofibrations, acyclic fibrations) for both model structures we get

$$
  \begin{aligned}
    Fib_{loc}
      &=
    (Cof_{loc} \cap W_{loc})Inj
    \\
      &\subset
    (Cof_{loc} \cap W)Inj
    \\
      & =
    Fib
  \end{aligned}
$$

and

$$
  \begin{aligned}
    Fib_{loc} \cap W_{loc}
      & =
    Cof_{loc} Inj
    \\
      & =
    Cof \, Inj
    \\
      & =
    Fib \cap W
  \end{aligned}
 \,.
$$


Next to see that the [[identity functor]] constitutes a [[Quillen adjunction]] (Def. \ref{QuillenAdjunction}): By construction, $id \colon \mathcal{C} \to \mathcal{C}_{loc}$ preserves cofibrations and acyclic cofibrations, hence is a left Quillen functor.

To see that the [[derived adjunction counit]] (Def. \ref{DerivedAdjunctionUnit})  is a [[weak equivalence]]:

Since we have an [[adjoint pair]] of [[identity functors]], the ordinary [[adjunction counit]] is the [[identity morphisms]] and hence the [[derived adjunction counit]] on a [[fibrant object]] $c$ is just a [[cofibrant resolution]]-morphism 

$$
  Q(c) \underoverset{ \in W_{\mathcal{D}} \cap Fib_{\mathcal{D}} }{p_c}{\longrightarrow} c
$$

but regarded in the model structure $\mathcal{D}_{loc}$. Hence it is sufficient to see that [[acyclic fibrations]] in $\mathcal{D}$ remain weak equivalences in the left Bousfield localized model structure. In fact they even remain acyclic fibrations, bu the first point above.

We may also easily check directly the equivalent statement (via Prop. \ref{QuillenReflectionViaReflectionOfHomotopyCategories}) that the induced adjunction of [[derived functors]] on [[homotopy category of a model category|homotopy categories]] is a [[reflective subcategory]]-inclusion: 

Since $Cof_{loc} = Cof$ the notion of [[left homotopy]] in $\mathcal{C}_{loc}$ is the same as that in $\mathcal{C}$, and hence the inclusion of the subcategory of local cofibrant-fibrant objects into the homotopy category of the original cofibrant-fibrant objects is clearly a [[full subcategory]] inclusion. Since $Fib_{loc} \subset Fib$ by the first statement above, on these cofibrant-fibrant objects the [[right derived functor]] of the identity is just the identity and hence does exhibit this inclusion.
The left adjoint to this inclusion is given by $\mathbb{L}id$, by the general properties of Quillen adjunctions (Prop. \ref{QuillenAdjunctionInducesAdjunctionOnHomotopyCategories})).

=--


+-- {: .num_example #BousfieldLocalizationIsQuillenReflection}
###### Example
**([[left Bousfield localization]] is [[Quillen reflection]])**

Let 


=--

+-- {: .proof}
###### Proof

We consider the case of [[left Bousfield localizations]], the other case is [[formal duality|formally dual]].

A left Bousfield localization is a [[Quillen adjunction]] by [[identity functors]] ([this Remark](Bousfield+localization+of+model+categories#ImmediateImpiciationsOfLeftBousfieldLocalization))

$$
  \mathcal{D}_{loc}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {{}_{\phantom{Qu}} \bot_{Qu}}
  \mathcal{D}
$$

This means that the ordinary [[adjunction counit]] is the [[identity morphisms]] and hence that the [[derived adjunction counit]] on a [[fibrant object]] $c$ is just a [[cofibrant resolution]]-morphism 

$$
  Q(c) \underoverset{ \in W_{\mathcal{D}} \cap Fib_{\mathcal{D}} }{p_c}{\longrightarrow} c
$$

but regarded in the model structure $\mathcal{D}_{loc}$. Hence it is sufficient to see that [[acyclic fibrations]] in $\mathcal{D}$ remain weak equivalences in the left Bousfield localized model structure. In fact they even remain acyclic fibrations, by [this Remark](Bousfield+localization+of+model+categories#ImmediateImpiciationsOfLeftBousfieldLocalization).

=--


The following proposition says that Definition \ref{CombinatorialModelCategory} of [[combinatorial model categories]] is indeed the suitable analog of Def. \ref{LocallyPresentableCategory} of [[locally presentable categories]]:

+-- {: .num_prop #DuggerTheorem}
###### Proposition
**([[Dugger's theorem]])**

Let $\mathcal{C}$ be a [[combinatorial model category]] (Def. \ref{CombinatorialModelCategory}). Then there exists 

1. a [[small category]] $\mathcal{S}$;

1. a [[small set]] $S \subset Mor_{[\mathcal{S}^{op}, sSet]}$ in its [[category of simplicial presheaves]] (Example \ref{CategoriesOfSimplicialPresheaves});

1 a [[Quillen equivalence]] (Def. \ref{QuillenEquivalence})

  $$
    [\mathcal{S}^{op}, sSet_{Qu}]_{proj,S}
      \underoverset
        {\underset{\phantom{AAAA}}{\longrightarrow}}
        {\overset{}{\longleftarrow}}
        {\phantom{{}_{Qu}}\simeq_{Qu}}
    \mathcal{C}  
  $$

  between $\mathcal{C}$ and the [[left Bousfield localization]] (Def. \ref{BousfieldLocalizationOfModelCategories}) of the [[projective model structure on simplicial presheaves]] over $\mathcal{C}$ (Prop. \ref{ModelCategoriesOfSimplicialPresheaves}) at the set $S$.


=--

+-- {: .num_defn #HoCombModCat}
###### Definition
**([[homotopy category]] of [[presentable (∞,1)-categories]])**

Write $CombModCat$ for the [[very large category]] whose [[objects]] are [[combinatorial model categories]] (Def. \ref{CombinatorialModelCategory}) and whose morphisms are [[left Quillen functors]] between them (Def. \ref{QuillenAdjunction}).

We write

[[Ho(CombModCat)]] $\coloneqq CombModCat\big[ QuillenEquivs^{-1}\big]$

for its [[localization]] (Def. \ref{LocalizationOfACategory}) at the [[Quillen equivalences]] (Def. \ref{QuillenEquivalence}).

We say:

* an [[object]] in [[Ho(CombModCat)]] is a _[[locally presentable (∞,1)-category]]_, 

* a [[morphism]] in [[Ho(CombModCat)]] is the _[[equivalence class]] of an _[[(∞,1)-colimit]]-[[preserved limit|preserving]] [[(∞,1)-functor]]_;

* an [[isomorphism]] in [[Ho(CombModCat)]] is an _[[equivalence of (∞,1)-categories]]_.

=--

The following example is the genralization of the [[category of sets]] (Def. \ref{CategoryOfSets}) as we pass to [[homotopy theory]]:

+-- {: .num_example #InfinityGroupoid}
###### Example
**([[∞Grpd]])**

The image of the [[classical model structure on simplicial sets]] $sSet_{Qu}$ (Def. \ref{ClassesOfMorphismsOnsSetQuillen}), which is [[combinatorial model category]] by example \ref{ClassicalModelStructureOnSimplicialSetsIsCombinatorial}, under the [[localization]] to [[Ho(CombModCat)]] (Def. \ref{HoCombModCat}), we call the [[presentable (∞,1)-category]] of _[[∞-groupoids]]_:

$$
  \array{
    CombModCat 
    &\overset{\phantom{AA}\gamma\phantom{AA}}{\longrightarrow}&
    Ho(CombModCat)
    \\
    sSet_{Qu} &\mapsto& \infty Grpd
  }
$$

=--

In order to get good control over [[left Bousfield localization]] (Def. \ref{BousfieldLocalizationOfModelCategories}) and hence over [[presentable (∞,1)-categories]] (Def. \ref{HoCombModCat}) we need the analog of Prop. \ref{ReflectiveLocalizationGivenByLocalObjects}, saying that [[reflective localization]] are reflections onto their [[full subcategories]] of [[local objects]]. For this, in turn, we need a good handle on the [[(infinity,1)-categorical hom-space|hom-infinity-groupoids]]:

+-- {: .num_defn #SimplicialModelCategory}
###### Definition
**([[simplicial model category]])**

An _[[classical model structure on simplicial sets|sSet]]${}_{Quillen}$-[[enriched model category]]_ or _[[simplicial model category]]_, for short is a [[category]] $\mathcal{C}$ (Def. \ref{Categories}) equipped with

1. the [[structure]] of an [[sSet]]-[[enriched category]] (Def. \ref{TopEnrichedCategory} via Example \ref{UnderlyingCategoryOfTopEnrichedCategory}), which is also [[tensored and cotensored category|tensored and cotensored]] over [[sSet]] (Def. \ref{TensoringAndPoweringOfTopologicallyEnrichedCopresheaves})

   (with [[sSet]] (Def. \ref{sSet}), equipped with its canonical [[structure]] of a [[cosmos]] from Prop. \ref{PropertiesOfSheafToposes}, Example \ref{ExamplesOfCosmoi}),

1. the [[structure]] of a [[model category]] (Def. \ref{ModelCategory})

such that these two structures are compatible in the following way:

* for every [[cofibration]] $X \overset{f}{\to} Y$ and every [[fibration]] $A \overset{g}{\to} B$ in $\mathcal{C}$, the induced [[pullback powering]]-morphism of [[hom-objects|hom]]-[[simplicial sets]]

  \[
    \label{SimplicialModelCategoryComparisonMorphism}
    \mathcal{C}(Y,A)
      \longrightarrow
     \mathcal{C}(X,A) 
       \underset{\mathcal{C}(X,B)}{\times}
     \mathcal{C}(Y,B)
  \]

  is a [[Kan fibration]] (Def. \ref{KanFibration}), and is a [[weak homotopy equivalence]] (Def. \ref{WeakHomotopyEquivalence}) as soon as one of the two morphisms is a [[weak equivalence]] in $\mathcal{C}$.

=--

+-- {: .num_prop #InSimplicialModelCategoryEnrichedHomIsHomotopical}
###### Proposition
**(in [[simplicial model category]] [[enriched hom-functor]] out of [[cofibrant object|cofibrant]] into [[fibrant object|fibrant]] is [[homotopical functor]])**


Let $\mathcal{C}$ be a [[simplicial model category]] (Def. \ref{SimplicialModelCategory}). 

If $Y \in \mathcal{C}$ is a [[cofibrant object]], then the [[enriched hom-functor]] (Example \ref{EnrichedHomFunctor}) out of $X$

$$
  \mathcal{C}(Y,-)
  \;\colon\; 
  \mathcal{C}
    \longrightarrow
  sSet_{Qu}
$$

preserves [[fibrations]] and [[acyclic fibrations]].

If $A \in \mathcal{C}$ is a [[fibrant object]], then the [[enriched hom-functor]] (Example \ref{EnrichedHomFunctor}) into $X$

$$
  \mathcal{C}(-,A)
  \;\colon\; 
  \mathcal{C}^{op}
    \longrightarrow
  sSet_{Qu}
$$

sends [[cofibrations]] and [[acyclic cofibrations]] in $\mathcal{C}$ to fibrations and acyclic fibrations, respectively, in the [[classical model structure on simplicial sets]].

=--

+-- {: .proof}
###### Proof

In the first case, consider the comparison morphism (eq:SimplicialModelCategoryComparisonMorphism) for $X =\emptyset$ the [[initial object]], in the second case consider it for $B = \ast$ the [[terminal object]] (Def. \ref{InitialObject})

Since $\mathcal{C}$ is a [[tensored and cotensored category]], Prop. \ref{InTensoredCotensoredCategoryInitialObjectIsEnrichedInitial} says that 

$$
  \mathcal{C}(\emptyset, -)
  \;\simeq\;
  \ast
  \phantom{AA}
  \text{and}
  \phantom{AA}
  \mathcal{C}(-,\ast)
  \;\ast\;
  \;\;\;
  \in sSet
  \,.
$$

This means that in the first case the comparison morphism 
$$
    \mathcal{C}(Y,A)
      \longrightarrow
     \mathcal{C}(X,A) 
       \underset{\mathcal{C}(X,B)}{\times}
     \mathcal{C}(Y,B)
$$
(eq:SimplicialModelCategoryComparisonMorphism) becomes equal to the top morphism in the following diagram 

$$
  \array{
    \mathcal{C}(Y,A)
       &\overset{\mathcal{C}(Y,g)}{\longrightarrow}&
    \mathcal{C}(Y,B)
    \\
    \Big\downarrow
      &&
    \Big\downarrow
    \\
    \ast &\underset{\phantom{AAA}}{\longrightarrow}& \ast
  }
$$

while in the second case it becomes equal to the left morphism in

$$
  \array{
    \mathcal{C}(Y,A)
       &\overset{\phantom{\mathcal{C}(Y,g)}}{\longrightarrow}&
    \ast
    \\
    {}^{\mathllap{ \mathcal{C}(f,A) }}\Big\downarrow
      &&
    \Big\downarrow
    \\
    \mathcal{C}(X,A) 
      &\underset{\phantom{AAA}}{\longrightarrow}& 
    \ast
  }
$$

Hence the claim follows by the defining condition on the comparison morphism in a [[simplicial model category]].

=--

+-- {: .num_defn #DerivedHomFunctorPOnSimplicialModelCategory}
###### Definition
**([[derived hom-functor]])**

Let $\mathcal{C}$ be a [[simplicial model category]] (Def. \ref{SimplicialModelCategory}). 

By Prop. \ref{InSimplicialModelCategoryEnrichedHomIsHomotopical} and by [[Ken Brown's lemma]] (Prop. \ref{KenBrownLemma}), the [[enriched hom-functor]]  (Example \ref{EnrichedHomFunctor}) has a [[right derived functor]] (Def. \ref{LeftAndRightDerivedFunctorsOnModelCategories}) when its first argument is [[cofibrant object|cofibrant]] and its second argument is [[fibrant object|fibrant]]. The combination is called the _[[derived hom-functor]]_

$$
  \mathbb{R}hom
  \;\colon\;
  Ho(\mathcal{C})^{op} \times Ho(\mathcal{C})
  \longrightarrow
  Ho(sSet_{Quillen})
$$

In view of the [[Quillen equivalence]] $sSet_{Qu} \simeq_{Qu} Top_{Qu}$ (Theorem \ref{TopsSetQuillenEquivalence}), the simplicial sets ([[Kan complexes]]) $\mathbb{R}hom(X,A)$ are also called the _[[derived hom-spaces]]_.

In the presence of [[functorial factorization|functorial]] [[cofibrant resolution]] $Q$ and [[fibrant resolution]] $P$ (Def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}) this is given by the ordinary [[enriched hom-functor]] $\mathcal{C}(-,-)$ as

$$
  \mathbb{R}hom(X,Y)
  \;\simeq\;
  \mathcal{C}(Q X, P Y)
  \,.
$$

=--


+-- {: .num_prop #RecognitionOfSimplicialQuillenAdjunction}
###### Proposition
**(recognition of [[simplicial Quillen adjunctions]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be two [[simplicial model categories]] (Def. \ref{SimplicialModelCategory}) such that $\mathcal{D}$ is also a [[left proper model category]] (Def. \ref{RightProperModelCategory}). Then for an [[sSet]]-[[enriched adjunction]] (Def. \ref{EnrichedAdjunction}) of the form

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{\phantom{AA}L\phantom{AA}}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

to be [[Quillen adjunction]] (Def. \ref{QuillenAdjunction}, hence a _[[simplicial Quillen adjunction]]_) it is sufficient that the following two conditions hold:

1. $L$ preserves [[cofibrations]],

1. $R$ preserves [[fibrant objects]]

(i.e. this already implies that $R$ preserves all [[fibrations]]).

=--

([[Higher Topos Theory|Lurie HTT, cor. A.3.7.2]])


+-- {: .num_prop #SimplicialPresheavesIsProperCombinatorialSimplicial}
###### Proposition
**([[model structure on simplicial presheaves]] is [[left proper model category|left proper]] [[combinatorial model category|combinatorial]] [[simplicial model category]])**

Let $\mathcal{C}$ be a [[small category|small]] (Def. \ref{SmallCategory}) [[sSet]]-[[enriched category]] (Def. \ref{TopEnrichedCategory} with Example \ref{ExamplesOfCosmoi}). Then the injective and projective [[model structure on simplicial presheaves]] over $\mathcal{C}$ (Prop. \ref{ModelCategoriesOfSimplicialPresheaves}) 

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
  \;,
  \phantom{A}
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
  \;\;\;
  \in 
  CombModCat
$$

are

1. [[proper model categories]] (Def. \ref{RightProperModelCategory}),

1. [[simplicial model categories]] (Def. \ref{SimplicialModelCategory}),

1. [[combinatorial model categories]] (Def. \ref{CombinatorialModelCategory}).

=--


The following is the [[model category]]-analog of the concept of _[[local objects]]_ from Def. \ref{LocalObjects}:

+-- {: .num_defn #DerivedLocalObjects}
###### Definition
**([[local objects]] and [[local morphisms]] in a [[model category]])**

Let $\mathcal{C}$ be a [[simplicial model category]] (Def. \ref{SimplicialModelCategory}) and let $S \subset Mor_{\mathcal{C}}$ be a sub-[[class]] of its class of [[morphisms]]. Then 

1. an [[object]] $A \in \mathcal{C}$ is called a (derived-)[[local object]] if for every $X \overset{s}{\to} Y \; \in S$ the value of the [[derived hom-functor]] (Def. \ref{DerivedHomFunctorPOnSimplicialModelCategory}) out of $s$ into $X$ is a [[weak equivalence]] (i.e. an [[isomorphism]] in the [[classical homotopy category]] $Ho(sSet)$)

   $$
     \mathbb{R}Hom(s,A)
     \;\colon\;
     \mathbb{R}Hom(Y,A)
       \overset{\simeq}{\longrightarrow}
     \mathbb{R}Hom(X,A)
   $$

1. a [[morphism]] $X \overset{f}{\to} Y$ in $\mathcal{C}$ is called a (derived-)[[local morphism]] if for every [[local object]] $A$ we have

   $$
     \mathbb{R}Hom(f,A)
     \;\colon\;
     \mathbb{R}Hom(Y,A)
       \overset{\simeq}{\longrightarrow}
     \mathbb{R}Hom(X,A)
   $$

=--

The following is the [[model category]]-analog of the characterization from Prop. \ref{ReflectiveLocalizationGivenByLocalObjects} of [[reflective localizations]] as reflections onto [[local objects]]: 

+-- {: .num_prop #ExistenceOfLeftBousfieldLocalization}
###### Proposition
**(existence of [[left Bousfield localization]] for [[left proper model category|left proper]] [[simplicial model category|simplicial]] [[combinatorial model categories]])**

Let $\mathcal{C}$ be a [[combinatorial model category]] (Def. \ref{CombinatorialModelCategory}) which is [[left proper model category|left proper]] (Def. \ref{RightProperModelCategory}) and [[simplicial model category|simplicial]] (Def. \ref{SimplicialModelCategory}), and let $S \subset Mor_{\mathcal{C}}$ be a [[small set]] of its [[morphisms]].

Then the [[left Bousfield localization]] (Def. \ref{BousfieldLocalizationOfModelCategories}) of $\mathcal{C}$ _at $S$_, namely at the class of $S$-[[local morphisms]] (Def. \ref{DerivedLocalObjects}) exist, to be denoted $L_S \mathcal{C}$, and it has the following properties:

1. $L_S \mathcal{C}$ is itself a [[left proper model category|left proper]] [[simplicial model category|simplicial]] [[combinatorial model category]];

1. the [[fibrant objects]] of $L_S \mathcal{C}$ are precisely those fibrant objects of $\mathcal{C}$ which in addition are $S$-[[local objects]] (Def. \ref{DerivedLocalObjects});

1. the [[homotopy category of a model category|homotopy category]] (Def. \ref{HomotopyCategoryOfAModelCategory}) of $L_S \mathcal{C}$ is the [[full subcategory]] of that of $\mathcal{C}$ on ( the [[images]] under [[localization of a category|localization]] of) the $S$-[[local objects]].

   $$
     Ho(L_S \mathcal{C})
     \hookrightarrow
     Ho(\mathcal{C})
   $$

=--



The following class of examples of [[left Bousfield localizations]] generalizes those of Def. \ref{HomotopyLocalizationOn1Categories} from [[1-categories]] to [[locally presentable (∞,1)-categories]]:

+-- {: .num_defn #HomotopyLocalizationOfCombinatorialModelCategories}
###### Definition
**([[homotopy localization]] of [[combinatorial model categories]])**

Let $\mathcal{C}$ be a [[combinatorial model category]] (Def. \ref{CombinatorialModelCategory}) which, by [[Dugger's theorem]] (Prop. \ref{DuggerTheorem}) is [[Quillen equivalence|Quillen equivalent]] to a [[left Bousfield localization]] of a [[model category of simplicial presheaves]] over some [[small category|small]] [[simplicial category]] $\mathcal{S}$

$$
  \mathcal{C}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\overset{\phantom{AA}id\phantom{AA}}{\longleftarrow}}
      {\bot_{Qu}}
  [\mathcal{S}^{op}, sSet_{Qu}]_{proj}
  \;
  \in CombModCat
  \;\text{i.e.}\;
  \mathcal{C}
    \underoverset
      {\underset{}{\hookrightarrow}}
      {\overset{\phantom{AA}L\phantom{AA}}{\longleftarrow}}
      {\bot}
   PSh_\infty(\mathcal{S})
  \;
   \in Ho(CombModCat)
$$

Let moreover 

$$
  \mathbb{A}
    \in 
  [\mathcal{S}^{op}, sSet_{Qu}]
$$ 

be any [[object]]. Then the _[[homotopy localization]]_ of $\mathcal{C}$ at $\mathbb{A}$ is the further [[left Bousfield localization]] (Def. \ref{ExistenceOfLeftBousfieldLocalization}) 
at the morphisms of the form

$$
  X \times \mathbb{A}
  \overset{p_1}{\longrightarrow}
  X
$$

for all $X \in \mathcal{S}$:

$$
  [\mathcal{S}^{op}, sSet_{Qu}]_{proj, \mathbb{A}}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\overset{\phantom{AA}id\phantom{AA}}{\longleftarrow}}
      {\bot_{Qu}}  
  [\mathcal{S}^{op}, sSet_{Qu}]_{proj}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longleftarrow}}
      {\overset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\simeq_{Qu}}
  \mathcal{C}
  \;\;\;\;
  \in
  CombModCat
  \,.
$$

The image of this [[homotopy localization]] in [[Ho(CombModCat)]] (Def. \ref{HoCombModCat}) we denote by

$$
  \mathcal{C}_{\mathbb{A}}
  \underoverset
    {\underset{\iota}{\hookrightarrow}}
    {\overset{L_{\mathbb{A}}}{\longleftarrow}}
    {\bot}
  \mathcal{C}
  \;\;\;
  \in Ho(CombModCat)
  \,.
$$


=--


### $\infty$-Modalities

The following is an [[homotopy theory|homotopy theoretic]] analog of _[[adjoint triples]]_ (Remark \ref{AdjointTriples}):

+-- {: .num_defn #QuillenAdjointTriple}
###### Definition
**([[Quillen adjoint triple]])**

Let $\mathcal{C}_1, \mathcal{C}_2, \mathcal{D}$ be [[model categories]] (Def. \ref{ModelCategory}), where $\mathcal{C}_1$ and $\mathcal{C}_2$ share the same underlying [[category]] $\mathcal{C}$, and such that the [[identity functor]] on $\mathcal{C}$ constitutes a [[Quillen equivalence]] (Def. \ref{QuillenEquivalence})

\[
  \label{EquivForQuillenAdjointTriple}
  \mathcal{C}_2 
    \underoverset
      {\underset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}}
      {\overset{ \phantom{AA}id\phantom{AA} }{\longleftarrow}}
      {{}_{\phantom{Qu}}\simeq_{Qu}}
  \mathcal{C}_1
\]

Then a _[[Quillen adjoint triple]]_

$$
  \mathcal{C}_1
    \underoverset
      {{\longleftarrow}}
      {\overset{L}{\longrightarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$
$$
  \mathcal{C}_2
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{C}{\longleftarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$

is a [[pair]] of [[Quillen adjunctions]] (Def. \ref{QuillenAdjunction}), as shown, together with a [[2-morphism]] in the [[double category of model categories]] (Def. \ref{DoubleCategoryOfModelCategories})

\[
  \label{Comparison2MorphismForQuillenAdjointTriple}
  \array{
    \mathcal{D}
     &\overset{\phantom{A}C\phantom{A}}{\longrightarrow}&
    \mathcal{C}_1
    \\
    {}^{\mathllap{C}}
    \Big\downarrow
      &\swArrow_{\mathrlap{id}}& 
    \Big\downarrow{}^{ \mathrlap{ id } }
    \\
    \mathcal{C}_2
    &\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}& 
    \mathcal{C}_2
  }
\]

whose [[derived natural transformation]] $Ho(id)$ (Def. \ref{DerivedNaturalTransformation}) is invertible (a [[natural isomorphism]]).
   
If two [[Quillen adjoint triples]] overlap 

$$
  \mathcal{C}_1
    \underoverset
      {{\longleftarrow}}
      {\overset{L \phantom{= A}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_1
$$
$$
  \mathcal{C}_2
    \underoverset
      {{\longrightarrow}}
      {\overset{C = L'}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_1
$$
$$
  \mathcal{C}_2
    \underoverset
      {\underset{\phantom{A=} R'}{\longleftarrow}}
      {\overset{R = C'}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_2
$$

we speak of a _[[Quillen adjoint quadruple]]_, and so forth.

=--

+-- {: .num_prop #QuillenAdjointTripleInducesAdjointTripleOfDerivedFunctors}
###### Proposition
**([[Quillen adjoint triple]] induces [[adjoint triple]] of [[derived functors]] on [[homotopy category of a model category|homotopy categories]])**

Given a [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple}), the induced [[derived functors]] (Def. \ref{DerivedFunctorOfAHomotopicalFunctor}) on the [[homotopy category of a model category|homotopy categories]] (Def. \ref{HomotopyCategoryOfAModelCategory}) form an ordinary [[adjoint triple]] (Remark \ref{AdjointTriples}):

$$
  \mathcal{C}_{1/2}
     \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longleftarrow}
      \\
      \overset{\phantom{AA}R\phantom{AA}}{\longrightarrow}
      \\
    }
  \mathcal{D}
  \phantom{AAAA}
  \overset{Ho(-)}{\mapsto}
  \phantom{AAAA}
  Ho(\mathcal{C})
     \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{\phantom{Qu}}}{\mathbb{L}L}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{\phantom{Qu}}}{\mathbb{L}C \simeq \mathbb{R}C}{\longleftarrow}
      \\
      \overset{\phantom{AA}\mathbb{R}R\phantom{AA}}{\longrightarrow}
      \\
    }
  Ho(\mathcal{D})
$$ 

=--

+-- {: .proof}
###### Proof

This follows immediately from the fact that passing to [[homotopy categories of model categories]] is a [[double pseudofunctor]] from the [[double category of model categories]] to the [[double category of squares]] in [[Cat]] (Prop. \ref{HomotopyDoublePseudofunctor}).

=--


+-- {: .num_example #QuillenAdjointTripleFromLeftAndRightQuillenFunctor}
###### Example
**([[Quillen adjoint triple]] from left and right [[Quillen functor]])**

Given an [[adjoint triple]] (Remark \ref{AdjointTriples})

$$
  \mathcal{C}
    \array{
      \underoverset{\phantom{AA}\bot\phantom{AA}}{L}{\longrightarrow}
      \\
      \underoverset{\phantom{AA}\bot\phantom{AA}}{C}{\longleftarrow}
      \\
      \underoverset{\phantom{AA}\phantom{\bot}\phantom{AA}}{R}{\longrightarrow}
    }
  \mathcal{D}
$$

such that $C$ is both a [[left Quillen functor]] as well as a [[right Quillen functor]] (Def. \ref{QuillenAdjunction}) for given [[model category]]-[[structures]] on the [[categories]] $\mathcal{C}$ and $\mathcal{D}$. Then this is a [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple}) of the form

$$
  \mathcal{C}
    \underoverset
      {{\longleftarrow}}
      {\overset{L}{\longrightarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$
$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{C}{\longleftarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$

=--

+-- {: .proof}
###### Proof

The condition of a [[Quillen equivalence]] (eq:EquivForQuillenAdjointTriple) is trivially satisfied (by Prop. \ref{TrivialQuillenEquivalence}). Similarly the required [[2-morphism]] (eq:Comparison2MorphismForQuillenAdjointTriple)

$$
  \array{
    \mathcal{C}
     &\overset{\phantom{A}C\phantom{A}}{\longrightarrow}&
    \mathcal{D}
    \\
    {}^{\mathllap{C}}
    \Big\downarrow
      &\swArrow_{\mathrlap{id}}& 
    \Big\downarrow{}^{ \mathrlap{ id } }
    \\
    \mathcal{D}
    &\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}& 
    \mathcal{D}
  }
$$

exists trivially. To check that its [[derived natural transformation]] (Def. \ref{DerivedNaturalTransformation}) is a [[natural isomorphism]] we need to check (by Prop. \ref{DerivedNaturalTransformationUpToIsos}) that for every [[fibrant and cofibrant object]] $d \in \mathcal{D}$ the composite

$$
  Q C(d)
    \overset{ p_{C(d)} }{\longrightarrow}
  C(d)
    \overset{ j_{C(d)} }{\longrightarrow}
  P C(C)  
$$ 

is a [[weak equivalence]]. But this is trivially the case, by definition of [[fibrant resolution]]/[[cofibrant resolution]] (Def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}; in fact, since $C$ is assumed to be both left and right Quillen, also $C(d)$ is a [[fibrant and cofibrant objects]] and hence we may even take both $p_{C(d)}$ as well as $j_{C(d)}$ to be the [[identity morphism]]).


=--

The following is the analog in [[homotopy theory]] of the [[adjoint triple]] of the [[adjoint triple]] [[colimit]]/[[constant functor]]/[[limit]] (Def. \ref{Limits}):

+-- {: .num_example #HomotopyLimitQuillenAdjointTriple}
###### Example
**([[Quillen adjoint triple]] of [[homotopy limits]]/[[homotopy colimits|colimits]] of [[simplicial sets]])**

Let $\mathcal{C}$ be a [[small category]] (Def. \ref{SmallCategory}), and write $[\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}$ for the projective/injective [[model structure on simplicial presheaves]] over $\mathcal{C}$ (Prop. \ref{ModelCategoriesOfSimplicialPresheaves}), which participate in a [[Quillen equivalence]] of the form 

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\overset{\phantom{AA}id\phantom{AA}}{\longleftarrow}}
      {\simeq_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
$$

Moreover, the [[constant functor|constant diagram]]-assigning functor

$$
  [\mathcal{C}^{op}, sSet] \overset{const}{\longleftarrow} sSet
$$

is clearly a [[left Quillen functor]] for the injective model structure, and a [[right Quillen functor]] for the projective model structure.

Together this means that in the [[double category of model categories]] (Def. \ref{DoubleCategoryOfModelCategories}) we have a [[2-morphism]] of the form

$$
  \array{
    sSet_{Qu}
      &\overset{const}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \\
    {}^{\mathllap{const}}
    \Big\downarrow
      &\swArrow_{\mathrlap{id}}& 
    \Big\downarrow{}^{ \mathrlap{ id } }
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{id}{\longrightarrow}& 
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
  }
$$

Moreover, the [[derived natural transformation]] $Ho(id)$ (Prop. \ref{HomotopyDoublePseudofunctor}) of this square is invertible, if for every [[Kan complex]] $X$

$$
  Q const X
    \overset{}{\longrightarrow}
  const X
    \longrightarrow
  P const X  
$$ 

is a [[weak homotopy equivalence]] (by Prop. \ref{DerivedNaturalTransformationUpToIsos}), which here is trivially the case.

Therefore we have a [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple}) of the form

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \underoverset
       {{\longleftarrow}}
       {\overset{ \underset{\longrightarrow}{\lim} }{\longrightarrow}}
       {\phantom{{}_{Qu}}\bot_{Qu} }
  sSet_{Qu}
$$ 
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
       {\underset{ \underset{\longleftarrow}{\lim} }{\longrightarrow}}
       {\overset{const}{\longleftarrow}}
       {\phantom{{}_{Qu}}\bot_{Qu} }
  sSet_{Qu}
$$


The induced [[adjoint triple]] of [[derived functors]] on the [[homotopy category of a model category|homotopy categories]] (via Prop. \ref{QuillenAdjunctionInducesAdjunctionOnHomotopyCategories}) is the [[homotopy colimit]]/[[homotopy limit]] [[adjoint triple]]

$$
  Ho([\mathcal{C}^{op}, sSet])
  \;
    \array{
       \overset{\phantom{AA}\mathbb{L}\underset{\longrightarrow}{\lim}\phantom{AA}}{\longrightarrow}
       \\
       \overset{\phantom{AA}const\phantom{AA}}{\longleftarrow}
       \\
       \overset{\phantom{AA}\mathbb{R}\underset{\longleftarrow}{\lim}\phantom{AA}}{\longrightarrow}
    }
  \;
  Ho(sSet)
$$ 

=--


More generally:

+-- {: .num_example #QuillenAdjointTripleHomotopyKanExtension}
###### Example
**([[Quillen adjoint triple]] of [[homotopy Kan extension]] of [[simplicial presheaves]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be [[small categories]] (Def. \ref{SmallCategory}), and let 

$$
  \mathcal{C}
    \overset{\phantom{AA}F\phantom{AA}}{\longrightarrow}
  \mathcal{D}
$$

be a [[functor]] between them. By [[Kan extension]] (Prop. \ref{TopologicalLeftKanExtensionBCoend}) [[enriched category theory|enriched]] over [[sSet]] (Example \ref{ExamplesOfCosmoi}) this induces an [[adjoint triple]] between [[categories of simplicial presheaves]] (Def. \ref{CategoriesOfSimplicialPresheaves}):

$$
  [\mathcal{C}^{op}, sSet]
    \array{
      \underoverset{\bot}{ \phantom{AA}F_!\phantom{AA}  }{\longrightarrow}
      \\
      \underoverset{\bot}{ \phantom{AA}F^\ast\phantom{AA}  }{\longleftarrow}
      \\
      \overset{ \phantom{AA}F_\ast\phantom{AA}  }{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet]
$$

where 

$$
  F^\ast \mathbf{X}
  \;\coloneqq\;
  \mathbf{X}(F(-))
$$

is the operation of precomposition with $F$. This means that $F^\ast$ preserves all objectwise cofibrations/fibrations/weak equivalences in the [[model structure on simplicial presheaves]] (Prop. \ref{ModelCategoriesOfSimplicialPresheaves}). Hence it is 

1. a [[right Quillen functor]] (Def. \ref{QuillenAdjunction}) $[\mathcal{D}^{op}, sSet]_{proj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{proj}$;

1. a [[left Quillen functor]] (Def. \ref{QuillenAdjunction}) $[\mathcal{D}^{op}, sSet]_{inj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{inj}$;

and since 

$$
  [\mathcal{D}^{op}, sSet]_{inj}
    \underoverset
      {\underset{id}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\phantom{AA}\bot\phantom{AA}}
  [\mathcal{D}^{op}, sSet]_{proj} 
$$ 

is also a [[Quillen adjunction]] (Def. \ref{QuillenAdjunction}), these imply that $F^\ast$ is also 

* a [[right Quillen functor]] $[\mathcal{D}^{op}, sSet]_{inj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{proj}$.


* a [[left Quillen functor]] $[\mathcal{D}^{op}, sSet]_{proj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{inj}$.

In summary this means that we have [[2-morphisms]] in the [[double category of model categories]] (Def. \ref{DoubleCategoryOfModelCategories}) of the following form:

$$
  \array{
    [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
      &\overset{\phantom{AA}F^\ast\phantom{AA}}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \\
    {}^{\mathllap{F^\ast}}
    \Big\downarrow
      &\swArrow_{\mathrlap{id}}& 
    \Big\downarrow{}^{ \mathrlap{ id } }
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{id}{\longrightarrow}& 
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
  }
  \phantom{AAA}
  \text{and}
  \phantom{AAA}
  \array{
    [\mathcal{D}^{op}, sSet_{Qu}]_{inj}
      &\overset{\phantom{AA}F^\ast\phantom{AA}}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \\
    {}^{\mathllap{F^\ast}}
    \Big\downarrow
      &\swArrow_{\mathrlap{id}}& 
    \Big\downarrow{}^{ \mathrlap{ id } }
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{id}{\longrightarrow}& 
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
  }
$$

To check that the corresponding [[derived natural transformations]] $Ho(id)$ are [[natural isomorphisms]], we need to check (by Prop. \ref{DerivedNaturalTransformationUpToIsos}) that the composites


$$
  Q_{inj} F^\ast \mathbf{X}
    \overset{ p_{F^\ast \mathbf{X}} }{\longrightarrow}
  F^\ast \mathbf{X}
    \overset{ j_{F^\ast \mathbf{X}} }{\longrightarrow}
  P_{proj} F^\ast \mathbf{X}  
$$ 

are invertible in the [[homotopy category of a model category|homotopy category]] $Ho([\mathcal{C}^{op}, sSet_{Qu}]_{inj/proj})$ (Def. \ref{HomotopyCategoryOfAModelCategory}), for all fibrant-cofibrant simplicial presheaves $\mathbf{X}$ in $[\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}$. But this is immediate, since the two factors are weak equivalences, by definition of [[fibrant resolution|fibrant/cofibrant resolution]] (Def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}).

Hence we have a [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple}) of the form

\[
  \label{QuillenAdjointTripleFromKanExtensionOfSimplicialPresheaves}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}
    \array{
       \underoverset{\bot}{\phantom{AA}F_!\phantom{AA}}{\longrightarrow}
       \\
       \underoverset{\bot}{\phantom{AA}F^\ast\phantom{AA}}{\longleftarrow}
       \\
       \underoverset{\bot}{\phantom{AA}F_\ast\phantom{AA}}{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
  \phantom{AAA}
  \text{and}
  \phantom{AAA}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}
    \array{
       \underoverset{\bot}{\phantom{AA}F_!\phantom{AA}}{\longrightarrow}
       \\
       \underoverset{\bot}{\phantom{AA}F^\ast\phantom{AA}}{\longleftarrow}
       \\
       \underoverset{\bot}{\phantom{AA}F_\ast\phantom{AA}}{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet_{Qu}]_{inj}
\]

The corresponding derived [[adjoint triple]] on [[homotopy category of a model category|homotopy categories]] (Prop. \ref{QuillenAdjointTripleInducesAdjointTripleOfDerivedFunctors}) is that of _[[homotopy Kan extension]]_:


$$
  Ho([\mathcal{C}^{op}, sSet])
    \array{
      \underoverset{\bot \phantom{\simeq A_a}}{ \phantom{A}\mathbb{L}F_! \phantom{\simeq A_a}\phantom{A}  }{\longrightarrow}
      \\
      \underoverset{\phantom{\simeq A_a} \bot}{ \phantom{A}\mathbb{R}F^\ast \simeq \mathbb{L}F^\ast\phantom{A}  }{\longleftarrow}
      \\
      \overset{ \phantom{A} \phantom{A_a \simeq} \mathbb{R}F_\ast\phantom{A}  }{\longrightarrow}
    }
  Ho([\mathcal{D}^{op}, sSet])
$$

=--

+-- {: .num_example #QuillenAdjointQuadrupleOfHomotopyKanExtensionAlongAdjointPair}
###### Example
**([[Quillen adjoint quadruple]] of [[homotopy Kan extension]] of [[simplicial presheaves]] along [[adjoint pair]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be [[small categories]] (Def. \ref{SmallCategory}), and let 

$$
  \mathcal{C}
    \underoverset
      {\underset{\phantom{AA}R\phantom{AA}}{\longleftarrow}}
      {\overset{\phantom{AA}L\phantom{AA}}{\longrightarrow}}
      {\bot}
  \mathcal{D}
$$

be a [[adjoint pair|pair]] of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}). By [[Kan extension]] this induces an [[adjoint quadruple]] (Prop. \ref{KanExtensionOfAdjointPairIsAdjointQuadruple}) between [[categories of simplicial presheaves]] (Def. \ref{CategoriesOfSimplicialPresheaves})

$$
  [\mathcal{C}^{op}, sSet]
    \array{
      \underoverset{\bot \phantom{\simeq A_a}}{ L_! \phantom{\simeq A_a} }{\longrightarrow}
      \\
      \underoverset{\bot \phantom{\simeq} \bot }{ L^\ast \simeq R_! }{\longleftarrow}
      \\
      \underoverset{\phantom{A_a \simeq}\bot}{ L_\ast \simeq R^\ast }{\longrightarrow}
      \\
      \overset{ \phantom{A_a \simeq } R_\ast }{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet]
$$

By Example \ref{QuillenAdjointTripleHomotopyKanExtension} the top three as well as the bottom three of these form [[Quillen adjoint triples]] (Def. \ref{QuillenAdjointTriple}) for [[model structures on simplicial presheaves]] (Prop. \ref{ModelCategoriesOfSimplicialPresheaves}) in two ways (eq:QuillenAdjointTripleFromKanExtensionOfSimplicialPresheaves). If for the top three we choose the first version, and for the bottom three the second version from (eq:QuillenAdjointTripleFromKanExtensionOfSimplicialPresheaves), then these combine to a Quillen [[adjoint quadruple]] of the form

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \underoverset
      {{\longleftarrow}}
      {\overset{L_! \phantom{= A_a}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {{\longrightarrow}}
      {\overset{L^\ast = R_!}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{\phantom{A=} R_\ast}{\longleftarrow}}
      {\overset{L_\ast = R^\ast}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{inj}
$$


=--

+-- {: .num_example #QuillenAdjointQuintupleOfHomotopyKanExtensionAlongAdjointTriple}
###### Example
**([[Quillen adjoint quintuple]] of [[homotopy Kan extension]] of [[simplicial presheaves]] along [[adjoint triple]])**


Let $\mathcal{C}$ and $\mathcal{D}$ be [[small categories]] (Def. \ref{SmallCategory}) and let

$$
  \mathcal{C}
    \array{
      \underoverset{\phantom{AA}\bot\phantom{AA}}{L}{\longrightarrow}
      \\
      \underoverset{\phantom{AA}\bot\phantom{AA}}{C}{\longleftarrow}
      \\
      \underoverset{\phantom{AA}\bot\phantom{AA}}{C}{\longleftarrow}
    }
  \mathcal{D}
$$

be a [[adjoint triple|triple]] of [[adjoint functors]] (Remark \ref{AdjointTriples}). By [[Kan extension]] (Prop. \ref{TopologicalLeftKanExtensionBCoend}) [[enriched category theory|enriched]] over [[sSet]] (Def. \ref{ExamplesOfCosmoi}) this induces an [[adjoint quintuple]] between [[categories of simplicial presheaves]]

\[
 \label{AdjointQuintupleFromKanExtensionInDiscussionOfQuillenAdjointQuintuple}
  [\mathcal{C}^{op}, sSet]
    \array{
      \underoverset{\bot \phantom{\simeq A_a \simeq A_a}}{ L_! \phantom{\simeq A_a \simeq A_a} }{\longrightarrow}
      \\
      \underoverset{\bot \phantom{\simeq} \bot \phantom{\simeq A_a} }{ L^\ast \simeq C_! \phantom{\simeq A_a} }{\longleftarrow}
      \\
      \underoverset{\phantom{A_a \simeq}\bot \phantom{\simeq} \bot}{ L_\ast \simeq C^\ast \simeq R_! }{\longrightarrow}
      \\
      \underoverset{\phantom{A_a \simeq A_a } \bot}{ \phantom{A_a \simeq } C_\ast \simeq R^\ast }{\longrightarrow}
      \\
      \underoverset{\phantom{A_a \simeq A_a } \phantom{\bot}}{ \phantom{A_a \simeq C_\ast \simeq}  R_\ast }{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet]
\]

By Example \ref{QuillenAdjointQuadrupleOfHomotopyKanExtensionAlongAdjointPair} the top four functors in (eq:AdjointQuintupleFromKanExtensionInDiscussionOfQuillenAdjointQuintuple) form a [[Quillen adjoint quadruple]] (Def. \ref{QuillenAdjointTriple}) on [[model structures on simplicial presheaves]] (Prop. \ref{ModelCategoriesOfSimplicialPresheaves}) ending in a [[right Quillen functor]]

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
   \overset{C_\ast \simeq R^\ast}{\longrightarrow}
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
  \,.
$$

But $R^\ast$ here is also a [[left Quillen functor]] (as in Example \ref{QuillenAdjointTripleHomotopyKanExtension}), and hence this continues by one more Quillen adjoint triple via Example \ref{QuillenAdjointTripleFromLeftAndRightQuillenFunctor} to a [[Quillen adjoint quintuple]] of the form

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \underoverset
      {{\longleftarrow}}
      {\overset{L_! \phantom{\simeq A_a \simeq A_a}}{\longrightarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {{\longrightarrow}}
      {\overset{L^\ast \simeq C_! \phantom{\simeq A_a}}{\longleftarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{}{\longleftarrow}}
      {\overset{L_\ast \simeq C^\ast \simeq R_!}{\longrightarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{inj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{ \phantom{ A_a \simeq A_a \simeq} R_\ast }{\longrightarrow}}
      {\overset{ \phantom{A_a \simeq} C_\ast \simeq R^\ast  }{\longleftarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{inj}
$$

Alternatively, we may regard the bottom four functors in (eq:AdjointQuintupleFromKanExtensionInDiscussionOfQuillenAdjointQuintuple) as a [[Quillen adjoint quadruple]] via example \ref{QuillenAdjointQuadrupleOfHomotopyKanExtensionAlongAdjointPair}, whose top functor is then the left Quillen functor

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \overset{ L^\ast }{\longleftarrow}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
  \,.
$$

But this is also a [[right Quillen functor]] (as in Example \ref{QuillenAdjointTripleHomotopyKanExtension}) and hence we may continue by one more [[Quillen adjoint triple]] upwards (via Example \ref{QuillenAdjointTripleFromLeftAndRightQuillenFunctor}) to obtain a [[Quillen adjoint quintuple]], now of the form

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \underoverset
      {{\longleftarrow}}
      {\overset{L_! \phantom{\simeq A_a \simeq A_a}}{\longrightarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \underoverset
      {{\longrightarrow}}
      {\overset{L^\ast \simeq C_! \phantom{\simeq A_a}}{\longleftarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{}{\longleftarrow}}
      {\overset{L_\ast \simeq C^\ast \simeq R_!}{\longrightarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{ \phantom{ A_a \simeq A_a \simeq} R_\ast }{\longrightarrow}}
      {\overset{ \phantom{A_a \simeq} C_\ast \simeq R^\ast  }{\longleftarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{inj}
$$


=--

We now discuss how to extract derived [[adjoint modalities]] from systems of [[Quillen adjoint triples]]. First we consider some preliminary lemmas.



+-- {: .num_lemma #DerivedAdjunctionUnitOfQuillenAdjointTriple}
###### Lemma
**([[derived adjunction units]] of [[Quillen adjoint triple]])**

Consider a [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple})

$$
  \mathcal{C}_1
    \underoverset
      {{\longleftarrow}}
      {\overset{L}{\longrightarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$
$$
  \mathcal{C}_2
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{C}{\longleftarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$


such that the two [[model category|model structures]] $\mathcal{C}_1$ and $\mathcal{C}_2$ on the category $\mathcal{C}$ share the same class of [[weak equivalences]].

Then:

1. the [[derived adjunction unit]] of $(L \dashv C)$ in $\mathcal{C}_1$ (Def. \ref{DerivedAdjunctionUnit}) differs only by a [[weak equivalence]] from the plain [[adjunction unit]] (Def. \ref{AdjunctionUnitFromHomIsomorphism}).

1. the [[derived adjunction counit]] of $(C \dashv R)$ (Def. \ref{DerivedAdjunctionUnit}) differs only by a [[weak equivalence]] form the plain [[adjunction counit]] (Def. \ref{AdjunctionUnitFromHomIsomorphism}).


=--


+-- {: .proof}
###### Proof

By Def. \ref{AdjunctionUnitFromHomIsomorphism}, the [[derived adjunction unit]] is on cofibrant objects $c \in \mathcal{C}_1$ given by

$$
  c 
    \overset{\eta_c}{\longrightarrow}
  C L (c)
    \overset{ C(j_{L(c)}) }{\longrightarrow}
  C P L (c)
$$

Here the [[fibrant resolution]]-morphism $j_{P(c)}$ is an [[acyclic cofibration]] in $\mathcal{D}$. Since $C$ is also a [[left Quillen functor]] $\mathcal{D} \overset{C}{\to} \mathcal{C}_2$, the comparison morphism $C(j_{L(c)})$ is an [[acyclic cofibration]] in $\mathcal{C}_2$, hence in particular a weak equivalence in $\mathcal{C}_2$ and therefore, by assumption, also in $\mathcal{C}_1$.

The [[derived adjunction counit]] of the second adjunction is

$$
  C Q R (c)
    \overset{ C(p_{R(c)}) }{\longrightarrow}
  C R (c) 
    \overset{ \epsilon_c }{\longrightarrow}
  c
$$

Here the [[cofibrant resolution]]-morphisms $p_{R(c)}$ is an [[acyclic fibration]] in $\mathcal{D}$. Since $C$ is also a [[right Quillen functor]] $\mathcal{D} \overset{C}{\to} \mathcal{C}_1$, the comparison morphism $C(p_{R(c)})$ is an acyclic fibration in $\mathcal{C}_1$, hence in particular a weak equivalence there, hence, by assumption, also a weak equivalence in $\mathcal{C}_2$.


=--


+-- {: .num_lemma #DerivedModalityFromQuillenAdjointTriple}
###### Lemma
**([[fully faithful functors]] in [[Quillen adjoint triple]])**

Consider a [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple}) 

$$
  \mathcal{C}_1
    \underoverset
      {{\longleftarrow}}
      {\overset{L}{\longrightarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$
$$
  \mathcal{C}_2
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{C}{\longleftarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$

If $L$ and $R$ are [[fully faithful functors]] (necessarily jointly, by Prop. \ref{FullyFaithfulAdjointTriple}), then so are their [[derived functors]] $\mathbb{L}L$ and $\mathbb{R}R$ (Prop. \ref{QuillenAdjunctionInducesAdjunctionOnHomotopyCategories}).

=--

+-- {: .proof}
###### Proof

We discuss that $R$ being fully faithful implies that $\mathbb{R}R$ is fully faithful. Since also the [[derived functors]] form an [[adjoint triple]] (by Prop. \ref{QuillenAdjointTripleInducesAdjointTripleOfDerivedFunctors}), this will imply the claim also for $L$ and $\mathbb{L}L$, by Prop. \ref{FullyFaithfulAdjointTriple}.

By Lemma \ref{DerivedAdjunctionUnitOfQuillenAdjointTriple} the [[derived adjunction counit]] of $C \dashv R$ is, up to weak equivalence, the ordinary [[adjunction counit]]. But the latter is an [[isomorphism]], since $R$ is fully faithful (by [this Prop.](adjoint+functor#FullyFaithfulAndInvertibleAdjoints)). In summary this means that the [[derived adjunction unit]] of $(C \dashv R)$ is a weak equivalence, hence that its image in the homotopy category is an isomorphism. But the latter is the ordinary [[adjunction unit]] of $\mathbb{L}C \dashv \mathbb{R}R$ (by [this Prop.](geometry+of+physics+--+categories+and+toposes#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)), and hence the claim follows again by [that Prop.](adjoint+functor#FullyFaithfulAndInvertibleAdjoints).

=--


+-- {: .num_lemma #DerivedAdjointModalityFromQuillenAdjointQuadruple}
###### Lemma
**([[fully faithful functors]] in [[Quillen adjoint quadruple]])**

Given a [[Quillen adjoint quadruple]] (Def. \ref{QuillenAdjointTriple})

$$
  \mathcal{C}_1
    \underoverset
      {{\longleftarrow}}
      {\overset{L \phantom{= A}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_1
$$
$$
  \mathcal{C}_2
    \underoverset
      {{\longrightarrow}}
      {\overset{C = L'}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_1
$$
$$
  \mathcal{C}_2
    \underoverset
      {\underset{\phantom{A=} R'}{\longleftarrow}}
      {\overset{R = C'}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_2
$$

if any of the four functors is [[fully faithful functor]], then so is its [[derived functor]].


=--

+-- {: .proof}
###### Proof

Observing that each of the four functors is either the leftmost or the rightmost adjoint in the top or the bottom [[adjoint triple]] within the [[adjoint quadruple]], the claim follows by Lemma \ref{DerivedAdjointModalityFromQuillenAdjointQuadruple}.

=--

In summary:

+-- {: .num_prop #DerivedAdjointModalitiesFromFullyFaithfulQuillenAdjointQuadruples}
###### Proposition
**([[derived functor|derived]] [[adjoint modalities]] from [[fully faithful functor|fully faithful]] [[Quillen adjoint quadruples]])**

Given a [[Quillen adjoint quadruple]] (Def. \ref{QuillenAdjointTriple})

$$
  \mathcal{C}_1
    \underoverset
      {{\longleftarrow}}
      {\overset{L \phantom{= A}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_1
$$
$$
  \mathcal{C}_2
    \underoverset
      {{\longrightarrow}}
      {\overset{C = L'}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_1
$$
$$
  \mathcal{C}_2
    \underoverset
      {\underset{\phantom{A=} R'}{\longleftarrow}}
      {\overset{R = C'}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_2
$$

then the corresponding [[derived functors]] form an [[adjoint quadruple]]

$$
  Ho(\mathcal{C})
    \array{
      \underoverset{\phantom{AA}\bot\phantom{AA}}{ 
        \mathbb{L}L
      }{\longrightarrow}
      \\
      \underoverset{\phantom{AA}\bot\phantom{AA}}{ 
        \mathbb{L}C \simeq \mathbb{R}C \simeq \mathbb{L}L'
      }{\longleftarrow}
      \\
      \underoverset{\phantom{AA}\bot\phantom{AA}}{ 
        \mathbb{R}R \simeq \mathbb{L}C' \simeq \mathbb{R}C'
      }{\longrightarrow}
      \\
      \underoverset{\phantom{AA}\phantom{\bot}\phantom{AA}}{ 
        \mathbb{R}R'
      }{\longleftarrow}
    }
  Ho(\mathcal{D})
$$

Moreover, if one of the functors in the [[Quillen adjoint quadruple]] is a [[fully faithful functor]], then so is the corresponding [[derived functor]]. 

Hence if the original [[adjoint quadruple]] induces an [[adjoint modality]] on $\mathcal{C}$ (Def. \ref{AdjointModality})

$$
  \bigcirc \dashv \Box \dashv \lozenge
$$

or on $\mathcal{D}$

$$
  \Box \dashv \bigcirc \dashv \triangle
$$

then so do the corresponding [[derived functors]] on the [[homotopy category of a model category|homotopy categories]], respectively.

=--

+-- {: .proof}
###### Proof

The existence of the derived [[adjoint quadruple]] followy by Prop. \ref{QuillenAdjointTripleInducesAdjointTripleOfDerivedFunctors} and by uniqueness of adjoints ([this Prop.](adjoint+functor#UniquenessOfAdjoints)).

The statement about fully faithful functors is Lemma \ref{DerivedAdjointModalityFromQuillenAdjointQuadruple}. The reformulation in terms of [[adjoint modalities]] is by [this Prop.](geometry+of+physics+--+categories+and+toposes#ModalOperatorsEquivalentToReflectiveSubcategories)

=--


$\,$

### $\infty$-Toposes

The characterization of [[sheaf toposes are equivalently the left exact reflective subcategories of presheaf toposes|sheaf toposes as the left exact reflective localizations of presheaf toposes]] (Prop. \ref{SheafToposViaLexReflection}) now has an immediate generalization from the realm of [[locally presentable categories]] to that of [[combinatorial model categories]] and their corresponding [[locally presentable (∞,1)-categories]] (Def. \ref{HoCombModCat}): This yields concept of [[model toposes]] and [[(∞,1)-toposes]] (Def. \ref{ModelTopos} below).

$\,$

+-- {: .num_defn #ModelTopos}
###### Definition
**([[model topos]] and [[(∞,1)-topos]])**

A [[combinatorial model category]] (Def. \ref{CombinatorialModelCategory}) is a _[[model topos]]_ if it has a presentation via [[Dugger's theorem]] (Prop. \ref{DuggerTheorem})

\[
  \label{LexBousfieldLocalizationOfSimplicialPresheaves}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj,S}
     \underoverset
       {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
       {\overset{id}{\longleftarrow}}
       {\bot_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}  
  \;\;
  \in CombModCat
\]

such that the [[left derived functor]] $\mathbb{L}id$ preserves [[finite limit|finite]] [[homotopy limits]].

We denote the image of such a [[combinatorial model category]] under the [[localization of a category|localization]] [[functor]] $\gamma$ in [[Ho(CombModCat)]] (Def. \ref{HoCombModCat}) by

$$
  Sh_\infty(\mathcal{C})
  \;\coloneqq\;
  \gamma([\mathcal{C}^{op}, sSet_{Qu}]_{proj,S})
  \;\in\;
  Ho(CombModCat)
$$

and call this an _[[(∞,1)-topos]]_ over a [[site]] $\mathcal{C}$.
Moreover, we denote the image of the defining [[Quillen adjunction]] (eq:LexBousfieldLocalizationOfSimplicialPresheaves) in [[Ho(CombModCat)]] by

$$
  Sh_\infty(\mathcal{C})
    \underoverset
      {\underset{\phantom{AAAA}}{\hookrightarrow}}
      {\overset{lex}{\longleftarrow}}
      {\bot}
  PSh_\infty(\mathcal{C})
  \;\;
  \in
  Ho(CombModCat)
  \,.
$$

=--

The following construction generalizes the _[[Cech groupoid]]_ (Example \ref{CechGroupoid}) as [[groupoids]] are generalized to [[Kan complexes]] (Def. \ref{KanComplexe}):

+-- {: .num_example #CechNerve}
###### Example
**([[Cech nerve]])**

Let $\mathcal{C}$ be a [[site]] (Def. \ref{Coverage}). Then for every [[object]] $X \in \mathcal{C}$ and every [[covering]] $\{U_i \overset{\iota_i}{\to}X\}$ there is a [[simplicial presheaf]] (Example \ref{CategoriesOfSimplicialPresheaves})

$$
  C(\{U_i\})
  \;\in\;
  [\mathcal{C}^{op}, sSet]
$$

which in degree $k$ is given by the [[disjoint union]] of the $k$-fold [[fiber products]] of [[presheaves]] over $y(X)$ of the patches $y(U_i) \in [\mathcal{C}^{op}, Set]$ of the cover, regarded as [[presheaves]] under the [[Yoneda embedding]] (Prop. \ref{YonedaEmbedding})

$$
  C(\{U_i\})_k
  \;\coloneqq\;
  \underset{i_1, \cdots, i_k}{\coprod}
  y(U_{i_1}) \times_{y(X)} y(U_{i_2})  \times_{y(X)} 
   \cdots 
   \times_{y(X)}  y(U_{i_k})
  \,.
$$ 

The [[face maps]] are the evident [[projection]] morphisms, and the [[degeneracy maps]] the evident [[diagonal]] morphisms.

This is called the _[[Cech nerve]]_ of the given cover.

By the definition of [[fiber products]] there is a canonical morphism of [[simplicial presheaves]] from the [[Cech nerve]] to $y(X)$

\[
  \label{CechNerveProjection}
  C(\{U_i\})
    \overset{p_{\{U_i\}}}{\longrightarrow}
  y(X)
\]

We call this the _Cech nerve projection_. 

More generally, for 

$$
  \mathbf{Y} \overset{f}{\longrightarrow} \mathbf{X}
  \;\;\;
  \in
  [\mathcal{C}^{op}, Set]
$$

any morphism of [[presheaves]], there is the correspnding [[Cech nerve]] [[simplicial presheaf]]

$$
  C(f) \in [\mathcal{C}^{op}, sSet]
$$

which in degree $k$ is the $k$-fold [[fiber product]] of $f$ with itself:

$$
  C(f)_k \;\coloneqq\;
  \underset{
    k \; \text{factors}
  }{
  \underbrace{
    \mathbf{Y} \times_{\mathbf{X}} \cdots \times_{\mathbf{X}} \mathbf{Y}
  }}
  \,.
$$

=--

The following is the generalization of Prop. \ref{CechGroupoidCoRepresents}, saying that [[Cech nerves]] are [[codescent]]-objects for [[(∞,1)-sheaves]]:

+-- {: .num_prop #TopologicalLocalization}
###### Proposition
**([[topological localization]])**

Let $\mathcal{C}$ be a [[site]] (Def. \ref{Coverage}) and let 

$$
  S 
  \;\coloneqq\;
  \big\{
    C(\{U_i\})
    \overset{p_{\{U_i\}}}{\longrightarrow}
    y(X)
    \;\vert\;
    \{U_i \overset{\iota_i}{\to} X\}_i
    \;
    \text{covering}
  \big\}
  \subset Mor_{[\mathcal{C}^{op}, sSet]}
$$ 

be the [[set]] of [[projections]] (eq:CechNerveProjection) out of the [[Cech nerves]] (Example \ref{example}) for [[coverings]] of all [[objects]] in the site, as a subset of the class of morphisms of [[simplicial presheaves]] over $\mathcal{C}$ (Example \ref{CategoriesOfSimplicialPresheaves}).


Then the [[left Bousfield localization]] (Def. \ref{ExistenceOfLeftBousfieldLocalization}) 
of the projective or injective [[model structure on simplicial presheaves]] (Prop. \ref{ModelCategoriesOfSimplicialPresheaves}), to be denoted 

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{{proj/inj} \atop {loc}}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\bot_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}  
$$

and to be called the (projective or injective) _[[local model structure on simplicial presheaves]]_, is left exact, in that it exhibits a [[model topos]] according to Def. \ref{ModelTopos}, hence in that its image in [[Ho(CombModCat)]] is an [[(∞,1)-topos]]

$$
  Sh_\infty(\mathcal{C})
   \underoverset
    {\underset{\phantom{AA}\iota\phantom{AA}}{\hookrightarrow}}
    {\overset{lex}{\longleftarrow}}
    {\bot}
  PSh_\infty(\mathcal{C})
  \,.
$$

=--

+-- {: .num_prop #QuillenEquivalenceBetweenProjectiveAndInjectiveTopologicalLocalization}
###### Proposition
**([[Quillen equivalence]] between projective and injective [[topological localization]])**


Let $\mathcal{C}$ be a [[site]] (Def. \ref{Coverage}) and let 

$$
  S 
  \;\coloneqq\;
  \big\{
    C(\{U_i\})
    \overset{p_{\{U_i\}}}{\longrightarrow}
    y(X)
    \;\vert\;
    \{U_i \overset{\iota_i}{\to} X\}_i
    \;
    \text{covering}
  \big\}
  \subset Mor_{[\mathcal{C}^{op}, sSet]}
$$ 

be the [[set]] of [[projections]] (eq:CechNerveProjection) out of the [[Cech nerves]] (Example \ref{example}) for [[coverings]] of all [[objects]] in the site, as a subset of the class of morphisms of [[simplicial presheaves]] over $\mathcal{C}$ (Example \ref{CategoriesOfSimplicialPresheaves}).

If each [[Cech nerve]] $C(\{U_i\})$ is already a [[cofibrant object]] in the [[projective model structure on simplicial presheaves]] (prop. \ref{ModelCategoriesOfSimplicialPresheaves})
then the [[identity functors]] constitute a [[Quillen equivalence]] (Def. \ref{QuillenEquivalence}) between the corresponding [[topological localizations]] (Def. \ref{TopologicalLocalization}) of the projective and the injective [[model structure on simplicial presheaves]]:

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj \atop loc}
    \underoverset
      {\underset{id}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj \atop loc}
$$

=--

+-- {: .proof}
###### Proof

First to see that we have a [[Quillen adjunction]] (Def. \ref{QuillenAdjunction}): By Prop. \ref{ModelCategoriesOfSimplicialPresheaves} this is the case before [[left Bousfield localization]]. By the nature of [[left Bousfield localization]], and since the model structures are [[left proper model category|left proper]] [[simplicial model categories]] (by Prop. \ref{SimplicialPresheavesIsProperCombinatorialSimplicial}), by Prop. \ref{RecognitionOfSimplicialQuillenAdjunction} it is sufficient to check that the right Quillen functor preserves [[fibrant objects]]. By Prop. \ref{ExistenceOfLeftBousfieldLocalization} this means to check that it preserves $S$-[[local objects]]. But since $C(\{U_i\})$ is assumed to be projectively cofibrant, and since injectively fibrant objects are already projectively fibrant, the condition on an injectively local object according to Def. \ref{DerivedLocalObjects} is exactly the same as for a projectively local object.

Now to see that this [[Quillen adjunction]] is a [[Quillen equivalence]],  it is sufficient to check that the corresponding left/right [[derived functors]] induce an [[equivalence of categories]] on [[homotopy category of a model category|homotopy categories]]. By Prop. \ref{ModelCategoriesOfSimplicialPresheaves} this is the case before [[left Bousfield localization]]. By Prop. \ref{ExistenceOfLeftBousfieldLocalization} it is thus sufficient to check that derived functors (before localization) preserves $S$-local objects. By Prop. \ref{ComputationOfLeftRightDerivedFunctorsViaResolutions} for this it is sufficient that the Quillen functors themselves preserve local objects. For the right Quillen functor we have just seen this in the previous paragaraph, for the left Quillen functor it follows analogously.


=--

+-- {: .num_exmple #HomotopyLocalizationOverSiteOfAns}
###### Example
**([[homotopy localization]] at $\mathbb{A}^1$ over the [[site]] of $\mathbb{A}^n$s)**

Let $\mathcal{C}$ be any [[site]] (Def. \ref{Coverage}), and write $[\mathcal{C}^{op}, sSet_{Qu}]_{proj, loc}$ for its local projective [[model category of simplicial presheaves]] (Prop. \ref{TopologicalLocalization}).

Assume that $\mathcal{C}$ contains an [[object]] $\mathbb{A} \in \mathcal{C}$, such that every other object is a [[finite product]] $\mathbb{A}^n \coloneqq \underset{n \; \text{factors}}{\underbrace{\mathbb{A} \times \cdots \times \mathbb{A}}}$, for some $n \in \mathbb{N}$. (In other words, assume that $\mathcal{C}$ is also the [[syntactic category]] of _[[Lawvere theory]]_.)

Consider the  $\mathbb{A}^1$-[[homotopy localization]] (Def. \ref{HomotopyLocalizationOfCombinatorialModelCategories}) of the [[(∞,1)-sheaf (∞,1)-topos]] over $\mathcal{C}$ (Prop. \ref{TopologicalLocalization})

$$
  Sh_\infty(\mathcal{C})_{\mathbb{A}}
    \underoverset
      {\underset{\phantom{AA}\iota\phantom{AA}}{\hookrightarrow}}
      {\overset{L_{\mathbb{A}}}{\longleftarrow}}
      {\bot}
  Sh_\infty(\mathcal{C})
  \;\;
  \in
  Ho(CombModCat)
$$

hence the [[left Bousfield localization]] of [[model categories]]

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj,loc,\mathbb{A}}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj,loc}
  \;\;
  \in 
  CombModCat
$$

at the set of morphisms

$$
  S
    \;\coloneqq\;
  \big\{
    \mathbb{A}^n \times \mathbb{A}
      \overset{p_1}{\longrightarrow}
    \mathbb{A}^n
  \big\}
$$

(according to Prop. \ref{ExistenceOfLeftBousfieldLocalization}).

Then this is [[equivalence of (∞,1)-categories|equivalent]] (Def. \ref{HoCombModCat}) to [[∞Grpd]] (Def. \ref{InfinityGroupoid}),


$$
  \infty Grpd
  \;\simeq\;
  Sh_\infty(\mathcal{C})_{\mathbb{A}}
    \underoverset
      {\underset{\phantom{AA}\iota\phantom{AA}}{\hookrightarrow}}
      {\overset{L_{\mathbb{A}}}{\longleftarrow}}
      {\bot}
  Sh_\infty(\mathcal{C})
  \;\;
  \in
  Ho(CombModCat)
$$

in that the ([[constant functor]] $\dashv$ [[limit]])-[[adjunction]] (Def. \ref{Limits})

\[
  \label{QuillenEquivalenceInABousfLocalization}
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj, loc, \mathbb{A}}
    \underoverset
      {\underset{ \underset{\longleftarrow}{\lim} }{\longrightarrow}}
      {\overset{ \phantom{AA}const\phantom{AA} }{\longleftarrow}}
      {\bot}
  sSet_{Qu}    
  \;\;\;\;
  \in 
  CombModCat
\]

is a [[Quillen equivalence]] (Def. \ref{QuillenEquivalence}).

=--

+-- {: .proof}
###### Proof

First to see that (eq:QuillenEquivalenceInABousfLocalization) is a [[Quillen adjunction]] (Def. \ref{QuillenAdjunction}): Since we have a [[simplicial Quillen adjunction]] before localization

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{ \underset{\longleftarrow}{\lim} }{\longrightarrow}}
      {\overset{ \phantom{AA}const\phantom{AA} }{\longleftarrow}}
      {\bot}
  sSet_{Qu}    
$$

(by Example \ref{HomotopyLimitOfSimplicialSets}) and since both [[model categories]] here are [[left proper model category|left proper]] [[simplicial model categories]] (by Prop. \ref{SimplicialPresheavesIsProperCombinatorialSimplicial} and Prop. \ref{ExistenceOfLeftBousfieldLocalization}), and since [[left Bousfield localization]] does not change the class of [[cofibrations]] (by Def. \ref{BousfieldLocalizationOfModelCategories}) it is sufficient to show that $\underset{\longleftarrow}{\lim}$ preserves [[fibrant objects]] (by Prop. \ref{RecognitionOfSimplicialQuillenAdjunction}).

But by assumption $\mathcal{C}$ has a [[terminal object]] $\ast = \mathbb{A}^0$ (Def. \ref{InitialObject}), which is hence the [[initial object]] of $\mathcal{C}^{op}$, so that the [[limit]] operation is given just by evaluation on that object:

$$
  \underset{\longleftarrow}{\lim}
  \mathbf{X}
  \;=\;
  \mathbf{X}(\mathbb{A}^0)
  \,.
$$

Hence it is sufficient to see that an injectively fibrant simplicial presheaf $\mathbf{X}$ is objectwise a [[Kan complex]]. This is indeed the case, by Prop. \ref{ModelCategoriesOfSimplicialPresheaves}.

To check that (eq:QuillenEquivalenceInABousfLocalization) is actually a [[Quillen equivalence]] (Def. \ref{QuillenEquivalence}), we check that the [[derived adjunction unit]] and [[derived adjunction counit]] (Def. \ref{DerivedAdjunctionUnit}) are weak equivalences:

For $X \in sSet$ any simplicial set (necessarily cofibrant), the [[derived adjunction unit]] is 

$$
  X 
    \overset{id_X}{\longrightarrow} 
  const(X)(\mathbb{A}^0)
    \overset{ const(j_X)(\mathbb{A}^0) }{\longrightarrow}
  const(P X)(\mathbb{A}^0)
$$

where $X \overset{j_X}{\longrightarrow} P X$ is a [[fibrant replacement]] (Def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}). But $const(-)(\mathbb{A}^0)$ is clearly the [[identity functor]] and the plain adjunction unit is the [[identity morphism]], so that this composite is just $j_X$ itself, which is indeed a weak equivalence.

For the other case, let $\mathbf{X} \in [\mathcal{C}^{op}, sSet_{Qu}]_{inj, loc, \mathbb{A}^1}$ be fibrant. This means (by Prop. \ref{ExistenceOfLeftBousfieldLocalization}) that $\mathbf{X}$ is fibrant in the injective [[model structure on simplicial presheaves]] as well as in the local model structure, and is a derived-$\mathbb{A}^1$-[[local object]] (Def. \ref{DerivedLocalObjects}), in that the [[derived hom-functor]] out of any $\mathbb{A}^n \times \mathbb{A}^1 \overset{p_1}{\longrightarrow} \mathbb{A}^n$  into $\mathbf{X}$ is a [[weak homotopy equivalence]]:

$$
  \mathbb{R}Hom( p_1 )
  \;\colon\;
  \mathbb{R}Hom( \mathbb{A}^n , \mathbf{X})
  \overset{\in W}{\longrightarrow}
  \mathbb{R}Hom( \mathbb{A}^n \times \mathbb{A}^1 , \mathbf{X})
$$

But since $\mathbf{X}$ is fibrant, this derived hom is equivalent to the ordinary [[hom-functor]] (Lemma \ref{HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory}), and hence with the [[Yoneda lemma]] (Prop. \ref{YonedaLemma}) we have that

$$
  \mathbf{X}(p_1)
  \;\colon\;
  \mathbf{X}(\mathbb{A}^n)
  \overset{\in W}{\longrightarrow}
  \mathbf{X}(\mathbb{A}^{n+1})
$$

is a weak equivalence, for all $n \in \mathbb{N}$. By [[induction]] on $n$ this means that in fact 

$$
  \mathbf{X}(\mathbb{A}^0)
   \overset{\in W}{\longrightarrow} 
  \mathbf{X}(\mathbb{A}^n) 
$$

is a weak equivalence for all $n \in \mathbb{N}$. But these are just the components of the [[adjunction counit]]

$$
  const (\mathbf{X}(\mathbb{A}^0))
   \underoverset{\in W}{\epsilon}{\longrightarrow}
  \mathbf{X}
$$

which is hence also a weak equivalence. Hence for the [[derived adjunction counit]]

$$
  const (Q \mathbf{X})(\mathbb{A}^0)
    \overset{const(p_{\mathbf{X}}(\mathbb{A}^0))}{\longrightarrow}
  const (\mathbf{X}(\mathbb{A}^0))
   \underoverset{\in W}{\epsilon}{\longrightarrow}
  \mathbf{X}
$$

to be a weak equivalence, it is now sufficient to see that the value of a [[cofibrant replacement]] $p_{\mathbf{X}}$ on $\mathbb{A}^0$ is a weak equivalence. But by definition of the weak equivalences of simplicial presheaves these are objectwise weak equivalences.

=--

+-- {: .num_prop #CechNerveProjectionOfLocalEpimorphismIsLocalWeakEquivalence}
###### Proposition
**([[Cech nerve]]-projection of [[local epimorphism]] is [[local weak equivalence]])**

Let $\mathcal{C}$ be a [[site]] (Def. \ref{Coverage}) and let 

$$
  \mathbf{Y} \overset{\phantom{A}f\phantom{A}}{\longrightarrow} \mathbf{X}
  \;\;\;
  \in [\mathcal{C}^{op}, Set]
$$

be a [[local epimorphism]] (Def. \ref{LocalEpimorphism}) in its [[category of presheaves]]. Then the corresponding [[Cech nerve]]-projection (Def. \ref{CechNerve}) 

$$
  C(f) \overset{}{\longrightarrow} \mathbf{X}
  \;\;\;
  \in [\mathcal{C}^{op}, sSet_{Qu}]_{proj,loc}
$$

is a [[weak equivalence]] in the local projective [[model structure on simplicial presheaves]] (Prop. \ref{TopologicalLocalization}).


=--

([Dugger-Hollander-Saksen 02, corollary A.3](local+epimorphism#DuggerHollanderIsaksen02))


$\,$

## Gros $\infty$-Toposes

We have established above enough [[higher category theory]]/[[homotopy theory]] that it is now fairly straightforward to generalize the discussion of [[gros toposes]] to [[model toposes]]/[[(∞,1)-toposes]].

$\,$



### Cohesive $\infty$-Toposes
 {#CohesiveInfinityToposes}

The following is a refinement to [[homotopy theory]] of the notion of _[[cohesive topos]]_ (Def. \ref{CohesiveTopos}):

+-- {: .num_defn #CohesiveInfinityTopos}
###### Definition
**([[cohesive model topos]])**

An [[(∞,1)-topos]] $\mathbf{H}$ (Def. \ref{ModelTopos}) is called a _[[cohesive (∞,1)-topos]]_ if it is presented by a [[model topos]] $[\mathcal{C}^{op}, sSet_{Qu}]_{loc}$ (Def. \ref{ModelTopos}) which admits a [[Quillen adjoint quadruple]] (Def. \ref{QuillenAdjointTriple}) to the [[classical model category of simplicial sets]] (Def. \ref{ClassesOfMorphismsOnsSetQuillen}) of the form

$$
  \array{
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}
      \array{
        \underoverset{{}_{\phantom{A}}\bot_{Qu}}{\phantom{AA}\Pi\phantom{AA}}{\longrightarrow}
        \\
        \underoverset{{}_{\phantom{A}}\bot_{Qu} }{\phantom{A}Disc\phantom{A}}{\hookleftarrow}
        \\
        \underoverset{{}_{\phantom{A}}\bot_{Qu}}{\phantom{AA}\Gamma\phantom{AA}}{\longrightarrow}
        \\
        \overset{\phantom{A}coDisc\phantom{A}}{\hookleftarrow}
        \\
      }
    sSet_{Qu}
  }
$$

such that 

1. $(Disc \dashv \Gamma)$ is a [[Quillen coreflection]] (Def. \ref{QuillenReflection});

1. $(\Gamma \dashv coDisc)$ is a [[Quillen reflection]] (Def. \ref{QuillenReflection});

1. $\Pi$ preserves [[finite products]].

=--

The following is the analog of Example \ref{PresheavesAdjointQuadrupleOnSiteWithTerminalObject}:

+-- {: .num_example #simplicialPresheavesAdjointQuadrupleOnSiteWithTerminalObject}
###### Example
**([[Quillen adjoint quadruple]] on [[simplicial presheaves]] over [[site]] with [[finite products]])**

Let $\mathcal{C}$ be a [[small category]] (Def. \ref{SmallCategory}) with [[finite products]] (hence with a [[terminal object]] $\ast \in \mathcal{C}$ and for any two [[objects]] $X,Y \in \mathcal{C}$ their [[Cartesian product]] $X \times Y \in \mathcal{C}$). By Example \ref{InitialAndTerminalObjectInTermsOfAdjunction} the [[terminal object]] is witnessed by an [[adjunction]]

\[
  \label{SiteAdjunctionForInfinityPresheafCohesion}
  \ast 
    \underoverset
     {\underset{}{\hookrightarrow}}
     {\overset{\phantom{AAAA}}{\longleftarrow}}
     {\bot}
  \mathcal{C}
\]


Consider the [[category of simplicial presheaves]] $[\mathcal{C}^{op}, sSet]$ (Example \ref{CategoriesOfSimplicialPresheaves}) with its projective and injective [[model structure on simplicial presheaves]] (Prop. \ref{ModelCategoriesOfSimplicialPresheaves}).
 
Then [[Kan extension]] (Prop. \ref{TopologicalLeftKanExtensionBCoend}) [[enriched category theory|enriched]] over [[sSet]] (Example \ref{ExamplesOfCosmoi}) along the [[adjoint pair]] (eq:SiteAdjunctionForInfinityPresheafCohesion) yields a [[simplicial Quillen adjunction|simplicial]] [[Quillen adjoint quadruple]] (Def. \ref{QuillenAdjointTriple})

\[
  \label{PreaheafAdjointQuadruple}
  [\mathcal{C}^{op}, Set_{Qu}]_{proj/inj}
    \array{
      \underoverset{{}_{\phantom{A}}\bot_{Qu}}{\phantom{AAA} \Pi \phantom{AAA}}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{A}}\bot_{Qu}}{\phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
      \\
      \underoverset{{}_{\phantom{A}}\bot_{Qu}}{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookleftarrow}
    }
  sSet_{Qu}
\]


such that:

1. the functor $\Gamma$ sends a [[simplicial presheaf]] $\mathbf{Y}$ to its [[simplicial set]] of [[global sections]], which here is its value on the [[terminal object]]:

   \[
     \label{CohesiveGlobalSectionsGivenByPointEvaluationModelCat}
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


1. $(Disc \dashv \Gamma)$ is a [[Quillen coreflection]] (Def. \ref{QuillenReflection})

1. $(\Gamma \dashv coDisc)$ is a [[Quillen reflection]] (Def. \ref{QuillenReflection});

1. $\Pi$ [[preserved limit|preserves]] [[finite products]]:

Hence the [[category of simplicial presheaves]] over a [[small category]] with [[finite products]] is a [[cohesive (∞,1)-topos]] (Def. \ref{CohesiveInfinityTopos}).

=--


+-- {: .proof}
###### Proof

The [[Quillen adjoint quadruple]] follows as the special case of Example \ref{QuillenAdjointQuadrupleOfHomotopyKanExtensionAlongAdjointPair} applied to the [[adjoint pair]]

$$
  \ast 
    \underoverset
      {\underset{}{\hookrightarrow}}
      {\overset{}{\longleftarrow}}
      {\bot}
  \mathcal{C}
$$

given by inclusion of the [[terminal object]] (Example \ref{InitialAndTerminalObjectInTermsOfAdjunction}).

Since the plain [[adjoint quadruple]] has $(\Pi \dashv \Disc)$ a [[reflective subcategory]] inclusion and $(Disc \dashv \Gamma)$ a [[coreflective subcategory]] inclusion (Example \ref{PresheavesAdjointQuadrupleOnSiteWithTerminalObject}) the Quillen (co-)reflection follows by Prop. \ref{DerivedAdjointModalitiesFromFullyFaithfulQuillenAdjointQuadruples}

=--

The following is a refinement to [[homotopy theory]] of the notion of _[[cohesive site]]_ (Def. \ref{OneCohesiveSite}):

+-- {: .num_defn #InfinityCohesiveSite}
###### Definition
**([[∞-cohesive site]])**

We call a [[site]] $\mathcal{C}$ (Def. \ref{Coverage}) _[[∞-cohesive site|∞-cohesive]]_ if the following conditions are satisfied:

1. The [[category]] $\mathcal{C}$ has [[finite products]];

1. For every [[covering]] family $\{U_i \to X\}_i$ in the given [[coverage]] on $\mathcal{C}$, the induced [[Cech nerve]] [[simplicial presheaf]] (Example \ref{CechNerve}) $C(\{U_i\}) \in [\mathcal{C}^{op}, sSet]$ satisfies the following conditions

   1. $C(\{U_i\})$ is a [[cofibrant object]] in the [[projective model structure on simplicial presheaves]] $[\mathcal{C}^{op}, sSet_{Qu}]_{proj}$ (Prop. \ref{ModelCategoriesOfSimplicialPresheaves})

   1. The [[simplicial set]] obtained as the degreewise [[colimit]] over the [[Cech nerve]] is [[weak homotopy equivalence|weakly homotopy equivalent]] to the point

      $$
        \underset{
          \underset{
            \mathcal{C}^{op}
          }{\longrightarrow}
        }{\lim} C(\{U_i\}) 
        \simeq 
        \ast
      $$

   1. The [[simplicial set]] obtained at the degreewise [[limit]] over the [[Cech nerve]] is [[weak homotopy equivalence|weakly homotopy equivalent]] to the underlying set of points of $X$:

      $$
        \underset{\underset{\mathcal{C}^{op}}{\longleftarrow}}{C(\{U_i\})}
        \simeq
        Hom_{\mathcal{C}}(\ast, X)
        \,.
      $$

=--

The following is the analog of Prop. \ref{CategoriesOfSheavesOnCohesiveSiteIsCohesive}:

+-- {: .num_prop #OverInfinityCohesiveSiteCohesiveInfinityTopos}
###### Proposition
**([[model topos]] over [[∞-cohesive site]] is [[cohesive model topos]])**

Let $\mathcal{C}$ be an [[∞-cohesive site]] (Def. \ref{InfinityCohesiveSite}). Then the [[(∞,1)-topos]] (Def. \ref{ModelTopos}) over it, obtained by [[topological localization]] (Prop. \ref{TopologicalLocalization}) is a [[cohesive (∞,1)-topos]] (Def. \ref{CohesiveInfinityTopos}).

=--


+-- {: .proof}
###### Proof

By Example \ref{simplicialPresheavesAdjointQuadrupleOnSiteWithTerminalObject} we have the required [[Quillen adjoint quadruple]] on the projective [[model structure on simplicial presheaves]], i.e. before [[left Bousfield localization]] at the [[Cech nerve]] projections 

$$
  [\mathcal{C}^{op}, Set_{Qu}]
    \array{
      \overset{\phantom{AAA} \Pi \phantom{AAA}}{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookleftarrow}
    }
  sSet_{Qu}
$$

Hence it remains to see that these [[Quillen adjunctions]] pass to the local model structures $[\mathcal{C}^{op}, Set_{Qu}]_{proj/inj, loc}$ from Prop. \ref{TopologicalLocalization}, and that $Disc$ and $coDisc$ then still participate in [[Quillen reflection|Quillen (co-)reflections]].

By Prop. \ref{SimplicialPresheavesIsProperCombinatorialSimplicial} and Prop. \ref{ExistenceOfLeftBousfieldLocalization} all model structures involved are [[left proper model category|left proper]] [[simplicial model categories]], and hence we may appeal to Prop. \ref{RecognitionOfSimplicialQuillenAdjunction} for recognition of the required [[Quillen adjunctions]]. Since, moreover, [[left Bousfield localization]] does not change the class of [[cofibrations]] (Def. \ref{BousfieldLocalizationOfModelCategories}), this means that we are reduced to checking that all [[right Quillen functors]] in the above global [[Quillen adjoint quadruple]] preserve [[fibrant objects]] with respect to the local model structure.

For the Quillen adjunctions 

$$
  (\Pi \dashv Disc), (\Gamma \dashv coDisc)
  \;\colon\;
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
  \leftrightarrow
  sSet_{Qu}
$$ 

this means to check that for every [[Kan complex]] $S \in sSet$ the [[simplicial presheaves]] $Disc(S)$ and $coDisc(S)$ are derived-[[local objects]] (Def. \ref{DerivedLocalObjects}, Prop. \ref{ExistenceOfLeftBousfieldLocalization}) with respect to the [[Cech nerve]] projections. Since $Disc$ and $coDisc$ are [[right Quillen functors]] with respect to the global model projective model structure, $Disc(S)$ and $coDisc(S)$ are globally projectively fibrant simplicial presheaves. Since, moreover, $C(\{U_i\})$ is projectively cofibrant by assumption, and since the representables $X \in \mathcal{C}$ are projectively cofibrant by Prop. \ref{SomeProjectivelyCofibrantSimplicialPresheaves}, the value of the [[derived hom-functor]] reduces to that of the ordinary [[enriched hom-functor]] (Def. \ref{EnrichedHomFunctor}), and hence the condition is that 

$$
  \array{
  [\mathcal{C}^{op}, sSet]( X, Disc(S) )
    &\overset{\in W}{\longrightarrow}&
  [\mathcal{C}^{op}, sSet]( C(\{U_i\}), Disc(S) )
  \\
  [\mathcal{C}^{op}, sSet]( X, coDisc(S) )
    &\overset{\in W}{\longrightarrow}&
  [\mathcal{C}^{op}, sSet]( C(\{U_i\}), coDisc(S) )
  }
$$

are weak equivalences. But now by the ordinary adjunction hom-isomorphism (eq:HomIsomorphismForAdjointFunctors), these are identified with

$$
  \array{
  [\mathcal{C}^{op}, sSet]( \underset{\longrightarrow}{\lim} X, S )
    &\overset{\in W}{\longrightarrow}&
  [\mathcal{C}^{op}, sSet]( \underset{\longrightarrow}{\lim}C(\{U_i\}), S )
  \\
  [\mathcal{C}^{op}, sSet]( \underset{\longleftarrow}{\lim}X, S )
    &\overset{\in W}{\longrightarrow}&
  [\mathcal{C}^{op}, sSet]( \underset{\longleftarrow}{\lim}C(\{U_i\}), S )
  }
$$

Since the [[colimit]] of a [[representable]] is the singleton (Lemma \ref{ColimitOfRepresentableIsSingleton}) and since the [[limit]] over the opposite of a category with terming object is evaluation at that object, this in turn is equivalent to 

$$
  \array{
  [\mathcal{C}^{op}, sSet]( \ast, S )
    &\overset{\in W}{\longrightarrow}&
  [\mathcal{C}^{op}, sSet]( \underset{\longrightarrow}{\lim}C(\{U_i\}), S )
  \\
  [\mathcal{C}^{op}, sSet]( Hom_{\mathcal{C}}(\ast, X), S )
    &\overset{\in W}{\longrightarrow}&
  [\mathcal{C}^{op}, sSet]( \underset{\longleftarrow}{\lim}C(\{U_i\}), S )
  }
$$

Here we recognize the [[internal hom]] in [[simplicial sets]] from the weak equivalences of the definition of an _[[∞-cohesive site]]_ (Def. \ref{InfinityCohesiveSite}), which necessarily go between cofibrant simplicial sets, into a fibrant simplicial set $S$. Hence this is the [[derived hom-functor]] (Def. \ref{DerivedHomFunctorPOnSimplicialModelCategory}) in the [[classical model structure on simplicial sets]]. Since the latter is a [[simplicial model category]] (Def. \ref{SimplicialModelCategory}) by Prop. \ref{SimplicialPresheavesIsProperCombinatorialSimplicial}, these morphisms are indeed weak equivalences of simplicial sets.

This establishes that $(\Pi \dashv Disc)$ and $(\Gamma \dashv \coDisc)$ descent to Quillen adjunctions on the local model structure. Finally, it is immediate that $\Gamma$ preserves fibrant objects, and hence also $(Disc \dashv \Gamma)$ passes to the local model structure.

=--

The following is the analog in [[homotopy theory]] of the [[cohesion|cohesive]] [[adjoint modalities]] from Def. \ref{CohesiveModalities}:

+-- {: .num_defn #DerivedCohesiveModalities}
###### Definition
**([[adjoint triple]] of [[derived functor|derived]] [[adjoint modality|adjoint]] [[modal operators]] on [[homotopy category of a model category|homotopy category]] of [[cohesive model topos]])**

Given a [[cohesive model topos]] (Def. \ref{CohesiveInfinityTopos}), its [[adjoint quadruple]] (Remark \ref{AdjointTriples}) of [[derived functor]] between [[homotopy category of a model category|homotopy categorues]] (via Prop. \ref{QuillenAdjointTripleInducesAdjointTripleOfDerivedFunctors})

$$
  \label{CohesopmAdjointQuadruple}
  \Pi \dashv Disc \dashv \Gamma \dashv coDisc
  \;\;\colon\;\;
  Ho([\mathcal{C}^{op}, sSet_{Qu}]_{loc})
    \array{
      \overset{\phantom{AAA} \Pi_0 \phantom{AAA}}{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookleftarrow}
    }
  Ho(sSet)
$$

induce, by [[composition]] of functors, an [[adjoint triple]] (Remark \ref{AdjointTriples}) of [[adjoint modalities]] (via Prop. \ref{DerivedAdjointModalitiesFromFullyFaithfulQuillenAdjointQuadruples}):

$$
  &#643; \dashv \flat \dashv \sharp
  \;\;\colon\;\;
  Ho([\mathcal{C}^{op}, sSet_{Qu}]_{loc})
    \array{
      \overset{ &#643; \;\coloneqq\; Disc \circ \Pi_0  }{\hookleftarrow}
      \\
      \overset{\flat \;\coloneqq\; Disc \circ \Gamma  }{\longrightarrow}
      \\
      \overset{ \sharp \;\coloneqq\; coDisc\circ \Gamma }{\hookleftarrow}
    }
  Ho([\mathcal{C}^{op}, sSet_{Qu}]_{loc})
  \,.
$$

Since $Disc$ and $coDisc$ are [[fully faithful functors]] by assumption,
these are ([[comodal operator|co-]])[[modal operators]] (Def. \ref{ModalOperator}), (by Prop. \ref{DerivedAdjointModalitiesFromFullyFaithfulQuillenAdjointQuadruples} and Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}).

We pronounce these as follows:

| $\phantom{A}$ [[shape modality]] $\phantom{A}$ | $\phantom{A}$ [[flat modality]] $\phantom{A}$ | $\phantom{A}$ [[sharp modality]] $\phantom{A}$ |
|--------------------|-------------------|--------------------|
|   $\phantom{A}$  $&#643; \;\coloneqq\; Disc \circ \Pi_0$  $\phantom{A}$ | $\phantom{A}$ $\flat \;\coloneqq\; Disc \circ \Gamma$ $\phantom{A}$  | $\phantom{A}$ $\sharp \;\coloneqq\; coDisc \circ \Gamma $ $\phantom{A}$  |
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


$\,$


### Elastic $\infty$-Toposes
 {#ElasticInfinityToposes}

The following is a refinement to [[homotopy theory]] of the notion of _[[elastic topos]]_ (Def. \ref{DifferentialCohesion}):

+-- {: .num_defn #ElasticModelTopos}
###### Definition
**([[elastic model topos]]

Given a [[cohesive model topos]] $[\mathcal{C}_{red}^{op}, sSet_{Qu}]_{{proj/inj} \atop loc}$ (Def. \ref{CohesiveInfinityTopos}), a _[[differential cohesion|differentially cohesive]]_ or _[[elastic model topos]]_ over it is another cohesive model topos $[\mathcal{C}_{red}^{op}, sSet_{Qu}]_{{proj/inj} \atop loc}$ equipped with a system of [[Quillen adjoint quadruples]] (Def. \ref{QuillenAdjointTriple}) of the form

$$
  \array{
  \phantom{
  sSet_{Qu}
    \underoverset
      {{\longrightarrow}}
      {\overset{\Pi_{red}}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}      
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{proj \atop loc}
    \underoverset
      {\underset{id}{\longleftarrow}}
      {\overset{id}{\longrightarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu} }
  }
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{proj \atop loc}
    \underoverset
      {{\longleftarrow}}
      {\overset{\iota_{inf}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{proj \atop loc}
  \\
  sSet_{Qu}
    \underoverset
      {{\longrightarrow}}
      {\overset{\Pi_{red}}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}      
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{proj \atop loc}
    \underoverset
      {{\longleftarrow}}
      {\overset{id}{\longrightarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu} }
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
    \underoverset
      {{\longrightarrow}}
      {\overset{ \Pi_{inf} }{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{proj \atop loc}
  \\
  sSet_{Qu}
    \underoverset
      {{\longleftarrow}}
      {\overset{Disc_{red}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
    \underoverset
      {{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu} }
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
    \underoverset
      {{\longleftarrow}}
      {\overset{ Disc_{inf} }{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
  \\
  sSet_{Qu}
    \underoverset
      {\underset{coDisc_{red}}{\longrightarrow}}
      {\overset{\Gamma_{red}}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}      
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
    \underoverset
      {\phantom{\underset{id}{\longrightarrow}}}
      {\overset{id}{\phantom{\longleftarrow}}}
      {\phantom{\phantom{{}_{Qu}}\simeq_{Qu}} }
  \phantom{
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
  }
    \underoverset
      {\phantom{{\longleftarrow}}}
      {\overset{ \Gamma_{inf} }{\phantom{\longrightarrow}}}
      {\phantom{\phantom{{}_{Qu}}\bot_{Qu}}}
   \phantom{[\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}}
  }
$$

such that 

1. $(\iota_{inf} \dashv \Pi_{inf})$ is a [[Quillen coreflection]] (Def. \ref{QuillenReflection});

1. $(\Pi_{inf} \dashv Disc_{inf})$ is a [[Quillen reflection]] (Def. \ref{QuillenReflection}).

=--


+-- {: .num_defn #InfinityElasticSite}
###### Definition
**([[∞-elastic site]])**

For $\mathcal{C}_{red}$ an [[∞-cohesive site]] (Def. \ref{InfinityCohesiveSite}), an _infinitesimal neighbourhood site_ of $\mathcal{C}_{red}$ is a [[coreflective subcategory]]-inclusion into another [[∞-cohesive site]] $\mathcal{C}$

$$
  \mathcal{C}_{red}
    \underoverset
      {\underset{\phantom{AA}\Pi_{inf}\phantom{AA}}{\longleftarrow}}
      {\overset{\iota_{inf}}{\hookrightarrow}}
      {\bot}
  \mathcal{C}
$$

such that

1. both $\iota_{inf}$ and $\Pi_{inf}$ send [[covers]] to [[covers]];

1. the [[left Kan extension]] of $\iota_{inf}$ [[preserved limit|preserves]] [[fiber products]] $y(U_i) \times_{y(X)} y(u_j)$ of morphisms in a [[covering]] $\{U_i \overset{\iota_i}{\to} X\}$;

1. if $\{ U_i \overset{\iota_i}{\to} X \}$ is a covering family in $\mathcal{C}_{red}$, and $p(\widehat X) \longrightarrow X$ is any morphism in $\mathcal{C}_{red}$, then there is a covering familiy $\{ \widehat U_i \overset{\widehat\iota_j}{\to} \widehat X \}$ such that for all $i$ there is a $j$ and a [[commuting square]] of the form

   \[
     \label{LiftingOfCoversThroughPiInfInElasticSite}
     \array{
       \Pi_{inf}(\widehat U_j) &\longrightarrow& U_i
       \\
       {}^{\mathllap{ \Pi_{inf}(\widehat\iota_j) }}\Big\downarrow 
         && 
       \Big\downarrow{}^{\mathrlap{ \iota_i }}
       \\
       \Pi_{inf}(\widehat X) &\longrightarrow& X
     }
   \]

We also call this an _[[∞-elastic site]]_, for short.

=--


+-- {: .num_prop #ModelToposOverInfinityElasticSiteIsElasticModelTopos}
###### Proposition
**([[model topos]] over [[∞-elastic site]] is [[elastic model topos]])**

Let 

$$
  \mathcal{C}_{red}
    \underoverset
      {\underset{\phantom{AA}\Pi_{inf}\phantom{AA}}{\longleftarrow}}
      {\overset{\iota_{inf}}{\hookrightarrow}}
      {\bot}
  \mathcal{C}
$$

be an [[∞-elastic site]] (Def. \ref{InfinityElasticSite}). Then [[Kan extension]] (Prop. \ref{TopologicalLeftKanExtensionBCoend}) [[enriched category theory|enriched]] over [[sSet]] (Example \ref{ExamplesOfCosmoi})  induces on the corresponding [[cohesive (infinity,1)-toposes|cohesive]] [[model toposes]] (Prop. \ref{OverInfinityCohesiveSiteCohesiveInfinityTopos}) the structure of an [[elastic model topos]] (Def. \ref{ElasticModelTopos}).


=--

+-- {: .proof}
###### Proof

By Example \ref{QuillenAdjointQuadrupleOfHomotopyKanExtensionAlongAdjointPair} we have a [[Quillen adjoint quadruple]] for the global [[projective model structure on simplicial presheaves]] of the form

$$
  [\mathcal{C}^{op}_{red}, sSet_{Qu}]_{proj}
    \underoverset
      {{\longleftarrow}}
      {\overset{ \iota_{inf} }{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}_{red}, sSet_{Qu}]_{inj}
    \underoverset
      {{\longrightarrow}}
      {\overset{C = L'}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}_{red}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{\phantom{A=} R'}{\longleftarrow}}
      {\overset{R = C'}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
$$

Here we denote [[left Kan extension]] along a functor by the same symbol as that functor, which is consistent by Prop. \ref{LeftKanExtensionPreservesRepresentableFunctors}.

By Prop. \ref{SimplicialPresheavesIsProperCombinatorialSimplicial} all [[model categories]] appearing here are [[left proper model category|left proper]] [[simplicial model categories]], and by Def. \ref{BousfieldLocalizationOfModelCategories} [[left Bousfield localization]] retains the [[class]] of [[cofibrations]].  Therefore Prop. \ref{RecognitionOfSimplicialQuillenAdjunction} says that to see that this is also a [[Quillen adjoint quadruple]] for the [[local model structure on simplicial presheaves]] (Prop. \ref{TopologicalLocalization}) it is sufficient that, for each [[Quillen adjunction]], the [[right adjoint]] preserves [[fibrant objects]], hence Cech-[[local objects]] (Def. \ref{DerivedLocalObjects}).

For each [[right adjoint]] $R$ here this means to consider any [[covering]] $\{U_i \overset{}{\to} X\}$ (either in $\mathcal{C}_{red}$ or in $\mathcal{C}$) with induced [[Cech nerve]] $C(\{U_i\})$ (Example \ref{CechNerve}) and to check that for a fibrant object $\mathbf{X}$ in the global projective/injective [[model structure on simplicial presheaves]], that 

$$
  [X, R\mathbf{X}] \longrightarrow [ C(\{U_i\}), R\mathbf{X} ]
$$

is a [[weak equivalence]]. Notice that this is indeed already the image under the correct [[derived hom-functor]], Def. \ref{DerivedHomFunctorPOnSimplicialModelCategory}, since both [[sites]] are assumed to be [[∞-cohesive sites]] (Def. \ref{InfinityCohesiveSite}), which means in particular that $C(\{U_i\})$ is projectively cofibrant, and hence also injectively cofibrant, by Prop. \ref{ModelCategoriesOfSimplicialPresheaves}.

Now by the [[enriched adjunction]]-isomorphism (eq:EnrichedAdjunctionIsomorphism) this means equivalently that 

\[
  \label{LocalityForInfinityCohesiveSite}
  [L X, \mathbf{X}] \longrightarrow [ L C(\{U_i\}), \mathbf{X} ]
\]

is a weak equivalence. This we now check in each of the three cases:

For the case $(\iota_{inf} \dashv \Pi_{inf})$ we have that 

$$
  \iota_{inf} C(\{U_i\}) \simeq C(\{\iota_{inf} U_i\})
$$

by the assumption that $\iota_{inf}$ preserves fiber products of [[Yoneda embedding]]-[[images]] of morphisms in a [[covering]]. Moreover, by the assumption that $\iota_{inf}$ preserves [[covering]]-families, $C(\{\iota_{inf} U_i\})$ is itself the [[Cech nerve]] of a covering family, and hence (eq:LocalityForInfinityCohesiveSite) is a weak equivalence since $\mathbf{X}$ is assumed to be a [[local object]].

The same argument directly applies also to $(\Pi_{inf} \dashv Disc_{inf})$, where now the respect of $\Pi_{inf}$ for fiber products follows already from the fact that this is a [[right adjoint]] (since [[right adjoints preserve limits]], Prop. \ref{AdjointsPreserveCoLimits}).

In the same way, for $(Disc_{inf} \dashv \Gamma_{inf})$ we need to check that $[ C(\{Disc_{inf}U_i\}) \to Disc_{inf} X, \mathbf{X} ]$ is a weak equivalence. Now $Disc_{inf}$ is no longer a [[left Kan extension]], hence $Disc_{inf}(U_i) \to Disc_{inf}(X)$ is no longer a morphism of [[representable presheaves]]. But the third assumption (eq:LiftingOfCoversThroughPiInfInElasticSite) on an $\infty$-elastic site manifestly means, under the adjunction isomorphism (eq:HomIsomorphismForAdjointFunctors) for $(Pi_{inf} \dashv Disc_{inf})$ that $Disc_{inf}(U_i) \to Disc_{inf}(X)$ is a [[local epimorphism]] (Def. \ref{LocalEpimorphism}). Therefore Prop. \ref{CechNerveProjectionOfLocalEpimorphismIsLocalWeakEquivalence} implies that 

$$
  C(\{Disc_{inf} U_i\}) \to Disc_{inf} X
$$

is a weak equivalence. With this, the fact (Prop. \ref{SimplicialPresheavesIsProperCombinatorialSimplicial} with Prop. \ref{ExistenceOfLeftBousfieldLocalization}) that $[\mathcal{C}^{op}, sSet_{Qu}]_{inj, loc}$ is a [[simplicial model category]] (Def. \ref{SimplicialModelCategory}) implies that $[C(\{Disc_{inf} U_i\}) \to Disc_{inf} X, \mathbf{X}]$ is a weak equivalence.

=--

The following is a refinement to [[homotopy theory]] of the [[adjoint modalities]] on an [[elastic topos]] from Def. \ref{DiffCohesiveModalities}:

+-- {: .num_defn #DerivedDiffCohesiveModalities}
###### Definition
**([[derived functor|derived]] [[adjoint modalities]] on [[elastic model topos]])**

Given an [[elastic model topos]] (def. \ref{ElasticModelTopos}), [[composition]] composition of the [[derived functors]] (Prop. \ref{QuillenAdjointTripleInducesAdjointTripleOfDerivedFunctors}) yields via Prop. \ref{DerivedAdjointModalitiesFromFullyFaithfulQuillenAdjointQuadruples} and Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}, the following [[adjoint modalities]] (Def. \ref{AdjointModality}) on the [[homotopy category of a model category|homotopy category]] (Def. \ref{HomotopyCategoryOfAModelCategory})

$$
  \Re \dashv \Im \dashv \&
  \;\;\colon\;\;
  Ho([\mathcal{C}^{op}, sSet]_{loc})
    \array{
      \overset{ \Re \;\coloneqq\; \iota_{inf} \circ \Pi_{inf}  }{\longleftarrow}
      \\
      \overset{\Im \;\coloneqq\; Disc_{inf} \circ \Pi_{inf}  }{\longrightarrow}
      \\
      \overset{ \& \;\coloneqq\; Disc_{inf}  \circ \Gamma_{inf} }{\longleftarrow}
    }
  Ho([\mathcal{C}^{op}, sSet]_{loc})
  \,.
$$

Since $\iota_{inf}$ and $Disc_{inf}$ are [[fully faithful functors]] by assumption, these are ([[comodal operator|co-]])[[modal operators]] (Def. \ref{ModalOperator}) on the [[cohesive topos]], by (Prop. \ref{  Ho([\mathcal{C}^{op}, sSet]_{loc})
} and Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}).

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


+-- {: .num_prop #DefivedProgressionOfModalitiesOnElasticTopos}
###### Proposition
**(progression of [[derived functor|derived]] [[adjoint modalities]] on [[elastic model topos]])**

Let $[\mathcal{C}^{op}, sSet]_{{proj/inj} \atop loc}$ be an [[elastic model topos]] (Def. \ref{ElasticModelTopos}) and consider the corresponding [[derived functor|derived]] [[adjoint modalities]] which it inherits

1. for being a [[cohesive topos]], from Def. \ref{DerivedCohesiveModalities},

1. for being an [[elastic topos]], from Def. \ref{DerivedDiffCohesiveModalities}:


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

This is just as in Prop. \ref{ProgressionOfModalitiesOnElasticTopos}.

=--


$\,$

### Solid $\infty$-Toposes
 {#SolidModelToposes}

The following is a refinement to [[homotopy theory]] of the notion of _[[solid topos]]_ (Def. \ref{SuperDifferentialCohesion}):

+-- {: .num_defn #SolidModelTopos}
###### Definition
**([[solid model topos]])**

Given an [[elastic model topos]] $[\mathcal{C}^{op}_{inf}, sSet_{Qu}]_{{proj/inj} \atop loc}$ (Def. \ref{ElasticModelTopos}) a _[[solid model topos]]_ over it is another [[elastic model topos]] $[\mathcal{C}^{op}, sSet_{Qu}]_{{proj/inj} \atop loc}$ and a system of [[Quillen adjoint quadruples]] (Def. \ref{QuillenAdjointTriple}) as follows 

$$
  \array{
  \phantom{
  sSet_{Qu}
    \underoverset
      {{\longrightarrow}}
      {\overset{\Pi_{red}}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}      
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{proj \atop loc}
    \underoverset
      {\underset{id}{\longleftarrow}}
      {\overset{id}{\longrightarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu} }
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{proj \atop loc}
    \underoverset
      {{\longleftarrow}}
      {\overset{\iota_{inf}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{proj \atop loc}
    \underoverset
      {{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu} }
  }
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{proj \atop loc}
    \underoverset
      {{\longrightarrow}}
      {\overset{even}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj \atop loc}
  \\
  \phantom{
  sSet_{Qu}
    \underoverset
      {{\longrightarrow}}
      {\overset{\Pi_{red}}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}      
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{proj \atop loc}
    \underoverset
      {\underset{id}{\longleftarrow}}
      {\overset{id}{\longrightarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu} }
  }
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{proj \atop loc}
    \underoverset
      {{\longleftarrow}}
      {\overset{\iota_{inf}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{proj \atop loc}
    \underoverset
      {{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu} }
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{proj \atop loc}
    \underoverset
      {{\longleftarrow}}
      {\overset{\iota_{sup}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
  \\
  sSet_{Qu}
    \underoverset
      {{\longrightarrow}}
      {\overset{\Pi_{red}}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}      
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{proj \atop loc}
    \underoverset
      {{\longleftarrow}}
      {\overset{id}{\longrightarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu} }
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
    \underoverset
      {{\longrightarrow}}
      {\overset{ \Pi_{inf} }{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{proj \atop loc}
    \underoverset
      {{\longleftarrow}}
      {\overset{id}{\longrightarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu} }
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
    \underoverset
      {{\longrightarrow}}
      {\overset{\Pi_{sup}}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
  \\
  sSet_{Qu}
    \underoverset
      {{\longleftarrow}}
      {\overset{Disc_{red}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
    \underoverset
      {{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu} }
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
    \underoverset
      {{\longleftarrow}}
      {\overset{ Disc_{inf} }{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
    \underoverset
      {{\longrightarrow}}
      {\overset{\;\;id}{\longleftarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu} }
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
    \underoverset
      {{\longleftarrow}}
      {\overset{\;Disc_{sup}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
  \\
  sSet_{Qu}
    \underoverset
      {\underset{coDisc_{red}}{\longrightarrow}}
      {\overset{\Gamma_{red}}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}      
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
    \underoverset
      {\phantom{\underset{id}{\longrightarrow}}}
      {\overset{id}{\phantom{\longleftarrow}}}
      {\phantom{\phantom{{}_{Qu}}\simeq_{Qu}} }
  \phantom{
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}
  }
    \underoverset
      {\phantom{{\longleftarrow}}}
      {\overset{ \Gamma_{inf} }{\phantom{\longrightarrow}}}
      {\phantom{\phantom{{}_{Qu}}\bot_{Qu}}}
   \phantom{[\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{inj\phantom{r} \atop loc}}
    \underoverset
      {\underset{}{\phantom{\longrightarrow}}}
      {\overset{id}{\phantom{\longleftarrow}}}
      {\phantom{\phantom{{}_{Qu}}\simeq_{Qu} }}
  \phantom{[\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{proj \atop loc}}
    \underoverset
      {\phantom{{\longleftarrow}}}
      {\overset{\Gamma_{sup}}{\phantom{\longrightarrow}}}
      {\phantom{\phantom{{}_{Qu}}\bot_{Qu}}}
  \phantom{[\mathcal{C}^{op}, sSet_{Qu}]_{proj \atop loc}}
  }
$$

such that

1. $(even \dashv \iota_{sup})$ is a [[Quillen reflection]] (def. \ref{QuillenReflection});

1. $(\iota_{sup} \dashv \Pi_{sup})$ is a [[Quillen coreflection]].

=--


+-- {: .num_defn #InfinitySolidSite}
###### Definition
**([[∞-solid site]])**

For 
$
  \mathcal{C}_{red}
    \underoverset
      {\underset{\phantom{AA}\Pi_{inf}\phantom{AA}}{\longleftarrow}}
      {\overset{\iota_{inf}}{\hookrightarrow}}
      {\bot}
  \mathcal{C}_{inf}
$
an [[∞-elastic site]] (Def. \ref{InfinityElasticSite}) over an _[[∞-cohesive site]]_ (Def. \ref{InfinityCohesiveSite}), a _super-infinitesimal neighbourhood site_ is a [[reflective subcategory|reflective]]/[[coreflective subcategory]]-inclusion into another [[∞-elastic site]] $
  \mathcal{C}_{red}
    \underoverset
      {\underset{\phantom{AA}\Pi_{inf}\phantom{AA}}{\longleftarrow}}
      {\overset{\iota_{inf}}{\hookrightarrow}}
      {\bot}
  \mathcal{C}
$


$$
  \ast
    \array{
      \phantom{\underoverset{\bot}{\phantom{AA}even\phantom{AA}}{\longleftarrow}}      
      \\
      \phantom{\underoverset{\bot}{\phantom{AA}\iota_{inf}\phantom{AA}}{\hookrightarrow}}
      \\
      \underoverset{\bot}{\phantom{AA}\Pi\phantom{AA}}{\longleftarrow}
      \\
      \underoverset{}{\phantom{A}Disc\phantom{A}}{\hookrightarrow}
    }
  \mathcal{C}_{red}
    \array{
      \phantom{\underoverset{\bot}{\phantom{AA}even\phantom{AA}}{\longleftarrow}}      
      \\
      \underoverset{\bot}{\phantom{AA}\iota_{inf}\phantom{AA}}{\hookrightarrow}
      \\
      \underoverset{}{\phantom{AA}\Pi_{inf}\phantom{AA}}{\longleftarrow}
      \\
      \phantom{\underoverset{}{\phantom{A}Disc\phantom{A}}{\hookrightarrow}}
    }
  \mathcal{C}_{inf}
    \array{
      \underoverset{\bot}{\phantom{AA}even\phantom{AA}}{\longleftarrow}      
      \\
      \underoverset{\bot}{\phantom{AA}\iota_{sup}\phantom{AA}}{\hookrightarrow}      
      \\
      \underoverset{}{\phantom{AA}\Pi_{sup}\phantom{AA}}{\longleftarrow}
      \\
      \phantom{\underoverset{}{\phantom{A}Disc\phantom{A}}{\hookrightarrow}}
    }
  \mathcal{C}_{sup}
$$

such that

1. all of $even$, $\iota_{sup}$ and $\Pi_{inf}$ send [[covers]] to [[covers]];

1. the [[left Kan extension]] of $even$ [[preserved limit|preserves]] [[fiber products]] $y(U_i) \times_{y(X)} y(u_j)$ of morphisms in a [[covering]] $\{U_i \overset{\iota_i}{\to} X\}$;

=--


+-- {: .num_prop #ModelToposOverInfinitySolidSiteIsSolidModelTopos}
###### Proposition
**([[model topos]] over [[∞-solid site]] is [[solid model topos]])**

Let 

$$
  \ast
    \array{
      \phantom{\underoverset{\bot}{\phantom{AA}even\phantom{AA}}{\longleftarrow}}      
      \\
      \phantom{\underoverset{\bot}{\phantom{AA}\iota_{inf}\phantom{AA}}{\hookrightarrow}}
      \\
      \underoverset{\bot}{\phantom{AA}\Pi\phantom{AA}}{\longleftarrow}
      \\
      \underoverset{}{\phantom{A}Disc\phantom{A}}{\hookrightarrow}
    }
  \mathcal{C}_{red}
    \array{
      \phantom{\underoverset{\bot}{\phantom{AA}even\phantom{AA}}{\longleftarrow}}      
      \\
      \underoverset{\bot}{\phantom{AA}\iota_{inf}\phantom{AA}}{\hookrightarrow}
      \\
      \underoverset{}{\phantom{AA}\Pi_{inf}\phantom{AA}}{\longleftarrow}
      \\
      \phantom{\underoverset{}{\phantom{A}Disc\phantom{A}}{\hookrightarrow}}
    }
  \mathcal{C}_{inf}
    \array{
      \underoverset{\bot}{\phantom{AA}even\phantom{AA}}{\longleftarrow}      
      \\
      \underoverset{\bot}{\phantom{AA}\iota_{sup}\phantom{AA}}{\hookrightarrow}      
      \\
      \underoverset{}{\phantom{AA}\Pi_{sup}\phantom{AA}}{\longleftarrow}
      \\
      \phantom{\underoverset{}{\phantom{A}Disc\phantom{A}}{\hookrightarrow}}
    }
  \mathcal{C}_{sup}
$$

be an [[∞-solid site]] (Def. \ref{InfinitySolidSite}). Then [[Kan extension]] (Prop. \ref{TopologicalLeftKanExtensionBCoend}) [[enriched category theory|enriched]] over [[sSet]] (Example \ref{ExamplesOfCosmoi})  induces on the corresponding [[elastic model toposes]] (Prop. \ref{ElasticModelTopos}) the structure of a [[solid model topos]] (Def. \ref{SolidModelTopos}).


=--

The following is a refinement to [[homotopy theory]] of the [[modal operators]] on a [[solid topos]] from Def. \ref{SuperDiffCohesiveModalities}:

+-- {: .num_defn #DerivedSuperDiffCohesiveModalities}
###### Definition
**([[derived functor|derived]] [[adjoint modalities]] on [[solid model topos]])** 

Given a [[solid model topos]] $[\mathcal{C}^{op}, sSet_{Qu}]_{{proj/inj} \atop loc}$ (Def. \ref{SolidModelTopos}), [[composition]] of [[derived functors]] via Prop. \ref{DerivedAdjointModalitiesFromFullyFaithfulQuillenAdjointQuadruples} and Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}, the following [[adjoint modalities]] (Def. \ref{AdjointModality})

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
these are ([[comodal operator|co-]])[[modal operators]] (Def. \ref{ModalOperator}) on the [[cohesive topos]], by (Prop. \ref{DerivedAdjointModalitiesFromFullyFaithfulQuillenAdjointQuadruples} and Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}).

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

Let $[\mathcal{C}^{op}, sSet_{Qu}]_{{proj/inj} \atop lco}$ be a [[solid model topos]] (Def. \ref{SolidModelTopos}) and consider the [[adjoint modalities]] which it inherits 

1. for being a [[cohesive topos]], from Def. \ref{DerivedCohesiveModalities}, 

1. for being an [[elastic topos]], from Def. \ref{DerivedDiffCohesiveModalities},

1. for being a [[solid topos]], from Def. \ref{DerivedSuperDiffCohesiveModalities}:


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

This is just as in Prop. \ref{ProgressionOfModalitiesOnSolidTopos}.

=--


$\,$

(...)
