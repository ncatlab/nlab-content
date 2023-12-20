
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


+-- {: .num_defn #kTop}
###### Definition

Write 

$$
  Top_{cg} \hookrightarrow Top
$$ 

for the [[full subcategory]] of [[Top]] on the [[compactly generated topological spaces]]. Under forming [[Cartesian product]] 

$$
  (-)\times (-)
  \;\colon\;
  Top_{cg} \times Top_{cg} \longrightarrow Top_{cg}
$$


and compactly generated [[mapping spaces]] 

$$
  (-)^{(-)}
  \;\colon\;
  Top_{cg}^{op}\times Top_{cg}
  \longrightarrow
  Top_{cg}
$$

this is a [[cartesian closed category]] (see at _[[convenient category of 
topological spaces]]_). 

=--

+-- {: .num_defn #TopEnrichedCategory}
###### Definition

A **[[topologically enriched category]]** $\mathcal{C}$ is a $Top_{cg}$-[[enriched category]], hence:

1. a [[class]] $Obj(\mathcal{C})$, called the **class of [[objects]]**;

1. for each $a,b\in Obj(\mathcal{C})$ a [[compactly generated topological space]]

   $$
     \mathcal{C}(a,b)\in Top_{cg}
     \,,
   $$

   called the **space of [[morphisms]]** or the **[[hom-space]]** between $a$ and $b$;

1. for each $a,b,c\in Obj(\mathcal{C})$ a [[continuous function]]

   $$
     \circ_{a,b,c} \;\colon\; \mathcal{C}(a,b)\times \mathcal{C}(b,c) \longrightarrow \mathcal{C}(a,c)
   $$

   out of the cartesian product, called the _[[composition]]_ operation

1. for each $a \in Obj(\mathcal{C})$ a point $id_a\in \mathcal{C}(a,a)$, called the _[[identity]]_ morphism on $a$

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
 
=--

The archetypical example is the following:

+-- {: .num_example #TopkAsATopologicallyEnrichedCategory}
###### Example

The category $Top_{cg}$ from def. \ref{kTop} itself, being a [[cartesian closed category]], canonically obtains the structure of a [[topologically enriched category]], def. \ref{TopEnrichedCategory}, with [[hom-spaces]] given by compactly generated [[mapping spaces]]

$$
  Top_{cg}(X,Y)
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

is a $Top_{cg}$-[[enriched functor]], hence:

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

A [[homomorphism]] of topologically enriched functors 

$$
  \eta \;\colon\; F \Rightarrow G
$$ 

is a $Top_{cg}$-[[enriched natural transformation]]: for each $c \in Obj(\mathcal{C})$ a choice of morphism $\eta_c \in \mathcal{D}(F(c),G(c))$ such that for each pair of objects $c,d \in \mathcal{C}$ the two continuous functions 

$$
  \eta_d \circ F(-) \;\colon\; \mathcal{C}(c,d) \longrightarrow \mathcal{D}(F(c), G(d))
$$

and

$$
  G(-) \circ \eta_c \;\colon\; \mathcal{C}(c,d) \longrightarrow \mathcal{D}(F(c), G(d))
$$

agree.

We write $[\mathcal{C}, \mathcal{D}]$ for the resulting category of topologically enriched functors. This itself naturally obtains the structure of [[topologically enriched category]], see at _[[enriched functor category]]_.

=--

## Topologically enriched presheaves

+-- {: .num_example #TopologicallyEnrichedFunctorsToTopk}
###### Example

For $\mathcal{C}$ any topologically enriched category, def. \ref{TopEnrichedCategory} then a topologically enriched functor

$$
  F \;\colon\; \mathcal{C} \longrightarrow Top_{cg}
$$

to the archetypical topologically enriched category from example \ref{TopkAsATopologicallyEnrichedCategory} may be thought of as a topologically [[enriched presheaf|enriched]] [[copresheaf]], at least if $\mathcal{C}$ is [[small category|small]] (in that its [[class]] of objects is a proper [[set]]).

Hence the category of topologically enriched functors

$$
  [\mathcal{C}, Top_{cg}] 
$$

according to def. \ref{TopologicallyEnrichedFunctor} may be thought of as the ([[copresheaf|co-]])[[presheaf category]] over $\mathcal{C}$ in the realm of topologically enriched categories.

A functor $F \in [\mathcal{C}, Top_{cg}]$ is equivalently 

* a [[compactly generated topological space]] $F_a\in Top_{cg}$ for each object $a \in Obj(\mathcal{C})$;

* a [[continuous function]]

  $$
     F_a \times \mathcal{C}(a,b) \longrightarrow F_b
  $$

  for all pairs of objects $a,b \in Obj(\mathcal{C})$

such that composition is respected, in the evident sense.

For every object $c \in \mathcal{C}$, there is a topologically enriched [[representable functor]], denoted $y(c)$ or $\mathcal{C}(c,-)$ which sends objects to 

$$
  y(c)(d) = \mathcal{C}(c,d) \in Top_{cg}
$$

and whose action on morphisms is, under the above identification, just the [[composition]] operation in $\mathcal{C}$.

=--

There is a full blown $Top_{cg}$-[[enriched Yoneda lemma]]. The following records a slightly simplified version.

+-- {: .num_prop #TopologicallyEnrichedYonedaLemma} 
###### Proposition
**(topologically enriched Yoneda-lemma)**

Let $\mathcal{C}$ be a [[topologically enriched category]], def. \ref{TopEnrichedCategory}, write $[\mathcal{C}, Top_{cg}]$ for its category of topologically enriched (co-)presheaves, and for $c\in Obj(\mathcal{C})$ write $y(c) = \mathcal{C}(c,-) \in [\mathcal{C}, Top_k]$ for the topologically enriched functor that it represents, all according to example \ref{TopologicallyEnrichedFunctorsToTopk}. Recall also the $Top_{cg}$-tensored functors $F \cdot X$ from that example.

For $c\in Obj(\mathcal{C})$, $X \in Top_{cg}$ and $F \in [\mathcal{C}, Top_{cg}]$, there is a [[natural bijection]] between 

1. morphisms $y(c) \cdot X \longrightarrow F$ in $[\mathcal{C}, Top_{cg}]$;

1. morphisms $X \longrightarrow F(c)$ in $Top_{cg}$.

=--

+-- {: .proof}
###### Proof

Given a morphism $\eta \colon y(c) \cdot X \longrightarrow F$ consider its component

$$
  \eta_c \;\colon\; \mathcal{C}(c,c)\times X \longrightarrow F(c)
$$

and restrict that to the identity morphism $id_c \in \mathcal{C}(c,c)$ in the first argument

$$
  \eta_c(id_c,-) \;\colon\; X \longrightarrow F(c)
  \,.
$$

We claim that just this $\eta_c(id_c,-)$ already uniquely determines all components 

$$
  \eta_d \;\colon\; \mathcal{C}(c,d)\times X \longrightarrow F(d)
$$

of $\eta$, for all $d \in Obj(\mathcal{C})$: By definition of the transformation $\eta$ (def. \ref{TopologicallyEnrichedFunctor}), the two functions

$$
   F(-) \circ \eta_c
  \;\colon\;
  \mathcal{C}(c,d)
  \longrightarrow
  F(d)^{\mathcal{C}(c,c) \times X}
$$

and

$$
  \eta_d  \circ \mathcal{C}(c,-) \times X
  \;\colon\;
  \mathcal{C}(c,d)
  \longrightarrow
  F(d)^{\mathcal{C}(c,c) \times X}
$$

agree. This means that they may be thought of jointly as a function with values in commuting squares in $Top$ of this form:

$$
  f
  \;\;\;\;
  \mapsto
  \;\;\;\;
  \array{
    \mathcal{C}(c,c) \times X &\overset{\eta_c}{\longrightarrow}& F(c)
    \\
    {}^{\mathllap{\mathcal{C}(c,f)}}\downarrow && \downarrow^{\mathrlap{F(f)}}
    \\
    \mathcal{C}(c,d) \times X &\underset{\eta_d}{\longrightarrow}& F(d)
  }
$$

For any $f \in \mathcal{C}(c,d)$, consider the restriction of

$$
  \eta_d \circ \mathcal{C}(c,f) \in F(d)^{\mathcal{C}(c,c) \times X}
$$

to $id_c \in \mathcal{C}(c,c)$, hence restricting the above commuting squares to

$$
  f
  \;\;\;\;
  \mapsto
  \;\;\;\;
  \array{
    \{id_c\} \times X &\overset{\eta_c}{\longrightarrow}& F(c)
    \\
    {}^{\mathllap{\mathcal{C}(c,f)}}\downarrow && \downarrow^{\mathrlap{F}(f)}
    \\
    \{f\} \times X &\underset{\eta_d}{\longrightarrow}& F(d)
  }
$$

This shows that $\eta_d$ is fixed to be the function

$$
  \eta_d(f,x) = F(f)\circ \eta_c(id_c,x)
$$

and this is a continuous function since all the operations it is built from are continuous.

Conversely, given a continuous function $\alpha \colon X \longrightarrow F(c)$, define for each $d$ the function

$$
  \eta_d \colon (f,x) \mapsto F(f) \circ \alpha
  \,.
$$

Running the above analysis backwards shows that this determines a transformation $\eta \colon y(c)\times X \to F$.


=--


+-- {: .num_remark}
###### Remark

With $Top_{cg}$ equipped with the [[classical model structure on topological spaces]], which is a [[locally presentable (∞,1)-category|presentation]] for the archetypical [[(∞,1)-category]] [[∞Grpd]] of [[∞-groupoids]], then the topological functor category

$$
  [\mathcal{C},Top_{cg}]
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

[[!redirects pointed topologically enriched category]]
[[!redirects pointed topologically enriched categories]]

[[!redirects pointed topologically enriched functor]]
[[!redirects pointed topologically enriched functors]]

