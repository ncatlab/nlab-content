#Contents#
* automatic table of contents goes here
{:toc}

# Idea #

A _presentable $(\infty,1)$-category_ is, as the name suggests, an [[(∞,1)-category]] that can be conveniently "presented by simpler means". It is the analog of the notion of [[presentable category]] for ordinary categories.

+--{: .query}
[[Mike Shulman]]: See [[presentable category]] for an objection to this terminology.  I prefer the standard term "locally presentable".
=--

There is a wealth of equivalent ways to make precise what this means, which are listed below. The two most important ones are maybe the following:

## presentation by simplicial model categories ##

Presentable $(\infty,1)$-categories are precisely those [[(∞,1)-categories]] which are _presented_ by a [[combinatorial simplicial model category]] $C$ in that they are the full [[simplicially enriched category|simplicial subcategory]] $C^\circ \hookrightarrow C$ on fibrant-cofibrant objects of $C$ 

(Or, equivalently, the [[quasi-category]] associated to this [[simplicially enriched category]]).

Under this presentation,
equivalence of presentable $(\infty,1)$-categories corresponds precisely
to spans of [[Quillen equivalence]]s between presenting
[[combinatorial simplicial model category|combinatorial simplicial model categories]].

$C^\circ$ and $D^\circ$ are equivalent as $(\infty,1)$-categories precisely
if there exists a chain of simplicial Quillen equivalence

$$
  C 
  \stackrel{\leftarrow}{\to}
  \stackrel{\to}{\leftarrow}
  \stackrel{\leftarrow}{\to}
  \cdots  
  D.
$$

This is remark A.3.7.7 in [[Higher Topos Theory|HTT]].



Partly due to the fact that [[simplicial model category|simplicial model categories]] have been studied for a longer time -- partly because they are simply more tractable -- than [[(∞,1)-categories]], many $(\infty,1)$-categories are indeed handled in terms of such a presentation by a [[simplicial model category]]. 

The canonical example is the presentation of the [[(∞,1)-category of (∞,1)-sheaves]] on an ordinary (1-categorical) [[site]] $S$ by the simplicial [[model structure on simplicial presheaves|model category of simplicial presheaves]] on $S$.


## presentation by conglomerates of objects in a small $(\infty,1)$-category ##

From another perspective, the notion of a presentable [[(∞,1)-category]] is a means to handle [[large category|large]] $(\infty,1)$-categories in terms of small ones.
It is is a slight refinement of the notion of an [[accessible (∞,1)-category]].

A _presentable_ $(\infty,1)$-category is one which may be [[large category|large]], but can entirely be _presented_ as an $(\infty,1)$-category of "conglomerates of objects" in a small $(\infty,1)$-category -- precisely: that it is [[accessible (infinity,1)-category|accessible]] but also admits all small [[limit in quasi-categories|colimits]].

This means that it is desireable to get hold of presentable $(\infty,1)$-categories. The following long list of equivalent definitions allows for many equivalent characterization of presentable $(\infty,1)$-categories. In particular, all [[(infinity,1)-category of (infinity,1)-sheaves|(∞,1)-categories of (∞,1)-sheaves]] are presentable.

# Definition #

An [[(∞,1)-category]] $C$ is **presentable** precisely 

* if there exists a [[combinatorial simplicial model category]] $A$ and an equivalence $ C \simeq N(A^\circ)$.


  Here $A^\circ$ is the full [[SSet]]-subcategory of $A$ on fibrant-cofibrant objects and where $N(A^\circ)$ is the [[quasi-category]] arising as the [[homotopy coherent nerve]] of $A^\circ$.

This is equivalent to all of the following equivalent statements.


* $C$ is [[accessible (infinity,1)-category|accessible]] and admits small [[limit in quasi-categories|colimits]];

* $C$ is the [[localization of an (∞,1)-category|localization]] of an [[(∞,1)-category of (∞,1)-presheaves]]:

  there exists a small $(\infty,1)$-category $D$ and a functor $f: PSh(D) \to C$ from the [[(infinity,1)-presheaf|(∞,1)-category of (∞,1)-presheaves]] on $D$ with a [[(infinity,1)-fully faithful functor|fully faithful]] [[right adjoint]].

  * (if in addition $f$ is left [[exact functor|exact]] then $C$ is an [[(∞,1)-category of (∞,1)-sheaves]] on $C$)

* $C$ is [[accessible (infinity,1)-category|accessible]] and for every [[cardinal number|regular cardinal]] $\kappa$ the full subcategory $C^\kappa$ (...explanation to be filled in...) admits $\kappa$-small [[limit in quasi-categories|colimits]];


* there exists a [[cardinal number|regular cardinal]] $\kappa$ such that $C$ is $\kappa$-[[accessible (infinity,1)-category|accessible]] and $C^\kappa$ ([explanation]()) admits $\kappa$-small [[limit in quasi-categories|colimits]];

* there exists a [[cardinal number|regular cardinal]] $\kappa$, a small $(\infty,1)$-category $D$ with $\kappa$-small [[limit in quasi-categories|colimits]] and an equivalence $Ind_\kappa D \stackrel{\simeq}{\to} D$ of $D$ with the category of $\kappa$-[[ind-object]]s of $D$;

* $C$ is [[locally small (infinity,1)-category|locally small]], admits small colimits, and there exists a [[cardinal number|regular cardinal]] $\kappa$ and a small [[set]] $Cmptcs$ of $\kappa$-[[compact object in an (infinity,1)-category|compact object]]s of $C$ such that every object in $C$ is a [[limit in quasi-categories|colimit]] of a small diagram in the full subcategory on $Cmpcts$.




# The $(\infty,1)$-category of presentable $(\infty,1)$-categories #

See

* [[symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]]

# References #

This is the topic of section 5 and section A.3.7 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

The long list of equivalent statements above is theorem 5.5.1.1., which is originally due to [[Carlos Simpson]].


The characterization in terms of 
[[combinatorial simplicial model category|combinatorial simplicial model categories]] is [[Higher Topos Theory|HTT, prop A.3.7.6]].


[[!redirects presentable (infinity,1)-categories]]
[[!redirects presentable (∞,1)-category]]
[[!redirects presentable (∞,1)-categories]]