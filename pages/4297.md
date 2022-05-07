
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Statement


+-- {: .num_theorem}
###### Theorem
**(Poincar&#233; conjecture)**

Every [[simply connected]] [[compact space|compact]] [[topological manifold|topological]] [[3-manifold]] without boundary is [[homeomorphism|homeomorphic]] to the 3-sphere.

=--

+-- {: .proof}
###### Proof strategy


A proof strategy was given by [[Richard Hamilton]]: imagine the manifold is equipped with a [[metric]]. Follow the [[Ricci flow]] of that metric through the space of metrics. As the flow proceeds along parameter time, it will from time to time pass through metrics that describe singular geometries where the compact metric manifold pinches off into separate manifolds. Follow the flow through these singularities and then continue the flow on each of the resulting components. If this process terminates in finite parameter time with the metric on each component stabilizing to that of the round 3-sphere, then the original manifold was a 3-sphere.

The hard technical part of this program is to show that the passage through the  singularities can be controlled. This was finally shown in ([Perelman 02](Perelman02)).

=--

See at _[[Ricci flow]]_ for more.

## Related entries

* [[geometrization conjecture]]

## References

### In dimension 3

* {#Perelman02} [[Grigori Perelman]], _The entropy formula for the Ricci flow and its geometric applications_ ([arXiv:math/0211159](http://arxiv.org/abs/math/0211159))

* {#BessiersEtAl} Laurent Bessieres, Gerard Besson, Michel Boileau, Sylvain Maillot, Joan Porti, _Geometrisation of 3-manifolds_ ([pdf](http://www-fourier.ujf-grenoble.fr/~besson/book.pdf))

Notes from a survey talk: 

* [Huisken on Uniformization I](http://golem.ph.utexas.edu/category/2007/02/huisken_on_uniformization.html)

* [Huisken on Uniformization II](http://golem.ph.utexas.edu/category/2007/02/huisken_on_uniformization_ii.html)

See also

* {#Martelli16} Bruno Martelli, _An Introduction to Geometric Topology_ ([arXiv:1610.02592](https://arxiv.org/abs/1610.02592))

### In higher dimesnions

The analog of the Poincaré conjecture in higher dimensions:

* {#Newman66} M. H. A. Newman, Theorem 7 in: *The Engulfing Theorem for Topological Manifolds*, Annals of Mathematics Second Series, *84** 3 (1966) 555-571  ([jstor:1970460](https://www.jstor.org/stable/1970460))

[[!redirects Poincare conjecture]]