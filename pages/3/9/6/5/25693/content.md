
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

In [[simplicial type theory]], a [[Segal type]] $A$ is a **Rezk type** if for all elements $x:A$ and $y:A$ there is an equivalence between the [[identity type]] $x =_A y$ and the [[type of isomorphisms in a Segal type]] $x \cong_A y$:

$$x:A, y:A \vdash \mathrm{RezkCond}(x, y):\mathrm{isEquiv}(\mathrm{idToIso}(x, y))$$

where 

$$\mathrm{idToIso}(x, y):(x =_A y) \to x \cong_A y$$
$$\mathrm{idToIso}(x, y)(\mathrm{refl}_A(x)) \coloneqq \mathrm{id}_A(x)$$

## Related concepts

* [[Segal type]]
* [[isomorphism in a Segal type]]
* [[univalent category]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$