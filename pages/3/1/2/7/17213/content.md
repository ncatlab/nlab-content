[[!redirects functor with smash product]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In suitable "[[coordinate-free spectrum|coordinate-free]]" presentations of [[spectra]], the structure of a ([[commutative monoid|commutative]]) [[monoid]] with respect to the [[smash product of spectra]] (an [[A-infinity ring]] ([[E-infinity ring]])) may be expressed directly as a [[lax monoidal functor]] on the indexing spaces, hence a functor that intertwines the [[smash product]] of indexing spaces with that of the component spaces, but without explicitly mentioning the [[smash product of spectra]].

### General

So a _functor with smash products_ is a suitably well behaved functor

$$
  E \;\colon\; \mathcal{D} \longrightarrow Spaces^{\ast/}
$$

from a [[monoidal category]] $(\mathcal{D},\wedge)$ to [[pointed topological spaces]]/[[pointed simplicial sets]] and equipped with [[natural transformations]] 

$$
  \mathbb{S}(V) \longrightarrow E(V)
$$

and

$$
  E(V) \wedge E(W) \longrightarrow E(V \wedge W)
$$

that are [[associativity|associative]] and [[unitality|unital]] in the evident sense.


### For highly structured spectra

For the case of [[highly structured spectra]] such as [[orthogonal spectra]], [[symmetric spectra]] and [[S-modules]], the equivalence of FSPs with monoids with respect to the [[symmetric smash product of spectra]] is due to [this proposition](Day+convolution#DayMonoidsAreLaxMonoidalFunctorsOnTheSite) at _[[Day convolution]]_.
([MMSS 00, prop. 22.1, prop. 22.6](#MMSS00)).

(For instance accounts such as ([Kochmann 96, section 3.3](Adams+category#Kochmann96),  [Schwede 14](orthogonal%20spectrum#Schwede14)) follow this perspective and define [[ring spectra]] first as FSPs, before or introducing the smash product on spectra)

### For excisive functors

For the monoidal [[model structure]] for excisive functors, the fact that monoids with respect to the [[symmetric smash product of spectra]] are equivalently FSPs is discussed in ([Lydakis 98, remark 5.12](#Lydakis98)). See [this proposition](model+structure+for+excisive+functors#MonoidsInLydakisModelStructureAreFSP).

## Details


### Topological ends and coends
 {#TopologicalEndsAndCoends}

For working with pointed [[topologically enriched functors]], a certain shape of [[limits]]/[[colimits]] is particularly relevant: these are called (pointed topological enriched) _[[ends]]_ and _[[coends]]_. We here introduce these and then derive some of their basic properties, such as notably the expression for topological [[left Kan extension]] in terms of [[coends]] (prop. \ref{TopologicalLeftKanExtensionBCoend} below). Below in (...) it is via left Kan extension along the ordinary smash product of pointed topological spaces ("[[Day convolution]]") that the [[symmetric monoidal smash product of spectra]] is induced.

+-- {: .num_defn #OppositeAndProductOfPointedTopologicallyEnrichedCategory}
###### Definition

Let $\mathcal{C}, \mathcal{D}$ be pointed [[topologically enriched categories]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)), i.e. [[enriched categories]] over $(Top_{cg}^{\ast/}, \wedge, S^0)$ from example \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}. 

1. The **pointed topologically enriched [[opposite category]]** $\mathcal{C}^{op}$ is the [[topologically enriched category]] with the same [[objects]] as $\mathcal{C}$, with [[hom-spaces]]

   $$
     \mathcal{C}^{op}(X,Y)
     \coloneqq
     \mathcal{C}(Y,X) 
   $$

   and with [[composition]] given by [[braiding]] followed by the composition in $\mathcal{C}$:

   $$
     \mathcal{C}^{op}(X,Y)
     \wedge
     \mathcal{C}^{op}(Y,Z)
     =
     \mathcal{C}(Y,X)\wedge \mathcal{C}(Z,Y)
     \underoverset{\simeq}{\tau}{\longrightarrow}
     \mathcal{C}(Z,Y) \wedge \mathcal{C}(Y,X)
       \overset{\circ_{Z,Y,X}}{\longrightarrow}
     \mathcal{C}(Z,X)
     =
     \mathcal{C}^{op}(X,Z) 
     \,.
   $$

1. the **pointed topological [[product category]]** $\mathcal{C} \times \mathcal{D}$ is the [[topologically enriched category]] whose [[objects]] are [[pairs]] of objects $(c,d)$ with $c \in \mathcal{C}$ and $d\in \mathcal{D}$, whose [[hom-spaces]] are the [[smash product]] of the separate hom-spaces

   $$
     (\mathcal{C}\times \mathcal{D})((c_1,d_1),\;(c_2,d_2) )
       \coloneqq
     \mathcal{C}(c_1,c_2)\wedge \mathcal{D}(d_1,d_2)
   $$

   and whose [[composition]] operation is the [[braiding]] followed by the [[smash product]] of the separate composition operations:

   $$
     \array{
       (\mathcal{C}\times \mathcal{D})((c_1,d_1), \; (c_2,d_2))
         \wedge
       (\mathcal{C}\times \mathcal{D})((c_2,d_2), \; (c_3,d_3))
       \\
       {}^{\mathllap{=}}\downarrow
       \\
       \left(\mathcal{C}(c_1,c_2) \wedge \mathcal{D}(d_1,d_2)\right)
         \wedge
       \left(\mathcal{C}(c_2,c_3) \wedge \mathcal{D}(d_2,d_3)\right)
       \\
       \downarrow^{\mathrlap{\tau}}_{\mathrlap{\simeq}}
       \\
       \left(\mathcal{C}(c_1,c_2)\wedge \mathcal{C}(c_2,c_3)\right)
         \wedge
       \left( \mathcal{D}(d_1,d_2)\wedge \mathcal{D}(d_2,d_3)\right)
         &\overset{
             (\circ_{c_1,c_2,c_3})\wedge (\circ_{d_1,d_2,d_3})
           }{\longrightarrow}
         &
       \mathcal{C}(c_1,c_3)\wedge \mathcal{D}(d_1,d_3)
       \\
       && \downarrow^{\mathrlap{=}}
       \\
       && (\mathcal{C}\times \mathcal{D})((c_1,d_1),\; (c_3,d_3))
     }
    \,.
   $$

=--

+-- {: .num_example #PointedTopologicalFunctorOnProductCategory}
###### Example

A pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) into $Top^{\ast/}_{cg}$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctorsToTopk)) out of a pointed topological [[product category]] as in def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory} 

$$
  F 
    \;\colon\;
  \mathcal{C} \times \mathcal{D}
    \longrightarrow
  Top^{\ast/}_{cg}
$$

(a "pointed topological [[bifunctor]]") has component maps of the form

$$
  F_{(c_1,d_1),(c_2,d_2)}
    \;\colon\;
  \mathcal{C}(c_1,c_2)
  \wedge
  \mathcal{D}(d_1,d_2)
    \longrightarrow
  Maps(F_0((c_1,d_1)),F_0((c_2,d_2)))_\ast
  \,.
$$

By functoriallity and under passing to [[adjuncts]] ([cor.](Introduction+to+Stable+homotopy+theory+--+P#SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces)) this is equivalent to two commuting _[[actions]]_


$$
  \rho_{c_1,c_2}(d)
   \;\colon\;
  \mathcal{C}(c_1,c_2) \wedge F_0((c_1,d)) 
    \longrightarrow
  F_0((c_2,d))
$$

and

$$
  \rho_{d_1,d_2}(c)
    \;\colon\;
  \mathcal{D}(d_1,d_2) \wedge F_0((c,d_1))
    \longrightarrow
  F_0((c,d_2))
  \,.
$$

In the special case of a functor out of the [[product category]] of some $\mathcal{C}$ with its [[opposite category]] (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory})

$$
  F 
    \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  Top^{\ast/}_{cg}
$$

then this takes the form

$$
  \rho_{c_2,c_1}(d)
   \;\colon\;
  \mathcal{C}(c_1,c_2) \wedge F_0((c_2,d)) 
    \longrightarrow
  F_0((c_1,d))
$$

and

$$
  \rho_{d_1,d_2}(c)
    \;\colon\;
  \mathcal{C}(d_1,d_2) \wedge F_0((c,d_1))
    \longrightarrow
  F_0((c,d_2))
  \,.
$$


=--


+-- {: .num_defn #EndAndCoendInTopcgSmash}
###### Definition

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)), i.e. an [[enriched category]] over $(Top_{cg}^{\ast/}, \wedge, S^0)$ from example \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}. Let

$$
  F 
    \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  Top^{\ast/}_{cg}
$$

be a pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) out of the pointed topological [[product category]] of $\mathcal{C}$ with its [[opposite category]], according to def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}.


1. The  **[[coend]]** of $F$, denoted $\overset{c \in \mathcal{C}}{\int} F(c,c)$, is the [[coequalizer]] in $Top_{cg}^{\ast}$ ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop), [exmpl.](Introduction+to+Stable+homotopy+theory+--+P#CoequalizerInTop), [prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects), [cor.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)) of the two actions encoded in $F$ via example \ref{PointedTopologicalFunctorOnProductCategory}:

   $$
     \underset{c,d \in \mathcal{C})}{\coprod} \mathcal{C}(c,d) \wedge F(c,d)
      \underoverset
        {\underset{\underset{c,d}{\sqcup} \rho_{(d,c)}(c) }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} \rho_{(c,d)}(d) }{\longrightarrow}}
        {\phantom{AAAAAAAA}}
     \underset{c \in \mathcal{C}}{\coprod} F(c,c)
      \overset{coeq}{\longrightarrow}
     \overset{c\in \mathcal{C}}{\int} F(c,c)
     \,.
   $$

