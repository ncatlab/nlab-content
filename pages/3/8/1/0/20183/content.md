
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[minimal model]] for a [[spherical fibration]] in [[rational homotopy theory]].

## Properties

### Rational Euler- and Pontryagin-class
 {#RationalEulerAndPontryaginClasses}

+-- {: .num_prop #SullivanModelForSphericalFibration}
###### Proposition

Let $n \in \mathbb{N}$ be a [[natural number]], $n \geq 1$, let

\[
  \label{SphericalFibration}
  \array{
    S^n &\longrightarrow& E
    \\
    && \big\downarrow
    \\
    && X
  }
\]

be a [[spherical fibration]] of [[topological spaces]] such that $X$ admits a [[Sullivan model]] $A_X \in dgcAlg$. Then a [[Sullivan model]] $A_E$ for the total space $E$ is of the following form:

**$n$ odd**

If $n = 2k+1$ is an [[odd number]], then

\[
  \label{SullivanModelForOddDimensionalSphericalFibration}
  A_E 
  \;=\;
  A_X 
    \otimes 
  \mathbb{Q}\big[
    \omega_{2k+1}
  \big]
  /
  \big(
    d \omega_{2k+1} = c_{2k+2}
  \big)
\]

for some 

\[
  \label{RationalEulerClass}
  c_{2k+2} \in A_X
\] 

being the rational [[Euler class]] of the [[spherical fibration]].

In particular, if $E = S(V)$ is the [[unit sphere bundle]] of a [[real vector bundle]] $V \to X$, then 

$$
  [c_{2k}] = \chi
$$

is the [[Euler class]] of that vector bundle and $\omega_{2k+1}$ is a [[cochain]] on the [[unit sphere bundle]] $S(E)$ which on the [[fundamental class]] of any [[n-sphere|(2k+1)-sphere]] [[fiber]] evaluates to minus unity:

\[
  \label{FiberIntegrationOfOddGenerator}
  \left\langle
    \omega_{2k+1},
    \left[
      S^{2k+1}
    \right]
  \right\rangle
  \;=\;
  -1
  \,.
\]

\linebreak

**$n$ even**

If $n = 2k$ is an [[even number]], then [[generalized the|the]] [[Sullivan model]] $A_E$ for a rank-$2k$ [[spherical fibration]] over some $X$ with [[Sullivan model]] $A_X$ is

\[
  \label{FibS2kModel}
  A_E
  \;=\;
  A_X 
    \otimes 
  \mathbb{Q}
  \Big[
    \omega_{2k} , \omega_{4k-1}
  \Big]
  /
  \left(
    \array{
      d 
      \,
      \omega_{2k}
      &=& 
      0
      \\
      d \omega_{4k-1} 
      & =& 
      -
      \omega_{2k} \wedge \omega_{2k}
      + 
      c_{4k} 
    }
  \right)
\]

where

1. the new generator $\omega_{2k}$ evaluates to unity on the [[fundamental classes]] of the [[n-sphere|2k-sphere]] [[fibers]] $S^{2k} \simeq E_x \hookrightarrow E$ over each point $x \in X$:

   $$
     \big\langle  \omega_{2k}, [S^{2k}] \big\rangle
     \;=\;
     1
   $$

1. $c_{4k} \in A_X$ is some element in the base algebra, which by (eq:FibS2kModel) is closed and represents the rational [[cohomology class]] of the [[cup product|cup]] square of the class of $\omega_{2k}$:

   $$
     \big[
       c_{4k}
     \big]
     \;=\;
     \big[ 
       \omega_{2k} 
     \big]^2
     \;\in\;
     H^{4k}
     \big( 
      X, \mathbb{Q}
     \big)
   $$

   and this class classifies the spherical fibration, rationally.

Moreover, if the [[spherical fibration]] $E \to X$ happens to be the [[unit sphere bundle]] $E = S(V)$ of a [[real vector bundle]] $V \to X$, then

1. the class of $\omega_{2k}$ is $1/2$ the rationalized [[Euler class]] $\chi(\widehat V)$ of the corresponding (...) rank [[reduction of the structure group|reduction]] $\widehat V$ of $V$:

   $$
     \big[ \omega_{2k} \big]
     \;=\;
     \tfrac{1}{2}\chi\big( \widehat V \big)
     \;\in\;
     H^{2k}\big( X, \mathbb{Q} \big)
   $$

1. the class of $c_{4k}$ is $1/4$th the rationalized $k$th [[Pontryagin class]] $p_k(V)$ of $V$:

   $$
     \big[
       c_{4k}
     \big]
     \;=\;
     \tfrac{1}{4}
     p_k(V)
     \;\in\;
     H^{4k}\big( X, \mathbb{Q}\big)
     \,.
   $$

=--

This may be found as [Félix-Halperin-Thomas 00, 15, Example 4, p. 202](#FelixHalperinThomas00), see also [Félix-Oprea-Tanré 16, Prop. 2.3](#FelixOpreaTanre16). The fiber integral (eq:FiberIntegrationOfOddGenerator) follows by [this Prop.](Euler+class#TrivializationOfEulerFormOnUnitSphereBundle).

+-- {: .num_remark #NonMinimalityOfSullivanModels}
###### Remark

Beware that the Sullivan models for spherical fibrations in Prop. \ref{SullivanModelForSphericalFibration} are not in general _minimal_ Sullivan models. 

For example over the [[classifying space]] $B SO(8)$ of [[SO(8)]] with indecomposable [[Euler class]] generator $\chi_8$ the equation $d \omega_7 = \chi_8$ (eq:SullivanModelForOddDimensionalSphericalFibration) for the univeral 7-sperical fibration $S^7 \sslash SO(8) \to B SO(8)$ violates the Sullivan minimality condition (which requires that the right hand side is at least a binary wedge product of generators, or equivalently that the degree of the new generator $\omega_7$ is greater than that of any previous generators).

But the Sullivan models in Prop. \ref{SullivanModelForSphericalFibration} are _relative_ minimal models, relative to the Sullivan model for the base.

This means in particular that the new generators of these models reflect non-[[torsion subgroup|torsion]] [[relative homotopy groups]], but not in general non-torsion absolute homotopy groups.

=--

### Relation to rational mapping space of spheres

By general facts (see at [[∞-action]]) a spherical fibration as in (eq:SphericalFibration) is classified by a map to the [[classifying space]] $B Aut(S^n)$ of the [[automorphism ∞-group]] $Aut(S^n) \hookrightarrow Maps(S^n, S^n)$ inside the [[mapping space]] from $S^n$ to itself, which is those [[connected components]] corresponding to [[degree of a continuous function|degree]] $\pm 1$

$$
  Aut(S^n) \;=\; Maps_{\pm 1}\big( S^n, S^n\big)
  \,.
$$

Hence the spherical fibration is given by the [[homotopy pullback]]

\[
  \label{SphericalFibration}
  \array{
    S^n 
      &\longrightarrow& 
    E
      &\longrightarrow& 
    S^{n}\sslash Aut(S^n)
    \\
    && 
    \big\downarrow
    &{}_{(pb)}&
    \big\downarrow
    \\
    && 
    X
    &\underset{c}{\longrightarrow}&
    B Aut(S^n)
  }
\]

of the universal spherical fibration along a classifying map $c$.


The rational homotopy type of these [[connected components]] of the [[mapping space]] are given by [[Sullivan models of mapping spaces]]:

+-- {: .num_prop #RationalTypeOfMappingSpaceSnToSn}
###### Proposition     

Let $n \in \mathbb{N}$ be a [[natural number]] and $fcolon S^n \to S^n$ a [[continuous function]] from the [[n-sphere]] to itself. Then the [[connected component]] $Maps_f\big( S^n, S^n\big)$ of the [[mapping space]] which contains this map has the following [[rational homotopy theory|rational]] [[homotopy type]]:

\[
  \label{RationalHomotopyTypeOfMappingSpacesSnToSn}
  Maps_f\big( S^n, S^n\big)
  \;\simeq_{\mathbb{Q}}\;
  \left\{
    \array{
      S^n \times S^{n-1} &\vert& n\,\text{even}\,, deg(f) = 0
      \\
      S^{2n-1} &\vert& n \, \text{even}\,, deg(f) \neq 0
      \\
      S^n &\vert& n\, \text{odd}
    }
  \right.
\]

where $deg(f)$ is the [[degree of a continuous function|degree]] of $f$.

=--

([Møller-Raussen 85, Example 2.5](#MollerRaussen85), [Cohen-Voronov 05, Lemma 5.3.5](#CohenVoronov05))

+-- {: .num_remark}
###### Remark

Here Prop. \ref{RationalTypeOfMappingSpaceSnToSn} and Prop. \ref{SullivanModelForSphericalFibration} are two aspects of the same situation: 

For $n = 2k+1$ an [[odd number]] the rational [[Euler class]] (eq:RationalEulerClass) of the spherical fibration is the class of the rational classifying map to the shift of $S^{2k+1}$ in (eq:RationalHomotopyTypeOfMappingSpacesSnToSn);

for $n = 2k$ an [[even number]] the rational [[Pontryagin class]] (eq:RationalPontryaginClass) of the spherical fibration is the class of the rational classifying map to the shift of $S^{4k-1}$ in (eq:RationalHomotopyTypeOfMappingSpacesSnToSn).

=--





## Related concepts

[[!include Sullivan models -- examples]]


## References

* {#FelixHalperinThomas00} [[Yves Félix]], [[Steve Halperin]], J.C. Thomas, _Rational Homotopy Theory_, Graduate Texts in Mathematics, 205, Springer-Verlag, 2000.

* {#MollerRaussen85} [[Jesper Møller]], [[Martin Raussen]], _Rational Homotopy of Spaces of Maps Into Spheres and Complex Projective Spaces_, Transactions of the American Mathematical Society Vol. 292, No. 2 (Dec., 1985), pp. 721-732 ([jstor:2000242 ](https://www.jstor.org/stable/2000242)) 

* {#CohenVoronov05} [[Ralph Cohen]], [[Alexander Voronov]], _Notes on string topology_ ([arXiv:math/0503625](https://arxiv.org/abs/math/0503625))

* {#FelixOpreaTanre16} [[Yves Félix]], John Oprea, Daniel Tanré, Prop. 2.3 in _Lie-model for Thom spaces of tangent bundles_, Proc. Amer. Math. Soc. 144 (2016), 1829-1840 ([pdf](http://www.ams.org/journals/proc/2016-144-04/S0002-9939-2015-12829-8/S0002-9939-2015-12829-8.pdf), [doi:10.1090/proc/12829](https://doi.org/10.1090/proc/12829))

[[!redirects Sullivan mode of spherical fibrations]]

[[!redirects Sullivan models of spherical fibrations]]

