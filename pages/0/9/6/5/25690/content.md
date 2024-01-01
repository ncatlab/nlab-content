
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

## Idea

Segal types are the (infinity,1)-categorical version of [[precategories]] in [[simplicial type theory]]

## Definition

In [[simplicial type theory]], a **Segal type** is a type $A$ such that given elements $x:A$, $y:A$, and $z:A$ and morphisms $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(y, z)$, the type 
$$\sum_{h:\mathrm{hom}_A(x, z)} \left\langle \Delta^2 \to A \vert_{[x, y, z, f, g, h]}^{\partial \Delta^2} \right\rangle$$
is a [[contractible type]], where $\Delta^2$ is the $2$-simplex probe shape and $\partial \Delta^2$ is its boundary. 

## Related concepts

* [[hom type]]
* [[discrete Segal type]]
* [[Rezk type]]
* [[isomorphism in a Segal type]]
* [[Segal space]]
* [[op modality]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$