1. The **[[end]]** of $F$, denoted $\underset{c\in \mathcal{C}}{\int} F(c,c)$, is the **[[equalizer]]** in $Top_{cg}^{\ast/}$ ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop), [exmpl.](Introduction+to+Stable+homotopy+theory+--+P#EqualizerInTop), [prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects), [cor.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)) of the [[adjuncts]] of the two actions encoded in $F$ via example \ref{PointedTopologicalFunctorOnProductCategory}:

   $$
     \underset{c\in \mathcal{C}}{\int} F(c,c)
       \overset{\;\;equ\;\;}{\longrightarrow}
     \underset{c \in \mathcal{C}}{\prod} F(c,c)
      \underoverset   
        {\underset{\underset{c,d}{\sqcup} \tilde \rho_{(c,d)}(d)  }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} \tilde\rho_{d,c}(c)}{\longrightarrow}}
        {\phantom{AAAAAAAA}}
      \underset{c\in \mathcal{C}}{\prod}
      Maps\left( \mathcal{C}\left(c,d\right), \;  F\left(c,d\right) \right)_\ast
     \,.
   $$

=--

+-- {: .num_example #NaturalTransformationsViaEnds}
###### Example

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). For 
$
  F,G
  \;\colon\;
  \mathcal{C}
    \longrightarrow
  Top^{\ast/}_{cg}
$
two pointed [[topologically enriched functors]], then the [[end]] (def. \ref{EndAndCoendInTopcgSmash}) of $Maps(F(-),G(-))_\ast$ is a topological space whose underlying [[pointed set]] is the pointed set of [[natural transformations]] $F\to G$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor))

