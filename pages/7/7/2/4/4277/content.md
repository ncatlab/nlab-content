
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **cobordism ring** $\Omega_*=\oplus_{n\geq 0}\Omega_n$ is the [[ring]] whose 

* degree $n$ elements are classes of $n$-dimensional [[manifold]]s modulo [[cobordism]]s;

* product operation is given by the [[Cartesian product]] of manifolds;

* addition operation is given by the [[disjoint union]] of manifolds.

Instead of bare manifolds one can consider manifolds with extra structure, such as [[orientation]], [[spin structure]], [[string structure]], etc. and accordingly there is _oriented cobordism ring_ $\Omega^{SO}_*$,  the _spin cobordism ring_ $\Omega^{Spin}_*$, etc. In this context the bare cobordism ring is also denoted $\Omega^O_*$ or $\Omega^{un}_*$.

A ring [[homomorphism]] out of the cobordism ring is a [[genus]].

For $T$ a fixed [[manifold]] there is a relative version $\Omega_\bullet(T)$ of the cobordism ring: 

* elements are classes modulo cobordism over $T$ of manifolds equipped with [[smooth function]]s to $T$;

* multiplication of $[f : X \to T]$ with $[g : Y \to T]$ is given by _transversal intersection_ $X \cap_T Y$ over $T$: perturb $f$ such $(f',g)$ becomes [[transversal maps]] and then form the [[pullback]] $X \times_{(f',g)} Y$ in [[Diff]].

This product is graded in that it satisfies the **dimension formula**

$$
  (dim T - dim X) + (dim T - dim Y) = dim T - dim (X \cap_T Y)
$$

hence

$$
  dim (X \cap_T Y ) = (dim X + dim Y) - dim T
  \,.
$$

## Properties

### Relation to cobordism cohomology theory

See _[[cobordism cohomology theory]]_.

### Relation to higher category theory

The cobordism ring finds its natural interpretation in [[higher category theory]].

+-- {: .num_theorem}
###### Theorem
**(Thom)**

The degree $n$ component $\Omega_n$ of the cobordism ring $\Omega_*$ is the $n$th [[homotopy group]] of the [[Thom spectrum]] $M O$

$$
  \Omega^O_n \simeq \pi_n (M O)
$$

=--

The [[Thom spectrum]] $M O$ is a connected [[spectrum]] hence essentially a [[symmetric monoidal (infinity,1)-category|symmetric monoidal]] [[∞-groupoid]] ([[infinite loop space]]) $\Omega^\infty M O$. 

By one aspect of the (proof of the) [[cobordism hypothesis]]-theorem, this is the [[(∞,n)-category of cobordisms]] for $n \to \infty$

$$
  Bord_{(\infty,\infty)} \simeq \Omega^\infty M O
  \,.
$$

Really on the left we have the $\infty$-groupoidification of that [[∞-category]], but since $Bord_{(\infty,\infty)}$ has duals for [[k-morphism]]s for _all_ $k$, it is already itself an $\infty$-groupoid: the [[Thom spectrum]]. See ([Francis](#Francis)).

Hence the cobordism ring in degree $n$ is the [[decategorification]] of the $n$-fold [[loop space object|looping]] of the $\infty$-category of cobordisms.

## Examples

### Oriented cobordism
 {#OrientedCobordismRing}

+-- {: .num_prop #OrientedCobordismOverPoint}
###### Proposition

The cobordism ring over the point for [[orientation|oriented]] manifolds starts out as

| $k$             | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | $\geq 9$ |
|-----------------|---|---|---|---|---|---|---|---|---|---|
| $\Omega^{SO}_k$ | $\mathbb{Z}$ | 0 | 0 | 0 | $\mathbb{Z}$ | $\mathbb{Z}_2$ | 0 | 0 | $\mathbb{Z}\oplus \mathbb{Z}$ | $\neq 0$ |

=--

see e.g. ([ManifoldAtlas](#ManifoldAtlas))

+-- {: .num_prop}
###### Proposition

For $X$ a [[CW-complex]] (for instance a [[manifold]]), then  the oriented cobordism ring is expressed in terms of the [[ordinary homology]] $H_q(X,\Omega^{SO}_{p-q})$ of $X$ with [[coefficients]] in the cobordism ring over the point, prop. \ref{OrientedCobordismOverPoint}, as

$$
  \Omega_p^{SO}(X)
  =
  \oplus_{q = 0}^p
  H_q(X,\Omega_{p-q}^{SO})
  \;
  mod\; odd \; torsion
  \,.
$$

=--

e.g. [Connor-Floyd 62, theorem 14.2](#ConnorFloyd62)


## References

Lecture notes include

* {#Francis} [[John Francis]] (notes by [[Owen Gwilliam]]), _[Topology of manifolds](http://math.northwestern.edu/~jnkf/classes/mflds/)_, _Lecture 2: Cobordism_ ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/2cobordism.pdf))

* [[Gerald Höhn]], _Komplexe elliptische Geschlechter und $S^1$-&#228;quivariante Kobordismustheorie_ (german) ([pdf](http://arxiv.org/PS_cache/math/pdf/0405/0405232v1.pdf))

* [[Sander Kupers]], _Oriented bordism: Calculation and application_ ([pdf](http://web.stanford.edu/~kupers/orientedbordism.pdf))

Further discussion of oriented cobordism includes

* {#ManifoldAtlas} Manifold Atlas, _[Oriented bordism](http://www.map.mpim-bonn.mpg.de/Oriented_bordism)_

* {#ConnorFloyd62} P. E. Conner, E. E. Floyd, _Differentiable periodic maps_, Bull. Amer. Math. Soc. Volume 68, Number 2 (1962), 76-86. ([Euclid](http://projecteuclid.org/euclid.bams/1183524501), [pdf](http://www.maths.ed.ac.uk/~aar/papers/cf1.pdf))

A historical review in the context of [[complex cobordism cohomology theory]]/[[Brown-Peterson theory]] is in 

* [[Doug Ravenel]], chapter 4, section 2 of _[[Complex cobordism and stable homotopy groups of spheres]]_


On [[fibered cobordism groups]]:

* Astey, Greenberg, Micha, Pastor, _Some fibered cobordisms groups are not finitely generated_ ([pdf](http://www.ams.org/journals/proc/1988-104-01/S0002-9939-1988-0958093-3/S0002-9939-1988-0958093-3.pdf))

[[!redirects bordism ring]]

[[!redirects cobordism rings]]


[[!redirects cobordism group]]
[[!redirects cobordism groups]]