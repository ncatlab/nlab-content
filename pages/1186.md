# Idea #

A _presentable $(\infty,1)$-category_ is, as the name suggests, an [[(infinity,1)-category]] that can be conveniently "presented by simpler means".

There is a wealth of equivalent ways to make precise what this means, which are listed below. The two most important ones are maybe the following:

## presentation by simplicial model categories ##

Presentable $(\infty,1)$-categories are precisely those [[(infinity,1)-category|(infinity,1)-category]] which are _presented_ by a combinatorial [[simplicial model category]] $C$ in that they are the full [[simplicially enriched category|simplicial subcategory]] $C^\circ \hookrightarrow C$ on fibrant-cofibrant objects of $C$ 

(Or, equivalently, the [[quasi-category]] associated to this [[simplicially enriched category]]).

Partly due to the fact that [[simplicial model category|simplicial model categories]] have been studied for a longer time than [[(infinity,1)-category|(infinity,1)-categories]], many $(\infty,1)$-categories are indeed handled in terms in terms of such a presentation by a [[simplicial model category]]. 

The canonical example is the presentation of the [[(infinity,1)-category of (infinity,1)-sheaves]] on an ordinary (1-categorical) [[site]] $S$ by the simplicial [[model structure on simplicial presheaves|model category of simplicial presheaves]] on $S$.


## presentation by conglomerates of objects in a small $(\infty,1)$-category ##

From another perspective, the notion of a presentable [[(infinity,1)-category]] is a means to handle [[large category|large]] $(\infinity,1)$-categories in terms of small ones.
It is is a slight refinement of the notion of an [[accessible (infinity,1)-category]].

A _presentable_ $(\infty,1)$-category is one which may be [[large category|large]], but can entirely be _presented_ as an $(\infty,1)$-category of "conglomerates of objects" in a small $(\infty,1)$-category -- precisely: that it is [[accessible (infinity,1)-category|accessible]] but also admits all small [[limit in quasi-categories|colimits]].

This means that it is desireable to get hold of presentable $(\infty,1)$-categories. The following long list of equivalent definitions allows for many equivalent characterization of presentable $(\infty,1)$-categories. In particular, all [[(infinity,1)-category of (infinity,1)-sheaves|(infinity,1)-categories of (infinity,1)-sheaves]] are presentable.

# Definition #

An [[(infinity,1)-category]] $C$ is **presentable** precisely 

* if there exists a combinatorial [[simplicial model category]] $A$ and an equivalence $ C \simeq N(A^\circ)$,
where $A^\circ$ is the full [[SSet]]-subcategory of $A$ on fibrant-cofibrant objects and where $N(A^\circ)$ is the [[quasi-category]] arising as the simplicial nerve of $A^\circ$.


This is equivalent to all of the following equivalent statements.


* $C$ is [[accessible (infinity,1)-category|accessible]] and admits small [[limit in quasi-categories|colimits]];

* there exists a small $(\infty,1)$-category $D$ and a functor $f: PSh(D) \to C$ from the [[(infinity,1)-presheaf|(infinity,1)-category of (infinity,1)-presheaves]] on $D$ with a [[(infinity,1)-fully faithful functor|fully faithful]] [[right adjoint]].


  * (if in addition $f$ is left [[exact functor|exact]] then $C$ is an [[(infinity,1)-category of (infinity,1)-sheaves]] on $C$)

* $C$ is [[accessible (infinity,1)-category|accessible]] and for every [[cardinal number|regular cardinal]] $\kappa$ the full subcategory $C^\kappa$ (...explanation to be filled in...) admits $\kappa$-small [[limit in quasi-categories|colimits]];


* there exists a [[cardinal number|regular cardinal]] $\kappa$ such that $C$ is $\kappa$-[[accessible (infinity,1)-category|accessible]] and $C^\kappa$ ([explanation]()) admits $\kappa$-small [[limit in quasi-categories|colimits]];

* there exists a [[cardinal number|regular cardinal]] $\kappa$, a small $(\infty,1)$-category $D$ with $\kappa$-small [[limit in quasi-categories|colimits]] and an equivalence $Ind_\kappa D \stackrel{\simeq}{\to} D$ of $D$ with the category of $\kappa$-[[ind-object]]s of $D$;

* $C$ is [[locally small (infinity,1)-category|locally small]], admits small colimits, and there exists a [[cardinal number|regular cardinal]] $\kappa$ and a small [[set]] $Cmptcs$ of $\kappa$-[[compact object in an (infinity,1)-category|compact object]]s of $C$ such that every object in $C$ is a [[limit in quasi-categories|colimit]] of a small diagram in the full subcategory on $Cmpcts$.




# The (infinity,1)-category of presentable $(\infty,1)$-categories #

(...)


# References #

This is the topic of section 5 and section A.3.7 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

The long list of equivalent statements above is theorem 5.5.1.1., which is originally due to Carlos Simpson.


The characterization in terms of simplicial model categories is proposition A.3.7.6.