
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Twisted de Rham cohomology is the [[twisted cohomology]]-version of [[de Rham cohomology]], a simple example of [[twisted differential cohomology]]. 

For degree-3 twists this is the [[codomain]] of the [[twisted Chern character]] on [[twisted K-theory]], and in its [[orbifold cohomology]]-generalization it is the [[codomain]] of the [[twisted equivariant Chern character]] on [[twisted equivariant K-theory]].

## Definition

### Plain

\begin{definition}\label{1TwistedDeRhamCohomology}
  **(1-twisted de Rham cohomology)**\linebreak
  (...)
\end{definition}

\begin{definition}\label{3TwistedDeRhamCohomology}
  **(3-twisted de Rham cohomology)** \linebreak
For $X$ a [[smooth manifold]] and $H \in \Omega^3(X)$ a closed [[differential form|differential 3-form]], the $H$ **twisted de Rham complex** is the $\mathbb{Z}_2$-[[graded vector space]] $\Omega^{even}(X) \oplus \Omega^{odd}(X)$ equipped with the $H$-twisted [[de Rham differential]]

$$
  d + H \wedge(-) \;\colon\; \Omega^{even/odd}(X) \to \Omega^{odd/even}(X)
  \,,
$$


Notice that this is nilpotent, due to the odd degree of $H$, such that $H \wedge H = 0$, and the closure of $H$, $d H = 0$.
\end{definition}

\begin{remark}
There is also the cohomology of the [[chain complex]] whose maps are just multiplication by $H$. 
$$
  H \wedge(-) \;\colon\; \Omega^{even/odd}(X) \to \Omega^{odd/even}(X)
  \,,
