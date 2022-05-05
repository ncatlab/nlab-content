
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


## Basic category theory

### Categories and Functors

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

Some terminology

+-- {: .num_defn #SmallCategory}
###### Definition
**([[small category]])**

If a [[category]] $\mathcal{C}$ (Def. \ref{Categories}) happens to have as [[class]] $Obj_{\mathcal{C}}$ of [[objects]] an actual [[set]] (i.e. a [[small set]] instead of a [[proper class]]), then $\mathcal{C}$ is called a _[[small category]]_.

=--


+-- {: .num_defn #Isomorphism}
###### Definition
**([[isomorphism]])**

For $\mathcal{C}$ a [[category]] (Def. \ref{Categories}), a [[morphism]] 

$$
  X \overset{f}{\to} Y \;\;\in Hom_{\mathcal{C}}(X,Y)
$$ 

is called an _[[isomorphism]]_ if there exists an [[inverse morphism]]

$$
  Y \overset{f^{-1}}{\longrightarrow} Y \;\; \in Hom_{\mathcal{C}}(Y,X)
$$

namely a morphism such that the [[compositions]] with $f$ are equal to the [[identity morphisms]] on $X$ and $Y$, respectively

$$
  f^{-1} \circ f  \;=\; id_X
  \phantom{AAA}
  f \circ f^{-1} \;=\; id_Y
$$

=--

+-- {: .num_defn #Groupoid}
###### Definition
**([[groupoid]])**

If $\mathcal{C}$ is a [[category]] in which _every_ [[morphism]] is an [[isomorphism]] (Def. \ref{Isomorphism}), then $\mathcal{C}$ is called a _[[groupoid]]_.

=--

+-- {: .num_example #DeloopingGroupoid}
###### Example
**([[delooping]] [[groupoid]])**

For $G$ a [[group]], there is a [[groupoid]] (Def. \ref{Groupoid}) $\mathbf{B}G$ with a single [[object]], whose single [[hom-set]] is $G$, with [[identity morphism]] the [[neutral element]] and [[composition]] the group operation in $G$:

* $Obj_{\mathbf{B}G} = \ast$

* $Hom_{\mathcal{C}}(\ast,\ast) \;=\; G$

In fact every [[groupoid]] with precisely one object is of the form.

=--

+-- {: .num_remark }
###### Remark
**([[groupoids]] and [[homotopy theory]])**

Even though [[groupoids]] (Def. \ref{Groupoid}) are special cases of [[categories]] (Def. \ref{Categories}), the theory of groupoids in itself has a rather different flavour than that of category theory: Part of the [[homotopy hypothesis]]-theorem is that the theory of groupoids is really _[[homotopy theory]]_ for the special case of [[homotopy 1-types]].

(In applications in [[homotopy theory]], groupoids are considered mostly in the case that the [[class]] $Obj_{\mathcal{C}}$ of [[objects]] is in fact a [[set]]: _[[small groupoids]]_, Def. \ref{SmallCategory}). 

For this reason we will not have more to say about [[groupoids]] here, and instead relegate their discussion to the chapter [[geometry of physics -- homotopy types|on homotopy theory]].


=--


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




### Natural transformations




+-- {: .num_defn #NaturalTransformations}
###### Definition
**([[natural transformation]] and [[natural isomorphism]])**

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

If all the component morphisms $\eta_X$ are [[isomorphisms]] (Def. \ref{Isomorphism}), then the natural transformation $\eta$ is called a _[[natural isomorphism]]_.

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



### Adjunctions


+-- {: .num_defn #AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}
###### Definition
**([[adjoint functors]])**

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

if there exists a [[natural isomorphism]] (Def. \ref{NaturalTransformations}) between the [[hom-functors]] (Example \ref{HomFunctor}) of the following form:

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

which is [[natural bijection|natural]] in $c$ and $d$.  This isomorphism is called the _adjunction hom-isomorphism_ and the [[image]] $\widetilde f$ of amorphism $f$ under this bijections is called the _[[adjunct]]_ of $f$. Conversely, $f$ is called the _[[adjunct]]_ of $\widetilde f$.

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

+-- {: .num_defn #AdjunctionUnitFromHomIsomorphism}
###### Definition
**([[adjunction unit]] and [[adjunction counit|counit]] in terms of hom-isomorphism)

Given a pair of [[adjoint functors]] 

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{\bot}
  \mathcal{D}
$$

according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}, one says that 

1. for any $c \in \mathcal{C}$ the [[adjunct]] of the [[identity morphism]] on  $L(c)$ is the _[[unit of an adjunction|unit morphism]]_ of the adjunction at that object, denoted

   $$
     \eta_c \coloneqq \widetilde{id_{L(c)}} \;\colon\; c \longrightarrow R(L(c))
   $$

1. for any $d \in \mathcal{D}$ the [[adjunct]] of the [[identity morphism]] on  $R(d)$ is the _[[counit of an adjunction|counit morphism]]_ of the adjunction at that object, denoted

   $$
     \epsilon_d \;\colon\; L(R(d)) \longrightarrow d
   $$



=--

+-- {: .num_prop #GeneralAdjunctsInTermsOfAdjunctionUnitCounit}
###### Proposition
**(general [[adjuncts]] in terms of [[adjunction unit|unit/counit]])**

Consider a pair of [[adjoint functors]] 

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{\bot}
  \mathcal{D}
$$

according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}, with [[adjunction units]] $\eta_c$ and [[adjunction counits]] $\epsilon_d$ according to Def. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}.

Then

1. The [[adjunct]] $\widetilde f$ of any morphism $L(c) \overset{f}{\to} d$ is obtained from $R$ and $\eta_c$ as the [[composition|composite]]

   \[
     \label{AdjunctFormula}
     \widetilde f 
     \;\colon\;
     c 
       \overset{\eta_c}{\longrightarrow} 
     R(L(c))
       \overset{R(f)}{\longrightarrow}
     R(d)
   \]

   Conversely, the [[adjunct]] $f$ of any morphism $c \overset{\widetilde f}{\longrightarrow} R(d)$ is obtained from $L$ and $\epsilon_d$ as

   \[
     \label{ConverseAdjunctFormula}
     f
     \;\colon\;
     L(c) 
       \overset{L(\widetilde f)}{\longrightarrow} 
     R(L(d))
       \overset{\epsilon_d}{\longrightarrow}
     d
   \]

1. The [[adjunction units]] $\eta_c$ and [[adjunction counits]] $\epsilon_d$ are components of [[natural transformations]] of the form

   $$
     \eta \;\colon\; Id_{\mathcal{C}} \Rightarrow R \circ L
   $$

   and

   $$
     \epsilon \;\colon\; L \circ R \Rightarrow Id_{\mathcal{D}}
   $$

1. The [[adjunction unit]] and [[adjunction counit]] satisfy the [[triangle identities]], saying that

   $$
      id_{L(c)}
      \;\colon\;
      L(c) 
        \overset{L(\eta_c)}{\longrightarrow} 
      L(R(L(c))) 
        \overset{\epsilon_{L(c)}}{\longrightarrow}
      L(c)
   $$

   and

   $$
     id_{R(d)}
     \;\colon\;
     R(d)
       \overset{\eta_{R(d)}}{\longrightarrow}
     R(L(R(d)))
       \overset{R(\epsilon_d)}{\longrightarrow}
     R(d)
   $$

=--

+-- {: .proof}
###### Proof

For the first statement, consider the [[naturality square]] (eq:NaturalitySquareForAdjointnessOfFunctors) in the form 

$$
  \array{
    id_{L(c)}
     \in 
    &
    Hom_{\mathcal{D}}(L(c), L(c)) 
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c, R(L(c)))
    \\
    &
    {}^{\mathllap{Hom_{\mathcal{D}}(L(id), f)}}\big\downarrow
     &&
    \big\downarrow^{\mathrlap{Hom_{\mathcal{C}}(id, R(f))}}
    \\
    &
    Hom_{\mathcal{D}}(L(c), d)
    &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}( c, R(d) )
  }
$$

and consider the element $id_{L(c_1)}$ in the top left entry. Its image under going down and then right in the diagram is $\widetilde f$, by Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}. On the other hand, its image under going right and then down is $ R(f)\circ \eta_{c}$, by Def. \ref{AdjunctionUnitFromHomIsomorphism}. Commutativity of the diagram means that these two morphisms agree, which is the statement to be shown, for the adjunct of $f$.

The converse formula follows analogously.

The third statement follows directly from this by applying these formulas for the [[adjuncts]] twice and using that the result must be the original morphism:

$$
  \begin{aligned}
    id_{L(c)}
    & =
    \widetilde \widetilde { id_{L(c)} }
    \\
    & = \widetilde{ c \overset{\eta_c}{\to} R(L(c))  }
    \\
    & = 
     L(c) 
       \overset{L(\eta_c)}{\longrightarrow} 
     L(R(L(c))) 
       \overset{\epsilon_{L(c)}}{\longrightarrow}
     L(c)
  \end{aligned}
$$

For the second statement, we have to show that for every moprhism $f \colon c_1 \to c_2$ the following [[commuting square|square commutes]]:

$$
  \array{    
     c_1 &\overset{f}{\longrightarrow}& c_2
     \\
     {}^{\mathllap{\eta_{c_1}}}\big\downarrow 
       && 
     \big\downarrow^{\mathrlap{\eta_{c_2}}}
     \\
     R(L(c_1))
      &\underset{ R(L(f)) }{\longrightarrow}&
     R(L(c_2))
  }
$$

To see this, consider the [[naturality square]] (eq:NaturalitySquareForAdjointnessOfFunctors) in the form 

$$
  \array{
    id_{L(c_2)}
    \in
    & Hom_{\mathcal{D}}(L(c_2), L(c_2)) 
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c_2, R(L(c_2)))
    \\
    &
    {}^{\mathllap{Hom_{\mathcal{D}}(L(f),id_{L(c_2)})}}\big\downarrow
     &&
    \big\downarrow^{\mathrlap{Hom_{\mathcal{C}}(f, R(id_{L(c_2)}))}}
    \\
    &
    Hom_{\mathcal{D}}(L(c_1),L(c_2))
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c_1,R(L(c_1)))
  }
