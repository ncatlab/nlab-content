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

In [[simplicial type theory]], given a type $A$ and [[terms]] $x:A$ and $y:A$, a morphism $f:\mathrm{hom}_A(x, y)$ is an **isomorphism** if the [[span in simplicial type theory|span]] $(f, \mathrm{id}_x)$ has a [[left quotient in simplicial type theory|left quotient]] and the [[cospan in simplicial type theory|cospan]] $(\mathrm{id}_y, f)$ has a [[right quotient in simplicial type theory|right quotient]]. 

$$\mathrm{isIso}(f) \coloneqq \mathrm{leftQuotient}(f, \mathrm{id}_x) \times \mathrm{rightQuotient}(\mathrm{id}_y, f)$$

The type of isomorphisms is given by the [[dependent sum type]]

$$\mathrm{iso}_A(x, y) \coloneqq \sum_{:\mathrm{hom}_A(x, y)} \mathrm{isIso}(f)$$

We say that two elements $x:A$ and $y:A$ are **merely isomorphic** if [[existential quantifier|there merely exists]] an isomorphism between $x$ and $y$:

$$x \cong_A y \coloneqq \exists f:\mathrm{hom}_A(x, y).\mathrm{isIso}(f)$$

## Related concepts

* [[hom type]]

* [[univalent type]]

* [[Rezk type]]

* [[skeletal Segal type]]

* [[isomorphism]]

* [[equivalence in an (∞,1)-category]]

* [[span in simplicial type theory]]

* [[cospan in simplicial type theory]]

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