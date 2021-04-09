
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

The notion of _equivariant tubular neighbourhood_ (often called "invariant"!) is the generalization of the notion of _[[tubular neighbourhood]]_ from [[differential topology]] to [[equivariant differential topology]].


## Definition


+-- {: .num_defn #GInvariantTubularNeighbourhood}
###### Definition
**($G$-[[equivariant tubular neighbourhood]])**

Let $X$ be a [[smooth  manifold]], $G$ a [[Lie group]] and $\rho \;\colon\; G \times X \to X$ a _[[proper action|proper]]_ [[action]] by [[diffeomorphisms]].

For $\Sigma \subset X^G \subset X$ a [[closed manifold|closed]] [[smooth manifold|smooth]] [[submanifold]] inside the [[fixed locus]], a _$G$-[[equivariant tubular neighbourhood]]_ $\mathcal{N}(\Sigma \subset X)$ of $\Sigma$ in $X$ is 

1. a [[smooth vector bundle]] $E \to \Sigma$ equipped with a [[fiber]]-wise [[linear map|linear]] $G$-[[action]];

1. an equivariant [[diffeomorphism]] $E \overset{}{\longrightarrow} X$ onto an [[open neighbourhood]] of $\Sigma$ in $X$ which takes the [[zero section]] identically to $\Sigma$.

=--

## Properties

### Existence

+-- {: .num_prop #GActionOnNormalBundleToFixedLocus}
###### Proposition/Definition
**($G$-action on [[normal bundle]] to [[fixed locus]])**

Let $X$ be a [[smooth  manifold]], $G$ a [[Lie group]] and $\rho \;\colon\; G \times X \to X$ a _[[proper action|proper]]_ [[action]] by [[diffeomorphisms]].

Then linearization of the $G$-action aroujnd the [[fixed locus]] $X^G \subset X$ equips the [[normal bundle]] $N_X\left( X^G\right)$ with [[smooth function|smooth]] and [[fiber]]-wise [[linear map|linear]]  $G$-[[action]].

=--

(e.g. [Crainic-Struchiner 13, Example 1.7](#CrainicStruchiner13))


+-- {: .num_prop #ExistenceOfGInvariantTubularNeighbourhoods}
###### Proposition
**(existence of $G$-[[equivariant tubular neighbourhoods]])**

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

1. $\Sigma$ admits a $G$-[[equivariant tubular neighbourhood]] $\Sigma \subset U \subset X$ (Def. \ref{GInvariantTubularNeighbourhood});

1. any two choices of such $G$-equivariant tubular neighbourhoods are $G$-[[equivariant function|equivariantly]] [[isotopy|isotopic]];

1. there always exists an $G$-equivariant tubular neighbourhood parametrized specifically by the [[normal bundle]] $N(\Sigma \subset X)$ of $Sigma$ in $X$, equipped with its induced $G$-[[action]] from Def. \ref{GActionOnNormalBundleToFixedLocus}, and such that the $G$-equivariant [[diffeomorphism]] is given by the [[exponential map]] 

   $$
     \exp_\epsilon
       \;\colon\;
     N(\Sigma \subset X)
       \overset{\simeq}{\longrightarrow}
     \mathcal{N}(\Sigma \subset X)
   $$

with respect to a $G$-invariant [[Riemannian metric]] (which exists according to Prop. \ref{ExistenceOfGInvariantRiemannianMetrics}):

=--

The existence of the $G$-equivariant tubular neighbourhoods is for instance in [Bredon 72 VI Theorem 2.2](#Bredon72), [Kankaanrinta 07, theorem 4.4](#Kankaanrinta07). The uniqueness up to equivariant isotopy is in [Kankaanrinta 07, theorem 4.4, theorem 4.6](#Kankaanrinta07). The fact that one may always use the [[normal bundle]] appears at the end of the proof of [Bredon 72 VI Theorem 2.2](#Bredon72), and as a special case of a more general statement about invariant tubular neighbourhoods in [[Lie groupoids]] it follows from [Pflaum-Posthuma-Tang 11, Theorem 4.1](#PflaumPosthumaTang11) by applying the construction there to each point in $\Sigma$ for one and the same choice of background metric. See also for instance [Pflaum-Wilkin 17, Example 2.5](#PflaumWilkin17).

## References

* {#Bredon72} [[Glen Bredon]], _[[Introduction to compact transformation groups]]_, Academic Press 1972 ([pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf), [ISBN:9780080873596](https://www.elsevier.com/books/introduction-to-compact-transformation-groups/bredon/978-0-12-128850-1))

* {#Kankaanrinta07} [[Marja Kankaanrinta]], _Equivariant collaring, tubular neighbourhood and gluing theorems for proper Lie group actions_,     Algebr. Geom. Topol. Volume 7, Number 1 (2007), 1-27 ([euclid:agt/1513796653](https://projecteuclid.org/euclid.agt/1513796653))

* {#PflaumPosthumaTang11} [[Markus Pflaum]], Hessel Posthuma, X. Tang, _Geometry of orbit spaces of proper Lie groupoids_, Journal für die reine und angewandte Mathematik (Crelles Journal) 2014.694 ([arXiv:1101.0180](https://arxiv.org/abs/1101.0180), [doi:10.1515/crelle-2012-0092](https://doi.org/10.1515/crelle-2012-0092))

* {#PflaumWilkin17} [[Markus Pflaum]], Graeme Wilkin, _Equivariant control data and neighborhood deformation retractions_, Methods and Applications of Analysis, 2019 ([arXiv:1706.09539](https://arxiv.org/abs/1706.09539))

[[!redirects equivariant tubular neighbourhoods]]


[[!redirects invariant tubular neighbourhood]]
[[!redirects invariant tubular neighbourhoods]]



