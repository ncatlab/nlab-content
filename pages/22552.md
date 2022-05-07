
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorification
+-- {: .hide}
[[!include categorification - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Just as a [[groupoid]] is the [[oidification]] of a [[group]] and a [[ringoid]] is the oidification of a [[ring]], a [[magmoid]] should be the oidification of a [[magma]]. 

## Definition

### With a class of morphisms

Let $Q$ be a [[quiver]] with a class of objects $Ob(Q)$, a class of morphisms $Mor(Q)$, for every morphism $f\in Mor(Q)$ an object $s(f)\in Ob{Q}$ called the __source__ or __domain__ of $f$ and an object $t(f) \in Ob{Q}$ called the __target__ or __codomain__ of $f$. A __magmoid__ is a [[partial map|partial binary operation]] 

$$\left(-\right)\circ\left(-\right): Mor(Q) \times Mor(Q) \to Mor(Q) + 1$$ 

with coproduct injections $inj:Mor(Q) \to Mor(Q) + 1$ and $pt: 1 \to Mor(Q) + 1$, such that for $f, g \in Mor(Q)$, there is a function $h$ in the inverse image of $inj(h) = f \circ g$ if $s(f) = t(g)$, and $f \circ g = pt(\bullet)$ otherwise. 

### With a family of classes of morphisms

Let $Q$ be a [[quiver]] with a class of objects $Ob(Q)$ and for all objects $a, b \in Ob(Q)$, a class of morphisms $Mor(a,b)$. A __magmoid__ is a quiver $Q$ with a binary operation 

$$\left(-\right)\circ\left(-\right): Mor(b,c) \times Mor(a,b) \to Mor(a,c)$$ 

for all $a,b,c \in Ob(Q)$. 

## Examples

A [[magma]] is a magmoid with only one object. 

A [[semicategory]] is a magmoid where the binary operation is [[associative]], a [[category]] is a semicategory (hence magmoid) such that each object has an [[identity element|identity morphism]] and each morphism has [[unit law|a left unit and a right unit]] equal to an identity element, and a [[groupoid]] is a category (hence magmoid) where each morphism has an [[inverse element|inverse morphism]]. 

## Related concepts

* [[magma]]

* [[oidification]]

* [[magma category]]

[[!redirects magmoids]]