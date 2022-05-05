

+-- {: .num_defn #CategoryWithWeakEquivalences}
###### Definition
**([[category with weak equivalences]])**

A _[[category with weak equivalences]]_ is 

1. a [[category]] $\mathcal{C}$

1. a [[subcategory]] $W \subset \mathcal{C}$

such that the [[morphisms]] in $W$

1. include all the [[isomorphisms]] of $\mathcal{C}$,

1. satisfy [[two-out-of-three]]: 

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

Let $W \subset \mathcal{C}$ be a [[category with weak equivalences]]. Then the _[[localization of a category|localization]]_ of $\mathcal{C}$ at $W$ is, if it exsists

1. a [[category]] $\mathcal{C}[W^{-1}]$

1. a [[functor]] $\gamma \;\colon\; \mathcal{C} \longrightarrow \mathcal{C}[W^{-1}]$

such that

1. $\gamma$ sends all morphisms in $W \subset \mathcal{C}$ to [[isomorphisms]],

1. $\gamma$ is [[universal property|universal with this property]]: If $F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ is any functor with this property, then it factors through $\gamma$, up to [[natural isomorphism]]:

   $$
     F \;\simeq\;
     D F \circ \gamma
     \phantom{AAAAAAA}
     \array{
       \mathcal{C} 
         &\overset{F}{\longrightarrow}&
       \mathcal{D}
       \\
       {}_{\mathllap{\gamma}}\searrow 
         &\swArrow_{\simeq}& 
       \nearrow_{\mathrlap{D F}}
       \\
       & \mathcal{C}[W^{-1}]
     }
   $$

   and any two such factorizations $D F$ and $D' F$ are related by a unique [[natural isomorphism]].

This is called a _[[reflective localization]]_ if the localization functor has a [[fully faithful functor|fully faithful]] [[right adjoint]], exhibiting it as the reflection functor of a [[reflective subcategory]]-inclusion

$$
  \mathcal{C}[W^{-1}]
  \underoverset
    {\underset{\phantom{AAAA}}{\hookrightarrow}}  
    {\overset{ \phantom{AA} \gamma \phantom{AA} }{\longleftarrow}} 
    {\bot}
  \mathcal{C}
$$

=--

+-- {: .num_prop }
###### Proposition

Every [[reflective subcategory]]-inclusion 

$$
  \mathcal{C}_{L}
  \underoverset
    {\underset{\phantom{AA}\iota \phantom{AA}}{\hookrightarrow}}  
    {\overset{ \phantom{AA} L \phantom{AA} }{\longleftarrow}} 
    {\bot}
  \mathcal{C}
$$

is [[generalized the|the]] [[reflective localization]] at the morphisms that are sent to isomorphisms by its reflector.

=--

+-- {: .proof}
###### Proof

Let $F \;\colon\; \mathcal{C} \to \mathcal{D}$ be a [[functor]] which inverts morphisms that are inverted by $L$.

First we need to show that it factors through $L$, up to natural isomorphism. But consider the following [[whiskering]]

$$
  \array{
    \mathcal{C}
    && \overset{F}{\longrightarrow} && 
    \mathcal{D}
    \\
    & {}_{\mathllap{L}}\searrow &\swArrow& \nearrow_{\mathrlap{D F}}
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
    & {}_{\mathllap{L}}\searrow &\swArrow_{\eta}& \nearrow_{\mathrlap{\iota}}
    \\
    && \mathcal{C}_L
  }
$$

By [[idempotent monad|idempotency]], the components of the [[adjunction unit]] $\eta$ are inverted by $L$, and hence by assumption they are also inverted by $F$, so that on the right the [[natural transformation]] $F(\eta)$ is indeed a [[natural isomorphism]].

It remains to show that this factorization is unique up to unique natural isomorphism. So consider any other factorization $D'F$ via a natural isomorphism $\rho$. Pasting this now with the [[adjunction counit]]

$$
  \array{
    &&
    \mathcal{C} && \overset{F}{\longrightarrow} &&  \mathcal{D}
    \\
    &
    {}^{\mathllap{\iota}}\nearrow
    &
    {}^{\epsilon}\swArrow
    & {}_{\mathllap{L}}\searrow 
    &\swArrow_{\rho}& \nearrow_{\mathrlap{D' F}}
    \\
    \mathcal{C}_L
    &&
      \underset{ id }{\longrightarrow}
    && 
    \mathcal{C}_L
  }
$$

exhibits a natural isomorphism $\epsilon \cdot \rho$ between $D F \simeq D' F$.

It is now sufficient to show that this is compatible with $F(\eta)$ in that 

$$
  F(\eta) \circ  \epsilon  \cdot \rho
  \;=\;
  \rho
  \,.
$$

But this follows by the [[triangle identity]]

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
    {}^{\mathllap{\eta}}\swArrow
    &
    {}^{\mathllap{\iota}}\nearrow
    &
    {}^{\epsilon}\swArrow
    & {}_{\mathllap{L}}\searrow 
    &\swArrow_{\rho}& \nearrow_{\mathrlap{D' F}}
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
    & \searrow &\swArrow_\rho& \swarrow
    \\
    && \mathcal{C}_L
  }
$$


=--

