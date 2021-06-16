
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}
 
## Idea 
 {#Idea}

The definition of _cohesive topos_ or _category of cohesion_ aims to axiomatize properties of a [[topos]] that make it a [[gros topos]] of [[spaces]] inside of which [[geometry]] may take place. See also at _[[motivation for cohesive toposes]]_ for a non-technical discussion.

The idea behind the term is that a _geometric space_ is roughly something consisting of points or pieces that are _held together_ by some cohesion - for instance by [[topology]], by [[smooth structure]], etc.

The canonical [[global section]] geometric morphism $\Gamma : \mathcal{E} \to Set$ of a cohesive topos over [[Set]] may be thought of as sending a space $X$ to its underlying set of points $\Gamma(X)$. Here $\Gamma(X)$ is $X$ with all _cohesion forgotten_ (for instance with the topology or the smooth structure forgotten)

Conversely, the [[left adjoint]] and [[right adjoint]] of $\Gamma$

$$
  \mathcal{E} 
    \stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{Codisc}{\leftarrow}}}
  Set
$$

send a set $S$ either to the [[discrete space]] $Disc(S)$ with _discrete_ cohesive structure (for instance with [[discrete topology]]) or to the [[codiscrete space]] $Codisc(S)$ with the _codiscrete_ cohesive structure (for instance with [[codiscrete topology]]). (An instance of an [[adjoint cylinder]]/[[unity of opposites]], a "[[category of being]]").

Moreover, the idea is that cohesion makes points lump together to _connected pieces_ . This is modeled by one more functor $\Pi_0 : \mathcal{E} \to Set$ [[left adjoint]] to $Disc$. In the context of 1-[[topos theory]] this sends a cohesive space to its [[connected topos|connected components]] $(\Pi = \pi_0)$. More generally in an [[(n,1)-topos]]-theory context, $\Pi$ sends a cohesive space $X$ to the $(n-1)$-[[truncated|truncation]] of its [[geometric homotopy groups in an (∞,1)-topos|geometric fundamental ∞-groupoid]] $\Pi(X)$. See [[cohesive (∞,1)-topos]].

In total this gives an [[adjoint quadruple]]

   $$
    (\Pi_0 \dashv Disc \dashv \Gamma \dashv Codisc) : 
    \mathcal{E}
     \stackrel{\stackrel{\overset{\Pi}{\longrightarrow}}{\overset{Disc}{\leftarrow}}}{\stackrel{\underset{\Gamma}{\longrightarrow}}{\underset{Codisc}{\leftarrow}}}
    Set
    \;
   $$

A cohesive topos is a topos whose terminal [[geometric morphism]] admits an extension to such a quadruple of adjoints, satisfying some further properties.


Notice that most objects in a cohesive topos are far from being just sets with extra structure: while the functor $\Gamma$ does produce the set of points underlying an object $X$ in the cohesive topos, it may happen that $X$ is very non-trivial but that nevertheless $\Gamma(X)$ has very few [[global element|points]] (possibly none, with the axioms so far). The [[subcategory]] of objects in $\mathcal{E}$ that we may think of as point sets equipped with extra structure is the [[quasitopos]] $Conc_\Gamma(\mathcal{E})$ of the [[concrete sheaves]] inside $\mathcal{E}$

$$
  Set 
   \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\hookrightarrow}}
  Conc_\Gamma(\mathcal{E}) 
    \stackrel{\overset{Conc}{\leftarrow}}{\hookrightarrow}
  \mathcal{E}
  \,.
$$


It is the fact that $\mathcal{E}$ is a [[local topos]] that allows to identify $Conc_\Gamma(E)$.

To ensure that there is a minimum of points, one can add further axioms. From the above adjunctions one gets a canonical natural morphism

$$
  \Gamma X \to \Pi_0 X
$$

from the points of $X$ to the set of connected pieces of $X$. Demanding this to be an [[epimorphism]] is demanding that _each piece has at least one point_ .

Moreover, one can demand that the cohesive pieces of product or power spaces are the products of the cohesive pieces of the factors.  For powers of a single space, this is demanding that for all $S \in Set$ the following canonical map is an [[isomorphism]]:

$$
  \Pi_0(X^S) \xrightarrow{\simeq} (\Pi_0(X))^S
  \,.
$$

For more general products, it would be a similar map $\Pi_0(\prod_i X_i) \to \prod_i \Pi_0(X_i)$.  See the examples at [[cohesive site]] for concrete illustrations of these ideas.


## Definition

### Fundamental  axioms

+-- {: .num_defn #CohesiveTopos}
###### Definition

A [[topos]] $\mathcal{E}$ over some base topos $\mathcal{S}$, i.e. equipped with a [[geometric morphism]]

$$
  (f^* \dashv f_*) : \mathcal{E} \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\longrightarrow}}
  \mathcal{S}
$$

is **cohesive** if it is a

* [[strongly connected topos]]

* and a [[local topos]].

In detail this means that it has the following [[stuff, structure, property|properties]]:

1. it is a [[locally connected topos]]: there exists a further [[left adjoint]] $(f_! \dashv f^*)$ satisfying a suitable condition;

1. it is a [[connected topos]]: the functor $f_!$ preserves the [[terminal object]], or equivalently $f^*$ is [[fully faithful functor|fully faithful]];

1. it is _[[strongly connected topos|strongly connected]]_ : $f_!$ preserves even all [[finite]] [[product]]s;

1. it is a [[local topos]]: there exists a further [[right adjoint]] $(f_* \dashv f^!)$ (this is sufficient for $f$ to be local, since we have already assumed it to be connected);

In summary $\mathcal{E}$ is cohesive over $\mathcal{S}$ if we have an [[adjoint quadruple|quadruple]] of [[adjoint functor]] of the form

$$
 (f_! \dashv f^* \dashv f_* \dashv f^!) : 
 \mathcal{E}
    \array{
      \overset{\phantom{AA} f_! \phantom{AA}}{\longrightarrow}
      \\
      \overset{\phantom{AA} f^\ast \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AA} f_\ast \phantom{AA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} f^! \phantom{AA} }{\hookleftarrow}
    }
 \mathcal{S}
$$

such that $f_!$ [[preserved limit|preserves]] [[finite products]].

=--

+-- {: .num_remark}
###### Remark

With $f^*$ being a [[full and faithful functor]] also $f^!$ is, as indicated (for instance by the discussion at [[adjoint triple]]). 

Hence the definition of cohesion specifies two [[full subcategories]], equivalent to each other, both [[reflective subcategory|reflective]] and one also [[coreflective subcategory|coreflective]].

