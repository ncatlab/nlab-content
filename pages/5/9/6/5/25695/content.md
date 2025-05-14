
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

## Idea

The analogue of an [[anima]] in [[simplicial type theory]]. 

## Definition

In [[simplicial type theory]], a type $A$ is a **simplicially discrete type** if for all elements $x:A$ and $y:A$ there is an equivalence between the [[identity type]] $x =_A y$ and the [[hom type]] $\mathrm{hom}_A(x, y)$:

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

Every simplicially discrete type is a [[Segal type]], so these are also called **discrete Segal types**. 

## Properties

The simplicially discrete types are the types which are cohesively discrete: given a type $A$, $A$ is simplicially discrete if and only if the $\flat$-counit $\flat(-):\flat A \to A$ is an [[equivalence of types]].  

## Examples

The [[unit type]], the [[empty type]], the [[type of booleans]], the [[natural numbers type]], and the [[circle type]] are all simplicially discrete. 

## Categorical semantics

The [[categorical semantics]] of a simplicially discrete type is a [[groupoid object in an (infinity,1)-category|groupoid object]] in a [[locally cartesian closed (infinity,1)-category|locally cartesian closed $(\infty,1)$-category]] $\mathbf{H}$. 

## Related concepts

* [[hom type]]
* [[anima]]
* [[univalent type]]
* [[univalent groupoid]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

[[!redirects simplicially discrete type]]
[[!redirects simplicially discrete types]]

[[!redirects discrete Segal type]]
[[!redirects discrete Segal types]]