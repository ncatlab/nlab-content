
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

On a [[space]] of suitable even [[dimension]] the _[[cup product]]_ on suitable mid-dimensional [[cohomology]] is often called the _intersection product_ -- this, or its evaluation on the [[fundamental class]] of the whole space.

Under [[Poincaré duality]] these cohomology classes may correspond to [[cycles]] and then under suitable conditions or in a suitable sense, the cup product dually counts (or otherwise detects) literally the [[intersection]] points of the two subspaces, whence the name. It is the topic of _[[intersection theory]]_ to make this statement precise, classical results to this extent include [[Bézout's theorem]] and its refinement to the [[Serre intersection formula]].

If here [[cohomology]] is replaced by [[differential cohomology]] then [[quadratic refinements]] of the intersection product provide the [[Lagrangians]] for [[higher dimensional Chern-Simons theory]] and govern the structure of [[self-dual higher gauge theory]]. See there for more.


In a little more detail:  For $X$ a [[space]] of [[dimension]] $2k$ and $H^k(X)$ a [[cohomology group]] on a space $X$ equipped with [[orientation in generalized cohomology|H-orientation]] in degree $k$ with coefficients in some $A$, the **intersection pairing** on [[cohomology]] is the map

$$
  H^k(X) \times H^k(X) \to A
$$

given by [[fiber integration]]

$$
  (\lambda, \omega) \mapsto \int_X (\lambda \cup \omega)
  \,,
$$

of the [[cup product]]

$$
  \cup : H^k(X) \times H^k(X) \to H^{2k}(X)
  \,.
$$



## Examples

### In integral cohomology

The [[signature of a quadratic form]] of the [[quadratic form]] induced by the intersection pairing in [[integral cohomology]] is the _[[signature genus]]_.

In dimension 4, see also:

* Wikipedia, _[Intersection form (4-manifold)](http://en.wikipedia.org/wiki/Intersection_form_%284-manifold%29)_.

### In $\mathbb{Z}_2$-cohomology

Over a [[Riemann surface]] $X$, the intersection pairing on $H^1(X, \mathbb{Z}_2)$ has a [[quadratic refinement]] by the function that sends a [[Theta characteristic]] to the mod 2-dimension of its space of sections. See _[Theta characteristic -- Over Riemann surfaces](Theta+characteristic#OverRiemannSurfaces)_.

### In ordinary differential cohomology: higher abelian Chern-Simons theory
 {#SecondaryIntersectionPairing}

For the case that the cohomology in question is [[ordinary differential cohomology]], 

* a [[cocycle]] in degree $k$ is a [[circle n-bundle with connection|circle (k-1)-bundle with connection]], 

* the cup product is the [[Beilinson-Deligne cup product]];

* and the required notion of orientation is now _[[orientation in differential cohomology]]_: a [[differential Thom class]].  

The differentially refined intersection pairing is non-trivial and interesting also on manifolds of dimension less than $2k$, where the integral intersection pairing vanishes: it provides a _[[secondary characteristic class]]_, a **secondary intersection pairing**.

Notably, the [[diagonal]] of the intersection pairing in in dimension $2k-1$ is the [[action functional]] of quadratic abelian [[higher dimensional Chern-Simons theory]].

Its [[quadratic refinement]] is discussed in 
([Hopkins-Singer](#HopkinsSinger)), induced from/modeled on [[characteristic elements of a bilinear form|characteristic elements]] given by [[integral Wu structures]].

### On framed manifolds

On a [[framed manifold]] the intersection pairing has a canonical [[quadratic refinement]], leading to the [[Kervaire invariant]].

## Related concepts

* [[functional cup product]]

* [[homotopy Whitehead integral formula]]

[[!include quadratic invariants - table]]

[[!include square roots of line bundles - table]]


## References

Introductions and surveys include

* [[Akhil Mathew]], _Intersection theory on surfaces_, 2013 ([web](http://amathew.wordpress.com/2013/01/27/intersection-theory-on-surfaces/))

* Wikipedia, _[Intersection theory](http://en.wikipedia.org/wiki/Intersection_theory)_

Discussion of the intersection pairing in [[ordinary differential cohomology]] and especially its [[quadratic refinement]] is in 

* {#HopkinsSinger} [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_
 

[[!redirects intersection pairings]]

[[!redirects secondary intersection pairing]]
[[!redirects secondary intersection pairings]]

[[!redirects intersection product]]
[[!redirects intersection products]]

[[!redirects intersection number]]
[[!redirects intersection numbers]]
