
> This entry is one chapter of _[[geometry of physics]]_.

> next chapters: _[[geometry of physics -- smooth sets|smooth sets]]_, _[[geometry of physics -- homotopy types|homotopy types]]_


$\,$

***

$\,$

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


[[category theory|Category theory]] and [[topos theory]] concern the general abstract structure underlying [[algebra]], [[geometry]] and [[logic]]. They are ubiquituous in and indispensible for organizing conceptual mathematical frameworks.

We give here an introduction to the basic concepts and results, aimed at providing background for the [[synthetic differential geometry|synthetic]] [[higher differential geometry|higher]] [[geometry of physics -- supergeometry|supergeometry]] of relevance in formulations of fundamental [[physics]], such as used in the chapters _[[geometry of physics -- perturbative quantum field theory|on perturbative quantum field theory]]_ and _[[geometry of physics -- fundamental super p-branes|on fundamental super p-branes]]_.

This makes use of the following curious dictionary between [[category theory]]/[[topos theory]] and the [[geometry]] of [[generalized spaces]], which we will explain in detail (following [Grothendieck 65](functorial+geometry#Grothendieck65), [Lawvere 86, p. 17](space+and+quantity#Lawvere86), [[Some Thoughts on the Future of Category Theory|Lawvere 91]]):

| $\phantom{A}$[[category theory]] | Rmk. \ref{PresaheavesAsGeneralizedSpaces}  | $\phantom{A}$[[geometry]] of [[generalized spaces]] |
|-------|--|---------|
| $\phantom{A}$[[presheaf]] | Expl. \ref{CategoryOfPresheaves} | $\phantom{A}$[[generalized space]] | 
| $\phantom{A}$[[representable presheaf]]$\phantom{A}$ | Expl. \ref{RepresentablePresheaves}$\phantom{A}$ |  $\phantom{A}$model [[space]] <br/> $\phantom{A}$regarded as [[generalized space]] |
| $\phantom{A}$[[Yoneda lemma]] | Prop. \ref{YonedaLemma}$\phantom{A}$  |  $\phantom{A}$sets of probes of [[generalized spaces]] <br/> $\phantom{A}$are indeed <br/> $\phantom{A}$sets of maps from model [[spaces]] $\phantom{A}$ |
| $\phantom{A}$[[Yoneda embedding]] $\phantom{A}$ | Prop. \ref{YonedaEmbedding}$\phantom{A}$ |  $\phantom{A}$nature of model [[spaces]] is preserved when <br/> $\phantom{A}$regarding them as [[generalized spaces]] $\phantom{A}$ |
| $\phantom{A}$[[Yoneda embedding]] is$\phantom{A}$ <br/> $\phantom{A}$[[free co-completion]]$\phantom{A}$ |  Prop. \ref{FreeCocompletion} | $\phantom{A}$[[generalized spaces]] really are$\phantom{A}$ <br/> $\phantom{A}$glued from ordinary [[spaces]]$\phantom{A}$  |
|  |  | |
| $\phantom{A}$**[[topos theory]]** | **Rmk. \ref{SheafConditionAsLocality}** |  $\phantom{A}$**[[local-global principle]] for [[generalized spaces]]**$\phantom{A}$  |
| $\phantom{A}$[[coverage]] | Defn. \ref{Coverage} | $\phantom{A}$notion of locality |
| $\phantom{A}$[[sheaf|sheaf condition]] | Defn. \ref{Sheaf}$\phantom{A}$ <br/> Prop. \ref{CechGroupoidCoRepresents} | $\phantom{A}$plots of [[generalized spaces]] <br/> $\phantom{A}$satisfy [[local-to-global principle]] $\phantom{A}$ |
| $\phantom{A}$[[comparison lemma]] | Prop. \ref{ComparisonLemma} |  $\phantom{A}$notion of [[generalized spaces]] <br/> $\phantom{A}$independent under change of model [[space]] | 
| $\phantom{A}$**[[gros topos|gros topos theory]]** |  **Rmk. \ref{CohesiveGeneralizedSpacesAsFoundations}** |  $\phantom{A}$**[[generalized spaces]] at the [[foundations]]** |
| $\phantom{A}$[[cohesion]] | Defn. \ref{CohesiveTopos}  | $\phantom{A}$[[generalized spaces]] obey <br/> $\phantom{A}$principles of [[differential topology]] |
| $\phantom{A}$[[differential cohesion]] | Defn. \ref{DifferentialCohesion} | $\phantom{A}$[[generalized spaces]] obey <br/> $\phantom{A}$principles of [[differential geometry]] |
| $\phantom{A}$super cohesion$\phantom{A}$ | Defn. \ref{SuperDifferentialCohesion} | $\phantom{A}$[[generalized spaces]] obey <br/> $\phantom{A}$principles of [[supergeometry]] |
{: style='margin:auto}
 
The perspective is that of _[[functorial geometry]]_ ([Grothendieck 65](#functorial+geometry#Grothendieck65)).  (For more exposition of this point see also at _[[motivation for sheaves, cohomology and higher stacks]]_.) This dictionary implies a wealth of useful tools for handling and reasoning about [[geometry]]:

We discuss [below](#BasicNotionsOfToposTheory) that [[sheaf toposes]], regarded as [[categories]] of [[generalized spaces]] via the above disctionary, are "convenient contexts" for geometry (Prop. \ref{PropertiesOfSheafToposes} below), in the technical sense that they provide just the right kind of generalization that makes all desireable constructions on spaces actually exist:

| $\phantom{A}$[[sheaf topos]]$\phantom{A}$ | $\phantom{A}$as [[category]] of [[generalized spaces]] $\phantom{A}$ |
|-----------------|-----------------|
| $\phantom{A}$[[Yoneda embedding]]: $\phantom{A}$ | $\phantom{A}$contains and generalizes ordinary [[spaces]] $\phantom{A}$ | 
| $\phantom{A}$has all [[limits]]: $\phantom{A}$ | $\phantom{A}$contains all [[Cartesian products]] and [[intersections]] $\phantom{A}$ |
| $\phantom{A}$has all [[colimits]]: $\phantom{A}$ | $\phantom{A}$contains all [[disjoint unions]] and [[quotients]] |
| $\phantom{A}$[[cartesian closed category|cartesian closure]]: $\phantom{A}$ | $\phantom{A}$contains all [[mapping spaces]]$\phantom{A}$ |
| $\phantom{A}$[[locally cartesian closed category|local cartesian closure]]: $\phantom{A}$ | $\phantom{A}$contains all [[fiber]]-wise [[mapping spaces]] $\phantom{A}$ |
{: style='margin:auto}

Notably [[mapping spaces]] play a pivotal role in [[physics]], in the guise of [[spaces of field histories]], but fall outside the applicability of traditional formulations of [[geometry]] based on just [[manifolds]]. [[topos theory|Topos theory]] provides their existence (Prop. \ref{PropertiesOfSheafToposes} below) and the relevant infrastructure, for example for the construction of [[transgression of differential forms]] to mapping spaces of [[smooth sets]], that is the basis for [[sigma-model]]-[[field theories]]. This is discussed in the following chapters _[[geometry of physics -- smooth sets|on smooth sets]]_ and _[[geometry of physics -- supergeometry|on supergeometry]]_.
 
In conclusion, one motivation for [[category theory]] and [[topos theory]] is _a posteriori_: As a matter of experience, there is just no other toolbox that allows to deeply understand and handle the [[geometry of physics]]. Similar comments apply to a wealth of other topics of mathematics.

We offer also an _a priori_ motivation: _Category theory is the theory of duality._

<div style="float:right;margin:0 10px 10px 0;"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/74/Cup_or_faces_paradox.svg/450px-Cup_or_faces_paradox.svg.png" width="200"></div>

_[[duality|Duality]]_ is of course an ancient notion in [[philosophy]]. At least as a term, it makes a curious re-appearance in the conjectural [[theory (physics)|theory]] of fundamental [[physics]] formerly known as _[[string theory]]_ as _[[duality in string theory]]_. In both cases, the literature left some room in delineating what precisely is meant. But the philosophically inclined mathematician could notice (see [Lambek 82](adjoint+functor#Lambek82)) that an excellent candidate to make precise the idea of _[[duality]]_ is the mathematical concept of _[[adjoint functor|adjunction]]_, from [[category theory]]. This is particularly pronounced for _[[adjoint triples]]_ (Remark \ref{AdjointTriples} below) and their induced [[adjoint modalities]] ([[Some Thoughts on the Future of Category Theory|Lawvere 91]], see Def. \ref{AdjointModality} below), which exhibit a given "[[modality|mode of being]]" of any object $X$ as intermediate between two dual opposite extremes (Prop. \ref{ComparisonMorphismBetweenOppositeExtremes} below):

$$
  \Box X 
    \overset{\phantom{AAAA}}{\longrightarrow}
  X 
    \overset{\phantom{AAAA}}{\longrightarrow}
  \bigcirc X
$$

For example, _[[cohesion|cohesive]]_ [[geometry|geometric]] [[structure]] on [[generalized spaces]] is captured, this way, as [[modality]] in between the [[discrete object|discrete]] and the [[codiscrete object|codiscrete]] (Example \ref{DiscreteTopologicalSpaces}, and Def. \ref{CohesiveTopos} below).

Historically, [[category theory]] was introduced in order to make precise the concept of _[[natural transformation]]_: The concept of _[[functors]]_ was introduced just so as to support that of natural transformations, and the concept of _[[categories]]_ only served that of functors (see e.g. [Freyd 65, Part II](category+theory#Freyd65)). 

<div style="float:left;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/Adjointness.jpg" width="460">
</div>

But natural transformations are, in turn, exactly the basis for the concept of _[[adjoint functors]]_ (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets} below), equivalently _[[adjunctions]] between categories_ (Prop. \ref{AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat} below), shown on the left. 
All _[[universal constructions]]_, the heart of category theory, are special cases of [[adjoint functors]] -- hence of dualities, if we follow [Lambek 82](adjoint+functor#Lambek82): This includes the concepts of _[[limits]]_ and _[[colimits]]_ (Def. \ref{Limits} below), [[ends]] and [[coends]] (Def. \ref{EndAndCoendInTopcgSmash} below) [[Kan extensions]] (Prop. \ref{TopologicalLeftKanExtensionBCoend} below), and the behaviour of these constructions, such as for instance the [[free co-completion]] nature of the [[Yoneda embedding]] (Prop. \ref{FreeCocompletion} below). 

Therefore it makes sense to regard category theory as the **theory of adjunctions**, hence the **theory of duality**:

<br/>

| $\phantom{A}$hierarchy of concepts$\phantom{A}$  | $\phantom{A}$[[category theory]]$\phantom{A}$ | $\phantom{A}$[[enriched category theory|enriched]]$\phantom{A}$ | $\phantom{A}$[[model category|homotopical]]$\phantom{A}$ |
|------------------------|------------|--------------------------|------|
| $\phantom{A}$ [[adjoint equivalence]] / $\phantom{A}$ <br/> $\phantom{AA}$ [[adjoint equivalence|dual equivalence]] $\phantom{AA}$ | $\phantom{A}$ Def. \ref{AdjointEquivalenceOfCategories} $\phantom{A}$ | $\phantom{A}$ Def. \ref{EnrichedEquivalenceOfCategories} $\phantom{A}$ | $\phantom{A}$Def. \ref{QuillenEquivalence} |
| $\phantom{A}$ [[adjoint functor|adjunction]] / [[duality]] $\phantom{A}$  | $\phantom{A}$ Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets} $\phantom{A}$ |  $\phantom{A}$ Def. \ref{EnrichedAdjunction} $\phantom{A}$  |  $\phantom{A}$Def. \ref{QuillenAdjunction} | 
| $\phantom{A}$ [[natural transformation]] $\phantom{A}$ | $\phantom{A}$ Def. \ref{NaturalTransformations} $\phantom{A}$ |  $\phantom{A}$ Def. \ref{EnrichedNaturalTransformation} $\phantom{A}$ |  |
| $\phantom{A}$ [[functor]] $\phantom{A}$ | $\phantom{A}$ Def. \ref{Functors} $\phantom{A}$ |  $\phantom{A}$ Def. \ref{TopologicallyEnrichedFunctor} $\phantom{A}$ |  | 
| $\phantom{A}$ [[category]] $\phantom{A}$ | $\phantom{A}$ Def. \ref{Categories} $\phantom{A}$ | $\phantom{A}$ Def. \ref{TopEnrichedCategory} $\phantom{A}$ | $\phantom{A}$ Def. \ref{ModelCategory} |
{: style='margin:auto}



The pivotal role of [[adjunctions]] in [[category theory]] ([Lawvere 08](adjoint+functor#fn:1)) and in the [[foundations of mathematics]] ([[Adjointness in Foundations|Lawvere 69]], [[Cohesive Toposes and Cantor's lauter Einsen|Lawvere 94]] ) was particularly amplified by [[F. W. Lawvere]][^LawvereOnAdjointFunctors]. Moreover, [[Lawvere]] saw the future of category theory ([[Some Thoughts on the Future of Category Theory|Lawvere 91]]) as concerned with [[adjunctions]] expressing systems of archetypical dualities that reveal foundations for [[geometry]] ([Lawvere 07](cohesive+topos#LawvereAxiomatic)) and [[physics]] ([[Toposes of laws of motion|Lawvere 97]], see Def. \ref{CohesiveTopos} and Def. \ref{DifferentialCohesion} below). He suggested ([Lawvere 94](objective+and+subjective+logic#Lawvere94)) this as a precise formulation of core aspects of the _theory of everything_
of early 19th century [[philosophy]]: [[Hegel]]'s _[[Science of Logic]]_.

[^LawvereOnAdjointFunctors]: "the universality of the concept
of adjointness, which was first isolated and named in the conceptual sphere of category theory" ([Lawvere 69](#Lawvere69)) "In all those areas where category theory is actively used the categorical concept of adjoint functor has come to play a key role." (first line from _[An interview with William Lawvere](https://ncatlab.org/nlab/show/William+Lawvere#Interview07)_, paraphrasing the first paragraph of _[Taking categories seriously](William+Lawvere#TakingCategoriesSeriously)_)


These days, of course, _[[theories of everything]]_, such as [[string theory]], are understood less ambitiously than Hegel's ontological process,
as mathematical formulations of fundamental theories of physics, that could conceptually unify the hodge-podge of currently available "standard models" [[standard model of particle physics|of particle physics]] and [[standard model of cosmology|of cosmology]] to a more coherent whole.

The idea of _[[duality in string theory]]_ refers to different perspectives on physics that appear dual to each other while being _equivalent_.
But one of the basic results of category theory (Prop. \ref{EveryEquivalenceOfCategoriesComesFromAnAdjointEquivalence}, below) is that equivalence is indeed a special case of adjunction. This allows to explore the possibility that there is more than a coincidence of terms.

Of course the usage of the term _[[duality in string theory]]_ is too loose for one to expect to be able to refine each occurrence of the term in the literature to a mathematical adjunction. However, we will see mathematical formalizations of core aspects of
key string-theoretic dualities, such as _[[topological T-duality]]_ and the _[[duality between M-theory and type IIA string theory]]_, in terms of [[adjunctions]]. Indeed, at the heart of these _[[dualities in string theory]]_ is the phenomenon of _[[double dimensional reduction]]_, which turns out to be formalized by one of the most fundamental adjunctions in ([[higher category theory|higher]] [[category theory]] ([[base change]] along the point inclusion into a [[classifying space]]). All this is discussed in the chapter on _[[geometry of physics -- fundamental super p-branes|fundamental super p-branes]]_.

This suggests that there may be a deeper relation here between the superficially alien uses of the word "duality", that is worth exploring.

In this respect it is worth noticing that core structure of string/M-theory arises via [[universal constructions]] from the [[superpoint]] (as explained in the chapter _[[geometry of physics -- fundamental super p-branes|on fundamental super p-branes]]_), while the superpoint itself arises, in a sense made precise by [[category theory]], "from nothing", by a system of twelve [[adjunctions]] (explained in the chapter [[geometry of physics -- supergeometry|on supergeometry]]). 

$\,$

Here we introduce the requisites for understanding these statements.

$\,$



#Contents#
* table of contents
{:toc}


[[!include geometry of physics – basic notions of category theory]]

$\,$

[[!include geometry of physics - basic notions of categorical algebra]]

$\,$

[[!include geometry of physics - universal constructions]]

$\,$

[[!include geometry of physics - basic notions of topos theory]]


$\,$

[[!include geometry of physics - cohesive toposes]]

$\,$

## Basic concepts of homotopy theory

Traditionally, [[mathematics]] and [[physics]] have been [[foundations|founded]] on [[set theory]], whose concept of _[[sets]]_ is that of "bags of distinguishable points". 

But fundamental [[physics]] is governed by the _[[gauge principle]]_. This says that given any two "things", such as two [[field histories]] $x$ and $y$, it is in general wrong to ask whether they are [[equality|equal]] or not, instead one has to ask where there is a _[[gauge transformation]]_ 

$$
  x \stackrel{\gamma}{\longrightarrow} y
$$

between them. In mathematics this is called a _[[homotopy]]_.

This principle applies also to [[gauge transformations]]/[[homotopies]] themselves, and thus leads to _[[gauge-of-gauge transformations]]_ or _[[homotopies of homotopies]]_

<center><img src="https://ncatlab.org/nlab/files/2Cell.jpg" width = "200"></center>

and so on to ever _[[higher gauge transformations]]_ or _[[higher homotopies]]_:

<center>
  <img src="https://ncatlab.org/nlab/files/3Cell.jpg" width = "200">
</center>

This shows that what $x$ an $y$ here are [[elements]] of is not really a [[set]] in the sense of [[set theory]]. Instead, such a collection of [[elements]] with [[higher gauge transformations]]/[[higher homotopies]] between them is called a _[[homotopy type]]_.

Hence the theory of [[homotopy types]] --  _[[homotopy theory]]_ -- is much like [[set theory]], but with the concept of [[gauge transformation]]/[[homotopy]] built right into its [[foundations]]. Homotopy theory is gauged mathematics.

Ideally, abstract homotopy theory would simply be a complete replacement of [[set theory]], obtained by _removing_ the assumption of strict [[equality]], relaxing it to [[gauge equivalence]]/[[homotopy]]. As such, abstract homotopy theory would be part and parcel of the [[foundations of mathematics]] themselves, not requiring any further discussion. This ideal perspective is the promise of _[[homotopy type theory]]_ and may become full practical reality in the next decades.

Until then, abstract homotopy theory has to be formulated on top of the traditional [[foundations of mathematics]] provided by [[set theory]], much like one may have to run a Linux emulator on a Windows machine, if one does happen to be stuck with the latter.

A very convenient and powerful such emulator for homotopy theory within set theory is _[[model categories|model category theory]]_, originally due to [Quillen 67](model+category#Quillen67) and highly developed since. This we introduce here. 

The idea is to consider ordinary [[categories]] ([this Def.](geometry+of+physics+--+categories+and+toposes#Categories)) but with the understanding that some of their [[morphisms]] 

$$
  X 
    \overset{f}{\longrightarrow}
  Y
$$

should be _[[homotopy equivalences]]_ (Def. \ref{HomotopyEquivalence}), namely similar to [[isomorphisms]] ([this Def.](geometry+of+physics+--+categories+and+toposes#Isomorphism)), but not necessarily satisfying the two [[equations]] defining an actual isomorphism 

$$
  f^{-1} \circ f \;=\; id_{X}
  \phantom{AAAA}
  f \circ f^{-1} \;=\; id_Y
$$ 

but intended to satisfy this only with [[equality]] relaxed to [[gauge transformation]]/[[homotopy]]:

\[
  \label{HomotopyEquivalenceCondition}
  f^{-1} \circ f \;\overset{gauge}{\Rightarrow}\; id_{X}
  \phantom{AAAA}
  f \circ f^{-1} \;\overset{gauge}{\Rightarrow}\; id_Y
  \,.
\] 

Such _would-be homotopy equivalences_ are called _[[weak equivalences]]_ (Def. \ref{CategoryWithWeakEquivalences} below). 

In principle, this information already defines a [[homotopy theory]] by a construction called _[[simplicial localization]]_, which turns [[weak equivalences]] into actual [[homotopy equivalences]] in a suitable way (Remark \ref{SimplicialLocalizationOutlook} below). 

However, without further tools this construction is very unwieldy. The extra structure of a _[[model category]]_ (Def. \ref{ModelCategory} below) on top of a [[category with weak equivalences]] provides a set of tools.

The idea here is to abstract (in Def. \ref{LeftAndRightHomotopyInAModelCategory} below) from the evident concepts in [[topological homotopy theory]] of _[[left homotopy]]_ (Def. \ref{LeftHomotopy}) and _[[right homotopy]]_ (Def. \ref{RightHomotopy}) between [[continuous functions]]: These are provided by continuous functions out of a [[cylinder|cylinder space]] $Cyl(X)  = X \times [0,1]$ or into a [[path space]] $Path(X) = X^{[0,1]}$, respectively, where in both cases the [[interval|interval space]] $[0,1]$ serves to parameterize the relevant [[gauge transformation]]/[[homotopy]].

Now a little reflection shows (this was the seminal insight of [Quillen 67](model+category#Quillen67)) that what really matters in this construction of homotopies is that the [[path space]] factors the [[diagonal morphism]] from a space $X$ to its [[Cartesian product]] as

$$
  diag_X 
    \;\colon\; 
  X 
    \underoverset{\text{weak equiv.}}{\text{ cofibration }}{\longrightarrow}
  Path(X)
     \overset{\text{ fibration }}{\longrightarrow}
  X \times X  
$$

while the cylinder serves to factor the [[codiagonal morphism]] as 

$$
  codiag_X
  \;\colon\;
  X \sqcup X
    \overset{ \text{cofibration} }{\longrightarrow}
  Cyl(X)
    \underoverset{ \text{weak equiv} }{ \text{fibration} }{\longrightarrow}
  X
$$

where in both cases "[[fibration]]" means something like _well behaved [[surjection]]_, while "[[cofibration]]" means something like _satisfying the [[lifting property]] (Def. \ref{LiftingAndExtension} below) against fibrations that are also weak equivalences_.

Such factorizations subject to lifting properties is what the definition of _[[model category]]_ axiomatizes, in some generality. That this indeed provides a good toolbox for handling [[homotopy equivalences]] is shown by the _[[Whitehead theorem]] in [[model categories]]_ (Lemma \ref{WhiteheadTheoremInModelCategories} below), which exhibits all [[weak equivalences]] as actual [[homotopy equivalences]] after passage to "good representatives" of objects (fibrant/cofibrant [[resolutions]], Def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory} below). Accordingly, the first theorem of model category theory ([Quillen 67, I.1 theorem 1](model+category#Quillen67), reproduced as Theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory} below), provides a tractable expression for the [[hom-sets]] modulo [[homotopy equivalence]] of the underlying [[category with weak equivalences]] in terms of actual morphisms out of [[cofibrant resolutions]] into [[fibrant resolutions]] (Lemma \ref{HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory} below).

This is then generally how [[model category]]-theory serves as a model for [[homotopy theory]]: All homotopy-theoretic constructions, such as that of [[long homotopy fiber sequences]] (Prop. \ref{LongFiberSequence} below), are reflected via constructions of ordinary [[category theory]] but applied to suitably [[resolution|resolved objects]].

$\,$


**Literature** ([Dwyer-Spalinski 95](model+category#DwyerSpalinski95))

$\,$


+-- {: .num_defn #CategoryWithWeakEquivalences}
###### Definition
**([[category with weak equivalences]])**

A **[[category with weak equivalences]]** is

1. a [[category]] $\mathcal{C}$ ([this Def.](geometry+of+physics+--+categories+and+toposes#Categories));

1. a sub-[[class]] $W \subset Mor(\mathcal{C})$ of its [[morphisms]];

such that

1. $W$ contains all the [[isomorphisms]] of $\mathcal{C}$;

1. $W$ is closed under **[[two-out-of-three]]**: in every [[commuting diagram]] in $\mathcal{C}$ of the form

   $$
     \array{
         && Y
         \\
         & \nearrow&& \searrow
         \\
         X
         &&
         \longrightarrow
         &&
         Z
     }
   $$

   if two of the three morphisms are in $W$, then so is the third.

=--

+-- {: .num_remark #SimplicialLocalizationOutlook}
###### Remark
**([[simplicial localization]])**

It turns out that a [[category with weak equivalences]], def. \ref{CategoryWithWeakEquivalences}, already determines a [[homotopy theory]]: the one given given by universally forcing weak equivalences to become actual [[homotopy equivalences]]. This may be made precise and is called the _[[simplicial localization]]_ of a category with weak equivalences ([Dwyer-Kan 80a](simplicial+localization#DwyerKanLocalizations), [Dwyer-Kan 80b](simplicial+localization#DwyerKanCalculating), [Dwyer-Kan 80c](simplicial+localization#DwyerKanFunctionComplexes)). However, without further auxiliary structure, these simplicial localizations are in general intractable. The further axioms of a [[model category]] serve the sole purpose of making the universal homotopy theory induced by a [[category with weak equivalences]] be tractable:

=--

+-- {: .num_defn #ModelCategory}
###### Definition
**([[model category]])**

A **[[model category]]** is

1. a [[category]] $\mathcal{C}$ with all [[limits]] and [[colimits]] (def. \ref{LimitsAndColimits});

1. three sub-[[classes]] $W, Fib, Cof \subset Mor(\mathcal{C})$ of its [[morphisms]];

such that

1. the class $W$ makes $\mathcal{C}$ into a **[[category with weak equivalences]]**, def. \ref{CategoryWithWeakEquivalences};

1. The pairs $(W \cap Cof\;,\; Fib)$ and $(Cap\;,\; W\cap Fib)$ are both [[weak factorization systems]], def. \ref{WeakFactorizationSystem}.

One says:

* elements in $W$ are _[[weak equivalences]]_,

* elements in $Cof$ are _[[cofibrations]]_,

* elements in $Fib$ are _[[fibrations]]_,

* elements in $W\cap Cof$ are _[[acyclic cofibrations]]_,

* elements in $W \cap Fib$ are _[[acyclic fibrations]]_.

=--

The form of def. \ref{ModelCategory} is due to ([Joyal, def. E.1.2](#Joyal)). It implies various other conditions that ([Quillen 67](model+category#Quillen67)) demands explicitly, see prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms} and prop. \ref{WeakEquivalencesAreClosedUnderRetracts} below.

We now dicuss the concept of [[weak factorization systems]] appearing in def. \ref{ModelCategory}.



### Factorization systems
 {#WeakFactorizationSystems}


+-- {: .num_defn #LiftingAndExtension}
###### Definition
**([[lift]] and [[extension]])**

Let $\mathcal{C}$ be any [[category]].
Given a [[diagram]] in $\mathcal{C}$ of the form

$$
  \array{
     X &\stackrel{f}{\longrightarrow}& Y
     \\
     {}^{\mathllap{p}}\downarrow
     \\
     B
  }
$$

then an *[[extension]]* of the [[morphism]] $f$ along the [[morphism]] $p$ is a completion to a [[commuting diagram]] of the form

$$
  \array{
     X &\stackrel{f}{\longrightarrow}& Y
     \\
     {}^{\mathllap{p}}\downarrow & \nearrow_{\mathrlap{\tilde f}}
     \\
     B
  }
  \,.
$$

Dually, given a [[diagram]] of the form

$$
  \array{
    && A
    \\
    && \downarrow^{\mathrlap{p}}
    \\
    X &\stackrel{f}{\longrightarrow}& Y
  }
$$

then a **[[lift]]** of $f$ through $p$ is a completion to a [[commuting diagram]] of the form

$$
  \array{
    && A
    \\
    &{}^{\mathllap{\tilde f}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    X &\stackrel{f}{\longrightarrow}& Y
  }
  \,.
$$

Combining these cases: given a [[commuting square]]

$$
  \array{
     X_1 &\stackrel{f_1}{\longrightarrow}& Y_1
     \\
     {}^{\mathllap{p_l}}\downarrow && \downarrow^{\mathrlap{p_r}}
     \\
     X_2 &\stackrel{f_1}{\longrightarrow}& Y_2
  }
$$

then a **[[lifting]]** in the diagram is a completion to a [[commuting diagram]] of the form

$$
  \array{
     X_1 &\stackrel{f_1}{\longrightarrow}& Y_1
     \\
     {}^{\mathllap{p_l}}\downarrow &\nearrow& \downarrow^{\mathrlap{p_r}}
     \\
     X_2 &\stackrel{f_1}{\longrightarrow}& Y_2
  }
  \,.
$$

Given a sub-[[class]] of morphisms $K \subset Mor(\mathcal{C})$, then

* a morphism $p_r$ as above is said to have the **[[right lifting property]] against $K$** or to be a **$K$-[[injective morphism]]** if in all square diagrams with $p_r$ on the right and any $p_l \in K$ on the left a lift exists.

dually:

* a morphism $p_l$ is said to have the **[[left lifting property]] against $K$** or to be a **$K$-[[projective morphism]]**  if in all square diagrams with $p_l$ on the left and any $p_r \in K$ on the left a lift exists.

=--

+-- {: .num_defn #WeakFactorizationSystem}
###### Definition

A **[[weak factorization system]]** (WFS) on a [[category]] $\mathcal{C}$ is a [[pair]] $(Proj,Inj)$ of [[classes]] of [[morphisms]] of $\mathcal{C}$ such that

1. Every [[morphism]] $f \colon X\to Y$ of $\mathcal{C}$ may be factored as the [[composition]] of a morphism in $Proj$ followed by one in $Inj$

   $$
     f\;\colon\;  X \overset{\in Proj}{\longrightarrow} Z \overset{\in Inj}{\longrightarrow} Y
     \,.
   $$

1. The classes are closed under having the [[lifting property]], def. \ref{LiftingAndExtension}, against each other:

   1. $Proj$ is precisely the class of morphisms having the [[left lifting property]] against every morphisms in $Inj$;

   1. $Inj$ is precisely the class of morphisms having the [[right lifting property]] against every morphisms in $Proj$.

=--

+-- {: .num_defn #FunctorialFactorization}
###### Definition

For $\mathcal{C}$ a [[category]], a **[[functorial factorization]]** of the morphisms in $\mathcal{C}$ is a [[functor]]

$$
  fact \;\colon\; \mathcal{C}^{\Delta[1]} \longrightarrow \mathcal{C}^{\Delta[2]}
$$

which is a [[section]] of the [[composition]] functor $d_1 \;\colon \;\mathcal{C}^{\Delta[2]}\to \mathcal{C}^{\Delta[1]}$.

=--

+-- {: .num_remark}
###### Remark

In def. \ref{FunctorialFactorization} we are using the following standard notation, see at _[[simplex category]]_ and at _[[nerve of a category]]_:

Write $[1] = \{0 \to 1\}$ and $[2] = \{0 \to 1 \to 2\}$ for the [[ordinal numbers]], regarded as [[posets]] and hence as [[categories]]. The [[arrow category]] $Arr(\mathcal{C})$ is equivalently the [[functor category]] $\mathcal{C}^{\Delta[1]} \coloneqq Funct(\Delta[1], \mathcal{C})$, while $\mathcal{C}^{\Delta[2]}\coloneqq Funct(\Delta[2], \mathcal{C})$ has as objects pairs of composable morphisms in $\mathcal{C}$. There are three injective functors $\delta_i \colon [1] \rightarrow [2]$, where $\delta_i$ omits the index $i$ in its image.
By precomposition, this induces [[functors]] $d_i  \colon \mathcal{C}^{\Delta[2]} \longrightarrow \mathcal{C}^{\Delta[1]}$. Here

* $d_1$ sends a pair of composable morphisms to their [[composition]];

* $d_2$ sends a pair of composable morphisms to the first morphisms;

* $d_0$ sends a pair of composable morphisms to the second morphisms.

=--

+-- {: .num_defn #FunctorialWeakFactorizationSystem}
###### Definition

A [[weak factorization system]], def. \ref{WeakFactorizationSystem}, is called a **functorial weak factorization system** if the factorization of morphisms may be chosen to be a [[functorial factorization]] $fact$, def. \ref{FunctorialFactorization}, i.e. such that $d_2 \circ fact$ lands in $Proj$ and $d_0\circ fact$ in $Inj$.

=--

+-- {: .num_remark}
###### Remark

Not all weak factorization systems are functorial, def. \ref{FunctorialWeakFactorizationSystem}, although most (including those produced by the [[small object argument]] (prop. \ref{SmallObjectArgument} below), with due care) are.

=--


+-- {: .num_prop #ClosurePropertiesOfInjectiveAndProjectiveMorphisms}
###### Proposition

Let $\mathcal{C}$ be a [[category]] and let $K\subset Mor(\mathcal{C})$ be a [[class]] of [[morphisms]]. Write $K Proj$ and $K Inj$, respectively, for the sub-classes of $K$-[[projective morphisms]] and of $K$-[[injective morphisms]], def. \ref{LiftingAndExtension}. Then:

1. Both classes contain the class of [[isomorphism]] of $\mathcal{C}$.

1. Both classes are closed under [[composition]] in $\mathcal{C}$.

   $K Proj$ is also closed under [[transfinite composition]].

1. Both classes are closed under forming [[retracts]] in the [[arrow category]] $\mathcal{C}^{\Delta[1]}$ (see remark \ref{RetractsOfMorphisms}).

1. $K Proj$ is closed under forming [[pushouts]] of morphisms in $\mathcal{C}$ ("[[cobase change]]").

   $K Inj$ is closed under forming [[pullback]] of morphisms in $\mathcal{C}$ ("[[base change]]").

1. $K Proj$ is closed under forming [[coproducts]] in $\mathcal{C}^{\Delta[1]}$.

   $K Inj$ is closed under forming [[products]] in $\mathcal{C}^{\Delta[1]}$.

=--

+-- {: .proof}
###### Proof

We go through each item in turn.

**containing isomorphisms**

Given a [[commuting square]]

$$
  \array{
    A &\overset{f}{\rightarrow}& X
    \\
    {}_{\mathllap{\in Iso}}^{\mathllap{i}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    B &\underset{g}{\longrightarrow}& Y
  }
$$

with the left morphism an isomorphism, then a [[lift]] is given by using the [[inverse]] of this isomorphism ${}^{{f \circ i^{-1}}}\nearrow$. Hence in particular there is a lift when $p \in K$ and so $i \in K Proj$. The other case is [[formal dual|formally dual]].

**closure under composition**

Given a [[commuting square]] of the form

$$
  \array{
    A &\longrightarrow& X
    \\
    \downarrow && \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in K Inj}}
    \\
    {}^{\mathllap{i}}_{\mathllap{\in K}}\downarrow && \downarrow^{\mathrlap{p_2}}_{\mathrlap{\in K Inj}}
    \\
    B &\longrightarrow& Y
  }
$$

consider its [[pasting]] decomposition as

$$
  \array{
    A &\longrightarrow& X
    \\
    \downarrow
    &\searrow& \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in K Inj}}
    \\
    {}^{\mathllap{i}}_{\mathllap{\in K}}\downarrow && \downarrow^{\mathrlap{p_2}}_{\mathrlap{\in K Inj}}
    \\
    B &\longrightarrow& Y
  }
  \,.
$$

Now the bottom commuting square has a lift, by assumption. This yields another [[pasting]] decomposition

$$
  \array{
    A &\longrightarrow& X
    \\
    {}^{\mathllap{i}}_{\mathllap{\in K}}\downarrow
    && \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in K Inj}}
    \\
    \downarrow &\nearrow& \downarrow^{\mathrlap{p_2}}_{\mathrlap{\in K Inj}}
    \\
    B &\longrightarrow& Y
  }
$$

and now the top commuting square has a lift by assumption. This is now equivalently a lift in the total diagram, showing that $p_1\circ p_1$ has the right lifting property against $K$ and is hence in $K Inj$. The case of composing two morphisms in $K Proj$  is [[formal dual|formally dual]]. From this the closure of $K Proj$ under [[transfinite composition]] follows since the latter is given by [[colimits]] of sequential composition and successive lifts against the underlying sequence as above constitutes a [[cocone]], whence the extension of the lift to the colimit follows by its [[universal property]].

**closure under retracts**

Let $j$ be the [[retract]] of an $i \in K Proj$, i.e. let there be a [[commuting diagram]] of the form.

$$
  \array{
    id_A \colon & A &\longrightarrow& C &\longrightarrow& A
    \\
    & \downarrow^{\mathrlap{j}} && \downarrow^{\mathrlap{i}}_{\mathrlap{\in K Proj}} && \downarrow^{\mathrlap{j}}
    \\
    id_B \colon & B &\longrightarrow& D &\longrightarrow& B
  }
  \,.
$$

Then for

$$
  \array{
     A &\longrightarrow& X
     \\
     {}^{\mathllap{j}}\downarrow && \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
     \\
     B &\longrightarrow& Y
  }
$$

a [[commuting square]], it is equivalent to its [[pasting]] composite with that retract diagram

$$
  \array{
    A &\longrightarrow& C &\longrightarrow& A &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{j}} && \downarrow^{\mathrlap{i}}_{\mathrlap{\in K Proj}} && \downarrow^{\mathrlap{j}} && \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    B &\longrightarrow& D &\longrightarrow& B &\longrightarrow & Y
  }
  \,.
$$

Here the pasting composite of the two squares on the right has a lift, by assumption:

$$
  \array{
    A &\longrightarrow& C &\longrightarrow& A &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{j}}
      &&
    \downarrow^{\mathrlap{i}}_{}
      &&
    \nearrow
      &&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    B &\longrightarrow& D &\longrightarrow& B &\longrightarrow & Y
  }
  \,.
$$

By composition, this is also a lift in the total outer rectangle, hence in the original square. Hence $j$ has the left lifting property against all $p \in K$ and hence is in $K Proj$. The other case is [[formal duality|formally dual]].



**closure under pushout and pullback**

Let $p \in K Inj$ and and let

$$
  \array{
    Z \times_f X &\longrightarrow& X
    \\
    {}^{\mathllap{{f^* p}}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    Z &\stackrel{f}{\longrightarrow} & Y
  }
$$

be a [[pullback]] diagram in $\mathcal{C}$. We need to show that $f^* p$ has the [[right lifting property]] with respect to all $i \in K$. So let

$$
  \array{
     A &\longrightarrow& Z \times_f X
     \\
     {}^{\mathllap{i}}_{\mathllap{\in K}}\downarrow && \downarrow^{\mathrlap{\mathrlap{f^* p}}}
     \\
     B &\stackrel{g}{\longrightarrow}& Z
  }
$$

be a [[commuting square]]. We need to construct a diagonal lift of that square. To that end, first consider the [[pasting]] composite with the pullback square from above to obtain the commuting diagram

$$
  \array{
     A &\longrightarrow& Z \times_f X &\longrightarrow& X
     \\
     {}^{\mathllap{i}}\downarrow && \downarrow^{\mathrlap{f^* p}}
     && \downarrow^{\mathrlap{p}}
     \\
     B &\stackrel{g}{\longrightarrow}& Z &\stackrel{f}{\longrightarrow}& Y
  }
  \,.
$$

By the right lifting property of $p$, there is a diagonal lift of the total outer diagram

$$
  \array{
    A &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{i}} &{}^{\hat {(f g)}}\nearrow&  \downarrow^{\mathrlap{p}}
    \\
    B &\stackrel{f g}{\longrightarrow}& Y
  }
  \,.
$$

By the [[universal property]] of the [[pullback]] this gives rise to the lift $\hat g$ in

$$
  \array{
     && Z \times_f X &\longrightarrow& X
     \\
     &{}^{\hat g} \nearrow& \downarrow^{\mathrlap{f^* p}}
     && \downarrow^{\mathrlap{p}}
     \\
     B &\stackrel{g}{\longrightarrow}& Z &\stackrel{f}{\longrightarrow}& Y
  }
  \,.
$$

In order for $\hat g$ to qualify as the intended lift of the total diagram, it remains to show that

$$
  \array{
     A &\longrightarrow& Z \times_f X
     \\
     \downarrow^{\mathrlap{i}} & {}^{\hat g}\nearrow
     \\
     B
  }
$$

commutes. To do so we notice that we obtain two [[cones]] with tip $A$:

* one is given by the morphisms
  1. $A \to Z \times_f X \to X$
  2. $A \stackrel{i}{\to} B \stackrel{g}{\to} Z$

  with universal morphism into the pullback being

  * $A \to Z \times_f X$

* the other by
  1. $A \stackrel{i}{\to} B \stackrel{\hat g}{\to} Z \times_f X \to X$
  2. $A \stackrel{i}{\to} B \stackrel{g}{\to} Z$.

  with universal morphism into the pullback being

  * $A \stackrel{i}{\to} B \stackrel{\hat g}{\to} Z \times_f X$.

The commutativity of the diagrams that we have established so far shows that the first and second morphisms here equal each other, respectively. By the fact that the universal morphism into a pullback diagram is _unique_ this implies the required identity of morphisms.

The other case is [[formal dual|formally dual]].

**closure under (co-)products**

Let $\{(A_s \overset{i_s}{\to} B_s) \in K Proj\}_{s \in S}$ be a set of elements of $K Proj$. Since [[colimits]] in the [[presheaf category]] $\mathcal{C}^{\Delta[1]}$ are computed componentwise, their [[coproduct]] in this [[arrow category]] is the universal morphism out of the coproduct of objects $\underset{s \in S}{\coprod} A_s$ induced via its [[universal property]] by the set of morphisms $i_s$:

$$
  \underset{s \in S}{\sqcup} A_s
  \overset{(i_s)_{s\in S}}{\longrightarrow}
  \underset{s \in S}{\sqcup} B_s
  \,.
$$

Now let

$$
  \array{
    \underset{s \in S}{\sqcup} A_s &\longrightarrow& X
    \\
    {}^{\mathllap{(i_s)_{s\in S}}}\downarrow && \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    \underset{s \in S}{\sqcup} B_s
    &\longrightarrow&
    Y
  }
$$

be a [[commuting square]]. This is in particular a [[cocone]] under the [[coproduct]] of objects, hence by the [[universal property]] of the coproduct, this is equivalent to a set of commuting diagrams

$$
  \left\{
  \;\;\;\;\;\;\;\;\;
  \array{
    A_s &\longrightarrow& X
    \\
    {}^{\mathllap{i_s}}_{\mathllap{\in K Proj}}\downarrow
      &&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    B_s
    &\longrightarrow&
    Y
  }
  \;\;\;\;
  \right\}_{s\in S}
  \,.
$$

By assumption, each of these has a lift $\ell_s$. The collection of these lifts

$$
  \left\{
  \;\;\;\;\;\;\;\;\;
  \array{
    A_s &\longrightarrow& X
    \\
    {}^{\mathllap{i_s}}_{\mathllap{\in Proj}}\downarrow
      &{}^{\ell_s}\nearrow& \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    B_s
    &\longrightarrow&
    Y
  }
  \;\;\;\;
  \right\}_{s\in S}
$$

is now itself a compatible [[cocone]], and so once more by the [[universal property]] of the coproduct, this is equivalent to a lift $(\ell_s)_{s\in S}$ in the original square

$$
  \array{
    \underset{s \in S}{\sqcup} A_s &\longrightarrow& X
    \\
    {}^{\mathllap{(i_s)_{s\in S}}}\downarrow
     &{}^{(\ell_s)_{s\in S}}\nearrow&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    \underset{s \in S}{\sqcup} B_s
    &\longrightarrow&
    Y
  }
  \,.
$$

This shows that the coproduct of the $i_s$ has the left lifting property against all $f\in K$ and is hence in $K Proj$. The other case is [[formal dual|formally dual]].



=--

An immediate consequence of prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms} is this:

+-- {: .num_prop #SaturationOfGeneratingCofibrations}
###### Corollary

Let $\mathcal{C}$ be a [[category]] with all small [[colimits]],
and let $K\subset Mor(\mathcal{C})$ be a sub-[[class]] of its morphisms.
Then every $K$-[[injective morphism]], def. \ref{LiftingAndExtension}, has the [[right lifting property]], def. \ref{LiftingAndExtension}, against all $K$-[[relative cell complexes]], def. \ref{TopologicalCCellComplex} and their [[retracts]], remark \ref{RetractsOfMorphisms}.

=--




+-- {: .num_remark #RetractsOfMorphisms}
###### Remark

By a [[retract]] of a [[morphism]] $X \stackrel{f}{\longrightarrow} Y$ in some [[category]] $\mathcal{C}$ we mean a retract of $f$ as an object in the [[arrow category]] $\mathcal{C}^{\Delta[1]}$, hence a morphism $A \stackrel{g}{\longrightarrow} B$ such that in $\mathcal{C}^{\Delta[1]}$ there is a factorization of the identity on $g$ through $f$

$$
  id_g \;\colon\;
  g \longrightarrow f \longrightarrow g
  \,.
$$

This means equivalently that in $\mathcal{C}$ there is a [[commuting diagram]] of the form

$$
  \array{
    id_A \colon & A &\longrightarrow& X &\longrightarrow& A
    \\
    & \downarrow^{\mathrlap{g}} && \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{g}}
    \\
    id_B \colon & B &\longrightarrow& Y &\longrightarrow& B
  }
  \,.
$$

=--

+-- {: .num_lemma #RetractPreservesIsomorphism}
###### Lemma

In every [[category]] $C$ the class of [[isomorphisms]] is preserved under retracts in the sense of remark \ref{RetractsOfMorphisms}.

=--


+-- {: .proof}
###### Proof

For

$$
  \array{
    id_A \colon & A &\longrightarrow& X &\longrightarrow& A
    \\
    & \downarrow^{\mathrlap{g}} && \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{g}}
    \\
    id_B \colon & B &\longrightarrow& Y &\longrightarrow& B
  }
  \,.
$$

a retract diagram and $X \overset{f}{\to} Y$ an isomorphism, the inverse to $A \overset{g}{\to} B$ is given by the composite

$$
  \array{
    &  & & X & \longrightarrow & A
    \\
    & && \uparrow^{\mathrlap{f^{-1}}} &&
    \\
    & B & \longrightarrow& Y&&
  }
  \,.
$$

=--

More generally:


+-- {: .num_prop #WeakEquivalencesAreClosedUnderRetracts}
###### Proposition

Given a [[model category]] in the sense of def. \ref{ModelCategory}, then its class of weak equivalences is closed under forming [[retracts]] (in the [[arrow category]], see remark \ref{RetractsOfMorphisms}).

=--

([Joyal, prop. E.1.3](#Joyal))


+-- {: .proof}
###### Proof

Let

$$
  \array{
    id \colon & A &\longrightarrow& X &\longrightarrow& A
    \\
    &
    {}^{\mathllap{f}}
    \downarrow
      &&
    \downarrow^{\mathrlap{w}}
      &&
    \downarrow^{\mathrlap{f}}
    \\
    id \colon & B &\longrightarrow& Y &\longrightarrow& B
  }
$$

be a [[commuting diagram]] in the given model category, with $w \in W$ a weak equivalence. We need to show that then also $f \in W$.

First consider the case that $f \in Fib$.

In this case, factor $w$ as a cofibration followed by an acyclic fibration. Since $w \in W$ and by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) this is even a factorization through an acyclic cofibration followed by an acyclic fibration. Hence we obtain a commuting diagram of the following form:

$$
  \array{
    id \colon
    &
    A
      &\longrightarrow&
    X
      &\overset{\phantom{AAAA}}{\longrightarrow}& A
    \\
    &
    {}^{\mathllap{id}}\downarrow
      &&
    \downarrow^{\mathrlap{\in W \cap Cof}}
      &&
    \downarrow^{\mathrlap{id}}
    \\
    id \colon
    & A' &\overset{s}{\longrightarrow}&
     X'
     &\overset{\phantom{AA}t\phantom{AA}}{\longrightarrow}& A'
    \\
    &
    {}^{\mathllap{f}}_{\mathllap{\in Fib}}
    \downarrow
      &&
    \downarrow^{\mathrlap{\in W \cap Fib}}
      &&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in Fib}}
    \\
    id \colon & B &\longrightarrow& Y &\underset{\phantom{AAAA}}{\longrightarrow}& B
  }
  \,,
$$

where $s$ is uniquely defined and where $t$ is any lift of the top middle vertical acyclic cofibration against $f$. This now exhibits $f$ as a retract of an acyclic fibration. These are closed under retract by prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}.

Now consider the general case. Factor $f$ as an acyclic cofibration followed by a fibration and form the [[pushout]] in the top left square of the following diagram

$$
  \array{
    id \colon
    &
    A
      &\longrightarrow&
    X
      &\overset{\phantom{AAAA}}{\longrightarrow}& A
    \\
    &
    {}^{\mathllap{\in W \cap Cof}}\downarrow
      &(po)&
    \downarrow^{\mathrlap{\in W \cap Cof}}
      &&
    \downarrow^{\mathrlap{\in W \cap Cof}}
    \\
    id \colon
    & A' &\overset{}{\longrightarrow}&
     X'
     &\overset{\phantom{AA}\phantom{AA}}{\longrightarrow}& A'
    \\
    &
    {}^{\mathllap{\in Fib}}
    \downarrow
      &&
    \downarrow^{\mathrlap{\in W }}
      &&
    \downarrow^{\mathrlap{\in Fib}}
    \\
    id \colon & B &\longrightarrow& Y &\underset{\phantom{AAAA}}{\longrightarrow}& B
  }
  \,,
$$

where the other three squares are induced by the [[universal property]] of the pushout, as is the identification of the middle horizontal composite as the identity on $A'$. Since acyclic cofibrations are closed under forming pushouts by prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}, the top middle vertical morphism is now an acyclic fibration, and hence by assumption and by [[two-out-of-three]] so is the middle bottom vertical morphism.

Thus the previous case now gives that the bottom left vertical morphism is a weak equivalence, and hence the total left vertical composite is.


=--



+-- {: .num_lemma #RetractArgument}
###### Lemma
**([[retract argument]])**

Consider a [[composition|composite]] morphism

$$
  f \;\colon\;
  X \stackrel{i}{\longrightarrow} A \stackrel{p}{\longrightarrow} Y
  \,.
$$

1. If $f$ has the [[left lifting property]] against $p$, then $f$ is a [[retract]] of $i$.

1. If $f$ has the [[right lifting property]] against $i$, then $f$ is a [[retract]] of $p$.

=--

+-- {: .proof}
###### Proof

We discuss the first statement, the second is [[formal duality|formally dual]].

Write the factorization of $f$ as a [[commuting square]] of the form

$$
  \array{
    X &\stackrel{i}{\longrightarrow}& A
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    Y &= & Y
  }
  \,.
$$

By the assumed [[lifting property]] of $f$ against $p$ there exists a diagonal filler $g$ making a [[commuting diagram]] of the form

$$
  \array{
    X &\stackrel{i}{\longrightarrow}& A
    \\
    {}^{\mathllap{f}}\downarrow &{}^{\mathllap{g}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    Y &= & Y
  }
  \,.
$$

By rearranging this diagram a little, it is equivalent to

$$
  \array{
    & X &=& X
    \\
    & {}^{\mathllap{f}}\downarrow
     &&
    {}^{\mathllap{i}}\downarrow
    \\
    id_Y \colon & Y &\underset{g}{\longrightarrow}& A &\underset{p}{\longrightarrow}&
    Y
  }
  \,.
$$

Completing this to the right, this yields a diagram exhibiting the required retract according to remark \ref{RetractsOfMorphisms}:

$$
  \array{
    id_X \colon & X &=& X &=& X
    \\
    & {}^{\mathllap{f}}\downarrow
     &&
    {}^{\mathllap{i}}\downarrow
     &&
     {}^{\mathllap{f}}\downarrow
    \\
    id_Y \colon & Y &\underset{g}{\longrightarrow}& A &\underset{p}{\longrightarrow}&
    Y
  }
  \,.
$$

=--



**Small object argument**

Given a set $C \subset Mor(\mathcal{C})$ of morphisms in some [[category]] $\mathcal{C}$, a natural question is how to factor any given morphism $f\colon X \longrightarrow Y$ through a relative $C$-cell complex, def. \ref{TopologicalCCellComplex}, followed by a $C$-[[injective morphism]], def. \ref{RightLiftingProperty}

$$
  f
    \;\colon\;
  X
    \stackrel{\in C cell}{\longrightarrow}
  \hat X
    \stackrel{\in C inj}{\longrightarrow}
  Y
  \,.
$$

A first approximation to such a factorization turns out to be given simply by forming $\hat X = X_1$ by attaching **all** possible $C$-cells to $X$. Namely let

$$
  (C/f)
   \coloneqq
  \left\{
    \array{
       dom(c) &\stackrel{}{\longrightarrow}& X
       \\
       {}^{\mathllap{c\in C}}\downarrow && \downarrow^{\mathrlap{f}}
       \\
       cod(c) &\longrightarrow& Y
    }
  \right\}
$$

be the set of **all** ways to find a $C$-cell attachment in $f$, and consider the [[pushout]] $\hat X$ of the [[coproduct]] of morphisms in $C$ over all these:

$$
  \array{
    \underset{c\in(C/f)}{\coprod} dom(c) &\longrightarrow& X
    \\
    {}^{\mathllap{\underset{c\in(C/f)}{\coprod} c}}\downarrow
    &(po)&
    \downarrow^{\mathrlap{}}
    \\
    \underset{c\in(C/f)}{\coprod} cod(c)
    &\longrightarrow&
    X_1
  }
  \,.
$$

This gets already close to producing the intended factorization:

First of all the resulting map $X \to X_1$ is a $C$-relative cell complex, by construction.

Second, by the fact that the coproduct is over all commuting squres to $f$, the morphism $f$ itself makes a [[commuting diagram]]

$$
  \array{
    \underset{c\in(C/f)}{\coprod} dom(c) &\longrightarrow& X
    \\
    {}^{\mathllap{\underset{c\in(C/f)}{\coprod} c}}\downarrow
    &&
    \downarrow^{\mathrlap{f}}
    \\
    \underset{c\in(C/f)}{\coprod} cod(c)
    &\longrightarrow&
    Y
  }
$$

and hence the [[universal property]] of the [[colimit]] means that $f$ is indeed factored through that $C$-cell complex $X_1$; we may suggestively arrange that factorizing diagram like so:

$$
  \array{
    \underset{c\in(C/f)}{\coprod} dom(c)
      &\longrightarrow&
    X
    \\
    {}^{\mathllap{id}}\downarrow
    &&
    \downarrow^{\mathrlap{}}
    \\
    \underset{c\in(C/f)}{\coprod} dom(c)
     &&
    X_1
    \\
    {}^{\mathllap{\underset{c\in(C/f)}{\coprod} c}}\downarrow
    &\nearrow& \downarrow
    \\
    \underset{c\in(C/f)}{\coprod} cod(c)
    &\longrightarrow&
    Y
  }
  \,.
$$

This shows that, finally, the colimiting [[co-cone]] map -- the one that now appears diagonally -- **almost** exhibits the desired right lifting of $X_1 \to Y$ against the $c\in C$. The failure of that to hold on the nose is only the fact that a horizontal map in the middle of the above diagram is missing: the diagonal map obtained above lifts not all commuting diagrams of $c\in C$ into $f$, but only those where the top morphism $dom(c) \to X_1$ factors through $X \to X_1$.

The idea of the [[small object argument]] now is to fix this only remaining problem by iterating the construction: next factor $X_1 \to Y$ in the same way into

$$
  X_1 \longrightarrow X_2 \longrightarrow Y
$$

and so forth. Since relative $C$-cell complexes are closed under composition, at stage $n$ the resulting $X \longrightarrow X_n$ is still a $C$-cell complex, getting bigger and bigger. But accordingly, the failure of the accompanying $X_n \longrightarrow Y$ to be a $C$-[[injective morphism]] becomes smaller and smaller, for it now lifts against all diagrams where $dom(c) \longrightarrow X_n$ factors through $X_{n-1}\longrightarrow X_n$, which intuitively is less and less of a condition as the $X_{n-1}$ grow larger and larger.

The concept of _[[small object]]_ is just what makes this intuition precise and finishes the small object argument. For the present purpose we just need the following simple version:

+-- {: .num_defn #ClassOfMorphismsWithSmallDomains}
###### Definition

For $\mathcal{C}$ a [[category]] and $C \subset Mor(\mathcal{C})$
a sub-[[set]] of its morphisms, say that these have _small [[domains]]_
if there is an [[ordinal]] $\alpha$ (def. \ref{PosetsWosetTosetsAndOrdinals}) such that for every $c\in C$ and for every $C$-[[relative cell complex]] given by a [[transfinite composition]] (def. \ref{TransfiniteComposition})

$$
  f
  \;\colon\;
  X \to X_1 \to X_2 \to \cdots  \to X_\beta \to \cdots  \longrightarrow \hat X
$$

every morphism  $dom(c)\longrightarrow \hat X$ factors through a stage $X_\beta \to \hat X$ of order $\beta \lt \alpha$:

$$
  \array{
     && X_\beta
     \\
     & \nearrow & \downarrow
     \\
     dom(c) &\longrightarrow& \hat X
  }
  \,.
$$

=--

The above discussion proves the following:

+-- {: .num_prop #SmallObjectArgument}
###### Proposition
**(small object argument)**

Let $\mathcal{C}$ be a [[locally small category]] with all small [[colimits]]. If a [[set]] $C\subset Mor(\mathcal{C})$ of morphisms has all small domains in the sense of def. \ref{ClassOfMorphismsWithSmallDomains}, then every morphism $f\colon X\longrightarrow $ in $\mathcal{C}$ factors through a $C$-[[relative cell complex]], def. \ref{TopologicalCCellComplex}, followed by a $C$-[[injective morphism]], def. \ref{RightLiftingProperty}

$$
  f \;\colon\;
  X \stackrel{\in C cell}{\longrightarrow} \hat X \stackrel{\in C inj}{\longrightarrow}
  Y
  \,.
$$

=--

([Quillen 67, II.3 lemma](model+category#Quillen67))

### Homotopy

We discuss how the concept of [[homotopy]] is abstractly realized in [[model categories]], def. \ref{ModelCategory}.

+-- {: .num_defn #PathAndCylinderObjectsInAModelCategory}
###### Definition

Let $\mathcal{C}$ be a [[model category]], def. \ref{ModelCategory}, and $X \in \mathcal{C}$ an [[object]].

* A **[[path space object]]** $Path(X)$ for $X$ is a factorization of the [[diagonal]] $\Delta_X \;\colon\; X \to X \times X$ as

$$
  \Delta_X
  \;\colon\;
   X \underoverset{\in W}{i}{\longrightarrow} Path(X) \underoverset{\in Fib}{(p_0,p_1)}{\longrightarrow} X \times X
  \,.
$$

where $X\to Path(X)$ is a weak equivalence and $Path(X) \to X \times X$ is a fibration.

* A **[[cylinder object]]** $Cyl(X)$ for $X$ is a factorization of the [[codiagonal]] (or "fold map") $\nabla_X \;\colon\; X \sqcup X \to X$ as

$$
  \nabla_X
  \;\colon\;
  X \sqcup X \underoverset{\in Cof}{(i_0,i_1)}{\longrightarrow} Cyl(X) \underoverset{\in W}{p}{\longrightarrow} X
  \,.
$$

where $Cyl(X) \to X$ is a weak equivalence. and $X \sqcup X \to Cyl(X)$ is a cofibration.

=--

+-- {: .num_remark #RemarkOnChoicesOfNonGoodPathAndCylinderObjects}
###### Remark

For every object $X \in \mathcal{C}$ in a model category, a cylinder object and a path space object according to def. \ref{PathAndCylinderObjectsInAModelCategory} exist: the factorization axioms guarantee that there exists

1. a factorization of the [[codiagonal]] as

   $$
     \nabla_X \;\colon\; X \sqcup X \overset{\in Cof}{\longrightarrow} Cyl(X) \overset{\in W \cap Fib}{\longrightarrow} X
   $$

1. a factorization of the diagonal as

   $$
     \Delta_X
       \;\colon\;
     X
      \overset{\in W \cap Cof}{\longrightarrow}
     Path(X)
      \overset{\in Fib}{\longrightarrow}
     X \times X
     \,.
   $$

The cylinder and path space objects obtained this way are actually better than required by def. \ref{PathAndCylinderObjectsInAModelCategory}: in addition to $Cyl(X)\to X$ being just a weak equivalence, for these this is actually an acyclic fibration, and dually in addition to $X\to Path(X)$ being a weak equivalence, for these it is actually an acyclic cofibrations.

Some authors call cylinder/path-space objects with this extra property "very good" cylinder/path-space objects, respectively.

One may also consider dropping a condition in def. \ref{PathAndCylinderObjectsInAModelCategory}: what mainly matters is the weak equivalence, hence some authors take cylinder/path-space objects to be defined as in def. \ref{PathAndCylinderObjectsInAModelCategory} but without the condition that $X \sqcup X\to Cyl(X)$ is a cofibration and without the condition that $Path(X) \to X$ is a fibration. Such authors would then refer to the concept in def. \ref{PathAndCylinderObjectsInAModelCategory} as "good" cylinder/path-space objects.

The terminology in def. \ref{PathAndCylinderObjectsInAModelCategory} follows the original ([Quillen 67, I.1 def. 4](model+category#Quillen67)). With the induced concept of left/right homotopy below in def. \ref{LeftAndRightHomotopyInAModelCategory}, this admits a quick derivation of the key facts in the following, as we spell out below.

=--

+-- {: .num_lemma #ComponentMapsOfCylinderAndPathSpaceInGoodSituation}
###### Lemma

Let $\mathcal{C}$ be a [[model category]]. If $X \in \mathcal{C}$ is cofibrant, then for every [[cylinder object]] $Cyl(X)$ of $X$, def. \ref{PathAndCylinderObjectsInAModelCategory}, not only is $(i_0,i_1) \colon X \sqcup X \to X$ a cofibration, but each

$$
  i_0, i_1 \colon X \longrightarrow Cyl(X)
$$

is an acyclic cofibration separately.

Dually, if $X \in \mathcal{C}$ is fibrant, then for every [[path space object]] $Path(X)$ of $X$, def. \ref{PathAndCylinderObjectsInAModelCategory}, not only is $(p_0,p_1) \colon Path(X)\to X \times X$ a cofibration, but each

$$
  p_0, p_1 \colon Path(X) \longrightarrow X
$$

is an acyclic fibration separately.


=--

+-- {: .proof}
###### Proof

We discuss the case of the path space object. The other case is [[formal dual|formally dual]].

First, that the component maps are weak equivalences follows generally: by definition they have a [[right inverse]] $Path(X) \to X$ and so this follows by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

But if $X$ is fibrant, then also the two projection maps out of the product $X \times X \to X$ are fibrations, because they are both pullbacks of the fibration $X \to \ast$

$$
  \array{
      X\times X &\longrightarrow& X
      \\
      \downarrow &(pb)& \downarrow
      \\
      X &\longrightarrow& \ast
  }
  \,.
$$

hence $p_i \colon Path(X)\to X \times X \to X$ is the composite of two fibrations, and hence itself a fibration, by prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}.

=--



Path space objects are very non-unique as objects up to isomorphism:

+-- {: .num_example #ComposedPathSpaceObjects}
###### Example

If $X \in \mathcal{C}$ is a fibrant object in a [[model category]], def. \ref{ModelCategory}, and for $Path_1(X)$ and $Path_2(X)$ two [[path space objects]] for $X$, def. \ref{PathAndCylinderObjectsInAModelCategory}, then the [[fiber product]] $Path_1(X) \times_X Path_2(X)$ is another path space object for $X$: the pullback square

$$
  \array{
     X &\overset{\Delta_X}{\longrightarrow}&  X \times X
     \\
     \downarrow && \downarrow
     \\
     Path_1(X) \underset{X}{\times} Path_2(X)
     &\longrightarrow&
     Path_1(X)\times Path_2(X)
     \\
     {}^{\mathllap{\in Fib}}\downarrow
     &(pb)&
     \downarrow^{\mathrlap{\in Fib}}
     \\
     X \times X \times X
     &\overset{(id,\Delta_X,id)}{\longrightarrow}& X \times X\times X \times X
     \\
     \downarrow^{\mathrlap{(pr_1,pr_3)}}_{\mathrlap{\in Fib}}
     &&
     \downarrow^{\mathrlap{(p_1, p_4)}}
     \\
     X\times X &=& X \times X
  }
$$

gives that the induced projection is again a fibration. Moreover, using lemma \ref{ComponentMapsOfCylinderAndPathSpaceInGoodSituation} and [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) gives that $X \to Path_1(X) \times_X Path_2(X)$ is a weak equivalence.

For the case of the canonical topological path space objects of def \ref{TopologicalPathSpace}, with $Path_1(X) = Path_2(X) = X^I = X^{[0,1]}$  then this new path space object is $X^{I \vee I} = X^{[0,2]}$, the [[mapping space]] out of the standard interval of length 2 instead of length 1.


=--



+-- {: .num_defn #LeftAndRightHomotopyInAModelCategory}
###### Definition
**(abstract [[left homotopy]] and abstract [[right homotopy]]

Let $f,g \colon X \longrightarrow Y$ be two [[parallel morphisms]] in a [[model category]].

* A **left homotopy** $\eta \colon f \Rightarrow_L g$ is a morphism $\eta \colon Cyl(X) \longrightarrow Y$ from a [[cylinder object]] of $X$,  def. \ref{PathAndCylinderObjectsInAModelCategory}, such that it makes this [[commuting diagram|diagram commute]]:

$$
  \array{
    X &\longrightarrow& Cyl(X) &\longleftarrow& X
    \\
    & {}_{\mathllap{f}}\searrow &\downarrow^{\mathrlap{\eta}}& \swarrow_{\mathrlap{g}}
    \\
    &&
    Y
  }
  \,.
$$

* A **right homotopy** $\eta \colon f \Rightarrow_R g$ is a morphism $\eta \colon X \to Path(Y)$ to some [[path space object]] of $X$, def. \ref{PathAndCylinderObjectsInAModelCategory}, such that this [[commuting diagram|diagram commutes]]:

$$
  \array{
    && X
    \\
    & {}^{\mathllap{f}}\swarrow & \downarrow^{\mathrlap{\eta}} & \searrow^{\mathrlap{g}}
    \\
    Y &\longleftarrow& Path(Y) &\longrightarrow& Y
  }
  \,.
$$

=--



+-- {: .num_lemma #LeftHomotopyWithCofibrantDomainImpliesRightHomotopyAndDually}
###### Lemma

Let $f,g \colon X \to Y$ be two [[parallel morphisms]] in a [[model category]].

1. Let $X$ be cofibrant. If there is a [[left homotopy]] $f \Rightarrow_L g$ then there is also a [[right homotopy]] $f \Rightarrow_R g$ (def. \ref{LeftAndRightHomotopyInAModelCategory}) with respect to any chosen path space object.

1. Let $X$ be fibrant. If there is a [[right homotopy]] $f \Rightarrow_R g$ then there is also a [[left homotopy]] $f \Rightarrow_L g$ with respect to any chosen cylinder object.

In particular if $X$ is cofibrant and $Y$ is fibrant, then by going back and forth it follows that every left homotopy is exhibited by every cylinder object, and every right homotopy is exhibited by every path space object.

=--

+-- {: .proof}
###### Proof

We discuss the first case, the second is [[formal dual|formally dual]].
Let $\eta \colon Cyl(X) \longrightarrow Y$ be the given left homotopy. Lemma \ref{ComponentMapsOfCylinderAndPathSpaceInGoodSituation} implies that we have a lift $h$ in the following [[commuting diagram]]

$$
  \array{
    X &\overset{i \circ f}{\longrightarrow}& Path(Y)
    \\
    {}^{\mathllap{i_0}}_{\mathllap{\in W \cap Cof}}\downarrow
    &{}^{\mathllap{h}}\nearrow&
    \downarrow^{\mathrlap{p_0,p_1}}_{\mathrlap{\in Fib}}
    \\
    Cyl(X)
    &\underset{(f \circ p,\eta)}{\longrightarrow}& Y \times Y
  }
  \,,
$$

where on the right we have the chosen path space object. Now the composite $\tilde \eta \coloneqq h \circ i_1$ is a right homotopy as required:

$$
  \array{
    && && Path(Y)
    \\
    && &{}^{\mathllap{h}}\nearrow&
    \downarrow^{\mathrlap{p_0,p_1}}_{\mathrlap{\in Fib}}
    \\
    X &\overset{i_1}{\longrightarrow}& Cyl(X)
    &\underset{(f \circ p,\eta)}{\longrightarrow}&
    Y \times Y
  }
  \,.
$$

=--


+-- {: .num_prop #BetweenCofibFibLeftAndRightHomotopyAreEquivalentEquivalenceRelations}
###### Proposition

For $X$ a cofibrant object in a [[model category]] and $Y$ a [[fibrant object]], then the [[relations]] of [[left homotopy]] $f \Rightarrow_L g$ and of [[right homotopy]] $f \Rightarrow_R g$ (def. \ref{LeftAndRightHomotopyInAModelCategory}) on the [[hom set]] $Hom(X,Y)$ coincide and are both [[equivalence relations]].

=--


+-- {: .proof}
###### Proof

That both relations coincide under the (co-)fibrancy assumption follows directly from lemma \ref{LeftHomotopyWithCofibrantDomainImpliesRightHomotopyAndDually}.

The [[symmetric relation|symmetry]] and [[reflexive relation|reflexivity]] of the relation is obvious.

That right homotopy (hence also left homotopy) with domain $X$ is a [[transitive relation]] follows from using example \ref{ComposedPathSpaceObjects} to compose path space objects.


=--



### The homotopy category
 {#TheHomotopyCategory}

We discuss the construction that takes a [[model category]], def. \ref{ModelCategory}, and then universally forces all its [[weak equivalences]] into actual [[isomorphisms]].

+-- {: .num_defn #HomotopyCategoryOfAModelCategory}
###### Definition

Let $\mathcal{C}$ be a [[model category]], def. \ref{ModelCategory}. Write $Ho(\mathcal{C})$ for the [[category]] whose

* [[objects]] are those objects of $\mathcal{C}$ which are both fibrant and cofibrant;

* [[morphisms]] are the [[homotopy classes]] of morphisms of $\mathcal{C}$, hence the [[equivalence classes]] of morphism under the equivalence relation of prop. \ref{BetweenCofibFibLeftAndRightHomotopyAreEquivalentEquivalenceRelations};

and whose [[composition]] operation is given on representatives by composition in $\mathcal{C}$.

This is, up to [[equivalence of categories]], the **[[homotopy category of a model category|homotopy category of the model category]]** $\mathcal{C}$.

=--

+-- {: .num_prop}
###### Proposition

Def. \ref{HomotopyCategoryOfAModelCategory} is well defined, in that composition of morphisms between fibrant-cofibrant objects in $\mathcal{C}$ indeed passes to [[homotopy classes]].

=--

+-- {: .proof}
###### Proof

Fix any morphism $X \overset{f}{\to} Y$ between fibrant-cofibrant objects. Then for precomposition

$$
 (-) \circ [f] \;\colon\; Hom_{Ho(\mathcal{C})}(Y,Z) \to Hom_{Ho(\mathcal{C}(X,Z))}
$$

to be well defined, we need that with $(g\sim h)\;\colon\; Y \to Z$ also $(f g \sim f h)\;\colon\; X \to Z$. But by prop \ref{BetweenCofibFibLeftAndRightHomotopyAreEquivalentEquivalenceRelations} we may take the homotopy $\sim$ to be exhibited by a right homotopy $\eta \colon Y \to Path(Z)$, for which case the statement is evident from this diagram:

$$
  \array{
    && && Z
    \\
    && & {}^{\mathllap{g}}\nearrow & \uparrow^{\mathrlap{p_1}}
    \\
    X
      &\overset{f}{\longrightarrow} &
    Y
      &\overset{\eta}{\longrightarrow}&
    Path(Z)
    \\
    && & {}_{\mathllap{h}}\searrow & \downarrow_{\mathrlap{p_0}}
    \\
    && && Z
  }
  \,.
$$

For postcomposition we may choose to exhibit homotopy by left homotopy and argue [[formal dual|dually]].

=--

We now spell out that def. \ref{HomotopyCategoryOfAModelCategory} indeed satisfies the [[universal property]] that defines the [[localization]] of a [[category with weak equivalences]] at its weak equivalences.

+-- {: .num_lemma #WhiteheadTheoremInModelCategories}
###### Lemma
**([[Whitehead theorem]] in [[model categories]])**

Let $\mathcal{C}$ be a [[model category]]. A [[weak equivalence]] between two objects which are both [[fibrant object|fibrant]] and [[cofibrant object|cofibrant]] is a [[homotopy equivalence]] (eq:HomotopyEquivalenceCondition).

=--

+-- {: .proof}
###### Proof

By the factorization axioms in the model category $\mathcal{C}$ and by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}), every weak equivalence $f\colon X \longrightarrow Y$ factors through an object $Z$ as an acyclic cofibration followed by an acyclic fibration. In particular it follows that with $X$ and $Y$ both fibrant and cofibrant, so is $Z$, and hence it is sufficient to prove that acyclic (co-)fibrations between such objects are homotopy equivalences.

So let $f \colon X \longrightarrow Y$ be an acyclic fibration between fibrant-cofibrant objects, the case of acyclic cofibrations is [[formal dual|formally dual]]. Then in fact it has a genuine [[right inverse]] given by a lift $f^{-1}$ in the diagram

$$
  \array{
    \emptyset &\rightarrow& X
    \\
    {}^{\mathllap{\in cof}}\downarrow
     &{}^{{f^{-1}}}\nearrow&
   \downarrow^{\mathrlap{f}}_{\mathrlap{\in Fib \cap W}}
    \\
    X &=& X
  }
  \,.
$$

To see that $f^{-1}$ is also a [[left inverse]] up to [[left homotopy]], let $Cyl(X)$ be any [[cylinder object]] on $X$ (def. \ref{PathAndCylinderObjectsInAModelCategory}), hence a factorization of the [[codiagonal]] on $X$ as a cofibration followed by a an acyclic fibration

$$
  X \sqcup X \stackrel{\iota_X}{\longrightarrow} Cyl(X) \stackrel{p}{\longrightarrow} X
$$

and consider the [[commuting square]]

$$
  \array{
    X \sqcup X
    &\stackrel{(f^{-1}\circ f, id)}{\longrightarrow}& X
    \\
    {}^{\mathllap{\iota_X}}{}_{\mathllap{\in Cof}}\downarrow && \downarrow^{\mathrlap{f}}_{\mathrlap{\in W \cap Fib}}
    \\
    Cyl(X) &\underset{f\circ p}{\longrightarrow}& Y
  }
  \,,
$$

which [[commuting square|commutes]] due to $f^{-1}$ being a genuine right inverse of $f$. By construction, this [[commuting square]] now admits a [[lift]] $\eta$, and that constitutes a [[left homotopy]] $\eta \colon f^{-1}\circ f \Rightarrow_L id$.

=--

+-- {: .num_defn #FibrantCofibrantReplacementFunctorToHomotopyCategory}
###### Definition
**([[fibrant resolution]] and [[cofibrant resolution]])**

Given a [[model category]] $\mathcal{C}$, consider a _choice_ for each object $X \in \mathcal{C}$ of

1. a factorization $\emptyset \underoverset{\in Cof}{i_X}{\longrightarrow} Q X \underoverset{\in W \cap Fib}{p_X}{\longrightarrow} X$ of the [[initial object|initial morphism]], such that when $X$ is already cofibrant then $p_X = id_X$;

1. a factorization $X \underoverset{\in W \cap Cof}{j_X}{\longrightarrow} P X \underoverset{\in Fib}{q_X}{\longrightarrow} \ast$ of the [[terminal object|terminal morphism]], such that when $X$ is already fibrant then $j_X = id_X$.

Write then

$$
  \gamma_{P,Q}
  \;\colon\;
  \mathcal{C}
   \longrightarrow
  Ho(\mathcal{C})
$$

for the [[functor]] to the homotopy category, def. \ref{HomotopyCategoryOfAModelCategory}, which sends an object $X$ to the object $P Q X$ and sends a morphism $f \colon X \longrightarrow Y$ to the [[homotopy class]] of the result of first lifting in

$$
  \array{
    \emptyset &\longrightarrow& Q Y
    \\
    {}^{\mathllap{i_X}}\downarrow &{}^{Q f}\nearrow& \downarrow^{\mathrlap{p_Y}}
    \\
    Q X &\underset{f\circ p_X}{\longrightarrow}& Y
  }
$$

and then lifting (here: [[extension|extending]]) in

$$
  \array{
    Q X &\overset{j_{Q Y} \circ Q f}{\longrightarrow}& P Q Y
    \\
    {}^{\mathllap{j_{Q X}}}\downarrow &{}^{P Q f}\nearrow& \downarrow^{\mathrlap{q_{Q Y}}}
    \\
    P Q X
    &\longrightarrow&
    \ast
  }
  \,.
$$

=--

+-- {: .num_lemma #ConstructionOfLocalizationFunctorForModelCategoryIsWellDefined}
###### Lemma

The construction in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory} is indeed well defined.

=--

+-- {: .proof}
###### Proof

First of all, the object $P Q X$ is indeed both fibrant and cofibrant (as well as related by a [[zig-zag]] of weak equivalences to $X$):

$$
  \array{
     \emptyset
     \\
     {}^{\mathllap{\in Cof}}\downarrow & \searrow^{\mathrlap{\in Cof}}
     \\
     Q X &\underset{\in W \cap Cof}{\longrightarrow}& P Q X &\underset{\in Fib}{\longrightarrow}& \ast
     \\
     {}^{\mathllap{\in W}}\downarrow
     \\
     X
  }
  \,.
$$

Now to see that the image on morphisms is well defined. First observe that any two choices $(Q f)_{i}$ of the first lift in the definition are left homotopic to each other, exhibited by lifting in

$$
  \array{
    Q X \sqcup Q X &\stackrel{((Q f)_1, (Q f)_2 )}{\longrightarrow}& Q Y
    \\
    {}^{\mathllap{\in Cof}}\downarrow
     &&
    \downarrow^{\mathrlap{p_{Y}}}_{\mathrlap{\in W \cap Fib}}
    \\
    Cyl(Q X)
    &\underset{f \circ p_{X} \circ \sigma_{Q X}}{\longrightarrow}&
    Y
  }
  \,.
$$

Hence also the composites $j_{Q Y}\circ (Q_f)_i $ are [[left homotopy|left homotopic]] to each other, and since their domain is cofibrant, then by lemma \ref{LeftHomotopyWithCofibrantDomainImpliesRightHomotopyAndDually} they are also [[right homotopy|right homotopic]] by a right homotopy $\kappa$. This implies finally, by lifting in

$$
  \array{
    Q X &\overset{\kappa}{\longrightarrow}& Path(P Q Y)
    \\
    {}^{\mathllap{\in W \cap Cof}}\downarrow
     &&
    \downarrow^{\mathrlap{\in Fib}}
    \\
    P Q X &\underset{(R (Q f)_1, P (Q f)_2)}{\longrightarrow}&
    P Q Y \times P Q Y
  }
$$

that also $P (Q f)_1$ and $P (Q f)_2$ are right homotopic, hence that indeed $P Q f$ represents a well-defined [[homotopy class]].

Finally to see that the assignment is indeed [[functor|functorial]], observe that the commutativity of the lifting diagrams for $Q f$ and $P Q f$ imply that also the following diagram commutes

$$
  \array{
    X &\overset{p_X}{\longleftarrow}& Q X &\overset{j_{Q X}}{\longrightarrow}& P Q X
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{Q f}} && \downarrow^{\mathrlap{P Q f}}
    \\
    Y &\underset{p_y}{\longleftarrow}& Q Y &\underset{j_{Q Y}}{\longrightarrow}& P Q Y
  }
  \,.
$$

Now from the [[pasting]] composite

$$
  \array{
    X &\overset{p_X}{\longleftarrow}& Q X &\overset{j_{Q X}}{\longrightarrow}& P Q X
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{Q f}} && \downarrow^{\mathrlap{P Q f}}
    \\
    Y &\underset{p_Y}{\longleftarrow}& Q Y &\underset{j_{Q Y}}{\longrightarrow}& P Q Y
    \\
    {}^{\mathllap{g}}\downarrow && \downarrow^{\mathrlap{Q g}} && \downarrow^{\mathrlap{P Q g}}
    \\
    Z &\underset{p_Z}{\longleftarrow}& Q Z &\underset{j_{Q Z}}{\longrightarrow}& P Q Z
  }
$$

one sees that $(P Q g)\circ (P Q f)$ is a lift of $g \circ f$ and hence the same argument as above gives that it is homotopic to the chosen $P Q(g \circ f)$.


=--

For the following, recall the concept of [[natural isomorphism]] between [[functors]]: for $F, G \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ two functors, then a _[[natural transformation]]_ $\eta \colon F \Rightarrow G$ is for each object $c \in Obj(\mathcal{C})$ a morphism $\eta_c \colon F(c) \longrightarrow G(c)$ in $\mathcal{D}$, such that for each morphism $f \colon c_1 \to c_2$ in $\mathcal{C}$ the following is a [[commuting square]]:

$$
  \array{
    F(c_1) &\overset{\eta_{c_1}}{\longrightarrow}& G(c_1)
    \\
    {}^{\mathllap{F(f)}}\downarrow && \downarrow^{\mathrlap{G(f)}}
    \\
    F(c_2) &\underset{\eta_{c_2}}{\longrightarrow}& G(c_2)
  }
  \,.
$$

Such $\eta$ is called a _[[natural isomorphism]]_ if its $\eta_c$ are [[isomorphisms]] for all objects $c$.

+-- {: .num_defn #HomotopyCategoryOfACategoryWithWeakEquivalences}
###### Definition

For $\mathcal{C}$ a [[category with weak equivalences]], its  **[[localization]] at the weak equivalences** is, if it exists,

1. a [[category]] denoted $\mathcal{C}[W^{-1}]$

1. a [[functor]]

   $$
     \gamma \;\colon\; \mathcal{C} \longrightarrow \mathcal{C}[W^{-1}]
   $$

such that

1. $\gamma$ sends weak equivalences to [[isomorphisms]];

1. $\gamma$ is [[universal property|universal with this property]], in that:

   for $F \colon \mathcal{C} \longrightarrow D$ any [[functor]] out of $\mathcal{C}$ into any [[category]] $D$, such that $F$ takes weak equivalences to [[isomorphisms]], it factors through $\gamma$ up to a [[natural isomorphism]] $\rho$

   $$
     \array{
       \mathcal{C} && \overset{F}{\longrightarrow} && D
       \\
       & {}_{\mathllap{\gamma}}\searrow &\Downarrow^{\rho}& \nearrow_{\mathrlap{\tilde F}}
       \\
       && Ho(\mathcal{C})
     }
   $$

   and this factorization is unique up to unique isomorphism, in that for $(\tilde F_1, \rho_1)$ and $(\tilde F_2, \rho_2)$ two such factorizations, then there is a unique [[natural isomorphism]] $\kappa \colon \tilde F_1 \Rightarrow \tilde F_2$ making the evident diagram of natural isomorphisms commute.

=--


+-- {: .num_theorem #UniversalPropertyOfHomotopyCategoryOfAModelCategory}
###### Theorem
**(convenient [[localization]] of [[model categories]])**

For $\mathcal{C}$ a [[model category]], the functor $\gamma_{P,Q}$ in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory} (for any choice of $P$ and $Q$) exhibits $Ho(\mathcal{C})$ as indeed being the [[localization]] of the underlying [[category with weak equivalences]] at its weak equivalences, in the sense of def. \ref{HomotopyCategoryOfACategoryWithWeakEquivalences}:

$$
  \array{
     \mathcal{C} &=& \mathcal{C}
     \\
     {}^{\mathllap{\gamma_{P,Q}}}\downarrow && \downarrow^{\mathrlap{\gamma}}
     \\
     Ho(\mathcal{C}) &\simeq& \mathcal{C}[W^{-1}]
  }
  \,.
$$

=--

([Quillen 67, I.1 theorem 1](model+category#Quillen67))

+-- {: .proof #ProofOfUniversalPropertyOfHomotopyCategoryOfAModelCategory}
###### Proof

First, to see that that $\gamma_{P,Q}$ indeed takes weak equivalences to isomorphisms: By [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) applied to the [[commuting diagrams]] shown in the proof of lemma \ref{ConstructionOfLocalizationFunctorForModelCategoryIsWellDefined}, the morphism $P Q f$ is a weak equivalence if $f$ is:

$$
  \array{
    X &\underoverset{\simeq}{p_X}{\longleftarrow}& Q X &\underoverset{\simeq}{j_{Q X}}{\longrightarrow}& P Q X
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{Q f}} && \downarrow^{\mathrlap{P Q f}}
    \\
    Y &\underoverset{p_y}{\simeq}{\longleftarrow}& Q Y &\underoverset{j_{Q Y}}{\simeq}{\longrightarrow}& P Q Y
  }
$$

With this the "Whitehead theorem for model categories", lemma \ref{WhiteheadTheoremInModelCategories}, implies that $P Q f$ represents an isomorphism in $Ho(\mathcal{C})$.

Now let $F \colon \mathcal{C}\longrightarrow D$ be any functor that sends weak equivalences to isomorphisms. We need to show that it factors as

$$
  \array{
    \mathcal{C} && \overset{F}{\longrightarrow} && D
    \\
    & {}_{\mathllap{\gamma}}\searrow &\Downarrow^{\rho}& \nearrow_{\mathrlap{\tilde F}}
    \\
    && Ho(\mathcal{C})
  }
$$

uniquely up to unique [[natural isomorphism]]. Now by construction of $P$ and $Q$ in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}, $\gamma_{P,Q}$ is the identity on the [[full subcategory]] of fibrant-cofibrant objects. It follows that if $\tilde F$ exists at all, it must satisfy for all $X \stackrel{f}{\to} Y$ with $X$ and $Y$ both fibrant and cofibrant that

$$
  \tilde F([f]) \simeq F(f)
  \,,
$$

(hence in particular $\tilde F(\gamma_{P,Q}(f)) = F(P Q f)$).

But by def. \ref{HomotopyCategoryOfAModelCategory} that already fixes $\tilde F$ on all of $Ho(\mathcal{C})$, up to unique [[natural isomorphism]]. Hence it only remains to check that with this definition of $\tilde F$ there exists any [[natural isomorphism]] $\rho$ filling the diagram above.

To that end, apply $F$ to the above [[commuting diagram]] to obtain

$$
  \array{
    F(X) &\underoverset{iso}{F(p_X)}{\longleftarrow}& F(Q X) &\underoverset{iso}{F(j_{Q X})}{\longrightarrow}& F(P Q X)
    \\
    {}^{\mathllap{F(f)}}\downarrow && \downarrow^{\mathrlap{F(Q f)}} && \downarrow^{\mathrlap{F(P Q f)}}
    \\
    F(Y) &\underoverset{F(p_y)}{iso}{\longleftarrow}& F(Q Y) &\underoverset{F(j_{Q Y})}{iso}{\longrightarrow}& F(P Q Y)
  }
  \,.
$$

Here now all horizontal morphisms are [[isomorphisms]], by assumption on $F$. It follows that defining $\rho_X \coloneqq F(j_{Q X}) \circ F(p_X)^{-1}$ makes the required natural isomorphism:

$$
  \array{
    \rho_X \colon & F(X) &\underoverset{iso}{F(p_X)^{-1}}{\longrightarrow}& F(Q X) &\underoverset{iso}{F(j_{Q X})}{\longrightarrow}& F(P Q X)
   &=&
   \tilde F(\gamma_{P,Q}(X))
    \\
    & {}^{\mathllap{F(f)}}\downarrow
     &&
     && \downarrow^{\mathrlap{F(P Q f)}}
     && \downarrow^{\tilde F(\gamma_{P,Q}(f))}
    \\
    \rho_Y\colon& F(Y) &\underoverset{F(p_y)^{-1}}{iso}{\longrightarrow}& F(Q Y) &\underoverset{F(j_{Q Y})}{iso}{\longrightarrow}& F(P Q Y)
   &=&
   \tilde F(\gamma_{P,Q}(X))
  }
  \,.
$$

=--

+-- {: .num_remark #EssentialUniquenessOfLocalizationFunctorOfModelCategory}
###### Remark

Due to theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory} we may suppress the choices of cofibrant $Q$ and fibrant replacement $P$ in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory} and just speak of [[generalized the|the]] [[localization functor]]

$$
  \gamma \;\colon\;
  \mathcal{C}
  \longrightarrow
  Ho(\mathcal{C})
$$

up to [[natural isomorphism]].

=--

In general, the localization $\mathcal{C}[W^{-1}]$ of a [[category with weak equivalences]] $(\mathcal{C},W)$ (def. \ref{HomotopyCategoryOfACategoryWithWeakEquivalences}) may invert _more_ morphisms than just those in $W$. However, if the category admits the structure of a [[model category]] $(\mathcal{C},W,Cof,Fib)$, then its localiztion precisely only inverts the weak equivalences.

+-- {: .num_prop #MorphismIsWeakEquivalenceIfIsoInHomotopyCategoryForQuillen}
###### Proposition

Let $\mathcal{C}$ be a [[model category]] (def. \ref{ModelCategory}) and let $\gamma \;\colon\; \mathcal{C} \longrightarrow Ho(\mathcal{C})$ be its [[localization]] functor (def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}, theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory}). Then a morphism $f$ in $\mathcal{C}$ is a weak equivalence precisely if $\gamma(f)$ is an isomorphism in $Ho(\mathcal{C})$.

=--

(e.g. [Goerss-Jardine 96, II, prop 1.14 ](Simplicial+homotopy+Theory))


While the construction of the homotopy category in def. \ref{HomotopyCategoryOfAModelCategory} combines the restriction to good (fibrant/cofibrant) objects with the passage to [[homotopy classes]] of morphisms, it is often useful to consider intermediate stages:

+-- {: .num_defn #FullSubcategoriesOfFibrantCofibrantObjects}
###### Definition

Given a [[model category]] $\mathcal{C}$, write

$$
  \array{
   && \mathcal{C}_{f c}
   \\
   & \swarrow && \searrow
   \\
   \mathcal{C}_c && && \mathcal{C}_f
   \\
   & \searrow && \swarrow
   \\
   && \mathcal{C}
  }
$$

for the system of [[full subcategory]] inclusions of:

1. the [[category of fibrant objects]] $\mathcal{C}_f$

1. the [[category of cofibrant objects]] $\mathcal{C}_c$,

1. the category of fibrant-cofibrant objects $\mathcal{C}_{fc}$,

all regarded a [[categories with weak equivalences]] (def. \ref{CategoryWithWeakEquivalences}), via the weak equivalences inherited from $\mathcal{C}$, which we write $(\mathcal{C}_f, W_f)$, $(\mathcal{C}_c, W_c)$ and $(\mathcal{C}_{f c}, W_{f c})$.


=--

+-- {: .num_remark #CategoriesOfFibrantObjects}
###### Remark
**([[categories of fibrant objects]] and [[cofibration categories]])**

Of course the subcategories in def. \ref{FullSubcategoriesOfFibrantCofibrantObjects} inherit more structure than just that of [[categories with weak equivalences]] from $\mathcal{C}$. $\mathcal{C}_f$ and $\mathcal{C}_c$ each inherit "half" of the factorization axioms. One says that $\mathcal{C}_f$ has the structure of a "[[fibration category]]" called a "Brown-[[category of fibrant objects]]", while $\mathcal{C}_c$ has the structure of a "[[cofibration category]]".

We discuss properties of these categories of (co-)fibrant objects below in _[Homotopy fiber sequences](#HomotopyFiberSequences)_.

=--

The proof of theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory} immediately implies the following:

+-- {: .num_cor #HomotopyCategoryOfSubcategoriesOfModelCategoriesOnGoodObjects}
###### Corollary

For $\mathcal{C}$ a [[model category]], the restriction of the localization functor $\gamma\;\colon\; \mathcal{C} \longrightarrow Ho(\mathcal{C})$ from def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory} (using remark \ref{EssentialUniquenessOfLocalizationFunctorOfModelCategory}) to any of the sub-[[categories with weak equivalences]] of def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}

$$
  \array{
   && \mathcal{C}_{f c}
   \\
   & \swarrow && \searrow
   \\
   \mathcal{C}_c && && \mathcal{C}_f
   \\
   & \searrow && \swarrow
   \\
   && \mathcal{C}
   \\
   && \downarrow^{\mathrlap{\gamma}}
   \\
   && Ho(\mathcal{C})
  }
$$

exhibits $Ho(\mathcal{C})$ equivalently as the [[localization]] also of these subcategories with weak equivalences, at their weak equivalences. In particular there are [[equivalences of categories]]

$$
  Ho(\mathcal{C})
    \simeq
  \mathcal{C}[W^{-1}]
   \simeq
  \mathcal{C}_f[W_f^{-1}]
   \simeq
  \mathcal{C}_c[W_c^{-1}]
    \simeq
  \mathcal{C}_{f c}[W_{f c}^{-1}]
  \,.
$$

=--

The following says that for computing the hom-sets in the [[homotopy category of a model category|homotopy category]], even a mixed variant of the above will do; it is sufficient that the domain is cofibrant and the codomain is fibrant:

+-- {: .num_lemma #HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory}
###### Lemma
**([[hom-sets]] of [[homotopy category]] via mapping [[cofibrant resolutions]] into [[fibrant resolutions]])**

For $X, Y \in \mathcal{C}$ with $X$ cofibrant and $Y$ fibrant, and for $P, Q$ fibrant/cofibrant replacement functors as in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}, then the morphism

$$
 Hom_{Ho(\mathcal{C})}(P X,Q Y)
  =
 Hom_{\mathcal{C}}(P X, Q Y)/_{\sim}
   \overset{Hom_{\mathcal{C}}(j_X, p_Y)}{\longrightarrow}
 Hom_{\mathcal{C}}(X,Y)/_{\sim}
$$

(on [[homotopy classes]] of morphisms, well defined by prop. \ref{BetweenCofibFibLeftAndRightHomotopyAreEquivalentEquivalenceRelations}) is a [[natural bijection]].

=--

([Quillen 67, I.1 lemma 7](model+category#Quillen67))

+-- {: .proof}
###### Proof

We may factor the morphism in question as the composite

$$
  Hom_{\mathcal{C}}(P X, Q Y)/_{\sim}
    \overset{Hom_{\mathcal{C}}(id_{P X}, p_Y)/_\sim }{\longrightarrow}
  Hom_{\mathcal{C}}(P X, Y)/_{\sim}
    \overset{Hom_{\mathcal{C}}(j_X, id_Y)/_\sim}{\longrightarrow}
  Hom_{\mathcal{C}}(X,Y)/_{\sim}
  \,.
$$

This shows that it is sufficient to see that for $X$ cofibrant and $Y$ fibrant, then

$$
  Hom_{\mathcal{C}}(id_X, p_Y)/_\sim
   \;\colon\;
  Hom_{\mathcal{C}}(X, Q Y)/_\sim \to Hom_{\mathcal{C}}(X,Y)/_\sim
$$

is an isomorphism, and dually that

$$
  Hom_{\mathcal{C}}(j_X, id_Y)/_\sim
  \;\colon\;
  Hom_{\mathcal{C}}(P X, Y)/_\sim \to Hom_{\mathcal{C}}(X,Y)/_\sim
$$

is an isomorphism. We discuss this for the former; the second is [[formal dual|formally dual]]:

First, that $Hom_{\mathcal{C}}(id_X, p_Y)$ is surjective is the [[lifting property]] in

$$
  \array{
    \emptyset &\longrightarrow& Q Y
    \\
    {}^{\mathllap{\in Cof}}\downarrow && \downarrow^{\mathrlap{p_Y}}_{\mathrlap{\in W \cap Fib}}
    \\
    X &\overset{f}{\longrightarrow}& Y
  }
  \,,
$$

which says that any morphism $f \colon X \to Y$ comes from a morphism $\hat f \colon X \to Q Y$ under postcomposition with $Q Y \overset{p_Y}{\to} Y$.

Second, that $Hom_{\mathcal{C}}(id_X, p_Y)$ is injective is the lifting property in

$$
  \array{
    X \sqcup X &\overset{(f,g)}{\longrightarrow}& Q Y
    \\
    {}^{\mathllap{\in Cof}}\downarrow && \downarrow^{\mathrlap{p_Y}}_{\mathrlap{\in W \cap Fib}}
    \\
    Cyl(X) &\underset{\eta}{\longrightarrow}& Y
  }
  \,,
$$

which says that if two morphisms $f, g \colon X \to Q Y$ become homotopic after postcomposition with $p_Y \colon Q X \to Y$, then they were already homotopic before.

=--

We record the following fact which will be used in [[Introduction to Stable homotopy theory -- 1-1|part 1.1]] ([here](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsTriangulated)):

+-- {: .num_lemma #RepresentingHomotopyCommutativeSquaresByCommutativeSquares}
###### Lemma

Let $\mathcal{C}$ be a [[model category]] (def. \ref{ModelCategory}). Then every [[commuting square]] in its [[homotopy category]] $Ho(C)$ (def. \ref{HomotopyCategoryOfAModelCategory}) is, up to [[isomorphism]] of squares, in the image of the [[localization]] functor $\mathcal{C} \longrightarrow Ho(\mathcal{C})$ of a commuting square in $\mathcal{C}$ (i.e.: not just commuting up to homotopy).

=--

+-- {: .proof}
###### Proof

Let

$$
  \array{
    A &\overset{f}{\longrightarrow}& B
    \\
    {}^{\mathllap{a}}\downarrow
      &&
    \downarrow^{\mathrlap{b}}
    \\
    A' &\underset{f'}{\longrightarrow}& B'
  }
  \;\;\;\;\;
  \in Ho(\mathcal{C})
$$

be a commuting square in the homotopy category. Writing the same symbols for fibrant-cofibrant objects in $\mathcal{C}$ and for morphisms in $\mathcal{C}$ representing these, then this means that in $\mathcal{C}$ there is a [[left homotopy]] of the form

$$
  \array{
    A &\overset{f}{\longrightarrow}& B
    \\
    {}^{\mathllap{i_1}}\downarrow && \downarrow^{\mathrlap{b}}
    \\
    Cyl(A) &\underset{\eta}{\longrightarrow}& B'
    \\
    {}^{\mathllap{i_0}}\uparrow && \uparrow^{\mathrlap{f'}}
    \\
    A &\underset{a}{\longrightarrow}& A'
  }
  \,.
$$

Consider the factorization of the top square here through the [[mapping cylinder]] of $f$

$$
  \array{
    A &\overset{f}{\longrightarrow}& B
    \\
    {}^{\mathllap{i_1}}\downarrow &(po)& \downarrow^{\mathrlap{\in W}}
    \\
    Cyl(A) &\underset{}{\longrightarrow}& Cyl(f)
    \\
    {}^{\mathllap{i_0}}\uparrow &{}_{\mathllap{\eta}}\searrow& \downarrow^{\mathrlap{}}
    \\
    A && B'
    \\
    & {}_{\mathllap{a}}\searrow & \uparrow_{\mathrlap{f'}}
    \\
    && A'
  }
$$

This exhibits the composite $A \overset{i_0}{\to} Cyl(A) \to Cyl(f)$ as an alternative representative of $f$ in $Ho(\mathcal{C})$, and $Cyl(f) \to B'$ as an alternative representative for $b$, and the commuting square

$$
  \array{
    A &\overset{}{\longrightarrow}& Cyl(f)
    \\
    {}^{\mathllap{a}}\downarrow
      &&
    \downarrow
    \\
    A' &\underset{f'}{\longrightarrow}& B'
  }
$$

as an alternative representative of the given commuting square in $Ho(\mathcal{C})$.

=--




### Derived functors
 {#DerivedFunctors}


+-- {: .num_defn #HomotopicalFunctor}
###### Definition

For $\mathcal{C}$ and $\mathcal{D}$ two [[categories with weak equivalences]], def. \ref{CategoryWithWeakEquivalences}, then a [[functor]] $F \colon \mathcal{C}\longrightarrow \mathcal{D}$ is called a **[[homotopical functor]]** if it sends weak equivalences to weak equivalences.

=--

+-- {: .num_defn #DerivedFunctorOfAHomotopicalFunctor}
###### Definition

Given a [[homotopical functor]] $F \colon \mathcal{C} \longrightarrow \mathcal{D}$ (def. \ref{HomotopicalFunctor}) between [[categories with weak equivalences]] whose [[homotopy categories]] $Ho(\mathcal{C})$ and $Ho(\mathcal{D})$ exist (def. \ref{HomotopyCategoryOfACategoryWithWeakEquivalences}), then its ("[[total derived functor|total]]") _[[derived functor]]_ is the functor $Ho(F)$ between these homotopy categories which is induced uniquely, up to unique isomorphism, by their universal property (def. \ref{HomotopyCategoryOfACategoryWithWeakEquivalences}):

$$
  \array{
    \mathcal{C} &\overset{F}{\longrightarrow}& \mathcal{D}
    \\
    {}^{\mathllap{\gamma_{\mathcal{C}}}}\downarrow
    &\swArrow_{\simeq}&
    \downarrow^{\mathrlap{\gamma_{\mathcal{D}}}}
    \\
    Ho(\mathcal{C})
      &\underset{\exists \; Ho(F)}{\longrightarrow}&
    Ho(\mathcal{D})
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

While many functors of interest between [[model categories]] are not homotopical in the sense of def. \ref{HomotopicalFunctor}, many become homotopical after restriction to the [[full subcategories]] $\mathcal{C}_f$ [[category of fibrant objects|of fibrant objects]] or $\mathcal{C}_c$ [[category of cofibrant objects|of cofibrant objects]], def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}. By corollary \ref{HomotopyCategoryOfSubcategoriesOfModelCategoriesOnGoodObjects} this is just as good for the purpose of [[homotopy theory]].

=--

Therefore one considers the following generalization of def. \ref{DerivedFunctorOfAHomotopicalFunctor}:

+-- {: .num_defn #LeftAndRightDerivedFunctorsOnModelCategories}
###### Definition

Consider a functor $F \colon \mathcal{C} \longrightarrow \mathcal{D}$ out of a [[model category]] $\mathcal{C}$ (def. \ref{ModelCategory}) into a [[category with weak equivalences]] $\mathcal{D}$ (def. \ref{CategoryWithWeakEquivalences}).

1. If the restriction of $F$ to the [[full subcategory]] $\mathcal{C}_f$ of fibrant object becomes a [[homotopical functor]] (def. \ref{HomotopicalFunctor}), then the [[derived functor]] of that restriction, according to def. \ref{DerivedFunctorOfAHomotopicalFunctor}, is called the _[[right derived functor]]_ of $F$ and denoted by $\mathbb{R}F$:

   $$
     \array{
       & \mathcal{C}_f &\hookrightarrow& \mathcal{C} &\overset{F}{\longrightarrow}& \mathcal{D}
       \\
       &
       {}^{\mathllap{\gamma}_{\mathcal{C}_f}}
       \downarrow
       &&
       \swArrow_{\simeq}
       &&
       \downarrow^{\mathrlap{\gamma_{\mathcal{D}}}}
       \\
       \mathbb{R} F \colon & \mathcal{C}_f[W^{-1}] &\simeq& Ho(\mathcal{C})
       &\underset{Ho(F)}{\longrightarrow}& Ho(\mathcal{D})
     }
     \,,
   $$

   where we use corollary \ref{HomotopyCategoryOfSubcategoriesOfModelCategoriesOnGoodObjects}.

1. If the restriction of $F$ to the [[full subcategory]] $\mathcal{C}_c$ of cofibrant object becomes a homotopical functor (def. \ref{HomotopicalFunctor}), then the [[derived functor]] of that restriction, according to def. \ref{DerivedFunctorOfAHomotopicalFunctor}, is called the _[[left derived functor]]_ of $F$ and denoted by $\mathbb{L}F$:

   $$
     \array{
       & \mathcal{C}_c &\hookrightarrow& \mathcal{C} &\overset{F}{\longrightarrow}& \mathcal{D}
       \\
       &
       {}^{\mathllap{\gamma}_{\mathcal{C}_f}}\downarrow
       &&
       \swArrow_{\simeq}
       &&
       \downarrow^{\mathrlap{\gamma_{\mathcal{D}}}}
       \\
       \mathbb{L} F \colon & \mathcal{C}_c[W^{-1}] &\simeq& Ho(\mathcal{C})
       &\underset{Ho(F)}{\longrightarrow}& Ho(\mathcal{D})
     }
     \,,
   $$

   where again we use corollary \ref{HomotopyCategoryOfSubcategoriesOfModelCategoriesOnGoodObjects}.

=--

The key fact that makes def. \ref{LeftAndRightDerivedFunctorsOnModelCategories} practically relevant is the following:

+-- {: .num_prop #KenBrownLemma}
###### Proposition
**([[Ken Brown's lemma]])**

Let $\mathcal{C}$ be a [[model category]] with [[full subcategories]] $\mathcal{C}_f, \mathcal{C}_c$ [[category of fibrant objects|of fibrant objects]] and [[cofibration category|of cofibrant objects]] respectively (def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}). Let $\mathcal{D}$ be a [[category with weak equivalences]].

1. A [[functor]] out of the [[category of fibrant objects]]

   $$
     F \;\colon\; \mathcal{C}_f \longrightarrow \mathcal{D}
   $$

   is a [[homotopical functor]], def. \ref{HomotopicalFunctor}, already if it sends acylic fibrations to weak equivalences.

1. A [[functor]] out of the [[category of cofibrant objects]]

   $$
     F \;\colon\; \mathcal{C}_c \longrightarrow \mathcal{D}
   $$

   is a [[homotopical functor]], def. \ref{HomotopicalFunctor}, already if it sends acylic cofibrations to weak equivalences.

=--

The following proof refers to the [[factorization lemma]], whose full statement and proof we postpone to further below (lemma \ref{FactorizationLemma}).

+-- {: .proof}
###### Proof

We discuss the case of a functor on a [[category of fibrant objects]] $\mathcal{C}_f$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}. The other case is [[formal dual|formally dual]].

Let $f \colon X \longrightarrow Y$ be a weak equivalence in $\mathcal{C}_f$. Choose a [[path space object]] $Path(X)$ (def. \ref{PathAndCylinderObjectsInAModelCategory}) and consider the diagram

$$
  \array{
    Path(f) &\underset{\in W \cap Fib}{\longrightarrow}& X
    \\
    {}^{\mathllap{p_1^\ast f}}_{\mathllap{\in W}}\downarrow
    &(pb)&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in W}}
    \\
    Path(Y) &\overset{p_1}{\underset{\in W \cap Fib}{\longrightarrow}}& Y
    \\
    {}^{\mathllap{p_0}}_{\mathllap{\in W \cap Fib}}\downarrow
    \\
    Y
  }
  \,,
$$

where the square is a [[pullback]] and $Path(f)$ on the top left is our notation for the universal [[cone]] object. (Below we discuss this in more detail, it is the _[[mapping cocone]]_ of $f$, def. \ref{MappingConeAndMappingCocone}).

Here:

1. $p_i$ are both acyclic fibrations, by lemma \ref{ComponentMapsOfCylinderAndPathSpaceInGoodSituation};

1. $Path(f) \to X$ is an acyclic fibration because it is the pullback of $p_1$.

1. $p_1^\ast f$ is a weak equivalence, because the [[factorization lemma]] \ref{FactorizationLemma} states that the composite vertical morphism factors $f$ through a weak equivalence, hence if $f$ is a weak equivalence, then $p_1^\ast f$ is by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

Now apply the functor $F$ to this diagram and use the assumption that it sends acyclic fibrations to weak equivalences to obtain

$$
  \array{
    F(Path(f)) &\underset{\in W }{\longrightarrow}& F(X)
    \\
    {}^{\mathllap{F(p_1^\ast f)}}_{\mathllap{}}\downarrow && \downarrow^{\mathrlap{F(f)}}
    \\
    F(Path(Y)) &\overset{F(p_1)}{\underset{\in W }{\longrightarrow}}& F(Y)
    \\
    {}^{\mathllap{F(p_0)}}_{\mathllap{\in W}}\downarrow
    \\
    Y
  }
  \,.
$$

But the [[factorization lemma]] \ref{FactorizationLemma}, in addition says that the vertical composite $p_0 \circ p_1^\ast f$ is a fibration, hence an acyclic fibration by the above. Therefore also $F(p_0 \circ p_1^\ast f)$ is a weak equivalence. Now the claim that also $F(f)$ is a weak equivalence follows with applying [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) twice.

=--

+-- {: .num_cor #LeftAndRightDerivedFunctors}
###### Corollary

Let $\mathcal{C}, \mathcal{D}$ be [[model categories]] and consider $F \colon \mathcal{C}\longrightarrow \mathcal{D}$ a [[functor]]. Then:

1. If $F$ preserves cofibrant objects and acyclic cofibrations between these, then its [[left derived functor]] (def. \ref{LeftAndRightDerivedFunctorsOnModelCategories}) $\mathbb{L}F$ exists, fitting into a [[diagram]]

   $$
     \array{
       \mathcal{C}_{c} &\overset{F}{\longrightarrow}& \mathcal{D}_{c}
       \\
       {}^{\mathllap{\gamma_{\mathcal{C}}}}\downarrow
       &\swArrow_{\simeq}&
       \downarrow^{\mathrlap{\gamma_{\mathcal{D}}}}
       \\
       Ho(\mathcal{C}) &\overset{\mathbb{L}F}{\longrightarrow}& Ho(\mathcal{D})
     }
   $$

1. If $F$ preserves fibrant objects and acyclic fibrants between these, then its [[right derived functor]] (def. \ref{LeftAndRightDerivedFunctorsOnModelCategories}) $\mathbb{R}F$ exists, fitting into a [[diagram]]

   $$
     \array{
       \mathcal{C}_{f} &\overset{F}{\longrightarrow}& \mathcal{D}_{f}
       \\
       {}^{\mathllap{\gamma_{\mathcal{C}}}}\downarrow
       &\swArrow_{\simeq}&
       \downarrow^{\mathrlap{\gamma_{\mathcal{D}}}}
       \\
       Ho(\mathcal{C}) &\underset{\mathbb{R}F}{\longrightarrow}& Ho(\mathcal{D})
     }
     \,.
   $$

=--

+-- {: .num_example #ComputationOfLeftRightDerivedFunctorsViaResolutions}
###### Proposition

Let $F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ be a functor between two [[model categories]] (def. \ref{ModelCategory}).

1. If $F$ preserves fibrant objects and weak equivalences between fibrant objects, then the total [[right derived functor]] $\mathbb{R}F \coloneqq \mathbb{R}(\gamma_{\mathcal{D}}\circ F)$ (def. \ref{LeftAndRightDerivedFunctorsOnModelCategories}) in

   $$
     \array{
       \mathcal{C}_f &\overset{F}{\longrightarrow}& \mathcal{D}
       \\
       {}^{\mathllap{\gamma_{\mathcal{C}_f}}}\downarrow
         &\swArrow_{\simeq}&
       \downarrow^{\mathrlap{\gamma_{\mathcal{D}}}}
       \\
       Ho(\mathcal{C})
         &\underset{\mathbb{R}F}{\longrightarrow}&
       Ho(\mathcal{D})
     }
   $$

   is given, up to isomorphism, on any object $ X\in \mathcal{C} \overset{\gamma_{\mathcal{C}}}{\longrightarrow} Ho(\mathcal{C})$ by appying $F$ to a fibrant replacement $P X$ of $X$ and then forming a cofibrant replacement $Q(F(P X))$ of the result:


  $$
    \mathbb{R}F(X)
      \simeq
    Q(F(P X))
    \,.
  $$

1. If $F$ preserves cofibrant objects and weak equivalences between cofibrant objects, then the total [[left derived functor]] $\mathbb{L}F \coloneqq \mathbb{L}(\gamma_{\mathcal{D}}\circ F)$ (def. \ref{LeftAndRightDerivedFunctorsOnModelCategories}) in

   $$
     \array{
       \mathcal{C}_c &\overset{F}{\longrightarrow}& \mathcal{D}
       \\
       {}^{\mathllap{\gamma_{\mathcal{C}_c}}}\downarrow
         &\swArrow_{\simeq}&
       \downarrow^{\mathrlap{\gamma_{\mathcal{D}}}}
       \\
       Ho(\mathcal{C})
         &\underset{\mathbb{L}F}{\longrightarrow}&
       Ho(\mathcal{D})
     }
   $$

   is given, up to isomorphism, on any object $ X\in \mathcal{C} \overset{\gamma_{\mathcal{C}}}{\longrightarrow} Ho(\mathcal{C})$ by appying $F$ to a cofibrant replacement $Q X$ of $X$ and then forming a fibrant replacement $P(F(Q X))$ of the result:


  $$
    \mathbb{L}F(X)
      \simeq
    P(F(Q X))
    \,.
  $$



=--

+-- {: .proof}
###### Proof

We discuss the first case, the second is [[formal duality|formally dual]]. By the proof of theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory} we have

$$
  \begin{aligned}
    \mathbb{R}F(X)
      & \simeq
    \gamma_{\mathcal{D}}(F(\gamma_{\mathcal{C}}))
    \\
      & \simeq
     \gamma_{\mathcal{D}}F(Q(P(X)) )
  \end{aligned}
  \,.
$$

But since $F$ is a homotopical functor on fibrant objects, the cofibrant replacement morphism $F(Q(P(X)))\to F(P(X))$ is a weak equivalence in $\mathcal{D}$, hence becomes an isomorphism under $\gamma_{\mathcal{D}}$. Therefore

$$
  \mathbb{R}F(X)
    \simeq
  \gamma_{\mathcal{D}}(F(P(X)))
  \,.
$$

Now since $F$ is assumed to preserve fibrant objects, $F(P(X))$ is fibrant in $\mathcal{D}$, and hence $\gamma_{\mathcal{D}}$ acts on it (only) by cofibrant replacement.

=--





### Quillen adjunctions
 {#QuillenAdjunctions}

In practice it turns out to be useful to arrange for the assumptions in corollary \ref{LeftAndRightDerivedFunctors} to be satisfied by pairs of [[adjoint functors]] ([this Def.](geometry+of+physics+--+categories+and+toposes#AdjointFunctorsInTermsOfNaturalBijectionOfHomSets)). Recall that this is a pair of [[functors]] $L$ and $R$ going back and forth between two categories

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {}
  \mathcal{D}
$$

such that there is a [[natural bijection]] between [[hom-sets]] with $L$ on the left and those with $R$ on the right:

$$
  \phi_{d,c}
   \;\colon\;
  Hom_{\mathcal{C}}(L(d),c)
   \underoverset{\simeq}{}{\longrightarrow}
  Hom_{\mathcal{D}}(d, R(c))
$$

for all objects $d\in \mathcal{D}$ and $c \in \mathcal{C}$. This being natural means that $\phi \colon Hom_{\mathcal{D}}(L(-),-) \Rightarrow Hom_{\mathcal{C}}(-, R(-))$ is a [[natural transformation]], hence that for all morphisms $g \colon d_2 \to d_1$ and $f \colon c_1 \to c_2$ the following is a [[commuting square]]:

$$
  \array{
    Hom_{\mathcal{C}}(L(d_1), c_1)
     & \underoverset{\simeq}{\phi_{d_1,c_1}}{\longrightarrow} &
    Hom_{\mathcal{D}}(d_1, R(c_1))
    \\
    {}^{\mathllap{L(f) \circ (-)\circ g}}\downarrow
     &&
    \downarrow^{\mathrlap{g\circ (-)\circ R(g)}}
    \\
    Hom_{\mathcal{C}}(L(d_2), c_2)
     & \underoverset{\phi_{d_2, c_2}}{\simeq}{\longrightarrow} &
    Hom_{\mathcal{D}}(d_2, R(c_2))
  }
  \,.
$$

We write $(L \dashv R)$ to indicate such an [[adjunction]] and call $L$ the _[[left adjoint]]_ and $R$ the _[[right adjoint]]_ of the adjoint pair.

The archetypical example of a pair of adjoint functors is that consisting of forming [[Cartesian products]] $Y \times (-)$ and forming [[mapping spaces]] $(-)^Y$, as in the category of [[compactly generated topological spaces]] of def. \ref{kTop}.

If $f \colon L(d) \to c$ is any morphism, then the image $\phi_{d,c}(f) \colon d \to R(c)$ is called its _[[adjunct]]_, and conversely. The fact that adjuncts are in bijection is also expressed by the notation

$$
  \frac{
    L(c) \overset{f}{\longrightarrow} d
  }{
    c \overset{\tilde f}{\longrightarrow} R(d)
  }
  \,.
$$

For an object $d\in \mathcal{D}$, the [[adjunct]] of the identity on $L d$ is called the _[[adjunction unit]]_ $\eta_d \;\colon\; d \longrightarrow R L d$.

For an object $c \in \mathcal{C}$, the [[adjunct]] of the identity on $R c$ is called the _[[adjunction counit]]_ $\epsilon_c \;\colon\; L R c \longrightarrow c$.

Adjunction units and counits turn out to encode the [[adjuncts]] of all other morphisms by the formulas

* $\widetilde{(L d\overset{f}{\to}c)} = (d\overset{\eta}{\to} R L d \overset{R f}{\to} R c)$

* $\widetilde{(d\overset{g}{\to} R c)} = (L d \overset{L g}{\to} L R c \overset{\epsilon}{\to} c)$.


+-- {: .num_defn #QuillenAdjunction}
###### Definition
**([[Quillen adjunction]])**

Let $\mathcal{C}, \mathcal{D}$ be [[model categories]]. A pair of [[adjoint functors]] ([this Def.](geometry+of+physics+--+categories+and+toposes#AdjointFunctorsInTermsOfNaturalBijectionOfHomSets)) between them

$$
  (L \dashv R)
  \;\colon\;
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {}
  \mathcal{D}
$$

is called a **[[Quillen adjunction]]** (and $L$,$R$ are called left/right **Quillen functors**, respectively) if the following equivalent conditions are satisfied

1. $L$ preserves cofibrations and $R$ preserves fibrations;

1. $L$ preserves acyclic cofibrations and $R$ preserves acyclic fibrations;

1. $L$ preserves cofibrations and acylic cofibrations;

1. $R$ preserves fibrations and acyclic fibrations.


=--

+-- {: .num_prop #ConditionsOnQuillenAdjunctionAreIndeedEquivalent}
###### Proposition

The conditions in def. \ref{QuillenAdjunction} are indeed all equivalent.

=--

([Quillen 67, I.4, theorem 3](model+category#Quillen67))

+-- {: .proof}
###### Proof

First observe that

* (i) _A [[left adjoint]] $L$ between [[model categories]] preserves acyclic cofibrations precisely if its [[right adjoint]] $R$ preserves fibrations.

* (ii) _A [[left adjoint]] $L$ between [[model categories]] preserves cofibrations precisely if its [[right adjoint]] $R$ preserves acyclic fibrations.

We discuss statement (i), statement (ii) is [[formal dual|formally dual]].  So let $f\colon A \to B$ be an acyclic cofibration in $\mathcal{D}$ and $g \colon X \to Y$ a fibration in $\mathcal{C}$. Then for every [[commuting diagram]] as on the left of the following, its $(L\dashv R)$-[[adjunct]] is a commuting diagram as on the right here:

$$
  \array{
    A &\longrightarrow& R(X)
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{R(g)}}
    \\
    B &\longrightarrow& R(Y)
  }
  \;\;\;\;\;\;
  \,,
  \;\;\;\;\;\;
  \array{
    L(A) &\longrightarrow& X
    \\
    {}^{\mathllap{L(f)}}\downarrow && \downarrow^{\mathrlap{g}}
    \\
    L(B) &\longrightarrow& Y
  }
  \,.
$$

If $L$ preserves acyclic cofibrations, then the diagram on the right has a [[lift]], and so the $(L\dashv R)$-[[adjunct]] of that lift is a lift of the left diagram. This shows that $R(g)$ has the [[right lifting property]] against all acylic cofibrations and hence is a fibration.
Conversely, if $R$ preserves fibrations, the same argument run from right to left gives that $L$ preserves acyclic fibrations.

Now by repeatedly applying (i) and (ii), all four conditions in question are seen to be equivalent.

=--

+-- {: .num_lemma #LeftRightQuillenFunctorsPreserveCyclinderPathSpaceObjects}
###### Lemma

Let $\mathcal{C} \stackrel{\overset{L}{\longleftarrow}}{\underoverset{R}{\bot}{\longrightarrow}} \mathcal{D}$ be a [[Quillen adjunction]], def. \ref{QuillenAdjunction}.

1. For $X \in \mathcal{C}$ a fibrant object and $Path(X)$ a [[path space object]] (def. \ref{PathAndCylinderObjectsInAModelCategory}), then $R(Path(X))$ is a path space object for $R(X)$.

1. For $X \in \mathcal{C}$ a cofibrant object and $Cyl(X)$ a [[cylinder object]] (def. \ref{PathAndCylinderObjectsInAModelCategory}), then $L(Cyl(X))$ is a path space object for $L(X)$.

=--

+-- {: .proof}
###### Proof

Consider the second case, the first is [[formal dual|formally dual]].

First Observe that  $L(Y \sqcup Y) \simeq L Y \sqcup L Y$ because $L$ is [[left adjoint]] and hence preserves [[colimits]], hence in particular [[coproducts]].

Hence

$$
  L(\X \sqcup X \overset{\in Cof}{\to} Cyl(X))
  =
  (L(X) \sqcup L(X) \overset{\in Cof}{\to } L (Cyl(X)))
$$

is a cofibration.

Second, with $Y$ cofibrant then also $Y \sqcup Cyl(Y)$ is a cofibrantion, since $Y \to Y \sqcup Y$ is a cofibration (lemma \ref{ComponentMapsOfCylinderAndPathSpaceInGoodSituation}). Therefore by [[Ken Brown's lemma]] (prop. \ref{KenBrownLemma}) $L$ preserves the weak equivalence $Cyl(Y) \overset{\in W}{\longrightarrow} Y$.

=--

+-- {: .num_prop #QuillenAdjunctionInducesAdjunctionOnHomotopyCategories}
###### Proposition
**([[Quillen adjunction]] descends to [[homotopy categories]])**

For $\mathcal{C} \underoverset{\underoverset{R}{\bot}{\longrightarrow}}{\overset{L}{\longleftarrow}}{} \mathcal{D}$ a [[Quillen adjunction]], def. \ref{QuillenAdjunction}, then also the corresponding left and right [[derived functors]], def. \ref{LeftAndRightDerivedFunctorsOnModelCategories}, via cor. \ref{LeftAndRightDerivedFunctors}, form a pair of [[adjoint functors]]

$$
  Ho(\mathcal{C})
    \underoverset
      {\underset{\mathbb{R}R}{\longrightarrow}}
      {\overset{\mathbb{L}L}{\longleftarrow}}
      {\bot}
  Ho(\mathcal{D})
  \,.
$$

=--

([Quillen 67, I.4 theorem 3](model+category#Quillen67))

+-- {: .proof}
###### Proof

By def. \ref{LeftAndRightDerivedFunctorsOnModelCategories} and lemma \ref{HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory} it is sufficient to see that for $X, Y \in \mathcal{C}$ with $X$ cofibrant and $Y$ fibrant, then there is a [[natural bijection]]

$$
  Hom_{\mathcal{C}}(L X , Y)/_\sim
   \simeq
  Hom_{\mathcal{C}}(X, R Y)/_\sim
  \,.
$$

Since by the [[adjoint functor|adjunction isomorphism]] for $(L \dashv R)$ such a natural bijection exists before passing to homotopy classes $(-)/_\sim$, it is sufficient to see that this respects homotopy classes. To that end, use from lemma \ref{LeftRightQuillenFunctorsPreserveCyclinderPathSpaceObjects} that with $Cyl(Y)$ a [[cylinder object]] for $Y$, def. \ref{PathAndCylinderObjectsInAModelCategory}, then $L(Cyl(Y))$ is a cylinder object for $L(Y)$. This implies that left homotopies

$$
  (f \Rightarrow_L g) \;\colon\;  L X \longrightarrow Y
$$

given by

$$
 \eta \;\colon\; Cyl(L X) =  L Cyl(X) \longrightarrow Y
$$

are in bijection to left homotopies

$$
  (\tilde f \Rightarrow_L \tilde g) \;\colon\; X \longrightarrow R Y
$$

given by

$$
  \tilde \eta \;\colon\; Cyl(X) \longrightarrow R X
  \,.
$$

=--

The following is the analog of [[adjoint equivalence of categories]] ([this Def.](geometry+of+physics+--+categories+and+toposes#AdjointEquivalenceOfCategories)) for [[model categories]].

+-- {: .num_defn #QuillenEquivalence}
###### Definition
**([[Quillen equivalence]])**

For $\mathcal{C}, \mathcal{D}$ two [[model categories]],  a [[Quillen adjunction]] (def.\ref{QuillenAdjunction})

$$
  (L \dashv R)
  \;\colon\;
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

is called a **[[Quillen equivalence]]**, to be denoted

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\simeq_{\mathrlap{Q}}}
  \mathcal{D}
  \,,
$$

if the following equivalent conditions hold.

1. The [[right derived functor]] of $R$ (via prop. \ref{ConditionsOnQuillenAdjunctionAreIndeedEquivalent}, corollary \ref{LeftAndRightDerivedFunctors}) is an [[equivalence of categories]]

   $$
     \mathbb{R}R \colon Ho(\mathcal{C}) \overset{\simeq}{\longrightarrow} Ho(\mathcal{D})
     \,.
   $$

1. The [[left derived functor]] of $L$ (via prop. \ref{ConditionsOnQuillenAdjunctionAreIndeedEquivalent}, corollary \ref{LeftAndRightDerivedFunctors}) is an [[equivalence of categories]]

   $$
     \mathbb{L}L \colon Ho(\mathcal{D}) \overset{\simeq}{\longrightarrow} Ho(\mathcal{C})
     \,.
   $$

1. For every cofibrant object $d\in \mathcal{D}$, the "derived adjunction unit", hence the composite

   $$
     d
       \overset{\eta}{\longrightarrow}
     R(L(d))
       \overset{R(j_{L(d)})}{\longrightarrow}
     R(P(L(d)))
   $$

   (of the [[adjunction unit]] with any fibrant replacement $P$ as in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}) is a weak equivalence;

   and for every fibrant object $c \in \mathcal{C}$, the "derived adjunction counit", hence the composite

     $$
       L(Q(R(c)))
         \overset{L(p_{R(c)})}{\longrightarrow}
       L(R(c))
         \overset{\epsilon}{\longrightarrow}
       c
     $$

     (of the [[adjunction counit]] with any cofibrant replacement as in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}) is a weak equivalence in $D$.


1. For every cofibrant object $d \in \mathcal{D}$ and every fibrant object $c \in \mathcal{C}$, a morphism $d \longrightarrow R(c)$ is a weak equivalence precisely if its [[adjunct]] morphism $L(c) \to d$ is:

   $$
      \frac{
        d \overset{\in W_{\mathcal{D}}}{\longrightarrow} R(c)
      }{
         L(d) \overset{\in W_{\mathcal{C}}}{\longrightarrow} c
      }
      \,.
   $$


=--

+-- {: .num_prop #ConditionsForQuillenAdjunctionAreIndeedEquivalent}
###### Poposition

The conditions in def. \ref{QuillenEquivalence} are indeed all equivalent.

=--

([Quillen 67, I.4, theorem 3](model+category#Quillen67))

+-- {: .proof}
###### Proof

That $1) \Leftrightarrow 2)$ follows from prop. \ref{QuillenAdjunctionInducesAdjunctionOnHomotopyCategories} (if in an adjoint pair one is an equivalence, then so is the other).

To see the equivalence $1),2) \Leftrightarrow 3)$, notice ([prop.](adjoint+functor#FullyFaithfulAndInvertibleAdjoints)) that a pair of [[adjoint functors]] is an [[equivalence of categories]] precisely if both the [[adjunction unit]] and the [[adjunction counit]] are [[natural isomorphisms]]. Hence it is sufficient to show that the morphisms called "derived adjunction (co-)units" above indeed represent the adjunction (co-)unit of $(\mathbb{L}L \dashv \mathbb{R}R)$ in the homotopy category.
We show this now for the adjunction unit, the case of the adjunction counit is formally dual.

To that end, first observe that for $d \in \mathcal{D}_c$, then the defining commuting square for the left derived functor from def. \ref{LeftAndRightDerivedFunctorsOnModelCategories}

$$
  \array{
    \mathcal{D}_c &\overset{L}{\longrightarrow}& \mathcal{C}
    \\
    {}^{\mathllap{\gamma_P}}\downarrow
      &\swArrow_{\simeq}&
    \downarrow^{\mathrlap{\gamma_{P,Q}}}
    \\
    Ho(\mathcal{D}) &\underset{\mathbb{L}L}{\longrightarrow}& Ho(\mathcal{C})
  }
$$

(using fibrant and fibrant/cofibrant replacement functors $\gamma_P$, $\gamma_{P,Q}$ from def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory} with their universal property from theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory}, corollary \ref{HomotopyCategoryOfSubcategoriesOfModelCategoriesOnGoodObjects}) gives that

$$
  (\mathbb{L} L ) d \simeq P L P d \simeq P L d \;\;\;\; \in Ho(\mathcal{C})
  \,,
$$

where the second isomorphism holds because the left Quillen functor $L$ sends the acyclic cofibration $j_d \colon d \to P d$ to a weak equivalence.

The adjunction unit of $(\mathbb{L}L \dashv \mathbb{R}R)$ on $P d \in Ho(\mathcal{C})$ is the image of the identity under

$$
  Hom_{Ho(\mathcal{C})}((\mathbb{L}L) P d, (\mathbb{L} L) P d)
  \overset{\simeq}{\to}
  Hom_{Ho(\mathcal{C})}(P d, (\mathbb{R}R)(\mathbb{L}L) P d)
  \,.
$$

By the above and the proof of prop. \ref{QuillenAdjunctionInducesAdjunctionOnHomotopyCategories}, that adjunction isomorphism is equivalently that of $(L \dashv R)$ under the isomorphism

$$
  Hom_{Ho(\mathcal{C})}(P L d , P L d)
    \overset{Hom(j_{L d}, id)}{\longrightarrow}
  Hom_{\mathcal{C}}(L d, P L d)/_\sim
$$

of lemma \ref{HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory}. Hence the derived adjunction unit is the $(L \dashv R)$-[[adjunct]] of

$$
  L d
    \overset{j_{L d}}{\longrightarrow}
  P L d
    \overset{id}{\to}
  P L d
  \,,
$$

which indeed (by the formula for [[adjuncts]]) is

$$
  X
    \overset{\eta}{\longrightarrow}
  R L d
    \overset{R (j_{L d})}{\longrightarrow}
  R P L d
  \,.
$$

To see that $4) \Rightarrow 3)$:

Consider the weak equivalence $L X \overset{j_{L X}}{\longrightarrow} P L X$. Its $(L \dashv R)$-[[adjunct]] is

$$
  X
    \overset{\eta}{\longrightarrow}
  R L X
    \overset{R j_{L X}}{\longrightarrow}
  R P L X
$$

by assumption 4) this is again a weak equivalence, which is the requirement for the derived unit in 3). Dually for derived counit.

To see $3) \Rightarrow 4)$:

Consider any $f \colon L d \to c$ a weak equivalence for cofibrant $d$, firbant $c$. Its [[adjunct]] $\tilde f$ sits in a commuting diagram

$$
  \array{
    \tilde f \colon & d &\overset{\eta}{\longrightarrow}&  R L d &\overset{R f}{\longrightarrow}& R c
    \\
    & {}^{\mathllap{=}}\downarrow && \downarrow^{\mathrlap{R j_{L d}}} && \downarrow^{\mathrlap{R j_c}}
    \\
    & d &\underset{\in W}{\longrightarrow}& R P L d &\overset{R P f}{\longrightarrow}& R P c
  }
  \,,
$$

where $P f$ is any lift constructed as in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}.

This exhibits the bottom left morphism as the derived adjunction unit, hence a weak equivalence by assumption. But since $f$ was a weak equivalence, so is $P f$ (by [[two-out-of-three]]).  Thereby also $R P f$ and $R j_Y$, are weak equivalences by [[Ken Brown's lemma]] \ref{KenBrownLemma} and the assumed fibrancy of $c$. Therefore by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) also the [[adjunct]] $\tilde f$ is a weak equivalence.

=--

In certain situations the conditions on a Quillen equivalence simplify. For instance:

+-- {: .num_prop #InCaseTheRightAdjointCreatesWeakEquivalences}
###### Proposition

If in a [[Quillen adjunction]]  $ \array{\mathcal{C} &\underoverset{\underset{R}{\to}}{\overset{L}{\leftarrow}}{\bot}& \mathcal{D}}$ (def. \ref{QuillenAdjunction}) the [[right adjoint]] $R$ "creates weak equivalences" (in that a morphism $f$ in $\mathcal{C}$ is a weak equivalence precisly if $U(f)$ is) then $(L \dashv R)$ is a [[Quillen equivalence]] (def. \ref{QuillenEquivalence}) precisely already if for all cofibrant objects $d \in \mathcal{D}$ the plain [[adjunction unit]]

$$
  d \overset{\eta}{\longrightarrow} R (L (d))
$$

is a weak equivalence.

=--

+-- {: .proof}
###### Proof

By prop. \ref{ConditionsForQuillenAdjunctionAreIndeedEquivalent}, generally, $(L \dashv R)$ is a Quillen equivalence precisely if

1. for every cofibrant object $d\in \mathcal{D}$, the "derived adjunction unit"

   $$
     d
       \overset{\eta}{\longrightarrow}
     R(L(d))
       \overset{R(j_{L(d)})}{\longrightarrow}
     R(P(L(d)))
   $$

   is a weak equivalence;

1. for every fibrant object $c \in \mathcal{C}$, the "derived adjunction counit"

   $$
     L(Q(R(c)))
       \overset{L(p_{R(c)})}{\longrightarrow}
     L(R(c))
       \overset{\epsilon}{\longrightarrow}
     c
   $$

   is a weak equivalence.

Consider the first condition: Since $R$ preserves the weak equivalence $j_{L(d)}$, then by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) the composite in the first item is a weak equivalence precisely if $\eta$ is.

Hence it is now sufficient to show that in this case the second condition above is automatic.

Since $R$ also reflects weak equivalences, the composite in item two is a weak equivalence precisely if its image

$$
  R(L(Q(R(c))))
    \overset{R(L(p_{R(c))})}{\longrightarrow}
  R(L(R(c)))
    \overset{R(\epsilon)}{\longrightarrow}
  R(c)
$$

under $R$ is.

Moreover, assuming, by the above, that $\eta_{Q(R(c))}$ on the cofibrant object $Q(R(c))$ is a weak equivalence, then by [[two-out-of-three]] this composite is a weak equivalence precisely if the further composite with $\eta$ is

$$
  Q(R(c))
    \overset{\eta_{Q(R(c))}}{\longrightarrow}
  R(L(Q(R(c))))
    \overset{R(L(p_{R(c))})}{\longrightarrow}
  R(L(R(c)))
    \overset{R(\epsilon)}{\longrightarrow}
  R(c)
  \,.
$$

By the formula for [[adjuncts]], this composite is the $(L\dashv R)$-adjunct of the original composite, which is just $p_{R(c)}$

$$
  \frac{
     L(Q(R(c)))
       \overset{L(p_{R(c)})}{\longrightarrow}
     L(R(c))
       \overset{\epsilon}{\longrightarrow}
     c
  }{
     Q(R(C)) \overset{p_{R(c)}}{\longrightarrow} R(c)
  }
  \,.
$$

But $p_{R(c)}$ is a weak equivalence by definition of cofibrant replacement.


=--

$\,$

### Mapping cones
 {#MappingCones}


In the context of [[homotopy theory]], a [[pullback]] diagram, such as in the definition of the [[fiber]] in example \ref{FiberAndCofiberInPointedObjects}

$$
  \array{
     fib(f) &\longrightarrow& X
     \\
     \downarrow && \downarrow^{\mathrlap{f}}
     \\
     \ast &\longrightarrow& Y
  }
$$

ought to [[commuting diagram|commute]] only up to a (left/right) [[homotopy]] (def. \ref{LeftAndRightHomotopyInAModelCategory}) between the outer composite morphisms. Moreover, it should satisfy its [[universal property]] up to such homotopies.

Instead of going through the full theory of what this means, we observe that this is plausibly modeled by the following construction, and then we check ([below](#HomotopyFibers)) that this indeed has the relevant abstract homotopy theoretic properties.


+-- {: .num_defn #MappingConeAndMappingCocone}
###### Definition

Let $\mathcal{C}$ be a [[model category]], def. \ref{ModelCategory} with $\mathcal{C}^{\ast/}$ its model structure on pointed objects, prop. \ref{ModelStructureOnSliceCategory}.
For $f \colon X \longrightarrow Y$ a morphism between cofibrant objects (hence a morphism in $(\mathcal{C}^{\ast/})_c\hookrightarrow \mathcal{C}^{\ast/}$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}), its **reduced [[mapping cone]]** is the object

$$
  Cone(f)
  \coloneqq
  \ast \underset{X}{\sqcup} Cyl(X) \underset{X}{\sqcup} Y
$$

in the colimiting diagram

$$
  \array{
    && X &\stackrel{f}{\longrightarrow}& Y
    \\
    && \downarrow^{\mathrlap{i_1}} && \downarrow^{\mathrlap{i}}
    \\
    X &\stackrel{i_0}{\longrightarrow}& Cyl(X)
    \\
    \downarrow && & \searrow^{\mathrlap{\eta}} & \downarrow
    \\
    {*} &\longrightarrow& &\longrightarrow& Cone(f)
  }
  \,,
$$

where $Cyl(X)$ is a [[cylinder object]] for $X$, def. \ref{PathAndCylinderObjectsInAModelCategory}.

Dually, for $f \colon X \longrightarrow Y$ a morphism between fibrant objects (hence a morphism in $(\mathcal{C}^{\ast})_f\hookrightarrow \mathcal{C}^{\ast/}$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}), its **[[mapping cocone]]** is the object

$$
  Path_\ast(f) \coloneqq \ast \underset{Y}{\times} Path(Y)\underset{Y}{\times} Y
$$

in the following limit diagram

$$
  \array{
    Path_\ast(f) &\longrightarrow& &\longrightarrow& X
    \\
    \downarrow &\searrow^{\mathrlap{\eta}}& && \downarrow^{\mathrlap{f}}
    \\
      &&  Path(Y) &\underset{p_1}{\longrightarrow}& Y
    \\
    \downarrow && \downarrow^{\mathrlap{p_0}}
    \\
    \ast &\longrightarrow& Y
  }
  \,,
$$

where $Path(Y)$ is a [[path space object]] for $Y$, def. \ref{PathAndCylinderObjectsInAModelCategory}.


=--

+-- {: .num_remark }
###### Remark

When we write homotopies (def. \ref{LeftAndRightHomotopyInAModelCategory}) as double arrows between morphisms, then the limit diagram in def. \ref{MappingConeAndMappingCocone} looks just like the square in the definition of [[fibers]] in example \ref{FiberAndCofiberInPointedObjects}, except that it is filled by the [[right homotopy]] given by the component map denoted $\eta$:

$$
  \array{
    Path_\ast(f) &\longrightarrow& X
    \\
    \downarrow &\swArrow_{\eta}& \downarrow^{\mathrlap{f}}
    \\
    \ast &\longrightarrow& Y
  }
  \,.
$$

Dually, the colimiting diagram for the mapping cone turns to look just like the square for the [[cofiber]], except that it is filled with a [[left homotopy]]

$$
  \array{
    X &\overset{f}{\longrightarrow}& Y
    \\
    \downarrow &\swArrow_{\eta}& \downarrow
    \\
    \ast &\longrightarrow& Cone(f)
  }
$$

=--


+-- {: .num_prop #ConeAndMappingCylinder}
###### Proposition

The colimit appearing in the definition of the reduced [[mapping cone]] in def. \ref{MappingConeAndMappingCocone} is equivalent to three consecutive [[pushouts]]:

$$
  \array{
    && X &\stackrel{f}{\longrightarrow}& Y
    \\
    && \downarrow^{\mathrlap{i_1}} &(po)& \downarrow^{\mathrlap{i}}
    \\
    X &\stackrel{i_0}{\longrightarrow}& Cyl(X) &\longrightarrow& Cyl(f)
    \\
    \downarrow &(po)& \downarrow & (po) & \downarrow
    \\
    {*} &\longrightarrow& Cone(X) &\longrightarrow& Cone(f)
  }
  \,.
$$

The two intermediate objects appearing here are called

* the plain **reduced [[cone]]**  $Cone(X) \coloneqq \ast \underset{X}{\sqcup} Cyl(X)$;

* the **reduced [[mapping cylinder]]** $Cyl(f) \coloneqq Cyl(X) \underset{X}{\sqcup} Y$.

Dually, the limit appearing in the definition of the [[mapping cocone]] in def. \ref{MappingConeAndMappingCocone} is equivalent to three consecutive [[pullbacks]]:

$$
  \array{
    Path_\ast(f) &\longrightarrow& Path(f) &\longrightarrow& X
    \\
    \downarrow &(pb)& \downarrow &(pb)& \downarrow^{\mathrlap{f}}
    \\
    Path_\ast(Y)  &\longrightarrow&  Path(Y) &\underset{p_1}{\longrightarrow}& Y
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{p_0}}
    \\
    \ast &\longrightarrow& Y
  }
  \,.
$$

The two intermediate objects appearing here are called

* the **based path space object** $Path_\ast(Y) \coloneqq \ast \underset{Y}{\prod} Path(Y)$;

* the **mapping path space** or **mapping co-cylinder** $Path(f) \coloneqq X \underset{Y}{\times} Path(X)$.

=--


+-- {: .num_defn #SuspensionAndLoopSpaceObject}
###### Definition

Let $X \in \mathcal{C}^{\ast/}$ be any [[pointed object]].

1. The [[mapping cone]], def. \ref{ConeAndMappingCylinder}, of $X \to \ast$ is called the  **[[reduced suspension|reduced]] [[suspension]]** of $X$, denoted

   $$
     \Sigma X = Cone(X\to\ast)\,.
   $$

   Via prop. \ref{ConeAndMappingCylinder} this is equivalently the coproduct of two copies of the cone on $X$ over their base:

   $$
     \array{
       && X &\stackrel{}{\longrightarrow}& \ast
       \\
       && \downarrow^{\mathrlap{i_1}} &(po)& \downarrow^{\mathrlap{}}
       \\
       X &\stackrel{i_0}{\longrightarrow}& Cyl(X) &\longrightarrow& Cone(X)
       \\
       \downarrow &(po)& \downarrow & (po) & \downarrow
       \\
       {*} &\longrightarrow& Cone(X) &\longrightarrow& \Sigma X
     }
     \,.
   $$

   This is also equivalently the [[cofiber]], example \ref{FiberAndCofiberInPointedObjects} of $(i_0,i_1)$, hence (example \ref{WedgeSumAsCoproduct}) of the [[wedge sum]] inclusion:

   $$
     X \vee X
      =
     X \sqcup X
      \overset{(i_0,i_1)}{\longrightarrow}
     Cyl(X)
       \overset{cofib(i_0,i_1)}{\longrightarrow}
     \Sigma X
     \,.
   $$


1. The [[mapping cocone]], def. \ref{ConeAndMappingCylinder}, of $\ast \to X$ is called the **[[loop space object]]** of $X$, denoted

   $$
     \Omega X = Path_\ast(\ast \to X)
     \,.
   $$

   Via prop. \ref{ConeAndMappingCylinder} this is equivalently

   $$
     \array{
       \Omega X &\longrightarrow& Path_\ast(X) &\longrightarrow& \ast
       \\
       \downarrow &(pb)& \downarrow &(pb)& \downarrow^{}
       \\
       Path_\ast(X)  &\longrightarrow&  Path(X) &\underset{p_1}{\longrightarrow}& X
       \\
       \downarrow &(pb)& \downarrow^{\mathrlap{p_0}}
       \\
       \ast &\longrightarrow& X
     }
     \,.
   $$

   This is also equivalently the [[fiber]], example \ref{FiberAndCofiberInPointedObjects} of $(p_0,p_1)$:

   $$
     \Omega X
     \overset{fib(p_0,p_1)}{\longrightarrow}
     Path(X) \overset{(p_0,p_1)}{\longrightarrow} X \times X
     \,.
   $$

=--

+-- {: .num_prop #ReducedSuspensionBySmashProductWithCircle}
###### Proposition

In [[pointed topological spaces]] $Top^{\ast/}$,

* the [[reduced suspension]] objects (def. \ref{SuspensionAndLoopSpaceObject}) induced from the standard [[reduced cylinder]] $(-)\wedge (I_+)$ of example \ref{StandardReducedCyclinderInTop} are isomorphic to the [[smash product]] (def. \ref{SmashProductOfPointedObjects}) with the [[1-sphere]], for later purposes we choose to smash **on the left** and write

  $$
    cofib(X \vee X \to X \wedge (I_+)) \simeq S^1 \wedge X
    \,,
  $$

Dually:

* the [[loop space objects]] (def. \ref{SuspensionAndLoopSpaceObject}) induced from the standard pointed path space object $Maps(I_+,-)_\ast$ are isomorphic to the [[pointed mapping space]] (example \ref{PointedMappingSpace})  with the [[1-sphere]]

  $$
    fib(Maps(I_+,X)_\ast \to X \times X)
      \simeq
    Maps(S^1, X)_\ast
    \,.
  $$


=--

+-- {: .proof}
###### Proof

By immediate inspection: For instance the [[fiber]] of $Maps(I_+,X)_\ast \longrightarrow X\times X$ is clearly the subspace of the unpointed mapping space $X^I$ on elements that take the endpoints of $I$ to the basepoint of $X$.

=--



+-- {: .num_example #MappingConesInTopologicalSpaces}
###### Example

<div style="float:right;margin:0 10px 10px 0;">
<img src="http://ncatlab.org/nlab/files/mappingcone.jpg" width="560" >
</div>

For $\mathcal{C} =$ [[Top]] with $Cyl(X) = X\times I$ the standard cyclinder object, def. \ref{TopologicalInterval}, then by example \ref{PushoutInTop}, the [[mapping cone]], def. \ref{MappingConeAndMappingCocone}, of a [[continuous function]] $f \colon X \longrightarrow Y$ is obtained by

1. forming the cylinder over $X$;

1. attaching to one end of that cylinder the space $Y$ as specified by the map $f$.

1. shrinking the other end of the cylinder to the point.

Accordingly the [[suspension]] of a topological space is the result of shrinking both ends of the cylinder on the object two the point. This is homeomoprhic to attaching two copies of the cone on the space at the base of the cone.

(graphics taken from [Muro 10](http://personal.us.es/fmuro/praha.pdf))

Below in example \ref{StandardTopologicalMappingConeIsHomotopyCofiber} we find the homotopy-theoretic interpretation of this standard topological mapping cone as a model for the _[[homotopy cofiber]]_.

=--

+-- {: .num_remark #UnreducedCone}
###### Remark

The _formula_ for the [[mapping cone]] in prop. \ref{ConeAndMappingCylinder} (as opposed to that of the mapping co-cone) does not require the presence of the basepoint: for $f \colon X \longrightarrow Y$ a morphism in $\mathcal{C}$ (as opposed to in $\mathcal{C}^{\ast/}$) we may still define

$$
  Cone'(f) \coloneqq Y \underset{X}{\sqcup} Cone'(X)
  \,,
$$

where the prime denotes the _unreduced cone_, formed from a cylinder object in $\mathcal{C}$.


=--

+-- {: .num_prop #UnreducedMappingConeAsReducedConeOfBasedPointAdjoined}
###### Proposition

For $f \colon X \longrightarrow Y$ a morphism in [[Top]], then its unreduced mapping cone, remark \ref{UnreducedCone}, with respect to the standard cylinder object $X \times I$ def. \ref{TopologicalInterval}, is isomorphic to the reduced mapping cone, def. \ref{MappingConeAndMappingCocone}, of the morphism $f_+ \colon X_+ \to Y_+$ (with a basepoint adjoined, def. \ref{BasePointAdjoined}) with respect to the standard [[reduced cylinder]] (example \ref{StandardReducedCyclinderInTop}):

$$
  Cone'(f) \simeq Cone(f_+)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{LimitsAndColimitsOfPointedObjects} and example \ref{WedgeAndSmashOfBasePointAdjoinedTopologicalSpaces}, $Cone(f_+)$ is given by the colimit in $Top$ over the following diagram:

$$
  \array{
    \ast &\longrightarrow& X \sqcup \ast &\overset{(f,id)}{\longrightarrow}& Y \sqcup \ast
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X \sqcup\ast &\longrightarrow& (X \times I) \sqcup \ast
    \\
    \downarrow && && \downarrow
    \\
    \ast &\longrightarrow& &\longrightarrow& Cone(f_+)
  }
  \,.
$$

We may factor the vertical maps to give

$$
  \array{
    \ast &\longrightarrow& X \sqcup \ast &\overset{(f,id)}{\longrightarrow}& Y \sqcup \ast
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X \sqcup\ast &\longrightarrow& (X \times I) \sqcup \ast
    \\
    \downarrow && && \downarrow
    \\
    \ast \sqcup \ast &\longrightarrow& &\longrightarrow& Cone'(f)_+
    \\
    \downarrow && && \downarrow
    \\
    \ast &\longrightarrow& &\longrightarrow& Cone'(f)
  }
  \,.
$$



This way the top part of the diagram (using the [[pasting law]] to compute the colimit in two stages) is manifestly a cocone under the result of applying $(-)_+$ to the diagram for the unreduced cone. Since $(-)_+$ is itself given by a colimit, it preserves colimits, and hence gives the partial colimit $Cone'(f)_+$ as shown. The remaining pushout then contracts the remaining copy of the point away.

=--


Example \ref{MappingConesInTopologicalSpaces} makes it clear that every [[cycle]] $S^n \to Y$ in $Y$ that happens to be in the image of $X$ can be _continuously_ translated in the cylinder-direction, keeping it constant in $Y$, to the other end of the cylinder, where it shrinks away to the point. This means that every [[homotopy group]] of $Y$, def. \ref{HomotopyGroupsOftopologicalSpaces}, in the image of $f$ vanishes in the mapping cone. Hence in the mapping cone **the image of $X$ under $f$ in $Y$ is removed up to homotopy**. This makes it intuitively clear how $Cone(f)$ is a homotopy-version of the [[cokernel]] of $f$. We now discuss this formally.


+-- {: .num_lemma #FactorizationLemma}
###### Lemma
**([[factorization lemma]])**

Let $\mathcal{C}_c$ be a [[category of cofibrant objects]],  def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}. Then for every morphism $f \colon X \longrightarrow Y$ the [[mapping cylinder]]-construction in def. \ref{ConeAndMappingCylinder} provides a cofibration resolution of $f$, in that

1. the composite morphism $X \overset{i_0}{\longrightarrow} Cyl(X) \overset{(i_1)_\ast f}{\longrightarrow} Cyl(f)$ is a cofibration;

1. $f$ factors through this morphism by a weak equivalence left inverse to an acyclic cofibration

   $$
     f
       \;\colon\;
     X
        \underoverset{\in Cof}{(i_1)_\ast f\circ i_0}{\longrightarrow}
     Cyl(f)
       \underset{\in W}{\longrightarrow}
     Y
     \,,
   $$

Dually:

Let $\mathcal{C}_f$ be a [[category of fibrant objects]],  def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}. Then for every morphism $f \colon X \longrightarrow Y$ the [[mapping cocylinder]]-construction in def. \ref{ConeAndMappingCylinder} provides a fibration resolution of $f$, in that

1. the composite morphism $Path(f) \overset{p_1^\ast f}{\longrightarrow} Path(Y) \overset{p_0}{\longrightarrow} Y$ is a fibration;

1. $f$ factors through this morphism by a weak equivalence right inverse to an acyclic fibration:

   $$
     f
       \;\colon\;
     X
       \underset{\in W}{\longrightarrow}
     Path(f)
        \underoverset{\in Fib}{p_0 \circ p_1^\ast f}{\longrightarrow}
     Y
     \,,
   $$

=--

+-- {: .proof #ProofOfFactorizationLemma}
###### Proof

We discuss the second case. The first case is [[formal dual|formally dual]].

So consider the [[mapping cocylinder]]-construction from prop. \ref{ConeAndMappingCylinder}

$$
  \array{
     Path(f) &\overset{\in W \cap Fib}{\longrightarrow}& X
     \\
     {}^{\mathllap{p_1^\ast f}}\downarrow &(pb)& \downarrow^{\mathrlap{f}}
     \\
     Path(Y) &\underoverset{\in W \cap Fib}{p_1}{\longrightarrow}& Y
     \\
     {}^{\mathllap{\in W \cap Fib}}\downarrow^{\mathrlap{p_0}}
     \\
     Y
  }
  \,.
$$


To see that the vertical composite is indeed a fibration, notice that, by the [[pasting law]], the above pullback diagram may be decomposed as a [[pasting]] of two pullback diagram as follows

$$
  \array{
    Path(f)
     &\underoverset{\in Fib}{(f,id)^\ast(p_1,p_0)}{\longrightarrow}&
     X \times Y
     &\stackrel{pr_1}{\to}&
     X
     \\
     \downarrow && \downarrow^{\mathrlap{(f, Id)}} && \downarrow^\mathrlap{f}
     \\
     Path(Y) &\overset{(p_1,p_0) \in Fib }{\longrightarrow}&
     Y \times Y &\stackrel{pr_1}{\longrightarrow}&
     Y
     \\
     {}^{\mathllap{p_0}}\downarrow & \swarrow_{\mathrlap{pr_2 \atop {\in Fib}}}
     \\
     Y
  }
  \,.
$$

Both squares are pullback squares. Since pullbacks of fibrations are fibrations by prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}, the morphism $Path(f) \to X \times Y$ is a fibration.
Similarly, since $X$ is fibrant, also the [[projection]] map $X \times Y \to Y$ is a fibration (being the pullback of $X \to \ast$ along $Y \to \ast$).

Since the vertical composite is thereby exhibited as the composite of two fibrations

$$
   Path(f)
     \overset{(f,id)^\ast(p_1,p_0)}{\longrightarrow}
   X \times Y
     \stackrel{pr_2 \circ (f ,Id) = pr_2}{\longrightarrow}
  Y
  \,,
$$

it is itself a fibration.

Then to see that there is a weak equivalence as claimed:

The [[universal property]] of the [[pullback]] $Path(f)$ induces a right inverse of $Path(f) \to X$ fitting into this diagram

$$
  \array{
     id_X \colon & X &\underoverset{\in W}{\exists}{\longrightarrow}
       & Path(f)
       &
         \overset{\in W \cap Fib}{\longrightarrow}&
       X
     \\
     & {}^{\mathrlap{f}}\downarrow && \downarrow && \downarrow^{\mathrlap{f}}
     \\
     id_Y\colon& Y
       &\underoverset{\in W}{i}{\longrightarrow}&
     Path(Y)
       &\stackrel{p_1}{\to}& Y
     \\
     & & {}_{\mathllap{Id}}\searrow& \downarrow^{\mathrlap{p_0}}
     \\
     & && Y
  }
  \,,
$$

which is a weak equivalence, as indicated, by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

This establishes the claim.

=--





### Categories of fibrant objects

[Below](#HomotopyFibers) we discuss the homotopy-theoretic properties of the [[mapping cone]]- and [[mapping cocone]]-constructions from [above](#MappingCones). Before we do so, we here establish a collection of general facts that hold in [[categories of fibrant objects]] and dually in [[categories of cofibrant objects]], def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}.

**Literature** ([Brown 73, section 4](#Brown73)).


+-- {: .num_lemma #ReplacementOfPathObjects}
###### Lemma

Let $f\colon X \longrightarrow Y$ be a morphism in a [[category of fibrant objects]], def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}. Then given any choice of [[path space objects]] $Path(X)$ and $Path(Y)$, def. \ref{PathAndCylinderObjectsInAModelCategory}, there is a replacement of $Path(X)$ by a path space object $\widetilde{Path(X)}$ along an acylic fibration, such that $\widetilde{Path(X)}$ has a morphism $\phi$ to $Path(Y)$ which is compatible with the structure maps, in that the following diagram commutes

$$
  \array{
    && X &\overset{f}{\longrightarrow}& Y
    \\
    &\swarrow& \downarrow && \downarrow
    \\
    Path(X) &\underset{\in W \cap Fib}{\longleftarrow}& \widetilde{Path(X)} &\overset{\phi}{\longrightarrow}& Path(Y)
    \\
    &{}_{\mathllap{(p^X_0,p^X_1)}}\searrow& \downarrow^{\mathrlap{(p^Y_0,p^Y_1)}} && \downarrow^{\mathrlap{(\tilde p^X_0,\tilde p^X_1)}}
    \\
    && X \times X &\overset{(f,f)}{\longrightarrow}& Y \times Y
  }
  \,.
$$

=--

([Brown 73, section 2, lemma 2](#Brown73))

+-- {: .proof}
###### Proof

Consider the [[commuting square]]

$$
  \array{
    X &\overset{f}{\longrightarrow}& Y &\longrightarrow& Path(Y)
    \\
    \downarrow &&  && \downarrow^{\mathrlap{(p_0^Y, p_1^Y)}}
    \\
    Path(X) &\overset{(p^X_0,p^X_1)}{\longrightarrow}& X \times X
    &\overset{(f,f)}{\longrightarrow}& Y \times Y
  }
  \,.
$$

Then consider its factorization  through the [[pullback]] of the right morphism along the bottom morphism,

$$
  \array{
    X &\longrightarrow& (f \circ p_0^X, f\circ p_1^X)^\ast Path(Y) &\longrightarrow& Path(Y)
    \\
    &{}_{\mathllap{\in W}}\searrow& \downarrow^{\mathrlap{\in W \cap Fib}} && \downarrow^{\mathrlap{(p_0^Y, p_1^Y)}}_{\mathrlap{\in Fib}}
    \\
    && Path(X) &\overset{(f \circ p_0^X, f\circ p_1^X)}{\longrightarrow}& Y \times Y
  }
  \,.
$$


Finally use the [[factorization lemma]] \ref{FactorizationLemma} to factor the morphism $X \to (f \circ p_0^X, f\circ p_1^X)^\ast Path(Y)$ through a weak equivalence followed by a fibration, the object this factors through serves as the desired path space resolution

$$
  \array{
    X &\overset{\in W}{\longrightarrow}& \widetilde{Path(X)} &\longrightarrow& Path(Y)
    \\
    &{}_{\mathllap{\in W}}\searrow& \downarrow^{\mathrlap{\in W \cap Fib}} && \downarrow^{\mathrlap{(p_0^Y, p_1^Y)}}
    \\
    && Path(X) &\overset{(f \circ p_0^X, f\circ p_1^X)}{\longrightarrow}& Y \times Y
  }
  \,.
$$


=--


+-- {: .num_lemma #BaseChangePreservesFibrationsAndWeakEquivalences}
###### Lemma

In a [[category of fibrant objects]] $\mathcal{C}_f$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}, let

$$
 \array{
  A_1 &&\stackrel{f}{\longrightarrow}&& A_2
  \\
  & {}_{\in Fib}\searrow && \swarrow_{\in Fib}
  \\
  && B
 }
$$

be a morphism over  some object $B$ in $\mathcal{C}_f$
and let $u \colon B' \to B$ be any morphism in
$\mathcal{C}_f$. Let

$$
 \array{
  u^*A_1 &&\stackrel{u^* f}{\longrightarrow}&& u^* A_2
  \\
  & {}_{\in Fib}\searrow && \swarrow_{\in Fib}
  \\
  && B'
 }
$$

be the corresponding morphism pulled back along $u$.

Then

* if $f$ is a fibration then also $u^* f$ is a fibration;

* if $f$ is a weak equivalence then also $u^* f$ is a weak equivalence.


=--

([Brown 73, section 4, lemma 1](#Brown73))


+-- {: .num_proof}
###### Proof

For $f \in Fib$ the statement follows from the [[pasting law]] which says that if in

$$
  \array{
    B' \times_B A_1 &\longrightarrow& A_1
    \\
    \;\;\downarrow^{\mathrlap{u^* f \in Fib}}
    && \;\;\downarrow^{\mathrlap{f \in Fib}}
    \\
    B' \times_B A_2 &\longrightarrow& A_2
    \\
    \;\downarrow^{\mathrlap{\in Fib}} && \;\downarrow^{\mathrlap{\in Fib}}
    \\
    B' &\stackrel{u}{\longrightarrow}& B
  }
$$

the bottom and the total square are pullback squares, then so is the top square. The same reasoning applies for $f \in W \cap Fib$.

Now to see the case that $f\in W$:

Consider the [[full subcategory]] $(\mathcal{C}_{/B})_f$ of the [[slice category]] $\mathcal{C}_{/B}$ (def. \ref{SliceCategory}) on its fibrant objects, i.e. the full subcategory of the slice category on the fibrations

$$
  \array{
    X
    \\
    \downarrow^{\mathrlap{p}}_{\mathrlap{\in Fib}}
    \\
    B
  }
$$

into $B$. By factorizing for every such fibration the [[diagonal morphisms]] into the [[fiber product]] $X \underset{B}{\times} X$ through a weak equivalence followed by a fibration, we obtain path space objects $Path_B(X)$ relative to $B$:

$$
  \array{
   (\Delta_X)/B
   \;\colon
    &
    X
      &\overset{\in W}{\longrightarrow}&
    Path_B(X)
      &\overset{\in Fib}{\longrightarrow}&
    X \underset{B}{\times} X
    \\
    & & {}_{\mathllap{\in Fib}}\searrow & \downarrow & \swarrow_{\mathrlap{\in Fib}}
    \\
    & && B
  }
  \,.
$$

With these, the [[factorization lemma]] (lemma \ref{FactorizationLemma}) applies in $(\mathcal{C}_{/B})_f$.

(Notice that for this we do need the restriction of $\mathcal{C}_{/B}$ to the fibrations, because this ensures that the projections $p_i \colon X_1 \times_B X_2 \to X_i$ are still fibrations, which is used in the proof of the factorization lemma ([here](#ProofOfFactorizationLemma)).)

So now given any

$$
  \array{
    X && \underoverset{\in W}{f}{\longrightarrow} && Y
    \\
    & {}_{\mathllap{\in Fib}}\searrow && \swarrow_{\mathrlap{\in Fib}}
    \\
    && B
  }
$$

apply the [[factorization lemma]] in $(\mathcal{C}_{/B})_f$ to factor it as

$$
  \array{
    X
      &\overset{i \in W}{\longrightarrow}&
    Path_B(f)
      &\overset{\in W \cap Fib}{\longrightarrow}& Y
    \\
    & {}_{\mathllap{\in Fib}}\searrow
     &\downarrow&
    \swarrow_{\mathrlap{\in Fib}}
    \\
    && B
  }
  \,.
$$

By the previous discussion it is sufficient now to show that the base change of $i$ to $B'$ is still a weak equivalence. But by the factorization lemma in $(\mathcal{C}_{/B})_f$, the morphism $i$ is right inverse to another acyclic fibration over $B$:

$$
  \array{
    id_X
    \;\colon
    &
    X
      &\overset{i \in W}{\longrightarrow}&
    Path_B(f)
      &\overset{\in W \cap Fib}{\longrightarrow}& X
    \\
    & &
    {}_{\mathllap{\in Fib}}\searrow
     &\downarrow&
    \swarrow_{\mathrlap{\in Fib}}
    \\
    & && B
  }
  \,.
$$

(Notice that if we had applied the factorization lemma of $\Delta_X$ in $\mathcal{C}_f$ instead of $(\Delta_X)/B$ in $(\mathcal{C}_{/B})$ then the corresponding triangle on the right here would not commute.)

Now we may reason as before: the base change of the top morphism here is exhibited by the following pasting composite of pullbacks:

$$
  \array{
    B' \underset{B}{\times} X
     &\longrightarrow&
    X
    \\
    \downarrow
      &(pb)&
    \downarrow
    \\
    B' \underset{B}{\times} Path_B(f)
      &\longrightarrow&
    Path_B(f)
    \\
    \downarrow
      &(pb)&
    \downarrow^{\mathrlap{\in W \cap Fib}}
    \\
    B' \underset{B}{\times}X
      &\longrightarrow&
    X
    \\
    \downarrow
      &(pb)&
    \downarrow
    \\
    B'
     &\longrightarrow&
    B
  }
  \,.
$$

The acyclic fibration $Path_B(f)$ is preserved by this pullback, as is the identity $id_X \colon X \to Path_B(X)\to X$. Hence the weak equivalence $X \to Path_B(X)$ is preserved by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

=--


+-- {: .num_lemma #InCfPullbackAlongFibrationPreservesWeakEquivalences}
###### Lemma

In a [[category of fibrant objects]], def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}, the pullback of a weak equivalence along a fibration is again a weak equivalence.

=--

([Brown 73, section 4, lemma 2](#Brown73))


+-- {: .proof}
###### Proof


Let
$u \colon B' \to B$ be a weak equivalence and
$ p \colon E \to B$ be a fibration. We want to show that the
left vertical morphism in the [[pullback]]

$$
  \array{
    E \times_B B' &\longrightarrow& B'
    \\
    \downarrow^{\mathrlap{\Rightarrow \in W} }
    && \;\downarrow^{\mathrlap{\in W}}
    \\
    E &\stackrel{\in Fib}{\longrightarrow}& B
  }
$$

is a weak equivalence.

First of all, using the [[factorization lemma]] \ref{FactorizationLemma}
we may factor $B' \to B$ as

$$
  B'
    \stackrel{\in W}{\longrightarrow}
  Path(u)
   \stackrel{\in W \cap F}{\longrightarrow}
  B
$$

with the first morphism a weak equivalence that is a right inverse to an acyclic fibration and the right one an acyclic fibration.

Then the pullback diagram in question may be decomposed
into two consecutive pullback diagrams

$$
  \array{
    E \times_B B' &\to& B'
    \\
    \downarrow && \downarrow
    \\
    Q &\stackrel{\in Fib}{\to}& Path(u)
    \\
    \;\;\downarrow^{\mathrlap{\in W \cap Fib}}
    && \;\;\downarrow^{\mathrlap{\in W \cap Fib}}
    \\
    E &\stackrel{\in Fib}{\longrightarrow}& B
  }
  \,,
$$

where the morphisms are indicated as fibrations and
acyclic fibrations using the stability of these
under arbitrary pullback.

This means that the proof reduces to proving that weak equivalences
$u : B' \stackrel{\in W}{\to} B$
that are right inverse to some acyclic fibration
$v : B \stackrel{\in W \cap F}{\to} B'$
map to a weak equivalence under pullback along a fibration.

Given such $u$ with right inverse $v$, consider the pullback diagram


$$
  \array{
    & E
    \\
    &
    {}^{\mathllap{{(p,id)}\atop \in W}}\downarrow
    &
      \searrow^{\mathrlap{id}}
    \\
    E_1 \coloneqq
      &
    B \times_{B'} E
      &
    \stackrel{\in W \cap Fib }{\longrightarrow}
      &
    E
    \\
    & \downarrow^{\mathrlap{\in Fib}} && \downarrow^{\mathrlap{p \in Fib }}
    \\
    & &(pb)& B
    \\
    & \downarrow && \downarrow^{\mathrlap{v \in W \cap Fib}}
    \\
    & B &\overset{v \in Fib \cap W}{\longrightarrow}& B'
  }
  \,.
$$

Notice that the indicated universal morphism  $p \times Id \colon E \stackrel{\in W}{\to} E_1$  into the pullback is a weak equivalence by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

The previous lemma \ref{BaseChangePreservesFibrationsAndWeakEquivalences} says that weak equivalences between fibrations over $B$ are themselves preserved by base extension along $u \colon B' \to B$. In total this yields the following diagram


$$
  \array{
    &&
    u^* E = B' \times_B E
      &\longrightarrow &
    E
    \\
    &&
    {}^{\mathllap{ {u^*(p \times Id)} \atop {\in W} }}\downarrow
      &&
    {}^{\mathllap{ {p \times Id} \atop {\in W}  }}\downarrow
     &
    \searrow^{\mathrlap{id}}
    \\
    &&
    u^* E_1
      &\longrightarrow&
    E_1
      &\stackrel{\in W \cap Fib}{\longrightarrow}&
    E
    \\
    &&\downarrow^{\mathrlap{\in Fib}}&&\downarrow^{\mathrlap{\in Fib}}
    && \downarrow^{\mathrlap{p \in Fib}}
    \\
    &&&&&& B
    \\
    &&\downarrow&&\downarrow && \downarrow^{\mathrlap{v \in W \cap Fib}}
    \\
    &&
    B'
      &\stackrel{u}{\longrightarrow}&
    B
      &\stackrel{v \in W \cap Fib}{\longrightarrow}&
    B'
  }
$$

so that with $p \times Id  : E \to E_1$ a weak equivalence also $u^* (p \times Id)$ is a weak equivalence, as indicated.

Notice that $u^* E = B' \times_B E \to E$ is the morphism that we want to show is a weak equivalence. By [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) for that it is now sufficient to show that $u^* E_1  \to E_1$ is a weak equivalence.

That finally follows now since, by assumption, the total bottom horizontal morphism is the identity. Hence so is the top horizontal morphism. Therefore $u^\ast E_1  \to E_1$ is right inverse to a weak equivalence, hence is a weak equivalence.

=--

+-- {: .num_lemma #UniquenessOfFibersOfQualizedMorphismsInHoC}
###### Lemma

Let $(\mathcal{C}^{\ast/})_f$ be a [[category of fibrant objects]], def. \ref{FullSubcategoriesOfFibrantCofibrantObjects} in a [[slice model structure|model structure on pointed objects]] (prop. \ref{ModelStructureOnSliceCategory}). Given any [[commuting diagram]] in $\mathcal{C}^{}$ of the form

$$
  \array{
    X'_1 &\underoverset{t}{\in W}{\longrightarrow}& X_1 &\stackrel{\overset{f}{\longrightarrow}}{\underset{g}{\longrightarrow}}& X_2
    \\
    && \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in Fib}}
      &&
    \downarrow^{\mathrlap{p_2}}_{\mathrlap{\in Fib}}
    \\
    && B &\overset{u}{\longrightarrow}& C
  }
$$

(meaning: both squares commute and $t$ equalizes $f$ with $g$) then the [[localization]] functor $\gamma \colon (\mathcal{C}^{\ast/})_f \to Ho(\mathcal{C}^{\ast/})$ (def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}, cor \ref{HomotopyCategoryOfSubcategoriesOfModelCategoriesOnGoodObjects}) takes the morphisms $fib(p_1) \stackrel{\longrightarrow}{\longrightarrow} fib(p_2)$ induced by $f$ and $g$ on [[fibers]] (example \ref{FiberAndCofiberInPointedObjects})  to the same morphism, in the homotopy category.

=--

([Brown 73, section 4, lemma 4](#Brown73))

+-- {: .proof}
###### Proof

First consider the pullback of $p_2$ along $u$: this forms the same kind of diagram but with the bottom morphism an identity. Hence it is sufficient to consider this special case.

Consider the [[full subcategory]] $(\mathcal{C}^{\ast/}_{/B})_f$ of the [[slice category]] $\mathcal{C}^{\ast/}_{/B}$ (def. \ref{SliceCategory}) on its fibrant objects, i.e. the full subcategory of the slice category on the fibrations

$$
  \array{
    X
    \\
    \downarrow^{\mathrlap{p}}_{\mathrlap{\in Fib}}
    \\
    B
  }
$$

into $B$. By factorizing for every such fibration the [[diagonal morphisms]] into the [[fiber product]] $X \underset{B}{\times} X$ through a weak equivalence followed by a fibration, we obtain path space objects $Path_B(X)$ relative to $B$:

$$
  \array{
   (\Delta_X)/B
   \;\colon
    &
    X
      &\overset{\in W}{\longrightarrow}&
    Path_B(X)
      &\overset{\in Fib}{\longrightarrow}&
    X \underset{B}{\times} X
    \\
    & & {}_{\mathllap{\in Fib}}\searrow & \downarrow & \swarrow_{\mathrlap{\in Fib}}
    \\
    & && B
  }
  \,.
$$

With these, the [[factorization lemma]] (lemma \ref{FactorizationLemma}) applies in $(\mathcal{C}^{\ast/}_{/B})_f$.

Let then $X\overset{s}{\to}Path_B(X_2)\overset{(p_0,p_1)}{\to} X_2 \times_B X_2$ be a [[path space object]] for $X_2$ in the slice over $B$ and consider the following commuting square

$$
  \array{
    X'_1 &\overset{s f t}{\longrightarrow}& Path_B(X_2)
    \\
    {}^{\mathllap{t}}_{\mathllap{\in W}}\downarrow && \downarrow^{\mathrlap{(p_0,p_1)}}_{\mathrlap{\in Fib}}
    \\
    X_1 &\overset{(f,g)}{\longrightarrow}& X_2\underset{B}{\times} X_2
  }
  \,.
$$

By factoring this through the pullback $(f,g)^\ast(p_0,p_1)$ and then applying the [[factorization lemma]] \ref{FactorizationLemma} and then [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) to the factoring morphisms, this may be replaced by a commuting square of the same form, where however the left morphism is an acyclic fibration

$$
  \array{
    X''_1 &\overset{}{\longrightarrow}& Path_B(X_2)
    \\
    {}^{\mathllap{t}}_{\mathllap{\in W\cap Fib}} \downarrow && \downarrow^{\mathrlap{(p_0,p_1)}}_{\mathrlap{\in Fib}}
    \\
    X_1 &\overset{(f,g)}{\longrightarrow}& X_2\underset{B}{\times} X_2
  }
  \,.
$$

This makes also the morphism $X''_1 \to B$ be a fibration, so that the whole diagram may now be regarded as a diagram in the category of fibrant objects $(\mathcal{C}_{/B})_f$ of the [[slice category]] over $B$.

As such, the top horizontal morphism now exhibits a [[right homotopy]] which under [[localization]] $\gamma_B \;\colon\; (\mathcal{C}_{/B})_f \longrightarrow Ho(\mathcal{C}_{/B})$ (def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}) of the [[slice model structure]] (prop. \ref{ModelStructureOnSliceCategory}) we have

$$
  \gamma_B(f) = \gamma_B(g)
  \,.
$$

The result then follows by observing that we have a commuting square of [[functors]]

$$
  \array{
     (\mathcal{C}^{\ast/}_{/B})_f &\overset{fib}{\longrightarrow}& \mathcal{C}^{\ast/}
     \\
     \downarrow^{\mathrlap{\gamma_B}} &\swArrow& \downarrow^{\mathrlap{\gamma}}
     \\
     Ho(\mathcal{C}^{\ast/}_{/B}) &\longrightarrow& Ho(\mathcal{C}^{\ast/})
  }
  \,,
$$

because, by lemma \ref{BaseChangePreservesFibrationsAndWeakEquivalences}, the top and right composite sends weak equivalences to isomorphisms, and hence the bottom filler exists by theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory}. This implies the claim.

=--






### Homotopy fibers
 {#HomotopyFibers}

We now discuss the homotopy-theoretic properties of the [[mapping cone]]- and [[mapping cocone]]-constructions from [above](#MappingCones).

**Literature** ([Brown 73, section 4](#Brown73)).

+-- {: .num_remark}
###### Remark

The [[factorization lemma]] \ref{FactorizationLemma} with prop. \ref{ConeAndMappingCylinder} says that the [[mapping cocone]] of a morphism $f$, def. \ref{MappingConeAndMappingCocone}, is equivalently the plain [[fiber]], example \ref{FiberAndCofiberInPointedObjects}, of a fibrant resolution $\tilde f$ of $f$:

$$
  \array{
    Path_\ast(f) &\longrightarrow& Path(f)
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{\tilde f}}
    \\
    \ast &\longrightarrow& Y
  }
  \,.
$$

=--

The following prop. \ref{FiberOfFibrationIsCompatibleWithWeakEquivalences} says that, up to equivalence, this situation is independent of the specific fibration resolution $\tilde f$ provided by the [[factorization lemma]] (hence by the prescription for the [[mapping cocone]]), but only depends on it being _some_ fibration resolution.


+-- {: .num_prop #FiberOfFibrationIsCompatibleWithWeakEquivalences}
###### Proposition

In the [[category of fibrant objects]] $(\mathcal{C}^{\ast/})_f$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}, of a [[slice model structure|model structure on pointed objects]] (prop. \ref{ModelStructureOnSliceCategory}) consider a morphism of [[fiber]]-diagrams, hence a [[commuting diagram]] of the form

$$
  \array{
    fib(p_1) &\longrightarrow& X_1 &\underoverset{\in Fib}{p_1}{\longrightarrow}& Y_1
    \\
    \downarrow^{\mathrlap{h}} && \downarrow^{\mathrlap{g}}
    && \downarrow^{\mathrlap{f}}
    \\
    fib(p_2) &\longrightarrow& X_2 &\underoverset{\in Fib}{p_2}{\longrightarrow}& Y_2
  }
  \,.
$$

If $f$ and $g$ weak equivalences, then so is $h$.

=--

+-- {: .proof}
###### Proof

Factor the diagram in question through the pullback of $p_2$ along $f$

$$
  \array{
    fib(p_1)
      &\longrightarrow&
    X_1
    \\
    \downarrow^{\mathrlap{h}}
      &&
    {}^{\mathllap{\in W}}\downarrow
      &
      \searrow^{\mathrlap{p_1}}
      &
    \\
    fib(f^\ast p_2)
      &\longrightarrow&
    f^\ast X_2
      &\underoverset{\in Fib}{f^\ast p_2}{\longrightarrow}&
    Y_1
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\in W}} && \downarrow^{\mathrlap{f}}_{\mathrlap{\in W}}
    \\
    fib(p_2) &\longrightarrow& X_2 &\underoverset{\in Fib}{p_2}{\longrightarrow}& Y_2
  }
$$

and observe that

1. $fib(f^\ast p_2) = pt^\ast f^\ast p_2 = pt^\ast p_2 = fib(p_2)$;

1. $f^\ast X_2 \to X_2$ is a weak equivalence by lemma \ref{InCfPullbackAlongFibrationPreservesWeakEquivalences};

1. $X_1 \to f^\ast X_2$ is a weak equivalence by assumption and by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences});

Moreover, this diagram exhibits $h \colon fib(p_1)\to fib(f^\ast p_2) = fib(p_2)$ as the base change, along $\ast \to Y_1$, of $X_1 \to f^\ast X_2$. Therefore the claim now follows with lemma \ref{BaseChangePreservesFibrationsAndWeakEquivalences}.

=--

Hence we say:

+-- {: .num_defn #HomotopyFiber}
###### Definition

Let $\mathcal{C}$ be a [[model category]] and $\mathcal{C}^{\ast/}$ its model category of [[pointed objects]], prop. \ref{ModelStructureOnSliceCategory}. For $f \colon X \longrightarrow Y$ any morphism in its [[category of fibrant objects]] $(\mathcal{C}^{\ast/})_f$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}, then its **[[homotopy fiber]]**

$$
  hofib(f)\longrightarrow X
$$

is the morphism in the [[homotopy category of a model category|homotopy category]] $Ho(\mathcal{C}^{\ast/})$, def. \ref{HomotopyCategoryOfAModelCategory}, which is represented by the [[fiber]], example \ref{FiberAndCofiberInPointedObjects}, of any fibration resolution $\tilde f$ of $f$ (hence any fibration $\tilde f$ such that $f$ factors through a weak equivalence followed by $\tilde f$).

Dually:

For $f \colon X \longrightarrow Y$ any morphism in its [[category of cofibrant objects]] $(\mathcal{C}^{\ast/})_c$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}, then its **[[homotopy cofiber]]**

$$
  Y \longrightarrow hocofib(f)
$$

is the morphism in the [[homotopy category of a model category|homotopy category]] $Ho(\mathcal{C})$, def. \ref{HomotopyCategoryOfAModelCategory}, which is represented by the [[cofiber]], example \ref{FiberAndCofiberInPointedObjects}, of any cofibration resolution of $f$ (hence any cofibration $\tilde f$ such that $f$ factors as $\tilde f$ followed by a weak equivalence).

=--

+-- {: .num_prop #HomotopyFiberIndependentOfChoiceOfFibrantReplacement}
###### Proposition

The homotopy fiber in def. \ref{HomotopyFiber} is indeed well defined, in that for $f_1$ and $f_2$ two fibration replacements of any morphisms $f$ in $\mathcal{C}_f$, then their fibers are isomorphic in $Ho(\mathcal{C}^{\ast/})$.

=--

+-- {: .proof}
###### Proof

It is sufficient to exhibit an isomorphism in $Ho(\mathcal{C}^{\ast/})$ from the fiber of the fibration replacement given by the [[factorization lemma]] \ref{FactorizationLemma} (for any choice of [[path space object]]) to the fiber of any other fibration resolution.

Hence given a morphism $f \colon Y \longrightarrow X$ and a factorization

$$
  f
  \;\colon\;
  X
    \underset{\in W}{\longrightarrow}
  \hat X
   \underoverset{f_1}{\in Fib}{\longrightarrow}
  Y
$$

consider, for any choice $Path(Y)$ of [[path space object]] (def. \ref{PathAndCylinderObjectsInAModelCategory}),  the diagram

$$
  \array{
    Path(f) &\overset{\in W \cap Fib}{\longrightarrow}& X
    \\
    {}^{\mathllap{\in W}}\downarrow
      &(pb)&
    \downarrow^{\mathrlap{\in W}}
    \\
    Path(f_1) &\overset{\in W \cap Fib}{\longrightarrow}& \hat X
    \\
    {}^{\mathllap{\in Fib}}\downarrow
      &(pb)&
    \downarrow^{\mathrlap{ {f_1} \atop {\in Fib}}}
    \\
    Path(Y) &\underoverset{\in W \cap Fib}{p_1}{\longrightarrow}& Y
    \\
    {}^{\mathllap{ {p_0} \atop \in W \cap Fib}}\downarrow
    \\
    Y
  }
$$

as in the proof of lemma \ref{FactorizationLemma}. Now by repeatedly using prop. \ref{FiberOfFibrationIsCompatibleWithWeakEquivalences}:

1. the bottom square gives a weak equivalence from the fiber of $Path(f_1) \to Path(Y)$ to the fiber of $f_1$;

1. The square

   $$
     \array{
        Path(f_1) &\overset{id}{\longrightarrow}& Path(f_1)
        \\
        \downarrow && \downarrow
        \\
        Path(Y) &\underset{p_0}{\longrightarrow}& Y
     }
   $$

   gives a weak equivalence from the fiber of $Path(f_1) \to Path(Y)$ to the fiber of $Path(f_1)\to Y$.

1. Similarly the total vertical composite gives a weak equivalence via

   $$
     \array{
        Path(f) &\overset{\in W}{\longrightarrow}& Path(f_1)
        \\
        \downarrow && \downarrow
        \\
        Y &\underset{id}{\longrightarrow}& Y
     }
   $$


from the fiber of $Path(f) \to Y$ to the fiber of $Path(f_1)\to Y$.

Together this is a [[zig-zag]] of weak equivalences of the form

$$
  fib(f_1)
    \;\overset{\in W}{\longleftarrow}\;
  fib(Path(f_1)\to Path(Y))
    \;\overset{\in W}{\longrightarrow}\;
  fib(Path(f_1)\to Y)
    \;\overset{\in W}{\longleftarrow}\;
  fib(Path(f) \to Y)
$$

between the fiber of $Path(f) \to Y$ and the fiber of $f_1$. This gives an isomorphism in the [[homotopy category of a model category|homotopy category]].

=--


+-- {: .num_example #FibersOfSerreFibrations}
###### Example
**(fibers of Serre fibrations)**

In showing that [[Serre fibrations]] are abstract fibrations in the sense of [[model category]] theory, theorem \ref{TopQuillenModelStructure} implies that the [[fiber]] $F$ (example \ref{FiberAndCofiberInPointedObjects}) of a [[Serre fibration]], def. \ref{SerreFibration}

$$
  \array{
    F &\longrightarrow& X
    \\
    && \downarrow^{\mathrlap{p}}
    \\
    && B
  }
$$

over any point is actually a [[homotopy fiber]] in the sense of def. \ref{HomotopyFiber}. With prop. \ref{FiberOfFibrationIsCompatibleWithWeakEquivalences} this implies that the [[weak homotopy type]] of the fiber only depends on the Serre fibration up to weak homotopy equivalence in that if $p' \colon X' \to B'$ is another Serre fibration fitting into a [[commuting diagram]] of the form

$$
  \array{
    X &\overset{\in W_{cl}}{\longrightarrow}& X'
    \\
    \downarrow^{\mathrlap{p}} && \downarrow^{\mathrlap{p'}}
    \\
    B &\overset{\in W_{cl}}{\longrightarrow}& B'
  }
$$

then $F \overset{\in W_{cl}}{\longrightarrow} F'$.

In particular this gives that the [[weak homotopy type]] of the fiber of a Serre fibration $p \colon X \to B$ does not change as the basepoint is moved in the same connected component. For let $\gamma \colon I \longrightarrow B$ be a path between two points

$$
  b_{0,1}
    \;\colon\;
  \ast
    \underoverset{\in W_{cl}}{i_{0,1}}{\longrightarrow}
  I
    \overset{\gamma}{\longrightarrow}
  B
  \,.
$$

Then since all objects in $(Top_{cg})_{Quillen}$ are fibrant, and since the endpoint inclusions $i_{0,1}$ are weak equivalences, lemma \ref{InCfPullbackAlongFibrationPreservesWeakEquivalences} gives the [[zig-zag]] of top horizontal weak equivalences in the following diagram:

$$
  \array{
    F_{b_0} = & b_0^\ast p
      &\overset{\in W_{cl}}{\longrightarrow}&
    \gamma^{\ast}p
      &\overset{\in W_{cl}}{\longleftarrow}&
    b_1^\ast p
    &
    = F_{b_1}
    \\
    & \downarrow &(pb)& \downarrow{\mathrlap{{\gamma^\ast f} \atop {\in \atop {Fib}}}} &\;\;(pb)& \downarrow
    \\
    & \ast
      &\underoverset{i_0}{\in W_{cl}}{\longrightarrow}&
    I
      &\underoverset{i_1}{\in W_{cl}}{\longleftarrow}&
    \ast
  }
$$

and hence an isomorphism $F_{b_0} \simeq F_{b_1}$ in the [[classical homotopy category]] (def. \ref{ClassicalHomotopyCategory}).

The same kind of argument applied to maps from the square $I^2$ gives that if $\gamma_1, \gamma_2\colon I \to B$ are two homotopic paths with coinciding endpoints, then the isomorphisms between fibers over endpoints which they induce are equal. (But in general the isomorphism between the fibers does depend on the choice of homotopy class of paths connecting the basepoints!)

The same kind of argument also shows that if $B$ has the structure of a [[cell complex]] (def. \ref{TopologicalCellComplex}) then the restriction of the Serre fibration to one cell $D^n$ may be identified in the homotopy category with  $D^n \times F$, and may be canonically identified so if the [[fundamental group]] of $X$ is trivial. This is used when deriving the [[Serre spectral sequence|Serre]]-[[Atiyah-Hirzebruch spectral sequence]] for $p$ ([prop.](Introduction+to+Stable+homotopy+theory+--+S#AHSSExistence)).

=--

+-- {: .num_example #StandardTopologicalMappingConeIsHomotopyCofiber}
###### Example

For every [[continuous function]] $f \colon X \longrightarrow Y$ between [[CW-complexes]], def. \ref{TopologicalCellComplex}, then the standard topological mapping cone is the [[attaching space]] (example \ref{PushoutInTop})

$$
  Y \cup_f Cone(X) \;\; \in Top
$$

of $Y$ with the standard cone $Cone(X)$ given by collapsing one end of the standard topological cyclinder $X \times I$ (def. \ref{TopologicalInterval}) as shown in example \ref{MappingConesInTopologicalSpaces}.

Equipped with the canonical continuous function

$$
  Y \longrightarrow Y \cup_f Cone(X)
$$

this represents the [[homotopy cofiber]], def. \ref{HomotopyFiber}, of $f$ with respect to the [[classical model structure on topological spaces]] $\mathcal{C}= Top_{Quillen}$ from theorem \ref{TopQuillenModelStructure}.

=--

+-- {: .proof}
###### Proof

By prop. \ref{TopologicalCylinderOnCWComplexIsGoodCylinderObject}, for $X$ a [[CW-complex]] then the standard topological cylinder object $X\times I$ is indeed a  cyclinder object in $Top_{Quillen}$. Therefore by prop. \ref{ConeAndMappingCylinder} and the [[factorization lemma]] \ref{FactorizationLemma}, the mapping cone construction indeed produces first a cofibrant replacement of $f$ and then the ordinary cofiber of that, hence a model for the homotopy cofiber.

=--

+-- {: .num_example}
###### Example

The [[homotopy fiber]] of the inclusion of [[classifying spaces]] $B O(n) \hookrightarrow B O(n+1)$ is the [[n-sphere]] $S^n$. See [this prop.](Introduction+to+Stable+homotopy+theory+--+S#HomotopyFiberOfInclusionOfConsecutiveClassifyingSpaces) at _[Classifying spaces and G-structure](Introduction+to+Stable+homotopy+theory+--+S#ClassifyingSpaces)_.

=--


+-- {: .num_example #FiberOfFibrationWeaklyEquivalentToFiberOfItsCocylinder}
###### Example

Suppose a morphism $f \colon X \longrightarrow Y$ already happens to be a fibration between fibrant objects. The [[factorization lemma]] \ref{FactorizationLemma} replaces it by a fibration out of the [[mapping cocylinder]] $Path(f)$, but such that the comparison morphism is a weak equivalence:

$$
  \array{
    fib(f) &\longrightarrow& X &\underoverset{\in Fib}{f}{\longrightarrow}& Y
    \\
    \downarrow^{\mathrlap{\in W}} && \downarrow^{\mathrlap{\in W}} && \downarrow^{\mathrlap{id}}
    \\
    fib(\tilde f) &\longrightarrow& Path(f) &\underoverset{\in Fib}{\tilde f}{\longrightarrow}& Y
  }
  \,.
$$

Hence by prop. \ref{FiberOfFibrationIsCompatibleWithWeakEquivalences} in this case the ordinary fiber of $f$ is weakly equivalent to the [[mapping cocone]], def. \ref{MappingConeAndMappingCocone}.

=--


We may now state the abstract version of the statement of prop. \ref{SerreFibrationGivesExactSequenceOfHomotopyGroups}:

+-- {: .num_prop #ExactSequenceOfHomotopyFiberAtOneStage}
###### Proposition

Let $\mathcal{C}$ be a [[model category]]. For $f \colon X \to Y$ any morphism of [[pointed objects]], and for $A$ a [[pointed object]], def. \ref{CategoryOfPointedObjects}, then the sequence

$$
  [A,hofib(f)]_\ast \overset{i_\ast}{\longrightarrow} [A,X]_\ast \overset{f_\ast}{\longrightarrow} [A,Y]_{\ast}
$$

is [[exact sequence|exact]] as a sequence of [[pointed sets]].

(Where the sequence here is the image of the [[homotopy fiber]] sequence of def. \ref{HomotopyFiber} under the hom-functor $[A,-]_\ast \;\colon\; Ho(\mathcal{C}^{\ast/}) \longrightarrow Set^{\ast/}$ from example \ref{HomotopyCategoryOfPointedModelStructureIsEnrichedInPointedSets}.)


=--

+-- {: .proof}
###### Proof

Let $A$, $X$ and $Y$ denote fibrant-cofibrant objects in $\mathcal{C}^{\ast/}$ representing the given objects of the same name in $Ho(\mathcal{C}^{\ast/})$. Moreover, let $f$ be a fibration in $\mathcal{C}^{\ast/}$ representing the given morphism of the same name in $Ho(\mathcal{C}^{\ast/})$.

Then by def. \ref{HomotopyFiber} and prop.
\ref{HomotopyFiberIndependentOfChoiceOfFibrantReplacement} there is a representative $hofib(f) \in \mathcal{C}$ of the homotopy fiber which fits into a pullback diagram of the form

$$
  \array{
    hofib(f) &\overset{i}{\longrightarrow}& X
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    \ast &\longrightarrow& Y
  }
$$

With this the hom-sets in question are represented by genuine morphisms in $\mathcal{C}^{\ast/}$, modulo homotopy. From this it follows immediately that $im(i_\ast)$ includes into $ker(f_\ast)$. Hence it remains to show the converse: that every element in $ker(f_\ast)$ indeed comes from $im(i_\ast)$.

But an element in $ker(f_\ast)$ is represented by a morphism $\alpha \colon A \to X$ such that there is a left homotopy as in the following diagram

$$
  \array{
     && A &\overset{\alpha}{\longrightarrow}& X
     \\
     && {}^{\mathllap{i_0}}\downarrow &{}^{\tilde \eta}\nearrow& \downarrow^{\mathrlap{f}}
     \\
     A &\overset{i_1}{\longrightarrow} & Cyl(A) &\overset{\eta}{\longrightarrow}& Y
     \\
     \downarrow && && \downarrow^{\mathrlap{=}}
     \\
     \ast && \longrightarrow && Y
  }
  \,.
$$

Now by lemma \ref{ComponentMapsOfCylinderAndPathSpaceInGoodSituation} the square here has a lift $\tilde \eta$, as shown. This means that $i_1 \circ\tilde \eta$ is left homotopic to $\alpha$. But by the universal property of the fiber, $i_1 \circ \tilde \eta$ factors through $i \colon hofib(f) \to X$.

=--

With prop. \ref{FiberOfFibrationIsCompatibleWithWeakEquivalences} it also follows notably that the loop space construction becomes well-defined on the homotopy category:

+-- {: .num_remark #ConcatenatedLoopSpaceObject}
###### Remark

Given an object $X \in \mathcal{C}^{\ast/}_f$, and picking any [[path space object]] $Path(X)$, def. \ref{PathAndCylinderObjectsInAModelCategory} with induced [[loop space object]] $\Omega X$, def. \ref{SuspensionAndLoopSpaceObject}, write $Path_2(X) = Path(X) \underset{X}{\times} Path(X)$ for the [[path space object]] given by the fiber product  of $Path(X)$ with itself, via example \ref{ComposedPathSpaceObjects}. From the pullback diagram there, the fiber inclusion $\Omega X \to Path(X)$ induces a morphism

$$
  \Omega X \times \Omega X \longrightarrow (\Omega X)_2
  \,.
$$

In the case where $\mathcal{C}^{\ast/} = Top^{\ast/}$ and $\Omega$ is induced, via def. \ref{SuspensionAndLoopSpaceObject}, from the standard path space object (def. \ref{TopologicalPathSpace}), i.e. in the case that

$$
  \Omega X = fib(Maps(I_+,X)_\ast \longrightarrow X \times X)
  \,,
$$

then this is the operation of concatenating two loops parameterized by $I = [0,1]$ to a single loop parameterized by $[0,2]$.

=--

+-- {: .num_prop #LoopingAsFunctorOnHomotopyCategory}
###### Proposition

Let $\mathcal{C}$ be a [[model category]], def. \ref{ModelCategory}. Then the construction of forming [[loop space objects]] $X\mapsto \Omega X$, def. \ref{SuspensionAndLoopSpaceObject} (which on $\mathcal{C}^{\ast/}_f$ depends on a choice of [[path space objects]], def. \ref{PathAndCylinderObjectsInAModelCategory}) becomes unique up to isomorphism in the [[homotopy category of a model category|homotopy category]] (def. \ref{HomotopyCategoryOfAModelCategory}) of the [[slice model structure|model structure on pointed objects]] (prop. \ref{ModelStructureOnSliceCategory}) and extends to a [[functor]]:

$$
  \Omega
    \;\colon\;
  Ho(\mathcal{C}^{\ast/})
    \longrightarrow
  Ho(\mathcal{C}^{\ast/})
  \,.
$$

Dually, the [[reduced suspension]] operation, def. \ref{SuspensionAndLoopSpaceObject}, which on $\mathcal{C}^{\ast/}$ depends on a choice of [[cylinder object]], becomes a functor on the homotopy category

$$
  \Sigma
   \;\colon\;
  Ho(\mathcal{C}^{\ast/})
    \longrightarrow
  Ho(\mathcal{C}^{\ast/})
  \,.
$$

Moreover, the pairing operation induced on the objects in the image of this functor via remark \ref{ConcatenatedLoopSpaceObject} (concatenation of loops) gives the objects in the image of $\Omega$ [[group object]] structure, and makes this functor lift as

$$
  \Omega
    \;\colon\;
  Ho(\mathcal{C}^{\ast/})
    \longrightarrow
  Grp(Ho(\mathcal{C}^{\ast/}))
  \,.
$$

=--

([Brown 73, section 4, theorem 3](#Brown73))

+-- {: .proof}
###### Proof


Given an object $X \in \mathcal{C}^{\ast/}$ and given two choices of path space objects $Path(X)$ and $\widetilde{Path(X)}$, we need to produce an isomorphism in $Ho(\mathcal{C}^{\ast/})$ between $\Omega X$ and $\tilde \Omega X$.

To that end, first lemma \ref{ReplacementOfPathObjects} implies that any two choices of path space objects are connected via a third path space by a [[span]] of morphisms compatible with the structure maps. By [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) every morphism of path space objects compatible with the inclusion of the base object is a weak equivalence. With this, lemma \ref{BaseChangePreservesFibrationsAndWeakEquivalences} implies that these morphisms induce weak equivalences on the corresponding loop space objects. This shows that all choices of loop space objects become isomorphic in the homotopy category.

Moreover, all the isomorphisms produced this way are actually equal: this follows from lemma \ref{UniquenessOfFibersOfQualizedMorphismsInHoC} applied to

$$
  \array{
     X &\overset{s}{\longrightarrow}& Path(X) &\stackrel{\longrightarrow}{\longrightarrow}& \widetilde{Path(X)}
     \\
     && \downarrow && \downarrow
     \\
     && X\times X &\overset{id}{\longrightarrow}&  X \times X
  }
  \,.
$$

This way we obtain a functor

$$
  \Omega \;\colon\; \mathcal{C}^{\ast/}_f \longrightarrow Ho(\mathcal{C}^{\ast/})
  \,.
$$

By prop. \ref{FiberOfFibrationIsCompatibleWithWeakEquivalences} (and using that Cartesian product preserves weak equivalences) this functor sends weak equivalences to isomorphisms. Therefore the functor on homotopy categories now follows with theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory}.

It is immediate to see that the operation of loop concatenation from remark \ref{ConcatenatedLoopSpaceObject} gives the objects $\Omega X \in Ho(\mathcal{C}^{\ast/})$ the structure of [[monoids]]. It is now sufficient to see that these are in fact groups:

We claim that the inverse-assigning operation is given by the left map in the following pasting composite

$$
  \array{
    \Omega' X &\longrightarrow& Path'(X) &\overset{}{\longrightarrow}& X \times X
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}} &(pb)& \downarrow^{\mathrlap{swap}}
    \\
    \Omega X &\longrightarrow& Path(X) &\underset{(p_0,p_1)}{\longrightarrow}& X \times X
  }
  \,,
$$

(where $Path'(X)$, thus defined, is the path space object obtained from $Path(X)$ by "reversing the notion of source and target of a path").

To see that this is indeed an inverse, it is sufficient to see that the two morphisms

$$
  \Omega X \stackrel{\longrightarrow}{\longrightarrow} (\Omega X)_2
$$

induced from

$$
  \array{
  Path(X)
\stackrel{\overset{\Delta}{\longrightarrow}}{\underset{(s\circ p_0,s \circ p_0)}{\longrightarrow}}
  Path(X) \times_X Path'(X)
 }
$$

coincide in the homotopy category. This follows with lemma \ref{UniquenessOfFibersOfQualizedMorphismsInHoC} applied to the following commuting diagram:

$$
  \array{
    X
      &\overset{i}{\longrightarrow}&
    Path(X)
      &\stackrel{\overset{\Delta}{\longrightarrow}}{\underset{(s\circ p_0,s \circ p_0)}{\longrightarrow}}&
    Path(X)\times_X Path'(X)
    \\
    && {}^{\mathllap{(p_0,p_1)}}\downarrow && \downarrow^{\mathrlap{}}
    \\
    && X\times X &\overset{\Delta \circ pr_1}{\longrightarrow}& X \times X
  }
  \,.
$$


=--





### Homotopy pullbacks
 {#HomotopyPullbacks}

The concept of [[homotopy fibers]] of def. \ref{HomotopyFiber} is a special case of the more general concept of [[homotopy pullbacks]].

+-- {: .num_defn #RightProperModelCategory}
###### Definition

A [[model category]] $\mathcal{C}$ (def. \ref{ModelCategory}) is called a **[[right proper model category]]** if [[pullback]] along fibrations preserves weak equivalences.

=--

+-- {: .num_example}
###### Example

By lemma \ref{InCfPullbackAlongFibrationPreservesWeakEquivalences}, a [[model category]] $\mathcal{C}$ (def. \ref{ModelCategory}) in which all objects are fibrant is a [[right proper model category]] (def. \ref{RightProperModelCategory}).

=--


+-- {: .num_defn #HomotopyPullback}
###### Definition

Let $\mathcal{C}$ be a [[right proper model category]] (def. \ref{RightProperModelCategory}). Then a [[commuting square]]

$$
  \array{
    A &\longrightarrow& B
    \\
    \downarrow && \downarrow^{\mathrlap{g}}
    \\
     C &\underset{f}{\longrightarrow}& D
  }
$$

in $\mathcal{C}_f$ is called a **[[homotopy pullback]]** (of $f$ along $g$ and equivalently of $g$ along $f$) if the following equivalent conditions hold:

1. for some factorization of the form

   $$
     g \colon B \overset{\in W }{\longrightarrow} \hat B \overset{\in Fib}{\longrightarrow} D
   $$

   the universally induced morphism from $A$ into the pullback of $\hat B$ along $f$ is a weak equivalence:

   $$
     \array{
       A &\longrightarrow& B
       \\
       {}^{\mathllap{\in W}}\downarrow && \downarrow^{\mathrlap{\in W}}
       \\
       C \underset{D}{\times} \hat B
        &\longrightarrow&
       \hat B
       \\
       \downarrow &(pb)& \downarrow^{\mathrlap{\in Fib}}
       \\
       C &\longrightarrow& D
     }
     \,.
   $$


1. for some factorization of the form

   $$
     f \colon C \overset{\in W }{\longrightarrow} \hat C \overset{\in Fib}{\longrightarrow} D
   $$

   the universally induced morphism from $A$ into the pullback of $\hat D$ along $g$ is a weak equivalence:

   $$
     A \overset{\in W}{\longrightarrow} \hat C \underset{D}{\times} B
     \,.
   $$

1. the above two conditions hold for every such factorization.

=--

(e.g. [Goerss-Jardine 96, II (8.14) ](Simplicial+homotopy+Theory))


+-- {: .num_prop #ConditionsForHomotopyPullbackAreIndeedEquivalent}
###### Proposition

The conditions in def. \ref{HomotopyPullback} are indeed equivalent.

=--

+-- {: .proof}
###### Proof

First assume that the first condition holds, in that

$$
  \array{
    A &\longrightarrow& B
    \\
    {}^{\mathllap{\in W}}\downarrow && \downarrow^{\mathrlap{\in W}}
    \\
    C \underset{D}{\times} \hat B
     &\longrightarrow&
    \hat B
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{\in Fib}}
    \\
    C &\longrightarrow& D
  }
  \,.
$$

Then let

$$
  f \colon C \overset{\in W }{\longrightarrow} \hat C \overset{\in Fib}{\longrightarrow} D
$$

be any factorization of $f$ and consider the [[pasting]] diagram (using the [[pasting law]] for pullbacks)

$$
  \array{
    A
      &\overset{}{\longrightarrow}&
    \hat C \underset{D}{\times} B
      &\longrightarrow&
    B
    \\
    {}^{\mathllap{\in W}}\downarrow
      &&
    \downarrow^{\mathrlap{\in W}}
      &(pb)&
    \downarrow^{\mathrlap{\in W}}
    \\
    C\underset{D}{\times} \hat B
      &\overset{\in W}{\longrightarrow}&
    \hat C \underset{D}{\times} \hat D
      &\overset{\in Fib}{\longrightarrow}&
    \hat B
    \\
    \downarrow
      &(pb)&
    \downarrow^{\mathrlap{\in \atop Fib}}
      &(pb)&
    \downarrow^{\mathrlap{\in Fib}}
    \\
    C
      &\underset{\in W}{\longrightarrow}&
    \hat C
      &\underset{\in Fib}{\longrightarrow}&
    D
  }
  \,,
$$

where the inner morphisms are fibrations and weak equivalences, as shown, by the pullback stability of fibrations (prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}) and then since pullback along fibrations preserves weak equivalences by assumption of [[right proper model category|right properness]] (def. \ref{RightProperModelCategory}).
Hence it follows by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) that also the comparison morphism $A \to \hat C \underset{D}{\times} B$ is a weak equivalence.

In conclusion, if the homotopy pullback condition is satisfied for one factorization of $g$, then it is satisfied for all factorizations of $f$. Since the argument is symmetric in $f$ and $g$, this proves the claim.

=---

+-- {: .num_remark #PullbackOfFibrationWithFibrantObjectsIsHomotopyPullback}
###### Remark

In particular, an ordinary pullback square of fibrant objects, one of whose edges is a fibration, is a homotopy pullback square according to def. \ref{HomotopyPullback}.

=--



+-- {: .num_prop #HomotopyPullbackPreservesWeakEquivalencesOfSpans}
###### Proposition

Let $\mathcal{C}$ be a [[right proper model category]] (def. \ref{RightProperModelCategory}). Given a [[diagram]] in $\mathcal{C}$ of the form

$$
  \array{
    A &\longrightarrow& B &\overset{\in Fib}{\longleftarrow}& C
    \\
    \downarrow^{\mathrlap{\in W}}
      &&
    \downarrow^{\mathrlap{\in W}}
      &&
    \downarrow^{\mathrlap{\in W}}
    \\
    D &\longrightarrow& E &\underset{\in Fib}{\longleftarrow}& F
  }
$$

then the induced morphism on [[pullbacks]] is a weak equivalence

$$
  A \underset{B}{\times} C
   \overset{\in W}{\longrightarrow}
  D \underset{E}{\times} F
  \,.
$$

=--

+-- {: .proof}
###### Proof

(The reader should draw the 3-dimensional cube diagram which we describe in words now.)

First consider the universal morphism $C \to E \underset{F}{\times} C$ and observe that it is a weak equivalence by [[right proper model category|right properness]] (def. \ref{RightProperModelCategory})
and [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

Then consider the universal morphism $A \underset{B}{\times}C \to A \underset{B}{\times}(E \underset{F}{\times}C)$ and observe that this is also a weak equivalence, since $A \underset{B}{\times} C$ is the limiting cone of a homotopy pullback square by remark \ref{PullbackOfFibrationWithFibrantObjectsIsHomotopyPullback}, and since the morphism is the comparison morphism to the pullback of the factorization constructed in the first step.

Now by using the [[pasting law]], then the commutativity of the "left" face of the cube, then the pasting law again, one finds that $A \underset{B}{\times} (E \underset{F}{\times} C) \simeq A \underset{D}{\times} (D \underset{E} F{\times})$. Again by [[right proper model category|right properness]] this implies that $A \underset{B}{\times} (E \underset{F}{\times} C)\to D \underset{E}{\times} F$ is a weak equivalence.

With this the claim follows by [[two-out-of-three]].

=--



Homotopy pullbacks satisfy the usual abstract properties of pullbacks:

+-- {: .num_prop #HomotopyPullbackOfWeakEquivalences}
###### Proposition

Let $\mathcal{C}$ be a [[right proper model category]] (def. \ref{RightProperModelCategory}).
If in a [[commuting square]] in $\mathcal{C}$ one edge is a weak equivalence, then the square is a [[homotopy pullback]] square precisely if the opposite edge is a weak equivalence, too.

=--

+-- {: .proof}
###### Proof

Consider a commuting square of the form

$$
  \array{
    A &\longrightarrow& B
    \\
    \downarrow && \downarrow
    \\
    C &\underset{\in W}{\longrightarrow}& D
  }
  \,.
$$

To detect whether this is a homotopy pullback, by def. \ref{HomotopyPullback} and prop. \ref{ConditionsForHomotopyPullbackAreIndeedEquivalent}, we are to choose any factorization of the right vertical morphism to obtain the pasting composite

$$
  \array{
    A &\longrightarrow& B
    \\
    \downarrow && \downarrow^{\mathrlap{\in W}}
    \\
    C \underset{D}{\times} \hat B
      &\overset{\in W}{\longrightarrow}&
    \hat B
    \\
    \downarrow
      &(pb)&
    \downarrow^{\mathrlap{\in Fib}}
    \\
    C &\underset{\in W}{\longrightarrow}& D
  }
  \,.
$$

Here the morphism in the middle is a weak equivalence by [[right proper model category|right properness]] (def. \ref{RightProperModelCategory}). Hence it follows by [[two-out-of-three]] that the top left comparison morphism is a weak equivalence (and so the original square is a homotopy pullback) precisely if the top morphism is a weak equivalence.

=--

+-- {: .num_prop #ClosurePropertiesOfHomotopyPullbacks}
###### Proposition

Let $\mathcal{C}$ be a [[right proper model category]] (def. \ref{RightProperModelCategory}).

1. ([[pasting law]]) If in a [[commuting diagram]]

   $$
     \array{
       A &\longrightarrow& B &\longrightarrow& C
        \\
        \downarrow
          &&
       \downarrow
          &&
        \downarrow
        \\
        D &\longrightarrow& E &\underset{}{\longrightarrow}& F
      }
   $$

   the square on the right is a homotoy pullback (def. \ref{HomotopyPullback}) then the left square is, too, precisely if the total rectangle is;

1. in the presence of [[functorial factorization]] (def. \ref{FunctorialFactorization}) through weak equivalences followed by fibrations:

   every [[retract]] of a homotopy pullback square (in the category $\mathcal{C}_f^{\Box}$ of commuting squares in $\mathcal{C}_f$) is itself a homotopy pullback square.

=--

+-- {: .proof}
###### Proof

For the first statement: choose a factorization of $C \overset{\in W}{\to} \hat F \overset{\in Fib}{\to} F$, pull it back to a factorization $B \to \hat B \overset{\in Fib}{\to} E$ and assume that $B \to \hat B$ is a weak equivalence, i.e. that the right square is a homotopy pullback. Now use the ordinary [[pasting law]] to conclude.


For the second statement: functorially choose a factorization of the two right vertical morphisms of the squares and factor the squares through the pullbacks of the corresponding fibrations along the bottom morphisms, respectively. Now the statement that the squares are homotopy pullbacks is equivalent to their top left vertical morphisms being weak equivalences. Factor these top left morphisms functorially as cofibrations followed by acyclic fibrations. Then the statement that the squares are homotopy pullbacks is equivalent to those top left cofibrations being acyclic. Now the claim follows using that the retract of an acyclic cofibration is an acyclic cofibration (prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}).

=--





### Long sequences
 {#LongSequences}

The ordinary [[fiber]], example \ref{FiberAndCofiberInPointedObjects}, of a morphism has the property that taking it _twice_ is always trivial:

$$
   \ast \simeq fib(fib(f)) \longrightarrow fib(f) \longrightarrow X \overset{f}{\longrightarrow} Y
  \,.
$$

This is crucially different for the [[homotopy fiber]], def. \ref{HomotopyFiber}. Here we discuss how this comes about and what the consequences are.

+-- {: .num_prop #HomotopyFiberOfHomotopyFiberIsLooping}
###### Proposition

Let $\mathcal{C}_f$ be a [[category of fibrant objects]] of a [[model category]], def. \ref{FullSubcategoriesOfFibrantCofibrantObjects} and let $f \colon X \longrightarrow Y$ be a morphism in its [[category of pointed objects]], def. \ref{CategoryOfPointedObjects}. Then the [[homotopy fiber]] of its [[homotopy fiber]], def. \ref{HomotopyFiber}, is isomorphic, in $Ho(\mathcal{C}^{\ast/})$, to the [[loop space object]] $\Omega Y$ of $Y$ (def. \ref{SuspensionAndLoopSpaceObject}, prop. \ref{LoopingAsFunctorOnHomotopyCategory}):

$$
  hofib(hofib(X \overset{f}{\to}Y)) \simeq \Omega Y
  \,.
$$

=--

+-- {: .proof}
###### Proof

Assume without restriction that $f \;\colon\; X \longrightarrow Y$ is already a fibration between fibrant objects in $\mathcal{C}$ (otherwise replace and rename). Then its homotopy fiber is its ordinary fiber, sitting in a [[pullback]] square

$$
  \array{
    hofib(f) \simeq & F &\overset{i}{\longrightarrow}& X
    \\
    & \downarrow && \downarrow^{\mathrlap{f}}
    \\
    & \ast &\longrightarrow& Y
  }
  \,.
$$

In order to compute $hofib(hofib(f))$, i.e. $hofib(i)$, we need to replace the fiber inclusion $i$ by a fibration. Using the [[factorization lemma]] \ref{FactorizationLemma} for this purpose yields, after a choice of [[path space object]] $Path(X)$ (def. \ref{PathAndCylinderObjectsInAModelCategory}), a replacement of the form

$$
  \array{
    F &\overset{\in W}{\longrightarrow}& F \times_X Path(X)
    \\
    &{}_{\mathllap{i}}\searrow& \downarrow^{\mathrlap{\tilde i}}_{\mathrlap{\in Fib}}
    \\
    && X
  }
  \,.
$$

Hence $hofib(i)$ is the ordinary fiber of this map:

$$
  hofib(hofib(f)) \simeq  F \times_X Path(X) \times_X \ast \;\;\;\; \in Ho(\mathcal{C}^{\ast/})
  \,.
$$

Notice that

$$
  F \times_X Path(X) \; \simeq \; \ast \times_Y Path(X)
$$

because of the [[pasting law]]:

$$
  \array{
     F \times_X Path(X) &\longrightarrow& Path(X)
     \\
     \downarrow &(pb)& \downarrow
     \\
     F &\overset{i}{\longrightarrow}& X
     \\
     \downarrow &(pb)& \downarrow^{\mathrlap{f}}
     \\
     \ast &\longrightarrow& Y
  }
  \,.
$$

Hence

$$
  hofib(hofib(f))
    \;\simeq\;
  \ast \times_Y Path(X) \times_X \ast
  \,.
$$

Now we claim that there is a choice of path space objects $Path(X)$ and $Path(Y)$ such that this model for the homotopy fiber (as an object in $\mathcal{C}^{\ast/}$) sits in a [[pullback]] diagram of the following form:

$$
  \array{
    \ast \times_Y Path(X) \times_X \ast &\longrightarrow& Path(X)
    \\
    \downarrow && \downarrow\mathrlap{\in W \cap F}
    \\
    \Omega Y &\longrightarrow& Path(Y)\times_Y X
    \\
    \downarrow &(pb)& \downarrow
    \\
    \ast &\longrightarrow&  Y \times X
  }
  \,.
$$

By the [[pasting law]] and the pullback stability of acyclic fibrations, this will prove the claim.

To see that the bottom square here is indeed a pullback, check the [[universal property]]: A morphism out of any $A$ into $\ast \underset{Y \times X}{\times} Path(Y) \times_Y X$ is a morphism $a \colon A \to Path(Y)$ and a morphism $b \colon A \to X$ such that $p_0(a) = \ast$, $p_1(a) = f(b)$ and $b = \ast$. Hence it is equivalently just a morphism $a \colon A \to Path(Y)$ such that $p_0(a) = \ast$ and $p_1(a) = \ast$. This is the defining universal property of $\Omega Y \coloneqq \ast \underset{Y}{\times} Path(Y) \underset{Y}{\times} \ast$.

Now to construct the right vertical morphism in the top square ([Quillen 67, page 3.1](model+category#Quillen67)): Let $Path(Y)$ be any path space object for $Y$ and let $Path(X)$ be given by a factorization

$$
  (id_X, \; i \circ f, \; id_X)
  \;\colon\;
  X
  \overset{\in W}{\to}
  Path(X)
  \overset{\in Fib}{\longrightarrow}
  X \times_Y Path(Y) \times_Y X
$$

and regarded as a path space object of $X$ by further comoposing with

$$
  (pr_1,pr_3)\colon X \times_Y Path(Y) \times_Y X \overset{\in Fib}{\longrightarrow} X \times X
  \,.
$$

We need to show that $Path(X)\to Path(Y) \times_Y X$ is an acyclic fibration.

It is a fibration because $X\times_Y Path(Y) \times_Y X \to Path(Y)\times_Y X$ is a fibration, this being the pullback of the fibration $X \overset{f}{\to} Y$.

To see that it is also a weak equivalence, first observe that $ Path(Y)\times_Y X \overset{\in W \cap Fib}{\longrightarrow} X$, this being the pullback of the acyclic fibration of lemma \ref{ComponentMapsOfCylinderAndPathSpaceInGoodSituation}. Hence we have a factorization of the identity as

$$
  id_X
  \;\colon\;
  X
    \underoverset{\in W}{i}{\longrightarrow}
  Path(X)
    \overset{}{\longrightarrow}
  Path(Y)\times_Y X
    \underset{\in W \cap Fib}{\longrightarrow}
  X
$$

and so finally the claim follows by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

=--

+-- {: .num_remark #HomotopyCommutativeSquares}
###### Remark

There is a conceptual way to understand prop. \ref{HomotopyFiberOfHomotopyFiberIsLooping} as follows:
If we draw double arrows to indicate [[homotopies]], then a [[homotopy fiber]] (def. \ref{HomotopyFiber}) is depicted by the following filled square:

$$
  \array{
    hofib(f) &\longrightarrow& \ast
    \\
    \downarrow &\swArrow& \downarrow
    \\
    X &\underset{f}{\longrightarrow}& Y
  }
$$

just like the ordinary [[fiber]] (example \ref{FiberAndCofiberInPointedObjects}) is given by a plain square

$$
  \array{
    fib(f) &\longrightarrow& \ast
    \\
    \downarrow && \downarrow
    \\
    X &\underset{f}{\longrightarrow}& Y
  }
  \,.
$$

One may show that just like the fiber is the _universal_ solution to making such a commuting square (a [[pullback]] [[limit|limit cone]] def. \ref{LimitsAndColimits}), so the homotopy fiber is the universal solution up to homotopy to make such a commuting square up to homotopy -- a [[homotopy pullback]] [[homotopy limit|homotopy limit cone]].

Now just like ordinary [[pullbacks]] satisfy the [[pasting law]] saying that attaching two pullback squares gives a pullback rectangle, the analogue is true for homotopy pullbacks. This implies that if we take the homotopy fiber of a homotopy fiber, thereby producing this double homotopy pullback square

$$
  \array{
    hofib(g) &\longrightarrow& hofib(f) &\longrightarrow& \ast
    \\
    \downarrow &\swArrow& \downarrow^{\mathrlap{g}} &\swArrow& \downarrow
    \\
    \ast &\longrightarrow& X &\underset{f}{\longrightarrow}& Y
  }
$$

then the total outer rectangle here is itself a homotopy pullback. But the outer rectangle exhibits the homotopy fiber of the point inclusion, which, via def. \ref{SuspensionAndLoopSpaceObject} and lemma \ref{FactorizationLemma}, is the [[loop space object]]:

$$
  \array{
    \Omega Y &\longrightarrow& \ast
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \ast &\longrightarrow& Y
  }
  \,.
$$

=--


+-- {: .num_prop #LongFiberSequence}
###### Proposition
**([[long homotopy fiber sequences]])**

Let $\mathcal{C}$ be a model category and let $f \colon X \to Y$ be morphism in the pointed homotopy category $Ho(\mathcal{C}^{\ast/})$ (prop. \ref{ModelStructureOnSliceCategory}). Then:

1. There is a long sequence to the left in $\mathcal{C}^{\ast/}$ of the form

   $$
     \cdots
       \longrightarrow
     \Omega X
       \overset{\overline{\Omega} f}{\longrightarrow}
     \Omega Y
       \longrightarrow
     hofib(f)
       \longrightarrow
     X
       \overset{f}{\longrightarrow}
     Y
     \,,
   $$

   where each morphism is the [[homotopy fiber]] (def. \ref{HomotopyFiber}) of the following one: the **[[homotopy fiber sequence]]** of $f$. Here $\overline{\Omega}f$ denotes $\Omega f$ followed by forming inverses with respect to the group structure on $\Omega(-)$ from prop. \ref{LoopingAsFunctorOnHomotopyCategory}.

   Moreover, for $A\in \mathcal{C}^{\ast/}$ any object, then there is a [[long exact sequence]]

   $$
     \cdots
     \to
     [A,\Omega^2 Y]_\ast
     \longrightarrow
     [A,\Omega hofib(f)]_\ast
     \longrightarrow
     [A, \Omega X]_\ast
     \longrightarrow
     [A,\Omega Y]
     \longrightarrow
     [A,hofib(f)]_\ast
     \longrightarrow
     [A,X]_\ast
     \longrightarrow
     [A,Y]_\ast
   $$

   of [[pointed sets]], where $[-,-]_\ast$ denotes the pointed set valued hom-functor of example \ref{HomotopyCategoryOfPointedModelStructureIsEnrichedInPointedSets}.

1. Dually, there is a long sequence to the right in $\mathcal{C}^{\ast/}$ of the form

   $$
     X
       \overset{f}{\longrightarrow}
     Y
       \overset{}{\longrightarrow}
     hocofib(f)
       \longrightarrow
     \Sigma X
       \overset{\overline{\Sigma} f}{\longrightarrow}
     \Sigma Y
       \to \cdots
     \,,
   $$

   where each morphism is the [[homotopy cofiber]] (def. \ref{HomotopyFiber}) of the previous one: the **[[homotopy cofiber sequence]]** of $f$. Moreover, for $A\in \mathcal{C}^{\ast/}$ any object, then there is a [[long exact sequence]]

   $$
     \cdots
     \to
     [\Sigma^2 X, A]_\ast
     \longrightarrow
     [\Sigma hocofib(f), A]_\ast
     \longrightarrow
     [\Sigma Y, A]_\ast
     \longrightarrow
     [\Sigma X, A]
     \longrightarrow
     [hocofib(f),A]_\ast
     \longrightarrow
     [Y,A]_\ast
     \longrightarrow
     [X,A]_\ast
   $$

   of [[pointed sets]], where $[-,-]_\ast$ denotes the pointed set valued hom-functor of example \ref{HomotopyCategoryOfPointedModelStructureIsEnrichedInPointedSets}.


=--

([Quillen 67, I.3, prop. 4](model+category#Quillen67))

+-- {: .proof}
###### Proof

That there are long sequences of this form is the result of combining prop. \ref{HomotopyFiberOfHomotopyFiberIsLooping} and  prop. \ref{ExactSequenceOfHomotopyFiberAtOneStage}.

It only remains to see that it is indeed the morphisms $\overline{\Omega} f$ that appear, as indicated.

In order to see this, it is convenient to adopt the following notation: for $f \colon X \to Y$ a morphism, then we denote the collection of [[generalized element]] of its homotopy fiber as

$$
  hofib(f)
  =
  \left\{
    (x, f(x) \overset{\gamma_1}{\rightsquigarrow} \ast)
  \right\}
$$

indicating that these elements are pairs consisting of an element $x$ of $X$ and a "path" (an element of the given path space object) from $f(x)$ to the basepoint.

This way the canonical map $hofib(f) \to X$ is $(x, f(x) \rightsquigarrow \ast) \mapsto x$. Hence in this notation the homotopy fiber of the homotopy fiber reads

$$
  hofib(hofib(f))
  =
  \left\{
    ( (x, f(x) \overset{\gamma_1}{\rightsquigarrow} \ast),
            x \overset{\gamma_2}{\rightsquigarrow} \ast  )
  \right\}
  \,.
$$

This identifies with $\Omega Y$ by forming the loops

$$
  \gamma_1 \cdot f(\overline{\gamma_2})
  \,,
$$

where the overline denotes reversal and the dot denotes concatenation.

Then consider the next homotopy fiber

$$
  hofib(hofib(hofib(f)))
  =
  \left\{
    \left(
      ( (x, f(x) \overset{\gamma_1}{\rightsquigarrow} \ast), x \overset{\gamma_2}{\rightsquigarrow} \ast  ),
      \left(
      \array{
         x && \overset{\gamma_3}{\rightsquigarrow} && \ast
         \\
         f(x) &&\overset{f(\gamma_3)}{\rightsquigarrow}&& \ast
         \\
         & {}_{\mathllap{\gamma_1}}\searrow & \Rightarrow & \swarrow_{\mathllap{}}
         \\
         && \ast
      }
      \right)
    \right)
  \right\}
  \,,
$$

where on the right we have a path in $hofib(f)$ from $(x, f(x)\overset{\gamma_1}{\rightsquigarrow} \ast)$ to the basepoint element. This is a path $\gamma_3$ together with a path-of-paths which connects $f_1$ to $f(\gamma_3)$.

By the above convention this is identified with the loop in $X$ which is

$$
  \gamma_2 \cdot (\overline{\gamma}_3)
  \,.
$$

But the map to $hofib(hofib(f))$ sends this data to $( (x, f(x) \overset{\gamma_1}{\rightsquigarrow} \ast), x \overset{\gamma_2}{\rightsquigarrow} \ast  )$, hence to the loop

$$
  \begin{aligned}
    \gamma_1 \cdot f( \overline{\gamma_2} )
    & \simeq
    f(\gamma_3) \cdot f(\overline{\gamma_2})
    \\
    & =
    f( \gamma_3 \cdot \overline{\gamma_2} )
    \\
    & =
    f ( \overline{\gamma_2 \cdot \overline{\gamma}_3} )
    \\
    & =
    \overline{f(\gamma_2 \cdot \overline{\gamma}_3) }
  \end{aligned}
  \,,
$$

hence to the reveral of the image under $f$ of the loop in $X$.





=--

+-- {: .num_remark}
###### Remark

In ([Quillen 67, I.3, prop. 3, prop. 4](model+category#Quillen67)) more is shown than stated in prop. \ref{LongFiberSequence}: there the [[connecting homomorphism]] $\Omega  Y \to hofib(f)$ is not just shown to exist, but is described in detail via an [[action]] of $\Omega Y$ on $hofib(f)$ in $Ho(\mathcal{C})$. This takes a good bit more work. For our purposes here, however, it is sufficient to know that such a morphism exists at all, hence that $\Omega Y \simeq hofib(hofib(f))$.

=--


+-- {: .num_example #LongExactSequeceOfHomotopyGroups}
###### Example

Let $\mathcal{C} = (Top_{cg})_{Quillen}$ be the [[classical model structure on topological spaces]] ([[compactly generated topological spaces|compactly generated]]) from theorem \ref{TopQuillenModelStructure}, theorem \ref{ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces}. Then using the  standard pointed topological path space objects $Maps(I_+,X)$ from def. \ref{TopologicalPathSpace} and example \ref{PointedMappingSpace} as the abstract path space objects in def. \ref{PathAndCylinderObjectsInAModelCategory}, via prop. \ref{TopologicalPathSpaceIsGoodPathSpaceObject}, this gives that

$$
  [\ast, \Omega^n X] \simeq \pi_n(X)
$$

is the $n$th [[homotopy group]], def. \ref{HomotopyGroupsOftopologicalSpaces}, of $X$ at its basepoint.

Hence using $A = \ast$ in the first item of prop. \ref{LongFiberSequence}, the [[long exact sequence]] this gives is of the form

$$
   \cdots
  \to
  \pi_3(X)
   \overset{f_\ast}{\longrightarrow}
  \pi_3(Y)
   \longrightarrow
  \pi_2(hofib(f))
   \overset{}{\longrightarrow}
  \pi_2(X)
   \overset{-f_\ast}{\longrightarrow}
  \pi_2(Y)
   \longrightarrow
  \pi_1(hofib(f))
   \overset{}{\longrightarrow}
  \pi_1(X)
    \overset{f_\ast}{\longrightarrow}
  \pi_1(Y)
   \overset{}{\longrightarrow}
  \ast
  \,.
$$


This is called the **[[long exact sequence of homotopy groups]]** induced by $f$.

=--

+-- {: .num_remark #}
###### Remark

As we pass to [[stable homotopy theory]] (in [[Introduction to Stable homotopy theory -- 1|Part 1)]]), the long exact sequences in example \ref{LongExactSequeceOfHomotopyGroups} become long not just to the left, but also to the right. Given then a [[tower of fibrations]], there is an induced sequence of such long exact sequences of homotopy groups, which organizes into an _[[exact couple]]_. For more on this see at _[[Introduction to Stable homotopy theory -- I|Interlude -- Spectral sequences]]_ ([this remark](Introduction+to+Stable+homotopy+theory+--+I#UnrolledExactCoupleOfAFiltrationOnASpectrum)).

=--

+-- {: .num_example}
###### Example

Let again $\mathcal{C} = (Top_{cg})_{Quillen}$ be the [[classical model structure on topological spaces]] ([[compactly generated topological space|compactly generated]]) from theorem \ref{TopQuillenModelStructure}, theorem \ref{ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces}, as in example \ref{LongExactSequeceOfHomotopyGroups}. For $E \in Top_{cg}^{\ast/}$ any [[pointed topological space]] and $i \colon A \hookrightarrow X$ an inclusion of pointed topological spaces, the exactness of the sequence in the second item of prop. \ref{LongFiberSequence}

$$
  \cdots \to [hocofib(i), E] \longrightarrow [X,E]_\ast \longrightarrow [A,E]_\ast \to \cdots
$$

gives that the functor

$$
  [-,E]_\ast
  \;\colon\;
  (Top^{\ast/}_{CW})^{op}
  \longrightarrow
  Set^{\ast/}
$$

behaves like one degree in an [additive](Introduction+to+Stable+homotopy+theory+--+S#WedgeAxiom) [[reduced cohomology theory]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#ReducedGeneralizedCohomology)). The [[Brown representability theorem]] ([thm.](Introduction+to+Stable+homotopy+theory+--+S#BrownRepresentabilityTraditional)) implies that all additive reduced cohomology theories are degreewise representable this way ([prop.](Introduction+to+Stable+homotopy+theory+--+S#AdditiveReducedCohomologyTheoryRepresentedByOmegaSpectrum)).

=--


[[!redirects geometry of physics -- categories and toposes]]
[[!redirects geometry of physics -- Categories and Toposes]]
