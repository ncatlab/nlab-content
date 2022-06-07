[[!redirects H-categories]]
[[!redirects A3-spaceoid]]
[[!redirects A3-spaceoids]]

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

The [[oidification]] of an [[A3-space]]/[[H-monoid]], or equivalently, a [[category]] internal to $Ho(Top)_*$. 

## Definition ##

### Classically ###

A **H-category** or **A3-spaceoid** is a [[category]] [[internalization|internal to]] the [[classical homotopy category]] of [[topological spaces]] [[Ho(Top)]], or in the homotopy category $Ho(Top)_*$ of [[pointed topological spaces]]. 

### In homotopy type theory ###

In [[homotopy type theory]], a **H-category** or **A3-spaceoid** is a [[type]] $A$ with

* For each $a,b:A$, a type $hom_A(a,b)$, whose elements are called **arrows** or **morphisms**.

* For each $a:A$, a morphism $1_a:hom_A(a,a)$, called the **identity morphism**.

* For each $a,b,c:A$, a function
$$hom_A(b,c) \to hom_A(a,b) \to hom_A(a,c)$$
called composition, and denoted infix by $g \mapsto f \mapsto g \circ f$, or sometimes $gf$.

* For each $a,b:A$ and $f:hom_A(a,b)$, we have $f=1_b \circ f$ and $f=f\circ 1_a$.

* For each $a,b,c,d:A$, 
$$f:hom_A(a,b),\ g:hom_A(b,c),\ h:hom_A(c,d)$$ 
we have $h\circ (g\circ f)=(h\circ g)\circ f$.

## See also ##

* [[category]]
* [[H-spaceoid]]
* [[A3-space]]
* [[homotopy category]]