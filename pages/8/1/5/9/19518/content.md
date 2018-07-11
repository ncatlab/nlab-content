
> under construction

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

## Properties

+-- {: .num_remark }
###### Remark

Let $(L \underset{Qu}{\dashv} R)$ be a [[Quillen adjunction]]. 
The following are equivalent: 

1. $(L \underset{Qu}{\dashv} R)$ is both a Quillen reflection and Quillen co-reflection (Def. \ref{QuillenReflection});

1. $(L \underset{Qu}{\dashv} R)$ is a [[Quillen equivalence]].

=--


+-- {: .num_prop}
###### Proposition

Let $(L \underset{Qu}{\dashv} R)$ be a [[Quillen adjunction]] and let

$$
  Ho(\mathcal{C})
    \underoverset
      {\underset{\phantom{AA}\mathbb{R}R\phantom{AA}}{\longrightarrow}}
      {\overset{\mathbb{L}L}{\longleftarrow}}
      {\bot}
  Ho(\mathcal{D})
$$

be the induced [[adjoint pair]] of [[derived functors]] on the [[homotopy category of a model category|homotopy categories]] ([this Prop.](geometry+of+physics+--+categories+and+toposes#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)).

* If $(L \underset{Qu}{\dashv} R)$ is a Quillen reflection, then $(\mathbb{L}L \dashv \mathbb{R}R)$ is a [[reflective subcategory]]-inclusion;

* If $(L \underset{Qu}{\dashv} R)$ is a Quillen coreflection, then $(\mathbb{L}L \dashv \mathbb{R}R)$ is a [[co-reflective subcategory]]-inclusion;

=--

+-- {: .proof}
###### Proof

By the proof of [this Prop.](geometry+of+physics+--+categories+and+toposes#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories), the adjunction hom-isomorphism 

$$
  Hom_{Ho(\mathcal{C})}(\mathbb{L}L(d),c)
    \simeq
  Hom_{Ho(\mathcal{D})}(d,\mathbb{R}R(c))  
$$

of the derived adjunction $(\mathbb{L}L \dashv \mathbb{R}R)$ on homotopy categories is just that of the plain adjunction $(L \dashv R)$ for $Q c$ a [[cofibrant replacement]] and $P d$ a fibrant replacement, quotiented by the homotopy relation:

$$
  \widetilde{(-)}
  \;\colon\;
  Hom_{\mathcal{C}}(L Q d ,P c)/\sim
    \simeq
  Hom_{Ho(\mathcal{D})}(Q d, R P c)/\sim 
$$

Hence the [[adjunction unit]] of the derived adjunction $(\mathbb{L}L \dashv \mathbb{R}R)$ is, up to composition with [[isomorphisms]], the ordinary [[adjunct]] $\widetilde{j_{L Q X}}$ of a [[fibrant replacement]] comparison morphism

$$
  L Q X \underoverset{\in W_{\mathcal{C}}}{j_{L Q X}}{\longrightarrow} P L Q X
  \;\;\;
  \in
  Hom_{\mathcal{C}}(L Q X ,P Y)/\sim
$$

By the formula for [[adjuncts]], this is 

$$
  ...
$$


=--

[[!redirects Quillen reflections]]

[[!redirects Quillen coreflection]]
[[!redirects Quillen coreflections]]

[[!redirects Quillen co-reflection]]
[[!redirects Quillen co-reflections]]

