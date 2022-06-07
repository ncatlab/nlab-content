

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



## Contents ##
* table of contents
{:toc}

## Idea ##

The [[oidification]] of an [[H-space]]. 

## Definition ##

### Classically ###

A **H-spaceoid** is a [[unital magmoid]] [[internalization|internal to]] the [[classical homotopy category]] of [[topological spaces]] [[Ho(Top)]], or in the homotopy category $Ho(Top)_*$ of [[pointed topological spaces]],  which has a [[unit]] up to [[homotopy]]. 

### In homotopy type theory ###

In [[homotopy type theory]], a **H-spaceoid** is a [[type]] $A$ with

* For each $a,b:A$, a type $hom_A(a,b)$, whose elements are called **arrows** or **morphisms**.

* For each $a:A$, a morphism $1_a:hom_A(a,a)$, called the **identity morphism**.

* For each $a,b,c:A$, a functor
$$hom_A(b,c) \to hom_A(a,b) \to hom_A(a,c)$$
called composition, and denoted infix by $g \mapsto f \mapsto g \circ f$, or sometimes $gf$.

* For each $a,b:A$ and $f:hom_A(a,b)$, terms $p:f = 1_b \circ f$ and $q:f=f\circ 1_a$.

## See also ##

* [[H-space]]
* [[unital magmoid]]
* [[H-magmoid]]
* [[H-category]] (category object internal to a homotopy category)
* [[homotopy category]]

[[!redirects H-spaceoids]]