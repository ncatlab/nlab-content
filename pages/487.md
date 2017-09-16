# Definition #

A category is **balanced** if every [[bimorphism]] (a morphism which is both [[monomorphism|monic]] and [[epimorphism|epic]]) is an [[isomorphism]].

+--{: .query}
[[Mike Shulman|Mike]]: I don't like the word "bimorphism."  If I've been thinking about [[bicategory|bicategories]] then it sounds like something that is "a morphism up to isomorphism," while if I've been thinking about [[biproduct|biproducts]] it sounds like something that is "both a morphism and a comorphism."  Are monic epics really an important enough concept to deserve its own word?  Can't we just say "monic and epic" or even just "monic epic"?
=--

# Remarks #

* The possibility of monic epics that are not isomorphisms does not survive any strengthening of "monic" or "epic."  Any monic [[extremal epimorphism]] is necessarily an isomorphism, and therefore so is any monic [[strong epimorphism]] or [[regular epimorphism]] (and dually).  It follows that if all epics, or all monos, are extremal, then the category is automatically balanced.

* In an "unbalanced" category it is frequently the case that the monomorphisms, the epimorphisms, or both, are not the "right" notion to consider and should be replaced by their [[extremal epimorphism|extremal]], [[strong epimorphism|strong]], or [[regular epimorphism|regular]] counterparts.


# Examples and non-examples #

* Any [[topos]] (in fact, any [[pretopos]]) is balanced.  Of course, this includes [[Set]].

* Some algebraic categories, such as [[Grp|the category of groups]], are balanced.

* Any [[abelian category]] is balanced.

* The category of rings is not balanced; $Z\hookrightarrow Q$ is monic and epic but not an isomorphism.

* Topological categories are rarely balanced; in [[Top]], for example, the bimorphisms are the continuous bijections.  However, the category of compact Hausdorff spaces is balanced.

* In a [[poset]] or a [[quiver]], _every_ morphism is both monic and epic; thus such categories are "as far as possible from being balanced."