$$

The image of the element $id_{L(c_2)}$ in the top left along the right and down is $ f \circ \eta_{c_2}$, by Def. \ref{AdjunctionUnitFromHomIsomorphism}, while its image down and then to the right is $\widetilde {L(f)} = R(L(f)) \circ \eta_{c_1}$, by the previous statement. Commutativity of the diagram means that these two morphisms agree, which is the statement to be shown.

The argument for the naturality of $\epsilon$ is directly analogous.


=--

+-- {: .num_prop #AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat}
###### Proposition
**([[adjoint functors]] equivalent to [[adjunction]] in [[Cat]])**

Two functors

$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{}
  \mathcal{C}
$$

are an [[adjoint pair]] in the sense that there is a [[natural isomorphism]] (eq:HomIsomorphismForAdjointFunctors) according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}, precisely if they participate in an _[[adjunction]]_ in the [[2-category]] [[Cat]], meaning that 

1. there exist [[natural transformations]] 

   $$
     \eta \;\colon\; Id_{\mathcal{C}} \Rightarrow R \circ L
   $$

   and

   $$
     \epsilon \;\colon\; L \circ R \Rightarrow Id_{\mathcal{D}}
   $$

2. which satisfy the [[triangle identities]]

   $$
      id_{L(c)}
      \;\colon\;
      L(c) 
        \overset{L(\eta_c)}{\longrightarrow} 
      L(R(L(c))) 
        \overset{\epsilon_{L(c)}}{\longrightarrow}
      L(c)
   $$

   and

   $$
     id_{R(d)}
     \;\colon\;
     R(d)
       \overset{\eta_{R(d)}}{\longrightarrow}
     R(L(R(d)))
       \overset{R(\epsilon_d)}{\longrightarrow}
     R(d)
   $$

=--

+-- {: .proof}
###### Proof

That a hom-isomorphism (eq:HomIsomorphismForAdjointFunctors) implies units/counits satisfying the [[triangle identities]] is the statement of the second two items of Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}.

Hence it remains to show the converse. But the argument is along the same lines as the proof of Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}: We now _define_ forming of adjuncts by the formula (eq:AdjunctFormula). That the resulting assignment $f \mapsto \widetilde f$ is an [[isomorphism]] follows from the computation

$$
  \begin{aligned}
    \widetilde {\widetilde f}
    & =
    \widetilde{ c \overset{\eta_c}{\to} R(L(c)) \overset{R(f)}{\to} R(d) }
    \\
    & =
    L(c) \overset{L(\eta_c)}{\to} L(R(L(c))) \overset{L(R(f))}{\to} L(R(d)) \overset{\epsilon_d}{\to} d
    \\ 
    & = 
    L(c) \overset{L(\eta_c)}{\to} L(R(L(c)))
         \overset{ \epsilon_{L(c)} }{\to}  L(c)
         \overset{f}{\longrightarrow} d
    \\
    & =  L(c) \overset{f}{\longrightarrow} d
  \end{aligned}
$$

where, after expanding out the definition, we used [[natural transformation|naturality]] of $\epsilon$ and then the [[triangle identity]]. 

Finally, that this construction satisfies the naturality condition (eq:NaturalitySquareForAdjointnessOfFunctors) follows from the functoriality of the functors involved, and the naturality of the unit/counit: 

$$
  \array{
    c_2 &\overset{ \eta_{c_2} }{\longrightarrow}& R(L(c_2))
    \\
    {}^{\mathllap{g}}\downarrow && \downarrow^{\mathrlap{R(L(g))}}
    & \searrow^{\mathrlap{ R( L(g) \circ f ) }}
    \\
    c_1 
      &\overset{\eta_{c_1}}{\longrightarrow}& 
    R(L(c_1))
     &\overset{R(f)}{\longrightarrow}&
    R(d_1)
    \\
    && & {}_{R( h\circ f)}\searrow & \downarrow^{\mathrlap{ R(h) }}
    \\
    && && R(d_2)
  }
$$


=--



The condition (eq:HomIsomorphismForAdjointFunctors) on adjoint functors $L \dashv R$ in Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets} implies in particular that for every [[object]] $d \in \mathcal{D}$ the functor $Hom_{\mathcal{D}}(L(-),d)$ is a _[[representable functor]]_ with _[[representing object]]_ $R(d)$. The following Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject} observes that the existence of such [[representing objects]] for all $d$ is, in fact, already sufficient to imply that there is a right adjoint functor.

This equivalent perspective on adjoint functors makes manifest that:

1. adjoint functors are, if they exist, unique up to natural isomorphism, this is Prop. \ref{UniquenessOfAdjoints} below;

1. the concept of adjoint functors makes sense also _[[relative adjoint functor|relative]]_ to a [[full subcategory]] on which representing objects exists, this is the content of Remark \ref{RelativeAdjointFunctors} below.


+-- {: .num_prop #AdjointFunctorFromObjectwiseRepresentingObject}
###### Proposition
**(adjoint functor from objectwise [[representing objects]])**

A [[functor]] $L \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ has a [[right adjoint]] $R \;\colon\; \mathcal{D} \to \mathcal{C}$, according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}, already if 
for all [[objects]] $d \in \mathcal{D}$ there is an object $R(d) \in \mathcal{C}$ such that there is a [[natural isomorphism]]

   $$ 
     Hom_{\mathcal{D}}(L(-),d)
     \underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}
     Hom_{\mathcal{C}}(-,R(d))
     \,,
   $$

   hence for each [[object]] $c \in \mathcal{C}$ a [[bijection]]

   $$
     Hom_{\mathcal{D}}(L(c),d)
     \underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}
     Hom_{\mathcal{C}}(c,R(d))
   $$

   such that for each [[morphism]] $g \;\colon\; c_2 \to c_1$, the following [[commuting diagram|diagram commutes]]

   \[
     \label{HalfNaturalitySquareForAdjointnessOfFunctors}
     \array{
       Hom_{\mathcal{D}}(L(c_1),d)
         &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
       Hom_{\mathcal{C}}(c_1,R(d))
       \\
       {}^{\mathllap{ Hom_{\mathcal{C}}(L(g),id_d) }}
       \big\downarrow 
       &&
       \big\downarrow^{\mathrlap{ Hom_{\mathcal{C}}( f, id_{R(d)}  ) }}
       \\
       Hom_{\mathcal{D}}(L(c_2),d)
         &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
       Hom_{\mathcal{C}}(c_2,R(d))
     }
   \]

   (This is as in (eq:NaturalitySquareForAdjointnessOfFunctors), except that only naturality in the first variable is required.)

In this case there is a unique way to extend $R$ from a function on [[objects]] to a function on [[morphisms]] such as to make it a [[functor]] $R \colon \mathcal{D} \to \mathcal{C}$ which is [[right adjoint]] to $L$.
, and hence the statement is that with this, naturality in the second variable is already implied.

=--

+-- {: .proof}
###### Proof

Notice that 

1. in the language of [[presheaves]] (Example \ref{CategoryOfPresheaves}) the assumption is that for each $d \in \mathcal{D}$ the presheaf 

   $$
     Hom_{\mathcal{D}}(L(-),d)
     \;\in\;
     [\mathcal{D}^{op}, Set]
   $$

   is [[representable functor|represented]] (eq:YonedaFunctor) by the object $R(d)$, and [[natural transformation|naturally]] so. 