$$
This is also called _[[H-cohomology]]_ ([Cavalcanti 03, p. 19](#Cavalcanti03)). 
\end{remark}

### Equivariant
 {#Equivariant}

We discuss notions of twisted de Rham cohomology on ([[global quotient orbifold|global quotient]]) [[orbifolds]], as they are used for the [[codomain]] of the [[twisted equivariant Chern character]] on [[twisted equivariant K-theory]].

This combines the above twistings in degrees 1 and 3, the latter induced from the [[curvature]] [[differential 3-form|3-form]] on a twisting 3-class, the former (an "[[inner local system]]") induced from the [[flat connection]] on the [[circle principal bundle]] (over the [[inertia orbifold]]) which is classified by the [[transgression]] of the 3-twist to a 2-class. This requires that this connection be [[flat connection|flat]], hence that the transgressed 2-class is [[torsion subgroup|torsion]], which is guaranteed by a Lemma that we discuss first, in *[Transgression of the 3-twist to a 1-twist on Inertia](#EquivariantPreliminaries)*.

\linebreak

In all of the the following:

* Let $G$ be a [[finite group]].

  * For $g \in G$ any [[element]], write $C_G(g) \,\subset\, G$ for its [[centralizer subgroup]].

  * Write $C_G(g) \times \mathbb{Z}$ for the [[direct product group]] with the additive [[abelian group]] of [[integers]].

* Let 

  \[
    \label{AProperSmoothGManifold}
    X \in Proper G Actions(SmthMfds)
  \] 

  be a proper smooth [[G-manifold]], hence a [[smooth manifold]] equipped with a [[proper action]] (from the right, say) of $G$ by [[diffeomorphisms]].

  * Notice that for any $g \in G$ the [[fixed locus]] 

    \[
      \label{gFixedLocusInGManifold}
      X^g \xhookrightarrow{\;i_g\;} X
    \] 

    is a smooth [[submanifold]] (by [this Prop.](equivariant+differential}topology#FixedLociOfSmoothProperActionsAreSubmanifolds)).

All twisting classes, in the following are in ordinary Borel-equivariant cohomology, hence in the [[ordinary cohomology]] of a [[Borel construction]]. The "3-twist" and "torsion 2-twist" are in [[integral cohomology]] (of the Borel construction) and the "1-twist" has [[coefficients]] a finite [[cyclic group]].

#### Transgression of 3-twist to 1-twist on inertia
 {#EquivariantPreliminaries}

We discuss the transgression of a 3-twist on a ([[global quotient orbifold|global quotient]]) [[orbifold]] to a 1-twist on its [[inertia orbifold]], namely to a torsion 2-class:

1. [via the Künneth theorem](#TransgressionOf3TwistTo1TwistVieKuenneth)

   as argued in [Becerra & Uribe 2009, Section 3.2](orbifold+K-theory#BecerraUribe09);

1. [via a Serre spectral sequence](#TransgressionOf3TwistTo1TwistViaSerreSpectralSequence)

   as sketched in [Freed, Hopkins & Teleman 07, (3.5)](#FreedHopkinsTeleman07).

There is also a corresponding argument in terms of [[bundle gerbes]], given in [Tu & Xu 2006, Prop. 2.6 & 3.6](#TuXu06).



##### Via Künneth theorem
 {#TransgressionOf3TwistTo1TwistVieKuenneth}

Throughout, fix an element $g \in G$. 

Consider the right [[group action]] of the [[direct product group]] $C_G(g) \times \mathbb{Z}$ (of the [[centralizer subgroup]] with the [[integers]]) on the [[fixed locus]] $X^g$ (eq:gFixedLocusInGManifold) given by

\[
  \label{ActionOfCentralizerTimesIntegersOnFixedLocus}
  \array{
    X^g \times C_G(g) \times \mathbb{Z}
    &\xrightarrow{\;\;\;\;}&
    X^g
    \\
    \big(
      x, \, (h, n)
    \big)
    &\mapsto&
    x \cdot h \cdot g^n
    \mathrlap{\,.}
  }
\]

and notice that the following [[function]] is a [[group homomorphism]] (by the fact that all elements of $C_G(g)$ commute with $g$ in $G$):

\[
  \label{GroupHomomorphismFromCentralizerTimesIntegersIntoG}
  \array{
    C_G(g) \times \mathbb{Z}
    &\xrightarrow{\;\;\phi_g\;\;}&
    G
    \\
    (h,n) &\mapsto& h \cdot g^n
    \mathrlap{\,.}
  }
\]

In view of the action (eq:ActionOfCentralizerTimesIntegersOnFixedLocus), the homomorphism (eq:GroupHomomorphismFromCentralizerTimesIntegersIntoG) induces a map of [[Borel constructions]]

$$
  \big(
    X^g \sslash C_G(g)
    \times 
    B \mathbb{Z}
  \big)
  \;\simeq\;
  X^g 
    \sslash   
  \big(
    C_G(g) \times \mathbb{Z}
  \big)
  \xrightarrow{ \;\; i_g \sslash \phi_g \;\; }
  X 
    \sslash 
  G
  \,,
$$

(where the [[homotopy equivalence]] shown on the left follows since the [[group action]] of  $\mathbb{Z}$ on $X^g$ is the [[trivial action]], by definition (eq:ActionOfCentralizerTimesIntegersOnFixedLocus), and using that the [[Borel construction]] on a point is the [[classifying space]] $ \ast \sslash \mathbb{Z} \,\simeq\, B \mathbb{Z} \simeq S^1$, hence the [[circle]], in the present case)

and hence the corresponding [[pullback in cohomology|pullback in]] [[integral cohomology]]:

\[
  \label{PullbackInCohomologyAlongMorphismOfBorelConstructions}
  \begin{array}{rrl}
  H^\bullet
  \big(
    X \sslash G
    \;
    \, 
    \mathbb{Z}
  \big)
  &
  \xrightarrow{ \; (i_g \sslash \phi_g)^\ast \; }
  & 
  H^\bullet
  \big(
    ( X^g \sslash C_G(g) )
    \times
    B \mathbb{Z}
    \;
    \, 
    \mathbb{Z}
  \big)
  \\
  &
  \,\simeq\,
  &
  H^\bullet
  \big(
    ( X^g \sslash C_G(g) )
    \;
    \, 
    \mathbb{Z}
  \big)
    \otimes_{\mathbb{Z}}
  \underset{
    \mathclap{
      \simeq 
      \left\{
      \array{
        \mathbb{Z} &\vert& \bullet \in \{0,1\}
        \\
        0 &\vert& else
      }
      \right.
    }
  }{
    \underbrace{
      H^\bullet
      \big(
        B \mathbb{Z}
        ;\,
        \mathbb{Z}
      \big)
    }
  }
  \\
  &\simeq &
  H^\bullet
  \big(
    ( X^g \sslash C_G(g) )
    \;
    \, 
    \mathbb{Z}
  \big)
  \,\oplus\,
  H^{\bullet-1}
  \big(
    ( X^g \sslash C_G(g) )
    \;
    \, 
    \mathbb{Z}
  \big)
  \,,
  \end{array}
\]

where the second line uses the [[Künneth theorem]].

(The following definition becomes a proposition if one uses conceptualization of [[transgression]] as laid out in *[[transgression in group cohomology]]*.)

\begin{definition}\label{TransgressionOntoFixedLocus}
  For $g \in G$ write 
  $$
    \tau_g
    \;\colon\;
    H^\bullet
    \big(
      X \sslash G
      ;\, 
      \mathbb{Z}
    \big)
    \xrightarrow{\;\;}
    H^{\bullet-1}
    \big(
      ( X^g \sslash C_G(g) )
      ;\, 
      \mathbb{Z}
    \big)
  $$ 
  for the [[composition|composite]] of (eq:PullbackInCohomologyAlongMorphismOfBorelConstructions) with [[projection]] onto the second [[direct sum|direct summand]].
\end{definition}

\begin{prop}\label{ImageOfTransgressionMapIsInTorsionSubgroup}
  The [[image]] of the transgression map $\tau_g$ (Def. \ref{TransgressionOntoFixedLocus}) is in the [[torsion subgroup]].
\end{prop}
([Becerra & Uribe 2009, Lemma 3.2](orbifold+K-theory#BecerraUribe09))
\begin{proof}
  The group homomorphism (eq:GroupHomomorphismFromCentralizerTimesIntegersIntoG) factors through the [[cyclic group]] $\mathbb{Z} \to \langle g\rangle \to G$ which is generated by $g \in G$. By the assumption that $G$ is a [[finite group]], so that its [[integral cohomology]] is entirely torsion. Since the transgression map factors through a tensor product with pullback along this factorization, by definition, the claim follows. 
\end{proof}

##### Via the Serre spectral sequence
 {#TransgressionOf3TwistTo1TwistViaSerreSpectralSequence}

\begin{lemma}
  For each $g \in G$ and each point in the [[Borel construction]] $X^g \!\sslash\! \frac{C_G(g)}{\langle{g}\rangle}$, there is a [[homotopy fiber sequence]] of the form

\[
  \label{HomotopyFibrationOfBorelConstructionsOnFixedLoci}
  \array{
    B \langle{g}\rangle
    &\longrightarrow&
    X^g \!\sslash\! \langle{g}\rangle
    \\
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow
    \\
    \ast
    &\longrightarrow&
    X^g \!\sslash\! \frac{C_G(g)}{\langle{g}\rangle}
  }
\]
\end{lemma}
\begin{proof}

First notice that the [[short exact sequence]]
$$
  1 
  \to
  \langle{g}\rangle 
    \hookrightarrow 
  C_G(g)
    \twoheadrightarrow 
  G/\langle{g}\rangle
  \to
  1
$$
[[delooping|deloops]] to a [[homotopy fiber]]-sequence of the form
\[
  \label{HomotopyFiberSequenceOfClassifyingSpacesForResidualGroupActions}
  \array{
    B \langle{g}\rangle
    &\longrightarrow&
    B C_G(g)
    \\
    &&
    \big\downarrow
    \\
    &&
    B \frac{C_G(g)}{\langle{g}\rangle}
  }
\]
(using [this Prop.](simplicial+classifying+space#DeloopedKanFibrationOfHomomorphismOfSimplicialGroups)).

Then notice that we have a [[pasting diagram]] of [[homotopy pullbacks]] as follows:

$$
  \array{
    B \langle{g}\rangle
    &\longrightarrow& 
    \ast
    \\
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow
    \\
    X^g \!\sslash\! C_G(g)
    &\xrightarrow{\;}&
    X^g \!\sslash\! \frac{C_G(g)}{\langle{g}\rangle}
    \\
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow
    \\
    B G
    &\xrightarrow{\;}&
    B \frac{C_G(g)}{\langle{g}\rangle}
  }
$$

Here:

* the bottom square being a homotopy pullback expresses that the [[group action]] of $\langle{g}\rangle$ on $X^g$ is trivial, so that the [[group action]] of $C_G(g)$ on $X^g$ is induced by that of $C_G(g)/\langle{g}\rangle$;

* the total rectangle is a homotopy pullback by (eq:HomotopyFiberSequenceOfClassifyingSpacesForResidualGroupActions);

* hence the top square is a homotopy pullback by the [[pasting law]].

\end{proof}

{#ItFollows} It follows -- once we know (do we?) that the action of the [[fundamental group]] of $X^g \sslash \frac{C_G(g)}{\langle{g}\rangle}$ on the [[integral cohomology]] of $B\langle{g}\rangle$ is [[trivial action|trivial]] -- that we have a [[Serre spectral sequence]]

\[
  \label{SerreSpectralSequenceForBorelConstructionOfResidualActions}
  H^p
  \left(
    X^g \!\sslash\! \frac{C_G(g)}{\langle{g}\rangle}
    ;\,
    H^q
    \big(
      B\langle{g}\rangle{g}
      ;\,
      \mathbb{Z}
    \big)
  \right)
  \;\;
    \overset{\;\;\;\;}{\Rightarrow}
  \;\;
  H^{p+q}
  \big(
    X^g \!\sslash\! C_G(g)
    ;\,
    \mathbb{Z}
  \big)
  \,.
\]

But since $\langle{g}\rangle \simeq \mathbb{Z}/(ord(g))$ is a [[cyclic group]] (by the assumption that $G$ is a [[finite group]]) it follows (by [this Prop.](finite+rotation+group#GroupCohomologyOfFiniteSubgroupsOfSU2) or Lem. 4.51 in [BSST 07](Pontrjagin+dual#BSST07)) that its [[group cohomology]] is concentrated in even degrees:

$$
  H^n
  \big(
    B \langle{g}\rangle
    ;\,
    \mathbb{Z}
  \big)
  \;=\;
  H^n_{grp}
  \big(
    \langle{g}\rangle
    ;\,
    \mathbb{Z}
  \big)
  \;\simeq\;
  \left\{
  \begin{array}{ccl}
    \mathbb{Z} &\vert& n = 0
    \\
    \mathbb{Z}/ord(g) &\vert& n = \,\text{positive multiple of}\, 2
    \\
    0 &\vert& \text{otherwise}
  \end{array}
  \right.
$$

Therefore the spectral sequence (eq:SerreSpectralSequenceForBorelConstructionOfResidualActions) associates with any 3-twist $\alpha \mapsto \alpha_{\vert X^g} \in H^3\big( X^g \sslash C_G(g);\, \mathbb{Z}  \big)$ a "transgressed" degree-1 class

\[
  \label{Transgression1ClassFromSerreSpectralSequence}
  \tau_g(\alpha)
  \;\in\;
  H^1
  \left(
    X^g
    ;\,
    \mathbb{Z}/ord(g)
  \right)
  \xrightarrow{\;\;\beta\;\;}
  H^2
  \left(
    X^g
    ;\,
    \mathbb{Z}
  \right)
  \,,
\]

which the [[Bockstein homomorphism]] identifies with a [[torsion subgroup|torsion]] 2-class in [[integral cohomology]].

Essentially this conclusion is claimed as [FHT 07, (3.5)](#FreedHopkinsTeleman07).


#### Definition
 {#DefinitionEquivariantTwistedDeRhamCohomology}

Now we can indicate the definition of the twisted equivariant de Rham cohomology. In outline:

Write $\Lambda (\prec (X \sslash G))$ for the [[inertia orbifold]] of the [[global quotient orbifold]] of $X$ (eq:AProperSmoothGManifold).

For $\alpha \in H^3\big( X \sslash G; \, \mathbb{Z}  \big)$ a "3-twist" in the degree-3 [[integral cohomology]] of the [[homotopy quotient]] ([[Borel construction]]) of $X$ by $G$ (eq:AProperSmoothGManifold)

* let $H_3 \in \Omega^3\big(  \Lambda (\prec (X \sslash G))  \big)$ be a [[de Rham isomorphism|de Rham image]] of $\alpha$ [[pullback in cohomology|pulled back]] to the [[inertia orbifold]], 

* let $\nabla$ be a [[circle bundle with connection|connection]] on the transgression (Def. \ref{TransgressionOntoFixedLocus}) of $\alpha$ to the [[inertia orbifold]], which is [[flat connection|flat]] by Prop. \ref{ImageOfTransgressionMapIsInTorsionSubgroup} or, alternatively, by (eq:Transgression1ClassFromSerreSpectralSequence).

Then equivariant twisted de Rham cohomology of $X$ is the de Rham cohomology of $\Lambda (\prec (X \sslash G))$ which is both 

* 1-twisted by $\nabla$ and 

* 3-twisted by $H_3$ 

([Tu & Xu 2006, Def. 3.10](#TuXu06), [Freed, Hopkins & Teleman 2007, (3.19)](#FreedHopkinsTeleman07), [Bunke, Spitzweck & Schick 08, Def. 3.15](#BunkeSpitzweckSchick08)).



\linebreak

## Properties

### Of 1-Twisted de Rham cohomology

#### Equivalence with $\pi_1$-invariant dR cohomology
 {#EquivalenceWithPiOneInvariantdRCohomology}

In the following, let $\mathrm{X}$ be a [[smooth manifold]], which we assume, without real restriction of generality, to be [[connected topological space|connected]]. Therefore we write $\pi_1(\mathrm{X})$ for its [[fundamental group]], for any fixed choice of [[basepoint]] $x_0 \,\in\, \mathrm{X}$.

We write $\widehat{\mathrm{X}} \xrightarrow{\;} \mathrm{X}$ for its [[universal cover]] (also canonically a smooth manifold). This is a $\pi_1(\mathrm{X})$-[[principal bundle]], in particular it has a canonical $\pi_1(\mathrm{X})$-[[group action|action]] by [[deck transformations]].

For $\mathcal{L}$ a [[complex line bundle]] over $\mathrm{X}$ with [[flat connection]] $\nabla$, write
\[
  \label{HolonomyMap}
  hol_\nabla
  \,\colon\,
  \pi_1(\mathrm{X})
  \xrightarrow{\;\;}
  \mathbb{C}^\times
\]
for the [[group homomorphism]] from the [[fundamental group]] to the multiplicative [[group of units]] $\mathbb{C}^\times \,=\, \mathbb{C} \setminus \{0\}$ which is given by sending a [[smooth curve]] $\lambda \colon [0,1] \to \mathrm{X}$ (with $\lambda(0) = \lambda(1)$) to its [[holonomy]] under the [[parallel transport]] with respect to $\nabla$.

\begin{proposition}
\label{OneTwisteddRCohomologyEquivalentToPiOneInvariantOnUniversalCover}
**(1-Twisted dR cohomology equivalent to $\pi_1$-invariant dR cohomology on universal cover)**
\linebreak
  For $\mathcal{L}$ a [[complex line bundle]] over $\mathrm{X}$ with [[flat connection]] $\nabla$, there is a [[natural isomorphism|natural]] [[isomorphism]] between

1. the $\nabla$-twisted de Rham cohomology on $\mathrm{X}$:

   $$
     H^\bullet
     \Big(
       \Omega_{dR}^\bullet
       \big(
         \mathrm{X}
          ;\,
          \mathcal{L}
       \big)
       ,\,
       \nabla
     \Big)
   $$

1. the untwisted but $\pi_1$-[[invariant]] complex-valued de Rham cohomology on the [[universal cover]] $\widehat{\mathrm{X}}$

   $$
     H^\bullet
     \bigg(
       \Big(
         \Omega^\bullet_{dR}
         \big(
           \widehat{\mathrm{X}}
           ;\,
           \mathbb{C}
         \big)
       \Big)^{\pi_1(\mathrm{X})}  
       ,\,
       \mathrm{d}
     \bigg)
   $$

   where [[fundamental group|$\pi_1(\mathrm{X})$]] [[group action|acts]] on [[differential forms]] by [[pullback of differential forms|pullback]] along [[deck transformations]] combined with multiplication by the [[holonomy]] (eq:HolonomyMap) of $\nabla$:

   $$
     \array{
       \pi_1(\mathrm{X})
       \times
       \Omega^\bullet_{\mathrm{dR}}
       \big(
         \widehat{\mathrm{X}}
         ;\,
         \mathbb{C}
       \big)
       &\xrightarrow{\phantom{--}}&
       \Omega^\bullet_{\mathrm{dR}}
       \big(
         \widehat{\mathrm{X}}
         ;\,
         \mathbb{C}
       \big)
       \\
       \big(
         [\lambda]
         ,\,
         A 
       \big)
       &\mapsto&
       hol_\nabla(\lambda)
       \cdot
       [\lambda]^\ast(A)
     }
   $$

\end{proposition}
A **proof** is spelled out in [this pdf](https://www.dropbox.com/s/l51nx8ptjgi1cff/TwistedDeRhamCohomology.pdf?dl=0). It proceeds by observing that the bundle and its connection trivialize after pullback to the universal cover $\widehat{\mathrm{X}}$, in fact that the local connection form $\widehat{\omega}$ on $\widehat{\mathrm{X}}$ becomes exact (by the [[Poincaré lemma]] for simply connected domains, [here](Poincaré+lemma#ForOneFormsOnSimplyConnectedDomain)):
\[
  \label{MasterFunction}
  \underset{
    \mathclap{\phantom{\vert^{\vert}}}
    { \ell \in }
    \atop
    { 
      C^\infty\big(
        \widehat{\mathrm{X}}
        ;\, 
        \mathbb{C}^\times
     \big) 
    }
  }{\exists}
  \;\;\;
  \widehat{\omega}
  \;=\;
  - \mathrm{d} log \ell
  \,,
  \;\;\;\;
  \in
  \;
  \Omega^1_{dR}
  \big(
    \widehat{\mathrm{X}}
    ,\,
    \mathbb{C}
  \big)
  \,,
\]
and checking that multiplication by this potential $\ell$ (eq:MasterFunction) constitutes a [[isomorphism|isomorphic]] ([[bijection|bijective]]) [[chain map]] between the [[cochain complexes]] in question.


\begin{example}
**(Hypergeometric integral solutions of KZ-equation)**
\linebreak
  For the special case that the [[complex line bundle]] $\mathcal{L}$ is [[trivial bundle|trivial]] (so that the [[flat connection]] $\nabla$ is represented by a globally defined [[differential 1-form]] already on the base manifold $\mathrm{X}$) the statement of Prop. \ref{OneTwisteddRCohomologyEquivalentToPiOneInvariantOnUniversalCover} (or rather its [[holomorphic line bundle|holomorphic]] version) plays a central role in the discussion of the "[hypergeometric integral construction](Knizhnik-Zamolodchikov+equation#BraidRepresentationsViaTwisteddRCohomologyOfConfigurationSpaces)" of solutions to the [[Knizhnik-Zamolodchikov equation]], where it is applied to the case that $\mathrm{X}$ is an $n$-punctured [[Riemann sphere]] (e.g. a [[trinion]]). In fact it is so central to this construction that the function $\ell$ (eq:MasterFunction)
which trivializes the connection form on the universal cover and thereby induces the isomorphism in Prop. \ref{OneTwisteddRCohomologyEquivalentToPiOneInvariantOnUniversalCover} came to be called the "master function", in this context ([Slinkin & Varchenko 2019, §2.1](#SlinkinVarchenko19)).

On the other hand, none of the many references listed [there](Knizhnik-Zamolodchikov+equation#BraidRepresentationsViaTwisteddRCohomologyOfConfigurationSpaces) really make the Proposition explicit.
\end{example}


\linebreak


### Of 3-Twisted de Rham cohomology

+-- {: .num_prop #TwistedDeRhamCohomologyCoincidesWithHCohomologyOnInfinitesimllayThickenedPoint}
###### Proposition

If the [[de Rham complex]] $(\Omega^\bullet(X),d_{dr})$ is [[formal dg-algebra|formal]], then for $H \in \Omega_{cl}^3(X)$ a [[closed differential form|closed]] [[differential 3-form]], the $H$-[[twisted de Rham cohomology]] (Def. \ref{3TwistedDeRhamCohomology}) of $X$ coincides with its [[H-cohomology]], for any closed 3-form $H$. 

=--

([Cavalcanti 03, theorem 1.6](#Cavalcanti03)).


## Related concepts

* [[twisted Chern character]], [[twisted equivariant Chern character]]

* [[inner local system]]

* [[Hanany-Witten effect]]


## References

### Twist in degree 1
 {#ReferencesForTwistInDegree1}

The classical case of twisted de Rham cohomology with twists in *degree 1*, given by [[flat connections]] on [[flat line bundles]] and more generally on [[flat vector bundles]]), and its equivalence to [[sheaf cohomology]] with [[coefficients]] in [[abelian sheaves]] of [[flat sections]] ([[local systems]]):

* {#Voisin02} [[Claire Voisin]] (translated by [[Leila Schneps]]), Section II 5.1.1 of: _[[Hodge theory and Complex algebraic geometry]] II_, Cambridge Stud. in Adv. Math. __76, 77__, 2002/3 ([doi:10.1017/CBO9780511615177](https://doi.org/10.1017/CBO9780511615177))

* [[Alexandru Dimca]], Section 2.5 of: *Sheaves in Topology*, Universitext, Springer (2004) $[$[doi:10.1007/978-3-642-18868-8](https://doi.org/10.1007/978-3-642-18868-8)$]$

Review:

* [[Anatoly Libgober]], [[Sergey Yuzvinsky]], *Cohomology of local systems*, Advanced Studies in Pure Mathematics **27**, Mathematics Society of Japan (2000) 169-184 &lbrack;[pdf](http://homepages.math.uic.edu/~libgober/otherpapers/export/2000sergeytokyo.pdf), [doi:10.2969/aspm/02710169](https://doi.org/10.2969/aspm/02710169)&rbrack;

* Cailan Li, *Cohomology of Local Systems on $X_\Gamma$* ([pdf](http://math.columbia.edu/~mundy/L3.pdf), [[Li_CohomologyOfLocalSystems.pdf:file]])

* Youming Chen, Song Yang, Section 2.1 in: *On the blow-up formula of twisted de Rham cohomology*. Annals of Global Analysis and Geometry volume 56, pages 277–290 (2019) ([arXiv:1810.09653](https://arxiv.org/abs/1810.09653), [doi:10.1007/s10455-019-09667-8](https://doi.org/10.1007/s10455-019-09667-8))

For extensive application, see also the "[hypergeometric integral construction](Knizhnik-Zamolodchikov+equation#BraidRepresentationsViaTwisteddRCohomologyOfConfigurationSpaces)" of solutions to the [[Knizhnik-Zamolodchikov equation]]. 

In this context there is also:

* {#SlinkinVarchenko19} [[Alexey Slinkin]], [[Alexander Varchenko]], *Twisted de Rham Complex on Line and Singular Vectors in $\widehat{\mathfrak{sl}}_2$ Verma Modules*, SIGMA **15** (2019) 075 &lbrack;[arXiv:1812.09791](https://arxiv.org/abs/1812.09791), [doi:10.3842/SIGMA.2019.075](https://doi.org/10.3842/SIGMA.2019.075)&rbrack;

See also at [[supersymmetric quantum mechanics]] and see

* [[Albert Schwarz]], [[Ilya Shapiro]], *Twisted de Rham cohomology, homological definition of the integral and "Physics over a ring"*, Nucl. Phys. B **809** (2009) 547-560 &lbrack;[arXiv:0809.0086](https://arxiv.org/abs/0809.0086), [doi:10.1016/j.nuclphysb.2008.10.005](https://doi.org/10.1016/j.nuclphysb.2008.10.005)&rbrack;




### Twist in degree 3
 {#ReferencesForTwistInDegree3}

#### Plain

The concept of $H_3$-twisted de Rham cohomology  was introduced (in discussion of the [[B-field]] in [[string theory]]), in:

* [[Ryan Rohm]], [[Edward Witten]], around (23) and appendix of: _The antisymmetric tensor field in superstring theory_, Annals of Physics Volume 170, Issue 2, September 1986, Pages 454-489 (<a href="https://doi.org/10.1016/0003-4916(86)90099-0">doi:10.1016/0003-4916(86)90099-0</a>)

Further discussion (often as the [[codomain]] of the [[twisted Chern character]] on [[twisted K-theory]]):

* {#CBMMS}  [[Peter Bouwknegt]], [[Alan Carey]], [[Varghese Mathai]], [[Michael Murray]], [[Danny Stevenson]], Section 9.3 of: _Twisted K-theory and K-theory of bundle gerbes_ ,  Commun Math Phys, 228 (2002) 17-49 ([arXiv:hep-th/0106194](http://arxiv.org/abs/hep-th/0106194), [doi:10.1007/s002200200646](https://doi.org/10.1007/s002200200646))

* [[Varghese Mathai]], [[Danny Stevenson]], Section 3 of: _Chern character in twisted K-theory: equivariant and holomorphic cases_, Commun. Math. Phys. 236:161-186, 2003 ([arXiv:hep-th/0201010](https://arxiv.org/abs/hep-th/0201010))

* {#FreedHopkinsTeleman07} [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], Section 2 of: _Twisted equivariant K-theory with complex coefficients_, Journal of Topology, Volume 1, Issue 1, 2007 ([arXiv:math/0206257](https://arxiv.org/abs/math/0206257), [doi:10.1112/jtopol/jtm001](https://doi.org/10.1112/jtopol/jtm001))

* {#Teleman04} [[Constantin Teleman]], around Prop. 3.7 in: _K-theory of the moduli of bundles over a Riemann surface and deformations of the Verlinde algebra_, in: [[Ulrike Tillmann]] (ed.) _Topology, geometry and quantum field theory_, Cambridge 2004 ([arXiv:math/0306347](https://arxiv.org/abs/math/0306347), [spire:660158](https://inspirehep.net/literature/660158))

* {#Cavalcanti03} [[Gil Cavalcanti]], Section I.4 of: _New aspects of the $d d^c$-lemma_, Oxford  2005 ([arXiv:math/0501406](https://arxiv.org/abs/math/0501406))


#### Equivariant
 {#ReferencesEquivariant3Twisted}

The generalization of 3-twisted de Rham cohomology to [[orbifolds]] (often as the [[codomain]] of the [[twisted equivariant Chern character]] on [[twisted equivariant K-theory]]):

* {#MathaiStevenson03} [[Varghese Mathai]], [[Danny Stevenson]], p. 18 of: *Chern character in twisted K-theory: equivariant and holomorphic cases*, Commun. Math. Phys. **236** (2003) 161-186 ([arXiv:hep-th/0201010](https://arxiv.org/abs/hep-th/0201010), [doi:10.1007/s00220-003-0807-7](https://doi.org/10.1007/s00220-003-0807-7))

  > (via [[equivariant de Rham cohomology]])

* {#TuXu06} [[Jean-Louis Tu]], [[Ping Xu]], Def. 3.10 in: *Chern character for twisted K-theory of orbifolds*, Advances in Mathematics Volume 207, Issue 2, 20 December 2006, Pages 455-483 ([arXiv:math/0505267](https://arxiv.org/abs/math/0505267), [doi:10.1016/j.aim.2005.12.001](https://doi.org/10.1016/j.aim.2005.12.001))

* {#BunkeSpitzweckSchick08} [[Ulrich Bunke]], [[Markus Spitzweck]], [[Thomas Schick]], Section 3.2 of: _Inertia and delocalized twisted cohomology_, Homotopy, Homology and Applications, vol 10(1), pp 129-180 (2008) ([arXiv:math/0609576](https://arxiv.org/abs/math/0609576), [doi:10.4310/HHA.2008.v10.n1.a6](https://dx.doi.org/10.4310/HHA.2008.v10.n1.a6))

See also 

* [Freed, Hopkins & Teleman 07, Paragraph (3.8)](#FreedHopkinsTeleman07)

### Twist in higher degrees
 {#ReferencesTwistInHigherDegrees}

Discussion of higher-degree twisted de Rham cohomology (often as the [[Chern character]]-like image of [higher twisted K-theory](twisted+K-theory#ReferencesHigherTwists)):

* [Teleman 04, Sec. 3](#Teleman04)

* [[Hisham Sati]], *A Higher Twist in String Theory*, J. Geom. Phys. 59:369-373, 2009 ([arXiv:hep-th/0701232](https://arxiv.org/abs/hep-th/0701232))

* [[Varghese Mathai]], [[Siye Wu]], _Analytic torsion for twisted de Rham complexes_, J. Diff. Geom. 88:297-332, 2011 ([arXiv:0810.4204](https://arxiv.org/abs/0810.4204))
  
  > (relation to [[analytic torsion]])

A [[spectral sequence]] for higher twisted de Rham cohomology (analgous to the [[Atiyah-Hirzebruch spectral sequence]] for [[twisted K-theory]] from [Atiyah & Segal 2005](Atiyah–Hirzebruch+spectral+sequence#AtiyahSegal05)):

* {#LiLiuWang09} Weiping Li, Xiugui Liu, [[He Wang]], _On a spectral sequence for twisted cohomologies_,  Chin. Ann. Math. Ser. B 35, 633–658 (2014) ([arXiv:0911.1417](https://arxiv.org/abs/0911.1417), [doi:10.1007/s11401-014-0842-z](https://doi.org/10.1007/s11401-014-0842-z)).

In the broader context of [[twisted cohomology theory]] and the [[Chern-Dold character map]]:

* {#FSS20} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Section 3.3 of: _[[schreiber:The Character Map in Twisted Non-Abelian Cohomology|The character map in (twisted differential) non-abelian cohomology]]_ ([arXiv:2009.11909](https://arxiv.org/abs/2009.11909))




[[!include hypergeometric KZ-solutions -- references]]





[[!redirects twisted de Rham complex]]
