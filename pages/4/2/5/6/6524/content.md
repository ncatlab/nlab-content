
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


> For other notions of _[[torsion]]_ see there.

***

#Contents#
* table of contents
{:toc} 

## Definition

A ([[pseudo-Riemannian metric|pseudo]]) [[Riemannian metric]] with metric-compatible [[Levi-Civita connection]] on a [[smooth manifold]] $X$ may be encoded by a [[connection on a bundle|connection]] with values in the [[Poincaré Lie algebra]] $\mathfrak{iso}(p,q)$.

This [[Lie algebra]] is the [[semidirect product]] 

$$
  \mathfrak{iso}(p,q) \simeq \mathfrak{so}(p,q) \ltimes \mathbb{R}^{p+q}
$$

of the [[special orthogonal Lie algebra]] and the abelian translation Lie algebra. Accordingly, a connection 1-form has two components

* $\Omega \in \Omega^1(U,\mathfrak{so}(p,q))$ (sometimes called the "[[spin connection]]");

* $E \in \Omega^1(U,\mathbb{R}^{p+q})$ (sometimes called the "[[vielbein]]").

The metric itself is 

$$
  g = \langle E \otimes E \rangle
  \,.
$$

Accordingly also the [[curvature]] 2-form has two components:

* $R = d \Omega + [\Omega \wedge \Omega] \in \Omega^2(U, \mathfrak{so}(p,q))$ -- the [[Riemann curvature]];

* $\tau = d E + [\Omega \wedge E]$ -- the **torsion**.

This is the special case of the more general concept of [[torsion of a Cartan connection]].

## Generalizations

In [[supergeometry]] a metric structure is given by a connection with values in the [[super Poincaré Lie algebra]]. The corresponding notion of torsion has an extra contribution from [[spinor]] fields: the [[super torsion]].

See also

* [[integrability of G-structures]]

## Related concepts

* [[first-order formulation of gravity]]

[[!include local and global geometry - table]]

## References

Monographs:

* {#Sharpe97} [[Richard W. Sharpe]], *Differential geometry -- Cartan's generalization of Klein's Erlagen program*, Graduare Texts in Mathematics **166**, Springer (1997) &lbrack;[ISBN:9780387947327](https://link.springer.com/book/9780387947327)&rbrack;

* {#CapSlovak09} [[Andreas Čap]], [[Jan Slovák]], chapter 1 of: _Parabolic Geometries I -- Background and General Theory_, AMS (2009) &lbrack;[ISBN:978-1-4704-1381-1](http://bookstore.ams.org/surv-154)&rbrack;

Discussion of torsion in [[gravity|gravitational]] [[classical field theory]]:

* [[Friedrich W. Hehl]], [[Yuri N. Obukhov]], *Élie Cartan’s torsion in geometry and in field theory, an essay*, Annales de la Fondation Louis de Broglie, **32** 2-3 (2007) 157-194 &lbrack;[pdf](https://fondationlouisdebroglie.org/AFLB-322/aflb322m595.pdf), [arXiv:0711.1535](https://arxiv.org/abs/0711.1535)&rbrack; 

Discussion with an eye towards [[torsion constraints in supergravity]]:

* {#Lott01} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_ &lbrack;[arXiv:0108125](http://arxiv.org/abs/math/0108125)&rbrack;

  following:

  [[John Lott]], *Torsion constraints in supergeometry*, Comm. Math. Phys. **133** (1990) 563-615 &lbrack;[doi:10.1007/BF02097010](https://doi.org/10.1007/BF02097010)&rbrack;






