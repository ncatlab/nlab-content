
<div class="rightHandSide toc">
[[!include manifolds and cobordisms - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The **cobordism ring** $\Omega_*=\oplus_{n\geq 0}\Omega_n$ is the [[ring]] whose 

* degree $n$ elements are classes of $n$-dimensional [[manifold]]s modulo [[cobordism]]s;

* product operation is given by the [[Cartesian product]] of manifolds;

* addition operation is given by the [[disjoint union]] of manifolds.

Instead of bare manifolds one can consider manifolds with extra structure, such as [[orientation]], [[spin structure]], [[string structure]], etc. and accordingly there is _oriented cobordism ring_ $\Omega^{SO}_*$,  the _spin cobordism ring_ $\Omega^{Spin}_*$, etc. In this context the bare cobordism ring is also denoted $\Omega^O_*$ or $\Omega^{un}_*$.

A ring [[homomorphism]] out of the cobordism ring is a [[genus]].

## Higher category interpretation

The cobordism ring finds its natural interpretation in [[higher category theory]].

+-- {: .un_theorem}
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

(Really on the left we have the $\infty$-groupoidification of that [[∞-category]], but since $Bord_{(\infty,\infty)}$ has duals for [[k-morphism]]s for _all_ $k$, it should already be an $\infty$-groupoid).

Hence the cobordism ring in degree $n$ is the [[decategorification]] of the $n$-fold [[loop space object|looping]] of the $\infty$-category of cobordisms.



## References

An useful review of the central definitions and theorems about the cobordism ring is in chapter 1 of

* [[Gerald Höhn]], _Komplexe elliptische Geschlechter und $S^1$-&#228;quivariante Kobordismustheorie_ (german) ([pdf](http://arxiv.org/PS_cache/math/pdf/0405/0405232v1.pdf))

A discussion of its relation to the Thom spectrum and the [[(∞,n)-category of cobordisms]] for $n = \infty$ is in

* [[John Francis]], _Cobordisms_ (notes by [[Owen Gwilliam]]) ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/2cobordism.pdf))


[[!redirects bordism ring]]
