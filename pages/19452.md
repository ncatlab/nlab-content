
This page is going to be one chapter in _[[geometry of physics]]_.

> under construction

$\,$

$\,$


We give here an introduction to the basic concepts and results of _[[category theory]]_ and of _[[topos theory]]_, aimed at providing background for the [[synthetic differential geometry|synthetic]] and [[higher differential geometry|higher]] [[geometry of physics -- supergeometry|supergeometry]] of relevance in formulations of fundamental [[physics]] (such as used in the chapters _[[geometry of physics -- A first idea of quantum field theory|on quantum field theory]]_ and _[[geometry of physics -- fundamental super p-branes|on fundamental super p-branes]]_).

One motivation for [[category theory]] and [[topos theory]] is _a posteriori_: As a matter of experience, there is just no other toolbox that allows one to really understand and handle the [[higher differential geometry|higher]] [[supergeometry]] of relevance in [[physics]].

We offer also an _a priori_ motivation: _Category theory is the theory of duality._

<div style="float:right;margin:0 10px 10px 0;"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/74/Cup_or_faces_paradox.svg/450px-Cup_or_faces_paradox.svg.png" width="200"></div>

_[[duality|Duality]]_ is of course an ancient notion in [[philosophy]]. At least as a term, it makes a curious re-appearance in the conjectural [[theory (physics)|theory]] of fundamental [[physics]] formerly known as _[[string theory]]_. In both cases, the literature left some room in delineating what precisely is meant. But the philosophically inclined mathematician could notice (see [Lambek 82](adjoint+functor#Lambek82)) that an excellent candidate to make precise the idea of _[[duality]]_ is the mathematical concept of _[[adjoint functor|adjunction]]_, from [[category theory]].

Historically, [[category theory]] was introduced in order to make precise the concept of _[[natural transformation]]_: The concept of _[[functors]]_ was introduced just so as to support that of natural transformations, and the concept of _[[categories]]_ only served that of functors (see e.g. [Freyd 65, Part II](category+theory#Freyd65)). But natural transformations are what allows us to define, in turn, the concept of _[[adjoint functors]]_, also called _[[adjunctions]]_ on categories. All the deep concepts of category theory (such as _[[representable functors]]_, _[[Yoneda embedding]]_, _[[Kan extensions]]_, hence _[[limits]]_ and _[[colimits]]_, to be introduced below) are special cases of [[adjoint functor]] constructions -- hence of dualities, if we follow [Lambek 82](adjoint+functor#Lambek82). Therefore it makes sense to regard category theory, to a large extent, as the **theory of adjunctions**, hence the **theory of duality**:


| $\phantom{A}$ hierarchy of concepts $\phantom{A}$  | $\phantom{A}$ Definition $\phantom{A}$ |
|------------------------|------------|
| $\phantom{A}$ [[adjoint functor|adjunction]] / [[duality]] $\phantom{A}$  | $\phantom{A}$ \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets} $\phantom{A}$ |
| $\phantom{A}$ [[natural transformation]] $\phantom{A}$ | $\phantom{A}$ \ref{NaturalTransformations} $\phantom{A}$ |
| $\phantom{A}$ [[functor]] $\phantom{A}$ | $\phantom{A}$ \ref{Functors} $\phantom{A}$ |
| $\phantom{A}$ [[category]] $\phantom{A}$ | $\phantom{A}$ \ref{Categories} $\phantom{A}$ |



The pivotal role of [[adjunctions]] in [[category theory]] ([Lawvere 08](adjoint+functor#fn:1)) and in the [[foundations of mathematics]] ([[Adjointness in Foundations|Lawvere 69]], [[Cohesive Toposes and Cantor's lauter Einsen|Lawvere 94]] ) was particularly amplified by [[F. W. Lawvere]].
Moreover, [[Lawvere]] saw the future of category theory
([[Some Thoughts on the Future of Category Theory|Lawvere 91]]) as concerned with [[adjunctions]] expressing systems of archetypical dualities that reveal foundations for [[geometry]] ([Lawvere 07](cohesive+topos#LawvereAxiomatic)) and [[physics]] ([[Toposes of laws of motion|Lawvere 97]]).
He suggested ([Lawvere 94](objective+and+subjective+logic#Lawvere94)) this as a precise formulation of core aspects of the _theory of everything_
of early 19th century [[philosophy]]: [[Hegel]]'s _[[Science of Logic]]_.

These days, of course, _[[theories of everything]]_, such as [[string theory]], are understood less ambitiously than Hegel's ontological process,
as mathematical formulations of fundamental theories of physics, that could conceptually unify the hodge-podge of currently available "standard models" [[standard model of particle physics|of particle physics]] and [[standard model of cosmology|of cosmology]] to a more coherent whole.

The idea of _[[duality in string theory]]_ refers to different perspectives on physics that appear dual to each other while being _equivalent_.
But one of the basic results of category theory, which we will discuss below, is that equivalence is indeed a special case of adjunction. This allows to explore the possibility that there is more than a coincidence of terms.

Of course the usage of the term _[[duality in string theory]]_ is too loose for one to expect to be able to refine each occurrence of the term in the literature to a mathematical adjunction. However, we will see mathematical formalizations of core aspects of
key string-theoretic dualities, such as _[[topological T-duality]]_ and the _[[duality between M-theory and type IIA string theory]]_, in terms of adjunctions. Indeed, at the heart of these _[[dualities in string theory]]_ is the phenomenon of _[[double dimensional reduction]]_, which turns out to be formalized by one of the most fundamental adjunctions in ([[higher category theory|higher]] [[category theory]] ([[base change]] along the point inclusion into a [[classifying space]]).
This suggests that there may be a deeper relation here between the superficially alien uses of the word "duality", that is worth exploring.

In this respect it is worth noticing that core structure of string/M-theory arises via universal constructions from the [[superpoint]] (as explained in the chapter _[[geometry of physics -- fundamental super p-branes|on fundamental super p-branes]]_), while the superpoint itself arises, in a sense made precise by [[category theory]], "from nothing", by a system of twelve [[adjunctions]] (explained in the chapter [[geometry of physics -- supergeometry|on supergeometry]]). 

Here we introduce the requisites for understanding these statements.

#Contents#
* table of contents
{:toc}


## Categories and Functors

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

The archetypical example of a [[category]] is the [[category of sets]]:

+-- {: .num_example #CategoryOfAllSets}
###### Example
**([[Set|category of all sets]])**

The [[class]] of all [[sets]] with [[functions]] between them is a [[category]] (Def. \ref{Categories}), to be denoted _[[Set]]_:

* $Obj_{Set} = \text{class of all sets}$;

* $Hom_{Set}(X,Y) = \text{set of functions from set X to set Y}$;

* $id_X \in Hom_{Set}(X,X) = $ [[identity function]] on set $X$;

* $\circ_{X_1,X_2,X_3} = \text{ordinary composition of functions}$. 

=--

More generally all kind of _sets with [[structure]]_, in the sense going back to [[Bourbaki]], form categories, where the [[morphisms]] are the _[[homomorphisms]]_ (whence the name "morphism"!). These are called _[[concrete categories]]_ (we characterize them precisely in Example \ref{StructuredSetsAndFaithfulFunctors}, further below): 

+-- {: .num_example #ExamplesOfConcreteCategories}
###### Example
**(basic examples of [[concrete categories]])**

For $\mathcal{S}$ a kind of [[mathematical structure]], there is the [[category]] (Def. \ref{Categories}) $\mathcal{S}Set$ whose [[objects]] are the corresponding [[structured sets]], and whose [[morphisms]] are the corresponding structure [[homomorphisms]], hence the [[functions]] of underlying sets which respect the given structure.

Basic examples of [[concrete categories]] include the following:

| $\phantom{A}$[[concrete category]]$\phantom{A}$ | $\phantom{A}$[[objects]]$\phantom{A}$ | $\phantom{A}$[[morphisms]]$\phantom{A}$ |
|-----------------------|-------------|---------------|
| $\phantom{A}$[[Grp]]   | $\phantom{A}$[[groups]]$\phantom{A}$ | $\phantom{A}$[[group homomorphisms]]$\phantom{A}$ |
| $\phantom{A}$[[Vect]]  | $\phantom{A}$[[vector spaces]]$\phantom{A}$ | $\phantom{A}$[[linear maps]]$\phantom{A}$ |
| $\phantom{A}$[[Alg]]   | $\phantom{A}$[[algebras]]$\phantom{A}$ | $\phantom{A}$[[algebra homomorphism]]$\phantom{A}$ |
| $\phantom{A}$[[Top]]  | $\phantom{A}$[[topological spaces]]$\phantom{A}$ |  $\phantom{A}$[[continuous functions]]$\phantom{A}$ |
| $\phantom{A}$[[Mfd]]${}_{k}$  | $\phantom{A}$[[differentiable manifolds]]$\phantom{A}$ | $\phantom{A}$[[differentiable functions]]$\phantom{A}$ |

=--

This is the motivation for the terminology "categories", as the examples in Example \ref{ExamplesOfConcreteCategories} are literally _categories of mathematical structures_. But not all categories are "[[concrete category|concrete]]" in this way.

There is a range of constructions that provide new categories from given ones:

+-- {: .num_example #OppositeCategory}
###### Example
**([[opposite category]])**

Let $\mathcal{C}$ be a [[category]]. Then its _[[opposite category]]_ $\mathcal{C}^{op}$ has the same [[objects]] as $\mathcal{C}$, but the direction of the [[morphisms]] is reversed. Accordingly, [[composition]] in the [[opposite category]] $\mathcal{C}^{op}$ is that in $\mathcal{C}$, but with the order of the arguments reversed:

* $Obj_{\mathcal{C}^{op}} \;\coloneqq\; Obj_{\mathcal{C}}$;

* $Hom_{\mathcal{C}^{op}}(X,y) \;\coloneqq\; Hom_{\mathcal{C}}(Y,X)$.

=--


+-- {: .num_example #ProductCategory}
###### Example
**([[product category]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be two [[categories]] (Def. \ref{Categories}). Then their _[[product category]]_ $\mathcal{C} \times \mathcal{D}$ has as [[objects]] [[pairs]] $(c,d)$ with $c \in Obj_{\mathcal{C}}$ and $d \in Obj_{\mathcal{D}}$, and as morphisms [[pairs]]  $ (c_1 \overset{f}{\to} c_2) \in Hom_{\mathcal{C}}(c_1,c_2)$, $ (d_1 \overset{g}{\to} d_2) \in Hom_{\mathcal{D}}(d_1,d_2)$, and [[composition]] is defined by composition in each entry:

* $Obj_{\mathcal{C} \times \mathcal{D}} \coloneqq Obj_{\mathcal{C}} \times Obj_{\mathcal{D}}$;

* $Hom_{\mathcal{C} \times \mathcal{D}}( (c_1,d_1), (c_2,d_2) ) \coloneqq  Hom_{\mathcal{C}}(c_1,c_2) \times Hom_{\mathcal{D}}( d_1, d_2 )$

* $(f_2, g_2) \circ (f_1, g_1) \;\coloneqq\; ( f_2 \circ f_1, g_2 \circ g_1 )$

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


+-- {: .num_example #HomFunctor}
###### Example
**([[hom-functor]])**

Let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}). Then its _[[hom-functor]]_ 

$$
  Hom_{\mathcal{C}}
  \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  Set
$$

is the [[functor]] (Def. \ref{Functors}) out of the [[product category]] (Def. \ref{ProductCategory}) of $\mathcal{C}$ with its [[opposite category]] to the [[category of sets]], which sends a [[pair]] $X,Y \in \mathcal{C}$ of [[objects]] to the [[hom-set]] $Hom_{\mathcal{C}}(X,Y)$ between them, and which sends a [[pair]] of [[morphisms]], with one of them into $X$ and the outher out of $Y$, to the operation of [[composition]] with these morphisms:

$$
  Hom_{\mathcal{C}}
  \;\;\colon\;\;\;
  \array{
    X_1 & Y_1 
    \\
    {}^{\mathllap{g}}\big\uparrow & \big\downarrow^{\mathrlap{h}}
    \\
    X_2 & Y_2
  }
  \;\;\mapsto\;\;
  \array{
    Hom_{\mathcal{C}}(X_1, Y_1)
    \\
    \big\downarrow^{ \mathrlap{ f \mapsto h \circ f \circ g  } }
    \\
    Hom_{\mathcal{C}}(X_2, Y_2)
  }
$$


=--

+-- {: .num_defn #FullyFaithfulFunctor}
###### Definition
**(Terminology: [[full functor|full]], [[faithful functor|faithful]] and [[fully faithful functors]])**

A [[functor]] $F \;\colon\; \mathcal{C} \to \mathcal{D}$ (Def. \ref{Functors}) is called


* a _[[full functor]]_ if all its hom-functions are [[surjective functions]] 

  $$
    Hom_{\mathcal{C}}(X,Y) 
      \underoverset{surj}{F_{X,Y}}{\longrightarrow} 
    Hom_{\mathcal{D}}(F(X), F(Y))
  $$

* a _[[faithful functor]]_ if all its hom-functions are [[injective functions]] 

  $$
    Hom_{\mathcal{C}}(X,Y) 
      \underoverset{inj}{F_{X,Y}}{\longrightarrow} 
    Hom_{\mathcal{D}}(F(X), F(Y))
  $$

* a _[[fully faithful functor]]_ if all its hom-functions are [[bijective functions]] 

  $$
    Hom_{\mathcal{C}}(X,Y) 
      \underoverset{bij}{F_{X,Y}}{\longrightarrow} 
    Hom_{\mathcal{D}}(F(X), F(Y))
  $$

A [[fully faithful functor]] is also called a _[[full subcategory]]-inclusion_. We will denote this situation by

$$
  \mathcal{C} \overset{\phantom{A}F\phantom{A}}{\hookrightarrow} \mathcal{D}
  \,.
$$

=--

This allows to make precise the idea of _[[concrete category]]_ from Example \ref{ExamplesOfConcreteCategories}:

+-- {: .num_example #StructuredSetsAndFaithfulFunctors}
###### Example
**([[structured sets]] and [[faithful functors]])**

Let $\mathcal{S}$ be a kind of [[mathematical structure]] and let $\mathcal{S} Set$ be the [[category]] of $\mathcal{S}$-[[structured sets]]. Then there is the  [[forgetful functor]]

$$
  \mathcal{S}Set \longrightarrow Set
$$

which sends each [[structured set]] to the underlying set ("forgetting" the [[structure]] that it carries), and which sends [[functions]] of sets to themselves. That a [[homomorphism]] of [[structured sets]] is a [[function]] between the underlying sets satisfying a _special condition_ implies that this is a _[[faithful functor]]_ (Def. \ref{FullyFaithfulFunctor}).

Conversely, it makes sense to _define_ [[structured sets]] in general to be the [[objects]] of a [[category]] $\mathcal{C}$ which is equipped with a [[faithful functor]] $\mathcal{C} \overset{faithful}{\longrightarrow} Set$ to the [[category of sets]]. See at _[[structure]]_ for more on this.

=--



+-- {: .num_example #SpacesViaAlgebrasOfFunctions}
###### Example
**([[spaces]] seen via their [[algebras of functions]])**

Consider 

1. the [[category]] [[Top]]${}_{cpt}$ of [[compact topological space|compact]] [[topological spaces]] with [[continuous functions]] between them;

1. the category [[C*Alg]] of [[C*-algebras]] over the [[complex numbers]]

from Example \ref{ExamplesOfConcreteCategories}.

Then there is a [[functor]] (Def. \ref{Functors})

$$
  C(-)
  \;\colon\;
  Top_{cpt}
   \longrightarrow
  C^\ast Alg^{op}
$$

from the former to the [[opposite category]] of the latter (Example \ref{OppositeCategory}) which sends any [[compact topological space|compact]] [[topological space]] $X$ to its [[C*-algebra]] $C(X)$ of [[continuous functions]] $X \overset{\phi}{\to} \mathbb{C}$ to the [[complex numbers]], and which sends every [[continuous function]] between compact spaces to the [[C*-algebra]]-[[homomorphism]] that is given by [[precomposition]]:

$$
  C(-)
  \;\;\;\colon\;\;\;
  \array{
    X &\mapsto & C(X) 
    \\
    {}^{\mathllap{ f }}\big\downarrow 
      && 
    \big\uparrow^{\mathrlap{ f^\ast : \phi \mapsto \phi \circ f }}
    \\
    Y &\mapsto& C(Y) 
  }
$$

Part of the statement of _[[Gelfand duality]]_ is that this is a [[fully faithful functor]], hence exhibiting a  [[full subcategory]]-inclusion (Def. \ref{FullyFaithfulFunctor}):

$$
  Top_{cpt}
   \hookrightarrow
  C*Alg^{op}
  \,.
$$

Similarly, consider

1. the [[category]] [[SmthMfd]]$ of [[smooth manifolds]] with [[smooth functions]] between them;

1. the category [[Alg]]${}_{\mathbb{R}}$ of [[associative algebras]] over the [[real numbers]]

from Example \ref{ExamplesOfConcreteCategories}.

Then there is a [[functor]] (Def. \ref{Functors})

$$
  C^\infty(-)
  \;\colon\;
  SmthMfd^{op}
    \longrightarrow
  Alg_{\mathbb{R}}^{op}
$$

from the former to the [[opposite category]] of the latter (Def. \ref{OppositeCategory}), which sends any [[smooth manifold]] $X$ to its [[associative algebra]] $C^\inft(X)$ of [[continuous functions]] $X \overset{\phi}{\to} \mathbb{R}$ to the [[real numbers]], and which sends every [[smooth function]] between smooth manifolds to the [[algebra homomorphism]] that is given by [[precomposition]]:


$$
  C^\infty(-)
  \;\;\;\colon\;\;\;
  \array{
    X &\mapsto & C^\infty(X) 
    \\
    {}^{\mathllap{ f }}\big\downarrow 
      && 
    \big\uparrow^{\mathrlap{ f^\ast : \phi \mapsto \phi \circ f }}
    \\
    Y &\mapsto& C^\infty(Y) 
  }
$$

The statement of _[[Milnor's exercise]]_ is that this  this is a [[fully faithful functor]], hence exhibiting a  [[full subcategory]]-inclusion (Def. \ref{FullyFaithfulFunctor}):

$$
  SmthMfd
   \hookrightarrow
  Alg_{\mathbb{R}}^{op}
  \,.
$$

These two statements, expressing categories of [[spaces]] as [[full subcategories]] of [[opposite categories]] of categories of [[algebras]], are the starting point for many developments in [[geometry]], such as _[[algebraic geometry]]_, _[[supergeometry]]_, _[[noncommutative geometry]]_ and _[[noncommutative topology]]_.

=--




## Natural transformations and Presheaves




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

  \[
    \label{NaturalTransformationComponent}
    F(X) \overset{ \eta_X }{\longrightarrow} G(X)
  \]

such that

* for each [[morphism]] $X \overset{f}{\longrightarrow} Y$ we have

  \[
    \label{Naturality}
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
  \]

For 

$$
  \mathcal{C}
    \underoverset
      {\underset{G}{\longrightarrow}}
      {\overset{F}{\longrightarrow}}
      {\phantom{AA}\Downarrow \mathrlap{\eta} \phantom{AA}}
  \mathcal{D}
  \phantom{AA}
  \text{and}
  \phantom{AA}
  \mathcal{C}
    \underoverset
      {\underset{H}{\longrightarrow}}
      {\overset{G}{\longrightarrow}}
      {\phantom{AA}\Downarrow \mathrlap{\rho} \phantom{AA}}
  \mathcal{D}
$$

two natural transformations as shown, their _composition_ is the natural transformation

$$
  \mathcal{C}
    \underoverset
      {\underset{H}{\longrightarrow}}
      {\overset{F}{\longrightarrow}}
      {\phantom{A}\Downarrow \mathrlap{\rho \circ \eta} \phantom{AAAA}}
  \mathcal{D}
$$

whose components (eq:NaturalTransformationComponent) are the [[compositions]] of the components of $\eta$ and $\rho$:

\[
  \label{NaturalTransformationComposition}
  (\rho \circ \eta)_X
  \;\coloneqq\;
  \rho_{X} \circ \eta_X
\]

=--


+-- {: .num_example #FunctorCategory}
###### Example
**([[functor category]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be [[categories]] (Def. \ref{Categories}). Then the _[[category of functors]]_ between them, to be denoted $[\mathcal{C}, \mathcal{D}]$, is the [[category]] whose [[objects]] are the [[functors]] $\mathcal{C} \overset{F}{\to} \mathcal{D}$ (Def. \ref{Functors}) and whose [[morphisms]] are the [[natural transformations]] $F \overset{\eta}{\Rightarrow} G$ between functors (Def. \ref{NaturalTransformations}) and whose [[composition]] operation is the composition of natural transformations (eq:NaturalTransformationComposition).

=--

+-- {: .num_example #CategoryOfPresheaves}
###### Example
**([[category of presheaves]])**

Given a [[category]] $\mathcal{C}$ (Def. \ref{Categories}), a [[functor]] (Def. \ref{Functors}) of the form

$$
  F \;\colon\; \mathcal{C}^{op} \longrightarrow Set
  \,,
$$

hence out of the [[opposite category]] of $\mathcal{C}$ (Def. \ref{OppositeCategory}), into the [[category of sets]] (Example \ref{CategoryOfAllSets}) is also called a _[[presheaf]]_ (for reasons discussed below) _on $\mathcal{C}$_ or _over $\mathcal{C}$_.

The corresponding [[functor category]] (Example \ref{FunctorCategory})

$$
  PSh(\mathcal{C})
  \;\coloneqq\; [\mathcal{C}^{op}, Set]
$$

is hence called the _[[category of presheaves]]_ over $\mathcal{C}$.

Essentially by Example \ref{HomFunctor}, there is the following [[functor]] (Def. \ref{Functors}) from $\mathcal{C}$ to its [[category of presheaves]]:

\[
  \label{YonedaFunctor}
  y
  \;\;\colon\;\;
  \array{
    \mathcal{C}
      &\longrightarrow&
    [\mathcal{C}^{op}, Set]
    \\
    X
    &\mapsto&
    Hom_{\mathcal{C}}(-,X)
  } 
\]

The [[presheaves]] $y(X) \coloneqq Hom_{\mathcal{C}}(-,X)$ in the [[image]] of this functor are called the _[[representable presheaves]]_ and $X \in Obj_{\mathcal{C}}$ is called their [[representing object]].

This functor is called the _[[Yoneda embedding]]_, due to Prop. \ref{YonedaEmbedding} below.

=--

+-- {: .num_remark #PresaheavesAsGeneralizedSpaces}
###### Remark
**([[presheaves]] as generalized spaces)**

If a given [[category]] $\mathcal{C}$ (Def. \ref{Categories}) is thought of as a category of _[[spaces]]_ of sorts, as those in Example \ref{SpacesViaAlgebrasOfFunctions}, then it will be most useful to think of the corresponding [[category of presheaves]] $[\mathcal{C}^{op}, Set]$ (Def. \ref{CategoryOfPresheaves}) as a category of _generalized spaces probe-able by_ the test spaces in $\mathcal{C}$.

Namely, imagine a generalized space $\mathbf{X}$ which is at least probe-able by spaces in $\mathcal{C}$. This should mean that for each [[object]] $c \in \mathcal{C}$ there is some [[set]] of geometric maps "$c \to \mathcal{X}$". Here the quotation marks are to warn us that, at this point, $\mathbf{X}$ is not defined yet, and even if it were, it is not expected to be an object of $\mathcal{C}$, so that, at this point, an actual morphism from $c$ to $\mathbf{X}$ is not defined. But we may anyway consider some set


\[
  \label{WouldBeMapsIntoGeneralizedSpace}
  \mathbf{X}(c)  \; \text{"=}  Hom(c,\mathbf{X})" 
\]

whose elements we do want to think of maps (homomorphisms of spaces) from $c$ to $X$. 

That this is indeed correct, in that we may remove the quotation remarks on the right, is the statement of the _[[Yoneda lemma]]_, which we discuss as Prop. \ref{YonedaLemma} below.


A minimum consistency condition for this to make sense (we will consider further conditions later on when we discuss _[[sheaves]]_) is that we may consistently pre-compose the would-be maps from $c$ to $\mathbf{X}$ with actual morphisms $d \overset{f}{\to} c$ in $\mathcal{C}$. This means that for every such morphism there should be a function between these sets of would-be maps

$$
  \array{
     c && \mathbf{X}(d)
     \\
     {}^{\mathllap{ f }}\big\downarrow 
       && 
     \big\uparrow{}^{\mathrlap{ \mathbf{X}(f) \, \text{"=}(-)\circ f"}}
     \\
     d && \mathbf{X}(c)
  }
$$

which respects composition and identity morphisms. But in summary, this says that what we have defined thereby is actually a _[[presheaf]]_ on $\mathcal{C}$ (Def. \ref{CategoryOfPresheaves}), namely a functor

$$
  \mathbf{X} \;\colon\; \mathcal{C}^{op} \longrightarrow Set
  \,.
$$

For this to make sense, it ought to be true that every "ordinary space", hence every [[object]] $X \in \mathcal{C}$ is also an example of a "generalized space probe-able by" object of $\mathcal{C}$, since, after all, these are the space which may manifestly be probed by objects $c \in \mathcal{C}$, in that morphisms $c \to X$ are already defined.

Hence the incarnation of $X \in \mathcal{C}$ as a generalized space probe-able by objects of $\mathcal{C}$ should be the presheaf $Hom_{\mathcal{C}}(-,X)$, hence the [[representable presheaf|presheaf represented]] by $X$, via the Yoneda functor (eq:YonedaFunctor).

At this point, however, a serious consistency condition arises: The "ordinary spaces" now exist as objects of two different categories, on the one hand there is the original $X \in \mathcal{C}$, on the other hand there is its Yoneda image $y(X) \in [\mathcal{C}^{op}, Set]$ in the category of generalized spaces, and we need to know that these two perspectives are compatible, notably that maps $X \to Y$ between ordinary spaces are the same whether viewed in $\mathcal{C}$ or in the more general context of $[\mathcal{C}^{op}, Set]$. 

That this, too, holds true, is the statement of the _[[Yoneda embedding]]_, which we discuss as Prop. \ref{YonedaEmbedding} below.

=--

+-- {: .num_prop #YonedaLemma}
###### Proposition
**([[Yoneda lemma]])**

Let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}), $X \in \mathcal{C}$ any object, and $\mathbf{Y} \in [\mathcal{C}^{op}, Set]$ a [[presheaf]] over $\mathcal{C}$ (Def. \ref{CategoryOfPresheaves}).

Then there is a [[bijection]]

$$
  \array{
    Hom_{[\mathcal{C}^{op},Set]}( y(X), \mathbf(Y) )
      &\overset{\simeq}{\longrightarrow}&
    \mathbf{Y}(X)
    \\
    \eta 
      &\mapsto&
    \eta_X(id_X)
  }
$$

between the [[hom-set]] of the [[category of presheaves]] from the [[representable presheaf|presheaf represented]] by $X$ (eq:YonedaFunctor) to $\mathbf{Y}$, and the set which is assigned by $\mathbf{Y}$ to $X$.

=--

+-- {: .proof}
###### Proof

By Example \ref{FunctorCategory}, an element in the set on the left is a [[natural transformation]] (Def. \ref{NaturalTransformations}) of the form

$$
  \mathcal{C}^{op}
    \underoverset
      {\underset{\mathbf{Y}}{\longrightarrow}}
      {\overset{y(X)}{\longrightarrow}}
      {\phantom{AA} \Downarrow \mathrlap{\eta}  \phantom{AA}}
  Set
$$

hence given by component functions (eq:NaturalTransformationComponent)

$$
  Hom_{\mathcal{C}}(c,X)
    \overset{\eta_c}{\longrightarrow}
  \mathbf{Y}(X)
$$

for each $c \in \mathcal{C}$. In particular there is the component at $c = X$
  
$$
  \array{
    Hom_{\mathcal{C}}(X,X)
      &\overset{\eta_X}{\longrightarrow}&
    \mathbf{Y}(X)
    \\
    id_X &\mapsto& \eta_X(id_X)
  }
$$

and the [[identity morphism]] $id_X$ on $X$ is a canonical element in the set on the left. The statement to be proven is hence equivalently that for every element in $\mathbf{Y}(X)$ there is precisely one $\eta$ such that this element equals $\eta_X(id_X)$.

Now the condition to be satisfied by $\eta$ is that it makes its [[naturality squares]] (eq:Naturality) commute. This includes those of the form

$$
  \array{
    id_X 
    \in
    & 
    Hom_{\mathcal{C}}(X,X)
      &\overset{\eta_X}{\longrightarrow}&
    \mathbf{Y}(X)
    \\ 
    & 
    {}^{\mathllap{ Hom_{\mathcal{C}}(f,X) }}
    \big\downarrow 
      && 
    \big\downarrow{}^{\mathrlap{\mathbf{Y}(f)}}
    \\
    & 
    Hom_{\mathcal{C}}(Y,X)
    &\underset{\eta_Y}{\longrightarrow}&
    \mathbf{Y}(Y)
  }
  \phantom{AAAA}
  \array{
     \{id_X\}
     &\longrightarrow&
     \{\eta_X(id_X)\}
     \\
     \big\downarrow 
     &&
     \big\downarrow
     \\
     \{f\}
     &\longrightarrow&
     \big\{ \eta_Y(F) = \mathbf{Y}(f)( \eta_X(id_X) ) \big\}
  }
$$

for any [[morphism]] 

$$
  (Y \overset{f}{\longrightarrow} X)
    \;\in\;
  Hom_{\mathcal{C}}(Y,X)
  \,.
$$

As the diagram chase of elements on the right shows, this commutativity fixes $\eta_Y(f)$ for all $Y \in \mathcal{C}$ and all $f \in Hom_{\mathcal{C}}(Y,X)$ uniquely in terms of the element $\eta_{X}(id_X)$.

It remains only to see that there is no condition on the element $\eta_X(id_X)$, hence that with $\eta_Y(f)$ defined this way, the commutativity of all the remaining naturality squares is implies: The general naturality square for a morphism $Y_2 \overset{g}{\longrightarrow} Y_1$ is of the form

$$
  \array{
    & 
    Hom_{\mathcal{C}}(Y_1,X)
      &\overset{\eta_{Y_1}}{\longrightarrow}&
    \mathbf{Y}(Y_1)
    \\ 
    & 
    {}^{\mathllap{ Hom_{\mathcal{C}}(g,X) }}
    \big\downarrow 
      && 
    \big\downarrow{}^{\mathrlap{\mathbf{Y}(g)}}
    \\
    & 
    Hom_{\mathcal{C}}(Y_2,X)
    &\underset{\eta_{Y_2}}{\longrightarrow}&
    \mathbf{Y}(Y_2)
  }
  \phantom{AAAA}
  \array{
     \{f_1\}
     &\longrightarrow&
     \{ \mathbf{Y}(f_1)( \eta_X(id_X) )  \}
     \\
     \big\downarrow 
     &&
     \big\downarrow
     \\
     \{f_2 = f_1\circ g\}
     &\longrightarrow&
     \{\mathbf{Y}(f_2)( \eta_X(id_X) ) = \mathbf{Y}(g) \circ \mathbf{Y}(f_1) ( \eta_X(id_X) ) \}
  }
$$

As shown on the right, the commutativity of this diagram now follows from the [[functor|functoriality]] $\mathbf{Y}(f_2) = \mathbf{Y}(f_1 \circ g)$ of the [[presheaf]] $\mathbf{Y}$.

=--

spring

As a direct corollary, we obtain the statement of the [[Yoneda embedding]]:

+-- {: .num_prop #YonedaEmbedding}
###### Proposition
**([[Yoneda embedding]])**

The assignment of [[representable presheaves|represented presheaves]] (eq:YonedaFunctor) is a [[fully faithful functor]] (Def. \ref{FullyFaithfulFunctor}), hence exhibits a [[full subcategory]] inclusion

$$
  y
  \;\;\colon\;\;
  \array{
    \mathcal{C}
      &\overset{\phantom{AAAA}}{\hookrightarrow}&
    [\mathcal{C}^{op}, Set]
    \\
    X
    &\mapsto&
    Hom_{\mathcal{C}}(-,X)
  } 
$$

of the given [[category]] $\mathcal{C}$ into its [[category of presheaves]].

=--

+-- {: .proof}
###### Proof

We need to show that for all $X_1, X_2 \in Obj_{\mathcal{C}}$ the function

\[
  \label{HomFunctionForYonedaEmbedding}
  \array{
    Hom_{\mathcal{C}}(X_1, X_2)
      &\overset{ }{\longrightarrow}&
    Hom_{[\mathcal{C}^{op}, Set]}
    \big(
      Hom_{\mathcal{C}}(-,X_1)
       \;,\;
      Hom_{\mathcal{C}}(-,X_2)
    \big)
    \\
    f 
      &\mapsto&  
    Hom_{\mathcal{C}}(-,f)
  }
\]

is a [[bijection]]. But the [[Yoneda lemma]] (Prop. \ref{YonedaLemma}) states a bijection the other way around

$$
  \array{
    Hom_{[\mathcal{C}^{op}, Set]}
    \big(
      Hom_{\mathcal{C}}(-,X_1)
       \;,\;
      Hom_{\mathcal{C}}(-,X_2)
    \big)
      &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(-,X_2)(X_1)
      &=&
    Hom_{\mathcal{C}}(X_1, X_2)
    \\
    \eta && \mapsto && \eta_{X_1}( id_{X_1} ) 
    \\
    Hom_{\mathcal{C}}(-,f) 
      && \mapsto && 
    Hom_{\mathcal{C}}(X_1,f)(id_{X_1}) = f
   }
$$

and hence it is sufficient to see that this is a [[left inverse]] to (eq:HomFunctionForYonedaEmbedding). This follows by inspection, as shown in the third line above.


=--



## Adjunction and duality


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
