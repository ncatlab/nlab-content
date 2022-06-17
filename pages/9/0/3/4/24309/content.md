+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

In [[homotopy type theory]], given [[types]] $A$ and $B$, a [[function]] $f:A \to B$ is an __effective epimorphism__ if for all [[terms]] $b:B$ the [[fiber]] of $f$ over $b$ is [[inhabited]]. 

$$isEffectiveEpic(f) \coloneqq \prod_{b:B} \Vert fiber(f, b) \Vert$$

The type of effective epimorphisms between $A$ and $B$ is defined as 

$$EffectiveEpis(A, B) \coloneqq \sum_{f:A \to B} isEffectiveEpic(f)$$

## Examples ##

* The [[surjections]] $f:A \to B$ between two [[set]]s $A$ and $B$ are effective epimorphisms. 

## See also

* [[n-monomorphism]]
* [[effective epimorphism in an (infinity,1)-category]]