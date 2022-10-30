
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
This generalizes the notion of _[[internal category]]_ from [[category theory]] to [[(∞,1)-category theory]]. In fact, a _category object_ internal to an $(\infty,1)$-category is automatically, externally, an [[(∞,1)-category]].


Let $\mathcal{C}$ be an [[(∞,1)-category]].

A general abstract way of defining an $(\infty,1)$-category $A$ _internal to_ $\mathcal{C}$ -- also called a _$(\infty,1)$-category object_ in $\mathcal{C}$ is to say that this is a [[simplicial object]] $A : \Delta^{op} \to \mathcal{C}$. The condition that the object $A_k$ in degree $k \in \mathbb{N}$ is to be thought of as the _object of sequences of composable morphisms of length $k$_ of $A$ is formalized by asking the canonical morphisms $A_k \to A_1 \times_{A_0} \cdots \times_{A_0} A_1$ (into the iterated [[(∞,1)-pullback]] over the [[source]] and [[target]] maps) to be an [[equivalence in an (∞,1)-category|equivalence in]] $\mathcal{C}$. In fact, this is literally just the definition of an [[internal category]] but interpreted in the [[internal logic]] of the $(\infty,1)$-category $\mathcal{C}$. Accordingly one may just as well equivalently speak just of a category object_ in $\mathcal{C}$.

Indeed, the obvious strengthening of this definition to enforce invertibility of [[morphisms]] yields the notion of [[groupoid object in an (∞,1)-category]], which could also be called an _[[internal ∞-groupoid]]_.

