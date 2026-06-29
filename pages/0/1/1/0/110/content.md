
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

The notion of _morphism_ in [[category theory]] is an abstraction of the notion of [[homomorphism]]. 

In a general [[category]], a morphism is an [[arrow]] between two [[objects]]. The word *[[map]]* is also sometimes used as a synonym.

## Definition

Given two objects in a (locally small) category, say $x$ and $y$, there is a set $hom(x,y)$, called a [[hom-set]], whose elements are morphisms from $x$ to $y$.  Given a morphism $f$ in this hom-set, we write $f:x \to y$ to indicate that it goes from $x$ to $y$.

More generally, a morphism is what goes between objects in any [[n-category]].


## Examples

The most familiar example is the category [[Set]], where the objects are sets and the morphisms are functions.  Here if $x$ and $y$ are sets, a morphism $f: x \to y$ is a function from $x$ to $y$.


## Variations
Morphisms are notable for being rich in [[stuff, structures, and properties]], and this is an incomplete list of just some of those variations. Henceforth set $A$, a [[category]].

**[[monomorphism]]**
A morphism $f \in hom _A (y,z)$, is a monomorphism if it satisfies left-cancellation, as-in; for all morphisms $g, h \in hom _A (x,y)$, $f \circ g=f \circ h \Rightarrow g=h$. This is a generalisation of left-uniqueness in relations, injectivity in functions, and monomorphisms in [[abstract algebra]]. From strongest to weakest:

* [[split monomorphism]]

* [[split monomorphism|absolute monomorphism]]

* [[effective monomorphism]]

* [[normal monomrophism]]

* [[regular monomorphism]]

* [[strict monomorphism]]

* [[strong monomorphism]]

* [[extremal monomorphism]]

* [[monomorphism]]

**[[epimorphism]]**
A morphism $f \in hom _A (x,y)$, is an epimorphism if it satisfies right-cancellation, as-in; for all morphisms $g, h \in hom _A (y,z)$, $g \circ f=h \circ f \Rightarrow g=h$. This is a generalisation of right-uniqueness in relations, surjectivity in functions, and epimorphisms in [[abstract algebra]]. From strongest to weakest:

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

**Note, list is incomplete.**

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