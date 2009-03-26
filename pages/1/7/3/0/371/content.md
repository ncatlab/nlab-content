#Definition#

A **zero object**, or **null object**, is an [[object]] of a [[category]] that is both an [[initial object]] and a [[terminal object]].

#Examples#

* The category of [[pointed set|pointed sets]] has a zero object, namely any one-element set.  

* The trivial group is a zero object in the categories of [[group|groups]] and of [[abelian group|abelian groups]].  

* However, the zero ring is not a zero object in the category of [[ring|rings]], at least as long as rings are required to have units (and ring homomorphisms to preserve them).

* For every category $C$ with a [[terminal object]] $pt$ the [[over category|under category]] $pt \downarrow C$ of [[pointed object]]s in $C$ has a zero object: the morphism $Id_{pt}$.

* In any category [[enriched category|enriched]] over pointed sets or abelian groups, any initial _or_ terminal object is automatically a zero object.  This is a special case of a [[Cauchy limit]].

# Consequences #

In a category with a zero object 0, there is always a canonical morphism from any object $A$ to any other object $B$ called the _[[zero morphism]]_, given by the composite $A\to 0 \to B$. Thus, such a category becomes [[enriched category|enriched]] over pointed sets, a partial converse to the last example above.