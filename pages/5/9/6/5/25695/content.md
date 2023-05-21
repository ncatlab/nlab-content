
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

In [[simplicial type theory]], a [[Segal type]] $A$ is a **discrete Segal type** if for all elements $x:A$ and $y:A$ there is an equivalence between the [[identity type]] $x =_A y$ and the [[hom type]] $\mathrm{hom}_A(x, y)$:

$$x:A, y:A \vdash \mathrm{disc}(x, y):\mathrm{isEquiv}(\mathrm{idToHom}(x, y))$$

where 

$$
  \mathrm{idToHom}(x, y)
  \;\colon\;
  (x =_A y) 
  \;
  \to 
  \;
  \mathrm{hom}_A(x, y)
$$

$$
  \mathrm{idToHom}(x, y)
  \big(
    \mathrm{refl}_A(x)
  \big) 
    \;\coloneqq\;
  \mathrm{id}_A(x)
$$

## Related concepts

* [[hom type]]
* [[Segal type]]
* [[Rezk type]]
* [[univalent groupoid]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

[[!redirects discrete Segal type]]
[[!redirects discrete Segal types]]