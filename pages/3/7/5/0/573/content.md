

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

* an [[n-category]] up to [[coherence|coherent]] [[homotopy theory|homotopy]];

* an [[(n,r)-category|(r,n)-category]] for $r = \infty$;

* a [[weak omega-category]] for which all [[k-morphisms]] with $k \gt n$ are [[equivalences]].

Accordingly, the notion of $(\infty,n)$-categories is a joint generalization of  _[[categories]]_, _[[2-categories]]_, _[[3-categories]]_, _[[4-categories]]_, etc. and of _[[∞-groupoids]]_ / _[[homotopy types]]_ and  _[[(∞,1)-categories]]_. From the point of [[homotopy theory]] they are a generalization to _[[directed homotopy theory]]_, from the point of view of [[homotopy type theory]] they are a generalization to _[[directed homotopy type theory]]_.

There are two main [[recursion|recursive]] definitions of $(\infty,n)$-categories: 

1. by iterated [[enriched (∞,1)-category|(∞,1)-enrichment]]

   $$
     Cat_{(\infty,n)} \simeq (\cdots((Cat_{(\infty,0)} Cat) Cat) \cdots) Cat
   $$ 

1. by iterated [[category object in an (∞,1)-category|(∞,1)-internalization]]

  $$
    Cat_{(\infty,n)} \simeq Cat(\cdots(Cat(Cat_{(\infty,0)}))\cdots)
    \,.
  $$

There is also a fairly simple axiomatization of the [[(∞,1)-category]] [[(infinity,n)Cat|$Cat_{(\infty,n)}$]] itself, as something _[[generators and relations|generated]]_ by [[strict n-categories]]. 

Then there is also a plethora of [[model category]] structures that [[presentable (∞,1)-category|present]] the [[(∞,1)-category]] $Cat_{(\infty,n)}$ of all $(\infty,n)$-categories, which means that there are many (and many different) very explicit ways to describe them.

A central result of $(\infty,n)$-category theory is the proof of the [[cobordism hypothesis]], which revolves around the _[[(∞,n)-category of cobordisms]]_. This turns out to be the [[free construction|free]] _[[symmetric monoidal (∞,n)-category]]_ _[[(∞,n)-category with duals|with duals]]_ and provides deep relations between [[algebraic topology]], [[higher algebra]] and [[extended topological quantum field theory]].
Other fundamental examples of $(\infty,n)$-categories, also in this context, are [[(∞,n)-categories of spans]] and of [[(∞,n)-vector spaces]].

While the subject is still young, visible at the horizon is its role in [[higher topos theory]]. Where [[(∞,1)-toposes]] regarded as [[(∞,1)-categories of (∞,1)-sheaves]]/[[∞-stacks]] are by now fairly well understood, it is clear that the [[(∞,2)-categories]] of [[(∞,2)-sheaves]] -- such as the [[codomain fibration]]/[[indexed category|self-indexing]] of an [[(∞,1)-topos]] -- will form an [[(∞,2)-topos]] in generalization of the non-homotopic notion of [[2-topos]]. And so on.


## Introduction

