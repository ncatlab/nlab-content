+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
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

In type theory, a 1-truncated [[An-space|$A_4$-space]]. In category theory, a [[magmoidal groupoid with unit]] with an [[associator]] that satisfy the [[pentagon identities]] but no higher coherence laws for the unitors. 

## Definitions

### In type theory

In [[intensional type theory]] with [[function extensionality]], a [[groupoid]] is a [[n-truncated|1-truncated]] [[type]] and an **$A_4$-spatial groupoid** is a [[groupoid]] that is also an [[An-space|$A_4$-space]]. 

### In category theory

In [[category theory]], an **$A_4$-spatial groupoid** is a [[magmoidal groupoid with unit]] $(G, \otimes, I, \lambda_{(-)}, \rho_{(-)})$ with natural unitary ismorphisms $\alpha_{A, B, C} \colon A \otimes (B \otimes C) \simeq^\dagger (A \otimes B) \otimes C$ such that the [[pentagon identity]] is satisfied for all objects $A$, $B$, $C$, and $D$: 

$$\alpha_{A,B,C \otimes D} \circ \alpha_{A \otimes B, C, D} = (id_A \otimes \alpha_{B,C,D}) \circ \alpha_{A,B \otimes C, D} \circ (\alpha_{A,B,C} \otimes id_D)$$

## See also

* [[An-space]]
* [[groupoid]]
* [[H-monoidal groupoid]]
* [[monoidal groupoid]]

[[!redirects A4-spatial groupoid]]
[[!redirects A4-spatial groupoids]]