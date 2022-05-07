
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[mathematics]], the term "configuration space" of a [[topological space]] $X$ typically refers by default to the topological space of pairwise distinct [[element|points]] in $X$, also called _[[Fadell's configuration space]]_, for emphasis.

In principle many other kinds of configurations and the spaces these form may be referred to by "configuration space", notably in [[physics]] the usage is in a broader sense, see at _[[configuration space (physics)]]_.


## Definition
  {#Definition}

Several variants of configuration spaces of points are of interest. They differ in whether

1. points are linearly ordered or not;

1. points are labeled in some labelling space;

1. points vanish on some subspace or if their labels are in some subspace.

Here are some of these variant definitions:

### Ordered unlabeled points

+-- {: .num_defn #OrderedUnlabeledConfigurations}
###### Definition
**(ordered unlabled configurations of a fixed number of points)**

Let $X$ be a [[closed manifold|closed]] [[smooth manifold]].
For $n \in \mathbb{N}$ write

$$
  \underset{ {}^{\{1,\cdots, n\}} }{ Conf }
  \big( 
    X
  \big)
  \;\coloneqq\;
  \big(
    X
  \big)^n
  \setminus
  \mathbf{\Delta}^n_X
$$

for the [[complement]] of the [[fat diagonal]] inside the $n$-fold [[Cartesian product]] of $X$ with itself.

This is the space of ordered but otherwise unlabeled configurations of $n$ points_ in $X$.

=--

\linebreak

### Unordered unlabeled points

+-- {: .num_defn #UnorderedUnlabeledConfigurations}
###### Definition
**(unordered unlabled configurations of a fixed number of points)**

Let $X$ be a [[closed manifold|closed]] [[smooth manifold]],
For $n \in \mathbb{N}$ write

\[
  \label{UnorderedUnlabelednPointConfigurationSpaces}
  \begin{aligned}
    Conf_n
    \big(
      X
    \big)
    &
    \coloneqq
    \;
    \Big(
      \underset{{}^{1,\cdots,n}}{Conf} 
      \big(
        X
      \big)
    \big) / Sym(n)
    \\
    &
    =\;
    \Big(
      \big(
        X
      \big)^n
      \setminus
      \mathbf{\Delta}^n_X
    \Big) / Sym(n)
  \end{aligned}
\]

for the [[quotient space]] of the ordered configuration space (Def. \ref{OrderedUnlabeledConfigurations}) by the evident [[action]] of the [[symmetric group]] $Sym(n)$ via [[permutation]] of the [[ordering]] of the points.

This is the space of unordered and unlabeled configurations of $n$ points_ in $X$.

We write

\[
  \label{UnorderedUnlabeledConfigurationSpace}
  Conf(X)
  \;\coloneqq\;
  \underset{n \in \mathbb{N}}{\sqcup}
  Conf_n\big( X\big)
\]

for the unordered unlabeled configuration space of any [[finite number]] of points, being the [[disjoint union]] of these spaces (eq:UnorderedUnlabelednPointConfigurationSpaces) over all [[natural numbers]] $n$.
 
=--


+-- {: .num_remark #MonoidStructureAndItsGroupCompletion}
###### Remark
**([[monoid]]-[[mathematical structure|structure]] on [[configuration space of points]])

For $X = \mathbb{R}^D$ a [[Euclidean spaces]] the configuration space of points $Conf\big( \mathbb{R}^D \big)$ (eq:UnorderedUnlabeledConfigurationSpace) carriesthe [[mathematical structure|structure]] of a [[topological monoid]] with product operation being the [[disjoint union]] of point configurations, after a suitable shrinking to put them next to each other ([Segal 73, p. 1-2](#Segal73)).

For emphasis, we write $B_{{}_{\sqcup}\!} Conf(\mathbb{R}^D)$ for the [[delooping]] ("[[classifying space]]") with respect to this [[topological monoid]]-[[structure]]. The corresponding [[based loop space]] is then the [[group completion]] of the configuration space, with respect to disjoint union of points:

\[
  \label{GroupCompletionOfConfigurationSpaceMonoid}
  Conf
  \big( 
    \mathbb{R}^D
  \big)
  \overset{\color{blue}\text{group completion}}{\longrightarrow}
  \Omega B_{{}_{\sqcup}\!} Conf(\mathbb{R}^D)
  \,.
\]

=--


+-- {: .num_remark }
###### Remark

The configuration space of unordered unlabeled configurations of $n$ points (Def. \ref{OrderedUnlabeledConfigurations}) is naturally a [[topological subspace]] of the [[space of finite subsets]] of [[cardinality]] $\leq n$

\[
  \label{InjectionOfUnorderedConfigurationSpaceOfPoints}
  Conf_n(X)
  \hookrightarrow
  \exp^n(X)
\]

=--

+-- {: .num_prop #UnorderedConfigurationSpaceInSpaceOfFiniteSubsets}
###### Proposition

Let $X$ be an [[inhabited set|non-empty]] [[regular topological space]] and $n \geq 2 \in \mathbb{N}$.

Then the injection (eq:InjectionOfUnorderedConfigurationSpaceOfPoints)

\[
  \label{UnorderedConfigurationSpaceOpenSubsetInQuotientOfSpacesOfFiniteSubsets}
  Conf_n(X)
  \hookrightarrow
  \exp^n(X)/\exp^{n-1}(X)
\]

of the [[unordered configuration space of n points]] of $X$ (Def. \ref{OrderedUnlabeledConfigurations}) into the [[quotient space]] of the [[space of finite subsets]] of cardinality $\leq n$ by its subspace of subsets of cardinality $\leq n-1$ is an [[open subspace]]-inclusion.

Moreover, if $X$ is [[compact topological space|compact]], then so is $\exp^n(X)/\exp^{n-1}(X)$ and the inclusion (eq:UnorderedConfigurationSpaceOpenSubsetInQuotientOfSpacesOfFiniteSubsets) exhibits the [[one-point compactification]] $\big(  Conf_n(X) \big)^{+} $ of the configuration space:

$$
  \big( 
    Conf_n(X)
  \big)^{+}
  \;\simeq\;
  \exp^n(X)/\exp^{n-1}(X)
  \,.
$$

=--

([Handel 00, Prop. 2.23](#Handel00), see also [Félix-Tanré 10](#FelixTanre10))


### Unordered labeled points
 {#UnorderedLabeledPoints}

+-- {: .num_defn #UnorderedLabeledFixedn}
###### Definition

For $X$ a [[smooth manifold]] and $k \in \mathbb{N}$, the space of _unordered configurations of points in $X$ with labels in $S^k$_ is

\[
  \label{UnorderedLabeledFixednCOnfigurationSpace}
  Conf_n\big(X, S^k \big)
  \;\coloneqq\;
  Conf_n\big(X\big) \underset{Sym(n)}{\times}
  \big(
    S^k 
  \big)^n
\]

=--

For $k \in \mathbb{N}$, consider the [[n-sphere|k-sphere]] as a [[pointed topological space]], with the base point regarded as the "vanishing label".

+-- {: .num_defn #UnorderedLabeledConfigurationsVanishingWithVanishingLabel}
###### Definition
**(unordered labeled configurations vanishing with vanishing label)**

For $X$ a [[smooth manifold]] and $k \in \mathbb{N}$, the space of _unordered configurations of points in $X$ with labels in $S^k$ and vanishing at vanishing label value_ is the [[quotient space]] 

\[
  \label{UnorderedLabeledCOnfigurationSpace}  
  Conf
  \big( 
    X,
    S^k
  \big)
  \;\coloneqq\;
  \Big(
    \underset{n \in \mathbb{N}}{\sqcup}
    Conf_n\big(X,S^k \big)
  \Big)/\sim
\]

of the [[disjoint union]] of all unordred labeled $n$-point configuration spaces (eq:UnorderedLabeledFixednCOnfigurationSpace) by the [[equivalence relation]] which regards points with vanishing label as absent. 

=--


<center>
<img src="https://ncatlab.org/nlab/files/UnorderedLabeledConfigurationOfPoints.jpg" width="700">
</center>

+-- {: .num_defn #ConfigurationSpacesOfnPoints}
###### Definition
**(unordered labeled configurations of a fixed number of points)**

Let $X$ be a [[manifold]], possibly with [[manifold with boundary|boundary]].
For $n \in \mathbb{N}$, the
 _**configuration space of $n$ unordered points** in $X$ disappearing at the boundary_ is the [[topological space]]
  $$
    \mathrm{Conf}_{n}(X)
    \;\coloneqq\;
    \Big(
      \big(
        X^n \setminus \mathbf{\Delta}_X^n
      \big)
      / \partial(X^n)
    \Big)
    /\Sigma(n)
    \,,
  $$
  where
  $\mathbf{\Delta}_X^n : = \{(x^i) \in X^n | \underset{i,j}{\exists} (x^i = x^j) \}$  is the [[fat diagonal]] in $X^n$
  and where $\Sigma(n)$ denotes the evident [[action]] of the [[symmetric group]] by [[permutation]] of factors of $X$ inside $X^n$.
  
  More generally, let $Y$ be another [[manifold]], possibly with [[manifold with boundary|boundary]]. For $n \in \mathbb{N}$, the _**configuration space of $n$ points** in $X \times Y$ vanishing at the boundary and distinct as points in $X$_ is the [[topological space]]
  $$
    \mathrm{Conf}_{n}(X,Y)
    \;\coloneqq\;
    \Big(
    \big(
      (
        X^n \setminus \mathbf{\Delta}_X^n
      )
      \times
      Y^n
    \big)
    /\Sigma(n)
    \Big)
    / \partial(X^n \times Y^n)
  $$
  where now $\Sigma(n)$ denotes the evident [[action]] of the [[symmetric group]] by [[permutation]] of factors of $X \times Y$ inside
  $X^n \times Y^n \simeq (X \times Y)^n$.
  
  This more general definition reduces to the previous case for $Y = \ast \coloneqq \mathbb{R}^0$ being the point:
  $$
    \mathrm{Conf}_n(X)
    \;=\;
    \mathrm{Conf}_n(X,\ast)
    \,.
  $$

Finally the _**configuration space of an arbitrary number of points** in $X \times Y$ vanishing at the boundary and distinct already as points of $X$_ is the [[quotient topological space]] of the [[disjoint union space]]

$$
  Conf\left( X, Y\right)
  \;\coloneqq\;
  \left(
  \underset{n \in \mathbb{n}}{\sqcup}
      \big(
      (
        X^n \setminus \mathbf{\Delta}_X^n
      )
      \times
      Y^k
    \big)
    /\Sigma(n)
  \right)/\sim
$$

by the [[equivalence relation]] $\sim$ given by

$$
  \big(
    (x_1, y_1), \cdots, (x_{n-1}, y_{n-1}), (x_n, y_n)
  \big)
  \;\sim\;
  \big(
    (x_1, y_1), \cdots, (x_{n-1}, y_{n-1})
  \big)
  \;\;\;\; \Leftrightarrow
  \;\;\;\; (x_n, y_n) \in \partial (X \times Y)
  \,.
$$
  
This is naturally a [[filtered topological space]] with filter stages

$$
  Conf_{\leq n}\left( X, Y\right)
  \;\coloneqq\;
  \left(
  \underset{k \in \{1, \cdots, n\}}{\sqcup}
      \big(
      (
        X^k \setminus \mathbf{\Delta}_X^k
      )
      \times
      Y^k
    \big)
    /\Sigma(k)
  \right)/\sim
  \,.
$$

The corresponding [[quotient topological spaces]] of the filter stages reproduces the above configuration spaces of a fixed number of points:

$$
  Conf_n(X,Y)
  \;\simeq\;
  Conf_{\leq n}(X,Y) / Conf_{\leq (n-1)}(X,Y)
  \,.
$$



=--



+-- {: .num_remark}
###### Remark
**(comparison to notation in the literature)**

The above Def. \ref{ConfigurationSpacesOfnPoints} is less general but possibly more suggestive than what is considered for instance in [Bödigheimer 87](#Boedigheimer87). Concretely, we have the following translations of notation:

  $$
    \array{
      \text{ here: }
        && 
      \array{ \text{ Segal 73,} \\ \text{ Snaith 74}: }
        &&
      \text{ Bödigheimer 87: }
      \\
      \\
      Conf(\mathbb{R}^d,Y) 
        &=& 
      C_d( Y/\partial Y )
        &=&
      C( \mathbb{R}^d, \emptyset; Y )  
      \\
      \mathrm{Conf}_n\left( \mathbb{R}^d \right)
      & = &
      F_n C_d( S^0 ) / F_{n-1} C_d( S^0 )
      & = &
      D_n\left( \mathbb{R}^d, \emptyset; S^0  \right)
      \\
      \mathrm{Conf}_n\left( \mathbb{R}^d, Y \right)
      & = &
      F_n C_d( Y/\partial Y ) / F_{n-1} C_d( Y/\partial Y )
      & = &
      D_n\left( \mathbb{R}^d, \emptyset; Y/\partial Y  \right)
      \\
      \mathrm{Conf}_n( X ) && &=& D_n\left( X, \partial X; S^0  \right) 
      \\
      \mathrm{Conf}_n( X, Y  ) && &=& D_n\left( X, \partial X; Y/\partial Y  \right)
    }
  $$
  Notice here that when $Y$ happens to have [[empty space|empty]] [[boundary]], $\partial Y = \emptyset$, then the [[pushout]] 

$$
  X / \partial Y \coloneqq Y \underset{\partial Y}{\sqcup} \ast
$$
 
is $Y$ with a [disjoint basepoint attached](pointed+topological+space#ForgettingAndAdjoiningBasepoints). Notably for $Y =\ast$ the [[point space]], we have that 

$$
  \ast/\partial \ast = S^0
$$

is the [[0-sphere]].


=--




A slight variation of the definition is sometimes useful:

+-- {: .num_defn #ConfigurationSpaceOfDisks}
###### Definition
**(configuration space of $dim(X)$-disks)**

In the situation of Def. \ref{ConfigurationSpaceOfParticleswithLabels}, with $X$ a [[manifold]] of [[dimension]] $dim(X) \in \mathbb{N}$

$$
  DiskConf(X,A)
  \longrightarrow
  Conf(X,A)
$$

be, on the left, the labeled configuration space of joint [[embedding of smooth manifolds|embeddings]] of [[tuples]]

$$
  \left(
    D^{dim(X)} 
      \overset{ \iota_i }{\hookrightarrow}
    X
  \right)
$$

of $dim(X)$-dimensional disks/[[closed balls]] into $X$, with identifications as in Def. \ref{ConfigurationSpaceOfParticleswithLabels} (in particular the disks centered at the basepoint are quotiented out) and with the comparison map sending each disk to its center.

This map is evidently a [[deformation retraction]] hence in particular a [[homotopy equivalence]].

=--


## Properties

### Ordered unlabeled configurations from unordered labeled configurations
 {#OrderedUnlabeledConfigurationsFromUnorderedLabeledConfigurations}

> under construction

(...)


<center>
<img src="https://ncatlab.org/nlab/files/OrderedUnlabeledFromUnorderedLabeledPoints.jpg" width="620">
</center>


(...)

### Cohomotopy charge map


The _Cohomotopy charge map_ is the [[function]] that assigns to a [[configuration space of points|configuration of points]] their total [[charge]] as measured in [[Cohomotopy]]-[[generalized cohomology|cohomology theory]].

This is alternatively known as the "electric field map" ([Salvatore 01](#Salvatore01) following [Segal 73, Section 1](#Segal73), see also [Knudsen 18, p. 49](#Knudsen18)) or the "scanning map" ([Kallel 98](#Kallel98)).


For $D \in \mathbb{N}$ the _Cohomotopy charge map_ is the  [[continuous function]]

\[
  \label{CohomotopyChargeMapOnEuclideanSpace}
  Conf\big( \mathbb{R}^D \big)
  \overset{cc}{\longrightarrow}
  \mathbf{\pi}^D
  \Big( 
    \big( \mathbb{R}^D \big)^{cpt}
  \Big)
  =
  Maps^{\ast/\!}\Big( \big(\mathbb{R}^D\big)^{cpt} , S^D\big)
  =
  \Omega^{D} S^D
\]

from the [[configuration space of points]] in the [[Euclidean space]] $\mathbb{R}^D$ to the $D$-[[Cohomotopy]] [[cocycle space]] [[vanishing at infinity]] on the [[Euclidean space]], which is equivalently the [[space of maps|space of pointed maps]] from the [[one-point compactification]] $S^D \simeq \big( \mathbb{R}^D \big)$ to itself, and hence equivalently the $D$-fold [[iterated based loop space]] of the [[n-sphere|D-sphere]]), which sends a configuration of points in $\mathbb{R}^D$, each regarded as carrying unit [[charge]] to their total [[charge]] as measured in  [[Cohomotopy]]-[[generalized cohomology|cohomology theory]] ([Segal 73, Section 3](#Segal73)).

The construction has evident generalizations to other manifolds than just Euclidean spaces, to spaces of labeled configurations and to [[equivariant Cohomotopy]]. The following graphics illustrates the Cohomotopy charge map on [[G-space]] [[tori]] for $G = \mathbb{Z}_2$ with values in $\mathbb{Z}_2$-[[equivariant Cohomotopy]]:

<center>
<a href="https://arxiv.org/pdf/1909.12277.pdf#page=24">
<img src="https://ncatlab.org/schreiber/files/EquivariantCohomotopyTadpoleCancellationN.jpg" width="700">
</a>
</center>

> graphics grabbed from [SS 19](Cohomotpy+charge+map#SatiSchreiber19)




#### Relation to iterated loop spaces of iterated suspensions
 {#LoopSpacesOfSuspensions}

In some situations the [[Cohomotopy charge map]] is a [[weak homotopy equivalence]] and hence exhibits, for all purposes of [[homotopy theory]], the [[Cohomotopy]] [[cocycle space]] of Cohomotopy charges as an equivalent reflection of the [[configuration space of points]]:


+-- {: .num_prop #GroupCompletionOfConfigurationSpaceIsIteratedBasedLoopSpace}
###### Proposition
**([[group completion]] on [[configuration space of points]] is [[iterated based loop space]])**

The [[Cohomotopy charge map]] (eq:CohomotopyChargeMapOnEuclideanSpace)

$$
  Conf
  \big(
    \mathbb{R}^D
  \big)
  \overset{
    cc
  }{\longrightarrow}
  \Omega^D S^D
$$

from the full unordered and unlabeled configuration space (eq:UnorderedUnlabeledConfigurationSpace) of [[Euclidean space]] $\mathbb{R}^D$  to the $D$-fold [[iterated based loop space]] of the [[n-sphere|D-sphere]], exhibits the [[group completion]] (eq:GroupCompletionOfConfigurationSpaceMonoid) of the configuration space monoid 

$$
  \Omega B_{{}_{\sqcup}\!} 
  Conf
  \big(
    \mathbb{R}^D
  \big)
  \overset{
    \simeq
  }{\longrightarrow}
  \Omega^D S^D
$$

=--

([Segal 73, Theorem 1](#Segal73))


+-- {: .num_prop #CohomotopyChargeMapIsEquivalenceOnSPhereLabeledConfihgurationSpace}
###### Proposition
**([[Cohomotopy charge map]] is [[weak homotopy equivalence]] on sphere-labeled [[configuration space of points]])**

For $D, k \in \mathbb{N}$ with $k \geq 1$, the [[Cohomotopy charge map]] (eq:CohomotopyChargeMapOnEuclideanSpace)

$$
  Conf
  \big(
    \mathbb{R}^D,
    S^k
  \big)
  \underoverset{\simeq}{\;\;cc\;\;}{\longrightarrow}
  \Omega^D S^{D + k}
  \;\simeq\;
  \mathbf{\pi}^{D+ k}\Big( \big( \mathbb{R}^{D}\big)^{cpt} \Big)
$$

is a [[weak homotopy equivalence]] 

* from the configuration space (eq:UnorderedLabeledCOnfigurationSpace) of unordered points with labels in $S^k$ and vanishing at the base point of the label space 

* to the $D$-fold [[iterated loop space]] of the [[n-sphere|D+k-sphere]]

hence equivalently

* to the [[cocycle space]] of [[Cohomotopy]] [[generalized cohomology theory|cohomology theory]] in degree $D + k$ [[vanishing at infinity]] on [[Euclidean space]] of [[dimension]] $D$.

=--

([Segal 73, Theorem 3](#Segal73))

This statement generalizes to [[equivariant homotopy theory]], with equivariant configurations carrying charge in [[equivariant Cohomotopy]]:

Let $G$ be a [[finite group]] and $V \in RO(G)$ an [[orthogonal group|orthogonal]] $G$-[[linear representation]], with its induced [[pointed topological space|pointed]] [[topological G-spaces]]:


1. the corresponding [[representation sphere]] $S^V \in G TopSpaces$, 

1. the corresponding [[Euclidean G-space]] $\mathbb{R}^V \in G TopSpaces$.


For $X \in G TopSpaces$ any [[pointed topological space|pointed]] [[topological G-space]], consider

1. the equivariant $V$-[[suspension]], given by the [[smash product]] with the $V$-[[representation sphere]]:

   $\Sigma^V X \;\coloneqq\; X \wedge S^V \;\in G TopSpaces\;$ 

1. the equivariant $V$-[[iterated based loop space]], given by the $G$-[[fixed point subspace]] inside the [[space of maps]] out of the [[representation sphere]]:

   $\Omega^V X \;\coloneqq\; Maps^{\ast/}\big( S^V, X\big)^G$.

+-- {: .num_defn #EquivariantUnorderedLabeledConfigurationsVanishingWithVanishingLabel}
###### Definition
**(equivariant unordered labeled configurations vanishing with vanishing label)**

Write

$$
  Conf\big( \mathbb{R}^V , X \big)^G
  \;\hookrightarrow\;
  Conf\big( \mathbb{R}^V , X \big)
$$

for the $G$-[[fixed point subspace]] in the unordered $X$-labelled configuration space of points (Def. \ref{UnorderedLabeledConfigurationsVanishingWithVanishingLabel}), with respect to the [[diagonal action]] on $\mathbb{R}^V \times X$.

=--

+-- {: .num_prop #EquivariantCohomotopyChargeMapEquivalence}
###### Proposition
**([[Cohomotopy charge map]]-equivalence for configurations on [[Euclidean G-spaces]])**

Let 

1. $G$ be a [[finite group]], 

1. $V$ an [[orthogonal group|orthogonal]] $G$-[[linear representation]] 

1.  $X$ a [[topological G-space]] 

If $X$ is $G$-connected, in that for all [[subgroups]] $H \subset G$ the $H$-[[fixed point subspace]] $X^H$ is a [[connected topological space]], then the [[Cohomotopy charge map]] 

$$
  Conf
  \big(
    \mathbb{R}^V,
    X
  \big)
  \underoverset{\simeq}{\;cc\;}{\longrightarrow}
  \Omega^V \Sigma^V X
  \phantom{AAA}
  \text{if X is G-connected}
$$

from the equivariant un-ordered $X$-labeled configuration space of points (Def. \ref{EquivariantUnorderedLabeledConfigurationsVanishingWithVanishingLabel}) in the corresponding [[Euclidean G-space]] to the based $V$-loop space of the $V$-suspension of $X$, is a [[weak homotopy equivalence]].

If $X$ is not necessarily $G$-connected, then this still holds for the [[group completion]] of the configuration space, under disjoint union of configurations


$$
  \Omega 
  B_{{}_{\sqcup}\!}
  Conf
  \big(
    \mathbb{R}^V,
    X
  \big)
  \underoverset{\simeq}{\;cc\;}{\longrightarrow}
  \Omega^{V+1} \Sigma^{V+1} X
  \,.
$$


=--

([Rourke-Sanderson 00, Theorem 1, Theorem 2](#RourkeSanderson00))


More generally:

+-- {: .num_prop #ScanningMapEquivalenceOverCartesianSpace}
###### Proposition
**([[iterated loop spaces]] equivalent to [[configuration spaces of points]])**


For 

1. $d \in \mathbb{N}$, $d \geq 1$ a [[natural number]] with $\mathbb{R}^d$ denoting the [[Cartesian space]]/[[Euclidean space]] of that [[dimension]],

1. $Y$ a [[manifold]], with [[inhabited set|non-empty]] [[manifold with boundary|boundary]] so that  $Y / \partial Y$ is [[connected topological space|connected]],

the [[Cohomotopy charge map]] constitutes a [[homotopy equivalence]]

$$
  Conf\left( 
    \mathbb{R}^D, Y
  \right)
  \overset{cc}{\longrightarrow}
  \Omega^D \Sigma^D (Y/\partial Y)
$$

between 

1. the configuration space of arbitrary points in $\mathbb{R}^d \times Y$ vanishing at the boundary (Def. \ref{ConfigurationSpacesOfnPoints}) 

1. the [[iterated loop space|d-fold loop space]] of the $d$-fold [[reduced suspension]] of the [[quotient space]] $Y / \partial Y$ (regarded as a [[pointed topological space]] with basepoint $[\partial Y]$).

In particular when $Y = \mathbb{D}^k$ is the [[closed ball]] of [[dimension]] $k \geq 1$ this gives a [[homotopy equivalence]]

$$
  Conf\left( 
    \mathbb{R}^D, \mathbb{D}^k
  \right)
  \overset{cc}{\longrightarrow}
  \Omega^D S^{ D + k }
$$

with the [[iterated loop space|d-fold loop space]] of the [[n-sphere|(d+k)-sphere]].

=--

([May 72, Theorem 2.7](#May72), [Segal 73, Theorem 3](#Segal73), see [Bödigheimer 87, Example 13](#Boedigheimer87))


+-- {: .num_prop #StableSplittingOfMappingSpacesOutOfEuclideanSpace}
###### Proposition
**([[stable splitting of mapping spaces]] out of [[Euclidean space]]/[[n-spheres]])**

For 

1. $d \in \mathbb{N}$, $d \geq 1$ a [[natural number]] with $\mathbb{R}^d$ denoting the [[Cartesian space]]/[[Euclidean space]] of that [[dimension]],

1. $Y$ a [[manifold]], with [[inhabited set|non-empty]] [[manifold with boundary|boundary]] so that  $Y / \partial Y$ is [[connected topological space|connected]],

there is a [[stable weak homotopy equivalence]]

$$
  \Sigma^\infty Conf(\mathbb{R}^d, Y)
  \overset{\simeq}{\longrightarrow}
  \underset{n \in \mathbb{N}}{\oplus} \Sigma^\infty Conf_n(\mathbb{R}^d, Y)
$$

between

1. the [[suspension spectrum]] of the [[configuration space of points|configuration space]] of an arbitrary number of points in $\mathbb{R}^d \times Y$ vanishing at the boundary and distinct already as points of $\mathbb{R}^d$ (Def. \ref{ConfigurationSpacesOfnPoints})

1. the [[direct sum]] (hence: [[wedge sum]]) of [[suspension spectra]] of the [[configuration space of points|configuration spaces]] of a fixed number of points in $\mathbb{R}^d \times Y$, vanishing at the boundary and distinct already as points in $\mathbb{R}^d$ (also Def. \ref{ConfigurationSpacesOfnPoints}).

Combined with the [[stabilization]] of the [[Cohomotopy charge map]] [[homotopy equivalence]] from Prop. \ref{ScanningMapEquivalenceOverCartesianSpace} this yields a [[stable weak homotopy equivalence]]

$$
  Maps_{cp}(\mathbb{R}^d, \Sigma^d (Y / \partial Y))
  =
  Maps^{\ast/}( S^d, \Sigma^d (Y / \partial Y))
  =
  \Omega^d \Sigma^d (Y/\partial Y)
  \underoverset{\Sigma^\infty cc}{\simeq}{\longrightarrow}
  \Sigma^\infty Conf(\mathbb{R}^d, Y)
  \overset{\simeq}{\longrightarrow}
  \underset{n \in \mathbb{N}}{\oplus} \Sigma^\infty Conf_n(\mathbb{R}^d, Y)
$$

between the latter direct sum and the [[suspension spectrum]] of the [[mapping space]] of pointed [[continuous functions]] from the [[n-sphere|d-sphere]] to the $d$-fold [[reduced suspension]] of $Y / \partial Y$.


=--

([Snaith 74, theorem 1.1](#Snaith74), [Bödigheimer 87, Example 2](#Boedigheimer87))

In fact by [Bödigheimer 87, Example 5](#Boedigheimer87) this equivalence still holds with $Y$ treated on the same footing as $\mathbb{R}^d$, hence with $Conf_n(\mathbb{R}^d, Y)$ on the right replaced by $Conf_n(\mathbb{R}^d \times Y)$ in the well-adjusted notation of Def. \ref{ConfigurationSpacesOfnPoints}:

$$
  Maps_{cp}(\mathbb{R}^d, \Sigma^d (Y / \partial Y))
  =
  Maps^{\ast/}( S^d, \Sigma^d (Y / \partial Y))
  \overset{\simeq}{\longrightarrow}
  \underset{n \in \mathbb{N}}{\oplus} \Sigma^\infty Conf_n(\mathbb{R}^d \times Y)
$$


#### Relation to classifying space of the symmetric group

Let $X= \mathbb{R}^\infty$. Then 

* the _unordered_ configuration space of $n$ points in $\mathbb{R}^\infty$ is a model for the [[classifying space]] $B \Sigma(n)$ of the [[symmetric group]] $\Sigma(n)$;

  (e.g. [Bödigheimer 87, Example 10](#Boedigheimer87))


* the _ordered_ configuration space of $n$ points, equipped with the canonical $\Sigma(n)$-[[action]], is a model for the $\Sigma(n)$-[[universal principal bundle]].


$\,$


#### Relation to James construction

The [[James construction]] of $X$ is [[homotopy equivalence|homotopy equivalent]] to the [[configuration space of points]] $C(\mathbb{R}^1, X)$ of points in the [[real line]] with labels taking values in $X$.

(e.g. [Bödigheimer 87, Example 9](#Boedigheimer87))

$\,$


#### In twisted Cohomotopy
 {#RelationToTwistedCohomotopy}

The May-Segal theorem \ref{ScanningMapEquivalenceOverCartesianSpace} generalizes from [[Euclidean space]] to [[closed manifold|closed]] [[smooth manifolds]] if at the same time one passes from plain [[Cohomotopy]] to [[twisted Cohomotopy]], twisted, via the [[J-homomorphism]], by the [[tangent bundle]]:

+-- {: .num_prop #ScanningMapEquivalenceOverClosedManifold}
###### Proposition

Let 

1. $X^n$ be a [[smooth manifold|smooth]] [[closed manifold]] of [[dimension]] $n$;

1. $1 \leq k \in \mathbb{N}$ a [[positive number|positive]] [[natural number]].

Then the [[Cohomotopy charge map]] constitutes a [[weak homotopy equivalence]]

$$
  \underset{
    \color{blue}
    { \phantom{a} \atop \text{ J-twisted Cohomotopy space}}
  }{
    Maps_{{}_{/B O(n)}}
    \Big(
      X^n 
      \;,\; 
      S^{
        \mathbf{n}_{def} + \mathbf{k}_{\mathrm{triv}}    
      }
      \!\sslash\!
      O(n)
    \Big)
  }
  \underoverset
  {\simeq}
  {
    \color{blue}
    \text{Cohomotopy charge map}
  }
  {\longleftarrow}
  \underset{
    \mathclap{
    \color{blue}
      {
        \phantom{a}
        \atop
        {
          \text{configuration space}
          \atop 
          \text{of points}
        }
      }
    }
  }{
    Conf
    \big(
      X^n,
      S^k
    \big)
  }
$$

between 

1. the [[J-homomorphism|J]]-[[twisted Cohomotopy|twisted (n+k)-Cohomotopy]] space of $X^n$, hence the [[space of sections]] of the $(n + k)$-[[spherical fibration]] over $X$ which is [[associated fiber bundle|associated]] via the [[tangent bundle]] by the [[O(n)]]-[[action]] on $S^{n+k} = S(\mathbb{R}^{n} \times \mathbb{R}^{k+1})$

1. the [[configuration space of points]] on $X^n$ with labels in $S^k$.

=--

([Bödigheimer 87, Prop. 2](#Boedigheimer87), following [McDuff 75](#McDuff75))

+-- {: .num_prop #ScanningMapEquivalenceOverClosedFramedManifold}
###### Remark

In the special case that the [[closed manifold]] $X^n$ in Prop. \ref{ScanningMapEquivalenceOverClosedManifold} is [[parallelizable manifold|parallelizable]], hence that its [[tangent bundle]] is [[trivial bundle|trivializable]], the statement of Prop. \ref{ScanningMapEquivalenceOverClosedManifold} reduces to this:

Let

1. $X^n$ be a [[parallelizable manifold|parallelizable]] [[closed manifold]] of [[dimension]] $n$;

1. $1 \leq k \in \mathbb{N}$ a [[positive number|positive]] [[natural number]].

Then the [[Cohomotopy charge map]] constitutes a [[weak homotopy equivalence]]

$$
  \underset{
    \color{blue}
    { \phantom{a} \atop \text{ Cohomotopy space}}
  }{
    Maps
    \Big(
      X^n 
      \;,\; 
      S^{
       n + k    
      }
    \Big)
  }
  \underoverset
  {\simeq}
  {
    \color{blue}
    \text{Cohomotopy charge map}
  }
  {\longleftarrow}
  \underset{
    \mathclap{
    \color{blue}
      {
        \phantom{a}
        \atop
        {
          \text{configuration space}
          \atop 
          \text{of points}
        }
      }
    }
  }{
    Conf
    \big(
      X^n,
      S^k
    \big)
  }
$$

between 

1. $(n+k)$-[[Cohomotopy]] space of $X^n$, hence the [[space of maps]] from $X$ to the [[n-sphere|(n+k)-sphere]]

1. the [[configuration space of points]] on $X^n$ with labels in $S^k$.

=--


### Knizhnik-Zamolodchicov connection

[[!include Knizhnik-Zamolodchikov-Kontsevich construction -- definition]]


### Action by little $n$-disk operad and by Goodwillie derivatives


Under some conditions and with suitable degrees/shifts,
configuration spaces of points canonically have the [[structure]] of [[algebras over an operad]] over the [[little n-disk operad]] and the [[Goodwillie derivatives of the identitity functor]].

For more see [there](Goodwillie+derivatives+of+the+identity+functor#Properties)



\linebreak


### Homology and stabilization in homology
 {#HomologyAndStabilization}

Let $X$ be a [[topological space]] which is the [[interior]] of a [[compact topological space|compact]] [[manifold with boundary]] $\overline{X}$. We may think of the [[boundary]] $\partial \overline X$ as consisting of the "points at infinity" in $X$. 

In particular, there are then inclusion maps

\[
  \label{InclusionOfUnorderedConfigurationSpaces}
  Conf_n
  \big(
    X
  \big)
  \overset{i_n}{\longrightarrow}
  Conf_{n+1}
  \big(
    X
  \big)
\]

of the unordered configuration space of $n$ points in $X$ (Def. \ref{UnorderedUnlabeledConfigurations}) into that of $n + 1$ points, 
formalizing the idea of "adding a point at infinity" to a configuration.
More formally, these maps are given by pushing configuration points away from the boundary a little and then adding a new point near to a point on the boundary of $X$.

([Randal-Williams 13, Section 4](#RandalWilliams13))

The [[homotopy class]] of these maps depends (just) on the [[connected component]] of the [[boundary]] $\partial \overline{X}$ at which one chooses to bring in the new point. But for any choice, they have the following effect on [[cycles]] in [[ordinary homology]]:

+-- {: .num_prop #HomologicalStabilizationForUnorderedConfigurationSpaces}
###### Proposition
**(homological stabilization for unordered configuration spaces)**

Let $X$ be 

* a [[connected topological space|connected]] [[smooth manifold]] 

* which is the [[interior]] of a [[compact topological space|compact]] [[manifold with boundary]] 

* of [[dimension]] $dim(X) \geq 2$.

Then for all $n \in \mathbb{N}$ the inclusion [[maps]] (eq:InclusionOfUnorderedConfigurationSpaces) are such that on [[ordinary homology]] with [[integer]] [[coefficients]] these maps induce [[split monomorphisms]] in all degrees, 

$$
  H_\bullet
  \big( 
    Conf_n(X)
    ,
    \mathbb{Z}
  \big)
  \overset{
    H_\bullet( i_n, \mathbb{Z} )
  }{\hookrightarrow}
  H_\bullet
  \big( 
    Conf_{n+1}(X)
    ,
    \mathbb{Z}
  \big)  
$$

and in degrees $\leq n/2$ these are even [[isomorphisms]]

$$
  H_p
  \big( 
    Conf_n(X)
    ,
    \mathbb{Z}
  \big)
  \underoverset{\simeq}{
    H_p( i_n, \mathbb{Z} )
  }{\hookrightarrow}
  H_p
  \big( 
    Conf_{n+1}(X)
    ,
    \mathbb{Z}
  \big)
  \phantom{AAAA}
  \text{for}
  \;
  p \leq n/2
  \,.
$$

Finally, for [[ordinary homology]] with [[rational number|rational]] [[coefficients]], these maps induce [[isomorphisms]] all the way up to degree $n$:


$$
  H_p
  \big( 
    Conf_n(X)
    ,
    \mathbb{Q}
  \big)
  \underoverset{\simeq}{
    H_p( i_n, \mathbb{Q} )
  }{\hookrightarrow}
  H_p
  \big( 
    Conf_{n+1}(X)
    ,
    \mathbb{Q}
  \big)
  \phantom{AAAA}
  \text{for}
  \;
  p \leq n
  \,.
$$

=--

([Randal-Williams 13, Theorem A and Threorem B](#RandalWilliams13))





\linebreak


### Rational homotopy type
 {#RationalHomotopyType}

We discuss aspects of the [[rational homotopy type]] of configuration spaces of points. See also at _[[graph complex]]_.


#### Rational cohomology
 {#Cohomology}


+-- {: .num_prop #RealCohomologyOfConfigurationSpaceOfOrderedPointsInEuclideanSpace}
###### Proposition
**([[real cohomology]] of configuration spaces of ordered points in [[Euclidean space]])**

The [[real cohomology|real]] [[cohomology ring]] of the configuration spaces $\underset{{}^{\{1,\cdots,n\}}}{Conf}\big( \mathbb{R}^D\big)$
(Def. \ref{OrderedUnlabeledConfigurations}) 
of $n$ ordered unlabeled points  in [[Euclidean space]] $\mathbb{R}^D$ 

is [[generators and relations|generated]] by elements in degree $D-1$

$$ 
  \omega_{i j}
  \;\;
  \in
  H^2
  \Big(
    \underset{
      {}^{\{1, \cdots, n\}}
    }{
      Conf
    }
    \big( 
      \mathbb{R}^D
    \big),
    \mathbb{R}
  \Big)
$$

for $i, j \in \{1, \cdots, n\}$

subject to these three [[generators and relations|relations]]:

1. **(anti-)symmetry)**

   $$\omega_{i j} = (-1)^D \omega_{j i} $$

1. **nilpotency**

   $$\omega_{i j} \wedge \omega_{i j} \;=\; 0$$

1. **3-term relation**

   $$
     \omega_{i j} 
       \wedge 
     \omega_{j k} 
       + 
     \omega_{j k}
       \wedge 
     \omega_{k i} 
       + 
     \omega_{k i} 
       \wedge 
     \omega_{i j} 
       = 
     0
   $$

Hence:

\[
  \label{RealCohomologyOfUnorderedConfigurationSpaceInEuclideanSpace}
  H^\bullet
  \Big(
    \underset{
      {}^{\{1,\cdots,n\}}
    }{Conf}
    \big( 
      \mathbb{R}^D 
    \big),
    \mathbb{R}
  \Big)
  \;\simeq\;
  \mathbb{R}\Big[ \big\{\omega_{i j} \big\}_{i, j \in \{1, \cdots, n\}} \Big]
  \Big/
  \left(
    \array{
      \omega_{i j} = (-1)^D \omega_{j i}
      \\
      \omega_{i j} \wedge \omega_{i j} = 0
      \\
      \omega_{i j} \wedge \omega_{j k} + \omega_{j k} \omega_{k i} + \omega_{k i} \wedge \omega_{i j} = 0    
     }
     \;\;
     \text{for}\;
     i,j \in \{1, \cdots, n\}
  \right)
\]

=--

This is due to [Cohen 76](#Cohen76), following  [Arnold 69](#Arnold69), [Cohen 73](#Cohen73). See also [Félix-Tanré 03, Section 2](#FelixTanre03)
[Lambrechts-Tourtchine 09, Section 3](#LambrechtsTourtchine09).

See also at _[[Fulton-MacPherson compactification]]_ the section _[de Rham cohomology](Fulton-MacPherson+operad#deRhamCohomology)_.



+-- {: .num_remark #RealCohomologyOfConfigurationSpaceInTermsOfGraphCohomology} 
###### Remark
**([[real cohomology]] of the configuration space in terms of [[graph cohomology]])**

In the [[graph complex]]-model for the [[rational homotopy type]] of the ordered unlabled [[configuration space of points]] 
$\underset{{}^{\{1,\cdots,n\}}}{Conf}\big( \mathbb{R}^D\big)$ the three relations in Prop. \ref{RealCohomologyOfConfigurationSpaceOfOrderedPointsInEuclideanSpace} are incarnated as follows:

1. a graph changes sign when one of its edges is reversed ([this Def.](graph+complex#SignRulesForGraphs))

1. a graph with [[parallel edges]] is a vanishing graph ([this Def.](graph+complex#VanishingGraphs))

1. the graph coboundary of a single trivalent internal vertex ([this Example](graph+complex#ThreeTermRelation)).

=--




\linebreak

#### Rational homotopy and Whitehead products
 {#RationalHomotopyGroups}

Write again

$$
  Conf_n\big( \mathbb{R}^D \big) 
  \;\coloneqq\;
  \big( \mathbb{R}^D \big)^n \setminus FatDiag
$$

for the configuration space of $n$ ordered points in [[Euclidean space]].

+-- {: .num_prop #RationalHomotopyOfConfigurationSpaceOfOrderedPointsInEuclideanSpace}
###### Proposition


The [[Whitehead product]] [[super Lie algebra]] of [[rationalization|rationalized]] [[homotopy groups]]

$$
  L^n
  \;\coloneqq\;
  \pi_{\bullet+1}\Big(  Conf_n\big( \mathbb{R}^D \big) \Big)
  \otimes_{\mathbb{Z}} \mathbb{Q}
$$

is [[generators and relations|generated]] from elements

$$
  \omega^{i j}
  \;\in\;
  \pi_2
  \Big(
    Conf_n\big( \mathbb{R}^D \big)  
  \Big)
  \otimes_{\mathbb{Z}} \mathbb{Q}
  \phantom{AAA}
  i \neq j \in \{1, \cdots, n\}
  \,,
$$

subject to the following [[generators and relations|relations]]:

1. $\omega^{i j} = (-1)^D \omega^{j i}$

1. $\big[ \omega^{i j}, \omega^{k l} \big]$ $\;\;\;$ if $i,j,k,l$ are pairwise distinct;

1. $\big[ \omega^{i j}, \omega^{j k} + \omega^{k i}  \big] = 0$.

=--


This is due to [Kohno 02](#Kohno02). See also [Lambrechts-Tourtchine 09, Section 3](#LambrechtsTourtchine09).

\linebreak


### Relation weight systems, chord diagrams and Vassiliev invariants

[[weight systems are cohomology of loop space of configuration space]]:

+-- {: .num_prop}
###### Proposition
**(integral [[horizontal weight systems]] are [[integral cohomology]] of [[based loop space]] of [[ordered configuration space of points]] in [[Euclidean space]])**

For [[ground ring]] $R = \mathbb{Z}$ the [[integers]], there is, for each [[natural number]] $n$, a canonical [[isomorphism]] of [[graded abelian groups]] between 

1. the integral [[weight systems]]

   $$
     \mathcal{W}^{pb}_n  
     \;\coloneqq\;
     Hom_{\mathbb{Z} Mod}
     \big(
       \underset{
         \mathcal{A}^{pb}_n
       }{
         \underbrace{
           \mathbb{Z}
           \langle 
             \mathcal{D}^{pb}_n 
           \rangle
           /(2T,4T)
         } 
       }
       ,
       \mathbb{Z}
     \big)
   $$

   on [[horizontal chord diagrams]] of $n$ strands (elements of the set $\mathcal{D}^{pb}$)

1. the [[integral cohomology]] of the [[based loop space]] of the [[ordered configuration space of n points]] in 3d [[Euclidean space]]:

$$
  H \mathbb{Z}^\bullet
  \big(
    \Omega 
    \underset{
      {}^{\{1,\cdots,n\}}
    }{Conf}
    (\mathbb{R}^3)
  \big)
  \;\simeq\;
  (\mathcal{W}^{pb}_n)^\bullet
  \;\simeq\;
  Gr^\bullet( \mathcal{V}^{pb}_n )
  \,.
$$

(the second equivalence on the right is the fact that [[weight systems are associated graded of Vassiliev invariants]]).

=--

This is stated as [Kohno 02, Theorem 4.1](#Kohno02)

+-- {: .num_prop}
###### Proposition
**([[weight systems]] are inside [[real cohomology]] of [[based loop space]] of [[ordered configuration space of points]] in [[Euclidean space]])**

For [[ground field]] $k = \mathbb{R}$ the [[real numbers]], 
there is a canonical [[injection]] of the [[real vector space]] $\mathcal{W}$ of [[framed weight systems]] ([here](weight+system#eq:SpaceOfWeightSystemsAsLinearDual)) into the [[real cohomology]] of the [[based loop spaces]] of the ordered [[configuration spaces of points]] in 3-[[dimension|dimensional]] [[Euclidean space]]:

$$
  \mathcal{W}
  \;\overset{\;\;\;\;}{\hookrightarrow}\;
  H\mathbb{R}^\bullet
  \Big(
    \underset{n \in \mathbb{N}}{\sqcup}
    \Omega 
    \underset{{}^{\{1,\cdots,n\}}}{Conf}
    \big(
      \mathbb{R}^3 
    \big)
  \Big)
$$

=--

This is stated as [Kohno 02, Theorem 4.2](#Kohno02)

[[!include chord diagrams and weight systems -- table]]




\linebreak

## Occurrences and Applications 
  {#OccurrencesAndApplications}

### Compactification

The [[Fulton-MacPherson compactification]] of configuration spaces of points in $\mathbb{R}^d$ serves to exhibit them as models for the [[little n-disk operad]]. 

### Stable splitting of mapping spaces

The [[stable splitting of mapping spaces]] says that [[suspension spectra]] of suitable [[mapping spaces]] are equivalently [[wedge sums]] of [[suspension spectra]] of configuration spaces of points.

### Correlators as differential forms on configuration spaces

In [[Euclidean field theory]] the [[correlators]] are often regarded as [[distributions of several variables]] with [[singularities]] on the [[fat diagonal]]. Hence they become [[non-singular distributions]] after [[restriction of distributions]] to the corresponding configuration space of points. 

For more on this see at _[[correlators as differential forms on configuration spaces of points]]_.

## Related concepts

* [[Hilbert scheme]]

## References

### General 

General accounts:

* [[Edward Fadell]], [[Lee Neuwirth]], _Configuration spaces_, Math. Scand. __10__ (1962) 111-118, [MR141126](http://www.ams.org/mathscinet-getitem?mr=141126), [pdf](http://www.mscand.dk/article.php?id=1623)

* [[Edward Fadell]], [[Sufian Husseini]], _Geometry and topology of configuration spaces_, Springer Monographs in Mathematics (2001)  ([MR2002k:55038](http://www.ams.org/mathscinet-getitem?mr=2002k:55038), [doi:10.1007/978-3-642-56446-8]([doi:10.1007/978-3-642-56446-8](https://link.springer.com/book/10.1007/978-3-642-56446-8)) xvi+313 

* [[Craig Westerland]], _Configuration spaces in geometry and topology_, 2011 ([pdf](https://www.austms.org.au/Publ/Gazette/2011/Nov11/TechPaperWesterland.pdf))

  (in [[geometry]] and [[topology]])

* {#Knudsen18} [[Ben Knudsen]], _Configuration spaces in algebraic topology_ ([arXiv:1803.11165](https://arxiv.org/abs/1803.11165))

  (in [[algebraic topology]])

* Lucas Williams, *Configuration Spaces for the Working Undergraduate*,  Rose-Hulman Undergraduate Mathematics Journal: Vol. 21 : Iss. 1 , Article 8. ([arXiv:1911.11186](https://arxiv.org/abs/1911.11186), [rhumj:vol21/iss1/8]( https://scholar.rose-hulman.edu/rhumj/vol21/iss1/8))


In relation to the [[space of finite subsets]]:

* {#Handel00} David Handel, _Some Homotopy Properties of Spaces of Finite Subsets of Topological Spaces_, Houston Journal of Mathematics, Electronic Edition Vol. 26, No. 4, 2000 (<a href="https://www.math.uh.edu/~hjm/pdf26(4)/08handel.pdf">pdf</a>[hjm:Vol26-4](https://www.math.uh.edu/~hjm/Vol26-4.html))

* {#FelixTanre2010} [[Yves Félix]], [[Daniel Tanré]] _Rational homotopy of symmetric products and Spaces of finite subsets_, Contemp. Math 519 (2010): 77-92 ([pdf](http://tanre.org/Pro/Articles_files/SpnFiniteDef.pdf))


The [[algebra over an operad|algebra]]-[[structure]] of configuration spaces over [[little n-disk operads]]/[[Fulton-MacPherson operads]]:

* {#Markl99} [[Martin Markl]], _A compactification  of  the  real  configuration  space  as  an  operadic completion, J. Algebra 215 (1999), no. 1, 185–204


### Cohomotopy charge map
 {#ReferencesCohomotopyChargeMap}

The [[Cohomotopy charge map]] ("electric field map", "scanning map") and hence the relation of configuration spaces to [[Cohomotopy]] goes back to 

* {#May72} [[Peter May]], _The geometry of iterated loop spaces_, Springer 1972 ([pdf](https://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf))

* {#Segal73} [[Graeme Segal]], _Configuration-spaces and iterated loop-spaces_, Invent. Math. __21__ (1973), 213&#8211;221. MR 0331377 ([pdf](http://dodo.pdmi.ras.ru/~topology/books/segal.pdf))
c
Generalization of these constructions and results is due to

* {#McDuff75} [[Dusa McDuff]], _Configuration spaces of positive and negative particles_, Topology Volume 14, Issue 1, March 1975, Pages 91-107 (<a href="https://doi.org/10.1016/0040-9383(75)90038-5">doi:10.1016/0040-9383(75)90038-5</a>)

* {#Boedigheimer87} [[Carl-Friedrich Bödigheimer]], _Stable splittings of mapping spaces_, Algebraic topology. Springer 1987. 174-187 ([pdf](http://www.math.uni-bonn.de/~cfb/PUBLICATIONS/stable-splittings-of-mapping-spaces.pdf), [[BoedigheimerStableSplittings87.pdf:file]])

* {#ManthorpeTillmann} Richard Manthorpe, [[Ulrike Tillmann]], _Tubular configurations: equivariant scanning and splitting_, Journal of the London Mathematical Society, Volume 90, Issue 3 ([arxiv:1307.5669](https://arxiv.org/abs/1307.5669), [doi:10.1112/jlms/jdu050](https://doi.org/10.1112/jlms/jdu050))


Generalization to [[equivariant homotopy theory]]:

* {#RourkeSanderson00} [[Colin Rourke]], [[Brian Sanderson]], _Equivariant Configuration Spaces_, J. London Math. Soc. 62 (2000) 544-552 ([arXiv:math/9712216](https://arxiv.org/abs/math/9712216))


The relevant construction for the [[group completion]] of the configuration space

* [Segal 73, Theorem 1](#Segal73)


* {#Salvatore99} [[Paolo Salvatore]], _Configuration spaces with summable labels_, In: Aguadé J., Broto C., [[Carles Casacuberta]]  (eds.) _Cohomological Methods in Homotopy Theory_. Progress in Mathematics, vol 196. Birkhäuser, Basel, 2001 ([arXiv:math/9907073](https://arxiv.org/abs/math/9907073))

and from the point of view of [[cobordism categories]]:


* [[Oscar Randal-Williams]], section 10 of: _Embedded Cobordism Categories and Spaces of Manifolds_, 	Int. Math. Res. Not. IMRN 2011, no. 3, 572-608 ([arXiv:0912.2505](https://arxiv.org/abs/0912.2505))

On the [[homotopy type]] of the [[space of maps|space of]] [[rational functions]] from the [[Riemann sphere]] to itself (related to the [[moduli space of monopoles]] in $\mathbb{R}^3$ and to the [[configuration space of points]] in $\mathbb{R}^2$):

* [[Graeme Segal]], _The topology of spaces of rational functions_, Acta Math. Volume 143 (1979), 39-72 ([euclid:1485890033](https://projecteuclid.org/euclid.acta/1485890033))


See also

* {#Kallel98} [[Sadok Kallel]], _Spaces of particles on manifolds and Generalized Poincaré Dualities_, The Quarterly Journal of Mathematics, Volume 52, Issue 1, 1 March 2001 ([doi:10.1093/qjmath/52.1.45](https://doi.org/10.1093/qjmath/52.1.45)) 


* Shingo Okuyama, Kazuhisa Shimakawa, _Interactions of strings and equivariant homology theories_, ([arXiv:0903.4667](https://arxiv.org/abs/0903.4667))

For relation to [[instantons]] via [[topological Yang-Mills theory]]:

* {#AtiyahJones78} [[Michael Atiyah]], [[John David Stuart Jones]], _Topological aspects of Yang-Mills theory_, Comm. Math. Phys. Volume 61, Number 2 (1978), 97-118 ([arXiv:1103904210](https://projecteuclid.org/euclid.cmp/1103904210))

In speculation regarding [[Galois theory]] over the [[sphere spectrum]]:

* {#MoravaBeardsly17} [[Jack Morava]], [[Jonathan Beardsley]], _Toward a Galois theory of the integers over the sphere spectrum_,  Journal of Geometry and Physics Volume 131, September 2018, Pages 41-51 ([arXiv:1710.05992](https://arxiv.org/abs/1710.05992))






### Stable splitting of mapping spaces

The appearance of configuration spaces as summands in [[stable splittings of mapping spaces]] is originally due to

* {#Snaith74} [[Victor Snaith]],  _A stable decomposition of $\Omega^n S^n X$_, Journal of the London Mathematical Society 7 (1974), 577 - 583 ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/snaiths.pdf))

An alternative proof is due to 

* {#Cohen80} [[Ralph Cohen]], _Stable proof of stable splittings_, Math. Proc. Camb. Phil. Soc., 1980, 88, 149 ([doi:10.1017/S030500410005742X](https://doi.org/10.1017/S030500410005742X), [pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/247D9F951F8AB99000E4FF6CB2DB9EA2/S030500410005742Xa.pdf/div-class-title-stable-proofs-of-stable-splittings-div.pdf))

Review and generalization is in 

* [Boedigheimer 87](#Boedigheimer87)

and the relation to the [[Goodwillie-Taylor tower]] of mapping spaces is pointed out in 

* [Arone 99](#Arone99)



### In Goodwillie-calculus
 {#ReferencesInGoodwillieCalculus}

The configuration spaces of a space $X$ appear as the [[Goodwillie derivatives]] of its [[mapping space]]/[[nonabelian cohomology]]-[[functor]] $Maps(X,-)$:


* {#Arone99} [[Greg Arone]], _A generalization of Snaith-type filtration_, Transactions of the American Mathematical Society 351.3 (1999): 1123-1150. ([pdf](https://www.ams.org/journals/tran/1999-351-03/S0002-9947-99-02405-8/S0002-9947-99-02405-8.pdf))

* {#Ching05} [[Michael Ching]], _Calculus of Functors and Configuration Spaces_, Conference on Pure and Applied Topology Isle of Skye, Scotland, 21-25 June, 2005 ([pdf](https://www3.amherst.edu/~mching/Work/skye.pdf))


### Compactification
 {#ReferencesCompactification}

A [[compactification]] of configuration spaces of points was introduced in 

* [[William Fulton]], [[Robert MacPherson]], _A compactification of configuration spaces_, Ann. of Math. (2), 139(1):183–225, 1994.

and an [[operad]]-[[structure]] defined on it ([[Fulton-MacPherson operad]]) in 

* [[Ezra Getzler]], [[John Jones]], _Operads, homotopy algebra and iterated integrals for double loop spaces_ ([arXiv:hep-th/9403055](https://arxiv.org/abs/hep-th/9403055))

Review includes

* {#LambrechtsVolic14} [[Pascal Lambrechts]], [[Ismar Volić]], section 5 of _Formality of the little $N$-disks operad_, Memoirs of the American Mathematical Society ; no. 1079, 2014  ([arXiv"0808.0457](https://arxiv.org/abs/0808.0457), [doi:10.1090/memo/1079](http://dx.doi.org/10.1090/memo/1079))

This underlies the models of configuration spaces by [[graph complexes]], see there for more.



### Homology and cohomology 
 {#ReferencesCohomology}

General discussion of [[ordinary homology]]/[[ordinary cohomology]] of configuration spaces of points:

* {#Arnold69} [[Vladimir Arnold]], _The cohomology ring of the colored braid group_, Mat. Zametki, 1969, Volume 5, Issue 2, Pages 227–231 ([mathnet:mz6827](http://mi.mathnet.ru/eng/mz6827))

* {#Cohen73} [[Fred Cohen]], _Cohomology of braid spaces_, Bull. Amer. Math. Soc. Volume 79, Number 4 (1973), 763-766 ([euclid:1183534761](https://projecteuclid.org/euclid.bams/1183534761))

* {#Cohen76} [[Fred Cohen]], _The homology of $C_{n+1}$-Spaces, $n \geq 0$_, In: _The Homology of Iterated Loop Spaces_, Lecture Notes in Mathematics, vol 533. Springer 1976 ([doi:10.1007/BFb0080467](https://doi.org/10.1007/BFb0080467))


* [[Carl-Friedrich Bödigheimer]], [[Fred Cohen]], L. Taylor, _On the homology of configuration spaces_, Topology Vol. 28 No. 1, p. 111-123 1989 ([pdf](https://core.ac.uk/download/pdf/82124359.pdf))


* E. Ossa, _On the cohomology of configuration spaces_, In: Broto C., [[Carles Casacuberta]], Mislin G. (eds.), _Algebraic Topology: New Trends in Localization and Periodicity_,  Progress in Mathematics, vol 136. Birkhäuser Basel (1996) ([doi:10.1007/978-3-0348-9018-2_26](https://doi.org/10.1007/978-3-0348-9018-2_26))



* [[Yves Félix]], [[Jean-Claude Thomas]], _Rational Betti numbers of configuration spaces_, Topology and its Applications, Volume 102, Issue 2, 8 April 2000, Pages 139-149 (<a href="https://doi.org/10.1016/S0166-8641(98)00148-5">doi:10.1016/S0166-8641(98)00148-5</a>)

* {#RandalWilliams13} [[Oscar Randal-Williams]], _Homological stability for unordered configuration spaces_, The Quarterly Journal of Mathematics, Volume 64, Issue 1, March 2013, Pages 303–326 ([arXiv:1105.5257](https://arxiv.org/abs/1105.5257))

* {#FelixTanre03} [[Yves Félix]], [[Daniel Tanré]], _The cohomology algebra of unordered configuration spaces_, Journal of the LMS, Vol 72, Issue 2 ([arxiv:math/0311323](https://arxiv.org/abs/math/0311323), [doi:10.1112/S0024610705006794](https://doi.org/10.1112/S0024610705006794))


* Thomas Church, _Homological stability for configuration spaces of manifolds_ ([arxiv:1602.04748](https://arxiv.org/abs/1602.04748))



* [[Ben Knudsen]], _Betti numbers and stability for configuration spaces via factorization homology_, Algebr. Geom. Topol. 17 (2017) 3137-3187 ([arXiv:1405.6696](https://arxiv.org/abs/1405.6696))

* Christoph Schiessl, _Betti numbers of unordered configuration spaces of the torus_ ([arxiv:1602.04748](https://arxiv.org/abs/1602.04748))

* Christoph Schiessl, _Integral cohomology of configuration spaces of the sphere_ ([arxiv:1801.04273](https://arxiv.org/abs/1801.04273))

* Dan Petersen, _Cohomology of generalized configuration spaces_ ([arXiv:1807.07293](https://arxiv.org/abs/1807.07293))

* Roberto Pagaria, _The cohomology rings of the unordered configuration spaces of the torus_, Algebr. Geom. Topol. 20 (2020) 2995–3012 ([doi:10.2140/agt.2020.20.2995](https://www.doi.org/10.2140/agt.2020.20.2995))

Expressing the [[rational cohomology]] of [[ordered configuration spaces of points]] via [[factorization homology]] and [[Ran spaces]]:

* Quoc P. Ho, _Higher representation stability for ordered configuration spaces and twisted commutative factorization algebras_ ([arXiv:2004.00252](https://arxiv.org/abs/2004.00252))


### Homotopy

Discussion of [[homotopy groups]] of configuration spaces:

* [Kohno 02](#Kohno02)

* {#LambrechtsTourtchine09} [[Pascal Lambrechts]], [[Victor Tourtchine]], _Homotopy graph-complex for configuration and knot spaces_, Transactions of the AMS, Volume 361, Number 1, January 2009, Pages 207–222 ([arxiv:math/0611766](https://arxiv.org/abs/math/0611766))

* [[Sadok Kallel]], Ines Saihi, _Homotopy Groups of Diagonal Complements_, Algebr. Geom. Topol. 16 (2016) 2949-2980 ([arXiv:1306.6272](https://arxiv.org/abs/1306.6272))


### Rational homotopy type

Discussion of the [[rational homotopy type]]:

* [[Igor Kriz]], _On the Rational Homotopy Type of Configuration Spaces_, Annals of Mathematics
Second Series, Vol. 139, No. 2 (Mar., 1994), pp. 227-237 ([jstor:2946581](https://www.jstor.org/stable/2946581))



### Cohomology modeled by graph complexes

That the [[de Rham cohomology]] of (the [[Fulton-MacPherson compactification]] of) configuration spaces of points may be modeled by [[graph complexes]] (exhibiting [[formality of the little n-disk operad]]) is due to

* {#Kontsevich99b} [[Maxim Kontsevich]], around Def. 15 and Lemma 3 in _Operads and Motives in Deformation Quantization_, Lett.Math.Phys.48:35-72,1999 ([arXiv:math/9904055](https://arxiv.org/abs/math/9904055))

nicely reviewed in [Lambrechts-Volic 14](#LambrechtsVolic14)


Further discussion of the graph complex as a model for the [[de Rham cohomology]] of  [[configuration spaces of points]] is in

* Najib Idrissi, _The Lambrechts-Stanley Model of Configuration Spaces_, Invent. Math, 2018 ([arXiv:1608.08054](https://arxiv.org/abs/1608.08054), [doi:10.1007/s00222-018-0842-9](https://dx.doi.org/10.1007/s00222-018-0842-9))

* {#CamposWillwacher16} [[Ricardo Campos]], [[Thomas Willwacher]], _A model for configuration spaces of points_ ([arXiv:1604.02043](https://arxiv.org/abs/1604.02043))

* [[Ricardo Campos]], Najib Idrissi, [[Pascal Lambrechts]], [[Thomas Willwacher]], _Configuration Spaces of Manifolds with Boundary_ ([arXiv:1802.00716](https://arxiv.org/abs/1802.00716))

* [[Ricardo Campos]], Julien Ducoulombier, Najib Idrissi, [[Thomas Willwacher]], _A model for framed configuration spaces of points_ ([arXiv:1807.08319](https://arxiv.org/abs/1807.08319))


### Loop spaces of configuration spaces of points
 {#ReferencesLoopSpacesOfConfigurationSpaces}

On [[loop spaces]] of [[configuration spaces of points]]:


* [[Edward Fadell]], [[Sufian Husseini]], _The space of loops on configuration spaces and the Majer-Terracini index_, Topol. Methods Nonlinear Anal. Volume 11, Number 2 (1998), 249-271 ([euclid:tmna/1476842829](https://projecteuclid.org/euclid.tmna/1476842829))

Specifically on [[ordinary homology]]/[[ordinary cohomology]] of [[based loop spaces]] of [[configuration spaces of points]] and the relation to [[weight systems]]/[[Vassiliev invariants]]:

* {#Kohno94} [[Toshitake Kohno]], _Vassiliev invariants and de Rham complex on the space of knots_, 
In: Yoshiaki Maeda, Hideki Omori, [[Alan Weinstein]] (eds.), _Symplectic Geometry and Quantization_, Contemporary Mathematics 179 (1994): 123-123 ([doi:10.1090/conm/179](http://dx.doi.org/10.1090/conm/179))


* {#CohenGitler01} [[Fred Cohen]], [[Samuel Gitler]], _Loop spaces of configuration spaces, braid-like groups, and knots_, In: Jaume Aguadé, Carles Broto, [[Carles Casacuberta]]  (eds.) _Cohomological Methods in Homotopy Theory_. Progress in Mathematics, vol 196. Birkhäuser, Basel 2001 ([doi:10.1007/978-3-0348-8312-2_7](https://doi.org/10.1007/978-3-0348-8312-2_7))

* {#Kohno02} [[Toshitake Kohno]], _Loop spaces of configuration spaces and finite type invariants_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arXiv:math/0211056](https://arxiv.org/abs/math/0211056))

* [[Fred Cohen]], [[Samuel Gitler]], _On loop spaces of configuration spaces_, Trans. Amer. Math. Soc. __354__ (2002), no. 5, 1705&#8211;1748, ([jstor:2693715](https://www.jstor.org/stable/2693715), [MR2002m:55020](http://www.ams.org/mathscinet-getitem?mr=1881013))

### In quantum field theory

In [[quantum field theory]] one may formalize [[correlators as differential forms on configuration spaces of points]].

This perspective was originally considered specifically for [[Chern-Simons theory]] in 

* {#AxelrodSinger93} [[Scott Axelrod]], [[Isadore Singer]],  _Chern--Simons Perturbation Theory II_, J. Diff. Geom. 39 (1994) 173-213 ([arXiv:hep-th/9304087](http://arxiv.org/abs/hep-th/9304087)) 

which was re-amplified  in 

* {#BottCattaneo97} [[Raoul Bott]], [[Alberto Cattaneo]], Remark 3.6 in _Integral invariants of 3-manifolds_, J. Diff. Geom., 48 (1998) 91-133 ([arXiv:dg-ga/9710001](https://arxiv.org/abs/dg-ga/9710001))

* {#CattaneoMnev10} [[Alberto Cattaneo]], [[Pavel Mnev]], Remark 11 in _Remarks on Chern-Simons invariants_, Commun.Math.Phys.293:803-836,2010 ([arXiv:0811.2045](https://arxiv.org/abs/0811.2045))

* [[Alberto Cattaneo]], [[Pavel Mnev]], [[Nicolai Reshetikhin]], appendix B of _Perturbative quantum gauge theories on manifolds with boundary_, Communications in Mathematical Physics, January 2018, Volume 357, Issue 2, pp 631–730  ([arXiv:1507.01221](https://arxiv.org/abs/1507.01221), [doi:10.1007/s00220-017-3031-6](https://doi.org/10.1007/s00220-017-3031-6))

and highlighted as a means to obtain [[graph complex]]-models for the [[de Rham cohomology]] of [[configuration spaces of points]] in 


* {#Kontsevich93} [[Maxim Kontsevich]], _Vassiliev's knot invariants_, Advances in Soviet Mathematics, Volume 16, Part 2, 1993 ([pdf](http://pagesperso.ihes.fr/~maxim/TEXTS/VassilievKnot.pdf))

* {#Kontsevich94} [[Maxim Kontsevich]], pages 11-12 of _Feynman diagrams and low-dimensional topology_, First European Congress of Mathematics, 1992, Paris, vol. II, Progress in Mathematics __120__, Birkh&#228;user (1994), 97&#8211;121 ([pdf](http://www.ihes.fr/~maxim/TEXTS/Feynman%20%20diagrams%20and%20low-dimensional%20topology.pdf))


with full details and proofs in

* {#LambrechtsVolic14} [[Pascal Lambrechts]], [[Ismar Volić]], sections 6 and 7 of _Formality of the little N-disks operad_, Memoirs of the American Mathematical Society no. 1079, 2014  ([arxiv:0808.0457](https://arxiv.org/abs/0808.0457), [doi:10.1090/memo/1079](http://dx.doi.org/10.1090/memo/1079))

see also

* {#CamposIdrissiLambrechtsWillwacher18} [[Ricardo Campos]], Najib Idrissi, [[Pascal Lambrechts]], [[Thomas Willwacher]], _Configuration Spaces of Manifolds with Boundary_ ([arXiv:1802.00716](https://arxiv.org/abs/1802.00716))


A systematic development of [[Euclidean field theory|Euclidean]] [[perturbative quantum field theory]] with [[n-point functions]] considered as [[smooth functions]] on [[Fulton-MacPherson compactifications]]/[[wonderful compactifications]] of [[configuration spaces of points]] and more generally of subspace arrangements is due to 

* {#BergbauerBrunettiKreimer09} [[Christoph Bergbauer]], [[Romeo Brunetti]], [[Dirk Kreimer]], _Renormalization and resolution of singularities_, ESI preprint 2010 ([arXiv:0908.0633](https://arxiv.org/abs/0908.0633), [ESI:2244](https://mat.univie.ac.at/~esiprpr/esi2244.pdf))

* {#Bergbauer09} [[Christoph Bergbauer]], _Renormalization and resolution of singularities_, talks as IHES and Boston, 2009 ([pdf](http://www.emg.uni-mainz.de/Dateien/bergbauer.pdf))

* {#Berghoff14a} [[Marko Berghoff]], _Wonderful renormalization_, 2014 ([pdf](http://www2.mathematik.hu-berlin.de/%7Ekreimer/wp-content/uploads/Berghoff-Marko.pdf), [doi:10.18452/17160](https://doi.org/10.18452/17160))

* {#Berghoff14b} [[Marko Berghoff]], _Wonderful compactifications in quantum field theory_,  Communications in Number Theory and Physics Volume 9 (2015) Number 3 ([arXiv:1411.5583](https://arxiv.org/abs/1411.5583))

Discussion specifically in [[topological quantum field theory]] with an eye towards [[supersymmetry|supersymmetric]] field theory, in terms of the [[ordinary homology]] of [[configuration spaces of points]]:

* [[Christopher Beem]], [[David Ben-Zvi]], [[Mathew Bullimore]], [[Tudor Dimofte]], [[Andrew Neitzke]], _Secondary products in supersymmetric field theory_ ([arXiv:1809.00009](https://arxiv.org/abs/1809.00009))


### As moduli of Dp-D(p+4)-brane bound states:
 {#AsModuliOfD0D4BraneBoundStates}

Discussion of configuration spaces of _possibly coincident_ points, hence of [[symmetric products]] $X^n/Sym(n)$ as [[moduli spaces]] of [[D0-D4-brane bound states]]:

* [[Cumrun Vafa]], _Instantons on D-branes_, Nucl. Phys. B463 (1996) 435-442 ([arXiv:hep-th/9512078](https://arxiv.org/abs/hep-th/9512078))

with emphasis to the resulting [[configuration spaces of points]], as in

* [[Cumrun Vafa]], [[Edward Witten]], Section 4.1 of: _A Strong Coupling Test of S-Duality_, Nucl. Phys. B431:3-77, 1994 ([arXiv:hep-th/9408074](https://arxiv.org/abs/hep-th/9408074))



[[!redirects configuration spaces of points]]
[[!redirects configuration space of n points]]
[[!redirects configuration spaces of n points]]


[[!redirects ordered configuration space of points]]
[[!redirects ordered configuration spaces of points]]
[[!redirects ordered configuration space of n points]]
[[!redirects ordered configuration spaces of n points]]

[[!redirects unordered configuration space of points]]
[[!redirects unordered configuration spaces of points]]
[[!redirects unordered configuration space of n points]]
[[!redirects unordered configuration spaces of n points]]


[[!redirects configuration space (mathematics)]]
[[!redirects configuration spaces (mathematics)]]





