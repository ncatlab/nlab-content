<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

##Idea##

A _category with [[weak equivalence]]s_ is an ordinary [[category]] with a class of morphisms called 'weak equivalences' that include the isomorphisms, but also typically other morphisms.  Such a category can be thought of as a presentation of an [[(∞,1)-category]] that gives only the 1-morphisms and the information about which of these 1morphisms should become _equivalences_ in the full [[(∞,1)-category]].

The desired $(\infty,1)$-category in question can be constructed from such a "presentation" by "freely adjoining inverse equivalences" to the weak equivalences, in a suitable $(\infty,1)$-categorical sense.  One way to make this precise is [[simplicial localization]].  A given $(\infty,1)$-category can admit many such presentations.  It is not entirely clear whether *every* $(\infty,1)$-category admits at least one such presentation, although it seems not unlikely.

Note that the category with weak equivalences which presents a given $(\infty,1)$-category will not, in general, be the [[homotopy category of an (∞,1)-category|homotopy category]] of this $(\infty,1)$-category; more "flab" must be built into it.  However, the homotopy category of an $(\infty,1)$-category can be recovered directly from any presentation of it, by freely adjoining inverse *isomorphisms* to the weak equivalences, resulting in the [[homotopy category]] of the category with weak equivalences.

+-- {: .query}
Surely you don\'t mean to suggest (with '*The* $(\infty,1)$-category is recovered [...]') that the composite
$$ (\infty,1) Cat \to Cat \to (\infty,1) Cat $$
is equivalent to the identity, do you?

[[Mike Shulman]]: I've tried to clarify the statements being made.

[[Urs Schreiber]]: Thanks. You mention homotopy categories. But I understood the question differently: supppose we start with an $(\infty,1)$-category in its incarnations as a simplicially enriched category. Then form the ordinary category obtained by retaining of all simplicial hom-sets only the set of 0-cells, now the set of morphisms. Mark those morphisms as weak equivalences that were equivalences in the original $(\infty,1)$-category. Then pass to the simplicial localization of the resulting category with weak equivalences. How does that relate to the original $(\infty,1)$-category?

[[Mike Shulman]]: Also an interesting question!  However, I believe the answer is "it's not the same."  Consider simplicially enriched groupoids, meaning simplicially enriched categories in which each category $C_n$ defined by $C_n(x,y) = C(x,y)_n$ is a groupoid.  The fundamental $\infty$-groupoid of *any* space can be realized as such a simplicially enriched groupoid.  However, when we discard the higher cells in a simplicially enriched groupoid, we obtain simply an ordinary groupoid, whose simplicial localization is just itself.  So in this case, the composite operation in question is the 1-truncation.
=--

Often categories with weak equivalences are equipped with further extra structure that helps with computing the [[simplicial localization]], the [[homotopy category]] and [[derived functor]]s. 

* In a [[homotopical category]] the condition on the weak equivalences is slightly stronger.

* In a [[category of fibrant objects]] there are additional auxiliary morphisms called fibrations.

* In a [[Waldhausen category]] there are additional auxiliary morphisms called cofibrations.

* In a [[model category]] there are both of these additional auxiliary classes of morphisms with special interrelation between them.


## Definition ##

A **category with weak equivalences** is a [[category]] $C$ equipped with a [[subcategory]] (in the na&#239;ve sense) $W \subset C$

* which contains all isomorphisms of $C$;

* which satisfies "two-out-of-three": for $f, g$ any two composable morphisms of $C$, if two of $\{f, g, g \circ f\}$ are in $W$, then so is the third.

## Purpose ##

The idea is that $C$ is a presentation of a [[higher category theory|higher category]] with higher morphisms, and that the weak equivalences are those morphisms which would become true [[equivalence]]s in this higher category.

This higher category may be reconstructed by Dwyer-Kan localization as an $(\infty,1)$-[[(infinity,1)-category|category]].

Alternatively, we may further project to the 1-category in which all weak equivalences become true [[isomorphism]]s: this is the [[homotopy category]] of $C$ with respect to $W$.

## Remarks ##

* If we denote by $Core(C)$ the maximal subgroupoid of $C$, then we have a chain of inclusions
$ 
 Core(C) \hookrightarrow W \hookrightarrow C
$.

* Sometimes it is useful to ask further closure properties of the weak equivalences.  One such is the "2-out-of-6" property (if $g f$ and $h g$ are weak equivalences, then so are $f$, $g$, $h$, and $h g f$) in which case one speaks of a [[homotopical category]].  Another such is closure under [[retract|retracts]] in the [[arrow category]] of $C$.  Both are satisfied automatically by any [[model category]].

* Many categories with weak equivalences can be equipped with the further structure of a [[model category]]. On the other hand, some categories with weak equivalences can _not_ be equipped with a useful structure of a model category.  In particular, categories of diagrams in a model category do not always inherit a useful model structure.  Several concepts exist that weaken the axioms of a model category in order to still obtain useful results in such a case -- for instance a [[category of fibrant objects]].

[[!redirects 2-out-of-3 property]]
[[!redirects two-out-of-three property]]
