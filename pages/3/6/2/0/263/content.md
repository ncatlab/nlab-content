<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _category with [[weak equivalence]]s_ is an ordinary [[category]] with a class of morphisms called 'weak equivalences' that include the isomorphisms, but also typically other morphisms.  Such a category can be thought of as a presentation of an [[(∞,1)-category]] that gives only the 1-morphisms and the information about which of these 1morphisms should become _equivalences_ in the full [[(∞,1)-category]].

The desired $(\infty,1)$-category in question can be constructed from such a "presentation" by "freely adjoining inverse equivalences" to the weak equivalences, in a suitable $(\infty,1)$-categorical sense.  One way to make this precise is [[simplicial localization]].  A given $(\infty,1)$-category can admit many such presentations. See the section _[Presentations of (∞,1)-categories](#InfCatPres)_ below for more details.


## Definition

A **category with weak equivalences** is a [[category]] $C$ equipped with a [[subcategory]] (in the na&#239;ve sense) $W \subset C$

* which contains all isomorphisms of $C$;

* which satisfies "two-out-of-three": for $f, g$ any two composable morphisms of $C$, if two of $\{f, g, g \circ f\}$ are in $W$, then so is the third.


## Examples and refinements

Often categories with weak equivalences are equipped with further extra structure that helps with computing the [[simplicial localization]], the [[homotopy category]] and [[derived functor]]s. 

* In a [[homotopical category]] the condition on the weak equivalences is slightly stronger.

* In a [[category of fibrant objects]] there are additional auxiliary morphisms called fibrations.

* In a [[Waldhausen category]] there are additional auxiliary morphisms called cofibrations.

* In a [[model category]] there are both of these additional auxiliary classes of morphisms with special interrelation between them.


## Remarks 

* If we denote by $Core(C)$ the maximal subgroupoid of $C$, then we have a chain of inclusions
$ 
 Core(C) \hookrightarrow W \hookrightarrow C
$.

* Sometimes it is useful to ask further closure properties of the weak equivalences.  One such is the "2-out-of-6" property (if $g f$ and $h g$ are weak equivalences, then so are $f$, $g$, $h$, and $h g f$) in which case one speaks of a [[homotopical category]].  Another such is closure under [[retract|retracts]] in the [[arrow category]] of $C$.  Both are satisfied automatically by any [[model category]].

* Many categories with weak equivalences can be equipped with the further structure of a [[model category]]. On the other hand, some categories with weak equivalences can _not_ be equipped with a useful structure of a model category.  In particular, categories of diagrams in a model category do not always inherit a useful model structure.  Several concepts exist that weaken the axioms of a model category in order to still obtain useful results in such a case -- for instance a [[category of fibrant objects]].



## Presentation of $(\infty,1)$-categories {#InfCatPres}

A category $C$ with weak equivalences serves as a presentation of an [[(∞,1)-category]] $\mathbf{C}$ with the same objects and at leaast the 1-morphisms of $C$, and such that every weak equivalence in $C$ becomes a true equivalence (a [[homotopy equivalence]]) in $\mathbf{C}$.

The procedure (or one of its equivalent variants) that constructs the [[(∞,1)-category]] $\mathbf{C}$ from the category with weak equivalences $C$ is called Dwyer-Kan [[simplicial localization]].

In fact, every [[(∞,1)-category]] may be presented this way (and indeed [[posets]] equipped with [[wide subcategory|wide subcategories]] of morphisms called weak equivalences) are sufficient. This is discussed at

* [[model structure on categories with weak equivalences]] .

Alternatively, we may further project to the 1-category in which all weak equivalences become true [[isomorphism]]s: this is the [[homotopy category]] of $C$ with respect to $W$. Equivalently this is the [[homotopy category of an (∞,1)-category]] of $\mathbf{C}$.

Note that the category with weak equivalences which presents a given $(\infty,1)$-category will not, in general, be the [[homotopy category of an (∞,1)-category|homotopy category]] of this $(\infty,1)$-category; more "flab" must be built into it.  



## Discussion

+-- {: .query}

> An earlier version of this entry led to the following discussion

Surely you don\'t mean to suggest (with '*The* $(\infty,1)$-category is recovered [...]') that the composite
$$ (\infty,1) Cat \to Cat \to (\infty,1) Cat $$
is equivalent to the identity, do you?

[[Mike Shulman]]: I've tried to clarify the statements being made.

[[Urs Schreiber]]: Thanks. You mention homotopy categories. But I understood the question differently: supppose we start with an $(\infty,1)$-category in its incarnations as a simplicially enriched category. Then form the ordinary category obtained by retaining of all simplicial hom-sets only the set of 0-cells, now the set of morphisms. Mark those morphisms as weak equivalences that were equivalences in the original $(\infty,1)$-category. Then pass to the simplicial localization of the resulting category with weak equivalences. How does that relate to the original $(\infty,1)$-category?

[[Mike Shulman]]: Also an interesting question!  However, I believe the answer is "it's not the same."  Consider simplicially enriched groupoids, meaning simplicially enriched categories in which each category $C_n$ defined by $C_n(x,y) = C(x,y)_n$ is a groupoid.  The fundamental $\infty$-groupoid of *any* space can be realized as such a simplicially enriched groupoid.  However, when we discard the higher cells in a simplicially enriched groupoid, we obtain simply an ordinary groupoid, whose simplicial localization is just itself.  So in this case, the composite operation in question is the 1-truncation.
=--





[[!redirects 2-out-of-3 property]]
[[!redirects two-out-of-three property]]