Since a [[topos]] is a [[cartesian closed category]] it follows with the
discussion [here](http://ncatlab.org/nlab/show/reflective+subcategory#ReflectiveSubcategoriesOfCartesianClosedCategotries) that both of these are [[exponential ideals]]. In fact the condition that the $f^*$-inclusion is an exponential ideal is equivalent to the condition that $f_!$ preserves finite products. 

=--

To reflect the geometric interpretation of these axioms we will here and in related entries often name these functors as follows

$$
 (\Pi_0 \dashv Disc \dashv \Gamma \dashv coDisc) : 
 \mathcal{E}
    \array{
      \overset{\phantom{AAA} \Pi_0 \phantom{AAA}}{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookleftarrow}
    }
  \mathcal{S}
  \,.
$$

+-- {: .num_defn #AdjointTriple}
###### Definition

The above [[adjoint quadruple]] canonically induces an [[adjoint triple]] of [[endofunctors]] on $\mathcal{E}$

$$
  (&#643; \dashv \flat \dashv \sharp)
  : 
  \mathcal{E}
   \stackrel{\overset{\Pi_0}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\longrightarrow}}}
  \mathcal{S}
  \stackrel{\overset{Disc}{\longrightarrow}}{\stackrel{\overset{\Gamma}{\leftarrow}}{\underset{coDisc}{\longrightarrow}}}
  \mathcal{E} 
  \,.
$$

Being [[idempotent monads]]/[[comonads]] on $\mathcal{E}$, these are [[modalities]] in the [[type theory]] ([[internal logic]]) of $\mathcal{E}$. As such we call them:
the

* _[[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]]_.

=--

$\,$

### Further axioms
 {#CanonicalComparison}

In addition to the fundamental axioms of cohesion above, there are several further axioms that one may (or may not) want to impose in order to formalize the concept of cohesion.

1. _[[pieces have points]]_;

   equivalently (Prop. \ref{PiecesHavePointsIsDiscreteObjectsAreConcrete} below):

   _[[discrete objects are concrete]]_;

1. equivalent over a [[Boolean topos|Boolean]] [[base topos]] (Prop. \ref{RelationOfPiecesToPointsToInitialAufhebung} below):

   _[[Aufhebung]] of [[bottom]] [[adjoint modality]]_

1. _pieces of powers are powers of pieces_ (Def. \ref{PiecesOfPowersArePowersOfPieces} below)

1. _the subobject classifier is connected_ (Def. \ref{SubobjectClassifierIsConnected} below).



$\,$

First we need some lemmas:

+-- {: .num_lemma #CoincidenceOfTransformsForAdjointTriple}
###### Lemma

Let 

$$
  \mathcal{C}
    \array{
      \overset{ \phantom{A} \Pi \phantom{A} }{\longrightarrow}
      \\
      \overset{ \phantom{A} Disc \phantom{A} }{\hookleftarrow}
      \\
      \overset{ \phantom{A} \Gamma \phantom{A} }{ \longrightarrow }
    }
  \mathcal{D}
$$

be an [[adjoint triple]], with $Disc$ a [[fully faithful functor]].  Denoting the [[adjunction units]]/[[adjunction counit|counits]] as

| $\phantom{A}$ [[adjunction]] $\phantom{A}$ | $\phantom{A}$ [[adjunction unit|unit]] $\phantom{A}$ | $\phantom{A}$ [[adjunction counit|counit]] $\phantom{A}$ |
|----------|-----------|----------|
| $\phantom{A}$ $(\Pi \dashv Disc)$ $\phantom{A}$ | $\phantom{A}$  $\eta^{&#643;}$ $\phantom{A}$ | $\phantom{A}$ $\epsilon^{&#643;}$ $\phantom{A}$ |
| $\phantom{A}$ $(Disc \dashv \Gamma)$ $\phantom{A}$ | $\phantom{A}$ $\eta^\flat$ $\phantom{A}$ | $\phantom{A}$ $\epsilon^\flat$ $\phantom{A}$ |
{: style='margin:auto}

we have that the following [[composition|composites]] of unit/counit components are equal:

\[
  \label{CoincidenceOfNaturalTransformationsForAdjointTriple}
  \left( 
    \eta^{\flat}_{\Pi X}
  \right)
  \circ
  \left( 
    \Pi \epsilon^\flat_X 
  \right)
  \;\;=\;\;
  \left(
    \Gamma \eta^{&#643;}_{X}
  \right)
  \circ
  \left(
    \epsilon^{&#643;}_{\Gamma X}
  \right)
  \phantom{AAAAAA}
  \array{
    \Pi Disc \Gamma X 
    &\overset{\epsilon^{&#643;}_{\Gamma X}}{\longrightarrow}& 
    \Gamma X
    \\
    {}^{ \mathllap{ \Pi \epsilon^\flat_X } }\big\downarrow
    && 
       \big\downarrow^{\mathrlap { \Gamma \eta^{&#643;}_{X} } }
    \\
    \Pi X
    &\underset{ \eta^\flat_{\Pi X} }{\longrightarrow}&
    \Gamma Disc \Pi X
  }
\]

=--

([Johnstone 11, lemma 2.1](#Johnstone11))

+-- {: .proof}
###### Proof

We claim that the following [[commuting diagram|diagram commutes]]:

$$
  \array{
    && && \Gamma X
    \\
    && & {}^{ \epsilon^&#643;_{\Gamma X} }\nearrow 
    && \searrow^{\mathrlap{ \Gamma \eta^{&#643;}_X }}
    \\
    && \Pi Disc \Gamma X
    && && \Gamma Disc \Pi X
    \\
    & {}^{ \Pi \epsilon^\flat_X }\swarrow
    && \searrow^{ \mathrlap{ \Pi Disc \Gamma \eta^{&#643;}_X } }
    && {}^{\mathllap{ \eta^{&#643;}_{\Gamma Disc \Pi X} }}\nearrow 
    && \nwarrow^{ \mathrlap{ \eta^{\flat}_{\Pi X} } }
    \\
    \Pi X
    && && \Pi Disc \Gamma Disc \Pi X
    && && \Pi X
    \\
    & {}_{\mathllap{ \Pi \eta^{&#643;}_X }}\searrow
    && {}^{\mathllap{iso}}\swarrow_{\mathrlap{ \Pi \epsilon^{\flat}_{Disc \Pi X} }}
    && {}_{\mathllap{ \Pi Disc \eta^\flat_{\Pi X} }}\nwarrow^{\mathrlap{iso}}
    && \nearrow_{\mathrlap{ \epsilon^{&#643;}_{\Pi X} }}
    \\
    && \Pi Disc \Pi X
    && \underset{id_{\Pi Disc \Pi X}}{\longleftarrow}  && 
    \Pi Disc \Pi X
  }
$$

This commutes, because:

1. the left square is the image under $\Pi$ of [[naturality square|naturality]] for $\epsilon^\flat$ on $\eta^{&#643;}_X$;

1. the top square is [[naturality square|naturality]] for $\epsilon^{&#643;}$ on $\Gamma \eta^{&#643;}_X$;

1. the right square is [[naturality square|naturality]] for $\epsilon^{&#643;}$ on $\eta^{\flat}_{\Pi X}$;

1. the bottom commuting triangle is the image under $\Pi$ of the [[zig-zag identity]] for $(Disc \dashv \Gamma)$ on $\Pi X$.

Moreover, notice that 

1. the total bottom composite is the [[identity morphism]] $id_{\Pi X}$, due to the [[zig-zag identity]] for $(Disc \dashv \Gamma)$;

1. also the other two morphisms in the bottom triangle are [[isomorphisms]], as shown, due to the [[idempotent monad|idempoency]] of the $(Disc-\Gamma)$-adjunction

Therefore the total composite from $\Pi Disc \Gamma X \to \Gamma Disc \Pi X$ along the bottom part of the diagram equals the left hand side of (eq:CoincidenceOfNaturalTransformationsForAdjointTriple), while the composite along the top part of the diagram clearly equals the right hand side of (eq:CoincidenceOfNaturalTransformationsForAdjointTriple).


=--


+-- {: .num_prop #PointsToPiecesTransform}
###### Proposition
**([[points-to-pieces transform]])**

Consider an [[adjoint triple]] of the form 

$$
  \Pi \dashv Disc \dashv \Gamma
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{\phantom{AA} \Pi \phantom{AA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
    }
  \mathbf{B}
$$

(for instance a [[cohesive topos]] over some [[base topos]] $\mathbf{B}$).

Then for all $X \in \mathbf{H}$ the following two [[natural transformations]], constructed from the [[adjunction units]]/[[adjunction counit|counits]] and their [[inverse morphisms]] (using [[idempotent monad|idempotency]]), are equal:

\[
  \label{PointsToPiecesInTheBase}
  ptp_{\mathbf{B}}
  \;\;\coloneqq\;\;
  \left(
    \Pi \epsilon^\flat_X
  \right)
  \circ
  \left(
    \eta^{&#643;}_{\Gamma X}
  \right)^{-1}
  \;\;=\;\;
  \left(
    \eta^\flat_{\Pi X}
  \right)^{-1}
  \circ
  \left(
    \Gamma \eta^{&#643;}_X
  \right)
  \phantom{AAAAAAA}
  \array{
    \Gamma X 
    & \overset{
       \Gamma \eta^{&#643;}_X
   }{\longrightarrow} & 
   \Gamma Disc \Pi X
   \\
   {}^{ \mathllap{
      \left(
       \eta^{&#643;}_{\Gamma X}
     \right)^{-1}    
   } }\big\downarrow 
     & \searrow^{ \mathrlap{ ptp_{\mathbf{B}} }  } & 
   \big\downarrow^{ \mathrlap{  
     \left(
       \eta^\flat_{\Pi X}
     \right)^{-1}
   } }
   \\ 
   \Pi Disc \Gamma X
   &\underset{ 
    \Pi \epsilon^\flat_X
    }{\longrightarrow}&
   \Pi X
  }
\]

Moreover, the image of these morphisms under $Disc$ equals the following composite:

\[
  \label{PointsToPieces}
  ptp_{\mathbf{H}}
  \;\colon\;
  \flat X 
    \overset{ \phantom{A} \epsilon^{\flat}_X \phantom{A} }{\longrightarrow}
  X
    \overset{ \phantom{A} \eta^{&#643;}_X \phantom{A} }{\longrightarrow}
  &#643; X
  \,,
\]

hence

\[
  \label{PiecesToPointsFromBase}
  ptp_{\mathbf{H}} \;=\; Disc(ptp_{\mathbf{B}})
  \,.
\]

Either of these morphisms we call the _[[points-to-pieces transform]]_.

=--

The first statement is due to ([Johnstone 11, Corollary 2.2](#Johnstone11)).

+-- {: .proof}
###### Proof

The first statement follows directly from Lemma \ref{CoincidenceOfTransformsForAdjointTriple}.

For the second statement, notice that the $(Disc \dashv \Gamma)$-[[adjunct]] of

$$
  ptp_{\mathbf{H}}
  \;\colon\;
  Disc \Gamma X 
    \overset{ \phantom{A} \epsilon^{\flat}_X \phantom{A} }{\longrightarrow}
  X
    \overset{ \phantom{A} \eta^{&#643;}_X \phantom{A} }{\longrightarrow}
  Disc \Pi X
$$

is

\[
  \label{AdjunctOfptpH}
  \widetilde{ ptp_{\mathbf{H}} }
  \;\;=\;\;
  \underset{
    = id_{\Gamma X}
  }{
  \underbrace{
    \Gamma X
      \underoverset{iso}{ \phantom{A} \eta^{\flat}_{\Gamma X} \phantom{A} }{ \longrightarrow }
    \Gamma Disc \Gamma X 
      \underoverset{iso}{ \phantom{A} \Gamma \epsilon^{\flat}_X \phantom{A} }{\longrightarrow}
    \Gamma X
  }}
      \overset{ \phantom{A} \Gamma \eta^{&#643;}_X \phantom{A}  }{\longrightarrow}
    \Gamma Disc \Pi X
  \,,
\]

where under the braces we uses the [[zig-zag identity]]. 

(As a side remark, for later usage, we observe that the morphisms on the left in (eq:AdjunctOfptpH) are [[isomorphisms]], as shown, by [[idempotent monad|idempotency]] of the adjunctions.)  

From this we obtain the following [[commuting diagram]]:

$$
  \array{
    Disc \Gamma X
      &\overset{ \phantom{A} Disc \Gamma \eta^{&#643;}_X \phantom{A} }{\longrightarrow}&
    Disc \Gamma Disc \Pi X
      &\underoverset{iso}{ \phantom{A} Disc \left(\eta^{ \flat }_{\Pi X}\right)^{-1} \phantom{A} }{ \longrightarrow }&
    Disc \Pi X
    \\
    &{}_{\mathllap{ ptp_{\mathbf{H}} }}\searrow&
    {}^{ \mathllap{ \epsilon^{\flat}_{Disc \Pi X} } }
    \big\downarrow^{\mathrlap{\simeq}}
     & 
    \nearrow_{\mathrlap{id_{\Pi X}}}
    \\
    && Disc \Pi X
  }
$$

Here:

1. on the left we identified $\widetilde {\widetilde {ptp_{\mathbf{H}}}} \;=\;  ptp_{\mathbf{H}}$ by applying the formula for $(Disc \dashv \Gamma)$-[[adjuncts]] to $\widetilde {ptp_{\mathbf{H}}} = \Gamma \eta^{&#643;}_X$ (eq:AdjunctOfptpH);

1. on the right we used the [[zig-zag identity]] for $(Disc \dashv \Gamma)$.

This proves the second statement.

=--


+-- {: .num_lemma #ReExpressingMiddleFunctorInAdjointTriple}
###### Lemma

Consider an [[adjoint triple]]

$$
  Disc \dashv \Gamma \dashv coDisc
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{\phantom{AA} Disc \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\longleftarrow}
    }
  \mathbf{B}
$$

Then application of the [[functor]] $\Gamma$ on any [[morphism]] $\mathbf{X} \overset{f}{\to} \mathbf{Y} \;\;\in \mathbf{H}$ is equal both to the operations of 

1. [[composition|pre-composition]] with the $(Disc \dashv \Gamma)$-[[adjunction counit]] $\epsilon^\flat_{\mathbf{X}}$, followed by passing to the  $(Disc \dashv \Gamma)$-[[adjunct]];

1. [[composition|post-composition]] with the $(\Gamma \dashv coDisc)$-[[adjunction unit]] $\eta^{ \sharp }_{\mathbf{Y}}$, followed by passing to the $(\Gamma \dashv coDisc)$-[[adjunct]]:

\[
  \label{PostcompositionWithEtaAsGamma}
  \widetilde{\eta^\sharp_{\mathbf{Y}} \circ (-)}
  \;=\;
  \Gamma_{\mathbf{X}, \mathbf{Y}} 
  \;=\;
  \widetilde{ (-) \circ \epsilon^\flat_{\mathbf{X}} }
  \,.
\]

=--

+-- {: .proof}
###### Proof

For the first equality, consider the following [[naturality square]] for the adjunction hom-isomorphism ([this Def.](geometry+of+physics+--+categories+and+toposes#AdjointFunctorsInTermsOfNaturalBijectionOfHomSets)):

$$
  \array{
    Hom_{\mathbf{B}}( \Gamma \mathbf{Y} , \Gamma \mathbf{Y} )
    &\overset{\widetilde {(-)}}{\longrightarrow}&
    Hom_{\mathbf{H}}( \mathbf{Y}, coDisc \Gamma \mathbf{Y} )
    \\
    {}^{\mathllap{ Hom_{\mathbf{B}}(\Gamma(f), \Gamma \mathbf{Y}) }}
    \big\downarrow
    &&
    \!\!\!\!\!
    \big\downarrow^{\mathrlap{ Hom_{\mathbf{H}}( f, coDisc \Gamma \mathbf{Y} ) }}
    \\
    Hom_{\mathbf{B}}( \Gamma \mathbf{X}, \Gamma \mathbf{Y} )
    &\overset{\widetilde{ (-) }}{\longleftarrow}&
    Hom_{\mathbf{H}}( \mathbf{X}, coDisc \Gamma \mathbf{Y} )
  }
  \phantom{AAAAA}
  \array{
    \{ \Gamma \mathbf{Y} \overset{id_{\Gamma \mathbf{Y}}}{\to} \Gamma \mathbf{Y}\}
    &\longrightarrow&
    \{ \mathbf{Y} \overset{\eta^\sharp_{\mathbf{Y}}}{\to} coDisc \Gamma \mathbf{Y} \}
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    \{ \Gamma \mathbf{X} \overset{\Gamma(f)}{\to} \Gamma \mathbf{Y} \}
    &\longleftarrow&
    \{ \mathbf{X} \overset{\eta^\sharp_{\mathbf{Y}} \circ f}{\longrightarrow} coDisc \Gamma \mathbf{Y} \}    
  }
$$

Chasing the [[identity morphism]] $id_{\Gamma \mathbf{Y}}$ through this diagram, yields the claimed equality, as shown on the right. Here we use that the right [[adjunct]] of the [[identity morphism]] is the [[adjunction unit]], as shown.

The second equality is [[formal duality|fomally dual]]:

$$
  \array{
    Hom_{\mathbf{B}}( \Gamma \mathbf{X}, \Gamma \mathbf{X})
    &\overset{\widetilde { (-) }}{\longrightarrow}&
    Hom_{\mathbf{H}}( Disc \Gamma \mathbf{X}  , \mathbf{X})
    \\
    {}^{\mathllap{ Hom_{\mathbf{B}}( \Gamma \mathbf{X}, \Gamma(f) )  }}
    \big\downarrow
    &&
    \big\downarrow^{ \mathrlap{ Hom_{\mathbf{X}}( Disc \Gamma \mathbf{X}, f ) 
} }
    \\
    Hom_{\mathbf{B}}( \Gamma \mathbf{X}, \Gamma \mathbf{Y} )
    &\overset{ \widetilde{ (-) } }{\longleftarrow}&
    Hom_{\mathbf{H}}( Disc \Gamma \mathbf{X}, \mathbf{Y} )
  }
  \phantom{AAAAA}
  \array{
     \{ \Gamma \mathbf{X} \overset{id_{\Gamma \mathbf{X}}}{\to} \Gamma \mathbf{X} \}
     &\longrightarrow&
     \{ Disc \Gamma \mathbf{X} \overset{\epsilon^{\flat}_X}{\to} \mathbf{X} \}
     \\
     \big\downarrow 
       &&
     \big\downarrow
     \\
     \{ \Gamma \mathbf{X} \overset{\Gamma(f)}{\to} \Gamma(\mathbf{Y}) \}
     &\longleftarrow& \{ Disc \Gamma \mathbf{X} \overset{f\circ \epsilon^\flat_{\mathbf{X}}  }{\longrightarrow} \mathbf{Y}\}
  }
$$


=--

+-- {: .num_prop #PiecesHavePointsIsDiscreteObjectsAreConcrete}
###### Proposition
**([[pieces have points]] $\simeq$ [[discrete objects are concrete]])**

Consider an [[adjoint quadruple]] of the form 

$$
  \Pi \dashv Disc \dashv \Gamma \dashv coDisc
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{\phantom{AA} \Pi \phantom{AA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookleftarrow}
    }
  \mathbf{B}
$$

(for instance a [[cohesive topos]] over some [[base topos]] $\mathbf{B}$).

Then the following are equivalent:

1. [[pieces have points]]: 

   1. as seen in $\mathbf{B}$: For every [[object]] $X \in \mathbf{X}$ the [[points-to-pieces transform]] (Prop. \ref{PointsToPiecesTransform}) in $\mathbf{B}$ (eq:PointsToPiecesInTheBase) is an [[epimorphism]]:

   $$
     ptp_{\mathbf{B}}
     \;\colon\;
     \Gamma X \overset{ epi }{\longrightarrow} \Pi X
   $$

   1. equivalently, as seen in $\mathbf{H}$: For every [[object]] $X \in \mathbf{X}$ the [[points-to-pieces transform]] (Prop. \ref{PointsToPiecesTransform}) in $\mathbf{H}$ (eq:PointsToPieces) is an [[epimorphism]]:

   $$
     ptp_{\mathbf{H}}
     \;\colon\;
     \flat X \overset{ epi }{\longrightarrow} &#643; X
   $$

1. [[discrete objects are concrete]]: For every [[object]] $S \in \mathbf{B}$ the [[discrete object]] $Disc(S)$ is a [[concrete object]], in that the [[sharp modality|sharp]] [[adjunction counit]] on $Disc(S)$ is a [[monomorphism]]:

   $$
     \eta^\sharp_{Disc(S)}
     \;\colon\;
     Disc S
       \overset{ mono }{\longrightarrow}
     \sharp Disc S
   $$
   
=--

+-- {: .proof}
###### Proof

First observe the equivalence of the first two statements:

$$
  ptp_{\mathbf{H}} \;\; \text{is epi}
  \phantom{AAA}
  \text{iff}
  \phantom{AAA}
  ptp_{\mathbf{B}} \;\; \text{is epi}
  \,.
$$

In one direction, assume that $ptp_{\mathbf{B}}$ is an epimorphism. By (eq:PiecesToPointsFromBase) we have $ptp_{\mathbf{H}} = Disc(ptp_{\mathbf{B}})$, but $Disc$ is a [[left adjoint]] and left adjoints preserve epimorphisms.

In the other direction, assume that $ptp_{\mathbf{H}}$ is an epimorphism. By (eq:PointsToPiecesInTheBase) and (eq:AdjunctOfptpH) we see that $ptp_{\mathbf{B}}$ is re-obtained from this by applying $\Gamma$ and then composition with isomorphisms. But $\Gamma$ is again a left adjoint, and hence preserves epimorphisms, as does composition with isomorphisms.

By applying (eq:PointsToPiecesInTheBase) again, we find in particular that _[[pieces have points]]_ is also equivalent to $\Pi \epsilon^\flat_{Disc S}$ being an epimorphism, for all $S \in \mathbf{B}$. But this is equivalent to

$$
  Hom_{\mathbf{B}}(\Pi \epsilon^\flat_{\mathbf{X}}, S)
  =
  Hom_{\mathbf{\mathbf{H}}}(\epsilon^\flat_{\mathbf{X}}, Disc(S))  
$$

being a [[monomorphism]] for all $S$ (by adjunction isomorphism and definition of [[epimorphism]]).

Now by Lemma \ref{ReExpressingMiddleFunctorInAdjointTriple}, this is equivalent to

$$
  Hom_{\mathbf{H}}( \mathbf{X}, \eta^\sharp_{Disc(S)} )
$$

being a monomorphism, which is equivalent to $\eta^\sharp_{Disc(S)}$ being a monomorphism, hence to _[[discrete objects are concrete]]_.


=--




+-- {: .num_example }
###### Example

In [[infinitesimal cohesion]] the [[points-to-pieces transform]], def. \ref{TransformationFromPointsToPieces}, is required to be an [[equivalence]].

=--

+-- {: .num_example }
###### Example

In [[tangent cohesion]] the [[points-to-pieces transform]], def. \ref{TransformationFromPointsToPieces}, is part of the canonical [[differential cohomology diagram]].

=--



This condition _[[pieces have points]]_ may also be expressed as follows:

+-- {: .num_prop #RelationOfPiecesToPointsToInitialAufhebung}
###### Proposition

If $\flat \to \int$ is epi, then there is [[Aufhebung]] of the initial opposition, in that $\sharp \emptyset \simeq \emptyset$. Conversely if this holds and the [[base topos]] is a [[Boolean topos]], then $\flat \to \int$ is epi.

=--

This is [Lawvere-Menni 15, lemma 4.1, 4.2](#LawvereMenni15).





+-- {: .num_defn #PiecesOfPowersArePowersOfPieces}
###### Definition

We say **pieces of powers are powers of pieces** if for all $S \in \mathcal{S}$ and $X \in E$ the natural morphism

$$
  f_! (X^{f^* S}) \stackrel{\simeq}{\longrightarrow} (f_!(X))^S
$$

is an [[isomorphism]].

=--

+-- {: .num_remark }
###### Remark

This morphism is the [[internal hom]]-[[adjunct]] of 

$$
  S \times f_!(X^{f^* S}) 
   \stackrel{\simeq}{\longrightarrow}
  f_!f^*(S) \times f_!(X^{f^* S})
   \stackrel{\simeq}{\longrightarrow}
  f_!(f^*(S) \times X^{f^* S})
  \longrightarrow
  f_!(X)
$$

where we use that by definition $f^*$ is [[full and faithful functor|full and faithful]] and then that $f_!$ preserves [[product]]s).

=--


These extra axioms are proposed in ([Lawvere, Axiomatic cohesion](#LawvereAxiomatic)). 

+-- {: .num_defn #SubobjectClassifierIsConnected}
###### Definition

For $f : \mathcal{E} \to \mathcal{S}$ a cohesive topos, we say that 
its **subobject classifier is connected** if for the [[subobject classifier]] $\Omega \in \mathcal{E}$ we have

$$
  f_!(\Omega) \simeq *
  \,.
$$

This implies that for all $X \in \mathcal{E}$ also $f_! \Omega^X \simeq *$.


=--

This appears as axiom 2 in ([Lawvere, Categories of spaces](#LawvereCatsOfSpaces)).

+-- {: .num_remark}
###### Remark

There is some overlap between the structures and conditions appearing here and those considered in the context of [[Q-categories]]. See there for more details.

=--

Another axiom to consider, also introduced by [[Lawvere]] (see at _[[Aufhebung]]_):

+-- {: .num_defn #AufhebungOfBecoming}
###### Definition

Say that a cohesive topos, def. \ref{CohesiveTopos}, has _[[Aufhebung]] of [[becoming]]_ if the [[sharp modality]], def. \ref{AdjointTriple}, preserves the [[initial object]]

$$
  \sharp \emptyset \simeq \emptyset
  \,.
$$

=--

+-- {: .num_example}
###### Example

The Aufhebungs axiom def. \ref{AufhebungOfBecoming} is satisfied by all cohesive toposes with a [[cohesive site]] of definition, see at _[Aufhebung -- Over cohesive sites](Aufhebung#ExamplesBecomingFormalization)_.

=--

+-- {: .num_remark}
###### Remark

In the Aufhebungs-axiom of def. \ref{AufhebungOfBecoming}, the extra exactness condition on the [[shape modality]] in def. \ref{CohesiveTopos}, which says (in particular) that shape preserves the [[terminal object]]

$$
  &#643; \ast \simeq \ast
$$


finds a dual companion. It might make sense to consider the variant of the axioms of cohesion which say

1. there is an [[adjoint triple]] of idempotent (co-)monads $&#643; \dashv \flat \dashv \sharp$;

1. such that $\sharp$ satisfies Aufhebung and $&#643;$ satisfies co-Aufhebung.



=--


## Properties 
  {#Properties}

We discuss properties of cohesive toposes. In 


* [Relations between the axioms](#RelationsBetweenTheAxioms)

we comment on the interdependency of the collection of axioms on a cohesive topos. In

* [Quasitopos of concrete objects](#ConcreteObjects)

we discuss the induced notion of concrete objects that comes with every cohesive topos and in

* [Objects with one point per cohesive piece](#ObjectsWithOnePointPerCohesivePiece)

the induced subcategory of objects with one point per piece.

Some of these phenomena have a natural 

* [Modality interpretation](#Modality).

For a long list of further structures that are canonically present in a cohesive context see

* [[cohesive (∞,1)-topos -- structures]]

For more structure available with a few more axioms see at 


* [[differential cohesion]]

* [[tangent cohesion]].

$\,$

$\,$

### Relations between the axioms
  {#RelationsBetweenTheAxioms}

We record some relations between the various axioms characterizing cohesive toposes.

+-- {: .num_prop #PiecesHavePointsEquivalentToDiscreteObjectsAreConcrete}
###### Proposition

The axioms [pieces have points](#PiecesHavePoints) and [discrete objects are concrete](#DiscreteObjectsAreConcrete) are equivalent.

=--

This is just a reformulation of the [above proposition](#TheEpiAndTheMono).

+-- {: .num_prop}
###### Proposition

A [[sheaf topos]] that

1. is [[locally connected topos|locally connected]] and [[connected topos|connected]];

1. satisfies [pieces have points](#PiecesHavePoints)

also is

1. [[local topos|local]];

1. [[hyperconnected topos|hyperconnected]];

1. [[strongly connected topos|strongly locally connected]]

1. [cohesive](#CohesiveTopos).

=--

The statement of the first items appears as ([Johnstone 11, prop. 1.6](#Johnstone11)). The last item is then a consequence by definition.

+-- {: .num_prop #HyperconnectivityAndPiecesHavePoints}
###### Proposition

For a [[sheaf topos]] the condition that it

1. is [[locally connected topos|locally connected]];

1. is [[connected topos|connected]];

1. satisfies [pieces have points](#PiecesHavePoints)

is equivalent to the condition that it

1. is [[locally connected topos|locally connected]];

1. is [[hyperconnected topos|hyperconnected]];

1. is [[local topos|local]].

=--

This is ([Johnstone 11, theorem 3.4](#Johnstone11)).

### Subcategories of discrete and codiscrete objects

+-- {: .num_prop }
###### Proposition

The [[reflective subcategories]] of [[discrete objects]] and of [[codiscrete objects]] are both [[exponential ideals]].

=--

+-- {: .proof}
###### Proof

By the discussion at [[exponential ideal]] a reflective subcategories of a [[cartesian closed category]] is an exponential ideal precisely if the [[reflector]] preserves [[products]]. For the [[codiscrete objects]] the reflector $\Gamma$ preserves even all [[limits]] and for the [[discrete objects]] the reflector $\Pi$ does so by assumption of strong connectedness.

=--

### Quasitoposes of concrete objects 
  {#ConcreteObjects}

A cohesive topos comes canonically with various [[subcategories]], sub-[[quasi-toposes]] and [[subtopos]]es of interest. We discuss some of these.


+-- {: .num_lemma}
###### Observation

For $(\Pi \dashv \Disc \dashv \Gamma \dashv coDisc) :  \mathcal{E} \to Set$ a cohesive topos, $(\Gamma \dashv coDisc)$ exhibits $Set$ as a [[subtopos]]

$$
  (\Gamma \dashv \coDisc) : Set \stackrel{\leftarrow}{\hookrightarrow}
  \mathcal{E}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By general properties of [[local topos]]es. See there.

=--

+-- {: .num_lemma}
###### Observation

The category $Set$ is equivalent to the full [[subcategory]] of $\mathcal{E}$ on those objects $X \in \mathcal{E}$ for which the $(\Gamma \dashv coDisc)$ [[unit of an adjunction|unit]]

$$
  X \to coDisc \Gamma X
$$

is an [[isomorphism]].

=--

+-- {: .proof}
###### Proof

By general properties of [[reflective subcategories]]. See there for details.

=--

+-- {: .num_defn}
###### Definition

An object $X$ of the cohesive topos $\mathcal{E}$ for which $X \to coDisc \Gamma X$ is a [[monomorphism]] we call a **concrete object**. 


Write 

$$Conc(\mathcal{E}) \hookrightarrow \mathcal{E}$$

for the [[full subcategory]] on concrete objects.

=--

+-- {: .num_prop}
###### Proposition

The functor $\Gamma : \mathcal{E} \to Set$ is a [[faithful functor]] on morphisms $(X \to Y) \in \mathcal{E}$ precisely if $Y$ is a concrete object.

In particular, the restriction $\Gamma : Conc(\mathcal{E}) \to Set$ makes the category of concrete objects a [[concrete category]].

=--

+-- {: .proof}
###### Proof

Observe that the composite morphism

$$
  F 
  : 
  \mathcal{E}(X,Y) \stackrel{\Gamma}{\longrightarrow} \mathcal{S}(\Gamma X, \Gamma Y)
  \stackrel{\simeq}{\longrightarrow}
  \mathcal{E}(X, coDisc \Gamma Y)
$$

is given (see [[adjunct]]) by postcomposition with the $(\Gamma \dashv coDisc)$-[[unit of an adjunction|unit]] $\eta_Y : Y \to coDisc \Gamma Y$

$$
  \array{
    X &\to& Y
    \\
    \downarrow && \downarrow
    \\
    coDisc \Gamma X &\to& coDisc \Gamma Y
  }
  \,.
$$

The condition that $Y$ is a concrete object, hence that $Y \to coDisc \Gamma Y$ is a [[monomorphism]] is therefore equivalent (see there) to the condition that $F$ is a monomorphism, which is equivalent to $F$ being a [[faithful functor]].

=--

+-- {: .num_remark}
###### Remark

This means that in the formal sense discussed at [[stuff, structure, property]] we may regard $Conc(\mathcal{E})$ as a category of sets _equipped with cohesive structure_ .

=--


+-- {: .num_prop}
###### Proposition


The category $Conc(\mathcal{E})$ is a [[quasitopos]] and a [[reflective subcategory]] of $\mathcal{E}$.

=--

+-- {: .proof}
###### Proof


Let $(C,J)$ be a [[site]] of definition for $\mathcal{E}$ with [[coverage]] $J$, so that $\mathcal{E} = Sh_J(C) \hookrightarrow PSh(C)$. Since $Set \stackrel{CoDisc}{\hookrightarrow} \mathcal{E}$ is a subtopos, we have that $Set$ is itself a [[category of sheaves]] on $C$

$$
  Set \simeq Sh_K(C) \stackrel{CoDisc}{\hookrightarrow} Sh_J(C) \hookrightarrow PSh(C)
$$

which must correspond to another [[coverage]] $K$:  $Set \simeq Sh_K(C)$. Since we have this sequence of inclusions, we have an inclusion of coverages $J \subset K$. We observe that the concrete objects in $\mathcal{E}$ are precisely the $(J,K)$-[[biseparated presheaves]] on $C$. The claim then follows by standard facts of quasitoposes of biseparated presheaves.

=--

+-- {: .num_prop}
###### Proposition

Precisely if the cohesive topos $\mathcal{E}$ satisfies the axiom _[[discrete objects]] are [[concrete object|concrete]]_ (saying that for all $S \in Set$ the canonical morphism $Disc S \to coDisc \Gamma Disc S \simeq coDisc S$ is a [[monomorphism]]) then $Conc(\mathcal{E})$ is a **cohesive quasitopos** in that we have a quadrupled of [[adjoint functor]]s.

$$
   Conc(\mathcal{E})
    \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
  Set
  \,.
$$

=--

+-- {: .proof}
###### Proof

The axiom says precisely that the functor $Disc : Set \to \mathcal{E}$ factors through $Conc(\mathcal{E})$. Also $coDisc : Set \to \mathcal{E}$ clearly factors through $Conc(\mathcal{E})$. Since $Conc(\mathcal{E})$ is a [[full subcategory]] therefore the restriction of $\Gamma$ and $\Pi$ to  $Conc(\mathcal{E})$ yields a quadruple of adjunctions as indicated.


Since by reflectivity [[limit]]s in $Conc(\mathcal{E})$ may be computed in $\mathcal{E}$, $\Pi$ preserves finite products on $Conc(\mathcal{E})$.



=--

### Objects with one point per cohesive piece
 {#ObjectsWithOnePointPerCohesivePiece}

+-- {: .num_theorem}
###### Theorem


Let $(\Pi \dashv Disc \dashv \Gamma \dashv Codisc) :  \mathcal{E} \to \mathcal{S}$ be a cohesive topos with $\Gamma X \to \Pi X$ an [[epimorphism]] for all $X$.

Let $s^* : \mathcal{L} \hookrightarrow \mathcal{E}$ be the [[full subcategory]] on those objects $X$ for which $\Gamma X \to \Pi X$ is an [[isomorphism]]. Then

1. $\mathcal{L}$ is a [[reflective subcategory]] and a [[coreflective subcategory]]

   $$
     (s_! \dashv s^* \dashv s_*)
     : 
     \mathcal{E}
       \stackrel{\overset{s_!}{\longrightarrow}}{\stackrel{\overset{s^*}{\leftarrow}}{\underset{s_*}{\longrightarrow}}}
     \mathcal{L} 
   $$

1. $s_*$ preserves [[coproduct]]s.

1. the components of the reflector $X \to s_! s^* X$ are [[epimorphism]]s.

=--

This is [theorem 2](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf#page=5) in ([Lawvere](#Lawvere)).

+-- {: .proof}
###### Proof

Since $\Gamma$ is a [[left adjoint]] it preserves [[colimit]]s, as does of course $\Pi$. Therefore the collection of objects for which $\Gamma X \to \Pi X$ is an isomorphism is closed under colimits and hence $\mathcal{L}$ has all colimits and the inclusion $s^* : \mathcal{L} \hookrightarrow \mathcal{E}$ obviously preserves them. 

To apply the [[adjoint functor theorem]] to deduce that therefore $s^*$ has a right adjoint $s_*$ it is sufficient to argue that $\mathcal{L}$ is a [[locally presentable category]]. To see this, notice that $\mathcal{L} \hookrightarrow \mathcal{E}$ is the [[inverter]] of $\Gamma \to \Pi$, a certain [[2-limit]] in [[Cat]].  Since the 2-category of [[accessible categories]] and [[accessible functors]] is closed under (non-strict) [[2-limit]]s in [[Cat]], it follows that $\mathcal{L}$ is accessible. Since we already know that it is also cocomplete it follows that it must be locally presentable.

Since $\Pi$ by assumption preserves finite products and $\Gamma$ preserves all products, it follows that $L$ is also closed under finite products and in particular contains the [[terminal object]] $*$. Since $\mathcal{E}$, being a [[topos]], is an [[extensive category]], it follows that $s_*$ preserves coproducts.

(...details...)

Using that $\Gamma X \to \Pi X$ is an epi, we find that $\mathcal{L}$ is also closed under [[subobject]]s: if $Y \hookrightarrow X$ is a [[monomorphism]] then if in

$$
  \array{
     \Gamma Y &\to& \Gamma X
     \\
     \downarrow && \downarrow^{\mathrlap{\simeq}}
     \\
     \Pi Y &\to& \Pi X
  }
$$

the right vertical morphism is an iso, then so is the left vertical one.

(...details...).

It then also follows that $\mathcal{L}$ is closed under arbitrary products.

(...details...)

This implies the existence of $s_!$ and the fact that $X \to s^* s_! X$ is epi.

(...details...)

=--


### Internal modal logic
  {#Modality}

Every [[topos]] $\mathcal{E}$ comes with its [[internal logic]]. From this internal perspective, the existence of extra external functors on $\mathcal{E}$ -- such as the $\Pi_0$ and the $coDisc$ on a cohesive topos -- is manifested by the existence of extra internal logical operators. These may be understood as _modalities_ equipping the internal logic with a structure of a [[modal logic]].

For the case of [[local toposes]], of which cohesive toposes are a special case, this internal modal interpretation of the extra external functor $coDisc$ has been noticed in ([AwodeyBirkedal, section 4.2](#AwodeyBirkedal)). (Beware that in that reference the symbols "$\flat$" and "#" are used precisely oppositely to their use here).

+-- {: .num_defn #DiscreteModality}
###### Definition


For $\phi \hookrightarrow A$ a [[monomorphism]] in a cohesive topos, hence a [[proposition]] of [[type]] $A$ in the [[internal logic]], we say that it is  _discretely true_ if the [[pullback]]  $# \phi|_A \to A$ in

$$
  \array{
    #\phi |_A &\to& # \phi
    \\  
    \downarrow && \downarrow
    \\
    A &\to& # A
  }
$$

is an [[isomorphism]], where $A \to # A$ is the $(\Gamma\dashv coDisc)$-[[unit of an adjunction|unit]] on $A$.

=--

+-- {: .num_remark }
###### Remark

If a proposition $\phi$ is true over all discrete objects, then it is discretely true. More precisely,
if for $X = \mathbf{\flat} X$ any discrete object we have that 

$$
  \mathcal{E}(X, \phi)
  \to 
  \mathcal{E}(X, A)
$$

is an isomorphism, then $\phi$ is discretely true.

Because if so, then 

$$
  \mathcal{E}(\flat X , \phi)
  \to
  \mathcal{E}(\flat X , A)  
$$

is an isomorphism and hence 

$$
  \mathcal{E}(\Gamma X , \Gamma \phi)
  \to
  \mathcal{E}(\Gamma X , \Gamma A)  
$$

is for all $X$. Therefore in this case $\Gamma \phi \to \Gamma A$ is an isomorphism and hence so is $# \phi \to # A$.

=--

+-- {: .num_example }
###### Example

For $\mathcal{E} = Sh(CartSp)$ the [[sheaf topos]] over [[CartSp]]${}_{smooth}$ ([[smooth infinity-groupoid|smooth spaces]]) and $\Omega^n_{cl}(-) \hookrightarrow \Omega^n(-)$ the inclusion of all closed $n$-[[differential forms]] into all $n$-forms, the proposition is "the $n$-form $\omega$ is closed". This is of course not true generally, but it is discretely true: over a [[discrete space]] every form is closed.

=--

## Examples

### Over a discrete site

We discuss some cohesive toposes over [[sites]] $C$ with trivial [[coverage]]/[[Grothendieck topology|topology]], so that the [[category of sheaves]] is the [[category of presheaves]]

$$
  Sh(C) \simeq PSh(C)
  \,.
$$

#### Families of sets -- the Sierpinski topos
  {#FamiliesOfSets}

We discuss an example of a cohesive topos over a [[cohesive site]] that is about the simplest non-trivial example that there is: the [[Sierpinski topos]]. Simple as it is, it does serve to already illustrate some key points. The following site is in fact also an [[∞-cohesive site]] and hence there is a corresponding example of a [[cohesive (∞,1)-topos]]: the [[Sierpinski (∞,1)-topos]].

Consider the site given by the [[interval category]] 

$$
  C = \{\emptyset \to *\}
$$

equipped with trivial [[Grothendieck topology|topology]]. This evidently has an [[initial object]] $\emptyset$ (which makes it [[cosifted category|cosifted]]) and a [[terminal object]] $*$.

The [[category of sheaves]] = [[category of presheaves|presheaves]] on this is the [[arrow category]] 

$$
  Sh(\{\emptyset \to *\})
  \simeq
   PSh(\{\emptyset \to *\})
  \simeq
  Arr(Set)
$$

since a presheaf $X$ on $C$ is given by a morphism

$$
  X : (\emptyset \to *) \mapsto (I \leftarrow S)
$$

in [[Set]]. We find

* $\Gamma : (I \leftarrow S) \mapsto S$

* $\Pi_0 : (I \leftarrow S) \mapsto I$.

Trivial as this is, it does provide some insight into the interpretation of cohesiveness: by decomposing $S$ into its [[fiber]]s, an object $(I \leftarrow S)$ is an $I$-indexed family of sets: $S = \coprod_i S_i$. The "cohesive pieces" are the $S_i$ and there are $|I|$-many of them. This is what $\Pi_0$ computes, which clearly preserves products.

Moreover we find for $K \in Set$:

* $Disc : K \mapsto (K \stackrel{Id}{\leftarrow} K)$;

* $CoDisc : K \mapsto (* \stackrel{}{\leftarrow} K)$

(and evidently both these functors are full and faithful).

This matches the interpretation we just found: $Disc K$ is the collection of elements of $K$ with no two of them lumped together by cohesion, while $Codisc K$ is all elements of $K$ lumped together.

The canonical morphism 

$$
  \Gamma (I \leftarrow S) \to \Pi_0 (I \leftarrow S)
$$

is

$$
  \Gamma Disc \Gamma (I \leftarrow S) \to \Gamma (I \leftarrow S) \to \Gamma Disc \Pi_0 (I \leftarrow S)
  \,.
$$

Plugging in the above this is just

$$
  S \to I
$$

itself. Indeed, by the above interpretation, this sends each point to its cohesive component. It is not an epimorphism in general, because the fiber $S_i$ over an element $i$ may be empty: the cohesive component $i$ may have no points.


#### Over a site with initial and terminal object

The [above](#FamiliesOfSets) example is the simplest special case of a more general but still very simple class of examples. 

First notice that for $C$ any [[small category]], we have the left and right [[Kan extension]] of presheaves $F : C^{op} \to Set$ along the [[functor]] $C^{op} \to *$. By definition, this are the [[colimit]] and [[limit]] functors

$$
  (\lim_\to \dashv Const \dashv \lim_\leftarrow) :
  PSh(C) \stackrel{\overset{\lim_{\to}}{\longrightarrow}}{\stackrel{\overset{Const}{\leftarrow}}{\underset{\lim_\leftarrow}{\longrightarrow}}}
  Set
  \,.
$$

+-- {: .num_lemma}

###### Observation

If $C$ has a [[terminal object]] $*$ then 

* the colimit is given by evaluation on this object;

* there is a further [[right adjoint]] $(\lim_\leftarrow \dashv CoConst)$

  given by

  $$
    CoConst : S \mapsto (c \mapsto Set(C(*,c), S)
    \,.
  $$

=--

+-- {: .proof}
###### Proof

The terminal object of $C$ is the [[initial object]] of the [[opposite category]] $C^{op}$ and therefore the limit over any functor $F : C^{op} \to Set$ is given by evaluation on this object

$$
  \lim_\leftarrow (C^{op} \stackrel{F}{\to} Set) \simeq F(*)
  \,.
$$

To see that we have a pair of [[adjoint functor]]s $(\lim_\to \dashv CoConst)$
we check the natural [[hom-set]] equivalence 
$PSh_C(F, CoConst S ) \simeq Set(\lim_\to F , S)$ by computing

$$
  \begin{aligned}
    PSh_C(F , CoConst S) 
     & \simeq 
      \int_{c \in C} Set(F(c), Set(C(*,c), S))
    \\
    & \simeq
        \int_{c \in C} Set(F(c) \times C(*,c), S)
    \\
     & \simeq 
         Set( \int^{c \in C} F(c) \times C(*,c) , \; S)
    \\
     & \simeq Set(F(*), S)
  \end{aligned}
  \,,
$$

Here the first step is the expression of [[natural transformation]]s by [[end]]-calculus, the second uses the fact that [[Set]] is a [[cartesian closed category]], the third uses that any [[hom-functor]] sends [[coend]]s in the first argument to ends, and the last one uses the [[co-Yoneda lemma]].

=--

The formal dual of this statement is the following.

+-- {: .num_lemma}
###### Corollary

If $C$ has an [[initial object]] $\emptyset$ then 

* the limit is given by evaluation on this object;

* there is a further [[left adjoint]] $(L \dashv \lim_\to)$,

  so that $\lim_\to$ preserves all small limits and in particular
  all finite products.

=--

In summary we have

+-- {: .num_lemma}
###### Proposition

If $C$ has both an [[initial object]] $\emptyset$ as well as a [[terminal object]] $*$ then there is a quadruple of adjoint functors

$$
  (\Pi_0 \dashv Disc \dashv \Gamma \dashv CoDisc)
   :
   PSh(C) \to Set
  \,,
$$

where

* $\Gamma$ is given by evaluation on $*$;

* $\Pi_0$ is given by evaluation of $\emptyset$ and preserves products.

=--

The above interpretation of the cohesiveness encoded by $C = \{\emptyset \to *\}$ still applies to the general case: a general object $X \in PSh(C)$ is, by restriction to the unique morphism $\emptyset \to *$ in $C$ a set-indexed  family of sets

$$
  X(\emptyset \to *) = (\Pi_0(X) = X(\emptyset) \leftarrow  X(*) = \Gamma(X))
$$

and $\Gamma$ picks out the total set of points, while $\Pi_0$ picks of the indexing set ("of cohesive components"). The extra information for general $C$ with initial and terminal object is that for every object $c \in C$ these cohesive lumps of points are refined to a hierarchy of lumps and lumps-of-lumps

$$
  X(\emptyset \to c \to *) = (\Pi_0(X) \leftarrow X(c) \leftarrow \Gamma(X))
  \,.
$$ 



#### Reflexive directed graphs {#Graphs}

+-- {: .num_prop}
###### Proposition

The category $RDGraph$ of reflexive [[directed graphs]] is a cohesive topos. 

The category $DGraph$ of just directed graphs, not necessarily reflexive, is _not_ a cohesive topos.

=--

This example was considered in ([Lawvere, Categories of spaces](#LawvereCatsOfSpaces)) as a simple test case for two very similar toposes, one of which is cohesive, the other not. 

We spell out some details on the cohesive topos of reflexive directed graphs.

+-- {: .num_defn}
###### Definition

Let $\mathbf{B}End(\Delta[1])$ be the one-object category coming from the [[monoid]] with three [[idempotent]] elements $\{Id, \sigma, \tau\}$

* $\sigma \circ  \sigma = \sigma$

* $\tau \circ  \tau = \tau$

* $ \tau \circ \sigma = \tau$

* $ \sigma \circ \tau = \sigma$

=--

A presheaf $X : C^{op} \to Set$ on this is a _reflexive [[directed graph]]_ : the set $X(\bullet)$ is the set of all edges and vertices regarded as identity edges, the projection

$$
  s := X(\sigma) : X \to X
$$

sends each edge to its source and the projection

$$
  t := X(\tau) : X \to X
$$

sends each edge to its target. The identities

$$
  s \circ t = t
$$

and

$$
  t \circ s = s
$$

express the fact that source and target are identity edges. 

Equivalently, this is a presheaf on the full [[subcategory]] $\Delta_{\leq [1]} \subset \Delta$ of the [[simplex category]] on the objects $[0]$ and $[1]$

$$
  \Delta_{\leq [1]} = ([1] \stackrel{\overset{\tau}{\leftarrow}}{\stackrel{\to}{\underset{\sigma}{\leftarrow}}} [0])
  \,.
$$

In fact this is the [[Cauchy completion]] of $\mathbf{B}End(\Delta[1])$, obtained by [[split idempotent|splitting the idempotents]].

In summary this shows that

+-- {: .num_prop}
###### Observation

We have an [[equivalence of categories]]

$$
  RDGraph \simeq PSh(\mathbf{B} End(\Delta[1])) \simeq PSh(\Delta_{\leq [1]})
  \,.
$$

=--

To see that this presheaf topos is cohesive, notice that the terminal geometric morphism

$$
  (Disc \dashv \Gamma) : Psh(C) \to Set
$$

$Disc S$ is the reflexive directed graph with set of vertices $S$ and no non-identity morphisms and $\Gamma X$ is the set of vertices = identity edges.

The extra left adjoint $\Pi_0 : PSh(C) \to Set$ sends a graph to its set of connected components, the [[coequalizer]] of the source and target maps

$$
  X_1 \stackrel{\overset{t}{\to}}{\underset{s}{\to}} X_0 \to \Pi_0 X
  \,.
$$

Since this is a [[reflexive coequalizer]] (by the existence of the unit map $X([1] \to [0])$) it does preserve products (as discussed there). This is the property that fails for the topos $DGraph$ of all directed graphs: a general coequalizer does not preserve products.

And $CoDisc : Set \to PSh(C)$ sends a set $S$ to the reflexive graph with vertices $S$ and one edge for every ordered pair of vertices (the [[indiscrete category|indiscrete]] or _chaotic_ graph).

The canonical morphism $\Gamma X \to \Pi_0 X$ sends each vertex to its connected component. Evidently this is epi, hence in $RDGraphs$ _cohesive pieces have points_ .

#### Simplicial sets {#SimplicialSets}

Let $C = \Delta$ be the [[simplex category]], regarded as a [[site]] with the trivial [[coverage]].

The corresponding [[sheaf topos]] $Sh(\Delta)$ is the [[presheaf topos]] $E = PSh(\Delta) = $ [[sSet]] of [[simplicial sets]]. 

Notice that reflexive [[directed graphs]] are equivalently [[simplicial skeleton|skeleta]] of [[simplicial sets]].

+-- {: .num_prop}
###### Proposition

The category [[sSet]] of simplicial sets is a [[cohesive topos]] in which _[[points-to-pieces transform|cohesive pieces have points]]_ . 

=--



We have for $X \in sSet$

* $\Gamma : X \mapsto X_0$;

* $\Pi_0 : X \mapsto \pi_0(X) = X_0/X_1$, the set of [[simplicial homotopy group|connected components]].

And for $S \in Set$:

* $Disc S$ the constant simplicial set on $S$;

* $Codisc S$ the simplicial set which in degree $k$ has the set of $(k+1)$-tuples of elements of $S$.


If $X, Y \in sSet$ are [[Kan complex]]es, then $\Pi_0(Y^X)$ is the set of [[simplicial homotopy]]-classes of maps $X \to Y$. We can therefore write the [[homotopy category]] of Kan complexes as

$$
  Ho_{KanCplx}(X,Y) = \Pi_0(Y^X)
  \,.
$$


### Over a cohesive site
 {#OverACohesiveSite}

We discuss here presentations of [[cohesive toposes]] as [[categories of sheaves]] over [[sites]] equipped with suitable [[extra properties]]: "[[cohesive sites]]" (Def. \ref{OneCohesiveSite}) below. The definition is readily motivated from the following basic Example \ref{PresheavesAdjointQuadrupleOnSiteWithTerminalObject}, which constitutes the special case of [[cohesive sites]] with [[trivial coverage]]:

+-- {: .num_example #PresheavesAdjointQuadrupleOnSiteWithTerminalObject}
###### Example
**([[adjoint quadruple]] of [[presheaves]] over [[site]] with [[terminal objects]])**

Let $\mathcal{C}$ be a [[small category]] with [[finite products]] (hence with a [[terminal object]] $\ast \in \mathcal{C}$ and for any two [[objects]] $X,Y \in \mathcal{C}$ their [[Cartesian product]] $X \times Y \in \mathcal{C}$).

Then there is an [[adjoint quadruple]] of [[functors]] between the [[category of presheaves]] over $\mathcal{C}$ ([this def.](geometry+of+physics+--+categories+and+toposes#CategoryOfPresheaves)), and the [[category of sets]] ([this Def.](geometry+of+physics+--+categories+and+toposes#CategoryOfSets))

\[
  \label{PreaheafAdjointQuadruple}
  [\mathcal{C}, Set]
    \array{
      \overset{\phantom{AAA} \Pi_0 \phantom{AAA}}{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookleftarrow}
    }
  Set
\]

such that:

1. the functor $\Gamma$ sends a [[presheaf]] $\mathbf{Y}$ to its set of [[global sections]], which here is its value on the [[terminal object]]:
   
   \[
     \label{CohesiveGlobalSectionsGivenByPointEvaluation}
     \begin{aligned}
       \Gamma \mathbf{Y}
       & =
       \underset{\underset{\mathcal{C}}{\longleftarrow}}{\lim}
       \mathbf{Y}
       \\
       & \simeq 
       \mathbf{Y}(\ast)
     \end{aligned}
   \]

1. $Disc$ and $coDisc$ are [[full and faithful functors]] ([this def.](geometry+of+physics+--+categories+and+toposes#FullyFaithfulFunctor)).

1. $\Pi_0$ preserves [[finite products]]: 

   for $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$, we have a [[natural bijection]]
  
   $$
     \Pi_0(\mathbf{X} \times \mathbf{Y}) 
     \;\simeq\; 
     \Pi_0(\mathbf{X}) \times \Pi_0(\mathbf{Y})
     \,.
   $$

Hence the [[category of presheaves]] over a [[small category]] with [[finite products]] is a [[cohesive topos]] (Def. \ref{CohesiveTopos}).

=--

+-- {: .proof}
###### Proof

The existence of the [[terminal object]] in $\mathcal{C}$ means equivalently, (by [this Example](geometry+of+physics+--+Categories+and+Toposes#InitialCategoryAndTerminalCategory)) that there is an [[adjoint pair]] of [[functors]] between $\mathcal{C}$ and the [[terminal category]] ([this def.](geometry+of+physics+--+categories+and+toposes#InitialCategoryAndTerminalCategory)):

$$
  \ast
    \underoverset
    {\underset{}{\hookrightarrow}}
    {\overset{p}{\longleftarrow}}
    {\bot}
   \mathcal{C}
$$

whose [[right adjoint]] takes the unique object of the terminal category to that terminal object.

From this it follows (by [this example](geometry+of+physics+--+Categories+and+Toposes#KanExtensionOfAdjointPairIsAdjointQuadruple)) that [[Kan extension]] produces an [[adjoint quadruple]] of functors between the [[category of presheaves]] $[\mathcal{C}^{op}, Set]$ and $[\ast, Set] \simeq Set$, as shown, where 

1. $\Gamma$ is the operation of pre-composition with the terminal object inclusion $\ast \hookrightarrow \mathcal{C}$

1. $Disc$ is the [[left Kan extension]] along the inclusion $\ast \hookrightarrow \mathcal{C}$ of the terminal object. 

The former is manifestly the operation of evaluating on the terminal object.
Moreover, since the terminal object inclusion is manifestly a [[fully faithful functor]] ([this def.](geometry+of+physics+--+Categories+and+Toposes#FullyFaithfulFunctor)), it follows that also its [[left Kan extension]] $Disc$ is fully faithful  ([this prop.](geometry+of+physics+--+Categories+and+Toposes#LeftKanExtensionAlongFullyFaithfulFunctor)). This implies that also $coDisc$ is fully faithful, by [this prop.](geometry+of+physics+--+Categories+and+Toposes#FullyFaithfulAdjointTriple).

Equivalently, $Disc \simeq p^\ast$ is the [[constant functor|constant]] [[diagram]]-assigning functor. By uniqueness of adjoints ([this prop.](geometry+of+physics+--+categories+and+toposes#UniquenessOfAdjoints)) implies that $\Pi_0$ is the functor that sends a presheaf, regarded as a [[functor]] $\mathbf{Y} \;\colon\; \mathcal{C}^{op} \to Set$, to its [[colimit]] 

\[
  \label{Pi0IsColimit}
  \Pi_0(\mathbf{Y})
  \;=\;
  \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim} \mathbf{Y}
  \,.
\]

The fact that this indeed preserves products follows from the assumption that $\mathcal{C}$ has [[finite products]], since [[categories with finite products are cosifted]] ([this prop.](geometry+of+physics+--+categories+and+toposes#CategoriesWithFiniteProductsAreCosifted))

=--


Example \ref{PresheavesAdjointQuadrupleOnSiteWithTerminalObject} suggests to  ask for [[coverages]] on categories with [[finite products]] which are such that the [[adjoint quadruple]]  (eq:PreaheafAdjointQuadruple) on the  [[category of presheaves]] ([[corestriction|co-]])[[restriction|restricts]] to the corresponding [[category of sheaves]]. The following Definition \ref{OneCohesiveSite} states a sufficient condition for this to be the case:

+-- {: .num_defn #OneCohesiveSite}
###### Definition
**([[cohesive site]])**

We call a [[site]] $\mathcal{C}$ ([this def.](geometry+of+physics+--+categories+and+toposes#Coverage)) _[[cohesive site|cohesive]]_ if the following conditions are satisfied:

1. The [[category]] $\mathcal{C}$ has [[finite products]] (as in Example \ref{PresheavesAdjointQuadrupleOnSiteWithTerminalObject}).
 
1. For every [[covering]] family $\{U_i \to X\}_i$ in the given [[coverage]] on  $\mathcal{C}$ the induced [[Cech groupoid]] $C(\{U_i\}_i) \in [C^{op}, Grpd]$ ([this def.](geometry+of+physics+--+categories+and+toposes#CechGroupoid)) satisfies the following two conditions:

   1. the set of [[connected components]] of the [[groupoid]] obtained as the [[colimit]] over the [[Cech groupoid]] is the [[singleton]]: 
 
      $$
        \pi_0
        \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim} 
         C(\{U_i\}) 
         \;\simeq\;
         \ast
      $$

   1. the set of [[connected components]] of the [[groupoid]] obtained as the [[limit]] of the [[Cech groupoid]] is [[equivalence of categories|equivalent]] to the set of points of $X$, regarded as a groupoid:

      $$
        \pi_0
        \underset{\underset{\mathcal{C}^{op}}{\longleftarrow}}{\lim} C(\{U_i\})
          \simeq
        Hom_{\mathcal{C}}(\ast,X)
        \,.
      $$
 
=--

This definition is designed to make the following true:

+-- {: .num_prop #CategoriesOfSheavesOnCohesiveSiteIsCohesive}
###### Proposition
**([[category of sheaves]] on a [[cohesive site]] is a [[cohesive topos]])**

Let $\mathcal{C}$ be a [[cohesive site]] (Def. \ref{OneCohesiveSite}). Then the [[adjoint quadruple]] on the [[category of presheaves]] over $\mathcal{C}$, from Example \ref{PresheavesAdjointQuadrupleOnSiteWithTerminalObject} (given that a [[cohesive site]] by definition has [[finite products]]) ([[corestriction|co-]])[[restriction|restricts]] from the [[category of presheaves]] over $\mathcal{C}$, to the [[category of sheaves]] ([this def.](geometry+of+physics+--+categories+and+toposes#Sheaf)) and hence exhibits $Sh(\mathcal{C})$ as a [[cohesive topos]] (Def. \ref{CohesiveTopos}):

\[
  \label{SheafToposAdjointQuadruple}
  Sh(\mathcal{C})
    \array{
      \overset{\phantom{AAA} \Pi_0 \phantom{AAA}}{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookleftarrow}
    }
  Set
\]


=--

+-- {: .proof}
###### Proof

With Example \ref{SmoothFunctionOnSmoothSpace} it only remains to be shown that for each [[set]] $S$ the [[presheaves]] $Disc(S)$ and $coDisc(S)$ are indeed [[sheaves]].

By the formulaton of the [[sheaf|sheaf condition]] via the [[Cech groupoid]] ([this prop](geometry+of+physics+--+categories+and+toposes#CechGroupoidCoRepresents)), and using the [[adjunction]] hom-isomorphisms ([here](geometry+of+physics+--+categories+and+toposes#eq:HomIsomorphismForAdjointFunctors)) this is readily seen to be equivalent to the two further conditions on a cohesive site (Def. \ref{OneCohesiveSite}):

Let $\{U_i \to X\}$ be a [[covering]] family. 

The sheaf condition (in [this form](geometry+of+physics+--+categories+and+toposes#eq:SheafIsLocalObjectWithRespectToCechCovers)) for $Disc(S)$ says that 

$$
  \left[
    C(\{U_i\}) \overset{p_{\{U_i\}_i}}{\to} y(X)
    \,,\,
    Disc(S)
  \right]
$$

is an [[isomorphism]] of [[groupoids]], which by adjunction and using (eq:Pi0IsColimit) means equivalently that 

$$
  \left[
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \left( C(\{U_i\}) \right) \to 
    \ast
    \,,\,
    S
  \right]
$$

is an isomorphism of groupoids, where we used that colimits of representables are [[singletons]] ([this Lemma](geometry+of+physics+--+categories+and+toposes#ColimitOfRepresentableIsSingleton)) to replace $\underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim} y(X) \simeq \ast$.

But now in this [[internal hom]] of [[groupoids]], the set $S$ is really a groupoid in the image of the [[reflective subcategory|reflective embedding]] of sets into groupoids, whose [[left adjoint]] is the [[connected components]]-functor $\pi_0$ ([this example](geometry+of+physics+--+categories+and+toposes#ReflectiveSubcategoryInclusionOfSetsIntoGroupoids)). Hence  by another adjunction isomoprhism this is equivalent to 

$$
  \left[
    \pi_0
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \left( C(\{U_i\}) \right) \to 
    \ast
    \,,\,
    S
  \right]
$$

being an isomorphism (a [[bijection]] of [[sets]], now). This is true for all $S \in Set$ precisely if (by the [[Yoneda lemma]], if you wish) the morphism

$$
    \pi_0
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \left( C(\{U_i\}) \right) \to 
    \ast
$$

is already an isomorphism (here: [[bijection]]) itself.

Similarly,  the sheaf condition (in [this form](geometry+of+physics+--+categories+and+toposes#eq:SheafIsLocalObjectWithRespectToCechCovers)) for $coDisc(S)$ says that 

$$
  \left[
    C(\{U_i\}) \overset{p_{\{U_i\}_i}}{\to} y(X)
    \,,\,
    coDisc(S)
  \right]
$$

is an [[isomorphism]], and hence by [[adjunction]] and using (eq:CohesiveGlobalSectionsGivenByPointEvaluation), this is equivalent to

$$
  \left[
    \pi_0
    \underset{\underset{\mathcal{C}^{op}}{\longleftarrow}}{\lim}
    C(\{U_i\}) 
    \overset{p_{\{U_i\}_i}}{\to} 
    Hom_{\mathcal{C}}(\ast, X)
    \,,\,
    S
  \right]
$$

being an isomorphism. This holds for all $S \in Set$ if (by the [[Yoneda lemma]], if you wish)

$$
    \pi_0
    \underset{\underset{\mathcal{C}^{op}}{\longleftarrow}}{\lim}
    C(\{U_i\}) 
    \overset{p_{\{U_i\}_i}}{\to} 
    Hom_{\mathcal{C}}(\ast, X)
$$

is an isomorphism.

=--

#### Smooth sets
  {#ExampleSmoothSets}

+-- {: .num_example #SmoothSetsFormACohesiveTopos}
###### Example
**([[smooth sets]] form a [[cohesive topos]])**

The [[category]] $SmoothSet$ of [[smooth sets]] ([this Def.](geometry+of+physics+--+smooth+sets#CategoryOfSmoothSets)) is a [[cohesive topos]] (Def. \ref{CohesiveTopos})

\[
  \label{SheafToposAdjointQuadruple}
  SmoothSet
    \array{
      \overset{\phantom{AAA} \Pi_0 \phantom{AAA}}{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\longleftarrow}
    }
  Set
\]


=--

+-- {: .proof}
###### Proof

First of all (by [this Prop](geometry+of+physics+--+smooth+sets#CategoryOfSmoothSets)) smooth sets indeed form a [[sheaf topos]], over the [[site]] [[CartSp]] of [[Cartesian spaces]] $\mathbb{R}^n$ with [[smooth functions]] between them, and equipped with the [[coverage]] of differentiably-[[good open covers]] ([this def.](geometry+of+physics+--+smooth+sets#DifferentiallyGoodOpenCover))

$$
  SmoothSet \simeq Sh(CartSp)
  \,.
$$

Hence, by Prop. \ref{CategoriesOfSheavesOnCohesiveSiteIsCohesive}, it is now sufficient to see that [[CartSp]] is a [[cohesive site]] (Def. \ref{OneCohesiveSite}).

It clearly has [[finite products]]: The [[terminal object]] is the [[point]], given by the 0-[[dimension|dimensional]] [[Cartesian space]]

$$
  \ast = \mathbb{R}^0
$$

and the [[Cartesian product]] of two [[Cartesian spaces]] is the Cartesian space whose [[dimension]] is the [[sum]] of the two separate dimensions:

$$
  \mathbb{R}^{n_1} \times \mathbb{R}^{n_2}
  \;\simeq\;
  \mathbb{R}^{ n_1 + n_2 }
  \,.
$$

This establishes the first clause in Def. \ref{OneCohesiveSite}. 

For the second clause, consider a differentiably-[[good open cover]] $\{U_i \overset{}{\to} \mathbb{R}^n\}$ ([this def.](geometry+of+physics+--+smooth+sets#DifferentiallyGoodOpenCover)). This being a [[good cover]] implies that its [[Cech groupoid]] is, as an [[internal groupoid]] (via [this remark](geometry+of+physics+--+categories+and+toposes#PresheavesOfGroupoidsAsInternalGroupoidsInPresheaves)), of the form

\[
  \label{CechGroupoidForCartSp}
  C(\{U_i\}_i)
  \;\simeq\;
  \left( 
    \array{
       \underset{i,j}{\coprod} y(U_i \underset{\mathbb{R}^n}{\cap} U_j)
       \\
       \big\downarrow \big\uparrow \big\downarrow
       \\
       \underset{i}{\coprod} y(U_i)
    }
  \right)
  \,.
\]

where we used the defining property of [[good open covers]] to identify $y(U_i) \times_X y(U_j) \simeq y( U_i \cap_X U_j )$. 

The [[colimit]] of (eq:CechGroupoidForCartSp), regarded just as a [[presheaf]] of [[reflexive graph|reflexive]] [[directed graph|directed]] [[graphs]] (hence ignoring [[composition]] for the moment), is readily seen to be the [[graph]] of the [[colimit]] of the components (the [[universal property]] follows immediately from that of the component colimits):


\[
  \label{ColimitOfCechGroupoidOverCartSp}
  \begin{aligned}
    \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
    C(\{U_i\}_i)
    & \simeq
    \left( 
      \array{
        \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
         \underset{i,j}{\coprod} y(U_i \underset{\mathbb{R}^n}{\cap} U_j)
         \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
         \underset{i}{\coprod} y(U_i)
      }
    \right)
    \\
    & \simeq
    \left( 
      \array{
         \underset{i,j}{\coprod} 
         \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
         y(U_i \underset{\mathbb{R}^n}{\cap} U_j)
         \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{i}{\coprod} 
         \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
         y(U_i)
      }
    \right)
    \\
    & \simeq
    \left( 
      \array{
         \underset{i,j}{\coprod} \ast
          \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{i}{\coprod} \ast
      }
    \right)
  \end{aligned}
  \,.
\]

Here we first used that [[colimits commute with colimits]], hence in particular with [[coproducts]] ([this prop.](geometry+of+physics+--+categories+and+toposes#LimitsCommuteWithLimits)) and then that the colimit of a [[representable presheaf]] is [[generalized the|the]] [[singleton]] set ([this Lemma](geometry+of+physics+--+categories+and+toposes#ColimitOfRepresentableIsSingleton)).

This colimiting [[graph]] carries a unique [[composition]] structure making it a [[groupoid]], since there is at most one morphism between any two objects, and every object carries a morphism from itself to itself. This implies that this groupoid is actually the colimiting groupoid of the Cech groupoid: hence the groupoid obtained from replacing each representable summand in the Cech groupoid by a point.

Precisely this operation on [[Cech groupoids]] of [[good open covers]] of [[topological spaces]] is what _[[Borsuk's nerve theorem]]_ is about, a classical result in [[topology]]/[[homotopy theory]]. This theorem implies directly that the set of [[connected components]] of the groupoid (eq:ColimitOfCechGroupoidOverCartSp) is in [[bijection]] with the set of [[connected components]] of the [[Cartesian space]] $\mathbb{R}^n$, regarded as a [[topological space]]. But this is evidently a [[connected topological space]], which finally shows that, indeed

$$
  \pi_0
  \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
    C(\{U_i\}_i)
  \;\simeq\;
  \ast
  \,.
$$

The second item of the second clause in Def. \ref{OneCohesiveSite} follows similarly, but more easily: The [[limit]] of the [[Cech groupoid]] is readily seen to be, as before, the unique groupoid structure on the limiting underlying graph of presheaves. Since $CartSp$ has a [[terminal object]] $\ast = \mathbb{R}^0$, which is hence an [[initial object]] in the [[opposite category]] $CartSp^{op}$, limits over $CartSp^{op}$ yield simply the evaluation on that object:

\[
  \label{ColimitOfCechGroupoidOverCartSp}
  \begin{aligned}
    \underset{\underset{CartSp^{op}}{\longleftarrow}}{\lim}
    C(\{U_i\}_i)
    & \simeq
    \left( 
      \array{
        \underset{\underset{CartSp^{op}}{\longleftarrow}}{\lim}
         \underset{i,j}{\coprod} y(U_i \underset{\mathbb{R}^n}{\cap} U_j)
         \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{\underset{CartSp^{op}}{\longleftarrow}}{\lim}
         \underset{i}{\coprod} y(U_i)
      }
      \phantom{A}
    \right)
    \\
    & \simeq
    \left( 
      \array{
         \underset{i,j}{\coprod} 
         Hom_{CartSp}\left( \ast,  U_i \underset{\mathbb{R}^n}{\cap} U_j \right)
         \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{i}{\coprod} 
         Hom_{CartSp}( \ast, U_i )
      }
    \right)
  \end{aligned}
  \,.
\]

Here we used that [[colimits]] (here [[coproducts]]) of [[presheaves]] are computed objectwise, and then the definition of the [[Yoneda embedding]] $y$.

But the [[equivalence relation]] induced by this graph on its set of objects $\underset{i}{\coprod}  Hom_{CartSp}( \ast, U_i )$ precisely identifies pairs of points, one in $U_i$ the other in $U_j$, that are actually the same point of the $\mathbb{R}^n$ being covered. Hence the set of [[equivalence classes]] is the set of points of $\mathbb{R}^n$, which is just what remained to be shown:

$$
  \pi_0
  \underset{\underset{CartSp^{op}}{\longleftarrow}}{\lim}
    C(\{U_i\}_i)
  \;\simeq\;
  Hom_{CartSp}(\ast, \mathbb{R}^n)
  \,.
$$



=--



#### Diffeological spaces


+-- {: .num_prop}
###### Proposition

The [[quasitopos]]  of [concrete objects](#ConcreteObjects)
in the cohesive topos of [[smooth sets]] (Example \ref{SmoothSetsFormACohesiveTopos}) is the category of [[diffeological spaces]].

$$
  \array{
    Conc(Sh(CartSp))
    &\hookrightarrow&
    Sh(CartSp)
    \\
    = && =
    \\
    DiffeolSp &\hookrightarrow& SmoothSets
  }
$$ 


=--

+-- {: .proof}
###### Proof

A sheaf $X$ on $CartSp$ is a [[separated presheaf]] with respect to the further localization given by $CoDisc$ precisely if the canonical morphism (the [[unit of an adjunction|unit]] of $(\Gamma \dashv CoDisc)$)

$$
  X \to CoDisc \Gamma X
$$

is a [[monomorphism]]. Monomorphisms of sheaves are tested objectwise, so that this is equivalent to 

$$
  Hom(U,X) \simeq X(U) \to Hom(U,CoDisc \Gamma X)
$$

being a monomorphism for all $U \in C$ (where in the first step we used the [[Yoneda lemma]]). By the adjunction relation this is equivalently

$$
  X(U) \to Set(\Gamma(U), \Gamma(X))
  \,.
$$

This being a monomorphism is precisely the condition on $X$ being a [[concrete sheaf]] on $CartSp$ that singles out diffeological spaces among all sheaves on $CartSp$.

=--


#### Formally smooth sets

+-- {: .num_prop}
###### Proposition

The site [[ThCartSp]] with the standard [[open cover]] [[coverage]] is a [[cohesive site]] and even an [[(∞,1)-cohesive site]]. 

=--


The corresponding cohesive topos is the [[Cahiers topos]] $ \simeq Sh(ThCartSp)$. This is a [[smooth topos]] that models the axioms of 
[[synthetic differential geometry]].

(...)


### Cohesive over-toposes

+-- {: .num_prop}
###### Proposition

Let $\mathcal{E}$ be a cohesive topos and $X \in \mathcal{E}$ an object. 

A necessary conditions that the [[over topos]] $\mathcal{E}/X$ is a [[connected topos]] is that

1. $X$ is connected $\Pi_0(X) \simeq *$;

Sufficient condition for $\mathcal{E}/X$ to be a [[local topos]] is that

1. $X$ is a [[tiny object]].


=--



### Infinitesimal thickening and formal smoothness
 {#InfinitesimalThickening}

See at _[[differential cohesion]]_. Examples include the _[[Cahiers topos]]_

+-- {: .num_example }
###### Example

Consider a [[full subcategory]] inclusion

$$ 
  Disc^{\mathcal{P}} \;\colon\; \mathcal{S} \hookrightarrow \mathcal{P}
$$

which has a [[left adjoint]] $\Pi_0^{\mathcal{P}}$ and a [[right adjoint]] $\Gamma^{\mathcal{P}}$ that coincide with each other

$$
  \Pi_0^{\mathcal{P}} \simeq \Gamma^{\mathcal{P}}
  \,.
$$

In ([Lawvere 07, def. 1](#LawvereAxiomatic)) this situation is said to exhibit $\mathcal{E}$ as a _[[quality type]]_ over $\mathcal{S}$.

It follows that there is an infinite sequence of adjoints, in particular that there is $coDisc^{\mathcal{P}} \coloneqq Disc^{\mathcal{P}}$ [[right adjoint]] to $\Gamma^{\mathcal{P}}$, which by the discussion at [[adjoint triple]] is also a [[full and faithful functor]], and that $\Pi_0^{\mathcal{P}}$ preserves [[finite products]] (in fact all [[limits]]). 

So the above adjoints makes $\mathcal{P}$ be a cohesive topos over the [[base topos]] $\mathcal{S}$ with the special property that $\Pi_0^{\mathcal{P}} \simeq \Gamma^{\mathcal{P}}$. In words this says that in $\mathcal{P}$ every cohesive neighbourhood contains precisely one point. This is a characteristic of [[infinitesimally thickened points]].

See at _[[infinitesimal cohesion]]_ for more on this.

=--



### Counter-examples {#CounterExamples}

+-- {: .num_example}
###### Counter-Example

Let $G$ be a non-trivial [[finite group]] of [[cardinality]] $n$. Write $\mathbf{B}G = \{\bullet \stackrel{g}{\to} \bullet | g \in G\}$ for its [[delooping]] [[groupoid]]. The [[presheaf topos]]

$$
  PSh(\mathbf{B}G) \simeq G Set
$$

is the category of [[permutation representation]]s of $G$. It comes with a triple of adjoint functors

$$
  (\Pi_0 \dashv Const \dashv \lim_\leftarrow) : G Set 
    \stackrel{\overset{\lim_\to}{\to}}{\stackrel{\overset{Const}{\leftarrow}}{\underset{\lim_\leftarrow}{\to}}}
   Set
  \,.
$$


The colimit over a representation $(V, \rho) : \mathbf{B}G \to Set$ is [[quotient]] set $V/\rho(G)$. So we have

$$
  \Pi_0(G) \simeq *
$$

but

$$
  \Pi_0(G \times G) \simeq \bar n
  \,,
$$

where $G$ denotes the fundamental representation of $G$ on itself. Therefore $\Pi_0$ does not preserve products in this case.

=--



## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]]

  * [[Pi modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]]

* **cohesive topos** / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]], [[locally ∞-connected site]]

* [[connected site]]

* [[local site]]

* [[cohesive site]]



## References
 {#References}

The axioms for a cohesive topos originate around

* {#LawvereCatsOfSpaces} [[William Lawvere]], _Categories of spaces may not be generalized spaces, as exemplified by directed graphs_ , preprint, State University of New York at Buffalo, (1986) Reprints in Theory and Applications of Categories, No. 9, 2005, pp. 1&#8211;7 ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.144.6357&rep=rep1&type=pdf))


where however the term "cohesive topos" was not yet used. 

This appears maybe first in

* [[William Lawvere]], _[[Cohesive Toposes and Cantor's "lauter Einsen"]]_ Philosophia Mathematica (3) Vol. 2 (1994), pp. 5-15. ([doi:10.1093/philmat/2.1.5](https://doi.org/10.1093/philmat/2.1.5), [[LawvereCohesiveToposes.pdf:file]])

The term "cohesion" and parts of its later axiomatization (p. 245) appears thoughout section C.1 of

* {#LawvereRosebrugh03} [[William Lawvere]], [[Robert Rosebrugh]], _[[Sets for Mathematics]]_, Cambridge University Press  2003 ([doi:10.1017/CBO9780511755460](https://doi.org/10.1017/CBO9780511755460), [book homepage](http://www.mta.ca/~rrosebru/setsformath/), [pdf](http://patryshev.com/books/Sets%20for%20Mathematics.pdf))

Under the name _categories of cohesion_ a formal axiomatization is given in

* {#LawvereAxiomatic} [[William Lawvere]], _Axiomatic cohesion_, Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([tac:19-03](http://www.tac.mta.ca/tac/volumes/19/3/19-03abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))
 

(This does demand the conditions that "cohesive piece have points" and "pieces of powers are powers of pieces" as part of the definition of "category of cohesion".)

This builds on a series of precursors of attempts to identify axiomatics for [[gros topos]]es.

In

* {#Lawvere91} [[William Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_, [[Como]] 1991

the term _category of Being_ is used for a notion resembling that of a cohesive topos (with an [[adjoint quadruple]] but not considering _pieces have points_ or _discrete objects are concrete_). Behaviour of objects with respect to the extra left adjoined is interpreted in terms of properties of _Becoming_. The terminology here is probably inspired from

* [[Georg Hegel]], _[[Science of Logic]]_ (see  _[On being and becoming](#http://ncatlab.org/nlab/show/Science+of+Logic#OnBeingAndBecoming)_ ).

and specifically the term "cohesion" probably from

* [[Georg Hegel]], part II "Philosophy of Nature", second section "Physics", B c) "cohesion", in _[[Encyclopedia of the Philosophical Sciences]]_


In 

* [[William Lawvere]], _Categories of space and quantity_ in: J. Echeverria et al (eds.), _The Space of mathematics_ , de Gruyter, Berlin, New York (1992)

a proposal for a general axiomatization of [[homotopy]]/[[homology]]-like "extensive quantities" and [[cohomology]]-like "intensive quantities") as covariant and contravariant functors out of a distributive category are considered.

The left and right adjoint to the global section functor as a means to identify discrete spaces and codiscrete space is mentioned

* [[William Lawvere]], _Taking categories seriously_, Reprints in Theory and Applications of Categories, No. 8, 2005, pp. 1&#8211;24. ([pdf](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf))

on [page 14](http://www.tac.mta.ca/tac/reprints/articles/8/tr8.pdf#page=14).

The precise term _cohesive topos_ apparently first appeared publically in the lecture 


* [[William Lawvere]], _[[Cohesive Toposes -- Combinatorial and Infinitesimal Cases]]_ Como (2008)

Notes for these lectures are in [this pdf](http://comocategoryarchive.com/People/Lawvere/FWLawvere-Cohesive-Toposes-Como-January-2008.pdf), made available on [[Bob Walters]]'s _[Como Category Theory Archive](http://comocategoryarchive.com/)_.

The notion of "cohesion" was explored earlier in

* [[William Lawvere]], _Volterra's functionals and covariant cohesion of space_ Perugia Studies in Mathematics (Proceedings of the May 1997 Meeting in Perugia) ([pdf](http://www.acsu.buffalo.edu/~wlawvere/Volterra.pdf))

where (on p. 9) it is suggested that "almost any" [[extensive category]]  may be called a "species of cohesion".

An analysis of the interdependency of the axioms on a cohesive topos is in

* {#Johnstone11} [[Peter Johnstone]], _Remarks on punctual local connectedness_, Theory and Applications of Categories, Vol. 25, 2011, No. 3, pp 51-63.  ([tac](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html))

Discussion of "sufficient cohesion" is in 

* {#Menni14} [[Matías Menni]], _Continuous Cohesion over sets_, Theory and Applications of Categories, Vol. 29, 2014, No. 20, pp 542-568.  ([TAC](http://www.tac.mta.ca/tac/volumes/29/20/29-20abs.html), [pdf](https://sites.google.com/site/matiasmenni/continuityOverSets12.pdf?attredirects=0))

* [[Matías Menni]], _Sufficient Cohesion over Atomic Toposes_ , Cah. Top.G&#233;om. Diff. Cat. **LV** (2014) ([preprint](https://sites.google.com/site/matiasmenni/SufCohesion12.pdf?attredirects=0))

Discussion of relation to [[double negation topology]] is in

* {#LawvereMenni15} [[William Lawvere]], [[Matías Menni]], _Internal choice holds in the discrete part of any cohesive topos satisfying stable connected codiscreteness_, Theory and Applications of Categories, Vol. 30, 2015, No. 26, pp 909-932. ([TAC](http://www.tac.mta.ca/tac/volumes/30/26/30-26abs.html))

And further relations of cohesion to [[Birkhoff's theorem]] in [[universal algebra]] is given in

* {#Lawvere16} [[William Lawvere]], _Birkhoff's Theorem from a geometric perspective: A simple example_, to appear in Categories and General Algebraic Structures with Applications (2016), [journal page](http://www.cgasa.ir/article_12425_0.html).

A good deal of the structure of cohesive toposes is also considered in 

* {#KontsevichRosenbergSpaces} [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative spaces_, preprint MPI-2004-35 ([ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2331), [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2303))
 

under the name _[[Q-categories]]_.

The [[internal logic]] of [[local toposes]] is discussed in 

* {#AwodeyBirkedal} [[Steve Awodey]], [[Lars Birkedal]], _Elementary axioms for local maps of toposes_, Journal of Pure and Applied Algebra, 177(3):215-230, (2003) ([ps](http://www.itu.dk/people/birkedal/papers/elealm.ps.gz))
  
Notation and terminology above, and generalization to [[differential cohesion]] etc., follows:

* [[Urs Schreiber]], *[[schreiber:differential cohomology in a cohesive topos]]* ([arXiv:1310.7930](https://arxiv.org/abs/1310.7930))

Exposition:

* {#Loregian19} [[Fosco Loregian]], *Cohesion in Rome*, talk notes, Dec. 2019  ([pdf](https://tetrapharmakon.github.io/stuff/cohesive_rome.pdf), [[LoregianCohesion.pdf:file]])



[[!redirects cohesive topos]]
[[!redirects cohesive toposes]]
[[!redirects cohesive topoi]]

[[!redirects category of cohesion]]
[[!redirects categories of cohesion]]