
> This entry is one chapter of _[[geometry of physics]]_.

> next chapters: _[[geometry of physics -- smooth sets|smooth sets]]_, _[[geometry of physics -- supergeometry|supergeometry]]_ 

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

We give here an introduction to the basic concepts and results, aimed at providing background for the [[synthetic differential geometry|synthetic]] [[higher differential geometry|higher]] [[geometry of physics -- supergeometry|supergeometry]] of relevance in formulations of fundamental [[physics]], such as used in the chapters _[[geometry of physics -- perturbative quantum field theory|on perturbative quantum field theory]]_ and _[[geometry of physics -- fundamental super p-branes|on fundamental super p-branes]]_. For quick informal survey see _[[schreiber:Introduction to Higher Supergeometry]]_.

This makes use of the following curious dictionary between [[category theory]]/[[topos theory]] and the [[geometry]] of [[generalized spaces]], which we will explain in detail (following [Grothendieck 65](functorial+geometry#Grothendieck65), [Lawvere 86, p. 17](space+and+quantity#Lawvere86), [[Some Thoughts on the Future of Category Theory|Lawvere 91]]):

{#GeometryOfGeneralizedSpaces}$\,$

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

We offer also an _a priori_ motivation: 

{#CategoryTheoryIsTheoryOfDuality} _Category theory is the theory of duality._

\begin{imagefromfile}
  "file_name": "DualityGraphics.jpg",
  "width": 200,
  "float": "right",
  "margin": {
    "top": -30,
    "right": 0,
    "bottom": 10,
    "left": 20,
    "unit": "px"
  }
\end{imagefromfile}

_[[duality|Duality]]_ is of course an ancient notion in [[philosophy]]. At least as a term, it makes a curious re-appearance in the conjectural [[theory (physics)|theory]] of fundamental [[physics]] formerly known as _[[string theory]]_, as _[[duality in string theory]]_. In both cases, the literature left some room in delineating what precisely is meant. But the philosophically inclined mathematician could notice (see [Lambek 82](adjoint+functor#Lambek82)) that an excellent candidate to make precise the idea of _[[duality]]_ is the mathematical concept of _[[adjoint functor|adjunction]]_, from [[category theory]]. This is particularly pronounced for _[[adjoint triples]]_ (Remark \ref{AdjointTriples} below) and their induced [[adjoint modalities]] ([[Some Thoughts on the Future of Category Theory|Lawvere 91]], see Def. \ref{AdjointModality} below), which exhibit a given "[[modality|mode of being]]" of any object $X$ as intermediate between two dual opposite extremes (Prop. \ref{ComparisonMorphismBetweenOppositeExtremes} below):

$$
  \Box X 
    \overset{\phantom{AAAA}}{\longrightarrow}
  X 
    \overset{\phantom{AAAA}}{\longrightarrow}
  \bigcirc X
$$

For example, _[[cohesion|cohesive]]_ [[geometry|geometric]] [[structure]] on [[generalized spaces]] is captured, this way, as [[modality]] in between the [[discrete object|discrete]] and the [[codiscrete object|codiscrete]] (Example \ref{DiscreteTopologicalSpaces}, and Def. \ref{CohesiveTopos} below).

Historically, [[category theory]] was introduced in order to make precise the concept of _[[natural transformation]]_: The concept of _[[functors]]_ was introduced just so as to support that of natural transformations, and the concept of _[[categories]]_ only served that of functors (see e.g. [Freyd 65, Part II](category+theory#Freyd65)). 

\begin{imagefromfile}
  "file_name": "Adjointness.jpg",
  "width": 460,
  "float": "right",
  "margin": {
    "top": -40,
    "right": 0,
    "bottom": 10,
    "left": 20,
    "unit": "px"
  }
\end{imagefromfile}


But natural transformations are, in turn, exactly the basis for the concept of _[[adjoint functors]]_ (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets} below), equivalently _[[adjunctions]] between categories_ (Prop. \ref{AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat} below), shown on the left. 
All _[[universal constructions]]_, the heart of category theory, are special cases of [[adjoint functors]] -- hence of dualities, if we follow [Lambek 82](adjoint+functor#Lambek82): This includes the concepts of _[[limits]]_ and _[[colimits]]_ (Def. \ref{Limits} below), [[ends]] and [[coends]] (Def. \ref{EndAndCoendInTopcgSmash} below) [[Kan extensions]] (Prop. \ref{TopologicalLeftKanExtensionBCoend} below), and the behaviour of these constructions, such as for instance the [[free co-completion]] nature of the [[Yoneda embedding]] (Prop. \ref{FreeCocompletion} below). 

$\,$

$\,$

$\,$

Therefore it makes sense to regard category theory as the **theory of adjunctions**, <br/> hence the **theory of duality**:

<br/>

{#HierarchyOfConcepts} $\,$

| $\phantom{A}$hierarchy of concepts$\phantom{A}$  | $\phantom{A}$[[category theory]]$\phantom{A}$ | $\phantom{A}$[[enriched category theory|enriched]]$\phantom{A}$ | $\phantom{A}$[[model category|homotopical]]$\phantom{A}$ |
|------------------------|------------|--------------------------|------|
| $\phantom{A}$[[adjoint triple|adjunction of adjunctions]]$\phantom{A}$ <br/> $\phantom{AA}$[[adjoint triple|duality of dualities]]$\phantom{A}$ | $\phantom{A}$Def. \ref{AdjunctionofAdjunction}$\phantom{A}$ |   |  $\phantom{A}$Def. \ref{QuillenAdjointTriple}$\phantom{A}$ |  
| $\phantom{A}$ [[adjoint equivalence]]$\phantom{A}$ <br/> $\phantom{AA}$[[adjoint equivalence|dual equivalence]] $\phantom{AA}$ | $\phantom{A}$ Def. \ref{AdjointEquivalenceOfCategories} $\phantom{A}$ | $\phantom{A}$ Def. \ref{EnrichedEquivalenceOfCategories} $\phantom{A}$ | $\phantom{A}$Def. \ref{QuillenEquivalence} |
| $\phantom{A}$ [[adjoint functor|adjunction]]$\phantom{A}$ <br/> $\phantom{AA}$[[duality]]$\phantom{A}$  | $\phantom{A}$ Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets} $\phantom{A}$ |  $\phantom{A}$ Def. \ref{EnrichedAdjunction} $\phantom{A}$  |  $\phantom{A}$Def. \ref{QuillenAdjunction} | 
| $\phantom{A}$ [[natural transformation]] $\phantom{A}$ | $\phantom{A}$ Def. \ref{NaturalTransformations} $\phantom{A}$ |  $\phantom{A}$ Def. \ref{EnrichedNaturalTransformation} $\phantom{A}$ |  |
| $\phantom{A}$ [[functor]] $\phantom{A}$ | $\phantom{A}$ Def. \ref{Functors} $\phantom{A}$ |  $\phantom{A}$ Def. \ref{TopologicallyEnrichedFunctor} $\phantom{A}$ |  | 
| $\phantom{A}$ [[category]] $\phantom{A}$ | $\phantom{A}$ Def. \ref{Categories} $\phantom{A}$ | $\phantom{A}$ Def. \ref{TopEnrichedCategory} $\phantom{A}$ | $\phantom{A}$ Def. \ref{ModelCategory} |
{: style='margin:auto}



The pivotal role of [[adjunctions]] in [[category theory]] ([Lawvere 08](adjoint+functor#fn:1)) and in the [[foundations of mathematics]] ([[Adjointness in Foundations|Lawvere 69]], [[Cohesive Toposes and Cantor's lauter Einsen|Lawvere 94]] ) was particularly amplified by [[F. W. Lawvere]][^LawvereOnAdjointFunctors]. Moreover, [[Lawvere]] saw the future of category theory ([[Some Thoughts on the Future of Category Theory|Lawvere 91]]) as concerned with [[adjunctions]] expressing systems of archetypical dualities that reveal foundations for [[geometry]] ([Lawvere 07](cohesive+topos#LawvereAxiomatic)) and [[physics]] ([[Toposes of laws of motion|Lawvere 97]], see Def. \ref{CohesiveTopos} and Def. \ref{DifferentialCohesion} below). He suggested ([Lawvere 94](objective+and+subjective+logic#Lawvere94)) this as a precise formulation of core aspects of the _theory of everything_
of early 19th century [[philosophy]]: [[Hegel]]'s _[[Science of Logic]]_.

[^LawvereOnAdjointFunctors]: "the universality of the concept
of adjointness, which was first isolated and named in the conceptual sphere of category theory" ([Lawvere 69](adjoint+functor#Lawvere69#Lawvere69)) "In all those areas where category theory is actively used the categorical concept of adjoint functor has come to play a key role." (first line from _[An interview with William Lawvere](https://ncatlab.org/nlab/show/William+Lawvere#Interview07)_, paraphrasing the first paragraph of _[Taking categories seriously](William+Lawvere#TakingCategoriesSeriously)_)


These days, of course, _[[theories of everything]]_, such as [[string theory]], are understood less ambitiously than Hegel's ontological process,
as mathematical formulations of fundamental theories of physics, that could conceptually unify the hodge-podge of currently available "standard models" [[standard model of particle physics|of particle physics]] and [[standard model of cosmology|of cosmology]] to a more coherent whole.

The idea of _[[duality in string theory]]_ refers to different perspectives on physics that appear dual to each other while being _equivalent_.
But one of the basic results of category theory (Prop. \ref{EveryEquivalenceOfCategoriesComesFromAnAdjointEquivalence}, below) is that equivalence is indeed a special case of adjunction. This allows to explore the possibility that there is more than a coincidence of terms.

Of course the usage of the term _[[duality in string theory]]_ is too loose for one to expect to be able to refine each occurrence of the term in the literature to a mathematical adjunction. However, we will see mathematical formalizations of core aspects of
key string-theoretic dualities, such as _[[topological T-duality]]_ and the _[[duality between M-theory and type IIA string theory]]_, in terms of [[adjunctions]]. Indeed, at the heart of these _[[dualities in string theory]]_ is the phenomenon of _[[double dimensional reduction]]_, which turns out to be formalized by one of the most fundamental adjunctions in ([[higher category theory|higher]]) [[category theory]]: _[[base change]]_ along the point inclusion into a [[classifying space]]. All this is discussed in the chapter on _[[geometry of physics -- fundamental super p-branes|fundamental super p-branes]]_.

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

[[!include geometry of physics -- homotopy types]]

$\,$

[[!include geometry of physics -- basic notions of higher topos theory]]


[[!redirects geometry of physics -- categories and toposes]]
[[!redirects geometry of physics -- Categories and Toposes]]
