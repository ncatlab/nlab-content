
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a given [[intuitionistic logic]] framework, such as a [[type theory]], the _logical topology_ ([Penon 81](#Penon81)) on a given object ([[type]]) $X$ is that whose [[open subsets]] are the sets $U$ for which any $X - \{x\}$ and $U$ cover $X$. This implies that an open subset contains for every point $x$ also the collection of points that are indistinguishable from it in [[classical logic]], hence that are [[double negation|not not]] equal to $x$.

The notion of Penon open is closely related to that of Zariski open. Consider the affine line $\mathbb{A} : \text{fpRing} \to \text{Set}$ as the forgetful functor from finitely presented rings to sets. The (category theorists') big Zariski topos is the largest subtopos of this topos of functors in which $\mathbb{A}$ is a local ring. A ring is local if for all $y$, either $y$ or $1- y$ is invertible; equivalently, we may ask that either $y$ or $x - y$ is invertible for a given invertible element $x$, by homogeneity. In this case, the locality of $\mathbb{A}$ is equivalent to the subset $\mathbb{G}_m \hookrightarrow \mathbb{A}$ of invertible elements being logically open.

## Related concepts

* [[synthetic differential topology]]

## References

The concept was introduced in 

* {#Penon81} [[Jacques Penon]], _Infinitésimaux et intuitionnisme_,  Cahiers de Topologie et Géométrie Différentielle Catégoriques, Volume 22 (1981) no. 1, p. 67-72 ([numdam:CTGDC_1981__22_1_67_0](http://www.numdam.org/item/?id=CTGDC_1981__22_1_67_0))

Review in the context of [[cohesive toposes]], [[modal type theory]] and [[cohesive homotopy type theory]] includes

* [[David Myers]], _Logical Topology and Axiomatic Cohesion_, talk at _[Geometry in Modal Homotopy Type Theory](http://www.andrew.cmu.edu/user/fwellen/modal-workshop.html)_ 2019 ([pdf slides](http://www.andrew.cmu.edu/user/fwellen/myers-slides.pdf), [video recording](https://youtu.be/GbzQMsr3Jf4))

[[!redirects logical topologies]]