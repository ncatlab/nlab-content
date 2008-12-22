A _category with weak equivalences_ is a [[category]] $C$ equipped with a [[subcategory]] $W \subset C$

* which contains all isomorphisms of $C$;

* which satisfies "two-out-of-three": for $f, g$ any two composable morphisms of $C$, if two of $\{f, g, g \circ f\}$ are in $W$, then so is the third.

#Purpose#

The idea is that $C$ is a 1-truncation of a [[higher category theory|higher category]] with higher morphisms, and that the weak equivalences are those morphisms which would be true [[equivalence]]s in this higher category.

This higher category may be reconstructed by Dwyer-Kan localization as an [[infinity comma one category]].

Alternatively, we may further project to the 1-category in which all weak equivalences become true [[isomorphism]]s: this is the [[homotopy category]] of $C$ with respect to $W$.

#Remarks#

If we denote by $Core(C)$ the maximal subgroupoid of $C$, then we have a chain of inclusions
$ 
 Core(C) \hookrightarrow W \hookrightarrow C
$.