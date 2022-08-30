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

In [[homotopy type theory]], when defining a [[category]] (meaning a *1-category*), one has to decide whether to impose an [[h-level]] restriction on the [[type]] of [[objects]].  A **precategory** is a category in which *no* such restriction is imposed; thus the type of objects may be a set, or a 1-type, or an even higher type.

Surprisingly much [[category theory]] can be done purely with precategories, and some authors call them merely "categories".  However, there are notable differences between precategories and the familiar notion of "category" from [[set theory|set-theoretic]] foundations.  Moreover, the two do not coincide under the standard interpretation of homotopy type theory into set theory (e.g. the model in [[simplicial sets]]).  Indeed, the semantics of a precategory is the 1-categorical analogue of a [[Segal space]].

Alternative notions of "1-category" in homotopy type theory include [[strict categories]], whose type of objects is a set, and [[univalent categories]], whose type of objects is a 1-type whose identifications coincide with isomorphisms for the category structure.  The latter are generally better-behaved and include naturally-occurring examples, but the former are sometimes technically useful.

## Definition

### In homotopy type theory

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

### In simplicial type theory

In [[simplicial type theory]] a **precategory** is a Segal type whose hom types are 0-truncated and discrete. 

### Internal to a (2, 1)-topos

A similar definition could be found internally in any [[(2,1)-topos]]:

A **precategory object** in a (2, 1)-topos $\mathcal{T}$ is an object $\mathcal{C} \in \mathcal{T}$ with a morphism $Hom: \mathcal{C} \times \mathcal{C} \to Set$, where $Set \in \mathcal{T}$ is a [[discrete object classifier]], such that 

  * for every [[global element]] $A:1 \to \mathcal{C}$, $B:1 \to \mathcal{C}$, and $C:1 \to \mathcal{C}$, where $1 \in \mathcal{T}$ is a [[terminal object]], there is a [[discrete morphism]] $(-)\circ_{A, B, C}(-):(Hom \circ (B, C) \times Hom \circ (A, B)) \to (Hom \circ (A, C))$ in the functor groupoid $1 \to Set$
  * for every global element $A:1 \to \mathcal{C}$, there is a [[discrete morphism]] $id_A:1_{Set} \to Hom \circ (A, A)$ in the functor groupoid $1 \to Set$ 

such that

  * composition is [[associative]]: for $A:1 \to \mathcal{C}$, $B:1 \to \mathcal{C}$, $C:1 \to \mathcal{C}$, and $D:1 \to \mathcal{C}$, and for $f:1_{Set} \to (Hom \circ (A, B))$, $g:1_{Set} \to (Hom \circ (B, C))$, and $h:1_{Set} \to (Hom \circ (C, D))$, 
$$h \circ_{A, C, D} (g \circ_{A, B, C} f) = h \circ_{B, C, D} (g \circ_{A, B, D} f)$$
  * composition satisfies the left and right [[unit laws]]: for $A:1 \to \mathcal{C}$ and $B :1 \to \mathcal{C}$ and $f:1_{Set} \to (Hom \circ (A, B))$, $\mathrm{id}_B \circ_{A, B, B} f = f$ and $f \circ_{A, A, B} \mathrm{id}_A = f$.

## The $(\infty,2)$-category PreCat

There should be an [[(infinity,2)-category|$(\infty,2)$-category]] PreCat whose objects are precategories and whose morphisms are functors between precategories.

PreCat should be a sub-$(\infty,2)$-category of the $(\infty,2)$-category $(\infty,1)Cat$ of [[(infinity,1)-category|$(\infty,1)$-categories]], since precategories are (infinity,1)-categories whose hom-infinity-groupoids are 0-truncated. 

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