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

### Monoidal categories

+-- {: .num_defn #MonoidalCategory} 
###### Definition

A **[[monoidal category]]** is a [[category]] $\mathcal{C}$ equipped with 

1. a [[functor]]

   $$ 
      \otimes 
        \;\colon\; 
      \mathcal{C} \times \mathcal{C}  
       \longrightarrow
      \mathcal{C}
   $$

   called the **[[tensor product]]**, 

1. an object

   $$ 
     1 \in \mathcal{C} 
   $$

   called the **[[unit object]]** or **[[tensor unit]]**, 

1. a [[natural isomorphism]] 

   $$
     a 
       \;\colon\; 
     ((-)\otimes (-)) \otimes (-)
       \overset{\simeq}{\longrightarrow}
     (-) \otimes ((-)\otimes(-))
   $$

   with components of the form 


   $$ 
     a_{x,y,z} : (x \otimes y) \otimes z \to x \otimes (y \otimes z) 
   $$

   called the **[[associator]]**, 

1. a [[natural isomorphism]] 

   $$
     \lambda 
       \;\colon\; 
     (1 \otimes (-)) 
       \overset{\simeq}{\longrightarrow}
     (-)
   $$

   with components of the form 


   $$ 
     \lambda_x \colon 1 \otimes x \to x 
   $$

   called the **[[left unitor]]**, and a natural isomorphism 

   $$
     \rho \;\colon\; (-) \otimes 1 \overset{\simeq}{\longrightarrow} (-)
   $$

   with components of the form 


   $$  
     \rho_x \colon x \otimes 1 \to x 
   $$

    called the **[[right unitor]]**, 

such that the following two kinds of [[commuting diagram|diagrams commute]], for all objects involved:

1. **triangle identity** (not to be confused with the [[triangle identities]] of an [[adjunction]]):

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


1. the **[[pentagon identity]]** (or **pentagon equation**):

+-- {: style="text-align:center"}
[[!include monoidal category > pentagon]]
=--


=--


+-- {: .num_defn #BraidedMonoidalCategory} 
###### Definition

A **[[braided monoidal category]]**, is a [[monoidal category]] $\mathcal{C}$ (def. \ref{MonoidalCategory}) equipped with a [[natural isomorphism]]

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


A **[[symmetric monoidal category]]** is a [[braided monoidal category]] (def. \ref{BraidedMonoidalCategory}) for which the [[braiding]] 

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

The category [[Set]] of [[sets]] and [[functions]] between them becomes a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}) with [[tensor product]] the [[Cartesian product]] $\times$ of sets. The [[associator]], [[unitor]] and [[braiding]] isomorphism are the evident (almost unnoticable) canonical identifications.

Similarly the category [[Top]] of [[topological spaces]] and its [[full subcategory]] $Top_{cg}$ of [[compactly generated topological spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#kTop)) become [[symmetric monoidal categories]] with [[tensor product]] the corresponding [[Cartesian products]], hence the operation of forming (k-ified [cor.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)) [[product topological spaces]] ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#ProductTopologicalSpace)). The underlying functions of the [[associator]], [[unitor]] and [[braiding]] isomorphisms are just those of the underlying sets, as above. 
 
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

### Topological ends and coends

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

Here the object in the middle is just the set of sets of component morphisms $\left\{ F(c)\overset{\eta_c}{\to} G(c)\right\}_{c\in \mathcal{C}}$. The two parallel maps in the equalizer diagram take such a collection to the functions which send any $c \overset{f}{\to} d$ to the result of precomposing

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

+-- {: .num_example #NaturalTransformationsViaEnds}
###### Proposition
**(topologically [[enriched Yoneda lemma]])**

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched categories]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). For $F \colon \mathcal{C}\to Top^{\ast/}_{cg}$ a pointed [[topologically enriched functor]] and for $c\in \mathcal{C}$ an object, there is a [[natural isomorphism]]

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
