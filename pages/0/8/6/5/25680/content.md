

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[dependent type theory]], a [[hom type]] on a type $A$ is a [[dependent type]] $\mathrm{hom}_A(x, y)$ which models the [[hom spaces]] of [[(infinity,1)-category|$\infty$-categories]]. 

## Definition 

### In simplicial homotopy type theory

In [[simplicial homotopy type theory]], the hom type is defined as the [[extension type]]

$$\mathrm{hom}_A(x, y) \coloneqq \langle \Delta^1 \to A \vert_{[x,y]}^{\partial \Delta^1} \rangle$$

where $\Delta^1$ is the directed interval primitive $\mathbb{2}$ and $\partial \Delta^1$ is the [[boundary]] of $\Delta^1$. 

## Related concepts

* [[simplicial homotopy type theory]]
* [[directed homotopy type theory]]
* [[identity type]]
* [[function type]]
* [[directed univalence]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$