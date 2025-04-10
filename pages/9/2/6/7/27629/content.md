
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

## Definition

In [[simplicial type theory]], a **univalent type** or **saturated type** is a type such that the canonical function which by the [[J rule]] takes an identification of elements $p:x =_A y$ to an isomorphism $J(\lambda t.\mathrm{id}_A(t), x, y, p):\mathrm{iso}_A(x, y)$ is an [[equivalence of types]] for all $x:A$ and $y:A$. 

$$\mathrm{isUnivalent}(A) \coloneqq \prod_{x:A} \prod_{y:A} \mathrm{isEquiv}(\lambda p.J(\lambda t.\mathrm{id}_A(t), x, y, p))$$ 

## Related concepts

* [[simplicial type theory]]
* [[isomorphism in a Segal type]]
* [[univalent category]]
* [[complete Segal space]]
* [[discrete Segal type]]

[[!redirects univalent type]]
[[!redirects univalent types]]

[[!redirects saturated type]]
[[!redirects saturated types]]