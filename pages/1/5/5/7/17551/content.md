
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In the context of [[equivariant stable homotopy theory]] and $G$ one distinguishes, for a [[G-spectrum]] $E$, between the plain  _[[fixed point spectrum]]_ $F^G(E)$ and its _geometric fixed point spectrum_ $\Phi^G(E)$. 

Here the terminology "geometric" is in the sense of _[[point-set topology]]_, as opposed to [[homotopy theory]]: If $X$ is a ([[pointed topological space|pointed]]) [[topological space]] equipped with a [[continuous function]] $G$-[[action]] (a [[topological G-space]]), so that one may consider its $G$-[[equivariant suspension spectrum]] $\Sigma^\infty_G X \in G Spectra$, then the _geometric fixed point spectrum_ $\Phi^G(\Sigma^\infty_G X)$ of the latter is equivalent to the plain [[suspension spectrum]] of the plain [[fixed point]]-space $X^G$:

$$
  \Phi^G\big(  \Sigma^\infty_G X \big) 
     \;\simeq\;   
  \Sigma^\infty\big( X^G \big)
  \,,
$$

see the characterization in Prop. \ref{AbstractCharacterizationOfGeometricFixedPointSpectra}, below.

In general this is different from (not [[equivalence in an (infinity,1)-category|equivalent]] to) both of the following other notions of fixed point spectra:

1. the plain (really: [[homotopy theory|homotopy theoretic]]) [[fixed point spectrum]] $F^G(\Sigma^\infty_G X)$, which is instead the [[derived functor]] of forming topological fixed points $X \mapsto X^G$, hence which applies this construction only after [[fibrant resolution]]; the difference between the two is described by the _[[tom Dieck splitting theorem]]_, see Prop. \ref{AsWedgeSummandInTomDieckSplitting} below.

1. the [[categorical fixed point spectrum]]...


## Definition

