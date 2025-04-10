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

There are many possible definitions of an isomorphism in [[simplicial type theory]]. 

### Bi-invertible morphisms

In [[simplicial type theory]], given a type $A$ and [[terms]] $x:A$ and $y:A$, a morphism $f:\mathrm{hom}_A(x, y)$ is a **bi-invertible morphism** if the [[span in simplicial type theory|span]] $(f, \mathrm{id}_x)$ has a [[left quotient in simplicial type theory|left quotient]] and the [[cospan in simplicial type theory|cospan]] $(\mathrm{id}_y, f)$ has a [[right quotient in simplicial type theory|right quotient]]. 

$$\mathrm{isIso}(f) \coloneqq \mathrm{leftQuotient}(f, \mathrm{id}_x) \times \mathrm{rightQuotient}(\mathrm{id}_y, f)$$

### Merely quasi-invertible morphisms

In [[simplicial type theory]], given a type $A$ and [[terms]] $x:A$ and $y:A$, a morphism $f:\mathrm{hom}_A(x, y)$ is a **quasi-invertible morphism** if one can construct a morphism $g:\mathrm{hom}_A(y, x)$ called a **quasi-inverse** such that $\mathrm{id}_x$ is the [[unique composite]] of $f$ and $g$ and $\mathrm{id}_y$ is the [[unique composite]] of $g$ and $f$. 

$$\mathrm{quasiInverses}(f) \coloneqq \sum_{g:\mathrm{hom}_A(y, x)} \mathrm{isUniqueComposite}(f, g, \mathrm{id}_x) \times \mathrm{isUniqueComposite}(g, f, \mathrm{id}_y)$$

A morphism $f:\mathrm{hom}_A(x, y)$ is a **merely quasi-invertible morphism** if [[there merely exists]] $g:\mathrm{hom}_A(y, x)$ such that $\mathrm{id}_x$ is the [[unique composite]] of $f$ and $g$ and $\mathrm{id}_y$ is the [[unique composite]] of $g$ and $f$. 

$$\mathrm{isIso}(f) \coloneqq \exists g:\mathrm{hom}_A(y, x).\mathrm{isUniqueComposite}(f, g, \mathrm{id}_x) \times \mathrm{isUniqueComposite}(g, f, \mathrm{id}_y)$$

If $A$ is a [[Segal type]], this is equivalent to the usual definition of a merely quasi-invertible morphism

$$\mathrm{isIso}(f) \coloneqq \exists g:\mathrm{hom}_A(y, x).(g \circ f = \mathrm{id}_x) \times (f \circ g = \mathrm{id}_y)$$

### Equivalence of definitions

These definitions of an isomorphism are equivalent for [[Segal types]]. It is unknown whether the definitions are still equivalent for types which are not Segal, and if not, which notion of isomorphism is the right notion for non-Segal types. 

## Type of isomorphisms

The type of isomorphisms is given by the [[dependent sum type]]

$$\mathrm{iso}_A(x, y) \coloneqq \sum_{:\mathrm{hom}_A(x, y)} \mathrm{isIso}(f)$$

We say that two elements $x:A$ and $y:A$ are **merely isomorphic** if [[existential quantifier|there merely exists]] an isomorphism between $x$ and $y$:

$$x \cong_A y \coloneqq \exists f:\mathrm{hom}_A(x, y).\mathrm{isIso}(f)$$

## Related concepts

* [[hom type]]

* [[univalent type]]

* [[Rezk type]]

* [[skeletal type]]

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