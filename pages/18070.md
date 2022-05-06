
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

In [[mathematics]] typically by default the term "configuration space" of a [[topological space]] $X$ refers to the topological space of pairwise distinct points in $X$, also called _[[Fadell's configuration space]]_, for emphasis.

In principle many other kinds of configurations and the spaces these form may be referred to by "configuration space", notably in [[physics]] the usage is in a broader sense, see at _[[configuration space (physics)]]_.

## Definition

+-- {: .num_defn #ConfigurationSpaceOfParticleswithLabels}
###### Definition
**(configuration space of particles with labels)**

Let $(X, \infty)$ and $(A, 0)$ be [[pointed topological spaces]].

Then the _configuration space of points in $X$ with labels in $A$_

$$
  Conf(X, A)
  \;\coloneqq\;
  \left(
    \underset{ n \in \mathbb{N} }{\coprod} 
    \left( 
      X^n \setminus \mathbf{\Delta}^n_X
    \right)
    \times A^n
  \right)/\sim
$$

is the [[quotient space]] of the [[disjoint union]] of the [[Cartesian products]] of the space of configurations of distinguishable but unlabeled [[n-tuples]] of points, hence the [[complement]] in $X^n$ of the [[fat diagonal]] $\mathbf{\Delta}_X^n$, with the products of label spaces, by the following [[equivalence relations]]:

1. [[action]] of the [[symmetric group]]:

   $$
     \big((x_1, \cdots, x_n), (a_1, \cdots, a_n)\big) 
     \sim 
     \big((x_{\sigma(1)}, \cdots, x_{\sigma(n)}), (a_{\sigma(1)}, \cdots, a_{\sigma(n)})\big) 
   $$

   for any [[permutation]] $\sigma \in S_n$


1. vanishing of particles of "zero charge":

   $$     
     \big((x_1, \cdots, x_{n-1}, x_n), (a_1, \cdots, a_{n-1}, 0)\big) 
     \;\sim\;
     \big((x_1, \cdots, x_{n-1}), (a_1, \cdots, a_{n-1})\big) 
   $$

1. vanishing of particles of "[[vanishing at infinity|at infinity]]":

   $$     
     \big((x_1, \cdots, x_{n-1}, \infty), (a_1, \cdots, a_{n-1}, a_n)\big) 
     \;\sim\;
     \big((x_1, \cdots, x_{n-1}), (a_1, \cdots, a_{n-1})\big) 
   $$


=--

(e.g. [Bödigheimer 87, 1](#Boedigheimer87))


+-- {: .num_example #UnlabeledConfigurationSpace}
###### Example
**(configuration space of unlabeled points)**

For $A = S^0 = \{1\}_+$ the [[0-sphere]] all points in Def. \ref{ConfigurationSpaceOfParticleswithLabels} carry the same label "1", which means that they are actually unlabeled, and we will write just

\[
  \label{ConfigurationSpaceOfUnlabeledPoints}
  Conf(X)
  \;\coloneqq\;
  Conf(X,S^0)
\]

in this case.

=--


## Properties

### Cocycle spaces and the Scanning map
 {#CocycleSpacesAndScanningMap}


In the context of Def. \ref{ConfigurationSpaceOfParticleswithLabels} let now 

1. $(X,\infty)$ be a [[compact topological space|compact]] [[pointed topological space|pointed]] [[smooth manifold]],

1. $(A,0)$ be a [[pointed topological space|pointed]] [[CW-complex]].


+-- {: .num_defn #TheSpaceOfSections}
###### Definition

Write 

\[
  \label{SPaceOfSections}
  \widetilde \Gamma_X
  \left(
     S_X^{T X}\wedge_X A  
  \right)
  \;\subset\;
  \Gamma_X\left(
    S_X^{T X}\wedge_X A  
  \right)
\]

for the [[topological subspace|subspace]] of the [[space of sections|space of]] [[continuous function|continuous]] [[sections]] of the  [[spherical fibration]] $S_X^{T X} \to X$ obtained from the [[tangent bundle]] $T X \to  X$ via [[fiber]]-wise [[one-point compactification]], on those sections which preserve the base point (take $\infty \in X$ to $0 \in A$).

If we let $\tau_X \;\colon X \to B O$ denote the [[classifying map]] of the [[tangent bundle]], then this spherical fibration is classified by it [[composition]] $J(\tau_X)$ with the [[J-homomorphism]] ([this Prop.](J-homomorphism#SphericalFibrationsOfVectorBundlesClassifiedViaJ)).

=--

+-- {: .num_defn #ScanningMap}
###### Definition
**([[scanning map]])**

The _[[scanning map]]_ is the [[continuous function]]

$$
  Conf(X, A)
   \overset{scan}{\longrightarrow}
  \widetilde \Gamma_X\left(
     S_X^{T X}\wedge_X A  
  \right)
$$

from the configuration space (Def. \ref{ConfigurationSpaceOfParticleswithLabels}) to the space of sections (Def \ref{TheSpaceOfSections}) given by ...
 
=--

([Segal 73](#Segal73), [McDuff 75, p. 94, 95](#McDuff75))

+-- {: .num_example}
###### Example
**(electric field map)**

In the case of the configuration space of unlabeled points ($A = S^0$, Example \ref{UnlabeledConfigurationSpace}), and taking $X = (\mathbb{R}^n)^\ast$ to be the [[one-point compactification]] of  [[Cartesian space]]/[[Euclidean space]] $\mathbb{R}^3$, if one thinks of each point as representing a [[particle]] of [[electric charge]] $+1$, then the [[scanning map]] of Def. \ref{ScanningMap} may be thought of as sending each configuration of charged particles to the [[electric field]] that it induces ([Segal 73](#Segal73)).

=--


+-- {: .num_prop #ScanningMapEquivalence}
###### Proposition
**([[scanning map]] [[homotopy equivalence|equivalence]])**

In the context of Def. \ref{ConfigurationSpaceOfParticleswithLabels} let

1. $(X,\infty)$ be a [[compact topological space|compact]] [[pointed topological space|pointed]] [[smooth manifold]],

1. $(A,0)$ be a [[pointed topological space|pointed]] [[CW-complex]].

and assume that $X$ or $A$ is [[connected topological space|connected]].

Then the [[scanning map]] (Def. \ref{ScanningMap}) is a [[homotopy equivalence]]:

$$
  Conf(X, A)
   \underoverset{\simeq_{he}}{scan}{\longrightarrow}
  \widetilde \Gamma_X\left(
     S_X^{T X}\wedge_X A  
  \right)
  \,.
$$


=--

This is due to ([McDuff 75](#McDuff75)), for review see ([Bödigheimer 87, Prop. 2](#Boedigheimer87), [Francis Lecture 17, Theorem 1.1](#FrancisLect17)).

(As discussed there, the statement holds also under somewhat weaker assumptions than stated here.)

+-- {: .num_remark #ConfigurationSpacesAndCocyclesForTwistedReducedCohomotopy}
###### Remark
**(configuration spaces and [[cocycles]] for [[twisted cohomology|twisted]] [[reduced cohomology|reduced]] [[cohomotopy]])**

In the case that the coefficient space in Def. \ref{ConfigurationSpaceOfParticleswithLabels} is an [[n-sphere]] 

$$
  A \;\coloneqq\; S^n
$$  

regarded as [[coefficients]] for [[non-abelian cohomology]], then the scanning map equivalence (Prop. \ref{ScanningMapEquivalence}) identifies the configuration space with the [[cocycle]]-space/-[[infinity-groupoid]] of [[reduced cohomology|reduced]] $\tau_X$-[[twisted cohomology|twisted]] [[cohomotopy]] in degree $\tau_X + n$, where $\tau_X \coloneqq [S_X^{T X}]$ is the class of the [[spherical fibration]] of the tangent bundle.

In particular if $X - \{\infty\}$ is a [[parallelizable manifold]]/[[framed manifold]], then 

$$
  \tau_X\vert_{ X - \{\infty\}} = dim(X)
$$ 

and the equivalence identifies the configuration space with the [[cocycle]]-space of plain [[reduced cohomology|reduced]] [[cohomotopy]] of $X$ in degree $dim(X) + n$:

$$
  Conf(X,S^n)
  \;\simeq\;
  \widetilde \mathbf{H}^{dim(X) + n}(X, S^0)
  \,.
$$

If here $X$ is the [[one-point compactification]] of some $Y$, then this is equivalently the [[compactly supported cohomology|compactly supported]] [[cohomotopy]] of $Y$

$$
  Conf(X,S^n)
  \;\simeq\;
  \mathbf{H}_{cp}^{dim(X) + n}(X, S^0)
  \,.
$$


In particular for configurations of un-labeled points (Example \ref{UnlabeledConfigurationSpace}) over [[manifolds]] that are [[one-point compactifications]] of [[parallelizable manifolds]], the scanning map equivalence (Prop. \ref{ScanningMapEquivalence}) identifies the plain configuration space (eq:ConfigurationSpaceOfUnlabeledPoints) with the [[cocycle]] space for [[reduced cohomology|reduced]] [[cohomotopy]] in degree the [[dimension]] of $X$.

\[
  \label{ConfigurationSpacesEquivalentToSpaceOfCocyclesForCohomotopy}
  Conf(X)
  \;\simeq\;
  \widetilde \mathbf{H}^{dim(X)}(X, S^0)
  \,.
\]

=--




## Examples

### Points on $n$-spheres and the sphere spectrum
 {#PointsOnNSpheresAndTheSphereSpectrum}

+-- {: .num_example}
###### Example

For $n \in \mathbb{N}$ consider the [[n-sphere]]

$$
  S^n \;=\; \left( \mathbb{R}^n\right)^\ast
$$

as the [[one-point compactification]] of the [[Cartesian space]]/[[Euclidean space]] $\mathbb{R}^n$.

Since $\mathbb{R}^n$ is trivially a [[parallelizable manifold]] it follows as in Remark \ref{ConfigurationSpacesAndCocyclesForTwistedReducedCohomotopy} that the [[scanning map]]-equivalence (Prop. \ref{ScanningMapEquivalence}) identifies 

$$
  \begin{aligned}
    Conf(S^n,A)
    &
    \simeq\;
    \widetilde \Gamma_{S^n}
    \left( 
       \underset{ 
         \underset{ \text{on} X - \{\infty\} }{\simeq }
         \mathbb{R}^n \wedge S^{n} 
       }{
         \underbrace{ S_X^{T X} } 
       } 
       \wedge A
   \right)
   \\
   & \simeq
   \Omega^n \Sigma^n A
  \end{aligned}
$$

the configuration of $A$-labeled points with the $n$-fold [[loop space]] of the $n$-fold [[reduced suspension]] of the label space $A$. 

In particular if $A = S^0$, then the configuration space of unlabeled points (Def. \ref{UnlabeledConfigurationSpace}) in $S^n$ is identified with 

$$
  Conf\left( (\mathbb{R}^n)^\ast \right)
  \;\simeq\;
  \Omega^n \Sigma^n S^0
  \;\simeq\;
  \widetilde \mathbf{H}^n(S^n, S^0)
  \;=\;
  \mathbf{H}_{cp}^{n}(\mathbb{R}^n, S^0)
  \,.
$$

Taking here the [[colimit]] over $n \in \mathbb{N}$ on both sides hence exhibits the configuration space in $\mathbb{R}^{\infty}$ as the degree-0 space of the [[sphere spectrum]]:

$$
  Conf\left( (\mathbb{R}^\infty)^\ast \right)
  \;\simeq\;
  \Omega^\infty \Sigma^\infty S^0
  \;\simeq\;
  \Omega^\infty \mathbb{S}
  \,.
$$

=--

This is originally ([Segal 73, theorem 3](#Segal73)). It follows via Remark \ref{ConfigurationSpacesAndCocyclesForTwistedReducedCohomotopy} as a special case of Prop. \ref{ScanningMapEquivalence} of [McDuff 75](#McDuff75), for reviw see e.g. [Bödigheimer 87, Example 13](#Boedigheimer87).



### Classifying space of the symmetric group

Let $X= \mathbb{R}^\infty$. Then 

* the _unordered_ configuration space of $n$ points in $\mathbb{R}^\infty$ is a model for the [[classifying space]] $B \Sigma(n)$ of the [[symmetric group]] $\Sigma(n)$;

  (e.g. [Bödigheimer 87, Example 10](#Boedigheimer87))


* the _ordered_ configuration space of $n$ points, equipped with the canonical $\Sigma(n)$-[[action]], is a model for the $\Sigma(n)$-[[universal principal bundle]].



### James construction

The [[James construction]] of $X$ is [[homotopy equivalence|homotopy equivalent]] to the [[configuration space (mathematics)|configuration space]] $C(\mathbb{R}^1, X)$ of points in the [[real line]] with "[[charges]]" taking values in $X$.

(e.g. [Bödigheimer 87, Example 9](#Boedigheimer87))


## References

### General 

General survey includes

* [[Craig Westerland]], _Configuration spaces in geometry and topology_, 2011 ([pdf](https://www.austms.org.au/Publ/Gazette/2011/Nov11/TechPaperWesterland.pdf))

* [[Ben Knudsen]], _Configuration spaces in algebraic topology_ ([arXiv:1803.11165](https://arxiv.org/abs/1803.11165))

See also

* Edward Fadell, Lee Neuwirth, _Configuration spaces_
Math. Scand. __10__ (1962) 111-118, [MR141126](http://www.ams.org/mathscinet-getitem?mr=141126), [pdf](http://www.mscand.dk/article.php?id=1623)


* Edward R. Fadell, Sufian Y. Husseini, _Geometry and topology of configuration spaces_, Springer Monographs in Mathematics (2001), [MR2002k:55038](http://www.ams.org/mathscinet-getitem?mr=2002k:55038), xvi+313 pp.

* F. R. Cohen, [[Sam Gitler|S. Gitler]], _On loop spaces of configuration spaces_, Trans. Amer. Math. Soc. __354__ (2002), no. 5, 1705&#8211;1748, [MR2002m:55020](http://www.ams.org/mathscinet-getitem?mr=1881013)


* [[Sadok Kallel]], Ines Saihi, _Homotopy Groups of Diagonal Complements_, Algebr. Geom. Topol. 16 (2016) 2949-2980 ([arXiv:1306.6272](https://arxiv.org/abs/1306.6272))





### Scanning map and Relation to cohomotopy

The [[scanning map]] and hence the relation of configuration spaces to [[cohomotopy]] goes back to 


* {#Segal73} [[Graeme Segal]], _Configuration-spaces and iterated loop-spaces_, Invent. Math. __21__ (1973), 213&#8211;221. MR 0331377 ([pdf](http://dodo.pdmi.ras.ru/~topology/books/segal.pdf))

where it is considered for point in Euclidean spaces without labels ("electric field map"). Generalization of these constructions and results to more general spaces and to points with labels is due to 

* {#McDuff75} [[Dusa McDuff]], _Configuration spaces of positive and negative particles_, Topology Volume 14, Issue 1, March 1975, Pages 91-107 (<a href="https://doi.org/10.1016/0040-9383(75)90038-5">doi:10.1016/0040-9383(75)90038-5</a>)

* {#Boedigheimer87} [[Carl-Friedrich Bödigheimer]], _Stable splittings of mapping spaces_, Algebraic topology. Springer 1987. 174-187 ([pdf](http://www.math.uni-bonn.de/~cfb/PUBLICATIONS/stable-splittings-of-mapping-spaces.pdf))

and generalization to [[equivariant cohomology]] is discussed in

* Colin Rourke, Brian Sanderson, _Equivariant Configuration Spaces_, 62(2), October 2000, pp. 544-552 ([pdf](http://wrap.warwick.ac.uk/828/1/WRAP_Rourke_Equivariant_configuration.pdf))


Reviews include


* {#FrancisLect17} [[John Francis]], _The H-Principle Lecture 17: The sheaf of configuration spaces and the scanning map_ ([pdf](http://math.northwestern.edu/~jnkf/classes/hprin/17configmapping.pdf))


See also

* [[Sadok Kallel]], _Particle Spaces on Manifolds and Generalized Poincaré Dualities_ ([arXiv:math/9810067](https://arxiv.org/abs/math/9810067)) 

* [[Shingo Okuyama]], [[Kazuhisa Shimakawa]], _Interactions of strings and equivariant homology theories_, ([arXiv:0903.4667](https://arxiv.org/abs/0903.4667))


### In Goodwillie-calculus
 {#ReferencesInGoodwillieCalculus}

The configuration spaces of a space $X$ appear as the [[Goodwillie derivatives]] of its [[mapping space]]/[[nonabelian cohomology]]-[[functor]] $Maps(X,-)$:


* {#Arone99} [[Greg Arone]], _A generalization of Snaith-type filtration_, Transactions of the American Mathematical Society 351.3 (1999): 1123-1150. ([pdf](https://www.ams.org/journals/tran/1999-351-03/S0002-9947-99-02405-8/S0002-9947-99-02405-8.pdf))

* {#Ching05} [[Michael Ching]], _Calculus of Functors and Configuration Spaces_, Conference on Pure and Applied Topology Isle of Skye, Scotland, 21-25 June, 2005 ([pdf](https://www3.amherst.edu/~mching/Work/skye.pdf))


[[!redirects scanning map]]
[[!redirects scanning maps]]

[[!redirects scanning map equivalence]]
[[!redirects scanning map equivalences]]

