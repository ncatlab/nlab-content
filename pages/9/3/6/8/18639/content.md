
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


# Funny tensor products

* table of contents
{: toc}

## Definition

For [[categories]] $C,D$, let $C \Rightarrow D$ be the category whose [[objects]] are [[functors]] from $C$ to $D$ and whose [[morphisms]] are [[unnatural transformations]].  This makes $Cat$ into a [[closed category]].  We can then define a [[tensor product]] by a [[universal property]] and make $Cat$ into a [[symmetric closed monoidal category]] $(Cat,\Box)$; this tensor product $\Box$ is called the **funny tensor product**.  

As shown by [Foltz, Lair & Kelly 1980](#FoltzLairKelly80), this constitutes one of precisely two [[symmetric monoidal closed category|symmetric monoidal closed]] structures on the [[1-category]] [[Cat|$Cat$]]; the other, of course, is the [[cartesian closed category]] structure. Both the funny product and the cartesian product are [[semicartesian monoidal category|semicartesian monoidal]]. 

More explicitly, the category $C \Box D$ can be defined as the pushout

$$\array{
C_0 \times D_0 & \to & C_0 \times D \\
\downarrow &&\downarrow  \\
C \times D_0 & \to & C \Box D
}$$

where $C_0,D_0$ are the [[discrete categories]] of objects of $C,D$ and the maps are the inclusions.

The funny tensor product can also be generalized to [[higher categories]].

## Separate functoriality
 {#SeparateFunctoriality}

A functor $F : C \Box D \to E$ can be described as being a functor of 2-variables that is "separately" functorial in the $C$ and $D$ arguments, in analogy with separate continuity. (See at [[multifunctor]] -- [separately functorial maps](multifunctor#SeparatelyFunctorialMaps)).

That is, it has an action on objects $F : C_0 \times D_0 \to E_0$ and for each object $c \in C$, a functorial action $F(id_c,-) : D \to E$ and for each object $d \in D$, a functorial action $F(-,id_d) : C \to E$, both of which agree on objects with $F$.

Contrast this to a "jointly" functorial functor of 2-arguments, also known as a [[bifunctor]], which is equivalent to a functor from the cartesian product $F : C \times D \to E$ where we have to define for any $f : c \to c'$ and $g : d \to d'$ a morphism $F(f,g) : F(c,d) \to F(c',d')$. With a separately functorial $F$, there are two candidates for this morphism: $F(f,id) \circ F(id,g)$ and $F(id,g) \circ F(f,id)$ that are not in general equal.

For a simple example of a separately functorial action that is not a bifunctor, consider the identity functor on $2 \Box 2$ where $2$ is the [[interval category|walking arrow category]]. If we label one copy of $2$ as $\top \to \bot$ and the other as $l \to r$ then $2 \Box 2$ is a non-commuting square:

$$\array{
(\top,l) & \to & (\top,r) \\
\downarrow &&\downarrow  \\
(\bot,l) & \to & (\bot,r)
}$$

then viewing the identity as a functor of 2-arguments, we get an obvious separately functorial action, but since the square does not commute, it is not a bifunctor.

## Enrichment

Categories enriched in the funny tensor product monoidal structure are precisely [[sesquicategories]].

## Related pages

* [[Gray tensor product]]
* Separately functorial functors arise naturally when studying effectful languages where the two sequencings of $F(f,id)$ and $F(id,g)$ correspond to the choices of order of evaluation of the two functions. See [[premonoidal category]] for more: a strict premonoidal category is precisely a monoid object in the monoidal category $(Cat, \Box)$, while a general premonoidal category is a pseudomonoid in the monoidal 2-category $(Cat, \Box)$. 

##References

* [[Mark Weber]], _Free products of higher operad algebras_, Theory and Applications of Categories **28** 2 (2013) 24-65. ([arXiv](https://arxiv.org/abs/0909.4722), [TAC](http://www.tac.mta.ca/tac/volumes/28/2/28-02abs.html))

This paper shows that there are just two [[symmetric closed monoidal category|symmetric closed monoidal]] structures on [[Cat]], the cartesian product and the funny tensor product:

* {#FoltzLairKelly80} [[François Foltz]], [[Christian Lair]], [[G. M. Kelly]], *Algebraic categories with few monoidal biclosed structures or none*, Journal of Pure and Applied Algebra **17** 2 (1980) 171-177 &lbrack;[pdf](https://core.ac.uk/download/pdf/82322397.pdf), <a href="https://doi.org/10.1016/0022-4049(80)90082-1">doi:10.1016/0022-4049(80)90082-1</a>&rbrack;

