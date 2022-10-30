
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $X$ a ([[spacetime]]) [[manifold]] and $E \to X$ a [[bundle]] with [[jet bundle]] $j_\infty E \to X$, the **variarional bicomplex** is essentially the [[de Rham complex]] of $j_\infty E$ with [[differential form]]s bigraded by horizontal degree (with respect to $X$) and vertical degree (along the [[fiber]]s of $j_\infty E$)). Accordingly the [[differential]] decomposes as

$$
  D = d + \delta
  \,,
$$

where $d$ is the [[de Rham differential]] on $X$ and $\delta$ is the variational differential.

Much of [[classical mechanics]] and [[classical field theory]] on $X$ is formalized in terms of the variational bicomplex. For instance 

* a field configuration is a [[section]] of $E$;

* a [[Lagrangian]] is an element $L \in \Omega^{n,0}(j_\infty E)$;

* a [[local action functional]] is a maps

  $$
    S : \Gamma(E) \to \marthbb{R}
  $$

  of the form

  $$
    S(\phi) = \int_X L(j_\infty \phi)
    \,,
  $$

* the [[Euler-Lagrange equation]] is 

  $$
    E(L) := \delta L mod im(d) = 0
  $$

* the [[covariant phase space]] is the locus 

  $$
    \{
     \phi \in \Gamma(E) | E(L)(j_\infty \phi) = 0
   \}
  $$

* a [[conserved current]] is an element in $\Omega^{n-1,0}(j_\infty E)$ that is $d$-closed on covariant phase space;

* a [[symmetry]] is a vertical vector field $v$ such that
  
  $$
    v(L) = 0 mod im(d)
  $$

* [[Noether's theorem]] asserts that every [[symmetry]] induces a [[conserved current]].


## References

An early discussion with application to [[covariant phase space]]s and their [[presymplectic structure]] is in

* [[Gregg Zuckerman|G. J. Zuckerman]], _Action Principles and Global Geometry_ , in Mathematical Aspects of String Theory, S. T. Yau (Ed.), World Scientific, Singapore, 1987, pp. 259&#8364;284. ([[ZuckermanVariation.pdf:file]])

Other references include

* Peter Olver, _Applications of Lie groups to differential equations_, Springer

* A. M. Vinogradov, A spectral sequence associated with a non-linear differential
equation, and the algebro-geometric foundations of Lagrangian field theory with
constraints, Soviet Math. Dokl. __19__ (1978), 144&#8211;148.

* A. M. Vinogradov, _The $C$-spectral sequence, Lagrangian formalism and conservation laws I, II_, J. Math. Anal. Appl. __100__ (1984), 1&#8211;129.

* Ian Anderson, _The variational bicomplex_ ([pdf](http://www.math.usu.edu/~fg_mp/Publications/VB/vb.pdf))

