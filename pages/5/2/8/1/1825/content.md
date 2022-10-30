
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

### Finite-dimensional spheres

The $n$-dimensional unit **sphere** , or simply **$n$-sphere**, is the [[topological space]] given by the [[subset]] of the $(n+1)$-dimensional [[Cartesian space]] $\mathbb{R}^{n+1}$ consisting of all points $x$ whose distance from the origin is $1$

$$ 
  S^n = \{ x: \mathbb{R}^{n+1} \;|\; \|x\| = 1 \} 
  \,.
$$

The $n$-dimensional sphere of radius $r$ is
$$ S^n_r = \{ x: \mathbb{R}^{n+1} \;|\; \|x\| = r \} .$$
Topologically, this is equivalent to the unit sphere for $r \gt 0$, or a [[point]] for $r = 0$.

This is naturally also a [[smooth manifold]] of [[dimension]] $n$, with the [[smooth structure]] induced from the standard sooth structure on $\mathbb{R}$^n.

### Infinite dimensional spheres 

One can also talk about a sphere in an arbitrary (possibly infinite-dimensional) [[normed vector space]] $V$:
$$ S(V) = \{ x: V \;\text{such that}\; {\|x\|} = 1 \} .$$

If a [[LCTVS|locally convex topological vector space]] admits a continuous linear injection into a [[normed vector space]], this can be used to define its sphere.  If not, one can still define the sphere as a *quotient* of the space of non-zero vectors under the scalar action of $(0,\infty)$.

Homotopy theorists define $S^\infty$ to be the sphere in the (incomplete) [[normed vector space]] (traditionally with the $l^2$ norm) of infinite [[sequence]]s almost all of whose values are $0$, which is the [[directed colimit]] of the $S^n$:
$$ S^{-1} \hookrightarrow S^0 \hookrightarrow S^1 \hookrightarrow S^2 \hookrightarrow \cdots S^\infty .$$
In themselves, these provide nothing new to [[homotopy theory]], as they are at least weakly contractible and usually [[contractible space|contractible]].  However, they are a very useful source of big contractible spaces and so are often used as a starting point for making concrete models of [[classifying spaces]].

If the vector space is a [[shift space]], then contractibility is straightforward to prove.

+-- {: .num_theorem #theorem}
###### Theorem
Let $V$ be a [[shift space]] of some order.  Let $S V$ be its sphere (either via a norm or as the quotient of non-zero vectors).  Then $S V$ is contractible.
=--

+-- {: .proof}
###### Proof
Let $T \colon V \to V$ be a [[shift map]].  The idea is to homotop the sphere onto the image of $T$, and then down to a point.

It is simplest to start with the non-zero vectors, $V \setminus \{0\}$.  As $T$ is injective, it restricts to a map from this space to itself which commutes with the scalar action of $(0,\infty)$.  Define a homotopy $H \colon [0,1] \times (V \setminus
 \{0\}) \to V \setminus \{0\}$ by $H_t(v) = (1 - t)v + t T v$.  It is clear that, assuming it is well-defined, it is a homotopy from the identity to $T$.  To see that it is well-defined, we need to show that $H_t(v)$ is never zero.  The only place where it could be zero would be on an eigenvector of $T$, but as $T$ is a [[shift map]] then it has none.

As $T$ is a [[shift map]], it is not surjective and so we can pick some $v_0$ not in its image.  Then we define a homotopy $G \colon [0,1] \times (V \setminus \{0\}) \to V \setminus \{0\}$ by $G_t(v) = (1 - t)T v + t v_0$.  As $v_0$ is not in the image of $T$, this is well-defined on $V \setminus \{0\}$.  Combining these two homotopies results in the desired contraction of $V \setminus \{0\}$.

If $V$ admits a suitable function defining a spherical subset (such as a norm) then we can modify the above to a contraction of the spherical subset simply by dividing out by this function.  If not, as the homotopies above all commute with the scalar action of $(0,\infty)$, they descend to the definition of the sphere as the quotient of $V \setminus \{0\}$.
=--


## Properties

* The $n$-sphere is the [[boundary]] of the $(n+1)$-[[ball]].

* These spheres, or rather their underlying [[topological space]]s or [[simplicial set]]s, are fundamental in (ungeneralised) [[homotopy theory]].  In a sense, [[Whitehead's theorem]] says that these are all that you need; no further [[generalized (Eilenberg-Steenrod) homotopy theory|generalised homotopy theory]] (in a sense [[Eckmann–Hilton duality|dual]] to [[Eilenberg–Steenrod cohomology theory]]) is needed.

* [[positive dimension spheres are H-cogroup objects]], and this is the origin of the [[group]] structure on [[homotopy groups]]). 

* Precisely four spheres are [[parallelizable]], and three of these are so via [[Lie group]] structure (hence are the only spheres with Lie group structure) (see at _[[Hopf invariant one theorem]]_):

  * $S^0$ (the [[group of order two]], the group of units of the [[real numbers]]);

  * $S^1$ (the [[circle group]], the group of unit [[complex numbers]]);

  * $S^3$ (the [[special unitary group]] $SU(2)$, the group of unit [[quaternions]]);

  * $S^7$ (the [[Moufang loop]] of unit [[octonions]])


## Low dimensions

*  The $(-1)$-sphere is the [[empty space]].
*  The [[0-sphere]] is the [[disjoint union]] of two [[points]].
*  The $1$-sphere is the [[circle]].
*  The $2$-sphere is usual sphere from ordinary geometry. This canonically carries the structure of a [[complex manifold]] which makes it the [[Riemann sphere]].

Note that this violates the convention that a $1$-foo is a foo; instead the ruling convention being used is that an $n$-foo has dimension $n$.  One could follow both by saying '$n$-circle' instead, although this might get confused with the $n$-[[torus]].

* The [[3-sphere]] and [[4-sphere]] and [[7-sphere]] are interesting, too.

## Related concepts

* [[homotopy groups of spheres]]

* [[rational n-sphere]]

* [[sphere spectrum]]

* [[spherical fibration]]

* [[geometric quantization of the 2-sphere]]

* [[representation sphere]]

* [[motivic sphere]]

## References

### Formalization

Axiomatization of the [[homotopy type]] of the 1-sphere (the [[circle]]) and the 2-sphere, as [[higher inductive types]], is in 

* [[Univalent Foundations Project]], section 6.4 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

Visualization of the idea of the construction for the 2-sphere is in 

* [[Andrej Bauer]], _HoTT $S^2$_ ([video](https://vimeo.com/119606901))

### Group actions on spheres

Discussion of [[free actions]] by [[finite groups]] on spheres includes

* {#Wall78} [[C. T. C. Wall]], _Free actions of finite groups on spheres_, Proceedings of Symposia in Pure Mathematics, Volume 32, 1978 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/wall7.pdf))


* [[Alejandro Adem]], _Constructing and Deconstructing Group Actions_ ([arXiv:0212280](http://arxiv.org/abs/math/0212280))


See also the [[ADE classification]] of such actions on the [[7-sphere]] (as discussed there)

[[!redirects n-sphere]]
[[!redirects n-spheres]]

[[!redirects spheres]]

[[!redirects infinite sphere]]

[[!redirects 1-sphere]]
[[!redirects 1-spheres]]

[[!redirects 2-sphere]]
[[!redirects 2-spheres]]