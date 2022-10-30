
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

A general abstract way of formalizing this is given in [Lurie, sections 1.1, 1.2](#Lurie). For historical reasons, the notion of _internal $(\infty,1)$-category_ there goes by the name _complete Segal space object_, in honor of the notion of a _[[complete Segal space]]_, which is an internal $(\infty,1)$-category in $\mathcal{C} = $ [[∞Grpd]].

There are a variety of [[model category]] structures that [[presentable (infinity,1)-category|present]] the $(\infty,1)$-category of all internal $(\infty,1)$-categories in a suitable $\mathcal{C}$, which typically go as models for _complete Segal space objects_. The soundness of these models is discussed below in _[Model category presentations](#ModelCategoryPresentations)_ ([Lurie, section 1.5](#Lurie)).


## Definition


### Groupoid objects in an $(\infty,1)$-category

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


+-- {: .num_defn #PreCategoryObject}
###### Definition

An **internal precategory** $X$ in $\mathcal{C}$ is a [[simplicial object in an (∞,1)-category]]

$$
  X : \Delta^{op} \to \mathcal{C}
$$

such that it satifies the _[[Segal condition]]_, hence such that for all $n \in \mathbb{N}$ $X$ exhibits $X([n])$ as the [[(∞,1)-limit]] / iterated [[(∞,1)-pullback]]

$$
  X([n]) \simeq X(\{0,1\}) \times_{X([0])} \cdots \times_{X[0]} X(\{n-1,n\})
  \,.
$$

Write $PreCat(\mathcal{C})$ for the $(\infty,1)$-category of internal pre-categories in $\mathcal{C}$, the [[full sub-(∞,1)-category]] of the [[simplicial objects]] on the internal precategories.

=--

This is called a _category object_ in ([Lurie, def. 1.1.1](#Lurie)).

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



+-- {: .num_defn #CategoryObject}
###### Definition

An **internal category** in $\mathcal{C}$ is an internal pre-category $X$, def. \ref{PreCategoryObject} such that its [[core]] $Core(X)$ is in the image of the inclusion $\mathcal{C} \hookrightarrow Grpd(\mathcal{C})$, prop. \ref{EmbeddingOfConstantGroupoidObjects}.

=--

This is called a _[[complete Segal space]] object_ in ([Lurie, def. 1.2.10](#Lurie)).

### Internal category in an $(\infty,1)$-category
 {#InAnInfinity1Category}

More generally, we have internal categories in a more general $(\infty,1)$-category $\mathcal{C}$ after equipping this with a notion of internal groupoids.

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

In the [[syntax]] of [[homotopy type theory]] the corresponding
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
