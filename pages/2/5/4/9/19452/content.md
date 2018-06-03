
This page is going to be one chapter in _[[geometry of physics]]_.

> under construction

$\,$

$\,$


We give here an introduction to the basic concepts and results of _[[category theory]]_ and of _[[topos theory]]_, aimed at providing background for the [[synthetic differential geometry|synthetic]] and [[higher differential geometry|higher]] [[geometry of physics -- supergeometry|supergeometry]] of relevance in formulations of fundamental [[physics]] (such as used in the chapters _[[geometry of physics -- A first idea of quantum field theory|on quantum field theory]]_ and _[[geometry of physics -- fundamental super p-branes|on fundamental super p-branes]]_).

One motivation for [[category theory]] and [[topos theory]] is _a posteriori_: As a matter of experience, there is just no other toolbox that allows to really understand and handle the [[higher differential geometry|higher]] [[supergeometry]] of relevance in [[physics]].

We offer also an _a priori_ motivation: _Category theory is the theory of duality._

<div style="float:right;margin:0 10px 10px 0;"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/74/Cup_or_faces_paradox.svg/450px-Cup_or_faces_paradox.svg.png" width="200"></div>

_[[duality|Duality]]_ is of course an ancient notion in [[philosophy]]. At least as a term, it makes a curious re-appearance in the conjectural [[theory (physics)|theory]] of fundamental [[physics]] formerly known as _[[string theory]]_. In both cases, the literature left some room in delienating what precisely is meant. But the philosophically inclined mathematician could notice (see [Lambek 82](adjoint+functor#Lambek82)) that an excellent candidate to make precise the idea of _[[duality]]_ is the mathematical concept of _[[adjoint functor|adjunction]]_, from [[category theory]].

Historically, [[category theory]] was introduced in order to make precise the concept of _[[natural transformation]]_: The concept of _[[functors]]_ was introduced just so as to support that of natural transformations, and the concept of _[[categories]]_ only served that of functors (see e.g. [Freyd 65, Part II](category+theory#Freyd65)). But natural transformations are what allows to define, in turn, the concept of _[[adjoint functors]]_, also called _[[adjunctions]]_ on categories. All the deep concepts of category theory (such as _[[representable functors]]_, _[[Yoneda embedding]]_, _[[Kan extensions]]_, hence _[[limits]]_ and _[[colimits]]_, to be introduced below) are special cases of [[adjoint functor]] constructions -- hence of dualities, if we follow [Lambek 82](adjoint+functor#Lambek82). Therefore it makes sense to regard category theory, to a large extent, as the **theory of adjunctions**, hence the **theory of duality**:


| hierarchy of concepts  | Definition |
|------------------------|------------|
| [[adjoint functor|adjunction]] / [[duality]]  | \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets} |
| [[natural transformation]] | \ref{NaturalTransformations} |
| [[functor]] | \ref{Functors} |
| [[category]] | \ref{Categories} |



The pivotal role of [[adjunctions]] in [[category theory]] ([Lawvere 08](adjoint+functor#fn:1)) and in the [[foundations of mathematics]] ([[Adjointness in Foundations|Lawvere 69]], [[Cohesive Toposes and Cantor's lauter Einsen|Lawvere 94]] ) was particularly amplified by [[F. W. Lawvere]].
Moreover, [[Lawvere]] saw the future of category theory
([[Some Thoughts on the Future of Category Theory|Lawvere 91]]) as concerned with [[adjunctions]] expressing systems of archetypical dualities that reveal foundations for [[geometry]] ([Lawvere 07](cohesive+topos#LawvereAxiomatic)) and [[physics]] ([[Toposes of laws of motion|Lawvere 97]]).
He suggested ([Lawvere 94](objective+and+subjective+logic#Lawvere94)) this as a precise formulation of core aspects of the _theory of everything_
of early 19th century [[philosophy]], before it fell out of favour: Hegel's _[[Science of Logic]]_.

These days, of course, _[[theories of everything]]_, such as [[string theory]], are understood less ambitiously than this ontological process,
as mathematical formulations of fundamental theories of physics, that could conceptually unify the hodge-podge of currently available "standard models" [[standard model of particle physics|of particle physics]] and [[standard model of cosmology|of cosmology]] to a more coherent whole.

The idea of _[[duality in string theory]]_ refers to different perspectives on physics that appear dual to each other while being _equivalent_.
One of the basic results of category theory, which we will discuss below, is that equivalence is indeed a special case of adjunction. 

But the usage of the word _[[duality in string theory]]_ is too loose as that one could expect to be able to refine each occurence of the term in the literature to a mathematical adjunction.  
However, we will see mathematical formalizations of core aspects of
key string-theoretic dualities, such as _[[topological T-duality]]_ and the _[[duality between M-theory and type IIA string theory]]_, in terms of adjunctions. Indeed, at the heart of these _[[dualities in string theory]]_ is the phenomenon of _[[double dimensional reduction]]_, which turns out to be formalized by one of the most fundamental adjunctions in ([[higher category theory|higher]] [[category theory]] ([[base change]] along the point inclusion into a [[classifying space]]).
This suggests that there may be a deeper relation here between the superficially alien uses of the word "duality", that is worth exploring.

In this respect it is worth noticing that core structure of string/M-theory arises via universal constructions from the [[superpoint]] (as explained in the chapter _[[geometry of physics -- fundamental super p-branes|on fundamental super p-branes]]_), while the superpoint itself arises, in a sense made precise by [[category theory]], "from nothing", by a system of twelve [[adjunctions]] (explained in the chapter [[geometry of physics -- supergeometry|on supergeometry]]). 

Here we introduce the requisites for understanding these statements.


## Categories

+-- {: .num_defn #Categories}
###### Definition
**([[category]])**

A _[[category]]_ $\mathcal{C}$ is 

1. a [[class]] $Obj_{\mathcal{C}}$, called the _class of [[objects]]_;

1. for each [[pair]] $X,Y \in Obj_{\mathcal{C}}$ of [[objects]], a [[set]] $Hom_{\mathcal{C}}(X,Y)$, called the _[[set of morphisms]] from $X$ to $Y$_.

   We denote the elements of this set by arrows like this:

   $$
     X \overset{f}{\longrightarrow} Y \;\;\in Hom_{\mathcal{C}}(X,Y)
     \,.
   $$ 

1. for each [[object]] $X \in Obj_{\mathcal{C}}$ a morphism 

   $$
      X \overset{id_X}{\to} X \;\; \in Hom_{\mathcal{C}}(X,X)
   $$

   called the _[[identity morphism]]_ on $X$;

1. for each [[triple]] $X_1, X_2, X_3 \in Obj$ of [[objects]], a [[function]]

   $$
     \array{
       Hom_{\mathcal{C}}(X_1, X_2) 
       &\times&
       Hom_{\mathcal{C}}(X_2, X_3) 
       &\overset{\circ_{X_1,X_2,X_3}}{\longrightarrow}&
       Hom_{\mathcal{C}}(X_1, X_3)
       \\
       X_1 \overset{f}{\to} X_2
       &,&
       X_2 \overset{f}{\to} X_3
       &\mapsto&
       X_1 \overset{ g \circ f }{\longrightarrow} X_3
     }
   $$

   called _[[composition]]_;

such that:

1. for all [[pairs]] of [[objects]] $X,Y \in Obj_{\mathcal{C}}$ [[unitality]] holds: given

   $$
     X \overset{f}{\to} Y \;\;\in Hom_{\mathcal{C}}(X,Y)
   $$

   then 

   $$
     X \overset{id_Y \circ f}{\longrightarrow} Y
     \;=\;
     X \overset{f}{\longrightarrow} Y
     \;=\;
     X \overset{f \circ id_X }{\longrightarrow} Y
     \,;
   $$

1. for all [[quadruples]] of [[objects]] $X_1, X_2, X_3, X_4 \in Obj_{\mathcal{C}}$ [[composition]] satifies _[[associativity]]_: given

   $$
     X_1 
       \overset{f_{12}}{\to} 
     X_2 
       \overset{f_{23}}{\to} 
     X_3
       \overset{f_{34}}{\to} 
     X_4 
   $$

   then 

   $$
     X_1 \overset{f_{34} \circ (f_{23} \circ f_{12})}{\longrightarrow} X_4
     \;\;=\;\;
     X_1 \overset{(f_{34} \circ f_{23}) \circ f_{12}}{\longrightarrow} X_4
     \,.
   $$

=--

+-- {: .num_example #CategoryOfAllSets}
###### Example
**([[Set|category of all sets]])**

The [[class]] of all [[sets]] with [[functions]] between them is a [[category]] (Def. \ref{Categories}), to be denoted _[[Set]]_:

* $Obj_{Set} = \text{class of all sets}$;

* $Hom_{Set}(X,Y) = \text{set of functions from set X to set Y}$;

* $id_X \in Hom_{Set}(X,X) = $ [[identity function]] on set $X$;

* $\circ_{X_1,X_2,X_3} = \text{ordinary composition of functions}. 

=--


+-- {: .num_defn #Functors}
###### Definition
**([[functor]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be two [[categories]] (Def. \ref{Categories}). A _[[functor]] from $\mathcal{C}$ to $\mathcal{D}$_, to be denoted

$$
  \mathcal{C} \overset{F}{\longrightarrow} \mathcal{D}
$$

is 

1. a [[function]] between the classes of [[objects]]:

   $$
     F_{Obj} \;\colon\; Obj_{\mathcal{C}} \longrightarrow Obj_{\mathcal{D}}
   $$

1. for each [[pair]] $X,Y \in Obj_{\mathcal{C}}$ of objects a [[function]]

   $$
     F_{X,Y} \;\colon\;  Hom_{\mathcal{C}}(X,Y) \longrightarrow Hom_{\mathcal{D}}(F_{Obj}(X), F_{Obj}(Y))

such that

1. For each [[object]] $X \in Obj_{\mathcal{C}}$ the [[identity morphism]] is respected:

   $$
     F_{X,X}(id_X) \;=\; id_{F_{Obj}(X)}
     \,;
   $$

1. for each [[triple]] $X_1, X_2, X_3 \in Obj_{\mathcal{C}}$ of [[objects]], [[composition]] is respected: given

   $$
      X_1 \overset{f}{\longrightarrow} X_2 \overset{g}{\longrightarrow} X_3
   $$

   then

   $$
      F_{X_1, X_3}(g \circ f ) \;=\;  F_{X_2, X_3}(g) \circ F_{X_1,X_2}(f)
      \,.
   $$

=--


+-- {: .num_defn #NaturalTransformations}
###### Definition
**([[natural transformation]])**

Given two [[categories]] $\mathcal{C}$ and $\mathcal{D}$ (Def. \ref{Categories}) and given two [[functors]] from $\mathcal{C}$ to $\mathcal{D}$ (Def. \ref{Functors}), then a _[[natural transformation]]_ from $F$ to $G$

$$
  \mathcal{C}
    \underoverset
      {\underset{G}{\longrightarrow}}
      {\overset{F}{\longrightarrow}}
      {\phantom{AA}\Downarrow \mathrlap{\eta} \phantom{AA}}
  \mathcal{D}
$$

is

* for each [[object]] $X \in Obj_{\mathcal{C}}$ a [[morphism]]

  $$
    F(X) \overset{ \eta_X }{\longrightarrow} G(X)
  $$

such that

* for each [[morphism]] $X \overset{f}{\longrightarrow} Y$ we have

  $$
    \eta_Y\circ F(X)
     \;=\;
    G(Y)\circ \eta_X
    \phantom{AAAAAA}
    \array{
       F(X) &\overset{\eta_X}{\longrightarrow}& G(X)
       \\
       {}^{\mathllap{F(f)}}\downarrow 
         && 
       \downarrow^{\mathrlap{G(f)}}
       \\
       F(Y) &\underset{\eta_Y}{\longrightarrow}& G(Y)
    }
  $$

=--

+-- {: .num_defn #AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}
###### Definition
**([[adjoint functor|adjunction]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be two [[categories]] (Def. \ref{Categories}), and let 

$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{}
  \mathcal{C}
$$

be a [[pair]] of [[functors]] between them (Def. \ref{Functors}), as shown. Then this is called a _pair of [[adjoint functors]]_ (or an _[[adjoint pair]] of [[functors]]_) with $L$ _[[left adjoint]]_ and $R$ _[[right adjoint]]_, denoted 

$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{\bot}
  \mathcal{C}
$$

if there exists a [[natural isomorphism]] between the [[hom-functors]] of the following form:

\[
  \label{HomIsomorphismForAdjointFunctors}
  Hom_{\mathcal{D}}(L(-),-) \;\simeq\; Hom_{\mathcal{C}}(-,R(-))
  \,.
\]

This means that for all [[objects]] $c \in \mathcal{C}$ and $d \in \mathcal{D}$ there is a [[bijection]] of [[hom-sets]]

$$
  \array{
    Hom_{\mathcal{D}}(L(c),d) 
      &\overset{\simeq}{\longrightarrow}& 
    Hom_{\mathcal{C}}(c,R(d))
    \\
    ( L(c) \overset{f}{\to} d )
    &\mapsto&
    (c \overset{\widetilde f}{\to} R(d))
  }
$$

which is [[natural bijection|natural]] in $c$ and $d$.  This isomorphism is the **adjunction isomorphism** and the [[image]] $\widetilde f$ of amorphism $f$ under this bijections is called the _[[adjunct]]_ of $f$. Conversely, $f$ is called the adjunct of $\widetilde f$.

Naturality here means that for every [[morphism]] $g \colon c_2 \to c_1$ in $\mathcal{C}$ and for every [[morphisms]] $h\colon d_1\to d_2$ in $\mathcal{D}$, the resulting square

\[
  \label{NaturalitySquareForAdjointnessOfFunctors}
  \array{
    Hom_{\mathcal{D}}(L(c_1), d_1) 
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c_1, R(d_1))
    \\
    {}^{\mathllap{Hom_{\mathcal{D}}(L(g), h)}}\big\downarrow
     &&
    \big\downarrow^{\mathrlap{Hom_{\mathcal{C}}(g, R(h))}}
    \\
    Hom_{\mathcal{D}}(L(c_2),d_2)
    &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c_2,R(d_2))
  }
\]

[[commuting square|commutes]] (see also at _[[hom-functor]]_ for the definition of the vertical maps here). 

Explicitly, this commutativity, in turn, means that for every morphism $f \;\colon\; L(c_1) \to d_1$ with [[adjunct]] $\widetilde f \;\colon\; c_1 \to R(d_1)$, the adjunct of the [[composition]] is

$$
  \widetilde{
  \array{
    L(c_1) &\overset{f}{\longrightarrow}& d_1
    \\
    {}^{\mathllap{L(g)}}\big\uparrow && \big\downarrow^{\mathrlap{h}}
    \\
    L(c_2) && d_2
  }
  }
  \;\;\;=\;\;\;
  \array{
    c_1 &\overset{\widetilde f}{\longrightarrow}& R(d_1)
    \\
    {}^{\mathllap{g}}\big\uparrow && \big\downarrow^{\mathrlap{R(h)}}
    \\
    c_2 && R(d_2)
  }
$$

=--

(...)
