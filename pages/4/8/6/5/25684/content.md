

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[dependent type theories]] with more than one layer of type, function extension types are types which behave like [[function types]] except the [[domain]] is the outer layer  (or equivalent) of type rather than the normal layer of type. 

## Definition

### In type theory with shapes

In [[type theory with shapes]], there are three different layers - there are the cube layer and the tope layer, which is [[logic over type theory]] where the cubes are the types and the topes are the propositions in the logic over type theory, and finally there is the type layer, which is a [[dependent type theory]]. 

Shapes are formed in the usual set-builder notation in [[set theory]]: given a cube $I$ and a predicate tope $t:I \vdash \phi$, one could construct the shape $\{t:I \vert \phi\}$. A cofibration in two-level type theory is an inclusion of shapes, which means shapes $\{t:I \vert \phi\}$ and $\{t:I \vert \psi\}$ with a predicate $t:I \vert \phi \vdash \psi$. 

Formation rules for dependent extension types
$$\frac{\{t:I \vert \phi\} \; \mathrm{shape} \quad \{t:I \vert \psi\} \; \mathrm{shape} \quad t:I \vert \phi \vdash \psi \quad \Xi \vert \Phi \vdash \Gamma \; \mathrm{ctx} \quad \Xi \vert \Phi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi, t:I \vert \Phi, \phi \vert \Gamma \vdash a:A}{\Xi \vert \Phi \vert \Gamma \vdash \langle \{t:I \vert \psi\} \to A \vert_a^\phi \rangle \; \mathrm{type}}$$

## Related concepts

* [[dependent extension type]]
* [[function type]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

* Tesla Zhang, *Three non-cubical applications of extension types* ([arXiv:2311.05658](https://arxiv.org/abs/2311.05658))

[[!redirects extension type]]
[[!redirects extension types]]