Here are some introductory words for readers unfamiliar with the general idea. Other readers should skip [ahead](#Definition).

* _[Introduction for 1-category theorists](#1CatIntro)_

* _[Introduction for homotopy theorists](#HomotopyIntro)_

### For 1-category theorists
 {#1CatIntro}

This section assumes that the reader is well familiar with [[category theory]] and maybe with [[strict omega-categories]] but in need of some introductory words on $(\infty,n)$-categories.

Ordinary [[category theory]] provides various powerful tools for generating higher order structures, among them notably

1. [[enriched category theory|enrichment]]

1. [[internalization]].

Here we are interested in higher order _[[categories]]_, so we consider [[Cat]] itself as a 1-categorical context for either of these procedures. Since [[Cat]] naturally a [[cartesian monoidal category]] 

$$
  (\mathcal{V}, \otimes) \coloneqq (Cat, \times)
$$ 

we may form the [[category of V-enriched categories]] $\mathcal{V}Cat \coloneqq Cat Cat$. A $Cat$-category consists of

* a collection of [[objects]];

* for each pair of objects $A$, $B$ a _category_ of morphisms, hence to be thought of as collection of ordinary morphisms $A \to B$ together with _morphisms between these morphisms_: [[2-morphisms]];

* such that composition is a _functor_ on these hom-categories.

This is the structure of a _[[strict 2-category]]_. We have that

$$
  Cat Cat \simeq Str 2 Cat
  \,.
$$

is the category of strict 2-categories.

By general results of [[enriched category theory]] (or by immediate inspection), this is still a [[cartesian monoidal category]] and so we may iterate this and consider now the enriching category

$$
  (\mathcal{V}, \otimes) \coloneqq (Cat Cat, \times)
$$

and construct again $\mathcal{V}Cat$, which now is

$$
  (Cat Cat) Cat \simeq Str 3 Cat
$$

the category of strict _[[3-categories]]_. It continues this way, and so for every $n \in \mathbb{N}$ the $n$-fold iterated enrichment of $Cat$ is the category 

$$
  Str n Cat \simeq  (\cdots ((Cat Cat)Cat) \cdots) Cat
$$

of _[[strict n-categories]]_. The [[inductive limit]] of this construction finally is the category of [[strict omega-categories]].

While this easily generates [[higher category theory|higher categorical structures]], it does so, as the terminology indicates, only in a very restrictive way: while every [[2-category]] still happens to be [[equivalence of 2-categories|equivalent]] to a [[strict 2-category]], already the general [[3-category]] is no longer equivalent to a strict 3-category, and the discrepancy only increases with $n$.

But inspection in the case of [[2-categories]] already shows what the problem is: in a [[bicategory|weak 2-category]] structural relations such as [[associativity]] and [[unitality]] no longer hold as equations but only _up to_ an _invertible_ [[2-morphism]], whereas objects in  $Str 2 Cat \simeq Cat Cat$, by definition of [[enriched category]], satisfy these relations _strictly_ -- therefore the name. 

But this problem directly corresponds to an evident shortcoming of the very starting point of the above recursive construction: that construction regarded [[Cat]] as a 1-category in order to fit it into the standard formulation of [[enriched category theory]]; however [[Cat]] is naturally rather a [[2-category]] itself. The enrichment procedure should be allowed to make use of this extra structure. On the other hand, as we have just seen, the failure of $Cat Cat$ to model all of [[2Cat]] is only in the lack of _invertible_ 2-morphisms. Therefore what should really matter for the improved enrichment is just the [[(2,1)-category]] underlying [[Cat]], which is the 2-category consisting of all [[categories]], all [[functors]] between them, but only _[[natural isomorphism]]_ instead of all [[natural transformations]] between those.

This way one does arrive at a suitable refined notion of enrichment over the [[(2,1)-category]] $Cat$, and interpreted this way one does finds that $Cat Cat$ then indeed produces all of [[2Cat]].

However, this only fixed the first step of the above recursive definition. In the next step we want $(2 Cat)Cat$ to produce all [[3-categories]], but their associativity and unitalness now involves invertible [[coherence]] _[[3-morphisms]]_ which do not appear in enriched $(2,1)$-category theory. And so on, as the recursion proceeds.

This shows that the natural starting point for a construction of [[n-categories]] by recursive enrichment must be a conception of 1-[[category theory]] which knows already about _invertible_ [[k-morphisms]] for all $k$. The notion of category where all 1-categorical operations are relaxed up to _invertible_ higher morphisms is that of _[[(∞,1)-category]]_. And this now turns out to be a good starting point for producing $n$-categories by recursive enrichment. 

If we then just replace in the above the naive [[Cat]] with [[(∞,1)Cat]], then the simple formula

$$
  Cat_{(\infty,n)} \coloneq (\cdots ((Cat_{(\infty,1)} Cat_{(\infty,1)})Cat_{(\infty,1)}) \cdots) Cat_{(\infty,1)}
$$

does produce a good general notion of $n$-categories, these are the _$(\infty,n)$-categories_ discussed here.

There is also an alternative road to the same conclusion: another standard procedure for producing higher order structures from the 1-category [[Cat]] is to consider [[internal categories]] in $Cat$. For $E$ a category with [[finite limits]], write $Cat(E)$ for the category of $E$-[[internal categories]], and hence $Cat(Cat)$ for the category of $Cat$-internal categories.

This gives _[[double categories]]_

$$
  DoubleCat \simeq Cat(Cat)
$$

and hence again not quite the [[2-categories]] that we are after. But it is of interest to note that now there are _two_ problems, not just the one above: while a $Cat$-internal category again has strict [[associativity]] and [[unitality]], instead of the desired version up to an invertible 2-morphism, in another direction it is more general than a [[strict 2-category]]: the latter only corresponds to those special double categories for which the "vertical" and the "horizontal" 1-morphisms come from the same 1-category and have sufficiently many degenerate 2-morphisms between them.

The first problem turns out to be solved as before: instead of working with the 1-category [[Cat]] we should already regard that as a [[(2,1)-category]] and then formulate _internal (2,1)-categories_ in straightforward generalization of the ordinary notion. For the second problem it turns out that one needs to slightly enhance that straightforward generalization and add a condition known (somewhat undescriptively) as _[[complete Segal space|completeness]]_. But if this is understood then (as discussed in detail at [[internal category in an (∞,1)-category]]) the simple idea of iterated internalization does work out and we obtain $(\infty,n)$-categories by

$$
  Cat_{(\infty,n)} \simeq Cat(\cdots(Cat(Cat_{(\infty,0)}))\cdots)
  \,.
$$





### For homotopy theorists
 {#HomotopyIntro}

This section assumes that the reader is well familiar with [[homotopy theory]] and maybe with [[(∞,1)-category theory]] but in need of some introductory words on $(\infty,n)$-categories.

A fundamental insight of [[homotopy theory]] is, of course,  that the [[geometric shapes for higher structures|cellular shape]] of [[simplices]] naturally serves to model paths and higher [[homotopies]] in "spaces", which here really means: in [[homotopy types]]/[[∞-groupoids]]. In fact, the simplices see a bit more: since $\Delta[n]$ is naturally identified with the [[total order|linear category]] $\{0 \to 1 \to 2 \to \cdots \to n\}$ on $(n+1)$-objects, there is a _direction_ on the paths which form the [[simplicial skeleton|1-skeleton]] of a map $\Delta^n \to X$. 

If $X$ is a [[topological space]]/[[simplicial set]]/[[homotopy type]], then this directedness in a way "disappears up to equivalence", in that for every such directed path there is also the reverse path, which is an inverse up to equivalence.

But it is straightforward to consider a slight generalization of this situation where we take $X$ to be such that _not_ all paths in it have inverses. Still thinking of $X$ as a homotopy type this may be thought of as modelling a _[[directed homotopy theory|directed homotopy type]]_. For $X$ instead modeled as a simplicial set, this has been formalized by the concept of a _[[quasi-category]]_ or _[[(∞,1)-category]]_. These are combinatorial models for _[[directed homotopy theory|directed homotopy types]]_ in direct generalization of how [[Kan complexes]] are combinatorial models for ordinary [[homotopy types]].

As the notation already suggests, the idea of $(\infty,n)$-category theory is that this generalization from [[∞-groupoids]] ("($\infty,0$)-categories") to [[(∞,1)-categories]] is but the first step in a tower of higher generalizations, where in step $n$ one considers "directed homotopy" up to and including dimension $n$.

It is natural that such _$(\infty,n)$-categories_ should be probed by corresponding higher dimensional analogs of the objects in the [[simplex category]], the linear categories $\Delta[n] = \{0 \to 1 \to 2 \to \cdots \to n\}$ that support traditional homotopy theory. There are many such generalizations which one could consider. One which has proven to be useful are the objects in the $n$th [[Theta-category]] $\Theta_n$. Where the linear categories as above arise from gluing -- [[pasting]] -- of cellular intervals, the objects of $\Theta_n$ arise from [[pasting]] of $n$-dimensional cellular _[[globes]]_ (an interval being a 1-dimensional globe). 

Accordingly, just as an [[∞-groupoid]]/[[homotopy type]] may be presented by a [[simplicial set]], hence a [[presheaf]] on the [[simplex category]] -- or more generally by a [[bisimplicial set|simplicial space]]-- satisfying some ([[Kan complex|Kan filler]]-)condition that encodes the existence of composites and inverses, so an [[(∞,n)-category]] may be presented by a presheaf of spaces on the $n$th [[Theta-category]], similarly subject to some conditions that ensure the existence of composites and inverses -- but only of inverses above dimension $n$.


## Definitions
 {#Definition}

There are various different ways of defining $(\infty,n)$-categories, which are all natural in their own right, and all equivalent to each other. 

There is an axiomatic characterization of the [[(∞,1)-category]] of $(\infty,n)$-categories by [[generators and relations|generation]] from [[strict n-categories]]:
 
* [Definition via generation from strict n-categories](#AxiomaticCharacterization)

Among the more direct definitions of $(\infty,n)$-categories one can roughly distinguish two flavors, those that build $(\infty,n)$-categories by _[[enriched category|enrichment]]_ over $(\infty,n-1)$-categories

* [Definitions via enrichment](#ViaEnrichment)


and those that build them by [[internalization]] in the collection of $(\infty,n-1)$-categories

* [Definitions via internalization](#ViaInternalization).



### Via generation by strict $n$-categories
 {#AxiomaticCharacterization}

We discuss a characterization of the [[(∞,1)-category]] of $(\infty,n)$-categories as an $(\infty,1)$-category [[generators and relations|generated]] by [[strict n-categories]], due to ([Barwick, Schommer-Pries](#BarwickSchommerPries)).

The blueprint for the following construction is the traditional fact that a [[category]] is characterized by the fact that its [[nerve]] is a [[simplicial set]] which satisfies the [[Segal conditions]], which reflect the existence of composition in a category. Since the simplicial nerve is induced from the [[total order|linear categories]] $\Delta[n] = \{0 \to 1 \to 2 \to \cdots \to n\}$ this can be taken as saying that these linear categories _generate_ [[Cat]], subject to the condition that there exists composites. 

The following discussion takes this point of view and generalizes it to a similar presentation of $(\infty,n)$-categories by very simple [[strict n-categories]].

#### Strict $n$-categories

The main definition is def. \ref{AxiomaticDefinition} below, which roughly says that the collection of $(\infty,n)$-categories is _generated_ from [[strict n-categories]] in a certain sense. Therefore we first need to fix some terminology and notions about strict $n$-categories and about the relevant notion of generation.




+-- {: .num_defn #GauntStrictNCategories}
###### Definition

Write $Str n Cat$ for the 1-[[category]] of [[strict n-categories]]. 

Write

$$
  Str n Cat_{gaunt} \hookrightarrow  Str n Cat
$$ 

for the [[full subcategory]] on the _[[gaunt category|gaunt]] $n$-categories_, those $n$-categories whose only invertible [[k-morphisms]] are the identities.

=--

This subcategory was considered in ([Rezk](#Rezk)). The term "gaunt" is due to ([Barwick, Schommer-Pries](#BarwickSchommerPries)). See prop. \ref{GauntIs0Truncated} below for a characterization intrinsic to $(\infty,n)$-categories.

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

+-- {: .num_defn #Suspension}
###### Definition

Write 

$$
  \sigma_k : Str (k) Cat \to Str (k+1) Cat
$$

for the "categorical suspension" functor which sends a strict $k$-category to the object $\sigma(X) \in Str (k+1) Cat \simeq (Str k Cat)Cat$ which has precisely two objects $a$ and $b$, has $\sigma(C)(a,a) = \{id_a\}$, $\sigma(C)(b,b) = \{id_b\}$, $\sigma(C)(b,a) = \emptyset$ and 

$$
  \sigma(C)(a,b) = C
  \,.
$$

=--

We usually suppress the subscript $k$ and write $\sigma^i = \sigma_{k+i} \circ \cdots \circ \sigma_{k+1} \circ \sigma_k$, etc.

+-- {: .num_example }
###### Example

The $k$-[[globe]] $G_k$ is the $k$-fold suspension of the 0-globe (the point)

$$
  G_k = \sigma^k(G_0)
  \,.
$$

The [[boundary]] $\partial G_k$ of the $k$-globe is the $k$-fold suspension of the
empty category

$$
  \partial G_k = \sigma^k(\emptyset)
  \,.
$$

Accordingly, the boundary inclusion $\partial G_k \hookrightarrow G_k$ is the $k$-fold suspension of the initial morphism $\emptyset \to G_0$

$$
  (\partial G_k \hookrightarrow G_k) = \sigma^k(\emptyset \to G_0)
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

The category $Str n Cat_{gaunt}$ is a [[locally presentable category]] and in fact a [[locally finitely presentable category]].

=--

([B-PS, lemma 3.5](#BarwickSchommerPries))

We are going to be interested in a full [[subcategory]] $Str n Cat_{gen} \hookrightarrow Str n Cat_{gaunt}$, given below in def. \ref{nCatGen}, which knows about the higher [[profunctors]]/[[correspondence|correspondences]] between $n$-categories.

\begin{remark}
For $A,B$ two categories, a [[profunctor]] $A^{op} \times B \to Set$ is equivalently a category [[slice category|over]] the 1-globe functor, hence a functor 

$$
  \array{
    K
    \\
    \downarrow
    \\
    G_1 & = \Delta[1]
  }
$$

equipped with an identification $A \simeq K_0$ and $B \simeq K_1$.
\end{remark}


This motivates the following definition.

+-- {: .num_defn }
###### Definition

A _$k$-profunctor_ / $k$-correspondence of strict $n$-categories is a morphism
$K \to G_k$ in $Str n Cat$. The category of $k$-correspondences is the [[slice category]] $Str n Cat/ G_k$.

=--

+-- {: .num_defn }
###### Definition

The categories  $Str n Cat_{gaunt}/G_k$ of $k$-correspondences between gaunt $n$-categories are [[cartesian closed category]].

=--

([B-SP, cor. 5.4](#BarwickSchommerPries))



+-- {: .num_remark}
###### Remark

By standard facts, in a [[locally presentable category]] $\mathcal{C}$ with [[finite limits]], a [[slice category|slice]] $\mathcal{C}/X$ is cartesian closed precisely if [[pullback]] along all morphisms $f : Y \to X$ with codomain $X$ preserves [[colimits]] (see at _[[locally cartesian closed category]]_ the section _[Cartesian closure in terms of base change and dependent product](locally%20cartesian%20closed%20category#EquivalentCharacterizations)_).

=--


+-- {: .num_example}
###### Example

Without the restriction that the codomain of $f$ in the above is a [[globe]], the pullback $f^*$ in $Str n Cat$ will in general fail to preserves colimits. For a simple example of this, consider the [[pushout]] diagram in [[Cat]] $\hookrightarrow Cat_{(\infty,1)}$ given by

$$
  \array{
     \Delta[0] &\stackrel{\delta_1}{\to}& \Delta[1]
     \\
     {}^{\mathllap{\delta_0}}\downarrow && \downarrow^{\mathrlap{\delta_0}}
     \\
     \Delta[1] &\stackrel{\delta_2}{\to}& \Delta[2]
  }
  \,.
$$

Notice that this is indeed also a [[homotopy pushout]]/[[(∞,1)-pushout]] since, by remark \ref{GauntIs0Truncted}, all objects involved are 0-truncated.

Regard this canonically as a pushout diagram in the [[slice category]] $Cat_{/\Delta[2]}$ and consider then the pullback $\delta_1^* : Cat_{/\Delta[1]} \to Cat_{/\Delta[1]}$ along the remaining face $\delta_1 : \Delta[1] \to \Delta[2]$. This yields the diagram

$$
  \array{
     \emptyset &\stackrel{}{\to}& \emptyset
     \\
     {}^{}\downarrow && \downarrow^{}
     \\
     \emptyset &\stackrel{}{\to}& \Delta[1]
  }
  \,,
$$

which evidently no longer is a pushout.

=--

(See also the discussion [here](http://golem.ph.utexas.edu/category/2011/11/the_1category_of_ncategories.html#c040335)).


The definition of $Cat_{(\infty,n)}$ below, def. \ref{AxiomaticDefinition}, will take this property to be one of the characteristic properties. Therefore consider

+-- {: .num_defn #nCatGen}
###### Definition

Write

$$
  Str n Cat_{gen} \hookrightarrow Str n Cat_{gaunt}
$$

for the smallest [[full subcategory]] that 

1. contains the [[globe category]] $\mathbb{G}_{\leq n}$, example \ref{Globes};
1. is closed under [[retracts]] in $Str n Cat_{gaunt}$; 
1. has all [[fiber products]] over [[globes]] (equivalently: such that all [[slice categories]] over globes have [[products]]).

=--

([B-SP, def. 5.6](#BarwickSchommerPries))

+-- {: .num_example }
###### Example

The following categories are naturally [[full subcategories]] of $Str n Cat_{gen}$

* the $n$-fold [[simplex category]] $\Delta^{\times n}$;

* the $n$th [[Theta-category]].

=--

This is discussed in more detail below in _[Presentation by Theta-spaces and by n-fold Segal spaces](#PresentationByThetaSpaces)_.

+-- {: .num_defn #FundamentalPushouts}
###### Definition

The following [[pushouts]] in $Str n Cat$ we call the **fundamental pushouts** 

1. Gluing two $k$-[[globes]] along their [[boundary]] gives the boundary of the $(k+1)$-globle

   $$G_k \coprod_{\partial C_{k-1}} G_k \simeq \partial G_{k+1}$$

1. Gluing two $k$-globes along an $i$-face gives a [[pasting]] composition of the two globles

   $$G_k \coprod_{G_i} G_k $$

1. The [[fiber product]] of globes along non-degenerate morphisms $G_{i+j} \to G_i$ and $G_{i+k} \to G_i$ is built from gluing of globes by

   $$
     G_{i+j} \times_{G_i} G_{i+k}
     \simeq
     (G_{i+j} \coprod_{G_i} G_{i+k}) \coprod_{\sigma^{i+1}(G_{j-1} \times G_{k-1})} (G_{i+k} \coprod_{G_i} G_{i+j})
   $$

1. The [[interval groupoid]] $(a \stackrel{\simeq}{\to} b)$ is obtained by forcing in $\Delta[3]$ the morphisms $(0\to 2)$ and $(1 \to 3)$ to be identities and it is equivalent, as an $n$-category, to the 0-globe

   $ \Delta[3] \coprod_{\{0,2\} \coprod \{1,3\}} (\Delta[0] \coprod \Delta[0])
   \stackrel{\sim}{\to} G_0$

   and the analog is true for all suspensions of this relation

   $$ 
     \sigma^k(\Delta[3]) \coprod_{\sigma^k\{0,2\} \coprod \sigma^k\{1,3\}} (G_k\coprod G_k)
     \stackrel{\sim}{\to} G_k
     \,.
   $$

We say a functor $i$ on $Str n Cat$ _preserves_ the fundamental pushouts if it preserves the first three classes of pushouts, and if for the last one the morphism
$i(\sigma^k(\Delta[3])) \coprod_{i(\sigma^k\{0,2\}) \coprod i(\sigma^k\{1,3\})} (i(G_k \coprod G_k)) \to i(G_k)$ is an equivalence.

=--



#### Generation by strict $n$-categories

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



+-- {: .num_defn #AxiomaticDefinition}
###### Definition

An **$(\infty,1)$-category of $(\infty,n)$-categories** $Cat_{(\infty,n)}$ is an [[(∞,1)-category]] equipped with a [[full and faithful functor]] 

$$
  i :  Str n Cat_{gen} \hookrightarrow \tau_{\leq 0}Cat_{(\infty,n)}
$$ 

from the generating strict $n$-categories, def. \ref{nCatGen} into its category of [[n-truncated object in an (infinity,1)-category|0-truncated]] objects, such that 

1. $Str n Cat_{gen} \to \tau_{\leq 0} Cat_{(\infty,n)} \hookrightarrow Cat_{(\infty,n)} $ [strongly generates](#StrongGeneration) $\mathcal{C}$;

1. $i$ preserves the [fundamental pushout](#FundamentalPushouts) relations;

1. the [[base change]] [[adjoint triple]] in $Cat_{(\infty,n)}$ exists along morphisms with codomain a [[globe]];

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

+-- {: .num_remark #GauntIs0Truncted}
###### Remark

The gaunt $n$-categories, def. \ref{GauntStrictNCategories} are indeed among the [[n-truncated object in an (∞,1)-category|0-truncated]] objects: since we are looking at just the [[(∞,1)-category]] of $(\infty,n)$-categories, instead of more generally the $(\infty,n+1)$-category the non-invertible [[transfors]] between $n$-categories are disregarded and so if an object $X \in Cat_{(\infty,n)}$ has no non-trivial invertible cells, then for every other objeyt $Y$, the hom-$\infty$-groupoid $Cat_{(\infty,n)}(Y,X)$ is 0-truncated, hence is a set.

=--

+-- {: .num_remark }
###### Remark

The first axiom in particular says that $Cat_{(\infty,n)}$ is a [[presentable (∞,1)-category]], and hence so are all its [[over-(∞,1)-category|slices]]. In view of this the [[adjoint (∞,1)-functor theorem]] says that the third condition is equivalent to [[(∞,1)-pullbacks]] 

$$
  f^* : Cat_{(\infty,n)}/_{i(G_k)} \to Cat_{(\infty,n)}/X
$$

along morphisms of the form $X \to i(G_k)$ preserving [[(∞,1)-colimits]].

=--


#### Universal presentation

By def. \ref{AxiomaticDefinition} $Cat_{(\infty,n)}$ is [[equivalence of (∞,1)-categories|equivalent]] to a [[localization of an (∞,1)-category|localization]] of the [[(∞,1)-category of (∞,1)-presheaves]] on $Str n Cat_{gen}$. In fact, various subcategories of $Str n Cat_{gen}$ are already sufficient, notable the [[Theta-category]] $\Theta_n \hookrightarrow Str n Cat$ (discussed below in \ref{PresentationByThetaSpaces}). Here we discuss these [[presentable (∞,1)-category|presentations]]. 


+-- {: .num_defn #UniversalLocalizingClass}
###### Definition

Let $S_{0} \subset Mor(PSh_\infty(Str n Cat_{gen}))$
be the  class of morphism generated under fiber product $X \times_{G_k} (-)$ with objects $X \in Str n Cat_{gen}$ over globes by 

1. the morphisms that witness the [fundamental pushout relations](#FundamentalPushouts)

1. the initial morphism $\emptyset \to i(\emptyset)$ into presheaf represented by the empty category (which coincides with the initial presheaf on all objects except on the empty category, where it is the singleton).


Write $S$ for the strongly saturated class of morphisms (see [[reflective sub-(∞,1)-category]]) generated by $S_0$.

=--

+-- {: .num_prop }
###### Proposition

The [[localization of an (∞,1)-category|localization]] of the [[(∞,1)-category of (∞,1)-presheaves]] over $Str n Cat_{gen}$, def. \ref{nCatGen} at the class of morphism $S$ from def. \ref{UniversalLocalizingClass} is a [[presentable (∞,1)-category|presentation]] of $Cat_{(\infty,n)}$, def. \ref{AxiomaticDefinition}:

$$
  Cat_{(\infty,n)} \simeq PSh_\infty(Str n Cat_{gen})[S^{-1}]
  \,.
$$

=--

([B-SP, theorem 7.6](#BarwickSchommerPries)).

+-- {: .proof}
###### Proof

The three axioms of def. \ref{AxiomaticDefinition} are satisfied effectively by construction  of $S$ (...). Conversely, every localization satisfying the second and third axiom must invert the morphisms in $S$, hence must be a sub-localization.

=--

+-- {: .num_remark }
###### Remark

This construction shows that the [fundamental pushout relations](#FundamentalPushouts) encode the _composition_ of [[k-morphisms]] in an $(\infty,n)$-category.

Let $X \in PSh_\infty(Str n Cat)$ be some object.

First, by the [[(∞,1)-Yoneda lemma]] the value of this [[(∞,1)-presheaf]] on a strict $n$-category $C$ is the $\infty$-groupoid of $(\infty,n)$-functors $C \to X$, [[natural equivalences]] between them, and so on.


And if $X$ is an $S$-[[local object]] then it has in particular the property that all the morphisms

$$
  Cat_{(\infty,n)}(
    i(G_k) \coprod_{i(G_j)} i(G_k)
    \to 
    i(G_jk \coprod_{ G_j } G_k)
    , 
    X
  )
$$

are equivalences of $\infty$-groupoids. So by the [[(∞,1)-Yoneda lemma]] this is equivalent to

$$
  X(G_k) \times_{X(G_i)} X(G_k)
  \to
  Cat_{(\infty,n)}(i(G_jk \coprod_{ G_j } G_k), X)
$$

being an equivalence. On the left this is the collection of all those pairs of $k$-globes in $X$ that touch at an $i$-boundary. On the right this is the collection of all [[k-morphisms]] in $X$ equipped with a choice of decomposing them into two $k$-morphisms touching at an $i$-boundary. So the statement that this morphism is an equivalence says that _composition_ of $k$-morphisms along $i$-boundaries exists in $X$.

=--

Various other presentations of $Cat_{(\infty,n)}$ are obtained by localizations over subcategories of  
$i : Str n Cat_{restr} \hookrightarrow Str n Cat_{gen}$ at a set of morphisms $T \subset Mor(PSh_\infty(R))$. Write

$$
  PSh_\infty(Str n Cat_{restr})
   \stackrel{\overset{i_!}{\to}}{\stackrel{\overset{i^*}{\leftarrow}}{\underset{i_*}{\to}}}
  PSh_\infty(Str n Cat_{gen})
$$

for the induced [[essential geometric morphism]].

+-- {: .num_prop #SufficientConditionsForPresentation}
###### Proposition

The following conditions are sufficient in order that 

$$
  Cat_{(\infty,n)} \simeq 
  PSh_\infty(Str n Cat_{gen})[S^{-1}]
  \stackrel{i^*}{\to} 
  PSh_\infty(Str n Cat_{restr})[T^{-1}]
$$

is an [[equivalence of (∞,1)-categories]]:

1. $i^*(S_0) \subset T$

1. $i_!(T_0) \subset S$

1. [[generalized the|the]] [[unit of an adjunction|counit]] $id \to i^* i_!$ has components in $T$;

1. the $k$-[[globe]] $G_k$ is in the essential image of $i$, for each $0 \leq k \leq n$.


=--

([B-SP, theorem 9.2](#BarwickSchommerPries)) 

#### Presentation by $\Theta_n$-spaces and $n$-fold complete Segal spaces
 {#PresentationByThetaSpaces}

We discuss now presentations of $Cat_{(\infty,n)}$ over subcategories of $Str n Cat_{gen}$, according to prop. \ref{SufficientConditionsForPresentation}.


+-- {: .num_prop }
###### Proposition

The $n$th [[Theta category]] is a [[full subcategory]] 

$$
  \Theta_n \hookrightarrow Str n Cat_{gen}
$$ 

and the localization of $PSh_\infty(\Theta_n)$ that defines the $(\infty,1)$-category $\Theta_n Space$ of $(\infty,n)$-[[Theta-spaces]] satisfies the conditions of prop. \ref{SufficientConditionsForPresentation}. 

Hence $(\infty,n)$-[[Theta-spaces]] are a model for $(\infty,n)$-categories, in the sense of def. \ref{AxiomaticDefinition}:

$$
  \Theta_n Space \simeq Cat_{(\infty,n)}
  \,.
$$


=--

([B-SP, theorem 11.15](#BarwickSchommerPries))

There is a further restriction from the objects of $\Theta_n$ to  _$n$-fold simplices_ regarded as _[grid object](Theta+category#EmbeddingOfGrids)_, under the canonical embedding

$$
  \delta_n : \Delta^{\times n} \to \Delta^{\wr n} \simeq \Theta_n
$$ 

induced by the identification of the $n$th[[Theta-category]] (see there) with the $n$-fold [[categorical wreath product]] of the [[simplex category]] with itself.


+-- {: .num_prop #CompleteSegalOvernFoldSimplicialSetsIsPresentation}
###### Proposition

The inclusion

$$
  \Delta^{\times n} \stackrel{\delta_n}{\to} 
  \Theta_n \hookrightarrow Str n Cat_{gen}
$$ 

and the localization of $PSh_\infty(\Delta^{\times n})$ that defines the $(\infty,1)$-category $CSS(\Delta^{\times n})$ of _[[n-fold complete Segal spaces]]_ satisfies the conditions of prop. \ref{SufficientConditionsForPresentation}. 

Hence [[n-fold complete Segal spaces]] are a model for $(\infty,n)$-categories, in the sense of def. \ref{AxiomaticDefinition}:

$$
  CSS(\Delta^{\times n}) \simeq Cat_{(\infty,n)}
  \,.
$$


=--

([B-SP, theorem 12.6](#BarwickSchommerPries))

+-- {: .num_remark}
###### Remark


Below in [Via ∞-Internalization -- Presentation by complete Segal spaces](#PresentationByCompleteSegal) is discussed that $n$-fold complete Segal spaces also naturally model an alternative definition of $(\infty,n)$-categories by [iterated ∞-internalization](#ViaInternalization). Then prop. \ref{CompleteSegalOvernFoldSimplicialSetsIsPresentation} serves to show that this is equivalent to def. \ref{AxiomaticDefinition} above.

=--


### Via $\infty$-enrichment
 {#ViaEnrichment}

#### General

There should be a general notion of _[[enriched (∞,1)-category]]_ (see there) over a [[monoidal (∞,1)-category]] $\mathcal{V}$. Write $\mathcal{V}Cat$ for the [[(∞,1)-category]] of $\mathcal{V}$-enriched $(\infty,1)$-categories.

+-- {: .num_defn #EnrichementDefinition}
###### Definition

For $n \in \mathbb{N}$ write

$$
  Cat_{(\infty,n)} \coloneqq
  (((\infty Grpd Cat) Cat) \cdots) Cat
  \,.
$$

=--


#### Presentation by Segal $n$-categories

The notion of _[[Segal n-categories]]_ is a realization of the
idea of _weak enrichment_ in a suitable [[model category]]. 
For nice enough model categories this can be further 
strictfied to just the notion of [[enriched model category]], 
discussed _[below](#ByEnrichedModelCategories)_

(...)

#### Presentation by enriched model categories
 {#ByEnrichedModelCategories}

(...)


### Via $\infty$-internalization
 {#ViaInternalization}

#### General



There is a general notion of _[[internal category in an (∞,1)-category]]_ $\mathcal{C}$ provided that

1. $\mathcal{C}$ has [[finite limit|finite]] [[(∞,1)-limits]] -- in order to formulate the [[Segal condition]];

1. $\mathcal{C}$ is equipped with a "choice of internal [[∞-groupoids]]" -- in order to formulate the [completeness condition](complete%20Segal%20space#CompleteSegalSpaces).

We can use this to define $Cat_{(\infty,n)}$ by iterative internalization.

+-- {: .num_defn }
###### Proposition

Write $Grpd(Cat_{(\infty,0)})$ for the catgeory of [[groupoid objects in an (∞,1)-category]] in $Cat_{(\infty,0)} \simeq $ [[∞Grpd]].

Assume we have already defined $Cat_{(\infty,n)}$, either by one of the methods above, or by the induction in the following. Then the canonical inclusion

$$
  Grpd(Cat_{(\infty,0)}) \hookrightarrow PreCat_{Grpd(Cat_{(\infty,0)})} (Cat_{(\infty,n)})
$$

into the $(\infty,1)$-category of [[simplicial objects]] $X_\bullet$ in $Cat_{(\infty,n)}$ that

1. satisfy the [[Segal conditions]]

1. such that $X_0 \in Cat_{(\infty,0)}$ 

has a [[right adjoint|right]] [[adjoint (∞,1)-functor]] $Core$.


=--

([Lurie, prop. 1.1.14](#Lurie)).


+-- {: .num_defn #IteratedInternalization}
###### Definition

An $(\infty,n+1)$-category is an object  $X \in PreCat_{Grpd(Cat_{(\infty,0)})}$
such that $Core(X) \in \infty Grpd \hookrightarrow Grpd(Cat_{(\infty,0)})$.



For $n \in \mathcal{N}$ the $(\infty,1)$-category of 
$(\infty,n)$-categories is

$$
  Cat_{(\infty,n)}
  \coloneqq  
  Cat^n(\infty Grpd)
  \coloneqq
  Cat(\cdots Cat(Cat_{(\infty,0)}) \cdots)
  \,.
$$

=--

([Lurie, prop. 1.1.14](#Lurie)).



+-- {: .num_prop }
###### Proposition

The $(\infty,1)$-category $Cat_{(\infty,n)}$ given by
def. \ref{IteratedInternalization} is [[equivalence of (∞,1)-categories|equivalent]] to that given by
def. \ref{AxiomaticDefinition}.

=--

This is prop. \ref{CompleteSegalOvernFoldSimplicialSetsIsPresentation}
in view of the presentation discussed [below](#PresentationByCompleteSegal).

#### Presentation by $n$-fold complete Segal spaces
 {#PresentationByCompleteSegal}

By the discussion [here](category+object+in+an+%28infinity,1%29-category#ModelCategoryPresentations) at _[[category object in an (∞,1)-category]]_ we have

+-- {: .num_prop }
###### Proposition

Write $cSegal_0 \coloneqq sSet_{Quillen}$ for the standard [[model structure on simplicial sets]]. Then recursively for $n \in \mathbb{N}$, $n \geq 1$, there is a model structure on 

$$
  cSegal_n \coloneqq [\Delta^{op}, cSegal_{n-1}]
$$

which [[presentable (infinity,1)-category|presents]] $Cat^n(\infty Grpd)$.

=--


+-- {: .num_prop }
###### Proposition

$cSegal_n$ is equivalent to the $CSS(\Delta^{\times n})$
from prop. \ref{CompleteSegalOvernFoldSimplicialSetsIsPresentation}.

=--

(...)

## Properties

### Generators
 {#Generators}

+-- {: .num_prop }
###### Proposition

The [[(∞,1)-category]] $Cat_{(\infty,n)}$ is generated under [[(∞,1)-colimits]] from the $k$-[[globes]] $G_k$ for $k \leq n$: every object is the [[(∞,1)-colimit]] over a diagram of globes.

=--

([B-SP, cor. 8.4](#BarwickSchommerPries))

+-- {: .num_prop }
###### Proposition

[[equivalence in an (∞,1)-category|Equivalences]] in the [[(∞,1)-category]] $Cat_{(\infty,n)}$ are detected on [[globes]]: a morphism $f : X \to Y$ in $Cat_{(\infty,n)}$ is an equivalence precisely if for all globes $G_{k \leq n}$ the induced morphism on [[derived hom-space|(∞,1)-categorical hom-spaces]]

$$
  Cat_{(\infty,n)}(G_k, f) : Cat_{(\infty,n)}(Y, f) \to Cat_{(\infty,n)}(X, f)
$$

is an equivalence of [[∞-groupoids]].

=--

([B-SP, cor. 8.5](#BarwickSchommerPries))

### Truncated objects

+-- {: .num_prop #GauntIs0Truncated}
###### Proposition

The [[truncated object in an (∞,1)-category|truncated objects]] in the [[(∞,1)-category]] $Cat_{(\infty,n)}$ are precisely the [gaunt](#GauntStrictNCategories) [[strict n-categories]]

=--

([B-SP, cor. 8.6](#BarwickSchommerPries))

+-- {: .num_remark }
###### Remark

That 0-truncated objects in the $Cat_{(\infty,n)}$ regarded as an $(\infty,1)$-category are gaunt is effectively the definition of 0-truncation in the absence of non-invertibles [[transfors]]. That these gaunt $(\infty,n)$-categories are then necessarily _[[strict n-category|strict]]_ reflects the fact that all the weakening, namely all the [[associators]] and [[unitors]] as well as all there [[coherence|coherences]] need to be invertible [[k-morphisms]], and hence must be trivial if there are no non-trivial such.

=--


### Moduli 

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

1. the [[automorphism ∞-group]] of $Cat_{(\infty,n)}$ in $\hat Cat_{(\infty,1)}$ is $(\mathbb{Z}_2)^n$, hence the only auto-equivalences are given by forming the $n$ analogs of forming an [[opposite (∞,1)-category]].

=--



+-- {: .proof}
###### Proof

The idea is this:

One first observes that $Str n Cat_{gaunt}$ from def. \ref{GauntStrictNCategories} has $(\mathbb{Z}_2)^{\times n}$ worth of automorphisms, given by 
reversing the directions of the [[k-morphisms]]. 

For this, 

1. observe that the identity is the only [[natural transformation]] [[endomorphism]] on $Id : Str n Cat_{gaunt} \to Str n Cat_{gaunt}$: this can be checked on [[globes]] for which one observes that if a functor $G_n \to G_n$ is the identity on $\partial G_n$, then it is so also on the unique $n$-cell. ([B-SP, lemma 4.1](#BarwickSchomerPries))

1. observe that every autoequivalence of $Str n Cat_{gaunt}$ restricts to one on  the [[globe category]] $\mathbb{G}_n$ ([B-SP, lemma 4.4](#BarwickSchomerPries)).

1. observe that the only autoequivalences of $\mathbb{G}_n$ are those that reverse the direction of the $k$-morphisms for $1 \leq k \neq n$, which with the above implies the same for all of $Str n Cat_{gaunt}$ ([B-SP, lemma 4.5](#BarwickSchomerPries)).

Now us that, by the [above discussion](#Generators), $Str n Cat_{gaunt}$ generates all of $Cat_{(\infty,n)}$ under [[(∞,1)-colimits]].


=--

### Web of Quillen equivalent model category presentations
 {#WebOfQuillenEquivalences}

We list [[model category]] structures that [[presentable (infinity,1)-category|present]] $Cat_{(\infty,n)}$ and [[Quillen equivalences]] between them.

In the following $A$ is an [[model category]] presenting $Cat_{(\infty,n-1)}$ that is an "absolute distributor" in the sense discussed at _[[category object in an (∞,1)-category]]_. (That includes most of the model structures in the table, so that one can recurse over these constructions.)

| [[model category]] | [[Quillen equivalence]] | [[model category]] | $n$Lab page | literature |
|---|--|---|---|---|
| [[model structure for Segal categories|projective structure for]]  $A$-[[Segal categories]] | $\stackrel{identity}{\leftrightarrow}$ | [[model structure for Segal categories|injective structure for]]  $A$-[[Segal categories]] | | ([Lurie, prop. 2.3.9](#Lurie))|
| [[model structure for Segal categories|projective structure for]]  $A$-[[Segal categories]] | $\stackrel{inclusion}{\leftarrow}$ | $A$-[[enriched categories]] | | [Lurie, theorem 2.2.16](#Lurie) |
| [[model structure for Segal categories|injective structure for]]  $A$-[[Segal categories]] | $\stackrel{UnPre}{\to}$ | [[model structure for complete Segal spaces|complete Segal space objects]] in $A$ | | [Lurie, prop 2.3.1](#Lurie) |
| [[Theta-space|Theta-(n-1)-space]]-[[Segal categories]] | | [[Theta-space|Theta-(n-1)-space]]-[[enriched categories]] | | ([Bergner-Rezk, prop. 7.2](#BergnerRezk)) |
|$\vdots$| |$\vdots$| | |

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

## Extra structure and properties

We discuss extra [[structure]] that an [[(∞,n)-category]] can carry
and extra [[properties]] that it may enjoy.

### $\mathcal{O}$-Monoidal $(\infty,n)$-categories 

* [[monoidal (∞,1)-category]]

* [[symmetric monoidal (∞,n)-category]]

### $(\infty,n)$-Categories with all adjoints

* [[(∞,n)-category with all adjoints]]


## Related concepts

* [[0-category]], [[(0,1)-category]]

* [[category]]

* [[2-category]]

* [[3-category]]

* [[n-category]]

* [[(∞,0)-category]]

* [[(∞,1)-category]]

  * [[table - models for (∞,1)-categories]]

* [[(∞,2)-category]]

* **(∞,n)-category**

  * [[category object in an (∞,1)-category]]

  * [[n-category object in an (∞,1)-category]]

  * [[n-fold complete Segal space]]

  * [[Theta-space]], [[n-quasicategory]], [[model structure on cellular sets]]

  * [[symmetric monoidal (∞,n)-category]]

* [[(n,r)-category]]

* [[(∞,n)-sheaf]], [[(∞,n)-topos]]

* [[directed homotopy type theory]]

## References ##

Definition in terms of [[n-fold complete Segal spaces]] and [[Segal n-categories]] are due to the (unpublished) thesis

* [[Clark Barwick]], _$(\infty,n)$-$Cat$ as a closed model category_ PhD (2005)

The definition in terms of [[Theta spaces]] is due to

* {#Rezk} [[Charles Rezk]], _A cartesian presentation of weak n-categories_ ([arXiv:0901.3602](http://arxiv.org/abs/0901.3602))
 

An iterartive definition in terms of [[n-fold complete Segal spaces]] is given in

* {#Lurie} [[Jacob Lurie]], _$(\infty,2)$-Categories and the Goodwillie Calculus I_ ([arXiv:0905.0462](http://arxiv.org/abs/0905.0462))
 

A summary of definitions and some known comparison results can be found in

* [[Julie Bergner]], _Models for $(\infty,n)$-Categories and the Cobordism Hypothesis_ , in [[Urs Schreiber]], [[Hisham Sati]] (eds.) _[[Mathematical Foundations of Quantum Field and Perturbative String Theory]]_, Proceedings of Symposia in Pure Mathematics, volume 83 
 AMS (2011) ([arXiv:1011.0110](http://arxiv.org/abs/1011.0110))

A textbook account focusing on [[n-fold complete Segal spaces]] and related models is in

* {#Paoli19} [[Simona Paoli]], _Simplicial Methods for Higher Categories -- Segal-type Models of Weak $n$-Categories_, Springer 2019  ([doi:10.1007/978-3-030-05674-2](https://doi.org/10.1007/978-3-030-05674-2), [toc pdf](https://link.springer.com/content/pdf/bfm%3A978-3-030-05674-2%2F1.pdf))


One axiomatic characterization is in 

* {#BarwickSchommerPries} [[Clark Barwick]], [[Chris Schommer-Pries]], *On the Unicity of the Homotopy Theory of Higher Categories*, J. Amer. Math. Soc. **34** (2021) 1011-1058  &lbrack;[arXiv:1112.0040](http://arxiv.org/abs/1112.0040), [slides](http://prezi.com/w0ykkhh5mxak/the-uniqueness-of-the-homotopy-theory-of-higher-categories/), [doi:10.1090/jams/972](https://doi.org/10.1090/jams/972)&rbrack;
 

Comparison of models ($\Theta_{n+1}$-spaces and [[enriched (infinity,1)-categories]] in $\Theta_n$-spaces) is in 

* {#BergnerRezk} [[Julie Bergner]], [[Charles Rezk]], _Comparison of models for $(\infty,n)$-categories_ ([arXiv:1204.2013](http://arxiv.org/abs/1204.2013))
 
* {#BergnerRezk14} [[Julie Bergner]], [[Charles Rezk]], _Comparison of models for $(\infty,n)$-categories II_ ([arXiv:1406.4182](http://arxiv.org/abs/1406.4182))

* [[Rune Haugseng]], *On the equivalence between $\Theta_n$-spaces and iterated Segal spaces*, [arXiv](https://arxiv.org/abs/1604.08480)

* [[Julie Bergner]], _A survey of models for $(\infty,n)$-categories_ ([arXiv:1810.10052](https://arxiv.org/abs/1810.10052))

A model for $(\infty,n)$-categories in terms of [[(∞,1)-sheaves]] on variant of a [[site]] of $n$-[[dimension|dimensional]] [[manifolds]] with [[embeddings]] between them is discussed in 

* [[David Ayala]], [[Nick Rozenblyum]], _Weak $n$-categories are sheaves on iterated submersions of $\leq n$-manifolds_ (in preparation)
 
previewed in

* [[David Ayala]], _Higher categories are sheaves on manifolds_, talk at _[FRG Conference on Topology and Field Theories](http://www.nd.edu/~cmnd/conferences/topology/)_, U. Notre Dame (2012) ([video](http://www.youtube.com/watch?v=8nm2ByS5NnY))

  **Abstract** [[topological chiral homology|Chiral]]/[[factorization homology]] gives a procedure for constructing a [[topological field theory]] from the data of an [[En-algebra]]. I'll explain a mulit-object version of this construction which produces a topological field theory from the data of an $n$-category with adjoints. This construction is a consequence of a more primitive result which asserts an equivalence between [[(infinity,n)-category|n-categories]] with adjoints and "transversality sheaves" on [[framed manifold|framed]] $n$-[[manifolds]] - of which there is an abundance of examples. 

This lends itself to a model of  _[[(∞,n)-category with adjoints]]_. See there for more.

The first globular and algebraic models of $(\infty,n)$-categories is in

* [[Camell Kachour]], Algebraic Definition of weak $(\infty,n)$-Categories, Published in Theory and Applications of Categories (2015), Volume 30, No. 22, pages 775-807: [journal web site](http://tac.mta.ca/tac/volumes/30/22/30-22abs.html)

A model structure using [[complicial sets]] is in

* [[Viktoriya Ozornova]], [[Martina Rovelli]], *Model structures for $(\infty,n)$-categories on (pre)stratified simplicial sets and prestratified simplicial spaces}, Algebr. Geom. Topol. **20** (2020) 1543-1600&lbrack;[arxiv:1809.10621](https://arxiv.org/abs/1809.10621), [doi:10.2140/agt.2020.20.1543](https://doi.org/10.2140/agt.2020.20.1543)&rbrack;


[[!redirects (infinity,r)-category]]
[[!redirects (infinity,k)-category]]
[[!redirects (infinity,r)-categories]]
[[!redirects (infinity,k)-categories]]

[[!redirects (∞,n)-category]]
[[!redirects (∞,n)-categories]]
[[!redirects (infinity,n)-categories]]

[[!redirects (∞,r)-category]]
[[!redirects (∞,r)-categories]]
[[!redirects (∞,k)-category]]
[[!redirects (∞,k)-categories]]