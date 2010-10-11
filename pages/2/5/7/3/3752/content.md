
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The definition of _semicategory_ or _category without units_  is like that of [[category]] but omitting the requirement of [[identity]]-morphisms.

This generalizes the notions of [[semigroup]], [[semiring]], etc: 

* a [[semigroup]] is (the [[hom-set]] of) a semicategory with a single object;

* a [[semiring]] is (the [[hom-set]] of) a semicategory [[enriched category|enriched]] in [[Ab]] with a single object.


Semicategories, like categories, appear as [[semipresheaf|semipresheaves]] on the category with two objects and two morphisms.  

## Definition

A **semicategory* or **category without units** $C$ consists of 

* a [[collection]] $C_0$ of _objects_;

* a collection $C_1$ of _morphisms_ (or _arrows_);

* two maps $s, t : C_1 \to C_0$ called _source_ (or _domain_) and _target_ (or _codomain_);

  * one writes $f : x \to y$ if $s(f) = x$ and $t(f) = y$;

* a rule which assigns to any pair of morphisms $f$, $g$ such that $t(f) = s(g)$ their _composite_ morphism $g \circ f \in C_1$ (also  written $g f$ or sometimes $f;g$&#8212; see [[diagrammatic order]]);

* such that the following properties are satisfied:

  * source and target are respected by composition: $s(g \circ f) = s(f)$ and $t(g\circ f) = t(g)$;

  * composition is _associative_: $(h \circ g)\circ f = h\circ (g \circ f)$ whenever $t(f) = s(g)$ and $t(g) = s(h)$;

People often write $hom(x,y)$, $hom_C(x,y)$, or $C(x,y)$ for the collection of morphisms $f : x \to y$; the latter two have the advantage of making clear which category is being discussed.  People also often write $x \in C$ instead of $x \in C_0$ as a short way to indicate that $x$ is an object of $C$.  Also, some people write $Ob(C)$ and $Mor(C)$ instead of $C_0$ and $C_1$.

## In higher category theory

The concept of semicategory has more or less evident analogs and generalizations in [[higher category theory]].

For models of higher categories by [[simplicial set]]s, i.e. presehaves on the [[simplex category]] (such as [[Kan complex]]es, [[quasi-categories]], [[weak complicial set]]s)  the corresponding semi-category notion is obtained by discarding the degeneracy maps (which are the identity-assigning maps in the simplicial framework), i.e. by considering just presheaves on the subcategory $\Delta_+ \subset \Delta$ on injective morphisms (see the discuss of $\Delta_+$ at [[Reedy model structure]] for more details).

[[Simpson's conjecture]] says that every $\infty$-category has a model where all [[composition]] operations are strict and only the [[unit law]]s hold up to [[coherent]] homotopies. This would mean that the $\infty$-semicategory underlying any $\infty$-category can always be chosen to be strict.

## References

Semicategories and semigroups are mentioned for instance in section 2 in

* W. Dale Garraway, _Sheaves for an involutive quantaloid_ Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 46 no. 4 (2005), p. 243-274  ([numdam](http://www.numdam.org/item?id=CTGDC_2005__46_4_243_0))



[[!redirects semicategories]]

[[!redirects category without units]]
[[!redirects categories without units]]