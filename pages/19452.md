[[!redirects geometry of physics -- Categories and Toposes]]

> This page is going to be one chapter in _[[geometry of physics]]_.

> next chapter: _[[geometry of physics -- smooth sets|smooth sets]]_

> under construction

$\,$

$\,$

[[category theory|Category theory]] and [[topos theory]] concern the general abstract structure underlying [[algebra]], [[geometry]] and [[logic]] and are ubiquituous in and indispensible for organizing concpetual mathematical frameworks.

We give here an introduction to the basic concepts and results of _[[category theory]]_ and of _[[topos theory]]_, aimed at providing background for the [[synthetic differential geometry|synthetic]] and [[higher differential geometry|higher]] [[geometry of physics -- supergeometry|supergeometry]] of relevance in formulations of fundamental [[physics]], such as used in the chapters _[[geometry of physics -- perturbative quantum field theory|on perturbative quantum field theory]]_ and _[[geometry of physics -- fundamental super p-branes|on fundamental super p-branes]]_.

This means that we emphasize the interpretation of _[[presheaves]]_ (Example \ref{CategoryOfPresheaves} and Example \ref{EnrichedPresheaf} below) on some _[[site]]_ (Def. \ref{Coverage} below) as **[[generalized spaces]]** modeled on the objects in the site ([Lawvere 86, p. 17](space+and+quantity#Lawvere86)). Accordingly, we highlight (Remark \ref{PresaheavesAsGeneralizedSpaces} below) that, from this perspective, the notorious core result of [[category theory]] called the _[[Yoneda lemma]]_ (Prop. \ref{YonedaLemma} below), or the _[[Yoneda embedding]]_ (Prop. \ref{YonedaEmbedding} below), as well as the core concept of [[topos theory]], namely the [[sheaf|sheaf condition]] (Def. \ref{Sheaf} below) express nothing but the consistency of the concept of [[generalized spaces]]. This is the perspective of _[[functorial geometry]]_ ([Grothendieck 65](#functorial+geometry#Grothendieck65)).  (For more exposition of this point see also at _[[motivation for sheaves, cohomology and higher stacks]]_.)

Hence one motivation for [[category theory]] and [[topos theory]] is _a posteriori_: As a matter of experience, there is just no other toolbox that allows one to really understand and handle the [[higher differential geometry|higher]] [[supergeometry]] of relevance in [[physics]]. Similar comments apply to a wealth of other topics of mathematics.

We offer also an _a priori_ motivation: _Category theory is the theory of duality._

<div style="float:right;margin:0 10px 10px 0;"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/74/Cup_or_faces_paradox.svg/450px-Cup_or_faces_paradox.svg.png" width="200"></div>

_[[duality|Duality]]_ is of course an ancient notion in [[philosophy]]. At least as a term, it makes a curious re-appearance in the conjectural [[theory (physics)|theory]] of fundamental [[physics]] formerly known as _[[string theory]]_. In both cases, the literature left some room in delineating what precisely is meant. But the philosophically inclined mathematician could notice (see [Lambek 82](adjoint+functor#Lambek82)) that an excellent candidate to make precise the idea of _[[duality]]_ is the mathematical concept of _[[adjoint functor|adjunction]]_, from [[category theory]].

Historically, [[category theory]] was introduced in order to make precise the concept of _[[natural transformation]]_: The concept of _[[functors]]_ was introduced just so as to support that of natural transformations, and the concept of _[[categories]]_ only served that of functors (see e.g. [Freyd 65, Part II](category+theory#Freyd65)). But natural transformations are what allows us to define, in turn, the concept of _[[adjoint functors]]_, also called _[[adjunctions]]_ between categories. All the deep concepts of category theory (such as _[[representable functors]]_, _[[Yoneda embedding]]_, _[[Kan extensions]]_, hence _[[limits]]_ and _[[colimits]]_, to be introduced below) are special cases of [[adjoint functor]] constructions -- hence of dualities, if we follow [Lambek 82](adjoint+functor#Lambek82). Therefore it makes sense to regard category theory, to a large extent, as the **theory of adjunctions**, hence the **theory of duality**:



| $\phantom{A}$ hierarchy of concepts $\phantom{A}$  | $\phantom{A}$ [[category theory]] $\phantom{A}$ | $\phantom{A}$ [[enriched category theory]] $\phantom{A}$ |
|------------------------|------------|--------------------------|
| $\phantom{A}$ [[adjoint equivalence]] / $\phantom{A}$ <br/> $\phantom{AA}$ [[adjoint equivalence|dual equivalence]] $\phantom{AA}$ | $\phantom{A}$ Def. \ref{AdjointEquivalenceOfCategories} $\phantom{A}$ | $\phantom{A}$ Def. \ref{EnrichedEquivalenceOfCategories} $\phantom{A}$ |
| $\phantom{A}$ [[adjoint functor|adjunction]] / [[duality]] $\phantom{A}$  | $\phantom{A}$ Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets} $\phantom{A}$ |  $\phantom{A}$ Def. \ref{EnrichedAdjunction} $\phantom{A}$  |
| $\phantom{A}$ [[natural transformation]] $\phantom{A}$ | $\phantom{A}$ Def. \ref{NaturalTransformations} $\phantom{A}$ |  $\phantom{A}$ Def. \ref{EnrichedNaturalTransformation} $\phantom{A}$ |
| $\phantom{A}$ [[functor]] $\phantom{A}$ | $\phantom{A}$ Def. \ref{Functors} $\phantom{A}$ |  $\phantom{A}$ Def. \ref{TopologicallyEnrichedFunctor} $\phantom{A}$ |
| $\phantom{A}$ [[category]] $\phantom{A}$ | $\phantom{A}$ Def. \ref{Categories} $\phantom{A}$ | $\phantom{A}$ Def. \ref{TopEnrichedCategory} $\phantom{A}$ |
{: style='margin:auto}



The pivotal role of [[adjunctions]] in [[category theory]] ([Lawvere 08](adjoint+functor#fn:1)) and in the [[foundations of mathematics]] ([[Adjointness in Foundations|Lawvere 69]], [[Cohesive Toposes and Cantor's lauter Einsen|Lawvere 94]] ) was particularly amplified by [[F. W. Lawvere]][^LawvereOnAdjointFunctors]. Moreover, [[Lawvere]] saw the future of category theory ([[Some Thoughts on the Future of Category Theory|Lawvere 91]]) as concerned with [[adjunctions]] expressing systems of archetypical dualities that reveal foundations for [[geometry]] ([Lawvere 07](cohesive+topos#LawvereAxiomatic)) and [[physics]] ([[Toposes of laws of motion|Lawvere 97]]). He suggested ([Lawvere 94](objective+and+subjective+logic#Lawvere94)) this as a precise formulation of core aspects of the _theory of everything_
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


## Basic notions of Category theory

### Categories and Functors

+-- {: .num_defn #Categories}
###### Definition
**([[category]])**

A _[[category]]_ $\mathcal{C}$ is 

1. a [[class]] $Obj_{\mathcal{C}}$, called the _class of [[objects]]_;

1. for each [[pair]] $X,Y \in Obj_{\mathcal{C}}$ of [[objects]], a [[set]] $Hom_{\mathcal{C}}(X,Y)$, called the _[[set of morphisms]] from $X$ to $Y$_, of the _[[hom-set]]_, for short.

   We denote the elements of this set by arrows like this:

   $$
     X \overset{f}{\longrightarrow} Y \;\;\in Hom_{\mathcal{C}}(X,Y)
     \,.
   $$ 

1. for each [[object]] $X \in Obj_{\mathcal{C}}$ a morphism 

   $$
      X \overset{id_X}{\to} X \;\; \in Hom_{\mathcal{C}}(X,X)
   $$

   called the _[[identity morphism]]_ on $X$;

1. for each [[triple]] $X_1, X_2, X_3 \in Obj$ of [[objects]], a [[function]]

   $$
     \array{
       Hom_{\mathcal{C}}(X_1, X_2) 
       &\times&
       Hom_{\mathcal{C}}(X_2, X_3) 
       &\overset{\circ_{X_1,X_2,X_3}}{\longrightarrow}&
       Hom_{\mathcal{C}}(X_1, X_3)
       \\
       X_1 \overset{f}{\to} X_2
       &,&
       X_2 \overset{f}{\to} X_3
       &\mapsto&
       X_1 \overset{ g \circ f }{\longrightarrow} X_3
     }
   $$

   called _[[composition]]_;

such that:

1. for all [[pairs]] of [[objects]] $X,Y \in Obj_{\mathcal{C}}$ [[unitality]] holds: given

   $$
     X \overset{f}{\to} Y \;\;\in Hom_{\mathcal{C}}(X,Y)
   $$

   then 

   $$
     X \overset{id_Y \circ f}{\longrightarrow} Y
     \;=\;
     X \overset{f}{\longrightarrow} Y
     \;=\;
     X \overset{f \circ id_X }{\longrightarrow} Y
     \,;
   $$

1. for all [[quadruples]] of [[objects]] $X_1, X_2, X_3, X_4 \in Obj_{\mathcal{C}}$ [[composition]] satifies _[[associativity]]_: given

   $$
     X_1 
       \overset{f_{12}}{\to} 
     X_2 
       \overset{f_{23}}{\to} 
     X_3
       \overset{f_{34}}{\to} 
     X_4 
   $$

   then 

   $$
     X_1 \overset{f_{34} \circ (f_{23} \circ f_{12})}{\longrightarrow} X_4
     \;\;=\;\;
     X_1 \overset{(f_{34} \circ f_{23}) \circ f_{12}}{\longrightarrow} X_4
     \,.
   $$

=--

The archetypical example of a [[category]] is the [[category of sets]]:

+-- {: .num_example #CategoryOfSets}
###### Example
**([[Set|category of all sets]])**

The [[class]] of all [[sets]] with [[functions]] between them is a [[category]] (Def. \ref{Categories}), to be denoted _[[Set]]_:

* $Obj_{Set} = \text{class of all sets}$;

* $Hom_{Set}(X,Y) = \text{set of functions from set X to set Y}$;

* $id_X \in Hom_{Set}(X,X) = $ [[identity function]] on set $X$;

* $\circ_{X_1,X_2,X_3} = \text{ordinary composition of functions}$. 

=--

More generally all kind of _sets with [[structure]]_, in the sense going back to [[Bourbaki]], form categories, where the [[morphisms]] are the _[[homomorphisms]]_ (whence the name "morphism"!). These are called _[[concrete categories]]_ (we characterize them precisely in Example \ref{StructuredSetsAndFaithfulFunctors}, further below): 

+-- {: .num_example #ExamplesOfConcreteCategories}
###### Example
**(basic examples of [[concrete categories]])**

For $\mathcal{S}$ a kind of [[mathematical structure]], there is the [[category]] (Def. \ref{Categories}) $\mathcal{S}Set$ whose [[objects]] are the corresponding [[structured sets]], and whose [[morphisms]] are the corresponding structure [[homomorphisms]], hence the [[functions]] of underlying sets which respect the given structure.

Basic examples of [[concrete categories]] include the following:

| $\phantom{A}$[[concrete category]]$\phantom{A}$ | $\phantom{A}$[[objects]]$\phantom{A}$ | $\phantom{A}$[[morphisms]]$\phantom{A}$ |
|-----------------------|-------------|---------------|
| $\phantom{A}$[[Grp]]   | $\phantom{A}$[[groups]]$\phantom{A}$ | $\phantom{A}$[[group homomorphisms]]$\phantom{A}$ |
| $\phantom{A}$[[Vect]]  | $\phantom{A}$[[vector spaces]]$\phantom{A}$ | $\phantom{A}$[[linear maps]]$\phantom{A}$ |
| $\phantom{A}$[[Alg]]   | $\phantom{A}$[[algebras]]$\phantom{A}$ | $\phantom{A}$[[algebra homomorphism]]$\phantom{A}$ |
| $\phantom{A}$[[Top]]  | $\phantom{A}$[[topological spaces]]$\phantom{A}$ |  $\phantom{A}$[[continuous functions]]$\phantom{A}$ |
| $\phantom{A}$[[Mfd]]${}_{k}$  | $\phantom{A}$[[differentiable manifolds]]$\phantom{A}$ | $\phantom{A}$[[differentiable functions]]$\phantom{A}$ |

=--

This is the motivation for the terminology "categories", as the examples in Example \ref{ExamplesOfConcreteCategories} are literally _categories of mathematical structures_. But not all categories are "[[concrete category|concrete]]" in this way.

Some terminology

+-- {: .num_defn #SmallCategory}
###### Definition
**([[small category]])**

If a [[category]] $\mathcal{C}$ (Def. \ref{Categories}) happens to have as [[class]] $Obj_{\mathcal{C}}$ of [[objects]] an actual [[set]] (i.e. a [[small set]] instead of a [[proper class]]), then $\mathcal{C}$ is called a _[[small category]]_.

=--

As usual, there are some trivial examples, that are however useful to make explicit for the development of the theory:

+-- {: .num_example #InitialCategoryAndTerminalCategory}
###### Example
**([[initial category]] and [[terminal category]])**

1. The _[[terminal category]]_ $\ast$ is [[generalized the|the]] [[category]] (Def. \ref{Categories}) whose [[class]] of [[objects]] is [[generalized the|the]] [[singleton]] [[set]], and which has a single [[morphism]] on this object, necessarily the [[identity morphism]].

1. The _[[initial category]]_ or _[[empty category]]_ $\emptyset$ is the [[category]] (Def. \ref{Categories}) whose [[class]] of [[objects]] is the [[empty set]], and which, hence, has no morphism whatsoever.

Clearly, these are [[small categories]] (Def. \ref{SmallCategory}).

=--

+-- {: .num_defn #Isomorphism}
###### Definition
**([[isomorphism]])**

For $\mathcal{C}$ a [[category]] (Def. \ref{Categories}), a [[morphism]] 

$$
  X \overset{f}{\to} Y \;\;\in Hom_{\mathcal{C}}(X,Y)
$$ 

is called an _[[isomorphism]]_ if there exists an [[inverse morphism]]

$$
  Y \overset{f^{-1}}{\longrightarrow} Y \;\; \in Hom_{\mathcal{C}}(Y,X)
$$

namely a morphism such that the [[compositions]] with $f$ are equal to the [[identity morphisms]] on $X$ and $Y$, respectively

$$
  f^{-1} \circ f  \;=\; id_X
  \phantom{AAA}
  f \circ f^{-1} \;=\; id_Y
$$

=--

+-- {: .num_defn #Groupoid}
###### Definition
**([[groupoid]])**

If $\mathcal{C}$ is a [[category]] in which _every_ [[morphism]] is an [[isomorphism]] (Def. \ref{Isomorphism}), then $\mathcal{C}$ is called a _[[groupoid]]_.

=--

+-- {: .num_example #DeloopingGroupoid}
###### Example
**([[delooping]] [[groupoid]])**

For $G$ a [[group]], there is a [[groupoid]] (Def. \ref{Groupoid}) $\mathbf{B}G$ with a single [[object]], whose single [[hom-set]] is $G$, with [[identity morphism]] the [[neutral element]] and [[composition]] the group operation in $G$:

* $Obj_{\mathbf{B}G} = \ast$

* $Hom_{\mathcal{C}}(\ast,\ast) \;=\; G$

In fact every [[groupoid]] with precisely one object is of the form.

=--

+-- {: .num_remark }
###### Remark
**([[groupoids]] and [[homotopy theory]])**

Even though [[groupoids]] (Def. \ref{Groupoid}) are special cases of [[categories]] (Def. \ref{Categories}), the theory of groupoids in itself has a rather different flavour than that of category theory: Part of the [[homotopy hypothesis]]-theorem is that the theory of groupoids is really _[[homotopy theory]]_ for the special case of [[homotopy 1-types]].

(In applications in [[homotopy theory]], groupoids are considered mostly in the case that the [[class]] $Obj_{\mathcal{C}}$ of [[objects]] is in fact a [[set]]: _[[small groupoids]]_, Def. \ref{SmallCategory}). 

For this reason we will not have more to say about [[groupoids]] here, and instead relegate their discussion to the chapter [[geometry of physics -- homotopy types|on homotopy theory]].

=--


There is a range of constructions that provide new categories from given ones:

+-- {: .num_example #OppositeCategory}
###### Example
**([[opposite category]])**

Let $\mathcal{C}$ be a [[category]]. Then its _[[opposite category]]_ $\mathcal{C}^{op}$ has the same [[objects]] as $\mathcal{C}$, but the direction of the [[morphisms]] is reversed. Accordingly, [[composition]] in the [[opposite category]] $\mathcal{C}^{op}$ is that in $\mathcal{C}$, but with the order of the arguments reversed:

* $Obj_{\mathcal{C}^{op}} \;\coloneqq\; Obj_{\mathcal{C}}$;

* $Hom_{\mathcal{C}^{op}}(X,Y) \;\coloneqq\; Hom_{\mathcal{C}}(Y,X)$.

=--


+-- {: .num_example #ProductCategory}
###### Example
**([[product category]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be two [[categories]] (Def. \ref{Categories}). Then their _[[product category]]_ $\mathcal{C} \times \mathcal{D}$ has as [[objects]] [[pairs]] $(c,d)$ with $c \in Obj_{\mathcal{C}}$ and $d \in Obj_{\mathcal{D}}$, and as morphisms [[pairs]]  $ (c_1 \overset{f}{\to} c_2) \in Hom_{\mathcal{C}}(c_1,c_2)$, $ (d_1 \overset{g}{\to} d_2) \in Hom_{\mathcal{D}}(d_1,d_2)$, and [[composition]] is defined by composition in each entry:

* $Obj_{\mathcal{C} \times \mathcal{D}} \coloneqq Obj_{\mathcal{C}} \times Obj_{\mathcal{D}}$;

* $Hom_{\mathcal{C} \times \mathcal{D}}( (c_1,d_1), (c_2,d_2) ) \coloneqq  Hom_{\mathcal{C}}(c_1,c_2) \times Hom_{\mathcal{D}}( d_1, d_2 )$

* $(f_2, g_2) \circ (f_1, g_1) \;\coloneqq\; ( f_2 \circ f_1, g_2 \circ g_1 )$

=--



+-- {: .num_defn #Functors}
###### Definition
**([[functor]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be two [[categories]] (Def. \ref{Categories}). A _[[functor]] from $\mathcal{C}$ to $\mathcal{D}$_, to be denoted

$$
  \mathcal{C} \overset{F}{\longrightarrow} \mathcal{D}
$$

is 

1. a [[function]] between the classes of [[objects]]:

   $$
     F_{Obj} \;\colon\; Obj_{\mathcal{C}} \longrightarrow Obj_{\mathcal{D}}
   $$

1. for each [[pair]] $X,Y \in Obj_{\mathcal{C}}$ of objects a [[function]]

   $$
     F_{X,Y} \;\colon\;  Hom_{\mathcal{C}}(X,Y) \longrightarrow Hom_{\mathcal{D}}(F_{Obj}(X), F_{Obj}(Y))

such that

1. For each [[object]] $X \in Obj_{\mathcal{C}}$ the [[identity morphism]] is respected:

   $$
     F_{X,X}(id_X) \;=\; id_{F_{Obj}(X)}
     \,;
   $$

1. for each [[triple]] $X_1, X_2, X_3 \in Obj_{\mathcal{C}}$ of [[objects]], [[composition]] is respected: given

   $$
      X_1 \overset{f}{\longrightarrow} X_2 \overset{g}{\longrightarrow} X_3
   $$

   then

   $$
      F_{X_1, X_3}(g \circ f ) \;=\;  F_{X_2, X_3}(g) \circ F_{X_1,X_2}(f)
      \,.
   $$

=--


+-- {: .num_example #CategoriesOfSmallCategories}
###### Example
**([[categories]] of [[small categories]] and of [[small groupoids]])**

It is clear that [[functors]] (Def. \ref{Functors}) have a [[composition]] operation given componentwise by the [[composition]] of their component functions. Accordingly, this composition is [[unitality|unital]] and [[associativity|associative]]. This means that there is 

1. the [[category]] (Def. \ref{Categories}) _[[Cat]]_ whose [[objects]] are [[small categories]] (Def. \ref{SmallCategory}) and whose [[morphisms]] are [[functors]] (Def. \ref{Functors}) between these

1. the [[category]] (Def. \ref{Categories}) _[[Grpd]]_ whose [[objects]] are [[small groupoids|small]] [[groupoids]] (Def. \ref{Groupoid}) and whose [[morphisms]] are [[functors]] (Def. \ref{Functors}) between these.

=--


+-- {: .num_example #HomFunctor}
###### Example
**([[hom-functor]])**

Let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}). Then its _[[hom-functor]]_ 

$$
  Hom_{\mathcal{C}}
  \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  Set
$$

is the [[functor]] (Def. \ref{Functors}) out of the [[product category]] (Def. \ref{ProductCategory}) of $\mathcal{C}$ with its [[opposite category]] to the [[category of sets]], which sends a [[pair]] $X,Y \in \mathcal{C}$ of [[objects]] to the [[hom-set]] $Hom_{\mathcal{C}}(X,Y)$ between them, and which sends a [[pair]] of [[morphisms]], with one of them into $X$ and the outher out of $Y$, to the operation of [[composition]] with these morphisms:

$$
  Hom_{\mathcal{C}}
  \;\;\colon\;\;\;
  \array{
    X_1 & Y_1 
    \\
    {}^{\mathllap{g}}\big\uparrow & \big\downarrow^{\mathrlap{h}}
    \\
    X_2 & Y_2
  }
  \;\;\mapsto\;\;
  \array{
    Hom_{\mathcal{C}}(X_1, Y_1)
    \\
    \big\downarrow^{ \mathrlap{ f \mapsto h \circ f \circ g  } }
    \\
    Hom_{\mathcal{C}}(X_2, Y_2)
  }
$$


=--

+-- {: .num_defn #Monomorphism}
###### Definition
**([[monomorphism]] and [[epimorphism]])**

Let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}). Then a [[morphism]] $X \overset{f}{\to } Y$ in $\mathcal{C}$ is called

* a _[[monomorphism]]_ if for every [[object]] $Z \in \mathcal{C}$ the [[hom-functor]] (Example \ref{HomFunctor}) out of $Z$ takes $f$ to an [[injective function]] of [[hom-sets]]:

  $$
    Hom_{\mathcal{C}}(Z,f)
    \;\colon\;
    Hom_{\mathcal{C}}(Z,X)
     \overset{\phantom{AAA}}{\hookrightarrow}
    Hom_{\mathcal{C}}(Z,Y)
    \,;
  $$

* an _[[epimorphism]]_ if for every [[object]] $Z \in \mathcal{Z}$ the [[hom-functor]] (Example \ref{HomFunctor}) into $Z$ takes $f$ to an [[injective function]]:

  $$
    Hom_{\mathcal{C}}( f,Z )
    \;\colon\;
    Hom_{\mathcal{C}}(Y, Z)
      \overset{\phantom{AAA}}{\hookrightarrow}
    Hom_{\mathcal{C}}(X, Z) 
    \,.
  $$

=--


+-- {: .num_defn #FullyFaithfulFunctor}
###### Definition
**([[full functor|full]], [[faithful functor|faithful]] and [[fully faithful functors]])**

A [[functor]] $F \;\colon\; \mathcal{C} \to \mathcal{D}$ (Def. \ref{Functors}) is called


* a _[[full functor]]_ if all its hom-functions are [[surjective functions]] 

  $$
    Hom_{\mathcal{C}}(X,Y) 
      \underoverset{surj}{F_{X,Y}}{\longrightarrow} 
    Hom_{\mathcal{D}}(F(X), F(Y))
  $$

* a _[[faithful functor]]_ if all its hom-functions are [[injective functions]] 

  $$
    Hom_{\mathcal{C}}(X,Y) 
      \underoverset{inj}{F_{X,Y}}{\longrightarrow} 
    Hom_{\mathcal{D}}(F(X), F(Y))
  $$

* a _[[fully faithful functor]]_ if all its hom-functions are [[bijective functions]] 

  $$
    Hom_{\mathcal{C}}(X,Y) 
      \underoverset{bij}{F_{X,Y}}{\longrightarrow} 
    Hom_{\mathcal{D}}(F(X), F(Y))
  $$

A [[fully faithful functor]] is also called a _[[full subcategory]]-inclusion_. We will denote this situation by

$$
  \mathcal{C} \overset{\phantom{A}F\phantom{A}}{\hookrightarrow} \mathcal{D}
  \,.
$$

=--

This allows to make precise the idea of _[[concrete category]]_ from Example \ref{ExamplesOfConcreteCategories}:

+-- {: .num_example #StructuredSetsAndFaithfulFunctors}
###### Example
**([[structured sets]] and [[faithful functors]])**

Let $\mathcal{S}$ be a kind of [[mathematical structure]] and let $\mathcal{S} Set$ be the [[category]] of $\mathcal{S}$-[[structured sets]]. Then there is the  [[forgetful functor]]

$$
  \mathcal{S}Set \longrightarrow Set
$$

which sends each [[structured set]] to the underlying set ("forgetting" the [[structure]] that it carries), and which sends [[functions]] of sets to themselves. That a [[homomorphism]] of [[structured sets]] is a [[function]] between the underlying sets satisfying a _special condition_ implies that this is a _[[faithful functor]]_ (Def. \ref{FullyFaithfulFunctor}).

Conversely, it makes sense to _define_ [[structured sets]] in general to be the [[objects]] of a [[category]] $\mathcal{C}$ which is equipped with a [[faithful functor]] $\mathcal{C} \overset{faithful}{\longrightarrow} Set$ to the [[category of sets]]. See at _[[structure]]_ for more on this.

=--



+-- {: .num_example #SpacesViaAlgebrasOfFunctions}
###### Example
**([[spaces]] seen via their [[algebras of functions]])**

Consider 

1. the [[category]] [[Top]]${}_{cpt}$ of [[compact topological space|compact]] [[topological spaces]] with [[continuous functions]] between them;

1. the category [[C*Alg]] of [[C*-algebras]] over the [[complex numbers]]

from Example \ref{ExamplesOfConcreteCategories}.

Then there is a [[functor]] (Def. \ref{Functors})

$$
  C(-)
  \;\colon\;
  Top_{cpt}
   \longrightarrow
  C^\ast Alg^{op}
$$

from the former to the [[opposite category]] of the latter (Example \ref{OppositeCategory}) which sends any [[compact topological space|compact]] [[topological space]] $X$ to its [[C*-algebra]] $C(X)$ of [[continuous functions]] $X \overset{\phi}{\to} \mathbb{C}$ to the [[complex numbers]], and which sends every [[continuous function]] between compact spaces to the [[C*-algebra]]-[[homomorphism]] that is given by [[precomposition]]:

$$
  C(-)
  \;\;\;\colon\;\;\;
  \array{
    X &\mapsto & C(X) 
    \\
    {}^{\mathllap{ f }}\big\downarrow 
      && 
    \big\uparrow^{\mathrlap{ f^\ast : \phi \mapsto \phi \circ f }}
    \\
    Y &\mapsto& C(Y) 
  }
$$

Part of the statement of _[[Gelfand duality]]_ is that this is a [[fully faithful functor]], hence exhibiting a  [[full subcategory]]-inclusion (Def. \ref{FullyFaithfulFunctor}):

$$
  Top_{cpt}
   \hookrightarrow
  C*Alg^{op}
  \,.
$$

Similarly, consider

1. the [[category]] [[SmthMfd]]$ of [[smooth manifolds]] with [[smooth functions]] between them;

1. the category [[Alg]]${}_{\mathbb{R}}$ of [[associative algebras]] over the [[real numbers]]

from Example \ref{ExamplesOfConcreteCategories}.

Then there is a [[functor]] (Def. \ref{Functors})

$$
  C^\infty(-)
  \;\colon\;
  SmthMfd^{op}
    \longrightarrow
  Alg_{\mathbb{R}}^{op}
$$

from the former to the [[opposite category]] of the latter (Def. \ref{OppositeCategory}), which sends any [[smooth manifold]] $X$ to its [[associative algebra]] $C^\inft(X)$ of [[continuous functions]] $X \overset{\phi}{\to} \mathbb{R}$ to the [[real numbers]], and which sends every [[smooth function]] between smooth manifolds to the [[algebra homomorphism]] that is given by [[precomposition]]:


$$
  C^\infty(-)
  \;\;\;\colon\;\;\;
  \array{
    X &\mapsto & C^\infty(X) 
    \\
    {}^{\mathllap{ f }}\big\downarrow 
      && 
    \big\uparrow^{\mathrlap{ f^\ast : \phi \mapsto \phi \circ f }}
    \\
    Y &\mapsto& C^\infty(Y) 
  }
$$

The statement of _[[Milnor's exercise]]_ is that this  this is a [[fully faithful functor]], hence exhibiting a  [[full subcategory]]-inclusion (Def. \ref{FullyFaithfulFunctor}):

$$
  SmthMfd
   \hookrightarrow
  Alg_{\mathbb{R}}^{op}
  \,.
$$

These two statements, expressing categories of [[spaces]] as [[full subcategories]] of [[opposite categories]] of categories of [[algebras]], are the starting point for many developments in [[geometry]], such as _[[algebraic geometry]]_, _[[supergeometry]]_, _[[noncommutative geometry]]_ and _[[noncommutative topology]]_.

=--




### Natural transformations




+-- {: .num_defn #NaturalTransformations}
###### Definition
**([[natural transformation]] and [[natural isomorphism]])**

Given two [[categories]] $\mathcal{C}$ and $\mathcal{D}$ (Def. \ref{Categories}) and given two [[functors]] from $\mathcal{C}$ to $\mathcal{D}$ (Def. \ref{Functors}), then a _[[natural transformation]]_ from $F$ to $G$

$$
  \mathcal{C}
    \underoverset
      {\underset{G}{\longrightarrow}}
      {\overset{F}{\longrightarrow}}
      {\phantom{AA}\Downarrow \mathrlap{\eta} \phantom{AA}}
  \mathcal{D}
$$

is

* for each [[object]] $X \in Obj_{\mathcal{C}}$ a [[morphism]]

  \[
    \label{NaturalTransformationComponent}
    F(X) \overset{ \eta_X }{\longrightarrow} G(X)
  \]

such that

* for each [[morphism]] $X \overset{f}{\longrightarrow} Y$ we have

  \[
    \label{Naturality}
    \eta_Y\circ F(X)
     \;=\;
    G(Y)\circ \eta_X
    \phantom{AAAAAA}
    \array{
       F(X) &\overset{\eta_X}{\longrightarrow}& G(X)
       \\
       {}^{\mathllap{F(f)}}\downarrow 
         && 
       \downarrow^{\mathrlap{G(f)}}
       \\
       F(Y) &\underset{\eta_Y}{\longrightarrow}& G(Y)
    }
  \]

If all the component morphisms $\eta_X$ are [[isomorphisms]] (Def. \ref{Isomorphism}), then the natural transformation $\eta$ is called a _[[natural isomorphism]]_.

For 

$$
  \mathcal{C}
    \underoverset
      {\underset{G}{\longrightarrow}}
      {\overset{F}{\longrightarrow}}
      {\phantom{AA}\Downarrow \mathrlap{\eta} \phantom{AA}}
  \mathcal{D}
  \phantom{AA}
  \text{and}
  \phantom{AA}
  \mathcal{C}
    \underoverset
      {\underset{H}{\longrightarrow}}
      {\overset{G}{\longrightarrow}}
      {\phantom{AA}\Downarrow \mathrlap{\rho} \phantom{AA}}
  \mathcal{D}
$$

two natural transformations as shown, their _composition_ is the natural transformation

$$
  \mathcal{C}
    \underoverset
      {\underset{H}{\longrightarrow}}
      {\overset{F}{\longrightarrow}}
      {\phantom{A}\Downarrow \mathrlap{\rho \circ \eta} \phantom{AAAA}}
  \mathcal{D}
$$

whose components (eq:NaturalTransformationComponent) are the [[compositions]] of the components of $\eta$ and $\rho$:

\[
  \label{NaturalTransformationComposition}
  (\rho \circ \eta)_X
  \;\coloneqq\;
  \rho_{X} \circ \eta_X
\]

=--


+-- {: .num_example #FunctorCategory}
###### Example
**([[functor category]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be [[categories]] (Def. \ref{Categories}). Then the _[[category of functors]]_ between them, to be denoted $[\mathcal{C}, \mathcal{D}]$, is the [[category]] whose [[objects]] are the [[functors]] $\mathcal{C} \overset{F}{\to} \mathcal{D}$ (Def. \ref{Functors}) and whose [[morphisms]] are the [[natural transformations]] $F \overset{\eta}{\Rightarrow} G$ between functors (Def. \ref{NaturalTransformations}) and whose [[composition]] operation is the composition of natural transformations (eq:NaturalTransformationComposition).

=--

+-- {: .num_example #CategoryOfPresheaves}
###### Example
**([[category of presheaves]])**

Given a [[category]] $\mathcal{C}$ (Def. \ref{Categories}), a [[functor]] (Def. \ref{Functors}) of the form

$$
  F \;\colon\; \mathcal{C}^{op} \longrightarrow Set
  \,,
$$

hence out of the [[opposite category]] of $\mathcal{C}$ (Def. \ref{OppositeCategory}), into the [[category of sets]] (Example \ref{CategoryOfSets}) is also called a _[[presheaf]]_ (for reasons discussed below) _on $\mathcal{C}$_ or _over $\mathcal{C}$_.

The corresponding [[functor category]] (Example \ref{FunctorCategory})

$$
  PSh(\mathcal{C})
  \;\coloneqq\; [\mathcal{C}^{op}, Set]
$$

is hence called the _[[category of presheaves]]_ over $\mathcal{C}$.

Essentially by Example \ref{HomFunctor}, there is the following [[functor]] (Def. \ref{Functors}) from $\mathcal{C}$ to its [[category of presheaves]]:

\[
  \label{YonedaFunctor}
  y
  \;\;\colon\;\;
  \array{
    \mathcal{C}
      &\longrightarrow&
    [\mathcal{C}^{op}, Set]
    \\
    X
    &\mapsto&
    Hom_{\mathcal{C}}(-,X)
  } 
\]

The [[presheaves]] $y(X) \coloneqq Hom_{\mathcal{C}}(-,X)$ in the [[image]] of this functor are called the _[[representable presheaves]]_ and $X \in Obj_{\mathcal{C}}$ is called their [[representing object]].

This functor is called the _[[Yoneda embedding]]_, due to Prop. \ref{YonedaEmbedding} below.

=--

+-- {: .num_remark #PresaheavesAsGeneralizedSpaces}
###### Remark
**([[presheaves]] as [[generalized spaces]])**

If a given [[category]] $\mathcal{C}$ (Def. \ref{Categories}) is thought of as a category of _[[spaces]]_ of sorts, as those in Example \ref{SpacesViaAlgebrasOfFunctions}, then it will be most useful to think of the corresponding [[category of presheaves]] $[\mathcal{C}^{op}, Set]$ (Def. \ref{CategoryOfPresheaves}) as a category of _[[generalized spaces]] probe-able by_ the test spaces in $\mathcal{C}$ ([Lawvere 86, p. 17](space+and+quantity#Lawvere86)).

Namely, imagine a [[generalized space]] $\mathbf{X}$ which is at least probe-able by spaces in $\mathcal{C}$. This should mean that for each [[object]] $c \in \mathcal{C}$ there is some [[set]] of geometric maps "$c \to \mathcal{X}$". Here the quotation marks are to warn us that, at this point, $\mathbf{X}$ is not defined yet, and even if it were, it is not expected to be an object of $\mathcal{C}$, so that, at this point, an actual morphism from $c$ to $\mathbf{X}$ is not defined. But we may anyway consider some set


\[
  \label{WouldBeMapsIntoGeneralizedSpace}
  \mathbf{X}(c)  \; \text{"=}  Hom(c,\mathbf{X})" 
\]

whose elements we do want to think of maps (homomorphisms of spaces) from $c$ to $X$. 

That this is indeed correct, in that we may remove the quotation remarks on the right, is the statement of the _[[Yoneda lemma]]_, which we discuss as Prop. \ref{YonedaLemma} below.


A minimum consistency condition for this to make sense (we will consider further conditions later on when we discuss _[[sheaves]]_) is that we may consistently pre-compose the would-be maps from $c$ to $\mathbf{X}$ with actual morphisms $d \overset{f}{\to} c$ in $\mathcal{C}$. This means that for every such morphism there should be a function between these sets of would-be maps

$$
  \array{
     c && \mathbf{X}(d)
     \\
     {}^{\mathllap{ f }}\big\downarrow 
       && 
     \big\uparrow{}^{\mathrlap{ \mathbf{X}(f) \, \text{"=}(-)\circ f"}}
     \\
     d && \mathbf{X}(c)
  }
$$

which respects composition and identity morphisms. But in summary, this says that what we have defined thereby is actually a _[[presheaf]]_ on $\mathcal{C}$ (Def. \ref{CategoryOfPresheaves}), namely a functor

$$
  \mathbf{X} \;\colon\; \mathcal{C}^{op} \longrightarrow Set
  \,.
$$

For this to make sense, it ought to be true that every "ordinary space", hence every [[object]] $X \in \mathcal{C}$ is also an example of a "generalized space probe-able by" object of $\mathcal{C}$, since, after all, these are the space which may manifestly be probed by objects $c \in \mathcal{C}$, in that morphisms $c \to X$ are already defined.

Hence the incarnation of $X \in \mathcal{C}$ as a generalized space probe-able by objects of $\mathcal{C}$ should be the presheaf $Hom_{\mathcal{C}}(-,X)$, hence the [[representable presheaf|presheaf represented]] by $X$, via the Yoneda functor (eq:YonedaFunctor).

At this point, however, a serious consistency condition arises: The "ordinary spaces" now exist as objects of two different categories, on the one hand there is the original $X \in \mathcal{C}$, on the other hand there is its Yoneda image $y(X) \in [\mathcal{C}^{op}, Set]$ in the category of generalized spaces, and we need to know that these two perspectives are compatible, notably that maps $X \to Y$ between ordinary spaces are the same whether viewed in $\mathcal{C}$ or in the more general context of $[\mathcal{C}^{op}, Set]$. 

That this, too, holds true, is the statement of the _[[Yoneda embedding]]_, which we discuss as Prop. \ref{YonedaEmbedding} below.

Eventually one will want to impose one more consistency condition, namely a _[[sheaf|sheaf condition]]_ (Def. \ref{Sheaf} below). This is what leads over from [[category]] theory to [[topos theory]] [below](#BasicNotionsOfToposTheory).

=--

+-- {: .num_prop #YonedaLemma}
###### Proposition
**([[Yoneda lemma]])**

Let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}), $X \in \mathcal{C}$ any object, and $\mathbf{Y} \in [\mathcal{C}^{op}, Set]$ a [[presheaf]] over $\mathcal{C}$ (Def. \ref{CategoryOfPresheaves}).

Then there is a [[bijection]]

$$
  \array{
    Hom_{[\mathcal{C}^{op},Set]}( y(X), \mathbf(Y) )
      &\overset{\simeq}{\longrightarrow}&
    \mathbf{Y}(X)
    \\
    \eta 
      &\mapsto&
    \eta_X(id_X)
  }
$$

between the [[hom-set]] of the [[category of presheaves]] from the [[representable presheaf|presheaf represented]] by $X$ (eq:YonedaFunctor) to $\mathbf{Y}$, and the set which is assigned by $\mathbf{Y}$ to $X$.

=--

+-- {: .proof}
###### Proof

By Example \ref{FunctorCategory}, an element in the set on the left is a [[natural transformation]] (Def. \ref{NaturalTransformations}) of the form

$$
  \mathcal{C}^{op}
    \underoverset
      {\underset{\mathbf{Y}}{\longrightarrow}}
      {\overset{y(X)}{\longrightarrow}}
      {\phantom{AA} \Downarrow \mathrlap{\eta}  \phantom{AA}}
  Set
$$

hence given by component functions (eq:NaturalTransformationComponent)

$$
  Hom_{\mathcal{C}}(c,X)
    \overset{\eta_c}{\longrightarrow}
  \mathbf{Y}(X)
$$

for each $c \in \mathcal{C}$. In particular there is the component at $c = X$
  
$$
  \array{
    Hom_{\mathcal{C}}(X,X)
      &\overset{\eta_X}{\longrightarrow}&
    \mathbf{Y}(X)
    \\
    id_X &\mapsto& \eta_X(id_X)
  }
$$

and the [[identity morphism]] $id_X$ on $X$ is a canonical element in the set on the left. The statement to be proven is hence equivalently that for every element in $\mathbf{Y}(X)$ there is precisely one $\eta$ such that this element equals $\eta_X(id_X)$.

Now the condition to be satisfied by $\eta$ is that it makes its [[naturality squares]] (eq:Naturality) commute. This includes those of the form

$$
  \array{
    id_X 
    \in
    & 
    Hom_{\mathcal{C}}(X,X)
      &\overset{\eta_X}{\longrightarrow}&
    \mathbf{Y}(X)
    \\ 
    & 
    {}^{\mathllap{ Hom_{\mathcal{C}}(f,X) }}
    \big\downarrow 
      && 
    \big\downarrow{}^{\mathrlap{\mathbf{Y}(f)}}
    \\
    & 
    Hom_{\mathcal{C}}(Y,X)
    &\underset{\eta_Y}{\longrightarrow}&
    \mathbf{Y}(Y)
  }
  \phantom{AAAA}
  \array{
     \{id_X\}
     &\longrightarrow&
     \{\eta_X(id_X)\}
     \\
     \big\downarrow 
     &&
     \big\downarrow
     \\
     \{f\}
     &\longrightarrow&
     \big\{ \eta_Y(F) = \mathbf{Y}(f)( \eta_X(id_X) ) \big\}
  }
$$

for any [[morphism]] 

$$
  (Y \overset{f}{\longrightarrow} X)
    \;\in\;
  Hom_{\mathcal{C}}(Y,X)
  \,.
$$

As the diagram chase of elements on the right shows, this commutativity fixes $\eta_Y(f)$ for all $Y \in \mathcal{C}$ and all $f \in Hom_{\mathcal{C}}(Y,X)$ uniquely in terms of the element $\eta_{X}(id_X)$.

It remains only to see that there is no condition on the element $\eta_X(id_X)$, hence that with $\eta_Y(f)$ defined this way, the commutativity of all the remaining naturality squares is implies: The general naturality square for a morphism $Y_2 \overset{g}{\longrightarrow} Y_1$ is of the form

$$
  \array{
    & 
    Hom_{\mathcal{C}}(Y_1,X)
      &\overset{\eta_{Y_1}}{\longrightarrow}&
    \mathbf{Y}(Y_1)
    \\ 
    & 
    {}^{\mathllap{ Hom_{\mathcal{C}}(g,X) }}
    \big\downarrow 
      && 
    \big\downarrow{}^{\mathrlap{\mathbf{Y}(g)}}
    \\
    & 
    Hom_{\mathcal{C}}(Y_2,X)
    &\underset{\eta_{Y_2}}{\longrightarrow}&
    \mathbf{Y}(Y_2)
  }
  \phantom{AAAA}
  \array{
     \{f_1\}
     &\longrightarrow&
     \{ \mathbf{Y}(f_1)( \eta_X(id_X) )  \}
     \\
     \big\downarrow 
     &&
     \big\downarrow
     \\
     \{f_2 = f_1\circ g\}
     &\longrightarrow&
     \{\mathbf{Y}(f_2)( \eta_X(id_X) ) = \mathbf{Y}(g) \circ \mathbf{Y}(f_1) ( \eta_X(id_X) ) \}
  }
$$

As shown on the right, the commutativity of this diagram now follows from the [[functor|functoriality]] $\mathbf{Y}(f_2) = \mathbf{Y}(f_1 \circ g)$ of the [[presheaf]] $\mathbf{Y}$.

=--

As a direct corollary, we obtain the statement of the [[Yoneda embedding]]:

+-- {: .num_prop #YonedaEmbedding}
###### Proposition
**([[Yoneda embedding]])**

The assignment of [[representable presheaves|represented presheaves]] (eq:YonedaFunctor) is a [[fully faithful functor]] (Def. \ref{FullyFaithfulFunctor}), hence exhibits a [[full subcategory]] inclusion

$$
  y
  \;\;\colon\;\;
  \array{
    \mathcal{C}
      &\overset{\phantom{AAAA}}{\hookrightarrow}&
    [\mathcal{C}^{op}, Set]
    \\
    X
    &\mapsto&
    Hom_{\mathcal{C}}(-,X)
  } 
$$

of the given [[category]] $\mathcal{C}$ into its [[category of presheaves]].

=--

+-- {: .proof}
###### Proof

We need to show that for all $X_1, X_2 \in Obj_{\mathcal{C}}$ the function

\[
  \label{HomFunctionForYonedaEmbedding}
  \array{
    Hom_{\mathcal{C}}(X_1, X_2)
      &\overset{ }{\longrightarrow}&
    Hom_{[\mathcal{C}^{op}, Set]}
    \big(
      Hom_{\mathcal{C}}(-,X_1)
       \;,\;
      Hom_{\mathcal{C}}(-,X_2)
    \big)
    \\
    f 
      &\mapsto&  
    Hom_{\mathcal{C}}(-,f)
  }
\]

is a [[bijection]]. But the [[Yoneda lemma]] (Prop. \ref{YonedaLemma}) states a bijection the other way around

$$
  \array{
    Hom_{[\mathcal{C}^{op}, Set]}
    \big(
      Hom_{\mathcal{C}}(-,X_1)
       \;,\;
      Hom_{\mathcal{C}}(-,X_2)
    \big)
      &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(-,X_2)(X_1)
      &=&
    Hom_{\mathcal{C}}(X_1, X_2)
    \\
    \eta && \mapsto && \eta_{X_1}( id_{X_1} ) 
    \\
    Hom_{\mathcal{C}}(-,f) 
      && \mapsto && 
    Hom_{\mathcal{C}}(X_1,f)(id_{X_1}) = f
   }
$$

and hence it is sufficient to see that this is a [[left inverse]] to (eq:HomFunctionForYonedaEmbedding). This follows by inspection, as shown in the third line above.


=--



### Adjunctions

We discuss four equivalent definitions of [[adjunctions]]:

1. via hom-isomorphism (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets} below);

1. via [[adjunction unit]] and -[[adjunction counit|counit]] satisfying [[triangle identities]] (Prop. \ref{AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat});

1. via [[representing objects]] (Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject});

1. via [[universal morphisms]] (Prop. \ref{CollectionOfUniversalArrowsEquivalentToAdjointFunctor} below).

Then we discuss some key properties:

1. uniqueness of adjoints (Prop. \ref{UniquenessOfAdjoints} below),

1. epi/mono/iso-characterization of adjunction (co-)units (Prop. \ref{FullyFaithfulAndInvertibleAdjoints} below).

$\,$


+-- {: .num_defn #AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}
###### Definition
**([[adjoint functors]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be two [[categories]] (Def. \ref{Categories}), and let 

$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{}
  \mathcal{C}
$$

be a [[pair]] of [[functors]] between them (Def. \ref{Functors}), as shown. Then this is called a _pair of [[adjoint functors]]_ (or an _[[adjoint pair]] of [[functors]]_) with $L$ _[[left adjoint]]_ and $R$ _[[right adjoint]]_, denoted 

$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{\bot}
  \mathcal{C}
$$

if there exists a [[natural isomorphism]] (Def. \ref{NaturalTransformations}) between the [[hom-functors]] (Example \ref{HomFunctor}) of the following form:

\[
  \label{HomIsomorphismForAdjointFunctors}
  Hom_{\mathcal{D}}(L(-),-) \;\simeq\; Hom_{\mathcal{C}}(-,R(-))
  \,.
\]

This means that for all [[objects]] $c \in \mathcal{C}$ and $d \in \mathcal{D}$ there is a [[bijection]] of [[hom-sets]]

$$
  \array{
    Hom_{\mathcal{D}}(L(c),d) 
      &\overset{\simeq}{\longrightarrow}& 
    Hom_{\mathcal{C}}(c,R(d))
    \\
    ( L(c) \overset{f}{\to} d )
    &\mapsto&
    (c \overset{\widetilde f}{\to} R(d))
  }
$$

which is [[natural bijection|natural]] in $c$ and $d$.  This isomorphism is called the _adjunction hom-isomorphism_ and the [[image]] $\widetilde f$ of amorphism $f$ under this bijections is called the _[[adjunct]]_ of $f$. Conversely, $f$ is called the _[[adjunct]]_ of $\widetilde f$.

Naturality here means that for every [[morphism]] $g \colon c_2 \to c_1$ in $\mathcal{C}$ and for every [[morphisms]] $h\colon d_1\to d_2$ in $\mathcal{D}$, the resulting square

\[
  \label{NaturalitySquareForAdjointnessOfFunctors}
  \array{
    Hom_{\mathcal{D}}(L(c_1), d_1) 
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c_1, R(d_1))
    \\
    {}^{\mathllap{Hom_{\mathcal{D}}(L(g), h)}}\big\downarrow
     &&
    \big\downarrow^{\mathrlap{Hom_{\mathcal{C}}(g, R(h))}}
    \\
    Hom_{\mathcal{D}}(L(c_2),d_2)
    &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c_2,R(d_2))
  }
\]

[[commuting square|commutes]] (see also at _[[hom-functor]]_ for the definition of the vertical maps here). 

Explicitly, this commutativity, in turn, means that for every morphism $f \;\colon\; L(c_1) \to d_1$ with [[adjunct]] $\widetilde f \;\colon\; c_1 \to R(d_1)$, the adjunct of the [[composition]] is

$$
  \widetilde{
  \array{
    L(c_1) &\overset{f}{\longrightarrow}& d_1
    \\
    {}^{\mathllap{L(g)}}\big\uparrow && \big\downarrow^{\mathrlap{h}}
    \\
    L(c_2) && d_2
  }
  }
  \;\;\;=\;\;\;
  \array{
    c_1 &\overset{\widetilde f}{\longrightarrow}& R(d_1)
    \\
    {}^{\mathllap{g}}\big\uparrow && \big\downarrow^{\mathrlap{R(h)}}
    \\
    c_2 && R(d_2)
  }
$$

=--

+-- {: .num_defn #AdjunctionUnitFromHomIsomorphism}
###### Definition
**([[adjunction unit]] and [[adjunction counit|counit]])

Given a pair of [[adjoint functors]] 

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{\bot}
  \mathcal{D}
$$

according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}, one says that 

1. for any $c \in \mathcal{C}$ the [[adjunct]] of the [[identity morphism]] on  $L(c)$ is the _[[unit of an adjunction|unit morphism]]_ of the adjunction at that object, denoted

   $$
     \eta_c \coloneqq \widetilde{id_{L(c)}} \;\colon\; c \longrightarrow R(L(c))
   $$

1. for any $d \in \mathcal{D}$ the [[adjunct]] of the [[identity morphism]] on  $R(d)$ is the _[[counit of an adjunction|counit morphism]]_ of the adjunction at that object, denoted

   $$
     \epsilon_d \;\colon\; L(R(d)) \longrightarrow d
   $$



=--

+-- {: .num_prop #GeneralAdjunctsInTermsOfAdjunctionUnitCounit}
###### Proposition
**(general [[adjuncts]] in terms of [[adjunction unit|unit/counit]])**

Consider a pair of [[adjoint functors]] 

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{\bot}
  \mathcal{D}
$$

according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}, with [[adjunction units]] $\eta_c$ and [[adjunction counits]] $\epsilon_d$ according to Def. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}.

Then

1. The [[adjunct]] $\widetilde f$ of any morphism $L(c) \overset{f}{\to} d$ is obtained from $R$ and $\eta_c$ as the [[composition|composite]]

   \[
     \label{AdjunctFormula}
     \widetilde f 
     \;\colon\;
     c 
       \overset{\eta_c}{\longrightarrow} 
     R(L(c))
       \overset{R(f)}{\longrightarrow}
     R(d)
   \]

   Conversely, the [[adjunct]] $f$ of any morphism $c \overset{\widetilde f}{\longrightarrow} R(d)$ is obtained from $L$ and $\epsilon_d$ as

   \[
     \label{ConverseAdjunctFormula}
     f
     \;\colon\;
     L(c) 
       \overset{L(\widetilde f)}{\longrightarrow} 
     R(L(d))
       \overset{\epsilon_d}{\longrightarrow}
     d
   \]

1. The [[adjunction units]] $\eta_c$ and [[adjunction counits]] $\epsilon_d$ are components of [[natural transformations]] of the form

   $$
     \eta \;\colon\; Id_{\mathcal{C}} \Rightarrow R \circ L
   $$

   and

   $$
     \epsilon \;\colon\; L \circ R \Rightarrow Id_{\mathcal{D}}
   $$

1. The [[adjunction unit]] and [[adjunction counit]] satisfy the [[triangle identities]], saying that

   \[
      \label{TriangleIdentities}
      id_{L(c)}
      \;\colon\;
      L(c) 
        \overset{L(\eta_c)}{\longrightarrow} 
      L(R(L(c))) 
        \overset{\epsilon_{L(c)}}{\longrightarrow}
      L(c)
   \]

   and

   $$
     id_{R(d)}
     \;\colon\;
     R(d)
       \overset{\eta_{R(d)}}{\longrightarrow}
     R(L(R(d)))
       \overset{R(\epsilon_d)}{\longrightarrow}
     R(d)
   $$

=--

+-- {: .proof}
###### Proof

For the first statement, consider the [[naturality square]] (eq:NaturalitySquareForAdjointnessOfFunctors) in the form 

$$
  \array{
    id_{L(c)}
     \in 
    &
    Hom_{\mathcal{D}}(L(c), L(c)) 
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c, R(L(c)))
    \\
    &
    {}^{\mathllap{Hom_{\mathcal{D}}(L(id), f)}}\big\downarrow
     &&
    \big\downarrow^{\mathrlap{Hom_{\mathcal{C}}(id, R(f))}}
    \\
    &
    Hom_{\mathcal{D}}(L(c), d)
    &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}( c, R(d) )
  }
$$

and consider the element $id_{L(c_1)}$ in the top left entry. Its image under going down and then right in the diagram is $\widetilde f$, by Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}. On the other hand, its image under going right and then down is $ R(f)\circ \eta_{c}$, by Def. \ref{AdjunctionUnitFromHomIsomorphism}. Commutativity of the diagram means that these two morphisms agree, which is the statement to be shown, for the adjunct of $f$.

The converse formula follows analogously.

The third statement follows directly from this by applying these formulas for the [[adjuncts]] twice and using that the result must be the original morphism:

$$
  \begin{aligned}
    id_{L(c)}
    & =
    \widetilde \widetilde { id_{L(c)} }
    \\
    & = \widetilde{ c \overset{\eta_c}{\to} R(L(c))  }
    \\
    & = 
     L(c) 
       \overset{L(\eta_c)}{\longrightarrow} 
     L(R(L(c))) 
       \overset{\epsilon_{L(c)}}{\longrightarrow}
     L(c)
  \end{aligned}
$$

For the second statement, we have to show that for every moprhism $f \colon c_1 \to c_2$ the following [[commuting square|square commutes]]:

$$
  \array{    
     c_1 &\overset{f}{\longrightarrow}& c_2
     \\
     {}^{\mathllap{\eta_{c_1}}}\big\downarrow 
       && 
     \big\downarrow^{\mathrlap{\eta_{c_2}}}
     \\
     R(L(c_1))
      &\underset{ R(L(f)) }{\longrightarrow}&
     R(L(c_2))
  }
$$

To see this, consider the [[naturality square]] (eq:NaturalitySquareForAdjointnessOfFunctors) in the form 

$$
  \array{
    id_{L(c_2)}
    \in
    & Hom_{\mathcal{D}}(L(c_2), L(c_2)) 
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c_2, R(L(c_2)))
    \\
    &
    {}^{\mathllap{Hom_{\mathcal{D}}(L(f),id_{L(c_2)})}}\big\downarrow
     &&
    \big\downarrow^{\mathrlap{Hom_{\mathcal{C}}(f, R(id_{L(c_2)}))}}
    \\
    &
    Hom_{\mathcal{D}}(L(c_1),L(c_2))
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c_1,R(L(c_1)))
  }
$$

The image of the element $id_{L(c_2)}$ in the top left along the right and down is $ f \circ \eta_{c_2}$, by Def. \ref{AdjunctionUnitFromHomIsomorphism}, while its image down and then to the right is $\widetilde {L(f)} = R(L(f)) \circ \eta_{c_1}$, by the previous statement. Commutativity of the diagram means that these two morphisms agree, which is the statement to be shown.

The argument for the naturality of $\epsilon$ is directly analogous.


=--

+-- {: .num_prop #AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat}
###### Proposition
**([[adjoint functors]] equivalent to [[adjunction]] in [[Cat]])**

Two functors

$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{}
  \mathcal{C}
$$

are an [[adjoint pair]] in the sense that there is a [[natural isomorphism]] (eq:HomIsomorphismForAdjointFunctors) according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}, precisely if they participate in an _[[adjunction]]_ in the [[2-category]] [[Cat]], meaning that 

1. there exist [[natural transformations]] 

   $$
     \eta \;\colon\; Id_{\mathcal{C}} \Rightarrow R \circ L
   $$

   and

   $$
     \epsilon \;\colon\; L \circ R \Rightarrow Id_{\mathcal{D}}
   $$

2. which satisfy the [[triangle identities]]

   $$
      id_{L(c)}
      \;\colon\;
      L(c) 
        \overset{L(\eta_c)}{\longrightarrow} 
      L(R(L(c))) 
        \overset{\epsilon_{L(c)}}{\longrightarrow}
      L(c)
   $$

   and

   $$
     id_{R(d)}
     \;\colon\;
     R(d)
       \overset{\eta_{R(d)}}{\longrightarrow}
     R(L(R(d)))
       \overset{R(\epsilon_d)}{\longrightarrow}
     R(d)
   $$

=--

+-- {: .proof}
###### Proof

That a hom-isomorphism (eq:HomIsomorphismForAdjointFunctors) implies units/counits satisfying the [[triangle identities]] is the statement of the second two items of Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}.

Hence it remains to show the converse. But the argument is along the same lines as the proof of Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}: We now _define_ forming of adjuncts by the formula (eq:AdjunctFormula). That the resulting assignment $f \mapsto \widetilde f$ is an [[isomorphism]] follows from the computation

$$
  \begin{aligned}
    \widetilde {\widetilde f}
    & =
    \widetilde{ c \overset{\eta_c}{\to} R(L(c)) \overset{R(f)}{\to} R(d) }
    \\
    & =
    L(c) \overset{L(\eta_c)}{\to} L(R(L(c))) \overset{L(R(f))}{\to} L(R(d)) \overset{\epsilon_d}{\to} d
    \\ 
    & = 
    L(c) \overset{L(\eta_c)}{\to} L(R(L(c)))
         \overset{ \epsilon_{L(c)} }{\to}  L(c)
         \overset{f}{\longrightarrow} d
    \\
    & =  L(c) \overset{f}{\longrightarrow} d
  \end{aligned}
$$

where, after expanding out the definition, we used [[natural transformation|naturality]] of $\epsilon$ and then the [[triangle identity]]. 

Finally, that this construction satisfies the naturality condition (eq:NaturalitySquareForAdjointnessOfFunctors) follows from the functoriality of the functors involved, and the naturality of the unit/counit: 

$$
  \array{
    c_2 &\overset{ \eta_{c_2} }{\longrightarrow}& R(L(c_2))
    \\
    {}^{\mathllap{g}}\downarrow && \downarrow^{\mathrlap{R(L(g))}}
    & \searrow^{\mathrlap{ R( L(g) \circ f ) }}
    \\
    c_1 
      &\overset{\eta_{c_1}}{\longrightarrow}& 
    R(L(c_1))
     &\overset{R(f)}{\longrightarrow}&
    R(d_1)
    \\
    && & {}_{R( h\circ f)}\searrow & \downarrow^{\mathrlap{ R(h) }}
    \\
    && && R(d_2)
  }
$$


=--



The condition (eq:HomIsomorphismForAdjointFunctors) on adjoint functors $L \dashv R$ in Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets} implies in particular that for every [[object]] $d \in \mathcal{D}$ the functor $Hom_{\mathcal{D}}(L(-),d)$ is a _[[representable functor]]_ with _[[representing object]]_ $R(d)$. The following Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject} observes that the existence of such [[representing objects]] for all $d$ is, in fact, already sufficient to imply that there is a right adjoint functor.

This equivalent perspective on adjoint functors makes manifest that adjoint functors are, if they exist, unique up to natural isomorphism, this is Prop. \ref{UniquenessOfAdjoints} below.



+-- {: .num_prop #AdjointFunctorFromObjectwiseRepresentingObject}
###### Proposition
**([[adjoint functor]] from objectwise [[representing objects]])**

A [[functor]] $L \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ has a [[right adjoint]] $R \;\colon\; \mathcal{D} \to \mathcal{C}$, according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}, already if 
for all [[objects]] $d \in \mathcal{D}$ there is an object $R(d) \in \mathcal{C}$ such that there is a [[natural isomorphism]]

   $$ 
     Hom_{\mathcal{D}}(L(-),d)
     \underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}
     Hom_{\mathcal{C}}(-,R(d))
     \,,
   $$

   hence for each [[object]] $c \in \mathcal{C}$ a [[bijection]]

   $$
     Hom_{\mathcal{D}}(L(c),d)
     \underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}
     Hom_{\mathcal{C}}(c,R(d))
   $$

   such that for each [[morphism]] $g \;\colon\; c_2 \to c_1$, the following [[commuting diagram|diagram commutes]]

   \[
     \label{HalfNaturalitySquareForAdjointnessOfFunctors}
     \array{
       Hom_{\mathcal{D}}(L(c_1),d)
         &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
       Hom_{\mathcal{C}}(c_1,R(d))
       \\
       {}^{\mathllap{ Hom_{\mathcal{C}}(L(g),id_d) }}
       \big\downarrow 
       &&
       \big\downarrow^{\mathrlap{ Hom_{\mathcal{C}}( f, id_{R(d)}  ) }}
       \\
       Hom_{\mathcal{D}}(L(c_2),d)
         &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
       Hom_{\mathcal{C}}(c_2,R(d))
     }
   \]

   (This is as in (eq:NaturalitySquareForAdjointnessOfFunctors), except that only naturality in the first variable is required.)

In this case there is a unique way to extend $R$ from a function on [[objects]] to a function on [[morphisms]] such as to make it a [[functor]] $R \colon \mathcal{D} \to \mathcal{C}$ which is [[right adjoint]] to $L$.
, and hence the statement is that with this, naturality in the second variable is already implied.

=--

+-- {: .proof}
###### Proof

Notice that 

1. in the language of [[presheaves]] (Example \ref{CategoryOfPresheaves}) the assumption is that for each $d \in \mathcal{D}$ the presheaf 

   $$
     Hom_{\mathcal{D}}(L(-),d)
     \;\in\;
     [\mathcal{D}^{op}, Set]
   $$

   is [[representable functor|represented]] (eq:YonedaFunctor) by the object $R(d)$, and [[natural transformation|naturally]] so. 

1. In terms of the [[Yoneda embedding]] (Prop. \ref{YonedaEmbedding})

   $$
     y 
       \;\colon\;
     \mathcal{D}
      \hookrightarrow
     [\mathcal{D}^{op}, Set]
   $$ 

   we have 

   \[
     \label{YonedanotationForRepresentable}
     Hom_{\mathcal{C}}(-,R(d))
     =
     y(R(d))
   \]



The condition (eq:NaturalitySquareForAdjointnessOfFunctors) says equivalently that $R$ has to be such that for all [[morphisms]] $h \;\colon\; d_1 \to d_2 $ the following diagram in the [[category of presheaves]] $[\mathcal{C}^{op}, Set]$ [[commuting diagram|commutes]]

$$
  \array{
    Hom_{\mathcal{D}}(L(-),d_1)
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(-,R(d_1))
    \\
    {}^{\mathllap{ Hom_{\mathcal{C}}( L(-) , h ) }}
    \big\downarrow 
    &&
    \big\downarrow^{\mathrlap{ Hom_{\mathcal{C}}( -, R(h)  ) }}
    \\
    Hom_{\mathcal{D}}(L(-),d_2)
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(-, R(d_2))
  }
$$

This manifestly has a unique solution 

$$
  y(R(h))
  \;=\;
  Hom_{\mathcal{C}}(-,R(h))
$$ 

for every morphism $h \colon d_1 \to d_2$ under  $y(R(-))$ (eq:YonedanotationForRepresentable). But the [[Yoneda embedding]] $y$ is a [[fully faithful functor]] (Prop. \ref{YonedaEmbedding}), which means that thereby also $R(h)$ is uniquely fixed.

=--

We consider one more equivalent characterization of [[adjunctions]]:

+-- {: .num_defn #UniversalArrow}
###### Definition
**([[universal morphism]])**

Let $\mathcal{C}, \mathcal{D}$ be two [[categories]] (Def. \ref{Categories})
and let $R \;\colon\; \mathcal{D} \to \mathcal{C}$ be a [[functor]] (Def. \ref{Functors})

Then for $c\in \mathcal{C}$ an [[object]], a _[[universal morphism]] from $c$ to $R$_ is

1. an [[object]] $L(c)\in \mathcal{D}$,

1. a [[morphism]] $\eta_c \;\colon\; c \to R(L(c))$, to be called the _[[adjunction unit|unit]]_,

such that for any $d\in \mathcal{D}$, any morphism $f \colon c\to R(d)$ factors through this unit $\eta_c$ as 

\[
  \label{UniversalArrowFactorization}
  f
  \;=\;
  \eta_c \circ R(\widetilde f)
  \phantom{AAAA}
  \array{
    && c 
    \\
    & {}^{\mathllap{\eta_c}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    R(L(c)) &&\underset{R (\widetilde f)}{\longrightarrow}&& R(d)
    \\
    \\
    L(c) &&\underset{ \widetilde f}{\longrightarrow}&& d
  }
\]

for a _unique_ morphism $\widetilde f  \;\colon\; L(c) \longrightarrow d$, to be called the [[adjunct]] of $f$.  

=--

+-- {: .num_prop #CollectionOfUniversalArrowsEquivalentToAdjointFunctor}
###### Proposition
**(collection of [[universal morphisms]] equivalent to [[adjoint functor]])**

Let $R \;\colon\; \mathcal{D} \to \mathcal{C}$ be a [[functor]] (Def. \ref{Functors}). Then the following are equivalent:

1. $R$ has a [[left adjoint]] functor $L \colon \mathcal{C} \to \mathcal{D}$ according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets},


1. For every [[object]] $c \in \mathcal{C}$ there is a [[universal morphism]] $c \overset{\eta_c}{\longrightarrow} R(L(c))$, according to Def. \ref{UniversalArrow}.

=--


+-- {: .proof}
###### Proof

In one direction, assume a [[left adjoint]] $L$ is given. Define the would-be universal arrow at $c \in \mathcal{C}$ to be the [[unit of an adjunction|unit of the adjunction]] $\eta_c$ via Def. \ref{AdjunctionUnitFromHomIsomorphism}. Then the statement that this really is a universal arrow is implied by Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}.

In the other direction, assume that universal arrows $\eta_c$ are given. The uniqueness clause in Def. \ref{UniversalArrow} immediately implies  [[bijections]] 

$$
  \array{
    Hom_{\mathcal{D}}(L(c),d) 
      &\overset{\simeq}{\longrightarrow}& 
    Hom_{\mathcal{C}}(c,R(d))
    \\
    \left( 
      L(c) \overset{\widetilde f}{\to} d
    \right)
      &\mapsto&
    \left(
      c \overset{\eta_c}{\to} R(L(c)) \overset{ R(\widetilde f) }{\to} R(d)
    \right)
  }
$$

Hence to satisfy (eq:HomIsomorphismForAdjointFunctors) it remains to show that these are [[natural transformation|natural]] in both variables. In fact, by Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject} it is sufficient to show naturality in the variable $d$. But this is immediate from the functoriality of $R$ applied in (eq:UniversalArrowFactorization): For $h \colon d_1 \to d_2$ any [[morphism]], we have

$$
  \array{
    && c 
    \\
    & {}^{\mathllap{\eta_c}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    R (L(c)) &&\underset{R (\widetilde f)}{\longrightarrow}&& R(d_1)
    \\
    && {}_{\mathllap{ R( h\circ \widetilde f ) }}\searrow && \downarrow^{\mathrlap{R(h)}}
    \\
    && && R(d_2)
  }
$$


=--


$\,$

After these equivalent characterizations of [[adjoint functors]], we now consider some of their main properties:

+-- {: .num_prop #UniquenessOfAdjoints}
###### Proposition
**([[adjoint functors]] are unique up to [[natural isomorphism]])**

The [[left adjoint]] or [[right adjoint]] to a [[functor]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}), if it exists, is unique up to  [[natural isomorphism]] (Def. \ref{NaturalTransformations}).

=--

+-- {: .proof}
###### Proof

Suppose the functor $L \colon \mathcal{D} \to \mathcal{C}$ is given, and we are asking for uniqueness of its right adjoint, if it exists. The other case is directly analogous.

Suppose that $R_1, R_2 \;\colon\; \mathcal{C} \to \mathcal{D}$ are two [[functors]] which both are [[right adjoint]] to $L$. Then for each $d \in \mathcal{D}$ the corresponding two hom-isomorphisms (eq:HomIsomorphismForAdjointFunctors) combine to say that there is a [[natural isomorphism]]/

$$
  \Phi_d
  \;\colon\;
  Hom_{\mathcal{C}}(-,R_1(d))
  \;\simeq\;
  Hom_{\mathcal{C}}(-,R_2(d))
$$

As in the proof of Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject}, the [[Yoneda lemma]] implies that 

$$
  \Phi_d \;=\; y( \phi_d )
$$

for some [[isomorphism]]

$$
  \phi_d \;\colon\;  R_1(d) \overset{\simeq}{\to} R_2(d)
  \,.
$$

But then the uniqueness statement of Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject} implies that the collection of these isomorphisms for each object constitues a [[natural isomorphism]] between the functors (Def. \ref{NaturalTransformations}).

=--


+-- {: .num_prop #FullyFaithfulAndInvertibleAdjoints}
###### Proposition
**(characterization of epi/mono/iso (co-)unit of adjunction)**

Let $L \dashv R$ be a pair of adjoint functors (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}). Then the following holds:

* $R$ is [[faithful functor|faithful]] precisely if the component of the [[unit of an adjunction|counit]] over every object $x$ is an [[epimorphism]] $L R x \stackrel{}{\to} x $ (Def. \ref{Monomorphism});

* $R$ is [[full functor|full]] precisely if the component of the [[unit of an adjunction|counit]] over every object $x$ is a [[split monomorphism]] $L R x \stackrel{}{\to} x $;

* $L$ is [[faithful functor|faithful]] precisely if the component of the [[unit of an adjunction|unit]] over every object $x$ is a [[monomorphism]] $x \hookrightarrow R L x $;

* $L$ is [[full functor|full]] precisely if the component of the [[unit of an adjunction|unit]] over every object $x$ is a [[split epimorphism]] $x \to R L x $;

* $R$ is [[full and faithful functor|full and faithful]] 
  (exhibits a [[reflective subcategory]])
  precisely if
  the [[unit of an adjunction|counit]] is a [[natural isomorphism]] 
  $\epsilon : L \circ R \stackrel{\simeq}{\to} Id_D$

* $L$ is [[full and faithful functor|full and faithful]]
  (exhibits a [[coreflective subcategory]]) precisely if
  the [[unit of an adjunction|unit]] 
  is a natural isomorphism 
  $\eta : Id_C \stackrel{\simeq}{\to} R \circ L$.

* The following are equivalent:

  * $L$ and $R$ are both [[full and faithful functor|full and faithful]];

  * $L$ is an [[equivalence of categories|equivalence]];

  * $R$ is an [[equivalence of categories|equivalence]].

=--

+-- {: .proof}
###### Proof

For the characterization of faithful $R$ by epi counit components, use from Def. \ref{Monomorphism} that $L R x \to x$ being an epimorphism means that the induced [[function]]

$$
  Hom(x, a) \to Hom(L R x, a)
$$

is an [[injection]] for all objects $a$. By the adjunction hom-isomorphism (eq:HomIsomorphismForAdjointFunctors)

$$
  Hom(L R x , a ) \stackrel{\simeq}{\to} Hom(R x, R a)
  \,,
$$ 

the formula for [[adjuncts]] (Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}) and the [[triangle identity]] (eq:TriangleIdentities), this is  such that the composite

$$
 R_{x,a} :  Hom(x,a) \to Hom(L R x, a) \stackrel{\simeq}{\to}
    Hom(R x, R a)
$$

is the component map of the functor $R$:

$$
  \begin{aligned}
    (x \stackrel{f}{\to} a) & \mapsto 
    (L R x \to x \stackrel{f}{\to} a)
    \\
    & \mapsto 
    (R L R x \to R x \stackrel{R f}{\to} R a)
    \\
    & \mapsto 
    (R x \to R L R x \to R x \stackrel{R f}{\to} R a)     
    \\
    & = (R x \stackrel{R f}{\to} R a)
  \end{aligned}
  \,.
$$

Therefore $R_{x,a}$ is injective for all $x,a$, hence $R$ is faithful, precisely if $L R x \to x$ is an epimorphism for all $x$. The characterization of $R$ full is just the same reasoning applied to the fact that $\epsilon_x \colon L R x \to x$ is a [[split monomorphism]] iff for all objects $a$ the induced function
\[
  Hom(x, a) \to Hom(L R x, a)
\]
is a surjection.

For the characterization of faithful $L$ by monic units notice that analogously (as discussed at [[monomorphism]]) $x \to R L x$ is a monomorphism if for all objects $a$ the function

$$
  Hom(a,x ) \to Hom(a, R L x)
$$

is an injection. Analogously to the previous argument we find that this is equivalent to 

$$
  L_{a,x} : Hom(a,x ) \to Hom(a, R L x) \stackrel{\simeq}{\to} Hom(L a, L x)
$$

being an injection. So $L$ is faithful precisely if all $x \to R L x$ are monos. For $L$ full, it's just the same applied to $x \to R L x$ [[split epimorphism]] iff the induced function
$$
  Hom(a,x ) \to Hom(a, R L x)
$$
is a surjection, for all objects $a$.

The proof of the other statements proceeds analogously.

=--





### Equivalences


+-- {: .num_defn #AdjointEquivalenceOfCategories}
###### Definition
**([[adjoint equivalence of categories]])**

Let $\mathcal{C}$, $\mathcal{D}$ be two [[categories]] (Def. \ref{Categories}). Then an _[[adjoint equivalence of categories]]_ between them is a [[pair]] [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets})

$$
  \array{
    \mathcal{C}
      \underoverset
        {\underset{R}{\longrightarrow}}
        {\overset{L}{\longleftarrow}}
        {\phantom{AA} \simeq \phantom{AA}}
    \mathcal{D}
  }
$$

such that their [[unit of an adjunction|unit]] $\eta$ and [[counit of an adjunction|counit]] $\epsilon$ (Def. \ref{AdjunctionUnitFromHomIsomorphism}) are [[natural isomorphisms]] (as opposed to just being [[natural transformations]])


$$
  \eta\;\colon\; id_{\mathcal{D}} \overset{\simeq}{\Rightarrow} R \circ L 
  \phantom{AAA}
   \text{and}
  \phantom{AAA}
  \epsilon\;\colon\;
  L \circ R \overset{\simeq}{\Rightarrow} id_{\mathcal{C}}
  \,.
$$

=--

There is also the following, seemingly weaker, notion:

+-- {: .num_defn #EquivalenceOfCategories}
###### Definition
**([[equivalence of categories]])**

Let $\mathcal{C}$, $\mathcal{D}$ be two [[categories]] (Def. \ref{Categories}). Then an _[[equivalence of categories]]_

$$
  \array{
    \mathcal{C}
      \underoverset
        {\underset{R}{\longrightarrow}}
        {\overset{L}{\longleftarrow}}
        {\phantom{AA} \simeq \phantom{AA}}
    \mathcal{D}
  }
$$

is a [[pair]] of [[functors]] back and forth, as shown (Def. \ref{Functors}), together with [[natural isomorphisms]] (Def. \ref{NaturalTransformations}) between their [[composition]] and the [[identity functors]]:

$$
  id_{\mathcal{D}} \overset{\simeq}{\Rightarrow} R \circ L 
  \phantom{AAA}
   \text{and}
  \phantom{AAA}
  L \circ R \overset{\simeq}{\Rightarrow} id_{\mathcal{C}}
  \,.
$$


=--

If a functor participates in an equivalence of categories, that functor alone is usually already called an equivalence of categories. If there is any equivalence of categories between two categories, these categories are called _equivalent_.


+-- {: .num_prop #EveryEquivalenceOfCategoriesComesFromAnAdjointEquivalence}
###### Proposition
**(every [[equivalence of categories]] comes from an [[adjoint equivalence of categories]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be two [[categories]] (Def. \ref{Categories}). Then the they are [[equivalence of categories|equivalent]] (Def. \ref{EquivalenceOfCategories}) precisely if there exists an [[adjoint equivalence of categories]] between them (Def. \ref{AdjointEquivalenceOfCategories}).

Moreover, let $R \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ be a [[functor]] (Def. \ref{Functors}) which participates in an [[equivalence of categories]] (Def. \ref{EquivalenceOfCategories}). Then for every functor $L \;\colon\; \mathcal{D} \to \mathcal{C}$ equipped with a [[natural isomorphism]]

$$
  \eta 
    \;\colon\;
  id_{\mathcal{D}}
    \overset{\simeq}{\Rightarrow}
  R \circ L
$$

there exists a [[natural isomorphism]]

$$
  \epsilon
  \;\colon\;
  L \circ R \overset{\simeq}{\Rightarrow} id_{\mathcal{C}}
$$

which completes this to an [[adjoint equivalence of categories]] (Def. \ref{AdjointEquivalenceOfCategories}).

=--

$\,$

### Modalities
  {#Modalities}

Generally, a [[full subcategory]]-inclusion (Def. \ref{FullyFaithfulFunctor}) may be thought of as a consistent [[proposition]] about [[objects]] in a [[category]]: The objects in the full subcategory are those that have the given property. 

This basic situation becomes particularly interesting when the inclusion functor has a [[left adjoint]] or a [[right adjoint]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}), in which case one speaks of a _[[reflective subcategory]]_, or a _[[coreflective subcategory]]_, respectively (Def. \ref{ReflectiveSubcategory} below). The [[adjunction]] now implies that each [[object]] is _[[reflector|reflected]]_ or _[[coreflector|coreflected]]_ into the subcategory, and equipped with a comparison morphism to or from its (co-)reflection (the adjunction (co-)unit, Def. \ref{AdjunctionUnitFromHomIsomorphism}). This comparison morphism turns out to always be an idempotent (co-)projection, in a sense made precise by Prop. \ref{ModalOpIdempotent} below.

This means that, while any object may not fully enjoy the property that defines the subcategory, one may ask for the "aspect" of it that does, which is what is (co-)projected out. Regarding objects only via these aspects of them hence means to regard them only _locally_ (where they exhibit that aspect) or only in the _mode_ of focus on this aspect. Therefore one also calls the (co-)reflection operation into the given subcategory a _([[colocalization|co]]-)[[localization]]_ or _([[comodal operator|co-]])[[modal operator]]_, or _[[modality]]_, for short (Def. \ref{ModalOperator} below).  

One finds that (co-)modalities are a fully equivalent perspective on  the (co-)reflective subcategories of their fully _([[comodal object|co-]])[[modal objects]]_ (Def. \ref{ModalObjects} below), this is the statement of Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories} below.



$\,$

+-- {: .num_defn #ReflectiveSubcategory}
###### Definition
**([[reflective subcategory]] and [[coreflective subcategory]])**

Let $\mathcal{D}$ be a [[category]] (Def. \ref{Categories}) and

$$
  \mathcal{C}
  \overset{\phantom{AA}\iota \phantom{AA}}{\hookrightarrow}
  \mathcal{D}
$$

a [[full subcategory]]-inclusion (hence a [[fully faithful functor]] Def. \ref{FullyFaithfulFunctor}). This is called:

1. a _[[reflective subcategory]] inclusion_ if the inclusion functor $\iota$ has a [[left adjoint]] $L$ def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets})

   $$
     \mathcal{C}
       \underoverset
         {\underset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}}
         {\overset{L}{\longleftarrow}}
         {\bot}
     \mathcal{D}
     \,,
   $$

   then called the _[[reflector]]_;

1. a _[[coreflective subcategory]]_-inclusion if the inclusion functor $\iota $ has a [[right adjoint]] $R$ (def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets})
   
   $$
     \mathcal{C}
       \underoverset
         \underset{R}{\longleftarrow}
         {\overset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}}
         {\bot}
     \mathcal{D}
     \,,
   $$

   then called the _[[coreflector]]_.

=--

+-- {: .num_example #ReflectiveSubcategoryInclusionOfSetsIntoGroupoids}
###### Example
**([[reflective subcategory]] inclusion of [[sets]] into [[small groupoid|small]] [[groupoids]])**

There is a [[reflective subcategory]]-inclusion (Def. \ref{ReflectiveSubcategory})

$$
  Set
    \underoverset
     {\underset{\phantom{AAAA}}{\hookrightarrow}}
     {\overset{\pi_0}{\longleftarrow}}
     {\bot}
  Grp
$$

of the [[category of sets]] (Example \ref{CategoryOfSets}) into the [[category]] [[Grpd]] (Example \ref{CategoriesOfSmallCategories}) of [[small groupoids|small]] [[groupoids]] (Example \ref{Groupoid}) where

* the [[right adjoint]] [[full subcategory]] inclusion (Def. \ref{FullyFaithfulFunctor}) sends a [[set]] $S$ to the [[groupoid]] with set of objects being $S$, and the only [[morphisms]] being the [[identity morphisms]] on these objects (also called the _[[discrete groupoid]]_ on $S$, but this terminology is ambiguous)

* the [[left adjoint]] [[reflector]] sends a [[small groupoid|small]] [[groupoid]] $\mathcal{G}$ to its set of [[connected components]], namely to the set of [[equivalence classes]] under the [[equivalence relation]] on the set of [[objects]], which regards two objects as equivalent, if there is any [[morphism]] between them.

=--


+-- {: .num_defn #ModalOperator}
###### Definition
**([[modality]])**

Let $\mathcal{D}$ be a [[category]] (Def. \ref{Categories}). Then 

1. a _[[modal operator]] on $\mathcal{D}$_ is

   1. an [[endofunctor]] 

      $$
        \bigcirc \;\colon\; \mathcal{D} \to \mathcal{D}
      $$

      whose [[full subcategory|full]] [[essential image]] we denote by

      $$
        Im(\bigcirc) 
          \overset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}
        \mathcal{D}
        \,,
      $$

   1. a [[natural transformation]] (Def. \ref{NaturalTransformations})
 
      \[
        \label{UnitOfAModalOperator}
        X \overset{\eta_X}{\longrightarrow} \bigcirc X
      \]

      for all [[objects]] $X \in \mathcal{D}$, 
      to be called the _unit morphism_;

   such that:

   * for every [[object]] $Y \in Im(\bigcirc) \hookrightarrow \mathcal{D}$ in the [[essential image]] of $\bigcirc$, every [[morphism]] $f$ into $Y$ factors _uniquely_ through the unit (eq:UnitOfAModalOperator)

     $$
       \array{
         && X
         \\
         & {}^{\mathllap{ \eta_X }}\swarrow && \searrow^{\mathrlap{f}}
         \\
         \mathrlap{\bigcirc X\;\;\;\;} && \underset{\exists !}{\longrightarrow} &&  Y & \in Im(\bigcirc)
       }
     $$

1. a _[[comodal operator]] on $\mathcal{D}$_ is

   1. an [[endofunctor]] 

      $$
        \Box \;\colon\; \mathcal{D} \to \mathcal{D}
      $$

      whose [[full subcategory|full]] [[essential image]] we denote by

      $$
        Im( \Box ) 
          \overset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}
        \mathcal{D}
      $$

   1. a [[natural transformation]] (Def. \ref{NaturalTransformations})
 
      \[
        \label{CounitOfModalOperator}
        \Box X \overset{ \epsilon_X }{\longrightarrow} X
      \]

      for all [[objects]] $X \in \mathcal{D}$, 
      to be called the _counit morphism_;

   such that:

   * for every [[object]] $Y \in Im( \Box ) \hookrightarrow \mathcal{D}$ in the [[essential image]] of $\Box$, every [[morphism]] $f$ out of $Y$ factors _uniquely_ through the counit (eq:UnitOfAModalOperator)

     $$
       \array{
          && X
          \\    
          & {}^{\mathllap{\epsilon_X}}\nearrow && \nwarrow^{\mathrlap{f}}
          \\
          \mathrlap{\Box X\;\;\;} && \underset{\exists !}{\longleftarrow} && Y \in Im( \Box )
       }
     $$

=--


+-- {: .num_prop #ModalOperatorsEquivalentToReflectiveSubcategories}
###### Proposition
**([[modal operators]] equivalent to [[reflective subcategories]])**

If 

$$
  \mathcal{C}
    \underoverset
      {\underset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

is a [[reflective subcategory]]-inclusion (Def. \ref{ReflectiveSubcategory}). Then the [[composition|composite]]  

$$
  \bigcirc
  \;\coloneqq\;
  \iota \circ L
  \;\colon\;
  \mathcal{D} \longrightarrow \mathcal{D}
$$

equipped with the [[adjunction unit]] [[natural transformation]] (Def. \ref{AdjunctionUnitFromHomIsomorphism})

$$
  X \overset{\eta_X}{\longrightarrow} \bigcirc X
$$

is a [[modal operator]] on $\mathcal{D}$ (Def. \ref{ModalOperator}).


Dually, if

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longleftarrow}}
      {\overset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}}
      {\bot}
  \mathcal{D}
$$

is a [[coreflective subcategory]]-inclusion (Def. \ref{ReflectiveSubcategory}). Then the [[composition|composite]]  

$$
  \Box
  \;\coloneqq\;
  \iota \circ R
  \;\colon\;
  \mathcal{D} \longrightarrow \mathcal{D}
$$

equipped with the [[adjunction counit]] [[natural transformation]] (Def. \ref{AdjunctionUnitFromHomIsomorphism})

$$
  \Box X \overset{ \epsilon_X }{\longrightarrow} X
$$

is a [[comodal operator]] on $\mathcal{D}$ (Def. \ref{ModalOperator}).

Conversely:

If an [[endofunctor]] $\bigcirc \;\colon\; \mathcal{D} \to \mathcal{D}$ with [[natural transformation]] $X \overset{\eta_X}{\to} \bigcirc X$ is a [[modal operator]] on a [[category]] $\mathcal{D}$ (Def. \ref{ModalOperator}), then the inclusion of its [[full subcategory|full]] [[essential image]] is a [[reflective subcategory]] inclusion (Def. \ref{ReflectiveSubcategory}) with [[reflector]] given by the [[corestriction]] of $\bigcirc$ to its image:

$$
  Im( \bigcirc )
    \underoverset
      {\underset{ \phantom{AA} \iota \phantom{AA} }{\hookrightarrow}}
      {\overset{ \bigcirc }{\longleftarrow}}
      {}
  \mathcal{D}
  \,.
$$

Dually, if an [[endofunctor]] $\Box \;\colon\; \mathcal{D} \to \mathcal{D}$ with [[natural transformation]] $\Box X \overset{\epsilon_X}{\longrightarrow} X$ is a [[comodal operator]] (Def. \ref{ModalOperator}), then the inclusion of its [[full subcategory|full]] [[essential image]] is a [[coreflective subcategory]] inclusion (Def. \ref{ReflectiveSubcategory}) with [[coreflector]] given by the [[corestriction]] of $\Box$ to its image

$$
  Im( \Box )
    \underoverset
      {\underset{ \Box }{\longleftarrow}}
      {\overset{ \phantom{AA} \iota \phantom{AA} }{\hookrightarrow}}
      {}
  \mathcal{D}
  \,.
$$


=--

+-- {: .proof}
###### Proof

The first two statements are immedialy a special case of the characterization of [[adjunctions]] via [[universal morphisms]] in Prop. \ref{CollectionOfUniversalArrowsEquivalentToAdjointFunctor}: Using that $R = \iota$ is here assumed to be [[fully faithful functor|fully faithful]], the uniqueness of $\tilde f$ in the [[universal morphism]]-factorization condition (eq:UniversalArrowFactorization)

$$
  \array{
    && c 
    \\
    & {}^{\mathllap{\eta_c}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    R(L(c)) &&\underset{R (\widetilde f)}{\longrightarrow}&& R(d)
    \\
    \\
    L(c) &&\underset{ \exists ! \, \widetilde f}{\longrightarrow}&& d
  }
$$

implies that also $R(\widetilde f) = \iota(\widetilde f)$ is the unique morphism making that triangle commute. 

Similarly for the converse: The assumption on a [[modal operator]] $\bigcirc$ is just so as to make its unit $\eta$ be a [[universal morphism]] (Def. \ref{UniversalArrow}) into the inclusion functor $\iota$ of its [[essential image]].

=--

+-- {: .num_prop #ModalOpIdempotent}
###### Proposition
**([[modal operator]] is [[idempotent]])**

Let $\mathcal{D}$ be a [[category]] (Def. \ref{Categories}). 

For $\bigcirc$ a [[modal operator]] on $\mathcal{D}$, with unit $\eta$ (Def. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}), it is _[[idempotent monad|idempotent]]_, in that it is [[natural isomorphism|naturally isomorphic]] (Def. \ref{NaturalTransformations}) to the [[composition]] with itself:

$$
  \bigcirc \;\simeq\; \bigcirc \bigcirc
  \,.
$$

In fact, the image under $\bigcirc$ of its unit is such an isomorphism

$$
  \bigcirc\left( X \overset{\eta_X}{\to} \bigcirc X \right)
  \;\;\colon\;\;
  \bigcirc X 
    \overset{\simeq}{\longrightarrow}
  \bigcirc ( \bigcirc X )
$$

as is its unit on its image

$$
  \eta_{\bigcirc X}
  \;\;\colon\;\;
  \bigcirc X 
    \overset{\simeq}{\longrightarrow}
  \bigcirc ( \bigcirc X )
  \,.
$$


[[formal dual|Dually]], for $\Box$ a [[comodal operator]] on $\mathcal{D}$, with counit $\epsilon$ (Def. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}), it is _[[idempotent monad|idempotent]]_, in that it is [[natural isomorphism|naturally isomorphic]] (Def. \ref{NaturalTransformations}) to the [[composition]] with itsef:

$$
  \Box \circ \Box
  \;\simeq\;
  \Box
  \,.
$$

In fact, the image under $\Box$ of its counit is such an isomorphism

$$
  \Box\left(  \Box X \overset{\epsilon_X}{\to} X \right)
  \;\;\colon\;\;
  \Box (\Box X)
    \overset{\simeq}{\longrightarrow}
  \Box X
$$

as is its counit on its image

$$
  \epsilon_{\Box X}
  \;\;\colon\;\;
  \Box ( \Box X )
    \overset{\simeq}{\longrightarrow}
  \Box X
  \,.
$$

=--

+-- {: .proof}
###### Proof

We discuss the first case. The second is [[formal dual|formally dual]].

By Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}, the modal operator is equivalent to the composite $\iota \circ L$ obtained from the [[reflective subcategory]]-inclusion (Def. \ref{ReflectiveSubcategory}) of its [[essential image]] of [[modal objects]]:

$$
  Im(\bigcirc)
    \underoverset
      {\underset{\phantom{AA}\iota \phantom{AA}}{\hookrightarrow}}
      {\overset{\phantom{AA}L \phantom{AA} }{\longleftarrow}}
      {\bot}
  \mathcal{D}
  \,.
$$

and its unit is the corresponding [[adjunction unit]] (Def. \ref{AdjunctionUnitFromHomIsomorphism})

$$
  X \overset{\eta_X}{\longrightarrow} \iota \circ L
  \,.
$$

Hence it is sufficient to show that the morphisms and $L( \eta_X )$ and $\eta_{\iota Y}$ are isomorphisms.

Now, the [[triangle identities]] (eq:TriangleIdentities) for the [[adjunction]] $L \dashv \iota$, which hold by Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}, say that their [[composition]] with the [[adjunction counit]] is the [[identity morphism]]

$$
  \epsilon_{L(\eta_X)} \circ L(\eta_X)
  \;=\;
  id_{L(X)}
  \phantom{AA} \text{and} \phantom{AA}
  \iota( \epsilon_Y )\circ \eta_{\iota(Y)}
  \;=\;
  id_{\iota(Y)}
  \,.
$$

But by Prop. \ref{FullyFaithfulAndInvertibleAdjoints}, the counit $\epsilon$ is a [[natural isomorphism]], since $\iota$ is [[fully faithful functor|fully faithful]]. Hence we may cancel it on both sides of the [[triangle identities]] and find that $L(\eta_X)$ and $\eta_{\iota(Y)}$ are indeed isomorphisms.



=--

+-- {: .num_defn #ModalObjects}
###### Definition
**([[modal objects]])**

Let $\mathcal{D}$ be a [[category]] (Def. \ref{Categories}).

For $\bigcirc$ a [[modal operator]] on $\mathcal{D}$ (Def. \ref{ModalOperator}), we say:

1. a _$\bigcirc$-[[modal object]]_ is an [[object]] $X \in \mathcal{D}$ such that the following conditions hold (which are all equivalent, by Prop. \ref{ModalOpIdempotent}):

   * it is in the $\bigcirc$-[[essential image]]: $X \in Im( \bigcirc ) \hookrightarrow \mathcal{D}$, 

   * it is isomorphic to its own $\bigcirc$-[[image]]: $X \simeq \bigcirc X$,

   * specifically its $\bigcirc$-unit is an [[isomorphism]] $\eta_X \;\colon\; X \overset{\simeq}{\to} \bigcirc X$.

1. a _$\bigcirc$-[[modal object|submodal object]]_ is an [[object]] $X \in \mathcal{D}$, such that 

   * its $\bigcirc$-unit is a [[monomorphism]] (Def. \ref{Monomorphism}): $\eta_X \;\colon\; X \hookrightarrow \bigcirc X$.

[[formal duality|Dually]]:

For $\Box$ a [[comodal operator]] on $\mathcal{D}$ (Def. \ref{ModalOperator}), we say:

1. a _$\Box$-[[comodal object]]_ is an [[object]] $X \in \mathcal{D}$ such that the following conditions hold (which are all equivalent, by Prop. \ref{ModalOpIdempotent}):

   * it is in the $\Box$-[[essential image]]: $X \in Im( \Box ) \hookrightarrow \mathcal{D}$, 

   * it is isomorphic to its own $\Box$-[[image]]: $\Box X \simeq X$,

   * specifically its $\Box$-counit is an [[isomorphism]] $\epsilon_X \;\colon\; \Box X \overset{\simeq}{\longrightarrow} X$

1. a _$\Box$-[[comodal object|supcomodal object]]_ is an [[object]] $X \in \mathcal{D}$, such that 

   * its $\Box$-counit is an [[epimorphism]] (Def. \ref{Monomorphism}): $\epsilon_X \;\colon\; \Box X \overset{epi}{\longrightarrow} X$.


=--

(...)

$\,$

## Basic notions of Categorical algebra

We have seen that the existence of [[Cartesian products]] in a [[category]] $\mathcal{C}$ equips is with a [[functor]] of the form

$$
  \mathcal{C} \times \mathcal{C}
    \overset{ (-) \times (-) }{\longrightarrow}
  \mathcal{C}
$$

which is directly analogous to the operation of [[multiplication]] in an [[associative algebra]] or even just in a [[semigroup]] (or [[monoid]]), just "[[categorification|categorified]]" (Example \ref{CartesianMonoidalCategory} below). This is made precise by the concept of a _[[monoidal category]]_ (Def. \ref{MonoidalCategory} below).

This relation between [[category theory]] and [[algebra]] leads to the fields of _[[categorical algebra]]_ and of _[[universal algebra]]_. 

Here we are mainly interested in [[monoidal categories]] as a foundations for [[enriched category theory]], to which we turn [below](#EnrichedCategories).

$\,$

### Monoidal categories

+-- {: .num_defn #MonoidalCategory}
###### Definition
**([[monoidal category]])**

An_[[monoidal category]]_ is a [[category]] $\mathcal{C}$ (Def. \ref{Categories}) equipped with

1. a [[functor]] (Def. \ref{Functors})

   $$
      \otimes
        \;\colon\;
      \mathcal{C} \times \mathcal{C}
       \longrightarrow
      \mathcal{C}
   $$

   out of the [[product category]] of $\mathcal{C}$ with itself (Example \ref{ProductCategory}), called the **[[tensor product]]**,

1. an [[object]]

   $$
     1 \in Obj_{\mathcal{C}}
   $$

   called the **[[unit object]]** or **[[tensor unit]]**,

1. a [[natural isomorphism]] (Def. \ref{NaturalTransformations})

   $$
     a
       \;\colon\;
     ((-)\otimes (-)) \otimes (-)
       \overset{\simeq}{\longrightarrow}
     (-) \otimes ((-)\otimes(-))
   $$

   called the **[[associator]]**,

1. {#MonoidalCategoryUnitors} a [[natural isomorphism]]

   $$
     \ell
       \;\colon\;
     (1 \otimes (-))
       \overset{\simeq}{\longrightarrow}
     (-)
   $$

   called the **[[left unitor]]**, and a natural isomorphism

   $$
     r \;\colon\; (-) \otimes 1 \overset{\simeq}{\longrightarrow} (-)
   $$

   called the **[[right unitor]]**,

such that the following two kinds of [[commuting diagram|diagrams commute]], for all objects involved:

1. **triangle identity**:

   $$
     \array{
        & (x \otimes 1) \otimes y &\stackrel{a_{x,1,y}}{\longrightarrow} & x \otimes (1 \otimes y)
         \\
         & {}_{\rho_x \otimes 1_y}\searrow
         && \swarrow_{1_x \otimes \lambda_y}
         &
        \\
        &&
        x \otimes y
        &&
     }
   $$


1. the **[[pentagon identity]]**:

   $$
     \array{
       && (w \otimes x) \otimes (y \otimes z)
       \\
       & {}^{\mathllap{\alpha_{w \otimes x, y, z}}}\nearrow
        &&
       \searrow^{\mathrlap{\alpha_{w,x,y \otimes z}}}
       \\
       ((w \otimes x ) \otimes y) \otimes z
        && &&
       (w \otimes (x \otimes (y \otimes z)))
       \\
       {}^{\mathllap{\alpha_{w,x,y}} \otimes id_z }\downarrow
        && &&
       \uparrow^{\mathrlap{ id_w \otimes \alpha_{x,y,z} }}
       \\
       (w \otimes (x \otimes y)) \otimes z
         && \underset{\alpha_{w,x \otimes y, z}}{\longrightarrow} &&
       w \otimes ( (x \otimes y) \otimes z )
     }
   $$


=--


+-- {: .num_example #CartesianMonoidalCategory}
###### Example
**([[cartesian monoidal category]])**

Let $\mathcal{C}$ be a [[category]] in which all [[finite products]] exist.
Then $\mathcal{C}$ becomes a [[monoidal category]] (Def. \ref{MonoidalCategory}) by

1. taking the [[tensor product]] to be the [[Cartesian product]]

   $$
     X \otimes Y \;\coloneqq\; X \times Y
   $$

1. taking the [[unit object]] to be the [[terminal object]]

   $$
     I \;\coloneqq\; \ast
   $$

Monoidal categories of this form are called _[[cartesian monoidal categories]]_.

=--


+-- {: .num_lemma #kel1}
###### Lemma
**([Kelly 64](monoidal+category#Kelly))**

Let $(\mathcal{C}, \otimes, 1)$ be a [[monoidal category]], def. \ref{MonoidalCategory}. Then the left and right [[unitors]] $\ell$ and $r$ satisfy the following conditions:

1. $\ell_1 = r_1 \;\colon\; 1 \otimes 1 \overset{\simeq}{\longrightarrow} 1$;

1. for all objects $x,y \in \mathcal{C}$ the following [[commuting diagram|diagrams commutes]]:

   $$
     \array{
       (1 \otimes x) \otimes y  & &
       \\
       {}^\mathllap{\alpha_{1, x, y}} \downarrow
       & \searrow^\mathrlap{\ell_x \otimes id_y} &
       \\
       1 \otimes (x \otimes y)
       & \underset{\ell_{x \otimes y}}{\longrightarrow} & x \otimes y
     }
     \,;
   $$

   and

   $$
     \array{
       x \otimes (y \otimes 1) & &
       \\
       {}^\mathllap{\alpha^{-1}_{1, x, y}} \downarrow
       & \searrow^\mathrlap{id_x \otimes r_y} &
       \\
       (x \otimes y) \otimes 1
         &
           \underset{r_{x \otimes y}}{\longrightarrow}
         &
       x \otimes y
     }
     \,;
   $$

=--

For **proof** see at _[[monoidal category]]_ [this lemma](monoidal+category#kel1) and [this lemma](monoidal+category#kel2).

+-- {: .num_remark #CoherenceForMonoidalCategories}
###### Remark

Just as for an [[associative algebra]] it is sufficient to demand $1 a = a$ and $a 1 = a$ and $(a b) c = a (b c)$ in order to have that expressions of arbitrary length may be re-bracketed at will, so there is a _[[coherence theorem for monoidal categories]]_ which states that all ways of freely composing the [[unitors]] and [[associators]] in a [[monoidal category]] (def. \ref{MonoidalCategory}) to go from one expression to another will coincide. Accordingly, much as one may drop the notation for the bracketing in an [[associative algebra]] altogether, so one may, with due care, reason about monoidal categories without always making all unitors and associators explicit.

(Here the qualifier "freely" means informally that we must not use any non-formal identification between objects, and formally it means that the diagram in question must be in the image of a [[strong monoidal functor]] from a _free_ monoidal category. For example if in a particular monoidal category it so happens that the object $X \otimes (Y \otimes Z)$ is actually _equal_ to $(X \otimes Y)\otimes Z$, then the various ways of going from one expression to another using only associators _and_ this equality no longer need to coincide.)

=--

+-- {: .num_defn #BraidedMonoidalCategory}
###### Definition
**([[braided monoidal category]])**

A **[[braided monoidal category]]**, is a [[monoidal category]] $\mathcal{C}$ (def. \ref{MonoidalCategory}) equipped with a [[natural isomorphism]] (Def. \ref{NaturalTransformations})

\[
  \label{BraidingIsomorphism}
  \tau_{x,y} \colon x \otimes y \to y \otimes x
\]

called the **[[braiding]]**, such that the following two kinds of [[commuting diagram|diagrams commute]] for all [[objects]] involved ("hexagon identities"):

$$
  \array{
   (x \otimes y) \otimes z
   &\stackrel{a_{x,y,z}}{\to}&
   x \otimes (y \otimes z)
   &\stackrel{\tau_{x,y \otimes z}}{\to}&
   (y \otimes z) \otimes x
   \\
   \downarrow^{\tau_{x,y}\otimes Id}
   &&&&
   \downarrow^{a_{y,z,x}}
   \\
   (y \otimes x) \otimes z
   &\stackrel{a_{y,x,z}}{\to}&
   y \otimes (x \otimes z)
   &\stackrel{Id \otimes \tau_{x,z}}{\to}&
   y \otimes (z \otimes x)
  }
$$

and

$$
  \array{
   x \otimes (y \otimes z)
   &\stackrel{a^{-1}_{x,y,z}}{\to}&
   (x \otimes y) \otimes z
   &\stackrel{\tau_{x \otimes y, z}}{\to}&
   z \otimes (x \otimes y)
   \\
   \downarrow^{Id \otimes \tau_{y,z}}
   &&&&
   \downarrow^{a^{-1}_{z,x,y}}
   \\
   x \otimes (z \otimes y)
   &\stackrel{a^{-1}_{x,z,y}}{\to}&
   (x \otimes z) \otimes y
   &\stackrel{\tau_{x,z} \otimes Id}{\to}&
   (z \otimes x) \otimes y
  }
  \,,
$$

where $a_{x,y,z} \colon (x \otimes y) \otimes z \to x \otimes (y \otimes z)$ denotes the components of the [[associator]] of $\mathcal{C}^\otimes$.

=--

+-- {: .num_defn #SymmetricMonoidalCategory}
###### Definition

A **[[symmetric monoidal category]]** is a [[braided monoidal category]] (def. \ref{BraidedMonoidalCategory}) for which the [[braiding]]

$$
   \tau_{x,y} \colon x \otimes y \to y \otimes x
$$

satisfies the condition:

$$
  \tau_{y,x} \circ \tau_{x,y} = 1_{x \otimes y}
$$

for all objects $x, y$

=--

+-- {: .num_remark #SymmetricMonoidalCategoriesCoherenceTheorem}
###### Remark

In analogy to the [[coherence theorem for monoidal categories]] (remark \ref{CoherenceForMonoidalCategories}) there is a [[coherence theorem for symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}), saying that every diagram built freely (see remark \ref{SymmetricMonoidalCategoriesCoherenceTheorem}) from [[associators]], [[unitors]] and [[braidings]] such that both sides of the diagram correspond to the same [[permutation]] of objects, coincide.

=--



+-- {: .num_defn #ClosedMonoidalCategory}
###### Definition
**([[symmetric monoidal category|symmetric]] [[closed monoidal category]])**

Given a [[symmetric monoidal category]] $\mathcal{C}$ with [[tensor product]] $\otimes$ (def. \ref{SymmetricMonoidalCategory}) it is called a _[[closed monoidal category]]_ if for each $Y \in \mathcal{C}$ the [[functor]] $Y \otimes(-)\simeq (-)\otimes Y$ has a [[right adjoint]], denoted $hom(Y,-)$

\[
  \label{InternalHomAdjunction}
  \mathcal{C}
    \underoverset
      {\underset{ [Y,-]}{\longrightarrow}}
      {\overset{(-) \otimes Y}{\longleftarrow}}
      {\bot}
  \mathcal{C}
  \,,
\]

hence if there are [[natural bijections]]

$$
  Hom_{\mathcal{C}}(X \otimes Y, Z)
   \;\simeq\;
  Hom_{\mathcal{C}}{C}(X, [Y,Z])
$$

for all objects $X,Z \in \mathcal{C}$.

Since for the case that $X = 1$ is the [[tensor unit]] of $\mathcal{C}$ this means that

$$
  Hom_{\mathcal{C}}(1, [Y,Z]) \simeq Hom_{\mathcal{C}}(Y,Z)
  \,,
$$

the object $[Y,Z] \in \mathcal{C}$ is an enhancement of the ordinary [[hom-set]] $Hom_{\mathcal{C}}(Y,Z)$ to an object in $\mathcal{C}$.
Accordingly, it is also called the **[[internal hom]]** between $Y$ and $Z$.

=--


+-- {: .num_example #SetIsCartesianClosed}
###### Example
**([[Set]] is a [[cartesian closed category]])**

The [[category]] [[Set]] of all [[sets]] (Example \ref{CategoryOfSets}) equipped with its [[cartesian monoidal category]]-structure (Example \ref{CartesianMonoidalCategory}) is a [[closed monoidal category]] (Def. \ref{ClosedMonoidalCategory}), hence a _[[cartesian closed category]_. The [[Cartesian product]] is the original [[Cartesian product]] of sets, and the [[internal hom]] is the [[function set]] $[X,Y]$ of functions from $X$ to $Y$

=--

+-- {: .num_example #GrpdIsACartesianClosedCategory}
###### Example
**([[Cat]] and [[Grpd]] are [[cartesian closed category]])**

The [[category]] [[Cat]] (Example \ref{CategoriesOfSmallCategories}) of all [[small categories]] (Example \ref{SmallCategory}) is a 
[[cartesian monoidal category]]-structure (Example \ref{CartesianMonoidalCategory}) with [[Cartesian product]] given by forming [[product categories]] (Example \ref{ProductCategory}).


Inside this, the [[full subcategory]] [[Grpd]] (Example \ref{CategoriesOfSmallCategories}) of all [[small groupoid|small]] [[groupoids]] (Example \ref{Groupoid}) is itself a 
[[cartesian monoidal category]]-structure (Example \ref{CartesianMonoidalCategory}) with [[Cartesian product]] given by forming [[product categories]] (Example \ref{ProductCategory}).

In both cases this yields a [[closed monoidal category]] (Def. \ref{ClosedMonoidalCategory}), hence a [[cartesian closed category]]: the [[internal hom]] is given by the [[functor category]] construction (Example \ref{FunctorCategory}).


=--

+-- {: .num_example #ExampleAbelianGroupsOfMonoidalCategory}
###### Example
**([[tensor product]] of [[abelian groups]] is [[closed monoidal category]] [[symmetric monoidal category|symmetric]] [[monoidal category]]-[[structure]])**

The category [[Ab]] of [[abelian groups]] (as in Example \ref{ExamplesOfConcreteCategories}) becomes a [[symmetric monoidal category]] (Def. \ref{SymmetricMonoidalCategory}) with [[tensor product]] the actual [[tensor product of abelian groups]] $\otimes_{\mathbb{Z}}$ and with [[tensor unit]] the additive group $\mathbb{Z}$ of [[integers]]. Again the [[associator]], [[unitor]] and [[braiding]] isomorphism are the evident ones coming from the underlying sets, as in example \ref{TopAsASymmetricMonoidalCategory}.

This is a [[closed monoidal category]] with [[internal hom]] $hom(A,B)$ being the set of [[homomorphisms]] $Hom_{Ab}(A,B)$ equipped with the pointwise group structure for $\phi_1, \phi_2 \in Hom_{Ab}(A,B)$ then $(\phi_1 + \phi_2)(a) \coloneqq \phi_1(a) + \phi_2(b) \; \in B$.

This is the archetypical case that motivates the notation "$\otimes$" for the pairing operation in a [[monoidal category]].

=--


The [[internal hom]] (Def. \ref{ClosedMonoidalCategory}) turns out to share all the abstract properties of the ordinary (external) [[hom-functor]] (Def. \ref{HomFunctor}), even though this is not completely manifest from its definition. We make this explicit by the following three propositions.

+-- {: .num_prop #InternalHomBifunctor}
###### Proposition
**([[internal hom]] [[bifunctor]])**

For $\mathcal{C}$ a [[closed monoidal category]] (Def. \ref{ClosedMonoidalCategory}), there is a unique [[functor]] (Def. \ref{Functors}) out of the [[product category]] (Def. \ref{ProductCategory}) of $\mathcal{C}$ with its [[opposite category]] (Def. \ref{OppositeCategory})

$$
  [-,-]
  \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  \mathcal{C}
$$

such that for each $X \in \mathcal{C}$ it coincides with the [[internal hom]] $[X,-]$ (eq:InternalHomAdjunction) as a functor in the second variable, and such that there is a [[natural isomorphism]]

$$
  Hom(X, [Y,Z])
  \;\simeq\;
  Hom(X \otimes Y, Z)
$$

which is natural not only in $X$ and $Z$, but also in $Y$.

=--

+-- {: .proof}
###### Proof

We have a natural isomorphism for each fixed $Y$, and hence in particular for fixed $Y$ and fixed $Z$ by (eq:InternalHomAdjunction). With this the statement follows by Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject}.

=--


In fact the 3-variable adjunction from Prop. \ref{InternalHomBifunctor} even holds internally:


+-- {: .num_prop #TensorHomAdjunctionIsoInternally}
###### Proposition
**(internal tensor/hom-adjunction)**

In a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] (def. \ref{ClosedMonoidalCategory}) there are [[natural isomorphisms]]

$$
  [X \otimes Y, Z]
   \;\simeq\;
  [X, [Y,Z]]
$$

whose image under $Hom_{\mathcal{C}}(1,-)$ (see also Example \ref{ChangeOfCosmosFromVToSet} below) are the defining [[natural bijections]] of Prop. \ref{InternalHomBifunctor}.

=--

+-- {: .proof}
###### Proof

Let $A \in \mathcal{C}$ be any object. By applying the natural bijections from Prop. \ref{InternalHomBifunctor}, there are composite [[natural bijections]]

$$
  \begin{aligned}
    Hom_{\mathcal{C}}(A , [X \otimes Y, Z])
    & \simeq
    Hom_{\mathcal{C}}(A \otimes (X \otimes Y), Z)
    \\
    & \simeq
    Hom_{\mathcal{C}}((A \otimes X)\otimes Y, Z)
    \\
    & \simeq
    Hom_{\mathcal{C}}(A \otimes X, [Y,Z])
    \\
    & \simeq
    Hom_{\mathcal{C}}(A, [X, [Y,Z]])
  \end{aligned}
$$

Since this holds for all $A$, the [[fully faithful functor|fully faithfulness]] of the [[Yoneda embedding]] (Prop. \ref{YonedaEmbedding}) says that there is an isomorphism $[ X\otimes Y, Z ] \simeq [X, [Y,Z]]$. Moreover, by taking $A = 1$ in the above and using the left [[unitor]] isomorphisms $A \otimes (X \otimes Y) \simeq X \otimes Y$ and $A\otimes X \simeq X$  we get a [[commuting diagram]]

$$
  \array{
    Hom_{\mathcal{C}}(1, [X\otimes Y, Z ))
      &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(1, [X, [Y,Z]])
    \\
    {}^{\mathllap{\simeq}}\downarrow
      &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    Hom_{\mathcal{C}}(X \otimes Y, Z)
     &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(X, [Y,Z])
  }
  \,.
$$

=--

Also the key respect of [[hom-functors]] for [[limits]] is inherited by [[internal hom]]-functors

+-- {: .num_prop #InternalHomPreservesLimits}
###### Proposition
**([[internal hom]] preserves [[limits]])**

Let $\mathcal{C}$ be a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] with [[internal hom]]-[[bifunctor]] $[-,-]$ (Prop. \ref{InternalHomBifunctor}). Then this bifunctor preserves [[limits]] in the second variable, and sends [[colimits]] in the first variable to limits:

$$
  [X, \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} Y(j)]
  \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [X, Y(j)]
$$

and

$$
  [\underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j),X]
  \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j),X]  
$$



=--


+-- {: .proof}
###### Proof

For $X \in \mathcal{X}$ any object, $[X,-]$ is a [[right adjoint]] by definition, and hence preserves limits by Prop. \ref{AdjointsPreserveCoLimits}.

For the other case, let $Y \;\colon\; \mathcal{L} \to \mathcal{C}$ be a [[diagram]] in $\mathcal{C}$, and let $C \in \mathcal{C}$ be any object. Then there are isomorphisms

$$
  \begin{aligned}
    Hom_{\mathcal{C}}(C, \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X )
    & \simeq
    Hom_{\mathcal{C}}( C \otimes \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X )
    \\
    & \simeq
    Hom_{\mathcal{C}}( \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} (C \otimes Y(j)), X )   
    \\
    & \simeq
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim}
    Hom_{\mathcal{C}}( (C \otimes Y(j)), X )    
    \\
    & \simeq
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim}
    Hom_{\mathcal{C}}( C, [Y(j), X] )    
    \\
    & \simeq
    Hom_{\mathcal{C}}( C, \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j), X] )    
  \end{aligned}
$$

which are [[natural isomorphism|natural]] in $C \in \mathcal{C}$, where we used that the ordinary [[hom-functor]] respects (co)limits as shown, and that the left adjoint $C \otimes (-)$ preserves colimits.

Hence by the [[fully faithful functor|fully faithfulness]] of the [[Yoneda embedding]], there is an isomorphism

$$
  \left[ \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X \right]  
  \overset{\simeq}{\longrightarrow}
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j), X] 
  \,.
$$


=--

$\,$

Now that we have seen [[monoidal categories]] with various extra [[properties]], we next look at [[functors]] which preserve these:

+-- {: .num_defn #LaxMonoidalFunctor}
###### Definition
**([[monoidal functors]])**

Let $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ be two [[monoidal categories]] (def. \ref{MonoidalCategory}). A _[[lax monoidal functor]]_ between them is

1. a [[functor]] (Def. \ref{Functors})

   $$
     F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
     \,,
   $$

1. a [[morphism]]

   \[
     \label{UnitComponentOfMonoidalFunctor}
     \epsilon \;\colon\; 1_{\mathcal{D}} \longrightarrow F(1_{\mathcal{C}})
   \]

1. a [[natural transformation]] (Def. \ref{NaturalTransformations})

   \[
     \label{MonoidalComponentsOfMonoidalFunctor}
     \mu_{x,y}
       \;\colon\;
     F(x) \otimes_{\mathcal{D}} F(y)
       \longrightarrow
     F(x \otimes_{\mathcal{C}} y)
   \]

   for all $x,y \in \mathcal{C}$

satisfying the following conditions:

1. **([[associativity]])** For all objects $x,y,z \in \mathcal{C}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (F(x) \otimes_{\mathcal{D}} F(y)) \otimes_{\mathcal{D}} F(z)
         &\underoverset{\simeq}{a^{\mathcal{D}}_{F(x),F(y),F(z)}}{\longrightarrow}&
       F(x) \otimes_{\mathcal{D}}( F(y)\otimes_{\mathcal{D}} F(z) )
       \\
       {}^{\mathllap{\mu_{x,y} \otimes id}}\downarrow
         &&
       \downarrow^{\mathrlap{id\otimes \mu_{y,z}}}
       \\
       F(x \otimes_{\mathcal{C}} y) \otimes_{\mathcal{D}} F(z)
        &&
       F(x) \otimes_{\mathcal{D}} ( F(x \otimes_{\mathcal{C}} y) )
       \\
       {}^{\mathllap{\mu_{x \otimes_{\mathcal{C}} y , z} } }\downarrow
         &&
       \downarrow^{\mathrlap{\mu_{ x, y \otimes_{\mathcal{C}} z  }}}
       \\
       F( ( x \otimes_{\mathcal{C}} y ) \otimes_{\mathcal{C}} z  )
         &\underset{F(a^{\mathcal{C}}_{x,y,z})}{\longrightarrow}&
       F( x \otimes_{\mathcal{C}} ( y \otimes_{\mathcal{C}} z ) )
     }
     \,,
   $$

   where $a^{\mathcal{C}}$ and $a^{\mathcal{D}}$ denote the [[associators]] of the monoidal categories;


1. **([[unitality]])** For all $x \in \mathcal{C}$ the following [[commuting diagram|diagrams commutes]]

   $$
     \array{
       1_{\mathcal{D}} \otimes_{\mathcal{D}} F(x)
         &\overset{\epsilon \otimes id}{\longrightarrow}&
       F(1_{\mathcal{C}}) \otimes_{\mathcal{D}} F(x)
       \\
       {}^{\mathllap{\ell^{\mathcal{D}}_{F(x)}}}\downarrow
         &&
       \downarrow^{\mathrlap{\mu_{1_{\mathcal{C}}, x }}}
       \\
       F(x)
         &\overset{F(\ell^{\mathcal{C}}_x )}{\longleftarrow}&
       F(1 \otimes_{\mathcal{C}} x  )
     }
   $$

   and

   $$
     \array{
       F(x) \otimes_{\mathcal{D}}  1_{\mathcal{D}}
         &\overset{id \otimes \epsilon }{\longrightarrow}&
       F(x) \otimes_{\mathcal{D}}  F(1_{\mathcal{C}})
       \\
       {}^{\mathllap{r^{\mathcal{D}}_{F(x)}}}\downarrow
         &&
       \downarrow^{\mathrlap{\mu_{x, 1_{\mathcal{C}} }}}
       \\
       F(x)
         &\overset{F(r^{\mathcal{C}}_x )}{\longleftarrow}&
       F(x \otimes_{\mathcal{C}} 1  )
     }
     \,,
   $$

   where $\ell^{\mathcal{C}}$, $\ell^{\mathcal{D}}$, $r^{\mathcal{C}}$, $r^{\mathcal{D}}$ denote the left and right [[unitors]] of the two monoidal categories, respectively.

If $\epsilon$ and alll $\mu_{x,y}$ are [[isomorphisms]], then $F$ is called a **[[strong monoidal functor]]**.

If moreover $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ are equipped with the structure of [[braided monoidal categories]] (def. \ref{BraidedMonoidalCategory}) with [[braidings]] $\tau^{\mathcal{C}}$ and $\tau^{\mathcal{D}}$, respectively, then the lax monoidal functor $F$ is called a **[[braided monoidal functor]]** if in addition the following [[commuting diagram|diagram commutes]] for all objects $x,y \in \mathcal{C}$

$$
  \array{
    F(x) \otimes_{\mathcal{C}} F(y)
      &\overset{\tau^{\mathcal{D}}_{F(x), F(y)}}{\longrightarrow}&
    F(y) \otimes_{\mathcal{D}} F(x)
    \\
    {}^{\mathllap{\mu_{x,y}}}\downarrow
      &&
    \downarrow^{\mathrlap{\mu_{y,x}}}
    \\
    F(x \otimes_{\mathcal{C}} y )
      &\underset{F(\tau^{\mathcal{C}}_{x,y}  )}{\longrightarrow}&
    F( y \otimes_{\mathcal{C}} x )
  }
  \,.
$$

A [[homomorphism]] $f\;\colon\; (F_1,\mu_1, \epsilon_1) \longrightarrow (F_2, \mu_2, \epsilon_2)$ between two (braided) lax monoidal functors is a **[[monoidal natural transformation]]**, in that it is a [[natural transformation]] $f_x \;\colon\; F_1(x) \longrightarrow F_2(x)$ of the underlying functors

compatible with the product and the unit in that the following [[commuting diagram|diagrams commute]] for all objects $x,y \in \mathcal{C}$:

$$
  \array{
    F_1(x) \otimes_{\mathcal{D}} F_1(y)
      &\overset{f(x)\otimes_{\mathcal{D}} f(y)}{\longrightarrow}&
    F_2(x) \otimes_{\mathcal{D}} F_2(y)
    \\
    {}^{\mathllap{(\mu_1)_{x,y}}}\downarrow
     &&
    \downarrow^{\mathrlap{(\mu_2)_{x,y}}}
    \\
    F_1(x\otimes_{\mathcal{C}} y)
     &\underset{f(x \otimes_{\mathcal{C}} y ) }{\longrightarrow}&
    F_2(x \otimes_{\mathcal{C}} y)
  }
$$

and

$$
  \array{
    && 1_{\mathcal{D}}
    \\
    & {}^{\mathllap{\epsilon_1}}\swarrow && \searrow^{\mathrlap{\epsilon_2}}
    \\
    F_1(1_{\mathcal{C}})
     &&\underset{f(1_{\mathcal{C}})}{\longrightarrow}&&
    F_2(1_{\mathcal{C}})
  }
  \,.
$$

We write $MonFun(\mathcal{C},\mathcal{D})$ for the resulting [[category]] of lax monoidal functors between monoidal categories $\mathcal{C}$ and $\mathcal{D}$, similarly $BraidMonFun(\mathcal{C},\mathcal{D})$ for the category of braided monoidal functors between [[braided monoidal categories]], and $SymMonFun(\mathcal{C},\mathcal{D})$ for the category of braided monoidal functors between [[symmetric monoidal categories]].

=--

+-- {: .num_remark #SymmetricMonoidalFunctor}
###### Remark

In the literature the term "monoidal functor" often refers by default to what in def. \ref{LaxMonoidalFunctor} is called a _strong monoidal functor_.  But for the purpose of the discussion of [[functors with smash product]] [below](#FunctorsWithSmashProduct), it is crucial to admit the generality of lax monoidal functors.

If $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ are [[symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}) then a [[braided monoidal functor]] (def. \ref{LaxMonoidalFunctor}) between them  is often called a **[[symmetric monoidal functor]]**.

=--

+-- {: .num_prop #MonoidalFunctorComp}
###### Proposition

For $\mathcal{C} \overset{F}{\longrightarrow} \mathcal{D} \overset{G}{\longrightarrow} \mathcal{E}$ two composable [[lax monoidal functors]] (def. \ref{LaxMonoidalFunctor}) between [[monoidal categories]], then their composite $F \circ G$ becomes a lax monoidal functor with structure morphisms

$$
  \epsilon^{G\circ F}
    \;\colon\;
  1_{\mathcal{E}}
    \overset{\epsilon^G}{\longrightarrow}
  G(1_{\mathcal{D}})
    \overset{G(\epsilon^F)}{\longrightarrow}
  G(F(1_{\mathcal{C}}))
$$

and

$$
  \mu^{G \circ F}_{c_1,c_2}
  \;\colon\;
  G(F(c_1)) \otimes_{\mathcal{E}} G(F(c_2))
   \overset{\mu^{G}_{F(c_1), F(c_2)}}{\longrightarrow}
  G( F(c_1) \otimes_{\mathcal{D}} F(c_2) )
    \overset{G(\mu^F_{c_1,c_2})}{\longrightarrow}
  G(F( c_1 \otimes_{\mathcal{C}} c_2 ))
  \,.
$$

=--


### Enriched categories
 {#EnrichedCategories}

The plain definition of [[categories]] in Def. \ref{Categories} is phrased in terms of [[sets]]. Via Example \ref{CategoryOfSets} this assigns a special role to the category [[Set]] of all sets, as the "base" on top, or the "[[cosmos]]" inside which [[category theory]] takes place. For instance, the fact that [[hom-sets]] in a plain [[category]] are indeed sets, is what makes the [[hom-functor]] (Example \ref{HomFunctor}) take values in [[Set]], and this, in turn, governs the form of the all-important [[Yoneda lemma]] (Prop. \ref{YonedaLemma}) and [[Yoneda embedding]] (Prop. \ref{YonedaEmbedding}) as statements about [[presheaves]] of sets (Example \ref{CategoryOfPresheaves}).

At the same time, [[category theory]] witnesses the utility of abstracting away from concrete choices to their abstract properties that are actually used in constructions. This makes it natural to ask if one could replace the category [[Set]] by some other category $\mathcal{V}$ which could similarly serve as a "[[cosmos]]" inside which category theory may be developed.

Indeed, such $\mathcal{V}$-[[enriched category theory]] (see Example  \ref{UnderlyingCategoryOfTopEnrichedCategory} below for the terminology) exists, beginning with the concept of $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory} below) and from there directly paralleling, hence generalizing, plain category theory, as long as one assumes the "cosmos" category $\mathcal{V}$ to share a minimum of abstract properties with [[Set]] (Def. \ref{Cosmos} below).

This turns out to be most useful. In fact, the perspective of [[enriched categories]] is helpful already when $\mathcal{V} = $ [[Set]], in which case it reproduces plain category theory (Example \ref{SetEnrichedCategoriesArePlainCategories} below), for instance in that it puts the [[limit|(co)limits]] of the special form of [[end|(co)ends]] (Def. \ref{EndAndCoendInTopcgSmash} below) to the forefront (discussed [below](#TopologicalEndsAndCoends)).

$\,$

+-- {: .num_defn #Cosmos}
###### Definition
**([[cosmos]])**

A _[[Jean Benabou|Bénabou]] [[cosmos]] for [[enriched category theory]]_, or just _[[cosmos]]_, for short, is a [[symmetric monoidal category|symmetric]] (Def. \ref{SymmetricMonoidalCategory}) [[closed monoidal category]] (Def. \ref{ClosedMonoidalCategory}) $\mathcal{V}$  which has all [[limits]] and [[colimits]].

=--

+-- {: .num_example #ExamplesOfCosmoi}
###### Example
**(examples of [[cosmoi]] for [[enriched category theory]])**

The following are examples of [[cosmoi]] (Def. \ref{Cosmos}):

1. [[Set]] (Def. \ref{CategoryOfSets}) equipped with its [[cartesian closed category]]-structure (Example \ref{SetIsCartesianClosed})

1. [[Grpd]] (Def. \ref{CategoriesOfSmallCategories}) equipped with its [[cartesian closed category]]-structure (Example \ref{GrpdIsACartesianClosedCategory}).

=--

+-- {: .num_example #ChangeOfCosmosFromVToSet}
###### Example
**underlying [[set]] of an object in a [[cosmos]]**

Let $\mathcal{V}$ be a [[cosmos]] (Def. \ref{Cosmos}), with $1 \in \mathcal{V}$ its [[tensor unit]] (Def. \ref{MonoidalCategory}). Then the [[hom-functor]] (Def. \ref{HomFunctor}) out of $1$

$$
  Hom_{\mathcal{V}}(1,-)
  \;\colon\;
  \mathcal{V}
    \longrightarrow
  Set
$$

admits the [[structure]] of a [[lax monoidal functor]] (Def. \ref{LaxMonoidalFunctor}) to [[Set]], with the latter regarded with its [[cartesian monoidal category|cartesian monoidal]] [[structure]] from Example \ref{SetIsCartesianClosed}.

Given $V \in \mathcal{V}$, we call

$$
  Hom_{\mathcal{V}}(1,V) \;\in\; Set
$$

also the _underlying_ set of $V$.

=--


+-- {: .proof}
###### Proof

Take the monoidal transformations (eq"MonoidalComponentsOfMonoidalFunctor) to be


$$
  \array{
    Hom_{\mathcal{V}}(1, V_1) 
    \times
    Hom_{\mathcal{V}}(1, V_2) 
    \longrightarrow
    Hom_{\mathcal{V}}(1, V_1 \otimes V_2)
    \\
    \big( 1 \overset{f_1}{\to} V_1\;,\; 1 \overset{f_2}{\to} V_2 \big)
    &\mapsto&
    \big(
      1 \overset{\simeq}{\to} 1 \otimes 1 
        \overset{f_1 \otimes f_2}{\longrightarrow}
      V_1 \otimes V_2
    \big)
  }
$$

and take the unit transformation (eq:UnitComponentOfMonoidalFunctor)

$$
  \array{
    \ast 
      &\longrightarrow& 
    Hom_{\mathcal{V}}(1,1)
  }
$$

to pick $id_1 \in Hom_{\mathcal{V}}(1,1)$.


=--

+-- {: .num_example #UnderlyingSetOfInternalHomIsHomSet}
###### Example
*(underlying set of [[internal hom]] is [[hom-set]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $X,Y \in Obj_{\mathcal{V}}$ be two [[objects]]. Then the underlying set (Def. \ref{ChangeOfCosmosFromVToSet}) of their [[internal hom]] $[X,Y] \in \mathcal{V}$ (Def. \ref{ClosedMonoidalCategory}) is the [[hom-set]] (Def. \ref{Categories}):

$$
  \mathcal{Hom}_{\mathcal{V}}\left( 1, [X,Y]\right)
  \;\simeq\;
  Hom_{\mathcal{V}}(X,Y)
  \,.
$$

This identification is the adjunction isomorphism (eq:HomIsomorphismForAdjointFunctors) for the internal hom adjunction (eq:InternalHomAdjunction) followed composed with a [[unitor]] (Def. \ref{MonoidalCategory}).

=--


+-- {: .num_defn #TopEnrichedCategory}
###### Definition
**([[enriched category]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), a  **$\mathcal{V}$-[[enriched category]]** $\mathcal{C}$ is:

1. a [[class]] $Obj_{\mathcal{C}}$, called the **class of [[objects]]**;

1. for each $a, b\in Obj_{\mathcal{C}}$, an [[object]]

   $$
     \mathcal{C}(a,b)\in \mathcal{V}
     \,,
   $$

   called the **$\mathcal{V}$-[[object of morphisms]]** between $a$ and $b$;

1. for each $a,b,c\in Obj(\mathcal{C})$ a [[morphism]] in $\mathcal{V}$

   $$
     \circ_{a,b,c} 
       \;\colon\; 
      \mathcal{C}(a,b)\times \mathcal{C}(b,c) 
        \longrightarrow 
      \mathcal{C}(a,c)
   $$

   out of the [[tensor product]] of [[hom-objects]], called the _[[composition]]_ operation;

1. for each $a \in Obj(\mathcal{C})$ a morphism  $Id_a \colon \ast \to  \mathcal{C}(a,a)$, called the _[[identity]]_ morphism on $a$

such that the composition is [[associativity|associative]] and [[unitality|unital]].

If the [[class]] $Obj_{\mathcal{C}}$ happens to be a [[set]] (hence a [[small set]] instead of a [[proper class]]) then we say the $\mathcal{V}$-enriched category $\mathcal{C}$ is _[[small category|small]]_, as in Def. \ref{SmallCategory}.

=--

+-- {: .num_example #SetEnrichedCategoriesArePlainCategories}
###### Example
**([[Set]]-[[enriched categories]] are plain [[categories]])**

An [[enriched category]] (Def. \ref{TopEnrichedCategory}) over the [[cosmos]] $\mathcal{V} = $ [[Set]], as in Example \ref{ExamplesOfCosmoi}, is the same as a plain [[category]] (Def. \ref{Categories}).

=--

+-- {: .num_example #UnderlyingCategoryOfTopEnrichedCategory}
###### Example
**(underlying [[category]] of an [[enriched category]])**

Let $\mathcal{C}$ be a $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}). 

Using the [[lax monoidal functor|lax monoidal]] [[structure]] (Def. \ref{LaxMonoidalFunctor}) on the 
[[hom functor]] (Example \ref{ChangeOfCosmosFromVToSet})

$$
  Hom_{\mathcal{V}}(1,-)
  \;\colon\;
  \mathcal{V} \longrightarrow Set
$$

out of the [[tensor unit]] $1 \in \mathcal{C}$ this induces a [[Set]]-[[enriched category]] $\vert \mathcal{C}\vert$ with hence an ordinary [[category]] (Example \ref{SetEnrichedCategoriesArePlainCategories}), with

* $Obj_{\vert \mathcal{C}\vert} \;\coloneqq\; Obj_{\mathcal{C}}$;

* $Hom_{\vert \mathcal{C}\vert}( X, Y ) 
   \;\coloneqq\; 
  Hom_{\mathcal{V}}(1, \mathcal{C}(X,Y))$.

It is in this sense that $\mathcal{C}$ is a plain [[category]] ${\vert \mathcal{C}\vert}$ equipped with [[extra structure]], and hence an "[[enriched category]]".


=---



The archetypical example is $\mathcal{V}$ itself:

+-- {: .num_example #TopkAsATopologicallyEnrichedCategory}
###### Example
**($\mathcal{V}$ as a $\mathcal{V}$-[[enriched category]])**

Evert [[cosmos]] $\mathcal{C}$ (Def. \ref{Cosmos})  canonically obtains the structure of a $\mathcal{V}$-[[enriched category]], def. \ref{TopEnrichedCategory}:

the [[hom-objects]] are the [[internal homs]]

$$
  \mathcal{v}(X,Y)
    \coloneqq
  [X,Y]
$$

and with [[composition]]

$$
  [X,Y] \times [Y,Z]
    \longrightarrow
  [X,Z]
$$

given by the [[adjunct]] under the ([[Cartesian product]]$\dashv$ [[internal hom]])-[[adjunction]] of the [[evaluation morphisms]]

$$
  X \otimes  [XmY] \otimes [Y,Z]
    \overset{(ev, id)}{\longrightarrow}
  Y \otimes [Y,Z]
    \overset{ev}{\longrightarrow}
  Z
  \,.
$$


=--

The usual construction on categories, such as that of [[opposite categories]] (Def. \ref{OppositeCategory}) and [[product categories]] (Def. \ref{ProductCategory}) have evident enriched analogs


+-- {: .num_defn #OppositeAndProductOfPointedTopologicallyEnrichedCategory}
###### Definition
**([[enriched category|enriched]] [[opposite category]] and [[product category]])**

For $\mathcal{V}$ a [[cosmos]], let $\mathcal{C}, \mathcal{D}$ be $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}).

1. The **[[opposite category|opposite]] [[enriched category]]** $\mathcal{C}^{op}$ is the [[enriched category]] with the same [[objects]] as $\mathcal{C}$, with [[hom-objects]]

   $$
     \mathcal{C}^{op}(X,Y)
     \coloneqq
     \mathcal{C}(Y,X)
   $$

   and with [[composition]] given by [[braiding]] (eq:BraidingIsomorphism) followed by the [[composition]] in $\mathcal{C}$:

   $$
     \mathcal{C}^{op}(X,Y)
     \otimes
     \mathcal{C}^{op}(Y,Z)
     =
     \mathcal{C}(Y,X) \otimes \mathcal{C}(Z,Y)
     \underoverset{\simeq}{\tau}{\longrightarrow}
     \mathcal{C}(Z,Y) \otimes \mathcal{C}(Y,X)
       \overset{\circ_{Z,Y,X}}{\longrightarrow}
     \mathcal{C}(Z,X)
     =
     \mathcal{C}^{op}(X,Z)
     \,.
   $$

1. the **[[enriched category|enriched]] [[product category]]** $\mathcal{C} \times \mathcal{D}$ is the [[enriched category]] whose [[objects]] are [[pairs]] of objects $(c,d)$ with $c \in \mathcal{C}$ and $d\in \mathcal{D}$, whose [[hom-spaces]] are the [[tensor product]] of the separate [[hom objects]]

   $$
     (\mathcal{C}\times \mathcal{D})((c_1,d_1),\;(c_2,d_2) )
       \coloneqq
     \mathcal{C}(c_1,c_2)\otimes \mathcal{D}(d_1,d_2)
   $$

   and whose [[composition]] operation is the [[braiding]] (eq:BraidingIsomorphism) followed by the [[tensor product]] of the separate composition operations:

   $$
     \array{
       (\mathcal{C}\times \mathcal{D})((c_1,d_1), \; (c_2,d_2))
         \otimes
       (\mathcal{C}\times \mathcal{D})((c_2,d_2), \; (c_3,d_3))
       \\
       {}^{\mathllap{=}}\downarrow
       \\
       \left(\mathcal{C}(c_1,c_2) \otimes \mathcal{D}(d_1,d_2)\right)
         \otimes
       \left(\mathcal{C}(c_2,c_3) \otimes \mathcal{D}(d_2,d_3)\right)
       \\
       \downarrow^{\mathrlap{\tau}}_{\mathrlap{\simeq}}
       \\
       \left(\mathcal{C}(c_1,c_2) \otimes \mathcal{C}(c_2,c_3)\right)
         \otimes
       \left( \mathcal{D}(d_1,d_2) \otimes  \mathcal{D}(d_2,d_3)\right)
         &\overset{
             (\circ_{c_1,c_2,c_3}) \otimes (\circ_{d_1,d_2,d_3})
           }{\longrightarrow}
         &
       \mathcal{C}(c_1,c_3) \otimes \mathcal{D}(d_1,d_3)
       \\
       && \downarrow^{\mathrlap{=}}
       \\
       && (\mathcal{C}\times \mathcal{D})((c_1,d_1),\; (c_3,d_3))
     }
    \,.
   $$

=--




+-- {: .num_defn #TopologicallyEnrichedFunctor}
###### Definition
**([[enriched functor]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$ and $\mathcal{D}$ be two $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}).

A _$\mathcal{V}$-[[enriched functor]]_ from $\mathcal{C}$ to $\mathcal{D}$

$$
  F \;\colon\;  \mathcal{C}  \longrightarrow \mathcal{D}
$$

is

1. a [[function]]

   $$
     F_{Obj} \;\colon\; Obj_{\mathcal{C}} \longrightarrow Obj_{\mathcal{D}}
   $$

   of [[objects]];

1. for each $a,b \in Obj_{\mathcal{C}}$ a [[morphism]] in $\mathcal{V}$

   $$
     F_{a,b} 
       \;\colon\; 
     \mathcal{C}(a,b) 
       \longrightarrow 
     \mathcal{D}(F_0(a), F_0(b))
   $$

   between [[hom-objects]]

such that this preserves [[composition]] and [[identity]] morphisms in the evident sense.

=--

+-- {: .num_example #EnrichedHomFunctor}
###### Example
**([[enriched hom-functor]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$ be a $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}). Then there is a $\mathcal{V}$-[[enriched functor]] out of the enriched [[product category]] of $\mathcal{C}$ with its enriched [[opposite category]] (Def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}) 

$$
  \mathcal{C}(-,-)
  \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  \mathcal{V}
$$

to $\mathcal{V}$, regarded as a $\mathcal{V}$-[[enriched category]] (Example \ref{TopkAsATopologicallyEnrichedCategory}), which sends a [[pair]] of [[objects]] $X,Y \in \mathcal{C}$ to the [[hom-object]] $\mathcal{C}(X,Y) \in \mathcal{V}$, and which acts on morphisms by [[composition]] in the evident way.

=--

+-- {: .num_example #EnrichedPresheaf}
###### Example
**([[enriched presheaves]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$ be a $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}). Then a $\mathcal{V}$-[[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor})

$$
  F \;\colon\; \mathcal{C} \longrightarrow \mathcal{V}
$$

to the archetypical $\mathcal{V}$-[[enriched category]] from Example \ref{TopkAsATopologicallyEnrichedCategory} is:

1. an [[object]] $F_a \in Obj_{\mathcal{V}}$ for each object $a \in Obj_{\mathcal{C}}$;

1. a [[morphism]] in $\mathcal{V}$ of the form

   $$
     F_a \otimes \mathcal{C}(a,b) \longrightarrow F_b
   $$

   for all pairs of objects $a,b \in Obj(\mathcal{C})$

   (this is the [[adjunct]] of $F_{a,b}$ under the [[adjunction]] (eq:InternalHomAdjunction) on $\mathcal{V}$)

such that composition is respected, in the evident sense.

For every object $c \in \mathcal{C}$, there is an enriched [[representable functor]], denoted 

$$
  y(c) \;\coloneqq\; \mathcal{C}(c,-) 
$$

(where on the right we have the [[enriched hom-functor]] from Example \ref{EnrichedHomFunctor})

which sends objects to

$$
  y(c)(d) = \mathcal{C}(c,d) \in \mathcal{V}
$$

and whose action on morphisms is, under the above identification, just the [[composition]] operation in $\mathcal{C}$.

=--


More generally, the following situation will be of interest:

+-- {: .num_example #PointedTopologicalFunctorOnProductCategory}
###### Example
**([[enriched functor]] on [[enriched category|enriched]] [[product category]] with [[opposite category]])**

An $\mathcal{V}$-[[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor}) into $\mathcal{V}$ (Example \ref{TopkAsATopologicallyEnrichedCategory})  out of 
an [[enriched category|enriched]] [[product category]] (Def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory})

$$
  F
    \;\colon\;
  \mathcal{C} \times \mathcal{D}
    \longrightarrow
  \mathcal{V}
$$

(an "enriched [[bifunctor]]") has component morphisms of the form

$$
  F_{(c_1,d_1),(c_2,d_2)}
    \;\colon\;
  \mathcal{C}(c_1,c_2)
  \otimes
  \mathcal{D}(d_1,d_2)
    \longrightarrow
  \big[ F_0((c_1,d_1)),F_0((c_2,d_2)) \big]
  \,.
$$

By functoriality and under passing to [[adjuncts]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) under (eq:InternalHomAdjunction)  this is equivalent to two commuting _[[actions]]_


$$
  \rho_{c_1,c_2}(d)
   \;\colon\;
  \mathcal{C}(c_1,c_2) \otimes F_0((c_1,d))
    \longrightarrow
  F_0((c_2,d))
$$

and

$$
  \rho_{d_1,d_2}(c)
    \;\colon\;
  \mathcal{D}(d_1,d_2) \otimes F_0((c,d_1))
    \longrightarrow
  F_0((c,d_2))
  \,.
$$

In the special case of a functor out of the [[enriched category|enriched]] [[product category]] of some $\mathcal{V}$-[[enriched category]] $\mathcal{C}$ with its enriched [[opposite category]] (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory})

$$
  F
    \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  \mathcal{V}
$$

then this takes the form of a "pullback action" in the first variable

$$
  \rho_{c_2,c_1}(d)
   \;\colon\;
  \mathcal{C}(c_1,c_2) \otimes F_0((c_2,d))
    \longrightarrow
  F_0((c_1,d))
$$

and a "pushforward action" in the second variable

$$
  \rho_{d_1,d_2}(c)
    \;\colon\;
  \mathcal{C}(d_1,d_2) \otimes F_0((c,d_1))
    \longrightarrow
  F_0((c,d_2))
  \,.
$$


=--


+-- {: .num_defn #EnrichedNaturalTransformation}
###### Definition
**([[enriched natural transformation]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$ and $\mathcal{D}$ be two $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}) and let

$$
  \mathcal{C}
    \underoverset
      {\underset{G}{\longrightarrow}}
      {\overset{F}{\longrightarrow}}
      {}
  \mathcal{D}
$$

be two $\mathcal{V}$-[[enriched functors]] (Def. \ref{TopologicallyEnrichedFunctor}) from $\mathcal{C}$ to $\mathcal{D}$.

Then a $\mathcal{V}$-[[enriched natural transformation]]

$$
  \mathcal{C}
    \underoverset
      {\underset{G}{\longrightarrow}}
      {\overset{F}{\longrightarrow}}
      {\phantom{AA}\Downarrow{\mathrlap{\eta}}\phantom{AA}}
  \mathcal{D}
$$

is 

* for each $c \in Obj_{\mathcal{C}}$ a choice of [[morphism]] 

  $$
    \eta_c \;\colon\; I \longrightarrow \mathcal{D}(F(c),G(c))
  $$ 

  such that for each [[pair]] of [[objects]] $c,d \in \mathcal{C}$ the two [[morphisms]] (in $\mathcal{V}$)

\[
  \label{OneComposite}
  \eta_d \circ F(-) 
   \;\colon\; 
  \mathcal{C}(c,d)
    \overset{r}{\simeq} 
  \mathcal{C}(c,d) \otimes I
    \overset{ G_{c,d} \otimes \eta_c }{\longrightarrow} 
  \mathcal{D}(G(c),G(d)) \otimes \mathcal{D}( F(c), G(c) ) 
    \overset{\circ_{F(c), G(c), G(d)}}{\longrightarrow} 
  \mathcal{D}(F(c), G(d))
\]

and

\[
  \label{OtherComposite}
  G(-) \circ \eta_c 
    \;\colon\; 
  \mathcal{C}(c,d) 
    \overset{\ell}{\simeq}
  I \otimes  \mathcal{C}(c,d) 
    \overset{ \eta_d \otimes F_{c,d} }{\longrightarrow}
  \mathcal{D}(F(d), G(d)) \otimes \mathcal{D}(F(c), F(d))
    \overset{\circ_{F(c),F(d), G(d)}}{\longrightarrow}
  \mathcal{D}(F(c), G(d))
\]

agree.

=--

+-- {: .num_example #CategoryOfEnrichedFunctors}
###### Example
**([[functor category]] of [[enriched functors]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos})
let $\mathcal{C}$, $\mathcal{D}$ be two $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}). Then there is a [[category]] (Def. \ref{Categories}) of [[enriched functors]] (Def. \ref{TopologicallyEnrichedFunctor}), to be denoted

$$
  [\mathcal{C}, \mathcal{D}]
$$

whose [[objects]] are the [[enriched functors]] $\mathcal{C} \overset{F}{\to} \mathcal{D}$ and whose [[morphisms]] are the [[enriched natural transformations]] between these (Def. \ref{EnrichedNaturalTransformation}).

In the case that $\mathcal{V} = $ [[Set]], via Def. \ref{ExamplesOfCosmoi}, with $Set$-enriched categories identified with plain categories via Example \ref{SetEnrichedCategoriesArePlainCategories}, this coincides with the [[functor category]] from Example \ref{FunctorCategory}.

Notice that, at this point, $[\mathcal{C}, \mathcal{D}]$ is a plain [[category]], not itself a $\mathcal{V}$-[[enriched category]], unless $\mathcal{V} = $ [[Set]]. But it may be enhanced to one, this is Def. \ref{PointedTopologicalFunctorCategory} below.

=--

+-- {: .num_defn #TensoringAndPoweringOfTopologicallyEnrichedCopresheaves}
###### Definition
**([[tensoring]] and [[powering]] of [[enriched presheaves]])**

Let $\mathcal{C}$ be a $\mathcal{V}$-[[enriched category]], def. \ref{TopEnrichedCategory}, with $[\mathcal{C}, \mathcal{V}]$ its [[functor category]] of [[enriched functors]] (Example \ref{CategoryOfEnrichedFunctors}).

1. Define a [[functor]]

   $$
     (-)\cdot(-)
       \;\colon\;
     [\mathcal{C}, \mathcal{V}] \times \mathcal{V}
      \longrightarrow
     [\mathcal{C}, \mathcal{V}]
   $$

   by forming objectwise [[tensor products]] 

   $$
     F \cdot X \;\colon\; c \mapsto F(c) \otimes X
     \,.
   $$

   This is called the **[[tensoring]]** of $[\mathcal{C}, \mathcal{V}]$ over $\mathcal{V}$.

1. Define a functor

   $$
     (-)^{(-)}
       \;\colon\;
     \mathcal{V}^{op} \times [\mathcal{C}, \mathcal{V}]
       \longrightarrow
     [\mathcal{C}, \mathcal{V}]
   $$

   by forming objectwise [[internal homs]] (Def. \ref{ClosedMonoidalCategory})

   $$
     F^X \;\colon\; c \mapsto [X,F(c)]
     \,.
   $$

   This is called the **[[powering]]** of $[\mathcal{C}, \mathcal{V}]$ over $\mathcal{V}$.


=--

There is now the following evident generalization of the concept of _[[adjoint functors]]_ (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) from plain [[category theory]] to [[enriched category theory]]:

+-- {: .num_defn #EnrichedAdjunction}
###### Definition
**([[enriched adjunction]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$, $\mathcal{D}$ be two $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}). Then an _[[adjoint pair]] of $\mathcal{V}$-[[enriched functors]]_ or _[[enriched adjunction]]_ 

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

is a [[pair]] of $\mathcal{V}$-[[enriched functors]] (Def. \ref{TopologicallyEnrichedFunctor}), as shown, such that there is a $\mathcal{V}$-[[enriched natural isomorphism]] (Def. \ref{EnrichedNaturalTransformation}) between [[enriched hom-functors]] (Def. \ref{EnrichedHomFunctor}) of the form

\[
  \label{EnrichedAdjunctionIsomorphism}
  \mathcal{C}(L(-),-)
  \;\simeq\;
  \mathcal{D}(-,R(-))
  \,.
\]

=--


+-- {: .num_defn #EnrichedEquivalenceOfCategories}
###### Definition
**([[enriched category theory|enriched]] [[equivalence of categories]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$, $\mathcal{D}$ be two $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}). Then an _equivalence of enriched categories_

$$
  \array{
    \mathcal{C}
      \underoverset
        {\underset{R}{\longrightarrow}}
        {\overset{L}{\longleftarrow}}
        {\phantom{AA} \simeq \phantom{AA}}
    \mathcal{D}
  }
$$

is a [[pair]] of $\mathcal{V}$-[[enriched functors]] back and forth, as shown (Def. \ref{TopologicallyEnrichedFunctor}), together with $\mathcal{V}$-[[enriched natural isomorphisms]] (Def. \ref{EnrichedNaturalTransformation}) between their [[composition]] and the [[identity functors]]:

$$
  id_{\mathcal{D}} \overset{\simeq}{\Rightarrow} R \circ L 
  \phantom{AAA}
   \text{and}
  \phantom{AAA}
  L \circ R \overset{\simeq}{\Rightarrow} id_{\mathcal{C}}
  \,.
$$


=--


## Universal constructions

### (Co)Limits

(...)


+-- {: .num_example #InitialAndTerminalObjectInTermsOfAdjunction}
###### Example
**([[initial object|initial]] and [[terminal object]] in terms of [[adjunction]])**

Let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}).

1. The following are equivalent:

   1. $\mathcal{C}$ has a [[terminal object]];

   1. the unique [[functor]] $\mathcal{C} \to \ast$ (Def. \ref{Functors}) to the [[terminal category]] (Example \ref{InitialCategoryAndTerminalCategory}) has a [[right adjoint]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets})

      $$
        \ast 
          \underoverset
             {\underset{}{\longrightarrow}}
             {\overset{}{\longleftarrow}}
             {\bot}
        \mathcal{C}
      $$

    Under this equivalence, the [[terminal object]] is identified with the image under the right adjoint of the unique object of the [[terminal category]].

1. Dually, the following are equivalent:

   1. $\mathcal{C}$ has an [[initial object]];

   1. the unique [[functor]] $\mathcal{C} \to \ast$ to the [[terminal category]] has a [[left adjoint]]

      $$
        \mathcal{C}
          \underoverset
             {\underset{}{\longrightarrow}}
             {\overset{}{\longleftarrow}}
             {\bot}
        \ast
      $$

    Under this equivalence, the [[initial object]] is identified with the image under the left adjoint of the unique object of the [[terminal category]].

=--

+-- {: .proof}
###### Proof

Since the unique [[hom-set]] in the [[terminal category]] is [[generalized the|the]] [[singleton]], the hom-isomorphism (eq:HomIsomorphismForAdjointFunctors) characterizing the [[adjoint functors]] is directly the [[universal property]] of an [[initial object]] in $\mathcal{C}$
 
$$
  Hom_{\mathcal{C}}( L(\ast) , X )
  \;\simeq\;
  Hom_{\ast}( \ast, R(X) ) 
  =
  \ast 
$$

or of a [[terminal object]]

$$
  Hom_{\mathcal{C}}( X , R(\ast) )
  \;\simeq\;
  Hom_{\ast}( L(X), \ast ) = \ast
  \,,
$$

respectively.

=--


+-- {: .num_prop #AdjointsPreserveCoLimits}
###### Proposition
**([[left adjoints preserve colimits and right adjoints preserve limits]])**

Let $(L \dashv R) \colon \mathcal{D} \to \mathcal{C}$ be a pair of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}). Then

* $L$ [[preserved limit|preserves]] all [[colimits]] that exist in $\mathcal{C}$, 

* $R$ preserves all [[limits]] in $\mathcal{D}$.  

=--

+-- {: .proof}
###### Proof

Let $y : I \to \mathcal{D}$ be a [[diagram]] whose [[limit]] $\lim_{\leftarrow_i} y_i$ exists. Then we have a sequence of [[natural isomorphism]]s, natural in $x \in C$

$$
  \begin{aligned}
    Hom_{\mathcal{C}}(x, R {\lim_\leftarrow}_i y_i)
    &  \simeq
    Hom_{\mathcal{D}}(L x, {\lim_\leftarrow}_i y_i)
    \\
    & \simeq
    {\lim_\leftarrow}_i Hom_{\mathcal{D}}(L x, y_i)
    \\
    & \simeq
    {\lim_\leftarrow}_i Hom_{\mathcal{C}}( x, R y_i)
    \\  
    & \simeq
    Hom_{\mathcal{C}}( x, {\lim_\leftarrow}_i R y_i)
    \,,
  \end{aligned}
$$

where we used the hom-isomorphism (eq:HomIsomorphismForAdjointFunctors) and the fact that any [[hom-functor]] preserves limits (see there). Because this is natural in $x$ the [[Yoneda lemma]] implies that we have an [[isomorphism]]

$$
  R {\lim_\leftarrow}_i y_i
  \simeq
  {\lim_\leftarrow}_i R y_i
  \,.
$$

The argument that shows the preservation of colimits by $L$ is analogous.

=--


+-- {: .num_prop #LimitsCommuteWithLimits}
###### Proposition
**([[limits commute with limits]])**

Let $\mathcal{D}$ and $\mathcal{D}'$ be [[small categories]] (Def. \ref{SmallCategory}) and let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}) which admits [[limits]] of shape $\mathcal{D}$ as well as [[limits]] of shape $\mathcal{D}'$. Then these limits "commute" with each other, in that 
for $F \;\colon\; \mathcal{D} \times {\mathcal{D}'} \to \mathcal{C}$ a [[functor]] (hence a [[diagram]] of shape the [[product category]]), with corresponding [[adjunct]] functors (via Example \ref{GrpdIsACartesianClosedCategory})

$$
  {\mathcal{D}'} 
    \overset{F_{\mathcal{D}}}{\longrightarrow} 
  [\mathcal{D},\mathcal{C}]
  \phantom{AAA}
  {\mathcal{D}} 
    \overset{F_{\mathcal{D}'}}{\longrightarrow} 
  [{\mathcal{D}'},   \mathcal{C}]
$$

we have that the canonical comparison morphism 

\[
  \label{ComparisonMorphismForCommutingLimits}
  lim F \simeq lim_{\mathcal{D}}  (lim_{\mathcal{D}'} F_{\mathcal{D}} )
  \simeq
   lim_{\mathcal{D}'}  (lim_{\mathcal{D}} F_{\mathcal{D}'} )
\]

is an [[isomorphism]].

=--

+-- {: .proof}
######Proof

Since the [[limit]]-construction is the [[right adjoint]] functor to the [[constant functor|constant]] [[diagram]]-functor, this is a special case of _[[right adjoints preserve limits]]_ (Prop. \ref{AdjointsPreserveCoLimits}).

=--


See _[[limits and colimits by example]]_ for what formula (eq:ComparisonMorphismForCommutingLimits) says for instance for the special case $\mathcal{C} =$ [[Set]].

+-- {: .num_remark}
###### Remark
**(general non-commutativity of limits with colimits)**

In general limits do _not_ commute with [[colimits]]. But under a number of special conditions of interest they do. Special cases and concrete examples are discussed at _[[commutativity of limits and colimits]]_.

=--




### Enriched (co)ends
 {#TopologicalEndsAndCoends}

For working with [[enriched categories]] (Def. \ref{TopEnrichedCategory}) , a certain shape of [[limits]]/[[colimits]] is particularly relevant: these are called _[[ends]]_ and _[[coends]]_ (Def. \ref{EndAndCoendInTopcgSmash} below). We here introduce these and then derive some of their basic properties, such as notably the expression for [[Kan extension]] in terms of ([[coends|co-]])[[ends]] (prop. \ref{TopologicalLeftKanExtensionBCoend} below). 

$\,$



+-- {: .num_defn #EndAndCoendInTopcgSmash}
###### Definition
**([[end|(co)end]])**

Let $\mathcal{C}$ be a [[small category|small]] $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}).  Let

$$
  F
    \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  \mathcal{V}
$$

be an [[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor}) out of the enriched [[product category]] of $\mathcal{C}$ with its [[opposite category]] (Def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}). Then:


1. The  **[[coend]]** of $F$, denoted 

   $$
     \overset{c \in \mathcal{C}}{\int} F(c,c)
     \;\in\;
     \mathcal{V}
     \,,
   $$

   is the [[coequalizer]] in $\mathcal{V}$ of the two [[actions]] encoded in $F$ via Example \ref{PointedTopologicalFunctorOnProductCategory}:

   $$
     \underset{c,d \in \mathcal{C}}{\coprod} \mathcal{C}(c,d) \otimes F(d,c)
      \underoverset
        {\underset{\underset{c,d}{\sqcup} \rho_{(d,c)}(c) }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} \rho_{(c,d)}(d) }{\longrightarrow}}
        {\phantom{AAAAAAAA}}
     \underset{c \in \mathcal{C}}{\coprod} F(c,c)
      \overset{coeq}{\longrightarrow}
     \overset{c\in \mathcal{C}}{\int} F(c,c)
     \,.
   $$

1. The **[[end]]** of $F$, denoted 

   $$
     \underset{c\in \mathcal{C}}{\int} F(c,c)
     \;\in\;
     \mathcal{V}
     \,,
   $$

   is the **[[equalizer]]** in $\mathcal{V}$ of the [[adjuncts]] of the two actions encoded in $F$ via example \ref{PointedTopologicalFunctorOnProductCategory}:

   $$
     \underset{c\in \mathcal{C}}{\int} F(c,c)
       \overset{\;\;equ\;\;}{\longrightarrow}
     \underset{c \in \mathcal{C}}{\prod} F(c,c)
      \underoverset
        {\underset{\underset{c,d}{\sqcup} \tilde \rho_{(c,d)}(c)  }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} \tilde\rho_{d,c}(d)}{\longrightarrow}}
        {\phantom{AAAAAAAA}}
      \underset{c\in \mathcal{C}}{\prod}
      \big[ 
      \mathcal{C}\left(c,d\right), \;  F\left(c,d\right) \big]
     \,.
   $$

=--

+-- {: .num_example #CoendGivesQuotientByDiagonalGroupAction}
###### Example

For $\mathcal{V}$ a [[cosmos]], let $G \in \mathcal{V}$ be a [[group object]]. There is the n the one-object $\mathcal{V}$-[[enriched category]] $\mathbf{B}G$ as in Example \ref{DeloopingGroupoid}.

Then a $\mathcal{V}$-[[enriched functor]]

$$
  (X,\rho_l) \;\colon\; \mathbf{B}G \longrightarrow \mathcal{V}
$$

is an [[object]] $X \coloneqq F(\ast) \; \in \mathcal{V}$ equipped with a [[morphism]]

$$
  \rho_l \;\colon\; G \otimes X \longrightarrow X
$$

satisfying the [[action]] property. Hence this is equivalently an [[action]]  of $G$ on $X$.

The [[opposite category]] (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}) $(\mathbf{B}G)^{op}$ comes from the [[opposite group]]-[[group object|object]]

$$
  (\mathbf{B}G)^{op}
  =
  \mathbf{B}(G^{op})
  \,.
$$

(The isomorphism $G \simeq G^{op}$ induces a canonical euqivalence of enriched categories $(\mathbf{B}G)^{op} \simeq \mathbf{B}G$.)

So an [[enriched functor]]

$$
  (Y,\rho_r) 
    \;\colon\; 
  (\mathbf{B} G)^{op} \longrightarrow \mathcal{V}
$$

is equivalently a  _right_ [[action]] of $G$.

Therefore the [[coend]] of two such functors (def. \ref{EndAndCoendInTopcgSmash}) coequalizes the relation

$$
  (x g,\;y)
   \sim
  (x,\; g y)
$$

(where juxtaposition denotes left/right action) and is the [[quotient]] of the plain [[tensor product]] by the [[diagonal action]] of the group $G$:

$$
  \overset{\ast \in \mathbf{B}(G_+)}{\int}
   (Y,\rho_r)(\ast) \,\otimes\, (X,\rho_l)(\ast)
  \;\simeq\;
  Y \otimes_G X
  \,.
$$


=--

+-- {: .num_example #NaturalTransformationsViaEnds}
###### Example
**([[enriched natural transformations]] as [[ends]])**

Let $\mathcal{C}$ be a [[small category|small]] [[enriched category]] (Def. \ref{TopEnrichedCategory}). For
$
  F, G
  \;\colon\;
  \mathcal{C}
    \longrightarrow
  \mathcal{V}
$
two [[enriched presheaves]] (Example \ref{EnrichedPresheaf}), the [[end]] (def. \ref{EndAndCoendInTopcgSmash}) of the [[internal-hom]]-functor

$$
  [F(-),G(-)]
  \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
  \longrightarrow
  \mathcal{V}
$$ 

is an [[object]] of $\mathcal{V}$ whose underlying [[set]] (Example \ref{ChangeOfCosmosFromVToSet}) is the set of [[enriched natural transformations]] $F \Rightarrow G$ (Def. \ref{EnrichedNaturalTransformation})

$$
  Hom_{\mathcal{V}}\left(1,
  \left(
    \underset{c \in \mathcal{C}}{\int} 
    \big[ F(c),G(c) \big]
  \right)
  \right)
  \;\simeq\;
  Hom_{[\mathcal{C}, \mathcal{V}]}(F,G)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The underlying pointed set functor $Hom_{\mathcal{V}}(1,-)\colon \mathcal{V}\to Set$ [[preserved limit|preserves]] all [[limits]]. Therefore there is an [[equalizer]] diagram in [[Set]] of the form

$$
  Hom_{\mathcal{V}}\left(1,
  \left(
    \underset{c\in \mathcal{C}}{\int}
    [F(c),G(c)]
  \right)
  \right)
    \overset{equ}{\longrightarrow}
  \underset{c\in \mathcal{C}}{\prod} Hom_{\mathcal{V}}(F(c),G(c))
      \underoverset
        {\underset{\underset{c,d}{\sqcup} U(\tilde \rho_{(c,d)}(c))  }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} U(\tilde\rho_{d,c}(d))}{\longrightarrow}}
        {\phantom{AAAAAAAA}}
   \underset{c,d\in \mathcal{C}}{\prod}
    Hom_{\mathcal{V}}(
      \mathcal{C}(c,d),
      [F(c),G(d)]
    )
 \,,
$$

where we used Example \ref{UnderlyingSetOfInternalHomIsHomSet} to identify underlying sets of internal homs with [[hom-sets]].

Here the object in the middle is just the set of [[indexed sets]] of component morphisms $\left\{ F(c)\overset{\eta_c}{\to} G(c)\right\}_{c\in \mathcal{C}}$. The two parallel maps in the equalizer diagram take such a collection to the [[indexed set]] of composites (eq:OneComposite) and (eq:OtherComposite). Hence that these two are equalized is precisely the condition that the indexed set of components constitutes an [[enriched natural transformation]].

=--

Conversely, example \ref{NaturalTransformationsViaEnds} says that [[ends]] over [[bifunctors]] of the form $[F(-),G(-))]$ constitute [[hom-spaces]] between pointed [[topologically enriched functors]]:


+-- {: .num_defn #PointedTopologicalFunctorCategory}
###### Definition
**([[enriched presheaf category]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$ be a [[small category|small]] $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}). 

Then the $\mathcal{V}$-[[enriched presheaf category]] $[\mathcal{C}, \mathcal{V}]$ is $\mathcal{V}$-[[enriched functor category]] from $\mathcal{C}$ to $\mathcal{V}$, hence is the following $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory})

1. the [[objects]] are the $\mathcal{C}$-[[enriched functors]] $\mathcal{C} \overset{F}{\to}\mathcal{V}$ (Def. \ref{TopologicallyEnrichedFunctor});

1. the [[hom-objects]] are the [[ends]]

   \[
     \label{HomObjectOfEnrichedFunctorCategoryViaEnd}
     [\mathcal{C}, \mathcal{V}](F,G)
       \;\coloneqq\;
     \int_{c\in \mathcal{C}} [F(c),G(c)]
   \]

1. the [[composition]] operation on these is defined to be the one induced by the composite maps

   $$
     \left(
       \underset{c\in \mathcal{C}}{\int} [F(c),G(c)]
     \right)
     \otimes
     \left(
       \underset{c \in \mathcal{C}}{\int} [G(c),H(c)]
     \right)
       \overset{}{\longrightarrow}
     \underset{c\in \mathcal{C}}{\prod}
       [F(c),G(c)] \otimes [G(c),H(c)]
     \overset{(\circ_{F(c),G(c),H(c)})_{c\in \mathcal{C}}}{\longrightarrow}
     \underset{c \in \mathcal{C}}{\prod}
       [F(c),H(c)]
     \,,
   $$

   where the first morphism is degreewise given by projection out of the limits that defined the ends. This composite evidently equalizes the two relevant adjunct actions (as in the proof of example \ref{NaturalTransformationsViaEnds}) and hence defines a map into the end

   $$
       \left(
       \underset{c\in \mathcal{C}}{\int} [F(c),G(c)]
     \right)
     \otimes
     \left(
       \underset{c \in \mathcal{C}}{\int} [G(c),H(c)]
     \right)
     \longrightarrow
     \underset{c\in \mathcal{C}}{\int} [F(c),H(c)]
     \,.
   $$

By Example \ref{NaturalTransformationsViaEnds}, the underlying plain category (Example \ref{UnderlyingCategoryOfTopEnrichedCategory}) of this [[enriched functor category]] is the plain [[functor category]] of [[enriched functors]] from Example \ref{CategoryOfEnrichedFunctors}.

=--




+-- {: .num_prop #YonedaReductionTopological}
###### Proposition
**([[enriched Yoneda lemma]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}) let $\mathcal{C}$ be a [[small category|small]] [[enriched category]] (Def. \ref{TopEnrichedCategory}). For $F \colon \mathcal{C} \to \mathcal{V}$ an [[enriched presheaf]] (Example \ref{EnrichedPresheaf}) and for $c\in \mathcal{C}$ an [[object]], there is a [[natural isomorphism]]

$$
  [\mathcal{C}, \mathcal{V}](\mathcal{C}(c,-),\; F)
  \;\simeq\;
  F(c)
$$

between the [[hom-object]] of the [[enriched functor category]] (Def. \ref{PointedTopologicalFunctorCategory}), from the [[representable functor|functor represented]] by $c$ to $F$, and the value of $F$ on $c$.

In terms of the [[ends]] (def. \ref{EndAndCoendInTopcgSmash}) defining these [[hom-objects]] (eq:HomObjectOfEnrichedFunctorCategoryViaEnd), this means that

$$
  \underset{d\in \mathcal{C}}{\int} [\mathcal{C}(c,d), F(d)]
    \;\simeq\;
  F(c)
  \,.
$$

In this form the statement is also known as **[[Yoneda reduction]]**.

=--

Now that [[natural transformations]] are expressed in terms of [[ends]] (example \ref{NaturalTransformationsViaEnds}), as is the [[enriched Yoneda lemma]] (prop. \ref{YonedaReductionTopological}), it is natural to consider the [[formal duality|dual]] statement involving [[coends]]:

+-- {: .num_prop #TopologicalCoYonedaLemma}
###### Proposition
**([[enriched co-Yoneda lemma]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$ be a [[small category|small]] $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}). For $F \colon \mathcal{C}\to \mathcal{V}$ an [[enriched presheaf]] (Def. \ref{EnrichedPresheaf}) and for $c\in \mathcal{C}$ an [[object]], there is a [[natural isomorphism]]

$$
  F(-)
    \simeq
  \overset{c \in \mathcal{C}}{\int}
  \mathcal{C}(c,-) \otimes F(c)
  \,.
$$

Moreover, the morphism that hence exhibits $F(c)$ as the [[coequalizer]] of the two morphisms in def. \ref{EndAndCoendInTopcgSmash} is componentwise the canonical action

$$
  \mathcal{C}(c,d) \otimes F(c)
   \longrightarrow
  F(d)
$$

which is [[adjunct]] to the component map $\mathcal{C}(d,c) \to [F(c),F(d)]$ of the [[enriched functor]] $F$.

=--

(e.g. [MMSS 00, lemma 1.6](#MMSS00))

+-- {: .proof}
###### Proof

By the definition of [[coends]] and the [[universal property]] of [[colimits]], [[enriched natural transformations]] of the form

$$
  \left(
    \overset{c \in \mathcal{C}}{\int} \mathcal{C}(c,-) \otimes F(c)
  \right)
    \longrightarrow
  G
$$

are in [[natural bijection]] with systems of component morphisms

$$
  \mathcal{C}(c,d) \otimes F(c)
    \longrightarrow
  G(d)
$$

which satisfy some compatibility conditions in their dependence on $c$ and $d$ ([[enriched natural transformation|natural]] in $d$ and "[[extranatural]]" in $c$). By the [[internal hom]] [[adjunction]], these are in [[natural bijection]] to systems of morphisms of the form

$$
  F(c)
   \longrightarrow
   [\mathcal{C}(c,d), G(d)]
$$

satisfying the analogous compatibility conditions. By Example \ref{NaturalTransformationsViaEnds} these are in [[natural bijection]] with systems of morphisms

$$
  F(c) \longrightarrow [\mathcal{C},\mathcal{V}](\mathcal{C}(c,-), G(-))
$$

natural in $c$

By the [[enriched Yoneda lemma]] (Prop. \ref{YonedaReductionTopological}), these, finally, are in [[natural bijection]] with systems of morphisms 

$$
  F(c) \longrightarrow G(c)
$$

natural in $c$. Moreover, all these identifications are also natural in $G$. Therefore, in summary, this shows that there is a [[natural isomorphism]]

$$
  Hom_{[\mathcal{C},\mathcal{V}]}
  \left(
    \overset{c \in \mathcal{C}}{\int} \mathcal{C}(c,-) \otimes F(c)
    \;,\;
    (-)
  \right)
  \;\simeq\;
  Hom_{[\mathcal{C},\mathcal{V}]}
  \left(
    F,
    (-)
  \right)
  \,.
$$

With this, the ordinary [[Yoneda lemma]] (Prop. \ref{YonedaLemma}) in the form of the [[Yoneda embedding]] of $[\mathcal{C},\mathcal{V}]$ implies the required isomorphism.


=--

+-- {: .num_example}
###### Example
**([[co-Yoneda lemma]] over [[Set]])**

Consider the [[co-Yoneda lemma]] (Prop. \ref{TopologicalCoYonedaLemma}) in the special case $\mathcal{V} =$ [[Set]] (Example \ref{ExamplesOfCosmoi}).

In this case the coequalizer in question is the set of [[equivalence classes]] of [[pairs]]

$$
  ( c \overset{}{\to} c_0,\; x  )
  \;\;
   \in
   \mathcal{C}(c,c_0) \otimes F(c)
  \,,
$$

where two such pairs

$$
  ( c \overset{f}{\to} c_0,\; x \in F(c) )
  \,,\;\;\;\;
  ( d \overset{g}{\to} c_0,\; y \in F(d) )
$$

are regarded as equivalent if there exists

$$
  c \overset{\phi}{\to} d
$$

such that

$$
  f = g \circ \phi
  \,,
  \;\;\;\;\;and\;\;\;\;\;
  y = \phi(x)
  \,.
$$

(Because then the two pairs are the two images of the pair $(g,x)$ under the two morphisms being coequalized.)

But now considering the case that $d = c_0$ and $g = id_{c_0}$, so that $f = \phi$ shows that any pair

$$
  ( c \overset{\phi}{\to} c_0, \; x \in F(c))
$$

is identified, in the coequalizer, with the pair

$$
  (id_{c_0},\; \phi(x) \in F(c_0))
  \,,
$$

hence with $\phi(x)\in F(c_0)$.

=--


+-- {: .num_remark}
###### Remark

The statement of the [[co-Yoneda lemma]] in prop. \ref{TopologicalCoYonedaLemma} is a kind of [[categorification]] of the following statement in [[analysis]] (whence the notation with the integral signs):

For $X$ a [[topological space]], $f \colon X \to\mathbb{R}$ a [[continuous function]] and $\delta(-,x_0)$ denoting the [[Dirac distribution]], then

$$
  \int_{x \in X} \delta(x,x_0) f(x)
  =
  f(x_0)
  \,.
$$

=--

It is this analogy that gives the name to the following statement:

+-- {: .num_prop #CoendsCommuteWithEachOther}
###### Proposition
**([[Fubini theorem]] for (co)-ends)**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}_1, \mathcal{C}_2$ be two $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}) and

$$
   F
  \;\colon\;
  \left(
    \mathcal{C}_1\times\mathcal{C}_2
  \right)^{op}
  \times
  (\mathcal{C}_1 \times\mathcal{C}_2)
  \longrightarrow
  \mathcal{V}
$$

a $\mathcal{V}$-[[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor})  from the [[product category]] with [[opposite categories]] (Def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}), as shown.

Then its [[end]] and [[coend]] (def. \ref{EndAndCoendInTopcgSmash}) is equivalently formed consecutively over each [[variable]], in either order:

$$
  \overset{(c_1,c_2)}{\int} F((c_1,c_2), (c_1,c_2))
  \simeq
  \overset{c_1}{\int}
  \overset{c_2}{\int}
  F((c_1,c_2), (c_1,c_2))
  \simeq
  \overset{c_2}{\int}
  \overset{c_1}{\int}
  F((c_1,c_2), (c_1,c_2))
$$

and

$$
  \underset{(c_1,c_2)}{\int} F((c_1,c_2), (c_1,c_2))
  \simeq
  \underset{c_1}{\int}
  \underset{c_2}{\int}
  F((c_1,c_2), (c_1,c_2))
  \simeq
  \underset{c_2}{\int}
  \underset{c_1}{\int}
  F((c_1,c_2), (c_1,c_2))
  \,.
$$

=--

+-- {: .proof}
###### Proof

Because [[limits]] commute with limits, and [[colimits]] commute with colimits.

=--



+-- {: .num_remark #MappingSpacePreservesEnds}
###### Remark
**([[internal hom]] preserves [[ends]])**

Let $\mathcal{V}$ be a [[cosmos]] (Def. \ref{Cosmos}). Since the [[internal hom]]-functor in $\mathcal{V}$ (Def. \ref{ClosedMonoidalCategory}) preserves [[limits]] in both variables (Prop. \ref{InternalHomPreservesLimits}), in particular it preserves [[ends]] (Def. \ref{EndAndCoendInTopcgSmash}) in the second variable, and sends coends in the second variable to ends:

For all [[small category|small]] $\mathcal{C}$-[[enriched categories]], $\mathcal{V}$-[[enriched functors]] $F \;\colon\; \mathcal{C}^{op} \otimes \mathcal{C} \to \mathcal{V}$ (Def. \ref{TopologicallyEnrichedFunctor}) and all [[objects]] $X \in \mathcal{V}$ we have [[natural isomorphisms]]

$$
  \left[ 
    X , \int^{c \in \mathcal{C}} F(c,c)
  \right]
  \;\simeq\;
  \int^{c \in \mathcal{C}} 
  \left[ X, F(c,c) \right]
$$

and

$$
  \left[ 
    \int_{c \in \mathcal{C}} F(c,c)
    ,
    X
  \right]
  \;\simeq\;
  \int^{c \in \mathcal{C}} 
  \left[ F(c,c), X \right]
  \,.
$$

=--



With this [[coend]] calculus in hand, there is an elegant proof of the defining [[universal property]] of the smash [[tensoring]] and [[powering]]  [[enriched presheaves]] (Def. \ref{TensoringAndPoweringOfTopologicallyEnrichedCopresheaves}):

+-- {: .num_prop #UniversalPropertyOfTensoringAndPoweringOfFunctorsToTopcg}
###### Proposition
**([[universal property]] of [[tensoring]] and [[powering]] of [[enriched presheaves]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$ be a [[small category|small]] $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}), with $[\mathcal{C},\mathcal{V}]$ the corresponding [[enriched presheaf|enriched presheaf category]].

Then there are [[natural isomorphisms]]

$$
  [\mathcal{C}, \mathcal{V}]( X \cdot K ,\, Y )
    \;\simeq\;
  [K,\big( [\mathcal{C}, \mathcal{V}]\left( X, Y \right) \big)]
$$

and

$$
  [\mathcal{C}, \mathcal{V}]\left( X,\, Y^K \right)
    \;\simeq\;
  [K, \big( [\mathcal{C}, \mathcal{C}](X,Y) \big) ]
$$

for all $X,Y \in [\mathcal{C}, \mathcal{V}]$ and all $K \in \mathcal{C}$, 
where $(-)^K$ is the [[powering]] and $(-)\cdot K$ the [[tensoring]] from Def. \ref{TensoringAndPoweringOfTopologicallyEnrichedCopresheaves}.

In particular there is the composite natural isomorphism

$$
  [\mathcal{C}, \mathcal{V}](X \cdot K, Y)
   \;\simeq\;
  [\mathcal{C}, \mathcal{V}]\left( X, Y^K \right)
$$

exhibiting a pair of [[adjoint functors]]

$$
  [\mathcal{C}, \mathcal{V}]
    \underoverset
      {\underset{(-)^K}{\longrightarrow}}
      {\overset{(-) \cdot K}{\longleftarrow}}
      {\bot}
  [\mathcal{C}, \mathcal{V}]
  \,.
$$

=--

+-- {: .proof}
###### Proof

Via the [[end]]-expression for $[\mathcal{C}, \mathcal{V}](-,-)$ from Example \ref{NaturalTransformationsViaEnds}, and the fact (remark \ref{MappingSpacePreservesEnds}) that the [[internal hom]]-functor ends in the second variable, this reduces to the fact that $[-,-]$ is the [[internal hom]] in the [[closed monoidal category]] $\mathcal{V}$ (Example \ref{TopkAsATopologicallyEnrichedCategory}) and hence satisfies the internal tensor/hom-adjunction isomorphism (prop. \ref{TensorHomAdjunctionIsoInternally}):

$$
  \begin{aligned}
    [\mathcal{C}, \mathcal{V}](X \cdot K, Y)
    & =
    \underset{c}{\int}
    [
      (X \cdot K)(c),
      Y(c)
    ]
    \\
    & \simeq
    \underset{c}{\int}
      [X(c) \otimes K, Y(x)]
    \\
    & \simeq
    \underset{c}{\int}
      [K,[X(c), Y(c)]]
    \\
    & \simeq
    [K, \underset{c}{\int} [X(c),Y(c)]]
    \\
    & =
    [K,\left( [\mathcal{C},\mathcal{V}](X,Y)\right)]
  \end{aligned}
$$

and

$$
  \begin{aligned}
    [\mathcal{C}, \mathcal{V}](X, Y^K)
    & =
    \underset{c}{\int}
      [X(c), Y^K(c)]
    \\
    & \simeq
    \underset{c}{\int}
     [ X(c), [K,Y(c)] ]
    \\
    & \simeq
    \underset{c}{\int} [ X(c) \otimes K, Y(c) ]
    \\
    & \simeq
    \underset{c}{\int} [K, [X(c),Y(c)]]
    \\
    & \simeq
    [K, \underset{c}{\int} [X(c),Y(c)] ]
    \\
    & \simeq
    [K, [\mathcal{C}, \mathcal{V}](X,Y]
    \,.
  \end{aligned}
$$

=--

$\,$


### Kan extensions


+-- {: .num_prop #TopologicalLeftKanExtensionBCoend}
###### Proposition
**([[Kan extension]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}, \mathcal{D}$ be [[small category|small]] $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}) and let

$$
  p \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
$$

be a $\mathcal{V}$-[[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor}). Then precomposition with $p$ constitutes a functor between the corresponding $\mathcal{V}$-[[enriched presheaf categories]] (Def. \ref{PointedTopologicalFunctorCategory}) 

\[
  \label{PrecompositionFunctorOnEnrichedPresheaves}
  p^\ast
  \;\colon\;
  \array{
    [\mathcal{D}, \mathcal{V}]
    &\longrightarrow&  
    [\mathcal{C}, \mathcal{V}]
    \\
    G &\mapsto& G \circ p
  }
\]

1. This [[enriched functor]] $p^\ast$ (eq:PrecompositionFunctorOnEnrichedPresheaves) has a [[enriched adjunction|enriched left adjoint]] $Lan_p$ (Def. \ref{EnrichedAdjunction}), called **left [[Kan extension]]** along $p$

   $$
     [\mathcal{D}, \mathcal{V}]
       \underoverset
         {\underset{p^\ast}{\longrightarrow}}
         {\overset{Lan_p }{\longleftarrow}}
         {\bot}
     [\mathcal{C}, \mathcal{V}]
   $$

   which is given objectwise by the [[coend]] (def. \ref{EndAndCoendInTopcgSmash}):

   \[
     \label{FormulaLeftKanExtensionByCoend}
     (Lan_p F)
     \;\colon\;
     d
     \;\mapsto \;
     \overset{c\in \mathcal{C}}{\int}
      \mathcal{D}(p(c),d) \otimes F(c)
     \,.
   \]

1. The [[enriched functor]] $p^\ast$ (eq:PrecompositionFunctorOnEnrichedPresheaves) has a [[enriched adjunction|enriched right adjoint]] $Ran_p$ (Def. \ref{EnrichedAdjunction}), called **right [[Kan extension]]** along $p$

   $$
     [\mathcal{C}, \mathcal{V}]
       \underoverset
         {\underset{Ran_p}{\longrightarrow}}
         {\overset{p^\ast}{\longleftarrow}}
         {\bot}
     [\mathcal{D}, \mathcal{V}]
   $$

   which is given objectwise by the [[end]] (def. \ref{EndAndCoendInTopcgSmash}):

   \[
     \label{FormulaRightKanExtensionByEnd}
     (Ran_p F)
     \;\colon\;
     d
     \;\mapsto \;
     \underset{c\in \mathcal{C}}{\int}
      [\mathcal{D}(d,p(c)), F(c)] 
     \,.
   \]

In summary, this means that the [[enriched functor]] 

$$
  \mathcal{C} 
    \overset{p}{\longrightarrow}
  \mathcal{D}
$$

induces, via [[Kan extension]], an [[adjoint triple]] of [[enriched functors]]

\[
  \label{KanExtensionAdjointTriple}
  Lan_p \;\dashv\; p^\ast \;\dashv\; Ran_p
  \;\colon\;
  [\mathcal{C},\mathcal{V}]    
     \leftrightarrow
  [\mathcal{D}, \mathcal{V}]
  \,.  
\]

=--

+-- {: .proof}
###### Proof

Use the expression of [[enriched natural transformations]] in terms of [[coends (example \ref{NaturalTransformationsViaEnds} and def. \ref{PointedTopologicalFunctorCategory}), then use the respect of $[-,-]$ for ends/coends (remark \ref{MappingSpacePreservesEnds}),  use the [[internal-hom]] [[adjunction]] (eq:InternalHomAdjunction), use the [[Fubini theorem]] (prop. \ref{CoendsCommuteWithEachOther}) and finally use [[Yoneda reduction]] (prop. \ref{YonedaReductionTopological}) to obtain a sequence of [[natural isomorphisms]] as follows:

$$
  \begin{aligned}
    [\mathcal{D}, \mathcal{V}]( Lan_p F, \, G )
    & =
   \underset{d \in \mathcal{D}}{\int}
    [ (Lan_p F)(d), \, G(d) ]
   \\
   & =
   \underset{d\in \mathcal{D}}{\int}
   \left[
     \overset{c \in \mathcal{C}}{\int} \mathcal{D}(p(c),d) \otimes F(c)
     ,\;
     G(d)
   \right]
    \\
  &\simeq
  \underset{d \in \mathcal{D}}{\int}
  \underset{c \in \mathcal{C}}{\int}
  [
    \mathcal{D}(p(c),d) \otimes F(c) \,,\; G(d)
  ]
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  \underset{d\in \mathcal{D}}{\int}
  [F(c),
    [
     \mathcal{D}(p(c),d) , \, G(d)
    ]
  ]
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  [F(c),
    \underset{d\in \mathcal{D}}{\int}
    [
      \mathcal{D}(p(c),d) , \, G(d)
    ]
  ]
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  [
    F(c), G(p(c))
  ]
  \\
  & =
  [\mathcal{C}, \mathcal{V}](F,p^\ast G)
  \end{aligned}
  \,.
$$

and similarly:

$$
  \begin{aligned}
    [\mathcal{D}, \mathcal{V}]( G,\, Ran_p F  )
    & \simeq
    \underset{d \in \mathcal{D}}{\int}
    [ G(d) ,\, (Ran_p F)(d), \, ]
    \\
    & \simeq
    \underset{d \in \mathcal{D}}{\int}
    \left[ G(d) 
      ,\, 
       \underset{c\in \mathcal{C}}{\int}
       [\mathcal{D}(d,p(c)), F(c)] 
    \right]
    \\
    & \simeq
    \underset{d \in \mathcal{D}}{\int}
    \underset{c\in \mathcal{C}}{\int}
    \left[  
      G(d) \otimes \mathcal{D}(d,p(c)),\, F(c)
    \right]
    \\
    & \simeq
    \underset{c\in \mathcal{C}}{\int}
    \left[  
      \overset{d \in \mathcal{D}}{\int}
      G(d) \otimes \mathcal{D}(d,p(c)),\, F(c)
    \right]
    \\
    & \simeq
    \underset{c \in \mathcal{D}}{\int}
    \left[   
      G(p(c)),\, F(c)
    \right]
    \\
    & \simeq
    [\mathcal{C}, \mathcal{V}]( p^\ast G , F )
  \end{aligned}
$$

=--

+-- {: .num_example #CoendFormulaForPresheavesOfSets}
###### Example
**([[coend]] formula for left [[Kan extension]] of ordinary [[presheaves]])**

Consider the [[cosmos]] to be $\mathcal{V} =$ [[Set]], via Example \ref{ExamplesOfCosmoi}, so that [[small category|small]] $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}) are just a plain [[small category]] (Def. \ref{Categories}) by Example \ref{SetEnrichedCategoriesArePlainCategories}, and $\mathcal{V}$-[[enriched presheaves]] (Example \ref{EnrichedPresheaf}) are just plain [[presheaves]] (Example \ref{CategoryOfPresheaves}).

Then for any plain [[functor]] (Def. \ref{Functors})

$$
  \mathcal{C}^{op}
    \overset{\phantom{AA} p \phantom{AA}}{\longrightarrow}
  (\mathcal{C}')^{op}
$$

the general formula (eq:FormulaLeftKanExtensionByCoend) for [[left Kan extension]]

$$
  [\mathcal{C}^{op},Set]
  \overset{Lan_p}{\longrightarrow}
  [(\mathcal{C}')^{op}, Set]
$$

is

$$
  (Lan_p F)(c') \simeq \int^{c \in C} C'(c', p(c)) \times F(c)
  \,.
$$

Using here the [[Yoneda lemma]] (Prop. \ref{YonedaLemma}) to rewrite $F(c) \simeq Hom_{PSh(C)}(c,F)$, this is

$$
  (Lan_p F)(c') \simeq \int^{c \in C} Hom_{C'}(c', p(c)) \times Hom_{PSh(C)}(c,F)
  \,.
$$

Hence this [[coend]]-set consists of [[equivalence classes]] of [[pairs]] of [[morphisms]]

$$
   (c' \to p(c), c \to F)
$$

where two such are regarded as equivalent whenever there is $f \colon c'_1 \to c'_2$ such that 

$$
  \array{
    && c'
    \\
    & \swarrow && \searrow
    \\
    p(c_1) && \stackrel{p(f)}{\longrightarrow} && p(c_2)
    \\
    c_1 && \stackrel{f}{\longrightarrow} && c_2
    \\
    & \searrow && \swarrow
    \\
    && F
  }
  \,.
$$

This is particularly suggestive when $p$ is a [[full subcategory]] inclusion (Def. \ref{FullyFaithfulFunctor}). For in that case we may imagine that a representative pair $(c' \to p(c), c \to F)$ is a stand-in for the actual pullback of elements of $F$ along the would-be composite "$c'\to c \to F$", only that this composite need not be defined. But the above equivalence relation is precisely that under which this composite would be invariant.

=--

### Properties

We collect here statement and proof of some key properties of the various [[universal constructions]] considered above.

$\,$

+-- {: .num_prop #FullyFaithfulAdjointTriple}
###### Proposition
**([[fully faithful functor|fully faithful]] [[adjoint triple]])**

Let $F \dashv G \dashv H$ be an [[adjoint triple]] of [[adjoint functors]]. Then $F$ is a [[fully faithful functor]] (Def. \ref{FullyFaithfulFunctor}) precisely when $H$ is. (see [this prop.](adjoint+triple#FullyFaithful))

=--


+-- {: .num_prop #LeftKanExtensionPreservesRepresentableFunctors}
###### Proposition
**([[left Kan extension]] preserves [[representable functors]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}),
let 

$$ 
  \mathcal{C}
  \overset{p}{\longrightarrow}
  \mathcal{D}
$$

be a $\mathcal{V}$-[[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor}) between [[small category|small]] $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}). 


Then the [[left Kan extension]] $Lan_p$ (Prop. \ref{TopologicalLeftKanExtensionBCoend}) takes [[representable functor|representable]] [[enriched presheaves]] $\mathcal{C}(c,-) \;\colon\; \mathcal{C} \to \mathcal{V}$ to their image under $p$:

   $$
     Lan_p \mathcal{C}(c, -) \;\simeq\; \mathcal{D}(p(c), -)
   $$

   for all $c \in C$.

=--

+-- {: .proof}
###### Proof

By the [[coend]] forumla (eq:FormulaLeftKanExtensionByCoend) have naturally in $d' \in \mathcal{D}$ the expression

$$
  \begin{aligned}
    Lan_p \mathcal{C}(c,-) 
    \;\colon\;
    d' 
    \mapsto 
     & 
    \int^{c' \in C} \mathcal{D}(p(c'), d') \otimes \mathcal{C}(c,-)(c')
    \\
    & \simeq
    \int^{c' \in C} \mathcal{D}(p(c'), d') \otimes \mathcal{C}(c,c')
    \\
    & \simeq 
    \mathcal{D}(p(c), d')
  \end{aligned} 
  \,,
$$

where the last step is the [[co-Yoneda lemma]] (Prop. \ref{TopologicalCoYonedaLemma}).

=--


+-- {: .num_example #KanExtensionOfAdjointPairIsAdjointQuadruple}
###### Example
**([[Kan extension]] of [[adjoint pair]] is [[adjoint quadruple]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$, $\mathcal{D}$ be two [[small category|small]] $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}) and let

$$
  \mathcal{C}
    \underoverset
      {\underset{p}{\longrightarrow}}
      {\overset{q}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

be a $\mathcal{V}$-[[enriched adjunction]] (Def. \ref{EnrichedAdjunction}). Then there are $\mathcal{V}$-[[enriched natural isomorphisms]] (Def. \ref{EnrichedNaturalTransformation})

$$
  (q^{op})^\ast \;\simeq\; Lan_{p^{op}}
  \;\colon\;
  [\mathcal{C}^{op},\mathcal{V}]
    \longrightarrow
  [\mathcal{D}^{op},\mathcal{V}]  
$$

$$
  (p^{op})^\ast \;\simeq\; Ran_{q^{op}}
  \;\colon\;
  [\mathcal{D}^{op},\mathcal{V}]
    \longrightarrow
  [\mathcal{C}^{op},\mathcal{V}]  
$$

between the precomposition on [[enriched presheaves]] with one functor and the left/right [[Kan extension]] of the other (Def. \ref{TopologicalLeftKanExtensionBCoend}).

By essential uniqueness of [[adjoint functors]], this means that the two [[adjoint triples]] (eq:KanExtensionAdjointTriple) of $q$ and $p$ 

$$
  \array{
    Lan_{q^{op}} &\dashv& (q^{op})^\ast &\dashv& Ran_{q^{op}}
    \\
    && Lan_{p^{op}} &\dashv& (p^{op})^\ast &\dashv& Ran_{p^{op}}
  }
$$

merge into an [[adjoint quadruple]]

$$
  \array{
    Lan_{q^{op}} &\dashv& (q^{op})^\ast &\dashv& (p^{op})^\ast &\dashv& Ran_{p^{op}}
  }
  \;\colon\;
  [\mathcal{C}^{op},\mathcal{V}]
    \leftrightarrow
  [\mathcal{D}^{op}, \mathcal{V}]
$$

=--

+-- {: .proof}
###### Proof

For every [[enriched presheaf]] $F \;\colon\; \mathcal{C}^{op} \to \mathcal{V}$ we have a sequence of $\mathcal{V}$-[[enriched natural isomorphism]] as follows

$$
  \begin{aligned}
    (Lan_{p^{op}} F)(d)
      & \simeq
    \int^{ c \in \mathcal{C} } \mathcal{D}(d,p(c)) \otimes F(c)
    \\
    & \simeq
    \int^{ c \in \mathcal{C} } \mathcal{C}(q(d),c) \otimes F(c)
    \\
    & \simeq
    F(q(d))
    \\
    & = \left( (q^{op})^\ast F\right) (d)
    \,.    
  \end{aligned}
$$

Here the first step is the [[coend]]-formula for [[left Kan extension]] (Prop. \ref{TopologicalLeftKanExtensionBCoend}), the second step if the [[enriched adjunction]]-isomorphism (eq:EnrichedAdjunctionIsomorphism) for $q \dashv p$ and the third step is the [[co-Yoneda lemma]].

This shows the first statement, which, by essential uniqueness of adjoints, implies the following statements.


=--


+-- {: .num_prop #LeftKanExtensionAlongFullyFaithfulFunctor}
###### Proposition
**([[left Kan extension]] along [[fully faithful functor]] is [[fully faithful functor|fully faithful]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}),
let 

$$ 
  \mathcal{C}
  \overset{\phantom{AA} p \phantom{AA}}{\hookrightarrow}
  \mathcal{D}
$$

be a [[fully faithful functor|fully faithful]] $\mathcal{V}$-[[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor}) between [[small category|small]] $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}). 

Then for all $c \in \mathcal{C}$
   
$$
  p^* (Lan_p c) \simeq c
$$ 

and in fact the $(Lan_F \dashv F^*)$-[[unit of an adjunction]] is a [[natural isomorphism]]

$$
  Id \stackrel{\simeq}{\to} p^* \circ Lan_{p}
  \,.
$$ 

=-- 

+-- {: .proof}
###### Proof

By the [[coend]] forumla (eq:FormulaLeftKanExtensionByCoend) have naturally in $d' \in \mathcal{D}$ the left Kan extension of any $F \;\colon\; \mathcal{C} \to \mathcal{V}$ on the image of $p$ is

$$
  \begin{aligned}
    Lan_p F 
   \;\colon\; 
   p(c) 
   \mapsto
     & \int^{c' \in C} \mathcal{D}(p(c'), p(c)) \cdot F(c') 
     \\
     & \simeq 
     \int^{c' \in C} \mathcal{C}(c', c) \cdot F(c')
     \\
     & \simeq F(c)
  \end{aligned}
  \,,
$$

where in the second step we used the assumption of [[fully faithful functor|fully faithfulness]] of $p$ and in the last step we used the [[co-Yoneda lemma]] (Prop. \ref{TopologicalCoYonedaLemma}).

=--


+-- {: .num_lemma #ColimitOfRepresentableIsSingleton}
###### Lemma
**([[colimit]] of representable is [[singleton]])**

Let $\mathcal{C}$ be a [[small category]] (Def. \ref{SmallCategory}). Then the [[colimit]] of a [[representable presheaf]] (Def. \ref{CategoryOfPresheaves}), regarded as a [[functor]]

$$
  y(c) \;\colon\; \mathcal{C}^{op} \longrightarrow Set
$$

is [[generalized the|the]] [[singleton]] set.

\[
  \label{ColimitOfRepresentableIsSingleton}
  \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim} y(c)
  \;\simeq\;
  \ast
  \,.
\]

=--

+-- {: .proof}
###### Proof

One way to see this is to regard the colimit as the [[left Kan extension]] (Prop. \ref{TopologicalLeftKanExtensionBCoend}) along the unique functor $\mathcal{C}^{op} \overset{p}{\to} \ast$ to the [[terminal category]] (Def. \ref{InitialCategoryAndTerminalCategory}). By the formula (eq:FormulaLeftKanExtensionByCoend) this is

$$
  \begin{aligned}
    \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
    y(c)
    & \simeq
    \int^{c_1 \in \mathcal{C}} 
      \underset{const_\ast(c_1)}{\underbrace{\ast(-,p(c_1))}} \times y(c)(c_1)
    \\
    & \simeq
    \int^{c_1 \in \mathcal{C}} const_\ast(c_1) \times \mathcal{C}(c_1,c) 
    \\
    & \simeq const_\ast(c)
    \\
    & \simeq \ast
  \end{aligned}
$$

where we made explicit the [[constant functor]] $const_\ast \;\colon\; \mathcal{C} \to Set$, constant on the [[singleton]] set $\ast$, and then applied the [[co-Yoneda lemma]] (Prop. \ref{TopologicalCoYonedaLemma}).

=--

+-- {: .num_prop #CategoriesWithFiniteProductsAreCosifted}
###### Proposition
**([[categories with finite products are cosifted]]**

Let $\mathcal{C}$ be a [[small category]] (Def. \ref{SmallCategory}) which has [[finite products]]. Then $\mathcal{C}$ is a _[[cosifted category]]_, equivalently its [[opposite category]] $\mathcal{C}^{op}$ is a _[[sifted category]]_, equivalently [[colimits]] over $\mathcal{C}^{op}$ with values in [[Set]] are _[[sifted colimits]]_, equivalently [[colimits]] over $\mathcal{C}^{op}$ with values in [[Set]] _[[limits commuting with colimits|commute]] with [[finite products]]_, as follows:

For $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$ to [[functors]] on the [[opposite category]] of $\mathcal{C}$ (hence two [[presheaves]] on $\mathcal{C}$, Example \ref{CategoryOfPresheaves}) we have a [[natural isomorphism]] (Def. \ref{NaturalTransformations})

$$
  \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
  \left(
    \mathbf{X} \times \mathbf{Y}
  \right)
  \;\simeq\;
  \left(
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \mathbf{X}
  \right)
  \times
  \left(
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \mathbf{Y}
  \right)
$$ 

between the [[colimit]] of their [[Cartesian product]] and the [[Cartesian product]] of their separate [[colimits]].

=--

+-- {: .proof}
###### Proof


First observe that for $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$ two [[presheaves]], their [[Cartesian product]] is a [[colimit]] over [[representable presheaf|presheaves represented]] by Cartesian products in $\mathcal{C}$. Explicity, using [[coend]]-notation, we have:

\[
  \label{OnSiteWithProductsExpandProductOfPresheaves}
  \mathbf{X} \times \mathbf{Y}
  \;\simeq\;
  \int^{c_1,c_2 \in \mathcal{C}}
  y(c_1 \times c_2) \times \mathbf{X}(c_1) \times \mathbf{Y}(c_2)
  \,,
\]

where $y \;\colon\; \mathcal{C} \hookrightarrow [\mathcal{C}^{op}, Set]$ denotes the [[Yoneda embedding]].

This is due to the following sequence of [[natural isomorphisms]]:

$$
  \begin{aligned}
    (\mathbf{X} \times \mathbf{Y})(c)
    & \simeq
    \left(
      \int^{c_1 \in \mathcal{C}}
      \mathcal{C}(c,c_1) \times \mathbf{X}(c_1)
    \right)
    \times
    \left(
      \int^{c_2 \in \mathcal{C}}
      \mathcal{C}(c,c_2) \times \mathbf{Y}(c_2)
    \right)
    \\
    & \simeq
    \int^{c_1 \in \mathcal{C}}
    \int^{c_2 \in \mathcal{C}}
    \underset{
      \simeq \mathcal{c}(c, c_1 \times c_2)
    }{
    \underbrace{
      \mathcal{C}(c,c_1) \times \mathcal{C}(c,c_2)
    }}
    \times 
    \left( 
      \mathbf{X}(c_1) \times \mathbf{X}(c_2)
    \right)
    \\
    & \simeq
    \int^{c_1 \in \mathcal{C}}
    \int^{c_2 \in \mathcal{C}}
    \mathcal{C}(c,c_1 \times c_2)
    \times 
       \mathbf{X}(c_1) \times \mathbf{X}(c_2)
    \,,
  \end{aligned}
$$

where the first step expands out both presheaves as colimits of representables separately, via the [[co-Yoneda lemma]] (Prop. \ref{TopologicalCoYonedaLemma}), the second step uses that the [[Cartesian product]] of presheaves is a two-variable [[left adjoint]] (by the [[symmetric monoidal category|symmetric]] [[closed monoidal structure on presheaves]]) and [[adjoints preserve (co-)limits|as such preserves colimits]] (in particular [[coends]]) in each [[variable]] separately (Prop. \ref{AdjointsPreserveCoLimits}), and under the brace we use the defining [[universal property]] of the [[Cartesian products]], assumed to exist in $\mathcal{C}$.

With this, we have the following sequence of [[natural isomorphisms]]:

$$
  \begin{aligned}
    \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
    \left(
      \mathbf{X} \times \mathbf{Y}
    \right)
    & 
    \simeq 
    \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
    \int^{c_1,c_2 \in \mathcal{C}}
    y(c_1 \times c_2) \times \mathbf{X}(c_1) \times \mathbf{Y}(c_2)  
    \\
    & \simeq
    \int^{c_1,c_2 \in \mathcal{C}}
    \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
    \left(
      y(c_1 \times c_2) \times \mathbf{X}(c_1) \times \mathbf{Y}(c_2)  
    \right)
    \\
    & \simeq
    \int^{c_1,c_2 \in \mathcal{C}}
    \left(
      \underset{
        \simeq \ast
      }{
      \underbrace{
        \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
        y(c_1 \times c_2) 
      }}
    \right)
    \times \mathbf{X}(c_1) \times \mathbf{Y}(c_2)  
    \\
    & \simeq
    \int^{c_1,c_2 \in \mathcal{C}}
    \left( 
      \mathbf{X}(c_1) \times \mathbf{Y}(c_2)  
    \right)
    \\
    & \simeq
    \left(
      \int^{c_1\in \mathcal{C}}
      \mathbf{X}(c_1) 
    \right)
    \times 
    \left(
      \int^{c_2\in \mathcal{C}}
      \mathbf{Y}(c_2)  
    \right)
    \\
    & \simeq
    \left(
      \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
      \mathbf{X}
    \right)
    \times
    \left(
      \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
      \mathbf{Y}
    \right)
  \end{aligned}
$$

Here the first step is (eq:OnSiteWithProductsExpandProductOfPresheaves), the second uses that [[colimits commute with colimits]] (Prop. \ref{LimitsCommuteWithLimits}), the third uses again that the [[Cartesian product]] respects colimits in each variable separately, the fourth is by Lemma \ref{ColimitOfRepresentableIsSingleton}, the last step is again the respect for colimits of the Cartesian product in each variable separately.

=--



$\,$


## Basic notions of Topos theory
  {#BasicNotionsOfToposTheory}

We have explained in Remark \ref{PresaheavesAsGeneralizedSpaces} how [[presheaves]] on a [[category]] $\mathcal{C}$ may be thought of as _[[generalized spaces]] probe-able by the objects of $\mathcal{C}$_, and that two consistency conditions on this interpretation are provided by the [[Yoneda lemma]] (Prop. \ref{YonedaLemma}) and the resulting [[Yoneda embedding]] (Prop. \ref{YonedaEmbedding}). Here we turn to a third consistency condition that one will want to impose:

If the [[objects]] of $\mathcal{C}$ are thought of as [[spaces]] of sorts, then there is typically a concept of _locality_ in these spaces, reflected by a notion of what it means to _[[cover]]_ a given space by ("smaller") spaces (a _[[coverage]]_, Def. \ref{Coverage} below).

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

 
+-- {: .num_remark}
###### Remark
**Warning**

Most (if not all) introductions to [[sheaf theory]] insist on motivating the concept from the special case of sheaves on [[topological spaces]]. This is good motivation for what Grothendieck called "[[petit topos]]"-theory. The motivation above, instead, naturally leads to the "[[gros topos]]"-perspective, which is more useful for discussing the [[synthetic differential geometry|synthetic]] [[higher differential geometry|higher]] [[geometry of physics -- supergeometry|supergeometry]] of [[physics]]. In fact, this is the perspective of _[[functorial geometry]]_ that has been highlighted since [Grothendieck 65](functorial+geometry#Grothendieck65), but which has maybe remained underappreciated.

=--

$\,$

We now first introduce the [[sheaf]]-condition (Def. \ref{Sheaf}) below in its traditional form via "[[matching families]]" (Def. \ref{CompatibleElements} below). Then we show (Prop. \ref{CechGroupoidCoRepresents} below) how this is equivalently expressed in terms of _[[Cech groupoids]]_ (Example \ref{CechGroupoid} below). This second formulation is convenient for understanding and handling various constructions in ordinary [[topos theory]] (for instance the definition of [[cohesive sites]]) and it makes immediate the generalization to [[higher topos theory]].

$\,$

### Descent


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

+-- {: .num_example #DifferentiablyGoodOpenCoversOfSmoothManifolds}
###### Example
**(differentiably [[good open covers]] of [[smooth manifolds]])**

The [[category]] [[SmthMfd]] of [[smooth manifold]] (Example \ref{ExamplesOfConcreteCategories}) carries a [[coverage]] (Def. \ref{Coverage}), where for $X \in SmthMfd$ any [[smooth manifold]] of [[dimension]] $D \in \mathbb{N}$, its [[coverings]] are collections of [[smooth functions]] from the [[Cartesian space]] $\mathbb{R}^D$ to $X$ whose [[image]] is the inclusion of an [[open ball]].

Hence these are the usual _[[open covers]]_ of $X$, but with the extra condition that every pathch is [[diffeomorphism|diffeomorphic]] to a Cartesian space (hence to a smooth [[open ball]]).

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

(That this indeed satisfies the matching condition follows immediately bu the [[functor|functoriality]] of $\mathbf{Y}$.)

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
**([[sheaf]])**

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

The [[full subcategory]] (Def. \ref{FullyFaithfulFunctor}) of the [[category of presheaves]] over a given [[site]] $\mathcal{C}$, on those that are sheaves is the _[[category of sheaves]]_, denoted

$$
  Sh(\mathcal{C})
    \overset{\phantom{AAAA}}{\hookrightarrow}
  [\mathcal{c}^{op}, Set]
  \,.
$$

A [[category]] which is [[equivalence of categories|equivalent]] (Def. \ref{EquivalenceOfCategories}) to a [[category of sheaves]] is called a _[[sheaf topos]]_, or often just _[[topos]]_, for short.

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


(...)

+-- {: .num_defn #SheafToposAsSubtopos}
###### Definition

A [[sheaf topos]] is [[subtopos]] of [[presheaf topos]]

$$
  Sh(C)
    \stackrel{\overset{\overline{(-)}}{\leftarrow}}{\hookrightarrow}
  PSh(C)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Here the [[left adjoint]] $\overline{(-)}$, which is equivalently

* the [[inverse image]] of the [[geometric embedding]] [[geometric morphism]]

* the [[sheafification]] functor

is precisely such that for every [[covering]] $\{U_i \to U\}_{i \in I}$ in the [[site]] $C$ the [[sieve]] inclusion

$$
  S(\{U_i\}) \hookrightarrow U \;\;\;\; \in PSh(C)
$$

(a [[dense monomorphism]]) is sent to an [[isomorphism]].

Hence the sheaf topos is the left exact [[localization]] at the covering sieve inclusions.

=--

+-- {: .num_remark}
###### Remark

The [[presheaf topos]] $PSh(C)$ is the [[free cocompletion]] of the [[category]] $C$, hence the category obtained from $C$ by [[free construction|freely]] forming [[colimits]] of its objects.

In contrast, the [[localization]] $Sh(C) \hookrightarrow PSh(C)$ enforces _relations_ between these free colimits.

Therefore in total we may think of $Sh(C)$ as obtained by [[generators and relations]] from the [[site]] $C$:

* the objects of $C$ are the generators;

* the [[coverings]] of $C$ are the relations.

=--

Def. \ref{SheafToposAsSubtopos} is the "external" characterization of sheaf toposes.

More intrinsically we have _[[Giraud's theorem]]_:

+-- {: .num_theorem}
###### Theorem

A [[sheaf topos]] is equivalently a [[presentable category]] with

1. [[universal colimits]]

1. [[effective quotients]]

1. [[disjoint coproducts]]

=--

This characterization, or rather its refinement to [[(infinity,1)-categories of (infinity,1)-sheaves]], is crucial, below, for the discussion of [[principal bundles]] and their [[associated bundle|associated]] [[fiber bundles]].

For other general considerations we need rather that every [[sheaf topos]] is in particular an _[[elementary topos]]_

+-- {: .num_defn}
###### Definition

An [[elementary topos]] is

* a [[locally cartesian closed category]]

* with a [[subobject classifier]].

=--

The first of these says that the [[internal language]] is [[dependent type theory]] with [[dependent sum types]] and [[dependent product types]], the second says that it has a [[type of propositions]]. 

(...)


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


## Cohesive toposes
  {#Cohesive}

+-- {: .num_defn #CohesiveTopos}
###### Definition
**([[cohesive topos]])**

A [[sheaf topos]] $\mathbf{H}$ (Def. \ref{Sheaf}) is called a _[[cohesive topos]]_ if there is a [[adjoint quadruple|quadruple]] of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) to the [[category of sets]] (Example \ref{CategoryOfSets})

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

Then there is an [[adjoint quadruple]] of [[functors]] between the [[category of presheaves]] over $\mathcal{C}$ (Example \ref{CategoryOfPresheaves}), and the [[category of sets]] (Example \ref{CategoryOfSets})

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

From this it follows, by Example \ref{KanExtensionOfAdjointPairIsAdjointQuadruple}, that [[Kan extension]] produces an [[adjoint quadruple]] of functors between the [[category of presheaves]] $[\mathcal{C}^{op}, Set]$ and $[\ast, Set] \simeq Set$, as shown, where 

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

With Example \ref{SmoothFunctionOnSmoothSpace} it only remains to be shown that for each [[set]] $S$ the [[presheaves]] $Disc(S)$ and $coDisc(S)$ are indeed [[sheaves]].

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
**([[adjoint triple]] of [[modal operators]] on [[cohesive topos]])**

Given a [[cohesive topos]] (Def. \ref{CohesiveTopos}), its [[adjoint quadruple]] of functors to and from [[Set]]

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

induce, by [[composition]] of functors, an [[adjoint triple]] of [[endofunctors]]

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

and we refer to the corressponding [[modal objects]] (Def. \ref{ModalObjects}) as follows:

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

+-- {: .num_prop #QuasitoposOfConcreteObjects}
###### Proposition
**([[quasitopos]] of [[concrete objects]] in a [[cohesive topos]])**

For $\mathbf{H}$ a [[cohesive topos]] (Def. \ref{CohesiveTopos}), write

$$
  \mathbf{H}_{conc} 
  \overset{ \phantom{AAAA} }{\hookrightarrow}
  \mathbf{H}
$$

for its [[full subcategory]] (Def. \ref{FullyFaithfulFunctor}) of [[concrete objects]] (Def. \ref{CohesiveModalities}).

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
    \overset{\phantom{AAA}}{\longrightarrow}
    \\
    \overset{\phantom{AAA}}{\hookleftarrow}
  }
  Set
$$

=--

+-- {: .proof}
###### Proof

For the adjunction on the right, we just need to observe that for every [[set]] $S \in Set$, the [[codiscrete object]] $coDisc(S)$ is [[concrete object|concrete]], which is immediate by [[idempotent monad|idempotency]] of $\sharp$ (Prop. \ref{ModalOpIdempotent}) and the fact that every [[isomorphism]] is also a [[monomorphism]].

For the adjunction on the left we claim that the [[left adjoint]] $conc$, (to be called _[[concretification]]_), is given by sending each [[object]] to the [[image]] (Def. \ref{SheafToposEpiMonoFactorization}) of its $(\Gamma \dashv coDisc)$ [[adjunction unit]] $\eta^\sharp$:

$$
  conc \;\colon\; X \mapsto im(\eta^\sharp_X)
  \,.
$$

The the [[adjunction unit]] of $(conc \dashv \iota_{conc})$ is provided by the [[epimorphism]] in the [[(epi, mono) factorization system|epi/mono-factorization]], via Prop. \ref{SheafToposEpiMonoFactorization}:

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

To see this, it is sufficient, by Prop. \ref{CollectionOfUniversalArrowsEquivalentToAdjointFunctor}, to show that $\eta^{conc}$ is a [[universal morphism]] in the sense of Def. \ref{UniversalArrow}. Hence consider any morphism $f \;\colon\; X_1 \to X_2$ with $X_2 \in \mathbf{H}_{conc} \hookrightarrow \mathbf{H}$. Then we need to show that there is a unique diagonal morphism as below, that makes the following _top left triangle_ [[commuting diagram|commute]]:

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

It remains to see that the lift is unique with the property of making (just) the top left triangle commute. But this is equivalently the statement that the left morphism is an epimorphism, by Def. \ref{Monomorphism}.

=--

(...)

[[!redirects geometry of physics -- categories and toposes]]

