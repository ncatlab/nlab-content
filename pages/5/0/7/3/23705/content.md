
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

## Definition ##

A **braided monoidal dagger category** is a [[monoidal dagger category]] $(C, \otimes, \Iota)$ which is also a [[braided monoidal category]], in that: 

* for objects $A \in Ob(C)$ and $B \in Ob(C)$, there is a [[natural unitary isomorphism]] called the **braiding** of $A$ and $B$

$$\beta_{A,B}: A\otimes B \cong^\dagger B\otimes A$$

* all objects $D \in Ob(C)$, $E \in Ob(C)$, and $F \in Ob(C)$ satisfy the **first hexagon identity** 

$$\alpha_{E,F,D} \circ \beta_{D, E \otimes F} \circ \alpha_{D,E,F} = (id \otimes \beta_{D,F}) \circ \alpha_{E,D,F} \circ (\beta_{D, E} \otimes id)$$ 

* all objects $D \in Ob(C)$, $E \in Ob(C)$, and $F \in Ob(C)$ satisfy the **second hexagon identity** 

$$\alpha_{F,D,E}^{-1} \circ \beta_{D \otimes E, F} \circ \alpha^{-1}_{D,E,F} = (\beta_{D, F} \otimes id) \circ \alpha^{-1}_{D,F,E} \circ (id \otimes \beta_{E, F})$$ 

## Examples ##

* [[symmetric monoidal dagger category]]

* [[compact closed dagger category]]

## See also ##

* [[dagger category]]

* [[monoidal dagger category]]

* [[braided monoidal category]]


