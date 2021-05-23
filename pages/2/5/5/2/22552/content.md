
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

### With a set of morphisms

Let $Q$ be a [[quiver]] with a collection of objects $Ob(Q)$, a set of morphisms $Mor(Q)$, a function $s: Mor(Q) \to Ob(Q)$ called the __source__ or __domain__ and a function $t: Mor(Q) \to Ob(Q)$ called the __target__ or __codomain__. A __magmoid__ is a quiver $Q$ with a [[partial map|partial binary operation]] 

$$\left(-\right)\circ\left(-\right): Mor(Q) \times Mor(Q) \to Mor(Q) + 1$$ 

with coproduct injections $inj:Mor(Q) \to Mor(Q) + 1$ and $pt: 1 \to Mor(Q) + 1$, such that for $f, g \in Mor(Q)$, there is a function $h$ in the inverse image of $inj(h) = f \circ g$ if $s(f) = t(g)$, and $f \circ g = pt(\bullet)$ otherwise. 

### With a family of sets of morphisms

Let $Q$ be a [[quiver]] with a collection of objects $Ob(Q)$ and a [[Set]]-valued functor $Mor: Ob(Q) \times Ob(Q) \to Set$ for all objects $a, b \in Ob(Q)$. A __magmoid__ is a quiver $Q$ with a binary operation 

$$\left(-\right)\circ\left(-\right): Mor(b,c) \times Mor(a,b) \to Mor(a,c)$$ 

for all $a,b,c \in Ob(Q)$. 

### Weak and strict magmoids

A __weak magmoid__ is a magmoid $Q$ whose collection of objects $Ob(Q)$ form a [[groupoid]], while a __strict magmoid__ is a magmoid $Q$ whose collection of objects $Ob(Q)$ form a [[set]]. 

### Enriched magmoids

Let $V$ be a [[monoidal category]] (or a [[monoidal (infinity,1)-category]]) and let $Q$ be a $V$-enriched [[quiver]], with a collection of objects $Ob(Q)$ and a $V$-valued functor $Mor: Ob(Q) \times Ob(Q) \to V$ for all objects $a, b \in Ob(Q)$. A __$V$-enriched magmoid__ is a $V$-enriched quiver $Q$ with a binary operation 

$$\left(-\right)\circ\left(-\right): Mor(b,c) \times Mor(a,b) \to Mor(a,c)$$ 

for all $a,b,c \in Ob(Q)$. 

### Unital magmoids

A __unital magmoid__ $Q$ is a magmoid where every object $a \in Ob(Q)$ has an [[identity morphism]] $id_a: a \to a$, such that for any morphism $f:a \to b$, $f \circ id_a = f$, and for any morphism $g:c \to a$, $id_a \circ g = g$. The hom-set of a unital magmoid with only one object is a __[[unital magma]]__. 

A unital magmoid is __invertible__ if for every pair of objects $a,b \in Ob(Q)$ and for every morphism $f:a \to b$, there exists an [[inverse morphism]] $g:b \to a$ such that $f \circ g = id_b$ and $g \circ f = id_a$. 

## Examples

A [[magma]] is a magmoid with only one object. 

A [[quasigroupoid]] is a magmoid. 

A [[semicategory]] is a magmoid where the binary operation is [[associative]], a [[category]] is a semicategory and a unital magmoid, and a [[groupoid]] is an invertible category. 

A [[transitive relation]] is a magmoid [[enriched category|enriched]] on [[truth values]], or a magmoid $M$ where thete is at most one morphism from every object $a$ to object $b$ in $M$

## Related concepts

* [[magma]]

* [[oidification]]

* [[magmoidal category]]

[[!redirects magmoids]]

[[!redirects unital magmoid]]
[[!redirects unital magmoids]]
[[!redirects invertible unital magmoid]]
[[!redirects invertible unital magmoids]]
[[!redirects invertible magmoid]]
[[!redirects invertible magmoids]]