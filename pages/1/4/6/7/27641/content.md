

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Directed homotopy type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

The concept of [[composition]] in [[simplicial type theory]]. 

## Definition

Let $A$ be a type in [[simplicial type theory]], and let $\Delta^2$ denote the [[boundary]] of the [[2-simplex]] type. A **composite of morphisms** from $x:A$ through $y:A$ to $z:A$ is a [[record]] consisting of

* a function $f:\Delta^2 \to A$

* an identification $p_x:f(0, 0) = x$

* an identification $p_y:f(0, 1) = y$

* an identification $p_z:f(1, 1) = z$

The type of composites of morphisms $\mathrm{comp}_A(x, y, z)$ between $x:A$, $y:A$, and $z:A$ is then the respective [[record type]]. It is also given by the dependent sum type 

$$\sum_{f:\Delta^2 \to A} (f(0, 0) = x) \times (f(0, 1) = y) \times (f(1, 1) = z)$$

In a [[Segal type]] $A$, for all elements $x:A$, $y:A$, and $z:A$, from the [[Segal condition]] one can construct a [[composition]] operation on [[hom-types]] 

$$\lambda (g, f).g \circ f:\mathrm{hom}_A(y, z) \times \mathrm{hom}_A(x, y) \to \mathrm{hom}_A(x, z)$$

which by the uniqueness condition is automatically [[associative]] and [[unital]]. 

## Related concepts

* [[simplicial type theory]]

* [[hom-type]]

* [[span in simplicial type theory]]

* [[cospan in simplicial type theory]]

* [[pair of composable morphisms]]

[[!redirects composition of morphisms]]

[[!redirects composite of morphisms]]
[[!redirects composites of morphisms]]

[[!redirects type of composite of morphisms]]
[[!redirects types of composites of morphisms]]

[[!redirects composition in simplicial type theory]]

[[!redirects composition of morphisms in simplicial type theory]]

[[!redirects composite of morphisms in simplicial type theory]]
[[!redirects composites of morphisms in simplicial type theory]]

[[!redirects type of composite of morphisms in simplicial type theory]]
[[!redirects types of composites of morphisms in simplicial type theory]]