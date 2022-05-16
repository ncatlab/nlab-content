+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
#### Categorification
+-- {: .hide}
[[!include categorification - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A *braided monoidal groupoid* is a [[braided monoidal category]] whose underlying [[category]] happens to be a [[groupoid]] (hence all whose [[morphisms]] are [[isomorphisms]].)

Equivalently: A [[monoidal groupoid]] with [[braiding]] that satisfies the [[hexagon identities]], 

Equivalently: A [[1-type|1-truncated]] [[En-algebra|$E_2$-space]]. 

## Definitions

A **braided monoidal groupoid** is a [[monoidal groupoid]] $G$ with a [[natural isomorphism|natural]] [[unitary morphism]] $\beta_{A,B} : A \otimes B \cong^\dagger B \otimes A $ such that for all objects $A:G$, $B:G$, and $C:G$, 

$$\alpha_{B,C,A} \circ \beta_{A, B \otimes C} \circ \alpha_{A,B,C} = (id_B \otimes \beta_{A,C}) \circ \alpha_{B,A,C} \circ (\beta_{A,B}\otimes id_C)$$

and 

$$\alpha^{-1}_{C,A,B} \circ \beta_{A \otimes B, C} \circ \alpha^{-1}_{A,B,C} = (\beta_{A,C} \otimes id_B) \circ \alpha^{-1}_{A,C,B} \circ (id_A \otimes \beta_{B,C}$$

## See also

* [[commutative monoid]]
* [[En-algebra]]
* [[groupoid]]
* [[monoidal groupoid]]
* [[braided 2-group]]
* [[symmetric monoidal groupoid]]
* [[k-tuply monoidal n-groupoid]]
* [[braided monoidal category]]

[[!redirects braided monoidal groupoid]]
[[!redirects braided monoidal groupoids]]