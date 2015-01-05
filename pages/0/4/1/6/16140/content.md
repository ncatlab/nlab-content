## Idea

_Semi-topological K-theory_ $K_*^{st}$ is a [[homology theory|homological invariant]] of [[complex varieties]] that interpolates between [[algebraic K-theory]] and [[topological K-theory]]. One recovers [[topological K-theory]] by inverting the [[Bott element]].

Semi-topological K-theory is related to [[morphic cohomology]] in the same way that [[algebraic K-theory]] is related to [[motivic cohomology]] and [[topological K-theory]] is related to [[singular cohomology]]. In fact there is an analogue of the [[Atiyah-Hirzebruch spectral sequence]].

Some [examples](#Examples) suggest that semi-topological K-theory may be a better suited invariant for complex varieties than either algebraic or topological K-theory.

## Examples
 {#Examples}

* On a [[point]], semi-topological K-theory coincides with [[topological K-theory]]:
  $$ K_*^{st}(\Spec(\mathbf{C})) \simeq K_*^{top}(\Spec(\mathbf{C})), $$
while the [[algebraic K-theory]] groups are uncountable for $i \gt 0$.

* With finite [[coefficients]], semi-topological K-theory coincides with [[algebraic K-theory]]:
  $$ K_*^{st}(X, \mathbf{Z}/n) \simeq K_*^{alg}(X, \mathbf{Z}/n) $$
while the [[topological K-theory]] only sees the [[homotopy type]] of the variety and not the finer algebraic structure.

* Rationally, semi-topological K-theory contains information about the cycles on $X$, and conjecturally, the rational [[Hodge filtration]] on [[singular cohomology]].

* $K_0^{st}(X)$ coincides with the [[Grothendieck group]] of [[vector bundles]] up to [[algebraic equivalence]]. Rationally, an analogue of the [[Chern character]] map induces canonical isomorphisms
  $$ K_0^{st}(X, \mathbf{Q}) \stackrel{\sim}{\longrightarrow} CH^*_alg(X, \mathbf{Q}), $$
where on the right hand side is the group of [[algebraic cycles]] modulo [[algebraic equivalence]].

## References

A first definition of semi-topological K-theory was given in

* [[Eric M. Friedlander]] and [[Mark E. Walker]], _Semi-topological K-theory using function complexes_, Topology, 41(3):591&#8211;644, 2002.

An analogue of the [[Atiyah-Hirzebruch spectral sequence]], and computations of semi-topological K-theory for a large class of varieties, are in

* [[Eric M. Friedlander]], [[Christian Haesemeyer]], and [[Mark E. Walker]]. _Techniques, computations, and conjectures for semi-topological K-theory_, Math. Ann., 330(4):759&#8211;807, 2004, [web](http://www.math.uiuc.edu/K-theory/0621/).

A survey is

* [[Eric M. Friedlander]], [[Mark E. Walker]], _Semi-topological K-theory_, in [[Handbook of K-theory]], Springer, 2005, [web](http://www.math.illinois.edu/K-theory/handbook/).

A state of the art treatment via [[dg-categories]], hence fitting into the framework of [[noncommutative motives]], was given in

* [[Anthony Blanc]], _Topological K-theory of complex noncommutative spaces_, Ph.D. thesis, [arXiv:1211.7360](http://arxiv.org/abs/1211.7360).

[[!redirects semitopological K-theory]]