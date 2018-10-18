
> This entry is about the concept of subspaces of [[vector bundles]] and [[Lie algebroids]]. For the concept in functional analysis see at _[[distribution]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Let $p:V\to M$ be a [[smooth vector bundle]]. Any smooth family of $k$-dimensional subspaces $W_m\subset p^{-1}(m)$ where $m\in M$ is called a _[[distribution of subspaces|distribution of k-dimensional subspaces]]_ in $V\to M$. If $V = T M$ is the [[tangent bundle]] of $M$ then we talk about distributions of tangent vectors. 

A distribution of [[tangent vectors]] is called _integrable_ if the [[Lie bracket]] of its [[sections]] is **involutive**, i.e. if $X,Y: M\to W\subset T M$ are two sections (vector fields belonging to the distribution) of $W\to M$ then the bracket $[X,Y]$ of these vector fields is also a section of $W$: $[X,Y]\in W$. 

More generally, if a vector bundle is equipped with the structure of a [[Lie algebroid]], then a [[distribution of subspaces]] is _integrable_ if its sections are closed under the given Lie bracket. This reduces to the previous case for the [[tangent Lie algebroid]]. Hence *integrable distributions are [[subobject|sub-]]Lie algebroids*. 

## Properties

A basic result on integrability is the Frobenius theorem ([Wikipedia](http://en.wikipedia.org/wiki/Frobenius_theorem_%28differential_topology%29)) which relates involutivity to integrability in the sense of partial differential equations. Examples include complex analytic manifolds which correspond exactly to complex manifolds with an integrable almost complex structure. [[Courant algebroid]]s are a quite general tool to express the integrability of geometric structure that include these as special cases.   

## Related concepts

* [[foliation]] 

  * [[foliation of a Lie algebroid]]

  * [[foliation of a Lie groupoid]]

* [[polarization]]

* [[exterior differential system]]

[[!redirects integrable distributions]]

[[!redirects integrable distribution]]
[[!redirects integrable distributions]]
