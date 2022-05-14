
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

The notion of a *semilattice object* is the generalization of that of *[[semilattice]]* as one passes from the ambient [[category of sets]] [[internalization|into]] more general ambient [[categories]] with suitable properties.


## Definition

In a [[symmetric monoidal category]] [[monoidal category with diagonals|with diagonals]] $(C, \otimes, I, \Delta_{(-)})$, a **semilattice object** is a [[commutative monoid object]] $(M, \mu, \eta)$ such that for every morphism $a:I \to M$, $\mu \circ \Delta_M \circ a = a$, where $\Delta_M$ is the [[diagonal morphism]] of $M$. 

## See also 

* [[commutative monoid object]]

* [[join-semilattice object]]

* [[meet-semilattice object]]

* [[semilattice]]

[[!redirects semilattice objects]]