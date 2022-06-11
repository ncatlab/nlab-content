
## Universal constructions
 {#UniversalConstructions}

What makes [[category theory]] be _theory_, as opposed to just a language, is the concept of _[[universal constructions]]_. This refers to the idea of [[objects]] with a prescribed [[property]] which are _universal_ with this property, in that they "know about" or "subsume" every other object with that same kind of property. Category theory allows to make precise what this means, and then to discover and prove theorems about it.

Universal constructions are all over the place in [[mathematics]]. Iteratively finding the universal constructions in a prescribed situation essentially amounts to systematically following the unravelling of the given situation or problem or theory that one is studying.

There are several different formulations of the concept of [[universal constructions]], discussed below:

* _[Limits and colimits](#LimitsAndColimits)_

* _[Ends and coends](#TopologicalEndsAndCoends)_

* _[Left and right Kan extensions](#KanExtension)_

But these three kinds of constructions all turn out to be special cases of each other, hence they really reflect different perspectives on a single topic of universal constructions. In fact, all three are also special cases of the concept of _[[adjunction]]_ (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}), thus re-amplifying that [[category]] theory is really the theory of [[adjunctions]] and hence, if we follow ([Lambek 82](adjoint+functor#Lambek82)), of [[duality]].

$\,$


### Limits and colimits
 {#LimitsAndColimits}

Maybe the most hands-on version of [[universal constructions]] are _[[limits]]_ (Def. \ref{Limits} below), which is short for _limiting [[cones]]_ (Remark \ref{LimitingCones} below). The [[formal duality|formally dual]] concept (Example \ref{OppositeCategory}) is called _[[colimits]]_ (which are hence [[limits]] in an [[opposite category]]). Other terminology is in use, too:

| $\phantom{A}$ $\underset{\longleftarrow}{\lim}$ $\phantom{A}$ | $\phantom{A}$ $\underset{\longrightarrow}{\lim}$ $\phantom{A}$ |
|-----------|---------------|
| $\phantom{A}$ [[limit]] $\phantom{A}$ | $\phantom{A}$ [[colimit]] $\phantom{A}$ |
| $\phantom{A}$ [[inverse limit]] $\phantom{A}$ | $\phantom{A}$ [[direct limit]]$\phantom{A}$  |
{: style='margin:auto'}

There is a variety of different kinds of [[limits]]/[[colimits]], depending on the [[diagram]] shape that they are limiting (co-)cones over. This includes [[universal constructions]] known as _[[equalizers]]_, _[[products]]_, _[[fiber products]]/[[pullbacks]]_, _[[filtered limits]]_ and various others, all of which are basic tools frequently used whenever [[category theory]] applies.

A key fact of [[category theory]], regarding [[limits]], is that [[right adjoints preserve limits]] and [[left adjoints preserve colimits]] (Prop. \ref{AdjointsPreserveCoLimits} below). This will be used all the time. A partial converse to this statement is that if a [[functor]] preserves [[limits]]/[[colimits]], then its [[adjoint functor]] is, if it exists, objectwise given by a [[limit]]/[[colimit]] over a [[comma category]] under/over the given functor (Prop. \ref{PointwiseExpressionOfLeftAdjoints} below). Since these [[comma categories]] are in general not [[small categories|small]], this involves set-theoretic size subtleties that are dealt with by the _[[adjoint functor theorem]]_ (Remark \ref{AdjointFunctorTheorem} below). We discuss in detail a very special but also very useful special case of this in Prop. \ref{TopologicalLeftKanExtensionBCoend}, further below.

$\,$


+-- {: .num_defn #Limits}
###### Definition
**([[limit]] and [[colimit]])**

Let $\mathcal{C}$ be a [[small category]] (Def. \ref{SmallCategory}), and let $\mathcal{D}$ be any [[category]] (Def. \ref{Categories}). In this case one also says that a [[functor]]

$$
  F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
$$

is a _[[diagram]] of shape $\mathcal{C}$ in $\mathcal{D}$_.

Recalling the [[functor category]] (Example \ref{FunctorCategory}) $[\mathcal{C}, \mathcal{D}]$, there is the _[[constant diagram]]-functor_

$$
  const
  \;\colon\;
  \mathcal{D}
  \longrightarrow
  [\mathcal{C}, \mathcal{D}]
$$

which sends an [[object]] $X \in \mathcal{D}$ to the [[functor]] that sends every $c \in \mathcal{C}$ to $X$, and every [[morphism]] in $\mathcal{C}$ to the [[identity morphism]] on $X$. Accordingly, every morphism in $\mathcal{D}$ is sent by $const$ to the [[natural transformation]] (Def. \ref{NaturalTransformations}) all whose components are equal to that morphism.

Now:

1. if $const$ has a [[right adjoint]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}), this is called the construction of forming the _limiting [[cone]] of $\mathcal{C}$-shaped diagrams in $\mathcal{D}$_, or just _[[limit]]_ (or _[[inverse limit]]_) for short, and denoted

   $$
     \underset{\underset{\mathcal{C}}{\longleftarrow}}{\lim}
     \;\colon\;
     [\mathcal{C}, \mathcal{D}] \longrightarrow \mathcal{D}
   $$

1. if $const$ has a [[left adjoint]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}), this is called the construction of forming the _colimiting [[cocone]] of $\mathcal{C}$-shaped diagrams in $\mathcal{D}$_, or just _[[colimit]]_ (or _[[direct limit]]_) for short, and denoted

   $$
     \underset{\underset{\mathcal{C}}{\longrightarrow}}{\lim}
     \;\colon\;
     [\mathcal{C}, \mathcal{D}] \longrightarrow \mathcal{D}
   $$

$$
  \label{LimitAndColimitAdj}
  [\mathcal{C}, \mathcal{D}]
    \array{
       \overset{ \phantom{AA}\underset{\underset{\mathcal{C}}{\longrightarrow}}{\lim} \phantom{AA} }{\longrightarrow}
       \\
       \overset{\phantom{AA} const \phantom{AA} }{ \longleftarrow }
       \\
       \overset{ \phantom{AA} \underset{\underset{\mathcal{C}}{\longleftarrow}}{\lim}  \phantom{AA}}{\longrightarrow}
    }
  \mathcal{D}
  \,.
$$

If $\underset{\underset{\mathcal{C}}{\longleftarrow}}{\lim}$ ($\underset{\underset{\mathcal{C}}{\longrightarrow}}{\lim}$) exists for a given $\mathcal{D}$, one says that $\mathcal{D}$ _has all limits_ (_has all colimits_) of shape $\mathcal{C}$_ or that all limits (colimits) of shape $\mathcal{D}$ _exist in $\mathcal{D}$_. If this is the case for all [[small category|small]] [[diagrams]] $\mathcal{C}$, one says that _$\mathcal{D}$ has all limits_ (_has all colimits_) or that _all limits exist in $\mathcal{D}$_, (_all colimits exist in $\mathcal{D}$_.)

=--

+-- {: .num_remark #LimitingCones}
###### Remark
**([[limit]] [[cones]])

Unwinding Definition \ref{Limits} of [[limits]] and [[colimits]], it says the following.

First of all, for $d \in \mathcal{D}$ any [[object]] and $F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ any [[functor]], a [[natural transformation]] (Def. \ref{NaturalTransformations}) of the form

\[
  \label{ConeAsNaturalTransformation}
  const_d \overset{i}{\Rightarrow} F
\]

has component morphisms

$$
  \array{
     d
     \\
     \big\downarrow^{\mathrlap{i_c}}
     \\
     F(c)
  }
$$

in $\mathcal{D}$, for each $c \in \mathcal{C}$, and the naturality condition (eq:Naturality) says that these form a [[commuting diagram]] (Def. \ref{CommutingDiagram}) of the form

\[
  \label{ConeInComponents}
  \array{
    && d
    \\
    & {}^{\mathllap{ i_{c_1} } }\swarrow && \searrow^{\mathrlap{ i_{c_2} }}
    \\
    F(c_1)
      && \underset{ \phantom{AA} F(f) \phantom{AA} }{\longrightarrow} &&
    F(c_2)
  }
\]

for each morphism $c_1 \overset{f}{\to} c_2$ in $\mathcal{C}$. Due to the look of this [[diagram]], one also calls such a natural transformation a _[[cone]]_ over the functor $F$.

Now the [[counit of an adjunction|counit]] (Def. \ref{AdjunctionUnitFromHomIsomorphism}) of the $(const \dashv \underset{\longleftarrow}{\lim})$-[[adjunction]] (eq:LimitAndColimitAdj) is a [[natural transformation]] of the form

\[
  const_{\underset{\longleftarrow}{\lim} F}
  \overset{ \phantom{AA} \epsilon_{F} \phantom{AA} }{\longrightarrow}
  F
\]

and hence is, in components, a [[cone]] (eq:ConeInComponents) over $F$:

\[
  \label{LimitCone}
  \array{
    && \underset{\longleftarrow}{\lim} F
    \\
    & {}^{\mathllap{ \epsilon_F(c_1) } }\swarrow && \searrow^{\mathrlap{ \epsilon_F(c_2) }}
    \\
    F(c_1)
      && \underset{ \phantom{AA} F(f) \phantom{AA} }{\longrightarrow} &&
    F(c_2)
  }
\]

to be called the _limiting cone_ over $F$

But the [[universal property]] of [[adjunctions]] says that this is a very special cone: By Prop. \ref{CollectionOfUniversalArrowsEquivalentToAdjointFunctor} the defining property of the limit is equivalently that for every natural transformation of the form (eq:ConeAsNaturalTransformation), hence for every [[cone]] of the form (eq:ConeInComponents), there is a _unique_ natural transformation

$$
  \array{
    const_d
    &\overset{\widetilde i}{\Rightarrow}&
    const_{ \underset{ \longleftarrow }{\lim} }
  }
$$

which, due to constancy of the two functors applied in the naturality condition (eq:Naturality), has a constant component morphism

\[
  \label{UniversalMorphismForLimit}
  d
    \overset{ \widetilde i }{\longrightarrow}
  \underset{\longleftarrow}{\lim} F
\]

such that

$$
  \array{
    const_d
    && \overset{\widetilde i}{\longrightarrow} &&
    const_{ \underset{\longleftarrow}{\lim} F }
    \\
    & {}_{\mathllap{ \epsilon_F }} \searrow && \swarrow_{ \mathrlap{i} }
    \\
    && F
  }
$$

hence such that (eq:UniversalMorphismForLimit) factors the given [[cone]] (eq:ConeInComponents) through the special cone (eq:LimitCone):

$$
  \array{
    && d
    \\
    & {}^{\mathllap{ i_{c_1} } }\swarrow && \searrow^{\mathrlap{ i_{c_2} }}
    \\
    F(c_1)
      && \underset{ \phantom{AA} F(f) \phantom{AA} }{\longrightarrow}
    F(c_2)
  }
  \phantom{AAA} = \phantom{AAA}
  \array{
    && d
    \\
    && \big\downarrow^{ \mathrlap{ \widetilde i } }
    \\
    && \underset{\longleftarrow}{\lim} F
    \\
    & {}^{\mathllap{ \epsilon_F(c_1) } }\swarrow && \searrow^{\mathrlap{ \epsilon_F(c_2) }}
    \\
    F(c_1)
      && \underset{ \phantom{AA} F(f) \phantom{AA} }{\longrightarrow}
    F(c_2)
  }
$$

In this case one also says that $\widetilde i$ is a _[[morphism]] of [[cones]]_.

Hence a _limit cone_ is a cone over $F$, such that every other cone factors through it in a unique way.

Of course this concept of (co)limiting cone over a functor $F \;\colon\; \mathcal{C} \to \mathcal{D}$ makes sense also when

1. $\mathcal{C}$ is not [[small category|small]],

1. and/or when a (co-)limiting cone exists only for some but not for all functors of this form.

=--



+-- {: .num_example #TerminalObjectIsEmptyLimit}
###### Example
**([[terminal object|terminal]]/[[initial object]] is [[empty category|empty]] [[limit]]/[[colimit]])**

Let $\mathcal{C}$ be a [[category]], and let $\ast \in \mathcal{C}$ be an [[object]]. The following are equivalent:

1. $\ast$ is a [[terminal object]] of $\mathcal{C}$ (Def. \ref{InitialObject});

1. $\ast$ is the [[limit]] of [[generalized the|the]] [[empty category|empty]] [[diagram]].

And [[formal dual|formally dual]] (example \ref{OppositeCategory}): Let $\emptyset \in \mathcal{C}$ be an object. The following are equivalent:

1. $\emptyset$ is an [[initial object]] of $\mathcal{C}$ (Def. \ref{InitialObject});

1. $\emptyset$ is the [[colimit]] of [[generalized the|the]] [[empty category|empty]] [[diagram]].

=--

+-- {: .proof}
###### Proof

We discuss the case of the [[terminal object]], the other case is [[formal duality|formally dual]] (Example \ref{OppositeCategory}).

It suffices to observe that a [[cone]] over the [[empty category|empty]] [[diagram]] (Remark \ref{LimitingCones}) is clearly just a plain [[object]] of $\mathcal{C}$. Hence a morphism of such cones is just a plain morphism of $\mathcal{C}$. This way the condition on a limiting cone is now manifestly the same as the condition on a terminal object.

=--

+-- {: .num_prop #InitialObjectIsLimitOverIdentityFunctor}
###### Example
**([[initial object]] is [[limit]] over [[identity functor]])**

Let $\mathcal{C}$ be a [[category]], and let $\emptyset \in \mathcal{C}$ be an [[object]]. The following are equivalent:

1. $\emptyset$ is an [[initial object]] of $\mathcal{C}$ (Def. \ref{InitialObject});

1. $\emptyset$ is the tip of a [[limit]] [[cone]] (Remark \ref{LimitingCones}) over the [[identity functor]] on $\mathcal{C}$.

=--

+-- {: .proof}
###### Proof

First let $\emptyset$ be an [[initial object]]. Then, by definition, it is the tip of a unique [[cone]] over the identity functor

\[
  \label{InitialObjectCone}
  \array{
    const_{\emptyset}&\phantom{AA}& && \emptyset
    \\
    {}^{\mathllap{i^{\emptyset}}}\Downarrow && & {}^{\mathllap{i^{\emptyset}_{c_1}}}\swarrow && \searrow^{\mathrlap{i^{\emptyset}_{c_2}}}
    \\
    id_{\mathcal{C}} && c_1 && \underset{f}{\longrightarrow} && c_2
  }
\]

We need to show that that every other cone $i^x$

$$
  \array{
    const_{x}&\phantom{AA}& && x
    \\
    {}^{\mathllap{\mathllap{i^x}}}\Downarrow && & {}^{i^x_{c_1}}\swarrow && \searrow^{\mathrlap{i^x_{c_2}}}
    \\
    id_{\mathcal{C}} && c_1 && \underset{f}{\longrightarrow} && c_2
  }
$$

factors uniquely through $i^\emptyset$.

First of all, since the cones are over the identity functor, there is the component $i^x_{\emptyset} \;\colon\; x \to \emptyset$, and it is a morphism of cones.

To see that this is the unique morphism of cones, consider any morphism of cones $j^x_\emptyset$, hence a morphism in $\mathcal{C}$ such that $i^x_c = i^\emptyset_c  \circ j^x_\emptyset $ for all $c \in \mathcal{C}$. Taking here $c = \emptyset$ yields

$$
  \begin{aligned}
    i^x_\emptyset
      & =
    \underset{ = id_\emptyset }{\underbrace{i^\emptyset_{\emptyset}}} \circ j^x_{\emptyset}
    \\
    & = j^x_\emptyset
    \,,
  \end{aligned}
$$

where under the brace we used that $\emptyset$ is initial. This proves that $i^\emptyset$ is the limiting cone.

For the converse, assume now that $i^\emptyset$ is a limiting cone over the identity functor, with labels as in (eq:InitialObjectCone). We need to show that its tip $\emptyset$ is an initial object.

Now the cone condition applied for any object $x \in \mathcal{C}$ over the morphims $f \coloneqq i^\emptyset_x$ says that

$$
  i^{\emptyset}_x \circ i^\emptyset_\emptyset = i^\emptyset_x
$$

which means that $i^\emptyset_\emptyset$ constitutes a morphism of cones from $i^\emptyset$ to itself. But since $i^\emptyset$ is assumed to be a limiting cone, and since the [[identity morphism]] on $\emptyset$ is of course also a morphism of cones from $i^\emptyset$ to itsely, we deduce that

\[
  \label{iemptyemptyIsIdempty}
  i^\emptyset_\emptyset
   \;=\;
  id_{\emptyset}
  \,.
\]

Now consider any morphism of the form $\emptyset \overset{f}{\to} x$. Since we already have the morphism $\emptyset \overset{i^\emptyset_x}{\to} x$, to show initiality of $\emptyset$ we need to show that $f = i^\emptyset_x$.

Indeed, the cone condition of $i^\emptyset_x$ applied to $f$ now yields

$$
  \begin{aligned}
    i^\emptyset_x
    & =
    f \circ \underset{ = id_{\emptyset} }{\underbrace{i^\emptyset_\emptyset}}
    \\
    & =
    f\,,
  \end{aligned}
$$

where under the brace we used (eq:iemptyemptyIsIdempty).

=--


+-- {: .num_example #LimitsOfPresheavesAreComputedObjectwise}
###### Example
**([[limits of presheaves are computed objectwise]])**

Let $\mathcal{C}$ be a [[category]] and write $[\mathcal{C}^{op}, Set]$ for its [[category of presheaves]] (Example \ref{CategoryOfPresheaves}). Let moreover $\mathcal{D}$ be a [[small category]] and consider any [[functor]]

$$
  F \;\colon\; \mathcal{D} \longrightarrow [\mathcal{C}^{op}, \mathcal{D}]
  \,,
$$

hence a $\mathcal{D}$-shaped [[diagram]] in the [[category of presheaves]].

Then

1. The [[limit]] (Def. \ref{Limits}) of $F$ exists, and is the [[presheaf]] which over any [[object]] $c \in \mathcal{C}$ is given by the [[limit]] in [[Set]] of the values of the presheaves at $c$:

   $$
     \left(
       \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{\lim}
       F(d)
     \right)(c)
     \;\simeq\;
     \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{\lim}
      F(d)(c)
   $$


1. The [[colimit]] (Def. \ref{Limits}) of $F$ exists, and is the [[presheaf]] which over any [[object]] $c \in \mathcal{C}$ is given by the [[colimit]] in [[Set]] of the values of the presheaves at $c$:

   $$
     \left(
       \underset{\underset{d \in \mathcal{D}}{\longrightarrow}}{\lim}
       F(d)
     \right)(c)
     \;\simeq\;
     \underset{\underset{d \in \mathcal{D}}{\longrightarrow}}{\lim}
      F(d)(c)
   $$

=--


+-- {: .proof}
###### Proof

We discuss the case of limits, the other case is [[formal duality|formally dual]] (Example \ref{OppositeCategory}).

Observe that there is a canonical [[equivalence of categories|equivalence]] (Def. \ref{EquivalenceOfCategories})

$$
  [\mathcal{D}, [\mathcal{C}^{op}, \Set]]
  \simeq
  [\mathcal{D} \times \mathcal{C}^{op}, Set]
$$

where $\mathcal{D} \times \mathcal{C}^{op}$ is the [[product category]].

This makes manifest that a [[functor]] $F \;\colon\; \mathcal{D} \to [\mathcal{C}^{op}, Set]$ is equivalently a [[diagram]] of the form

$$
  \array{
    &&
    \vdots && && \vdots
    \\
    && \big\downarrow && &&  \big\downarrow
    \\
    \cdots &\longrightarrow&
    F(d_1)(c_2)
      && \overset{\phantom{AA}}{\longrightarrow} &&
    F(d_2)(c_2)
      &\longrightarrow&
      \cdots
    \\
    &&
    \big\downarrow && &&  \big\downarrow
    \\
    \cdots
    &\longrightarrow&
    F(d_1)(c_1)
      && \overset{\phantom{AA}}{\longrightarrow} &&
    F(d_2)(c_1)
      &\longrightarrow&
      \cdots
    \\
    &&
    \big\downarrow && && \big\downarrow
    \\
    && \vdots && &&  \vdots
  }
$$


Then observe that taking the limit of each "horizontal row" in such a diagram indead does yield a presheaf on $\mathcal{C}$, in that the construction extends from objects to morphisms, and uniquely so:
This is because for any [[morphism]] $c_1 \overset{g}{\to} c_2$ in $\mathcal{C}$, a [[cone]] over $F(-)(c_2)$ (Remark \ref{LimitingCones}) induces a cone over $F(-)(c_1)$, by vertical composition with $F(-)(g)$

$$
  \array{
    &&
    \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{lim}
    F(d)(c_2)
    \\
    & {}^{ }\swarrow && \searrow
    \\
    F(d_1)(c_2)
      && \overset{\phantom{AA}}{\longrightarrow} &&
    F(d_2)(c_2)
    \\
    {}^{\mathllap{F(d_1)(g)}}\big\downarrow
      && &&
    \big\downarrow^{\mathrlap{F(d_2)(g)}}
    \\
    F(d_1)(c_1)
      && \overset{\phantom{AA}}{\longrightarrow} &&
    F(d_2)(c_1)
  }
$$

From this, the universal property of limits of sets (as in Remark \ref{LimitingCones}) implies that there is a _unique_ morphism between the pointwise limits which constitutes a presheaf over $\mathcal{C}$

$$
  \array{
    \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{lim}
    F(d)(c_2)
    \\
    \big\downarrow^{\mathrlap{
      \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{lim}
      F(d)(g)
    }}
    \\
    \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{lim}
    F(d)(c_1)
  }
$$

and that is the tip of a cone over the diagram $F(-)$ in presheaves.

Hence it remains to see that this cone of presheaves is indeed universal.

Now if $I$ is any other cone over $F$ in the category of presheaves, then by the universal property of the pointswise limits, there is for each $c \in \mathcal{C}$ a unique morphism of cones in sets

$$
  I(c)
    \longrightarrow
    \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{lim}
   F(d)(c)
   \,.
$$

Hence there is at most one morphisms of cones of presheaves, namely if these components make all their naturality squares commute.


$$
  \array{
    I(c_2)
      &\longrightarrow&
      \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{lim}
     F(d)(c_2)
     \\
     \big\downarrow && \big\downarrow
     \\
    I(c_1)
      &\longrightarrow&
      \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{lim}
     F(d)(c_1)
   }
   \,.
$$

But since everything else commutes, the two ways of going around this diagram constitute two morphisms from a cone over $F(-)(c_1)$ to the limit cone over $F(-)(c_1)$, and hence they must be equal, by the universal property of limits.

=--





+-- {: .num_prop #HomFunctorPreservesLimits}
###### Proposition
**([[hom-functor preserves limits]])**

Let $\mathcal{C}$ be a [[category]] and write

$$

  Hom_{\mathcal{C}}
   \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
   \longrightarrow
  Set
$$

for its [[hom-functor]]. This [[preserved limit|preserves]] [[limits]] (Def. \ref{Limits}) in both its arguments (recalling that a limit in the [[opposite category]] $\mathcal{C}^{op}$ is a [[colimit]] in $\mathcal{C}$).

More in detail, let $X_\bullet \colon \mathcal{I} \longrightarrow \mathcal{C}$ be a [[diagram]]. Then:

1. If the [[limit]] $\underset{\longleftarrow}{\lim}_i X_i$ exists in $\mathcal{C}$ then for all $Y \in \mathcal{C}$ there is a [[natural isomorphism]]

   $$
     Hom_{\mathcal{C}}\left(Y, \underset{\longleftarrow}{\lim}_i X_i \right)
     \simeq
     \underset{\longleftarrow}{\lim}_i \left( Hom_{\mathcal{C}}\left( Y, X_i \right) \right)
      \,,
   $$

   where on the right we have the limit over the diagram of [[hom-sets]] given by

   $$
     Hom_{\mathcal{C}}(Y,-) \circ X \;\colon\; \mathcal{I} \overset{X}{\longrightarrow} \mathcal{C} \overset{Hom_{\mathcal{C}}(Y,-)  }{\longrightarrow} Set\,.
   $$

1. If the [[colimit]] $\underset{\longrightarrow}{\lim}_i X_i$ exists in $\mathcal{C}$ then for all $Y \in \mathcal{C}$ there is a [[natural isomorphism]]

   $$
     Hom_{\mathcal{C}}\left(\underset{\longrightarrow}{\lim}_i X_i ,Y\right)
     \simeq
     \underset{\longleftarrow}{\lim}_i \left( Hom_{\mathcal{C}}\left( X_i , Y\right) \right)
      \,,
   $$

   where on the right we have the limit over the diagram of [[hom-sets]] given by

   $$
     Hom_{\mathcal{C}}(-,Y) \circ X \;\colon\; \mathcal{I}^{op} \overset{X}{\longrightarrow} \mathcal{C}^{op} \overset{Hom_{\mathcal{C}}(-,Y)  }{\longrightarrow} Set\,.
   $$

=--

+-- {: .proof}
###### Proof

We give the proof of the first statement, the proof of the second statement is [[formal dual|formally dual]] (Example \ref{OppositeCategory}).

First observe that, by the very definition of [[limit|limiting]] [[cones]], maps out of some $Y$ into them are in natural bijection
with the set $Cones\left(Y, X_\bullet \right)$ of cones over the diagram $X_\bullet$ with tip $Y$:

$$
  Hom\left(
    Y,
    \underset{\longleftarrow}{\lim}_{i} X_i
  \right)
    \;\simeq\;
  Cones\left(
    Y, X_\bullet
  \right)
  \,.
$$

Hence it remains to show that there is also a natural bijection like so:

$$
  Cones\left(
    Y,
    X_\bullet
  \right)
    \;\simeq\;
  \underset{\longleftarrow}{\lim}_{i} \left( Hom(Y,X_i) \right)
  \,.
$$

Now, again by the very definition of limiting cones, a single element in the limit on the right is equivalently a cone of the form

$$
  \left\{
  \array{
    && \ast
    \\
    & {}^{\mathllap{const_{p_i}}}\swarrow && \searrow^{\mathrlap{const_{p_j}}}
    \\
    Hom(Y,X_i)
     && \underset{X_\alpha \circ (-)}{\longrightarrow} &&
    Hom(Y,X_j)
  }
  \right\}_{i, j \in Obj(\mathcal{I}), \alpha \in Hom_{\mathcal{I}}(i,j) }
  \,.
$$

This is equivalently for each object $i \in \mathcal{I}$ a choice of morphism $p_i \colon Y \to X_i$ , such that  for each pair of objects $i,j \in \mathcal{I}$
and each $\alpha \in Hom_{\mathcal{I}}(i,j)$ we have $X_\alpha \circ p_i = p_j$. And indeed, this is precisely the characterization of an element in the
set $  Cones\left( Y, X_\bullet\} \right)$.

=--



+-- {: .num_example #InitialAndTerminalObjectInTermsOfAdjunction}
###### Example
**([[initial object|initial]] and [[terminal object]] in terms of [[adjunction]])**

Let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}).

1. The following are equivalent:

   1. $\mathcal{C}$ has a [[terminal object]] (Def. \ref{InitialObject});

   1. the unique [[functor]] $\mathcal{C} \to \ast$ (Def. \ref{Functors}) to the [[terminal category]] (Example \ref{InitialCategoryAndTerminalCategory}) has a [[right adjoint]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets})

      $$
        \ast
          \underoverset
             {\underset{}{\longrightarrow}}
             {\overset{}{\longleftarrow}}
             {\bot}
        \mathcal{C}
      $$

    Under this equivalence, the [[terminal object]] is identified with the image under the right adjoint of the unique object of the [[terminal category]].

1. Dually, the following are equivalent:

   1. $\mathcal{C}$ has an [[initial object]] (Def. \ref{InitialObject});

   1. the unique [[functor]] $\mathcal{C} \to \ast$ to the [[terminal category]] has a [[left adjoint]]

      $$
        \mathcal{C}
          \underoverset
             {\underset{}{\longrightarrow}}
             {\overset{}{\longleftarrow}}
             {\bot}
        \ast
      $$

    Under this equivalence, the [[initial object]] is identified with the image under the left adjoint of the unique object of the [[terminal category]].

=--

+-- {: .proof}
###### Proof

Since the unique [[hom-set]] in the [[terminal category]] is [[generalized the|the]] [[singleton]], the hom-isomorphism (eq:HomIsomorphismForAdjointFunctors) characterizing the [[adjoint functors]] is directly the [[universal property]] of an [[initial object]] in $\mathcal{C}$

$$
  Hom_{\mathcal{C}}( L(\ast) , X )
  \;\simeq\;
  Hom_{\ast}( \ast, R(X) )
  =
  \ast
$$

or of a [[terminal object]]

$$
  Hom_{\mathcal{C}}( X , R(\ast) )
  \;\simeq\;
  Hom_{\ast}( L(X), \ast ) = \ast
  \,,
$$

respectively.

=--


+-- {: .num_prop #AdjointsPreserveCoLimits}
###### Proposition
**([[left adjoints preserve colimits and right adjoints preserve limits]])**

Let $(L \dashv R) \colon \mathcal{D} \to \mathcal{C}$ be a pair of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}). Then

* $L$ [[preserved limit|preserves]] all [[colimits]] (Def. \ref{Limits}) that exist in $\mathcal{C}$,

* $R$ preserves all [[limits]] (Def. \ref{Limits}) in $\mathcal{D}$.

=--

+-- {: .proof}
###### Proof

Let $y : I \to \mathcal{D}$ be a [[diagram]] whose [[limit]] $\lim_{\leftarrow_i} y_i$ exists. Then we have a sequence of [[natural isomorphism]]s, natural in $x \in C$

$$
  \begin{aligned}
    Hom_{\mathcal{C}}(x, R {\lim_\leftarrow}_i y_i)
    &  \simeq
    Hom_{\mathcal{D}}(L x, {\lim_\leftarrow}_i y_i)
    \\
    & \simeq
    {\lim_\leftarrow}_i Hom_{\mathcal{D}}(L x, y_i)
    \\
    & \simeq
    {\lim_\leftarrow}_i Hom_{\mathcal{C}}( x, R y_i)
    \\
    & \simeq
    Hom_{\mathcal{C}}( x, {\lim_\leftarrow}_i R y_i)
    \,,
  \end{aligned}
$$

where we used the hom-isomorphism (eq:HomIsomorphismForAdjointFunctors) and the fact that any [[hom-functor preserves limits]] (Def. \ref{HomFunctorPreservesLimits}). Because this is natural in $x$ the [[Yoneda lemma]] implies that we have an [[isomorphism]]

$$
  R {\lim_\leftarrow}_i y_i
  \simeq
  {\lim_\leftarrow}_i R y_i
  \,.
$$

The argument that shows the preservation of colimits by $L$ is analogous.

=--


+-- {: .num_prop #LimitsCommuteWithLimits}
###### Proposition
**([[limits commute with limits]])**

Let $\mathcal{D}$ and $\mathcal{D}'$ be [[small categories]] (Def. \ref{SmallCategory}) and let $\mathcal{C}$ be a [[category]] (Def. \ref{Categories}) which admits [[limits]] (Def. \ref{Limits}) of shape $\mathcal{D}$  as well as [[limits]] of shape $\mathcal{D}'$. Then these limits "commute" with each other, in that
for $F \;\colon\; \mathcal{D} \times {\mathcal{D}'} \to \mathcal{C}$ a [[functor]] (hence a [[diagram]] of shape the [[product category]]), with corresponding [[adjunct]] functors (via Example \ref{GrpdIsACartesianClosedCategory})

$$
  {\mathcal{D}'}
    \overset{F_{\mathcal{D}}}{\longrightarrow}
  [\mathcal{D},\mathcal{C}]
  \phantom{AAA}
  {\mathcal{D}}
    \overset{F_{\mathcal{D}'}}{\longrightarrow}
  [{\mathcal{D}'},   \mathcal{C}]
$$

we have that the canonical comparison morphism

\[
  \label{ComparisonMorphismForCommutingLimits}
  lim F \simeq lim_{\mathcal{D}}  (lim_{\mathcal{D}'} F_{\mathcal{D}} )
  \simeq
   lim_{\mathcal{D}'}  (lim_{\mathcal{D}} F_{\mathcal{D}'} )
\]

is an [[isomorphism]].

=--

+-- {: .proof}
######Proof

Since the [[limit]]-construction is the [[right adjoint]] functor to the [[constant functor|constant]] [[diagram]]-functor, this is a special case of _[[right adjoints preserve limits]]_ (Prop. \ref{AdjointsPreserveCoLimits}).

=--


See _[[limits and colimits by example]]_ for what formula (eq:ComparisonMorphismForCommutingLimits) says for instance for the special case $\mathcal{C} =$ [[Set]].

+-- {: .num_remark}
###### Remark
**(general non-commutativity of limits with colimits)**

In general limits do _not_ commute with [[colimits]]. But under a number of special conditions of interest they do. Special cases and concrete examples are discussed at _[[commutativity of limits and colimits]]_.

=--

$\,$


+-- {: .num_prop #PointwiseExpressionOfLeftAdjoints}
###### Proposition
**(pointwise expression of [[left adjoints]] in terms of [[limits]] over [[comma categories]])**

A [[functor]] $R \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ (Def. \ref{Functors}) has a [[left adjoint]] $L \;\colon\; \mathcal{D} \longrightarrow \mathcal{C}$ (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) precisely if

1. $R$ [[preserved limit|preserves]] all [[limits]] (Def. \ref{Limits}) that exist in $\mathcal{C}$;

1. for each [[object]] $d \in \mathcal{D}$, the [[limit]] (Def. \ref{Limits}) of the canonical functor (eq:CanonicalFunctorOutOfCommaCategoryOfcOverF) out of the [[comma category]] (Example \ref{CommaCategoryWithOneSideConstant})

   $$
     d/R \longrightarrow \mathcal{C}
   $$

   exists.

In this case the value of the [[left adjoint]] $L$ on $d$ is given by that limit:

\[
  \label{FormulaForLeftAdjointByPointwiseLimit}
  L(d)
  \;\simeq\;
  \underset{\underset{ \left( c,  \array{ d \\ \downarrow^{\mathrlap{f}} \\ R(c) } \right)  \in d/R }{\longleftarrow}}{\lim} c
\]

=--


+-- {: .proof}
###### Proof

First assume that the left adjoint exist. Then

1. $R$ is a [[right adjoint]] and hence preserves limits since all [[right adjoints preserve limits]] (Prop. \ref{AdjointsPreserveCoLimits});

1. by Prop. \ref{CollectionOfUniversalArrowsEquivalentToAdjointFunctor} the [[adjunction unit]] provides a [[universal morphism]] $\eta_d$ into $L(d)$, and hence, by Prop. \ref{UniversalMorphismsAreInitialObjectsInCommaCategory}, exhibits $(L(d), \eta_d)$ as the [[initial object]] of  the [[comma category]] $d/R$. The limit over any category with an initial object exists, as it is given by that initial object.

Conversely, assume that the two conditions are satisfied and let $L(d)$ be given by (eq:FormulaForLeftAdjointByPointwiseLimit). We need to show that this yields a left adjoint.

By the assumption that $R$ preserves all limits that exist, we have

\[
  \label{RAppliedtoFormulaForLeftAdjointByPointwiseLimit}
  \array{
    R(L(d))
    & =
    R\left(
    \underset{\underset{ \left( c,  \array{ d \\ \downarrow^{\mathrlap{f}} \\ R(c) } \right)  \in d/R }{\longleftarrow}}{\lim} c
  \right)
   \\
   & \simeq
    \underset{\underset{ \left( c,  \array{ d \\ \downarrow^{\mathrlap{f}} \\ R(c) } \right)  \in d/R }{\longleftarrow}}{\lim} R(c)
  }
\]

Since the $d \overset{f}{\to} R(d)$ constitute a [[cone]] over the [[diagram]] of the $R(d)$, there is universal morphism

$$
  d \overset{\phantom{AA} \eta_d \phantom{AA}}{\longrightarrow} R(L(d))
  \,.
$$

By Prop. \ref{CollectionOfUniversalArrowsEquivalentToAdjointFunctor} it is now sufficient to show that $\eta_d$ is a [[universal morphism]] into $L(d)$, hence that for all $c \in \mathcal{C}$ and $d \overset{g}{\longrightarrow} R(c)$ there is a unique morphism $L(d) \overset{\widetilde f}{\longrightarrow} c$ such that

$$
  \array{
    && d
    \\
    & {}^{\mathllap{ \eta_d }}\swarrow && \searrow^{\mathrlap{f}}
    \\
    R(L(d)) && \underset{\phantom{AA}R(\widetilde f)\phantom{AA}}{\longrightarrow} && R(c)
    \\
    L(d)
      &&\underset{\phantom{AA}\widetilde f\phantom{AA}}{\longrightarrow}&&
    c
  }
$$

By Prop. \ref{UniversalMorphismsAreInitialObjectsInCommaCategory}, this is equivalent to $(L(d), \eta_d)$ being the [[initial object]] in the [[comma category]] $c/R$, which in turn is equivalent to it being the [[limit]] of the [[identity functor]] on $c/R$ (by Example \ref{InitialObjectIsLimitOverIdentityFunctor}). But this follows directly from the limit formulas (eq:FormulaForLeftAdjointByPointwiseLimit) and (eq:RAppliedtoFormulaForLeftAdjointByPointwiseLimit).

=--

+-- {: .num_remark #AdjointFunctorTheorem}
###### Remark
**([[adjoint functor theorem]])**

Beware the subtle point in Prop. \ref{PointwiseExpressionOfLeftAdjoints}, that the [[comma category]] $c/F$ is in general not a [[small category]] (Def. \ref{SmallCategory}): It has typically "as many" objects as $\mathcal{C}$ has, and $\mathcal{C}$ is not assumed to be small (while of course it may happen to be). But typical categories, such as notably the [[category of sets]] (Example \ref{CategoryOfSets}) are generally guaranteed only to admit limits over [[small categories]]. For this reason, Prop. \ref{PointwiseExpressionOfLeftAdjoints} is rarely useful for _finding_ an [[adjoint functor]] which is not already established to exist by other means.

But there are good sufficient conditions known, on top of the condition that $R$ preserves limits, which guarantee the existence of an adjoint functor, after all. This is the topic of the _[[adjoint functor theorem]]_ (one of the rare instances of useful and non-trivial theorems in mathematics for which issues of [[set theory|set theoretic]] size play a crucial role for their statement and proof).

A very special but also very useful case of the [[adjoint functor theorem]] is the existence of adjoints of [[base change]] functors between categories of ([[enriched presheaf|enriched]]) [[presheaves]] via [[Kan extension]]. This we discuss as Prop. \ref{TopologicalLeftKanExtensionBCoend} below. Since this is most conveniently phrased in terms of special [[limits]]/[[colimits]] called [[ends]]/[[coends]] (Def. \ref{EndAndCoendInTopcgSmash} below) we first discuss these.

=--




$\,$


### Ends and coends
 {#TopologicalEndsAndCoends}

For working with [[enriched categories]] (Def. \ref{TopEnrichedCategory}) , a certain shape of [[limits]]/[[colimits]] (Def. \ref{Limits}) is particularly relevant: these are called _[[ends]]_ and _[[coends]]_ (Def. \ref{EndAndCoendInTopcgSmash} below). We here introduce these and then derive some of their basic properties, such as notably the expression for [[Kan extension]] in terms of ([[coends|co-]])[[ends]] (prop. \ref{TopologicalLeftKanExtensionBCoend} below).

$\,$



+-- {: .num_defn #EndAndCoendInTopcgSmash}
###### Definition
**([[end|(co)end]])**

Let $\mathcal{C}$ be a [[small category|small]] $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}).  Let

$$
  F
    \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  \mathcal{V}
$$

be an [[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor}) out of the enriched [[product category]] of $\mathcal{C}$ with its [[opposite category]] (Def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}). Then:


1. The  **[[coend]]** of $F$, denoted

   $$
     \overset{c \in \mathcal{C}}{\int} F(c,c)
     \;\in\;
     \mathcal{V}
     \,,
   $$

   is the [[coequalizer]] in $\mathcal{V}$ of the two [[actions]] encoded in $F$ via Example \ref{PointedTopologicalFunctorOnProductCategory}:

   $$
     \underset{c,d \in \mathcal{C}}{\coprod} \mathcal{C}(c,d) \otimes F(d,c)
      \underoverset
        {\underset{\underset{c,d}{\sqcup} \rho_{(d,c)}(c) }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} \rho_{(c,d)}(d) }{\longrightarrow}}
        {\phantom{AAAAAAAA}}
     \underset{c \in \mathcal{C}}{\coprod} F(c,c)
      \overset{coeq}{\longrightarrow}
     \overset{c\in \mathcal{C}}{\int} F(c,c)
     \,.
   $$

1. The **[[end]]** of $F$, denoted

   $$
     \underset{c\in \mathcal{C}}{\int} F(c,c)
     \;\in\;
     \mathcal{V}
     \,,
   $$

   is the **[[equalizer]]** in $\mathcal{V}$ of the [[adjuncts]] of the two actions encoded in $F$ via example \ref{PointedTopologicalFunctorOnProductCategory}:

   $$
     \underset{c\in \mathcal{C}}{\int} F(c,c)
       \overset{\;\;equ\;\;}{\longrightarrow}
     \underset{c \in \mathcal{C}}{\prod} F(c,c)
      \underoverset
        {\underset{\underset{c,d}{\sqcup} \tilde \rho_{(c,d)}(c)  }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} \tilde\rho_{d,c}(d)}{\longrightarrow}}
        {\phantom{AAAAAAAA}}
      \underset{c\in \mathcal{C}}{\prod}
      \big[
      \mathcal{C}\left(c,d\right), \;  F\left(c,d\right) \big]
     \,.
   $$

=--

+-- {: .num_example #CoendGivesQuotientByDiagonalGroupAction}
###### Example

For $\mathcal{V}$ a [[cosmos]], let $G \in \mathcal{V}$ be a [[group object]]. There is the n the one-object $\mathcal{V}$-[[enriched category]] $\mathbf{B}G$ as in Example \ref{DeloopingGroupoid}.

Then a $\mathcal{V}$-[[enriched functor]]

$$
  (X,\rho_l) \;\colon\; \mathbf{B}G \longrightarrow \mathcal{V}
$$

is an [[object]] $X \coloneqq F(\ast) \; \in \mathcal{V}$ equipped with a [[morphism]]

$$
  \rho_l \;\colon\; G \otimes X \longrightarrow X
$$

satisfying the [[action]] property. Hence this is equivalently an [[action]]  of $G$ on $X$.

The [[opposite category]] (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}) $(\mathbf{B}G)^{op}$ comes from the [[opposite group]]-[[group object|object]]

$$
  (\mathbf{B}G)^{op}
  =
  \mathbf{B}(G^{op})
  \,.
$$

(The isomorphism $G \simeq G^{op}$ induces a canonical euqivalence of enriched categories $(\mathbf{B}G)^{op} \simeq \mathbf{B}G$.)

So an [[enriched functor]]

$$
  (Y,\rho_r)
    \;\colon\;
  (\mathbf{B} G)^{op} \longrightarrow \mathcal{V}
$$

is equivalently a  _right_ [[action]] of $G$.

Therefore the [[coend]] of two such functors (def. \ref{EndAndCoendInTopcgSmash}) coequalizes the relation

$$
  (x g,\;y)
   \sim
  (x,\; g y)
$$

(where juxtaposition denotes left/right action) and is the [[quotient]] of the plain [[tensor product]] by the [[diagonal action]] of the group $G$:

$$
  \overset{\ast \in \mathbf{B}(G_+)}{\int}
   (Y,\rho_r)(\ast) \,\otimes\, (X,\rho_l)(\ast)
  \;\simeq\;
  Y \otimes_G X
  \,.
$$


=--

+-- {: .num_example #NaturalTransformationsViaEnds}
###### Example
**([[enriched natural transformations]] as [[ends]])**

Let $\mathcal{C}$ be a [[small category|small]] [[enriched category]] (Def. \ref{TopEnrichedCategory}). For
$
  F, G
  \;\colon\;
  \mathcal{C}
    \longrightarrow
  \mathcal{V}
$
two [[enriched presheaves]] (Example \ref{EnrichedPresheaf}), the [[end]] (def. \ref{EndAndCoendInTopcgSmash}) of the [[internal-hom]]-functor

$$
  [F(-),G(-)]
  \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
  \longrightarrow
  \mathcal{V}
$$

is an [[object]] of $\mathcal{V}$ whose underlying [[set]] (Example \ref{ChangeOfCosmosFromVToSet}) is the set of [[enriched natural transformations]] $F \Rightarrow G$ (Def. \ref{EnrichedNaturalTransformation})

$$
  Hom_{\mathcal{V}}\left(1,
  \left(
    \underset{c \in \mathcal{C}}{\int}
    \big[ F(c),G(c) \big]
  \right)
  \right)
  \;\simeq\;
  Hom_{[\mathcal{C}, \mathcal{V}]}(F,G)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The underlying pointed set functor $Hom_{\mathcal{V}}(1,-)\colon \mathcal{V}\to Set$ [[preserved limit|preserves]] all [[limits]], since [[hom-functors preserve limits]] (Prop. \ref{HomFunctorPreservesLimits}). Therefore there is an [[equalizer]] diagram in [[Set]] of the form

$$
  Hom_{\mathcal{V}}\left(1,
  \left(
    \underset{c\in \mathcal{C}}{\int}
    [F(c),G(c)]
  \right)
  \right)
    \overset{equ}{\longrightarrow}
  \underset{c\in \mathcal{C}}{\prod} Hom_{\mathcal{V}}(F(c),G(c))
      \underoverset
        {\underset{\underset{c,d}{\sqcup} U(\tilde \rho_{(c,d)}(c))  }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} U(\tilde\rho_{d,c}(d))}{\longrightarrow}}
        {\phantom{AAAAAAAA}}
   \underset{c,d\in \mathcal{C}}{\prod}
    Hom_{\mathcal{V}}(
      \mathcal{C}(c,d),
      [F(c),G(d)]
    )
 \,,
$$

where we used Example \ref{UnderlyingSetOfInternalHomIsHomSet} to identify underlying sets of internal homs with [[hom-sets]].

Here the object in the middle is just the set of [[indexed sets]] of component morphisms $\left\{ F(c)\overset{\eta_c}{\to} G(c)\right\}_{c\in \mathcal{C}}$. The two parallel maps in the equalizer diagram take such a collection to the [[indexed set]] of composites (eq:OneComposite) and (eq:OtherComposite). Hence that these two are equalized is precisely the condition that the indexed set of components constitutes an [[enriched natural transformation]].

=--

Conversely, example \ref{NaturalTransformationsViaEnds} says that [[ends]] over [[bifunctors]] of the form $[F(-),G(-))]$ constitute [[hom-spaces]] between pointed [[topologically enriched functors]]:


+-- {: .num_defn #PointedTopologicalFunctorCategory}
###### Definition
**([[enriched presheaf category]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$ be a [[small category|small]] $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}).

Then the $\mathcal{V}$-[[enriched presheaf category]] $[\mathcal{C}, \mathcal{V}]$ is $\mathcal{V}$-[[enriched functor category]] from $\mathcal{C}$ to $\mathcal{V}$, hence is the following $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory})

1. the [[objects]] are the $\mathcal{C}$-[[enriched functors]] $\mathcal{C} \overset{F}{\to}\mathcal{V}$ (Def. \ref{TopologicallyEnrichedFunctor});

1. the [[hom-objects]] are the [[ends]]

   \[
     \label{HomObjectOfEnrichedFunctorCategoryViaEnd}
     [\mathcal{C}, \mathcal{V}](F,G)
       \;\coloneqq\;
     \int_{c\in \mathcal{C}} [F(c),G(c)]
   \]

1. the [[composition]] operation on these is defined to be the one induced by the composite maps

   $$
     \left(
       \underset{c\in \mathcal{C}}{\int} [F(c),G(c)]
     \right)
     \otimes
     \left(
       \underset{c \in \mathcal{C}}{\int} [G(c),H(c)]
     \right)
       \overset{}{\longrightarrow}
     \underset{c\in \mathcal{C}}{\prod}
       [F(c),G(c)] \otimes [G(c),H(c)]
     \overset{(\circ_{F(c),G(c),H(c)})_{c\in \mathcal{C}}}{\longrightarrow}
     \underset{c \in \mathcal{C}}{\prod}
       [F(c),H(c)]
     \,,
   $$

   where the first morphism is degreewise given by projection out of the limits that defined the ends. This composite evidently equalizes the two relevant adjunct actions (as in the proof of example \ref{NaturalTransformationsViaEnds}) and hence defines a map into the end

   $$
       \left(
       \underset{c\in \mathcal{C}}{\int} [F(c),G(c)]
     \right)
     \otimes
     \left(
       \underset{c \in \mathcal{C}}{\int} [G(c),H(c)]
     \right)
     \longrightarrow
     \underset{c\in \mathcal{C}}{\int} [F(c),H(c)]
     \,.
   $$

By Example \ref{NaturalTransformationsViaEnds}, the underlying plain category (Example \ref{UnderlyingCategoryOfTopEnrichedCategory}) of this [[enriched functor category]] is the plain [[functor category]] of [[enriched functors]] from Example \ref{CategoryOfEnrichedFunctors}.

=--




+-- {: .num_prop #YonedaReductionTopological}
###### Proposition
**([[enriched Yoneda lemma]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}) let $\mathcal{C}$ be a [[small category|small]] [[enriched category]] (Def. \ref{TopEnrichedCategory}). For $F \colon \mathcal{C} \to \mathcal{V}$ an [[enriched presheaf]] (Example \ref{EnrichedPresheaf}) and for $c\in \mathcal{C}$ an [[object]], there is a [[natural isomorphism]]

$$
  [\mathcal{C}, \mathcal{V}](\mathcal{C}(c,-),\; F)
  \;\simeq\;
  F(c)
$$

between the [[hom-object]] of the [[enriched functor category]] (Def. \ref{PointedTopologicalFunctorCategory}), from the [[representable functor|functor represented]] by $c$ to $F$, and the value of $F$ on $c$.

In terms of the [[ends]] (def. \ref{EndAndCoendInTopcgSmash}) defining these [[hom-objects]] (eq:HomObjectOfEnrichedFunctorCategoryViaEnd), this means that

$$
  \underset{d\in \mathcal{C}}{\int} [\mathcal{C}(c,d), F(d)]
    \;\simeq\;
  F(c)
  \,.
$$

In this form the statement is also known as **[[Yoneda reduction]]**.

=--

Now that [[natural transformations]] are expressed in terms of [[ends]] (example \ref{NaturalTransformationsViaEnds}), as is the [[enriched Yoneda lemma]] (prop. \ref{YonedaReductionTopological}), it is natural to consider the [[formal duality|dual]] statement (Example \ref{OppositeCategory}) involving [[coends]]:

+-- {: .num_prop #TopologicalCoYonedaLemma}
###### Proposition
**([[enriched co-Yoneda lemma]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$ be a [[small category|small]] $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}). For $F \colon \mathcal{C}\to \mathcal{V}$ an [[enriched presheaf]] (Def. \ref{EnrichedPresheaf}) and for $c\in \mathcal{C}$ an [[object]], there is a [[natural isomorphism]]

$$
  F(-)
    \simeq
  \overset{c \in \mathcal{C}}{\int}
  \mathcal{C}(c,-) \otimes F(c)
  \,.
$$

Moreover, the morphism that hence exhibits $F(c)$ as the [[coequalizer]] of the two morphisms in def. \ref{EndAndCoendInTopcgSmash} is componentwise the canonical action

$$
  \mathcal{C}(c,d) \otimes F(c)
   \longrightarrow
  F(d)
$$

which is [[adjunct]] to the component map $\mathcal{C}(d,c) \to [F(c),F(d)]$ of the [[enriched functor]] $F$.

=--

(e.g. [MMSS 00, lemma 1.6](#MMSS00))

+-- {: .proof}
###### Proof

By the definition of [[coends]] and the [[universal property]] of [[colimits]], [[enriched natural transformations]] of the form

$$
  \left(
    \overset{c \in \mathcal{C}}{\int} \mathcal{C}(c,-) \otimes F(c)
  \right)
    \longrightarrow
  G
$$

are in [[natural bijection]] with systems of component morphisms

$$
  \mathcal{C}(c,d) \otimes F(c)
    \longrightarrow
  G(d)
$$

which satisfy some compatibility conditions in their dependence on $c$ and $d$ ([[enriched natural transformation|natural]] in $d$ and "[[extranatural]]" in $c$). By the [[internal hom]] [[adjunction]], these are in [[natural bijection]] to systems of morphisms of the form

$$
  F(c)
   \longrightarrow
   [\mathcal{C}(c,d), G(d)]
$$

satisfying the analogous compatibility conditions. By Example \ref{NaturalTransformationsViaEnds} these are in [[natural bijection]] with systems of morphisms

$$
  F(c) \longrightarrow [\mathcal{C},\mathcal{V}](\mathcal{C}(c,-), G(-))
$$

natural in $c$

By the [[enriched Yoneda lemma]] (Prop. \ref{YonedaReductionTopological}), these, finally, are in [[natural bijection]] with systems of morphisms

$$
  F(c) \longrightarrow G(c)
$$

natural in $c$. Moreover, all these identifications are also natural in $G$. Therefore, in summary, this shows that there is a [[natural isomorphism]]

$$
  Hom_{[\mathcal{C},\mathcal{V}]}
  \left(
    \overset{c \in \mathcal{C}}{\int} \mathcal{C}(c,-) \otimes F(c)
    \;,\;
    (-)
  \right)
  \;\simeq\;
  Hom_{[\mathcal{C},\mathcal{V}]}
  \left(
    F,
    (-)
  \right)
  \,.
$$

With this, the ordinary [[Yoneda lemma]] (Prop. \ref{YonedaLemma}) in the form of the [[Yoneda embedding]] of $[\mathcal{C},\mathcal{V}]$ implies the required isomorphism.

=--

+-- {: .num_example #coYonedaLemmaOverSet}
###### Example
**([[co-Yoneda lemma]] over [[Set]])**

Consider the [[co-Yoneda lemma]] (Prop. \ref{TopologicalCoYonedaLemma}) in the special case $\mathcal{V} =$ [[Set]] (Example \ref{ExamplesOfCosmoi}).

In this case the coequalizer in question is the set of [[equivalence classes]] of [[pairs]]

$$
  ( c \overset{}{\to} c_0,\; x  )
  \;\;
   \in
   \mathcal{C}(c,c_0) \otimes F(c)
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

=--

As a conceptually important corollary we obtain:

+-- {: .num_prop #FreeCocompletion}
###### Proposition
**([[category of presheaves]] is [[free co-completion]])**

For $\mathcal{C}$ a [[small category]] (Def. \ref{SmallCategory}), its [[Yoneda embedding]] $\mathcal{C} \overset{y}{\hookrightarrow} [\mathcal{C}^{op}, Set]$ (Prop. \ref{YonedaEmbedding}) exhibits the [[category of presheaves]] $[\mathcal{C}^{op}, Set]$ (Example \ref{CategoryOfPresheaves}) as the _[[free co-completion]]_ of $\mathcal{C}$ under forming [[colimits]] (Def. \ref{Limits}), in that it is a [[universal morphism]], as in Def. \ref{UniversalArrow}  but "up to natural isomorphism", into a category with all colimits (by Example \ref{LimitsOfPresheavesAreComputedObjectwise}) in the following sense:

1. for $\mathcal{D}$ any [[category]] with all [[colimits]] (Def. \ref{Limits});

1. for $F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ any [[functor]];

there is a [[functor]] $\widetilde F \;\colon\; [\mathcal{C}^{op}, Set] \longrightarrow \mathcal{D}$, unique up to [[natural isomorphism]] such that

1. $\widetilde F$ [[preserved limit|preserves]] all [[colimits]],

1. $\widetilde F$ [[extension|extends]] $F$ through the [[Yoneda embedding]], in that the following [[commuting diagram|diagram commutes]], up to [[natural isomorphism]] (Def. \ref{NaturalTransformations}):

$$
  \array{
    && \mathcal{C}
    \\
    & {}^{y}\swarrow &\swArrow& \searrow^{\mathrlap{F}}
    \\
    \mathrlap{ \!\!\!\!\!\!\!\!\!\!\!\!\! [\mathcal{C}^{op}, Set] }
      && \underset{ \widetilde F }{\longrightarrow} &&
    \mathcal{D}
  }
$$


Hence when interpreting [[presheaves]] as [[generalized spaces]], this says that "generalized spaces are precisely what is obtained from allowing arbitrary gluings of ordinary spaces", see also Remark \ref{OrdinarySpacesAreGeneratorsAndRelationsForGeneralizedSpaces} below.


=--

+-- {: .proof}
###### Proof

The last condition says that $\widetilde F$ is fixed on [[representable presheaves]] by

\[
  \label{YonedaRestriction}
  \widetilde F( y(c) ) \simeq F(c)
  \,.
\]

and in fact [[natural isomorphism|naturally]] so:

\[
  \label{FunctorialYonedaRestriction}
  \array{
    c_1&&
    \widetilde F( y(c_1) ) &\simeq& F(c_1)
    \\
    {}^{\mathllap{f}}\big\downarrow
     && {}^{\mathllap{ F(y(f)) }}\big\downarrow && \big\downarrow^{\mathrlap{ F(f) }}
    \\
    c_2 && \widetilde F (y(c_2)) &\simeq& F(c_2)
  }
\]

But the [[co-Yoneda lemma]] (Prop. \ref{TopologicalCoYonedaLemma}) expresses every [[presheaf]] $\mathbf{X} \in [\mathcal{C}^{op}, Set]$ as a [[colimit]] of [[representable presheaves]] (in the special case of enrichment over $Set$, Example \ref{coYonedaLemmaOverSet})

$$
  \mathbf{X} \;\simeq\; \int^{c \in \mathcal{C}} y(c) \cdot \mathbf{X}(c)
  \,.
$$

Since $\tilde F$ is required to preserve any colimit and hence these particular colimits, (eq:YonedaRestriction) implies that $\widetilde F$ is fixed to act, up to isomorphism, as


$$
  \begin{aligned}
    \widetilde F(\mathbf{X})
    & =
    \widetilde F
    \left(
      \int^{c \in \mathcal{C}} y(c) \cdot \mathbf{X}(c)
    \right)
    & \coloneqq
    \int^{c \in \mathcal{C}} F(c) \cdot \mathbf{X}(c)
    \;\;\;\;\in \mathcal{D}
  \end{aligned}
$$

(where the colimit on the right is computed in $\mathcal{D}$!).

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

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}_1, \mathcal{C}_2$ be two $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}) and

$$
   F
  \;\colon\;
  \left(
    \mathcal{C}_1\times\mathcal{C}_2
  \right)^{op}
  \times
  (\mathcal{C}_1 \times\mathcal{C}_2)
  \longrightarrow
  \mathcal{V}
$$

a $\mathcal{V}$-[[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor})  from the [[product category]] with [[opposite categories]] (Def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}), as shown.

Then its [[end]] and [[coend]] (def. \ref{EndAndCoendInTopcgSmash}) is equivalently formed consecutively over each [[variable]], in either order:

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
**([[internal hom]] preserves [[ends]])**

Let $\mathcal{V}$ be a [[cosmos]] (Def. \ref{Cosmos}). Since the [[internal hom]]-functor in $\mathcal{V}$ (Def. \ref{ClosedMonoidalCategory}) preserves [[limits]] in both variables (Prop. \ref{InternalHomPreservesLimits}), in particular it preserves [[ends]] (Def. \ref{EndAndCoendInTopcgSmash}) in the second variable, and sends coends in the second variable to ends:

For all [[small category|small]] $\mathcal{C}$-[[enriched categories]], $\mathcal{V}$-[[enriched functors]] $F \;\colon\; \mathcal{C}^{op} \otimes \mathcal{C} \to \mathcal{V}$ (Def. \ref{TopologicallyEnrichedFunctor}) and all [[objects]] $X \in \mathcal{V}$ we have [[natural isomorphisms]]

$$
  \left[
    X , \int^{c \in \mathcal{C}} F(c,c)
  \right]
  \;\simeq\;
  \int^{c \in \mathcal{C}}
  \left[ X, F(c,c) \right]
$$

and

$$
  \left[
    \int_{c \in \mathcal{C}} F(c,c)
    ,
    X
  \right]
  \;\simeq\;
  \int^{c \in \mathcal{C}}
  \left[ F(c,c), X \right]
  \,.
$$

=--



With this [[coend]] calculus in hand, there is an elegant proof of the defining [[universal property]] of the smash [[tensoring]] and [[powering]]  [[enriched presheaves]]

+-- {: .num_defn #TensoringAndPoweringOfTopologicallyEnrichedCopresheaves}
###### Definition
**([[tensoring]] and [[powering]] of [[enriched presheaves]])**

Let $\mathcal{C}$ be a $\mathcal{V}$-[[enriched category]], def. \ref{TopEnrichedCategory}, with $[\mathcal{C}, \mathcal{V}]$ its [[functor category]] of [[enriched functors]] (Example \ref{CategoryOfEnrichedFunctors}).

1. Define a [[functor]]

   $$
     (-)\cdot(-)
       \;\colon\;
     [\mathcal{C}, \mathcal{V}] \times \mathcal{V}
      \longrightarrow
     [\mathcal{C}, \mathcal{V}]
   $$

   by forming objectwise [[tensor products]]

   $$
     F \cdot X \;\colon\; c \mapsto F(c) \otimes X
     \,.
   $$

   This is called the **[[tensoring]]** of $[\mathcal{C}, \mathcal{V}]$ over $\mathcal{V}$.

1. Define a functor

   $$
     (-)^{(-)}
       \;\colon\;
     \mathcal{V}^{op} \times [\mathcal{C}, \mathcal{V}]
       \longrightarrow
     [\mathcal{C}, \mathcal{V}]
   $$

   by forming objectwise [[internal homs]] (Def. \ref{ClosedMonoidalCategory})

   $$
     F^X \;\colon\; c \mapsto [X,F(c)]
     \,.
   $$

   This is called the **[[powering]]** of $[\mathcal{C}, \mathcal{V}]$ over $\mathcal{V}$.


=--

+-- {: .num_prop #UniversalPropertyOfTensoringAndPoweringOfFunctorsToTopcg}
###### Proposition
**([[universal property]] of [[tensoring]] and [[powering]] of [[enriched presheaves]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$ be a [[small category|small]] $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}), with $[\mathcal{C},\mathcal{V}]$ the corresponding [[enriched presheaf|enriched presheaf category]].

Then there are [[natural isomorphisms]]

$$
  [\mathcal{C}, \mathcal{V}]( X \cdot K ,\, Y )
    \;\simeq\;
  [K,\big( [\mathcal{C}, \mathcal{V}]\left( X, Y \right) \big)]
$$

and

$$
  [\mathcal{C}, \mathcal{V}]\left( X,\, Y^K \right)
    \;\simeq\;
  [K, \big( [\mathcal{C}, \mathcal{C}](X,Y) \big) ]
$$

for all $X,Y \in [\mathcal{C}, \mathcal{V}]$ and all $K \in \mathcal{C}$,
where $(-)^K$ is the [[powering]] and $(-)\cdot K$ the [[tensoring]] from Def. \ref{TensoringAndPoweringOfTopologicallyEnrichedCopresheaves}.

In particular there is the composite natural isomorphism

$$
  [\mathcal{C}, \mathcal{V}](X \cdot K, Y)
   \;\simeq\;
  [\mathcal{C}, \mathcal{V}]\left( X, Y^K \right)
$$

exhibiting a pair of [[adjoint functors]]

$$
  [\mathcal{C}, \mathcal{V}]
    \underoverset
      {\underset{(-)^K}{\longrightarrow}}
      {\overset{(-) \cdot K}{\longleftarrow}}
      {\bot}
  [\mathcal{C}, \mathcal{V}]
  \,.
$$

=--

+-- {: .proof}
###### Proof

Via the [[end]]-expression for $[\mathcal{C}, \mathcal{V}](-,-)$ from Example \ref{NaturalTransformationsViaEnds}, and the fact (remark \ref{MappingSpacePreservesEnds}) that the [[internal hom]]-functor ends in the second variable, this reduces to the fact that $[-,-]$ is the [[internal hom]] in the [[closed monoidal category]] $\mathcal{V}$ (Example \ref{TopkAsATopologicallyEnrichedCategory}) and hence satisfies the internal tensor/hom-adjunction isomorphism (prop. \ref{TensorHomAdjunctionIsoInternally}):

$$
  \begin{aligned}
    [\mathcal{C}, \mathcal{V}](X \cdot K, Y)
    & =
    \underset{c}{\int}
    [
      (X \cdot K)(c),
      Y(c)
    ]
    \\
    & \simeq
    \underset{c}{\int}
      [X(c) \otimes K, Y(x)]
    \\
    & \simeq
    \underset{c}{\int}
      [K,[X(c), Y(c)]]
    \\
    & \simeq
    [K, \underset{c}{\int} [X(c),Y(c)]]
    \\
    & =
    [K,\left( [\mathcal{C},\mathcal{V}](X,Y)\right)]
  \end{aligned}
$$

and

$$
  \begin{aligned}
    [\mathcal{C}, \mathcal{V}](X, Y^K)
    & =
    \underset{c}{\int}
      [X(c), Y^K(c)]
    \\
    & \simeq
    \underset{c}{\int}
     [ X(c), [K,Y(c)] ]
    \\
    & \simeq
    \underset{c}{\int} [ X(c) \otimes K, Y(c) ]
    \\
    & \simeq
    \underset{c}{\int} [K, [X(c),Y(c)]]
    \\
    & \simeq
    [K, \underset{c}{\int} [X(c),Y(c)] ]
    \\
    & \simeq
    [K, [\mathcal{C}, \mathcal{V}](X,Y]
    \,.
  \end{aligned}
$$

=--

$\,$

### Tensoring and cotensoring

We make explicit the general concept of which Prpp. \ref{UniversalPropertyOfTensoringAndPoweringOfFunctorsToTopcg} provides a key class of examples:

$\,$


+-- {: .num_defn #TensoringAndCotensoring}
###### Definition
**([[tensoring]] and [[cotensoring]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}) let $\mathcal{C}$ be a $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}). Recall the [[enriched hom-functors]] (Example \ref{EnrichedHomFunctor})

$$
  \mathcal{C}(-,-)
  \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C} \longrightarrow \mathcal{V}
$$

and (via Example \ref{TopkAsATopologicallyEnrichedCategory})

$$
  \mathcal{V}(-,-)
  =
  [-,-]
  \;\colon\;
  \mathcal{V}^{op} \times \mathcal{V} \longrightarrow \mathcal{V}
  \,.
$$


1. A _[[powering]]_ (or _[[cotensoring]]_) of $\mathcal{C}$ over $\mathcal{V}$ is 

   1. a [[functor]] (Def. \ref{Functors})

      $$
        [-,-] 
        \;\colon\;
        \mathcal{V}^{op} \times \mathcal{C} \longrightarrow \mathcal{C}
      $$

   1. for each $v \in \mathcal{V}$ a [[natural isomorphism]] (Def. \ref{NaturalTransformations}) of the form

      \[
        \label{NaturalIsomorphismForCotensoring}
        \mathcal{V}(v, \mathcal{C}(c_1,c_2)  )
        \;\simeq\;
        \mathcal{C}(c_1,[v,c_2])
      \]

1. A _[[copowering]]_ (or _[[tensoring]]_) of $\mathcal{C}$ over $\mathcal{V}$ is 

   1. a [[functor]] (Def. \ref{Functors})

      $$
        (-)\otimes(-)
        \;\colon\;
        \mathcal{V} \times \mathcal{C} \longrightarrow \mathcal{C}
      $$

   1. for each $v \in \mathcal{V}$ a [[natural isomorphism]] (Def. \ref{NaturalTransformations}) of the form

      \[
        \label{NaturalIsomorphismForTensoring}
        \mathcal{C}(v \otimes c_1, c_2)
        \;\simeq\;
        \mathcal{V}(v, \mathcal{C}(c_1,c_2)  )
      \]

If $\mathcal{C}$ is equipped with a (co-)powering it is called _(co-)powered_
over $\mathcal{V}$.

=--

+-- {: .num_prop #TensoringLeftAdjointToCotensoring}
###### Proposition
**([[tensoring]] [[left adjoint]] to [[cotensoring]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}) let $\mathcal{C}$ be a $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}).

If $\mathcal{C}$ is both [[tensored and cotensored category|tensored and cotensored]] over $\mathcal{V}$ (Def. \ref{TensoringAndCotensoring}), then for fixed $v \in \mathcal{V}$ the operations of [[tensoring]] with $v$ and of [[cotensoring]] with $\mathcal{V}$ form a pair of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets})

$$
  \mathcal{C}
    \underoverset
      {\underset{ [v,-] }{\longrightarrow}}
      {\overset{ v \otimes (-) }{\longleftarrow}}
      {\phantom{AA}\bot\phantom{AA}}
  \mathcal{C}
$$

=--

+-- {: .proof}
###### Proof

The hom-isomorphism (eq:HomIsomorphismForAdjointFunctors) characterizing the pair of [[adjoint functors]] is provided by the [[composition]] of 
the [[natural isomorphisms]] (eq:NaturalIsomorphismForCotensoring) and (eq:NaturalIsomorphismForTensoring):

$$
  \array{
    \mathcal{C}(v \otimes c_1, c_2)
    \;\simeq\;
    \mathcal{V}(v, \mathcal{C}(c_1,c_2)  )
    \;\simeq\;
    \mathcal{C}(c_1,[v,c_2])
  }
$$

=--


+-- {: .num_prop #InTensoredCotensoredCategoryInitialObjectIsEnrichedInitial}
###### Proposition
**(in [[tensored and cotensored categories]] [[initial object|initial]]/[[terminal objects]] are enriched initial/terminal)**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}) let $\mathcal{C}$ be a $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}).

If $\mathcal{C}$ is both [[tensored and cotensored category|tensored and cotensored]] over $\mathcal{V}$ (Def. \ref{TensoringAndCotensoring}) then 

1. an [[initial object]] $\emptyset$ (Def. \ref{InitialObject}) of the underlying [[category]] of $\mathcal{C}$ (Example \ref{UnderlyingCategoryOfTopEnrichedCategory}) is also enriched initial, in that the [[hom-object]] out of it is the [[terminal object]] $\ast$ of $\mathcal{V}$

   $$
     \mathcal{C}(\emptyset, c) \;\simeq\; \ast
   $$

1. a [[terminal object]] $\ast$ (Def. \ref{InitialObject}) of the underlying category of $\mathcal{C}$ (Example \ref{UnderlyingCategoryOfTopEnrichedCategory}) is also enriched terminal, in that the [[hom-object]] into it is the [[terminal object]] of $\mathcal{V}$:

   $$
     \mathcal{C}(c, \ast) \;\simeq\; \ast
   $$

=--

+-- {: .proof}
###### Proof

We discuss the first claim, the second is [[formal duality|formally dual]].

By prop. \ref{TensoringLeftAdjointToCotensoring}, tensoring is a [[left adjoint]]. Since [[left adjoints preserve colimits]] (Prop. \ref{AdjointsPreserveCoLimits}), and since an [[initial object]] is the [[colimit]] over the [[initial category|empty diagram]] (Example \ref{TerminalObjectIsEmptyLimit}), it follows that 

$$
  v \otimes \emptyset \;\simeq\; \emptyset
$$

for all $v \in \mathcal{V}$, in particular for $\emptyset \in \mathcal{V}$. Therefore the natural isomorphism (eq:NaturalIsomorphismForTensoring) implies for all $v \in \mathcal{V}$ that 

$$
  \mathcal{C}(\emptyset, c)
  \;\simeq\;
  \mathcal{C}( \emptyset \otimes \emptyset, c )
  \;\simeq\;
  \mathcal{V}( \emptyset, \mathcal{C}(\emptyset, c) )
  \;\simeq\;
  \ast
$$

where in the last step we used that the [[internal hom]] $\mathcal{V}(-,-) = [-,-]$ in $\mathcal{V}$ sends [[colimits]] in its first argument to [[limits]] (Prop. \ref{InternalHomPreservesLimits}) and used that a terminal object is [[generalized the|the]] [[limit]] over the [[empty category|empty diagram]] (Example \ref{TerminalObjectIsEmptyLimit}).

=--

  


$\,$


### Kan extensions
  {#KanExtension}


+-- {: .num_prop #TopologicalLeftKanExtensionBCoend}
###### Proposition
**([[Kan extension]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}, \mathcal{D}$ be [[small category|small]] $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}) and let

$$
  p \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
$$

be a $\mathcal{V}$-[[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor}). Then precomposition with $p$ constitutes a functor between the corresponding $\mathcal{V}$-[[enriched presheaf categories]] (Def. \ref{PointedTopologicalFunctorCategory})

\[
  \label{PrecompositionFunctorOnEnrichedPresheaves}
  p^\ast
  \;\colon\;
  \array{
    [\mathcal{D}, \mathcal{V}]
    &\longrightarrow&
    [\mathcal{C}, \mathcal{V}]
    \\
    G &\mapsto& G \circ p
  }
\]

1. This [[enriched functor]] $p^\ast$ (eq:PrecompositionFunctorOnEnrichedPresheaves) has an [[enriched adjunction|enriched left adjoint]] $Lan_p$ (Def. \ref{EnrichedAdjunction}), called _[[left Kan extension]]_ along $p$

   $$
     [\mathcal{D}, \mathcal{V}]
       \underoverset
         {\underset{p^\ast}{\longrightarrow}}
         {\overset{Lan_p }{\longleftarrow}}
         {\bot}
     [\mathcal{C}, \mathcal{V}]
   $$

   which is given objectwise by the [[coend]] (def. \ref{EndAndCoendInTopcgSmash}):

   \[
     \label{FormulaLeftKanExtensionByCoend}
     (Lan_p F)
     \;\colon\;
     d
     \;\mapsto \;
     \overset{c\in \mathcal{C}}{\int}
      \mathcal{D}(p(c),d) \otimes F(c)
     \,.
   \]

1. The [[enriched functor]] $p^\ast$ (eq:PrecompositionFunctorOnEnrichedPresheaves) has an [[enriched adjunction|enriched right adjoint]] $Ran_p$ (Def. \ref{EnrichedAdjunction}), called _[[right Kan extension]]_ along $p$

   $$
     [\mathcal{C}, \mathcal{V}]
       \underoverset
         {\underset{Ran_p}{\longrightarrow}}
         {\overset{p^\ast}{\longleftarrow}}
         {\bot}
     [\mathcal{D}, \mathcal{V}]
   $$

   which is given objectwise by the [[end]] (def. \ref{EndAndCoendInTopcgSmash}):

   \[
     \label{FormulaRightKanExtensionByEnd}
     (Ran_p F)
     \;\colon\;
     d
     \;\mapsto \;
     \underset{c\in \mathcal{C}}{\int}
      [\mathcal{D}(d,p(c)), F(c)]
     \,.
   \]

In summary, this means that the [[enriched functor]]

$$
  \mathcal{C}
    \overset{p}{\longrightarrow}
  \mathcal{D}
$$

induces, via [[Kan extension]], an [[adjoint triple]] (Remark \ref{AdjointTriples}) of [[enriched functors]]

\[
  \label{KanExtensionAdjointTriple}
  Lan_p \;\dashv\; p^\ast \;\dashv\; Ran_p
  \;\colon\;
  [\mathcal{C},\mathcal{V}]
     \leftrightarrow
  [\mathcal{D}, \mathcal{V}]
  \,.
\]

=--

+-- {: .proof}
###### Proof

Use the expression of [[enriched natural transformations]] in terms of [[coends]] (example \ref{NaturalTransformationsViaEnds} and def. \ref{PointedTopologicalFunctorCategory}), then use the respect of $[-,-]$ for ends/coends (remark \ref{MappingSpacePreservesEnds}),  use the [[internal-hom]] [[adjunction]] (eq:InternalHomAdjunction), use the [[Fubini theorem]] (prop. \ref{CoendsCommuteWithEachOther}) and finally use [[Yoneda reduction]] (prop. \ref{YonedaReductionTopological}) to obtain a sequence of [[natural isomorphisms]] as follows:

$$
  \begin{aligned}
    [\mathcal{D}, \mathcal{V}]( Lan_p F, \, G )
    & =
   \underset{d \in \mathcal{D}}{\int}
    [ (Lan_p F)(d), \, G(d) ]
   \\
   & =
   \underset{d\in \mathcal{D}}{\int}
   \left[
     \overset{c \in \mathcal{C}}{\int} \mathcal{D}(p(c),d) \otimes F(c)
     ,\;
     G(d)
   \right]
    \\
  &\simeq
  \underset{d \in \mathcal{D}}{\int}
  \underset{c \in \mathcal{C}}{\int}
  [
    \mathcal{D}(p(c),d) \otimes F(c) \,,\; G(d)
  ]
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  \underset{d\in \mathcal{D}}{\int}
  [F(c),
    [
     \mathcal{D}(p(c),d) , \, G(d)
    ]
  ]
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  [F(c),
    \underset{d\in \mathcal{D}}{\int}
    [
      \mathcal{D}(p(c),d) , \, G(d)
    ]
  ]
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  [
    F(c), G(p(c))
  ]
  \\
  & =
  [\mathcal{C}, \mathcal{V}](F,p^\ast G)
  \end{aligned}
  \,.
$$

and similarly:

$$
  \begin{aligned}
    [\mathcal{D}, \mathcal{V}]( G,\, Ran_p F  )
    & \simeq
    \underset{d \in \mathcal{D}}{\int}
    [ G(d) ,\, (Ran_p F)(d), \, ]
    \\
    & \simeq
    \underset{d \in \mathcal{D}}{\int}
    \left[ G(d)
      ,\,
       \underset{c\in \mathcal{C}}{\int}
       [\mathcal{D}(d,p(c)), F(c)]
    \right]
    \\
    & \simeq
    \underset{d \in \mathcal{D}}{\int}
    \underset{c\in \mathcal{C}}{\int}
    \left[
      G(d) \otimes \mathcal{D}(d,p(c)),\, F(c)
    \right]
    \\
    & \simeq
    \underset{c\in \mathcal{C}}{\int}
    \left[
      \overset{d \in \mathcal{D}}{\int}
      G(d) \otimes \mathcal{D}(d,p(c)),\, F(c)
    \right]
    \\
    & \simeq
    \underset{c \in \mathcal{D}}{\int}
    \left[
      G(p(c)),\, F(c)
    \right]
    \\
    & \simeq
    [\mathcal{C}, \mathcal{V}]( p^\ast G , F )
  \end{aligned}
$$

=--

+-- {: .num_example #CoendFormulaForPresheavesOfSets}
###### Example
**([[coend]] formula for left [[Kan extension]] of ordinary [[presheaves]])**

Consider the [[cosmos]] to be $\mathcal{V} =$ [[Set]], via Example \ref{ExamplesOfCosmoi}, so that [[small category|small]] $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}) are just a plain [[small category]] (Def. \ref{Categories}) by Example \ref{SetEnrichedCategoriesArePlainCategories}, and $\mathcal{V}$-[[enriched presheaves]] (Example \ref{EnrichedPresheaf}) are just plain [[presheaves]] (Example \ref{CategoryOfPresheaves}).

Then for any plain [[functor]] (Def. \ref{Functors})

$$
  \mathcal{C}^{op}
    \overset{\phantom{AA} p \phantom{AA}}{\longrightarrow}
  (\mathcal{C}')^{op}
$$

the general formula (eq:FormulaLeftKanExtensionByCoend) for [[left Kan extension]]

$$
  [\mathcal{C}^{op},Set]
  \overset{Lan_p}{\longrightarrow}
  [(\mathcal{C}')^{op}, Set]
$$

is

$$
  (Lan_p F)(c') \simeq \int^{c \in C} C'(c', p(c)) \times F(c)
  \,.
$$

Using here the [[Yoneda lemma]] (Prop. \ref{YonedaLemma}) to rewrite $F(c) \simeq Hom_{PSh(C)}(c,F)$, this is

$$
  (Lan_p F)(c') \simeq \int^{c \in C} Hom_{C'}(c', p(c)) \times Hom_{PSh(C)}(c,F)
  \,.
$$

Hence this [[coend]]-set consists of [[equivalence classes]] of [[pairs]] of [[morphisms]]

$$
   (c' \to p(c), c \to F)
$$

where two such are regarded as equivalent whenever there is $f \colon c'_1 \to c'_2$ such that

$$
  \array{
    && c'
    \\
    & \swarrow && \searrow
    \\
    p(c_1) && \stackrel{p(f)}{\longrightarrow} && p(c_2)
    \\
    c_1 && \stackrel{f}{\longrightarrow} && c_2
    \\
    & \searrow && \swarrow
    \\
    && F
  }
  \,.
$$

This is particularly suggestive when $p$ is a [[full subcategory]] inclusion (Def. \ref{FullyFaithfulFunctor}). For in that case we may imagine that a representative pair $(c' \to p(c), c \to F)$ is a stand-in for the actual pullback of elements of $F$ along the would-be composite "$c'\to c \to F$", only that this composite need not be defined. But the above equivalence relation is precisely that under which this composite would be invariant.

=--

### Further properties

We collect here further key properties of the various [[universal constructions]] considered above.

$\,$


+-- {: .num_prop #LeftKanExtensionPreservesRepresentableFunctors}
###### Proposition
**([[left Kan extension]] preserves [[representable functors]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}),
let

$$
  \mathcal{C}
  \overset{p}{\longrightarrow}
  \mathcal{D}
$$

be a $\mathcal{V}$-[[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor}) between [[small category|small]] $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}).


Then the [[left Kan extension]] $Lan_p$ (Prop. \ref{TopologicalLeftKanExtensionBCoend}) takes [[representable functor|representable]] [[enriched presheaves]] $\mathcal{C}(c,-) \;\colon\; \mathcal{C} \to \mathcal{V}$ to their image under $p$:

   $$
     Lan_p \mathcal{C}(c, -) \;\simeq\; \mathcal{D}(p(c), -)
   $$

   for all $c \in C$.

=--

+-- {: .proof}
###### Proof

By the [[coend]] formula (eq:FormulaLeftKanExtensionByCoend) we have, naturally in $d' \in \mathcal{D}$, the expression

$$
  \begin{aligned}
    Lan_p \mathcal{C}(c,-)
    \;\colon\;
    d'
    \mapsto
     &
    \int^{c' \in C} \mathcal{D}(p(c'), d') \otimes \mathcal{C}(c,-)(c')
    \\
    & \simeq
    \int^{c' \in C} \mathcal{D}(p(c'), d') \otimes \mathcal{C}(c,c')
    \\
    & \simeq
    \mathcal{D}(p(c), d')
  \end{aligned}
  \,,
$$

where the last step is the [[co-Yoneda lemma]] (Prop. \ref{TopologicalCoYonedaLemma}).

=--


+-- {: .num_example #KanExtensionOfAdjointPairIsAdjointQuadruple}
###### Example
**([[Kan extension]] of [[adjoint pair]] is [[adjoint quadruple]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$, $\mathcal{D}$ be two [[small category|small]] $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}) and let

$$
  \mathcal{C}
    \underoverset
      {\underset{p}{\longrightarrow}}
      {\overset{q}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

be a $\mathcal{V}$-[[enriched adjunction]] (Def. \ref{EnrichedAdjunction}). Then there are $\mathcal{V}$-[[enriched natural isomorphisms]] (Def. \ref{EnrichedNaturalTransformation})

$$
  (q^{op})^\ast \;\simeq\; Lan_{p^{op}}
  \;\colon\;
  [\mathcal{C}^{op},\mathcal{V}]
    \longrightarrow
  [\mathcal{D}^{op},\mathcal{V}]
$$

$$
  (p^{op})^\ast \;\simeq\; Ran_{q^{op}}
  \;\colon\;
  [\mathcal{D}^{op},\mathcal{V}]
    \longrightarrow
  [\mathcal{C}^{op},\mathcal{V}]
$$

between the precomposition on [[enriched presheaves]] with one functor and the left/right [[Kan extension]] of the other (Def. \ref{TopologicalLeftKanExtensionBCoend}).

By essential uniqueness of [[adjoint functors]], this means that the two [[adjoint triples]] (Remark \ref{AdjointTriples}) given by [[Kan extension]] (eq:KanExtensionAdjointTriple) of $q$ and $p$

$$
  \array{
    Lan_{q^{op}} &\dashv& (q^{op})^\ast &\dashv& Ran_{q^{op}}
    \\
    && Lan_{p^{op}} &\dashv& (p^{op})^\ast &\dashv& Ran_{p^{op}}
  }
$$

merge into an [[adjoint quadruple]] (Remark \ref{AdjointTriples})

$$
  \array{
    Lan_{q^{op}} &\dashv& (q^{op})^\ast &\dashv& (p^{op})^\ast &\dashv& Ran_{p^{op}}
  }
  \;\colon\;
  [\mathcal{C}^{op},\mathcal{V}]
    \leftrightarrow
  [\mathcal{D}^{op}, \mathcal{V}]
$$

=--

+-- {: .proof}
###### Proof

For every [[enriched presheaf]] $F \;\colon\; \mathcal{C}^{op} \to \mathcal{V}$ we have a sequence of $\mathcal{V}$-[[enriched natural isomorphism]] as follows

$$
  \begin{aligned}
    (Lan_{p^{op}} F)(d)
      & \simeq
    \int^{ c \in \mathcal{C} } \mathcal{D}(d,p(c)) \otimes F(c)
    \\
    & \simeq
    \int^{ c \in \mathcal{C} } \mathcal{C}(q(d),c) \otimes F(c)
    \\
    & \simeq
    F(q(d))
    \\
    & = \left( (q^{op})^\ast F\right) (d)
    \,.
  \end{aligned}
$$

Here the first step is the [[coend]]-formula for [[left Kan extension]] (Prop. \ref{TopologicalLeftKanExtensionBCoend}), the second step if the [[enriched adjunction]]-isomorphism (eq:EnrichedAdjunctionIsomorphism) for $q \dashv p$ and the third step is the [[co-Yoneda lemma]].

This shows the first statement, which, by essential uniqueness of adjoints, implies the following statements.


=--


+-- {: .num_prop #LeftKanExtensionAlongFullyFaithfulFunctor}
###### Proposition
**([[left Kan extension]] along [[fully faithful functor]] is [[fully faithful functor|fully faithful]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}),
let

$$
  \mathcal{C}
  \overset{\phantom{AA} p \phantom{AA}}{\hookrightarrow}
  \mathcal{D}
$$

be a [[fully faithful functor|fully faithful]] $\mathcal{V}$-[[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor}) between [[small category|small]] $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}).

Then for all $c \in \mathcal{C}$

$$
  p^* (Lan_p c) \simeq c
$$

and in fact the $(Lan_F \dashv F^*)$-[[unit of an adjunction]] is a [[natural isomorphism]]

$$
  Id \stackrel{\simeq}{\to} p^* \circ Lan_{p}
  \,.
$$

hence, by Prop. \ref{FullyFaithfulAndInvertibleAdjoints}, 

$$
  [\mathcal{C}^{op}, Set]
  \overset{\phantom{AA} Lan_p \phantom{AA}}{\hookrightarrow}
  [\mathcal{D}^{op}, Set]
$$

is a [[fully faithful functor]].




=--

+-- {: .proof}
###### Proof

By the [[coend]] formula (eq:FormulaLeftKanExtensionByCoend) we have, naturally in $d' \in \mathcal{D}$, the left Kan extension of any $F \;\colon\; \mathcal{C} \to \mathcal{V}$ on the image of $p$ is

$$
  \begin{aligned}
    Lan_p F
   \;\colon\;
   p(c)
   \mapsto
     & \int^{c' \in C} \mathcal{D}(p(c'), p(c)) \cdot F(c')
     \\
     & \simeq
     \int^{c' \in C} \mathcal{C}(c', c) \cdot F(c')
     \\
     & \simeq F(c)
  \end{aligned}
  \,,
$$

where in the second step we used the assumption of [[fully faithful functor|fully faithfulness]] of $p$ and in the last step we used the [[co-Yoneda lemma]] (Prop. \ref{TopologicalCoYonedaLemma}).

=--


+-- {: .num_lemma #ColimitOfRepresentableIsSingleton}
###### Lemma
**([[colimit]] of representable is [[singleton]])**

Let $\mathcal{C}$ be a [[small category]] (Def. \ref{SmallCategory}). Then the [[colimit]] of a [[representable presheaf]] (Def. \ref{CategoryOfPresheaves}), regarded as a [[functor]]

$$
  y(c) \;\colon\; \mathcal{C}^{op} \longrightarrow Set
$$

is [[generalized the|the]] [[singleton]] set.

\[
  \label{ColimitOfRepresentableIsSingleton}
  \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim} y(c)
  \;\simeq\;
  \ast
  \,.
\]

=--

+-- {: .proof}
###### Proof

One way to see this is to regard the colimit as the [[left Kan extension]] (Prop. \ref{TopologicalLeftKanExtensionBCoend}) along the unique functor $\mathcal{C}^{op} \overset{p}{\to} \ast$ to the [[terminal category]] (Def. \ref{InitialCategoryAndTerminalCategory}). By the formula (eq:FormulaLeftKanExtensionByCoend) this is

$$
  \begin{aligned}
    \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
    y(c)
    & \simeq
    \int^{c_1 \in \mathcal{C}}
      \underset{const_\ast(c_1)}{\underbrace{\ast(-,p(c_1))}} \times y(c)(c_1)
    \\
    & \simeq
    \int^{c_1 \in \mathcal{C}} const_\ast(c_1) \times \mathcal{C}(c_1,c)
    \\
    & \simeq const_\ast(c)
    \\
    & \simeq \ast
  \end{aligned}
$$

where we made explicit the [[constant functor]] $const_\ast \;\colon\; \mathcal{C} \to Set$, constant on the [[singleton]] set $\ast$, and then applied the [[co-Yoneda lemma]] (Prop. \ref{TopologicalCoYonedaLemma}).

=--

+-- {: .num_prop #CategoriesWithFiniteProductsAreCosifted}
###### Proposition
**([[categories with finite products are cosifted]]**

Let $\mathcal{C}$ be a [[small category]] (Def. \ref{SmallCategory}) which has [[finite products]]. Then $\mathcal{C}$ is a _[[cosifted category]]_, equivalently its [[opposite category]] $\mathcal{C}^{op}$ is a _[[sifted category]]_, equivalently [[colimits]] over $\mathcal{C}^{op}$ with values in [[Set]] are _[[sifted colimits]]_, equivalently [[colimits]] over $\mathcal{C}^{op}$ with values in [[Set]] _[[limits commuting with colimits|commute]] with [[finite products]]_, as follows:

For $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$ to [[functors]] on the [[opposite category]] of $\mathcal{C}$ (hence two [[presheaves]] on $\mathcal{C}$, Example \ref{CategoryOfPresheaves}) we have a [[natural isomorphism]] (Def. \ref{NaturalTransformations})

$$
  \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
  \left(
    \mathbf{X} \times \mathbf{Y}
  \right)
  \;\simeq\;
  \left(
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \mathbf{X}
  \right)
  \times
  \left(
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \mathbf{Y}
  \right)
$$

between the [[colimit]] of their [[Cartesian product]] and the [[Cartesian product]] of their separate [[colimits]].

=--

+-- {: .proof}
###### Proof


First observe that for $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$ two [[presheaves]], their [[Cartesian product]] is a [[colimit]] over [[representable presheaf|presheaves represented]] by Cartesian products in $\mathcal{C}$. Explicity, using [[coend]]-notation, we have:

\[
  \label{OnSiteWithProductsExpandProductOfPresheaves}
  \mathbf{X} \times \mathbf{Y}
  \;\simeq\;
  \int^{c_1,c_2 \in \mathcal{C}}
  y(c_1 \times c_2) \times \mathbf{X}(c_1) \times \mathbf{Y}(c_2)
  \,,
\]

where $y \;\colon\; \mathcal{C} \hookrightarrow [\mathcal{C}^{op}, Set]$ denotes the [[Yoneda embedding]].

This is due to the following sequence of [[natural isomorphisms]]:

$$
  \begin{aligned}
    (\mathbf{X} \times \mathbf{Y})(c)
    & \simeq
    \left(
      \int^{c_1 \in \mathcal{C}}
      \mathcal{C}(c,c_1) \times \mathbf{X}(c_1)
    \right)
    \times
    \left(
      \int^{c_2 \in \mathcal{C}}
      \mathcal{C}(c,c_2) \times \mathbf{Y}(c_2)
    \right)
    \\
    & \simeq
    \int^{c_1 \in \mathcal{C}}
    \int^{c_2 \in \mathcal{C}}
    \underset{
      \simeq \mathcal{c}(c, c_1 \times c_2)
    }{
    \underbrace{
      \mathcal{C}(c,c_1) \times \mathcal{C}(c,c_2)
    }}
    \times
    \left(
      \mathbf{X}(c_1) \times \mathbf{X}(c_2)
    \right)
    \\
    & \simeq
    \int^{c_1 \in \mathcal{C}}
    \int^{c_2 \in \mathcal{C}}
    \mathcal{C}(c,c_1 \times c_2)
    \times
       \mathbf{X}(c_1) \times \mathbf{X}(c_2)
    \,,
  \end{aligned}
$$

where the first step expands out both presheaves as colimits of representables separately, via the [[co-Yoneda lemma]] (Prop. \ref{TopologicalCoYonedaLemma}), the second step uses that the [[Cartesian product]] of presheaves is a two-variable [[left adjoint]] (by the [[symmetric monoidal category|symmetric]] [[closed monoidal structure on presheaves]]) and [[adjoints preserve (co-)limits|as such preserves colimits]] (in particular [[coends]]) in each [[variable]] separately (Prop. \ref{AdjointsPreserveCoLimits}), and under the brace we use the defining [[universal property]] of the [[Cartesian products]], assumed to exist in $\mathcal{C}$.

With this, we have the following sequence of [[natural isomorphisms]]:

$$
  \begin{aligned}
    \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
    \left(
      \mathbf{X} \times \mathbf{Y}
    \right)
    &
    \simeq
    \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
    \int^{c_1,c_2 \in \mathcal{C}}
    y(c_1 \times c_2) \times \mathbf{X}(c_1) \times \mathbf{Y}(c_2)
    \\
    & \simeq
    \int^{c_1,c_2 \in \mathcal{C}}
    \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
    \left(
      y(c_1 \times c_2) \times \mathbf{X}(c_1) \times \mathbf{Y}(c_2)
    \right)
    \\
    & \simeq
    \int^{c_1,c_2 \in \mathcal{C}}
    \left(
      \underset{
        \simeq \ast
      }{
      \underbrace{
        \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
        y(c_1 \times c_2)
      }}
    \right)
    \times \mathbf{X}(c_1) \times \mathbf{Y}(c_2)
    \\
    & \simeq
    \int^{c_1,c_2 \in \mathcal{C}}
    \left(
      \mathbf{X}(c_1) \times \mathbf{Y}(c_2)
    \right)
    \\
    & \simeq
    \left(
      \int^{c_1\in \mathcal{C}}
      \mathbf{X}(c_1)
    \right)
    \times
    \left(
      \int^{c_2\in \mathcal{C}}
      \mathbf{Y}(c_2)
    \right)
    \\
    & \simeq
    \left(
      \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
      \mathbf{X}
    \right)
    \times
    \left(
      \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
      \mathbf{Y}
    \right)
  \end{aligned}
$$

Here the first step is (eq:OnSiteWithProductsExpandProductOfPresheaves), the second uses that [[colimits commute with colimits]] (Prop. \ref{LimitsCommuteWithLimits}), the third uses again that the [[Cartesian product]] respects colimits in each variable separately, the fourth is by Lemma \ref{ColimitOfRepresentableIsSingleton}, the last step is again the respect for colimits of the Cartesian product in each variable separately.

=--

