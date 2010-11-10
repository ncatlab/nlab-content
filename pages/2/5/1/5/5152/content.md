+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}
 
##Idea

Spherical objects in a general [[pointed category|pointed]]  [[model category]] play the role of the spheres in $Top$.


Let $\mathcal{C}$ be a [[pointed category|pointed]] [[model category]].
+--
{: .un_defn}
######Definition######
A **spherical object** for $\mathcal{C}$ is a [[model category|cofibrant]] homotopy [[cogroup]] in $\mathcal{C}$.
=--

##Examples

1. The spheres form the obvious examples of spherical objects in the category $Top$, but the rational spheres give other examples.

1. In the category of path connected pointed spaces with action of a discrete group, $Gr.Top^*_0$ and space of form $S^n_G= \bigvee_G S^n$ is a spherical object.(see Baues, 1991, ref. below, p.273).

1. Any rational sphere is a sphere object (in a suitable category for [[rational homotopy theory]]).

1. Let $T$ be a contractible locally finite 1-dimensional simplicial complex, with $T^0$ its 0-skeleton. Let $\epsilon : E'T^0$ be a finite-to-one function. By $S^n_\epsilon$ we mean the space obtained by attaching an $n$-sphere to the vertices of $T$ with at vertex $v$, the spheres attached to $v$ being indexed by $\epsilon^{-1}(v)$. This space $S^n_\epsilon$ is a spherical object in the proper category, $Proper_\infinity^T$, of $T$-based spaces. (In this context $T$ is acting as the analogue of the base point.  It gives a base tree within the spaces.  This is explored a bit more in [[proper homotopy theory]].)

For instance, take $T = \mathbb{R}_{\geq 0}$, made up of an infinite number of closed unit intervals (end-to-end), then $S^n_\epsilon$ will be the infinite string of spheres considered in the entry on the [[Brown-Grossmann homotopy groups]] if we take $\epsilon$ to be the identity function on $T^0$. 


+--
{: .un_defn}
######Definition######
By a  **family of spherical objects** for $\mathcal{C}$ is meant .
=--
##References

Spherical objects are considered in 

*  [[Hans-Joachim Baues]] and [[David Blanc]], Comparing cohomology obstructions, [Arxiv](http://arxiv.org/PS_cache/arxiv/pdf/1008/1008.1712v1.pdf) (to appear JPAA).

Examples are given in earlier work by Baues and by Blanc. 

The group action case is in 

*  [[Hans-Joachim Baues]],  _Combinatorial Homotopy and 4-Dimensional Complexes_, de Gruyter Expositions in Mathematics 2, Walter de Gruyter, (1991).

The example from [[proper homotopy theory]] is discussed in

* H.-J. Baues and  Antonio Quintero, _Infinite Homotopy Theory_,  K-monographs in mathematics, Volume 6, Kluwer, 2001.