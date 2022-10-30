
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
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _[[(∞,1)-category]]_ may be formulated [[internalization|internal]] to any other $(\infty,1)$-category with sufficient properties (with a rich enough [[internal logic]]). 
This generalizes the notion of _[[internal category]]_ from [[category theory]] to [[(∞,1)-category theory]]. In fact, an internal category in an $(\infty,1)$-category is automatically, externally, itself an [[(∞,1)-category]].


A category internal to some given $(\infty,1)$-category $\mathcal{C}$ is a [[simplicial object in an (∞,1)-category]] $A : \Delta^{op} \to \mathcal{C}$ in $\mathcal{C}$, where the object in degree $k$ is to be thought of as "the object of $k$-tuples of composable morphisms" in $A$. This is formalized by requiring the canonical morphisms $A_k \to A_1 \times_{A_0} \cdots \times_{A_0} A_1$ (into the iterated [[(∞,1)-pullback]] over the [[source]] and [[target]] maps) to be an [[equivalence in an (∞,1)-category|equivalence in]] $\mathcal{C}$ (the "[[Segal category|Segal condition]]"). 

If $\mathcal{C}$ happens to be just a 1-category, then this already makes $A$ an [[internal category]]. Generally, however, $\mathcal{C}$ comes with its own notion of [[homotopy]], and one must ask in addition that the notion of [[equivalence in an (∞,1)-category|equivalence]] in $A$ is compatible with that in $\mathcal{C}$ (the "[[complete Segal space|completeness condition]]").

