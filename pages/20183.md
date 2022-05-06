Y
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

If $n = 2k+1$ is an [[odd number]]:

$$
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
$$

for some 

\[
  \label{RationalEulerClass}
  c_{2k+2} \in A_X
\] 

being the rational [[Euler class]] of the [[spherical fibration]];


If $n = 2k$ is an [[even number]]:

$$
  A_E
  \;=\;
  A_X 
    \otimes 
  \mathbb{Q}
  \Big[
    \big(\omega_{2k} + \tfrac{1}{2} a_{2k} \big) , \omega_{4k-1}
  \Big]
  /
  \left(
    \array{
      d 
      \big( 
        \omega_{2k} 
        + 
        \tfrac{1}{2} a_{2k}
      \big)
      &=& 
      0
      \\
      d \omega_{4k-1} 
      & =& 
      \big(
         \omega_{2k} 
          + 
          \tfrac{1}{2} a_{2k}
       \big)^2
       + 
       c_{4k}
    }
  \right)
$$

for some 

\[
  \label{RationalPontryaginClass}
  c_{4k} \in A_X
\]

being the rational [[Pontryagin class]] of the [[spherical fibration]],

and some $a_{2k} \in A_X$.


=--

([Félix-Halperin-Thomas 00, 15, Example 4, p. 202](#FelixHalperinThomas00))


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
      S^{2n-1} &\vert& n \, \text{odd}\,, deg(f) \neq 0
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

* [[Sullivan model of a sphere]]

* [[Sullivan model of mapping space]]

* [[Sullivan model of free loop space]]


## References

* {#FelixHalperinThomas00} [[Yves Félix]], [[Steve Halperin]], J.C. Thomas, _Rational Homotopy Theory_, Graduate Texts in Mathematics, 205, Springer-Verlag, 2000.

* {#MollerRaussen85} [[Jesper Møller]], [[Martin Raussen]], _Rational Homotopy of Spaces of Maps Into Spheres and Complex Projective Spaces_, Transactions of the American Mathematical Society Vol. 292, No. 2 (Dec., 1985), pp. 721-732 ([jstor:2000242 ](https://www.jstor.org/stable/2000242)) 

* {#CohenVoronov05} [[Ralph Cohen]], [[Alexander Voronov]], _Notes on string topology_ ([arXiv:math/0503625](https://arxiv.org/abs/math/0503625))


[[!redirects Sullivan mode of spherical fibrations]]

[[!redirects Sullivan models of spherical fibrations]]

