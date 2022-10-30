
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

In the following we say _[[Top]]-[[enriched category]]_ and _[[Top]]-[[enriched functor]]_ etc. for what often is referred to as "[[topological category]]" and "[[topological functor]]" etc. As discussed there, these latter terms are ambiguous.


+-- {: .num_defn #TopEnrichedCategory}
###### Definition

A **[[topologically enriched category]]** $\mathcal{C}$ is a [[Top]]-[[enriched category]], hence:

1. a [[class]] $Obj(\mathcal{C})$, called the **class of [[objects]]**;

1. for each $a,b\in Obj(\mathcal{C})$ a topological space 

   $$
     \mathcal{C}(a,b)\in Top
     \,,
   $$

   called the **space of [[morphisms]]** or the **[[hom-space]]** between $a$ and $b$;

1. for each $a,b,c\in Obj(\mathcal{C})$ a [[continuous function]]

   $$
     \circ_{a,b,c} \;\colon\; \mathcal{C}(a,b)\times \mathcal{C}(b,c) \longrightarrow \mathcal{C}(a,c)
   $$

   out of the [[product topological space]], called the _[[composition]]_ operation

1. for each $a \in Obj(\mathcal{C})$ a point $Id_a\in \mathcal{C}(a,a)$, called the _[[identity]]_ morphism on $a$

such that the composition is [[associativity|associative]] and [[unitality|unital]].

=--

+-- {: .num_remark #UnderlyingCategoryOfTopEnrichedCategory}
###### Remark

Given a [[topologically enriched category]] as in def. \ref{TopEnrichedCategory}, then forgetting the topology on the [[hom-spaces]] (along the [[forgetful functor]] $U \colon Top_k \to Set$) yields an ordinary [[locally small category]] with

$$
  Hom_{\mathcal{C}}(a,b) = U(\mathcal{C}(a,b))
  \,.
$$

It is in this sense that $\mathcal{C}$ is a category with [[extra structure]], and hence "[[enriched category|enriched]]".
 
=---

The archetypical example is the following:

+-- {: .num_example #TopkAsATopologicallyEnrichedCategory}
###### Example

Write 

$$
  Top_k \hookrightarrow Top
$$ 

for the [[full subcategory]] of [[Top]] on the [[compactly generated topological spaces]]. Under forming [[Cartesian product]] 

$$
  (-)\times (-)
  \;\colon\;
  Top_k \times Top_k \longrightarrow Top_k
$$


and [[mapping spaces]] 

$$
  (-)^{(-)}
  \;\colon\;
  Top_k^{op}\times Top_k
  \longrightarrow
  Top_k
$$

this is a [[cartesian closed category]] (see at _[[convenient category of topological spaces]]_). As such it canonically obtains the structure of a [[topologically enriched category]], def. \ref{TopEnrichedCategory}, with [[hom-spaces]] given by [[mapping spaces]]

$$
  Top_k(X,Y)
  \coloneqq
  Y^X
$$

and with [[composition]] 

$$
  Y^X \times Z^Y
  \longrightarrow
  Z^X
$$

given by the (product$\dashv$ mapping-space)-[[adjunct]] of the [[evaluation morphism]]

$$
  X \times Y^X \times Z^Y
  \overset{(ev, id)}{\longrightarrow}
  Y \times Z^Y
  \overset{ev}{\longrightarrow}
  Z
  \,.
$$

=--

+-- {: .num_defn #TopologicallyEnrichedFunctor}
###### Definition

A [[topologically enriched functor]] between two [[topologically enriched categories]] 

$$
  F \;\colon\;  \mathcal{C}  \longrightarrow \mathcal{D}
$$

is a [[Top]]-[[enriched functor]], hence:

1. a [[function]]

   $$
     F_0 \colon Obj(\mathcal{C}) \longrightarrow Obj(\mathcal{D})
   $$

   of [[objects]];

1. for each $a,b \in Obj(\mathcal{C})$ a [[continuous function]]

   $$
     F_{a,b} \;\colon\; \mathcal{C}(a,b) \longrightarrow \mathcal{D}(F_0(a), F_0(b))
   $$

   of [[hom-spaces]]

such that this preserves [[composition]] and [[identity]] morphisms in the evident sense.

A [[homomorphism]] of topologically enriched functors $F \Rightarrow G$ is a [[Top]]-[[enriched natural transformation]], which is just a [[natural transformation]] of the underlying ordinary functors.

We write $[\mathcal{C}, \mathcal{D}]$ for the resulting category of topologically enriched functors. This itself naturally obtains the structure of [[topologically enriched category]], see at _[[enriched functor category]]_.

=--

## Topologically enriched presheaves

+-- {: .num_example #TopologicallyEnrichedFunctorsToTopk}
###### Example

For $\mathcal{C}$ any topologically enriched category, def. \ref{TopEnrichedCategory} then a topologiclly enriched functor

$$
  F \;\colon\; \mathcal{C} \longrightarrow Top_k
$$

to the archetical topologically enriched category from example \ref{TopkAsATopologicallyEnrichedCategory} may be thought of as a topologically enriched [[copresheaf]], at least if $\mathcal{C}$ is [[small category|small]] (in that its [[class]] of objects is a proper [[set]]).

Such a functor is equivalently 

* a [[compactly generated topological space]] $F_a\in Top_k$ for each object $a \in Obj(\mathcal{C})$;

* a [[continuous function]]

  $$
     F_a \times \mathcal{C}(a,b) \longrightarrow F_b
  $$

  for all pairs of objects $a,b \in Obj(\mathcal{C})$

such that composition is respected, in the evident sense.

For every object $c \in \mathcal{C}$, there is a topologically enriched [[representable functor]], denoted $y(c) or \mathcal{C}(c,-)$ which sends objects to 

$$
  y(c)(d) = \mathcal{C}(c,d) \in Top
$$

and whose action on morphisms is, under the above identification, just the [[composition]] operation in $\mathcal{C}$.


=--

+-- {: .num_remark}
###### Remark

With $Top_k$ equipped with the [[classical model structure on topological spaces]], which is a [[locally presentable (∞,1)-category|presentation]] for the archetypical [[(∞,1)-category]] [[∞Grpd]] of [[∞-groupoids]], then the topological functor category

$$
  [\mathcal{C},Top_k]
$$

(def. \ref{TopologicallyEnrichedFunctor}, def. \ref{TopkAsATopologicallyEnrichedCategory}) is a model for the [[(∞,1)-category of (∞,1)-presheaves]] on $\mathcal{C}^{op}$. This is made precise by the _[[model structure on enriched functors]]_, $[\mathcal{C},Top_{Quillen}]_{proj}$. See at _[classical model structure on topological spaces -- Model structure on functors](classical+model+structure+on+topological+spaces#ModelStructureOnTopEnrichedFunctors)_ for details.

=--


## Related concepts

* [[simplicially enriched category]]

* [[model structure on enriched functors]]

* [[(infinity,1)-category]]

[[!redirects topologically enriched categories]]

[[!redirects Top-enriched category]]
[[!redirects Top-enriched categories]]

[[!redirects topologically enriched functor]]
[[!redirects topologically enriched functors]]

[[!redirects Top-enriched functor]]
[[!redirects Top-enriched functors]]