A general abstract way of formalizing this is given in [Lurie, sections 1.1, 1.2](#Lurie). For historical reasons, the notion of _internal $(\infty,1)$-category_ there goes by the name _complete Segal space object_, in honor of the notion of a _[[complete Segal space]]_ (due to [[Charles Rezk]] and in turn chose in honor of the [[Segal conditions]] for ordinary categories), which is an internal $(\infty,1)$-category in $\mathcal{C} = $ [[∞Grpd]].

There are a variety of [[model category]] structures that [[presentable (infinity,1)-category|present]] the $(\infty,1)$-category of all internal $(\infty,1)$-categories in a suitable $\mathcal{C}$, which typically go as models for _complete Segal space objects_. The soundness of these models is discussed below in _[Model category presentations](#ModelCategoryPresentations)_ ([Lurie, section 1.5](#Lurie)).


## Definition
 {#Definition}

The definition of category objects in an [[(∞,1)-category]] makes recourse to the notion of [[groupoid object in an (∞,1)-category]], and so we first review that in 

* [Groupoid objects in an (∞,1)-category](#GroupoidObjects).

Then we discuss the definition of 

* [Internal categories in an (∞,1)-topos](#CategoryObjectInTopos).

The canonical example here is the archtypical [[(∞,1)-topos]] $\mathbf{H} = $ [[∞Grpd]] of [[∞-groupoids]]: a category object internal to that is essentially what is also called a [[complete Segal space]]. But the definition works for any other [[(∞,1)-topos]], hence for general [[(∞,1)-categories of (∞,1)-sheaves]] (of [[∞-stacks]]).

More generally, given a [[full and faithful (∞,1)-functor|fully faithful inclusion]] $\mathbf{H} \hookrightarrow \mathcal{C}$ of an [[(∞,1)-topos]] into some other [[(∞,1)-category]], we can define 

* [Internal categories in an (∞,1)-category](#InAnInfinity1Category).

The archetypical example here is the case where again $\mathbf{H} =$ [[∞Grpd]] $=: (\infty,0)Cat$ and where then, by [[induction]] on $n$, the inclusion is $\infty Grpd \hookrightarrow (\infty,n)Cat$ that of $\infty$-groupoids into [[(∞,n)-categories]]. The resulting internal category objects are then externally essentially [[n-fold complete Segal spaces|(n+1)-fold complete Segal spaces]], hence $(\infty,n+1)$-categories.

But again, more generally, $\mathbf{H}$ can be an [[(∞,1)-category of (∞,1)-sheaves]] and $\mathcal{C}$ for instance an [[(∞,2)-topos]] of [[(∞,2)-sheaves]], yielding $(\infty,3)$-sheaves, and so on.

### Groupoid objects in an $(\infty,1)$-category
 {#GroupoidObjects}

Let $\mathcal{C}$ be an [[(∞,1)-category]].

+-- {: .num_defn #GroupoidObject}
###### Definition

A _[[groupoid object in an (∞,1)-category|groupoid object]]_ in $\mathcal{C}$ is a [[simplicial object in an (∞,1)-category]] 

$$
  X : \Delta^{op} \to \mathcal{C}
$$ 

that satisfies the groupoidal _[[Segal conditions]]_, meaning that for all $n \in \mathbb{N}$ and all partitions $[n] \simeq S \cup S'$  that share a single element $S \cap S' = \{s\}$, the [[(∞,1)-functor]] $X$ exhibits an [[(∞,1)-pullback]]

$$
  X([n]) \simeq X(S) \times_{X(S \cap S')} X(S')
  \,.
$$

Write $Grpd(\mathcal{C})$ for the [[(∞,1)-category]] of groupoid objects in $\mathcal{C}$, the [[full sub-(∞,1)-category]] of [[simplicial object in an (∞,1)-category|simplicial objects]] on the groupoid objects.

=--

+-- {: .num_remark}
###### Remark

We are to think of $X([0])$ as the _$\mathcal{C}-$[[object]] of [[objects]]_ of a groupoid internal to $\mathcal{C}$, and of $X([1])$ as its _$\mathcal{C}$-[[object]] of [[morphisms]]_. In terms of this the above condition says two things:

1. for $S \cup S'$ an order-preserving partition (meaning that for all $s \in S$, $s' \in S'$ we have $s \leq s'$) it says that  $X([n])$ may be identified with the _object of sequences of lenght $n$ of [[composition|composable]] [[morphisms]]_ ;

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



### Internal category in an $(\infty,1)$-topos
 {#CategoryObjectInTopos}

Let $\mathcal{C}$ be an [[(∞,1)-topos]]. Then every object of $\mathcal{C}$ may be thought of as an [[groupoid object in an (∞,1)-category|internal groupoid]], which facilitates the definition of internal categories. The general case is discussed [below](#InAnInfinity1Category).

#### Pre-category objects

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

This is called a _category object_ in ([Lurie, def. 1.1.1](#Lurie)).

+-- {: .num_remark }
###### Remark

By the discussion at [Segal conditions -- In terms of sheaf conditions](Segal%20condition#InTermsOfSheafConditionForSimplicialObjects), this means that $PreCat(\mathcal{C})$ sits in an [[(∞,1)-pullback]] square in [[(∞,1)Cat]]

$$
  \array{
    PreCat(\mathcal{C}) &\to& \mathcal{C}^{\Delta^{op}}
    \\
    \downarrow && \downarrow
    \\
    Graphs(\mathcal{C})
    &\hookrightarrow&
    \mathcal{D}^{\Delta_0^{op}}
  }
  \,,
$$

where $\Delta_0^{op} \to \Delta$ is the [[wide subcategory]] of the [[simplex category]] on the injective maps that send elementary edges to elementary edges, and the bottom morphism is the functor that sends a group object $X_1 \stackrel{\overset{\partial_1}{\to}}{\underset{\partial_0}{\to}} X_0$ to the object which in degree $n$ is $\underbrace{ X_1 \underset{X_0}{\times} \cdots \underset{X_0}{\times} X_1}_{n\; factors}$.

=--


+-- {: .num_defn #HomotopyCategoryOfPreCategoryObject}
###### Definition

For $X_\bullet \in \mathcal{C}$ a precategory object, def. \ref{PreCategoryObject}, its corresponding **[[H-category]]** is, up to [[equivalence of categories|equivalence]], the [[Ho(∞Grpd)]]-[[enriched category]] $h X_\bullet$ with

* the [[objects]] are the points of $X_0$;

* the [[homotopy type]] of morphisms for any pair $(x_0,x_1)$ of objects is that of

  $$
    h X(x_0,X1) \coloneqq \{x_0\} \underset{X_0}{\times} X_1 \underset{X_0}{\times} \{x_1\}
    \in \infty Grpd \to Ho(\infty Grpd)
  $$

* the [[composition]] is given by the morphism
  
  $$
    \begin{aligned}
      h X(x_0,x_1) \times h X(x_1, x_2) 
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

where the second map is an isomorphism that exists by the [[Segal conditions]].

=--

+-- {: .num_defn #Equivalences}
###### Definition

For $X_\bullet \in \mathcal{C}^{\Delta^{op}}$ a pre-category object, we say that a point $f \colon * \to X_1$ is an [[equivalence]] if it is an [[isomorphism]] in the category $h X$, def. \ref{HomotopyCategoryOfPreCategoryObject}. For $n \in \mathbb{N}$, $n \geq 1$, write

$$
  Equiv(X_n) \hookrightarrow X_n
$$

for the [[1-monomorphism]] that includes the full-sub-$\infty$-groupoid on the sequences of equivalences. Write furthermore

$$
  Core(X)_\bullet \in Grpd(\mathcal{C}) \hookrightarrow \mathcal{C}^{\Delta^{op}}
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

In order to state the completeness condition on pre-category objects that make them be genuine category objects, we need this [[core]]-construction exhibits groupoid objects as a [[coreflective sub-(∞,1)-category]] of pre-category objects.

#### Coreflection of groupoid objects in pre-category objects

+-- {: .num_prop }
###### Proposition

Every [[groupoid object in an (∞,1)-category|groupoid object in]] $\mathcal{C}$ is canonically an internal pre-category. 
Under this inclusion the groupoid objects form a [[coreflective sub-(∞,1)-category]] of that of pre-catgegory objects.

$$
  Grpd(\mathcal{C})
  \stackrel{\hookrightarrow}{\underset{Core}{\leftarrow}}
  PreCat(\mathcal{C})
  \,.
$$

The coreflection is the _[[core]]_ operation that discards non-invertible morphisms.

=--

This is ([Lurie, prop. 1.1.14](#Lurie)).

+-- {: .proof}
###### Proof

It is straightforward to establish the statement for the case that
$\mathcal{C} \simeq $ [[∞Grpd]]. ([Lurie, cor. 1.1.11](#Lurie)) From this it follows also for the case that $\mathcal{C} \simeq PSh_\infty(\mathcal{D})$ is an [[(∞,1)-category of (∞,1)-presheaves]]. 
In the general case, $\mathcal{C}$ is a [[reflective sub-(∞,1)-category]] of such, $\mathcal{C} \hookrightarrow PSh_\infty(\mathcal{D})$. It is then sufficient to show that the core operation on the presheaf $\infty$-toposes respects these inclusions, so that we have

$$
  \array{
    Grpd(\mathcal{C}) &\hookrightarrow& Grpd(PSh_\infty(\mathcal{D}))
    \\
    \downarrow \uparrow && \downarrow \uparrow^{\mathrlap{Core}}
    \\
    PreCat(\mathcal{C}) &\hookrightarrow& PreCat(PSh_\infty(\mathcal{D}))
  }
  \,.
$$

This means that we need to show that if $X_\bullet \in \mathcal{C} \hookrightarrow PSh_\infty(\mathcal{D})$ is a category object, then $Core_{PSh}(X_\bullet)$ is degreewise in $\mathcal{C}$. By the pre-category condition and since the refletive inclusion is [[right adjoint]] and hence preserves the fiber products, for this it is sufficient that $Core_{Psh}(X)_0$ and $Core_{PSh}(X)_1$ are in $\mathcal{C}$.  To complete the proof it is sufficient to show that the first of these is $X_0$ and (again since the inclusion preserves limits) the second is the [[powering]] $X^K$, where

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

1. for $X \in PreCat(\mathcal{C})$ the canonical morphism $Core(X)^K \to X^K$ is an equivalence;

1. for $Y \in Grpd(\mathcal{C})$ the canonical morphism $Y^K \to Y^{K^0}$ is an equivalence.

(This is ([Lurie, prop. 1.1.13](#Lurie)).)

Here

$$
  X^K \coloneqq  X_0 \underset{\{0,2\}}{\times} X_3 \underset{\{1,3\}}{\times} X_0
$$

etc. Heuristically it is clear, by the nature of $K$, that this picks all those 3-simplices in $X_\bullet$ for which the $\{0,1\}$-edges is a weak inverse to the $\{2,3\}$-edge. Formally this follows from [this proposition](simplicial+object+in+an+%28infinity%2C1%29-category#SlicingOverPoweringOfSimplicialObjects) at _[[simplicial object in an (∞,1)-category]]_. Hence $Core(X)^K \to X^K$ is an equivalence. Moreover $K^0 \hookrightarrow K$ is a weak equivalence, and hence so is $Core(X)^K \to Core(X)^{K^0} \simeq Core(X)_1$.


=--

#### Category objects

+-- {: .num_defn #CategoryObject}
###### Definition

An **internal category** in $\mathcal{C}$ is an internal pre-category $X$, def. \ref{PreCategoryObject}, such that its [[core]] $Core(X)$ is in the image of the inclusion $const \colon \mathcal{C} \hookrightarrow Grpd(\mathcal{C})$, prop. \ref{EmbeddingOfConstantGroupoidObjects}.

=--

This is called a _[[complete Segal space]] object_ in ([Lurie, def. 1.2.10](#Lurie)).

### Internal category in an $(\infty,1)$-category
 {#InAnInfinity1Category}

More generally, we have internal categories in a more general $(\infty,1)$-category $\mathcal{C}$ after equipping this with a notion of internal groupoids.

#### Relative core -- Choice of groupoid objects

+-- {: .num_defn #ChoiceOfInternalGroupoids}
###### Definition

For $\mathcal{C}$ an [[presentable (∞,1)-category]], a **choice of internal groupoids** is
a choice of presentable [[full sub-(∞,1)-category]] $\mathcal{X} \hookrightarrow \mathcal{C}$ such that

* the inclusion is closed under small [[(∞,1)-limits]] and [[(∞,1)-colimits]], hence (by the [[adjoint (∞,1)-functor theorem]]) the inclusion is one of "[[discrete objects]]"

  $$
    \mathcal{C}
     \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{Disc}{\hookleftarrow}}{\underset{\Gamma}{\to}}}
    \mathcal{X}
    \,;
  $$

* [[base change]] $f^* : \mathcal{X}_{/X} \to \mathcal{C}_{/Y}$ along morphisms $f : Y \to X$ with $X \in \mathcal{X}$ preserves [[(∞,1)-colimits]];

* the [[codomain fibration]] of $\mathcal{C}$ is an [[(∞,2)-sheaf]] when restricted to $\mathcal{X}$: its [[(∞,1)-Grothendieck construction|classifying functor]] $\chi : \mathcal{C}^{op} \to $ [[(∞,1)Cat]] preserves [[(∞,1)-limits]] when restricted along $\mathcal{X} \hookrightarrow \mathcal{C}$.

=--

This is the definition of "distributor" in ([Lurie, def. 1.2.1](#Lurie)).

+-- {: .num_prop }
###### Proposition

If $\mathcal{X} \simeq \mathcal{C}$ then $\mathcal{X}$ being a choice of internal groupoids is equivalent to $\mathcal{C}$ being an [[(∞,1)-topos]].

=--

This is ([Lurie, remark 1.2.2](#Lurie)).

+-- {: .proof}
###### Proof

By the [[Giraud theorem|(∞,1)-Giraud theorem]]. 

=--

#### Category objects


In the following, let $\mathcal{C}$ be a [[presentable (∞,1)-category]] eqipped with a choice of internal groupoids $\mathcal{X} \hookrightarrow \mathcal{C}$, def. \ref{ChoiceOfInternalGroupoids}.

+-- {: .num_defn #PreCategoryObject}
###### Definition

An **internal precategory** $X$ in $\mathcal{C}$ relative to the choice of internal groupoids $\mathcal{X} \hookrightarrow \mathcal{C}$ is a [[simplicial object]]

$$
  X : \Delta^{op} \to \mathcal{C}
$$

such that for all $n \in \mathbb{N}$ $X$ exhibits $X([n])$ as the [[(∞,1)-limit]] / iterated [[(∞,1)-pullback]]

$$
  X([n]) \simeq X(\{0,1\}) \times_{X([0])} \cdots \times_{X[0]} X(\{n-1,n\})
$$

_and_ such that 

* $X_0 \in \mathcal{X} \hookrightarrow \mathcal{C}$.

Write $PreCat_{\mathcal{X}}(\mathcal{C})$ for the $(\infty,1)$-category of internal pre-categories in $\mathcal{C}$ relative to $\mathcal{X}$, the [[full sub-(∞,1)-category]] of the [[simplicial objects]] on the internal precategories.

=--

This is the definition of _Segal object_ in ([Lurie, def. 1.2.7](#Lurie)).

+-- {: .num_prop }
###### Proposition

The inclusion

$$
  Grpd(\mathcal{X}) \hookrightarrow PreCat(\mathcal{X}) \hookrightarrow
  PreCat_{\mathcal{X}}(\mathcal{C})
$$

has a [[right adjoint|right]] [[adjoint (∞,1)-functor]]

$$
  Core_{\mathcal{X}} : PreCat_{\mathcal{X}}(\mathcal{C}) \to Grpd(\mathcal{X})
  \,.
$$

=--

This is ([Lurie, prop. 1.1.14](#Lurie)).

+-- {: .num_defn }
###### Definition

An internal pre-category $A$ in $\mathcal{C}$ is called an **internal category** if 

$$
  Core_{\mathcal{X}}(A) \in \mathcal{X} \hookrightarrow Grpd(\mathcal{X})
  \,.
$$ 

Write

$$
  Cat_{\mathcal{X}}(\mathcal{C}) \hookrightarrow PreCat_{\mathcal{X}}(\mathcal{C})
$$

for the [[full sub-(∞,1)-category]] of internal precategories on the internal categories.

=--

This is ([Lurie, def. 1.2.10](#Lurie)).


### Enriched categories as internal categories

The 1-categorical notion of [[enriched category]] is similar to that of [[internal category]], a main difference being that an internal category has an _object of objects_ in the ambient category $\mathcal{C}$, whereas an enriched category has a [[set]]/[[class]] of objects. If, however, $\mathcal{C}$ is equipped with a notion of [[discrete objects]], thought of as the inclusion of sets into $\mathcal{C}$, then $\mathcal{C}$-enriched categories may be thought of as those categories internal to $\mathcal{C}$ such that their object of objects is discrete.

Accordingly, if for $\mathcal{C}$ a [[presentable (∞,1)-category]] equipped with a _choice of internal groupoids_ $\mathcal{X} \hookrightarrow \mathcal{C}$, def. \ref{ChoiceOfInternalGroupoids}, for $\mathcal{X} \simeq $ [[∞Grpd]], then an $A \in Cat_{\mathcal{X}}(\mathcal{C})$ by definition has a bare (external / [[discrete ∞-groupoid|discrete]]) $\infty$-groupoid "of objects". The underlying simplicial object is thus more like a [[Segal category]] object (though still different from that).

In ([Lurie, def. 1.3.3](#Lurie)) such an choice of internal groupoids $\infty Grpd \hookrightarrow \mathcal{C}$ is called an "absolute distributor".


+-- {: .num_prop}
###### Observation

For $\mathcal{C} = \mathbf{H}$ an [[(∞,1)-topos]] over [[∞Grpd]], the [[inverse image]] of its [[global section]] [[geometric morphism]] $\infty Grpd \to \mathbf{H}$ is a _choice of internal groupoids_, def. \ref{ChoiceOfInternalGroupoids}, precisely if $\mathbf{H}$ is [[locally ∞-connected (∞,1)-topos|locally]] and [[∞-connected (∞,1)-topos|globally ∞-connected]].

=--

$$
  (\Pi \dashv \Disc \dashv \Gamma)
  :
  \mathbf{H}
   \stackrel{\stackrel{\Pi}{\to}}{\stackrel{\overset{Disc}{\hookleftarrow}}{\underset{\Gamma}{\to}}}
   \infty Grpd
$$

=--



## Properties

### Localization

+-- {: .num_prop #CatIsReflectiveInSimpl}
###### Proposition

The inclusion of internal categories into all [[simplicial objects]]

$$
  Cat_{\mathcal{X}}(\mathcal{C}) \hookrightarrow \mathcal{C}^{\Delta^{op}}
$$

is [[reflective sub-(∞,1)-category|reflective]].

=--

This is ([Lurie, remark 1.2.11](#Lurie)), based on ([[Higher Topos Theory|HTT, lemma 5.5.4.17]]).


### Model category presentations
 {#ModelCategoryPresentations}

We discuss here [[presentable (infinity,1)-category|presentations]] of category objects internal to an $(\infty,1)$-category by [[model category]] theory methods.

+-- {: .num_prop }
###### Proposition

Let $C$ be a [[left proper model category|left proper]] [[combinatorial model category]].

Then then category $[\Delta^{op}, C]$ of [[simplicial objects]] in $C$ admits a [[left proper model category|left proper]] [[combinatorial model category]] structure characterized by the following properties:

1. it is a [[Bousfield localization of model categories|left Bousfield localization]] of the injective or projective or [[Reedy model structure|Reedy]] [[model structure on functors]] $[\Delta^{op}, C]_{proj/inj/Reedy}$;

1. an object $\Delta^{op} \to C$ is [[fibrant object|fibrant]] precisely if it is fibrant in $[\Delta^{op}, C]_{proj/inj/Reedy}$ and if the corresponding simplicial object $\Delta^{op}\to C^\circ$ in the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by $C$ is an internal category.

=--

This is stated as ([Lurie, prop. 1.5.4](#Lurie)).

+-- {: .proof}
###### Proof

By prop. \ref{CatIsReflectiveInSimpl} combined with ([[Higher Topos Theory|HTT, prop. A.3.7.8]]).

=--

This gives in particular to the standard [[model structure for complete Segal spaces]].

### Homotopy type theory formulation
 {#HomotopyTypeTheoryFormulation}

For $\mathbf{H}$ an [[(∞,1)-topos]], another way of saying that we have an internal category object in $\mathbf{H}$ should be to say that we formulate it in the [[internal language]] of $\mathbf{H}$, which is a [[homotopy type theory]].

However, at the time of this writing little is known for how to speak of _non-finite_ [[diagrams]] fully internally. To appreciate the issue, notice that the "internal" formulation of categories by [[simplicial objects in an (∞,1)-category]] as [above](#Definition) is in fact not fully internal to the ambient $(\infty,1)$-category $\mathcal{C}$, but assumes that it is known what externally an [[(∞,1)-functor]] $\Delta^{op} \to \mathcal{C}$ is. When we speak in [[homotopy type theory]] this is not an option and we have to genuinely stick to internal reasoning.

Nevertheless, we can speak fully internally of $(\infty,n)$-categories for "low $n$" by making use of the following observations.

1. By the discussion at _[[semi-Segal space]]_ a category object should equivalently be a [[semi-category]] object $X_\bullet$: a [[semi-simplicial object]] satisfying the [[Segal conditions]], and which is unital in that $Eq(X_1) \hookrightarrow X_1 \stackrel{\partial_1}{\to} X_0$ is an equivalence.

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

So in conclusion an _$n$-truncated category type_ in [[homotopy type theory]] should be an $(n+2)$-skeleton of a [[semi-simplicial type]] $X_{0 \leq \bullet \leq 3}$ as above, such that

1. [[Segal condition]]: for each $2 \leq k \leq n$ the canonical function $X_n \to X_1 \times_{X_0} \cdots \times_{X_0} X_1$ into the $n$-fold [[homotopy pullback]] is an [[equivalence]];

1. [[univalence]]/unitality: the canonical function $Eq(X_1) \to X_1 \stackrel{\partial_1}{\to} X_0$ is an [[equivalence]].

1. $X_0$ is [[n-truncated]] (of [[h-level]] $n+2$).

We spell this out in more detail below for

* $n = 0$ -- [(0,1)-Category types](#0CategoryTypes)

* $n = 1$ -- [(1,1)-Category types](#1CategoryTypes).

+-- {: .num_remark }
###### Remark
**(homotopy coherence by dependent types)**

The formulation of [[simplicial objects in an (∞,1)-category]] in the [[internal language]] of [[homotopy type theory]] has to deal with the issue of formulating a simplicial "[[homotopy coherent diagram]]" in the internal language. One may think of the above formulation via [[semisimplicial object|semisimplicial]] [[dependent types]] as dealing with this by 

1. discarding the explicit discussion of the degeneracy maps (which are not homotopy-theoretically necessary anyway);

1. formulating [[simplicial identities]] _not_ as [[propositional equalities]] (i.e. as [[terms]] of some [[identity type]] $(\partial_j \circ\partial_i \simeq \partial_j \circ \partial_{i-1})$ which would need to be subjected to their own coherent identities) but in fact as typing [[judgements]]: the face maps are given directly by [[substitution]] of [[variables]] on which the types of cells [[dependent type|depend]].

This is how the above formulation implicitly deals with [[homotopy coherent diagram|homotopy coherence]]. Under [[categorical semantics]] this state of affairs translates into the statement that [[Reedy model structure|Reedy]] [[fibrant object|fibrant]] [[semisimplicial objects]] are already a good (fibrant+cofibrant) model for [[homotopy types]].

=--

#### H-Category types

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

1. **[[n-truncated|0-truncation]]** --  $X_0$ is [[0-truncated]]/is an [[h-set]]

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

*  a [[dependent type]]
 
   $$
     (\sigma_{123}, \sigma_{023}, \sigma_{013}, \sigma_{012}) \colon X^{\partial \Delta^3}
      \;\vdash\;
      X_3(\sigma_{123}, \sigma_{023}, \sigma_{013}, \sigma_{012})
      \colon 
       Type
   $$

such that 

1. **[[n-truncated|1-truncation]]** --  $X_1$ is [[1-truncated]]/is an [[h-groupoid]]

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

### Ordinary $(\infty,1)$-categories
 {#OrdinaryInfinityCategories}

An ordinary [[(∞,1)-category]] is equivalently an internal category in the [[(∞,1)-topos]] $\mathcal{C} :=$ [[∞Grpd]]:

$$
  Cat_{(\infty,1)} \simeq Cat(\infty Grpd)
  \,.
$$

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

This yields an inductive construction of [[(∞,n)Cat]], the [[(∞,1)-category]] of [[(∞,n)-categories]]

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

A general abstract formulation is in 

* [[Jacob Lurie]], _$(\infty,2)$-Categories and the Goodwillie calculus_ ([arXiv:0905.0462](http://arxiv.org/abs/0905.0462))
 {#Lurie}

The model given by complete Segal space objects is due to

* [[Charles Rezk]], _A model for the homotopy theory of homotopy theory_. Transactions of the American Mathematical Society 35 (2001), no. 3, 973-1007

and has since seen a multitude of further developments.

Influential but unpublished discussion of [[higher Segal spaces]] is due to [[Clark Barwick]].

[[!redirects category object in an (∞,1)-category]]

[[!redirects category objects in an (∞,1)-category]]
[[!redirects category objects in (∞,1)-categories]]
[[!redirects category objects in an (infinity,1)-category]]
[[!redirects category objects in (infinity,1)-categories]]


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
