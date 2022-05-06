
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
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
 {#Idea}

In analogy to how the [[representation ring]] of a [[finite group]] is equivalently the [[equivariant K-theory]] of the point, so the [[equivariant stable cohomotopy]] of the point is the _[[Burnside ring]]_.

[[!include Segal completion -- table]]


## Statement


+-- {: .num_prop #BurnsideRingIsEquivariantStableCohomotopyOfPoint}
###### Proposition
**([[Burnside ring]] is [[equivariant stable cohomotopy]] of the [[point]])**

Let $G$ be a [[compact Lie group]] (for instance a [[finite group]]). Its [[Burnside ring]] $A(G)$ is [[isomorphism|isomorphic]] to the [[equivariant stable cohomotopy]] [[cohomology ring]] $\mathbb{S}_G(\ast)$ of the [[point]] in degree 0, via the Lefschwetz-Dold index:

$$
  A(G)
    \underoverset{\simeq}{LD}{\longrightarrow} 
  \mathbb{S}_G(\ast)
  \,.
$$

More in detail, for $G$ a [[finite group]], this [[isomorphism]] identifies the [[Burnside character]] on the left with the [[fixed locus]]-[[degree of a continuous function|degrees]] on the right, hence for all [[subgroups]] $H \subset G$ it identifies

1. the $H$-[[Burnside marks]] $\left\vert S^H \right\vert \in \mathbb{Z}$ of [[virtual representation|virtual]] [[finite set|finite]] [[G-sets]] $S$ 

   (which, as $H \subset G$ ranges, completely characterize the [[G-set]], by [this Prop.](table+of+marks#BurnsideCharacterIsInjective))

1. the [[degree of a continuous function|degrees]] $deg\left( \left(LD(S)\right)^H\right) \in \mathbb{Z}$ at $H$-[[fixed points]] of representative [[equivariant Cohomotopy]] [[cocycles]] $LD(S) \colon S^V \to S^V$ 

   (which completely characterize the [[equivariant Cohomotopy]]-class by the [[equivariant Hopf degree theorem]], [this Prop.](Hopf+degree+theorem#EquivariantHopfDegreeTheorem))

\[
  \label{CorrespondenceOnMarksAndDegrees}
  \array{
    A(G)
    &\underoverset{\simeq}{LD}{\longrightarrow}&
    \underset{\longrightarrow_{\mathrlap{V}}}{\lim}
    \;\;
    \left(
      \pi_0 
      \mathrm{Maps}^{\{0\}/}
      \left(
        S^V, S^V
      \right)^G
    \right)
    &=&
    \mathbb{S}_G(\ast)
    \\
    S &\mapsto& LD(S)
    \\
    \underset{
      \mathclap{
        \text{Burnside character}
      }
    }{
    \underbrace{
    \left(
      H \mapsto
      \left\vert 
        S^H
      \right\vert
    \right)
    }
    }
    &=&
    \underset{
      \mathclap{
        \text{degrees on fixed strata}
      }
    }{
      \underbrace{
      \left(
        H 
        \;\mapsto\;
        deg
        \left(
          S^{ dim\left( V^H\right) }
          \overset{\big(LD(S)\big)^H}{\longrightarrow}
          S^{ dim\left( V^H\right) }
        \right)
      \right)
      }
    }
  }
\]

For $G$ a [[compact Lie group]] this correspondence remains intact, with the relevant conditions on subgroups $H$ ([[closed subset|closed]] subgroups such that the [[Weyl group]] $W_G(H) \coloneqq N_G(H)/H$ is a [[finite group]]) and generalizing the [[Burnside marks]] to the [[Euler characteristic]] of [[fixed loci]].

=--

The statement is due to [Segal 71](#Segal71), a detailed proof making manifest the correspondence (eq:CorrespondenceOnMarksAndDegrees) is given by [tom Dieck 79, theorem 8.5.1](#tomDieck79). See also [tom Dieck-Petrie 78](#tomDieckPetrie78), [Lück 05, theorem 1.13](#Lueck05).

From a broader perspective of [[equivariant stable homotopy theory]], this statement is a special case of [[tom Dieck splitting]] of [[equivariant suspension spectra]] (e.g. [Schwede 15, theorem 6.14](#Schwede15)), see [there](tom+Dieck+splitting#OfFixedPointSpectraOfEquivariantSuspensionSpectra). 


## References

* {#Segal71} [[Graeme Segal]], _Equivariant stable homotopy theory_, In Actes du Congr&egrave;s International des Math &eacute;maticiens (Nice, 1970), Tome 2 , pages 59–63. Gauthier-Villars, Paris, 1971

* {#tomDieckPetrie78} [[Tammo tom Dieck]], T. Petrie,  _Geometric modules over the Burnside ring_, Invent. Math. 47 (1978) 273-287 ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/tomDieck-geometric.pdf))

* {#tomDieck79} [[Tammo tom Dieck]], _[[Transformation Groups and Representation Theory]]_, Springer 1979


* {#Lueck05} [[Wolfgang Lück]], _The Burnside Ring and Equivariant Stable Cohomotopy for Infinite Groups_ ([arXiv:math/0504051](https://arxiv.org/abs/math/0504051))

* {#Schwede15} [[Stefan Schwede]], section 6 of _[[Lectures on Equivariant Stable Homotopy Theory]]_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/equivariant.pdf))

