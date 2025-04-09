
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

## Idea

In [[simplicial type theory]], a *heterogeneous hom type* or *dependent hom type* is to a [[hom type]] in the same way that a [[heterogeneous identity type]] is to an [[identity type]]. 

## Definition

In [[simplicial type theory]], given a type $A$, elements $x:A$ and $y:A$, a function $f:\mathbb{I} \to A$, [[identifications]] $p_0:f(0) =_A x$ and $p_1:f(1) =_A y$ a type family $x:A \vdash B(x)$, and elements $u:B(x)$ and $v:B(y)$, the **heterogeneous hom-type** or **dependent hom-type** is defined as the [[dependent sum type]] 

$$\mathrm{hhom}_{t.B(t)}(x, y, f, p_0, p_1, u, v) \coloneqq \sum_{g:\prod_{i:\mathbb{I}} B(f(i))} (g(0) =_{t.B(t)}^{(f(0), x, p_0)} u) \times (g(1) =_{t.B(t)}^{(f(1), y, p_1)} v)$$ 

where the type $u =_{t.B(t)}^{(x, y, p)} v$ is the [[heterogeneous identity type]] over the type family $x:A \vdash B(x)$. 

The elements of heterogeneous hom-types are called **heterogeneous morphisms** or **dependent morphisms**. 

### Type theory with shapes formalism

In [[simplicial homotopy type theory]] in the [[type theory with shapes]] formalism, given a type $A$, elements $x:A$ and $y:A$, a type family $x:A \vdash B(x)$, elements $u:B(x)$ and $v:B(y)$, and a morphism $f:\mathrm{hom}_A(x, y)$ of a [[hom-type]], the heterogeneous hom type is defined as the [[dependent extension type]]

$$\mathrm{hhom}_{t.B(t)}(x, y, f, u, v) \coloneqq \left\langle\prod_{t:\mathbb{2}} C(f(t)) \vert_{[u,v]}^{\partial \Delta^1} \right\rangle$$
where $\mathbb{2}$ is the directed interval primitive, $\Delta^1$ is the $1$-simplex probe shape, and $\partial \Delta^1$ is its boundary.

## Related concepts

* [[simplicial homotopy type theory]]
* [[directed homotopy type theory]]
* [[heterogeneous identity type]]
* [[dependent function type]]
* [[directed univalence]]
* [[Segal type]], [[Rezk type]]
* [[covariant type family]]
* [[hom type]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

[[!redirects heterogeneous hom type]]
[[!redirects heterogeneous hom types]]
[[!redirects heterogeneous hom-type]]
[[!redirects heterogeneous hom-types]]

[[!redirects dependent hom type]]
[[!redirects dependent hom types]]
[[!redirects dependent hom-type]]
[[!redirects dependent hom-types]]

[[!redirects heterogeneous morphism]]
[[!redirects heterogeneous morphisms]]

[[!redirects dependent morphism]]
[[!redirects dependent morphisms]]