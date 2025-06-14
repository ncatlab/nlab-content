
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
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

The notion of an *idempotent monoid object* is the generalization of that of *[[idempotent monoid]]* as one passes from the ambient [[category of sets]] [[internalization|into]] more general ambient [[categories]] with suitable properties.

## Definition

In a [[monoidal category with diagonals]] $(C, \otimes, I, \Delta_{(-)})$, an **idempotent monoid object** is a [[monoid object]] $(M, \mu, \eta)$ such that for every morphism $a:I \to M$, $\mu \circ \Delta_M \circ a = a$, where $\Delta_M$ is the [[diagonal morphism]] of $M$. 

## See also 

* [[monoid object]]

* [[semilattice object]]

* [[idempotent monoid]]

[[!redirects idempotent monoid objects]]