1. In terms of the [[Yoneda embedding]] (Prop. \ref{YonedaEmbedding})

   $$
     y 
       \;\colon\;
     \mathcal{D}
      \hookrightarrow
     [\mathcal{D}^{op}, Set]
   $$ 

   we have 

   \[
     \label{YonedanotationForRepresentable}
     Hom_{\mathcal{C}}(-,R(d))
     =
     y(R(d))
   \]



The condition (eq:NaturalitySquareForAdjointnessOfFunctors) says equivalently that $R$ has to be such that for all [[morphisms]] $h \;\colon\; d_1 \to d_2 $ the following diagram in the [[category of presheaves]] $[\mathcal{C}^{op}, Set]$ [[commuting diagram|commutes]]

$$
  \array{
    Hom_{\mathcal{D}}(L(-),d_1)
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(-,R(d_1))
    \\
    {}^{\mathllap{ Hom_{\mathcal{C}}( L(-) , h ) }}
    \big\downarrow 
    &&
    \big\downarrow^{\mathrlap{ Hom_{\mathcal{C}}( -, R(h)  ) }}
    \\
    Hom_{\mathcal{D}}(L(-),d_2)
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(-, R(d_2))
  }
$$

This manifestly has a unique solution 

$$
  y(R(h))
  \;=\;
  Hom_{\mathcal{C}}(-,R(h))
$$ 

for every morphism $h \colon d_1 \to d_2$ under  $y(R(-))$ (eq:YonedanotationForRepresentable). But the [[Yoneda embedding]] $y$ is a [[fully faithful functor]] (Prop. \ref{YonedaEmbedding}), which means that thereby also $R(h)$ is uniquely fixed.

=--

+-- {: .num_prop #UniquenessOfAdjoints}
###### Proposition
**([[adjoint functors]] are unique up to [[natural isomorphism]])**

The [[left adjoint]] or [[right adjoint]] to a [[functor]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}), if it exists, is unique up to  [[natural isomorphism]] (Def. \ref{NaturalTransformations}).

=--

+-- {: .proof}
###### Proof

Suppose the functor $L \colon \mathcal{D} \to \mathcal{C}$ is given, and we are asking for uniqueness of its right adjoint, if it exists. The other case is directly analogous.

Suppose that $R_1, R_2 \;\colon\; \mathcal{C} \to \mathcal{D}$ are two [[functors]] which both are [[right adjoint]] to $L$. Then for each $d \in \mathcal{D}$ the corresponding two hom-isomorphisms (eq:HomIsomorphismForAdjointFunctors) combine to say that there is a [[natural isomorphism]]/

$$
  \Phi_d
  \;\colon\;
  Hom_{\mathcal{C}}(-,R_1(d))
  \;\simeq\;
  Hom_{\mathcal{C}}(-,R_2(d))
$$

As in the proof of Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject}, the [[Yoneda lemma]] implies that 

$$
  \Phi_d \;=\; y( \phi_d )
$$

for some [[isomorphism]]

$$
  \phi_d \;\colon\;  R_1(d) \overset{\simeq}{\to} R_2(d)
  \,.
$$

But then the uniqueness statement of Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject} implies that the collection of these isomorphisms for each object constitues a [[natural isomorphism]] between the functors (Def. \ref{NaturalTransformations}).

=--



## Categorical algebra

### Enriched categories

+-- {: .num_defn #CartesianClosedCategory}
###### Definition
**([[cartesian closed category]])**

A [[category]] $\mathcal{V}$ is called 

1. a _[[cartesian monoidal category]]_ if 

   1. it has a [[terminal object]] $\ast$;

   1. for all [[objects]] $X,Y \in \mathcal{V}$ their [[Cartesian product]] $X \times Y$ exists;

1. a _[[cartesian closed category]]_ if, in addition, for each [[object]] $X \in \mathcal{V}$ the [[functor]] of taking the [[Cartesian product]] with $X$ has a [[right adjoint functor]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}), to be denoted $[X,-]$

   $$
     \mathcal{V}
       \underoverset
         {\underset{[X,-]}{\longrightarrow}}
         {\overset{X \times (-)}{\longleftarrow}}
         {\bot}
     \mathcal{V}
   $$

   In this case $[X,Y] \in \mathcal{V}$ is called the _[[internal hom]]_ from $X$ to $Y$.

=--

