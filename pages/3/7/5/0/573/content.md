

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##

In [[higher category theory]] an _$(\infty,n)$-category_ may be thought of as

* an [[n-category]] up to [[coherence|coherent]] [[homotopy]];

* [[(n,r)-category|(r,n)-category]] for $r = \infty$;

* a [[weak omega-category]] for which all [[k-morphisms]] with $k \gt n$ are [[equivalences]].


## Definitions

There is an axiomatic characterization of the [[(∞,1)-category]] of $(\infty,n)$-categories (hence of these structures with all morphisms but only invertible [[transfors]] between them).

* [Axiomatic definition](#AxiomaticCharacterization)

Among the concrete constructions one can roughly distinguish two flavors, those that build $(\infty,n)$-categories by _[[enriched category|enrichment]]_ over $(\infty,n-1)$-categories

* [Definitions via enrichment](#ViaEnrichment)

and those that build them by [[internalization]] in the collection of $(\infty,n-1)$-categories

* [Definitions via internalization](#ViaInternalization).



### Axiomatic definition
 {#AxiomaticCharacterization}

We discuss the axiomatic characterization of the [[(∞,1)-category]] of $(\infty,n)$-categories due to ([Barwick, Schommer-Pries](#BarwickSchommerPries)).

#### Preliminaries

The main definition is def. \ref{AxiomaticDefinition} below, which roughly says that the collection of $(\infty,n)$-categories is _generated_ from [[strict n-categories]] in a certain sense. Therefore we first need to fix some terminology and notions about strict $n$-categories and about the relevant notion of generation.

+-- {: .num_defn}
###### Definition

Write $Str n Cat$ for the 1-[[category]] of [[strict n-categories]]. Write
$Str n Cat_{gaunt} \hookrightarrow  Str n Cat$ for the [[full subcategory]] on the _gaunt $n$-categories_, those $n$-categories whose only invertible [[k-morphisms]] are the identities.

=--

This subcategory was considered in ([Rezk](#Rezk)). The term "gaunt" is due to ([Barwick, Schommer-Pries](#BarwickSchommerPries)).

+-- {: .num_example #Globes}
###### Example

For $k \leq n $ the $k$-[[globe]] is gaunt, $G_k \in Str n Cat_{gaunt} \hookrightarrow \in Str n Cat$.

Write

$$
  \mathbb{G}_{\leq n} \hookrightarrow Str n Cat_{gaunt}
$$

for the [[full subcategory]] of the [[globe category]] on the $k$-globes for $k \leq n$.

Being a [[subobject]] of a gaunt $n$-category, also the [[boundary]] of a globe $\partial G_k \hookrightarrow G_k$ is gaunt, i.e. the $(k-1)$-[[skeleton]] of $G_k$.

=--

+-- {: .num_defn #nCatGen}
###### Definition

Write

$$
  Str n Cat_{gen} \hookrightarrow Str n Cat_{gaunt}
$$

for the smallest [[full subcategory]] that 

1. contains the [[globe category]] $\mathbb{G}_{\leq n}$, example \ref{Globes};
1. is closed under [[retracts]] in $Str n Cat_{gaunt}$; 
1. has all [[fiber products]] over [[globes]].

=--

([B-SP, def. 5.6](#BarwickSchommerPries))

+-- {: .num_defn #FundamentalPushouts}
###### Definition

The following [[pushout]] identities in $Str n Cat$ we call the _fundamental pushouts_ in the following

1. Gluing two $k$-globes along their boundary gives the boundary of the $(k+1)$-globle

   $G_k \coprod_{\partial C_{k-1}} G_k \simeq \partial G_{k+1}$

1. Gluing two $k$-globes along an $i$-face gives a [[pasting]] composition of the two globles

   $G_k \coprod_{G_i} G_k$

1. The [[fiber product]] of globes along non-degenerate morphisms $G_{i+j} \to G_i$ and $G_{i+k} \to G_i$ is built from gluing of globes by

   $$
     G_{i+j} \times_{G_i} G_{i+k}
     \simeq
     (G_{i+j} \coprod_{G_i} G_{i+k}) \coprod_{\sigma^{i+1}(G_{j-1} \times G_{k-1})} (G_{i+k} \coprod_{G_i} G_{i+j})
   $$

=--

Def. \ref{AxiomaticDefinition} considers an $(\infty,1)$-category _generated_ from $Str n Cat_{gen}$ in the following sense

+-- {: .num_defn #StrongGeneration}
###### Definition

For $\mathcal{D}$ an [[(∞,1)-category]] with all small [[(∞,1)-colimits]], say that an [[(∞,1)-functor]] 

$$
  f : \mathcal{C} \to \mathcal{D}
$$

_strongly generates_ $\mathcal{D}$ if its $(\infty,1)$-[[Yoneda extension]] on the [[(∞,1)-category of (∞,1)-presheaves]]

$$
  f : \mathcal{C} \stackrel{y}{\hookrightarrow} PSh_\infty(\mathcal{C}) \stackrel{Lan_y}{\to} \mathcal{D}
$$

is the reflector of a [[reflective sub-(∞,1)-category]]

$$
  \mathcal{D} \stackrel{\overset{Lan_y}{\leftarrow}}{\hookrightarrow}
  PSh_\infty(\mathcal{C})
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

By definition, a strongly generated $(\infty,1)$-category is in particular a 
[[presentable (∞,1)-category]].

=--

#### Characterization

+-- {: .num_defn #AxiomaticDefinition}
###### Definition

An **$(\infty,1)$-category of $(\infty,n)$-categories** $Cat_{(\infty,n)}$ is an [[(∞,1)-category]] equipped with a [[full and faithful functor]] 

$$
  i :  Str n Cat_{gen} \hookrightarrow \tau_{\leq 0}Cat_{(\infty,n)}
$$ 

from the generating strict $n$-categories, def. \ref{nCatGen} into its category of [[n-truncated object in an (infinity,1)-category|0-truncated]] objects, such that 

1. $\mathcal{Y}_n \to \tau_{\leq 0} Cat_{(\infty,n)} \hookrightarrow Cat_{(\infty,n)} $ [strongly generates](#StrongGeneration) $\mathcal{C}$;

1. $i$ preserves the [fundamental pushouts](#FundamentalPushouts);
   and sends (...) to an equivalence.

1. the [[base change]] [[adjoint triple]] in $Cat_{(\infty,n)}$ exists along morphisms with codomain in the image of $i$;

and such that $\mathcal{C}$ is [[universal property|universal]] with respect to these properties in that for any other $j : Str n Cat_{gen} \hookrightarrow \mathcal{C}$ satisfying these three conditions it factors through $i$

$$
  j : Str n Cat \stackrel{i}{\to} Cat_{(\infty,n)} \stackrel{L}{\to} \mathcal{C}
$$

by an [[(∞,1)-functor]] $L$ which is the reflector of a [[reflective sub-(∞,1)-category|reflective inclusion]] $\mathcal{C} \hookrightarrow Cat_{(\infty,n)}$.

=--

([B-SP, def. 6.8](#BarwickSchommerPries))



+-- {: .num_remark }
###### Remark

By the first axiom, the localization demanded in the universal property is essentially unique. In particular, therefore, $Cat_{(\infty,n)}$ is defined uniquely, up to [[equivalence of (∞,1)-categories]].
For more on this see prop. \ref{AutomorphismInfinityGroup} below.

=--

### Presentations

By def. \ref{AxiomaticDefinition} $Cat_{(\infty,n)}$ is [[equivalence of (∞,1)-categories]] to a [[localization of an (∞,1)-category|localization]] of the [[(∞,1)-category of (∞,1)-presheaves]] on $Str n Cat_{gen}$. In fact, various subcategories of $Str n Cat_{gen}$ are already sufficient. Here we discuss these [[presentable (∞,1)-category|presentations]]. 


+-- {: .num_defn #UniversalLocalizingClass}
###### Definition

Let $S_{0} \subset Mor(PSh_\infty(Str n Cat_{gen}))$
be the  class of morphism generated under fiber product $X \times_{G_k} (-)$ with objects $X \in Str n Cat_{gen}$ over globes by the following finite sets of morphisms

1. (...)

1. (...)

1. (...)

1. (...)

Write $S$ for the strongly saturated class of morphisms (see [[reflective sub-(∞,1)-category]]) generated by $S_0$.

=--

+-- {: .num_prop }
###### Proposition

The [[localization of an (∞,1)-category|localization]] of the [[(∞,1)-category of (∞,1)-presheaves]] over $Str n Cat_{gen}$, def. \ref{nCatGen} at the class of morphism $S$ from def. \ref{UniversalLocalizingClass} is a [[presentable (∞,1)-category|presentation]] of $Cat_{(\infty,n)}$, def. \ref{AxiomaticDefinition}:

$$
  Cat_{(\infty,n)} \simeq PSh_\infty(Str n Cat_{gen})[S^-1]
  \,.
$$

=--

([B-SP, theorem 7.6](#BarwickSchommerPries)).

### Via $\infty$-enrichment
 {#ViaEnrichment}

* [[enriched (∞,1)-category]]

* [[Segal n-category]]

### Via $\infty$-internalization
 {#ViaInternalization}

* [[internal category in an (∞,1)-category]]

* [[n-fold complete Segal space]]


## Properties

### Uniqueness and equivalences

+-- {: .num_prop #AutomorphismInfinityGroup}
###### Proposition

Let $Models_{(\infty,n)} \hookrightarrow \hat Cat_{(\infty,1)}$
be the [[core]] (maximal [[∞-groupoid]] inside) the full [[sub-(∞,1)-category]]
of [[(∞,1)Cat]] on those that satisfy the definition \ref{AxiomaticDefinition}. 

This is [[equivalence of (∞,1)-categories|equivalent]] to

$$
  Models_{(\infty,n)} \simeq B (\mathbb{Z}_2)^n,
$$

the [[delooping]] [[groupoid]] of the [[group]] $(\mathbb{Z}_2)^n$, the $n$-fold [[product]] of the [[group of order 2]] with itself.

The nontrivial element $\sigma \in \mathbb{Z}_2$ in the $k$th slot acts by passing to the $k$-opposite $(\infty,n)$-category.

=--

([B-SP, theorem 8.13](#BarwickSchommerPries))

+-- {: .num_remark }
###### Remark

This means that 

1. the $(\infty,1)$-category $Cat_{(\infty,n)}$ from def. \ref{AxiomaticDefinition} is uniquely defined, up to [[equivalence of (∞,1)-categories]];

1. the [[automorphism ∞-group]] of $Cat_{(\infty,n)}$ in $\hat Cat_{(\infty,1)}$ is $(\mathbb{Z}_2)^n$, hence the only auto-equivalences are given by reversal of [[k-morphisms]].

=--

## Examples ##

### Special cases 

* [[∞-groupoid]] = $(\infty,0)$-category
* [[(∞,1)-category]]
* [[(∞,2)-category]]
* etc ...

In addition,
* [[(n,r)-category|(m,n)-categories]] can be obtained as particular $(\infty,n)$-categories whose $k$-cells are trivial for $k\gt m$.
* In particular, [[n-categories]] = $(n,n)$-categories can be so obtained. 



### Specific examples

* One motivating example for $(\infty,n)$-categories is the [[(∞,n)-category of cobordisms]] which plays a central role in the formalization of the [[cobordism hypothesis]]. 

* Another class of examples are [[(∞,n)-categories of spans]].

## Related concepts

* [[0-category]], [[(0,1)-category]]

* [[category]]

* [[2-category]]

* [[3-category]]

* [[n-category]]

* [[(∞,0)-category]]

* [[(∞,1)-category]]

* [[(∞,2)-category]]

* **(∞,n)-category**

* [[(n,r)-category]]


## References ##

The definition in terms of [[Theta spaces]] is due to

* [[Charles Rezk]], _A cartesian presentation of weak n-categories_ ([arXiv:0901.3602](http://arxiv.org/abs/0901.3602))
 {#Rezk}

An iterartive definition in terms of [[n-fold complete Segal spaces]] is given in

* [[Jacob Lurie]], _$(\infty,2)$-Categories and the Goodwillie Calculus I_ ([arXiv:0905.0462](http://arxiv.org/abs/0905.0462))

A summary of definitions and some known comparison results can be found at

* [[Julie Bergner]], *Models for $(\infty, n)$-categories and the cobordism hypothesis*, [arXiv:1011.0110](http://arxiv.org/abs/1011.0110)

* [[Julie Bergner]], _Models for $(\infty,n)$-Categories and the Cobordism Hypothesis_ , in _[[Mathematical Foundations of Quantum Field and Perturbative String Theory]]_

An axiomatic characterization is in 

* [[Clark Barwick]], [[Chris Schommer-Pries]], _On the Unicity of the Homotopy Theory of Higher Categories_ ([arXiv:1112.0040](http://arxiv.org/abs/1112.0040), [unusual slides](http://prezi.com/w0ykkhh5mxak/the-uniqueness-of-the-homotopy-theory-of-higher-categories/))
 {#BarwickSchommerPries}

Comparison of models is in 

* [[Julie Bergner]], [[Charles Rezk]], _Comparison of models for $(\infty,n)$-categories_ ([arXiv:1204.2013](http://arxiv.org/abs/1204.2013))

[[!redirects (infinity,r)-category]]
[[!redirects (infinity,k)-category]]
[[!redirects (infinity,r)-categories]]
[[!redirects (infinity,k)-categories]]
[[!redirects (∞,n)-category]]
[[!redirects (∞,n)-categories]]
[[!redirects (∞,r)-category]]
[[!redirects (∞,r)-categories]]
[[!redirects (∞,k)-category]]
[[!redirects (∞,k)-categories]]
