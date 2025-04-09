
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

In [[simplicial type theory]], given a [[Segal type]] $A$ and [[terms]] $x \colon A$ and $y \colon A$, a "morphism" ([[term]] of [[hom type]]) $f \colon \mathrm{hom}_A(x, y)$ is an **isomorphism** if there exist morphisms $g:\mathrm{hom}_A(y, x)$ and $h:\mathrm{hom}_A(y, x)$ such that $g \circ f = \mathrm{id}_x$ and $f \circ h = \mathrm{id}_y$
$$\mathrm{isIso}(f) \coloneqq \left(\sum_{g:\mathrm{hom}_A(y, x)} g \circ f = \mathrm{id}_x\right) \times \left(\sum_{h:\mathrm{hom}_A(y, x)} f \circ h = \mathrm{id}_y\right)$$

The type of all isomorphisms between $x$ and $y$ in $A$ is defined as 
$$
  \big(x \cong_A y\big) 
   \;\;\coloneqq\;\; 
  \sum_{
    \mathclap{
      f \colon \mathrm{hom}_A(x, y)  
    }
  } 
  \mathrm{isIso}(f)
$$

We say that two elements $x:A$ and $y:A$ are **merely isomorphic** if [[existential quantifier|there merely exists]] an isomorphism between $x$ and $y$:

$$\mathrm{isMerelyIso}(x, y) \coloneqq \exists f:\mathrm{hom}_A(x, y).\mathrm{isIso}(f)$$

## Related concepts

* [[hom type]]

* [[Segal type]]

* [[Rezk type]]

* [[skeletal Segal type]]

* [[isomorphism]]

* [[equivalence in an (∞,1)-category]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

[[!redirects isomorphism in a Segal type]]
[[!redirects isomorphisms in a Segal type]]

[[!redirects type of isomorphisms in a Segal type]]