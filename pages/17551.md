
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

{#PartialGeometricFixedPoint} This generalizes to a "partial" geometric fixed point functor, which for a given [[subgroup]] $H \subset G$ sends 

$$
  \Phi^H \;\colon\; G Spectra \longrightarrow W_G H Spectra
$$

(for $W_G/H$ the [[Weyl group]], which is the [[quotient group]] $G/H$ in the case that $H$ is a [[normal subgroup]]) and satisfies for a $G$-[[equivariant suspension spectrum]] $\Sigma^\infty_G X$ the relation

\[
  \label{PartialGeometricFixedPointsOfEqui}
  \Phi^N \big(  \Sigma^\infty_G X \big) 
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

([Lewis-May-Steinberger 86, II.9, cor. 9.9](#LewisMaySteinberger86), [Lewis 00, Scholium 10.2](#Lewis00))



### As inversion of Euler classes
 {#AsInversionOfEulerClasses}

We discuss an explicit formula (Prop. \ref{GeometricFixedPointCohomologtIsColimitOverSmashWithEulerClasses} below) that expresses [[equivariant cohomology|equivariant]] [[cohomology groups]] with [[coefficients]] in partial geometric fixed point spectra as the [[equivariant cohomology|equivariant]] [[cohomology groups]] with [[coefficients]] in the original spectrum, but with certain "[[Euler classes]] [[localization|inverted]]".

A key role in this discussion is played by those [[RO(G)-degrees]] which trivialize when passing to partial fixed points:

+-- {: .num_defn #ROGDegreeWithoutNonTrivialHFixedPoints}
###### Definition
**([[RO(G)-degrees]] without non-trivial $H$-fixed points)**

For $H \subset G$ a [[subgroup]], say that a $G$-[[representation]] $V$ has _no non-trivial $H$-fixed points_ if the [[fixed point space]] of $V$ with respect to the $H$-[[action]] is the origin (which is necessarily fixed), hence is the [[zero object|zero]]-[[representation]]:

$$
  V^H \;=\; 0
$$


=--

Fix now 

$$
  N \overset{\phantom{AA}}{\hookrightarrow} G 
  \overset{ \phantom{A} \epsilon \phantom{A} }{\longrightarrow}
  G/N
$$ 

a [[normal subgroup]]-inclusion with induced [[projection]] $\epsilon$ to the [[quotient group]] $G/N$. 

By [[base change]] this induces various comparison maps between concepts defined with respect to $G$ and $G/N$, we denote these by

\[
  \label{PullbackGSpace}
  G/N Spaces 
  \overset{ \epsilon^\sharp }{\longrightarrow}
  G Spaces
\]

\[
  \label{PullbackRepresentation}
  G/N Rep \overset{ \epsilon^\ast }{\longrightarrow} G Rep
\]



Let now

$$
  E
  \;\in\;
  G Spectra
$$ 

be a [[G-spectrum]] with partial geometric fixed point spectrum

$$
  \Phi^N E \;\in\; G/N Spectra
  \,.
$$

and let

$$
  X
  \;\in\;
  G/N Spectra^{fin}
  \overset{\epsilon^\sharp}{\longrightarrow}
  G Specta
$$

be [[finite spectrum|finite]] $G$-[[CW-spectrum]], 


+-- {: .num_prop #GeometricFixedPointCohomologtIsColimitOverSmashWithEulerClasses}
###### Proposition
**(partial geometric fixed point cohomology via inversion of Euler classes)**

The $G/N$-[[equivariant cohomology|equivariant]] [[cohomology groups]] in [[RO(G)-degree|RO(G/N)-degree]] $\alpha$ of $X$ with [[coefficients]] in the partial geometric fixed point spectrum $\Phi^N E$ are equivalently the [[colimit]] over the $G$-[[equivariant cohomology|equivariant]] [[cohomology groups]] of $\epsilon^\sharp X$ (eq:PullbackGSpace) with [[coefficients]] in $E$, but in [[RO(G)-degree]] $\epsilon^\ast \alpha$ (eq:PullbackRepresentation) plus a shift by all those [[representations]] $V$ that have no nontrivial $N$-fixed points (Def. \ref{ROGDegreeWithoutNonTrivialHFixedPoints}):

\[
\label{ColimitConstructionForCohomologyWithCoeffsInPartialGeometricFixedPointSpectra}
  (\Phi^N E)^\bullet_{G/N}(X)
  \;\simeq\;
  \underset{\underset{\{V \vert V^N = 0\}}{\longrightarrow}}{\lim}
  E^{\epsilon^\ast \bullet + V}(\epsilon^\sharp X)  
  \,,
\]

where the [[colimit]] is over the [[diagram]] that has precisely one morphism for every inclusion  $V_1 \subset V_2$ of $G$-representations without non-trivial $N$-fixed points (Def. \ref{ROGDegreeWithoutNonTrivialHFixedPoints})

$$
  E^{\epsilon^\ast \bullet + V_1}(\epsilon^\sharp X)   
  \overset{ (-) \wedge \chi_{V_2 - V_1} }{\longrightarrow}
  E^{\epsilon^\ast \bullet + V_2}(\epsilon^\sharp X)   
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

of $V = V_2 - V_1$.

=--

([Lewis-May-Steinberger 86, chapter II, prop. 9.13](#LewisMaySteinberger86))

+-- {: .num_defn #CanonicalComparisonMap}
###### Definition
**(canonical comparison map to partial geometric fixed point cohomology)**

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

from the $G$-[[equivariant cohomology|equivariant]] [[cohomology groups]] with [[coefficients]] in $E$ to the those with [[coefficients]] in the partial geometric fixed point spectrum:

The morphism is the component of the [[colimit|colimiting]] [[cocone]](eq:ColimitConstructionForCohomologyWithCoeffsInPartialGeometricFixedPointSpectra) at stage $V = 0$:

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

=--


+-- {: .num_example}
###### Example
**([[equivariant stable cohomotopy]] of the point in non-trivial [[RO(G)-degree]])**

Let $G$ be a [[finite group]]. Then the canonical comparison morphism (eq:ComparisonMap) from Def. \ref{CanonicalComparisonMap} exhibits the $G$-[[equivariant stable cohomotopy]] [[cohomology groups|group]] of the point in any [[RO(G)-degree]] $V$ that has trivial $N$-fixed points ($V^N = 0$, Def. \ref{ROGDegreeWithoutNonTrivialHFixedPoints}) as a [[group extension]] of the $G/N$-[[equivariant stable cohomotopy]] of the point in [[RO(G)-degree|RO(G/N)-degree]] zero:

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

where the latter group is equivalently that underlying the [[Burnside ring]] $A(G/N)$ ([this Prop.](equivariant+stable+cohomotopy#BurnsideRingIsEquivariantStableCohomotopyOfPoint)).

=--

Proof idea (check):

First observe that, in the given situation, the comparison morphism $p_{\mathbb{S}^N(\ast)}$ (eq:ComparisonMap) is indeed of the form shown, up to isomorphism: We are in the situation of Prop. \ref{GeometricFixedPointCohomologtIsColimitOverSmashWithEulerClasses} for

1. $X \coloneqq \Sigma^\infty_{G/N}(\ast_+) = \Sigma^\infty_{G/N} S^0$, which is clearly a [[finite spectrum|finite]] $G/N$-[[CW-spectrum]];

1. $E \coloneqq \Sigma^V_G\mathbb{S}_G \coloneqq \Sigma^\infty_G S^V$ the $V$-shifted $G$-[[equivariant sphere spectrum]], being the [[G-spectrum]] [[Brown representability theorem|\representing]] $G$-[[equivariant stable cohomotopy]], by definition;

1. $\Phi^N E \simeq \Sigma^\infty_{G/N} (S^V)^N \simeq \Sigma^\infty_{G/N} S^0 \simeq \mathbb{S}_{G/N}$ the unshifted $G/N$-[[equivariant sphere spectrum]], by (eq:PartialGeometricFixedPointsOfEqui) and by assumption on $V$.

Hence with all identifications made explicit, the morphism (eq:SurjectionFromEquivariantStableCohomotopyInDegreeVToDegreeZero) in question is this:

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
  \,.
\]

We first prove that this is a surjection for the case that $V = 0$. In this case the identification with the [[Burnside ring]] (via [this Prop.](equivariant+stable+cohomotopy#BurnsideRingIsEquivariantStableCohomotopyOfPoint)) applies also to the [[domain]] cohomology group, so that (eq:SurjectionFromEquivariantStableCohomotopyInDegreeVToDegreeZero) becomes simply the projection of [[Burnside rings]]

$$
  A(G) \overset{ \phantom{AA} (-)^N \phantom{AA} }{\longrightarrow} A(G/N)
$$

given by... 

> (does this need justification?)

...sending any [[G-set]] $S$ to its [[subset]] $S^N$ of $N$-[[fixed points]] regarded with its residual $G/N$-[[action]].

This is clearly surjective. (The irreducible elements on the right are the isomorphism classes of the  [[transitive action|transitive]] $G/N$-[[actions]]  $(G/N)/H$ for $H \subset G/H$, which are canonically also [[G-sets]], hence have a pre-image on the left.)

But Prop. \ref{GeometricFixedPointCohomologtIsColimitOverSmashWithEulerClasses} says that this projection map is also part of a [[colimit|colimiting]] [[cocone]]-[[diagram]], which for each $G$-[[representation]] $V$ without non-trivial $N$-fixed points (Def. \ref{ROGDegreeWithoutNonTrivialHFixedPoints}) contains a [[cocone]] component of the following form:


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
   (\Sigma^\infty_G S^0)^0_{G/N}(\ast) 
  }
\]

Since we know that the map $(-)^N$ on the left is surjection, the [[commutative diagram|commutativity]] of this diagram implies that also the component projection $p_V$ is surjective. (Every element $c \in A(G/N)$ has a lift to $\widehat c \in A(G)$, but then the commutativity of the triangle means that $\widehat c \wedge \chi_V$ is a pre-image of $c$ under $p_V$.)

This we may use to deduce the statement for the general case, where the codomain of (eq:ProjectionFromEquivariantCohomotopyOfPpintInRODegreeToBurnside) is in degree $V$: 

By the assumption that the [[RO(G)-degree]] $V$ has no non-trivial $N$-fixed points, Prop. \ref{GeometricFixedPointCohomologtIsColimitOverSmashWithEulerClasses} says that the [[colimit|colimiting]] [[cocone]] in which the map $p_{ \Sigma^V_G \mathbb{S}_G }^N(\ast)$ appears, by Def. \ref{CanonicalComparisonMap}, looks just like the one above, except that it "starts" not in degree 0, but in degree $V$: 

\[
  \label{ColimitingCoconeForComparisonAtNonTrivialROG}
  \array{
   &&
   (\Sigma^\infty_G S^V)^0_{G}(\ast)  
   &\to& \cdots
   \\
   {}^{\mathllap{}}\big\downarrow{}^{  } & 
   \swarrow_{\mathrlap{p_V}}
   \\
   (\Sigma^\infty_G S^0)^0_{G/N}(\ast) 
  }
\]

In particular the [[cocone]] in (eq:ColimitingCoconeForComparisonAtTrivialROG) restricts to a [[cocone]] over this sub-diagram in (eq:ColimitingCoconeForComparisonAtNonTrivialROG), so that the [[universal property]] of the cocone in (eq:ColimitingCoconeForComparisonAtNonTrivialROG) implies an [[endomorphism]] $\phi$ of the [[abelian group]] underlying the[[Burnside ring]] $(\Sigma^\infty_G S^0)^0_{G/N}(\ast) = A(G/n)$ such that

\[
  \label{Factorization}
  p_V
  \;\;
  \phi \circ p_{ \Sigma^V_G \mathbb{S}_G }^N(\ast)
  \,.
\]

Since $p_V$ is surjective, by the previous dicussion, it must be that $\phi$ is surjective.

Now the [[abelian group]] underlying the [[Burnside ring]] is a [[finitely generated module|finitely generated]] [[free abelian group]].
This implies (...) that for the endomorphism $\phi$ to be surjective, it must indeed be an isomorphism. With this, (eq:Factorization) says that $p_{ \Sigma^V_G \mathbb{S}_G }^N(\ast)$ is isomorphic to a surjection, hence is itself surjective.


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



[[!redirects geometric fixed point spectra]]

[[!redirects geometric fixed point]]
[[!redirects geometric fixed points]]


