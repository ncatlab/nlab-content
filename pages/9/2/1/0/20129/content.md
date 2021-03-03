

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

A _normal framing_ is a [[trivial vector bundle|trivialization]] of a [[normal bundle]].

Specifically, if $X$ is a [[smooth manifold]] and $\Sigma \overset{\iota}{\hookrightarrow} X$ is a [[submanifold]], then a normal framing for $\Sigma$ is a [[trivial vector bundle|trivialization]] of the [[normal bundle]] $N_\iota(X)$.

A [[submanifold]] equipped with such normal framing is a _normally framed submanifold_ ([Pontrjagin 55, Sec. 6](#Pontrjagin55) e.g. [Kosinski 93, IX (2.1)](#Kosinski93)). Beware that this is often called just a _framed submanifold_, despite the potential class with "[[framed manifold]]".


## Properties

### Pontryagin's theorem

For $X$ a [[closed manifold|closed]] [[smooth manifold]] of [[dimension]] $D$, the [[Pontryagin theorem]] (e.g. [Kosinski 93, IX.5](#Kosinski93)) identifies the [[set]] 

$$
  Cob_{Fr}^{d}(X)
$$

of [[cobordism classes]] of  [[closed manifold|closed]] and [[normally framed submanifolds]] $\Sigma \overset{\iota}{\hookrightarrow} X$ of [[dimension]] $d$ inside $X$ with the [[cohomotopy]] $\pi^{D-d}(X)$ of $X$ in degree $D- d$

$$
  Cob_{Fr}^{d}(X)
    \underoverset{\simeq}{PT}{\longrightarrow}
  \pi^{D-d}(X)
  \,.
$$

(e.g. [Kosinski 93, IX Theorem (5.5)](#Kosinski93))

In particular, by this [[bijection]] the canonical [[group]] [[structure]] on [[cobordism groups]] in sufficiently high [[codimension]] (essentially given by [[disjoint union]] of [[submanifolds]]) this way induces a group structure on the cohomotopy sets in sufficiently high degree.


## Related concepts

* [[framed manifold]]

* [[normal twisted framing]]

## References

* {#Pontrjagin38} [[Lev Pontrjagin]], _[[Classification of continuous maps of a complex into a sphere]]_, Dokl. Akad. Nauk SSSR 19 (1938), 361-363

* {#Pontrjagin55} [[Lev Pontrjagin]], Section 6 of: _[[Smooth manifolds and their applications in homotopy theory]]_, Trudy Mat. Inst. im Steklov, No 45, Izdat. Akad. Nauk. USSR, Moscow, 1955, AMS Translation Series 2, Vol. 11, 1959 ([doi:10.1142/9789812772107_0001](https://www.worldscientific.com/doi/abs/10.1142/9789812772107_0001), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/pont001.pdf))


* {#Kosinski93} [[Antoni Kosinski]], chapter IX of _Differential manifolds_, Academic Press 1993 ([pdf](http://www.maths.ed.ac.uk/~v1ranick/papers/kosinski.pdf))


[[!redirects normal framings]]

[[!redirects normally framed submanifold]]
[[!redirects normally framed submanifolds]]

[[!redirects framed submanifold]]
[[!redirects framed submanifolds]]

