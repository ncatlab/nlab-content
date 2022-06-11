
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _category with [[weak equivalence]]s_ is an ordinary [[category]] with a [[class]] of [[morphisms]] singled out -- called 'weak equivalences' -- that include the [[isomorphisms]], but also typically other morphisms.  Such a category can be thought of as a _presentation_ of an [[(∞,1)-category]] that defines explicitly only the 1-morphisms (as opposed to [[n-morphism]]s for all $n$) and the information about which of these morphisms should become _[[equivalence in an (infinity,1)-category|equivalences]]_ in the full [[(∞,1)-category]].

The desired $(\infty,1)$-category in question can be constructed from such a "presentation" by "freely adjoining inverse equivalences" to the [[weak equivalences]], in a suitable $(\infty,1)$-categorical sense.  One way to make this precise is by the process of _[[simplicial localization]]_ .  A single $(\infty,1)$-category can admit many different such presentations. See the section _[Presentations of (∞,1)-categories](#InfCatPres)_ below for more details.


## Definition

A **category with weak equivalences** is a [[category]] $C$ equipped with a [[subcategory]] (in the na&#239;ve sense) $W \subset C$

* which contains all [[isomorphisms]] of $C$;

* which satisfies [[two-out-of-three]]: for $f, g$ any two composable morphisms of $C$, if two of $\{f, g, g \circ f\}$ are in $W$, then so is the third.


## Examples and refinements

Often categories with weak equivalences are equipped with further extra [[structure]] that helps with computing the [[simplicial localization]], the [[homotopy category]] and [[derived functor]]s. 

* In a [[homotopical category]] the condition on the weak equivalences is slightly stronger; see below.

* In a [[relative category]] the condition is slightly weaker. Relative categories have a good [[homotopy theory]]. See at _[[relative category]]_.

* In a [[category of fibrant objects]] there are additional auxiliary morphisms called fibrations.

* In a [[Waldhausen category]] there are additional auxiliary morphisms called [[cofibrations]].

* In a [[model category]] there are both of these additional auxiliary classes of morphisms with special interrelation between them.

Other variants include

* [[Cartan-Eilenberg category]], ...

## Additional conditions

Three additional conditions which categories with weak equivalences often satisfy are:

* the weak equivalences are closed under [[retracts]], as a subcategory of the [[arrow category]] of $C$.

* the weak equivalences satisfy the [[two-out-of-six property]]; in this case the category is called a [[homotopical category]].

* the weak equivalences are *saturated* in the sense that any morphism which becomes an isomorphism in the [[localization]] $C[W^{-1}]$ is already a weak equivalence.  (This is unrelated to the notion of [[saturated class of maps]] used in the theory of [[weak factorization systems]].)

In fact, these three conditions are closely related.

* Obviously, saturation implies closure under retracts and two-out-of-six, since the isomorphisms in any category satisfy both.

* In any model category, all three conditions hold automatically.

* If the weak equivalences admit a [[calculus of fractions]], or a well-behaved class of cofibrations or fibrations, then the three conditions are equivalent.  See [[two-out-of-six property]] for the proofs, which are from [[Categories and Sheaves]] (for the calculus of fractions) and [Blumberg-Mandell](#BlumbergMandell) (for the case of cofibrations, in the context of a [[Waldhausen category]]).


## Remarks 

* If we denote by $Core(C)$ the [[core]] of $C$ -- the maximal sub[[groupoid]] of $C$ -- then we have a chain of inclusions
$ 
 Core(C) \hookrightarrow W \hookrightarrow C
$.

* Many categories with weak equivalences can be equipped with the further [[structure]] of a [[model category]]. On the other hand, some categories with weak equivalences can _not_ be equipped with a useful structure of a model category.  In particular, categories of [[diagrams]] in a model category do not always inherit a useful model structure (on the other hand often they do, see [[model structure on functors]]).  Several concepts exist that weaken the axioms of a model category in order to still obtain useful results in such a case -- for instance a [[category of fibrant objects]].

* Although categories of weak equivalences do not usually have limits and colimits, they are often [[accessible category|accessible]], and can be presented as an [[injectivity class]] or a [[cone-injectivity class]].  This is used in Smith's recognition theorem for [[combinatorial model categories]] and can be "algebraicized" as in [Bourke17](#Bourke17).

## Presentation of $(\infty,1)$-categories {#InfCatPres}

A category $C$ with weak equivalences serves as a presentation of an [[(∞,1)-category]] $\mathbf{C}$ with the same objects and at least the 1-morphisms of $C$, and such that every weak equivalence in $C$ becomes a true equivalence (a [[homotopy equivalence]]) in $\mathbf{C}$.

The procedure (or one of its equivalent variants) that constructs the [[(∞,1)-category]] $\mathbf{C}$ from the category with weak equivalences $C$ is called Dwyer-Kan [[simplicial localization]].

In fact, every [[(∞,1)-category]] may be presented this way (and indeed [[posets]] equipped with [[wide subcategory|wide subcategories]] of morphisms called weak equivalences are sufficient). This is discussed at

* [[model structure on categories with weak equivalences]].

Alternatively, we may further project to the 1-category in which all weak equivalences become true [[isomorphism]]s: this is the [[homotopy category]] of $C$ with respect to $W$. Equivalently this is the [[homotopy category of an (∞,1)-category]] of $\mathbf{C}$.

Note that the category with weak equivalences which presents a given $(\infty,1)$-category can not, in general, be taken to be the [[homotopy category of an (∞,1)-category|homotopy category]] of that $(\infty,1)$-category; more "flab" must be built into it.

It also cannot, in general, be the underlying 1-category of a simplicially enriched presentation of that $(\infty,1)$-category.  For instance, every $\infty$-groupoid can be realized as a simplicially enriched groupoid, but the underlying 1-category of a simplicially enriched groupoid is a 1-groupoid, which cannot be localized any further to produce a non-1-truncated $\infty$-groupoid.

## Related concepts

* [[localizer]], [[modelizer]]

* [[localizing subcategory]]

* [[relative category]]

[[!include algebraic model structures - table]]

## References

* {#Bourke17} [[John Bourke]], *Equipping weak equivalences with algebraic structure*, [arXiv:1712.02523](https://arxiv.org/abs/1712.02523)

[[!redirects categories with weak equivalences]]
