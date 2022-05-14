
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

A version of a [[Boolean algebra]] without the preorder being an [[antisymmetric relation]], [[internal relation|internal]] to a [[finitely complete category]]. 

## Definition

In a [[finitely complete category]] $C$, a **Boolean prealgebra object** is a [[bicartesian closed preordered object]] $X$ with a function
$$\zeta:((* \to X) \times (* \to X)) \to (* \to R)$$ 
such that for all global elements $a:* \to X$ and $b:* \to X$, 

* $s \circ \zeta(a, b) = a \Rightarrow b$
* $t \circ \zeta(a, b) = (a \Rightarrow \bot) \vee b$ 

## See also 

* [[bicartesian closed preordered object]]

* [[Boolean algebra]]

[[!redirects Boolean prealgebra objects]]