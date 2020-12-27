
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Model category theory
+-- {: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+-- {: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

> This page means to give an introduction to the notion of _[[locally presentable category]]_, and its related notions in [[higher category theory]] and survey some fundamental properties.

> Expected background of the reader:

> * For the first section _[Basic idea in category theory](#BasicIdea)_ the reader is assumed to be familiar with basic notions of [[category theory]] such as _[[presheaves]]_ and _[[colimits]]_.

> * For the section _[Basic idea in model category theory](#BasicIdeaInModelCategoryTheory)_ the reader is assumed to be familiar with basic notions in [[model category|model category theory]] such as _[[cofibrantly generated model categories]]_ and _[[homotopy colimits]]_.

> * For the third section _[Basic idea in (∞,1)-category theory](#BasicIdeaInInfinityCategoryTheory)_ the reader is assumed to be familiar with basic concepts of [[(∞,1)-category|(∞,1)-category theory]] such as _[[(∞,1)-categories of (∞,1)-presheaves]]_ and _[[(∞,1)-colimits]]_.

# Contents
* table of contents
{: toc}

## Basic idea in category theory
 {#BasicIdea}

The general idea is that a _[[locally presentable category]]_ is a [[large category]] [[generators and relations|generated from]] small data: from [[small objects]] under [[small colimit]]. 

### Generation from generators

The notion of _[[locally presentable category]]_ is, at least roughly, an analogue for [[categories]] of the notion of a [[finitely generated module]].

+-- {: .num_example #FinitelyGeneratedAbelianGroup}
###### Example

An [[abelian group]] $A$ is called _[[finitely generated module|finitely generated]]_ if there is a [[finite set|finite]] [[subset]]

$$
  \iota \colon S \hookrightarrow U(A)
$$ 

of the underlying set $U(A)$ of $A$, such that every element of $A$ is a sum of such generating elements. 

=--

+-- {: .num_remark}
###### Remark

We always have the maximal such presentation where $S = U(A)$ is the whole underlying set and $\iota \colon F(U(A)) \to A$ is the [[counit of an adjunction|counit]] of the [[free-forgetful adjunction]]. But the presentation is all the more interesting/useful the _smaller_ $S$ is. 

=--

Now, the [[categorification]] of "commutative sum" is _[[colimit]]_. Hence let now $\mathcal{C}$ be a category with all [[small colimits]].

+-- {: .num_defn #GenerationOfCategoryFromSubcategoryUnderColimits}
###### Definition

We say a subclass $S \hookrightarrow Obj(\mathcal{C})$ of [[objects]] or equivalently the [[full subcategory]] $\mathcal{C}^0 \hookrightarrow \mathcal{C}$ on this subclass _generates_ $\mathcal{C}$ if every object in $\mathcal{C}$ is a [[colimit]] of objects in $\mathcal{C}^0$, hence the colimit over a [[diagram]] of the form

$$
  D \to \mathcal{C}^0 \hookrightarrow \mathcal{C}
  \,.
$$

=--

As before, such a presentation is all the more useful the "smaller" the generating data is. In order to grasp the various aspects of the notion of "smallness" in [[category theory]] we need to recall the notion of [[regular cardinal]].

### Small data

+-- {: .num_defn}
###### Definition

The [[cardinality]] $\kappa = {\vert S\vert}$ of a [[set]] $S$ is _[[regular cardinal|regular]]_ if every [[coproduct]]/[[disjoint union]] of sets of cardinality smaller than $\kappa$ and indexed by a set of cardinality smaller than $\kappa$ is itself of cardinality smaller than $\kappa$.

=--

+-- {: .num_example}
###### Example

The smallest [[regular cardinal]] is $\aleph_0 = {\vert \mathbb{N}\vert}$: every finite union of finite sets is itself a finite set. (See the entry on [[regular cardinal]]s for a discussion as to whether one might consider some finite cardinals as being `regular'.)

=--

We can now speak of objects that are "$\kappa$-small sums" using the notion of $\kappa$-[[filtered colimits]]:

+-- {: .num_defn}
###### Definition

For $\kappa$ a [[regular cardinal]], a $\kappa$-[[filtered category]] is one where every [[diagram]] of size $\lt \kappa$ has a [[cocone]].

=--

+-- {: .num_example}
###### Example

In an $\aleph_0$-[[filtered category]] every finite diagram has a cocone. This is equivalent to: 

1. for every pair of objects there is a third object such that both have a morphism to it;

1. for every pair of [[parallel morphisms]] there is a morphism out of their codomain such that the two composites are equal.

=--

+-- {: .num_example}
###### Example

The [[tower diagram]] category $(\mathbb{N}, \leq)$ 

$$
  X_0 \to X_1 \to X_2 \to \cdots
$$

is filtered.

=--

+-- {: .num_remark}
###### Remark

For $\lambda \gt \kappa$ a bigger [[regular cardinal]], every $\lambda$-[[filtered category]] is in particular also $\kappa$-filtered.

=--

Using this we have the central definition now:

+-- {: .num_defn}
###### Definition

A $\kappa$-[[filtered colimit]] is a [[colimit]] over a $\kappa$-filtered diagram.

=--

A crucial characterizing property of $\kappa$-filtered colimits is the following:

+-- {: .num_prop #FilteredColimitsAndFiniteLimits}
###### Proposition

A colimit in [[Set]] is $\kappa$-filtered precisely if it commutes with all $\kappa$-[[small limits]].

In particular a colimit in [[Set]] is filtered (meaning: $\aleph_0$-filtered) precisely if it commutes with all [[finite limits]].

=--

+-- {: .num_defn}
###### Definition

An [[object]] $A \in \mathcal{C}$ is a $\kappa$-[[compact object]] if it commutes with $\kappa$-filtered colimits, hence  if for $X \colon I \to \mathcal{C}$ any $\kappa$-[[filtered category|filtered]] [[diagram]], the canonical [[function]]

$$
  \underset{\to_i}{\lim} \mathcal{C}(A,X_i) \to \mathcal{C}(A, \underset{\to_i}{\lim} X_i)
$$

is a [[bijection]]. 

We say $X$ is a **[[small object]]** if it is $\kappa$-compact for _some_ [[regular cardinal]] $\kappa$.

=--

+-- {: .num_remark}
###### Remark

If $\lambda \gt \kappa$, then being $\lambda$-compact is a weaker condition than being $\kappa$-compact. 

=--

+-- {: .num_remark}
###### Remark


The object $A$ commutes with the colimit over $I$ precisely if every morphism $A \to \underset{\to_i}{\lim} X_i $ lifts to a morphism $A \to X_j$ into one of the $X_j$. Schematically, depicting specifically a [[sequential colimit]], this means that we have:

$$
  \array{
    \cdots&\to&X_{j-1} &\to& X_j &\to& X_{j+1} &\to& \cdots
    \\
    &&&{}^{\mathllap{\exists \hat f}}\nearrow&\downarrow & \swarrow
    \\
    &&A& \stackrel{f}{\to} & \underset{\to}{\lim} X_i
  }
  \,.
$$

Hence $A$ is "small enough" such that mapping it into the sum of all the $X_i$ it always entirely lands inside one of the $X_i$.

=--

+-- {: .num_remark}
###### Remark

There is a close relation between the notion of "compact" as in, on the one hand, _[[compact topological space]]_ and _[[compact topos]] _, and on the other as in _[[compact object]]_ as above. This is mediated by proposition \ref{FilteredColimitsAndFiniteLimits}. But the relation is a bit more subtle and takes a bit more discussion than we maybe want to get into here.


=--

### Locally presentable category: generated from colimits over small objects

Using this we can now say:

+-- {: .num_defn #LocallyPresentableCategory}
###### Definition

A [[locally small category]] $\mathcal{C}$ is a _[[locally presentable category]]_ if it has all small [[colimits]] and there is a [[small set]] $S \hookrightarrow Obj(\mathcal{C})$ of [[small objects]] such that this generates $\mathcal{C}$, by def. \ref{GenerationOfCategoryFromSubcategoryUnderColimits}.

=--

+-- {: .num_remark}
###### Remark

The adjective "locally" in "[[locally presentable category]]" is to indicate that the condition is all about the [[objects]], only. There is a different notion of "presented category".

=--

There are a bunch of equivalent reformulations of the notion of locally presentable category. One of the more important ones we again motivate first by analogy with presentable modules:

### Generation exhibited by epimorphism from a free object

+-- {: .num_example}
###### Example

If an [[abelian group]] $A$ is generated by a set $S \hookrightarrow U(A)$ as in example \ref{FinitelyGeneratedAbelianGroup}, this means equivalently that there is an [[epimorphism]]

$$
  L \colon F(S) \to A
$$

from the [[free abelian group]] $F(S)$ generated by $S$, hence the group obtained by forming [[formal linear combination|formal sums]] of elements in $S$. Here the epimorphism sends formal sums to actual sums in $A$:

$$
  L(\sum_k s_k) \coloneqq \sum_k \iota(s_k)
  \,.
$$

=--


+-- {: .num_remark}
###### Remark

The [[categorification]] of the notion _[[free abelian group]]_ is the notion of _[[free cocompletion]]_ of a category $\mathcal{C}^0$: the [[category of presheaves]] $PSh(\mathcal{C}^0)$. 

=--

Accordingly:

+-- {: .num_example}
###### Example

If a [[full subcategory]] $\iota \colon \mathcal{C}^0 \hookrightarrow \mathcal{C}$ generates $\mathcal{C}$ under colimits as in defn. \ref{GenerationOfCategoryFromSubcategoryUnderColimits}, then there is a [[functor]]

$$
  L \colon PSh(\mathcal{C}^0) \to \mathcal{C}
$$

which sends formal colimits to actual colimits in $\mathcal{C}$

$$
  L(\underset{\to_k}{\lim} s_k) \coloneqq \underset{\to_k}{\lim} \iota(s_k)
  \,.
$$

Here $L$ by construction preserves all colimits. 

=--

Therefore conversely, given a colimit-preserving functor $L \colon PSh(\mathcal{C}^0) \to \mathcal{C}$ we want to say that it _locally presents_ $\mathcal{C}$ if $L$ is "suitably epi".

It turns out that "suitably epi" is to be the following:

+-- {: .num_defn #Localization}
###### Definition

A [[functor]] $L \colon PSh(\mathcal{C}^0) \to \mathcal{C}$ from the [[category of presheaves]] over a [[small category]] $\mathcal{C}^0$ is an **[[accessible functor|accessible]] [[localization]]** if

*  $L$ has a [[section]], hence a [[functor]] $R \colon \mathcal{C} \to PSh(\mathcal{C}^0)$ with a [[natural isomorphism]] $L\circ R \simeq id_{\mathcal{C}}$;

* such that 

  1. $R$ is [[right adjoint]] to $L$;

  1. $R\circ L$ preserves $\kappa$-[[filtered colimits]].

=--

With this notion we have the following analog of the familiar statement that an abelian group is generated by $S$ precisely if there is an epimorphism $L \colon F(S) \to A$:

+-- {: .num_theorem #AdamekRosickyTheorem}
###### Theorem

A category $\mathcal{C}$ is locally presentable according to def. \ref{LocallyPresentableCategory} precisely if it is an accessible localization, def. \ref{Localization}, 

$$
  L \colon PSh(\mathcal{C}^0) \to \mathcal{C}
$$

for some small category $\mathcal{C}^0$. 


=--

This is due to ([Ad&#225;mek-Rosick&#253;, prop 1.46](#AdamekRosicky)).


### Left exact localizations


+-- {: .num_remark}
###### Remark

A [[locally presentable category]] $\mathcal{C}$ is called a _[[topos]]_, precisely if the localization functor $L \colon PSh(\mathcal{C}^0) \to \mathcal{C} $ from theorem \ref{AdamekRosickyTheorem} in addition is a [[left exact functor]], meaning that it preserves [[finite limits]].

=--

## Summary and overview {#summary}

In summary the discussion [above](#BasicIdea) says that the notion of locally presentable categories sits in a sequence of notions as indicated in the row labeled "category theory" in the following table. The other rows are supposed to indicate that regarding a category as a [[(1,1)-category]] and simply varying in this story the parameters $(n,r)$ in "[[(n,r)-category]]" one obtains fairly straightforward analogs of the notion of locally presentable category in other fragments of [[higher category theory]]. These we discuss in more detail further below.

**Locally presentable categories:** [[large categories|Large categories]] whose [[objects]] arise from [[small object|small]] [[generators]] under [[small colimit|small]] [[relations]].

| [[(n,r)-categories]] ... | satisfying [[Giraud's axioms]] | inclusion of [[left exact functor|left exact]] [[localizations]] | [[generators and relations|generated]] under [[colimits]] from [[small objects]] | | [[localization]] of [[free cocompletion]] | | [[generators and relations|generated]] under [[filtered colimits]] from [[small objects]] |
| - | - | - | - | - | - | - | - |
| **[[(0,1)-category theory]]** | [[(0,1)-toposes]] | $\hookrightarrow$ | [[algebraic lattices]] | $\simeq$ [Porst's theorem](algebraic+lattice#RelationToLocallyFinitelyPresentableCategories) | [[subobject lattices]] in [[accessible functor|accessible]] [[reflective subcategories]] of [[presheaf categories]] | | |
| **[[category theory]]** | [[toposes]] | $\hookrightarrow$ | [[locally presentable categories]] | $\simeq$ [Ad&#225;mek-Rosick&#253;'s theorem](#AdamekRosickyTheorem) | [[accessible functor|accessible]] [[reflective subcategories]] of [[presheaf categories]] | $\hookrightarrow$ | [[accessible categories]] |
| **[[model category|model category theory]]** | [[model toposes]] | $\hookrightarrow$ | [[combinatorial model categories]] | $\simeq$ [Dugger's theorem](#DuggerTheorem) | [[left Bousfield localization]] of global [[model structures on simplicial presheaves]] | | |
| **[[(∞,1)-topos theory]]** | [[(∞,1)-toposes]] |$\hookrightarrow$ | [[locally presentable (∞,1)-categories]] | $\simeq$ <br/> [Simpson's theorem](#SimpsonTheorem) | [[accessible (∞,1)-functor|accessible]] [[reflective sub-(∞,1)-categories]] of [[(∞,1)-presheaf (∞,1)-categories]] | $\hookrightarrow$ |[[accessible (∞,1)-categories]] |

## Basic idea in model category theory
 {#BasicIdeaInModelCategoryTheory}

### Model structure on simplicial presheaves


The analog of a [[category of presheaves]] in [[model category]] theory is the [[model structure on simplicial presheaves]], which we now briefly indicate.

Write [[sSet]] for the category of [[simplicial sets]]. Here we always regard this as equipped with the standard [[model structure on simplicial sets]] $sSet_{Quillen}$.

+-- {: .num_defn }
###### Definition

For $C$ a [[small category]] write $[C^{op}, sSet]\simeq [C^{op}, Set]^{\Delta^{op}}$ for the category of [[simplicial presheaves]]. The **global projective [[model structure on simplicial presheaves]]** $[C^{op}, sSet]_{proj}$ has as

* [[weak equivalences]] the objectwise [[weak homotopy equivalences]] of simplicial sets

* [[fibrations]] the objectwise [[Kan fibrations]]. 

=--

+-- {: .num_remark }
###### Remark

Accordingly $[C^{op}, sSet]$ is a [[cofibrantly generated model category]] with generating (acyclic) cofibrations the [[tensoring]] of objects of $C$ with the generating (acyclic) cofibrations of $sSet_{Quillen}$. 

=--


### Left Bousfield localization

+-- {: .num_defn #BousfieldLocalizationOfModelStructureOnSimplicialPresheaves}
###### Definition

Given a [[model category]] $[C^{op}, Set]_{proj}$ and set $\mathcal{S} \subset Mor([C^{op}, Set])$ of morphisms, the [[Bousfield localization of model categories|left Bousfield localization]] is the model structure with the same cofibrations and weak equivalences the $\mathcal{S}$-[[local morphisms]].

$$
 [C^{op}, Set]_{proj,\mathcal{S}}
  \stackrel{\overset{id}{\leftarrow}}{\underset{id}{\to}}
 [C^{op}, Set]_{proj}
  \,.
$$

=--


### Combinatorial model categories

The simple idea of the following definition is to say that the model category analog of _[[locally presentable category]]_ is simply a model structure on a locally presentable category.

+-- {: .num_defn #CombinatorialModelCategory}
###### Definition

A model category is a **[[combinatorial model category]]** if 

1. the underlying category is a [[locally presentable category]];

1. the model structure is a [[cofibrantly generated model category]]. 

=--

### Dugger's theorem

+-- {: .num_theorem #DuggerTheorem}
###### Theorem

Every [[combinatorial model category]], def. \ref{CombinatorialModelCategory}, is [[Quillen equivalence|Quillen equivalent]] to a [[Bousfield localization of model categories|left Bousfield localization]] of a global [[model structure on simplicial presheaves]] as in def. \ref{BousfieldLocalizationOfModelStructureOnSimplicialPresheaves}.

=--

See at [combinatorial model category - Dugger's theorem](combinatorial%20model%20category#DuggerTheorem).

## Basic idea in $(\infty,1)$-category theory
 {#BasicIdeaInInfinityCategoryTheory}



### $(\infty,1)$-Presheaves

+-- {: .num_defn}
###### Definition

For $\mathcal{C}$ and $\mathcal{D}$ two [[(∞,1)-categories]] and $\mathcal{C}_{s}, \mathcal{D}_s \in sSet$ two models as [[quasi-categories]], an [[(∞,1)-functor]] $F \colon \mathcal{C} \to \mathcal{D}$ is simply a homomorphism of simplicial set $\mathcal{C}_s \to \mathcal{D}_s$. 

The [[(∞,1)-category of (∞,1)-functors]] $Func(\mathcal{C}, \mathcal{D})_s$ as a [[quasi-category]] is simply the [[hom object]] of simplicial set

$$
  Func(\mathcal{C}, \mathcal{D})_s = sSet(\mathcal{C}_s, \mathcal{D}_s)
  \in 
   QuasiCat \hookrightarrow sSet
  \,.
$$

=--



+-- {: .num_defn #InfinityPresheaves}
###### Definition

For $\mathcal{D}$ an [[(∞,1)-category]], the **[[(∞,1)-category of (∞,1)-presheaves]]** on $\mathcal{D}$ is the functor category

$$
  PSh_\infty(\mathcal{D})
  =
  Func(\mathcal{D}^{op}, \infty Grpd)
$$

out of the [[opposite (∞,1)-category]] of $\mathcal{D}$ into the [[∞Grpd|(∞,1)-category of ∞-groupoids]].

=--

### Localizations of $(\infty,1)$-categories

The notions of [[adjoint functors]], [[full and faithful functors]] etc. have straightforward, essentially verbatim generalizations to $(\infty,1)$-categories:

+-- {: .num_defn}
###### Definition

A pair of [[(∞,1)-functors]] 

$$ 
  C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} 
  D
$$

is a pair of **[[adjoint (∞,1)-functors]]**, if there exists a _unit transformation_  $\epsilon : Id_C \to R \circ L$ -- a morphism in the [[(∞,1)-category of (∞,1)-functors]] $Func(C,D)$ -- such that for all $c \in C$ and $d \in D$ the induced morphism

$$
  Hom_C(L(c),d)
   \stackrel{R_{L(c), d}}{\to}  
  Hom_D(R(L(c)), R(d))
  \stackrel{Hom_D(\epsilon, R(d))}{\to}
  Hom_D(c,R(d))
$$

is an [[equivalence of ∞-groupoids]].

=--


+-- {: .num_defn}
###### Definition

An [[(∞,1)-functor]] $F \colon \mathcal{C} \to \mathcal{D}$ is a 
**[[full and faithful (∞,1)-functor]]** if for all objects $X,Y \in \mathcal{C}$ the component

$$
  F_{X,Y} \colon \mathcal{C}(X,Y) \stackrel{\simeq}{\to} \mathcal{D}(F(X), F(Y))
$$

is an [[equivalence of ∞-groupoids]]. 

=--


+-- {: .num_defn #ReflectiveLocalization}
###### Definition

A [[reflective sub-(∞,1)-category]] $\mathcal{C} \hookrightarrow \mathcal{D}$ is a [[full and faithful (∞,1)-functor]] with a left [[adjoint (∞,1)-functor]].

=--


### Locally presentable $(\infty,1)$-categories

We have then the essentially verbatim analog of the situation for ordinary categories:

+-- {: .num_defn #LocallyPresentableInfinityCategory}
###### Definition

An [[(∞,1)-category]] $\mathcal{C}$ is a **[[locally presentable (∞,1)-category]]** if there exists a [[small set]] of objects such that the [[full sub-(∞,1)-category]] $\mathcal{C}^0 \hookrightarrow \mathcal{C}$ on it generates $\mathcal{C}$ under [[(∞,1)-colimits]].

=--

And the equivalent characterization is now as before

+-- {: .num_theorem #SimpsonTheorem}
###### Theorem

An [[(∞,1)-category]] is a [[locally presentable (∞,1)-category]], def. \ref{LocallyPresentableInfinityCategory}, precisely if it is [[equivalence of (∞,1)-categories|equivalent]] to  [[localization of an (∞,1)-category|localization]], def. \ref{ReflectiveLocalization}, 

$$
  \mathcal{C} \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\hookrightarrow}}
  PSh_\infty(\mathcal{C}^0)
$$

of an [[(∞,1)-category of (∞,1)-presheaves]], def. \ref{InfinityPresheaves}, such that $R \circ L$ preserves $\kappa$-[[filtered (∞,1)-colimits]] for some [[regular cardinal]] $\kappa$.

=--

This appears as [Lurie, theorem 5.5.1.1](#Lurie), attributed there to [[Carlos Simpson]].

### $(\infty,1)$-Toposes

As before, if a locally presentable $(\infty,1)$-category arises as the [[localization of an (∞,1)-category|localization]] $L \colon PSh_\infty(\mathcal{C}^0) \to \mathcal{C}$ of a [[left exact (∞,1)-functor]], then it is an [[(∞,1)-topos]].


### Presentation by combinatorial model categories

There is a close match between the theory of [[combinatorial model categories]] and [[locally presentable (∞,1)-categories]].

+-- {: .num_theorem }
###### Theorem

Every [[locally presentable (∞,1)-category]] arises, up to [[equivalence of (∞,1)-categories]], as the [[simplicial localization]] of a [[combinatorial model category]].

=--

This is part of [Lurie, theorem 5.5.1.1](#Lurie).


Accordingly, every [[simplicial Quillen adjunction]] between [[combinatorial model categories]] gives rise to a pair of [[adjoint (∞,1)-functors]] between the corresponding locally presentable $(\infty,1)$-categories.

Hence a [[left Bousfield localization]] of a [[model structure on simplicial presheaves]] presents a corresponding localization of an [[(∞,1)-category of (∞,1)-presheaves]] to a [[locally presentable (∞,1)-category]].


$$
  \array{   
    \mathcal{C} &\stackrel{\overset{}{\leftarrow}}{\hookrightarrow}& PSh_\infty(C)
    \\
    \left[C^{op}, sSet\right]_{proj,\mathcal{S}}
    &\stackrel{\overset{id}{\leftarrow}}{\underset{id}{\to}}&
    [C^{op}, sSet]_{proj}
  }
$$


## References

The standard textbook for [[locally presentable categories]] is

* [[Jiří Adámek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)
 {#AdamekRosicky}

Decent accounts of [[combinatorial model categories]] include secton A.2.6 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
 {#Lurie}
 
and 

* [[Clark Barwick]], _On (Enriched) Left Bousfield Localization of Model Categories_ ([arXiv:0708.2067](http://arxiv.org/abs/0708.2067))

The standard text for [[locally presentable (∞,1)-categories]] is section 5 of [Lurie](#Lurie).


