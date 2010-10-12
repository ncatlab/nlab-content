
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _3-manifold_ is a [[manifold]] of [[dimension]] 3.

## Properties

### Poincar&#233; conjecture

+-- {: .un_theorem}
###### Theorem
**([[Poincaré conjecture]])**

Every [[simply connected]] [[compact space|compact]] 3-manifold without boundary is [[homeomorphism|homeomorphic]] to the 3-sphere.

=--

+-- {: .proof}
###### Proof


A proof strategy was given by [[Richard Hamilton]]: imagine the manifold is equipped with a [[metric]]. Follow the [[Ricci flow]] of that metric through the space of metrics. As the flow proceeds along parameter time, it will from time to time pass through metrics that describe singular geometries where the compact metric manifold pinches off into seperate manifolds. Follow the flow through these singularities and then continue the flow on each of the resulting components. If this process terminates in finite parameter time with the metric on each component stabilizing to that of the round 3-sphere, then the original manifold was a 3-sphere.

The hard technical part of this program is to show that the passage through the  singularities can be controlled. This was finally shown by [[Grigori Perelman]].

=--


