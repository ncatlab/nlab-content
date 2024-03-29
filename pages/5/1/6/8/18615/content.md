## Definition

Let $\Lambda$ be a [[directed set]], which we may also view as the associated [[order category]], a directed category. View a [[pro-object]] $X:\Lambda^{op}\to C$ as a family of objects $\{X_\lambda\}_{\lambda\in\Lambda}$ in $C$ and bonding morphisms $p_{\lambda\lambda'}:X_{\lambda'}\to X_\lambda$ whenever $\lambda'\gt\lambda$.

A pro-object $X$ is movable if for every $\lambda\in\Lambda$ there is $\lambda'\gt\lambda$ ('the movability index of $\lambda$') such that for every $\lambda''\gt\lambda'$ there is a morphism $r : X_{\lambda'}\to X_{\lambda''}$ such that 
$p_{\lambda\lambda''} \circ r = p_{\lambda\lambda'}$.

#### Relative version 

Let $C$ be a category and $C_0\subset C$ a full subcategory. $(\Lambda, X, p)$ in pro-$C$ is movable with respect to $C_0$ (or $C_0$-movable) if every $\lambda\in\Lambda$ admits $\lambda'\gt\lambda$ such that for every $\lambda''\gt\lambda$ and every morphism $h:Y\to X_{\lambda'}$ in $C$ such that $Y\in C_0$ there is a morphism 
$r:Y\to X_{\lambda''}$ in pro-$C$ such that 
$$p_{\lambda\lambda''}\circ r = p_{\lambda\lambda'}\circ h.$$

## Movability of topological spaces

Term movability comes from topology where it denotes a property studied by Borsuk and which generalizes the class of topological spaces having the [[shape]] of an [[absolute neighborhood retract]]. This can be restated using expansions by pro-objects. There are versions for topological spaces and for pointed topological spaces. As pointed space is a special case of a pair of topological spaces it is natural to define  the movability of pairs by requiring that there exist an expansion of the pair by the pro-object in the category of pairs in the homotopy category of polyhedra which is movable as an abstract pro-object. 

## Properties

Every [[retract]] in pro-$C$ of a movable pro-object is a movable pro-object.  

Let $\mathcal{F}$ be a full subcategory of the category Grp of groups whose objects are the free groups. Then a pro-group is $\mathcal{F}$-movable iff the underlying pro-object in the category of [[pointed set]]s is movable. A pointed pro-set is movable iff it satisfies the [[Mittag-Leffler property]]. This may be used to show that every retract of a pro-object satisfying Mittag-Leffler property is also Mittag-Leffler.

## Literature

* Ch. II, Sec. 2 in [[S. Mardešić]], J. Segal, _Shape theory_, North Holland 1982