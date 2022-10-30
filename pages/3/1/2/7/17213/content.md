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

## Ingredients

### Topological ends and coends
 {#TopologicalEndsAndCoends}

For working with pointed [[topologically enriched functors]], a certain shape of [[limits]]/[[colimits]] is particularly relevant: these are called (pointed topological enriched) _[[ends]]_ and _[[coends]]_. We here introduce these and then derive some of their basic properties, such as notably the expression for topological [[left Kan extension]] in terms of [[coends]] (prop. \ref{TopologicalLeftKanExtensionBCoend} below). Further below it is via left Kan extension along the ordinary smash product of pointed topological spaces ("[[Day convolution]]") that the [[symmetric monoidal smash product of spectra]] is induced.

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
     \underset{c,d \in \mathcal{C}}{\coprod} \mathcal{C}(c,d) \wedge F(d,c)
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
        {\underset{\underset{c,d}{\sqcup} \tilde \rho_{(c,d)}(c)  }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} \tilde\rho_{d,c}(d)}{\longrightarrow}}
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

Now that [[natural transformations]] are phrased in terms of [[ends]] (example \ref{NaturalTransformationsViaEnds}), as is the Yoneda lemma (prop. \ref{YonedaReductionTopological}), it is natural to consider the [[formal duality|dual]] statement involving [[coends]]:

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

But now considering the case that $d = c_0$ and $g = id_{c_0}$, so that $f = \phi$ shows that any pair

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
  \overset{c}{\int} \mathcal{C}(c,c_0) \wedge F(c)
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

We recall the basic definitions of [[monoidal categories]] and of [[monoid in a monoidal category|monoids]] and [[module object|modules]] [[internalization|internal]] to monoidal categories. All examples are at the end of this section, starting with example \ref{TopAsASymmetricMonoidalCategory} below.

+-- {: .num_defn #MonoidalCategory} 
###### Definition

A **(pointed) [[topologically enriched category|topologically enriched]] [[monoidal category]]** is a (pointed) [[topologically enriched category]] $\mathcal{C}$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)) equipped with 

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


+-- {: .num_lemma #kel1} 
###### Lemma 
**([Kelly 64](monoidal+category#kel1))** 

Let $(\mathcal{C}, \otimes, 1)$ be a [[monoidal category]], def. \ref{MonoidalCategory}. Then the left and right [[unitors]] $\ell$ and $r$ satisfy the following conditions: 

1. $\ell_1 = r_1 \;\colon\; 1 \otimes 1 \overset{\simeq}{\longrightarrow} 1$;

1. for all objects $x,y \in \mathcal{C}$ the following [[commuting diagram|diagram commutes]]:
 
   $$ 
     \array{
       (1 \otimes x) \otimes y  & & 
       \\
       {}^\mathllap{\alpha_{1, x, y}} \downarrow 
       & \searrow^\mathrlap{\ell_x y} & 
       \\
       1 \otimes (x \otimes y) 
       & \underset{\ell_{x \otimes y}}{\longrightarrow} & x \otimes y
     }
     \,.
   $$ 

   Analogously for the right unitor.

=-- 


+-- {: .num_defn #BraidedMonoidalCategory} 
###### Definition

A **(pointed) [[topologically enriched category|topological]] [[braided monoidal category]]**, is a (pointed) [[topologically enriched category|topological]] [[monoidal category]] $\mathcal{C}$ (def. \ref{MonoidalCategory}) equipped with a [[natural isomorphism]]

$$ 
  \tau_{x,y} \colon x \otimes y \to y \otimes x 
$$

called the **[[braiding]]**, such that the following two kinds of [[commuting diagram|diagrams commute]] for all [[objects]] involved:

$$
  \array{
   (x \otimes y) \otimes z 
   &\stackrel{a_{x,y,z}}{\to}&
   x \otimes (y \otimes z)
   &\stackrel{\tau_{x,y \otimes z}}{\to}&
   (y \otimes z) \otimes x
   \\
   \downarrow^{\tau_{x,y}\otimes Id}
   &&&&
   \downarrow^{a_{y,z,x}}
   \\
   (y \otimes x) \otimes z
   &\stackrel{a_{y,x,z}}{\to}&
   y \otimes (x \otimes z)
   &\stackrel{Id \otimes \tau_{x,z}}{\to}&
   y \otimes (z \otimes x)
  }
$$

and

$$
  \array{
   x \otimes (y \otimes z) 
   &\stackrel{a^{-1}_{x,y,z}}{\to}&
   (x \otimes y) \otimes z
   &\stackrel{\tau_{x \otimes y, z}}{\to}&
   z \otimes (x \otimes y)
   \\
   \downarrow^{Id \otimes \tau_{y,z}}
   &&&&
   \downarrow^{a^{-1}_{z,x,y}}
   \\
   x \otimes (z \otimes y)
   &\stackrel{a^{-1}_{x,z,y}}{\to}&
   (x \otimes z) \otimes y
   &\stackrel{\tau_{x,z} \otimes Id}{\to}&
   (z \otimes x) \otimes y
  }
  \,,
$$

where $a_{x,y,z} \colon (x \otimes y) \otimes z \to x \otimes (y \otimes z)$ denotes the components of the [[associator]] of $\mathcal{C}^\otimes$. 

=--

+-- {: .num_defn #SymmetricMonoidalCategory} 
###### Definition

A **(pointed) [[topologically enriched category|topological]] [[symmetric monoidal category]]** is a (pointed) topological [[braided monoidal category]] (def. \ref{BraidedMonoidalCategory}) for which the [[braiding]] 

$$ 
   \tau_{x,y} \colon x \otimes y \to y \otimes x 
$$

satisfies the condition:

$$ 
  \tau_{y,x} \circ \tau_{x,y} = 1_{x \otimes y}  
$$

for all objects $x, y$

=--

+-- {: .num_defn #ClosedMonoidalCategory}
###### Definition

Given a (pointed) [[topologically enriched category|topological]] [[symmetric monoidal category]] $\mathcal{C}$ with [[tensor product]] $\otimes$ (def. \ref{SymmetricMonoidalCategory}) it is called a **[[closed monoidal category]]** if for each $Y \in \mathcal{C}$ the functor $Y \otimes(-)\simeq (-)\otimes X$ has a [[right adjoint]], denoted $[Y,-]$

$$
  \mathcal{C}
    \underoverset
      {\underset{[Y,-]}{\longrightarrow}}
      {\overset{(-) \otimes Y}{\longleftarrow}}
      {\bot}
  \mathcal{C}
  \,,
$$

hence if there are [[natural isomorphisms]]

$$
  Hom_{\mathcal{C}}(X \otimes Y, Z)
   \;\simeq\;
  Hom_{\mathcal{C}}{C}(X, [Y,Z])
$$

for all objects $X,Z \in \mathcal{C}$. 

Since for the case that $X = 1$ is the [[tensor unit]] of $\mathcal{C}$ this means that

$$
  Hom_{\mathcal{C}}(1,[Y,Z]) \simeq Hom_{\mathcal{C}}(Y,Z)
  \,,
$$

the object $[Y,Z] \in \mathcal{C}$ is an enhancement of the ordinary [[hom-set]] $Hom_{\mathcal{C}}(Y,Z)$ to an object in $\mathcal{C}$.
Accordingly, it is also called the **[[internal hom]]** between $Y$ and $Z$. 

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


+-- {: .num_example #ExampleAbelianGroupsOfMonoidalCategory}
###### Example

The category [[Ab]] of [[abelian groups]], regarded as enriched in [[discrete topological spaces]], becomes a [[symmetric monoidal category]] with tensor product the actual [[tensor product of abelian groups]] $\otimes_{\mathbb{Z}}$ and with [[tensor unit]] the additive group $\mathbb{Z}$ of [[integers]]. Again the [[associator]], [[unitor]] and [[braiding]] isomorphism are the evident ones coming from the underlying sets, as in example \ref{TopAsASymmetricMonoidalCategory}.

This is the archetypical case that motivates the notation "$\otimes$" for the pairing operation in a [[monoidal category]]: 

1. A [[monoid in a monoidal category|monoid in]] $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{MonoidsInMonoidalCategory}) is equivalently a [[ring]]. 

1. A [[commutative monoid in a symmetric monoidal category|commutative monoid in]] in $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{MonoidsInMonoidalCategory}) is equivalently a [[commutative ring]] $R$.

1. An $R$-[[module object]] in $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{ModulesInMonoidalCategory}) is equivalently an $R$-[[module]];

1. The tensor product of $R$-module objects (def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}) is the standard [[tensor product of modules]].

1. The [[category of modules|category of module objects]] $R Mod(Ab)$ (def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}) is the standard [[category of modules]] $R Mod$.

=--

### Algebras and modules
 {#AlgebrasAndModules}


+-- {: .num_defn #MonoidsInMonoidalCategory}
###### Definition

Given a (pointed) [[topologically enriched category|topological]] [[monoidal category]] $(\mathcal{C}, \otimes, 1)$, then a **[[monoid in a monoidal category|monoid internal to]]** $(\mathcal{C}, \otimes, 1)$ is

1. an [[object]] $A \in \mathcal{C}$;

1. a morphism $e \;\colon\; 1 \longrightarrow A$ (called the _[[unit]]_)

1. a morphism $\mu \;\colon\; A \otimes A \longrightarrow A$ (called the _product_); 

such that

1. ([[associativity]]) the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (A\otimes A) \otimes A 
         &\underoverset{\simeq}{a_{A,A,A}}{\longrightarrow}&
       A \otimes (A \otimes A)
         &\overset{A \otimes \mu}{\longrightarrow}&
       A \otimes A
       \\
       {}^{\mathllap{\mu \otimes A}}\downarrow  
         && &&
       \downarrow^{\mathrlap{\mu}}
       \\
       A \otimes A
         &\longrightarrow&
         &\overset{\mu}{\longrightarrow}&
       A
     }
     \,,
   $$

   where $a$ is the associator isomorphism of $\mathcal{C}$;

1. ([[unitality]]) the following [[commuting diagram|diagram commutes]]:

   $$
     \array{
       1 \otimes A 
         &\overset{e \otimes id}{\longrightarrow}&
       A \otimes A
         &\overset{id \otimes e}{\longleftarrow}& 
       A \otimes 1
       \\
       & {}_{\mathllap{\ell}}\searrow 
       & \downarrow^{\mathrlap{\mu}} &
       & \swarrow_{\mathrlap{r}}
       \\
       && A
     }
     \,,
   $$

   where $\ell$ and $r$ are the left and right unitor isomorphisms of $\mathcal{C}$.

Moreover, if $(\mathcal{C}, \otimes , 1)$ has the structure of a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}) $(\mathcal{C}, \otimes, 1, B)$ with symmetric [[braiding]] $\tau$, then a monoid $(A,\mu, e)$ as above is called a **[[commutative monoid in a symmetric monoidal category|commutative monoid in]]** $(\mathcal{C}, \otimes, 1, B)$ if in addition

* (commutativity) the following [[commuting diagram|diagram commutes]]

  $$
    \array{
      A \otimes A 
        && \underoverset{\simeq}{\tau_{A,A}}{\longrightarrow} &&
      A \otimes A
      \\
      & {}_{\mathllap{\mu}}\searrow && \swarrow_{\mathrlap{\mu}}
      \\
      && A
    }
    \,.
  $$

A [[homomorphism]] of monoids $(A_1, \mu_1, e_1)\longrightarrow (A_2, \mu_2, f_2)$ is a morphism

$$
  f \;\colon\; A_1 \longrightarrow A_2
$$ 

in $\mathcal{C}$, such that the following two [[commuting diagram|diagrams commute]]

$$
  \array{
    A_1 \otimes A_1 
      &\overset{f \otimes f}{\longrightarrow}&
    A_2 \otimes A_2
    \\
    {}^{\mathllap{\mu_1}}\downarrow && \downarrow^{\mathrlap{\mu_2}}
    \\
    A_1 &\underset{f}{\longrightarrow}& A_2
  }
$$

and

$$
  \array{
    1_{\mathcal{c}} &\overset{e_1}{\longrightarrow}& A_1
    \\
    & {}_{\mathllap{e_2}}\searrow & \downarrow^{\mathrlap{f}}
    \\
    && A_2
  }
  \,.
$$

Write $Mon(\mathcal{C}, \otimes,1)$ for the [[category of monoids]] in $\mathcal{C}$, and $CMon(\mathcal{C}, \otimes, 1)$ for its subcategory of commutative monoids.


=--

+-- {: .num_example #MonoidGivenByTensorUnit}
###### Example

Given a (pointed) [[topologically enriched category|topological]] [[monoidal category]] $(\mathcal{C}, \otimes, 1)$, then the [[tensor unit]] $1$ is a [[monoid in a monoidal category|monoid in]] $\mathcal{C}$ (def. \ref{MonoidsInMonoidalCategory}) with product given by either the left or right [[unitor]]

$$
  \ell_1 = r_1 \;\colon\; 1 \otimes 1 \overset{\simeq}{\longrightarrow} 1
  \,.
$$

By lemma \ref{kel1}, these two morphisms coincide and define an [[associativity|associative]] product with unit the identity $id \colon 1 \to 1$.

If $(\mathcal{C}, \otimes , 1)$ is a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}), then this monoid is a [[commutative monoid in a symmetric monoidal category|commutative monoid]].