$$
  U
  \left(
    \underset{c \in \mathcal{C}}{\int} Maps(F(c),G(c))_\ast
  \right)
  \;\simeq\;
  Hom_{[\mathcal{C},Top^{\ast/}_{cg}]}(F,G)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The underlying pointed set functor $U\colon Top^{\ast/}_{cg}\to Set^{\ast/}$ [[preserved limit|preserves]] all [[limits]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop), [prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects), [prop.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)). Therefore there is an [[equalizer]] diagram in $Set^{\ast/}$ of the form

$$
  U
  \left(
    \underset{c\in \mathcal{C}}{\int}
    Maps(F(c),G(c))_\ast
  \right)
    \overset{equ}{\longrightarrow}
  \underset{c\in \mathcal{C}}{\prod} Hom_{Top^{\ast/}_{cg}}(F(c),G(c))
      \underoverset   
        {\underset{\underset{c,d}{\sqcup} U(\tilde \rho_{(c,d)}(d))  }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} U(\tilde\rho_{d,c}(c))}{\longrightarrow}}
        {\phantom{AAAAAAAA}}
   \underset{c,d\in \mathcal{C}}{\prod}
    Hom_{Top^{\ast/}_{cg}}(
      \mathcal{C}(c,d),
      Maps(F(c),G(d))_\ast
    )
  \,.
$$

Here the object in the middle is just the set of collections of component morphisms $\left\{ F(c)\overset{\eta_c}{\to} G(c)\right\}_{c\in \mathcal{C}}$. The two parallel maps in the equalizer diagram take such a collection to the functions which send any $c \overset{f}{\to} d$ to the result of precomposing

$$
  \array{
    F(c)
    \\
    {}^{\mathllap{f(f)}}\downarrow
    \\
    F(d) &\underset{\eta_d}{\longrightarrow}& G(d)
  }
$$

and of postcomposing

$$
  \array{
    F(c) &\overset{\eta_c}{\longrightarrow}& G(c)
    \\
    && \downarrow^{\mathrlap{G(f)}}
    \\
    && G(d)
  }
$$

each component in such a collection, respectively. These two functions being equal, hence the collection $\{\eta_c\}_{c\in \mathcal{C}}$ being in the equalizer, means precisley that for all $c,d$ and all $f\colon c \to d$ the square

$$
  \array{
    F(c) &\overset{\eta_c}{\longrightarrow}& G(c)
    \\
    {}^{\mathllap{F(f)}}\downarrow && \downarrow^{\mathrlap{G(f)}}
    \\
    F(d) &\underset{\eta_d}{\longrightarrow}& G(g)
  }
$$

is a [[commuting square]]. This is precisley the condition that the collection $\{\eta_c\}_{c\in \mathcal{C}}$ be a [[natural transformation]].

=--

Conversely, example \ref{NaturalTransformationsViaEnds} says that [[ends]] over [[bifunctors]] of the form $Maps(F(-),G(-)))_\ast$ constitute [[hom-spaces]] between pointed [[topologically enriched functors]]:

+-- {: .num_defn #PointedTopologicalFunctorCategory}
###### Definition

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched categories]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). Define the structure of a pointed [[topologically enriched category]] on the category $[\mathcal{C}, Top_{cg}^{\ast/}]$ of pointed [[topologically enriched functors]] to $Top^{\ast/}_{cg}$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctorsToTopk)) by taking the [[hom-spaces]] to be given by the [[ends]] (def. \ref{EndAndCoendInTopcgSmash}) of example \ref{NaturalTransformationsViaEnds}:

$$
  [\mathcal{C},Top^{\ast/}_{cg}](F,G)
    \;\coloneqq\;
  \int_{c\in \mathcal{C}} Maps(F(c),G(c))_\ast
$$

and by taking the composition maps to be the morphisms induced by the maps

$$
  \left(
    \underset{c\in \mathcal{C}}{\int} Maps(F(c),G(c))_\ast
  \right)
  \wedge
  \left(
    \underset{c \in \mathcal{C}}{\int} Maps(G(c),H(c))_\ast
  \right)
    \overset{}{\longrightarrow}
  \underset{c\in \mathcal{C}}{\prod}
    Maps(F(c),G(c))_\ast \wedge Maps(G(c),H(c))_\ast
  \overset{(\circ_{F(c),G(c),H(c)})_{c\in \mathcal{C}}}{\longrightarrow}
  \underset{c \in \mathcal{C}}{\prod}
    Maps(F(c),H(c))_\ast
$$

by observing that these equalize the two actions in the definition of the [[end]].

The resulting pointed [[topologically enriched category]] $[\mathcal{C},Top^{\ast/}_{cg}]$ is also called the **$Top^{\ast/}_{cg}$-[[enriched functor category]]** over $\mathcal{C}$ with coefficients in $Top^{\ast/}_{cg}$.

=--

First of all this yields a concise statement of the pointed topologically [[enriched Yoneda lemma]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedYonedaLemma))

+-- {: .num_prop #YonedaReductionTopological}
###### Proposition
**(topologically [[enriched Yoneda lemma]])**

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched categories]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). For $F \colon \mathcal{C}\to Top^{\ast/}_{cg}$ a pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) and for $c\in \mathcal{C}$ an object, there is a [[natural isomorphism]]

$$
  [\mathcal{C}, Top^{\ast/}_{cg}](\mathcal{C}(c,-),\; F)
  \;\simeq\;
  F(c)
$$

between the [[hom-space]] of the pointed topological functor category, according to def. \ref{PointedTopologicalFunctorCategory}, from the [[representable functor|functor represented]] by $c$ to $F$, and the value of $F$ on $c$.

In terms of the [[ends]] (def. \ref{EndAndCoendInTopcgSmash}) defining these [[hom-spaces]], this means that

