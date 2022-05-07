
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Inertia orbifold_ is a particular model for the [[free loop space object]] of an [[orbifold]] $X$ (or plain [[groupoid]] or [[smooth groupoid]]/[[stack]] etc.): the [[smooth groupoid]] whose [[objects]] are [[automorphisms]] in $X$ and whose [[morphisms]] are [[conjugation]] of automorphisms by morphisms in $X$. In fact for each fibered category one can construct another fibered category, its inertia and the inertia stacks are a special case of this construction.

## Definition

Given a [[groupoid]] $G$ (in the category of [[sets]]) with the set of [[objects]] $G_0$ and the set of [[morphisms]] $G_1$, one defines its __inertia groupoid__ as the groupoid whose set $S$ of objects is the set of loops, i.e. the [[equalizer]] of the [[source]] and [[target]] maps $s,t: G_1\to G_0$; and whose set of maps from $f\colon a\to a$ to $g\colon b\to b$ consists of the [[commutative squares]] with the same vertical maps of the form 

$$\array{a &\stackrel{f}\rightarrow& a\\
u \downarrow && \downarrow u\\
b &\stackrel{g}\rightarrow& b
}$$

i.e. of the morphisms $u \colon a\to b$ in $G_1$ such that $u^{-1}\circ g\circ u = f$.

This is [[isomorphism|isomorphic]] to the [[functor category]] $\big[&#643;S^1,G\big]$, where $&#643;S^1$ (the [[shape modality|shape]] of the [[circle]]) denotes the free groupoid on a single object with a single [[automorphism]] (equivalently, the [[delooping groupoid]] $B\mathbb{Z}$ of the [[integers]]).  It is [[equivalence of categories|equivalent]] to the [[free loop space object]] of $G$ in the [[(2,1)-category]] of groupoids.

The same construction can be performed for a groupoid [[internal category|internal]] to any [[finitely complete category]], or more generally whenever the relevant [[limits]] exist.  If a ([[differentiable stack|differential]], [[topological stack|topological]] or [[algebraic stack|algebraic]]) stack (or, in particular, an [[orbifold]]) is represented by a groupoid, then the inertia groupoid of that groupoid represents its [[inertia stack]].  In particular, an orbifold corresponds to a Morita equivalence class of a proper &#233;tale groupoid. The inertia groupoid $\Lambda G$ of $G$ is the Morita equivalence class of the (proper &#233;tale) action groupoid for the action of $G_1$ by conjugation on the subspace $S\subset G_1$ of closed loops.  

For [[quantum field theory]] on orbifolds the inertia orbifold is related to so called _twisted sectors_ of the corresponding QFT. One can also consider more generally twisted multisectors. 

## Properties

### Convolution algebra and Relation to Drinfeld double

At least for a [[finite group]] $G$, the [[groupoid convolution algebra]] of the inertia groupoid of $\mathbf{B}G$ is the [[Drinfeld double]] of the [[group convolution algebra]] of $G$.

## References

Original articles:

* Tetsuro Kawasaki, _The signature theorem for V-manifolds_, Topology __17__ (1978), no. 1, 75&#8211;83 (<a href="https://doi.org/10.1016/0040-9383(78)90013-7">doi:10.1016/0040-9383(78)90013-7</a>)

Review and further development:

* [[Ernesto Lupercio]], [[Bernardo Uribe]], Section 4 of: _Inertia orbifolds, configuration spaces and the ghost loop space_, Quarterly Journal of Mathematics __55__, Issue 2, pp. 185-201, [arxiv/math.AT/0210222](http://arxiv.org/abs/math/0210222); _Loop groupoids, gerbes, and twisted sectors on orbifolds_, in: *[[Orbifolds in Mathematics and Physics]]*, Madison, WI, 2001, in: Contemp. Math. __310__, Amer. Math. Soc., Providence, RI, 2002, pp. 163&#8211;184, [MR2004c:58043](http://www.ams.org/mathscinet-getitem?mr=1950946), [math.AT/0110207](http://arxiv.org/abs/math/0110207)

See also:

* [[The Stacks Project]], [The inertia stack](https://stacks.math.columbia.edu/tag/036X), [more](https://stacks.math.columbia.edu/tag/034H), [more](https://stacks.math.columbia.edu/tag/034I)


* [[V. Hinich]], _Drinfeld double for orbifolds_, Contemporary Math. __433__, AMS Providence, 2007, 251-265,
[arXiv:math.QA/0511476](http://arxiv.org/abs/math/0511476)

* [[Jean-Louis Tu]], [[Ping Xu]], _Chern character for twisted K-theory of orbifolds_, Advances in Mathematics __207__ (2006) 455&#8211;483, [pdf](http://www.math.univ-metz.fr/~tu/publi/orb.pdf) (cf. sec. 2.3)

[[!redirects inertia orbifolds]]

[[!redirects inertia stack]]
[[!redirects inertia stacks]]

[[!redirects inertia groupoid]]
[[!redirects inertia groupoids]]



category: Lie theory
