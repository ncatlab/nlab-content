
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

This combines the above twistings in degrees 1 and 3, the latter induced from the [[curvature]] [[differential 3-form|3-form]] on a twisting 3-class, the former induced from the [[flat connection]] on the [[circle principal bundle]] (over the [[inertia orbifold]]) which is classified by the [[transgression]] of the 3-twist to a 2-class. This requires that this connection be [[flat connection|flat]], hence that the transgressed 2-class is [[torsion subgroup|torsion]], which is guaranteed by a Lemma that we discuss first, in *[Transgression of the 3-twist to a 1-twist on Inertia](#EquivariantPreliminaries)*.

\linebreak

In all of the the following:

* Let $G$ be a [[finite group]].

  * For $g \in G$ any [[element]], write $C_G(g) \,\subset\, G$ for [[centralizer subgroup]].

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

For $g \in G$ consider the right [[group action]] of the [[direct product group]] $C_G(g) \times \mathbb{Z}$ on the [[fixed locus]] $X^g$ (eq:gFixedLocusInGManifold) given by

\[
  \label{ActionOfCentralizerTimesIntegersOnFixedLocus}
  \array{
    X^g \times C_G(g) \times \mathbb{Z}
    &\xrightarrow{\;\;\;\;}&
    x
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

But since $\langle{g}\rangle \simeq \mathbb{Z}/(ord(g))$ is a [[cyclic group]] (by the assumption that $G$ is a [[finite group]]) it follows (by [this Prop.](finite+rotation+group#GroupCohomologyOfFiniteSubgroupsOfSU2)) that its [[group cohomology]] is concentrated in even degrees:

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

Essentially this conclusion appears as [FHT 07, (3.5)](#FreedHopkinsTeleman07).


#### Definition
 {#DefinitionEquivariantTwistedDeRhamCohomology}

Now we can indicate the definition of the twisted equivariant de Rham cohomology. In outline:

Write $\Lambda (\prec (X \sslash G))$ for the [[inertia orbifold]] of the [[global quotient orbifold]] of $X$ (eq:AProperSmoothGManifold).

For $\alpha \in H^3_G(X)$

* let $H_3 \in \Omega^3\big(  \Lambda (\prec (X \sslash G))  \big)$ be a de Rham image of $\alpha$ pulled back to the inertia orbifold, 

* let $\nabla$ be a connection on the transgression (Def. \ref{TransgressionOntoFixedLocus}) of $\alpha$ to the inertia orbifold, which is [[flat connection|flat]] by Prop. \ref{ImageOfTransgressionMapIsInTorsionSubgroup} or, alternatively, by (eq:Transgression1ClassFromSerreSpectralSequence).

Then equivariant twisted de Rham cohomology of $X$ is the de Rham cohomology of $\Lambda (\prec (X \sslash G))$ which is both 

* 1-twisted by $\nabla$ and 

* 3-twisted by $H_3$ 

([Tu & Xu 2006, Def. 3.10](#TuXu06), see also [Bunke, Spitzweck & Schick 08, Def. 3.15](#BunkeSpitzweckSchick08)).

\linebreak

## Properties

+-- {: .num_prop #TwistedDeRhamCohomologyCoincidesWithHCohomologyOnInfinitesimllayThickenedPoint}
###### Proposition

If the [[de Rham complex]] $(\Omega^\bullet(X),d_{dr})$ is [[formal dg-algebra|formal]], then for $H \in \Omega_{cl}^3(X)$ a [[closed differential form|closed]] [[differential 3-form]], the $H$-[[twisted de Rham cohomology]] (Def. \ref{3TwistedDeRhamCohomology}) of $X$ coincides with its [[H-cohomology]], for any closed 3-form $H$. 

=--

([Cavalcanti 03, theorem 1.6](#Cavalcanti03)).

## References

### Twist in degree 1
 {#ReferencesForTwistInDegree1}

The classical case of twisted de Rham cohomology with twists in *degree 1*, given by [[flat connections]] on [[flat line bundles]] and more generally on [[flat vector bundles]]), and its equivalence to [[sheaf cohomology]] with [[coefficients]] in [[abelian sheaves]] of [[flat sections]] ([[local systems]]):

* {#Voisin02} [[Claire Voisin]] (translated by [[Leila Schneps]]), Section II 5.1.1 of: _[[Hodge theory and Complex algebraic geometry]] II_, Cambridge Stud. in Adv. Math. __76, 77__, 2002/3 ([doi:10.1017/CBO9780511615177](https://doi.org/10.1017/CBO9780511615177))

Review:

* Cailan Li, *Cohomology of Local Systems on $X_\Gamma$* ([pdf](http://math.columbia.edu/~mundy/L3.pdf), [[Li_CohomologyOfLocalSystems.pdf:file]])

* Youming Chen, Song Yang, Section 2.1 in: *On the blow-up formula of twisted de Rham cohomology*. Annals of Global Analysis and Geometry volume 56, pages 277–290 (2019) ([arXiv:1810.09653](https://arxiv.org/abs/1810.09653), [doi:10.1007/s10455-019-09667-8](https://doi.org/10.1007/s10455-019-09667-8))


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

Discussion of higher-degree twisted de Rham cohomology (often a the character image of [higher twisted K-theory](twisted+K-theory#ReferencesHigherTwists)):

* [Teleman 04, Sec. 3](#Teleman04)

* [[Hisham Sati]], *A Higher Twist in String Theory*, J. Geom. Phys. 59:369-373, 2009 ([arXiv:hep-th/0701232](https://arxiv.org/abs/hep-th/0701232))

* [[Varghese Mathai]], [[Siye Wu]], _Analytic torsion for twisted de Rham complexes_, J. Diff. Geom. 88:297-332, 2011 ([arXiv:0810.4204](https://arxiv.org/abs/0810.4204))
  
  > (relation to [[analytic torsion]])

In the broader context of [[twisted cohomology theory]] and the [[Chern-Dold character map]]:

* {#FSS20} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Section 3.3 of: _[[schreiber:The Character Map in Twisted Non-Abelian Cohomology|The character map in (twisted differential) non-abelian cohomology]]_ ([arXiv:2009.11909](https://arxiv.org/abs/2009.11909))



[[!redirects twisted de Rham complex]]
