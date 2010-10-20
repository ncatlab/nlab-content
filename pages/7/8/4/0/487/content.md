+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition 

A category is **balanced** if every [[monomorphism|monic]] [[epimorphism|epic]] morphism is an [[isomorphism]].  Monic epics are  sometimes called [[bimorphism]]s.


## Remarks 

* The possibility of monic epics that are not isomorphisms does not survive any strengthening of "monic" or "epic."  Any monic [[extremal epimorphism]] is necessarily an isomorphism, and therefore so is any monic [[strong epimorphism]] or [[regular epimorphism]] (and dually).  It follows that if all epics, or all monos, are extremal, then the category is automatically balanced.

* In an "unbalanced" category it is frequently the case that the monomorphisms, the epimorphisms, or both, are not the "right" notion to consider and should be replaced by their [[extremal epimorphism|extremal]], [[strong epimorphism|strong]], or [[regular epimorphism|regular]] counterparts.


## Examples and non-examples 

* Any [[topos]] (in fact, any [[pretopos]]) is balanced.  Of course, this includes [[Set]].

* Some algebraic categories, such as [[Grp|the category of groups]], are balanced.

* Any [[abelian category]] is balanced.

* The category of rings is not balanced; $Z\hookrightarrow Q$ is monic and epic but not an isomorphism.

* Topological categories are rarely balanced; in [[Top]], for example, the monic epimorphisms are the continuous bijections.  However, the category of [[compact Hausdorff space]]s is balanced.

* In a [[partial order|poset]] or a [[quiver]], _every_ morphism is both monic and epic; thus such categories are "as far as possible from being balanced."


[[!redirects balanced categories]]