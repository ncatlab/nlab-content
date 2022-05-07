
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _[[(∞,1)-category]]_ may be formulated [[internalization|internally]] to any other $(\infty,1)$-category with sufficient properties (with a rich enough [[internal logic]]). 
This generalizes the notion of _[[internal category]]_ from [[category theory]] to [[(∞,1)-category theory]]. In fact, an internal category in an $(\infty,1)$-category is automatically, externally, itself an [[(∞,1)-category]].


A category internal to some given $(\infty,1)$-category $\mathcal{C}$ is a [[simplicial object in an (∞,1)-category]] $A : \Delta^{op} \to \mathcal{C}$ in $\mathcal{C}$, where the object in degree $k$ is to be thought of as "the object of $k$-tuples of composable morphisms" in $A$. This is formalized by requiring the canonical morphisms $A_k \to A_1 \times_{A_0} \cdots \times_{A_0} A_1$ (into the iterated [[(∞,1)-pullback]] over the [[source]] and [[target]] maps) to be an [[equivalence in an (∞,1)-category|equivalence in]] $\mathcal{C}$ (the "[[Segal category|Segal condition]]"). 

If $\mathcal{C}$ happens to be just a 1-category, then this already makes $A$ an [[internal category]]. Generally, however, $\mathcal{C}$ comes with its own notion of [[homotopy]], and one must ask in addition that the notion of [[equivalence in an (∞,1)-category|equivalence]] in $A$ is compatible with that in $\mathcal{C}$ (the "[[complete Segal space|completeness condition]]").

