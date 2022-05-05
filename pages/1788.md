


+-- {: .num_remark #LimitingCones}
###### Remark
**([[limit|limiting]] [[cones]])

Unwinding Definition \ref{Limits} of [[limits]] and [[colimits]], it says the following.

First of all, for $d \in \mathcal{D}$ any [[object]] and $F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ any [[functor]], a [[natural transformation]] (Def. \ref{NaturalTransformations}) of the form

\[
  \label{ConeAsNaturalTransformation}
  const_d \overset{i}{\longrightarrow} F
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
    && \underset{longleftarrow}{\lim} F
    \\
    & {}^{\mathllap{ \epsilon_F(c_1) } }\swarrow && \searrow^{\mathrlap{ \epsilon_F(c_2) }}
    \\
    F(c_1) 
      && \underset{ \phantom{AA} F(f) \phantom{AA} }{\longrightarrow}
    F(c_2)
  }
$$

Hence a _limit cone_ is a cone over $F$, such that every other cone factors through it in a unique way.


=--


+-- {: .num_example #SliceCategory}
###### Example
**([[slice category]])**

Let $\mathcal{C}$ be a [[category]], and let $c \in \mathcal{C}$ be any [[object]]. Then 

1. The _[[slice category]]_ (or "[[overcategory]]") $\mathcal{C}_{/c}$ is the [[category]] whose [[objects]] are the [[morphisms]] $X \overset{f}{\to} c$ in $\mathcal{C}$, into $c$, and whose [[morphisms]] $(X_1,f_1) \to (X_2,f_2)$ are the [[morphisms]] $X_1 \overset{g}{\longrightarrow} X_2$ in $\mathcal{C}$ that make a commuting triangle (Def. \ref{CommutingDiagram}):

   $$
     f_2\circ g
     \;=\;
     f_1
     \phantom{AAAAAA}
     \array{
        X_1 
          && 
          \overset{\phantom{AA} g \phantom{AA}}{\longrightarrow} 
          &&
        X_2
        \\
        & {}_{\mathllap{f_1}}\searrow && \swarrow_{\mathrlap{f_2}}
        \\
        && c
     }
   $$

   Hence there is a canonical [[functor]] 

   $$
     \array{
       \mathcal{C}_{/c}
       &\overset{}{\longrightarrow}& 
       \mathcal{C}
     }
   $$

   given by forgetting the morphisms to $c$.


1. The _[[coslice category]]_ (or "[[undercategory]]") $\mathcal{C}^{c/}$ is the [[category]] whose [[objects]] are the [[morphisms]] $c \overset{f}{\to} X$ in $\mathcal{C}$, out of $c$, and whose [[morphisms]] $(X_1,f_1) \to (X_2,f_2)$ are the [[morphisms]] $X_1 \overset{g}{\longrightarrow} X_2$ in $\mathcal{C}$ that make a commuting triangle (Def. \ref{CommutingDiagram}):

   $$
     f_2\circ g
     \;=\;
     f_1
     \phantom{AAAAAA}
     \array{
        && c
        \\
        & {}^{\mathllap{f_1}}\swarrow && \searrow^{\mathrlap{f_2}}
        \\
        X_1 
          && 
          \underset{\phantom{AA} g \phantom{AA}}{\longrightarrow} 
          &&
        X_2
     }
   $$

   Again, there is a canonical [[functor]] 

   $$
     \array{
       \mathcal{C}^{c/}
       &\overset{}{\longrightarrow}& 
       \mathcal{C}
     }
   $$

   given by forgetting the morphisms to $c$.


=--

More generally:

+-- {: .num_example #CommaCategoryWithOneSideConstant}
###### Example
**([[comma category]])**

Let $\mathcal{C}$ be a [[category]], let $c \in \mathcal{C}$ be any [[object]], and let $F \;\colon\; \mathcal{D} \to \mathcal{C}$ be a [[functor]]

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

+-- {: .num_prop #UniversalMorphismsAreInitialObjectsInCommaCategory}
###### Proposition
**([[universal morphisms]] are [[initial objects]] in the [[comma category]])**

Let $\mathcal{C} \overset{R}{\longrightarrow} \mathcal{D}$ be a [[functor]] and $d \in \mathcal{D}$ an [[object]]. Then the following are equivalent:

1. $d \overset{\eta_d}{\to} R(c)$ is a [[universal morphism]] into $R(c)$;

1. $(d, \eta_d)$ is the [[initial object]] in the [[comma category]] $d/R$


=--

+-- {: .num_prop #PointwiseExpressionOfLeftAdjoints}
###### Proposition
**(pointwise expression of [[left adjoints]] in terms of [[limits]] over [[comma categories]])**

A [[functor]] $R \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ has a [[left adjoint]] $L \;\colon\; \mathcal{D} \longrightarrow \mathcal{C}$ precisely if 

1. $R$ [[preserved limit|preserves]] all [[limits]] that exist in $\mathcal{C}$; 

1. for each [[object]] $d \in \mathcal{D}$, the [[limit]] of the canonical functor (eq:CanonicalFunctorOutOfCommaCategoryOfcOverF)

   $$
     d/R \longrightarrow \mathcal{C}
   $$

   out of the [[comma category]] (Example \ref{CommaCategoryWithOneSideConstant}) exists.

In this case the [[left adjoint]] on $d$ is given by that limit:

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

1. $R$ is a [[right adjoint]] and hence preserves limits since all [[right adjoints preserve limits]];

1. by ... the [[adjunction unit]] provides a [[universal morphism]] $\eta_d$ into $L(d)$, and hence, by Prop. \ref{UniversalMorphismsAreInitialObjectsInCommaCategory}, exhibits $(L(d), \eta_d)$ as the [[initial object]] of  the [[comma category]] $d/R$. The limit over any category with an initial object exists, by ... 

Conversely, assume that the two conditions are satisfied. 
Let $L(d)$ be given by (eq:FormulaForLeftAdjointByPointwiseLimit). We need to show that this yields a left adjoint.

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
  d \overset{\phantom{AA} d \phantom{AA}}{\longrightarrow} R(L(d))
  \,.
$$

By Prop. ... it is now sufficient to show that $\eta_d$ is a [[universal morphism]] into $L(d)$, hence that for all $c \in \mathcal{C}$ and $d \overset{g}{\longrightarrow} R(c)$ there is a unique morphism $L(d) \overset{\widetilde f}{\longrightarrow} c$ such that

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

This is equivalent to $(L(d), \eta_d)$ being the [[initial object]] in the [[comma category]] $c/R$, which in turn is equivalent to it being the [[limit]] of the [[identity functor]] on $c/R$. But this follows directly from the limit formulas (eq:FormulaForLeftAdjointByPointwiseLimit) and (eq:RAppliedtoFormulaForLeftAdjointByPointwiseLimit).

=--