$$
  \underset{d\in \mathcal{C}}{\int} Maps(\mathcal{C}(c,d), F(d))_\ast
    \;\simeq\;
  F(c)
  \,.
$$

In this form the statement is also known as **[[Yoneda reduction]]**.

=--

The **proof** of prop. \ref{YonedaReductionTopological} is essentially dual to the proof of the next prop. \ref{TopologicalCoYonedaLemma}.

Now that [[natural transformations]] are phrased in terms of [[ends]] (example \ref{NaturalTransformationsViaEnds}), as is the Yoneda lemma (prop. \ref{YonedaReductionTopological}), it is natural to consider the [[formal duality|dual]] statement involvng [[coends]]:

+-- {: .num_prop #TopologicalCoYonedaLemma}
###### Proposition
**([[co-Yoneda lemma]])**

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched categories]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). For $F \colon \mathcal{C}\to Top^{\ast/}_{cg}$ a pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) and for $c\in \mathcal{C}$ an object, there is a [[natural isomorphism]]

$$
  F(-)
    \simeq
  \overset{c \in \mathcal{C}}{\int}
  \mathcal{C}(c,-) \wedge F(c)
  \,.
$$

Moreover, the morphism that hence exhibits $F(c)$ as the [[coequalizer]] of the two morphisms in def. \ref{EndAndCoendInTopcgSmash} is componentwise the canonical action 

$$
  \mathcal{C}(d,c) \wedge F(c)
   \longrightarrow
  F(d)
$$

which is [[adjunct]] to the component map $\mathcal{C}(d,c) \to Maps(F(c),F(d))_{\ast}$ of the [[topologically enriched functor]] $F$.

=--

(e.g. [MMSS 00, lemma 1.6](#MMSS00))

+-- {: .proof}
###### Proof

The coequalizer of pointed topological spaces that we need to consider has underlying it a coequalizer of underlying pointed sets  ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop), [prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects), [prop.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)). That in turn is the colimit over the diagram of underlying sets with the basepointe adjoined to the diagram ([prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects)). For a coequalizer diagram adding that extra point to the diagram clearly does not change the colimit, and so we need to consider the plain coequalizer of sets.

That is just the set of [[equivalence classes]] of [[pairs]]

$$
  ( c \overset{}{\to} c_0,\; x \in F(c) )
  \,,
$$

where two such pairs

$$
  ( c \overset{f}{\to} c_0,\; x \in F(c) )
  \,,\;\;\;\;
  ( d \overset{g}{\to} c_0,\; y \in F(d) )  
$$

are regarded as equivalent if there exists

$$
  c \overset{\phi}{\to} d
$$

such that 

$$
  f = g \circ \phi
  \,,
  \;\;\;\;\;and\;\;\;\;\;
  y = \phi(x)
  \,.
$$

(Because then the two pairs are the two images of the pair $(g,x)$ under the two morphisms being coequalized.)

But now considering the case that $d = c_0$ and $d = id_{c_0}$, so that $f = \phi$ shows that any pair

$$
  ( c \overset{\phi}{\to} c_0, \; x \in F(c))
$$

is identified, in the coequalizer, with the pair

$$
  (id_{c_0},\; \phi(x) \in F(c_0))
  \,,
$$ 

hence with $\phi(x)\in F(c_0)$. 

