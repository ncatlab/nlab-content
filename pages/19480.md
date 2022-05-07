## Basic notions of Category theory
  {#BasicNotionsOfCategoryTheory}

We introduce here the basic notions of [[category theory]], along with examples and motivation from [[geometry]]:

1. _[Categories and functors](#CategoriesAndFunctors)_

1. _[Natural transformations and presheaves](#NaturalTransformationsAndPresheaves)_

1. _[Adjunctions](#Adjunctions)_

1. _[Equivalences](#Equivalences)_

1. _[Modalities](#Modalities)_



This constitutes what is sometimes called the _language of categories_. While we state and prove some basic facts here, notably the notorious _[[Yoneda lemma]]_ (Prop. \ref{YonedaLemma} below), what makes [[category theory]] be a _mathematical theory_ in the sense of a coherent collection of non-trivial [[theorems]] is all concerned with the topic of _[[universal constructions]]_, which may be formulated (only) in this language. This we turn to further [below](#UniversalConstructions).

$\,$

### Categories and Functors
 {#CategoriesAndFunctors}

The notion of a _[[category]]_ (Def. \ref{Categories} below) embodies the idea of [[structuralism]] applied to concepts in [[mathematics]]: it collects, on top of the [[set]] (or generally: [[class]]) of mathematical [[objects]] that belong to it, also all the _[[structure]]-preserving maps_ between them, hence the [[homomorphisms]] in the case of [[Bourbaki]]-style [[mathematical structures]].

The first achievement of the notion of a [[category]] is to abstract away from such manifestly _[[concrete categories]]_ (Examples \ref{ExamplesOfConcreteCategories}, \ref{StructuredSetsAndFaithfulFunctors} below) to more indirectly defined mathematical objects whose "structure" is only defined, after the fact, by which maps, now just called _[[morphisms]]_, there are between them.

This [[structuralism]]-principle bootstraps itself to life by considering [[morphisms]] between [[categories]] themselves to be those "maps" that respect their [[structuralism]], namely the connectivity and [[composition]] of the [[morphisms]] between their objects: These are the _[[functors]]_ (Def. \ref{Functors} below).

For the purpose of [[geometry]], a key class of examples of [[functors]] are the assignments of _[[algebras of functions]] to [[spaces]]_, this is Example \ref{SpacesViaAlgebrasOfFunctions} below.

$\,$


+-- {: .num_defn #Categories}
###### Definition
**([[category]])**

A _[[category]]_ $\mathcal{C}$ is

1. a [[class]] $Obj_{\mathcal{C}}$, called the _class of [[objects]]_;

1. for each [[pair]] $X,Y \in Obj_{\mathcal{C}}$ of [[objects]], a [[set]] $Hom_{\mathcal{C}}(X,Y)$, called the _[[set of morphisms]] from $X$ to $Y$_, or the _[[hom-set]]_, for short.

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

+-- {: .num_example #CategoryOfSets}
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

{#BasicExamplesOfConcreteCategories} Basic examples of [[concrete categories]] include the following:

| $\phantom{A}$[[concrete category]]$\phantom{A}$ | $\phantom{A}$[[objects]]$\phantom{A}$ | $\phantom{A}$[[morphisms]]$\phantom{A}$ |
|-----------------------|-------------|---------------|
| $\phantom{A}$[[Set]] | $\phantom{A}$[[sets]] | $\phantom{A}$[[functions]]  |
| $\phantom{A}$[[Top]]  | $\phantom{A}$[[topological spaces]]$\phantom{A}$ |  $\phantom{A}$[[continuous functions]]$\phantom{A}$ |
| $\phantom{A}$[[Mfd]]${}_{k}$  | $\phantom{A}$[[differentiable manifolds]]$\phantom{A}$ | $\phantom{A}$[[differentiable functions]]$\phantom{A}$ |
| $\phantom{A}$[[Vect]]  | $\phantom{A}$[[vector spaces]]$\phantom{A}$ | $\phantom{A}$[[linear functions]]$\phantom{A}$ |
| $\phantom{A}$[[Grp]]   | $\phantom{A}$[[groups]]$\phantom{A}$ | $\phantom{A}$[[group homomorphisms]]$\phantom{A}$ |
| $\phantom{A}$[[Alg]]   | $\phantom{A}$[[algebras]]$\phantom{A}$ | $\phantom{A}$[[algebra homomorphism]]$\phantom{A}$ |
{: style='margin:auto}


=--

This is the motivation for the terminology "categories", as the examples in Example \ref{ExamplesOfConcreteCategories} are literally _categories of mathematical structures_. But not all categories are "[[concrete category|concrete]]" in this way.

Some terminology:

+-- {: .num_defn #CommutingDiagram}
###### Definition
**([[commuting diagram]])**

Let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}), then a [[directed graph]] with [[edges]] labeled by [[morphisms]] of the category is called a _[[commuting diagram]]_ if for any two [[vertices]] any two ways of passing along edges from one to the other yields the same [[composition]] of the corresponding [[morphisms]].

For example, a _commuting triangle_ is

$$
  f = h \circ g
  \phantom{AAAAAA}
  \array{
    && X
    \\
    & {}^{\mathllap{ g }}\swarrow && \searrow^{ \mathrlap{ f } }
    \\
    Y && \underset{\phantom{A}h\phantom{A}}{\longrightarrow}  && Z
  }
$$

while a _[[commuting square]]_ is

$$
  g_1 \circ f_1
  \;=\;
  g_2 \circ f_2
  \phantom{AAAAAA}
  \array{
    X &\overset{\phantom{A}f_1\phantom{A}}{\longrightarrow}& Y_1
    \\
    {}^{ \mathllap{f_2} }\big\downarrow && \big\downarrow^{\mathrlap{ g_1 }}
    \\
    Y_2 &\underset{\phantom{A}g_2\phantom{A}}{\longrightarrow}&  Z
  }
$$

=--

+-- {: .num_defn #InitialObject}
###### Definition
**([[initial object]] and [[terminal object]])**

Let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}). Then

1. an [[object]] $\ast \in \mathcal{C}$ is called a _[[terminal object]]_ if for every other [[object]] $c \in \mathcal{C}$, there is a unique [[morphism]] from $c$ to $\ast$

   $$
     c \overset{\exists!}{\longrightarrow} \ast
   $$

   hence if the [[hom-set]] is a [[singleton]] $\ast \in Set$:

   $$
     Hom_{\mathcal{C}}(c,\ast) \;\simeq\; \ast
     \,.
   $$

1. an [[object]] $\emptyset \in \mathcal{C}$ is called an _[[initial object]]_ if for every other [[object]] $c \in \mathcal{C}$, there is a unique [[morphism]] from $\emptyset$ to $c$

   $$
     \emptyset \overset{\exists!}{\longrightarrow} c
   $$

   hence if the [[hom-set]] is a [[singleton]] $\ast \in Set$:

   $$
     Hom_{\mathcal{C}}(\emptyset,c) \;\simeq\; \ast
     \,.
   $$


=--

+-- {: .num_defn #SmallCategory}
###### Definition
**([[small category]])**

If a [[category]] $\mathcal{C}$ (Def. \ref{Categories}) happens to have as [[class]] $Obj_{\mathcal{C}}$ of [[objects]] an actual [[set]] (i.e. a [[small set]] instead of a [[proper class]]), then $\mathcal{C}$ is called a _[[small category]]_.

=--

As usual, there are some trivial examples, that are however usefully made explicit for the development of the theory:

+-- {: .num_example #InitialCategoryAndTerminalCategory}
###### Example
**([[initial category]] and [[terminal category]])**

1. The _[[terminal category]]_ $\ast$ is [[generalized the|the]] [[category]] (Def. \ref{Categories}) whose [[class]] of [[objects]] is [[generalized the|the]] [[singleton]] [[set]], and which has a single [[morphism]] on this object, necessarily the [[identity morphism]].

1. The _[[initial category]]_ or _[[empty category]]_ $\emptyset$ is the [[category]] (Def. \ref{Categories}) whose [[class]] of [[objects]] is the [[empty set]], and which, hence, has no morphism whatsoever.

Clearly, these are [[small categories]] (Def. \ref{SmallCategory}).

=--

+-- {: .num_example #PartiallyOrderedSetsAsSmallCategories}
###### Example
**([[preordered sets]] as [[thin categories]])**

Let $(S, \leq)$ be a [[preordered set]]. Then this induces a [[small category]] whose [[set]] of [[objects]] is $S$, and which has precisely one morphism $x \to y$ whenever $x \leq y$, and no such morphism otherwise:

\[
  \label{RelationsAsMorphismInPartiallyOrderedSet}
  x \overset{\exists !}{\to} y
  \phantom{AAA}
  \text{precisely if}
  \phantom{AAA}
  x \leq y
\]

Conversely, every [[small category]] with at most one morphism from any object to any other, called a _[[thin category]]_, induces on its set of objects the [[structure]] of a  [[partially ordered set]] via (eq:RelationsAsMorphismInPartiallyOrderedSet).

Here the [[axioms]] for [[preordered sets]] and for [[categories]] match as follows:

| |  $\phantom{A}$[[reflexive relation|reflexivity]]$\phantom{A}$ | $\phantom{A}$[[transitive relation|transitivity]]$\phantom{A}$ |
|----|-----|------|
| $\phantom{A}$[[partially ordered sets]]$\phantom{A}$ | $\phantom{A}$ $x \leq x$ $\phantom{A}$ | $\phantom{A}$ $(x \leq y \leq z) \Rightarrow (x \leq z)$ $\phantom{A}$ |
| $\phantom{A}$[[thin categories]]$\phantom{A}$ | $\phantom{A}$[[identity morphisms]]$\phantom{A}$ | $\phantom{A}$[[composition]]$\phantom{A}$ |
{: style='margin:auto}

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
  Y \overset{f^{-1}}{\longrightarrow} X \;\; \in Hom_{\mathcal{C}}(Y,X)
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

For this reason we will not have more to say about [[groupoids]] here, and instead relegate their discussion to the section on homotopy theory, further [below](#BasicNotionsOfHomotopyTheory).

=--


There is a range of constructions that provide new categories from given ones:

+-- {: .num_example #OppositeCategory}
###### Example
**([[opposite category]] and [[formal duality]])**

Let $\mathcal{C}$ be a [[category]]. Then its _[[opposite category]]_ $\mathcal{C}^{op}$ has the same [[objects]] as $\mathcal{C}$, but the direction of the [[morphisms]] is reversed. Accordingly, [[composition]] in the [[opposite category]] $\mathcal{C}^{op}$ is that in $\mathcal{C}$, but with the order of the arguments reversed:

* $Obj_{\mathcal{C}^{op}} \;\coloneqq\; Obj_{\mathcal{C}}$;

* $Hom_{\mathcal{C}^{op}}(X,Y) \;\coloneqq\; Hom_{\mathcal{C}}(Y,X)$.

Hence for every statementa about some [[category]] $\mathcal{C}$ there is a corresponding "dual" statement about its opposite category, which is "the same but with the direction of all morphisms reversed". This relation is known as _[[formal duality]].

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
     F_{X,Y} 
       \;\colon\;  
     Hom_{\mathcal{C}}(X,Y) 
       \longrightarrow 
     Hom_{\mathcal{D}}(F_{Obj}(X), F_{Obj}(Y))
   $$

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

   we have

   $$
      F_{X_1, X_3}(g \circ f ) \;=\;  F_{X_2, X_3}(g) \circ F_{X_1,X_2}(f)
      \,.
   $$

=--


+-- {: .num_example #CategoriesOfSmallCategories}
###### Example
**([[categories]] of [[small categories]] and of [[small groupoids]])**

It is clear that [[functors]] (Def. \ref{Functors}) have a [[composition]] operation given componentwise by the [[composition]] of their component functions. Accordingly, this composition is [[unitality|unital]] and [[associativity|associative]]. This means that there is

1. the [[category]] (Def. \ref{Categories}) _[[Cat]]_ whose [[objects]] are [[small categories]] (Def. \ref{SmallCategory}) and whose [[morphisms]] are [[functors]] (Def. \ref{Functors}) between these

1. the [[category]] (Def. \ref{Categories}) _[[Grpd]]_ whose [[objects]] are [[small groupoids|small]] [[groupoids]] (Def. \ref{Groupoid}) and whose [[morphisms]] are [[functors]] (Def. \ref{Functors}) between these.

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

is the [[functor]] (Def. \ref{Functors}) out of the [[product category]] (Def. \ref{ProductCategory}) of $\mathcal{C}$ with its [[opposite category]] to the [[category of sets]], which sends a [[pair]] $X,Y \in \mathcal{C}$ of [[objects]] to the [[hom-set]] $Hom_{\mathcal{C}}(X,Y)$ between them, and which sends a [[pair]] of [[morphisms]], with one of them into $X$ and the other out of $Y$, to the operation of [[composition]] with these morphisms:

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

+-- {: .num_defn #Monomorphism}
###### Definition
**([[monomorphism]] and [[epimorphism]])**

Let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}). Then a [[morphism]] $X \overset{f}{\to } Y$ in $\mathcal{C}$ is called

* a _[[monomorphism]]_ if for every [[object]] $Z \in \mathcal{C}$ the [[hom-functor]] (Example \ref{HomFunctor}) out of $Z$ takes $f$ to an [[injective function]] of [[hom-sets]]:

  $$
    Hom_{\mathcal{C}}(Z,f)
    \;\colon\;
    Hom_{\mathcal{C}}(Z,X)
     \overset{\phantom{AAA}}{\hookrightarrow}
    Hom_{\mathcal{C}}(Z,Y)
    \,;
  $$

* an _[[epimorphism]]_ if for every [[object]] $Z \in \mathcal{Z}$ the [[hom-functor]] (Example \ref{HomFunctor}) into $Z$ takes $f$ to an [[injective function]]:

  $$
    Hom_{\mathcal{C}}( f,Z )
    \;\colon\;
    Hom_{\mathcal{C}}(Y, Z)
      \overset{\phantom{AAA}}{\hookrightarrow}
    Hom_{\mathcal{C}}(X, Z)
    \,.
  $$

=--


+-- {: .num_defn #FullyFaithfulFunctor}
###### Definition
**([[full functor|full]], [[faithful functor|faithful]] and [[fully faithful functors]])**

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


+-- {: .num_example #FullSubcategoryOnClassOfObjects}
###### Example
**([[full subcategory]] on a [[subobject|sub]]-[[class]] of [[objects]])**

Let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}) and let $S \subset Obj_{\mathcal{C}}$ be a [[subobject|sub]]-[[class]] of its [[class]] of [[objects]]. The there is a [[category]] $\mathcal{C}_S$ whose class of [[objects]] is $S$, and whose [[morphisms]] are precisely the morphisms of $\mathcal{C}$, between these given objects:

$$
  Hom_{\mathcal{C}_S}(s_1, s_2)
  \;\coloneqq\;
  Hom_{\mathcal{C}}(s_1, s_2)
$$

with [[identity morphisms]] and [[composition]] defined as in $\mathcal{C}$. Then there is a [[fully faithful functor]] (Def. \ref{FullyFaithfulFunctor})

$$
  \array{
    \mathcal{C}_S &\overset{\phantom{AAAA}}{\hookrightarrow}& \mathcal{C}
  }
$$

which is the evident inclsuion on objects, and the [[identity function]] on all [[hom-sets]].

This is called the _[[full subcategory]] of $\mathcal{C}$ on the objects in $S$_.

Beware that not every [[fully faithful functor]] is, in components, exactly of this form, but, assuming the [[axiom of choice]], every fully faithful functor is so up to _[[equivalence of categories]]_ (Def. \ref{EquivalenceOfCategories}).


=--


The concept of _[[faithful functor]]_ from Def. \ref{FullyFaithfulFunctor} allows to make precise the idea of _[[concrete category]]_ from Example \ref{ExamplesOfConcreteCategories}:

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

In any given context of [[geometry]], there is typically a [[functor]] which sends any [[space]] of the given kind to its [[algebra of functions]], and which sends a map (i.e. [[homomorphism]]) between the given spaces to the algebra [[homomorphism]] given by precomposition with that map (a [[hom-functor]], Def. \ref{HomFunctor}). Schematically:

$$
  \array{
    \big\{
      \text{geometric spaces}
    \big\}
    &
    \overset{
      \text{algebra of functions}
    }{
      \longrightarrow
    }
    &
    \big\{
      \text{algebras}
    \big\}^{op}
    \\
    \\
    X_1 &\mapsto& FunctionsOn(X_1)
    \\
    {}^{\mathllap{f}}\big\downarrow && \big\uparrow^{ \phi \mapsto \phi \circ f }
    \\
    X_2 &\mapsto& FunctionsOn(X_2)
  }
$$

Since the precomposition operation reverses the direction of [[morphisms]], as shown, these are functors from the given [[category]] of [[spaces]] to the _[[opposite category|opposite]]_ (Example \ref{OppositeCategory}) of the relevant category of [[algebras]].

In broad generality, there is a [[duality]] ("[[Isbell duality]]") between [[geometry]]/[[spaces]] and [[algebra]]/[[algebras of functions]]) ("[[space and quantity]]", [Lawvere 86](space+and+quantity#Lawvere86)).

We now mention some concrete examples of this general pattern:

$\,$

**[[topological spaces]] and [[C*-algebras]]**

Consider

1. the [[category]] [[Top]]${}_{cpt}$ of [[compact topological space|compact]] [[topological spaces|topological]] [[Hausdorff spaces]] with [[continuous functions]] between them;

1. the category [[C*Alg]] of [[unital algebra|unital]] [[C*-algebras]] over the [[complex numbers]]

from Example \ref{ExamplesOfConcreteCategories}.

Then there is a [[functor]] (Def. \ref{Functors})

$$
  C(-)
  \;\colon\;
  Top_{H,cpt}
   \longrightarrow
  C^\ast Alg^{op}
$$

from the former to the [[opposite category]] of the latter (Example \ref{OppositeCategory}) which sends any [[compact topological space|compact]] [[topological space]] $X$ to its [[C*-algebra]] $C(X)$ of [[continuous functions]] $X \overset{\phi}{\to} \mathbb{C}$ with values in the [[complex numbers]], and which sends every [[continuous function]] between compact spaces to the [[C*-algebra]]-[[homomorphism]] that is given by [[precomposition]]:

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

Part of the statement of _[[Gelfand duality]]_ is that this is a [[fully faithful functor]], hence exhibiting a  [[full subcategory]]-inclusion (Def. \ref{FullyFaithfulFunctor}), namely that of [[commutative C*-algebras]]:

$$
  Top_{H,cpt}
   \overset{\phantom{AAA}}{\hookrightarrow}
  C^\ast Alg^{op}
  \,.
$$


$\,$

**[[affine schemes]] and [[commutative algebras]]**

The starting point of [[algebraic geometry]] is to consider _[[affine schemes]]_ as the [[formal duals]] (Example \ref{OppositeCategory}) of [[finitely generated object|finitely generated]] [[commutative algebras]] over some [[algebraically closed field|algebraically closed]] [[ground field]] $\mathbb{K}$:

\[
  \label{FormalDualsOfCommutativeRings}
  Aff_{\mathbb{K}}
   \;\;\coloneqq\;\;
  CAlg^{fin}_{\mathbb{K}}^{op}
  \,.
\]

Beware that the immediate identification (eq:FormalDualsOfCommutativeRings) is often obscured by the definition of [[affine schemes]] as [[locally ringed spaces]]. While the latter is much more complicated, at face value, in the end it yields an [[equivalence of categories|equivalent]] [[category]] (Def. \ref{EquivalenceOfCategories} below) to the simple [[formal dual|formal dualization]] (Example \ref{OppositeCategory}) in (eq:FormalDualsOfCommutativeRings), see [here](affine+scheme#AffineSchemesFullSubcategoryOfOppositeOfRings). Already in 1973 [[Alexander Grothendieck]] had urged to abandon, as a foundational concept, the more complicated definition in favor of the simpler one in (eq:FormalDualsOfCommutativeRings), see [Lawvere 03](functorial+geometry#Lawvere16Quote).


$\,$

**[[smooth manifolds]] and [[real numbers|real]] [[associative algebras]]**

Consider

1. the [[category]] [[SmthMfd]] of [[smooth manifolds]] with [[smooth functions]] between them;

1. the category [[Alg]]${}_{\mathbb{R}}$ of [[associative algebras]] over the [[real numbers]]

from Example \ref{ExamplesOfConcreteCategories}.

Then there is a [[functor]] (Def. \ref{Functors})

$$
  C^\infty(-)
  \;\colon\;
  SmthMfd
    \longrightarrow
  Alg_{\mathbb{R}}^{op}
$$

from the former to the [[opposite category]] of the latter (Def. \ref{OppositeCategory}), which sends any [[smooth manifold]] $X$ to its [[associative algebra]] $C^\infty(X)$ of [[continuous functions]] $X \overset{\phi}{\to} \mathbb{R}$ to the [[real numbers]], and which sends every [[smooth function]] between smooth manifolds to the [[algebra homomorphism]] that is given by [[precomposition]]:


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
   \overset{\phantom{AAAA}}{
     \hookrightarrow
   }
  Alg_{\mathbb{R}}^{op}
  \,.
$$

These two statements, expressing categories of [[spaces]] as [[full subcategories]] of [[opposite categories]] of categories of [[algebras]], are the starting point for many developments in [[geometry]], such as _[[algebraic geometry]]_, _[[supergeometry]]_, _[[noncommutative geometry]]_ and _[[noncommutative topology]]_.

$\,$

Since a [[fully faithful functor]]/[[full subcategory]]-embedding $\mathcal{C} \hookrightarrow \mathcal{D}$ exhibits the [[objects]] of $\mathcal{D}$ as a consistent generalization of the objects of $\mathcal{C}$, one may turn these examples around and _define_ more general kinds of [[spaces]] as _[[formal duality|formal duals]]_ (Example \ref{OppositeCategory}) to certain [[algebras]]:

$\,$

**[[infinitesimally thickened points]] and [[formal Cartesian spaces]]**

The [[category]] of _[[infinitesimally thickened points]]_ is, by definition, the [[full subcategory]] (Example \ref{FullSubcategoryOnClassOfObjects}) of the [[opposite category]] (Example \ref{OppositeCategory}) of that of [[commutative algebras]] (Example \ref{ExamplesOfConcreteCategories}) over the [[real numbers]]

$$
  \array{
    InfThckPoint
    &\overset{\phantom{AAAA}}{\hookrightarrow}&
    Alg_{\mathbb{R}}^{op}
    \\
    \mathbb{D} &\mapsto& C^\infty(\mathbb{D})
    \\
    &&   \coloneqq \mathbb{R} \oplus V
  }
$$

on those with a unique [[maximal ideal]] $V$ which is a finite-[[dimensional]] as an $\mathbb{R}$-[[vector space]] and a [[nilradical]]: for each $a \in V$ there exists $n \in \mathbb{N}$ such that $a^n = 0$.


The [[category]] of _[[formal Cartesian spaces]]_ is, by definition, the [[full subcategory]] (Example \ref{FullSubcategoryOnClassOfObjects}) of the [[opposite category]] (Example \ref{OppositeCategory}) of that of [[commutative algebras]] (Example \ref{ExamplesOfConcreteCategories}) over the [[real numbers]]

$$
  \array{
    FormalCartSp
    &\overset{\phantom{AAAA}}{\hookrightarrow}&
    Alg_{\mathbb{R}}^{op}
    \\
    \mathbb{R}^n \times \mathbb{D}
      &\mapsto&
    C^\infty(\mathbb{R}^n \times \mathbb{D})
    \\
    &&  \coloneqq C^\infty(\mathbb{R}^n) \otimes_{\mathbb{R}}(\mathbb{R} \oplus V)
  }
$$

on those which are [[tensor products of algebras]], of an [[algebra of functions|algebra of]] [[smooth functions]] on a [[Cartesian space]] $\mathbb{R}^n$, for some $n \in \mathbb{Z}$, and the algebra of functions on an [[infinitesimally thickened point]].

Notice that the [[formal Cartesian spaces]] $\mathbb{R}^{n\vert q}$ are fully _defined_ by this assignment.



$\,$

**[[super points]] and [[super Cartesian spaces]]**

The [[category]] of **[[super points]]** is _by definition_, the [[full subcategory]] (Example \ref{FullSubcategoryOnClassOfObjects})
of the [[opposite category]] (Example \ref{OppositeCategory}) of that of [[supercommutative algebras]] (Example \ref{ExamplesOfConcreteCategories}) over the [[real numbers]]

$$
  \array{
    SuperPoint
     &\overset{\phantom{AAAA}}{\hookrightarrow}&
    sCAlg_{\mathbb{R}}^{op}
    \\
    \mathbb{R}^{0\vert q}
    &\mapsto&
    \Lambda_q
  }
$$

on the [[Grassmann algebras]]:

$$
  \Lambda_q \;\coloneqq\; \mathbb{R}[ \theta_1, \cdots, \theta_q ]/( \theta_i \theta_j = - \theta_j \theta_i )
 \phantom{AAAAA}
  q \in \mathbb{N}
  \,.
$$

More generally, the [[category]] of **[[super Cartesian spaces]]** is _by definition_, the [[full subcategory]]
$$
  \array{
    SuperCartSp
    &\overset{\phantom{AAAA}}{\hookrightarrow}&
    sCAlg_{\mathbb{R}}^{op}
    \\
    \mathbb{R}^{n\vert q}
    &\mapsto&
    C^\infty(\mathbb{R}^n) \otimes_{\mathbb{R}} \Lambda_q
  }
$$

on the [[tensor product of algebras]], over $\mathbb{R}$ of the [[algebra of functions|algebra of]] [[smooth functions]] on a [[Cartesian space]], and a [[Grassmann algebra]], as above.

Notice that the [[super Cartesian spaces]] $\mathbb{R}^{n\vert q}$ are fully _defined_ by this assignment. We discuss this in more detail in the chapter [[geometry of physics -- supergeometry|on supergeometry]].

=--



$\,$

### Natural transformations and presheaves
 {#NaturalTransformationsAndPresheaves}

Given a system of ([[homomorphism|homo-]])[[morphisms]] ("transformations") in some [[category]] (Def. \ref{Categories})

$$
  F_X \overset{\phantom{A}\eta_X\phantom{A}}{\longrightarrow} G_X
$$

between [[objects]] that depend on some [[variable]] $X$, hence that are values of [[functors]] of $X$ (Def. \ref{Functors}), one says that this is _natural_, hence a _[[natural transformation]]_ (Def. \ref{NaturalTransformations} below) if it is compatible with ([[homomorphism|homo-]])[[morphisms]] of the variable itself.

These [[natural transformations]] are the evident [[homomorphisms]] between [[functors]]

$$
  F \overset{\phantom{A}\eta\phantom{A}}{\longrightarrow} G
  \,,
$$

and hence there is a _[[category of functors]]_ between any two [[categories]] (Example \ref{FunctorCategory} below).

A key class of such [[functor categories]] are those between an [[opposite category]] $\mathcal{C}^{op}$ and the base [[category of sets]], these are also called _[[categories of presheaves]]_ (Example \ref{CategoryOfPresheaves} below). It makes good sense (Remark \ref{PresaheavesAsGeneralizedSpaces} below) to think of these as categories of "generalized objects of $\mathcal{C}$", a perspective which is made precise by the statement of the _[[Yoneda lemma]]_ (Prop. \ref{YonedaLemma} below) and the resulting _[[Yoneda embedding]]_ (Prop. \ref{YonedaEmbedding} below). This innocent-looking lemma is the heart that makes [[category theory]] tick.

$\,$

+-- {: .num_defn #NaturalTransformations}
###### Definition
**([[natural transformation]] and [[natural isomorphism]])**

Given two [[categories]] $\mathcal{C}$ and $\mathcal{D}$ (Def. \ref{Categories}) and given two [[functors]] $F$ and $G$ from $\mathcal{C}$ to $\mathcal{D}$ (Def. \ref{Functors}), then a _[[natural transformation]]_ from $F$ to $G$

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

* for each [[morphism]] $X \overset{f}{\longrightarrow} Y$ we have a [[commuting square]] (Def. \ref{CommutingDiagram}) of the form

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

  (sometimes called the _naturality square_ of the natural transformation).

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

two [[natural transformations]] as shown, their _[[composition]]_ is the natural transformation

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
  \phantom{AAAAA}
  \array{
     F(X) &\overset{\eta_X}{\longrightarrow}& G(X)
      &\overset{\rho_X}{\longrightarrow}& H(X)
     \\
     {}^{\mathllap{F(f)}}\downarrow
       &&
     \downarrow^{\mathrlap{G(f)}}
       &&
     \downarrow^{\mathrlap{H(f)}}
     \\
     F(Y) &\underset{\eta_Y}{\longrightarrow}& G(Y)
       &\underset{\rho_Y}{\longrightarrow}& H(Y)
  }
\]

=--


+-- {: .num_example #ReductionOnFormalCartesianSpace}
###### Example
**([[reduction modality|reduction]] of [[formal Cartesian spaces]])**

On the [[category]] [[FormalCartSp]] of [[formal Cartesian spaces]] Example \ref{SpacesViaAlgebrasOfFunctions}, consider the [[endofunctor]]

$$
  \array{
    FormalCartSp
      &\overset{ \phantom{AA}\Re \phantom{AA} }{\longrightarrow}&
    FormalCartSp
    \\
    \mathbb{R}^n \times \mathbb{D}
    &\mapsto&
    \mathbb{R}^n
  }
$$

which sends each [[formal Cartesian space]] to the underlying ordinary [[Cartesian space]], forgetting the [[infinitesimally thickened point]]-factor. Moreover, on [[morphisms]] this functor is defined via the [[retraction]]

$$
  \array{
    id \colon
    &
    \mathbb{R}^n
    &\overset{i}{\longrightarrow}&
    \mathbb{R}^n \times \mathbb{D}
    &\overset{r}{\longrightarrow}&
    \mathbb{R}^n
    \\
    &
    C^\infty(\mathbb{R}^n)
    &\underoverset{\text{quotient projection}}{i^\ast}{\longleftarrow}&
    C^\infty(\mathbb{R}^n) \otimes_{\mathbb{R}} (R \oplus V)
    &\underoverset{f \mapsto f \otimes 1}{r^\ast}{\longleftarrow}&
    C^\infty(\mathbb{R}^n)
  }
$$

as

$$
  \array{
     C^\infty(\mathbb{R}^n \times \mathbb{D})
       &\phantom{AAA}&&
     C^\infty(\mathbb{R}^n)
       &\overset{i^\ast}{\longleftarrow}&
     C^\infty( \mathbb{R}^n \times \mathbb{D} )
     \\
     {}^{\mathllap{ f^\ast }}\big\uparrow
       && &
     {}^{ \mathllap{\Re( f^\ast ) \coloneqq i^\ast \circ f^\ast \circ r^\ast } }\big\uparrow
       &&
     \big\uparrow^{ \mathrlap{ f^\ast } }
     \\
     C^\infty(\mathbb{R}^{n'} \times {\mathbb{D}}')
       &&&
     C^\infty(\mathbb{R}^{n'})
       &\overset{r^\ast}{\longrightarrow}&
     C^\infty( \mathbb{R}^{n'}  \times {\mathbb{D}}')
  }
$$

This is indeed functorial due to the fact that any algebra [[homomorphism]] $f^\ast$ needs to send nilpotent elements to nilpotent elements, so that the following identity holds:

\[
  \label{ProjectingOutNilpotentsLater}
  i^\ast \circ f^\ast
  \;=\;
  i^\ast \circ f^\ast \circ r^\ast \circ i^\ast 
  \,.
\]

Then there is a [[natural transformation]] (Def. \ref{NaturalTransformations}) from this functor to the [[identity functor]]

$$
  \Re
    \overset{ \phantom{A} \eta^{\Re} \phantom{A} }{\longrightarrow}
  Id
$$

whose components inject the underlying Cartesian space along the unit point inclusion of the [[infinitesimally thickened point]]:

$$
  \array{
    \Re\left( \mathbb{R}^n \times \mathbb{D} \right)
      \coloneqq
    &
    \mathbb{R}^n
    &\overset{ \phantom{A} \eta^\Re_{\mathbb{R}^n \times \mathbb{D}} }{\longrightarrow}&
    \mathbb{R}^n \times \mathbb{D}
    \\
    &
    C^\infty(\mathbb{R}^n)
    &\overset{i^\ast}{\longleftarrow}&
    C^\infty(\mathbb{R}^n \times \mathbb{D})
    \\
    &
    {}^{ \mathllap{ i^\ast \circ f^\ast \circ r^\ast } }\big\uparrow && \big\uparrow^{\mathrlap{ f^\ast }}
    \\
    &
    C^\infty(\mathbb{R}^{n'})
    &\overset{i^\ast}{\longleftarrow}&
    C^\infty(\mathbb{R}^{n'} \times \mathbb{D}')
  }
$$

The commutativity of this naturality square is again the identity (eq:ProjectingOutNilpotentsLater).

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

hence out of the [[opposite category]] of $\mathcal{C}$ (Def. \ref{OppositeCategory}), into the [[category of sets]] (Example \ref{CategoryOfSets}) is also called a _[[presheaf]]_ (for reasons discussed below) _on $\mathcal{C}$_ or _over $\mathcal{C}$_.

The corresponding [[functor category]] (Example \ref{FunctorCategory})

$$
  PSh(\mathcal{C})
  \;\coloneqq\; [\mathcal{C}^{op}, Set]
$$

is hence called the _[[category of presheaves]]_ over $\mathcal{C}$.

=--


+-- {: .num_example #RepresentablePresheaves}
###### Example
**([[representable presheaves]])**

Given a [[category]] $\mathcal{C}$ (Def. \ref{Categories}), the [[hom-functor]] (Example \ref{HomFunctor}) induces the following [[functor]] (Def. \ref{Functors}) from $\mathcal{C}$ to its [[category of presheaves]] (Def. \ref{CategoryOfPresheaves}):

\[
  \label{YonedaFunctor}
  \array{
    y & \colon &
    \mathcal{C}
      &\longrightarrow&
    [\mathcal{C}^{op}, Set]
    \\
    \\
    && && && c_1 &\overset{g}{\longrightarrow}& c_2
    \\
    &&
    X
    &\mapsto&
    Hom_{\mathcal{C}}(-,X)
     &\phantom{AA}\colon\phantom{AA}&
    Hom_{\mathcal{C}}(c_1,X)
      &\overset{Hom_{\mathcal{C}}( g, X ) }{\longleftarrow}&
    Hom_{\mathcal{C}}(c_2, X)
    \\
    &&
    {}^{\mathllap{ f }}\big\downarrow
    &&
    \big\downarrow^{ \mathrlap{ Hom_{\mathcal{C}}(-,f) } }
    &&
    \big\downarrow^{ \mathrlap{ Hom_{\mathcal{C}}( c_1, f )  } }
    &&
    \big\downarrow^{ \mathrlap{ Hom_{\mathcal{C}}(c_2,f) } }
    \\
    &&
    Y &\mapsto&
    Hom_{\mathcal{C}}(-,Y)
      &\phantom{AA}\colon\phantom{AA}&
    Hom_{\mathcal{C}}(c_1,Y)
      &\overset{Hom_{\mathcal{C}}( g, Y ) }{\longleftarrow}&
    Hom_{\mathcal{C}}(c_2, Y)
  }
\]

The [[presheaves]] $y(X) \coloneqq Hom_{\mathcal{C}}(-,X)$ in the [[image]] of this functor are called the _[[representable presheaves]]_ and $X \in Obj_{\mathcal{C}}$ is called their [[representing object]].

The functor (eq:YonedaFunctor) is also called the _[[Yoneda embedding]]_, due to Prop. \ref{YonedaEmbedding} below.

=--

+-- {: .num_remark #PresaheavesAsGeneralizedSpaces}
###### Remark
**([[presheaves]] as [[generalized spaces]])**

If a given [[category]] $\mathcal{C}$ (Def. \ref{Categories}) is thought of as a category of _[[spaces]]_ of sorts, as those in Example \ref{SpacesViaAlgebrasOfFunctions}, then it will be most useful to think of the corresponding [[category of presheaves]] $[\mathcal{C}^{op}, Set]$ (Def. \ref{CategoryOfPresheaves}) as a category of _[[generalized spaces]] probe-able by_ the test spaces in $\mathcal{C}$ ([Lawvere 86, p. 17](space+and+quantity#Lawvere86)).

Namely, imagine a [[generalized space]] $\mathbf{X}$ which is at least probe-able by spaces in $\mathcal{C}$. This should mean that for each [[object]] $c \in \mathcal{C}$ there is some [[set]] of geometric maps "$c \to \mathbf{X}$". Here the quotation marks are to warn us that, _at this point_, $\mathbf{X}$ is not defined yet; and even if it were, it is not expected to be an object of $\mathcal{C}$, so that, at this point, an actual morphism from $c$ to $\mathbf{X}$ is not definable. But we may anyway consider some _abstract set_


\[
  \label{WouldBeMapsIntoGeneralizedSpace}
  \mathbf{X}(c)  \; \text{"=}  Hom(c,\mathbf{X})"
\]

whose elements we do want to think of maps (homomorphisms of spaces) from $c$ to $\mathbf{X}$.

That this is indeed consistent, in that we may actually remove the quotation remarks on the right of (eq:WouldBeMapsIntoGeneralizedSpace), is the statement of the _[[Yoneda lemma]]_, which we discuss as Prop. \ref{YonedaLemma} below.


A minimum consistency condition for this to make sense (we will consider further conditions later on when we discuss _[[sheaves]]_) is that we may consistently pre-compose the would-be maps from $c$ to $\mathbf{X}$ with actual morphisms $d \overset{f}{\to} c$ in $\mathcal{C}$. This means that for every such morphism there should be a function between these sets of would-be maps

$$
  \array{
     c && \mathbf{X}(d)
     \\
     {}^{\mathllap{ f }}\big\downarrow
       &&
     \big\uparrow{}^{\mathrlap{ \mathbf{X}(f) \, \text{"=}(-)\circ f\text{"}}}
     \\
     d && \mathbf{X}(c)
  }
$$

which respects composition and identity morphisms. But in summary, this says that what we have defined thereby is actually a _[[presheaf]]_ on $\mathcal{C}$ (Def. \ref{CategoryOfPresheaves}), namely a functor

$$
  \mathbf{X} \;\colon\; \mathcal{C}^{op} \longrightarrow Set
  \,.
$$

For consistency of regarding this presheaf as a _presheaf of sets of plots of a generalized space_, it ought to be true that every "ordinary space", hence every [[object]] $X \in \mathcal{C}$, is also an example of a "generalized space probe-able by" object of $\mathcal{C}$, since, after all, these are the spaces which may manifestly be probed by objects $c \in \mathcal{C}$, in that morphisms $c \to X$ are already defined.

Hence the incarnation of $X \in \mathcal{C}$ as a generalized space probe-able by objects of $\mathcal{C}$ should be the presheaf $Hom_{\mathcal{C}}(-,X)$, hence the [[representable presheaf|presheaf represented]] by $X$ (Example \ref{RepresentablePresheaves}), via the Yoneda functor (eq:YonedaFunctor).

At this point, however, a serious consistency condition arises: The "ordinary spaces" now exist as objects of two different categories: on the one hand there is the original $X \in \mathcal{C}$, on the other hand there is its Yoneda image $y(X) \in [\mathcal{C}^{op}, Set]$ in the category of generalized spaces. Hence we need to know that these two perspectives are compatible, notably that maps $X \to Y$ between ordinary spaces are the same whether viewed in $\mathcal{C}$ or in the more general context of $[\mathcal{C}^{op}, Set]$.

That this, too, holds true, is the statement of the _[[Yoneda embedding]]_, which we discuss as Prop. \ref{YonedaEmbedding} below.

Eventually one will want to impose one more consistency condition, namely that plots are determined by their _local behaviour_. This is the _[[sheaf|sheaf condition]]_ (Def. \ref{Sheaf} below) and is what leads over from [[category theory]]  to [[topos theory]] [below](#BasicNotionsOfToposTheory).

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

Now the condition to be satisfied by $\eta$ is that it makes its [[naturality squares]] (eq:Naturality) commute (Def. \ref{CommutingDiagram}). This includes those of the form

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

As the diagram chase of elements on the right shows, this commutativity (Def. \ref{CommutingDiagram}) fixes $\eta_Y(f)$ for all $Y \in \mathcal{C}$ and all $f \in Hom_{\mathcal{C}}(Y,X)$ uniquely in terms of the element $\eta_{X}(id_X)$.

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

The assignment (eq:YonedaFunctor) of [[representable presheaves|represented presheaves]] (Example \ref{RepresentablePresheaves})  is a [[fully faithful functor]] (Def. \ref{FullyFaithfulFunctor}), hence exhibits a [[full subcategory]] inclusion

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

As a direct corollary we obtain the following alternative characterization of [[isomorphisms]], to be compared with the definition of [[epimorphisms]]/[[monomorphisms]] in Def. \ref{Monomorphism}:

+-- {: .num_example #YonedaCharacterizationOfIsomorphism}
###### Example
**([[isomorphism]] via [[bijection]] of [[hom-sets]])**

Let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}), let $X, Y \in Obj_{X}$ be a [[pair]] of [[objects]], and let $X \overset{f}{\to} Y \;\; \in Hom_{\mathcal{C}}(X,Y)$ be a [[morphism]] between them. Then the following are equivalent:

1. $X \overset{f}{\to} Y$ is an [[isomorphism]] (Def. \ref{Isomorphism}),

1. the [[hom-functors]] into and out of $f$ take values in [[bijections]] of [[hom-sets]]: i.e. for all [[objects]] $A \in Obj_{\mathcal{C}}$, we have

   $$
     Hom_{\mathcal{C}}(A,f)
     \;\colon\;
     Hom_{\mathcal{C}}(A,X) 
       \overset{\simeq}{\longrightarrow}
     Hom_{\mathcal{C}}(A,Y)
   $$

   and

   $$
     Hom_{\mathcal{C}}(f,A)
     \;\colon\;
     Hom_{\mathcal{C}}(Y,A) 
       \overset{\simeq}{\longrightarrow}
     Hom_{\mathcal{C}}(X,A)
   $$

=--


$\,$


### Adjunctions
  {#Adjunctions}

The concepts of [[categories]], [[functors]] and [[natural transformations]] constiture the "language of categories". This language now allows to formulate the concept of _[[adjoint functors]]_ (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) and more generally that of _[[adjunctions]]_ (Def. \ref{AdjunctionInA2Category} below. This is concept that [[category theory]], as a theory, is all about.

Part of the data involved in an [[adjunction]] is its _[[adjunction unit]]_ and _[[adjunction counit]]_ (Def. \ref{AdjunctionUnitFromHomIsomorphism} below) and depending on their behaviour special cases of [[adjunctions]] are identified (Prop. \ref{FullyFaithfulAndInvertibleAdjoints} below), which we discuss in detail in following sections:

|   |    |    |
|---|----|----|
| $\phantom{A}$**[[adjunction]]**$\phantom{A}$ <br/> $\phantom{A}$Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}, Def. \ref{AdjunctionInA2Category}$\phantom{A}$  |  |  $\phantom{A}$[[adjunction unit|unit]] is [[isomorphism|iso]]:$\phantom{A}$  | 
|  |  | $\phantom{A}$[[coreflective subcategory|coreflection]]$\phantom{A}$ <br/> $\phantom{A}$Def. \ref{ReflectiveSubcategory}$\phantom{A}$ | 
| $\phantom{A}$[[adjunction counit|counit]] is [[isomorphism|iso]]:$\phantom{A}$ | $\phantom{A}$[[reflective subcategory|reflection]]$\phantom{A}$ <br/> $\phantom{A}$Def. \ref{ReflectiveSubcategory} | $\phantom{A}$[[adjoint equivalence of categories|adjoint equivalence]]$\phantom{A}$ <br/> $\phantom{A}$Def. \ref{AdjointEquivalenceOfCategories}$\phantom{A}$  |  
{: style='margin:auto}

We now discuss four equivalent definitions of [[adjoint functors]]:

1. via hom-isomorphism (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets} below);

1. via [[adjunction unit]] and -[[adjunction counit|counit]] satisfying [[triangle identities]] (Prop. \ref{AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat});

1. via [[representing objects]] (Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject});

1. via [[universal morphisms]] (Prop. \ref{CollectionOfUniversalArrowsEquivalentToAdjointFunctor} below).

Then we discuss some key properties:

1. uniqueness of adjoints (Prop. \ref{UniquenessOfAdjoints} below),

1. epi/mono/iso-characterization of adjunction (co-)units (Prop. \ref{FullyFaithfulAndInvertibleAdjoints} below).


$\,$


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

[[commuting square|commutes]] (Def. \ref{CommutingDiagram}), where the vertical morphisms are given by the [[hom-functor]] (Example \ref{HomFunctor}).

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
**([[adjunction unit]] and [[adjunction counit|counit]])

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

+-- {: .num_remark #AdjointTriples}
###### Remark
**([[adjoint triples]])**

It happens that there are subsequence [[adjoint functors]]:

If two functors are [[adjoint functors|adjoint]] to each other as in Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}, we also say that we have an _[[adjoint pair]]_:

$$
  L \;\dashv\; R
  \,.
$$

If one of these has yet another adjoint in the other direction, we speak of an _[[adjoint triple]]_

\[
  \label{AdjointTriple}
  L \;\dashv\; C \;\dashv\; R
  \,.
\]

Below in Example \ref{AdjunctionofAdjunction} we identify adjoint triples as _adjunctions of adjunctions_.

Similarly there are [[adjoint quadruples]], etc.

Notice that in the case of an [[adjoint triple]] (eq:AdjointTriple), the [[adjunction unit]] of $C \dashv R$ and the [[adjunction counit]] of $L \dashv R$ (Def. \ref{AdjunctionUnitFromHomIsomorphism}) provide, for each object $X$ in the [[domain]] of $C$, a [[diagram]]

\[
  \label{OppositeExtremesAdjointTriple}
  L(C(X))
   \overset{ \phantom{AA} \epsilon_X \phantom{AA} }{\longrightarrow}
  X
    \overset{ \phantom{AA} \eta_X \phantom{AA} }{\longrightarrow}
  R(C(X))
\]

which is usefully thought of as exhibiting the nature of $X$ as being in between two _opposite extreme aspects_ $L(C(X))$ and $R(C(X))$ of $X$. This is illustrated by the following examples, and formalized by the concept of _[[modalities]]_ that we turn to in Def. \ref{ModalOperator} below.

=--



+-- {: .num_example #FloorAndCeilingAsAdjointFunctors}
###### Example
**([[floor]] and [[ceiling]] as [[adjoint functors]])**

Consider the canonical inclusion

$$
  \mathbb{Z}_{\leq}
    \overset{\phantom{AA}\iota \phantom{AA}}{\hookrightarrow}
  \mathbb{R}_{\leq}
$$

of the [[integers]] into the [[real numbers]], both regarded as [[preorders]] in the standard way ("lower or equal"). Regarded as [[full subcategory]]-inclusion (Def. \ref{FullyFaithfulFunctor}) of the corresponding [[thin categories]], via Example \ref{PartiallyOrderedSetsAsSmallCategories}, this inclusion functor has both a left and right [[adjoint functor]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}):

* the [[left adjoint]] to $\iota$ is the [[ceiling function]];

* the [[right adjoint]] to $\iota$ is the [[floor function]];

forming an [[adjoint triple]] (Def. \ref{AdjointTriples})

\[
  \label{FloorCeilingAdjointTriple}
  \lceil(-)\rceil \;\;\dashv\;\; \iota \;\;\dashv\;\; \lfloor (-) \rfloor
  \,.
\]

The [[adjunction unit]] and [[adjunction counit]] express that each real number is in between its "opposite extreme integer aspects" (eq:OppositeExtremesAdjointTriple) given by floor and ceiling

$$
  \iota \lfloor x \rfloor \;\overset{\epsilon_X}{\leq}\; x \;\overset{\eta_x}{\leq}\; \iota \lceil x \rceil
  \,.
$$

=--

+-- {: .proof}
###### Proof

First of all, observe that we indeed have [[functors]] (Def. \ref{Functors})

$$
  \lfloor(-)\rfloor \;,\;
  \lceil(-)\rceil
  \;\;\colon\;
  \mathbb{R}
    \longrightarrow
  \mathbb{Z}
$$

since floor and ceiling preserve the ordering relation.

Now in view of the identification of [[preorders]] with [[thin categories]] in Example \ref{PartiallyOrderedSetsAsSmallCategories}, the hom-isomorphism (eq:HomIsomorphismForAdjointFunctors) defining [[adjoint functors]] of the form $\iota \dashv \lfloor(-)\rfloor$ says for all $n \in \mathbb{Z}$ and $x \in \mathbb{R}$, that we have

$$
  \underset{ \in \mathbb{Z}}{\underbrace{n \leq \lfloor x \rfloor}}
  \;\Leftrightarrow\;
  \underset{ \in \mathbb{R}}{\underbrace{n \leq x }}
  \,.
$$

This is clearly already the defining condition on the [[floor]] function $\lfloor x \rfloor$.

Similarly, the  hom-isomorphism defining [[adjoint functors]] of the form $\lceil(-)\rceil \dashv \iota$ says that for all $n \in \mathbb{Z}$ and $x \in \mathbb{R}$, we have

$$
  \underset{ \in \mathbb{Z}}{\underbrace{\lceil x \rceil \leq n}}
  \;\Leftrightarrow\;
  \underset{ \in \mathbb{R}}{\underbrace{x \leq n }}
  \,.
$$

This is evidently already the defining condition on the [[floor]] function $\lfloor x \rfloor$.


Notice that in both cases the condition of a _[[natural isomorphism]]_ in both variables, as required for an [[adjunction]], is automatically satisfied: For let $x \leq x'$ and $n' \leq n$, then naturality as in (eq:NaturalitySquareForAdjointnessOfFunctors) means, again in view of the identifications in Example \ref{PartiallyOrderedSetsAsSmallCategories}, that

$$
  \array{
    (n \leq \lfloor x \rfloor) &\Leftrightarrow& (n \leq x)
    \\
    \Downarrow && \Downarrow
    \\
    (n' \leq \lfloor x' \rfloor) &\Leftrightarrow& (n' \leq x')
    \\
    \\
    \in \mathbb{Z} && \in \mathbb{R}
  }
$$

Here the logical implications are equivalently functions between [[sets]] that are either [[empty set|empty]] or [[singletons]]. But Functions between such sets are unique, when they exist.

=--

+-- {: .num_example #DiscreteTopologicalSpaces}
###### Example
**([[discrete topological space|discrete]] and [[codiscrete topological spaces]])**

Consider the "[[forgetful functor]]" $Top \overset{U}{\longrightarrow} Set$ from the [[category]] [[Top]] of [[topological spaces]] (Example \ref{ExamplesOfConcreteCategories}) to the [[category of sets]] (Def. \ref{CategoryOfSets}) which sends every [[topological space]] to its underlying [[set]].

This has

* a [[left adjoint]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) $Disc$ which equips a set with its [[discrete topology]],

* a [[right adjoint]] $coDisc$ which equips a set with the [[codiscrete topology]].

These hence form an [[adjoint triple]] (Remark \ref{AdjointTriples})

$$
  Disc
  \;\dashv\;
  U
  \;\dashv\;
  coDisc
  \,.
$$

Hence the [[adjunction unit]] of $Disc \dashv U$ and the [[adjunction counit]] of $U \dashv coDisc$ exhibit every [[topological space|topology]] on a given set as "in between the opposite extremes" (eq:OppositeExtremesAdjointTriple) of the discrete and the co-discrete

$$
  Disc(U(X))
    \overset{\epsilon}{\longrightarrow}
  X
    \overset{\eta}{\longrightarrow}
  coDisc(U(X))
  \,.
$$

=--





\begin{lemma}\label{ReExpressingMiddleFunctorInAdjointTriple}
**(pre/post-[[composition]] with ([[adjunction counit|co-]])[[adjunction unit|unit]] followed by [[adjunct]] is [[adjoint functor]])**
\linebreak
If a [[functor]] $C$ is the [[right adjoint]]

$$
  L \dashv C
  \;\;\colon\;\;
  \mathcal{C}
    \array{
      \overset{\phantom{AA} L \phantom{AA} }{\longleftarrow}
      \\
      \underset{\phantom{AA} C \phantom{AA} }{\longrightarrow}
    }
  \mathcal{D}
$$

in a [[adjoint pair|pair]] of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}), then its application to any [[morphism]] $X \overset{f}{\to} Y \;\;\in \mathcal{C}$ is equal to the joint operation of
[[composition|pre-composition]] with the $(L \dashv C)$-[[adjunction counit]] $\epsilon^\flat_{X}$ (Def. \ref{AdjunctionUnitFromHomIsomorphism}), followed by passing to the  $(L \dashv C)$-[[adjunct]]:


$$
  C_{X, Y}
  \;=\;
  \widetilde{ (-) \circ \epsilon^\flat_{X} }
  \,.
$$


Dually, if $C$ is a [[left adjoint]]

$$
  C \dashv R
  \;\;\colon\;\;
  \mathcal{C}
    \array{
      \overset{\phantom{AA} C \phantom{AA} }{\longrightarrow}
      \\
      \underset{\phantom{AA} R \phantom{AA} }{\longleftarrow}
    }
  \mathcal{D}
$$

then its action on any [[morphism]] $X \overset{f}{\to} Y \;\;\in \mathcal{C}$ equals the joint operation of [[composition|post-composition]] with the $(C \dashv R)$-[[adjunction unit]] $\eta^{ \sharp }_{Y}$ (Def. \ref{AdjunctionUnitFromHomIsomorphism}), followed by passing to the $(C \dashv R)$-[[adjunct]]:

$$
  \widetilde{\eta^\sharp_{Y} \circ (-)}
  \;=\;
  C_{X, Y}  
  \,.
$$


In particular, if $C$ is the middle functor in an [[adjoint triple]] (Remark \ref{AdjointTriples})

$$
  L \dashv C \dashv R
  \;\;\colon\;\;
  \mathcal{C}
  \;\;
    \array{
      \overset{\phantom{AA} L \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AAA} C \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} R \phantom{AA} }{\longleftarrow}
    }
  \;\;
  \mathcal{D}
$$

then these two operations coincide:

\[
  \label{PostcompositionWithEtaAsGamma}
  \widetilde{\eta^\sharp_{Y} \circ (-)}
  \;=\;
  C_{X, Y}
  \;=\;
  \widetilde{ (-) \circ \epsilon^\flat_{X} }
  \,.
\]

\end{lemma}

\begin{proof}
For the first equality, consider the following [[naturality square]] (eq:Naturality) for the adjunction hom-isomorphism (eq:HomIsomorphismForAdjointFunctors):

$$
  \array{
    Hom_{\mathcal{D}}\big( C (X) ,\, C (X) \big)
    &\overset{\widetilde { (-) }}{\longrightarrow}&
    Hom_{\mathcal{C}}\big( L C (X)  ,\, X \big)
    \\
    {}^{\mathllap{ Hom_{\mathcal{D}}\big( C (id_X) ,\, C(f) \big)  }}
    \big\downarrow
    &&
    \big\downarrow {}^{ \mathrlap{ Hom_{X}\big( L C (id_X) ,\, f \big)
} }
    \\
    Hom_{\mathcal{D}}\big( C (X) ,\, C (Y) \big)
    &\overset{ \widetilde{ (-) } }{\longleftarrow}&
    Hom_{\mathcal{C}    }( L C (X) ,\, Y )
  }
  \phantom{AAAAA}
  \array{
     \{ C X \overset{id_{C X}}{\to} C X \}
     &\longrightarrow&
     \{ L C X \overset{\epsilon^{\flat}_X}{\to} X \}
     \\
     \big\downarrow
       &&
     \big\downarrow
     \\
     \{ C X \overset{C(f)}{\to} C(Y) \}
     &\longleftarrow& \{ L C X \overset{f\circ \epsilon^\flat_{X}  }{\longrightarrow} Y\}
  }
$$




Chasing the [[identity morphism]] $id_{C Y}$ through this diagram, yields the claimed equality, as shown on the right. Here we use that the left [[adjunct]] of the [[identity morphism]] is the [[adjunction counit]], as shown.

The second equality is [[formal duality|fomally dual]]:

$$
  \array{
    Hom_{\mathcal{D}}
    \big( C Y ,\, C Y \big)
    &\overset{\widetilde {(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}
    \big( Y ,\, R C Y \big)
    \\
    {}^{\mathllap{ Hom_{\mathcal{D}}\big(C(f), C(id_Y)\big) }}
    \big\downarrow
    &&
    \!\!\!\!\!
    \big\downarrow {}^{\mathrlap{ Hom_{\mathcal{C}}\big( f, R C (id_Y) \big) }}
    \\
    Hom_{\mathcal{D}}\big( C(X),\, C(Y) \big)
    &\overset{\widetilde{ (-) }}{\longleftarrow}&
    Hom_{\mathcal{C}}\big( X, R C (Y) \big)
  }
  \phantom{AAAAA}
  \array{
    \{ C Y \overset{id_{C Y}}{\to} C Y\}
    &\longrightarrow&
    \{ Y \overset{\eta^\sharp_{Y}}{\to} R C Y \}
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    \{ C X \overset{C(f)}{\to} C Y \}
    &\longleftarrow&
    \{ X \overset{\eta^\sharp_{Y} \circ f}{\longrightarrow} R C Y \}
  }
$$

\end{proof}





$\,$

$\,$

We now consider a **sequence of equivalent reformulations** of the condition of adjointness.

+-- {: .num_prop #GeneralAdjunctsInTermsOfAdjunctionUnitCounit}
###### Proposition
**(general [[adjuncts]] in terms of [[adjunction unit|unit/counit]])**

Consider a pair of [[adjoint functors]]

$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{\bot}
  \mathcal{C}
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

   \[
      \label{TriangleIdentities}
      id_{L(c)}
      \;\colon\;
      L(c)
        \overset{L(\eta_c)}{\longrightarrow}
      L(R(L(c)))
        \overset{\epsilon_{L(c)}}{\longrightarrow}
      L(c)
   \]

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

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/Adjointness.jpg" width="380">
</div>


1. there exist [[natural transformations]]

   $$
     \eta \;\colon\; Id_{\mathcal{C}} \Rightarrow R \circ L
   $$

   and

   $$
     \epsilon \;\colon\; L \circ R \Rightarrow Id_{\mathcal{D}}
   $$

2. which satisfy the _[[triangle identities]]_

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

This equivalent perspective on adjoint functors makes manifest that adjoint functors are, if they exist, unique up to natural isomorphism, this is Prop. \ref{UniquenessOfAdjoints} below.



+-- {: .num_prop #AdjointFunctorFromObjectwiseRepresentingObject}
###### Proposition
**([[adjoint functor]] from objectwise [[representing objects]])**

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

We consider one more equivalent characterization of [[adjunctions]]:

+-- {: .num_defn #UniversalArrow}
###### Definition
**([[universal morphism]])**

Let $\mathcal{C}, \mathcal{D}$ be two [[categories]] (Def. \ref{Categories})
and let $R \;\colon\; \mathcal{D} \to \mathcal{C}$ be a [[functor]] (Def. \ref{Functors})

Then for $c\in \mathcal{C}$ an [[object]], a _[[universal morphism]] from $c$ to $R$_ is

1. an [[object]] $L(c)\in \mathcal{D}$,

1. a [[morphism]] $\eta_c \;\colon\; c \to R(L(c))$, to be called the _[[adjunction unit|unit]]_,

such that for any $d\in \mathcal{D}$, any morphism $f \colon c\to R(d)$ factors through this unit $\eta_c$ as

\[
  \label{UniversalArrowFactorization}
  f
  \;=\;
  \eta_c \circ R(\widetilde f)
  \phantom{AAAA}
  \array{
    && c
    \\
    & {}^{\mathllap{\eta_c}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    R(L(c)) &&\underset{R (\widetilde f)}{\longrightarrow}&& R(d)
    \\
    \\
    L(c) &&\underset{ \widetilde f}{\longrightarrow}&& d
  }
\]

for a _unique_ morphism $\widetilde f  \;\colon\; L(c) \longrightarrow d$, to be called the [[adjunct]] of $f$.

=--

+-- {: .num_prop #CollectionOfUniversalArrowsEquivalentToAdjointFunctor}
###### Proposition
**(collection of [[universal morphisms]] equivalent to [[adjoint functor]])**

Let $R \;\colon\; \mathcal{D} \to \mathcal{C}$ be a [[functor]] (Def. \ref{Functors}). Then the following are equivalent:

1. $R$ has a [[left adjoint]] functor $L \colon \mathcal{C} \to \mathcal{D}$ according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets},


1. For every [[object]] $c \in \mathcal{C}$ there is a [[universal morphism]] $c \overset{\eta_c}{\longrightarrow} R(L(c))$, according to Def. \ref{UniversalArrow}.

=--


+-- {: .proof}
###### Proof

In one direction, assume a [[left adjoint]] $L$ is given. Define the would-be universal arrow at $c \in \mathcal{C}$ to be the [[unit of an adjunction|unit of the adjunction]] $\eta_c$ via Def. \ref{AdjunctionUnitFromHomIsomorphism}. Then the statement that this really is a universal arrow is implied by Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}.

In the other direction, assume that universal arrows $\eta_c$ are given. The uniqueness clause in Def. \ref{UniversalArrow} immediately implies  [[bijections]]

$$
  \array{
    Hom_{\mathcal{D}}(L(c),d)
      &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(c,R(d))
    \\
    \left(
      L(c) \overset{\widetilde f}{\to} d
    \right)
      &\mapsto&
    \left(
      c \overset{\eta_c}{\to} R(L(c)) \overset{ R(\widetilde f) }{\to} R(d)
    \right)
  }
$$

Hence to satisfy (eq:HomIsomorphismForAdjointFunctors) it remains to show that these are [[natural transformation|natural]] in both variables. In fact, by Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject} it is sufficient to show naturality in the variable $d$. But this is immediate from the functoriality of $R$ applied in (eq:UniversalArrowFactorization): For $h \colon d_1 \to d_2$ any [[morphism]], we have

$$
  \array{
    && c
    \\
    & {}^{\mathllap{\eta_c}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    R (L(c)) &&\underset{R (\widetilde f)}{\longrightarrow}&& R(d_1)
    \\
    && {}_{\mathllap{ R( h\circ \widetilde f ) }}\searrow && \downarrow^{\mathrlap{R(h)}}
    \\
    && && R(d_2)
  }
$$


=--

The following equivalent formulation (Prop. \ref{UniversalMorphismsAreInitialObjectsInCommaCategory}) of [[universal morphisms]] is often useful:

+-- {: .num_example #CommaCategoryWithOneSideConstant}
###### Example
**([[comma category]])**

Let $\mathcal{C}$ be a [[category]], let $c \in \mathcal{C}$ be any [[object]], and let $F \;\colon\; \mathcal{D} \to \mathcal{C}$ be a [[functor]].

1. The _[[comma category]]_ $c/F$ is the [[category]] whose [[objects]] are [[pairs]] consisting of an object $d \in \mathcal{D}$ and [[morphisms]] $X \overset{f}{\to} F(d)$ in $\mathcal{C}$, and whose [[morphisms]] $(d_1,X_1,f_1) \to (d_2,X_2,f_2)$ are the [[morphisms]] $X_1 \overset{g}{\longrightarrow} X_2$ in $\mathcal{C}$ that make a commuting triangle (Def. \ref{CommutingDiagram}):

   $$
     f_2\circ F(g)
     \;=\;
     f_1
     \phantom{AAAAAA}
     \array{
        X_1 && \overset{\phantom{AA} g \phantom{AA}}{\longrightarrow} && X_2
        \\
        F(X_1)
          &&
          \overset{\phantom{AA} F(g) \phantom{AA}}{\longrightarrow}
          &&
        F(X_2)
        \\
        & {}_{\mathllap{f_1}}\searrow && \swarrow_{\mathrlap{f_2}}
        \\
        && c
     }
   $$

   There is a canonical [[functor]]

   $$
     \array{
       F/c
       &\overset{}{\longrightarrow}&
       \mathcal{D}
     }
     \,.
   $$


1. The _[[comma category]]_ $F/c$ is the [[category]] whose [[objects]] are [[pairs]] consisting of an [[object]] $d \in \mathcal{D}$ and a [[morphism]] $F(d) \overset{f}{\to} X$ in $\mathcal{C}$, and whose [[morphisms]] $(d_1,X_1,f_1) \to (d_2,X_2,f_2)$ are the [[morphisms]] $X_1 \overset{g}{\longrightarrow} X_2$ in $\mathcal{C}$ that make a commuting triangle (Def. \ref{CommutingDiagram}):

   $$
     f_2\circ F(g)
     \;=\;
     f_1
     \phantom{AAAAAA}
     \array{
        && c
        \\
        & {}^{\mathllap{f_1}}\swarrow && \searrow^{\mathrlap{f_2}}
        \\
        F(X_1)
          &&
          \underset{\phantom{AA} F(g) \phantom{AA}}{\longrightarrow}
          &&
        F(X_2)
        \\
        X_1 && \underset{ \phantom{AA} g \phantom{AA} }{\longrightarrow} && X_2
     }
   $$

   Again, there is a canonical [[functor]]

   \[
     \label{CanonicalFunctorOutOfCommaCategoryOfcOverF}
     \array{
       c/F
       &\overset{}{\longrightarrow}&
       \mathcal{D}
     }
   ]

=--

With this definition, the following is evident:

+-- {: .num_prop #UniversalMorphismsAreInitialObjectsInCommaCategory}
###### Proposition
**([[universal morphisms]] are [[initial objects]] in the [[comma category]])**

Let $\mathcal{C} \overset{R}{\longrightarrow} \mathcal{D}$ be a [[functor]] and $d \in \mathcal{D}$ an [[object]]. Then the following are equivalent:

1. $d \overset{\eta_d}{\to} R(c)$ is a [[universal morphism]] into $R(c)$ (Def. \ref{UniversalArrow});

1. $(d, \eta_d)$ is the [[initial object]] (Def. \ref{InitialObject}) in the [[comma category]] $d/R$ (Example \ref{CommaCategoryWithOneSideConstant}).


=--


$\,$

$\,$

After these equivalent characterizations of [[adjoint functors]], we now consider some of their main properties:

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


+-- {: .num_prop #FullyFaithfulAndInvertibleAdjoints}
###### Proposition
**(characterization of [[epimorphism|epi]]/[[monomorphism|mono]]/[[isomorphism|iso]] [[adjunction counit|(co-)]][[adjunction unit|unit]] of [[adjunction]])**

Let 

$$
  L \dashv R
  \;\colon\;
  \mathcal{D}
    \underoverset
      {\underset{\phantom{A}R\phantom{A}}{\longrightarrow}}
      {\overset{\phantom{A}L\phantom{A}}{\longleftarrow}}
      {\bot}
  \mathcal{C}
$$ 

be a pair of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}). 

Recall the definition of 

1. [[adjunction unit]]/[[adjunction counit|counit]], from Def. \ref{AdjunctionUnitFromHomIsomorphism})

1. [[faithful functor|faithful]]/[[fully faithful functor]] from Def. \ref{FullyFaithfulFunctor}

1. [[monomorphism|mono]]/[[epimorphism|epi]]/[[isomorphism]] from Def. \ref{Isomorphism} and Def. \ref{Monomorphism}.
 
The following holds:

* $R$ is [[faithful functor|faithful]] precisely if all components of the [[unit of an adjunction|counit]] are [[epimorphisms]] $L R(c) \underoverset{\phantom{A}epi\phantom{A}}{\eta_c}{\to} c$;

* $L$ is [[faithful functor|faithful]] precisely if all components of the [[adjunction unit|unit]] are [[monomorphisms]] $d \underoverset{mono}{\eta_d}{\to} R L(d)$


* $R$ is [[full and faithful functor|full and faithful]]
  (exhibits a _[[reflective subcategory]]_, Def. \ref{ReflectiveSubcategory})
  precisely if all components of the [[adjunction counit|counit]] are [[isomorphisms]] $L R(c) \underoverset{\phantom{A}iso\phantom{A}}{\eta_c}{\to} c$

* $L$ is [[full and faithful functor|full and faithful]]
  (exhibits a [[coreflective subcategory]], def. \ref{ReflectiveSubcategory}) precisely if all component of the [[adjunction unit|unit]] are [[isomorphisms]] $d \underoverset{\phantom{A}iso\phantom{A}}{\eta_d}{\to} R L(d)$.

=--

+-- {: .proof}
###### Proof

This follows directly by Lemma \ref{ReExpressingMiddleFunctorInAdjointTriple}, using the definition of epi/monomorphism (Def. \ref{Monomorphism}) and the characterization of [[isomorphism]] from Example \ref{YonedaCharacterizationOfIsomorphism}.

=--

To complete this pattern, we will see below in Prop. \ref{EveryEquivalenceOfCategoriesComesFromAnAdjointEquivalence} that following are equivalent:

* the [[adjunction unit|unit]] and [[adjunction counit|counit]] are both [[natural isomorphism]], hence $L$ and $R$ are both [[full and faithful functor|fully faithful]];

* $L$ is an [[equivalence of categories|equivalence]] (Def. \ref{EquivalenceOfCategories});

* $R$ is an [[equivalence of categories|equivalence]] (Def. \ref{EquivalenceOfCategories})

* $L \dashv R$ is an [[adjoint equivalence]] (Def. \ref{AdjointEquivalenceOfCategories}).


+-- {: .num_prop #LeftAdjointFunctorPreservesEpi}
###### Proposition
**(right/left [[adjoint functors]] preserve [[monomorphism]]/[[epimorphisms]] and [[terminal object|terminal]]/[[initial objects]])**

Every [[right adjoint]] functor (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) preserves

1. [[terminal objects]] (Def. \ref{InitialObject}),

1. [[monomorphisms]] (Def. \ref{Monomorphism})

Every [[left adjoint]] functor (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) preserves

1. [[initial objects]] (Def. \ref{InitialObject}),

1. [[epimorphisms]] (Def. \ref{Monomorphism}).

=--

+-- {: .proof}
###### Proof

This is immediate from the adjunction hom-isomorphism (eq:HomIsomorphismForAdjointFunctors), but we spell it out:

We consider the first case, the second is [[formal duality|formally dual]] (Example \ref{OppositeCategory}).
So let $R \;\colon\; \mathcal{C} \to \mathcal{D}$ be a [[right adjoint functor]] with [[left adjoint]] $L$.

Let $\ast \in \mathcal{C}$ be a [[terminal object]] (Def. \ref{InitialObject}). We need to show that for every [[object]] $d \in \mathcal{D}$ the [[hom-set]]  $Hom_{\mathcal{D}}(d,R(\ast)) \simeq \ast$ is a [[singleton]]. But by the hom-isomorphism (eq:HomIsomorphismForAdjointFunctors) we have a [[bijection]]

$$
  \begin{aligned}
    Hom_{\mathcal{d}}(d,R(\ast))
    & \simeq
    Hom_{\mathcal{C}}(L(d), \ast)
    \\
    & \simeq \ast
    \,,
  \end{aligned}
$$

where in the last step we used that $\ast$ is a terminal object, by assumption.

Next let $c_1 \overset{f}{\hookrightarrow} c_2$ be a [[monomorphism]]. We need to show that for $d \in \mathcal{D}$ any [[object]], the [[hom-functor]] out of $d$ yields a monomorphism

$$
  Hom_{\mathcal{D}}(d, R(f))
  \;\colon\;
  Hom_{\mathcal{D}}(d, R(c_1))
    \hookrightarrow
  Hom_{\mathcal{D}}(d, R(c_2))
  \,.
$$

Now consider the following [[naturality square]] (eq:NaturalitySquareForAdjointnessOfFunctors) of the adjunction hom-isomorphism (eq:HomIsomorphismForAdjointFunctors):

$$
  \array{
    Hom_{\mathcal{D}}(d, R(c_1))
    &\simeq&
    Hom_{\mathcal{C}}(L(d), c_1)
    \\
    {}^{ \mathllap{ Hom_{\mathcal{D}}(d,R(f)) } }\big\downarrow
      &&
    \big\downarrow^{ \mathrlap{ Hom_{\mathcal{C}}( L(d),f ) } }_{\mathrlap{mono}}
    \\
    Hom_{\mathcal{D}}(d, R(c_2))
    &\simeq&
    Hom_{\mathcal{C}}(L(d), c_2)
  }
$$

Here the right vertical [[function]] is an [[injective function]], by assumption on $f$ and the definition of [[monomorphism]]. Since the two horizontal functions are [[bijections]], this implies that also $Hom_{\mathcal{d}}(d,R(f))$ is an injection.

=--

But the main preservation property of [[adjoint functors]] is that _[[adjoints preserve (co-)limits]]_. This we discuss as Prop. \ref{AdjointsPreserveCoLimits} below, after introducing [[limits]] and [[colimits]] in Def. \ref{Limits} below.

$\,$

Prop. \ref{AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat} says that [[adjoint functors]] are equivalenty "[[adjunctions]] in [[Cat]]", as defined there. This is a special case of a general more abstract concept of [[adjunction]], that is useful:


+-- {: .num_defn #Strict2Categories}
###### Definition
**([[strict 2-category]])**

A _[[strict category]]_ $\mathcal{C}$ is

1. a [[class]] $Obj_{\mathcal{C}}$, called the _class of [[objects]]_;

1. for each [[pair]] $X,Y \in Obj_{\mathcal{C}}$ of [[objects]], a [[small category]] $Hom_{\mathcal{C}}(X,Y) \in Cat$ (Def. \ref{SmallCategory}), called the _[[hom-category]] from $X$ to $Y$_.

   We denote the [[objects]] of this [[hom-category]] by arrows like this:

   $$
     X \overset{f}{\longrightarrow} Y \;\;\in Obj_{Hom_{\mathcal{C}}(X,Y)}
   $$

   and call them the _[[1-morphisms]]_ of $\mathcal{C}$,

   and we denote the [[morphisms]] in the [[hom-category]] by double arrows, like this:

   $$
     X
       \underoverset
         {\underset{g}{\longrightarrow}}
         {\overset{f}{\longrightarrow}}
         {\Downarrow{}^{\mathrlap{\phi}}}
     Y
   $$

   and call these the _[[2-morphisms]]_ of $\mathcal{C}$;

1. for each [[object]] $X \in Obj_{\mathcal{C}}$ a [[1-morphism]]

   $$
      X \overset{id_X}{\to} X \;\; \in Hom_{\mathcal{C}}(X,X)
   $$

   called the _[[identity morphism]]_ on $X$;

1. for each [[triple]] $X_1, X_2, X_3 \in Obj$ of [[objects]], a [[functor]] (Def. \ref{Functors})

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

   from the [[product category]] (Example \ref{ProductCategory}) of [[hom-categories]], called _[[composition]]_;

such that:

1. for all [[pairs]] of [[objects]] $X,Y \in Obj_{\mathcal{C}}$ [[unitality]] holds:

   the [[functors]] of [[composition]] with [[identity morphisms]] are [[identity functors]]

   $$
     (-) \circ id_X
     \;=\;
     id_{ Hom_{\mathcal{C}}(X,Y) }
     \phantom{AAAA}
     id_Y \circ (-)      
     \;=\;
     id_{ Hom_{\mathcal{C}}(X,Y) }
   $$

1. for all [[quadruples]] of [[objects]] $X_1, X_2, X_3, X_4 \in Obj_{\mathcal{C}}$ [[composition]] satifies _[[associativity]]_, in that the following two composite [[functors]] are [[equality|equal]]:

   $$
     \array{
       Hom_{\mathcal{C}}(X_1, X_2) 
        \times 
       Hom_{\mathcal{C}}(X_2, X_3) 
        \times 
       Hom_{\mathcal{C}}(X_3, X_4) 
       &\overset{((-)\circ (-))\circ (-)}{\longrightarrow}&
       Hom_{\mathcal{C}}(X_1, X_3) \times Hom_{\mathcal{C}}(X_3, X_4)
       \\
       {}^{ \mathllap{ (-) \circ ( (-) \circ (-) ) } }\Big\downarrow 
       && 
       \Big\downarrow{}^{ (-) \circ (-) }
       \\
       Hom_{\mathcal{C}}(X_1, X_2) \times Hom_{\mathcal{C}}(X_2, X_4)
       &\underset{(-)\circ (-)}{\longrightarrow}&
       Hom_{\mathcal{C}}(X_1, X)4)
     }
   $$


=--
 

The archetypical example of a [[strict 2-category]] is the [[category of categories]]:

+-- {: .num_example #2CategoryOfCategories}
###### Example
**([[2-category of categories]])**

There is a [[strict 2-category]] (Def. \ref{Strict2Categories}) [[Cat]] whose

* [[objects]] are [[small categories]] (Def. \ref{SmallCategory});

* [[1-morphisms]] are [[functors]] (Def. \ref{Functors});

* [[2-morphisms]] are [[natural transformations]] (Def. \ref{NaturalTransformations})

with the evident [[composition]] operations.

=--

With a concept of [[2-category]] in hand, we may phrase Prop. \ref{AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat} more abstractly:

+-- {: .num_defn #AdjunctionInA2Category}
###### Definition
**([[adjunction]] in a [[2-category]])**

Let $\mathcal{C}$ be a [[strict 2-category]] (Def. \ref{Strict2Categories}). Then an _[[adjunction]]_ in $\mathcal{C}$ is

1. a [[pair]] of [[objects]] $\mathcal{C}, \mathcal{D} \in Obj_{\mathcal{C}}$;

1. [[1-morphisms]] 

   $$
     \mathcal{D}
       \underoverset
         {\underset{\phantom{AA}R\phantom{AA}}{\longrightarrow}}
         {\overset{L}{\longleftarrow}}
         {}
     \mathcal{C}
   $$

   called the _[[left adjoint]]_ $L$ and _[[right adjoint]]_ $R$;

1. [[2-morphisms]]

   $id_{\mathcal{C}} \overset{\eta}{\Rightarrow} R \circ L$, called the [[adjunction unit]]

   $L \circ R \overset{\epsilon}{\Rightarrow} id_{\mathcal{D}}$, called the [[adjunction counit]]


such that the following _[[triangle identities]]_ hold:

<center>
<img src="https://ncatlab.org/nlab/files/Adjointness.jpg" width="380">
</center>

We denote this situation by 

   $$
     \mathcal{D}
       \underoverset
         {\underset{\phantom{AA}R\phantom{AA}}{\longrightarrow}}
         {\overset{L}{\longleftarrow}}
         {\bot}
     \mathcal{C}
   $$
   
=--

Hence via Example \ref{2CategoryOfCategories}, Prop. \ref{AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat} says that an [[adjoint pair]] of [[functors]] is equivalente an [[adjunction]] in the general sense of Def. \ref{AdjunctionInA2Category}, realized in the [[very large category|very large]] [[strict 2-category]] [[Cat]] of [[categories]]. 

This more abstract perspecive on [[adjunctions]] allow us now to understand "duality of dualities" as [[adjunction]] in a [[2-category]] of [[adjunctions]]:

+-- {: .num_example #2CategoryOfCategoriesWithAdjointFunctorsBetweenThem}
###### Example
**([[strict 2-category]] of [[categories]] with [[adjoint functors]] between them)**

Let $Cat_{Adj}$ be the [[strict 2-category]] which is defined just as [[Cat]] (Def. \ref{2CategoryOfCategories}) but with the [[1-morphisms]] being [[functors]] that are required to be [[left adjoints]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}). 

Since adjoints are unique up to natural isomorphism (Prop. \ref{UniquenessOfAdjoints}), this may be thought of as a 2-category whose [[1-morphisms]] are [[adjoint pairs]] of [[functors]].

=--

+-- {: .num_example #AdjunctionofAdjunction}
###### Example
**([[adjunctions]] of [[adjoint pairs]] are [[adjoint triples]])**

An [[adjunction]] (Def. \ref{AdjunctionInA2Category}) in the [[2-category]] $Cat_{Adj}$ of [[categories]] with [[adjoint functors]] between them (Example \ref{2CategoryOfCategoriesWithAdjointFunctorsBetweenThem}) is equivalently an [[adjoint triple]] of functors (Remark \ref{AdjointTriples}):

The adjunction says that two [[left adjoint functors]] $L_1$ and $L_2$, which, hence each participate in an [[adjoint pair]] 

$$
  L_1 \dashv R_1
  \phantom{AAAA}
  L_2 \dashv R_2
$$

form themselves an [[adjoint pair]] 

$$
  L_1 \dashv L_2
  \,.
$$

By essentiall uniqueness of adjoints (Prop. \ref{UniquenessOfAdjoints}) this implies a [[natural isomorphism]] $R_1 \simeq L_2$ and hence an [[adjoint triple]]:

$$
  \mathcal{D}
    \array{
      \underoverset{\bot \phantom{\simeq A_a}}{ L_1 \phantom{\simeq A_a} }{\longleftarrow}
      \\
      \underoverset{\phantom{A_a \simeq}\bot}{R_1 \simeq L_2}{\longrightarrow}
      \\
      \overset{ \phantom{A_a \simeq} R_2 }{\longleftarrow}
    }
  \mathcal{C}
$$



=--

Example \ref{AdjunctionofAdjunction} suggest to consider a slight variant of the concept of [[strict 2-categories]] which allows to make the duality between [[left adjoints]] and [[right adjoints]] explicit:

+-- {: .num_defn #DoubleCategory}
###### Definition
**([[double category]])**

A _[[double category]]_ $\mathcal{C}$ is

1. a [[pair]] of [[categories]] $\mathcal{C}_h$, $\mathcal{C}_v$ (Def. \ref{Categories}) which share the same class of objects: $Obj_{\mathcal{C}_1} = Obj_{\mathcal{C}_2}$, to be called the class $Obj_{\mathcal{C}}$ of _objects of $\mathcal{C}$_

   where the [[morphisms]] of $\mathcal{C}_h$ are to be called the _[[horizontal morphisms]]_ of $\mathcal{C}$,

   while the [[morphisms]] of $\mathcal{C}_v$ are to be called the _[[vertical morphisms]]_ of $\mathcal{C}$,

1. for each [[quadruple]] of [[objects]] $a,b,c,d,e \in Obj_{\mathcal{C}}$ and [[pairs]] of [[pairs]] of horizontal/vertical morphisms of the form

   $$
     \array{
       a &\overset{f \in \mathcal{C}_h}{\longrightarrow}& b
       \\
       {}^{\mathllap{h \in \mathcal{C}_v}}\big\downarrow && \big\downarrow{}^{\mathrlap{k \in \mathcal{C}_v}}
       \\
       c &\underset{g \in \mathcal{C}_h}{\longrightarrow}&
     }
   $$

   a [[set]] $2Hom(f,g,h,k)$, to be called the set of _[[2-morphisms]]_ of $\mathcal{C}$ between the given [[1-morphisms]], whose elements we denote by

   $$
     \array{
       a &\overset{f \in \mathcal{C}_h}{\longrightarrow}& b
       \\
       {}^{\mathllap{h \in \mathcal{C}_v}}\big\downarrow 
       &\swArrow& \big\downarrow{}^{\mathrlap{k \in \mathcal{C}_v}}
       \\
       c &\underset{g \in \mathcal{C}_h}{\longrightarrow}& d
     }
   $$

1. a horizontal and a vertical [[composition operation]] of 2-morphisms which is [[unitality]] and [[associativity|associative]] in both directions in the evident way, which respects composition in $\mathcal{C}_h$ and $\mathcal{C}_v$, and such that horizontal and vertical composition commute over each other in the evident way.

=--

+-- {: .num_example #DoubleCategoryOfSquares}
###### Example
**([[double category of squares]] of a [[strict 2-category]])**

Let $\mathcal{C}$ be a [[strict 2-category]] (Def. \ref{Strict2Categories}). Then its _[[double category of squares]]_ $Sq(\mathcal{C})$ is the [[double category]] (Def. \ref{DoubleCategory}) whose

* [[objects]] are those of $\mathcal{C}$;

* [[horizontal morphisms]] and [[vertical morphisms]] are both the [[1-morphisms]] of $\mathcal{C}$;

* [[2-morphisms]] 

  $$
    \array{
      a &\overset{f \in \mathcal{C}_h}{\longrightarrow}& b
      \\
      {}^{\mathllap{h \in \mathcal{C}_v}}\big\downarrow 
        &{}^{\mathllap{\phi}}\swArrow& 
      \big\downarrow{}^{\mathrlap{k \in \mathcal{C}_v}}
      \\
      c &\underset{g \in \mathcal{C}_h}{\longrightarrow}& d
    }
  $$

  are the [[2-morphisms]] of $\mathcal{C}$ between the evident composites of 1-morphisms:


  $$
    k \circ f \overset{\phi}{\Rightarrow} g\circ h
  $$

and composition is given by the evident compositions in $\mathcal{C}$.

=--


+-- {: .num_remark #StrictAndWeak2Functors}
###### Remark
**([[strict 2-functor|strict]] and [[weak 2-functor|weak]] [[2-functors]])**

Given two [[strict 2-categories]] (Def. \ref{Strict2Categories}) or [[double categories]] (Def. \ref{DoubleCategory}), $\mathcal{C}, \mathcal{D}$, there is an evident notion of _[[2-functor]]_ or _[[double functor]]_ 

$$
  \mathcal{C} \overset{F}{\longrightarrow} \mathcal{D}
$$ 

between them, namely [[functions]] on [[objects]], [[1-morphisms]] and [[2-morphisms]] which respect all the [[composition]] operations and [[identity morphisms]].

These are also called _[[strict 2-functors]]_. 

This is in contrast to a more flexible concept of _[[weak 2-functors]]_, often called _[[pseudofunctors]]_, which respect [[composition]] of [[1-morphisms]] only up to invertible [[2-morphisms]] (which themselves are required to satisfy some [[coherence]] condition):

$$
  \array{
    && Y
    \\
    & {}^{\mathllap{ F(f) }}\nearrow 
      &\Downarrow{}^{\rho}_{}\simeq& 
    \searrow^{\mathrlap{F(G)}}
    \\
    X && \underset{F(g \circ f)}{\longrightarrow} && Z
  }
$$

=--

We will see an important example of a weak double functor in the construction of [[derived functors]] of [[Quillen functors]], below in Prop. \ref{HomotopyDoublePseudofunctor}. 


$\,$

### Equivalences
 {#Equivalences}

We have seen [[functors]] (Def. \ref{Functors}) as the [[homomorphisms]] between [[categories]] (Def. \ref{Categories}). But functors themselves are identified only up to [[natural isomorphism]] (Def. \ref{NaturalTransformations}), reflective the fact that they are the [[1-morphisms]] in a [[2-category]] of categories (Example \ref{2CategoryOfCategories}). This means that in identifying two categories, we should not just ask for _[[isomorphisms]]_ between them, hence for a [[functor]] between them that has a strict [[inverse morphism]], but just for an inverse up to [[natural isomorphism]]. 

This is called an _[[equivalence of categories]]_ (Def. \ref{EquivalenceOfCategories} below). A particularly well-behaved equivalence of categories is an equivalence exhibited by an [[adjoint pair]] of functors, called an _[[adjoint equivalence of categories]]_ (Def. \ref{AdjointEquivalenceOfCategories} below). In fact every [[equivalence of categories]] may be improved to an [[adjoint equivalence]] (Prop. \ref{EveryEquivalenceOfCategoriesComesFromAnAdjointEquivalence}).

$\,$

 
+-- {: .num_defn #AdjointEquivalenceOfCategories}
###### Definition
**([[adjoint equivalence of categories]])**

Let $\mathcal{C}$, $\mathcal{D}$ be two [[categories]] (Def. \ref{Categories}). Then an _[[adjoint equivalence of categories]]_ between them is a [[pair]] [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets})

$$
  \array{
    \mathcal{C}
      \underoverset
        {\underset{R}{\longrightarrow}}
        {\overset{L}{\longleftarrow}}
        {\phantom{A} \phantom{{}_{\bot}}\simeq_{\bot} \phantom{A}}
    \mathcal{D}
  }
$$

such that their [[unit of an adjunction|unit]] $\eta$ and [[counit of an adjunction|counit]] $\epsilon$ (Def. \ref{AdjunctionUnitFromHomIsomorphism}) are [[natural isomorphisms]] (as opposed to just being [[natural transformations]])


$$
  \eta\;\colon\; id_{\mathcal{D}} \overset{\simeq}{\Rightarrow} R \circ L
  \phantom{AAA}
   \text{and}
  \phantom{AAA}
  \epsilon\;\colon\;
  L \circ R \overset{\simeq}{\Rightarrow} id_{\mathcal{C}}
  \,.
$$

=--

There is also the following, seemingly weaker, notion:

+-- {: .num_defn #EquivalenceOfCategories}
###### Definition
**([[equivalence of categories]])**

Let $\mathcal{C}$, $\mathcal{D}$ be two [[categories]] (Def. \ref{Categories}). Then an _[[equivalence of categories]]_

$$
  \array{
    \mathcal{C}
      \underoverset
        {\underset{R}{\longrightarrow}}
        {\overset{L}{\longleftarrow}}
        {\phantom{AA} \simeq \phantom{AA}}
    \mathcal{D}
  }
$$

is a [[pair]] of [[functors]] back and forth, as shown (Def. \ref{Functors}), together with [[natural isomorphisms]] (Def. \ref{NaturalTransformations}) between their [[composition]] and the [[identity functors]]:

$$
  id_{\mathcal{D}} \overset{\simeq}{\Rightarrow} R \circ L
  \phantom{AAA}
   \text{and}
  \phantom{AAA}
  L \circ R \overset{\simeq}{\Rightarrow} id_{\mathcal{C}}
  \,.
$$


=--

If a functor participates in an equivalence of categories, that functor alone is usually already called an equivalence of categories. If there is any equivalence of categories between two categories, these categories are called _equivalent_.


+-- {: .num_prop #EveryEquivalenceOfCategoriesComesFromAnAdjointEquivalence}
###### Proposition
**(every [[equivalence of categories]] comes from an [[adjoint equivalence of categories]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be two [[categories]] (Def. \ref{Categories}). Then the they are [[equivalence of categories|equivalent]] (Def. \ref{EquivalenceOfCategories}) precisely if there exists an [[adjoint equivalence of categories]] between them (Def. \ref{AdjointEquivalenceOfCategories}).

Moreover, let $R \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ be a [[functor]] (Def. \ref{Functors}) which participates in an [[equivalence of categories]] (Def. \ref{EquivalenceOfCategories}). Then for every functor $L \;\colon\; \mathcal{D} \to \mathcal{C}$ equipped with a [[natural isomorphism]]

$$
  \eta
    \;\colon\;
  id_{\mathcal{D}}
    \overset{\simeq}{\Rightarrow}
  R \circ L
$$

there exists a [[natural isomorphism]]

$$
  \epsilon
  \;\colon\;
  L \circ R \overset{\simeq}{\Rightarrow} id_{\mathcal{C}}
$$

which completes this to an [[adjoint equivalence of categories]] (Def. \ref{AdjointEquivalenceOfCategories}).

=--

Inside every [[adjunction]] sits its maximal [[adjoint equivalence]]:


+-- {: .num_prop #FixedPointEquivalenceOfAnAdjunction}
###### Proposition
**([[fixed point equivalence of an adjunction]])**

Let

$$
  \mathcal{D}
    \underoverset
      {\underset{ R }{\longrightarrow}}
      {\overset{ L }{\longleftarrow}}
      {\phantom{AA}\bot\phantom{AA}}
  \mathcal{C}
$$

be a pair of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}). Say that 

1. an [[object]] $c \in \mathcal{C}$ is a _[[fixed point of an adjunction|fixed point of the adjunction]]_ if its  [[adjunction unit]] (Def. \ref{AdjunctionUnitFromHomIsomorphism}) is an [[isomorphism]] (Def. \ref{Isomorphism})

   $$
     c \underoverset{\simeq}{\eta_c}{\longrightarrow} R L (c)
   $$

   and write 

   $$
     \mathcal{C}_{fix} \hookrightarrow \mathcal{C}
   $$

   for the [[full subcategory]] on these fixed objects (Example \ref{FullSubcategoryOnClassOfObjects})


1. an [[object]] $d \in \mathcal{D}$ is a _[[fixed point of an adjunction|fixed point of the adjunction]]_ if its  [[adjunction counit]] (Def. \ref{AdjunctionUnitFromHomIsomorphism}) is an [[isomorphism]] (Def. \ref{Isomorphism})

   $$
    L R(d) \underoverset{\simeq}{\epsilon_d}{\longrightarrow}
   $$

   and write 

   $$
     \mathcal{D}_{fix} \hookrightarrow \mathcal{D}
   $$

   for the [[full subcategory]] on these fixed objects (Example \ref{FullSubcategoryOnClassOfObjects})


Then the [[adjunction]] ([[corestriction|co]]-)[[restriction|restrics]] to an [[adjoint equivalence]] (Def. \ref{AdjointEquivalenceOfCategories}) on these [[full subcategories]] of [[fixed points]]

$$
  \mathcal{D}_{fix}
    \underoverset
      {\underset{ R }{\longrightarrow}}
      {\overset{ L }{\longleftarrow}}
      {\phantom{A}\phantom{{}_{\bot}}\simeq_{\bot}\phantom{A}}
  \mathcal{C}_{fix}
$$


=--


+-- {: .proof}
###### Proof

It is sufficient to see that the functors ([[corestriction|co-]])[[restriction|restrict]] as claimed, for then the restricted adjunction unit/counit are [[isomorphisms]] by definition, and hence exhibit an [[adjoint equivalence]].

Hence we need to show that 

1. for $c \in \mathcal{C}_{fix} \hookrightarrow \mathcal{C}$ we have that $\eta_{R(d)}$ is an [[isomorphism]];

1. for $d \in \mathcal{D}_{fix} \hookrightarrow \mathcal{D}$ we have that $\epsilon_{L(c)}$ is an [[isomorphism]].

For the first case we claim that $R(\eta_{d})$ provides an [[inverse morphism|inverse]]: by the [[triangle identity]] (eq:TriangleIdentities) it is a [[right inverse]], but by assumption it is itself an [[invertible morphism]], which implies that $\eta_{R(d)}$ is an isomorphism.

The second claim is [[formal duality|formally dual]].

=--


$\,$

### Modalities
  {#Modalities}

Generally, a [[full subcategory]]-inclusion (Def. \ref{FullyFaithfulFunctor}) may be thought of as a consistent [[proposition]] about [[objects]] in a [[category]]: The objects in the full subcategory are those that have the given property.

This basic situation becomes particularly interesting when the inclusion functor has a [[left adjoint]] or a [[right adjoint]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}), in which case one speaks of a _[[reflective subcategory]]_, or a _[[coreflective subcategory]]_, respectively (Def. \ref{ReflectiveSubcategory} below). The [[adjunction]] now implies that each [[object]] is _[[reflector|reflected]]_ or _[[coreflector|coreflected]]_ into the subcategory, and equipped with a comparison morphism to or from its (co-)reflection (the adjunction (co-)unit, Def. \ref{AdjunctionUnitFromHomIsomorphism}). This comparison morphism turns out to always be an idempotent (co-)projection, in a sense made precise by Prop. \ref{ModalOpIdempotent} below.

This means that, while any object may not fully enjoy the property that defines the subcategory, one may ask for the "aspect" of it that does, which is what is (co-)projected out. Regarding objects only via these aspects of them hence means to regard them only _locally_ (where they exhibit that aspect) or only in the _mode_ of focus on this aspect. Therefore one also calls the (co-)reflection operation into the given subcategory a _([[colocalization|co]]-)[[localization]]_ or _([[comodal operator|co-]])[[modal operator]]_, or _[[modality]]_, for short (Def. \ref{ModalOperator} below).

One finds that (co-)modalities are a fully equivalent perspective on  the (co-)reflective subcategories of their fully _([[comodal object|co-]])[[modal objects]]_ (Def. \ref{ModalObjects} below), this is the statement of Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories} below.

Another alternative perspective on this situation is given by the concept of _[[localization of categories]]_ (Def. \ref{LocalizationOfACategory} below), which is about [[universal property|universally]] forcing a given collection of [[morphisms]] ("[[weak equivalences]]", Def. \ref{CategoryWithWeakEquivalences} below) to become [[inverse morphism|invertible]]. A _[[reflective localization]]_ is equivalently a [[reflective subcategory]]-inclusion (Prop. \ref{ReflectiveSubcategoriesAreLocalizations} below), and this exhibits the [[modal objects]] (Def. \ref{ModalObjects} below) as equivalently forming the [[full subcategory]] of _[[local objects]]_ (Def. \ref{LocalObjects} below). 

Conversely, every [[reflective subcategory|reflection]] onto [[full subcategories]] of $S$-[[local objects]] (Def. \ref{LocalizationAtACollectionOfMorphisms} below) satisfies the [[universal property]] of a [[localization]] at $S$ with respect to [[left adjoint]] [[functors]] (Prop. \ref{ReflectionOntoLocalObjectsIsLocalizationWithRespectToLeftAdjoints} below). 

In conclusion, we have the following three equivalent perspectives on [[modalities]].


| $\phantom{A}$[[reflective subcategory]]$\phantom{A}$ | $\phantom{A}$[[modal operator]]$\phantom{A}$ | $\phantom{A}$[[reflective localization]]$\phantom{A}$ | 
|-------------|------------|-------------|
| $\phantom{A}$[[object]] in [[reflective subcategory|reflective]]$\phantom{A}$ <br/> $\phantom{A}$[[full subcategory]]$\phantom{A}$ | $\phantom{A}$[[modal object]]$\phantom{A}$ | $\phantom{A}$[[local object]]$\phantom{A}$ | 
{: style='margin:auto}



$\,$

+-- {: .num_defn #ReflectiveSubcategory}
###### Definition
**([[reflective subcategory]] and [[coreflective subcategory]])**

Let $\mathcal{D}$ be a [[category]] (Def. \ref{Categories}) and

$$
  \mathcal{C}
  \overset{\phantom{AA}\iota \phantom{AA}}{\hookrightarrow}
  \mathcal{D}
$$

a [[full subcategory]]-inclusion (hence a [[fully faithful functor]] Def. \ref{FullyFaithfulFunctor}). This is called:

1. a _[[reflective subcategory]] inclusion_ if the inclusion functor $\iota$ has a [[left adjoint]] $L$ def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets})

   $$
     \mathcal{C}
       \underoverset
         {\underset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}}
         {\overset{L}{\longleftarrow}}
         {\bot}
     \mathcal{D}
     \,,
   $$

   then called the _[[reflector]]_;

1. a _[[coreflective subcategory]]_-inclusion if the inclusion functor $\iota $ has a [[right adjoint]] $R$ (def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets})

   $$
     \mathcal{C}
       \underoverset
         \underset{R}{\longleftarrow}
         {\overset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}}
         {\bot}
     \mathcal{D}
     \,,
   $$

   then called the _[[coreflector]]_.

=--

+-- {: .num_example #ReflectiveSubcategoryInclusionOfSetsIntoGroupoids}
###### Example
**([[reflective subcategory]] inclusion of [[sets]] into [[small groupoid|small]] [[groupoids]])**

There is a [[reflective subcategory]]-inclusion (Def. \ref{ReflectiveSubcategory})

$$
  Set
    \underoverset
     {\underset{\phantom{AAAA}}{\hookrightarrow}}
     {\overset{\pi_0}{\longleftarrow}}
     {\bot}
  Grp
$$

of the [[category of sets]] (Example \ref{CategoryOfSets}) into the [[category]] [[Grpd]] (Example \ref{CategoriesOfSmallCategories}) of [[small groupoids|small]] [[groupoids]] (Example \ref{Groupoid}) where

* the [[right adjoint]] [[full subcategory]] inclusion (Def. \ref{FullyFaithfulFunctor}) sends a [[set]] $S$ to the [[groupoid]] with set of objects being $S$, and the only [[morphisms]] being the [[identity morphisms]] on these objects (also called the _[[discrete groupoid]]_ on $S$, but this terminology is ambiguous)

* the [[left adjoint]] [[reflector]] sends a [[small groupoid|small]] [[groupoid]] $\mathcal{G}$ to its set of [[connected components]], namely to the set of [[equivalence classes]] under the [[equivalence relation]] on the set of [[objects]], which regards two objects as equivalent, if there is any [[morphism]] between them.

=--



$\,$

We now re-consider the concept of [[reflective subcategories]] from the point of view of [[modalities]]:

+-- {: .num_defn #ModalOperator}
###### Definition
**([[modality]])**

Let $\mathcal{D}$ be a [[category]] (Def. \ref{Categories}). Then

1. a _[[modal operator]] on $\mathcal{D}$_ is

   1. an [[endofunctor]]

      $$
        \bigcirc \;\colon\; \mathcal{D} \to \mathcal{D}
      $$

      whose [[full subcategory|full]] [[essential image]] we denote by

      $$
        Im(\bigcirc)
          \overset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}
        \mathcal{D}
        \,,
      $$

   1. a [[natural transformation]] (Def. \ref{NaturalTransformations})

      \[
        \label{UnitOfAModalOperator}
        X \overset{\eta_X}{\longrightarrow} \bigcirc X
      \]

      for all [[objects]] $X \in \mathcal{D}$,
      to be called the _unit morphism_;

   such that:

   * for every [[object]] $Y \in Im(\bigcirc) \hookrightarrow \mathcal{D}$ in the [[essential image]] of $\bigcirc$, every [[morphism]] $f$ into $Y$ factors _uniquely_ through the unit (eq:UnitOfAModalOperator)

     $$
       \array{
         && X
         \\
         & {}^{\mathllap{ \eta_X }}\swarrow && \searrow^{\mathrlap{f}}
         \\
         \mathrlap{\bigcirc X\;\;\;\;} && \underset{\exists !}{\longrightarrow} &&  Y & \in Im(\bigcirc)
       }
     $$

     which equivalently means that if $Y \in Im(\bigcirc)$ the operation of [[composition|precomposition]] with the unit $\eta_X$ yields a [[bijection]] of [[hom-sets]]

     \[
       \label{ModalityUnitPrecomposition}
       (-)\circ \eta_X
       \;\colon\;
       Hom_{\mathcal{D}}(\bigcirc X, Y)
       \overset{\phantom{AA}\simeq\phantom{AA}}{\longrightarrow}
       Hom_{\mathcal{D}}(X, Y)
       \,,
     \]

1. a _[[comodal operator]] on $\mathcal{D}$_ is

   1. an [[endofunctor]]

      $$
        \Box \;\colon\; \mathcal{D} \to \mathcal{D}
      $$

      whose [[full subcategory|full]] [[essential image]] we denote by

      $$
        Im( \Box )
          \overset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}
        \mathcal{D}
      $$

   1. a [[natural transformation]] (Def. \ref{NaturalTransformations})

      \[
        \label{CounitOfModalOperator}
        \Box X \overset{ \epsilon_X }{\longrightarrow} X
      \]

      for all [[objects]] $X \in \mathcal{D}$,
      to be called the _counit morphism_;

   such that:

   * for every [[object]] $Y \in Im( \Box ) \hookrightarrow \mathcal{D}$ in the [[essential image]] of $\Box$, every [[morphism]] $f$ out of $Y$ factors _uniquely_ through the counit (eq:UnitOfAModalOperator)

     $$
       \array{
          && X
          \\
          & {}^{\mathllap{\epsilon_X}}\nearrow && \nwarrow^{\mathrlap{f}}
          \\
          \mathrlap{\Box X\;\;\;} && \underset{\exists !}{\longleftarrow} && Y \in Im( \Box )
       }
     $$

     which equivalently means that if $Y \in Im(\bigcirc)$ the operation of [[composition|postcomposition]] with the counit $\epsilon_X$ yields a [[bijection]] of [[hom-sets]]

     \[
       \label{CoModalityCoUnitPostcomposition}
       \epsilon_X \circ (-)
       \;\colon\;
       Hom_{\mathcal{D}}(Y, \Box X)
       \overset{\phantom{AA}\simeq\phantom{AA}}{\longrightarrow}
       Hom_{\mathcal{D}}(Y , X)
       \,,
     \]

=--


+-- {: .num_prop #ModalOperatorsEquivalentToReflectiveSubcategories}
###### Proposition
**([[modal operators]] equivalent to [[reflective subcategories]])**

If

$$
  \mathcal{C}
    \underoverset
      {\underset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

is a [[reflective subcategory]]-inclusion (Def. \ref{ReflectiveSubcategory}). Then the [[composition|composite]]

$$
  \bigcirc
  \;\coloneqq\;
  \iota \circ L
  \;\colon\;
  \mathcal{D} \longrightarrow \mathcal{D}
$$

equipped with the [[adjunction unit]] [[natural transformation]] (Def. \ref{AdjunctionUnitFromHomIsomorphism})

$$
  X \overset{\eta_X}{\longrightarrow} \bigcirc X
$$

is a [[modal operator]] on $\mathcal{D}$ (Def. \ref{ModalOperator}).


Dually, if

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longleftarrow}}
      {\overset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}}
      {\bot}
  \mathcal{D}
$$

is a [[coreflective subcategory]]-inclusion (Def. \ref{ReflectiveSubcategory}). Then the [[composition|composite]]

$$
  \Box
  \;\coloneqq\;
  \iota \circ R
  \;\colon\;
  \mathcal{D} \longrightarrow \mathcal{D}
$$

equipped with the [[adjunction counit]] [[natural transformation]] (Def. \ref{AdjunctionUnitFromHomIsomorphism})

$$
  \Box X \overset{ \epsilon_X }{\longrightarrow} X
$$

is a [[comodal operator]] on $\mathcal{D}$ (Def. \ref{ModalOperator}).

Conversely:

If an [[endofunctor]] $\bigcirc \;\colon\; \mathcal{D} \to \mathcal{D}$ with [[natural transformation]] $X \overset{\eta_X}{\to} \bigcirc X$ is a [[modal operator]] on a [[category]] $\mathcal{D}$ (Def. \ref{ModalOperator}), then the inclusion of its [[full subcategory|full]] [[essential image]] is a [[reflective subcategory]] inclusion (Def. \ref{ReflectiveSubcategory}) with [[reflector]] given by the [[corestriction]] of $\bigcirc$ to its image:

$$
  Im( \bigcirc )
    \underoverset
      {\underset{ \phantom{AA} \iota \phantom{AA} }{\hookrightarrow}}
      {\overset{ \bigcirc }{\longleftarrow}}
      {}
  \mathcal{D}
  \,.
$$

Dually, if an [[endofunctor]] $\Box \;\colon\; \mathcal{D} \to \mathcal{D}$ with [[natural transformation]] $\Box X \overset{\epsilon_X}{\longrightarrow} X$ is a [[comodal operator]] (Def. \ref{ModalOperator}), then the inclusion of its [[full subcategory|full]] [[essential image]] is a [[coreflective subcategory]] inclusion (Def. \ref{ReflectiveSubcategory}) with [[coreflector]] given by the [[corestriction]] of $\Box$ to its image

$$
  Im( \Box )
    \underoverset
      {\underset{ \Box }{\longleftarrow}}
      {\overset{ \phantom{AA} \iota \phantom{AA} }{\hookrightarrow}}
      {}
  \mathcal{D}
  \,.
$$


=--

+-- {: .proof}
###### Proof

The first two statements are immedialy a special case of the characterization of [[adjunctions]] via [[universal morphisms]] in Prop. \ref{CollectionOfUniversalArrowsEquivalentToAdjointFunctor}: Using that $R = \iota$ is here assumed to be [[fully faithful functor|fully faithful]], the uniqueness of $\tilde f$ in the [[universal morphism]]-factorization condition (eq:UniversalArrowFactorization)

$$
  \array{
    && c
    \\
    & {}^{\mathllap{\eta_c}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    R(L(c)) &&\underset{R (\widetilde f)}{\longrightarrow}&& R(d)
    \\
    \\
    L(c) &&\underset{ \exists ! \, \widetilde f}{\longrightarrow}&& d
  }
$$

implies that also $R(\widetilde f) = \iota(\widetilde f)$ is the unique morphism making that triangle commute.

Similarly for the converse: The assumption on a [[modal operator]] $\bigcirc$ is just so as to make its unit $\eta$ be a [[universal morphism]] (Def. \ref{UniversalArrow}) into the inclusion functor $\iota$ of its [[essential image]].

=--

+-- {: .num_prop #ModalOpIdempotent}
###### Proposition
**([[modal operator]] is [[idempotent]])**

Let $\mathcal{D}$ be a [[category]] (Def. \ref{Categories}).

For $\bigcirc$ a [[modal operator]] on $\mathcal{D}$, with unit $\eta$ (Def. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}), it is _[[idempotent monad|idempotent]]_, in that it is [[natural isomorphism|naturally isomorphic]] (Def. \ref{NaturalTransformations}) to the [[composition]] with itself:

$$
  \bigcirc \;\simeq\; \bigcirc \bigcirc
  \,.
$$

In fact, the image under $\bigcirc$ of its unit is such an isomorphism

$$
  \bigcirc\left( X \overset{\eta_X}{\to} \bigcirc X \right)
  \;\;\colon\;\;
  \bigcirc X
    \overset{\simeq}{\longrightarrow}
  \bigcirc ( \bigcirc X )
$$

as is its unit on its image

$$
  \eta_{\bigcirc X}
  \;\;\colon\;\;
  \bigcirc X
    \overset{\simeq}{\longrightarrow}
  \bigcirc ( \bigcirc X )
  \,.
$$


[[formal dual|Formally dually]], for $\Box$ a [[comodal operator]] on $\mathcal{D}$, with counit $\epsilon$ (Def. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}), it is _[[idempotent monad|idempotent]]_, in that it is [[natural isomorphism|naturally isomorphic]] (Def. \ref{NaturalTransformations}) to the [[composition]] with itsef:

$$
  \Box \circ \Box
  \;\simeq\;
  \Box
  \,.
$$

In fact, the image under $\Box$ of its counit is such an isomorphism

$$
  \Box\left(  \Box X \overset{\epsilon_X}{\to} X \right)
  \;\;\colon\;\;
  \Box (\Box X)
    \overset{\simeq}{\longrightarrow}
  \Box X
$$

as is its counit on its image

$$
  \epsilon_{\Box X}
  \;\;\colon\;\;
  \Box ( \Box X )
    \overset{\simeq}{\longrightarrow}
  \Box X
  \,.
$$

=--

+-- {: .proof}
###### Proof

We discuss the first case, the second is [[formal dual|formally dual]] (Example \ref{OppositeCategory}).

By Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}, the modal operator is equivalent to the composite $\iota \circ L$ obtained from the [[reflective subcategory]]-inclusion (Def. \ref{ReflectiveSubcategory}) of its [[essential image]] of [[modal objects]]:

$$
  Im(\bigcirc)
    \underoverset
      {\underset{\phantom{AA}\iota \phantom{AA}}{\hookrightarrow}}
      {\overset{\phantom{AA}L \phantom{AA} }{\longleftarrow}}
      {\bot}
  \mathcal{D}
  \,.
$$

and its unit is the corresponding [[adjunction unit]] (Def. \ref{AdjunctionUnitFromHomIsomorphism})

$$
  X \overset{\eta_X}{\longrightarrow} \iota \circ L
  \,.
$$

Hence it is sufficient to show that the morphisms and $L( \eta_X )$ and $\eta_{\iota Y}$ are isomorphisms.

Now, the [[triangle identities]] (eq:TriangleIdentities) for the [[adjunction]] $L \dashv \iota$, which hold by Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}, say that their [[composition]] with the [[adjunction counit]] is the [[identity morphism]]

$$
  \epsilon_{L(\eta_X)} \circ L(\eta_X)
  \;=\;
  id_{L(X)}
  \phantom{AA} \text{and} \phantom{AA}
  \iota( \epsilon_Y )\circ \eta_{\iota(Y)}
  \;=\;
  id_{\iota(Y)}
  \,.
$$

But by Prop. \ref{FullyFaithfulAndInvertibleAdjoints}, the counit $\epsilon$ is a [[natural isomorphism]], since $\iota$ is [[fully faithful functor|fully faithful]]. Hence we may cancel it on both sides of the [[triangle identities]] and find that $L(\eta_X)$ and $\eta_{\iota(Y)}$ are indeed isomorphisms.



=--

+-- {: .num_defn #ModalObjects}
###### Definition
**([[modal objects]])**

Let $\mathcal{D}$ be a [[category]] (Def. \ref{Categories}).

For $\bigcirc$ a [[modal operator]] on $\mathcal{D}$ (Def. \ref{ModalOperator}), we say:

1. a _$\bigcirc$-[[modal object]]_ is an [[object]] $X \in \mathcal{D}$ such that the following conditions hold (which are all equivalent, by Prop. \ref{ModalOpIdempotent}):

   * it is in the $\bigcirc$-[[essential image]]: $X \in Im( \bigcirc ) \hookrightarrow \mathcal{D}$,

   * it is isomorphic to its own $\bigcirc$-[[image]]: $X \simeq \bigcirc X$,

   * specifically its $\bigcirc$-unit is an [[isomorphism]] $\eta_X \;\colon\; X \overset{\simeq}{\to} \bigcirc X$.

1. a _$\bigcirc$-[[modal object|submodal object]]_ is an [[object]] $X \in \mathcal{D}$, such that

   * its $\bigcirc$-unit is a [[monomorphism]] (Def. \ref{Monomorphism}): $\eta_X \;\colon\; X \hookrightarrow \bigcirc X$.

[[formal duality|Dually]] (Example \ref{OppositeCategory}):

For $\Box$ a [[comodal operator]] on $\mathcal{D}$ (Def. \ref{ModalOperator}), we say:

1. a _$\Box$-[[comodal object]]_ is an [[object]] $X \in \mathcal{D}$ such that the following conditions hold (which are all equivalent, by Prop. \ref{ModalOpIdempotent}):

   * it is in the $\Box$-[[essential image]]: $X \in Im( \Box ) \hookrightarrow \mathcal{D}$,

   * it is isomorphic to its own $\Box$-[[image]]: $\Box X \simeq X$,

   * specifically its $\Box$-counit is an [[isomorphism]] $\epsilon_X \;\colon\; \Box X \overset{\simeq}{\longrightarrow} X$

1. a _$\Box$-[[comodal object|supcomodal object]]_ is an [[object]] $X \in \mathcal{D}$, such that

   * its $\Box$-counit is an [[epimorphism]] (Def. \ref{Monomorphism}): $\epsilon_X \;\colon\; \Box X \overset{epi}{\longrightarrow} X$.


=--

+-- {: .num_defn #AdjointModality}
###### Definition
**([[adjoint modality]])**

Let 

$$
  L \;\dashv\; C \;\dashv\; R
  \;\colon\;
  \mathcal{C}
    \array{
      \overset{\phantom{A} L \phantom{A}}{\hookleftarrow}
      \\
      \overset{\phantom{A} C \phantom{A}}{\longrightarrow}
      \\
      \overset{\phantom{A} R \phantom{A}}{\hookleftarrow}
    }
  \mathcal{D}
$$ 

be an [[adjoint triple]] (Remark \ref{AdjointTriples}) such that $L$ and $R$ are [[fully faithful functors]] (necessarily both, by Prop. \ref{FullyFaithfulAdjointTriple}). By Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}, there are induced [[modal operators]]

$$
  \Box \;\coloneqq\; L \circ C
  \phantom{AA}
  \bigcirc \;\coloneqq\; R \circ C
$$

which themselves form am [[adjoint pair]]

$$
  \Box \;\dashv\; \bigcirc
  \,,
$$

hence called an _[[adjoint modality]]_. The [[adjunction unit]] and [[adjunction counit]] as in (eq:OppositeExtremesAdjointTriple) may now be read as exhibiting each object $X$ in the [[domain]] of $C$ as "in between the opposite extremes of its $\bigcirc$-modal aspect and its $\Box$-modal aspect"

$$
  \Box X
    \overset{\phantom{AA}\epsilon^\Box_X \phantom{AA}}{\longrightarrow}
  X
    \overset{\phantom{AA}\eta^{\bigcirc}_X\phantom{AA}}{\longrightarrow}
  \bigcirc X
  \,.
$$

A [[formal duality|formally dual]] situation (Example \ref{OppositeCategory}) arises when $C$ is [[fully faithful functor|fully faithful]].


$$
  L \;\dashv\; C \;\dashv\; R
  \;\colon\;
  \mathcal{C}
    \array{
      \overset{\phantom{A} L \phantom{A}}{\longrightarrow}
      \\
      \overset{\phantom{A} C \phantom{A}}{\hookleftarrow}
      \\
      \overset{\phantom{A} R \phantom{A}}{\longrightarrow}
    }
  \mathcal{D}
$$ 

with

$$
  \left(
    \bigcirc \;\coloneqq\; C \circ L
  \right)
  \;\dashv\;
  \left(
    \Box \;\coloneqq\; C \circ R
  \right)
$$

and canonical [[natural transformation]] between opposite extreme aspects given by

\[
   \label{OppositeExtrmeComparison}
   \Box X 
     \overset{ \phantom{AA} \epsilon^{\Box}_X \phantom{AA} }{\longrightarrow}
   X
    \overset{ \phantom{AA} \eta^{\bigcirc}_X \phantom{AA} }{\longrightarrow}
   \bigcirc X
\]

=--


+-- {: .num_prop #FullyFaithfulAdjointTriple}
###### Proposition
**([[fully faithful functor|fully faithful]] [[adjoint triple]])**

Let $L \dashv C \dashv R$ be an [[adjoint triple]] (Remark \ref{AdjointTriples}). Then the following are equivalent:

1. $L$ is a [[fully faithful functor]];

1. $R$ is a [[fully faithful functor]],

1. $(\Box \;\coloneqq\; L \circ C) \dashv (\bigcirc \;\coloneqq\; R \circ C)$ is an [[adjoint modality]] (Def. \ref{FullyFaithfulAdjointTriple}).


=--

For **proof** see [this prop.](adjoint+triple#FullyFaithful).



In order to analyze (in Prop. \ref{ComparisonMorphismBetweenOppositeExtremes}  below) the comparison morphism of opposite extreme aspects (eq:OppositeExtrmeComparison) induced by an [[adjoint modality]] (Def. \ref{AdjointModality}), we need the following technical Lemma:


+-- {: .num_lemma #CoincidenceOfTransformsForAdjointTriple}
###### Lemma

Let

$$
  \mathcal{C}
    \array{
      \overset{ \phantom{A} L \phantom{A} }{\longrightarrow}
      \\
      \overset{ \phantom{A} C \phantom{A} }{\hookleftarrow}
      \\
      \overset{ \phantom{A} R \phantom{A} }{ \longrightarrow }
    }
  \mathcal{D}
$$

be an [[adjoint triple]] with induced [[adjoint modality]] (Def. \ref{AdjointModality}) to be denoted

$$
  \left( \Box \;\coloneqq\; C \circ L\right)
  \;\dashv\;
  \left(
    \bigcirc \;\coloneqq\; C \circ R
  \right)
$$

Denoting the [[adjunction units]]/[[adjunction counit|counits]] (Def. \ref{AdjunctionUnitFromHomIsomorphism}) as

| $\phantom{A}$ [[adjunction]] $\phantom{A}$ | $\phantom{A}$ [[adjunction unit|unit]] $\phantom{A}$ | $\phantom{A}$ [[adjunction counit|counit]] $\phantom{A}$ |
|----------|-----------|----------|
| $\phantom{A}$ $(L \dashv C)$ $\phantom{A}$ | $\phantom{A}$  $\eta^{\bigcirc}$ $\phantom{A}$ | $\phantom{A}$ $\epsilon^{\bigcirc}$ $\phantom{A}$ |
| $\phantom{A}$ $(C \dashv R)$ $\phantom{A}$ | $\phantom{A}$ $\eta^\Box$ $\phantom{A}$ | $\phantom{A}$ $\epsilon^\Box$ $\phantom{A}$ |
{: style='margin:auto}

we have that the following [[composition|composites]] of unit/counit components are equal:

\[
  \label{CoincidenceOfNaturalTransformationsForAdjointTriple}
  \left(
    \eta^{\Box}_{L X}
  \right)
  \circ
  \left(
    L \epsilon^\Box_X
  \right)
  \;\;=\;\;
  \left(
    R \eta^{\bigcirc}_{X}
  \right)
  \circ
  \left(
    \epsilon^{\bigcirc}_{R X}
  \right)
  \phantom{AAAAAA}
  \array{
    L C R X
    &\overset{\epsilon^{\bigcirc}_{R X}}{\longrightarrow}&
    R X
    \\
    {}^{ \mathllap{ L \epsilon^\Box_X } }\big\downarrow
    &&
       \big\downarrow^{\mathrlap { R \eta^{\bigcirc}_{X} } }
    \\
    L X
    &\underset{ \eta^\Box_{L X} }{\longrightarrow}&
    R C L X
  }
\]

=--

([Johnstone 11, lemma 2.1](adjoint+quadruple#Johnstone11))

+-- {: .proof}
###### Proof

We claim that the following [[commuting diagram|diagram commutes]] (Def. \ref{CommutingDiagram}):

$$
  \array{
    && && R X
    \\
    && & {}^{ \epsilon^\bigcirc_{R X} }\nearrow
    && \searrow^{\mathrlap{ R \eta^{\bigcirc}_X }}
    \\
    && L C R X
    && && R C L X
    \\
    & {}^{ L \epsilon^\Box_X }\swarrow
    && \searrow^{ \mathrlap{ L C R \eta^{\bigcirc}_X } }
    && {}^{\mathllap{ \eta^{\bigcirc}_{R C L X} }}\nearrow
    && \nwarrow^{ \mathrlap{ \eta^{\Box}_{L X} } }
    \\
    L X
    && && L C R C L X
    && && L X
    \\
    & {}_{\mathllap{ L \eta^{\bigcirc}_X }}\searrow
    && {}^{\mathllap{iso}}\swarrow_{\mathrlap{ L \epsilon^{\Box}_{C L X} }}
    && {}_{\mathllap{ L C \eta^\Box_{L X} }}\nwarrow^{\mathrlap{iso}}
    && \nearrow_{\mathrlap{ \epsilon^{\bigcirc}_{L X} }}
    \\
    && L C L X
    && \underset{id_{L C L X}}{\longleftarrow}  &&
    L C L X
  }
$$

This commutes, because:

1. the left square is the image under $L$ of [[naturality square|naturality]] (eq:Naturality) for $\epsilon^\Box$ on $\eta^{\bigcirc}_X$;

1. the top square is [[naturality square|naturality]] (eq:Naturality) for $\epsilon^{\bigcirc}$ on $R \eta^{\bigcirc}_X$;

1. the right square is [[naturality square|naturality]] (eq:Naturality) for $\epsilon^{\bigcirc}$ on $\eta^{\Box}_{L X}$;

1. the bottom commuting triangle is the image under $L$ of the [[triangle identity]] (eq:TriangleIdentities) for $(C \dashv R)$ on $L X$.

Moreover, notice that

1. the total bottom composite is the [[identity morphism]] $id_{L X}$, due to the [[triangle identity]] (eq:TriangleIdentities) for $(C \dashv R)$;

1. also the other two morphisms in the bottom triangle are [[isomorphisms]], as shown, due to the [[idempotent monad|idempoency]] of the $(C-R)$-adjunction (Prop. \ref{ModalOpIdempotent}.)

Therefore the total composite from $L C R X \to R/ C L X$ along the bottom part of the diagram equals the left hand side of (eq:CoincidenceOfNaturalTransformationsForAdjointTriple), while the composite along the top part of the diagram clearly equals the right hand side of (eq:CoincidenceOfNaturalTransformationsForAdjointTriple).


=--


+-- {: .num_prop #ComparisonMorphismBetweenOppositeExtremes}
###### Proposition
**(comparison transformation between opposite extremes of [[adjoint modality]])**

Consider an [[adjoint triple]] of the form 

$$
  L \dashv C \dashv R 
  \;\;\colon\;\;
  \mathcal{C}
    \array{
      \overset{\phantom{AA} L \phantom{AA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} C \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AAA} R \phantom{AAA} }{\longrightarrow}
    }
  \mathcal{B}
$$

with induced [[adjoint modality]] (Def. \ref{AdjointModality}) to be denoted

$$
  \left( 
    \Box \;\coloneqq\; C \circ L 
  \right)
  \;\dashv\;
  \left(
    \bigcirc \;\coloneqq\; C \circ R 
  \right)
$$

Denoting the [[adjunction units]]/[[adjunction counit|counits]] (Def. \ref{AdjunctionUnitFromHomIsomorphism}) as

| $\phantom{A}$ [[adjunction]] $\phantom{A}$ | $\phantom{A}$ [[adjunction unit|unit]] $\phantom{A}$ | $\phantom{A}$ [[adjunction counit|counit]] $\phantom{A}$ |
|----------|-----------|----------|
| $\phantom{A}$ $(L \dashv C)$ $\phantom{A}$ | $\phantom{A}$  $\eta^{\bigcirc}$ $\phantom{A}$ | $\phantom{A}$ $\epsilon^{\bigcirc}$ $\phantom{A}$ |
| $\phantom{A}$ $(C \dashv E)$ $\phantom{A}$ | $\phantom{A}$ $\eta^\Box$ $\phantom{A}$ | $\phantom{A}$ $\epsilon^\Box$ $\phantom{A}$ |
{: style='margin:auto}


Then for all $X \in \mathcal{C}$ the following two [[natural transformations]], constructed from the [[adjunction units]]/[[adjunction counit|counits]] (Def. \ref{AdjunctionUnitFromHomIsomorphism}) and their [[inverse morphisms]] (using [[idempotent monad|idempotency]], Prop. \ref{ModalOpIdempotent}), are equal:

\[
  \label{PointsToPiecesInTheBase}
  comp_{\mathcal{B}}
  \;\;\coloneqq\;\;
  \left(
    L \epsilon^\Box_X
  \right)
  \circ
  \left(
    \eta^{\bigcirc}_{R X}
  \right)^{-1}
  \;\;=\;\;
  \left(
    \eta^\Box_{L X}
  \right)^{-1}
  \circ
  \left(
    \Gamma \eta^{\bigcirc}_X
  \right)
  \phantom{AAAAAAA}
  \array{
    R X 
    & \overset{
       \Gamma \eta^{\bigcirc}_X
   }{\longrightarrow} & 
   R C L X
   \\
   {}^{ \mathllap{
      \left(
       \eta^{\bigcirc}_{R X}
     \right)^{-1}    
   } }\big\downarrow 
     & \searrow^{ { comp_{\mathcal{B}} }  } & 
   \big\downarrow^{ \mathrlap{  
     \left(
       \eta^\Box_{L X}
     \right)^{-1}
   } }
   \\ 
   L C R X
   &\underset{ 
    L \epsilon^\Box_X
    }{\longrightarrow}&
   L X
  }
\]

Moreover, the image of these morphisms under $C$ equals the following composite:

\[
  \label{PointsToPieces}
  comp_{\mathcal{C}}
  \;\colon\;
  \Box X 
    \overset{ \phantom{A} \epsilon^{\Box}_X \phantom{A} }{\longrightarrow}
  X
    \overset{ \phantom{A} \eta^{\bigcirc}_X \phantom{A} }{\longrightarrow}
  \bigcirc X
  \,,
\]

hence

\[
  \label{PiecesToPointsFromBase}
  comp_{\mathcal{C}} \;=\; C(comp_{\mathcal{B}})
  \,.
\]

=--


+-- {: .proof}
###### Proof

The first statement follows directly from Lemma \ref{CoincidenceOfTransformsForAdjointTriple}.

For the second statement, notice that the $(C \dashv R)$-[[adjunct]] (Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}) of

$$
  comp_{\mathcal{C}}
    \;\colon\;
  C R X 
    \overset{ \phantom{A} \epsilon^{\Box}_X \phantom{A} }{\longrightarrow}
  X
    \overset{ \phantom{A} \eta^{\bigcirc}_X \phantom{A} }{\longrightarrow}
  C L X
$$

is

\[
  \label{AdjunctOfptpH}
  \widetilde{ comp_{\mathcal{C}} }
  \;\;=\;\;
  \underset{
    = id_{R X}
  }{
  \underbrace{
    \Gamma X
      \underoverset{iso}{ \phantom{A} \eta^{\Box}_{R X} \phantom{A} }{ \longrightarrow }
    R C R X 
      \underoverset{iso}{ \phantom{A} \Gamma \epsilon^{\Box}_X \phantom{A} }{\longrightarrow}
    R X
  }}
      \overset{ \phantom{A} R \eta^{\bigcirc}_X \phantom{A}  }{\longrightarrow}
    R C L X
  \,,
\]

where under the braces we uses the [[triangle identity]] (Prop. \ref{AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat}). 

(As a side remark, for later usage, we observe that the morphisms on the left in (eq:AdjunctOfptpH) are [[isomorphisms]], as shown, by [[idempotent monad|idempotency]] of the adjunctions.)  

From this we obtain the following [[commuting diagram]]:

$$
  \array{
    C R X
      &\overset{ \phantom{A} C R \eta^{\bigcirc}_X \phantom{A} }{\longrightarrow}&
    C R C L X
      &\underoverset{iso}{ \phantom{A} C \left(\eta^{ \Box }_{L X}\right)^{-1} \phantom{A} }{ \longrightarrow }&
    C L X
    \\
    &{}_{\mathllap{ comp_{\mathcal{C}} }}\searrow&
    {}^{ \mathllap{ \epsilon^{\Box}_{C L X} } }
    \big\downarrow^{\mathrlap{\simeq}}
     & 
    \nearrow_{\mathrlap{id_{L X}}}
    \\
    && C L X
  }
$$

Here:

1. on the left we identified $\widetilde {\widetilde {comp_{\mathcal{C}}}} \;=\;  comp_{\mathcal{C}}$ by applying the formula (Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}) for $(C \dashv R)$-[[adjuncts]] to $\widetilde {comp_{\mathcal{C}}} = R \eta^{\bigcirc}_X$ (eq:AdjunctOfptpH);

1. on the right we used the [[triangle identity]] (Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}) for $(C \dashv R)$.

This proves the second statement.

=--



+-- {: .num_defn #PreorderOnModalities}
###### Definition
**([[preorder]] on [[modalities]])**

Let $\bigcirc_1$ and $\bigcirc_2$ be two [[modal operators]] on a [[category]] $\mathcal{C}$. By Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories} these are equivalently characterized by their [[reflective subcategory|reflective]] [[full subcategories]] $\mathcal{C}_{\bigcirc_1}, \mathcal{C}_{\bigcirc}_2 \hookrightarrow \mathcal{C}$ of [[modal objects]].

There is an evident [[preorder]] on [[full subcategories]] of $\mathcal{C}$, given by full inclusions of full subcategories into each other. We write $\mathcal{C}_{\bigcirc_1} \subset \mathcal{C}_{\bigcirc_2}$ if the full subcategory on the left is contained, as a full subcategory of $\mathcal{C}$, in that on the right. Via prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories} there is the induced [[preorder]] on [[modal operators]], and we write

$$
  \bigcirc_1
  \;\lt\;
  \bigcirc_2
  \phantom{AA}
  iff
  \phantom{AA}
  \mathcal{C}_{\bigcirc_1}
  \;\subset\;
  \mathcal{C}_{\bigcirc_2}
  \,.
$$

There is an analogous [[preorder]] on [[comodal operators]] (Def. \ref{ModalOperator}).

If we have two [[adjoint modalities]] (Def. \ref{AdjointModality}) of the same type (both modal left adjoint or both comodal left adjoint) such that both the modalities and the comodalities are compatibly ordered in this way, we denote this situation as follows:

$$
  \array{
    \bigcirc_2 &\dashv& \Box_2
    \\
    \vee && \vee
    \\
    \bigcirc_1 &\dashv& \Box_1
  }
  \phantom{AAAA} \text{or} \phantom{AAAA}
  \array{
    \Box_2 &\dashv& \bigcirc_2
    \\
    \vee && \vee
    \\
    \Box_1 &\dashv& \bigcirc_1
  }
$$

etc.

=--

+-- {: .num_example #InitialAndFinalAdjointModality}
###### Example
**([[bottom]] and [[top]] [[adjoint modality]])**

Let $\mathcal{C}$ be a [[category]] with both an [[initial object]] $\emptyset$ and a [[terminal object]] $\ast$ (Def. \ref{InitialObject}). Then, by Example \ref{InitialAndTerminalObjectInTermsOfAdjunction} there is an [[adjoint triple]] between $\mathcal{C}$ and the [[terminal category]] $\ast$ (Example \ref{InitialCategoryAndTerminalCategory}) of the form

$$
  \mathcal{C}
    \array{
      \overset{ \phantom{A} const_\emptyset \phantom{A} }{\hookleftarrow}
      \\
      \overset{\phantom{AAAA}}{\longrightarrow}
      \\
      \overset{ \phantom{A} const_\ast \phantom{A} }{\hookleftarrow}
    }
  \ast
  \,.
$$

The induced [[adjoint modality]] (Def. \ref{AdjointModality}) is

$$
  const_{\emptyset}
  \;\dashv\;
  const_\ast
  \;\;\colon\;\;
  \mathcal{C} \to \mathcal{C}
  \,.
$$

By slight abuse of notation, we will also write this as

\[
  \label{BottomAdjointModality}
  \emptyset
    \;\dashv\;
  \ast
  \;\;\colon\;\;
  \mathcal{C} \to \mathcal{C}
  \,.
\]

On the other extreme, for $\mathcal{C}$ any [[category]] whatsoever, the [[identity]] functor on it is [[adjoint functor]] to itself, and constitutes an [[adjoint modality]] (Def. \ref{AdjointModality})

\[
  \label{AdjointModalityTop}
  id_{\mathcal{C}}
  \;\dashv\;
  id_{\mathcal{C}}
  \;\;\colon\;\;
  \mathcal{C} \to \mathcal{C}
  \,.
\]


Here

1. (eq:BottomAdjointModality) is the _[[bottom]]_ (or _ground_)

2. (eq:AdjointModalityTop) is the _[[top]]_

in the [[preorder]] on [[adjoint modalities]] according to Def. \ref{PreorderOnModalities}, in that for every [[adjoint modality]] of the form $\bigcirc \dashv \Box$ we have the following:

$$
  \array{
    id &\dashv& id
    \\
    \vee && \vee
    \\
    \Box &\dashv& \bigcirc
    \\
    \vee && \vee
    \\
    \emptyset &\dashv& \ast
  }
$$



=--

+-- {: .num_defn #Aufhebung}
###### Definition
**([[Aufhebung]])**

On some [[category]] $\mathcal{C}$, consider an inclusion of [[adjoint modalities]], according to Def. \ref{PreorderOnModalities}:

$$
  \array{
    \Box_2 &\dashv& \bigcirc_2
    \\
    \vee && \vee
    \\
    \Box_1 &\dashv& \bigcirc_1
  }
$$

We say:

1. This provides _right [[Aufhebung]] of the opposition_ exhibited by $\Box_1 \dashv \bigcirc_1$ if there is also the diagonal inclusion

   $$
     \Box_1 \lt \bigcirc_2
     \phantom{AAA}
     equivalently
     \phantom{AAA}
     \mathcal{C}_{\Box_1}
     \subset
     \mathcal{C}_{\bigcirc_2}
   $$

   We indicate this situation by
 
   $$
     \array{
       \Box_2 &\dashv& \bigcirc_2
       \\
       \vee &/& \vee
       \\
       \Box_1 &\dashv& \bigcirc_1
     }
   $$


1. This provides _left [[Aufhebung]] of the opposition_ exhibited by $\Box_1 \dashv \bigcirc_1$ if there is also the diagonal inclusion

   $$
     \bigcirc_1 \lt \Box_2
     \phantom{AAA}
     equivalently
     \phantom{AAA}
     \mathcal{C}_{\bigcirc_1}
     \subset
     \mathcal{C}_{\Box_2}
   $$

   We indicate this situation by
 
   $$
     \array{
       \Box_2 &\dashv& \bigcirc_2
       \\
       \vee &\backslash& \vee
       \\
       \Box_1 &\dashv& \bigcirc_1
     }
   $$


=--

+-- {: .num_remark #TrivialAufhebung}
###### Remark

For a progression of [[adjoint modalities]] of the form

$$
   \array{
     \bigcirc_2 &\dashv& \Box_2
     \\
     \vee && \vee
     \\
     \bigcirc_1 &\dashv& \Box_1
   }
$$

the analog of [[Aufhebung]] (Def. \ref{Aufhebung}) is automatic, since, by Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}, in this situation the [[full subcategories]] [[modal objects]] at each stage coincide already.

For emphasis we may denote this situation by

$$
   \array{
     \bigcirc_2 &\dashv& \Box_2
     \\
     \vee &\vert& \vee
     \\
     \bigcirc_1 &\dashv& \Box_1
   }
  \,.
$$


=--



+-- {: .num_example}
###### Example
**([[top]] [[adjoint modality]] provides [[Aufhebung]] of all oppositions)**

For $\mathcal{C}$ any [[category]], the [[top]] [[adjoint modality]] $id \dashv id$ (Def. \ref{InitialAndFinalAdjointModality}) provides [[Aufhebung]] (Def. \ref{Aufhebung}) of every other [[adjoint modality]].

=--

But already [[Aufhebung]] of the [[bottom]] [[adjoint modality]] is a non-trivial and interesting condition. We consider this below in Prop. \ref{PiecesHavePoints}.



$\,$

We now re-consider the concept of [[reflective subcategories]] from the point of view of [[localization of categories]]:

+-- {: .num_defn #CategoryWithWeakEquivalences}
###### Definition
**([[category with weak equivalences]])**

A _[[category with weak equivalences]]_ is

1. a [[category]] $\mathcal{C}$ (Def. \ref{Categories})

1. a [[subcategory]] $W \subset \mathcal{C}$ (i.e. sub-class of objects and morphisms that inherits the structure of a [[category]])

such that the [[morphisms]] in $W$

1. include all the [[isomorphisms]] of $\mathcal{C}$,

1. satisfy _[[two-out-of-three]]_:

   If for $g$, $f$ any two [[composition|composable]] [[morphisms]] in $\mathcal{C}$, two out of the set $\{g,\, f,\, g \circ f \}$ are in $W$, then so is the third.

   $$
     \array{
       & {}^{\mathllap{f}}\nearrow && \searrow^{\mathrlap{g}}
       \\
       && \underset{ g \circ f }{\longrightarrow}
     }
   $$

=--

+-- {: .num_defn #LocalizationOfACategory}
###### Definition
**([[localization of a category]])**

Let $W \subset \mathcal{C}$ be a [[category with weak equivalences]] (Def. \ref{CategoryWithWeakEquivalences}). Then the _[[localization of a category|localization]]_ of $\mathcal{C}$ at $W$ is, if it exsists

1. a [[category]] $\mathcal{C}[W^{-1}]$,

1. a [[functor]] $\gamma \;\colon\; \mathcal{C} \longrightarrow \mathcal{C}[W^{-1}]$ (Def. \ref{Functors})

such that

1. $\gamma$ sends all morphisms in $W \subset \mathcal{C}$ to [[isomorphisms]] (Def. \ref{Isomorphism}),

1. $\gamma$ is [[universal property|universal with this property]]: If $F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ is any functor with this property, then it factors through $\gamma$, up to [[natural isomorphism]] (Def. \ref{NaturalTransformations}):

   $$
     F \;\simeq\;
     D F \circ \gamma
     \phantom{AAAAAAA}
     \array{
       \mathcal{C}
         && \overset{F}{\longrightarrow} &&
       \mathcal{D}
       \\
       & {}_{\mathllap{\gamma}}\searrow
         &{}^{\rho}\Downarrow_{\simeq}&
       \nearrow_{\mathrlap{D F}}
       \\
       && \mathcal{C}[W^{-1}]
     }
   $$

   and any two such factorizations $D F$ and $D^' F$ are related by a unique [[natural isomorphism]] $\kappa$ compatible with $\rho$ and $\rho^'$:

\[
  \label{CompatibleNaturalIsoForLocalization}
     \array{
       \mathcal{C}
         && \overset{F}{\longrightarrow} &&
       \mathcal{D}
       \\
       &
       {}_{\mathllap{\gamma}}\searrow
         &{}^{\rho}\Downarrow_{\simeq}&
       \nearrow_{\mathrlap{D F}}
       && \searrow^{\mathrlap{id}}
       \\
       && \mathcal{C}[W^{-1}]
       && {}_{\simeq}\seArrow^{\kappa} && \mathcal{D}
       \\
       && &  {}_{\mathllap{id}}\searrow && \swarrow_{\mathrlap{D^' F}}
       \\
       && && \mathcal{C}[W^{-1}]
     }
     \phantom{AAAA}
     =
     \phantom{AAAA}
     \array{
       \mathcal{C}
         && \overset{F}{\longrightarrow} &&
       \mathcal{D}
       \\
       & {}_{\mathllap{\gamma}}\searrow
         &{}^{\rho^'}\Downarrow_{\simeq}&
       \nearrow_{\mathrlap{D^' F}}
       \\
       && \mathcal{C}[W^{-1}]
     }
\]

Such a localization is called a _[[reflective localization]]_ if the localization functor has a [[fully faithful functor|fully faithful]] [[right adjoint]], exhibiting it as the reflection functor of a [[reflective subcategory]]-inclusion (Def. \ref{ReflectiveSubcategory})

$$
  \mathcal{C}[W^{-1}]
  \underoverset
    {\underset{\phantom{AAAA}}{\hookrightarrow}}
    {\overset{ \phantom{AA} \gamma \phantom{AA} }{\longleftarrow}}
    {\bot}
  \mathcal{C}
  \,.
$$

=--


+-- {: .num_prop #ReflectiveSubcategoriesAreLocalizations}
###### Proposition
**([[reflective subcategories]] are [[localizations]])**

Every [[reflective subcategory]]-inclusion (Def. \ref{ReflectiveSubcategory})

$$
  \mathcal{C}_{L}
  \underoverset
    {\underset{\phantom{AA}\iota \phantom{AA}}{\hookrightarrow}}
    {\overset{ \phantom{AA} L \phantom{AA} }{\longleftarrow}}
    {\bot}
  \mathcal{C}
$$

is [[generalized the|the]] [[reflective localization]] (Def. \ref{LocalizationOfACategory}) at the class $W \coloneqq L^{-1}(Isos)$ of morphisms that are sent to isomorphisms by the reflector $L$.

=--

+-- {: .proof}
###### Proof

Let $F \;\colon\; \mathcal{C} \to \mathcal{D}$ be a [[functor]] which inverts morphisms that are inverted by $L$.

First we need to show that it factors through $L$, up to natural isomorphism. But consider the following [[whiskering]] of the [[adjunction unit]] $\eta$ (Def. \ref{AdjunctionUnitFromHomIsomorphism}) with $F$:

$$
  \array{
    \mathcal{C}
    && \overset{F}{\longrightarrow} &&
    \mathcal{D}
    \\
    & {}_{\mathllap{L}}\searrow &\Downarrow& \nearrow_{\mathrlap{D F}}
    \\
    && \mathcal{C}_L
  }
  \phantom{AA} \coloneqq \phantom{AA}
  \array{
    \mathcal{C}
      && \overset{id}{\longrightarrow} &&
    \mathcal{C}
      & \overset{F}{\longrightarrow}&
    \mathcal{D}
    \\
    & {}_{\mathllap{L}}\searrow &\Downarrow^{\eta}& \nearrow_{\mathrlap{\iota}}
    \\
    && \mathcal{C}_L
  }
$$

By [[idempotent monad|idempotency]] (Prop. \ref{ModalOpIdempotent}), the components of the [[adjunction unit]] $\eta$ are inverted by $L$, and hence by assumption they are also inverted by $F$, so that on the right the [[natural transformation]] $F(\eta)$ is indeed a [[natural isomorphism]].

It remains to show that this factorization is unique up to unique natural isomorphism. So consider any other factorization $D^' F$ via a natural isomorphism $\rho$. [[pasting|Pasting]] this now with the [[adjunction counit]]

$$
  \array{
    &&
    \mathcal{C} && \overset{F}{\longrightarrow} &&  \mathcal{D}
    \\
    &
    {}^{\mathllap{\iota}}\nearrow
    &
    {}^{\epsilon}\Downarrow
    & {}_{\mathllap{L}}\searrow
    &\Downarrow^{\rho}& \nearrow_{\mathrlap{D^' F}}
    \\
    \mathcal{C}_L
    &&
      \underset{ id }{\longrightarrow}
    &&
    \mathcal{C}_L
  }
$$

exhibits a natural isomorphism $\epsilon \cdot \rho$ between $D F \simeq D^' F$. Moreover, this is compatible with $F(\eta)$ according to (eq:CompatibleNaturalIsoForLocalization), due to the [[triangle identity]] (Prop. \ref{AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat}):

$$
  \array{
    \mathcal{C}
    &&
     \overset{id}{\longrightarrow}
    &&
    \mathcal{C} && \overset{F}{\longrightarrow} &&  \mathcal{D}
    \\
    &
      {}_{\mathllap{id}}\searrow
    &
    {}^{\mathllap{\eta}}\Downarrow
    &
    {}^{\mathllap{\iota}}\nearrow
    &
    {}^{\epsilon}\Downarrow
    & {}_{\mathllap{L}}\searrow
    &\Downarrow^{\rho}& \nearrow_{\mathrlap{D^' F}}
    \\
    &&
    \mathcal{C}_L
    &&
      \underset{ id }{\longrightarrow}
    &&
    \mathcal{C}_L
  }
  \phantom{AAAA}
  =
  \phantom{AAAA}
  \array{
    \mathcal{C} && \overset{F}{\longrightarrow} &&  \mathcal{D}
    \\
    & \searrow &\Downarrow^\rho& \swarrow
    \\
    && \mathcal{C}_L
  }
$$

Finally, since $L$ is [[essentially surjective functor]], by [[idempotent monad|idempotency]] (Prop. \ref{AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat}), it is clear that this is the unique such natural isomorphism.

=--

+-- {: .num_defn #LocalObjects}
###### Definition
**([[local object]])**


Let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}) and let $S \subset Mor_{\mathcal{C}}$ be a set of [[morphisms]]. Then an [[object]] $X \in \mathcal{C}$ is called an _$S$-[[local object]]_ if for all $A \overset{s}{\to} B \; \in S$ the [[hom-functor]] (Def. \ref{HomFunctor}) from $s$ into $X$ yields a [[bijection]]

$$
  Hom_{\mathcal{C}}(s,X)
  \;\colon\;
  Hom_{\mathcal{C}}(B,X)
   \overset{ \phantom{AA} \simeq \phantom{AA} }{\longrightarrow}
  Hom_{\mathcal{C}}(A,X)
  \,,
$$

hence if every morphism $A \overset{f}{\longrightarrow} X$ [[extension|extends]] uniquely along $w$ to $B$:

$$
  \array{
    A &\overset{\phantom{A}f\phantom{A}}{\longrightarrow}& X
    \\
    {}^{\mathllap{w}}\big\downarrow & \nearrow_{\mathrlap{ \exists! }}
    \\
    B
  }
$$

We write 

\[
  \label{FullSubcategoryOfSLocalObjects}
  \mathcal{C}_S
  \overset{\phantom{AA}\iota\phantom{AA}}{\hookrightarrow}
  \mathcal{C}
\]

for the [[full subcategory]] (Example \ref{FullSubcategoryOnClassOfObjects}) of $S$-local objects.

=--


+-- {: .num_defn #LocalizationAtACollectionOfMorphisms}
###### Definition
**([[reflective subcategory|reflection]] onto [[full subcategory]] of [[local objects]])**

Let $\mathcal{C}$ be a [[category]] and set $S \subset Mor_{\mathcal{C}}$ be a sub-[[class]] of its [[morphisms]]. Then the _reflection onto local $S$-objects_ (often just called "localization at the collection $S$" is, if it exists, a [[left adjoint]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) $L$ to the [[full subcategory]]-inclusion of the $S$-[[local objects]] (eq:FullSubcategoryOfSLocalObjects):

$$
  \mathcal{C}_S
    \underoverset
      {\underset{\iota}{\hookrightarrow}}
      {\overset{\phantom{AA}L\phantom{AA}}{\longleftarrow}}
      {\bot}
  \mathcal{C}
  \,.
$$

=--

A class of examples is the following, which comes to its full nature (only) after passage to [[homotopy theory]] (Example \ref{HomotopyLocalizationOfCombinatorialModelCategories} below):

+-- {: .num_defn #HomotopyLocalizationOn1Categories}
###### Definition
**([[homotopy localization]] of [[1-categories]])**

Let $\mathcal{C}$ be a [[category]], let $\mathbb{A} \in \mathcal{C}$ be an [[object]], and consider the class of [[morphisms]] given by [[projection]] out of the [[Cartesian product]] with $\mathbb{A}$, of all objects $X \in \mathcal{C}$:

$$
  X \times \mathbb{A} 
    \overset{p_1}{\longrightarrow}
  X
  \,.
$$

If the corresponding [[reflective subcategory|reflection]] onto the [[full subcategory]] of [[local objects]] (Def. \ref{LocalizationAtACollectionOfMorphisms}) exists, we say this is _[[homotopy localization]]_ at that object , and denote the [[modal operator]] corresponding to this (via Prop. \ref{ModalOperatorsEquivalentToReflectiveSubcategories}) by

$$
  \bigcirc\!\!\!\!\!\!\!\!\mathbb{A}
  \;\colon\;
  \mathcal{C}
  \longrightarrow 
  \mathcal{C}
  \,.
$$


=--


+-- {: .num_prop #ReflectiveLocalizationGivenByLocalObjects}
###### Proposition
**([[reflective localization]] [[reflective subcategory|reflects]] onto [[full subcategory]] of [[local objects]])**


Let $W \subset \mathcal{C}$ be a [[category with weak equivalences]] (Def. \ref{CategoryWithWeakEquivalences}). If its [[reflective localization]] (Def. \ref{LocalizationOfACategory}) exists

$$
  \mathcal{C}[W^{-1}]
    \underoverset
      {\underset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}}
      {\overset{ \phantom{AA} L \phantom{AA} }{\longleftarrow}}
      {\bot}
  \mathcal{C}
$$

then $\mathcal{C}[W^{-1}] \overset{\iota}{\hookrightarrow} \mathcal{C}$ is [[equivalence of categories|equivalently]] the inclusion of the [[full subcategory]] (Example \ref{FullSubcategoryOnClassOfObjects}) on the $W$-[[local objects]] (Def. \ref{LocalObjects}), and hence $L$ is equivalently reflection onto the $W$-local objects, according to Def. \ref{LocalizationAtACollectionOfMorphisms}.

=--

+-- {: .proof}
###### Proof

We need to show that 

1. every $X \in \mathcal{C}[W^{-1}] \overset{\iota}{\hookrightarrow} \mathcal{C}$ is $W$-[[local object|local]], 

1. every $Y \in \mathcal{C}$ is $W$-[[local object|local]] precisely if it is [[isomorphism|isomorphic]] to an object in $\mathcal{C}[W^{-1}] \overset{\iota}{\hookrightarrow} \mathcal{C}$.

The first statement follows directly with the [[adjoint functor|adjunction isomorphism]] (eq:HomIsomorphismForAdjointFunctors):

$$
  Hom_{\mathcal{C}}(w, \iota(X))
    \simeq
  Hom_{\mathcal{C}[W^{-1}]}(L(w), X)
$$

and the fact that the [[hom-functor]] takes [[isomorphisms]] to [[bijections]] (Example \ref{YonedaCharacterizationOfIsomorphism}).

For the second statement, consider the case that $Y$ is $W$-local. Observe that then $Y$ is also local with respect to the class 

$$
  W_{sat} \;\coloneqq\; L^{-1}(Isos)
$$ 

of _all_ morphisms that are inverted by $L$ (the "[[saturated class of morphisms]]"): For consider the [[hom-functor]] $\mathcal{C} \overset{Hom_{\mathcal{C}}(-,Y)}{\longrightarrow} Set^{op}$ to the [[opposite category|opposite]] of the [[category of sets]]. By assumption on $Y$ this takes elements in $W$ to isomorphisms. Hence, by the defining [[universal property]] of the [[localization]]-functor $L$, it factors through $L$, up to [[natural isomorphism]]. 

Since, by [[idempotent monad|idempotency]] (Prop. \ref{ModalOpIdempotent}),  the [[adjunction unit]] $\eta_Y$ is in $W_{sat}$, this implies that we have a [[bijection]] of the form

$$
  Hom_{\mathcal{C}}( \eta_Y, Y )
  \;\colon\;
  Hom_{\mathcal{C}}( \iota L(Y), Y )
    \overset{\simeq}{\longrightarrow}
  Hom_{\mathcal{C}}(Y, Y)
  \,.
$$

In particular the [[identity morphism]] $id_Y$ has a [[preimage]] $\eta_Y^{-1}$ under this function, hence a [[left inverse]] to $\eta$:

$$
  \eta_Y^{-1} \circ \eta_Y \;=\; id_Y
  \,.
$$

But by [[2-out-of-3]] this implies that $\eta_Y^{-1} \in W_{sat}$. Since the first item above shows that $\iota L(Y)$ is $W_{sat}$-local, this allows to apply this same kind of argument again, 


$$
  Hom_{\mathcal{C}}( \eta^{-1}_Y, \iota L(Y) )
    \;\colon\;
  Hom_{\mathcal{C}}( Y, \iota L(Y) )
    \overset{\simeq}{\longrightarrow}
  Hom_{\mathcal{C}}( \iota L(Y) , \iota L(Y))
  \,,
$$

to deduce that also $\eta_Y^{-1}$ has a [[left inverse]] $(\eta_Y^{-1})^{-1} \circ \eta_Y^{-1}$. But since a [[left inverse]] that itself has a [[left inverse]] is in fact an [[inverse morphisms]] ([this Lemma](retract#LeftInverseWithLeftInverseIsLeftInverse)), this means that $\eta^{-1}_Y$ is an [[inverse morphism]] to $\eta_Y$, hence that $\eta_Y \;\colon\; Y \to \iota L (Y)$ is an [[isomorphism]] and hence that $Y$ is isomorphic to an object in $\mathcal{C}[W^{-1}] \overset{\iota}{\hookrightarrow} \mathcal{C}$.

Conversely, if there is an [[isomorphism]] from $Y$ to a morphism in the image of $\iota$ hence, by the first item, to a $W$-local object, it follows immediatly that also $Y$ is $W$-local, since the [[hom-functor]] takes [[isomorphisms]] to [[bijections]] and since bijections satisfy [[2-out-of-3]].

=--


+-- {: .num_prop #ReflectionOntoLocalObjectsIsLocalizationWithRespectToLeftAdjoints}
###### Proposition
**([[reflective subcategory|reflection]] onto [[local objects]] is [[localization]] with respect to [[left adjoints]])**

Let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}) and let $S \subset Mor_{\mathcal{C}}$ be a [[class]] of [[morphisms]] in $\mathcal{C}$. Then the [[reflective subcategory|reflection]] onto the $S$-[[local objects]] (Def. \ref{LocalizationAtACollectionOfMorphisms}) 
satisfies, if it exists, the [[universal property]] of a [[localization of categories]] (Def. \ref{LocalizationOfACategory}) with respect to _[[left adjoint]]_ functors inverting $S$.

=--

+-- {: .proof}
###### Proof

Write

$$
  \mathcal{C}_S 
    \underoverset
      {\underset{ \phantom{AA}\iota\phantom{AA} }{\hookrightarrow}}
      {\overset{\phantom{AA}L\phantom{AA}}{\longleftarrow}}
      {\bot}
  \mathcal{C}
$$

for the [[reflective subcategory]]-inclusion of the $S$-[[local objects]].

Say that a [[morphism]] $f$ in $\mathcal{C}$ is an _$S$-[[local morphism]]_ if for every $S$-[[local object]] $A \in \mathcal{C}$ the [[hom-functor]] (Example \ref{HomFunctor}) from $f$ to $A$ yields a [[bijection]] $Hom_{\mathcal{C}}(f,A)$.
Notice that, by the [[Yoneda embedding]] for $\mathcal{C}_S$ (Prop. \ref{YonedaEmbedding}), the $S$-[[local morphisms]] are precisely the morphisms that are taken to isomorphisms by the reflector $L$ (via Example \ref{YonedaCharacterizationOfIsomorphism}).

Now let 

$$
  (F \dashv G)
  \;\colon\;
  \mathcal{C} 
    \underoverset
      {\underset{G}{\longleftarrow}}
      {\overset{ \phantom{AA} F \phantom{AA} }{\longrightarrow}}
      {\bot}
   \mathcal{D}
$$

be a pair of [[adjoint functors]], such that the [[left adjoint]] $F$ inverts the morphisms in $S$. By the adjunction hom-isomorphism (eq:HomIsomorphismForAdjointFunctors) it follows that $G$ takes values in $S$-[[local objects]]. This in turn implies, now via the [[Yoneda embedding]] for $\mathcal{D}$, that $F$ inverts all $S$-[[local morphisms]], and hence all morphisms that are inverted by $L$. 

Thus the essentially unique factorization of $F$ through $L$ now follows by Prop. \ref{ReflectiveSubcategoriesAreLocalizations}.

=--