Therefore, a further condition is necessary to ensure that the notion of [[homotopy]] in $\mathcal{C}$ is compatible with that in $A$ (this is caled the "completeness condition", see [below](#Completeness)).

A general abstract [[(∞,1)-category theory|(∞,1)-category theoretic]] way of formalizing this is given in [Lurie, sections 1.1, 1.2](#Lurie). For historical reasons, the notion of _internal $(\infty,1)$-category_ there goes by the name _complete Segal space object_, in honor of the notion of a _[[complete Segal space]]_, which may be thought of as perceiving an ordinary [[(∞,1)-category]] as an internal $(\infty,1)$-category in $\mathcal{C} = $ [[∞Grpd]].

There are a variety of [[model category]] structures that [[presentable (infinity,1)-category|present]] the $(\infty,1)$-category of all internal $(\infty,1)$-categories in a suitable $\mathcal{C}$, which typically go as models for _complete Segal space objects_. The soundness of these models is discussed below in _[Model category presentations](#ModelCategoryPresentations)_ ([Lurie, section 1.5](#Lurie)).


## Definition


### Groupoid objects in an $(\infty,1)$-category

Let $\mathcal{C}$ be an [[(∞,1)-category]].

+-- {: .num_defn #GroupoidObject}
###### Definition

A _[[groupoid object in an (∞,1)-category|groupoid object]]_ in $\mathcal{C}$ is a [[simplicial object]] 

$$
  X : \Delta^{op} \to \mathcal{C}
$$ 

such that for all $n \in \mathbb{N}$ and all partitions $[n] \simeq S \cup S'$  that share a single element $S \cap S' = \{s\}$, the [[(∞,1)-functor]] $X$ exhibits an [[(∞,1)-pullback]]

$$
  X([n]) \simeq X(S) \times_{X(S \cap S')} X(S')
  \,.
$$

Write $Grpd(\mathcal{C})$ for the [[(∞,1)-category]] of groupoid objects in $\mathcal{C}$, the [[full sub-(∞,1)-category]] of [[simplicial objects]] on the groupoid objects.

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

There will be one additional condition on category objects ("completeness"). In order to see where this comes, notice the following.

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



### Category objects in an $(\infty,1)$-topos
 {#CategoryObjectInTopos}

Let $\mathcal{C}$ be an [[(∞,1)-topos]].


+-- {: .num_defn #PreCategoryObject}
###### Definition

A **pre-category object** $X$ in $\mathcal{C}$ is a [[simplicial object]]

$$
  X : \Delta^{op} \to \mathcal{C}
$$

such that for all $n \in \mathbb{N}$ $X$ exhibits $X([n])$ as the [[(∞,1)-limit]] / iterated [[(∞,1)-pullback]]

$$
  X([n]) \simeq X(\{0,1\}) \times_{X([0])} \cdots \times_{X[0]} X(\{n-1,n\})
  \,.
$$

Write $PreCat(\mathcal{C})$ for the $(\infty,1)$-category of pre-category objects in $\mathcal{C}$, the [[full sub-(∞,1)-category]] of the [[simplicial objects]] on the pre-category objects.

=--

This is called a _category object_ in ([Lurie, def. 1.1.1](#Lurie)).

+-- {: .num_prop }
###### Proposition

Every [[groupoid object in an (∞,1)-category|groupoid object in]] $\mathcal{C}$ is canonically a pre-category object. 
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

A **category object** in $\mathcal{C}$ is a pre-category object $X$, def. \ref{PreCategoryObject} such that its [[core]] $Core(X)$ is in the image of the inclusion $\mathcal{C} \hookrightarrow Grpd(\mathcal{C})$, prop. \ref{EmbeddingOfConstantGroupoidObjects}.

=--

This is called a _complete Segal space object_ in ([Lurie, def. 1.2.10](#Lurie)).

### Category objects in an $(\infty,1)$-category

(...)

## Iterated internalization

We introduce some conditions on an ambient $(\infty,1)$-category $\mathcal{C}$
such that its $(\infty,1)$-category of internal $(\infty,1)$-categories is itself again a good context for internalization.


The following definition is the specialization of the notion termed _absolute distributor_ in [Lurie, def. 1.2.1, 1.3.3](#Lurie) to [[(∞,1)-toposes]].

+-- {: .num_defn #WellSuitedTopos}
###### Definition

Call an [[(∞,1)-topos]] $\mathbf{H}$ **well-suited for iterated internalization** if 
it is [[locally ∞-connected (∞,1)-topos|locally]] and [[∞-connected (∞,1)-topos|globally ∞-connected]],

=--

+-- {: .num_remark}
###### Remark

Spelled out, this definition says the following.

The first condition says that the [[global section]] [[geometric morphism]] $(Disc \dashv \Gamma)$ admits an extra [[left adjoint]] $\Pi$

$$
  (\Pi \dashv \Disc \dashv \Gamma)
  :
  \mathbf{H}
   \stackrel{\stackrel{\Pi}{\to}}{\stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}}}
   \infty Grpd
$$

and that the [[inverse image]] $Disc$ is [[full and faithful]]. The corresponding [[full sub-(∞,1)-category]] is called that of _[[discrete objects]]_.


=--

+-- {: .num_remark}
###### Remark

In the terminology of ([Lurie](#Lurie)) this is indeed equivalent to $Disc : \infty Grpd \to \mathbf{H}$ being an "absolute distributor". The formulation there corresponds to the formulation here as follows.

Item 1) and 3) of ([Lurie, def. 1.2.1](#Lurie)) are automatically satisfied by assumption that $\mathbf{H}$ is an [[(∞,1)-topos]]. With this, item 2) of ([Lurie, def. 1.2.1](#Lurie)) and item 1) of ([Lurie, def. 1.3.3](#Lurie)) precisely encode [[locally ∞-connected (∞,1)-topos|local]] and global [[∞-connected (∞,1)-topos|∞-connectedness]] (notice that by the [[adjoint (∞,1)-functor theorem]] for [[presentable (∞,1)-categories]] the condition that $Disc$ preserves [[(∞,1)-limits]] is equivalent to it having the further [[left adjoint]] $\Pi$).

Finally notice that the version of item 4) of ([Lurie, def. 1.2.1](#Lurie)) available at time of this writing has a typo: it is indeed $\mathbf{H}^{op} \to CAT_{(\infty,1)}$ that is supposed to preserve $\infty$-limits, not $\mathbf{H} \to CAT_{(\infty,1)}^{op}$. This is clear from comparing with the proof of the next statement there, which is ([Lurie, prop. 1.2.4](#Lurie)).

So this condition is that the [[(∞,1)-functor]] 

$$
  \chi_{cod} : \infty Grpd^{op} \to CAT_{(\infty,1)}
$$ 

to the [[universe enlargement|very large]] [[(∞,1)-category of (∞,1)-categories]] which 
[[(∞,1)-Grothendieck construction|classifies]] the [[codomain fibration]] $cod : \mathbf{H}^I \to \mathbf{H}$ 
restricted along $Disc$ to the [[discrete objects]], hence assigning to an [[∞-groupoid]] $S$ the [[over-(∞,1)-topos]]

$$
  \chi : S \mapsto \mathbf{H}_{/Disc(S)},
$$

satisfies [[descent]] with respect to the [[canonical topology]], hence that it preserves [[(∞,1)-limits]] (sends [[(∞,1)-colimits]] in [[∞Grpd]] to [[(∞,1)-limits]] in $\mathbf{H}$).

But over an [[(∞,1)-topos]] the [[codomain fibration]] is always a [[canonical topology|canonical]] [[(∞,2)-sheaf]] (see there).

=--


## Properties

### Localization

+-- {: .num_prop #CatIsReflectiveInSimpl}
###### Proposition

The inclusion of category objects into all [[simplicial objects]]

$$
  Cat(\mathcal{C}) \hookrightarrow \mathcal{C}^{\Delta^{op}}
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

1. an obect $\Delta^{op} \to C$ is [[fibrant object|fibrant]] precisely if it is fibrant in $[\Delta^{op}, C]_{proj/inj/Reedy}$ and if the corresponding simplicial object $\Delta^{op}\to C^\circ$ in the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by $C$ is a category object, def. \ref{CategoryObject}.

=--

This is stated as ([Lurie, prop. 1.5.4](#Lurie)).

+-- {: .proof}
###### Proof

By prop. \ref{CatIsReflectiveInSimpl} combined with ([[Higher Topos Theory|HTT, prop. A.3.7.8]]).

=--

## Examples

### Ordinary $(\infty,1)$-categories
 {#OrdinaryInfinityCategories}

An ordinary [[(∞,1)-category]] is equivalently a category object in the [[(∞,1)-topos]] $\mathcal{C} :=$ [[∞Grpd]]:

$$
  Cat_{(\infty,1)} \simeq Cat(\infty Grpd)
  \,.
$$

Internal to [[∞Grpd]]

* a pre-category object is known as a _[[Segal space]]_;

* a [[connected]] pre-category object is known as a _[[reduced Segal space]]_;

* a category object is known as a _[[complete Segal space]]_.

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

Then the $(\infty,1)$-category $Cat(\mathcal{C})$ of category objects in $\mathcal{C}$ is, up to [[equivalence of (∞,1)-categories|equivalence]], the $(\infty,1)$-category of [[(∞,2)-categories]]

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
