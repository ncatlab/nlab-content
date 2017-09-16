For a given fixed [[ETCS|category of sets]] $S$, a __Grothendieck [[topos]]__ over $S$ may be defined as a category of [[sheaf|sheaves]] over a [[site]] which is [[small category|small]] relative to $S$, that is a site [[internal category|internal]] to $S$. (The site is not considered part of the structure; different sites may give rise to the same category of sheaves.) 

Giraud characterized Grothendieck toposes as categories satisfying certain exactness and small [[complete category|completeness]] properties (where "small" is again relative to the given category of sets $S$). The exactness properties are elementary (not depending on $S$), and are satisfied in any elementary [[topos]], or even a [[pretopos]].

Giraud\'s theorem characterises Grothendieck toposes as follows:
* a [[locally small category]] with a small [[generating set]],
* with all finite [[limit]]s,
* with all small [[coproduct]]s, which are [[disjoint coproduct|disjoint]], and [[pullback stability|pullback-stable]],
* where all [[congruence]]s have effective [[quotient object]]s, which are also pullback-stable.

These conditions are equivalent to

* a locally small [[pretopos|infinitary pretopos]] with a small generating set.

(See [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Topos#Giraud.27s_axioms).)

This characterisation may be suitable even when the base category $S$ is only a [[pretopos]], although in that case a Grothendieck 'topos' need not actually be a topos. More generally, a Grothendieck topos will inherit properites from $S$, not only having a [[subobject classifier]], but also (for example) having a [[natural numbers object]]. Thus the concept makes sense even with weak [[foundations]] of mathematics, although it may not have all of the usual properties.