+-- {: .num_example #SetIsCartesianClosed}
###### Example
**([[Set]] is a [[cartesian closed category]])**

The [[category]] [[Set]] of all [[sets]] (Example \ref{CategoryOfAllSets}) is a [[cartesian closed category]] (Def. \ref{CartesianClosedCategory}). The [[Cartesian product]] is the original Cartesian product of sets, and the [[internal hom]] is the [[function set]] $[X,Y]$ of functions from $X$ to $Y$

=--



+-- {: .num_defn #TopEnrichedCategory}
###### Definition

Let $\mathcal{V}$ be a [[cartesian closed category]] (Def. \ref{CartesianClosedCategory}).

A **$\mathcal{V}$-[[enriched category]]** $\mathcal{C}$ is:

1. a [[class]] $Obj(\mathcal{C})$, called the **class of [[objects]]**;

1. for each $a, b\in Obj(\mathcal{C})$ a an [[object]]

   $$
     \mathcal{C}(a,b)\in \mathcal{V}
     \,,
   $$

   called the **$\mathcal{V}$-object of [[morphisms]]** between $a$ and $b$;

1. for each $a,b,c\in Obj(\mathcal{C})$ a [[morphism]] in $\mathcal{V}$

   $$
     \circ_{a,b,c} 
       \;\colon\; 
      \mathcal{C}(a,b)\times \mathcal{C}(b,c) 
        \longrightarrow 
      \mathcal{C}(a,c)
   $$

   out of the [[cartesian product]], called the _[[composition]]_ operation;

1. for each $a \in Obj(\mathcal{C})$ a morphism  $Id_a \colon \ast \to  \mathcal{C}(a,a)$, called the _[[identity]]_ morphism on $a$

such that the composition is [[associativity|associative]] and [[unitality|unital]].

=--

+-- {: .num_remark #UnderlyingCategoryOfTopEnrichedCategory}
###### Remark

Given a (pointed) [[topologically enriched category]] as in def. \ref{TopEnrichedCategory}, then forgetting the topology on the [[hom-spaces]] (along the [[forgetful functor]] $U \colon Top_{cg} \to Set$) yields an ordinary [[locally small category]] with

$$
  Hom_{\mathcal{C}}(a,b) = U(\mathcal{C}(a,b))
  \,.
$$

It is in this sense that $\mathcal{C}$ is a category with [[extra structure]], and hence "[[enriched category|enriched]]".

=---

The archetypical example is $Top_{cg}$ itself:

+-- {: .num_example #TopkAsATopologicallyEnrichedCategory}
###### Example

The category $Top_{cg}$ (def. \ref{kTop}) canonically obtains the structure of a [[topologically enriched category]], def. \ref{TopEnrichedCategory}, with [[hom-spaces]] given by the compactly generated [[mapping spaces]] (def. \ref{CompactlyGeneratedMappingSpaces})

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

given by the [[adjunct]] under the (product$\dashv$ mapping-space)-[[adjunction]] from prop. \ref{CartesianClosureOfTopcg} of the [[evaluation morphisms]]

$$
  X \times Y^X \times Z^Y
    \overset{(ev, id)}{\longrightarrow}
  Y \times Z^Y
    \overset{ev}{\longrightarrow}
  Z
  \,.
$$

Similarly, [[pointed topological spaces|pointed]] [[compactly generated topological spaces]] $Top_k^{\ast/}$ form a pointed topologically enriched category, using the [[pointed mapping spaces]] from example \ref{PointedMappingSpace}:

$$
  Top^{\ast/}_{cg}(X,Y)
   \coloneqq
  Maps(X,Y)_\ast
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
     F_0 \;\colon\; Obj(\mathcal{C}) \longrightarrow Obj(\mathcal{D})
   $$

   of [[objects]];

1. for each $a,b \in Obj(\mathcal{C})$ a [[continuous function]]

   $$
     F_{a,b} \;\colon\; \mathcal{C}(a,b) \longrightarrow \mathcal{D}(F_0(a), F_0(b))
   $$

   of [[hom-spaces]],

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

We write $[\mathcal{C}, \mathcal{D}]$ for the resulting category of topologically enriched functors.

=--

+-- {: .num_remark #TopologicallyEnrichedNaturalTransformationIsTransformationOfUnderlyingFunctors}
###### Remark

The condition on an [[enriched natural transformation]] in def. \ref{TopologicallyEnrichedFunctor} is just that on an ordinary [[natural transformation]] on the underlying unenriched functors, saying that for every morphisms $f \colon c \to d$ there is a [[commuting square]]

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
  \,.
$$

=--


+-- {: .num_example #TopologicallyEnrichedFunctorsToTopk}
###### Example

For $\mathcal{C}$ any [[topologically enriched category]], def. \ref{TopEnrichedCategory} then a [[topologically enriched functor]] (def. \ref{TopologicallyEnrichedFunctor})

$$
  F \;\colon\; \mathcal{C} \longrightarrow Top_{cg}
$$

to the archetical topologically enriched category from example \ref{TopkAsATopologicallyEnrichedCategory} may be thought of as a topologically enriched [[copresheaf]], at least if $\mathcal{C}$ is [[small category|small]] (in that its [[class]] of objects is a proper [[set]]).

Hence the category of topologically enriched functors

$$
  [\mathcal{C}, Top_{cg}]
$$

according to def. \ref{TopologicallyEnrichedFunctor} may be thought of as the ([[copresheaf|co-]])[[presheaf category]] over $\mathcal{C}$ in the realm of topological enriched categories.

A functor $F \in [\mathcal{C}, Top_{cg}]$ is equivalently

1. a [[compactly generated topological space]] $F_a \in Top_{cg}$ for each object $a \in Obj(\mathcal{C})$;

1. a [[continuous function]]

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

+-- {: .num_prop #TopologicallyEnrichedCopresheavesHaveAllLimitsAndColimits}
###### Proposition

For $\mathcal{C}$ any [[small category|small]] [[topologically enriched category]], def. \ref{TopEnrichedCategory} then the [[enriched functor category]] $[\mathcal{C}, Top_{cg}]$ from example \ref{TopologicallyEnrichedFunctorsToTopk} has all [[limits]] and [[colimits]], and they are computed objectwise:

if

$$
  F_\bullet
    \;\colon\;
  I
    \longrightarrow
  [\mathcal{C}, Top_{cg}]
$$

is a [[diagram]] of [[functors]] and $c\in \mathcal{C}$ is any object, then

$$
  (\underset{\longleftarrow}{\lim}_i F_i)(c) \simeq \underset{\longleftarrow}{\lim}_i (F_i(c)) \;\;\in Top_{cg}
$$

and

$$
  (\underset{\longrightarrow}{\lim}_i F_i)(c) \simeq \underset{\longrightarrow}{\lim}_i (F_i(c)) \;\; \in Top_{cg}
  \,.
$$

=--

+-- {: .proof}
###### Proof

First consider the underlying diagram of functors $F_i^\circ$ where the topology on the [[hom-spaces]] of $\mathcal{C}$ and of $Top_{cg}$ has been forgotten. Then one finds

$$
  (\underset{\longleftarrow}{\lim}_i F^\circ_i)(c) \simeq \underset{\longleftarrow}{\lim}_i (F^\circ_i(c)) \;\;\in Set
$$

and

$$
  (\underset{\longrightarrow}{\lim}_i F^\circ _i)(c) \simeq \underset{\longrightarrow}{\lim}_i (F^\circ_i(c)) \;\; \in Set
$$

by the [[universal property]] of limits and colimits. (Given a morphism of diagrams then a unique compatible morphism between their limits or colimits, respectively, is induced as the universal factorization of the morphism of diagrams regarded as a cone or cocone, respectvely, over the codomain or domain diagram, respectively).

Hence it only remains to see that equipped with topology, these limits and colimits in $Set$ become limits and colimits in $Top_{cg}$. That is just the statement of prop. \ref{DescriptionOfLimitsAndColimitsInTop} with corollary \ref{kTopIsCoreflectiveSubcategory}.


=--


+-- {: .num_defn #TensoringAndPoweringOfTopologicallyEnrichedCopresheaves}
###### Definition

Let $\mathcal{C}$ be a [[topologically enriched category]], def. \ref{TopEnrichedCategory}, with $[\mathcal{C}, Top_{cg}]$ its category of topologically enriched copresheaves from example \ref{TopologicallyEnrichedFunctorsToTopk}.

1. Define a functor

   $$
     (-)\cdot(-)
       \;\colon\;
     [\mathcal{C}, Top_{cg}] \times Top_{cg}
      \longrightarrow
     [\mathcal{C}, Top_{cg}]
   $$

   by forming objectwise [[cartesian products]] (hence $k$ of [[product topological spaces]])

   $$
     F \cdot X \;\colon\; c \mapsto F(c) \times X
     \,.
   $$

   This is called the **[[tensoring]]** of $[\mathcal{C},Top_{cg}]$ over $Top_{cg}$.

1. Define a functor

   $$
     (-)^{(-)}
       \;\colon\;
     (Top_{cg})^{op} \times [\mathcal{C}, Top_{cg}]
       \longrightarrow
     [\mathcal{C}, Top_{cg}]
   $$

   by forming objectwise compactly generated [[mapping spaces]] (def. \ref{CompactlyGeneratedMappingSpaces})

   $$
     F^X \;\colon\; c \mapsto F(c)^X
     \,.
   $$

   This is called the **[[powering]]** of $[\mathcal{C}, Top_{cg}]$ over $Top_{cg}$.

Analogously, for $\mathcal{C}$ a pointed [[topologically enriched category]], def. \ref{TopEnrichedCategory}, with $[\mathcal{C}, Top_{cg}^{\ast/}]$ its category of pointed topologically enriched copresheaves from example \ref{TopologicallyEnrichedFunctorsToTopk}, then:

1. Define a functor

   $$
     (-)\wedge(-)
       \;\colon\;
     [\mathcal{C}, Top^{\ast/}_{cg}] \times Top^{\ast/}_{cg}
      \longrightarrow
     [\mathcal{C}, Top^{\ast/}_{cg}]
   $$

   by forming objectwise [[smash products]] (def. \ref{SmashProductOfPointedObjects})

   $$
     F \wedge X \;\colon\; c \mapsto F(c) \wedge X
     \,.
   $$

   This is called the **smash [[tensoring]]** of $[\mathcal{C},Top^{\ast/}_{cg}]$ over $Top^{\ast/}_{cg}$.

1. Define a functor

   $$
     Maps(-,-)_\ast
       \;\colon\;
     Top^{\ast/}_{cg} \times [\mathcal{C}, Top^{\ast/}_{cg}]
       \longrightarrow
     [\mathcal{C}, Top^{\ast/}_{cg}]
   $$

   by forming objectwise [[pointed mapping spaces]] (example \ref{PointedMappingSpace})

   $$
     F^X \;\colon\; c \mapsto Maps(X,F(c))_\ast
     \,.
   $$

   This is called the **pointed [[powering]]** of $[\mathcal{C}, Top_{cg}]$ over $Top_{cg}$.


=--

There is a full blown $Top_{cg}$-[[enriched Yoneda lemma]]. The following records a slightly simplified version which is all that is needed here:

+-- {: .num_prop #TopologicallyEnrichedYonedaLemma}
###### Proposition
**(topologically enriched Yoneda-lemma)**

Let $\mathcal{C}$ be a [[topologically enriched category]], def. \ref{TopEnrichedCategory}, write $[\mathcal{C}, Top_{cg}]$ for its category of topologically enriched (co-)presheaves, and for $c\in Obj(\mathcal{C})$ write $y(c) = \mathcal{C}(c,-) \in [\mathcal{C}, Top_k]$ for the topologically enriched functor that it represents, all according to example \ref{TopologicallyEnrichedFunctorsToTopk}. Recall the [[tensoring]] operation $(F,X) \mapsto F \cdot X$ from def. \ref{TensoringAndPoweringOfTopologicallyEnrichedCopresheaves}.

For $c\in Obj(\mathcal{C})$, $X \in Top_{cg}$ and $F \in [\mathcal{C}, Top_{cg}]$, there is a [[natural bijection]] between

1. morphisms $y(c) \cdot X \longrightarrow F$ in $[\mathcal{C}, Top_{cg}]$;

1. morphisms $X \longrightarrow F(c)$ in $Top_{cg}$.

In short:

$$
  \frac{
    y(c)\cdot X \longrightarrow F
  }{
    X \longrightarrow F(c)
  }
$$


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

agree. This means (remark \ref{TopologicallyEnrichedNaturalTransformationIsTransformationOfUnderlyingFunctors}) that they may be thought of jointly as a function with values in commuting squares in $Top_{cg}$ of this form:

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



### Monoidal enriched categories


+-- {: .num_defn #MonoidalCategory}
###### Definition

An **[[enriched category|enriched]] [[monoidal category]]** is a  [[enriched category]] $\mathcal{C}$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)) equipped with

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

1. {#MonoidalCategoryUnitors} a [[natural isomorphism]]

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

   $$
     \array{
       && (w \otimes x) \otimes (y \otimes z)
       \\
       & {}^{\mathllap{\alpha_{w \otimes x, y, z}}}\nearrow
        &&
       \searrow^{\mathrlap{\alpha_{w,x,y \otimes z}}}
       \\
       ((w \otimes x ) \otimes y) \otimes z
        && &&
       (w \otimes (x \otimes (y \otimes z)))
       \\
       {}^{\mathllap{\alpha_{w,x,y}} \otimes id_z }\downarrow
        && &&
       \uparrow^{\mathrlap{ id_w \otimes \alpha_{x,y,z} }}
       \\
       (w \otimes (x \otimes y)) \otimes z
         && \underset{\alpha_{w,x \otimes y, z}}{\longrightarrow} &&
       w \otimes ( (x \otimes y) \otimes z )
     }
   $$


=--


+-- {: .num_lemma #kel1}
###### Lemma
**([Kelly 64](monoidal+category#Kelly))**

Let $(\mathcal{C}, \otimes, 1)$ be a [[monoidal category]], def. \ref{MonoidalCategory}. Then the left and right [[unitors]] $\ell$ and $r$ satisfy the following conditions:

1. $\ell_1 = r_1 \;\colon\; 1 \otimes 1 \overset{\simeq}{\longrightarrow} 1$;

1. for all objects $x,y \in \mathcal{C}$ the following [[commuting diagram|diagrams commutes]]:

   $$
     \array{
       (1 \otimes x) \otimes y  & &
       \\
       {}^\mathllap{\alpha_{1, x, y}} \downarrow
       & \searrow^\mathrlap{\ell_x \otimes id_y} &
       \\
       1 \otimes (x \otimes y)
       & \underset{\ell_{x \otimes y}}{\longrightarrow} & x \otimes y
     }
     \,;
   $$

   and

   $$
     \array{
       x \otimes (y \otimes 1) & &
       \\
       {}^\mathllap{\alpha^{-1}_{1, x, y}} \downarrow
       & \searrow^\mathrlap{id_x \otimes r_y} &
       \\
       (x \otimes y) \otimes 1
         &
           \underset{r_{x \otimes y}}{\longrightarrow}
         &
       x \otimes y
     }
     \,;
   $$

=--

For **proof** see at _[[monoidal category]]_ [this lemma](monoidal+category#kel1) and [this lemma](monoidal+category#kel2).

+-- {: .num_remark #CoherenceForMonoidalCategories}
###### Remark

Just as for an [[associative algebra]] it is sufficient to demand $1 a = a$ and $a 1 = a$ and $(a b) c = a (b c)$ in order to have that expressions of arbitrary length may be re-bracketed at will, so there is a _[[coherence theorem for monoidal categories]]_ which states that all ways of freely composing the [[unitors]] and [[associators]] in a [[monoidal category]] (def. \ref{MonoidalCategory}) to go from one expression to another will coincide. Accordingly, much as one may drop the notation for the bracketing in an [[associative algebra]] altogether, so one may, with due care, reason about monoidal categories without always making all unitors and associators explicit.

(Here the qualifier "freely" means informally that we must not use any non-formal identification between objects, and formally it means that the diagram in question must be in the image of a [[strong monoidal functor]] from a _free_ monoidal category. For example if in a particular monoidal category it so happens that the object $X \otimes (Y \otimes Z)$ is actually _equal_ to $(X \otimes Y)\otimes Z$, then the various ways of going from one expression to another using only associators _and_ this equality no longer need to coincide.)

=--

+-- {: .num_defn #BraidedMonoidalCategory}
###### Definition

A **(pointed) [[topologically enriched category|topological]] [[braided monoidal category]]**, is a (pointed) [[topologically enriched category|topological]] [[monoidal category]] $\mathcal{C}$ (def. \ref{MonoidalCategory}) equipped with a [[natural isomorphism]]

$$
  \tau_{x,y} \colon x \otimes y \to y \otimes x
$$

called the **[[braiding]]**, such that the following two kinds of [[commuting diagram|diagrams commute]] for all [[objects]] involved ("hexagon identities"):

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

+-- {: .num_remark #SymmetricMonoidalCategoriesCoherenceTheorem}
###### Remark

In analogy to the [[coherence theorem for monoidal categories]] (remark \ref{CoherenceForMonoidalCategories}) there is a [[coherence theorem for symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}), saying that every diagram built freely (see remark \ref{SymmetricMonoidalCategoriesCoherenceTheorem}) from [[associators]], [[unitors]] and [[braidings]] such that both sides of the diagram correspond to the same [[permutation]] of objects, coincide.

=--


+-- {: .num_defn #ClosedMonoidalCategory}
###### Definition

Given a (pointed) [[topologically enriched category|topological]] [[symmetric monoidal category]] $\mathcal{C}$ with [[tensor product]] $\otimes$ (def. \ref{SymmetricMonoidalCategory}) it is called a **[[closed monoidal category]]** if for each $Y \in \mathcal{C}$ the functor $Y \otimes(-)\simeq (-)\otimes Y$ has a [[right adjoint]], denoted $hom(Y,-)$

$$
  \mathcal{C}
    \underoverset
      {\underset{hom(Y,-)}{\longrightarrow}}
      {\overset{(-) \otimes Y}{\longleftarrow}}
      {\bot}
  \mathcal{C}
  \,,
$$

hence if there are [[natural bijections]]

$$
  Hom_{\mathcal{C}}(X \otimes Y, Z)
   \;\simeq\;
  Hom_{\mathcal{C}}{C}(X, hom(Y,Z))
$$

for all objects $X,Z \in \mathcal{C}$.

Since for the case that $X = 1$ is the [[tensor unit]] of $\mathcal{C}$ this means that

$$
  Hom_{\mathcal{C}}(1,hom(Y,Z)) \simeq Hom_{\mathcal{C}}(Y,Z)
  \,,
$$

the object $hom(Y,Z) \in \mathcal{C}$ is an enhancement of the ordinary [[hom-set]] $Hom_{\mathcal{C}}(Y,Z)$ to an object in $\mathcal{C}$.
Accordingly, it is also called the **[[internal hom]]** between $Y$ and $Z$.

=--


In a [[closed monoidal category]], the adjunction isomorphism between [[tensor product]] and [[internal hom]] even holds internally:

+-- {: .num_prop #TensorHomAdjunctionIsoInternally}
###### Proposition

In a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] (def. \ref{ClosedMonoidalCategory}) there are [[natural isomorphisms]]

$$
  hom(X \otimes Y, Z)
   \;\simeq\;
  hom(X, hom(Y,Z))
$$

whose image under $Hom_{\mathcal{C}}(1,-)$ are the defining [[natural bijections]] of def. \ref{ClosedMonoidalCategory}.

=--

+-- {: .proof}
###### Proof

Let $A \in \mathcal{C}$ be any object. By applying the defining natural bijections twice, there are composite natural bijections

$$
  \begin{aligned}
    Hom_{\mathcal{C}}(A , hom(X \otimes Y, Z))
    & \simeq
    Hom_{\mathcal{C}}(A \otimes (X \otimes Y), Z)
    \\
    & \simeq
    Hom_{\mathcal{C}}((A \otimes X)\otimes Y, Z)
    \\
    & \simeq
    Hom_{\mathcal{C}}(A \otimes X, hom(Y,Z))
    \\
    & \simeq
    Hom_{\mathcal{C}}(A, hom(X,hom(Y,Z)))
  \end{aligned}
  \,.
$$

Since this holds for all $A$, the [[Yoneda lemma]] (the [[fully faithful functor|fully faithfulness]] of the [[Yoneda embedding]]) says that there is an isomorphism $hom(X\otimes Y, Z) \simeq hom(X,hom(Y,Z))$. Moreover, by taking $A = 1$ in the above and using the left [[unitor]] isomorphisms $A \otimes (X \otimes Y) \simeq X \otimes Y$ and $A\otimes X \simeq X$  we get a [[commuting diagram]]

$$
  \array{
    Hom_{\mathcal{C}}(1,hom(X\otimes Y, ))
      &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(1,hom(X,hom(Y,Z)))
    \\
    {}^{\mathllap{\simeq}}\downarrow
      &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    Hom_{\mathcal{C}}(X \otimes Y, Z)
     &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(X, hom(Y,Z))
  }
  \,.
$$

=--



+-- {: .num_example #TopAsASymmetricMonoidalCategory}
###### Example

The category [[Set]] of [[sets]] and [[functions]] between them, regarded as enriched in [[discrete topological spaces]], becomes a [[symmetric monoidal category]] according to def. \ref{SymmetricMonoidalCategory} with [[tensor product]] the [[Cartesian product]] $\times$ of sets. The [[associator]], [[unitor]] and [[braiding]] isomorphism are the evident (almost unnoticable but nevertheless nontrivial) canonical identifications.

Similarly the category $Top_{cg}$ of [[compactly generated topological spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#kTop)) becomes a [[symmetric monoidal category]] with [[tensor product]] the corresponding [[Cartesian products]], hence the operation of forming k-ified ([cor.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)) [[product topological spaces]] ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#ProductTopologicalSpace)). The underlying functions of the [[associator]], [[unitor]] and [[braiding]] isomorphisms are just those of the underlying sets, as above.

Symmetric monoidal categories, such as these, for which the tensor product is the [[Cartesian product]] are called _[[Cartesian monoidal categories]]_.

Both examples are [[closed monoidal categories]] (def. \ref{ClosedMonoidalCategory}), with [[internal hom]] the [[mapping spaces]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#MappingTopologicalSpaceIsExponentialObject)).

=--

+-- {: .num_example #PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}
###### Example

The category $Top_{cg}^{\ast/}$ of [[pointed topological space|pointed]] [[compactly generated topological spaces]] with [[tensor product]] the  [[smash product]] $\wedge$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#SmashProductOfPointedObjects))

$$
  X \wedge Y \coloneqq \frac{X\times Y}{X\vee Y}
$$

is a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}) with [[unit object]] the pointed [[0-sphere]] $S^0$.

The components of the [[associator]], the [[unitors]] and the [[braiding]] are those of [[Top]] as in example \ref{TopAsASymmetricMonoidalCategory}, descended to the [[quotient topological spaces]] which appear in the definition of the [[smash product]]. This works for pointed [[compactly generated spaces]] (but not for general pointed topological spaces) by [this prop.](Introduction+to+Stable+homotopy+theory+--+P#SmashProductInTopcgIsAssociative).

The category $Top^{\ast/}_{cg}$ is also a [[closed monoidal category]] (def. \ref{ClosedMonoidalCategory}), with [[internal hom]] the pointed [[mapping space]] $Maps(-,-)_\ast$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#PointedMappingSpace))

=--


+-- {: .num_example #ExampleAbelianGroupsOfMonoidalCategory}
###### Example

The category [[Ab]] of [[abelian groups]], regarded as enriched in [[discrete topological spaces]], becomes a [[symmetric monoidal category]] with tensor product the actual [[tensor product of abelian groups]] $\otimes_{\mathbb{Z}}$ and with [[tensor unit]] the additive group $\mathbb{Z}$ of [[integers]]. Again the [[associator]], [[unitor]] and [[braiding]] isomorphism are the evident ones coming from the underlying sets, as in example \ref{TopAsASymmetricMonoidalCategory}.

This is a [[closed monoidal category]] with [[internal hom]] $hom(A,B)$ being the set of [[homomorphisms]] $Hom_{Ab}(A,B)$ equipped with the pointwise group structure for $\phi_1, \phi_2 \in Hom_{Ab}(A,B)$ then $(\phi_1 + \phi_2)(a) \coloneqq \phi_1(a) + \phi_2(b) \; \in B$.

This is the archetypical case that motivates the notation "$\otimes$" for the pairing operation in a [[monoidal category]]:

=--

### Enriched ends and coends
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

By functoriality and under passing to [[adjuncts]] ([cor.](Introduction+to+Stable+homotopy+theory+--+P#SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces)) this is equivalent to two commuting _[[actions]]_


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

then this takes the form of a "pullback action" in the first variable

$$
  \rho_{c_2,c_1}(d)
   \;\colon\;
  \mathcal{C}(c_1,c_2) \wedge F_0((c_2,d))
    \longrightarrow
  F_0((c_1,d))
$$

and a "pushforward action" in the second variable

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

+-- {: .num_example #CoendGivesQuotientByDiagonalGroupAction}
###### Example

Let $G$ be a [[topological group]]. Write $\mathbf{B}(G_+)$ for the pointed [[topologically enriched category]] that has a single object $\ast$, whose single [[hom-space]] is $G_+$ ($G$ with a basepoint freely adjoined ([def.](Introduction+to+Stable+homotopy+theory+--+P#BasePointAdjoined)))

$$
  \mathbf{B}(G_+)(\ast,\ast) \coloneqq G_+
$$

and whose composition operation is the product operation $(-)\cdot(-)$ in $G$ under adjoining basepoints ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#WedgeAndSmashOfBasePointAdjoinedTopologicalSpaces))

$$
  G_+ \wedge G_+
   \simeq
  (G \times G)_+
    \overset{((-)\cdot (-))_+}{\longrightarrow}
   G_+
  \,.
$$

Then a [[topologically enriched functor]]

$$
  (X,\rho_l) \;\colon\; \mathbf{B}(G_+) \longrightarrow Top^{\ast/}_{cg}
$$

is a pointed topological space $X \coloneqq F(\ast)$ equipped with a continuous function

$$
  \rho_l \;\colon\; G_+ \wedge X \longrightarrow X
$$

satisfying the [[action]] property. Hence this is equivalently a continuous and basepoint-preserving left [[action]] (non-linear [[representation]]) of $G$ on $X$.

The [[opposite category]] (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}) $(\mathbf{B}(G_+))^{op}$ comes from the [[opposite group]]

$$
  (\mathbf{B}(G_+))^{op}
  =
  \mathbf{B}(G^{op}_+)
  \,.
$$

(The canonical continuous isomorphism $G \simeq G^{op}$ induces a canonical euqivalence of topologically enriched categories $(\mathbf{B}(G_+))^{op} \simeq \mathbf{B}(G_+)$.)

So a topologically enriched functor

$$
  (Y,\rho_r) \;\colon\; (\mathbf{B}(G_+))^{op} \longrightarrow Top^{\ast}_{cg}
$$

is equivalently a basepoint preserving continuous _right_ action of $G$.

Therefore the [[coend]] of two such functors (def. \ref{EndAndCoendInTopcgSmash}) coequalizes the relation

$$
  (x g,\;y)
   \sim
  (x,\; g y)
$$

(where juxtaposition denotes left/right action) and hence is equivalently the canonical smash product of a right $G$-action with a left $G$-action, hence the [[quotient topological space|quotient]] of the plain smash product by the [[diagonal action]] of the group $G$:

$$
  \overset{\ast \in \mathbf{B}(G_+)}{\int}
   (Y,\rho_r)(\ast) \,\wedge\, (X,\rho_l)(\ast)
  \;\simeq\;
  Y \wedge_G X
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
two pointed [[topologically enriched functors]], then the [[end]] (def. \ref{EndAndCoendInTopcgSmash}) of $Maps(F(-),G(-))_\ast$ is a topological space whose underlying [[pointed set]] is the pointed set of [[natural transformations]] $F\to G$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)):

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
        {\underset{\underset{c,d}{\sqcup} U(\tilde \rho_{(c,d)}(c))  }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} U(\tilde\rho_{d,c}(d))}{\longrightarrow}}
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

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). Define the structure of a pointed [[topologically enriched category]] on the category $[\mathcal{C}, Top_{cg}^{\ast/}]$ of pointed [[topologically enriched functors]] to $Top^{\ast/}_{cg}$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctorsToTopk)) by taking the [[hom-spaces]] to be given by the [[ends]] (def. \ref{EndAndCoendInTopcgSmash}) of example \ref{NaturalTransformationsViaEnds}:

$$
  [\mathcal{C},Top^{\ast/}_{cg}](F,G)
    \;\coloneqq\;
  \int_{c\in \mathcal{C}} Maps(F(c),G(c))_\ast
$$

The [[composition]] operation on these is defined to be the one induced by the composite maps

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
  \,,
$$

where the first, morphism is degreewise given by projection out of the limits that defined the ends. This composite evidently equalizes the two relevant adjunct actions (as in the proof of example \ref{NaturalTransformationsViaEnds}) and hence defines a map into the end

$$
    \left(
    \underset{c\in \mathcal{C}}{\int} Maps(F(c),G(c))_\ast
  \right)
  \wedge
  \left(
    \underset{c \in \mathcal{C}}{\int} Maps(G(c),H(c))_\ast
  \right)
  \longrightarrow
  \underset{c\in \mathcal{C}}{\int} Maps(F(c),H(c))_\ast
  \,.
$$


The resulting pointed [[topologically enriched category]] $[\mathcal{C},Top^{\ast/}_{cg}]$ is also called the **$Top^{\ast/}_{cg}$-[[enriched functor category]]** over $\mathcal{C}$ with coefficients in $Top^{\ast/}_{cg}$.

=--

This yields an equivalent formulation in terms of ends of the pointed topologically [[enriched Yoneda lemma]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedYonedaLemma)):

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

The **proof** of prop. \ref{YonedaReductionTopological} is [[formal dual|formally dual]] to the proof of the next prop. \ref{TopologicalCoYonedaLemma}.

Now that [[natural transformations]] are expressed in terms of [[ends]] (example \ref{NaturalTransformationsViaEnds}), as is the Yoneda lemma (prop. \ref{YonedaReductionTopological}), it is natural to consider the [[formal duality|dual]] statement involving [[coends]]:

+-- {: .num_prop #TopologicalCoYonedaLemma}
###### Proposition
**([[co-Yoneda lemma]])**

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). For $F \colon \mathcal{C}\to Top^{\ast/}_{cg}$ a pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) and for $c\in \mathcal{C}$ an object, there is a [[natural isomorphism]]

$$
  F(-)
    \simeq
  \overset{c \in \mathcal{C}}{\int}
  \mathcal{C}(c,-) \wedge F(c)
  \,.
$$

Moreover, the morphism that hence exhibits $F(c)$ as the [[coequalizer]] of the two morphisms in def. \ref{EndAndCoendInTopcgSmash} is componentwise the canonical action

$$
  \mathcal{C}(c,d) \wedge F(c)
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
  ( c \overset{}{\to} c_0,\; x  )
  \;\;
   \in
   \mathcal{C}(c,c_0) \wedge F(c)
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

Since the pointed compactly generated [[mapping space]] functor ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#PointedMappingSpace))

$$
  Maps(-,-)_\ast
  \;\colon\;
  \left(Top^{\ast/}_{cg}\right)^{op}
  \times
  Top^{\ast/}_{cg}
  \longrightarrow
  Top^{\ast/}_{cg}
$$

takes [[colimits]] in the first argument and [[limits]] in the second argument to limits ([cor.](Introduction+to+Stable+homotopy+theory+--+P#MappingSpacesSendsColimitsInFirstArgumentToLimits)), it in particular takes [[coends]] in the first argument and [[ends]] in the second argument, to ends (def. \ref{EndAndCoendInTopcgSmash}):

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

With this [[coend]] calculus in hand, there is an elegant proof of the defining [[universal property]] of the smash [[tensoring]]  of [[topologically enriched functors]] $[\mathcal{C},Top^{\ast}_{cg}]$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#TensoringAndPoweringOfTopologicallyEnrichedCopresheaves))


+-- {: .num_prop #UniversalPropertyOfTensoringAndPoweringOfFunctorsToTopcg}
###### Proposition

For $\mathcal{C}$ a pointed [[topologically enriched category]], there are [[natural isomorphisms]]

$$
  [\mathcal{C},Top^{\ast/}_{cg}]( X \wedge K ,\, Y )
    \;\simeq\;
  Maps(K,\; [\mathcal{C},Top^{\ast/}_{cg}](X,Y))_\ast
$$

and

$$
  [\mathcal{C},Top^{\ast/}_{cg}](X,\, Maps(K,Y)_\ast)
    \;\simeq\;
  Maps(K,\; [\mathcal{C},Top^{\ast/}_{cg}](X,Y))
$$

for all $X,Y \in [\mathcal{C},Top^{\ast/}_{cg}]$ and all $K \in Top^{\ast/}_{cg}$.

In particular there is the combined natural isomorphism

$$
  [\mathcal{C}, Top^{\ast/}_{cg}](X\wedge K, Y)
   \;\simeq\;
  [\mathcal{C}, Top^{\ast/}_{cg}](X, Maps(K,Y)_\ast)
$$

exhibiting a pair of [[adjoint functors]]

$$
  [\mathcal{C}, Top^{\ast/}_{cg}]
    \underoverset
      {\underset{Maps(K,-)_\ast}{\longrightarrow}}
      {\overset{(-)\wedge K}{\longleftarrow}}
      {\bot}
  [\mathcal{C}, Top^{\ast}_{cg}]
  \,.
$$

=--

+-- {: .proof}
###### Proof

Via the [[end]]-expression for $[\mathcal{C},Top^{\ast/}_{cg}](-,-)$ from def. \ref{PointedTopologicalFunctorCategory} and the fact (remark \ref{MappingSpacePreservesEnds}) that the pointed mapping space construction $Maps(-,-)_\ast$ preserves ends in the second variable, this reduces to the fact that $Maps(-,-)_\ast$ is the [[internal hom]] in the [[closed monoidal category]] $Top^{\ast/}_{cg}$ (example \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}) and hence satisfies the internal tensor/hom-adjunction isomorphism (prop. \ref{TensorHomAdjunctionIsoInternally}):

$$
  \begin{aligned}
    [\mathcal{C},Top^{\ast/}_{cg}](X \wedge K, Y)
    & =
    \underset{c}{\int}
    Maps(
      (X \wedge K)(c),
      Y(c)
    )_\ast
    \\
    & \simeq
    \underset{c}{\int}
      Maps(X(c) \wedge K, Y(x))_\ast
    \\
    & \simeq
    \underset{c}{\int}
      Maps(K,Maps(X(c), Y(c))_\ast)_\ast
    \\
    & \simeq
    Maps(K, \underset{c}{\int} Maps(X(c),Y(c)))_\ast
    \\
    & =
    Maps(K,[\mathcal{C},Top^{\ast/}_{cg}](X,Y))_\ast
  \end{aligned}
$$

and

$$
  \begin{aligned}
    [\mathcal{C},Top^{\ast/}_{cg}](X, Maps(K,Y)_\ast)
    & =
    \underset{c}{\int}
      Maps(X(c), (Maps(K,Y)_\ast)(c))_\ast
    \\
    & \simeq
    \underset{c}{\int}
     Maps(X(c), Maps(K,Y(c))_\ast)_\ast
    \\
    & \simeq
    \underset{c}{\int} Maps(X(c) \wedge K, Y(c))_\ast
    \\
    & \simeq
    \underset{c}{\int} Maps(K, Maps(X(c),Y(c))_\ast)_\ast
    \\
    & \simeq
    Maps(K, \underset{c}{\int} Maps(X(c),Y(c))_\ast)_\ast
    \\
    & \simeq
    Maps(K, [\mathcal{C},Top^{\ast/}_{cg}](X,Y))_\ast
    \,.
  \end{aligned}
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
  d
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



## Basic topos theory

We have explained in Remark \ref{PresaheavesAsGeneralizedSpaces} how [[presheaves]] on a [[category]] $\mathcal{C}$ may be thought of as _generalized spaces probe-able by the objects of $\mathcal{C}$_, and that two consistency conditions on this interpretation are provided by the [[Yoneda lemma]] (Prop. \ref{YonedaLemma}) and the resulting [[Yoneda embedding]] (Prop. \ref{YonedaEmbedding}). Here we turn to a third consistency condition that one will want to impose:

If the [[objects]] of $\mathcal{C}$ are thought of as [[spaces]] of sorts, then there is typically a concept of _locality_ in these spaces, reflected by a notion of what it means to _[[cover]]_ a given space by ("smaller") spaces (a _[[coverage]]_, Def. \ref{Coverage} below).

But if a space $X \in \mathcal{C}$ is covered, say by two other spaces $U_1, U_2 \in \mathcal{C}$, via morphisms 

$$
  \array{
    U_1 && && U_2
    \\
    & {}_{\mathllap{i_1}}\searrow && \swarrow_{\mathrlap{i_2}}
    \\
    && X
  }
$$

then this must be reflected in the behaviour of the probes of any generalized space $\mathbf{Y}$ (in the sense of Remark \ref{PresaheavesAsGeneralizedSpaces}) by these test spaces:

For ease of discussion, suppose that there is a sense in which these two patches above [[intersection|intersect]] in $X$ to form a space $U_1 \cap_X U_2 \in \mathcal{C}$. Then locality of probes should imply that the ways of mapping $U_1$ and $U_2$ into $\mathbf{Y}$ such that these maps agree on the intersection $U_1 \cap_X U_2$, should be equivalent to the ways of mapping all of $X$ into $\mathbf{Y}$. 

$$
  \text{locality}
  \;:\;
  \left\{
    \array{
       \text{maps from}\,U_1\,\text{and}\,U_2\,\text{to}\,\mathbf{Y}
       \\
       \text{that coincide on}\,U_1 \cap_X U_2
    }
  \right\}
  \;\simeq\;
  \left\{
    \text{maps from}\,X\,\text{into}\,\mathbf{Y}
  \right\}
$$

One could call this the condition of _locality of probes of generalized spaces probeable by objects of $\mathcal{C}$_. But the established terminology is that this is the _[[sheaf|sheaf condition]] (eq:SheafCondition) on [[presheaves]] over $\mathcal{C}$_. Those presheaves which satisfy this condition are called the _[[sheaves]]_ (Def. \ref{Sheaf} below).

 
+-- {: .num_remark}
###### Remark
**Warning**

Most (if not all) introductions to [[sheaf theory]] insist on motivating the concept from the special case of sheaves on [[topological spaces]]. This is good motivation for what Grothendieck called "[[petit topos]]"-theory. The motivation above, instead, naturally leads to the "[[gros topos]]"-perspective, which is more useful for discussing the [[synthetic differential geometry|synthetic]] [[higher differential geometry|higher]] [[geometry of physics -- supergeometry|supergeometry]] of [[physics]]. In fact, this is the perspective of _[[functorial geometry]]_ that has been highlighted since [Grothendieck 65](functorial+geometry#Grothendieck65), but which has maybe remained underappreciated.

=--

+-- {: .num_defn #Coverage}
###### Definition
**([[coverage]] and [[site]])**

Let $\mathcal{C}$ be a [[small category]] (Def. \ref{SmallCategory}). Then a _[[coverage]]_ on $\mathcal{C}$ is

* for each [[object]] $X \in \mathcal{C}$ a [[set]] of [[indexed sets]] of [[morphisms]] into $X$

  $$
    \left\{ U_i \overset{\iota_i}{\to} X \right\}_{i \in I}
  $$

  called the _[[coverings]]_ of $X$,

such that

* for every [[covering]] $\left\{ U_i \overset{\iota_i}{\to} X \right\}_{i \in I}$ of $X$ and every [[morphism]] $Y \overset{f}{\longrightarrow} X$ there exists a _refining covering_ $\left\{ V_j \overset{\iota_j}{\to} Y \right\}_{j \in J}$ of $Y$, meaning that for each $j \in J$ there exists $i \in I$ and a morphism $V_j \overset{\iota_{j,i}}{\to} U_i$ such that

  \[
    \label{ConditionOnCoverage}
    f \circ \iota_j
     \;=\;
    \iota_i \circ \iota_{j,i}
    \phantom{AAAAAAA}
    \array{
      V_j
        &\overset{\iota_{j,i}}{\longrightarrow}&
      U_i
      \\
      {}^{\mathllap{ \iota_j }}\big\downarrow 
        && 
      \big\downarrow{}^{\mathrlap{ \iota_i}}
      \\
      Y &\underset{f}{\longrightarrow}& X
    }
  \] 

A [[small category]] $\mathcal{C}$ equipped with a [[coverage]] is called a _[[site]]_.

=--

+-- {: .num_example #DifferentiablyGoodOpenCoversOfSmoothManifolds}
###### Example
**(differentiably [[good open covers]] of [[smooth manifolds]])**

The [[category]] [[SmthMfd]] of [[smooth manifold]] (Example \ref{ExamplesOfConcreteCategories}) carries a [[coverage]] (Def. \ref{Coverage}), where for $X \in SmthMfd$ any [[smooth manifold]] of [[dimension]] $D \in \mathbb{N}$, its [[coverings]] are collections of [[smooth functions]] from the [[Cartesian space]] $\mathbb{R}^D$ to $X$ whose [[image]] is the inclusion of an [[open ball]].

Hence these are the usual _[[open covers]]_ of $X$, but with the extra condition that every pathch is [[diffeomorphism|diffeomorphic]] to a Cartesian space (hence to a smooth [[open ball]]).

One may further constrain this and ask that also all the non-empty finite [[intersections]] of these open balls are [[diffeomorphism|diffeomorphic]] to open balls. These are the _differentiably [[good open covers]]_.

To see that these coverings satisfy the condition (eq:ConditionOnCoverage): The plain pullback of an [[open cover]] along any continuous function is again an open cover, just not necessarily by patches diffeomorphic to open balls. But every open cover may be _refined_ by one that is (see at _[[good open cover]]_), and this is sufficient for (eq:ConditionOnCoverage). 

=--

Example \ref{DifferentiablyGoodOpenCoversOfSmoothManifolds} is further developed in the chapter _[[geometry of physics -- smooth homotopy types|on smooth homotopy types]]_.


+-- {: .num_prop #CompatibleElements}
###### Definition
**([[matching family]])**

Let $\mathcal{C}$ be a [[small category]] equipped with a [[coverage]], hence a [[site]] (Def. \ref{Coverage}) and consider a [[presheaf]] $\mathbf{Y} \in [\mathcal{C}^{op}, Set]$ (Example \ref{CategoryOfPresheaves}) over $\mathcal{C}$.

Given an [[object]] $X \in \mathcal{C}$ and a [[covering]] $\left\{ U_i \overset{\iota_i}{\to} X \right\}_{i \in I}$ of it (Def. \ref{Coverage}) we say that a _[[matching family]]_ (of probes of $\mathbf{Y}$) is a [[tuple]] $(\phi_i \in \mathbf{Y}(U_i))_{i \in I}$ such that for all $i,j \in I$ and [[pairs]] of [[morphisms]] $U_i \overset{\kappa_i}{\leftarrow} V \overset{\kappa_j}{\to} U_j$ satisfying

$$
  \iota_i \circ \kappa_i
  \;=\;
  \iota_j \circ \kappa_j
  \phantom{AAAAAAAA}
  \array{
    && V
    \\
    & {}^{\mathllap{\kappa_i}}\swarrow && \searrow^{\mathrlap{\kappa_j}}
    \\
    U_i && && U_j
    \\
    & {}_{\mathllap{\iota_i}}\searrow && \swarrow_{\mathrlap{\iota_j}}
    \\
    && X
  }
$$

we have 

$$
  \mathbf{Y}(\kappa_i)(\phi_i)
  \;=\;
  \mathbf{Y}(\kappa_j)(\phi_j)
  \,.
$$

We write

$$
  Match\big( 
    \{U_i\}_{i \in I}
    \,,\,
    \mathbf{Y}
  \big)
  \;\in\;
  Set
$$

for the set of [[matching families]] for the given presheaf and covering.

=--

+-- {: .num_example #MatchingFamiliesThatGlue}
###### Example
**([[matching families]] that glue)**

Let $\mathcal{C}$ be a [[small category]] equipped with a [[coverage]], hence a [[site]] (Def. \ref{Coverage}) and consider a [[presheaf]] $\mathbf{Y} \in [\mathcal{C}^{op}, Set]$ (Example \ref{CategoryOfPresheaves}) over $\mathcal{C}$.

Given an [[object]] $X \in \mathcal{C}$ and a [[covering]] $\left\{ U_i \overset{\iota_i}{\to} X \right\}_{i \in I}$ of it (Def. \ref{Coverage}), then every element

$$
  \phi \;\in\; \mathbf{Y}(X)
$$

induces a [[matching family]] (Def. \ref{CompatibleElements}) by

$$
  \big( \mathbf{Y}(\iota_i)(\phi)  \big)_{i \in I}
  \,.
$$

(That this indeed satisfies the matching condition follows immediately bu the [[functor|functoriality]] of $\mathbf{Y}$.)

This construction provides a [[function]] of the form

\[
  \label{SheafComparison}
  \mathbf{Y}(X)
    \longrightarrow
  Match\big( 
    \{U_i\}_{i \in I}
    \,,\,
    \mathbf{Y}
  \big)
\]

The matching families in the image of this function are hence those [[tuples]] of probes of $\mathbf{Y}$ by the patches $U_i$ of $X$ which _glue_ to a global probe out of $X$.

=--



+-- {: .num_defn #Sheaf}
###### Definition
**([[sheaf]])**

Let $\mathcal{C}$ be a [[small category]] equipped with a [[coverage]], hence a [[site]] (Def. \ref{Coverage}) and consider a [[presheaf]] $\mathbf{Y} \in [\mathcal{C}^{op}, Set]$ (Example \ref{CategoryOfPresheaves}) over $\mathcal{C}$.

The presheaf $\mathbf{Y}$ is called a _[[sheaf]]_ if for every [[object]] $X \in \mathcal{C}$ and every [[covering]] $\left\{ U_i \overset{\iota_i}{\to} X \right\}_{i \in I}$ of $X$ _all [[matching families]] glue uniquely_, hence if the comparison morphism (eq:SheafComparison) is a [[bijection]]

\[
  \label{SheafCondition}
  \mathbf{Y}(X)
    \overset{\simeq}{\longrightarrow}
  Match\big( 
    \{U_i\}_{i \in I}
    \,,\,
    \mathbf{Y}
  \big)
  \,.
\]

=--


### Simplicial presheaves

In order to understand the sheaf condition (eq:SheafCondition) better, it is useful to introduce _[[simplicial sets]]_.





(...)

