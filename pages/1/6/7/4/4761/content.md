
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Bigroupoids
* table of contents
{: toc}

## Idea

A _bigroupoid_ is an [[algebraic definition of higher categories|algebraic model]] for (weak) [[2-groupoid]]s along the lines of a [[bicategory]].


## Definition

A __bigroupoid__ is a [[bicategory]] in which every [[morphism]] is an [[equivalence]] and every [[2-morphism]] is an [[isomorphism]].

More explicitly, a bigroupoid consists of:

*  A [[collection]] of __[[objects]]__ $x,y,z,\dots$, also called __$0$-cells__;
*  For each pair of $0$-cells $x,y$, a [[groupoid]] $B(x,y)$, whose objects are called __[[morphisms]]__ or __$1$-cells__ and whose morphisms are called __[[2-morphisms]]__ or __$2$-cells__;
*  For each $0$-cell $x$, a distinguished $1$-cell $1_x\colon B(x,x)$ called the __[[identity morphism]]__ or __identity $1$-cell__ at $x$;
*  For each triple of $0$-cells $x,y,z$, a [[functor]] ${\circ}\colon B(y,z) \times B(x,y) \to B(x,z)$ called __[[horizontal composition]]__;
*  For each pair of $0$-cells $x,y$, a functor ${-}^{-1}\colon B(y,x) \to B(x,y)$ called the __[[inverse morphism|inverse]]__ operation;
*  For each pair of $0$-cells $x,y$, two [[natural isomorphisms]] called __[[unitors]]__: $id_{B(x,y)} \circ const_{1_x} \cong id_{B(x,y)} \cong const_{1_y} \circ id_{B(x,y)}\colon B(x,y) \to B(x,y)$;
*  For each quadruple of $0$-cells $w,x,y,z$, a natural isomorphism called the __[[associator]]__ between the two functors from $B_{y,z} \times B_{x,y} \times B_{w,x}$ to $B_{w,z}$ built out of ${\circ}$; and
*  For each triple of $0$-cells $x,y,z$, two natural isomorphisms called the __[[unit of an adjunction|unit]]__ and __[[counit]]__ between the two composites of ${-}^{-1}$ and $id_{B(x,y)}$ and the constant functors on the relevant identity morphisms; such that
*  The unitors and associator satisfy the same axioms as the constraint isomorphisms in a [[monoidal category]] (which we do not write out in full here); and
*  The unit and counit satisfy the same axioms as the constraint isomorphisms in an [[adjunction]] (which we also do not write out in full here).


[[!redirects bigroupoid]]
[[!redirects bigroupoids]]
