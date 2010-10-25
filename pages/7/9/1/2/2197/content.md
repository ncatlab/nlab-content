
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Definition

A [[topological vector space]] is __locally convex__ if it has a base of topology consisting of convex open subsets.  Equivalently, it is a vector space equipped with a [[gauge space|gauge]] consisting of [[seminormed vector space|seminorms]].  As with other topological vector spaces, a locally convex space (LCS) is often assumed to be [[Hausdorff space]].

Locally convex (topological vector) spaces are the standard setup for much of the contemporary [[functional analysis]]. 


## Functionals 

One reason why locally convex TVS are important is that lots of (continuous!) [[functional]]s exist on them, at least if one assumes an appropriate choice principle, e.g., [[axiom of choice]] or [[ultrafilter theorem]] (or just [[dependent choice]] for a [[separable space]]). This fact is encapsulated in the [[Hahn-Banach theorem]]; a nice exposition is given in Terry Tao's [lecture notes](http://terrytao.wordpress.com/2009/01/26/245b-notes-6-duality-and-the-hahn-banach-theorem/). By way of contrast, a TVS which is _not_ locally convex, such as the topological vector space $L^p([0, 1])$ where $0 \lt p \lt 1$, need not have any (nonzero) functionals at all. 

The collections of functionals on a LCTVS is used in a way analogous to the collection of coordinate projections $pr_i:\mathbb{R}^n\to \mathbb{R}$. For example, curves in a LCTVS over the reals can be composed with functionals to arrive at a collection of functions $\mathbb{R} \to \mathbb{R}$ which are analogous to the 'components' of the curve.

In one respect, a locally convex TVS is a [[nice space]] in that there are enough co-probes by maps to the base field.


[[!redirects locally convex]]
[[!redirects locally convex spaces]]
[[!redirects locally convex vector space]]
[[!redirects locally convex vector spaces]]
[[!redirects locally convex topological vector space]]
[[!redirects locally convex topological vector spaces]]
[[!redirects locally convex TVS]]
[[!redirects LCS]]
[[!redirects LCTVS]]