
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

The analogue of a [[Rezk category]] or [[complete Segal space]] in [[simplicial type theory]]. 

## Definition

In [[simplicial type theory]], a **[[Rezk category|Rezk]] type** or **[[complete Segal space|complete Segal]] type** is a [[univalent type|univalent]] [[Segal type]]

$$\mathrm{isRezk}(A) \coloneqq \mathrm{isSegal}(A) \times \mathrm{isUnivalent}(A)$$ 

## Examples

Examples of Rezk types include the interval $\mathbb{I}$, the $n$-cubes $\mathrm{Fin}(n) \to \mathbb{I}$, and the $n$-simplices inductively defined by 
 
$$\Delta^0 \coloneqq \mathrm{Fin}(0) \to \mathbb{I}$$

$$n:\mathbb{N} \vdash \Delta^{n + 1} \coloneqq \sum_{t:\mathrm{Fin}(n + 1) \to \mathbb{I}} \prod_{i:\mathrm{Fin}(n)} t(\pi_1(i)) \leq t(\pi_1(i + 1))$$

## Categorical semantics

The categorical semantics of a complete Segal type is a [[complete Segal space object]] in a [[locally cartesian closed (infinity,1)-category|locally cartesian closed $(\infty,1)$-category]] $\mathbf{H}$. 

## Related concepts

* [[Segal type]]
* [[univalent type]]
* [[simplicially discrete type]]
* [[complete Segal space]]
* [[univalent category]]
* [[skeletal Segal type]]
* [[gaunt Segal type]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

[[!redirects Rezk type]]
[[!redirects Rezk types]]

[[!redirects complete Segal type]]
[[!redirects complete Segal types]]

[[!redirects univalent Segal type]]
[[!redirects univalent Segal types]]

[[!redirects saturated Segal type]]
[[!redirects saturated Segal types]]