A concrete definition of geometric fixed points of an equivariant spectrum is in ([Schwede 15, 7.3](#Schwede15)). A conceptual characterization in terms of [[localization of spectra]] is in ([Mathew-Naumann-Noel 15, def. 6.12](#MathewNaumannNoel15)).

## Properties

### For equivariant suspension spectra
 {#ForEquivariantSuspensionSpectra}


+-- {: .num_prop #AsWedgeSummandInTomDieckSplitting}
###### Proposition
**(as a [[wedge sum|wedge summand]] in the [[tom Dieck splitting]])** 

For $X$ a [[topological G-space]] and $\Sigma^\infty_G X$ its [[equivariant suspension spectrum]], there is a canonical comparison morphism (...) 

$$
  \Phi^G(\Sigma^\infty_G X) 
  \;\simeq\; 
  \Sigma^\infty( X^G )
  \hookrightarrow
  F^G(\Sigma^\infty_G X)
$$

which exhibits its geometric fixed point spectrum as precisely the first summand in the [[tom Dieck splitting]] of the plain [[fixed point spectrum]]

$$
  F^G(\Sigma^\infty_G X)
  \simeq
  \Sigma^\infty( X^G )
    \vee
  \left(
    \underset{{[H\subset G]} \atop {1 \neq H \neq G}}{\vee}
    \Sigma^\infty( E (W_G H)_+ \wedge_{W_G H} X^H )
  \right)
    \vee
  \Sigma^\infty( E G_+ \wedge_{G} X )
  \,.
$$

=--

([Schwede 15, Example 7.7](#Schwede15))

In fact:

+-- {: .num_prop #AbstractCharacterizationOfGeometricFixedPointSpectra}
###### Proposition

The construction of geometric fixed point spectra is essentially uniquely characterized by the  property 

$$
  \Phi^G\big(  \Sigma^\infty_G X \big) 
     \;\simeq\;   
  \Sigma^\infty\big( X^G \big)
$$

and the property of being [[left derived functor|left derived]] [[strong monoidal functor|strong monoidal]] and preserving [[homotopy colimits]].

=--

([Schwede 15, remark 7.15](#Schwede15), [Blumberg 17, around Def. 2.5.16](#Blumberg17))

More generally:

+-- {: .num_prop #PartialGeometricFixedPoint}
###### Proposition/Remark
**(partial geometric fixed point spectra)**

There is a "partial" geometric fixed point functor, which for a given [[subgroup]] $H \subset G$ sends 

$$
  \Phi^H \;\colon\; G Spectra \longrightarrow W_G H Spectra
$$

(for $W_G/H$ the [[Weyl group]], which is the [[quotient group]] $G/H$ in the case that $H$ is a [[normal subgroup]]) and satisfies for a $G$-[[equivariant suspension spectrum]] $\Sigma^\infty_G X$ the relation

\[
  \label{PartialGeometricFixedPointsOfEqui}
  \Phi^H \big(  \Sigma^\infty_G X \big) 
  \;\simeq\;
  \Sigma^\infty_{W_G H} X^H
  \,,
\]

hence, if $H = N \subset G$ already happens to be a [[normal subgroup]]:

\[
  \Phi^N \big(  \Sigma^\infty_G X \big) 
  \;\simeq\;
  \Sigma^\infty_{G/N} X^H
  \,.
\]

=--

([Lewis-May-Steinberger 86, II.9, Def. 9.7, Cor. 9.9](#LewisMaySteinberger86), [Lewis 00, Scholium 10.2](#Lewis00))

$\,$


### In terms of smashing localization
 {#InTermsOfSmashingLocalization}

We collect some facts from [Lewis-May-Steinberger 86, section II.9](#LewisMaySteinberger86).

Throughout, consider a [[finite group]] $G$ and a [[normal subgroup]] $N \subset G$. 

+-- {: .num_defn}
###### Definition

We write

$$
  \mathcal{F}[N]
  \;\coloneqq\;
  \big\{
    N &#8836; H\; \subset G 
  \big\}
$$ 

for the set of [[subgroups]] of $G$ that do not contain $N$, and

$$
  \mathcal{F}[N]^'
  \;\coloneqq\;
  \big\{
    N \subset H \subset G 
  \big\}
$$ 

for the subset of [[subgroups]] of $G$ that do contain $N$.

=--

([LMS86, p. 107 & bottom of p. 109](#LewisMaySteinberger86))


+-- {: .num_defn #tildeE}
###### Definition

There is a [[pointed topological space|pointed]] [[G-space]] 

$$
  \widetilde E \mathcal{F}[N]
  \;\in\;
  G Spaces
$$

whose [[fixed point spaces]] for [[subgroups]] $H \subset G$ are

$$
  \big(
    \widetilde E \mathcal{F}[N]
  \big)^H
  \;\simeq\;
  \left\{
    \array{
      \ast 
        &\vert& 
      H \in \mathcal{F}[N] 
        \;\Leftrightarrow\; 
      N &#8836; H 
      \\
      S^0 
        &\vert&
      H \in \mathcal{F}[N]^' 
        \;\Leftrightarrow\; 
      N \subset H 
    }
  \right.
$$

=--

([LMS86, beginning of II.9](#LewisMaySteinberger86))

+-- {: .num_defn #FPrimeEquivalences}
###### Definition

We say that a morphism $f \colon X \to Y$ of [[G-spectra]] is an _$\mathcal{F}[N]^'$-equivalence_ if its [[smash product]] with $\tilde E \mathcal{F}[N]$ (Def. \ref{tildeE})

$$
  f \wedge id_{\tilde E \mathcal{F}[N]}
  \;\colon\;
  X \wedge \tilde E \mathcal{F}[N]
   \longrightarrow
  Y \wedge \tilde E \mathcal{F}[N]
$$

is an equivalence of [[G-spectra]].

=--

[LMS 86, bottom of p. 107](#LewisMaySteinberger86)

+-- {: .num_prop #FPrimeLocalizationIsSmashingLocalization}
###### Proposition

The [[localization]] of $G Spectra$ at the $\mathcal{F}[N]'$-equivalences (Def. \ref{FPrimeEquivalences}) is a [[smashing localization]], given by smashing with the [[equivariant suspension spectrum]] of $\tilde E \mathcal{F}[N]$ (Def. \ref{tildeE})
 
$$
  \Sigma^\infty_G \tilde E \mathcal{F}[N]
  \;\in\;
  G Spectra
$$

In particular, we have

$$
  Ho_{G Spectra}\left( 
    \tilde E \mathcal{F}[N] \wedge X, 
    \tilde E \mathcal{F}[N] \wedge Y
  \right)
  \;\simeq\;
  Ho_{G Spectra}\left( 
    X, 
    \tilde E \mathcal{F}[N] \wedge Y
  \right)
$$


=--

([Lewis-May-Steinberger 86, Prop. II 9.1, 9.2 & top of p. 109](#LewisMaySteinberger86))

+-- {: .num_remark #LocalizationBySmashingWithtildeEF}
###### Remark

Hence

$$
  (L_{\mathcal{F}[N]'})_{X,Y}
  \coloneqq
  Ho_{G Spectra}(X, (S^0 \to \tilde E \mathcal{F}) \wedge Y)
  \;\colon\;
  Ho_{G Spectra}(X,Y)
    \longrightarrow
  Ho_{L_{\mathcal{F}[N]'} G Spectra}(X,Y)
$$

is $\mathcal{F}'[N]$-localization on [[hom-objects]].

=--

+-- {: .num_lemma #SmashingWithTildeOnSpaces}
###### Lemma

For $X$ and $Y$ [[G-CW-complexes]], the following are [[bijections]] of [[hom-sets]]:

$$
  \array{
  Ho_{G Spaces)}
  \big(
    X, \widetilde E \mathcal{F}[N] \wedge Y
  \big)
  &
  \underoverset{\simeq}{
    Ho_{G Spaces}
    \big(
      X^N \hookrightarrow X, \widetilde E \mathcal{F}[N]
    \big)
  }{\longrightarrow}
   &
  \mathrm{Hom}_{Ho(G Spaces)}
  \big(
    X^N, \widetilde E \mathcal{F}[N] \wedge Y
  \big)  
  \\
  && =
  \\
  Ho_{G Spaces}
  \big( 
    X^N, Y
  \big)
  &
  \underoverset{\simeq}{
    Ho_{G Spaces}
    \big(
      X^N, (S^0 \to \tilde E \mathcal{F}[N]) \wedge Y 
    \big)
    }{\longrightarrow}
  &
  Ho_{G Spaces}
  \big(
    X^N, \widetilde E \mathcal{F}[N] \wedge Y
  \big)  
  \\
  =
  \\
  Ho_{G Spaces}
  \big( 
    X^N, Y^N
  \big)
  }
$$

=--

([LMS 86, prop. II 9.3 with remark below the proof](#LewisMaySteinberger86))


+-- {: .num_cor #SmashingWithTildeEOnspacesEquivalentToRestriction}
###### Corollary

On [[hom-sets]] of [[G-spaces]] $Ho_{G Spaces}(X,Y)$, [[postcomposition|postcomposing]] with the [[smash product|smashing]] $(S^0 \to \tilde E \mathcal{F}[N]) \wedge Y$ is isomorphic to restricting along $X^N \hookrightarrow X$: The following is a [[commuting square]] (by nature of the [[hom-functor]]) and the right and bottom morphisms are bijections by Lemma \ref{SmashingWithTildeOnSpaces}:

$$
  \array{
    Ho_{G Spaces}
    \big( 
      X, Y
    \big)
    &
    \overset{ 
      Ho_{G Spaces}
      \big( 
        X^N \hookrightarrow N, Y 
      \big)  
    }{ \longrightarrow }
    &
    Ho_{G Spaces}\big( X^N, Y \big)
    &\simeq&
    Ho_{G Spaces}\big( X^N, Y^N \big)
    \\
    {}^{
      \mathllap{
        Ho_{G Spaces}( X, (S^0 \to \tilde E \mathcal{F}[N]) \wedge Y )         
      }
    }
    \big\downarrow 
    &&
    {}^{\mathllap{\simeq}}\big\downarrow
    {}^{
      \mathrlap{
        Ho_{G Spaces}( X^N, (S^0 \to \tilde E \mathcal{F}[N]) \wedge Y )
      }
    }
    \\
    Ho_{G Spaces}\big( X, \tilde E \mathcal{F}[N] \wedge Y  \big)
    &
      \underoverset
        {\simeq}
        {
          Ho_{G Spaces}
          \big( 
            X^N \hookrightarrow X, \tilde E \mathcal{F}[N] \wedge Y 
          \big)
        }
        {\longrightarrow}
    &
    Ho_{G Spaces}\big( X^N, \tilde E \mathcal{F}[N] \wedge Y  \big)
  }
$$

=--



+-- {: .num_lemma #GeometricFixedPointsInTermsOfPlainFixedPoints}
###### Lemma
**(geometric fixed point spectra in terms of homotopy fix point spectra)**

The partial geometric fixed point functor (Prop. \ref{PartialGeometricFixedPoint})

$$
  \Phi^N 
  \;\colon\;
  G Spectra 
    \longrightarrow
  G/N Spectra
$$

is given on [[equivariant suspension spectra]] $\Sigma^\infty_G X$ equivalently by first smashing with $\tilde E \mathcal{F}[N]$ (Def. \ref{tildeE}) followed by forming the partial plain [[fixed point spectrum]]:

$$
  \Phi^N \Sigma^\infty_G X \;\simeq\;
  \big(
    \tilde E \mathcal{F}[N]
    \;\wedge\;
    \Sigma^\infty_G X
  \big)^N
  \,.
$$

=--

([Lewis-May-Steinberger 86, Cor. 9.9](#LewisMaySteinberger86))


We will also need this here:

+-- {: .num_lemma #FixedPointSpectrumOfSmashProduct}
###### Lemma

For $X$ a [[G-CW-complex]] $E$ a [[G-spectrum|G-]] [[CW-spectrum]] and $N \subset G$ a [[normal subgroup]], the partial $N$-[[fixed point spectrum]] functor on spectra and the plain fixed point functor on spaces are compatible with smash product:

$$
  \left(
     \tilde E \mathcal{F}[N]
     \wedge E 
     \wedge X
  \right)^N
  \;\simeq\;
  \left(
     \tilde E \mathcal{F}[N]
     \wedge E 
  \right)
     \wedge X^N
$$

=--

([Lewis-May-Steinberger 86, prop. II 9.12](#LewisMaySteinberger86))








### Via inversion of Euler classes
 {#AsInversionOfEulerClasses}

We discuss an explicit formula (Prop. \ref{GeometricFixedPointCohomologtIsColimitOverSmashWithEulerClasses} below, due to [Lewis-May-Steinberger 86](#LewisMaySteinberger86)) that expresses [[equivariant cohomology|equivariant]] [[cohomology groups]] with [[coefficients]] in partial geometric fixed point spectra (Prop. \ref{PartialGeometricFixedPoint}) as the [[equivariant cohomology|equivariant]] [[cohomology groups]] with [[coefficients]] in the original spectrum, but with certain "[[Euler classes]] [[localization|inverted]]".

As an application, we show (Example \ref{EquivariantStableCohomotopyOfPointsInNontrivalROGDegree} below) that the [[equivariant stable cohomotopy]] of the point in certain non-trivial [[RO(G)-degrees]] $V$ surjects onto the corresponding partially equivariant stable cohomotopy in degree 0 (the latter being well-understood: given by the [[Burnside ring]], by [[Burnside ring is equivariant stable cohomotopy of the point|this Prop]]).

$\,$

A key role in this discussion is played by those [[RO(G)-degrees]] which trivialize when passing to partial fixed points:

+-- {: .num_defn #ROGDegreeWithoutNonTrivialHFixedPoints}
###### Definition
**([[RO(G)-degrees]] without non-trivial $H$-fixed points)**

For $H \subset G$ a [[subgroup]], say that a $G$-[[representation]] $V$ has _no non-trivial $H$-fixed points_ if the [[fixed point space]] of $V$ with respect to the $H$-[[action]] is the origin (which is necessarily fixed), hence is the [[zero object|zero]]-[[representation]]:

$$
  V^H \;=\; 0
$$


=--

We also use the following notation, following [Lewis-May-Steinberger 86](#LewisMaySteinberger86):

+-- {: .num_defn}
###### Definition
**([[base change]] along [[normal subgroup]]-inclusions of [[equivariant homotopy theory|equivariance]]-groups)**


Given a [[normal subgroup]]-inclusion

$$
  N \overset{\phantom{AA}}{\hookrightarrow} G 
  \overset{ \phantom{A} \epsilon \phantom{A} }{\longrightarrow}
  G/N
$$ 

with induced [[projection]] $\epsilon$ to the [[quotient group]] $G/N$
this induces various [[base change]] [[adjunctions]] (on [[homotopy categories]], say), such as on [[topological G-spaces]], to be denoted

\[
  \label{PullbackGSpace}
  G/N Spaces 
  \overset{ \epsilon^\sharp }{\longrightarrow}
  G Spaces
\]

and on $G$-[[representations]], to be denoted

\[
  \label{PullbackRepresentation}
  G/N Rep 
      { \overset{ \epsilon^\ast }{\longrightarrow} }
  G Rep
\]

and on [[G-spectra]], to be denoted


\[
  \label{PullbackSpectrum}
  G/N Spectra
    \underoverset
      { \underset{(-)^N}{\longleftarrow} }
      { \overset{ \epsilon^\sharp }{\longrightarrow} }
      {\phantom{AA}\bot\phantom{AA}}
  G Spectra
\]


where the [[right adjoint]] $(-)^N$ is the partial [[fixed point spectrum]]-functor (in contrast to the _geometric_ fixed point functor).

=--

(e.g. [Lewis-May-Steinberger 86, above theorem 9.5](#LewisMaySteinberger86))


+-- {: .num_prop #GeometricFixedPointCohomologtIsColimitOverSmashWithEulerClasses}
###### Proposition
**(partial geometric fixed point cohomology via inversion of Euler classes)**

Let $E \;\in\; G Spectra$ be a [[G-spectrum]] with partial geometric fixed point spectrum $\Phi^N E \;\in\; G/N Spectra$ (Prop. \ref{PartialGeometricFixedPoint})
and let
$
  X
  \;\in\;
  G/N Spectra^{fin}
  \overset{\epsilon^\sharp}{\longrightarrow}
  G Spectra
$
be [[finite spectrum|finite]] $G$-[[CW-spectrum]].


Then the $G/N$-[[equivariant cohomology|equivariant]] [[cohomology groups]] in [[RO(G)-degree|RO(G/N)-degree]] $\alpha$ of $X$ with [[coefficients]] in the partial geometric fixed point spectrum $\Phi^N E$ are equivalently the [[colimit]] over the $G$-[[equivariant cohomology|equivariant]] [[cohomology groups]] of $\epsilon^\sharp X$ (eq:PullbackGSpace) with [[coefficients]] in $E$, but in [[RO(G)-degree]] $\epsilon^\ast \alpha$ (eq:PullbackRepresentation) plus a shift by all those [[representations]] $V$ that have no nontrivial $N$-fixed points (Def. \ref{ROGDegreeWithoutNonTrivialHFixedPoints}):

\[
\label{ColimitConstructionForCohomologyWithCoeffsInPartialGeometricFixedPointSpectra}
  (\Phi^N E)^\bullet_{G/N}(X)
  \;\simeq\;
  \underset{\underset{\{V \vert V^N = 0\}}{\longrightarrow}}{\lim}
  E_G^{\epsilon^\ast \bullet + V}(\epsilon^\sharp X)  
  \,,
\]

where the [[colimit]] is over the [[diagram]] that has precisely one morphism for every inclusion  $V_1 \subset V_2$ of $G$-representations without non-trivial $N$-fixed points (Def. \ref{ROGDegreeWithoutNonTrivialHFixedPoints})

$$
  E_G^{\epsilon^\ast \bullet + V_1}(\epsilon^\sharp X)   
  \overset{ (-) \wedge \chi_{V_2 - V_1} }{\longrightarrow}
  E_G^{\epsilon^\ast \bullet + V_2}(\epsilon^\sharp X)   
$$

given by [[smash product]] with the [[Euler class]] 

$$
  \chi_{V}
  \;\coloneqq\;
  1 
  \in
  E_G^V(S^V)
  \overset{ (S^0 \to S^V)^\ast }{\longrightarrow}
  E_G^V(S^0)
$$

of $V \coloneqq V_2 - V_1$.

=--

([Lewis-May-Steinberger 86, chapter II, prop. 9.13](#LewisMaySteinberger86))


+-- {: .num_prop #CanonicalComparisonMap}
###### Proposition
**(comparison map to partial geometric fixed point cohomology)**

Prop. \ref{GeometricFixedPointCohomologtIsColimitOverSmashWithEulerClasses} provides a canonical comparison morphism, to be denoted

\[
  \label{ComparisonMap}
  E_G^{\epsilon^\ast \bullet}(\epsilon^\sharp X)
  \overset{
    \phantom{AA}
      p_E^N(X)
    \phantom{AA}
  }{\longrightarrow}
  (\Phi^N E)^\bullet_{G/N}(X)
\]

from the $G$-[[equivariant cohomology|equivariant]] [[cohomology groups]] with [[coefficients]] in $E$ to those with [[coefficients]] in the partial geometric fixed point spectrum: Namely the component of the [[colimit|colimiting]] [[cocone]](eq:ColimitConstructionForCohomologyWithCoeffsInPartialGeometricFixedPointSpectra) at stage $V = 0$:

$$
  \array{
    E^{\epsilon^\ast \bullet }(\epsilon^\sharp X)   
    && \overset{ (-) \wedge \chi_{V} }{\longrightarrow} &&
    E^{\epsilon^\ast \bullet + V}(\epsilon^\sharp X)  
    &\to&
    \cdots 
    \\
    & {}_{ \mathllap{ p_E^N(X) } }\searrow && \swarrow & \cdots
    \\
    && 
    (\Phi^N E)^\bullet_{G/N}(X)
  }
$$

This component is equal to the following composite of isomorphisms with $\mathcal{F}[N]'$-localization $L_{\mathcal{F}[N]'}$ (Def. \ref{FPrimeEquivalences}):

\[
  \label{LocalizationIsComparisonMorphism}
  \begin{aligned}
  p_E^N(X)
  \;\colon\;
  E^{\epsilon^\ast \alpha}(\epsilon^\sharp X)
  & =
  Ho_{G Spectra}\left( 
    \epsilon^\sharp \Sigma^\infty_{G/N} X  
    \;,\;  
    \Sigma^\infty_G S^{\epsilon \alpha} \wedge E
  \right)
  \\
  & \simeq
  Ho_{G Spectra}\left( 
    \epsilon^\sharp \Sigma^\infty_{G/N} X  
    \;,\;  
    \Sigma^\infty_G S^{\epsilon \alpha} \wedge S^0 \wedge E
  \right)
  \\
  & 
  \overset{ L_{\mathcal{F}[N]'} }{\longrightarrow}
  Ho_{G Spectra}\left( 
    \epsilon^\sharp \Sigma^\infty_{G/N} X  
    \;,\;  
    \Sigma^\infty_G S^{\epsilon \alpha} \wedge \tilde E \mathcal{F}[N]\wedge E
  \right)
  \\
  & \simeq
  Ho_{G/N Spectra}\left( 
     \Sigma^\infty_{G/N} X
    \;,\; 
    \left(    
       \Sigma^\infty_G S^{\epsilon^\ast \alpha} 
         \wedge 
       \tilde E \mathcal{F}[N] \wedge E
    \right)^N
  \right)
  \\
  & \simeq
  Ho_{G/N Spectra}\left( 
     \Sigma^\infty_{G/N} X
    \;,\; 
    \left(    
      S^{\epsilon^\ast \alpha} 
    \right)^N
         \wedge 
    \left(
       \tilde E \mathcal{F}[N] \wedge E
    \right)^N
  \right)
  \\  
  & \simeq
  Ho_{G/N Spectra}\left( 
     \Sigma^\infty_{G/N} X
    \;,\; 
    S^{\alpha}
    \wedge 
    \Phi^N E
  \right)  
  \\
  & =
  (\Phi^N E)^{\alpha}(X)
  \end{aligned}
\]


=--



+-- {: .proof}
###### Proof

This follows from the proof of ([Lewis-May-Steinberger 86, chapter II, prop. 9.13](#LewisMaySteinberger86)). We make this explicit: The proof there says that the comparison map is given by the [[smashing localization|smashing]] with $S^0 \to \tilde E \mathcal{F}$, up to re-identifications:

1. The first equality in (eq:LocalizationIsComparisonMorphism) is the definition of cohomology classes;

1. the second step  is the [[unitor]] isomorphism for the [[tensor unit]] being the [[sphere spectrum]];

1. the third step is smashing with $S^0 \to \tilde E \mathcal{F}[N]$, which is $\mathcal{F}'$-localization by Prop. \ref{FPrimeLocalizationIsSmashingLocalization};

1. the fourth step is the hom-isomorphism for the [[adjoint functor|adjunction]] $( \epsilon^\sharp \dashv (-)^N )$ from (eq:PullbackSpectrum);

1. the fifth step is application of Lemma \ref{FixedPointSpectrumOfSmashProduct};

1. the sixth step is the evident identification $(S^{\epsilon^\ast \alpha})^N = S^\alpha$ in the first smash factor, and is Lemma \ref{GeometricFixedPointsInTermsOfPlainFixedPoints} in the second factor.

1. the seventh step is again the definition of cohomology.


=--

$\,$

## Examples

+-- {: .num_example #EquivariantStableCohomotopyOfPointsInNontrivalROGDegree}
###### Example
**([[equivariant stable cohomotopy]] of the point in non-trivial [[RO(G)-degree]])**

Let $G$ be a [[finite group]]. Then the canonical comparison morphism (eq:ComparisonMap) from Def. \ref{CanonicalComparisonMap} exhibits the $G$-[[equivariant stable cohomotopy]] [[cohomology groups|group]] of the point in any [[RO(G)-degree]] $V$ that has trivial $N$-fixed points ($V^N = 0$, Def. \ref{ROGDegreeWithoutNonTrivialHFixedPoints}) as a [[group extension]] of the $G/N$-[[equivariant stable cohomotopy]] of the point in [[RO(G)-degree|RO(G/N)-degree]] zero, hence of the group underlying 
the [[Burnside ring]] $A(G/N)$ ([[Burnside ring is equivariant stable cohomotopy of the point|this Prop.]]):

\[
  \label{SurjectionFromEquivariantStableCohomotopyInDegreeVToDegreeZero}
  \mathbb{S}_G^{V}(\ast)
  \overset
    { \phantom{A} \text{epi} \phantom{A} }
    {\longrightarrow}
  \mathbb{S}_{G/N}^0(\ast)
  \simeq
  A(G/N)
  \,.
\]

=--

+-- {: .proof}
###### Proof

First observe that, in the given situation, the comparison morphism $p_{\mathbb{S}}^N(\ast)$ (eq:ComparisonMap) is indeed of the form shown, up to isomorphism: We are in the situation of Prop. \ref{GeometricFixedPointCohomologtIsColimitOverSmashWithEulerClasses} for

1. $X \coloneqq \Sigma^\infty_{G/N}(\ast_+) = \Sigma^\infty_{G/N} S^0$, which is clearly a [[finite spectrum|finite]] $G/N$-[[CW-spectrum]];

1. $E \coloneqq \Sigma^V_G\mathbb{S}_G \coloneqq \Sigma^\infty_G S^V$ the $V$-shifted $G$-[[equivariant sphere spectrum]], being the [[G-spectrum]] [[Brown representability theorem|representing]] $G$-[[equivariant stable cohomotopy]], by definition;

1. $\Phi^N E \simeq \Sigma^\infty_{G/N} (S^V)^N \simeq \Sigma^\infty_{G/N} S^0 \simeq \mathbb{S}_{G/N}$ the unshifted $G/N$-[[equivariant sphere spectrum]], by (eq:PartialGeometricFixedPointsOfEqui) and by assumption on $V$.

Hence with all identifications made explicit, the morphism (eq:SurjectionFromEquivariantStableCohomotopyInDegreeVToDegreeZero) in question is the composite

\[
  \label{ProjectionFromEquivariantCohomotopyOfPpintInRODegreeToBurnside}
  \mathbb{S}_G^V(\ast)
  \simeq
  (\Sigma^\infty_G S^V)^0_{G}(\ast)
  \overset{
    \phantom{AA} 
      p_{ \Sigma^V_G \mathbb{S}_G }^N(\ast) 
    \phantom{AA} 
   }{\longrightarrow}
  (\Phi^N \Sigma^\infty_G S^V)^0_{G/N}(\ast)
  \simeq
  (\Sigma^\infty_{G/N} S^0)^0_{G/N}(\ast)  
  \simeq
  \mathbb{S}^0_{G/N}(\ast)
  \simeq
  A(G/N)
\]

of $p_{ \Sigma^V_G \mathbb{S}_G }^N(\ast)$ with a sequence of [[isomorphisms]], and hence our task is to prove that $p_{ \Sigma^V_G \mathbb{S}_G }^N(\ast)$ is a surjection.

We first prove this for the case that $V = 0$. In this case the identification with the [[Burnside ring]] (via [[Burnside ring is equivariant stable cohomotopy of the point|this Prop.]]) applies also to the [[domain]] cohomology group:

$$
  \mathbb{S}_G^V(\ast)
  \;\simeq\;
  \underset{\underset{V \in G Rep}{\longrightarrow}}{\lim}
  Ho_{G Spaces}\big(S^V, S^V \big)
  \simeq A(G)
  \,,
$$

By Prop. \ref{CanonicalComparisonMap} 
the comparison morphism acts on this by smashing the [[codomain]] of the [[hom-sets]] with $(S^0 \to \tilde E \mathcal{F}[N])$. But by Corollary \ref{SmashingWithTildeEOnspacesEquivalentToRestriction} this is equivalent to restricting to $N$-[[fixed point spaces]] so that (eq:SurjectionFromEquivariantStableCohomotopyInDegreeVToDegreeZero) becomes simply the projection of [[Burnside rings]]

$$
  \array{
    A(G) 
      &\simeq& 
    \underset{\underset{ V \in G Rep }{\longrightarrow}}{\lim}
    &
    Ho_{G Spaces}\big( S^V, S^V \big)
      &\simeq& 
    \mathbb{S}^0_G(\ast) 
    \\
    {}^{\mathllap{ (-)^N }}\big\downarrow 
    &&
    \big\downarrow
    {}^{{}_{
    \mathrlap{
      \array{
        \underset{\underset{V \in G Rep}{\longrightarrow}}{\lim}
        Ho_{G Spaces}\big( 
          S^V, 
          S^V \wedge (S^0 \to \tilde E\mathcal{F}[E]) 
        \big) 
        \\
        =
        \\
        \underset{\underset{V \in G Rep}{\longrightarrow}}{\lim}
        Ho_{G Spaces}\big( 
          (S^V)^N \hookrightarrow  S^V, 
          S^V  
        \big) 
      }
      }
    }
    }
    &
    &&
    \big\downarrow{}^{
      \mathrlap{
        p_\mathbb{S}^N(\ast)
      }
    }
    \\
    A(G/N)
      &\simeq& 
    \underset{\underset{ W \in G/N Rep }{\longrightarrow}}{\lim}
    &
    Ho_{G/N Spaces}\big( S^W, S^W \big)
      &\simeq& 
    \mathbb{S}^0_{G/N}(\ast) 
  }
$$

sending any [[G-set]] $K$ to its [[subset]] $K^N$ of $N$-[[fixed points]] regarded with its residual $G/N$-[[action]].

This is clearly surjective. (The irreducible elements on the right are the isomorphism classes of the  [[transitive action|transitive]] $G/N$-[[actions]]  $(G/N)/H$ for $H \subset G/H$, which are canonically also [[G-sets]], hence have a pre-image on the left.)

In order to deduce the general statement from this special case, we now make use of the fact that Prop. \ref{GeometricFixedPointCohomologtIsColimitOverSmashWithEulerClasses} says that the comparison map for $V = 0$ is one coprojection map of a [[colimit|colimiting]] [[cocone]]-[[diagram]], which for each $G$-[[representation]] $V$ without non-trivial $N$-fixed points (Def. \ref{ROGDegreeWithoutNonTrivialHFixedPoints}) contains a [[cocone]] component of the following form:

\[
  \label{ColimitingCoconeForComparisonAtTrivialROG}
  \array{
    A(G) 
    &=& 
   (\Sigma^\infty_G S^0)^0_{G}(\ast)
   &\overset{ (-) \wedge \chi_V }{\longrightarrow}&
   (\Sigma^\infty_G S^V)^0_{G}(\ast)  
   &\to& \cdots
   \\
   {}^{(-)^N}\big\downarrow && {}^{\mathllap{epi}}\big\downarrow{}^{p_0} & 
   \swarrow_{\mathrlap{p_V}}
   \\
   A(G/N) 
   &=&
   (\Sigma^\infty_{G/N} S^0)^0_{G/N}(\ast) 
  }
\]

Since we know, as just argued, that the map $(-)^N$ on the left is a surjection, the [[commutative diagram|commutativity]] of this diagram implies that also the component projection $p_V$ is surjective. (Every element $c \in A(G/N)$ has a lift to $\widehat c \in A(G)$, but then the commutativity of the triangle means that $\widehat c \wedge \chi_V$ is a pre-image of $c$ under $p_V$.)

This we may use to deduce the statement for the general case, where the codomain of (eq:ProjectionFromEquivariantCohomotopyOfPpintInRODegreeToBurnside) is in degree $V$: 

By the assumption that the [[RO(G)-degree]] $V$ has no non-trivial $N$-fixed points, Prop. \ref{GeometricFixedPointCohomologtIsColimitOverSmashWithEulerClasses} says that the [[colimit|colimiting]] [[cocone]] in which the map $p_{ \Sigma^V_G \mathbb{S}_G }^N(\ast)$ appears, by Def. \ref{CanonicalComparisonMap}, looks just like the one above, except that it "starts" not in degree 0, but in degree $V$: 

\[
  \label{ColimitingCoconeForComparisonAtNonTrivialROG}
  \array{
   &&
   (\Sigma^\infty_G S^V)^0_{G}(\ast)  
   &\to& \cdots
   \\
   & 
   \swarrow_{\mathrlap{p_V}}
   \\
   (\Sigma^\infty_G S^0)^0_{G/N}(\ast) 
  }
\]

In particular the [[cocone]] in (eq:ColimitingCoconeForComparisonAtTrivialROG) restricts to a [[cocone]] over this sub-diagram in (eq:ColimitingCoconeForComparisonAtNonTrivialROG), so that the [[universal property]] of the cocone in (eq:ColimitingCoconeForComparisonAtNonTrivialROG) implies an [[endomorphism]] $\phi$ of the [[abelian group]] underlying the [[Burnside ring]] $(\Sigma^\infty_G S^0)^0_{G/N}(\ast) = A(G/n)$ such that

\[
  \label{Factorization}
  p_V
  \;=\;
  \phi \;\circ\; p_{ \Sigma^V_G \mathbb{S}_G }^N(\ast)
  \,.
\]

Since $p_V$ is surjective, it is now sufficient to prove that this $\phi$ is in fact an [[isomorphism]].

To see this, observe that, since $G$ is a [[finite group]] by assumption, the [[abelian group]] underlying the [[Burnside ring]] $A(G/N)$ is a [[finitely generated module|finitely generated]] [[free abelian group]] (spanned by the cosets $(G/N)/H$ as $H$ ranges over the [[finite set]] of [[conjugacy classes]] of [[subgroups]] of $G/N$ ).
By the [structure theory of free abelian groups](principal+ideal+domain#StructureTheoryOfModules), this means that $\phi$ may be represented by a [[matrix]] in [[Smith normal form]]. Specifically, since $\phi$ is an [[endomorphism]], it is represented by a square matrix in [[Smith normal form]]. Since $\phi \circ p_{ \Sigma^V_G \mathbb{S}_G }^N(\ast)$ is surjective, by (eq:Factorization) and the surjectivity of $p_V$ established before, this implies that $\phi$ is represented by a [[diagonal matrix]] all whose diagonal entries are non-vanishing and invertible, hence that $\phi$ is in fact an [[isomorphism]]. 

With this, (eq:Factorization) says that with $p_V$ also $p_{ \Sigma^V_G \mathbb{S}_G }^N(\ast)$ is surjective.

=--



## Related concepts

* [[fixed point space]]

* [[fixed point spectrum]]

* [[categorical fixed point spectrum]]

* [[homotopy fixed points]]

## References

* {#LewisMaySteinberger86} [[L. Gaunce Lewis]], [[Peter May]], and Mark Steinberger (with contributions by J.E. McClure), _Equivariant stable homotopy theory_, Springer Lecture Notes in Mathematics Vol.1213. 1986 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf))


* {#Lewis00} [[L. Gaunce Lewis, Jr.]], section 10 of _Splitting theorems for certain equivariant spectra_, Memoirs of the AMS, number 686, March 2000, Volume 144 ([pdf](http://hopf.math.purdue.edu/LewisG/spltspec.pdf))

* {#Schwede15} [[Stefan Schwede]], section 7.3 of _[[Lectures on Equivariant Stable Homotopy Theory]]_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/equivariant.pdf))

* {#Schwede18} [[Stefan Schwede]], section 3.3. of _[[Global homotopy theory]]_ ([arXiv:1802.09382](https://arxiv.org/abs/1802.09382))

* {#Blumberg17} [[Andrew Blumberg]], Def. 2.5.16 in _Equivariant homotopy theory_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))

* {#MathewNaumannNoel15} [[Akhil Mathew]], [[Niko Naumann]], [[Justin Noel]], _Nilpotence and descent in equivariant stable homotopy theory_ ([arXiv:1507.06869](http://arxiv.org/abs/1507.06869))

* [[Tom Bachmann]], [[Marc Hoyois]], remark 9.9 in _Norms in motivic homotopy theory_ ([arxiv:1711.03061](https://arxiv.org/abs/1711.03061))

Relation to [[spectral Mackey functors]]:

* {#Glasman15} [[Saul Glasman]], _Stratified categories, geometric fixed points and a generalized Arone-Ching theorem_ ([arXiv:1507.01976](https://arxiv.org/abs/1507.01976), [talk notes pdf](http://www-users.math.umn.edu/~sglasman/strattalk.pdf))


[[!redirects geometric fixed point spectra]]

[[!redirects geometric fixed point]]
[[!redirects geometric fixed points]]

[[!redirects geometric fixed point functor]]
[[!redirects geometric fixed point functors]]

