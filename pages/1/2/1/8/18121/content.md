
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Definition

The following terminology is used in [[topology]]:

+-- {: .num_defn #SubsetSaturated}
###### Definition
**(saturated subset)**

Let $f \;\colon\; X \longrightarrow Y$ be a [[function]] of [[sets]]. 
Then a [[subset]] $S \subset X$ is called an _$f$-[[saturated subset]]_ (or just _saturated subset_, if $f$ is understood)
if $S$ is the [[pre-image]] of its [[image]]:

$$
  \left(S \subset X \,\, f\text{-saturated} \right)
    \,\Leftrightarrow\,
  \left(
    S = f^{-1}(f(S))
  \right)
  \,.
$$

If $S$ is not necessarily $f$-saturated, then $f^{-f}(f(S))$ is called its _saturation_. Notice that $S \subset f^{-1}(f(S))$.

=--

## Properties

+-- {: .num_lemma #ComplementOfSaturatedSubsetIsSaturated}
###### Lemma

Let $f \colon X \longrightarrow Y$ be a [[function]]. Then a [[subset]] $S \subset X$
is $f$-saturated (def. \ref{SubsetSaturated}) precisely if its [[complement]]
$X \backslash S$ is so.

=--


+-- {: .num_prop #DetectViaSaturatedSubsetsContinuousQuotientMap}
###### Proposition

A [[continuous function]]

$$
  f \;\colon\; (X, \tau_X) \longrightarrow (Y,\tau_Y)
$$

whose underlying function $f \colon X \longrightarrow Y$ is [[surjective function|surjective]]
exhibits $\tau_Y$ as the corresponding [[quotient topological space|quotient topology]]
precisely if $f$ sends open and $f$-[[saturated subsets]] in $X$ (def. \ref{SubsetSaturated}) to open subsets of $Y$.
By lemma \ref{ComplementOfSaturatedSubsetIsSaturated} this is the case precisely if it sends
closed and $f$-saturated subsets to closed subsets.

=--

+-- {: .num_lemma #FindSatureatedOpenInsideOpenNeighbourhood}
###### Lemma

Let

1. $f \;\colon\; (X, \tau_X) \longrightarrow (Y, \tau_Y)$ be a [[closed map]].

1. $C \subset X$ be a [[closed subset]] which is $f$-[[saturated subset|saturated]];

1. $U \supset C$ an [[open subset]] containing $C$

then there exists a smaller open subset $V$ still containing $C$

$$
  U \supset V \supset C
$$

and such that $V$ is $f$-[[saturated subset|saturated]].

=--

+-- {: .proof}
###### Proof

We claim that

$$
  V \coloneqq X \backslash \left(  f^{-1}\left( f\left(  X \backslash U \right)  \right) \right)
$$

has the desired properties. To see this, observe first that

1. the [[complement]] $X \backslash U$ is closed, since $U$ is assumed to be open;

1. hence the image $f(X\backslash U)$ is closed, since $f$ is assumed to be a closed map;

1. hence the pre-image $f^{-1}\left( f\left(  X \backslash U \right)\right)$ is closed, since $f$ is continuous, therefore its complement $V$ is indeed open;

1. this pre-image $f^{-1}\left( f\left(  X \backslash U \right) \right)$ is saturated, as all pre-images clearly are, 
   and hence also its complement $V$ is saturated, by lemma \ref{ComplementOfSaturatedSubsetIsSaturated}. 

Therefore it now only remains to see that $U \supset V \supset C$.

The inclusion $U \supset V$ means equivalently that $f^{-1}\left( f\left(  X \backslash U \right)\right) \supset X \backslash U$,
which is clearly the case. 

The inclusion $V \supset C$ meas that $f^{-1}\left( f\left(  X \backslash U \right) \right) \,\cap \, C = \emptyset$.
Since $C$ is saturated by assumption, this means that $f^{-1}\left( f\left(  X \backslash U \right)\right) \,\cap \, f^{-1}(f(C)) = \emptyset$.
This in turn holds precisely if $f\left(  X \backslash U \right) \,\cap \, f(C)  = \emptyset$.
Since $C$ is saturated, this holds precisely if $X \backslash U \cap C = \emptyset$, and this is true by the assumption
that $U \supset C$.

=--

## Applications

* [[quotient projections out of compact Hausdorff spaces are closed precisely if the codomain is Hausdorff]]


[[!redirects saturated subset]]
[[!redirects saturated subsets]]