=--


+-- {: .num_defn #ModulesInMonoidalCategory}
###### Definition

Given a (pointed) [[topologically enriched category|topological]] [[monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidalCategory}), and given $(A,\mu,e)$ a [[monoid in a monoidal category|monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}), then a **left [[module object]]** in $(\mathcal{C}, \otimes, 1)$ over $(A,\mu,e)$ is

1. an [[object]] $N \in \mathcal{C}$;

1. a [[morphism]] $\rho \;\colon\; A \otimes N \longrightarrow N$ (called the _[[action]]_);

such that 

1. ([[unitality]]) the following [[commuting diagram|diagram commutes]]:

   $$
     \array{
       1 \otimes N 
         &\overset{e \otimes id}{\longrightarrow}&
       A \otimes N
       \\
       & {}_{\mathllap{\ell}}\searrow 
       & \downarrow^{\mathrlap{\rho}} 
       \\
       && A
     }
     \,,
   $$

   where $\ell$ is the left unitor isomorphism of $\mathcal{C}$.


1. (action property) the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (A\otimes A) \otimes N
         &\underoverset{\simeq}{a_{A,A,N}}{\longrightarrow}&
       A \otimes (A \otimes N)
         &\overset{A \otimes \rho}{\longrightarrow}&
       A \otimes N
       \\
       {}^{\mathllap{\mu \otimes N}}\downarrow  
         && &&
       \downarrow^{\mathrlap{\rho}}
       \\
       A \otimes N
         &\longrightarrow&
         &\overset{\rho}{\longrightarrow}&
       N
     }
     \,,
   $$

A [[homomorphism]] of left $A$-module objects 

$$
  (N_1, \rho_1) \longrightarrow (N_2, \rho_2)
$$

is a morphism 

$$
  f\;\colon\; N_1 \longrightarrow N_2
$$

in $\mathcal{C}$, such that the following [[commuting diagram|diagram commutes]]:

$$
  \array{
    A\otimes N_1 &\overset{A \otimes f}{\longrightarrow}& A\otimes N_2
    \\
    {}^{\mathllap{\rho_1}}\downarrow 
      && 
    \downarrow^{\mathrlap{\rho_2}}
    \\
    N_1 &\underset{f}{\longrightarrow}& N_2
  }
  \,.
$$

For the resulting **[[category of modules]]** of left $A$-modules in $\mathcal{C}$ with $A$-module homomorphisms between them, we write

$$
  A Mod(\mathcal{C})
  \,.
$$

This is naturally a (pointed) [[topologically enriched category]] itself.

=--

