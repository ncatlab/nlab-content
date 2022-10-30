
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
  {#Definition}



+-- {: .num_defn #ConfigurationSpacesOfnPoints}
###### Definition
**([[configuration spaces of points]])**

Let $X$ be a [[manifold]], possibly with [[manifold with boundary|boundary]].
For $n \in \mathbb{N}$, the
 _**configuration space of $n$ points** in $X$ disappearing at the boundary_ is the [[topological space]]
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
  and where $\Sigma(n)$ denotes the evident [[action]] of the [[symmetric group]] by [[permutation]] of factors of $X$ inside
  $X^n$.
  
  More generally, let $Y$ be another [[manifold]], possibly with [[manifold with boundary|boundary]].
  For $n \in \mathbb{N}$, the
  _**configuration space of $n$ points** in $X \times Y$ vanishing at the boundary and distinct as points in $X$_ is the [[topological space]]
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


### Relation to iterated loop spaces of iterated suspensions
 {#LoopSpacesOfSuspensions}


+-- {: .num_prop #ScanningMapEquivalenceOverCartesianSpace}
###### Proposition
**([[iterated loop spaces]] equivalent to [[configuration spaces of points]])**


For 

1. $d \in \mathbb{N}$, $d \geq 1$ a [[natural number]] with $\mathbb{R}^d$ denoting the [[Cartesian space]]/[[Euclidean space]] of that [[dimension]],

1. $Y$ a [[manifold]], with [[inhabited set|non-empty]] [[manifold with boundary|boundary]] so that  $Y / \partial Y$ is [[connected topological space|connected]],

the electric field map/[[scanning map]] constitutes a [[homotopy equivalence]]

$$
  Conf\left( 
    \mathbb{R}^d, Y
  \right)
  \overset{scan}{\longrightarrow}
  \Omega^d \Sigma^d (Y/\partial Y)
$$

between 

1. the configuration space of arbitrary points in $\mathbb{R}^d \times Y$ vanishing at the boundary (Def. \ref{ConfigurationSpacesOfnPoints}) 

1. the [[iterated loop space|d-fold loop space]] of the $d$-fold [[reduced suspension]] of the [[quotient space]] $Y / \partial Y$ (regarded as a [[pointed topological space]] with basepoint $[\partial Y]$).

In particular when $Y = \mathbb{D}^k$ is the [[closed ball]] of [[dimension]] $k \geq 1$ this gives a [[homotopy equivalence]]

$$
  Conf\left( 
    \mathbb{R}^d, \mathbb{D}^k
  \right)
  \overset{scan}{\longrightarrow}
  \Omega^d S^{ d + k }
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

Combined with the [[stabilization]] of the electric field map/[[scanning map]] [[homotopy equivalence]] from Prop. \ref{ScanningMapEquivalenceOverCartesianSpace} this yields a [[stable weak homotopy equivalence]]

$$
  Maps_{cp}(\mathbb{R}^d, \Sigma^d (Y / \partial Y))
  =
  Maps^{\ast/}( S^d, \Sigma^d (Y / \partial Y))
  =
  \Omega^d \Sigma^d (Y/\partial Y)
  \underoverset{\Sigma^\infty scan}{\simeq}{\longrightarrow}
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


### Relation to twisted Cohomotopy
 {#RelationToTwistedCohomotopy}

The May-Segal theorem \ref{ScanningMapEquivalenceOverCartesianSpace} generalizes from [[spheres]] to [[closed manifold|closed]] [[smooth manifolds]] if at the same time one passes from plain [[Cohomotopy]] to [[twisted Cohomotopy]], twisted, via the [[J-homomorphism]], by the [[tangent bundle]]:

+-- {: .num_prop #ScanningMapEquivalenceOverClosedManifold}
###### Proposition

Let 

1. $X^n$ be a [[smooth manifold|smooth]] [[closed manifold]] of [[dimension]] $n$;

1. $1 \leq k \in \mathbb{N}$ a [[positive number|positive]] [[natural number]].

Then the [[scanning map]] constitutes a [[weak homotopy equivalence]]

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
    \text{scanning map}
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

Then the [[scanning map]] constitutes a [[weak homotopy equivalence]]

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
    \text{scanning map}
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



### Action by little $n$-disk operad and by Goodwillie derivatives


Under some conditions and with suitable degrees/shifts,
configuration spaces of points canonically have the [[structure]] of [[algebras over an operad]] over the [[little n-disk operad]] and the [[Goodwillie derivatives of the identitity functor]].

For more see [there](Goodwillie+derivatives+of+the+identity+functor#Properties)




\linebreak


### Rational homotopy type
 {#RationalHomotopyType}

We discuss aspects of the [[rational homotopy type]] of configuration spaces of points. See also at _[[graph complex]]_.


#### Rational cohomology
 {#Cohomology}


+-- {: .num_prop #RealCohomologyOfConfigurationSpaceOfOrderedPointsInEuclideanSpace}
###### Proposition
**([[real cohomology]] of configuration spaces of ordered points in [[Euclidean space]])**

The [[real cohomology|real]] [[cohomology ring]] of the configuration spaces 

$$
  Conf_n\big( \mathbb{R}^D \big) 
  \;\coloneqq\;
  \big( \mathbb{R}^D \big)^n \setminus FatDiag
$$

of $n$ ordered points in [[Euclidean space]] $\mathbb{R}^D$ is [[generators and relations|generated]] by elements 

$$ 
  \omega_{i j}
  \;\;
  \in
  H^2
  \Big(
    Conf_n\big( \mathbb{R}^D \big),
    \mathbb{R}
  \Big)
$$

for $i, j \in \{1, \cdots, n\}$

subject to these three [[generators and relations|relations]]:

1. $\omega_{i j} = (-1)^D \omega_{j i} $;

1. $\omega_{i j} \wedge \omega_{i j} \;=\; 0$;

1. $\omega_{i j} \wedge \omega_{j k} + \omega_{j k} \omega_{k i} + \omega_{k i} \wedge \omega_{i j} = 0$.

Hence:

$$
  H^\bullet
  \Big(
    Conf_n\big( \mathbb{R}^D \big),
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
$$

=--

This is due to [Arnold 69](#Arnold69), [Cohen 73](#Cohen73). See also [Lambrechts-Tourtchine 09, Section 3](#LambrechtsTourtchine09).

See also at _[[Fulton-MacPherson compactification]]_ the section _[de Rham cohomology](Fulton-MacPherson+operad#deRhamCohomology)_.



+-- {: .num_remark #RealCohomologyOfConfigurationSpaceInTermsOfGraphCohomology} 
###### Remark
**([[real cohomology]] of the configuration space in terms of [[graph cohomology]])**

In the [[graph complex]]-model for the [[rational homotopy type]] of the ordered [[configuration space of points]] $Conf_n\big( \mathbb{R}^D\big)$ the three relations in Prop. \ref{RealCohomologyOfConfigurationSpaceOfOrderedPointsInEuclideanSpace} are incarnated as follows:

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

## Occurrences and Applications 
  {#OccurrencesAndApplications}

### Compactification

The [[Fulton-MacPherson compactification]] of configuration spaces of points in $\mathbb{R}^d$ serves to exhibit them as models for the [[little n-disk operad]]. 

### Stable splitting of mapping spaces

The [[stable splitting of mapping spaces]] says that [[suspension spectra]] of suitable [[mapping spaces]] are equivalently [[wedge sums]] of [[suspension spectra]] of configuration spaces of points.

### Correlators as differential forms on configiration spaces

In [[Euclidean field theory]] the [[correlators]] are often regarded as [[distributions of several variables]] with [[singularities]] on the [[fat diagonal]]. Hence they become [[non-singular distributions]] after [[restriction of distributions]] to the corresponding configuration space of points. 

For more on this see at _[[correlators as differential forms on configuration spaces of points]]_.

## Related concepts

* [[Hilbert scheme]]

## References

### General 

General survey includes

* [[Craig Westerland]], _Configuration spaces in geometry and topology_, 2011 ([pdf](https://www.austms.org.au/Publ/Gazette/2011/Nov11/TechPaperWesterland.pdf))

* [[Ben Knudsen]], _Configuration spaces in algebraic topology_ ([arXiv:1803.11165](https://arxiv.org/abs/1803.11165))

See also

* Edward Fadell, Lee Neuwirth, _Configuration spaces_
Math. Scand. __10__ (1962) 111-118, [MR141126](http://www.ams.org/mathscinet-getitem?mr=141126), [pdf](http://www.mscand.dk/article.php?id=1623)


* Edward R. Fadell, Sufian Y. Husseini, _Geometry and topology of configuration spaces_, Springer Monographs in Mathematics (2001), [MR2002k:55038](http://www.ams.org/mathscinet-getitem?mr=2002k:55038), xvi+313 pp.

* [[Fred Cohen]], [[Sam Gitler|S. Gitler]], _On loop spaces of configuration spaces_, Trans. Amer. Math. Soc. __354__ (2002), no. 5, 1705&#8211;1748, [MR2002m:55020](http://www.ams.org/mathscinet-getitem?mr=1881013)


* [[Sadok Kallel]], Ines Saihi, _Homotopy Groups of Diagonal Complements_, Algebr. Geom. Topol. 16 (2016) 2949-2980 ([arXiv:1306.6272](https://arxiv.org/abs/1306.6272))





### Electric field map/Scanning map and cohomotopy

The electric field map/[[scanning map]] and hence the relation of configuration spaces to [[cohomotopy]] goes back to 

* {#May72} [[Peter May]], _The geometry of iterated loop spaces_, Springer 1972 ([pdf](https://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf))

* {#Segal73} [[Graeme Segal]], _Configuration-spaces and iterated loop-spaces_, Invent. Math. __21__ (1973), 213&#8211;221. MR 0331377 ([pdf](http://dodo.pdmi.ras.ru/~topology/books/segal.pdf))

Generalization of these constructions and results is due to

* {#McDuff75} [[Dusa McDuff]], _Configuration spaces of positive and negative particles_, Topology Volume 14, Issue 1, March 1975, Pages 91-107 (<a href="https://doi.org/10.1016/0040-9383(75)90038-5">doi:10.1016/0040-9383(75)90038-5</a>)

* {#Boedigheimer87} [[Carl-Friedrich Bödigheimer]], _Stable splittings of mapping spaces_, Algebraic topology. Springer 1987. 174-187 ([pdf](http://www.math.uni-bonn.de/~cfb/PUBLICATIONS/stable-splittings-of-mapping-spaces.pdf), [[BoedigheimerStableSplittings87.pdf:file]])


and generalization to [[equivariant homotopy theory]] is discussed in

* Colin Rourke, Brian Sanderson, _Equivariant Configuration Spaces_, 62(2), October 2000, pp. 544-552 ([pdf](http://wrap.warwick.ac.uk/828/1/WRAP_Rourke_Equivariant_configuration.pdf))


See also

* [[Sadok Kallel]], _Particle Spaces on Manifolds and Generalized Poincaré Dualities_ ([arXiv:math/9810067](https://arxiv.org/abs/math/9810067)) 

* Shingo Okuyama, Kazuhisa Shimakawa, _Interactions of strings and equivariant homology theories_, ([arXiv:0903.4667](https://arxiv.org/abs/0903.4667))

For relation to [[instantons]] via [[topological Yang-Mills theory]]:

* {#AtiyahJones78} [[Michael Atiyah]], [[John David Stuart Jones]], _Topological aspects of Yang-Mills theory_, Comm. Math. Phys. Volume 61, Number 2 (1978), 97-118 ([arXiv:1103904210](https://projecteuclid.org/euclid.cmp/1103904210))

In speculation regarding [[Galois theory]] over the [[sphere spectrum]]:

* {#MoravaBeardsly17} [[Jack Morava]], [[Jonathan Beardsley]], _Toward a Galois theory of the integers over the sphere spectrum_,  Journal of Geometry and Physics Volume 131, September 2018, Pages 41-51 ([arXiv:1710.05992](https://arxiv.org/abs/1710.05992))


### Algebra structure over little $dim(X)$-disk operad
  {#ReferencesAlgebraStructureOverOperad}

The [[algebra over an operad|algebra]]-[[structure]] of configuration spaces over [[little n-disk operads]]/[[Fulton-MacPherson operads]]:

* {#Markl99} [[Martin Markl]], _A compactification  of  the  real  configuration  space  as  an  operadic completion, J. Algebra 215 (1999), no. 1, 185–204


* ...



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

* {#LambrechtsVolic14} [[Pascal Lambrechts]], [[Ismar Volić]], section 5 of _Formality of the little N-disks operad_, Memoirs of the American Mathematical Society ; no. 1079, 2014  ([arXiv"0808.0457](https://arxiv.org/abs/0808.0457), [doi:10.1090/memo/1079](http://dx.doi.org/10.1090/memo/1079))

This underlies the models of configuration spaces by [[graph complexes]], see there for more.



### Homology and cohomology 
 {#ReferencesCohomology}

General discussion of [[ordinary homology]]/[[ordinary cohomology]] of configuration spaces of points:

* {#Arnold69} [[Vladimir Arnold]], _The cohomology ring of the colored braid group_, Mat. Zametki, 1969, Volume 5, Issue 2, Pages 227–231 ([mathnet:mz6827](http://mi.mathnet.ru/eng/mz6827))

* {#Cohen73} [[Fred Cohen]], _Cohomology of braid spaces_, Bull. Amer. Math. Soc. Volume 79, Number 4 (1973), 763-766 ([euclid:1183534761](https://projecteuclid.org/euclid.bams/1183534761))

* [[Carl-Friedrich Bödigheimer]], [[Fred Cohen]], L. Taylor, _On the homology of configuration spaces_, Topology Vol. 28 No. 1, p. 111-123 1989 ([pdf](https://core.ac.uk/download/pdf/82124359.pdf))

* [[Yves Félix]], _Rational Betti numbers of configuration spaces_, Topology and its Applications, Volume 102, Issue 2, 8 April 2000, Pages 139-149 (<a href="https://doi.org/10.1016/S0166-8641(98)00148-5">doi:10.1016/S0166-8641(98)00148-5</a>)


* Thomas Church, _Homological stability for configuration spaces of manifolds_ ([arxiv:1602.04748](https://arxiv.org/abs/1602.04748))



* [[Ben Knudsen]], _Betti numbers and stability for configuration spaces via factorization homology_, Algebr. Geom. Topol. 17 (2017) 3137-3187 ([arXiv:1405.6696](https://arxiv.org/abs/1405.6696))

* Christoph Schiessl, _Betti numbers of unordered configuration spaces of the torus_ ([arxiv:1602.04748](https://arxiv.org/abs/1602.04748))

* Christoph Schiessl, _Integral cohomology of configuration spaces of the sphere_ ([arxiv:1801.04273](https://arxiv.org/abs/1801.04273))






### Cohomology modeled by graph complexes

That the [[de Rham cohomology]] of (the [[Fulton-MacPherson compactification]] of) configuration spaces of points may be modeled by [[graph complexes]] (exhibiting [[formality of the little n-disk operad]]) is due to

* {#Kontsevich99b} [[Maxim Kontsevich]], around Def. 15 and Lemma 3 in _Operads and Motives in Deformation Quantization_, Lett.Math.Phys.48:35-72,1999 ([arXiv:math/9904055](https://arxiv.org/abs/math/9904055))

nicely reviewed in [Lambrechts-Volic 14](#LambrechtsVolic14)


Further discussion of the graph complex as a model for the [[de Rham cohomology]] of  [[configuration spaces of points]] is in

* Najib Idrissi, _The Lambrechts-Stanley Model of Configuration Spaces_, Invent. Math, 2018 ([arXiv:1608.08054](https://arxiv.org/abs/1608.08054), [doi:10.1007/s00222-018-0842-9](https://dx.doi.org/10.1007/s00222-018-0842-9))

* {#CamposWillwacher16} [[Ricardo Campos]], [[Thomas Willwacher]], _A model for configuration spaces of points_ ([arXiv:1604.02043](https://arxiv.org/abs/1604.02043))

* [[Ricardo Campos]], Najib Idrissi, [[Pascal Lambrechts]], [[Thomas Willwacher]], _Configuration Spaces of Manifolds with Boundary_ ([arXiv:1802.00716](https://arxiv.org/abs/1802.00716))

* [[Ricardo Campos]], Julien Ducoulombier, Najib Idrissi, [[Thomas Willwacher]], _A model for framed configuration spaces of points_ ([arXiv:1807.08319](https://arxiv.org/abs/1807.08319))

### Homotopy

Discussion of [[homotopy groups]] of configuration spaces:

* {#Kohno02} [[Toshitake Kohno]], _Loop spaces of configuration spaces and finite type invariants_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arXiv:math/0211056](https://arxiv.org/abs/math/0211056))

* {#LambrechtsTourtchine09} [[Pascal Lambrechts]], [[Victor Tourtchine]], _Homotopy graph-complex for configuration and knot spaces_, Transactions of the AMS, Volume 361, Number 1, January 2009, Pages 207–222 ([arxiv:math/0611766](https://arxiv.org/abs/math/0611766))

### As moduli of Dp-D(p+4)-brane bound states:
 {#AsModuliOfD0D4BraneBoundStates}

Discussion of [[configuration spaces of points]] as [[moduli spaces]] of [[D0-D4-brane bound states]]

* [[Cumrun Vafa]], _Instantons on D-branes_, Nucl. Phys. B463 (1996) 435-442 ([arXiv:hep-th/9512078](https://arxiv.org/abs/hep-th/9512078))

with emphasis to the resulting [[configuration spaces of points]], as in

* [[Cumrun Vafa]], [[Edward Witten]], Section 4.1 of: _A Strong Coupling Test of S-Duality_, Nucl. Phys. B431:3-77, 1994 ([arXiv:hep-th/9408074](https://arxiv.org/abs/hep-th/9408074))




[[!redirects configuration space of points]]
[[!redirects configuration spaces of points]]

[[!redirects configuration space (mathematics)]]
[[!redirects configuration spaces (mathematics)]]


[[!redirects scanning map]]
[[!redirects scanning maps]]

[[!redirects scanning map equivalence]]
[[!redirects scanning map equivalences]]




