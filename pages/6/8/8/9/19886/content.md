

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Goodwillie calculus
+--{: .hide}
[[!include Goodwillie calculus - contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea


The [[stabilization]]/[[suspension spectrum]] $\Sigma^\infty  Maps(X,A)$ of  [[mapping spaces]] $Maps(X,A)$ between suitable [[CW-complexes]] $X, A$ happens to decompose as a [[direct sum]] of [[spectra]] (a [[wedge sum]]) in a useful way, related to the expression of the [[Goodwillie derivatives]] of the functor $Maps(X,-)$ and often expressible in terms of the [[configuration space (mathematics)|configuration spaces]] of $X$.

## Definition
 {#Definition}

The stable splitting of mapping spaces discussed [below](#StableSplittings) have summands given by [[configuration spaces of points]], or generalizations thereof. To be self-contained, we recall the relevant definitions here.

The following Def. \ref{ConfigurationSpacesOfnPoints} is not the most general definition of [[configuration spaces of points]] that one may consider in this context, instead it is streamlined to certain applications. See Remark \ref{ComparisonToNotationInLiterature} below for comparison of notation used here to notation used elsewhere.

+-- {: .num_defn #ConfigurationSpacesOfnPoints}
###### Definition
**([[configuration spaces of points]])**

Let $X$ be a [[manifold]], possibly with [[manifold with boundary|boundary]].



For $n \in \mathbb{N}$, the _**configuration space of $n$ distinguishable points** in $X$ disappearing at the boundary_ is the [[topological space]]

\[
    \label{DistinguishableConfigurationSpaceJustForX}
    \mathrm{Conf}^{ord}_{n}(X)
    \;\coloneqq\;
      \big(
        X^n \setminus \mathbf{\Delta}_X^n
      \big)
      / \partial(X^n)
\]

which is the [[complement]] of the [[fat diagonal]] $\mathbf{\Delta}_X^n \coloneqq \{(x^i) \in X^n | \underset{i,j}{\exists} (x^i = x^j) \}$ inside the $n$-fold [[product space]] of $X$ with itself, followed by [[quotient space|collapsing]] any configurations with elements on the [[boundary]] of $X$ to a common [[pointed topological space|base point]].

Then the _**configuration space of $n$ in-distinguishable points** in $X$ is the further [[quotient topological space]]

  \[
    \label{ConfigurationSpaceJustForX}
    \mathrm{Conf}_{n}(X)
    \;\coloneqq\;
    Conf_n^{ord}(X)/\Sigma_n
    \;=\;
    \Big(
      \big(
        X^n \setminus \mathbf{\Delta}_X^n
      \big)
      / \partial(X^n)
    \Big)
    /\Sigma(n)
    \,,
  \]

where $\Sigma(n)$ denotes the evident [[action]] of the [[symmetric group]] by [[permutation]] of factors of $X$ inside $X^n$.
  
  More generally, let $Y$ be another [[manifold]], possibly with [[manifold with boundary|boundary]]. For $n \in \mathbb{N}$, the _**configuration space of $n$ points** in $X \times Y$ vanishing at the boundary and distinct as points in $X$_ is the [[topological space]]

  \[
    \label{ConfigurationSpaceWithXAndY}
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
    / \partial(X^n \times Y^n)
    \Big)
    /\Sigma(n)
  \]

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



+-- {: .num_remark #ComparisonToNotationInLiterature}
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
  Y / \partial Y \coloneqq Y \underset{\partial Y}{\sqcup} \ast
$$
 
is $Y$ with a [disjoint basepoint attached](pointed+topological+space#ForgettingAndAdjoiningBasepoints). Notably for $Y =\ast$ the [[point space]], we have that 

$$
  \ast/\partial \ast = S^0
$$

is the [[0-sphere]].


=--

## Statements
 {#Statements}

### Prelude: Equivalence to the infinite configuration space

First recall the following equivalence already before [[stabilization]]:

+-- {: .num_prop #ScanningMapEquivalenceOverCartesianSpace}
###### Proposition

For 

1. $d \in \mathbb{N}$, $d \geq 1$ a [[natural number]] with $\mathbb{R}^d$ denoting the [[Cartesian space]]/[[Euclidean space]] of that [[dimension]],

1. $Y$ a [[manifold]], with [[inhabited set|non-empty]] [[manifold with boundary|boundary]] so that  $Y / \partial Y$ is [[connected topological space|connected]],

the [[scanning map]] constitutes a [[homotopy equivalence]]

$$
  Conf\left( 
    \mathbb{R}^d, Y
  \right)
  \overset{scan}{\longrightarrow}
  \Omega^d \Sigma^d (Y/\partial Y)
$$

between 

1. the configuration space of arbitrary points in $\mathbb{R}^d \times Y$ vanishing at the boundary (Def. \ref{ConfigurationSpacesOfnPoints}) 

1. the $d$-fold [[loop space]] of the $d$-fold [[reduced suspension]] of the [[quotient space]] $Y / \partial Y$ (regarded as a [[pointed topological space]] with basepoint $[\partial Y]$).

In particular when $Y = \mathbb{D}^k$ is the [[closed ball]] of [[dimension]] $k \geq 1$ this gives a [[homotopy equivalence]]

$$
  Conf\left( 
    \mathbb{R}^d, \mathbb{D}^k
  \right)
  \overset{scan}{\longrightarrow}
  \Omega^d S^{ d + k }
$$

with the $d$-fold [[loop space]] of the [[n-sphere|(d+k)-sphere]].

=--

([May 72, Theorem 2.7](#May72),  [Segal 73, Theorem 3](#Segal73))


### Stable splitting of mapping spaces
 {#StableSplittings}

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

Combined with the [[stabilization]] of the [[scanning map]] [[homotopy equivalence]] from Prop. \ref{ScanningMapEquivalenceOverCartesianSpace} this yields a [[stable weak homotopy equivalence]]

\[
  \label{StableSplittingOfMappingSpacesOutOfSphere}
  Maps_{cp}(\mathbb{R}^d, \Sigma^d (Y / \partial Y))
  =
  Maps^{\ast/}( S^d, \Sigma^d (Y / \partial Y))
  =
  \Omega^d \Sigma^d (Y/\partial Y)
  \underoverset{\Sigma^\infty scan}{\simeq}{\longrightarrow}
  \Sigma^\infty Conf(\mathbb{R}^d, Y)
  \overset{\simeq}{\longrightarrow}
  \underset{n \in \mathbb{N}}{\oplus} \Sigma^\infty Conf_n(\mathbb{R}^d, Y)
\]

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

### In terms of Goodwillie-Taylor towers
 {#InTermsOfGoodwillieTowers}

We discuss the interpretation of the above stable splitting of mapping spaces from the point of view of [[Goodwillie calculus]], following [Arone 99, p. 1-2](#Arone99), [Goodwillie 03, p. 6](#Goodwillie03).

Observe that the [[configuration space of points]] $Conf_n(X,Y)$ from Def. \ref{ConfigurationSpacesOfnPoints}, given by the formula (eq:ConfigurationSpaceWithXAndY)

$$
  Conf_n(X,Y)
  \;\coloneqq\;
  \Big(
    \big(
      (
        X^n \setminus \mathbf{\Delta}_X^n
      )
      \times
      Y^n
    \big)
    / \partial(X^n \times Y^n)
  \Big)
  /\Sigma(n)
$$

is the [[quotient]] by the [[symmetric group]]-[[action]] of the _[[smash product]]_ $Conf_n(X) \wedge (Y/\partial Y)^n$ of the plain Configuration space $Conf_n(X)$  (eq:ConfigurationSpaceJustForX) (regarded as a [[pointed topological space]] with basepoint the class of the [[boundary]] $\left[\partial\left(X^n\right)\right]$) with the analogous [[pointed topological space]] given by $Y$, the latter in fact being (since here we do not form the [[complement]] by the [[fat diagonal]]) an $n$-fold [[smash product]] itself:

$$
  Y^{\times_n}/\partial (Y^{\times_n}) 
  \;\simeq\;
  ( Y/\partial Y )^{\wedge_n}
  \,.
$$

Hence in summary:

\[
  \label{ConfSplitsAsSmashProduct}
  Conf_n(X, Y)
  \;\simeq\;
  Conf^{ord}_n(X) \wedge_{\Sigma(n)} \left( Y/\partial Y \right)^{\wedge_n}
  \,,
\]

where 

$$
  Conf_n^{ord}(X)
  \;\coloneqq\;
  \left(
    X^{\times_n} \setminus \mathbf{\Delta}_X^n
  \right)/ \partial(X^n)
$$

is the ordered configuration space (eq:DistinguishableConfigurationSpaceJustForX).

This construction, regarded as a [[functor]] from [[pointed topological spaces]] to [[spectra]]

$$
  \array{
    Top^{\ast/} 
    &\longrightarrow&
    Spectra
    \\
    Z 
      &\mapsto&
    \Sigma^\infty Conf^{ord}_n(X) \wedge_{\Sigma(n)} Z^{\wedge_n}
  }
$$

is an [[n-homogeneous (∞,1)-functor]] in the sense of [[Goodwillie calculus]], and hence the partial [[wedge sums]] as $n$ ranges

\[
  \label{IdentifyingTheGoodwillieTaylorStage}
  Z 
    \;\mapsto\;
  \underset{k \in \{1, \cdot, n\}}{\bigoplus}
  \Sigma^\infty Conf^{ord}_k(X) \wedge_{\Sigma(k)} Z^{\wedge_k}
\]

are [[n-excisive (∞,1)-functors]]. Moreover, by the stable splitting of mapping spaces (eq:StableSplittingOfMappingSpacesOutOfSphere) of Prop. \ref{StableSplittingOfMappingSpacesOutOfEuclideanSpace}, there is a [[projection]] morphism onto the first $n$ [[wedge sum|wedge summands]]

\[
  \label{ProjectionMaps}
  \array{
    Maps_{cp}(\mathbb{R}^d, \Sigma^d Z)
    &=&
    Maps^{\ast/}( S^d, \Sigma^d Z)
    &\simeq&
    \underset{k \in \mathbb{N}}{\oplus} 
      \Sigma^\infty Conf^{ord}_k(\mathbb{R}^d) \wedge_{\Sigma(k)} Z^{\wedge_k}
    \\
    &&
    &&
    \Big\downarrow {}^{\mathrlap{ p_n }}
    \\
    &&
    &&
     \underset{k \in \{1, \cdot, n\}}{\bigoplus}
     \Sigma^\infty Conf^{ord}_k( \mathbb{R}^d ) \wedge_{\Sigma(k)} Z^{\wedge_k}
  }
\]

and this is [[n-connected morphism|(n+1)k-connected]] when $Z$ is [[n-connected object|k-connected]]. 

By [[Goodwillie calculus]] this means that (eq:IdentifyingTheGoodwillieTaylorStage) are, up to [[equivalence in an (infinity,1)-category|equivalence]], the stages 

\[
  \label{TheGoodwillieStagesOfTheMappingSpaceFunctor}
  P_n Maps^{\ast/}( S^d, \Sigma^d (-))
  \;\colon\;
  Z \mapsto
  \underset{k \in \{1, \cdot, n\}}{\bigoplus}
  \Sigma^\infty Conf^{ord}_k(S^d, Z) 
\]

at $Z \in Top^{\ast/}$ of the [[Goodwillie-Taylor tower]] for the [[mapping space]]-functor 

$$
  Maps_{cp}(\mathbb{R}^d, \Sigma^d (-))
  =
  Maps^{\ast/}( S^d, \Sigma^d (-))
  \;\colon\;
  Top^{\ast/} \longrightarrow Top^{\ast/}
  \,.
$$

Therefore the stable splitting theorem \ref{StableSplittingOfMappingSpacesOutOfEuclideanSpace} may equivalently be read as expressing the mapping space functor equivalently as the [[limit]] over its [[Goodwillie-Taylor tower]].

([Arone 99, p. 1-2](#Arone99), [Goodwillie 03, p. 6](#Goodwillie03))


$\,$

### Lax closed structure on $\Sigma^\infty$ 

Notice that the first stage in the [[Goodwillie-Taylor tower]] of $Maps(S^d, \Sigma^d(-))$ is

$$
  \begin{aligned}
    P_1 Maps^{\ast/}( S^d, \Sigma^d (Y / \partial Y) )
    & =
    \Sigma^\infty Conf^{ord}_1( \mathbb{R}^d , Y )
    \\
    & \simeq
    \Sigma^\infty 
      \underset{\simeq S^0}{\underbrace{Conf^{ord}_1( \mathbb{R}^d )}} 
      \wedge (Y/\partial Y)
    \\
    & \simeq
     \Sigma^\infty (Y/\partial Y)
    \\
    & \simeq 
     \Omega^d \Sigma^d  \Sigma^\infty (Y/\partial Y)
    \\
    & \simeq
    Maps\left(  \Sigma^\infty S^d, \Sigma^d (Y/\partial Y) \right)
  \end{aligned}
$$

Here in the first step we used (eq:TheGoodwillieStagesOfTheMappingSpaceFunctor), in the second step we used (eq:ConfSplitsAsSmashProduct). Under the brace we observe that space of configurations of a single point in $\mathbb{R}^d$ is trivially $\mathbb{R}^d$ itself, which is [[contractible topological space|contractible]] $\mathbb{R}^d \simeq \ast$ and, due to [[empty set|empty]] [[boundary]] of $\mathbb{R}^d$, contributes a [[0-sphere]]-factor to the [[smash product]], which disappears. In the last last two steps we trivially rewrote the result to exhibit it as a [[mapping spectrum]].

Therefore the projection $p_1$ (eq:ProjectionMaps) to the first stage of the [[Goodwillie-Taylor tower]] is of the form

$$
  p_1
  \;\colon\;
  \Sigma^\infty Maps\left(  S^d , \Sigma^d (Y /\partial Y) \right)
  \longrightarrow
  Maps
  \left(  
    \Sigma^\infty S^d, \Sigma^\infty \Sigma^d (Y / \partial Y)
  \right)
  \,.
$$

Since $\Sigma^\infty$ is a [[strong monoidal functor]] ([here](suspension+spectrum#StrongMonoidalness)), there is a canonical comparison morphism of this form, exhibiting the induce [[closed functor|lax closed]]-structure on $\Sigma^\infty$. Probably $p_1$ coincides with that canonical morphism, up to equivalence.

> Does it?

## Related concepts

* [[mapping spectrum]]

## References

The theorem is originally due to 

* {#Snaith74} [[Victor Snaith]],  _A stable decomposition of $\Omega^n S^n X$_, Journal of the London Mathematical Society 7 (1974), 577 - 583 ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/snaiths.pdf))

using the homotopy equivalence before stabilization due to 

* {#May72} [[Peter May]], _The geometry of iterated loop spaces_, Springer 1972 ([pdf](https://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf))

* {#Segal73} [[Graeme Segal]], _Configuration-spaces and iterated loop-spaces_, Invent. Math. __21__ (1973), 213&#8211;221. MR 0331377 ([pdf](http://dodo.pdmi.ras.ru/~topology/books/segal.pdf))

An alternative proof is due to 

* {#Cohen80} [[Ralph Cohen]], _Stable proof of stable splittings_, Math. Proc. Camb. Phil. Soc., 1980, 88, 149 ([doi:10.1017/S030500410005742X](https://doi.org/10.1017/S030500410005742X), [pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/247D9F951F8AB99000E4FF6CB2DB9EA2/S030500410005742Xa.pdf/div-class-title-stable-proofs-of-stable-splittings-div.pdf))

Review and generalization is due to 

* {#Boedigheimer87} [[Carl-Friedrich Bödigheimer]], _Stable splittings of mapping spaces_, Algebraic topology. Springer 1987. 174-187 ([pdf](http://www.math.uni-bonn.de/~cfb/PUBLICATIONS/stable-splittings-of-mapping-spaces.pdf))

Interpretation in terms of the [[Goodwillie-Taylor tower]] of mapping spaces is due to

* {#Arone99} [[Greg Arone]], _A generalization of Snaith-type filtration_, Transactions of the American Mathematical Society 351.3 (1999): 1123-1150. ([pdf](https://www.ams.org/journals/tran/1999-351-03/S0002-9947-99-02405-8/S0002-9947-99-02405-8.pdf))

* {#Ching05} [[Michael Ching]], _Calculus of Functors and Configuration Spaces_, Conference on Pure and Applied Topology Isle of Skye, Scotland, 21-25 June, 2005 ([pdf](https://www3.amherst.edu/~mching/Work/skye.pdf))

* {#Goodwillie03} [[Thomas Goodwillie]], p. 6 of _Calculus. III. Taylor series_, Geom. Topol. 7 (2003), 645--711 ([journal](http://www.msp.warwick.ac.uk/gt/2003/07/p019.xhtml), [arXiv:math/0310481](http://arxiv.org/abs/math/0310481)))

A proof via [[nonabelian Poincaré duality]]:

* Lauren Bandklayder, _Stable splitting of mapping spaces via nonabelian Poincaré duality_ ([arxiv:1705.03090](https://arxiv.org/abs/1705.03090))

See also:

* [[Douglas Ravenel]], *What we still don't understand about loop spaces of spheres*, Contemporary Mathematics 1998 ([pdf](https://people.math.rochester.edu/faculty/doug/mypapers/loop.pdf), [[Ravenel_LoopSpacesOfSpheres.pdf:file]])



[[!redirects stable splittings of mapping spaces]]