+-- {: .num_example #EveryObjectIsModuleOverTensorUnit}
###### Example

Given a [[monoidal category]] $(\mathcal{C},\otimes, 1)$ (def. \ref{MonoidalCategory}) with the [[tensor unit]] $1$ regarded as a [[monoid in a monoidal category]] via example \ref{MonoidGivenByTensorUnit}, then the left [[unitor]]

$$
  \ell_C 
    \;\colon\;
  1\otimes C \longrightarrow C
$$

makes every object $C \in \mathcal{C}$ into a left module, according to def. \ref{ModulesInMonoidalCategory}, over $C$. The action property holds due to lemma \ref{kel1}. This gives an [[equivalence of categories]]

$$
  \mathbb{C} \simeq 1 Mod(\mathcal{C})
$$

of $\mathcal{C}$ with the [[category of modules]] over its tensor unit.


=--


+-- {: .num_prop #MonoidModuleOverItself} 
###### Proposition

In the situation of def. \ref{ModulesInMonoidalCategory}, the monoid $(A,\mu, e)$ canonically becomes a left module over itself by setting $\rho \coloneqq \mu$. More generally, for $C \in \mathcal{C}$ any object, then $A \otimes C$ naturally becomes a left $A$-module by setting:

$$
  \rho
  \;\colon\;
  A \otimes (A \otimes C)
   \underoverset{\simeq}{a^{-1}_{A,A,C}}{\longrightarrow}
  (A \otimes A) \otimes C
    \overset{\mu \otimes id}{\longrightarrow}
  A \otimes C
  \,.
$$

The $A$-modules of this form are called **[[free modules]]**.

The [[free functor]] $F$ constructing free $A$-modules is [[left adjoint]] to the [[forgetful functor]] $U$ which sends a module $(N,\rho)$ to the underlying object $U(N,\rho) \coloneqq N$.

$$
  A Mod(\mathcal{C})
    \underoverset
     {\underset{U}{\longrightarrow}}
     {\overset{F}{\longleftarrow}}
     {\bot}
  \mathcal{C}
  \,.
$$

=--

+-- {: .proof}
###### Proof

A homomorphism out of a free $A$-module is a morphism in $\mathcal{C}$ of the form

$$
  f \;\colon\; A\otimes C \longrightarrow N
$$

fitting into the diagram (where we are notationally suppressing the [[associator]])

$$
  \array{
    A \otimes A \otimes C
      &\overset{A \otimes f}{\longrightarrow}&
    A \otimes N
    \\
    {}^{\mathllap{\mu \otimes id}}\downarrow 
      && 
    \downarrow^{\mathrlap{\rho}}
    \\
    A \otimes C
      &\underset{f}{\longrightarrow}&
    N
  }
  \,.
$$

Consider the composite

$$
  \tilde f
    \;\colon\;
  C
    \underoverset{\simeq}{\ell_C}{\longrightarrow}
  1 \otimes C
    \overset{e\otimes id}{\longrightarrow}
  A \otimes C
    \overset{f}{\longrightarrow}
  N
  \,,
$$

i.e. the restriction of $f$ to the unit "in" $A$. By definition, this fits into a [[commuting square]] of the form (where we are now notationally suppressing the [[associator]] and the [[unitor]])

$$
  \array{
   A \otimes C
     &\overset{id \otimes \tilde f}{\longrightarrow}&
   A \otimes N
   \\
   {}^{\mathllap{id \otimes e \otimes id}}\downarrow 
     && 
   \downarrow^{\mathrlap{=}}
   \\
   A \otimes A \otimes C
    &\underset{id \otimes f}{\longrightarrow}&
   A \otimes N
  }
  \,.
$$

Pasting this square onto the top of the previous one yields

$$
  \array{
   A \otimes C
     &\overset{id \otimes \tilde f}{\longrightarrow}&
   A \otimes N
   \\
   {}^{\mathllap{id \otimes e \otimes id}}\downarrow 
     && 
   \downarrow^{\mathrlap{=}}
    \\
    A \otimes A \otimes C
      &\overset{A \otimes f}{\longrightarrow}&
    A \otimes N
    \\
    {}^{\mathllap{\mu \otimes id}}\downarrow 
      && 
    \downarrow^{\mathrlap{\rho}}
    \\
    A \otimes C
      &\underset{f}{\longrightarrow}&
    N
  }
  \,,
$$

where now the left vertical composite is the identity, by the unit law in $A$. This shows that $f$ is uniquely determined by $\tilde f$ via the relation

$$
  f = \rho \circ (id_A \otimes \tilde f)
  \,.
$$

This natural bijection between $f$ and $\tilde f$ establishes the adjunction.


=--

+-- {: .num_defn #TensorProductOfModulesOverCommutativeMonoidObject}
###### Definition

Given a (pointed) [[topologically enriched category|topological]] [[symmetric monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{SymmetricMonoidalCategory}), given $(A,\mu,e)$ a [[commutative monoid in a symmetric monoidal category|commutative monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}), and given $(N_1, \rho_1)$ and $(N_2, \rho_2)$ two left $A$-[[module objects]] (def.\ref{MonoidsInMonoidalCategory}), then the **[[tensor product of modules]]** $N_1 \otimes_A N_2$ is, if it exists, the [[coequalizer]]

$$
  N_1 \otimes A \otimes N_2
  \underoverset
    {\underset{\rho_{1}\circ (\tau_{N_1,A} \otimes N_2)}{\longrightarrow}}
    {\overset{N_1 \otimes \rho_2}{\longrightarrow}}
    {\phantom{AAAA}}
  N_1 \otimes N_1
    \overset{coequ}{\longrightarrow}
  N_1 \otimes_A N_2
$$

=--

+-- {: .num_prop #MonoidalCategoryOfModules}
###### Proposition

Given a (pointed) [[topologically enriched category|topological]] [[symmetric monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{SymmetricMonoidalCategory}), and given $(A,\mu,e)$ a [[commutative monoid in a symmetric monoidal category|commutative monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}). If all [[coequalizers]] exist in $\mathcal{C}$, then the [[tensor product of modules]] $\otimes_A$ from def. \ref{TensorProductOfModulesOverCommutativeMonoidObject} makes the [[category of modules]] $A Mod(\mathcal{C})$ into a [[symmetric monoidal category]], $(A Mod, \otimes_A, A)$ with [[tensor unit]] the object $A$ itself, regarded as an $A$-module via prop. \ref{MonoidModuleOverItself}.

=--

+-- {: .num_defn #AAlgebra}
###### Definition

Given a [[monoidal category|monoidal]] [[category of modules]] $(A Mod , \otimes_A , A)$ as in prop. \ref{MonoidalCategoryOfModules}, then a [[monoid in a monoidal category|monoid]] $(E, \mu, e)$ in  $(A Mod , \otimes_A , A)$ (def. \ref{MonoidsInMonoidalCategory}) is called an **$A$-[[associative algebra|algebra]]**.

=--

+-- {: .num_prop #AlgebrasOverAAreMonoidsUnderA}
###### Propposition

Given a [[monoidal category|monoidal]] [[category of modules]] $(A Mod , \otimes_A , A)$ in a [[monoidal category]] $(\mathcal{C},\otimes, 1)$ as in prop. \ref{MonoidalCategoryOfModules}, and an $A$-algebra $(E,\mu,e)$ (def. \ref{AAlgebra}), then there is an [[equivalence of categories]]

$$
  A Alg_{comm}(\mathcal{C}) 
    \coloneqq 
  CMon(A Mod)
   \simeq
  CMon(\mathcal{C})^{A/}
$$

between the [[category of commutative monoids]] in $A Mod$ and the [[coslice category]] of commutative monoids in $\mathcal{C}$ under $A$, hence between commutative $A$-algebras in $\mathcal{C}$ and commutative monoids $E$ in $\mathcal{C}$ that are equipped with a homomorphism of monoids $A \longrightarrow E$.

=--

(e.g. [EKMM 97, VII lemma 1.3](#EKMM97))

+-- {: .proof}
###### Proof

In one direction, consider a $A$-algebra $E$ with unit $e_E \;\colon\; A \longrightarrow E$ and product $\mu_{E/A} \colon E \otimes_A E \longrightarrow E$. There is the underlying product $\mu_E$ 

$$
  \array{
    E \otimes A \otimes E
    & 
    \underoverset
      {\underset{}{\longrightarrow}}
      {\overset{}{\longrightarrow}}
      {\phantom{AAA}}
    &
    E \otimes E
     &\overset{coeq}{\longrightarrow}&
    E \otimes_A E
    \\
    && & {}_{\mathllap{\mu_E}}\searrow & \downarrow^{\mathrlap{\mu_{E/A}}}
    \\
    && && E
  }
  \,.
$$

By considering a diagram of such coequalizer diagrams with middle vertical morphism $e_E\circ e_A$, one find that this is a unit for $\mu_E$ and that $(E, \mu_E, e_E \circ e_A)$ is a commutative monoid in $(\mathcal{C}, \otimes, 1)$.

Then consider the two conditions on the unit $e_E \colon A \longrightarrow E$. First of all this is an $A$-module homomorphism, which means that

$$
  (\star)
  \;\;\;\;\;
  \;\;\;\;\;
  \array{
    A \otimes A &\overset{id \otimes e_E}{\longrightarrow}& A \otimes E
    \\
    {}^{\mathllap{\mu_A}}\downarrow && \downarrow^{\mathrlap{\rho}}
    \\
    A &\underset{e_E}{\longrightarrow}& E
  }
$$

[[commuting diagram|commutes]]. Moreover it satisfies the unit property

$$
  \array{
    A \otimes_A E 
      &\overset{e_A \otimes id}{\longrightarrow}&
    E \otimes_A E
    \\
    & {}_{\mathllap{\simeq}}\searrow & \downarrow^{\mathrlap{\mu_{E/A}}}
    \\
    && E
  }
  \,.
$$

By forgetting the tensor product over $A$, the latter gives

$$
  \array{
    A \otimes E 
      &\overset{e \otimes id}{\longrightarrow}&
    E \otimes E
    \\
    \downarrow && \downarrow^{\mathrlap{}}
    \\
    A \otimes_A E 
      &\overset{e_E \otimes id}{\longrightarrow}&
    E \otimes_A E
    \\
    {}^{\mathllap{\simeq}}\downarrow 
      && 
    \downarrow^{\mathrlap{\mu_{E/A}}}
    \\
    E &=& E
  }
  \;\;\;\;\;\;\;\;
   \simeq
  \;\;\;\;\;\;\;\;
  \array{
    A \otimes E 
      &\overset{e_E \otimes id}{\longrightarrow}&
    E \otimes E
    \\
    {}^{\mathllap{\rho}}\downarrow && \downarrow^{\mathrlap{\mu_{E}}}
    \\
    E &\underset{id}{\longrightarrow}& E  
  }
  \,,
$$

where the top vertical morphisms on the left the canonical coequalizers, which identifies the vertical composites on the right as shown. Hence this may be [[pasting|pasted]] to the square $(\star)$ above, to yield a [[commuting square]]

$$
  \array{
    A \otimes A
     &\overset{id\otimes e_E}{\longrightarrow}&
    A \otimes E 
      &\overset{e_E \otimes id}{\longrightarrow}&
    E \otimes E
    \\
    {}^{\mathllap{\mu_A}}\downarrow
      &&
    {}^{\mathllap{\rho}}\downarrow 
      && 
    \downarrow^{\mathrlap{\mu_{E}}}
    \\
    A &\underset{e_E}{\longrightarrow}& E &\underset{id}{\longrightarrow}& E  
  }  
  \;\;\;\;\;\;\;\;\;\;
   =
  \;\;\;\;\;\;\;\;\;\;
  \array{
    A \otimes A 
     &\overset{e_E \otimes e_E}{\longrightarrow}&
    E \otimes E
    \\
    {}^{\mathllap{\mu_A}}\downarrow
      &&
    \downarrow^{\mathrlap{\mu_E}}
    \\
    A &\underset{e_E}{\longrightarrow}& E
  }
  \,.
$$

This shows that the unit $e_A$ is a homomorphism of monoids $(A,\mu_A, e_A) \longrightarrow (E, \mu_E, e_E\circ e_A)$.

Now for the converse direction, assume that $(A,\mu_A, e_A)$ and $(E, \mu_E, e'_E)$ are two commutative monoids in $(\mathcal{C}, \otimes, 1)$ with $e_E \;\colon\; A  \to E$ a monoid homomorphism. Then $E$ inherits a left $A$-[[module]] structure by

$$
  \rho
    \;\colon\;
  A \otimes E 
    \overset{e_A \otimes id}{\longrightarrow} 
  E \otimes E
    \overset{\mu_E}{\longrightarrow}
  E
  \,.
$$

By commutativity and associativity it follows that $\mu_E$ coequalizes the two induced morphisms $E \otimes A \otimes E \underoverset{\longrightarrow}{\longrightarrow}{\phantom{AA}} E \otimes E$. Hence the [[universal property]] of the [[coequalizer]] gives a factorization through some $\mu_{E/A}\colon E \otimes_A E \longrightarrow E$. This shows that $(E, \mu_{E/A}, e_E)$ is a commutative $A$-algebra.

Finally one checks that these two constructions are inverses to each other, up to isomorphism.

=--




### Day convolution



+-- {: .num_defn #TopologicalDayConvolutionProduct}
###### Definition

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category|topological]] [[monoidal category]] (def. \ref{MonoidalCategory}) with [[tensor product]] denoted $\otimes_{\mathcal{C}} \;\colon\; \mathcal{C} \times\mathcal{C} \to \mathcal{C}$. 

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
    \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_2, c) \wedge X(c_1) \wedge Y(c_2)
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
    \overset{(n_1,n_2)}{\int}
     Seq(n_1 + n_2 , n)
     \wedge 
     X_{n_1} \wedge X_{n_2}
    \\
    & = \underset{{n_1+n_2} \atop {= n}}{\coprod} \left(X_{n_1}\wedge X_{n_2}\right)
  \end{aligned} 
  \,.
$$

=--


We observe now that [[Day convolution]] is equivalently a [[left Kan extension]] (def. \ref{TopologicalLeftKanExtensionBCoend}). This will be key for understanding [[monoids]] and [[modules]] with respect to Day convolution.

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

The [[Day convolution]] product (def. \ref{TopologicalDayConvolutionProduct}) of two functors is equivalently the [[left Kan extension]] (def. \ref{TopologicalLeftKanExtensionBCoend}) of their external tensor product (def. \ref{ExternalTensorProduct}) along the tensor product $\otimes_{\mathcal{C}}$: there is a [[natural isomorphism]]

$$
  X \otimes_{Day} Y
  \simeq
  Lan_{\otimes_{\mathcal{C}}} (X \overline{\wedge} Y)
  \,.
$$

Hence the [[adjunction unit]] is a [[natural transformation]] of the form

$$
  \array{
    \mathcal{C} \times \mathcal{C}
    &&
      \overset{X \overline{\wedge} Y}{\longrightarrow}
    &&
      Top^{\ast/}_{cg}
    \\
    & {}^{\mathllap{\otimes}}\searrow 
     &\Downarrow&
    \nearrow_{\mathrlap{X \otimes_{Day} Y}}
    \\
    && \mathcal{C}
  }
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
      \overset{(c_1,c_2)}{\int} 
      \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_2, c )
      \wedge
      (X\overline{\wedge}Y)(c_1,c_2)
     \\
    & =
    \overset{(c_1,c_2)}{\int}
    \mathcal{C}(c_1\otimes c_2) 
    \wedge
     X(c_1)\wedge X(c_2) 
  \end{aligned} 
  \,.
$$


=--

+-- {: .num_cor #DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor}
###### Corollary

The [[Day convolution]] $\otimes_{Day}$ (def. \ref{TopologicalDayConvolutionProduct}) is universally characterized by the property that there are [[natural isomorphisms]]

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


Write

$$
  y \;\colon\; \mathcal{C}^{op} \longrightarrow [\mathcal{C}, Top^{\ast/}_{cg}]
$$

for the $Top^{\ast/}_{cg}$-[[Yoneda embedding]], so that for $c\in \mathcal{C}$ any [[object]], $y(c)$ is the [[representable functor|corepresented functor]] $y(c)\colon d \mapsto \mathcal{C}(c,d)$.


+-- {: .num_prop #DayConvolutionYieldsMonoidalCategoryStructure}
###### Proposition

For $\mathcal{C}$ a [[small category|small]] pointed [[topologically enriched category|topological]] [[monoidal category]] (def. \ref{MonoidalCategory}), the [[Day convolution]] tensor product $\otimes_{Day}$ of def. \ref{TopologicalDayConvolutionProduct} makes the pointed topologically [[enriched functor category]]

$$
  ( [\mathcal{C}, Top^{\ast/}_{cg}], \otimes_{Day}, y(1))
$$

a pointed topological [[monoidal category]] (def. \ref{MonoidalCategory}) with [[tensor unit]] $y(1)$ [[representable functor|co-represented]] by the tensor unit $1$ of $\mathcal{C}$. 

=--

+-- {: .proof}
###### Proof

Regarding [[associativity]], observe that

$$
  \begin{aligned}
    (X \otimes_{Day} ( Y \otimes_{Day} Z ))(c)
    & \simeq
    \overset{(c_1,c_2)}{\int}
      \mathcal{C}(c_1 \otimes_{\mathcal{D}} c_2, \,c) 
        \wedge
      X(c_1) 
       \wedge
      \overset{(d_1,d_2)}{\int}
       \mathcal{C}(d_1 \otimes_{\mathcal{C}} d_2, c_2 )
       (Y(d_2) \wedge Z(d_2))
    \\
    &\simeq \overset{c_1, d_1, d_2}{\int}
    \underset{\simeq \mathcal{C}(c_1 \otimes_{\mathcal{C}} d_1 \otimes_{\mathcal{C}} d_2, c )}{
      \underbrace{
       \overset{c_2}{\int} 
         \mathcal{C}(c_1 \otimes_{\mathcal{D}} c_2 , c)
           \wedge
         \mathcal{C}(d_1 \otimes_{\mathcal{C}}d_2, c_2 )
      }
    }
    \wedge X(c_1) \wedge (Y(d_1) \wedge Z(d_2))
    \\
    &\simeq 
    \overset{c_1, d_1, d_2}{\int}
     \mathcal{C}(c_1\otimes_{\mathcal{C}} d_1 \otimes_{\mathcal{C}} d_2, c ) 
       \wedge  
     X(c_1) \wedge (Y(d_1) \wedge Z(d_2))
  \end{aligned}
  \,,
$$

where we used the [[Fubini theorem]] for [[coends]] (prop. \ref{CoendsCommuteWithEachOther}) and then twice the [[co-Yoneda lemma]] (prop. \ref{TopologicalCoYonedaLemma}). An analogous formula follows for $X \otimes_{Day}  (Y \otimes_{Day} Z)))(c)$, and so associativity follows via prop. \ref{DayConvolutionViaKanExtensionOfExternalTensorAlongTensor} from the associativity of the [[smash product]] and of the tensor product $\otimes_{\mathcal{C}}$.

To see that $y(1)$ is the tensor unit for $\otimes_{Day}$, 
use the [[Fubini theorem]] for [[coends]] (prop. \ref{CoendsCommuteWithEachOther}) and then twice the [[co-Yoneda lemma]] (prop. \ref{TopologicalCoYonedaLemma}) to get for any $X \in [\mathcal{C},Top^{\ast/}_{cg}]$ that

$$
  \begin{aligned}
     X \otimes_{Day} y(1)
     & 
     =
     \overset{c_1,c_2 \in \mathcal{C}}{\int}
     \mathcal{C}(c_1\otimes_{\mathcal{D}} c_2,-) 
      \wedge 
     X(c_1) \wedge \mathcal{C}(1,c_2)
     \\
     & \simeq 
     \overset{c_1\in \mathcal{C}}{\int}
      X(c_1) 
        \wedge  
      \overset{c_2 \in \mathcal{C}}{\int}  
        \mathcal{C}(c_1\otimes_{\mathcal{C}} c_2,-)
        \wedge 
        \mathcal{C}(1,c_2) 
    \\
    & \simeq 
      \overset{c_1\in \mathcal{C}}{\int}
      X(c_1) 
         \wedge
      \mathcal{C}(c_1 \otimes_{\mathcal{C}} 1, -)
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


+-- {: .num_prop #DayMonoidalStructureIsClosed}
###### Proposition

For $\mathcal{C}$ a [[small category|small]] pointed [[topologically enriched category|topological]] [[monoidal category]] (def. \ref{MonoidalCategory}) with [[tensor product]] denoted $\otimes_{\mathcal{C}} \;\colon\; \mathcal{C} \times\mathcal{C} \to \mathcal{C}$, the [[monoidal category]] with [[Day convolution]] $([\mathcal{C},Top^{\ast/}_{cg}], \otimes_{Day}, y(1))$ from def. \ref{DayConvolutionYieldsMonoidalCategoryStructure} is a [[closed monoidal category]] (def. \ref{ClosedMonoidalCategory}). Its [[internal hom]] $[-,-]_{Day}$ is given by the [[end]] (def. \ref{EndAndCoendInTopcgSmash})

$$
  [X,Y]_{Day}(c)
  \simeq
   \underset{c_1,c_2}{\int}
      Maps\left( 
        \mathcal{C}(c \otimes_{\mathcal{C}} c_1,c_2),
        \;
        Maps(X(c_1) ,  Y(c_2))_\ast 
      \right)_\ast       
  \,.
$$

=--

+-- {: .proof}
###### Proof

Using the [[Fubini theorem]] (def. \ref{CoendsCommuteWithEachOther}) and the [[co-Yoneda lemma]] (def. \ref{TopologicalCoYonedaLemma}) and in view of definition \ref{PointedTopologicalFunctorCategory} of the [[enriched functor category]], there is the following sequence of [[natural isomorphisms]]:

$$
  \begin{aligned}
     [\mathcal{C},V]( X, [Y,Z]_{Day} )
       & \simeq
     \underset{c}{\int} 
     Maps\left(
        X(c), 
        \underset{c_1,c_2}{\int}
        Maps\left( 
          \mathcal{C}(c \otimes_{\mathcal{C}} c_1 , c_2),
          Maps(Y(c_1), Z(c_2))_\ast 
        \right)_\ast
     \right)_\ast
     \\
     &
     \simeq
     \underset{c}{\int}
     \underset{c_1,c_2}{\int}
     Maps\left(
       \mathcal{C}(c \otimes_{\mathcal{C}} c_1, c_2)
         \wedge
       X(c)
         \wedge
       Y(c_1)
       ,\;
       Z(c_2)
     \right)_\ast
     \\
     & \simeq
     \underset{c_2}{\int}
     Maps\left(
       \overset{c,c_1}{\int}
       \mathcal{C}(c \otimes_{\mathcal{C}} c_1, c_2)
         \wedge
       X(c)
         \wedge 
       Y(c_1)
       ,\;
       Z(c_2)
     \right)_\ast
     \\
     &\simeq
     \underset{c_2}{\int}
       Maps\left(
         (X \otimes_{Day} Y)(c_2),
         Z(c_2)
       \right)_\ast
     \\
     &\simeq
     [\mathcal{C},V](X \otimes_{Day} Y, Z)
  \end{aligned}
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

In the situation of def. \ref{DayConvolutionYieldsMonoidalCategoryStructure}, the [[Yoneda embedding]] $c\mapsto \mathcal{C}(c,-)$  constitutes a  [[strong monoidal functor]] 

$$
  (\mathcal{C},\otimes_{\mathcal{C}}, I) \hookrightarrow ([\mathcal{C},V], \otimes_{Day}, y(I))
  \,.
$$

=--

+-- {: .proof}
###### Proof

That the [[tensor unit]] is respected is part of prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure}. To see that the [[tensor product]] is respected, apply the [[co-Yoneda lemma]] (prop \ref{TopologicalCoYonedaLemma}) twice to get the following natural isomorphism

$$
  \begin{aligned}
    (y(c_1) \otimes_{Day} y(c_2))(c)
    &
    \simeq
    \overset{d_1, d_2}{\int} 
      \mathcal{C}(d_1 \otimes_{\mathcal{C}} d_2, c )
    \wedge
      \mathcal{C}(c_1,d_1)
    \wedge
      \mathcal{C}(c_2,d_2)
    \\
    & \simeq \mathcal{C}(c_1\otimes_{\mathcal{C}}c_2 , c )
    \\
    & 
    = y(c_1 \otimes_{\mathcal{C}} c_2 )(c)
  \end{aligned}
  \,.
$$

=--



## Functors with smash product
 {#FunctorsWithSmashProduct}

+-- {: .num_defn #LaxMonoidalFunctor}
###### Definition

Let $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ be two (pointed) [[topologically enriched category|topologically enriched]] [[monoidal categories]] (def. \ref{MonoidalCategory}). A topologically enriched **lax monoidal functor** between them is

1. a [[topologically enriched functor]] 

   $$
     F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
     \,,
   $$

1. a morphism

   $$
     \epsilon \;\colon\; 1_{\mathcal{D}} \longrightarrow F(1_{\mathcal{C}})
   $$  

1. a [[natural transformation]]

   $$
     \mu_{x,y} 
       \;\colon\; 
     F(x) \otimes_{\mathcal{D}} F(y) 
       \longrightarrow 
     F(x \otimes_{\mathcal{C}} y)
   $$

   for all $x,y \in \mathcal{C}$

satisfying the following conditions:

1. **([[associativity]])** For all objects $x,y,z \in \mathcal{C}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (F(x) \otimes_{\mathcal{D}} F(y)) \otimes_{\mathcal{D}} F(z)
         &\underoverset{\simeq}{a^{\mathcal{D}}_{F(x),F(y),F(z)}}{\longrightarrow}&
       F(x) \otimes_{\mathcal{D}}( F(y)\otimes_{\mathcal{D}} F(z) )
       \\
       {}^{\mathllap{\mu_{x,y} \otimes id}}\downarrow 
         && 
       \downarrow^{\mathrlap{id\otimes \mu_{y,z}}}
       \\
       F(x \otimes_{\mathcal{C}} y) \otimes_{\mathcal{D}} F(z)
        &&
       F(x) \otimes_{\mathcal{D}} ( F(x \otimes_{\mathcal{C}} y) )
       \\
       {}^{\mathllap{\mu_{x \otimes_{\mathcal{C}} y , z} } }\downarrow 
         && 
       \downarrow^{\mathrlap{\mu_{ x, y \otimes_{\mathcal{C}} z  }}}
       \\
       F( ( x \otimes_{\mathcal{C}} y ) \otimes_{\mathcal{C}} z  )
         &\underset{F(a^{\mathcal{C}}_{x,y,z})}{\longrightarrow}&
       F( x \otimes_{\mathcal{C}} ( y \otimes_{\mathcal{C}} z ) )
     }
     \,,
   $$

   where $a^{\mathcal{C}}$ and $a^{\mathcal{D}}$ denote the [[associators]] of the monoidal categories;


1. **([[unitality]])** For all $x \in \mathcal{C}$ the following [[commuting diagram|diagrams commutes]]

   $$
     \array{
       1_{\mathcal{D}} \otimes_{\mathcal{D}} F(x)
         &\overset{\epsilon \otimes id}{\longrightarrow}&
       F(1_{\mathcal{C}}) \otimes_{\mathcal{D}} F(x)
       \\
       {}^{\mathllap{\ell^{\mathcal{D}}_{F(x)}}}\downarrow 
         && 
       \downarrow^{\mathrlap{\mu_{1_{\mathcal{C}}, x }}}
       \\
       F(x) 
         &\overset{F(\ell^{\mathcal{C}}_x )}{\longleftarrow}&
       F(1 \otimes_{\mathcal{C}} x  )
     }
   $$

   and  

   $$
     \array{
       F(x) \otimes_{\mathcal{D}}  1_{\mathcal{D}}
         &\overset{id \otimes \epsilon }{\longrightarrow}&
       F(x) \otimes_{\mathcal{D}}  F(1_{\mathcal{C}}) 
       \\
       {}^{\mathllap{r^{\mathcal{D}}_{F(x)}}}\downarrow 
         && 
       \downarrow^{\mathrlap{\mu_{x, 1_{\mathcal{C}} }}}
       \\
       F(x) 
         &\overset{F(r^{\mathcal{C}}_x )}{\longleftarrow}&
       F(x \otimes_{\mathcal{C}} 1  )
     }
     \,,
   $$

   where $\ell^{\mathcal{C}}$, $\ell^{\mathcal{D}}$, $r^{\mathcal{C}}$, $r^{\mathcal{D}}$ denote the left and right [[unitors]] of the two monoidal categories, respectively.

If $\epsilon$ and alll $\mu_{x,y}$ are [[isomorphisms]], then $F$ is called a **strong monoidal functor**. 

If moreover $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ are equipped with the structure of [[braided monoidal categories]] (def. \ref{BraidedMonoidalCategory}), then the lax monoidal functor $F$ is called a **[[braided monoidal functor]]** if in addition the following [[commuting diagram|diagram commutes]] for all objects $x,y \in \mathcal{C}$

$$
  \array{
    F(x) \otimes_{\mathcal{C}} F(y)
      &\overset{\tau^{\mathcal{D}}_{F(x), F(y)}}{\longrightarrow}&
    F(y) \otimes_{\mathcal{D}} F(x)
    \\
    {}^{\mathllap{\mu_{x,y}}}\downarrow 
      && 
    \downarrow^{\mathrlap{\mu_{y,x}}}
    \\
    F(x \otimes_{\mathcal{C}} y )
      &\underset{F(\tau^{\mathcal{C}}_{x,y}  )}{\longrightarrow}&
    F( y \otimes_{\mathcal{C}} x )
  }
  \,.
$$

A [[homomorphism]] $f\;\colon\; (F_1,\mu_1, \epsilon_1) \longrightarrow (F_2, \mu_2, \epsilon_2)$ between two (braided) lax monoidal functors is a **[[monoidal natural transformation]]**, in that it is

* a [[natural transformation]] $f_x \;\colon\; F_1(x) \longrightarrow F_2(x)$ of the underlying functors

compatible with the product and the unit in that the following [[commuting diagram|diagrams commute]] for all objects $x,y \in \mathcal{C}$:

$$
  \array{
    F_1(x) \otimes_{\mathcal{D}} F_1(y)
      &\overset{f(x)\otimes_{\mathcal{D}} f(y)}{\longrightarrow}&
    F_2(x) \otimes_{\mathcal{D}} F_2(y)
    \\
    {}^{\mathllap{(\mu_1)_{x,y}}}\downarrow
     &&
    \downarrow^{\mathrlap{(\mu_2)_{x,y}}}
    \\
    F_1(x\otimes_{\mathcal{C}} y)
     &\underset{f(x \otimes_{\mathcal{C}} y ) }{\longrightarrow}&
    F_2(x \otimes_{\mathcal{C}} y)
  }
$$

and 

$$
  \array{
    && 1_{\mathcal{D}}
    \\
    & {}^{\mathllap{\epsilon_1}}\swarrow && \searrow^{\mathrlap{\epsilon_2}}
    \\
    F_1(1_{\mathcal{C}})
     &&\underset{f(1_{\mathcal{C}})}{\longrightarrow}&&
    F_2(1_{\mathcal{C}})
  }
  \,.
$$

We write $MonFun(\mathcal{C},\mathcal{D})$ for the resulting [[category]] of lax monoidal functors between monoidal categories $\mathcal{C}$ and $\mathcal{D}$, similarly $BraidMonFun(\mathcal{C},\mathcal{D})$ for the category of braided monoidal functors between [[braided monoidal categories]], and $SymMonFun(\mathcal{C},\mathcal{D})$ for the category of braided monoidal functors between [[symmetric monoidal categories]].

=--

+-- {: .num_remark}
###### Remark

In the literature the term "monoidal functor" often refers by default to what in def. \ref{LaxMonoidalFunctor} is called a strong monoidal functor.  But for the purpose of the discussion of [[functors with smash product]] [below](#FunctorsWithSmashProduct), it is crucial to admit the generality of lax monoidal functors.

If $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ are [[symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}) then a braided monoidal functor (def. \ref{LaxMonoidalFunctor}) between them  is often called a **[[symmetric monoidal functor]]**. 

=--

+-- {: .num_defn #ModuleOverAMonoidalFunctor}
###### Definition

Let $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ be two (pointed) [[topologically enriched category|topologically enriched]] [[monoidal categories]] (def. \ref{MonoidalCategory}), and let $F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ be a [[topologically enriched functor|topologically enriched]] [[lax monoidal functor]] between them, with product operation $\mu$.

Then a left **[[module over a monoidal functor|module over the lax monoidal functor]]** is 

1. a [[topologically enriched functor]] 

   $$
     G \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
     \,;
   $$

1. a [[natural transformation]] 
 
   $$
     \rho_{x,y} 
       \;\colon\; 
     F(x) \otimes_{\mathcal{D}} N(y)
      \longrightarrow
    N(x \otimes_{\mathcal{C}} y )
   $$

such that

* **(action property)** For all objects $x,y,z \in \mathcal{C}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (F(x) \otimes_{\mathcal{D}} F(y)) \otimes_{\mathcal{D}} G(z)
         &\underoverset{\simeq}{a^{\mathcal{D}}_{F(x),F(y),F(z)}}{\longrightarrow}&
       F(x) \otimes_{\mathcal{D}}( F(y)\otimes_{\mathcal{D}} G(z) )
       \\
       {}^{\mathllap{\mu_{x,y} \otimes id}}\downarrow 
         && 
       \downarrow^{\mathrlap{id\otimes \rho_{y,z}}}
       \\
       F(x \otimes_{\mathcal{C}} y) \otimes_{\mathcal{D}} G(z)
        &&
       F(x) \otimes_{\mathcal{D}} ( G(x \otimes_{\mathcal{C}} y) )
       \\
       {}^{\mathllap{\rho_{x \otimes_{\mathcal{C}} y , z} } }\downarrow 
         && 
       \downarrow^{\mathrlap{\rho_{ x, y \otimes_{\mathcal{C}} z  }}}
       \\
       G( ( x \otimes_{\mathcal{C}} y ) \otimes_{\mathcal{C}} z  )
         &\underset{F(a^{\mathcal{C}}_{x,y,z})}{\longrightarrow}&
       G( x \otimes_{\mathcal{C}} ( y \otimes_{\mathcal{C}} z ) )
     }
     \,,
   $$

A [[homomorphism]] $f\;\colon\; (G_1, \rho_1) \longrightarrow (G_2,\rho_2)$ between two modules over a monoidal functor $(F,\mu,\epsilon)$ is 

* a [[natural transformation]] $f_x \;\colon\; N_1(x) \longrightarrow N_2(x)$ of the underlying functors

compatible with the action in that the following [[commuting diagram|diagram commute]] for all objects $x,y \in \mathcal{C}$:

$$
  \array{
    F(x) \otimes_{\mathcal{D}} N_1(y)
      &\overset{id \otimes_{\mathcal{D}} f(y)}{\longrightarrow}&
    F(x) \otimes_{\mathcal{D}} N_2(y)
    \\
    {}^{\mathllap{(\rho_1)_{x,y}}}\downarrow
     &&
    \downarrow^{\mathrlap{(\rhi_2)_{x,y}}}
    \\
    N_1(x\otimes_{\mathcal{C}} y)
     &\underset{f(x \otimes_{\mathcal{C}} y ) }{\longrightarrow}&
    N_2(x \otimes_{\mathcal{C}} y)
  }
$$

We write $F Mod$ for the resulting category of modules over the monoidal functor $F$.

=--


+-- {: .num_prop #DayMonoidsAreLaxMonoidalFunctorsOnTheSite}
###### Proposition

Let $(\mathcal{C},\otimes I)$ be a pointed [[topologically enriched category]] ([[symmetric monoidal category]]) [[monoidal category]] (def. \ref{MonoidalCategory}). Regard $(Top_{cg}^{\ast/}, \wedge , S^0)$ as a topological [[symmetric monoidal category]] as in example \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}.

Then ([[commutative monoid in a symmetric monoidal category|commutative]]) [[monoid in a monoidal category|monoids in]] (def. \ref{MonoidsInMonoidalCategory}) the [[Day convolution]] monoidal category $([\mathcal{C}, Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{C}}))$ of prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure} are equivalent to ([[braided monoidal functor|braided]]) [[lax monoidal functors]] (def. \ref{LaxMonoidalFunctor}) of the form

$$
  (\mathcal{C},\otimes, I) \longrightarrow (Top^{\ast}_{cg}, \wedge, S^0)
  \,,
$$

called **functors with smash products** on $\mathcal{C}$, i.e. there are [[equivalences of categories]] of the form

$$
  \begin{aligned}
    Mon([\mathcal{C},Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{C}}))
      &\simeq
    MonFunc(\mathcal{C},Top^{\ast/}_{cg})
    \\
    CMon([\mathcal{C},Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{C}}))
      &\simeq
    SymMonFunc(\mathcal{C},Top^{\ast/}_{cg})
  \end{aligned}
  \,.
$$

Moreover, [[module objects]] over these monoid objects are equivalent to the corresponding [[modules over monoidal functors]].

=--

This is stated in some form in ([Day 70, example 3.2.2](Day+convolution#Day70)). It is highlighted again in ([MMSS 00, prop. 22.1](#MMSS00)). 

+-- {: .proof}
###### Proof

By definition \ref{LaxMonoidalFunctor}, a [[lax monoidal functor]] $F \colon \mathcal{C} \to Top^{\ast/}_{cg}$ is a topologically enriched functor equipped with a morphism of [[pointed topological spaces]] of the form

$$
  S^0 \longrightarrow F(1_{\mathcal{C}})
$$

and equipped with a [[natural transformation|natural]] system of maps of pointed topological spaces of the form

$$
  F(c_1) \wedge F(c_2) \longrightarrow F(c_1 \otimes_{\mathcal{C}} c_2)
$$

for all $c_1,c_2 \in \mathcal{C}$.

Under the [[Yoneda lemma]] (prop. \ref{YonedaReductionTopological}) the first of these is equivalently a morphism in $[\mathcal{C}, Top^{\ast/}_{cg}]$ of the form

$$
  y(S^0) \longrightarrow F
  \,.
$$

Moreover, under the [[natural isomorphism]] of corollary \ref{DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor} the second of these is equivalently a morphism in $[\mathcal{C}, Top^{\ast/}_{cg}]$ of the form

$$
  F \otimes_{Day} F \longrightarrow F
  \,.
$$

Translating the conditions of def. \ref{LaxMonoidalFunctor} satisfied by a [[lax monoidal functor]] through these identifications gives precisely the conditions of def. \ref{MonoidsInMonoidalCategory} on a ([[commutative monoid in a symmetric monoidal category|commutative]]) [[monoid in a monoidal category|monoid in]] object $F$ under $\otimes_{Day}$.

Similarly for [[module objects]] and [[modules over monoidal functors]].

=--


+-- {: .num_prop #PullbackAlongLaxMonoidalFunctorPreservesMonoidsForDayConvolution}
###### Proposition

Let $f \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ be a [[lax monoidal functor]] (def. \ref{LaxMonoidalFunctor}) between pointed [[topologically enriched category|topologically enriched]] [[monoidal categories]] (def. \ref{MonoidalCategory}). Then the induced functor

$$
  f^\ast
    \;\colon\;
  [\mathcal{D}, Top^{\ast/}_{cg}]
    \longrightarrow
  [\mathcal{C}, Top_{cg}^{\ast}]
$$

given by $(f^\ast X)(c)\coloneqq X(f(c))$ preserves [[monoid in a monoidal category|monoids]] under [[Day convolution]]

$$
  f^\ast
    \;\colon\;
  Mon([\mathcal{D}, Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{D}}))
    \longrightarrow
  Mon([\mathcal{C}, Top_{cg}^{\ast}], \otimes_{Day}, y(1_{\mathcal{C}})
$$


Moreover, if $\mathcal{C}$ and $\mathcal{D}$ are [[symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}) and $f$ is a [[braided monoidal functor]] (def. \ref{LaxMonoidalFunctor}), then $f^\ast$ also preserves [[commutative monoids in a symmetric monoidal category|commutative monoids]]

$$
  f^\ast
    \;\colon\;
  CMon([\mathcal{D}, Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{D}}))
    \longrightarrow
  CMon([\mathcal{C}, Top_{cg}^{\ast}], \otimes_{Day}, y(1_{\mathcal{C}})
  \,.
$$


=--

+-- {: .proof}
###### Proof

This is an immediate corollary of prop. \ref{DayMonoidsAreLaxMonoidalFunctorsOnTheSite}, since the composite of two (braided) lax monoidal functors is itself canonically a (braided) lax monoidal functor.

=--





## Examples


### For excisive functors


+-- {: .num_defn #FinitePointedCWComplexes}
###### Definition

Write 

$$
  \iota_{fin}\;\colon\; Top^{\ast/}_{cg,fin} \hookrightarrow Top^{\ast/}_{cg}
$$ 

for the [[full subcategory]] of [[pointed topological spaces|pointed]] [[compactly generated topological spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#Top)) on those that admit the structure of a [[finite CW-complex]] (a [[CW-complex]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicalCellComplex)) with a [[finite number]] of cells). 

We say that the pointed topological [[enriched functor category]] (def. \ref{PointedTopologicalFunctorCategory})

$$
  Exc(Top_{cg})
   \coloneqq 
  [Top^{\ast/}_{cg,fin}, Top^{\ast/}_{cg}]
$$

is the category of **[[pre-excisive functors]]**. 

Write

$$
  \mathbb{S}_{exc}
    \coloneqq
  y(S^0)
  \coloneqq
  Top^{\ast/}_{cg,fin}(S^0,-)
$$

for the [[representable functor|functor co-represented]] by [[0-sphere]]. This is equivalently the inclusion $\iota_{fin}$ itself:

$$
  \mathbb{S}_{exc} = \iota_{fin} 
    \;\colon\;
  K \mapsto K
  \,.
$$

We call this the standard incarnation of the **[[sphere spectrum]]** as a pre-excisive functor.

By prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure} the [[smash product]] of [[pointed topological spaces|pointed]] [[compactly generated topological spaces]] induces the structure of a [[closed monoidal category|closed]] (def. \ref{ClosedMonoidalCategory}) [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory})

$$
  \left( 
    Exc(Top_{cg})
    ,\;
    \wedge_{Day}
    ,\; 
   \mathbb{S}_{exc}
  \right)
$$

with 

1. [[tensor unit]] the [[sphere spectrum]] $\mathbb{S}_{exc}$;

1. [[tensor product]] the [[Day convolution product]] $\otimes_{Day}$ from def. \ref{TopologicalDayConvolutionProduct},

   called the **[[symmetric monoidal smash product of spectra]]** for the model of pre-excisive functors;

1. [[internal hom]] the dual operation $[-,-]_{Day}$ from prop. \ref{DayMonoidalStructureIsClosed},

   called the **[[mapping spectrum]]** construction for pre-excisive functors.

=--

+-- {: .num_remark #EveryPreExcisiveFunctorIsSModule}
###### Remark

By example \ref{MonoidGivenByTensorUnit} the [[sphere spectrum]] incarnated as a pre-excisive functor $\mathbb{S}_{exc}$ (according to def. \ref{FinitePointedCWComplexes}) is canonically a [[commutative monoid in a symmetric monoidal category|commutative monoid in]] the category of pre-excisive functors  (def. \ref{MonoidsInMonoidalCategory})

Moreover, by example \ref{EveryObjectIsModuleOverTensorUnit}, every object of $Exc(Top_{cg})$ (def. \ref{FinitePointedCWComplexes}) is canonically a [[module object]] over $\mathbb{S}_{exc}$. We may therefore tautologically identify the category of pre-excisive functors with the [[module category]] over the sphere spectrum:

$$
  Exc(Top_{cg})
    \simeq
  \mathbb{S}_{exc}Mod
  \,.
$$

=--

We now consider restricting the domain of the pre-excisive functors of def. \ref{FinitePointedCWComplexes}.

+-- {: .num_defn #TopologicalDiagramCategoriesForSpectra}
###### Definition

Define the following [[pointed topologically enriched categories|pointed topologically enriched]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)) [[symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}):

1. $Seq$ is the category whose objects are the [[natural numbers]] and which has only identity morphisms and [[zero morphisms]] on these objects, hence the [[hom-spaces]] are

   $$
     Seq(n_1,n_2) = 
     \left\{
       \array{
          S^0 & for\; n_1 = n_2
          \\
          \ast & otherwise
       }
    \right.
   $$

   The tensor product is the addition of natural numbers, $\otimes = +$, and the [[tensor unit]] is 0. 

1. $Sym$ is the standard [[skeletal category|skeleton]] of the [[core]] of [[FinSet]] with [[zero morphisms]] adjoined: its [[objects]] are the [[finite sets]] $\{1, \cdots,n\}$ for $n \in \mathbb{N}$, all non-[[zero morphism|zero]] morphisms are [[automorphisms]] and the [[automorphism group]] of $\{1,\cdots,n\}$ is the [[symmetric group]] $\Sigma_n$, hence the [[hom-spaces]] are the following [[discrete topological spaces]]:

   $$
     Sym(n_1, n_2) =
     \left\{
       \array{
          (\Sigma_{n_1})_+ & for \; n_1 = n_2
          \\
          \ast & otherwise
       }
     \right.
   $$

   The tensor product is the [[disjoint union]] of sets, tensor unit is the [[empty set]].

1. $Orth$ has as objects finite dimenional real linear [[inner product spaces]] $(V, \langle -,-\rangle)$ and as non-zero morphisms the [[linear map|linear]] [[isometry|isometric]] [[isomorphisms]] between these; hence the [[automorphism group]] of the object $(V, \langle -,-\rangle)$ is the [[orthogonal group]] $O(V)$; the monoidal product is [[direct sum]] of linear spaces, the tensor unit is the 0-vector space; again we turn this into a $Top^{\ast/}$-enriched category by adjoining a basepoint to the hom-spaces;
  
   $$
     Orth(V_1,V_2) 
     \simeq
     \left\{
        \array{
          O(V_1)_+ & for \; dim(V_1) = dim(V_2)
          \\
          \ast & otherwise
        }
     \right.
   $$


There is a sequence of canonical [[faithful functor|faithful]] pointed topological [[subcategory]] inclusions 

$$
 \array{
   Seq 
     &\stackrel{seq}{\hookrightarrow}& 
   Sym 
    &\stackrel{sym}{\hookrightarrow}& 
   Orth 
     &\stackrel{orth}{\hookrightarrow}& 
   Top_{cg,fin}^{\ast/}
   \\
   n 
    &\mapsto& 
   \{1,\cdots, n\} 
     &\mapsto& 
   \mathbb{R}^n 
    &\mapsto& 
   S^n
   \\
    && 
    && 
   V
    &\mapsto& 
   S^V
  }
  \,,
$$

into the pointed topological category of pointed compactly generated topological spaces of finite CW-type (def. \ref{FinitePointedCWComplexes}).

Here $S^V$ denotes the [[one-point compactification]] of $V$. On morphisms $sym \colon (\Sigma_n)_+ \hookrightarrow (O(n))_+$ is the canonical inclusion of [[permutation]] matrices into [[orthogonal group|orthogonal]] matrices and $orth \colon O(V)_+ \hookrightarrow Aut(S^V)$ is on $O(V)$ the [[topological subspace]] inclusions of the pointed [[homeomorphisms]] $S^V \to S^V$ that are induced under forming [[one-point compactification]] from linear isometries of $V$ ("[[representation spheres]]").


Consider the sequence of restrictions of topological diagram categories, according to prop. \ref{PullbackAlongLaxMonoidalFunctorPreservesMonoidsForDayConvolution} along the above inclusions:

$$
  Exc(Top_{cg})
    \overset{orth^\ast}{\longrightarrow}
  [Orth,Top^{\ast/}_{cg}]
    \overset{sym^\ast}{\longrightarrow}
  [Sym,Top^{\ast/}_{cg}]
    \overset{seq^\ast}{\longrightarrow}
  [Seq,Top^{\ast/}_{cg}]
  \,.
$$

Write 

$$
  \mathbb{S}_{Orth} \coloneqq orth^\ast \mathbb{S}_{exc} 
  \,,
  \;
  \mathbb{S}_{Sym} \coloneqq sym^\ast \mathbb{S}_{orth} 
  \,,
  \;
  \mathbb{S}_{Seq} \coloneqq seq^\ast \mathbb{S}_{sym} 
$$

for the restriction of the excisive functor incarnation of the [[sphere spectrum]] (from def. \ref{FinitePointedCWComplexes}) along these inclusions.

=--


+-- {: .num_remark}
###### Remark


Since $\mathbb{S}_{exc}$ is the [[tensor unit]] with repect to the [[Day convolution]] product on pre-excisive functors, and since it is therefore canonically a [[commutative monoid]], by prop. \ref{PullbackAlongLaxMonoidalFunctorPreservesMonoidsForDayConvolution}, all these restricted sphere spectra are still [[monoid object|monoids]]. However, while $orth$ and $sym$ are [[braided monoidal functors]], the functor $seq$ is not braided, hence $\mathbb{S}_{orth}$ and $\mathbb{S}_{sym}$ are commutative monoids, but $\mathbb{S}_{Seq}$ is not commutative.



| | $\mathbb{S}$ | $\mathbb{S}_{Orth}$ | $\mathbb{S}_{Sym}$ | $\mathbb{S}_{Seq}$ |
|--|--------------|---------------------|--------------------|-------------------|
| [[monoid in a monoidal category|monoid]] | yes | yes | yes | yes |
| [[commutative monoid in a symmetric monoidal category|commutative monoid]] | yes | yes | yes | no |
| [[tensor unit]] | yes | no | no | no |


=--


Therefore we may consider [[module objects]] over the restrictions of [[generalized the|the]] [[sphere spectrum]] from def. \ref{TopologicalDiagramCategoriesForSpectra}.

+-- {: .num_prop #HighlyStructuredSpectraAsDayConvolutionSModules}
###### Proposition

The [[categories of modules]] (def. \ref{ModulesInMonoidalCategory}) over $\mathbb{S}_{Orth}$, $\mathbb{S}_{Sym}$ and $\mathbb{S}_{Seq}$ (def. \ref{TopologicalDiagramCategoriesForSpectra}) are [[equivalence of categories|equivalent]], respectively, to the categories of [[orthogonal spectra]], [[symmetric spectra]] and [[sequential spectra]] (in [[compactly generated topological spaces]]):

$$
  \mathbb{S}_{Orth} Mod \simeq OrthSpec(Top_{cg})
$$

$$
  \mathbb{S}_{Sym} Mod \simeq SymSpec(Top_{cg})
$$

$$
  \mathbb{S}_{Seq} Mod \simeq SeqSpec(Top_{cg})
  \,.
$$

=--

+-- {: .proof}
###### Proof

Write $\mathbb{S}_{dia}$ for any of the three monoids. By prop. \ref{DayMonoidsAreLaxMonoidalFunctorsOnTheSite}, left modules with respect to [[Day convolution]] are equivalently [[modules over monoidal functors]] over the monoidal functor corresponding to $\mathbb{S}_{dia}$. This means that for $\mathbb{S}_{Sym}$ and $\mathbb{S}_{Seq}$ they are functors $X \colon Sym \longrightarrow sSet^{\ast/}$ or $X \colon Seq \longrightarrow sSet^{\ast/}$, respectively equipped with [[natural transformations]]

$$
  S^1 \wedge X_p   \longrightarrow X_{p+q}
$$

satisfying the evident [[categorification|categorified]] [[action]] property. In the present case this action property says that these morphisms are determined by 

$$
  S^1 \wedge X_p  \longrightarrow X_{p+1}
$$

under the isomorphisms $S^p \simeq S^1 \wedge S^{p-1}$. Naturality of all these morphisms as functors on $Sym$ is the equivariance under the symmetric group actions in the definition of [[symmetric spectra]]. 

Similarly, modules over $\mathbb{S}_{Orth}$ are equivalently functors

$$
  S^W \wedge X_V   \longrightarrow X_{V \oplus W}
$$

etc. and their functoriality embodies the [[orthogonal group]]-equivariance in the definition of [[orthogonal spectra]].


=--

### For orthogonal spectra

Consider the non-full inclusion of [[topologically enriched categories]]

$$
  Orth \hookrightarrow Top^{\ast/}_{cg,fin}
$$

on the standard [[n-spheres]] $S^n \coloneqq (S^1)^{\wedge^n}$, with [[hom-spaces]] given by the [[orthogonal groups]] with basepoint adjoint, acting on these spheres as their canonical [[representation spheres]]

$$
  Orth(S^{n_1}, S^{n_2})
   \coloneqq
  \left\{
    \array{
      O(n_1)_+ & if \; n_1= n_2
      \\
      \ast & otherwise
    }
  \right.
  \,.
$$

Regard Orth as a [[monoidal category]] with monoidal structure induced form $(Top^{\ast/}_{cg}, \wedge, S^0)$ (via example \ref{TopAsASymmetricMonoidalCategory}) under the restriction. This makes the inclusion a [[braided monoidal functor|braided]] [[monoidal functor]].


Restricting the standard pre-excisive model $y(S^0)$ of the [[sphere spectrum]] yields $\mathbb{S}_{orth}$. Since restriction is a monoidal functor, and since $y(S^0)$ is the tensor unit and hence canonically a monoid, prop. \ref{PullbackAlongLaxMonoidalFunctorPreservesMonoidsForDayConvolution} says that $\mathbb{S}_{orth}$ is still a commutative monoid with respect to Day convolution:

$$
  CMon([Top^{\ast/}_{cg,fin}, Top^{\ast/}_{cg}], \otimes_{Day}, y(S^0))
  \longrightarrow
  CMon([Orth, Top^{\ast/}_{cg}], \otimes_{Day}, y(S^0))
$$

$$
  (\mathbb{S}_{exc},\mu = id,e = id) \mapsto (\mathbb{S}_{orth}, \mu, e)
  \,.
$$

The category of [[orthogonal spectra]] is the category of $\mathbb{S}_{orth}$-modules (def. \ref{ModulesInMonoidalCategory}):

$$
  \begin{aligned}
    OrthSpec(Top_{cg})
    &=
    \mathbb{S}_{orth}Mod( [Top^{\ast/}_{cg,fin}, Top^{\ast/}_{cg}] )
  \end{aligned}
  \,,
$$



Since $\mathbb{S}_{orth}$ is a commutative monoid, prop. \ref{MonoidalCategoryOfModules} says that there is a [[symmetric monoidal category]] structure $\otimes_{\mathbb{S}_{orth}}$ on $OrthSpec(Top_{cg})$.
This is the [[symmetric monoidal smash product of spectra]] for orthogonal spectra.

An orthogonal _[[ring spectrum]]_ $E$ is a monoid with respect to $\otimes_{\mathbb{S}_{orth}}$, hence an $\mathbb{S}_{orth}$-[[associative algebra|algebra]] (def. \ref{AAlgebra}). By prop. \ref{AlgebrasOverAAreMonoidsUnderA}, such $E$ is equivalently a monoid with respect to $\otimes_{Day}$ and equipped with a monoid homomorphism $\mathbb{S}_{orth} \longrightarrow E$. Finally, by prop. \ref{DayMonoidsAreLaxMonoidalFunctorsOnTheSite} this is equivalently a functor with smash products

$$
  E \;\colon\; Orth \longrightarrow Top^{\ast/}_{cg}
$$

equipped with a natural transformation of functors with smash product

$$
  \mathbb{S}_{orth} \longrightarrow E
  \,.
$$


In the terminology of [MMSS 00, def. 22.5](#MMSS00) this is an "$Orth$-FSP over $\mathbb{S}_{Orth}$".

### Symmetric spectra

Restrict further along the non-full inclusion

$$
  Sym \hookrightarrow Orth \hookrightarrow Top^{\ast/}_{cg,fin}
  \,,
$$

where $Sym$ has the same objects, but the [[hom-spaces]] are now just the [[symmetric groups]] (with basepoint adjoint)

$$
  \Sigma_n \hookrightarrow O(n)
  \,.
$$

Then proceed as for orthogonal spectra.

### For sequential spectra (non-example)

Restrict further along 

$$
  Seq \hookrightarrow Sym \hookrightarrow Orth \hookrightarrow Top^{\ast/}_{cg}
  \,,
$$

where $Seq$ still has the same objects, the $n$-spheres, but no non-trivial morphisms (just the identity morphisms and the zero morphisms).

Now the inclusion $Seq \longrightarrow Top^{\ast/}_{cg}$ is no longer a [[braided monoidal functor]], for the braiding on $Seq$ is trivial, while on $Top^{\ast/}_{cg}$ it is not. Accordingly the assumption of the second clause in prop. \ref{PullbackAlongLaxMonoidalFunctorPreservesMonoidsForDayConvolution} is vialoted.

Indeed, restricting $\mathbb{S}$ along this inclusion yields the stndard sequential [[sphere spectrum]] $\mathbb{S}_{seq}$ which is still a monoid with respect to Day convolution, but not a commutative monoid anymore (see at [smash product of spectra -- graded commutativity](smash+product+of+spectra#GradedCommutativity)) and hence the assumption of prop. \ref{MonoidalCategoryOfModules} is violated. 

The $\mathbb{S}_{seq}$-[[module objects]] (def. \ref{ModulesInMonoidalCategory}) are equivalently the [[sequential spectra]].

But since $\mathbb{S}_{seq}$ is not a commutative monoid, the assumption of prop. \ref{MonoidalCategoryOfModules}  there is no induced tensor product on $\mathbb{S}_{seq}Mod$ and hence the story ends here. 


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

Based on discussion in

* {#EKMM97} [[Anthony Elmendorf]], [[Igor Kriz]], [[Michael Mandell]], [[Peter May]], _Rings, modules and algebras in stable homotopy theory_ 1997 ([pdf](www.math.uchicago.edu/~may/BOOKS/EKMM.pdf))


[[!redirects FSP]]
[[!redirects FSPs]]

[[!redirects functors with smash product]]

[[!redirects functor with smash products]]
[[!redirects functors with smash products]]
