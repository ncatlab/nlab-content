
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A generalization of the [[Tietze extension theorem]] to [[equivariant functions]] provides conditions under which a [[continuous function|continuous]] and [[equivariant function]] from a [[subspace]] of a [[topological G-space]] to another [[topological G-space]] has an [[extension]] to a [[continuous function|continuous]] and [[equivariant function]] to the full $G$-space.

## Statement

+-- {: .num_theorem #TietzeGleasonExtensionTheorem}
###### Theorem
**(Tietze-Gleason extension theorem)

Let 

* $G$ be a [[compact Lie group]],

* $X$ a [[topological G-space]],

* $A \subset X^G \subset X$ a [[fixed point|G-fixed]] [[topological subspace]] of $X$,

* $E$ be a [[finite-dimensional vector space|finite-dimensional]] [[orthogonal group|orthogonal]] $G$-[[linear representation]], regarded as a [[Euclidean space|Euclidean]] [[topological G-space]],

* $A \overset{f}{\longrightarrow} E$ a $G$-[[equivariant function|equivariant]] [[continuous function]].

If 

* $A \subset X$ is a [[compact subspace]]

[[or]]

* $X$ is a [[normal topological space]] [[and]] $A \subset X$ is a [[closed subspace]] 

then $f$ has an [[extension]] to an [[equivariant function|equivariant]] [[continuous function]] $\widehat f$ on all of $X$.

$$
  \array{
    A &\overset{f}{\longrightarrow}& E
    \\
    \cap & \nearrow_{\mathrlap{ \widehat{f} }}
    \\
    X
  }
$$

=--

([Gleason 50](#Gleason50), see [Palais 60, Theorem 1.4.3](#Palais60))

Other/more general conditions for the equivariant extension to exist:

\begin{prop}\label{JaworowskiExtensionTheorem}
**(Jaworowski-extension theorem)** \linebreak

If

1. the ambient [[domain]] [[G-space]] $X$ is a

   1. [[locally compact topological space|locally comact]] 

   1. [[separable metric space]]

   1. of [[finite number|finite]] [[dimension of a separable metric space|dimension]]

   1. with a [[finite number]] of [[orbit type|orbit types]];

1. the [[domain]] $A \subset X^G \subset X$ is a

   * [[closed subspace]];
  
1. the [[codomain]] [[G-space]] is a

   1. [[locally compact topological space|locally comact]] 

   1. [[separable metric space]]

   1. such that for every $G$-[[orbit type]] $(H)$ in the [[complement]] $X \setminus A$ 

      the [[fixed locus]] $E^H$ is an [[absolute neighbourhood retract]].

Then every [[continuous function]] $f \colon A \to E$ has an [[extension]] to a $G$-[[equivariant function|equivariant]] [[continuous function]] $\widehat f$ on an [[open neighbourhood]] $A \subset O_A \subset X$

$$
  \left(
    \underset{ G/H \subset X \setminus A  }{\forall}
    \;
    E^H 
    \;\;
    \text{is absolute neighbourhood retract}
  \right)
  \;\;\;\;
    \Rightarrow
  \;\;\;\;
  \left(
    \underset{\widehat f}{\exists}
    \;\;\;\;
    \array{
      A &\overset{f}{\longrightarrow}& E
      \\
      \cap 
      & 
      \nearrow_{\mathrlap{ \widehat{f} }}
      \\
      O_A
      \\
      \cap
      \\
      X
     }
   \right)
   \,.
$$

Moreover, if the above [[fixed loci]] $E^H$ are even [[absolute retracts]], then an extension $\widehat f$ exists on all of $X$:

$$
  \left(
    \underset{ G/H \subset X \setminus A  }{\forall}
    \;
    E^H 
    \;\;
    \text{is absolute retract}
  \right)
  \;\;\;\;
    \Rightarrow
  \;\;\;\;
  \left(
    \underset{\widehat f}{\exists}
    \;\;\;\;
    \array{
      A &\overset{f}{\longrightarrow}& E
      \\
      \cap 
      & 
      \nearrow_{\mathrlap{ \widehat{f} }}
      \\
      X
     }
   \right)
   \,.
$$




\end{prop}

([Jaworowski 76](#Jaworowski76), [Lashof 81](#Lashof81))

## Related concepts

[[!include extension theorems -- table]]

## References
 {#References}

* {#Gleason50} [[Andrew Gleason]], _Spaces with a compact Lie group of transformations_,  Proc. Amer. Math. Soc. 1 (1950), 35-43 ([doi:10.1090/S0002-9939-1950-0033830-7](https://doi.org/10.1090/S0002-9939-1950-0033830-7))

* {#Palais60} [[Richard Palais]], Theorem 1.4.3 in: _The classification of $G$-spaces_, Memoirs of the American Mathematical Society, Number 36, 1960 ([pdf](http://vmm.math.uci.edu/PalaisPapers/ClassificationOfG-Spaces.pdf))

* {#Jaworowski73} [[Jan Jaworowski]], _Equivariant extensions of maps_, Pacific J. Math. Volume 45, Number 1 (1973), 229-244 ([euclid:1102947720](https://projecteuclid.org/euclid.pjm/1102947720))

* {#Jaworowski73b} [[Jan Jaworowski]], _Extending equivariant maps for compact Lie group actions_, Bull. Amer. Math. Soc. Volume 79, Number 4 (1973), 698-701 ([euclid:1183534741](https://projecteuclid.org/euclid.bams/1183534741))

* {#Jaworowski76} [[Jan Jaworowski]], _Extensions of $G$-maps and Euclidean $G$-retracts_, Math Z (1976) 146: 143 ([doi:10.1007/BF01187702](https://doi.org/10.1007/BF01187702))

* {#Jaworowski81} [[Jan Jaworowski]], _An equivariant extension theorem and $G$-retracts with a finite structure_, Manuscripta Math (1981) 35: 323 ([doi:10.1007/BF01263266](https://doi.org/10.1007/BF01263266))

* {#Lashof81} [[Richard Lashof]], _The Equivariant Extension Theorem_, Proceedings of the American Mathematical Society Vol. 83, No. 1 (Sep., 1981), pp. 138-140 ([jstor:2043909](https://www.jstor.org/stable/2043909))

[[!redirects equivariant Tietze extension theorems]]

[[!redirects Tietze-Gleason extension theorem]]
[[!redirects Tietze-Gleason extension theorems]]

[[!redirects equivariant extension theorem]]
[[!redirects equivariant extension theorems]]
