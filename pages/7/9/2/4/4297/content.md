
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--



+-- {: .un_theorem}
###### Theorem
**(Poincar&#233; conjecture)**

Every [[simply connected]] [[compact space|compact]] [[3-manifold]] without boundary is [[homeomorphism|homeomorphic]] to the 3-sphere.

=--

+-- {: .proof}
###### Proof


A proof strategy was given by [[Richard Hamilton]]: imagine the manifold is equipped with a [[metric]]. Follow the [[Ricci flow]] of that metric through the space of metrics. As the flow proceeds along parameter time, it will from time to time pass through metrics that describe singular geometries where the compact metric manifold pinches off into seperate manifolds. Follow the flow through these singularities and then continue the flow on each of the resulting components. If this process terminates in finite parameter time with the metric on each component stabilizing to that of the round 3-sphere, then the original manifold was a 3-sphere.

The hard technical part of this program is to show that the passage through the  singularities can be controlled. This was finally shown by [[Grigori Perelman]].

=--

## References

Notes from a survey talk: 

* [Huisken on Uniformization I](http://golem.ph.utexas.edu/category/2007/02/huisken_on_uniformization.html)

* [Huisken on Uniformization II](http://golem.ph.utexas.edu/category/2007/02/huisken_on_uniformization_ii.html)

[[!redirects Poincare conjecture]]