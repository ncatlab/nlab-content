


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

The subject of _equivariant differential topology_ is the enhancement of results of [[differential topology]] from plain [[manifolds]]/[[topological spaces]] to those equipped with [[actions]] of some [[group]] ([[G-spaces]]) -- the _[[equivariance group]]_.

## Properties



+-- {: .num_prop #FixedLociOfSmoothProperActionsAreSubmanifolds}
###### Proposition
**([[fixed loci]] of [[smooth function|smooth]] [[proper actions]] are [[submanifolds]])**

Let $X$ be a [[smooth  manifold]], $G$ a [[Lie group]] and $\rho \;\colon\; G \times X \to X$ a _[[proper action|proper]]_ [[action]] by [[diffeomorphisms]] (e.g. any smooth action if $G$ is [[compact Lie group|compact]], by [this Prop.](proper+action#SmoothActionOfCompactLieGroupOnSmoothManifoldIsProper)).

Then the $G$-[[fixed locus]] $X^G \hookrightarrow X$ is a [[smooth manifold|smooth]] [[submanifold]].

If in addition $X$ is equipped with a [[Riemannian metric]] and $G$ acts by [[isometries]], then the [[submanifold]] $X^G$ is a [[totally geodesic submanifold]].

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

(e.g. [Crainic-Struchiner 13, Example 1.7](#CrainicStruchiner13))


+-- {: .num_prop #ExistenceOfGInvariantRiemannianMetrics}
###### Proposition
**(existence of $G$-invariant [[Riemannian metric]])**

Let $X$ be a [[smooth  manifold]], $G$ a [[compact Lie group]] and $\rho \;\colon\; G \times X \to X$ a _[[proper action|proper]]_ [[action]] by [[diffeomorphisms]].

Then there exists a [[Riemannian metric]] on $X$ with its [[invariant]] with respect to the $G$-[[action]], hence such that all elements of $G$ act by [[isometries]].


=--

([Bredon 72, VI Theorem 2.1](#Bredon72), see also [Ziller 13, Theorem 3.0.2](#Ziller13))

+-- {: .num_defn #GInvariantTubularNeighbourhood}
###### Definition
**($G$-invariant [[tubular neighbourhood]])**

Let $X$ be a [[smooth  manifold]], $G$ a [[Lie group]] and $\rho \;\colon\; G \times X \to X$ a _[[proper action|proper]]_ [[action]] by [[diffeomorphisms]].

For $\Sigma \subset X^G \subset X$ a [[closed manifold|closed]] [[smooth manifold|smooth]] [[submanifold]] inside the [[fixed locus]], a _$G$-invariant [[tubular neighbourhood]]_ $\mathcal{N}(\Sigma \subset X)$ of $\Sigma$ in $X$ is 

1. a [[smooth vector bundle]] $E \to \Sigma$ equipped with a [[fiber]]-wise [[linear map|linear]] $G$-[[action]];

1. an equivariant [[diffeomorphism]] $E \overset{}{\longrightarrow} X$ onto an [[open neighbourhood]] of $\Sigma$ in $X$ which takes the [[zero section]] identically to $\Sigma$.

=--


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


then 

1. $\Sigma$ admits a $G$-invariant [[tubular neighbourhood]] $\Sigma \subset U \subset X$ (Def. \ref{GInvariantTubularNeighbourhood});

1. any two choices of such $G$-invariant tubular neighbourhoods are $G$-equivariantly [[isotopy|isotopic]];

1. there always exists an $G$-invariant tubular neighbourhood parametrized specifically by the [[normal bundle]] $N(\Sigma \subset X)$ of $Sigma$ in $X$, equipped with its induced $G$-[[action]] from Def. \ref{GActionOnNormalBundleToFixedLocus}, and such that the $G$-equivariant [[diffeomorphism]] is given by the [[exponential map]] 

   $$
     \exp_\epsilon
       \;\colon\;
     N(\Sigma \subset X)
       \overset{\simeq}{\longrightarrow}
     \mathcal{N}(\Sigma \subset X)
   $$

with respect to a $G$-invariant [[Riemannian metric]] (which exists according to Prop. \ref{ExistenceOfGInvariantRiemannianMetrics}):

=--

The existence of the $G$-invariant tubular neighbourhoods is for instance in [Bredon 72 VI Theorem 2.2](#Bredon72), [Kankaanrinta 07, theorem 4.4](#Kankaanrinta07). The uniqueness up to equivariant isotopy is in [Kankaanrinta 07, theorem 4.4, theorem 4.6](#Kankaanrinta07). The fact that one may always use the [[normal bundle]] appears at the end of the proof of [Bredon 72 VI Theorem 2.2](#Bredon72), and as a special case of a more general statement about invariant tubular neighbourhoods in [[Lie groupoids]] it follows from [Pflaum-Posthuma-Tang 11, Theorem 4.1](#PflaumPosthumaTang11) by applying the construction there to each point in $\Sigma$ for one and the same choice of background metric. See also for instance [Pflaum-Wilkin 17, Example 2.5](#PflaumWilkin17).


## Applications

* [[equivariant Hopf degree theorem]]

* [[equivariant Pontrjagin theorem]]



## Related concepts

* [[equivariant bundle]]

* [[equivariant homotopy theory]]

* [[equivariant stable homotopy theory]]

* [[equivariant rational homotopy theory]]

* [[equivariant cohomology]]

* [[equivariant cobordism theory]]

## References

* {#Wasserman69} [[Arthur Wasserman]], section 3 of: _Equivariant differential topology_, Topology Vol. 8, pp. 127-150, 1969 (<a href="https://doi.org/10.1016/0040-9383(69)90005-6">doi:10.1016/0040-9383(69)90005-6</a>[pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/wasserman.pdf))

* {#Bredon72} [[Glen Bredon]], _Introduction to compact transformation groups_, Academic Press 1972 ([pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf), [ISBN:9780080873596](https://www.elsevier.com/books/introduction-to-compact-transformation-groups/bredon/978-0-12-128850-1))

* [[Tammo tom Dieck]], Section I.5 of: _[[Transformation Groups]]_, de Gruyter 1987  ([doi:10.1515/9783110858372]( https://doi.org/10.1515/9783110858372))


* {#Kankaanrinta07} [[Marja Kankaanrinta]], _Equivariant collaring, tubular neighbourhood and gluing theorems for proper Lie group actions_,     Algebr. Geom. Topol. Volume 7, Number 1 (2007), 1-27 ([euclid:agt/1513796653](https://projecteuclid.org/euclid.agt/1513796653))

* {#PflaumPosthumaTang11} [[Markus Pflaum]], Hessel Posthuma, X. Tang, _Geometry of orbit spaces of proper Lie groupoids_, Journal für die reine und angewandte Mathematik (Crelles Journal) 2014.694 ([arXiv:1101.0180](https://arxiv.org/abs/1101.0180), [doi:10.1515/crelle-2012-0092](https://doi.org/10.1515/crelle-2012-0092))

* {#Ziller13} Wolfgang Ziller, _Group actions_, 2013 ([pdf](https://www.math.upenn.edu/~wziller/math661/LectureNotesLee.pdf))

* {#CrainicStruchiner13} Marius Crainic, Ivan Struchiner, _On the linearization theorem for proper Lie groupoids_,  Annales scientifiques de l'École Normale Supérieure, Série 4, Volume 46 (2013) no. 5, p. 723-746 ([numdam:ASENS_2013_4_46_5_723_0](http://www.numdam.org/item/ASENS_2013_4_46_5_723_0/) [doi:10.24033/asens.2200](https://doi.org/10.24033/asens.2200))

* {#PflaumWilkin17} [[Markus Pflaum]], Graeme Wilkin, _Equivariant control data and neighborhood deformation retractions_, Methods and Applications of Analysis, 2019 ([arXiv:1706.09539](https://arxiv.org/abs/1706.09539))