A general abstract way of formalizing this is given in [Lurie, sections 1.1, 1.2](#Lurie). For historical reasons, the notion of _internal $(\infty,1)$-category_ there goes by the name _complete Segal space object_, in honor of the notion of a _[[complete Segal space]]_ (due to [[Charles Rezk]] and in turn chosen in honor of the [[Segal conditions]] for ordinary categories), which is an internal $(\infty,1)$-category in $\mathcal{C} = $ [[∞Grpd]]. But more generally we can consider internal category in a more general [[(∞,1)-topos]], and these are [[(∞,2)-sheaves]] of [[(∞,1)-categories]]

There are a variety of [[model category]] structures that [[presentable (infinity,1)-category|present]] the $(\infty,1)$-category of all internal $(\infty,1)$-categories in a suitable $\mathcal{C}$, which typically go as models for _complete Segal space objects_. The soundness of these models is discussed below in _[Model category presentations](#ModelCategoryPresentations)_ ([Lurie, section 1.5](#Lurie)).

## Motivation and introduction
 {#MotivationAndIntroduction}

Before coming to the formal definitions below in _[Definition](#Definition)_, here are some words for the reader looking for introduction and orientation into the general problem of formulating categories internally in [[homotopy theory]].

Whatever exactly the right or desired nature of a _category internal to an $(\infty,1)$-category/[[homotopy theory]]_ is (and we will see that there are some subtleties to beware of and some variants to account for), the bare minimum must be that it consists of

1. a _collection_ $X_0$ of [[objects]] -- but we shouldn't say [[set]] of objects, of course, instead the generic terminology is: a _[[type]] of objects_ and so we should write

   $\vdash \; X_0 \colon Type$;

1. for each [[pair]] $x_0, x_1 \colon X_0$ of objects, an _$(x_0,x_1)$-[[dependent type]] of [[morphisms]]_ $X_1(x_0,x_1)$ "from $x_0$ to $x_1$,
  
   $x_0, x_1 \colon X_0 \;\vdash \; X_1(x_0, x_1)$.

(One might decide to collect these all together to a single type $X_1 \coloneqq \underset{x_0,x_1 \colon Type}{\sum} X_1(x_0,x_1)$, but the theory flows much more naturally if we do keep the dependency on the objects explicit.)

At this point one might be tempted to proceed in close analogy to traditional formulations in [[internal category]] theory in non-homotopic 1-[[category theory]] and consider an explicit [[composition]] [[function]]

$$
  x_0, x_1, x_2 \colon X_0 \;\vdash\; comp_{x_0,x_1,x_2} \colon X_1(x_0,x_1) \times X_1(x_1, x_2) \to X_1(x_0, x_2)
$$

to be thought of as taking a [[pair]] $(g,f)$ of composable morphisms to their composite morphism $g \circ f$, and demand that it satisfies [[associativity]] up to [[homotopy]]. This approach is explored below in the section _[H-category types](#HCategoryTypes)_, where it is also discussed that this is _not_ the correct notion of category objects internal to a homotopy-theoretic context. 

To get a hint for what the correct formulation should be, it is useful to turn this around and investigate which internal-homotopy-theory structure an _ordinary_ [[small category]] ([[internal category|internal to]] [[Set]]) gives rise to.

Namely, bare [[homotopy theory]] is about [[groupoids]] and then [[n-groupoids]] and [[∞-groupoids]], and so it should be relevant that a groupoid is itself a category and that, conversely, every category $C \in Cat(Set)$ already contains some "homotopy theory", namely its maximal groupoid, its _[[core]]_ $i_C \colon core(C) \to C$. This groupoid is "the [[homotopy theory]] of the [[objects]] of $C$" in the sense that is contains all the information about the objects and their [[equivalences]]. Therefore it is natural to regard this as the "type of objects" and declare $X_0 \coloneqq core(C)$, regarded as an object of objects in the ambient [[(∞,1)-category]] [[Grpd]] $\hookrightarrow$ [[∞Grpd]].

But once we take that perspective, it is clear what the type $X_1$ of morphisms should be: it should be the [[comma object]] of the core inclusion with itself: $X_1 \coloneqq (i_C/i_C)$. 

This exposition is further developed in _[Segal space -- construction from a category](#Segal%20space#ConstructionFromACategory)_. There it is discussed how proceeding this way, one finds from $C$ a homotopy-theoretic kind of [[nerve]] which is now not a [[simplicial object]] in [[Set]] anymore (a [[simplicial set]]) as the nerve in ordinary [[category theory]] is, but which is now a [[simplicial object in an (∞,1)-category]], namely in [[Grpd]] $\hookrightarrow$ [[∞Grpd]]. In degree $k \in \mathbb{N}$ it contains not the _set_ of sequences of composable morphisms, but the "space" of such sequences, which just as the "space" $X_0$ of objects knows all the [[homotopies]], namely all the [[equivalences]] between such sequences of composable morphisms.

One then recalls a basic fact of traditional [[category theory]]: a [[simplicial set]] is the [[nerve]] of a [[category]] precisely if it satisfies the [[Segal conditions]]: which say that it is built from certain iterated [[fiber products]] of the 1-[[simplices]] over the [[vertices]]. Accordingly, here one should expect that the simplicial groupoid $X_\bullet$ is built in degree $k$ by a $k$-fold [[homotopy fiber product]] of the space of 1-simplices over the space of vertices, and indeed one finds that it is. 

In traditional category theory a simplicial set is the nerve of a category if and only if it satisfies the [[Segal conditions]]. Does the converse already hold here? The above inspection shows that instead of the core inclusion $i_C \colon core(C) \to C$ we could have started with _any_ [[functor]] $i \colon K \to C$ and $X_n \coloneqq i^{/^n}$ would still defined a simplicial groupoid that satisfies the [[Segal conditions]]. So in homotopy theory the Segal conditions, which witness the fact that we formed a nerve by iterated [[homotopy fiber product]], need to be accompanied by one more condition which ensures that we are indeed forming the homotopy fiber product not of any map, but of the [[core]]-inclusion (this is often, but somewhat undescrptively, called the "[[complete Segal space|compleness]] condition", and more recently also called a [[univalence]] condition). 

Finally, the [[nerve]] of a category in fact contains lots of redundant information. It is [[coskeleton|2-coskeletal]] and hence in a precise sense already its [[skeleton|2-skeleton]] $X_2 \stackrel{\to}{\stackrel{\to}{\to}} X_1 \stackrel{\to}{\to} X_0$ contains all the relevant information. Therefore we may decide to write this out explicitly in terms of a further [[dependent type]] $X_2$ of [[compositions]]. This explicit 2-skeletal formulation of internal [[(1,1)-categories]] in [[homotopy theory]] is spelled out below in _[(1,1)-Category types](#1CategoryTypes)_.

But of course the point of category objects internal ot an $(\infty,1)$-category is to speak about structures of higher homotopical degree, hence about untruncated [[simplicial objects in an (∞,1)-category]] and the appropriate conditions on them to qualify as internal categories. The comprehensive discussion of this definition we turn to in _[Definition](#Definition)_.





## Definition
 {#Definition}

We define category objects internal to an [[(∞,1)-category]] $\mathcal{C}$ (and with respect to a choice of "inclusion of groupoids" $\mathbf{H}\hookrightarrow \mathcal{C}$) by a sequence of full ([[coreflective subcategory|co]])[[reflective sub-(∞,1)-categories]]

$$
  \mathbf{H}
   \hookrightarrow
  Cat_{\mathbf{H}}(\mathcal{C})
   \hookrightarrow
  PreCat_{\mathbf{H}}(\mathcal{C})
    \hookrightarrow 
  \mathcal{C}^{\Delta^{op}}
$$

of that of 

* [Simplicial objects in an (∞,1)-category](#SimplicialObjects).

The definition makes recourse to the notion of [[groupoid object in an (∞,1)-category]], and so we first review that in 

* [Groupoid objects in an (∞,1)-category](#GroupoidObjects).

Then we discuss the definition of 

* [Internal categories in an (∞,1)-topos](#CategoryObjectInTopos).

The canonical example here is the archtypical [[(∞,1)-topos]] $\mathbf{H} = $ [[∞Grpd]] of [[∞-groupoids]]: a category object internal to that is essentially what is also called a [[complete Segal space]]. But the definition works for any other [[(∞,1)-topos]], hence for general [[(∞,1)-categories of (∞,1)-sheaves]] (of [[∞-stacks]]).

More generally, given a [[full and faithful (∞,1)-functor|fully faithful inclusion]] $\mathbf{H} \hookrightarrow \mathcal{C}$ of an [[(∞,1)-topos]] into some other [[(∞,1)-category]], we can define 

* [Internal categories in an (∞,1)-category](#InAnInfinity1Category).

The archetypical example here is the case where again $\mathbf{H} =$ [[∞Grpd]] $=: (\infty,0)Cat$ and where then, by [[induction]] on $n$, the inclusion is $\infty Grpd \hookrightarrow (\infty,n)Cat$ that of $\infty$-groupoids into [[(∞,n)-categories]]. The resulting internal category objects are then externally essentially [[n-fold complete Segal spaces|(n+1)-fold complete Segal spaces]], hence $(\infty,n+1)$-categories.

But again, more generally, $\mathbf{H}$ can be an [[(∞,1)-category of (∞,1)-sheaves]] and $\mathcal{C}$ for instance an [[(∞,2)-topos]] of [[(∞,2)-sheaves]], yielding $(\infty,3)$-sheaves, and so on.

### Simplicial objects 
 {#SimplicialObjects}

Let $\mathcal{C}$ be an [[(∞,1)-category]]. We discuss in the following a sequence of [[reflective sub-(∞,1)-categories]] of that of [[simplicial objects in an (∞,1)-category]] $\mathcal{C}^{\Delta^{op}}$ in $\mathcal{C}$, see there for more details.

We frequently refer to the [[powering]] of a simplicial object $X_\bullet$ by a [[simplicial set]], into an object in $\mathcal{C}$, denoted $X(K)$. For details on this see at _[simplicial object in an (∞,1)-category -- Powering](simplicial+object+in+an+%28infinity%2C1%29-category#Powering)_ .


+-- {: .num_remark #RemarkNoNeedForLocalization}
###### Remark

It is noteworthy that category objects internal to $\mathcal{C}$, as defined below, will form a _full_ [[sub-(∞,1)-category]] of that of [[simplicial objects in an (∞,1)-category]]. In traditional theory of [[internal categories]]a major issue is that in general there are not enough [[internal functors]]: the full subcategory of internal [[graphs]] on the internal categories needs to be further [[localization|localized]], in general. But this turns out to be an artefact of the ambient category being an [[(n,1)-category]] for $n$ too low. 

For a discussion of how for plain [[internal categories]] (those that also externally are [[1-categories]]) the traditional localization becomes superfluous if the ambient context is a [[(2,1)-category]] (instead of just a [[1-category]]) see at [[2-topos]] the section _[In terms of internal categories](2-topos#InTermsOfInternalCategories)_. The following may be thought of as a generalization of that discussion. 

=--

### Pre-category objects
 {#PreCategoryInTopos}

Let $\mathcal{C}$ be an [[(∞,1)-category]] with [[finite limit|finite]] [[(∞,1)-limits]]


+-- {: .num_defn #PreCategoryObject}
###### Definition

An **internal precategory** $X$ in $\mathcal{C}$ is a [[simplicial object in an (∞,1)-category]]

$$
  X : \Delta^{op} \to \mathcal{C}
$$

such that it satifies the _[[Segal condition]]_, hence such that for all $n \in \mathbb{N}$, $X$ exhibits $X([n])$ as the [[(∞,1)-limit]] / iterated [[(∞,1)-pullback]]

$$
  X([n]) \simeq 
  \underbrace{
    X(\{0,1\}) \underset{X([0])}{\times} \cdots \underset{X[0]}{\times} X(\{n-1,n\})
  }_{n \; factors}
  \,.
$$

Write $PreCat(\mathcal{C})$ for the $(\infty,1)$-category of internal pre-categories in $\mathcal{C}$, the [[full sub-(∞,1)-category]] of the [[simplicial objects]] on the internal precategories.

=--

This is called a _category object_ in ([Lurie, def. 1.1.1](#Lurie)). Here we reserve that term for those objects that behave more like category objects should, which are the _[[complete Segal space]] objects_, below. 

+-- {: .num_remark }
###### Remark

By the discussion at _[Segal conditions -- In terms of sheaf conditions](Segal%20condition#InTermsOfSheafConditionForSimplicialObjects)_, this means that $PreCat(\mathcal{C})$ sits in an [[(∞,1)-pullback]] square in [[(∞,1)Cat]]

$$
  \array{
    PreCat(\mathcal{C}) &\hookrightarrow& \mathcal{C}^{\Delta^{op}}
    \\
    \downarrow && \downarrow
    \\
    Graphs(\mathcal{C})
    &\hookrightarrow&
    \mathcal{C}^{\Delta_0^{op}}
  }
  \,,
$$

where $\Delta_0^{op} \to \Delta$ is the [[wide subcategory]] of the [[simplex category]] on the injective maps that moreover send elementary edges to elementary edges (morphisms of linear [[graphs]]), and the bottom morphism is the functor that sends a [[graph]] object $X_1 \stackrel{\overset{\partial_1}{\to}}{\underset{\partial_0}{\to}} X_0$ to the object which in degree $n$ is $\underbrace{ X_1 \underset{X_0}{\times} \cdots \underset{X_0}{\times} X_1}_{n\; factors}$.

=--

+-- {: .num_remark #CompositionInPreCategory}
###### Remark

The [[Segal conditions]] imply that for $X_\bullet$ a pre-category object, there is a [[composition]] map

$$
  X_1 \times_{X_0} X_1
  \underoverset{\simeq}{(\partial_0, \partial_2)^{-1}}{\to}
  X_2
  \stackrel{\partial_1}{\to}
  X_1
$$

which satisfies [[associativity]] and the [[unit law]] up to higher [[coherence|coherent]] [[homotopy]]. A [[subobject in an (∞,1)-category]] $Y \hookrightarrow X_1$ on such that restricted along this inclusion this composition becomes invertible we call a subobject of equivalences.

=--


+-- {: .num_defn #Equivalences}
###### Definition

For $X_\bullet$ a pre-category object, def. \ref{PreCategoryObject}, write

$$
  Equiv(X_1) \hookrightarrow X_1
$$

for the maximal [[subobject in an (∞,1)-category]] of the object of 1-morphisms on those which are [[equivalences]] with respect to the [[composition]] of remark \ref{CompositionInPreCategory}.

=--

### Groupoid objects
 {#GroupoidObjects}

A _groupoid object_ is a pre-category object, def. \ref{PreCategoryObject} whose composition operation according to remark \ref{CompositionInPreCategory} is invertible. This is discussed in more detail at _[[groupoid object in an (∞,1)-category]]_. Here we briefly recall the 

* [Definition](#GroupoidObjectDefinition)

and then discuss the crucial property for the further developments here, which is the 

* [Coreflection of gropoid objects into pre-category objects](#CoreflectionOfGroupoidsIntoPrecategories).

#### Definition
 {#GroupoidObjectDefinition}

Let $\mathcal{C}$ be an [[(∞,1)-category]] with finite $(\infty,1)$-limits.

+-- {: .num_defn #GroupoidObject}
###### Definition

A _[[groupoid object in an (∞,1)-category|groupoid object]]_ in $\mathcal{C}$ is a [[simplicial object in an (∞,1)-category]] 

$$
  X : \Delta^{op} \to \mathcal{C}
$$ 

satisfying the following equivalent conditions

1. $X_\bullet$ satisfies the  _groupoidal [[Segal conditions]]_, meaning that for all $n \in \mathbb{N}$ and all partitions $[n] \simeq S \cup S'$  that share a single element $S \cap S' = \{s\}$, the [[(∞,1)-functor]] $X$ exhibits an [[(∞,1)-pullback]]

   $$
     X([n]) \simeq X(S) \times_{X(S \cap S')} X(S')
     \,;
   $$

1. $X_\bullet$ is a pre-category object, def. \ref{PreCategoryObject}, and the morphism 

   $$
     X(\Delta^2) \to X(\Lambda^2_0)
   $$

   is an [[equivalence in an (∞,1)-category|equivalence]] in $\mathcal{C}$.

Write $Grpd(\mathcal{C})$ for the [[(∞,1)-category]] of groupoid objects in $\mathcal{C}$, the [[full sub-(∞,1)-category]] of [[simplicial object in an (∞,1)-category|simplicial objects]] on the groupoid objects.

=--

The equivalence follows with [[HTT|HTT prop. 6.1.2.6]], see at _[groupoid object -- equivalent characterizations](groupoid+object+in+an+%28infinity%2C1%29-category#EquivalentCharacterizations)_.

+-- {: .num_remark }
###### Remark

For $\mathcal{C} = \infty Grpd$,
a _[[groupoid object in an (∞,1)-category|groupoid object]]_  $X$ in $\mathcal{C}$ is a pre-category object $X_\bullet \in PreCat(\mathcal{C}) \hookrightarrow \mathcal{C}^{\Delta^{op}}$, def. \ref{PreCategoryObject}, such that the full inclusion

$$
  Equiv(X_1) \hookrightarrow X_1
$$

is an [[equivalence in an (∞,1)-category]].

=--

+-- {: .num_remark}
###### Remark

We are to think of $X([0])$ as the _$\mathcal{C}-$[[object]] of [[objects]]_ of a groupoid internal to $\mathcal{C}$, and of $X([1])$ as its _$\mathcal{C}$-[[object]] of [[morphisms]]_. In terms of this the above condition says two things:

1. for $S \cup S'$ an order-preserving partition (meaning that for all $s \in S$, $s' \in S'$ we have $s \leq s'$) it says that  $X([n])$ may be identified with the _object of sequences of lenght $n$ of [[composition|composable]] [[morphisms]]_;

1. for $S \cup S'$ not order-preserving, it says that morphisms have [[inverses]]. For instance for the partition of $[2]$ given by $S = \{0,1\}$ and $S' = \{0,2\}$ the above says intuitively that [[diagrams]] in the internal groupoid of the form 

   $$
     \array{
        && b
        \\
        & \nearrow && \searrow
        \\
        a &&&& c
     }
   $$

   (an [[inner Kan fibration|inner]] [[horn]]) are equivalent to those of the form

   $$
     \array{
        && b
        \\
        & \nearrow && 
        \\
        a &&\to&& c
     }
   $$

   (an [[Kan fibration|outer]] [[horn]]).

   The equivalence defines and is defined by forming the [[inverse]] of the morphism $b \to c$.

=--

Accordingly, below a _category object_ is defined analogously, but demanding the above condition only for ordered decompositions.

There will be one additional condition on category objects ("completeness"). In order to see where this comes from, notice the following.

+-- {: .num_prop #EmbeddingOfConstantGroupoidObjects}
###### Proposition

There is a [[full and faithful (∞,1)-functor]]

$$
  const : \mathcal{C} \hookrightarrow Grpd(\mathcal{C})
$$

sending an [[object]] $X$ of $\mathcal{C}$ to the corresponding constant [[simplicial object]] $(const X) : [n] \mapsto X$.

If $\mathcal{C}$ has [[small (∞,1)-category|small]] [[(∞,1)-colimits]], then this is a [[reflective sub-(∞,1)-category|reflective embedding]], whose reflector 

$$
  \lim_\to : Grpd(\mathcal{C}) \to \mathcal{C}
$$

forms the [[(∞,1)-colimit]] in $\mathcal{C}$ over the simplicial diagram underlying a groupoid object.

=--

See ([Lurie, example 1.1.4](#Lurie)). 

#### Coreflection into pre-category objects
 {#CoreflectionOfGroupoidsIntoPrecategories}

In order to state the [[complete Segal space|completeness condition]] on a precategory object, def. \ref{PreCategoryObject}, we need to reflect, or rather _coreflect_, it onto its [[core]] groupoid object, 
def. \ref{GroupoidObject}.

We first consider this for the ambient [[(∞,1)-topos]] $\mathbf{H}$ being [[∞Grpd]], then we use that to deal with the general case.

+-- {: .num_defn #HomotopyCategoryOfPreCategoryObject}
###### Definition

For $X_\bullet \in \infty Grpd^{\Delta^{op}}$ a precategory object, def. \ref{PreCategoryObject}, its corresponding **[[H-category]]** is, up to [[equivalence of categories|equivalence]], the [[Ho(∞Grpd)]]-[[enriched category]] $h X_\bullet$ with

* the [[objects]] are the points of $X_0$ (more invariantly: the objects are any [[set]] of points in $X_0$ containing at least one point in each connected components);

* the [[homotopy type]] of morphisms for any pair $(x_0,x_1)$ of objects is that of the of the [[(∞,1)-pullback]]

  $$
    h X(x_0,X1) \coloneqq \{x_0\} \underset{X_0}{\times} X_1 \underset{X_0}{\times} \{x_1\}
    \in \infty Grpd \to Ho(\infty Grpd)
  $$

* the [[composition]] $comp_{x_0,x_1, x_2}$ is given by the morphism
  
  $$
    \begin{aligned}
      h X(x_0,x_1) \times h X(x_1, x_2) 
      & \simeq \{x_0\} \underset{X_0}{\times} \{x_1\} \underset{X_0}{\times} X_1 \underset{X_0}{\times} \{x_2\}
      \\
      & \to \{x_0\} \underset{X_0}{\times} X_1 \underset{X_0}{\times} X_1 \underset{X_0}{\times} \{x_2\}
      \\
      & \stackrel{\simeq}{\to}
       \{x_0\} \underset{X_0}{\times} X_2 \underset{X_0}{\times} \{x_1\}
      \\
      & \stackrel{\partial_1}{\to}
       \{x_0\} \underset{X_0}{\times} X_1 \underset{X_0}{\times} \{x_2\}      
      \\
      & = h X(x_0,x_2)
    \end{aligned}
    \,,
  $$

where the second map is an isomorphism in [[Ho(∞Grpd)]] which is the inverse of the [[equivalence]] in [[∞Grpd]] that exists by the [[Segal conditions]] assumed to be satisfied by $X_\bullet$.

=--

(In ([Lurie](#Lurie)) this is def. 1.1.6.)

+-- {: .num_defn #Equivalences}
###### Definition

For $X_\bullet \in \infty Grpd^{\Delta^{op}}$ a pre-category object, we say that a point $f \colon * \to X_1$ in the degree-1 object is an [[equivalence]] if it is an [[isomorphism]] in the category $h X$, def. \ref{HomotopyCategoryOfPreCategoryObject}. For $n \in \mathbb{N}$, $n \geq 1$, write

$$
  Equiv(X_n) \hookrightarrow X_n
$$

for the [[1-monomorphism]] that includes the full-sub-$\infty$-groupoid on the sequences of equivalences. Write furthermore

$$
  Core(X)_\bullet \in Grpd(\infty Grpd) \hookrightarrow \infty Grpd^{\Delta^{op}}
$$

for the [[simplicial object]] with

$$
  Core(X)_0 \coloneqq X_0
$$

and

$$
  Core(X)_n \coloneqq Equiv(X_n)
  \,.
$$

This is evidently a [[groupoid object in an (infinity,1)-category|groupoid object]], def. \ref{GroupoidObject}, called the **[[core]]** of the pre-category object $X_\bullet$.

=--

+-- {: .num_remark }
###### Remark

This is a more abstract formulation of what equivalently is [[presentable (infinity,1)-category|presented]] by the corresponding discussion for [[Segal spaces]] and [[complete Segal space]], see at _[complete Segal space -- Definition](http://ncatlab.org/nlab/show/complete+Segal+space#Definition)_.

=--


In order to state the completeness condition on pre-category objects that make them be genuine category objects, we need this [[core]]-construction exhibits groupoid objects as a [[coreflective sub-(∞,1)-category]] of pre-category objects.

+-- {: .num_prop #CoreOnPreCategoryObjects}
###### Proposition

Let $\mathbf{H}$ be an [[(∞,1)-topos]].
Every [[groupoid object in an (∞,1)-category|groupoid object in]] $\mathbf{H}$ is canonically an internal pre-category. 
Under this inclusion $i \colon Grpd(\mathbf{H}) \hookrightarrow PreCat(\mathbf{H})$ the groupoid objects form a [[coreflective sub-(∞,1)-category]] of that of pre-catgegory objects,

$$
  (i \dashv core)
  \colon
  Grpd(\mathbf{H})
  \stackrel{\hookrightarrow}{\underset{Core}{\leftarrow}}
  PreCat(\mathbf{H})
  \,.
$$

The coreflection is the _[[core]]_ operation that discards non-invertible morphisms.

=--

This is ([Lurie, prop. 1.1.14](#Lurie)).

+-- {: .proof}
###### Proof

With def. \ref{Equivalences} it is direct to establish the statement for the case that $\mathcal{C} \simeq $ [[∞Grpd]], ([Lurie, cor. 1.1.11](#Lurie)), for instance by using the standard theory of [[Segal spaces]]. From this it follows also for the case that $\mathbf{H} \simeq PSh_\infty(\mathcal{D})$ is an [[(∞,1)-category of (∞,1)-presheaves]] by arguing objectwise over objects in $\mathcal{D}$. 
In the general case, $\mathbf{H}$ is a [[reflective sub-(∞,1)-category]] of such, $\mathcal{C} \hookrightarrow PSh_\infty(\mathcal{D})$. It is then sufficient to show that the core operation on the presheaf $\infty$-toposes respects these inclusions, so that we have

$$
  \array{
    Grpd(\mathbf{H}) &\hookrightarrow& Grpd(PSh_\infty(\mathcal{D}))
    \\
    \downarrow \uparrow^{\mathrlap{Core}} && \downarrow \uparrow^{\mathrlap{Core}_{PSh}}
    \\
    PreCat(\mathbf{H}) &\hookrightarrow& PreCat(PSh_\infty(\mathcal{D}))
  }
  \,.
$$

This means that we need to show that if $X_\bullet$ is degreewise in $\mathbf{H} \hookrightarrow PSh_\infty(\mathcal{D})$ and is a pre-category object, then $Core_{PSh}(X_\bullet)$ is degreewise in $\mathbf{H}$. By the pre-category condition and since the refletive inclusion is [[right adjoint]] and hence preserves the fiber products, for this it is sufficient that $Core_{Psh}(X)_0$ and $Core_{PSh}(X)_1$ are in $\mathbf{H}$.  To complete the proof it is sufficient to show that the first of these is $X_0$ and (again since the inclusion preserves limits) the second is equivalent to the [powering](simplicial%20object%20in%20an%20%28infinity,1%29-category#Powering) $X(K)$, where

$$
  K \coloneqq \Delta^0 \coprod_{\Delta^{\{0,2\}}} \Delta^3 \coprod_{\Delta^{\{1,3\}}} \Delta^
  \;\;\;
  \in 
  sSet
$$

is the [[simplicial set]] obtained from the [[simplex|3-simplex]] by collapsing the $(0,2)$-edge and the $\{1,3\}$-edge. Write $K^0 \coloneqq \{1,2\} \hookrightarrow K$ for the image of the $(1,2)$-edge of $\Delta^3$. Schematically:

$$
  K =
  \left\{
    \array{
      1 &\stackrel{K^0}{\to}& 0
      \\
      \uparrow &\nearrow_{\mathrlap{id}}& \downarrow
      \\
      0 &\to& 1
    }
    \;\;\; \Rightarrow \;\;\;
    \array{
      1 &\stackrel{K^0}{\to}& 0
      \\
      \uparrow &\searrow^{\mathrlap{id}}& \downarrow
      \\
      0 &\to& 1
    }   
  \right\}
  \,.
$$

We claim generally that

1. for $X \in PreCat(\mathbf{H})$ the canonical morphism $Core(X)(K) \to X(K)$ is an equivalence;

1. for $Y \in Grpd(\mathbf{H})$ the canonical morphism $Y(K) \to Y(K^0)$ is an equivalence.

(This is ([Lurie, prop. 1.1.13](#Lurie)).)

Here

$$
  X(K) \simeq  X_0 \underset{X(\{0,2\})}{\times} X_3 \underset{X(\{1,3\})}{\times} X_0
$$

etc. By construction, $Core(X)(K) \to X(K)$ is fully faithful.  Hence to see that it is an equivalence, hence in addition essentially surjective, it is sufficient to observe that 

$$
  X(K)
  \simeq
  X_0 \underset{X_{\{0,1\}}}{\times} X_3 \underset{X_{\{1,3\}}}{\times} X_0
$$ 

is the space of those 3-simplices in $X_\bullet$ for which the $\{0,1\}$-edges is a weak inverse to the $\{2,3\}$-edge. 
Hence $Core(X)(K) \to X(K)$ is an equivalence. Moreover $K^0 \hookrightarrow K$ is a weak equivalence, and hence so is $Core(X)(K) \to Core(X)({K^0}) \simeq Core(X)_1$,
by [this proposition](simplicial+object+in+an+%28infinity%2C1%29-category#SlicingOverPoweringOfSimplicialObjects) at _[[simplicial object in an (∞,1)-category]]_.

=--

### Category objects


#### In an $(\infty,1)$-topos
 {#CategoryObjectInTopos}
 {#CompleteCategoryInTopos}

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. Then every object of $\mathbf{H}$ may already be thought of as being an [[groupoid object in an (∞,1)-category|internal groupoid]], which facilitates the definition of internal categories. This we discus here.  The more general case where the ambient $(\infty,1)$-category is not necessarily an [[(∞,1)-topos]] is discussed further [below](#InAnInfinity1Category).


+-- {: .num_defn #CategoryObject}
###### Definition

An **internal category** in an [[(∞,1)-topos]] $\mathbf{H}$ is an internal pre-category $X_\bullet \in \mathbf{H}^{\Delta^{op}}$, def. \ref{PreCategoryObject}, such that its [[core]] $Core(X)$ is in the image of the inclusion $const \colon \mathbf{H} \hookrightarrow Grpd(\mathbf{H})$ of prop. \ref{EmbeddingOfConstantGroupoidObjects}.

=--

This is called a _[[complete Segal space]] object_ in ([Lurie, def. 1.2.10](#Lurie)).

+-- {: .num_remark }
###### Remark

A groupoid object, def. \ref{GroupoidObject}, is always a pre-category object, but is a category object only and precisely if it is in the image of the constant inclusion $Const \colon \mathbf{H} \to Grpd(\mathbf{H})$.

In a sense these are the genuine groupoid objects, while the others are groupoid objects _equipped with an atlas_ (...).

=--



For internalizing in an $(\infty,1)$-category $\mathcal{C}$ which is not an [[(∞,1)-topos]], we need to specify what the constant groupoid objects in $\mathcal{C}$ are supposed to be. This is the topic of

* [Relative core -- Choice of groupoid objects](#ChoiceOfGroupoidObjects).

Once one has this, the definition of

* [Category objects](#CategoryObjectsInC)

works essentially as before in an $(\infty,1)$-topos. The key point is that the ambient [[(∞,1)-topos]] $\mathbf{H}$ serves itself naturally as the collection of groupoid objects inside its [[(∞,1)-category]] of inernal categories and so this yields a natural notion of

* [Iterated internalization -- Internal n-categories](#InternalnCategories).

Internal to the archetypical base $(\infty,1)$-topos [[∞Grpd]] these are, externally, the bare [[(∞,n)-categories]]. Internal to an [[(∞,1)-category of (∞,1)-sheaves]] over some [[(∞,1)-site]], these are the [[(∞,n)-sheaves|(∞,n+1)-sheaves]] on that site. More on this is in the 

* _[Examples](#Examples)_

below.



#### Relative core -- Choice of groupoid objects
 {#ChoiceOfGroupoidObjects}

The structure necessary to formulate the [[complete Segal space|completeness]] condition, which in an [[(∞,1)-topos]] is def. \ref{CategoryObject}, internal to a more general [[(∞,1)-category]] $\mathcal{C}$ is the following.

+-- {: .num_defn #ChoiceOfInternalGroupoids}
###### Definition

For $\mathcal{C}$ an [[presentable (∞,1)-category]], a **choice of internal groupoids** is a choice of [[full sub-(∞,1)-category]] inclusion $\mathbf{H} \hookrightarrow \mathcal{C}$ of an [[(∞,1)-topos]] $\mathbf{H}$ such that

* the inclusion is closed under small [[(∞,1)-limits]] and [[(∞,1)-colimits]], hence (by the [[adjoint (∞,1)-functor theorem]]) the inclusion is one of "[[discrete objects]]", given by an [[adjoint triple]]

  $$
    (\Pi \dashv Disc \dashv \Gamma)
    \colon
    \mathcal{C}
     \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{Disc}{\hookleftarrow}}{\underset{\Gamma}{\to}}}
    \mathbf{H}
    \,;
  $$

* [[base change]] $f^* : \mathbf{H}_{/X} \to \mathcal{C}_{/Y}$ along morphisms $f : Y \to X$ with $X \in \mathbf{H}$ preserves [[(∞,1)-colimits]];

* the [[codomain fibration]] of $\mathcal{C}$ is an [[(∞,2)-sheaf]] when restricted to $\mathbf{H}$: its [[(∞,1)-Grothendieck construction|classifying functor]] $\chi : \mathcal{C}^{op} \to $ [[(∞,1)Cat]] preserves [[(∞,1)-limits]] when restricted along $\mathbf{H} \hookrightarrow \mathcal{C}$ 

  (a _[[van Kampen colimit]]-condition_, see [there](van+Kampen+colimit#InHigherCategories) for more)

=--

This is the definition of "distributor" in ([Lurie, def. 1.2.1](#Lurie)), where we are making use of ([Lurie, remark 1.2.6](#Lurie)) which identifies $\mathbf{H}$ here as being necessarily an [[(∞,1)-topos]], by the [[Giraud theorem|(∞,1)-Giraud theorem]].

+-- {: .num_example }
###### Example

The identity $\mathbf{H} \simeq \mathcal{C}$ is a choice of internal groupoids in $\mathbf{H}$, by the [[Giraud theorem|(∞,1)-Giraud theorem]]. For this choice the following theory of category objects in $\mathcal{C}$ relative to $\mathbf{H}$ reduces to that of category objects in $\mathbf{H}$, as discussed [above](#CompleteCategoryInTopos).

=--

For the discussion of [[(∞,n)-categories]], the central property of such _choices of internal groupoids_, def. \ref{ChoiceOfInternalGroupoids} is that they behave well with forming internal categories, this is cor. \ref{InductiveChoicesOfInternalGroupoids} below.


This corresponds to ([Lurie, notation 1.2.9](#Lurie)).


#### In a general $(\infty,1)$-category
 {#CategoryObjectsInC}

In the following, let $\mathcal{C}$ be a [[presentable (∞,1)-category]] eqipped with a choice of internal groupoids $\mathbf{H} \hookrightarrow \mathcal{C}$, def. \ref{ChoiceOfInternalGroupoids}.

+-- {: .num_defn #PreCategoryObject}
###### Definition

An **internal precategory** $X$ in $\mathcal{C}$ relative to the choice of internal groupoids $\mathbf{H} \hookrightarrow \mathcal{C}$ is a [[simplicial object in an (∞,1)-category|simplicial object]]

$$
  X : \Delta^{op} \to \mathcal{C}
$$

such that 

1. for all $n \in \mathbb{N}$ the functor $X$ exhibits $X_n$ as the [[(∞,1)-limit]] / iterated [[(∞,1)-pullback]]

  $$
    X([n]) \simeq X(\{0,1\}) \times_{X([0])} \cdots \times_{X[0]} X(\{n-1,n\})
$$

1. such that the object of objects lies in the inclusion of $\mathbf{H}$

   $$X_0 \in \mathbf{H} \hookrightarrow \mathcal{C}\,.$$

Write $PreCat_{\mathbf{H}}(\mathcal{C})$ for the $(\infty,1)$-category of internal pre-categories in $\mathcal{C}$ relative to $\mathbf{H}$, the [[full sub-(∞,1)-category]] of the [[simplicial objects]] on the internal precategories.

=--

This is the definition of _Segal object_ in ([Lurie, def. 1.2.7](#Lurie)).

+-- {: .num_prop #HCore}
###### Proposition

The inclusion

$$
  Grpd(\mathbf{H}) \hookrightarrow PreCat(\mathbf{H}) \hookrightarrow
  PreCat_{\mathbf{H}}(\mathcal{C})
$$

has a [[right adjoint|right]] [[adjoint (∞,1)-functor]]

$$
  Core_{\mathbf{H}} : PreCat_{\mathbf{H}}(\mathcal{C}) \to Grpd(\mathbf{H})
  \,.
$$

=--

+-- {: .proof}
###### Proof

The left morphism has a right adjoint by prop. \ref{CoreOnPreCategoryObjects}.  The right adjoint of the right functor is implied by the first of the axioms on the choice of groupoids $Disc \colon \mathbf{H} \hookrightarrow \mathcal{C}$, by which $Disc$ has a right adjoint $\Gamma$ and is itself a right adjoint. This means that their prolongations to simplicial objects both preserve pre-category objects and hence induce an adjunction of pre-category objects. Moreover, since $Disc$ is in addition fully faithful, $\Gamma$ takes objects in the inclusion back to themselves, and hence this preserves also $(\mathbf{H}\hookrightarrow \mathcal{C})$-relative precategory objects.

=--


+-- {: .num_defn #HInternalCategory}
###### Definition

An internal pre-category $X_\bullet \mathcal{C}^{\Delta^{op}}$, def. \ref{PreCategoryObject}, is called an **internal category** if its $\mathbf{H}$-Core, def. \ref{HCore}, is an essentially constant groupoid object, hence if

$$
  Core_{\mathbf{H}}(A) \in \mathbf{H} \stackrel{const}{\hookrightarrow} Grpd(\mathbf{H})
  \,.
$$ 

Write

$$
  Cat_{\mathbf{H}}(\mathcal{C}) \hookrightarrow PreCat_{\mathbf{H}}(\mathcal{C})
$$

for the [[full sub-(∞,1)-category]] of internal precategories on the internal categories.

=--

This is ([Lurie, def. 1.2.10](#Lurie)).

+-- {: .num_prop }
###### Proposition

The inclusion of pre-category objects, def. \ref{HInternalCategory} into category objects is [[reflective sub-(infinity,1)-category|reflective]]

$$
  Cat_{\mathbf{H}}(\mathcal{C})
  \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}
  PreCat_{\mathbf{H}}(\mathcal{C})
  \,.
$$

=--

This is ([Lurie, remark 1.2.11](#Lurie)).

+-- {: .proof}
###### Proof

By prop. \ref{EmbeddingOfConstantGroupoidObjects} and by the first axiom in def. \ref{ChoiceOfInternalGroupoids}, we have a reflective inclusion 

$$
\mathbf{H} \stackrel{const}{\hookrightarrow} \mathbf{H}^{\Delta^{op}} \stackrel{Disc^{\Delta^{op}}}{\hookrightarrow} \mathcal{C}^{\Delta^{op}}
  \,.
$$ 

From this the [[right adjoint]] [[core]], prop. \ref{HCore}, induces the claimed inclusion by using the statement of _[reflective sub-(∞,1)-category -- Transport of reflective subategories](reflective+sub-%28infinity,1%29-category#TransportOfReflectiveSubcategories)_, which says that $Cat_{\mathbf{H}}(\mathcal{C}) \simeq Core^{-1}(\mathbf{H})(PreCat_{\mathbf{H}}(\mathcal{C}))$ is a reflective inclusion

$$
  \array{
    \mathbf{H} &\stackrel{const}{\hookrightarrow}& \mathcal{C}^{\Delta^{op}}
    \\
    {}^{\mathllap{Core}}\uparrow\downarrow^{\mathrlap{incl}}
    && 
    {}^{\mathllap{Core}}\uparrow\downarrow^{\mathrlap{incl}}
    \\
    Cat_{\mathbf{H}}(\mathcal{C})
    &\hookrightarrow&
    PreCat_{\mathbf{H}}(\mathcal{C})
  }
  \,.
$$

=--

In summary we have:

+-- {: .num_cor #ReflectiveInclusionOfCategoryObjectsIntoSimplicialObjects}
###### Corollary

In summary we have a reflective inclusion

$$ 
  Cat_{\mathbf{H}}
  \hookrightarrow
  PreCat_{\mathbf{H}}(\mathcal{C})
  \hookrightarrow
  \mathcal{C}^{\Delta^{op}}
  \,.
$$

=--


+-- {: .num_remark }
###### Remark

So far we have only ever used the first axiom in def. \ref{ChoiceOfInternalGroupoids}. We now describe the reflector $PreCat_{\mathbf{H}}(\mathcal{C}) \to Cat_{\mathbf{H}}(\mathcal{C})$ in more detail, and for that we use the other two axioms.

=--

The corresponding reflector is "Segal completion". We now describe this in more detail.


+-- {: .num_defn #CategoricalEquivalence}
###### Definition

For $X_\bullet, Y_\bullet \in PreCat_{\mathcal{H}}(\mathcal{C})$, a [[morphism]] $f_\bullet \colon X_\bullet \to Y_\bullet$ of pre-category objects (hence of the underlying [[simplicial object in an (infinity,1)-category|simplicial objects]]) is a **categorical equivalence** if

1. **[[essentially surjective functor|essential surjectivity]]** -- $\underset{\to}{\lim}(core(X_\bullet)) \to \underset{\to}{\lim} (core(Y_\bullet))$ is an [[equivalence in an (∞,1)-category|equivalence]] in $\mathbf{H}$;

1. **[[full and faithful functor|full faithfulness]]** -- the [[diagram]]

   $$   
     \array{
       X_1 &\stackrel{f_1}{\to}& Y_1
       \\
       \downarrow^{\mathrlap{(\partial_0,\partial_1)}} && \downarrow^{\mathrlap{(\partial_0,\partial_1)}}
       \\
       X_0 \times X_0 &\stackrel{(f_0,f_0)}{\to}& Y_0 \times Y_0
     }
   $$

   is an [[(∞,1)-pullback]] diagram in $\mathcal{C}$.


=--

+-- {: .num_prop }
###### Proposition

The inclusion $Cat_{\mathbf{H}}(\mathcal{C}) \hookrightarrow PreCat_{\mathbf{H}}(\mathcal{C})$ of def. \ref{HInternalCategory} is [[reflective sub-(∞,1)-category|reflective]]. The [[localization of an (∞,1)-category|reflector]]

$$
 L \colon PreCat_{\mathbf{H}}(\mathcal{C}) \to Cat_{\mathbf{H}}(\mathcal{C})
$$

inverts precisely the categorical equivalences, def. \ref{CategoricalEquivalence}.

=--

This is ([Lurie, theorem 1.2.13](#Lurie)).

+-- {: .num_remark }
###### Remark

In particular, by reflectivity, this means that a morphism $f_\bullet \colon X_\bullet \to Y_\bullet$ in $Cat_\mathbf{H}(\mathcal{C})$ is an equivalence (hence an equivalence in $\mathcal{C}^{\Delta^{op}}$) precisely if it is a categorical equivalence.

=--


#### Iterated internalization -- Internal $n$-categories
 {#InternalnCategories}

A central point of the formulation of internal category objects is that it can be iterated to yields categories objects internal to category objects ... internal to an $(\infty,1)$-topos.

+-- {: .num_prop }
###### Proposition

Let $\mathbf{H} \hookrightarrow \mathcal{C}$ be a choice of 
internal groupoids, def. \ref{ChoiceOfInternalGroupoids}. Then also the constant inclusion

$$
  \mathbf{H} \hookrightarrow Cat_{\mathbf{H}}(\mathcal{C})
$$

into the $(\infty,1)$-category of the corresponding category objects is a choice of internal groupoids.

=--

This is ([Lurie, prop.1.3.2](#Lurie)). 

+-- {: .proof}
###### Proof

We consider the first of the three axioms, that the inclusion preserves limits and colimits: The constant inclusion 

$$
  \mathbf{H} 
    \stackrel{const}{\to} 
  \mathbf{H}^{\Delta^{op}} 
    \stackrel{Disc^{\Delta^{op}}}{\to}
  \mathcal{C}^{\Delta^{op}}
$$ 

is [[full and faithful (∞,1)-functor|fully faithful]], since $\Delta^{op}$ is a contractible $(\infty,1)$-category . The first inclusion preserves limits and colimits since in presheaf categories these are computed objectwise, similarly for the second, using the condition that already $Disc \colon \mathbf{H} \to \mathcal{C}$ preserves limits and colimits. Moreover, this inclusion clearly factors through $Cat_{\mathbf{H}}(\mathcal{C}) \hookrightarrow \mathcal{C}^{\Delta^{op}}$, by def. \ref{HInternalCategory}, and since that is also fully faithful, also $\mathbf{H} \to Cat_{\mathbf{H}}(\mathcal{C})$ preserves limits and colimits.

=--

In particular therefore we have the following:

+-- {: .num_cor #InductiveChoicesOfInternalGroupoids}
###### Corollary

For $\mathbf{H}$ an [[(∞,1)-topos]], the canonical inclusion 

$$
  \mathbf{H} \stackrel{const}{\hookrightarrow} Grpd(\mathbf{H}) \hookrightarrow Cat(\mathbf{H})
$$

is a choice of internal groupoids in $Cat(\mathbf{H})$, in the sense of def. \ref{ChoiceOfInternalGroupoids}. Moreover, by [[induction]], each of the induced constant inclusions

$$
  \mathbf{H} \stackrel{const}{\hookrightarrow} Cat(Cat(\cdots (Cat(\mathbf{H}))))
$$

is a choice of internal groupoids.

=--

This is ([Lurie, corollary 1.3.4, variant 1.3.8](#Lurie)).

Therefore it makes sense to write:

+-- {: .num_defn #nCategoriesByRecursiveInternalization}
###### Definition

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. 
For $n = 0$ set

$$
  0 Cat(\mathbf{H}) \coloneqq \mathbf{H}
  \,.
$$ 

Then by [[induction]] on $n \in \mathbb{N}$ set 

$$
  (n+1)Cat(\mathbf{H}) \coloneqq Cat_{\mathbf{H}}(n Cat(\mathbf{H}))
  \,.
$$

We call $n Cat(\mathbf{H})$ the $(\infty,1)$-category of **[[(∞,n)-categories]]** in $\mathbf{H}$, or of **[[(∞,n)-sheaves|(∞,n+1)-sheaves]]** or (-**[[stacks]]) of $(\infty,n)$-categories** on (the [[(∞,1)-site]] of definition of) $\mathbf{H}$. 

=--

See also at _[[n-category object in an (∞,1)-category]]_.





### Enriched categories as internal categories

The 1-categorical notion of [[enriched category]] is similar to that of [[internal category]], a main difference being that an internal category has an _object of objects_ in the ambient category $\mathcal{C}$, whereas an enriched category has a [[set]]/[[class]] of objects. If, however, $\mathcal{C}$ is equipped with a notion of [[discrete objects]], thought of as the inclusion of sets into $\mathcal{C}$, then $\mathcal{C}$-enriched categories may be thought of as those categories internal to $\mathcal{C}$ such that their object of objects is discrete.

Accordingly, if for $\mathcal{C}$ a [[presentable (∞,1)-category]] equipped with a _choice of internal groupoids_ $\mathbf{H} \hookrightarrow \mathcal{C}$, def. \ref{ChoiceOfInternalGroupoids}, for $\mathbf{H} \simeq $ [[∞Grpd]], then an $A \in Cat_{\mathbf{H}}(\mathcal{C})$ by definition has a bare (external / [[discrete ∞-groupoid|discrete]]) $\infty$-groupoid "of objects". The underlying simplicial object is thus more like a [[Segal category]] object (though still different from that).

In ([Lurie, def. 1.3.3](#Lurie)) such an choice of internal groupoids $\infty Grpd \hookrightarrow \mathcal{C}$ is called an "absolute distributor".


+-- {: .num_prop}
###### Observation

For $\mathcal{C} = \mathbf{H}$ an [[(∞,1)-topos]] over [[∞Grpd]], the [[inverse image]] of its [[global section]] [[geometric morphism]] $\infty Grpd \to \mathbf{H}$ is a _choice of internal groupoids_, def. \ref{ChoiceOfInternalGroupoids}, precisely if $\mathbf{H}$ is [[locally ∞-connected (∞,1)-topos|locally]] and [[∞-connected (∞,1)-topos|globally ∞-connected]].


$$
  (\Pi \dashv \Disc \dashv \Gamma)
  :
  \mathbf{H}
   \stackrel{\stackrel{\Pi}{\to}}{\stackrel{\overset{Disc}{\hookleftarrow}}{\underset{\Gamma}{\to}}}
   \infty Grpd
$$

=--



## Properties

### Model category presentations
 {#ModelCategoryPresentations}

We discuss here [[presentable (infinity,1)-category|presentations]] of category objects internal to an $(\infty,1)$-category by [[model category]] theory methods.

+-- {: .num_prop }
###### Proposition

Let $C$ be a [[left proper model category|left proper]] [[combinatorial model category]] that [[presentable (∞,1)-category|presents]]  the [[(∞,1)-category]] $\mathcal{C}$ in that $\mathcal{C} \simeq C^\circ$.

Then the category $[\Delta^{op}, C]$ of [[simplicial objects]] in $C$ admits a [[left proper model category|left proper]] [[combinatorial model category]] structure characterized by the following properties:

1. it is a [[Bousfield localization of model categories|left Bousfield localization]] of the injective or projective or [[Reedy model structure|Reedy]] [[model structure on functors]] $[\Delta^{op}, C]_{proj/inj/Reedy}$;

1. an object $\Delta^{op} \to C$ is [[fibrant object|fibrant]] precisely if it is fibrant in $[\Delta^{op}, C]_{proj/inj/Reedy}$ and if the corresponding simplicial object $\Delta^{op}\to C^\circ$ in the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by $C$ is an internal category.

=--

This is stated as ([Lurie, prop. 1.5.4](#Lurie)).

+-- {: .proof}
###### Proof

By the discussion at [[model structure on functors]]. Either of $[\Delta^{op}, C]_{proj/inj/Reedy}$ is a [[presentable (∞,1)-category|presentation]] of $\mathcal{C}^{op}$; and moreover, by the discussion at [reflective sub-(∞,1)-category -- model category presentation](reflective+sub-%28infinity%2C1%29-category#ModelCategoryPresentation) the reflective inclusion $Cat_{\mathbf{H}}(\mathcal{C}) \hookrightarrow \mathcal{C}^{\Delta^{op}}$ of cor. \ref{ReflectiveInclusionOfCategoryObjectsIntoSimplicialObjects} is presented by the [[Bousfield localization of model categories|left Bousfield localization]] as claimed.

=--

+-- {: .num_example }
###### Example

For $C = sSet_{Quillen}$ the standard [[model structure on simplicial sets]], this gives in particular rise to the standard [[model structure for complete Segal spaces]].

=--

### Homotopy type theory formulation
 {#HomotopyTypeTheoryFormulation}

For $\mathbf{H}$ an [[(∞,1)-topos]], another way of saying that we have an internal category object in $\mathbf{H}$ should be to say that we formulate it in the [[internal language]] of $\mathbf{H}$, which is a [[homotopy type theory]]. (For more see at _[[internal category in homotopy type theory]]_.)

However, at the time of this writing little is known for how to speak of _non-finite_ [[diagrams]] fully internally. To appreciate the issue, notice that the "internal" formulation of categories by [[simplicial objects in an (∞,1)-category]] as [above](#Definition) is in fact not fully internal to the ambient $(\infty,1)$-category $\mathcal{C}$, but assumes that it is known what externally an [[(∞,1)-functor]] $\Delta^{op} \to \mathcal{C}$ is. When we speak in [[homotopy type theory]] this is not an option and we have to genuinely stick to internal reasoning.

Nevertheless, we can speak fully internally of $(n,1)$-categories for "low $n$" by making use of the following observations.

1. By the discussion at _[[semi-Segal space]]_ a category object should equivalently be a [[semi-category]] object $X_\bullet$: a [[semi-simplicial object]] satisfying the [[Segal conditions]], and which is unital in that $Eq(X_1) \hookrightarrow X_1 \stackrel{\partial_1}{\to} X_0$ is an equivalence.

   A similar formalization of 1-category objects in homotopy type theory has been presented and studied in some detail in ([AKS](#AKS)).

1. To finite (and "low") degree a [[semi-simplicial type]] may be given "by hand" as a sequence of [[dependent types]] like this:
  
   $$
     \begin{aligned}
       & \vdash\; X_0 \colon Type
       \\
       x_0,x_1 \colon X_0 \;& \vdash \; X_1(x_0,x_1) \colon Type
       \\
     x_0,x_1,x_2 \colon X_1; f_2 \colon X_1(x_0,x_1); f_1 \colon X_1(x_0,x_2); f_2 \colon X_1(x_0,x_1) \; 
       & \vdash \; X_2(f_0,f_1,f_2) \colon Type
       \\
       \vdots \; &\vdash\; \vdots
    \end{aligned}
   $$

   etc.  (Where in principle we can go on like this to any finite $n$; but it is open how to say this in one go for all $n$ at once.)

   Notice that in the [[model category|model]]-[[categorical semantics]] of [[dependent types]] in [[homotopy type theory]], such a structure interprets indeed (up to the given degree) as a [[Reedy model structure|Reedy]] [[fibrant object|fibrant]] [[semi-simplicial object]] as used in the standard model-category theoretic constructions of internal $\infty$-categories discussed [above](#ModelCategoryPresentations).

1. If $X_0$ is [[n-truncated]] ([[h-level]] $n+2$) so that we are dealing with an internal category that is externally an [[(n,1)-category]], then a complete semi-Segal object $X_\bullet$ should indeed already be determined by its [[simplicial skeleton]] $X_{0 \leq \bullet \leq n+2}$. 
Note however that requiring $X_0$ to be [[n-truncated]] is not sufficient since we also need that $X_1$, $X_2$, ... are truncated; see the remark below. 

So in conclusion an _$n$-truncated category type_ in [[homotopy type theory]] should be an $(n+2)$-skeleton of a [[semi-simplicial type]] $X_{0 \leq \bullet \leq 3}$ as above, such that

1. [[Segal condition]]: for each $2 \leq k \leq n$ the canonical function $X_n \to X_1 \times_{X_0} \cdots \times_{X_0} X_1$ into the $n$-fold [[homotopy pullback]] is an [[equivalence]];

1. [[univalence]]/unitality: the canonical function $Eq(X_1) \to X_1 \stackrel{\partial_1}{\to} X_0$ is an [[equivalence]].

1. truncation: for every $i$, $X_i$ is $(n-i)$-truncated (of [[h-level]] $n-i+2$).

This approach to [[(n,1)-categories]] is discussed in ([CapriottiKraus17](CapriottiKraus17)). There, the last condition is replaced by requiring $X_1$ to be $(n-1)$-truncated, which does imply that $X_i$ is $(n-i)$-truncated. One can in fact ask for the truncation property for a _single_ positive $i$, and it will imply the truncation property for all $i$. This is discussed in the conclusions of ([CapriottiKraus17](CapriottiKraus17)). However, it would be insufficient to only say that $X_0$ is $n$-truncated since this controls $Eq(X_1)$ but not $X_1$ itself.

We spell the above definition out in more detail below for

* $n = 0$ -- [(0,1)-Category types](#0CategoryTypes), choosing $i = 1$ for the truncation condition

* $n = 1$ -- [(1,1)-Category types](#1CategoryTypes), choosing $i = 2$.

+-- {: .num_remark }
###### Remark
**(homotopy coherence by dependent types)**

The formulation of [[simplicial objects in an (∞,1)-category]] in the [[internal language]] of [[homotopy type theory]] has to deal with the issue of formulating a simplicial "[[homotopy coherent diagram]]" in the internal language. One may think of the above formulation via [[semisimplicial object|semisimplicial]] [[dependent types]] as dealing with this by 

1. discarding the explicit discussion of the degeneracy maps (which are not homotopy-theoretically necessary anyway);

1. formulating [[simplicial identities]] _not_ as [[propositional equalities]] (i.e. as [[terms]] of some [[identity type]] $(\partial_j \circ\partial_i \simeq \partial_j \circ \partial_{i-1})$ which would need to be subjected to their own coherent identities) but in fact as typing [[judgements]]: the face maps are given directly by [[substitution]] of [[variables]] on which the types of cells [[dependent type|depend]].

This is how the above formulation implicitly deals with [[homotopy coherent diagram|homotopy coherence]]. Under [[categorical semantics]] this state of affairs translates into the statement that [[Reedy model structure|Reedy]] [[fibrant object|fibrant]] [[semisimplicial objects]] are already a good (fibrant+cofibrant) model for [[homotopy types]].

=--

#### H-Category types
 {#HCategoryTypes}

It may be instructive to begin by discussing a notion of [[internal category]] in [[homotopy theory]] which is _not_ an category object in an $(\infty,1)$-category and which does _not_ interpret as an [[(∞,1)-category]], but which serves to illustrate a subtlety in the correct definition. In fact, it is an internal formulation of the [[H-category]] that underlies in particular any genuine precategory object, by def. \ref{HomotopyCategoryOfPreCategoryObject} above.

Notice that historically one says that:

+-- {: .num_defn }
###### Definition

An **[[H-monoid]]** is a [[monoid object]] internal to the [[homotopy category]] [[Ho(∞Grpd)]]/[[Ho(Top)]]. 

=--

+-- {: .num_remark }
###### Remark

This means that an [[H-monoid]] is 

1. a [[homotopy type]] $X$;

1. equipped with a binary operation $\cdot \colon X \times X \to X$;

1. and equipped with a point $i \colon * \to X$

such that 

1. there [[existential quantifier|exists]] an [[associativity]] [[homotopy]]

   $$
     \left(\left(-\right) \cdot \left(\left(-\right) \cdot \left(-\right)\right)\right)
     \Rightarrow
     \left(\left(\left(-\right) \cdot \left(-\right)\right) \cdot \left(-\right)\right)
     \colon
     X \times X \times X \to X
   $$

1. there exists a [[unit law|unitality]] [[homotopy]]

   $$
     (i \cdot (-)) \to id \colon  X \to X
     \,.
   $$

The point here is that these homotopies are only required to exist, but are not specified and are not part of the data of an [[H-monoid]].

=--

One also speaks of an _[[H-group]]_ for an [[H-monoid]] for which the product operation similarly has [[inverses]] up to unspecified homotopies. 
Hence it makes sense to consider the following many-object version ("[[oidification]]") of this classical concept:

+-- {: .num_defn }
###### Definition

An **[[H-category]] type** $X$ is a 

1. a [[type]] $\vdash \; X_0  \colon $ [[Type]] 

1. a [[dependent type]] $x_0,x_1 \colon X_0 \;\vdash\; X_1(x_0,x_1) \colon Type$

1. a [[term]] $\vdash \; i \colon X_0$;

1. a [[function]] 

   $$
     x_0,x_1,x_2 \colon X_0 \;\vdash\; comp_{x_1,x_2,x_2} \colon X_1(x_0,x_1) \times X_1(x_1,x_2) \to X_1(x_0,x_2)
   $$

such that there is a [[term]] of [[identity type]]

$$
  x_0, x_1, x_2, x_3 \colon X_0 \;\vdash\; ( com_{x_0,x_2,x_3} \circ comp_{x_0,x_1,x_2} \simeq  comp_{x_0, x_1, x_2} \circ comp_{x_1,x_2,x_3})
$$

(hence, equivalently, a necessarily unique term of the [[proposition]] [[type]] [[inhabited type|isInhabited]](...) of this identity type ).

=--

The archetypical example of [[H-groups]] already illustrates the deficiency of this notion

+-- {: .num_example }
###### Example

For $ \colon * \to Y$ a pointed [[homotopy type]], its [[loop space]][[loop space object|object]] $\Omega_y Y$ is naturally equipped with the structure of an [[H-group]] by 

1. taking the unit $* \to \Omega_y Y$ to be the constant loop on $Y$;

1. taking the product to be given by any choice of concatenation of loops.

=--

The natural question arising then is: how are those [[H-groups]] characterized that arise as [[loop space objects]], this way? 

One observes that those that areise this way carry much more structure than just a composition and unit up to unspecified homotopy: we can instead make an explicit choice of such homotopies by choosing ways to reparameterize the interval and, crucially, any two such choices are themselves related by a choice of higher order homotopy, and so ever on. Such a structure is called a **strong homotopy monoid** structure with **strong homotopy associativity** (as opposed to just bare homotopy associativity as in an [[H-monoid]]). Later this was abbreviated to **[[A-∞ algebra|A-∞]]** structure.

The classical result by [[Jim Stasheff]] answered the question by saying that:

+-- {: .num_theorem }
###### Theorem

An [[H-group]] $(X, \cdot)$ arises as a [[loop space object]], $X \simeq \Omega Y$ precisely if its homotopy-monoidal structure may be lifted to an [[A-∞ algebra]] structure.

=--

The point of the following constructions is to take care of that additional _strong_ homotopy information.

#### $(0,1)$-Category types
 {#0CategoryTypes}

We spell out the [above](#HomotopyTypeTheoryFormulation) strategy for defining [[(n,1)-category]] types in [[homotopy type theory]] for the case of [[(0,1)-categories]].

> The following is experimental. 

A **$(0,1)$-category type** is 

1. a [[type]] $\vdash\; X_0 \colon Type$

1. a [[dependent type]] $x_0,x_1 \colon X_0 \; \vdash \; X_1(x_0,x_1) \colon Type$;

   we write

   $$
     X^{\partial \Delta^2} 
      \coloneqq
     \underset{x_0,x_1,x_2 \colon X_0}{\sum}
       X_1(x_1,x_2) \times X_1(x_0,x_2) \times X_1(x_0,x_1)
     \,;
   $$

1. a dependent type

   $$
     ((x_0,x_1,x_2), (f_0, f_1, f_2)) \colon X^{\partial \Delta^2}
     \;\vdash \;
     X_2(f_0,f_1,f_2) \colon Type
     \,;
   $$

such that 

1. **[[n-truncated|0-truncation]]** --  $X_0$ is [[0-truncated]]/is an [[h-set]] (although this is automatic and does not have to be required explicitly);

1. **[[coskeleton|1-coskeletalness]]** -- the function 
   
   $$
     p_1 
    \colon
     \underset{(x_0,x_1) \colon X_0 \times X_0 }{\sum} X_1(x_0,x_1)
     \to
     X_0 \times X_0
   $$

   is a [[1-monomorphism]];

1. **[[Segal condition]]** -- the function

   $$
     ( (f_{12},f_{02},f_{01}) \mapsto (f_{12},f_{01}) )
     \colon
     \underset{((x_0,x_1,x_2),(f_{12},f_{02},f_{01})) \colon X^{\partial \Delta^2}}{\sum}  
       X_2 
     \to 
     \underset{ (x_0,x_1,x_2) \colon X_0 }{\sum}
     X_1(x_0,x_1) \times X_1(x_1, x_2)
   $$

   is an [[equivalence in homotopy type theory|equivalence]];

1. **[[univalence|unitality]]** -- the function

   $$
     p_1
     \colon
     \underset{x \colon X_0}{\sum} X_1(x,x)
     \to
     X_0
   $$

   is an [[equivalence in homotopy type theory|equivalence]].

#### $(1,1)$-Category types
 {#1CategoryTypes}

We spell out the [above](#HomotopyTypeTheoryFormulation) strategy for defining [[(n,1)-category]] types in [[homotopy type theory]] for the case of [[(1,1)-categories]].


> The following is experimental. 

A **$(1,1)$-category type** is 

1. a [[type]] $\vdash\; X_0 \colon Type$

1. a [[dependent type]] $x_0,x_1 \colon X_0 \; \vdash \; X_1(x_0,x_1) \colon Type$;

   we write

   $$
     X^{\partial \Delta^2} 
      \coloneqq
     \underset{x_0,x_1,x_2 \colon X_0}{\sum}
       X_1(x_1,x_2) \times X_1(x_0,x_2) \times X_1(x_0,x_1)
     \,;
   $$

1. a dependent type

   $$
     ((x_0,x_1,x_2), (f_{12}, f_{02}, f_{01})) \colon X^{\partial \Delta^2}
     \;\vdash \;
     X_2(f_{12}, f_{02}, f_{01}) \colon Type
     \,;
   $$

   we write

   $$
     X^{\partial \Delta^3}
     \coloneqq
     \underset{(x_0,x_1,x_2,x_3,x_4 \colon X_1) }{\sum}
     \underset{ f_{i j} \colon X_1(x_i, x_j)}{\sum}
     X_2(f_{12},f_{02},f_{01})
     \times
     X_2(f_{23}, f_{13}, f_{12})
     \times
     \cdots
     \,,
   $$

1. a [[dependent type]]
 
   $$
     (\sigma_{123}, \sigma_{023}, \sigma_{013}, \sigma_{012}) \colon X^{\partial \Delta^3}
      \;\vdash\;
      X_3(\sigma_{123}, \sigma_{023}, \sigma_{013}, \sigma_{012})
      \colon 
       Type
   $$

such that 

1. **[[n-truncated|1-truncation]]** --  $X_0$ is [[1-truncated]]/is an [[h-groupoid]] (which again is automatic and could be omitted)

1. **[[coskeleton|2-coskeletalness]]** -- the function 
   
   $$
     p_1
     \colon
     \underset{(f_{12},f_{02}, f_{01}) \colon X^{\partial \Delta^2}}{\sum}
     X_2(f_{12},f_{02}, f_{01})
     \to 
     X^{\partial \Delta^2}
   $$

   is a [[1-monomorphism]];

1. **[[Segal condition]]** -- the functions 

   $$
     ( (f_{12},f_{02},f_{01}) \mapsto (f_{12},f_{01}) )
     \colon
     \underset{((x_0,x_1,x_2),(f_0,f_1,f_2)) \colon X^{\partial \Delta^2}}{\sum}  
       X_2 
     \to 
     \underset{ (x_0,x_1,x_2) \colon X_0 }{\sum}
     X_1(x_1,x_2) \times X_1(x_0, x_1)
   $$

   and

   $$
     ( (f_{i j}, \sigma_{i j k})  \mapsto (f_{01}, f_{12}, f_{23}) )
     \colon
     \underset{f_{i j} \colon X_1(x_i,x_j)}{\sum}
     \underset{\sigma_{i_0 i_1 i_2} \colon X_2(f_{i_1 i_2}, f_{i_0 i_2}, f_{i_0 i_1})}{\sum}
      X_3( \sigma_{\cdots}, \cdots )
     \to
     \underset{(x_0,x_1,x_2,x_3) \colon X_0}{\sum}
     X_1(x_0,x_1)
     \times
     X_1(x_1,x_2)
     \times
     X_1(x_2,x_3)
   $$

   are [[equivalence in homotopy type theory|equivalences]];

1. **[[univalence|unitality]]** --  the function

   $$
     (((x_0,x_1),f) \mapsto x_0)
     \colon
     \underset{x_0,x_1 \colon X_0}{\sum}
     X_1(x_0,x_1)_{\simeq}
     \to
     X_0
   $$

   is an [[equivalence in homotopy type theory|equivalence]].


 
## Examples
 {#Examples}

We discuss some examples and applications of the above notions. For more on examples internal to $\infty Grpd$ see also at _[Segal space -- examples](Segal+space#Examples)_.

### The relative contexts

+-- {: .num_prop}
###### Proposition

The canonical inclusion [[∞Grpd]] $\hookrightarrow$ [[(∞,1)Cat]] is a consistent "choice of groupoid objects"("distributor") in the sense of def. \ref{ChoiceOfGroupoidObjects}.

=--

This is ([Lurie, theorem 1.4.1](#Lurie)).

### Ordinary $(\infty,1)$-categories
 {#OrdinaryInfinityCategories}

+-- {: .num_prop #GrpdInCatIsChoiceOfGroupoidObjects}
###### Proposition


An ordinary [[(∞,1)-category]] is equivalently an internal category in the [[(∞,1)-topos]] $\mathcal{C} :=$ [[∞Grpd]]:

$$
  Cat_{(\infty,1)} \simeq Cat(\infty Grpd)
  \,.
$$

=--

This is ([Lurie, corollary 4.3.16](#Lurie)).

Internal to [[∞Grpd]]

* an internal pre-category is known as a _[[Segal space]]_;

* a [[connected]] internal pre-category is known as a _[[reduced Segal space]]_;

* an internal category is known as a _[[complete Segal space]]_.

The model category presentations for $Cat(\infty Grpd)$ discussed [above](#ModelCategoryPresentations) are given in this case by the _[[model structure for complete Segal spaces]]_.




### $(\infty,n)$-categories

By iterating the construction of category objects, one obtains 
[[n-category]] objects. Externally these are [[(∞,n)-categories]]. 

An [[∞-groupoid]] may be thought of as an [[(∞,0)-category]]. Write therefore

$$
  Cat_{(\infty,0)} := \infty Grpd
  \,.
$$

Then by the [above](#OrdinaryInfinityCategories) the [[(∞,1)-category of (∞,1)-categories]] is

$$
  Cat_{(\infty,1)} \simeq Cat(Cat_{(\infty,0)})
  \,.
$$

Now by prop. \ref{GrpdInCatIsChoiceOfGroupoidObjects} the inclusion $\infty Grpd \hookrightarrow Cat(\infty Grpd)$ is a consistent choice of groupoid objects, and so we can continue the internalization.

Then the $(\infty,1)$-category $Cat(\mathcal{C})$ of internal categories in $\mathcal{C}$ is, up to [[equivalence of (∞,1)-categories|equivalence]], the $(\infty,1)$-category of [[(∞,2)-categories]]

$$
  Cat(Cat(\infty Grpd))
  \simeq
  Cat(Cat(Cat_{(\infty,0)}))
  \simeq
  Cat(Cat_{(\infty,1)})
  \simeq
  Cat_{(\infty,2)}
  \,.
$$

This yields, with def. \ref{nCategoriesByRecursiveInternalization}, an inductive construction of [[(∞,n)Cat]], the [[(∞,1)-category]] of [[(∞,n)-categories]]

$$
  Cat(Cat(\cdots (Cat_{(\infty,0)})))
  \simeq
  Cat_{(\infty,n)}
  \,.
$$

The corresponding model category presentation is that of _[[n-fold complete Segal spaces]]_.

### The internal self-reflection / internal base $(\infty,1)$-topos
 {#InternalBaseTopos}

For $\mathbf{H}$ an [[(∞,1)-topos]] it should come canonically
equipped (for each choice of [[regular cardinal]] $\kappa$)
with an internal category object $\mathcal{Type} \in Cat(\mathbf{H})$,
which is the canonical internal [[base (∞,1)-topos]], classifying the
(relatively $\kappa$-compact part of) the 
[[codomain fibration]]-[[(∞,2)-sheaf]] on $\mathbf{H}$.

In the [[syntax]] of [[homotopy type theory]] as discussed [above](#HomotopyTypeTheoryFormulation) the corresponding
simplicial object should be

$$
  \array{
    \vdots &&  \vdots & \vdots
    \\
    \downarrow \downarrow \downarrow \downarrow
    \\
    \mathcal{Type}_2 & \coloneqq & [ (f,g,h) : \sum_{(A,B,C) : Type_\kappa \times Type_\kappa \times Type_\kappa} (A \to B)\times (B \to C) \times (A \to C)  & \dashv (g\circ f = h) : Type_\kappa ]
    \\
    \downarrow \downarrow \downarrow
    \\
    \mathcal{Type}_1 & \coloneqq & [ (A,B) : Type_{\kappa} & \vdash A \to B : Type_\kappa ]
    \\
    \downarrow  \downarrow
    \\
    \mathcal{Type}_0 & \coloneqq  & [ & \vdash Type_{\kappa} : Type_\lambda]
  }
  \,,
$$

where $\lambda \gt \kappa$ is another [[regular cardinal]] and where $Type_\kappa$ and $Type_\lambda$ are the corresponding [[object classifier in an (infinity,1)-topos|object classifiers]] of the $(\infty,1)$-topos $\mathbf{H}$;

and equipped with the evident degeneracy maps

$$
  A : Type \vdash s_0 A \to (A \to A)
$$

etc. In the [[categorical semantics]] in a [[type-theoretic model category]] this makes a fibrant and cofibrant [[Reedy model structure|Reedy diagram]], it manifestly satisfies the [[Segal conditions]], and it is precisely [[univalence]] in the type theory that makes this a _[[complete Segal space]]_ object. 

## Related concepts

* [[n-category object in an (infinity,1)-category]]

* [[internal category]], [[internal functor]]

* [[2-congruence]], [[(n,r)-congruence]]

* [[Segal space]], [[semi-Segal space]]

## References

### General

A general abstract formulation is in 

* [[Jacob Lurie]], _[[(∞,2)-Categories and the Goodwillie Calculus]]_ ([arXiv:0905.0462](http://arxiv.org/abs/0905.0462))
 {#Lurie}

The model given by complete Segal space objects is due to

* [[Charles Rezk]], _A model for the homotopy theory of homotopy theory_. Transactions of the American Mathematical Society 35 (2001), no. 3, 973-1007

and has since seen a multitude of further developments.

Influential but unpublished discussion of [[higher Segal spaces]] is due to [[Clark Barwick]].

A treatment of the [[Yoneda lemma]] for categories internal to an arbitrary [[(∞,1)-topos]] is in 

* Louis Martini, _Yoneda's lemma for internal higher categories_, ([arXiv:2103.17141](https://arxiv.org/abs/2103.17141))


### Formalization in homotopy type theory
 {#ReferencesFormalizationInHomotopyTypeTheory}

Formalizations of [[1-categories]] and [[(n,1)-categories]] internal to [[homotopy type theory]] (see _[[internal categories in homotopy type theory]]_) are discussed in 

* {#AKS} [[Benedikt Ahrens]], [[Chris Kapulkin]], [[Michael Shulman]], _Univalent categories and the Rezk completion_ ([arXiv:1303.0584](http://arxiv.org/abs/1303.0584))

* {#CapriottiKraus17} [[Paolo Capriotti]], [[Nicolai Kraus]], _Univalent Higher Categories via Complete Semi-Segal Types_ ([arXiv:1707.03693](https://arxiv.org/abs/1707.03693))

  

[[!redirects category object in an (∞,1)-category]]

[[!redirects category objects in an (∞,1)-category]]
[[!redirects category objects in (∞,1)-categories]]
[[!redirects category objects in an (infinity,1)-category]]
[[!redirects category objects in (infinity,1)-categories]]

[[!redirects category object in an (∞,1)-topos]]
[[!redirects category objects in an (∞,1)-topos]]
[[!redirects category object in an (infinity,1)-topos]]
[[!redirects category objects in an (infinity,1)-topos]]


[[!redirects internal (∞,1)-category]]
[[!redirects (infinity,1)-category object]]
[[!redirects (∞,1)-category object]]

[[!redirects internal (infinity,1)-categories]]
[[!redirects internal (∞,1)-categories]]
[[!redirects (infinity,1)-category objects]]
[[!redirects (∞,1)-category objects]]

[[!redirects complete Segal space object]]
[[!redirects complete Segal space objects]]

[[!redirects internal category in an (∞,1)-category]]
[[!redirects internal category in an (infinity,1)-category]]
[[!redirects internal categories in an (∞,1)-category]]
[[!redirects internal categories in an (infinity,1)-category]]


[[!redirects internal (infinity,1)-category]]

[[!redirects pre-category object in an (infinity,1)-category]]
[[!redirects pre-category object in an (∞,1)-category]]
[[!redirects pre-category objects in an (infinity,1)-category]]
[[!redirects pre-category objects in an (∞,1)-category]]
[[!redirects pre-category objects in (infinity,1)-categories]]
[[!redirects pre-category objects in (∞,1)-categories]]

[[!redirects precategory object in an (infinity,1)-category]]
[[!redirects precategory object in an (∞,1)-category]]
[[!redirects precategory objects in an (infinity,1)-category]]
[[!redirects precategory objects in an (∞,1)-category]]
[[!redirects precategory objects in (infinity,1)-categories]]
[[!redirects precategory objects in (∞,1)-categories]]

[[!redirects categories in an (∞,1)-category]]

