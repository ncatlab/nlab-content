
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Directed homotopy type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[simplicial type theory]], given a type $A$ and [[terms]] $x:A$ and $y:A$, a morphism $f:\mathrm{hom}_A(x, y)$ is an **isomorphism** if it comes with morphisms $g:\mathrm{hom}_A(y, x)$ and $h:\mathrm{hom}_A(y, x)$ such that the identity morphism $\mathrm{id}_x$ is the [[unique composite]] of $g$ and $f$ and the identity morphism $\mathrm{id}_y$ is the [[unique composite]] of $f$ and $g$ 

$$\mathrm{isIso}(f) \coloneqq \left(\sum_{g:\mathrm{hom}_A(y, x)} \mathrm{isUniqueComposite}(x, y, x, f, g, \mathrm{id}_x)\right) \times \left(\sum_{h:\mathrm{hom}_A(y, x)} \mathrm{isUniqueComposite}(y, x, y, h, f, \mathrm{id}_y)\right)$$

The type of all isomorphisms between $x$ and $y$ in $A$ is defined as 
$$\mathrm{iso}_A(x, y) \coloneqq \sum_{f:\mathrm{hom}_A(x, y)} \mathrm{isIso}(f)$$

We say that two elements $x:A$ and $y:A$ are **merely isomorphic** if [[existential quantifier|there merely exists]] an isomorphism between $x$ and $y$:

$$x \cong_A y \coloneqq \exists f:\mathrm{hom}_A(x, y).\mathrm{isIso}(f)$$

## Related concepts

* [[hom type]]

* [[univalent type]]

* [[Rezk type]]

* [[skeletal Segal type]]

* [[isomorphism]]

* [[equivalence in an (∞,1)-category]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

[[!redirects isomorphism in simplicial type theory]]
[[!redirects isomorphisms in simplicial type theory]]

[[!redirects type of isomorphism in simplicial type theory]]
[[!redirects type of isomorphisms in simplicial type theory]]

[[!redirects isomorphism in a Segal type]]
[[!redirects isomorphisms in a Segal type]]

[[!redirects type of isomorphisms in a Segal type]]
[[!redirects types of isomorphisms in a Segal type]]

[[!redirects isomorphism in a complete Segal type]]
[[!redirects isomorphisms in a complete Segal type]]

[[!redirects type of isomorphisms in a complete Segal type]]
[[!redirects types of isomorphisms in a complete Segal type]]

[[!redirects isomorphism in a Rezk type]]
[[!redirects isomorphisms in a Rezk type]]

[[!redirects type of isomorphisms in a Rezk type]]
[[!redirects types of isomorphisms in a Rezk type]]