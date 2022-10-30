


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

[[fiber integration|Fiber integration]] in [[ordinary differential cohomology]] is the partial [[higher parallel transport|higher]] [[holonomy]] operation for [[circle n-bundles with connection]]:

for $Y \to X$ a [[bundle]] of [[compact space|compact]] [[smooth manifolds]] $S$ of [[dimension]] $k$ and $[\nabla] \in H_{diff}^n(Y)$ a class in [[ordinary differential cohomology]] of degree $n$ on $Y$, its [[fiber integration]]

$$
  \left[\exp(i \int_{Y/X} \nabla)\right] \in H^{n-k}_{diff}(X)
$$

is a differential cohomology class on $X$ of degree $k$ less.

In the particular case that $X = *$ is the [[point]] and $dim Y = k = n-1$ the element

$$
  \exp(i \int_{Y} \nabla) \in H^{1}_{diff}(*) \simeq U(1)
$$

is the [[higher parallel transport|higher]] [[holonomy]] of $\nabla$ over $Y$.


## Definition

### Differential orientation

The operation of [[fiber integration]] in [[generalized (Eilenberg-Steenrod) cohomology]] requires a choice of [[orientation in generalized cohomology]]. For fiber integration in [[differential cohomology]] this is to be refined to a _differential orientation_ .

Accordingly, instead of a [[Thom class]] there is a _differential Thom class_ .

+-- {: .num_defn #DifferentialThomCocycle}
###### Definition

For $X$ a [[compact space|compact]] [[smooth manifold]] and $V \to X$ a smooth real [[vector bundle]] of [[rank]] $k$ a **differential Thom cocycle** on $V$ is

* a [[compact support|compactly supported]] [[cocycle]] $\hat \omega$ in the [[ordinary differential cohomology]] of degree $k$ of $V$;

* such that for each $x \in X$ we have 
  
  $$
    \int_{V_x} \omega = \pm 1
    \,.
  $$

=--

+-- {: .num_remark}
###### Remark

The underlying class $[\hat \omega] \in H^{k}_{compact}(V, \mathbb{Z})$ in [[compact support|compactly supported]] [[integral cohomology]] is an ordinary [[Thom class]] for $V$.

=--

+-- {: .num_defn #DifferentialOrientation}
###### Definition

Let $p : X \to Y$ be a [[smooth function]] of [[smooth manifold]]s.

An **$H \mathbb{Z}_{diff}$-orientation** on $p$ is

1. A factorization through an [[embedding of smooth manifolds]] 

   $$
     p : X \hookrightarrow Y \times \mathbb{R}^N \stackrel{}{\to} Y
   $$

   for some $N \in \mathbb{N}$;

1. a [[tubular neighbourhood]] $W \hookrightarrow Y \times \mathbb{R}^N$ of $X$;

1. a differential Thom cocycle, def. \ref{DifferentialThomCocycle}, $U$ on $W \to X$.

=--

This appears as ([HopkinsSinger, def. 2.9](#HopkinsSinger)).


### Via differential Thom cocycles
 {#FiberIntegration}

Write $H^n_{diff}(-)$ for [[ordinary differential cohomology]]. For any choice of presentation, there is a fairly evident fiber integration of [[compact support|compactly supported]] [[cocycles]] along trivial [[Cartesian space]] bundles $Y \times \mathbb{R}^N \to Y$ over a [[compact space|compact]] $Y$:

$$
  \int_{\mathbb{R}^N} 
   : H^{n+N}_{diff,cpt}(Y \times \mathbb{R}^n)
  \to
  H^n_{diff}(Y)
  \,.
$$

+-- {: .num_defn}
###### Definition

Let $X \to Y$ be a [[smooth function]] equipped with differential $H\mathbb{Z}$-orientation $U$, def. \ref{DifferentialOrientation}. Then the corresponding **fiber integration** of ordinary differential cohomology is the composite

$$
  \int_{X/Y} :
   H_{diff}^{n+k}(X)
    \stackrel{(-)\cup U}{\to}
   H_{diff, cpt}^{n+N}(X \times \mathbb{R}^N)
    \stackrel{\int_{\mathbb{R}^N}}{\to}
   H_{diff}^n(Y)
  \,.
$$

=--

This appears as ([HopkinsSinger, def. 3.11](#HopkinsSinger)).

### In terms of Deligne cocycles

We discuss an explicit formula for fiber integration along [[product]]-bundles with [[compact topological space|compact]] [[fibers]] in terms of [[Deligne complex]], following ([Gomi-Terashima](#GomiTerashima)).

For $X$ a [[smooth manifold]], write $\mathbf{H}(X, \mathbf{B}^n U(1)_{conn})$ for the [[Deligne complex]] in degree $(n+1)$ over $X$.

+-- {: .num_defn}
###### Definition

Let $X$ be a [[paracompact topological space|paracompact]] [[smooth manifold]] and let $F$ be a [[compact topological space|compact]] [[smooth manifold]] of [[dimension]] $k$ without [[boundary]]. Then there is a morphism

$$
  \int_F 
    : 
  \mathbf{H}(X, \mathbf{B}^n U(1)_{conn})
    \to 
  \mathbf{H}(X, \mathbf{B}^{n-k} U(1)_{conn})
$$

given by (...)

=--

([Gomi-Terashima, section 2, corollary 3.2](#GomiTerashima))

## Properties

### General

(...)

### Abstract formulation

At least the fiber integration all the way to the point exists on general grounds for the <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos%20--%20structures#DifferentialCohomology">intrinsic differential cohomology</a> in any [[cohesive (∞,1)-topos]]: the general abstract formulation is in the section _<a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos%20--%20structures#ChernSimonsTheory">Higher holonomy and Chern-Simons functional</a>_ and the implementation in [[smooth ∞-groupoid]]s is in the section _<a href="http://nlab.mathforge.org/nlab/show/smooth+infinity-groupoid#StrucChernSimons">Smooth higher holonomy and Chern-Simons functional</a>_ .

## Related concepts

* [[higher parallel transport]], [[higher holonomy]]

## References

A discussion in the general sense of [[fiber integration]] in [[generalized (Eilenberg-Steenrod) cohomology]] is in section 3.4 of 

* [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_
 {#HopkinsSinger}

Explicit formulas for fiber integration of cocycles in [[Cech cohomology|Cech]]-[[Deligne cohomology]] are given in

* [[Kiyonori Gomi]] and Yuji Terashima, _A Fiber Integration Formula for the Smooth Deligne Cohomology_ International Mathematics Research Notices
2000, No. 13 ([pdf](http://imrn.oxfordjournals.org/content/2000/13/699.full.pdf))
 {#GomiTerashima}

* [[Kiyonori Gomi]] and Yuji Terashima, _Higher dimensional parallel transport_ Mathematical Research Letters 8, 25&#8211;33 (2001) ([pdf](http://mrlonline.org/mrl/2001-008-001/2001-008-001-004.pdf))

* [[Johan Dupont]], Rune Ljungmann, _Integration of simplicial forms and Deligne cohomology_ Math. Scand. 97 (2005), 11&#8211;39 ([pdf](http://www.mscand.dk/article.php?id=897))

[[!redirects differential Thom class]]