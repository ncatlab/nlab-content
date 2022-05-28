+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

## Definition

A **condensed infinity-groupoid** is a [[(infinity,1)-sheaf]] of [[infinity-groupoids]] on the [[pro-étale (infinity,1)-site]] of the point. 

Equivalently, it is an [[(infinity,1)-functor]] 

$$T:ProObjectsIn \infty Grpd^\op \longrightarrow \infty Grpd$$

from the [[opposite category|opposite]] [[(infinity,1)-category]] of [[pro-object in an (infinity,1)-category|pro objects]] in [[infinity-groupoids]] to the [[(infinity,1)-category]] [[Infinity-Grpd]] of [[infinity-groupoids]], such that the natural maps

$$T(\mathbb{0}) \to \mathbb{1}$$

and 

$$T(S + S^{'}) \to T(S) \times T(S^{'})$$

are [[homotopy equivalences]] for any pro-object in infinity-groupoids $S$ and $S^{'}$, whereas the natural fork 

$$T(S) \to T(S^{'}) \rightrightarrows T(S^{'} \times_S S^{'})$$

is an [[(infinity,1)-equalizer]] for any [[covering]] of pro-objects in infinity-groupoids $S^{'} \to S$. 

## Properties

The [[(infinity,1)-category]] 
$\mathrm{Cond}\infty\mathrm{Grpd}$ of condensed infinity-groupoids is a locally small [[locally cartesian closed (infinity,1)-category|locally cartesian closed]] [[(infinity,1)-pretopos]]. 

## Terminology

In the model of [[infinity-groupoids]] as [[simplicial sets]]/[[Kan complexes]], condensed infinity-groupoids are sometimes referred to as **condensed anima**. 

## Related concepts

* [[condensed mathematics]]
* [[condensed set]]
* [[condensed spectrum]]
* [[condensed E-infinity ring]]
* [[condensed module spectrum]]

## References

See [[condensed mathematics]] and [[infinity-groupoid#Anima]]. 

[[!redirects condensed infinity-groupoids]]
[[!redirects condensed anima]]