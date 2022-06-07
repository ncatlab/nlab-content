
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

The [[oidification]] of an "H-magma", which is to [[magmas]] what [[H-spaces]] are to [[unital magmas]]. 

## Definition ##

### Classically ###

A **H-magmoid** is a [[magmoid]] [[internalization|internal to]] the [[classical homotopy category]] of [[topological spaces]] [[Ho(Top)]], or in the homotopy category $Ho(Top)_*$ of [[pointed topological spaces]],  which has a [[unit]] up to [[homotopy]]. 

### In homotopy type theory ###

In [[homotopy type theory]], an H-magmoid $A$ consists of the following.

* A type $A_0$, whose elements are called objects. Typically $A$ is coerced to $A_0$ in order to write $x:A$ for $x:A_0$.

* For each $a,b:A$, a type $hom_A(a,b)$, whose elements are called **arrows** or **morphisms**.

* For each $a,b,c:A$, a function
$$hom_A(b,c) \to hom_A(a,b) \to hom_A(a,c)$$
called composition, and denoted infix by $g \mapsto f \mapsto g \circ f$, or sometimes $gf$.

## See also ##

* [[magmoid]]
* [[H-spaceoid]]
* [[H-category]] (category object internal to a homotopy category)
* [[homotopy category]]

[[!redirects H-magmoids]]
