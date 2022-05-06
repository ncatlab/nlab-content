
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


## Properties

### Cocycle spaces and the Scanning map
 {#CocycleSpacesAndScanningMap}

+-- {: .num_prop #ScanningMapEquivalence}
###### Proposition
**([[scanning map]] [[homotopy equivalence|equivalence]])**

In the context of Def. \ref{ConfigurationSpaceOfParticleswithLabels} let now 

1. $(X,\infty)$ be a [[compact topological space|compact]] [[pointed topological space|pointed]] [[smooth manifold]],

1. $(A,0)$ a [[pointed topological space|pointed]] [[CW-complex]].

Then there is a [[continuous function]], called the _[[scanning map]]_

$$
  Conf(X, A)
  \longrightarrow
  \Gamma( S_X(T X)\wedge_X A  )
$$

(from the configuration space of points in $X$ with charge in $A$ (Def. \ref{ConfigurationSpaceOfParticleswithLabels}) to the [[space of sections|space of]] [[continuous function|continuous]] [[sections]] of the [[spherical fibration]] induced by the [[tangent bundle]] of $X$ (the [[J-homomorphism]], [this Prop.](J-homomorphism#SphericalFibrationsOfVectorBundlesClassifiedViaJ)) [[fiber]]-wise [[smash product|smashed]] with the [[coefficient]] space $A$)

which is a [[homotopy equivalence]] if $X$ or $A$ is [[connected topological space|connected]].

=--

This is due to ([McDuff 75](#McDuff75)), for review see ([Bödigheimer 87, Prop. 2](#Boedigheimer87), [Francis Lecture 17, Theorem 1.1](#FrancisLect17)).

(As discussed there, the statement holds also under somewhat weaker assumptions than stated here.)

+-- {: .num_remark }
###### Remark
**(configuration spaces and [[twisted cohomology|twisted]] [[cohomotopy]])**

In the case that the coefficient space in Def. \ref{ConfigurationSpaceOfParticleswithLabels} is an [[n-sphere]] 

$$
  A \;\coloneqq\; S^n
$$  

regarded as [[coefficients]] for [[non-abelian cohomology]], then the scanning map equivalence (Prop. \ref{ScanningMapEquivalence}) identifies the configuration space with the [[cocycle]]-space/-[[infinity-groupoid]] of $\tau_X$-[[twisted cohomology|twisted]] [[cohomotopy]] in degree $\tau + n$, where $\tau_X \coloneqq [S_X(T X)]$ is the class of the [[spherical fibration]] of the tangent bundle.

In particular if $X$ is a [[parallelizable manifold]]/[[framed manifold]], then $\tau_X = dim(X)$ and the equivalence identifies the configuration space with the plain [[cohomotopy]] of $X$ in degree $dim(X) + n$:

$$
  Conf(X,S^n)
  \;\simeq\;
  Maps( X, S^{dim(X) + n} )
  \,.
$$


=--




## Examples

### Classifying space of the symmetric group

Let $X= \mathbb{R}^\infty$. Then 

* the _unordered_ configuration space of $n$ points in $\mathbb{R}^\infty$ is a model for the [[classifying space]] $B \Sigma(n)$ of the [[symmetric group]] $\Sigma(n)$;

  (e.g. [Bödigheimer 87, Example 10](#Boedigheimer87))


* the _ordered_ configuration space of $n$ points, equipped with the canonical $\Sigma(n)$-[[action]], is a model for the $\Sigma(n)$-[[universal principal bundle]].

### Points on $n$-spheres and the sphere spectrum
 {#PointsOnNSpheresAndTheSphereSpectrum}

+-- {: .num_example}
###### Example

The configuration space (Def. \ref{ConfigurationSpaceOfParticleswithLabels}) 
of the [[n-sphere]] with labels in any $A$ is identified by the [[scanning map]]-equivalence (Prop. \ref{ScanningMapEquivalence}) with the $n$-fold [[loop space]] of the $n$-fold [[suspension]] of $A$:

$$
  Conf(S^n,A)
  \;\simeq\;
  \Omega^n \Sigma^n A
$$

hence the [[colimit]] over $n$ yields the degree-0 space of the [[suspension spectrum]] of $A$ (the [[sphere spectrum]] when $A = S^0$ is the [[0-sphere]]). 

=--

(e.g. [Bödigheimer 87, Example 13](#Boedigheimer87))



### James construction

The [[James construction]] of $X$ is [[homotopy equivalence|homotopy equivalent]] to the [[configuration space (mathematics)|configuration space]] $C(\mathbb{R}^1, X)$ of points in the [[real line]] with "[[charges]]" taking values in $X$.

(e.g. [Bödigheimer 87, Example 9](#Boedigheimer87))


## References

### General

Review includes 

* {#FrancisLect17} [[John Francis]], _The H-Principle Lecture 17: The sheaf oof configuration spaces and the scanning map_ ([pdf](http://math.northwestern.edu/~jnkf/classes/hprin/17configmapping.pdf))


* {#Boedigheimer87} [[Carl-Friedrich Bödigheimer]], _Stable splittings of mapping spaces_, Algebraic topology. Springer 1987. 174-187 ([pdf](http://www.math.uni-bonn.de/~cfb/PUBLICATIONS/stable-splittings-of-mapping-spaces.pdf))

* [[Ben Knudsen]], _Configuration spaces in algebraic topology_, ([arXiv:1803.11165](https://arxiv.org/abs/1803.11165))


See also

* Edward Fadell, Lee Neuwirth, _Configuration spaces_
Math. Scand. __10__ (1962) 111-118, [MR141126](http://www.ams.org/mathscinet-getitem?mr=141126), [pdf](http://www.mscand.dk/article.php?id=1623)

* [[Graeme Segal]], _Configuration-spaces and iterated loop-spaces_, Invent. Math. __21__ (1973), 213&#8211;221. MR 0331377 ([pdf](http://dodo.pdmi.ras.ru/~topology/books/segal.pdf))


* {#McDuff75} [[Dusa McDuff]], _Configuration spaces of positive and negative particles_, Topology Volume 14, Issue 1, March 1975, Pages 91-107 (<a href="https://doi.org/10.1016/0040-9383(75)90038-5">doi:10.1016/0040-9383(75)90038-5</a>)


* [[Craig Westerland]], _Configuration spaces in geometry and topology_, 2011, [pdf](https://www.austms.org.au/Publ/Gazette/2011/Nov11/TechPaperWesterland.pdf)


* Edward R. Fadell, Sufian Y. Husseini, _Geometry and topology of configuration spaces_, Springer Monographs in Mathematics (2001), [MR2002k:55038](http://www.ams.org/mathscinet-getitem?mr=2002k:55038), xvi+313 pp.

* F. R. Cohen, [[Sam Gitler|S. Gitler]], _On loop spaces of configuration spaces_, Trans. Amer. Math. Soc. __354__ (2002), no. 5, 1705&#8211;1748, [MR2002m:55020](http://www.ams.org/mathscinet-getitem?mr=1881013)

### In Goodwillie-calculus
 {#ReferencesInGoodwillieCalculus}

The configuration spaces of a space $X$ appear as the [[Goodwillie derivatives]] of its [[mapping space]]/[[nonabelian cohomology]]-[[functor]] $Maps(X,-)$:


* {#Arone99} [[Greg Arone]], _A generalization of Snaith-type filtration_, Transactions of the American Mathematical Society 351.3 (1999): 1123-1150. ([pdf](https://www.ams.org/journals/tran/1999-351-03/S0002-9947-99-02405-8/S0002-9947-99-02405-8.pdf))

* {#Ching05} [[Michael Ching]], _Calculus of Functors and Configuration Spaces_, Conference on Pure and Applied Topology Isle of Skye, Scotland, 21-25 June, 2005 ([pdf](https://www3.amherst.edu/~mching/Work/skye.pdf))


[[!redirects scanning map]]
[[!redirects scanning maps]]

[[!redirects scanning map equivalence]]
[[!redirects scanning map equivalences]]

