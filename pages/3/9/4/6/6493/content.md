Given a discrete groupoid $G$ with the set of objects $G_0$ and the set of morphisms $G_1$, one defines its __inertia groupoid__ as the groupoid whose space of objects is the space of loops, i.e. the equalizer of the source and target maps $s,t: G_1\to G_0$; whose space of maps from $f: a\to a$ to $g: b\to b$ consists of the commutative squares with the same vertical maps of the form 

$$\array{a &\stackrel{f}\rightarrow& a\\
u \downarrow && \downarrow u\\
b &\stackrel{g}\rightarrow& b
}$$

i.e. of the morphisms $u : a\to b$ in $G_1$ such that $u^{-1}\circ g\circ u = f$.


If a ([[differentiable stack|differential]], [[topological stack|topological]] or [[algebraic stack|algebraic]]) stack (or, in particular, an [[orbifold]]) is represented by a groupoid, then the inertia groupoid of that groupoid represents another stack (orbifold).

For [[quantum field theory]] on orbifolds the inertia orbifold is related to so called twisted sectors of the corresponding QFT. One can also consider more generally twisted multisectors. 

* [[Ernesto Lupercio]], [[Bernardo Uribe]], _Inertia orbifolds, configuration spaces and the ghost loop space_, Quarterly Journal of Mathematics __55__, Issue 2, pp. 185-201, [arxiv/math.AT/0210222](http://arxiv.org/abs/math/0210222).
* T. Kawasaki, _The signature theorem for V -manifolds_, Topology __17__ (1978), no. 1, 75&#8211;83.
* [[V. Hinich]], _Drinfeld double for orbifolds_, Contemporary Math. __433__, AMS Providence, 2007, 251-265,
[arXiv:math.QA/0511476](http://arxiv.org/abs/math/0511476)
* L. Dixon, J. A. Harvey, C. Vafa, E. Witten, _Strings on orbifolds_,  Nuclear Phys. B __261__ (1985), no. 4, 678&#8211;686. [MR87k:81104a](http://www.ams.org/mathscinet-getitem?mr=818423), [doi](http://dx.doi.org/10.1016/0550-3213(85)90593-0), _Strings on orbifolds. II_, Nuclear Phys. B __274__ (1986), no. 2, 285&#8211;314, [87k:81104b](http://www.ams.org/mathscinet-getitem?mr=851703), <a href="http://dx.doi.org/10.1016/0550-3213(86)90287-7">doi</a>

[[!redirects inertia stack]]
[[!redirects inertia groupoid]]