This shows the claim at the level of the underlying sets. To conclude it is now sufficient ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop)) to show that the topology on $F(c_0) \in Top^{\ast/}_{cg}$ is the [[final topology]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#InitialAndFinalTopologies)) of the system of component morphisms

$$
  \mathcal{C}(d,c) \wedge F(c)
    \longrightarrow
  \underset{c}{\int} \mathcal{C}(c,c_0) \wedge F(c)
$$

which we just found. But that system includes 

$$
  \mathcal{C}(c,c) \wedge F(c) \longrightarrow F(c)
$$

which is a [[retraction]]

$$
  id \;\colon\; F(c) \longrightarrow \mathcal{C}(c,c) \wedge F(c)
  \longrightarrow F(c)
$$

and so if all the preimages of a given subset of the coequalizer under these component maps is open, it must have already been open in $F(c)$.


=--


+-- {: .num_remark}
###### Remark

The statement of the [[co-Yoneda lemma]] in prop. \ref{TopologicalCoYonedaLemma} is a kind of [[categorification]] of the following statement in [[analysis]] (whence the notation with the integral signs):

For $X$ a [[topological space]], $f \colon X \to\mathbb{R}$ a [[continuous function]] and $\delta(-,x_0)$ denoting the [[Dirac distribution]], then

$$
  \int_{x \in X} \delta(x,x_0) f(x)
  = 
  f(x_0)
  \,.
$$

=--

It is this analogy that gives the name to the following statement:

+-- {: .num_prop #CoendsCommuteWithEachOther}
###### Proposition
**([[Fubini theorem]] for (co)-ends)**

For $F$ a pointed topologically enriched [[bifunctor]] on a small pointed topological [[product category]] $\mathcal{C}_1 \times \mathcal{C}_2$ (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}), i.e.

$$
   F 
  \;\colon\;
  \left(
    \mathcal{C}_1\times\mathcal{C}_2
  \right)^{op}
  \times
  (\mathcal{C}_1 \times\mathcal{C}_2)
  \longrightarrow
  Top^{\ast/}_{cg}
$$

then its [[end]] and [[coend]] (def. \ref{EndAndCoendInTopcgSmash}) is equivalently formed consecutively over each variable, in either order:

$$
  \overset{(c_1,c_2)}{\int} F((c_1,c_2), (c_1,c_2))
  \simeq
  \overset{c_1}{\int}
  \overset{c_2}{\int}
  F((c_1,c_2), (c_1,c_2))
  \simeq
  \overset{c_2}{\int}
  \overset{c_1}{\int}
  F((c_1,c_2), (c_1,c_2))
$$

and

$$
  \underset{(c_1,c_2)}{\int} F((c_1,c_2), (c_1,c_2))
  \simeq
  \underset{c_1}{\int}
  \underset{c_2}{\int}
  F((c_1,c_2), (c_1,c_2))
  \simeq
  \underset{c_2}{\int}
  \underset{c_1}{\int}
  F((c_1,c_2), (c_1,c_2))
  \,.
$$

=--

+-- {: .proof}
###### Proof

Because [[limits]] commute with limits, and [[colimits]] commute with colimits.

=--



+-- {: .num_remark #MappingSpacePreservesEnds}
###### Remark

Because the pointed compactly generated [[mapping space]] functor ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#PointedMappingSpace)) 

$$
  Maps(-,-)_\ast
  \;\colon\;
  \left(Top^{\ast/}_{cg}\right)^{op}
  \times
  Top^{\ast/}_{cg}
  \longrightarrow
  Top^{\ast/}_{cg}
$$

takes [[colimits]] in the first argument and [[limits]] in the second argument to limits ([cor.](Introduction+to+Stable+homotopy+theory+--+P#MappingSpacesSendsColimitsInFirstArgumentToLimits)), it also takes [[coends]] in the first argument and [[ends]] in the second argument, to ends (def. \ref{EndAndCoendInTopcgSmash}):

$$
  Maps( X, \; \int_{c} F(c,c))_\ast
  \simeq
  \int_c Maps(X, F(c,c)_\ast)
$$

and

$$
  Maps( \int^{c} F(c,c),\; Y  )_\ast
  \simeq
  \underset{c}{\int} Maps( F(c,c),\; Y )_\ast
  \,.
$$

=--

+-- {: .num_prop #TopologicalLeftKanExtensionBCoend}
###### Proposition
**(left Kan extension via coends)**

Let $\mathcal{C}, \mathcal{D}$ be [[small category|small]] pointed [[topologically enriched categories]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)) and let 

$$
  p \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
$$

be a pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)). Then precomposition with $p$ constitutes a functor

$$
  p^\ast 
  \;\colon\;
  [\mathcal{D}, Top^{\ast/}_{cg}]
  \longrightarrow
  [\mathcal{C}, Top^{\ast/}_{cg}]
$$

$G\mapsto G\circ p$. This functor has a [[left adjoint]] $Lan_p$, called **left [[Kan extension]]** along $p$

$$
  [\mathcal{D}, Top^{\ast/}_{cg}]
    \underoverset
      {\underset{p^\ast}{\longrightarrow}}
      {\overset{Lan_p }{\longleftarrow}}
      {\bot}
  [\mathcal{C}, Top^{\ast/}_{cg}]
$$

which is given objectwise by a [[coend]] (def. \ref{EndAndCoendInTopcgSmash}):

$$
  (Lan_p F)
  \;\colon\;
  c 
  \;\mapsto \;
  \overset{c\in \mathcal{C}}{\int}
   \mathcal{D}(p(c),d) \wedge F(c)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Use the expression of natural transformations in terms of ends (example \ref{NaturalTransformationsViaEnds} and def. \ref{PointedTopologicalFunctorCategory}), then use the respect of $Maps(-,-)_\ast$ for ends/coends (remark \ref{MappingSpacePreservesEnds}),  use the smash/mapping space adjunction ([cor.](Introduction+to+Stable+homotopy+theory+--+P#SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces)), use the [[Fubini theorem]] (prop. \ref{CoendsCommuteWithEachOther}) and finally use [[Yoneda reduction]] (prop. \ref{YonedaReductionTopological}) to obtain a sequence of [[natural isomorphisms]] as follows:

$$
  \begin{aligned}
    [\mathcal{D},Top^{\ast/}_{cg}]( Lan_p F, \, G )
    & =
   \underset{d \in \mathcal{D}}{\int}
    Maps( (Lan_p F)(d), \, G(d) )_\ast
   \\
   & =
   \underset{d\in \mathcal{D}}{\int}
   Maps\left(
     \overset{c \in \mathcal{C}}{\int} \mathcal{D}(p(c),d) \wedge F(c)
     ,\;
     G(d)
   \right)_\ast
    \\
  &\simeq
  \underset{d \in \mathcal{D}}{\int}
  \underset{c \in \mathcal{C}}{\int}
  Maps(
    \mathcal{D}(p(c),d)\wedge F(c) \,,\; G(d)
  )_\ast
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  \underset{d\in \mathcal{D}}{\int}
  Maps(F(c), 
    Maps(
     \mathcal{D}(p(c),d) , \, G(d)
    )_\ast
  )_\ast
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  Maps(F(c), 
   \underset{d\in \mathcal{D}}{\int}
   Maps(
    \mathcal{D}(p(c),d) , \, G(d)
   )_\ast
  )_\ast
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  Maps(F(c), G(p(c))
  )_\ast  
  \\
  & =
  [\mathcal{C}, Top^{\ast/}_{cg}](F,p^\ast G)
  \end{aligned}
  \,.
$$

=--

### Monoidal topological categories

+-- {: .num_defn #MonoidalCategory} 
###### Definition

A **(pointed) topologically enriched [[monoidal category]]** is a (pointed) [[topologically enriched category]] $\mathcal{C}$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)) equipped with 

1. a (pointed) [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor))

   $$ 
      \otimes 
        \;\colon\; 
      \mathcal{C} \times \mathcal{C}  
       \longrightarrow
      \mathcal{C}
   $$

   out of the (pointed) topologival [[product category]] of $\mathcal{C}$ with itself (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}), called the **[[tensor product]]**, 

1. an object

   $$ 
     1 \in \mathcal{C} 
   $$

   called the **[[unit object]]** or **[[tensor unit]]**, 

1. a [[natural isomorphism]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor))

   $$
     a 
       \;\colon\; 
     ((-)\otimes (-)) \otimes (-)
       \overset{\simeq}{\longrightarrow}
     (-) \otimes ((-)\otimes(-))
   $$

   called the **[[associator]]**, 

