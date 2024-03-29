
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

A **complete lattice** is a [[partial order|poset]] which has all small [[join|joins]] and [[meet|meets]] (as opposed to just finite joins and meets).  

In particular, it is a [[lattice]].  

Complete lattices and complete lattice homomorphisms form a [[concrete category]] [[CompLat]].


=--

+-- {: .num_remark}
###### Remark

By the [[adjoint functor theorem]] for posets, having either all joins or all meets is sufficient for the other.  However, a [[suplattice]] morphism may preserve only joins, while dually an [[inflattice]] morphism may preserve only meets.  Furthermore, a *large* poset with all *small* joins or meets need not have the other.

=--

+-- {: .num_remark}
###### Remark

Regarded as a [[small category]], a complete lattice is [[complete category|complete]].  Conversely, in [[classical logic]] and in any [[Grothendieck topos]], any [[complete small category]] is in fact a preorder, and hence a complete lattice.

=--

## Examples

* Any [[power set]];
* Any finite inhabited [[total order|toset]];
* The ordered set of [[real number]]s, if a [[top]] element $\infty$ and a [[bottom]] element $-\infty$ are added;
* The [[unit interval]] $[0,1]$.

Complete lattices are harder to come by in [[constructive mathematics]] and nearly impossible in [[predicative mathematics]] (at least if they are to be small).  In particular, one must use the Mac Neille reals (and be a bit careful about infinity) for the analytic examples to work constructively.


## Related concepts

* [[completely distributive lattice]]

[[!redirects complete lattices]]