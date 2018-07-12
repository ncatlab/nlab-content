

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The analog of a [[reflective subcategory]]-inclusion as [[adjoint functor|adjunctions of functors]] are replaced by [[Quillen adjunctions]].

## Definition

+-- {: .num_defn #QuillenReflection}
###### Definition

Let $\mathcal{C}$ and $\mathcal{D}$ be [[model categories]], and let

$$
  \mathcal{C}  
    \underoverset
      {\underset{\phantom{AA}R\phantom{AA}}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot_{Qu}}
  \mathcal{D}
$$

be a [[Quillen adjunction]] between them. Then this may be called 

1. a _Quillen reflection_ if the [[derived adjunction counit]] is componentwise a [[weak equivalence]];

1. a _Quillen co-reflection_ if the [[derived adjunction unit]] is componentwise a [[weak equivalence]].

=--

+-- {: .num_example #BousfieldLocalizationIsQuillenReflection}
###### Example
**([[left Bousfield localization]] is [[Quillen reflection]])**

1. A [[left Bousfield localization]] is a Quillen reflection.

1. A [[right Bousfield localization]] is a Quillen coreflection.

=--

+-- {: .proof}
###### Proof

We consider the case of [[left Bousfield localizations]], the other case is [[formal duality|formally dual]].

A left Bousfield localization is a [[Quillen adjunction]] by [[identity functors]] ([this Remark](Bousfield+localization+of+model+categories#ImmediateImpiciationsOfLeftBousfieldLocalization))

$$
  \mathcal{D}_{loc}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {{}_{\phantom{Qu}} \bot_{Qu}}
  \mathcal{D}
$$

This means that the ordinary [[adjunction counit]] is the [[identity morphism]] and hence that the [[derived adjunction counit]] on a [[fibrant object]] $c$ is just a [[cofibrant resolution]]-morphism 

$$
  Q(c) \underoverset{ \in W_{\mathcal{D}} \cap Fib_{\mathcal{D}} }{p_c}{\longrightarrow} c
$$

but regarded in the model structure $\mathcal{D}_{loc}$. Hence it is sufficient to see that [[acyclic fibrations]] in $\mathcal{D}$ remain weak equivalences in the left Bousfield localized model structure. In fact they even remain acyclic fibrations, by [this Remark](Bousfield+localization+of+model+categories#ImmediateImpiciationsOfLeftBousfieldLocalization).

=--




## Properties

+-- {: .num_prop }
###### Proposition

Let

$$
  \mathcal{C}  
    \underoverset
      {\underset{\phantom{AA}R\phantom{AA}}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot_{Qu}}
  \mathcal{D}
$$

be a [[Quillen adjunction]] and write

$$
  Ho(\mathcal{C})
    \underoverset
      {\underset{\phantom{AA}\mathbb{R}R\phantom{AA}}{\longrightarrow}}
      {\overset{\mathbb{L}L}{\longleftarrow}}
      {\bot_{Qu}}
  Ho(\mathcal{D})
$$

for the induced [[adjoint pair]] of [[derived functors]] on the [[homotopy category of a model category|homotopy categories]] ([this Prop.](geometry+of+physics+--+categories+and+toposes#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)).

Then 

1. $(L \underset{Qu}{\dashv} R)$ is a Quillen reflection precisely if $(\mathbb{L}L \dashv \mathbb{R}R)$ is a [[reflective subcategory]]-inclusion;

1. $(L \underset{Qu}{\dashv} R)$ is a Quillen co-reflection precisely if $(\mathbb{L}L \dashv \mathbb{R}R)$ is a [[co-reflective subcategory]]-inclusion;

1. $(L \underset{Qu}{\dashv} R)$ is a [[Quillen equivalence]] precisely if $(\mathbb{L}L \dashv \mathbb{R}R)$ is an [[equivalence of categories]].

=--


+-- {: .proof}
###### Proof

By [this Prop.](geometry+of+physics+--+categories+and+toposes#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories) the components of the [[adjunction unit]]/[[adjunction counit|counit]] of $(\mathbb{L}L \dashv \mathbb{R}R)$ are precisely the images under [[localization]] of the [[derived adjunction unit]]/[[derived adjunction counit|counit]] of $(L \underset{Qu}{\dashv} R)$. Moreover, by [this Prop.](geometry+of+physics+--+categories+and+toposes#MorphismIsWeakEquivalenceIfIsoInHomotopyCategoryForQuillen) the localization functor of a [[model category]] inverts precisely the [[weak equivalences]]. Hence the adjunction (co-)unit of $(\mathbb{L}L \dashv \mathbb{R}R)$ is an isomorphism if and only if the derived (co-)unit of $(L \underset{Qu}{\dashv} R)$ is a weak equivalence, respectively.

With this the statement reduces to the characterization of (co-)reflections via invertible units/counits, respectively ([this Prop.](adjoint+functor#FullyFaithfulAndInvertibleAdjoints)).

=--

[[!redirects Quillen reflections]]

[[!redirects Quillen coreflection]]
[[!redirects Quillen coreflections]]

[[!redirects Quillen co-reflection]]
[[!redirects Quillen co-reflections]]

