


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
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

The subject of _equivariant differential topology_ is the enhancement of results of [[differential topology]] from plain [[manifolds]]/[[topological spaces]] to those equipped with [[actions]] of some [[group]] ([[G-spaces]]).

## Properties

+-- {: .num_prop #ExistenceOfGInvariantTubularNeighbourhoods}
###### Proposition
**(existence of $G$-invariant [[tubular neighbourhoods]])**

Let $X$ be a [[smooth  manifold]], $G$ a [[Lie group]] and $\rho \;\colon\; G \times X \to X$ a _[[proper action|proper]]_ [[action]] by [[diffeomorphisms]].

If $\Sigma \overset{\iota}{\hookrightarrow} X$ is a [[closed manifold|closed]] [[smooth manifold|smooth]] [[submanifold]] inside the $G$-[[fixed locus]]

\begin{center}
  \begin{xymatrix}
    \Sigma 
    \ar@{^{(}->}[rr]^-{\iota^G}
    \ar@{^{(}->}[dr]_{\iota}
    &&
    X^G
    \ar@{^{(}->}[dl]
    \\
    & 
    X
  \end{xymatrix}
\end{center}


then $\Sigma$ admits a $G$-invariant [[tubular neighbourhood]] $\Sigma \subset U \subset X$.

Moreover, any two choices of such $G$-invariant tubular neighbourhoods are $G$-equivariantly [[isotopy|isotopic]].

=--

([Kankaanrinta 07, theorem 4.4, theorem 4.6](#Kankaanrinta07))


+-- {: .num_prop #FixedLociOfSmoothProperActionsAreSubmanifolds}
###### Proposition
**([[fixed loci]] of [[smooth function|smooth]] [[proper actions]] are [[submanifolds]])**

Let $X$ be a [[smooth  manifold]], $G$ a [[Lie group]] and $\rho \;\colon\; G \times X \to X$ a _[[proper action|proper]]_ [[action]] by [[diffeomorphisms]].

Then the $G$-[[fixed locus]] $X^G \hookrightarrow X$ is a [[smooth manifold|smooth]] [[submanifold]].

If in addition $X$ is equipped with a [[Riemannian metric]] and $G$ acts by [[isometries]] then the [[submanifold]] $X^G$ is a [[totally geodesic submanifold]].

=--

(e.g. [Ziller 13, theorem 3.5.2](#Ziller13), see also [this MO discussion](https://math.stackexchange.com/a/1739784/58526))

+-- {: .proof}
###### Proof

Let $x \in X^G \subset X$ be any [[fixed point]]. Since this is in particular a closed invariant [[submanifold]], Prop. \ref{ExistenceOfGInvariantTubularNeighbourhoods} applies and shows that an [[open neighbourhood]] of $x$ in $X$ is $G$-equivariantly [[diffeomorphism|diffeomorphic]] to a [[linear representation]] $V \in RO(G)$. The [[fixed locus]] $V^G \subset V$ of that is hence [[diffeomorphism|diffeomorphic]] to an [[open neighbourhood]] of $x$ in $\Sigma$.

=--


+-- {: .num_remark}
###### Remark

Without the assumption of [[proper action]] in Prop. \ref{FixedLociOfSmoothProperActionsAreSubmanifolds} the conclusion generally fails. See [this MO comment](https://math.stackexchange.com/a/1739768/58526) for a counter-example.

=--



+-- {: .num_prop #GActionOnNormalBundleToFixedLocus}
###### Proposition/Definition
**($G$-action on [[normal bundle]] to [[fixed locus]])**

Let $X$ be a [[smooth  manifold]], $G$ a [[Lie group]] and $\rho \;\colon\; G \times X \to X$ a _[[proper action|proper]]_ [[action]] by [[diffeomorphisms]].

Then linearization of the $G$-action aroujnd the [[fixed locus]] $X^G \subset X$ equips the [[normal bundle]] $N_X\left( X^G\right)$ with [[smooth function|smooth]] and [[fiber]]-wise [[linear map|linear]]  $G$-[[action]].

=--

(as in [Crainic-Struchiner 13, Example 1.7](#CrainicStruchiner13))

+-- {: .num_prop #NormalBundleOfFixedLocusToTubularNeighbourhood}
###### Proposition (check)

Let $X$ be a [[smooth  manifold]], $G$ a [[Lie group]] and $\rho \;\colon\; G \times X \to X$ a _[[proper action|proper]]_ [[action]] by [[diffeomorphisms]].

Then for the [[normal bundle]] $N_X\left( X^G\right)$ of the [[fixed locus]] $X^G \subset X$ equipped with its induced $G$-[[action]] according to Prop./Def. \ref{GActionOnNormalBundleToFixedLocus} there exists a $G$-equivariant [[diffeomorphism]]

$$
  N_X
  \left(
    X^G
  \right)
  \overset{\simeq}{\longrightarrow}
  \mathcal{N}_X\left( X^G \right)
$$

onto a $G$-invariant [[tubular neighbourhood]] 
$\mathcal{N}_X\left( X^G \right)$ of $X^G$.

=--

+-- {: .proof}
###### Proof idea

Restricted to a small enough [[open neighbourhood]] of any point $x \in X^G$ this is the statement of the _slice theorem_. That these local identifications glue should follow by applying the isomoprhisms of [Pflaum-Posthuma-Tang 11, Theorem 4.1](#PflaumPosthumaTang11) at each for one fixe background metric.


=--


## Related concepts

* [[equivariant homotopy theory]]

* [[equivariant stable homotopy theory]]

* [[equivariant rational homotopy theory]]

* [[equivariant cohomology]]

## References

* {#Wasserman69} [[Arthur Wasserman]], section 3 of _Equivariant differential topology_, Topology Vol. 8, pp. 127-150, 1969 ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/wasserman.pdf))

* {#Bredon72} [[Glen Bredon]], _Introduction to compact transformation groups_, Academic Press 1972 ([pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf))

* {#Kankaanrinta07} [[Marja Kankaanrinta]], _Equivariant collaring, tubular neighbourhood and gluing theorems for proper Lie group actions_,     Algebr. Geom. Topol. Volume 7, Number 1 (2007), 1-27 ([euclid:agt/1513796653](https://projecteuclid.org/euclid.agt/1513796653))

* {#PflaumPosthumaTang11} Markus Pflaum, Hessel Posthuma, X. Tang, _Geometry of orbit spaces of proper Lie groupoids_ ([arXiv:1101.0180](https://arxiv.org/abs/1101.0180))

* {#Ziller13} Wolfgang Ziller, _Group actions_, 2013 ([pdf](https://www.math.upenn.edu/~wziller/math661/LectureNotesLee.pdf))

* {#CrainicStruchiner13} Marius Crainic, Ivan Struchiner, _On the linearization theorem for proper Lie groupoids_,  Annales scientifiques de l'École Normale Supérieure, Série 4, Volume 46 (2013) no. 5, p. 723-746 ([numdam:ASENS_2013_4_46_5_723_0](http://www.numdam.org/item/ASENS_2013_4_46_5_723_0/) [doi:10.24033/asens.2200](https://doi.org/10.24033/asens.2200))

