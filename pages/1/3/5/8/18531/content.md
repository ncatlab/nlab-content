

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _pullback_ of a [[distribution]] $u \in \mathcal{D}'(X)$ along a [[smooth function]] $f\colon Y \to X$ is supposed to like the [[composition]] $u \circ f$ if $u$ is thought of as a [[generalized function]], such that it is exactly this in the case that $u$ actually is an ordinary function. 


## Definition


+-- {: .num_prop #PullbackOfDistributionAlongSubmersion}
###### Proposition
**([[pullback of distributions]] along submersion)**

If $X_1, X_2 \subset \mathbb{R}^n$ are two [[open subsets]] of [[Euclidean space]], and if

$$
  f \;\colon\; X_1 \overset{}{\longrightarrow} X_2
$$

is a [[submersion]] (i.e. its [[differential]] is a [[surjective function]] $d f_x \;\colon\; T_x X_1 \to T_{f(x)} X_2$ for all $x \in X_1$), then there is a unique [[continuous linear functional]]

$$
  f^\ast \;\colon\; \mathcal{D}'(X_2) \longrightarrow \mathcal{D}'(X_1)
$$

between spaces of distributions ([this def.](distribution#DistributionOnOpenSubsetOfEuclideanSpace)) which extends the [[pullback of functions]] in that on a distribution represented by a [[bump function]] $b$ it is given by pre-[[composition]]

$$
  f^\ast b = b \circ f
  \,.
$$

This is hence called the _pullback of distributions_.

If $f$ happens to be a [[diffeomorphism]] with [[inverse function]] $f^{-1}$ then $f^\ast u$ for $u \in \mathcal{D}'(X_2)$ is explicitly given by

$$
  \langle  f^\ast u , b \rangle
  \;=\;
  \langle u, \frac{1}{det(D f)}  b \circ f^{-1} \rangle
$$

where $det(D f)$ denotes the [[Jacobian determinant]] (the [[determinant]] of the [[derivative]] of $f$).

=--

(e.g. [H&#246;rmander 90, theorem 6.1.2](#Hoermander90))


## Related concepts

* [[pullback of differential forms]]

* [[composition of distributions]]

* [[scaling degree of a distribution]]

## References


* {#Hoermander90} [[Lars Hörmander]], _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990

[[!redirects pullback of distributions]]
