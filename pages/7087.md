
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A [[localization of a category]]/[[localization of an (∞,1)-category|of an (∞,1)-category]] is called **reflective** if its [[localization functor]] has a [[fully faithful functor|fully faithful]] [[right adjoint]], hence if it the reflector of a [[reflective subcategory]]/[[reflective sub-(∞,1)-category]]-inclusion.

In fact every [[reflective subcategory]] inclusion exhibits a reflective localization (Prop. \ref{ReflectiveSubcategoriesAreLocalizations} below).

For reflective localizations the localized category has a particularly useful description (Prop. \ref{ReflectiveLocalizationGivenByLocalObjects} below): It is equivalent to the [[full subcategory]] of _[[local objects]]_ (Def. \ref{LocalObjects} below).

For a left exact reflective localization, the class of morphisms that is inverted forms a left-[[multiplicative system]]. For the moment see  at _[[geometric embedding]]_ for details on this.

Sometimes reflective localizations are understood as the default concept of localization. Notably [[left Bousfield localizations]] are [[presentable (infinity,1)-category|presentations]] of reflective [[localizations of (∞,1)-categories]].


## Definition




+-- {: .num_defn #CategoryWithWeakEquivalences}
###### Definition
**([[category with weak equivalences]])**

A _[[category with weak equivalences]]_ is

1. a [[category]] $\mathcal{C}$,

1. a [[subcategory]] $W \subset \mathcal{C}$

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

Such a localization is called a _[[reflective localization]]_ if the localization functor has a [[fully faithful functor|fully faithful]] [[right adjoint]], exhibiting it as the reflection functor of a [[reflective subcategory]]-inclusion

$$
  \mathcal{C}[W^{-1}]
  \underoverset
    {\underset{\phantom{AAAA}}{\hookrightarrow}}
    {\overset{ \phantom{AA} \gamma \phantom{AA} }{\longleftarrow}}
    {\bot}
  \mathcal{C}
$$

=--

## Properties

+-- {: .num_prop #ReflectiveSubcategoriesAreLocalizations}
###### Proposition
**([[reflective subcategories]] are [[localizations]])**

Every [[reflective subcategory]]-inclusion

$$
  \mathcal{C}_{L}
  \underoverset
    {\underset{\phantom{AA}\iota \phantom{AA}}{\hookrightarrow}}
    {\overset{ \phantom{AA} L \phantom{AA} }{\longleftarrow}}
    {\bot}
  \mathcal{C}
$$

is [[generalized the|the]] [[reflective localization]] at the class $W \coloneqq L^{-1}(Isos)$ of morphisms that are sent to isomorphisms by the reflector $L$.

=--

+-- {: .proof}
###### Proof

Let $F \;\colon\; \mathcal{C} \to \mathcal{D}$ be a [[functor]] which inverts morphisms that are inverted by $L$.

First we need to show that it factors through $L$, up to natural isomorphism. But consider the following [[whiskering]] $F(\eta)$ of the [[adjunction unit]] $\eta$ with $F$:

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

By [[idempotent monad|idempotency]], the components of the [[adjunction unit]] $\eta$ are inverted by $L$, and hence by assumption they are also inverted by $F$, so that on the right the [[natural transformation]] $F(\eta)$ is indeed a [[natural isomorphism]].

It remains to show that this factorization is unique up to unique natural isomorphism. So consider any other factorization $D^' F$ via a natural isomorphism $\rho$. Pasting this now with the [[adjunction counit]]

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

exhibits a natural isomorphism $\epsilon \cdot \rho$ between $D F \simeq D^' F$. Moreover, this is compatible with $F(\eta)$ according to (eq:CompatibleNaturalIsoForLocalization), due to the [[triangle identity]]:

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

Finally, since $L$ is [[essentially surjective functor]], by [[idempotent monad|idempotency]], it is clear that this is the unique such natural isomorphism.

=--

+-- {: .num_defn #LocalObjects}
###### Definition
**([[local object]])**

Let $W \subset \mathcal{C}$ be a [[category with weak equivalences]] (Def. \ref{CategoryWithWeakEquivalences}). Then an [[object]] $X \in \mathcal{C}$ is called a _$W$-[[local object]]_ if for all $A \overset{w}{\to} B \; \in W$ the [[hom-functor]] from $w$ into $X$ yields a [[bijection]]:

$$
  Hom_{\mathcal{C}}(w,X)
  \;\colon\;
  Hom_{\mathcal{C}}(B,X)
   \overset{ \phantom{AA} \simeq \phantom{AA} }{\longrightarrow}
  Hom_{\mathcal{C}}(A,X)
$$

=--

+-- {: .num_prop #ReflectiveLocalizationGivenByLocalObjects}
###### Proposition
**([[reflective localization]] is given by the [[local objects]])**

Let $W \subset \mathcal{C}$ be a [[category with weak equivalences]] (Def. \ref{CategoryWithWeakEquivalences}). If its [[reflective localization]] (Def. \ref{LocalizationOfACategory}) exists

$$
  \mathcal{C}[W^{-1}]
    \underoverset
      {\underset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}}
      {\overset{ \phantom{AA} L \phantom{AA} }{\longleftarrow}}
      {\bot}
  \mathcal{C}
$$

then $\mathcal{C}[W^{-1}] \overset{\iota}{\hookrightarrow} \mathcal{C}$ is [[equivalence of categories|equivalently]] the inclusion of the [[full subcategory]] on the $W$-[[local objects]] (Def. \ref{LocalObjects}).

=--

+-- {: .proof}
###### Proof

We need to show that 

1. every $X \in \mathcal{C}[W^{-1}] \overset{\iota}{\hookrightarrow} \mathcal{C}$ is $W$-[[local object|local]], 

1. every $Y \in \mathcal{C}$ is $W$-[[local object|local]] precisely if it is [[isomorphism|isomorphic]] to an object in $\mathcal{C}[W^{-1}] \overset{\iota}{\hookrightarrow} \mathcal{C}$.

The first statement follows directly with the [[adjoint functor|adjunction isomorphism]]:

$$
  Hom_{\mathcal{C}}(w, \iota(X))
    \simeq
  Hom_{\mathcal{C}[W^{-1}]}(L(w), X)
$$

and the fact that the [[hom-functor]] takes [[isomorphisms]] to [[bijections]].

For the second statement, consider the case that $Y$ is $W$-local. Observe that then $Y$ is also local with respect to the class 

$$
  W_{sat} \;\coloneqq\; L^{-1}(Isos)
$$ 

of _all_ morphisms that are inverted by $L$ (the "[[saturated class of morphisms]]"): For consider the [[hom-functor]] $\mathcal{C} \overset{Hom_{\mathcal{C}}(-,Y)}{\longrightarrow} Set^{op}$ to the [[opposite category|opposite]] of the [[category of sets]]. But assumption on $Y$ this takes elements in $W$ to isomorphisms. Hence, by the defining [[universal property]] of the [[localization]]-functor $L$, it factors through $L$, up to [[natural isomorphism]]. 

Since by [[idempotent monad|idempotency]] the [[adjunction unit]] $\eta_Y$ is in $W_{sat}$, this implies that we have a [[bijection]] of the form

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

## Related concepts

* [[reflective subcategory]], [[coreflective subcategory]]

* [[reflective factorization system]]

* [[Bousfield localization]]

## References

The concept was originally highligted in

* {#GabrielZisman67} [[Pierre Gabriel]], [[Michel Zisman]], _[[Calculus of fractions and homotopy theory]]_, Springer 1967 ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/GZ.pdf))



[[!redirects reflective localizations]]