# Idea #

The notion of a presentable [[(infinity,1)-category]] is a means to handle [[large category|large]] $(\infinity,1)$-categories.
It is is a slight refinement of the notion of an [[accessible (infinity,1)-category]].

A _presentable_ $(\infty,1)$-category is one which may be [[large category|large]], but can entirely be _presented_ as an $(\infty,1)$-category of "conglomerates of objects" in a small $(\infty,1)$-category -- precisely: that it is [[accessible (infinity,1)-category|accessible]] but also admits all small [[limit in quasi-categories|colimits]].

This means that it is desireable to get hold of presentable $(\infty,1)$-categories. The following long list of equivalent definitions allows for many equivalent characterization of presentable $(\infty,1)$-categories. In particular, all [[(infinity,1)-category of (infinity,1)-sheaves|(infinity,1)-categories of (infinity,1)-sheaves]] are presentable.

# Definition #

An [[(infinity,1)-category]] $C$ is **presentable** it it satisfies the following equivalent conditions:

* $C$ is [[accessible (infinity,1)-category|accesible]] and admits small [[limit in quasi-categories|colimits]];

* there exists a small $\infty$-category $D$ and a functor $f: PSh(D) \to D$ from the [[(infinity,1)-presheaf|(infinity,1)-presheaves]] to $D$ with a [[(infinity,1)-fully faithful functor|fully faithful]] [[right adjoint]]

  * (if in addition $f$ is left [[exact functor|exact]] then $C$ is an [[(infinity,1)-category of (infinity,1)-sheaves]] on $C$)

* $C$ is [[accessible (infinity,1)-category|accessible]] and for every [[cardinal number|regular cardinal]] $\kappa$ the full subcategory $C^\kappa$ ([explanation]()) admits $\kappa$-small [[limit in quasi-categories|colimits]];

+--{: .query}
What are these 'explanation' links supposed to do?  ---Toby
=--

* there exists a [[cardinal number|regular cardinal]] $\kappa$ such that $C$ is $\kappa$-[[accessible (infinity,1)-category|accesible]] and $C^\kappa$ ([explanation]()) admits $\kappa$-small [[limit in quasi-categories|colimits]];

* there exists a [[cardinal number|regular cardinal]] $\kappa$, a small $(\infty,1)$-category $D$ with $\kappa$-small [[limit in quasi-categories|colimits]] and an equivalence $Ind_\kappa D \stackrel{\simeq}{\to} D$ of $D$ with the category of $\kappa$-[[ind-object]]s of $D$;

* $C$ is [[locally small (infinity,1)-category|locally small]], admits small colimits, and there exists a [[cardinal number|regular cardinal]] $\kappa$ and a small [[set]] $Cmptcs$ of $\kappa$-[[compact object in an (infinity,1)-category|compact object]]s of $C$ such that every object in $C$ is a [[limit in quasi-categories|colimit]] of a small diagram in the full subcategory on $Cmpcts$.

#Remark#

* The proof of the equivalence of these conditions is due to Carlos Simpson.


# The (infinity,1)-category of presentable $(\infty,1)$-categories #

(...)


# References #

This is the topic of section 5 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

The equivalence of the above conditions is theorem 5.5.1.1.