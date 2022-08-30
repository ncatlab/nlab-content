> This entry is about a category whose objects form a [[type]] or [[infinity-groupoid]] rather than a [[set]]. For the specific type of paracategory also known as a *precategory*, in which all the composites are generated from binary and nullary ones, see [[paracategory]]. 

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

In [[homotopy type theory]] (or more generally [[intensional type theory]]), when defining a [[category]] (meaning a *1-category*), one has to decide whether to impose an [[h-level]] restriction on the [[type]] of [[objects]].  A **precategory** is a category in which *no* such restriction is imposed; thus the type of objects may be a set, or a 1-type, or an even higher type.

Surprisingly much [[category theory]] can be done purely with precategories, and some authors call them merely "categories".  However, there are notable differences between precategories and the familiar notion of "category" from [[set theory|set-theoretic]] foundations.  Moreover, the two do not coincide under the standard interpretation of homotopy type theory into set theory (e.g. the model in [[simplicial sets]]).  Indeed, the semantics of a precategory is the 1-categorical analogue of a [[Segal space]].

Alternative notions of "1-category" in homotopy type theory include [[strict categories]], whose type of objects is a set, and [[univalent categories]], whose type of objects is a 1-type whose identifications coincide with isomorphisms for the category structure.  The latter are generally better-behaved and include naturally-occurring examples, but the former are sometimes technically useful.

## Definition

A **precategory** $\mathcal{C}$ consists of 

* a [[type]] of [[objects]] $Ob(\mathcal{C})$, 
* for each object $A:Ob(\mathcal{C})$ and $B:Ob(\mathcal{C})$, a [[set]] $Hom(A, B)$ of [[morphisms]]
* for each object $A:Ob(\mathcal{C})$, $B:Ob(\mathcal{C})$, and $C:Ob(\mathcal{C})$, a [[binary function]] 
$$(-)\circ_{A, B, C}(-) :Hom(B, C) \times Hom(A, B) \to Hom(A, C)$$
* for each object $A:Ob(\mathcal{C})$, a morphism $\mathrm{id}_A:Hom(A, A)$
* such that 
  * the composition of morphisms is [[associative]]: for each object $A:Ob(\mathcal{C})$, $B:Ob(\mathcal{C})$, $C:Ob(\mathcal{C})$, and $D:Ob(\mathcal{C})$, and for each morphism $f:Hom(A, B)$, $g:Hom(B, C)$, and $h:Hom(C, D)$, 
$$h \circ_{A, C, D} (g \circ_{A, B, C} f) = h \circ_{B, C, D} (g \circ_{A, B, D} f)$$
  * the composition of morphisms satisfies the left and right [[unit laws]]: for each object $A:Ob(\mathcal{C})$ and $B :Ob(\mathcal{C})$ and morphism $f:Hom(A, B)$, $\mathrm{id}_B \circ_{A, B, B} f = f$ and $f \circ_{A, A, B} \mathrm{id}_A = f$.

Of course, the latter two axioms are actually inhabitants of the [[identity type]], hence are data included in the definition just like the first four.  However, since each $Hom(A,B)$ is a set, such equalities are (typally) unique whenever they exist, so in most cases their presence as data can be ignored.

## Remarks

* The interpretation of the notion of precategory in the model of homotopy type theory in [[simplicial sets]] yields a [[Segal space]] in which the morphism $A_1 \to A_0 \times A_0$ has homotopically discrete fibers.

* The definition of precategory is evidently a type-theoretic notion of the definition of category with [[category#AFamilyOfCollectionsOfMorphisms|a family of collections of morphisms]].  An equivalent definition analogous to the definition of category with [[category#OneCollectionOfMorphisms|one collection of morphisms]] could be given, but it would be much less convenient to use.  In particular, the "type of all morphisms" $\sum_{A,B:Ob(\mathcal{C})} Hom(A,B)$ in a precategory is *not* itself a set, since it can incorporate nontrivial identifications from $Ob(\mathcal{C})$; the "hom-types are sets" condition in a one-type-of-morphisms definition of precategory would have to be stated as "the function $\mathcal{C}_1 \to \mathcal{C}_0$ is 0-truncated" (i.e. its fibers are sets).


## See also

* [[category]]

* [[strict category]]

* [[univalent category]]

* [[wild category]]

* [[Segal space]]

* [[complete Segal space]]

## References

* {#UFP13} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* {#AhrensKapulkinShulman13} [[Benedikt Ahrens]], [[Chris Kapulkin]], [[Michael Shulman]], _Univalent categories and the Rezk completion_, Mathematical Structures in Computer Science **25** 5 (*From type theory and homotopy theory to Univalent Foundations of Mathematics*),  (2015) 1010-1039   $[$[arXiv:1303.0584](https://arxiv.org/abs/1303.0584), [doi:10.1007/978-3-319-21284-5_14](https://doi.org/10.1007/978-3-319-21284-5_14)$]$

[[!redirects precategories]]
[[!redirects prefunctor]]
[[!redirects prefunctors]]