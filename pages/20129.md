
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

A _normal framing_ is a [[trivial vector bundle|trivialization]] of a [[normal bundle]].

Specifically, if $X$ is a [[smooth manifold]] and $\Sigma \overset{\iota}{\hookrightarrow} X$ is a [[submanifold]], then a normal framing for $\Sigma$ is a [[trivial vector bundle|trivialization]] of the [[normal bundle]] $N_\iota(X)$.

A [[submanifold]] equipped with such normal framing is a _normally framed submanifold_ (e.g. [Kosinski 93, IX (2.1)](#Kosinski93)).


## Properties

### Pontryagin-Thom isomorphism

For $X$ a [[closed manifold|closed]] [[smooth manifold]] of [[dimension]] $D$, the [[Pontryagin-Thom construction]] (e.g. [Kosinski 93, IX.5](#Kosinski93)) identifies the [[set]] 

$$
  SubMfd_{/bord}^{d}(X)
$$

of [[cobordism classes]] of  [[closed manifold|closed]] and [[normally framed submanifolds]] $\Sigma \overset{\iota}{\hookrightarrow} X$ of [[dimension]] $d$ inside $X$ with the [[cohomotopy]] $\pi^{D-d}(X)$ of $X$ in degree $D- d$

$$
  SubMfd_{/bord}^{d}(X)
    \underoverset{\simeq}{PT}{\longrightarrow}
  \pi^{D-d}(X)
  \,.
$$

(e.g. [Kosinski 93, IX Theorem (5.5)](#Kosinski93))

In particular, by this [[bijection]] the canonical [[group]] [[structure]] on [[cobordism groups]] in sufficiently high [[codimension]] (essentially given by [[disjoint union]] of [[submanifolds]]) this way induces a group structure on the cohomotopy sets in sufficiently high degree.


## Related concepts

* [[framed manifold]]

## References

* {#Kosinski93} [[Antoni Kosinski]], chapter IX of _Differential manifolds_, Academic Press 1993 ([pdf](http://www.maths.ed.ac.uk/~v1ranick/papers/kosinski.pdf))


[[!redirects normal framings]]

[[!redirects normally framed submanifold]]
[[!redirects normally framed submanifolds]]


