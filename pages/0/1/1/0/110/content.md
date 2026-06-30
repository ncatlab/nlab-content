
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea

The notion of _morphism_, or _mapping_ in [[category theory]] is an abstraction, and generalisation of that notion of [[relation]], [[function]], or [[homomorphism]].

In [[diagram|diagrams]] of [[category|categories]], a morphism  is depicted as the directed edge — the [[arrow]] — of a pair of incident vertex — the [[object|objects]] — in a [[directed graph]].


## Definition

For two objects $x$, and $y$ in a ([[locally small category|locally-small]]) category $A$, the [[set]], 
$Hom _A (x,y)$, is called the [[hom-set]], the [[element|elements]] being morphisms of [[domain]] $x$, and [[codomain]] $y$. For a morphism $f$, denote $f : x \rightarrow y$ to mean $f \in Hom _A (x,y)$. In [[enriched category|enriched categories]], the object, $Hom _A (x,y)$, is called the [[hom-object]].

In [[higher category theory]], a morphism is a [[cell|1-cell]] of 0-cells in [[n-category|n-categories]].


## Examples

A familiar example is the [[topos]] [[Set]] of sets and mappings; the objects are sets, and the morphisms are mappings, or [[functions]].

In [[Grp]], the locally-small category of [[group|groups]], and group homomorphisms; the objects are set-theoretical groups, and the morphisms are group homomorphisms.

In [[Top]], the locally-small category of [[topological space|topological spaces]], and [[continuous function|continuous functions]]; the objects are sets of topological structure, and the morphisms are continuous functions.

## Variations
Morphisms are notable for being rich in [[stuff, structures, and properties]]. This is an incomplete list of just some of those variations. Henceforth denote by $A$, a [[category]].

**Monomorphism**

A morphism $f \in hom _A (y,z)$, is a monomorphism, or is monic if it satisfies left-cancellation, as-in; for all morphisms $g, h \in hom _A (x,y)$, $f \circ g=f \circ h \Rightarrow g=h$. This is a generalisation of left-uniqueness in relations, injectivity in functions, and monomorphism in [[algebra]]. From strongest to weakest in properties:

* [[split monomorphism]]

* [[split monomorphism|absolute monomorphism]]

* [[effective monomorphism]]

* [[normal monomorphism]]

* [[regular monomorphism]]

* [[strict monomorphism]]

* [[strong monomorphism]]

* [[extremal monomorphism]]

* [[monomorphism]]

**Epimormphism**

A morphism $f \in hom _A (x,y)$, is an epimorphism, or epic, if it satisfies right-cancellation, as-in; for all morphisms $g, h \in hom _A (y,z)$, $g \circ f=h \circ f \Rightarrow g=h$. This is a generalisation of right-totality in relations, surjectivity in functions, and epimorphism in abstract algebra. From strongest to weakest in properties:

* [[split epimorphism]]

* [[split epimorphism|absolute epimorphism]]

* [[effective descent morphism]]

* [[descent morphism]]

* [[effective epimorphism]]

* [[normal epimorphism]]

* [[regular epimorphism]]

* [[strict epimorphism]]

* [[strong epimorphism]]

* [[extremal epimorphism]]

* [[epimorphism]]

**Epic, and Monic**

A morphism $f \in Hom _A (x,y)$, is a bimorphism, bimonomorphism, or is epic, and monic, if it satisfies left-cancellation, and right-cancellation. This is a generalisation of left-unique right-totality in relations, bijection in functions, and isomorphism in abstract algebra.

**Isomorphism**

A morphism, $f \in Hom _A (x,y)$, is an isomorphism, or is iso, if both it and its [[inverse]] morphism are epic, and monic. This is a generalisation of left-unique left-total right-unique right-totality in relations, bijection in functions, and isomorphism in abstract algebra.

**Note, list is still incomplete.**

## Related concepts

* [[object]]

* **morphism**, [[multimorphism]]

  * [[inverse morphism]]

  * [[adjoint morphism]]

  * [[heteromorphism]]

  * [[endomorphism]], [[automorphism]], [[monomorphism]], [[epimorphism]], [[isomorphism]]

* [[1-morphism]]

  [[horizontal morphism]], [[vertical morphism]]

* [[2-morphism]]

* [[3-morphism]]

* [[k-morphism]]




[[!redirects morphisms]]
[[!redirects Morphism]]
[[!redirects Morphisms]]