
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

### Homology groups

For $X$ a [[manifold]], the [[group]] $MU_\ast(X)$ is the group of equivalence classes of maps $\Sigma \to X$ from manifolds $\Sigma$ with [[complex structure]] on the stable [[normal bundle]], modulo suitable complex [[cobordisms]].

e.g ([Ravenel chapter 1, section 2](#Ravenel))

(...)

### As represented by a spectrum

_Cobordism cohomology theory_, denoted $M O$ for _oriented cobordism cohomology_ , $M U$ for _complex cobordism cohomology_  etc, is the [[generalized (Eilenberg-Steenrod) cohomology]] theory represented by the universal [[Thom spectrum]].

This spectrum, also denoted $M U$
is the [[spectrum]] is in degree $2 n$ given by the [[Thom space]] of the [[vector bundle]] that is  [[associated bundle|associated]] by the defining [[representation]] of the [[unitary group]] $U(n)$ on $\mathbb{C}^n$ to the [[generalized universal bundle|universtal]] $U(n)$-[[principal bundle]]:

$$
  M U(2n) = Thom
  \left(
    standard\;associated\;bundle\;to\;universal\;bundle
    \array{
      E U(n) \\ \downarrow \\ B U(n)
    }
  \right)
$$


The _periodic_ complex cobordism theory is given by adding up all the even degree powers of this theory:

$$
  M P = \vee_{n \in \mathbb{Z}} \Sigma^{2 n} M U
$$

There is a canonical [[oriented cohomology theory|orientation]] on this obtained from the map

$$
  \omega : \mathbb{C}P^\infty \stackrel{\simeq}{\to}
  M U(1)
  \;\;\;\;
  M U(\mathbb{C}P^\infty)
$$

(???)

this is the universal even periodic cohomology theory with orientation

The [[cohomology ring]] $M P({*})$ is the [[Lazard ring]] which is the universal coefficient ring for [[formal group law]]s.

The [[periodic cohomology theory|periodic]] version is sometimes written $PMU$.

## Differential cohomology refinement

The refinement of cobordism cohomology theory to [[differential cohomology]] is [[differential cobordism cohomology]].

## Properties

### Complex bordism ring

The complex [[cobordism ring]] is the graded [[polynomial]] [[ring]]

$$
  MU_\ast(pt) \simeq \mathbb{Z}[x_1, x_2, \cdots]
  \,,
$$

where the generator $x_i$ is in degree $2 i$.

e.g ([Ravenel theorem 1.2.18](#Ravenel))


### Homotopy groups 

The [[homotopy groups]] of the [[Thom spectrum]] $MU$ form the [[ring]]

$$
  \pi_\bullet(MU) \simeq \mathbb{Z}[x_1, x_2, \cdots]
$$

with the generator $x_i$ in degree $2i$.

This is due to ([Milnor 60](#Milnor60), [Novikov 60](#Novikov60), [Novikov 62](#Novikov62)). A review is in ([Ravenel, ch. 3, theorem 3.1.5](#Ravenel)).

### Snaith's theorem

[[Snaith's theorem]] asserts that the [[periodic complex cobordism spectrum]] is the [[∞-group ∞-ring]] of the [[classifying space]] for stable [[complex vector bundles]] (the classifying space for [[topological K-theory]]) localized at the [[Bott element]] $\beta$:

$$
  PMU \simeq \mathbb{S}[B U][\beta^{-1}]
  \,.
$$

## Related concepts

* [[algebraic cobordism]], [[algebraic cobordism spectrum]]

* [[Adams-Novikov spectral sequence]]


## References

Original articles include

* [[John Milnor]], _On the cobordism ring &#173;$\Omega^\bullet$ and a complex analogue_, Amer. J. Math. 82 (1960), 505&#8211;521.
 {#Milnor60}

* [[Sergei Novikov]], _Some problems in the topology of manifolds connected with the theory of Thom spaces_, Dokl. Akad. Nauk. SSSR. 132 (1960), 1031&#8211;1034 (Russian).
 {#Novikov60}

* [[Sergei Novikov]], _Homotopy properties of Thom complexes_, Mat. Sb. (N.S.) 57 (99) (1962), 407&#8211;442.
 {#Novikov62}

Textbooks accounts include

* [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_
 {#Ravenel}

with an emphasis on the use of $MU$ in the [[Adams-Novikov spectral sequence]], and

* [[Yuli Rudyak]], _On Thom spectra, orientability and cobordism_, Springer Monographs in Mathematics, 1998 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/rudyakthom.pdf))
 {#Rudyak98}


Lecture notes include lecture 5 in 

* [[Jacob Lurie]], _Chromatic Homotopy Theory_ Lecture series ([lecture notes](http://www.math.harvard.edu/~lurie/252x.html))


For further context see also the discussion at

* _[[A Survey of Elliptic Cohomology - cohomology theories]]_

See also

* [[Haynes Miller]], _"Chromatic" homotopy theory_ May 2011 ([pdf](http://www-math.mit.edu/~hrm/papers/chromatic.pdf))



[[!redirects complex cobordism spectrum]]
[[!redirects periodic complex cobordism spectrum]]


[[!redirects complex cobordism cohomology theory]]
[[!redirects complex cobordism]]

[[!redirects complex bordism]]

[[!redirects cobordism homology theory]]

[[!redirects complex cobordism cohomology]]
[[!redirects complex cobordism cohomology theory]]