1. a [[natural isomorphism]] 

   $$
     \ell
       \;\colon\; 
     (1 \otimes (-)) 
       \overset{\simeq}{\longrightarrow}
     (-)
   $$

   called the **[[left unitor]]**, and a natural isomorphism 

   $$
     r \;\colon\; (-) \otimes 1 \overset{\simeq}{\longrightarrow} (-)
   $$

   called the **[[right unitor]]**, 

such that the following two kinds of [[commuting diagram|diagrams commute]], for all objects involved:

1. **triangle identity**:

   $$
     \array{
        & (x \otimes 1) \otimes y &\stackrel{a_{x,1,y}}{\longrightarrow} & x \otimes (1 \otimes y)
         \\     
         & {}_{\rho_x \otimes 1_y}\searrow       
         && \swarrow_{1_x \otimes \lambda_y}
         & 
        \\
        &&
        x \otimes y
        &&
     }
   $$


1. the **[[pentagon identity]]**:

+-- {: style="text-align:center"}
[[!include monoidal category > pentagon]]
=--


=--


+-- {: .num_defn #BraidedMonoidalCategory} 
###### Definition

A **(pointed) topological [[braided monoidal category]]**, is a (pointed) topological [[monoidal category]] $\mathcal{C}$ (def. \ref{MonoidalCategory}) equipped with a [[natural isomorphism]]

$$ 
  \tau_{x,y} \colon x \otimes y \to y \otimes x 
$$

called the **[[braiding]]**, such that the following two kinds of [[commuting diagram|diagrams commute]] for all [[objects]] involved:

$$
  \array{
   (x \otimes y) \otimes z 
   &\stackrel{a_{x,y,z}}{\to}&
   x \otimes (y \otimes z)
   &\stackrel{B_{x,y \otimes z}}{\to}&
   (y \otimes z) \otimes x
   \\
   \downarrow^{B_{x,y}\otimes Id}
   &&&&
   \downarrow^{a_{y,z,x}}
   \\
   (y \otimes x) \otimes z
   &\stackrel{a_{y,x,z}}{\to}&
   y \otimes (x \otimes z)
   &\stackrel{Id \otimes B_{x,z}}{\to}&
   y \otimes (z \otimes x)
  }
$$

and

$$
  \array{
   x \otimes (y \otimes z) 
   &\stackrel{a^{-1}_{x,y,z}}{\to}&
   (x \otimes y) \otimes z
   &\stackrel{B_{x \otimes y, z}}{\to}&
   z \otimes (x \otimes y)
   \\
   \downarrow^{Id \otimes B_{y,z}}
   &&&&
   \downarrow^{a^{-1}_{z,x,y}}
   \\
   x \otimes (z \otimes y)
   &\stackrel{a^{-1}_{x,z,y}}{\to}&
   (x \otimes z) \otimes y
   &\stackrel{B_{x,z} \otimes Id}{\to}&
   (z \otimes x) \otimes y
  }
  \,,
$$

where $a_{x,y,z} \colon (x \otimes y) \otimes z \to x \otimes (y \otimes z)$ denotes the components of the [[associator]] of $\mathcal{C}^\otimes$. 

=--

+-- {: .num_defn #SymmetricMonoidalCategory} 
###### Definition

A **(pointed) topological [[symmetric monoidal category]]** is a (pointed) topological [[braided monoidal category]] (def. \ref{BraidedMonoidalCategory}) for which the [[braiding]] 

$$ 
   B_{x,y} \colon x \otimes y \to y \otimes x 
$$

satisfies the condition:

$$ 
  B_{y,x} \circ B_{x,y} = 1_{x \otimes y}  
$$

for all objects $x, y$

=--

+-- {: .num_example #TopAsASymmetricMonoidalCategory} 
###### Example

The category [[Set]] of [[sets]] and [[functions]] between them, regarded as enriched in [[discrete topological spaces]], becomes a [[symmetric monoidal category]] according to def. \ref{SymmetricMonoidalCategory} with [[tensor product]] the [[Cartesian product]] $\times$ of sets. The [[associator]], [[unitor]] and [[braiding]] isomorphism are the evident (almost unnoticable but nevertheless nontrivial) canonical identifications.

Similarly the $Top_{cg}$ of [[compactly generated topological spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#kTop)) becomes a [[symmetric monoidal category]] with [[tensor product]] the corresponding [[Cartesian products]], hence the operation of forming k-ified ([cor.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)) [[product topological spaces]] ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#ProductTopologicalSpace)). The underlying functions of the [[associator]], [[unitor]] and [[braiding]] isomorphisms are just those of the underlying sets, as above. 
 
Symmetric monoidal categories, such as these, for which the tensor product is the [[Cartesian product]] are called _[[Cartesian monoidal categories]]_.

=--

+-- {: .num_example #PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory} 
###### Example

The category $Top_{cg}^{\ast/}$ of [[pointed topological space|pointed]] [[compactly generated topological spaces]] with [[tensor product]] the  [[smash product]] $\wedge$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#SmashProductOfPointedObjects)) 

$$
  X \wedge Y \coloneqq \frac{X\times Y}{X\vee Y}
$$

is a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}) with [[unit object]] the pointed [[0-sphere]] $S^0$.

The components of the [[associator]], the [[unitors]] and the [[braiding]] are those of [[Top]] as in example \ref{TopAsASymmetricMonoidalCategory}, descended to the [[quotient topological spaces]] which appear in the definition of the [[smash product]]). This works for pointed [[compactly generated spaces]] (but not for general pointed topological spaces) by [this prop.](Introduction+to+Stable+homotopy+theory+--+P#SmashProductInTopcgIsAssociative).

=--


### Day convolution

+-- {: .num_defn #TopologicalDayConvolutionProduct}
###### Definition

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category|topological]] [[monoidal category]] (def. \ref{MonoidalCategory}) with [[tensor product]] denoted $\otimes\;\colon\; \mathcal{C} \times\mathcal{C} \to \mathcal{C}$. 

Then the **[[Day convolution]] tensor product** on the pointed topological [[enriched functor category]] $[\mathcal{C},Top^{\ast/}_{cg}]$ (def. \ref{PointedTopologicalFunctorCategory}) is the [[functor]]

$$
  \otimes_{Day} 
    \;\colon\; 
  [\mathcal{C},Top^{\ast/}_{cg}] \times [\mathcal{C},Top^{\ast/}_{cg}] 
    \longrightarrow 
  [\mathcal{C},Top^{\ast/}_{cg}]
$$

out of the pointed topological [[product category]] (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}) given by the following [[coend]] (def. \ref{EndAndCoendInTopcgSmash})

$$
  X \otimes_{Day} Y
    \;\colon\;
  c 
    \;\mapsto\;
  \overset{(c_1,c_2)\in \mathcal{C}\times \mathcal{C}}{\int}
    \mathcal{C}(c_1 \otimes_{\mathcal{D}} c_2, c) \wedge X(c_1) \wedge Y(c_2)
  \,.
$$

=--

+-- {: .num_example}
###### Example

Let $Seq$ denote the category with objects the [[natural numbers]], and only the [[zero morphisms]] and [[identity morphisms]] on these objects:

$$
  Seq(n_1,n_2)
  \coloneqq
  \left\{
    \array{
      S^0 & if\; n_1 = n_2
      \\
      \ast & otherwise
    }
  \right.
  \,.
$$

Regard this as a pointed topologically enriched category in the unique way. The operation of addition of natural numbers $\otimes = +$ makes this a monoidal category.

An object $X_\bullet \in [Seq, Top_{cg}^{\ast/}]$ is an $\mathbb{N}$-sequence of pointed topological spaces. Given two such, then their Day convolution according to def. \ref{TopologicalDayConvolutionProduct} is

$$
  \begin{aligned}
    (X \otimes_{Day} Y)_n
    & =
    \overset{(n_1,n_2) \in\mathbb{N}\times\mathbb{N}}{\int}
     Seq(n_1 + n_2 , n)
     \wedge 
     X_{n_1} \wedge X_{n_2}
    \\
    & = \underset{n_1+n_2 = n}{\coprod} X_{n_1}\wedge X_{n_2}
  \end{aligned} 
  \,.
$$

=--


Day convolution is equivalently a [[left Kan extension]] (def. \ref{TopologicalLeftKanExtensionBCoend}):

+-- {: .num_defn #ExternalTensorProduct}
###### Definition

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)).  Its **[[external tensor product]]** is the pointed [[topologically enriched functor]]

$$
  \overline{\wedge} 
   \;\colon\; 
  [\mathcal{C},Top^{\ast/}_{cg}] 
    \times 
  [\mathcal{C},Top^{\ast/}_{cg}] 
    \longrightarrow 
  [\mathcal{C}\times \mathcal{C}, Top^{\ast/}_{cg}]
$$

given by 

$$
  X \overline{\wedge} Y  
    \;\coloneqq\; 
  \wedge \circ (X,Y)
  \,,
$$

i.e.

$$
  (X \overline\wedge Y)(c_1,c_2)
  =
  X(c_1)\wedge X(c_2)
  \,.
$$

=--


+-- {: .num_prop #DayConvolutionViaKanExtensionOfExternalTensorAlongTensor}
###### Proposition

The Day convolution product (def. \ref{TopologicalDayConvolutionProduct}) of two functors is equivalently the [[left Kan extension]] (def. \ref{TopologicalLeftKanExtensionBCoend}) of their external tensor product (def. \ref{ExternalTensorProduct}) along the tensor product $\otimes_{\mathcal{C}}$: there is a [[natural isomorphism]]

$$
  X \otimes_{Day} Y
  \simeq
  Lan_{\otimes_{\mathcal{C}}} (X \overline{\wedge} Y)
  \,.
$$

=--

This perspective is highlighted in ([MMSS 00, p. 60](#MMSS00)).

+-- {: .proof}
###### Proof

By prop. \ref{TopologicalLeftKanExtensionBCoend} we may compute the left Kan extension as the following [[coend]]:

$$
  \begin{aligned}
     Lan_{\otimes_{\mathcal{C}}} (X\overline{\wedge} Y)(c)
     &
     \simeq
      \overset{(c_1,c_2) \in \mathcal{C}\times \mathcal{C}}{\int} 
      \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_2, c )
      \wedge
      (X\overline{\wedge}Y)(c_1,c_2)
     \\
    & =
    \overset{(c_1,c_2)\in \mathcal{C}\times \mathcal{C}}{\int}
    \mathcal{C}(c_1\otimes c_2) 
    \wedge
     X(c_1)\wedge X(c_2) 
  \end{aligned} 
  \,.
$$


=--

+-- {: .num_cor #DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor}
###### Corollary

Day convolution $\otimes_{Day}$, def. \ref{TopologicalDayConvolutionProduct}, is universally characterized by the property that there are [[natural isomorphisms]]

$$
  [\mathcal{C},Top^{\ast/}_{cg}](X \otimes_{Day} Y, Z) 
    \simeq 
  [\mathcal{C}\times \mathcal{C},Top^{\ast/}_{cg}](
    X \overline{\wedge} Y,\; Z \circ \wedge
  )
  \,,
$$

where $\overline{\wedge}$ is the external product of def. \ref{ExternalTensorProduct}.

=--

+-- {: .proof}
###### Proof

By prop. \ref{DayConvolutionViaKanExtensionOfExternalTensorAlongTensor} and since left [[Kan extension]] along any $f$ is the [[left adjoint]] to precomposition with $f$.

=--

Write

$$
  y \;\colon\; \mathcal{C}^{op} \longrightarrow [\mathcal{C}, Top^{\ast/}_{cg}]
$$

for the $Top^{\ast/}_{cg}$-[[Yoneda embedding]], so that for $c\in \mathcal{C}$ any [[object]], $y(c)$ is the [[representable functor|corepresented functor]] $y(c)\colon d \mapsto \mathcal{C}(c,d)$.


+-- {: .num_prop #DayConvolutionYieldsMonoidalCategoryStructure}
###### Proposition

For $\mathcal{C}$ a small monoidal pointed topologically enriched category,
the Day convolution product $\otimes_{Day}$ of def. \ref{TopologicalDayConvolutionProduct} makes the pointed topologically [[enriched functor category]]

$$
  ( [\mathcal{C}, Top^{\ast/}_{cg}], \otimes_{Day}, y(I))
$$

a topological [[monoidal category]] with [[tensor unit]] $y(I)$ co-represented by the tensor unit $I$ of $\mathcal{C}$. 

=--

+-- {: .proof}
###### Proof

To see that $y(I)$ is the tensor unit for $\otimes_{Day}$, 
use the [[Fubini theorem]] for [[coends]] (prop. \ref{CoendsCommuteWithEachOther}) and then twice the [[co-Yoneda lemma]] (prop. \ref{TopologicalCoYonedaLemma}) to get for any $X \in [\mathcal{C},Top^{\ast/}_{cg}]$ that

$$
  \begin{aligned}
     X \otimes_{Day} y(I)
     & 
     =
     \overset{c_1,c_2 \in \mathcal{C}}{\int}
     \mathcal{C}(c_1\otimes_{\mathcal{D}} c_2,-) 
      \wedge 
     X(c_1) \wedge \mathcal{C}(I,c_2)
     \\
     & \simeq 
     \overset{c_1\in \mathcal{C}}{\int}
      X(c_1) 
        \wedge  
      \overset{c_2 \in \mathcal{C}}{\int}  
        \mathcal{C}(c_1\otimes_{\mathcal{C}} c_2,-)
        \wedge 
        \mathcal{C}(I,c_2) 
    \\
    & \simeq 
      \overset{c_1\in \mathcal{C}}{\int}
      X(c_1) 
         \wedge
      \mathcal{C}(c_1 \otimes_{\mathcal{C}} I, -)
    \\
    & \simeq 
      \overset{c_1\in \mathcal{C}}{\int}
      X(c_1) 
         \wedge
      \mathcal{C}(c_1, -)
    \\
    & \simeq
    X(-)
    \\
    & \simeq 
    X
  \end{aligned}
  \,.
$$

=--

### Pre-Excisive functors

Write $Top^{\ast}_{cg,fin} \hookrightarrow Top^{\ast/}_{cg}$ for the full inclusion on the topological spaces isomorphic to a [[finite CW-complex]].

Then 

$$
 [Top^{\ast/}_{cg,fin}, Top^{\ast/}_{cg}]
$$

is the category of _[[pre-excisive functors]]_. Its [[symmetric monoidal smash product of spectra]] is the [[Day convolution]] $\wedge_{Day}$ (def. \ref{TopologicalDayConvolutionProduct}) of the plain smash product. By prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure} this gives a topological [[monoidal category]]


$$
  \left( 
    [Top^{\ast/}_{cg,fin}, Top^{\ast/}_{cg}]
    ,\;
    \wedge_{Day}
    , y(S^0)
  \right)
$$


## Examples

* The [[ring spectrum]]-structure on [[Thom spectra]] naturally arises in FSP-form, see _[Thom spectrum -- Properties -- Ring spectrum structure](Thom+spectrum#RingSpectrumStructure)_.

## Related concepts

* [[symmetric ring spectrum]]

* [[Day convolution]]

## Reference

The concept was introduced (before [[symmetric smash products of spectra]] had been found) in

* {#B&#246;kstedt86} [[Marcel Bökstedt]], _Topological Hochschild homology_. Preprint, Bielefeld, 1986

Restricted to spheres as "FSPs defined on spheres" they were considered in

* [[Lars Hesselholt]], [[Ib Madsen]],  1.7 of _On the K-theory of finite algebras over Witt vectors of perfect fields_ ([K-theory](http://www.math.uiuc.edu/K-theory/0055/)).

and identified there as the monoids in [[symmetric spectra]] as previously introduced by [[Jeff Smith]].

In the [[model structure for excisive functors]] the concept was recovered in

* {#Lydakis98} Lydakis, _Simplicial functors and stable homotopy theory_ Preprint, available via Hopf archive, 1998 ([pdf](http://hopf.math.purdue.edu/Lydakis/s_functors.pdf))

and in the model of [[connective spectra]] by [[Gamma-spaces]] in

* {#Lydakis98b} Lydakis, _Smash products and $\Gamma$-spaces_, Math. Proc. Cam. Phil. Soc. 126 (1999), 311-328 ([pdf](http://hopf.math.purdue.edu/Lydakis/smash_gamma.pdf))


A systematic account is in 

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], part III of _[[Model categories of diagram spectra]]_, Proceedings London Mathematical Society Volume 82, Issue 2, 2000 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf), [publisher](http://plms.oxfordjournals.org/content/82/2/441.short?rss=1&ssource=mfc))



[[!redirects FSP]]
[[!redirects FSPs]]

[[!redirects functors with smash product]]

[[!redirects functor with smash products]]
[[!redirects functors with smash products]]
