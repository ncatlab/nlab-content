
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category Theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The semantics of the [[circle type]] in (2,1)-category theory.

## Definition 

In a weak (2,1)-category $C$ with [[terminal object]] $*$, a **circle object** is an object $S^1$ in $C$ with a [[global element]] $\beta:* \to S^1$ and an [[equivalence]] $\lambda:\beta \cong \beta$ such that for every other object $A$ in $C$ with a [[global element]] $\beta_A:* \to A$ and an [[equivalence]] $\lambda_A:\beta_A \cong \beta_A$, there is a [[functor]] $f:S^1 \cong A$ and a functor $f^{'}:(\beta \cong \beta) \to (\beta_A \cong \beta_A)$ and [[equivalences]] $p:f \circ \beta \cong \beta_A$ and $q:f^{'} \circ \lambda \cong \lambda_A \circ f^{'}$ satisfying [[coherence laws]]. 

## Properties

The [[loop space object]] of the object $S^1$ with global element $\beta$ the circle object is equivalent to an [[integers object]] $Z$. 

## See also 

* [[circle type]]

* [[integers object]]