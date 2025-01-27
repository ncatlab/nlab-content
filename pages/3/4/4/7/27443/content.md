
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Family fibration

* toc
{: toc}

## Definition

For a [[category]] $C$, its **family fibration** is the [[Grothendieck fibration]] $Fam(C) \to Set$, where

* An object of $Fam(C)$ is a set-indexed [[family]] of [[objects]] of $C$, say $(X_i)_{i\in I}$ where each $X_i\in Ob(C)$ for some set $I$.

* A morphism of $Fam(C)$ from $(X_i)_{i\in I}$ to $(Y_j)_{j\in J}$ consists of a [[function]] $u:I\to J$ along with a family of morphisms $(f_i : X_i \to Y_{u(i)})_{i\in I}$.

The functor $Fam(C) \to Set$ sends $(X_i)_{i\in I}$ to the set $I$, and a morphism as above to the function $u$.  This is a Grothendieck fibration, and its [[fiber]] over a set $I$ is the [[power]] category $C^I$.

## Remarks

* Concepts in the category theory of fibrations (or equivalently [[indexed categories]]) are generally defined so that when applied to family fibrations, they specialize to the corresponding notions in ordinary category theory.

* When $C=Set$, the family fibration is equivalent to the [[codomain fibration]] of $Set$.

[[!redirects family fibrations]]
[[!redirects families fibration]]
[[!redirects families fibrations]]