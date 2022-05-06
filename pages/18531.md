

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

In general, the pullback of distributions along a smooth function $f$ is meant to be a unique extension to distributions of the operation which on [[bump functions]] is given by pre-composition with $f$. There are various different conditions that are sufficient for this being well defined.

If the map $f$ we are pulling back along is a [[submersion]], the all distributions pull back:

+-- {: .num_prop #PullbackOfDistributionAlongSubmersion}
###### Proposition
**(pullback of any distribution along a [[submersion]])**

If $X_1, X_2 \subset \mathbb{R}^n$ are two [[open subsets]] of [[Euclidean space]], and if

$$
  f \;\colon\; X_1 \overset{}{\longrightarrow} X_2
$$

is a [[submersion]] (i.e. its [[differential]] is a [[surjective function]] $d f_x \;\colon\; T_x X_1 \to T_{f(x)} X_2$ for all $x \in X_1$), then there is a unique [[continuous linear functional]]

$$
  f^\ast \;\colon\; \mathcal{D}'(X_2) \longrightarrow \mathcal{D}'(X_1)
$$

between spaces of distributions ([this def.](distribution#DistributionOnOpenSubsetOfEuclideanSpace)) which extends the [[pullback of functions]] in that on a [[non-singular distribution]] represented by a [[bump function]] $b$ it is given by pre-[[composition]]

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

([H&#246;rmander 90, theorem 6.1.2](#Hoermander90), [Melrose 03, sections 4.17, 4.19 and 4.21](#Melrose03))

If $f$ is not a submerision, then pullback is still defined on those distributions whose [[wave front set]] does not intersect the [[conormal bundle]] of $f$:

+-- {: .num_defn #PullbackOfDistributionsWhoseWaveFrontDoesNotIntersectNormalBundle}
###### Proposition
**(pullback if [[wave front set]] is [[disjoint subset|disjoint]] from [[conormal bundle]])**

Given a [[smooth function]] $f \colon X \to Y$, then there is a unique [[continuous linear functional]] $f^\ast$ from the space of those distributions on $Y$ whose [[wave front set]] does not intersect the [[conormal bundle]] of $f$

$$
  f^\ast 
   \;\colon\;
  \left\{
    u \in \mathcal{D}'(Y) \;\vert\; WF(u) \cap N^\ast_f = \emptyset
  \right\}
    \longrightarrow
  \mathcal{D}'(X)
$$

such that 

1. on [[non-singular distributions]] $u_g$ corresponding to [[smooth functions]] $g \colon Y \to \mathbb{C}$ it acts by [[precomposition]] with $f$:

   $$
     f^\ast (u_g) = u_{g \circ f}
   $$

1. for $u$ a distribution in the domain on the left, the [[wave front set]] of its pullback is inside the pullback of its wave front set

  $$
    \label{WaveFrontSetOfPullbackDistributionIsInsidePullbackOfWaveFrontSet}
    WF(f^\ast u)
    \subset
    f^\ast WF(u)
    \coloneqq
    \left\{ 
      (x, (d f(x))^\ast k)
      \;\vert\;
      ( f(x), \eta )
      \in 
      WF(u)
    \right\}
  $$


=--

([Hörmander 90, theorem 8.2.4](#Hoermander90))

## Properties

* for continuity see at _[[Hörmander topology]]_


## Examples

+-- {: .num_example #RestrictionOfDistributions}
###### Example
**(restriction of distributions)**

Let $i \;\colon\; Y \hookrightarrow X$ be an [[open subset]] inclusion. This is clearly a [[submersion]], in fact a [[local diffeomorphism]], and hence prop. \ref{PullbackOfDistributionAlongSubmersion} applies. The resulting pullback operation

$$
  i^\ast \;\colon\; \mathcal{D}'(Y) \longrightarrow \mathcal{D}'(X)
$$

is also called _restriction of distributions_ ([H&#246;rmander 90, first lines of section 2.2](#Hoermander90)). For $b \in C^\infty_c(Y)$ a [[bump function]] on $Y$, the restriction $i^\ast u$ of a distribution $u \in \mathcal{D}'(X)$ acts by

$$
  \langle i^\ast u, b\rangle = \langle  u, i_\ast b \rangle
  \,,
$$

where $i_\ast b \in C^\infty_{cp}(X)$ is the result of [[extension|extending]] $b$ by zero to all of $X$.


=--



## Related concepts

* [[change of integration variables]]

* [[composition of distributions]]

* [[scaling degree of a distribution]]

* [[extension of distributions]]

* [[support of a distribution]]

[[!include notions of pullback -- contents]]



## References


* {#Hoermander90} [[Lars Hörmander]], _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990

* {#Melrose03} [[Richard Melrose]], sections 4.17, 4.19 and 4.21 of _Introduction to microlocal analysis_, 2003 ([pdf](http://www-math.mit.edu/~rbm/iml90.pdf))

* [[Sergiu Klainerman]], chapter 3, section 4 of _Lecture notes in analysis_, 2011 ([pdf](https://web.math.princeton.edu/~seri/homepage/courses/Analysis2011.pdf))

[[!redirects pullbacks of a distribution]]

[[!redirects pullback of distributions]]
[[!redirects pullbacks of distributions]]

[[!redirects restriction of a distribution]]
[[!redirects restrictions of a distribution]]


[[!redirects restriction of distributions]]
[[!redirects restrictions of distributions]]

